#### Description

Check the admin scratchpad! http://fickle-tempest.picoctf.net:65300

**Solución**

```

Fercho@MSI:/mnt/c/Users/ferga$ hashcat -m 16500 hash /usr/share/wordlists/rockyou.txt
hashcat (v6.2.6) starting

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiRkVSTkFORE8ifQ.K1WNYgQr-WP2yGDJgusVdByT9EMoWCo93YyiZ7fKCL4:ilovepico


```


```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s


picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}

```
**Notas adicionales**

- Se detecto que el servidor de **picoCTF** usaba un **JSON Web Token (JWT)** para manejar la sesión. Al decodificarlo, el usuario era **"FERNANDO"** y  el algoritmo de firma era **HS256**.
- Como el servidor solo acepta tokens firmados con una "Secret Key" desconocida, se utilizo **Hashcat** con el diccionario `rockyou.txt`. Se probaron millones de claves hasta encontrar la correcta: **`ilovepico`**.
- un script de **Python** para crear un nuevo token. En este nuevo token:
     Se cambio el nombre de usuario a **"admin"**.
     Se genero una firma nueva y válida usando la clave **`ilovepico`**.
- Se sustituyo el token original en las **cookies** del navegador por el que se fabrico en Python. Al refrescar, el servidor validó la firma, creyó que era el administrador y se liberó la **flag**.

**Referencias**

- https://en.wikipedia.org/wiki/JSON
- https://www.jwt.io/introduction#what-is-json-web-token
- https://www.jwt.io/#debugger-io
- https://github.com/openwall/john