# TEMA 24: Lenguajes de programación. Tipos. Características
> #### Bloque 3

- [TEMA 24: Lenguajes de programación. Tipos. Características](#tema-24-lenguajes-de-programación-tipos-características)
  - [1.1. Definición](#11-definición)
  - [1.2. Historia de los lenguajes de programación](#12-historia-de-los-lenguajes-de-programación)
  - [2. Lenguajes de programación](#2-lenguajes-de-programación)
  - [3. Tipos de lenguajes de programación](#3-tipos-de-lenguajes-de-programación)
    - [3.1. Clasificación por paradigmas](#31-clasificación-por-paradigmas)
    - [3.2. Clasificación por dominio de aplicación](#32-clasificación-por-dominio-de-aplicación)
  - [4. Características de los lenguajes de programación](#4-características-de-los-lenguajes-de-programación)
    - [4.1. Características en el diseño de lenguajes de programación](#41-características-en-el-diseño-de-lenguajes-de-programación)
    - [4.2. Aspectos de la implementación](#42-aspectos-de-la-implementación)
  - [5. Lenguajes de programación actuales y tendencias](#5-lenguajes-de-programación-actuales-y-tendencias)
  - [6. Conclusiones](#6-conclusiones)
  - [7. Bibliografía](#7-bibliografía)
  - [Clasificación en función de los paradigmas de programación](#clasificación-en-función-de-los-paradigmas-de-programación)


## 1.1. Definición
Un lenguaje de programación puede definirse como un conjunto estructurado y formalizado de símbolos, reglas y convenciones que permiten a los desarrolladores expresar algoritmos e instrucciones de manera comprensible para las computadoras, facilitando la comunicación entre el ser humano y las máquinas (Aho, Lam, Sethi, & Ullman, 2006; Sebesta, 2016; Mitchell, 2003).

"Un lenguaje de programación es un sistema notacional para describir computaciones en una forma legible para el ser humano y que sea procesable por una máquina. Los lenguajes de programación son utilizados para facilitar la comunicación acerca de la tarea de organizar y manipular información y para expresar algoritmos de forma precisa" (Sebesta, R.W. Concepts of Programming Languages. 11th ed., Pearson, 2016).  

## 1.2. Historia de los lenguajes de programación

Las generaciones de lenguajes de programación se refieren a la evolución de estos lenguajes a lo largo del tiempo, clasificándose generalmente en cinco categorías principales. Cada generación presenta características distintivas y avances en comparación con las generaciones anteriores.

**Primera generación: Lenguajes de máquina**
Los lenguajes de primera generación son lenguajes de bajo nivel y corresponden al código máquina. Estos lenguajes utilizan instrucciones binarias (0 y 1) para comunicarse directamente con el hardware del computador. El código máquina es difícil de leer y escribir para los humanos, ya que requiere conocimientos detallados del hardware específico de la computadora.

**Segunda generación: Lenguajes ensambladores**
Los lenguajes de segunda generación, también conocidos como lenguajes ensambladores, representan un avance con respecto al código máquina. En lugar de utilizar códigos binarios, los lenguajes ensambladores emplean mnemónicos (abreviaturas de palabras) para representar instrucciones y registros. Los programas escritos en lenguaje ensamblador son más fáciles de leer y escribir que el código máquina, pero aún requieren un conocimiento profundo del hardware subyacente. Los ensambladores son utilizados para convertir el código fuente en lenguaje ensamblador a código máquina.

**Tercera generación: Lenguajes de alto nivel**
Los lenguajes de tercera generación son lenguajes de alto nivel que permiten a los programadores escribir código utilizando una sintaxis más cercana al lenguaje natural humano. Estos lenguajes son más fáciles de aprender y usar, y ofrecen una mayor abstracción del hardware subyacente. Algunos ejemplos de lenguajes de programación de tercera generación incluyen FORTRAN, COBOL, Pascal, C, C++, Java y Python. Los compiladores e intérpretes se utilizan para convertir el código fuente en lenguaje de alto nivel a código máquina.

**Cuarta generación: Lenguajes de consulta y manipulación de datos**
Los lenguajes de cuarta generación (4GL) se centran en la manipulación de datos y la realización de tareas específicas, como la generación de informes y la creación de formularios. Estos lenguajes ofrecen un mayor nivel de abstracción y son más fáciles de usar que los lenguajes de tercera generación. Algunos ejemplos de lenguajes de cuarta generación incluyen SQL (Structured Query Language), Prolog y MATLAB.

**Quinta generación: Lenguajes de programación basados en inteligencia artificial**
Los lenguajes de quinta generación (5GL) son lenguajes de programación orientados a la inteligencia artificial, la resolución de problemas y la manipulación de símbolos. Estos lenguajes utilizan técnicas de programación basadas en la lógica y el razonamiento para expresar problemas y soluciones. Algunos ejemplos de lenguajes de quinta generación incluyen Lisp, Prolog y Mercury.

## 2. Lenguajes de programación

## 3. Tipos de lenguajes de programación

Los lenguajes de programación pueden ser clasificados como **compilados** o **interpretados**. Esta clasificación se basa en cómo se ejecuta el código escrito en estos lenguajes.

- **Lenguajes Compilados:**

Los lenguajes compilados son aquellos en los que el código fuente es traducido directamente en código máquina por un compilador antes de que sea ejecutado. Este código máquina es específico para la arquitectura del sistema y no puede ser ejecutado en diferentes tipos de sistemas sin ser recompilado.

*Características:*

1. Son generalmente más rápidos en la ejecución porque el código ya ha sido traducido a código máquina antes de la ejecución.
2. Una vez compilado, el código no necesita del compilador para ser ejecutado.
3. El código compilado es específico para la arquitectura del sistema.

*Ejemplos:* C, C++, Swift, Go, Rust.

- **Lenguajes Interpretados:**

Los lenguajes interpretados son aquellos en los que el código fuente es leído y ejecutado línea por línea por un intérprete en tiempo de ejecución. Esto significa que el código no se traduce a código máquina antes de su ejecución.

*Características:*

1. Son generalmente más lentos que los lenguajes compilados porque el intérprete tiene que traducir el código a código máquina en tiempo real.
2. El código puede ser ejecutado en cualquier sistema que tenga un intérprete para ese lenguaje, lo que los hace más portables.
3. El código necesita del intérprete para ser ejecutado.

*Ejemplos:* Python, Ruby, JavaScript, PHP, Perl.

**Similitudes y Diferencias:**

Tanto los lenguajes compilados como los interpretados son utilizados para escribir software y ambos pueden ser usados para crear programas complejos. La principal diferencia entre ellos es cómo y cuándo se traduce el código a código máquina.

- **Otros tipos de lenguajes:**

Además de los lenguajes compilados e interpretados, existe otro tipo de lenguaje conocido como lenguaje de programación de nivel intermedio o lenguajes de bytecode.

Estos lenguajes son una especie de híbrido entre los dos anteriores. El código fuente se compila a un código de bytes (bytecode), que es una versión intermedia del código que no es específica de la máquina. Este bytecode luego se interpreta o se compila en tiempo de ejecución (Just-In-Time compilation, JIT) para ser ejecutado.

El beneficio de este enfoque es que permite una portabilidad similar a la de los lenguajes interpretados, pero con un rendimiento que puede acercarse al de los lenguajes compilados.

*Ejemplos:* Java, C#, Kotlin.

### 3.1. Clasificación por paradigmas

Los lenguajes de programación se pueden clasificar en función de los paradigmas de programación que siguen. Un paradigma de programación es un enfoque o estilo particular para resolver problemas y diseñar soluciones utilizando un lenguaje de programación. A continuación se presentan algunos de los paradigmas de programación más relevantes y los lenguajes de programación asociados, basados en bibliografías destacadas:

- **Paradigma imperativo/procedural**
El paradigma imperativo se basa en la ejecución secuencial de instrucciones y en la manipulación del estado del programa mediante variables y estructuras de control (como bucles y condicionales). Los lenguajes procedurales son un subconjunto de los lenguajes imperativos que se centran en la organización del código en procedimientos o funciones.

*Lenguajes representativos*: C, Pascal, FORTRAN 

- **Paradigma orientado a objetos**
El paradigma orientado a objetos se centra en la organización del código en objetos, que son instancias de clases que encapsulan datos y comportamientos. Este enfoque promueve la reutilización de código, la modularidad y el encapsulamiento.

*Lenguajes representativos:* Java, C++, C#, Python, Ruby

- **Paradigma funcional**
El paradigma funcional trata la computación como una secuencia de funciones matemáticas y evita el cambio de estado y los datos mutables. Este enfoque promueve la programación sin efectos secundarios y puede facilitar el razonamiento sobre el código y la concurrencia.

*Lenguajes representativos:* Haskell, Lisp, Erlang, ML, Scala

- **Paradigma lógico**
El paradigma lógico se basa en la programación declarativa, donde los programas consisten en declaraciones de hechos y reglas lógicas. El sistema de programación se encarga de deducir nuevas conclusiones y encontrar soluciones a los problemas.

*Lenguajes representativos:*  Prolog, Mercury

- **Paradigma de script**
El paradigma de script se refiere a lenguajes de programación que se utilizan para la automatización de tareas, la manipulación de archivos y la interacción entre programas. Los lenguajes de script son a menudo interpretados en lugar de compilados y pueden ser utilizados para el desarrollo rápido de aplicaciones.

*Lenguajes representativos:* JavaScript, Python, Perl, Ruby, Lua

Cabe destacar que algunos lenguajes de programación admiten múltiples paradigmas, lo que permite a los programadores utilizar diferentes enfoques según las necesidades del proyecto. Por ejemplo, Python y Scala admiten tanto la programación orientada a objetos como la programación funcional.

### 3.2. Clasificación por dominio de aplicación

Los lenguajes de programación también pueden clasificarse según el dominio de aplicación para el que se diseñaron o en el que son especialmente adecuados. A continuación, se enumeran algunos lenguajes de programación y sus dominios de aplicación típicos, basados en bibliografías relevantes:

**Desarrollo web**
Frontend: JavaScript, TypeScript, HTML, CSS
Backend: PHP, Ruby (Ruby on Rails), Python (Django, Flask), JavaScript (Node.js), Java (Spring), C# (ASP.NET)

**Desarrollo de aplicaciones móviles**
iOS: Swift, Objective-C
Android: Java, Kotlin
Multiplataforma: Flutter (Dart), React Native (JavaScript), Xamarin (C#)

**Desarrollo de videojuegos**
C++, C#, Lua (en combinación con motores de juego como Unity, Unreal Engine, Godot, etc.)

**Inteligencia artificial y aprendizaje automático**
Python (bibliotecas como TensorFlow, PyTorch, scikit-learn), R, Julia  

**Análisis de datos y visualización**
R, Python (bibliotecas como Pandas, NumPy, Matplotlib, Seaborn), MATLAB

**Computación científica y de alto rendimiento**
FORTRAN, C, C++, Python (bibliotecas como NumPy, SciPy), Julia

**Sistemas embebidos y desarrollo de hardware**
C, C++, Rust, Ada, Assembly

Es importante tener en cuenta que estos dominios de aplicación no son mutuamente excluyentes, y algunos lenguajes de programación pueden ser aplicables a varios dominios. Además, la elección del lenguaje de programación para un proyecto específico puede depender de otros factores, como la experiencia del equipo de desarrollo, las restricciones de rendimiento y las preferencias personales.

## 4. Características de los lenguajes de programación

### 4.1. Características en el diseño de lenguajes de programación

Cuando se diseña un lenguaje de programación, hay varias características clave a considerar según la bibliografía relevante. Estas características pueden afectar tanto la facilidad de uso como la eficiencia del lenguaje en cuestión. Algunas de las principales características a abordar incluyen:

**Legibilidad y facilidad de escritura:** Un buen lenguaje de programación debe ser fácil de leer y escribir para los desarrolladores. La legibilidad permite a los programadores entender rápidamente el código escrito por otros, mientras que la facilidad de escritura facilita la implementación de soluciones de manera eficiente (Sebesta, 2016).
**
Abstracción:** La abstracción es la capacidad de simplificar problemas complejos y representarlos de manera más manejable. Un lenguaje de programación debe proporcionar mecanismos de abstracción para permitir a los programadores expresar soluciones sin tener que lidiar con detalles innecesarios (Aho et al., 2006).

**Expresividad:** La expresividad se refiere a la capacidad de un lenguaje para representar ideas y algoritmos de manera concisa y clara. Un lenguaje expresivo permite a los programadores escribir código que refleje de manera efectiva sus intenciones y pensamientos (Mitchell, 2003).

**Eficiencia:** Un lenguaje de programación debe permitir la generación de código eficiente en términos de tiempo de ejecución y uso de recursos. Esto es particularmente importante en aplicaciones donde el rendimiento es crítico, como en la computación de alto rendimiento o en sistemas embebidos (Patterson & Hennessy, 2013).

**Portabilidad:** La portabilidad es la capacidad de un lenguaje de programación para funcionar en diferentes plataformas y sistemas operativos sin modificaciones significativas. Un lenguaje portable permite a los desarrolladores escribir una vez y ejecutar en múltiples entornos (Sebesta, 2016).

**Capacidad de depuración y mantenimiento:** Un buen lenguaje de programación debe facilitar la depuración y el mantenimiento del código a lo largo del tiempo. Esto incluye la capacidad de identificar y corregir errores, así como de realizar modificaciones y mejoras en el código existente (McConnell, 2004).

**Integración con otras tecnologías y herramientas:** Un lenguaje de programación debe ser compatible con otras tecnologías y herramientas para permitir a los desarrolladores aprovechar bibliotecas existentes, frameworks y sistemas de desarrollo (Gamma et al., 1994).


### 4.2. Aspectos de la implementación

Los lenguajes de programación son herramientas que permiten a los desarrolladores crear software. Para ser efectivos, estos lenguajes deben poseer ciertas características o cualidades. Aquí te menciono algunas de las más importantes:

1. **Legibilidad y Claridad:** Un buen lenguaje de programación debe ser fácil de leer y entender. Esto no solo facilita el aprendizaje del lenguaje, sino que también hace más sencillo el mantenimiento y la revisión del código en el futuro.

2. **Eficiencia:** Los lenguajes de programación deben permitir la creación de software que se ejecute de manera eficiente. Esto implica tanto la velocidad de ejecución como el uso eficiente de los recursos del sistema, como la memoria y el procesador.

3. **Portabilidad:** La portabilidad se refiere a la capacidad de un programa para ser ejecutado en diferentes plataformas sin necesidad de cambios significativos. Un lenguaje de programación con alta portabilidad permitirá que el código escrito en él se ejecute en una variedad de sistemas operativos y arquitecturas de hardware.

4. **Expresividad:** Un lenguaje de programación debe ser expresivo, es decir, debe permitir a los programadores expresar sus ideas de manera clara y concisa. Un lenguaje de programación expresivo puede hacer que el código sea más legible y fácil de mantener.

5. **Uniformidad y Consistencia:** Los buenos lenguajes de programación suelen tener reglas y estructuras consistentes, lo que facilita su aprendizaje y uso. Además, esto puede reducir la probabilidad de errores.

6. **Robustez y Seguridad:** Un lenguaje de programación debe ser robusto y proporcionar mecanismos para manejar errores y excepciones. Además, debe proporcionar características que ayuden a prevenir problemas de seguridad, como el desbordamiento de búfer o la inyección de código.

7. **Soporte y Comunidad:** Un buen lenguaje de programación a menudo tiene un fuerte soporte y una comunidad activa. Esto puede incluir documentación extensa, una gran cantidad de bibliotecas y marcos de trabajo, y una comunidad de desarrolladores que pueden proporcionar asistencia y soporte.

Cabe destacar que no todos los lenguajes de programación necesitan todas estas características en la misma medida. Dependiendo de la aplicación específica, algunas características pueden ser más importantes que otras. Por ejemplo, para el desarrollo de sistemas embebidos, la eficiencia y el control a bajo nivel pueden ser más importantes que la facilidad de uso o la legibilidad.
## 5. Lenguajes de programación actuales y tendencias

Para desarrollar este punto, es importante destacar que el mundo de la programación es dinámico y en constante evolución. Los lenguajes de programación surgen, cambian y caen en desuso conforme evolucionan las necesidades de la industria y la tecnología. Aquí se presentarán algunos de los lenguajes de programación más utilizados actualmente y las tendencias actuales en este campo.

**Lenguajes de Programación Actuales**

1. **Python:** Este lenguaje de programación de alto nivel se ha vuelto muy popular por su sintaxis clara y legible. Python es ampliamente utilizado en ciencia de datos, aprendizaje automático, desarrollo web, automatización y muchas otras áreas (Pierce, B.C., Types and Programming Languages, MIT Press, 2002).

2. **JavaScript:** Originalmente desarrollado para la programación del lado del cliente en la web, JavaScript ha evolucionado y ahora también se utiliza para el desarrollo del lado del servidor (Node.js), así como para aplicaciones móviles y de escritorio. Su popularidad sigue siendo alta debido a su papel central en la web moderna (Flanagan, D., JavaScript: The Definitive Guide, O'Reilly Media, 2020).

3. **Java:** Java ha sido un pilar en el mundo de la programación desde su introducción en la década de 1990. Aunque ha habido fluctuaciones en su popularidad, Java sigue siendo ampliamente utilizado en empresas para el desarrollo de aplicaciones de back-end y de Android (Arnold, K., Gosling, J., The Java Programming Language, Addison-Wesley Professional, 2005).

4. **C# y .NET:** C# es un lenguaje desarrollado por Microsoft y es ampliamente utilizado en el desarrollo de aplicaciones de Windows y juegos (a través de Unity). El entorno .NET de Microsoft proporciona un marco robusto para el desarrollo con C# (Albahari, J., Albahari, B., C# 7.0 in a Nutshell, O'Reilly Media, 2017).

**Tendencias en Lenguajes de Programación**

1. **Rust:** Rust es un lenguaje de programación de sistemas que se centra en la seguridad, especialmente en lo que respecta a la concurrencia y la memoria segura. Rust ha estado ganando popularidad recientemente debido a su rendimiento y seguridad (Klabnik, S., Nichols, C., The Rust Programming Language, No Starch Press, 2018).

2. **Kotlin:** Kotlin es un lenguaje de programación moderno que se ejecuta en la Máquina Virtual de Java (JVM). Kotlin ha sido adoptado por Google como lenguaje preferido para el desarrollo de Android, lo que ha impulsado su popularidad (Jemerov, D., Isakova, S., Kotlin in Action, Manning Publications, 2017).

3. **Go:** Desarrollado por Google, Go (o Golang) es un lenguaje de programación que se centra en la simplicidad y la eficiencia. Es especialmente adecuado para aplicaciones de red y de sistemas distribuidos (Donovan, A.A., Kernighan, B.W., The Go Programming Language, Addison-Wesley Professional, 2015).

4. **Swift:** Swift es el lenguaje de programación desarrollado por Apple para reemplazar Objective-C para el iOS y macOS. Swift ofrece una sintaxis más limpia y segura, y está ganando popularidad entre los desarrolladores de Apple (Hudson, P., Pro Swift, Hacking with Swift, 2016).

**Tendencias Generales en Programación**

1. **Programación Funcional:** Aunque la programación funcional no es nueva, ha estado ganando más atención recientemente. Los lenguajes como Scala y Haskell son puramente funcionales, mientras que otros lenguajes, como JavaScript y Python, están incorporando más características funcionales.

2. **Desarrollo Web Full Stack con JavaScript:** Con la introducción de Node.js, los desarrolladores pueden usar JavaScript tanto en el front-end como en el back-end. Esta tendencia hacia el desarrollo web full stack con JavaScript está creciendo.

3. **Lenguajes Específicos de Dominio (DSL):** Los DSL son lenguajes de programación especializados en un dominio específico. Estos lenguajes permiten resolver problemas o tareas específicas de manera más eficiente que con un lenguaje de programación general. Ejemplos de DSL incluyen SQL para consultas de bases de datos y HTML para la creación de páginas web.

4. **Aprendizaje Automático y Ciencia de Datos:** Con el auge del Big Data, la ciencia de datos y el aprendizaje automático se han vuelto cada vez más importantes. Los lenguajes de programación como Python y R son particularmente populares en este campo debido a sus robustas bibliotecas y herramientas.

5. **Lenguajes de Programación Seguros:** Con la creciente importancia de la seguridad en la informática, los lenguajes de programación que enfatizan la seguridad, como Rust, están ganando popularidad. Estos lenguajes intentan prevenir errores comunes que pueden llevar a vulnerabilidades de seguridad.

## 6. Conclusiones
## 7. Bibliografía

> Aho, A. V., Lam, M. S., Sethi, R., & Ullman, J. D. (2006). Compilers: Principles, Techniques, and Tools (2nd ed.). Pearson/Addison Wesley.  

> Patterson, D. A., & Hennessy, J. L. (2013). Computer Organization and Design: The Hardware/Software Interface (5th ed.). Morgan Kaufmann.

> McConnell, S. (2004). Code Complete: A Practical Handbook of Software Construction (2nd ed.). Microsoft Press.
Gamma, E., Helm, R., Johnson, R., & V

> Sebesta, R. W. (2016). Concepts of Programming Languages (11th ed.). Pearson.

> Mitchell, J. C. (2003). Concepts in Programming Languages. Cambridge University Press.



---
## Clasificación en función de los paradigmas de programación

Los lenguajes de programación también pueden ser clasificados según el paradigma de programación que utilizan. Los paradigmas de programación son formas de clasificar los lenguajes de programación según sus características. Los cuatro paradigmas más comunes son: imperativo, declarativo, orientado a objetos y funcional.

**Lenguajes de Programación Imperativos:**

Los lenguajes imperativos son aquellos en los que los programas son una serie de comandos para la computadora. Estos comandos cambian el estado de la computadora de una forma que se puede seguir paso a paso.

*Características:*

1. Los programas están formados por una secuencia de comandos o instrucciones.
2. Los programas cambian el estado de la computadora a medida que se ejecutan las instrucciones.
3. Son excelentes para tareas que requieren un control detallado del hardware de la computadora.

*Ejemplos:* C, Pascal, Fortran.

**Lenguajes de Programación Declarativos:**

Los lenguajes declarativos son aquellos en los que los programas describen el resultado deseado, pero no necesariamente cómo lograrlo. Estos lenguajes son buenos para resolver problemas complejos que requieren una gran cantidad de datos.

*Características:*

1. Los programas describen el resultado deseado, no cómo alcanzarlo.
2. Son útiles para tareas de procesamiento de datos y problemas que requieren un alto nivel de abstracción.
3. Los programas no cambian el estado de la computadora.

*Ejemplos:* SQL, Prolog, HTML.

**Lenguajes de Programación Orientados a Objetos:**

Los lenguajes orientados a objetos son aquellos en los que los programas están formados por objetos, que son instancias de clases, que encapsulan datos y métodos.

*Características:*

1. Los programas están formados por objetos.
2. Los objetos son instancias de clases que encapsulan datos y métodos.
3. Promueven la reutilización de código a través de la herencia y la composición.

*Ejemplos:* Java, C++, Python, Ruby.

**Lenguajes de Programación Funcionales:**

Los lenguajes funcionales son aquellos en los que los programas se componen de funciones. Estos lenguajes evitan cambiar el estado y los datos mutables.

*Características:*

1. Los programas están formados por funciones.
2. Evitan cambiar el estado y los datos mutables.
3. Son excelentes para tareas que requieren un alto grado de abstracción y para problemas que pueden ser resueltos con una serie de transformaciones de datos.

*Ejemplos:* Lisp, Haskell, Erlang, Scala.

**Similitudes y Diferencias:**

Todos los lenguajes de programación se utilizan para escribir software y pueden ser usados para crear programas complejos. Sin embargo, los diferentes paradigmas de programación enfatizan diferentes formas de pensar sobre los problemas y de organizar y estructurar el código para resolverlos.

Además de estos cuatro, existen otros paradigmas de programación como la programación lógica (Prolog), programación concurrente (Erlang), programación orientada a aspectos (AspectJ), entre otros.
