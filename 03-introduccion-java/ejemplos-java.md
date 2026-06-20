# Ejemplos Básicos en Java

## 1. Presentación

Este archivo contiene ejemplos introductorios en Java.  
Los programas son secuenciales y buscan practicar estructura básica, entrada, salida, variables y operaciones.

---

# Ejemplo 1. Mensaje de bienvenida

```java
public class Bienvenida {
    public static void main(String[] args) {
        System.out.println("Bienvenido al curso de Algoritmia y Programación");
    }
}
```

---

# Ejemplo 2. Mostrar datos del curso

```java
public class DatosCurso {
    public static void main(String[] args) {
        System.out.println("Universidad del Pacífico");
        System.out.println("Programa: Ingeniería de Sistemas");
        System.out.println("Asignatura: Algoritmia y Programación");
        System.out.println("Lenguaje: Java");
    }
}
```

---

# Ejemplo 3. Leer nombre

```java
import java.util.Scanner;

public class LeerNombre {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;

        System.out.print("Ingrese su nombre: ");
        nombre = entrada.nextLine();

        System.out.println("Hola, " + nombre);

        entrada.close();
    }
}
```

---

# Ejemplo 4. Leer edad

```java
import java.util.Scanner;

public class LeerEdad {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int edad;

        System.out.print("Ingrese su edad: ");
        edad = entrada.nextInt();

        System.out.println("La edad ingresada es: " + edad);

        entrada.close();
    }
}
```

---

# Ejemplo 5. Sumar dos números

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

# Ejemplo 6. Calcular promedio

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

# Ejemplo 7. Área de un rectángulo

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

        System.out.println("El área del rectángulo es: " + area);

        entrada.close();
    }
}
```

---

# Ejemplo 8. Uso de Math.pow

```java
import java.util.Scanner;

public class PotenciaNumero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double base;
        double exponente;
        double resultado;

        System.out.print("Ingrese la base: ");
        base = entrada.nextDouble();

        System.out.print("Ingrese el exponente: ");
        exponente = entrada.nextDouble();

        resultado = Math.pow(base, exponente);

        System.out.println("El resultado es: " + resultado);

        entrada.close();
    }
}
```

---

# Ejemplo 9. Área de un círculo

```java
import java.util.Scanner;

public class AreaCirculo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double radio;
        double area;

        System.out.print("Ingrese el radio: ");
        radio = entrada.nextDouble();

        area = Math.PI * Math.pow(radio, 2);

        System.out.println("El área del círculo es: " + area);

        entrada.close();
    }
}
```

---

# Ejemplo 10. Nombre, asignatura y nota

```java
import java.util.Scanner;

public class DatosEstudiante {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String nombre;
        String asignatura;
        double nota;

        System.out.print("Ingrese el nombre del estudiante: ");
        nombre = entrada.nextLine();

        System.out.print("Ingrese el nombre de la asignatura: ");
        asignatura = entrada.nextLine();

        System.out.print("Ingrese la nota final: ");
        nota = entrada.nextDouble();

        System.out.println("El estudiante " + nombre + " obtuvo " + nota + " en " + asignatura);

        entrada.close();
    }
}
```

---

## Recomendación

Para cada ejemplo:

1. Escribirlo manualmente.
2. Ejecutarlo.
3. Cambiar los datos.
4. Modificar los mensajes.
5. Explicar qué hace cada línea.
6. Subirlo a GitHub si corresponde.
