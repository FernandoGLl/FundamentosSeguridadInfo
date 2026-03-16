#### Description

We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.

**Solución**

picoCTF{c0rrupt10n_1847995}

**Notas adicionales**

- Lo primero que se realizo fue comprobar que tipo de archivo era el que descargamos
- Una vez esto identificado se procedió a arreglar el archivo para que el encabezado fuera el de una imagen PNG, luego de esto se procedió a la alineación de los bloques críticos como pHYs e IDAT.
- Por ultimo se corrigió la dimensión de la imagen y con esto se soluciono, todo esto se realizo desde un codificador hexadecimal.

**Referencias**
- https://hexed.it/
- https://en.wikipedia.org/wiki/List_of_file_signatures


