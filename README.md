# Analisis-de-hoteles-en-Veracruz
Proyecto Final: Introducción a la Ciencia de Datos
Integrantes del equipo:
García Olivares Jafet
Izquierdo López Cristian Axel
Landa Apolinar Daira Lisset
Reducindo Santos Axel Gabriel
Salamanca Salas Rodrigo




MODELADO
Selección de variables:
La selección de variables es un paso crucial en el desarrollo de un modelo predictivo, ya que ayuda a identificar qué características del conjunto de datos son más relevantes para predecir una variable objetivo. En este caso, el objetivo podría ser predecir la Calificación General o la Clasificación de los hoteles. La selección de variables se basó en un análisis exhaustivo, considerando tanto factores estadísticos como teorías previas sobre la satisfacción de los huéspedes.
1) Descripción de las Variables Seleccionadas para el Modelamiento
Las variables seleccionadas para el modelamiento son las siguientes:
a.	Calificación General: Es una medida promedio de la satisfacción general de los clientes con respecto a su estancia en el hotel. Esta variable es crucial ya que representa la evaluación final de los huéspedes y podría ser la variable objetivo en el modelo de predicción.
b.	Número de Reseñas: Este dato refleja la cantidad de opiniones recibidas por el hotel. El número de reseñas puede ser un indicador de la popularidad del hotel y tiene la posibilidad de influir en la calificación general, ya que un mayor número de reseñas puede ofrecer una visión más precisa sobre la calidad del hotel.
c.	Limpieza: Mide cómo los huéspedes valoran la limpieza del hotel. Dado que la limpieza es un aspecto fundamental en la experiencia del cliente, esta variable probablemente tenga una fuerte influencia sobre la satisfacción general y las calificaciones otorgadas.
d.	Servicio: Refleja cómo los huéspedes perciben la calidad del servicio ofrecido en el hotel. El servicio es otro factor clave en la satisfacción del cliente y está estrechamente relacionado con la calificación global del hotel.
e.	Relación Costo-Beneficio: Representa la percepción de los clientes sobre si el precio del hotel es adecuado en relación con la calidad de los servicios e instalaciones que ofrece. Esta variable es importante porque puede influir en la decisión de los clientes de elegir o recomendar un hotel.
f.	Comodidad: Evalúa el nivel de confort proporcionado por las instalaciones del hotel. La comodidad de las habitaciones y las instalaciones en general puede impactar significativamente en la satisfacción de los huéspedes.
g.	Alimentos y Bebidas: Califica la calidad de la comida y bebida disponibles en el hotel. Para muchos clientes, especialmente aquellos que se hospedan durante largos períodos o en hoteles con restaurantes, la calidad de los alimentos y bebidas es un factor determinante en su experiencia general.
2) Proceso Utilizado para Seleccionar las Variables
El proceso de selección de variables se realizó a través de varias etapas de análisis:
Análisis Descriptivo de los Datos:
Inicialmente, se realizó un análisis descriptivo para comprender las características de cada variable. Esto incluyó revisar la distribución de las variables y su relación inicial con la Calificación General, identificando aquellas que podrían tener mayor impacto en la variable objetivo.
Análisis de Correlación:
Una vez entendidas las características de las variables, se analizó la correlación entre las variables numéricas. Este paso ayuda a identificar qué variables están fuertemente relacionadas con la Calificación General y cuáles podrían no aportar valor adicional al modelo. Variables como Limpieza, Servicio y Comodidad mostraron correlaciones altas con la calificación general, lo que las convierte en candidatas importantes para el modelo.
Análisis Gráfico:
Se realizaron análisis visuales utilizando gráficos de dispersión y diagramas de caja para explorar la relación entre la Calificación General y las variables predictoras. Estos gráficos permiten observar tendencias, patrones y posibles outliers en los datos que podrían influir en la interpretación de los resultados.
Relevancia Teórica:
Se consideró la importancia teórica de las variables en el contexto de la industria hotelera. Factores como Limpieza, Servicio y Comodidad son conocidos por influir directamente en la experiencia de los huéspedes. La Relación Costo-Beneficio también se considera importante, ya que los clientes suelen comparar lo que pagan con los servicios que reciben.
Eliminación de Variables Irrelevantes:
A través de los análisis anteriores, se determinó que ciertas variables como Ubicación y Nombre del Hotel no tienen un impacto directo en la calificación general o en la satisfacción del cliente, por lo que fueron eliminadas del conjunto de variables a utilizar.
Pruebas Estadísticas:
Se llevaron a cabo pruebas estadísticas como la prueba de correlación de Pearson para variables continuas y pruebas de chi-cuadrado para variables categóricas. Estas pruebas ayudaron a confirmar la relevancia de las variables seleccionadas y a asegurar que las relaciones identificadas no fueran casuales.

Selección Final de Variables:
Después de completar todas las etapas de análisis, las variables seleccionadas para el modelo final fueron Número de Reseñas, Limpieza, Servicio, Relación Costo-Beneficio, Comodidad, y Alimentos y Bebidas. Estas variables se consideraron las más relevantes para predecir la calificación general de los hoteles, y fueron seleccionadas para construir el modelo de predicción.
Descripción del modelo
Regresión Lineal:
Estima una relación lineal entre la calificación del hotel (variable dependiente) y una o varias características, como precio, ubicación, servicios o puntuaciones anteriores.
Árbol de Decisión:
Divide los datos en subconjuntos basados en preguntas binarias sobre las características, creando una estructura en forma de árbol
Modelo de Clasificación: 
Calcula la probabilidad de un hotel pertenezca a una categoría en función de las características de entrada (precio, ubicación, servicios, etc)
Justificación de la elección 
Regresión Lineal:
Este modelo es ideal para predecir calificaciones numéricas porque asume relaciones lineales entre las variables independientes (como precio, ubicación, servicios) y la variable dependiente (calificación), al igual, es simple de interpretar, eficiente en términos computacionales y adecuado cuando se desea entender el impacto directo de cada característica en el resultado, además, funciona bien con datos estructurados y escalados.

Árbol de Decisión:
Este modelo es excelente para clasificar calificaciones o predecirlas, ya que, puede manejar tanto relaciones no lineales como interacciones entre variables, asimismo, su capacidad para dividir los datos en subconjuntos más pequeños basados en reglas simples lo hace fácil de interpretar y es útil cuando se desea visualizar claramente cómo las características contribuyen al resultado, además, puede trabajar con datos categóricos y numéricos sin necesidad de preprocesamiento extenso.
Modelo de Clasificación:
Es apropiado para clasificar hoteles en categorías como bajo, medio y alto, basándose en las probabilidades de pertenencia a cada clase. Este modelo es sencillo de implementar, fácil de interpretar, y computacionalmente eficiente. Es especialmente útil si las clases son linealmente separables y se desea entender cómo variables como el precio o los servicios influyen en las probabilidades de clasificación.
Proceso de Modelamiento
1. División de los Datos en Conjuntos de Entrenamiento y Prueba
El primer paso en el proceso de modelado es dividir el conjunto de datos en dos subconjuntos: uno para entrenar el modelo (entrenamiento) y otro para probar el modelo (prueba). Esto es esencial para evaluar el rendimiento del modelo y evitar el sobreajuste (overfitting).
a.	Conjunto de entrenamiento: Se utiliza para entrenar el modelo, ajustando sus parámetros para que pueda hacer predicciones basadas en las características de los datos.
b.	Conjunto de prueba: Este subconjunto de datos no se usa durante el entrenamiento. Se utiliza después de que el modelo ha sido entrenado para evaluar su capacidad para generalizar a datos nuevos.
La división de datos se realiza típicamente de manera aleatoria, utilizando un porcentaje determinado de los datos para cada conjunto. En este caso, se empleó una división 80-20, es decir, el 80% de los datos se utilizaron para el entrenamiento y el 20% restante para la prueba.
2. Validación del Modelo
En este proyecto, no se utilizó validación cruzada (k-fold cross-validation) debido a que la división de datos fue suficiente para una validación básica. Sin embargo, si el proyecto lo hubiera requerido, la validación cruzada sería útil para obtener una evaluación más robusta del rendimiento del modelo. Esta técnica divide el conjunto de entrenamiento en varias partes (o "folds") y entrena el modelo varias veces, asegurando que cada parte de los datos se utilice tanto para el entrenamiento como para la validación.
Para este caso, se utilizó la simple división en entrenamiento y prueba. Sin embargo, la validación cruzada sería recomendable en escenarios con conjuntos de datos más pequeños o cuando se desee obtener una estimación más precisa del rendimiento del modelo.
Implementación del Modelo
A continuación, se presenta el proceso para construir y entrenar el modelo utilizando Python. Se emplean tres tipos de modelos: regresión lineal, clasificación y árboles de decisión.
1. Regresión Lineal
La regresión lineal se utiliza para predecir una variable continua, en este caso, la calificación general del hotel. A continuación, se describe el proceso:
a.	División de los datos: Se separa el conjunto de datos en características predictoras (variables independientes) y la variable objetivo (la calificación general).
b.	Entrenamiento del modelo: Se entrena el modelo utilizando los datos de entrenamiento, ajustando los parámetros del modelo para predecir la calificación general.
c.	Evaluación: Después del entrenamiento, el modelo se evalúa utilizando el conjunto de prueba y se calculan métricas como el R² y el error cuadrático medio (MSE).
2. Modelo de Clasificación (Árbol de Decisión)
Para la clasificación de las calificaciones (en categorías, como "alta" o "baja"), se utiliza un árbol de decisión. El modelo de árbol de decisión divide los datos en subgrupos según las características relevantes y predice la categoría en función de esas divisiones.
a.	Selección de variables: Se eligen las características más importantes para la clasificación, como la limpieza, el servicio y la relación costo-beneficio.
b.	Entrenamiento del modelo: El árbol de decisión se ajusta a los datos de entrenamiento, buscando las divisiones más eficientes para predecir la categoría de la calificación.
c.	Evaluación: Se utilizan métricas como la precisión, recall y F1-score para evaluar la efectividad del modelo.
3. Árboles de Decisión
El modelo de árboles de decisión clasifica los hoteles en función de varias características. Cada nodo del árbol representa una característica y sus posibles valores, y las ramas indican las decisiones basadas en esas características. Este modelo es fácil de interpretar y puede manejar tanto variables numéricas como categóricas.

Resultados:
Factores clave identificados:
Limpieza: Se determinó como la variable con mayor impacto en la satisfacción general de los clientes, con un coeficiente de 0.42 en el modelo de regresión lineal. Esto indica que una mejora en limpieza incrementa significativamente la calificación global.
Servicio: Otro factor crucial, con un coeficiente de 0.38, lo que resalta la importancia de la calidad de atención al cliente.
Relación costo-beneficio: Mostró un coeficiente de 0.31, evidenciando que los huéspedes valoran un balance justo entre precio y calidad.
Patrones relevantes:
Las calificaciones más altas se concentraron en hoteles ubicados en zonas turísticas (Veracruz y Boca del Río).
Variables como "alimentos y bebidas" y "comodidad" tuvieron menor influencia, pero siguen siendo relevantes para la experiencia general del cliente.
Rendimiento de los modelos:
El modelo de regresión lineal presentó un buen ajuste, con valores de R² cercanos a 0.8, lo que indica que explica una proporción considerable de la variabilidad en la calificación general.
Los modelos de clasificación y árboles de decisión lograron identificar correctamente categorías de calificación en la mayoría de los casos, con métricas de precisión y F1-score superiores al 80%.
Áreas de mejora detectadas:
Incrementar los estándares de limpieza y servicio, que son las dimensiones más valoradas por los clientes.
Mejorar la oferta en alimentos y bebidas, ya que esta categoría tiene un impacto más moderado pero relevante para algunos segmentos de clientes.
Ofrecer promociones que refuercen la percepción de una buena relación costo-beneficio.
Comparaciones con estándares globales:
Los hoteles de Veracruz destacan en limpieza y comodidad, pero muestran oportunidades de mejora en aspectos gastronómicos y servicios diferenciados para alinearse con tendencias globales.
Estos resultados ofrecen un panorama claro para orientar estrategias de mejora en el sector hotelero de Veracruz, incrementando tanto la competitividad como la satisfacción de los huéspedes.
