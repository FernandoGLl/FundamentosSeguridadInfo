#### Description

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses. Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools! You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/20/challenge.zip)

`ssh -p 61052 ctf-player@atlas.picoctf.net` Using the password `6abf4a82`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!

**Solución** 

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ ssh -p 61052 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password:
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 1
Higher! Try again.
Enter your guess: 1000
Lower! Try again.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Congratulations! You guessed the correct number: 750
Here's your flag: picoCTF{g00d_gu355_bee04a2a}
Connection to atlas.picoctf.net closed.
```

**Notas adicionales**

Se utilizo la siguiente ideología
	- Se divide el rango a la mitad
	- Dependiendo de si decía mas alto o mas bajo se dividía la mitad para abajo o arriba.
	- Y así repetir el proceso.

**Referencias**




