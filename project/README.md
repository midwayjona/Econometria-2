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
