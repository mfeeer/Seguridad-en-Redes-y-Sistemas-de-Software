
## Descripción

This website puts a two-factor prompt between you and the flag. Register an account, then take a close look at the requests your browser is actually sending. Try [here](http://xebec.cylabacademy.net:42021/) to find the flag

pistas:
1. Try using burpsuite to intercept request to capture the flag.
2. Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## Solución

Para resolver este reto debemos de llenar el registro que aparece, al llegar a la validación en 2 pasos, no tenemos nuestro código que nos ayude a ingresar. 
Para lograr entrar, activamos el proxy de foxyproxy y empezamos a interceptar con burpsuite, al mandar una solicitud, deberemos de eliminar el parámetro otp para darle un error a la página, la cual nos dará nuestra flag:
academy{#0TP_Bypvss_SuCc3$S_f182f0ef}

## Notas adicionales
- El nombre del reto ("Intro to Burp") apunta a la herramienta pensada para resolverlo: interceptar la petición del formulario de OTP con **Burp Suite** (proxy/Repeater) y cambiar manualmente el `Content-Type`/`Accept` a `application/json` antes de reenviarla — exactamente lo que se automatizó aquí con `requests` directamente.
## Referencias
