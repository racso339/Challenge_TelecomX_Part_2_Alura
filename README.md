# Challenge_TelecomX_Part_2_Alura

# Análisis de la Tasa de Cancelación de Clientes (Churn Rate)

## Resumen del Proyecto
Este proyecto tuvo como propósito **analizar y predecir la tasa de cancelación (Churn Rate)** de clientes.  
El objetivo principal fue construir un modelo de Machine Learning capaz de identificar aquellos clientes con mayor probabilidad de abandonar el servicio.  
A partir del análisis, se determinaron los factores clave detrás de la cancelación y se plantearon **estrategias de retención** fundamentadas en estos hallazgos.

---

## Metodología

La segunda fase del proyecto se enfocó en el diseño, evaluación y justificación de los modelos de Machine Learning.  
El flujo de trabajo contempló los siguientes pasos:

### 1. Preparación de Datos y Modelado
- **División de datos:** 80% para entrenamiento y 20% para prueba, garantizando una evaluación justa.  
- **Normalización:** Se aplicó a las variables numéricas, paso esencial en modelos sensibles a la escala, como la Regresión Logística.

### 2. Entrenamiento y Evaluación de Modelos
Se entrenaron dos modelos principales: **Regresión Logística** y **Árbol de Decisión**.

#### 🔹 Regresión Logística
- **Rendimiento:** Exactitud del 80%.  
- **Justificación:** Mostró un buen balance, con resultados consistentes en entrenamiento (79%) y prueba (80%). Esto refleja capacidad de generalización y ausencia de sobreajuste.

#### 🔹 Árbol de Decisión
- **Rendimiento:** Exactitud del 72% en los datos de prueba.  
- **Justificación:** Presentó sobreajuste claro: 99% de exactitud en entrenamiento frente a solo 72% en prueba, lo que indica falta de generalización.

### 3. Análisis de Importancia de Variables
Se identificaron las variables más relevantes para explicar la cancelación:  
- **Charges.Total**  
- **Charges.Monthly**  
- **Cuentas_Diarias**  
- **Contract**  

Ambos modelos coincidieron en que los **patrones de gasto y el tipo de contrato** son los factores más determinantes.

### 4. Conclusiones y Estrategias
El modelo elegido como final fue la **Regresión Logística**, por su desempeño y estabilidad.  

Con base en los resultados, se propusieron acciones de retención como:  
- **Añadir valor agregado:** ofrecer servicios adicionales (ej. streaming, datos extra) a clientes con cargos mensuales elevados.  
- **Promover contratos largos:** incentivar planes de uno o dos años para reducir la probabilidad de cancelación.

---

## Archivos Relevantes
- **modelo_lr.pkl** → Modelo de Regresión Logística serializado con *pickle*, listo para cargarse y usarse en predicciones futuras.
