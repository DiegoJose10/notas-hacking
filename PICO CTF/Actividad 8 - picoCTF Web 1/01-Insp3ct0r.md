Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/9670/` ([link](https://jupiter.challenges.picoctf.org/problem/9670/)) or http://jupiter.challenges.picoctf.org:9670
Hints:
- How do you inspect web code on a browser?
- There's 3 parts
# Solucion

Se abre el sitio web, se da click derecho y verificar el código fuente, ahí aparece el código html de la pagina web y en ese código hay un comentario, el cual contiene la primera parte de la bandera, después le hacemos click a la hoja de estilos, la cual es mycss.cs y en la ultima linea aparece la segunda parte de la bandera y finalmente nos regresamos al código html y le damos click en la hoja de javascript que es myjs.js y en la ultima linea aparece la ultima parte de la bandera.
Juntando las tres partes nos da la respuesta:
picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}