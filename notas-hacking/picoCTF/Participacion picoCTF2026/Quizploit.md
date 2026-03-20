## Descripcion

Solve the quiz. Download the source code to answer questions [here](https://challenge-files.picoctf.net/c_lonely_island/8b1f899673bb6f6ec2e7026fabfff7e9baf8c65088a033bcd78d39805068cce1/vuln.c). Download the binary to answer questions [here](https://challenge-files.picoctf.net/c_lonely_island/8b1f899673bb6f6ec2e7026fabfff7e9baf8c65088a033bcd78d39805068cce1/vuln). Connect with the challenge instance here: `nc lonely-island.picoctf.net 62652`

## Solucion

```

┌──(min㉿WIN-U49VUBQG3G3)-[~/retos/quizploit]

└─$ nc lonely-island.picoctf.net 62652

  

=========================================================================================================

                                   ELF BINARY ANALYSIS QUIZ

=========================================================================================================

  
  

◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉

◉                                                                                                       ◉

◉  This is a simple questionnaire to analyze the binary characteristics.                                ◉

◉                                                                                                       ◉

◉  When compiling C/C++ source code in Linux, an ELF (Executable and Linkable Format) file is           ◉

◉  created. The flags added when compiling can affect the binary in various ways, like the              ◉

◉  protections.                                                                                         ◉

◉                                                                                                       ◉

◉  Dynamic Linking:                                                                                     ◉

◉  Dynamic linking is a process where a program uses external code libraries (called shared             ◉

◉  libraries or dynamic link libraries) that are loaded into memory at runtime, rather than             ◉

◉  being built directly into the executable file.                                                       ◉

◉                                                                                                       ◉

◉  Static Linking:                                                                                      ◉

◉  The code for all the routines called by your program becomes part of the executable file.            ◉

◉                                                                                                       ◉

◉  Stripped:                                                                                            ◉

◉  The binary does not contain debugging information which can be used with debuggers                   ◉

◉  like GDB.                                                                                            ◉

◉                                                                                                       ◉

◉  Non Stripped:                                                                                        ◉

◉  The binary contains no debuggig information which makes it difficult for analysis.                   ◉

◉                                                                                                       ◉

◉  Canary: A random/specific value which is stored on the stack for protection against                  ◉

◉  buffer overflow.                                                                                     ◉

◉                                                                                                       ◉

◉  Run 'file' and 'checksec' commands on the binary to answer the questions.                            ◉

◉                                                                                                       ◉

◉  Find out what are 'pwntools' and how can this library be used for exploit creation.                  ◉

◉                                                                                                       ◉

◉  To run the binary: chmod +x ./vuln , followed by ./vuln                                              ◉

◉                                                                                                       ◉

◉  Analyze the provided C program and the corresponding binary to answer the questions.                 ◉

◉                                                                                                       ◉

◉  Answer the questions about this binary to get the flag.                                              ◉

◉                                                                                                       ◉

◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉◉

  

[*] Question number 0x1:

  

Is this a '32-bit' or '64-bit' ELF? (e.g. 100-bit)

  

💡 Hint: Check if the system is x86_64 or x86. No compilation flag specified means default.

  

>> 64-bit

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x2:

  

What's the linking of the binary? (e.g. static, dynamic)

  

💡 Hint: The program uses standard library functions like fprintf, fgets, and system.

  

>> dynamic

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x3:

  

Is the binary 'stripped' or 'not stripped'?

  

💡 Hint: By default, binaries compiled without the -s flag contain debugging symbols.

  

>> not stripped

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x4:

  

Looking at the vuln() function, what is the size of the buffer in bytes? (e.g. 0x10)

  

💡 Hint: Check the declaration in the function and answer in either hex or decimal

  

>> 0x15

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x5:

  

How many bytes are read into the buffer? (e.g. 0x10)

  

💡 Hint: Check the fgets

  

>> 0x90

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x6:

  

Is there a buffer overflow vulnerability? (yes/no)

  

💡 Hint: Compare buffer size and input size

  

>> yes

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x7:

  

Name a standard C function that could cause a buffer overflow in the provided C code.

  

💡 Hint: (e.g. fprintf)

  

>> fgets

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x8:

  

What is the name of function which is not called any where in the program?

  

💡 Hint: Analyze the source

  

>>      win

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0x9:

  

What type of attack could exploit this vulnerability? (e.g. format string, buffer overflow, etc.)

  

💡 Hint: Try interpreting the information gathered so far

  

>> buffer overflow

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0xa:

  

How many bytes of overflow are possible? (e.g. 0x10)

  

💡 Hint: Subtract values

  

>> 0x7b

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0xb:

  

What protection is enabled in this binary?

  

💡 Hint: Learn to use checksec

  

>> PIE

  
  

🔥 🔥 🔥 🔥 🔥 🔥 🔥 🔥

🔥                    🔥

🔥       Wrong!       🔥

🔥                    🔥

🔥 🔥 🔥 🔥 🔥 🔥 🔥 🔥

  
  

❌ Incorrect. Try again!

  

[*] Question number 0xb:

  

What protection is enabled in this binary?

  

💡 Hint: Learn to use checksec

  

>> nx

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0xc:

  

What exploitation technique could bypass NX? (e.g. shellcode, ROP, format string)

  

💡 Hint: Choose from the options

  

>> ROP

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

[*] Question number 0xd:

  

What is the address of 'win()' in hex? (e.g. 0x4011eb)

  

💡 Hint: Use gdb/objdump to find the address

  

>> 0x401176

  
  

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

✅                    ✅

✅      Correct!      ✅

✅                    ✅

✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅

  
  

=========================================================================================================

QUIZ COMPLETE!

=========================================================================================================

  

🎉 PERFECT SCORE! 🎉

You got 13/13 questions correct!

  

Flag: picoCTF{my_bIn@4y_3xpl0it_fL@g_0235704f}

  

=========================================================================================================

  

┌──(min㉿WIN-U49VUBQG3G3)-[~/retos/quizploit]

└─$

```

## Notas

-

## Referencias

-