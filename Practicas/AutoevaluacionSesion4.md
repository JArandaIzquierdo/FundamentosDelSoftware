## Autoevaluacion Sesion 2. Fundamentos del Software

####1. ¿Por qué puede ser necesario exportar una variable? ¿De qué formas puedes exportar una variable?
	Para poder utilizarla en otra shell diferente a la que estamos actualmente trabajo. Si no la exportamos no podremos trabajar con ella.
	Para exportar una variable utilizaremos la orden export y el nombre de la variable

####2. ¿Qué orden has ejecutado para resolver el ejercicio 4.7(e)?
#####e) Cree una variable de tipo vector con los valores iniciales de las tres variables.
	VAR4=(hola adios 14)

####3. ¿Qué solución has dado al ejercicio 4.8?

#####Cree un alias que se llame ne (nombrado así para indicar el número de elementos) y que devuelva el número de archivos que existen en el directorio actual. ¿Qué cambiaría si queremos que haga lo mismo pero en el directorio home correspondiente al usuario que lo ejecuta?

	alias ne='ls -A | wc -l'
	Si queremos que lo haga en el directorio home:
    alias ne='cd;ls -A | wc -l'

####4. ¿Y para el 4.9?

#####Indique la línea de orden necesaria para buscar todos los archivos a partir del directorio home de usuario ($HOME) que tengan un tamaño menor de un bloque. ¿Cómo la modificaría para que además imprima el resultado en un archivo que se cree dentro del directorio donde nos encontremos y que se llame archivosP?
	find $HOME -size -1
	Para que imprima el resultado de la orden en un archivo llamado archivosP:
    find $HOME -size -1 > archivosP