Theres tapping coming in from the wires. What's it saying `nc jupiter.challenges.picoctf.org 21610`.
Hints:
- What kind of encoding uses dashes and dots?
- The flag is in the format PICOCTF{}
# Solución
Después de conectarnos a este puerto, se nos da una secuencia de puntos y guiones.
Esto nos permite deducir que el encriptado esta en código morse. Asi que se usa una herramienta en línea para decodificarlo, al decodificarlo nos da la bandera
PICOCTF{M0RS3C0D31SFUN3902019519}

# Referencias
https://morsecodetranslator.com/es/