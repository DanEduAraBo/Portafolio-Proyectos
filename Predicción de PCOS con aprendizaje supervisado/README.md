# Diagnóstico del Síndrome de Ovario Poliquístico (PCOS) con Aprendizaje Supervisado

Este proyecto implementa modelos de aprendizaje supervisado para predecir la presencia del **Síndrome de Ovario Poliquístico (PCOS)** en mujeres, utilizando un dataset clínico recopilado en hospitales de la India. Se aplicaron dos enfoques: **redes neuronales** y **random forest**, comparando su precisión y utilidad en contextos médicos.

## Objetivo

Desarrollar modelos de inteligencia artificial que permitan predecir con precisión el diagnóstico de PCOS en mujeres, considerando parámetros clínicos, físicos y hormonales.

## Dataset

- Fuente: [Kaggle - Polycystic Ovary Syndrome (PCOS)](https://www.kaggle.com/datasets/prasoonkottarathil/polycystic-ovary-syndrome-pcos)
- Tamaño: 999 registros, 45 columnas
- Contenido:
  - Parámetros clínicos: niveles hormonales, antecedentes familiares, síntomas físicos
  - Variables categóricas y numéricas
  - Etiqueta binaria: presencia o ausencia de PCOS (`PCOS (Y/N)`)

## Proceso

1. **Limpieza de datos:**
   - Eliminación de registros con valores nulos (<0.3%)
   - Transformaciones logarítmicas en variables con sesgo

2. **Análisis exploratorio:**
   - Histogramas, diagramas de cajas y conteos categóricos
   - Selección y codificación de variables relevantes

3. **Modelado:**
   - **Red Neuronal (MLPClassifier con GridSearchCV):**
     - Arquitectura final: capas ocultas (50, 25), `max_iter=2500`
     - División 80/20 entrenamiento/prueba
     - Validación cruzada para elegir hiperparámetros
   - **Random Forest:**
     - 100 árboles (`n_estimators`)
     - División 80/20 con los mismos datos para comparación justa

## Resultados

### Red Neuronal:
- **Precision:** 0.91 (PCOS) / 0.42 (No-PCOS)  
- **Recall:** 0.91 (PCOS) / 0.42 (No-PCOS)  
- Ventaja: Detecta muy bien casos positivos, aunque a costa de falsos positivos.

### Random Forest:
- **Precision:** 0.86 (PCOS) / 0.89 (No-PCOS)  
- **Recall:** 0.74 (PCOS) / 0.95 (No-PCOS)  
- Ventaja: Excelente para descartar falsos positivos, menor sensibilidad en casos reales de PCOS.

Ambos modelos superan el azar (ROC AUC > 0.5), pero con perfiles de utilidad distintos.

## Recomendaciones

- Utilizar técnicas de balanceo de clases como **SMOTE** para mejorar la detección de la clase minoritaria.
- Explorar modelos híbridos o más avanzados como XGBoost o redes neuronales profundas.
- Ajustar umbrales de decisión según el contexto clínico.

## Recursos del proyecto

- [Repositorio del proyecto (DRIVE)](https://colab.research.google.com/drive/1ZBj469Bg1qYPRsv-S0e8pSs3uxwS3m_1?usp=sharing)
- [Base de datos original](https://drive.google.com/file/d/1iJV5HXXIab-9ja2b2PwgXOH_OaR8inXX/view?usp=sharing)

## Equipo

- Daniel Eduardo Arana Bodart  
- Jose Manuel Guerrero Arellano  
- Valeria García Hernández  

## Profesora

- Dra. María Valentina Navárez Terán

## Curso

Modelación del Aprendizaje con Inteligencia Artificial  
Tecnológico de Monterrey

Abril 2024

---

> Este trabajo demuestra el potencial y las limitaciones del aprendizaje supervisado en aplicaciones clínicas, y promueve el uso responsable de la inteligencia artificial como herramienta de apoyo médico.
