#### Description

This website can be rendered only by picobrowser, go and catch the flag! http://fickle-tempest.picoctf.net:50195

**Solución**

![[Pasted image 20260222180518.png]]

`picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}`

**Notas adicionales**

Lo que se realizo fue cambiar el user agent, que es una cadena de texto que envía cada sitio web que se visita, su función principal es decirle al servidor que navegador se esta usando, por eso al momento de cambiarlo ya funciona, ya que solo permitía utilizar uno que fuera de pico.


**Referencias**

- https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Headers/User-Agent