# Ejemplos en Java: Arreglos

## Presentación

Este archivo contiene ejemplos prácticos sobre arreglos en Java.  
Cada ejemplo está pensado para estudiantes que están iniciando en programación.

---

# Ejemplo 1. Crear y mostrar un arreglo

```java
public class ArregloNumeros {
    public static void main(String[] args) {
        int[] numeros = {10, 20, 30, 40, 50};

        for (int i = 0; i < numeros.length; i++) {
            System.out.println("Posición " + i + ": " + numeros[i]);
        }
    }
}
```

## Explicación

```java
int[] numeros = {10, 20, 30, 40, 50};
```

Crea un arreglo de enteros con cinco valores.

```java
numeros.length
```

Devuelve el tamaño del arreglo.

```java
numeros[i]
```

Accede al valor de la posición `i`.

---

# Ejemplo 2. Leer notas y mostrarlas

```java
import java.util.Scanner;

public class LeerNotas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[5];

        for (int i = 0; i < notas.length; i++) {
            System.out.print("Ingrese la nota " + (i + 1) + ": ");
            notas[i] = entrada.nextDouble();
        }

        System.out.println("Notas ingresadas:");

        for (int i = 0; i < notas.length; i++) {
            System.out.println("Nota " + (i + 1) + ": " + notas[i]);
        }

        entrada.close();
    }
}
```

---

# Ejemplo 3. Promedio de notas

```java
import java.util.Scanner;

public class PromedioNotasArreglo {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[5];
        double suma = 0;
        double promedio;

        for (int i = 0; i < notas.length; i++) {
            System.out.print("Ingrese la nota " + (i + 1) + ": ");
            notas[i] = entrada.nextDouble();

            suma = suma + notas[i];
        }

        promedio = suma / notas.length;

        System.out.println("El promedio es: " + promedio);

        entrada.close();
    }
}
```

## Explicación

La variable `suma` acumula todas las notas.  
Luego se divide entre el tamaño del arreglo.

---

# Ejemplo 4. Mayor y menor de un arreglo

```java
public class MayorMenorArreglo {
    public static void main(String[] args) {
        int[] numeros = {18, 5, 32, 7, 21};

        int mayor = numeros[0];
        int menor = numeros[0];

        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > mayor) {
                mayor = numeros[i];
            }

            if (numeros[i] < menor) {
                menor = numeros[i];
            }
        }

        System.out.println("Mayor: " + mayor);
        System.out.println("Menor: " + menor);
    }
}
```

## Explicación

Se inicia suponiendo que el primer valor es el mayor y también el menor.  
Después se comparan los demás valores.

---

# Ejemplo 5. Buscar un número

```java
import java.util.Scanner;

public class BuscarNumero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int[] numeros = {10, 25, 30, 45, 50};
        int buscado;
        boolean encontrado = false;

        System.out.print("Ingrese el número a buscar: ");
        buscado = entrada.nextInt();

        for (int i = 0; i < numeros.length; i++) {
            if (numeros[i] == buscado) {
                encontrado = true;
                System.out.println("Número encontrado en la posición: " + i);
            }
        }

        if (!encontrado) {
            System.out.println("El número no se encontró");
        }

        entrada.close();
    }
}
```

---

# Ejemplo 6. Contar aprobados y reprobados

```java
import java.util.Scanner;

public class ContarAprobados {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[5];
        int aprobados = 0;
        int reprobados = 0;

        for (int i = 0; i < notas.length; i++) {
            System.out.print("Ingrese la nota " + (i + 1) + ": ");
            notas[i] = entrada.nextDouble();

            if (notas[i] >= 3.0) {
                aprobados++;
            } else {
                reprobados++;
            }
        }

        System.out.println("Aprobados: " + aprobados);
        System.out.println("Reprobados: " + reprobados);

        entrada.close();
    }
}
```

---

# Ejemplo 7. Arreglo de nombres

```java
import java.util.Scanner;

public class ArregloNombres {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String[] nombres = new String[3];

        for (int i = 0; i < nombres.length; i++) {
            System.out.print("Ingrese el nombre " + (i + 1) + ": ");
            nombres[i] = entrada.nextLine();
        }

        System.out.println("Nombres registrados:");

        for (String nombre : nombres) {
            System.out.println(nombre);
        }

        entrada.close();
    }
}
```

---

# Ejemplo 8. Validar notas dentro de un arreglo

```java
import java.util.Scanner;

public class NotasValidadas {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double[] notas = new double[5];

        for (int i = 0; i < notas.length; i++) {
            do {
                System.out.print("Ingrese la nota " + (i + 1) + " entre 0.0 y 5.0: ");
                notas[i] = entrada.nextDouble();
            } while (notas[i] < 0.0 || notas[i] > 5.0);
        }

        System.out.println("Notas válidas ingresadas:");

        for (int i = 0; i < notas.length; i++) {
            System.out.println(notas[i]);
        }

        entrada.close();
    }
}
```

---

## Recomendación

Para dominar arreglos, el estudiante debe practicar:

- Llenar arreglos.
- Recorrer arreglos.
- Sumar valores.
- Buscar valores.
- Contar elementos.
- Encontrar mayor y menor.
