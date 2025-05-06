# Clustering de Salud Mental Estudiantil con Aprendizaje No Supervisado

Este proyecto emplea técnicas de aprendizaje no supervisado para segmentar a estudiantes universitarios según su estado de salud mental. Utilizando un dataset con variables psicológicas, académicas y de estilo de vida, se aplicaron modelos de **K-Means** y **K-Modes** para identificar perfiles recurrentes sin necesidad de etiquetas.

## 🎯 Objetivo

Agrupar a estudiantes universitarios de acuerdo con características relacionadas con su salud mental, permitiendo así:

- Detectar patrones comunes de estrés, ansiedad o depresión.
- Comprender factores asociados a la salud mental en la comunidad estudiantil.
- Proponer futuros modelos de intervención o estudio más específicos.

## 🗃️ Dataset

- Fuente: [Kaggle - Students Mental Health Assessment](https://www.kaggle.com/datasets/sonia22222/students-mental-health-assessments)
- Tamaño: 7022 registros, 20 columnas
- Variables incluyen:
  - Edad, género, carrera, promedio, número de créditos
  - Niveles de estrés, ansiedad, depresión
  - Calidad del sueño, dieta, actividad física
  - Apoyo social, historial familiar de salud mental
  - Consumo de sustancias y enfermedades crónicas

## ⚙️ Proceso

1. **Limpieza de datos:**
   - Eliminación de registros con valores nulos (<0.4%)
   - Codificación numérica de variables categóricas ordinales

2. **Exploración de datos:**
   - Histogramas, diagramas de caja, gráficos de pastel y barras
   - Análisis por tipo de variable (numérica y categórica)

3. **Modelado:**
   - 🔹 **K-Means:** Usado tras reducción de dimensionalidad con PCA
     - Determinación de número óptimo de clusters con método del codo y coeficiente de siluetas
     - Mejores resultados con **4 clusters**
   - 🔸 **K-Modes:** Enfocado en variables categóricas
     - Resultados pobres debido a mezcla de tipos de datos
     - Consideración futura: uso de K-Prototypes

## 📊 Resultados

- **K-Means (4 clusters):**
  - Agrupaciones claras tras transformación PCA
  - Permite interpretación y análisis posterior de perfiles estudiantiles
- **K-Modes:**
  - Coeficiente de siluetas cercano a 0 → agrupaciones poco distinguibles
  - Recomendación de eliminar variables numéricas o cambiar de algoritmo

## 🧠 Conclusión

El análisis demostró que es posible agrupar perfiles de estudiantes basados en su salud mental mediante técnicas no supervisadas. Se recomienda el uso de algoritmos mixtos como **K-Prototypes** para mejorar la segmentación con variables categóricas y numéricas combinadas.

## 🔗 Recursos del proyecto

- 📁 [Notebook en Google Colab](https://colab.research.google.com/drive/1cgZ1ezkdVXi_3qEUXlhkc4nZRmMdQEMn?usp=sharing)
- 📊 [Base de datos en Google Drive](https://drive.google.com/file/d/1CKvM020-eHGErHYtVX1WSGN2mVtz1gy1/view?usp=sharing)

## 👥 Equipo

- Daniel Eduardo Arana Bodart  
- Jose Manuel Guerrero Arellano  
- Valeria García Hernández  

## 🧑‍🏫 Profesora

- Dra. María Valentina Navárez Terán

## 🏫 Curso

Modelación del Aprendizaje con Inteligencia Artificial  
Tecnológico de Monterrey
📅 Abril 2024

---

> Este proyecto busca sensibilizar sobre el estado emocional de estudiantes universitarios y explorar cómo la inteligencia artificial puede apoyar a la salud mental desde un enfoque exploratorio y no invasivo.
