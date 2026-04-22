#### Description

We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/128/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

**Solución** 

**`picoCTF{R0UND_N_R0UND_B6B25531}`**

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat message.txt
165 248 94 346 299 73 198 221 313 137 205 87 336 110 186 69 223 213 216 216 177 138

>>> numbers = [165, 248, 94, 346, 299, 73, 198, 221, 313, 137, 205, 87, 336, 110, 186, 69, 223, 213, 216, 216, 177, 138]

>>> for x in numbers:
...     print(x%37)
...
17
26
20
13
3
36
13
36
17
26
20
13
3
36
1
32
1
28
31
31
29
27

Se decodifico sigueindo las reglas del reto y se obtuvo este resultado:
picoCTF{R0UND_N_R0UND_B6B25531}

```

- Identificamos que el reto "basic-mod1" requería tomar una serie de números, calcular su módulo 37 y usar ese residuo para encontrar un carácter basado en un conjunto de reglas (0-25 para A-Z, 26-35 para 0-9, y 36 para guion bajo).
- Procesamos la lista exacta de números que proporcionaste y logramos descifrar el mensaje oculto, obteniendo la bandera final.

**Referencias**

