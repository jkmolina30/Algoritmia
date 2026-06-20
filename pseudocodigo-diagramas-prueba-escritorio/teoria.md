# Unidad 3. Pseudocódigo, Diagramas de Flujo y Prueba de Escritorio

## Presentación de la unidad

Antes de escribir código en Java, es importante aprender a representar una solución de forma clara.

Para eso se usan herramientas como:

- Lenguaje natural.
- Pseudocódigo.
- Diagramas de flujo.
- Prueba de escritorio.

Estas herramientas ayudan a organizar el pensamiento lógico antes de programar.

---

## 1. ¿Qué es pseudocódigo?

El **pseudocódigo** es una forma de escribir algoritmos usando instrucciones parecidas al lenguaje humano y a los lenguajes de programación.

No es un lenguaje de programación formal como Java, pero sirve para diseñar la solución.

Ejemplo:

```pseint
Algoritmo Saludo
    Definir nombre Como Caracter

    Escribir "Ingrese su nombre:"
    Leer nombre

    Escribir "Hola ", nombre
FinAlgoritmo
```

---

## 2. ¿Para qué sirve el pseudocódigo?

Sirve para:

- Organizar la lógica.
- Entender el problema antes de programar.
- Representar pasos de forma clara.
- Evitar depender de la sintaxis de Java desde el inicio.
- Facilitar la prueba de escritorio.
- Preparar la solución antes de implementarla.

---

## 3. Ventajas del pseudocódigo

| Ventaja | Explicación |
|---|---|
| Es más fácil de leer | Usa instrucciones cercanas al lenguaje humano |
| Ayuda a pensar | Permite concentrarse en la lógica |
| Evita errores iniciales de sintaxis | No exige tantas reglas como Java |
| Facilita el paso a código | Sirve como puente hacia Java |
| Permite explicar soluciones | Es útil para socializar la lógica |

---

## 4. Estructura básica de un algoritmo en PSeInt

```pseint
Algoritmo NombreDelAlgoritmo
    Definir variable Como Tipo

    Escribir "Mensaje"
    Leer variable

    // Procesos

    Escribir "Resultado"
FinAlgoritmo
```

---

## 5. Partes principales de un algoritmo

| Parte | Función |
|---|---|
| Nombre del algoritmo | Identifica la solución |
| Declaración de variables | Define los datos que se usarán |
| Entrada | Recibe datos del usuario |
| Proceso | Realiza operaciones |
| Salida | Muestra resultados |
| Fin | Indica que el algoritmo termina |

---

## 6. Entrada en pseudocódigo

La entrada se realiza con `Leer`.

```pseint
Leer edad
```

Esto significa que el usuario debe ingresar un valor, y ese valor se guarda en la variable `edad`.

---

## 7. Salida en pseudocódigo

La salida se realiza con `Escribir`.

```pseint
Escribir "Hola mundo"
```

También se puede mostrar texto junto con variables:

```pseint
Escribir "La edad es: ", edad
```

---

## 8. Proceso en pseudocódigo

El proceso corresponde a las operaciones.

```pseint
promedio <- (nota1 + nota2 + nota3) / 3
```

El símbolo `<-` indica asignación.

Lectura sencilla:

```text
A la variable promedio se le asigna el resultado de sumar las tres notas y dividir entre tres.
```

---

## 9. ¿Qué es un diagrama de flujo?

Un **diagrama de flujo** es una representación gráfica de un algoritmo.

Muestra los pasos mediante símbolos conectados por flechas.

Permite visualizar el orden de ejecución de una solución.

---

## 10. ¿Para qué sirven los diagramas de flujo?

Sirven para:

- Representar gráficamente un algoritmo.
- Visualizar el flujo de instrucciones.
- Entender decisiones y procesos.
- Detectar errores de orden.
- Explicar soluciones de forma visual.

---

## 11. Símbolos básicos de diagramas de flujo

| Símbolo | Nombre | Uso |
|---|---|---|
| Óvalo | Inicio/Fin | Indica dónde empieza o termina |
| Paralelogramo | Entrada/Salida | Leer o mostrar datos |
| Rectángulo | Proceso | Cálculos u operaciones |
| Rombo | Decisión | Condiciones |
| Flecha | Flujo | Dirección del proceso |

---

## 12. Ejemplo de algoritmo secuencial

Problema:

```text
Calcular el área de un rectángulo.
```

### Pseudocódigo

```pseint
Algoritmo AreaRectangulo
    Definir base, altura, area Como Real

    Escribir "Ingrese la base:"
    Leer base

    Escribir "Ingrese la altura:"
    Leer altura

    area <- base * altura

    Escribir "El área es: ", area
FinAlgoritmo
```

---

## 13. ¿Qué es la prueba de escritorio?

La **prueba de escritorio** es una revisión manual del algoritmo usando datos de prueba.

Se hace una tabla donde se observa cómo cambian las variables.

Ejemplo:

| Paso | base | altura | area | Salida |
|---|---:|---:|---:|---|
| Inicio | - | - | - | - |
| Leer base | 5 | - | - | - |
| Leer altura | 5 | 4 | - | - |
| Calcular área | 5 | 4 | 20 | - |
| Mostrar área | 5 | 4 | 20 | 20 |

---

## 14. Relación entre pseudocódigo, diagrama y prueba

| Herramienta | Función |
|---|---|
| Pseudocódigo | Escribe la solución de forma estructurada |
| Diagrama de flujo | Representa la solución gráficamente |
| Prueba de escritorio | Verifica manualmente si funciona |

---

## 15. Proceso recomendado para resolver problemas

```text
Leer el problema
    ↓
Identificar entradas, proceso y salida
    ↓
Escribir lenguaje natural
    ↓
Crear pseudocódigo
    ↓
Diseñar diagrama de flujo
    ↓
Hacer prueba de escritorio
    ↓
Pasar a Java
```

---

## 16. Ejemplo completo

### Problema

Leer dos números y mostrar la suma.

### Entrada

```text
num1, num2
```

### Proceso

```text
suma = num1 + num2
```

### Salida

```text
suma
```

### Pseudocódigo

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

### Prueba de escritorio

| Paso | num1 | num2 | suma |
|---|---:|---:|---:|
| Inicio | - | - | - |
| Leer num1 | 8 | - | - |
| Leer num2 | 8 | 5 | - |
| Calcular suma | 8 | 5 | 13 |
| Mostrar suma | 8 | 5 | 13 |

---

## 17. Buenas prácticas

- No escribir Java sin haber entendido el problema.
- Usar nombres claros para variables.
- Mantener el pseudocódigo ordenado.
- Verificar cada fórmula.
- Usar diagramas cuando el problema tenga varios pasos.
- Hacer prueba de escritorio antes de ejecutar.
- Probar con más de un caso.

---

## 18. Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder representar soluciones mediante pseudocódigo, diagramas de flujo y pruebas de escritorio, como paso previo a la implementación en Java.
