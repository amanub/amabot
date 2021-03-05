# Mi primer Bot

Una vez tengamos instaladas las dependencias que necesitamos y hemos creado el bot desde la página de Discord, podemos empezar a trabajar, y como es tradición en el mundo de la programación, vamos a crear nuestro primer hola mundo, este programa sencillo nos ayuda a corroborar que se hayan instalado correctamente las librerías y que nuestro entorno esté funcionando bien.

Después de haber iniciado un nuevo proyecto de Node y haber instalado las dependecias procederemos a crear un nuevo archivo llamado `index.js` en la carpeta del proyecto, este archivo será el punto de entrada de nuestro programa, donde escribiremos el código siguiente:

```js
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  if (msg.content === 'Hello') {
    msg.reply('World!');
  }
});

client.login('token'); // este será el token del bot, que se encuentra en la seccion bot

```

Podremos correr el programa desde la terminal con el comando `node index.js`, debemos tomar en cuenta que tenemos que estar situados en la carpeta donde se encuentra el archivo "index.js".

Al correr el programa creamos un servidor para nuestro bot, el cuál se conecta usando el token que nos entregan al crear nuestro bot en la página de desarrolladores de  discord, si la conexion se logra sin errores aparecerá en la terminal el mensaje `logged in as ` seguido del id del bot, además de que al enviar un mensaje en el servidor con el contenido "Hello" nos responderá el bot con un mensaje "World!"
![](./images/hello/1.png)

**Nota:** El punto de entrada de un proyecto de node por defecto es `index.js`, pero puede variar de acuerdo a la configuración del archivo `package.json`.

# Breakdown

A continuación explicaremos cada linea del programa para entenderlo mejor



```js
const Discord = require('discord.js');
const client = new Discord.Client();
```
La función *require* se usa para importar la libreria de discord.js y se guarda en la variable "Discord", posteriormente instanciamos un nuevo objeto *Cliente* (.Client()) desde el objeto *Discord*, que contiene la librería, para instanciar un objeto cliente de bot y poder trabajar con él.

```js
client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});
```
El objeto *client* que creamos tiene varios métodos, los cuales podemos ver en la documentación de discord.js, el método "on()" crea un emisor de eventos que espera que ocurra el evento que le pasamos como primer parámetro, y al suceder ese evento ejecuta la función que le hayamos pasado como segundo parámetro.

En este caso, está esperando el evento *"ready"* que se dispara al conectarse exitosamente a un servidor, después hace un console.log() de el mensaje de conexión usando el tag del bot que se encuentra en *client.user.tag*

```js
client.on('message', msg => {
  if (msg.content === 'Hello') {
    msg.reply('World!');
  }
});
```
Ahora se crea otro emisor de eventos esperando un mensaje, y después ejecuta la función que checa si el contenido del mensaje recibido es igual al texto "Hello", si es igual, entonces le responde al usuario con la función ".reply()" con el texto "World!".

```js
client.login('token'); 
```
La función login() de client toma el **token** de nuestro bot, y se conecta con este a través de un *webSocket* el cual establece una conexión bidireccional con Discord, al realizarse esta conexión se manda el evento "ready" lo cual ejecuta la función del listener que muestra el nombre del bot en la terminal.

