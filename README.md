# Analisis-de-hoteles-en-Veracruz
Proyecto Final: Introducción a la Ciencia de Datos

Integrantes del equipo:

García Olivares Jafet

Izquierdo López Cristian Axel

Landa Apolinar Daira Lisset

Reducindo Santos Axel Gabriel

Salamanca Salas Rodrigo

Descripción General del Proyecto: 
Este proyecto analizó datos de 50 hoteles en Veracruz para identificar patrones y tendencias que impactan la satisfacción de los huéspedes y el desempeño hotelero. Utilizando herramientas de ciencia de datos, se exploraron aspectos clave de la industria para proponer estrategias de mejora competitiva.

Objetivo Principal: 
Determinar las características más relevantes que influyen en la satisfacción de los huéspedes y proporcionar recomendaciones para mejorar el posicionamiento y competitividad de los hoteles en el mercado turístico de Veracruz.

Resumen de los Pasos Realizados: 
Exploración de los datos: Identificación de variables clave y análisis inicial para garantizar la calidad del dataset.
Selección de variables relevantes: Basada en análisis descriptivos, correlaciones y criterios teóricos.
Modelado: Implementación de modelos de regresión lineal y árboles de decisión para evaluar el impacto de diferentes factores en la calificación general.
Evaluación de modelos: Análisis de métricas de desempeño como R² y MSE para validar la precisión de las predicciones.
Interpretación y propuestas: Identificación de áreas de mejora y generación de estrategias basadas en los hallazgos del modelo.

Principales Resultados Obtenidos: 
Factores clave: Limpieza (coef. 0.42) y servicio (coef. 0.38) son los principales impulsores de la satisfacción general.
Tendencias: Los hoteles mejor evaluados ofrecen servicios diferenciados y están en zonas turísticas.
Relación costo-beneficio: Influye significativamente en la percepción del cliente, destacando la importancia de tarifas competitivas.
Áreas de mejora: Potenciar limpieza, servicio, y alimentos y bebidas para alinearse con estándares internacionales y atraer más turistas.
## Archivos del Proyecto

A continuación se listan los archivos principales utilizados en este proyecto:

1. **[Gráfico de Calificaciones Generales](images/califgeneral.png)**  
   Visualización clave que muestra las calificaciones generales de los hoteles.

2. **[Código 1: Análisis de Datos](codigo1)**  
   Primer notebook con el análisis exploratorio de los datos.

3. **[Código 2: Limpieza de Datos](notebooks/codigo2.ipynb)**  
   Segundo notebook que contiene el proceso de limpieza de los datos.

4. **[Código 3: Modelado de Datos](notebooks/codigo3.ipynb)**  
   Tercer notebook para el modelado y análisis predictivo de los datos.

5. **[Dataset de Hoteles](data/hoteles.csv)**  
   Archivo CSV con los datos de los hoteles en Veracruz, utilizado para el análisis.

6. **[Gráfico de Limpieza de Datos](images/limpieza.png)**  
   Visualización que muestra el proceso de limpieza y los datos transformados.

<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fases del Proyecto</title>
  <style>
    body {
        font-family: Arial, sans-serif;
    }
    ol {
        list-style: decimal;
        margin: 20px;
        padding: 0;
    }
    a {
        text-decoration: none;
        color: blue;
    }
    a:hover {
        text-decoration: underline;
    }
    section {
        margin-top: 50px;
    }
</style>

</head>
<body>
    <h2>Fases del Proyecto</h2>
    <ol>
        <li><a href="#introduccion">Introducción</a></li>
        <li><a href="#problema">Planteamiento del problema</a></li>
        <li><a href="#datos">Conjunto de datos</a></li>
        <li><a href="#modelamiento">Modelamiento de datos</a></li>
        <li><a href="#resultados">Resultados</a></li>
        <li><a href="#conclusiones">Conclusiones</a></li>
    </ol>
    <section id="introduccion">
        <h3>Introducción</h3>
        <p>El turismo en Veracruz es una de las principales actividades económicas y sociales del estado, gracias a su diversidad cultural, histórica y natural. Este estado, ubicado en la costa del Golfo de México, ofrece una amplia gama de atractivos turísticos que van desde playas y zonas arqueológicas hasta ciudades con un rico legado histórico y tradiciones vivas. Sin embargo, para que el turismo contribuya de manera sostenida al desarrollo regional, es fundamental garantizar que la experiencia de los visitantes sea positiva y que los servicios ofrecidos por la industria hotelera cumplan con las expectativas de calidad.
        

A pesar de su riqueza turística, Veracruz enfrenta retos en términos de competitividad dentro del sector hotelero. La calidad percibida de los servicios, la atención al cliente y la infraestructura varían considerablemente entre los diferentes municipios del estado. Estas diferencias pueden afectar la reputación de los destinos turísticos y, en consecuencia, influir en las decisiones de los visitantes al momento de elegir dónde hospedarse. En este contexto, analizar las opiniones y calificaciones de los hoteles se convierte en una herramienta clave para comprender las áreas prioritarias de mejora y tomar decisiones informadas.


Este proyecto tiene como objetivo analizar la calidad de los servicios hoteleros en el estado de Veracruz a través de un dataset ficticio que integra variables como limpieza, servicio, instalaciones y satisfacción general de los huéspedes. Se busca explorar las características del desempeño hotelero en los distintos municipios del estado, identificar patrones en las calificaciones y destacar las áreas que requieren atención inmediata. Al proporcionar un análisis estadístico y visual de estas variables, este estudio pretende generar información valiosa para las autoridades turísticas y los propietarios de hoteles, con el fin de mejorar la oferta turística y fomentar el desarrollo del sector en todo el estado.</p>
    </section>
    <section id="problema">
        <h3>Planteamiento del problema</h3>
        <p>Características que influyen en la satisfacción: Limpieza, comodidad, atención al cliente, ubicación y servicios adicionales son aspectos prioritarios que impactan significativamente en la fidelización y percepción de los huéspedes.
Tendencias en servicios: Adaptarse a tendencias modernas es crucial para alinearse con las expectativas de los viajeros. Esto incluye ofrecer servicios diferenciados y ajustarse a estándares globales.

Impacto de las calificaciones: Las opiniones en plataformas como Booking.com son decisivas para el posicionamiento de los hoteles, influyendo en las reservas y la reputación en línea.

Relación tarifas-calidad: El balance entre precio y calidad percibida es clave para mejorar la competitividad y ajustar estrategias de mercado.
Áreas de mejora: Se deben reforzar la innovación, diferenciación, limpieza, servicio y relación calidad-precio para aumentar la competitividad y atraer más turistas.
</p>
    </section>
    <section id="datos">
        <h3>Conjunto de datos</h3>
        <p>El dataset utilizado en este análisis se centra en las características, calificaciones y servicios ofrecidos por 50 hoteles ubicados en diferentes ciudades del estado de Veracruz, además, fue diseñado para identificar patrones y tendencias en las opiniones de los clientes, evaluando aspectos clave que afectan la experiencia de los huéspedes. 
Fuente de los datos:
            
Los datos utilizados en este proyecto fueron obtenidos de Booking.com, una plataforma pública que proporciona información detallada sobre hoteles, calificaciones de clientes y servicios ofrecidos. Esta información es accesible a cualquier usuario interesado en comparar opciones hoteleras, lo que la hace adecuada para análisis académicos enfocados en identificar patrones y tendencias en el sector turístico.

Características Principales:

1.	Total, de registros: 50
2.	Variables principales:
·	Ubicación: Indica la localidad donde se encuentra el hotel. Es una variable categórica representada por nombres de ciudades del estado de Veracruz, como Xalapa, Veracruz, Coatepec, Orizaba o Boca del Río. Esta variable es útil para analizar cómo varían las calificaciones entre diferentes regiones.

·	Calificación General: Refleja la puntuación promedio que los huéspedes han otorgado al hotel en una escala de 3 a 5. Es una variable numérica que mide la percepción global del servicio y la experiencia en el hotel.

·	Número de Reseñas: Representa la cantidad de opiniones recibidas por cada hotel. Es una variable numérica entera que proporciona información sobre la popularidad o nivel de atención que el hotel ha recibido por parte de los visitantes.

·	Limpieza: Mide la calidad de la limpieza del hotel según las opiniones de los huéspedes. Es una variable numérica en una escala de 3 a 5, donde un puntaje más alto indica un nivel de limpieza superior.

·	Servicio: Evalúa la atención brindada por el personal del hotel, con calificaciones en una escala de 3 a 5. Esta variable es un indicador clave de la satisfacción del cliente con el trato recibido.

·	Relación Costo-Beneficio: Indica si el precio pagado por los huéspedes corresponde a la calidad de los servicios y comodidades ofrecidos. Es una variable numérica en la misma escala de 3 a 5.

·	Comodidad: Refleja la percepción de los huéspedes sobre el confort y la funcionalidad de las habitaciones y áreas comunes del hotel. También se mide en una escala de 3 a 5.

·	Alimentos y Bebidas: Evalúa la calidad y variedad de los servicios de alimentos y bebidas proporcionados por el hotel. Es una variable numérica en una escala de 3 a 5, que mide aspectos como sabor, presentación y atención en este rubro.

Procedencia de los datos
Los datos provienen de Booking.com, una plataforma pública utilizada para comparar y reservar alojamientos. La información fue recopilada manualmente de hoteles en Veracruz, considerando ubicación, calificaciones y servicios.
Enlace: https://www.booking.com/</p>
    </section>
    <section id="modelamiento">
        <h3>Modelamiento de datos</h3>
        <p>Selección de variables:
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

3) Proceso Utilizado para Seleccionar las Variables

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

4. Validación del Modelo
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
</p>
    </section>
    <section id="resultados">
        <h3>Resultados</h3>
        <p>Factores clave identificados:
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

Estos resultados ofrecen un panorama claro para orientar estrategias de mejora en el sector hotelero de Veracruz, incrementando tanto la competitividad como la satisfacción de los huéspedes.</p>
    </section>
    <section id="conclusiones">
        <h3>Conclusiones</h3>
        <p>Desempeño Hotelero por Municipio
El análisis realizado reveló disparidades significativas en la calidad de los servicios ofrecidos por los hoteles en diferentes municipios del estado de Veracruz. Ciudades turísticas como Veracruz y Boca del Río destacaron por contar con calificaciones más altas en limpieza y servicio, mientras que municipios menos desarrollados o con menor afluencia turística presentaron evaluaciones más bajas en aspectos clave como infraestructura y atención al cliente.


Factores Clave de Satisfacción
Las calificaciones en limpieza y servicio fueron identificadas como los factores que más influyen en la satisfacción general de los huéspedes. La falta de consistencia en estos aspectos en algunos municipios podría estar afectando negativamente la experiencia del visitante y, en consecuencia, la percepción global de los destinos turísticos en el estado.


Identificación de Áreas Prioritarias
El uso de análisis de datos permitió localizar municipios con mayores carencias en la industria hotelera. Estas zonas requieren atención específica en:


Mejora de la capacitación del personal para garantizar un servicio de calidad.
Inversión en la modernización de las instalaciones hoteleras.
Estrategias de promoción turística para aumentar la ocupación y la inversión.
Patrones Geográficos de Desempeño
El análisis geográfico evidenció que los municipios costeros y aquellos con una infraestructura turística consolidada suelen presentar mejores calificaciones. Por otro lado, municipios del interior del estado enfrentan mayores retos para competir en el mercado turístico debido a sus limitaciones en servicios y conectividad.


Relevancia del Proyecto
Este proyecto demuestra el valor de aplicar la ciencia de datos para evaluar y mejorar la competitividad de la industria hotelera en Veracruz. Los hallazgos obtenidos pueden servir como base para que las autoridades turísticas, propietarios de hoteles y otros actores clave diseñen estrategias que impulsen el desarrollo del sector y potencien el impacto del turismo como motor económico en el estado.



</p>
    </section>
</body>
</html>






