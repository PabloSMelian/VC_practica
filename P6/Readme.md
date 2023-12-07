# VC Práctica 6
## Introducción
Para esta práctica hemos propuesto 2 partes. En la primera parte usamos la webcam para detectar caras. Una vez detectada al menos 1 cara, analizamos la primera cara que encontramos y mostramos la edad del individuo, la raza, el género (masculino o femenino) y la emoción primaria detectadas. Mostramos esta información en tiempo real en una ventana arriba a la izquierda.

## Entrega 
### Carga de los componentes 
Importamos los componentes necesarios para poder ejecutar el programa. 
### Funcionamiento
Añadimos la ventana al video que captura la webcam en tiempo real, y analizamos con DeepFace las caras que aparecen en el frame actual. Recogemos la información de la primera cara, y la añadimos en la ventana, actualizando los valores que nos devuelve en cada iteración del bucle. 
### Segunda parte: Análisis de caras en un archivo de vídeo
Esta parte tiene un funcionamiento similar al anterior, pero utiliza un video anteriormente grabado. Por tanto, la carga de los componentes y el funcionamiento son muy parecidos. Aquí se ve un ejemplo de su funcionamiento: 

## Preguntas
### Tras la ejecución, para todas las variantes se muestran métricas y matriz de confusión. ¿Qué esquema consideras que es mejor?
Dado el dataset que hemos utilizado, se puede observar que el esquema que clasifica con componentes PCA como características con SVM es el que da mejores resultados, obteniendo un 92% para las mujeres y un 86% en los hombres. Este esquema funciona correctamente un 89% de las veces, haciéndolo bastante fiable.
