# Ordenamiento por Selección en Java

## 1. ¿Qué es el ordenamiento por selección?

El **ordenamiento por selección** consiste en buscar el menor elemento del arreglo y colocarlo en la primera posición. Luego busca el siguiente menor y lo coloca en la segunda posición, y así sucesivamente.

---

## 2. Idea básica

Arreglo inicial:

```text
[5, 3, 8, 1, 2]
```

Paso 1: buscar el menor.

```text
Menor = 1
```

Intercambiar con la primera posición:

```text
[1, 3, 8, 5, 2]
```

Paso 2: buscar el menor desde la segunda posición.

```text
Menor = 2
```

Resultado:

```text
[1, 2, 8, 5, 3]
```

Se repite hasta ordenar todo.

---

## 3. Código básico

```java
public class OrdenamientoSeleccion {
    public static void main(String[] args) {
        int[] numeros = {5, 3, 8, 1, 2};

        for (int i = 0; i < numeros.length - 1; i++) {
            int posicionMenor = i;

            for (int j = i + 1; j < numeros.length; j++) {
                if (numeros[j] < numeros[posicionMenor]) {
                    posicionMenor = j;
                }
            }

            int temporal = numeros[i];
            numeros[i] = numeros[posicionMenor];
            numeros[posicionMenor] = temporal;
        }

        System.out.println("Arreglo ordenado:");

        for (int numero : numeros) {
            System.out.println(numero);
        }
    }
}
```

---

## 4. Explicación

```java
int posicionMenor = i;
```

Se asume que el menor está en la posición actual.

```java
if (numeros[j] < numeros[posicionMenor])
```

Si se encuentra un valor menor, se actualiza la posición.

```java
numeros[i] = numeros[posicionMenor];
```

Se intercambia el menor encontrado con la posición actual.

---

## 5. Orden descendente

Para ordenar de mayor a menor, se busca el mayor.

Cambiar la condición:

```java
if (numeros[j] > numeros[posicionMayor]) {
```

---

## 6. Prueba de escritorio corta

Arreglo:

```text
[5, 3, 8, 1]
```

Primera pasada:

| i | Menor encontrado | Acción | Resultado |
|---:|---:|---|---|
| 0 | 1 | Intercambiar 5 con 1 | [1, 3, 8, 5] |

Segunda pasada:

| i | Menor encontrado | Acción | Resultado |
|---:|---:|---|---|
| 1 | 3 | No cambia | [1, 3, 8, 5] |

Tercera pasada:

| i | Menor encontrado | Acción | Resultado |
|---:|---:|---|---|
| 2 | 5 | Intercambiar 8 con 5 | [1, 3, 5, 8] |

---

## 7. Comparación con burbuja

| Aspecto | Burbuja | Selección |
|---|---|---|
| Idea | Compara vecinos | Busca el menor |
| Intercambios | Puede hacer muchos | Hace menos intercambios |
| Dificultad | Fácil | Media |
| Uso educativo | Muy útil | Muy útil |

---

## 8. Recomendación

El ordenamiento por selección ayuda a fortalecer la idea de búsqueda del menor o mayor dentro de un arreglo.
