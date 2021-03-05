# Cargador de comandos

Al crear un bot, y en general cualquier pieza de software, se hace evidente que insertar manualmente
todos los comandos requeridos no es la mejor manera de hacerlo, para eso se puede desarrollar una utilidad que 
hará el trabajo repetitivo de insertarlos

En el caso de nuestro bot crearemos un cargador de comandos (command Loader) para facilitarnos la tarea y permitirnos
modularizar nuestro bot

El command loader buscará todos los archivos con extención ".js" de la carpeta "commands", donde buscará los
atributos del comando que acordamos previamente, cargará los comandos en memoria para poder ser usado.
