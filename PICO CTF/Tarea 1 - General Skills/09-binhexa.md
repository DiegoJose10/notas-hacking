How well can you perfom basic binary operations? Start searching for the flag here `nc titan.picoctf.net 62645`
# Solucion
Se conecta al puerto dado en la descripcion, para obtener la bandera se realizan varias operaciones binarias y una conversion de binario a hexadecimal, para obtenerlas se utilizara una calculadora binaria de la pagina de lambdatest
```
diegojfh1000-picoctf@webshell:~$ nc titan.picoctf.net 62645

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 11001001
Binary Number 2: 10011110


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11011111
Correct!

Question 2/6:
Operation 2: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 1001111
Correct!

Question 3/6:
Operation 3: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 111110000001110
Correct!

Question 4/6:
Operation 4: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 110010010
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10001000
Correct!

Question 6/6:
Operation 6: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101100111
Correct!

Enter the results of the last operation in hexadecimal: 167

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}
```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}

# Referencias

- https://www.lambdatest.com/free-online-tools/binary-calculator
