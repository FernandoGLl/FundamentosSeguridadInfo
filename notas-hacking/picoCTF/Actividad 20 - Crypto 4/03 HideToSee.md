#### Description

How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/240/atbash.jpg).

**Solución** 

picoCTF{atbash_crack_ca00558b}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://artifacts.picoctf.net/c/240/atbash.jpg
--2026-04-21 21:39:37--  https://artifacts.picoctf.net/c/240/atbash.jpg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 51508 (50K) [application/octet-stream]
Saving to: ‘atbash.jpg’

atbash.jpg                    100%[=================================================>]  50.30K  --.-KB/s    in 0.05s

2026-04-21 21:39:37 (976 KB/s) - ‘atbash.jpg’ saved [51508/51508]

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ steghide extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_xz00558y}
fergll@FerGLl:/mnt/c/Users/ferch/Documents$


```


- Se utilizo la herramienta `steghide`, que nos ayuda a extraer información oculta dentro de imágenes.
- Luego de esto al usar esta herramienta, nos genera un documento donde podemos encontrar la bandera en formato atbash.
- Por lo tanto utilizamos Cyberchef para decodificar la bandera. 

**Referencias**

- https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfeHowMDU1OHl9&oeol=FF
