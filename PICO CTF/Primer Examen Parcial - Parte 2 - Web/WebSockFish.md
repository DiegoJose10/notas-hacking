Can you win in a convincing manner against this chess bot? He won't go easy on you! You can find the challenge [here](http://verbal-sleep.picoctf.net:54668/).
Hints:
- Try understanding the code and how the websocket client is interacting with the server
# Solucion
Al entrar al sitio web, podemos jugar ajedrez contra un pez, viendo el codigo fuente, vemos un codigo que crea un WebSocket. Un WebSocket es un protocolo de comunicación que crea una conexión persistente de dos vías entre un cliente y un servidor sobre un solo enchufe TCP. A diferencia de HTML, un WebSocket permite que el servidor y el cliente se envíen datos en cualquier momento sin iniciar una nueva solicitud.

Este script crea un WebSocket que escucha mensajes del servidor y luego actualiza el cuadro de chat azul con el mensaje. Y mas abajo del codigo vemos la funcion sendMessage, la cual envia 
 la evaluación del juego al servidor, que responde con un mensaje para el cuadro de chat. 
 Por lo cual vamos ahora al inspector y abrimos la consola,, de ahi podemos llamar a la funcion sendMessage con el parametro val:  sendMessage("eval 0") de esa manera podemos ir controlando lo que dice el pez y tras usar varias llamadas como: sendMessage("eval -1"), sendMessage("eval -100"), sendMesage("eval -1000"). Finalmente usando sendMessage("eval -1000000) el pez se rinde y nos da la bandera.

picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_50441bef}