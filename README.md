# SentimentAnalysis
Sentiment Analysis
Grupo NPL 7
Franz Josef Haidacher Avila
Victor Ernesto De Leon Müller
Jaime Miguel García González
Curso TEXT MINING & NATURAL LANGUAGE PROCESSING - SECCIÓN - 10 -2022 -1
UVG

INSTRUCCIONES:

1. Utilizar Jupiter Notebook.
2. Debe cargarse el archivo .csv con nombre puerto_escondido_hotels.csv a su directorio raiz de jupiter. El archivo .csv se adjunto en el directorio de github.
3. Favor seguir los comentarios y las conclusiones en el documento con nombre Tarea 3_Grupo 7_Final.ipynb

Variaciones de hiperparámetros realizadas:

Se utilizarón dos algoritmos de clasificación y se realizarón cambios de hiperparámetros únicamente en la función CountVectorizer.

* Modelo 1, Regresión logística, Countvectorizer: min_df=5; max_df=0.5;ngram_range=(1,3);strip_accents=unicode;lowercase=True;stop_words=english

* Modelo 2, Regresión logística, Countvectorizer: se vario de min_df=5 a min_df=10

* Modelo 3, Regresión logística, Countvectorizer: se agregó el feature max_features=2000 y se devolvió el min_df=5

* Modelo 4, Regresión logística, Countvectorizer: se removió el feature max_features=2000 y se agregó el token_pattern ='(?<!\S)[A-Za-z]+(?!\S)|(?<!\S)[A-Za-z]+(?=:(?!\S))'

Para los modelos 5 al 8, se realizó  la misma secuencia de cambios en la función Countvectorizer, pero con el algoritomo BernoulliNB()

Se probó el hiperparámetro tokenizer=LemmaTokenizer() , pero este ocasionó que no pudieramos ejecutar otros hiperparámetros, por ejemplo el de stop_words. Por lo que optamos, no incluirlo. 

Conclusiones de la Tarea:

El mejor modelo que vemos desde las predicciones de las frases, es el de BernoulliNB; con parámetro min_df igual a 10 en la función Countvectorizer.

En las frases propuestas se consideraron 3 con sentido negativo y 2 con sentido positivo validadas en la función predict solamente el modelo 6 (nb2), cumplió con exactitud las expectativas de predicción.
