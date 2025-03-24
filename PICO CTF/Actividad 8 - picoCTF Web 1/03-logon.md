The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573
Hints:
- Hmm it doesn't seem to check anyone's password, except for Joe's?
# Solucion
Entramos con un usuario y contraseña inventados por nosotros, al entrar nos dice que no hay bandera, así que descargamos un cookie editor, después en el editor de cookies cambiamos el valor del nombre de usuario que pusimos, en vez de que tenga el valor false, ponemos el valor true y recargamos la pagina y ahora si aparece la bandera:

picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}`