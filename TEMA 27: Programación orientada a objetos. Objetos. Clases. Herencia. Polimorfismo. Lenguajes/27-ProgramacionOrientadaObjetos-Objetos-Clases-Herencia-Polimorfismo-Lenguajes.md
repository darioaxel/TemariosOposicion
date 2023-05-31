# Tema 27: Programación orientada a objetos
> #### Bloque 3
---

- [Tema 27: Programación orientada a objetos](#tema-27-programación-orientada-a-objetos)
  - [2. Programación orientada a objetos](#2-programación-orientada-a-objetos)
    - [2.1. Definición y características](#21-definición-y-características)
    - [2.2. Ventajas sobre otros tipos de programación](#22-ventajas-sobre-otros-tipos-de-programación)
  - [3. Clases](#3-clases)
    - [3.1. Definición](#31-definición)
    - [3.2. Miembros de una clase (encapsulación)](#32-miembros-de-una-clase-encapsulación)
    - [3.3. Constructores y destructores](#33-constructores-y-destructores)
    - [3.4. Niveles de acceso a los componentes](#34-niveles-de-acceso-a-los-componentes)
  - [4. Herencia](#4-herencia)
    - [4.1. Definición](#41-definición)
    - [4.2. Tipos de herencia](#42-tipos-de-herencia)
    - [4.3. Funcionalidades de la herencia](#43-funcionalidades-de-la-herencia)
  - [5. Polimorfismo](#5-polimorfismo)
    - [5.1. Sobrecarga de método](#51-sobrecarga-de-método)
    - [5.2. Sobrecarga de operadores](#52-sobrecarga-de-operadores)
  - [6. Lenguajes Orientados a objetos](#6-lenguajes-orientados-a-objetos)
    - [6.1. Lenguajes orientados a objetos puros e híbridos](#61-lenguajes-orientados-a-objetos-puros-e-híbridos)
    - [6.2. Java](#62-java)
    - [6.2.1. Tipos de herencia y polimorfismo en Java](#621-tipos-de-herencia-y-polimorfismo-en-java)
        - [Herencia simple en Java](#herencia-simple-en-java)
        - [Polimorfismo en Java](#polimorfismo-en-java)
    - [6.2.2. Clases abstractas e interfaces](#622-clases-abstractas-e-interfaces)
    - [6.3. Lenguajes más utilizados y orientación a objetos](#63-lenguajes-más-utilizados-y-orientación-a-objetos)
  - [7. Conclusión](#7-conclusión)
    - [7.1. Relación del tema con la enseñanza en fp](#71-relación-del-tema-con-la-enseñanza-en-fp)
  - [Referencias Bibliográficas:](#referencias-bibliográficas)
  - [8. Bibliografía](#8-bibliografía)

## 2. Programación orientada a objetos

### 2.1. Definición y características

La Programación Orientada a Objetos (POO) es un paradigma de programación que utiliza objetos y sus interacciones para diseñar aplicaciones y programas de software. Como Grady Booch, uno de los pioneros en esta área, afirmó: "La programación orientada a objetos es un método de implementación en el que los programas se organizan como objetos cooperantes, cada uno de los cuales representa una instancia de alguna clase, y cuyas clases son miembros de una jerarquía de clases unidas por medio de relaciones de herencia" (Booch, 1991).

Esta metodología está basada en varios principios, entre los que se incluyen la abstracción, la encapsulación, la herencia y el polimorfismo.

- **Abstracción**: La abstracción se refiere a la capacidad de ignorar los detalles de las partes para enfocarse en un nivel más alto de un problema. Por ejemplo, cuando conducimos un coche, no necesitamos entender todos los detalles de cómo funciona el motor o el sistema de frenado; simplemente necesitamos saber cómo usar los controles.

- **Encapsulación**: La encapsulación es un método para ocultar los valores o el estado de un objeto de datos estructurado, evitando el acceso directo al mismo. En un objeto 'coche', por ejemplo, los datos del motor estarían encapsulados y solo se podría interactuar con ellos a través de métodos específicos, como 'arrancar' o 'parar'.

- **Herencia**: La herencia es un principio que permite distribuir métodos y campos de una clase a otra. Por ejemplo, si tenemos una clase 'vehículo', podríamos tener clases 'coche' y 'camión' que hereden atributos de 'vehículo', como la velocidad máxima o el número de ruedas.

- **Polimorfismo**: El polimorfismo permite tratar objetos de diferentes clases de la misma manera, siempre y cuando compartan el mismo método o interfaz. Por ejemplo, si tenemos una función 'dibujar' que puede dibujar diferentes formas (círculos, cuadrados, triángulos), podemos pasar cualquier objeto de esas clases a la función 'dibujar' y se comportará de la manera apropiada.

### 2.2. Ventajas sobre otros tipos de programación

La Programación Orientada a Objetos tiene varias ventajas sobre otros tipos de programación, como la programación procedural o la programación funcional. Algunas de estas ventajas son:

- **Reutilización de código**: Gracias a la herencia y el polimorfismo, es posible reutilizar y extender las clases existentes. Por ejemplo, si ya tenemos una clase 'coche' y queremos crear una clase 'coche eléctrico', podemos heredar la mayoría de las características de 'coche' y simplemente añadir o modificar las que son únicas para 'coche eléctrico'.

- **Modularidad**: Los objetos en la POO se crean de manera independiente y pueden interactuar entre sí, lo que proporciona una estructura de código más limpia y fácil de mantener. Por ejemplo, en un programa de gestión de una biblioteca, podríamos tener objetos separados para 'libros', 'usuarios' y 'préstamos', cada uno con sus propias propiedades y métodos.

- **Intuitividad**: Los objetos son a menudo analogías de objetos del mundo real, lo que hace que el código sea más comprensible y más fácil de diseñar y mantener. Por ejemplo, es mucho más intuitivo diseñar una clase 'Perro' con propiedades como 'raza', 'edad' y 'color', y métodos como 'ladrar' y 'comer', que tratar de modelar esas características y comportamientos en una estructura de datos abstracta o un conjunto de funciones no relacionadas.

## 3. Clases

### 3.1. Definición

Una clase en la programación orientada a objetos es, según Erich Gamma, uno de los "Gang of Four", "un modelo o prototipo que define las variables y los métodos comunes a todos los objetos de cierto tipo" (Gamma et al., 1994). Esencialmente, una clase es un plano o plantilla para crear objetos. Por ejemplo, podríamos tener una clase 'Perro' que define propiedades como 'raza', 'edad' y 'color', y métodos como 'ladrar' y 'comer'.

### 3.2. Miembros de una clase (encapsulación)

Los miembros de una clase son las propiedades y los métodos que definen esa clase. Por ejemplo, en una clase 'Perro', los miembros podrían incluir propiedades como 'raza', 'edad' y 'color', y métodos como 'ladrar' y 'comer'. 

La encapsulación se refiere a la práctica de hacer que los miembros de una clase sean privados o protegidos, es decir, solo accesibles desde dentro de la propia clase, y proporcionar métodos públicos para interactuar con esos miembros. Por ejemplo, podríamos tener un método 'ponerEdad' que nos permite cambiar la edad de un perro, pero no podríamos cambiar directamente la propiedad 'edad' desde fuera de la clase.

### 3.3. Constructores y destructores

Un constructor es un método especial de una clase que se invoca cuando se crea un objeto de esa clase. El propósito de un constructor es inicializar el objeto. Por ejemplo, cuando creamos un nuevo objeto 'Perro', el constructor podría establecer la raza, la edad y el color de ese perro.

Un destructor es un método que se invoca cuando un objeto está a punto de ser destruido. Su propósito es liberar los recursos que el objeto ha estado utilizando. En la mayoría de los lenguajes de programación orientados a objetos modernos, como Java y Python, la gestión de memoria se realiza automáticamente, y no es necesario definir destructores explícitos.

### 3.4. Niveles de acceso a los componentes

Los niveles de acceso determinan la visibilidad de las variables, métodos y clases en la programación orientada a objetos. Hay tres niveles de acceso principales:

- **Privado**: Los miembros privados de una clase solo pueden ser accedidos desde dentro de la misma clase.

- **Protegido**: Los miembros protegidos pueden ser accedidos desde la misma clase y desde sus subclases.

- **Público**: Los miembros públicos pueden ser accedidos desde cualquier parte del código.

Estos niveles de acceso permiten un alto grado de control sobre cómo y dónde se pueden utilizar los miembros de una clase, lo que contribuye a la encapsulación y la seguridad del código.

## 4. Herencia

### 4.1. Definición

La herencia es un principio fundamental de la programación orientada a objetos que permite crear una nueva clase a partir de una existente. Según Barbara Liskov, profesora del Instituto de Tecnología de Massachusetts (MIT) y una de las figuras más relevantes en el desarrollo de la POO, "la herencia es una forma de factorización del código que permite definir una clase en términos de otra ya definida con la posibilidad de reutilizar, extender y modificar el comportamiento que se hereda" (Liskov & Guttag, 2001).

Por ejemplo, podríamos tener una clase 'Animal' con propiedades como 'nombre', 'edad' y 'peso', y una clase 'Perro' que hereda de 'Animal' y añade una propiedad adicional, 'raza'.

### 4.2. Tipos de herencia

Existen varios tipos de herencia en la programación orientada a objetos, los cuales permiten una gran flexibilidad en la forma en que se pueden organizar y reutilizar las clases:

- **Herencia simple**: Una clase solo puede heredar de una única clase. Por ejemplo, en el caso de 'Perro' heredando de 'Animal'.

- **Herencia múltiple**: Una clase puede heredar de varias clases. Este tipo de herencia puede ser poderoso, pero también puede llevar a complicaciones, como el problema del diamante (cuando una clase hereda de dos clases que a su vez heredan de una misma clase). Algunos lenguajes de programación, como Python, permiten la herencia múltiple, mientras que otros, como Java, no la soportan.

- **Herencia multinivel**: Una clase puede heredar de otra clase que a su vez hereda de otra clase, y así sucesivamente. Por ejemplo, podríamos tener una clase 'Mamífero' que hereda de 'Animal', y luego una clase 'Perro' que hereda de 'Mamífero'.

### 4.3. Funcionalidades de la herencia

La herencia proporciona varias funcionalidades útiles en la programación orientada a objetos:

- **Reutilización de código**: Una clase que hereda de otra puede reutilizar todos los miembros públicos y protegidos de la clase padre.

- **Polimorfismo**: Un objeto de una subclase puede ser tratado como un objeto de su superclase. Por ejemplo, si tenemos un método que toma un 'Animal' como argumento, podemos pasarle un 'Perro', ya que un 'Perro' es un tipo de 'Animal'.

- **Organización y estructura**: La herencia permite organizar las clases en una jerarquía que refleja las relaciones "es un tipo de" entre diferentes tipos de objetos.

## 5. Polimorfismo

### 5.1. Sobrecarga de método

La sobrecarga de método es una característica del polimorfismo en la que una clase tiene varios métodos con el mismo nombre, pero con diferentes parámetros. Esencialmente, estos métodos realizan la misma función básica, pero están configurados para trabajar con diferentes tipos o números de argumentos. 

Por ejemplo, podríamos tener una clase 'Calculadora' con un método 'sumar' que puede tomar dos números enteros, dos números de coma flotante o una lista de números. La implementación exacta del método 'sumar' que se llamará dependerá de los argumentos que se pasen.

```java
public class Calculadora {
    int sumar(int a, int b) {
        return a + b;
    }

    float sumar(float a, float b) {
        return a + b;
    }

    int sumar(int[] numeros) {
        int suma = 0;
        for (int numero : numeros) {
            suma += numero;
        }
        return suma;
    }
}
```

### 5.2. Sobrecarga de operadores

La sobrecarga de operadores es una característica de algunos lenguajes de programación orientados a objetos que permite cambiar la forma en que funcionan los operadores integrados para tipos de datos definidos por el usuario. Esto significa que puedes definir cómo se deben comportar los operadores (como +, -, *, /, etc.) cuando se aplican a objetos de una clase específica.

Por ejemplo, en C++, podríamos sobrecargar el operador + para una clase 'Vector', para que puedas sumar dos objetos 'Vector' usando el operador +, en lugar de tener que llamar a un método 'sumar'.

```cpp
class Vector {
public:
    int x, y;

    Vector(int x, int y) : x(x), y(y) {}

    Vector operator + (const Vector& otro) {
        return Vector(x + otro.x, y + otro.y);
    }
};
```

En este caso, si tienes dos vectores v1 y v2, puedes sumarlos simplemente escribiendo "v1 + v2".

Es importante destacar que no todos los lenguajes de programación permiten la sobrecarga de operadores. Por ejemplo, Java no lo permite, mientras que lenguajes como C++ y Python sí.



## 6. Lenguajes Orientados a objetos

### 6.1. Lenguajes orientados a objetos puros e híbridos
Los lenguajes orientados a objetos puros son aquellos que están completamente diseñados y orientados a la Programación Orientada a Objetos, donde todos los elementos del lenguaje son objetos y se siguen rigurosamente los principios de la POO. Ejemplos de lenguajes orientados a objetos puros incluyen Smalltalk y Ruby.

Por otro lado, los lenguajes orientados a objetos híbridos son aquellos que combinan características de la POO con elementos de otros paradigmas de programación, como la programación imperativa o la programación funcional. Lenguajes como Java y C++ son considerados lenguajes orientados a objetos híbridos, ya que permiten la programación orientada a objetos pero también admiten otros estilos de programación.

### 6.2. Java

Java es uno de los lenguajes de programación orientados a objetos más populares y ampliamente utilizados. Fue desarrollado por Sun Microsystems (ahora propiedad de Oracle) en la década de 1990 con el objetivo de ser "simple, orientado a objetos y familiar" (Gosling et al., 2000). 

Java implementa completamente los conceptos de la programación orientada a objetos, incluyendo clases, objetos, herencia, polimorfismo y encapsulación. Además, tiene varias características que lo hacen particularmente adecuado para aplicaciones empresariales y de gran escala, como su robusto sistema de manejo de excepciones, su soporte para multithreading y su recolector de basura automático.

Un ejemplo sencillo de una clase en Java sería:

```java
public class Perro {
    // Propiedades
    private String raza;
    private int edad;

    // Constructor
    public Perro(String raza, int edad) {
        this.raza = raza;
        this.edad = edad;
    }

    // Métodos
    public void ladrar() {
        System.out.println("Guau!");
    }

    public void cumplirAños() {
        this.edad += 1;
    }
}
```
### 6.2.1. Tipos de herencia y polimorfismo en Java
En Java, se pueden implementar diferentes tipos de herencia y polimorfismo. A continuación, se explican algunos ejemplos de cada uno:

##### Herencia simple en Java
La herencia simple en Java permite que una subclase herede de una única superclase. La subclase adquiere los atributos y métodos de la superclase y puede añadir nuevos atributos y métodos propios.

```java

public class Animal {
    public void emitirSonido() {
        System.out.println("El animal emite un sonido");
    }
}

public class Perro extends Animal {
    public void ladrar() {
        System.out.println("El perro está ladrando");
    }
}
```

En este ejemplo, la clase Perro hereda de la clase Animal. La subclase Perro tiene su propio método ladrar(), además de heredar el método emitirSonido() de la superclase Animal.

##### Polimorfismo en Java
El polimorfismo en Java se puede lograr mediante la herencia y la implementación de interfaces. Permite utilizar un objeto de una subclase como si fuera un objeto de la superclase, permitiendo así reutilizar el código y hacer que el programa sea más flexible.

```java
public interface Animal {
    void emitirSonido();
}

public class Perro implements Animal {
    public void emitirSonido() {
        System.out.println("El perro ladra");
    }
}

public class Gato implements Animal {
    public void emitirSonido() {
        System.out.println("El gato maulla");
    }
}
```

En este ejemplo, la interfaz Animal define el método emitirSonido(). La clase Perro y la clase Gato implementan la interfaz Animal y proporcionan su propia implementación del método emitirSonido(). Luego, se puede tratar un objeto de tipo Perro o Gato como un objeto de tipo Animal y llamar al método emitirSonido() en ambos casos.

### 6.2.2. Clases abstractas e interfaces
En Java, las clases abstractas e interfaces son constructos utilizados para definir comportamientos y establecer contratos para las clases que las implementan.

**Clases abstractas:** Una clase abstracta en Java es una clase que no se puede instanciar directamente, sino que se utiliza como base para otras clases. Puede contener métodos abstractos (sin implementación) y métodos concretos (con implementación). Las clases que heredan de una clase abstracta deben implementar todos los métodos abstractos definidos en la clase padre.

**Interfaces:** Una interfaz en Java es una colección de métodos abstractos (sin implementación) y constantes. Las interfaces se utilizan para definir un contrato que las clases deben cumplir. Una clase puede implementar múltiples interfaces, lo que permite lograr la herencia múltiple en Java.

### 6.3. Lenguajes más utilizados y orientación a objetos

Muchos de los lenguajes de programación más utilizados son orientados a objetos o incluyen características de la programación orientada a objetos. Algunos de estos incluyen:

- **Python**: Es un lenguaje interpretado y dinámico que es famoso por su legibilidad y simplicidad. Aunque es multiparadigma (admite varios estilos de programación), Python tiene un fuerte soporte para la programación orientada a objetos.

- **C++**: Es un lenguaje de programación de propósito general que ofrece un soporte de bajo nivel y de alto nivel. C++ es una extensión del lenguaje C que añade soporte para la programación orientada a objetos.

- **C#**: Es un lenguaje de programación moderno desarrollado por Microsoft. C# es completamente orientado a objetos y se utiliza principalmente para desarrollar aplicaciones de Windows y juegos con el motor de juegos Unity.

- **JavaScript**: Aunque es conocido como un lenguaje de programación para la web, JavaScript también soporta la programación orientada a objetos. JavaScript utiliza un modelo de objetos basado en prototipos, que es un poco diferente del modelo de clases utilizado en la mayoría de los otros lenguajes orientados a objetos.

## 7. Conclusión

### 7.1. Relación del tema con la enseñanza en fp

La programación orientada a objetos (POO) es un pilar esencial en la formación en tecnología de la información y comunicación. Su estudio y comprensión son fundamentales en los programas educativos de Formación Profesional (FP) relacionados con el desarrollo de software.

El conocimiento de los conceptos fundamentales de la POO, como las clases, los objetos, la herencia, el polimorfismo y la encapsulación, no solo proporciona a los estudiantes las herramientas necesarias para diseñar y construir software de calidad, sino que también promueve una mentalidad de resolución de problemas que es útil en todas las áreas de la informática.

Además, dado que muchos de los lenguajes de programación más populares y utilizados en la industria son orientados a objetos (como Java, C++, C# y Python), el estudio de la POO prepara a los estudiantes para una amplia gama de roles en el desarrollo de software, desde el desarrollo de aplicaciones web y móviles hasta el desarrollo de juegos y sistemas empresariales.

Por lo tanto, es esencial que los profesores de FP estén bien versados en la POO y sean capaces de transmitir estos conceptos de manera efectiva a sus estudiantes. La inclusión de ejemplos prácticos y relevantes, así como la realización de proyectos de programación orientada a objetos, puede ayudar a los estudiantes a consolidar su comprensión de la POO y a desarrollar habilidades prácticas que serán valiosas en su futura carrera.

## Referencias Bibliográficas:

Gosling, J., Joy, B., Steele, G., & Bracha, G. (2000). The Java Language Specification (2nd Edition). Addison-Wesley.

Liskov, B., & Guttag, J. (2001). Program Development in Java: Abstraction, Specification, and Object-Oriented Design. Addison-Wesley.

Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). Design Patterns: Elements of Reusable Object-Oriented Software. Addison-Wesley.



## 8. Bibliografía
> Booch, G. (1991). ***Object Oriented Design: With Applications.*** Benjamin Cummings.

> Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). ***Design Patterns: Elements of Reusable Object-Oriented Software.*** Addison-Wesley Professional.  

> Liskov, B., & Guttag, J. (2001). ***Program Development in Java: Abstraction, Specification, and Object-Oriented Design.*** Addison-Wesley.

> Gosling, J., Joy, B., Steele, G., & Bracha, G. (2000). ***The Java Language Specification (2nd Edition).*** Addison-Wesley.  

> Fowler, M. (2002). ***Patterns of Enterprise Application Architecture.*** Addison-Wesley Professional.  
