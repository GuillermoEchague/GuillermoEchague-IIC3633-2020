# Lectura 4

## BPR: Bayesian personalized ranking from implicit feedback


Acá se busca obtener un sistema recomendador de predicción a un ranking personalizado en un conjunto de ítem, utilizando recomendaciones implícitas, el foco de este trabajo es la recomendación de Ítem. Estos sistemas son utilizados en sitios web de ventas como Amazon o un portal de videos como Youtube. La tarea de recomendación de ítem es creado para el ranking de un usuario específico para un conjunto de ítems. Dentro de los trabajos relacionados, el modelo más popular es el k-Vecinos cercanos (KNN) de filtros colaborativos y Descomposición de valores singulares (SVD). En este paper se investigan escenarios donde el ranking es inferido del comportamiento implicito de los usuarios, tomando solo observaciones positivas.

El paper busca poder atacar el problema del feedback implícito, el cual deja data sin analizar ya que solo observa o considera las clases positivas. Por esta razón se utiliza Machine Learning para poder realizar el entrenamiento, principalmente porque estos métodos no discriminan los datos y son estrategias para prevenir el overfitting, como regularización. Para lo anterior se presenta un criterio de optimización genérico y un algoritmo de aprendizaje para la clasificación personalizada

Acá se utiliza un enfoque diferente mediante el uso de pares de elementos como datos de entrenamiento y se optimiza para clasificar correctamente los pares de elementos en lugar de puntuar elementos individuales, ya que esto representa mejor el problema que simplemente reemplazar los valores faltantes con valores negativos. 

El criterio de optimización BPR-Opt es el estimador posterior máximo que se deriva de un análisis bayesiano del problema

Para los modelos de aprendizaje con respecto a BPR-Opt, se utiliza el algoritmo de aprendizaje genérico LearnBPR que se basa en el descenso de gradiente estocástico. Este método genérico se puede aplicar a los dos modelos de recomendación de última generación de factorización matricial y kNN adaptativo.

De manera empírica, los autores del paper demuestran que, para la tarea de ranking personalizado, los modelos aprendidos por BPR superan a los mismos modelos que están optimizados con respecto a otros criterios. Además la calidad de la predicción no solo depende del modelo, sino también en gran medida del criterio de optimización.
