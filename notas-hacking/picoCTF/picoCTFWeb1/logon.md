#### Description

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:57043

**Solución**

`picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}`

**Notas adicionales**

Se inspecciono el código de la pagina y se observo que el apartado de las cookies estaba desactivado, para poderlo activar se descargo una extensión que permite administrar las cookies, para poder modificarlas y así activar la cookie y tener como resultado la bandera.


**Referencias**

- https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers
- https://developer.mozilla.org/en-US/docs/Glossary/Request_header
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods
- https://en.wikipedia.org/wiki/HTTP_cookie
