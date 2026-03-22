#### Description

I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/3/challenge.zip)

The same files are accessible via SSH here: `ssh -p 53656 ctf-player@atlas.picoctf.net` Using the password `6dd28e9b`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

**Solución**

picoCTF{p33k_@_b00_a81f0a35}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ unzip challenge.zip
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
 extracting: home/ctf-player/drop-in/flag.png
 
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ zbarimg home/ctf-player/drop-in/flag.png
QR-Code:picoCTF{p33k_@_b00_a81f0a35}
scanned 1 barcode symbols from 1 images in 0 seconds

```

- **Navegación:** Identificamos que la imagen no estaba suelta, sino guardada dentro de una ruta de carpetas anidadas (`home/ctf-player/drop-in/flag.png`).
    
- **Decodificación:** Al ser literalmente un código QR, el reto se resolvió escaneando la imagen (ya sea usando la herramienta de terminal `zbarimg` o de forma gráfica con la cámara de un celular) para traducir el código a texto y obtener la bandera `picoCTF{...}`.

**Referencias**
- 