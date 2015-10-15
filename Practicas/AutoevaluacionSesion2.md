## Autoevaluacion Sesion 2. Fundamentos del Software

##### 1. Suponiendo que nos encontramos en el directorio de trabajo /bin, donde hemos realizado el ejercicio 2.7 de la práctica, indique qué órdenes ejecutaría para:

	a) Orden para moverse a su directorio de usuario (su home directory, es decir, /home/usuario).
    
    Las tres posibles ordenes que se podrian ejecutar son: 
     - $ cd
     - $ cd ~
     - $ cd /home/javi

	b) Qué orden debe indicar para listar de su directorio de usuario aquellos archivos “ocultos” cuyo nombre comienza por .g o .c seguido de uno o más caracteres.
    
    Las dos opciones que podriamos utilizar serian: 
     - $ ls -a .g* .c*
     - $ ls -a {.g,.c}*

##### 2. En el ejercicio anterior habrá encontrado que uno de los objetos listados que cumplen la condición es .gconf. Indique qué tipo de objeto es, archivo o directorio, y qué permisos tiene asociados para cada tipo de usuario.

	En este caso, .gconf se trata de un directorio porque contiene la letra d.  Para el usuario propietario del archivo tiene permiso de lectura, escritura y ejercucion. Para grupos y otros usuarios no tiene ningun tipo de permiso habilitado.