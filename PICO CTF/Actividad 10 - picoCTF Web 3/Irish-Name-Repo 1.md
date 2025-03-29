There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!
Hints:
- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.
# Solucion
La inyección SQL generalmente ocurre cuando le pides a un usuario una entrada, como su nombre de usuario o ID de usuario, y en lugar de un nombre o ID, el usuario te da una declaración SQL que, sin saberlo, ejecutarás en tu base de datos.
Al abrir la pagina, vemos que hay personas irlandeses y al usar el menu y elegir la pagina de soporte vemos una consulta que dice "Hola. Intenté agregar a mi irlandés favorito, Conan O'Brien. Pero sigo recibiendo un error SQL. Esto indica que el sitio usa una base de datos SQL. Al acceder al inicio de sesión de administrador que esta colocado en el menu, podemos intentar una inyección SQL básica para omitir el portal. Nuestra inyección consiste en especificar el nombre de usuario o la contraseña como ' or 1=1; en este caso lo pondremos en contraseña y en username usaremos admin. Al hacerlo entramos y podemos ver la bandera: picoCTF{s0m3_SQL_c218b685}
# Referencias
- https://www.w3schools.com/sql/sql_injection.asp