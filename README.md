# Instrucciones de instalación y configuración Front-end

## Instalación

### Laravel 9
Requisitos Previos:
- Instalación de NodeJS versión 18.12.1, el cual se puede descargar desde la página oficial y por medio de un .exe se configura
globalmente.
- En el caso de requerir ejecutar localmente se puede usar el servidor Wampserver 3.3.0 que cuenta por defecto con PHP 8.0 y 7.2
por defecto, ademas de apache, MySQL y MongoDB.

*NOTA:* una vez instalado Composer antes de instalarlo es necesario agregar en las variables de entorno la ruta de PHP y la
    respectiva versión a usar (Recomendación v.8.0.x)

- Instalación de Composer 2.5.8 para administrar los paquetes necesarios y poder instalar Laravel con sus respectivas
dependencias.

*INSTALACIÓN*

Instalar Laravel por medio de composer.

```sh
composer global require laravel/installer

```

Crear proyecto con el CLI de Laravel, para esto el comando es:

```sh

laravel new nameproject
cd nameproject
```

Es necesario ingresar a la carpeta del proyecto creado con Laravel para ejercutar los comandos internos de *"artisan"*

Comprobar la versión y el correcto funcionamiento de CLI de Laravel
```sh

php artisan --version
```

Una vez comprobado la versión finalmente queda ejecutar el proyecto con el servidor.

```sh
php artisan serve

Starting Laravel development server: http://127.0.0.1:8000
```



### React

Versión 8.19.2

Instalar el front del proyecto con React, se ingresa a la carpeta del proyecto y se ejecuta el siguiente comando.
```sh

npx create-react-app reactfront
cd reactfront
```

Añadir paquetes del proyecto
```sh

npm i axios bootstrap react-router-dom@6
```

Ejecutar el comando para iniciar el servidor de React y comprobar que quedo correctamente.

```sh
npm react start
```

Importar a la base de datos el archivo SQL que cuenta con las tablas y registros de demostración del proyecto."DumpAppLR-Demo.sql"
## Funcionamiento general

1. Al ingresar al Localhost:3000 el proyecto por medio de React Automaticamente se redirecciona a un Home donde se encuentran
los tres botones solicitados:
    + Inicio de Sesión: el cual redirecciona a un formulario de inicio o registro de usuario.
    + Registro: El cual dirige al formulario de crear un usuario en el sistema, donde solicita Nombre, Email y Password.
    + Editar perfil: Para facilitar la interacción de esta opción se genero un la tabla que listara todos los usuarios
    registrados en el proyecto para el demo.

2. El flujo de interacción es el siguiente:

- Al iniciar sesión la aplicación indica por medio de un mensaje si se ingreso correctamente y direcciona al "Home", en caso de
de no acceder correctamente el formulario indica el mensaje respectivo y se queda en el mismo modulo.
- Desde el formulario es posible acceder al modulo "Registrarse" para ser un usuario nuevo en el demo.
- Y finalmente desde el botón de editar perfil, que lleva al listado de todos los usuarios es posible editar los existentes; modificando Nombre y clave del usuario requerido.
