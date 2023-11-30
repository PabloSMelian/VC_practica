# VC Práctica 5
## Introducción
En esta práctica desarrollamos un modelo que detecta matrículas de coches españolas y lee la matrícula en cuestión. Para esta práctica usamos YOLO_v8 para detectar las matrículas y usamos easyocr para leer la mátricula una vez detectada.  
## Creación del dataset
Para la creación del dataset pensamos en usar un dataset hecho por nosotros, pero al ver las diversas opciones que ofrecía Roboflow, nos decantamos por él. Estuvimos viendo varios datasets que ofrecía la página, pero solían ser coches con mátriculas internacionales o europeas no españolas. Después de varias búsquedas encontramos un dataset con suficientes imágenes y con matrículas españolas. 
## Entrenamiento de YOLO_v8
Una vez obtenido el dataset, empezamos con el entrenamiento del modelo. Primero intentamos entrenarlo en nuestro portátil como se describía en el guión de la práctica. Sin embargo, nos encontramos con varios problemas:
* No pudimos entrenar usando la GPU de nuestro portátil debido a que es muy antigua.
* Entrenando con la CPU nos tardaba más de 40 minutos, que nos parece una cantidad demasiado grande de tiempo.

Para resolver esto, decidimos usar Google Collab. Gracias a Google Collab pudimos entrenar nuestro modelo usando las GPUs que nos ofrece Google en la nube, que nos da unos tiempos de entrenamientos deseados.

## Recorte de la imagen
Una vez que comprobamos que nuestro modelo detectaba las matrículas, pasamos al recorte de la imagen. Crremos que podríamos recortar la imagen de una forma más precisa, pero no encontramos una manera adecuada de hacerlo. Nuestro recorte es bastante generoso para no pasarnos recortando, asegurando que la matrícula esté en la imagen. 

## Lector OCR
Finalmente, toca leer la matrícula. Para esta sección decidimos usar EasyOCR, que nos pareció fácil de implementar y bastante cómodo. Tuvimos en cuenta que las matrículas solo podían contener números y letras mayúsculas. 

## Incidencias
Nuestro modelo tiene algunos problemas cuando la matrícula tiene algun tipo de oclusión, está parcialmente tapada (aunque sea una cantidad muy baja) o si tiene una calidad baja.
