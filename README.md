# Credit-Scoring-con-python
Predicción del riesgo crediticio con  Machine Learning en Python


En este proyecto, utilizaremos un conjunto de datos de aprendizaje automático desequilibrado, denominado conjunto de datos " German Credit " o simplemente " German"

El conjunto de datos de crédito alemán describe los detalles financieros y bancarios de los clientes y la tarea es determinar si el cliente es bueno o malo. El supuesto es que la tarea implica predecir si un cliente devolverá un préstamo o no.

Hay dos clases, 1 para buenos clientes y 0 para malos clientes. Los buenos clientes son la clase predeterminada o negativa, mientras que los malos clientes son la excepción o la clase positiva. Un total del 70 % de los ejemplos son buenos clientes, mientras que el 30 % restante de los ejemplos son malos clientes.

Buenos Clientes : Clase negativa o mayoritaria (70%).
Malos Clientes : Clase positiva o minoritaria (30%).

Se espera que un modelo predictivo elaborado a partir de estos datos sirva de guía al gerente del banco para tomar una decisión sobre la aprobación de un préstamo a un posible solicitante en función de su perfil.

Fuente de la data:
El conjunto de datos contiene 1000 filas con 10 variables .En este conjunto de datos, cada entrada representa a un cliente que recibe un crédito de un banco. Cada cliente se clasifica con riesgo crediticio bueno o malo según el conjunto de variables. El enlace al conjunto de datos original se puede encontrar a continuación.
https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data)
https://www.kaggle.com/uciml/german-credit



Variables:

1.	Edad (numérica)
2.	Sexo (texto: masculino, femenino)
3.	Trabajo (numérico: 0 - no calificado y no residente, 1 - no calificado y residente, 2 - calificado, 3 - altamente calificado)
4.	Vivienda (texto: propia, alquilada o gratuita)
5.	Cuenta de ahorros (texto: pequeño, moderado, bastante rico, rico)
6.	Cuenta corriente (numérica, en DM - Deutsch Mark)
7.	Monto del crédito (numérico, en DM)
8.	Duración (numérica, en meses)
9.	Propósito (texto: automóvil, muebles / equipo, radio / TV, electrodomésticos, reparaciones, educación, negocios, vacaciones / otros)
10.	Risk: indica si el cliente cumplirá con el pago o no (Bueno , Malo)


Objetivo: Encontrar el mejor modelo que clasifique los préstamos potenciales de clientes, como riesgo malo o riesgo bueno.

Qué se aplicará para lograr el objetivo?

•	Pre-procesamiento de Datos.

•	Análisis Exploratorio de Datos.

•	Ingeniería de características.

o	Dumificación de variables (convertir características categóricas a numéricas).

o	Escalamiento de variables.

•	Manejar datos desequilibrados:

    La variable dependiente Default está desequilibrada, por lo que se aplicará técnicas de sampling para solucionar este problema.
    
  o	SMOTE 
  
  o	SMOTE-TomeLinks
  
  o	Random Oversampling
  
  o	ADASYN
  
  
  •	Para cada técnica de sampling de datos desequilibrados, se desarrollará 5 modelos de clasificación de aprendizaje  supervisado, para predecir si un préstamo es un riesgo         bueno o malo:

  o	Logistic Regression

  o	Support vector Machine

  o	Random Forest 

  o	Gradient Boosting Classifier

  o	AdaBoost Classifier
  
  
  Para cada técnica de sampling de datos desequilibrados, se  seleccionará los 2 mejores modelos basados en su recall.

  Realizar Tunning/Ajuste de hiperpárametros de los 2 mejores modelos seleccionados, con las mejores técnicas para datos desequilibrados.
  
  
  
Hallazgo principal:


Después de aplicar los 5 modelos, con las 4 distintas técnicas de sampling (Oversampling, SMOTE, SMOTE-TOMELINK y ADASYN) para datos desequilibrados y modelos Baseline, se procedió a seleccionar los 2 modelos con el mayor rendimiento (Recall). Los 2 modelos seleccionados fueron, Support Vector Machine (SVM) y Logistic Regression, ya que como se muestra en el cuadro tienen los 2 recall más altos. El recall para Support Vector Machine es de 0.83, mientras que el recall para Logistic Regression es de 0.78, 0.75 y 0.73 respectivamente, para las técnicas SMOTE-Tome Links, ADASYN y SMOTE.

Al realizar el ajuste/Tunning de hiperparámetros con las técnicas SMOTE-Tome Links, ADASYN y SMOTE, y los modelos SVM y Logistic Rgression se encontró que el mejor modelo era SVM con SMOTE-TomeLinks.





  
  




















