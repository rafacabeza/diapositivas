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

``` 
git init
nano README.md  # editar README de algún modo
nano .gitignore # ignorar node_modules
git add .
git status # comprobar que no está node_modules
git commit -m "commit inicial"
```


## Subir código

- Crear repositorio en GitHub
- Seguir instrucciones:

``` 
git remote add "xxxxx"
git push -u origin master
```


## Habilitar GitHub Pages

- Settings del repositorio
- Activar *Pages*
- Asociar la rama *master*
- Comprobar en el enlace mostrado