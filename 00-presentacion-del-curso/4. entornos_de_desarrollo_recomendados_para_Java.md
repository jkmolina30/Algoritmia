## 7. Entornos de Desarrollo Recomendados para Java
Para programar en Java se necesita un entorno donde el estudiante pueda escribir, organizar, compilar y ejecutar sus programas. En este curso se proponen tres opciones principales:

1. NetBeans.
2. Eclipse.
3. Visual Studio Code.

Aunque las tres herramientas permiten trabajar con Java, se recomienda iniciar preferiblemente con **NetBeans**, porque ofrece un entorno completo para programar sin depender de ayudas automáticas avanzadas o herramientas de inteligencia artificial integradas.

La intención pedagógica es que el estudiante fortalezca su capacidad de análisis, lea los errores, piense la solución y comprenda la lógica del programa antes de apoyarse en asistentes automáticos.

---

## 7.1. NetBeans

### ¿Qué es NetBeans?
NetBeans es un entorno de desarrollo integrado, también conocido como **IDE**. Un **IDE** es un programa que reúne varias herramientas necesarias para programar:

* Editor de código.
* Compilador.
* Ejecutor de programas.
* Organización de proyectos.
* Detección de errores.
* Consola de salida.

En palabras sencillas, NetBeans es una herramienta que permite escribir y ejecutar programas Java de manera organizada.

---

### ¿Por qué se recomienda NetBeans en este curso?
NetBeans se recomienda como primera opción porque permite trabajar Java de forma clara y estructurada. Además, al no tener integrada una inteligencia artificial de forma directa como parte central del entorno, el estudiante se ve obligado a:

* Leer el enunciado con más atención.
* Pensar la solución antes de escribir código.
* Analizar los errores del programa.
* Corregir problemas de sintaxis.
* Comprender la estructura de una clase Java.
* Desarrollar autonomía en la solución de problemas.
* Fortalecer la lógica de programación.

Esto es importante porque en un curso inicial de algoritmia el objetivo no es que el estudiante obtenga una respuesta automática, sino que aprenda a construirla.

---

### Descarga de NetBeans

Para descargar NetBeans se puede ingresar al sitio oficial:

```text
https://netbeans.apache.org/
```

Se recomienda descargar una versión reciente de Apache NetBeans.

---

### Instalación de NetBeans
Pasos generales:

1. Ingresar a la página oficial de NetBeans.
2. Descargar el instalador correspondiente al sistema operativo.
3. Verificar que el JDK esté instalado previamente.
4. Ejecutar el instalador.
5. Seguir los pasos del asistente de instalación.
6. Abrir NetBeans.
7. Crear un nuevo proyecto Java.

---

### Crear un primer proyecto en NetBeans
Para crear un proyecto básico:

1. Abrir NetBeans.
2. Ir a `File`.
3. Seleccionar `New Project`.
4. Elegir la categoría `Java with Ant` o `Java`.
5. Seleccionar `Java Application`.
6. Escribir el nombre del proyecto.

Ejemplo:

```text
PrimerProgramaJava
```

7. Finalizar la creación del proyecto.
8. Escribir el código dentro del método `main`.

---

### Primer programa en NetBeans

```java
public class PrimerProgramaJava {
    public static void main(String[] args) {
        System.out.println("Hola, bienvenido al curso de Algoritmia y Programación");
    }
}
```

---

### Explicación del programa

```java
public class PrimerProgramaJava
```

Define una clase llamada `PrimerProgramaJava`.

En Java, el código se organiza principalmente dentro de clases.

---

```java
public static void main(String[] args)
```

Es el método principal del programa.

Cuando se ejecuta un programa Java, la ejecución inicia en el método `main`.

---

```java
System.out.println()
```

Permite mostrar un mensaje en pantalla.

---

## 7.2. Eclipse

### ¿Qué es Eclipse?
Eclipse es otro entorno de desarrollo integrado utilizado ampliamente para programar en Java. Es una herramienta profesional que permite crear proyectos, organizar paquetes, ejecutar programas y trabajar con diferentes tecnologías.

---

### ¿Cuándo usar Eclipse?
Eclipse puede ser una buena opción para estudiantes que quieran conocer otro entorno usado en contextos académicos y profesionales. Se recomienda especialmente cuando el estudiante ya comprende lo básico de Java y quiere explorar una herramienta más flexible.

---

### Ventajas de Eclipse

* Permite crear proyectos Java organizados.
* Es ampliamente usado en entornos académicos y empresariales.
* Tiene muchas extensiones.
* Permite trabajar con diferentes lenguajes y tecnologías.
* Ayuda a identificar errores de sintaxis.

---

### Descarga de Eclipse

Sitio oficial:

```text
https://www.eclipse.org/downloads/
```

Se recomienda descargar la opción:

```text
Eclipse IDE for Java Developers
```

---

### Instalación de Eclipse

Pasos generales:

1. Ingresar a la página oficial de Eclipse.
2. Descargar el instalador.
3. Seleccionar `Eclipse IDE for Java Developers`.
4. Verificar que Java JDK esté instalado.
5. Instalar Eclipse.
6. Abrir Eclipse.
7. Seleccionar una carpeta de trabajo o `workspace`.

---

### ¿Qué es el workspace?
El **workspace** es la carpeta donde Eclipse guarda los proyectos. En palabras sencillas, es el espacio de trabajo donde estarán almacenados los ejercicios del curso.

Ejemplo de carpeta:

```text
Documentos/AlgoritmiaJava
```

---

### Crear un proyecto en Eclipse

1. Abrir Eclipse.
2. Ir a `File`.
3. Seleccionar `New`.
4. Seleccionar `Java Project`.
5. Escribir el nombre del proyecto.

Ejemplo:

```text
EjerciciosCondicionales
```

6. Crear una clase.
7. Marcar la opción para crear el método `main`.
8. Escribir el código.
9. Ejecutar el programa.

---

## 7.3. Visual Studio Code

### ¿Qué es Visual Studio Code?
Visual Studio Code, también llamado VS Code, es un editor de código liviano y flexible. A diferencia de NetBeans o Eclipse, VS Code no viene preparado únicamente para Java. Para trabajar con Java se deben instalar algunas extensiones.

---

### ¿Cuándo usar Visual Studio Code?
Visual Studio Code puede ser una buena opción cuando el estudiante quiere trabajar con varios lenguajes de programación en una sola herramienta. También es útil para trabajar con Git, GitHub y archivos Markdown, como los archivos `.md` usados en este repositorio.

---

### Ventajas de Visual Studio Code

* Es liviano.
* Es rápido.
* Permite trabajar con muchos lenguajes.
* Tiene buena integración con Git.
* Permite editar archivos Markdown.
* Es muy utilizado en desarrollo de software.
* Tiene muchas extensiones.

---

### Precaución pedagógica sobre Visual Studio Code
Visual Studio Code puede integrarse fácilmente con herramientas de inteligencia artificial y asistentes de código. En este curso, si se utiliza VS Code, se recomienda hacerlo con responsabilidad. El estudiante debe evitar depender de respuestas automáticas y debe concentrarse en comprender la lógica de cada solución.

La regla principal es:

```text
Si no puedes explicar el código, todavía no lo has aprendido.
```

---

### Descarga de Visual Studio Code

Sitio oficial:

```text
https://code.visualstudio.com/
```

---

### Extensiones recomendadas para Java
Después de instalar VS Code, se recomienda instalar las siguientes extensiones:

* Extension Pack for Java.
* Code Runner.
* Markdown All in One.
* GitLens.

---

### ¿Para qué sirve cada extensión?

| Extensión               | Uso                                                   |
| ----------------------- | ----------------------------------------------------- |
| Extension Pack for Java | Permite escribir, compilar y ejecutar programas Java  |
| Code Runner             | Permite ejecutar código de manera rápida              |
| Markdown All in One     | Ayuda a escribir archivos Markdown para GitHub        |
| GitLens                 | Mejora la visualización de cambios realizados con Git |

---

### Crear un archivo Java en Visual Studio Code

1. Abrir Visual Studio Code.
2. Crear una carpeta para el curso.
3. Abrir la carpeta desde VS Code.
4. Crear un archivo llamado:

```text
HolaMundo.java
```

5. Escribir el siguiente código:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola desde Visual Studio Code");
    }
}
```

6. Ejecutar el programa.

---

## 7.4. Comparación de Herramientas

| Herramienta        | Nivel recomendado    | Ventaja principal                                 | Recomendación pedagógica                      |
| ------------------ | -------------------- | ------------------------------------------------- | --------------------------------------------- |
| NetBeans           | Inicial              | Entorno completo y organizado para Java           | Recomendado como primera opción del curso     |
| Eclipse            | Inicial - Intermedio | Muy usado en contextos académicos y profesionales | Buena alternativa para conocer otro IDE       |
| Visual Studio Code | Intermedio           | Flexible, liviano e integrado con Git             | Usar con responsabilidad y sin depender de IA |

---

## 7.5. Recomendación del Curso
Para este curso se recomienda el siguiente orden:

### Primera opción: NetBeans
Se recomienda para iniciar porque permite trabajar Java de forma ordenada y favorece que el estudiante piense la solución, lea errores y comprenda la estructura del programa.

### Segunda opción: Eclipse
Es una alternativa completa para trabajar Java y familiarizarse con un entorno usado en escenarios profesionales.

### Tercera opción: Visual Studio Code
Es una herramienta muy útil, especialmente para trabajar con GitHub y archivos Markdown, pero debe usarse con responsabilidad para no depender de herramientas automáticas.

---

## 7.6. Recomendación final sobre el uso de herramientas
La herramienta no reemplaza el pensamiento lógico. Un buen programador no se forma únicamente por usar un editor avanzado, sino por desarrollar la capacidad de analizar, diseñar, probar y corregir soluciones.

Por eso, en este curso las herramientas se usarán como apoyo, pero el aprendizaje principal estará en la construcción de la lógica algorítmica.
