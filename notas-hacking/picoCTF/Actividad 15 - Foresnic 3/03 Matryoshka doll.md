#### Description

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/b236ead0cb75e5a4b8b8d5aa15c6cc80369b3ea778f1a116911f23d774a92bf4/dolls.jpg)

**Solución**

```

fergll@FerGLl:/mnt/c/Users/ferch/documents/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v1.0 to extract, compressed size: 42, uncompressed size: 42, name: flag.txt
79764         0x13794         End of Zip archive, footer length: 22

fergll@FerGLl:/mnt/c/Users/ferch/documents/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
fergll@FerGLl:/mnt/c/Users/ferch/documents/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt
picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}

```

- picoCTF{LL9lb1dR4QbGe4l4iWCvGq9pdtwt7392}

**Notas adicionales**

- Lo que se realizao fue un "analisis forence" de las capas de una imagen, que en realidad eran multiples archivos ZIP.
- Se insyalo la herramienta binwalk es una herramienta para analizar archivos binarios y código ejecutable.
- Luego de esto fuimos abriendo las capas con los sigueintes comandos:
```

binwalk -e dolls.jpg
cd _dolls.jpg.extracted/base_images/
binwalk -e 2_c.jpg
cd _2_c.jpg.extracted/base_images/
binwalk -e 3_c.jpg
cd _3_c.jpg.extracted/base_images/
binwalk -e 4_c.jpg
cd _4_c.jpg.extracted/
cat flag.txt

```

**Referencias**
- https://www-kali-org.translate.goog/tools/binwalk/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc