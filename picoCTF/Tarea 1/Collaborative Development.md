
#### Description

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/70/challenge.zip)

**Solución**
```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ unzip challenge.zip

Fercho@MSI:/mnt/c/Users/ferga/downloads$ cd drop-in
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
  master
  
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git checkout -f feature/part-1
cat flag.py
Switched to branch 'feature/part-1'
print("Printing the flag...")
Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git checkout -f feature/part-2in$ git checkout -f feature/part-2
cat flag.py
Switched to branch 'feature/part-2'
print("Printing the flag...")

Fercho@MSI:/mnt/c/Users/ferga/downloads/drop-in$ git checkout -f feature/part-3n$ git checkout -f feature/part-3
cat flag.py
Switched to branch 'feature/part-3'
print("Printing the flag...")

print("w0rk_7ffa0077}")
  
```

picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ffa0077}


**Notas adicionales**

- El primer paso fue descomprimir el archivo, luego de esto de entro al archivo de drop-in
- Una vez dentro del archivo se procedió a realizar lo que nos indico la pista que fue utilizar el comando "git branch -a"  
- Luego de esto como la bandera esta dividida en 3 partes se leyó el contenido de cada rama y con eso obtuvimos la bandera completa
- Para que funcione el programa se tiene que instalar .git

**Referencias**

https://git-scm.com/install/linux