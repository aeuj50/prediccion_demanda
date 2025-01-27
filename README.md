# Predicción de la Demanda con Light Gradient Boosting Machine (LGBM)

Este repositorio contiene los notebooks y recursos utilizados en un proyecto de predicción de la demanda basado en datos históricos de ventas de una empresa minorista. El enfoque principal del proyecto es aplicar modelos de aprendizaje automático para predecir las ventas a diferentes niveles de detalle y mejorar la planificación de inventarios.

## Descripción de los Archivos

### 1. [preprocesamiento-transformaci-n-y-limpieza.ipynb](preprocesamiento-transformaci-n-y-limpieza.ipynb)
Este notebook detalla los pasos realizados para preparar y transformar los datos en conjuntos listos para el modelado. Incluye:
- **Revisión y carga de datos**: Los conjunto de datos iniciales fueron obtenidos en Kaggle, dentro de la competencia M5: https://www.kaggle.com/c/m5-forecasting-accuracy/overview Una vez cargados los datos, se procedió a con una exploración inicial de las tablas de ventas, calendario y precios.
- **Transformaciones clave**: 
  - Conversión de formatos de datos.
  - Filtrado de registros específicos, como datos de una tienda en California y los últimos tres años.
  - Creación de niveles de agregación por categoría (`FOODS`) y por ítem (`FOODS_2_347`).
- **Limpieza de datos**: Manejo de valores faltantes, duplicados y optimización de tipos de datos.

### 2. [modelo-predictivo-demanda-por-categoria.ipynb](modelo-predictivo-demanda-por-categoria.ipynb)
Este notebook presenta el desarrollo y optimización de un modelo de predicción de demanda a nivel de categoría. Incluye:
- Carga del archivo: 'df_foods_agg.csv' disponible en este repositorio
- Exploración de los datos de la categoría `FOODS`.
- Construcción y evaluación del modelo LightGBM, utilizando validación cruzada y búsqueda aleatoria para optimizar hiperparámetros.
- Visualización de predicciones y análisis de importancia de características.

### 3. [modelo-predictivo-demanda-por-tem.ipynb](modelo-predictivo-demanda-por-tem.ipynb)
Este notebook se enfoca en la predicción de demanda a nivel de ítem, específicamente para `FOODS_2_347`. Incluye:
- Carga del archivo: 'df_foods_2_347_agg.csv' disponible en este repositorio
- Análisis detallado de los datos del ítem seleccionado.
- Implementación de técnicas avanzadas de ingeniería de características, como medias móviles ponderadas y retrasos (`lags`).
- Optimización del modelo LightGBM y análisis de desempeño utilizando métricas como MAE y RMSE.

## Tecnologías Utilizadas
- **Python**: Para el análisis de datos y modelado.
- **Bibliotecas principales**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `lightgbm`, `scikit-learn`.
- **Notebooks**: Ejecutados en un entorno Jupyter.

