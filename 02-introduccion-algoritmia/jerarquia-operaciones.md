# Jerarquía de Operaciones y Orden de Evaluación

## Unidad 2. Introducción a la Algoritmia

Este archivo explica la **jerarquía de operaciones**, también conocida como **orden de las operaciones** o **precedencia de operadores**.

Este tema es fundamental en algoritmia y programación porque permite comprender en qué orden se resuelven las operaciones matemáticas dentro de una expresión.

Cuando un algoritmo o programa tiene una expresión como:

```text
resultado = 8 + 4 * 2
```

no se resuelve necesariamente de izquierda a derecha. Primero se aplica la jerarquía de operaciones.

---

## 1. ¿Qué es la jerarquía de operaciones?

La **jerarquía de operaciones** es el conjunto de reglas que indica qué operaciones deben resolverse primero dentro de una expresión matemática.

En palabras sencillas, es el orden que se debe seguir para calcular correctamente una expresión.

Por ejemplo:

```text
8 + 4 * 2
```

Si se resolviera de izquierda a derecha:

```text
8 + 4 = 12
12 * 2 = 24
```

Pero ese resultado no es correcto según la jerarquía.

La multiplicación tiene mayor prioridad que la suma, por eso se resuelve primero:

```text
4 * 2 = 8
8 + 8 = 16
```

Resultado correcto:

```text
16
```

---

## 2. ¿Por qué es importante en programación?

En programación, los computadores también siguen reglas de prioridad cuando evalúan expresiones.

Si el programador no conoce estas reglas, puede escribir una fórmula que aparentemente está bien, pero que produce un resultado incorrecto.

Ejemplo:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

A simple vista parece que calcula el promedio de tres notas.  
Sin embargo, Java primero divide `nota3 / 3` y después suma `nota1 + nota2`.

La forma correcta es:

```java
promedio = (nota1 + nota2 + nota3) / 3;
```

Los paréntesis obligan a que primero se sumen las tres notas y luego se divida entre 3.

---

## 3. Orden general de las operaciones

El orden más común es:

| Prioridad | Operación | Ejemplo |
|---:|---|---|
| 1 | Paréntesis | `(5 + 3)` |
| 2 | Potencias y raíces | `2^3`, `√9` |
| 3 | Multiplicación, división y módulo | `4 * 2`, `10 / 2`, `10 % 3` |
| 4 | Suma y resta | `8 + 2`, `9 - 5` |

En programación, especialmente en Java, también existen operadores relacionales y lógicos. Sin embargo, en esta unidad nos enfocaremos principalmente en operadores aritméticos.

---

## 4. Regla principal

La regla principal es:

```text
Primero se resuelven los paréntesis.
Luego las potencias o raíces.
Después multiplicaciones y divisiones.
Finalmente sumas y restas.
```

Cuando hay operaciones con la misma prioridad, normalmente se resuelven de izquierda a derecha.

Ejemplo:

```text
20 / 5 * 2
```

División y multiplicación tienen la misma prioridad. Entonces se resuelve de izquierda a derecha:

```text
20 / 5 = 4
4 * 2 = 8
```

Resultado:

```text
8
```

---

## 5. Uso de paréntesis

Los paréntesis permiten cambiar o aclarar el orden de evaluación.

Ejemplo 1:

```text
8 + 4 * 2
```

Primero se multiplica:

```text
4 * 2 = 8
8 + 8 = 16
```

Resultado:

```text
16
```

Ejemplo 2:

```text
(8 + 4) * 2
```

Primero se resuelve el paréntesis:

```text
8 + 4 = 12
12 * 2 = 24
```

Resultado:

```text
24
```

Aunque las expresiones tienen los mismos números y operadores, el resultado cambia por el uso de paréntesis.

---

## 6. Paréntesis anidados

Los paréntesis anidados son paréntesis dentro de otros paréntesis.

Ejemplo:

```text
(10 + (6 * 2)) / 2
```

Primero se resuelve el paréntesis más interno:

```text
6 * 2 = 12
```

Luego:

```text
10 + 12 = 22
```

Finalmente:

```text
22 / 2 = 11
```

Resultado:

```text
11
```

---

## 7. Multiplicación y división

La multiplicación y la división tienen la misma prioridad.

Cuando aparecen juntas, se resuelven de izquierda a derecha.

Ejemplo:

```text
24 / 6 * 3
```

Paso 1:

```text
24 / 6 = 4
```

Paso 2:

```text
4 * 3 = 12
```

Resultado:

```text
12
```

No se debe multiplicar primero solo porque aparece una multiplicación.  
Como multiplicación y división tienen la misma prioridad, se respeta el orden de izquierda a derecha.

---

## 8. Suma y resta

La suma y la resta tienen la misma prioridad.

Cuando aparecen juntas, se resuelven de izquierda a derecha.

Ejemplo:

```text
15 - 5 + 2
```

Paso 1:

```text
15 - 5 = 10
```

Paso 2:

```text
10 + 2 = 12
```

Resultado:

```text
12
```

---

## 9. Potencias en PSeInt

En PSeInt se puede usar el operador `^` para representar potencias.

Ejemplo:

```pseint
resultado <- 2 ^ 3
```

Esto significa:

```text
2 elevado a 3
```

Resultado:

```text
8
```

---

## 10. Potencias en Java

En Java no se usa el símbolo `^` para calcular potencias.

Esto es muy importante.

En Java, el símbolo `^` no significa potencia aritmética como en matemáticas escolares o PSeInt. En Java, `^` es un operador bit a bit.

Para calcular potencias en Java se usa:

```java
Math.pow(base, exponente)
```

Ejemplo:

```java
double resultado = Math.pow(2, 3);
```

Resultado:

```text
8.0
```

---

## 11. Diferencia entre PSeInt y Java con potencias

| Operación | PSeInt | Java |
|---|---|---|
| 2 elevado a 3 | `2 ^ 3` | `Math.pow(2, 3)` |

Ejemplo en PSeInt:

```pseint
Algoritmo PotenciaPSeInt
    Definir resultado Como Real

    resultado <- 2 ^ 3

    Escribir "El resultado es: ", resultado
FinAlgoritmo
```

Ejemplo en Java:

```java
public class PotenciaJava {
    public static void main(String[] args) {
        double resultado;

        resultado = Math.pow(2, 3);

        System.out.println("El resultado es: " + resultado);
    }
}
```

---

## 12. El operador módulo

El operador módulo permite obtener el residuo de una división.

En Java se usa el símbolo:

```java
%
```

Ejemplo:

```java
int residuo = 10 % 3;
```

La división de 10 entre 3 da 3 y sobra 1.

Por eso:

```text
10 % 3 = 1
```

El módulo es muy usado para saber si un número es par o impar.

Ejemplo:

```java
int residuo = numero % 2;
```

Si el residuo es 0, el número es par.  
Si el residuo es diferente de 0, el número es impar.

Este análisis se trabajará con más detalle en la unidad de condicionales.

---

## 13. Jerarquía aritmética en Java

En Java, las operaciones aritméticas básicas siguen este orden:

| Prioridad | Operadores | Descripción |
|---:|---|---|
| 1 | `()` | Paréntesis |
| 2 | `*`, `/`, `%` | Multiplicación, división y módulo |
| 3 | `+`, `-` | Suma y resta |

Java no tiene operador aritmético directo para potencia usando `^`.  
Para potencias se usa `Math.pow()`.

---

## 14. Ejemplo explicado paso a paso

Expresión:

```text
6 + 4 * 3 - 8 / 2
```

Paso 1: resolver multiplicación.

```text
4 * 3 = 12
```

La expresión queda:

```text
6 + 12 - 8 / 2
```

Paso 2: resolver división.

```text
8 / 2 = 4
```

La expresión queda:

```text
6 + 12 - 4
```

Paso 3: resolver suma y resta de izquierda a derecha.

```text
6 + 12 = 18
18 - 4 = 14
```

Resultado:

```text
14
```

---

## 15. Ejemplo con paréntesis

Expresión:

```text
(6 + 4) * (3 - 1)
```

Paso 1: resolver primer paréntesis.

```text
6 + 4 = 10
```

Paso 2: resolver segundo paréntesis.

```text
3 - 1 = 2
```

Paso 3: multiplicar.

```text
10 * 2 = 20
```

Resultado:

```text
20
```

---

## 16. Ejemplo con promedio

Problema:

Calcular el promedio de tres notas:

```text
nota1 = 4.0
nota2 = 3.5
nota3 = 5.0
```

Expresión correcta:

```text
promedio = (nota1 + nota2 + nota3) / 3
```

Paso 1:

```text
4.0 + 3.5 + 5.0 = 12.5
```

Paso 2:

```text
12.5 / 3 = 4.166
```

Resultado:

```text
4.166
```

Expresión incorrecta:

```text
promedio = nota1 + nota2 + nota3 / 3
```

Paso 1:

```text
5.0 / 3 = 1.666
```

Paso 2:

```text
4.0 + 3.5 + 1.666 = 9.166
```

Resultado incorrecto:

```text
9.166
```

Conclusión:

Los paréntesis son necesarios cuando se desea cambiar el orden natural de las operaciones.

---

## 17. Ejemplo en PSeInt

### Problema

Leer tres notas y calcular el promedio correctamente usando paréntesis.

```pseint
Algoritmo PromedioConParentesis
    Definir nota1, nota2, nota3, promedio Como Real

    Escribir "Ingrese la primera nota:"
    Leer nota1

    Escribir "Ingrese la segunda nota:"
    Leer nota2

    Escribir "Ingrese la tercera nota:"
    Leer nota3

    promedio <- (nota1 + nota2 + nota3) / 3

    Escribir "El promedio es: ", promedio
FinAlgoritmo
```

---

## 18. Ejemplo en Java

### Problema

Leer tres notas y calcular el promedio correctamente usando paréntesis.

```java
import java.util.Scanner;

public class PromedioConParentesis {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        double nota1;
        double nota2;
        double nota3;
        double promedio;

        System.out.print("Ingrese la primera nota: ");
        nota1 = entrada.nextDouble();

        System.out.print("Ingrese la segunda nota: ");
        nota2 = entrada.nextDouble();

        System.out.print("Ingrese la tercera nota: ");
        nota3 = entrada.nextDouble();

        promedio = (nota1 + nota2 + nota3) / 3;

        System.out.println("El promedio es: " + promedio);

        entrada.close();
    }
}
```

---

## 19. División entera en Java

En Java, cuando se dividen dos números enteros, el resultado también será entero.

Ejemplo:

```java
int resultado = 5 / 2;
```

El resultado será:

```text
2
```

No será:

```text
2.5
```

Esto ocurre porque `5` y `2` son enteros.

Para obtener decimales, al menos uno de los valores debe ser decimal.

Ejemplo:

```java
double resultado = 5.0 / 2;
```

Resultado:

```text
2.5
```

También puede hacerse:

```java
double resultado = (double) 5 / 2;
```

---

## 20. Error común con división entera

Código:

```java
int nota1 = 4;
int nota2 = 5;
int nota3 = 4;

double promedio = (nota1 + nota2 + nota3) / 3;
```

Aunque `promedio` es `double`, la operación:

```java
(nota1 + nota2 + nota3) / 3
```

se hace primero con enteros.

```text
13 / 3 = 4
```

Resultado:

```text
4.0
```

Para obtener el promedio decimal:

```java
double promedio = (nota1 + nota2 + nota3) / 3.0;
```

Resultado:

```text
4.333333333333333
```

---

## 21. Expresiones aritméticas en algoritmia

En algoritmia, una expresión aritmética combina:

- Variables.
- Números.
- Operadores.
- Paréntesis.

Ejemplo:

```text
total = precio * cantidad + domicilio
```

Si el precio es 2000, la cantidad es 3 y el domicilio es 5000:

```text
total = 2000 * 3 + 5000
total = 6000 + 5000
total = 11000
```

---

## 22. Buenas prácticas

Para evitar errores:

1. Usar paréntesis cuando la expresión pueda generar duda.
2. Revisar la fórmula antes de programar.
3. Hacer prueba de escritorio.
4. Probar con datos sencillos.
5. Verificar si se necesitan resultados decimales.
6. En Java, tener cuidado con la división entre enteros.
7. No usar `^` como potencia en Java.
8. Usar nombres de variables claros.

---

## 23. Ejercicios resueltos

### Ejercicio 1

Resolver:

```text
8 + 2 * 5
```

Solución:

```text
2 * 5 = 10
8 + 10 = 18
```

Resultado:

```text
18
```

---

### Ejercicio 2

Resolver:

```text
(8 + 2) * 5
```

Solución:

```text
8 + 2 = 10
10 * 5 = 50
```

Resultado:

```text
50
```

---

### Ejercicio 3

Resolver:

```text
20 - 12 / 4 + 3
```

Solución:

```text
12 / 4 = 3
20 - 3 + 3
17 + 3 = 20
```

Resultado:

```text
20
```

---

### Ejercicio 4

Resolver:

```text
6 + 4 * 3 - 8 / 2
```

Solución:

```text
4 * 3 = 12
8 / 2 = 4
6 + 12 - 4 = 14
```

Resultado:

```text
14
```

---

### Ejercicio 5

Resolver:

```text
(6 + 4) * (3 - 1)
```

Solución:

```text
6 + 4 = 10
3 - 1 = 2
10 * 2 = 20
```

Resultado:

```text
20
```

---

## 24. Ejercicios propuestos

Resuelve las siguientes expresiones aplicando la jerarquía de operaciones.

### Nivel básico

1. `5 + 3 * 2`
2. `10 - 4 / 2`
3. `8 + 6 / 3`
4. `7 * 2 + 5`
5. `20 / 5 + 6`

### Nivel intermedio

6. `(5 + 3) * 2`
7. `10 - (4 / 2)`
8. `(8 + 6) / 2`
9. `7 * (2 + 5)`
10. `(20 / 5) + 6`

### Nivel aplicado

11. `6 + 4 * 3 - 8 / 2`
12. `(6 + 4) * 3 - 8 / 2`
13. `30 / 5 * 2 + 4`
14. `50 - 10 * 3 + 8`
15. `(50 - 10) * (3 + 8)`

---

## 25. Ejercicios para PSeInt

Diseña algoritmos en PSeInt para resolver los siguientes problemas.

### Ejercicio 1

Leer tres números y calcular:

```text
resultado = (num1 + num2) * num3
```

---

### Ejercicio 2

Leer tres notas y calcular el promedio correctamente.

```text
promedio = (nota1 + nota2 + nota3) / 3
```

---

### Ejercicio 3

Leer el precio de un producto, la cantidad y el valor del domicilio. Calcular:

```text
total = precio * cantidad + domicilio
```

---

### Ejercicio 4

Leer la base y la altura de un triángulo. Calcular:

```text
area = (base * altura) / 2
```

---

### Ejercicio 5

Leer el radio de un círculo. Calcular:

```text
area = 3.1416 * radio ^ 2
```

---

## 26. Ejercicios para Java

Crea programas en Java para resolver los siguientes problemas.

### Ejercicio 1

Leer tres números y calcular:

```text
resultado = (num1 + num2) * num3
```

---

### Ejercicio 2

Leer tres notas y calcular el promedio correctamente.

```text
promedio = (nota1 + nota2 + nota3) / 3
```

---

### Ejercicio 3

Leer el precio de un producto, la cantidad y el valor del domicilio. Calcular:

```text
total = precio * cantidad + domicilio
```

---

### Ejercicio 4

Leer la base y la altura de un triángulo. Calcular:

```text
area = (base * altura) / 2
```

---

### Ejercicio 5

Leer el radio de un círculo. Calcular el área usando `Math.pow`.

```text
area = 3.1416 * radio elevado a 2
```

En Java:

```java
area = 3.1416 * Math.pow(radio, 2);
```

---

## 27. Mini reto

Crear un programa en Java y otro en PSeInt para calcular la nota definitiva de una asignatura.

El programa debe leer:

- Nota del primer corte.
- Nota del segundo corte.
- Nota del tercer corte.

La fórmula es:

```text
definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40
```

Luego debe mostrar la nota definitiva.

---

## 28. Checklist de aprendizaje

Al finalizar este archivo, el estudiante debe poder responder:

- [ ] ¿Qué es la jerarquía de operaciones?
- [ ] ¿Qué operación se resuelve primero?
- [ ] ¿Para qué sirven los paréntesis?
- [ ] ¿Qué diferencia hay entre `2 ^ 3` en PSeInt y Java?
- [ ] ¿Cómo se calcula una potencia en Java?
- [ ] ¿Qué hace el operador `%`?
- [ ] ¿Qué ocurre cuando Java divide dos enteros?
- [ ] ¿Por qué es importante usar paréntesis en el promedio?
- [ ] ¿Puedo hacer una prueba de escritorio de una expresión?

---

## 29. Conclusión

La jerarquía de operaciones permite que las expresiones matemáticas se resuelvan correctamente.

En algoritmia y programación, conocer este orden evita errores en fórmulas, promedios, áreas, porcentajes y cálculos financieros.

La recomendación principal es usar paréntesis cuando exista duda.  
Un paréntesis bien ubicado puede evitar un error lógico difícil de detectar.
