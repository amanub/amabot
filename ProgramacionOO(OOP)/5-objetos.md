# Objetos
Los objetos son la instancia de una clase, es decir, el alocamiento y creación de una variable que representa un ente de la clase descrita.

## instanciamiento
Declarar una clase no es suficiente para poder trabajar con ella, hace falta crear un objeto que esté basado en la "plantilla" que la clase provee haciendo uso de el *método constructor*, esto se hace con la palabra *new* y se ve de la siguiente manera:

```js

class Bot {
    name ;
    server ;
    constructor(name, server){
        this.name= name
        this.server = server
    }
}

let nombre = "robotin"
let server = "127.0.0.1"

let myBot = new Bot(nombre, server) //instanciamiento

```
En el código anterior se ha creado un ente de la clase "Bot" usando *new* y pasandole los parámetros que requiere el método constructor.

## Modificando Objetos
Cabe mencionar que cada objeto que creemos tiene sus propios valores independientes, lo cuales pueden ser accesados y modificados mediante la sintáxis de punto (.) o la sintáxis de corchetes ([  ]), por ejemplo:

```js
let robotin = new Bot ('robin', '127.0.0.1')
let mrRoboto = new Bot ('Mr. Roboto', '127.0.0.0')

robotin.name = 'robotin'
mrRoboto[server] = '8.8.8.8'

console.log(robotin.name) // 'robotin'
console.log(robotin.server) // '127.0.0.1'
console.log(mrRoboto.name) // 'Mr. Roboto'
console.log(mrRoboto.server) // "8.8.8.8"

```
Aunque JS permite modificar los datos directamente accesandolos a través de sus propiedades, no es la manera más recomendada de modificar los datos de un objeto y se debe hacer uso de los métodos conocidos como "setters" y "getters" que se explican en la sección de clases en js.

Los objetos de JS se tratan más profundidad en la sección de conceptos básicos de JS
