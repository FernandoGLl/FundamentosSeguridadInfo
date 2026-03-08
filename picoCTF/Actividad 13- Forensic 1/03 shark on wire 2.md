#### Description

We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/4d884ac4c144f7871b97b96ae69a31a8483651db7929cd4ecb05d7447832f87c/capture.pcap). Recover the flag.

**Solución** 

```

(ctf-env) Fercho@MSI:/mnt/c/Users/ferga/downloads$ python3 solucion.py
	Bandera encontrada: picoCTF{p1LLf3r3d_data_v1a_st3g0}

```

**Notas adicionales** 

- Se enviaron múltiples paquetes a una IP específica por el puerto **22**.
- Los puertos de origen (_Source Ports_) no eran aleatorios; todos estaban en el rango de los **5000** (por ejemplo, 5112, 5105, 5099).
- Este comportamiento es una anomalía, ya que los puertos efímeros suelen ser asignados dinámicamente por el sistema operativo y no siguen una secuencia lógica tan estricta.
DECODIFICACION 

- **Filtrado**: Separó únicamente los paquetes UDP dirigidos al puerto 22.
- **Extracción**: Tomó el número del puerto de origen de cada paquete.
- **Transformación**: Restó la constante **5000** a cada número.
	- Ejemplo: 5112−5000=112.    
- **Interpretación**: Tradujo ese resultado a su carácter correspondiente en la tabla **ASCII**.
	- El número 112 corresponde a la letra **'p'**, iniciando así la bandera `picoCTF{...}`.

**Referencias**

- https://scapy.readthedocs.io/en/latest/
- 


