# Lectura 2

## Post original FunkSVD

Esta lectura corresponde a un blog, escrito por Simon, donde describe su proceso para obtener un Sistema recomendador SVN para el concurso de netflix prize, en el cual obtuvo el tercer lugar. El realiza una descripción de lo que consiste este concurso, que intenta realizar recomendaciones, solo sabiendo los títulos de las películas, y algunos gustos de usuarios. Para este concurso Netflix proporcionó 100 millones de calificaciones (de 1 a 5) de 17 mil películas por 500 mil usuarios. Estos llegan esencialmente en forma de un triplete de números: (Usuario, Película, Calificación). Esta matriz tendría aproximadamente 8.500 millones de entradas (número de usuarios multiplicado por el número de películas). Además, solo tiene valores para 1 de cada 85 de las celdas. El resto está en blanco.

El blog se centra en como poder encontrar un SVD que permita predecir la calificación de una recomendación de un usuario con información desconocida. Para este desafío el autor se enfoca en poder dar una solución por medio de modelos matemáticos que sean capaces de representar el proceso descrito anteriormente.

Simon, para la obtención de los modelos asume que la calificación de un usuario de una película se compone de una suma de preferencias sobre los diversos aspectos de esa película. 

Lo que recalca el autor es que la obtención de una solución, es un proceso iterativo, donde cada supuesto es valioso, hasta que es refutado por otro.

Lo interesante de este artículo, es que el autor cuenta la experiencia en primera persona dentro de un concurso, en el cual existe un premio millonario e intenta por medio de modelos matemáticos y las limitaciones computacionales en ese momento para el desarrollo de un SVN con un gran volumen de datos. Aun así, lograr llegar a una solución que cumpla los parámetros y juegos que el concurso lo somete. Simon, describe gran parte del proceso como cualquier persona podría reflexionar y realizar suposiciones a la hora de enfrentar este desafío.

Lo que no tengo muy claro, de este blog es que el autor, hace hincapié en desarrollos por medio de modelos y suposiciones estadísticas y no hace mucha relación a posibles publicaciones que puedan ayudar a probar otras metodologías, pero eso se puede deber a que tal vez no exista un gran desarrollo de estos temas como lo es en el presente.
