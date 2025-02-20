Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
Hints
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
Se usa wget para descargar el archivo, luego vi para editarlo y arreglarlo, ya que tenia un problema de identacion y finalmente se usa el comando python 3 para ejecutarlo y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/27/fixme1.py
--2025-02-19 20:32:38--  https://artifacts.picoctf.net/c/27/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py.1'

fixme1.py.1                                                100%[=======================================================================================================================================>]     837  --.-KB/s    in 0s      

2025-02-19 20:32:39 (700 MB/s) - 'fixme1.py.1' saved [837/837]

diegojfh1000-picoctf@webshell:~$ vi fixme1.py
diegojfh1000-picoctf@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
```
picoCTF{1nd3nt1ty_cr1515_182342f7}