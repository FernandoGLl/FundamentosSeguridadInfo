#### Description

Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information... [warm](https://challenge-files.picoctf.net/c_wily_courier/c293351e09ee53217c6a868e7f98a0a2ba0cf9cdc4e4ed0e18f685d47111c216/warm)

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ chmod +x warm
Fercho@MSI:/mnt/c/Users/ferga/downloads$ ./warm
Hello user! Pass me a -h to learn what I can do!
Fercho@MSI:/mnt/c/Users/ferga/downloads$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}

**Notas adicionales**

- chmod - se usa para cambiar los permisos de archivos y directorios.
- "+ x"  - se usa para establecer específicamente el permiso de ejecución de un archivo.
- el argumento - h sopn opciones dee ayuda o para cambiar el comportamiento de un programa. 

Referencias:

https://www-warp-dev.translate.goog/terminus/chmod-x?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc&_x_tr_hist=true




