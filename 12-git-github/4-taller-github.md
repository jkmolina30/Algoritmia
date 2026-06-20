# Taller Práctico: Git y GitHub

## Objetivo del taller

Aplicar los comandos básicos de Git y GitHub mediante la creación y publicación de un proyecto Java.

---

## Competencias a fortalecer

Al finalizar el taller, el estudiante estará en capacidad de:

- Crear un repositorio local.
- Organizar archivos de un proyecto Java.
- Crear commits.
- Subir un proyecto a GitHub.
- Documentar el proyecto con `README.md`.
- Compartir el enlace del repositorio.

---

# Parte 1. Crear proyecto Java

## Actividad 1

Crear un proyecto Java llamado:

```text
taller-github-java
```

El proyecto debe contener al menos tres programas:

```text
Saludo.java
PromedioNotas.java
MayorEdad.java
```

---

## Actividad 2. Programa Saludo

Crear un programa que muestre:

```text
Bienvenido al taller de Git y GitHub
```

---

## Actividad 3. Programa PromedioNotas

Crear un programa que lea tres notas y calcule el promedio.

---

## Actividad 4. Programa MayorEdad

Crear un programa que lea una edad e indique si la persona es mayor de edad.

---

# Parte 2. Crear documentación

## Actividad 5

Crear un archivo:

```text
README.md
```

Debe contener:

```markdown
# Taller Git y GitHub

## Descripción

Este repositorio contiene programas básicos en Java desarrollados para practicar Git y GitHub.

## Programas incluidos

- Saludo.java
- PromedioNotas.java
- MayorEdad.java

## Autor

Nombre del estudiante.
```

---

# Parte 3. Inicializar Git

Abrir terminal dentro de la carpeta del proyecto y ejecutar:

```bash
git init
```

Luego revisar estado:

```bash
git status
```

---

# Parte 4. Primer commit

Agregar archivos:

```bash
git add .
```

Crear commit:

```bash
git commit -m "Agrega proyecto inicial del taller"
```

---

# Parte 5. Crear repositorio en GitHub

1. Ingresar a GitHub.
2. Crear un repositorio nuevo.
3. Nombre sugerido:

```text
taller-github-java
```

4. Crear el repositorio vacío.

---

# Parte 6. Conectar y subir

Conectar el repositorio local con GitHub:

```bash
git remote add origin URL_DEL_REPOSITORIO
```

Cambiar rama a `main`:

```bash
git branch -M main
```

Subir:

```bash
git push -u origin main
```

---

# Parte 7. Realizar una modificación

Modificar el archivo `README.md` agregando una sección:

```markdown
## Temas practicados

- Git init.
- Git status.
- Git add.
- Git commit.
- Git push.
- GitHub.
```

Luego ejecutar:

```bash
git status
git add .
git commit -m "Actualiza README con temas practicados"
git push
```

---

# Parte 8. Evidencia de entrega

El estudiante debe entregar:

1. Enlace del repositorio de GitHub.
2. Captura del historial de commits.
3. Captura del README en GitHub.
4. Captura de ejecución de los programas.
5. Breve explicación de qué hace cada comando utilizado.

---

# Preguntas de reflexión

Responder en el README o en un archivo aparte:

1. ¿Qué es Git?
2. ¿Qué es GitHub?
3. ¿Qué es un commit?
4. ¿Para qué sirve `git status`?
5. ¿Para qué sirve `git add .`?
6. ¿Para qué sirve `git push`?
7. ¿Por qué es importante documentar un proyecto?
8. ¿Cómo puede GitHub ayudar en la formación profesional?

---

# Criterios de evaluación

| Criterio | Descripción |
|---|---|
| Proyecto Java | Contiene los programas solicitados |
| README | Está completo y organizado |
| Git | Usa commits correctamente |
| GitHub | El proyecto está publicado |
| Evidencias | Entrega capturas o enlace funcional |
| Explicación | Comprende los comandos usados |
| Orden | La estructura del proyecto es clara |

---

# Reto opcional

Agregar dos programas más al repositorio:

```text
TablaMultiplicar.java
CalculadoraBasica.java
```

Luego hacer un nuevo commit:

```bash
git add .
git commit -m "Agrega programas adicionales"
git push
```
