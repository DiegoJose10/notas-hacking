We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 39894`.
Hints:
- Flag is not in the usual flag format
# Solución
Al entrar al servidor nos muestra un mensaje codificado y esta vez la bandera no está en un formato habitual. Podemos usar una herramienta como [DCODE](https://www.dcode.fr/monoalphabetic-substitution) para resolver esto. Nuestra primera conjetura para un método de cifrado de sustitución es la sustitución monoalfabética, en la que cada caracter es reemplazado por otros caracteres. DCODE tiene un método de descifrado automático que busca mensajes en inglés conherentes y nos consigue nuestra bandera. Dentro de todo el texto decodificado nos aparece la bandera y esta vez sin picoCTF{}.
frequency_is_c_over_lambda_agflcgtyue 

# Referencias
- https://www.dcode.fr/cifrado-cesar

