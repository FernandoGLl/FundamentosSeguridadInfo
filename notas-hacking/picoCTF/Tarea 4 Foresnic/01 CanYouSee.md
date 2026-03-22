#### Description

How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).

**Solución**

picoCTF{ME74D47A_HIDD3N_4dabddcb}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://artifacts.picoctf.net/c_titan/5/unknown.zip
--2026-03-22 13:40:53--  https://artifacts.picoctf.net/c_titan/5/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.64, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252228 (2.1M) [application/octet-stream]
Saving to: ‘unknown.zip’

unknown.zip                   100%[=================================================>]   2.15M  7.46MB/s    in 0.3s

2026-03-22 13:40:53 (7.46 MB/s) - ‘unknown.zip’ saved [2252228/2252228]

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ unzip unknown.zip
Archive:  unknown.zip
  inflating: ukn_reality.jpg
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ exiftool ukn_reality.jpg
ExifTool Version Number         : 12.76
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:15 16:40:17-06:00
File Access Date/Time           : 2026:03:22 13:41:00-06:00
File Inode Change Date/Time     : 2026:03:22 13:41:00-06:00
File Permissions                : -rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==" | base64 -d
picoCTF{ME74D47A_HIDD3N_4dabddcb}
fergll@FerGLl:/mnt/c/Users/ferch/Documents$

```

- **Recuperación del archivo:** Primero extrajimos el archivo `.zip` correcto para obtener la imagen `ukn_reality.jpg`.
    
- **Análisis de Metadata:** En lugar de mirar la foto, usamos la herramienta `exiftool` para inspeccionar su **metadata** . Estos son los "datos sobre los datos" (como el autor, la resolución o el software usado) que se guardan de forma invisible en el código del archivo.
    
- **Búsqueda de la anomalía:** Al leer esa información técnica, buscamos un campo que contuviera una cadena de texto extraña o fuera de lugar en lugar de los datos normales de una fotografía.
    
- **Decodificación Base64:** Esa cadena sospechosa estaba codificada en Base64. Usamos el comando `base64 -d` en la terminal para traducirla a texto normal, revelando por fin la bandera `picoCTF{...}`.

**Referencias**



 