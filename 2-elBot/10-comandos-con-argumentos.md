# Creando un comando que reciba argumentos (roll)
Ya hemos creado nuestro comando 'hello', sin embargo este no recibe ningún parámetro, así que la respuesta es muy sencilla, ahora subiremos un poco la dificultad y nos aventuraremos a crear un comando que reciba parámetros y en base a estos realice su operación

## roll (nFaces, nTimes)
Esta función roll tomará dos parámetros, el primero será el número de caras que tendrá nuestro dado, el segundo será el número de veces que tiraremos el dado, simularemos los dados con un **generador de números aleatorios** incluido en JS el cuál se encuentra dentro de la clase **Math**, la función se llama **random()** y al ser invocada *nos devuelve un valor entre el 0 y el 1*, también ocuparemos otra función dentro de la clase
Math, llamada **ceil()** el cual redondea un número al entero mayor más cercano, a continuación veremos su uso:

```js
function roll(nFaces, nTimes){
    let results = [] // creamos un arreglo vacío, que contendrá los resultados
        for (let i = 0; i < nTimes; i++){
            let randomNumber = Math.random() * nFaces // nos regresa un número del 0 al 1
             // al número que nos dan lo multiplicamos por el número de caras

             // como random() nos regresa un número decimal lo redondearemos con ceil()
            let result = Math.ceil(randomNumber)
            
            results.push(result) // ahora meteremos el resultado en nuestro arreglo de resultados llamando la función push de nuestro arreglo de resultados
            }
    return results //se regresa el arreglo con resultados de los dados
}
```
La función creada arriba regresará un arreglo de números que serán los resultados de nuestras tiradas, y se responderá al usuario que envió el comando, lo cual veremos en la siguiente sección.