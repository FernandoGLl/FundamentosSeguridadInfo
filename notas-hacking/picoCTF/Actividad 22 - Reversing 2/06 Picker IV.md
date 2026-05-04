#### Description

Can you figure out how this program works to get the flag? Connect to the program with netcat: `$ nc saturn.picoctf.net 58513` The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV).

**Solución**

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ readelf -s picker-IV | grep win
    63: 000000000040129e   150 FUNC    GLOBAL DEFAULT   15 win
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc saturn.picoctf.net 58513
Enter the address in hex to jump to, excluding '0x': 40129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}

```

- Descargamos el archivo ejecutable y utilizamos el comando `readelf -s` en la terminal para inspeccionar sus símbolos internos.
- Al filtrar los resultados (`grep win`), descubrimos que la función estaba alojada en la dirección hexadecimal `40129e`.
- Nos conectamos al servidor por `netcat` e ingresamos esa dirección (`40129e`), lo que hizo que el programa saltara a esa instrucción específica y nos entregara la bandera.

**Referencias**





