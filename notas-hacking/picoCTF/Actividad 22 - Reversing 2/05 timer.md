#### Description

You will find the flag after analysing this apk Download [here](https://artifacts.picoctf.net/c/449/timer.apk).

**Solución** 

picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ apktool d timer.apk -o timer_decodificado
I: Using Apktool 2.7.0-dirty on timer.apk
I: Loading resource table...
I: Decoding AndroidManifest.xml with resources...
I: Loading resource table from file: /home/fergll/.local/share/apktool/framework/1.apk
I: Regular manifest package...
I: Decoding file-resources...
I: Decoding values */* XMLs...
I: Baksmaling classes.dex...
I: Baksmaling classes3.dex...
I: Baksmaling classes2.dex...
I: Copying assets and libs...
I: Copying unknown files...
I: Copying original files...
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ grep -rn "picoCTF{" timer_decodificado/
timer_decodificado/apktool.yml:64:  versionName: picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

```

- Se descargo la herramienta de apktool para poder abrir el archivo descargado, ya que es un archivo de tipo .apk y con esta herramienta es mas fácil de decodificar.
- Luego mediante el código "grep -rn "picoCTF" timer_decodificado/" se obtuvo la bandera de manera mas rápida y sencilla.

**Referencias**


