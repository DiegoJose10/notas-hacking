Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.
# Solucion 
Se descarga el archivo flag y se utiliza cat flag
```
diegojfh1000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
--2025-02-12 18:46:17--  https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                        100%[=========================================>]      34  --.-KB/s    in 0s      

2025-02-12 18:46:17 (12.9 MB/s) - 'flag' saved [34/34]

diegojfh1000-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
```
