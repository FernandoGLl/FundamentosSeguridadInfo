#### Description

Find the flag in this [picture](https://challenge-files.picoctf.net/c_fickle_tempest/010f805d3d59e58913240f26904349f886a0ee71c205d46185ada895377818af/pico_img.png).

---

**Solución**

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ exiftool pico_img.png
ExifTool Version Number         : 13.25
File Name                       : pico_img.png
Directory                       : .
File Size                       : 109 kB
File Modification Date/Time     : 2026:03:08 13:03:56-06:00
File Access Date/Time           : 2026:03:08 13:03:58-06:00
File Inode Change Date/Time     : 2026:03:08 13:03:56-06:00
File Permissions                : -rwxrwxrwx
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Artist                          : picoCTF{s0_m3ta_19ebefe2}
Image Size                      : 600x600
Megapixels                      : 0.360

```

**Notas adicionales**

-  ExifTool en Linux es una potente herramienta de línea de comandos basada en Perl para leer, escribir y editar metadatos (EXIF, IPTC, XMP, GPS, etc.) en imágenes, audio, video y PDFs.


**Referencias**

- https://www-geeksforgeeks-org.translate.goog/linux-unix/installing-and-using-exiftool-on-linux/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc&_x_tr_hist=true

