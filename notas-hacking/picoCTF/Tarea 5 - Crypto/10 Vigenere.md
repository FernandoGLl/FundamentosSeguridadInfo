#### Description

Can you decrypt this message? Decrypt this [message](https://artifacts.picoctf.net/c/158/cipher.txt) using this key "CYLAB".

**Solución** 

picoCTF{D0NT_US3_V1G3N3R3_C1PH3R_ae82272q}

**Notas adicionales** 

Esto se encontor dentro del archivo del reto:

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat cipher.txt
rgnoDVD{O0NU_WQ3_G1G3O3T3_A1AH3S_cc82272b}

```

- Como el nombre dedl reto lo indica se utilizo la herramienta de cyberchef para decodificar en formato Vigenere, utilizando la llave de CYLAB que nos proporciona la descripción.

**Referencias**

- https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('CYLAB')&input=cmdub0RWRHtPME5VX1dRM19HMUczTzNUM19BMUFIM1NfY2M4MjI3MmJ9

