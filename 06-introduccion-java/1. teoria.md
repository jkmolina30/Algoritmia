# Teoría: Introducción al Lenguaje Java

## 1. ¿Qué es Java?

Java es un **lenguaje de programación de alto nivel**, orientado a objetos, fuertemente tipado y multiplataforma.

En palabras sencillas, Java es un lenguaje que permite escribir instrucciones para que un computador realice tareas. Esas instrucciones pueden convertirse en programas de consola, aplicaciones de escritorio, sistemas web, aplicaciones empresariales, servicios backend y otros tipos de software.

---

## 2. ¿Por qué estudiar Java en un curso de algoritmia?

Java es útil en la formación inicial de un ingeniero de sistemas porque obliga al estudiante a trabajar con una estructura clara.

Java ayuda a fortalecer:

- La lógica de programación.
- El uso correcto de tipos de datos.
- La escritura ordenada de instrucciones.
- La comprensión de clases y métodos.
- La disciplina en la sintaxis.
- La transición hacia la programación orientada a objetos.

En pseudocódigo se aprende primero la lógica.  
En Java se aprende a escribir esa lógica en un lenguaje formal.

---

## 3. Origen de Java

Java tuvo su origen en un proyecto desarrollado por Sun Microsystems. Inicialmente el lenguaje se llamó **Oak** y luego fue renombrado como **Java**.

El lenguaje comenzó a desarrollarse alrededor de 1991, inicialmente orientado a dispositivos como tarjetas inteligentes y sintonizadores de televisión. Posteriormente fue presentado públicamente como Java en la década de los noventa.

Uno de los nombres más importantes en su creación es **James Gosling**, reconocido como una de las figuras principales del desarrollo del lenguaje.

---

## 4. La idea principal de Java

Una de las ideas más conocidas asociadas a Java es:

```text
Escríbelo una vez, ejecútalo donde quieras.
```

Esta frase resume la intención de Java de permitir que un programa pueda ejecutarse en diferentes sistemas operativos, siempre que exista una Máquina Virtual de Java instalada.

En términos sencillos:

- Se escribe el programa una vez.
- Se compila.
- Se genera un archivo intermedio.
- Ese archivo puede ejecutarse en diferentes plataformas mediante la JVM.

---

## 5. Java como lenguaje multiplataforma

Un lenguaje o tecnología es **multiplataforma** cuando puede funcionar en diferentes sistemas operativos.

Por ejemplo:

- Windows.
- Linux.
- macOS.

Java logra esto mediante la **JVM**, que significa **Java Virtual Machine** o Máquina Virtual de Java.

El programador escribe el código en Java, el compilador lo convierte en bytecode y luego la JVM ejecuta ese bytecode en el sistema operativo correspondiente.

---

## 6. ¿Qué significa que Java sea orientado a objetos?

Java es un lenguaje orientado a objetos porque permite organizar los programas usando clases y objetos.

Un **objeto** puede representar un elemento del mundo real o del problema que se quiere resolver.

Ejemplo:

Si queremos crear un sistema académico, podríamos tener objetos como:

- Estudiante.
- Asignatura.
- Docente.
- Nota.
- Curso.

Cada objeto puede tener características y comportamientos.

Ejemplo de clase:

```java
public class Estudiante {
    String nombre;
    double notaFinal;
}
```

En este curso se iniciará con programas básicos y más adelante se trabajará la Programación Orientada a Objetos con mayor profundidad.

---

## 7. ¿Qué significa que Java sea fuertemente tipado?

Java es un lenguaje **fuertemente tipado** porque cada variable debe tener un tipo de dato definido.

Ejemplo:

```java
int edad = 18;
double nota = 4.5;
String nombre = "Ana";
boolean aprobado = true;
```

Esto significa que Java necesita saber qué tipo de dato se va a guardar en cada variable.

En palabras sencillas:

- Si vas a guardar una edad, puedes usar `int`.
- Si vas a guardar una nota con decimales, puedes usar `double`.
- Si vas a guardar texto, puedes usar `String`.
- Si vas a guardar verdadero o falso, puedes usar `boolean`.

---

## 8. ¿Qué tipos de aplicaciones se pueden crear con Java?

Con Java se pueden crear muchos tipos de aplicaciones, por ejemplo:

- Aplicaciones de consola.
- Aplicaciones de escritorio.
- Aplicaciones web.
- Servicios backend.
- Aplicaciones empresariales.
- Sistemas académicos.
- Sistemas de inventario.
- Sistemas bancarios.
- Aplicaciones móviles con tecnologías relacionadas.
- Aplicaciones de procesamiento de datos.

En este curso se iniciará con aplicaciones de consola, porque son las más adecuadas para aprender lógica de programación.

---

## 9. ¿Qué es una aplicación de consola?

Una aplicación de consola es un programa que se ejecuta en una ventana de texto.

Ejemplo de salida en consola:

```text
Ingrese su nombre:
Ana
Bienvenida, Ana
```

Este tipo de aplicación permite practicar:

- Entrada de datos.
- Salida de datos.
- Variables.
- Operaciones.
- Condicionales.
- Ciclos.
- Métodos.
- Arreglos.

Es ideal para iniciar porque permite concentrarse en la lógica sin distraerse con interfaces gráficas.

---

## 10. Java frente a pseudocódigo

| Aspecto | Pseudocódigo | Java |
|---|---|---|
| Propósito | Diseñar la lógica | Implementar programas reales |
| Sintaxis | Flexible | Estricta |
| Ejecución | PSeInt | JDK/JVM |
| Tipos de datos | Más simples | Más formales |
| Errores | Más fáciles de interpretar | Más técnicos |
| Uso | Aprendizaje inicial | Desarrollo de software |

---

## 11. Primer vistazo a un programa Java

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

Aunque parece corto, este programa contiene varios elementos importantes:

- Una clase.
- Un método principal.
- Llaves de apertura y cierre.
- Una instrucción de salida.
- Punto y coma.

Cada parte tiene una función específica.

---

## 12. Elementos básicos de Java

Al iniciar con Java se deben reconocer estos elementos:

| Elemento | Ejemplo | Explicación |
|---|---|---|
| Clase | `public class HolaMundo` | Contenedor principal del programa |
| Método principal | `main` | Punto de inicio de ejecución |
| Llaves | `{ }` | Agrupan bloques de código |
| Punto y coma | `;` | Finaliza instrucciones |
| Comentario | `// texto` | Explica el código |
| Variable | `int edad;` | Guarda datos |
| Salida | `System.out.println()` | Muestra información |
| Entrada | `Scanner` | Lee datos del teclado |

---

## 13. ¿Por qué Java exige tanta precisión?

Java tiene reglas estrictas. Por ejemplo, distingue entre mayúsculas y minúsculas.

Esto significa que no es lo mismo:

```java
System
```

que:

```java
system
```

Tampoco es lo mismo:

```java
PromedioNotas
```

que:

```java
promedionotas
```

Esa precisión ayuda a formar buenos hábitos desde el inicio.

---

## 14. Relación entre algoritmo y Java

Antes de escribir Java, conviene diseñar el algoritmo.

Ejemplo:

Problema:

```text
Calcular el doble de un número.
```

Algoritmo en lenguaje natural:

```text
1. Pedir un número.
2. Multiplicar el número por 2.
3. Mostrar el resultado.
```

Programa en Java:

```java
import java.util.Scanner;

public class CalcularDoble {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;
        int doble;

        System.out.print("Ingrese un número: ");
        numero = entrada.nextInt();

        doble = numero * 2;

        System.out.println("El doble es: " + doble);

        entrada.close();
    }
}
```

---

## 15. Recomendación metodológica

En este curso se recomienda seguir siempre esta ruta:

```text
Problema
   ↓
Análisis de entrada, proceso y salida
   ↓
Pseudocódigo
   ↓
Prueba de escritorio
   ↓
Código Java
   ↓
Ejecución y corrección
```

La finalidad es evitar que el estudiante copie código sin comprenderlo.

---

## 16. Resumen

Java es un lenguaje de programación de alto nivel, multiplataforma, orientado a objetos y fuertemente tipado. Es una herramienta adecuada para aprender programación porque exige orden, claridad y precisión.

En este curso se usará Java para implementar soluciones algorítmicas, iniciando con programas de consola y avanzando progresivamente hacia estructuras de control, arreglos, métodos y programación orientada a objetos.
