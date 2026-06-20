# Entrega del Proyecto Final en GitHub

## Presentación

El proyecto final debe entregarse mediante un repositorio de GitHub.

GitHub permite revisar:

- Código fuente.
- Organización del proyecto.
- README.
- Evidencias.
- Historial de commits.
- Documentación.

---

## 1. Nombre sugerido del repositorio

Usar un nombre claro.

Ejemplos:

```text
proyecto-final-algoritmia
sistema-notas-java
inventario-java
biblioteca-java
agenda-tareas-java
```

Evitar nombres como:

```text
trabajo
final
proyecto1
cosas
```

---

## 2. Estructura recomendada

```text
proyecto-final/
│
├── README.md
├── src/
│   ├── Principal.java
│   ├── Clase1.java
│   └── Clase2.java
│
├── docs/
│   ├── analisis.md
│   ├── pruebas.md
│   └── evidencias.md
│
└── recursos/
    └── imagenes/
```

---

## 3. README obligatorio

El archivo `README.md` debe incluir:

```markdown
# Nombre del proyecto

## Descripción

Explicación breve del problema que resuelve.

## Funcionalidades

- Funcionalidad 1
- Funcionalidad 2
- Funcionalidad 3

## Tecnologías utilizadas

- Java
- Git
- GitHub

## Estructura del proyecto

Explicar las carpetas principales.

## Cómo ejecutar

Instrucciones para abrir y ejecutar el proyecto.

## Autor

Nombre del estudiante o integrantes.
```

---

## 4. Archivo de análisis

Crear en `docs/analisis.md`:

```markdown
# Análisis del proyecto

## Problema

## Entradas

## Procesos

## Salidas

## Clases identificadas

## Métodos principales
```

---

## 5. Archivo de pruebas

Crear en `docs/pruebas.md`:

```markdown
# Pruebas del proyecto

| Caso | Datos de entrada | Resultado esperado | Resultado obtenido |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |
```

---

## 6. Evidencias

En `docs/evidencias.md` incluir:

- Capturas de ejecución.
- Explicación de las pruebas.
- Errores encontrados y corregidos.
- Funcionalidades terminadas.

Las imágenes pueden guardarse en:

```text
recursos/imagenes/
```

---

## 7. Comandos básicos para subir

Dentro de la carpeta del proyecto:

```bash
git init
git status
git add .
git commit -m "Primer commit del proyecto final"
git branch -M main
git remote add origin URL_DEL_REPOSITORIO
git push -u origin main
```

---

## 8. Actualizaciones posteriores

Cada vez que se avance:

```bash
git status
git add .
git commit -m "Agrega funcionalidad de registro"
git push
```

Ejemplos de buenos mensajes:

```bash
git commit -m "Agrega clase Estudiante"
git commit -m "Implementa cálculo de promedio"
git commit -m "Agrega validación de notas"
git commit -m "Actualiza README"
```

---

## 9. Checklist antes de entregar

- [ ] El proyecto compila.
- [ ] El proyecto ejecuta.
- [ ] Tiene README.md.
- [ ] Tiene análisis del problema.
- [ ] Tiene pruebas documentadas.
- [ ] Tiene evidencias.
- [ ] Usa clases y objetos.
- [ ] Usa métodos.
- [ ] Usa condicionales y ciclos.
- [ ] Usa arreglos o ArrayList.
- [ ] Tiene commits.
- [ ] El repositorio está en GitHub.
- [ ] El enlace es público o accesible para el docente.
- [ ] El estudiante puede explicar el código.

---

## 10. Formato de entrega

Entregar:

```text
Nombre del estudiante:
Nombre del proyecto:
Enlace de GitHub:
Breve descripción:
```

---

## 11. Recomendación final

No subir el proyecto solo al final.  
Lo ideal es hacer commits durante todo el desarrollo para evidenciar el proceso.
