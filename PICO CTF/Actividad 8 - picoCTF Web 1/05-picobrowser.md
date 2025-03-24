This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704
Hints:
- You don't need to download a new web browser
# Solucion
Entramos a la pagina, le damos clic en flag y nos dice que no obtenemos la bandera porque no estamos usando el navegador pico browser, así que después usamos clic derecho e inspeccionar, nos vamos a la pestaña de red, después en la solicitud de flag le damos clic derecho y le damos a editar y reenviar y ahora en el campo que dice User-Agent en vez del valor que tenemos ponemos el valor de picobrowser y entonces enviamos la solicitud y ahora si ya aparece la bandera:

picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0}`