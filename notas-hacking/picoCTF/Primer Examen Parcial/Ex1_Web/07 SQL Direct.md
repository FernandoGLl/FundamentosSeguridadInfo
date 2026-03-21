#### Description

Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 59559 -U postgres pico` Password is `postgres`

**Solución**

picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents/EX1$ psql -h saturn.picoctf.net -p 59559 -U postgres pico
Password for user postgres:
psql (16.13 (Ubuntu 16.13-0ubuntu0.24.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_31fd14c0}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=#

```

- **Conexión Remota:** se uso el comando `psql` pasándole los parámetros exactos (servidor, puerto, usuario y base de datos) para autenticarte en el servidor del reto.
    
- **Reconocimiento (Enumeración):** Una vez dentro del prompt de la base de datos (`pico=#`), se uso el comando especial `\dt` para listar todas las tablas existentes y localizar la que contenía la información importante.
    
- **Extracción de Datos:** se ejecuto una consulta básica en lenguaje SQL (`SELECT * FROM flags;`) para volcar todo el contenido de la tabla en tu pantalla y leer la flag.

**Referencias** 