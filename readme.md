### Problema con login y sesiones al insertar en l bdd

**Autor: Carles Far Pierres**

view app: [VER](http://encuentratucamino.herokuapp.com/)

### TECNOLOGÍAS USADAS

![front-back](https://github.com/LITULANDIO/myFinalProject_Skylab/blob/master/assets/technologies.gif?raw=true) 

### INSTALACIÓN DEL PROYECTO

 Para clonar el proyecto:

```
git clone https://github.com/LITULANDIO/solution-sesion-users.git
```

Para instalar las dependencias:

```
npm install
```

URL mongoDB

```
Pruebas
mongodb://localhost:27017/XXXXX

En producción
'mongodb://admin:admin@ds129010.mlab.com:29010/db_encuentra'
```

Palabra secreta para la session y el cifrado:

```
SECRET=XXXXXXXXXXXXXXXXXX
```


Puedes utilizar el puerto que prefieras

```
PORT =XXXX
```


Configuración de la cuenta Cloudinary (registro: register in https://cloudinary.com)

```
CLOUD_NAME=XXXXXXX
API_KEY=XXXXXXXXXXX
API_SECRET=XXXXXXXXXXXXX
UPLOAD_FOLDER= upload
```

Para iniciar la aplicación:

```
npm run dev
```

Problemas:

Al iniciar sessión con cualquier usuario accedemos a la cuenta donde se pueden crear anuncios. Al querer crear un anuncio parece ser que desactiva la sesión.... pero si no existe ningun registro en la bd nos hará la insercción correctamente. Pero en consola nos muestra un error en la página fullEvent.pug
Si queremos insertar un segundo evento, aparentemente hace el mismo proceso a diferencia de que no inserta en la bdd.

Archivos implicados:

1. app.js 

2. models: bdd
    - retiro
    - counts
    
3. routes/auth: passport/sessions
    - index.js
     
4. routes/events/handlers: consulta a la bd para mostrar todos los eventos del user
    - getCategories.js

5. views: renders
    - layout
    - login-register.pug
    - myAcount.pug
    - add-event.pug

Siguiendo los pasos de las imágenes....

HOME
![1](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/process_1-home.png)

REGISTER
![2](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/process_2-login.pug.pn.png)

LOGIN
![3](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/process_3-login.pug.png)

MY ACOUNT
![4](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/process_4-myAcount.pug.png)

ADD EVENT
![5](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/process_5-addEvent.pug.png)

ERROR
![6](https://github.com/LITULANDIO/solution-sesion-users/blob/master/assets/error.png)