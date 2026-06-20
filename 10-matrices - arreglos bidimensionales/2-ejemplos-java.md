# Ejemplos en Java: Matrices

## Presentación

Este archivo contiene ejemplos prácticos sobre matrices en Java.

---

# Ejemplo 1. Crear y mostrar una matriz

```java
public class MostrarMatriz {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                System.out.print(matriz[fila][columna] + "\t");
            }
            System.out.println();
        }
    }
}
```

---

# Ejemplo 2. Leer una matriz 3x3

```java
import java.util.Scanner;

public class LeerMatriz {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int[][] matriz = new int[3][3];

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                System.out.print("Ingrese valor [" + fila + "][" + columna + "]: ");
                matriz[fila][columna] = entrada.nextInt();
            }
        }

        System.out.println("Matriz ingresada:");

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                System.out.print(matriz[fila][columna] + "\t");
            }
            System.out.println();
        }

        entrada.close();
    }
}
```

---

# Ejemplo 3. Sumar todos los elementos

```java
public class SumaMatriz {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int suma = 0;

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                suma = suma + matriz[fila][columna];
            }
        }

        System.out.println("La suma total es: " + suma);
    }
}
```

---

# Ejemplo 4. Mayor y menor de una matriz

```java
public class MayorMenorMatriz {
    public static void main(String[] args) {
        int[][] matriz = {
            {18, 5, 32},
            {7, 21, 9},
            {14, 3, 27}
        };

        int mayor = matriz[0][0];
        int menor = matriz[0][0];

        for (int fila = 0; fila < matriz.length; fila++) {
            for (int columna = 0; columna < matriz[fila].length; columna++) {
                if (matriz[fila][columna] > mayor) {
                    mayor = matriz[fila][columna];
                }

                if (matriz[fila][columna] < menor) {
                    menor = matriz[fila][columna];
                }
            }
        }

        System.out.println("Mayor: " + mayor);
        System.out.println("Menor: " + menor);
    }
}
```

---

# Ejemplo 5. Sumar filas

```java
public class SumaFilas {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        for (int fila = 0; fila < matriz.length; fila++) {
            int sumaFila = 0;

            for (int columna = 0; columna < matriz[fila].length; columna++) {
                sumaFila = sumaFila + matriz[fila][columna];
            }

            System.out.println("Suma fila " + fila + ": " + sumaFila);
        }
    }
}
```

---

# Ejemplo 6. Sumar columnas

```java
public class SumaColumnas {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int columnas = matriz[0].length;

        for (int columna = 0; columna < columnas; columna++) {
            int sumaColumna = 0;

            for (int fila = 0; fila < matriz.length; fila++) {
                sumaColumna = sumaColumna + matriz[fila][columna];
            }

            System.out.println("Suma columna " + columna + ": " + sumaColumna);
        }
    }
}
```

---

# Ejemplo 7. Diagonal principal

```java
public class DiagonalPrincipal {
    public static void main(String[] args) {
        int[][] matriz = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        System.out.println("Diagonal principal:");

        for (int i = 0; i < matriz.length; i++) {
            System.out.println(matriz[i][i]);
        }
    }
}
```

---

# Ejemplo 8. Promedio de notas por estudiante

```java
import java.util.Scanner;

public class PromedioNotasMatriz {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int estudiantes = 3;
        int notasPorEstudiante = 3;

        double[][] notas = new double[estudiantes][notasPorEstudiante];

        for (int fila = 0; fila < notas.length; fila++) {
            System.out.println("Estudiante " + (fila + 1));

            for (int columna = 0; columna < notas[fila].length; columna++) {
                System.out.print("Ingrese nota " + (columna + 1) + ": ");
                notas[fila][columna] = entrada.nextDouble();
            }
        }

        for (int fila = 0; fila < notas.length; fila++) {
            double suma = 0;

            for (int columna = 0; columna < notas[fila].length; columna++) {
                suma = suma + notas[fila][columna];
            }

            double promedio = suma / notas[fila].length;

            System.out.println("Promedio estudiante " + (fila + 1) + ": " + promedio);
        }

        entrada.close();
    }
}
```

---

## Recomendación

Para trabajar matrices es importante hacer una prueba de escritorio pequeña, por ejemplo con matrices de 2x2, antes de pasar a matrices más grandes.
