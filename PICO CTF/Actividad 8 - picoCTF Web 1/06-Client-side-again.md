Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/60786/` ([link](https://jupiter.challenges.picoctf.org/problem/60786/)) or http://jupiter.challenges.picoctf.org:60786
Hints:
- What is obfuscation?
# Solucion
En tecnología, la ofuscación es sinónimo de seguridad. Es una herramienta que se utiliza para aumentar la seguridad del código. En términos generales, la ofuscación convierte el código de un software o proyecto en un tipo de código que es más difícil de comprender para los humanos. Logra este objetivo aplicando mecánicas y patrones de encriptación para evitar el acceso a secciones críticas del código.
Le damos click derecho a la pagina web y le ponemos inspeccionar, nos vamos a la pestaña de depurador y ahi aparece la pista de la bandera, la cual esta en idioma de java script y nos da el valor de la variable var, pero el codigo esta ofuscado, asi que usamos la ayuda de la pagina web JS NICE para hacerlo mas legible y ahi aparece el valor de la variable var, el cual es un arreglo, seleccionamos elementos del arreglo que se aparezcan a la estructura de la bandera y las ordenamos y unimos y de esa manera nos aparece la solucion:
picoCTF{not_this_again_ef49bf}
# Referencias

- https://insights.encora.com/es/blog/ofuscacion-de-codigo
- http://jsnice.org/
