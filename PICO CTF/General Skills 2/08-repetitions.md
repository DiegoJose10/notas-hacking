Can you make sense of this file? Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
Hints:
- Multiple decoding is always good.
# Solucion

Se usa wget para descargar el archivo, luego se usa cat para leerlo, despues se tiene que decodificar a base64 usando base64 -d, pero se tiene que repetir muchas veces para que se pueda decodificar por completo, en este caso se usa 6 veces
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/471/enc_flag
--2025-02-17 23:31:06--  https://artifacts.picoctf.net/c/471/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag              100%[=======================>]     349  --.-KB/s    in 0s      

2025-02-17 23:31:06 (16.3 MB/s) - 'enc_flag' saved [349/349]

diegojfh1000-picoctf@webshell:~$ ls
Addadshashanammu      README.txt  file  salida  strings    warm
Addadshashanammu.zip  enc_flag    flag  static  strings.1
diegojfh1000-picoctf@webshell:~$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFpSV0VKWVZGVmtNRTVHV2tWU2JYUlVDbUpXV25sVWJGcHZWbGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
diegojfh1000-picoctf@webshell:~$ base64 -d enc_flag
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlZRWEJYVFVkME5GWkVSbXRUCmJWWnlUbFpvVldGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
diegojfh1000-picoctf@webshell:~$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
