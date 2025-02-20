Find the flag in the Python script! [Download Python script](https://artifacts.picoctf.net/c/36/serpentine.py)
Hints
- Try running the script and see what happens
- In the webshell, try examining the script with a text editor like `nano`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# Solucion
Usando wget se descargar el archivo luego editandolo usando vi, se coloca la llamada a la funcion print_flag() y se comenta todo el codigo desde la funcion def main y al ejecutarlo con python3 aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/36/serpentine.py
--2025-02-19 21:30:23--  https://artifacts.picoctf.net/c/36/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py.1'

serpentine.py.1                                            100%[=======================================================================================================================================>]   2.49K  --.-KB/s    in 0s      

2025-02-19 21:30:23 (99.9 MB/s) - 'serpentine.py.1' saved [2550/2550]

diegojfh1000-picoctf@webshell:~$ vi serpentine.py.1
diegojfh1000-picoctf@webshell:~$ python3 serpentine.py.1
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}
```
picoCTF{7h3_r04d_l355_7r4v3l3d_aa2340b2}