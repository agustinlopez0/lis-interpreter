# 🚀 Intérprete LIS

Un intérprete completo para el lenguaje de programación **LIS** (Lenguaje Imperativo Simple), implementado en Haskell. Este proyecto incluye un parser, múltiples estrategias de evaluación y un sistema de pruebas.

## 📋 Descripción

LIS es un lenguaje de programación imperativo simple diseñado para la enseñanza de conceptos fundamentales de lenguajes de programación. Este intérprete permite ejecutar programas escritos en LIS, que incluyen:

- **Expresiones aritméticas**: suma, resta, multiplicación, división
- **Expresiones booleanas**: operadores lógicos y comparaciones
- **Variables enteras**: asignación y manipulación de variables
- **Estructuras de control**: condicionales (`if-then-else`) y bucles (`repeat-until`)
- **Operaciones especiales**: incremento de variables (`++`)

## ✨ Características

- 🔍 **Parser completo** para el lenguaje LIS
- ⚡ **Múltiples estrategias de evaluación** (Eval1, Eval2, Eval3)
- 🎨 **Pretty Printer** para visualización legible de programas
- 🧪 **Sistema de pruebas** con HUnit
- 📦 **Gestión de dependencias** con Stack
- 🛡️ **Type-safe** gracias a GADTs de Haskell

## 🛠️ Tecnologías

- **Haskell** - Lenguaje de programación funcional
- **Stack** - Herramienta de gestión de proyectos
- **Parsec** - Biblioteca de parsing
- **GADTs** - Tipos de datos algebraicos generalizados
- **HUnit** - Framework de testing

## 📦 Requisitos

- [Stack](https://docs.haskellstack.org/) (versión reciente)
- GHC (se instala automáticamente con Stack)

## 🚀 Instalación

1. Clona el repositorio:
```bash
git clone <url-del-repositorio>
cd TP-ALP
```

2. Configura el entorno (solo la primera vez):
```bash
stack setup
```

3. Compila el proyecto:
```bash
stack build
```

## 💻 Uso

### Ejecutar un programa LIS

```bash
stack exec TP1-exe -- ejemplos/sqrt.lis
```

### Opciones disponibles

- `-p`: Imprime el programa de entrada de forma legible
- `-a`: Muestra el AST (Abstract Syntax Tree) del programa
- `-e N`: Selecciona el evaluador (1, 2 o 3). Por defecto usa el evaluador 1
- `-h`: Muestra la ayuda

### Ejemplos

Imprimir un programa de forma legible:
```bash
stack exec TP1-exe -- ejemplos/sqrt.lis -p
```

Ejecutar con un evaluador específico:
```bash
stack exec TP1-exe -- ejemplos/sqrt.lis -e 2
```

Ver el AST de un programa:
```bash
stack exec TP1-exe -- ejemplos/sqrt.lis -a
```

### Usar GHCi para desarrollo

Para probar funciones en el intérprete interactivo:
```bash
stack ghci
```

### Ejecutar tests

```bash
stack test
```

## 📁 Estructura del Proyecto

```
.
├── app/
│   └── Main.hs              # Punto de entrada del ejecutable
├── src/
│   ├── AST.hs               # Definición del árbol de sintaxis abstracta
│   ├── Parser.hs            # Parser del lenguaje LIS
│   ├── Eval1.hs             # Evaluador 1
│   ├── Eval2.hs             # Evaluador 2
│   ├── Eval3.hs             # Evaluador 3
│   └── PPLis.hs             # Pretty Printer
├── ejemplos/                # Programas de ejemplo en LIS
│   ├── sqrt.lis
│   ├── div.lis
│   └── ...
├── tests/                   # Casos de prueba
└── INSTRUCCIONES.md         # Guía técnica detallada
```

## 📝 Ejemplo de Programa LIS

```lis
n = 25;
i = -1;
a = 0;
g = 0;
repeat {
    i = i + 1; 
    t = i * i;
    g = a++
} until t > n || t == n
```

## 📚 Documentación

Para más detalles técnicos sobre la implementación, configuración y uso avanzado, consulta el archivo [INSTRUCCIONES.md](INSTRUCCIONES.md).

## 📄 Licencia

Este proyecto está bajo la licencia BSD-3-Clause. Ver el archivo [LICENSE](LICENSE) para más detalles.

## 👥 Contribuciones

Este es un proyecto académico. Las contribuciones son bienvenidas, pero por favor asegúrate de mantener la estructura y convenciones del código existente.

---

⭐ Si este proyecto te resultó útil, ¡no olvides darle una estrella!
