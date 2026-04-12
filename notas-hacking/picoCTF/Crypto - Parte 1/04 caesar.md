#### Description

Decrypt this message. Message: [message](https://challenge-files.picoctf.net/c_fickle_tempest/324327ef0dc439d37f8ea25706618c6a389672b2ce2bc56101d6ee6e24f98e15/data.enc)

**Solución**

picoCTF{crossingtherubiconpixkahqg}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://challenge-files.picoctf.net/c_fickle_tempest/324327ef0dc439d37f8ea25706618c6a389672b2ce2bc56101d6ee6e24f98e15/data.enc
--2026-04-12 14:35:38--  https://challenge-files.picoctf.net/c_fickle_tempest/324327ef0dc439d37f8ea25706618c6a389672b2ce2bc56101d6ee6e24f98e15/data.enc
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.174.207.96, 3.174.207.125, 3.174.207.121, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.174.207.96|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 36 [application/octet-stream]
Saving to: ‘data.enc’

data.enc                      100%[=================================================>]      36  --.-KB/s    in 0s

2026-04-12 14:35:39 (7.47 MB/s) - ‘data.enc’ saved [36/36]

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat data.enc
picoCTF{furvvlqjwkhuxelfrqslandktj}

```

 - Se utilizo el decodificador Cyberchef utilizando el formato ROT13 con el valor de 23.
- Cyberchef es una pagina que me permite decodificar en diferentes formatos.

**Referencias**

- https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,23)&input=cGljb0NURntmdXJ2dmxxandraHV4ZWxmcnFzbGFuZGt0an0&oeol=FF