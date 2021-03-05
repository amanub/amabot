# Aplication Programming Interface
Como vimos en el capitulo anterior, uno de los principios mas importantes de la programacion orientada a objetos es la abstracción, las API son un claro ejemplo de esto ya que son una interface que expone un servicio para que nosotros podamos usarlos, describiendo a los usuarios la manera de interactuar con este sin tener que describir como funciona, lo cual facilita el trabajo de los usuarios (en este caso los programadores).

Ya que las empresas que proveen el servicio son las que determinan el uso de la API, la forma de interacuar varía, sin embargo el principio
es el mismo, enviar un mensaje a una direccion específica siguiendo siguiendo los lineamientos de cómo enviar los parametros y en caso de que nuestra petición sea correcta, recibir un mensaje con los datos solicitados, dichos datos pueden venir en distintos tipos de formatos, siendo JSON, XML y YAML los mas utilizados.

XML era el formato estandar hasta la llegada de JSON, que ha sido extensamente adoptada por los desarrolladores. Se trató el Formato JSON en los conceptos basicos de js

## Peticiones HTTP
Para usar una API se requieren hacer *peticiones* a una dirección, estas peticiones pueden ser de varios tipos, los tipos más comunes de peticiones son:
- GET
  - Se usa para obtener información de un objeto de la base de datos
- POST
  - Se usa para la creación de nuevos objetos, deben indicarsele todos los parámetros necesarios
- PUT
  - Se usa para actualizar un objeto previamente creado, deben indicarsele todos los parámetros
- PATCH
  - Similar al put, se usa para la actualización parcial de objetos
- DELETE
  - Borra un objeto de la base de datos



## Base URL
La URL base o base URL es el punto base de la API donde "viven" los recursos, de esta URL base se desprenden todos los servicios que provee el API, por ejemplo en el caso de Discord, la URL base es: `https://discord.com/api` desde esa url se deprenden los servivios para obtener los Canales, Usuarios, Guilds y demás objetos.

## Endpoint (punto de entrada)
Los endpoits o puntos de entrada son las direcciones donde se enviará la petición que necesitemos a la API para solicitar los recursos necesarios a partir de la URL base, seguido de la dirección del endpoint y el modo de la petición dependerá de lo que querramos realizar, por ejemplo: para obtener información de un canal de discord, hacer una petición del tipo GET al endpoint `/channels/{channel.id}` donde el parámetro que debemos especificar se indica entre llaves, suponiendo que el id de el canal del que requiero información es `123456` nuestra petición quedaría de la forma:

`GET https://discord.com/api/channels/123456`





