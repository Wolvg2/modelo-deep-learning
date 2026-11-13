# Detección de tumores cerebrales en resonancias magnéticas con Deep Learning

Los tumores cerebrales son una de las enfermedades neurológicas más graves: su diagnóstico temprano influye directamente en las opciones de tratamiento y en el pronóstico del paciente. La resonancia magnética (MRI) es la técnica de imagen más utilizada para detectarlos, ya que ofrece un alto contraste entre tejidos blandos sin emplear radiación ionizante.

Sin embargo, la interpretación de estas imágenes depende de radiólogos especializados; es un proceso que consume tiempo y puede verse afectado por la fatiga o por la variabilidad entre especialistas. Además, en muchas regiones el número de especialistas es limitado frente a la demanda de estudios.

En este proyecto se plantea un problema de **clasificación binaria de imágenes**: dada una resonancia magnética cerebral, determinar si presenta un tumor o no. Para resolverlo se emplean **redes neuronales convolucionales (CNN)** implementadas con Keras y TensorFlow, comparando un modelo diseñado desde cero con un modelo basado en *transfer learning*.

El objetivo no es sustituir el diagnóstico médico, sino explorar cómo un modelo de este tipo podría funcionar como **herramienta de apoyo**: priorizar estudios sospechosos, servir como segunda opinión o agilizar la revisión de grandes volúmenes de imágenes. Por ello, además de la exactitud general, se da especial importancia al *recall* de la clase tumor, ya que un tumor no detectado es el error más costoso en este contexto.

Se utilizará el dataset público de Kaggle *"Brian Tumor Dataset"* (autor: Preet Viradiya), que contiene 4,600 imágenes de resonancia magnética (MRI) cerebral divididas en dos clases: **tumor** (2,513 imágenes) y **normal/sano** (2,087 imágenes). El objetivo es entrenar un clasificador binario capaz de distinguir entre ambos casos.

Las imágenes tienen tamaños y formatos heterogéneos (JPEG, PNG y TIFF; en RGB y escala de grises), por lo que fue necesario un preprocesamiento para uniformizarlas.

**Fuente:** [Brian Tumor Dataset – Kaggle](https://www.kaggle.com/datasets/preetviradiya/brian-tumor-dataset)
