# REPORT.md

## 📌 Descripción general

Este proyecto implementa un pipeline de integración continua (CI) para una API de gestión de tareas desarrollada en Node.js, utilizando objetos de tareas (tasks) simulados en memoria. El pipeline fue creado usando **Jenkins** y tiene como objetivo la ejecución de despliegues simulados.

---

## ⚙️ Pasos realizados

### 1. Configuración del repositorio

- Se inicializó un repositorio Git local.
- Se creó un repositorio remoto en GitHub y se configuró como origen del repo local.

### 2. Configuración básica de la API

- Se creo un archivo server.js para levantar una API REST fake con los datos de tareas en memoria.
- Se verificó que los endpoints estuvieran funcionales en `http://localhost:3000`.

### 3. Pipeline en Jenkins

- Se instaló Jenkins en un entorno local.
- Se creó un `Jenkinsfile` con las siguientes etapas:
  - Clonar el repositorio (`git`).
  - Instalar dependencias (`npm install`).
  - Ejecución de Test (`npm run test`).
  - Creación de la imagen docker (`docker build -t desafio-tasks .`).

---

## ❗ Cambios realizados

- Se agregó el archivo `Jenkinsfile` en la raíz del proyecto.

---

## 🧪 Resultados de pruebas

- ✅ Imagen creada correctamente en Pipeline de Jenkins.

---

## 🚧 Problemas encontrados

- **Error en ejecución de test en Pipeline**: Se resolvió agregando `--forceExit` al final del comando `jest` en el script de test en el package.json.

---

## 🔍Evidencias

![desafio-tasks_2_Console_[Jenkins].pdf](desafio-tasks_2_Console_[Jenkins].pdf)
