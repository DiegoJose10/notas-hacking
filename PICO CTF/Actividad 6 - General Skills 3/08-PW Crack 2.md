Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
Hints
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.
# Solucion
Se usa wget para descargar los archivos, luego vi para ver el codigo del archivo .py, ahi se puede ver la contraseña en unicode, asi que usando cyberchef la convertimos en caracteres y finalmente se ejecuta el archivo .py y pide contraseña, se usa la contraseña obtenida anteriormente, la cual de76 y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.py
--2025-02-19 20:48:00--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                                  100%[=======================================================================================================================================>]     914  --.-KB/s    in 0s      

2025-02-19 20:48:00 (241 MB/s) - 'level2.py' saved [914/914]

diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2025-02-19 20:48:09--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                                        100%[=======================================================================================================================================>]      31  --.-KB/s    in 0s      

2025-02-19 20:48:09 (2.63 MB/s) - 'level2.flag.txt.enc' saved [31/31]

diegojfh1000-picoctf@webshell:~$ vi level2.py
diegojfh1000-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

Cyberchef
Input:64 65 37 36
Recipes:
From Charcode
Base: 16
Output: de76
```
picoCTF{tr45h_51ng1ng_489dea9a}
# Referencias

- https://gchq.github.io/CyberChef/