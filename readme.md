### Problema con login y sesiones al insertar en l bdd

**Autor: Carles Far Pierres**

view app: [VER](http://encuentratucamino.herokuapp.com/)

### TECNOLOGÍAS USADAS

![front-back](https://github.com/LITULANDIO/myFinalProject_Skylab/blob/master/assets/technologies.gif?raw=true) 

### INSTALACIÓN DEL PROYECTO

 Para clonar el proyecto:

```
git clone https://github.com/LITULANDIO/-Find-your-way.git
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

Siguiendo los pasos de las imágenes....