# Bucles en JS
Un bucle es una estructura de codigo que nos permite **repetir la ejecucion de un bloque de codigo mientras se cumpla una condicion**, uno de los bucles mas sencillos es el bucle while, con el cual tambien aprenderemos algunas características de estos 

## while... do...
un ciclo while necesita una condicion la cual decidira si se ejecutara el bloque en caso de ser verdadero o ignorara el bloque en caso de ser falso; Por ejemplo, para imprimir los numeros del 1 a un numero que el usuario indique, usando un bucle while se haria lo siguiente
```js
let contador = 1;
let condicion = 100;

while ( contador <= condicion ) {
	console.log(contador);
	contador++;
}
//0
//1
//2
//...
//100 
```
Es importante mencionar que **los bucles tienen que terminar en algun momento**, de lo contrario se creara lo que se conoce un *bucle infinito* y consumirá los recursos del cpu
causando que se congele o deje de funcionar el programa

Las estructuras de repeticion son muy utiles, imaginate tener que escribir 100 veces el mismo codigo, aparte de ser ineficiente, puede que el numero que nos pasen sea otro, por lo que copiar y pegar código 100 veces no funcionaria.

como podemos distingir, el bucle o loop necesita de 3 mecanismos, la condicion, un contador y una manera de modificar el contador para no crear el bucle infinito

Estos mecanismos se pueden apreciar mejor en el siguiente ciclo el cual es el for

## For

**El ciclo *for* es el ciclo mas usado**, su sintaxis es la siguiente:
```
for (<inicializacionContador> ; <condicion> ; <modificacionContador>){
	//codigo a repetir
}
```
se muestra un ejemplo de una traducción del while visto anteriormente a una estructura for:
```js
let condicion = 100;

for( let contador = 0 ; contador <= codicion ; contador++){
	console.log(contador)
}
```
Se pueden observar los 3 elementos de un bucle los cuales están separados por un ";" y se encuantran entre los paréntesis del for

## Do... While
Existe otro bucle el cual es el bucle *do... While* que es básicamente un ciclo while, pero donde *el código se ejecuta antes de verificar la condición del ciclo*, por lo que se garantiza que el código se ejecutará al menos una vez, la sintaxis en la siguiente:
```
do{
	//code
}
while(<<condicion>>)
```
Existen otros tipos de bucles, los cuales se verán en la sección de *bucles y arreglos*