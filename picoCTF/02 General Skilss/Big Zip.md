#### Description

Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)

Solución
- Se instala la libreria unzip para abrir archivos en modo zip
- Luego se descomprime la carpeta con el comando unzip "nombre del archivo"
-  por ultimo se utiliza el comando unzip -p big-zip-files.zip | grep "picoCTF{" . para encontrar la bandera mas rápido

picoCTF{gr3p_15_m4g1c_ef8790dc}

Notas adicionales

-El comando unzip -p big-zip-files.zip | grep "picoCTF{" es mas eficiente ya que extrae lo que se busca principalmente

Referencias
https://www.hostinger.com/mx/tutoriales/comando-unzip-linux





