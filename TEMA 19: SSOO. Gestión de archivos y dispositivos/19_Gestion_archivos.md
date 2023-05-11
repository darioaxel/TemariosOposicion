# Tema 19. Gestión de archivos y dispositivos
# 1. Introducción
# 2. Definiciones

"Operating System Concepts" de Abraham Silberschatz, Peter B. Galvin y Greg Gagne:
**Fichero (archivo):** Un archivo es una colección de información relacionada almacenada en el almacenamiento secundario de un sistema de computación, como un disco duro o una unidad de estado sólido. Los archivos pueden contener datos, programas o ambos, y son identificados por un nombre único en el sistema de archivos.

**Directorio:** Un directorio es una estructura especial de archivos que almacena información sobre otros archivos y directorios. Un directorio funciona como un contenedor que organiza y agrupa archivos y otros directorios en una estructura jerárquica.

"Modern Operating Systems" de Andrew S. Tanenbaum y Herbert Bos:
**Fichero (archivo):** Un archivo es una colección de datos almacenados en un dispositivo de almacenamiento secundario, que tiene un nombre y está estructurado de alguna manera. Los archivos pueden ser de varios tipos, como archivos de texto, archivos binarios o archivos ejecutables.

**Directorio:** Un directorio es una estructura de datos que contiene entradas de archivos y otros directorios. Los directorios permiten a los usuarios organizar y estructurar archivos de manera lógica y jerárquica.

"Operating Systems: Internals and Design Principles" de William Stallings:
**Fichero (archivo):** Un archivo es una entidad lógica en un sistema de archivos que contiene información y metadatos. Los archivos pueden ser de diferentes tipos, como archivos de texto, archivos binarios o archivos ejecutables, y se almacenan en dispositivos de almacenamiento secundario.

**Directorio**: Un directorio es una estructura lógica en un sistema de archivos que contiene información sobre archivos y otros directorios. Los directorios permiten a los usuarios organizar y estructurar archivos en una jerarquía, facilitando la búsqueda y el acceso a la información almacenada.

## Admon. y asignación del espacio libre

Los sistemas operativos utilizan varias técnicas y algoritmos para administrar y asignar espacio libre en el almacenamiento secundario (como discos duros o unidades de estado sólido) durante la creación de nuevos archivos. Algunas de las estrategias más comunes para asignar espacio libre son las siguientes:

**Asignación contigua**: En este enfoque, el sistema operativo asigna un espacio contiguo en el disco para el archivo completo. Esta asignación facilita el acceso rápido a los archivos, ya que todos los bloques de datos están ubicados uno junto al otro. Sin embargo, la asignación contigua puede provocar fragmentación externa, ya que el espacio libre se divide en bloques más pequeños y no contiguos a medida que se crean y eliminan archivos.

**Asignación enlazada**: En la asignación enlazada, el archivo se divide en bloques de igual tamaño y se almacena en bloques no contiguos en el disco. Cada bloque de datos contiene un enlace al siguiente bloque en la cadena. Este enfoque evita la fragmentación externa, pero puede resultar en un acceso más lento a los archivos, ya que los bloques de datos pueden estar dispersos por todo el disco. Además, la asignación enlazada puede generar fragmentación interna si el tamaño del archivo no es un múltiplo exacto del tamaño de bloque.

**Asignación indexada**: En este método, el sistema operativo utiliza una estructura de datos llamada tabla de índices para rastrear los bloques de datos de un archivo. Todos los bloques de datos pueden estar dispersos en el disco, pero la tabla de índices mantiene la ubicación de cada bloque. La asignación indexada permite un acceso rápido a los archivos y evita la fragmentación interna y externa. Sin embargo, este método requiere un espacio adicional para almacenar las tablas de índices.

**Asignación basada en extents**: Utilizada en sistemas de archivos como ext4 (Linux), esta técnica combina elementos de asignación contigua y asignación indexada. Un archivo se divide en extents, que son bloques contiguos de datos. Los extents se almacenan en una tabla de índices, lo que permite que el archivo ocupe bloques no contiguos en el disco. Este enfoque mejora el rendimiento y reduce la fragmentación.