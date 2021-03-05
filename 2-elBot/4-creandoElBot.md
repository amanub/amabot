# Creando una aplicación
Para crear nuestro Bot de Discord, primero tenemos que crear una aplicación en el [*portal de desarrolladores*](https://discord.com/developers/applications), eso se puede hacer muy
fácilmente yendo a la sección de [applications](https://discord.com/developers/applications)

![Developer Menu](images/1.png)

y presionando "New application"

![Developer Menu](images/2.png)

A continuación introducimos el nombre que queremos para nuestra aplicación

![Developer Menu](images/3.png)

Y listo!!! con esto tendremos creada nuestra aplicación de Discord.

![Developer Menu](images/4.png)

# Creando nuestro bot
Una vez creada la aplicación debemos crear el Bot, para eso deberemos ir a la sección de "bot"

![Developer Menu](images/5.png)

**Nota**: Debemos tomar en cuenta que no se puede borrar una vez creado y para borrarlo deberemos eliminar nuestra aplicación completa.

![Developer Menu](images/6.png)

Con esto se ha creado un *usuario bot* que nos servirá para interactuar con la aplicación, a continuación deberemos guardar el *token* dando click en "copy", el token es muy importante ya que nos da acceso a el usuario bot que creamos, **siempre debes tener seguro tu token**, ya que el que lo tenga podrá también conectarse desde ese usuario

![Developer Menu](images/7.png)


## Dándole permisos al bot
 
Ahora que tenemos nuestro bot creado deberemos añadirlo a un servidor, para eso necesitamos un link el cual podremos crear en la sección de *OAuth2*, que es el sistema de autorización que usa la app de discord

![Developer Menu](images/8.png)

En la pestaña de *Oauth2* en la parte de "scope" deberemos seleccionar "bot"
![Developer Menu](images/9.png)

Lo cual nos mostrará los siguientes permisos que le podemos otorgar a nuestro bot:

![Developer Menu](images/10-2.png)

Debemos de tomar en consideración que los permisos son muy importantes ya que limitan lo que nuestro bot puede hacer, siempre debemos de asignar **los roles mínimos necesarios** para que nuestro bot funcione.

Los permisos de administrador son los que más acciones nos permiten hacer y es el que usaremos nosotros para experimentar con la API, pero a la hora de crear un Bot **debemos tomar en cuenta las acciones que nuestro bot realizará y los permisos que vamos a usar** y siempre tratar de asignar los mínimos necesarios.

![Developer Menu](images/11.png)

Esto nos genera un link el cual nos va apermitir agregar el bot a un servidor con los permisos que le asignamos

![Developer Menu](images/12.png)

Pegamos el link en el navegador y nos desplegará un cuadro donde podremos seleccionar el servidor de discord al que queremos agregar nuestro bot

![Developer Menu](images/13.png)

Nos mostrará los permisos que solicita

![Developer Menu](images/14.png)

Si todo sale bien veremos una pantalla de confirmación y tendremos nuestro bot en el servidor de Discord

![Developer Menu](images/15.png)
