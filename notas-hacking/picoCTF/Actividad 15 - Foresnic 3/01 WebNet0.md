#### Description

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.

**Solución**

```
fergll@FerGLl:/mnt/c/Users/ferch/documents$ tshark -r capture.pcap -o "tls.keys_list:0.0.0.0,443,http,picopico.key" -P -V | grep "picoCTF"
    Pico-Flag: picoCTF{nongshim.shrimp.crackers}\r\n
    Pico-Flag: picoCTF{nongshim.shrimp.crackers}\r\n
```
picoCTF{nongshim.shrimp.crackers}

**Notas adicionales**

- En lugar de usar wiresherk utilice la herramienta TShark  y la configure para que aplicara la llave al trafico del puerto 443.
- Luego de descifrar el trafico con la herramienta filtramos los datos en busca del patrón `picoCTF{}` 
- `tshark -r capture.pcap -o "tls.keys_list:0.0.0.0,443,http,picopico.key" -P -V | grep "picoCTF"` 

**Referencias**
- https://en.wikipedia.org/wiki/Transport_Layer_Security

