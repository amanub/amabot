# Entrevista de google
Para reclutar a los desarrolladores que tabajarán en empresas se les aplica un test para comprobar su conocimiento, existen muchas variedades de test y dependen del puesto de trabajo que se planea alcanzar, pero existe uno que se ha ganado mucha fama debido a que las personas dicen que se han usado para reclutar desarrolladores en Google, Facebook, Amazon y Netflix.

## El famoso FizzBuzz
Para practicar el control de flujo con los if y reforzar lo aprendido anteriormente desarrollaremos un ejercicio muy icónico en el mundo de la programación, el problema parece sencillo a primera vista, pero muestra la importancia de el orden en el que hacemos decisiones y cómo se comportan los ifs, el problema es el siguiente:

*Desarrolla un programa que dependiendo de un número que le pasemos diga 'Fizz' si el número es divisible entre de 3, 'Buzz' si el número es divisible entre 5 y 'FizzBuzz' si el número es divisible entre ambos*

Siguiendo el orden del problema podriamos extraer que se nos piden 3 condiciónes
```js
número % 3 == 0 // indica que el número es divisible con el 3
número % 5 == 0 // indica que el número es divisible con el 5
número % 3 == 0 && número % 5 == 0
// indica que el número es divisible con el 3 y el 5
```
si implementamos una solución siguiendo las condiciones extraidas nuestro código quedaria como:
```js
let número = 15;
if (número % 3 == 0) {
	console.log('Fizz');
}
if (número % 5 == 0) {
	console.log('Buzz');
}
if (número % 3 == 0 && número % 5 == 0){
	console.log('FizzBuzz');
}
// Fizz
// Buzz
// FizzBuzz
```
Como podemos ver nuestro programa imprime todas las opciones posibles, ya que el número cumple con todas las condiciones, podemos usar el else if para encadenar las condiciónes y hacer que solo una de ellas se cumpla
```js
let número = 15;
if (número % 3 == 0) {
	console.log('Fizz');
}
else if (número % 5 == 0) {
	console.log('Buzz');
}
else if (número % 3 == 0 && número % 5 == 0){
	console.log('FizzBuzz');
}
// Fizz
```
Ahora nuestro programa ejecuta el primer bloque de código con el que cumple la condición, en este caso imprime 'Fizz' ya que el la primera condición decide si es divisor de 3 o no, en este caso si lo es, por lo que se ejecuta el bloque then correspondiente y se ignoran las demas condiciónes de la estructura

Ya casi tenemos la solución al problema descrito, ahora como vimos, las condiciónes se van evaluando en orden, por lo que para que nuestro programa funcione correctamente se debe alterar el orden de nuestras comparaciones, y sabiendo que un número que cumple con las dos condiciónes debe imprimir 'FizzBuzz' y nada mas, nuestro código quedaria como a continuación
```js
let número = 15;
if (número % 3 == 0 && número % 5 == 0){
	console.log('FizzBuzz');
}
else if (número % 3 == 0) {
	console.log('Fizz');
}
else if (número % 5 == 0) {
	console.log('Buzz');
}
```
Con esto habremos terminado la solución de este problema y con suerte tendremos un trabajo en una de las empresas mas importantes en el mundo de la tecnologia, puedes agradecerme después.

