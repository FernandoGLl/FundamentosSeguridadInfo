#### Description

There is a nice program that you can talk to by using this command in a shell: $ nc wily-courier.picoctf.net 61237, but it doesn't speak English...

Solución:
- nc wily-courier.picoctf.net 61237

https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false)&input=MTEyCjEwNQo5OQoxMTEKNjcKODQKNzAKMTIzCjEwMwo0OAo0OAoxMDAKOTUKMTA3CjQ5CjExNgoxMTYKMTIxCjMzCjk1CjExMAo0OQo5OQo1MQo5NQoxMDcKNDkKMTE2CjExNgoxMjEKMzMKOTUKNDkKNTcKNTMKMTAyCjEwMQoxMjUKMTA

Notas adicionales

- el comando nc wily-courier.picoctf.net 61237 nos dará una serie de números que estan en código ASCII.
- utilizaremos la pagina de CyberChef para no tener que convertirlos de manera manual.
- Cyberchef es una pagina que me permite decodificar en diferentes formatos.

Referencias
https://gchq.github.io/CyberChef/#recipe=From_Decimal('Line%20feed',false)&input=MTEyCjEwNQo5OQoxMTEKNjcKODQKNzAKMTIzCjEwMwo0OAo0OAoxMDAKOTUKMTA3CjQ5CjExNgoxMTYKMTIxCjMzCjk1CjExMAo0OQo5OQo1MQo5NQoxMDcKNDkKMTE2CjExNgoxMjEKMzMKOTUKNDkKNTcKNTMKMTAyCjEwMQoxMjUKMTA

