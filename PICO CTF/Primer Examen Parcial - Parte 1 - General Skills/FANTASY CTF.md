Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF. Connect to the program with netcat: `$ nc verbal-sleep.picoctf.net 55628`
Hints:
- When a choice is presented like [a/b/c], choose one, for example: `c` and then press Enter.
# Solucion
Usando la webshell de pico ctf usamos el comando que aparece en la descripción para conectarnos al programa y vamos usando el boton enter y eligiendo opciones hasta elegir la opcion de play the game y asi hasta alcanzar el final del programa para que nos suelte la bandera.
picoCTF{m1113n1um_3d1710n_da2cd4b9}