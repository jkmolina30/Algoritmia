# Ordenamiento Burbuja en Java

## 1. ¿Qué es ordenar?

Ordenar significa organizar datos siguiendo un criterio.

Ejemplos:

- Números de menor a mayor.
- Nombres en orden alfabético.
- Notas de mayor a menor.
- Precios de menor a mayor.

---

## 2. ¿Qué es el ordenamiento burbuja?

El **ordenamiento burbuja** es un algoritmo sencillo que compara elementos vecinos y los intercambia si están en el orden incorrecto.

Se llama burbuja porque los valores más grandes van “subiendo” hacia el final del arreglo, como burbujas.

---

## 3. Idea básica

Arreglo inicial:

```text
[5, 3, 8, 1]
```

Comparaciones:

```text
5 y 3 → están mal, se intercambian
5 y 8 → están bien
8 y 1 → están mal, se intercambian
```

Después de una pasada:

```text
[3, 5, 1, 8]
```

El mayor ya quedó al final.

---

## 4. Código básico

```java
public class OrdenamientoBurbuja {
    public static void main(String[] args) {
        int[] numeros = {5, 3, 8, 1, 2};

        for (int i = 0; i < numeros.length - 1; i++) {
            for (int j = 0; j < numeros.length - 1 - i; j++) {
                if (numeros[j] > numeros[j + 1]) {
                    int temporal = numeros[j];
                    numeros[j] = numeros[j + 1];
                    numeros[j + 1] = temporal;
                }
            }
        }

        System.out.println("Arreglo ordenado:");

        for (int numero : numeros) {
            System.out.println(numero);
        }
    }
}
```

---

## 5. Explicación

```java
for (int i = 0; i < numeros.length - 1; i++)
```

Controla las pasadas generales.

```java
for (int j = 0; j < numeros.length - 1 - i; j++)
```

Compara elementos vecinos.

```java
if (numeros[j] > numeros[j + 1])
```

Verifica si están en orden incorrecto.

```java
int temporal = numeros[j];
numeros[j] = numeros[j + 1];
numeros[j + 1] = temporal;
```

Intercambia los valores.

---

## 6. ¿Por qué se usa una variable temporal?

Para no perder un valor durante el intercambio.

Ejemplo:

```text
a = 5
b = 3
```

Si hacemos:

```java
a = b;
```

Ahora `a` vale 3, pero perdimos el 5 original.

Por eso se usa:

```java
temporal = a;
a = b;
b = temporal;
```

---

## 7. Orden descendente

Para ordenar de mayor a menor, se cambia la condición:

```java
if (numeros[j] < numeros[j + 1]) {
```

---

## 8. Prueba de escritorio corta

Arreglo:

```text
[5, 3, 8, 1]
```

Primera pasada:

| Comparación | Acción | Resultado |
|---|---|---|
| 5 y 3 | Intercambia | [3, 5, 8, 1] |
| 5 y 8 | No intercambia | [3, 5, 8, 1] |
| 8 y 1 | Intercambia | [3, 5, 1, 8] |

---

## 9. Ventajas y desventajas

| Aspecto | Descripción |
|---|---|
| Ventaja | Fácil de entender |
| Ventaja | Bueno para aprender comparaciones e intercambios |
| Desventaja | Poco eficiente con muchos datos |
| Desventaja | Realiza muchas comparaciones |

---

## 10. Recomendación

El ordenamiento burbuja es ideal para aprender cómo funciona un algoritmo de ordenamiento, aunque no es el más eficiente para grandes volúmenes de datos.
