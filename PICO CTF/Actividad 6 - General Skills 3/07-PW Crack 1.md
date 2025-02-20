Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
Hints
- To view the file in the webshell, do: `$ nano level1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.
# Solucion
Se usa wget para descargar los archivos, luego vi para ver el codigo del archivo .py, ahi se puede ver la contraseña 1e1a y finalmente se ejecuta el archivo .py y pide contraseña, se usa la contraseña obtenida anteriormente y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py
--2025-02-19 20:44:09--  https://artifacts.picoctf.net/c/11/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py.2'

level1.py.2                                                100%[=======================================================================================================================================>]     876  --.-KB/s    in 0s      

2025-02-19 20:44:09 (37.4 MB/s) - 'level1.py.2' saved [876/876]

diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
--2025-02-19 20:44:20--  https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                        100%[=======================================================================================================================================>]      30  --.-KB/s    in 0s      

2025-02-19 20:44:20 (2.30 MB/s) - 'level1.flag.txt.enc' saved [30/30]

diegojfh1000-picoctf@webshell:~$ vi level1.py
diegojfh1000-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```
picoCTF{545h_r1ng1ng_fa343060}