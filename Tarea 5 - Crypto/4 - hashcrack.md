## Descripción
A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server? Access the server using `nc chatelaine.cylabacademy.net 39039`

pistas:
1. Understanding hashes is very crucial. [Read more here](https://primer.cylabacademy.org/#_hashing).

2. Can you identify the hash algorithm? Look carefully at the length and structure of each hash identified.

3. Tried using any hash cracking tools?
## Solución

```
Se utilizó Netcat para conectarse a la instancia del reto:

```bash
nc chatelaine.cylabacademy.net 39039
```

El servidor mostró un hash y solicitó ingresar la contraseña correspondiente.

```text
482c811da5d5b4bc6d497ffa98491e38
```

Por su longitud de 32 caracteres hexadecimales, se identificó como un posible hash MD5.

Contraseña encontrada:

```text
password123
```

Se ingresó en el servidor para continuar con el reto.

El servidor proporcionó el siguiente hash:

```text
b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
```

Por su longitud de 40 caracteres hexadecimales, se identificó como un posible hash SHA-1. Se intentó recuperar la contraseña para avanzar al siguiente nivel.
El servidor presentó el siguiente hash:

```text
916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
```

Se identificó como un posible hash SHA-256 por tener 64 caracteres hexadecimales.

Primero se intentó utilizar Hashcat con el diccionario RockYou:

```bash
hashcat -m 1400 -a 0 '916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745' /usr/share/wordlists/rockyou.txt
```

Como el archivo del diccionario no estaba disponible en la ruta indicada, se instaló el paquete correspondiente:

```bash
sudo apt update
sudo apt install wordlists -y
```

Después, se intentó descomprimir el diccionario:

```bash
sudo gzip -dk /usr/share/wordlists/rockyou.txt.gz
```

Una vez disponible el diccionario, se ejecutó nuevamente Hashcat para buscar la contraseña.

La contraseña recuperada fue:

```text
qwerty098
```

```
encontramos la flag:
academy{UseStr0nG_h@shEs_&PaSswDs!_a8894b1b}
```


```
## Notas adicionales
## Referencias
