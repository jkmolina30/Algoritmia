# Ejercicios Propuestos en Java

## Unidad 2. Introducción a la Algoritmia

Este archivo contiene ejercicios propuestos para resolver en **Java**.

El propósito es que el estudiante practique la implementación de problemas secuenciales usando:

- Variables.
- Tipos de datos básicos.
- Entrada de datos con `Scanner`.
- Operaciones aritméticas.
- Salida de datos con `System.out.println`.
- Buenas prácticas iniciales de programación.

---

## Instrucciones generales

Para cada ejercicio se debe entregar:

1. Análisis de entrada, proceso y salida.
2. Código Java.
3. Prueba de escritorio.
4. Captura o evidencia de ejecución si el docente lo solicita.
5. Explicación breve de la solución.

---

## Estructura base sugerida

```java
import java.util.Scanner;

public class NombreDelEjercicio {
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        // Declaración de variables

        // Entrada de datos

        // Proceso

        // Salida de datos

        entrada.close();
    }
}
```

---

## Recomendaciones para nombrar archivos y clases

En Java, si la clase es pública, el archivo debe llamarse igual que la clase.

Ejemplo:

Archivo:

```text
PromedioTresNotas.java
```

Clase:

```java
public class PromedioTresNotas {
}
```

También se recomienda usar nombres claros:

| Mal nombre | Buen nombre |
|---|---|
| `Ej1` | `SumaDosNumeros` |
| `Programa` | `AreaRectangulo` |
| `Prueba` | `PromedioNotas` |

---

# Nivel 1. Ejercicios básicos

## Ejercicio 1. Saludo personalizado

Crear un programa que lea el nombre de una persona y muestre un saludo personalizado.

Ejemplo de salida:

```text
Hola, Ana. Bienvenida al curso de Algoritmia.
```

Nombre sugerido de la clase:

```java
SaludoPersonalizado
```

---

## Ejercicio 2. Suma de dos números

Crear un programa que lea dos números enteros y muestre su suma.

Nombre sugerido:

```java
SumaDosNumeros
```

---

## Ejercicio 3. Resta de dos números

Crear un programa que lea dos números enteros y muestre su resta.

---

## Ejercicio 4. Multiplicación de dos números

Crear un programa que lea dos números enteros y muestre su multiplicación.

---

## Ejercicio 5. División de dos números

Crear un programa que lea dos números reales y muestre el resultado de la división.

Nota: en esta unidad no se validará división entre cero. Esa validación se trabajará cuando se estudien condicionales.

---

## Ejercicio 6. Doble de un número

Crear un programa que lea un número entero y muestre su doble.

---

## Ejercicio 7. Triple de un número

Crear un programa que lea un número entero y muestre su triple.

---

## Ejercicio 8. Cuadrado de un número

Crear un programa que lea un número entero y muestre su cuadrado.

Fórmula:

```text
cuadrado = numero * numero
```

---

## Ejercicio 9. Horas a minutos

Crear un programa que lea una cantidad de horas y la convierta a minutos.

Fórmula:

```text
minutos = horas * 60
```

---

## Ejercicio 10. Minutos a segundos

Crear un programa que lea una cantidad de minutos y la convierta a segundos.

Fórmula:

```text
segundos = minutos * 60
```

---

# Nivel 2. Ejercicios con fórmulas geométricas

## Ejercicio 11. Área de un rectángulo

Crear un programa que lea la base y la altura de un rectángulo. Calcular y mostrar su área.

Fórmula:

```text
area = base * altura
```

Nombre sugerido:

```java
AreaRectangulo
```

---

## Ejercicio 12. Perímetro de un rectángulo

Crear un programa que lea la base y la altura de un rectángulo. Calcular y mostrar su perímetro.

Fórmula:

```text
perimetro = 2 * (base + altura)
```

---

## Ejercicio 13. Área de un triángulo

Crear un programa que lea la base y la altura de un triángulo. Calcular y mostrar su área.

Fórmula:

```text
area = (base * altura) / 2
```

---

## Ejercicio 14. Área de un cuadrado

Crear un programa que lea el lado de un cuadrado. Calcular y mostrar su área.

Fórmula:

```text
area = lado * lado
```

---

## Ejercicio 15. Perímetro de un cuadrado

Crear un programa que lea el lado de un cuadrado. Calcular y mostrar su perímetro.

Fórmula:

```text
perimetro = lado * 4
```

---

## Ejercicio 16. Área de un círculo

Crear un programa que lea el radio de un círculo. Calcular y mostrar su área.

Fórmula:

```text
area = 3.1416 * radio * radio
```

---

## Ejercicio 17. Longitud de una circunferencia

Crear un programa que lea el radio de una circunferencia. Calcular y mostrar su longitud.

Fórmula:

```text
longitud = 2 * 3.1416 * radio
```

---

# Nivel 3. Ejercicios académicos

## Ejercicio 18. Promedio de tres notas

Crear un programa que lea tres notas de un estudiante y calcule el promedio.

---

## Ejercicio 19. Promedio de cuatro notas

Crear un programa que lea cuatro notas de un estudiante y calcule el promedio.

---

## Ejercicio 20. Nota definitiva con porcentajes

Crear un programa que lea tres notas:

- Primer corte.
- Segundo corte.
- Tercer corte.

Calcular la nota definitiva sabiendo que:

```text
Primer corte = 30%
Segundo corte = 30%
Tercer corte = 40%
```

Fórmula:

```text
definitiva = corte1 * 0.30 + corte2 * 0.30 + corte3 * 0.40
```

---

## Ejercicio 21. Datos de estudiante

Crear un programa que lea el nombre de un estudiante, el nombre de una asignatura y la nota final. Mostrar un mensaje con esos datos.

Ejemplo:

```text
El estudiante Carlos obtuvo 4.2 en Algoritmia.
```

Nota técnica:

Si se combina `nextDouble()` con `nextLine()`, se debe limpiar el salto de línea pendiente.

Ejemplo:

```java
entrada.nextLine();
```

---

## Ejercicio 22. Sillas disponibles

Crear un programa que lea la cantidad de estudiantes de un grupo y la cantidad de sillas disponibles. Mostrar la diferencia entre sillas y estudiantes.

Nota: la interpretación de si sobran o faltan sillas se trabajará con condicionales.

---

# Nivel 4. Ejercicios aplicados

## Ejercicio 23. Valor total de una compra

Crear un programa que lea el precio de un producto y la cantidad comprada. Calcular el total a pagar.

Fórmula:

```text
total = precio * cantidad
```

---

## Ejercicio 24. Cambio de una compra

Crear un programa que lea el valor de una compra y el dinero entregado por el cliente. Calcular el cambio.

Fórmula:

```text
cambio = dineroEntregado - valorCompra
```

---

## Ejercicio 25. Salario semanal

Crear un programa que lea las horas trabajadas y el valor de cada hora. Calcular el salario semanal.

Fórmula:

```text
salario = horasTrabajadas * valorHora
```

---

## Ejercicio 26. Producto con IVA

Crear un programa que lea el valor de un producto y calcule el valor con IVA del 19%.

Fórmulas:

```text
iva = valorProducto * 0.19
total = valorProducto + iva
```

---

## Ejercicio 27. Total de servicios públicos

Crear un programa que lea el valor de la factura de energía, agua e internet. Calcular el total a pagar.

---

## Ejercicio 28. Gasto semanal en transporte

Crear un programa que lea:

- Valor de un pasaje.
- Cantidad de pasajes diarios.
- Cantidad de días que asiste a la universidad.

Calcular el gasto semanal en transporte.

Fórmula:

```text
gastoSemanal = valorPasaje * pasajesDiarios * dias
```

---

## Ejercicio 29. Costo de impresión

Crear un programa que lea:

- Cantidad de páginas.
- Valor por página.
- Valor de la portada.

Calcular el costo total de impresión.

Fórmula:

```text
total = cantidadPaginas * valorPagina + valorPortada
```

---

## Ejercicio 30. Total de gastos de tres días

Crear un programa que lea los gastos de tres días. Calcular:

- Total gastado.
- Promedio diario.

---

# Reto integrador en Java

## Reto. Calculadora académica básica

Crear un programa en Java que lea:

- Nombre del estudiante.
- Nombre de la asignatura.
- Nota del primer corte.
- Nota del segundo corte.
- Nota del tercer corte.

Debe calcular la nota definitiva usando:

```text
Primer corte = 30%
Segundo corte = 30%
Tercer corte = 40%
```

Debe mostrar un mensaje como:

```text
El estudiante Ana obtuvo una definitiva de 4.1 en Algoritmia.
```

---

## Requisitos técnicos del reto

El programa debe:

- Usar `Scanner`.
- Usar variables con nombres claros.
- Usar `String` para textos.
- Usar `double` para las notas.
- Aplicar correctamente la fórmula.
- Mostrar una salida clara.
- Cerrar el objeto `Scanner`.

---

## Criterios de revisión

| Criterio | Descripción |
|---|---|
| Análisis | Identifica correctamente entrada, proceso y salida |
| Código Java | Compila y ejecuta correctamente |
| Variables | Usa nombres claros y tipos adecuados |
| Fórmulas | Aplica correctamente las operaciones |
| Salida | Muestra mensajes comprensibles |
| Orden | El código está indentado |
| Explicación | El estudiante puede explicar su solución |

---

## Checklist antes de entregar

Antes de entregar un ejercicio en Java, verificar:

- [ ] El archivo tiene el mismo nombre que la clase pública.
- [ ] El programa tiene el método `main`.
- [ ] Se importó `Scanner` si se leen datos.
- [ ] Las variables tienen nombres claros.
- [ ] Los tipos de datos son adecuados.
- [ ] El programa compila.
- [ ] El programa ejecuta.
- [ ] Se probó con diferentes valores.
- [ ] La salida es clara.
- [ ] Puedo explicar el código con mis palabras.

---

## Recomendación final

No se debe copiar el código sin entenderlo.

La pregunta principal antes de entregar es:

```text
¿Puedo explicar qué hace cada parte de mi programa?
```

Si la respuesta es no, todavía se debe seguir practicando.
