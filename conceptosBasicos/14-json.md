# JSON (Javascript Object Notation)
JSON es una manera de representar objetos complejos, **basado en la sintaxis de JavaScript**, y aunque inició con el lenguaje, la especificación se ha vuelto **independiente del lenguaje**, y muchas aplicaciones usan este formato para intercambiar la informacion, e incluso se ha vuelto un estándar en la industria

Los objetos JSON son simplemente un par de datos tipo *llave-valor*, con diferentes reglas para representar un objeto, un ejemplo de un JSON es el siguiente

```json
{"nombre" : "robotin",
"id": 1,
"hobbies" : ["chat", "play games", "ban players"]
"lobby" : {"id",
	"name" : "amanub's server",
	"members" : [{"name": "amanub",
			"id": 0,
			"role" : "admin"} ,
			{"name": "john",
			"id": 0,
			"role" : "moderator"},
			{"name": "jane",
			"id": 0,
			"role" : "user"}]
	},
"active" : true}
```
Como puedes ver los JSON tienen mucha similitud a un objeto normal de javascript, a excepción de algunas características, la primera es que **el nombre del atributo se escribe como si fuera una cadena** y la segunda es que el formato JSON es solo para datos, por lo que **no podemos tener funciones en un objeto JSON**.

El lenguaje de **javascript nos provee de utilidades para poder convertir los datos en este formato** a un objeto de javascript y vice versa, estas utilidades vienen dentro de un **objeto global llamado apropiadamente "JSON"**, los métodos que nos proveen estas funcionalidades son los siguientes:

```
JSON.parse(<JSON>) // devuelve un objeto de JS
JSON.stringify(<objeto>) // convierte un valor de JS a una cadena JSON
```
Convertir un objeto JSON a un objeto que el lenguaje entienda se le llama "parse" o "parsing" en inglés, y nos permite accesar a los datos de la manera en como se haria con un objeto normal, ya sea por notacion de punto o de corchetes.

suponiendo que llamando al metodo "getData" del objeto "API" se nos devolviera el JSON descrito anteriormente convertido a un objeto nativo podriamos hacer lo siguiente:

```JS
let bot = API.getData();

let id = bot.id; // 1
let name = bot.name; // "robotin"
let channelAdmin = bot.lobbie.members[0]; // "amanub"
let channelName = bot.lobbie.name; // "amanub's server"
let active = bot.active; // true
 
```