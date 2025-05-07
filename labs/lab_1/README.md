# Laboratorio #1 – Ingeniería de Características Parte 1

Este laboratorio se centra en la aplicación de técnicas fundamentales de **ingeniería de características** utilizando un dataset proporcionado.

## Objetivo

Realizar un análisis exploratorio de las características del dataset y aplicar técnicas adecuadas para el manejo de datos faltantes y codificación de variables categóricas.

## Instrucciones

A partir del dataset proporcionado, realizar las siguientes tareas:

1. **Detección de Valores Faltantes**:
   - Identificar columnas con valores nulos (NA).
   - Calcular proporciones de faltantes por columna.
   - Visualizar con una gráfica de barras los porcentajes de faltantes.

2. **Imputación de Datos**:
   - Variables numéricas: evaluar y aplicar los siguientes métodos de imputación:
     - Análisis de casos completos (CCA)
     - Imputación por media
     - Imputación por mediana
     - Imputación aleatoria (opcional)
   - Variables categóricas:
     - Considerar el impacto en la variable objetivo (target).
     - Evaluar si se debe usar el valor más frecuente.
     - Aplicar indicadores de clase faltante si corresponde.

3. **Codificación de Variables Categóricas**:
   - Aplicar el enfoque más adecuado por variable:
     - One Hot Encoding
     - Codificación por Frecuencia
     - Codificación por Densidad

4. **Clasificación de Variables**:
   - Identificar y clasificar las variables como:
     - Discretas
     - Continuas

## Entregables

- Notebook Jupyter (`lab1.ipynb`) con todo el código, análisis y comentarios explicativos.
- Archivo `dataset_modificado.csv` con los cambios realizados según el procedimiento aplicado.

---

> Este laboratorio sienta las bases para un manejo robusto de datos en proyectos de Machine Learning.
