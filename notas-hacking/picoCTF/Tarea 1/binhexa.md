#### Description

How well can you perfom basic binary operations?

Start searching for the flag here `nc titan.picoctf.net 53869`

**Solución** 

```
Fercho@MSI:/mnt/c/Users/ferga/downloads$ nc titan.picoctf.net 53869

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00001010
Binary Number 2: 00111000


Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 0 0 0 1 1 1 0 0

Incorrect input. Provide the right input
Enter the binary result: 0001 1100

Incorrect input. Provide the right input
Enter the binary result: 00011100
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 00010100
Correct!

Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01000010
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 1000110000
Correct!

Question 5/6:
Operation 5: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00111010
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00001000
Correct!

Enter the results of the last operation in hexadecimal: 08

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}

```

**Notas Adicionales**

Se fueron realizando las operaciones que se pedían para poder resolver la actividad.

**Referencias**




