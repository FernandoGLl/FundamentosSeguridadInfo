#### Description

Can you get the flag? Go to this [website](http://saturn.picoctf.net:54813/) and see what you can discover.

**Solución** 

function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}

picoCTF{j5_15_7r4n5p4r3n7_05df90c8}

**Notas adicionales**

- Lo que se realizo fue un Hardcoded Credentials,  es un error grave de seguridad porque la "llave" para entrar está pegada en la puerta por fuera; cualquier usuario puede simplemente leer el código fuente y ver cuál es el usuario y la contraseña correctos.

**Referencias**

