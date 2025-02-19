Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
Hints
- On the webshell, use `ls` to see if both files are in the directory you are in
- The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
Se usa wget para descargar los archivos .py y .txt y con el comando python3 se ejecuta el archivo .py
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2025-02-19 20:18:58--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py               100%[=======================>]   1.25K  --.-KB/s    in 0s      

2025-02-19 20:18:59 (526 MB/s) - 'code.py' saved [1278/1278]

diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2025-02-19 20:19:07--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt          100%[=======================>]      27  --.-KB/s    in 0s      

2025-02-19 20:19:07 (16.5 MB/s) - 'codebook.txt' saved [27/27]

diegojfh1000-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
```
picoCTF{c0d3b00k_455157_d9aa2df2}