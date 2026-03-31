#### Description

Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer. `ssh -p 57795 ctf-player@saturn.picoctf.net`. The password is `af86add3`


**Solución** 

picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_a8567b6f}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ ssh -p 57795 ctf-player@saturn.picoctf.net
ctf-player@saturn.picoctf.net's password:
Specialer$ ls
-bash: ls: command not found
Specialer$ echo *
abra ala sim
Specialer$ cd abra
Specialer$ echo $(<abra)
-bash: abra: No such file or directory

Specialer$ echo $(<magia.txt)
-bash: magia.txt: No such file or directory

Specialer$ echo *
cadabra.txt cadaniel.txt
Specialer$ echo $(<cadabra)
-bash: cadabra: No such file or directory

Specialer$ echo $(<cadabra.txt)
Nothing up my sleeve!
Specialer$ cd ../ala
Specialer$ echo *
kazam.txt mode.txt
Specialer$ echo $(kazam.txt)
-bash: kazam.txt: command not found

Specialer$ echo $(<kazam.txt)
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_a8567b6f}

```

- **Navegación:** se movió entre los directorios usando `cd` (ej. `cd abra`, `cd ../ala`) y se volvió a listar su contenido.
    
- **Evasión de `cat`:** se aplico la redirección nativa de Bash con la sintaxis `echo $(<archivo)` para leer textos sin depender de programas externos.
    
- **Captura de la Flag:** se exploraron los archivos, se detecto `cadabra.txt` y finalmente leíste `kazam.txt` en la carpeta `ala`, revelando la bandera

**Referencias**


