How about trying to match a regular expression The website is running [here](http://saturn.picoctf.net:62593/).
Hints:
- Access the webpage and try to match the regular expression associated with the text field
# Solucion
Al entrar al codigo fuente del sitio web podemos notar que hay una expresion regular en el codigo de java script: // ^p.....F!?
Las expresiones regulares son patrones de busqueda de texto que se usan en lenguajes de programacion, dicho de otra forma, una expresión regular (regex) es una cadena de caracteres que se usa para buscar, validar o manipular texto. Se basa en reglas sintácticas que permiten describir secuencias de caracteres, Usando la pagina de regexr ponemos la expresion regular obtenida y nos da el patron de como son sus reglas sintacticas, asi que creamos un texto basado en esas reglas: p12345F y lo ingresamos al sitio web y le damos submit y asi aparece la bandera:
picoCTF{succ3ssfully_matchtheregex_08c310c6}

# Referencias
- https://regexr.com/