#### Description

This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 49191` The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/1ce03df0245f787fd1d116ac8502051905222e1138057a4070872f3a5d38c232/encrypt.py).

**Solución** 

picoCTF{tw0_1$_pr!m375129bb1}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$  nc verbal-sleep.picoctf.net 49191
N: 25067830240642677149082141280255419692941325981452026113761885181102390839529553120640339879886454814756138291911244917779034022444396133232490307712744922
e: 65537
cyphertext: 9103433996323260074344796108757926703529714665867855621929574473939052381628006768829462673852879368426403915290094912482550126947689557321138036579176621

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ python3
Python 3.12.3 (main, Mar  3 2026, 12:15:18) [GCC 13.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> N = 2506783024064267714908214128025541969294132598145202611376188518110239083952955312064033987988645481475613829191
1244917779034022444396133232490307712744922
>>> e = 65537
>>> c = 9103433996323260074344796108757926703529714665867855621929574473939052381628006768829462673852879368426403915290094912482550126947689557321138036579176621
>>> p = 2
>>> q = N // 2
>>> phi = (p - 1) * (q - 1)
>>> d = pow(e, -1, phi)
>>> m = pow(c, d, N)
>>> flag = m.to_bytes((m.bit_length() + 7) // 8, 'big').decode('utf-8')
>>> print(f"--> {flag} <--")
--> picoCTF{tw0_1$_pr!m375129bb1} <--


```

- En un cifrado RSA normal y seguro, el módulo N se calcula multiplicando dos números primos gigantescos (N=p×q).
- **Cómo se  utilizo:** p=2 y q=N/2.
- Luego utilizamos la Indicatriz de Euler para calcular cuantos numero enteros menores de N no comparten divisores: phi = (p - 1) * (q - 1)
- Luego se calculo la clave privada con la siguiente formula: d = pow(e, -1, phi)
- Y al final desciframos el RSA con lo sigueinte: m = pow(c, d, N)

**Referencias**

