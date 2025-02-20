Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
Hints
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
Se usa wget para descargar el archivo, luego vi para editarlo y arreglarlo, ya que tenia un problema, en vez de = debia tener == y finalmente se usa el comando python 3 para ejecutarlo y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2025-02-19 20:36:27--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                                  100%[=======================================================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-02-19 20:36:27 (73.8 MB/s) - 'fixme2.py' saved [1029/1029]

diegojfh1000-picoctf@webshell:~$ vi fixme2.py
diegojfh1000-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}