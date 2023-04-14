

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
