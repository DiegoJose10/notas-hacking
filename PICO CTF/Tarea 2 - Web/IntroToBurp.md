Try [here](http://titan.picoctf.net:65227/) to find the flag
Hints:
- Try using burpsuite to intercept request to capture the flag.
- Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
# Solucion
Al entrar al sitio web ingresamos todos los datos pedidos y al ingresar el otp nos dice invalid otp, por lo cual usamos el inspector y en la pestaña de red editamos la solicitud quitando el otp y al reenviarla nos aparece la bandera: picoCTF{#0TP_Bypvss_SuCc3$S_b3fa4f1a}
