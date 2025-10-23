
Robocup2026 – Avance Clasificación de Objetos con Visión Artificial
Datos utilizados

Se trabajó con tres clases de objetos seleccionadas por las limitaciones mecánicas de la garra robótica de Colombia. Los objetos fueron elegidos por su tamaño.
Las clases utilizadas son:

Tuna

Sponge

Golf Ball

Cada categoría contó con aproximadamente 60 imágenes iniciales, obtenidas de fuentes abiertas.

Procesamiento de imágenes

Se implementó un script en Python para procesar automáticamente los conjuntos de imágenes.
El código realiza los siguientes pasos:

Descomprime los archivos .zip de cada clase.

Convierte todas las imágenes al formato .png.

Rota las imágenes en ángulos de 90°, 180°, 270° y 360°, generando nuevas vistas.

Organiza las imágenes procesadas en cuatro carpetas separadas según su ángulo.

Comprime los resultados nuevamente dentro de una carpeta general por clase.

Este procedimiento permitió ampliar la cantidad de muestras disponibles para el entrenamiento y mejorar la variabilidad del conjunto de datos.
Algunas imágenes no fueron utilizadas debido a problemas de resolución o redundancia visual.

Creación del dataset

Una vez procesadas las imágenes, se cargaron al entorno de Roboflow. Se clasificaron cada imagen con su respectiva clase, la cual llevaba el nombre de  los objetos
Se generaron tres carpetas correspondientes a las tres clases seleccionadas, con el siguiente conteo final:

Clase	Imágenes cargadas
Tuna	238
Golf Ball	240
Sponge	254

Total general: 732 imágenes.

Se creó la versión V2 del dataset, que fue dividida automáticamente por Roboflow en:

Training set: 513 imágenes

Validation set: 146 imágenes

Testing set: 73 imágenes

Generación del código y vinculación con el repositorio

En Roboflow se generó automáticamente el fragmento de código en Python para la descarga del dataset en formato YOLOv8, el cual ya fue incorporado dentro del repositorio de GitHub.


Este script permite acceder directamente al conjunto de datos desde un entorno de Python, asegurando la trazabilidad del dataset con Roboflow.

Estado actual del entrenamiento


Enlace al proyecto en Roboflow: https://app.roboflow.com/andesrobot/robocup2026-y7rar/annotate
