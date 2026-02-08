#### Description

Our flag printing service has started glitching! `$ nc saturn.picoctf.net 54676`

Solución

- Fercho@MSI:/mnt/c/Users/ferga$ nc saturn.picoctf.net 54676
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'

- Fercho@MSI:/mnt/c/Users/ferga$ python3
Python 3.13.5 (main, Jun 25 2025, 18:55:22) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) \
+ chr(0x64) + '}')

- picoCTF{gl17ch_m3_n07_9c42a45d}

Notas adicionales

- Primero se obtiene el código glitcheado con el comando  nc saturn.picoctf.net 54676`.
- Después nos da como resultado una cadena de texto de Phyton, por lo tanto se debe instalar Phyton en la terminal para poder resolver este ejercicio.
- Una vez instalado Python  se ejecuta el comando phython3 para entrar.
- Despues solo se escribe print("la cadena que se quiere transformar").

Referencias
https://www.hostinger.com/mx/tutoriales/comando-cat-linux