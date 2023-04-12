# TEMA 12: Organización lógica de los datos. Estructuras dinámicas.

# Introducción

En la era actual de la información, el manejo eficiente de los datos es un aspecto fundamental para el buen funcionamiento de cualquier sistema informático. Las estructuras de datos, tanto estáticas como dinámicas, desempeñan un papel crucial en la organización y manipulación de la información, lo que permite a los profesionales de la informática desarrollar soluciones eficientes y efectivas para una amplia gama de problemas. 

Una estructura de datos es una forma especializada de organizar y almacenar información que permite acceder y modificarla de manera eficiente. 

Las estructuras de datos dinámicas,  ~~ como los arrays y las estructuras de registros, son aquellas cuyo tamaño y organización se mantienen constantes a lo largo de la ejecución del programa. ~~ Estas estructuras son fundamentales para el diseño y análisis de algoritmos, ya que proporcionan una base sólida para el desarrollo de soluciones informáticas.

Según Cormen et al. (2009), ***"la elección adecuada de las estructuras de datos es crucial para el desempeño de un algoritmo, ya que esta elección afecta directamente la eficiencia en tiempo y espacio de la solución propuesta"***. Esta afirmación resalta la importancia de enseñar y dominar las estructuras de datos estáticas en la formación de futuros profesionales de la informática, ya que su comprensión y aplicación adecuada son esenciales para el éxito en la resolución de problemas y el desarrollo de sistemas informáticos eficientes.



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

Ventajas de la estructura de datos estática : 

- Tiempo de acceso rápido: Las estructuras de datos estáticas ofrecen un tiempo de acceso rápido porque la memoria se asigna en tiempo de compilación y el tamaño es fijo, lo que hace que acceder a los elementos sea una simple operación de indexación.
- Uso predecible de la memoria: Dado que la asignación de memoria se fija en tiempo de compilación, el programador puede predecir con exactitud cuánta memoria utilizará el programa, lo cual es un factor importante en entornos con restricciones de memoria.
- Facilidad de implementación y optimización: Las estructuras de datos estáticas pueden ser más fáciles de implementar y optimizar, ya que la estructura y el tamaño son fijos, y los algoritmos se pueden optimizar para la estructura de datos específica, lo que reduce las pérdidas de caché y puede aumentar el rendimiento general del programa.
- Gestión eficaz de la memoria: Las estructuras de datos estáticas permiten una asignación y gestión eficientes de la memoria. Dado que el tamaño de la estructura de datos se fija en tiempo de compilación, la memoria puede asignarse y liberarse de forma eficiente, sin necesidad de reasignaciones frecuentes o copias de memoria.
- Código simplificado: Dado que las estructuras de datos estáticas tienen un tamaño fijo, pueden simplificar el código al eliminar la necesidad de asignar memoria dinámica y la comprobación de errores asociada.
- Reducción de la sobrecarga: Las estructuras de datos estáticas suelen tener una sobrecarga menor que las dinámicas, ya que no requieren una contabilidad adicional para gestionar la asignación y liberación de memoria.

Ventajas de las estructuras de datos dinámicas : 

- Flexibilidad: Las estructuras de datos dinámicas pueden crecer o decrecer en tiempo de ejecución según sea necesario, lo que les permite adaptarse a los cambios en los requisitos de datos. Esta flexibilidad las hace idóneas para situaciones en las que el tamaño de los datos no se conoce de antemano o es probable que cambie con el tiempo.
- Menor desperdicio de memoria: Dado que las estructuras de datos dinámicas pueden cambiar de tamaño por sí mismas, pueden ayudar a reducir el desperdicio de memoria. Por ejemplo, si una matriz dinámica necesita crecer, puede asignar memoria adicional en el heap en lugar de reservar una gran cantidad fija de memoria que podría no utilizarse.
- Mejora del rendimiento de algunas operaciones: Las estructuras de datos dinámicas pueden ser más eficaces que las estáticas en determinadas operaciones. Por ejemplo, insertar o eliminar elementos en medio de una lista dinámica puede ser más rápido que con una matriz estática, ya que los elementos restantes pueden desplazarse de forma más eficiente.
- Código simplificado: Las estructuras de datos dinámicas pueden simplificar el código al eliminar la necesidad de gestionar manualmente la memoria. Las estructuras de datos dinámicas también pueden reducir la complejidad del código de las estructuras de datos que deben redimensionarse con frecuencia.
- Escalabilidad: Las estructuras de datos dinámicas pueden ser más escalables que las estáticas, ya que pueden adaptarse a las necesidades cambiantes de los datos a medida que éstos crecen. 
- 
# Estructuras de datos dinámicas

## Listas enlazadas
Las listas enlazadas son una estructura de datos lineal que consiste en una serie de nodos, donde cada nodo contiene un valor y una referencia al siguiente nodo de la lista. A diferencia de los arreglos, las listas enlazadas no tienen una capacidad fija y pueden crecer o disminuir de tamaño según sea necesario.

### Funcionamiento:

Cada nodo tiene dos partes: un campo de datos que contiene el valor almacenado y un campo de referencia que apunta al siguiente nodo de la lista.
El primer nodo de la lista se llama "cabeza" (head) y el último nodo se llama "cola" (tail). La cola apunta a un valor nulo, lo que indica el final de la lista.
Para recorrer la lista, se comienza desde el nodo cabeza y se sigue el enlace al siguiente nodo hasta llegar al final.

```
Copy code
    head                      tail
      |                         |
      v                         v
+----------+    +----------+    +----------+
| data | *---->| data | *---->| data |null|
+----------+    +----------+    +----------+
```

### Ejemplo de uso:

Las listas enlazadas son útiles en situaciones donde es necesario insertar o eliminar elementos con frecuencia, como en un administrador de tareas o en una cola de impresión.

Implementación en pseudocódigo:

```
Copy code
class Node
    data
    next

class LinkedList
    head
    tail

    function insertAtEnd(value)
        newNode = new Node(value, null)
        if head is null
            head = newNode
            tail = newNode
        else
            tail.next = newNode
            tail = newNode
        end if
    end function

    function deleteWithValue(value)
        if head is null
            return
        end if

        if head.data == value
            head = head.next
            return
        end if

        currentNode = head
        while currentNode.next is not null
            if currentNode.next.data == value
                currentNode.next = currentNode.next.next
                return
            end if
            currentNode = currentNode.next
        end while
    end function

    function printList()
        currentNode = head
        while currentNode is not null
            print currentNode.data
            currentNode = currentNode.next
        end while
    end function
end class
```
Este pseudocódigo define una clase Node que representa un nodo de la lista enlazada y una clase LinkedList que implementa la lista enlazada en sí. La clase LinkedList tiene métodos para insertar elementos al final de la lista, eliminar elementos con un valor específico y imprimir los elementos de la lista.


## Pilas (Stacks)
Son estructuras de datos que siguen una política de acceso LIFO (Last In, First Out), lo que significa que el último elemento añadido es el primero en ser eliminado. Se pueden visualizar como una colección de elementos apilados, donde solo se puede acceder al elemento superior.
### Funciones principales de una pila:

- push: agregar un elemento al tope de la pila
- pop: eliminar el elemento en el tope de la pila y devolver su valor
- peek: revisar el valor en el tope de la pila sin eliminarlo
### Diagrama de pila:

```
Copy code
   top
    |
    v
+-------+
| value |
+-------+
| value |
+-------+
| value |
+-------+
```


Las pilas se utilizan en situaciones donde se requiere un acceso LIFO, como en el control de llamadas a funciones en lenguajes de programación, algoritmos de búsqueda en profundidad y evaluación de expresiones aritméticas.

Implementación en pseudocódigo:

```javascript
Copy code
class Stack
    elements

    function push(value)
        elements.add(value)
    end function

    function pop()
        if isEmpty()
            return null
        end if
        return elements.removeLast()
    end function

    function peek()
        if isEmpty()
            return null
        end if
        return elements.last()
    end function

    function isEmpty()
        return elements.isEmpty()
    end function
end class
```

## Colas (Queues)

Son estructuras de datos que siguen una política de acceso FIFO (First In, First Out), lo que significa que el primer elemento añadido es el primero en ser eliminado. Se pueden visualizar como una fila de elementos, donde solo se puede acceder al elemento al frente de la fila.

### Funciones principales de una cola:

- enqueue: agregar un elemento al final de la cola
- dequeue: eliminar el elemento al frente de la cola y devolver su valor
- front: revisar el valor al frente de la cola sin eliminarlo

### Diagrama de cola:

```
Copy code
   front                       rear
    |                            |
    v                            v
+-------+     +-------+     +-------+
| value |<----| value |<----| value |
+-------+     +-------+     +-------+
```
### Ejemplo de uso de una cola:
Las colas se utilizan en situaciones donde se requiere un acceso FIFO, como en la planificación de procesos en sistemas operativos, algoritmos de búsqueda en anchura y simulaciones de eventos discretos.


```javascript
Copy code
class Queue
    elements

    function enqueue(value)
        elements.add(value)
    end function

    function dequeue()
        if isEmpty()
            return null
        end if
        return elements.removeFirst()
    end function

    function front()
        if isEmpty()
            return null
        end if
        return elements.first()
    end function

    function isEmpty()
        return elements.isEmpty()
    end function
end class
```

Estos pseudocódigos de pila y cola utilizan listas para almacenar sus elementos, aunque podrían implementarse también con arreglos o listas enlazadas.


## Árboles

Los árboles son una estructura de datos no lineal que consta de nodos organizados de manera jerárquica. Un árbol tiene un nodo raíz y, a partir de ahí, se ramifica en nodos hijos. Cada nodo hijo puede tener sus propios nodos hijos, formando así una estructura en forma de árbol.

### Funcionamiento:

Un árbol tiene un nodo raíz único desde el cual se originan todos los demás nodos.
Cada nodo del árbol tiene cero o más nodos hijos.
Un nodo sin hijos se denomina nodo hoja.
Los nodos que tienen al menos un hijo se denominan nodos internos.

### Diagrama de árbol genérico:

```mathematica

        A
      / | \
     B  C  D
    /|  |   \
   E F  G    H
```

Hay varios tipos de árboles con características específicas:

- Árbol binario: Un árbol en el que cada nodo tiene como máximo dos hijos, denominados hijo izquierdo y hijo derecho.
```mathematica

        A
       / \
      B   C
     / \   \
    D   E   F
```
- Árbol binario completo: Un árbol binario en el que todos los niveles, excepto quizás el último, están completamente llenos y todos los nodos están lo más a la izquierda posible.
```mathematica

        A
       / \
      B   C
     / \ /
    D  E F
```
- Árbol binario perfectamente equilibrado: Un árbol binario en el que todos los niveles están completamente llenos.
```mathematica

        A
       / \
      B   C
     / \ / \
    D  E F  G
```
- Árbol binario de búsqueda (BST): Un árbol binario con la propiedad de que el valor de cada nodo es mayor que o igual a los valores de todos los nodos en su subárbol izquierdo y menor o igual a los valores de todos los nodos en su subárbol derecho.
```
        8
       / \
      3   10
     / \   \
    1   6   14
       /  \
      4    7
```
Ejemplo de uso:

Los árboles se utilizan en situaciones donde se requiere una estructura de datos jerárquica, como el sistema de archivos de un computador, la representación de la jerarquía organizacional de una empresa o el análisis sintáctico en compiladores.

### Implementación en pseudocódigo (árbol binario de búsqueda):

```
class TreeNode
    value
    left
    right

class BinaryTree
    root

    function insert(value)
        root = insertNode(root, value)
    end function

    function insertNode(node, value)
        if node is null
            return new TreeNode(value, null, null)
        end if

        if value < node.value
            node.left = insertNode(node.left, value)
        else
            node.right = insertNode(node.right, value)
        end if

        return node
    end function

    function search(value)
        return searchNode(root, value)
    end function

    function searchNode(node, value)
        if node is null or node.value == value
            return node
        end if

        if value < node.value
  return searchNode(node.left, value)
    else
        return searchNode(node.right, value)
    end if
end function

function remove(value)
    root = removeNode(root, value)
end function

function removeNode(node, value)
    if node is null
        return null
    end if

    if value < node.value
        node.left = removeNode(node.left, value)
    else if value > node.value
        node.right = removeNode(node.right, value)
    else
        if node.left is null and node.right is null
            return null
        else if node.left is null
            return node.right
        else if node.right is null
            return node.left
        else
            minValueNode = findMinValueNode(node.right)
            node.value = minValueNode.value
            node.right = removeNode(node.right, minValueNode.value)
        end if
    end if

    return node
end function

function findMinValueNode(node)
    if node.left is null
        return node
    end if
    return findMinValueNode(node.left)
end function

function traverseInOrder()
    inOrderTraversal(root)
end function

function inOrderTraversal(node)
    if node is not null
        inOrderTraversal(node.left)
        print node.value
        inOrderTraversal(node.right)
    end if
end function
end class
```

Este pseudocódigo muestra la implementación de un árbol binario de búsqueda (BST) con funciones para insertar, buscar y eliminar nodos, así como para recorrer los nodos en orden ascendente. La estructura general de este pseudocódigo se puede adaptar a otros tipos de árboles modificando las funciones y reglas de inserción y eliminación según sea necesario.

## Grafos

Los grafos son una estructura de datos no lineal que consta de nodos (también llamados vértices) y aristas (también llamadas enlaces o conexiones) que conectan estos nodos. Los grafos se utilizan para representar relaciones entre pares de elementos.

### Funcionamiento:

Un grafo consta de un conjunto de nodos y un conjunto de aristas.
Cada arista conecta dos nodos y puede tener una dirección y un peso asociado.
Los grafos se pueden utilizar para representar redes, relaciones y conjuntos de datos interconectados.
Hay varios tipos de grafos con características específicas:

- Grafo no dirigido: Un grafo en el que las aristas no tienen dirección, lo que significa que si hay una arista entre dos nodos A y B, se puede viajar desde A hasta B y desde B hasta A.
Diagrama de grafo no dirigido:

```
   A--B
   | /|
   |/ |
   C--D
```
- Grafo dirigido (digrafo): Un grafo en el que las aristas tienen dirección, lo que significa que si hay una arista desde el nodo A al nodo B, no se puede viajar automáticamente desde B hasta A.
Diagrama de grafo dirigido:

```
   A-->B
   ^  /|
   | / v
   C<--D
```

- Grafo ponderado: Un grafo en el que las aristas tienen pesos asociados, que pueden representar costos, distancias u otras métricas relevantes.
Diagrama de grafo ponderado:

```
   A--4--B
   | \  |
  3|  \2|6
   |   \|
   C--5--D
  ```
### Ejemplo de uso:

Los grafos se utilizan en situaciones donde se requiere modelar relaciones entre elementos, como en la planificación de rutas en sistemas de navegación, sistemas de recomendación, redes sociales y la representación de dependencias en sistemas complejos.

### Implementación en pseudocódigo (grafo no dirigido y ponderado):

```
class Graph
    adjacencyList

    function addNode(node)
        adjacencyList[node] = []
    end function

    function addEdge(node1, node2, weight)
        adjacencyList[node1].append((node2, weight))
        adjacencyList[node2].append((node1, weight))
    end function

    function getNeighbors(node)
        return adjacencyList[node]
    end function

    function getWeight(node1, node2)
        for neighbor, weight in adjacencyList[node1]
            if neighbor == node2
                return weight
            end if
        end for
        return null
    end function

    function printGraph()
        for node, neighbors in adjacencyList
            print node, "->", neighbors
        end for
    end function
end class
```
Este pseudocódigo muestra la implementación de un grafo no dirigido y ponderado utilizando una lista de adyacencia para almacenar las conexiones entre los nodos. La estructura general de este pseudocódigo se puede adaptar a otros tipos de grafos modificando las funciones y reglas de conexión según sea necesario. Por ejemplo, para implementar un grafo dirigido, solo se agregaría una arista en una dirección en la función addEdge.


# BIBLIOGRAFÍA

> Stallings, W. (2016). Data and Computer Communications (10th ed.). Pearson.  
> Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2009). Introduction to Algorithms (3rd ed.). The MIT Press.  
> Joyanes, L (2008) Fundamentos de programación. Algoritmos, estructuras de datos y objetos. McGraw-Hill  
> Langsam, Tanembaum (1997) Estructuras de datos en C y C++  
> Daniel Liang, Y. (2017) Introduction to Java programming and data structures. Ed. Pearsons  