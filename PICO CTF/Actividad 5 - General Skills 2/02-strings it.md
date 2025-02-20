Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
Hints:
- [strings](https://linux.die.net/man/1/strings)
# Solucion

Se usa wget junto con el enlace del archivo para descargarlo, el archivo se llama strings, asi que se usa el comando strings para buscar las strings del archivo y  se usa el comando grep para filtrar las cadenas que aparezcan con picoCTF, ya que ahi se encontrara la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
--2025-02-17 23:07:25--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings.1'

strings.1             100%[=======================>] 757.84K  1.86MB/s    in 0.4s    

2025-02-17 23:07:25 (1.86 MB/s) - 'strings.1' saved [776032/776032]

diegojfh1000-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_827aee91}
```
picoCTF{5tRIng5_1T_827aee91}