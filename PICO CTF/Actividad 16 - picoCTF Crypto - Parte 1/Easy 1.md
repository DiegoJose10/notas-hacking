The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.
Hints:
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
- Please use all caps for the message.
# Solución
El pad de una sola vez (OTP) es un cifrado teóricamente irrompible. Sin embargo, en la práctica es de una usabilidad limitada porque requiere un clave pre-compartida de al menos la misma longitud que el mensaje. 
Se usa una herramienta online de one pad para descifrar el mensaje usando la bandera encriptada y la key. Usando los valores en la descripcion se obtiene el resultado de CRYPTOISFUN, lo ponemos dentro de picoCTF{} y obtenemos la bandera
`picoCTF{CRYPTOISFUN}`

# Referencias
- https://www.dcode.fr/cifrado-cesar
- https://www.boxentriq.com/code-breaking/one-time-pad