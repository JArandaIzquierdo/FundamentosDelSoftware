###Auto-evaluación de la Práctica 8. Compilacion de programas

#####1. ¿Cual es la solución al ejercicio 8.2?

El código objeto se puede generar ya que el preprocesador no comprueba las referencias externas. El error viene a la hora de enlazar, porque no se le ha indicado la librería ni la ruta que queremos usar.


#####2. ¿Cual es el contenido de tu archivo makefile para el ejercicio 8.8?
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