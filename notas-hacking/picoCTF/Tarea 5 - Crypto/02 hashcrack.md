#### Description

A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server? Access the server using `nc verbal-sleep.picoctf.net 53959`

**Solución** 

picoCTF{UseStr0nG_h@shEs_&PaSswDs!_4c95d69f}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc verbal-sleep.picoctf.net 53959
Welcome!! Looking For the Secret?

We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
Enter the password for identified hash: password123
Correct! You've cracked the MD5 hash with no secret found!

Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
Enter the password for the identified hash: letmein
Correct! You've cracked the SHA-1 hash with no secret found!

Almost there!! Crack this hash: 916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
Enter the password for the identified hash: qwerty098
Correct! You've cracked the SHA-256 hash with a secret found.
The flag is: picoCTF{UseStr0nG_h@shEs_&PaSswDs!_4c95d69f}

```

- Como lo indica en la descripción las contraseñas son débilmente hasheadas y esto quiere decir que son fáciles de encontrar.
- Lo que se realizo fue entrar a una herramienta en linea llamada CrackStation para poder encontrar la solución.
- Se fue introduciendo el hash que se nos daba hasta llegar a la bandera. 

**Referencias** 

- https://crackstation.net/
