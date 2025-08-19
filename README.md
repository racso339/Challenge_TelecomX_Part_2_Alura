# 📊 Análisis de la Tasa de Cancelación de Clientes (Churn Rate)

## 📝 Resumen del Proyecto
Este proyecto tuvo como propósito **analizar y predecir la tasa de cancelación (Churn Rate)** de clientes.  
🎯 El objetivo central fue desarrollar un modelo de Machine Learning capaz de detectar a los clientes con alta probabilidad de cancelar.  
A partir de este análisis se identificaron **factores determinantes** y se diseñaron **estrategias de retención** basadas en dichos hallazgos.

---

## 🔧 Metodología

La segunda etapa del proyecto se concentró en el diseño, entrenamiento y validación de los modelos.  
El flujo de trabajo incluyó:

### 1️⃣ Preparación de Datos y Modelado
- ✂️ **División de datos:** 80% entrenamiento / 20% prueba.  
- 📏 **Normalización:** aplicada a variables numéricas, esencial en modelos sensibles a escala como la **Regresión Logística**.

### 2️⃣ Entrenamiento y Evaluación de Modelos
Se probaron dos algoritmos principales: **Regresión Logística** y **Árbol de Decisión**.

#### 🔹 Regresión Logística
- 📈 **Exactitud:** 80%.  
- ✅ **Conclusión:** Modelo equilibrado, con resultados similares en entrenamiento (79%) y prueba (80%). Sin señales de sobreajuste.

#### 🔹 Árbol de Decisión
- 📉 **Exactitud:** 72% en prueba.  
- ⚠️ **Conclusión:** Presentó **overfitting**: 99% en entrenamiento pero caída al 72% en prueba.

### 3️⃣ Análisis de Variables Clave
Tanto la Regresión Logística como el Árbol de Decisión coincidieron en que los factores más influyentes son:  
- 💵 **Charges.Total**  
- 💳 **Charges.Monthly**  
- 📊 **Cuentas_Diarias**  
- 📜 **Contract**  

👉 Los **patrones de gasto** y el **tipo de contrato** son los elementos más decisivos en la cancelación.

### 4️⃣ Conclusiones y Estrategias
El modelo seleccionado fue la **Regresión Logística** por su rendimiento y estabilidad.  

🔑 Estrategias derivadas del análisis:  
- 🎁 **Ofrecer valor agregado** → incluir servicios extra (streaming, datos móviles, beneficios exclusivos) para clientes con altos cargos mensuales.  
- 🤝 **Fomentar contratos largos** → incentivar planes de 1 o 2 años con descuentos y beneficios, reduciendo la tasa de cancelación.

---

## 📂 Archivos Relevantes
- 🗂️ **modelo_lr.pkl** → Modelo de Regresión Logística serializado con *pickle*, listo para predicciones futuras.
