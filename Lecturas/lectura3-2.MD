# Lectura 6

## Evaluating recommendation systems

Un sistema de recomendación calcula y proporciona contenido relevante al usuario basado en el conocimiento del usuario, el contenido y las interacciones entre el usuario y el artículo. Por lo que se pueden presentar varias preguntas en este tema, tales como:

¿Por qué implementar un recomendador?, ¿Qué querías ganar?, ¿Quieres ganar más?, ¿Tienes más visitantes?, ¿Probar nueva tecnología? No importa lo que se responda, es posible que no se traduzca directamente en una forma de calcular si está mejorando o no. A menudo se oye hablar de algoritmos que son mejores o ligeramente mejorados en comparación con los algoritmos de vanguardia actuales, pero ¿qué mejoran? y ¿cómo?

El acuerdo general entre los investigadores de sistemas de recomendación es que es casi imposible evaluar un sistema o algoritmo de recomendación sin tener un sistema en vivo para probarlo. Aun así, es importante saber si su sistema de recomendación va en la dirección correcta.


¿Por qué es importante evaluar?, ¿Su sistema de recomendación funciona correctamente? Después de haber, sudado y sangrado para hacer que un sistema de recomendación funcione, no se quiere que falle. A menudo, probar un sistema de recomendación es una búsqueda para encontrar pruebas de que funciona. También se espera no encontrar señales de que podría no funcionar perfectamente o de que devuelva resultados inesperados a más de la mitad de los usuarios. Sin duda, sería bueno saber que esto iba a suceder antes de que lo hicieran todos los usuarios.


**Tipos de evaluación**

Se tiene varias formas de probar un algoritmo de recomendación. No todos darán una visión precisa de cómo funcionará el algoritmo, si es que se agrega a un sitio web, por ejemplo.
La triste verdad es que la única forma real de saberlo es poner uno en acción en el sitio. Pero antes de hacer eso, puede facilitar la transición haciendo otras evaluaciones. Asumiendo que ya tiene un conjunto de datos que contiene calificaciones. Para hacer una evaluación verdadera, se necesita lo que se llama un conjunto completo de verdad fundamental, que es un conjunto de datos que contiene información sobre todas las combinaciones de usuarios y contenido. Sin embargo, si tiene eso, es posible que no necesite un sistema de recomendación porque el usuario ya sabe exactamente cómo se siente con respecto a todos los elementos. Si no se tiene ese conjunto, se debe asumir que las combinaciones de usuario-elemento presentes en los datos son verdaderas y representativas de todos los usuarios.
Se pueden realizar pruebas en tres tipos de escenarios: experimentos Offline, experimentos de user studies y experimentos online. Los investigadores del sistema de recomendación hablan de que los experimentos Offline no funcionan y que los user studies y en online son demasiado costosos, pero a veces es difícil hacer felices a todos. Sean McNee y sus colegas investigadores de GroupLens8 señalan que el enfoque en mejorar la precisión de los sistemas de recomendación ha sido erróneo e incluso perjudicial. Cada experimento (Evaluación Offline, user studies y online) tiene un propósito. Solo necesita seleccionar el adecuado para el trabajo.

**Evaluación Offline**

La idea de la evaluación Offline es utilizar datos que se consideren veraces. Luego, se dividen los datos en dos partes y enviar una parte al recomendante. Utilizando la otra parte para verificar que el recomendante predice calificaciones sobre los elementos del conjunto que estaban ocultos para él; aquellos que están cerca de las calificaciones reales o aquellos que producen recomendaciones que contienen elementos que fueron altamente calificados en datos ocultos. O puede decir que los usuarios consumieron artículos que calificaron incluso si no les gustaban, por lo que los artículos aún cuentan para algo.


**Evaluación Online** 

Una vez que se está satisfecho de que un algoritmo de recomendación está funcionando, es hora de implementar el sistema y probarlo en humanos reales. Pero se puede hacer por etapas.
Primero, se recomienda hacer experimentos controlados. Luego, cuando la retroalimentación sea buena, se continúa con las pruebas con usuarios aleatorios en su sistema.


Antes de implementar el recomendador, Un proverbio interesante en este punto es: la lámpara solo arderá tan bien como el aceite que le eches, así que aquí hay algunos pasos a considerar:

* Verificar el algoritmo
* Verificar los datos
* Haz una prueba de regresión


**Cobertura**
La diversidad conduce muy bien a la cobertura porque cuanto mejor es la diversidad, mejor es la cobertura.
Una de las principales razones para implementar un sistema de recomendación es permitir a los usuarios navegar por el catálogo completo, lo que se conoce como cobertura de contenido. La cobertura se refiere tanto a garantizar que el algoritmo recomendará todo en su catálogo como a si puede recomendar algo a todos los usuarios registrados, lo que se denomina cobertura de usuario.
La forma de fuerza bruta de calcular la cobertura de usuarios es iterar sobre todos los usuarios, llamar al algoritmo de recomendación y luego ver si devuelve algo.