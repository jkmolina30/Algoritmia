# Ejercicios: ArrayList en Java

## Instrucciones generales

Para cada ejercicio entregar:

1. Análisis.
2. Código Java.
3. Prueba de escritorio.
4. Explicación breve.
5. Evidencia de ejecución si el docente lo solicita.

---

# Nivel 1. Creación y recorrido

## Ejercicio 1

Crear un `ArrayList<String>` con 5 nombres y mostrarlos en pantalla.

---

## Ejercicio 2

Crear un `ArrayList<Integer>` con 5 edades y mostrarlas.

---

## Ejercicio 3

Crear un `ArrayList<Double>` con 5 notas y calcular el promedio.

---

## Ejercicio 4

Leer desde teclado una cantidad de nombres indicada por el usuario y guardarlos en un `ArrayList`.

---

## Ejercicio 5

Leer desde teclado una cantidad de números indicada por el usuario y mostrarlos al final.

---

# Nivel 2. Búsqueda y modificación

## Ejercicio 6

Crear una lista de nombres. Pedir un nombre al usuario e indicar si está registrado.

---

## Ejercicio 7

Crear una lista de números. Pedir un número e indicar si está en la lista.

---

## Ejercicio 8

Crear una lista de nombres y modificar el elemento de la posición 1.

---

## Ejercicio 9

Crear una lista de productos y eliminar un producto por nombre.

---

## Ejercicio 10

Crear una lista de tareas y eliminar una tarea por posición. Validar que la posición exista.

---

# Nivel 3. Operaciones con números

## Ejercicio 11

Leer varios números en un `ArrayList<Integer>` y calcular la suma.

---

## Ejercicio 12

Leer varias notas en un `ArrayList<Double>`, validarlas entre 0.0 y 5.0, y calcular el promedio.

---

## Ejercicio 13

Leer varios números y mostrar el mayor.

---

## Ejercicio 14

Leer varios números y mostrar el menor.

---

## Ejercicio 15

Leer varios números y contar cuántos son pares.

---

# Nivel 4. Aplicados

## Ejercicio 16

Crear un programa para registrar estudiantes en un `ArrayList<String>`. El programa debe permitir:

1. Agregar estudiante.
2. Mostrar estudiantes.
3. Buscar estudiante.
4. Eliminar estudiante.
5. Salir.

---

## Ejercicio 17

Crear un programa para registrar notas en un `ArrayList<Double>`. El programa debe permitir:

1. Agregar nota.
2. Mostrar notas.
3. Calcular promedio.
4. Contar aprobadas.
5. Salir.

---

## Ejercicio 18

Crear una lista de productos y otra lista de precios. Registrar varios productos y mostrar el total de la compra.

---

## Ejercicio 19

Crear una lista de tareas pendientes. Permitir agregar, mostrar y eliminar tareas.

---

## Ejercicio 20

Crear una lista de gastos diarios. Calcular total gastado y promedio de gasto.

---

# Reto integrador

## Sistema de registro académico con ArrayList

Crear un programa en Java que use:

```java
ArrayList<String> nombres
ArrayList<Double> notas
```

El programa debe tener un menú:

1. Registrar estudiante.
2. Mostrar estudiantes.
3. Buscar estudiante.
4. Calcular promedio del grupo.
5. Mostrar aprobados.
6. Eliminar estudiante.
7. Salir.

Reglas:

- La nota debe estar entre 0.0 y 5.0.
- Un estudiante aprueba si su nota es mayor o igual a 3.0.
- Al eliminar un estudiante, también debe eliminarse su nota.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| ArrayList | Usa listas dinámicas correctamente |
| Métodos | Usa `.add()`, `.get()`, `.set()`, `.remove()`, `.size()` |
| Validación | Valida notas y posiciones |
| Ciclos | Recorre listas correctamente |
| Condicionales | Aplica decisiones |
| Claridad | Usa nombres adecuados |
| Orden | Código indentado |
