# Unidad 6. Arreglos en Java

## Presentación de la unidad

Hasta este momento se han trabajado variables simples. Una variable simple permite guardar un solo dato.

Ejemplo:

```java
double nota = 4.2;
```

Pero en muchos problemas necesitamos guardar varios datos del mismo tipo.

Ejemplo:

```text
Notas de 10 estudiantes
Edades de 20 personas
Precios de 15 productos
Nombres de varios estudiantes
```

Para estos casos se utilizan los **arreglos**.

---

## 1. ¿Qué es un arreglo?

Un **arreglo** es una estructura que permite almacenar varios datos del mismo tipo usando un solo nombre.

En palabras sencillas, un arreglo es como una fila de casillas donde cada casilla guarda un dato.

Ejemplo:

```text
notas = [4.0, 3.5, 5.0, 2.8, 4.3]
```

Todas esas notas están guardadas dentro de una misma estructura llamada `notas`.

---

## 2. ¿Por qué usar arreglos?

Sin arreglos, si queremos guardar cinco notas, tendríamos que hacer esto:

```java
double nota1;
double nota2;
double nota3;
double nota4;
double nota5;
```

Con arreglos, podemos hacer esto:

```java
double[] notas = new double[5];
```

Esto crea un arreglo llamado `notas` con espacio para cinco valores `double`.

---

## 3. Características de los arreglos en Java

Los arreglos en Java tienen estas características:

| Característica | Explicación |
|---|---|
| Tienen tamaño fijo | Una vez creado, su tamaño no cambia |
| Guardan datos del mismo tipo | Todos los elementos deben ser del mismo tipo |
| Usan índices | Cada posición se identifica con un número |
| El primer índice es 0 | La primera posición no es 1, sino 0 |
| Se recorren comúnmente con ciclos | Especialmente con `for` |

---

## 4. Índices de un arreglo

En Java los arreglos empiezan en la posición 0.

Ejemplo:

```java
int[] numeros = {10, 20, 30, 40, 50};
```

| Índice | Valor |
|---:|---:|
| 0 | 10 |
| 1 | 20 |
| 2 | 30 |
| 3 | 40 |
| 4 | 50 |

Para acceder al primer elemento:

```java
numeros[0]
```

Para acceder al último elemento:

```java
numeros[4]
```

---

## 5. Declaración de un arreglo

Declarar un arreglo significa indicar que se va a crear una estructura para almacenar varios datos.

Sintaxis general:

```java
tipo[] nombreArreglo;
```

Ejemplos:

```java
int[] edades;
double[] notas;
String[] nombres;
```

---

## 6. Creación de un arreglo

Después de declarar un arreglo, se puede crear con `new`.

```java
int[] edades = new int[5];
```

Esto crea un arreglo de enteros con 5 posiciones.

---

## 7. Declarar e inicializar con valores

También se puede crear un arreglo con valores iniciales:

```java
int[] numeros = {10, 20, 30, 40, 50};
```

En este caso, Java entiende que el arreglo tiene 5 elementos.

---

## 8. Asignar valores a un arreglo

Para guardar un valor en una posición se usa el índice.

```java
notas[0] = 4.0;
notas[1] = 3.5;
notas[2] = 5.0;
```

Lectura sencilla:

```text
En la posición 0 del arreglo notas se guarda 4.0.
En la posición 1 se guarda 3.5.
En la posición 2 se guarda 5.0.
```

---

## 9. Leer valores de un arreglo

Para obtener un valor también se usa el índice.

```java
System.out.println(notas[0]);
```

Esto muestra el primer valor del arreglo.

---

## 10. Tamaño de un arreglo

En Java se usa `.length` para conocer el tamaño del arreglo.

```java
notas.length
```

Ejemplo:

```java
double[] notas = new double[5];

System.out.println(notas.length);
```

Salida:

```text
5
```

---

## 11. Recorrer un arreglo

Recorrer un arreglo significa visitar cada una de sus posiciones.

La forma más común es usar un ciclo `for`.

```java
for (int i = 0; i < notas.length; i++) {
    System.out.println(notas[i]);
}
```

Explicación:

- `i = 0`: inicia en la primera posición.
- `i < notas.length`: se repite mientras `i` sea menor que el tamaño.
- `i++`: avanza a la siguiente posición.
- `notas[i]`: accede al valor de la posición actual.

---

## 12. Llenar un arreglo con datos del usuario

```java
Scanner entrada = new Scanner(System.in);

double[] notas = new double[5];

for (int i = 0; i < notas.length; i++) {
    System.out.print("Ingrese la nota " + (i + 1) + ": ");
    notas[i] = entrada.nextDouble();
}
```

Se usa `(i + 1)` para mostrar al usuario una numeración más natural: nota 1, nota 2, nota 3.

Internamente el arreglo sigue usando índices desde 0.

---

## 13. Mostrar los elementos de un arreglo

```java
for (int i = 0; i < notas.length; i++) {
    System.out.println("Nota " + (i + 1) + ": " + notas[i]);
}
```

---

## 14. Sumar los valores de un arreglo

```java
double suma = 0;

for (int i = 0; i < notas.length; i++) {
    suma = suma + notas[i];
}
```

La variable `suma` es un acumulador.

---

## 15. Calcular promedio

```java
double promedio = suma / notas.length;
```

El promedio se obtiene dividiendo la suma entre la cantidad de elementos.

---

## 16. Buscar un elemento

Buscar significa revisar si un dato está dentro del arreglo.

```java
int buscado = 30;
boolean encontrado = false;

for (int i = 0; i < numeros.length; i++) {
    if (numeros[i] == buscado) {
        encontrado = true;
    }
}
```

---

## 17. Encontrar el mayor

```java
int mayor = numeros[0];

for (int i = 1; i < numeros.length; i++) {
    if (numeros[i] > mayor) {
        mayor = numeros[i];
    }
}
```

Se inicia suponiendo que el primer elemento es el mayor.  
Luego se compara con los demás.

---

## 18. Encontrar el menor

```java
int menor = numeros[0];

for (int i = 1; i < numeros.length; i++) {
    if (numeros[i] < menor) {
        menor = numeros[i];
    }
}
```

---

## 19. Error común: salir del rango

Si un arreglo tiene 5 posiciones, los índices válidos son:

```text
0, 1, 2, 3, 4
```

Este acceso es incorrecto:

```java
notas[5]
```

Genera un error porque la posición 5 no existe.

El error se conoce como:

```text
ArrayIndexOutOfBoundsException
```

---

## 20. Arreglo de textos

También se pueden crear arreglos de `String`.

```java
String[] nombres = new String[3];

nombres[0] = "Ana";
nombres[1] = "Carlos";
nombres[2] = "María";
```

---

## 21. Arreglo con ciclo mejorado `for-each`

Java permite recorrer arreglos de forma más simple cuando solo se necesita leer los valores.

```java
for (String nombre : nombres) {
    System.out.println(nombre);
}
```

Lectura sencilla:

```text
Para cada nombre dentro del arreglo nombres, mostrar el nombre.
```

---

## 22. Cuándo usar arreglos

Usa arreglos cuando:

- Necesitas guardar varios datos del mismo tipo.
- Sabes cuántos datos vas a manejar.
- Necesitas recorrer datos.
- Necesitas calcular sumas, promedios, mayores o menores.
- Necesitas buscar valores.

---

## 23. Diferencia entre variable simple y arreglo

| Variable simple | Arreglo |
|---|---|
| Guarda un solo dato | Guarda varios datos |
| Ejemplo: `nota` | Ejemplo: `notas[]` |
| No usa índice | Usa índices |
| Es más sencilla | Permite manejar listas |

---

## 24. Recomendaciones

- Recordar que los índices inician en 0.
- Usar `.length` en lugar de escribir el tamaño manualmente.
- Validar datos cuando sea necesario.
- Usar nombres claros para los arreglos.
- Inicializar acumuladores antes de usarlos.
- Tener cuidado con los límites del arreglo.
- Hacer prueba de escritorio.

---

## Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder declarar, crear, llenar, recorrer y procesar arreglos en Java, aplicando ciclos, acumuladores, contadores, búsquedas y cálculos básicos.
