#### Description

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/500/files.zip)

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ unzip -p files.zip "*/uber-secret.txt"
picoCTF{f1nd_15_f457_ab443fd1}

**Notas adicionales**

- unzip -p es un comando que extrae el contenido del archivo específico directamente a la pantalla sin crear carpetas ni descomprimir el resto del paquete.

**Referencias**

https://elementor.com/blog/how-to-use-the-unzip-command-in-linux/
