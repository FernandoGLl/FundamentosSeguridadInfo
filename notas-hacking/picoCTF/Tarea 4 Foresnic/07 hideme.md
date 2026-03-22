#### Description

Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/257/flag.png).

**Solución**

picoCTF{Hiddinng_An_imag3_within_@n_ima9e_dc2ab58f}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png
42998         0xA7F6          End of Zip archive, footer length: 22

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2959, uncompressed size: 3108, name: secret/flag.png
42998         0xA7F6          End of Zip archive, footer length: 22

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cd _flag.png.extracted
fergll@FerGLl:/mnt/c/Users/ferch/Documents/_flag.png.extracted$ cd secret
fergll@FerGLl:/mnt/c/Users/ferch/Documents/_flag.png.extracted/secret$ explorer.exe .

```

- **Análisis:** Al escanearla con `binwalk`, descubrimos que no era solo una foto, sino que tenía un archivo comprimido oculto en su código.
    
- **Extracción:** Usamos `binwalk -e flag.png` para forzar la separación y extraer automáticamente ese archivo escondido.
    
- **Navegación:** Entramos a la carpeta generada por la herramienta (recordando que siempre empiezan con un guion bajo `_flag.png.extracted`).
    
- **Resultado:** Dentro de la carpeta `secret`, abrimos la imagen oculta que contenía escrita la bandera `picoCTF{...}`.

**Referencia