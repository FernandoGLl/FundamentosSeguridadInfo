#### Description

The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:50396/) out.

**Solución** 

picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}

**Notas adicionales**

- **Vulnerabilidad Principal:** **Exposición de Información Sensible** a través de archivos de configuración pública (`robots.txt`).
- **Mecanismo de Evasión:** Uso de **Base64** como método de ofuscación (no cifrado), lo cual es ineficaz contra un análisis manual.

**Referencias** 