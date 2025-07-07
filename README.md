Objetivo del trabajo: 
El objetivo es crear un sistema para la identificación automática de armas (como pistolas, cuchillos, rifles o granadas) utilizando técnicas de procesamiento de imágenes y aprendizaje automático. Aunque la idea general contempla la integración en sistemas de videovigilancia, en este proyecto en particular solo se trabajó con imágenes estáticas debido a la disponibilidad y facilidad de anotación de datos.

Nombre de los alumnos participantes: 
Francesca Nicole Bances Torres
Marcos Aaron Bedia Torres
Lizbeth Teresita Olivera Alvarez

Breve descripción del dataset:
El dataset a utilizar es “Test Computer Vision Project”, disponible en la plataforma Roboflow. Este conjunto de datos fue diseñado para proyectos de visión por computadora, específicamente la detección de armas como granadas, rifles, pistolas y cuchillos. 
Dataset: Test Computer Vision Project
Origen: Roboflow Universe
Cantidad total de imágenes: 4666
Cantidad de imágenes por clase: 
Grenade: 1413
Rifle: 1226
Pistol: 1010
Knife: 845

Conclusiones: 
- El desarrollo y entrenamiento de modelos de detección de armas mediante visión por computadora demuestra ser una solución efectiva y viable para mejorar los sistemas de seguridad en diversos escenarios.
- La precisión y fiabilidad del sistema dependen en gran medida de la calidad y cantidad de los datos utilizados en el entrenamiento, destacando la importancia de contar con un conjunto de datos representativo y bien anotado.
- La implementación de modelos como YOLOv 8s permite una detección en tiempo real, contribuyendo significativamente a la prevención y respuesta rápida ante situaciones de riesgo en ámbitos de seguridad pública y vigilancia.
- La comparación entre las versiones Nano y Small de los modelos YOLO permitió identificar que YOLOv8s ofrece el mejor equilibrio entre precisión, velocidad y eficiencia, cumpliendo con los requerimientos del sistema propuesto. Aunque modelos como YOLOv8n destacan por su rapidez y bajo consumo de recursos, su menor precisión representa un riesgo en contextos sensibles como la detección de armas. Por lo tanto, YOLOv8s fue seleccionado como el modelo más adecuado, garantizando una detección confiable y en tiempo real en dispositivos con capacidad moderada.
- YOLOv8s demostró ser el modelo más adecuado para el contexto del problema, dado que obtuvo el mayor Recall (0.72473), métrica prioritaria en tareas de detección de armas. Esto significa que tiene mayor capacidad para detectar armas reales, minimizando los falsos negativos, los cuales representan un riesgo significativo para la seguridad.
- En las imágenes comparativas, se observó que YOLOv8s realiza detecciones más precisas y con mayor confianza, aunque aún presenta algunos falsos positivos. Sin embargo, estos son aceptables dentro del contexto del problema, ya que pueden corregirse manualmente sin comprometer la seguridad.Por lo tanto, YOLOv8s se posiciona como el modelo más confiable y efectivo para la tarea de detección de armas, considerando tanto el análisis cuantitativo de métricas como la evaluación cualitativa de las predicciones.
