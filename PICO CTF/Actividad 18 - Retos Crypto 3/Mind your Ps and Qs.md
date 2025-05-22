In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/3cfeb09681369c26e3f19d886bc1e5d9/values)
Hints:
- Bits are expensive, I used only a little bit over 100 to save money
# Solución
El reto incluye un hipervinculo a un archivo de texto el cual pide descifrar rsa, se puede usar un descifrador online e introducir los valores de C, **E** y **N** y el descifrador te da la frase, la cual es la bandera.
picoCTF{sma11_N_n0_g0od_45369387}
# Referencias
- https://www.dcode.fr/rsa-cipher
