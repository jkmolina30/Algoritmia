# Ejercicios Resueltos en Java

## Unidad 2. Introducción a la Algoritmia

Este archivo contiene ejercicios resueltos únicamente en **Java**.  
El propósito es que el estudiante observe cómo una solución algorítmica puede implementarse en un lenguaje de programación real.

Cada ejercicio incluye:

1. Enunciado.
2. Análisis de entrada, proceso y salida.
3. Código en Java.
4. Explicación línea a línea.
5. Prueba de escritorio.

---

# Estructura básica de los programas

En esta unidad todos los programas tienen una estructura similar:

```java
import java.util.Scanner;

public class NombreDelPrograma {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        // Instrucciones del programa

        entrada.close();
    }
}
```

## Explicación sencilla

```java
import java.util.Scanner;
```

Importa la clase `Scanner`, que permite leer datos desde el teclado.

```java
public class NombreDelPrograma
```

Define una clase. En Java, el código se organiza dentro de clases.

```java
public static void main(String[] args)
```

Es el método principal. Desde aquí inicia la ejecución del programa.

```java
Scanner entrada = new Scanner(System.in);
```

Crea un objeto llamado `entrada` que permite recibir datos del usuario.

```java
entrada.close();
```

Cierra el objeto `Scanner` al final del programa.

---

# Ejercicio 1. Suma de dos números

## Enunciado

Diseñar un programa en Java que lea dos números enteros y muestre la suma.

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `num1`, `num2` |
| Proceso | `suma = num1 + num2` |
| Salida | Resultado de la suma |

---

## Código Java

```java
import java.util.Scanner;

public class SumaDosNumeros {
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

## Explicación línea a línea

```java
int num1;
int num2;
int suma;
```

Se declaran tres variables enteras.  
`num1` y `num2` guardan los números ingresados.  
`suma` guarda el resultado.

```java
num1 = entrada.nextInt();
```

Lee un número entero y lo guarda en `num1`.

```java
num2 = entrada.nextInt();
```

Lee otro número entero y lo guarda en `num2`.

```java
suma = num1 + num2;
```

Suma los dos valores.

```java
System.out.println("La suma es: " + suma);
```

Muestra el resultado.

---

## Prueba de escritorio

Datos de prueba:

```text
num1 = 12
num2 = 8
```

| Paso | num1 | num2 | suma | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer num1 | 12 | - | - | - |
| Leer num2 | 12 | 8 | - | - |
| Calcular suma | 12 | 8 | 20 | - |
| Mostrar resultado | 12 | 8 | 20 | La suma es: 20 |

---

# Ejercicio 2. Área de un triángulo

## Enunciado

Diseñar un programa en Java que calcule el área de un triángulo a partir de su base y altura.

---

## Fórmula

```text
area = (base * altura) / 2
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `base`, `altura` |
| Proceso | `area = (base * altura) / 2` |
| Salida | Área del triángulo |

---

## Código Java

```java
import java.util.Scanner;

public class AreaTriangulo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double base;
        double altura;
        double area;

        System.out.print("Ingrese la base del triángulo: ");
        base = entrada.nextDouble();

        System.out.print("Ingrese la altura del triángulo: ");
        altura = entrada.nextDouble();

        area = (base * altura) / 2;

        System.out.println("El área del triángulo es: " + area);

        entrada.close();
    }
}
```

---

## Explicación línea a línea

```java
double base;
double altura;
double area;
```

Se usa `double` porque los valores pueden ser decimales.

```java
base = entrada.nextDouble();
altura = entrada.nextDouble();
```

Lee los valores ingresados por el usuario.

```java
area = (base * altura) / 2;
```

Calcula el área usando la fórmula.

---

## Prueba de escritorio

Datos de prueba:

```text
base = 10
altura = 6
```

| Paso | base | altura | area | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer base | 10 | - | - | - |
| Leer altura | 10 | 6 | - | - |
| Calcular área | 10 | 6 | 30 | - |
| Mostrar resultado | 10 | 6 | 30 | El área del triángulo es: 30 |

---

# Ejercicio 3. Conversión de kilómetros a metros

## Enunciado

Diseñar un programa en Java que lea una cantidad de kilómetros y muestre su equivalente en metros.

---

## Fórmula

```text
metros = kilometros * 1000
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `kilometros` |
| Proceso | `metros = kilometros * 1000` |
| Salida | Metros equivalentes |

---

## Código Java

```java
import java.util.Scanner;

public class KilometrosAMetros {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double kilometros;
        double metros;

        System.out.print("Ingrese la cantidad de kilómetros: ");
        kilometros = entrada.nextDouble();

        metros = kilometros * 1000;

        System.out.println(kilometros + " kilómetros equivalen a " + metros + " metros.");

        entrada.close();
    }
}
```

---

## Explicación

```java
double kilometros;
double metros;
```

Se usa `double` para permitir valores con decimales.

```java
metros = kilometros * 1000;
```

Convierte kilómetros a metros.

---

## Prueba de escritorio

Dato de prueba:

```text
kilometros = 3.5
```

| Paso | kilometros | metros | Salida |
|---|---:|---:|---|
| Inicio | - | - | - |
| Leer kilómetros | 3.5 | - | - |
| Calcular metros | 3.5 | 3500 | - |
| Mostrar resultado | 3.5 | 3500 | 3.5 kilómetros equivalen a 3500 metros |

---

# Ejercicio 4. Salario semanal

## Enunciado

Diseñar un programa en Java que lea las horas trabajadas por una persona y el valor de cada hora. Luego debe mostrar el salario semanal.

---

## Fórmula

```text
salario = horasTrabajadas * valorHora
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `horasTrabajadas`, `valorHora` |
| Proceso | `salario = horasTrabajadas * valorHora` |
| Salida | Salario semanal |

---

## Código Java

```java
import java.util.Scanner;

public class SalarioSemanal {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double horasTrabajadas;
        double valorHora;
        double salario;

        System.out.print("Ingrese las horas trabajadas: ");
        horasTrabajadas = entrada.nextDouble();

        System.out.print("Ingrese el valor de cada hora: ");
        valorHora = entrada.nextDouble();

        salario = horasTrabajadas * valorHora;

        System.out.println("El salario semanal es: " + salario);

        entrada.close();
    }
}
```

---

## Explicación

El programa recibe dos datos: horas trabajadas y valor por hora.  
Luego multiplica esos valores para obtener el salario semanal.

---

## Prueba de escritorio

Datos de prueba:

```text
horasTrabajadas = 40
valorHora = 12000
```

| Paso | horasTrabajadas | valorHora | salario |
|---|---:|---:|---:|
| Inicio | - | - | - |
| Leer horas | 40 | - | - |
| Leer valor hora | 40 | 12000 | - |
| Calcular salario | 40 | 12000 | 480000 |
| Mostrar resultado | 40 | 12000 | 480000 |

---

# Ejercicio 5. Valor final de una compra

## Enunciado

Diseñar un programa en Java que lea el precio de un producto, la cantidad comprada y muestre el total a pagar.

---

## Fórmula

```text
total = precio * cantidad
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `precio`, `cantidad` |
| Proceso | `total = precio * cantidad` |
| Salida | Total a pagar |

---

## Código Java

```java
import java.util.Scanner;

public class ValorCompra {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double precio;
        int cantidad;
        double total;

        System.out.print("Ingrese el precio del producto: ");
        precio = entrada.nextDouble();

        System.out.print("Ingrese la cantidad comprada: ");
        cantidad = entrada.nextInt();

        total = precio * cantidad;

        System.out.println("El total a pagar es: " + total);

        entrada.close();
    }
}
```

---

## Explicación

```java
double precio;
```

Se usa `double` porque el precio puede tener decimales.

```java
int cantidad;
```

Se usa `int` porque la cantidad suele ser un número entero.

---

## Prueba de escritorio

Datos de prueba:

```text
precio = 2500
cantidad = 4
```

| Paso | precio | cantidad | total |
|---|---:|---:|---:|
| Inicio | - | - | - |
| Leer precio | 2500 | - | - |
| Leer cantidad | 2500 | 4 | - |
| Calcular total | 2500 | 4 | 10000 |
| Mostrar resultado | 2500 | 4 | 10000 |

---

# Ejercicio 6. Edad aproximada

## Enunciado

Diseñar un programa en Java que lea el año actual y el año de nacimiento de una persona. Luego debe mostrar su edad aproximada.

---

## Fórmula

```text
edad = anioActual - anioNacimiento
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `anioActual`, `anioNacimiento` |
| Proceso | `edad = anioActual - anioNacimiento` |
| Salida | Edad aproximada |

---

## Código Java

```java
import java.util.Scanner;

public class EdadAproximada {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int anioActual;
        int anioNacimiento;
        int edad;

        System.out.print("Ingrese el año actual: ");
        anioActual = entrada.nextInt();

        System.out.print("Ingrese el año de nacimiento: ");
        anioNacimiento = entrada.nextInt();

        edad = anioActual - anioNacimiento;

        System.out.println("La edad aproximada es: " + edad);

        entrada.close();
    }
}
```

---

## Explicación

Este cálculo entrega una edad aproximada porque no considera el mes ni el día de nacimiento.

---

## Prueba de escritorio

Datos de prueba:

```text
anioActual = 2026
anioNacimiento = 2008
```

| Paso | anioActual | anioNacimiento | edad |
|---|---:|---:|---:|
| Inicio | - | - | - |
| Leer año actual | 2026 | - | - |
| Leer año nacimiento | 2026 | 2008 | - |
| Calcular edad | 2026 | 2008 | 18 |
| Mostrar resultado | 2026 | 2008 | 18 |

---

# Ejercicio 7. Promedio de tres notas

## Enunciado

Diseñar un programa en Java que lea tres notas y calcule el promedio.

---

## Fórmula

```text
promedio = (nota1 + nota2 + nota3) / 3
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `nota1`, `nota2`, `nota3` |
| Proceso | `promedio = (nota1 + nota2 + nota3) / 3` |
| Salida | Promedio de las tres notas |

---

## Código Java

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

## Explicación importante

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

Los paréntesis son necesarios porque primero se suman las tres notas y luego se divide el resultado entre 3.

Si se escribiera así:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

El resultado sería incorrecto, porque Java dividiría primero `nota3 / 3`.

---

## Prueba de escritorio

Datos de prueba:

```text
nota1 = 4.0
nota2 = 3.5
nota3 = 5.0
```

| Paso | nota1 | nota2 | nota3 | promedio |
|---|---:|---:|---:|---:|
| Inicio | - | - | - | - |
| Leer nota1 | 4.0 | - | - | - |
| Leer nota2 | 4.0 | 3.5 | - | - |
| Leer nota3 | 4.0 | 3.5 | 5.0 | - |
| Calcular promedio | 4.0 | 3.5 | 5.0 | 4.166 |
| Mostrar resultado | 4.0 | 3.5 | 5.0 | 4.166 |

---

# Recomendación final

Antes de copiar el código, el estudiante debe responder:

```text
¿Qué dato entra?
¿Qué proceso se realiza?
¿Qué resultado se muestra?
¿Qué tipo de dato necesito?
```

El objetivo es entender la lógica, no memorizar instrucciones.
