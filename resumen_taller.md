Análisis de correspondencias con R: aplicación a (micro) datos de encuestas
===========================================================================

Objetivo
------------

El objetivo general de este taller es doble: aprender a realizar análisis de correspondencias
con R y practicar el tratamiento de datos de encuestas disponibles públicamente. 


Justificación
-------------
Los resultados de los estudios realizados por diversos organismos públicos como
el Instituto Nacional de Estadística (INE), el Centro de Investigaciones Sociológicas (CIS),
EUROSTAT, y muchos otros (incluídos organismos regionales), se han publicado tradicionalmente
en forma resumida o con las principales conclusiones. Estos resultados se transmiten a la ciudadanía en forma
de informes y notas de prensa que después los medios interpretan. Siendo esta una 
forma importante de difusión al público en general, tiene especial interés para investigadores
de todo tipo el analizar los datos _originales_ de las encuestas, esto es, los **microdatos**.
Las tendencias actuales en transparencia y _Open Data_ están haciendo que cada vez más 
organismos publiquen estos microdatos de forma que puedan ser utilizados por terceros
para realizar sus estudios. Esta es una fuente de información muy rica que se puede
explotar en investigación de mercados, de salud pública, economía, sociología, etc.
Por otra parte, los datos que contienen las encuestas son principalmente cualitativos,
por lo que el análisis de correspondencias, que precisamente pretende identificar 
patrones, tendencias y relaciones entre atributos, es una técnica estadística
muy apropiada para sacar partido de los microdatos de encuestas.

Audiencia
---------
El taller es adecuado para cualquier analista que trate datos cualitativos de cualquier tipo.
Es especialmente útil para quienes trabajen con datos de encuestas, sea cual sea el ámbito
(socioeconómico, sanitario, psicología, marketing, etc.), y en general para cualquier persona
interesada en R y/o el análisis de datos.

Contenido
---------
En este taller vamos a trabajar con la última Encuesta europea de salud en España (EESE) que elabora el Instituto Nacional de Estadística. No obstante, las técnicas son de aplicación a cualquier otra encuesta (EPA, EGM, ...). La diferencia va a estar 
generalmente en la forma de importar los datos en forma de tabla para poder trabajar con ellos en R.

En primer lugar, se revisarán los documentos metodológicos que acompañan a las publicaciones del INE. Así, la información relevante de cada estudio contendrá:

1. Informes de resultados
2. Microdatos
3. Documentos metodológicos
    - Los cuestionarios
    - Metodología general
    - Diseño de registro
    
La metodología general suele ser un documento bastante extenso, pero con las primeras páginas, los cuestionarios, y el diseño de registro, debemos ser capaces de averiguar el formato de los microdatos para importarlos y tratarlos con R. Es importante 
señalar que algunos microdatos se pueden tratar fácilmente con el paquete `MicroDatosEs`, aunque el objetivo de este taller es tratar datos más _crudos_ de otras encuestas.

Una vez revisados los documentos relevantes y los ficheros de datos, procederemos a la importación de los datos al entorno de trabajo de R desde RStudio. Los datos de la EESE están disponibles en formato texto plano de ancho fijo, que se pueden importar de forma muy eficiente con ayuda del diseño de registro. Pero también están en formato Excel, cuya importación es trivial con
el paquete `readxl` por lo que se usará este formato para el taller. 

A continuación, se realizarán para algunas variables seleccionadas de esta encuesta análisis de correspondencias
simples y múltiples, principalmente utilizando el paquete `FactoMineR` y también `factoextra` para algunas visualizaciones.

Finalmente, se darán algunas pinceladas de temas avanzados de R para que los asistentes exploren en el futuro y saquen aún más provecho de las técnicas.


Material y Requisitos
---------------------
El material del taller estará disponible en un repositorio github en forma de proyecto de RStudio que los asistentes
podrán descargar y ejecutar automáticamente con la función `usethis::use_course`. Es aconsejable que antes del comienzo
del taller los asistentes tengan instalado en el equipo que lo vayan a seguir R, RStudio y los paquetes a utilizar.
Esta última tarea se puede realizar con la siguiente expresión en la consola de RStudio:

    install.packages(c("usethis", "readxl", "FactoMineR", "factoextra", 
                   "dplyr", "gplots", "corrplot", "knitr"))


Sobre el ponente
----------------
Emilio López Cano es entusiasta y activista de R. Profesor Contratado Doctor Interino en la Universidad de Castilla-La Mancha, área de Estadística; investigando en la sección de Métodos Cuantitativos y Desarrollo Socioeconómico del Instituto de Desarrollo Regioanl de la UCLM. Previamente investigador en la Universidad Rey Juan Carlos y Estadístico en varias empresas. Autor de dos libros en la serie Use R! de Springer y creador del paquete `SixSigma` y otros. Formador en la Asociación Española para la Calidad y vocal en el subcomité técnico de normalización UNE CTN 66/SC 3 (Métodos Estadísticos). 
Publicaciones y actividades actualizadas en: http://blog.uclm.es/emiliolcano/

https://encuestas.um.es/encuestas/DC45A041FC2CAABFE67C515259BD0CDA1E51C8B74005CE43.pend

ENVIADO REALMENTE (MAX 4000 CARACTERES)
Objetivo
------------
El objetivo general de este taller es doble: aprender a realizar análisis de correspondencias
con R y practicar el tratamiento de datos de encuestas disponibles públicamente. 

Justificación
-------------
Los resultados de los estudios realizados por diversos organismos públicos como
el Instituto Nacional de Estadística (INE), el Centro de Investigaciones Sociológicas (CIS),
EUROSTAT, y muchos otros (incluídos organismos regionales), se han publicado tradicionalmente
en forma resumida o con las principales conclusiones. Tiene especial interés para investigadores
de todo tipo el analizar los datos _originales_ de las encuestas, esto es, los microdatos.
Las tendencias actuales en transparencia y _Open Data_ están haciendo que cada vez más 
organismos publiquen estos microdatos de forma que puedan ser utilizados por terceros
para realizar sus estudios. Esta es una fuente de información muy rica que se puede
explotar en investigación de mercados, de salud pública, economía, sociología, etc.
Por otra parte, los datos que contienen las encuestas son principalmente cualitativos,
por lo que el análisis de correspondencias, que precisamente pretende identificar 
patrones, tendencias y relaciones entre atributos.

Audiencia
---------
El taller es adecuado para cualquier analista que trate datos cualitativos de cualquier tipo.
Es especialmente útil para quienes trabajen con datos de encuestas, sea cual sea el ámbito
(socioeconómico, sanitario, psicología, marketing, etc.), y en general para cualquier persona
interesada en R y/o el análisis de datos.

Contenido
---------
En este taller vamos a trabajar con la última Encuesta europea de salud en España (EESE) que elabora el Instituto Nacional de Estadística. No obstante, las técnicas son de aplicación a cualquier otra encuesta (EPA, EGM, ...). La diferencia va a estar 
generalmente en la forma de importar los datos en forma de tabla para poder trabajar con ellos en R.

En primer lugar, se revisarán los documentos metodológicos que acompañan a las publicaciones del INE. Así, la información relevante de cada estudio contendrá:

1. Informes de resultados
2. Microdatos
3. Documentos metodológicos
    - Los cuestionarios
    - Metodología general
    - Diseño de registro

La metodología general suele ser un documento bastante extenso, pero con las primeras páginas, los cuestionarios, y el diseño de registro, debemos ser capaces de averiguar el formato de los microdatos para importarlos y tratarlos con R. Algunos microdatos se pueden tratar fácilmente con el paquete `MicroDatosEs`, aunque en este taller se tratan datos más _crudos_ de otras encuestas.

Una vez revisados los documentos relevantes y los ficheros de datos, procederemos a la importación de los datos al entorno de trabajo de R desde RStudio. Los datos de la EESE están disponibles en formato texto plano de ancho fijo, que se pueden importar de forma muy eficiente con ayuda del diseño de registro. Pero también están en formato Excel, cuya importación es trivial con
el paquete `readxl` por lo que se usará este formato para el taller. 

A continuación, se realizarán para algunas variables seleccionadas de esta encuesta análisis de correspondencias
simples y múltiples, principalmente utilizando el paquete `FactoMineR` y también `factoextra` para algunas visualizaciones.

Finalmente, se darán algunas pinceladas de temas avanzados de R para que los asistentes exploren en el futuro y saquen aún más provecho de las técnicas.

Material y Requisitos
---------------------
El material del taller estará en un repositorio github en forma de proyecto de RStudio descargable con función `usethis::use_course`. Recomendado tener paquetes a usar.

Sobre el ponente
----------------
Emilio López Cano,  entusiasta y activista de R. Profesor en la Universidad de Castilla-La Mancha. Autor de dos libros en la serie Use R! de Springer y creador del paquete `SixSigma`. Formador en AEC.
Info actualizada: http://blog.uclm.es/emiliolcano/
