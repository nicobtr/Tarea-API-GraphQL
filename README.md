# Tarea Parte I - API

## ¿Qué API elegiste y por qué?

Elegí dos APIs, la primera es la de Studio Ghibli, la elegí porque me he visto varias de sus películas y en general me gusta todo su contenido, también porque consideré que sería buena opción para construir las request básicas dado que tiene varios endpoints interesantes. (CRUD).
La otra que elegí fue la API de El Señor de los Anillos, soy fan de los libros y las películas de ese universo de fantasía de Tolkien, también porque vi que era una de las opciones más viables para implementar algunas request usando un JWT o Bearer Token. 

## ¿Qué datos devuelve?

Ambas APIs devuelven JSON (JavaScript Object Notation), y en los endpoints que probé la API de Studio Ghibli devuelve la lista de películas que han hecho con un id único, el titulo en inglés, el titulo original, una descripción, el año de salida, entre otros campos. 
Por otro lado, la API de El Señor de los Anillos devuelve las peliculas que se han realizado sobre este universo exhibiendo un id único, el nombre de la película, la duración en minutos, los premios ganados, entre otros. También devuelve los personajes cada uno con su id, nombre, raza, género, etc. 

## ¿Usa token? ¿Qué tipo?

La API de El Señor de los Anillos usa un Bearer Token. A diferencia del lab, aquí no hay un flujo de login mediante POST, el token se obtiene registrándose manualmente en la web y se usa directamente en el header Authorization: Bearer <token> de cada request.

## ¿Qué código de estado recibiste en cada request?

En la mayoria de los request recibí el código de estado 200 OK el cual significa que la request fue recibida y procesada de forma exitosa por el servidor, esto sucedió para la mayoría de los GET, para el DELETE, PUT y PATCH.
Para el request con POST recibió el código de estado 201 Created indicando que el recurso que la request fue procesada de forma exitosa y el recurso se creó en el servidor (aunque realmente no se creó porque es una API de prueba). 
Para la request GET /movie con la API de El Señor de los Anillos sin utilizar token, el servidor me devolvía en el response un código de estado 401 Unauthorized indicando que no estoy autenticado y por lo tanto no puedo acceder al recurso porque el servidor no sabe quien soy. 

## ¿Qué aprendiste diferente a JSONPlaceholder?

Aprendí principalmente que se pueden filtrar datos del JSON de un response por medio de los Query Params, de esta manera se recibe solo un JSON con la información específica que se necesita. 
También aprendí como manipular un token para hacer request, esto en Jsonplaceholder no estaba.

## Requests

### CRUD
#### Películas
<img width="1360" height="908" alt="image" src="https://github.com/user-attachments/assets/d367a2b2-4966-4e8d-82b7-d7df1a861afe" />

#### Filtrar ID película
<img width="1363" height="907" alt="image" src="https://github.com/user-attachments/assets/0a217213-1ca7-4501-8d4c-355f42ee2df4" />

#### Crear película
<img width="1361" height="914" alt="image" src="https://github.com/user-attachments/assets/aff8c51f-4971-4e55-8f83-ff2ad0c8cfb5" />

#### Actualizar película
<img width="1374" height="920" alt="image" src="https://github.com/user-attachments/assets/30fca2aa-c117-48ed-a602-3344bd62a303" />

#### Actualizar solo un campo
<img width="1369" height="925" alt="image" src="https://github.com/user-attachments/assets/d1653e85-77cf-44f1-bdb2-1176953cd03d" />

#### Borrar película
<img width="1368" height="908" alt="image" src="https://github.com/user-attachments/assets/16a13126-c5ed-404d-bbf7-3cbdae036d81" />

### Query Params

#### Solo tres películas
<img width="1368" height="916" alt="image" src="https://github.com/user-attachments/assets/d670b136-bad4-4355-9ec5-8e63e08b6cdf" />

#### Una película con cuatro campos (y tests)
<img width="1376" height="735" alt="image" src="https://github.com/user-attachments/assets/b01bae0f-d1db-4f13-9742-a47e4ae2a931" />
<img width="1361" height="745" alt="image" src="https://github.com/user-attachments/assets/c05a9b0d-cdc3-41d8-a059-967ede3670bf" />

### Auth JWT

#### GET sin token
<img width="1372" height="529" alt="image" src="https://github.com/user-attachments/assets/5fb74599-2d06-4418-8355-f2100c05893b" />

#### Mostrar películas (y tests)
<img width="1440" height="903" alt="image" src="https://github.com/user-attachments/assets/170eb62a-c7a3-4531-9680-4117658e213f" />
<img width="1438" height="600" alt="image" src="https://github.com/user-attachments/assets/d2b8e413-0d1c-4e90-8eaa-0380ce310479" />

#### Mostrar personajes
<img width="1434" height="907" alt="image" src="https://github.com/user-attachments/assets/0c392818-ca3c-4d7a-96b2-49f4af6fa5ff" />
