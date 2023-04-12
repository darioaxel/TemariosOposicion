# TEMA 13. Ficheros. Tipos. Características. Organizaciones
# Introducción
# Ficheros
## Definición de fichero
Una de las definiciones de fichero referentes dentro de los textos sobre informática describe que 
>*"Un archivo es una colección de información relacionada definida por su creador. Los archivos de computadora pueden ser creados, leídos, escritos y eliminados, y pueden ser referenciados por su nombre."*  
Fuente: Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). Hoboken, NJ: John Wiley & Sons.

Esta definición abarca la idea básica de que un fichero es una entidad que almacena datos o información en un sistema informático y puede ser manipulado mediante operaciones como creación, lectura, escritura y eliminación.   

Los ficheros son esenciales para la organización y gestión de datos en sistemas operativos y aplicaciones informáticas. Se componen de colecciones de información relacionada que se guarda en un sistema de almacenamiento secundario persistente: discos opticos, magnéticos, etc. Desde el punto de vista del sistema operativo, un fichero es una secuencia de bits, bytes, líneas o registros cuyo significado es definido por el usuario que lo crea. 

## Estructura de un fichero
La estructura de un fichero debe ajustarse a un formato requerido que el sistema operativo pueda entender.
Un fichero tiene una estructura definida según su tipo.
Un fichero de texto es una secuencia de caracteres organizados en líneas.
Un fichero fuente es una secuencia de procedimientos y funciones.
Un fichero objeto es una secuencia de bytes organizados en bloques comprensibles por la máquina.

Cuando el sistema operativo define diferentes estructuras de archivos, también contiene el código para soportar estas estructuras de archivos. Unix, MS-DOS soportan un número mínimo de estructuras de ficheros.

# Tipos de ficheros
El tipo de fichero se refiere a la capacidad del sistema operativo para distinguir diferentes tipos de ficheros, como ficheros de texto, ficheros fuente, ficheros binarios, etc. Muchos sistemas operativos soportan muchos tipos de ficheros. Los sistemas operativos como MS-DOS y UNIX tienen los siguientes tipos de ficheros.

### Ficheros ordinarios
Son los ficheros que contienen información del usuario.
Pueden contener texto, bases de datos o programas ejecutables.
El usuario puede aplicar varias operaciones en este tipo de ficheros como añadir, modificar, borrar o incluso eliminar el fichero completo.
### Archivos de directorio
Estos archivos contienen una lista de nombres de archivos y otra información relacionada con estos archivos.
### Archivos especiales
Estos ficheros también se conocen como ficheros de dispositivo.
Estos archivos representan dispositivos físicos como discos, terminales, impresoras, redes, unidades de cinta, etc.
Estos archivos son de dos tipos -

**Ficheros especiales de caracteres** - los datos se tratan carácter por carácter, como en el caso de terminales o impresoras.

**Ficheros especiales de bloques**: los datos se tratan en bloques, como en el caso de los discos y las cintas.

# Características

## Operaciones básicas con ficheros
Hay varias operaciones básicas que se pueden realizar con ficheros en un sistema operativo. Algunas de las operaciones más comunes incluyen la creación, lectura, escritura, copia, movimiento, renombramiento y eliminación de ficheros. A continuación, se presentan algunos ejemplos de comandos en Linux para realizar estas operaciones:

* Creación de ficheros:

**touch file.txt**: crea un fichero vacío llamado "file.txt" si no existe. Si el fichero ya existe, actualiza la fecha y hora de su última modificación.

***Lectura de ficheros:***

**cat file.txt**: muestra el contenido de "file.txt" en la terminal.
less file.txt: permite navegar por el contenido de "file.txt" de manera interactiva.

***Escritura en ficheros:***

**echo "Hello, world!" > file.txt**: escribe "Hello, world!" en "file.txt", sobrescribiendo su contenido.
echo "This is a new line" >> file.txt: añade "This is a new line" al final de "file.txt" sin sobrescribir el contenido existente.

***Copia de ficheros:***
**cp source.txt destination.txt**: copia el fichero "source.txt" en "destination.txt". Si "destination.txt" ya existe, se sobrescribe.

***Movimiento y renombramiento de ficheros:***
**mv source.txt destination.txt**: mueve el fichero "source.txt" a "destination.txt". Si "destination.txt" ya existe, se sobrescribe. Este comando también se puede utilizar para renombrar un fichero cambiando su ubicación dentro del mismo directorio.

***Eliminación de ficheros:***
**rm file.txt**: elimina el fichero "file.txt".
rm -f file.txt: elimina el fichero "file.txt" sin pedir confirmación.

***Cambio de permisos de ficheros:***
**chmod 644 file.txt**: cambia los permisos de "file.txt" a lectura y escritura para el propietario, lectura para el grupo y lectura para otros usuarios.

***Comprimir y descomprimir ficheros:***
**gzip file.txt**: comprime el fichero "file.txt" y lo guarda como "file.txt.gz".
gunzip file.txt.gz: descomprime el fichero "file.txt.gz" y lo guarda como "file.txt".

# Organización
## File Access Mechanisms
File access mechanism refers to the manner in which the records of a file may be accessed. There are several ways to access files −

* Sequential access
* Direct/Random access
* Indexed sequential access

**Sequential access**
A sequential access is that in which the records are accessed in some sequence, i.e., the information in the file is processed in order, one record after the other. This access method is the most primitive one. Example: Compilers usually access files in this fashion.

**Direct/Random access**
El acceso directo (también conocido como acceso aleatorio o random) a ficheros es un método de lectura y escritura de datos en un archivo que permite acceder a cualquier parte del archivo sin necesidad de leer o escribir secuencialmente desde el principio. Este mecanismo es especialmente útil cuando se trabaja con archivos grandes o cuando se necesita acceder rápidamente a cierta información sin procesar todo el archivo.

El acceso directo a ficheros funciona de la siguiente manera:

- Identificación de la posición deseada: El programa o la aplicación determina la posición exacta dentro del archivo donde se desea leer o escribir datos. Esta posición se mide en bytes desde el comienzo del archivo y se llama "offset" o desplazamiento.

- Posicionamiento del puntero de archivo: Antes de leer o escribir datos en la posición deseada, es necesario posicionar el puntero de archivo en el offset correspondiente. La mayoría de los lenguajes de programación y sistemas operativos proporcionan funciones o llamadas al sistema para realizar esta tarea (por ejemplo, fseek() en C, seek() en Python, lseek() en llamadas al sistema de Linux).

- Lectura o escritura de datos: Una vez que el puntero de archivo está en la posición correcta, se pueden leer o escribir datos directamente en esa posición utilizando las funciones de lectura y escritura estándar proporcionadas por el lenguaje de programación o el sistema operativo (por ejemplo, fread() y fwrite() en C, read() y write() en Python, read() y write() en llamadas al sistema de Linux).

- Actualización del puntero de archivo: Después de leer o escribir datos, el puntero de archivo se actualizará automáticamente para apuntar a la siguiente posición en el archivo. Si se requiere realizar más operaciones de acceso directo, el proceso se repite desde el paso 2.

La organización de archivos de acceso aleatorio permite acceder directamente a los registros.

> Cada registro tiene su propia dirección en el archivo con la ayuda de la cual se puede acceder directamente para leer o escribir.

Los registros no necesitan estar en ninguna secuencia dentro del archivo y no necesitan estar en ubicaciones adyacentes en el medio de almacenamiento.

**Acceso secuencial indexado**

Este mecanismo se basa en el acceso secuencial.
Se crea un índice para cada fichero que contiene punteros a varios bloques.
El índice se busca secuencialmente y su puntero se utiliza para acceder directamente al fichero.

## Asignación de espacio
El sistema operativo asigna espacios de disco a los archivos. Los sistemas operativos utilizan tres formas principales para asignar espacio de disco a los archivos.

- Asignación contigua
- Asignación vinculada
- Asignación indexada

### Asignación contigua
Cada archivo ocupa un espacio de dirección contiguo en el disco.
Las direcciones de disco asignadas siguen un orden lineal.
Fácil de implementar.
La fragmentación externa es un problema importante con este tipo de técnica de asignación.
### Asignación vinculada
Cada fichero lleva una lista de enlaces a bloques de disco.
El directorio contiene el enlace / puntero al primer bloque de un fichero.
No hay fragmentación externa
Eficaz en ficheros de acceso secuencial.
Ineficiente en caso de archivo de acceso directo.
### Asignación indexada
Proporciona soluciones a los problemas de asignación contigua y vinculada.
Se crea un bloque índice que contiene todos los punteros a los ficheros.
Cada fichero tiene su propio bloque índice que almacena las direcciones del espacio de disco ocupado por el fichero.
El directorio contiene las direcciones de los bloques índice de los ficheros.
