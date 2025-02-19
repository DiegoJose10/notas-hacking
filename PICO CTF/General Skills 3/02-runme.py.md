Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
Hints
- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
- To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
- Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!
# Solucion
Se descarga el archivo usando wget y se ejecuta con el comando python3
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-02-19 20:16:02--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py              100%[=======================>]     270  --.-KB/s    in 0s      

2025-02-19 20:16:02 (137 MB/s) - 'runme.py' saved [270/270]

diegojfh1000-picoctf@webshell:~$ ls
Addadshashanammu      big-zip-files        enc_flag  files.zip  salida   strings.1
Addadshashanammu.zip  big-zip-files.zip    file      flag       static   warm
README.txt            big-zip-files.zip.1  files     runme.py   strings
diegojfh1000-picoctf@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
```
picoCTF{run_s4n1ty_run}