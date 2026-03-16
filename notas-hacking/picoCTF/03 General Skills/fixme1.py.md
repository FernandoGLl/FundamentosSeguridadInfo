#### Description

Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

**Solucion**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 fixme1.py
  File "/mnt/c/Users/ferga/downloads/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano fixme1.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano fixme1.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano fixme1.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}

import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + >

flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)

**Notas adicionales**

- Se resolvió el ejercicio siguiendo una de las pistas que decía que en Python es muy importante la identacion. 

**Referencias**

