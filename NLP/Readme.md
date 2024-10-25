

![NLP](images/PNL.jpg)


Este repositorio fue pensado para contener las experiencias de aprendizajes durante el curso de **Procesamiento del Lenguaje Natural** de la Especialización en Inteligencia Artificial de la UBA, dependiente de la Facultad de Ingeniería.

<h2> Descripción del curso </h2>

## Introducción a NLP y Vectorización de Documentos
- Fundamentos del Procesamiento del Lenguaje Natural.
- Técnicas de vectorización: Bag of Words (BoW) y TF-IDF.

## Pre-procesamiento de Texto y Word Embeddings
- Limpieza y normalización de texto.
- Introducción a word embeddings: Word2Vec, GloVe y FastText.

## Modelos No-BOW I: Convolucionales y Recurrentes
- Modelos alternativos a BoW para relaciones en secuencias.
- Redes neuronales convolucionales (CNNs) y recurrentes (RNNs), LSTMs y GRUs.
- Generación de texto secuencial.

## Modelos No-BOW II: Mecanismo de Atención
- Introducción al mecanismo de atención en modelos secuenciales.
- Aplicaciones de atención en PLN.

## Modelos Seq2seq
- Arquitectura encoder-decoder para tareas de secuencias a secuencias.
- Aplicaciones: traducción automática, chatbots y resumen de texto.

## Transformers
- Arquitectura de Transformers y modelo de atención completa.
- Modelos como BERT y GPT y su impacto en PLN.

## Grandes Modelos de Lenguaje y RAG
- Introducción a grandes modelos de lenguaje (LLMs).
- Modelos de recuperación-augmented generation (RAG) para mejorar respuestas en diálogos.

## Miscelaneos
- Generación automática de descripciones de imágenes (Image Captioning).
- Reconocimiento automático del habla (ASR).
- Síntesis de texto a voz (TTS).


<h2> Desafios </h2>

<h3> Desafio 1 </h3>

Para este desafío, se llevó a cabo un análisis de similaridad de documentos con el conjunto de datos 20 Newsgroups:

**Vectorización y Similaridad:** 

Se utilizaron métodos TF-IDF para vectorizar los documentos y se midió la similaridad de coseno entre un documento seleccionado y los 5 más similares.
Modelos de ML: Se entrenaron modelos de Naive Bayes (Multinomial y ComplementNB) para clasificar documentos, optimizando hiperparámetros mediante búsqueda aleatoria para maximizar el f1-score macro en el conjunto de prueba.

**Similaridad de Palabras:** 

Se seleccionaron 5 palabras y se analizaron sus palabras más similares utilizando el mismo enfoque de vectorización.

**Modelo:** Se entrenaron modelos de Naive Bayes (Multinomial y ComplementNB) para clasificar documentos con ajustes de hiperparámetros.


<h3> Desafio 2 </h3>
Para este desafío, se utilizó una muestra de reseñas del conjunto de datos IMDB reviews para entrenar un modelo Word2Vec y analizar la similaridad entre palabras en el contexto:

**Tokenización y Entrenamiento de Word2Vec:** 
Se tokenizaron las reseñas y se entrenó un modelo Word2Vec con Gensim.
**Análisis de Similaridad:** 
Se analizaron palabras seleccionadas y se identificaron las más cercanas en el espacio vectorial de Word2Vec.

**Visualización de Embeddings:** Se visualizaron los embeddings en 2D.

![desafio2](https://github.com/Cmendez13/EIAUBA/blob/main/NLP/images/desafio_2_similaritud.png))

<h3> Desafio 3 </h3>

En este desafío, se utilizó una muestra del archivo **74376.txt** para entrenar un modelo LSTM para la generación de texto:

**Prepocesamiento de datos:** 
Se cargaron los datos del archivo **txt**, segmentando el texto en palabras. Se utilizó un Tokenizer para convertir palabras en índices numéricos, se dividió el conjunto en entrenamiento y validación.

**Modelo LSTM:** 
Se definió y entrenó un modelo LSTM secuencial en Keras:

![Modelo Desafio 3](https://github.com/Cmendez13/EIAUBA/blob/main/NLP/images/Modelo_deasafio_3.png)

<h3> Desafio 4 </h3>

Para este desafío, se entrenó un bot de preguntas y respuestas (QA) utilizando un conjunto de datos de conversaciones y una arquitectura encoder-decoder con LSTM y embeddings preentrenados de FastText. 
Para ello:

**Carga y Preparación de Datos:** Se cargaron diálogos del archivo data_volunteers.json, limpiando y tokenizando las oraciones, y añadiendo los tokens <sos> y <eos>.

**Tokenización y Padding:** Se utilizó el Tokenizer de Keras para crear diccionarios (word2idx_inputs y word2idx_outputs) y se aplicó padding para unificar las longitudes

**Embeddings:** Se emplearon embeddings preentrenados de FastText(*) para inicializar la capa de embeddings del modelo.

**Entrenamiento del Modelo LSTM:** Se entrenaron dos modelos, siendo el primero una arquitectura simple encoder-decoder con LSTM de 128 unidades en ambas partes, conectados a una capa de embeddings 

(*) Los archivos de embeddings hubo que cargarlos directamente desde Kaggle para facilitar su uso.

<h3> Desafio 5 </h3>

Resumen del Desafio de Clasificación de Sentimientos con BERT

Se trabajó en la clasificación de reseñas de Google Apps para predecir el sentimiento utilizando un modelo basado en BERT:

**Tokenización y División de Datos:** 

Después de limpiar y balancear el conjunto de datos, se tokenizaron las críticas con el tokenizador de BERT y su división en entrenamiento y validación.

Se definión un módelo personalizado que permitiera modificar max_length y se le agrego una capa densa adicional

Se probaron: 

![max_legth_100](https://github.com/Cmendez13/EIAUBA/blob/main/NLP/images/model_5_100.png)

**max_length = 100**

![max_legth_140](https://github.com/Cmendez13/EIAUBA/blob/main/NLP/images/model_5_140.png)

**max_length = 140**




