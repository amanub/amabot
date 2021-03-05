# Operadores aritméticos

Los operadores aritméticos no son mas que las operaciones que se pueden hacer con los números y que JS integra por defecto, los cuales son suma, resta, multiplicación, división, exponenciación y el operador de módulo.

## Suma

`let suma = 5 + 5;`

El codigo anterior guarda el numero 10 en la variable llamada suma, javascript resuelve la operacion antes de almacenarla en la memoria, esto lo hace con todas las operaciones y las llamadas a funciones

Puedes sumar variables, guardando el resultado en otras variables (WOW).

```js
let a = 5;
let b = 5;
let suma = a + b; //suma = 5 + 5;
```

Una consideración a la hora de hacer las operaciones de suma es verificar que los tipos de datos que estamos usando sean numeros, ya que en caso de tratarse de una cadena de texto el lenguaje aplicaría la operacion de *concatenación* de manera que el siguiente codigo:

```js
let a = "5";
let b = 5;
let suma = a + b // suma = "5" + 5;
```

El resultado de la operacion anterior guardara la cadena "55" en la variable de nombre suma, lo cual no era el número 10 que esperabamos, por lo cual es importante verificar el tipo de datos con el que trabajamos y hacer el *casting de tipos* si es necesario

## Resta
Es la operación inversa de la suma, el símbolo es el "-":

```js
let a = 5;
let b = 5;
let resta = a - b; // resta = 5 - 5;
```

En caso de hacer una resta entre un número y un String el intérprete tratará de convertir el string a número, devolviendo el resultado correcto, en caso de que la cadena no haya podido ser convertida a un número devolvera la cadena 'NaN' que significa *Not a Number* es decir que la operación que se trato de hacer no es correcta.
```js
let resta = '5' - 5; // resta = 10
let resta = 'a' - 5; // resta = NaN
```

## Multiplicación
El operador de multiplicación suma un numero tantas veces como se le diga
se usa de la siguiente manera

```js
let multiplicacion = 5 * 5; // multiplicacion = 25
```

## División
El operador de division resta cierto numero a un numero inicial y devuelve las veces que se puede hacer la operación
```js
let division = 5 / 5; // division = 1
```
## Modulo
Es el **residuo** de la division de un numero por otro, es 0 si el número divide perfectamente al otro
```js
let modulo = 5 % 5; // modulo = 0
```
Exponenciación
La exponenciacion es el proceso de multiplicar un número por sí mismo un
determinado numero de veces (potencia) se puede hacer de la siguiente manera
```js
let potencia = 2**4; // potencia = 16
```
Paréntesis
los paréntesis nos sirven para agrupar operaciones e indicar qué operaciones deben resolverse primero, se puede usar de la siguiente manera
```js
let parentesis = 5 - (5 + 1); // parentesis = 5 - 6
```

## Jerarquia de operaciones matematicas
En las matematicas hay muchas reglas, unas reglas importantes son las que
tienen que ver con el orden en el que se deben resolver las operaciones, ya
que dependiendo de este nuestro resultado puede variar al esperado

El truco más útil para recordar el orden es recordar la palabra **PEMDAS**, ¿qué es PEMDAS? Es un acrónimo que describe el orden en el que las operaciones son resueltas, el cual es el siguiente

- **P**aréntesis
- **E**xponenciación
- **M**ultiplicación
- **D**ivisión
- **A**dición
- **S**ustracción

Es importante tenerlo en cuenta, por casos como el siguiente
```js
let caso1 = 5 + 5 * 2 - 1;
```
En caso de resolverlo ignorando la jerarquia de operaciones nos da el
siguiente resultado
`19`
Pero aplicando las reglas nos da:
`14`


