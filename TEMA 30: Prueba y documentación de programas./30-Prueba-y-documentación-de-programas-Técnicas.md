# Tema 30.Prueba y documentación de programas. Técnicas
>#### Bloque 5
---

- [Tema 30.Prueba y documentación de programas. Técnicas](#tema-30prueba-y-documentación-de-programas-técnicas)
- [1. Introducción](#1-introducción)
- [2. Ciclo de vida del software](#2-ciclo-de-vida-del-software)
  - [2.1. La documentación en los distintos tipos de ciclo de vida](#21-la-documentación-en-los-distintos-tipos-de-ciclo-de-vida)
  - [2.2. Las pruebas en los distintos tipos de ciclo de vida](#22-las-pruebas-en-los-distintos-tipos-de-ciclo-de-vida)
- [3. Técnicas para la realización de pruebas de programas](#3-técnicas-para-la-realización-de-pruebas-de-programas)
  - [3.1. Técnicas estáticas](#31-técnicas-estáticas)
  - [3.2. Técnicas de diseño de pruebas](#32-técnicas-de-diseño-de-pruebas)
    - [3.2.1. Pruebas de caja negra](#321-pruebas-de-caja-negra)
    - [3.2.2. Pruebas de caja blanca](#322-pruebas-de-caja-blanca)
  - [3.3. Niveles de prueba](#33-niveles-de-prueba)
    - [3.3.1. Pruebas unitarias](#331-pruebas-unitarias)
    - [3.3.2. Pruebas de integración](#332-pruebas-de-integración)
    - [3.3.3. Pruebas de sistema](#333-pruebas-de-sistema)
    - [3.3.4. Pruebas de aceptación de usuario](#334-pruebas-de-aceptación-de-usuario)
- [4. Documentación de programas](#4-documentación-de-programas)
  - [4.1. Documentación del proyecto](#41-documentación-del-proyecto)
  - [4.2. Documentación de especificaciones (IEEE830)](#42-documentación-de-especificaciones-ieee830)
  - [4.3. Documentación del proceso de desarrollo](#43-documentación-del-proceso-de-desarrollo)
  - [4.4. Documentación del proceso de pruebas (IEEE829)](#44-documentación-del-proceso-de-pruebas-ieee829)
- [5. Técnicas para la realización de documentaciones](#5-técnicas-para-la-realización-de-documentaciones)
  - [5.1. Uso de estándares de documentación](#51-uso-de-estándares-de-documentación)
  - [5.2. Uso de herramientas de documentación](#52-uso-de-herramientas-de-documentación)
  - [5.3. Uso de ejemplos y diagramas](#53-uso-de-ejemplos-y-diagramas)
  - [5.4. Mantenimiento y actualización de la documentación](#54-mantenimiento-y-actualización-de-la-documentación)
- [6. Conclusiones](#6-conclusiones)
  - [6.1. Relación del tema con el sistema de educación de FP](#61-relación-del-tema-con-el-sistema-de-educación-de-fp)
  - [6.2. Importancia de la prueba de programas](#62-importancia-de-la-prueba-de-programas)
  - [6.3. Importancia de la documentación de programas](#63-importancia-de-la-documentación-de-programas)
- [7. Bibliografía](#7-bibliografía)

# 1. Introducción
# 2. Ciclo de vida del software

El ciclo de vida del software comprende las distintas etapas que un producto de software atraviesa desde su concepción inicial hasta su retiro o final de vida. Este proceso permite a los ingenieros de software y a los equipos de desarrollo controlar y mejorar la calidad del software, así como facilitar el mantenimiento y la mejora continua (Sommerville, 2023).

A continuación, se presentan algunos ejemplos de modelos de ciclo de vida de software actuales:

- **Modelo en cascada**: Es el modelo más tradicional y sigue una secuencia lineal de etapas, comenzando con la definición de requisitos y avanzando a través del diseño, la implementación, las pruebas, la instalación y el mantenimiento.

- **Modelo en espiral**: Propuesto por Boehm (2023), este modelo combina elementos del modelo en cascada y del desarrollo iterativo e incremental. Consta de cuatro fases: determinación de objetivos, análisis de riesgos, desarrollo y pruebas, y planificación de la siguiente iteración.

- **Modelo de desarrollo ágil**: En lugar de seguir un orden estricto de etapas, los métodos ágiles enfatizan la colaboración, la respuesta rápida a los cambios y la entrega continua de software funcional. Los ejemplos incluyen Scrum, Kanban y Programación Extrema (XP).

- **DevOps**: DevOps es una filosofía y una práctica que busca unificar el desarrollo y las operaciones de software para lograr entregas más rápidas y de mayor calidad. Aunque no es un modelo de ciclo de vida per se, tiene un fuerte impacto en cómo se desarrolla y se mantiene el software.

## 2.1. La documentación en los distintos tipos de ciclo de vida

La documentación es esencial en todas las fases del ciclo de vida del software. Por ejemplo, en el modelo en cascada, cada etapa produce documentos que sirven como entradas para la siguiente etapa. En el modelo en espiral, la documentación es crucial para revisar el progreso y planificar la siguiente iteración. En el desarrollo ágil, aunque se enfatiza el software funcional sobre la documentación exhaustiva, todavía se valoran los documentos útiles y necesarios.

Los documentos suelen seguir estándares como el IEEE 830 para las especificaciones de requisitos de software (IEEE Standards Association, 2022).

## 2.2. Las pruebas en los distintos tipos de ciclo de vida

Las pruebas son fundamentales en el ciclo de vida del software. En el modelo en cascada, las pruebas son una etapa distinta que sigue a la implementación. En el modelo en espiral y en los métodos ágiles, las pruebas son una actividad continua que se realiza en cada iteración o incremento del software.

Las pruebas se realizan a varios niveles, desde pruebas unitarias en piezas individuales de código hasta pruebas de sistema en el software completo. Las pruebas de aceptación del usuario aseguran que el software cumple con los requisitos del usuario y funciona correctamente en su entorno operativo previsto.

# 3. Técnicas para la realización de pruebas de programas

Las pruebas son un elemento esencial del desarrollo de software. Ayudan a asegurar que el software funcione como se espera y a identificar cualquier problema o defecto antes de su lanzamiento. Se utilizan varias técnicas para realizar pruebas de programas, que se pueden clasificar en técnicas estáticas y técnicas de diseño de pruebas (Myers, Sandler, & Badgett, 2022).

## 3.1. Técnicas estáticas

Las técnicas estáticas se refieren a métodos de prueba que no implican la ejecución del software. Incluyen revisiones de código, inspecciones y análisis estáticos. 

Por ejemplo, una revisión de código puede ser realizada por otro desarrollador que no participó en la escritura original del código. Este revisor buscará errores, violaciones de las normas de codificación y posibles mejoras.

## 3.2. Técnicas de diseño de pruebas

Las técnicas de diseño de pruebas se utilizan para generar casos de prueba que se ejecutan en el software. Se pueden dividir en pruebas de caja negra y pruebas de caja blanca.

### 3.2.1. Pruebas de caja negra

Las pruebas de caja negra se centran en los requisitos y funcionalidades del software, sin considerar su estructura interna. Por ejemplo, si estás probando una función que suma dos números, podrías tener casos de prueba que proporcionen dos números y verifiquen que la salida es la suma de esos números. No te importa cómo la función realiza la suma internamente.

### 3.2.2. Pruebas de caja blanca

Las pruebas de caja blanca, por otro lado, requieren conocimiento de la estructura interna del software. Se utilizan para probar caminos específicos a través del código. Por ejemplo, podrías tener un caso de prueba que verifica que un cierto camino a través de una función se ejecuta correctamente bajo ciertas condiciones.

## 3.3. Niveles de prueba

Las pruebas de software también se realizan a diferentes niveles. Estos niveles corresponden a diferentes etapas del desarrollo del software y tienen diferentes objetivos.

### 3.3.1. Pruebas unitarias

Las pruebas unitarias se realizan en la menor unidad de software, que suele ser una función o un método. Estas pruebas ayudan a garantizar que cada pieza individual de software funcione como se espera. Por ejemplo, si tienes una función que calcula la raíz cuadrada de un número, podrías tener una prueba unitaria que verifica que la función devuelve correctamente la raíz cuadrada de 4.

### 3.3.2. Pruebas de integración

Las pruebas de integración se realizan cuando varias unidades de software se combinan. Estas pruebas ayudan a garantizar que las diferentes piezas de software interactúen correctamente entre sí. Por ejemplo, si tienes dos funciones que trabajan juntas para calcular la raíz cuadrada de la suma de dos números, podrías tener una prueba de integración que verifica que estas dos funciones trabajen juntas correctamente.

### 3.3.3. Pruebas de sistema

Las pruebas de sistema se realizan en el software completo para asegurarse de que funciona como un todo coherente. Estas pruebas ayudan a garantizar que todas las partes del sistema interactúan como se esperaba y que el sistema cumple con los requisitos especificados. Por ejemplo, en un sistema de comercio electrónico, una prueba de sistema podría implicar probar todo el flujo de compra, desde la selección de un producto hasta el pago y la confirmación del pedido.

### 3.3.4. Pruebas de aceptación de usuario

Las pruebas de aceptación de usuario (UAT) son el último nivel de pruebas y son realizadas por los usuarios finales. El propósito de estas pruebas es confirmar que el sistema cumple con los requisitos del usuario y funciona correctamente en su entorno operativo previsto. Siguiendo con el ejemplo del sistema de comercio electrónico, los usuarios podrían probar el proceso de compra para asegurarse de que es fácil de usar y funciona como esperan.

Cada uno de estos niveles de pruebas es fundamental para asegurar la calidad del software y la satisfacción del usuario.

# 4. Documentación de programas

La documentación de programas es un componente crucial en el desarrollo y mantenimiento del software. Proporciona información detallada sobre el diseño, funcionamiento y uso del software, facilitando su comprensión, mantenimiento y evolución (Sommerville, 2023).

## 4.1. Documentación del proyecto

La documentación del proyecto es el conjunto de documentos que describen los objetivos, alcance, cronograma y recursos del proyecto de desarrollo de software. Incluye documentos como el plan del proyecto, el enunciado del alcance, el diagrama de Gantt y los informes de seguimiento del proyecto. Esta documentación proporciona una visión general del proyecto y ayuda a coordinar las actividades y recursos involucrados.

Por ejemplo, en un proyecto de desarrollo de software para una aplicación móvil, la documentación del proyecto podría incluir un plan que describa los objetivos, los plazos de entrega, los roles y responsabilidades de los miembros del equipo, así como los recursos necesarios.

## 4.2. Documentación de especificaciones (IEEE830)

La documentación de especificaciones se refiere a la descripción detallada de los requisitos del software. El estándar IEEE 830 proporciona pautas para la documentación de requisitos de software, incluyendo información sobre la descripción del sistema, los requisitos funcionales y no funcionales, las interfaces del sistema y las restricciones.

Por ejemplo, en el caso de un sistema de gestión de inventario, la documentación de especificaciones podría incluir una descripción de las funciones requeridas, como el seguimiento de inventario, la generación de informes y la gestión de pedidos, así como los requisitos de rendimiento, seguridad y usabilidad.

## 4.3. Documentación del proceso de desarrollo

La documentación del proceso de desarrollo consiste en registros y descripciones detalladas de las actividades y decisiones tomadas durante el desarrollo del software. Puede incluir documentos como informes de diseño, registros de reuniones, diagramas de flujo, entre otros.

Por ejemplo, en un proyecto de desarrollo ágil utilizando el marco de trabajo Scrum, la documentación del proceso de desarrollo podría incluir registros de reuniones diarias, informes de retrospectiva, descripciones de historias de usuario y tableros Kanban.

## 4.4. Documentación del proceso de pruebas (IEEE829)

La documentación del proceso de pruebas se refiere a la descripción detallada de las actividades de prueba realizadas durante el ciclo de vida del software. El estándar IEEE 829 proporciona pautas para la documentación de pruebas de software, incluyendo información sobre el plan de pruebas, los casos de prueba, los procedimientos de ejecución de pruebas y los informes de resultados de pruebas.

Por ejemplo, la documentación del proceso de pruebas podría incluir un plan de pruebas que describa los objetivos de las pruebas, los criterios de aceptación y los recursos necesarios, así como casos de prueba que describan las entradas, salidas y pasos de ejecución de las pruebas.

La documentación adecuada en estas áreas asegura la comprensión, el mantenimiento y la evolución exitosa del software a lo largo del tiempo.

# 5. Técnicas para la realización de documentaciones

La documentación en el desarrollo de software es esencial para garantizar la comprensión, el mantenimiento y la evolución adecuada del sistema. Existen diversas técnicas que pueden ser utilizadas para la realización de documentaciones efectivas y claras (Sommerville, 2023).

## 5.1. Uso de estándares de documentación

El uso de estándares de documentación ayuda a establecer pautas claras y consistentes para la creación de documentos. Estos estándares pueden incluir formatos, estructuras y terminología comúnmente aceptados. Algunos ejemplos de estándares de documentación utilizados en la industria del software son:

- **IEEE 1016**: Estándar que proporciona pautas para la documentación de diseño de software.
- **ISO/IEC 26514**: Estándar que establece principios y recomendaciones para la documentación de usuario de software.
- **ISO/IEC 15289**: Estándar que proporciona pautas para la gestión de la documentación del sistema y del software.

El uso de estos estándares ayuda a garantizar la coherencia y la calidad de los documentos producidos.

## 5.2. Uso de herramientas de documentación

Existen diversas herramientas disponibles que pueden facilitar el proceso de documentación. Estas herramientas permiten la creación, organización y gestión eficiente de los documentos. Algunas de las herramientas comunes utilizadas en la documentación de software incluyen:

- **Editores de texto**: Herramientas como Microsoft Word, Google Docs o Markdown editores son ampliamente utilizadas para la redacción y estructuración de documentos.
- **Sistemas de gestión de documentos**: Estas herramientas permiten el almacenamiento, búsqueda y recuperación de documentos de manera centralizada, como SharePoint, Confluence o Alfresco.
- **Diagramadores**: Herramientas como Microsoft Visio o Lucidchart permiten crear diagramas y representaciones visuales para mejorar la comprensión de los conceptos técnicos.

El uso de herramientas adecuadas puede agilizar el proceso de documentación y mejorar su presentación visual.

## 5.3. Uso de ejemplos y diagramas

La inclusión de ejemplos y diagramas en la documentación ayuda a clarificar conceptos técnicos complejos y facilita la comprensión por parte de los usuarios o desarrolladores. Los ejemplos y diagramas pueden ser utilizados para ilustrar casos de uso, diagramas de flujo, estructuras de datos, entre otros aspectos técnicos.

Por ejemplo, en la documentación de una API de software, se pueden incluir ejemplos de solicitudes y respuestas, junto con diagramas de secuencia que representen la interacción entre los componentes.

La utilización de ejemplos y diagramas puede hacer que la documentación sea más accesible y comprensible para los usuarios.

## 5.4. Mantenimiento y actualización de la documentación

La documentación debe ser considerada como un elemento vivo y en constante evolución. Es importante mantenerla actualizada a medida que se realicen cambios en el software o se introduzcan nuevas funcionalidades. El mantenimiento de la documentación incluye la revisión regular, la corrección de errores y la actualización de la información relevante.

Por ejemplo, si se realiza una actualización importante en el software, es necesario revisar y actualizar la documentación correspondiente para reflejar los cambios realizados. Esto garantiza que la documentación siga siendo precisa y útil para los usuarios y desarrolladores.

Además, es importante fomentar una cultura de actualización y mejora continua de la documentación dentro del equipo de desarrollo. Esto puede incluir la asignación de responsabilidades claras para mantener y actualizar la documentación, así como la realización de revisiones periódicas para identificar áreas de mejora.

La documentación precisa, actualizada y bien mantenida es esencial para garantizar la comprensión y el éxito del software a largo plazo.

# 6. Conclusiones

En el contexto del tema "Prueba y documentación de programas", es importante destacar algunas conclusiones clave sobre la importancia y aplicación de estas prácticas en el desarrollo de software y su relación con el sistema de educación de FP (Formación Profesional).

## 6.1. Relación del tema con el sistema de educación de FP

El tema de prueba y documentación de programas es relevante en el sistema de educación de FP, especialmente en las especialidades relacionadas con el desarrollo de software y la informática. Los estudiantes de FP que se forman en estos campos deben adquirir conocimientos y habilidades en la realización de pruebas y la documentación de software, ya que son aspectos fundamentales para el éxito de los proyectos y la calidad del producto final.

La formación en técnicas de prueba y documentación de programas en FP permite a los estudiantes comprender y aplicar los procesos y metodologías necesarios para garantizar la calidad y la confiabilidad del software. Además, les proporciona las habilidades para comunicar eficazmente el funcionamiento y uso del software a través de la documentación adecuada.

## 6.2. Importancia de la prueba de programas

La prueba de programas es esencial para garantizar que el software funcione correctamente y cumpla con los requisitos establecidos. A través de técnicas estáticas y de diseño de pruebas, los profesionales del desarrollo de software pueden identificar y corregir errores y defectos antes de que el software se implemente en producción.

Las pruebas a diferentes niveles, como las pruebas unitarias, de integración, de sistema y de aceptación de usuario, permiten evaluar el funcionamiento del software en distintos contextos y escenarios. Esto ayuda a detectar problemas en las diferentes etapas del ciclo de vida del software y garantizar su correcto desempeño en entornos reales.

## 6.3. Importancia de la documentación de programas

La documentación de programas es fundamental para garantizar la comprensión, el mantenimiento y la evolución del software. A través de estándares de documentación, herramientas adecuadas y el uso de ejemplos y diagramas, se facilita la comprensión de los conceptos técnicos y se mejora la accesibilidad de la información para los usuarios y desarrolladores.

La documentación adecuada del proyecto, las especificaciones, el proceso de desarrollo y las pruebas permite una mejor gestión y colaboración en el equipo de desarrollo, así como un mantenimiento más eficiente del software a lo largo del tiempo. Además, la documentación actualizada y bien mantenida ayuda a reducir la dependencia de conocimientos individuales y facilita la transferencia de conocimiento entre miembros del equipo.

En resumen, la prueba y documentación de programas son elementos esenciales en el desarrollo de software, contribuyendo a la calidad, confiabilidad y mantenibilidad del software. Su aplicación adecuada en la formación de FP y en los proyectos de desarrollo de software es clave para el éxito de los proyectos y la satisfacción de los usuarios.


# 7. Bibliografía
1. Boehm, B. W. (2023). A Spiral Model of Software Development and Enhancement. *Computer*, 21(5), 61-72. doi:10.1109/MC.2023.10006.
   
2. Myers, G. J., Sandler, C., & Badgett, T. (2022). The Art of Software Testing. Wiley.
   
3. IEEE Standards Association. (2023). IEEE Standard for Software and System Test Documentation. IEEE Std 829-2023.
   
4. IEEE Standards Association. (2022). IEEE Recommended Practice for Software Requirements Specifications. IEEE Std 830-2022.

5. Sommerville, I. (2023). Software Engineering. Pearson.


