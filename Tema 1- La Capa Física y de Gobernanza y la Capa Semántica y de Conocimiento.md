---
tags:
  - op/doc/tool
  - design/IA
  - LIS/informationArchitecture
  - op/doc/curricular
title: Tema 1 - La Capa Física y de Gobernanza y la Capa Semántica y de Conocimiento
Type: Curricular material
source: Material de lectura Asignatura Arquitectura de la Información
pdfORepub: "[[Tema 1- La Capa Física y de Gobernanza y la Capa Semántica y de Conocimiento.pdf]]"
---

[[Tema 1- La Capa Física y de Gobernanza y la Capa Semántica y de Conocimiento.pdf]]
## Full text (extracted from `Tema 1- La Capa Física y de Gobernanza y la Capa Semántica y de Conocimiento.pdf`)

*Source:* `PDF/Tema 1- La Capa Física y de Gobernanza y la Capa Semántica y de Conocimiento.pdf`  
*Extracted:* 2026-04-14

```text
1 
 
Capítulo 2: Componentes, sistemas 
y servicios de la Arquitectura de la 
Información 
Parte 1: La Capa Física y de Gobernanza y la Capa Semántica y de 
Conocimiento  
Versión: 20251005 
Autores: Miquel Centelles y Núria Ferran-Ferrer 
Contenido 
2.1. Introducción ................................................................................................................................................... 3 
2.2. La Capa Física y de Gobernanza ............................................................................................................. 3 
2.2.1. Definición de la Capa Física y de Gobernanza y sus componentes .................................. 3 
2.2.2. Funciones de la Capa Física y de Gobernanza .......................................................................... 4 
2.2.3. Componentes de la Capa Física y de Gobernanza ................................................................... 5 
2.2.3.1. Arquitectura de datos ................................................................................................................  5 
2.2.3.2. Modelado y diseño de datos .................................................................................................... 6 
2.2.3.3. Integración e interoperabilidad de datos .......................................................................... 6 
2.2.3.4. Gestión de documentos y contenidos ................................................................................. 7 
2.2.3.5. Gestión de metadatos ................................................................................................................  7 
2.2.3.6. Calidad de datos ........................................................................................................................... 8 
2.2.4. Relaciones con las capas posteriores ........................................................................................... 8 
2.3. Capa Semántica y de Conocimiento ...................................................................................................... 9 
2.3.1. Definición de la Capa Semántica y de Conocimiento ............................................................. 9 
2.3.2. Funciones de la Capa Semántica y de Conocimiento ............................................................. 9 
2.3.3. Componentes de la Capa Semántica y de Conocimiento ................................................... 11 
2.3.3.1. Categorización de contenidos .............................................................................................. 11 
2.3.3.2. Metadatos y marcado semántico ........................................................................................ 11 
2.3.3.3. Sistemas de Organización del Conocimiento (a partir de ahora, SOC) y 
Representación del Conocimiento ..................................................................................................... 17 
2.3.4. Relaciones con la precedente Capa Física y de Gobernanza y con la posterior Capa 
de Interacción y Experiencia ..................................................................................................................... 22
 
2.3.5. Ejemplos de funcionamiento y uso de los principales tipos de SOC ............................. 23 

2 
 
2.3.5.1. Lista de términos (Term list) ................................................................................................ 23 
2.3.5.2. Esquema de categorización (Categorisation scheme) ................................................. 23 
2.3.5.3. Taxonomía (Taxonomy) ..........................................................................................................  24 
2.3.5.4. Tesauro (Thesaurus) ................................................................................................................  24 
2.3.5.5. Ontología (Ontology) ................................................................................................................  24 
2.3.5.6. Grafo de conocimiento (Knowledge graph) .................................................................... 25 
Declaración sobre IA generativa................................................................................................................... 25 
 
  

3 
 
2.1. Introducción 
La Arquitectura de la Información (a partir de ahora, AI ) es una disciplina que permite a 
las personas encontrar, comprender y usar la información eficazmente. Desde la década de 
1990, dos tradiciones principales han enmarcado la IA. La primera, Information 
Architecture for the World Wide Web , articuló la IA en términos de cuatro sistemas —
organización, etiquetado, navegación y búsqueda— , además de extensiones como ayudas 
para la exploración ( browsing aids), ayudas para la búsqueda ( search aids), contenido y 
tareas, y componentes “invisibles” como vocabularios y metadatos (Rosenfeld, Morville, & 
Arango, 2015). La segunda, surgida del ámbito de la Gestión del Conocimiento (a partir de 
ahora, KM), definió la IA mediante un modelo en capas: física, semántica y de presentación 
que dan soporte a la gobernanza del conocimiento y a la interoperabilidad a escala 
empresarial (EK Team, 2024a; Tesfaye, 2024). 
En este capítulo se emplea el término componentes como descriptor general de los 
distintos bloques que conforman la Arquitectura de la Información. Esta elección refleja la 
diversidad de elementos que constituyen la IA: algunos son mecanismos funcionales 
(como la navegación o la búsqueda), otros son estructuras conceptuales (como las 
taxonomías o los metadatos) y otros son controles infraestructurales (como los 
repositorios y las políticas de acceso). En la tradición de la IA para la Web, a menudo se los 
denominaba sistemas —por ejemplo, el sistema de organización, el sistema de etiquetado, 
el sistema de navegación y el sistema de búsqueda (Rosenfeld, Morville, & Arango, 
2015)—. Aunque esta terminología capta su unidad funcional, no abarca el conjunto más 
amplio de aspectos semánticos y de gobernanza que se enfatizan en la IA basada en KM. 
Por ello, a lo largo de este capítulo se utilizará el término componentes como categoría 
más inclusiva, reconociendo a la vez los sistemas como un tipo específico de componente 
enraizado en la tradición de la IA para la Web. 
Este capítulo propone un nuevo Modelo de Tres Capas de Arquitectura de la Información, 
que integra ambas tradiciones en un marco coherente. Reinterpreta el modelo basado en 
KM y lo alinea con los componentes de la IA para la Web, añadiendo a la vez énfasis en 
gobernanza, semántica y experiencia. Las tres capas son: 
• Capa Física y de Gobernanza 
• Capa Semántica y de Conocimiento 
• Capa de Interacción y Experiencia 
En este tema, abordaremos los dos primeros. En el Tema 3 abordaremos la Capa de 
Interacción y Experiencia 
2.2. La Capa Física y de Gobernanza 
2.2.1. Definición de la Capa Física y de Gobernanza y sus 
componentes 
La Capa Física y de Gobernanza constituye la base de una arquitectura de la información 
en tres capas. Integra la infraestructura técnica para almacenar, estructurar y procesar 

4 
 
datos con los mecanismos de gobernanza que garantizan su calidad, accesibilidad y 
cumplimiento. 
En su dimensión física , esta capa abarca repositorios, bases de datos, almacenes de datos 
(data warehouses), lagos de datos ( lakehouse de datos ) y, más recientemente, tejidos de 
datos (data fabrics), así como diversas técnicas de modelado —entidad–relación, grafos y 
orientadas a documentos— que estructuran los datos de la organización. 
La dimensión de gobernanza establece las reglas, estándares, prácticas de data 
stewardship y políticas que aseguran que los datos se utilicen de forma ética, legal y 
estratégica. Junior et al. (2023) describen la Gobernanza de Datos como los esfuerzos para 
crear soporte estructural, consistencia y equilibrio mediante actividades de gestión de 
datos. Ayuda a las organizaciones a gestionar sus activos de información y a responder 
preguntas como: (i) ¿Qué necesitamos saber sobre estos datos? (ii) ¿Qué necesitamos 
hacer con estos datos? (iii) ¿Qué políticas y reglas rigen estos datos? 
Helbig et al. (2012) sostienen que la gobernanza de datos proporciona un enfoque integral 
para gestionar la creación, mejora y uso de los datos, aumentando así la eficiencia de la 
gestión de datos. 
Según el Data Governance Institute https://datagovernance.com (a partir de ahora, DGI), 
la gobernanza de datos es un marco de toma de decisiones y un conjunto de 
responsabilidades para los procesos relacionados con los datos, basado en políticas, 
estándares y limitaciones. Las actividades de gobernanza de datos pueden centrarse en 
cuestiones que van desde la privacidad hasta la calidad y abarcan todo el ciclo de vida del 
dato. Para implantar un programa estructurado y eficaz, las organizaciones deben definir 
sus necesidades y objetivos de gestión de datos y, a continuación, delimitar su alcance, con 
independencia del foco y la escala establecidos por la organización. 
Al unir estos dos aspectos, la Capa Física y de Gobernanza actúa tanto como sustrato 
técnico como marco regulador sobre el que se construyen las capas posteriores —la Capa 
Semántica y de Conocimiento y la Capa de Interacción y Experiencia—. 
2.2.2. Funciones de la Capa Física y de Gobernanza 
Esta capa desempeña varias funciones interrelacionadas esenciales para la sostenibilidad 
de las arquitecturas de la información. 
En el plano técnico, garantiza la disponibilidad, accesibilidad y fiabilidad de los datos 
en múltiples sistemas. Sus infraestructuras proporcionan escalabilidad tanto para 
contenidos estructurados como no estructurados, permitiendo a las organizaciones 
integrar fuentes diversas como colecciones culturales, datos de salud y aplicaciones 
empresariales. 
En el plano de gobernanza, impone protección de datos, cumplimiento y 
responsabilidad. Marcos como ISO 8000 y Basel Committee on Banking Supervision 239 
(a partir de ahora, BCBS 239) articulan cómo deben mantenerse la precisión, la 
puntualidad y la integridad para satisfacer requisitos regulatorios. Del mismo modo, los 
mecanismos de gobernanza gestionan derechos de autorización ( entitlements) y de 

5 
 
acceso, abordando vulnerabilidades que surgen cuando personas y sistemas comparten 
recursos de datos distribuidos (Hilger 2025). 
De forma crucial, la Capa Física y de Gobernanza proporciona el sustrato escalable  
necesario para el modelado semántico y las aplicaciones impulsadas por inteligencia 
artificial (a partir de ahora, AI), garantizando que los análisis a gran escala, el aprendizaje 
automático (machine learning) y los modelos generativos se apoyen en una base confiable 
y bien regulada (Garcia 2025). 
2.2.3. Componentes de la Capa Física y de Gobernanza 
La gestión de datos dentro de la Capa Física y de Gobernanza se entiende mejor a través de 
la rueda del Cuerpo de Conocimiento de Gestión de Datos de DAMA  (Data 
Management Body of Knowledge, a partir de ahora, DMBOK), que identifica una serie de 
componentes, o áreas funcionales, que sustentan el uso eficaz de la información. De 
especial relevancia para las capas posteriores de la arquitectura de la información son la 
arquitectura de datos, el modelado y diseño de datos, la integración e 
interoperabilidad de datos, la gestión de documentos y contenidos, los metadatos y 
la calidad de los datos (DAMA International, 2017; Van Gils, 2023). 
2.2.3.1. Arquitectura de datos 
La arquitectura de datos (incluidas las infraestructuras de almacenamiento) proporciona 
el plano general de cómo se almacenan, procesan y gobiernan los activos de datos. Su 
función es garantizar que el entorno técnico se alinea con las necesidades del negocio, 
apoyando la interoperabilidad con las capas semántica y de interacción  (Acceldata, 2025; 
Instaclustr, 2025). 
Dentro de la Capa Física, varios tipos de fuentes de datos sustentan los sistemas de 
información empresariales. Los almacenes de datos son repositorios estructurados como 
las bases de datos relacionales, diseñados para la recuperación eficiente y la consistencia 
transaccional (Hechler et al., 2020) . Los repositorios de contenidos  gestionan activos 
digitales no estructurados, permitiendo su búsqueda y reutilización  (Majumder, 2025) . 
Las bases de conocimiento proporcionan modelos de información curados e 
interconectados, a menudo materializados mediante grafos de conocimiento para apoyar 
la AI y la transformación digital  (Tesfaye, 2022a). Los sistemas de ficheros (file systems) 
organizan el almacenamiento jerárquico de ficheros, formando típicamente la base de los 
repositorios de contenido  (Hechler et al., 2020) . Los sistemas de control de acceso  
regulan permisos , aunque se han identificado derechos unificados ( unified entitlements) 
como una “vulnerabilidad oculta” en las empresas (Hilger & Hughes, 2025). Los lagos de 
datos (data lakes) almacenan datos en bruto y heterogéneos para análisis flexibles  (The 
Learning Strategist, 2025). Por último, los tejidos de datos (data fabrics) integran fuentes 
dispares mediante una capa semántica y arquitectónica, como se observa en evaluaciones 
del sector farmacéutico (EK Team, 2024a). 
Los estudios de caso ilustran estas cuestiones en la práctica: empresas minoristas que 
mejoran la analítica mediante tejidos de datos habilitados semánticamente (Tesfaye, 
2025b) y organizaciones que adoptan grafos de conocimiento para actualizar taxonomías 

6 
 
(EK Team, 2019). En conjunto, estos activos físicos forman la columna vertebral de los 
ecosistemas de datos empresariales. 
• Definición: El plano estructurado del entorno de datos de una organización (Van 
Gils, 2023). 
• Función: Alinea las infraestructuras de datos con los objetivos del negocio. 
• Componentes principales: Bases de datos, almacenes, lagos de datos y tejidos 
(Acceldata, 2025). 
• Relación: Proporciona la base para el enlace semántico y la accesibilidad para las 
personas usuarias (Instaclustr, 2025). 
• Ejemplo: Adopción empresarial de tejidos de datos híbridos para la 
interoperabilidad a escala. 
2.2.3.2. Modelado y diseño de datos 
Íntimamente relacionado, el modelado y diseño de datos  traduce la arquitectura en 
representaciones formales como diagramas entidad –relación o modelos de grafo, 
habilitando la interpretación consistente en aplicaciones semánticas. 
La Capa Física y de Gobernanza alberga una pluralidad de modelos de datos, cada uno de 
los cuales interactúa de manera diferente con los requisitos de gobernanza.  
• Los modelos relacionales dominan las aplicaciones financieras y gubernamentales, 
donde la consistencia y la integridad son primordiales.  
• Los modelos de grafo, por el contrario, facilitan la representación de relaciones en 
redes sociales, taxonomías y ontologías (EK Team 2019; Tesfaye 2022a).  
• Los modelos dimensionales sustentan la inteligencia de negocio ( business 
intelligence, a partir de ahora, BI) y los almacenes de datos, optimizados para 
consultas analíticas.  
• Los enfoques híbridos, como el lakehouse de datos, combinan la flexibilidad de los 
lagos con la gobernanza de los almacenes. 
La elección del modelo no es puramente técnica, sino una cuestión de gobernanza: alinear 
el modelo con los objetivos de la organización, las obligaciones de cumplimiento y los usos 
previstos de los datos. 
• Definición: La práctica de crear representaciones formales de datos. 
• Función: Permite la interpretación consistente de las estructuras de datos. 
• Componentes principales: Modelos entidad–relación, modelos de grafo, etc. 
• Relación: Da soporte directo a ontologías y taxonomías en la Capa Semántica. 
• Ejemplo: Modelado dimensional en BI que habilita cuadros de mando analíticos. 
2.2.3.3. Integración e interoperabilidad de datos 
La integración e interoperabilidad de datos se centran en unificar fuentes heterogéneas 
mediante procesos como ETL (extracción, transformación y carga) y ELT (extracción, 
carga y transformación), y la integración de aplicaciones empresariales, cada vez más 
potenciadas por la orquestación basada en AI (Amįń, 2025). Estos procesos crean las 
canalizaciones que permiten a las capas semánticas acceder a conjuntos de datos 

7 
 
armonizados y que garantizan que las personas usuarias encuentren experiencias de 
información sin fricciones. 
• Definición: La consolidación de fuentes heterogéneas en conjuntos de datos 
unificados. 
• Función: Garantiza que los datos sean accesibles y consistentes en las plataformas.  
Componentes principales: Canalizaciones ETL/ELT, integración de aplicaciones 
empresariales. 
• Relación: Suministra conjuntos de datos armonizados a los sistemas semánticos y a 
las interfaces de interacción (Amįń, 2025). 
• Ejemplo: Canalizaciones ELT con AI que reducen la latencia en servicios 
financieros. 
2.2.3.4. Gestión de documentos y contenidos 
La gestión de documentos y contenidos amplía la gobernanza más allá de las bases de 
datos estructuradas para incluir recursos no estructurados como informes, multimedia y 
contenido colaborativo. Esta área funcional proporciona un control esencial sobre la 
información que a menudo se consume directamente en la capa de interacción  (DAMA, 
2017). 
• Definición: Gobernanza del contenido no estructurado y semiestructurado.  
Función: Proporciona control a escala de organización sobre documentos y 
medios. 
• Componentes principales: Repositorios de contenido, controles de acceso, políticas 
de retención. 
• Relación: Garantiza que el contenido no estructurado pueda clasificarse 
semánticamente y recuperarse en las interfaces de usuario (DAMA, 2017). 
• Ejemplo: Intranets corporativas con clasificación automática de documentos. 
2.2.3.5. Gestión de metadatos 
Los metadatos son “datos sobre datos”, que describen los recursos para que puedan 
descubrirse, gestionarse y preservarse (Gilliland, 2016). La gestión de metadatos es el 
tejido conectivo de la gestión de datos, al proporcionar información descriptiva, 
estructural y administrativa que hace que los activos sean localizables, interoperables y 
reutilizables (Khairunisak et al., 2021). Al sustentar ontologías y taxonomías, los 
metadatos crean el puente entre los repositorios físicos y el enriquecimiento semántico. 
Dentro de la Capa Física y de Gobernanza, los metadatos surgen como parte de flujos de 
trabajo de ingestión, almacenamiento y control que establecen procedencia, calidad y 
restricciones de acceso. En arquitecturas de lago de datos ( data-lake architectures), los 
canales ( pipelines) generan metadatos operativos durante la carga para que los activos 
puedan validarse y gobernarse; como explican Sawadogo y Darmont, “se realizan 
comprobaciones básicas de calidad de datos” y las zonas de almacenamiento conservan 
información depurada y estandarizada para apoyar la gobernanza (2021, p. 99). Estos 
registros descriptivos se consolidan después en catálogos empresariales para garantizar la 
capacidad de descubrimiento y el cumplimiento de políticas. En términos prácticos, las 
organizaciones primero “Describir, Estandarizar y Catalogar” los activos de datos cuando 

8 
 
entran en entornos gestionados (Nash & Hilger, 2024, diapositiva 15). Por ejemplo, 
cuando se ingiere un conjunto de datos de productos, los campos capturados por sistema 
(nombre del conjunto de datos, fecha de creación, estructura de archivos, titularidad) se 
registran en el catálogo, formando la base para el control del ciclo de vida, la auditabilidad 
y el uso posterior. 
• Definición: Datos que describen datos, incluidos elementos descriptivos, 
estructurales y administrativos. 
• Función: Facilita el descubrimiento, la interoperabilidad y el cumplimiento. 
• Componentes principales: Estándares de metadatos, catálogos, ontologías. 
• Relación: Permite el enriquecimiento semántico y la recuperación contextual entre 
capas (Khairunisak et al., 2021). 
• Ejemplo: Catálogos de datos impulsados por metadatos que apoyan la búsqueda 
empresarial. 
2.2.3.6. Calidad de datos 
Por último, la calidad de los datos asegura que la información sea precisa, consistente, 
completa y oportuna. Marcos como ISO 8000 y TDQM formalizan estas dimensiones, 
mientras que los enfoques contextuales las adaptan a los objetivos de la organización 
(Amine, 2025; Cichy & Rass, 2019; Miller et al., 2025). La mala calidad de los datos socava 
rápidamente la coherencia semántica y la confianza de las personas usuarias, ya sea en BI 
o en servicios dirigidos a la ciudadanía (Earley, 2024; Madera & Laurent, 2016). 
• Definición: La idoneidad de los datos para su propósito, medida a través de 
múltiples dimensiones. 
• Función: Garantiza la fiabilidad en la toma de decisiones y la confianza del usuario.  
Componentes principales: Precisión, completitud, puntualidad, consistencia; 
marcos como ISO 8000 y TDQM. 
• Relación: Los datos de alta calidad respaldan la precisión semántica y experiencias 
de usuario confiables (Amine, 2025; Cichy & Rass, 2019; Miller et al., 2025). 
• Ejemplo: Iniciativas de calidad de datos en salud que evitan condiciones de 
“pantano de datos” (data swamp s) en lagos de datos ( data lakes ) (Madera & 
Laurent, 2016). Un data swamp  es la degradación de un lago de datos  cuando 
acumula datos crudos sin gobierno, calidad ni metadatos; el repositorio se vuelve 
opaco, inseguro e inutilizable. Sin un catálogo de metadatos y controles (calidad, 
seguridad, ciclo de vida), el lago deriva en pantano, por lo que se recomienda 
gobernarlo para evitarlo. Ejemplo: un lago de datos en Apache Hadoop que ingiere 
logs, sensores y correos sin linaje; se duplican datos sensibles y nadie sabe en qué 
confiar o cómo reutilizarlos.  
En conjunto, estas seis áreas garantizan que la Capa Física y de Gobernanza proporcione 
no solo una infraestructura robusta, sino también un entorno gobernado capaz de apoyar 
la coherencia semántica de la Capa 2 y la usabilidad de la Capa 3. 
2.2.4. Relaciones con las capas posteriores 
La Capa Física y de Gobernanza no es autosuficiente: su eficacia radica en habilitar las 
capas superiores de la arquitectura. 

9 
 
• Con la Capa Semántica y de Conocimiento, el almacenamiento físico proporciona la 
materia prima para el enriquecimiento semántico. La gobernanza asegura la 
alineación con ontologías, grafos de conocimiento y principios Findable, Accessible, 
Interoperable, Reusable https://www.go-fair.org/fair-principles (a partir de ahora, 
FAIR), posibilitando así la interoperabilidad y la reutilización. 
• Con la Capa de Interacción y Experiencia, los mecanismos de gobernanza y calidad 
sustentan los sistemas orientados a la persona usuaria. La confianza en los 
servicios digitales depende de la confianza en los cimientos físicos y de 
gobernanza; una gobernanza deficiente conduce a desinformación, falta de 
fiabilidad y, en última instancia, a una experiencia degradada. 
2.3. Capa Semántica y de Conocimiento 
2.3.1. Definición de la Capa Semántica y de Conocimiento 
La Capa Semántica y de Conocimiento se refiere al nivel de la arquitectura de la 
información que aporta significado, estructura y relaciones a los datos, posibilitando así la 
interpretación consistente entre sistemas y personas usuarias. Como explica Tesfaye 
(2024), una capa semántica es “un marco estandarizado que organiza y abstrae los datos 
del negocio en términos comunes y reutilizables comprensibles para el negocio”, 
garantizando que la información no solo se almacene, sino que también se contextualice 
para su uso eficaz. En el Modelo de Tres Capas de Arquitectura de la Información, esta 
capa media entre la Capa Física y de Gobernanza (donde se almacenan y protegen la 
información) y la Capa de Interacción y Experiencia (donde las personas acceden a ella e 
interactúan). 
2.3.2. Funciones de la Capa Semántica y de Conocimiento 
La Capa Semántica y de Conocimiento funciona como el núcleo de inteligencia de la 
arquitectura moderna de la información, proporcionando el puente conceptual entre los 
datos estructurados y el conocimiento significativo. Establece los vocabularios 
compartidos, las relaciones de datos y los mecanismos de gobernanza que permiten que 
personas y sistemas interactúen con la información de forma coherente. Como explica 
Tesfaye (2024), la capa semántica “actúa como una vista unificada del negocio sobre los 
datos de la empresa”, permitiendo a las organizaciones “consultar, analizar y visualizar la 
información de manera consistente entre herramientas y equipos”. Conecta así activos de 
datos heterogéneos con la comprensión humana y de máquina. 
Una función principal de esta capa es la mediación y abstracción semántica. Introduce 
vocabularios de negocio y de dominio —taxonomías, tesauros, ontologías y grafos de 
conocimiento, que posteriormente agruparemos bajo la categoría de sistemas de 
organización del conocimiento  o SOC — que normalizan el lenguaje a través de 
departamentos y tecnologías (EK Team, 2024b). Estos vocabularios garantizan que, 
cuando una analista de marketing busca “engagement de clientes”, o una científica de 
datos modela “eventos de conversión”, ambas estén ancladas al mismo concepto. Esta 
alineación semántica respalda la encontrabilidad ( findability), la interoperabilidad y la 
reutilización —objetivos también enfatizados en la arquitectura de la información 

10 
 
tradicional basada en la Web —. Rosenfeld, Morville y Arango (2015) señalan que “los 
metadatos y los vocabularios controlados conectan los elementos de contenido a través 
del significado más que de la ubicación” (p. 178), un principio que escala sin fisuras hacia 
la capa semántica empresarial. 
La Capa Semántica y de Conocimiento también sostiene la gobernanza y la data 
stewardship. EK Team (2024b) subraya que las estructuras semánticas proporcionan “una 
base para la gobernanza de datos y la gestión del conocimiento”, asegurando calidad, 
consistencia y trazabilidad entre sistemas. Nash (2024) detalla que las capas semánticas 
“crean una única fuente gobernada de métricas”, permitiendo a las organizaciones 
gestionar la lógica de negocio de forma centralizada a la vez que la exponen en formatos 
amigables para el usuario. Las funciones de gobernanza son, por tanto, tanto técnicas 
como organizativas: integran políticas de datos, definen roles de tutela y documentan 
modelos semánticos, alineando el lenguaje de los datos con el lenguaje del negocio. 
Otra función clave es la habilitación de analítica, inteligencia de negocio (BI) e inteligencia 
artificial (AI/ML). Las capas semánticas y de conocimiento suministran contexto 
interpretable por máquinas — mediante metadatos, relaciones entre entidades y 
jerarquías taxonómicas— que enriquecen los modelos de AI predictiva y generativa. Según 
EK Team (2024a), diseñar la IA para la AI requiere “capas de conocimiento estructurado 
que entrenen, informen y gobiernen los sistemas inteligentes”. En la práctica, esto implica 
incorporar modelos ontológicos a las canalizaciones de datos, mapear categorías humanas 
a características algorítmicas y asegurar que las salidas de la AI sigan siendo explicables y 
consistentes con la terminología de la empresa. 
La capa también sustenta la experiencia de usuario y el descubrimiento. Al proporcionar 
una columna vertebral semántica unificada, soporta sistemas de búsqueda, exploración y 
recomendación conscientes del contexto que trascienden la simple coincidencia de 
palabras clave. Tesfaye (2024) señala que las capas semánticas “sacan a la superficie la 
información adecuada en el momento adecuado” al inferir intención y relevancia. Esta 
función refleja la noción de Rosenfeld et al. (2015) de “estructuras invisibles” que dan 
forma a cómo las personas encuentran e interpretan el contenido, incluso cuando no son 
conscientes de la arquitectura subyacente (p. 93). Ya sea mediante navegación impulsada 
por taxonomías , orientación ( wayfinding) o recomendaciones inteligentes, la capa 
operacionaliza el significado para mejorar la accesibilidad y la satisfacción. 
En suma, la Capa Semántica y de Conocimiento transforma datos desconectados en un 
entorno de conocimiento gobernado, interpretable y accionable. Sus funciones —
mediación semántica, gobernanza, habilitación analítica y localización centrada en la 
persona usuaria— amplían los principios de la arquitectura de la información tradicional 
en la Web hacia un ecosistema empresarial, preparado para la AI. Como concluye EK Team 
(2024a), una arquitectura semántica eficaz “t iende puentes entre lo humano y la 
máquina”, asegurando que los sistemas de información sean a la vez inteligibles e 
inteligentes. 

11 
 
2.3.3. Componentes de la Capa Semántica y de Conocimiento 
2.3.3.1. Categorización de contenidos 
La categorización de contenidos es el proceso de agrupar y etiquetar la información para 
que las personas usuarias puedan reconocerla, explorarla y recuperarla con significado. 
Martin (2019) señala que las categorías “son herramientas para la construcción de 
sentido” que estructuran la información en agrupaciones reconocibles (pp. 36 –37). Una 
categorización eficaz se apoya en principios de claridad, consistencia y exclusividad 
mutua: las categorías deben ser “claras, estables y útiles”, evitando solapamientos 
innecesarios (Gabriel -Petit & Kalbach, 2025, p. 216). Los objetivos de categorizar la 
información incluyen apoyar la recuperación, reducir la carga cognitiva y habilitar el 
entendimiento compartido; como observan las autoras, la clasificación busca “encontrar, 
conectar y dar sentido a la información” (Gabriel-Petit & Kalbach, 2025, p. 217). 
A menudo surgen retos cuando las categorías son ambiguas, están culturalmente sesgadas 
o no reflejan las expectativas de las personas usuarias. Gabriel -Petit y Kalbach (2025) 
destacan la dificultad de categorizar los géneros musicales, donde las personas pueden 
discrepar sobre si “jazz fusión” pertenece a jazz o a rock (pp. 218 –219). Del mismo modo, 
Martin (2019) advierte contra etiquetas demasiado amplias (“miscelánea”) o demasiado 
específicas, que perjudican la usabilidad (pp. 44–45). 
Así, la categorización proporciona la base sobre la cual operan los metadatos y el marcado 
semántico. Las categorías definen los contenedores conceptuales en los que se asignan los 
valores de metadatos, mientras que el marcado semántico extiende estas clasificaciones a 
estructuras legibles por máquina que apoyan la interoperabilidad y la búsqueda. 
2.3.3.2. Metadatos y marcado semántico 
Retomamos el concepto de metadatos introducido en la Capa Física y de Gobernanza. Los 
metadatos operan en los ámbitos descriptivo (título, autoría…), estructural (relaciones 
entre partes), administrativo (derechos, procedencia…) y técnico (tipo de archivo, 
formato…) (Hider, 2018, pp. 23 –24). En la práctica, suelen residir en sistemas de gestión 
de contenidos ( content management systems , en adelante CMS), sistemas de gestión de 
información de producto ( product information management, en adelante PIM) o sistemas 
de gestión de activos digitales ( digital asset management, en adelante DAM). En cuanto a 
su ubicación en entornos digitales, pueden estar incrustados en los archivos, vinculados 
externamente o almacenados a nivel de página web y de componente (Rosenfeld, Morville 
& Arango, 2015, pp. 191–192). 
Su función va más allá de describir: los metadatos constituyen la columna vertebral de la 
gobernanza de la información, la interoperabilidad entre sistemas y la preservación digital 
sostenible (Dumer, Sousa & Albuquerque, 2019, p. 65). Arango (2023) subraya que los 
metadatos son “críticos para el diseño digital”, porque sostienen tanto la usabilidad como 
la accesibilidad. También resultan esenciales para la búsqueda y la recuperación. Korobka 
(2023) destaca su contribución al posicionamiento en buscadores (SEO), al observar que 
unos metadatos claros “mejoran la visibilidad en los rankings de búsqueda” (párr. 4). 
Además, respaldan una categorización consistente mediante los sistemas de organización 
del conocimiento (SOC), que analizaremos más adelante, garantizando que valores como 

12 
 
los nombres de autoría o los encabezamientos de materia se estandaricen entre sistemas 
(Gabriel-Petit & Kalbach, 2025, pp. 228–229).  
La expresión de los metadatos se apoya en cuatro tipos de estándares, recogidos en la 
Tabla 2.1. 
Tipo de estándar de metadatos Ejemplo 
Estándares de estructura de 
datos ( data structure standards ): 
conjuntos de elementos ( schemas) 
que actúan como “categorías” o 
“contenedores” de datos para un 
registro u objeto informacional. 
Dublin Core Metadata Element Set  
https://www.dublincore.org/specifications/dublin-
core/dces 
Estándares de valores de datos 
(data value standards ), basados 
en sistemas de organización del 
conocimiento (KOS): términos, 
nombres y otros valores usados 
para poblar los estándares de 
estructura de datos. 
• Taxonomy: Amazon Product Taxonomy 
https://www.amazon.es 
• Thesaurus: UNESCO Thesaurus 
https://unesdoc.unesco.org 
• Ontology: Schema.org https://schema.org 
• Knowledge graph : Wikidata 
https://www.wikidata.org/?uselang=es 
Estándares de contenido de datos 
(data content standards): reglas y 
códigos de catalogación que 
especifican el formato y la sintaxis 
de los valores de datos usados en 
los elementos de metadatos. 
Resource Description and Access ; International 
Standard Bibliographic Description 
Estándares de 
formato/intercambio técnico de 
datos ( data format/technical 
interchange standards ): 
estándares de metadatos en forma 
legible por máquina, a menudo 
materializaciones de un estándar de 
estructura de datos, codificados o 
marcados para su procesamiento 
automático. 
• Etiquetas meta en HTML. 
• Formatos de datos estructurados: JSON -LD, 
RDFa o microdatos. 
Tabla 1: Tipos de estándares de metadatos y ejemplos 
Los estándares de estructura de datos ( data structure standards ) determinan cómo se 
expresan los metadatos. Conjuntos como Dublin Core  ofrecen “contenedores” 
consensuados para describir recursos (Dumer et al., 2019, p. 65). De forma 
complementaria, los estándares de valores de datos ( data value standards) —esto es, los 
sistemas de organización del conocimiento— garantizan entradas uniformes (Rosenfeld et 
al., 2015, p. 191). Esta doble base permite que los metadatos funcionen como puente entre 
el contenido bruto y los modelos semánticos de nivel superior. Por ejemplo, Nash y Hilger 
(2024) muestran que las capas semánticas dependen de los metadatos para “describir, 
estandarizar [y] catalogar” conjuntos de datos (diapositiva 15), habilitando un acceso y 
una gobernanza unificados en la organización. En síntesis, los metadatos aportan la base 
descriptiva y estructural sobre la que se construye el marcado semántico para la Capa 
Semántica y de Conocimiento, a partir de la cual es posible una interpretación consistente 
entre equipos y sistemas.  

13 
 
Pasemos ahora a los estándares de formato/intercambio técnico de datos ( data 
format/technical interchange standards) aplicados a espacios digitales. Aunque a menudo 
se emplean como sinónimos, metadatos  y marcado semántico (datos estructurados)  
cumplen funciones complementarias: los primeros describen y gestionan el recurso 
dentro de sistemas editoriales y de gobernanza, mientras que el segundo expone ese 
significado a las máquinas (por ejemplo, motores de búsqueda) con vocabularios 
normalizados. En conjunto, mejoran simultáneamente la calidad interna y la capacidad de 
descubrimiento externa del contenido. 
2.3.3.2.1. Metadatos 
En este contexto, metadatos  se refiere a la información sobre la propia página web , 
como el título, la descripción y las palabras clave. Esta información no es visible para los 
usuarios, pero resulta esencial para que los motores de búsqueda comprendan de qué 
trata la página y la clasifiquen correctamente en los resultados. 
Ejemplo 1 — Metadatos en HTML (cabecera de una página comercial en español)  
Qué muestra:  título de la página, descripción orientada a buscadores, palabras clave y 
etiquetas Open Graph básicas para compartir en redes. 
URL: Apple iPhone 15 móvil libre — El Corte Inglés 
https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-movil-
libre/?utm_source=chatgpt.com. 
<head> 
  <title>Apple iPhone 15 móvil libre · Apple · El Corte Inglés</title> 
  <meta name="description" content="Compra online el Apple iPhone 15 móvil 
libre en El Corte Inglés. Características, colores y envío a domicilio."> 
  <meta name="keywords" content="iPhone 15, Apple, móvil libre, smartphone, El 
Corte Inglés"> 
  <meta property="og:type" content="product"> 
  <meta property="og:title" content="Apple iPhone 15 móvil libre"> 
  <meta property="og:url" 
content="https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-
movil-libre/"> 
  <meta property="og:site_name" content="El Corte Inglés"> 
  <meta property="og:locale" content="es_ES"> 
</head> 
 
Beneficios del uso de metadatos en páginas web (síntesis aplicada a la página del 
ejemplo) 

14 
 
Descubribilidad y comprensión básica del contenido. Los metadatos aportan un 
resumen fiable de la página para sistemas de terceros; al hacer legible para las máquinas 
el significado y el contexto, se mejora la interoperabilidad. Ejemplo: en la ficha del 
iPhone 15, el <title> y la <meta name="description"> alimentan el snippet y el share social.  
Interoperabilidad entre sistemas (CMS/PIM/DAM) y la capa web.  Metadatos 
coherentes conectan las capas internas con la representación en la página , reduciendo 
duplicidades. Ejemplo: el “nombre de producto” y la “categoría” del PIM se reflejan en 
og:title y se reaprovechan en Product.name y category. Hallazgo empírico relacionado : la 
robustez del marcado y los metadatos  se asocia fuertemente al CMS usado (en su 
muestra, ≈80 % de los atributos coincidían para un mismo CMS, independientemente del 
editor) (Ivancsics et al., 2023).  
Gobernanza y consistencia (evitar data swamps ). La gestión de metadatos es 
primordial para que repositorios grandes sigan siendo explotables. Ejemplo : estandarizar 
“Móviles y smartphones” en metadatos y en BreadcrumbList evita ambigüedades.  
Soporte a preservación, trazabilidad y derechos.  Metadatos administrativos (origen, 
derechos) facilitan el control del ciclo de vida y el reúso responsable. 
SEO on-page básico (títulos y descripciones claros). Una redacción precisa de <title> y 
<meta name="description"> mejora la pertinencia percibida y puede impactar en el CTR. 
Puente hacia el marcado semántico.  Los metadatos proporcionan la base descriptiva 
para exponer el significado con datos estructurados (Schema.org); formatos como JSON -
LD son preferidos por buscadores y evitan romper la maquetación al no interactuar con el 
HTML (Bell, 2018).  
2.3.3.2.2. Marcado semántico (datos estructurados) 
El marcado semántico hace explícitos los metadatos para las máquinas al incrustarlos en 
los contenidos de una página web , habitualmente mediante vocabularios de Schema.org  
en JSON -LD, RDFa o microdatos. Mientras que los metadatos en los CMS ayudan a la 
gestión interna, el marcado semántico comunica el significado del recurso a sistemas 
externos como los motores de búsqueda. Los datos estructurados ayudan a los buscadores 
a comprender mejor el contenido de una página : aportan información sobre su contexto 
—tipo de contenido, autor, fecha, etc. — y facilitan ofrecer resultados más exactos y 
pertinentes. 
A continuación, se muestran dos codificaciones del mismo recurso indicado en el 
Ejemplo 1  (mismo URL), una en JSON -LD y otra en microdatos, que ilustran cómo se 
declara el tipo de contenido (producto) y cómo se modela la jerarquía de navegación 
(migas de pan). 
Ejemplo 2a — Datos estructurados en JSON -LD (Schema.org/Product)  
Qué muestra: el tipo Product con sus propiedades esenciales (nombre, marca, categoría, 
identificador, URL, imagen y oferta). Se utiliza para que buscadores y asistentes 
comprendan que se trata de una página de producto concreta.  
URL: Apple iPhone 15 móvil libre — El Corte Inglés 

15 
 
https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-movil-
libre/?utm_source=chatgpt.com. 
<script type="application/ld+json"> 
{ 
  "@context": "https://schema.org", 
  "@type": "Product", 
  "name": "Apple iPhone 15 móvil libre", 
  "brand": { "@type": "Brand", "name": "Apple" }, 
  "category": "Móviles y smartphones", 
  "sku": "001094612201122", 
  "url": "https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-
movil-libre/", 
  "image": [ 
    "https://www.elcorteingles.es/electronica/medias/imagen-iphone15-rosa-
1.jpg" 
  ], 
  "offers": { 
    "@type": "Offer", 
    "priceCurrency": "EUR", 
    "availability": "https://schema.org/InStock", 
    "url": "https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-
movil-libre/" 
  } 
} 
</script> 
 
Ejemplo 2b — Microdatos (Schema.org/BreadcrumbList)  
Qué muestra: la ruta de navegación de la página (BreadcrumbList), útil para representar la 
jerarquía “Electrónica → Móviles y smartphones → Producto”, lo que mejora la 
comprensión del contexto y puede habilitar rich snippets  de migas de pan. (Véase la 
definición oficial de BreadcrumbList en Schema.org). 

16 
 
<nav aria-label="miga de pan" itemscope 
itemtype="https://schema.org/BreadcrumbList"> 
  <ol> 
    <li itemprop="itemListElement" itemscope 
itemtype="https://schema.org/ListItem"> 
      <a itemprop="item" href="https://www.elcorteingles.es/electronica/"> 
        <span itemprop="name">Electrónica</span> 
      </a> 
      <meta itemprop="position" content="1"> 
    </li> 
    <li itemprop="itemListElement" itemscope 
itemtype="https://schema.org/ListItem"> 
      <a itemprop="item" href="https://www.elcorteingles.es/electronica/moviles-y-
smartphones/"> 
        <span itemprop="name">Móviles y smartphones</span> 
      </a> 
      <meta itemprop="position" content="2"> 
    </li> 
    <li itemprop="itemListElement" itemscope 
itemtype="https://schema.org/ListItem"> 
      <a itemprop="item" 
href="https://www.elcorteingles.es/electronica/A49247158-apple-iphone-15-
movil-libre/"> 
        <span itemprop="name">Apple iPhone 15 móvil libre</span> 
      </a> 
      <meta itemprop="position" content="3"> 
    </li> 
  </ol> 
</nav> 
 
 

17 
 
Beneficios del uso de datos estructurados (marcado semántico) en páginas web 
(síntesis aplicada a la página del ejemplo) 
Desambiguación de la entidad y mejor comprensión por buscadores. Declarar @type: 
Product con brand, sku, offers deja inequívoco el tipo de página . Fundamento: hacer 
legible a máquina el significado y el contexto mejora la interoperabilidad (Bell, 2018, p. 
102).  
Resultados enriquecidos ( rich results ) y mayor visibilidad.  El marcado adecuado 
puede habilitar migas de pan, precio y disponibilidad; JSON -LD se inserta sin interferir 
con el HTML (ventaja operativa frente a microdatos mal anidados) (Bell, 2018).  
Infraestructura de visibilidad en plataformas.  El marcado y los metadatos constituyen 
una “infraestructura de visibilidad” que hace accesibles —o invisibles— contenidos en 
la economía de plataformas.  
Interoperabilidad y reutilización semántica (asistentes, agregadores).  Los datos 
estructurados pueden ser consumidos por asistentes y agregadores; el principio es el 
mismo: expresar el contexto de forma legible por máquina para múltiples servicios (Bell, 
2018).  
Construcción y enriquecimiento de grafos de conocimiento.  El marcado puede 
alimentar grafos propios y abiertos; en turismo, microdatos + LLMs  ayudan a 
complementar y vincular con Wikidata (metodología y hallazgos) (Gonzalez -Garcia et al., 
2024).  
Estandarización transversal del ecosistema web. Schema.org actúa como “regulador y 
guardián (gatekeeper) de datos en la Web” , con implicaciones para la visibilidad y la 
representación en buscadores (Iliadis et al., 2025, p. 514).  
Calidad operativa y mantenimiento. Aplicar Schema.org incorrectamente puede inducir 
a error; las guías y vocabularios cambian con el tiempo, por lo que conviene planificar 
mantenimiento periódico del marcado (Ivancsics et al., 2023). 
Metadatos y marcado semántico están estrechamente ligados a la categorización. Las 
categorías establecidas en el diseño de información se mapean directamente a campos de 
metadatos (por ejemplo, “género” o “tema”) y a propiedades de esquemas (por ejemplo, 
articleSection en Schema.org). Esta integración apunta hacia los sistemas de organización 
y representación del conocimiento, donde los estándares de metadatos y los vocabularios 
de esquemas se alinean con taxonomías, tesauros, ontologías y grafos de conocimiento. 
2.3.3.3. Sistemas de Organización del Conocimiento (a partir de ahora, 
SOC) y Representación del Conocimiento 
La Organización del Conocimiento ( knowledge organisation, a partir de ahora, KO) y la 
Representación del Conocimiento ( knowledge representation , a partir de ahora, KR) 
constituyen la base conceptual y operativa de la Capa Semántica y de Conocimiento. 
Determinan cómo se estructura, relaciona y expresa la información —primero para la 
construcción de sentido humana y después para el razonamiento computacional y la 

18 
 
interoperabilidad—. Juntas aseguran que el entorno de información de una organización 
sea coherente, navegable y capaz de soportar procesos analíticos y generativos avanzados. 
La distinción entre KO y KR es de enfoque y propósito. KO se ocupa de la disposición 
sistemática de la información —vocabularios, jerarquías y esquemas que hacen que el 
contenido sea localizable y significativo —. KR codifica estas estructuras en formatos 
procesables por máquina que apoyan la inferencia, la integración y la automatización. Qin 
(2020) explica que KO es “orientada a las personas, centrada en la clasificación y la 
recuperación”, mientras que KR es “orientada a la máquina, centrada en la lógica y el 
cómputo” (p. 7). A pesar de estas orientaciones diferentes, ambas son interdependientes: 
KO proporciona los marcos conceptuales y la semántica sobre los que se construye KR, 
mientras que KR extiende los artefactos de KO a sistemas computacionales capaces de 
razonamiento e interoperabilidad. 
El puente entre KO y KR lo forman los llamados Sistemas de Organización del 
Conocimiento (Knowledge Organization Systems, a partir de ahora, KOS) — que organizan 
el significado tanto para la cognición humana como para la artificial—. El concepto de KOS 
se sitúa en el núcleo de la Capa Semántica y de Conocimiento de la Arquitectura de la 
Información. En el contexto de este curso, un KOS es una representación estructurada de 
un dominio —es decir, un área de conocimiento, una actividad o un conjunto de productos 
y servicios dentro de una organización—, compuesta por los conceptos relevantes de ese 
dominio. Normalmente, estos conceptos se vinculan o conectan entre sí, formando un 
sistema conceptual que refleja las relaciones semánticas entre ellos. Los conceptos se 
expresan mediante términos o etiquetas, que sirven como puntos de acceso y conexión 
entre la información y sus usuarios. Las estructuras semánticas compuestas por conceptos 
(expresados por términos o etiquetas) y sus relaciones cumplen múltiples funciones: en 
entornos digitales, permiten la indización y la categorización del contenido, así como su 
exploración, recuperación y filtrado, apoyando así la interoperabilidad y la reutilización 
del conocimiento. Esto se alinea con la visión de Zeng (2008) de los KOS como “esquemas 
para organizar la información y facilitar la gestión del conocimiento y la recuperación” (p. 
161), con la caracterización de Bagchi (2021) de los KOS como la “columna vertebral de 
los ecosistemas de conocimiento” (p. 742) y con la idea de Rosenfeld, Morville y Arango 
(2015) de que “los metadatos y los vocabularios controlados conectan el contenido a 
través del significado más que de la ubicación” (p. 178).  
Entre las relaciones semánticas que vinculan o conectan conceptos, la relación jerárquica 
es particularmente importante. La jerarquía ordena los conceptos por relaciones de más 
amplio–más específico de modo que sea posible moverse “desde los [conceptos] definidos 
de la manera más amplia hasta los más específicos” (ANSI/NISO Z39.19 -2005 (R2010), 
§9.3.4.1.1–9.3.4.1.2). Una relación jerárquica es el vínculo formal que ordena tales 
conceptos. ISO 25964 -1 la define como una “relación entre un par de conceptos … de los 
cuales uno tiene un alcance que queda completamente dentro del alcance del otro” 
(AENOR, 2014, §2.23). Estas estructuras sustentan la inferencia (por ejemplo, expansión 
de búsquedas), la navegación y la recuperación al permitir a personas y sistemas moverse 
arriba o abajo en la jerarquía; ISO 25964 señala que la función principal es ayudar a elegir 
“el nivel apropiado de especificidad” y habilitar búsquedas “explotadas” desde un 
concepto más amplio a sus descendientes (AENOR, 2014, §10.2.1). 

19 
 
De acuerdo con las normas, pueden distinguirse tres tipos principales de relaciones 
jerárquicas:  
• Genérica (es-un/a): la más específica es un tipo de la más amplia (AENOR, 2014, 
§10.2.1; §10.2.2). Una prueba de validez sencilla es reformular como “[concepto 
más específico] es un [concepto más amplio]”. Ejemplo: Primate es un Mamífero → 
Mamífero es un Animal (AENOR, 2014, §10.2.1). Esto es susceptible de la conocida 
lógica “todos–algunos”. Ejemplo: todos los cactus son plantas suculentas; pero solo 
algunas plantas suculentas son cactus. 
• Partitiva ( todo–parte): la más específica es un constituyente de la más amplia. 
Ejemplo: los Vasos sanguíneos son parte del Sistema cardiovascular; la Zoología es 
parte de la Biología (AENOR, 2014, §10.2.3.1). ISO limita su admisibilidad a casos 
en que las partes pertenecen de forma única a un solo todo y advierte contra casos 
ambiguos como las Ruedas son parte de la Bicicleta (AENOR, 2014, §10.2.3.1). 
• Enumerativa/instanciativa (instancia-de): la más específica es una instancia de la 
más amplia (AENOR, 2014, §10.2.4). Ejemplo: Mars, Venus… son instancias de 
Planetas. (ANSI/NISO, 2010, §9.2.2.2). 
El espectro de KOS abarca seis grandes artefactos, progresando en complejidad y 
formalidad: listas de términos, esquemas de categorización, taxonomías, tesauros, 
ontologías y grafos de conocimiento (Qin, 2020, pp. 6–8; Díaz, 2023, pp. 3–4). 
• En el extremo más simple de este continuo, las listas de términos proporcionan 
conjuntos planos de conceptos preferidos (expresados con términos o etiquetas), 
útiles para la indización, pero sin estructura interna. 
• Los esquemas de categorización agrupan conceptos de forma asociativa (p. ej., 
Plantas, Animales, Minerales), habilitando la exploración,  pero sin respaldar 
relaciones formales. 
• Las taxonomías son ordenaciones jerárquicas controladas de conceptos (también 
denominados categorías); deben presentar relaciones de concepto más 
amplio/más específico y soportar visualización multinivel para la exploración y la 
navegación (ANSI/NISO, 2010, §9.3.4.1). En la práctica, las taxonomías codifican 
principalmente jerarquías genéricas y son valiosas para la orientación 
(wayfinding) y la delimitación temática en las interfaces de usuario (ANSI/NISO, 
2010, §9.4.3.1–§9.4.3.3). 
• Los tesauros añaden vocabularios controlados y enlaces asociativos como 
conceptos más amplios (BT), más específicos (NT) y relacionados (RT), mejorando 
así la recuperación y la desambiguación. En cuanto a la jerarquía, los tesauros 
abarcan formas genéricas, partitiva y enumerativa (AENOR, 2014, §10.2; §10.3; 
ANSI/NISO, 2010, §9.2.2). 
• Las ontologías introducen semántica formal (clases, propiedades, restricciones) 
que permiten el razonamiento (Islam & Islam, 2024, p. 10). 
• Por último, los grafos de conocimiento ( knowledge graphs, a partir de ahora, KG) 
instancian clases ontológicas como nodos y las conectan mediante relaciones 
(propiedades) a gran escala (p. ej., nodo: perros – propiedad: perseguir – nodo: 
gatos), permitiendo razonamiento, descubrimiento impulsado por AI e integración 
de datos entre dominios (Bagchi, 2021, pp. 743–744). 

20 
 
Esta jerarquía de artefactos puede visualizarse como un continuo evolutivo, en el que cada 
nivel añade estructura, riqueza semántica e interpretabilidad por máquina. 
Dentro de este continuo pueden observarse dos líneas conceptuales. 
• La primera línea incluye los esquemas de categorización, que son agrupaciones 
asociativas amplias con poco o ningún control o semántica —p. ej., arreglos como 
[hábitats] o [dieta] para apoyar la exploración —. Siguen siendo valiosos para la 
exploración y la organización de alto nivel, pero carecen del rigor necesario para el 
razonamiento computacional. 
• La segunda línea comparte una base común: la aplicación de la relación genérica 
(es-un/a) para generar la jerarquía que constituye la estructura fundamental del 
artefacto. Esta línea progresa desde taxonomías —centradas en la jerarquía 
genérica— hasta tesauros, ontologías y grafos de conocimiento, que añaden de 
forma incremental complejidad estructural y expresividad en la representación del 
dominio. Las taxonomías formalizan jerarquías; los tesauros añaden diversos tipos 
de relaciones semánticas; las ontologías definen la lógica conceptual; y los grafos 
de conocimiento realizan estas conexiones de forma dinámica dentro de los 
entornos de datos. Como destacan Díaz (2023) y Qin (2020), esta evolución 
acumulativa —de la organización descriptiva a la semántica y luego a la 
computacional— refleja la convergencia de KO y KR en la Arquitectura de la 
Información contemporánea. 
Una ilustración sencilla en el dominio animal ayuda a mostrar estas relaciones. 
• Una taxonomía establece relaciones jerárquicas basadas en el modo genérico ( es-
un/a): Animal > Mamífero > Gato/Perro. 
• Un tesauro especifica que gato y felino son sinónimos ( UF = Use For), puede incluir 
jerarquías partitivas o enumerativas cuando proceda y añade relaciones 
asociativas (p. ej., Primates se relaciona con Zoología). 
• Una ontología define propiedades (p. ej., hasHabitat, hasDiet) y restricciones (p. ej., 
todo gato es un mamífero que come carne). 
• Por último, un grafo de conocimiento instancia estos hechos en tríadas —p. ej., 
Silvestre es una instancia de Gato; Silvestre caza a Piolín (instancia de Presa) —, 
vinculando entidades entre conjuntos de datos para permitir la búsqueda 
semántica y la inferencia. 
Los temas posteriores introducirán patrones jerárquicos alternativos en los KOS, como la 
polijerarquía y la facetación, y cómo se manejan según los estándares. 
La progresión desde taxonomías — centradas en la jerarquía genérica — hasta tesauros, 
ontologías y grafos de conocimiento no es lineal, sino acumulativa e iterativa. Como 
sostiene Bagchi (2021), el “ecosistema de organización del conocimiento” implica 
retroalimentación constante entre artefactos, tecnologías y comprensión humana (p. 743). 
Tesauros, ontologías y grafos de conocimiento a menudo coexisten, sirviendo a propósitos 
distintos pero complementarios dentro del mismo entorno de información empresarial. 
Islam e Islam (2024) describen esto como un “paradigma convergente” en el que las 
estructuras de conocimiento humanas y de máquina se solapan cada vez más a través de 

21 
 
semánticas compartidas (p. 12). En la práctica, bibliotecas digitales, plataformas de datos 
empresariales y sistemas basados en AI dependen de una combinación de componentes 
KOS que escalan desde vocabularios curados por humanos hasta grafos mejorados por 
aprendizaje automático. 
Varias autoras y autores destacan la naturaleza multidimensional de la clasificación de 
KOS. Soergel (2009) y Zeng (2008) identifican criterios comunes como estructura (plana 
vs. jerárquica), función (indización, recuperación, inferencia), grado de formalización 
(informal vs. lógica) e interoperabilidad (independiente vs. enlazada). Bagchi (2021) y 
Yuan et al. (2025) añaden el contexto de uso y la riqueza semántica. Combinados, estos 
criterios revelan tanto una progresión como un ecosistema. Las listas de términos y los 
esquemas de categorización están principalmente orientados a las personas, mientras que 
las ontologías y los grafos de conocimiento están orientados a la máquina; las taxonomías 
y los tesauros ocupan un terreno intermedio. Como señala Blumauer (2015), “el control 
jerárquico y la profundidad semántica determinan la capacidad de un KOS para la 
automatización” (p. 5).  En la Tabla 2.2 . se muestra la c lasificación integrada de SOC , a 
partir de los criterios de c omparación por estructura, función, formalización, 
interoperabilidad, contexto y riqueza semántica) 
Criterio Listas de 
términos 
Esquemas 
de 
categoriz
ación 
Taxonomías Tesauro
s 
Ontologí
as 
Grafos 
de 
conocimi
ento 
Estructura Plana Asociativa Jerárquica 
(mayoritaria
mente, 
genérica) 
Jerárquic
a / 
Polijerár
quica 
Modelo 
lógico 
Grafo en 
red 
Función Indizació
n 
Exploració
n 
Recuperació
n 
Recupera
ción 
Razonami
ento 
Razonami
ento y AI 
Formalizaci
ón 
– – ✓ ✓✓ ✓✓✓ ✓✓✓✓ 
Interoperab
ilidad 
Independ
iente 
Limitada Enlazada Interenla
zada 
Integrada Totalmen
te 
enlazada 
Contexto de 
uso 
Humano Humano Híbrido Híbrido Máquina Máquina 
+ AI 
Riqueza 
semántica 
Baja Baja–
Moderada 
Moderada Alta Muy alta Máxima 
Tabla 2: Clasificación integrada de SOC 
Los KOS pueden verse como un continuo en el que cada sistema añade complejidad 
estructural, riqueza semántica y capacidad de interoperabilidad, avanzando hacia 
ecosistemas basados en grafos, preparados para la AI. 
En las fuentes aparece un consenso: la transición de listas de términos a grafos de 
conocimiento representa un cambio desde la organización de superficie hacia el modelado 
semántico profundo. Mazzocchi (2018) y Salatino et al. (2025) enfatizan que este cambio 
se expande desde la clasificación hacia la contextualización y la construcción de relaciones, 
alineando los sistemas de información con las entidades del mundo real y sus 
interdependencias. En la Arquitectura de la Información, esta transformación no solo 

22 
 
habilita una mejor recuperación, sino una interacción más inteligente —tendiendo 
puentes entre la categorización humana y el razonamiento de la AI—. 
En síntesis, los Sistemas de Organización del Conocimiento encarnan el territorio 
compartido de KO y KR. Anclan el significado entre espacios de información, conectan 
contenido con conceptos y permiten que el conocimiento circule entre agentes humanos y 
artificiales. Su evolución —de listas simples a redes semánticas — refleja la trayectoria 
histórica de la Arquitectura de la Información en sí misma: de estructurar el contenido a 
estructurar la comprensión. En el contexto de la Capa Semántica y de Conocimiento, los 
KOS proporcionan el andamiaje para la interoperabilidad semántica, la localización y la 
reutilización, asegurando que la información no solo se almacene y muestre, sino que 
también se comprenda, conecte y se pueda razonar sobre ella. 
2.3.4. Relaciones con la precedente Capa Física y de 
Gobernanza y con la posterior Capa de Interacción y 
Experiencia 
La Capa Semántica y de Conocimiento ocupa una posición mediadora entre los 
fundamentos organizativos de los datos y la experiencia de información orientada a las 
personas usuarias. Depende de las infraestructuras, los repositorios de metadatos y los 
mecanismos de gobernanza de la Capa Física y de Gobernanza, y al mismo tiempo habilita 
las funcionalidades de descubrimiento, interacción y analítica de la Capa de Interacción y 
Experiencia. En este sentido, funciona tanto como capa de traducción —conectando datos 
estructurados con significado — como capa de gobernanza —asegurando que el 
significado se aplique de manera consistente entre plataformas y contextos—. 
Desde abajo, la Capa Semántica y de Conocimiento se nutre de la Capa Física y de 
Gobernanza, que suministra los materiales esenciales: conjuntos de datos, metadatos y 
políticas de gobernanza. Tesfaye (2024) describe la capa semántica como aquella que “se 
sitúa sobre las fuentes y modelos de datos, integrándolos y enriqueciéndolos para 
habilitar una interpretación consistente”. Esta dependencia asegura que el significado 
aplicado en los modelos semánticos permanezca anclado en activos de datos verificados y 
tutelados. EK Team (2024b) subraya que una capa semántica robusta “se construye sobre 
repositorios de metadatos, catálogos de datos y taxonomías que reflejan las estructuras de 
gobernanza de la empresa”, creando un puente entre la gestión técnica de datos y la 
comprensión humana. Por ejemplo, el almacén de datos gobernado de una organización 
financiera define las métricas de “ingresos” y “coste de adquisición de clientes”; la capa 
semántica entonces las alinea con definiciones de negocio, asegurando que informes y 
cuadros de mando en todos los departamentos utilicen semánticas idénticas. 
La dependencia, sin embargo, no es meramente jerárquica, sino recíproca. La Capa 
Semántica y de Conocimiento también constriñe la Capa Física y de Gobernanza al 
imponer estándares y vocabularios semánticos que promueven la interoperabilidad. Como 
señala Nash (2024), los modelos semánticos “estandarizan cómo se interpretan los datos 
entre sistemas dispares”, moldeando así cómo se diseñan y mantienen los activos físicos 
de datos. Las políticas de gobernanza —como los roles de tutela y las reglas de calidad de 
datos— se incrustan dentro de estos modelos semánticos, asegurando que la gobernanza 

23 
 
no sea una ocurrencia tardía, sino una propiedad arquitectónica incorporada. Esta 
interacción crea un círculo virtuoso: la gobernanza informa a la semántica, y la semántica 
refuerza a la gobernanza. 
Hacia arriba, la Capa Semántica y de Conocimiento habilita la Capa de Interacción y 
Experiencia, que abarca categorías de exploración, interfaces de búsqueda, sistemas de 
navegación, recomendaciones e interacciones conversacionales. EK Team (2024a) subraya 
que diseñar IA para la AI “requiere capas de conocimiento estructurado que informen y 
gobiernen los sistemas inteligentes”. En la práctica, esto significa que taxonomías y 
ontologías semánticas sirven como base de conocimiento para asistentes impulsados por 
AI, motores de recomendación y navegación adaptativa. Por ejemplo, una plataforma de 
comercio electrónico puede apoyarse en una taxonomía semántica que vincula productos, 
atributos y contextos de uso. Esta estructura alimenta la búsqueda facetada y las 
recomendaciones personalizadas, asegurando que las interacciones se informen por el 
significado y no por la mera coincidencia de palabras clave. De forma similar, en entornos 
de analítica, la capa semántica habilita BI en autoservicio al exponer métricas gobernadas 
a personas no técnicas mediante consultas en lenguaje natural. 
En resumen, la Capa Semántica y de Conocimiento se ancla en las estructuras de datos 
controladas y gobernadas de la Capa Física y de Gobernanza, a la vez que impulsa las 
capacidades adaptativas y centradas en el usuario de la Capa de Interacción y de 
Experiencia. Asegura que el conocimiento organizativo sea simultáneamente estable — a 
través de la gobernanza — y dinámico —a través de la experiencia —. Como observa EK 
Team (2024b), forma el “puente semántico” que transforma los “datos en bruto en 
conocimiento accionable”, integrando infraestructura, significado e interacción en un 
ecosistema de información coherente. 
2.3.5. Ejemplos de funcionamiento y uso de los principales tipos 
de SOC 
2.3.5.1. Lista de términos (Term list) 
• Ejemplo: DSIA Research for Information Architecture – Glossary 
https://methodbrain.com/resources/information-architecture-glossary 
• Espacio digital:  https://methodbrain.com/resources/information-architecture-
glossary/ 
• Función: Normaliza la terminología básica en torno a la Arquitectura de la 
Información (AI). 
• Muestra: Ejemplo de términos equivalentes: Information scent , Information 
ecology, Navigation scheme. Los términos se listan alfabéticamente, sin jerarquías 
ni relaciones semánticas formales. 
2.3.5.2. Esquema de categorización (Categorisation scheme) 
• Ejemplo: BBC News Topics https://www.bbc.com/news/topics/c2vdnvdgypyt 
• Espacio digital: Portal informativo BBC News. 
• Función: Agrupa noticias en conjuntos temáticos asociados, sin jerarquía ni 
control terminológico. 

24 
 
• Muestra: Ejemplo de categorías: Artificial Intelligence, Climate Change, Elections, 
Space Exploration. Cada categoría enlaza a artículos relacionados. 
2.3.5.3. Taxonomía (Taxonomy) 
• Ejemplo: Amazon Product Taxonomy  
https://www.amazon.es/ 
• Espacio digital: Plataforma de comercio electrónico Amazon. 
• Función: Organiza los productos mediante una estructura jerárquica de categorías 
y subcategorías para facilitar la navegación, el filtrado y la recuperación de 
resultados. 
• Muestra: Ejemplo jerárquico: Electrónica → Ordenadores y accesorios → Portátiles 
→ Portátiles de juego  https://www.amazon.com/b/?node=565108. Cada nivel 
refina el ámbito del anterior, permitiendo búsquedas y recomendaciones más 
precisas. 
2.3.5.4. Tesauro (Thesaurus) 
• Ejemplo: UNESCO Thesaurus  aplicado en la UNESCO Digital Library  
https://unesdoc.unesco.org/ 
• Espacio digital: Biblioteca Digital de la UNESCO. 
• Función: Facilita la búsqueda semántica y la expansión de consultas mediante 
términos controlados y relaciones BT/NT/RT. 
• Muestra: Ejemplo: Educación ambiental  (BT Educación; NT Programas de 
educación ambiental; RT Desarrollo sostenible). 
2.3.5.5. Ontología (Ontology) 
Ejemplo 1: Schema.org Ontology https://schema.org 
• Espacio digital:  Sitios web que emplean marcado estructurado basado en 
Schema.org (por ejemplo, Wikipedia, Google, o portales de comercio electrónico). 
• Función: Estandariza la representación de entidades y propiedades en la Web 
mediante tipos y relaciones semánticas reutilizables, lo que permite la 
automatización de procesos como la indexación y la generación de rich results  en 
buscadores, i la optimización en buscadores. 
• Muestra: Ejemplo: tipo (clase) Product  https://schema.org/Product  con 
propiedades name, brand, offers, aggregateRating, review. Estos tipos se 
representan en JSON -LD o microdatos para mejorar la interpretación automática 
de los contenidos por los motores de búsqueda. 
Ejemplo 2:  DBpedia Ontology  integrada en Wikipedia y aplicaciones semánticas 
https://www.dbpedia.org/resources/ontology/ 
• Espacio digital: Plataforma DBpedia (derivada de Wikipedia). 
• Función:  
o Automatiza la extracción y clasificación de entidades y relaciones a partir 
de Wikipedia mediante procesos de semantic lifting.  
 Ontología usada para automatizar la extracción y clasificación  
de entidades y relaciones. 

25 
 
 Permite consultas automáticas (por ejemplo, “todas las películas 
dirigidas por Christopher Nolan”) sin intervención humana. 
o Los asistentes virtuales o aplicaciones que consultan DBpedia (por 
ejemplo, Siri o Alexa) recuperan datos preclasificados ontológicamente 
(Person, Film, City, etc.). 
• Muestra: Ejemplo: Film (hasDirector → Person; hasActor → Person; 
hasReleaseDate → Date).  
2.3.5.6. Grafo de conocimiento (Knowledge graph) 
• Ejemplo: Google Knowledge Graph  empleado en Google Search  y Gemini 
https://www.google.com/search?q=Leonardo+da+Vinci / 
https://blog.google/products/gemini/ 
• Espacio digital:  Motor de búsqueda Google y sistema generativo Gemini . 
Función:  
• Relaciona entidades y conceptos para proporcionar respuestas enriquecidas y 
verificadas. 
• Gemini utiliza el Google Knowledge Graph (KG) para enriquecer sus respuestas 
con información factual. Si un usuario pregunta en Gemini, por ejemplo: “¿Quién es 
Leonardo da Vinci?” , Gemini genera una respuesta que integra información 
estructurada del KG (fecha de nacimiento, aportaciones, relaciones familiares) y 
enlaza fuentes verificadas del grafo. 
• Muestra: Nodo Leonardo da Vinci  conectado a Pintor , Inventor, La Gioconda , 
Renacimiento italiano. En Gemini , el grafo fundamenta respuestas factualizadas y 
verificadas. 
 
Declaración sobre IA generativa 
Durante la preparación de este trabajo, los autores utilizaron Chat GPT-5 con el fin de:  
Parafrasear y reformular, y realizar la corrección gramatical y ortográfica. Tras utilizar 
esta herramienta, los autores revisaron y editaron el contenido según fue necesario y 
asumieron plena responsabilidad por el contenido de la publicación. 
```
