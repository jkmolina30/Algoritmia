# Ejemplos de Introducción a la Computación

## Presentación

Este archivo contiene ejemplos sencillos para comprender cómo un computador recibe datos, los procesa y entrega resultados.

Los ejemplos no buscan todavía profundizar en la sintaxis de Java, sino mostrar la relación entre computador, datos, programa y solución de problemas.

---

## Ejemplo 1. Calcular el promedio de tres notas

### Problema

Un estudiante desea calcular el promedio de tres notas.

---

### Análisis computacional

| Elemento       | Descripción                                   |
| -------------- | --------------------------------------------- |
| Entrada        | nota1, nota2, nota3                           |
| Procesamiento  | sumar las tres notas y dividir entre 3        |
| Almacenamiento | guardar temporalmente las notas y el promedio |
| Salida         | mostrar el promedio                           |

---

### Solución en lenguaje natural

1. Pedir la primera nota.
2. Pedir la segunda nota.
3. Pedir la tercera nota.
4. Sumar las tres notas.
5. Dividir la suma entre tres.
6. Mostrar el promedio.

---

### Pseudocódigo

```pseint
Algoritmo PromedioTresNotas
    Definir nota1, nota2, nota3, promedio Como Real

    Escribir "Ingrese la primera nota:"
    Leer nota1

    Escribir "Ingrese la segunda nota:"
    Leer nota2

    Escribir "Ingrese la tercera nota:"
    Leer nota3

    promedio <- (nota1 + nota2 + nota3) / 3

    Escribir "El promedio es: ", promedio
FinAlgoritmo
```

---

### Implementación en Java

```java
import java.util.Scanner;

public class PromedioTresNotas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota1;
        double nota2;
        double nota3;
        double promedio;

        System.out.print("Ingrese la primera nota: ");
        nota1 = entrada.nextDouble();

        System.out.print("Ingrese la segunda nota: ");
        nota2 = entrada.nextDouble();

        System.out.print("Ingrese la tercera nota: ");
        nota3 = entrada.nextDouble();

        promedio = (nota1 + nota2 + nota3) / 3;

        System.out.println("El promedio es: " + promedio);

        entrada.close();
    }
}
```

---

### Explicación desde la computación

| Parte                | Explicación                                       |
| -------------------- | ------------------------------------------------- |
| `Scanner`            | Permite recibir datos de entrada desde el teclado |
| Variables            | Guardan temporalmente las notas y el promedio     |
| Operación matemática | Representa el procesamiento                       |
| `System.out.println` | Muestra la salida al usuario                      |

---

## Ejemplo 2. Determinar si una persona es mayor de edad

### Problema

Se desea saber si una persona es mayor de edad a partir de su edad.

---

### Análisis computacional

| Elemento       | Descripción                                   |
| -------------- | --------------------------------------------- |
| Entrada        | edad                                          |
| Procesamiento  | comparar si la edad es mayor o igual a 18     |
| Almacenamiento | guardar temporalmente la edad                 |
| Salida         | mensaje indicando si es mayor o menor de edad |

---

### Solución en lenguaje natural

1. Pedir la edad.
2. Comparar si la edad es mayor o igual a 18.
3. Si cumple la condición, mostrar que es mayor de edad.
4. Si no cumple la condición, mostrar que es menor de edad.

---

### Pseudocódigo

```pseint
Algoritmo MayorEdad
    Definir edad Como Entero

    Escribir "Ingrese su edad:"
    Leer edad

    Si edad >= 18 Entonces
        Escribir "La persona es mayor de edad."
    Sino
        Escribir "La persona es menor de edad."
    FinSi
FinAlgoritmo
```

---

### Implementación en Java

```java
import java.util.Scanner;

public class MayorEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int edad;

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        if (edad >= 18) {
            System.out.println("La persona es mayor de edad.");
        } else {
            System.out.println("La persona es menor de edad.");
        }

        entrada.close();
    }
}
```

---

### Explicación desde la computación

El computador recibe un dato numérico llamado `edad`.

Luego compara ese dato con el valor `18`.

La comparación produce un resultado lógico:

```text
Verdadero o falso
```

Si la condición es verdadera, se ejecuta una salida. Si es falsa, se ejecuta otra.

---

## Ejemplo 3. Registrar el nombre de un estudiante

### Problema

Se desea pedir el nombre de un estudiante y mostrar un mensaje de bienvenida.

---

### Análisis computacional

| Elemento       | Descripción                        |
| -------------- | ---------------------------------- |
| Entrada        | nombre                             |
| Procesamiento  | construir un mensaje con el nombre |
| Almacenamiento | guardar temporalmente el nombre    |
| Salida         | mostrar mensaje de bienvenida      |

---

### Pseudocódigo

```pseint
Algoritmo SaludoEstudiante
    Definir nombre Como Caracter

    Escribir "Ingrese su nombre:"
    Leer nombre

    Escribir "Bienvenido al curso, ", nombre
FinAlgoritmo
```

---

### Implementación en Java

```java
import java.util.Scanner;

public class SaludoEstudiante {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;

        System.out.print("Ingrese su nombre: ");
        nombre = entrada.nextLine();

        System.out.println("Bienvenido al curso, " + nombre);

        entrada.close();
    }
}
```

---

### Explicación desde la computación

El dato ingresado no es numérico, sino texto.

Por eso en Java se usa:

```java
String nombre;
```

`String` permite guardar cadenas de texto.

---

## Ejemplo 4. Calcular el área de un rectángulo

### Problema

Se desea calcular el área de un rectángulo conociendo su base y altura.

---

### Análisis computacional

| Elemento       | Descripción                 |
| -------------- | --------------------------- |
| Entrada        | base, altura                |
| Procesamiento  | multiplicar base por altura |
| Almacenamiento | guardar base, altura y área |
| Salida         | mostrar el área             |

---

### Fórmula

```text
Área = base * altura
```

---

### Pseudocódigo

```pseint
Algoritmo AreaRectangulo
    Definir base, altura, area Como Real

    Escribir "Ingrese la base:"
    Leer base

    Escribir "Ingrese la altura:"
    Leer altura

    area <- base * altura

    Escribir "El área es: ", area
FinAlgoritmo
```

---

### Implementación en Java

```java
import java.util.Scanner;

public class AreaRectangulo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double base;
        double altura;
        double area;

        System.out.print("Ingrese la base: ");
        base = entrada.nextDouble();

        System.out.print("Ingrese la altura: ");
        altura = entrada.nextDouble();

        area = base * altura;

        System.out.println("El área es: " + area);

        entrada.close();
    }
}
```

---

## Ejemplo 5. Relación entre hardware y software en un programa

### Situación

Un estudiante ejecuta un programa en Java para sumar dos números.

---

### Hardware utilizado

| Componente | Función                          |
| ---------- | -------------------------------- |
| Teclado    | Permite ingresar los números     |
| CPU        | Realiza la suma                  |
| RAM        | Guarda temporalmente los valores |
| Pantalla   | Muestra el resultado             |
| Disco      | Guarda el archivo `.java`        |

---

### Software utilizado

| Software          | Función                                              |
| ----------------- | ---------------------------------------------------- |
| Sistema operativo | Permite usar el computador                           |
| JDK               | Permite compilar y ejecutar Java                     |
| NetBeans          | Permite escribir y organizar el código               |
| Programa Java     | Contiene las instrucciones creadas por el estudiante |

---

## Ejemplo 6. De la idea al programa

### Idea inicial

```text
Quiero saber si un estudiante aprobó una asignatura.
```

---

### Análisis

| Elemento | Descripción                                 |
| -------- | ------------------------------------------- |
| Entrada  | nota final                                  |
| Proceso  | verificar si la nota es mayor o igual a 3.0 |
| Salida   | mensaje de aprobado o reprobado             |

---

### Algoritmo en lenguaje natural

1. Pedir la nota final.
2. Si la nota es mayor o igual a 3.0, mostrar “Aprobó”.
3. Si la nota es menor que 3.0, mostrar “Reprobó”.

---

### Pseudocódigo

```pseint
Algoritmo AprobarAsignatura
    Definir nota Como Real

    Escribir "Ingrese la nota final:"
    Leer nota

    Si nota >= 3.0 Entonces
        Escribir "Aprobó"
    Sino
        Escribir "Reprobó"
    FinSi
FinAlgoritmo
```

---

### Java

```java
import java.util.Scanner;

public class AprobarAsignatura {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota final: ");
        nota = entrada.nextDouble();

        if (nota >= 3.0) {
            System.out.println("Aprobó");
        } else {
            System.out.println("Reprobó");
        }

        entrada.close();
    }
}
```

---

## Conclusión de los ejemplos

En todos los ejemplos se repite la misma lógica:

```text
Entrada → Procesamiento → Salida
```

Esta estructura será la base para resolver problemas durante todo el curso.

Antes de programar, el estudiante debe aprender a identificar qué datos necesita, qué debe hacer con ellos y qué resultado espera obtener.

---
