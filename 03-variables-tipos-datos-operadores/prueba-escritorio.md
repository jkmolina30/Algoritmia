# Prueba de Escritorio: Variables, Tipos de Datos y Operadores

## 1. ¿Qué es una prueba de escritorio?

La **prueba de escritorio** consiste en revisar manualmente el comportamiento de un algoritmo o programa usando datos de ejemplo.

Sirve para verificar si:

- Las variables reciben los valores correctos.
- Las operaciones están bien planteadas.
- La salida corresponde al resultado esperado.
- La jerarquía de operaciones está bien aplicada.

---

## 2. ¿Por qué es importante?

Porque permite encontrar errores antes de ejecutar el programa.

Muchos errores no son de sintaxis, sino de lógica.

Ejemplo:

```java
promedio = nota1 + nota2 + nota3 / 3;
```

El programa puede compilar, pero el resultado será incorrecto porque faltan paréntesis.

---

# Ejemplo 1. Suma de dos números

## Algoritmo

```pseint
Algoritmo SumaDosNumeros
    Definir num1, num2, suma Como Entero

    Leer num1
    Leer num2

    suma <- num1 + num2

    Escribir suma
FinAlgoritmo
```

---

## Datos de prueba

```text
num1 = 8
num2 = 5
```

---

## Tabla de prueba de escritorio

| Paso | num1 | num2 | suma | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer num1 | 8 | - | - | - |
| Leer num2 | 8 | 5 | - | - |
| Calcular suma | 8 | 5 | 13 | - |
| Mostrar suma | 8 | 5 | 13 | 13 |

---

# Ejemplo 2. Promedio de tres notas

## Fórmula

```text
promedio = (nota1 + nota2 + nota3) / 3
```

---

## Datos de prueba

```text
nota1 = 4.0
nota2 = 3.5
nota3 = 5.0
```

---

## Tabla de prueba de escritorio

| Paso | nota1 | nota2 | nota3 | promedio | Salida |
|---|---:|---:|---:|---:|---|
| Inicio | - | - | - | - | - |
| Leer nota1 | 4.0 | - | - | - | - |
| Leer nota2 | 4.0 | 3.5 | - | - | - |
| Leer nota3 | 4.0 | 3.5 | 5.0 | - | - |
| Calcular promedio | 4.0 | 3.5 | 5.0 | 4.166 | - |
| Mostrar promedio | 4.0 | 3.5 | 5.0 | 4.166 | 4.166 |

---

# Ejemplo 3. Compra con IVA

## Fórmulas

```text
iva = valorProducto * 0.19
total = valorProducto + iva
```

---

## Datos de prueba

```text
valorProducto = 100000
```

---

## Tabla de prueba de escritorio

| Paso | valorProducto | iva | total | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer valorProducto | 100000 | - | - | - |
| Calcular IVA | 100000 | 19000 | - | - |
| Calcular total | 100000 | 19000 | 119000 | - |
| Mostrar total | 100000 | 19000 | 119000 | 119000 |

---

# Ejemplo 4. Nota definitiva

## Fórmula

```text
definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40
```

---

## Datos de prueba

```text
corte1 = 3.5
corte2 = 4.0
corte3 = 4.5
```

---

## Proceso manual

```text
corte1 * 0.30 = 3.5 * 0.30 = 1.05
corte2 * 0.30 = 4.0 * 0.30 = 1.20
corte3 * 0.40 = 4.5 * 0.40 = 1.80
definitiva = 1.05 + 1.20 + 1.80 = 4.05
```

---

## Tabla de prueba de escritorio

| Paso | corte1 | corte2 | corte3 | definitiva | Salida |
|---|---:|---:|---:|---:|---|
| Inicio | - | - | - | - | - |
| Leer corte1 | 3.5 | - | - | - | - |
| Leer corte2 | 3.5 | 4.0 | - | - | - |
| Leer corte3 | 3.5 | 4.0 | 4.5 | - | - |
| Calcular definitiva | 3.5 | 4.0 | 4.5 | 4.05 | - |
| Mostrar definitiva | 3.5 | 4.0 | 4.5 | 4.05 | 4.05 |

---

## Plantilla para prueba de escritorio

```text
Nombre del algoritmo:

Datos de prueba:

Variables:

Tabla:

| Paso | variable1 | variable2 | resultado | Salida |
|---|---|---|---|---|
| Inicio | - | - | - | - |
```

---

## Recomendaciones

- Usar datos sencillos al inicio.
- Revisar cada operación con calma.
- Verificar si hay paréntesis.
- Comprobar que la salida responde al problema.
- Si el resultado manual no coincide con el programa, revisar la lógica.
