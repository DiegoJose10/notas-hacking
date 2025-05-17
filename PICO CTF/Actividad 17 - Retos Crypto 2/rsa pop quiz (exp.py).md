Class, take your seats! It's PRIME-time for a quiz... `nc jupiter.challenges.picoctf.org 18821`
Hints:
- [RSA info](https://simple.wikipedia.org/wiki/RSA_algorithm)
# Solución
Se usa el comando de la descripcion para conectarnos a un servidor donde nos presentan una serie de preguntas relacionadas con RSA. Cada pregunta requiere cálculos o información sobre la criptografía de RSA para responder correctamente.
El algoritmo RSA es un sistema de cifrado de clave pública que se utiliza para encriptar y desencriptar datos, así como para la firma digital. Se basa en la dificultad de factorizar grandes números primos. 
Para resolver cada pregunta se puede hacer uso de un programa en python que nos ayuda a obtener los resultados haciendo distintas formulas, entre ellas estan:
n = p * q
q = n // p
totient = (p-1)*(q-1)
ciphertext = pow(m, e, n)
d = mod_inverse(e, totient)
plaintext = pow(ciphertext, d, n)
Y tambien se sabe que obtener p y q de n es computacionalmente prohibitivo (tardaría mucho en calcular debido al hecho de que n es más grande que 2048. Por lo tanto, sin p y q, o sin cierta vulnerabilidad el descifrado no es factible.
Al final de la ultima pregunta, nos pide convertir el ultimo plainttext  en hex, y luego a ascii y al hacerlo obtenemos la bandera
picoCTF{wA8_th4t$_ill3aGal..oa2d2239b} 
# Referencias
- https://gchq.github.io/CyberChef/