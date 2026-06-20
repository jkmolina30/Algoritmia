# Teoría de Condicionales en PSeInt

## Unidad 4. Condicionales

## Presentación

Antes de trabajar condicionales en Java, es importante comprender la lógica de decisión usando **PSeInt**.

PSeInt permite escribir algoritmos en pseudocódigo, usando una sintaxis más cercana al lenguaje natural. Esto ayuda a que el estudiante entienda primero la lógica antes de preocuparse por la sintaxis estricta de Java.

En esta unidad se estudiarán las estructuras condicionales en PSeInt:

- Condicional simple.
- Condicional doble.
- Condicional anidado.
- Condicional múltiple.
- Estructura `Segun`.
- Operadores relacionales.
- Operadores lógicos.
- Validación básica de datos.

---

## 1. ¿Qué es una condición?

Una condición es una expresión que puede ser verdadera o falsa.

Ejemplo:

```pseint
edad >= 18
```

Esta condición pregunta:

```text
¿La edad es mayor o igual a 18?
```

Si la edad vale 20, la respuesta es verdadera.  
Si la edad vale 15, la respuesta es falsa.

---

## 2. ¿Para qué sirven los condicionales?

Los condicionales permiten que un algoritmo tome decisiones.

Ejemplo cotidiano:

```text
Si la nota es mayor o igual a 3.0, el estudiante aprueba.
Si no, el estudiante reprueba.
```

En PSeInt:

```pseint
Si nota >= 3.0 Entonces
    Escribir "Aprobó"
Sino
    Escribir "Reprobó"
FinSi
```

---

## 3. Operadores relacionales en PSeInt

Los operadores relacionales permiten comparar valores.

| Operador | Significado | Ejemplo |
|---|---|---|
| `>` | Mayor que | `edad > 18` |
| `<` | Menor que | `edad < 18` |
| `>=` | Mayor o igual que | `nota >= 3.0` |
| `<=` | Menor o igual que | `nota <= 5.0` |
| `=` | Igual que | `opcion = 1` |
| `<>` | Diferente de | `opcion <> 0` |

---

## 4. Diferencia importante con Java

En PSeInt, para comparar igualdad se usa:

```pseint
opcion = 1
```

En Java, para comparar igualdad se usa:

```java
opcion == 1
```

Por eso se debe tener cuidado al pasar un algoritmo de PSeInt a Java.

| Comparación | PSeInt | Java |
|---|---|---|
| Igualdad | `opcion = 1` | `opcion == 1` |
| Diferente | `opcion <> 1` | `opcion != 1` |

---

## 5. Operadores lógicos en PSeInt

Los operadores lógicos permiten combinar varias condiciones.

| Operador | Significado | Ejemplo |
|---|---|---|
| `Y` | Ambas condiciones deben cumplirse | `nota >= 0 Y nota <= 5` |
| `O` | Al menos una condición debe cumplirse | `opcion = 1 O opcion = 2` |
| `NO` | Niega una condición | `NO aprobado` |

---

## 6. Ejemplo con operador `Y`

Problema:

Una nota es válida si está entre 0.0 y 5.0.

```pseint
Si nota >= 0.0 Y nota <= 5.0 Entonces
    Escribir "Nota válida"
Sino
    Escribir "Nota no válida"
FinSi
```

Explicación:

La nota será válida solo si se cumplen las dos condiciones:

```text
nota >= 0.0
nota <= 5.0
```

---

## 7. Ejemplo con operador `O`

Problema:

Una opción es válida si es 1 o 2.

```pseint
Si opcion = 1 O opcion = 2 Entonces
    Escribir "Opción válida"
Sino
    Escribir "Opción no válida"
FinSi
```

La condición será verdadera si al menos una de las dos comparaciones se cumple.

---

# 8. Condicional simple

El condicional simple se usa cuando solo queremos ejecutar instrucciones si una condición es verdadera.

## Sintaxis

```pseint
Si condicion Entonces
    instrucciones
FinSi
```

## Ejemplo

```pseint
Si edad >= 18 Entonces
    Escribir "La persona es mayor de edad"
FinSi
```

Si la condición no se cumple, el algoritmo simplemente continúa.

---

# 9. Condicional doble

El condicional doble permite ejecutar una acción si la condición es verdadera y otra si es falsa.

## Sintaxis

```pseint
Si condicion Entonces
    instrucciones si la condición es verdadera
Sino
    instrucciones si la condición es falsa
FinSi
```

## Ejemplo

```pseint
Si nota >= 3.0 Entonces
    Escribir "Aprobó"
Sino
    Escribir "Reprobó"
FinSi
```

---

# 10. Condicional anidado

Un condicional anidado es un condicional dentro de otro.

## Ejemplo

```pseint
Si nota >= 0.0 Y nota <= 5.0 Entonces
    Si nota >= 3.0 Entonces
        Escribir "Aprobó"
    Sino
        Escribir "Reprobó"
    FinSi
Sino
    Escribir "Nota no válida"
FinSi
```

Explicación:

Primero se valida si la nota está entre 0.0 y 5.0.  
Si la nota es válida, se revisa si aprueba o reprueba.  
Si la nota no es válida, se muestra un mensaje de error.

---

# 11. Condicional múltiple usando `Si`, `Sino`, `Si`

En PSeInt se pueden encadenar condicionales para evaluar varias posibilidades.

## Ejemplo

```pseint
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
```

Este tipo de estructura se usa cuando hay varias categorías.

---

# 12. Estructura `Segun`

La estructura `Segun` se usa cuando una variable puede tomar varios valores específicos.

Es muy útil para menús.

## Sintaxis

```pseint
Segun variable Hacer
    valor1:
        instrucciones
    valor2:
        instrucciones
    De Otro Modo:
        instrucciones
FinSegun
```

---

## Ejemplo de `Segun`

```pseint
Segun opcion Hacer
    1:
        Escribir "Saludar"
    2:
        Escribir "Mostrar curso"
    3:
        Escribir "Salir"
    De Otro Modo:
        Escribir "Opción no válida"
FinSegun
```

---

# 13. Diferencia entre `Si` y `Segun`

| Estructura | Uso recomendado |
|---|---|
| `Si` | Cuando se evalúan condiciones generales |
| `Segun` | Cuando una variable tiene opciones exactas |

Ejemplo para `Si`:

```pseint
Si nota >= 3.0 Entonces
```

Ejemplo para `Segun`:

```pseint
Segun opcion Hacer
```

---

# 14. Validación de datos en PSeInt

Validar significa revisar si un dato cumple una condición antes de procesarlo.

Ejemplo:

```pseint
Si edad >= 0 Y edad <= 120 Entonces
    Escribir "Edad válida"
Sino
    Escribir "Edad no válida"
FinSi
```

La validación evita que el algoritmo trabaje con datos incorrectos.

---

# 15. Ejemplo completo: validar nota y desempeño

```pseint
Algoritmo ValidarNotaYDesempeno
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

# 16. Prueba de escritorio para condicionales

Cuando se trabaja con condicionales, se deben probar varios casos.

Ejemplo:

Para una nota se deben probar valores como:

| Nota | Resultado esperado |
|---:|---|
| -1.0 | Nota no válida |
| 2.5 | Desempeño bajo |
| 3.5 | Desempeño básico |
| 4.2 | Desempeño alto |
| 4.8 | Desempeño superior |
| 5.5 | Nota no válida |

No basta con probar un solo dato.

---

# 17. Errores comunes en PSeInt

## Error 1. Olvidar `FinSi`

Incorrecto:

```pseint
Si edad >= 18 Entonces
    Escribir "Mayor de edad"
```

Correcto:

```pseint
Si edad >= 18 Entonces
    Escribir "Mayor de edad"
FinSi
```

---

## Error 2. Confundir `Y` con `O`

Incorrecto para validar nota:

```pseint
Si nota >= 0 O nota <= 5 Entonces
```

Esto casi siempre será verdadero.

Correcto:

```pseint
Si nota >= 0 Y nota <= 5 Entonces
```

---

## Error 3. No contemplar todos los casos

Ejemplo incompleto:

```pseint
Si numero > 0 Entonces
    Escribir "Positivo"
FinSi
```

Este algoritmo no indica qué pasa si el número es negativo o cero.

---

## Error 4. Evaluar mal los rangos

Incorrecto:

```pseint
Si nota >= 3.0 Y nota >= 4.0 Entonces
```

Esta condición no representa un rango entre 3.0 y 4.0.

Correcto:

```pseint
Si nota >= 3.0 Y nota < 4.0 Entonces
```

---

# 18. Buenas prácticas en condicionales con PSeInt

- Usar nombres de variables claros.
- Validar los datos antes de clasificarlos.
- Usar `Y` cuando todas las condiciones deben cumplirse.
- Usar `O` cuando basta con que una condición se cumpla.
- Cerrar cada estructura con `FinSi` o `FinSegun`.
- Hacer prueba de escritorio con varios casos.
- Mantener una buena indentación.
- No hacer condicionales más complicados de lo necesario.

---

# 19. Relación con Java

Después de entender la lógica en PSeInt, se puede pasar a Java.

| PSeInt | Java |
|---|---|
| `Si condicion Entonces` | `if (condicion) {` |
| `Sino` | `} else {` |
| `FinSi` | `}` |
| `Y` | `&&` |
| `O` | `||` |
| `=` para comparar | `==` |
| `<>` | `!=` |
| `Segun` | `switch` |

---

# 20. Resultado de aprendizaje

Al finalizar este archivo, el estudiante debe poder construir algoritmos en PSeInt que tomen decisiones usando `Si`, `Sino`, condicionales anidados, operadores relacionales, operadores lógicos y la estructura `Segun`.
