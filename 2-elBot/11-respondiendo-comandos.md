# Respondiendo comandos
Ahora que ya sabemos cómo identificar si el mensaje empieza con el prefijo predefinido y sabemos extraer el comando y argumentos del mensaje, es tiempo de realizar las acciones apropiadas de acuerdo al comando, si nos mandan un mensaje '!hello' debemos responder con 'World!' y si nos mandan un mensaje '!roll 2 5' debemos mostrar el resultado de tirar dos dados de 5 caras y así dependiendo del comando deberemos dar la resúesta correcta

Primero identificaremos que el comando exista, usando la función *.indexOf()* el cual toma un elemento y nos devuelve el indice del elemento en caso de haberlo encontrado, y nos devuelve -1 en caso de no haberlo encontrado.

para eso crearemos un arreglo con los comandos válidos de nuestro bot

```js
let commands = ["hello","roll"]
```
ahora verificaremos que el comando que nos envió en usuario después del prefijo, el cual extrajimos en la leccion de comandos y argumentos, existe con indexOf:

```js
let commandIndex = commands.indexOf(command)
```
Después de verificar que el mensaje empieza con el prefijo podemos seguir con la respuesta de nuestro bot dependiendo de el caso, usaremos una estructura switch en el indice de nuestro comando y responderemos de acuerdo a lo solicitado.

```js
if (startsWithPrefix) {
    switch (commandIndex) {
      case 0: // el primer elemento de nuestro arreglo de comando es "hello"
        ctx.reply("World!")
        break
      case 1:
          let dados = roll(arguments[0], arguments[1]) // utilizamos la función que creamos
          // pasandole el primer y segundo elemento del arreglo arguments en los parámetros correspondientes
        ctx.reply(dados) // le respondemos al usuario con el resultado
        break
      default:
          ctx.reply("el comando no se encontró")
          //usamos el caso default para notificar errores
        break

    }
  }
