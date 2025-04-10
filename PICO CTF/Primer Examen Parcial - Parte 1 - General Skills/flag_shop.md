There's a flag shop selling stuff, can you buy a flag? [Source](https://jupiter.challenges.picoctf.org/static/dd28f0987f28c894f35d5d48564c3402/store.c). Connect with `nc jupiter.challenges.picoctf.org 44566`.
Hints:
- Two's compliment can do some weird things when numbers get really big!
# Solucion
Abrimos el programa, y vemos que el servicio es una tienda simple. 

La segunda opcion ofrece banderas falsas y la bandera real. La bandera real cuesta `100000`dólares, y sólo empezamos con `1100`. Vemos que cada bandera falsa cuesta `900`dólares y resta el costo total de nuestro saldo de cuenta. Pero que pasaria si total_cost es negativo? Entonces añadimos `total_cost`a nuestro balance y si `total_cost`es lo suficientemente negativo, entonces podemos obtener un gran saldo de cuenta. Para obtener negative total cost se usa un desbordamiento entero para asi desbordar el total_costvariable y aumentar el saldo de nuestra cuenta. Necesitamos un total_cost que es un gran número negativo, pero no demasiado grande que también desborde nuestro account_balance. Un ejemplo seria 3000000, el cual funciona muy bien para las banderas falsas que queramos comprar.
Para hacer eso se usan las siguientes opciones:  2, 1, 3000000, 2, 2 y 1
picoCTF{m0n3y_bag5_68d16363}