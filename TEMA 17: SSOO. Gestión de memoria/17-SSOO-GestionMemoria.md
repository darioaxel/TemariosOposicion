# Introducción

## 
### Funciones del Sistema de gestión de memoria de un SO
Las principales funciones de un sistema gestor de memoria en un sistema operativo son:

Asignación de memoria: El sistema gestor de memoria es responsable de asignar espacio en la memoria principal a los procesos y sus datos. Esto implica mantener un registro de las áreas de memoria disponibles y ocupadas, y decidir qué proceso obtendrá qué espacio de memoria.

Protección de memoria: El sistema gestor de memoria debe garantizar que un proceso no pueda acceder ni modificar la memoria asignada a otro proceso. Esto se logra mediante el uso de técnicas de protección, como la asignación de direcciones de memoria base y límites para cada proceso.

Compartir memoria: A veces, es necesario que dos o más procesos compartan datos o recursos en memoria. El sistema gestor de memoria debe ser capaz de permitir el acceso compartido a la memoria, garantizando al mismo tiempo la seguridad y la integridad de los datos.

Gestión de la memoria virtual: La memoria virtual es una técnica que permite a un proceso utilizar más memoria de la que está físicamente disponible en la máquina. El sistema gestor de memoria debe ser capaz de administrar el intercambio de datos entre la memoria principal y la memoria secundaria (por ejemplo, disco duro), de tal manera que los procesos puedan ejecutarse sin problemas, aunque sus datos no quepan en la memoria principal.

Paginación y segmentación: Estas son técnicas que facilitan la administración y el acceso a la memoria. La paginación divide la memoria en bloques de tamaño fijo llamados páginas, mientras que la segmentación divide la memoria en segmentos de tamaño variable. El sistema gestor de memoria debe ser capaz de administrar y controlar el uso de estas técnicas para optimizar el rendimiento del sistema.

Liberación de memoria: El sistema gestor de memoria es responsable de liberar la memoria asignada a un proceso cuando este termina o ya no necesita un bloque de memoria. Esto implica actualizar el registro de áreas de memoria disponibles y liberar los recursos asignados al proceso.

Compactación de memoria: La compactación es un proceso que reorganiza la memoria física de tal manera que se agrupen los espacios vacíos contiguos. Esto ayuda a prevenir la fragmentación de la memoria y a maximizar el uso del espacio de memoria disponible.

Caché de memoria: El sistema gestor de memoria puede utilizar una caché para almacenar temporalmente datos recientes o frecuentemente utilizados. Esto puede mejorar el rendimiento del sistema al reducir el tiempo de acceso a estos datos, ya que se encuentran en una memoria más rápida y cercana al procesador.

Monitorización del rendimiento: El sistema gestor de memoria debe monitorear continuamente el rendimiento del sistema en relación con el uso de la memoria. Esto puede incluir la supervisión de la tasa de fallos de página, la cantidad de memoria utilizada y disponible, y la eficacia de las políticas de reemplazo de página. Esta información puede utilizarse para ajustar las políticas de gestión de memoria y mejorar el rendimiento general del sistema.

Políticas de reemplazo de página: En sistemas que utilizan memoria virtual, el gestor de memoria debe decidir qué páginas de memoria se deben reemplazar o eliminar cuando se necesita espacio para nuevas páginas. Para ello, se pueden emplear diferentes políticas de reemplazo, como el algoritmo de reemplazo óptimo, el algoritmo de reemplazo de la página menos recientemente utilizada (LRU) o el algoritmo del reloj, entre otros. El sistema gestor de memoria es responsable de aplicar e implementar estas políticas.

### Multiprogramación

La multiprogramación es una técnica utilizada en los sistemas operativos para permitir que varios procesos se ejecuten en la memoria principal al mismo tiempo. Esto permite una utilización más eficiente de los recursos de la computadora y un mejor rendimiento del sistema. Existen diferentes esquemas de multiprogramación en memoria principal, y a continuación, se describen algunos de ellos, incluidos ejemplos, pros y contras:

**Particiones fijas**:
En este esquema, la memoria principal se divide en particiones de tamaño fijo, y cada proceso se carga en una partición. El sistema operativo asigna las particiones a los procesos según sus necesidades de memoria.
Pros:

Simple de implementar y administrar.
Evita la fragmentación externa.
Contras:

Puede provocar fragmentación interna si la partición asignada es más grande que la memoria requerida por el proceso.
No es muy flexible, ya que el tamaño de las particiones es fijo.  
**Particiones variables**:  
Este esquema permite que las particiones de memoria se ajusten dinámicamente según las necesidades de memoria de los procesos. Cuando un proceso termina, su espacio de memoria se libera y se vuelve a combinar con la memoria adyacente disponible.  
Pros:

Más flexible que las particiones fijas, ya que el tamaño de las particiones se ajusta dinámicamente.
Reduce la fragmentación interna.
Contras:  

Más complejo de implementar y administrar que las particiones fijas.
Puede provocar fragmentación externa.  
**Paginación**:  
La paginación es un esquema de multiprogramación en el que la memoria se divide en bloques de tamaño fijo llamados páginas. Los procesos se dividen en páginas de igual tamaño y se cargan en cualquier espacio de memoria disponible, sin necesidad de que sean contiguos.
Pros:  
 
Evita la fragmentación externa.
Permite la asignación de memoria más granular, lo que reduce la fragmentación interna.
Facilita la implementación de la memoria virtual.
Contras:  

Requiere una tabla de páginas para mantener un registro de las páginas asignadas, lo que puede aumentar la sobrecarga del sistema.
Los fallos de página pueden afectar el rendimiento del sistema si no se gestionan adecuadamente.  
**Segmentación**:  
La segmentación es un esquema de multiprogramación en el que la memoria se divide en segmentos de tamaño variable, según las necesidades de los procesos. A diferencia de la paginación, los segmentos se cargan en áreas contiguas de memoria.  
Pros:  
Permite asignaciones de memoria más flexibles que la paginación.
Facilita el intercambio de datos y recursos entre procesos.  
Contras:  
Puede provocar fragmentación externa.
Requiere una tabla de segmentos para mantener un registro de los segmentos asignados, lo que puede aumentar la sobrecarga del sistema.  

En la actualidad, los sistemas operativos modernos, como Windows, Linux y macOS, utilizan principalmente la paginación y la segmentación, a menudo en combinación. Estos esquemas ofrecen una mejor flexibilidad y eficiencia en la gestión de la memoria, y permiten la implementación de características avanzadas, como la memoria virtual y el acceso compartido a recursos en memoria.



----

El **heap**, también conocido como montículo, es una región de la memoria gestionada por el sistema operativo en la que se asigna memoria dinámicamente a los programas en tiempo de ejecución. A diferencia de la memoria asignada en la pila (stack), la memoria asignada en el heap no sigue un patrón estructurado de acceso (como el comportamiento LIFO en la pila). La asignación de memoria en el heap se realiza según las necesidades del programa y se libera explícitamente cuando ya no es necesaria.

El heap es fundamental para la gestión de memoria en un sistema operativo, ya que proporciona flexibilidad en la asignación de memoria y permite el uso eficiente de recursos en situaciones donde el tamaño de la memoria requerida no se conoce en tiempo de compilación. A continuación, se describen algunas características del funcionamiento del heap y cómo aporta a la gestión de memoria en un sistema operativo:

Asignación dinámica de memoria: La principal ventaja del heap es que permite asignar memoria dinámicamente en tiempo de ejecución. Los programas pueden solicitar y liberar memoria según sea necesario, lo que permite a los sistemas operativos gestionar eficientemente los recursos y adaptarse a las necesidades de memoria de los programas.

Persistencia: A diferencia de la memoria asignada en la pila, la memoria en el heap no se libera automáticamente cuando una función termina su ejecución. Esto hace que el heap sea útil para almacenar estructuras de datos y objetos cuyo tiempo de vida excede el alcance de la función o el bloque de código en el que se crean.

Fragmentación: El heap está sujeto a la fragmentación, ya que la asignación y liberación de memoria se realiza de manera arbitraria. La fragmentación puede resultar en un uso ineficiente del espacio de memoria y una degradación del rendimiento del sistema. Los sistemas operativos emplean algoritmos de asignación de memoria y técnicas de compactación para minimizar la fragmentación y mejorar el rendimiento.

Funciones de asignación y liberación de memoria: Los lenguajes de programación proporcionan funciones específicas para solicitar y liberar memoria en el heap, como malloc(), calloc(), realloc() y free() en C o new y delete en C++. Estas funciones interactúan con el sistema operativo para gestionar la asignación y liberación de memoria en el heap.

Gestión de memoria automática: En algunos lenguajes de programación, como Java o Python, la gestión de memoria en el heap es automática, utilizando un recolector de basura (garbage collector) que libera automáticamente la memoria no utilizada por el programa. Esto reduce la carga en el programador para gestionar explícitamente la asignación y liberación de memoria, pero puede introducir una sobrecarga adicional en el sistema operativo y afectar el rendimiento en ciertas situaciones.

En general, quizás el 50 por ciento del espacio total de memoria de un ordenador puede estar sin utilizar en un momento dado. El sistema operativo posee y gestiona la memoria no utilizada, y se conoce colectivamente como el heap. El heap es extremadamente importante porque está disponible para ser utilizado por las aplicaciones durante la ejecución mediante las funciones C malloc (asignación de memoria) y free (liberación). El heap permite a los programas asignar memoria exactamente cuando la necesitan durante la ejecución de un programa, en lugar de preasignarla con una declaración de matriz de tamaño específico.

La respuesta rápida es: El Garbage Collector (GC) administra de forma automática la memoria, ya que es el encargado de liberar los objetos que ya no están en uso y que no serán usados en el futuro.

Pero ahora entremos a describir detalladamente el GC:

Muchos de ustedes (los lectores), son bastante jovenes y están acostumbrados a utilizar lenguajes de programación de alto nivel y tal vez nunca han escuchado o no se han preocupado por el concepto del GC. Pero muchos de los desarrolladores de lenguajes como C o C++ entre otros, saben lo que es estar pendiente de ir recolectando la basura (objetos que ya no se usarán) a mano. Es decir, escribir el código para recolectar dicha basura.

¿Por qué necesitamos un gestor de memoria automático como el GC?
Cuando creamos aplicaciones suficientemente grandes como para comenzar a perder el control de absolutamente todos los objetos que estamos creando, podemos caer en errores humanos como el ejemplo siguiente:

Supongamos que creamos un Objeto llamado A y dicho objeto vamos a referenciarlo desde diferentes punteros*, entonces podemos caer en el error de que en alguno de los punteros eliminemos el objeto y es allí cuando los problemas comienzan, ya que los demas punteros no podrán acceder a dicho objeto porque no existe.

En términos generales un puntero es una referencia a la dirección de memoria donde se encuentra un objeto.

Peor aún, imaginemos que el objeto A está referenciado por dos punteros p1 y p2, por error en p1 liberamos el objeto A, entonces esa dirección de memoria donde estaba el objeto A ya no tiene ningún valor, pero supongamos que dentro del proceso, la memoria ha ocupado dicha dirección con otro objeto diferente, entonces el puntero p2 estará haciendo referencia a un objeto que no era el esperado para el proceso, y los resultados son totalmente inesperados. Allí es cuando queremos que la tierra se abra y que nos trague.

Desventajas de los GC ?
Los GC permiten administrar de forma óptima el uso de la memoria realizando un proceso complejo de revisión a los objetos que se usan o no. Sin embargo, esto puede tener consecuencias en el performance de nuestras aplicaciones. Pero no se preocupen, tampoco es el fin del mundo, si haces un buen código los GC se encargarán de realizar ese proceso de forma óptima. Tampoco es que sea muy fuerte el proceso a menos que tu código sea un verdadero desastre.

Lo más eficiente es hacerlo manualmente por lo que no hay que estar preguntando si el objeto existe o si se necesitará en el futuro, simplemente cuando sabes que no vas a usar un objeto lo liberas, pero... debes ser MUY bueno codeando y utilizando la lógica del ciclo de vida de tus objetos.

¡Los GC al rescate!
Cada lenguaje de programación utiliza una lógica diferente para su GC. No hay una forma de decir cuál es el mejor ya que todos tienen sus ventajas y sus desventajas. Pero no te preocupes por eso, por ahora solo debes saber que el lenguaje de programación "moderno" que estás usando ya tiene un GC.

Cada vez que se crea un objeto se está solicitando espacio disponible en memoria RAM, ahora bien, la memoria RAM tiene un espacio reservado para la ejecución de los programas llamado HEAP, en este espacio es donde se van almacenando los objetos y es como una pila en la que cada objeto que va llegando se va almacenando.

El GC es el encargado de administrar este HEAP y estará revisando frecuentemente cuales objetos están en uso y cuales no lo están. A estos últimos los los debe remover del HEAP pero este proceso no es tan sencillo debido a que debe quitarlos de la pila y reorganizar el resto de objetos (compactar) para que el HEAP no se encuentre con espacios vacios.

Ahora el GC también organiza en generaciones los objetos. Qué significa esto? Bueno, el GC revisa los objetos que se van creando y los categoriza como Generación 0 y cada vez que encuentra un objeto que sobrevive a la limpieza de la memoria (el objeto sigue en uso), lo eleva a la siguiente generación hasta llegar a la 2.

¿Cuál es el objetivo? Identificar cuales son los objetos que son suceptibles de ser borrados más rápidamente y cuales son los que van a permanecer mucho tiempo durante la ejecución del programa.

Ejemplo, cuando hacemos un ciclo for, por lo general utilizamos la variable i para iterar sobre dicho ciclo. Esa variable cuando nace es categorizada como Generación 0 ya que muy seguramente va a morir muy rápido dentro de la ejecución del programa. Y efectivamente cuando el ciclo for termina, esa variable ya no es necesaria.

Ahora, las variables que tenemos de manera global, muy seguramente irán sobreviviendo a cada ciclo del GC y esas variables irán subiendo de generación. El GC realizará menos revisiones a los objetos de Generación 2 que a los objetos de generaciones menores.

----
**Linux** utiliza una combinación de paginación y segmentación para gestionar la memoria principal. La paginación es el método principal utilizado para administrar el espacio de memoria física, mientras que la segmentación se utiliza para organizar el espacio de memoria lógica en segmentos, como el segmento de código, datos y pila.

Aquí hay una descripción general de cómo Linux gestiona la memoria principal:

División en páginas: La memoria física se divide en bloques de tamaño fijo llamados páginas. Por otro lado, la memoria lógica (la vista de la memoria desde la perspectiva del proceso) también se divide en bloques de igual tamaño llamados páginas lógicas.

Asignación de marcos de página: La memoria física se asigna en forma de marcos de página a los procesos. Estos marcos de página se asignan a páginas lógicas en el espacio de memoria del proceso.

Tabla de páginas: Cada proceso tiene su propia tabla de páginas que mapea las páginas lógicas en el espacio de direcciones del proceso a los marcos de página en la memoria física.

Traducción de direcciones: Cuando un proceso accede a una dirección de memoria, el hardware de la CPU utiliza la tabla de páginas para traducir la dirección lógica en la dirección física correspondiente.

Segmentación: Aunque Linux utiliza principalmente paginación, la segmentación también está presente. La memoria lógica se organiza en segmentos, como el segmento de código, el segmento de datos y el segmento de pila. Estos segmentos están compuestos por páginas lógicas.

Memoria virtual: Linux implementa la memoria virtual utilizando un área de almacenamiento en disco llamada área de intercambio (swap). Cuando la memoria física se llena, los datos menos utilizados se intercambian entre la memoria principal y el área de intercambio en el disco para permitir que los procesos continúen ejecutándose.