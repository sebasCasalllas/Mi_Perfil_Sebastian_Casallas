#Taller de sistemas operativos

****Taller 1****
---
1. Busque en la carpeta / los archivo *.sh y guarde el resultado en un archivo y en el mismo comando imprimir en consola el archivo de salida

Para este punto se utilizo el comando "find" para realizar la busqueda de archivos. Como en el punto se indica que deben ser los archivos con extensión .sh lo que se
debe hacer es agregar despues del fin el siguiente caracter "/" para indicar que la busqueda se realiza en la ubicación actual, se agrega "-name" para indicar que la
busqueda se realizara en base al nombre de los archivos y por ultimo se agrega "*.sh" lo que indica que se requieren todos los archivos con extension .sh. Adicional se
indica que los resultados se deben guardar dentro de un archivo para lo cual se debe proporcionar el comando tee seguido del nombre del archivo. Finalmente la linea de
comando queda de la siguiente forma: "find / -name "*-sh" | tee archivoResultados". A continuación se presenta el resultado.
