Can you abuse the banner? The server has been leaking some crucial information on `tethys.picoctf.net 62128`. Use the leaked information to get to the server. To connect to the running application use `nc tethys.picoctf.net 49211`. From the above information abuse the machine and find the flag in the /root directory.
Hints:
- Do you know about symlinks?
- Maybe some small password cracking or guessing
# Solucion
La contraseña se puede ver al conectarse al servidor que ha estado filtrando información con este comando: `nc tethys.picoctf.net 62128

Ahora que la contraseña ha sido recibida el servidor se puede introducir con este comando: `nc tethys.picoctf.net 49211

Hay una bienvenida y luego pide la contraseña que es `My_Passw@rd_@1234`. Le siguen dos preguntas:

Cuál es la conferencia de seguridad cibernética más importante del mundo? [defcon](https://defcon.org/)  
El primer hacker jamás conocido por hacer llamadas telefónicas gratis, quién era? [john draper](https://search-guard.com/john-draper-captain-crunch/)

En la descripción del desafío dice que la bandera está en `/root`En ese directorio, está el archivo flag.txt que no se puede leer con los permisos actuales. También hay un script.py que muestra la bandera inicial y las preguntas utilizadas para entrar en la webshell.

En el archivo, muestra que agarra la bandera de `/home/player/banner`, y si no existe dice `Please supply banner in /home/player/banner`. Debido a que este script de Python se encuentra en el directorio raíz se ejecuta con privilegios de raíz, pero tira del banner de `/home/player`.

Regresando con `cd /home/player`la bandera podría ser modificada y volver a entrar con el comando netcat para ver el banner cambiado. Al crear un enlace simbólico a la bandera en el directorio raíz y llamarla banner leerá el archivo flag.txt con los permisos de raíz y lo mostrara como el banner. Ahora, cuando vuelve a entrar,  nc tethys.picoctf.net 49211, la bandera se obtiene.

Para eliminar el archivo de banner se usa `rm banner` y se usa `ln -s /root/flag.txt banner`para crear el enlace simbólico y llamar al banner del archivo., ya al salir y  al conectarse de neuvo se muestra la bandera
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_b3ee718e}