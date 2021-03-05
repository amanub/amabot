# La API de Discord
Discord es una aplicacion de VoIP, videochat y mensajeria instántanea, creada por la empresa del mismo nombre, dentro de este software puedes crear un servidor, en el que tienes la posibilidad de hacer canales de texto y voz, crear roles, administrar a los usuarios y muchas cosas mas, y lo mejor de todo es que todo esto se puede hacer a traves de su API, abriendo un amplio espectro de posibilidades a los programadores.

## Documentacion
Los desarrolladores de Discord proveen una gran y extensa documentación la cual podemos visitar en su [pagina de programadores](https://discord.com/developers/docs/intro) , en esta página podemos encontrar diferentes secciones detallando cada una de los servicios a nuestra disposición, así como información legal acerca de su uso (recordemos que Discord es una empresa privada), tambien encontraremos varios tutoriales básicos para familiarizarnos con su uso, en la seccion [reference](https://discord.com/developers/docs/reference) podemos ver la dirección a la que tenemos que hacer las peticiones, la cual es `https://discordapp.com/api`, conocida como *base URL* así como consideraciones como la autenticación, el formato y tipo de las peticiones.

En esa documentación se pueden encontrar todos los servicios junto con sus caracteristicas de un forma muy detallada que nos pueden ayudar a guiarnos si alguna vez no sabemos por qué el resultado que obtenemos no es el que esperabamos.

## Por qué no usaremos la API?
La API de Discord a pesar de estar extensamente documentada, puede resultar un poco intimidante y tediosos trabajar con ella desde cero, ya que tendríamos que elaborar manualmente las peticiones y validar las respuestas, por lo tanto, en la próxima sección veremos una alternativa para trabajar con esta API