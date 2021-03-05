# Qué es la programación?
La programación es simplemente darle instrucciones a la computadora, como una receta, para que realice un trabajo, a estas recetas se les llaman *algoritmos* en el mundo de las ciencias computacionales, y simplemente es una serie de pasos en orden secuencial, escrito en un *lenguaje de programacion* que es un leguaje que puede entender la computadora.

JavaScript es un lenguaje de programación *interpretado*, basado en prototipos y que empezó como el primer lenguaje para la web, es un lenguaje de tipado dinámico (también llamado tipado débil) y las especificaciones de su implementación está dictada por el ECMAScript (ES1, ES2, ES3 ... ES10) y es regulada por la W3C (World Wide Web Consortium).

## NodeJS
JavaScript comenzó como el lenguaje para la web, por lo que sólo podía ser ejecutado en el navegador, pero con la llegada de Node en el 2009, eso cambió, ya que es un entorno de ejecución de JavaScript que nos permite correr el código desde nuestra computadora sin tener que usar el navegador, permitiendolo usar en servidor.

Para esta guía usaremos Node.js como entorno de ejecución, el cual se puede descargar de su [página oficial](https://nodejs.org/), contiene el gestor de paquetes NPM, para poder usarlo se necesita una terminal o línea de comandos, en la terminal basta con escribir 
`node`
para entrar al interprete interactivo de javascript, donde podrás probar todos los comandos

## Comentarios
Al escribir un programa a veces es útil dejar comentarios acerca de lo que hace nuestro código, cada lenguaje de programación tiene distintas maneras de escribir *comentarios* que son texto que no se tomará en cuenta como código y será ignorado por la computadora.

En JS los comentarios se escriben con *"//"* seguido de el texto que quieras poner, recuerda que el texto que pongas en un comentario no se tomará en cuenta al correr el programa.


## Nuestro primer programa
Uno de los programas más conocidos y que se ha vuelto una tradicion en el mundo de la programación, es el 'hola mundo!' el cual se trata de un programa que sirve como introducción a cualquier lenguaje de programación, ademas de que sirve para comprobar que nuestro ambiente de desarrollo está funcionando correctamente.

En JavaScript hacer este programa es muy sencillo:

`console.log('hola mundo!') // hola mundo`

Esta instruccion le dice al interprete de JS que muestre el texto 'hola mundo!' en "consola" que es la palabra que se usa para referirse a la terminal donde se corre el programa.

la instruccion *console.log()* es la que se encarga de mostrar lo que sea que le pasemos en los paréntesis en consola y lo que queremos imprimir es el texto *"hola mundo!"* el cual lo pasamos entre comillas ya que es una *cadena de texto*.

