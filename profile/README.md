# 🛒 DSMarket - Your Next Generation Store

## 📌 Descripción General

**DSMarket** es un proyecto de *end-to-end Machine Learning* desarrollado como parte del proyecto final del Máster en Data Science. La misión: transformar una cadena de supermercados tradicional mediante el uso de ciencia de datos, inteligencia artificial y tecnologías en la nube. Este repositorio contiene tanto el análisis exploratorio y modelado predictivo, como la infraestructura MLOps necesaria para llevar los modelos a producción.

---

## 🧠 Contexto del Proyecto

DSMarket (anteriormente TradiStores) es una cadena de supermercados en EE.UU. que ha comenzado una transformación digital profunda. El objetivo es:

- Mejorar la predicción de ventas.
- Optimizar la reposición de stock.
- Apoyar decisiones estratégicas de negocio.

Se trabaja con tres ciudades: **Nueva York, Boston y Filadelfia**.

---

## 🧾 Tareas Principales

### ✅ Tarea 1: Análisis Exploratorio
- Análisis de tendencias de ventas por ciudad/tienda/producto.
- Identificación de productos populares y en declive.
- Diseño de dashboard BI para stakeholders.

### ✅ Tarea 2: Clustering
- Agrupación de productos por comportamiento de ventas.
- Agrupación de tiendas por similitud en patrones de consumo.

### ✅ Tarea 3: Predicción de Ventas
- Desarrollo de modelos predictivos para horizonte de 28 días.
- Evaluación con datos de prueba proporcionados por la empresa.

### ✅ Tarea 4: Caso de Uso - Abastecimiento de Tiendas
- Aplicación del modelo predictivo para mejorar la reposición de stock.
- Productivización del modelo a través de una API.
- Diseño de una prueba piloto controlada para medir impacto financiero.

---

## 🏗️ Arquitectura MLOps

### 🌐 Backend: API con FastAPI
- `/predict`: endpoint para predicción de ventas en tiempo real.
- `/ventas`: recuperación de datos históricos desde AlloyDB.
- Desplegado con **Uvicorn** en contenedor Docker.

### 🐳 Contenerización: Docker
- Imagen ligera reproducible.
- Publicación en **Google Artifact Registry**.

### ☁️ Despliegue: Google Cloud Run
- Escalabilidad automática según la demanda.
- Bajo mantenimiento y coste optimizado.

### 🗄️ Base de Datos: AlloyDB for PostgreSQL
- Carga inicial de datos históricos desde archivo `.pkl`.
- Consultas de baja latencia para uso en producción.

### 🚀 Automatización CI/CD: Google Cloud Build + GitHub Actions
- Construcción y despliegue automático al hacer `push` en GitHub.
- Imagen Docker y despliegue en Cloud Run sin intervención manual.

### 🖥️ Frontend: GitHub Pages
- Interfaz simple para seleccionar fechas y consultar predicciones.

---

## 🔐 Seguridad y Escalabilidad

- Autenticación vía **IAM** y acceso restringido por IP.
- Logs centralizados en **Google Cloud Logging**.
- Escalado automático de API y base de datos para alta disponibilidad.

---

## 📊 Tecnologías Utilizadas

| Tecnología            | Uso Principal                                 |
|----------------------|-----------------------------------------------|
| FastAPI              | Backend para predicción                       |
| Docker               | Contenerización de la API                     |
| Google Cloud Run     | Despliegue sin servidor                       |
| AlloyDB              | Base de datos escalable y de alto rendimiento|
| Google Cloud Build   | CI/CD Automatizado                            |
| GitHub Pages         | Frontend ligero para demostraciones           |

---

## 👥 Equipo

Este proyecto fue desarrollado por el equipo del Máster en Data Science durante el Capstone Project. Cada miembro participó en el análisis, modelado y despliegue.
- Adrián Ortega Fernández
- Ariana Puentes Lafée
- Cristina Sánchez García
- Juan José Guerrero López

Tutor:
Daniel Pegalajar Luque




---

## 📂 Estructura del Repositorio
DSMarket/
├── notebooks/              # Análisis exploratorio y clustering
├── model/                  # Entrenamiento y guardado del modelo
├── api/                    # Código de la API FastAPI
├── docker/                 # Dockerfile y configuración
├── cloudbuild.yaml         # Configuración de CI/CD
├── frontend/               # index.html y recursos para GitHub Pages
├── data/                   # Datos de entrada (.csv, .pkl, etc.)
└── README.md               # Documentación del proyecto

---

## 📬 Contacto

Para cualquier duda o comentario, por favor contacta con el equipo docente del máster o abre un *issue* en este repositorio.

---

🚀 *DSMarket: Impulsando el retail con inteligencia de datos.*

