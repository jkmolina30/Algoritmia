# Ejercicios: Funciones, Procedimientos y Métodos

## Instrucciones generales

Para cada ejercicio entregar:

1. Análisis.
2. Código en PSeInt o Java, según se indique.
3. Prueba de escritorio.
4. Explicación breve.
5. Evidencia de ejecución si el docente lo solicita.

---

# Nivel 1. Funciones en PSeInt

## Ejercicio 1

Crear una función en PSeInt que reciba dos números y devuelva la suma.

---

## Ejercicio 2

Crear una función en PSeInt que reciba dos números y devuelva la resta.

---

## Ejercicio 3

Crear una función que calcule el área de un rectángulo.

---

## Ejercicio 4

Crear una función que calcule el área de un triángulo.

---

## Ejercicio 5

Crear una función que reciba una nota y devuelva `Verdadero` si está entre 0.0 y 5.0.

---

# Nivel 2. Métodos básicos en Java

## Ejercicio 6

Crear un método `saludar()` que muestre un mensaje de bienvenida.

---

## Ejercicio 7

Crear un método `sumar(int a, int b)` que devuelva la suma.

---

## Ejercicio 8

Crear un método `calcularAreaRectangulo(double base, double altura)`.

---

## Ejercicio 9

Crear un método `calcularAreaTriangulo(double base, double altura)`.

---

## Ejercicio 10

Crear un método `validarNota(double nota)` que devuelva `true` si la nota está entre 0.0 y 5.0.

---

# Nivel 3. Métodos con condicionales

## Ejercicio 11

Crear un método `esMayorEdad(int edad)` que devuelva `true` si la edad es mayor o igual a 18.

---

## Ejercicio 12

Crear un método `esPar(int numero)` que devuelva `true` si el número es par.

---

## Ejercicio 13

Crear un método `determinarDesempeno(double nota)` que devuelva un texto:

- Bajo.
- Básico.
- Alto.
- Superior.

---

## Ejercicio 14

Crear un método `calcularDescuento(double valorCompra)` que devuelva el descuento según la regla:

- Si la compra supera 100000, descuento del 10%.
- Si no, descuento de 0.

---

## Ejercicio 15

Crear un método `calcularDefinitiva(double corte1, double corte2, double corte3)`.

---

# Nivel 4. Métodos con arreglos

## Ejercicio 16

Crear un método que reciba un arreglo de enteros y devuelva la suma.

---

## Ejercicio 17

Crear un método que reciba un arreglo de notas y devuelva el promedio.

---

## Ejercicio 18

Crear un método que reciba un arreglo de enteros y devuelva el mayor.

---

## Ejercicio 19

Crear un método que reciba un arreglo de enteros y devuelva el menor.

---

## Ejercicio 20

Crear un método que reciba un arreglo de notas y devuelva cuántas son aprobadas.

---

# Nivel 5. Métodos con matrices

## Ejercicio 21

Crear un método que reciba una matriz de enteros y devuelva la suma total.

---

## Ejercicio 22

Crear un método que reciba una matriz de enteros y devuelva el mayor elemento.

---

## Ejercicio 23

Crear un método que reciba una matriz de enteros y devuelva el menor elemento.

---

## Ejercicio 24

Crear un método que reciba una matriz de notas y devuelva el promedio general.

---

## Ejercicio 25

Crear un método que reciba una matriz cuadrada y devuelva la suma de la diagonal principal.

---

# Reto integrador

## Sistema académico modular en Java

Crear un programa en Java usando métodos.

El programa debe permitir registrar notas de varios estudiantes.

Debe tener como mínimo estos métodos:

```java
public static boolean validarNota(double nota)
public static double calcularPromedio(double[] notas)
public static String determinarResultado(double promedio)
public static void mostrarResumen(String nombre, double promedio, String resultado)
```

El programa debe:

1. Leer el nombre de un estudiante.
2. Leer 3 notas.
3. Validar cada nota.
4. Calcular el promedio.
5. Determinar si aprobó o reprobó.
6. Mostrar un resumen final.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Modularidad | Divide el programa en métodos |
| Parámetros | Usa parámetros correctamente |
| Retorno | Usa `return` cuando corresponde |
| Claridad | Nombres de métodos claros |
| Validación | Valida datos |
| Arreglos | Usa arreglos cuando corresponde |
| Orden | Código indentado |
| Explicación | Puede explicar cada método |
