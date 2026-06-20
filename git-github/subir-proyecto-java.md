# Subir un Proyecto Java a GitHub

## Presentación

Este archivo explica cómo subir un proyecto Java a GitHub usando Git.

La guía sirve para proyectos creados en:

- NetBeans.
- Eclipse.
- Visual Studio Code.
- Carpeta Java creada manualmente.

---

## 1. Requisitos previos

Antes de iniciar, se debe tener:

- Git instalado.
- Cuenta en GitHub.
- Proyecto Java creado.
- Carpeta del proyecto organizada.
- Archivo `README.md` recomendado.

---

## 2. Estructura recomendada del proyecto

Ejemplo:

```text
mi-proyecto-java/
│
├── README.md
├── src/
│   └── Main.java
└── .gitignore
```

Si el proyecto fue creado en NetBeans o Eclipse, puede tener otras carpetas. Lo importante es reconocer cuál es la carpeta principal del proyecto.

---

## 3. Crear archivo README.md

Crear un archivo llamado:

```text
README.md
```

Ejemplo de contenido:

```markdown
# Mi Proyecto Java

## Descripción

Este proyecto contiene ejercicios básicos de Java desarrollados en el curso de Algoritmia y Programación.

## Temas trabajados

- Variables.
- Condicionales.
- Ciclos.
- Arreglos.
- Métodos.

## Autor

Nombre del estudiante.
```

---

## 4. Crear archivo .gitignore

El archivo `.gitignore` indica qué archivos no se deben subir.

Ejemplo básico para Java:

```gitignore
*.class
*.jar
*.war
*.ear

build/
dist/
target/
out/
bin/

*.log
```

Esto evita subir archivos compilados o temporales.

---

## 5. Abrir terminal en la carpeta del proyecto

Desde la carpeta del proyecto, abrir una terminal.

En Windows puede ser:

- Git Bash.
- Terminal de VS Code.
- CMD.
- PowerShell.

---

## 6. Inicializar Git

```bash
git init
```

Esto crea el repositorio local.

---

## 7. Revisar estado

```bash
git status
```

Git mostrará los archivos nuevos o modificados.

---

## 8. Agregar archivos

```bash
git add .
```

Esto prepara todos los archivos para el commit.

---

## 9. Crear primer commit

```bash
git commit -m "Primer commit del proyecto Java"
```

---

## 10. Crear repositorio en GitHub

Pasos generales:

1. Ingresar a GitHub.
2. Seleccionar `New repository`.
3. Escribir el nombre del repositorio.
4. Agregar descripción si se desea.
5. Elegir si será público o privado.
6. No marcar opciones si ya tienes archivos locales.
7. Crear repositorio.

---

## 11. Conectar repositorio local con GitHub

GitHub mostrará una URL del repositorio.

Ejemplo:

```text
https://github.com/usuario/mi-proyecto-java.git
```

Conectar:

```bash
git remote add origin https://github.com/usuario/mi-proyecto-java.git
```

---

## 12. Cambiar nombre de rama a main

```bash
git branch -M main
```

---

## 13. Subir proyecto

```bash
git push -u origin main
```

---

## 14. Flujo para futuras actualizaciones

Después de modificar archivos:

```bash
git status
git add .
git commit -m "Describe los cambios realizados"
git push
```

Ejemplo:

```bash
git commit -m "Agrega ejercicios de ciclos"
```

---

## 15. Recomendaciones para NetBeans

En NetBeans, ubicar la carpeta principal del proyecto.

No es necesario subir archivos compilados. Se recomienda revisar `.gitignore`.

Archivos o carpetas que normalmente no son esenciales:

```text
build/
dist/
```

---

## 16. Recomendaciones para Eclipse

En Eclipse, el proyecto puede tener carpetas como:

```text
src/
bin/
.project
.classpath
```

Generalmente se debe evitar subir archivos compilados en `bin/`.

---

## 17. Recomendaciones para VS Code

En VS Code se puede abrir la carpeta del proyecto y usar la terminal integrada.

Comando para abrir terminal:

```text
Terminal → New Terminal
```

Luego usar los comandos de Git.

---

## 18. Problemas frecuentes

### Error: remote origin already exists

Significa que ya existe un remoto llamado `origin`.

Solución posible:

```bash
git remote -v
```

Si se necesita cambiar la URL:

```bash
git remote set-url origin URL_NUEVA
```

---

### Error: src refspec main does not match any

Puede ocurrir si no se ha creado ningún commit.

Solución:

```bash
git add .
git commit -m "Primer commit"
git branch -M main
git push -u origin main
```

---

### Error de autenticación

GitHub puede pedir iniciar sesión o usar token según la configuración del equipo.

Se recomienda seguir las instrucciones que muestre GitHub o configurar Git Credential Manager.

---

## 19. Checklist antes de entregar

- [ ] El proyecto compila.
- [ ] El programa ejecuta.
- [ ] El README.md explica el proyecto.
- [ ] No se subieron archivos innecesarios.
- [ ] Hay al menos un commit.
- [ ] El repositorio está en GitHub.
- [ ] El enlace abre correctamente.
- [ ] El estudiante puede explicar el código.

---

## Recomendación final

Subir un proyecto a GitHub no es solo una entrega. También es una forma de construir portafolio académico y profesional.
