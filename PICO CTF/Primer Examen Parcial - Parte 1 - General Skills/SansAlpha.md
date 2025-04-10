The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols. `ssh -p 53527 ctf-player@mimas.picoctf.net` Use password: `1db87a14`
Hints:
- Where can you get some letters?
# Solucion
La descripción del desafío insinua un teclado restringido, permitiendo sólo números y símbolos para la interacción.
Despues de varios intentos usando wildcards, la conclusion para obtener la bandera es utilizar los comandos:
_1=(/???/????64)
"${_1[0]}" */????.???`
Aqui nos aparece un codigo en base64, el cual al decodificarlo usando cyberchef nos salta la bandera

picoCTF{7h15_mu171v3r53_15_m4dn355_4945630a}

# Referencias
- https://gchq.github.io/CyberChef/