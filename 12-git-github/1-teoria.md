# Unidad 11. Git y GitHub

## Presentación de la unidad

En programación no basta con escribir código. También es importante organizarlo, guardar versiones y compartirlo.

Para eso se utilizan herramientas como:

- **Git**
- **GitHub**

Estas herramientas son fundamentales para el trabajo académico y profesional en desarrollo de software.

---

## 1. ¿Qué es Git?

Git es un sistema de control de versiones.

Permite guardar el historial de cambios de un proyecto.

En palabras sencillas, Git ayuda a responder preguntas como:

- ¿Qué cambios hice?
- ¿Cuándo los hice?
- ¿Qué archivos modifiqué?
- ¿Puedo volver a una versión anterior?
- ¿Quién hizo un cambio en un proyecto?

---

## 2. ¿Qué es control de versiones?

El control de versiones permite administrar diferentes estados de un proyecto.

Ejemplo:

```text
Version 1: Primer programa
Version 2: Agregué Scanner
Version 3: Agregué condicionales
Version 4: Corregí errores
```

Sin Git, muchas personas guardan archivos así:

```text
ProyectoFinal.java
ProyectoFinalNuevo.java
ProyectoFinalAhoraSi.java
ProyectoFinalDefinitivo.java
ProyectoFinalDefinitivoFinal.java
```

Con Git, esto se organiza mediante commits.

---

## 3. ¿Qué es un commit?

Un commit es un registro de cambios.

Es como una fotografía del proyecto en un momento determinado.

Cada commit debe tener un mensaje claro.

Ejemplo:

```bash
git commit -m "Agrega ejercicio de promedio de notas"
```

---

## 4. ¿Qué es GitHub?

GitHub es una plataforma en línea donde se pueden alojar repositorios Git.

Permite:

- Guardar proyectos en la nube.
- Compartir código.
- Trabajar en equipo.
- Publicar portafolios.
- Revisar historial de cambios.
- Documentar proyectos con archivos Markdown.

---

## 5. Diferencia entre Git y GitHub

| Git | GitHub |
|---|---|
| Herramienta de control de versiones | Plataforma web para alojar repositorios |
| Funciona en el computador | Funciona en internet |
| Permite crear commits | Permite subir y compartir commits |
| Se usa desde terminal o herramientas gráficas | Se usa desde navegador o Git |

---

## 6. ¿Qué es un repositorio?

Un repositorio es una carpeta controlada por Git.

Puede contener:

- Código fuente.
- Archivos Markdown.
- Imágenes.
- Documentación.
- Ejercicios.
- Proyectos.

Ejemplo:

```text
algoritmia-ingenieria-sistemas/
```

---

## 7. ¿Qué es Markdown?

Markdown es un lenguaje sencillo para escribir documentación.

Los archivos Markdown tienen extensión:

```text
.md
```

Ejemplo:

```text
README.md
```

GitHub muestra los archivos `.md` como documentos bien formateados.

---

## 8. ¿Qué es README.md?

El archivo `README.md` es la presentación principal de un repositorio.

Debe explicar:

- Nombre del proyecto.
- Descripción.
- Objetivos.
- Estructura.
- Instrucciones de uso.
- Autor.
- Licencia si aplica.

---

## 9. Flujo básico de trabajo con Git

El flujo básico es:

```text
Modificar archivos
      ↓
git status
      ↓
git add .
      ↓
git commit -m "mensaje"
      ↓
git push
```

---

## 10. Estados de los archivos

| Estado | Significado |
|---|---|
| Modificado | El archivo cambió |
| Preparado | El archivo fue agregado con `git add` |
| Confirmado | El cambio quedó guardado en un commit |
| Subido | El commit fue enviado a GitHub |

---

## 11. Buenas prácticas

- Hacer commits frecuentes.
- Escribir mensajes claros.
- No subir archivos innecesarios.
- Mantener una estructura ordenada.
- Documentar con README.
- Revisar `git status` antes de confirmar.
- No entregar proyectos sin probar.
- Usar nombres de carpetas y archivos claros.

---

## 12. GitHub como portafolio

Un repositorio bien organizado puede convertirse en evidencia del aprendizaje del estudiante.

Permite mostrar:

- Ejercicios realizados.
- Buenas prácticas.
- Avance progresivo.
- Capacidad de documentación.
- Proyectos finales.

---

## Resultado de aprendizaje

Al finalizar esta unidad, el estudiante debe poder crear un repositorio, organizar un proyecto Java, realizar commits, subir el proyecto a GitHub y documentarlo usando Markdown.
