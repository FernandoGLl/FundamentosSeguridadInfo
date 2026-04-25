#### Description

We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

**Solución** 

picoCTF{C7r1F_54V35_71M3}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ tar -xvf leak.tar
leak/
leak/passwords.txt
leak/usernames.txt
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cd leak
fergll@FerGLl:/mnt/c/Users/ferch/Documents/leak$ grep -n "cultiris" usernames.txt
378:cultiris
fergll@FerGLl:/mnt/c/Users/ferch/Documents/leak$ sed -n '378p' passwords.txt
cvpbPGS{P7e1S_54I35_71Z3}

picoCTF{C7r1F_54V35_71M3}

```

- Se entiende que la línea donde está el usuario en `usernames.txt` es la misma línea de su contraseña en `passwords.txt`.
- Se localiza el número de línea exacto del usuario objetivo (`cultiris`).
- Se saca el texto cifrado de esa misma línea en el archivo de contraseñas.
- Se reconoce el formato cifrado como **ROT13** (un cifrado César clásico) y se revierte el desplazamiento de letras para obtener la _flag_ final.
- Se utilizo la herramienta cyberchef para decodificar la bandera.
- El comando `378p` junto con `-n` le indica a la terminal: _"Ignora todo el archivo, solo imprime (p) en pantalla el contenido de la línea 378"_.

**Referencias**

- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tQN2UxU181NEkzNV83MVozfQ

