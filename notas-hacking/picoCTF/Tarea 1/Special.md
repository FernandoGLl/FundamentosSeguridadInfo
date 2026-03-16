#### Description

Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM) 
Start your instance to see connection details. 
`ssh -p 61444 ctf-player@saturn.picoctf.net` 
The password is `483e80d4`

**Solución**

```
Fercho@MSI:/mnt/c/Users/ferga$ ssh -p 61444 ctf-player@saturn.picoctf.net
ctf-player@saturn.picoctf.net's password:
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Fri Feb 20 00:13:00 2026 from 127.0.0.1
Special$ find .
Find .
sh: 1: Find: not found
Special$ Clear & found .
Clear & found .
sh: 1: found: not found
sh: 1: Clear: not found
Special$ Clear & find .
Clear & find .
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```

**Notas adicionales**

- El comando "find ."  es una de las herramientas mas fuertes en Linux, al estar acompañado por un punto le indica que debe de buscar en el directorio actual y en todas las subcarpetas.


**Referencias**

https://superuser.com/questions/1827027/find-and-delete-files-with-linux-command-line
