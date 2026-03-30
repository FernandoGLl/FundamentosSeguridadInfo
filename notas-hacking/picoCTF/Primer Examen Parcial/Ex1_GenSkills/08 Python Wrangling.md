#### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [ende.py](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/ende.py) using [password.txt](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/password.txt) to get [flag.txt.en](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/flag.txt.en)?

**Solución** 

picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

**Notas adicionales** 

- Se descargaron los 3 archivos
- Luego se realizo lo siguiente:
```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat password.txt
720b6ad346f84cd483c60c7464dd95d4
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ python3 ende.py -d flag.txt.en
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}

```

- **Inspección del script:** Se ejecutó **`python3 ende.py -h`** para entender la sintaxis del programa y confirmar que la bandera **`-d`** se utiliza para desencriptar (decrypt).
    
- **Lectura de credenciales:** Se visualizó el contenido de la contraseña usando **`cat password.txt`** para tenerla lista en el portapapeles.
    
- **Ejecución y Desencriptado:** Se corrió el comando **`python3 ende.py -d flag.txt.en`** y se ingresó la contraseña cuando el script la solicitó.
    
- **Obtención de la Flag:** El script procesó el archivo y mostró la bandera **`picoCTF{...}`** directamente en la terminal.

**Referencias** 
