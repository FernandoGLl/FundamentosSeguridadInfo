#### Description

Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way. The flag is in this [file](https://challenge-files.picoctf.net/c_fickle_tempest/9e4f9113960f157ceb824bdb449dc2a74504b484346c1442e64854408d5a90c5/file).

Solución:

- grep -oaE "picoCTF{.*?}" file
- picoCTF{grep_is_good_to_find_things_9C6Ef2F7}

Notas adicionales
- El comando grep -oaE se utiliza en Linux para extraer únicamente el texto que coincide con un patrón de búsqueda. 

Referencias

https://www.hostinger.com/tutorials/grep-command-in-linux?utm_campaign=Generic-Tutorials-DSA-t1|NT:Se|Lang:EN|LO:MX&utm_medium=ppc&gad_source=1&gad_campaignid=20980195875&gclid=Cj0KCQiA4pvMBhDYARIsAGfgwvzqYYJ21eRkKjsikssMAGEf08ZVj0LNexo-FyrxYPfWTbprgEasNkkaAgqyEALw_wcB

