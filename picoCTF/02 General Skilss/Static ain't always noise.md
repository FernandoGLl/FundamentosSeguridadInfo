#### Description

Can you look at the data in this binary? The bash script might help! [static](https://challenge-files.picoctf.net/c_wily_courier/34dfb62cf2c94a618c7cdc292ff1c4062b104773695071e9a16ab25ad8cc935c/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/34dfb62cf2c94a618c7cdc292ff1c4062b104773695071e9a16ab25ad8cc935c/ltdis.sh)

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ strings static | grep "picoCTF{"
picoCTF{d15a5m_t34s3r_20335e41}

Notas adicionales

El comando strings es un comando de linux que se encarga de de extraer los fragmentos de datos o cadenas imprimibles de los archivos para que todos los comandos puedan usarlas sin tener que lidiar con caracteres no imprimibles. 

Referencias:

https://www-howtogeek-com.translate.goog/427805/how-to-use-the-strings-command-on-linux/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc

https://superuser-com.translate.goog/questions/1387294/whats-the-difference-between-h-and-help?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc