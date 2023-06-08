# Tema 16. SSOO. Gestión de procesos.

# Introducción

La gestión de procesos por parte del sistema operativo es un tema crucial en el estudio de la informática y la administración de recursos de un sistema informático. Los sistemas operativos tienen la responsabilidad de gestionar y coordinar las actividades y el uso de los recursos del hardware y software de una computadora (Stallings, 2018). La eficiencia en la gestión de procesos es esencial para el rendimiento óptimo y la administración de recursos del sistema, especialmente en un entorno actual donde la complejidad y la demanda de recursos computacionales están en constante crecimiento.

Según Patterson y Hennessy (2018), el sistema operativo es el programa que controla la ejecución de todas las aplicaciones y servicios en un sistema informático. Su tarea principal es administrar los recursos del sistema, incluidos los procesos, la memoria, el almacenamiento y los dispositivos de entrada/salida. La gestión de procesos es uno de los componentes más importantes de esta tarea, ya que permite al sistema operativo controlar y coordinar la ejecución de múltiples procesos, asegurando que todos ellos reciban el tiempo y los recursos necesarios para su correcto funcionamiento.

Los sistemas operativos modernos, como lo señala Tanenbaum (2015), deben enfrentarse a una serie de desafíos en la gestión de procesos, como la asignación de recursos de manera justa y eficiente, la protección de procesos de interferencias no deseadas y el mantenimiento de un alto rendimiento en entornos de multitarea. En un entorno actual, donde los sistemas informáticos son cada vez más heterogéneos y se espera que soporten una creciente diversidad de aplicaciones y usuarios, es esencial contar con un conocimiento sólido de la gestión de procesos por parte del sistema operativo para garantizar un funcionamiento eficiente y seguro.

La investigación y el estudio de la gestión de procesos por parte del sistema operativo son necesarios para desarrollar sistemas operativos más eficientes, seguros y adaptativos, que puedan enfrentar los desafíos actuales y futuros en el ámbito de la informática.

## Historia de los SS.OO.
Los sistemas operativos (SSOO) han evolucionado a lo largo de la historia de la informática, adaptándose y mejorando con el tiempo para satisfacer las necesidades cambiantes de los usuarios y aprovechar los avances en la tecnología del hardware. A continuación, se presenta una breve introducción a los sistemas operativos actuales, mencionando ejemplos históricos y hitos importantes:

Los primeros sistemas operativos surgieron en la década de 1950 con la aparición de las primeras computadoras. Estos sistemas eran simples y se centraban en la ejecución de tareas por lotes, es decir, la ejecución secuencial de programas sin interacción con el usuario. Ejemplos de estos primeros sistemas operativos incluyen el IBM 701 y el General Motors-North American Aviation Monitor.

En la década de 1960, los sistemas operativos comenzaron a incorporar características de multiprogramación y tiempo compartido, lo que permitió a múltiples usuarios ejecutar programas de manera concurrente en una misma máquina. Un ejemplo destacado de esta época es el sistema operativo Compatible Time-Sharing System (CTSS) desarrollado en el MIT.

A mediados de la década de 1960, IBM lanzó el sistema operativo OS/360, un hito importante en la historia de los sistemas operativos. Fue uno de los primeros sistemas operativos en ser desarrollados para una familia completa de computadoras, desde mainframes hasta sistemas de mediano tamaño.

La década de 1970 vio el nacimiento de UNIX, desarrollado por Ken Thompson y Dennis Ritchie en los laboratorios Bell de AT&T. UNIX fue un hito en la historia de los SSOO por su diseño modular, la inclusión de un sistema de archivos jerárquico y el uso de un lenguaje de programación de alto nivel (C) para su implementación. UNIX influyó en el desarrollo de muchos sistemas operativos posteriores y dio lugar a una gran cantidad de variantes, como BSD y Linux.

En la década de 1980, Microsoft lanzó MS-DOS, un sistema operativo de línea de comandos que se convirtió en el estándar de facto para las computadoras personales IBM compatibles. Posteriormente, en 1985, Microsoft lanzó Windows, una interfaz gráfica de usuario (GUI) que se ejecutaba sobre MS-DOS y que marcaría el comienzo de una nueva era en la informática personal.

Apple también hizo una contribución significativa en esta época con el lanzamiento del sistema operativo Macintosh en 1984, que introdujo una interfaz gráfica de usuario fácil de usar y popularizó el uso del mouse en la informática personal.

En la década de 1990, Linux, un sistema operativo de código abierto basado en UNIX, fue desarrollado por Linus Torvalds. Linux ha crecido hasta convertirse en uno de los sistemas operativos más populares en el mundo, especialmente en servidores y dispositivos embebidos.

Hoy en día, los sistemas operativos actuales incluyen Windows, macOS (sucesor del sistema operativo Macintosh), Linux y sus diversas distribuciones, así como sistemas operativos móviles como Android e iOS. Estos sistemas operativos modernos incorporan características avanzadas como multiprocesamiento, memoria virtual, soporte para dispositivos de almacenamiento masivo y soporte para redes y comunicaciones, entre otros. La evolución de los sistemas operativos a lo largo de la historia ha sido impulsada por avances en la tecnología del hardware, las demandas crecientes de los usuarios y la necesidad de mayor seguridad y eficiencia en la gestión de recursos.

Los sistemas operativos modernos también han avanzado en áreas como la virtualización, permitiendo la ejecución de múltiples sistemas operativos en una sola máquina física, y el soporte para la computación en la nube, donde los recursos de computación se proveen a través de Internet.

Además, los sistemas operativos móviles como Android e iOS han revolucionado la forma en que interactuamos con la tecnología, permitiendo a los usuarios acceder a aplicaciones, servicios y contenido en cualquier momento y lugar a través de dispositivos móviles como teléfonos inteligentes y tabletas.

## Definición de SSOO

Un *sistema operativo es un conjunto de programas y componentes de software que actúan como una capa de abstracción y control entre el hardware de una computadora y las aplicaciones de usuario.* Su función principal es gestionar y coordinar los recursos del sistema, como la CPU, la memoria, los dispositivos de entrada/salida y el almacenamiento, para proporcionar un entorno eficiente, seguro y fácil de usar en el que los usuarios y las aplicaciones puedan interactuar y realizar tareas. Además, el sistema operativo ofrece servicios y funciones esenciales, como la gestión de procesos, la administración de memoria, el sistema de archivos y la interfaz de usuario, facilitando el desarrollo y la ejecución de programas de software.

# Proceso e hilo

## Proceso
Un proceso, según Stallings (2018), se define como una instancia de un programa en ejecución, que consta de instrucciones y datos asociados, así como de los recursos asignados por el sistema operativo. Un proceso es una entidad activa que requiere tiempo de CPU para llevar a cabo su tarea, y es el principal objeto de gestión de procesos en un sistema operativo.

### Bloque de Control de Procesos BCP
El Bloque de Control de Procesos (BCP) es una estructura de datos que contiene información sobre un proceso en particular (Stallings, 2018). El BCP incluye varias partes, como:

- **Identificador de Proceso (PID)**: un número único que identifica al proceso.
- **Estado del proceso**: indica si el proceso está ejecutándose, listo, bloqueado, etc.
- **Contador de programa (PC)**: almacena la dirección de la siguiente instrucción a ejecutar.
- **Registros**: almacena el contenido actual de los registros de la CPU para el proceso.
- **Espacio de direcciones**: contiene información sobre la asignación de memoria para el proceso.
- **Información de E/S**: detalles sobre los dispositivos de entrada/salida utilizados por el proceso.
- **Información de prioridad**: indica la prioridad del proceso para la asignación de recursos.


### El ciclo de vida de un proceso
Según Tanenbaum (2015), incluye varias etapas:

- **Creación**: el sistema operativo crea un nuevo proceso y asigna recursos.
- **Ejecución**: el proceso se encuentra en la CPU y se ejecuta.
- **Bloqueo**: el proceso espera un evento, como la finalización de una operación de E/S.
- **Desbloqueo**: el proceso es despertado por un evento y se encuentra listo para ejecutarse.
- **Terminación**: el proceso ha completado su ejecución y libera los recursos asignados.

### Concurrencia entre procesos

La **concurrencia** de procesos se refiere a la capacidad del sistema operativo para administrar múltiples procesos que se ejecutan simultáneamente, compartiendo recursos y tiempo de CPU (Patterson & Hennessy, 2018). Los sistemas operativos gestionan la concurrencia de procesos mediante el uso de técnicas como la multiprogramación y la planificación de procesos, asegurando que todos los procesos reciban una porción justa de los recursos y tiempo de CPU disponibles.

La **multiprogramación** permite al sistema operativo cargar varios procesos en memoria al mismo tiempo, mientras que la planificación de procesos decide cuándo y por cuánto tiempo se ejecuta cada proceso. La concurrencia de procesos mejora la utilización de recursos y permite a los sistemas informáticos realizar múltiples tareas de manera eficiente (Tanenbaum, 2015).

### Interrupciones y cambio de procesos

Cuando una interrupción ocurre, el sistema operativo debe realizar un cambio de contexto para atender la interrupción y posiblemente cambiar a otro proceso. El cambio de contexto es el proceso mediante el cual el sistema operativo guarda el estado actual del proceso en ejecución y carga el estado de un nuevo proceso que debe ser ejecutado. Los pasos que toma un sistema operativo para realizar un cambio de procesos debido a una interrupción son los siguientes (Stallings, 2018):

- Detectar la interrupción: El hardware detecta una interrupción y envía una señal al procesador. La interrupción puede ser generada por diversos motivos, como la finalización de una operación de E/S, la llegada de un temporizador, un error de hardware o una solicitud de otro proceso.

- Guardar el estado actual del proceso en ejecución: El sistema operativo guarda el estado actual del proceso en ejecución, incluyendo el contenido de los registros de la CPU, el contador de programa (PC) y cualquier otra información relevante, en su correspondiente Bloque de Control de Procesos (BCP).

- Determinar el tipo de interrupción y la rutina de servicio: El sistema operativo examina el vector de interrupciones para identificar el tipo de interrupción y la ubicación de la rutina de servicio correspondiente. El vector de interrupciones es una tabla que contiene las direcciones de las rutinas de servicio de interrupción, donde cada entrada de la tabla corresponde a un tipo específico de interrupción.

- Ejecutar la rutina de servicio de interrupción: El sistema operativo ejecuta la rutina de servicio de interrupción, que es un conjunto de instrucciones diseñadas para manejar la interrupción específica. Esta rutina puede realizar acciones como leer datos de un dispositivo de E/S, actualizar la información del proceso o cambiar el estado del proceso.

- Decidir el siguiente proceso a ejecutar: Tras atender la interrupción, el sistema operativo utiliza el planificador de procesos para decidir qué proceso debe ser ejecutado a continuación. Esto puede involucrar algoritmos de planificación como el Round Robin, prioridad o planificación basada en tiempo compartido, entre otros.

- Cargar el estado del nuevo proceso: El sistema operativo carga el estado del nuevo proceso seleccionado desde su BCP, restaurando el contenido de los registros de la CPU, el contador de programa y cualquier otra información relevante.

- Reanudar la ejecución del nuevo proceso: Finalmente, el sistema operativo reanuda la ejecución del nuevo proceso, comenzando desde el punto en el que fue interrumpido previamente.

El cambio de procesos por una interrupción permite que el sistema operativo responda a eventos externos y garantice un reparto justo de recursos y tiempo de CPU entre los diferentes procesos.
## Hilos (Threads)

Un hilo, también conocido como "thread" en inglés, es una unidad básica de ejecución dentro de un proceso. Un proceso puede contener múltiples hilos que se ejecutan concurrentemente y comparten el mismo espacio de memoria y recursos del sistema. Los hilos permiten a un proceso realizar múltiples tareas simultáneamente, mejorando el rendimiento y la capacidad de respuesta del sistema.

Cada hilo tiene su propio conjunto de registros, una pila de llamadas y un contador de programa, lo que le permite mantener su propio flujo de control y ejecutar instrucciones de forma independiente de otros hilos. Sin embargo, los hilos de un mismo proceso comparten el espacio de direcciones de memoria, los archivos abiertos, los descriptores de recursos y otras estructuras de datos del proceso.

La introducción de hilos en los sistemas operativos permite una mayor concurrencia y paralelismo en la ejecución de programas. Esto es especialmente útil en aplicaciones que realizan múltiples tareas simultáneas, como servidores web, aplicaciones de bases de datos o programas de interfaz gráfica de usuario.

La gestión de hilos en un sistema operativo es similar a la gestión de procesos, pero con un menor costo de creación, cambio de contexto y terminación. Los sistemas operativos pueden proporcionar soporte para hilos a nivel de usuario (User-Level Threads) o a nivel de núcleo (Kernel-Level Threads), dependiendo de la implementación y las necesidades del sistema.  

# Gestión de procesos
## Comunicación entre procesos (IPC):

La comunicación entre procesos (IPC, por sus siglas en inglés) permite que los procesos compartan información y colaboren en la realización de tareas. Existen dos enfoques principales para la IPC (Tanenbaum, 2015):

- Tubos (pipes): Los pipes permiten la comunicación unidireccional entre dos procesos relacionados. Un proceso escribe en un extremo del pipe, mientras que el otro proceso lee del otro extremo. Los pipes son útiles para implementar la comunicación en secuencias de procesos en sistemas operativos como Unix y Linux.

- Tubos con nombre (named pipes): Los named pipes son similares a los pipes regulares, pero permiten la comunicación entre procesos no relacionados. Los named pipes tienen un nombre en el sistema de archivos y pueden ser accedidos por cualquier proceso que tenga los permisos adecuados. Son comunes en sistemas operativos Unix, Linux y Windows.

- Sockets: Los sockets son mecanismos de comunicación bidireccional que permiten a los procesos comunicarse a través de redes o en la misma máquina. Los sockets son ampliamente utilizados en aplicaciones de red y sistemas distribuidos, y están disponibles en la mayoría de los sistemas operativos, incluidos Unix, Linux, Windows y macOS.

- Memoria compartida: La memoria compartida es un mecanismo de IPC que permite a varios procesos acceder a una región de memoria común. Los procesos pueden leer y escribir en la memoria compartida para intercambiar información. La memoria compartida es un método de comunicación eficiente y de alto rendimiento, pero requiere la implementación de mecanismos de sincronización para evitar condiciones de carrera y garantizar la coherencia de los datos.

- Mensajería (message passing): La mensajería es un mecanismo de IPC en el que los procesos intercambian mensajes para comunicarse y sincronizarse. Los mensajes pueden ser enviados a través de canales de comunicación establecidos entre procesos y pueden ser de tamaño fijo o variable. Los sistemas operativos y las bibliotecas de programación a menudo proporcionan funciones y abstracciones para facilitar el paso de mensajes entre procesos.

- Señales (signals): Las señales son un mecanismo de IPC que permite a los procesos enviar notificaciones de eventos a otros procesos. Las señales se utilizan para indicar la ocurrencia de eventos como interrupciones, terminación de procesos o cambios en el estado del sistema. Los sistemas operativos como Unix, Linux y Windows proporcionan soporte para señales y funciones para enviar, recibir y manejar señales entre procesos.

## Sincronización de procesos:

La sincronización de procesos es necesaria para garantizar la correcta secuencia y coordinación entre procesos que comparten recursos o dependen unos de otros. Existen varias técnicas y mecanismos de sincronización (Stallings, 2018):

- Semáforos: Son variables enteras utilizadas para controlar el acceso a recursos compartidos. Los semáforos pueden ser incrementados o decrementados para indicar la disponibilidad de un recurso, y los procesos pueden esperar o liberar un semáforo para obtener o liberar el acceso a dicho recurso. Los semáforos son utilizados en muchos sistemas operativos, incluidos Unix y Windows.

- Monitores: Son abstracciones de alto nivel que encapsulan datos compartidos y funciones de sincronización en una estructura de datos. Los monitores garantizan que solo un proceso puede acceder a los datos compartidos en un momento dado, evitando condiciones de carrera. Ejemplos de sistemas que utilizan monitores incluyen sistemas basados en lenguajes de programación concurrentes como Java y Ada.

- Variables de condición: Permiten a los procesos esperar hasta que se cumpla una condición específica. Las variables de condición se utilizan en combinación con monitores u otros mecanismos de sincronización para coordinar el acceso a recursos compartidos. Ejemplos de sistemas que utilizan variables de condición incluyen sistemas basados en POSIX y sistemas operativos que implementan la API de Pthreads.

## Concurrencia de procesos:

La competencia (también conocida como contienda) y la inanición (starvation) de procesos son dos problemas relacionados con la gestión de procesos en sistemas operativos, especialmente en situaciones donde los procesos compiten por recursos limitados.

* Competencia (contienda):

La competencia ocurre cuando varios procesos intentan acceder a un recurso compartido al mismo tiempo, lo que puede resultar en un rendimiento degradado y una subutilización de los recursos del sistema. Por ejemplo, si varios procesos intentan leer o escribir en el mismo archivo o dispositivo de E/S simultáneamente, es posible que tengan que esperar a que el recurso esté disponible, lo que provoca retrasos y una posible ralentización del sistema.

* Inanición (starvation):

La inanición ocurre cuando un proceso no puede acceder a un recurso necesario para su ejecución durante un período prolongado de tiempo debido a que otros procesos con mayor prioridad o demanda están monopolizando dicho recurso. Un proceso en inanición puede quedar en un estado de espera indefinidamente, lo que afecta negativamente su rendimiento y la eficiencia del sistema.

### Condiciones y prevención:

La competencia y la inanición pueden ser causadas por diversas condiciones y factores, como la asignación inadecuada de recursos, la falta de sincronización entre procesos o políticas de planificación ineficientes.

Las condiciones de Coffman fueron identificadas por primera vez por Edward G. Coffman, Jr., y sus colaboradores en 1971. Estas condiciones describen las cuatro circunstancias necesarias y suficientes que deben ocurrir simultáneamente para que se produzca un interbloqueo en un sistema:

- Exclusión mutua: Al menos un recurso debe ser compartido y no se puede utilizar por más de un proceso a la vez.
- Espera mientras se mantiene (hold and wait): Los procesos deben mantener al menos un recurso mientras esperan adquirir recursos adicionales.
- No apropiación (no preemption): Los recursos no pueden ser retirados forzosamente de un proceso que los está utilizando; solo el proceso que tiene el recurso puede liberarlo voluntariamente.
- Espera circular (circular wait): Debe existir un conjunto de procesos esperando recursos en una cadena circular, donde cada proceso está esperando un recurso que está siendo retenido por el siguiente proceso en la cadena.  

Para evitar interbloqueos, un sistema operativo debe diseñarse para eliminar al menos una de las condiciones de Coffman. Algunas estrategias para prevenir interbloqueos incluyen:

- Prevención de interbloqueos: Se asegura que el sistema nunca entre en un estado de interbloqueo al negar una o más condiciones de Coffman. Por ejemplo, se puede requerir que los procesos soliciten todos los recursos que necesitarán al mismo tiempo (eliminando la condición de espera mientras se mantiene), o se puede implementar una política de apropiación de recursos (eliminando la condición de no apropiación).

- Evitación de interbloqueos: Se permite que las condiciones de Coffman existan, pero se evalúa dinámicamente si otorgar o denegar las solicitudes de recursos podría llevar al sistema a un estado de interbloqueo. Un algoritmo comúnmente utilizado para la evitación de interbloqueos es el algoritmo del banquero.

- Detección y recuperación de interbloqueos: Se permite que el sistema entre en estados de interbloqueo, pero se implementan mecanismos para detectar y recuperarse de dichos estados. La detección de interbloqueos puede implicar el uso de gráficos de asignación de recursos y la búsqueda de ciclos en estos gráficos. La recuperación puede involucrar la terminación de procesos o la apropiación de recursos para romper el interbloqueo.

- Ignorar el problema: En algunos casos, el costo de prevenir, evitar o recuperarse de interbloqueos puede ser mayor que el costo de lidiar con interbloqueos ocasionales. En estos casos, un sistema operativo puede optar por no abordar el problema de interbloqueo y dejar que el usuario o el administrador del sistema maneje situaciones de interbloqueo según sea necesario.

## Planificación de procesos:
Los objetivos de la planificación de procesos en un sistema operativo son garantizar la utilización eficiente y justa de los recursos del sistema, así como proporcionar un buen rendimiento y una experiencia de usuario adecuada. Según la bibliografía estudiada (Stallings, 2018; Tanenbaum, 2015; Patterson & Hennessy, 2018), los objetivos principales de la planificación de procesos son:

- Maximizar la utilización de la CPU: La planificación de procesos debe asegurar que la CPU esté ocupada realizando trabajo útil la mayor parte del tiempo, minimizando el tiempo de inactividad.

- Maximizar el rendimiento: La planificación de procesos debe garantizar que se procese la mayor cantidad posible de trabajos en un período determinado, optimizando el rendimiento global del sistema.

- Minimizar el tiempo de respuesta: La planificación de procesos debe asegurar que los procesos interactivos reciban atención rápida y oportuna, minimizando el tiempo que un usuario debe esperar para obtener una respuesta del sistema.

- Minimizar el tiempo de espera: La planificación de procesos debe reducir el tiempo que los procesos pasan en cola esperando acceso a recursos, como la CPU o dispositivos de E/S.

- Proporcionar equidad en la asignación de recursos: La planificación de procesos debe garantizar que todos los procesos tengan una oportunidad justa de acceder a los recursos del sistema, evitando la inanición y la monopolización de recursos.

- Garantizar la previsibilidad y la estabilidad del sistema: La planificación de procesos debe proporcionar un comportamiento consistente y predecible en cuanto a la ejecución de procesos y la asignación de recursos.

Para lograr estos objetivos, los sistemas operativos implementan diversas políticas y algoritmos de planificación de procesos, como FIFO, SJF, Round Robin, planificación basada en prioridades y planificación de tiempo compartido (multinivel). Estas políticas y algoritmos tienen diferentes características y se adaptan mejor a diferentes tipos de cargas de trabajo y requisitos del sistema.

La selección e implementación de políticas y algoritmos de planificación adecuados es fundamental para lograr los objetivos de la planificación de procesos y garantizar un funcionamiento eficiente y equitativo del sistema operativo.

La planificación de procesos es el proceso mediante el cual el sistema operativo decide qué proceso debe ejecutar en un momento dado, y por cuánto tiempo. Existen varias políticas de planificación (Patterson & Hennessy, 2018):

**FIFO (First In, First Out)**: Los procesos son ejecutados en el orden en que llegan. Un ejemplo de sistema que utiliza esta política es el sistema operativo Batch, que procesa trabajos en un orden secuencial.

**SJF (Shortest Job First)**: Los procesos con el menor tiempo de ejecución estimado se ejecutan antes que los procesos con tiempos de ejecución más largos. Esta política es óptima en términos de tiempo de espera promedio y se utiliza en algunos sistemas de planificación de trabajos por lotes.

**Round Robin**: Los procesos se ejecutan en un orden cíclico, asignándoles un tiempo limitado, llamado "quantum", durante el cual pueden ejecutarse. Una vez que un proceso agota su quantum, el siguiente proceso en la cola comienza a ejecutarse. El Round Robin es una política de planificación ampliamente utilizada en sistemas operativos modernos, como Linux y Windows, debido a su simplicidad y equidad en la distribución del tiempo de CPU.

**Planificación basada en prioridades**: Los procesos se asignan a diferentes niveles de prioridad y los de mayor prioridad se ejecutan antes que los de menor prioridad. En caso de empate, se puede aplicar otra política de planificación, como Round Robin. La planificación basada en prioridades es común en sistemas operativos en tiempo real y en sistemas que admiten una amplia gama de aplicaciones y usuarios, como Unix y Windows.

**Planificación de tiempo compartido (multinivel)**: Los procesos se organizan en diferentes colas según su prioridad, y se aplica una política de planificación, como Round Robin, dentro de cada cola. La CPU se asigna a las colas en función de su prioridad y de la cantidad de procesos en cada cola. Un ejemplo de sistema que utiliza la planificación de tiempo compartido es el sistema operativo Unix, que implementa la planificación de múltiples colas (Multi-level Queue Scheduling).

Cada política de planificación tiene sus ventajas y desventajas, y el sistema operativo debe seleccionar la política más adecuada según las necesidades y características de las aplicaciones y del entorno en el que se ejecutan.


# Ejercicios sobre el tema
Los ejercicios prácticos en el ámbito de la gestión de procesos del sistema operativo pueden ayudar a los alumnos de ciclos formativos de grado superior en informática a desarrollar habilidades prácticas y a comprender mejor los conceptos teóricos. Aquí hay algunas ideas de ejercicios prácticos sobre este tema:

Simulación de algoritmos de planificación de procesos: Los alumnos pueden implementar y comparar diferentes algoritmos de planificación de procesos (FIFO, SJF, Round Robin, planificación basada en prioridades, etc.) en un entorno simulado. Esto les permitirá comprender cómo funcionan estos algoritmos y cómo afectan el rendimiento del sistema.

Creación y manipulación de procesos en sistemas operativos reales: Los alumnos pueden practicar la creación, manipulación y terminación de procesos utilizando comandos y funciones de sistemas operativos populares como Linux, Windows o macOS. Esto puede incluir la utilización de comandos como fork(), exec(), wait() en Linux, o el uso de las API de creación de procesos en Windows.

Comunicación entre procesos utilizando pasaje de mensajes o memoria compartida: Los alumnos pueden escribir programas que utilicen mecanismos de IPC, como pasaje de mensajes (por ejemplo, pipes o sockets) o memoria compartida, para comunicarse entre sí y coordinar la realización de tareas.

Implementación de mecanismos de sincronización: Los alumnos pueden practicar la implementación de semáforos, monitores y variables de condición en programas concurrentes para garantizar la correcta sincronización entre procesos que comparten recursos o dependen unos de otros.

Estudio de casos de sistemas operativos y sus técnicas de gestión de procesos: Los alumnos pueden investigar y analizar casos de sistemas operativos reales, como Linux, Windows o macOS, para entender cómo abordan la gestión de procesos, la sincronización y la comunicación entre procesos en un entorno real.

Análisis de rendimiento de sistemas operativos: Los alumnos pueden utilizar herramientas de monitoreo de rendimiento y análisis, como el Administrador de tareas en Windows, el Monitor del sistema en Linux o el Monitor de actividad en macOS, para observar cómo se administran los procesos, la memoria y los recursos del sistema en tiempo real.



# Bibliografía

> Patterson, D. A., & Hennessy, J. L. (2018). ***Computer Organization and Design MIPS Edition: The Hardware/Software Interface.*** Morgan Kaufmann.

> Stallings, W. (2018). ***Operating Systems: Internals and Design Principles.*** Pearson.

> Tanenbaum, A. S. (2015).***Modern Operating Systems***. Pearson.
> De Miguel Anasagasti (2016) ***Sistemas operativos***. Universidad politecnica de madrid


> 
