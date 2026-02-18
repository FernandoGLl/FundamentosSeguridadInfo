#### Description

Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)

**Solución**

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ unzip challenge.zip
Archive:  challenge.zip
replace drop-in/message.py? [y]es, [n]o, [A]ll, [N]one, [r]ename: A

Archivo descomprimido 

Fercho@MSI:/mnt/c/Users/ferga/downloads$ cd drop-in
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ strings .git/objects/pack/*.pack | grep "picoCTF{"
strings: '.git/objects/pack/*.pack': No such file
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ grep -ra "picoCTF{" .git/
.git/logs/HEAD:c9e851509190f5887e91339ee18087e3e77ebfda 0351e0474493168ca76441c24630c17554fd09ca picoCTF{@sk_th3_1nt3rn_d2d29f22} <ops@picoctf.com> 1710202021 +0000  commit: optimize file size of prod code
.git/logs/refs/heads/master:c9e851509190f5887e91339ee18087e3e77ebfda 0351e0474493168ca76441c24630c17554fd09ca picoCTF{@sk_th3_1nt3rn_d2d29f22} <ops@picoctf.com> 1710202021 +0000     commit: optimize file size of prod code

```

**Notas Adicionales**

- Primero se descarga el archivo de la actividad.
- Luego de esto descomprimimos y esperamos a que se termine este proceso.
- Una vez descomprimido buscamos la bandera con el comando  grep -ra "picoCTF{" .git/

**Referencias**

