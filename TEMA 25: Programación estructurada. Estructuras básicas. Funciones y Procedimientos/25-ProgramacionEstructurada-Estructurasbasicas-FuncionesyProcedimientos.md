# TEMA 25: Programación estructurada. Estructuras básicas. Funciones y Procedimientos

# Introducción

# Programación Estructurada

La *programación estructurada* es un enfoque de la programación que busca facilitar la comprensión, diseño y mantenimiento de programas de software mediante el uso de estructuras de control simples y modulares. 

Surge como respuesta a los desafíos que enfrentaban los programadores en el desarrollo y mantenimiento de software durante las primeras décadas de la informática. En ese momento, muchos programas se escribían utilizando técnicas de programación desorganizadas y difíciles de comprender, como el uso excesivo de saltos incondicionales y código ensamblador. Estas prácticas conducían a programas difíciles de leer, mantener y depurar, lo que se conoció como "código espagueti". La programación estructurada surgió como una solución a estos problemas, proponiendo un enfoque sistemático y organizado para el diseño y desarrollo de software.

## Definición

La programación estructurada fue definida y promovida por varios científicos y programadores influyentes en la década de 1960 y 1970. Algunos de los principales contribuyentes a este campo incluyen:

*Edsger W. Dijkstra:* Dijkstra fue uno de los primeros en abogar por la programación estructurada y criticar el uso de saltos incondicionales (GOTO) en su famoso artículo "GOTO Statement Considered Harmful" publicado en 1968. También contribuyó a la formalización de las técnicas de programación estructurada en sus trabajos posteriores.

Corrado Böhm y Giuseppe Jacopini: En 1966, Böhm y Jacopini publicaron un artículo titulado *"Flow Diagrams, Turing Machines and Languages with Only Two Formation Rules"*, en el cual demostraron teóricamente que cualquier programa puede ser escrito utilizando únicamente tres tipos básicos de estructuras de control: secuencia, selección y repetición. Este trabajo proporcionó una base teórica sólida para la programación estructurada.

## Fundamentos

Los fundamentos de la programación estructurada se basan en las siguientes ideas y conceptos:

**Modularidad:** La modularidad se refiere a dividir un programa en funciones o módulos más pequeños e independientes, que pueden ser desarrollados, probados y depurados por separado. Esto mejora la organización del código, la reutilización y la facilidad de mantenimiento.

**Estructuras de control**: La programación estructurada utiliza tres tipos básicos de estructuras de control para gestionar el flujo de un programa: secuencial, selección y repetición.

a. Secuencial: El flujo de control se ejecuta en un orden secuencial, de arriba abajo, sin saltos ni ramificaciones.

b. Selección: Se utiliza para tomar decisiones en función de ciertas condiciones, como "if", "if-else" y "switch-case".

c. Repetición: Se utiliza para ejecutar un bloque de código varias veces, dependiendo de una condición. Incluye estructuras como "for", "while" y "do-while".

**Variables y tipos de datos:** La programación estructurada requiere el uso de variables y tipos de datos para almacenar y manipular información en un programa. Las variables tienen un tipo de dato asociado que define el tipo de información que pueden almacenar (enteros, flotantes, caracteres, etc.).

**Funciones y procedimientos:** Las funciones y procedimientos son bloques de código que realizan una tarea específica y pueden ser llamados desde cualquier parte del programa. Ayudan a reducir la redundancia de código y a mejorar la legibilidad y la modularidad del programa.

**Diseño descendente (Top-down):** La programación estructurada sigue un enfoque de diseño descendente, en el cual se descompone un problema en subproblemas más pequeños y se abordan estos subproblemas de manera individual. Este enfoque permite un diseño más ordenado y sistemático de los programas.

# Estructuras básicas
utilizando principalmente tres estructuras de control: secuencial, selección y repetición.

- **Secuencial:** Es la más básica y natural. Las instrucciones se ejecutan una tras otra en el orden en que aparecen en el programa.

- **Selección:** Las instrucciones se ejecutan según alguna condición. Incluye la estructura if-else y switch-case.

- **Repetición:** Las instrucciones se repiten mientras se cumpla alguna condición. Incluye las estructuras for, while, y do-while.

Ahora, hagamos un esquema para cada estructura de control:

**Secuencial:**

```
    A[Inicio] --> B[Instrucción 1]
    B --> C[Instrucción 2]
    C --> D[Instrucción 3]
    D --> E[Fin]
```

En este esquema, las instrucciones se ejecutan en secuencia desde el inicio hasta el final.

**Selección (if-else):**

```
    A[Inicio] --> B{Condición}
    B -- Si --> C[Instrucción 1]
    B -- No --> D[Instrucción 2]
    C --> E[Fin]
    D --> E
```

En este esquema, si la condición es verdadera, se ejecuta la Instrucción 1. Si la condición es falsa, se ejecuta la Instrucción 2.

**Repetición (while):**

```
    A[Inicio] --> B{Condición}
    B -- Si --> C[Instrucción]
    C --> B
    B -- No --> D[Fin]
```
En este esquema, mientras la condición sea verdadera, se ejecuta la instrucción y se vuelve a comprobar la condición. Cuando la condición es falsa, se termina el ciclo.

# Funciones y procedimientos

En la programación, los términos "función" y "procedimiento" se utilizan a veces de manera intercambiable, pero técnicamente tienen diferencias importantes. Ambos son subrutinas, es decir, bloques de código que pueden ser llamados desde diferentes lugares en un programa. Sin embargo, difieren principalmente en si devuelven o no un valor.

## Funciones

En programación, una función es un bloque de código organizado y reutilizable que realiza una tarea específica. Las funciones proporcionan una mejor modularidad para tu aplicación y un alto grado de reutilización de código.

Aquí están los principales conceptos relacionados con las funciones en la programación:

**Definición de la función:** Para definir una función, generalmente necesitas proporcionar un nombre para la función, posiblemente algunos parámetros y luego el bloque de código que la constituye.

**Parámetros de la función:** Los parámetros son valores que puedes pasar a una función para que los utilice cuando realice su tarea. Los parámetros se definen en la declaración de la función y se convierten en variables dentro del cuerpo de la función cuando se llama a la función.

**Llamada de función:** Una vez que se define una función, puedes "llamar" a la función por su nombre en cualquier parte de tu código. Cuando se llama a una función, el control del programa se traslada a la función definida y los parámetros (si los hay) se pasan a la función.

**Valor de retorno de la función:** Una función puede devolver un valor. En otras palabras, después de que se ejecuta la función, puede producir un resultado que luego se puede usar en otras partes de tu código. Para devolver un valor, se usa la palabra clave 'return' en la mayoría de los lenguajes de programación.

**Funciones de primera clase:** En algunos lenguajes de programación, las funciones son "de primera clase", lo que significa que las funciones se pueden asignar a variables, almacenar en estructuras de datos, pasar como argumentos a otras funciones y devolver como valores de otras funciones.

Un ejemplo de una función simple en Python sería:
```python
def saludo(nombre):
    return "Hola, " + nombre

print(saludo("Mundo"))  # Imprime: Hola, Mundo

```
### Funciones Lambda
Las funciones Lambda (también conocidas como funciones anónimas o funciones de flecha en algunos lenguajes como JavaScript) son funciones que se definen sin un nombre. Mientras que las funciones normales se definen usando la palabra clave def en Python y function en JavaScript, las funciones lambda se definen usando la palabra clave lambda y => respectivamente.

- Diferencias:

**Sintaxis:** Las funciones lambda generalmente tienen una sintaxis más concisa que las funciones tradicionales. Esto las hace útiles para pequeñas funciones que se utilizan una vez o un número limitado de veces.

**Nombre:** Las funciones lambda son funciones anónimas. Esto significa que no necesitan un nombre cuando se definen.

**Número de expresiones:** Las funciones lambda están limitadas a una sola expresión. Esto significa que no puedes tener bloques de código complejos dentro de una función lambda.

**Valor de retorno:** En una función lambda, el valor de retorno es el resultado de la expresión única. No necesitas usar la palabra clave return.

- Ventajas de las funciones lambda:

**Sintaxis concisa:** Las funciones lambda pueden ser más breves que las funciones tradicionales, lo que puede hacer que tu código sea más fácil de leer (si se usa correctamente).

**Uso en tiempo de ejecución:** Dado que son anónimas, las funciones lambda pueden definirse y utilizarse justo donde las necesitas, como dentro de funciones de orden superior, como map(), filter(), reduce() en Python o JavaScript.

**No requieren una declaración de función:** No necesitas nombrar una función lambda, lo que las hace convenientes para usar en lugares donde solo necesitas una pequeña función una vez.


## Procedimientos

Un procedimiento, también conocido a veces como subrutina, procedimiento almacenado, procedimiento void o método, es un conjunto de instrucciones de código que realiza una tarea específica en un programa. La idea es que una tarea que necesita realizarse varias veces puede ser aislada en un procedimiento para evitar repetir el mismo código en varios lugares.

Las características principales de un procedimiento son las siguientes:

**Tarea específica:** Un procedimiento se utiliza para realizar una tarea específica en un programa. Esa tarea podría ser algo como imprimir un mensaje en la pantalla, calcular el valor de una función matemática, etc.

**Reutilización de código:** El principal beneficio de un procedimiento es que permite reutilizar código. Si tienes una tarea que necesita realizarse en varios lugares, puedes aislarla en un procedimiento y luego llamar a ese procedimiento desde todos los lugares necesarios.

**Parámetros:** Un procedimiento puede tener parámetros, que son valores que se pasan al procedimiento cuando se llama. Dentro del procedimiento, los parámetros se tratan como variables locales que pueden ser utilizadas para realizar la tarea del procedimiento.

**No devuelve un valor:** A diferencia de una función, un procedimiento normalmente no devuelve un valor. En lugar de eso, realiza su tarea y luego termina. Dicho esto, el uso de este término puede variar entre diferentes lenguajes de programación. En algunos lenguajes, un "procedimiento" puede ser simplemente una función que no devuelve un valor (o devuelve void).


# Parámetros y ámbito

En programación, cuando pasamos parámetros a una función o método, generalmente lo hacemos de una de dos maneras: *paso por valor* o *paso por referencia.* En el caso del lenguaje de programación Java, debido a su diseño y semántica, se dice a menudo que los parámetros se pasan "por valor". Sin embargo, es importante entender lo que realmente significa en este contexto.

**Paso por valor: **En el paso por valor, una copia del valor del argumento se pasa a la función. Cualquier cambio que hagas en el parámetro dentro de la función no afectará el valor original. Java utiliza el paso por valor para tipos de datos primitivos.

Ejemplo en Java:
```java 
public class Test {
    static void updateValue(int value) {
        value = 55;
    }

    public static void main(String[] args) {
        int value = 22;
        updateValue(value);
        System.out.println(value);  // Imprime: 22
    }
}
```
En este ejemplo, el valor de la variable value en el método main no se ve afectado por lo que ocurre en el método updateValue.

**Paso por referencia:** En el paso por referencia, lo que realmente se pasa es la referencia al objeto, no una copia del objeto en sí. Por lo tanto, si modificas el objeto dentro de la función, el cambio se reflejará fuera de la función. Aunque Java no admite el paso por referencia en el sentido estricto de la palabra, cuando pasamos un objeto a un método, el "valor" que se pasa es realmente la referencia al objeto.

Ejemplo en Java:
```java 
public class Test {
    static void updateObjectValue(MyObject obj) {
        obj.setValue(55);
    }

    public static void main(String[] args) {
        MyObject obj = new MyObject(22);
        updateObjectValue(obj);
        System.out.println(obj.getValue());  // Imprime: 55
    }
}

class MyObject {
    private int value;

    public MyObject(int value) {
        this.value = value;
    }

    public void setValue(int value) {
        this.value = value;
    }

    public int getValue() {
        return this.value;
    }
}

```

En este ejemplo, el método updateObjectValue cambia el valor del objeto MyObject que se pasa. Aunque la referencia al objeto se pasa por valor, la referencia en sí apunta al mismo objeto, por lo que los cambios en el objeto son visibles fuera del método.

## Ámbito o scope
El ámbito (también conocido como "scope" en inglés) de una variable, parámetro o método se refiere a la región del código en la que es visible y puede ser referenciada o accedida. Los conceptos clave en relación con el ámbito incluyen el ámbito de bloque, el ámbito de clase y el ámbito de método.

**Ámbito de bloque: **Una variable definida dentro de un bloque de código (como dentro de un método, un bucle for o una declaración if) solo es visible y accesible dentro de ese bloque de código.

Ejemplo en Java:
```java 
public void myMethod() {
    int x = 10;  // x tiene ámbito de bloque, solo es visible dentro de este método

    if (x == 10) {
        int y = 20;  // y tiene ámbito de bloque, solo es visible dentro de esta declaración if
        System.out.println(x + y);  // Imprime: 30
    }

    // System.out.println(y);  // Esto daría un error de compilación porque y no es visible aquí
}

```

**Ámbito de clase:** Una variable definida a nivel de clase (también conocida como variable de miembro o de instancia) es visible y accesible en todos los métodos y bloques de código dentro de la clase.

Ejemplo en Java:
```java 
public class MyClass {
    private int x = 10;  // x tiene ámbito de clase, es visible dentro de toda la clase

    public void method1() {
        System.out.println(x);  // Imprime: 10
    }

    public void method2() {
        System.out.println(x);  // Imprime: 10
    }
}
```

**Ámbito de método (parámetros):** Los parámetros de un método tienen ámbito de método, es decir, solo son visibles y accesibles dentro del método en el que están definidos.

Ejemplo en Java:
```java 
public void myMethod(int x) {  // x tiene ámbito de método, es visible dentro de este método
    System.out.println(x);
}

public void anotherMethod() {
    // System.out.println(x);  // Esto daría un error de compilación porque x no es visible aquí
}
```