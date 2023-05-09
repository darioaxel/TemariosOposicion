# Introducción

# Programación Modular

La **programación modular **es un enfoque de diseño de software que subdivide una aplicación en una serie de partes o módulos funcionales separados. Cada módulo se centra en una única responsabilidad y puede funcionar de forma independiente. Este enfoque tiene como objetivo hacer que los programas sean más fáciles de leer, entender, mantener y reutilizar.

La programación modular surgió en los años 60 y 70 como respuesta a los desafíos que planteaba el crecimiento de los programas de software. A medida que los programas se volvían más grandes y complejos, era cada vez más difícil entender y mantener todo el código en un solo lugar. La programación modular ofrecía una solución a este problema, al permitir que los desarrolladores dividieran los programas en piezas más pequeñas y manejables.


La programación modular es beneficiosa por varias razones:

Legibilidad: Los módulos más pequeños y bien definidos son más fáciles de leer y entender que un gran bloque de código.

Mantenibilidad: Es más fácil hacer cambios en un módulo individual sin afectar al resto del programa.

Reutilización de código: Los módulos que realizan funciones útiles pueden reutilizarse en diferentes programas.

Depuración: Los errores son más fáciles de localizar y corregir cuando el código está dividido en módulos.

Desarrollo paralelo: Diferentes equipos o individuos pueden trabajar en diferentes módulos al mismo tiempo, lo que puede acelerar el proceso de desarrollo.

# Recursividad

La recursividad es un concepto fundamental en la programación que se refiere a la capacidad de una función o procedimiento de llamarse a sí misma de forma repetitiva hasta alcanzar una condición de salida o base que detenga la recursión. En términos más técnicos, la recursividad es un método que permite la definición de una función en términos de sí misma.

El uso de la recursividad en la programación puede ser muy útil para resolver problemas que involucran estructuras de datos complejas o para simplificar la implementación de algoritmos que involucran iteraciones complejas. Por ejemplo, la recursividad es comúnmente utilizada en la implementación de algoritmos de búsqueda, ordenamiento y análisis de árboles.

Sin embargo, la recursividad también puede llevar a errores y problemas de rendimiento si no se utiliza adecuadamente. Por lo tanto, es importante tener en cuenta ciertas consideraciones al utilizar la recursividad en la programación, como establecer una condición de salida clara y asegurarse de que la recursión no se vuelva infinita.

## Estructura de una función recursiva

La estructura de una función recursiva consta de dos partes principales: el caso base y el caso recursivo.

El caso base es la condición que detiene la recursión. Es decir, es el caso en el que la función deja de llamarse a sí misma y devuelve un valor. Este caso es fundamental para evitar la recursión infinita y asegurar que la función se detenga en algún momento.

El caso recursivo, por otro lado, es la parte de la función que se llama a sí misma. En este caso, se realiza una llamada a la misma función con una entrada ligeramente diferente. En cada llamada, se acerca al caso base hasta que se alcanza y se devuelve un valor.

La combinación del caso base y el caso recursivo es lo que hace que una función sea recursiva. La función se llama a sí misma varias veces hasta que se alcanza el caso base, momento en el que se devuelve un valor y la recursión se detiene.

Por ejemplo, una función recursiva para calcular el factorial de un número podría tener la siguiente estructura:

```pseudocode
funcion factorial(n):
  si n == 0:
    devuelve 1
  sino:
    devuelve n * factorial(n-1)
```

En este caso, el caso base es cuando n es igual a cero, momento en el que se devuelve 1. El caso recursivo es n * factorial(n-1), donde se llama a la función factorial con un valor ligeramente menor en cada llamada hasta que se alcanza el caso base.


# Bibliografía

"Structured Programming" (Dahl, Dijkstra y Hoare, 1972). Este libro fue uno de los primeros en proponer la idea de dividir los programas en módulos o funciones independientes.

"The Art of Computer Programming" (Donald Knuth, 1968-). Aunque este libro no se centra específicamente en la programación modular, proporciona muchos de los fundamentos de diseño y organización de programas que la hacen posible.

"The Pragmatic Programmer: Your Journey to Mastery" (Hunt y Thomas, 1999). Este libro incluye una discusión sobre la importancia de la programación modular y ofrece consejos sobre cómo implementarla en la práctica.

"Clean Code: A Handbook of Agile Software Craftsmanship" (Robert C. Martin, 2008). Este libro ofrece consejos sobre cómo escribir código que sea fácil de leer y mantener, incluyendo el uso de la programación modular.

"Code Complete: A Practical Handbook of Software Construction" (Steve McConnell, 2004). Este libro ofrece una cobertura detallada de muchos aspectos de la programación, incluyendo la programación modular.