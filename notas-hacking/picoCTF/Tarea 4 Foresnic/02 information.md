#### Description

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)

**Solución**

picoCTF{the_m3tadata_1s_modified}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg
--2026-03-22 13:49:45--  https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.161.44.103, 3.161.44.61, 3.161.44.84, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.161.44.103|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: ‘cat.jpg’

cat.jpg                       100%[=================================================>] 857.55K  3.55MB/s    in 0.2s

2026-03-22 13:49:46 (3.55 MB/s) - ‘cat.jpg’ saved [878136/878136]

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ exiftool cat.jpg
ExifTool Version Number         : 12.76
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2025:12:12 13:21:14-06:00
File Access Date/Time           : 2026:03:22 13:49:46-06:00
File Inode Change Date/Time     : 2026:03:22 13:49:45-06:00
File Permissions                : -rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
picoCTF{the_m3tadata_1s_modified}fergll@FerGLl:/mnt/c/Users/ferch/Documents$

```

- **Descarga del archivo:** Primero, bajamos la imagen `cat.jpg` proporcionada por el reto.
    
- **Análisis de Metadata:** Siguiendo la pista de "mirar los detalles", usamos nuevamente la herramienta `exiftool` en la terminal para inspeccionar los datos internos (Exif) de la fotografía.
    
- **Búsqueda de la anomalía:** Revisamos la salida del comando y localizamos un campo de texto (usualmente el de **License**) que en lugar de tener información normal de derechos de autor, contenía una cadena de texto larga y extraña.
    
- **Decodificación Base64:** Identificamos que esa cadena estaba ofuscada usando codificación Base64. Al pasarla por el comando `base64 -d`, el texto se tradujo y reveló la bandera final.

**Referencias**
