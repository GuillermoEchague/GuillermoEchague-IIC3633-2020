# Lectura 15#

## Deep learning based recommender system: A survey and new perspectives

Este trabajo, lo interesantes es como los sistemas recomendadores han facilitado la experiencia de usuario en diversos ámbitos como compras, elección de películas, navegación web, etc. En general, estos sistemas han desempeñado un papel vital e indispensable en varios sistemas de acceso a la información para impulsar el negocio y facilitar el proceso de toma de decisiones y están generalizados en numerosos dominios web, como el comercio electrónico y los sitios web de medios. En este sentido han aparecido las redes neuronales y en especial Deep Learning para la obtención de modelos de Sistemas Recomendadores basados en aprendizaje profundo. Acá, además se proporciona un resumen completo del estado de la técnica. También, intenta ampliar en las tendencias actuales y brindar nuevas perspectivas relacionadas con este nuevo y emocionante desarrollo del campo.

Los sistemas de recomendación estiman la preferencia de los usuarios sobre los elementos y recomiendan elementos que a los usuarios les pueden gustar de forma proactiva. Los modelos de recomendación se clasifican principalmente en filtrado colaborativo haciendo recomendaciones al aprender de las interacciones históricas del usuario y el elemento, sistema de recomendación basado en contenido basada principalmente en comparaciones entre elementos y la información auxiliar de los usuarios y sistema de recomendación híbrido basado en los tipos de datos de entrada. Recientemente, el aprendizaje profundo ha revolucionado dramáticamente las arquitecturas de recomendación y brinda más oportunidades para mejorar el rendimiento del recomendador. El aprendizaje profundo es capaz de capturar de manera efectiva las relaciones no lineales y no triviales entre el usuario y el elemento, y permite la codificación de abstracciones más complejas como representaciones de datos en las capas superiores. Además, captura las intrincadas relaciones dentro de los datos en sí, a partir de abundantes fuentes de datos accesibles, como información contextual, textual y visual.

El éxito del aprendizaje profundo para la recomendación tanto en el ámbito académico como en la industria requiere una revisión y un resumen completos para que los investigadores y profesionales sucesivos comprendan mejor las fortalezas y debilidades, y los escenarios de aplicación de estos modelos.
En el estado del arte de este trabajo se mencionan varios estudios en sistemas de recomendación tradicionales. Sin embargo, hay una falta de revisión exhaustiva sobre el sistema de recomendación basado en el aprendizaje profundo que en este trabajo buscan desarrollar.

El aprendizaje profundo se puede considerar generalmente como un subcampo del aprendizaje automático. La esencia definitoria típica del aprendizaje profundo es que aprende representaciones profundas, es decir, aprende múltiples niveles de representaciones y abstracciones a partir de datos.

En este trabajo se explican un conjunto diverso de paradigmas arquitectónicos que están estrechamente relacionados con el estudio de este trabajo son: El perceptrón multicapa (MLP), Autoencoder (AE), La red neuronal convolucional (CNN), Red neuronal recurrente (RNN), La máquina de Boltzmann restringida (RBM), La estimación de distribución autoregresiva neuronal (NADE), Adversarial Networks (AN), Aprendizaje por refuerzo profundo (DRL) 
Las fortalezas de los modelos de recomendación basados en el aprendizaje profundo son: Transformación no lineal, Aprendizaje de representación, Modelado de secuencia y Flexibilidad. 

Pero dentro de sus limitaciones esta la Interpretabilidad al comportase como cajas negras, y proporcionar predicciones explicables parece ser una tarea realmente desafiante. Requisito de datos, ya que el aprendizaje profundo consume mucha información y un amplio ajuste de hiperparámetros. Aunque en este trabajo no es explicito, uno de los principales obstáculos que presentan estos modelos son que necesitan una gran capacidad de cálculo, esta es una especie de letra chica para estos modelos.

En el estado del arte de Deep Learning en sistemas recomendadores se discuten los desafíos y los problemas abiertos, e identifican las nuevas tendencias y direcciones futuras en este campo de investigación.

En esta sección, primero se presentan las categorías de modelos de recomendación basados en el aprendizaje profundo y luego destacan los prototipos de investigación de vanguardia, con el objetivo de identificar el avance más notable y prometedor de los últimos años.
Recomendación con bloques de construcción neuronales, los modelos se dividen en ocho subcategorías de conformidad con los ocho modelos de aprendizaje profundo antes mencionados: MLP, AE, CNNs, RNNs, RBM, NADE, AM, AN y sistema de recomendación basado en DRL. 

Recomendación con modelos Deep Hybrid, utilizan más de una técnica de aprendizaje profundo. La flexibilidad de las redes neuronales profundas hace posible combinar varios bloques de construcción neuronales para complementarse entre sí y formar un modelo híbrido más poderoso.

MLP es una red concisa pero eficaz que ha demostrado ser capaz de aproximar cualquier función medible a cualquier grado deseado de precisión. Como tal, es la base de numerosos enfoques avanzados y se usa ampliamente en muchas áreas.
Extensión neuronal de los métodos de recomendación tradicionales. Muchos modelos de recomendación existentes son esencialmente métodos lineales. MLP se puede utilizar para agregar transformación no lineal a enfoques RS existentes e interpretarlos en extensiones neuronales.

Casi todas las variantes del codificador automático, como el codificador automático de eliminación de ruido, el codificador automático variacional, el codificador automático de contacto y el codificador automático marginalizado se pueden aplicar a la tarea de recomendación.

Las redes neuronales de convolución son poderosas para procesar datos multimedia no estructurados con operaciones de convolución y agrupación. La mayoría de los modelos de recomendación basados en CNN utilizan CNN para la extracción de características.

