# Configuración y actualización de Git

* En el presente documento se describe la configuración y pasos a seguir para hacer uso de un repositorio Git.

Lo primero que se debe realizar es crear el repositorio. A continuacion se describen los pasos.

# Crear repositorio

1. Ingresar a la pagina de Git:

```
https://github.com/
```
2. Ingresar con la cuenta registrada.

3. En la parte izquierda se muestra un menu, se debe dar clic en el boton "new".

![crear repositorio parte 1](https://user-images.githubusercontent.com/68363695/224461494-3690a8f5-c7b4-4d14-ba59-5f61f39c28d8.png)

4. Ingresar los datos deseados para el repositorio, como lo son el nombre, si desea que sea un repositorio publico es decir que cualquiera pueda acceder o privado que solo usted y las personas a las que les de permiso puedan acceder. Se recomienda seleccionar la opción de adcionar el README. Como ejemplo se presenta la creación del repositorio Mi_Perfil_Sebastian_Casallas, de tipo publico y seleccionando la adición del README

![crear repositorio parte 2](https://user-images.githubusercontent.com/68363695/224461495-e76a95e7-916d-4444-9af6-4cd3fd3ddcdc.png)

5. Una vez se tengan las configuraciones debe dar clic en el boton "Create repository"

![crear repositorio parte 3](https://user-images.githubusercontent.com/68363695/224461496-90e1386f-6081-4840-8a12-8dd1ba116531.png)

6. Una vez creado el repositorio, se muestra la siguiente ventana.

![crear repositorio parte 4](https://user-images.githubusercontent.com/68363695/224461497-c51d1559-4ea9-4eb9-ae3a-9708c43ee6d4.png)

7. Lo siguiente que debe hacer luego de crear el respositorio es crear las ramas en las cuales va a trabajar. Esto se realiza dando clic donde aparece el nombre de la rama principal en este caso la rama "main", lo cual hace que se despliegue una ventana, asi como se puede apreciar en la siguiente imagen:

![crear repositorio parte 5](https://user-images.githubusercontent.com/68363695/224461498-c1f9fe7f-9ccc-4df2-b49f-4fc2e5430bc9.png)

8. Se ecribe el nombre que desea poner a la rama en el espacio que dice "Find o create branch" y luego da clicl en la parte inferior donde aparece el mensaje "Create branch: 'Nombre que suministro' from main".

![crear repositorio parte 6](https://user-images.githubusercontent.com/68363695/224461487-8077df47-51e2-47ad-9a81-b226b7bf7a3e.png)

Luego de haber crear y configurar el repositorio se debe crear una copia en el equipo local donde se vaya a llevar a cabo el desarrollo del proyecto. Lo anterior para crear una carpeta en el equipo local la cual este conectada al respositorio que se creo, con el fin de que el proyecto contenido en la carpeta se vaya actualizando en el repositorio mediante los comandos que se presentan mas adelante.

# Clonar repositorio en equipo local

1. Lo primero que se debe hacer para clonar el repositorio es indicarle al equipo como se va a presentar al repositorio, es decir indicar quien esta trabajando desde ese equipo para asi tener presente cuales fueron las modificaciones que realizo cada persona que tenga acceso al repositorio. Los comandos para hacer dicha configuración son:

```
git config --global user.email "correo@gmail.com" >>> Comando para indicar el correo de la persona
git config --global user.name "Sebastian Casallas" >>> Nombre con el cual se va a presentar al respositorio
git config --global core.autocrlf false >>> Se usa para evitar conflictos con los finales de linea
```

2. Una vez se tengan las configuraciones globales se procede a clonar el respositorio mediante el comando "git clone" y la url que nos otorga Git hub segun se muestra en la siguiente imagen: 

![Clonar repositorio parte 1](https://user-images.githubusercontent.com/68363695/224461493-520b9eed-fb1c-45ee-a3cb-6feb4fc9bd9e.png)

quedando el siguiente comando:

```
git clone https://github.com/sebasCasalllas/Mi_Perfil_Sebastian_Casallas.git
```

Una vez clonado se procede a realizar la actualización del repositorio.

# Actualización del repositorio

1. Revisar el estado del repositorio con el comando "status", el cual proporciona si existe alguna actualización en el repositorio y en su equipo local no, tambien indica en que rama del repositorio se encuentra. La forma correta de ingresar el comando es:

```
git status
```

2. Seleccionar la rama adecuada para ralizar los cambios en el repositorio. Debido a que existen diferentes ramas se puede ubicar en la que desee realizar los cambios mediante el siguiente comando:

```
git checkout nombre_de_rama
```
 
3. Una vez seleccionada la rama se procede a actualizar el respositorio, primero indicando cual es el contenido que va a adionar mediante el comando "add", en caso de querer adicionar todo el contenido usar el comando de la siguiente forma:

```
git add .
```

4. Adicionar un comentario, en el cual se haga una muy breve descripción de los cambios que va a realizar en el repositior:

```
git commit -m "Comentario"
```

5. Finalmente se procede a subir los cambios realizados al repositorio:

```
git push
```

# Configuración de Git en una instancia

En caso de no poder acceder a la cuenta git mediante la proporcion de las credenciales o para facilitar y automatizar el proceso de actualización del repositiorio se debe realizar la configuración de un para de llaves.

1. Crear el par de llaves desde la instacia donde se va a clonar el repositorio. Mediante el siguiente comando

```
ssh-keygen
```

Luego dar enter 3 veces para que el par de llaves no queden con contraseña.

2. Usar el comando "cat" seguido de la ruta donde se almaceno la llave publica para acceder a su contenido, esto debido a que la cadena de caracteres que se muestre es la llave publica que vamos a configurar en el repositorio.

3. Ingresar a la configuración de la cuenta de git hub, y dar clic en la opción "SSH and GPG keys" para luego dar clic en "new SSH key".

4. Proporcionar el nombre que dese otorgarle a la llave y pegar el contenido del la llave publica.

5. Por ultimo dar clic en "Add SSH key"

![LLave ](https://user-images.githubusercontent.com/68363695/224461491-bed33165-d59e-40e7-81c5-c3ad6296f356.png)



