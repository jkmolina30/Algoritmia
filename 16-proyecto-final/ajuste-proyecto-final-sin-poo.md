# Ajuste para el Proyecto Final: Sin POO

## Aclaración para estudiantes

En el proyecto final **no se exigirá Programación Orientada a Objetos (POO)**.

Aunque durante el curso se hará una introducción mínima a clases y objetos, este tema se estudiará con mayor profundidad en el segundo semestre. Por tanto, el proyecto final debe centrarse en los fundamentos de programación trabajados durante el semestre.

---

## Temas que sí debe aplicar el proyecto

El proyecto debe integrar:

- Variables y tipos de datos.
- Operadores.
- Entrada y salida de datos con `Scanner`.
- Condicionales.
- Ciclos.
- Métodos.
- Arreglos o `ArrayList`.
- Búsqueda o recorrido de información.
- Cálculos, acumuladores y contadores.
- Validación de datos.
- Menú de opciones.
- Git y GitHub.
- Documentación en Markdown.

---

## Temas que no serán obligatorios

No será obligatorio usar:

- Clases propias adicionales.
- Objetos.
- Atributos.
- Constructores.
- Encapsulamiento.
- Getters y setters.
- Herencia.
- Polimorfismo.

---

## Estructura sugerida

El proyecto puede desarrollarse con una clase principal:

```text
proyecto-final/
│
├── README.md
├── src/
│   └── Principal.java
├── docs/
│   ├── analisis.md
│   ├── pruebas.md
│   └── evidencias.md
└── recursos/
    └── imagenes/
```

---

## Ejemplo de enfoque correcto

Un sistema de notas puede usar:

```java
ArrayList<String> nombres;
ArrayList<Double> notas;
```

Y métodos como:

```java
registrarEstudiante()
mostrarEstudiantes()
buscarEstudiante()
calcularPromedio()
contarAprobados()
validarNota()
```

Este enfoque es suficiente para el proyecto final, sin necesidad de crear clases como `Estudiante`, `Curso` o `RegistroNota`.

---

## Recomendación final

El objetivo del proyecto final es demostrar que el estudiante comprende la lógica de programación, sabe organizar un programa en Java, usa estructuras de control, trabaja con listas o arreglos, valida datos y puede explicar su solución.
