#### Description

I found a web app that can help process images: PNG images only! Try it [here](http://atlas.picoctf.net:56824/)!

**Solución**

picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_03d1d548}

**Notas Adicionales** 

- **Bypass de filtros**: se engaño al servidor usando **Magic Bytes** (escribiendo `PNG` al inicio del archivo) y una **doble extensión** (`.png.php`) para que aceptara un script malicioso como si fuera una imagen.

- **RCE (Ejecución Remota de Código)**: se implemento una **webshell** minimalista que utiliza la función `system()` para recibir comandos de la terminal a través del parámetro `?cmd=` en la URL.

- **Exfiltración**: Una vez cargado el script, se utilizo el comando `cat` para leer el archivo oculto en el servidor y extraer la bandera.

**Referencias**

