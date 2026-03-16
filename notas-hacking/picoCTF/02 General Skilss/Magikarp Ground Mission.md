#### Description

Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `61140`.

Solucion

ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat lof3.flag.txt
cat: lof3.flag.txt: No such file or directory
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  boot       dev  home                      lib    media  opt   root  sbin  sys  usr
bin            challenge  etc  instructions-to-3of3.txt  lib64  mnt    proc  run   srv   tmp  var
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_//4t3r_
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt
0b24fc4f}ctf-player@pico-chall$ Connection to wily-courier.picoctf.net closed by remote host.
Connection to wily-courier.picoctf.net closed.

picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}

Notas adicionales
Se intalo la paqueteria build-essential para poder utilizar el comando ssh
luego se entro al servidor y despues se fureon abriendo las carpetas y leyendo los archivos para ir pbteniendo las 3 partes de la bandera.

Referencias

https://www.hostinger.com/mx/tutoriales/como-configurar-claves-ssh?utm_campaign=Generic-Tutorials-DSA-t3|NT:Se|LO:MX&utm_medium=ppc&gad_source=1&gad_campaignid=17999056699&gclid=Cj0KCQiAy6vMBhDCARIsAK8rOgnv34hdq0d_YanNZyMGPRutmCAGfKRRKE74sgxLNfHiYiB3aaK55rQaAhPUEALw_wcB
