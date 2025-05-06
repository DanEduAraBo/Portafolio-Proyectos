# Impacto de factores no antropogénicos en los niveles de contaminación del aire

Este proyecto analiza cómo los **factores climáticos y meteorológicos** (no antropogénicos) influyen en los niveles de contaminación del aire en Monterrey, Nuevo León. Utilizando técnicas estadísticas y de inteligencia artificial, se estudió la capacidad de estos factores para predecir contaminantes como el ozono, PM2.5, CO, entre otros.

## 🧭 Objetivo

Evaluar si variables como **temperatura, humedad, presión atmosférica y velocidad del viento** tienen un impacto significativo en la calidad del aire, sin tomar en cuenta factores humanos, mediante modelos de:

- 📊 **Regresión Lineal Multivariada**  
- 🤖 **Redes Neuronales Recurrentes (LSTM)**

## 📊 Datos

- **Origen:** Sistema Integral de Monitoreo Ambiental (SIMA), Nuevo León  
- **Periodo:** 2023–2024  
- **Variables principales:**
  - Contaminantes: CO, NO, NO₂, NOₓ, O₃, PM10, PM2.5, SO₂
  - Meteorológicos: Temperatura, Humedad Relativa, Presión, Velocidad del viento, etc.
  - Más de **13,800 registros** y **239 columnas**

## ⚙️ Procesamiento

- **Imputación de valores faltantes** con K-Nearest Neighbors
- **Escalamiento de variables** con StandardScaler
- **Transformaciones estadísticas** usando `bestNormalize` para cumplir supuestos de normalidad
- Selección de estaciones de monitoreo con menor tasa de valores nulos

## 🧪 Modelado

### 🔹 Regresión Lineal Multivariada (RStudio)

- Se modeló cada contaminante con base en 4 variables meteorológicas
- Validación de supuestos: residuos normales, homocedasticidad, correlación canónica
- Mejor 𝑅² ajustado: **0.46** (modelo de O₃)
- Limitación: multicolinealidad y transformación forzada

### 🔸 Redes Neuronales (Python - Keras)

- **Arquitectura LSTM:** 2 capas densas (64 y 32 neuronas), activación ReLU
- **Entrenamiento:** 150 épocas, early stopping, optimizador Adam
- Se entrenaron redes para predecir Ozono (O₃) con:
  - Solo factores no antropogénicos (mejor rendimiento)
  - Combinaciones con NO, NO₂, NOₓ (menor precisión)

#### 🔍 Mejor resultado:
- MAE: **0.01014**
- Predicción acertada de patrones temporales, incluso sin variables antropogénicas

## 🧠 Conclusión

Sí, los **factores no antropogénicos tienen un impacto significativo** en los niveles de contaminación, especialmente en el Ozono. Aunque no explican completamente el fenómeno, permiten generar modelos predictivos precisos. La red neuronal con solo factores naturales superó incluso a modelos que incluían contaminantes como predictores.

## 📁 Recursos
- 📄 [Repositorio del proyecto (DRIVE)](https://drive.google.com/drive/folders/1n8xeJCoJLUbla0iFVKPEUHZIQIs49O5u?usp=sharing)

## 👥 Equipo

- Daniel Eduardo Arana Bodart  
- Isis Yaneth Malfavón Díaz  
- Santiago Juárez Roaro  
- Ericka Sofía Rodríguez Sánchez  
- Alfredo André Durán Treviño  

## 🧑‍🏫 Profesores

- Dra. Blanca Rosa Ruiz Hernández  
- Mtro. Rodolfo Fernández de Lara Hadad  

## 🏫 Curso

Aplicación de Métodos Multivariados en Ciencia de Datos  
Tecnológico de Monterrey — Campus Monterrey  
📅 Septiembre 2024

---

> Este proyecto fue realizado en colaboración con **SIMA Nuevo León** y busca contribuir al diseño de estrategias preventivas basadas en modelos predictivos de calidad del aire.
