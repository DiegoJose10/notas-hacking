Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/37821/` ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821
Hints:
- Never trust the client
# Solucion
Le damos click derecho a la pagina web y le ponemos inspeccionar, nos vamos a la pestaña de depurador y ahi aparece la pista de la bandera, la cual es la siguiente:
if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'a3c8') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_1') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == '9}') {
Tenemos que ir ordenando la bandera en base a la posicion que aparece al lado de split, lo hacemos de forma ascendente con cada valor que aparece, asi obteniendo y ordenando la bandera da como solución:
picoCTF{no_clients_plz_1a3c89}
