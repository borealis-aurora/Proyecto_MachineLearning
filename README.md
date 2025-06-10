# Proyecto Final 💻 - Segmentación de Imágenes de Leucocitos mediante SegFormer 
```
Universidad de Guanajuato - Campus León, División de Ciencias e Ingenierías
Elaborado por: Aurora Pinzón Arzola, a.pinzonarzola@ugto.mx
Programa educativo: Licenciatura en Física
Curso: Temas Selectos de Física (Aprendizaje Automático)
Profesor: Dr. Luis Carlos Padierna García
Ciclo escolar: Enero - Junio 2025
```
🟥 **Introducción**

🩸 Los glóbulos blancos o leucocitos forman parte del sistema inmune y participan en las respuestas inmunitarias innatas del cuerpo y en la producción de anticuerpos. Circulan por la sangre y organizan respuestas inflamatorias y celulares ante lesiones o agentes patógenos.

La visión computacional es un campo de la Inteligencia Artificial basada en el aprendizaje profundo y las Redes Neuronales Convolucionales (CNN), ambas pertenecientes a Machine Learning, y cuyo uso ha aumentado en el campo de la salud debido a la gran cantidad de ventajas y buenos resultados reportados en la literatura.

En este proyecto se presenta la aplicación de visión computacional através del uso de la segmentación semántica de imágenes de leucocitos mediante SegFormer, una poderosa arquitectura que unifica Transformers con decoders compuestos por perceptrón multicapa (MLP), con el propósito de contribuir a la automatización del Conteo Diferencial de Leucocitos.

🟧 **Objetivo**

* Implementar SegFormer para presentar un enfoque alternativo a la recreación de la tesis “ESTUDIO E IMPLEMENTACIÓN DE TÉCNICAS DE VISIÓN COMPUTACIONAL BASADAS EN APRENDIZAJE PROFUNDO PARA EL CONTEO DIFERENCIAL Y SEGMENTACIÓN DE LEUCOCITOS EN IMÁGENES DE ASPIRADO DE MÉDULA ÓSEA”, del licenciado Ángel Daniel Canales Ramírez.
* Presentar el proyecto y sus resultados utilizando un formato poco convencional, por ejemplo, a través de un repositorio de GitHub, una página Web, visión aumentada, etc. 

🟨 **Justificación**

La implementación de tecnologías de visión computacional en el área de la salud ha sido de gran relevancia al facilitar y agilizar la detección, clasificación y observación de elementos en imágenes médicas. Es por ello por lo que, se considera importante poder estudiar y aprender estas tecnologías ya que han demostrado un potencial para automatizar y estandarizar el análisis de imágenes médicas.

🟩 **Marco Teórico**

Los leucocitos son un tipo de célula sanguínea producida en la médula ósea, y se encuentran en la sangre (representando aproximadamente 1% de nuestra sangre) y el tejido linfático (amígdalas, el timo, el bazo y la médula ósea). Los glóbulos blancos forman parte del sistema inmune y participan en las respuestas inmunitarias innatas y producción de anticuerpos.

El conteo diferencial de leucocitos es una prueba que se realiza para determinar la proporción de diferentes tipos de leucocitos, mediante la clasificación de al menos 100 leucocitos consecutivos en neutrófilos, neutrófilos en banda, linfocitos, monocitos, eosinófilos y basófilos, mediante un frotis de sangre preparado y teñido. Para poder realizar este conteo es necesario, obtener una muestra de sangre, obtener un frotis y realizar la tinción y preparación adecuada para llevar a cabo el conteo. 

Es por lo anterior que, con el propósito de contribuir a la automatización del Conteo Diferencial de Leucocitos, se plantea implementar visión computacional para facilitar y automatizar la identificación de leucocitos. 

Los Transformers se introdujeron en 2020 con el artículo “Attention Is All You Need”. Son un tipo de modelo de aprendizaje profundo que utilizan el mecanismo de atención para aumentar la velocidad de procesamiento y mejorar el rendimiento en tareas que implican datos secuenciales. Dos componentes importantes de esta arquitectura son: 
* Mecanismo de Atención: es posible procesar múltiples partes de una secuencia de entrada simultáneamente al procesar cada parte individual, al calcular el attention score que captura la relación contextual entre cada palabra y el resto de la oración.
* 	Problema de Descenso de Gradiente (Backpropagation): problema común en redes neuronales, como RNN, en el que los gradientes se vuelven muy pequeños y los pesos de la red no se actualizan correctamente, llevando a un mal entrenamiento y rendimiento. 
 
Los Transfomers están constituídos por un encoder y un decoder. 

➡️ *ENCODER*:
Procesa la secuencia de entrada. Consiste de varias capas apiladas conformadas por subcapas: multi-head self-attention mechanism and the fully connected feed-forward network.
* Multi-head self-attention mechanism: procesa la secuencia de entrada al determinar la relevancia o “atencións” que se le debe de asignar a diferentes partes del texto.
* Feed-forward network: aplica una transformación a la secuencia procesada por el mecanismo de atención.
  
➡️ *DECODER*:  
Genera la secuencia de salida basada en la información del encoder, con la restricción de únicamente utilizar salidas conocidas (masked self-attention). 

 **Segformer**

Para este proyecto, se utilizó el SegFormer, una arquitectura que unifica un codificador jerárquico Transformer con un decodificador ligero de perceptrón multicapa (MLP). Su diseño destaca por dos características principales:
*	Codificador Transformer jerárquico: Genera características multiescala a diferentes resoluciones, capturando tanto detalles finos como gruesos de la imagen. A diferencia de los transformadores tradicionales, SegFormer no utiliza codificaciones posicionales explícitas, lo que lo hace resistente a las variaciones de resolución de imagen entre el entrenamiento y la inferencia.
*	Decodificador ligero basado en MLP: SegFormer utiliza un decodificador sencillo basado en MLP. Este decodificador fusiona características de diferentes capas del codificador, combinando el contexto local y global para producir máscaras de segmentación precisas de manera eficiente.

> ``📝`` **NOTA:** Mayor información sobre el proyecto se puede encontrar en el video, la presentación y los códigos adjuntos en este repositorio. 

[![VIDEO:](https://img.youtube.com/vi/FNfDsF6lk5Q/maxresdefault.jpg)](https://youtu.be/FNfDsF6lk5Q)


