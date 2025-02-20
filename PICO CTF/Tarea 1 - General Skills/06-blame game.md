Someone's commits seems to be preventing the program from working. Who is it? You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)

Hints
- In collaborative projects, many users can make many changes. How can you see the changes within one file?
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
# Solucion
Se descarga el archivo, se descomprime, luego entramos a la carpeta de drop-in, despues usamos los comandos de git log para ver la informacion del archivo message.py y ahi aparece la bandera

```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/156/challenge.zip
--2025-02-20 00:33:40--  https://artifacts.picoctf.net/c_titan/156/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 293739 (287K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip         100%[=======================>] 286.85K  1.81MB/s    in 0.2s    

2025-02-20 00:33:40 (1.81 MB/s) - 'challenge.zip' saved [293739/293739]

diegojfh1000-picoctf@webshell:~$ unzip challenge.zip
diegojfh1000-picoctf@webshell:~$ cd drop-in
diegojfh1000-picoctf@webshell:~/drop-in$ ls -la
total 4
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  36 Mar 12  2024 .
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  91 Feb 20 00:33 ..
drwxr-xr-x 8 diegojfh1000-picoctf diegojfh1000-picoctf 166 Mar 12  2024 .git
-rw-r--r-- 1 diegojfh1000-picoctf diegojfh1000-picoctf  22 Mar 12  2024 message.py
diegojfh1000-picoctf@webshell:~/drop-in$ git log message.py
```
```
Git log message.py
commit 0351e0474493168ca76441c24630c17554fd09ca
Author: picoCTF{@sk_th3_1nt3rn_d2d29f22} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:01 2024 +0000

    optimize file size of prod code

commit c9e851509190f5887e91339ee18087e3e77ebfda
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:01 2024 +0000

    create top secret project
(END)
```
picoCTF{@sk_th3_1nt3rn_d2d29f22}