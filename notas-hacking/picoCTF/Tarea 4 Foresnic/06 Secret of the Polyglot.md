#### Description

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/96/flag2of2-final.pdf).

**Solución**

picoCTF{f1u3n7_1n_pn9_&_pdf_90974127}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ mv flag2of2-final.pdf flag2of2-final.png

```

- **Concepto Políglota:** Identificamos que el archivo está modificado para funcionar como dos tipos de archivo totalmente distintos al mismo tiempo (PDF y PNG).
    
- **Primera mitad (PDF):** Abrimos el archivo como un documento PDF normal, lo que reveló visualmente una parte de la bandera en el texto.
    
- **Segunda mitad (PNG):** Le cambiamos la extensión al archivo a `.png` y lo abrimos como imagen, lo que mostró visualmente la otra parte oculta.
    
- **Unión:** Juntamos los textos encontrados en ambos formatos para armar la bandera completa `picoCTF{...}`.

**Referencias**
- 