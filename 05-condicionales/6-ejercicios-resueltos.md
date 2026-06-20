# Ejercicios Resueltos: Condicionales en Java

## Presentación

Este archivo contiene ejercicios resueltos de condicionales, con enfoque principal en Java.

Cada ejercicio incluye:

1. Enunciado.
2. Análisis.
3. Código Java.
4. Explicación.
5. Prueba de escritorio.

---

# Ejercicio 1. Mayor de edad

## Enunciado

Leer la edad de una persona e indicar si es mayor o menor de edad.

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | edad |
| Proceso | comparar si edad >= 18 |
| Salida | mensaje de mayor o menor de edad |

## Código Java

```java
import java.util.Scanner;

public class MayorEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int edad;

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        if (edad >= 18) {
            System.out.println("La persona es mayor de edad");
        } else {
            System.out.println("La persona es menor de edad");
        }

        entrada.close();
    }
}
```

## Prueba de escritorio

| edad | Condición `edad >= 18` | Salida |
|---:|---|---|
| 20 | true | La persona es mayor de edad |
| 15 | false | La persona es menor de edad |

---

# Ejercicio 2. Número par o impar

## Enunciado

Leer un número entero e indicar si es par o impar.

## Análisis

Un número es par si al dividirlo entre 2 el residuo es 0.

En Java:

```java
numero % 2 == 0
```

## Código Java

```java
import java.util.Scanner;

public class ParImpar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;

        System.out.print("Ingrese un número entero: ");
        numero = entrada.nextInt();

        if (numero % 2 == 0) {
            System.out.println("El número es par");
        } else {
            System.out.println("El número es impar");
        }

        entrada.close();
    }
}
```

## Explicación

El operador `%` obtiene el residuo de una división.

Ejemplo:

```text
10 % 2 = 0
11 % 2 = 1
```

---

# Ejercicio 3. Mayor de dos números

## Enunciado

Leer dos números e indicar cuál es mayor o si son iguales.

## Código Java

```java
import java.util.Scanner;

public class MayorDosNumeros {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double num1;
        double num2;

        System.out.print("Ingrese el primer número: ");
        num1 = entrada.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        num2 = entrada.nextDouble();

        if (num1 > num2) {
            System.out.println("El mayor es: " + num1);
        } else if (num2 > num1) {
            System.out.println("El mayor es: " + num2);
        } else {
            System.out.println("Los números son iguales");
        }

        entrada.close();
    }
}
```

---

# Ejercicio 4. Validar nota y determinar aprobación

## Enunciado

Leer una nota. Si está fuera del rango 0.0 a 5.0, mostrar que no es válida. Si es válida, indicar si aprueba o reprueba.

## Código Java

```java
import java.util.Scanner;

public class ValidarYAprobar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        System.out.print("Ingrese la nota: ");
        nota = entrada.nextDouble();

        if (nota < 0.0 || nota > 5.0) {
            System.out.println("Nota no válida");
        } else if (nota >= 3.0) {
            System.out.println("Nota válida. El estudiante aprobó");
        } else {
            System.out.println("Nota válida. El estudiante reprobó");
        }

        entrada.close();
    }
}
```

## Explicación

Primero se valida el rango.  
Luego, solo si la nota es válida, se revisa si aprobó.

---

# Ejercicio 5. Descuento en compra

## Enunciado

Leer el valor de una compra. Si supera 100000, aplicar descuento del 10%. Si no, no aplicar descuento.

## Código Java

```java
import java.util.Scanner;

public class DescuentoCompra {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double valorCompra;
        double descuento;
        double total;

        System.out.print("Ingrese el valor de la compra: ");
        valorCompra = entrada.nextDouble();

        if (valorCompra > 100000) {
            descuento = valorCompra * 0.10;
        } else {
            descuento = 0;
        }

        total = valorCompra - descuento;

        System.out.println("Valor de la compra: " + valorCompra);
        System.out.println("Descuento: " + descuento);
        System.out.println("Total a pagar: " + total);

        entrada.close();
    }
}
```

---

# Ejercicio 6. Menú de operaciones

## Enunciado

Crear un programa que lea dos números y una opción. Según la opción, realizar suma, resta, multiplicación o división.

## Código Java

```java
import java.util.Scanner;

public class MenuOperaciones {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double num1;
        double num2;
        int opcion;

        System.out.print("Ingrese el primer número: ");
        num1 = entrada.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        num2 = entrada.nextDouble();

        System.out.println("1. Sumar");
        System.out.println("2. Restar");
        System.out.println("3. Multiplicar");
        System.out.println("4. Dividir");
        System.out.print("Seleccione una opción: ");
        opcion = entrada.nextInt();

        switch (opcion) {
            case 1:
                System.out.println("Resultado: " + (num1 + num2));
                break;
            case 2:
                System.out.println("Resultado: " + (num1 - num2));
                break;
            case 3:
                System.out.println("Resultado: " + (num1 * num2));
                break;
            case 4:
                if (num2 != 0) {
                    System.out.println("Resultado: " + (num1 / num2));
                } else {
                    System.out.println("No se puede dividir entre cero");
                }
                break;
            default:
                System.out.println("Opción no válida");
                break;
        }

        entrada.close();
    }
}
```

---

## Recomendación final

En los ejercicios de condicionales no basta con probar un solo dato.  
Se deben probar todos los caminos posibles.

Por ejemplo, si hay un `if-else`, se debe probar:

- Un dato que haga verdadera la condición.
- Un dato que haga falsa la condición.
