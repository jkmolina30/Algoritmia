# Búsqueda Binaria en Java

## 1. ¿Qué es la búsqueda binaria?

La **búsqueda binaria** es un algoritmo eficiente para encontrar un dato dentro de una lista ordenada.

A diferencia de la búsqueda secuencial, no revisa elemento por elemento desde el inicio.  
La búsqueda binaria divide el conjunto de datos en mitades.

---

## 2. Condición importante

Para usar búsqueda binaria, los datos deben estar ordenados.

Ejemplo válido:

```text
[5, 10, 15, 20, 25, 30, 35]
```

Ejemplo no válido:

```text
[20, 5, 35, 10, 25]
```

Si los datos no están ordenados, la búsqueda binaria puede dar resultados incorrectos.

---

## 3. Idea básica

Supongamos que buscamos el número 25 en este arreglo:

```text
[5, 10, 15, 20, 25, 30, 35]
```

La búsqueda revisa el centro.

Centro inicial:

```text
20
```

Como 25 es mayor que 20, se descarta la mitad izquierda.

Ahora se busca en:

```text
[25, 30, 35]
```

Centro:

```text
30
```

Como 25 es menor que 30, se descarta la mitad derecha.

Ahora queda:

```text
[25]
```

Encontrado.

---

## 4. Variables necesarias

| Variable | Función |
|---|---|
| `inicio` | Marca el inicio del rango de búsqueda |
| `fin` | Marca el final del rango |
| `medio` | Posición central |
| `buscado` | Valor que se desea encontrar |
| `encontrado` | Indica si se encontró el dato |

---

## 5. Código básico

```java
public class BusquedaBinaria {
    public static void main(String[] args) {
        int[] numeros = {5, 10, 15, 20, 25, 30, 35};

        int buscado = 25;
        int inicio = 0;
        int fin = numeros.length - 1;
        int posicion = -1;

        while (inicio <= fin) {
            int medio = (inicio + fin) / 2;

            if (numeros[medio] == buscado) {
                posicion = medio;
                break;
            } else if (buscado > numeros[medio]) {
                inicio = medio + 1;
            } else {
                fin = medio - 1;
            }
        }

        if (posicion != -1) {
            System.out.println("Número encontrado en la posición: " + posicion);
        } else {
            System.out.println("Número no encontrado");
        }
    }
}
```

---

## 6. Explicación paso a paso

```java
int inicio = 0;
```

La búsqueda inicia en la primera posición.

```java
int fin = numeros.length - 1;
```

El final es la última posición.

```java
int medio = (inicio + fin) / 2;
```

Calcula la posición central.

```java
if (numeros[medio] == buscado)
```

Verifica si el valor del centro es el que buscamos.

```java
inicio = medio + 1;
```

Busca en la mitad derecha.

```java
fin = medio - 1;
```

Busca en la mitad izquierda.

---

## 7. Ejemplo con Scanner

```java
import java.util.Scanner;

public class BuscarBinarioScanner {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int[] numeros = {5, 10, 15, 20, 25, 30, 35};

        int buscado;
        int inicio = 0;
        int fin = numeros.length - 1;
        int posicion = -1;

        System.out.print("Ingrese el número a buscar: ");
        buscado = entrada.nextInt();

        while (inicio <= fin) {
            int medio = (inicio + fin) / 2;

            if (numeros[medio] == buscado) {
                posicion = medio;
                break;
            } else if (buscado > numeros[medio]) {
                inicio = medio + 1;
            } else {
                fin = medio - 1;
            }
        }

        if (posicion != -1) {
            System.out.println("Número encontrado en la posición: " + posicion);
        } else {
            System.out.println("Número no encontrado");
        }

        entrada.close();
    }
}
```

---

## 8. Prueba de escritorio

Arreglo:

```text
[5, 10, 15, 20, 25, 30, 35]
```

Buscado:

```text
25
```

| inicio | fin | medio | numeros[medio] | Acción |
|---:|---:|---:|---:|---|
| 0 | 6 | 3 | 20 | Buscar derecha |
| 4 | 6 | 5 | 30 | Buscar izquierda |
| 4 | 4 | 4 | 25 | Encontrado |

---

## 9. Ventajas y desventajas

| Aspecto | Descripción |
|---|---|
| Ventaja | Es más rápida que la búsqueda secuencial en listas grandes |
| Ventaja | Reduce el espacio de búsqueda en cada paso |
| Desventaja | Requiere datos ordenados |
| Desventaja | Es más difícil de entender al inicio |

---

## 10. Comparación con búsqueda secuencial

| Aspecto | Secuencial | Binaria |
|---|---|---|
| Requiere orden | No | Sí |
| Revisa | Uno por uno | Por mitades |
| Dificultad | Baja | Media |
| Eficiencia | Menor | Mayor |

---

## 11. Recomendación

Usa búsqueda binaria cuando los datos ya estén ordenados.  
Si los datos no están ordenados, primero deben ordenarse o se debe usar búsqueda secuencial.
