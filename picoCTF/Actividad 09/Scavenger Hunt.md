#### Description

There is some interesting information hidden around this site. Can you find it? http://wily-courier.picoctf.net:55600/

**Solución**

```
p> <!-- Here's the first part of the flag: picoCTF{t -->

/* CSS makes the page look nice, and yes, it also has part of the flag. Here's 
part 2: h4ts_4_l0 */

User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?

# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.

Congrats! You've completed the scavenger hunt! Part 5: _9588550}

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}

```


**Notas adicionales**

- Para obtener la primera pate de la bandera lo que se realizo fue inspeccionar la pagina a donde nos llevo el link de la actividad, ahí se nos da la primeara parte de la bandera, luego reviso el contenido en la parte del HTML y ahí se encontró la segunda parte.
- Luego gracias a la pista que nos dejan se procede a utilizar el robots.txt y ahí nos dan la 3ra parte.
- Después se utiliza el .htaccess y se encontró la 4ta parte.
- por ultimo se utilizo el .DS_Store y ahí nos da la ultima parte.


**Referencias**

- https://httpd.apache.org/docs/2.4/en/howto/htaccess.html
- https://en.wikipedia.org/wiki/.DS_Store