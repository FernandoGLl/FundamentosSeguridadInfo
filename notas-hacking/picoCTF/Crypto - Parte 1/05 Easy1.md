#### Description

The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? 
We've given you the encrypted flag, key, and a table to help UFJKXQZQUNB with the key of SOLVECRYPTO. Can you use this [table](https://challenge-files.picoctf.net/c_fickle_tempest/859ffc313a4d8b63149f144745043a7312fc4f993e405eeeb8ee5ae6ca8444a8/table.txt) to solve it?.

**Solución**

picoCTF{CRYPTOISFUN}

**Notas adicionales**

- Se utilizo el decodificador Cyberchef utilizando el formato Viegenere Decode donde se introduce la llave que se nos proporciona y en la entrada ponemos lo que nos dieron para decodific.
- Cyberchef es una pagina que me permite decodificar en diferentes formatos.

**Referencias** 

- https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('SOLVECRYPTO')&input=VUZKS1hRWlFVTkIg&oeol=FF
