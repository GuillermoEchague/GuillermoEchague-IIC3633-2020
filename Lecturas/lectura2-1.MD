# Lectura 3

## Collaborative filtering for implicit feedback datasets

En el desarrollo de este trabajo se realiza un sistema recomendador, pero a diferencia de los primeros paper, como Item-based Collaborative Filtering Recommendation Algorithms, acá se busca generar recomendaciones que sean realizadas de forma personalizada, muy parecido a un traje a la medida, pero intentando encontrar por medio de un feedback de intereses pero considerando que un usuario puede entregar información no solo de gusto, por ejemplo la compra de un regalo, ver un programa en específico para poder dormir en la noche, etc. También lograr información explicita con lo que el usuario no le gusta. Como trabajo previo se basa en modelo relacionados a la vecindad que utilizan el coeficiente de correlación de Person para modelar valores. Para este trabajo se plantea un modelo para un feedback implícito, el cual utiliza variables binarias 0 o 1, indicando las preferencias de un usuario a un ítem, asignado 1 si le gusta y 0 si es que no hay preferencia. Estos valores pueden representar las preferencias de forma indirecta de los usuarios.

A diferencia de él paper mencionado anteriormente, para la realización de la parte experimental del método se utiliza data desde un servicio de televisión digital, obteniendo sobre 300.000 set top box. Toda la data fue obtenida con los gustos de los usuarios finales,


