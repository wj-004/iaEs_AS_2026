# 📚 Clase de Git - Introducción práctica para estudiantes

Basado en buenas prácticas de control de versiones (Git + flujo de trabajo en equipos de desarrollo).

---

# 📌 1. ¿Qué es Git?

Git es un sistema de control de versiones distribuido.

## ✔ ¿Para qué sirve?
- Guardar historial de cambios
- Trabajar en equipo sin pisarse código
- Volver a versiones anteriores
- Experimentar sin romper el proyecto

---

# 📌 2. Conceptos básicos

## 🧠 Repositorio (repo)
Es el proyecto con todo su historial.

## 📁 Working Directory
Archivos que estás editando.

## 📦 Staging Area
Zona intermedia donde preparas cambios antes de guardarlos.

## 💾 Commit
Es una foto del proyecto en un momento específico.

---

# 📌 3. Flujo básico de Git

```
Working Directory
        ↓
   git add
        ↓
Staging Area
        ↓
   git commit
        ↓
Repositorio (historial)
```

---

# 📌 4. Comandos esenciales

## Inicializar repositorio
```bash
git init
```

## Ver estado
```bash
git status
```

## Agregar cambios
```bash
git add archivo.txt
git add .
```

## Crear commit
```bash
git commit -m "Mensaje descriptivo"
```

## Ver historial
```bash
git log
```

---

# 📌 5. Flujo de trabajo real

```
Editar archivos
     ↓
git status
     ↓
git add .
     ↓
git commit -m "cambio realizado"
     ↓
git push (si hay remoto)
```

---

# 📌 6. Ejercicio 1 - Primer repositorio

## 🎯 Objetivo
Crear un repositorio y hacer tu primer commit.

### 🧪 Pasos:
1. Crear carpeta
2. Inicializar Git
```bash
git init
```
3. Crear archivo index.txt
4. Escribir:
```
Hola Git
```
5. Ver estado:
```bash
git status
```
6. Agregar archivo:
```bash
git add index.txt
```
7. Commit:
```bash
git commit -m "primer commit"
```

---

# 📌 7. Ejercicio 2 - Modificación y seguimiento

## 🎯 Objetivo
Ver cómo Git detecta cambios.

### 🧪 Pasos:
1. Modificar index.txt:
```
Hola Git
Estoy aprendiendo control de versiones
```

2. Ver cambios:
```bash
git status
```

3. Agregar y commitear:
```bash
git add .
git commit -m "agrego segunda línea"
```

---

# 📌 8. Ejercicio 3 - Historial

## 🎯 Objetivo
Ver la evolución del proyecto.

### 🧪 Comando:
```bash
git log
```

---

# 📌 9. Ramas (Branches)

```
main
  |
  |---- feature/login
  |---- feature/dashboard
```

## 📌 Crear rama
```bash
git branch nueva-rama
```

## 📌 Cambiar de rama
```bash
git checkout nueva-rama
```

## 📌 Crear + cambiar
```bash
git checkout -b nueva-rama
```

---

# 📌 10. Ejercicio 4 - Ramas

1. Crear rama:
```bash
git checkout -b feature/saludo
```

2. Modificar archivo:
```
Hola Git
Versión en rama feature/saludo
```

3. Commit:
```bash
git add .
git commit -m "agrego saludo en nueva rama"
```

4. Volver a main:
```bash
git checkout main
```

---

# 📌 11. Merge

```
feature/saludo → main
```

```bash
git checkout main
git merge feature/saludo
```

---

# 📌 12. Ejercicio 5 - Merge

```bash
git merge feature/saludo
```

---

# 📌 13. Conflictos

main: Hola Git
feature: Hola Git versión nueva

Git no sabe cuál versión elegir → hay que resolver manualmente.

---

# 📌 14. Repositorios remotos

## Conectar remoto
```bash
git remote add origin https://github.com/usuario/repo.git
```

## Ver remotos
```bash
git remote -v
```

## Push
```bash
git push origin main
```

## Pull
```bash
git pull origin main
```

## Clone
```bash
git clone https://github.com/usuario/repo.git
```

---

# 📌 15. Ramas remotas

## Subir rama
```bash
git push -u origin feature/saludo
```

## Ver ramas remotas
```bash
git branch -r
```

## Fetch
```bash
git fetch
```

## Crear local desde remota
```bash
git checkout -b feature/saludo origin/feature/saludo
```

---

# 📌 16. Tracking branches

## Ver tracking
```bash
git branch -vv
```

## Set upstream
```bash
git branch --set-upstream-to=origin/main
```

---

# 📌 17. Pull Request (PR)

Un Pull Request es una solicitud para fusionar cambios en un repositorio remoto.

## Flujo:
1. Crear rama
2. Hacer commits
3. Push
4. Crear PR
5. Revisar
6. Merge

## Ejemplo:
```bash
git checkout -b feature/login
git add .
git commit -m "agrego login"
git push -u origin feature/login
```

Luego en GitHub:
feature/login → main

---

# 📌 18. Buenas prácticas

- Commits pequeños
- Mensajes claros
- Usar ramas
- No trabajar en main
- Hacer pull antes de push
- Usar PR para revisión

---

# 📌 19. Ejercicio final

- init repo
- 3 commits
- rama feature/info
- push remoto
- PR
- merge

---

# 🎓 Fin de la clase
