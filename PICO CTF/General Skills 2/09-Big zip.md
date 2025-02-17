Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)
Hints:
- Can grep be instructed to look at every file in a directory and its subdirectories?
# Solucion

Se usa wget para descargar el archivo, al descomprimirlo usando unzip hay muchisimos archivos, por lo cual para encontrar referencias de strings en los archivos se usa el siguiente comando: 
grep -r "pico" big-zip-files big-zip-
Lo cual nos ayudara a encontrar la palabra pico en los archivos
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
--2025-02-17 23:40:03--  https://artifacts.picoctf.net/c/504/big-zip-files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3182988 (3.0M) [application/octet-stream]
Saving to: 'big-zip-files.zip.1'

big-zip-files.zip.1   100%[=======================>]   3.04M  1.82MB/s    in 1.7s    

2025-02-17 23:40:04 (1.82 MB/s) - 'big-zip-files.zip.1' saved [3182988/3182988]

diegojfh1000-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files        enc_flag  salida   strings.1
Addadshashanammu.zip  big-zip-files.zip    file      static   warm
README.txt            big-zip-files.zip.1  flag      strings
diegojfh1000-picoctf@webshell:~$ grep -r "pico" big-zip-files
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```
picoCTF{gr3p_15_m4g1c_ef8790dc}