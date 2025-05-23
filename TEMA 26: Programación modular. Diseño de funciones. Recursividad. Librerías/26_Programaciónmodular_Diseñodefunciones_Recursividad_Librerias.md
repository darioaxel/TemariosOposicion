# Tema 26. Programación Modular. Diseño de funciones. Recursividad. Librerías
> #### Bloque 3
---
- [Tema 26. Programación Modular. Diseño de funciones. Recursividad. Librerías](#tema-26-programación-modular-diseño-de-funciones-recursividad-librerías)
  - [1. Introducción](#1-introducción)
  - [2. Programación modular](#2-programación-modular)
    - [2.1. Definición y características](#21-definición-y-características)
    - [2.2. Ventajas e inconvenientes](#22-ventajas-e-inconvenientes)
    - [2.3. Módulos](#23-módulos)
  - [3. Funciones y procedimientos](#3-funciones-y-procedimientos)
    - [3.1. Funciones](#31-funciones)
    - [3.2. Procedimientos](#32-procedimientos)
    - [3.3 Paso de parámetros](#33-paso-de-parámetros)
      - [3.3.1 Paso por valor y paso por referencia](#331-paso-por-valor-y-paso-por-referencia)
      - [3.3.2 Ámbito (scope)](#332-ámbito-scope)
- [Programación Modular](#programación-modular)
  - [4. Recursividad](#4-recursividad)
    - [4.1. Características y tipos](#41-características-y-tipos)
  - [5. Librerías](#5-librerías)
    - [5.1. Composición y estructura](#51-composición-y-estructura)
    - [5.2. Características](#52-características)
    - [5.3. Tipos](#53-tipos)
  - [6. Diseño de funciones y procedimientos](#6-diseño-de-funciones-y-procedimientos)
  - [6.1. Diseño estructurado](#61-diseño-estructurado)
  - [6.2. Atributos de la calidad de un diseño](#62-atributos-de-la-calidad-de-un-diseño)
  - [7. Conclusión](#7-conclusión)
  - [7.1. Relación del tema con la enseñanza en FP](#71-relación-del-tema-con-la-enseñanza-en-fp)
  - [8 Bibliografía](#8-bibliografía)


## 1. Introducción

## 2. Programación modular

*La **programación modular** es un enfoque de diseño de software que subdivide una aplicación en una serie de partes o módulos funcionales separados. Cada módulo se centra en una única responsabilidad y puede funcionar de forma independiente. Este enfoque tiene como objetivo hacer que los programas sean más fáciles de leer, entender, mantener y reutilizar.*

La programación modular surgió en los años 60 y 70 como respuesta a los desafíos que planteaba el crecimiento de los programas de software. A medida que los programas se volvían más grandes y complejos, era cada vez más difícil entender y mantener todo el código en un solo lugar. La programación modular ofrecía una solución a este problema, al permitir que los desarrolladores dividieran los programas en piezas más pequeñas y manejables.


### 2.1. Definición y características

En la programación modular cada módulo es una unidad independiente que puede ser compilada y probada por separado.
Las principales características de la programación modular incluyen:

- **Cohesión:** cada módulo realiza una única tarea o función.
- **Encapsulación:** los detalles de implementación de un módulo están ocultos a los demás módulos.
- **Independencia:** los módulos pueden ser desarrollados y probados independientemente.

### 2.2. Ventajas e inconvenientes

Las ventajas de la programación modular incluyen:

- Facilita la comprensión del código.
- Permite la reutilización de código.
- Facilita el mantenimiento y la depuración.

Los inconvenientes pueden incluir:

- Puede requerir más tiempo y esfuerzo para diseñar y desarrollar módulos eficientes.
- Es posible que no sea la opción más eficiente para programas pequeños o simples.

### 2.3. Módulos

Un módulo es una unidad de código independiente que puede contener funciones, procedimientos, clases, entre otros. Los módulos pueden importarse en otros módulos o programas para reutilizar su funcionalidad.

## 3. Funciones y procedimientos

Las funciones y los procedimientos son bloques de código reutilizables que realizan una tarea específica dentro de un programa.

### 3.1. Funciones

Una función es un bloque de código que se ejecuta cuando se llama. En general, una función toma uno o más argumentos y devuelve un valor.

### 3.2. Procedimientos

Un procedimiento, también conocido como una función que no devuelve un valor, es similar a una función pero no devuelve un valor. En lugar de eso, realiza alguna acción, como imprimir en la pantalla o modificar una variable.

### 3.3 Paso de parámetros

El paso de parámetros es el proceso mediante el cual se proporcionan argumentos a una función o procedimiento.

#### 3.3.1 Paso por valor y paso por referencia

El paso por valor significa que se pasa una copia del valor del argumento a la función. Por otro lado, el paso por referencia significa que se pasa una referencia al argumento original, permitiendo que la función modifique el valor original.

#### 3.3.2 Ámbito (scope)

El ámbito de una variable se refiere a la región de código en la que una variable es visible y acces

# Programación Modular

La **programación modular **es un enfoque de diseño de software que subdivide una aplicación en una serie de partes o módulos funcionales separados. Cada módulo se centra en una única responsabilidad y puede funcionar de forma independiente. Este enfoque tiene como objetivo hacer que los programas sean más fáciles de leer, entender, mantener y reutilizar.

La programación modular surgió en los años 60 y 70 como respuesta a los desafíos que planteaba el crecimiento de los programas de software. A medida que los programas se volvían más grandes y complejos, era cada vez más difícil entender y mantener todo el código en un solo lugar. La programación modular ofrecía una solución a este problema, al permitir que los desarrolladores dividieran los programas en piezas más pequeñas y manejables.


La programación modular es beneficiosa por varias razones:

Legibilidad: Los módulos más pequeños y bien definidos son más fáciles de leer y entender que un gran bloque de código.

Mantenibilidad: Es más fácil hacer cambios en un módulo individual sin afectar al resto del programa.

Reutilización de código: Los módulos que realizan funciones útiles pueden reutilizarse en diferentes programas.

Depuración: Los errores son más fáciles de localizar y corregir cuando el código está dividido en módulos.

Desarrollo paralelo: Diferentes equipos o individuos pueden trabajar en diferentes módulos al mismo tiempo, lo que puede acelerar el proceso de desarrollo.

## 4. Recursividad

La recursividad es un concepto fundamental en la programación que se refiere a la capacidad de una función o procedimiento de llamarse a sí misma de forma repetitiva hasta alcanzar una condición de salida o base que detenga la recursión. En términos más técnicos, la recursividad es un método que permite la definición de una función en términos de sí misma.

El uso de la recursividad en la programación puede ser muy útil para resolver problemas que involucran estructuras de datos complejas o para simplificar la implementación de algoritmos que involucran iteraciones complejas. Por ejemplo, la recursividad es comúnmente utilizada en la implementación de algoritmos de búsqueda, ordenamiento y análisis de árboles.

Sin embargo, la recursividad también puede llevar a errores y problemas de rendimiento si no se utiliza adecuadamente. Por lo tanto, es importante tener en cuenta ciertas consideraciones al utilizar la recursividad en la programación, como establecer una condición de salida clara y asegurarse de que la recursión no se vuelva infinita.

### 4.1. Características y tipos

La estructura de una función recursiva consta de dos partes principales: el *caso base* y el *caso recursivo*.

- El **caso base** es la condición que detiene la recursión. Es decir, es el caso en el que la función deja de llamarse a sí misma y devuelve un valor. Este caso es fundamental para evitar la recursión infinita y asegurar que la función se detenga en algún momento.
- El **caso recursivo**, por otro lado, es la parte de la función que se llama a sí misma. En este caso, se realiza una llamada a la misma función con una entrada ligeramente diferente. En cada llamada, se acerca al caso base hasta que se alcanza y se devuelve un valor.
- La **combinación del caso base y el caso recursivo** es lo que hace que una función sea recursiva. La función se llama a sí misma varias veces hasta que se alcanza el caso base, momento en el que se devuelve un valor y la recursión se detiene.

Por ejemplo, una función recursiva para calcular el factorial de un número podría tener la siguiente estructura:

```pseudocode
funcion factorial(n):
  si n == 0:
    devuelve 1
  sino:
    devuelve n * factorial(n-1)
```

En este caso, el caso base es cuando n es igual a cero, momento en el que se devuelve 1. El caso recursivo es n * factorial(n-1), donde se llama a la función factorial con un valor ligeramente menor en cada llamada hasta que se alcanza el caso base.
Existen varios tipos de funciones recursivas, entre ellas:

- **Recursión lineal:** en este tipo de recursión, la función se llama a sí misma solo una vez en cada llamada. Por lo tanto, la función se llama "lineal". Un ejemplo de una función recursiva lineal podría ser:
- 
```pseudocode
funcion suma(n):
  si n == 0:
    devuelve 0
  sino:
    devuelve n + suma(n-1)
```  

En este caso, la función suma se llama a sí misma solo una vez en cada llamada, lo que la hace una función recursiva lineal.

- **Recursión de cola:** este tipo de recursión ocurre cuando la llamada recursiva es la última operación en la función. En otras palabras, no hay operaciones adicionales que se realicen después de la llamada recursiva. Esto se llama recursión de cola porque las llamadas recursivas se alinean en una cola. Un ejemplo de una función recursiva de cola podría ser:
```pseudocode
funcion factorial(n, acumulador=1):
  si n == 0:
    devuelve acumulador
  sino:
    devuelve factorial(n-1, acumulador*n)
``` 

En este caso, la llamada recursiva se realiza como la última operación en la función y se utiliza un parámetro adicional acumulador para realizar la multiplicación acumulativa. Esta es una función recursiva de cola.

- **Recursión múltiple:** en este tipo de recursión, la función se llama a sí misma varias veces en cada llamada. Por lo tanto, la función se llama "múltiple". Un ejemplo de una función recursiva múltiple podría ser:
```pseudocode
funcion fibonacci(n):
  si n == 0:
    devuelve 0
  sino si n == 1:
    devuelve 1
  sino:
    devuelve fibonacci(n-1) + fibonacci(n-2)
```

En este caso, la función fibonacci se llama a sí misma dos veces en cada llamada (una para n-1 y otra para n-2), lo que la hace una función recursiva múltiple.

## 5. Librerías

En programación y desarrollo de aplicaciones, una librería (también conocida como biblioteca) es un conjunto de funciones, clases y/o módulos preescritos que pueden ser utilizados por otros programas o aplicaciones para realizar tareas específicas. Las librerías están diseñadas para facilitar el desarrollo de software al proporcionar una funcionalidad comúnmente necesaria sin que el programador tenga que escribir todo el código desde cero.  

Las librerías pueden ser específicas de un lenguaje de programación o de un entorno de desarrollo en particular. Por ejemplo, una librería para Python puede contener funciones para trabajar con matemáticas, procesamiento de texto o gráficos, mientras que una librería para Java puede proporcionar clases para interactuar con bases de datos o realizar operaciones de red.

Al utilizar una librería, el programador no tiene que preocuparse por implementar algoritmos complejos o lidiar con la complejidad técnica detrás de una tarea determinada. En cambio, pueden simplemente llamar a las funciones proporcionadas por la librería y utilizarlas como una "caja negra" para realizar la tarea deseada. Esto ahorra tiempo y reduce la posibilidad de errores.

### 5.1. Composición y estructura

La estructura exacta de una librería puede variar dependiendo del lenguaje de programación y el sistema operativo. Sin embargo, en términos generales, una librería se compone de una serie de módulos o componentes que realizan tareas específicas. Cada módulo puede contener una o más funciones, clases, o variables que pueden ser utilizadas por otros programas.

Las librerías pueden ser tan simples como una colección de funciones relacionadas, o tan complejas como un marco de trabajo completo con su propia arquitectura y API (interfaz de programación de aplicaciones).

Los detalles de cómo se utilizan las librerías en un lenguaje de programación específico suelen estar cubiertos en la documentación oficial del lenguaje o en libros de texto sobre ese lenguaje. Por ejemplo, "The C Programming Language" (Kernighan y Ritchie, 1988) cubre el uso de librerías en C, y "Java: The Complete Reference" (Schildt, 2018) cubre las librerías en Java.

### 5.2. Características

- **Reusabilidad**: Las librerías están diseñadas para ser reutilizadas en múltiples aplicaciones. Esto puede ahorrar mucho tiempo y esfuerzo a los desarrolladores, ya que no tienen que escribir y probar el mismo código una y otra vez. 
- **Modularidad**: Las librerías suelen estar organizadas de manera modular, lo que significa que se dividen en piezas que realizan tareas específicas. Esto hace que sean más fáciles de entender y usar.
- **Independencia de la plataforma**: Algunas librerías están diseñadas para ser independientes de la plataforma, lo que significa que se pueden usar en diferentes sistemas operativos o entornos de hardware.
- **Eficiencia**: Las librerías a menudo contienen código que ha sido optimizado para realizar tareas específicas de manera eficiente.

### 5.3. Tipos

**Librerías estáticas**: Son archivos que se vinculan a un programa durante el proceso de compilación. Los archivos binarios de la librería se incluyen directamente en el ejecutable final del programa.

**Librerías dinámicas**: Son archivos que se vinculan a un programa en tiempo de ejecución. Esto significa que los binarios de la librería no están incluidos en el ejecutable final, sino que se cargan desde la librería mientras el programa se está ejecutando.

## 6. Diseño de funciones y procedimientos
 ## 6.1. Diseño estructurado
 ## 6.2. Atributos de la calidad de un diseño


## 7. Conclusión

La programación modular, el diseño de funciones, la recursividad y el uso de librerías son elementos fundamentales en la formación de cualquier estudiante de informática. No solo proporcionan las herramientas necesarias para abordar problemas complejos y desarrollar soluciones eficientes, sino que también fomentan una mentalidad de pensamiento lógico y estructurado que es invaluable en la industria de la tecnología.

Las ventajas de la programación modular son innumerables, incluyendo la mejora de la legibilidad, la reusabilidad y la eficiencia en el código. Las funciones y los procedimientos permiten un código más ordenado y una mejor distribución de las tareas. La recursividad, aunque puede ser un concepto desafiante para los principiantes, es fundamental para resolver ciertos tipos de problemas de manera eficiente. Las librerías, por otro lado, permiten aprovechar el trabajo de otros programadores para evitar "reinventar la rueda".

## 7.1. Relación del tema con la enseñanza en FP

En la Formación Profesional (FP), los conceptos de programación modular, diseño de funciones, recursividad y librerías son esenciales. Los estudiantes de FP en el área de informática necesitan entender estos conceptos para poder desarrollar soluciones eficientes a problemas reales.

En el aula, estos conceptos se pueden enseñar de manera teórica, pero también deben ser reforzados con ejemplos prácticos y ejercicios. Los estudiantes deben tener la oportunidad de experimentar con la creación de módulos y funciones, el uso de la recursividad y la implementación de librerías. 

Además, estos conceptos no solo son relevantes para la programación. La idea de dividir un problema complejo en partes más pequeñas y manejables es una habilidad valiosa en muchas áreas de la vida. Asimismo, el uso eficiente de los recursos disponibles (en este caso, las librerías) es una lección importante para cualquier profesional.

Espero que esta conclusión y relación con la enseñanza en FP sea de utilidad. Por favor, si necesitas que desarrolle más apartados del tema, estaré encantado de ayudarte.

## 8 Bibliografía

"Structured Programming" (Dahl, Dijkstra y Hoare, 1972). Este libro fue uno de los primeros en proponer la idea de dividir los programas en módulos o funciones independientes.

"The Art of Computer Programming" (Donald Knuth, 1968-). Aunque este libro no se centra específicamente en la programación modular, proporciona muchos de los fundamentos de diseño y organización de programas que la hacen posible.

"The Pragmatic Programmer: Your Journey to Mastery" (Hunt y Thomas, 1999). Este libro incluye una discusión sobre la importancia de la programación modular y ofrece consejos sobre cómo implementarla en la práctica.

"Clean Code: A Handbook of Agile Software Craftsmanship" (Robert C. Martin, 2008). Este libro ofrece consejos sobre cómo escribir código que sea fácil de leer y mantener, incluyendo el uso de la programación modular.

"Code Complete: A Practical Handbook of Software Construction" (Steve McConnell, 2004). Este libro ofrece una cobertura detallada de muchos aspectos de la programación, incluyendo la programación modular.
