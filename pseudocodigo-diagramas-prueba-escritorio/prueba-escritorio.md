# Prueba de Escritorio

## 1. ¿Qué es la prueba de escritorio?

La prueba de escritorio es una técnica que permite revisar manualmente el funcionamiento de un algoritmo.

Consiste en usar datos de ejemplo y registrar cómo cambian las variables paso a paso.

---

## 2. ¿Para qué sirve?

Sirve para:

- Verificar la lógica.
- Detectar errores antes de programar.
- Revisar fórmulas.
- Comprobar el orden de instrucciones.
- Entender cómo cambian las variables.
- Preparar mejor la implementación en Java.

---

## 3. ¿Cuándo se debe hacer?

Se debe hacer después de escribir el pseudocódigo y antes de pasar a Java.

Ruta recomendada:

```text
Enunciado
   ↓
Análisis
   ↓
Pseudocódigo
   ↓
Prueba de escritorio
   ↓
Java
```

---

## 4. Elementos de una prueba de escritorio

Una prueba de escritorio debe tener:

- Datos de prueba.
- Variables.
- Tabla de seguimiento.
- Salida esperada.
- Revisión del resultado.

---

# Ejemplo 1. Doble de un número

## Pseudocódigo

```pseint
Algoritmo CalcularDoble
    Definir numero, doble Como Entero

    Leer numero

    doble <- numero * 2

    Escribir doble
FinAlgoritmo
```

---

## Datos de prueba

```text
numero = 7
```

---

## Tabla

| Paso | numero | doble | Salida |
|---|---:|---:|---|
| Inicio | - | - | - |
| Leer numero | 7 | - | - |
| Calcular doble | 7 | 14 | - |
| Mostrar doble | 7 | 14 | 14 |

---

# Ejemplo 2. Área de triángulo

## Pseudocódigo

```pseint
Algoritmo AreaTriangulo
    Definir base, altura, area Como Real

    Leer base
    Leer altura

    area <- (base * altura) / 2

    Escribir area
FinAlgoritmo
```

---

## Datos de prueba

```text
base = 10
altura = 4
```

---

## Tabla

| Paso | base | altura | area | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer base | 10 | - | - | - |
| Leer altura | 10 | 4 | - | - |
| Calcular área | 10 | 4 | 20 | - |
| Mostrar área | 10 | 4 | 20 | 20 |

---

# Ejemplo 3. Nota definitiva

## Pseudocódigo

```pseint
Algoritmo NotaDefinitiva
    Definir corte1, corte2, corte3, definitiva Como Real

    Leer corte1
    Leer corte2
    Leer corte3

    definitiva <- corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40

    Escribir definitiva
FinAlgoritmo
```

---

## Datos de prueba

```text
corte1 = 3.0
corte2 = 4.0
corte3 = 5.0
```

---

## Cálculo manual

```text
3.0 * 0.30 = 0.90
4.0 * 0.30 = 1.20
5.0 * 0.40 = 2.00
definitiva = 0.90 + 1.20 + 2.00 = 4.10
```

---

## Tabla

| Paso | corte1 | corte2 | corte3 | definitiva | Salida |
|---|---:|---:|---:|---:|---|
| Inicio | - | - | - | - | - |
| Leer corte1 | 3.0 | - | - | - | - |
| Leer corte2 | 3.0 | 4.0 | - | - | - |
| Leer corte3 | 3.0 | 4.0 | 5.0 | - | - |
| Calcular definitiva | 3.0 | 4.0 | 5.0 | 4.10 | - |
| Mostrar definitiva | 3.0 | 4.0 | 5.0 | 4.10 | 4.10 |

---

## 5. Plantilla general

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

## 6. Errores que se pueden detectar

Con una prueba de escritorio se pueden detectar errores como:

- Fórmulas mal escritas.
- Variables sin valor.
- Operaciones en orden incorrecto.
- Salidas incompletas.
- Uso incorrecto de paréntesis.
- Variables con nombres confusos.

---

## 7. Recomendación final

Si un algoritmo no funciona en la prueba de escritorio, probablemente tampoco funcionará en Java.

Por eso, antes de programar, se debe comprobar manualmente la lógica.
