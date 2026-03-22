#### Description

🥛 http://wily-courier.picoctf.net:60195/

**Solución** 

"picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg concat_v.png
imagedata           .. text: "\n\n\n\n\n\n\t\t"
chunk:0:IHDR        .. file: Adobe Photoshop Color swatch, version 0, 1280 colors; 1st RGB space (0), w 0xb9a0, x 0x802, y 0, z 0; 2nd HSB space (1), w 0, x 0, y 0, z 0
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"
b1,bgr,lsb,xy       .. <wbStego size=0x941a5b ext=nil data="\xB6\xAD\xB6}\xDB\xB2lR\x7F\xDF\x86\xB7c\xFC\xFF\xBF\x02Zr\x8E\xE2Z\x12\xD8q\xE5&MJ-X:\xB5\xBF\xF7\x7F\xDB\xDFI\bm\xDB\xDB\x80m\x00\x00\x00\xB6m\xDB\xDB\xB6\x00\x00\x00\xB6\xB6\x00m\xDB\x12\x12m\xDB\xDB\x00\x00\x00\x00\x00\xB6m\xDB\x00\xB6\x00\x00\x00\xDB\xB6mm\xDB\xB6\xB6\x00\x00\x00\x00\x00m\xDB" even=true hdr=nil enc=nil mix=true controlbyte="[">
b2,r,lsb,xy         .. text: ["U" repeated 8 times]
b2,r,msb,xy         .. file: VISX image file
b2,g,lsb,xy         .. file: VISX image file
b2,g,msb,xy         .. file: SoftQuad DESC or font file binary - version 15722
b2,b,msb,xy         .. text: "UfUUUU@UUU"
b4,r,lsb,xy         .. text: "\"\"\"\"\"#4D"
b4,r,msb,xy         .. text: "wwww3333"
b4,g,lsb,xy         .. text: "wewwwwvUS"
b4,g,msb,xy         .. text: "\"\"\"\"DDDD"
b4,b,lsb,xy         .. text: "vdUeVwweDFw"
b4,b,msb,xy         .. text: "UUYYUUUUUUUU"
fergll@FerGLl:/mnt/c/Users/ferch/Documents$

```

- Se utilizo la herramienta `zsteg` está programada en Ruby y utiliza una librería interna (`zpng`) para leer los píxeles de la imagen.
- En este caso se aumento temporalmente el límite de memoria de la pila (Stack Size) de Ruby indicándole una variable de entorno especial en la misma línea de comandos. para poder obtener la bandera

**Referencias**

- https://0xrick-github-io.translate.goog/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=sge&_x_tr_hist=true#zsteg 


