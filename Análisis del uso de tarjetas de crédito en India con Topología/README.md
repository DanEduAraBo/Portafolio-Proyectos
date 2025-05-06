# Formas de Gasto: Una Segmentación Bancaria con Análisis Topológico de Datos

Este proyecto explora el uso del **Análisis Topológico de Datos (TDA)** para segmentar usuarios de tarjetas de crédito en la India a partir de sus patrones de gasto. Utilizando técnicas como **Mapper**, **homología persistente** y **clasificación supervisada**, se buscó descubrir estructuras subyacentes en los datos que pudieran informar decisiones comerciales y de segmentación.

## Objetivo

Determinar si es posible agrupar a los clientes en segmentos diferenciables y persistentes desde una perspectiva topológica, evaluando:

- La existencia de patrones repetitivos y conectividad entre clientes.
- La estabilidad de las estructuras topológicas.
- La viabilidad de predecir a qué segmento pertenece un nuevo cliente.

## Metodología

El análisis se desarrolló en cuatro fases:

1. **Preprocesamiento:** Codificación One-Hot y normalización con `RobustScaler` de Scikit-learn.
2. **Análisis exploratorio:** Estadísticas descriptivas y reducción de dimensionalidad.
3. **TDA:** Aplicación de Mapper (con UMAP + DBSCAN) y homología persistente (Ripser).
4. **Clasificación:** Modelo Random Forest para predecir etiquetas generadas por Mapper.

## Resultados

- **Mapper** reveló un único cluster dominante con pocos grupos periféricos.
- **Diagramas de persistencia** y **landscapes** mostraron patrones cíclicos poco diferenciados entre grupos.
- **Clasificación** exitosa debido a la existencia de un solo grupo significativo, más que a la calidad del modelo.

## Conclusiones

Aunque la hipótesis de segmentos topológicamente diferenciables fue rechazada, el proyecto valida el **potencial del TDA como herramienta exploratoria** en contextos financieros. Se identificó un comportamiento común entre la mayoría de usuarios y se destacó la estabilidad estructural del dataset.

## Recursos

- [Repositorio del proyecto (DRIVE)](https://drive.google.com/drive/folders/18y8eEKzNlYgTUEgfbORL4XxV4MVaJBHO)
- Dataset original: [Kaggle - Analyzing Credit Card Spending Habits in India](https://www.kaggle.com/datasets/thedevastator/analyzing-credit-card-spending-habits-in-india)

## Herramientas utilizadas

- Python 3, Scikit-learn, Ripser, UMAP, DBSCAN
- Jupyter Notebooks basados en materiales del profesor Alejandro Ucán (2025)

## Autor

Daniel Eduardo Arana Bodart  
Mayo 2025

---

> Este proyecto fue desarrollado como parte de un ejercicio académico para explorar aplicaciones reales del TDA en sistemas financieros.
