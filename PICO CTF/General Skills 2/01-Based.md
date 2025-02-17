To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.
Hints:
- I hear python can convert things
- It might help to have multiple windows open.
# Solucion
Se conecta al servidor dado en la descripcion y nos da una serie de preguntas sobre conversiones de sistemas numericos a palabras, asi que una forma de resolverlo es usando cyberchef
```
diegojfh1000-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
map
Please give the 01101101 01100001 01110000 as a word.
...
you have 45 seconds.....

Input:
map
Please give me the  146 141 154 143 157 156 as a word.
Input:
falcon
Please give me the 6c697a617264 as a word.
Input:
lizard
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}
```

Resolviendo con cyberchef:
```
Input:  01101101 01100001 01110000
	    146 141 154 143 157 156
	    6c697a617264
Recipe: From Binary
		From Octal
		From Hex
Output: map
	    falcon
	    lizard
```
picoCTF{learning_about_converting_values_00a975ff}
# Referencias

https://gchq.github.io/CyberChef/