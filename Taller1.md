#Taller de sistemas operativos

****Taller 1****
---
1. Busque en la carpeta / los archivo *.sh y guarde el resultado en un archivo y en el mismo comando imprimir en consola el archivo de salida

Para este punto se utilizo el comando "find" para realizar la busqueda de archivos. Como en el punto se indica que deben ser los archivos con extensión .sh lo que se
debe hacer es agregar despues del fin el siguiente caracter "/" para indicar que la busqueda se realiza en la ubicación actual, se agrega "-name" para indicar que la
busqueda se realizara en base al nombre de los archivos y por ultimo se agrega "*.sh" lo que indica que se requieren todos los archivos con extension .sh. Adicional se
indica que los resultados se deben guardar dentro de un archivo para lo cual se debe proporcionar el comando tee seguido del nombre del archivo. Finalmente la linea de
comando queda de la siguiente forma: "find / -name "*-sh" | tee archivoResultados". A continuación se presenta el resultado.

![Punto 1](https://user-images.githubusercontent.com/68363695/222876126-54918101-6fd0-4507-a3c7-f6f131adfe2d.png)

2. Cree una lista de archivos separados por enter llamándolo entrada.in, después con la lista leer entrada.in y crear los archivos con la listada creada en la carpeta file_salida/, liste los archivos creados, guarde en un archivo salida.out e imprma el archivo   enumerando la lista de archivos creados.

Para el desarrollo de este punto, lo primero fue usar el editor "nano" para ingresar el nombre de los archivos que se iban a crear junto con sus respectivas extensiones. En la siguiente imagen se puede observar el comando utilizado para abrir el editor para modificar el contenido del archivo entrada.in.

![punto 2-3](https://user-images.githubusercontent.com/68363695/222876132-ba24d943-fa48-46b5-81d8-9ec36e1f1b23.png)

Editando el contenido con los nombres de archivos:

![punto 2-1](https://user-images.githubusercontent.com/68363695/222876130-9644e872-8327-42f5-b149-1a9ed1c1a73b.png)

Guardando los cambios en el archivo:

![punto 2-2](https://user-images.githubusercontent.com/68363695/222876131-723f25cb-e694-44d2-a5e7-50a493bca54c.png)

Verificando el contendio del archivo entrada.in mediante el comando "cat":

![punto 2-4](https://user-images.githubusercontent.com/68363695/222876133-fd4e978b-64f3-426c-af6f-5f6512e3080a.png)

Para poder crear los archivos en base al contenido del archivo entrada.in se requiere de un scrip el cual se muestra a continuacion:

![punto 2-7](https://user-images.githubusercontent.com/68363695/222876136-b3ae1742-7d7a-44f9-9da4-d2237deeffba.png)

En el script lo primero que se encutra es un ciclo con la sentencia for, el cual es utilizado para leer cada una de las lineas de texto contenidas en el archivo entrada.in, el contenido de cada linea de texto se almacena temporalmente en la variable "LINEA". De acuerdo a lo requerido en el punto los archivos que se van a crear deben quedar en una carpeta con nombre "file_salida" para esto se utiliza el comando "cd" seguido de la ruta donde se encuentra la carpeta para indicarle al sistema que se ubique en esa carpeta. Luego de ubicarse en la carpeta y extraer la informacion del archivo en la variable "LINEA" se utiliza el comando "touch" para crear los archivos con el nombre que se encuentre almacena en la variable "LINEA".

Finalmente se implementa el comando "ls" para obtener el contenido de la carpeta "file_salida", seguido del caracter ">" para almacenar el texto en el archivo "salida.out".

Antes de ejecutar el script se requiere darle permisos al archivo de extensión sh mediante el comando "chmod +x" seguido del nombre del archivo donde se encuetra el script, tal como se muestra en la siguiente imagen:

![punto 2-6](https://user-images.githubusercontent.com/68363695/222876135-3c7d731a-de02-44cb-955d-20d93afc45c7.png)

Luego de dar los permisos se ejecuta el script mediante la siguiente instuccion "./Nombre_Script", asi como se muestra en la siguiente imagen:

![punto 2-5](https://user-images.githubusercontent.com/68363695/222876134-048f112e-bd3b-44c8-bd56-e0df0260430a.png)

Al ejecutar el script se muestra en consola una lista enumerada de los archivos contenidos en la carpeta "file_salida".








