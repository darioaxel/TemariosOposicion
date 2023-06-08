# Tema 15. SSOO. Componentes. Estructura. Funciones.

# Introducción

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

Un sistema operativo es un conjunto de programas y componentes de software que actúan como una capa de abstracción y control entre el hardware de una computadora y las aplicaciones de usuario. Su función principal es gestionar y coordinar los recursos del sistema, como la CPU, la memoria, los dispositivos de entrada/salida y el almacenamiento, para proporcionar un entorno eficiente, seguro y fácil de usar en el que los usuarios y las aplicaciones puedan interactuar y realizar tareas. Además, el sistema operativo ofrece servicios y funciones esenciales, como la gestión de procesos, la administración de memoria, el sistema de archivos y la interfaz de usuario, facilitando el desarrollo y la ejecución de programas de software.

# Componentes de un SSOO

## Niveles de un sistema operativo
Los sistemas operativos (SSOO) pueden estructurarse en diferentes niveles o capas, lo que facilita su diseño, implementación y mantenimiento. A continuación, se presentan los niveles de un sistema operativo basados en la misma visión de los libros mencionados anteriormente:****

- **Núcleo (kernel)**: Es el núcleo del sistema operativo y la parte que se ejecuta en modo privilegiado o modo kernel. El núcleo es responsable de administrar directamente los recursos de hardware, como la CPU, la memoria y los dispositivos de E/S. También proporciona servicios fundamentales para la gestión de procesos, la comunicación entre procesos y la gestión de memoria.

- **Subsistemas de servicios del sistema operativo**: Estos subsistemas proporcionan servicios de alto nivel a los programas de usuario y abstraen los detalles del hardware subyacente. Algunos ejemplos incluyen el sistema de archivos, la gestión de red y los servicios de seguridad. Los subsistemas se comunican con el núcleo para solicitar recursos y servicios.

- Bibliotecas del sistema: Son conjuntos de funciones y rutinas de programación que facilitan a los desarrolladores de software la creación de aplicaciones y el acceso a los servicios del sistema operativo. Estas bibliotecas actúan como una interfaz entre las aplicaciones y los servicios del sistema operativo, permitiendo el uso de funciones comunes sin tener que implementarlas desde cero.

- Interfaz de usuario: Como se mencionó anteriormente, el sistema operativo debe proporcionar una interfaz de usuario para que los usuarios puedan interactuar con la computadora y sus programas. Esta interfaz puede ser una línea de comandos (CLI) o una interfaz gráfica de usuario (GUI). La interfaz de usuario se comunica con los subsistemas del sistema operativo y las bibliotecas del sistema para ejecutar comandos y acciones del usuario.

- Aplicaciones de usuario: Estos son programas y aplicaciones desarrollados para ejecutarse en el sistema operativo y que utilizan sus servicios y recursos. Las aplicaciones de usuario interactúan con el sistema operativo a través de las bibliotecas del sistema y las interfaces de usuario, y pueden incluir navegadores web, procesadores de texto, reproductores multimedia y juegos, entre otros.

## Componentes
Los componentes de un sistema operativo pueden variar dependiendo del enfoque y la implementación específica. Sin embargo, tomando como base los libros "Operating Systems: Internals and Design Principles" de William Stallings y "Modern Operating Systems" de Andrew S. Tanenbaum, podemos describir los siguientes componentes fundamentales de un sistema operativo:

- Gestión de procesos: El sistema operativo es responsable de administrar los procesos, que son las instancias de los programas en ejecución. Esto incluye la creación y destrucción de procesos, la asignación de recursos, la planificación del tiempo de CPU y la sincronización y comunicación entre procesos.

- Gestión de memoria: La memoria es un recurso crítico que el sistema operativo debe administrar de manera eficiente. Esto incluye la asignación y liberación de memoria para procesos, la administración de la memoria virtual y la implementación de políticas de reemplazo de páginas.

- Sistema de archivos: El sistema operativo debe proporcionar una forma de almacenar y acceder a la información en dispositivos de almacenamiento secundarios (como discos duros) de manera estructurada y organizada. Esto implica la implementación de un sistema de archivos, el cual gestiona la creación, eliminación, lectura y escritura de archivos, así como la asignación de espacio en disco y la protección de archivos.

- Gestión de entrada/salida (E/S): El sistema operativo es responsable de administrar los dispositivos de E/S, como teclados, ratones, impresoras y otros periféricos. Esto incluye la asignación y liberación de recursos de E/S, la abstracción y el control de acceso a estos dispositivos y la comunicación entre el hardware y el software.

- Interfaz de usuario: El sistema operativo debe proporcionar una forma para que los usuarios interactúen con la computadora y los programas. Esta interfaz puede ser en forma de una línea de comandos (CLI) o una interfaz gráfica de usuario (GUI), permitiendo a los usuarios ejecutar programas, manipular archivos y ajustar la configuración del sistema.

- Gestión de seguridad y protección: El sistema operativo debe garantizar que los recursos de la computadora estén protegidos y utilizados de manera apropiada. Esto implica implementar mecanismos de autenticación, autorización y auditoría, así como garantizar la integridad y confidencialidad de los datos almacenados.

- Comunicación y sincronización: El sistema operativo debe proporcionar mecanismos para la comunicación y sincronización entre procesos y/o hilos de ejecución, ya sea dentro de un sistema o en sistemas distribuidos a través de una red.

# Estructuras de los SS.OO.

- **Monolítico**: En un sistema operativo monolítico, todo el código del sistema operativo se encuentra en un único bloque de código y se ejecuta en el mismo espacio de direcciones de memoria. Este enfoque permite una comunicación rápida y eficiente entre los diferentes componentes del sistema operativo, pero puede ser difícil de mantener y actualizar debido a la falta de modularidad y aislamiento entre los componentes.

- **Micronúcleo (Microkernel)**: Un sistema operativo basado en un micronúcleo tiene un núcleo pequeño y mínimo que se ejecuta en modo privilegiado, mientras que la mayoría de los servicios del sistema operativo, como la gestión de procesos, la gestión de memoria y el sistema de archivos, se ejecutan en modo usuario como procesos separados. Este enfoque proporciona mayor modularidad y aislamiento entre los componentes, lo que facilita su mantenimiento y actualización. Sin embargo, la comunicación entre los componentes puede ser más lenta en comparación con un sistema monolítico debido al uso de mecanismos de comunicación entre procesos (IPC).

- **Capas (Layered)**: Los sistemas operativos de capas organizan sus componentes en una serie de niveles o capas, donde cada capa proporciona servicios a la capa superior y utiliza los servicios de la capa inferior. Este enfoque permite una estructura modular y bien definida, lo que facilita el diseño, la implementación y la depuración del sistema operativo. Sin embargo, el rendimiento puede verse afectado debido a la sobrecarga de comunicación entre las capas.

- **Modelo cliente-servidor**: En un sistema operativo basado en el modelo cliente-servidor, los servicios del sistema operativo se implementan como procesos de servidor independientes que se comunican con otros procesos cliente mediante mecanismos de comunicación entre procesos (IPC). Este enfoque puede ser utilizado en sistemas operativos distribuidos y permite una mayor escalabilidad y flexibilidad en la asignación de recursos y la provisión de servicios. Sin embargo, la sobrecarga de comunicación entre los procesos cliente y servidor puede afectar el rendimiento del sistema.

- **Máquinas virtuales (Virtual Machines):** Los sistemas operativos que utilizan máquinas virtuales proporcionan abstracciones de hardware a los programas de usuario en forma de múltiples instancias de una máquina virtual. Cada máquina virtual ejecuta su propio sistema operativo y aplicaciones en un entorno aislado, lo que permite mayor seguridad, flexibilidad y capacidad de administración. Los sistemas operativos de este tipo a menudo incluyen un hipervisor o un monitor de máquinas virtuales (VMM) que administra y controla el acceso a los recursos del hardware subyacente.

# Tipos de SS.OO.
Los tipos de sistemas operativos más relevantes que han existido a lo largo de la historia incluyen:

- Sistemas operativos por lotes (Batch): Estos sistemas operativos, que surgieron en los primeros días de la informática, se centraban en la ejecución secuencial de programas sin interacción con el usuario. Los trabajos se agrupaban en lotes y se procesaban uno tras otro, lo que permitía un mejor aprovechamiento de los recursos de la computadora pero con tiempos de respuesta largos.

- Sistemas operativos de tiempo compartido (Time-sharing): En estos sistemas operativos, el tiempo de CPU se divide entre múltiples usuarios, lo que permite a varios programas ejecutarse de manera concurrente en una misma máquina. Los sistemas de tiempo compartido mejoraron la eficiencia y la interacción con el usuario al proporcionar un entorno multitarea y multiusuario.

- Sistemas operativos de tiempo real (Real-time): Estos sistemas operativos están diseñados para controlar procesos y aplicaciones en tiempo real, es decir, para responder a eventos y acciones en un tiempo determinado y predecible. Los sistemas de tiempo real son críticos en aplicaciones como sistemas de control industrial, robótica y sistemas de navegación.

- Sistemas operativos de red (Network): Los sistemas operativos de red están diseñados para permitir la comunicación y el intercambio de recursos entre computadoras conectadas en una red. Estos sistemas operativos proporcionan funciones de gestión de redes y comunicación, así como acceso a recursos compartidos, como archivos y dispositivos de hardware.

- Sistemas operativos distribuidos: Los sistemas operativos distribuidos integran un conjunto de computadoras independientes y sus recursos en una única entidad lógica y coherente. Estos sistemas operativos proporcionan la ilusión de un sistema de computación unificado y están diseñados para aprovechar al máximo los recursos disponibles en una red de computadoras.

- Sistemas operativos de computadoras personales: Estos sistemas operativos están diseñados para su uso en computadoras personales, como ordenadores de escritorio, portátiles y estaciones de trabajo. Estos sistemas operativos incluyen características como una interfaz gráfica de usuario (GUI), soporte para múltiples dispositivos de hardware y una amplia variedad de aplicaciones de software.

- Sistemas operativos móviles: Los sistemas operativos móviles están diseñados para dispositivos móviles, como teléfonos inteligentes y tabletas. Estos sistemas operativos ofrecen funciones específicas para dispositivos móviles, como una interfaz táctil, soporte para aplicaciones móviles, conectividad inalámbrica y funciones de ahorro de energía.

## Clasificación de los sistemas operativos

Algunas de las clasificaciones más comunes son:

* Según la cantidad de usuarios:  
a. Monousuario: Sistemas operativos diseñados para ser utilizados por un único usuario en un momento dado. Ejemplo: MS-DOS.  
b. Multiusuario: Sistemas operativos que permiten la utilización simultánea por parte de múltiples usuarios, proporcionando mecanismos de protección y aislamiento entre ellos. Ejemplo: UNIX, Linux.

* Según la cantidad de tareas:  
a. Monotarea: Sistemas operativos que solo pueden ejecutar un proceso o tarea a la vez. Ejemplo: MS-DOS.  
b. Multitarea: Sistemas operativos que permiten la ejecución simultánea de múltiples procesos o tareas, gestionando el tiempo y los recursos que se asignan a cada uno. Ejemplo: Windows, macOS, Linux.

* Según la estructura:  
a. Monolíticos: Sistemas operativos cuyo núcleo incluye todos los servicios y controladores de hardware en un único bloque de código. Ejemplo: UNIX tradicional.  
b. Microkernel: Sistemas operativos con un núcleo mínimo que solo proporciona servicios básicos, mientras que los servicios adicionales se implementan en procesos separados. Ejemplo: Minix, QNX.  
c. Exokernel: Sistemas operativos que permiten a las aplicaciones acceder directamente al hardware, proporcionando un control más detallado sobre los recursos. Ejemplo: ExOS, Aegis.

* Según el tipo de computadora o dispositivo:  
a. Sistemas operativos para mainframes: Diseñados para ser utilizados en grandes sistemas informáticos que manejan grandes volúmenes de datos y usuarios. Ejemplo: z/OS de IBM.  
b. Sistemas operativos para servidores: Orientados a proporcionar servicios a otros sistemas o dispositivos en una red. Ejemplo: Windows Server, Linux.  
c. Sistemas operativos para estaciones de trabajo y computadoras personales: Diseñados para uso individual o en grupos de trabajo. Ejemplo: Windows, macOS, Linux.  
d. Sistemas operativos para dispositivos móviles: Diseñados específicamente para dispositivos móviles como teléfonos inteligentes y tabletas. Ejemplo: Android, iOS.

* Según la aplicación y el entorno:  
a. Sistemas operativos de propósito general: Diseñados para ser utilizados en una amplia variedad de aplicaciones y entornos. Ejemplo: Windows, macOS, Linux.  
b. Sistemas operativos de tiempo real: Diseñados para sistemas que requieren una respuesta rápida y predecible a eventos externos, como sistemas de control industrial o robótica. Ejemplo: QNX, VxWorks.  
c. Sistemas operativos embebidos: Diseñados para ser utilizados en sistemas embebidos o dispositivos de propósito específico. Ejemplo: FreeRTOS, Embedded Linux.

Estas clasificaciones no son mutuamente excluyentes, y un sistema operativo puede pertenecer a varias categorías al mismo tiempo. Por ejemplo, Linux es un sistema operativo multiusuario, multitarea y de propósito general, que puede ser utilizado en servidores

## Sistemas Operativos Actual

Android es un sistema operativo que puede ser clasificado y descrito de la siguiente manera, según las clasificaciones, estructuras y tipos proporcionados por los autores mencionados:

* Cantidad de usuarios: Android es principalmente un sistema operativo monousuario, ya que está diseñado para ser utilizado por un único usuario en dispositivos como teléfonos inteligentes y tabletas. Sin embargo, admite múltiples perfiles de usuario con ciertas restricciones y aislamiento entre ellos, especialmente en el caso de tabletas.

* Cantidad de tareas: Android es un sistema operativo multitarea, ya que permite la ejecución simultánea de múltiples procesos y aplicaciones. Gestiona el tiempo y los recursos asignados a cada proceso y puede suspender y reanudar aplicaciones según sea necesario para optimizar el rendimiento y la duración de la batería.

* Estructura: Android utiliza un enfoque de kernel monolítico modificado, basado en el kernel de Linux. El kernel de Linux proporciona servicios básicos de sistemas operativos y controladores de hardware. Sin embargo, Android también incorpora componentes adicionales, como la máquina virtual de Android (Dalvik o ART) y los servicios de Google, que permiten ejecutar aplicaciones específicas de Android y proporcionan una capa de abstracción adicional entre el hardware y las aplicaciones.

* Tipo de computadora o dispositivo: Android es un sistema operativo para dispositivos móviles, diseñado específicamente para teléfonos inteligentes, tabletas y otros dispositivos móviles, como relojes inteligentes y televisores.

* Aplicación y entorno: Android es un sistema operativo de propósito general para dispositivos móviles, ya que admite una amplia variedad de aplicaciones y entornos. Sin embargo, también puede adaptarse para su uso en sistemas embebidos y dispositivos de propósito específico, como sistemas de entretenimiento en automóviles o dispositivos IoT.

# Bibliografía
* De Miguel Anasagasti, P., & Gómez Pérez, J. J. (1999). Sistemas Operativos: una visión aplicada. McGraw-Hill/Interamericana de España.
* Tanenbaum, A. S., & Bos, H. (2014). Modern Operating Systems (4th ed.). Pearson.
* Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). Operating System Concepts (10th ed.). John Wiley & Sons.
