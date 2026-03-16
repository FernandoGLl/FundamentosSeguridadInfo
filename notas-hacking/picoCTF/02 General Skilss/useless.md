#### Description

There's an interesting script in the user's home directory
The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     50175
Username: picoplayer
Password: password
```

Solucion

Fercho@MSI:/mnt/c/Users/ferga/downloads$ ssh picoplayer@saturn.picoctf.net -p 50175
The authenticity of host '[saturn.picoctf.net]:50175 ([13.59.203.175]:50175)' can't be established.
ED25519 key fingerprint is SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:50175' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password:
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ man useless

useless
     useless, — This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_8504}

Notas adicionales

el comando man es para leer el manual de cualquier programa en Linux.
se usa useless para encontrar lo "mas" útil dentro del manual. 

Referencias

https://www.hostinger.com/mx/tutoriales/como-configurar-claves-ssh?utm_campaign=Generic-Tutorials-DSA-t3|NT:Se|LO:MX&utm_medium=ppc&gad_source=1&gad_campaignid=17999056699&gclid=Cj0KCQiA7rDMBhCjARIsAGDBuEDPHAq8p6_Dbp1c1s74Yu7qAUB8ushAFTUeaumRuOLG9Bmi6Ls9Ny8aAgibEALw_wcB

https://man.cx/man(1)/es


