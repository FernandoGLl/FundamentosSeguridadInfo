#### Description

A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag. To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder! Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/a917f567b9cc0f1a730a7801b309955df4d2234a8114326857b9759e9e5d0453/myNetworkTraffic.pcap) and try to get the flag.

**Solución**

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}

**Notas adicionales**

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ strings myNetworkTraffic.pcap | grep "=="
ezF0X3c0cw==
cGljb0NURg==
bnRfdGg0dA==
YmhfNHJfOQ==
fQ==
XzM0c3lfdA==
NTlmNTBkMw==
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "ezF0X3c0cw==" | base64 -d
{1t_w4sfergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "cGljb0NURg==" | base64 -d
picoCTFfergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "bnRfdGg0dA==^C| base64 -d
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "bnRfdGg0dA==" | base64 -d
nt_th4tfergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "YmhfNHJfOQ==" | base64 -d
bh_4r_9fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "fQ==" | base64 -d
}fergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "XzM0c3lfdA==" | base64 -d
_34sy_tfergll@FerGLl:/mnt/c/Users/ferch/Documents$ echo "NTlmNTBkMw==" | base64 -d
59f50d3fergll@FerGLl:/mnt/c/Users/ferch/Documents$

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_959f50d3}
```

- **Filtro rápido:** Usamos `strings` y `grep "=="` en la terminal para extraer directamente las cadenas de texto ocultas.
    
- **Decodificación:** Pasamos esos textos por `base64 -d` para revelar las palabras reales.
    
- **Ensamblaje:** Ordenamos lógicamente los fragmentos decodificados para armar la frase de la bandera.

**Referencias**

- 