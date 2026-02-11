#### Description

Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/563d66bbed3925c75ed71efa974bfafab26460ae99938d699a8881cd173fca60/strings) without running it?

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ strings strings | grep "picoCTF{"
picoCTF{5tRIng5_1T_dB2CEA76}

Notas adicionales

El comando strings es un comando de linux que se encarga de de extraer los fragmentos de datos o cadenas imprimibles de los archivos para que todos los comandos puedan usarlas sin tener que lidiar con caracteres no imprimibles. 

Referencias:

https://www-howtogeek-com.translate.goog/427805/how-to-use-the-strings-command-on-linux/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc
