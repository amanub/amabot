# Prefijo del Bot

Como ya vimos en la sección "*holaDiscord*", el evento "message" se activa cuando algún usuario envía un mensaje en nuestro servidor, pero quizás no queremos responder a todos los mensajes que se nos mandan, o en el caso de nuestro bot, todos los mensajes que tengan la palabra "Hello", para solucionar este problema podemos usar un identificador que nos permita distinguir cuándo se dirigen al bot y cuándo no, la forma más usada es definir un **prefijo**, es decir, un **caracter o palabra clave que irá antes del comando**.

Por ejemplo : **!**

Para que de esta manera el usuario que quiera interactuar con el bot escriba "!" seguido de la palabra o comando que desee ejecutar

Ejemplo: `!Hola`

*Nota: el caracter identificador puede ser cualquiera, no solo "!", entre los más comunes están: -, ?, $.*

Para que podamos procesar este mensaje debemos escuchar el evento "message", para después corroborar que el mensaje recibido comienza con el caracter que hayamos definido que irá seguido de el comando que el usuario quiere ejecutar.

JS nos provee de una función que es muy útil y nos sive perfectamente para lo que necesitamos, se trata de la función **startsWith()** , la cual *pertenece a todos los objetos de tipo cadena de texto*, toma como parámetro el texto que queremos encontrar al inicio del texto y regresa *true* si coincide y *false* si no.

También usaremos la función **.substr()**, el cual toma un número como parámetro y devuelve una cadena partiendo de la posición que le pasamos como primer parámetro y opcionalmente el tamaño que queremos que tenga la cadena devuelta como segundo parámetro

Ahora modificaremos nuestro código para integrar el uso de un prefijo en nuestro bot:

```js
// creamos una variable, la cual contendrá el prefijo que hayamos definido
const prefix = "!"

// escucharemos los eventos de mensaje

client.on("message", ctx => {
    let content = ctx.content //guardamos el contenido del mensaje en la variable content
    let startsWithPrefix = content.startsWith(prefix) // devuelve verdadero si empieza con el prefijo
    if (startsWithPrefix){   // verificamos si el contenido empieza con el prefijo
        let message = content.substr(1) // guardamos el contenido omitiendo el prefijo
        if (message = "Hello") { // verificamos el comando que mandó el usuario
            ctx.reply("World!")
        }
    } 
})
```
