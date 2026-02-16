#### Description

Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 fixme2.py
  File "/mnt/c/Users/ferga/downloads/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano fixme2.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 fixme2.py
  File "/mnt/c/Users/ferga/downloads/fixme2.py", line 22
    if flag = " ":
       ^^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano fixme2.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

**Notas adicionales**

Se resolvió solo añadiendo == en la linea 22

**Referenicas**

