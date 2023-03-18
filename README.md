# Analisis Discriminante
Ejercicio académico de análisis discriminante realizado para la Maestría en Ciencias con mención en Estadística Aplicada de la Universidad Nacional de Trujillo.

Para este ejercicio se utilizará la base de datos "Iris", que contiene información sobre 150 flores de iris de tres especies diferentes: Iris setosa, Iris versicolor e Iris virginica. Cada flor se mide en cuatro variables: longitud y ancho del sépalo y longitud y ancho del pétalo, medidas en centímetros.

Esta base de datos fue recopilada por el biólogo británico Ronald Fisher en 1936 para ilustrar la técnica de análisis discriminante. Desde entonces, se ha utilizado como una base de datos de prueba para muchos métodos estadísticos y de aprendizaje automático, como análisis discriminante, regresión logística,  análisis de componentes principales, clustering y redes neuronales.

La base de datos iris es muy útil en la enseñanza de técnicas de clasificación y agrupamiento, ya que se pueden separar fácilmente  las tres especies de iris en  función de las mediciones de las cuatro variables. Además, es una base de datos pequeña pero representativa que es fácil de entender y visualizar, lo que la hace útil para la enseñanza y la divulgación de la ciencia de datos.

# Explicación del código
# iris.lda <- lda(Species ~ ., data = iris)"

Este código ajusta un modelo de análisis discriminante lineal (LDA) a los datos de la base de datos "iris" en R.

La sintaxis "Species ~ ." especifica que la variable "Species" será la variable dependiente o la variable que se intentará predecir a partir de las otras variables independientes incluidas en la base de datos "iris". El "." representa todas las demás variables en la base de datos, en este caso las cuatro variables de medición de las flores de iris (longitud y ancho del sépalo y del pétalo).

El modelo LDA busca maximizar la separación entre las clases de flores de iris (setosa, versicolor y virginica) utilizando una combinación lineal de las variables de medición. Una vez ajustado el modelo, se puede usar para clasificar nuevas observaciones en las tres clases de flores de iris en función de sus mediciones de las cuatro variables de medición.

El resultado del ajuste del modelo se almacena en el objeto "iris.lda" que puede ser utilizado para hacer predicciones de clasificación o para realizar  otras operaciones y análisis. En resumen, este código ajusta un modelo LDA para la clasificación de las especies de flores de iris en función de las mediciones de las cuatro variables de medición en la base de datos "iris".

# iris.lda$scaling

Esta linea hace referencia a una operación que se puede realizar después de ajustar un modelo de análisis discriminante lineal (LDA, por sus siglas en inglés). Específicamente, el código "iris.lda$scaling" extrae los coeficientes de discriminante lineal, también conocidos como vectores de pesos, para cada variable en el modelo de LDA ajustado. Estos coeficientes representan la contribución de cada variable a la discriminación entre las diferentes categorías de la variable dependiente.

En otras palabras, después de ajustar el modelo de LDA en la base de datos "iris", el comando "iris.lda$scaling" permite examinar la importancia relativa de cada variable independiente en la separación de las tres especies de iris que se están clasificando en este modelo. Por lo tanto, la salida de este comando proporciona información sobre cómo se está discriminando cada especie basándose en los valores de las variables independientes.

# table(iris$Species, iris.pred$class)

Esta linea de código se utiliza para generar una matriz de confusión a partir de los resultados de una predicción de clasificación en la base de datos "iris".

En este código, "iris$Species" es el vector que contiene la variable de especies verdaderas en la base de datos "iris", mientras que "iris.pred$class" es el vector que contiene las especies predichas por un modelo de clasificación, que previamente se ha ajustado a los datos de "iris". Al aplicar la función "table()" a estos dos vectores, se crea una matriz que resume los resultados de la predicción y permite analizar la precisión del modelo.

La matriz de confusión muestra los resultados de la clasificación en términos de los verdaderos positivos (TP), verdaderos negativos (TN), falsos positivos (FP) y falsos negativos (FN) para cada categoría de la variable dependiente. 

Específicamente, en la matriz de confusión, las filas representan las categorías verdaderas (o reales) de la variable dependiente y las columnas representan las categorías predichas.

En el caso del código "table(iris$Species, iris.pred$class)", las filas representan las tres especies de iris (setosa, versicolor y virginica) y las columnas representan las especies que el modelo predijo para cada una de ellas.

Cada celda de la matriz de confusión contiene el número de observaciones que se clasificaron en una categoría específica, de acuerdo con la clasificación verdadera y la clasificación predicha. Por ejemplo, el valor en la celda (1,1) corresponde al número de observaciones que fueron verdaderas positivas para la especie setosa, es decir, el número de observaciones que se clasificaron correctamente como setosa por el modelo.

# Matriz de confusión

La matriz de confusión es una herramienta útil para evaluar la precisión de un modelo de clasificación y para identificar qué categorías son más difíciles de clasificar correctamente. También se pueden calcular medidas de evaluación del modelo, como la precisión, la sensibilidad y la especificidad, a partir de la matriz de confusión.

