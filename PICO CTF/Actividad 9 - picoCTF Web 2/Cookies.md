Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:64944/](http://mercury.picoctf.net:64944/)
# Solucion
Hay 3 posibles formas de solucionarlo
- Entrando a la consola usamos el comando curl http://mercury.picoctf.net:21939/check -H "Cookie: name=1" y seguimos cambiando el valor de name de forma ascendente de 1 en 1 hasta finalmente encontrar la cookie, la cual se encuentra en la cookie con valor 18
- Usando la aplicacion burpsuite generamos 20 solicitudes y checamos los resultados y en la cookie con valor 18 aparece la bandera
- Programamos en python un codigo que se usa como exploit para encontrar el valor de la cookie en la cual se encuentra la bandera

picoCTF{3v3ry1_l0v3s_c00k135_cc9110ba}
