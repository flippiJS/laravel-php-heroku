Aplicación Laravel Framework PHP con despliegue automático en Heroku.
==============================

## Introducción
El principal objetivo de este repo es poder desplegar de forma automática nuestra aplicación PHP Laravel Framework en Heroku.

## 1- Forkear proyecto
Como primer paso, forkeamos este proyecto desde el boton ubicado en la parte superior derecha de la pagina del repositorio.

## 2- Subimos nuestro codigo
Una vez forkeado, clonamos el repo con `git clone <url del repo>` y agregamos nuestro codigo PHP (SLIM Framework) dentro de la carpeta `/app/`.
Luego comiteamos y pusheamos los cambios.

```sh
git add .
git commit -m "first commit"
git push -u origin main
```

## 3- Crear y configurar la App en Heroku

Nos dirigimos a la página de Heroku https://heroku.com/, iniciamos sesión si tenemos cuenta o creamos una.

Heroku al iniciar sesión nos muestra su dashboard, aquí haremos clic en **New** y luego en **Create new app**:

![Heroku1](https://i.ibb.co/MVTSH69/heroku1.png)