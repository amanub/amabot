# Casting de tipos
El *casting* se refiere a **pasar un tipo de variable a otro**, aunque javascript nos ayuda en este proceso por su naturaleza *dinamica*, esta misma naturaleza es la que nos puede traer errores inesperados, como el siguiente caso:

```js
let a = '5';
let b = 5.5;
let suma =  a + b; 
console.log(suma) // "55.5"
```

El resutado del codigo anterior nos da "55.5" y se debe a que el lenguaje trata de unir dos textos, por lo que convierte el numero almacenado en *b* a una cadena de texto y hace la operacion de *concatenacion* (unir texto) para evitar eso se usa la funcion *parseInt()* la cual es una funcion que toma un *string* (cadena de texto) y lo convierte a un numero entero (un numero sin la parte decimal), también se usa la funcion parseFloat() si es un número decimal

```js
let textoEntero = '5';
let textoDecimal = '5.5';

let suma = parseInt(textoEntero) + parseFloat(textoDecimal);
console.log(suma) // 10.5
```
Tambien se puede hacer lo contrario, y pasar un numero a un string con la funcion toString() la cual está implementada directamente en el *prototipo de objeto* por lo cual todos los objetos que descienden de Object la tienen

```js
let numeroFavorito = 25;
let frase = 'mi numero favorito es ' + numeroFavorito.toString();
console.log(frase); // 'mi numero favorito es 25
```
