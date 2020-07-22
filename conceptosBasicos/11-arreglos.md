# Arreglos
Un arreglo es un tipo especial de variable el cual nos permite almacenar más de un valor en ella, cada valor almacenado debe estar separado de una coma, a excepcion de otros lenguajes, donde elementos de un arreglo deben ser del mismo tipo, javascript por su naturaleza dinamica admite cualquier tipo de datos en los arreglos, un ejemplo seria el siguiente
```JS
let cosasFavoritas = ["queso", 12, true, function Hi(){return 'Hi'},{name:
'robotin', id: 1}]
```
A pesar de poder tener varios tipos de datos dentro de un arreglo, por lo general los datos son de uno solo, esto facilita el trabajo con arreglos

## Acceder a los arreglos
Para obtener un elemento de un arreglo debemos conocer su indice el cual es asignado por el orden en el que estan, empezando desde 0, se tiene que hacer referencia al arreglo y despues indicar el numero de indice entre corchetes como se muestra a continuacion.
```JS
let numeroFavorito = cosasFavoritas[1]; //12
```
## Arreglos dentro de arreglos
Como vimos podemos tener diferentes tipos de datos en nuestros arreglos, incluso podemos tener arreglos dentro de un arreglo, esto se conoce como arreglo bidimensional o matriz, se podria anotar de la siguiente manera:
```js
let arreglo2d = [[1,2,3],['1','2','3'],[true, false]]
```
si accedemos a los índices de una matriz, accesaremos a el arreglo que contiene desde donde podremos accesar a los datos que contiene, mediante sus índices como en el siguiente ejemplo:

```js
let numeros = arreglo2d[0]; // [1,2,3]
let booleanos = arreglo2d[2]; // [true,false]

let verdadero = booleanos[0]; // true

let textoTres = arreglo2d[1][2]; //"tres"
```
Se puede observar en el ejemplo 3 como se puede acceder a un dato rápidamente, de la misma forma se pueden crear "arreglos dentro de arreglos de arreglos o" arreglos tridimensionales, en teoria pueden haber arreglos dentro de arreglos infinitamente, pero por lo general se trabajan arreglos unidimensionales o vectores y matrices, a menos que tengas que trabajar con graficos en 3d donde obviamente necesitas un arreglo de 3d para realizar las operaciones

## cambiar valores de un arreglo
Para modificar un valor guardado en un arreglo, debemos hacer referencia al
valor que queremos cambiar y con el operador de asignacion darle un nuevo
valor de la siguiente manera
```js
let numerosDeLaSuerte = [5,7,13]

numerosDeLaSuerte[2] = 12;

console.log(numerosDeLaSuerte) // [5,7,12]
```

Los arreglos son especialmente utiles cuando se usan en conjunto con
estructuras de repeticion para recorrer y operar en cada uno de sus elementos,
esto se vera en la seccion de estructuras de repeticion.

Operaciones comunes con arreglos
Al trabajar con arreglos se encuentra que muchos procedimientos se repiten por
lo que se han integrado metodos dentro de la clase "Array" que es a la que
pertenecen los arreglos, tales operaciones son:


- consultar el tamaño de un arreglo
`arreglo.length`

- Añadir un elemento al final de un arreglo
`arreglo.push(<<nuevo elemento>>);`

- Añadir un elemento al inicio
`arreglo.unshift(<<nuevo elemento>>);`

- Eliminar el ultimo elemento
`arreglo.pop();`

- Eliminar el primer elemento
`arreglo.shift()`

- Obtener el indice de un elemento que se encuentre en la lista
`arreglo.indexOf(<<elemento>>)`

- eliminar un rango de elementos de una lista
`arreglo.slice(<<indiceInicial>> , <<IndiceFinal>>)`


Nota: estos metodos regresan valores, los cuales pueden ser guardados
en una variable.


