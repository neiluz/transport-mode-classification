# transport-mode-classification

![transporte](https://github.com/AndreaTJ/Tech-Girls-Glovo/raw/main/docs/banner-madrid.jpg)

## **Índice**
- [Introducción](#introducción)
- [Descripción del proyecto](#descripción-del-proyecto)
- [Conjuntos de datos](#conjuntos-de-datos)
- [Metodología](#metodología)
- [Estructura del Repositorio](#estructura-del-repositorio)
- [Resultados del Proyecto](#resultados-del-proyecto)
   - [Análisis Exploratorio de Datos (EDA)](#análisis-exploratorio-de-datos-eda)
   - [Entrenamiento de Modelos](#entrenamiento-de-modelos)
   - [Evaluación de Resultados](#evaluación-de-resultados)
   - [Visualizaciones](#visualizaciones)
- [Conclusiones](#conclusiones)
- [Limitaciones](#limitaciones)
- [Instrucciones de Uso](#instrucciones-de-uso)
- [Licencia](#licencia)
- [Integrantes del Grupo](#integrantes-del-grupo)


# Project 8: Predicción del modo de transporte mediante registro de dispositivos móviles usando SVM

## Propuesto por: Esteve Codina

## Introducción
Este proyecto aborda el desarrollo de un modelo de clasificación para predecir el modo de transporte utilizando señales registradas en dispositivos móviles. A través de técnicas avanzadas como Máquinas de Vectores de Soporte (SVM), el modelo se entrena con datos provenientes de múltiples sensores.

## Descripción del proyecto

Este proyecto tiene como objetivo desarrollar un modelo de clasificación basado en Máquinas de Vectores de Soporte (SVM) para predecir el modo de transporte utilizado durante la grabación de datos provenientes de diferentes sensores de un dispositivo móvil. La información registrada incluye señales de sensores como acelerómetro, giroscopio, barómetro, GPS y magnetómetro, capturada en varios contextos de transporte.

El modelo busca inferir el tipo de transporte (e.g., coche, bicicleta, autobús, caminar) a partir de un conjunto de datos estructurado en formato .csv.

---

## Conjuntos de datos

Los datos disponibles contienen registros de los siguientes sensores y variables:

- Instante de tiempo: Marca temporal asociada a cada registro.
- Acelerómetro: Coordenadas del vector aceleración (éjes X, Y, Z).
- Orientación angular: Coordenadas X, Y, Z del vector orientación angular y su vector derivada.
- Rotación: Matriz de rotación y quaternion de rotación.
- Ubicación GPS: Longitud, latitud, velocidad, rumbo y altitud.
- Barómetro: Presión atmosférica y altitud relativa.
- Magnetómetro: Coordenadas X, Y, Z del campo magnético terrestre.
- Modo de transporte: Etiqueta del tipo de transporte utilizado (e.g., coche, bicicleta, caminar) junto con un índice de confianza.

---
## Metodología

### 1. Preparación de los datos:

- Selección de un subconjunto de datos al azar para evitar redundancia y reducir el tamaño del conjunto.
- Preprocesamiento, incluyendo manejo de valores nulos, normalización y creación de nuevas variables derivadas (e.g., magnitud de aceleración, velocidad angular total).

### 2. Desarrollo del modelo:

- Entrenamiento de un modelo de clasificación utilizando SVM con diferentes kernels (lineal, radial, polinómico, sigmoide).
- Fine-tuning de hiperparámetros mediante búsqueda en malla (Grid Search).

### 3. Validación del modelo:
- Evaluación del error de predicción utilizando Cross-validation.
- Cálculo de métricas como precisión, recall, F1-score y curva ROC.

### 4. Visualizaciones:
- Análisis exploratorio de datos (EDA) mediante histogramas, heatmaps y boxplots.
- Visualización de resultados del modelo y tiempos de entrenamiento.

---
## **Estructura del Repositorio**
```plaintext
📂 Nombre_del_Proyecto
├── 📂 data/                 # Datos crudos y procesados
├── 📂 notebooks/            # Notebooks para análisis y desarrollo
├── 📂 scripts/              # Funciones y código modular
├── 📂 results/              # Salidas del proyecto
├── 📂 docs/                 # Documentación
└── requirements.R           # Librerías necesarias
```
---

## **Resultados del Proyecto**
> **Estado:** En progreso.

### **Análisis Exploratorio de Datos (EDA)**
- Distribución de la aceleración total calculada a partir de las componentes X, Y y Z del acelerómetro.
- Relación entre las variables principales como aceleración, velocidad angular y altitud, analizada mediante correlaciones.
- Identificación de valores atípicos en variables clave como aceleración y velocidad angular.

### **Entrenamiento de Modelos**
- Entrenamiento con **SVM** utilizando diferentes kernels: lineal, radial (RBF), polinómico y sigmoide.
- Comparación del rendimiento de los modelos mediante métricas como:
  - Accuracy
  - Precision
  - Recall
  - F1-Score

### **Evaluación de Resultados**
- Validación cruzada para estimar el error de predicción promedio en los diferentes kernels.
- Ajuste de hiperparámetros mediante **Grid Search** para encontrar las mejores combinaciones de `C` y `gamma`.

### **Visualizaciones**
- Matriz de confusión para evaluar el desempeño del modelo en cada kernel.
- Curvas **ROC** y **AUC** para analizar la capacidad del modelo de distinguir entre clases.
- Comparación de tiempos de entrenamiento para cada kernel.
- Gráficas de error que muestran cómo mejora el modelo durante el entrenamiento.

---

## **Conclusiones**
Este apartado incluirá las observaciones clave y lecciones aprendidas una vez finalizado el proyecto.

---

## **Limitaciones**
> **Estado:** En progreso.

- Restricciones relacionadas con los datos disponibles.
- Desafíos en la optimización del modelo.
- Posibles sesgos y errores en la predicción.
  
---

## **Instrucciones de Uso**
> **Estado:** En progreso.

## Integrantes del Grupo:
> **Estado:** En progreso.
