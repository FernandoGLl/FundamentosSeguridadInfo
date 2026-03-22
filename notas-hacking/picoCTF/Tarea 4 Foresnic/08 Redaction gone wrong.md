#### Description

Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

**Solución**

picoCTF{C4n_Y0u_S33_m3_fully}

**Notas adicionales**

- **Diagnóstico:** Identificamos que la "censura" era falsa. El atacante solo dibujó rectángulos negros por encima del texto original, pero no borró la información real del código del archivo.
    
- **Extracción:** Al seleccionar todo el contenido del PDF (`Ctrl + A`) y pegarlo en un bloc de notas, o al usar una herramienta de terminal como `pdftotext`, logramos extraer el texto puro, dejando atrás los gráficos negros.
    
- **Resultado:** El texto que supuestamente estaba oculto se pegó sin problemas, revelando la bandera `picoCTF{...}`.

**Referencia
