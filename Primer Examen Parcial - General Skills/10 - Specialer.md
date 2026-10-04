## Descripción
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer. `ssh -p 33814 ctf-player@chatelaine.cylabacademy.net`. The password is `6313d317`
## Solución
1. Se inició sesión en el servidor mediante SSH con:

```
ssh -p 33814 ctf-player@chatelaine.cylabacademy.net
```

usando la contraseña proporcionada.

2. Como algunos comandos comunes estaban deshabilitados, se utilizó `echo *` para visualizar los archivos y carpetas disponibles. Después se accedió a `ala` con `cd ala`.
    
3. Se localizó `kazam.txt` y se obtuvo su contenido mediante:
    

```bash
echo "$(<kazam.txt)"
```

Con esto se mostró la flag del reto.
## Notas adicionales
## Referencias
