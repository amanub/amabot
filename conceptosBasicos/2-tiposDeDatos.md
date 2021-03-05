# Tipos de datos
Aunque En javavascript no debamos preocuparnos por el tipo de dato al declarar una variable es importante tener en cuenta qué tipo de dato vamos a tratar, ya que el no hacerlo bien puede llevar a errores de ejecucion

Los tipos de datos mas comunes son los Strings, numeros, booleanos, arreglos, funciones y se trataran a continuación

## Strings
Tambien llamadas cadenas de texto, se refiere como su nombre lo dice a texto, el cual es representado como una cadena de caracteres en javascript y en varios lenguajes se puede declarar una variable de tipo String de la siguiente manera 
`let texto = "";`

Todas las cadenas de texto deben estar rodeados de comillas simples o comillas dobles

Con las cadenas de texto podemos hacer una operación llamada concatenación, la cual es simplemente unir dos cadenas de texto, el operador de concatenacion es el "+".
para unir dos textos podemos hacer lo siguiente:
```js
let texto1 = "hola";
let texto2 = "mundo";
let textoUnido = texto1 + texto2; // "holamundo"
```

Aparte de la concatenacion, con los Strings se pueden hacer multiples operaciones tales como dividir cadenas, copiar cadenas, buscar un caracter o texto y sobreeescribirlas.

## Numeros
Pertenecen a la clase "Number", como bien se puede asumir, se refiere a cualquier numero, el cual puede ser un numero entero o un numero decimal, y con el cual se pueden hacer las operaciones de cualquier numero: suma, resta, multiplicacion, division, modulo, exponenciacion, y con ayuda de la libreria de Math, otras funciones mas, como redondear, obtener raiz cuadrada, seno, coseno ,etc...

para declarar un numero se hace de la siguiente manera
`let numero = 0;`



## Booleanos
Son un tipo especial de datos, el cual solo admite dos valores, uno representando verdadero y otro representando falso, es muy util sobre todo combinado con el uso de estructuras de control, un resultado booleano es el producto de una comparacion o una evaluacion logica

la declaracion de los booleanos se hace de la siguiente manera:
`let boleano = true; //puede ser "false"para ser inicializado con un valor falso`


## Arreglos
Son una estructura de datos especial que puede contener mas de un dato, normalmente en otros lenguajes el dato que contienen debe ser de un mismo tipo, pero javascript al no tener tipos permite almacenar diferentes tipos de datos en un arreglo

se puede declarar un arreglo de la siguiente forma:
`let arreglo = [];`

Con los arreglos se pueden hacer diferentes operaciones, dividirlos, invertirlos, buscar elementos, etc, aparte de que javascript nos provee de funciones muy utiles basadas en la programacion funcional como map(), filter() y reduce(), que ayudan a escribir codigo mas limpio

## Funciones
Las funciones son un tipo de dato, que contiene un conjunto de instrucciones que realizan un procedimiento en JS, las funciones son una de las bases de la programacion en javascript y es muy  importante saber definirlas, la forma clasica de guardar una funcion en una variable es:
```js
let funcion = function(){ 
	//codigo
};
```

pero ahora con la especificacion de Ecmascript2017 llegaron las arrow functions (conocidas como lambdas en otros lenguajes) las cuales permiten definir funciones cortas de manera mas concisa de la siguiente manera

`let funcionFlecha = () => //{codigo};`

Las funciones son consideradas como objetos de primera clase, es decir se pueden pasar como parametros a otras funciones

## Objetos
un objeto es una coleccion de propiedades y valores que describen un ente, para declarar un objeto vacio se hace lo siguiente:

`let objetoVacio = {};`

los objetos on la base de la programación en js, en JavaScrip TODO es un objeto, por lo tanto se le dedicara una seccion especialmente enfocada a objetos, 