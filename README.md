# Servidor en node http, https y certiificado

Creación de un servidor node http y https

## Configuración inicial

- Conocimientops básicos de javascript y nodejs
- Disponer de node y npm instalados
- Crear una carpeta que englobe el proyecto
- Navegar a la carpeta del proyecto

## Creación y arranque del servidor http

1. `npm init` : inicializa el packages json del proyecto, para cualquier npm install que se use añadir -- save para que se añadan los módulos a este fichero
2. Crear el fichero index.html
3. `npm install express --save` : Instalar el módulo express usado para implementar el servidor
4. Introducir el siguiente código en el fichero index.js para inicializar el servidor http
~~~
var express = require('express'); //Importar la librería
const PORT = 80;
var app = express();
// Aranque del servidor
app.listen(PORT, () => console.log("http server escucha en el puerto " + PORT + " ...")); 
 // Si se accede desde un navegador a la url http://IP_SERVER/test imprimir un texto en consola y enviar al navegador Hola
app.get('/test', (req,res) => { console.log("Se ha accedido al recurso test del servidor");
                                res.send('Hola'); });

~~~
5. `node index.js` : Introducir el comando en la consola para inicializar el servidor y ver que aparece el texto http server escucha ... en la consola
6. Comprobar que si accedemos desde un navegador a http://IP_SERVER/test en la consola aparece el texto Se ha accedido ... y en el navegador se ve Hola
7. Ya hay un servidor http funcionando
