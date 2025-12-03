# IA-NLP-ClasificacionSpam-
1.- Descripción General
El objetivo de este ejercicio es entrenar un modelo de clasificación de texto (NLP) capaz de identificar mensajes no deseados (spam). La variable objetivo es spam_label.



Deberás aplicar técnicas de procesamiento de lenguaje natural (NLP) y modelos de clasificación supervisada.



Este trabajo tiene un peso de 10 puntos sobre la nota final de la asignatura y debe ser individual y original.

El notebook que entregues debe ser tu propio trabajo, no una copia ni una modificación directa de notebooks ajenos.



Material de apoyo proporcionado
Para facilitar el inicio del trabajo, se entrega junto con este enunciado:

Notebook introductorio (SPAM_Intro_NLP.ipynb)
Contiene el flujo completo para cargar el texto desde los datasets y generar un archivo .csv de predicciones.
Sirve como punto de partida. Debes ampliarlo con tu propio pipeline, pruebas y análisis.
Dataset comprimido (Spam_Data.zip)
Incluye los conjuntos train, test y un ejemplo de submission.csv.
Debe descomprimirse en el mismo directorio que el notebook antes de ejecutar.


2.- Objetivo
Entrenar un modelo que, dada un texto, determine si corresponde a un mensaje SPAM (1) o NO SPAM (0).

El resultado del modelo debe presentarse en formato binario, almacenado en un archivo .csv de predicciones.



La métrica oficial es el Matthews Correlation Coefficient (MCC), definida como:



﻿M C C igual fracción numerador T P multiplicación en cruz T N menos F P multiplicación en cruz F N entre denominador raíz cuadrada de paréntesis izquierdo T P más F P paréntesis derecho paréntesis izquierdo T P más F N paréntesis derecho paréntesis izquierdo T N más F P paréntesis derecho paréntesis izquierdo T N más F N paréntesis derecho fin raíz fin fracción espacio﻿



Ejemplo en Python:

from sklearn.metrics import matthews_corrcoef
mcc = matthews_corrcoef(y_true, y_pred)
print(mcc)


3.- Formato de Salida
Tu archivo de entrega debe llamarse submission.csv y tener exactamente el siguiente formato:

row_id,spam_label
7097,0
7098,0
7099,0
8000,0
...
Donde:

row_id → identificador del texto en el conjunto de test.
spam_label → 0 para NO SPAM y 1 para SPAM.


4.- Evaluación
El trabajo se calificará sobre 10 puntos, atendiendo a los siguientes criterios:



               Criterio

  Descripción

  Ponderación

               Claridad y presentación

 Estructura, legibilidad y explicaciones del notebook

 25%

               Metodología

 Diseño de la CNN y aplicación del Transfer Learning

 35%

               Resultados y análisis

 Métricas, visualización y análisis de errores

 25%

               Conclusiones y referencias

 Reflexión sobre el proceso y fuentes utilizadas

 15%

              

Se valorará más la documentación, claridad y razonamiento que la mera puntuación obtenida en MCC
