#### Description

Let's decrypt this. Can you decrypt this [ciphertext](https://challenge-files.picoctf.net/c_fickle_tempest/f22de819031f813589921b4f389356232ea5b6d7637fafb60bb325d596dc10de/ciphertext)? Something seems a bit small.

**Solución**

picoCTF{n33d_a_lArg3r_e_bc950e0e}

**Notas adicionales**

```
(ctf_env) fergll@FerGLl:/mnt/c/Users/ferch/Documents$ python3
Python 3.12.3 (main, Mar  3 2026, 12:15:18) [GCC 13.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from gmpy2 import *
>>> from Crypto.Util.number import long_to_bytes
>>> gmpy.get_context().precision=2048
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'gmpy' is not defined. Did you mean: 'gmpy2'?
>>> gmpy2.get_context().precision=2048
>>> e = 3
>>> c = 2205316413931134031074603746928247799030155221252519872650063628948700193645785517947578323929195613275812391565725176391984484116767211515666360482188604701858613934317828196821638422191523186931460211047129119943550415435824004862735461
>>> root, exact = iroot(c, e)
>>> root
mpz(13016382529449106065894479374027604750406953699090365388203689570618549013079421)
>>> print( long_to_bytes(root) )
b'picoCTF{n33d_a_lArg3r_e_bc950e0e}'

```

- Como lo indicaba en las pistas se procedió a la obtención de la bandera de otra forma.
- Se utilizo la función de iroot para extraer la raíz cubica exacta entera del texto cifrado. Lo que nos devolvió los valores de la raíz calculada y el booleano que era exacta.
- Al convertir la raíz numérica obtenemos de vuelta a bytes usando la función lon_to_bytes, y así obtenemos la bandera.
- 
**Referencias**
