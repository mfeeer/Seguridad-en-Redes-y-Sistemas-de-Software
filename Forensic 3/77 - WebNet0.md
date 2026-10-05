## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.

Pistas:

1. Try using a tool like Wireshark.

2. How can you decrypt the TLS stream?
## Solución
- descargarmos el .pcap 
- usar la key que se nos da para el encriptado TLS 
-  Primero debemos descargar el .pcap y la key, después debemos de usar Wireshark  
``wireshark webnet0-capture.pcap  &
``[1] 369
con el le introducimos que maneje para el flujo de las TLS la key que se nos dio, para que con ello podamos desencriptar la información, luego de eso solamente hacemos una búsqueda de detalles de paquetes con picoCTF y con eso obtenemos la flag

academy{nongshim.shrimp.crackers}|


## Notas adicionales
## Referencias
