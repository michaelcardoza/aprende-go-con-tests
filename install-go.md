# Instalar Go y configurar el entorno para ser productivo

Las instrucciones oficiales para instalar Go están disponibles [aquí](https://golang.org/doc/install).

## Entorno de Go

### Módulos de Go

Go 1.11 introdujo los [Módulos](https://go.dev/wiki/Modules). Este enfoque es el modo de construcción predeterminado desde Go 1.16, por lo tanto, no se recomienda el uso de `GOPATH`.

Los módulos buscan resolver problemas relacionados con la gestión de dependencias, selección de versiones y compilaciones reproducibles; además permiten a los usuarios ejecutar código Go fuera de `GOPATH`.

Usar módulos es bastante sencillo. Selecciona cualquier directorio fuera de `GOPATH` como raíz de tu proyecto y crea un nuevo módulo con el comando `go mod init`.

Se generará un archivo `go.mod`, que contiene la ruta del módulo, la versión de Go y los requisitos de dependencias, que son los otros módulos necesarios para una compilación exitosa.

Si no se especifica un `<modulepath>`, `go mod init` intentará adivinar la ruta del módulo a partir de la estructura del directorio. También se puede sobrescribir proporcionando un argumento.

```sh
mkdir my-project
cd my-project
go mod init <modulepath>
```

Un archivo `go.mod` puede verse así:

```
module cmd

go 1.16
```

La documentación incorporada proporciona una visión general de todos los comandos disponibles de `go mod`.

```sh
go help mod
```

```sh
go help mod init
```

## Linter de Go

Se puede configurar una mejora sobre el linter predeterminado usando [GolangCI-Lint](https://golangci-lint.run).

Puede instalarse con:

```sh
brew install golangci-lint
```

## Refactorización y tus herramientas

Este libro hace mucho énfasis en la importancia de la refactorización.

Tus herramientas pueden ayudarte a hacer refactorizaciones más grandes con confianza.

Debes estar lo suficientemente familiarizado con tu editor para realizar lo siguiente con una simple combinación de teclas:

- **Extraer/Inline de variables**. Dar nombre a valores mágicos te permite simplificar tu código rápidamente.
- **Extraer método/función**. Es vital poder tomar una sección de código y extraer funciones o métodos.
- **Renombrar**. Debes poder renombrar símbolos a través de varios archivos con confianza.
- **go fmt**. Go tiene un formateador con opiniones llamado go fmt. Tu editor debe ejecutarlo al guardar cada archivo.
- **Ejecutar pruebas**. Debes poder hacer cualquiera de las acciones anteriores y luego ejecutar rápidamente tus pruebas para asegurarte de que tu refactorización no haya roto nada.

Además, para ayudarte a trabajar con tu código, deberías poder:

- **Ver la firma de una función**. Nunca deberías tener dudas sobre cómo llamar a una función en Go. Tu IDE debería describir una función con su documentación, sus parámetros y lo que devuelve.
- **Ver la definición de una función**. Si aún no está claro qué hace una función, deberías poder ir al código fuente e investigarlo tú mismo.
- **Encontrar usos de un símbolo**. Entender el contexto de una función puede ayudarte a tomar decisiones al refactorizar.

Dominar tus herramientas te ayudará a concentrarte en el código y reducir el cambio de contexto.

## Conclusión

A este punto, deberías tener Go instalado, un editor disponible y algunas herramientas básicas configuradas. Go tiene un ecosistema muy amplio de productos de terceros. Aquí hemos identificado algunos componentes útiles. Para una lista más completa, visita [https://awesome-go.com](https://awesome-go.com).
