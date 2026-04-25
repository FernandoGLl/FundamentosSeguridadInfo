#### Description

We received an encrypted message. The modulus is built from primes large enough that factoring them isn’t an option, at least not today. See if you can make sense of the numbers and reveal the flag. Download the [message](https://challenge-files.picoctf.net/c_amiable_citadel/3dcd347a6e654c8e7e4c10bd3ad888f73c14cb5375535053baef6ed5cbe2baa8/message.txt).

**Solución**

picoCTF{t1ny_e_46e014ec}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nano solve.py


import binascii

# 1. Pega aquí los valores que vienen en el archivo descargado
n = 7182044538179166323847455947619004644121442847053964595557169963193125715155927639431459349236735519153391415315530>
e = 20
c = 6406374308104068575005667020962740799532346754425887123121060719047394997533981965273446408112118637225072542394156>

def find_root(c, e):
    """Calcula la raíz e-ésima exacta de un número gigante usando búsqueda binaria"""
    low = 1
    high = c
    while low < high:
        mid = (low + high) // 2
        if mid ** e < c:
            low = mid + 1
        else:
            high = mid
    return low

print("Calculando la raíz matemática gigante...")
# 2. Calculamos la raíz e-ésima de c
m = find_root(c, e)

# Verificamos que la raíz sea exacta
if m ** e == c:
    print("¡Raíz exacta encontrada!")
    
    # 3. Convertimos el número a texto
    hex_data = hex(m)[2:] # Quitamos el '0x' inicial
    if len(hex_data) % 2 != 0:
        hex_data = '0' + hex_data

    flag = binascii.unhexlify(hex_data).decode('utf-8')
    print(f"\n--> {flag} <--")
else:
    print("Error: La raíz no es exacta. El mensaje m^e era mayor que N y sí dio la vuelta al módulo.")


-------------EJECUCION-----------
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nano solve.py
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ python3 solve.py
Calculando la raíz matemática gigante...
¡Raíz exacta encontrada!

--> picoCTF{t1ny_e_46e014ec} <--


```

- El creador del reto configuró RSA usando un exponente público (e) demasiado pequeño
- En RSA, el mensaje se cifra elevándolo a e y aplicando el módulo N. Pero al ser e tan pequeño, el resultado de me nunca llega a ser más grande que el gigante módulo N.
- Como el valor no sobrepasa a N, el "reloj" del módulo nunca da la vuelta. La compleja fórmula c≡me(modN) se reduce a una simple potencia de secundaria: c=me.
- En lugar de intentar factorizar N (que era imposible por su tamaño), simplemente calculamos la **raíz cúbica exacta** (o raíz e-ésima) del texto cifrado (c) para obtener el mensaje numérico original (m)

**Referencias**