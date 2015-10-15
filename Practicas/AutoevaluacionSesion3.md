## Autoevaluacion Sesion 3. Fundamentos del Software

##### 1. Mi solución al Ejercicio 3.3 ha sido:

##### Ejercicio 3.3. Utilizando el metacarácter de creación de cauces y sin utilizar la orden cd:
	- Muestre por pantalla el listado (en formato largo) de los últimos 6 archivos del directorio /etc.

	$ ls -l /etc | tail -6

	- La orden wc muestra por pantalla el número de líneas, palabras y bytes de un archivo (consulta la orden man para conocer más sobre ella). Utilizando dicha orden, muestre por pantalla el número de caracteres (sólo ese número) de los archivos del directorio de trabajo que comiencen por los caracteres “e” o “f”.
	
    $ cat e* f* | wc -m





##### 2. Mi solución al Ejercicio 3.4 ha sido: