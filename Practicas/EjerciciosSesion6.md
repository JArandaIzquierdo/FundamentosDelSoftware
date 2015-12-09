###Fundamentos del Software

##Relacion de ejercicios 6. Programacion del Shell

#####Ejercicio 6.1. 
#####Escriba un guion que acepte dos argumentos. El primero será el nombre de un directorio y el segundo será un valor entero. El funcionamiento del guion será el siguiente: deberán anotarse en un archivo denominado archivosSizN.txt aquellos archivos del directorio dado como argumento y que cumplan la condición de tener un tamaño menor al valor aportado en el segundo argumento. Se deben tener en cuenta las comprobaciones sobre los argumentos, es decir, debe haber dos argumentos, el primero deberá ser un directorio existente y el segundo un valor entero.

[Solucion ejercicio 6.1](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/Practicas/Scrips/Ejercicio6-1)

#####Ejercicio 6.2.
#####Escriba un guion que acepte el nombre de un directorio como argumento y muestre como resultado el nombre de todos y cada uno de los archivos del mismo y una leyenda que diga "Directorio", "Enlace" o "Archivo regular", según corresponda. Incluya la comprobación necesaria sobre el argumento, es decir, determine si el nombre aportado se trata de un directorio existente.

[Solucion ejercicio 6.2](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/Practicas/Scrips/Ejercicio6-2)

#####Ejercicio 6.3.
#####Escriba un guion en el que, a partir de la pulsación de una tecla, detecte la zona del teclado donde se encuentre. Las zonas vendrán determinadas por las filas. La fila de los números 1, 2, 3, 4, ... será la fila 1, las teclas donde se encuentra la Q, W, E, R, T, Y,... serán de la fila 2, las teclas de la A, S, D, F,...serán de la fila 3 y las teclas de laZ,X,C,V,...serán de la fila 4. La captura de la tecla se realizará mediante la orden read.

#####Ejercicio 6.4.
#####Escriba un guion que acepte como argumento un parámetro en el que el usuario indica el mes que quiere ver, ya sea en formato numérico o usando las tres primeras letras del nombre del mes, y muestre el nombre completo del mes introducido. Si el número no está comprendido entre 1 y 12 o las letras no son significativas del nombre de un mes, el guion deberá mostrar el correspondiente mensaje de error.

#####Ejercicio 6.5.
#####Escriba un guion que solicite un número hasta que su valor esté comprendido entre 1 y 10. Deberá usar la orden while y, para la captura del número, la orden read.

[Solucion ejercicio 6.5](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/Practicas/Scrips/Ejercicio6-5)

#####Ejercicio 6.6.
#####Copie este ejercicio y pruébelo en su sistema para ver su funcionamiento. ¿Qué podemos modificar para que el giro se vea más rápido o más lento? ¿Qué hace la opción -e de las órdenes echo del guion?
#####Ejercicio 6.7.
#####Escriba un guion que admita como argumento el nombre de un tipo de shell (por ejemplo, csh, sh, bash, tcsh, etc.) y nos dé un listado ordenado alfabéticamente de los usuarios que tienen dicho tipo de shell por defecto cuando abren un terminal. Dicha información del tipo de shell asignado a un usuario se puede encontrar en el archivo /etc/passwd, cuyo contenido está delimitado por ':'. Cada información situada entre esos delimitadores representa un campo y precisamente el campo que nos interesa se encuentra situado en primer lugar. En definitiva, para quedarnos con lo que aparece justo antes del primer delimitador será útil la orden siguiente:
	cut -d':' -f1 /etc/passwd
#####Donde la opción –d indica cuál es el delimitador utilizado y la opción –f1 representa a la secuencia de caracteres del primer campo. Realice, utilizando el mecanismo de cauces, el ejercicio pero usando la orden cat para mostrar el contenido de un archivo y encauzado con la orden cut para filtrar la información que aparece justo antes del delimitador ':'4.
#####Realice también la comprobación de la validez del tipo de Shell que se introduce como argumento. Use para ello la información que encontrará en el archivo /etc/shells donde encontrará los tipos de Shell que se pueden utilizar en el sistema.

#####Ejercicio 6.8. 
#####Dos órdenes frecuentes de Unix son tar y gzip. La orden tar permite almacenar/extraer varios archivos de otro archivo. Por ejemplo, podemos almacenar el contenido de un directorio en un archivo con
	tar -cvf archivo.tar directorio (la opción -x extrae los archivos de un archivo .tar).
#####La orden gzip permite comprimir el contenido de un archivo para que ocupe menos espacio. Por ejemplo, gzip archivo comprime archivo y lo sustituye por otro con el mismo nombre y con la extensión .gz. La orden para descomprimir un archivo .gz o .zip es gunzip.
#####Dadas estas órdenes construya un guion, denominado cpback, que dado un directorio o lista de archivos como argumento(s) los archive y comprima en un archivo con nombre copiaYYMMDD, donde YY corresponde al año, la MM al mes y la DD al día, dentro de un directorio denominado CopiasSeguridad. El guion debe realizar las comprobaciones oportunas: los argumentos existen, el directorio de destino existe y si no, lo crea.

#####Ejercicio 6.9. 
#####Hacer un script en Bash denominado newdirfiles con los siguientes tres argumentos:
  	<dirname> Nombre del directorio que, en caso de no existir, se debe crear para alojar en él los archivos que se han de crear.
  	<num_files> Número de archivos que se han de crear.
  	<basefilename> Será una cadena de caracteres que represente el nombre base de los archivos.
#####Ese guion debe realizar lo siguiente:
      
	Comprobar que el número de argumentos es el correcto y que el segundo argumento tenga un valor comprendido entre 1 y 99.
	Crear, en caso de no existir, el directorio dado en el primer argumento a partir del directorio donde se esté situado y que posea permisos de lectura y escritura para el usuario $USER.
	Dentro del directorio dado en el primer argumento, crear archivos cuyos contenidos estarán vacíos y cuyos nombres lo formarán el nombre dado como tercer argumento y un número que irá desde 01 hasta el número dado en el segundo argumento.