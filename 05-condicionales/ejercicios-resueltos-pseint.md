# Ejercicios Resueltos en PSeInt: Condicionales

## Presentación

Este archivo contiene ejercicios resueltos de condicionales usando **PSeInt**.

El objetivo es que el estudiante comprenda la lógica de decisión antes de implementar los programas en Java.

Cada ejercicio incluye:

1. Enunciado.
2. Análisis de entrada, proceso y salida.
3. Pseudocódigo en PSeInt.
4. Explicación.
5. Prueba de escritorio.

---

# Ejercicio 1. Mayor de edad

## Enunciado

Leer la edad de una persona e indicar si es mayor o menor de edad.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | edad |
| Proceso | Comparar si `edad >= 18` |
| Salida | Mensaje indicando si es mayor o menor de edad |

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo MayorEdad
    Definir edad Como Entero

    Escribir "Ingrese su edad:"
    Leer edad

    Si edad >= 18 Entonces
        Escribir "La persona es mayor de edad"
    Sino
        Escribir "La persona es menor de edad"
    FinSi
FinAlgoritmo
```

---

## Explicación

La condición principal es:

```pseint
edad >= 18
```

Si la condición es verdadera, se muestra:

```text
La persona es mayor de edad
```

Si la condición es falsa, se muestra:

```text
La persona es menor de edad
```

---

## Prueba de escritorio

| Edad | Condición `edad >= 18` | Salida esperada |
|---:|---|---|
| 20 | Verdadero | La persona es mayor de edad |
| 15 | Falso | La persona es menor de edad |

---

# Ejercicio 2. Número par o impar

## Enunciado

Leer un número entero e indicar si es par o impar.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | numero |
| Proceso | Calcular `numero MOD 2` |
| Salida | Mensaje indicando si es par o impar |

---

## Concepto clave

Un número es par si el residuo al dividirlo entre 2 es igual a 0.

Ejemplo:

```text
10 MOD 2 = 0
11 MOD 2 = 1
```

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo ParImpar
    Definir numero Como Entero

    Escribir "Ingrese un número entero:"
    Leer numero

    Si numero MOD 2 = 0 Entonces
        Escribir "El número es par"
    Sino
        Escribir "El número es impar"
    FinSi
FinAlgoritmo
```

---

## Explicación

La expresión:

```pseint
numero MOD 2 = 0
```

verifica si el residuo de dividir el número entre 2 es cero.

---

## Prueba de escritorio

| Número | `numero MOD 2` | Salida esperada |
|---:|---:|---|
| 10 | 0 | El número es par |
| 11 | 1 | El número es impar |

---

# Ejercicio 3. Mayor de dos números

## Enunciado

Leer dos números e indicar cuál es mayor o si son iguales.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | num1, num2 |
| Proceso | Comparar `num1` y `num2` |
| Salida | Mayor número o mensaje de igualdad |

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo MayorDosNumeros
    Definir num1, num2 Como Real

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    Si num1 > num2 Entonces
        Escribir "El mayor es: ", num1
    Sino
        Si num2 > num1 Entonces
            Escribir "El mayor es: ", num2
        Sino
            Escribir "Los números son iguales"
        FinSi
    FinSi
FinAlgoritmo
```

---

## Explicación

El algoritmo evalúa tres casos:

1. Si el primer número es mayor.
2. Si el segundo número es mayor.
3. Si ninguno es mayor, significa que son iguales.

---

## Prueba de escritorio

| num1 | num2 | Resultado esperado |
|---:|---:|---|
| 8 | 5 | El mayor es 8 |
| 3 | 9 | El mayor es 9 |
| 6 | 6 | Los números son iguales |

---

# Ejercicio 4. Validar nota

## Enunciado

Leer una nota e indicar si está en el rango válido de 0.0 a 5.0.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | nota |
| Proceso | Verificar si `nota >= 0.0 Y nota <= 5.0` |
| Salida | Mensaje de nota válida o no válida |

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo ValidarNota
    Definir nota Como Real

    Escribir "Ingrese la nota:"
    Leer nota

    Si nota >= 0.0 Y nota <= 5.0 Entonces
        Escribir "La nota es válida"
    Sino
        Escribir "La nota no es válida"
    FinSi
FinAlgoritmo
```

---

## Explicación

Se usa el operador lógico `Y` porque se deben cumplir dos condiciones al mismo tiempo:

```text
La nota debe ser mayor o igual a 0.0
La nota debe ser menor o igual a 5.0
```

---

## Prueba de escritorio

| Nota | Condición | Salida esperada |
|---:|---|---|
| 4.2 | Verdadero | La nota es válida |
| -1.0 | Falso | La nota no es válida |
| 6.0 | Falso | La nota no es válida |

---

# Ejercicio 5. Validar nota y determinar aprobación

## Enunciado

Leer una nota. Si está fuera del rango 0.0 a 5.0, mostrar que no es válida. Si es válida, indicar si aprueba o reprueba.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | nota |
| Proceso | Validar rango y luego comparar con 3.0 |
| Salida | Nota no válida, aprobó o reprobó |

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo ValidarYAprobar
    Definir nota Como Real

    Escribir "Ingrese la nota:"
    Leer nota

    Si nota < 0.0 O nota > 5.0 Entonces
        Escribir "Nota no válida"
    Sino
        Si nota >= 3.0 Entonces
            Escribir "Nota válida. El estudiante aprobó"
        Sino
            Escribir "Nota válida. El estudiante reprobó"
        FinSi
    FinSi
FinAlgoritmo
```

---

## Explicación

Primero se revisa si la nota está fuera del rango:

```pseint
nota < 0.0 O nota > 5.0
```

Si eso se cumple, se muestra que la nota no es válida.

Si la nota sí está dentro del rango, se evalúa si es mayor o igual a 3.0.

---

## Prueba de escritorio

| Nota | Resultado esperado |
|---:|---|
| -0.5 | Nota no válida |
| 2.8 | Nota válida. El estudiante reprobó |
| 3.7 | Nota válida. El estudiante aprobó |
| 5.5 | Nota no válida |

---

# Ejercicio 6. Desempeño académico

## Enunciado

Leer una nota y mostrar el desempeño académico.

Criterios:

| Rango | Desempeño |
|---|---|
| Menor que 3.0 | Bajo |
| Desde 3.0 hasta menor que 4.0 | Básico |
| Desde 4.0 hasta menor que 4.6 | Alto |
| Desde 4.6 hasta 5.0 | Superior |

También se debe validar que la nota esté entre 0.0 y 5.0.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo DesempenoAcademico
    Definir nota Como Real

    Escribir "Ingrese la nota:"
    Leer nota

    Si nota < 0.0 O nota > 5.0 Entonces
        Escribir "Nota no válida"
    Sino
        Si nota < 3.0 Entonces
            Escribir "Desempeño bajo"
        Sino
            Si nota < 4.0 Entonces
                Escribir "Desempeño básico"
            Sino
                Si nota < 4.6 Entonces
                    Escribir "Desempeño alto"
                Sino
                    Escribir "Desempeño superior"
                FinSi
            FinSi
        FinSi
    FinSi
FinAlgoritmo
```

---

## Explicación

El algoritmo primero valida el rango de la nota.  
Después clasifica el desempeño usando condicionales anidados.

---

## Prueba de escritorio

| Nota | Salida esperada |
|---:|---|
| -1.0 | Nota no válida |
| 2.5 | Desempeño bajo |
| 3.5 | Desempeño básico |
| 4.2 | Desempeño alto |
| 4.8 | Desempeño superior |
| 6.0 | Nota no válida |

---

# Ejercicio 7. Descuento en compra

## Enunciado

Leer el valor de una compra. Si supera 100000, aplicar descuento del 10%. Si no, no aplicar descuento. Mostrar el descuento y el total a pagar.

---

## Análisis

| Elemento | Descripción |
|---|---|
| Entrada | valorCompra |
| Proceso | Si valorCompra > 100000, descuento = valorCompra * 0.10 |
| Salida | descuento y total |

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo DescuentoCompra
    Definir valorCompra, descuento, total Como Real

    Escribir "Ingrese el valor de la compra:"
    Leer valorCompra

    Si valorCompra > 100000 Entonces
        descuento <- valorCompra * 0.10
    Sino
        descuento <- 0
    FinSi

    total <- valorCompra - descuento

    Escribir "Valor de la compra: ", valorCompra
    Escribir "Descuento: ", descuento
    Escribir "Total a pagar: ", total
FinAlgoritmo
```

---

## Prueba de escritorio

| Valor compra | Descuento | Total |
|---:|---:|---:|
| 150000 | 15000 | 135000 |
| 80000 | 0 | 80000 |

---

# Ejercicio 8. Menú básico con `Segun`

## Enunciado

Crear un algoritmo que muestre un menú con tres opciones:

1. Saludar.
2. Mostrar el nombre del curso.
3. Salir.

Si la opción no existe, mostrar opción no válida.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo MenuBasico
    Definir opcion Como Entero

    Escribir "===== MENÚ ====="
    Escribir "1. Saludar"
    Escribir "2. Mostrar curso"
    Escribir "3. Salir"
    Escribir "Ingrese una opción:"
    Leer opcion

    Segun opcion Hacer
        1:
            Escribir "Hola, bienvenido"
        2:
            Escribir "Curso de Algoritmia y Programación"
        3:
            Escribir "Saliendo del programa"
        De Otro Modo:
            Escribir "Opción no válida"
    FinSegun
FinAlgoritmo
```

---

## Explicación

La estructura `Segun` evalúa el valor de `opcion`.

Si `opcion` vale 1, ejecuta el caso 1.  
Si vale 2, ejecuta el caso 2.  
Si vale 3, ejecuta el caso 3.  
Si no coincide con ninguno, ejecuta `De Otro Modo`.

---

## Prueba de escritorio

| Opción | Salida esperada |
|---:|---|
| 1 | Hola, bienvenido |
| 2 | Curso de Algoritmia y Programación |
| 3 | Saliendo del programa |
| 8 | Opción no válida |

---

# Ejercicio 9. Calculadora básica con `Segun`

## Enunciado

Leer dos números y una opción. Según la opción, realizar:

1. Sumar.
2. Restar.
3. Multiplicar.
4. Dividir.

Validar división entre cero.

---

## Pseudocódigo en PSeInt

```pseint
Algoritmo CalculadoraBasica
    Definir num1, num2 Como Real
    Definir opcion Como Entero

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    Escribir "1. Sumar"
    Escribir "2. Restar"
    Escribir "3. Multiplicar"
    Escribir "4. Dividir"
    Escribir "Ingrese una opción:"
    Leer opcion

    Segun opcion Hacer
        1:
            Escribir "Resultado: ", num1 + num2
        2:
            Escribir "Resultado: ", num1 - num2
        3:
            Escribir "Resultado: ", num1 * num2
        4:
            Si num2 <> 0 Entonces
                Escribir "Resultado: ", num1 / num2
            Sino
                Escribir "No se puede dividir entre cero"
            FinSi
        De Otro Modo:
            Escribir "Opción no válida"
    FinSegun
FinAlgoritmo
```

---

## Explicación

Para dividir se valida que `num2` sea diferente de cero:

```pseint
num2 <> 0
```

Si `num2` vale cero, no se realiza la división.

---

## Prueba de escritorio

| num1 | num2 | opción | Salida esperada |
|---:|---:|---:|---|
| 8 | 4 | 1 | Resultado: 12 |
| 8 | 4 | 2 | Resultado: 4 |
| 8 | 4 | 3 | Resultado: 32 |
| 8 | 4 | 4 | Resultado: 2 |
| 8 | 0 | 4 | No se puede dividir entre cero |
| 8 | 4 | 9 | Opción no válida |

---

# Recomendación final

Para dominar condicionales en PSeInt, el estudiante debe probar varios datos.

Cada condicional representa caminos diferentes.  
Si solo se prueba un caso, no se puede asegurar que el algoritmo funciona correctamente.
