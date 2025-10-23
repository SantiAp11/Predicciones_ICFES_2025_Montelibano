# Análisis Predictivo ICFES Saber 11°: Proyección 2025 para Montelíbano

Este proyecto de Data Science aplica el análisis de series de tiempo para proyectar los puntajes globales promedio (Puntaje Global) de 8 colegios del municipio de Montelíbano, Córdoba, para el año 2025.

El objetivo principal es pasar de la simple visualización de datos históricos a la generación de **insights estratégicos** basados en la inercia de crecimiento de cada institución.

## Perfil Profesional

Conéctate o revisa otros proyectos:

| Plataforma | Enlace |
| :--- | :--- |
| **LinkedIn** | Santiago Aparicio Pérez](https://www.linkedin.com/in/santiap/) |
| **Portafolio** |(https://santiap11.github.io/) |

---

## Objetivo y Enfoque

El proyecto busca medir y predecir el rendimiento educativo individual de los colegios. El valor clave de este análisis es el **Coeficiente de Tendencia Anual**, que revela la velocidad de mejora (o deterioro) de cada institución a lo largo del tiempo.

## Metodología

El análisis se basa en datos históricos del ICFES Saber 11° entre los años 2014 y 2024.

1.  **Limpieza y Filtrado:** Estandarización de nombres geográficos y filtrado de datos para el municipio de Montelíbano, Córdoba.
2.  **Imputación:** Manejo de datos faltantes para garantizar una serie de tiempo continua para cada institución.
3.  **Modelado:** Se entrenó un modelo de **Regresión Lineal Simple** (LinearRegression de Scikit-learn) por separado para cada uno de los 8 colegios.
4.  **Métricas Clave:** El **RMSE** (Root Mean Squared Error) valida la fiabilidad del modelo, y el **Coeficiente** es utilizado como la **Tendencia Anual (pts/año)**.

## Resultados Clave (Predicción 2025)

El liderazgo se mantiene, pero las tendencias son cruciales para la toma de decisiones. A continuación, la tabla resumen generada por el modelo:

### Tabla de Resultados de la Regresión Lineal
![Tabla de resultados del modelo de Regresión Lineal con predicción 2025 y tendencias](assets/tabla_regresion.png)

| Colegio | Predicción Puntaje Global 2025 | Tendencia Anual (Coeficiente) | RMSE (Error Histórico) |
| :--- | :--- | :--- | :--- |
| **FUNDACIÓN EDUCATIVA DE MONTELÍBANO** | 331.37 | +0.99 | 5.88 |
| **I.E. SAN ANTONIO MARÍA CLARET** | 311.22 | **+4.20** | 10.12 |
| **COLEGIO BERNARDO OSPINA VILLA** | 282.17 | **+4.88** | 5.69 |
| **COLEGIO EL ROSARIO** | 327.76 | +2.51 | 12.00 |
| **I.E. CONCENTRACIÓN EDUCATIVA DEL SUR DE MONTELÍBANO** | 230.59 | **-0.19 (ALERTA)** | 3.69 |


## Visualización de la Proyección

El siguiente gráfico de líneas muestra la trayectoria histórica de cada colegio (líneas sólidas) y cómo el modelo de Regresión Lineal proyecta esa tendencia hasta el año 2025.

### Gráfico de Proyección Histórica
![Gráfico de líneas con trayectoria histórica de puntajes y proyección a 2025](assets/grafico_proyeccion.png)

## Archivos y Tecnologías

* `prediccion_icfes.ipynb`: Notebook de Google Colab/Jupyter con el código completo, desde la limpieza de datos hasta el entrenamiento de los 8 modelos.
* **Tecnologías:** Python, Pandas, Scikit-learn (Regresión Lineal), Plotly (Visualización).
