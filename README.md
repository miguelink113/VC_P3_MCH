# Clasificación de Contornos en Imágenes

Este proyecto implementa un sistema de detección y clasificación de contornos en imágenes utilizando técnicas de procesamiento de imágenes y clasificación heurística basada en características ponderadas.

## Requisitos
- Python 3.x
- Bibliotecas: OpenCV (`cv2`), NumPy, Pandas, Matplotlib, Seaborn, scikit-learn

## Descripción
El script realiza las siguientes tareas:
1. **Detección de contornos**: Identifica contornos válidos en imágenes basándose en rangos de área y evitando solapamientos significativos.
2. **Extracción de características**: Calcula características como área, perímetro, compacidad, relación de aspecto, entre otras, para cada contorno.
3. **Clasificación**: Clasifica contornos en tres clases (`FRA`, `PEL`, `TAR`) utilizando una distancia euclidiana ponderada y normalizada.
4. **Evaluación**: Compara las predicciones con anotaciones de verdad fundamental (Ground Truth) utilizando IoU (Intersección sobre Unión) ≥ 0.5 y calcula métricas como precisión, sensibilidad y F1-score.
5. **Visualización**: Genera imágenes con contornos dibujados, mapas de calor de características normalizadas y una matriz de confusión.

## Archivos
- **Imágenes de entrenamiento**:
  - `fragment-03-olympus-10-01-2020.JPG` (FRA)
  - `pellet-03-olympus-10-01-2020.JPG` (PEL)
  - `tar-03-olympus-10-01-2020.JPG` (TAR)
- **Imagen de prueba**: `MPs_test.jpg`
- **Anotaciones**: `MPs_test_bbs.csv` (contiene etiquetas y bounding boxes de la imagen de prueba)

## Uso
1. Asegúrate de que las imágenes y el archivo CSV estén en el mismo directorio que el script.
2. Instala las dependencias: `pip install opencv-python numpy pandas matplotlib seaborn scikit-learn`
3. Ejecuta el script en un entorno Python con las bibliotecas instaladas.

## Salidas
- Visualización de contornos detectados en las imágenes de entrenamiento y prueba.
- Mapa de calor de medias normalizadas de características por clase.
- Imágenes comparativas (Ground Truth vs. Predicciones).
- Métricas de evaluación (precisión, sensibilidad, F1-score) y matriz de confusión si hay coincidencias con IoU ≥ 0.5.

## Notas
- Ajusta los parámetros `min_area` y `max_area` en `detect_valid_contours` y `process_image` según las necesidades específicas.
- Los pesos de las características (`feature_weights`) pueden modificarse para optimizar la clasificación.
- Requiere que las imágenes y el archivo CSV estén correctamente formateados y accesibles.

## Autor
Desarrollado con fines de análisis de imágenes y clasificación de objetos.