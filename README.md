# Análisis multimodal de Emociones en audio y texto

Este repositorio contiene el código fuente para entrenar y evaluar modelos de reconocimiento de emociones utilizando técnicas de Natural Language Processing (NLP) y espectrogramas de Mel generados a partir de audio. Se ha desarrollado una arquitectura híbrida que combinan CNNs preentrenadas (como VGG16 o EfficientNet) con características numéricas adicionales extraidas del entrenamiento de modelos Transformer (BERT o RoBERTa), con soporte tanto para tareas de clasificación simple (como MELD) como multietiqueta (como MOSEI).

## Estructura del repositorio

- `utils.py`: Script de Python auxiliar que contiene funciones de preprocesamiento, generación de espectrogramas, normalización de emociones y sentimientos, y limpieza de datasets.
- `implementacion.ipynb`: Notebook principal donde se entrena y evalúa la arquitectura híbrida, incluyendo comparaciones entre modelos de texto y audio, ajustes de hiperparámetros y visualización de resultados.

## Modelos creados

- `EmotionModel`: Modelo híbrido CNN + atención + features numéricas.
- `HybridTransformerClassifier`: Clasificador híbrido texto + features.
- Backbones disponibles para texto: `bert-base-uncased`, `bertweet-base-sentiment-analysis`, `roberta-base`, `twitter-roberta-base-sentiment` o `xlnet-base-cased`
- Backbones disponibles para audio: `vgg16` o `efficientnet_b0`.

## Dataset seleccionados

- `MELD`: Multimodal EmotionLines Dataset.
- `MOSEI`: CMU Multimodal Opinion Sentiment and Emotion Intensity dataset.

Los datos se pueden encontrar en Kaggle bajo los siguientes dataset:
- `MELD`: [link](https://www.kaggle.com/datasets/zaber666/meld-dataset)
- `MOSEI datasets`: [link](https://www.kaggle.com/datasets/gnurtqh/cmu-mosei)
- `MOSEI audios`: [link](https://www.kaggle.com/datasets/maunberg/cmu-mosei)
- `Espectrogramas`: [link](https://www.kaggle.com/datasets/mariaisabelglezschez/spectrograms)

## Ejecución

1. Carpa el código contenido en `utils.py` importándolo como librería en `Implementacion.ipynb`.
2. Ejecuta los experimentos con `Implementacion.ipynb`.

## ⚙️ Requisitos

- Python ≥ 3.8
- PyTorch ≥ 1.12
- GPU, targeta gráfica

En caso de no tener targeta gráfica o una de poca potencia, el código original proviene de Kaggle y se puede usar sus GPUs por 30h/semana.



