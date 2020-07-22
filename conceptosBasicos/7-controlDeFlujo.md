## Control de flujo ( if, switch)
En la vida real nos encontramos con decisiones y las acciones que tomamos con estas decisiones dependen de alguna condición, para ejecutar procedimientos basados en alguna condición usamos el bloque 'if' en programacion el cual permite la ejecución de código basado en una condición
```
if (true){
\\ código
}
```
**La condición que se evaluara se encuentra entre paréntesis** del lado derecho de la palabra clave if y el código que se ejecutará en caso de evaluarse a verdadero sera el que esta entre las llaves que proceden la condición.

## El nombre completo
Para comprender mejor el funcionamiento de un bloque *if* hay que conocer 'el nombre completo' ya que nos ayuda a recordar las partes de esta estructura, el nombre completo de un if es "*if... then... else...*" cada una de estas partes es importante y a continuación veremos la función de cada una de ellas

### if <condición>
Esta parte es donde definiremos la condición que queremos entre parentesis, la
condición se evaluara dando como resultado un booleano el cual definira el
siguiente paso

`if (10 > 5)`


### then...
**En caso de que se cumpla la condición**, es decir el booleano de la condición haya resultado verdadero se procedera a ejecutar el código del bloque then, el cual se encuentra después de la condición
```js
if (true) {
	//bloque then
}
```

### Else...
**En caso de que no se cumpla la condición** (de *false* como resultado), se pasará a ejecutar el bloque de código que pertenece a else, el cual **se puede encontrar después de la llave de cierre de el bloque then**, cabe mencionar que no es necesario poner un bloque else en caso de que nuestro problema no lo requiera.

if (false){
	//...
}
else {
	//bloque else
}


## El if en crack
**Muchas veces es necesario hacer mas de una decision** y para este caso los *if anidados* o *ifs enlazados* son la herramienta indicada, consiste en poner otra condición en la parte del else la cual tiene su propio else, como se muestra en el ejemplo siguiente
```js
if (false){
	//then
}
else if (true){
	//then 
	//true
}
else{
	//else
}
```

Al encadenar ifs *siempre se checa la primera opcion*, continuando en orden con las condiciónes y **terminando la ejecucion de la estructura al momento de que se cumple alguna de las condiciónes** o hasta haber llegado hasta el bloque else, el cual sera el que se ejecute en el caso de que ninguna se cumpla, puede pensarse como el valor por defecto


## Switch, el primo feo del if

Otra estructura de control es el llamado switch, el cual **se comporta muy parecido a el if**, pero con otra sintaxis especial la cual es la siguiente
```
switch (<variable>){
	case <condición 1> :
		//código caso 1
		break;
	case <condición 2> :
		//código caso 2
		break;
	default:
		//código por defecto
		break;
}
```

El switch se utiliza más eficientemente cuando se sabe el valor final de la variable a comparar, esto es muy útil a la hora de hacer menús o decisiones de las cuales sabemos de antemano su posible valor.

Por ejemplo, al crear algunas funciones en nuestro bot, esperaremos que el usuario nos pase alguna opcion y de acuerdo a ésta haremos la operacion apropiada

Digamos que le damos una lista de opciones al usuario, de la cual decidirá qué operación aritmética se aplicará a dos numeros:

1: suma
2: resta
3: multiplicacion
4: division
5: modulo

el usuario seleccionará un numero y en base al numero seleccionado se decidirá la operación a realizar, esto se podria lograr con una serie de ifs encadenados, pero el switch se adapta muy bien a este tipo de casos, el cual se utilizaría de la siguiente manera:
```js
let a = 5;
let b = 5;

let resultado = 0;

let opcion = 3; //elegimos multiplicación

switch (opcion) {
	case 1:
		resultado = a + b
	break;

	case 2:
		resultado = a - b
	break;
	
	case 3:
		resultado = a * b
	break;
	case 4:
		resultado = a / b
	break;
	case 5:
		resultado = a % b
	break;
}
console.log(resultado);
```
El switch no solo acepta numeros como valores, **tambien puede comparar cadenas**, en caso de querer cambiar el ejemplo anterior usando el nombre de la operacion simplemente en el case se pondra el string de cada una de las opciones (`case 'suma' : `)

tambien **es importante recordar poner la palabra clave *break*** , ya que en caso de no tenerla, el switch probará con el siguiente case y en caso de que no se cuente con ninguna palabra break ejecutara todos los casos del switch con los que cumpla la condición

En caso de que no se cumpla ninguna condición se ejecutará el bloque *default* que es el bloque por defecto

