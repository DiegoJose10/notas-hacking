Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 62193 -U postgres pico` Password is `postgres`
Hints:
- What does a SQL database contain?
# Solucion
Con los comandos en la descripción nos conactamos desde la terminal, ahi nos sugieren que le demos help para ver los comandos disponibles, dando help nos damos cuenta que podemos ver las bases de datos con el comando \d ahí nos aparece que hay una tabla llamada flags, asi que para ver su todo su contenido usamos select * from flags y ahi nos aparece  la bandera en la seccion de address del primer dato.
picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}