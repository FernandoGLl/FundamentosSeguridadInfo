#### Description

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/ab5453de03105a8aab9c68b0b46e66a4fe0a781c3915ab519f7fab31b3ce6894/whitepages.txt) is all blank!

**Solución**

```
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)

print(data)

-----------------------------------------------------------------------------------


Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 exp.py
b'\npicoCTF\n\nSEE PUBLIC RECORDS & BACKGROUND REPORT\n5000 Forbes Ave, Pittsburgh, PA 15213\npicoCTF{not_all_spaces_are_created_equal_bbc4f54c75763bd78dc840f05eb7a752}\n'

```

**Notas adicionales**

Se realizo lo siguiente:

- **Detectar** patrones de espacios diferentes.
- **Mapear** un tipo de espacio a `0` y el otro a `1`.
- **Interpretar** esa secuencia binaria como texto real

**Referencia**

- https://en.wikipedia.org/wiki/Unicode
- https://en.wikipedia.org/wiki/UTF-8
- https://www.compart.com/en/unicode/category/Zs