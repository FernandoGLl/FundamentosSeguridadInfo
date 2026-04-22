#### Description

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/3dced65f7a857f7a28f538da0f98fdceca989646f69d4651133b5c04590b0b0d/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/3dced65f7a857f7a28f538da0f98fdceca989646f69d4651133b5c04590b0b0d/scrambled2.png)

**Solución** 

picoCTF{8cdf93c3}

**Notas adicionales**

- Con la ayuda de la herramienta  StegSolve  se logo la union de las 2 imagenes y se logro decifrar la bandera.
- Al iterar por los diferentes modos de combinación en la herramienta, se aplicó una operación matemática (como ADD o XOR) sobre los píxeles correspondientes. Esta operación canceló el ruido aleatorio compartido entre ambas imágenes.

**Referencias**
- https://github.com/zardus/ctf-tools/blob/master/stegsolve/install




