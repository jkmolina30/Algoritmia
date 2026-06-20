# Unidad 7. Matrices en Java

## Presentación de la unidad

Una matriz es una estructura que permite organizar datos en **filas y columnas**.

Si un arreglo se puede imaginar como una lista, una matriz se puede imaginar como una tabla.

Ejemplo de matriz:

```text
[ 4.0  3.5  5.0 ]
[ 2.8  4.2  3.9 ]
[ 5.0  4.8  4.6 ]
```

Las matrices son útiles cuando necesitamos representar datos organizados en dos dimensiones.

---

## 1. ¿Qué es una matriz?

Una **matriz** es un arreglo bidimensional.

Esto significa que para acceder a un dato se necesitan dos índices:

```text
fila
columna
```

En Java:

```java
matriz[fila][columna]
```

---

## 2. Diferencia entre arreglo y matriz

| Arreglo | Matriz |
|---|---|
| Tiene una dimensión | Tiene dos dimensiones |
| Se recorre con un índice | Se recorre con dos índices |
| Ejemplo: lista de notas | Ejemplo: tabla de notas |
| `notas[i]` | `notas[fila][columna]` |

---

## 3. Declaración de una matriz

Sintaxis:

```java
tipo[][] nombreMatriz;
```

Ejemplos:

```java
int[][] numeros;
double[][] notas;
String[][] nombres;
```

---

## 4. Creación de una matriz

```java
int[][] matriz = new int[3][4];
```

Esto crea una matriz con:

```text
3 filas
4 columnas
```

---

## 5. Inicialización con valores

```java
int[][] numeros = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

Esta matriz tiene 3 filas y 3 columnas.

---

## 6. Índices en matrices

Los índices también inician en 0.

Ejemplo:

```java
int[][] numeros = {
    {10, 20, 30},
    {40, 50, 60}
};
```

| Posición | Valor |
|---|---:|
| `numeros[0][0]` | 10 |
| `numeros[0][1]` | 20 |
| `numeros[0][2]` | 30 |
| `numeros[1][0]` | 40 |
| `numeros[1][1]` | 50 |
| `numeros[1][2]` | 60 |

---

## 7. Recorrer una matriz

Para recorrer una matriz se usan dos ciclos.

```java
for (int fila = 0; fila < matriz.length; fila++) {
    for (int columna = 0; columna < matriz[fila].length; columna++) {
        System.out.print(matriz[fila][columna] + " ");
    }
    System.out.println();
}
```

---

## 8. ¿Por qué dos ciclos?

Porque una matriz tiene dos dimensiones:

- Un ciclo para las filas.
- Otro ciclo para las columnas.

El ciclo externo controla las filas.  
El ciclo interno controla las columnas.

---

## 9. Número de filas

Para conocer el número de filas:

```java
matriz.length
```

---

## 10. Número de columnas

Para conocer el número de columnas de una fila:

```java
matriz[fila].length
```

---

## 11. Llenar una matriz con datos del usuario

```java
Scanner entrada = new Scanner(System.in);

int[][] matriz = new int[3][3];

for (int fila = 0; fila < matriz.length; fila++) {
    for (int columna = 0; columna < matriz[fila].length; columna++) {
        System.out.print("Ingrese valor [" + fila + "][" + columna + "]: ");
        matriz[fila][columna] = entrada.nextInt();
    }
}
```

---

## 12. Mostrar una matriz

```java
for (int fila = 0; fila < matriz.length; fila++) {
    for (int columna = 0; columna < matriz[fila].length; columna++) {
        System.out.print(matriz[fila][columna] + "\t");
    }
    System.out.println();
}
```

`"\t"` agrega una tabulación para que los valores se vean más organizados.

---

## 13. Sumar todos los elementos

```java
int suma = 0;

for (int fila = 0; fila < matriz.length; fila++) {
    for (int columna = 0; columna < matriz[fila].length; columna++) {
        suma = suma + matriz[fila][columna];
    }
}
```

---

## 14. Sumar una fila

```java
int filaSeleccionada = 1;
int sumaFila = 0;

for (int columna = 0; columna < matriz[filaSeleccionada].length; columna++) {
    sumaFila = sumaFila + matriz[filaSeleccionada][columna];
}
```

---

## 15. Sumar una columna

```java
int columnaSeleccionada = 0;
int sumaColumna = 0;

for (int fila = 0; fila < matriz.length; fila++) {
    sumaColumna = sumaColumna + matriz[fila][columnaSeleccionada];
}
```

---

## 16. Diagonal principal

La diagonal principal aparece en matrices cuadradas.

Una matriz cuadrada tiene igual número de filas y columnas.

Ejemplo:

```text
[1]  2   3
 4  [5]  6
 7   8  [9]
```

Los elementos de la diagonal principal son:

```text
matriz[0][0]
matriz[1][1]
matriz[2][2]
```

---

## 17. Recorrer la diagonal principal

```java
for (int i = 0; i < matriz.length; i++) {
    System.out.println(matriz[i][i]);
}
```

---

## 18. Matriz transpuesta

La transpuesta de una matriz se obtiene intercambiando filas por columnas.

Ejemplo:

Matriz original:

```text
1 2 3
4 5 6
```

Matriz transpuesta:

```text
1 4
2 5
3 6
```

---

## 19. Usos de matrices

Las matrices se usan para representar:

- Tablas de datos.
- Notas por estudiante y asignatura.
- Tableros.
- Horarios.
- Mapas sencillos.
- Imágenes.
- Datos estadísticos.
- Información organizada en filas y columnas.

---

## 20. Errores comunes

- Confundir filas con columnas.
- Usar índices fuera de rango.
- Olvidar el ciclo interno.
- Usar `matriz.length` como si fuera cantidad de columnas.
- No inicializar acumuladores.
- No validar datos.

---

## Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear, llenar, recorrer y procesar matrices en Java, usando ciclos anidados, acumuladores y condicionales.
