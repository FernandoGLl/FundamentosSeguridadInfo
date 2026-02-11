#### Description

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

**Solución**

Fercho@MSI:/mnt/c/Users/ferga/downloads$ nc fickle-tempest.picoctf.net 52236
Let us see how data is stored
computer
Please give the 01100011 01101111 01101101 01110000 01110101 01110100 01100101 01110010 as a word.
...
you have 45 seconds.....

Input:
computer
Please give me the  o156 o165 o162 o163 o145 as a word.
Input:
nurse
Please give me the 6c696d65 as a word.
Input:
lime
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_563BAF26}

**Notas adicionales**
Cyberchef es una pagina que me permite decodificar en diferentes formatos.

**Referencias**
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDExMDAwMTEgMDExMDExMTEgMDExMDExMDEgMDExMTAwMDAgMDExMTAxMDEgMDExMTAxMDAgMDExMDAxMDEgMDExMTAwMTA
https://gchq.github.io/CyberChef/#recipe=From_Octal('Space')&input=MTU2IDE2NSAxNjIgMTYzIDE0NQ
https://gchq.github.io/CyberChef/#recipe=From_Hex('Auto')&input=NmM2OTZkNjU
