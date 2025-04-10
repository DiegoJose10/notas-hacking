Help us test the form by submiting the username as `test` and password as `test!` The website running [here](http://saturn.picoctf.net:49186/).
Hints:
- any redirections?
# Solucion
Al entrar al sitio web nos pide usuario y contraseña, si ponemos unas incorrectas, nos dice que usuario es test y contraseña es test!, al regresar a la pagina principal e ingresando esos valores antes de que direccione la pagina cancelamos la conexion y usando el inspector podemos ver en la pestaña de red que la conexion cancelada tiene valores en iniciador y en archivo que estan codificados en base 64 despues de id=, por lo cual usando cyberchef los juntamos y los decodificamos para de esa manera obtener la bandera.
picoCTF{proxies_all_the_way_25bbae9a}
# Referencias
- https://gchq.github.io/CyberChef/