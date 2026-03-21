#### Description

Why search for the flag when I can make a bookmarklet to print it for me? Browse [here](http://titan.picoctf.net:50989/), and find the flag!

**Solución** 

picoCTF{p@g3_turn3r_0148cb05}

**Notas adicionales** 

```

        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓ¡ÒÅ¤í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    

```

- Se entro al link donde nos direccionaba la actividad y dentro del cuadro de texto se nos proporciono un código.
- Este código lo pegamos en la consola de la pagina web que se despliega al inspeccionar la pagina, ahí ponemos el código y este nos da la bandera.

**Referencias**
