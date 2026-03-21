#### Description

Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag. The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden. The website is running [picoCTF News](http://verbal-sleep.picoctf.net:57552/).

**Solución** 

fergll@FerGLl:/mnt/c/Users/ferch/Documents/EX1$ grep "picoCTF{" heapdump-1774124167168.heapsnapshot
picoCTF{Pat!3nt_15_Th3_K3y_a485f162}

**Notas adicionales** 

- Lo que se realizo fue navegar en el citio web buscando endpoint mal configruados
- Loego de esto se descarga el archivo que no se deberia de poder ver que es un dump de memoria 
- Por ultimo buscamos la bandera dentrro del archivo con la ayuda del comando grep.

**Referencias**

