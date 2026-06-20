# Ejercicios Propuestos: Condicionales en Java

## Instrucciones generales

Para cada ejercicio entregar:

1. Análisis de entrada, proceso y salida.
2. Código Java.
3. Prueba de escritorio.
4. Evidencia de ejecución si el docente lo solicita.
5. Explicación breve.

---

# Nivel 1. Condicional simple y doble

## Ejercicio 1

Leer la edad de una persona e indicar si es mayor de edad.

---

## Ejercicio 2

Leer una nota e indicar si el estudiante aprobó o reprobó.

---

## Ejercicio 3

Leer un número entero e indicar si es par o impar.

---

## Ejercicio 4

Leer un número e indicar si es positivo, negativo o cero.

---

## Ejercicio 5

Leer dos números e indicar cuál es mayor o si son iguales.

---

# Nivel 2. Validaciones

## Ejercicio 6

Leer una nota e indicar si está en el rango válido de 0.0 a 5.0.

---

## Ejercicio 7

Leer una edad e indicar si está en el rango válido de 0 a 120 años.

---

## Ejercicio 8

Leer el precio de un producto e indicar si el precio es válido. Un precio válido debe ser mayor que cero.

---

## Ejercicio 9

Leer una contraseña e indicar si coincide con la contraseña guardada.

Contraseña guardada:

```text
java123
```

---

## Ejercicio 10

Leer el nombre de un usuario e indicar si es `admin`. Usar `equalsIgnoreCase`.

---

# Nivel 3. Condicional múltiple

## Ejercicio 11

Leer una nota y mostrar el desempeño:

- Menor que 3.0: bajo.
- Desde 3.0 hasta menor que 4.0: básico.
- Desde 4.0 hasta menor que 4.6: alto.
- Desde 4.6 hasta 5.0: superior.

Validar primero que la nota esté entre 0.0 y 5.0.

---

## Ejercicio 12

Leer el número de un mes e indicar su nombre.

Ejemplo:

```text
1 = enero
2 = febrero
```

---

## Ejercicio 13

Leer un número del 1 al 7 e indicar el día de la semana.

---

## Ejercicio 14

Leer una calificación de servicio del 1 al 5 y mostrar un mensaje:

- 1: Muy malo.
- 2: Malo.
- 3: Regular.
- 4: Bueno.
- 5: Excelente.

---

# Nivel 4. `switch`

## Ejercicio 15

Crear un menú con tres opciones:

1. Saludar.
2. Mostrar nombre del curso.
3. Salir.

---

## Ejercicio 16

Crear una calculadora básica usando `switch`:

1. Sumar.
2. Restar.
3. Multiplicar.
4. Dividir.

Validar división entre cero.

---

## Ejercicio 17

Crear un menú para calcular áreas:

1. Área de rectángulo.
2. Área de triángulo.
3. Área de círculo.

---

# Nivel 5. Aplicados

## Ejercicio 18

Leer el valor de una compra. Si supera 100000, aplicar descuento del 10%. Mostrar descuento y total.

---

## Ejercicio 19

Leer horas trabajadas y valor por hora. Si las horas son mayores a 40, calcular horas extra con un recargo del 25%.

---

## Ejercicio 20

Leer edad y valor de una entrada a cine. Si la persona es menor de 12 años, aplicar descuento del 50%. Si es adulto mayor, aplicar descuento del 30%. En otro caso, paga tarifa normal.

---

## Ejercicio 21

Leer tres notas y calcular el promedio. Validar que cada nota esté entre 0.0 y 5.0 antes de calcular.

---

## Ejercicio 22

Leer usuario y contraseña. Permitir acceso solo si el usuario es `admin` y la contraseña es `1234`.

---

# Reto integrador

## Sistema básico de matrícula

Crear un programa en Java que lea:

- Nombre del estudiante.
- Edad.
- Nota final.
- Valor de matrícula.
- Estrato socioeconómico.

Reglas:

- Si la edad no está entre 15 y 80, mostrar error.
- Si la nota no está entre 0.0 y 5.0, mostrar error.
- Si el estrato es 1 o 2, aplicar descuento del 40%.
- Si el estrato es 3, aplicar descuento del 20%.
- Si el estrato es 4, 5 o 6, no aplicar descuento.
- Mostrar nombre, nota, descuento y total a pagar.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Uso de `if` | Aplica correctamente condicionales |
| Uso de operadores | Usa relacionales y lógicos |
| Validaciones | Controla datos inválidos |
| Claridad | Usa nombres adecuados |
| Orden | Código indentado |
| Explicación | Puede explicar cada decisión |
