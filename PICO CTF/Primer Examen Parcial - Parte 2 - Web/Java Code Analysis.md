BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/484/bookshelf-pico.zip). Website can be accessed [here!](http://saturn.picoctf.net:62255/).
Hints:
- Maybe try to find the JWT Signing Key ("secret key") in the source code? Maybe it's hardcoded somewhere? Or maybe try to crack it?
- The 'role' and 'userId' fields in the JWT can be of interest to you!
- The 'controllers', 'services' and 'security' java packages in the given source code might need your attention. We've provided a README.md file that contains some documentation.
- Upgrade your 'role' with the _new_ (cracked) JWT. And re-login for the new role to get reflected in browser's localStorage.
# Solucion
Entramos al sitio web usando en email y en contraseña user, le damos clic al libro de la bandera, pero dice que esta bloqueado, por lo cual viendo todo el codigo fuente de java nos damos cuenta que hay que generar un jwt que tenga los datos del administrador para poder entrar como admin y poder ver el libro en el cual esta la bandera, para eso usando un jwt decode online: https://supertokens.com/jwt-encoder-decoder copiamos el jwt que teniamos en la cuenta user y modificamos el payload, en role le ponemos Admin en vez de User, en userId le ponemos 2 en vez de 1, en email le ponemos admin en vez de user y por ultimo en la secret key le ponemos 1234, copiamos el token jwt generador y nos vamos al inspector y en la seccion de almacenamiento->almacenamiento local cambiamos el valor de auth-token y de token-payload con los datos de admin que obtuvimos en jwt y al recargarla la pagina del libro flag nos aparece la bandera.
picoCTF{w34k_jwt_n0t_g00d_6e5d7df5}
# Referencias
- https://supertokens.com/jwt-encoder-decoder
