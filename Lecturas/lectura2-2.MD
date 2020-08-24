# Lectura 4

## BPR: Bayesian personalized ranking from implicit feedback

Acá se busca obtener un sistema recomendador de predicción a un ranking personalizado en un conjunto de ítem, utilizando recomendaciones implícitas, el foco de este trabajo es la recomendación de Ítem. Estos sistemas son utilizados en sitios web de ventas como Amazon o un portal de videos como Youtube. La tarea de recomendación de ítem es creado para el ranking de un usuario específico para un conjunto de ítems. Dentro de los trabajos relacionados, el modelo más popular es el k-Vecinos cercanos (KNN) de filtros colaborativos y Descomposición de valores singulares (SVD). En este paper se investigan escenarios donde el ranking es inferido del comportamiento implicito de los usuarios, tomando solo observaciones positivas.

El paper busca poder atacar el problema del feedback implícito, el cual deja data sin analizar ya que solo observa o considera las clases positivas. Por esta razón se utiliza Machine Learning para poder realizar el entrenamiento, principalmente porque estos métodos no discriminan los datos y son estrategias para prevenir el overfitting, como regularización.

