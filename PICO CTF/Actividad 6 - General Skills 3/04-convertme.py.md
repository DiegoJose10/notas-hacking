Run the Python script and convert the given number from decimal to binary to get the flag. [Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
Hints
- Look up a decimal to binary number conversion app on the web or use your computer's calculator!
- The `str_xor` function does not need to be reverse engineered for this challenge.
- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.
- To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
- Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 convertme.py`

# Solucion
Se usa wget para descargar el archivo y para obtener la bandera se escribe la respuesta de una conversion de numero decimal a numero binario usando cyberchef
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2025-02-19 20:23:39--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py.1'

convertme.py.1        100%[=======================>]   1.16K  --.-KB/s    in 0s      

2025-02-19 20:23:39 (60.5 MB/s) - 'convertme.py.1' saved [1189/1189]

diegojfh1000-picoctf@webshell:~$ python3 convertme.py
If 23 is in decimal base, what is it in binary base?
Answer: 10111
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
```
```
Cyberchef
Input:23
Recipes:
From Decimal
To Binary: Byte Length: 1
Output: 10111
```
picoCTF{4ll_y0ur_b4535_722f6b39}
# Referencias

- https://gchq.github.io/CyberChef/