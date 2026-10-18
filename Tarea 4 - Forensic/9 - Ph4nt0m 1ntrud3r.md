## Descripción
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.cylabacademy.net/library/cdf8425b82c6532c974b1a04fedc342a6d94dab1825f90cb223f67cb15193c15/myNetworkTraffic.pcap) and try to get the flag.
## Solución
Primero descargamos el .pcap, después al abrirlo con wireshark podemos observar que si filtramos por tiempos, se va formando una cadena que es la flag encriptada, por lo que para conseguirla de manera automática, utilizamos el comando de "tshark -r myNetworkTraffic.pcap -T fields -e frame.time_epoch -e tcp.payload | sort -n | awk '{print $2}' | tr -d '\n' | xxd -r -p | base64 -d" y con ello obtenemos la flag

```
academy{1t_w4snt_th4t_34sy_tbh_4r_a8139a41}
```
## Notas adicionales
## Referencias
