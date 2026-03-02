#### Description

Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:61178/).

**Solución**

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_3b0fca37}

**Notas adicionales**

- Primero se utilizo el mismo modo para poder entrar que en uno de los ejercicios anteriores qeu es la técnica de la "Inyección". El usuario fue admin y la contraseña  ' or 1=1 -- .
- Una vez dentro nos proporciono un campo de búsqueda o una tabla, en SQLite, la tabla maestra es donde se guardan todos los nombres de las tablas y esta se llama sqlite_master. Por lo tanto inyectamos esto en el campo de búsqueda para ver los nombres de las tablas: ' UNION SELECT 1, sql, 3 FROM sqlite_master -- 
- Cuando funciono se busco la tabla que contuviera algo relacionado con flag  o algo así y la que se encontró fue una tabla llamada "more_table", por lo tanto se inyecto esta en la barra de búsqueda y nos dio la bandera 
- ' UNION SELECT 1, flag, 3 FROM more_table --

**Referencias**
- https://www.w3schools.com/sql/sql_injection.asp
