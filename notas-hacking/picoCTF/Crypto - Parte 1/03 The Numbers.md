#### Description

The numbers... what do they mean? [numbers.png](https://challenge-files.picoctf.net/c_fickle_tempest/7b39deba4212c233b1628c93f16639ed02ad90f51436d2a8914bb11f74a982d3/the_numbers.png)

**Solución** 

PICOCTF{THENUMBERSMASON}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ python3 -c "print(''.join([chr(int(x) + 64) if x.isdigit() else x for x in '16 9 3 15 3 20 6 { 20 8 5 14 21 13 2 5 18 19 13 1 19 15 14 }'.split()]))"
PICOCTF{THENUMBERSMASON}


```

**Referencias**


