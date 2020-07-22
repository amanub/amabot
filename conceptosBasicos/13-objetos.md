# Objetos en javascript
Son pieza fundamental de la programacion en JS, ya que *todo es un objeto en JavaScript* y por lo tanto es importante saber como están estructurados; los objetos son una coleccion de "propiedades" o "atributos" separados por comas, las cuales se componen de un nombre de propiedad y un valor en el fomato `"<<nombre>> : <<valor>>"` las propiedades de un objeto en JS pueden ser de cualquiera de los tipos disponibles en el lenguaje, veamos un ejemplo:
```js
let bot = {
	name: "amanub",
	id: 1,
	isConected: true,
	sayHi: function (){
		console.log("Hi, my name is " + this.name
	}
}
```
## Accesar a propiedades de los objetos
Las propiedades de un objeto se pueden accesar, haciendo referencia al objeto
y despues colocar un punto, seguido de el nombre de la propiedad, por ejemplo,
para accesar al nombre de nuestro objeto "bot" haremos lo siguiente
```js
let nombre = bot.name ;
console.log (nombre) //"amanub"
```
Otra forma de acceder a estas propiedades es con la notación llamada notación de corchetes, ya que sorpresa, se usan corchetes para acceder a las propiedades, entre los corchetes se ecribe el nombre de la propiedad que se necesita, Ejemplo:
```js
let edad = bot["id"]; // 1
```
Se puede usar cualquier notacion, pero la notación de punto es mas comunmente utilizada en programacion orientada a objetos, el cual es el paradigma que usaremos (no te preocupes, se dedicará un capitulo especial a este tema)

Como tambien vimos una propiedad puede ser una función, cuando una función pertenece a un objeto, se le llama método, para usar un método se hace de la misma forma que una función normal, simplemente se referencia y se le pasan los parámetros necesarios.
```js
bot.sayHi() // "Hi, my name is amanub"
```
El metodo *sayHi* muestra un mensaje con el nombre del bot, la palabra "this" hace referencia al objeto bot, para despues acceder a la propiedad "name" del objeto, Esto no funcionaria con una función de flecha, ya que al usar "this" en el cuerpo de la función no se referenciaria al bot, ya que como vimos las
funciones de flecha no ligan el contexto a "this".

Como una propiedad puede ser de cualquier tipo aceptado por JS, los objetos pueden contener objetos dentro de sí, lo que habilita la posibilidad de hacer estructuras muy complejas con objetos.

## Modificar las propiedades de un objeto
Para modificar un valor ya establecido en un objeto de js, se tiene que referenciar dicha propiedad y usando el operador de asignacion se establece el nuevo valor a guardar:
```js
bot.name = "robotin";
```
Esta linea de codigo ha accesado a la propiedad name de el objeto bot y ha asignado el texto "robotin" como nuevo valor

Aparte de poder modificar un valor ya existente, podemos incluso definir nuevas propiedades para el objeto de la siguiente manera:
```js
bot.phrase = 'Siempre hay alguien peor que tú';

bot["helloWorld"] = function () {
	console.log('Hola Mundo!")
} 
```
Como se puede apreciar, se puede usar cualquiera de las notaciones ya descritas.


