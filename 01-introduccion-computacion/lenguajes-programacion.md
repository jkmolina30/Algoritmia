# Lenguajes de Programación

## 1. ¿Qué es un lenguaje de programación?

Un lenguaje de programación es un conjunto de reglas, símbolos y palabras que permite escribir instrucciones para que un computador realice una tarea.

Así como las personas usan idiomas para comunicarse, los programadores usan lenguajes de programación para comunicarse con el computador.

Ejemplos de lenguajes de programación:

* Java.
* Python.
* C.
* C++.
* JavaScript.
* C#.
* PHP.
* Ruby.
* Go.

En este curso se trabajará principalmente con pseudocódigo, PSeInt y Java.

---

## 2. ¿Por qué existen los lenguajes de programación?

Los computadores internamente trabajan con señales eléctricas y datos binarios.

Esto significa que a nivel muy bajo utilizan valores como:

```text
0 y 1
```

Para una persona sería muy difícil escribir programas directamente usando solo ceros y unos.

Por eso existen lenguajes de programación, que permiten escribir instrucciones más comprensibles.

---

## 3. Lenguaje de máquina

El lenguaje de máquina es el lenguaje más básico que entiende directamente el computador.

Está formado por instrucciones en código binario.

Ejemplo representativo:

```text
10110000 01100001
```

Este tipo de lenguaje no es práctico para la mayoría de programadores, porque es difícil de leer, escribir y corregir.

---

## 4. Lenguajes de bajo nivel

Los lenguajes de bajo nivel están más cerca del funcionamiento interno del computador.

Un ejemplo es el lenguaje ensamblador.

Estos lenguajes permiten controlar con mucho detalle el hardware, pero son más difíciles de aprender.

Ejemplo representativo de ensamblador:

```asm
MOV AX, 5
ADD AX, 3
```

No es necesario dominar este tipo de lenguaje en un curso inicial de algoritmia, pero es importante saber que existen.

---

## 5. Lenguajes de alto nivel

Los lenguajes de alto nivel son más cercanos al lenguaje humano.

Permiten escribir instrucciones de forma más comprensible.

Ejemplo en Java:

```java
int suma = 5 + 3;
```

Ejemplo en Python:

```python
suma = 5 + 3
```

Estos lenguajes facilitan el desarrollo de programas, porque permiten concentrarse más en la solución del problema que en los detalles internos de la máquina.

---

## 6. Java como lenguaje de programación

Java es un lenguaje de programación de alto nivel, ampliamente utilizado en educación, desarrollo de aplicaciones empresariales, sistemas web, aplicaciones móviles y proyectos de software.

En este curso se usa Java porque permite aprender:

* Sintaxis formal.
* Tipos de datos.
* Condicionales.
* Ciclos.
* Métodos.
* Arreglos.
* Matrices.
* Programación Orientada a Objetos.
* Buenas prácticas de programación.

---

## 7. Pseudocódigo

El pseudocódigo no es un lenguaje de programación formal como Java.

El pseudocódigo es una forma de representar algoritmos usando instrucciones cercanas al lenguaje humano.

Ejemplo:

```pseint
Escribir "Ingrese su nombre"
Leer nombre
```

Su objetivo es ayudar a comprender la lógica antes de escribir código real.

---

## 8. PSeInt

PSeInt es una herramienta que permite escribir y ejecutar algoritmos en pseudocódigo.

Es muy útil para estudiantes que están aprendiendo a programar, porque permite concentrarse en la lógica sin preocuparse demasiado por la sintaxis estricta de un lenguaje como Java.

Ejemplo en PSeInt:

```pseint
Algoritmo Saludo
    Definir nombre Como Caracter

    Escribir "Ingrese su nombre:"
    Leer nombre

    Escribir "Hola ", nombre
FinAlgoritmo
```

---

## 9. Diferencia entre pseudocódigo y Java

| Aspecto            | Pseudocódigo               | Java                        |
| ------------------ | -------------------------- | --------------------------- |
| Propósito          | Diseñar la lógica          | Crear programas ejecutables |
| Nivel de exigencia | Flexible                   | Estricto                    |
| Sintaxis           | Cercana al lenguaje humano | Reglas formales             |
| Uso principal      | Aprendizaje y diseño       | Desarrollo de software      |
| Ejecución          | Herramientas como PSeInt   | JDK y entorno Java          |

---

## 10. Ejemplo comparativo

Problema:

```text
Leer dos números y mostrar la suma.
```

### Solución en pseudocódigo

```pseint
Algoritmo SumarDosNumeros
    Definir num1, num2, suma Como Entero

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    suma <- num1 + num2

    Escribir "La suma es: ", suma
FinAlgoritmo
```

### Solución en Java

```java
import java.util.Scanner;

public class SumarDosNumeros {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int num1;
        int num2;
        int suma;

        System.out.print("Ingrese el primer número: ");
        num1 = entrada.nextInt();

        System.out.print("Ingrese el segundo número: ");
        num2 = entrada.nextInt();

        suma = num1 + num2;

        System.out.println("La suma es: " + suma);

        entrada.close();
    }
}
```

---

## 11. Compilador

Un compilador es un programa que traduce el código escrito por el programador a un formato que la máquina puede ejecutar o interpretar.

En Java, el archivo con extensión `.java` se compila y se convierte en un archivo `.class`.

Ejemplo:

Archivo original:

```text
HolaMundo.java
```

Después de compilar:

```text
HolaMundo.class
```

---

## 12. Intérprete

Un intérprete ejecuta instrucciones directamente, generalmente línea por línea o mediante una máquina de ejecución.

En Java existe la **Máquina Virtual de Java**, conocida como **JVM**.

La JVM permite ejecutar el bytecode generado por el compilador de Java.

---

## 13. Proceso básico de ejecución en Java

El proceso general es:

```text
Código Java (.java)
        ↓
Compilador javac
        ↓
Bytecode (.class)
        ↓
Máquina Virtual de Java JVM
        ↓
Ejecución del programa
```

### Explicación sencilla

1. El programador escribe el código en un archivo `.java`.
2. El compilador revisa y traduce el código.
3. Se genera un archivo `.class`.
4. La JVM ejecuta ese archivo.
5. El usuario ve el resultado del programa.

---

## 14. Código fuente

El código fuente es el archivo escrito por el programador.

Ejemplo:

```java
public class HolaMundo {
    public static void main(String[] args) {
        System.out.println("Hola mundo");
    }
}
```

Este código debe guardarse en un archivo llamado:

```text
HolaMundo.java
```

---

## 15. Errores de sintaxis

Un error de sintaxis ocurre cuando el código no cumple las reglas del lenguaje.

Ejemplo incorrecto:

```java
System.out.println("Hola mundo")
```

Falta el punto y coma.

Ejemplo correcto:

```java
System.out.println("Hola mundo");
```

En Java, muchos errores aparecen porque falta un símbolo, una llave, una comilla, un paréntesis o un punto y coma.

---

## 16. Errores lógicos

Un error lógico ocurre cuando el programa se ejecuta, pero el resultado es incorrecto.

Ejemplo:

Queremos calcular el promedio de tres notas, pero escribimos:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

El problema es que la división se realiza solo sobre `nota3`.

La forma correcta sería:

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

Los paréntesis son importantes porque indican qué operación debe hacerse primero.

---

## 17. Importancia de los lenguajes de programación

Los lenguajes de programación permiten crear soluciones tecnológicas para diferentes áreas.

Ejemplos:

| Área             | Aplicación                            |
| ---------------- | ------------------------------------- |
| Educación        | Plataformas académicas                |
| Salud            | Sistemas de historias clínicas        |
| Comercio         | Sistemas de ventas                    |
| Transporte       | Aplicaciones de rutas                 |
| Finanzas         | Cajeros y banca virtual               |
| Ciencia de datos | Análisis y predicción                 |
| Entretenimiento  | Videojuegos y aplicaciones multimedia |

---

## 18. Resumen

Un lenguaje de programación permite escribir instrucciones para que un computador realice tareas. En este curso se inicia con pseudocódigo para aprender la lógica y luego se usa Java para construir programas reales. Comprender esta relación ayuda a que el estudiante no memorice instrucciones, sino que entienda cómo se transforma una idea en una solución computacional.

---
