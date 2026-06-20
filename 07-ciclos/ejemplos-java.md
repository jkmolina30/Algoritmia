# Ejemplos en Java: Ciclos

## Presentación

Este archivo reúne ejemplos prácticos de ciclos en Java usando:

- `while`
- `do-while`
- `for`

La idea es que el estudiante comprenda cuándo usar cada ciclo.

---

# Ejemplo 1. Números del 1 al 5 con `while`

```java
public class NumerosWhile {
    public static void main(String[] args) {
        int contador = 1;

        while (contador <= 5) {
            System.out.println(contador);
            contador++;
        }
    }
}
```

---

# Ejemplo 2. Números del 1 al 5 con `do-while`

```java
public class NumerosDoWhile {
    public static void main(String[] args) {
        int contador = 1;

        do {
            System.out.println(contador);
            contador++;
        } while (contador <= 5);
    }
}
```

---

# Ejemplo 3. Números del 1 al 5 con `for`

```java
public class NumerosFor {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

---

# Ejemplo 4. Sumar números ingresados hasta escribir 0

```java
import java.util.Scanner;

public class SumarHastaCero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;
        int suma = 0;

        System.out.print("Ingrese un número, 0 para terminar: ");
        numero = entrada.nextInt();

        while (numero != 0) {
            suma = suma + numero;

            System.out.print("Ingrese otro número, 0 para terminar: ");
            numero = entrada.nextInt();
        }

        System.out.println("La suma total es: " + suma);

        entrada.close();
    }
}
```

---

# Ejemplo 5. Menú repetitivo con `do-while`

```java
import java.util.Scanner;

public class MenuRepetitivo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int opcion;

        do {
            System.out.println("===== MENÚ =====");
            System.out.println("1. Saludar");
            System.out.println("2. Mostrar curso");
            System.out.println("3. Salir");
            System.out.print("Ingrese una opción: ");
            opcion = entrada.nextInt();

            switch (opcion) {
                case 1:
                    System.out.println("Hola, bienvenido");
                    break;
                case 2:
                    System.out.println("Algoritmia y Programación");
                    break;
                case 3:
                    System.out.println("Saliendo...");
                    break;
                default:
                    System.out.println("Opción no válida");
                    break;
            }

        } while (opcion != 3);

        entrada.close();
    }
}
```

---

# Ejemplo 6. Tabla de multiplicar con `for`

```java
import java.util.Scanner;

public class TablaMultiplicar {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numero;

        System.out.print("Ingrese un número: ");
        numero = entrada.nextInt();

        for (int i = 1; i <= 10; i++) {
            System.out.println(numero + " x " + i + " = " + (numero * i));
        }

        entrada.close();
    }
}
```

---

# Ejemplo 7. Promedio de notas con `for`

```java
import java.util.Scanner;

public class PromedioNotasFor {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int cantidad;
        double nota;
        double suma = 0;
        double promedio;

        System.out.print("Ingrese la cantidad de notas: ");
        cantidad = entrada.nextInt();

        for (int i = 1; i <= cantidad; i++) {
            System.out.print("Ingrese la nota " + i + ": ");
            nota = entrada.nextDouble();

            suma = suma + nota;
        }

        promedio = suma / cantidad;

        System.out.println("El promedio es: " + promedio);

        entrada.close();
    }
}
```

---

# Ejemplo 8. Contar números pares

```java
public class ContarPares {
    public static void main(String[] args) {
        int cantidadPares = 0;

        for (int i = 1; i <= 20; i++) {
            if (i % 2 == 0) {
                cantidadPares++;
            }
        }

        System.out.println("Cantidad de pares entre 1 y 20: " + cantidadPares);
    }
}
```

---

# Ejemplo 9. Validar nota con `do-while`

```java
import java.util.Scanner;

public class ValidarNotaDoWhile {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota;

        do {
            System.out.print("Ingrese una nota entre 0.0 y 5.0: ");
            nota = entrada.nextDouble();
        } while (nota < 0.0 || nota > 5.0);

        System.out.println("Nota válida: " + nota);

        entrada.close();
    }
}
```

---

# Ejemplo 10. Adivinar número sencillo

```java
import java.util.Scanner;

public class AdivinarNumero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int numeroSecreto = 7;
        int intento;

        System.out.print("Adivine el número secreto: ");
        intento = entrada.nextInt();

        while (intento != numeroSecreto) {
            System.out.println("Número incorrecto");
            System.out.print("Intente nuevamente: ");
            intento = entrada.nextInt();
        }

        System.out.println("Correcto. Adivinaste el número.");

        entrada.close();
    }
}
```

---

## Recomendación final

Para estudiar ciclos, no basta con leer el código.  
Se debe hacer prueba de escritorio y revisar cómo cambian las variables en cada repetición.
