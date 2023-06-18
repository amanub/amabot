# Respondiendo comandos
Ahora que ya sabemos cómo identificar si el mensaje empieza con el prefijo predefinido y sabemos extraer el comando y argumentos del mensaje, es tiempo de realizar las acciones apropiadas de acuerdo al comando, si nos mandan un mensaje '*!hello*' debemos responder con '*World*!' y si nos mandan un mensaje '*!roll 2 5*' debemos mostrar el resultado de tirar dos dados de 5 caras y dependiendo del comando que nos envíen deberemos dar la resúesta correcta.

Primero identificaremos que el comando exista, usando la función **.indexOf()** el cual toma un elemento y nos devuelve el indice del elemento en caso de haberlo encontrado en un arreglo, o nos devuelve -1 en caso de no haberlo encontrado.

Para eso crearemos un arreglo con los comandos válidos de nuestro bot

```js
let commands = ["hello","roll"]
```
ahora verificaremos que el comando que nos envió en usuario después del prefijo está dentro de nuestro arreglo, usando la función indexOf( ):

```js
let command = 'hello'
let commandIndex = commands.indexOf(command)
```
Después de verificar que el mensaje empieza con el prefijo y el comando que mandaron existe dentro del arreglo de comandos, podemos seguir con la respuesta de nuestro bot dependiendo de el caso, usaremos una estructura switch en el indice de nuestro comando y responderemos de acuerdo a lo solicitado.

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
