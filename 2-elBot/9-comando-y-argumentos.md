# Comandos y argumentos
Ahora que sabemos cómo diferenciar entre un mensaje normal y un mensaje dirigido al bot podemos hablar de otro obstáculo que se nos presenta, el cual es cómo saber qué comando se requiere ejecutar y los parámetros que debe tener, en el caso de 'hello' es fácil ya que este comando no requiere ninguna información extra y solo debe contener la palabra del comando, pero para hacer otros comandos más interactivos debemos saber qué parte de el mensaje corresponde a los parámetros.

Por ejemplo, queremos crear un comando llamado 'roll' este comando va a hacer que nuestro bot tire dados, de el número de caras que le pidan y el número de veces que le especifiquen, por ejemplo si quisieramos tirar un dado de 5 caras dos veces escribiriamos: `!roll 5 2` lo que haría el comando es simular los dados generando dos números aleatorios en el rango que nos pidieron y devolver el resultado en un mensaje



## Obteniendo los parámetros
Para el comando *!roll* necesitamos obtener los parámetros y para eso debemos de separar el mensaje que el usuario nos envía en dos partes: el nombre del comando y los parámetros, en la sección anterior creamos la cadena que contenía sólo el mensaje omitiendo el prefijo, ahora a esa cadena la debemos separar de acuerdo usando cada espacio, afortunadamente javascript nos provee de varias funciones de cadenas incluidas dentro del lenguaje, en esta caso usaremos el método '.split()' el cual separa una cadena de acuerdo al caracter que le pasemos como parámetro.

`cadena.split(<character>)`
 
 Esta función nos devuelve un arreglo con las palabras que se separaron usando el caracter especificado, ejemplo:

 ```js
let message = 'roll 2 5' //creamos una cadena que contiene el mensaje
let words = message.split(' ') // el caracter que usamos como separador es un espacio (' ')

console.log(words) // ['roll', '2', '5']

 ```
Ya que tenemos las palabras separadas, lo siguiente que toca hacer es almacenar el comando, que es el primer elemento del arreglo, en una variable y los argumentos en otra; Recordando que la variable *words* es un arreglo, nuestro código quedaría de la siguiente forma:

```js
let comando = words[0] // el primer elemento de el arreglo palabras
let arguments = words.splice(1) // regresa los demás elementos 
```
Para obtener los parámetros desde el arreglo de palabras usamos la función '**splice()**' el cual nos pide un índice desde el cual iniciar y nos regresa los elementos a partir de este índice, es similar a la función substr() pero para datos de tipo arreglo.

Con esto hemos obtenido los parámetros que nuestro comando necesita para ejecutarse correctamente.