Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)
Hints:
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses
# Solucion

```
HTTP define un conjunto de **métodos de petición** para indicar la acción que se desea realizar para un recurso determinado. Aunque estos también pueden ser sustantivos, estos métodos de solicitud a veces son llamados _HTTP verbs_. Cada uno de ellos implementan una semántica diferente, pero algunas características similares son compartidas por un grupo de ellos.

El método `GET` solicita una representación de un recurso específico. Las peticiones que usan el método `GET` sólo deben recuperar datos.

El método `HEAD` pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.

El método `POST` se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

El modo `PUT` reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

El método `DELETE` borra un recurso en específico.

El método `CONNECT` establece un túnel hacia el servidor identificado por el recurso.

El método `OPTIONS` es utilizado para describir las opciones de comunicación para el recurso de destino.

El método `TRACE` realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.

El método `PATCH` es utilizado para aplicar modificaciones parciales a un recurso.
```

Se nos proporciona una página web que muestra dos colores de fondo: azul y rojo, El botón rojo utiliza una petición GET y el azul usa una petición POST. Pero no hay nada mas, como el nombre del reto incluye HEAD, podriamos intentar haciendo una petición HEAD con curl en la consola:
```
curl -I http://mercury.picoctf.net:21939
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
Content-type: text/html; charset=UTF-8
```
Y al hacerlo nos muestra la bandera:
picoCTF{r3j3ct_th3_du4l1ty_6ef27873}

# Referencias

- https://developer.mozilla.org/es/docs/Web/HTTP/Reference/Methods