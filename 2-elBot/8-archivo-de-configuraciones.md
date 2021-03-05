# Archivo de configuración
Hasta ahora hemos puesto nuestro token y el prefijo en el archivo principal, sin embargo esto puede ser considerado una mala práctica, por lo que ahora reestructuraremos nuestro código para tomar las configuraciones de un archivo externo, el cual estará en formato **JSON**

Crearemos un archivo llamado config.json donde crearemos un objeto JSON con las llaves "token", y "prefix" como el siguiente:

```json
{
    "token" : "aqui tu token de el bot",
    "prefix": "!"
}
```

Ahora para poder usar estos datos debemos referenciarlo en el código principal de la siguiente manera

```js
config = require(./cofig.json)
```
ahora el objeto *config* contendrá todas nuestras configuraciones y podran ser accesadas desde el código con la sintaxis de punto de manera que nuestro código quedaría refactorizado de la siguiente manera:

```js
const Discord = require('discord.js');
const client = new Discord.Client();
const config = require('./config.json') // cargamos el archivo de configuración

const prefix = config.prefix // obtenemos el prefijo desde el archivo de configuración

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', ctx => {
  const content = ctx.content;
  const startsWithPrefix = content.startsWith(prefix)
  if (startsWithPrefix){
        let message = content.substr(1) 
        if (message = "Hello"){
            msg.reply("World!")
        }
    } 
})

client.login(config.token); // obtenemos el token del bot desde el archivo
```

**Nota:** Esto se hace para que al momento de subir nuestro bot a un repositorio no se exponga nuestro token, además hace que sea más facil la configuración de nuestro bot.