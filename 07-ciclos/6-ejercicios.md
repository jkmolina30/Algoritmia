# Ejercicios: Ciclos en Java

## Instrucciones generales

Para cada ejercicio entregar:

1. Análisis del problema.
2. Código Java.
3. Prueba de escritorio.
4. Explicación breve.
5. Evidencia de ejecución si el docente lo solicita.

---

# Nivel 1. Ciclo `while`

## Ejercicio 1

Mostrar los números del 1 al 10 usando `while`.

---

## Ejercicio 2

Mostrar los números del 10 al 1 usando `while`.

---

## Ejercicio 3

Sumar los números del 1 al 100 usando `while`.

---

## Ejercicio 4

Pedir una contraseña hasta que sea correcta.

Contraseña correcta:

```text
java123
```

---

## Ejercicio 5

Pedir números enteros y sumarlos hasta que el usuario ingrese 0.

---

# Nivel 2. Ciclo `do-while`

## Ejercicio 6

Crear un menú que se repita hasta que el usuario elija salir.

Opciones:

1. Saludar.
2. Mostrar curso.
3. Salir.

---

## Ejercicio 7

Pedir una nota hasta que esté en el rango de 0.0 a 5.0.

---

## Ejercicio 8

Pedir una edad hasta que esté entre 0 y 120.

---

## Ejercicio 9

Pedir una opción entre 1 y 5 hasta que sea válida.

---

## Ejercicio 10

Crear una calculadora repetitiva con opciones:

1. Sumar.
2. Restar.
3. Multiplicar.
4. Dividir.
5. Salir.

---

# Nivel 3. Ciclo `for`

## Ejercicio 11

Mostrar los números del 1 al 20 usando `for`.

---

## Ejercicio 12

Mostrar los números pares del 2 al 50.

---

## Ejercicio 13

Mostrar los números impares del 1 al 49.

---

## Ejercicio 14

Leer un número y mostrar su tabla de multiplicar del 1 al 10.

---

## Ejercicio 15

Leer 5 notas y calcular el promedio.

---

# Nivel 4. Contadores y acumuladores

## Ejercicio 16

Leer 10 números y contar cuántos son positivos.

---

## Ejercicio 17

Leer 10 números y contar cuántos son pares.

---

## Ejercicio 18

Leer 5 precios de productos y calcular el total de la compra.

---

## Ejercicio 19

Leer la cantidad de estudiantes de un grupo. Luego leer la nota de cada estudiante y calcular el promedio del grupo.

---

## Ejercicio 20

Leer la cantidad de trabajadores. Para cada trabajador, leer horas trabajadas y valor por hora. Calcular el total pagado por la empresa.

---

# Nivel 5. Ejercicios aplicados

## Ejercicio 21

Crear un programa que pida notas hasta que el usuario ingrese `-1`. Al final debe mostrar el promedio de las notas válidas.

---

## Ejercicio 22

Crear un programa que pida edades hasta que el usuario ingrese `0`. Al final debe mostrar:

- Cantidad de edades ingresadas.
- Promedio de edad.
- Cantidad de mayores de edad.

---

## Ejercicio 23

Crear un programa que simule intentos de acceso. El usuario tiene máximo 3 intentos para ingresar la contraseña correcta.

---

## Ejercicio 24

Crear un programa que muestre un menú de gestión académica:

1. Registrar nota.
2. Mostrar nota registrada.
3. Validar si aprobó.
4. Salir.

El menú debe repetirse hasta elegir salir.

---

## Ejercicio 25

Crear un programa que calcule el gasto semanal de transporte de varios estudiantes.  
El usuario debe indicar cuántos estudiantes va a registrar. Para cada estudiante se debe leer:

- Nombre.
- Valor del pasaje.
- Pasajes diarios.
- Días de asistencia.

Mostrar el gasto semanal de cada estudiante y el total general.

---

# Reto integrador

## Sistema básico de registro de notas

Crear un programa en Java que permita registrar notas de varios estudiantes.

El programa debe:

1. Preguntar cuántos estudiantes se van a registrar.
2. Para cada estudiante, leer:
   - Nombre.
   - Nota final.
3. Validar que la nota esté entre 0.0 y 5.0.
4. Contar cuántos aprobaron.
5. Contar cuántos reprobaron.
6. Calcular el promedio del grupo.
7. Mostrar un resumen final.

Criterio:

```text
Aprueba si nota >= 3.0
```

---

## Requisitos técnicos

El programa debe usar:

- `Scanner`.
- `for` para recorrer estudiantes.
- `do-while` para validar notas.
- `if` para determinar aprobación.
- Contadores.
- Acumuladores.
- Variables con nombres claros.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Ciclos | Usa correctamente `while`, `do-while` o `for` |
| Condicionales | Aplica decisiones correctamente |
| Validación | Controla datos inválidos |
| Contadores | Cuenta correctamente eventos |
| Acumuladores | Suma correctamente valores |
| Claridad | Usa nombres comprensibles |
| Orden | Código indentado |
| Explicación | Puede explicar la lógica |
