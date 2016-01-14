###Fundamentos del Software

##Relacion de ejercicios 8.Compilacion de programas

#####Ejercicio 8.1. Pruebe a comentar en el archivo fuente main.cpp la directiva de procesamiento “#include ”functions.h”. La línea quedaría así: //#include ”functions.h”. Pruebe a generar ahora el módulo objeto con la orden de compilación mostrada anteriormente. ¿Qué ha ocurrido?

Como hemos comentado #include "functions.h" no encuentra las funciones print_hello ni factorial y nos da un error.

#####Ejercicio 8.2. Explique por qué el enlazador no ha podido generar el programa archivo ejecutable programa2 del ejemplo anterior y, sin embargo, ¿por qué sí hemos podido generar el módulo main2.o?

El archivo .o si se general porque no comprueba las referencias externas. Se produce el error al enlacer por no haber indicado la libreria que queremos usar

#####Ejercicio 8.3. Explique por qué la orden g++ previa ha fallado. Explique los tipos de errores que ha encontrado.

No encuentra la libretia functions.h

#####Ejercicio 8.4. Copie el contenido del makefile previo a un archivo llamado makefileE ubicado en el mismo directorio en el que están los archivos de código fuente .cpp. Pruebe a modificar distintos archivos .cpp (puede hacerlo usando la orden touch sobre uno o varios de esos archivos) y compruebe la secuencia de instrucciones que se muestra en el terminal al ejecutarse la orden make. ¿Se genera siempre la misma secuencia de órdenes cuando los archivos han sido modificados que cuando no? ¿A qué cree puede deberse tal comportamiento?

La salida de la orden make cambia dependiendo de que archivos hayamos modificado, para no tener que ejecutar todos los archivos si solo han cambiado alguno de ellos.




```shell
# Nombre archivo: makefileG
# Uso: make –f makefileG
# Descripción: Mantiene todas las dependencias entre los módulos y la
# biblioteca que utiliza el programa2. 
# Variable que indica el compilador que se va a utilizar CC=g++
# Variable que indica el directorio en donde se encuentran los archivos de cabecera INCLUDE_DIR= ./includes
# Variable que indica el directorio en donde se encuentran las bibliotecas LIB_DIR= ./
programa2: main2.o factorial.o hello.o libmates.a
$(CC) -L$(LIB_DIR) -o programa2 main2.o factorial.o hello.o -lmates
main2.o: main2.cpp
      $(CC) -I$(INCLUDE_DIR) -c main2.cpp
factorial.o: factorial.cpp
$(CC) -I$(INCLUDE_DIR) -c factorial.cpp
hello.o: hello.cpp
      $(CC) -I$(INCLUDE_DIR) -c hello.cpp
libmates.a: sin.o cos.o tan.o
      $(AR) -rvs libmates.a sin.o cos.o tan.o
sin.o: sin.cpp
      $(CC) -I$(INCLUDE_DIR) -c sin.cpp
cos.o: cos.cpp
      $(CC) -I$(INCLUDE_DIR) -c cos.cpp
tan.o: tan.cpp
      $(CC) -I$(INCLUDE_DIR) -c tan.cpp
```