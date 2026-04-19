#### Description

In RSA, a small e value can be problematic, but what about N? Can you decrypt this? [values](https://challenge-files.picoctf.net/c_wily_courier/2bbb4086ce95d3e431695877b72b7ea062756cb58e97fb4b5a9f3b61ae21ce28/values)

**Solución** 

picoCTF{sma11_N_n0_g0od_1dc7ae91}

**Notas adicionales**

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat values
Decrypt my super sick RSA:
c: 15341890103764929939105506004034128738090325640037083301857608662849501626260517
n: 948406957756830799684818171639547165784816468744946013083947881743680617123566349
e: 65537


```

- Se extrajo el contenido que venia dentro del documento de values.
- Luego de esto se pusieron los valores dentro de un decodificador web que nos ayudo a encontrar la solución.
- La pagina nos dio el resultado de forma incorrecta simplemente se leyó el texto de atrás hacia adelante. Al invertir la cadena obtenemos la bandera en el formato correcto. 

**Referencias** 
- https://www-dcode-fr.translate.goog/rsa-cipher?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc
