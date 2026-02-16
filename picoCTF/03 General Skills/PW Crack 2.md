#### Description

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano level2.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}

**Notas adicionales**

- Se utilizo la función nano para abrir el archivo level1.py
- En el archivo .py se busco la linea donde se estaba declarando la contraseña. 
-  Dentro del archivo la contraseña venia en formato hexadecimal por lo tanto se decodifico y se obtuvo la contraseña con ayuda de la pagina CybeyChef.
- Cyberchef es una pagina que me permite decodificar en diferentes formatos.

**Referencias**
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=MHgzNCArIDB4NjUgKyAweDYzICsgMHgzOQ&oeol=FF
