# 📊 TelecomX — Predicción de Churn con Machine Learning

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-F7931E?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-yellow)

**Parte 2** del desafío Alura TelecomX. Modelado de clasificación para predecir la cancelación de clientes (churn), identificación de factores clave y selección de estrategias de retención.

---

## 🎯 Problema de negocio

TelecomX necesita identificar **qué clientes están en riesgo de cancelar el servicio** para actuar proactivamente con campañas de retención. Predecir el churn permite priorizar acciones de fidelización sobre los clientes de mayor riesgo, entender qué variables influyen más en la decisión de cancelar, y diseñar políticas comerciales basadas en evidencia.

Este proyecto continúa el [Análisis Exploratorio (Parte 1)](https://github.com/racso339/racso339-Challenge_TelecomX_Alura) con la fase de **modelado predictivo**.

---

## 🛠️ Stack técnico

**Python 3.10+** · **Pandas** · **NumPy** · **scikit-learn** (LogisticRegression, DecisionTreeClassifier, KNeighborsClassifier, train_test_split, LabelEncoder, MinMaxScaler, accuracy_score, confusion_matrix, precision_score, recall_score, f1_score) · **Matplotlib** · **Seaborn** · **Pickle** · **Jupyter Notebook (Google Colab)**

---

## 📂 Estructura del repositorio

`Challenge_TelecomX_Pt2.ipynb` — Notebook con todo el análisis y modelado

`telecom_df_final.csv` — Dataset procesado (output del EDA)

`requirements.txt` — Dependencias del proyecto

`README.md`

---

## 🚀 Cómo reproducir

**Paso 1.** Clonar el repositorio: `git clone https://github.com/racso339/Challenge_TelecomX_Part_2_Alura.git`

**Paso 2.** Instalar dependencias: `pip install -r requirements.txt`

**Paso 3.** Abrir el notebook: `jupyter notebook Challenge_TelecomX_Pt2.ipynb`

O abrir directamente en [Google Colab](https://colab.research.google.com/github/racso339/Challenge_TelecomX_Part_2_Alura/blob/master/Challenge_TelecomX_Pt2.ipynb).

---

## 📈 Metodología

**(a)** Carga e importación de datos (CSV procesado del EDA de la Parte 1).

**(b)** Eliminación de columnas irrelevantes para el modelado.

**(c)** Encoding de variables categóricas con LabelEncoder.

**(d)** Verificación de la proporción de churn y diagnóstico de desbalance de clases.

**(e)** Balanceo de clases para evitar sesgo del modelo hacia la clase mayoritaria.

**(f)** Normalización de variables numéricas con MinMaxScaler.

**(g)** Separación de datos en train/test.

**(h)** Entrenamiento y evaluación de tres modelos: Regresión Logística, K-Nearest Neighbors (KNN) y Árbol de Decisión.

**(i)** Análisis de correlación y análisis dirigido de variables clave.

**(j)** Selección y serialización del mejor modelo con pickle.

---

## 🏆 Resultados clave

| Modelo | Accuracy (aprox.) |
|---|---|
| **Regresión Logística** ⭐ | **80 %** |
| K-Nearest Neighbors | 77 % |

La **Regresión Logística** fue seleccionada como el modelo final por su mejor desempeño (~3 puntos porcentuales sobre KNN), su interpretabilidad y su menor tendencia al sobreajuste en este dataset.

El modelo final se serializó como `modelo_lr.pkl` para reutilización sin re-entrenar.

---

## 📊 Visualizaciones en el notebook

El notebook contiene tres gráficos clave: importancia de variables (correlación de cada feature con churn), gasto total vs cancelación (boxplot que muestra cargos mensuales más altos en clientes que cancelan), y tipo de contrato vs tasa de churn (los contratos mes-a-mes presentan mucha mayor tasa de cancelación que los anuales).

👉 **[Abrir notebook con todos los gráficos](Challenge_TelecomX_Pt2.ipynb)**

---

## 💡 Conclusiones de negocio

▸ Los **contratos de corto plazo (mes-a-mes)** son la mayor fuente de churn. Recomendación: incentivar migración a contratos anuales con descuentos.

▸ Los clientes con **cargos mensuales altos** y poco tiempo en la compañía son los más propensos a cancelar. Priorizar atención y ofertas de retención en este segmento.

▸ La mayoría de cancelaciones ocurre en **etapas tempranas de la relación**. Reforzar onboarding y experiencia de los primeros meses.

---

## 🔗 Proyectos relacionados

🔍 [**TelecomX — Parte 1 (EDA)**](https://github.com/racso339/racso339-Challenge_TelecomX_Alura) — Análisis exploratorio que precede a este modelado.

---

## 👤 Autor

**Oscar Serna** — Ingeniero electricista (UNAL) en pivot a roles de datos.

🔗 LinkedIn: [linkedin.com/in/oscar-hserna](https://www.linkedin.com/in/oscar-hserna)

📧 Email: ohsernap@unal.edu.co · racso339@gmail.com

🐙 GitHub: [@racso339](https://github.com/racso339)

---

📜 Distribuido bajo licencia MIT.
