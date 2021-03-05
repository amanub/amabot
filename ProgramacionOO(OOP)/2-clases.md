# Clases
Una clase es una abstracción de un ente o idea de la vida real Las clases son un concepto principal de la POO, ya que permiten la reutilización de código y son base de la herencia, una clase se puede pensar como si fuera una plantilla para crear un objeto, la plantilla nos dice qué caracteristicas y comportamientos debe contener el objeto creado.

## Objeto
Se ha hablado de objeto, pero no se ha dado la definición sobre qué es, en la parte de objetos en javascript vimos que un objeto tiene una serie de atributos y métodos asociados a él, pero los objetos se definen como la instacia de una clase, es decir, usamos una clase a forma de plantilla para poder contruir el objeto, el instanciamiento se hace con un método constructor


## Constructor
Al definir los métodos de una clase, existe un  método especial que se le llama "constructor", que se encarga de inicializar los valores de los atributos de un objeto al momento de crearlo, un método constructor *debe tener el mismo nombre que el de la clase*

## Instanciamiento
Se le conoce como instanciamiento al hecho de **crear un objeto en base a la definición de una clase**, para esto se usa el método constructor y se le pasan los parámetros que necesite para crear en nuevo objeto, instanciar significa reservar un espacio de memoria para el objeto, para que pueda ser usado y referenciado desde el código.

## Herencia
La Herencia es un pilar de la OOP que permite la jerarquización y organización de el código de una manera más semántica, puedes hacer que una clase se base de otra, al hacer esto la clase toma o *hereda* los atributos y propiedades de la otra. A la clase que toma los atributos de otra se le conoce como clase hijo/a y a la clase del que ésta se basa se le conoce como clase padre.

## Clases en JavaScript
Javascript al ser basado en prototipos técnicamente no tiene "clases" y el instanciamiento de objetos se hace en base a otros objetos ya creados, que se les denomina prototipos, sin embargo el uso tan popular de la POO, ha propiciado que la especificación del lenguaje incluya "azúcar sintáctico" para la definición de clases, simplificando la manera de definir e instanciar un objeto

para definir una clase en javascript debemos usar la palabra clave "class" seguido de el nombre que queremos asignar a la clase
ej:
```js
class bot{
    
}
```
En la próxima sección se abarcarán más a fondo estos temas enfocados en JS.


