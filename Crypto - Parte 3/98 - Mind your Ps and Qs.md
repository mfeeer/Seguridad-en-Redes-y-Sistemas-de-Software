## Descripción

In RSA, a small ee value can be problematic, but what about NN? Can you decrypt this? [values](https://challenge-files.cylabacademy.net/library/6195bbe5645e383e13ba14724021967d4dacce9f6077e41b5e663ccb23dbb861/values)

1. Bits are expensive, I used only a little bit over 100 to save money
## Solución

```
-descargué el archivo de values
Decrypt my super sick RSA:
c: 717608817902276639011922897702552744324264244069272484013719744328086856277690292
n: 1368992139315019955067447961537607041364451719382349005056752379702694554965203011
e: 65537

-- Factoricé \(n\) para encontrar los números primos \(p\) y \(q\).
    
- Calculé \(\phi(n)=(p-1)(q-1)\).
    
- Obtuve la clave privada con \(d=e^{-1}\bmod\phi(n)\).
    
- Descifré el mensaje mediante \(m=c^d\bmod n\).
    
- Convertí el resultado numérico a texto y corregí el orden inverso para obtener el flag
  academy{sma11_N_n0_g0od_a3ac7152}
```
## Notas adicionales
## Referencias
