#### Description

Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/2/enc_flag).

**Solución**`

picoCTF{caesar_d3cr9pt3d_78250afc}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://artifacts.picoctf.net/c_titan/2/enc_flag
--2026-04-12 14:10:52--  https://artifacts.picoctf.net/c_titan/2/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                      100%[=================================================>]      73  --.-KB/s    in 0s

2026-04-12 14:10:53 (13.5 MB/s) - ‘enc_flag’ saved [73/73]

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat enc_flag
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6YzRNalV3YUcxcWZRPT0nCg==
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat enc_flag | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ=='
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaGlqfQ==" | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_78250hij}fergll@FerGLl:/mnt/c/Users/ferch/Documents$

```

- Se utilizo el decodificador Cyberchef utilizando el formato ROT13 con el valor de 19.
- Cyberchef es una pagina que me permite decodificar en diferentes formatos.

**Referencias**

- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzc4MjUwaG1qfQ&oeol=FF