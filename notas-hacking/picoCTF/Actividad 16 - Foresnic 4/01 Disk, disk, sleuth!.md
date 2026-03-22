#### Description

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a118330a1c5e12f3b59fc45a75b8838700482f89c8ea71a28aa1bd66c7ba3968/dds1-alpine.flag.img.gz)

**Solución**

picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ gzip -d dds1-alpine.flag.img.gz
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_5e56e786}
fergll@FerGLl:/mnt/c/Users/ferch/Documents$

```

- Lo primero que se realizo fue descomprimir el archivo utilizando el comando `gzip - d` para extraer la imagen "cruda".
- Luego se escaneo el código binario de la imagen y extraer únicamente las secuencias de caracteres que fueran legibles filtrando con la palabra pico.


**Referencias** 

