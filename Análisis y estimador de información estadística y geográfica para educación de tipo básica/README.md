# TinyPred: Predicción de población infantil en México con datos del INEGI

Este proyecto, desarrollado en colaboración con el **INEGI**, busca predecir el número de niños de entre 0 y 5 años por manzana en tres estados de México: **Coahuila, Querétaro y Tabasco**. A partir de datos censales del INEGI, se construyeron modelos de regresión que permitan informar decisiones estratégicas como la ubicación óptima de escuelas preescolares.

## 🧭 Objetivo

Identificar patrones sociodemográficos que permitan predecir de manera precisa la población infantil en una manzana geográfica determinada, utilizando técnicas de **regresión supervisada** y visualización geoespacial.

## 🧩 Datos

Los datos fueron extraídos del Censo 2020 y el DENUE (Directorio Estadístico Nacional de Unidades Económicas). Las variables consideradas incluyen:

- Población total
- Mujeres de 12 a 49 años
- Personas casadas o unidas
- Afiliación religiosa
- Ocupación
- Servicios de salud
- Acceso a internet
- Grado escolar promedio

La **variable objetivo** es la población de niños de 0 a 5 años (`P_0A5`).

## 🔎 Exploración y Transformación

- Análisis exploratorio por estado (Tabasco, Querétaro, Coahuila)
- Limpieza de datos y manejo de valores censurados
- Transformación logarítmica para reducir sesgo y atípicos
- Cálculo de correlaciones y visualizaciones estadísticas

## 🧠 Modelado

Se aplicaron varios modelos de regresión:

- 🔹 Regresión Lineal
- 🔹 Árboles de Decisión
- 🔹 Lasso
- 🔹 Ridge
- 🔹 **Random Forest (modelo seleccionado)**

La evaluación de los modelos se hizo mediante métricas como **R²** y **MSE**, y se aplicó **validación cruzada** con `GridSearchCV`.

## 🌎 Visualización

Se desarrollaron mapas comparativos con **GeoPandas** para mostrar:
- La distribución real de la población infantil
- Las predicciones generadas por el modelo

Esto permite identificar regiones con carencia de infraestructura educativa.

## ✅ Resultados

- El modelo **Random Forest** obtuvo el mejor rendimiento en los tres estados, alcanzando valores de R² de hasta **0.89**.
- Las zonas identificadas como prioritarias para intervención educativa coinciden con regiones de baja cobertura escolar.
- El proyecto tiene viabilidad de implementación real con valor social inmediato.

## 🤝 Equipo

- Daniel Eduardo Arana Bodart
- Isis Yaneth Malfavón Díaz
- Santiago Juárez Roaro  
- Mónica Isabel Casillas Rodríguez  
- Alberto Rodríguez Reyes
- Jose Manuel Guerrero Arellano 


Colaboración con **INEGI**, bajo la guía del profesor **Felipe Castillo Rendón** y **Luis Daniel Mendoza Morales**.

## 📌 Fecha

**Mayo 2024**

---

> Este proyecto fue desarrollado como parte del curso *Análisis de Ciencia de Datos* en el Tecnológico de Monterrey.

