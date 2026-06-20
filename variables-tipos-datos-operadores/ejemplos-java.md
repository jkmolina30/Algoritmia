# Ejemplos en Java: Variables, Tipos de Datos y Operadores

## Presentación

Este archivo contiene ejemplos en Java para practicar:

- Declaración de variables.
- Tipos de datos.
- Entrada y salida de datos.
- Operadores aritméticos.
- Operadores relacionales.
- Expresiones.
- Uso de `Scanner`.

---

# Ejemplo 1. Datos personales

## Problema

Leer el nombre, la edad y el programa académico de un estudiante. Mostrar los datos ingresados.

---

## Código Java

```java
import java.util.Scanner;

public class DatosPersonales {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;
        String programa;
        int edad;

        System.out.print("Ingrese su nombre: ");
        nombre = entrada.nextLine();

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        entrada.nextLine();

        System.out.print("Ingrese su programa académico: ");
        programa = entrada.nextLine();

        System.out.println("Nombre: " + nombre);
        System.out.println("Edad: " + edad);
        System.out.println("Programa: " + programa);

        entrada.close();
    }
}
```

---

## Explicación

```java
String nombre;
String programa;
```

Se usan variables de tipo `String` porque guardan texto.

```java
int edad;
```

Se usa `int` porque la edad normalmente se representa como número entero.

```java
entrada.nextLine();
```

Después de leer un número con `nextInt()`, esta línea limpia el salto de línea pendiente antes de leer otro texto.

---

# Ejemplo 2. Operaciones básicas

## Problema

Leer dos números y mostrar suma, resta, multiplicación y división.

---

## Código Java

```java
import java.util.Scanner;

public class OperacionesBasicas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double num1;
        double num2;
        double suma;
        double resta;
        double multiplicacion;
        double division;

        System.out.print("Ingrese el primer número: ");
        num1 = entrada.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        num2 = entrada.nextDouble();

        suma = num1 + num2;
        resta = num1 - num2;
        multiplicacion = num1 * num2;
        division = num1 / num2;

        System.out.println("Suma: " + suma);
        System.out.println("Resta: " + resta);
        System.out.println("Multiplicación: " + multiplicacion);
        System.out.println("División: " + division);

        entrada.close();
    }
}
```

---

## Explicación

Se usa `double` porque los números pueden tener decimales.  
La división entre cero se validará más adelante cuando se estudien condicionales.

---

# Ejemplo 3. Promedio de tres notas

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

Los paréntesis hacen que primero se sumen las notas y luego se divida entre 3.

---

# Ejemplo 4. Área de un círculo

## Código Java

```java
import java.util.Scanner;

public class AreaCirculo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double radio;
        double area;

        System.out.print("Ingrese el radio del círculo: ");
        radio = entrada.nextDouble();

        area = Math.PI * Math.pow(radio, 2);

        System.out.println("El área del círculo es: " + area);

        entrada.close();
    }
}
```

---

## Explicación

En Java no se usa `^` para potencias.  
Para elevar un número se usa:

```java
Math.pow(radio, 2)
```

`Math.PI` representa el valor de PI.

---

# Ejemplo 5. Compra con IVA

## Código Java

```java
import java.util.Scanner;

public class CompraConIVA {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double valorProducto;
        double iva;
        double total;

        System.out.print("Ingrese el valor del producto: ");
        valorProducto = entrada.nextDouble();

        iva = valorProducto * 0.19;
        total = valorProducto + iva;

        System.out.println("Valor del producto: " + valorProducto);
        System.out.println("IVA: " + iva);
        System.out.println("Total a pagar: " + total);

        entrada.close();
    }
}
```

---

# Ejemplo 6. Comparación de nota

## Código Java

```java
import java.util.Scanner;

public class CompararNota {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;
        boolean resultado;

        System.out.print("Ingrese la nota: ");
        nota = entrada.nextDouble();

        resultado = nota >= 3.0;

        System.out.println("¿La nota es mayor o igual a 3.0?: " + resultado);

        entrada.close();
    }
}
```

---

## Explicación

```java
boolean resultado;
```

Una variable `boolean` guarda únicamente `true` o `false`.

```java
resultado = nota >= 3.0;
```

La comparación produce un valor lógico.

---

# Ejemplo 7. Nota definitiva

## Código Java

```java
import java.util.Scanner;

public class NotaDefinitiva {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double corte1;
        double corte2;
        double corte3;
        double definitiva;

        System.out.print("Ingrese la nota del primer corte: ");
        corte1 = entrada.nextDouble();

        System.out.print("Ingrese la nota del segundo corte: ");
        corte2 = entrada.nextDouble();

        System.out.print("Ingrese la nota del tercer corte: ");
        corte3 = entrada.nextDouble();

        definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40;

        System.out.println("La nota definitiva es: " + definitiva);

        entrada.close();
    }
}
```

---

## Explicación

Primero se multiplican las notas por sus porcentajes.  
Luego se suman los resultados.
