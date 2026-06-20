# Funciones y Subprocesos en PSeInt

## Presentación

En PSeInt se pueden crear bloques separados para organizar mejor los algoritmos.

Estos bloques pueden ser:

- Funciones.
- Subprocesos.

Una función generalmente devuelve un valor.  
Un subproceso realiza una tarea, pero no necesariamente devuelve un valor.

---

# 1. Función en PSeInt

Una función permite calcular un resultado y devolverlo.

## Ejemplo: sumar dos números

```pseint
Funcion resultado <- Sumar(a, b)
    Definir resultado Como Entero

    resultado <- a + b
FinFuncion
```

---

## Uso de la función

```pseint
Algoritmo EjemploFuncionSuma
    Definir num1, num2, suma Como Entero

    Escribir "Ingrese el primer número:"
    Leer num1

    Escribir "Ingrese el segundo número:"
    Leer num2

    suma <- Sumar(num1, num2)

    Escribir "La suma es: ", suma
FinAlgoritmo

Funcion resultado <- Sumar(a, b)
    Definir resultado Como Entero

    resultado <- a + b
FinFuncion
```

---

# 2. Explicación

```pseint
Funcion resultado <- Sumar(a, b)
```

Define una función llamada `Sumar`.

La función recibe dos valores: `a` y `b`.

```pseint
resultado <- a + b
```

Calcula la suma.

```pseint
FinFuncion
```

Indica el final de la función.

---

# 3. Subproceso en PSeInt

Un subproceso permite ejecutar instrucciones sin devolver necesariamente un valor.

## Ejemplo

```pseint
SubProceso MostrarMenu()
    Escribir "1. Sumar"
    Escribir "2. Restar"
    Escribir "3. Salir"
FinSubProceso
```

---

## Uso del subproceso

```pseint
Algoritmo EjemploMenu
    MostrarMenu()
FinAlgoritmo

SubProceso MostrarMenu()
    Escribir "1. Sumar"
    Escribir "2. Restar"
    Escribir "3. Salir"
FinSubProceso
```

---

# 4. Función para calcular promedio

```pseint
Algoritmo PromedioConFuncion
    Definir nota1, nota2, nota3, promedio Como Real

    Escribir "Ingrese la primera nota:"
    Leer nota1

    Escribir "Ingrese la segunda nota:"
    Leer nota2

    Escribir "Ingrese la tercera nota:"
    Leer nota3

    promedio <- CalcularPromedio(nota1, nota2, nota3)

    Escribir "El promedio es: ", promedio
FinAlgoritmo

Funcion resultado <- CalcularPromedio(n1, n2, n3)
    Definir resultado Como Real

    resultado <- (n1 + n2 + n3) / 3
FinFuncion
```

---

# 5. Función para validar nota

```pseint
Algoritmo ValidarNotaFuncion
    Definir nota Como Real
    Definir esValida Como Logico

    Escribir "Ingrese una nota:"
    Leer nota

    esValida <- ValidarNota(nota)

    Si esValida Entonces
        Escribir "La nota es válida"
    Sino
        Escribir "La nota no es válida"
    FinSi
FinAlgoritmo

Funcion resultado <- ValidarNota(nota)
    Definir resultado Como Logico

    resultado <- nota >= 0.0 Y nota <= 5.0
FinFuncion
```

---

# 6. Subproceso para mostrar datos

```pseint
Algoritmo MostrarDatosEstudiante
    Definir nombre Como Caracter
    Definir nota Como Real

    Escribir "Ingrese el nombre:"
    Leer nombre

    Escribir "Ingrese la nota:"
    Leer nota

    MostrarResultado(nombre, nota)
FinAlgoritmo

SubProceso MostrarResultado(nombre, nota)
    Escribir "Estudiante: ", nombre
    Escribir "Nota final: ", nota
FinSubProceso
```

---

# 7. Buenas prácticas en PSeInt

- Usar funciones para cálculos.
- Usar subprocesos para mostrar información o menús.
- Dar nombres claros.
- No hacer funciones demasiado largas.
- Probar cada función con datos sencillos.
- No repetir código si se puede crear una función.

---

# 8. Ejercicios rápidos

1. Crear una función que reciba dos números y devuelva la resta.
2. Crear una función que calcule el área de un rectángulo.
3. Crear una función que calcule el área de un triángulo.
4. Crear una función que valide si una edad está entre 0 y 120.
5. Crear un subproceso que muestre un menú de operaciones.
