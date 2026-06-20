# Ejercicios: Variables, Tipos de Datos y Operadores

## Instrucciones generales

Para cada ejercicio entregar:

1. Análisis de entrada, proceso y salida.
2. Pseudocódigo en PSeInt.
3. Código en Java.
4. Prueba de escritorio.
5. Explicación breve.

---

# Nivel 1. Variables y tipos de datos

## Ejercicio 1

Leer el nombre de una persona y mostrarlo en pantalla.

---

## Ejercicio 2

Leer el nombre, edad y ciudad de una persona. Mostrar todos los datos.

---

## Ejercicio 3

Leer el nombre de un estudiante, el programa académico y el semestre. Mostrar un resumen.

---

## Ejercicio 4

Leer una letra que represente el grupo de un estudiante. Mostrar la letra ingresada.

---

## Ejercicio 5

Leer un valor lógico que indique si un estudiante está matriculado. Mostrar el valor.

---

# Nivel 2. Operadores aritméticos

## Ejercicio 6

Leer dos números enteros y calcular suma, resta, multiplicación y división.

---

## Ejercicio 7

Leer un número y calcular su doble, triple y cuadrado.

---

## Ejercicio 8

Leer una cantidad de horas y convertirla a minutos.

---

## Ejercicio 9

Leer una cantidad de días y convertirla a horas.

---

## Ejercicio 10

Leer una cantidad de kilómetros y convertirla a metros.

---

# Nivel 3. Fórmulas

## Ejercicio 11

Leer base y altura de un rectángulo. Calcular área y perímetro.

---

## Ejercicio 12

Leer base y altura de un triángulo. Calcular el área.

---

## Ejercicio 13

Leer el radio de un círculo. Calcular el área.

En PSeInt usar:

```pseint
area <- 3.1416 * radio ^ 2
```

En Java usar:

```java
area = Math.PI * Math.pow(radio, 2);
```

---

## Ejercicio 14

Leer el lado de un cuadrado. Calcular área y perímetro.

---

## Ejercicio 15

Leer el precio de un producto y la cantidad comprada. Calcular el total.

---

# Nivel 4. Porcentajes y expresiones

## Ejercicio 16

Leer el valor de un producto y calcular el IVA del 19%.

---

## Ejercicio 17

Leer el valor de una compra y calcular un descuento del 10%.

---

## Ejercicio 18

Leer el valor de una compra, calcular descuento del 10%, IVA del 19% sobre el valor con descuento y total a pagar.

---

## Ejercicio 19

Leer tres notas y calcular el promedio.

---

## Ejercicio 20

Leer las notas de tres cortes y calcular la definitiva:

```text
definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40
```

---

# Nivel 5. Operadores relacionales y lógicos

## Ejercicio 21

Leer una nota y guardar en una variable lógica si la nota es mayor o igual a 3.0.

---

## Ejercicio 22

Leer una edad y guardar en una variable lógica si la persona es mayor de edad.

---

## Ejercicio 23

Leer una edad y guardar en una variable lógica si está entre 18 y 25 años.

En Java:

```java
resultado = edad >= 18 && edad <= 25;
```

---

## Ejercicio 24

Leer una nota y guardar en una variable lógica si está en el rango de 0.0 a 5.0.

---

## Ejercicio 25

Leer el valor de una compra y guardar en una variable lógica si supera 100000.

---

# Reto integrador

## Reto. Liquidación básica de matrícula

Crear un algoritmo en PSeInt y un programa en Java que lea:

- Nombre del estudiante.
- Valor base de matrícula.
- Valor del carné.
- Valor del seguro.
- Valor de derechos complementarios.
- Porcentaje de descuento.

Debe calcular:

```text
subtotal = valorMatricula + valorCarne + valorSeguro + derechosComplementarios
descuento = subtotal * porcentajeDescuento / 100
total = subtotal - descuento
```

Debe mostrar:

- Nombre del estudiante.
- Subtotal.
- Descuento.
- Total a pagar.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Variables | Usa nombres claros |
| Tipos de datos | Selecciona tipos adecuados |
| Operadores | Aplica correctamente las operaciones |
| Precedencia | Usa paréntesis si es necesario |
| PSeInt | El pseudocódigo es claro |
| Java | El programa compila y ejecuta |
| Prueba de escritorio | Verifica la solución |
