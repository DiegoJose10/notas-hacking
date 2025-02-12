What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
Hint:
- 1.- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.
# Solucion 1
Cyberchef
```
Input: bDNhcm5fdGgzX3IwcDM1
Recipe: From Base64
Output: l3arn_th3_r0p35
picoCTF{l3arn_th3_r0p35}

```
# Solucion 2
Usando el bash
```
diegojfh1000-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 -d
l3arn_th3_r0p35diegojfh1000-picoctf@webshell:~$ 
picoCTF{l3arn_th3_r0p35}
```
# Solucion 3
Usando python
```
diegojfh1000-picoctf@webshell:~$ python
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
```
# Referencias
- https://es.wikipedia.org/wiki/Base64
