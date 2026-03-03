# 📊 Portafolio de Análisis de Riesgo y Modelado Predictivo (Actuarial Data Science)

Este repositorio contiene una serie de proyectos técnicos enfocados en la modernización de pipelines de datos y la aplicación de simulaciones estocásticas y Machine Learning al sector asegurador. El objetivo principal de estos entregables es transicionar la lógica de reportes operativos tradicionales hacia modelos computacionales escalables en Python.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3
* **Manipulación de Datos:** Pandas, NumPy
* **Probabilidad y Estadística:** SciPy (stats)
* **Machine Learning:** Scikit-Learn (RandomForestClassifier, Metrics)
* **Visualización:** Matplotlib

## 📂 Estructura de los Proyectos

### 1. Limpieza Vectorizada de Cartera (ETL)
Transformación de un dataset crudo de pólizas con anomalías de formato, texto sucio y valores nulos.
* **Técnicas:** Expresiones regulares (`regex`) para limpieza de strings, imputación de nulos sesgados mediante promedios filtrados, y aplicación de máscaras booleanas para eliminación de outliers (edades irreales).

### 2. Simulación de Monte Carlo (Modelo de Riesgo Colectivo)
Cálculo de la Prima Pura y el Valor en Riesgo (VaR) al 99% mediante simulación computacional de miles de escenarios anuales.
* **Técnicas:** Generación de variables aleatorias cruzando distribuciones de Poisson (Frecuencia de siniestros) y distribuciones Lognormales (Severidad de siniestros). Dominio absoluto de `matplotlib.ticker` para control de notación y escalas financieras.

### 3. Detección de Fuga de Clientes (Churn) y Optimización Financiera
Desarrollo de un modelo predictivo para identificar asegurados con alto riesgo de cancelación de póliza, superando la limitación del accuracy general mediante el ajuste de pesos en clases desbalanceadas.
* **Técnicas:** Entrenamiento de un *Random Forest Classifier* (`class_weight='balanced'`), extracción de *Feature Importances* para explicar los causales de riesgo a la gerencia, e iteración dinámica de la función `predict_proba`.
* **Impacto de Negocio:** Sustitución de la matriz de confusión estática por una Matriz de Costos financiera. Se iteraron más de 100 umbrales de probabilidad para encontrar el punto de equilibrio matemático exacto que maximiza la retención de capital aplicando un 10% de descuento dinámico sobre la prima pura.

---
*Explora los archivos `.ipynb` para revisar el código fuente y las imágenes adjuntas para visualizar los reportes finales.*
