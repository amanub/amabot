# Prefijo del Bot

Como ya vimos en la sección "holaBot" el evento "message" se activa cuando algún usuario envía un mensaje en nuestro servidor pero quizás no queramos responder a todos los mensajes que se nos mandan, o en el caso de nuestro bot, todos los mensajes de "Hola", para solucionar este problema podemos usar un identificador que nos permita distinguir cuando se dirigen al bot y cuando no, la forma más usada es definir un prefijo, es decir, un caracter o palabra clave que irá antes del comando.

Por ejemplo : **!**

Para que de esta manera el usuario que quiera interactuar con el bot escriba "!" seguido de la palabra o comando que desee ejecutar

Ejemplo: `!Hola`

*Nota: el caracter identificador puede ser cualquiera, no solo "!", entre los más comunes están: -, ?, /, $.*

Para que podamos procesar este mensaje debemos escuchar el evento "message" para después corroborar que el mensaje recibido comienza con el caracter que hayamos definido, y después identificar el comando que nos ha enviado:

JS nos provee de una función que es muy útil y nos sive perfectamente para lo que necesitamos, se trata de la función **startsWith()** , la cual pertenece a todas las cadenas, toma como parámetro el texto que queremos comparar y regresa *true* si coincide y *false* si no.

También usaremos la función *.substr()*, el cual toma un numero y devuelve una cadena partiendo del indice que le pasamos como parámetro

Ahora modificaremos nuestro código para cumplir con esta nueva regla:

```js
// creamos una variable, la cual contendrá el prefijo que hayamos definido
const prefix = "!"

// escucharemos los eventos de mensaje

client.on("message", ctx => {
    let content = ctx.content //guardamos el contenido del mensaje en la variable content
    let startsWithPrefix = content.startsWith(prefix) // devuelve un verdadero si empieza con el prefijo
    if (startsWithPrefix){   // verificamos si el contenido empieza con el prefijo
        let message = content.substr(1) // guardamos el resto del contenido
        if (message = "Hello"){
            ctx.reply("World!")
        }
    } 
})
```
