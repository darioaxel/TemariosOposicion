# TEMA 11: Organización lógica de los datos. Estructuras estáticas.

# Introducción

En la era actual de la información, el manejo eficiente de los datos es un aspecto fundamental para el buen funcionamiento de cualquier sistema informático. Las estructuras de datos, tanto estáticas como dinámicas, desempeñan un papel crucial en la organización y manipulación de la información, lo que permite a los profesionales de la informática desarrollar soluciones eficientes y efectivas para una amplia gama de problemas. 

Una estructura de datos es una forma especializada de organizar y almacenar información que permite acceder y modificarla de manera eficiente. Las estructuras de datos estáticas, como los arrays y las estructuras de registros, son aquellas cuyo tamaño y organización se mantienen constantes a lo largo de la ejecución del programa. Estas estructuras son fundamentales para el diseño y análisis de algoritmos, ya que proporcionan una base sólida para el desarrollo de soluciones informáticas.

Según Cormen et al. (2009), ***"la elección adecuada de las estructuras de datos es crucial para el desempeño de un algoritmo, ya que esta elección afecta directamente la eficiencia en tiempo y espacio de la solución propuesta"***. Esta afirmación resalta la importancia de enseñar y dominar las estructuras de datos estáticas en la formación de futuros profesionales de la informática, ya que su comprensión y aplicación adecuada son esenciales para el éxito en la resolución de problemas y el desarrollo de sistemas informáticos eficientes.

En el tema "Organización lógica de los datos: Estructuras estáticas" de la oposición de profesor de informática, se abordará la importancia de comprender y aplicar correctamente las estructuras de datos estáticas en la resolución de problemas y en la enseñanza de esta materia.

# Organización lógica de los datos
## Descripción de datos

Un dato en un sistema informático se define como una representación simbólica de un valor o una entidad que puede ser procesada, almacenada y transmitida por una computadora. En otras palabras, un dato es una pieza de información codificada de manera que pueda ser comprendida e interpretada por un sistema informático para realizar diversas operaciones y cálculos.

Stallings (2016) define un dato como ***"un conjunto de valores cuantitativos o cualitativos que representan hechos, conceptos o instrucciones en un formato adecuado para la comunicación, interpretación o procesamiento por humanos o por máquinas automáticas".***

En un sistema informático, un dato se identifica mediante su dirección de memoria y su tipo de dato. La dirección de memoria es la ubicación específica en la memoria del sistema donde se almacena el dato, mientras que el tipo de dato define la naturaleza y las características del dato almacenado en esa dirección.

## Tipos de datos

Los tipos de datos en un sistema informático se pueden clasificar en dos categorías principales: simples y compuestos. Los tipos de datos simples, también conocidos como tipos de datos primitivos, son aquellos que representan un único valor o entidad y forman la base para la construcción de estructuras de datos más complejas. Por otro lado, los tipos de datos compuestos, también llamados estructuras de datos, son aquellos que agrupan varios elementos de datos simples o compuestos en una única entidad, permitiendo representar y manipular información de manera más organizada y estructurada.

Los tipos de datos simples incluyen:

**Enteros**: Representan números enteros, tanto positivos como negativos, sin parte decimal.  
**Números de coma flotante**: Representan números reales con parte decimal, permitiendo representar valores con mayor precisión.  
**Caracteres**: Representan letras, números, símbolos y otros caracteres utilizando un código específico, como ASCII o Unicode.  
**Booleanos**: Representan valores de verdad, es decir, verdadero (true) o falso (false).  

Las estructuras de datos se pueden clasificar según su forma de almacenamiento en dos categorías principales: estructuras de datos lineales y estructuras de datos no lineales.

**Estructuras de datos lineales**: Son aquellas en las que los elementos se almacenan de manera secuencial y se organizan en una estructura de una sola dimensión. En estas estructuras, cada elemento tiene a lo sumo un predecesor y un sucesor, excepto los elementos ubicados en los extremos. Algunas de las estructuras de datos lineales más comunes son:

- ***Arrays***: Colecciones de elementos del mismo tipo de dato, almacenados de forma secuencial en la memoria y accesibles mediante un índice.
- ***Listas enlazadas***: Colecciones de elementos en las que cada elemento contiene una referencia al siguiente elemento de la lista.
- ***Pilas (Stacks)***: Estructuras en las que los elementos se organizan siguiendo el principio de "último en entrar, primero en salir" (LIFO, por sus siglas en inglés).
- ***Colas (Queues)***: Estructuras en las que los elementos se organizan siguiendo el principio de "primero en entrar, primero en salir" (FIFO, por sus siglas en inglés).

**Estructuras de datos no lineales**: Son aquellas en las que los elementos se almacenan de manera jerárquica, formando estructuras de múltiples dimensiones. En estas estructuras, cada elemento puede tener múltiples predecesores y sucesores. Algunas de las estructuras de datos no lineales más comunes son:

- ***Árboles***: Estructuras jerárquicas en las que los elementos se organizan en nodos conectados por aristas, siguiendo una relación de parentesco. Ejemplos de árboles incluyen árboles binarios, árboles AVL y árboles B.
- ***Grafos***: Estructuras en las que los elementos se representan como nodos y las relaciones entre ellos como aristas. Los grafos pueden ser dirigidos (las aristas tienen dirección) o no dirigidos (las aristas no tienen dirección). Ejemplos de grafos incluyen grafos de adyacencia y grafos ponderados.


Por otro lado, cuando se hace referencia a cómo se gestionan su tamaño y su organización en la memoria durante la ejecución del programa, las estructuras de datos se pueden dividir en **dinámicas** y **estáticas**. La principal diferencia entre ambas radica en la flexibilidad y adaptabilidad de la estructura en función de las necesidades del programa.

***Estructuras de datos estáticas***: Son aquellas cuyo tamaño y organización se mantienen constantes a lo largo de la ejecución del programa. Una vez creadas, no se pueden redimensionar ni modificar su estructura interna. Esto implica que la cantidad de memoria asignada a estas estructuras se determina en tiempo de compilación. Las estructuras de datos estáticas pueden ser más rápidas y menos propensas a errores, pero también menos flexibles y menos eficientes en cuanto al uso de la memoria en ciertos casos. Ejemplos de estructuras de datos estáticas son los arrays y las estructuras de registros.

***Estructuras de datos dinámicas***: Son aquellas cuyo tamaño y organización pueden cambiar durante la ejecución del programa. La cantidad de memoria asignada a estas estructuras puede variar en tiempo de ejecución, lo que permite adaptar la estructura a las necesidades específicas del programa en cada momento. Las estructuras de datos dinámicas suelen ser más flexibles y eficientes en cuanto al uso de la memoria, pero también pueden ser más complejas de manejar y estar más expuestas a errores, como fugas de memoria o desbordamientos de memoria. Ejemplos de estructuras de datos dinámicas son las listas enlazadas, los árboles y los grafos.

# Estructuras de datos estáticas
## Arrays
Los arrays (arreglos) son generalmente considerados estructuras de datos estáticas en muchos lenguajes de programación, ya que su tamaño se define en tiempo de compilación y no puede cambiar en tiempo de ejecución. Sin embargo, es importante mencionar que algunos lenguajes de programación ofrecen arrays dinámicos, que pueden cambiar de tamaño durante la ejecución del programa.

Un array es una estructura de datos que almacena una colección de elementos del mismo tipo en una ubicación contigua de memoria. Los elementos del array son accesibles mediante índices enteros que indican la posición de cada elemento dentro del array. El tamaño de un array se define en tiempo de compilación y no puede cambiar en tiempo de ejecución.

### Estructura:

Un array en C++ tiene una estructura secuencial y contigua en memoria, donde cada elemento se encuentra inmediatamente después del elemento anterior. Los elementos del array son del mismo tipo, lo que garantiza que todos tengan el mismo tamaño. Por ejemplo, un array de enteros en C++ se define de la siguiente manera:

```cpp
Copy code
int numeros[5]; // Array de 5 enteros
```

### Almacenamiento en memoria:

Los arrays en C++ se almacenan en memoria de forma contigua y secuencial, lo que facilita el acceso a los elementos a través de sus índices y optimiza el rendimiento en términos de localidad de referencia. El primer elemento del array se almacena en la dirección base, y los elementos siguientes se almacenan en direcciones consecutivas, según el tamaño del tipo de dato del array.

### Operaciones básicas:

Acceso a elementos: Leer o escribir valores en posiciones específicas del array utilizando índices enteros. En C++, se utilizan corchetes para acceder a los elementos del array:
```cpp
numeros[0] = 42; // Asigna el valor 42 al primer elemento del array
int valor = numeros[0]; // Lee el primer elemento del array
```
Recorrido: Iterar a través de los elementos del array, normalmente utilizando bucles for o for-each. Por ejemplo:
```cpp
for (int i = 0; i < 5; i++) {
  cout << numeros[i] << endl; // Imprime cada elemento del array
}
```
Inicialización: Asignar valores iniciales a los elementos del array durante su declaración:
```cpp
int numeros[5] = {1, 2, 3, 4, 5}; // Inicializa el array con los valores especificados
```
Copia de arrays: Copiar elementos de un array a otro requiere un bucle para recorrer los elementos y asignarlos uno por uno. C++ no permite asignar directamente un array a otro ni copiarlo mediante el operador de asignación =.
```cpp
int original[5] = {1, 2, 3, 4, 5};
int copia[5];

for (int i = 0; i < 5; i++) {
  copia[i] = original[i]; // Copia los elementos del array original al array copia
}
```
## Matrices
Las matrices son estructuras de datos bidimensionales que almacenan elementos en una disposición tabular, consistente en filas y columnas. Cada elemento de una matriz se identifica mediante dos índices: el primero indica la posición de la fila y el segundo indica la posición de la columna. Las matrices pueden considerarse como una extensión de los arrays, donde los elementos se organizan en más de una dimensión.

### Estructura en memoria:

En la memoria, las matrices se almacenan de dos formas principales: por filas (orden de filas) o por columnas (orden de columnas). En el orden de filas, los elementos de una misma fila se almacenan de manera contigua, mientras que en el orden de columnas, los elementos de una misma columna se almacenan de manera contigua. El orden de almacenamiento utilizado depende del lenguaje de programación o del diseño específico del sistema informático.

### Tipos de matrices según su tamaño:

Matriz rectangular: Es una matriz que tiene un número constante de filas y de columnas. Todos los elementos en la matriz se almacenan en una estructura tabular regular. Ejemplo: una matriz de 3x4 tiene 3 filas y 4 columnas.

Matriz cuadrada: Es un caso especial de matriz rectangular en la que el número de filas es igual al número de columnas. Ejemplo: una matriz de 3x3 tiene 3 filas y 3 columnas.

Matriz irregular o matriz enjambre (jagged array): Es una matriz cuyas filas tienen un número variable de columnas. En este caso, cada fila es un array de longitud variable. Ejemplo: una matriz en la que la primera fila tiene 2 columnas, la segunda fila tiene 3 columnas y la tercera fila tiene 1 columna.

## Registros
Los registros son estructuras de datos estáticas que permiten agrupar diferentes tipos de datos bajo un único nombre o identificador. Cada uno de los elementos que conforman un registro se denomina campo y puede ser de cualquier tipo de dato, como enteros, caracteres, booleanos, etc. Los registros son útiles para representar entidades que tienen múltiples atributos de diferentes tipos de datos.

### Tipos:

Los registros pueden tener campos de cualquier tipo de dato, incluyendo tipos de datos simples (enteros, flotantes, caracteres, booleanos) y otros tipos de datos compuestos (arrays, otras estructuras de registro, listas, etc.). Además, los campos del registro pueden ser de diferente tamaño, lo que permite una mayor flexibilidad en la representación de información.

### Definición:

La definición de un registro implica la declaración de su estructura, es decir, los campos que lo componen y sus respectivos tipos de datos. La definición de un registro varía según el lenguaje de programación utilizado. Por ejemplo, en C, la definición de un registro se realiza mediante la palabra clave "struct":

```C
struct Estudiante {
  int id;
  char nombre[50];
  float promedio;
};
```

En este ejemplo, se define un registro llamado "Estudiante" con tres campos: "id" de tipo entero, "nombre" de tipo array de caracteres y "promedio" de tipo flotante.
### Tipos de registros
 los registros pueden tener longitudes fijas o variables, dependiendo de los campos que los componen y cómo se manejan en el lenguaje de programación específico.

**Registros de longitud fija**: Estos registros tienen un tamaño constante, ya que todos sus campos son de tamaño fijo. Es decir, cada campo tiene un tamaño predefinido en tiempo de compilación, y la suma de los tamaños de todos los campos determina el tamaño total del registro. Los registros de longitud fija son más simples de manejar y generalmente más rápidos en tiempo de ejecución, pero pueden ser menos flexibles y menos eficientes en términos de uso de la memoria en ciertos casos. Ejemplo:

```C
struct Empleado {
  int id;
  char nombre[50];
  float salario;
};
```
En este ejemplo, el registro "Empleado" tiene tres campos, todos de tamaño fijo, y la longitud del registro es la suma de los tamaños de los campos: 4 bytes (int) + 50 bytes (char array) + 4 bytes (float) = 58 bytes.

**Registros de longitud variable**: Estos registros tienen un tamaño variable, ya que al menos uno de sus campos es de tamaño variable. Estos campos pueden ser, por ejemplo, cadenas de caracteres con tamaño dinámico, listas enlazadas, entre otros. Los registros de longitud variable suelen ser más flexibles y eficientes en términos de uso de la memoria, pero también pueden ser más complejos de manejar y estar más expuestos a errores, como desbordamientos de memoria o fugas de memoria. Ejemplo:
```c
struct Articulo {
  int id;
  char *descripcion; // Puntero a una cadena de caracteres de tamaño variable
  float precio;
};
```
En este ejemplo, el registro "Articulo" tiene tres campos, pero uno de ellos, "descripcion", es un puntero a una cadena de caracteres de tamaño variable. La longitud del registro en sí es fija (suma de los tamaños de los campos: 4 bytes (int) + 8 bytes (puntero) + 4 bytes (float) = 16 bytes), pero el tamaño total ocupado por el registro y la cadena de caracteres a la que apunta "descripcion" es variable.


### Operaciones:

Las operaciones más comunes en registros son las siguientes:

Creación de registros: Crear una instancia de un registro utilizando su definición previamente establecida. Por ejemplo, en C:
```C
struct Estudiante estudiante1;
```

Acceso a campos: Leer o escribir valores en los campos de un registro. Para acceder a los campos de un registro, se utiliza el operador "." (punto) en la mayoría de los lenguajes de programación:

```C
estudiante1.id = 1;
estudiante1.promedio = 95.0;
strcpy(estudiante1.nombre, "Juan Pérez");
```
Asignación de registros: Asignar el contenido de un registro a otro registro de la misma estructura. En algunos lenguajes de programación, esta operación implica la copia de todos los campos de un registro a otro.

Comparación de registros: Comparar dos registros para determinar si son iguales o diferentes. Esta operación puede implicar la comparación de todos los campos de los registros o la comparación de campos específicos.

Pasar registros como argumentos a funciones o devolver registros desde funciones: Utilizar registros como parámetros de entrada, salida o entrada/salida en funciones, lo que permite una mayor modularidad y reutilización del código.

# BIBLIOGRAFÍA

> Stallings, W. (2016). Data and Computer Communications (10th ed.). Pearson.  
> Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). Introduction to Algorithms (3rd ed.). The MIT Press.  
> Joyanes, L (2008) Fundamentos de programación. Algoritmos, estructuras de datos y objetos. McGraw-Hill  
> Langsam, Tanembaum (1997) Estructuras de datos en C y C++  
> Daniel Liang, Y. (2017) Introduction to Java programming and data structures. Ed. Pearsons  