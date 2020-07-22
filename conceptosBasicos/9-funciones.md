# funciones

Las funciones son una parte muy importante de cualquier lenguaje de programacion, ya que nos permiten encapsular codigo para poder reutilizarlo después, simplemente *llamando* la función y pasando los *parámetros* que nos pide

## Declaracion de una función
Para usar una función primero debemos definir qué es lo que hara y darle un nombre, para así asignarle un espacio en memoria, a esto se le llama declarar una función y se hace de la siguiente manera:

```js
function miFunción(parametro1, parametro2){
	//code
}
```

Podemos ver que **la pabra clave "*function*" se usa para definir la función**, después de esta palabra clave viene el nombre de nuestra función el cual es "miFunción", a continuación podemos ver los parámetros rodeados entre paréntesis, en este caso son dos, separados  por una coma, pero puede tomar mas argumentos o incluso no tomar ninguno, a continuación tenemos la llave de apertura y la llave de cierre en donde ira nuestro código.


## llamar una función
Ahora ya sabemos declarar una función, pero **para poder usarla tendremos que "llamarla" o "invocarla"** y proveerle de los parámetros que nos pida, para esto, se debe usar el nombre de la función seguido de paréntesis donde debemos pasar los argumentos o parámetros necesarios para que la función trabaje, la función anterior se podria llamar de la siguiente manera:

```js
let parametro1 = 'hola '
let parametro2 = 'mundo!'

mifunción(parametro1, parametro2)
```

Como vemos se pone el nombre de nuestra función y después los parámetros. *Se deben proveer todos los parámetros necesarios para que la función se pueda ejecutar correctamente*.


## Valor de retorno

Al llamar a una función se espera que ésta realice un proceso y devuelva un resultado, para posteriormente poder trabajar con los datos que nos arroje.

Para que una función regrese un valor, se usa la palabra clave "return" dentro del bloque de la función, por ejemplo, para crear una función que al ser llamada regrese el texto "hola" seguido de el nombre que le pasaremos al invocarla, haremos lo siguiente:

```js
function holaBot(nombre){
	return "hola " + nombre
}
let miNombre = 'Amabot'
holaBot(nombre) //"hola Amabot"
```

Como nuestra función nos esta regresando un string, **podemos guardar ese valor que nos regresa en una variable** y posteriormente usar esa variable para hacer operaciones con ella, por ejemplo, guardaremos el texto en una variable llamada texto y después la pasaremos a otra función que hemos usado la cual es *console.log()* la cual escribe en consola:
```js
let texto = holaBot(nombre);
console.log( texto ); // "hola Amabot"
```

En el ejemplo anterior se pueden ver dos funciones, una que regresa un valor, la cual es la que definimos, y otra que no, la cual es "console.log", la cual solo realiza el proceso de imprimir en consola, pero si quisieramos guardarl el valor nos arrojaria un valor "undefined", para hacer una función que solo realice un proceso y no regrese un valor, se tiene que omitir la palabra 'return'

## Tipos de retorno

El tipo de retorno se refiere al **tipo de dato que la función nos devuelve**, la cual depende del valor que proceda a la palabra "return", se pueden devolver todo los tipos de datos en una función, incluso otras funciones, si una función no tiene la palabra clave return, se considera de tipo "void" o vacía, y regresara un valor "undefined".




## Todos los caminos conducen a roma

### funciones anonimas
la palabra function puede ser utilizada para crear una función con nombre, sin embargo en js tambien existen las funciones anonimas, es decir, que no tienen nombre, para poder hacer uso de estas funciones deben ser guardadas en una variable, y se hace de la siguiente manera
```
let mifunción = function () {
	//code
}
```
El código anterior nos crea una función, que se guarda en la variable llamada mufunción, para hacer uso de la función, se llama de la misma manera que una función normal, es decir, poniendo el nombre seguido de los argumentos entre paréntesis, en este caso la función se llama usando el nombre de la variable que la contiene.

Cabe mencionar que guardar las funciones anónimas en una variable no es la unica manera de usarlas, y de hecho las funciones anónimas son normalmente usadas como argumentos para otras funciones, este es un patrón muy usado en javascript el cual se llama "callback", pero no veremos a fondo esto en este curso

### Arrow functions

La especificacion del ECMAScript conocida como la *ES6* introdujo una nueva manera de escribir una función a la que se le conoce como arrow function, la cual es una forma mas consisa y algunos dirian que elegante de escribir funciones, y se hace de la siguiente forma
```js
let arrowFunction = (param1, param2) => { 
	//code
}
```
como podemos ver, para definir una función de flecha, no se usa la palabra function, simplemente se omite y se empiezan a listar los argumentos entre paréntesis, obviamente separandolos por una coma, después viene el simbolo "=>" el cual es el que le da el nombre a este tipo de declaración de funciones y después sigue el bloque de código que ejecuta la función

**Si la función solo tiene un argumento, se pueden omitir los paréntesis** y simplemente poner nombre del parámetro, esto reduce un poco el código y lo hace más legible, otra consideración es que si es una función que regresa un valor que puede ser descrita en una sola linea se pueden omitir las llaves del bloque y se regresará el valor que esté después de el simbolo de flecha (=>).

```js
let multiplicarPorDos = numero => numero * 2;

let resultado = multiplicarPorDos( 4 )

console.log( resultado ); // 8
```

Una característica importante de las funciones de flecha es que no ligan la palabra "this" con el contexto de la clase u objeto, sino con el contexto de ejecución desde donde es llmada, esto puede ser beneficioso o no, dependiendo de el tipo de operaciones que se vayan a realizar, las funciones de flecha son utilizadas para procesos en donde solo se requieren los parámetros pasados y no necesita acceder al contexto de "this".


