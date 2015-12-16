###Auto-evaluación de la Práctica 7. Depuracion y control de trabajos
#####1. ¿Cuál es la solución al ejercicio 7.4?
[Solucion Ejercicio 7.4](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/Practicas/Scrips/Ejercicio7-4)
Detener la ejecucion desde otro terminal:

	kill -STOP 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'
Reanudar la ejecucion desde otro terminal:

	kill -CONT 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'

Terminar la ejecucion desde otro terminal:

	kill -TERM 'ps -A .o pid, cmd | grep 7-4impnum | head -n 1 | cut -d " " -f 1'
#####2. ¿Cuál es el contenido de tu guion para el ejercicio 7.5?
Si se puede, con la orden kill pid
#####3. Para el ejercicio 7.6, el contenido de tu guion es:
top -U nombre_usuario