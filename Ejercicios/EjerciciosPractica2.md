## Ejercicios Sesion 2. Fundamentos del Software

##### Ejercicio 2.1. Cree el siguiente árbol de directorios a partir de un directorio de su cuenta de usuario. Indique también cómo sería posible crear toda esa estructura de directorios mediante una única orden (mire las opciones de la orden de creación de directorios mediante man mkdir). Posteriormente realice las siguientes acciones:
	a) En Ejer1 cree los archivos arch100.txt, filetags.txt, practFS.ext y robet201.me.
		- $ touch arch100.txt
		- $ touch filetags.txt
		- $ touch practFS.ext
		- $ touch robet201.me
    
	b) En Ejer21 cree los archivos robet202.me, ejer11sol.txt y blue.me.
    	- $ touch robet202.me
    	- $ touch ejer11sol.txt
    	- $ touch blue.me
    	
	￼￼￼￼￼c) En Ejer2 cree los archivos ejer2arch.txt, ejer2filetags.txt y readme2.pdf.
    	- $ touch ejer2arch.txt
    	- $ touch ejer2filetags.txt
    	- $ touch readme2.pdf
    
	d) En Ejer3 cree los archivos ejer3arch.txt, ejer3filetags.txt y readme3.pdf.
    	- $ touch ejer3arch.txt
    	- $ touch ejer3filetags.txt
    	- $ touch readme3.pdf
    	
	e) ¿Podrían realizarse las acciones anteriores empleando una única orden? Indique cómo.
    	Se haria con la orden touch seguido de los nombre de los archivos a crear junto con su extension separado por espacios. Por ejemplo:
        - $ touch robet22.me ejer11sol.txt blue.me

![](https://github.com/JArandaIzquierdo/FundamentosDelSoftware/blob/master/images/Ejercicio2-1.png)
    
##### Ejercicio 2.2. Situados en el directorio ejercicio1 creado anteriormente, realice las siguientes acciones:

Para hacer este ejercicio nos situamos siempre en el directorio ejercicio1
    
	a) Mueva el directorio Ejer21 al directorio Ejer2.
    
    	- $ mv Ejer1/Ejer21 Ejer2
    	
	b) Copie los archivos de Ejer1 cuya extensión tenga una x al directorio Ejer3.
    
    	- $ cp Ejer1/*.*x* Ejer3
        
	c) Si estamos situado en el directorio Ejer2 y ejecutamos la orden ls -la ../Ejer3/*arch*, ¿qué archivo/s, en su caso, debería mostrar?
    
    	- arch100.txt
    	- ejer3arch.txt 
    
##### Ejercicio 2.3. Si estamos situados en el directorio Ejer2, indique la orden necesaria para listar sólo los nombres de todos los archivos del directorio padre.

	$ ls ../*.*

##### Ejercicio 2.4. Liste los archivos que estén en su directorio actual y fíjese en alguno que no disponga de la fecha y hora actualizada, es decir, la hora actual y el día de hoy. Ejecute la orden touch sobre dicho archivo y observe qué sucede sobre la fecha del citado archivo cuando se vuelva a listar.

	- Al hacer touch sobre un archivo ya existente se modifica su fecha y hora a la fecha y hora actual

##### Ejercicio 2.5. La organización del espacio en directorios es fundamental para poder localizar fácilmente aquello que estemos buscando. En ese sentido, realice las siguientes acciones dentro de su directorio home (es el directorio por defecto sobre el que trabajamos al entrar en el sistema):
	a) Obtenga en nombre de camino absoluto (pathname absoluto) de su directorio home. ¿Es el mismo que el de su compañero/a?
    
    	- Nos es el mismo que el de mi compañero, en mi caso es: /home/javia
    
	b) Cree un directorio para cada asignatura en la que se van a realizar prácticas de laboratorio y, dentro de cada directorio, nuevos directorios para cada una de las prácticas realizadas hasta el momento.
    
    	- Para crear esto directorios lo haremos con la orden mkdir seguido del nombre de los directorios.
    
	c) Dentro del directorio de la asignatura fundamentos del software (llamado FS) y dentro del directorio creado para esta práctica, copie los archivos hosts y passwd que se encuentran dentro del directorio /etc.
    
    	- $ cp -a /etc/hosts -a /etc/passwd ~/Escuela/FS/Practicas
    
	d) Muestre el contenido de cada uno de los archivos.
     
     	- Para mostrar el contenido de cada uno de los archivos utilizamos la orden cat, por ejemplo: $ cat hosts  o $ cat passwd 


##### Ejercicio 2.6. Situados en algún lugar de su directorio principal de usuario (directorio HOME), cree los directorios siguientes: Sesion.1, Sesion.10, Sesion.2, Sesion.3, Sesion.4, Sesion.27, Prueba.1 y Sintaxis.2 y realice las siguientes tareas:
	a) Borre el directorio Sesion.4
    
    	- $ rm -d Sesion.4 , ya que el directorio esta vacio, utilizamos la funcion -d
    
	b) Liste todos aquellos directorios que empiecen por Sesion. y a continuación tenga un único carácter
    
    	- $ ls Sesion.?
    
	c) Liste aquellos directorios cuyos nombres terminen en .1
    
    	- $ ls *.1
    
	d) Liste aquellos directorios cuyos nombres terminen en .1 o .2
    
    	- $ ls -d *.[12]
    
	e) Liste aquellos directorios cuyos nombres contengan los caracteres si
    
    	- Tras probar que el comando $ ls -d *{si}* no funciona, necesitamos 2 o mas partones dentro de {} separado por comas para que funcione, utilizo el comando: 
    		- $ ls *si*	  
    
	f) Liste aquellos directorios cuyos nombres contengan los caracteres si y terminen en .2
    
    	- $ ls -d *si*.2
    	
##### Ejercicio 2.7. Desplacémonos hasta el directorio /bin, genere los siguientes listados de archivos (siempre de la forma más compacta y utilizando los metacaracteres apropiados):
	a) Todos los archivos que contengan sólo cuatro caracteres en su nombre.
    
    	-
    
	b) Todos los archivos que comiencen por los caracteres d, f.
    
    	- $ ls -a d* f*
    
	c) Todos los archivos que comiencen por las parejas de caracteres sa, se, ad.
    
    	- $ ls -a sa* se* ad*
    
	d) Todos los archivos que comiencen por t y acaben en r.
    
    	- $ ls -a t*r
    
##### Ejercicio 2.8. Liste todos los archivos que comiencen por tem y terminen por .gz o .zip :
	a) De tu directorio HOME.
    
    	- $ ls tem*.gz tem*.zip	
    
	b) Del directorio actual.
    
	c) ¿Hay alguna diferencia en el resultado de su ejecución? Razone la respuesta.
    
    
##### Ejercicio 2.9. Muestre del contenido de un archivo regular que contenga texto:
	a) Las 10 primeras líneas.
    
    	- $ head archivo.txt
    
	b) Las 5 últimas líneas.
    
    	- tail -5 archivo.txt

##### Ejercicio 2.10. Cree un archivo empleando para ello cualquier editor de textos y escriba en el mismo varias palabras en diferentes líneas. A continuación trate de mostrar su contenido de manera ordenada empleando diversos criterios de ordenación.


##### Ejercicio 2.11. ¿Cómo podría ver el contenido de todos los archivos del directorio actual que terminen en .txt o .c?

	- $ cat *.txt *.c