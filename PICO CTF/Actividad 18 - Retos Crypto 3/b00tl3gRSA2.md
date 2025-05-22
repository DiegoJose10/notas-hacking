In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 18243`.
Hints:
- What is e generally?
# Solución
El reto incluye que nos conectemos a un servidor, el cual nos da valores de C, **E** y **N**, asi que usamos un descifrador online y al introducir los valores de c, e y n que nos da el servidor el descifrador te da la frase, la cual es la bandera.

picoCTF{bad_1d3a5_4783252}

# Referencias
- https://www.dcode.fr/rsa-cipher