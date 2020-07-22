# Comparaciónes y operadores lógicos
## Comparaciones

Como ya vimos los *Booleanos* nos permiten guardar un valor verdadero o uno falso ( true / false), muchas veces **los valores boleanos se usan para tomar decisiones** y son resultado de una comparación.

para hacer una comparación se deben conocer los diferentes operadores de comparación los cuales son los siguientes:

### igualdad (==)
Compara si **un elemento es igual** a otro, hay que tener en cuenta que en caso de realizar una comparación entre un número y string, en caso de representar el mismo número dara como verdadero ya que el **==** no compara el tipo de datos; Para verificar que se trata del mismo tipo de dato asi como el valor, se usa **===** (triple igual), que es el operador que se asegura que tanto el valor como la clase sean iguales

```js
let comparación = 0 == '0'; // comparación = true
let comparaciónEstricta = 0 === '0'; // comparaciónEstricta = false
```

### Mayor que (>)
El operador de 'mayor que' se utiliza para saber si un número es MAYOR que el de la derecha, regresando verdadero en ese caso, se usa de la siguiente manera:

```js
let mayorQue = 5 > 5; //mayorQue = false
```

### Menor que (<)
El operador menor que regresa un valor verdadero en caso de que el número de la izquierda sea menor que el de la derecha
```js
let menorQue = 5 < 5; //menorQue = false
```

### mayor o igual que (>=)
Se usa para saber si un número esta en un rango MAYOR O IGUAL que el de la derecha:
```js
let MayorOIgual = 5 >= 5;
```
### Menor o igual que (<=)
Se usa para saber si un número esta en un rango MENOR o IGUAL que el de la derecha:
```js
let menorOIgual = 5 <=5; //menorOigual = true;
```

### diferente de (!=)
Este operador se usa para buscar un número que sea cualquier otro excepto el de la derecha, se usa de la siguiente manera
```js
let diferenteDe = 5 != 5; //diferenteDe = false
```
## Operadores lógicos

### not (!)
Es el operador más sencillo, simplemente *niega* el valor de una variable booleana, es decir, regresa el resultado opuesto.
```js
let libre = true
console.log(!libre) //false
```

### and (&&)
Al trabajar con booleanos a veces necesitamos hacer desiciones basadas en comparaciónes mas complejas, por ejemplo si quisieramos saber si un número pertenece al rango de números entre 0 y 100 podemos ocupar el operador and y hacer lo siguiente:
```js
let número = 50;
let estaEnRango = número > 0 && número < 100; // estaEnRango = verdadero
```
El operador and (&&) o "Y" en español nos ayuda si queremos que **dos condiciones se cumplan estrictamente**, ya que nos devuelve un  valor verdadero en caso de que el resultado de los valores de cada lado sean ambos verdaderos, regresando un valor falso en caso de que alguno de los dos términos sea falso


### or (||)
El operador *or* es un operador que nos ayuda a obtener un valor verdadero en caso de que **una de las dos condiciones se cumplan**, devolviendo un valor falso solo en el caso que las dos comparaciónes sean falsas por ejemplo, para saber si un número es mayor a 100 o menor que 0 podriamos hacer lo siguiente:

```js
let número = 100;
let es100o0 = número == 100 || número == 0; // es100o0 = verdadero
```
## Uniendo operadores lógicos
En comparaciónes aún mas complejas es muchas veces necesario ocupar más de un operador lógico y es muy común encontrar mas de uno junto, por ejemplo para saber si un usario tiene mas de 1000 puntos y mas de 18 años o es un usario "VIP"  se puede hacer lo siguiente:

```js
let years = 19;
let points = 1000;
let isVIP = false;

let getsReward = (years > 18 && points > 1000) || isVip ; 
```

