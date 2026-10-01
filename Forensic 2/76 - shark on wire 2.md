## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/f76620763560ca0683be36e0ed4648743f969ab4d852fda0d8fb4d3ae21a173d/shark-on-wire-2-capture.pcap). Recover the flag that was pilfered from the network.
## Solución
Para este reto deberemos de buscar cierta comunicación entre los paquetes que nos proporciona el reto, encontramos que hay algunos paquetes UDP que llevan cierto parecido con la bandera, pero no se encontró cual es el bueno.

Debemos de instalar scapy:

```
sudo apt install python3-scapy
```

Encontramos el puerto al que se van (22) y encontramos que la información corresponde a algunas letras, por lo que podemos usar el siguiente script:

```
from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''

for p in packets:
	if UDP in p and p[UDP].dport == 22:
		if p[UDP].sport > 5000:
			flag += chr(p[UDP].sport-5000)
			
print(flag)

academy{p1LLf3r3d_data_v1a_st3g0}
```
## Notas adicionales
## Referencias