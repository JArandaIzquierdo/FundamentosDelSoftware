###Fundamentos del Software

##Relacion de ejercicios 5. Expresiones con variables y expresiones regulares

#####Ejercicio 5.1: Utilizando una variable que contenga el valor entero 365 y otra que guarde el número del día actual del año en curso, realice la misma operación del ejemplo anterior usando cada una de las diversas formas de cálculo comentadas hasta el momento, es decir, utilizando expr, $(( ... )) y $[ ... ].

	dia=365
    fechaActual=$(date +%j)
	echo "Faltan $(( (dia - fechaActual) / 7 )) semanas hasta fin de año"
    echo "Faltan $[ (dia - fechaActual) / 7 ] semanas hasta fin de año"

#####Ejercicio 5.2: Realice las siguientes operaciones para conocer el funcionamiento del operador de incremento como sufijo y como prefijo. Razone el resultado obtenido en cada una de ellas:
	$ v=1
	$ echo $v
    1
	$ echo $((v++))
    1
    $ echo $v
    2
	$ echo $((++v))
    2
	$ echo $v
	3

#####Ejercicio 5.3: Utilizando el operador de división, ponga un caso concreto donde se aprecie que la asignación abreviada es equivalente a la asignación completa, es decir, que x/=y equivale a x=x/y.

	x=10
    y=5
    
    echo $((x/=y))
    2
	
    echo $((x=x/y))
    2
#####Ejercicio 5.4: Compruebe qué ocurre si en el ejemplo anterior utiliza comillas dobles o simples para acotar todo lo que sigue a la orden echo. ¿Qué sucede si se acota entre comillas dobles solamente la expresión aritmética que se quiere calcular?, ¿y si se usan comillas simples?


#####Ejercicio 5.5: Calcule con decimales el resultado de la expresión aritmética (3-2)/5. Escriba todas las expresiones que haya probado hasta dar con una respuesta válida. Utilizando una solución válida, compruebe qué sucede cuando la expresión aritmética se acota entre comillas dobles; ¿qué ocurre si se usan comillas simples?, ¿y si se ponen apóstrofos inversos?

#####Ejercicio 5.6: Consulte la sintaxis completa de la orden let utilizando la orden de ayuda para las órdenes empotradas (help let) y tome nota de su sintaxis general.


#####Ejercicio 5.7: Con la orden let es posible realizar asignaciones múltiples y utilizar operadores que nosotros no hemos mencionado anteriormente. Ponga un ejemplo de asignación múltiple y, por otra parte, copie en un archivo el orden en el que se evalúan los operadores que admite. Apóyese a través de la ayuda que ofrece help let.

#####Ejercicio 5.8: Haciendo uso de las órdenes conocidas hasta el momento, construya un guion que admita dos parámetros, que compare por separado si el primer parámetro que se le pasa es igual al segundo, o es menor, o es mayor, y que informe tanto del valor de cada uno de los parámetros como del resultado de cada una de las evaluaciones mostrando un 0 o un 1 según corresponda.

#####Ejercicio 5.9: Usando test, construya un guion que admita como parámetro un nombre de archivo y realice las siguientes acciones: asignar a una variable el resultado de comprobar si el archivo dado como parámetro es plano y tiene permiso de ejecución sobre él; asignar a otra variable el resultado de comprobar si el archivo es un enlace simbólico; mostrar el valor de las dos variables anteriores con un mensaje que aclare su significado. Pruebe el guion ejecutándolo con /bin/cat y también con /bin/rnano.


#####Ejercicio 5.10: Ejecute help test y anote qué otros operadores se pueden utilizar con la orden test y para qué sirven. Ponga un ejemplo de uso de la orden test comparando dos expresiones aritméticas y otro comparando dos cadenas de caracteres.

#####Ejercicio 5.11: Responda a los siguientes apartados:
	a) Razone qué hace la siguiente orden:
		if test -f ./sesion5.pdf ; then printf “El archivo ./sesion5.pdf existe\n”; fi
	b) Añada los cambios necesarios en la orden anterior para que también muestre un mensaje de aviso en caso de no existir el archivo. (Recuerde que, para escribir de forma legible una orden que ocupe más de una línea, puede utilizar el carácter “\” como final de cada línea que no sea la última.)
	c) Sobre la solución anterior, añada un bloque elif para que, cuando no exista el archivo ./sesion5.pdf, compruebe si el archivo /bin es un directorio. Ponga los mensajes adecuados para conocer el resultado en cada caso posible.
	d) Usando como base la solución del apartado anterior, construya un guion que sea capaz de hacer lo mismo pero admitiendo como parámetros la ruta relativa del primer archivo a buscar y la ruta absoluta del segundo. Pruébelo con los dos archivos del apartado anterior.


#####Ejercicio 5.12: Construya un guion que admita como argumento el nombre de un archivo o directorio y que permita saber si somos el propietario del archivo y si tenemos permiso de lectura sobre él.

#####Ejercicio 5.13: Escriba un guion que calcule si el número de días que faltan hasta fin de año es múltiplo de cinco o no, y que comunique el resultado de la evaluación. Modifique el guion anterior para que admita la opción -h de manera que, al ejecutarlo con esa opción, muestre información de para qué sirve el guion y cómo debe ejecutarse.
#####El siguiente guion de ejemplo se puede utilizar para borrar el archivo temporal que se le dé como argumento. Si rm devuelve 0, se muestra el mensaje de confirmación del borrado; en caso contrario, se muestra el código de error. Como se puede apreciar, hemos utilizado la variable $LINENO que indica la línea actualmente en ejecución dentro del guion.

```bash
#!/bin/bash
declare -rx SCRIPT=${0##*/}
# donde SCRIPT contiene sólo el nombre del guión # ${var##Patron} actúa eliminando de $var aquella parte # que cumpla de $Patron desde el principio de $var
# En este caso: elimina todo lo que precede al
# último slash “/".
if rm ${1} ; then
	printf "%s\n" "$SCRIPT: archivo temporal borrado"
else
    STATUS=177
	printf "%s – código de finalizacion %d\n" \
	"$SCRIPT:$LINENO no es posible borrar archivo" $STATUS
fi 2> /dev/null

```

#####Ejercicio 5.14: ¿Qué pasa en el ejemplo anterior si eliminamos la redirección de la orden if?

#####Ejercicio 5.15: Haciendo uso del mecanismo de cauces y de la orden echo, construya un guion que admita un argumento y que informe si el argumento dado es una única letra, en mayúsculas o en minúsculas, o es algo distinto de una única letra.


#####Ejercicio 5.16: Haciendo uso de expresiones regulares, escriba una orden que permita buscar en el árbol de directorios los nombres de los archivos que contengan al menos un dígito y la letra e. ¿Cómo sería la orden si quisiéramos obtener los nombres de los archivos que tengan la letra e y no contengan ni el 0 ni el 1?


#####Ejercicio 5.17: Utilizando la orden grep, exprese una forma alternativa de realizar lo mismo que con wc -l.