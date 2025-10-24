# CFE-IA-E10

# Clasificación de Opiniones

## El objetivo de este proyecto es entrenar un modelo de Procesamiento de Lenguaje Natural (PLN) capaz de predecir la opinión binaria (1 = positiva, 0 = negativa) de cada registro, utilizando como entrada el contenido textual presente en la columna declaración.

# Datos

## Datasets utilizados:

## dataset_train.csv: conjunto de entrenamiento con las columnas declaracion y etiqueta (objetivo).

## dataset_test_sin_etiqueta.csv: conjunto de prueba sin etiquetas, utilizado para generar las predicciones finales.

# Variable objetivo:

## etiqueta: valor binario que indica la opinión del texto (1 = positiva, 0 = negativa).

# El conjunto de entrenamiento se dividió en 90% para entrenamiento y 10% para prueba, garantizando una evaluación representativa del modelo.

# Pasos realizados
# 1. Carga y limpieza de datos

## Se cargaron los archivos CSV con pandas.

## Se verificaron valores nulos y no se encontraron datos faltantes.

## Se eliminaron las filas duplicadas para evitar sesgos durante el entrenamiento.

# 2. División del dataset

## Se utilizó train_test_split para separar los datos en conjuntos de entrenamiento y prueba (90% / 10%).

# 3. Vectorización del texto

## Se aplicó CountVectorizer, una técnica de representación que convierte el texto en una matriz de frecuencias de palabras.

## Este paso permite que el modelo trabaje con datos numéricos derivados del lenguaje natural.

# 4. Entrenamiento del modelo

## Se entrenó un modelo de Regresión Logística (LogisticRegression) utilizando las declaraciones vectorizadas como entrada y las etiquetas como salida.

## El modelo fue evaluado en el conjunto de prueba utilizando la métrica accuracy (precisión).

# 5. Evaluación

## La métrica Accuracy mide el porcentaje de predicciones correctas realizadas por el modelo.

## Se obtuvo un resultado satisfactorio, mostrando un buen rendimiento en la clasificación binaria de opiniones.

# 6. Generación de archivo de entrega

## Se cargó el archivo dataset_test_sin_etiqueta.csv.

## Se aplicó el modelo entrenado para predecir la columna etiqueta.

## Se generó el archivo final dataset_test.csv, que incluye las columnas:

## id: identificador del registro.

## etiqueta: valor predicho (1 o 0).

# Resultado final

## El modelo de Regresión Logística demostró ser eficaz para la tarea de clasificación binaria de opiniones. COn un resultado promedio de 99.96% en el modelo
