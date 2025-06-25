# Proyecto de Machine Learning para Regresiones – Predicción de Ventas Semanales de Walmart

Proyecto final del curso **Econometría II – Machine Learning** (Maestría en Investigación de Operaciones, Universidad Galileo).
El reto consiste en construir y comparar varios modelos de regresión que pronostiquen las ventas semanales de tiendas Walmart a partir de variables económicas y temporales.

---

## Archivos clave (raíz del repositorio)

| Archivo                                              | Descripción                                                                                                                                                                |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`proyecto_final.ipynb`](./proyecto_final.ipynb)     | Notebook con todo el flujo: EDA → ingeniería de características → pipelines → ajuste de hiper‑parámetros → evaluación y conclusiones. **Haz clic para abrirlo en GitHub.** |
| [`Walmart.csv`](./Walmart.csv)                       | Dataset original con registros de ventas y variables externas.                                                                                                             |
| [`resultados_modelos.csv`](./resultados_modelos.csv) | Salida del notebook con el ranking final de modelos y sus métricas (RMSE). **Disponible tras ejecutar el notebook.**                                                       |
| `Proyecto_Final_v2025.pdf`                           | Guía oficial del proyecto (resumen abajo).                                                                                                                                 |

---

## Resumen de la guía del proyecto (`Proyecto_Final_v2025.pdf`)

La guía establece un flujo de trabajo en cuatro fases:

1. **Exploratory Data Analysis (EDA)** – análisis gráfico y estadístico del target (`Weekly_Sales`) y de las variables explicativas; detección de tendencias temporales y correlaciones.
2. **Ingeniería de características** – imputación de valores faltantes, codificación de variables categóricas, tratamiento de outliers, transformaciones y escalado dentro de un `Pipeline` reproducible.
3. **Modelado y comparación** – entrenamiento de al menos siete algoritmos de regresión (Lineal, Ridge/Lasso, SVR, Árboles, Random Forest, Gradient Boosting, K‑NN y Redes Neuronales), optimizando hiper‑parámetros con validación cruzada repetida y comparando el desempeño mediante **RMSE**.
4. **Reporte de resultados** – selección del modelo campeón, generación de un archivo `.csv` con el ranking de modelos y redacción de conclusiones accionables.

---

## Conjunto de datos

| Archivo       | Descripción                                                        | Variables clave                                                                                      |
| ------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `Walmart.csv` | Datos históricos de ventas semanales de Walmart entre 2010 y 2012. | `Store`, `Date`, `Weekly_Sales`, `Holiday_Flag`, `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`. |

* **Tamaño aproximado**: 6435 filas × 8 columnas.
* **Target**: `Weekly_Sales` (ventas semanales en USD).
* **Granularidad**: Una observación por tienda y semana.

---
## Contexto del curso

* **Workflow completo de ML**: ingestión de datos, ingeniería de características, selección y optimización de modelos, y MLOps básico.
* Implementación práctica en **Python** con `pandas`, `scikit‑learn`, `tensorflow/keras` y gestión del ciclo de vida en **GitHub**.

---


---

> *Autor: Jonathan Amado — Carnet 14002285*
>
> *Maestría en Investigación de Operaciones, Universidad Galileo — 2025*


















# Proyecto de Machine Learning para Regresiones – Predicción de Ventas Semanales de Walmart

Proyecto final del curso **Econometría II (Machine Learning)** de la Maestría en Investigación de Operaciones de la Universidad Galileo. El objetivo es construir y comparar distintos modelos de regresión para pronosticar las ventas semanales de tiendas Walmart a partir de variables económicas y temporales.

---

## 1. Objetivos del proyecto

1. **Análisis Exploratorio de Datos (EDA)**

   * Identificar patrones, tendencias estacionales y posibles valores atípicos.
   * Comprender la distribución y correlación de las variables con el target `Weekly_Sales`.
2. **Ingeniería de Características**

   * Limpieza y tratamiento de valores faltantes.
   * Codificación de variables categóricas y creación de atributos derivados a partir de la fecha.
   * Escalado/transformación de variables numéricas y tratamiento de outliers.
3. **Modelado y Evaluación**

   * Implementar un pipeline reproducible en `scikit‑learn` que incluya pre‑procesamiento y entrenamiento.
   * Ajustar y comparar múltiples algoritmos de regresión (Lineal, SVR, Árboles, Ensambles, KNN, Redes Neuronales) usando **RMSE** como métrica principal.
   * Documentar resultados y conclusiones dentro del notebook Jupyter.

---

## 2. Conjunto de datos

| Archivo       | Descripción                                                        | Variables clave                                                                                      |
| ------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------- |
| `Walmart.csv` | Datos históricos de ventas semanales de Walmart entre 2010 y 2012. | `Store`, `Date`, `Weekly_Sales`, `Holiday_Flag`, `Temperature`, `Fuel_Price`, `CPI`, `Unemployment`. |

* **Tamaño aproximado**: 6435 filas × 8 columnas.
* **Target**: `Weekly_Sales` (ventas semanales en USD).
* **Granularidad**: Una observación por tienda y semana.

---

## 3. Metodología de trabajo

1. Crear un entorno virtual y clonar este repositorio.
2. Abrir el notebook `proyecto_final.ipynb` y ejecutar las celdas secuencialmente:

   1. **Carga de datos y EDA**.
   2. **Construcción del ColumnTransformer** con la ingeniería de características.
   3. **Entrenamiento y afinamiento de modelos** mediante *GridSearchCV* o *RandomizedSearchCV* dentro de un *RepeatedKFold*.
   4. **Comparación de RMSE** y selección del modelo campeón.
   5. **Conclusiones** y guardado de métricas en `resultados_modelos.csv`.

> **Nota:** Todos los archivos del proyecto (datos, notebook, scripts y resultados) residen en el mismo directorio raíz para simplificar la entrega y la revisión.
