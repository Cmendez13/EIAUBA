# Trabajo Práctico 1

´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´

En primer lugar pone de manifiesto la importancia de los hiperparámetros **path_size** y **embedding_dimensión**. 

Su configuración debe considerar el **trade off** entre costo computacional y el nivel de flexibilidad para capturar características locales y/o globales.

Path_size muy  grandes puede perder de vista características locales pero con un costo computacional bajo (debido a que generaria menor cantidad de bloques a procesar)

embedding_dimensión grandes puede brinda mayor flexibilidad para aprender patrones complejos (con mayor costo computacional) 


´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´´

Por otra parte, se busco resaltar el uso de los embeddings posicionales aprendidos como una forma de dotar a la implementación de mayor flexibilidad (para afrontar relaciones entre los parches no lineales o muy complejas). Sin embargo al ser modelos aprendidos puede sobre ajustar en modelos con pocos datos .
