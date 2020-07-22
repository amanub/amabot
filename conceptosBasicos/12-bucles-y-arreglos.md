# Bucles y arreglos
Es común ver que un bucle es utilizado para recorrer y operar sobre un arreglo, ya que los bucles nos permiten iterar sobre los indices de éste, permitiendonos accesar a cada elemento

como podemos recordar, los arreglos son colecciones de datos, y en el caso e javascript pueden ser diferentes tipos de datos, es facil trabajar manualmente con un arreglo pequeño, pero conforme el tamaño del arreglo aumenta se vuelve cada vez más complicado hacerlo de esta forma y se hacen necesario maneras de trabajar con arreglos, por lo que el lenguaje ofrece una gran variedad de herramientas para trabajar con la clase Array 

## Método tradicional
Éste método consiste en definir un contador, que usará para recorrer todos los indices del array, el código se ejecutará mientras el contador sea menor que el número de elementos del arreglo, se desarrollará en el siguiente ejemplo con un bucle while

supongamos que queremos multiplicar cada uno de los numeros de un arreglo por dos y guardarlo en otra variable, esto se haría de la siguiente manera:
```js
let arreglo = [5,4,7,2,9]
let dobles = []

let contador = 0
while(contador < arreglo.length){
    dobles.push( arreglo[contador] * 2 );
    contador = contador + 1;   
}

console.log(dobles) // [10,8,14,4,18]
```

como podemos ver, la condicion dentro de nuestro while nos dice que ejecutaremos el código dentro de las llaves, mientras el numero que contenga "contador" sea menor que el numero total de elementos en el arreglo, el cual obtenemos mendiante la propiedad "length" la cual tienen todos los elementos de la clase Array (arreglos)

dentro de las llaves después de la condición se puede ver el código que se ejecutará cada vez que pase la condición, se puede observar que usamos el método push(), el cual vimos en la sección de arreglos y nos permite insertar un nuevo elemento a un arreglo, en este caso le añadiremos un elemento nuevo a "dobles" , el elemento que añadimos es uno de el arreglo cuyo índice estáa determinado por el valor que "contador" tenga en el momento.

como recordamos, necesitamos una manera de modificar el contador, para no quedar en un bucle infinito, lo cual hacemos con la linea "contador = contador + 1", la cual se encarga de sumar el valor de la variable mas uno.

el bucle empieza desde el contador valiendo 0 hasta 4, ya que la condición dice que sea menor que el numero de elementos (5), y añade el elemento en la posicion que contador indique multiplicandolo por dos, es importante recordar que los indices de los arreglos comienzan de 0.

## Método for
Tomando como ejemplo el mismo ejercicio, en forma de for quedaría de la siguiente manera.
```js
let arreglo = [5,4,7,2,9]
let dobles = []

for(let contador = 0 ; contador < arreglo.length; contador++){
    dobles.push( arreglo[contador] * 2 );
}

console.log(dobles) // [10,8,14,4,18]
```
como vemos el código de la estructura for es más conciso, pero cuenta con exactamente las mismas partes que el bucle while, todas dentro de el paréntesis, haciendo solo la operación en el bloque de código.

## metodo foreach
Este método es realmente un método ya que está integrada en la clase Array, todos los arreglos cuentan con el método forEach() y se usa de la siguiente manera:
```
<<nombreArreglo>>.forEach(function callback (<<currentValue>>, <<index>>, <<array>>) {
    // tu operación
}[, thisArg]);
```
El método forEach trabaja a base de una función llamada genéricamente "callback", la cual se ejecuta en cada uno de los elementos del arreglo, el "callback" de el método forEach nos da tres parámetros, podemos ocupar 1 o los 3, el primer parámetro "currentValue" es el elemento que el arreglo contiene, el segundo (index) es el índice del elemento del arreglo y el tercer parámetro es una referencia al arreglo sobre el que se itera

como el "callback" es una función, también puede ser declarado como una función de flecha o arrow function, aplicandosele las caracteristicas mencionadas en la sección de "Funciones" de este curso

siguiendo con el mismo ejemplo un forEach usando una función de flecha quedaría de la siguiente manera

```js
let arreglo = [5,4,7,2,9]
let dobles = []

arreglo.forEach( (numero, indice) => {
    dobles.push(numero * 2);
    } )
```

como explicamos, forEach usa un "callback" para hacer su trabajo, en este caso usamos dos de los tres parametros que nos provee, el elemento (numero) y el indice , el cual ocupamos para meterlo en el arreglo con el método push() .



## Map
este método también pertenece a la clase Array y usa un "callback" exactamente igual al que se usa en el forEach, con la diferencia que la función map() nos regresa un nuevo arreglo del mismo tamaño, que contendrá los resultados de la llamada a la función "callback", continuando con el ejercicio el código quedaría de la siguiente forma:

```js
let arreglo = [5,4,7,2,9]
let dobles = arreglo.map( numero => numero * 2 )
```
como la función map() regresa un resultado el cual es el arreglo modificado, guardaremos ese resultado dentro de "dobles", llamamos al map sobre el arreglo y en el callback utilizamos el elemento solamente, en este caso no es necesario hacer push del elemento a un arreglo, simplemente regresarlo del callback con return, lo cual nos produce el mismo resultado que los métodos anteriores.

 
