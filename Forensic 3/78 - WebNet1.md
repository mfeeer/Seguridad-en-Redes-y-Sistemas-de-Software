## Descripción
We found this [packet capture](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/webnet1-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/afb7599dd63cad30a04eb98d0e4057608120371eb3e8943b632505e32c8b622c/picopico.key). Recover the flag.

pistas:

1. Try using a tool like Wireshark.

2. How can you decrypt the TLS stream?

## Solución 
- Primero debemos descargar el .pcap y la key
- después debemos de usar Wireshark, con el le introducimos que maneje para el flujo de las TLS la key que se nos dio, para que con ello podamos desencriptar la información.
- luego de eso descargamos la imagen de vulture y a la imagen le aplicamos un strings para poder obtener la flag

academy{honey.roasted.peanuts}
## Notas adicionales

## Referencias
