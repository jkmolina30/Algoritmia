# Búsqueda Secuencial en Java

## 1. ¿Qué es buscar?

Buscar significa revisar un conjunto de datos para encontrar un valor específico.

Ejemplos:

- Buscar un nombre en una lista.
- Buscar una nota en un arreglo.
- Buscar un producto en un inventario.
- Buscar una edad en un conjunto de datos.

---

## 2. ¿Qué es la búsqueda secuencial?

La **búsqueda secuencial** consiste en revisar los elementos uno por uno, desde el inicio hasta el final, hasta encontrar el dato buscado o hasta terminar la lista.

También se conoce como búsqueda lineal.

---

## 3. Idea básica

Supongamos que tenemos este arreglo:

```java
int[] numeros = {10, 25, 8, 40, 15};
```

Queremos buscar el número `40`.

El programa revisa:

```text
10 → no es 40
25 → no es 40
8  → no es 40
40 → encontrado
```

---

## 4. ¿Cuándo usar búsqueda secuencial?

Se puede usar cuando:

- La lista no está ordenada.
- La cantidad de datos es pequeña.
- Se necesita una solución sencilla.
- No se conoce otra estructura de búsqueda.

---

## 5. Código básico

```java
public class BusquedaSecuencial {
    public static void main(String[] args) {
        int[] numeros = {10, 25, 8, 40, 15};

        int buscado = 40;
        boolean encontrado = false;

        for (int i = 0; i < numeros.length; i++) {
            if (numeros[i] == buscado) {
                encontrado = true;
                System.out.println("Número encontrado en la posición: " + i);
            }
        }

        if (!encontrado) {
            System.out.println("Número no encontrado");
        }
    }
}
```

---

## 6. Explicación

```java
boolean encontrado = false;
```

Al inicio asumimos que el número no ha sido encontrado.

```java
for (int i = 0; i < numeros.length; i++)
```

Recorre todas las posiciones del arreglo.

```java
if (numeros[i] == buscado)
```

Compara cada elemento con el número buscado.

---

## 7. Detener la búsqueda con `break`

Si solo necesitamos encontrar la primera aparición, podemos detener el ciclo.

```java
for (int i = 0; i < numeros.length; i++) {
    if (numeros[i] == buscado) {
        encontrado = true;
        posicion = i;
        break;
    }
}
```

`break` termina el ciclo inmediatamente.

---

## 8. Ejemplo completo con Scanner

```java
import java.util.Scanner;

public class BuscarNumero {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        int[] numeros = {10, 25, 8, 40, 15};

        int buscado;
        boolean encontrado = false;
        int posicion = -1;

        System.out.print("Ingrese el número a buscar: ");
        buscado = entrada.nextInt();

        for (int i = 0; i < numeros.length; i++) {
            if (numeros[i] == buscado) {
                encontrado = true;
                posicion = i;
                break;
            }
        }

        if (encontrado) {
            System.out.println("Número encontrado en la posición: " + posicion);
        } else {
            System.out.println("Número no encontrado");
        }

        entrada.close();
    }
}
```

---

## 9. Búsqueda de texto

Para buscar textos se usa `.equalsIgnoreCase()`.

```java
if (nombres[i].equalsIgnoreCase(buscado)) {
    encontrado = true;
}
```

Ejemplo:

```java
import java.util.Scanner;

public class BuscarNombre {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        String[] nombres = {"Ana", "Carlos", "María", "Luis"};

        String buscado;
        boolean encontrado = false;

        System.out.print("Ingrese el nombre a buscar: ");
        buscado = entrada.nextLine();

        for (int i = 0; i < nombres.length; i++) {
            if (nombres[i].equalsIgnoreCase(buscado)) {
                encontrado = true;
                System.out.println("Nombre encontrado en la posición: " + i);
                break;
            }
        }

        if (!encontrado) {
            System.out.println("Nombre no encontrado");
        }

        entrada.close();
    }
}
```

---

## 10. Ventajas y desventajas

| Aspecto | Descripción |
|---|---|
| Ventaja | Es fácil de entender e implementar |
| Ventaja | Funciona aunque los datos no estén ordenados |
| Desventaja | Puede ser lenta con muchos datos |
| Desventaja | En el peor caso revisa todos los elementos |

---

## 11. Prueba de escritorio

Arreglo:

```text
[10, 25, 8, 40, 15]
```

Dato buscado:

```text
40
```

| i | numeros[i] | ¿Es 40? | encontrado |
|---:|---:|---|---|
| 0 | 10 | No | false |
| 1 | 25 | No | false |
| 2 | 8 | No | false |
| 3 | 40 | Sí | true |

---

## 12. Recomendación

La búsqueda secuencial es una buena primera técnica para aprender búsqueda, porque permite comprender claramente cómo se recorren los datos.
