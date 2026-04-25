# Tarea Parte II - GraphQL

## ¿Qué diferencia encontraste vs REST?

Encontré varias diferencias. En primer lugar, GraphQL no implementa de forma semántica los métodos HTTP ni sus códigos de estado. A diferencia de REST, todas las requests se realizan usando el método POST, aunque aquí no significa que se esté creando un recurso — simplemente es el método que usa GraphQL para enviar sus queries. Además, los códigos de estado casi siempre son 200 OK incluso cuando hay errores; en ese caso el error viene dentro del cuerpo del JSON en un campo errors, no en el código de estado.
Otra diferencia relevante es que GraphQL usa un único endpoint para acceder a todos los recursos, mientras que en REST cada recurso tiene su propio endpoint. La especificación de qué datos se quieren no va en la URL sino en la query del body.
Por último, GraphQL permite anidar información relacionada dentro de una misma query, lo que evita tener que hacer múltiples requests como ocurre en REST. Por ejemplo, en una sola query se puede pedir un continente junto con todos sus países y las monedas de cada uno. 

## ¿Cuántos requests REST necesitarías para reemplazar tu query más compleja?

La query más compleja fue la del continente con sus países, que devuelve Sudamérica con todos sus países y los campos de cada uno en una sola request. En REST necesitaría al menos dos: una para obtener el continente y otra para obtener los países de ese continente. Si además quisiera los idiomas de cada país, necesitaría una request adicional por cada país, lo que podrían ser varias requests, probablemente más de 10 para obtener la misma información. 

## ¿En qué proyecto real usarías GraphQL?

Lo usaría en una aplicación móvil donde el consumo de datos importa, por ejemplo una app de viajes que muestre información de países, ciudades y atracciones. Que no pida más datos de los que necesita para no hacer la conexión lenta.

## Requests y test

#### Mostrar países
<img width="1387" height="912" alt="image" src="https://github.com/user-attachments/assets/7657debd-6011-4025-8760-4fa926ce968d" />
<img width="1389" height="770" alt="image" src="https://github.com/user-attachments/assets/9ea40ce9-eedd-41e5-92a6-78bdeebf272d" />

#### Un país específico - Query con filtro por argumento
<img width="1392" height="717" alt="image" src="https://github.com/user-attachments/assets/0ca382c1-0e89-4c3b-a80c-09efce7cb421" />
<img width="1381" height="723" alt="image" src="https://github.com/user-attachments/assets/8e42ca15-3324-4d63-b192-ea520a41096a" />

#### Un país y sus idiomas - Query anidada
<img width="1380" height="829" alt="image" src="https://github.com/user-attachments/assets/41c54d88-3bd3-4686-8d36-081cb9d2ff5e" />
<img width="1397" height="720" alt="image" src="https://github.com/user-attachments/assets/4f6b9c8e-e70d-459a-b568-6813d4f91b8c" />

#### Mostrar continentes
<img width="1387" height="907" alt="image" src="https://github.com/user-attachments/assets/ba7a212c-3a36-4bf4-aaff-6d869564fbab" />
<img width="1392" height="745" alt="image" src="https://github.com/user-attachments/assets/1e5da88e-11c8-47a0-a6d8-cb84106de2b5" />

#### Un continente con sus países - Query anidada
<img width="1388" height="903" alt="image" src="https://github.com/user-attachments/assets/40628f8d-8d85-4b82-a5db-709c7d809dbc" />
<img width="1404" height="773" alt="image" src="https://github.com/user-attachments/assets/6c734e75-29bf-476d-952e-bb20fe08a001" />
