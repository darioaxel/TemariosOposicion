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
A File Structure should be according to a required format that the operating system can understand.

A file has a certain defined structure according to its type.

A text file is a sequence of characters organized into lines.

A source file is a sequence of procedures and functions.

An object file is a sequence of bytes organized into blocks that are understandable by the machine.

When operating system defines different file structures, it also contains the code to support these file structure. Unix, MS-DOS support minimum number of file structure.

# Tipos de ficheros
File type refers to the ability of the operating system to distinguish different types of file such as text files source files and binary files etc. Many operating systems support many types of files. Operating system like MS-DOS and UNIX have the following types of files −

### Ordinary files
These are the files that contain user information.
These may have text, databases or executable program.
The user can apply various operations on such files like add, modify, delete or even remove the entire file.
### Directory files
These files contain list of file names and other information related to these files.
### Special files
These files are also known as device files.
These files represent physical device like disks, terminals, printers, networks, tape drive etc.
These files are of two types −

**Character special files** − data is handled character by character as in case of terminals or printers.

**Block special files** − data is handled in blocks as in the case of disks and tapes.

# Características

## Operaciones básicas con ficheros
Hay varias operaciones básicas que se pueden realizar con ficheros en un sistema operativo. Algunas de las operaciones más comunes incluyen la creación, lectura, escritura, copia, movimiento, renombramiento y eliminación de ficheros. A continuación, se presentan algunos ejemplos de comandos en Linux para realizar estas operaciones:

* Creación de ficheros:

**touch file.txt**: crea un fichero vacío llamado "file.txt" si no existe. Si el fichero ya existe, actualiza la fecha y hora de su última modificación.
Lectura de ficheros:

****cat file.txt**: muestra el contenido de "file.txt" en la terminal.
less file.txt: permite navegar por el contenido de "file.txt" de manera interactiva.
Escritura en ficheros:

**echo "Hello, world!" > file.txt**: escribe "Hello, world!" en "file.txt", sobrescribiendo su contenido.
echo "This is a new line" >> file.txt: añade "This is a new line" al final de "file.txt" sin sobrescribir el contenido existente.
Copia de ficheros:

**cp source.txt destination.txt**: copia el fichero "source.txt" en "destination.txt". Si "destination.txt" ya existe, se sobrescribe.
Movimiento y renombramiento de ficheros:

**mv source.txt destination.txt**: mueve el fichero "source.txt" a "destination.txt". Si "destination.txt" ya existe, se sobrescribe. Este comando también se puede utilizar para renombrar un fichero cambiando su ubicación dentro del mismo directorio.
Eliminación de ficheros:

**rm file.txt**: elimina el fichero "file.txt".
rm -f file.txt: elimina el fichero "file.txt" sin pedir confirmación.
Cambio de permisos de ficheros:

**chmod 644 file.txt**: cambia los permisos de "file.txt" a lectura y escritura para el propietario, lectura para el grupo y lectura para otros usuarios.
Comprimir y descomprimir ficheros:

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

Identificación de la posición deseada: El programa o la aplicación determina la posición exacta dentro del archivo donde se desea leer o escribir datos. Esta posición se mide en bytes desde el comienzo del archivo y se llama "offset" o desplazamiento.

Posicionamiento del puntero de archivo: Antes de leer o escribir datos en la posición deseada, es necesario posicionar el puntero de archivo en el offset correspondiente. La mayoría de los lenguajes de programación y sistemas operativos proporcionan funciones o llamadas al sistema para realizar esta tarea (por ejemplo, fseek() en C, seek() en Python, lseek() en llamadas al sistema de Linux).

Lectura o escritura de datos: Una vez que el puntero de archivo está en la posición correcta, se pueden leer o escribir datos directamente en esa posición utilizando las funciones de lectura y escritura estándar proporcionadas por el lenguaje de programación o el sistema operativo (por ejemplo, fread() y fwrite() en C, read() y write() en Python, read() y write() en llamadas al sistema de Linux).

Actualización del puntero de archivo: Después de leer o escribir datos, el puntero de archivo se actualizará automáticamente para apuntar a la siguiente posición en el archivo. Si se requiere realizar más operaciones de acceso directo, el proceso se repite desde el paso 2.
Random access file organization provides, accessing the records directly.
> Each record has its own address on the file with by the help of which it can be directly accessed for reading or writing.

The records need not be in any sequence within the file and they need not be in adjacent locations on the storage medium.

**Indexed sequential access**
This mechanism is built up on base of sequential access.
An index is created for each file which contains pointers to various blocks.
Index is searched sequentially and its pointer is used to access the file directly.

## Space Allocation
Files are allocated disk spaces by operating system. Operating systems deploy following three main ways to allocate disk space to files.

- Contiguous Allocation
- Linked Allocation
- Indexed Allocation


### Contiguous Allocation

Each file occupies a contiguous address space on disk.
Assigned disk address is in linear order.
Easy to implement.
External fragmentation is a major issue with this type of allocation technique.
### Linked Allocation
Each file carries a list of links to disk blocks.
Directory contains link / pointer to first block of a file.
No external fragmentation
Effectively used in sequential access file.
Inefficient in case of direct access file.
### Indexed Allocation
Provides solutions to problems of contiguous and linked allocation.
A index block is created having all pointers to files.
Each file has its own index block which stores the addresses of disk space occupied by the file.
Directory contains the addresses of index blocks of files.