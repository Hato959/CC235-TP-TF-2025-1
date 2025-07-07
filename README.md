[yolo_detection_readme.md](https://github.com/user-attachments/files/21095277/yolo_detection_readme.md)
Detección de Objetos con YOLO: Modelos Small, Nano y YOLOv12

Se evaluaron los modelos en base a:
[Uploading yolo_detection_read# Detección de Objetos con YOLO: Modelos Small, Nano y YOLOv12

Este proyecto presenta una comparación y análisis de diferentes modelos de detección de objetos basados en YOLO (You Only Look Once). Se enfocan en las versiones Nano y Small de YOLOv5 y YOLOv8, además del modelo YOLOv12, con énfasis en métricas, velocidad y aplicaciones en tiempo real.

## Tabla de Contenidos

- [Introducción](#introducción)
- [Objetivo](#objetivo)
- [Modelos Comparados](#modelos-comparados)
- [Métricas y Resultados](#métricas-y-resultados)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Cómo Ejecutar el Proyecto](#cómo-ejecutar-el-proyecto)
- [Conclusiones](#conclusiones)
- [Referencias](#referencias)

## Introducción

Este proyecto realiza una comparación entre diferentes versiones ligeras de los modelos YOLO (Nano y Small) y el modelo YOLOv12, con el objetivo de evaluar su desempeño en tareas de detección de objetos en tiempo real, particularmente en tareas específicas como la detección de armas. La evaluación se realiza a través de métricas clave como precisión (Precision), recall, mAP@0.5 y mAP@0.5:0.95, además de analizar la velocidad de inferencia.

## Objetivo

- Comparar el rendimiento de los modelos Nano (n) y Small (s) de YOLOv5 y YOLOv8.
- Incluir el análisis del modelo YOLOv12 como una opción ligera y rápida.
- Determinar cuál modelo es más adecuado para aplicaciones en tiempo real con recursos limitados.
- Proporcionar una referencia clara para la selección de modelos en diferentes escenarios.

## Modelos Comparados

| Modelo | Tamaño (px) | Precisión (mAP@0.5:0.95) | Velocidad (ms) | Ventajas | Desventajas |
|--------|-------------|---------------------------|----------------|----------|-------------|
| YOLOv5n (Nano) | 640x640 | 0.42625 | ~3 ms | Muy rápido, bajo consumo, ideal para hardware restringido | Menor precisión, menos robusto en escenarios complejos |
| YOLOv8n (Nano) | 640x640 | 0.54554 | ~1.2 ms | Alta velocidad, arquitectura moderna | Menor precisión en detección de objetos pequeños |
| YOLO12n (futuro, ligera) | 640x640 | 0.53217 | ~2.6 ms | Muy rápida, ligera | Precisión menor, menos robustez frente a escenas complejas |
| YOLOv5s (Small) | 640x640 | 0.42625 | ~5.5 ms | Buen equilibrio velocidad y precisión | Requiere más recursos que Nano |
| YOLOv8s (Small) | 640x640 | 0.54554 | ~1.2 ms | Excelente balance velocidad y precisión | Mayor requerimiento de recursos |

## Métricas y Resultados

Se evaluaron los modelos en base a:

- **Precisión (Precision):** Capacidad de NO generar falsos positivos.
- **Recall:** Capacidad de detectar la mayoría de los objetos presentes.
- **mAP@0.5:** Métrica promedio de precisión en diferentes objetos.
- **mAP@0.5:0.95:** Evaluación más exigente, considerando diferentes umbrales.

Los resultados muestran que modelos Nano y Small ofrecen un excelente balance para aplicaciones en tiempo real, siendo ideales para hardware con limitaciones de recursos.

## Tecnologías Utilizadas

- Python 3.x: Lenguaje de programación principal para la implementación y evaluación de modelos.
- PyTorch: Framework de deep learning utilizado para entrenar y cargar modelos YOLO.
- Ultralytics YOLO: Implementación oficial de los modelos YOLOv5 y YOLOv8.
- OpenCV: Biblioteca para procesamiento de imágenes y videos.
- NumPy: Biblioteca para procesamiento numérico y manejo de matrices.
- Matplotlib: Para graficar métricas y resultados de evaluación.
- CUDA/cuDNN: Para aceleración con GPU en entrenamiento y evaluación (opcional).

## Cómo Ejecutar el Proyecto
Cómo Ejecutar el Proyecto

Clona el repositorio:

bashgit clone <URL_del_repositorio>
cd <nombre_del_directorio>

Crea un entorno virtual (opcional pero recomendable):

bashpython -m venv venv
source venv/bin/activate  # En Linux/Mac
venv\Scripts\activate     # En Windows

Instala las dependencias:

bashpip install -r requirements.txt

Descarga o predefine los modelos YOLO (nano, small, etc.)
Asegúrate de tener los archivos de peso (.pt) en tu directorio.
Ejecuta la detección o evaluación:

bashpython detect.py --weights <modelo.pth> --source <ruta_a_video_o_imagen> --img-size 640
(Reemplaza <modelo.pth> por el modelo que quieres usar y <ruta_a_video_o_imagen> por la fuente de entrada.)

## Conclusiones

-Los modelos ligeros como Nano y Small permiten realizar detecciones en tiempo real en hardware con recursos limitados, aunque con una leve disminución en precisión.

-La elección del modelo adecuado depende del balance entre velocidad y precisión que requiera tu aplicación.

-La versión YOLOv8s combina velocidad y precisión de una manera muy favorable para tareas en tiempo real.

-Es importante evaluar el hardware disponible y los requisitos específicos del proyecto antes de seleccionar el modelo.

-La integración de estos modelos en sistemas embebidos y aplicaciones móviles puede facilitar detecciones eficientes sin -necesidad de hardware potente.

## Referencias

-YOLOv5 GitHub

-YOLOv8 GitHub

-Documentación Ultralytics YOLO
