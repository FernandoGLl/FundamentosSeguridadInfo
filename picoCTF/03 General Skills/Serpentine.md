#### Description

Find the flag in the Python script! [Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)

**Solución**
```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 serpentine.py
/mnt/c/Users/ferga/downloads/serpentine.py:41: SyntaxWarning: invalid escape sequence '\ '
  /     \      .- ~ ~ -.

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nano serpentine.py
Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 serpentine.py
/mnt/c/Users/ferga/downloads/serpentine.py:41: SyntaxWarning: invalid escape sequence '\ '
  /     \      .- ~ ~ -.

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}
a) Print encouragement
b) Print flag
c) Quit
```

**Notas adicionales**

- Para la solcion de este ejercicio, se modifico el código fuente de serpentie.py, lo que se hizo fue reemplazar la función que daba la otra opción, por la que ya se encontraba dentro del codigo que nos da la bandera.



