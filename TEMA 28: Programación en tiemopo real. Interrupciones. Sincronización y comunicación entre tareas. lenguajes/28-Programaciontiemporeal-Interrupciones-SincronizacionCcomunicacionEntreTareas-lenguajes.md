# TEMA 28: Programación en tiempo real. Interrupciones. Sincronización y comunicación entre tareas. Lenguajes
>### Bloque 3
---
- [TEMA 28: Programación en tiempo real. Interrupciones. Sincronización y comunicación entre tareas. Lenguajes](#tema-28-programación-en-tiempo-real-interrupciones-sincronización-y-comunicación-entre-tareas-lenguajes)
  - [1. Introducción](#1-introducción)
  - [2. Sistemas de tiempo real](#2-sistemas-de-tiempo-real)
    - [2.1. Aspectos de integración y de rendimiento](#21-aspectos-de-integración-y-de-rendimiento)
    - [2.2. SS.OO. de tiempo real (SOT)](#22-ssoo-de-tiempo-real-sot)
    - [2.3. Características de los sistemas de tiempo real](#23-características-de-los-sistemas-de-tiempo-real)
    - [2.4. Clasificación de los sistemas de tiempo real](#24-clasificación-de-los-sistemas-de-tiempo-real)
    - [2.5. Fiabilidad y tolerancia a fallos](#25-fiabilidad-y-tolerancia-a-fallos)
      - [2.5.1 Técnicas de programación para la tolerancia a fallos](#251-técnicas-de-programación-para-la-tolerancia-a-fallos)
    - [2.6. Sincronización con sucesos externos](#26-sincronización-con-sucesos-externos)
    - [2.7. Sincronización interna](#27-sincronización-interna)
    - [2.8. Gestión de recursos](#28-gestión-de-recursos)
    - [2.9. Pruebas y depuración](#29-pruebas-y-depuración)
  - [3. Manejo de interrupciones](#3-manejo-de-interrupciones)
    - [3.1. Concepto de interrupción. Interrupciones múltiples](#31-concepto-de-interrupción-interrupciones-múltiples)
    - [3.2. Tratamiento de interrupciones](#32-tratamiento-de-interrupciones)
  - [4. Sincronización y comunicación de tareas](#4-sincronización-y-comunicación-de-tareas)
    - [4.1. Semáforos](#41-semáforos)
    - [4.2. Memoria compartida](#42-memoria-compartida)
    - [4.3. Intercambio de mensajes](#43-intercambio-de-mensajes)
    - [4.4. Buzones y puertos](#44-buzones-y-puertos)
    - [4.5. Pipes](#45-pipes)
    - [4.6. Llamadas a procedimientos remotos](#46-llamadas-a-procedimientos-remotos)
      - [4.7 Bases de datos de tiempo real](#47-bases-de-datos-de-tiempo-real)
  - [5. Lenguajes de programación en tiempo real](#5-lenguajes-de-programación-en-tiempo-real)
    - [5.1. ADA](#51-ada)
    - [5.2. Java](#52-java)
    - [5.3. C](#53-c)
  - [7. Conclusión](#7-conclusión)
    - [7.1. Relación del tema con la enseñanza en FP](#71-relación-del-tema-con-la-enseñanza-en-fp)
  - [8. Bibliografía](#8-bibliografía)

## 1. Introducción
## 2. Sistemas de tiempo real

Los sistemas de tiempo real son sistemas informáticos que necesitan interactuar con el mundo real de manera consistente y dentro de plazos de tiempo estrictos y predecibles. Estos sistemas están diseñados para procesar datos y reaccionar a los cambios en un período de tiempo específico. Si no se cumple este requisito, podrían producirse fallos graves, e incluso catastróficos. Por ejemplo, los sistemas de control de vuelo en aviones son sistemas de tiempo real donde un retraso en la respuesta podría tener consecuencias desastrosas (Liu, 2000).

### 2.1. Aspectos de integración y de rendimiento

En los sistemas de tiempo real, los aspectos de integración y rendimiento son fundamentales. La integración se refiere a cómo los diferentes componentes del sistema trabajan juntos para cumplir con los requisitos de tiempo real. Por ejemplo, en un automóvil moderno, diferentes sistemas como frenos, dirección y control de tracción deben trabajar de manera integrada para proporcionar una conducción segura y eficiente.

El rendimiento, por otro lado, se refiere a la capacidad del sistema para procesar tareas y manejar interrupciones en tiempo real. Esto podría compararse con un chef en una cocina ocupada que debe realizar múltiples tareas simultáneamente y responder a imprevistos sin retrasar el servicio (Burns & Wellings, 2019).

### 2.2. SS.OO. de tiempo real (SOT)

Los Sistemas Operativos de Tiempo Real (SOT) son componentes cruciales en los sistemas de tiempo real. Estos sistemas operativos están diseñados específicamente para manejar las demandas de las aplicaciones de tiempo real, proporcionando características como la planificación de tareas en tiempo real y la gestión de interrupciones. Por ejemplo, el sistema operativo RTLinux se utiliza en muchas aplicaciones industriales y científicas donde se requiere un control en tiempo real estricto (Laplante, 2017).

### 2.3. Características de los sistemas de tiempo real

Las características de los sistemas de tiempo real incluyen, entre otras, la capacidad de respuesta rápida, la predictibilidad, la confiabilidad y la eficiencia. Estas características son esenciales para garantizar que el sistema pueda cumplir con sus requisitos de tiempo real. Por ejemplo, un sistema de bolsa de valores debe ser capaz de procesar transacciones en milisegundos y hacerlo de manera confiable y eficiente para evitar pérdidas financieras (Liu, 2000).

### 2.4. Clasificación de los sistemas de tiempo real

Los sistemas de tiempo real pueden clasificarse de diversas formas, pero la más común es la división en sistemas de tiempo real duro y sistemas de tiempo real blando. En los sistemas de tiempo real duro, es absolutamente esencial que las tareas se completen dentro de un plazo determinado. Un ejemplo de esto podría ser un sistema de control de airbags en un automóvil, donde un retraso en la activación podría ser fatal.

Por otro lado, en los sistemas de tiempo real blando, aunque se prefiere que las tareas se completen a tiempo, no es esencial. Los retrasos son indeseables pero tolerables. Un ejemplo podría ser un reproductor de video en streaming, donde un retraso podría causar un ligero parpadeo en la imagen, pero no tendría consecuencias graves (Buttazzo, 2011).

### 2.5. Fiabilidad y tolerancia a fallos

En los sistemas de tiempo real, la fiabilidad y la tolerancia a fallos son vitales. La fiabilidad se refiere a la capacidad del sistema de funcionar correctamente durante un período prolongado de tiempo, mientras que la tolerancia a fallos se refiere a la capacidad del sistema de seguir funcionando correctamente incluso cuando ocurre un fallo.

Por ejemplo, en los sistemas de control de tráfico aéreo, la fiabilidad es esencial para garantizar que todos los aviones en el espacio aéreo estén rastreados en todo momento. Además, estos sistemas deben ser tolerantes a fallos, ya que un fallo en el sistema podría tener consecuencias catastróficas. Para garantizar la tolerancia a fallos, se suelen implementar técnicas como la redundancia, en la que se disponen sistemas de respaldo que pueden asumir el control si el sistema principal falla (Laplante, 2017).

#### 2.5.1 Técnicas de programación para la tolerancia a fallos

Existen varias técnicas de programación que se utilizan para implementar la tolerancia a fallos en sistemas de tiempo real. Una de estas técnicas es la redundancia, ya mencionada anteriormente, que puede ser tanto de hardware como de software. Otra técnica es la diversidad de diseño, en la que se utilizan diferentes enfoques para el diseño y la implementación de funciones críticas, de modo que si un enfoque falla, el otro puede seguir funcionando correctamente.

Un ejemplo de esto podría ser un sistema de control de vuelo, que podría tener un sistema de control principal y un sistema de respaldo que utilice un enfoque de diseño completamente diferente. De esta manera, si se encuentra un error en el sistema principal que causa un fallo, es menos probable que el sistema de respaldo tenga el mismo error y pueda asumir el control (Burns & Wellings, 2019).

### 2.6. Sincronización con sucesos externos

En los sistemas de tiempo real, a menudo es necesario sincronizarse con sucesos externos. Esto puede implicar responder a señales de entrada en tiempo real, como los sensores en un sistema de control de vuelo, o sincronizarse con eventos de tiempo, como un reloj en tiempo real.

Por ejemplo, en un sistema de producción automatizado, las máquinas deben sincronizarse con las cintas transportadoras y otras máquinas para garantizar un flujo de trabajo eficiente y sin problemas. Si una máquina se desincroniza, podría causar retrasos o incluso dañar los productos en la línea de producción (Buttazzo, 2011).

### 2.7. Sincronización interna

Aparte de la sincronización con eventos externos, la sincronización interna también es crucial en los sistemas de tiempo real. Esto se refiere a la coordinación de múltiples hilos de ejecución o tareas dentro del sistema. Por ejemplo, en un sistema operativo de tiempo real, puede ser necesario que una tarea espere a que otra tarea complete su trabajo antes de que pueda proceder. Para manejar esto, se utilizan mecanismos de sincronización como semáforos, monitores y candados.

Imagínese un sistema de control de tráfico en un cruce de trenes. Hay varias tareas que deben coordinarse: el control de las barreras, la señalización a los trenes y la detección de la posición de los trenes. Estas tareas deben sincronizarse con precisión para evitar accidentes (Burns & Wellings, 2019).

### 2.8. Gestión de recursos

La gestión eficiente de los recursos es esencial en cualquier sistema de tiempo real. Los recursos, como la CPU, la memoria y los dispositivos de E/S, deben asignarse y liberarse de manera eficiente para garantizar que todas las tareas se puedan completar en los plazos requeridos.

Por ejemplo, en un sistema de control de vuelo, puede haber múltiples tareas que requieran acceso a la CPU, como el control de la actitud del avión, la navegación y la comunicación con el control de tráfico aéreo. Un planificador de tareas de tiempo real en el sistema operativo debe garantizar que todas estas tareas tengan acceso a la CPU cuando lo necesiten y que se cumplan los plazos de tiempo real (Laplante, 2017).

### 2.9. Pruebas y depuración

Las pruebas y la depuración son partes esenciales del desarrollo de sistemas de tiempo real. Dado que estos sistemas a menudo operan en entornos críticos y deben ser extremadamente confiables, las pruebas y la depuración deben ser exhaustivas. Las pruebas a menudo implican la simulación de condiciones del mundo real y la comprobación de que el sistema responde de manera adecuada.

Por ejemplo, en el desarrollo de un sistema de frenado antibloqueo (ABS), se simularían situaciones de conducción en diferentes condiciones de carretera y clima para asegurar que el sistema siempre reacciona correctamente (Buttazzo, 2011).

## 3. Manejo de interrupciones

Las interrupciones son una parte crucial de los sistemas de tiempo real. Permiten al sistema responder a eventos externos de manera oportuna, lo que es esencial para muchos tipos de aplicaciones de tiempo real (Liu, 2000).

### 3.1. Concepto de interrupción. Interrupciones múltiples

Una interrupción es una señal que detiene la ejecución normal de un programa y provoca que se ejecute un conjunto específico de instrucciones, conocido como rutina de servicio de interrupción. Las interrupciones pueden ser generadas por una variedad de fuentes, como hardware (por ejemplo, un temporizador o un dispositivo de entrada/salida) o software (por ejemplo, una operación de división por cero en un programa).

En los sistemas de tiempo real, a menudo es necesario manejar múltiples interrupciones simultáneamente. Por ejemplo, en un sistema de control de vuelo, pueden llegar interrupciones del sistema de navegación, del sistema de comunicaciones y de los sensores de la aeronave al mismo tiempo. El sistema debe ser capaz de priorizar y manejar estas interrupciones de manera eficiente para garantizar una respuesta oportuna (Burns & Wellings, 2019).

### 3.2. Tratamiento de interrupciones

El tratamiento de interrupciones en un sistema de tiempo real es un proceso de múltiples pasos. Cuando llega una interrupción, el sistema primero debe guardar el estado actual del programa que se está ejecutando. Luego, ejecuta la rutina de servicio de interrupción correspondiente. Una vez que se ha completado la rutina de servicio de interrupción, el sistema restaura el estado del programa y continúa la ejecución.

En un sistema con múltiples interrupciones, puede haber situaciones en las que llegue una interrupción mientras se está procesando otra. En estos casos, el sistema puede tener que decidir si interrumpe la rutina de servicio de interrupción actual para manejar la nueva interrupción. Esta decisión puede depender de varios factores, como las prioridades de las interrupciones y los requisitos del sistema en términos de tiempo real (Laplante, 2017).

Para ilustrar este proceso, considere un sistema de control de tráfico aéreo. Si llega una interrupción indicando que un avión ha entrado en el espacio aéreo, el sistema podría tener que interrumpir la tarea que está realizando para procesar esta interrupción. Una vez que se ha tratado la interrupción, el sistema puede volver a la tarea que estaba realizando antes de que llegara la interrupción (Buttazzo, 2011).

## 4. Sincronización y comunicación de tareas

La sincronización y comunicación de tareas es un aspecto fundamental en los sistemas de tiempo real, especialmente en aquellos que son multiproceso o multihilo. Estas técnicas permiten coordinar la ejecución de varias tareas para que trabajen de manera cooperativa y efectiva (Laplante, 2017).

### 4.1. Semáforos

Los semáforos son una técnica comúnmente utilizada para la sincronización en sistemas de tiempo real. Un semáforo es una variable que se utiliza para controlar el acceso a un recurso compartido. Por ejemplo, si varias tareas necesitan acceder a un dispositivo de hardware, un semáforo puede utilizarse para asegurar que solo una tarea tenga acceso a la vez.

```pseudo
Semaphore s = 1 // Initialize semaphore

P(s): // Entry section
  while s <= 0 ; // Wait until resource is available
  s = s - 1 // Acquire resource

// Critical section: Access shared resource

V(s): // Exit section
  s = s + 1 // Release resource
```

### 4.2. Memoria compartida

La memoria compartida es un método de comunicación entre tareas en un sistema de tiempo real. En este modelo, varias tareas pueden acceder a una región común de memoria para leer y escribir datos.

```pseudo
SharedMemory memory // Initialize shared memory

Task1:
  memory.write(data) // Write data to shared memory

Task2:
  data = memory.read() // Read data from shared memory
```

### 4.3. Intercambio de mensajes

El intercambio de mensajes es otra técnica de comunicación en sistemas de tiempo real. En este modelo, las tareas comunican enviando y recibiendo mensajes.

```pseudo
Task1:
  send(Task2, message) // Send message to Task2

Task2:
  message = receive(Task1) // Receive message from Task1
```

### 4.4. Buzones y puertos

Los buzones y puertos son abstracciones que se utilizan para el intercambio de mensajes en algunos sistemas de tiempo real. Un buzón es una cola de mensajes que puede ser leída por una o más tareas. Un puerto es similar, pero puede ser utilizado para enviar y recibir mensajes entre diferentes sistemas.

```pseudo
Mailbox mailbox // Initialize mailbox

Task1:
  mailbox.post(message) // Post message to mailbox

Task2:
  message = mailbox.fetch() // Fetch message from mailbox
```

### 4.5. Pipes

Un pipe es una técnica que permite la comunicación entre dos tareas a través de un canal de lectura y escritura. Los datos escritos en el extremo de escritura del pipe pueden ser leídos desde el extremo de lectura.

```pseudo
Pipe pipe // Initialize pipe

Task1:
  pipe.write(data) // Write data to pipe

Task2:
  data = pipe.read() // Read data from pipe
```

### 4.6. Llamadas a procedimientos remotos

Las llamadas a procedimientos remotos permiten que una tarea en un sistema invoque un procedimiento en otro sistema. Esta es una forma potente de comunicación y sincronización en sistemas de tiempo real distribuidos.

```pseudo
Task1:
  result = remoteProcedureCall(Task2, procedure, args) // Call remote procedure

Task2:
  procedure(args) // Execute procedure
```

#### 4.7 Bases de datos de tiempo real

Las bases de datos de tiempo real son un medio especializado de comunicación y sincronización. Estas bases de datos pueden garantizar que las operaciones de lectura y escritura se completen dentro de plazos de tiempo específicos, lo que es crucial en muchos sistemas de tiempo real.

```pseudo
RealTimeDatabase db // Initialize real-time database

Task1:
  db.write(key, data, deadline) // Write data to database with a deadline

Task2:
  data = db.read(key, deadline) // Read data from database with a deadline
```

En todos estos casos, es crucial que el sistema de tiempo real pueda garantizar que las operaciones de sincronización y comunicación se completen dentro de los plazos requeridos. Los mecanismos de sincronización y comunicación deben ser diseñados e implementados cuidadosamente para evitar problemas como la inanición (cuando una tarea no puede progresar porque nunca obtiene acceso a un recurso) o la interbloqueo (cuando dos o más tareas se bloquean mutuamente porque cada una está esperando un recurso que la otra tiene) (Burns & Wellings, 2019).

## 5. Lenguajes de programación en tiempo real

Los lenguajes de programación juegan un papel crucial en el desarrollo de sistemas de tiempo real. Hay varios lenguajes de programación que proporcionan características que facilitan el desarrollo de software de tiempo real, como la programación concurrente y la manipulación directa de hardware (Buttazzo, 2011).

### 5.1. ADA

ADA es un lenguaje de programación de alto nivel diseñado por el Departamento de Defensa de los Estados Unidos. ADA proporciona un rico conjunto de características para la programación concurrente y en tiempo real, lo que lo convierte en una opción popular para los sistemas de tiempo real, especialmente en aplicaciones de defensa y aviación.

```ada
task body MyTask is
begin
  -- Task implementation here
end MyTask;
```

### 5.2. Java

Java es un lenguaje de programación de propósito general que también se utiliza en algunos sistemas de tiempo real. La Real-Time Specification for Java (RTSJ) proporciona un conjunto de extensiones a Java que facilitan el desarrollo de software de tiempo real.

```java
import javax.realtime.*;

public class MyRealTimeTask extends RealtimeThread {
    public void run() {
        // Task implementation here
    }
}
```

### 5.3. C

C es un lenguaje de programación de bajo nivel que se utiliza ampliamente en el desarrollo de sistemas operativos y software de tiempo real. C proporciona un control detallado sobre el hardware y la memoria, lo que puede ser beneficioso en sistemas de tiempo real donde el rendimiento y la eficiencia son críticos.

```c
#include <pthread.h>

void* myTask(void* arg) {
    // Task implementation here
    return NULL;
}

int main() {
    pthread_t thread;
    pthread_create(&thread, NULL, myTask, NULL);
    pthread_join(thread, NULL);
    return 0;
}
```

Estos lenguajes de programación, junto con sus respectivos ecosistemas de herramientas y bibliotecas, proporcionan una base sólida para el desarrollo de software de tiempo real. Sin embargo, el uso efectivo de estos lenguajes requiere una comprensión sólida de los conceptos y técnicas de programación de tiempo real (Laplante, 2017).
## 7. Conclusión

La programación en tiempo real es un campo esencial en la informática, y es especialmente relevante en los sistemas que deben responder a eventos dentro de un plazo determinado. A lo largo de este tema, hemos explorado varios aspectos de la programación en tiempo real, incluyendo los sistemas de tiempo real, la gestión de interrupciones, la sincronización y comunicación de tareas, y los lenguajes de programación relevantes (Buttazzo, 2011).

### 7.1. Relación del tema con la enseñanza en FP

La programación en tiempo real es un tema relevante para la Formación Profesional (FP) en informática, ya que muchos sistemas que los estudiantes pueden encontrarse en el mundo laboral son sistemas de tiempo real. Las habilidades y conceptos aprendidos en este tema pueden ser aplicados en una variedad de contextos, desde sistemas de control industrial hasta software para vehículos autónomos o sistemas de salud.

Enseñar este tema en FP implica no sólo enseñar los conceptos teóricos, sino también proporcionar a los estudiantes oportunidades para aplicar estos conceptos a través de proyectos y ejercicios prácticos. Los estudiantes podrían, por ejemplo, programar un sistema simple de tiempo real usando un lenguaje de programación como C o Java, o experimentar con la sincronización de tareas en un sistema operativo de tiempo real (Burns & Wellings, 2019).

En conclusión, la programación en tiempo real es un campo desafiante pero gratificante de la informática. Los educadores en FP pueden desempeñar un papel crucial en preparar a los estudiantes para trabajar en este campo, proporcionándoles los conocimientos y habilidades que necesitarán para tener éxito (Laplante, 2017).

## 8. Bibliografía

1. Burns, A., & Wellings, A. (2019). *Real-Time Systems and Programming Languages: Ada, Real-Time Java and C/Real-Time POSIX* (5th ed.). Addison-Wesley.

2. Liu, J. W. S. (2000). *Real-Time Systems*. Prentice Hall.

3. Laplante, P. A. (2017). *Real-Time Systems Design and Analysis: Tools for the Practitioner* (4th ed.). Wiley-IEEE Press.

4. Buttazzo, G. (2011). *Hard Real-Time Computing Systems: Predictable Scheduling Algorithms and Applications* (3rd ed.). Springer.

