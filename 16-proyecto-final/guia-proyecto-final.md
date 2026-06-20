# Guía del Proyecto Final

## Curso: Algoritmia y Programación

## Presentación

El proyecto final tiene como propósito integrar los temas trabajados durante el curso mediante el desarrollo de una aplicación básica en Java.

Este proyecto **no se enfocará en Programación Orientada a Objetos (POO)**, ya que este tema se trabajará solamente de forma introductoria. La profundización de POO corresponde al segundo semestre.

Por esta razón, el proyecto final debe centrarse en la aplicación de la programación estructurada y en los fundamentos de algoritmia trabajados durante el semestre.

---

## 1. Objetivo general

Desarrollar una aplicación en Java que solucione un problema sencillo, aplicando variables, condicionales, ciclos, métodos, arreglos o `ArrayList`, validaciones, búsqueda o procesamiento de datos y documentación en GitHub.

---

## 2. Objetivos específicos

El proyecto debe permitir que el estudiante demuestre que puede:

- Analizar un problema e identificar entradas, procesos y salidas.
- Diseñar una solución mediante programación estructurada.
- Usar variables y tipos de datos adecuados.
- Aplicar condicionales para tomar decisiones.
- Aplicar ciclos para repetir procesos.
- Crear métodos para organizar el código.
- Usar arreglos o `ArrayList` para manejar varios datos.
- Realizar búsquedas, conteos, acumulaciones o cálculos.
- Validar datos ingresados por el usuario.
- Documentar y subir el proyecto a GitHub.
- Explicar el funcionamiento del programa.

---

## 3. Temas que debe integrar el proyecto

El proyecto debe incluir, según corresponda:

- Variables.
- Tipos de datos.
- Operadores aritméticos, relacionales y lógicos.
- Entrada y salida de datos con `Scanner`.
- Condicionales `if`, `else if`, `else` o `switch`.
- Ciclos `while`, `do-while` o `for`.
- Métodos.
- Arreglos o `ArrayList`.
- Contadores y acumuladores.
- Búsqueda secuencial.
- Ordenamiento básico, si aplica.
- Validaciones.
- Menú de opciones.
- Git y GitHub.
- Documentación en Markdown.

---

## 4. Tema que no será exigido

Para este proyecto **no será obligatorio aplicar Programación Orientada a Objetos**.

No se evaluará el uso de:

- Clases propias adicionales.
- Objetos.
- Atributos.
- Constructores.
- Encapsulamiento.
- Getters y setters.
- Herencia.
- Polimorfismo.

El estudiante puede desarrollar el proyecto usando una clase principal y métodos estáticos.

Ejemplo:

```java
public class Principal {
    public static void main(String[] args) {
        // Menú principal
    }

    public static void registrarDato() {
        // Código del método
    }

    public static void mostrarDatos() {
        // Código del método
    }
}
```

---

## 5. Requisitos mínimos del proyecto

El proyecto debe cumplir con los siguientes requisitos:

1. Estar desarrollado en Java.
2. Tener un menú de opciones.
3. Usar `Scanner` para entrada de datos.
4. Usar condicionales.
5. Usar ciclos.
6. Usar métodos.
7. Usar arreglos o `ArrayList`.
8. Validar datos importantes.
9. Realizar al menos una búsqueda o recorrido de información.
10. Realizar cálculos, conteos, acumulaciones o resúmenes.
11. Mostrar resultados claros al usuario.
12. Estar organizado en carpetas.
13. Tener un archivo `README.md`.
14. Estar subido a GitHub.
15. Poder ser explicado por el estudiante.

---

## 6. Estructura sugerida del proyecto

```text
proyecto-final/
│
├── README.md
├── src/
│   └── Principal.java
│
├── docs/
│   ├── analisis.md
│   ├── pruebas.md
│   └── evidencias.md
│
└── recursos/
    └── imagenes/
```

Si el estudiante desea organizar el código en más archivos `.java`, puede hacerlo. Sin embargo, no será obligatorio aplicar POO.

---

## 7. Etapas del proyecto

### Etapa 1. Selección del problema

El estudiante debe seleccionar un problema sencillo y claro.

Ejemplos:

- Sistema de notas.
- Sistema de inventario básico.
- Agenda de tareas.
- Control de gastos.
- Registro de ventas.
- Control de asistencia.
- Calculadora académica.
- Registro básico de biblioteca.

---

### Etapa 2. Análisis del problema

Antes de programar, el estudiante debe identificar:

| Elemento | Pregunta guía |
|---|---|
| Problema | ¿Qué situación se quiere resolver? |
| Usuario | ¿Quién usará el programa? |
| Entradas | ¿Qué datos se van a ingresar? |
| Procesos | ¿Qué cálculos, decisiones o búsquedas se harán? |
| Salidas | ¿Qué resultados se mostrarán? |

---

### Etapa 3. Diseño de la solución

El estudiante debe planear:

- Nombre del proyecto.
- Opciones del menú.
- Variables principales.
- Arreglos o listas necesarias.
- Métodos que se van a crear.
- Validaciones.
- Búsquedas.
- Cálculos.
- Resultados esperados.

---

## 8. Ejemplo de diseño básico

Para un sistema de notas, se podría usar:

```java
ArrayList<String> nombres = new ArrayList<>();
ArrayList<Double> notas = new ArrayList<>();
```

Métodos sugeridos:

```java
registrarEstudiante()
mostrarEstudiantes()
buscarEstudiante()
calcularPromedio()
contarAprobados()
validarNota()
```

Menú sugerido:

```text
===== SISTEMA DE NOTAS =====
1. Registrar estudiante
2. Mostrar estudiantes
3. Buscar estudiante
4. Calcular promedio del grupo
5. Mostrar aprobados y reprobados
6. Salir
```

---

## 9. Recomendaciones para el código

- Usar nombres claros para variables y métodos.
- No escribir todo el programa dentro del `main`.
- Crear métodos para organizar cada opción del menú.
- Validar datos numéricos.
- Evitar repetir código.
- Usar comentarios cuando sea necesario.
- Probar cada opción del menú.
- Guardar avances en GitHub mediante commits.

---

## 10. Validaciones esperadas

El programa debe validar datos importantes.

Ejemplos:

- Una nota debe estar entre 0.0 y 5.0.
- Una edad no debe ser negativa.
- Un precio debe ser mayor que cero.
- Una opción de menú debe estar dentro del rango permitido.
- Una lista no debe estar vacía antes de buscar o eliminar.
- Una posición debe existir antes de eliminar un dato.

---

## 11. Pruebas del proyecto

El estudiante debe probar su programa con diferentes casos.

Ejemplo para sistema de notas:

| Caso | Dato probado | Resultado esperado |
|---|---|---|
| Nota válida | 4.2 | Se registra correctamente |
| Nota inválida | 6.0 | El programa muestra error |
| Buscar estudiante existente | Ana | Muestra información |
| Buscar estudiante inexistente | Pedro | Indica que no existe |
| Lista vacía | Mostrar estudiantes | Informa que no hay registros |

---

## 12. Documentación requerida

El repositorio debe incluir:

### README.md

Debe contener:

- Nombre del proyecto.
- Descripción.
- Funcionalidades.
- Temas aplicados.
- Tecnologías utilizadas.
- Cómo ejecutar el programa.
- Autor o integrantes.

### docs/analisis.md

Debe contener:

- Problema.
- Entradas.
- Procesos.
- Salidas.
- Estructuras de datos utilizadas.
- Métodos principales.
- Validaciones.

### docs/pruebas.md

Debe contener casos de prueba.

### docs/evidencias.md

Debe incluir capturas o descripción de la ejecución.

---

## 13. Entrega en GitHub

El estudiante debe subir el proyecto a GitHub.

Comandos básicos:

```bash
git init
git status
git add .
git commit -m "Primer commit del proyecto final"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

Para actualizaciones:

```bash
git status
git add .
git commit -m "Agrega funcionalidad de registro"
git push
```

---

## 14. Sustentación del proyecto

Durante la sustentación, el estudiante debe poder explicar:

- Qué problema resuelve el proyecto.
- Qué datos se ingresan.
- Qué procesos realiza.
- Qué resultados muestra.
- Qué métodos creó.
- Qué arreglos o `ArrayList` usó.
- Cómo funcionan las validaciones.
- Cómo se realiza la búsqueda o el cálculo principal.
- Qué dificultades tuvo.
- Qué aprendió.

---

## 15. Criterios generales de evaluación

El proyecto será evaluado teniendo en cuenta:

- Análisis del problema.
- Diseño de la solución.
- Sintaxis y funcionamiento en Java.
- Uso de condicionales y ciclos.
- Uso de arreglos o `ArrayList`.
- Uso de métodos.
- Búsqueda, cálculos y procesamiento de datos.
- Validaciones.
- Documentación y GitHub.
- Sustentación.

---

## 16. Recomendación sobre uso de IA

La inteligencia artificial puede usarse como apoyo para:

- Resolver dudas.
- Revisar errores.
- Pedir explicaciones.
- Mejorar el README.
- Preparar la sustentación.
- Generar casos de prueba.

Pero el estudiante no debe entregar código que no comprenda.

Regla principal:

```text
Si no puedes explicar el código, todavía no es tu solución.
```

---

## 17. Recomendación final

El proyecto final no busca una aplicación avanzada. Busca demostrar que el estudiante comprende la lógica de programación y puede construir una solución funcional, organizada, documentada y explicable en Java.
