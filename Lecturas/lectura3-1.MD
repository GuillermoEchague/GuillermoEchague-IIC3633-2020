# Lectura 5

## Performance of recommender algorithms on top-n recommendation tasks

La mayoría de los sistemas de recomendación se basan en el filtrado colaborativo (FC), independientemente de conocimiento del dominio. Hay dos enfoques principales para la FC:

* El enfoque de vecindad. 
* El enfoque de factor latente.

**Enfoque de vecindad**

Una vecindad es simplemente el conjunto de elementos que son similares al contenido que se está viendo actualmente. Esto es llamado vecindad porque hablamos de elementos con una pequeña distancia entre ellos. Para definir y calcular dicho este vecindario se utiliza el método Top-N.

Los algoritmos centrados en la similitud artículo-artículo calculan la preferencia del usuario por un artículo basándose en sus propias calificaciones sobre artículos similares.

ya que generalmente funciona mejor en términos de RMSE, mientras que es más escalable. Ambas ventajas están relacionadas con el hecho de que el número de elementos suele ser menor que el número de usuarios. Otra ventaja de los algoritmos artículo-artículo es que el razonamiento detrás de una recomendación a un usuario específico puede explicarse en términos de los artículos previamente calificados por los usuarios.

El enfoque Top-N puede obligar al sistema a usar puntos diferentes al punto activo, lo que lo convierte en un mal recomendante. Para garantizar una mejor calidad, debe adoptar otro enfoque, como el método del umbral.

El método Top-N se desempeña mejor para la cantidad.

En un conjunto de datos utópico, todos los elementos se distribuirán por igual en toda el área, N será fácil de seleccionar. Pero eso no sucede a menudo, y se trata de equilibrar qué tan buenas deben ser las recomendaciones para las personas que les gustan las cosas populares y qué tan buenas deben ser las recomendaciones para las personas con gustos peculiares.

Si bien la mayor parte de la literatura se centra en métricas de error convenientes (RMSE, MAE), estos criterios de error clásicos no miden realmente el rendimiento de top-N. A lo sumo, pueden servir como representantes de la verdadera experiencia top-N. La evaluación directa del desempeño de top-N debe lograrse mediante metodologías alternativas basadas en métricas de precisión (por ejemplo, recuperación y precisión).

**El enfoque de factor latente**

Recientemente se han propuesto varios algoritmos de recomendación basados en modelos de factores latentes. La mayoría de ellos se basan en la factorización de la matriz de calificaciones de los elementos del usuario, también conocidos informalmente como modelos SVD después de la descomposición de valores singulares relacionada.

Dos formas de hacer recomendaciones ahora son calcular todas las calificaciones previstas y tomar las más grandes que el usuario no haya visto antes, o recorrer cada elemento y encontrar productos similares en el espacio reducido. Una tercera forma podría ser usar las nuevas matrices que tiene para calcular el filtrado colaborativo de vecindario. La razón por la que podría ser una buena idea es que las matrices tienen todas las entradas distintas de cero (al menos si está normalizado). En este espacio denso, tiene muchas más posibilidades de encontrar elementos o usuarios similares.

Para finalizar, algo interesante de este trabajo es que los autores realizan pruebas para no sesgar las metricas de precisión.