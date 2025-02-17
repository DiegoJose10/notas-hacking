Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static)? This [BASH script](https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/ltdis.sh) might help!
# Solucion
Se usa wget junto con el enlace del archivo para descargarlo, el archivo se llama static, asi que se usa el comando strings para buscar las strings del archivo y  se usa el comando grep para filtrar las cadenas que aparezcan con pico, ya que ahi se encontrara la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
--2025-02-17 23:18:46--  https://mercury.picoctf.net/static/ec4dbd8898ade34e1d60d5b70c1b8c8c/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                100%[=======================>]   8.18K  --.-KB/s    in 0s      

2025-02-17 23:18:46 (167 MB/s) - 'static' saved [8376/8376]

diegojfh1000-picoctf@webshell:~$ ls
README.txt  file  flag  salida  static  strings  strings.1  warm
diegojfh1000-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_98d35619}
```
picoCTF{d15a5m_t34s3r_98d35619}