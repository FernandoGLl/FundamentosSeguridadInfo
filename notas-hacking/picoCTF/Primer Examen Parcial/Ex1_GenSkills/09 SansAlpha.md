#### Description

The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
`ssh -p 59612 ctf-player@mimas.picoctf.net` 
Use password: `83dcefb7`

Solución

picoCTF{7h15_mu171v3r53_15_m4dn355_36a674c0}

Notas adicionales 

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ ssh -p 59612 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:59612 ([52.15.88.75]:59612)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[mimas.picoctf.net]:59612' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password:
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

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

SansAlpha$ /???/???[!_]64 /????/??????????/??????/????????
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV8zNmE2NzRjMH0=

```

- Se uso cyberchef para decodificar el resultado https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y21WMGRYSnVJREFnY0dsamIwTlVSbnMzYURFMVgyMTFNVGN4ZGpOeU5UTmZNVFZmYlRSa2JqTTFOVjh6Tm1FMk56UmpNSDA&oeol=FF


Referencias

- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y21WMGRYSnVJREFnY0dsamIwTlVSbnMzYURFMVgyMTFNVGN4ZGpOeU5UTmZNVFZmYlRSa2JqTTFOVjh6Tm1FMk56UmpNSDA&oeol=FF
