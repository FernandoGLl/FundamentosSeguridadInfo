#### Description

I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/139/challenge.zip)

**Solución** 

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ unzip challenge
Fercho@MSI:/mnt/c/Users/ferga/downloads$ cd drop-in
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git log
commit 144fdc44b09058d7ea7f224121dfa5babadddbb9 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    remove sensitive info

commit 7d3aa557ff7ba7d116badaf5307761efb3622249
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:25 2024 +0000

    create flag
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git show HEAD~1:message.txt
picoCTF{s@n1t1z3_be3dd3da}
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$

```


**Notas adicionales**

- Una vez descomprimido el archivo se busco lo que el autor había borrado con el comando git log, con este podemos regresar a un punto de guardado donde el archivo si estaba
- Luego de esto usamos el comando git show que se usa para detallar informacion y cambios de varios Git.
- HEAD~1 se refiere al commit antes del actual.


**Referencias**
https://primer.picoctf.org/#_git_version_control
https://www.youtube.com/watch?v=a60XqbxQEbg&t=438s

