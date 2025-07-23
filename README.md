# Aprende Go con tests

<p align="center">
  <img src="red-green-blue-gophers-smaller.png" />
</p>

[Art by Denise](https://twitter.com/deniseyu21)

## Formatos

- [Gitbook](https://michaelcardoza.gitbook.io/aprende-go-con-tests)
- [EPUB or PDF](https://github.com/michaelcardoza/learn-go-with-tests/releases)

## Motivación

* Explora Go escribiendo pruebas
* **Obtén una base con TDD**. Go es un buen lenguaje para aprender TDD porque es un lenguaje simple de aprender y el testing está incorporado.
* Serás capaz de comenzar a escribir sistemas robustos y bien probados en Go.
* [Mira un video o lee sobre por qué el unit testing y TDD son importantes.](why.md)

## Índice

### Fundamentos de Go

1. [Instalar Go](install-go.md) - Configura el entorno para ser productivo.
2. [Hola, mundo](hello-world.md) - Declaración de variables, constantes, sentencias if/else, switch, escribe tu primer programa en Go y tu primera prueba. Sintaxis de sub-test y closures.
3. [Enteros](integers.md) - Explora más a fondo la sintaxis de declaración de funciones y aprende nuevas formas de mejorar la documentación de tu código.
4. [Iteración](iteration.md) - Aprende sobre el uso de `for` y cómo hacer benchmarking.
5. [Arrays and slices](arrays-and-slices.md) - Aprende sobre arrays, slices, `len`, varargs, `range` y cobertura de pruebas.
6. [Structs, methods & interfaces](structs-methods-and-interfaces.md) - Aprende sobre `struct`, métodos, `interface` y pruebas con enfoque table-driven.
7. [Pointers & errors](pointers-and-errors.md) - Aprende sobre punteros y manejo de errores.
8. [Maps](maps.md) - Aprende a almacenar valores usando la estructura de datos map.
9. [Inyección de Dependencias](dependency-injection.md) - Aprende sobre inyección de dependencias, su relación con el uso de interfaces y una introducción al paquete I/O.
10. [Mocking](mocking.md) - Toma código existente sin pruebas y usa inyección de dependencias con mocks para probarlo.
11. [Concurrencia](concurrency.md) - Aprende a escribir código concurrente para hacer tu software más rápido.
12. [Select](select.md) - Aprende a sincronizar procesos asíncronos de forma elegante.
13. [Reflection](reflection.md) - Aprende sobre "reflection".
14. [Sync](sync.md) - Aprende algunas funcionalidades del paquete sync, incluyendo `WaitGroup` y `Mutex`.
15. [Context](context.md) - Usa el paquete context para gestionar y cancelar procesos de larga duración.
16. [Introducción a las pruebas basadas en propiedades](roman-numerals.md) - Practica algo de TDD con la kata de Números Romanos y una introducción breve en las pruebas basadas en propiedades.
17. [Maths](math.md) - Usa el paquete `math` para dibujar un reloj en SVG.
18. [Manejo de archivos](reading-files.md) - Lee archivos y procésalos.
19. [Plantillas](html-templates.md) - Usa el paquete html/template de Go para renderizar HTML a partir de datos, y aprende también sobre "approval testing".
20. [Genéricos](generics.md) - Aprende a escribir funciones que aceptan argumentos genéricos y crea tu propia estructura de datos genérica.
21. [Revisando arrays y slices con genéricos](revisiting-arrays-and-slices-with-generics.md) - Los genéricos son muy útiles al trabajar con colecciones. Aprende a escribir tu propia función `Reduce` y mejora algunos patrones comunes.

### Construir una aplicación

Ahora que, con suerte, has asimilado la sección de _Fundamentos de Go_, tienes una base sólida de la mayoría de las características del lenguaje Go y de cómo aplicar TDD.

Esta siguiente sección consistirá en construir una aplicación.

Cada capítulo iterará sobre el anterior, ampliando la funcionalidad de la aplicación según lo indique nuestro "product owner".

Se introducirán nuevos conceptos para facilitar la escritura de buen código, pero la mayoría del nuevo material consistirá en aprender lo que se puede lograr con la biblioteca estándar de Go.

Al final de esta sección, deberías tener un conocimiento sólido de cómo escribir una aplicación en Go de forma iterativa, respaldada por pruebas.

* [HTTP server](http-server.md) - Crearemos una aplicación que escuche solicitudes HTTP y responda a ellas.
* [JSON, routing and embedding](json.md) - Haremos que nuestros endpoints devuelvan JSON y exploraremos cómo hacer routing.
* [I/O and sorting](io.md) - Persistiremos y leeremos nuestros datos desde disco, y cubriremos cómo ordenar datos.
* [Command line & project structure](command-line.md) - Soportar múltiples aplicaciones desde una misma base de código y leer entrada desde la línea de comandos.
* [Time](time.md) - Usar el paquete `time` para programar actividades.
* [WebSockets](websockets.md) - Aprender a escribir y probar un servidor que usa WebSockets.

### Fundamentos de testing

Abordando otros temas relacionados con las pruebas.

* [Introducción a acceptance tests](intro-to-acceptance-tests.md) - Aprende cómo escribir "acceptance tests" para tu código, con un ejemplo del mundo real sobre cómo cerrar un servidor HTTP de forma elegante.
* [Escalamiento de acceptance tests](scaling-acceptance-tests.md) - Aprende técnicas para gestionar la complejidad al escribir "acceptance tests" para sistemas complejos.
* [Trabajando sin mocks, stubs and spies](working-without-mocks.md) - Aprende cómo usar fakes y contracts para crear pruebas más realistas y mantenibles.
* [Guía básica para refactorización](refactoring-checklist.md) - Una discusión sobre qué es el refactoring y algunos consejos básicos sobre cómo hacerlo.
* [OS exec](os-exec.md) - Un ejemplo de cómo podemos interactuar con el sistema operativo para ejecutar comandos y obtener datos, manteniendo nuestra lógica de negocio testeable.
* [Error types](error-types.md) - Ejemplo de cómo crear tus propios tipos de error para mejorar tus pruebas y hacer que tu código sea más fácil de trabajar.
* [Context-aware Reader](context-aware-reader.md) - Aprende cómo aplicar TDD para extender `io.Reader` con soporte para cancelación. Basado en [Context-aware io.Reader for Go](https://pace.dev/blog/2020/02/03/context-aware-ioreader-for-golang-by-mat-ryer)
* [HTTP Handlers](http-handlers-revisited.md) - Probar HTTP handlers parece ser la pesadilla de muchos desarrolladores. Este capítulo explora los problemas en torno al diseño correcto de los handlers.

### Meta / Discusión

* [Por qué realizar pruebas unitarias y cómo hacer que funcionen para usted](why.md) - Mira un video o lee sobre por qué el unit testing y TDD son importantes.
* [Anti-patterns](anti-patterns.md) - Un capítulo breve sobre anti-patrones en TDD y pruebas unitarias.

## Contribuir

* _El proyecto original está en desarrollo._ Si te gustaría contribuir, no dudes en ponerte en contacto.
* Lee [contributing.md](https://github.com/quii/learn-go-with-tests/tree/842f4f24d1f1c20ba3bb23cbc376c7ca6f7ca79a/contributing.md) para conocer las pautas.
* ¿Tienes alguna idea? Crea una issue [aquí](https://github.com/quii/learn-go-with-tests).

## A quién va dirigido

* Personas interesadas en aprender Go.
* Personas que ya conocen algo de Go, pero quieren profundizar en las pruebas utilizando TDD.

## Lo que necesitarás

* ¡Una computadora!
* [Go instalado](https://golang.org/)
* Un editor de texto
* Algo de experiencia en programación. Comprensión de conceptos como `if`, variables, funciones, etc.
* Sentirte cómodo usando la terminal

## Comentarios

* Crea issues o envía PRs [aquí](https://github.com/quii/learn-go-with-tests)
* [Twitter @quii - Autor Original](https://twitter.com/quii)
* [Twitter @Mike_ErrNil - Autor de versión en español](https://twitter.com/Mike_ErrNil)

[Licencia MIT](LICENSE.md)

[El logo es de egonelbre](https://github.com/egonelbre) ¡Una estrella!
