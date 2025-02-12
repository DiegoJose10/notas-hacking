Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.
Hints:
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
# Solucion
- Me conecte por netcat, luego mande la salida a un archivo y luego busque la bandera
```
diegojfh1000-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 > salida

diegojfh1000-picoctf@webshell:~$ cat salida | grep pico
picoCTF{digital_plumb3r_5ea1fbd7}

```
- Me conecte y redirigi la salida al grep para encontrar la bandera
```
diegojfh1000-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 | grep pico
picoCTF{digital_plumb3r_5ea1fbd7}
```