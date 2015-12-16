###Fundamentos del Software

##Relacion de ejercicios 7. Depuracion y control de trabajos

#####Ejercicio 7.1. Indique cuál ha sido el error introducido en el guion anterior y cómo se corregiría.

#####Ejercicio 7.2. Aplicar las herramientas de depuración vistas en la sección 2 para la detección de errores durante el desarrollo de los guiones propuestos como ejercicios en la práctica 6.

#####Ejercicio 7.3. Escribir un guion que nos dé el nombre del proceso del sistema que consume más memoria.
[Solucion Ejercicio 7.3]()

#####Ejercicio 7.4. Escribir un guion que escriba números desde el 1 en adelante en intervalos de un segundo ¿Cómo se podría, desde otro terminal, detener la ejecución de dicho proceso, reanudarlo y terminar definitivamente su ejecución?
[Solucion Ejercicio 7.4](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/Practicas/Scrips/Ejercicio7-4)
Detener la ejecucion desde otro terminal:

	kill -STOP 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'
Reanudar la ejecucion desde otro terminal:

	kill -CONT 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'

Terminar la ejecucion desde otro terminal:

	kill -TERM 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'

#####Ejercicio 7.5. ¿Se puede matar un proceso que se encuentra suspendido? En su caso, ¿cómo? 

Si se puede, con la orden kill pid

#####Ejercicio 7.6. ¿Qué debemos hacer a la orden top para que nos muestre sólo los procesos nuestros?
	top -U nombre_usuario