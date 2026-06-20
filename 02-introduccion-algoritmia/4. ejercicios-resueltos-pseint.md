# Ejercicios Resueltos en PSeInt

## Unidad 2. Introducción a la Algoritmia

Este archivo contiene ejercicios resueltos únicamente en **PSeInt**.  
El propósito es que el estudiante fortalezca primero la lógica algorítmica antes de pasar a Java.

Cada ejercicio incluye:

1. Enunciado.
2. Análisis de entrada, proceso y salida.
3. Algoritmo en lenguaje natural.
4. Pseudocódigo en PSeInt.
5. Prueba de escritorio.
6. Explicación.

---

# Ejercicio 1. Suma de dos números

## Enunciado

Diseñar un algoritmo que lea dos números enteros y muestre la suma.

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `num1`, `num2` |
| Proceso | `suma <- num1 + num2` |
| Salida | Resultado de la suma |

---

## Algoritmo en lenguaje natural

1. Pedir el primer número.
2. Pedir el segundo número.
3. Sumar los dos números.
4. Guardar el resultado.
5. Mostrar la suma.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo SumaDosNumeros
    Definir num1, num2, suma Como Entero

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    suma <- num1 + num2

    Escribir "La suma es: ", suma
FinAlgoritmo
```

---

## Explicación línea a línea

```pseint
Algoritmo SumaDosNumeros
```

Indica el inicio del algoritmo y define su nombre.

```pseint
Definir num1, num2, suma Como Entero
```

Declara tres variables de tipo entero.  
`num1` y `num2` guardan los datos ingresados.  
`suma` guarda el resultado.

```pseint
Leer num1
Leer num2
```

Permite recibir los datos digitados por el usuario.

```pseint
suma <- num1 + num2
```

Realiza la operación de suma y guarda el resultado.

```pseint
Escribir "La suma es: ", suma
```

Muestra el resultado final.

---

## Prueba de escritorio

Datos de prueba:

```text
num1 = 12
num2 = 8
```

| Paso | num1 | num2 | suma | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer num1 | 12 | - | - | - |
| Leer num2 | 12 | 8 | - | - |
| Calcular suma | 12 | 8 | 20 | - |
| Mostrar resultado | 12 | 8 | 20 | La suma es: 20 |

---

# Ejercicio 2. Área de un triángulo

## Enunciado

Diseñar un algoritmo que calcule el área de un triángulo a partir de su base y altura.

---

## Fórmula

```text
area = (base * altura) / 2
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `base`, `altura` |
| Proceso | `area <- (base * altura) / 2` |
| Salida | Área del triángulo |

---

## Algoritmo en lenguaje natural

1. Pedir la base del triángulo.
2. Pedir la altura del triángulo.
3. Multiplicar base por altura.
4. Dividir el resultado entre 2.
5. Mostrar el área.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo AreaTriangulo
    Definir base, altura, area Como Real

    Escribir "Ingrese la base del triángulo:"
    Leer base

    Escribir "Ingrese la altura del triángulo:"
    Leer altura

    area <- (base * altura) / 2

    Escribir "El área del triángulo es: ", area
FinAlgoritmo
```

---

## Explicación

Se usa el tipo `Real` porque la base, la altura y el área pueden tener valores decimales.

Por ejemplo:

```text
base = 7.5
altura = 4.2
```

En ese caso, el resultado también puede ser decimal.

---

## Prueba de escritorio

Datos de prueba:

```text
base = 10
altura = 6
```

| Paso | base | altura | area | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer base | 10 | - | - | - |
| Leer altura | 10 | 6 | - | - |
| Calcular área | 10 | 6 | 30 | - |
| Mostrar resultado | 10 | 6 | 30 | El área del triángulo es: 30 |

---

# Ejercicio 3. Conversión de kilómetros a metros

## Enunciado

Diseñar un algoritmo que lea una cantidad de kilómetros y muestre su equivalente en metros.

---

## Fórmula

```text
metros = kilometros * 1000
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `kilometros` |
| Proceso | `metros <- kilometros * 1000` |
| Salida | Metros equivalentes |

---

## Algoritmo en lenguaje natural

1. Pedir la cantidad de kilómetros.
2. Multiplicar los kilómetros por 1000.
3. Mostrar el resultado en metros.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo KilometrosAMetros
    Definir kilometros, metros Como Real

    Escribir "Ingrese la cantidad de kilómetros:"
    Leer kilometros

    metros <- kilometros * 1000

    Escribir kilometros, " kilómetros equivalen a ", metros, " metros."
FinAlgoritmo
```

---

## Explicación

La variable `kilometros` guarda el valor ingresado por el usuario.  
La variable `metros` guarda el resultado de la conversión.

---

## Prueba de escritorio

Dato de prueba:

```text
kilometros = 3.5
```

| Paso | kilometros | metros | Salida |
|---|---:|---:|---|
| Inicio | - | - | - |
| Leer kilómetros | 3.5 | - | - |
| Calcular metros | 3.5 | 3500 | - |
| Mostrar resultado | 3.5 | 3500 | 3.5 kilómetros equivalen a 3500 metros |

---

# Ejercicio 4. Salario semanal

## Enunciado

Diseñar un algoritmo que lea las horas trabajadas por una persona y el valor de cada hora. Luego debe mostrar el salario semanal.

---

## Fórmula

```text
salario = horasTrabajadas * valorHora
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `horasTrabajadas`, `valorHora` |
| Proceso | `salario <- horasTrabajadas * valorHora` |
| Salida | Salario semanal |

---

## Algoritmo en lenguaje natural

1. Pedir las horas trabajadas.
2. Pedir el valor de cada hora.
3. Multiplicar las horas trabajadas por el valor de la hora.
4. Mostrar el salario semanal.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo SalarioSemanal
    Definir horasTrabajadas, valorHora, salario Como Real

    Escribir "Ingrese las horas trabajadas:"
    Leer horasTrabajadas

    Escribir "Ingrese el valor de cada hora:"
    Leer valorHora

    salario <- horasTrabajadas * valorHora

    Escribir "El salario semanal es: ", salario
FinAlgoritmo
```

---

## Explicación

El algoritmo multiplica la cantidad de horas trabajadas por el valor pagado por cada hora.

Este ejercicio es secuencial porque no toma decisiones ni repite instrucciones.  
Solo sigue un orden: leer, calcular y mostrar.

---

## Prueba de escritorio

Datos de prueba:

```text
horasTrabajadas = 40
valorHora = 12000
```

| Paso | horasTrabajadas | valorHora | salario | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer horas | 40 | - | - | - |
| Leer valor hora | 40 | 12000 | - | - |
| Calcular salario | 40 | 12000 | 480000 | - |
| Mostrar resultado | 40 | 12000 | 480000 | El salario semanal es: 480000 |

---

# Ejercicio 5. Valor final de una compra

## Enunciado

Diseñar un algoritmo que lea el precio de un producto, la cantidad comprada y muestre el total a pagar.

---

## Fórmula

```text
total = precio * cantidad
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `precio`, `cantidad` |
| Proceso | `total <- precio * cantidad` |
| Salida | Total a pagar |

---

## Algoritmo en lenguaje natural

1. Pedir el precio del producto.
2. Pedir la cantidad comprada.
3. Multiplicar el precio por la cantidad.
4. Mostrar el total a pagar.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo ValorCompra
    Definir precio, total Como Real
    Definir cantidad Como Entero

    Escribir "Ingrese el precio del producto:"
    Leer precio

    Escribir "Ingrese la cantidad comprada:"
    Leer cantidad

    total <- precio * cantidad

    Escribir "El total a pagar es: ", total
FinAlgoritmo
```

---

## Explicación

Se usa `Real` para el precio porque puede tener decimales.  
Se usa `Entero` para la cantidad porque normalmente se compran unidades completas.

---

## Prueba de escritorio

Datos de prueba:

```text
precio = 2500
cantidad = 4
```

| Paso | precio | cantidad | total | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer precio | 2500 | - | - | - |
| Leer cantidad | 2500 | 4 | - | - |
| Calcular total | 2500 | 4 | 10000 | - |
| Mostrar resultado | 2500 | 4 | 10000 | El total a pagar es: 10000 |

---

# Ejercicio 6. Edad aproximada

## Enunciado

Diseñar un algoritmo que lea el año actual y el año de nacimiento de una persona. Luego debe mostrar su edad aproximada.

---

## Fórmula

```text
edad = anioActual - anioNacimiento
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `anioActual`, `anioNacimiento` |
| Proceso | `edad <- anioActual - anioNacimiento` |
| Salida | Edad aproximada |

---

## Algoritmo en lenguaje natural

1. Pedir el año actual.
2. Pedir el año de nacimiento.
3. Restar el año de nacimiento al año actual.
4. Mostrar la edad aproximada.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo EdadAproximada
    Definir anioActual, anioNacimiento, edad Como Entero

    Escribir "Ingrese el año actual:"
    Leer anioActual

    Escribir "Ingrese el año de nacimiento:"
    Leer anioNacimiento

    edad <- anioActual - anioNacimiento

    Escribir "La edad aproximada es: ", edad
FinAlgoritmo
```

---

## Explicación

Este cálculo entrega una edad aproximada porque no tiene en cuenta el mes ni el día de nacimiento.

---

## Prueba de escritorio

Datos de prueba:

```text
anioActual = 2026
anioNacimiento = 2008
```

| Paso | anioActual | anioNacimiento | edad | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer año actual | 2026 | - | - | - |
| Leer año nacimiento | 2026 | 2008 | - | - |
| Calcular edad | 2026 | 2008 | 18 | - |
| Mostrar resultado | 2026 | 2008 | 18 | La edad aproximada es: 18 |

---

# Ejercicio 7. Promedio de tres notas

## Enunciado

Diseñar un algoritmo que lea tres notas y calcule el promedio.

---

## Fórmula

```text
promedio = (nota1 + nota2 + nota3) / 3
```

---

## Análisis del problema

| Elemento | Descripción |
|---|---|
| Entrada | `nota1`, `nota2`, `nota3` |
| Proceso | `promedio <- (nota1 + nota2 + nota3) / 3` |
| Salida | Promedio de las tres notas |

---

## Pseudocódigo en PSeInt

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

Los paréntesis indican que primero se suman las tres notas y luego se divide el resultado entre 3.

---

## Prueba de escritorio

Datos de prueba:

```text
nota1 = 4.0
nota2 = 3.5
nota3 = 5.0
```

| Paso | nota1 | nota2 | nota3 | promedio |
|---|---:|---:|---:|---:|
| Inicio | - | - | - | - |
| Leer nota1 | 4.0 | - | - | - |
| Leer nota2 | 4.0 | 3.5 | - | - |
| Leer nota3 | 4.0 | 3.5 | 5.0 | - |
| Calcular promedio | 4.0 | 3.5 | 5.0 | 4.166 |
| Mostrar resultado | 4.0 | 3.5 | 5.0 | 4.166 |

---

# Recomendación final

Antes de pasar a Java, el estudiante debe lograr explicar cada pseudocódigo con sus propias palabras.

La pregunta clave es:

```text
¿Entiendo qué dato entra, qué proceso se realiza y qué resultado sale?
```
