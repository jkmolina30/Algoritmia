# Ejemplos en PSeInt: Variables, Tipos de Datos y Operadores

## Presentación

Este archivo contiene ejemplos en PSeInt para practicar:

- Declaración de variables.
- Tipos de datos.
- Entrada y salida.
- Operadores aritméticos.
- Expresiones.
- Jerarquía de operaciones.

---

# Ejemplo 1. Datos personales

## Problema

Leer el nombre, la edad y el programa académico de un estudiante. Mostrar los datos ingresados.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | nombre, edad, programa |
| Proceso | No realiza cálculos; solo organiza la información |
| Salida | Datos del estudiante |

---

## Pseudocódigo

```pseint
Algoritmo DatosPersonales
    Definir nombre, programa Como Caracter
    Definir edad Como Entero

    Escribir "Ingrese su nombre:"
    Leer nombre

    Escribir "Ingrese su edad:"
    Leer edad

    Escribir "Ingrese su programa académico:"
    Leer programa

    Escribir "Nombre: ", nombre
    Escribir "Edad: ", edad
    Escribir "Programa: ", programa
FinAlgoritmo
```

---

## Explicación

- `nombre` y `programa` son de tipo `Caracter` porque guardan texto.
- `edad` es de tipo `Entero` porque representa años completos.
- El algoritmo recibe datos y luego los muestra.

---

# Ejemplo 2. Suma, resta, multiplicación y división

## Problema

Leer dos números y mostrar las cuatro operaciones básicas.

---

## Pseudocódigo

```pseint
Algoritmo OperacionesBasicas
    Definir num1, num2 Como Real
    Definir suma, resta, multiplicacion, division Como Real

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    suma <- num1 + num2
    resta <- num1 - num2
    multiplicacion <- num1 * num2
    division <- num1 / num2

    Escribir "Suma: ", suma
    Escribir "Resta: ", resta
    Escribir "Multiplicación: ", multiplicacion
    Escribir "División: ", division
FinAlgoritmo
```

---

## Explicación

Se usa `Real` para permitir valores decimales.  
Este algoritmo todavía no valida división entre cero; eso se trabajará cuando se estudien condicionales.

---

# Ejemplo 3. Promedio de tres notas

## Problema

Leer tres notas y calcular el promedio.

---

## Pseudocódigo

```pseint
Algoritmo PromedioTresNotas
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

## Explicación

Los paréntesis son importantes porque primero se deben sumar las tres notas y luego dividir entre 3.

---

# Ejemplo 4. Área de un círculo

## Problema

Leer el radio de un círculo y calcular su área.

---

## Fórmula

```text
area = PI * radio ^ 2
```

---

## Pseudocódigo

```pseint
Algoritmo AreaCirculo
    Definir radio, area Como Real
    Definir PI Como Real

    PI <- 3.1416

    Escribir "Ingrese el radio del círculo:"
    Leer radio

    area <- PI * radio ^ 2

    Escribir "El área del círculo es: ", area
FinAlgoritmo
```

---

## Explicación

En PSeInt el operador `^` permite calcular potencias.

```pseint
radio ^ 2
```

significa:

```text
radio elevado al cuadrado
```

---

# Ejemplo 5. Valor total de compra con IVA

## Problema

Leer el valor de un producto y calcular el IVA del 19%. Luego mostrar el total a pagar.

---

## Pseudocódigo

```pseint
Algoritmo CompraConIVA
    Definir valorProducto, iva, total Como Real

    Escribir "Ingrese el valor del producto:"
    Leer valorProducto

    iva <- valorProducto * 0.19
    total <- valorProducto + iva

    Escribir "Valor del producto: ", valorProducto
    Escribir "IVA: ", iva
    Escribir "Total a pagar: ", total
FinAlgoritmo
```

---

## Explicación

El IVA se calcula multiplicando el valor del producto por `0.19`.  
Luego se suma el IVA al valor inicial.

---

# Ejemplo 6. Uso de operadores relacionales

## Problema

Leer una nota y mostrar el resultado de comparar si es mayor o igual a 3.0.

---

## Pseudocódigo

```pseint
Algoritmo CompararNota
    Definir nota Como Real
    Definir resultado Como Logico

    Escribir "Ingrese la nota:"
    Leer nota

    resultado <- nota >= 3.0

    Escribir "¿La nota es mayor o igual a 3.0?: ", resultado
FinAlgoritmo
```

---

## Explicación

La expresión:

```pseint
nota >= 3.0
```

produce un valor lógico:

```text
Verdadero o Falso
```

---

# Ejemplo 7. Expresión compuesta

## Problema

Calcular la nota definitiva de una asignatura usando tres cortes.

- Corte 1: 30%
- Corte 2: 30%
- Corte 3: 40%

---

## Pseudocódigo

```pseint
Algoritmo NotaDefinitiva
    Definir corte1, corte2, corte3, definitiva Como Real

    Escribir "Ingrese la nota del primer corte:"
    Leer corte1

    Escribir "Ingrese la nota del segundo corte:"
    Leer corte2

    Escribir "Ingrese la nota del tercer corte:"
    Leer corte3

    definitiva <- corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40

    Escribir "La nota definitiva es: ", definitiva
FinAlgoritmo
```

---

## Explicación

La expresión usa multiplicaciones y sumas.  
Por precedencia, primero se hacen las multiplicaciones y luego las sumas.
