###Fundamentos del Software

##Relacion de ejercicios 8.Compilacion de programas

#####Ejercicio 8.1. Pruebe a comentar en el archivo fuente main.cpp la directiva de procesamiento “#include ”functions.h”. La línea quedaría así: //#include ”functions.h”. Pruebe a generar ahora el módulo objeto con la orden de compilación mostrada anteriormente. ¿Qué ha ocurrido?

Como hemos comentado #include "functions.h" no encuentra las funciones print_hello ni factorial y nos da un error.

#####Ejercicio 8.2. Explique por qué el enlazador no ha podido generar el programa archivo ejecutable programa2 del ejemplo anterior y, sin embargo, ¿por qué sí hemos podido generar el módulo main2.o?

El archivo .o si se general porque no comprueba las referencias externas. Se produce el error al enlacer por no haber indicado la libreria que queremos usar