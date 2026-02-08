#### Description

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to fickle-tempest.picoctf.net 58859.

Solución

- nc fickle-tempest.picoctf.net 58859 | grep "picoCTF"
- picoCTF{digital_plumb3r_0BAc587E}

Notas adicionales

- nc abre la conexion con el servidor.
- " | " Se utiliza para tomar el texto "basura" antes de imprimirse en la pantalla y lo para a grep.
- grep busca únicamente la línea que contiene la palabra especificada.

Referencias
https://www.zonasystem.com/2020/07/tipos-de-conexiones-directas-inversas-transferencia-ficheros-netcat-nc.html

