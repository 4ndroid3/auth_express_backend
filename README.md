# API Backend Sistema de autenticación.
##### Creado en NODE con express, utiliza JWT para realizar la autenticación de la API.

Dependencias del proyecto, pueden instalarse con `npm i`:

    "bcryptjs": "^2.4.3",
    "cors": "^2.8.5",
    "dotenv": "^16.0.3",
    "express": "^4.18.2",
    "express-validator": "^6.14.2",
    "jsonwebtoken": "^8.5.1",
    "mongoose": "^6.7.0"
    "mongoose": "^6.7.0"


Al descargar el repositorio se crear un archivo **.env** que tenga las siguientes variables de entorno:

    PORT=PUERTO DONDE SE VA A CORRER EL SERVIDOR DE NODE, ej: 4000
    DB_CNN=Key que otorga mongodb Atlas  para conectarse remotamente.
    SECRET_JWT_SEED=CODIGO SECREO PARA GENERAR TOKEN JWT

------------
Tambien se debe tener instalado nodemon en forma global para poder correr los scripts y que el servidor esté con live reload.

`sudo npm install -g nodemon`

------------


Una vez instaladas las dependencias y configurado el archivo de environment se puede correr el servidor con el comando: `npm run dev`

### Rutas del proyecto:
**/api/auth/new **-> crea un usuario con el siguiente payload:

    {
    	"email" : "email",
    	"name": "name",
    	"password": "password"
    }
    
**/api/auth/login **-> hace login de un usuario con el siguiente payload:

    {
    	"email" : "email",
    	"password": "password"
    }
    
**/api/auth/renew **-> renueva el token para darle vigencia al usuario logueado.

Hay que agregar un **HEADER** en el endpoint llamado **x-token** y su valor debe ser el token vigente.

    
