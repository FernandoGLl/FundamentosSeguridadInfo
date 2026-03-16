#### Description

Find the flag being held on this server to get ahead of the competition http://wily-courier.picoctf.net:56578/

---

**Solución**

|   |   |
|---|---|
|flag|picoCTF{r3j3ct_th3_du4l1ty_8b13f07}|


**Notas adicionales** 

- Dentro de la pagina web, la inspeccionamos y entramos al apartado de red, esto njos permite ver las peticiones del navegador que envia al servidor,en este caso para nosotros lo mas importante es la respuesta que este devuelve. lo
- Lo que se realizao fue modificar la respuesta POST por una HEAD que es como nos indicaba el nombre del ejercicio y esta nos dio como respuesta en el encabezado la bandera

**Referencias**

- https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods
- https://learn.onemonth.com/web-hacking-tools-proxies/
- https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/