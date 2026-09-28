## Descripción

We found this [packet capture](https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap). Recover the flag.

1.   Try using a tool like Wireshark, What are streams?
## Solución
```
wget https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap

(Fer㉿Fersita)-[~]
└─$ sudo apt install wireshark
abrimos wireshark
abrimos el archivo y buscamos uno que sea UDP, para poder buscar la flag correspondiente
```
## Notas adicionales
## Referencias