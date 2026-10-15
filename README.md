##Introducción: 
Eres analista de datos en ConnectaTel, una empresa de telecomunicaciones con operaciones en México y Colombia.

Tu equipo debe entregar un reporte para entender cómo los clientes usan realmente los servicios móviles (llamadas y mensajes).

El objetivo de la empresa es identificar patrones de uso, detectar comportamientos atípicos y comprender qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario.

Para ello, trabajarás con tres fuentes de datos:

plans.csv: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
users_latam.csv: información de clientes: edad, ciudad, fecha de registro, plan contratado.
usage.csv: el detalle de uso real: llamadas (duración) y mensajes (longitud).
Tu misión será explorar, limpiar y analizar estas bases de datos para construir una visión clara, confiable y accionable sobre el comportamiento de uso de los clientes y cómo varía entre diferentes grupos de usuarios.

💡 Preguntas del negocio
¿Qué segmentos de clientes muestran mayor o menor uso de llamadas y mensajes?
¿Qué usuarios presentan valores atípicos que puedan indicar comportamientos inusuales, fraude o errores de registro?
¿Cómo varía el uso según la edad y el tipo de plan contratado?
¿Qué patrones pueden ayudar a diseñar mejores planes, optimizar la oferta y mejorar la satisfacción del cliente?
🎯 Objetivos de aprendizaje del proyecto
Al finalizar este proyecto, podrás:

Integrar y limpiar bases de datos provenientes de tres fuentes distintas.
Aplicar técnicas de validación, estandarización de tipos de datos y detección de valores inconsistentes.
Construir un perfil estadístico del uso (llamadas y mensajes) por cliente y por segmentos demográficos.
Detectar outliers y comportamientos atípicos mediante métodos estadísticos y visuales.
Crear segmentaciones de clientes basadas en edad, país y comportamiento de uso.
Visualizar diferencias entre segmentos y extraer insights comerciales relevantes.
Documentar todo el proceso en un Jupyter Notebook, junto con un README reproducible para subirlo a GitHub.
🛠️ Herramientas de la lección
Jupyter Notebook
Python: pandas, numpy, seaborn, matplotlib
Datasets del Proyecto
Trabajarás con tres fuentes principales de información, relacionadas con usuarios, actividad y planes del servicio de telecomunicaciones:

plans.csv: Catálogo de planes con sus precios y beneficios. Descárgalo aquí.
users_latam.csv: Información de cada usuario (datos personales, plan, fecha de registro, churn). Descárgalo aquí.
usage.csv: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud. Descárgalo aquí.
Estos datasets se complementan para analizar el comportamiento del usuario, su consumo y cómo este se relaciona con el plan contratado, permitiendo detectar patrones de uso y churn.

📝 Plan de acción (pensamiento programático)
Contexto del negocio
Tu misión es analizar el negocio usando los 3 datasets (clientes, uso_real y planes) para que ConnectaTel entienda cómo se comportan sus usuarios según edad, volumen de llamadas/mensajes y nivel de consumo. El entregable será un análisis completo (distribuciones, outliers, segmentación y oportunidades comerciales) acompañado de un notebook limpio y reproducible.

🔄 Flujo general del proyecto
Paso	Acción	Resultado para el negocio
1. Cargar y explorar	Cargar y explorar plans, users_latam, usage.	Visión clara de la estructura y tipos de columna de cada dataset.
2. Identificación de problemas de calidad	Contar nulos, detectar sentinels, revisar fechas fuera de rango.	Lista priorizada de problemas que pueden sesgar decisiones.
3. Limpieza básica	Reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas.	Datos consistentes y listos para análisis estadístico.
4. Summary statistics	Revisar las medidas clave en variables categóricas y numéricas.	Medidas clave (media, mediana, percentiles) que muestran el comportamiento típico y extremo
5. Visualización & outliers	Creación de histogramas y boxplots.	Visualización de sesgos, patrones de usuarios o datos atípicos.
6. Segmentación	Crear segmentaciones basadas en reglas claras; visualizar proporciones con countplots.	Segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.
7. Insight ejecutivo	Redactar conclusiones y recomendaciones comerciales basadas en los pasos anteriores.	Responder a las preguntas del negocio y proponer acciones concretas.
8. Publicación	Subir tu notebook + README a GitHub.	Entrega reproducible para revisión y ejecución por stakeholders.
