#### Description

Help us test the form by submiting the username as `test` and password as `test!` The website running [here](http://saturn.picoctf.net:51887/).

**Solución** 

picoCTF{proxies_all_the_way_df44c94c}

**Notas adicionales** 

- **Captura:** Se uso el "Preserve log" en la pestaña de **Network** para no perder el rastro.
    
- **Intercepción:** se identificaron las respuestas del servidor que tuvieran id.
    
- **Ensamblaje:** se unieron las dos partes de la cadena encontradas en las URLs.
    
- **Traducción:** con ayuda de Cyberchef se decodifico de **Base64** a texto plano para revelar la bandera `picoCTF{...}`.

```

parte 1: http://saturn.picoctf.net:51887/next-page/id=cGljb0NURntwcm94aWVzX2Fs
parte 2: http://saturn.picoctf.net:51887/next-page/id=bF90aGVfd2F5X2RmNDRjOTRjfQ==

```

**Referencias** 

- https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnR3Y205NGFXVnpYMkZzYkY5MGFHVmZkMkY1WDJSbU5EUmpPVFJqZlE9PQ&oeol=FF