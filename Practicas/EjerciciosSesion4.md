###Fundamentos del Software

##Relacion de problemas 4.	Variables, alias, ordenes de busqueda y guiones

#####Ejercicio 4.1
#####Escriba, al menos, cinco variables de entorno junto con el valor que tienen.

	TERM_PROGRAM=Apple_Terminal
	TERM=xterm-256color
	SHELL=/bin/bash
	CLICOLOR=1
	HOME=/Users/JaviAir


#####Ejercicio 4.2
#####Ejecute las órdenes del cuadro e indique qué ocurre y cómo puede resolver la situación para que la variable NOMBRE se reconozca en el shell hijo.
	$ NOMBRE=FS
	$ echo $NOMBRE
    
	$ bash
	$ echo $NOMBRE

$ NOMBRE solo es visible en el shell actual. Al cambiar el shell no podemos acceder a la variable anteriormente definida. Para exportar una variable a otro shell utilizamos las orden $ export variable

#####Ejercicio 4.3
#####Compruebe qué ocurre en las expresiones del ejemplo si se quitan las comillas dobles del final y se ponen después de los dos puntos. ¿Qué sucede si se sustituyen las comillas dobles por comillas simples?

	$ echo “Los archivos que hay en el directorio son: $(ls -l)”
    $ echo “Los archivos que hay en el directorio son: `ls -l`”

Si pones las dobles comillas despues de los dos puntos, la orden sigue funcionando pero se vera la frase del echo seguida de la lista de los archivos y directorios de esa ruta pero uno detras de otros.

Sustituir las comillas dobles por las simples no funciona, el echo muestra tambien la orden $(ls -l)


#####Ejercicio 4.4
#####Pruebe la siguiente asignación:
	 $ numero=$numero+1
     $ echo $numero


#####Ejercicio 4.5
#####Construya un guion que acepte como argumento una cadena de texto (por ejemplo, su nombre) y que visualice en pantalla la frase Hola y el nombre dado como argumento.


#####Ejercicio 4.6
#####Varíe el guion anterior para que admita una lista de nombres.


#####Ejercicio 4.7
#####Cree tres variables llamadas VAR1, VAR2 y VAR3 con los siguientes valores respectivamente “hola”, “adios” y “14”.
	a) Imprima los valores de las tres variables en tres columnas con 15 caracteres de ancho.
    
    
    
	b) ¿Son variables locales o globales?
    
    
    
	c) Borre la variable VAR2.
    
    
    
	d) Abra otra ventana de tipo terminal, ¿puede visualizar las dos variables restantes?
    
    
    
	e) Cree una variable de tipo vector con los valores iniciales de las tres variables.
    
    
    
	f) Muestre el segundo elemento del vector creado en el apartado e.
    
    
    
#####Ejercicio 4.8
#####Cree un alias que se llame ne (nombrado así para indicar el número de elementos) y que devuelva el número de archivos que existen en el directorio actual. ¿Qué cambiaría si queremos que haga lo mismo pero en el directorio home correspondiente al usuario que lo ejecuta?




#####Ejercicio 4.9
#####Indique la línea de orden necesaria para buscar todos los archivos a partir del directorio home de usuario ($HOME) que tengan un tamaño menor de un bloque. ¿Cómo la modificaría para que además imprima el resultado en un archivo que se cree dentro del directorio donde nos encontremos y que se llame archivosP?

#####Ejercicio 4.10
#####Indique cómo buscaría todos aquellos archivos del directorio actual que contengan la palabra “ejemplo”.

#####Ejercicio 4.11
#####Complete la información de find y grep utilizando para ello la orden man.


#####Ejercicio 4.12
#####Indique cómo buscaría si un usuario dispone de una cuenta en el sistema.

#####Ejercicio 4.13
#####Indique cómo contabilizar el número de ficheros de la propia cuenta de usuario que no tengan permiso de lectura para el resto de usuarios.


#####Ejercicio 4.14
#####Modifique el ejercicio 8 de forma que, en vez de un alias, sea un guion llamado numE el que devuelva el número de archivos que existen en el directorio que se le pase como argumento.













