#### Description

I've hidden a flag in this file. Can you find it? [Forensics_is_fun.pptm](https://challenge-files.picoctf.net/c_wily_courier/d78815176c19ddc85a1388233268d2f4c459fcbbaab197b4a29ebafc88294c54/Forensics_is_fun.pptm)

**Solución** 

```

fergll@FerGLl:/mnt/c/Users/ferch/documents$ cd filtrado/ppt/slideMasters/
fergll@FerGLl:/mnt/c/Users/ferch/documents/filtrado/ppt/slideMasters$ cat hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Qfergll@FerGLl:/mnt/c/Users/ferch/documents/filtrado/ppt/slideMasters$ cat hidden | tr -d ' ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
fergll@FerGLl:/mnt/c/Users/ferch/documents/filtrado/ppt/slideMasters$


```

picoCTF{D1d_u_kn0w_ppts_r_z1p5}

**Notas adicionales**

- Lo que se realizo fue identificar  que tipo de archivo es realmente, como un archivo zip.
- Luego de esto realizamos la extracción de datos con el siguiente comando `unzip Forensics_is_fun.pptm -d filtrado` .
- Luego identificamos anomalias que el autor del reto dejo en rutas muy esprecificas como `ppt/slideMasters/hidden`, para poder ver que tiene el archivo y decodificarlo se utilizo el siguiente código:  `cat hidden | tr -d ' ' | base64 -d`.
- Aquí fue cuándo ya nos dio la bandera .

**Referencias**

