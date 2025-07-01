# Analizando el Control Orientado en el Fútbol: Definición e Impacto
Este repositorio contiene el código y los recursos asociados al Trabajo de Fin de Grado (TFG) cuyo nombre da título a esta descripción. El trabajo presente se centra en lograr una definición formal y matemática del control orientado en el fútbol a través de un consenso de expertos (jugadores, entrenadores, analistas, etc). Una vez obtenida, se validará para que tenga rigor táctico y se demostrará su importancia en el rendimiento deportivo comparando su poder predictivo para los ratings de los jugadores en cada partido, obtenidos mediante APIs.

## Estructura del Repositorio
El repositorio está organizado en carpetas que corresponden a las diferentes fases del proyecto, facilitando la comprensión del flujo de trabajo y la localización de los recursos.
```
├── 01_Consenso_Expertos/
├── 02_Obtencion_Metrica/
├── 03_Analisis_Metrica/
├── 04_Obtencion_Ratings_API/
├── 05_Prediccion_Ratings_Modelos/
└── README.md
```


A continuación, se detalla el contenido de cada carpeta:

### `01_ConsensoExpertos/`

Esta carpeta alberga los resultados del formulario para el **consenso de expertos**. En esta etapa inicial, se recopiló y analizó la opinión de profesionales del fútbol (entrenadores, analistas de rendimiento, etc.) para definir los criterios cualitativos y los factores clave que caracterizan un buen control orientado. Más tarde se procesaron todas estas respuestas mediante un flujo de trabajo en VectorShift, que desarrolló una fórmula en base a las respuestas de los expertos. Este flujo se ejecutó dos veces, en español y en inglés, para asegurar que tenía en cuenta todas las respuestas. Los resultados de este flujo también se reflejan aquí.

### `02_MetricaControlOrientado/`

Aquí se encuentra el código utilizado para la **obtención de la métrica** del control orientado. Esta fase implica el procesamiento de datos de eventos de Statsbomb para derivar una métrica cuantificable que represente la calidad e impacto de un control orientado. No vienen los datos ya que se obtienen mediante la librería de Statsbomb para Python, statsbombpy. El conjunto de datos resultante no se incluye aquí, ya que más adelante se utilizará para su análisis.

### `03_AnalisisMetrica/`

Esta carpeta contiene el análisis exploratorio y estadístico de la métrica de control orientado obtenida. El **análisis de la métrica** busca comprender sus propiedades, distribuciones, y cómo se relaciona con otros aspectos del juego. Se incluyen visualizaciones, pruebas estadísticas y la identificación de patrones. El principal objetivo es lograr demostrar que la métrica representa bien la naturaleza de un buen control orientado, teniendo rigor táctico.

### `04_ObtencionRatings/`

En esta sección se gestiona la **obtención de ratings de jugadores a través de APIs**. Para comparar el rendimiento de los modelos predictivos, es necesario disponer de datos de las valoraciones o "ratings" de jugadores de fuentes externas. Esta carpeta contendrá los scripts para interactuar con estas APIs y almacenar los datos obtenidos. Se compararán diferentes APIs, aunque al final se escogerán los datos ofrecidos por Sportmonks. Los resultados se encuentran en la carpeta dedicada a la predicción, ya que el notebook carga el archivo para procesar los datos.

### `05_PrediccionRatings/`

Esta es la carpeta central donde se realiza la **predicción de los ratings de jugadores y la comparación de modelos**. Aquí se implementan y entrenan los diferentes modelos de *machine learning* (Ridge, Random Forest, Gradient Boosting, SVR) para predecir los ratings en base al control orientado y el rendimiento general de los jugadores. Se incluye el código para el entrenamiento, la evaluación y la comparación del rendimiento de cada modelo. También se incluyen los datos de Statsbomb con el control orientado junto con los ratings de los jugadores necesarios para el preprocesamiento del dataset final.

---
Se espera que esta estructura facilite la navegación y comprensión de este proyecto de ciencia de datos aplicada al fútbol. Para más información acerca del proyecto consultar la memoria publicada por la UPM o consultar al autor a través del siguiente correo electrónico: antonio.reviejo@alumnos.upm.es
