#### Description

Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

**Solucion**
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 level1.py
Please enter correct password for flag: 1
That password is incorrect
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano level1.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano level1.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}

**Notas adicionales**

- Se utilizo la función nano para abrir el archivo level1.py
- En el archivo .py se busco la linea donde se estaba declarando la contraseña. 
**Referencias**


