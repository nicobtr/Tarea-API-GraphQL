# Tarea Parte I - API

## ¿Qué API elegiste y por qué?

Elegí dos APIs, la primera es la de Studio Ghibli, la elegí porque me he visto varias de sus películas y en general me gusta todo su contenido, también porque consideré que sería buena opción para construir las request básicas dado que tiene varios endpoints interesantes. (CRUD).
La otra que elegí fue la API de El Señor de los Anillos, soy fan de los libros y las películas de ese universo de fantasía de Tolkien, también porque vi que era una de las opciones más viables para implementar algunas request usando un JWT o Bearer Token. 

## ¿Qué datos devuelve?

Ambas APIs devuelven JSON (JavaScript Object Notation), y en los endpoints que probé la API de Studio Ghibli devuelve la lista de películas que han hecho con un id único, el titulo en inglés, el titulo original, una descripción, el año de salida, entre otros campos. 
Por otro lado, la API de El Señor de los Anillos devuelve las peliculas que se han realizado sobre este universo exhibiendo un id único, el nombre de la película, la duración en minutos, los premios ganados, entre otros. También devuelve los personajes cada uno con su id, nombre, raza, género, etc. 

## ¿Usa token? ¿Qué tipo?

La API de El Señor de los Anillos usa un Bearer Token. A diferencia del lab, aquí no hay un flujo de login mediante POST — el token se obtiene registrándose manualmente en la web y se usa directamente en el header Authorization: Bearer <token> de cada request.

## ¿Qué aprendiste diferente a JSONPlaceholder?

Aprendí principalmente que se pueden filtrar datos del JSON de un response por medio de los Query Params, de esta manera se recibe solo un JSON con la información específica que se necesita. 
También aprendí como manipular un token para hacer request, esto en Jsonplaceholder no estaba.

## Requests

### CRUD
#### GET Películas
[captura request + respuesta]
[captura test results]
...

### Query Params
...

### Auth JWT (LOTR)
...

