Can you get the flag? Go to this [website](http://saturn.picoctf.net:64238/) and see what you can discover.
Hints:
- Do you know how to modify cookies?
# Solucion
Al entramos y dando click en continuar como invitado no nos sale nada, asi que utilizando cookie editor o desde el inspector en la pestaña de almacenamiento y en las cookies cambiamos el valor de la cookie isAdmin de 0 a 1 y refrescamos la pagina y asi nos aparece la bandera:
picoCTF{gr4d3_A_c00k13_0d351e23}