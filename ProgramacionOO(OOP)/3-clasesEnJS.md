# Clases en JavaScript
Javascript al ser basado en prototipos técnicamente no tiene "clases" y el instanciamiento de objetos se hace en base a otros objetos previamente creados, sin embargo el uso tan popular de la POO, ha propiciado que la especificación del lenguaje incluya "azúcar sintáctico" para la definición de clases, simplificando la manera de definir e instanciar un objeto.

## Declaración de clases
Para definir una clase en javascript debemos usar la palabra clave `class` seguido de el nombre que queremos asignar a la clase, por ejemplo para crear una clase "bot" haríamos lo siguiente:

```js
class bot{
  // código
}
```
## Método constructor
El método constructor nos ayuda a inicializar los valores (asigar un valor válido) de nuestros objetos a la hora de crearlos, **en JS una clase sólo puede tener un método constructor**, arrojando un error en caso de no ser así, el método constructor se define usando la palabra "constructor" como se muestra a continuación:

```js
class bot{
    constructor (nombre, server) {
        this.name = nombre;
        this.server = server
    }
}
```
Como se puede ver se usa la palabra "this" para hacer referencia al objeto que se está creando. En caso de no ser necesario inicializar valores al crear un objeto se puede omitir el constructor



## atributos y métodos de la clase
Como bien dijimos, las clases se componen de *atributos y métodos*, los cuales son definidos dentro de el bloque de la clase de la siguiente manera:

```js
class Bot{
    id = 0
    owner = ""
    name = ""
    server = ""

    constructor (nombre, server) {
        this.name = nombre;
        this.server = server
    }

    sayHi(){
        console.log('Hi! my name is ' + this.name)
    }

}
```
Como podemos observar se definen los atributos simplemente nombrandolos, sin necesidad de usar la palabra reservada "let" o "const", también se le asigna un valor inicial, esto no es necesario, pero ayuda a tener al menos un valor válido al inicio para evitar errores, sin embargo el método constructor se usa para inicializar valores necesarios.

Los métodos tampoco necesitan de la palabra "function" cuando declaramos métodos de una clase, fuera de esto, la declaracíon de métodos de clase siguen las mismas reglas que la declaración de una función normal.

El método *sayHi* que definimos nos imprime un saludo con el nombre del Bot, como se puede apreciar se pueden referenciar a los atributos de la clase usando la palabra clave "this", que como bien sabemos, referencía al contexto donde se ejecuta el código.

**Nota**: Las arrow functions no referencían al objeto de la clase con la palabra this, por lo que no se utiliza para la definición de métodos de clase que necesiten accesar a atributos de la clase.

## herencia de clases en JS
Para extender la funcionalidad de una clase, se puede crear otra basada en ésta, lo que se conoce como herencia, en JavaScript para indicar que una clase hereda de otra se usa la palabra reservada *extends* seguido del nombre de la clase padre, como se ve en el ejemplo:

```js
    class DiscordBot extends Bot{
        exclusiveProperty = 'exclusive';
        constructor(nombreDiscordBot, serverDiscordBot, owner, id){
            super(nombreDiscordBot, serverDiscordBot)
            this.owner = owner
            this.id = id
            this.sayHi()
        }
        getExclusive(){
            return this.exclusiveProperty
        }
    }
```

Al definir esta clase estamos indicando que se basa o extiende a la clase Bot (definida anteriormente) **obteniendo todas sus propiedades y métodos**, es decir ahora aunque no hemos escrito nada ya contamos con las propiedades: *id, owner, name, server*, Así como el método *sayHi* e incluso el método constructor del padre.

El  método constructor de esta nueva clase tiene acceso a la palabra reservada **super**, que permite hacer el llamado a un constructor de una clase padre, también llamada *superclase*, donde se le deben de pasar los parámetros necesarios y **debe ser la primera línea de código en el bloque del constructor**.

También podemos definir otros atributos y métodos que serán exclusivos de la clase hija como es el caso de *exclusiveProperty* y *getExlusive()*

## Métodos getter y setter
En el ejemplo anterior vimos el método getExclusive() el cual nos regresa el valor de la propiedad *exclusiveProperty*, a este tipo de métodos que nos devuelven el valor de una propiedad de clase se les llama método *getter*, get del inglés obtener y son muy utililzados en OOP.

También existen los métodos setter que son los que se encargan de configurar el valor de un atributo, un ejemplo de un setter y un getter de la misma propiedad sería el siguiente.

```js
class nuevaClase{
    myProp = 0
    getProp(){
        return myProp
    }
    setProp(newVal){
        this.myProp = newVal
    }
}
```

Como puedes ver estos métodos se escriben con "get" o "set" antecedidos de el nombre de la propiedad, aunque no es necesario, pero es una práctica muy común, lo impSortante es saber reconocer que los getters devuelven una propiedad y los setters toman un valor y se lo asignan a la propiedad
