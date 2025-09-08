# 📊 Análisis Exploratorio de Datos (EDA) - Dataset de Diabetes

## 📝 Resumen del Proyecto

Este proyecto presenta un análisis exploratorio completo del dataset de diabetes, aplicando técnicas de EDA para identificar patrones, detectar anomalías y obtener insights sobre los factores que influyen en el desarrollo de diabetes.

## 🎯 Objetivos

- Realizar un análisis exploratorio detallado del dataset de diabetes
- Identificar patrones y relaciones entre variables
- Detectar y tratar datos sospechosos o erróneos
- Proporcionar insights accionables sobre factores de riesgo de diabetes

## 📊 Dataset

- link de descarga del dataset: https://www.kaggle.com/datasets/mathchi/diabetes-data-set


**Estructura del Dataset:**
- **Registros totales iniciales:** 768 filas
- **Variables:** 9 columnas
- **Registros después de limpieza:** 532 filas
- **Registros eliminados:** 236 (datos sospechosos)

### Variables del Dataset:
1. `Pregnancies` - Número de embarazos
2. `Glucose` - Nivel de glucosa en sangre
3. `BloodPressure` - Presión arterial diastólica
4. `SkinThickness` - Grosor del pliegue cutáneo del tríceps
5. `Insulin` - Insulina en suero de 2 horas
6. `BMI` - Índice de masa corporal
7. `DiabetesPedigreeFunction` - Función de pedigrí de diabetes
8. `Age` - Edad
9. `Outcome` - Variable objetivo (0 = No diabetes, 1 = Diabetes)

## 🔍 Análisis Exploratorio de Datos (EDA)

### 1. ¿Qué es el EDA y cuál es su propósito?

El **Análisis Exploratorio de Datos (EDA)** es el proceso de examinar, visualizar y resumir las características principales de un dataset para entender su estructura, patrones, anomalías y relaciones entre variables antes de aplicar técnicas de modelado más complejas.

**Propósitos principales:**
- Comprender la distribución y características de los datos
- Identificar patrones, tendencias y anomalías
- Detectar errores en los datos
- Formular hipótesis para análisis posteriores
- Decidir qué técnicas de preprocesamiento aplicar

**Ejemplo práctico aplicado:** En nuestro dataset de diabetes, el EDA nos permitió descubrir que 5 registros tenían glucosa = 0 (biológicamente imposible), identificar que personas mayores de 60 años con glucosa < 100 eran casos atípicos, y encontrar una diferencia del 30.2% en valores entre diabéticos y no diabéticos.

### 2. Tipos de Datos y Tratamiento

**Tipos identificados en nuestro dataset:**
- **Numéricos continuos:** BMI, DiabetesPedigreeFunction
- **Numéricos discretos:** Pregnancies, Age, Glucose, BloodPressure, SkinThickness, Insulin
- **Binarios:** Outcome (0/1)

**Tratamiento aplicado:**
- **Numéricos:** Estadísticas descriptivas, histogramas, boxplots, detección de outliers
- **Binarios:** Tablas de frecuencia, análisis de distribución

### 3. Técnicas Básicas Utilizadas

1. **Estadísticas descriptivas:** Media, mediana, desviación estándar
2. **Visualizaciones:** Histogramas, boxplots, scatter plots
3. **Detección de outliers:** Método IQR y Z-score
4. **Análisis de correlación:** Matriz de correlación
5. **Análisis comparativo:** Diabéticos vs no diabéticos

### 4. Análisis Univariado, Bivariado y Multivariado

**Univariado:** Análisis individual de cada variable
- Distribución de glucosa por rangos de edad
- Frecuencia de diabetes por grupo etario

**Bivariado:** Relaciones entre pares de variables
- Glucosa vs Outcome
- Edad vs nivel de glucosa en diabéticos

**Multivariado:** Análisis de múltiples variables simultáneamente
- Matriz de correlación completa
- Patrones combinados de edad, glucosa y embarazos

### 5. Limpieza de Datos

**Proceso implementado:**
- **Detección de valores imposibles:** 5 registros con glucosa = 0
- **Eliminación de datos sospechosos:** 236 registros eliminados
- **Validación biológica:** Verificación de rangos lógicos para variables médicas
- **Resultado:** Dataset más confiable con 532 registros válidos

### 6. Librerías Utilizadas

- **pandas:** Manipulación y análisis de datos estructurados
- **matplotlib:** Visualizaciones básicas (histogramas, scatter plots)
- **seaborn:** Visualizaciones estadísticas avanzadas (heatmaps, boxplots)
- **numpy:** Operaciones numéricas y estadísticas
- **scipy:** Tests estadísticos y análisis avanzado

### 7. Flujo del EDA

1. **Carga de datos** → Importación del dataset
2. **Inspección inicial** → Estructura, tipos de datos, primeras observaciones
3. **Análisis de calidad** → Detección de nulos, duplicados, valores sospechosos
4. **Limpieza** → Eliminación de datos erróneos
5. **Análisis descriptivo** → Estadísticas por variable
6. **Visualizaciones** → Distribuciones y relaciones
7. **Análisis comparativo** → Diabéticos vs no diabéticos
8. **Conclusiones** → Insights y recomendaciones

### 8. Matriz de Correlación

Herramienta clave para identificar relaciones lineales entre variables numéricas. En nuestro análisis reveló las correlaciones más fuertes con el desarrollo de diabetes.

### 9. Detección de Outliers

**Métodos aplicados:**
- **Análisis visual:** Boxplots para identificar valores atípicos
- **Método IQR:** Para detectar outliers en cada variable
- **Validación médica:** Verificación de rangos biológicamente posibles

### 10. Hypothesis Testing

Aplicado para validar diferencias estadísticamente significativas entre grupos de diabéticos y no diabéticos en cada variable del dataset.

## 🔍 Hallazgos Principales

### Distribución de Diabetes
- **No diabetes:** ~69% de la población
- **Con diabetes:** ~31% de la población
- **Diferencia significativa:** 30.2% entre grupos en variables clave

### Patrones por Edad
- **Observación crítica:** Ninguna persona mayor de 60 años tiene glucosa < 100
- **Tendencia:** Los niveles de glucosa tienden a aumentar con la edad
- **Implicación:** La edad es un factor de riesgo importante

### Calidad de Datos
- **Datos sospechosos eliminados:** 30.7% del dataset original
- **Mejora en precisión:** Dataset más confiable para análisis posteriores

## 📈 Visualizaciones Implementadas

1. **Distribuciones univariadas** - Histogramas de cada variable
2. **Análisis bivariado** - Scatter plots y boxplots comparativos
3. **Heatmaps de correlación** - Relaciones entre variables
4. **Análisis por grupos** - Comparativa diabéticos vs no diabéticos
5. **Distribución por rangos de edad** - Patrones etarios específicos

## 🎯 Conclusiones

1. **Limpieza crucial:** La eliminación de datos sospechosos mejoró significativamente la calidad del análisis
2. **Patrones claros:** Existen diferencias marcadas entre diabéticos y no diabéticos
3. **Factor edad:** La edad es un predictor importante, especialmente después de los 60 años
4. **Glucosa como indicador:** Los niveles de glucosa muestran patrones claros según la edad
5. **Dataset válido:** Después de la limpieza, el dataset es confiable para modelado posterior

## 🚀 Próximos Pasos

1. **Modelado predictivo:** Implementar algoritmos de Machine Learning
2. **Feature engineering:** Crear nuevas variables derivadas
3. **Validación cruzada:** Evaluar modelos con diferentes métricas
4. **Interpretabilidad:** Análisis de importancia de características

## 🛠️ Tecnologías Utilizadas

- **Python 3.x**
- **Jupyter Notebook**
- **pandas, numpy**
- **matplotlib, seaborn**
- **scipy.stats**

## 📚 Referencias

- Dataset: Diabetes Prediction Dataset
- Metodología EDA: Técnicas estándar de análisis exploratorio
- Validación médica: Rangos biológicos normales para variables de salud