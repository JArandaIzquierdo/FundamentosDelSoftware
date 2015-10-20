## Ejercicios Sesion 3. Fundamentos del Software

##### Ejercicio 3.1. Se debe utilizar solamente una vez la orden chmod en cada apartado. Los cambios se harán en un archivo concreto del directorio de trabajo (salvo que se indique otra cosa). Cambiaremos uno o varios permisos en cada apartado (independientemente de que el archivo ya tenga o no dichos permisos) y comprobaremos que funciona correctamente:
􏰆 􏰆 􏰆 􏰆 􏰆
	- Dar permiso de ejecución al “resto de usuarios”.

	$ chmod o+x archivo

	- Dar permiso de escritura y ejecución al “grupo”.

	$ chmod g+wx archivo

	- Quitar el permiso de lectura al “grupo” y al “resto de usuarios”.

	$ chmod go-r archivo

	- Dar permiso de ejecución al “propietario” y permiso de escritura el “resto de usuarios”.

	$ chmod u+x, o+w archivo

	- Dar permiso de ejecución al “grupo” de todos los archivos cuyo nombre comience con la letra “e”. Nota: Si no hay más de dos archivos que cumplan esa condición, se deberán crear archivos que empiecen con “e” y/o modificar el nombre de archivos ya existentes para que cumplan esa condición.

	$ chmod g+x e*


##### Ejercicio 3.2. Utilizando solamente las órdenes de la práctica anterior y los metacaracteres de redirección de salida:
	- Cree un archivo llamado ej31 , que contendrá el nombre de los archivos del directorio padre del directorio de trabajo.

	$ ls .. > ej31

	- Cree un archivo llamado ej32 , que contendrá las dos últimas líneas del archivo creado en el ejercicio anterior.

	$ tail -2 ej31 > ej32

	- Añada al final del archivo ej32 , el contenido del archivo ej31 .
	
    $ cat ej32 >> ej31

##### Ejercicio 3.3. Utilizando el metacarácter de creación de cauces y sin utilizar la orden cd:
	- Muestre por pantalla el listado (en formato largo) de los últimos 6 archivos del directorio /etc.

	$ ls -l /etc | tail -6

	- La orden wc muestra por pantalla el número de líneas, palabras y bytes de un archivo (consulta la orden man para conocer más sobre ella). Utilizando dicha orden, muestre por pantalla el número de caracteres (sólo ese número) de los archivos del directorio de trabajo que comiencen por los caracteres “e” o “f”.
	
    $ cat e* f* | wc -m


##### Ejercicio 3.4. Resuelva cada uno de los siguientes apartados.
	a) Cree un archivo llamado ejercicio1, que contenga las 17 últimas líneas del texto que proporciona la orden man para la orden chmod (se debe hacer en una única línea de órdenes y sin utilizar el metacarácter “;” ).
    
    $ man chmod | tail -17 > ejercicio1
    
    b) Al final del archivo ejercicio1, añada la ruta completa del directorio de trabajo actual.
    
    $ pwd >> ejercicio1
    
    c)Usando la combinación de órdenes mediante paréntesis, cree un archivo llamado ejercicio3 que contendrá el listado de usuarios conectados al sistema (orden who) y la lista de archivos del directorio actual.
    
    $ (who ; pwd) > ejercicio3
    
    d)Añada, al final del archivo ejercicio3, el número de líneas, palabras y caracteres del archivo ejercicio1. Asegúrese de que, por ejemplo, si no existiera ejercicio1, los mensajes de error también se añadieran al final de ejercicio3.
    
    
    
    e)Con una sola orden chmod, cambie los permisos de los archivos ejercicio1 y ejercicio3, de forma que se quite el permiso de lectura al “grupo” y se dé permiso de ejecución a las tres categorías de usuarios.
    
    $ chmod g-r,a+x ejercicio1 ejercicio3
    
    
    
    