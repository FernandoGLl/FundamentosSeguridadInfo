#### Description

If you want to hash with the best, beat this test! `nc saturn.picoctf.net 50738`

**Solución**

picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ nc saturn.picoctf.net 50738
Please md5 hash the text between quotes, excluding the quotes: 'UV rays'
Answer:
fa572056bc7677e6104801f2773fcc76
fa572056bc7677e6104801f2773fcc76
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'stun guns'
Answer:
d1bc34c1bbadaea803f9ab0284e25adf
d1bc34c1bbadaea803f9ab0284e25adf
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Americans'
Answer:
165813154207e6cacef030430ea09616
165813154207e6cacef030430ea09616
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}


```


Se fue resolviendo a la pregunta con los siguientes comandos:

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo -n 'Corvettes' | md5sum
0d18e8c9500eebd5748b6ad225652080  -
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo -n 'UV rays' | md5sum
fa572056bc7677e6104801f2773fcc76  -
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo -n 'stun guns' | md5sum
d1bc34c1bbadaea803f9ab0284e25adf  -
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo -n 'Americans' | md5sum
165813154207e6cacef030430ea09616  -

```


**Referencias**:

