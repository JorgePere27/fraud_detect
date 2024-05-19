
# Financial Fraud Detector
![image](https://github.com/JorgePere27/fraud_detect/assets/104606154/ff81f926-f96d-44b8-9b0f-e66b4b3a60b3)


La urgencia por detectar fraudes en transacciones móviles de dinero ha llevado a una empresa del segmento Fintech a buscar soluciones innovadoras. Como científicos de datos hemos sido convocados para desarrollar un modelo de machine learning que pueda distinguir de manera precisa entre transacciones legítimas y fraudulentas, estableciendo así un estándar de seguridad en el sector financiero móvil global.

PaySim simula transacciones de dinero móvil basadas en una muestra de transacciones reales extraídas de un mes de registros financieros de un servicio de dinero móvil implementado en un país africano. Los registros originales fueron proporcionados por una empresa multinacional, que es el proveedor del servicio financiero móvil que actualmente opera en más de 14 países en todo el mundo.

Este conjunto de datos sintéticos se ha reducido a 1/4 del conjunto de datos original y se ha creado exclusivamente para Kaggle.

El dataset a utilizar tiene los siguientes datos.

* step - Indica una unitdad de tiempo en el mundo real. En este caso 1 step es 1 hora de tiempo. Total de steps 744 (simulación de 31 dias).
* type - El tipo de transacción ya sea CASH-IN, CASH-OUT, DEBIT, PAYMENT o TRANSFER.
* amount - Cantidad de la transacción.
* nameOrig - Cliente que empieza la transacción.
* oldbalanceOrg - Saldo inicial antes de la transacción.
* newbalanceOrg - Saldo nuevo después de la transacción.
* nameDest - Cliente que recibe la transacción.
* oldbalanceDest - Saldo inicial del receptor antes de la transacción.
* newbalanceDest - Saldo nuevo del receptor después de la transacción.
* isFraud - Indica si la transacción realizada es fraudulenta.
* isFlaggedFraud - El modelo de negocio tiene como objetivo controlar transferencias masivas de una cuenta a otra y marcar los intentos ilegales. Un intento ilegal en este conjunto de datos es un intento de transferir más de 200.000 en una sola transacción.



Las principales taras son las siguientes:

1. Preprocesamiento de Datos: Realizar limpieza de datos, manejar valores faltantes, codificación de variables categóricas y normalización/escalado de datos.

2. Exploración de Datos: Analizar y comprender el conjunto de datos proporcionado, identificar variables llaves y realizar visualizaciones para entender las relaciones entre las variables y seleccionar las características relevantes.

3. Construcción de Modelos: Experimentar con algunos algoritmos de machine learning como Regresión Logística, Árboles de Decisión, Random Forest, Naive Bayes, entre otros.

4. Evaluación y Selección del Modelo: Evaluar los modelos utilizando métricas como precisión, recall, área bajo la curva ROC, y F1-score. Seleccionar el modelo con el mejor rendimiento para la detección de transacciones bancarias fraudulentas.


## Conclusiones

Después del entrenamiento y prueba de todos los modelos, observamos que en la métrica de recall, que es la más relevante para nosotros en este caso porque mide la proporción de verdaderos positivos entre los ejemplos que realmente son positivos, los resultados son prácticamente los mismos tanto para Random Forest como para el árbol de decisión.

Por lo tanto, podemos concluir que elegir cualquiera de estos dos modelos nos dará resultados similares. Sin embargo, si tuviéramos que escoger uno, optaríamos por Random Forest, ya que presenta una mayor precisión (accuracy).



## Screenshots

La mayor parte de las transacciones se encuentra en el umbral de los 200,000 por lo que las transacciones mayores a este valor tienen que ser revisadas con mayor atención ya que podrian estar realacionadas con transacciones ilegales. 

![image](https://github.com/JorgePere27/fraud_detect/assets/104606154/28f0330d-d990-4de3-a7aa-dbeaadd83aea)



Se observa un desbalance agresivo en la columna target, dentro del notebook se encuentra la solución al problema.
![image](https://github.com/JorgePere27/fraud_detect/assets/104606154/04ceed00-037f-4126-be97-6d05fb1555bf)



Resultado de las métricas de los modelos entrenados y evaluados.
![image](https://github.com/JorgePere27/fraud_detect/assets/104606154/986c79bd-9a3a-473e-ad34-b3df61ebe876)



## Skills

* Python
* Seaborn
* Sklearn
* Pandas
* EDA (Exploratory Data Analysis)
* Data pre-processing
* Statistical Analysis
* Machine Learning
* Model creation


## Acknowledgements

Este proyecto fue realizado como parte del Data science Bootcamp Experience mismo que está basado en el proyecto de investigación ”Scalable resource-efficient systems for big data analytics” realizado por Knowledge Foundation (grant: 20140032) in Sweden que se encuentra en la plataforma de kaggle.

https://www.kaggle.com/datasets/ealaxi/paysim1

Referencia al dataset:
E. A. Lopez-Rojas , A. Elmir, and S. Axelsson. "PaySim: A financial mobile money simulator for fraud detection". In: The 28th European Modeling and Simulation Symposium-EMSS, Larnaca, Cyprus. 2016
## Authors

- Esteban Ferraz [@estebanferraz1](https://github.com/estebanferraz1)
- Jorge Perez [@JorgePere27](https://www.github.com/JorgePere27)
- Jhonatan Rodriguez[@JhonatanRC03](https://github.com/JhonatanRC03)


## Contributing

Contributions are always welcome!



