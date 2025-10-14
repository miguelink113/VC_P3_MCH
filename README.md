#Proyecto de Visión por Computadora: Monedas y Fragmentos

Este proyecto integra clasificación automática de monedas y fragmentos/objetos usando Python y OpenCV, combinando detección de contornos, análisis de color, extracción de características geométricas, y clasificación heurística ponderada.

Se incluyen visualizaciones, métricas de desempeño y resúmenes económicos o científicos, mostrando cómo aplicar visión por computadora a problemas reales de análisis de imágenes.

Contenido del Proyecto

Detección y clasificación de monedas de euro: identificación por tamaño y color, cálculo de valor total y visualización anotada.

Clasificación de fragmentos/objetos: detección de contornos, extracción de características ponderadas y normalizadas, evaluación con Ground Truth y métricas estándar.

Visualización de contornos detectados, mapas de calor, comparaciones de clasificación y matrices de confusión.

Dependencias

Python 3.x

OpenCV
 (cv2)

NumPy
 (numpy)

Matplotlib
 (matplotlib)

Seaborn
 (seaborn)

Pandas
 (pandas)

scikit-learn
 (accuracy_score, precision_score, recall_score, f1_score, confusion_matrix)

Instalación rápida:

pip install opencv-python numpy matplotlib seaborn pandas scikit-learn

1️⃣ Clasificación de Monedas de Euro
Características

Detección de monedas mediante Transformada de Hough.

Clasificación por tamaño relativo a una moneda de referencia (1 euro).

Análisis de color RGB para distinguir cobrizo, dorado y plateado.

Etiquetado visual con valor, color y radio aproximado.

Resumen económico total (euros y céntimos).

Flujo de Trabajo

Cargar imagen (Monedas.jpg).

Seleccionar la moneda de 1 euro con clic del ratón.

Detectar y clasificar las demás monedas según tamaño y color.

Visualizar resultados con anotaciones y valor total.

Paleta de Colores y Valores
Color	Valores Posibles
Cobrizo	1, 2, 5 ct
Dorado	10, 20, 50 ct
Plateado	1 €, 2 €
2️⃣ Clasificación de Fragmentos/Objetos
Características

Detección de contornos válidos con filtrado por área y solapamiento mínimo.

Extracción de características geométricas y de color:

Área, perímetro, compacidad

Relación área/contorno, relación de aspecto

Relación de ejes, distancia relativa al centroide

Distancia al negro (color)

Clasificación heurística ponderada y normalizada usando pesos por característica.

Evaluación comparando con Ground Truth usando IoU ≥ 0.5.

Cálculo de métricas: Accuracy, Precision, Recall, F1-score y matriz de confusión.

Paleta de Colores por Clase
Clase	Color (BGR)
FRA	Verde (0,255,0)
PEL	Rojo (0,0,255)
TAR	Azul (255,0,0)
3️⃣ Visualización y Resultados

Contornos detectados en imágenes de entrenamiento y test.

Mapas de calor de medias normalizadas de características por clase.

Comparación lado a lado de Ground Truth vs Clasificación heurística.

Resumen económico para monedas y métricas cuantitativas para fragmentos.

4️⃣ Ejecución
Monedas
python clasificacion_monedas.py


Selecciona la moneda de 1 euro.

Obtén imagen final con anotaciones y total económico.

Fragmentos/Objetos
python classification_fragments.py


Detecta contornos, extrae características y clasifica según heurística ponderada.

Visualiza resultados y métricas comparadas con Ground Truth.

5️⃣ Metodología Combinada

Preprocesamiento de imágenes: corrección de iluminación, suavizado, umbral adaptativo.

Detección de objetos: contornos externos o círculos según el tipo de proyecto.

Extracción de características: geométricas y de color.

Clasificación:

Monedas: combinación de tamaño y color.

Fragmentos: distancia ponderada y normalizada a centroides de clase.

Visualización y evaluación: anotaciones, resúmenes, métricas y mapas de calor.

6️⃣ Mejora y Extensiones Futuras

Clasificación automática sin intervención manual (monedas).

Robustez ante solapamiento y fondos complejos.

Optimización de pesos por característica usando aprendizaje supervisado.

Interfaz gráfica interactiva para experimentación en tiempo real.

Integración de métodos de machine learning avanzados (Random Forest, CNNs) para mejorar precisión.

7️⃣ Autor

Tu Nombre – Apasionado de la visión por computadora y la automatización de análisis de imágenes.