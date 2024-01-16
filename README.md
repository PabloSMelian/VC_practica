# Detección y aviso de peligros en cruces de visibilidad reducida

## Argumentación del trabajo:

El profesor de la asignatura comentó en clase que en la ciudad de Las Palmas de Gran Canaria hay algunos cruces con visibilidad reducida que pueden llegar a ser peligrosos para todos los usuarios de la vía. Como uno de nosotros se había percatado de ese mismo problema a la hora de hacer las prácticas de conducir, decidimos que queríamos abordarlo para proponer una medida que podría aumentar la seguridad en este tipo de intersecciones, informando de los posibles peligros que se encuentran al otro lado del giro, donde normalmente es difícil obtener una buena visibilidad.

## Objetivo de la propuesta:

Nuestro objetivo es que las intersecciones de visibilidad reducida sean más seguras para todos los usuarios de la vía. Esto se consigue informando de tanto vehículos como peatones e incluso animales que puedan haber al otro lado de la intersección.

## Descripción técnica del trabajo realizado:

Nuestro trabajo consiste en colocar cámaras en estas intersecciones o curvas de visibilidad reducida acompañadas de una pantalla en el otro lado de la intersección. Las imágenes recopiladas por la cámara serán tratadas por YoloV8 en tiempo real y la información detectada será procesada y mostrada por la pantalla.

Para la cumplimentación de estos requisitos nos hemos basado en el trabajo de la práctica 5, donde hemos podido aprovechar el entrenamiento para YoloV8 que se nos proporcionaba ya que tenía todas las clases que necesitábamos. Una vez tenemos la imagen lo que hacemos es ir guardando las coincidencias según su confianza, filtrando las que no nos interesan y las que no tienen confianza suficiente. A continuación añadimos una prioridad customizable para cada obstáculo (la prioridad utilizada fue: camión, guagua, coche, moto, bicicleta, persona, paraguas, caballo, perro, gato, pájaro). También se tiene en cuenta la confianza para establecer dicha prioridad.

Una vez detectados los obstáculos se muestra un texto donde indica el obstáculo de mayor prioridad. Este texto cambia el color; más rojo indica más certeza en la detección. Además, se muestra una imagen de dicho obstáculo en pantalla, dándole al usuario más información.

A fin de facilitar la lectura de estos datos (nombre del obstáculo e imagen) la actualización de los mismos es interrumpida, al solo escoger una muestra de cada 10. Si se actualizara de forma constante, sería más complicado de leer.

## Fuentes:
Éstas son las fuentes que hemos usado para el desarrollo de nuestro trabajo de curso. Nos basamos mayoritariamente en prácticas anteriores, sobre todo la práctica 5, teniendo alguna inspiración de otras prácticas como la 6 o la 3. El vídeo que usamos que contiene gran variedad de vehículos y personas lo encontramos en el guión de la práctica 5. Resolvimos muchas dudas gracias a algunas consultas con ChatGPT y búsquedas en google, en páginas como www.geeksforgeeks.org, www.cherryservers.com, www.programiz.com, docs.opencv.org y docs.ultralytics.com. Finalmente, usamos Dall-E 3 para crear una de las imágenes de la portada. 

## Tecnologías utilizadas:
Las tecnologías en las que nos hemos apoyado son: python, opencv, yolo de ultralytics, Visual Studio Code, Anaconda navigator y Discord (para reunirnos).

## Conclusión:
En resumen, hemos creado una herramienta software basada en YoloV8 que puede ayudar a aumentar la seguridad en zonas potencialmente peligrosas de la carretera.

## Propuestas de mejora:
En nuestro proyecto, cuando mostramos el obstáculo más peligroso, se ven las cajas contenedoras de las clases detectadas; creemos que, como posible mejora, se podrían eliminar. Otra mejora que se podría añadir sería entender la dirección en la que se dirige cada objeto y su velocidad, dando lugar a posibles cálculos para entender mejor cuán peligroso es el obstáculo. Como último retoque, se podrían cambiar los umbrales para satisfacer mejor los objetivos del proyecto y entrenar el modelo para que tenga mayor precisión.

## Herramientas/tecnologías con las que nos hubiera gustado contar:
Vídeo completo con todas las clases desde diferentes ángulos. Poder hacer un vídeo propio con todas las clases de forma artificial nos dejaría poder probar todo tipo de casos y poder corregir fácilmente los errores que pudiéramos ver. 

## Créditos materiales no originales del grupo:
Nos hemos apoyado en diversos materiales que no han sido desarrollados exclusivamente por el grupo, el guión del trabajo de curso de VC, un vídeo de cruce y paso de peatón y una imagen generada por Dall-E 3 para la portada del trabajo.
