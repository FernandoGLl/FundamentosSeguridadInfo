#### Description

What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/162/challenge.zip)

**Solución**

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ unzip challenge.zip
Fercho@MSI:/mnt/c/Users/ferga/downloads$ cd drop-in
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git log
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$
```

**Notas adicionales** 

- Una vez descomprimido el archivo se busco lo que el autor había borrado con el comando git log, con este podemos regresar a un punto de guardado donde el archivo si estaba.

**Notas Adicionales**

https://primer.picoctf.org/#_git_version_control

