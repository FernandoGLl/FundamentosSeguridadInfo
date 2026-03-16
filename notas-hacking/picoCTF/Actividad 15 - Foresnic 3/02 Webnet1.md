#### Description

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.

**Solución**
```
fergll@FerGLl:/mnt/c/Users/ferch/documents/webnet01$ tshark -r capture.pcap -o "tls.keys_list:0.0.0.0,443,http,picopico.key" -Y "http" -T fields -e http.request.uri -e http.file_data


fergll@FerGLl:/mnt/c/Users/ferch/documents/webnet01$ mkdir extraido
tshark -r capture.pcap -o "tls.keys_list:0.0.0.0,443,http,picopico.key" --export-objects http,extraido

fergll@FerGLl:/mnt/c/Users/ferch/documents/webnet01$ exiftool extraido/* | grep "pico"
Artist                          : picoCTF{honey.roasted.peanuts}

```

picoCTF{honey.roasted.peanuts}

**Notas adicionales**

- Usamos la llave privada (`picopico.key`) para convertir el tráfico cifrado (TLS) en datos legibles (HTTP). Sin la llave, solo verías ruido binario.
- A diferencia del reto anterior, la flag no estaba en el texto de la página. Usamos tshark para rearmar los archivos (imágenes, scripts o documentos) que se enviaron en los paquetes de red y guardarlos en una carpeta.
- Buscamos la flag dentro de esos archivos reconstruidos, ya sea leyendo su contenido con grep o revisando sus datos ocultos (metadatos) con exiftool.

**Referencias**


