# Lectura 13

## Multi-armed recommender system bandit ensembles

En ente trabajo se hace relación a como la configuración de los conjuntos obtienen mejores resultados que por si solos, pero solo evaluados en sistemas de dominio acotado. Lo interesante de este trabajo es el hecho de realizar pruebas en ambientes más reales que sean capaces de representar el trabajo cíclico que realizan los sistemas.

Lo interesante que mencionan en este paper es el hecho de agregar valor al algoritmo de recomendación, que, aunque se han estudiado varios modelos, con buenos resultados, el desarrollo de un algoritmo hibrido tiene relevancia si es que agrega valor en la recomendación. 

El principal aporte de este trabajo es el análisis critico que existe en los trabajos presentados hasta el momento y la mejora que ellos proponen, que es en ámbito del testing del modelo. Ya que el proceso cíclico brinda la oportunidad para que los conjuntos prueben, observen y aprendan sobre la efectividad de los sistemas combinados, y mejoren la configuración del conjunto progresivamente, lanzando la configuración del conjunto como una tarea de aprendizaje por refuerzo.

Acá se adaptan dos algoritmos de bandidos básicos, muestreo de Thompson y ε-greedy, y se verifican que los enfoques resultantes son empíricamente más efectivos que las técnicas de conjuntos alternativas que carecen de la perspectiva a largo plazo en experimentos basados en conjuntos de datos fuera de línea.

Dentro de los trabajos relacionados, se menciona una aplicación que es las pruebas A / B, donde un método de bandidos decide automáticamente entre varios algoritmos en función de su interpretación anterior.

La selección del algoritmo a recomendar en cada paso se basa en su desempeño en los ciclos anteriores en los que se ha seleccionado. Por ejemplo, en ε-greedy, se selecciona con probabilidad 1 − ε, y con probabilidad ε, un algoritmo se selecciona de manera uniforme al azar independientemente de su efectividad histórica. Para el muestreo de Thompson, la parte posterior de la distribución de recompensa desconocida de cada brazo se modela como una distribución Beta (𝛼𝑎, 𝛽𝑎), donde 𝛼𝑎 y 𝛽𝑎 son el número de recomendaciones exitosas y no exitosas del algoritmo 𝑎, respectivamente. 

Para verificar el rendimiento de los conjuntos de recomendación de bandidos se ejecutan los algoritmos utilizando datos del conjunto de datos MovieLens 1M, que contiene 1.000.209 calificaciones de 6.040 usuarios a 3.706 películas. Binarizando las calificaciones mapeando los valores 1-3 a 0 y 4-5 a 1.

Dentro de los resultados obtenido de los algoritmos de filtrado colaborativo no pueden funcionar mejor que la recomendación por popularidad. Esto puede atribuirse a su vulnerabilidad a la escasez de datos inicial, mientras que la popularidad no personalizada obtiene una ventaja en las primeras iteraciones, cuando no hay suficientes datos para el filtrado colaborativo orientado a la explotación para producir recomendaciones personalizadas confiables.