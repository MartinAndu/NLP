
---
👤 Autor
```
Martín Andújar
CEIA — 2025
```

Este repositorio reúne la resolución completa de los Desafíos 1, 2, 3 y 4 de la materia, conformando un
recorrido progresivo por distintas etapas del aprendizaje profundo aplicado.

El trabajo comienza con el preprocesamiento y análisis exploratorio de datos (Desafío 1), continúa con la
construcción de modelos basales y primeros enfoques supervisados (Desafío 2) y avanza hacia la experimentación
con arquitecturas más complejas como redes neuronales profundas (Desafío 3).

Finalmente, el Desafío 4 desarrolla un modelo de traducción automática basado en la arquitectura seq2seq
encoder–decoder utilizando TensorFlow/Keras. Este modelo incluye tokenización bilingüe, generación de secuencias
con `<sos>` y `<eos>`, entrenamiento sobre miles de pares de oraciones, experimentos variando la cantidad de
neuronas internas (`latent_dim`) y la implementación de distintas estrategias de decodificación
(greedy, sampling, top-k y beam search). Además, se incorpora una variante opcional con embeddings
pre-entrenados (GloVe).

En conjunto, estos trabajos cubren el pipeline completo de aprendizaje profundo: preparación de datos, modelos
base, redes avanzadas y la aplicación de técnicas modernas de **Procesamiento de Lenguaje Natural (NLP)** para
resolver un problema real de traducción automática.


# Desafío 1 — Preprocesamiento y análisis exploratorio

En este desafío se trabaja con:

- Limpieza y normalización de datos.
- Análisis exploratorio detallado.
- Visualizaciones descriptivas.
- Preparación del dataset para tareas de modelado posteriores.

El objetivo es establecer un pipeline de preprocesamiento claro y reproducible.

---

# Desafío 2 — Modelos clásicos / Baselines supervisados

Incluye:

- División del dataset en subconjuntos de entrenamiento y validación.
- Entrenamiento de modelos base (según la consigna de la materia).
- Evaluación con métricas relevantes.
- Identificación de overfitting / underfitting.
- Primeros ajustes de hiperparámetros.

Este desafío establece un punto de referencia para modelos más complejos.

---

# Desafío 3 — Modelos avanzados (CNN / RNN )

Este desafío incorpora arquitecturas más expresivas:

- Redes neuronales profundas.
- Experimentación con capas, activaciones y regularización.
- Análisis de curvas de entrenamiento.
- Comparación entre configuraciones y discusión de resultados.

El objetivo es profundizar la comprensión de arquitecturas modernas y su comportamiento.

---

# Desafío 4 — Traductor Seq2Seq (TensorFlow / Keras)

El cuarto desafío implementa un modelo **encoder–decoder con LSTM** para traducir texto de **inglés → español**, extendiendo el ejemplo provisto en la Clase 6.

### Componentes principales

- Preprocesamiento del dataset Anki / ManyThings.
- Tokenización independiente por idioma.
- Construcción de secuencias con `<sos>` y `<eos>`.
- Arquitectura seq2seq estándar:
    - **Encoder:** Embedding + LSTM
    - **Decoder:** Embedding + LSTM + Dense(softmax)
- Entrenamiento con secuencias de longitud configurable.
- Evaluación cualitativa mediante 5+ ejemplos reales.
- Implementación de múltiples estrategias de decodificación:
    - Greedy decoding
    - Sampling con temperatura
    - Top-k sampling
    - Beam search
- Experimentos sistemáticos variando el tamaño del estado interno (`latent_dim`).
- Celda opcional para integrar **embeddings GloVe pre-entrenados**.

### Objetivos alcanzados

- Reproducir y **extender** el traductor original de la Clase 6.
- Analizar empíricamente cómo influye la capacidad del modelo.
- Explorar estrategias de inferencia y sus efectos en la calidad de traducción.
- Sentar las bases para introducción de mecanismos de atención.

---

# Requisitos

**Python:** 3.9+  
**Dependencias principales:**

- tensorflow / keras
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- tqdm

Los notebooks están pensados para ejecutarse fácilmente en **Google Colab** sin configuraciones adicionales.

---

# ▶Cómo ejecutar

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/usuario/repositorio.git
   cd repositorio
    ```
2. Abrir cualquier notebook en Jupyter o Colab.

3. Ejecutar las celdas en orden.

4. Para el Desafío 4, asegurarse de ejecutar primero la celda que descarga el dataset `spa-eng`.   
