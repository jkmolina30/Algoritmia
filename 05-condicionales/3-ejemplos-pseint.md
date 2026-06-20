# Ejemplos en PSeInt: Condicionales

## Presentación

Aunque de ahora en adelante el curso se enfocará más en Java, PSeInt sigue siendo útil para comprender primero la lógica de decisión.

Este archivo presenta ejemplos cortos en PSeInt para reforzar la idea de condición, decisión y salida.

---

# Ejemplo 1. Mayor de edad

## Problema

Leer la edad de una persona e indicar si es mayor de edad.

## Pseudocódigo

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

## Explicación

La condición es:

```pseint
edad >= 18
```

Si la condición es verdadera, se muestra que la persona es mayor de edad.  
Si es falsa, se muestra que es menor de edad.

---

# Ejemplo 2. Número positivo, negativo o cero

## Problema

Leer un número e indicar si es positivo, negativo o cero.

## Pseudocódigo

```pseint
Algoritmo PositivoNegativoCero
    Definir numero Como Real

    Escribir "Ingrese un número:"
    Leer numero

    Si numero > 0 Entonces
        Escribir "El número es positivo"
    Sino
        Si numero < 0 Entonces
            Escribir "El número es negativo"
        Sino
            Escribir "El número es cero"
        FinSi
    FinSi
FinAlgoritmo
```

---

# Ejemplo 3. Nota aprobada o reprobada

```pseint
Algoritmo AprobarMateria
    Definir nota Como Real

    Escribir "Ingrese la nota final:"
    Leer nota

    Si nota >= 3.0 Entonces
        Escribir "El estudiante aprobó"
    Sino
        Escribir "El estudiante reprobó"
    FinSi
FinAlgoritmo
```

---

# Ejemplo 4. Validar rango de nota

## Problema

Leer una nota y verificar si está en el rango permitido de 0.0 a 5.0.

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

# Ejemplo 5. Desempeño académico

## Problema

Leer una nota y mostrar el desempeño.

Criterio:

- Menor que 3.0: bajo.
- Desde 3.0 hasta menor que 4.0: básico.
- Desde 4.0 hasta menor que 4.6: alto.
- Desde 4.6 hasta 5.0: superior.

```pseint
Algoritmo DesempenoAcademico
    Definir nota Como Real

    Escribir "Ingrese la nota:"
    Leer nota

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
FinAlgoritmo
```

---

# Ejemplo 6. Menú básico

## Problema

Leer una opción y mostrar una operación simulada.

```pseint
Algoritmo MenuBasico
    Definir opcion Como Entero

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

## Recomendación

Después de entender cada ejemplo en PSeInt, el estudiante debe implementarlo en Java para practicar sintaxis formal.
