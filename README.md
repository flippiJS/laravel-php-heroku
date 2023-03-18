> **⚠️ Atención** Esta opción dejó de ser gratuita debido a cambios en la plataforma de Heroku. [Mas info](https://help.heroku.com/RSBRUH58/removal-of-heroku-free-product-plans-faq).

Aplicación Laravel Framework PHP con despliegue automático en Heroku.
==============================

## Introducción
El principal objetivo de este repo es poder desplegar de forma automática nuestra aplicación PHP Laravel Framework en Heroku.

## 1- Forkear proyecto
Como primer paso, forkeamos este proyecto desde el boton ubicado en la parte superior derecha de la pagina del repositorio.

## 2- Subimos nuestro codigo
Una vez forkeado, clonamos el repo con `git clone <url del repo>` y agregamos nuestro codigo dentro del proyecto Laravel.
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

En esta sección agregamos el nombre de la app, seleccionamos la región United States y luego clic en botón **Create app**

![Heroku2](https://i.ibb.co/TwPJnrW/heroku2.png)

Ahora vamos a la sección **Deploy** y hacemos clic en la opción de GitHub, la cual nos mostrará nuestro usuario o tendremos que iniciar sesión con GitHub. Después   buscamos el nombre de nuestro repo y aparecerá abajo:

![Heroku3](https://i.ibb.co/vZjZgD6/heroku3.png)

Seleccionamos el repo y hacemos clic en **Connect**

Una vez hecho esto, elegimos la rama de github que queremos deplegar con nuestra aplicación Heroku, en nuestro caso `main`, y hacemos clic en **Enable Automatic Deploys**. De esta forma, cada vez que se haga una modificación a esta rama, Heroku va actualizar automáticamente la aplicación.

![Heroku4](https://i.ibb.co/0Z1Psrx/heroku8.png)

Luego deberiamos hacer clic en el botón **Deploy Branch**. Esto solo se hace una sola vez, luego se hará de forma automática.

![Heroku5](https://i.ibb.co/sVYwVZx/heroku5.png)

Ahora vamos dentro del dashboard de Heroku a a la opcion de **More** > **Run console**

![Heroku11](https://i.ibb.co/Htvyp0x/11.png)

Ejecutamos el siguiente comando para obtener la APP KEY que necesitaremos para que corra la aplicación.

`php artisan key:generate --show`

![Heroku12](https://i.ibb.co/zJpkKDT/12.png)

La consola nos va a devolver un string hasheado similar a `ZEqur46KTEG91iWPhKGY42wtwi3rtkx2`

![Heroku14](https://i.ibb.co/93f688g/13.png)

Copiamos ese valor y vamos a la pestaña **Settings** y luego a la sección **Config Vars** y agregamos 2 variables:

`APP_DEBUG: true`

`APP_KEY: ZEqur46KTEG91iWPhKGY42wtwi3rtkx2`

![Heroku13](https://i.ibb.co/cxmyR1q/10.png)

Podemos verificar desde GitHub si el depliegue se hizo con exito.

![Heroku6](https://i.ibb.co/RQzHTzp/9.png)

Desde el botón **View deployment** accedemos a la URL de la app desplegada.

https://laravel-php-heroku.herokuapp.com/


### 2021 - UTN FRA
