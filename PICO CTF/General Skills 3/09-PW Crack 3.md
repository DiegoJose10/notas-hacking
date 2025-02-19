Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
Hints
- To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
- To exit `bvi` type `:q` and press enter.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
Se usa wget para descargar todos los archivos y usando vi se verifica el archivo .py para saber las posibles contraseñas y luego se ejecutar ese archivo usando python 3 e ingresamos las contraseñas vistas en el archivo hasta que sea la correcta y aparezca la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py | wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc | wget https://artifacts.picoctf.net/c/18/level3.hash.bin 
--2025-02-19 21:17:47--  https://artifacts.picoctf.net/c/18/level3.hash.bin
--2025-02-19 21:17:47--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... Resolving artifacts.picoctf.net (artifacts.picoctf.net)... --2025-02-19 21:17:47--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
3.160.22.92, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... HTTP request sent, awaiting response... connected.
HTTP request sent, awaiting response... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc.2'

level3.flag.txt.enc.2                                      100%[=======================================================================================================================================>]      31  --.-KB/s    in 0s      

2025-02-19 21:17:47 (2.64 MB/s) - 'level3.flag.txt.enc.2' saved [31/31]

200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin.2'

level3.hash.bin.2                                          100%[=======================================================================================================================================>]      16  --.-KB/s    in 0s      

2025-02-19 21:17:47 (1.25 MB/s) - 'level3.hash.bin.2' saved [16/16]

200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py.3'

level3.py.3                                                100%[=======================================================================================================================================>]   1.31K  --.-KB/s    in 0s      

2025-02-19 21:17:47 (23.4 MB/s) - 'level3.py.3' saved [1337/1337]

diegojfh1000-picoctf@webshell:~$ vi level3.py.3
diegojfh1000-picoctf@webshell:~$ python3 level3.py.3
Please enter correct password for flag: 8799
That password is incorrect
diegojfh1000-picoctf@webshell:~$ python3 level3.py.3
Please enter correct password for flag: d3ab
That password is incorrect
diegojfh1000-picoctf@webshell:~$ python3 level3.py.3
Please enter correct password for flag: 1ea2
That password is incorrect
diegojfh1000-picoctf@webshell:~$ python3 level3.py.3
Please enter correct password for flag: acaf
That password is incorrect
diegojfh1000-picoctf@webshell:~$ python3 level3.py.3
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
picoCTF{m45h_fl1ng1ng_6f98a49f}