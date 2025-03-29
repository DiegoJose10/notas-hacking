Can you get the flag? Go to this [website](http://saturn.picoctf.net:62327/) and see what you can discover.
Hints:
- How is the password checked on this website?
# Solucion
Al entrar al sitio web y poner cualquier valor en username y contraseña nos dice que fallo el acceso, una forma de poder conocer el nombre de usuario y contraseña es utilizando el inspector y en la pestaña de red y en la solicitud de get aparece el archivo secure.js y ahi aparece la funcion de check password en la cual aparece el usuario y la contraseña de admin y al ingresarlas en el sitio web nos da la bandera:
picoCTF{j5_15_7r4n5p4r3n7_a8788e61}