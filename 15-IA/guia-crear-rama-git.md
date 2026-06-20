# Guía: Crear una Rama de Git para Inteligencia Artificial

## Presentación

Si se desea trabajar el tema de inteligencia artificial en una rama especial del repositorio, se puede crear una rama llamada:

```text
ia-educativa
```

Esta rama puede contener los archivos de la carpeta:

```text
14-inteligencia-artificial/
```

---

## 1. Verificar el estado actual

Antes de crear una rama, revisar:

```bash
git status
```

Si hay cambios pendientes, se recomienda guardarlos con commit.

---

## 2. Crear y cambiar a la rama

```bash
git checkout -b ia-educativa
```

O usando el comando moderno:

```bash
git switch -c ia-educativa
```

---

## 3. Agregar la carpeta de IA

Crear la carpeta:

```text
14-inteligencia-artificial/
```

Agregar dentro los archivos de esta rama especial.

---

## 4. Agregar cambios

```bash
git add .
```

---

## 5. Crear commit

```bash
git commit -m "Agrega rama de inteligencia artificial educativa"
```

---

## 6. Subir la rama a GitHub

```bash
git push -u origin ia-educativa
```

---

## 7. Volver a la rama principal

```bash
git checkout main
```

O:

```bash
git switch main
```

---

## 8. Unir la rama a main

Cuando se quiera integrar el contenido a la rama principal:

```bash
git checkout main
git merge ia-educativa
git push
```

---

## 9. Ver ramas

```bash
git branch
```

Para ver ramas remotas:

```bash
git branch -a
```

---

## 10. Recomendación

Usar una rama especial permite trabajar el contenido de IA sin afectar directamente el contenido principal del curso hasta que esté revisado.
