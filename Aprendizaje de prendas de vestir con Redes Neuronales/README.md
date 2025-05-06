# Clasificación y Generación de Imágenes de Moda con CNN y GANs

Este proyecto explora el potencial del aprendizaje profundo aplicado al procesamiento de imágenes utilizando la base de datos **Fashion-MNIST**. Se desarrollaron dos enfoques complementarios: una **Red Neuronal Convolucional (CNN)** para clasificar prendas, y dos tipos de **Redes Generativas Antagónicas (GAN y DCGAN)** para generar imágenes sintéticas de ropa.

## Objetivo

- Clasificar imágenes de prendas de vestir mediante CNN.
- Generar nuevas imágenes realistas con GAN y DCGAN.
- Evaluar precisión, pérdida y calidad visual de los modelos.

## Dataset

- **Fuente:** Fashion-MNIST (70,000 imágenes en escala de grises, 28x28 px)
- **Categorías:** camiseta, pantalón, sudadera, vestido, abrigo, sandalia, camisa, tenis, bolsa, botín
- **Distribución:** 60,000 entrenamiento / 10,000 prueba

## Modelos Implementados

### Red Neuronal Convolucional (CNN)

- 3 capas convolucionales (32, 64, 128 filtros)
- MaxPooling, Dropout (25%-50%), Flatten, 2 capas densas (256 y 128 neuronas)
- Activaciones: ReLU en ocultas, Softmax en salida
- Optimización con Adam, función de pérdida `categorical_crossentropy`
- **Precisión final:**
  - Entrenamiento: 0.9299
  - Prueba: 0.9194

### Red Generativa Antagónica (GAN)

- **Generador:** capas densas con BatchNorm y LeakyReLU
- **Discriminador:** capas densas con Dropout y Sigmoid
- Entrenado por 40 épocas
- Imágenes generadas con formas generales de prendas
- **Resultado:** Imágenes borrosas pero con estructura reconocible

### Deep Convolutional GAN (DCGAN)

- **Generador:** 2 capas de convolución transpuesta con BatchNorm
- **Discriminador:** 2 capas convolucionales + Dense + Dropout
- Entrenado por 130 épocas
- **Resultado:** Imágenes más nítidas, siluetas de ropa más definidas
- **Tiempo de entrenamiento:**
  - GAN simple: ~31 minutos
  - DCGAN: ~87 minutos

## Resultados y Comparaciones

| Modelo     | Precisión/Realismo | Tiempo entrenamiento | Complejidad |
|------------|--------------------|----------------------|-------------|
| CNN        | 91.9%              | ~20 min              | Media       |
| GAN        | Bajo               | ~31 min              | Media       |
| DCGAN      | Alto               | ~87 min              | Alta        |

- CNN fue ideal para clasificación con buen balance de rendimiento y eficiencia.
- DCGAN mostró imágenes más realistas que GAN simple.
- GANs requieren más recursos y tiempo, pero son útiles para generación de datos sintéticos.

## Tecnologías

- Python 3.10, TensorFlow/Keras, Matplotlib, NumPy
- Entrenamiento en Google Colab con GPU


## Equipo

- Daniel Eduardo Arana Bodart  
- Isis Yaneth Malfavón Díaz  
- Alejandro Adriaensens Martínez  
- Karla Sofía Cantú Zendejas  

## Profesor

- Dr. Santiago Enrique Conant Pablos

## Curso

Diseño de Redes Neuronales y Aprendizaje Profundo  
Tecnológico de Monterrey 

Septiembre 2024

---

> Este proyecto demuestra cómo las redes convolucionales y generativas pueden aplicarse tanto al reconocimiento como a la creación de imágenes visuales, y destaca los retos computacionales y arquitectónicos del aprendizaje profundo.
