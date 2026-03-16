#### Description

We found this file. Recover the flag. [tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)

**Solución** 

picoCTF{qu1t3_a_v13w_2020}

**Notas adicionales** 

- Al ejecutar el comando file nos dimos cuenta que este era un archivo corrupto o estaba mal configurado
- Se utilizo un editor hexadecimal para corregir el encabezado del formato BMP
- Para solucionar esto cambiamos el encabezado por `28 00 00 00` que es un formato estándar para que Windows lo reconozca.
- Luego aumentamos la altura de forma manual para obtener la bandera

**Referencias**
- https://en.wikipedia.org/wiki/List_of_file_signatures
- https://en.wikipedia.org/wiki/BMP_file_format