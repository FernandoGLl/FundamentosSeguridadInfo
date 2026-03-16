#### Description

This is a really weird text file. Can you find the flag? Get the flag from [TXT](https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt).

**Solución**

picoCTF{now_you_know_about_extensions}

**Notas adicionales**

- El sistema operativo o el usuario pueden ser engañados por una extensión falsa (.txt), pero la estructura interna del archivo (los Magic Bytes o firma) revela su verdadera naturaleza. En forense, nunca confiamos en la extensión del archivo para determinar su contenido.
- En este caso lo que se realizo fue revisar que tipo de archivo era verdaderamente y después de eso se cambio a la extensión correcta en este caso png. 

**Referencias**



