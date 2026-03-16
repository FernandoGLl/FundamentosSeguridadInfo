#### Description

Can you break into this super secure portal? http://fickle-tempest.picoctf.net:55714

**Solución**

```

<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'eb02') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_2') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == 'b45}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
```

picoCTF{no_clients_plz_2eb02b45}

**Notas adicionales**

- Se entro al link que se proporcionaba en la actividad, después de esto se observo que el código de la contraseña el creador lo dejo del lado del cliente.
- Por lo tanto para poder obtener la bandera se inspecciono el código fuente y en el apartado de depurador y luego index se encontró la función chackpass donde se encontró la bandera separada.

**Referencias**

- https://www.educative.io/answers/client-side-vs-server-side

- https://firefox-source-docs.mozilla.org/devtools-user/debugger/index.html
