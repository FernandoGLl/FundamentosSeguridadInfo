#### Description

How to automate tasks to run at intervals on linux servers?

Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 64398
Username: picoplayer 
Password: ENAFb6zfzn
```

**Solución**
```

Fercho@MSI:/mnt/c/Users/ferga/downloads$ ssh -p 64398 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:64398 ([13.59.203.175]:64398)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yeas
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[saturn.picoctf.net]:64398' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password:
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1044-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed

```

Notas adicionales

- El comando cat /etc/crontab  se utiliza para  mostrar las tareas programadas para todo el sistema, junto con comentarios que explican el formato del archivo.

Referencias

https://www.sysadmit.com/2023/05/linux-resolver-errores-en-cron.html