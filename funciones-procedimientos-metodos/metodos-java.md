# Métodos en Java

## Presentación

En Java, los bloques reutilizables de código se llaman **métodos**.

Los métodos permiten dividir el programa en partes más pequeñas y comprensibles.

---

# 1. Método sin parámetros y sin retorno

```java
public class MetodoSaludo {
    public static void saludar() {
        System.out.println("Hola, bienvenido");
    }

    public static void main(String[] args) {
        saludar();
    }
}
```

## Explicación

```java
public static void saludar()
```

Define un método llamado `saludar`.

`void` indica que no devuelve ningún valor.

---

# 2. Método con parámetros

```java
public class SaludoPersonalizado {
    public static void saludar(String nombre) {
        System.out.println("Hola, " + nombre);
    }

    public static void main(String[] args) {
        saludar("Ana");
        saludar("Carlos");
    }
}
```

El método recibe un dato llamado `nombre`.

---

# 3. Método con retorno

```java
public class MetodoSuma {
    public static int sumar(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int resultado = sumar(5, 3);

        System.out.println("La suma es: " + resultado);
    }
}
```

---

# 4. Método para calcular promedio

```java
public class MetodoPromedio {
    public static double calcularPromedio(double nota1, double nota2, double nota3) {
        return (nota1 + nota2 + nota3) / 3;
    }

    public static void main(String[] args) {
        double promedio = calcularPromedio(4.0, 3.5, 5.0);

        System.out.println("El promedio es: " + promedio);
    }
}
```

---

# 5. Método para validar nota

```java
public class ValidarNotaMetodo {
    public static boolean validarNota(double nota) {
        return nota >= 0.0 && nota <= 5.0;
    }

    public static void main(String[] args) {
        double nota = 4.2;

        if (validarNota(nota)) {
            System.out.println("Nota válida");
        } else {
            System.out.println("Nota no válida");
        }
    }
}
```

---

# 6. Método que recibe un arreglo

```java
public class PromedioArregloMetodo {
    public static double calcularPromedio(double[] notas) {
        double suma = 0;

        for (int i = 0; i < notas.length; i++) {
            suma = suma + notas[i];
        }

        return suma / notas.length;
    }

    public static void main(String[] args) {
        double[] notas = {4.0, 3.5, 5.0, 4.2};

        double promedio = calcularPromedio(notas);

        System.out.println("Promedio: " + promedio);
    }
}
```

---

# 7. Método para encontrar el mayor de un arreglo

```java
public class MayorArregloMetodo {
    public static int encontrarMayor(int[] numeros) {
        int mayor = numeros[0];

        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > mayor) {
                mayor = numeros[i];
            }
        }

        return mayor;
    }

    public static void main(String[] args) {
        int[] numeros = {8, 15, 3, 22, 7};

        int mayor = encontrarMayor(numeros);

        System.out.println("Mayor: " + mayor);
    }
}
```

---

# 8. Método que recibe una matriz

```java
public class SumaMatrizMetodo {
    public static int sumarMatriz(int[][] matriz) {
        int suma = 0;

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                suma = suma + matriz[fila][columna];
            }
        }

        return suma;
    }

    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6}
        };

        int suma = sumarMatriz(matriz);

        System.out.println("Suma: " + suma);
    }
}
```

---

# 9. Programa con varios métodos

```java
import java.util.Scanner;

public class SistemaNotasMetodos {
    public static boolean validarNota(double nota) {
        return nota >= 0.0 && nota <= 5.0;
    }

    public static double calcularPromedio(double[] notas) {
        double suma = 0;

        for (int i = 0; i < notas.length; i++) {
            suma = suma + notas[i];
        }

        return suma / notas.length;
    }

    public static void mostrarResultado(double promedio) {
        System.out.println("Promedio: " + promedio);

        if (promedio >= 3.0) {
            System.out.println("Aprobó");
        } else {
            System.out.println("Reprobó");
        }
    }

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[3];

        for (int i = 0; i < notas.length; i++) {
            do {
                System.out.print("Ingrese la nota " + (i + 1) + ": ");
                notas[i] = entrada.nextDouble();
            } while (!validarNota(notas[i]));
        }

        double promedio = calcularPromedio(notas);

        mostrarResultado(promedio);

        entrada.close();
    }
}
```

---

## Recomendación

Cuando un programa crece, conviene preguntarse:

```text
¿Qué parte de este código podría convertirse en un método?
```

Si una acción se repite o tiene una responsabilidad clara, probablemente puede ser un método.
