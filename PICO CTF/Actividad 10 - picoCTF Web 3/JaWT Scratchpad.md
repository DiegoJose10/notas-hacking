Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
Hints:
- What is that cookie?
- Have you heard of JWT?
# Solucion
Una cookie es una parte de informacion que la aplicacion utiliza para almacenar un registro cada vez que navegamos en un sitio web
Si buscamos "jwt", descubrimos que se trata de un JSON Web Token (Una forma compacta y segura de compartir información entre partes usando JSON) que se compone de tres componentes: la cabecera, la carga útil y la firma. 
Si decodificamos la cookie jwt que tenemos en [jwt.io](https://jwt.io/), vemos en la cabecera que este es un jwt que utiliza el algoritmo HS256. Sabemos que el nombre de usuario correcto es "admin", ya que el sitio web no deja entrar en sesión, pero no sabemos la firma. Desde aquí, tenemos que utilizar JohnTheRipper, el cual usa un método de fuerza bruta para averiguar la firma de jwt. usando una lista de palabras. Una lista de palabras muy buena es [rockyou](https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt), que tiene una colección masiva de palabras comunes. Después de dirigir esto, JohnTheRipper te tiene una palabra secreto: `ilovepico`. Volvemos a jwt.io y ponemos junto con el usuario siendo 'admin' y el resultado se inserta como cookie de jwt en el sitio web y al refrescar se obtiene la bandera: picoCTF{jawt_was_just_what_you_thought_1ca14548}
# Referencias
- https://jwt.io/
- https://github.com/openwall/john
-