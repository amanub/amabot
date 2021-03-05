# Variables en JavaScript
## Que es una variable?
Una variable es un espacio en memoria donde se puede almacenar algún tipo de dato, para posteriormente solicitar el dato y hacer operaciones con este.

Todos los lenguajes de programacion tienen una manera de declarar variables, en javascript existen tres maneras de hacerlo, con las palabras clave "var", "const" y "let", lo cual causa un poco de confusión con respecto a cual se debe usar.

### Que quiere decir declarar una variable?

Declarar una variable es decirle al la computadora que tiene que asignar un espacio de memoria para la variable, es un paso importante que el interprete del lenguaje hace por nosotros, en ese espacio de memoria sera donde se guardaran los datos que necesitemos.

## Como declarar variables?
En JS declarar una variable es muy sencillo, ya que es un lenguaje dinamico y debilmente tipado, no necesitamos especificar el tipo de dato que queremos guardar, el lenguaje se encarga de eso, esta caracteristica puede facilitar la escritura de programas, sin embargo, tambien trae consigo sus desventajas e
inconveniencias a la hora de depurar el codigo.

Sixtáxis: `let|const <<nombre>> = <<valor>>;`
Sixtáxis: `let|const <<nombre>>;`

Ejemplo: `let bot = 'hola';`

## *var* vs *let* vs *const*
Al principio solo existia la palabra clave *var*, pero presentaba algunos comportamientos extraños debido al *hoisting* que hace el interprete de JavaScript, así que en las nuevas especificaciones de *ECMAScript* se definieron *const* y *let*, los cuales tienen diferentes ventajas.

**let** se tiene pensado como el remplazo de **var**, ya que hace que la variable esté **sólo disponible dentro del bloque de código** y se recomienda usar *let* en lugar de *var* en la mayoria de los casos, a menos que se requiera hacer uso del *hoisting*, pero en general hoy en dia es considerado una **mala practica declarar variables con var**.

**const** fue pensado para declarar **valores que no cambiaran**, lo cual evita que una variable importante sea alterada por el programa ya que no se puede cambiar el valor inicial de una constante.





## Qué es un tipo (tipos de variable)?
El **tipo de dato de una variable define qué datos puede aceptar**, javascript al ser un *lenguaje dinámico* puede  guardar cualquier tipo de dato en una variable sin tener que declarar explícitamente su tipo como en otros lenguajes, sin embargo se tiene que tomar en cuenta que existen los tipos de datos, ya que muchos errores pueden ocurrir debido al uso de operaciones en tipos de datos incompatibles.

los tipos de dato primitivos de JavaScript son:
- Undefined
- Boolean
- Null
- Number
- String
- Symbol (nuevo en ECMAScript 6)

para determinar el tipo de una variable podemos usar la palabra clave 'typeof' el cual nos dice el tipo de dato de una variable y se usa de la siguiente
manera:

```js
let numero = 5;
console.log(typeof numero); // "number"
```

Es importante tener en cuenta el tipo de datos con el que estamos tabajar para evitar errores  en la ejecucion de nuestros programas

En secciones posteriores se abordarán más a fondo cada tipo de dato.
