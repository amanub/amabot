## Contexto de ejecución en JS (scope)
El contexto o scope **hace referencia a el lugar en donde se declaran** las variables y funciones, y mas importante aún desde donde pueden ser accedidas, esto es importante para que variables con el mismo nombre no colapsen entre si.

Como regla general **una variable que se declare dentro de un bloque** de código (clases, funciones, objetos, bucles) **sólo sera válida dentro del bloque** de código (es decir, dentro de las llaves '**{**' y '**}**'), la variable no podrá ser accedida desde fuera de este bloque, ya que técnicamente **afuera no existe**, por lo que es importante tener en cuenta en qué parte del código se declara una variable.

Esto es verdad con el uso de las palabras *let* y *const* que trajo el *ES6* (ECMAScript 6) y que vienen a remplazar *var*, el cual se comporta diferente ya que su ámbito es en base a la función y no al bloque.

la declaracion de variables con la palabra clave *var* está siendo obsoleta y se considera una mala practica a la hora de escribir código, por su comportamiento tan peculiar en cuanto al scope.

# Scope global y scope local

El *scope global* se refiere a una variable que esta fuera de un bloque y tiene la caracteristica de que **puede ser accedida desde cualquier funcion u objeto hijo**.

Esto puede ser beneficioso, pero se recomienda que las variables globales sean constantes ya que al poder ser accedidas desde todos lados también **pueden ser alteradas en cualquier momento**, lo cual hace difícil encontrar un error con un programa de varias lineas de código, por lo que **no se recomienda usar variables globales** a menos que sean constantes.

El *scope local* hace referencia a una variable que fue declarada dentro de un bloque de código, el cual no puede ser referenciado fuera de él, este tipo de variables son las declaradas con la palabra *let*.



# This, that

La palabra *this*, es una palabra reservada que hace referencia al objeto al que pertenece, el valor de la palabra this depende de la manera en que se haya llamado el objeto o función.

El comportamiento de la palabra this, es un poco diferente en js a comparación de otros lenguajes, por lo que causa algunas dificultades a la hora de trabajar con éste valor y siempre hay que tener en cuenta qué objeto refencía.
