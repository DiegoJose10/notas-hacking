Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip)
Hints:
- After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
# Solucion
Usando wget descargamos el archivo, despues usando unzip lo descomprimimos, luego con cd entramos al ultimo directorio, se verifica el tipo de archivo que tiene y como es ejecutable, lo ejecutamos y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip
--2025-02-17 23:24:33--  https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4521 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip  100%[=======================>]   4.42K  --.-KB/s    in 0s      

2025-02-17 23:24:33 (1.31 GB/s) - 'Addadshashanammu.zip' saved [4521/4521]

diegojfh1000-picoctf@webshell:~$ ls
Addadshashanammu.zip  file  salida  strings    warm
README.txt            flag  static  strings.1
diegojfh1000-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
diegojfh1000-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku
diegojfh1000-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ file fang-of-haynekhtnamet
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=47e898db922f38cb54ab4a08fb4e3def5a1cb6a1, not stripped
diegojfh1000-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ /fang-of-haynekhtnamet
-bash: /fang-of-haynekhtnamet: No such file or directory
diegojfh1000-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurna
bitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}
```
picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}