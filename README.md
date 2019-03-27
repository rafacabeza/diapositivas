# Diapositivas con Reveal.js y Markdonw


## Dos opciones

- Sin Node.js: Editar en local y verlo sólo en ***github.io***
- Con Node.js.
    - Editamos en local
    - Servimos las diapositivas en local
    - Lo subimos a ***github.com*** y lo vemos en ***github.io***



# Instalación local


## Instalar Node.js

- Buscamos e instalamos
- Recomendación: instalar nvm
- https://nodejs.org/es/download/


## Iniciar proyecto Node

- Creamos directorio: `mkdir diapositivas`
- Iniciamos proyecto con npm: `npm init`
- Añadimos la dependencia de reveal-md: `npm install reveal-md`
- Creamos un fichero de prueba `apuntes.md`

```
# Título apuntes

## Apartado 1
- Bla, bla
- Bla, bla
```


## Ficheros de configuración de node

- Copia los ficheros reveal-md.json y reveal.json en tu directorio raíz.
- reveal-md.json
```
{
  "separator": "^\n\n\n",
  "verticalSeparator": "^\n\n"
}
```
- reveal.json
```
{
 "slideNumber": true
}
```


## Probar las diapositivas

- Ejecutamos *npm start*



#  Llevar nuestra presentación a GitHub


## Iniciamos el repositorio

```bash 
git init
nano README.md  # editar README de algún modo
nano .gitignore # ignorar node_modules 
#(ver el .gitignore de este proyecto)
git add .
git status # comprobar que no está node_modules
git commit -m "commit inicial"
```


## Subir código

- Crear repositorio en GitHub
- Seguir instrucciones de GitHub, algo así...:

``` 
git remote add "xxxxx"
git push -u origin master
```


## Habilitar GitHub Pages

- Settings del repositorio
- Activar *Pages*
- Asociar la rama *master*
- Comprobar en el enlace mostrado


## ¿Html o markdown?

- *reveal.js* convierte markdown (*.md) a Html
- En local, es nuestro servidor node.js quien ejecuta *reveal.js*
- En GitHub Pages debe ser nuestro navegador quien lo haga.
- El servidor de GitHub no sabe hacer esa traducción


## Mover reveal.js

- Para que reveal.js esté disponible en GitHub hemos de sacarlo de *node_modules*.

```
cp -r node_modules/reveal.js ./
```

- Hemos de construir uno o más ficheros html que sí pueden ser servidos por GitHub Pages.
- Recomendación: un html por cada markdown de nuestro proyecto.
- Ficheros de ejemplo: index.html y readme.md


## Base para el *index.html*

- Hay una plantilla dentro de *reveal.js*
- Si ubicamos ficheros html fuera de reveal.js hemos de modificar las rutas.
- Para incluir markdown de un fichero externo mirar este proyecto o leer [aquí](https://github.com/hakimel/reveal.js/#markdown)



# Versión sin node.js

- Hacemos fork de https://github.com/hakimel/reveal.js/
- Editamos el fichero html para crear diapositivas
- Ojo que la muestra no incluye el uso de markdown