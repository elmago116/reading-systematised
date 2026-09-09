---
title: "Guía de prompting para modelos de lenguaje: fundamentos, buenas prácticas y técnicas"
author: Rubén Alcaraz-Martínez
year: "2026"
Type: Report
DOI: 10.5281/zenodo.19605052
source: https://doi.org/10.5281/zenodo.19605052
created: 2026-05-06
description: Este informe introduce recoge múltiples estrategias, métodos y técnicas orientadas al uso de modelos de lenguaje de forma más controlada y fiable. En primer lugar, se introducen los conceptos básicos y, a continuación, se reúnen buenas prácticas para redactar y estructurar instrucciones (claridad, c
tags:
  - op/acc/pending-review
pdfORepub: "[[Guía de prompting para modelos de lenguaje-fundamentos, buenas prácticas y técnicas.pdf]]"
---
[[Guía de prompting para modelos de lenguaje-fundamentos, buenas prácticas y técnicas.pdf]]

> **Abstract:** Este informe introduce recoge múltiples estrategias, métodos y técnicas orientadas al uso de modelos de lenguaje de forma más controlada y fiable. En primer lugar, se introducen los conceptos básicos y, a continuación, se reúnen buenas prácticas para redactar y estructurar instrucciones (claridad, contexto, restricciones, formato de salida), incluyendo un apartado de sintaxis (cómo formular, delimitar y especificar el output), además de secciones específicas sobre cuestiones éticas y vinculadas a la privacidad. El núcleo del informe es una clasificación de técnicas de prompting por finalidad: (1) razonamiento y resolución estructurada de problemas; (2) fiabilidad y verificación; (3) metacognición y autorregulación; (4) contexto y dinámica conversacional; (5) control del objetivo y de la salida; (6) código, herramientas y formalización; (7) dimensiones de estilo/afectividad; (8) multimodalidad e interdisciplinariedad, y (9) creatividad y generación abierta.
## Full text (extracted from `Guía de prompting para modelos de lenguaje-fundamentos, buenas prácticas y técnicas.pdf`)

*Source:* `2PDF/Guía de prompting para modelos de lenguaje-fundamentos, buenas prácticas y técnicas.pdf`  
*Extracted:* 2026-05-06

```text
 
 
Rubén Alcaraz-Martínez
 
 

1 
 
Facultat d’Informació i Mitjans Audiovisuals 
Universitat de Barcelona 
Melcior de Palau, 140 
08014 Barcelona 
 
Autor: Rubén Alcaraz-Martínez 
 
Obra distribuida bajo una licencia Creative Commons BY-NC-SA 4.0 
 
Cita recomendada 
Alcaraz-Martínez, Rubén (2026). Guía de prompting para modelos de lenguaje: 
fundamentos, buenas prácticas y técnicas. Barcelona: Universitat de Barcelona. 
https://doi.org/10.5281/zenodo.19605053 
  


2 
Rubén Alcaraz Martínez es doctor en Ingeniería y Tecnologías de la Información, máster 
en Gestión de Contenidos Digitales y diplomado en Biblioteconomía y Documentación. Es 
profesor del Departamento de Biblioteconomía, Documentación y Comunicación 
Audiovisual de la Universidad de Barcelona donde imparte docencia en el grado en 
Gestión de Información y Documentación Digital, el máster en Gestión de Contenidos 
Digitales, el máster en Humanidades Digitales y el máster en Bibliotecas Públicas. Es 
miembro del grupo de innovación docente consolidado Adaptabit, dedicado a la 
investigación en accesibilidad digital y forma parte del Centro de Investigación en 
Información, Comunicación y Cultura (CRICC). 
ORCID: https://orcid.org/0000-0002-7185-0227  
Contacto: ralcaraz@ub.edu 
 
 
  

3 
Este informe introduce recoge múltiples estrategias, métodos y técnicas orientadas al 
uso de modelos de lenguaje de forma más controlada y fiable. En primer lugar, se 
introducen los conceptos básicos y, a continuación, se reúnen buenas prácticas para 
redactar y estructurar instrucciones (claridad, contexto, restricciones, formato de 
salida), incluyendo un apartado de sintaxis (cómo formular, delimitar y especificar el 
output), además de secciones específicas sobre cuestiones éticas y vinculadas a la 
privacidad. El núcleo del informe es una clasificación de técnicas de prompting por 
finalidad: (1) razonamiento y resolución estructurada de problemas; (2) fiabilidad y 
verificación; (3) metacognición y autorregulación; (4) contexto y dinámica 
conversacional; (5) control del objetivo y de la salida; (6) código, herramientas y 
formalización; (7) dimensiones de estilo/afectividad; (8) multimodalidad e 
interdisciplinariedad, y (9) creatividad y generación abierta. 
Modelos de lenguaje, LLM, Prompts, Ingeniería de prompts, Diseño de prompts. 
Aquest informe recull múltiples estratègies, mètodes i tècniques orientades a l’ús de 
models de llenguatge d’una manera més controlada i fiable. En primer lloc, s’hi 
presenten els conceptes bàsics i, tot seguit, s’hi apleguen bones pràctiques per redactar i 
estructurar instruccions (claredat, context, restriccions i format de sortida). També 
inclou un apartat de sintaxi (com formular, delimitar i especificar la sortida), a més de 
seccions específiques sobre qüestions ètiques i relacionades amb la privacitat. El nucli 
de l’informe és una classificació de tècniques de prompting segons la finalitat: (1) 
raonament i resolució estructurada de problemes; (2) fiabilitat i verificació; (3) 
metacognició i autoregulació; (4) context i dinàmica conversacional; (5) control de 
l’objectiu i de la sortida; (6) codi, eines i formalització; (7) dimensions d’estil/afectivitat; 
(8) multimodalitat i interdisciplinarietat, i (9) creativitat i generació oberta. 
Models de llenguatge, LLM, Prompts, Enginyeria de prompts, Disseny de prompts. 
 

4 
This report brings together multiple strategies, methods and techniques aimed at using 
language models in a more controlled and reliable manner. First, it introduces the 
foundational concepts and then compiles good practices for drafting and structuring 
instructions (clarity, context, constraints and output format). It also includes a section on 
syntax (how to formulate, delimit and specify the output), as well as dedicated sections 
on ethical issues and privacy-related matters. The core of the report is a classification of 
prompting techniques by purpose: (1) reasoning and structured problem-solving; (2) 
reliability and verification; (3) metacognition and self-regulation; (4) context and 
conversational dynamics; (5) control of the objective and the output; (6) code, tools and 
formalisation; (7) stylistic/affective dimensions; (8) multimodality and interdisciplinarity; 
and (9) creativity and open-ended generation. 
Language models, LLM, Prompts, Prompt engineering, Prompt design. 
 
 
  

5 
1. Introducción 6 
1.1. Qué es un prompt 7 
1.2. Qué es la ingeniería de prompts 8 
2. Buenas prácticas en materia de prompting 10 
2.1. Buenas prácticas generales orientadas a la redacción y estructuración  
de los prompts 10 
2.2. Sintaxis 16 
2.3. Seguridad 18 
2.4. Privacidad y datos personales 19 
2.5. Cuestiones éticas 20 
2.6. Control de sesgos 23 
2.7. Uso responsable y sostenible 25 
3. Clasificación y ejemplificación de las técnicas de prompting 26 
3.1. Razonamiento y resolución estructurada de problemas 28 
3.2. Fiabilidad y verificación 40 
3.3. Metacognición y autorregulación 45 
3.4. Contexto y dinámica conversacional 46 
3.5. Control del objetivo y de la salida 48 
3.6. Código, herramientas y formalización 51 
3.7. Dimensión afectiva y estilística 51 
3.8. Multimodalidad e interdisciplinariedad 52 
3.9. Creatividad y generación abierta 53 
Recomendaciones finales 55 
Conclusiones 55 
Referencias 57 
 

6 
Este informe tiene como objetivo sistematizar y presentar estrategias, métodos y técnicas 
de prompting para el uso de modelos de lenguaje de forma más controlada, fiable y 
responsable, proporcionando un marco aplicable a contextos académicos y profesionales. 
También poner sobre la mesa diversas cuestiones éticas, así como criterios de gobernanza 
y buenas prácticas. En particular, en materia de privacidad y protección de datos, control 
y mitigación de sesgos, transparencia y trazabilidad del uso, seguridad y prevención de 
usos indebidos, y uso razonable y sostenible. 
Los modelos de lenguaje de gran escala, grandes modelos de lenguaje, o modelos 
extensos de lenguaje (large language models, LLM) han modificado de manera sustancial 
el panorama del aprendizaje automático (Zhao et al., 2023a). Este cambio responde, en 
buena medida, a los avances derivados de la incorporación de redes neuronales y de 
técnicas de aprendizaje profundo (deep learning) en el ámbito del procesamiento del 
lenguaje natural (natural language processing, NLP), que han permitido a estos modelos 
aprender a partir de volúmenes masivos de datos y, en consecuencia, adaptarse a un 
abanico mucho más amplio de tareas (Petroni et al., 2019; Brown et al., 2020). 
Un hito decisivo en esta trayectoria fue la introducción de la arquitectura 
transformer1 (Vaswani et al., 2017), que estableció los fundamentos para el desarrollo de 
modelos progresivamente más complejos y con mayor capacidad. Con posterioridad, la 
irrupción de modelos como BERT (Devlin et al., 2018) y GPT (Radford et al., 2019) 
evidenció el potencial del preentrenamiento sobre grandes volúmenes de datos, 
complementado por un proceso de ajuste fino (fine-tuning)2 orientado a optimizar el 
rendimiento en tareas concretas. 
Esta evolución tecnológica propició la aparición de un tipo específico de LLM, 
conocidos como variantes conversacionales de transformadores decodificadores 
unidireccionales (conversational decoder-only transformer variants) (Vaswani et al., 
2017), entre los que se encuentran modelos como GPT (Brown et al., 2020; Ouyang et al., 
2022), LaMDA (Thoppilan et al., 2022), PaLM (Chowdhery et al., 2023), LLaMA (Touvron 
et al., 2023) y Mistral (Jiang et al., 2023). 
Estos modelos destacan por su elevada capacidad para procesar, generar e 
interpretar lenguaje natural, lo que ha motivado su adopción en una amplia diversidad 
de dominios. Entre ellos se incluyen ámbitos tan dispares como las finanzas (Wu et al., 
2023), la programación (Xu et al., 2022), el contexto educativo (Kasneci et al., 2023) o la 
atención sanitaria (Thirunavukarasu et al., 2023). 
 
1 Arquitectura de redes neuronales basada en mecanismos de atención (self-attention) que permiten 
modelar dependencias entre elementos de una secuencia sin recurrir a estructuras recurrentes o 
convolucionales. Esta aproximación mejora la eficiencia computacional y la capacidad de capturar 
relaciones a largo plazo en tareas de procesamiento del lenguaje natural. 
2 Proceso mediante el cual un modelo previamente preentrenado sobre grandes volúmenes de datos 
generales se adapta a una tarea específica mediante un nuevo entrenamiento sobre un conjunto de datos 
más reducido y especializado, ajustando sus parámetros para optimizar el rendimiento en un dominio o 
problema concreto. 

7 
Por otra parte, su naturaleza conversacional, junto con la popularización de 
interfaces basadas en chat como ChatGPT (Brown et al., 2020; Yang et al., 2024a), ha 
facilitado que las sofisticadas capacidades computacionales de estos modelos resulten 
accesibles para el gran público, incluso sin experiencia previa. No obstante, para que el 
modelo ofrezca respuestas adecuadas a las consultas de los usuarios, resulta necesario 
saber cómo comunicarse con él mediante la formulación de un prompt apropiado. 
El prompt, entendido como instrucción o entrada, funciona como un puente de 
traducción entre la comunicación humana y las capacidades computacionales de los 
LLM (Fagbohun et al., 2023). Se compone de instrucciones formuladas en lenguaje 
natural que actúan como intermediarias, al transformar las peticiones humanas en 
tareas susceptibles de ser ejecutadas por el software (Liu et al., 2023b). Más allá de una 
instrucción puntual, los prompts configuran un marco contextual para la interacción, al 
transmitir la relevancia de la información y delimitar tanto el formato como el contenido 
esperado en la salida del modelo. 
Aunque la interacción en lenguaje natural mediante prompts puede generar la 
percepción de resultar altamente accesible, diversos estudios han demostrado que los 
usuarios sin experiencia en inteligencia artificial presentan, en gran medida, dificultades 
para emplear un LLM de forma eficiente en la resolución de tareas (Zamfirescu-Pereira et 
al., 2023). La mayoría de las personas no recurre a técnicas avanzadas de prompting, y 
los prompts utilizados suelen ser breves, simples y poco elaborados, incluso en 
contextos en los que podrían optimizarse con relativa facilidad (Desmond y Brachman, 
2024; Zamfirescu-Pereira et al., 2023). 
No obstante, también se ha observado que cuando el propio sistema proporciona 
apoyo –por ejemplo, mediante la sugerencia de prompts, el uso de plantillas, la 
presentación de ejemplos o la visualización del proceso– los resultados mejoran y los 
usuarios perciben una colaboración más efectiva con la IA (Gutheil et al., 2025; White et 
al., 2023). Esto sugiere que el prompting no depende exclusivamente del usuario, sino 
también del diseño de la herramienta. Estas limitaciones han puesto de manifiesto la 
relevancia de la optimización estratégica de los prompts y han impulsado la necesidad de 
perfiles especializados en esta materia. 
Un prompt está compuesto por varios componentes clave que funcionan 
conjuntamente para guiar a la IA. Aunque no todos los prompts contienen 
necesariamente todos los elementos que se muestran a continuación, conocerlos y 
entender la función de cada uno de ellos es fundamental para redactarlos de forma eficaz 
(Kuka, 2025): 
— Directiva: la directiva es la instrucción principal del prompt. Recoge la tarea 
que se debe realizar y debe ser lo más clara y concisa posible para evitar 
respuestas genéricas o irrelevantes. La directiva puede incluir ejemplos para 
guiar a la IA. 

8 
— Rol (Persona): el rol indica a la IA que actué como un determinado experto, 
de acuerdo con un estilo determinado o tono. 
— Formato de salida: el formato de salida permite especificar el formato en 
que se desea que el modelo presente la respuesta (tabla, texto en prosa, en 
un lenguaje de programación específico y con unas estructuras 
determinadas…). 
— Información adicional: en el prompt es posible incluir información adicional 
de contexto o antecedentes que la IA puede necesitar para generar 
respuestas más precisas, así como para evitar generalizaciones o 
alucinaciones. Esto incluye aportar documentos, datos o ejemplos extensos. 
Aunque no existe un mejor orden para todos los prompts, la recomendación más 
habitual es iniciarlos con los ejemplos o información adicional (por ejemplo, ficheros 
adjuntos), seguir con el rol, continuar con la directiva y finalizar con el formato de salida 
esperado. En este sentido, cuando en una consulta se aporta primero el contexto y luego 
la pregunta, el modelo procesa la pregunta habiendo visto ya el contexto, mientras que, 
si se comienza con la pregunta para, posteriormente, aportar el contexto, podría no 
disponer de esa información en el mismo marco contextual durante el procesamiento 
inicial (Leviathan et al., 2025). 
La ingeniería de prompts se define como el proceso estratégico de diseño de entradas o 
instrucciones específicas para cada tarea, orientadas a guiar a los LLM en la generación 
de respuestas pertinentes y alineadas con los objetivos planteados (Fagbohun et al., 
2023; Sahoo et al., 2025). 
Los ingenieros de prompts explotan las capacidades predictivas y los amplios 
conjuntos de datos de entrenamiento de los modelos de IA, combinándolos con los 
matices propios de la comunicación humana para influir de manera estratégica en el 
comportamiento del modelo sin recurrir a un entrenamiento específico para cada tarea 
(Brown et al., 2020; Petroni et al., 2019; Radford et al., 2019; Schick y Schütze, 2021). 
Una ingeniería de prompts eficaz aplica de forma táctica diversas buenas prácticas de 
diseño, seleccionadas según el contexto, con el fin de maximizar el rendimiento de los 
LLM y hacerlos más precisos y relevantes en tareas concretas. 
Mientras que un prompt cuidadosamente diseñado puede orientar a estos modelos 
hacia la generación de respuestas más precisas, relevantes y adecuadas al contexto, los 
prompts deficientes pueden conducir a salidas ambiguas, irrelevantes o incluso 
incorrectas (Brown et al., 2020; Ouyang et al., 2022). En consecuencia, la efectividad de 
los LLM en aplicaciones prácticas depende en gran medida de la calidad de la ingeniería 
de prompts y del grado de experiencia de quienes los desarrollan. 
El rápido y fragmentado crecimiento de las técnicas de prompting dificulta que los 
profesionales identifiquen qué enfoque resulta más adecuado en cada situación 
(Fagbohun et al., 2023), lo que ha contribuido a que la ingeniería de prompts se consolide 
como una técnica clave para potenciar las capacidades tanto de los LLM como de los 

9 
modelos visión-lenguaje (vision-language models, VLM)3 (Bahng et al., 2022; Sahoo et al., 
2025).  
Los estudios que han evaluado estas técnicas en contextos de uso reales –como la 
programación, la escritura, el análisis de requisitos o el aprendizaje– coinciden en 
señalar que no existe un prompt universalmente óptimo y que su efectividad depende de 
factores como la tarea concreta, el modelo empleado y el dominio de aplicación (Chen et 
al., 2024; Garcia et al., 2025). En general, los prompts bien estructurados, que 
incorporan ejemplos claros y proporcionan indicaciones explícitas sobre lo que la IA 
puede o debe hacer, tienden a ofrecer mejores resultados que formulaciones genéricas 
del tipo “actúa como un experto” o instrucciones vagas y poco organizadas (Wang et al., 
2024; DiCuffa et al., 2025; Garcia et al., 2025). En consecuencia, la forma y la estructura 
del prompt resultan más determinantes que el tono o la asignación de un rol. 
Este informe recoge buenas prácticas en materia de prompting y diversas técnicas 
específicas documentadas en la literatura (Fagbohun et al., 2023; Sahoo et al., 2025), 
para finalizar con un conjunto de ejemplos aplicables a diferentes ámbitos relacionados 
con el área de conocimiento de la información y la documentación. 
  
 
3 Modelos que integran información visual y textual para comprender o generar salidas a partir de ambas 
modalidades (Rahman, 2026). 

10 
En materia de buenas prácticas de prompting encontramos un conjunto de principios 
operativos orientados a mejorar la calidad, la fiabilidad y la controlabilidad de las 
respuestas generadas por modelos de lenguaje (Fagbohun et al., 2024).  
En primer lugar, la literatura subraya la importancia de formular instrucciones 
claras. Esto implica incluir detalles relevantes en la consulta, definir explícitamente la 
persona o el tono deseado, separar las distintas partes del encargo mediante delimitadores 
y especificar el formato esperado de la salida. La claridad inicial del prompt actúa como un 
marco que reduce la ambigüedad interpretativa del modelo. 
En segundo lugar, se destaca la necesidad de proporcionar un contexto relevante. El 
uso de textos de referencia, la aportación de información adicional, la descripción 
explícita del problema y la inclusión de ejemplos auxiliares permiten situar la tarea y 
acotar el espacio de respuesta, favoreciendo resultados más ajustados al objetivo 
planteado. 
Rol: 
Actúa como un especialista en análisis de legibilidad de textos 
en inglés. 
Contexto: 
El texto adjunto forma parte de una guía de uso en línea del 
catálogo de una biblioteca universitaria y está dirigido 
principalmente a estudiantes. 
Tarea: 
Calcula el índice de legibilidad SMOG del texto en inglés e 
interpreta brevemente el resultado en términos del nivel lector 
aproximado necesario para comprenderlo. 
Requisitos: 
− No reescribas, corrijas ni resumas el texto. 
− Aplica la fórmula estándar de SMOG: 1,0430 × √(número 
de palabras polisilábicas × 30 / número de frases) + 
3,1291. 
− Considera como palabras polisilábicas las palabras de 
tres o más sílabas. 
− Indica el número de frases analizadas y el número de 
palabras polisilábicas utilizadas en el cálculo. 
− Si el texto tiene menos de 30 frases, señala expresamente 
que el resultado es una estimación menos fiable. 
− No infieras datos no observables ni simules un cálculo 
exacto si no puedes contar de manera fiable frases o 

11 
palabras polisilábicas; en ese caso, indícalo como 
limitación. 
− Utiliza un tono descriptivo y no prescriptivo. 
Formato de salida: 
Un único párrafo en prosa que incluya el valor del índice, los 
datos básicos empleados en el cálculo y una breve interpretación 
del resultado. 
En esta misma línea, trabajos recientes (Leviathan et al., 2025) sugieren que, en 
determinadas tareas y, especialmente cuando no se solicita razonamiento paso a paso, la 
repetición íntegra del prompt puede contribuir a mejorar la respuesta del modelo. Esta 
estrategia parece resultar útil porque refuerza la disponibilidad del contexto dentro de la 
propia entrada y facilita que el modelo reutilice con mayor eficacia la información 
relevante, sobre todo en consultas donde el orden de los elementos puede condicionar la 
interpretación. Además, su interés práctico radica en que no modifica el formato de salida 
y, en términos generales, no comporta un aumento apreciable de la longitud de la 
respuesta, por lo que tampoco incrementa de forma significativa el coste asociado a la 
generación de tokens4 de salida. De este modo, puede entenderse como un ajuste simple 
de redacción y estructuración del prompt más que como una técnica compleja de 
razonamiento. 
Un tercer principio consiste en dividir las tareas complejas. Para ello, se recomienda 
clasificar la intención de la consulta, resumir o filtrar diálogos extensos, segmentar 
documentos largos en partes manejables y proporcionar pasos explícitos que el modelo 
pueda seguir. Esta descomposición facilita el tratamiento de problemas complejos 
mediante operaciones más simples y controlables.  
Asimismo, se señala la conveniencia de dar tiempo al modelo para “pensar”. En la 
práctica, esto se traduce en requerir explicaciones de las respuestas, utilizar monólogos 
internos o consultas intermedias, solicitar la autoevaluación del resultado y plantear 
preguntas de seguimiento. Estas estrategias fomentan respuestas más elaboradas y 
reflexivas. 
Rol: 
Actúa como asistente técnico especializado en tratamiento de 
datos tabulares, con conocimientos en normalización de datos, 
limpieza de registros y cálculo básico en hojas de cálculo y 
ficheros CSV. 
Contexto: 
Estoy trabajando con un conjunto de datos para un análisis 
académico y necesito preparar un fichero CSV a partir de una 
tabla con registros heterogéneos. La tarea consiste en 
estandarizar el contenido, detectar inconsistencias formales y 
 
4 Un token es una unidad mínima de texto en la que un modelo de lenguaje divide la entrada para poder 
procesarla, y puede corresponder a una palabra completa, a una parte de una palabra, a un signo de 
puntuación o a otros elementos del texto. 

12 
realizar cálculos simples que después serán revisados por una 
persona. 
Tarea general: 
Procesa la siguiente tabla de datos y prepara una salida en 
formato CSV limpia y coherente. 
Texto a analizar: 
[Aquí se facilitaría la tabla o los registros a la IA] 
Realiza la tarea siguiendo estrictamente estos pasos: 
1. Identifica la estructura de los datos y determina qué 
columnas contiene la tabla, explicando brevemente la 
función de cada una si puede inferirse del contenido. 
2. Limpia y normaliza los registros, corrigiendo únicamente 
aspectos formales como espacios sobrantes, mayúsculas 
y minúsculas inconsistentes, formatos de fecha, 
separadores decimales, valores vacíos o duplicados 
exactos. 
3. Genera el contenido en formato CSV, respetando una 
estructura uniforme de columnas y un criterio consistente 
de codificación de valores. 
4. Realiza los cálculos solicitados a partir de los datos ya 
normalizados, por ejemplo, recuentos, sumas, medias, 
porcentajes o subtotales, e indica claramente sobre qué 
campos se han aplicado. 
5. Autoevalúa el resultado, señalando qué transformaciones 
han sido puramente mecánicas y qué casos dudosos, 
ambiguos o incompletos deberían revisarse manualmente 
antes de dar el fichero por definitivo. 
Requisitos adicionales: 
− No inventes datos ausentes ni completes información que 
no aparezca en los registros originales. 
− Si detectas ambigüedades, consérvalas o señálalas 
explícitamente en lugar de resolverlas de forma arbitraria. 
− Utiliza un tono técnico, preciso y neutral. 
− Distingue claramente entre limpieza formal de datos e 
interpretaciones que requieran supervisión humana. 
Formato de salida: 
— Cinco apartados numerados, uno por cada paso del 
proceso. 
— Un bloque titulado “CSV generado”, que incluya 
exclusivamente el fichero CSV final. 
— Un bloque titulado “Cálculos realizados”, separado del 
anterior, con los recuentos, sumas, medias, porcentajes o 
métricas obtenidas. 
— Un bloque titulado “Casos que requieren revisión 
humana”, con ambigüedades, datos incompletos o 
decisiones no resueltas automáticamente. 

13 
Otro eje relevante es el uso de herramientas externas. Se contempla la posibilidad 
de dar acceso a ficheros externos, aprovechar capacidades de navegación web, solicitar 
la ejecución de código mediante alguna API5 o habilitar el uso de complementos 
relevantes. Estas prácticas amplían las capacidades del modelo más allá del texto 
proporcionado en el prompt.  
Finalmente, se recomienda probar los cambios de manera sistemática. Ajustar los 
prompts de forma incremental, evaluar los resultados intermedios, comenzar con 
consultas simplificadas y formular preguntas relacionadas permite refinar 
progresivamente la interacción y comprender mejor el impacto de cada modificación. 
Por su parte, Hewing y Leinhos (2024) identifican técnicas y enfoques adicionales 
que amplían el marco habitual del prompting y lo aproximan a una metodología más 
sistemática y reutilizable.  
En primer lugar, introducen explícitamente el diseño de Personas y audiencias 
como elementos diferenciados. No se trata solo de asignar un rol al modelo, sino de 
definir con detalle a quién va dirigido el resultado, incorporando características, 
expectativas y el nivel de conocimiento del público objetivo. Esta distinción entre 
Persona del modelo y audiencia del contenido añade una capa de precisión comunicativa 
que no siempre está presente en guías básicas de prompting.  
En segundo lugar, se refuerza la formulación de la tarea mediante la definición 
explícita de la intención y el objetivo, enfatizando el uso de verbos de acción y la 
delimitación clara del propósito del encargo. Este enfoque conecta el prompting con 
prácticas propias del diseño de tareas y de la redacción técnica orientada a objetivos.  
Otro aporte relevante es la separación entre contexto y referencias. Mientras el 
contexto recoge información situacional y de fondo, las referencias se conciben como 
fuentes concretas, datos esenciales o documentos específicos que deben ser utilizados o 
citados. Esta diferenciación es especialmente pertinente en entornos académicos y 
profesionales donde la trazabilidad de la información es crítica.  
También es importante explicitar la extensión, estructura y formato de la salida, 
incluyendo la solicitud de citas textuales o referencias a fuentes. 
En cuanto al estilo, se introduce la definición del tono como un elemento 
independiente, vinculado a atributos como calidad, lujo, cercanía o alineación con una 
marca o estilo de escritura determinado. 
Wang et al. (2024) plantean estrategias de prompting metacognitivo, orientadas a 
guiar no solo la producción de respuestas, sino también los procesos de razonamiento 
que el propio modelo despliega para alcanzarlas. En este enfoque, el prompt no se limita 
a formular una instrucción o tarea, sino que estructura la interacción en fases 
secuenciales de reflexión y control cognitivo, lo que contribuye a mejorar la coherencia, 
la explicabilidad y la fiabilidad de los resultados. 
En concreto, proponen una secuencia de cinco etapas que pueden integrarse de 
forma explícita en el diseño del prompt. La primera corresponde a la clarificación de la 
 
5 Interfaz de programación de aplicaciones. Es un punto de acceso o conjunto de funciones con sintaxis 
definida que permite a un programa utilizar servicios o capacidades de otro sistema. 

14 
comprensión, en la que se solicita al modelo que explicite su interpretación inicial de la 
tarea o de las preguntas planteadas. Esta fase cumple una función análoga a la 
verificación de requisitos en el diseño de sistemas, ya que permite detectar 
ambigüedades conceptuales o malentendidos antes de avanzar hacia el razonamiento 
propiamente dicho. La segunda etapa consiste en un juicio preliminar, donde el modelo 
formula una primera evaluación basada en similitudes semánticas, contexto o contenido 
general. Se trata de una estimación inicial, deliberadamente provisional, que actúa como 
hipótesis de trabajo y que prepara el terreno para análisis más profundos. Este paso 
resulta especialmente útil en tareas de clasificación, comparación o detección de 
equivalencias conceptuales, ya que separa la intuición inicial del análisis crítico 
posterior. A continuación, el análisis crítico o evaluación reflexiva introduce una revisión 
explícita del juicio preliminar. En esta fase se invita al modelo a reconsiderar su 
evaluación inicial, contrastarla con matices relevantes, excepciones o criterios 
adicionales, y, si es necesario, reformular su posición. Este mecanismo de autorevisión 
es clave para reducir errores derivados de respuestas superficiales y se alinea con las 
recomendaciones de “dar tiempo al modelo para pensar”, ya que fuerza un razonamiento 
más deliberado y estructurado. La cuarta etapa corresponde a la confirmación de la 
decisión, en la que el modelo debe emitir un juicio final explícito y justificarlo de manera 
razonada. Esta fase consolida el proceso argumentativo y permite obtener respuestas 
más transparentes, al hacer explícitos los criterios empleados y la lógica que sustenta la 
conclusión alcanzada. Finalmente, se incorpora una evaluación de la confianza, 
solicitando al modelo que estime el grado de seguridad de su respuesta, generalmente en 
términos porcentuales, y que explique las razones de dicha valoración. Aunque esta 
autoevaluación no equivale a una medida objetiva de fiabilidad, sí que aporta una señal 
adicional sobre la estabilidad del razonamiento y la claridad de los criterios aplicados, lo 
que puede resultar útil en contextos académicos, analíticos o de apoyo a la toma de 
decisiones. 
Integradas en el marco general de buenas prácticas, estas estrategias de prompting 
metacognitivo refuerzan los principios previamente descritos. La claridad de 
instrucciones se amplía hacia la claridad del proceso; la descomposición de tareas 
incorpora fases explícitas de reflexión y revisión; y la evaluación sistemática de cambios 
se ve enriquecida por la posibilidad de analizar no solo la respuesta final, sino también 
las etapas intermedias del razonamiento. De este modo, el prompting deja de ser una 
técnica puramente instrumental para convertirse en un dispositivo metodológico que 
estructura, documenta y controla el proceso cognitivo del modelo de lenguaje. 

15 
  
  


16 
 
En el uso de estas herramientas conviene seguir algunas convenciones de sintaxis para 
estructurar mejor los prompts.  
En líneas generales, es preferible situar las instrucciones al inicio y separar 
claramente instrucciones y contexto mediante delimitadores con el fin de reducir 
ambigüedades y mejorar la fiabilidad de la respuesta. Open AI (2025) recomienda, por 
ejemplo, usar los caracteres ### o """ para introducir el contexto. Por ejemplo: 
Extrae del texto: título, autor, fecha y tema principal. Devuelve un 
JSON válido. 
Texto: """ 
{aquí el texto} 
"""  
También Open AI (MacCallum y Lee, 2025) en sus directrices para desarrolladores 
recomienda usar marcado ligero en Markdown6 para las secciones y subsecciones 
principales, así como para jerarquías más profundas si es necesario, listas, etc. También 
usar comillas invertidas simples (backticks) en línea o bloques delimitados por backticks 
para envolver el código con precisión, y listas estándar numeradas o con viñetas cuando 
sea necesario. 
# Análisis de logs de servidor 
## Objetivo 
Identifica las causas más probables de errores **500** y propón acciones 
correctivas. 
 
6 Markdown es un lenguaje de marcado ligero para dar estructura básica al texto. Los backticks son comillas 
invertidas usadas en Markdown para delimitar código en línea o bloques de código 


17 
## Entrada 
### Contexto 
- Entorno: ‘Ubuntu 22.04’ 
- Servidor web: ‘Nginx’ 
- App: ‘PHP-FPM’ 
- Ventana temporal: 2026-02-01 a 2026-02-15 
### Logs 
``` 
{aquí los logs} 
Al utilizar prompts complejos que incorporan varios componentes (instrucciones, 
contexto, ejemplos…), el uso de lenguajes de marcas estructurados ayuda a los LLM a 
interpretarlos con mayor precisión. Con ellos es posible desarrollar prompts más claros, 
estructurados, precisos, flexibles y reutilizables (resulta más fácil añadir, eliminar o 
modificar secciones fácilmente) o incluso que tanto el usuario como el modelo puedan 
referirse más fácilmente a secciones concretas del prompt bien identificadas (Claude, 
2026). En el caso de utilizar lenguajes de marcas como XML o JSON (MacCallum y Lee, 
2025), es importante ser consistentes durante toda la interacción con el LLM. 
<prompt> 
  <instructions> 
    Resume el contenido de <context> en 5–7 viñetas. 
    - No añadas ni asumas nada que no aparezca en el texto. 
    - Mantén nombres propios y fechas exactamente como aparecen. 
  </instructions> 
  <formatting> 
    Devuelve la respuesta así: 
    <output> 
      <bullet_points> 
        - ... 
      </bullet_points> 
    </output> 
  </formatting> 
 
  <context> 
    <document title="Informe de actividad" date="2026-02-10"> 
      {aquí el texto a resumir} 
    </document> 
  </context> 
 
  <examples> 
    <example> 
      <output> 
        <bullet_points> 
          - El proyecto comenzó en enero de 2025. 
          - Participaron Ana y Luis. 
          - El objetivo fue digitalizar 300 incunables. 
        </bullet_points> 
      </output> 
    </example> 
  </examples> 
</prompt> 

18 
Si no se desea utilizar una sintaxis tan verbosa, como mínimo se recomienda 
utilizar prefijos de entrada / salida para marcar semánticamente partes de contenido 
(Gemini, 2025). 
Instrucción: {aquí la instrucción} 
Texto: ```{aquí el texto que debe procesar}``` 
Formato de salida: {aquí el formato de salida deseado} 
Al trabajar con ficheros conviene tanto trabajar con formatos estructurados (mejor 
un CSV que un PDF), como explicar en el prompt cómo se encuentran organizados los 
datos en esos ficheros. 
En el diseño de prompts conviene partir de un principio sencillo: el prompt no debe 
convertirse en un canal para manejar secretos. Esto implica evitar la exposición 
indirecta por “comodidad” (pegarlas en el contexto, en ejemplos o prompt) de nombres 
de usuario, contraseñas, claves API, entre otros. El objetivo es reducir el riesgo de 
exfiltración –por filtrado en la propia respuesta, por registro en logs, o por propagación 
a herramientas externas– y asumir que, si un secreto entra en el contexto del modelo, 
deja de estar bajo nuestro control (OWASP, 2025). Relacionado con lo anterior, hay que 
tratar los prompts como semipúblicos. En la práctica, un atacante puede intentar forzar 
su revelado de forma directa (solicitándolo) o indirecta (mediante inyección de 
instrucciones, contenido recuperado en RAG7 o manipulación de herramientas), y 
además puede inferir parte de la lógica de control observando respuestas. 
Finalmente, un área especialmente sensible es la salida del modelo cuando se 
convierte en entrada de otros sistemas. Esta situación se da, por ejemplo, cuando se 
solicita código SQL, comandos, scripts, reglas de cortafuegos, consultas a APIs u otros. 
Una buena práctica es especificar formatos estructurados y requisitos de seguridad (“no 
generes comandos destructivos”, “no incluyas payloads”, “documenta supuestos”), 
pero, sobre todo, asumir que el texto generado no se debe ejecutar ni desplegar sin 
validación previa (OWASP, 2025). Esto exige controles y revisión humana en acciones 
de alto impacto y pruebas en entornos aislados. La idea es evitar “copiar-pegar y 
ejecutar” y optar por un flujo de trabajo en el que el modelo se limita a producir 
borradores.  
 
7 Técnica que combina un modelo generativo con recuperación de información externa, incorporando al 
prompt fragmentos recuperados de una base documental para mejorar la actualización y la precisión 
factual de la respuesta. 

19 
Estrechamente relacionado con el apartado anterior, otro aspecto importante es no 
introducir datos personales identificables, credenciales, códigos, claves API, 
conexiones a bases de datos o cualquier otro tipo de información sensible. Para trabajar 
con seguridad es imprescindible anonimizar o seudonimizar (sustituir datos reales por 
alias como [Persona A] o [Empresa B]), eliminar o generalizar campos innecesarios 
(fechas exactas, ubicaciones concretas, números de identificación reales…) y compartir 
únicamente el mínimo fragmento de texto o datos requerido para obtener una respuesta 
útil. En esa misma línea, conviene evitar adjuntar documentos completos si no es 
estrictamente necesario. Es preferible pegar extractos acotados, recortar tablas a las 
columnas relevantes, resumir el contexto con variables o plantillas, y revisar antes de 
enviar que no queden “rastros” en metadatos, encabezados, firmas, capturas o rutas de 
archivo. Estas medidas reducen la exposición, facilitan el cumplimiento normativo y 
minimizan riesgos de filtración o reutilización indebida de información. Finalmente, 
cuando se trata de información extremadamente sensible se debe priorizar el uso de 
modelos de código abierto e instalados en local, frente a servicios disponibles en abierto 
en la nube. 
Al trabajar específicamente con imágenes, conviene evitar rostros, direcciones, 
documentos fotografiados, credenciales o códigos identificables. También resulta 
imprescindible eliminar todos los metadatos incrustados (EXIF, XMP, IPTC…)8 en los 
ficheros antes de cargarlos, entre ellos puede haber información de localización, fechas, 
modelos de dispositivos, identificadores, notas, entre otros. Para ello se pueden utilizar 
herramientas como ExifTool.9 
Más allá de los metadatos, es importante revisar otros datos “invisibles” o no 
perceptibles a primera vista como reflejos en cristales, miniaturas incrustadas en el 
fichero (por ejemplo, en formatos RAW), capas en formatos como DNG o TIF. Esto 
incluye también los nombres de los ficheros, los cuales en algunos casos pueden ser 
muy informativos. 
Por supuesto, no deben integrarse datos relacionados con menores u otros 
colectivos vulnerables.  
 
8 EXIF es un conjunto de metadatos técnicos incrustados en imágenes y otros ficheros; XMP es una 
tecnología estandarizada para incrustar metadatos en ficheros; IPTC es un estándar ampliamente usado 
para metadatos descriptivos, administrativos y de derechos en imágenes. 
9 En esta guía se muestra cómo realizarlo: Alcaraz Martínez, Rubén (2026). Guía de uso de ExifTool. 
https://hdl.handle.net/2445/226841 

20 
Las consideraciones éticas en el diseño de prompts son fundamentales (Tokayev, 2023), 
ya que, pese a las notables capacidades de los LLM, estos presentan desafíos éticos 
relevantes que deben abordarse para garantizar un uso responsable y seguro. Entre ellos 
destaca la capacidad de generar salidas sesgadas (O’Neil, 2017), derivadas tanto de los 
datos de entrenamiento como del propio diseño de los prompts. Estos sesgos pueden 
manifestarse en estereotipos, prejuicios o representaciones injustas de determinados 
grupos o ideas (Tokayev, 2023). Los sesgos ocupan un lugar central entre las cuestiones 
éticas. No obstante, por su importancia y dado que su mitigación exige técnicas 
específicas de formulación y revisión, este aspecto se aborda de forma específica en el 
apartado siguiente. 
Con todo, el prompting ético no se limita a la reducción de sesgos, sino que implica 
la elaboración de prompts alineados con normas y valores sociales, orientados a 
promover la equidad y a fomentar respuestas constructivas (Shaikh et al., 2022). Con ello 
se busca asegurar que las salidas respeten principios éticos y contribuyan positivamente 
al bienestar colectivo, lo que exige evaluar cuidadosamente las posibles consecuencias 
de los prompts y guiar a los LLM hacia la generación de contenidos responsables y 
socialmente aceptables mediante la reformulación iterativa de las respuestas (Ma et al., 
2023). En este marco, también resulta necesario considerar como riesgo la posible 
reproducción no autorizada de contenidos preexistentes. Investigaciones recientes 
(Liu et al., 2026) han mostrado que, bajo determinadas condiciones, los modelos pueden 
llegar a reactivar y reproducir fragmentos literales o muy próximos a obras protegidas 
por derechos de autor, incluso a partir de instrucciones semánticas que no contienen el 
texto original. Este hallazgo cuestiona la idea de que los modelos únicamente “aprenden 
patrones” de forma abstracta y obliga a incorporar al análisis ético del prompting la 
posibilidad de inducir, aunque sea de manera no intencional, respuestas que repliquen 
expresiones protegidas o excesivamente dependientes de materiales ajenos. 
Un primer aspecto que resulta necesario considerar antes de interactuar con un 
LLM es si contamos con el consentimiento y la autorización necesaria al utilizar 
contenido de terceros en los prompts. Esta precaución es especialmente relevante 
cuando se introducen materiales que no son de elaboración propia o que contienen 
información no destinada a su difusión o reutilización en este tipo de herramientas, 
como materiales docentes, trabajos de estudiantes, correos electrónicos, informes 
internos, manuscritos en evaluación, actas de reuniones o documentos profesionales 
compartidos en contextos de confianza. Estas prácticas pueden plantear problemas 
éticos –y, en algunos casos, legales– si no existe autorización expresa de las personas 
implicadas. Del mismo modo, introducir fragmentos de entrevistas, expedientes o 
evaluaciones sin una anonimización adecuada puede vulnerar compromisos de 
confidencialidad. Incluso cuando el contenido introducido no sea sensible, ciertos 
prompts pueden empujar al modelo a reconstruir o aproximarse en exceso a textos 
protegidos, especialmente si se le solicita continuar, expandir, reescribir “en el mismo 
estilo” o desarrollar pasajes a partir de resúmenes detallados. Por ello, antes de usar 

21 
este tipo de materiales conviene verificar la legitimidad de su uso, valorar si el 
tratamiento es proporcional a la finalidad perseguida y, cuando sea posible, optar por 
versiones anonimizadas, sintetizadas o con datos ficticios equivalentes. Del mismo 
modo, conviene formular las instrucciones de manera que promuevan la elaboración 
original, la síntesis y la transformación crítica, y no la reproducción de expresiones 
reconocibles o atribuibles a terceros. 
Otro aspecto fundamental gira en torno a la necesaria supervisión y validación 
humana de las respuestas obtenidas. Los autores deben responder siempre por el 
resultado final, evitando delegar decisiones sensibles de forma automática en el sistema. 
Esta exigencia es especialmente importante cuando las respuestas del LLM pueden 
influir en decisiones profesionales, recomendaciones a terceros o comunicaciones con 
impacto reputacional, jurídico o social. Por ejemplo, emitir una recomendación 
profesional basada en un resumen no verificado, o redactar una respuesta institucional 
sobre un asunto delicado sin comprobar datos, tono y contexto, puede trasladar 
indebidamente al sistema una responsabilidad que corresponde a la persona. Además de 
posibles errores factuales (alucinaciones), los LLM pueden omitir matices relevantes, 
introducir formulaciones ambiguas o presentar con excesiva seguridad contenidos 
discutibles. Asimismo, pueden generar pasajes indebidamente próximos a fuentes 
preexistentes sin señalizarlo de forma clara, lo que incrementa el riesgo de reutilización 
acrítica de materiales ajenos. Por ello, su uso debe entenderse como el propio de una 
herramienta de soporte a la redacción, no como sustituto del juicio experto, lo que 
implica revisar críticamente las respuestas, contrastar la información cuando proceda, 
verificar la originalidad y adecuación del contenido generado y asumir explícitamente la 
responsabilidad sobre la versión final. 
El uso de la IA debe declararse, especialmente cuando su intervención haya 
influido en la búsqueda de información, la elaboración de contenidos, la redacción, el 
análisis o la toma de decisiones, y con mayor motivo en contextos académicos, 
científicos, profesionales o institucionales donde la transparencia metodológica y la 
atribución de responsabilidades resultan esenciales. Esta exigencia de transparencia 
también resulta pertinente porque permite contextualizar cómo se han obtenido 
determinadas formulaciones, síntesis o propuestas textuales y advertir de los límites del 
proceso, incluidos los riesgos de sesgo, error o dependencia excesiva de materiales 
previos. 
Resnik y Hosseini (2025) proponen una serie de escenarios en los que el uso de la IA 
debe declararse obligatoriamente, opcionalmente o en los que no es necesario, en el 
marco de investigaciones y publicaciones académicas (tabla 1). 

22 
Tabla 1. Criterios y ejemplos de usos de la IA que deben declararse obligatoriamente, de forma opcional 
o que no son necesarios declarar de acuerdo con Resnik y Hosseini (2025). 
Categoría Criterio Ejemplos 
Obligatoria La declaración debe ser obligatoria 
solo cuando el uso de IA sea 
intencional y sustancial. El uso de IA 
es sustancial cuando 1) produce 
evidencia, análisis o discusión que 
sustenta o desarrolla las 
conclusiones/hallazgos de un 
estudio; o 2) afecta directamente al 
contenido de la investigación / 
publicación. La declaración del uso 
de IA debe ser obligatoria cuando 
cumpla al menos uno de estos 
criterios: (a) La herramienta de IA 
toma decisiones que afectan 
directamente a los resultados de la 
investigación; (b) La herramienta de 
IA genera o sintetiza contenido, datos 
o imágenes; o (c) La herramienta de 
IA analiza contenido, datos o 
imágenes. 
— Para formular preguntas o hipótesis, diseñar y 
realizar experimentos. 
— Para redactar partes del artículo, resumir, 
parafrasear, revisar significativamente o 
sintetizar contenido textual. 
— Para traducir partes o la totalidad del artículo. 
— Para recopilar, analizar, interpretar o 
visualizar datos (cuantitativos o cualitativos). 
— Para extraer datos para la revisión de la 
literatura (sistemática o no) e identificar 
lagunas de conocimiento. 
— Para generar datos e imágenes sintéticos 
utilizados en la investigación. 
Opcional Los autores distinguen tres 
situaciones (obligatoria, opcional e 
innecesaria). En el caso de la 
categoría opcional, la adscripción se 
apoya en ejemplos y en 
consideraciones contextuales. 
— Para editar texto existente en cuanto a 
gramática, ortografía u organización. 
— Para encontrar referencias o verificar la 
pertinencia de referencias encontradas por 
humanos. 
— Para encontrar y generar ejemplos para 
contenido existente. 
— Para hacer lluvia de ideas y ofrecer 
sugerencias para la organización de un 
artículo o el título de un artículo/sección. 
— Para validar u ofrecer retroalimentación sobre 
ideas, texto y código existentes 
Innecesaria La declaración es innecesaria cuando 
el uso de la IA no es sustancial. 
— Para sugerir palabras o frases que mejoren la 
claridad / legibilidad de una oración existente. 
— Como parte de una operación más amplia en la 
que la IA no está generando ni sintetizando 
contenido ni tomando decisiones de 
investigación; por ejemplo, cuando la IA está 
integrada en otros sistemas/máquinas. 
— Como asistente digital, por ejemplo, para 
ayudar a organizar y mantener los activos 
digitales y los flujos de trabajo de un proyecto. 
 

23 
En continuidad con las cuestiones éticas expuestas en el apartado anterior, este 
apartado se centra la identificación y mitigación de sesgos en la formulación de prompts 
y en la revisión de las respuestas. 
Es sabido que los LLM son sensibles a ciertos sesgos. Los sesgos algorítmicos 
consisten en que el modelo puede producir respuestas sistemáticamente inclinadas, 
injustas, estereotipadas o desiguales hacia ciertos grupos, ideas, lenguas, culturas o 
perspectivas (Comisión Europea, 2019). Los sesgos no se limitan a un desequilibrio 
demográfico o a la representatividad de los datos. El marco AI RMF 1.0 (NIST, 2023) 
distingue al menos tres grandes categorías de sesgo: sistémico, computacional / 
estadístico y humano-cognitivo, y subraya que pueden aparecer incluso sin una voluntad 
discriminatoria. Esta distinción es especialmente útil en el contexto de los LLM, ya que 
permite entender que los sesgos observables en las respuestas pueden derivar tanto del 
corpus y los procesos algorítmicos como de los marcos organizativos y de las propias 
interpretaciones humanas durante el diseño, uso y evaluación del sistema. Por ello, los 
diseñadores de prompts deben ser conscientes de estos riesgos y actuar de forma 
proactiva para mitigarlos, revisando y depurando las formulaciones con el fin de evitar la 
reproducción de estereotipos dañinos o contenido discriminatorio. 
En líneas generales, los LLM son sensibles a sesgos en al menos dos sentidos: (1) 
pueden reproducir sesgos en sus respuestas porque han aprendido a partir de datos y 
decisiones humanas; y (2) pueden activar sesgos como resultado de un prompt 
tendencioso que influye en la respuesta. Por lo tanto, tanto el preentrenamiento, como el 
contexto de trabajo, la formulación de los prompts o, incluso los criterios de 
parametrización y ajuste de la herramienta (qué se considera una respuesta adecuada, 
etc.), pueden producir sesgos en un sentido determinado (Torres-Salinas, 2025). 
Los sesgos derivados de un entrenamiento específico pueden, en parte, mitigarse 
mediante prompts que delimiten explícitamente el alcance de la consulta e incorporen 
diversidad geográfica, cultural, temporal y epistemológica. Así, en lugar de formular 
preguntas como “¿Quién inventó la medicina moderna?”, podríamos aproximarnos 
mediante formulaciones tales como: “¿Cómo se desarrolló la medicina moderna a partir 
de aportaciones de diferentes tradiciones médicas y contextos históricos?”, con el 
objetivo de evitar reproducir el posible desequilibrio en la representación de temas, 
culturas, tradiciones, etc., sobrerepresentadas durante el entrenamiento. Ahora bien, la 
reformulación de prompts para mitigar sesgos no debe llevar a una “corrección” acrítica 
de signo contrario. Es recomendable revisar las respuestas para comprobar que la 
búsqueda de diversidad y representación no produzca selecciones forzadas, 
desproporcionadas o poco justificadas en relación con la evidencia disponible, la 
relevancia histórica o el contexto de la consulta. En otras palabras, mitigar sesgos no 
consiste en sustituir un canon limitado por una lista artificial, sino en ampliar y 
contextualizar la respuesta con criterios explícitos y una representatividad razonada. 
En el caso de los sesgos introducidos a través de las instrucciones, uno que 
puede darse de forma habitual es el sesgo de confirmación. Por ejemplo, preguntas como 

24 
¿Por qué el teletrabajo reduce la productividad? o ¿Por qué las redes sociales dañan la 
salud mental? Introducen afirmaciones implícitas que orientan la respuesta hacia una 
conclusión predeterminada y pueden reforzar un sesgo de confirmación, en lugar de 
favorecer un análisis equilibrado de factores, contextos y evidencias. En este sentido, 
formulaciones como “¿Qué efectos tiene el teletrabajo sobre la productividad según el 
tipo de tarea, sector y condiciones laborales?” o “¿Qué relación existe entre redes 
sociales y salud mental, y qué factores pueden generar efectos positivos o negativos?” 
permiten desplazar la consulta desde una premisa cerrada hacia un enfoque analítico 
más abierto, contextualizado y matizado, favoreciendo respuestas que consideren 
variables, condiciones y resultados diversos en lugar de confirmar una hipótesis previa. 
Los ejemplos anteriores recogen ejemplos de sesgos culturales derivados del 
preentrenamiento o de confirmación en la instrucción escrita por el usuario. Otros 
posibles sesgos que conviene mitigar son: 
— Geográficos: se produce cuando la pregunta o la respuesta privilegia 
implícitamente realidades, referencias o criterios de una región (a menudo 
occidentales), presentándolos como universales. Por ejemplo, “¿Cuál es el 
mejor modelo educativo?” frente “¿Compara modelos educativos de 
diferentes países o regiones, indicando fortalezas, limitaciones y contexto de 
aplicación?” 
— De generalización: se produce cuando se atribuyen rasgos, conductas o 
carencias a un grupo amplio (por edad, país, generación, etc.) como si fuera 
homogéneo. Por ejemplo, “¿Por qué los jóvenes no leen?” o “¿Por qué las 
personas mayores no entienden las tecnologías?, en lugar de “¿Qué hábitos 
de lectura presentan distintos grupos de jóvenes y qué factores influyen en 
ellos?” o “¿Qué barreras y facilitadores influyen en la adopción tecnológica 
en cada grupo de edad?”). 
— De lenguaje valorativo: aparece cuando la formulación incorpora términos 
con carga emocional, moral o ideológica que orientan la respuesta hacia una 
interpretación previa. Por ejemplo, “¿Cuáles son las ideologías más 
peligrosas?” en lugar de “¿Qué riesgos y efectos históricos se han asociado a 
distintas ideologías en determinados contextos, y según qué criterios se 
evalúan?”). 
— Sesgo temporal o presentista: se produce cuando se juzgan prácticas, 
ideas o procesos del pasado con categorías o expectativas del presente, o 
cuando se presupone que lo más reciente es necesariamente superior. Por 
ejemplo, “Las metodologías tradicionales ya no sirven, ¿verdad?”, en lugar 
de “¿Qué ventajas y limitaciones presentan metodologías tradicionales y 
contemporáneas según el tipo de aprendizaje?”. 
— Sesgo binario o de falsa dicotomía: aparece cuando la pregunta reduce un 
problema complejo a dos opciones excluyentes, ignorando alternativas 
intermedias, combinaciones o matices. Por ejemplo, “¿Es mejor la 
enseñanza presencial o la online?” en lugar de “¿Qué ventajas y limitaciones 

25 
tienen la enseñanza presencial, online e híbrida según objetivos, perfil del 
alumnado y contexto?”. 
— Sesgo de anclaje: aquí la primera premisa o dato del prompt fija un marco 
que condiciona la respuesta. Por ejemplo, “Partiendo de que el fracaso 
escolar se debe principalmente a la falta de esfuerzo…” 
— Sesgo de encuadre: cuando en la formulación se introduce un marco 
semántico que orienta la interpretación. Por ejemplo, “¿Cómo evitar que la 
regulación ahogue la innovación?” en lugar de “¿Cómo pueden diseñarse 
marcos regulatorios que equilibren innovación, competencia, seguridad y 
derechos?” 
— Sesgo por omisión: se produce cuando se dejan fuera perspectivas, grupos, 
periodos o contraejemplos relevantes. Por ejemplo, “Dame una lista de los 
grandes filósofos de la historia”, que puede dejar fuera a ciertas tradiciones 
o a filósofas en el corpus de entrenamiento. 
Finalmente, es importante tener en cuenta que un mismo prompt puede activar 
varios sesgos simultáneamente. En este sentido, resulta útil identificar cuál es el sesgo 
principal que estructura la pregunta y qué sesgos secundarios lo refuerzan, para poder 
reformularla de manera más precisa, contextualizada y equilibrada, pero teniendo en 
cuanta también que no se debe alterar innecesariamente la intención de la consulta. 
En líneas generales el factor más ligado al consumo energético es la longitud de la 
respuesta y no tanto la longitud del prompt (Adamska et al., 2025). No obstante, 
elementos del prompt como el tipo de tarea, complejidad, apertura / cierre de la 
instrucción, entre otros, influyen de forma significativa en la extensión de la respuesta. 
En este sentido, algunas recomendaciones para producir prompts más “verdes” son 
(Adamska et al., 2025): 
— Diseñar prompts que induzcan respuestas más cortas. 
— No asumir que un prompt más corto será necesariamente más eficiente. Es 
decir, recortar tokens del prompt por sí mismo, no tiene un impacto 
significativo en el consumo energético. 
— Formular prompts muy específicos y con instrucciones muy concretas, ya 
que reducen la necesidad de incurrir en varias interacciones con el LLM 
hasta que devuelva lo que se precisa. 
— Utilizar proyectos y referirse en los prompts a datos, documentos o 
instrucciones facilitadas previamente al LLM. 
— Solicitar salidas en formatos restringidos y concretos. Por ejemplo, 
especificando el lenguaje de programación, estructura del código esperado, 
bloques o apartados de la respuesta, entre otros. 
— Evitar solicitar explicaciones detalladas si no son imprescindibles. 
— Solicitar sólo aquellos fragmentos necesarios que deben modificarse, por 
ejemplo, en un código fuente, fórmula, etc. 

26 
En la literatura encontramos clasificaciones de las técnicas de prompting determinadas 
fundamentalmente por facetas funcionales y operativas, con un fuerte anclaje en el tipo de 
problema que se quiere resolver con el prompt: área de aplicación (por ejemplo, 
razonamiento y lógica, manejo de emociones y tono, entre otras) qué aspecto del LLM se 
quiere estimular o corregir (razonamiento secuencia, uso de conocimiento externo, 
autorreflexión…), estrategias de mitigación de problemas conocidos (alucinaciones, 
coherencia, fidelidad…) (Sahoo et al., 2025). Otros autores basan su clasificación en 
facetas cognitivas, comunicativas y pragmáticas del uso de prompts: tipo de estrategia 
cognitiva o comunicativa empleada, rol del prompt en la interacción humano-modelo, 
grado de control frente a la salida, dimensión multimodal u orientación práctica y 
experiencial (Fagbohun et al., 2024).  
Si atendemos a la faceta cognitiva, funcional o interactiva que activan en el modelo, 
podemos clasificar las técnicas de prompting bajo las categorías que se recogen en la tabla 
2, la cual, si bien no es totalmente exhaustiva, sí que presenta una amplia representación 
de las técnicas recogidas en la literatura. 
Tabla 2. Técnicas de prompting. 
Dimensión Subdimensión Técnicas Referencias 
Razonamiento y 
resolución estructurada 
Razonamiento 
secuencial básico 
Zero-shot prompting 
Few-shot prompting 
Brown et al., 2020; 
Harrison et al., 2023; 
Kojima et al., 2022; 
Radford et al., 2019 
Razonamiento paso 
a paso 
Chain-of-thought (CoT) 
Automatic CoT 
Self-consistency 
Fagbohun et al., 2024; 
Kojima et al., 2022; Lyu 
et al., 2023; Wang et al., 
2023; Wei et al., 2022; 
Zhang et al., 2022 
Razonamiento 
estructural 
Logical CoT (LogiCoT) 
Chain-of-symbol (CoS) 
Skeleton-of-thought (SoT) 
Layer-of-Thoughts (LoT) 
Prompting 
Fagbohun et al., 2024; 
Fungwacharakorn et al., 
2024; Hu et al., 2023; 
Ning et al., 2023; Zhao et 
al., 2023b 
Exploración de 
trayectorias 
Tree-of-thoughts (ToT) 
Graph-of-thoughts (GoT) 
Thread-of-thought (ThoT) 
Buffer of thoughts (BoT) 
Fagbohun et al., 2024; 
Long, 2023; Yang et al., 
2024b; Yao et al., 2023; 
Zhou et al., 2023 
Razonamiento 
narrativo y sintético 
Narrative-of-thought (NoT) 
Chain of draft (CoD) 
Zhang et al., 2024 

27 
Dimensión Subdimensión Técnicas Referencias 
Fiabilidad y verificación Anclaje en 
conocimiento 
externo 
Retrieval-augmented 
generation (RAG) 
Chain-of-Knowledge (CoK) 
Lewis et al., 2020; Li et 
al., 2023a 
 
Verificación interna Chain-of-Verification (CoVe) 
Chain-of-Note (CoN) 
Dhuliawala et al., 2023; 
Sahoo et al., 2025; Yu et 
al., 2024 
Contraste y 
corrección 
Contrastive CoT (CCoT) 
Responsive feedback 
prompting 
Chia et al., 2023; 
Fagbohun et al., 2024; 
Paul et al., 2023; Zheng 
et al., 2023 
Metacognición y 
autorregulación 
Refinamiento 
iterativo 
Self-refine prompting Madaan et al., 2023 
Abstracción del 
problema 
Take a step back prompting Zheng et al., 2023 
Reflexión sobre el 
proceso 
Self-reflection prompting 
Meta-Prompting 
Fagbohun et al., 2024; 
Madaan et al., 2023; 
Shinn et al., 2023; Wang 
y Zhao, 2024 
Anticipación Anticipatory prompting Fagbohun et al., 2024; 
Contexto y dinámica 
conversacional 
Contexto en 
ventana de 
atención 
In-Context prompting Dong et al., 2024; 
Fagbohun et al., 2024; 
Rubin et al., 2021; Ye et 
al., 2022 
Gestión del diálogo Conversational prompting 
Socratic prompting 
Chang, 2023; Fagbohun 
et al., 2024; Liu et al., 
2023a; Wei et al., 2023 
Gestión de roles Multi-Personas prompting Fagbohun et al., 2024; 
Gu et al., 2023 
Selección 
adaptativa 
Active prompting Diao et al., 2023 
Control del objetivo 
y del output 
Clarificación 
semántica 
Rephrase and respond (RaR) Deng et al., 2023 
Direccionamiento 
del output 
Show-me vs tell-me 
Target-your-response (TAR) 
Fagbohun et al., 2024; 
Perez et al., 2021; Zhao 
et al., 2021 
Planificación macro Prompt macros 
End-goal planning 
Fagbohun et al., 2024; 
Restricción formal Constrained vocabulary 
prompting 
Fagbohun et al., 2024; 
Reformulación en 
código 
Code prompting 
Prompt to code 
Chen et al., 2023; 
Fagbohun et al., 2024; 
Puerto et al., 2024 

28 
Dimensión Subdimensión Técnicas Referencias 
Dimensión afectiva 
y estilística 
Emoción y tono Emotion prompting Li et al., 2023b 
Multimodalidad e 
interdisciplinariedad 
Multimodalidad Multimodal prompting 
Visual prompting 
Bang et al., 2023; 
Fagbohun et al., 2024; 
Lee et al., 2023 
Integración 
disciplinar 
Cross-disciplinary prompting Fagbohun et al., 2024; 
Harrison et al., 2023 
Contextualización Historical context prompting 
Modular prompting 
Fagbohun et al., 2024; 
Liu et al., 2023b 
Creatividad y 
generación abierta 
Exploración abierta Ambiguous prompting Fagbohun et al., 2024; 
Creatividad guiada Directional stimulus 
prompting 
Fagbohun et al., 2024; 
Shum et al., 2023 
Inversión de roles Flipped interaction 
prompting 
Fagbohun et al., 2024; 
Reescritura 
expresiva 
Grammar correction (no 
puramente mecánica) 
Fagbohun et al., 2024; 
En los siguientes apartados se explican con algo más de detalle cada una de las 
técnicas recogidas en la tabla anterior y se incluyen ejemplos centrados específicamente 
en ilustrar el funcionamiento de cada una de ellas. No obstante, en contextos reales de 
uso, estas técnicas no suelen aparecer de forma aislada, sino integradas en prompts más 
extensos y combinadas con otras estrategias, restricciones o elementos de 
contextualización. 
Esta dimensión agrupa técnicas de prompting diseñadas para inducir en el modelo 
procesos explícitos de razonamiento, descomposición lógica y exploración sistemática 
de soluciones, ya sea mediante razonamiento secuencial, estructurado, narrativo o 
multitrayectoria.10 Mediante estas técnicas de procesamiento lógico y secuencial se espera 
que el LLM aborde tareas de razonamiento complejas y de múltiples pasos dividiéndolas 
en etapas manejables. Los métodos que se encuadran dentro de esta categoría se basan en 
la idea de fragmentar la tarea en componentes más pequeños, y cuentan con una 
justificación científica y matemática que respalda su aplicación. Estas metodologías no 
solo mejoran las capacidades de resolución de problemas de los modelos, sino que 
también proporcionan un marco para un razonamiento más intuitivo y “similar” al 
humano (Yu et al., 2023). 
Su objetivo principal es mejorar la capacidad del modelo para abordar tareas 
complejas que requieren inferencias encadenadas, planificación o análisis paso a 
 
10 El concepto “multitrayectoria” se refiere aquí a la capacidad inducida por el prompt para que el modelo 
genere, explore y evalúe más de una cadena de razonamiento posible antes de producir una respuesta final. 

29 
paso, sin modificar los parámetros del modelo. Entre las técnicas que podemos distinguir 
en esta categoría encontramos: zero-shot prompting, few-shot prompting, chain-of-thought 
(CoT), automatic CoT, self-consistency, logical CoT (LogiCoT), chain-of-symbol (CoS), 
skeleton-of-thought (SoT), layer-of-thoughts (LoT), tree-of-thoughts (ToT), graph-of-thoughts 
(GoT), thread-of-thought (ThoT), buffer of thoughts (BoT), narrative-of-thought (NoT), chain 
of draft (CoD). 
El prompting de disparo cero (zero-shot prompting), sin ejemplos o sin 
entrenamiento específico previo supone un cambio de paradigma en el uso de los LLM de 
gran tamaño, al prescindir de la necesidad de contar con amplios conjuntos de datos de 
entrenamiento. En su lugar, esta técnica se basa en instrucciones cuidadosamente 
diseñadas que orientan al modelo en la realización de tareas nuevas o no vistas 
previamente. En este enfoque, el modelo recibe una descripción explícita de la tarea 
dentro del prompt, sin disponer de ejemplos que establezcan correspondencias concretas 
entre entradas y salidas. A partir de ahí, el modelo explota el conocimiento adquirido 
durante su preentrenamiento para generar respuestas coherentes con la tarea planteada. 
(Harrison et al., 2023; Kojima et al., 2022; Radford et al., 2019). 
Ejemplo 
Interpreta los siguientes valores agregados (medias y desviaciones 
estándar) obtenidos en un estudio sobre la satisfacción de 
usuarios. 
Explica qué indican estos resultados de forma comprensible para 
un público no especializado en estadística. 
Evita tecnicismos innecesarios y no introduzcas conclusiones no 
sustentadas por los datos. 
En el ejemplo anterior, el modelo recibe solo la tarea y los datos, sin ejemplos de 
interpretaciones previas. Se confía en su capacidad para traducir indicadores estadísticos 
básicos a un lenguaje no especializado. 
El prompting de pocos disparos o con pocos ejemplos (few-shot prompting) 
consiste en proporcionar al modelo un número reducido de ejemplos de pares entrada-
salida con el objetivo de facilitar la comprensión de una tarea concreta (Brown et al., 
2020). Incluso la inclusión de unos pocos ejemplos bien seleccionados ha demostrado 
mejorar de forma significativa el rendimiento de los modelos en tareas complejas. Esta 
técnica implica el uso de tokens adicionales para incorporar dichos ejemplos, lo que puede 
resultar limitante cuando se trabaja con entradas de texto extensas. Asimismo, la 
selección y formulación de los ejemplos dentro del prompt pueden influir de manera 
notable en el comportamiento del modelo, por ejemplo, introduciendo sesgos (Brown et 
al., 2020).  

30 
Ejemplo 
Analiza el nivel de uso de los servicios digitales de una biblioteca 
pública a partir de los siguientes ejemplos. 
Ejemplo 1 
Datos: 
— Préstamos de libros electrónicos mensuales: 850 
— Accesos a la biblioteca digital infantil: 2.400 
Análisis: 
El número de accesos a la biblioteca digital infantil es 
notablemente superior al préstamo de libros electrónicos, lo que 
sugiere una alta demanda de recursos digitales orientados a 
público infantil y familiar, posiblemente vinculada a actividades 
educativas o de ocio supervisado. 
Ejemplo 2 
Datos: 
— Consultas al catálogo en línea: 7.200 
— Renovaciones de préstamos en línea: 1.900 
Análisis: 
La diferencia entre las consultas al catálogo y las renovaciones 
indica que el catálogo se utiliza principalmente como herramienta 
de exploración y búsqueda, mientras que la gestión activa de 
préstamos digitales presenta un uso más moderado. 
Tarea 
Aplica el mismo tipo de análisis al siguiente conjunto de datos: 
Datos: 
— Reservas en línea de documentos físicos: 1.150 
— Reservas presenciales de documentos físicos: 310 
En el ejemplo anterior, se incluyen dos ejemplos completos11 de entrada-salida, 
adaptados al contexto de una biblioteca pública. Los ejemplos fijan el tipo de indicadores, 
el nivel interpretativo y el registro. El modelo debe reconocer el patrón analítico mostrado 
y reproducirlo en un nuevo caso, sin instrucciones adicionales sobre cómo razonar. 
El prompting de cadena de razonamiento (chain-of-thought o CoT) provoca que el 
modelo “piense” de manera secuencial al procesar la información paso a paso (Wei et al., 
2022; Kojima et al., 2022; Lyu et al., 2023). En lugar de saltar directamente a una 
conclusión, esta técnica induce al modelo a tomarse un momento para descomponer 
consultas complejas en pasos intermedios explicables. Al hacer que el modelo “muestre 
su trabajo” y razone de forma lógica a través de cada etapa de la resolución de problemas, 
suele observarse un aumento general en la precisión de sus soluciones. Viene a solucionar 
las dificultades que los LLM presentan a la hora de abordar tareas que requieren 
razonamiento complejo (Wei et al., 2022). 
  
 
11 Reducidos en este documento por razones de espacio. 

31 
Ejemplo 
Analiza los siguientes datos de uso de una biblioteca pública y 
determina cuál de los servicios digitales presenta un mayor nivel 
de adopción relativa. 
Explica tu razonamiento paso a paso antes de presentar la 
conclusión final. 
Datos: 
— Usuarios activos totales de la biblioteca: 12.000 
— Usuarios que han utilizado el préstamo digital al menos 
una vez: 2.400 
— Usuarios que han utilizado el catálogo en línea al menos 
una vez: 6.600 
— Usuarios que han utilizado el servicio de referencia virtual 
al menos una vez: 900 
Estructura tu respuesta en dos partes: 
— Razonamiento paso a paso 
— Conclusión final 
En el ejemplo anterior, se solicita explícitamente que el modelo muestre el 
razonamiento intermedio, no solo el resultado. El análisis requiere varios pasos lógicos 
encadenados: 1) relacionar usuarios de cada servicio con el total, 2) comparar 
proporciones relativas, y 3) interpretar qué significa “mayor nivel de adopción”. La 
estructura del prompt separa claramente proceso y resultado. Por otro lado, no se 
proporcionan ejemplos previos, por lo que el foco no está en el aprendizaje por imitación 
(few-shot), sino en la externalización del razonamiento. La técnica permite revisar la 
coherencia del análisis, detectar errores de interpretación, así como aumentar la 
transparencia del proceso. 
El prompting de cadena de razonamiento automático (automatic chain-of-thought 
o automatic CoT) se basa en un enfoque que permite generar de forma automática cadenas 
de razonamiento a partir de instrucciones sencillas, como el prompt “vamos a pensar paso 
a paso”, animando al modelo a explicar su razonamiento paso a paso sin necesidad de 
ejemplos previamente preparados (Zhang et al. 2022). En la práctica, el método selecciona 
diferentes preguntas y genera varias explicaciones alternativas para cada una, 
construyendo así un conjunto más amplio y variado de ejemplos. Este procedimiento 
reduce la probabilidad de errores sistemáticos y mejora el rendimiento del few-shot 
prompting, evitando al mismo tiempo el esfuerzo manual que supone crear cadenas de 
razonamiento de forma explícita (Sahoo et al., 2025).  

32 
Ejemplo 
Vamos a razonar paso a paso. 
A partir de los siguientes resultados de un test de usabilidad en el 
sitio web de una institución cultural, identifica cuál es el principal 
problema de experiencia de usuario. 
Datos: 
— Porcentaje de usuarios que completan una tarea sin ayuda: 
42 % 
— Tiempo medio de finalización de la tarea: 6 minutos 
— Porcentaje de usuarios que abandonan antes de finalizar: 
31 % 
Explica el razonamiento de forma ordenada antes de presentar la 
conclusión. 
En el ejemplo anterior, no se define una estructura formal del razonamiento a 
diferencia del ejemplo aplicado a CoT (“Estructura tu respuesta en dos partes: 
razonamiento paso a paso y conclusión final”). Por otro lado, se utiliza un disparador 
genérico (“vamos a pensar paso a paso”). Por su parte, el modelo genera autónomamente 
la cadena de razonamiento: decide cuántos pasos, cómo organizarlos y cómo expresarlos. 
El prompting de consistencia interna (self-consistency) es una estrategia de 
decodificación orientada a mejorar el rendimiento en tareas de razonamiento complejo, 
donde pueden existir múltiples trayectorias de razonamiento igualmente válidas. Esta 
técnica genera diversas cadenas de razonamiento alternativas, cada una siguiendo un 
camino lógico diferente (Wang et al., 2022). 
Ejemplo 
A partir de los siguientes datos de una biblioteca universitaria, 
formula distintas interpretaciones razonadas sobre el grado de uso 
del repositorio institucional. 
Tras considerar esas interpretaciones, indica cuál resulta más 
consistente con los datos disponibles. 
Datos: 
— Descargas de documentos: 42.000 
— Usuarios únicos del repositorio: 9.800 
— Usuarios totales de la comunidad universitaria: 28.000 
En el ejemplo anterior, se solicita explícitamente la generación de múltiples 
razonamientos alternativos a partir de los mismos datos. Cada razonamiento sigue un 
camino lógico independiente. La respuesta final se basa en la consistencia entre las 
distintas cadenas de razonamiento, no en una única trayectoria. El objetivo es mejorar el 
rendimiento en tareas de razonamiento complejo, reduciendo la dependencia de una sola 
explicación potencialmente errónea. 
El prompting de cadena de razonamiento lógico (logical CoT o LogiCoT) viene a 
intentar resolver las limitaciones del chain-of-thought prompting en lo que respecta a la 
verificación de la corrección de los razonamientos. Este enfoque alternativo de carácter 

33 
neurosimbólico integra principios de lógica simbólica con el fin de promover un 
razonamiento más coherente y estructurado (Zhao et al., 2023b). A través de un ciclo 
iterativo de pensar-verificar-revisar, este enfoque contribuye a reducir errores lógicos y 
alucinaciones (Sahoo et al., 2025). 
Ejemplo 
Analiza el siguiente argumento sobre la arquitectura de la 
información de un sitio web institucional. 
1. Identifica la conclusión planteada. 
2. Comprueba si las premisas conducen lógicamente a esa 
conclusión. 
3. Revisa el razonamiento si detectas saltos lógicos.12 
Premisas: 
— El 70 % de los usuarios accede al contenido desde el menú 
principal. 
— El menú principal contiene más de 12 opciones de primer 
nivel. 
Conclusión inicial: 
“La arquitectura de la información es clara y eficiente.” 
En el ejemplo anterior, el prompt introduce explícitamente un proceso de 
verificación del razonamiento, no solo su exposición. El razonamiento se articula en un 
ciclo iterativo de pensar, verificar y revisar. Se emplean criterios lógicos básicos para 
comprobar si las conclusiones se derivan correctamente de las premisas. El objetivo es 
detectar y corregir errores lógicos, alineándose con la función del LogiCoT de reducir 
razonamientos incorrectos o poco fundamentados.  
El prompting de cadena de símbolos (chain-of-symbol o CoS) consiste en una 
técnica que sustituye el lenguaje natural por representaciones simbólicas condensadas 
como soporte del razonamiento (Hu et al., 2023). Esto permite construir prompts más 
claros y concisos, refuerza la capacidad de razonamiento espacial de los modelos y 
facilita la interpretación humana de los procesos de razonamiento. No obstante, también 
plantea desafíos importantes, entre ellos la escalabilidad del enfoque, su capacidad de 
generalización, la integración con otras técnicas de prompting y la interpretación del 
razonamiento simbólico generado por el modelo (Sahoo et al., 2025).  
 
12 Por ejemplo, cuando el modelo afirma una conclusión, sin que esta se derive de forma necesaria o 
justificada de las premisas o datos proporcionados. 

34 
Ejemplo 
Modela el siguiente razonamiento sobre la arquitectura de la 
información utilizando símbolos. 
Leyenda: 
— M = número de opciones de menú 
— T = tasa de éxito de tareas 
— A = tasa de abandono 
Datos: 
— M > 10 
— T = 45 % 
— A = 35 % 
Objetivo: 
Representar simbólicamente la relación entre complejidad del 
menú y desempeño del usuario. 
En el ejemplo anterior, la forma de razonamiento (no necesariamente todo el prompt) 
no se articula en lenguaje natural, sino mediante representaciones simbólicas 
condensadas. Se utilizan símbolos definidos explícitamente en el propio prompt como 
soporte del razonamiento. El foco no está en narrar o explicar, sino en estructurar el 
razonamiento de forma abstracta y compacta. 
El prompting de esqueleto de razonamiento (skeleton-of-thought o SoT) 
proporciona al modelo un “esqueleto” o estructura de alto nivel que debe completar. Este 
enfoque permite al modelo generar contenido en paralelo dentro de secciones previamente 
definidas, manteniendo al mismo tiempo una organización clara y coherente (Ning et al., 
2023). Al ofrecer una estructura previa, se reduce el riesgo de desviaciones irrelevantes y 
se mejora la consistencia global de la salida generada (Fagbohun et al., 2024). 
Ejemplo 
Para redactar un correo electrónico, se puede proporcionar al 
modelo un esquema como:  
[Saludo] – [Introducción del tema] – [Cuerpo principal] – [Cierre] – 
[Firma]  
En el ejemplo anterior, el modelo completa cada sección respetando la estructura de 
alto nivel indicada, produciendo un resultado bien organizado y alineado con el propósito 
comunicativo. 
El prompting de capas de razonamiento (layer-of-thoughts o LoT) introduce un 
marco jerárquico de razonamiento que emplea jerarquías de restricciones para 
estructurar el proceso inferencial, con el objetivo de mejorar tanto la precisión en la 
recuperación de la información como la interpretabilidad de los resultados 
(Fungwacharakorn et al., 2024). Utilizado en el ámbito de la recuperación de documentos 
legales, el LoT organiza el razonamiento en distintos niveles, diferenciando entre 
pensamientos de capa y pensamientos de opción, y aplica restricciones de forma 

35 
secuencial para filtrar y refinar progresivamente las respuestas candidatas (Sahoo et al., 
2025). 
Ejemplo 
Analiza la calidad de un sitio web institucional aplicando un 
razonamiento por capas jerárquicas. 
Capa 1 – Accesibilidad 
Evalúa el grado de cumplimiento de los criterios de accesibilidad 
más relevantes y determina si existen barreras críticas. 
Capa 2 – Usabilidad 
Analiza los resultados de los test conducidos para identificar 
problemas de usabilidad. 
Capa 3 – Experiencia global 
Integra los resultados de las capas anteriores para valorar la 
experiencia de usuario del sitio web. 
Datos disponibles: 
— Accesibilidad 
— Cumplimiento WCAG 2.1 nivel A: completo 
— Cumplimiento WCAG 2.1 nivel AA: parcial 
— Errores de contraste detectados: 14 
— Formularios sin etiquetas asociadas: 3 
— […] 
— Usabilidad 
— Tasa de éxito de tareas: 47 % 
— Tiempo medio de realización de tareas: 5 minutos y 
40 segundos 
— Tasa de abandono antes de completar la tarea: 33 
% 
— Solicitudes de ayuda durante la prueba: 41 % de los 
usuarios 
— […] 
Contexto de uso 
— Acceso desde dispositivos móviles: 62 % 
— Acceso desde escritorio: 38 % 
En el ejemplo anterior, el razonamiento sigue organizado en capas jerárquicas. Cada 
capa introduce nuevas restricciones y refina progresivamente la interpretación de la capa 
anterior. 
El prompting de árbol de razonamientos (tree-of-thoughts o ToT) y el de grafo de 
razonamientos (graph-of-thoughts o GoT) extienden el razonamiento secuencial lineal 
hacia estructuras más ramificadas. En lugar de seguir una única cadena de pensamiento, 
estas técnicas permiten al modelo explorar múltiples trayectorias de razonamiento en 
paralelo, evaluando diferentes alternativas o escenarios posibles (Besta et al., 2023; Long, 
2023; Fagbohun et al., 2024; Yao et al., 2023). El ToT organiza estas trayectorias en forma 
de árbol, mientras que el GoT permite conexiones más complejas entre ideas, 

36 
representadas como un grafo. Ambas aproximaciones amplían los métodos secuenciales 
tradicionales para alinearse mejor con las características no lineales del pensamiento 
humano (Sahoo et al., 2025). 
Ejemplos ToT:  
Analiza distintas opciones para mejorar el servicio de referencia 
virtual de una biblioteca pública. 
Explora varias alternativas posibles de forma independiente y 
analiza para cada una sus ventajas y limitaciones antes de 
formular una conclusión final. 
Considera, al menos, las siguientes dimensiones: 
— Accesibilidad del servicio, 
— Carga de trabajo del personal, 
Calidad de la atención al usuario 
Ejemplo GoT: 
Examina las relaciones entre los distintos componentes del 
sistema de información de una biblioteca universitaria. 
Considera las interdependencias entre: 
— Repositorio institucional 
— Sistemas de descubrimiento 
— Políticas de acceso abierto 
— Apoyo a la investigación 
Analiza el problema teniendo en cuenta conexiones cruzadas entre 
estos elementos, no como procesos independientes. 
En el primer ejemplo anterior, este tipo de instrucción anima al modelo a considerar 
diversas posibilidades antes de converger en una solución final. Cada alternativa 
constituye una rama independiente de razonamiento, analizada por separado. El objetivo 
no es solo razonar paso a paso, sino comparar escenarios posibles antes de converger en 
una decisión. En el segundo caso, el razonamiento no se organiza como un árbol 
jerárquico ni como una secuencia lineal. Por otro lado, se invita explícitamente al modelo a 
considerar conexiones cruzadas entre distintos elementos del problema. 
El prompting de hilo de razonamiento (thread-of-thought o ThoT) es una técnica de 
prompting inspirada en la cognición humana que busca mejorar el razonamiento mediante 
el análisis progresivo de la información. En lugar de procesar el contexto de forma global, 
el ThoT lo descompone sistemáticamente en segmentos manejables, lo que permite un 
razonamiento incremental y más controlado (Zhou et al., 2023).  

37 
Ejemplo 
Analiza el siguiente informe sobre el uso de servicios de una 
biblioteca pública aplicando el siguiente procedimiento: 
— Resume y analiza cada apartado del informe por separado. 
— A continuación, integra los resultados parciales para 
formular una interpretación global del uso de los servicios. 
Informe: 
— Apartado 1: Datos de uso del préstamo digital 
— Apartado 2: Datos de uso del catálogo en línea 
— Apartado 3: Datos del servicio de referencia virtual 
El enfoque se articula en un proceso de dos fases. En primer lugar, el modelo resume 
y analiza cada segmento de manera individual en partes más manejables, posteriormente, 
integra y refina la información obtenida para generar una respuesta final coherente. Esta 
técnica favorece un razonamiento incremental y controlado, especialmente adecuado para 
contextos extensos o complejos. Una de las principales fortalezas de esta técnica es su 
flexibilidad, ya que puede incorporarse como un módulo y mejorar el razonamiento en 
distintos modelos y en combinación con otros métodos de prompting (Sahoo et al., 2025). 
El buffer de razonamientos (buffer of thoughts o BoT) introduce un enfoque 
orientado a mejorar el razonamiento de los LLM mediante el uso de patrones de 
razonamiento reutilizables de alto nivel, con el objetivo de equilibrar universalidad, 
eficiencia y robustez. En lugar de generar razonamientos desde cero para cada consulta, el 
BoT almacena y reutiliza estructuras de razonamiento previamente aprendidas que 
pueden adaptarse a distintas tareas. El método se apoya en dos componentes principales: 
un meta-buffer, que actúa como repositorio de patrones de razonamiento abstractos, y un 
gestor dinámico, encargado de recuperar y adaptar las plantillas más adecuadas en 
función de la tarea planteada (Yang et al., 2024b). 
Ejemplo 
Meta-buffer (plantilla guardada) 
“Ordenar + punto de corte (h)” 
− Reúne la lista de citas por publicación. 
− Ordena de mayor a menor:  c1 ≥ c2 ≥ ⋯ ≥ cn 
− Recorre las posiciones i =1..n y busca el mayor i tal que ci ≥ i 
− Devuelve h = i 
− Verificación final: verifica el “borde”:  ch ≥ h y (si existe) ch + 1 
< h + 1 
Prompt 
Una investigadora tiene 8 artículos con estas citas: 
25,10,8,5,4,3,1,0 ¿Cuál es su índice h?”  
El prompting de narrativas de razonamiento (narrative-of-thought o NoT) se 
orienta a abordar el razonamiento temporal. Para ello, introduce una estrategia de 
prompting que mejora la capacidad del modelo para razonar sobre secuencias temporales 

38 
sin necesidad de un entrenamiento adicional. El enfoque se basa en estructurar la 
información y el razonamiento de forma narrativa, facilitando la comprensión de 
relaciones temporales complejas (Zhang et al., 2024). La técnica se articula en torno a tres 
componentes fundamentales. En primer lugar, emplea una representación estructurada 
de la información que puede implementarse mediante clases en Python u otros formatos 
estructurados (tabular, etc.), que permite modelar explícitamente eventos y relaciones 
temporales. En segundo lugar, utiliza una plantilla de prompting con un enfoque narrativo 
que guía al modelo en la construcción del razonamiento. Por último, incorpora 
demostraciones alineadas con la narrativa, lo que refuerza la coherencia temporal del 
razonamiento generado. En conjunto, esta combinación permite mejorar de forma efectiva 
el razonamiento temporal de los LLM sin modificar sus parámetros internos (Sahoo et al., 
2025). 
Ejemplo 
1) Representación estructurada de eventos y relaciones 
temporales 
Evento 1 (2019) 
— Hecho: Implantación del repositorio institucional de una 
universidad. 
— Consecuencia: Se crea por primera vez una infraestructura 
formal para el acceso abierto a la producción científica. 
Evento 2 (2020) 
— Hecho: Aprobación de una política institucional de acceso 
abierto. 
— Consecuencia: El depósito de publicaciones pasa de ser 
voluntario a estar recomendado institucionalmente. 
Relación temporal: 
— La política institucional se apoya en la infraestructura 
creada con la implantación previa del repositorio. 
Evento 3 (2021) 
— Hecho: Integración del repositorio institucional con los 
sistemas de evaluación académica. 
— Consecuencia: El depósito de publicaciones comienza a 
tener impacto directo en los procesos de evaluación del 
personal investigador. 
Relación temporal: 
— La integración solo es posible tras la existencia de una 
política institucional que legitima el uso del repositorio. 
Evento 4 (2022) 
— Hecho: Puesta en marcha de campañas de formación 
dirigidas al personal investigador. 
— Consecuencia: Mejora tanto el volumen como la calidad de 
los depósitos realizados. 
Relación temporal: 

39 
— Las acciones formativas responden a los problemas 
detectados tras el aumento del uso del repositorio en fases 
anteriores. 
2) Plantilla de prompting con enfoque narrativo 
A partir de los eventos descritos, construye una narración 
razonada que explique la evolución temporal de la política de 
acceso abierto en la universidad. 
Relata los acontecimientos en orden cronológico, explicando cómo 
cada evento condiciona el siguiente y cómo se va consolidando el 
proceso a lo largo del tiempo. 
Presenta el razonamiento como una narración coherente en prosa, 
evitando listas o esquemas. 
3) Demostración alineada con la narrativa (ejemplo previo que 
sirve de guía) 
Demostración: 
En una fase inicial, la implantación del repositorio institucional 
permitió establecer una base técnica para el acceso abierto, 
aunque su adopción fue todavía limitada. Posteriormente, la 
aprobación de una política institucional formalizó este 
compromiso y favoreció un aumento progresivo de los depósitos. 
Con el paso del tiempo, la integración del repositorio en los 
sistemas de evaluación académica transformó esta tendencia en 
un crecimiento sostenido, al vincular el acceso abierto con 
incentivos profesionales. Finalmente, las campañas de formación 
contribuyeron a consolidar el modelo, mejorando no solo la 
cantidad, sino también la calidad de los contenidos depositados. 
4) Tarea solicitada al modelo (instanciación) 
Utilizando la misma lógica narrativa que en el ejemplo anterior, 
explica la evolución del proceso descrito en los eventos 
proporcionados, destacando la relación temporal y causal entre 
ellos. 
En el ejemplo anterior, los eventos están claramente delimitados y las relaciones 
temporales y de dependencia son explícitas. Por otro lado, mediante la plantilla el 
modelo es guiado para razonar en forma de narración temporal, priorizando la 
coherencia cronológica y causal. Finalmente, el ejemplo previo muestra cómo articular la 
historia de forma coherente.  
El prompting de cadena de borradores (chain of draft o CoD) (Xu et al., 2025) es 
una estrategia diseñada para mejorar la eficiencia del razonamiento. A diferencia de CoT, 
CoD genera salidas concisas y densas en información en cada paso, reduciendo el 
consumo de tokens y la latencia sin sacrificar precisión.  

40 
Ejemplo 
Evalúa los resultados de una prueba de usabilidad mediante una 
cadena de borradores concisos. 
— Borrador 1: identifica únicamente los indicadores críticos. 
— Borrador 2: expresa la conclusión principal en una frase a 
basada únicamente en el borrador 1. 
Datos: 
— Tasa de éxito de tareas: 46 % 
— Tasa de abandono: 34 % 
— […] 
El razonamiento se desarrolla en borradores sucesivos, no en una cadena extensa de 
explicaciones. Cada borrador es intencionalmente breve y denso en información. El 
segundo borrador se apoya exclusivamente en el anterior, refinando el resultado sin 
reexplicar el proceso. El enfoque permite mantener la precisión del razonamiento con 
menor coste computacional que el método CoT. 
Esta dimensión agrupa técnicas de prompting orientadas a mejorar la fiabilidad, la 
factualidad y la robustez de las respuestas generadas por los LLM, abordando de forma 
explícita uno de sus principales límites: la generación de contenidos incorrectos, 
incompletos o no verificables, comúnmente descritos como alucinaciones. A diferencia de 
las técnicas centradas en el razonamiento interno del modelo, este conjunto de enfoques 
introduce mecanismos de contraste, verificación, validación externa o retroalimentación 
iterativa, con el objetivo de reforzar la calidad epistémica de las salidas. 
Las técnicas incluidas en esta categoría se apoyan en estrategias como la 
incorporación de conocimiento externo, la verificación paso a paso de las respuestas, la 
evaluación crítica de los propios razonamientos del modelo o la corrección guiada 
mediante feedback. Mediante estos mecanismos, se busca que el LLM no solo genere una 
respuesta plausible, sino que pueda justificarla, contrastarla o revisarla, aproximándose a 
prácticas humanas de comprobación y validación de la información. Este enfoque resulta 
especialmente relevante en contextos sensibles o de alto riesgo, como la investigación 
académica, la educación, la salud, el ámbito jurídico o la toma de decisiones informadas. 
Entre las técnicas que se encuadran en esta categoría se incluyen: retrieval-
augmented generation (RAG), chain-of-knowledge (CoK), chain-of-verification (CoVe), 
chain-of-note (CoN), contrastive CoT (CCoT) y responsive feedback prompting. 
La generación aumentada por recuperación (retrieval-augmented generation o 
RAG) integra de forma directa la recuperación de información en el proceso de 
generación mediante prompts (Lewis et al., 2020). Con esta técnica se busca mitigar la 
dependencia de datos de entrenamiento y su posible falta de actualización, pertinencia o 
calidad, la cual dificulta la producción de respuestas precisas en tareas que requieren 
acceso a conocimiento externo o actualizado. En estos escenarios, el prompting 
tradicional resulta insuficiente y, en muchos casos, obliga a recurrir a costosos procesos 

41 
de reentrenamiento (Sahoo et al., 2025). El enfoque RAG analiza la entrada del usuario, 
formula una consulta específica y recupera información relevante desde una base de 
conocimiento previamente construida. Los fragmentos obtenidos se incorporan al 
prompt original, enriqueciéndolo con contexto adicional. Este prompt aumentado 
permite al modelo generar respuestas que combinan creatividad con mayor precisión 
factual. 
Ejemplo 
Utilizando los siguientes documentos institucionales recuperados, 
describe las obligaciones del personal investigador respecto al 
depósito de publicaciones en el repositorio institucional. 
Basa la respuesta únicamente en los textos proporcionados. 
Documentos recuperados [documentos adjuntos]: 
— Política institucional de acceso abierto 
— Guía de depósito en el repositorio 
En el ejemplo anterior, podemos hablar de un caso de RAG manual en el que es el 
usuario quien selecciona los documentos y los proporciona directamente en el prompt 
para exigir una respuesta que se base en ellos. 
El prompting de cadena de conocimiento (chain-of-knowledge o CoK) plantea un 
enfoque que descompone sistemáticamente las tareas complejas en pasos coordinados. 
El proceso se inicia con una fase de preparación del razonamiento, en la que se delimita 
el contexto y se formula con precisión el problema. A continuación, el modelo entra en 
una etapa dinámica de adaptación del conocimiento, en la que recopila y contrasta 
evidencias procedentes de múltiples fuentes, incluyendo su conocimiento interno, 
recursos externos y la información aportada en el propio prompt (Li et al., 2023a). 
Ejemplo 
Explica por qué un sitio web institucional debe cumplir 
determinados criterios de accesibilidad, enlazando de forma 
explícita los distintos niveles normativos que lo justifican. 
Organiza las afirmaciones de forma que cada una se apoye en la 
anterior, evitando afirmaciones no fundamentadas. 
Para cada afirmación relevante, indica explícitamente el 
documento, norma o fuente de la que procede. 
Información disponible [documentos adjuntos]: 
— Directiva (UE) 2016/2102 del Parlamento Europeo y del 
Consejo, de 26 de octubre de 2016, relativa a la 
accesibilidad de los sitios web y aplicaciones para 
dispositivos móviles de los organismos del sector público. 
— España. Real Decreto 1112/2018, de 7 de septiembre, sobre 
accesibilidad de los sitios web y aplicaciones para 
dispositivos móviles del sector público. Boletín Oficial del 
Estado, núm. 217, de 8 de septiembre de 2018, pp. 88444–
88462. 

42 
— World Wide Web Consortium (W3C). (2018). Web Content 
Accessibility Guidelines (WCAG) 2.1. W3C 
Recommendation, 5 June 2018. 
En el ejemplo anterior, el foco no está en el razonamiento interno del modelo, sino 
en la organización explícita del conocimiento. La respuesta se construye como una 
cadena de piezas informativas enlazadas, donde cada una fundamenta la siguiente. Se 
hace visible de dónde procede cada afirmación, reforzando la fiabilidad y trazabilidad del 
contenido generado. Esta técnica resulta especialmente útil en contextos normativos, 
institucionales o donde la justificación documental es clave. 
El prompting de cadena de verificación (chain-of-verification o CoVe) busca 
mitigar el problema de las alucinaciones en los LLM mediante un enfoque que introduce 
un proceso estructurado de verificación interna en varias etapas. En concreto, el método 
se articula en cuatro pasos: (1) el modelo genera una respuesta inicial, (2) formula de 
manera explícita preguntas de verificación destinadas a comprobar la validez de su 
propio razonamiento, (3) responde a dichas preguntas de forma independiente, y (4) 
produce una respuesta final revisada que integra los resultados del proceso de 
verificación (Dhuliawala et al., 2024). El CoVe emula los mecanismos humanos de 
comprobación y revisión, contribuyendo a mejorar la coherencia y la precisión de las 
salidas generadas. 
Ejemplo 
Paso 1 (respuesta inicial) 
Explica cuáles suelen ser las obligaciones del personal 
investigador respecto al depósito de publicaciones en el repositorio 
institucional. 
Paso 2 (cadena de verificación) 
Identifica las afirmaciones clave (por ejemplo: obligatoriedad, 
plazos, tipos de documentos, excepciones) que requieren 
verificación. 
Paso 3 (comprobación interna) 
Evalúa cada afirmación y determina si está plenamente justificada 
por lo que has dicho o si has introducido supuestos. 
Paso 4 (versión final) 
Produce una versión final depurada, eliminando o matizando lo no 
verificado. 
En el ejemplo anterior, se separan explícitamente una respuesta inicial de un 
proceso posterior de verificación en cadena. La verificación no se plantea como una 
única revisión general, sino como una secuencia de comprobaciones sobre afirmaciones 
clave. El resultado final es una respuesta revisada, donde se depura lo no verificado y se 
intentan eliminar todas las incertidumbres. 
El prompting de cadena de notas (chain-of-note o CoN) aplica un enfoque 
orientado a mejorar la robustez de los documentos en implementaciones RAG mediante 

43 
un proceso sistemático de evaluación de la relevancia de los documentos recuperados, 
priorizando la información crítica y fiable y filtrando el contenido que no resulta 
pertinente (Yu et al., 2023). Este método se centra en generar notas de lectura 
secuenciales que sirven como una capa de razonamiento adicional entre los documentos 
recuperados y la respuesta final (Greyling, 2023). 
Ejemplo 
Pregunta: 
¿Puede una biblioteca pública limitar el acceso al préstamo digital 
a determinados perfiles de usuarios? 
Documentos recuperados (o pasados al LLM): 
— Reglamento de uso de bibliotecas públicas (artículos 2–6) 
— Política municipal de servicios digitales 
— Nota de prensa sobre actividades culturales digitales 
Instrucciones (CoN): 
Lee cada documento y redacta notas breves indicando qué 
información es relevante para responder a la pregunta. 
Clasifica cada documento como: 
a) responde directamente a la pregunta, 
b) aporta contexto útil pero no una respuesta directa, 
c) no es relevante para la pregunta. 
Y justifica el uso o descarte de cada documento. 
Elabora la respuesta final solo a partir de las notas relevantes. 
Si ningún documento permite responder con seguridad, indícalo 
explícitamente. 
En el ejemplo anterior, en vez de pasar directamente los documentos recuperados 
al modelo para que construya la respuesta, CoN instruye al LLM a leer esos textos 
primero y generar notas de lectura que capturen los puntos clave, permitan evaluar la 
relevancia de cada fragmento respecto a la consulta e identifiquen qué partes son útiles y 
cuáles no. En este caso en concreto, teóricamente se evitaría que el modelo use la nota 
de prensa (ruido). Además, se obliga a justificar el uso de descarte de cada documento. 
Sus principales limitaciones son que los documentos recuperados (o pasados al LLM) 
pueden no incluir una respuesta clara y, por otro lado, la recuperación de información 
puede incluir fragmentos irrelevantes o fuera de dominio. 

44 
 
Figura 1. Síntesis del método chain-of-note (CoN). Fuente: Greyling, 2023. 
El prompting de cadena de razonamiento contrastiva (contrastive CoT o CCoT) 
aborda la carencia de aprender a partir de los errores presentes en la técnica CoT. Con 
este enfoque se complementa los prompts convencionales con demostraciones de 
razonamiento tanto correctas como incorrectas (Chia et al., 2023). 
Ejemplo 
Prompt 
Una biblioteca universitaria dispone de 90.000 € para recursos 
electrónicos. 
Se asignan 40.000 € a revistas electrónicas. 
Del presupuesto restante, se reserva un 25 % para renovaciones. 
¿Cuánto presupuesto queda disponible? 
Explicación correcta 
— Restante: 90.000 − 40.000 = 50.000 
— Reserva: 50.000 × 0,25 = 12.500 
— Disponible: 50.000 − 12.500 = 37.500 € 
Explicación incorrecta 
Se reserva el 25 % del total inicial (22.500 €). 
Este razonamiento es incorrecto porque: 
— Aplica el porcentaje al total inicial en lugar de al 
presupuesto restante. 
Pregunta 
A partir del presupuesto correctamente calculado, la biblioteca 
decide destinar 15.000 € adicionales a nuevas bases de datos 
¿Cuánto presupuesto queda finalmente sin asignar? 
Salida 
Presupuesto disponible inicial: 37.500 € 
Tras la nueva asignación: 37.500 − 15.000 = 22.500 € 
 


45 
El prompting con retroalimentación adaptativa (responsive feedback prompting) 
consiste en proporcionar retroalimentación directa al modelo inmediatamente después 
de que haya generado una respuesta. Esta retroalimentación se utiliza para guiar la 
siguiente salida del modelo, refinando progresivamente el resultado (Paul et al., 2023; 
Zheng et al., 2023). 
Ejemplo 
El contenido es correcto, pero necesito que se destaque mejor qué 
pasos son obligatorios y cuáles opcionales. 
Ante esta petición el modelo ajusta el documento reorganizando la estructura y 
marcando explícitamente los pasos críticos.  
Las técnicas de metacognición y autorreflexión se centran en mejorar las capacidades 
asistenciales de los LLM mediante prompts introspectivos, la anticipación de necesidades 
del usuario y la generación de código. Estas técnicas fomentan que el modelo evalúe, 
revise o amplíe sus propias respuestas (Fagbohun et al., 2024; Wang y Zhao, 2024). 
Las técnicas introducidas en esta sección incluyen: self-refine prompting, take a step 
back prompting, self-reflection prompting, y el meta-Prompting y anticipatory prompting. 
El prompting de autorefinamiento (self-refine prompting) es una técnica orientada 
a mejorar el rendimiento de los LLM mediante un proceso de refinamiento iterativo de las 
respuestas, basado en retroalimentación generada por el propio modelo y análogo a los 
procesos de revisión humana. Aunque los LLM son capaces de abordar una amplia 
variedad de tareas, suelen presentar limitaciones cuando se enfrentan a objetivos 
complejos, metas poco definidas o razonamientos que requieren múltiples pasos, lo que 
puede dar lugar a respuestas iniciales imprecisas o con fallos lógicos. Inspirado en los 
mecanismos de revisión iterativa propios de la cognición humana, esta técnica introduce 
un procedimiento estructurado en tres etapas: en primer lugar, el modelo genera una 
respuesta inicial; a continuación, se le induce a evaluar críticamente su propia salida; 
finalmente, se le pide que refine la respuesta a partir de esa retroalimentación. Este ciclo 
se repite hasta que se alcanzan criterios de parada previamente establecidos, lo que 
permite obtener resultados progresivamente más precisos y mejor ajustados al contexto 
(Madaan et al., 2023; Sahoo et al., 2025). 
El prompting de dar un paso atrás (take a step back prompting) busca afrontar el 
reto persistente del razonamiento complejo de múltiples pasos mediante un mecanismo 
explícito de abstracción, que permite al modelo extraer conceptos de alto nivel y 
principios generales a partir de casos concretos antes de abordar la resolución del 
problema (Zheng et al., 2023). La técnica se articula en un procedimiento de dos etapas 
que combina abstracción y razonamiento dirigido. En primer lugar, el modelo “da un 
paso atrás” (step back) para identificar las ideas generales o los principios subyacentes 
al problema planteado. En una segunda fase, estas abstracciones se utilizan como guía 

46 
para estructurar el razonamiento posterior y resolver la tarea original de manera más 
eficaz y fundamentada (Sahoo et al., 2025). 
El prompting de autorreflexión instruye al modelo para que revise críticamente 
una respuesta previa, evaluando su precisión o coherencia (Madaan et al., 2023; Shinn et 
al., 2023).  
Ejemplo 
Tras proporcionar una respuesta sobre una cuestión ética 
compleja, se puede preguntar al modelo:  
¿Estás seguro de esta respuesta? 
lo que induce una reevaluación y posible corrección. 
El meta-prompting implica pedir al modelo que analice el propio proceso de 
prompting o la efectividad de los prompts utilizados, con el objetivo de sugerir mejoras 
(Wang y Zhao, 2024). Sirve para reducir ambigüedades, mejorar la precisión, adaptar el 
tono y nivel, incluir restricciones adicionales útiles o crear plantillas reutilizables. Es 
posible proponer simplemente mejoras, o solicitar que defina formatos de salida, 
identifique lagunas o añada criterios de calidad específicos. 
Ejemplo 
Analiza la efectividad de los últimos cinco prompts y sugiere 
cómo podrían mejorarse para obtener resultados más precisos. 
El prompting de anticipación (anticipatory prompting) anima al modelo a anticipar 
preguntas o necesidades adicionales del usuario y a proporcionar información 
complementaria relevante junto con la respuesta principal.  
Ejemplo 
Ante la pregunta:  
¿Qué resolución debo usar para escanear documentos? 
el modelo puede indicar una resolución estándar y anticipar 
necesidades adicionales incluyendo consideraciones sobre el 
tipo de documento (texto, fotografía), el formato de salida, el uso 
de OCR y el impacto en el tamaño del archivo. 
Las técnicas de comprensión contextual y memoria se centran en permitir que los LLM 
recuerden y hagan referencia a interacciones pasadas con el fin de ofrecer experiencias 
conversacionales fluidas y garantizar la coherencia y la relevancia en diálogos 
prolongados. Estas técnicas aprovechan el contexto proporcionado dentro de un prompt o 
a lo largo de una interacción para mantener la continuidad temática y semántica de las 
respuestas del modelo. Al incorporar información previa o instrucciones acumulativas, 
estas técnicas permiten que los LLM produzcan respuestas más alineadas con las 

47 
expectativas del usuario y con el flujo general de la conversación. Este enfoque resulta 
especialmente valioso en aplicaciones conversacionales, donde la pérdida de contexto 
puede dar lugar a respuestas inconexas o redundantes (Fagbohun et al., 2024). 
Entre las técnicas que podemos distinguir en esta categoría encontramos: in-context 
prompting, conversational prompting, socratic prompting, multi-personas prompting y 
active prompting. 
El prompting en contexto (in-context prompting) aprovecha la capacidad del 
modelo para utilizar información proporcionada anteriormente dentro de la ventana de 
contexto. Al incluir interacciones previas o datos relevantes en el prompt, el modelo 
puede “recordar” y reutilizar esta información para generar respuestas coherentes y 
contextualmente apropiadas (Dong et al., 2024; Fagbohun et al., 2024; Rubin et al., 2021; 
Ye et al., 2022). 
Ejemplo 
Un usuario explica inicialmente que está evaluando el impacto 
del uso de un framework CSS en el web de una biblioteca 
universitaria. Más adelante, al preguntar:  
¿Qué consecuencias puede tener esto a largo plazo? 
el modelo tiene en cuenta el contexto previo y discute 
implicaciones en accesibilidad, mantenimiento, rendimiento y 
dependencia tecnológica, sin que el usuario tenga que reiterar el 
ámbito ni los objetivos del análisis. 
El prompting conversacional (conversational prompting) estructura la interacción 
como un diálogo continuo, en el que cada respuesta del modelo puede dar lugar a nuevas 
preguntas o aclaraciones por parte del usuario. Esta técnica fomenta una interacción 
iterativa que permite refinar progresivamente las respuestas y profundizar en un tema 
determinado (Fagbohun et al., 2024; Liu et al., 2023a).  
Ejemplo 
El usuario pregunta inicialmente qué significa que una biblioteca 
digital sea accesible. Tras la respuesta, plantea cómo comprobar 
si su web cumple con las WCAG. A partir de ahí, pregunta qué 
errores son más frecuentes y cómo priorizar las correcciones. La 
interacción conversacional permite profundizar paso a paso en 
un tema técnico complejo. 
El prompting socrático (socratic prompting) se inspira en el método socrático y 
utiliza una secuencia de preguntas para guiar el razonamiento del modelo y profundizar 
en un concepto. En lugar de proporcionar respuestas directas, el modelo formula o 
responde a preguntas que conducen gradualmente hacia una comprensión más 
profunda del tema (Chang, 2023; Fagbohun et al., 2024).  

48 
Ejemplo 
Para reflexionar sobre la automatización en bibliotecas, se puede 
plantear:  
¿Qué tareas bibliotecarias son susceptibles de automatización? 
seguido de preguntas como:  
¿Qué se gana y qué se pierde al delegar decisiones en sistemas 
automáticos? O ¿Dónde debería situarse la responsabilidad 
profesional?, favoreciendo un análisis crítico del impacto 
tecnológico. 
El prompting de múltiples personas (multi-personas prompting) implica instruir al 
modelo para que adopte múltiples perspectivas, roles o Personas al generar respuestas. 
Esta técnica permite explorar diferentes puntos de vista o estilos comunicativos dentro 
de una misma interacción (Gu et al., 2023; Fagbohun et al., 2024).   
Ejemplo 
Se puede pedir al modelo que redacte una explicación sobre las 
normas de préstamo “como las comunicaría un bibliotecario en el 
mostrador de atención al público” y luego “como la presentaría 
un responsable de la biblioteca en un documento institucional”. 
El modelo adapta el tono, la extensión y el grado de formalidad en 
cada caso. 
Las técnicas de prompting activo (active prompting) nacen como una solución al 
reto de adaptar los LLM a una amplia variedad de tareas de razonamiento. Este enfoque 
tiene como objetivo mejorar el rendimiento de los modelos en tareas complejas de 
respuesta a preguntas mediante el uso de prompts con ejemplos específicos por tarea 
que incorporan razonamiento de tipo chain-of-thought (Diao et al., 2024). 
Las técnicas bajo esta categoría están diseñadas para mejorar la precisión de los LLM y 
fomentar respuestas orientadas a metas concretas. Estas técnicas distinguen entre 
distintos tipos de información y alinean las salidas del modelo con objetivos claramente 
definidos (Fagbohun et al., 2024). Al establecer restricciones explícitas sobre el formato, 
la extensión o el propósito de la respuesta, estas técnicas reducen la ambigüedad y 
aumentan la relevancia de los resultados generados. 
Entre las técnicas que podemos distinguir en esta categoría encontramos: rephrase 
and respond (RaR), show-me vs tell-me, target-your-response (TAR), prompt macros, end-
goal planning y constrained vocabulary prompting. 
La técnica de reformular y responder (rephrase and respond o RaR) busca que los 
LLM reformulen y amplíen la pregunta original dentro de un mismo prompt antes de 
generar la respuesta, lo que contribuye a una mejor comprensión de la tarea y a una 
mayor precisión en las salidas (Deng et al., 2023). 

49 
El prompting de “muéstrame” frente a “dímelo” (show-me vs tell-me) distingue 
entre solicitar al modelo que “muestre” un concepto, por ejemplo, mediante diagramas o 
demostraciones, o que lo “explique” mediante una descripción textual (Perez et al., 
2021). 
Ejemplo 
Se puede pedir al modelo que muestre las fases de un plan de 
preservación digital mediante una lista estructurada o diagrama 
(“muéstrame”) o que explique de forma narrativa los objetivos y 
decisiones clave de cada fase (“explícame”), adaptando la 
representación al perfil del destinatario. 
El prompting orientado a la respuesta (target-your-response o TAR) consiste en 
definir explícitamente el objetivo y el formato de la respuesta esperada. Esta técnica 
ayuda a enfocar la salida del modelo en información relevante y concisa (Zhao et al., 
2021). 
Ejemplo 
Se puede pedir al modelo:  
Proporciona una definición de cuatro líneas sobre qué es el 
control de autoridades en bibliotecas, dirigida a estudiantes de 
primer curso universitario. 
Las macros13 de prompts (prompt macros) integran múltiples consultas o 
instrucciones dentro de una única instrucción orientadas a un objetivo final amplio, pero 
bien delimitado. Este enfoque permite abordar tareas complejas de manera estructurada 
sin necesidad de múltiples interacciones separadas. 
Ejemplo 
“Elabora una guía introductoria en español para estudiantes de 
grado sobre citación académica. Debe incluir: (1) qué es citar y 
por qué, (2) citación vs bibliografía, (3) citas directas e indirectas 
con ejemplos, (4) errores frecuentes, (5) ejemplos. Usa el estilo 
[APA 7 / MLA / Chicago] y limita la guía a [X] palabras.”.  
La instrucción anterior condensa implícitamente múltiples microconsultas: qué es 
una cita, por qué se cita, tipos de citas, ejemplos de citas… El modelo decide de forma 
autónoma que subtareas abordar, en qué orden, con qué nivel de detalle… Es reutilizable 
porque solo se precisa cambiar variables: estilo, audiencia, extensión, idioma, etc. 
 
13 En informática, una macro es una instrucción o conjunto de instrucciones predefinidas que se reutilizan 
para automatizar tareas repetitivas. La idea central es encapsular una secuencia de acciones, 
parametrizarla si es necesario y reutilizarla de forma consistente. Aplicado al ámbito del prompting, surge 
para describir plantillas de prompts estructuradas y reutilizables que encapsulan: un rol o persona, una 
estructura de razonamiento, restricciones de formato, y variables que pueden cambiar. 

50 
El prompting orientado a una meta final (end-goal planning) también utiliza 
prompts amplios, pero se diferencia en que el objetivo final está explícitamente definido 
como un resultado concreto que debe alcanzarse. El modelo no solo debe responder, 
sino planificar y orientar sus respuestas hacia la consecución de ese objetivo final, 
manteniendo la coherencia entre las distintas partes de la salida. 
Ejemplo 
Cuando se solicita: 
Redacta un documento de instrucciones que permita a un 
estudiante universitario elaborar correctamente la sección de 
referencias bibliográficas de un trabajo académico, de modo que 
pueda aplicar el procedimiento paso a paso sin necesitar 
aclaraciones adicionales.  
El objetivo final está explícitamente formulado: permitir que el estudiante actúe de 
forma autónoma. Las subtareas están subordinadas al cumplimiento del objetivo final. 
El prompting con vocabulario restringido (constrained vocabulary prompting) 
implica restringir la respuesta del modelo a un conjunto específico de palabras o a un 
vocabulario definido. Esta técnica impone limitaciones explícitas a la salida deseada del 
modelo, garantizando que el contenido generado se ajuste a un léxico predefinido. 
Al restringir el vocabulario, se obtiene un mayor control sobre el proceso de 
generación del lenguaje, lo que resulta especialmente útil en escenarios donde la 
precisión, la adherencia a una terminología específica o la evitación de lenguaje sensible 
o inapropiado son de suma importancia.  
Ejemplo 
Al desarrollar un asistente virtual para una biblioteca 
universitaria, se puede instruir al modelo: responde a las 
consultas de los usuarios utilizando únicamente terminología 
bibliotecaria básica y evita anglicismos o jerga técnica. 
Este enfoque asegura respuestas comprensibles para público general sin perder 
corrección terminológica. 
Ejemplo 
Para contenidos dirigidos a personas con dificultades de 
comprensión lectora, se puede pedir, entre otras: redacta el texto 
usando frases cortas y un vocabulario común, evitando 
tecnicismos y abreviaturas. 
En este caso el control léxico contribuye a mejorar la accesibilidad del contenido.  

51 
Esta dimensión agrupa técnicas de prompting orientadas a aprovechar las capacidades de 
los LLM para razonar mediante estructuras computacionales y producir código 
ejecutable, ya sea como medio para resolver una tarea o como resultado final esperado. A 
diferencia de las técnicas centradas exclusivamente en el razonamiento lingüístico, estos 
enfoques trasladan parcial o totalmente la carga inferencial al lenguaje formal del código, 
que ofrece mayor precisión, menor ambigüedad y una estructura lógica explícita. Entre las 
técnicas que podemos distinguir en esta categoría encontramos: code prompting y prompt 
to code. 
El prompting basado en código (code prompting) es una técnica que transforma las 
tareas formuladas en lenguaje natural en código estructurado, lo que permite interactuar 
directamente con LLM de texto y código sin necesidad de ejecutar el código de manera 
externa (Puerto et al., 2024). 
La conversión de prompts en código (prompt to code) consiste en solicitar 
explícitamente la generación de código que cumpla con determinados requisitos 
funcionales (Chen et al., 2023). 
Ejemplo  
Pedir al modelo que genere una función que convierta fechas 
bibliográficas en distintos formatos (por ejemplo, DD/MM/AAAA, 
AAAA-MM-DD, texto libre) a un formato normalizado ISO 8601,14 
especificando claramente los formatos de entrada aceptados y el 
formato de salida esperado. 
El prompting emocional (emotion prompting) añade un estímulo o encuadre 
emocional a una instrucción (por ejemplo, urgencia, importancia, responsabilidad, 
empatía) para modular el comportamiento del modelo: suele buscar respuestas más 
cuidadas, completas, “atentas” a matices, o con mayor esfuerzo aparente en tareas de 
razonamiento o redacción. No se trata de hacer que el modelo “sienta”, pues esto es 
imposible, sino en cambiar el contexto lingüístico y, con ello, el estilo y, en ocasiones, el 
desempeño (Kuka, 2024). El esquema básico es [Prompt] [estímulo emocional]. 
Ejemplo  
— Quiero una respuesta especialmente rigurosa; si hay 
supuestos, decláralos explícitamente. 
— Es un tema sensible; responde con empatía y sin juicios. 
 
14 Norma internacional para la representación no ambigua de fechas y horas en formatos legibles por 
personas y máquinas. https://en.wikipedia.org/wiki/ISO_8601 

52 
Las técnicas multimodales y transdisciplinarias integran múltiples modos de entrada y 
diversos dominios de conocimiento con el fin de ampliar la versatilidad de los LLM y 
extender sus aplicaciones a escenarios contextualmente complejos. Estas técnicas 
reflejan la creciente capacidad de los modelos para procesar y combinar información 
procedente de diferentes fuentes y disciplinas (Fagbohun et al., 2024). 
Entre las técnicas que podemos distinguir en esta categoría encontramos: 
multimodal prompting, visual prompting, cross-disciplinary prompting, historical context 
prompting y modular prompting. 
El prompting multimodal combina diferentes modalidades de entrada, como texto e 
imágenes, para guiar la generación de respuestas del modelo. Este enfoque permite 
enriquecer el contexto y mejorar la expresividad de las salidas generadas (Bang et al., 
2023; Lee et al., 2023).  
Ejemplo 
Un usuario proporciona una captura de pantalla del web de una 
biblioteca y pide al modelo que identifique posibles problemas de 
accesibilidad visibles (contraste de color, jerarquía visual, 
tamaño de texto) y sugiera mejoras preliminares basadas en la 
observación visual. 
El prompting interdisciplinar implica la combinación de conocimientos y enfoques 
procedentes de múltiples disciplinas para abordar una consulta o tarea determinada. Esta 
técnica permite generar explicaciones o soluciones que integran perspectivas diversas.  
Ejemplo 
Describe la preservación digital utilizando analogías de la 
ecología, comparando los ecosistemas naturales con los 
ecosistemas digitales. 
Esto ayuda a entender conceptos como sostenibilidad, 
obsolescencia tecnológica y equilibrio entre acceso y 
conservación.  
Explica qué son los metadatos recurriendo a conceptos de la 
lingüística, como la gramática o la sintaxis 
Esto permite presentar los metadatos como un sistema de reglas 
que da sentido y estructura a los documentos, facilitando su 
interpretación y recuperación. 
Las técnicas de prompting con contexto histórico, visual y modular se centran en la 
incorporación de contexto histórico, elementos visuales y construcciones modulares 
dentro de los prompts (Liu et al., 2023b). Un prompt con contexto histórico puede solicitar 
al modelo que responda conforme a un entorno o referencia histórica específica, mientras 
que el prompting visual puede implicar el uso de imágenes para guiar las respuestas del 

53 
modelo, y el modular aprovecha estructuras basadas en componentes para abordar 
consultas complejas.  
Ejemplo 
Describe el concepto de acceso abierto como lo entendería un 
editor académico de la década de 1970. 
El modelo ajusta su explicación teniendo en cuenta el sistema 
editorial predominante en ese periodo y las limitaciones 
tecnológicas del momento. 
Las técnicas creativas y generativas permiten a los LLM producir contenido creativo y 
suscitar respuestas diversas, innovadoras y provocadoras de reflexión. Mediante el 
empleo de una variedad de estrategias de prompting, que van desde el fomento de la 
ambigüedad hasta la imposición de restricciones léxicas, estas técnicas amplían las 
capacidades de los LLM en tareas creativas y abren nuevas vías para su aplicación en 
dominios como la narración, la generación de contenidos educativos y la escritura 
creativa. (Fagbohun et al., 2024). 
Entre las técnicas que podemos distinguir en esta categoría encontramos: ambiguous 
prompting, directional stimulus prompting, flipped interaction prompting y grammar 
correction (no puramente mecánica). 
El prompting ambiguo (ambiguous prompting) emplea deliberadamente 
instrucciones vagas o abiertas para fomentar una gama más amplia de respuestas 
posibles. Al reducir el nivel de especificidad, esta técnica estimula la creatividad y la 
exploración de ideas por parte del modelo.  
Ejemplo 
Describe una biblioteca del futuro. 
Esto da lugar a respuestas muy distintas según el énfasis que el 
modelo otorgue a la tecnología, los espacios, los servicios o la 
relación con los usuarios. 
Pedir: Reflexiona sobre la importancia de saber buscar 
información. 
Permite interpretaciones que pueden ir desde lo práctico 
(estrategias de búsqueda) hasta lo crítico (desinformación, 
pensamiento crítico). 
El prompting con estímulos direccionales utiliza pistas o estímulos direccionales 
para orientar al modelo hacia un resultado deseado sin imponer una solución 
completamente definida. Este enfoque mantiene un equilibrio entre orientación y 
flexibilidad, permitiendo que el modelo conserve cierto grado de creatividad (Shum et al., 
2023). 

54 
Ejemplo 
Al pedir un ejemplo práctico sobre evaluación de fuentes, el 
usuario puede señalar:  
Plantea el caso desde la perspectiva de un estudiante que 
prepara su TFG. 
Este estímulo direccional condiciona el escenario narrativo y el 
nivel de profundidad. 
El prompting de interacción invertida invierte la dinámica convencional entre el 
modelo y el usuario. En lugar de que el usuario dirija la conversación, el modelo plantea 
preguntas o solicita aclaraciones al usuario. Al invertir los roles esperados de la 
interacción, el modelo guía al usuario en la creación de sus propios resultados mediante 
consultas dirigidas. 
Ejemplo 
El usuario solicita: Guíame mediante preguntas para definir 
indicadores de uso de una biblioteca digital. 
El modelo comienza con:  
¿Qué objetivos estratégicos quiere medir la biblioteca? y continúa 
con preguntas sobre métricas, fuentes de datos y periodicidad. 
Los prompts de corrección gramatical son instrucciones específicas dadas al 
modelo para identificar y corregir errores gramaticales o inconsistencias en el texto 
proporcionado por el usuario. Dado que los LLM han sido entrenados con grandes corpus 
de datos textuales, estos prompts pueden aprovechar las capacidades lingüísticas 
avanzadas del modelo para actuar como corrector gramatical conversacional, ofreciendo 
sugerencias y mejoras conforme a los requisitos de salida solicitados. Al pedir al LLM que 
mejore la redacción y el estilo de escritura, los usuarios pueden aumentar la calidad y 
claridad de su comunicación escrita y adaptar fácilmente sus textos a distintos usos y 
contextos. 
Ejemplo 
Un usuario ha preparado un procedimiento interno y solicita: 
Corrige la gramática y mejora la redacción de este documento 
para que sea claro y coherente, pero sin cambiar la estructura ni 
el sentido original. 
El modelo actúa como revisor lingüístico, no como redactor del 
texto.  
Un usuario redacta una nota dirigida a usuarios de la biblioteca y 
pide: Revisa el texto para asegurar un lenguaje correcto, 
accesible y profesional, evitando tecnicismos innecesarios. 
El modelo ajusta el tono y la gramática al público objetivo 
definido.  
Un usuario ha redactado una guía rápida de uso del catálogo y 
pide: Corrige la ortografía, la gramática y revisa la claridad del 

55 
texto para que sea comprensible para público general, pero con un 
tono institucional. 
El modelo ajusta el lenguaje respetando el equilibrio entre claridad 
y formalidad. 
A continuación, se recogen algunas recomendaciones finales que redundan en aspectos 
comentados a lo largo del documento: 
− Estandariza plantillas de prompts para tareas recurrentes e incorpora siempre 
objetivo, contexto mínimo, restricciones y formato de salida.  
− Define el rol y las expectativas respecto a las características de las respuestas que 
esperas. 
− Trabaja de forma incremental. Empieza con prompts simples, introduce cambios 
uno a uno y comparar resultados para entender qué mejora realmente el 
rendimiento. 
− Prioriza la verificabilidad. Pide justificación, solicita fuentes y recursos 
adicionales para verificar la corrección de las respuestas, delimita el uso de 
fuentes y aplica estrategias de verificación / autorreflexión cuando la precisión 
sea crítica. 
− Cuida la higiene de datos. No incluyas información sensible, anonimizar o 
seudonimizar y comparte únicamente el fragmento necesario (especialmente en 
textos e imágenes).  
− Alinea técnica y finalidad. Elege técnicas de prompting según el tipo de problema 
(razonamiento, control de la salida, fiabilidad, diálogo, etc.) y no por “moda” o por 
preferencias estilísticas. 
Este informe ha sistematizado un conjunto amplio de recomendaciones, métodos y 
técnicas de prompting orientadas a mejorar el uso de los modelos de lenguaje en 
contextos académicos y profesionales. Como se ha mencionado en diversos apartados a 
lo largo del documento, la calidad de las respuestas no depende de una única técnica 
aislada, sino del acierto en la combinación de distintos elementos de diseño, tales como 
la claridad del prompt, la integración de una contextualización suficiente, la delimitación 
de restricciones, la especificación del formato de salida, la descomposición de tareas 
cuando estas son complejas o la aplicación de mecanismos de verificación cuando la 
fiabilidad resulta crítica. En este sentido, las buenas prácticas generales y las técnicas 
específicas descritas a lo largo del documento no deben entenderse como enfoques 
excluyentes, sino como estrategias plenamente compatibles entre sí, que pueden y 
deben combinarse en función del objetivo perseguido. Desde esta perspectiva, un 
prompt efectivo no es necesariamente el más largo, el más complejo o el que incorpora 
más técnicas, sino aquel que selecciona y articula de forma coherente los componentes 

56 
realmente necesarios para cada tarea. Así, en muchas situaciones bastará con un prompt 
breve, pero claro, bien contextualizado y con un formato de salida definido, mientras 
que, en otras, será conveniente añadir ejemplos, instrucciones paso a paso, estrategias 
de autorreflexión, mecanismos de contraste o indicaciones explícitas para verificar 
fuentes y supuestos. 
Mejorar la calidad de los prompts eficaz exige una lógica de experimentación ante la 
imposibilidad de conocer por completo el funcionamiento interno de unos sistemas que, 
pese a contar ya con abundante documentación y buenas prácticas, siguen siendo en 
gran medida opacos por su propia arquitectura de caja negra. Diseñar buenos prompts 
implica probar, comparar, ajustar e iterar. En la práctica, esto supone comenzar con 
formulaciones simples, introducir cambios de manera incremental, observar el efecto de 
cada modificación y conservar aquellas decisiones que mejoran realmente el 
rendimiento para una tarea concreta. No existe un prompt universalmente óptimo, sino 
que su eficacia depende del tipo de problema, del dominio, del modelo empleado y del 
grado de precisión o creatividad que se requiera. 
Del mismo modo, conviene insistir en que un prompt de calidad no se limita a 
obtener respuestas plausibles, fluidas o bien redactadas, sino respuestas que puedan 
ser examinadas críticamente. De ahí la importancia de priorizar la verificabilidad a 
través de la solicitud de justificaciones, fuentes, delimitando marcos de referencia, o 
solicitando que se indiquen limitaciones en aquellas situaciones en las que el modelo no 
pueda calcular, inferir o afirmar algo con suficiente base.  

57 
Adamska, Marta, Smirnova, Daria, Nasiri, Hamid, Yu, Zhengxin, Garraghan, Peter (2025). 
Green prompting. https://doi.org/10.48550/arXiv.2503.10666 
Bahng, Hyojin, Jahanian, Ali, Sankaranarayanan, Swami, Isola, Phillip (2022). Exploring 
visual prompts for adapting large-scale models. 
https://doi.org/10.48550/arXiv.2203.17274  
Bang, Yejin, Cahyawijaya, Samuel, Lee, Nayeon, et al. (2023). A multitask, multilingual, 
multimodal evaluation of ChatGPT on reasoning, hallucination, and interactivity. In 
Proceedings of the 13th International Joint Conference on Natural Language 
Processing and the 3rd Conference of the Asia-Pacific Chapter of the Association for 
Computational Linguistics (pp. 675–718). https://doi.org/10.18653/v1/2023.ijcnlp-
main.45 
Besta, Maciej, Blach, Nils, Kubicek, Ales, et al. (2023). Graph of thoughts: Solving 
elaborate problems with large language models. 
https://doi.org/10.1609/aaai.v38i16.29720 
Brown, Tom B., Mann, Benajmin, Ryder, Nick, et al. (2020). Language models are few-
shot learners. In NIPS'20: Proceedings of the 34th International Conference on 
Neural Information Processing Systems (pp. 1877–1900).  
https://doi.org/10.48550/arXiv.2005.14165  
Chang, Edward (2023). Prompting large language models with the socratic method. In 
2023 IEEE 13th Annual Computing and Communication Workshop and Conference 
(CCWC) (pp. 351–360). https://doi.org/10.48550/arXiv.2303.08769 
Chen, Eason, Wang, Danyang, Xu, Luyi, Cao, Chen, Fang, Xiao, & Lin, Jionghao (2024). A 
systematic review on prompt engineering in large language models for K-12 STEM 
education. https://doi.org/10.48550/arXiv.2410.11123  
Chia, Yew Ken, Chen, Guizhen, Tuan, Luu Anh, Poria, Soujanya, & Bing, Lidong (2023). 
Contrastive chain-of-thought prompting. https://doi.org/10.48550/arXiv.2311.09277 
Chowdhery, Aakanksha, Narang, Sharan, Devlin, Jacob, et al. (2023). PaLM: Scaling 
language modeling with pathways. Journal of Machine Learning Research, 24(240), 
1–113. https://doi.org/10.48550/arXiv.2204.02311  
Claude (2026). Use XML tags to structure your prompts. In Claude API docs. 
https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/use-
xml-tags 
Comisión Europea (2019). Directrices éticas para una IA fiable. https://digital-
strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai 
Deng, Yihe, Zhang, Weitong, Chen, Zixiang, & Gu, Quanquan (2023). Rephrase and 
respond: Let large language models ask better questions for themselves. 
https://doi.org/10.48550/arXiv.2311.04205 
Desmond, Michael, & Brachman, Michelle (2024). Exploring prompt engineering 
practices in the enterprise. https://doi.org/10.48550/arXiv.2403.08950  

58 
Devlin, Jacob, Chang, Ming-Wei, Lee, Kenton, Toutanova, Kristina (2018). BERT: Pre-
training of deep bidirectional transformers for language understanding. 
https://doi.org/10.48550/arXiv.1810.04805  
Diao, Shizhe, Wang, Pengcheng, Lin, Yong, & Zhang, Tong (2023). Active prompting with 
chain-of-thought for large language models. In Proceedings of the 62nd Annual 
Meeting of the Association for Computational Linguistics (pp. 1330–1350). 
https://doi.org/10.18653/v1/2024.acl-long.73 
DiCuffa, Sophia, Zambrana, Amanda, Yadav, Priyanshi, Madiraju, Sashidhar, Suman, 
Khushi, & Alomar, Eman (2025). Exploring prompt patterns in AI-assisted code 
generation: Towards faster and more effective developer-AI collaboration. In 2025 
IEEE 4th International Conference on Computing and Machine Intelligence (ICMI) 
(pp. 1–7). https://doi.org/10.1109/ICMI65310.2025.11141320  
Dong, Qingxiu, Li, Lei, Dai, Damai, et al. (2024). A survey for in-context learning. In 
Proceedings of the 2024 Conference on Empirical Methods in Natural Language 
Processing (pp. 1107–1128). https://doi.org/10.18653/v1/2024.emnlp-main.64 
Dhuliawala, Shehzaad, Komeili, Mojtaba, Xu, Jing, Raileanu, Roberta, Li, Xian, 
Celikyilmaz, Asli, & Weston, Jason (2024). Chain-of-verification reduces 
hallucination in large language models. In Findings of the Association for 
Computational Linguistics: ACL 2024 (pp. 3563–3578). 
https://doi.org/10.18653/v1/2024.findings-acl.212 
Fagbohun, Oluwole, Harrison, Rachel M., & Dereventsov, Anton (2023). An empirical 
categorization of prompting techniques for large language models: A practitioner's 
guide. Journal of Artificial Intelligence, Machine Learning and Data Science, 1(4), 1–
11. https://doi.org/10.51219/JAIMLD/Oluwole-Fagbohun/15 
Fungwacharakorn, Wachara, Thanh, Nguyen Ha, Myo Zin, May, & Satoh, Ken (2024). 
Layer-of-thoughts prompting (LoT): Leveraging LLM-based retrieval with constraint 
hierarchies. https://doi.org/10.48550/arXiv.2410.12153 
Garcia, Enio Santan Junior, Benjamin, Gabriel, Araujo, Melissa, et al. (2025). Which 
prompting technique should I use? An empirical investigation of prompting 
techniques for software engineering tasks. 
https://doi.org/10.48550/arXiv.2506.05614  
Gemini (2025). Prompt design strategies. In Gemini API. https://ai.google.dev/gemini-
api/docs/prompting-strategies 
Greyling, Cobus (2023). Chain-of-note (CoN) retrieval for LLMs. Medium. 
https://cobusgreyling.medium.com/chain-of-note-con-retrieval-for-llms-
763ead1ae5c5 
Gu, Heng, Degachi, Chadha, Genç, Uğur, Chandrasegaran, Senthil, & Verma, Himanshu 
(2023). On the effectiveness of creating conversational agent personalities through 
prompting. https://doi.org/10.48550/arXiv.2310.11182 
Gutheil, Niklas, Mayer, Valentin, Müller, Leopold, Römmelt, Jörg, & Kühl, Niklas (2025). 
PromptPilot: Improving human-AI collaboration through LLM-enhanced prompt 
engineering. https://doi.org/10.48550/arXiv.2510.00555  

59 
Harrison, Rachel M., Dereventsov, Anton, & Bibin, Anton (2023). Zero-shot 
recommendations with pre-trained large language models for multimodal nudging. 
https://doi.org/10.48550/arXiv.2309.01026 
Hewing, Michael, & Leinhos, Vincent (2024). The prompt canvas: A literature-based 
practitioner guide for creating effective prompts in large language models 
https://doi.org/10.48550/arXiv.2412.05127  
Hu, Hanxu, Lu, Hongyuan, Zhang, Huajian, Song, Yun-Ze, Lam, Wai, & Zhang, Yue 
(2023). Chain-of-symbol prompting elicits planning in large language models. 
https://doi.org/10.48550/arXiv.2305.10276 
Jiang, Albert Q., Sablayrolles, Alexandre, Mensch, Arthur, et al. (2023). Mistral 7B. 
https://doi.org/10.48550/arXiv.2310.06825   
Kasneci, Enkelejda, Seßler, Kathrin, Küchemann, Stefan, et al. (2023). Chatgpt for good? 
on opportunities and challenges of large language models for education. Learning 
and Individual differences, 103(102274). 
https://doi.org/10.1016/j.lindif.2023.102274   
Kojima, Takeshi, Gu, Shixiang Shane, Reid, Machel, & Matsuo, Yutaka, & Iwasawa, 
Yusuke (2023). Large language models are zero-shot reasoners. 
https://doi.org/10.48550/arXiv.2205.11916 
Kuka, Valeriia (2024). Emotion prompting. In Learn prompting. 
https://learnprompting.org/docs/basics/prompt_structure 
Kuka, Valeriia (2025). Basic prompt structure and key parts. In Learn prompting. 
https://learnprompting.org/docs/basics/prompt_structure 
Lee, Yi-Lun, Tsai, Yi-Hsuan, Chiu, Wei-Chen, & Lee, Chen-Yu (2023). Multimodal 
prompting with missing modalities for visual recognition. In Proceedings of the 
IEEE/CVF Conference on Computer Vision and Pattern Recognition (pp. 14943–
14952). 
https://openaccess.thecvf.com/content/CVPR2023/papers/Lee_Multimodal_Prompti
ng_With_Missing_Modalities_for_Visual_Recognition_CVPR_2023_paper.pdf 
Leviathan, Yaniv, Kalman, Matan, & Matias, Yossi (2025). Prompt Repetition Improves Non-
Reasoning LLM. https://doi.org/10.48550/arXiv.2512.14982 
Lewis, Patrick, Perez, Ethan, Piktus, Aleksandra, et al. (2020). Retrieval-augmented 
generation for knowledge-intensive NLP tasks. In NIPS'20: Proceedings of the 34th 
International Conference on Neural Information Processing Systems (pp. 9459–
9474). https://dl.acm.org/doi/abs/10.5555/3495724.3496517 
Li, Xingxuan, Zhao, Ruochen, Chia, Yew Ken, Ding, Bosheng, Joty, Shafiq, Poria, 
Soujanya, & Bing, Lidong (2023a). Chain-of-knowledge: Grounding large language 
models via dynamic knowledge adapting over heterogeneous sources. 
https://doi.org/10.48550/arXiv.2305.13269 
Li, Cheng, Wang, Jindong, Zhang, Yixuan, et al. (2023b). Large language models 
understand and can be enhanced by emotional stimuli. 
https://doi.org/10.48550/arXiv.2307.11760 
Liu, Shixuan, Peng, Chen, Wang, Chao, Chen, Xiangyan, Song, Shuangyong (2023a). 
icsBERTs: Optimizing pre-trained language models in intelligent customer service. 

60 
Procedia Computer Science, 222, 127–136. 
https://doi.org/10.1016/j.procs.2023.08.150  
Liu, Pengfei, Yuan, Weizhe, Fu, Jinlan, Jiang, Zhengbao, Hayashi, Hiroaki, & Neubig, 
Graham (2023b). Pre-train, prompt, and predict: A systematic survey of prompting 
methods in natural language processing. ACM Computing Surveys, 55(9), 1–35. 
https://doi.org/10.1145/3560815 
Liu, Xinyue, Mireshghallah, Niloofar, Ginsburg, Jane C., Chakrabarty, Tuhin (2026). 
Alignment whack-a-mole: Finetuning activates verbatim recall of copyrighted books 
in large language models. https://doi.org/10.48550/arXiv.2603.20957 
Long, Jieyi (2023). Large language model guided tree-of-thought. 
https://doi.org/10.48550/arXiv.2305.08291 
Lyu, Qing, Havaldar, Shreya, Stein, Adam, Zhang, Li, Rao, Delip, Wong, Eric, Apidianaki, 
Marianna, & Callison-Burch, Chris (2023). Faithful chain-of-thought reasoning. 
https://doi.org/10.48550/arXiv.2301.13379 
Ma, Pingchuan, Li, Zongjie, Sun, Ao, & Wang, Shuai (2023). “Oops, Did I just say that? 
Testing and repairing unethical suggestions of large language models with suggest-
critique-reflect process. https://doi.org/10.48550/arXiv.2305.02626 
Madaan, Aman, Tandon, Niket, & Gupta, Prakhar, et al. (2023). Self-refine: Iterative 
refinement with self-feedback. https://doi.org/10.48550/arXiv.2303.17651 
MacCallum, & Noah, Julian (2025). GPT-4.1 Prompting guide. In Cookbook: Recipes, 
guides, and notebooks to help you build with OpenAI models. 
https://developers.openai.com/cookbook/examples/gpt4-1_prompting_guide 
Ning, Xuefei, Lin, Zinan, Zhou, Zixan, Yang, Zifu, & Wang, Yu (2023). Skeleton-of-thought: 
Large language models can do parallel decoding. 
https://doi.org/10.48550/arXiv.2307.15337 
NIST, National Institute of Standards and Technology (2023). Artificial intelligence risk 
management framework (AI RMF 1.0). https://doi.org/10.6028/NIST.AI.100-1 
O’Neil, Cathy (2017). Armas de destrucción matemática: Cómo el big data aumenta la 
desigualdad y amenaza la democracia. Capitan Swing. 
Open AI (2025). Best practices for prompt engineering with the OpenAI API. 
https://help.openai.com/en/articles/6654000-best-practices-for-prompt-
engineering-with-the-openai-api 
Ouyang, Long, Wu, Jeff, Jiang, Xu, et al. (2022). Training language models to follow 
instructions with human feedback. In Advances in Neural Information Processing 
Systems 35 (NeurIPS 2022). https://doi.org/10.48550/arXiv.2203.02155  
OWASP (2025). OWASP top 10 for LLM applications 2025. https://owasp.org/www-
project-top-10-for-large-language-model-applications/assets/PDF/OWASP-Top-10-
for-LLMs-v2025.pdf 
Paul, Debjit, Ismayilzada, Mete, Peyrard, Maxime, Borges, Breatriz, Bosselut, Antoine, 
West, Robert, & Faltings, Boi (2024). Refiner: Reasoning feedback on intermediate 
representations. In Proceedings of the 18th Conference of the European Chapter of 
the Association for Computational Linguistics (pp. 1100–1126). 

61 
https://dlab.epfl.ch/people/west/pub/Paul-Ismayilzada-Peyrard-Borges-Bosselut-
West-Faltings.pdf 
Perez, Ethan, Kiela, Douwe. & Cho, Kyunghyun (2021). True few-shot learning with 
language models. In NIPS'21: Proceedings of the 35th International Conference on 
Neural Information Processing Systems, 845 (pp. 11054–11070). 
https://dl.acm.org/doi/10.5555/3540261.3541106 
Petroni, Fabio, Rocktäschel Tim, Lewis Patrick, Bakhtin, Anton, Wu, Yuxiang, Miller, 
Alexander H., & Riedel, Sebastian (2019). Language models as knowledge bases?. In 
Proceedings of the 2019 Conference on Empirical Methods in Natural Language 
Processing and the 9th International Joint Conference on Natural Language 
Processing (pp. 2463–2473). https://doi.org/10.48550/arXiv.1909.01066  
Puerto, Haritz, Tutek, Martin, Aditya, Somak, Zhu, Xiaodan, & Gurevych, Iryna (2024). 
Code prompting elicits conditional reasoning abilities in text+code LLMs. In 
Proceedings of the 2024 Conference on Empirical Methods in Natural Language 
Processing (pp. 11234–11258). https://doi.org/10.18653/v1/2024.emnlp-main.629 
Radford, Alec, Wu, Jeffrey, Child, Rewon, Luan, David, Amodei, Dario, Sutskever, Ilya 
(2019). Language models are unsupervised multitask learners. 
https://cdn.openai.com/better-language-
models/language_models_are_unsupervised_multitask_learners.pdf  
Rahman, Arifur (2026). A systematic review of vision language models: Comprehensive 
analysis of architectures, applications, datasets and challenges towards robust 
multimodal intelligence. Array, 30, 100739, 1–41. 
https://doi.org/10.1016/j.array.2026.100739 
Resnik, David B., Hosseini, Mohammad (2025). Disclosing artificial intelligence use in 
scientific research and publication: When should disclosure be mandatory, 
optional, or unnecessary?. Accountability in Research, 33(2), 1–13. 
https://doi.org/10.1080/08989621.2025.2481949 
Rubin, Ohad, Herzig, Jonathan, & Berant, Jonathan (2021). Learning to retrieve prompts 
for in-context learning. https://doi.org/10.48550/arXiv.2112.08633 
Sahoo, P., A. K. Singh, S. Saha, V. Jain, S. Mondal, and A. Chadha (2024). A systematic 
survey of prompt engineering in large language models: Techniques and 
applications. https://doi.org/10.48550/arXiv.2402.07927 
Shaikh, Omar, Zhang, Hongxin, Held, William, Bernstein, Michael, & Yang, Diyi (2023). 
On second thought, let’s not think step by step! Bias and toxicity in zero-shot 
reasoning. In Proceedings of the 61st Annual Meeting of the Association for 
Computational Linguistics (pp. 4454–4470). https://doi.org/10.18653/v1/2023.acl-
long.244 
Schick, Timo, & Schütze, Hinrich (2020). It's not just size that matters: small language 
models are also few-shot learners. https://doi.org/10.48550/arXiv.2009.07118  
Shinn, Noah, Labash, Beck, & Gopinath, Ashwin (2023). Reflexion: An autonomous agent 
with dynamic memory and self-reflection. 
https://doi.org/10.48550/arXiv.2303.11366 

62 
Shum, Kashun, Diao, Shizhe, & Zhang, Tong (2023). Automatic prompt augmentation and 
selection with chain-of-thought from labeled data. In Findings of the Association for 
Computational Linguistics: EMNLP 2023 (pp. 12113–12139). 
https://doi.org/10.18653/v1/2023.findings-emnlp.811 
Thirunavukarasu, Arun James, Ting, Darren Shu Jeng, Elangovan, Kabilan, Gutierrez, 
Laura, Tan, Ting Fan, Ting, Daniel Shu Wei (2023). Large language models in 
medicine. Nature Medicine, 29(8), 1930–1940. https://doi.org/10.1038/s41591-023-
02448-8  
Thoppilan, Romal, De Freitas, Daniel, Hall, Jamie, et al. (2022). LaMDA: Language models 
for dialog applications. https://doi.org/10.48550/arXiv.2201.08239  
Tokayev, Kassym-Jomart (2023). Ethical implications of large language models: A 
multidimensional exploration of societal, economic, and technical concerns. 
International Journal of Social Analytics, 8(9), 17-33. 
https://norislab.com/index.php/ijsa/article/view/42 
Torres-Salinas, Daniel (2025). Primeros pasos con ChatGPT e ingeniería de prompts. 
https://doi.org/10.5281/zenodo.15260566 
Touvron, Hugo, Lavril, Thibaut, Izacard, Gautier, et al. LLaMA: Open and efficient 
foundation language models. https://doi.org/10.48550/arXiv.2302.13971  
Wang, Xuezhi, Wei, Jason, Schuurmans, Dale, et al. (2023). Self-consistency improves 
chain of thought reasoning in language models. 
https://doi.org/10.48550/arXiv.2203.11171 
Wang, Yuqing, & Zhao, Yun (2024). Metacognitive prompting improves understanding in 
large language models. In Proceedings of the 2024 Conference of the North 
American Chapter of the Association for Computational Linguistics: Human 
Language Technologies (pp. 1914–1926). https://aclanthology.org/2024.naacl-
long.106.pdf 
Wang, Ming, Liu, Yuanzhong, Liang, Xiaoyu, Huang, Yijie, et al. 2024. Minstrel: Structural 
prompt generation with multi-agents coordination for non-AI experts. 
https://doi.org/10.48550/arXiv.2409.13449  
Vaswani, Ashish, Shazeer, Noam, Parmar, Niki, et al. (2017). Attention is all you need. In 
NIPS'17: Proceedings of the 31st International Conference on Neural Information 
Processing Systems (pp. 6000–6010). https://doi.org/10.48550/arXiv.1706.03762  
Wei, Jason, Wang, Xuezhi, Schuurmans, Dale, Bosma, Maarten, Ichter, Brian, Xia, Fei, 
Chi, Ed, Le, Quoc, & Zhou, Denny (2022). Chain-of-thought prompting elicits 
reasoning in large language models. In NIPS'22: Proceedings of the 36th 
International Conference on Neural Information Processing Systems (pp. 24824–
2483). https://dl.acm.org/doi/10.5555/3600270.3602070 
Wei, Jing, Kim, Sungdong, Jung, Hyunhoon, & Kim, Young-Ho (2023). Leveraging large 
language models to power chatbots for collectiong user self-reported data. 
Proceedings of the ACM on Human-Computer Interaction, 8(87), 1–35. 
https://doi.org/10.1145/3637364 
White, Jules, Fu, Quchen, Hays, Sam, Sandborn, Michael, Olea, Carlos, Gilbert, Henry, 
Elnashar, Ashraf. Spencer-Smith, Jesse, & Schmidt, Douglas C. (2023). A prompt 

63 
pattern catalog to enhance prompt engineering with ChatGPT. 
https://doi.org/10.48550/arXiv.2302.11382  
Wu, Shijie, Irsoy, Ozan, Lu, Steven, et al. Bloomberg GPT: A large language model for 
finance. https://doi.org/10.48550/arXiv.2303.17564  
Xu, Frank F., Alon, Uri, Neubig, Graham, Hellendoorn Vincent, J. (2022). A systematic 
evaluation of large language models of code. In Proceedings of the 6th ACM 
SIGPLAN International Symposium on Machine Programming 2022 (pp. 1–10). 
https://doi.org/10.48550/arXiv.2202.13169  
Xu, Silei, Xie, Wenhao, Zhao, Lingxiao, & He, Pengcheng (2025). Chain of draft: Thinking 
faster by writing less. https://doi.org/10.48550/arXiv.2502.18600 
Yang, Jingfeng, Jin, Hongye, Tang, Ruixian, et al. (2024a). Harnessing the power of LLMs 
in practice: A survey on ChatGPT and beyond. ACM Transactions on Knowledge 
Discovery from Data, 18(6), 1–32. https://doi.org/10.1145/3649506  
Yang, Ling, Yu, Zhaochen, Zhang, Tianjun, Cao, Shiyi, Xu, Minkai, Zhang, Wentao, 
Gonzalez, Joseph E., & Cui, Bin (2024b) Buffer of thoughts: Thought-augmented 
reasoning with large language models. In NIPS '24: Proceedings of the 38th 
International Conference on Neural Information Processing Systems (pp. 113519–
113544). https://dl.acm.org/doi/10.5555/3737916.3741523 
Yao, Shunyu, Yu, Dian, Zhao, Jeffrey, Shafran, Izhak, Griffiths, Thomas L., Cao, Yuan, & 
Narasimhan, Karthik (2023). Tree of thoughts: Deliberate problem solving with large 
language models. https://doi.org/10.48550/arXiv.2305.10601 
Ye, Xi, Iyer, Srinivassan, Celikyilmaz, Asli, Stoyanov, Ves, Durrett, Greg, & Pasunuru, 
Ramakanth (2022). Complementary explanations for effective in-context learning. 
https://doi.org/10.48550/arXiv.2211.13892 
Yu, Wenhao, Zhang, Hongming, Pan, Xiaoman, Ma, Kaixin, Wang, Hongwei, & Yu, Dong 
(2023). Chain-of-note: Enhancing robustness in retrieval-augmented language 
models. In Proceedings of the 2024 Conference on Empirical Methods in Natural 
Language Processing (pp. 14672-14685). https://doi.org/10.18653/v1/2024.emnlp-
main.813 
Zamfirescu-Pereira, J.D., Wong, Richmond, Y, Hartmann, Bjoern, Yang, Qian (2023). Why 
Johnny can’t prompt: How non-AI experts try (and fail) to design LLM prompts. In 
CHI '23: Proceedings of the 2023 CHI Conference on Human Factors in Computing 
System (pp. 1–21). https://doi.org/10.1145/3544548.3581388  
Zheng, Huaixiu Steven, Mishra, Swaroop, Chen, Xinyun, Cheng, Heng-Tze, Chi, Ed H. Le, 
Quoc V., & Zhou, Denny (2023). Take a step back: Evoking reasoning via abstraction 
in large language models. https://doi.org/10.48550/arXiv.2310.06117 
Zhang, Zhuosheng, Zhang, Aston, Li, Mu, & Smola, Alex (2022). Automatic chain of 
thought prompting in large language models. 
https://doi.org/10.48550/arXiv.2210.03493 
Zhang, Xinliang Frederick, Beauchamp, Nick, & Wang, Lu (2024). Narrative-of-thought: 
Improving temporal reasoning of large language models via recounted narratives. In 
Findings of the Association for Computational Linguistics: EMNLP 2024 (pp. 16507–
16530). https://doi.org/10.18653/v1/2024.findings-emnlp.963 

64 
Zhao, Tony Z., Wallace, Eric, Feng, Shi, Klein, Dan & Singh, Sameer (2021). Calibrate 
before use: Improving few-shot performance of language models. 
https://doi.org/10.48550/arXiv.2102.09690 
Zhao, Wayne Xin, Zhou, Kun, Li, Junyi, et al. (2023a). A survey of large language models. 
https://doi.org/10.48550/arXiv.2303.18223 
Zhao, Xufeng, Li, Mengdi, Lu, Wenhao, Weber, Cornelius, Lee, Jae Hee, Chu, Kun & 
Wermter, Stefan (2023b). Enhancing zero-shot chain-of-thought reasoning in large 
language models through logic. https://doi.org/10.48550/arXiv.2309.13339 
Zhou, Yucheng, Geng, Xiubo, Shen, Tao, Tao, Chongyang, Long, Guodong, Lou, Jian-
Guang, & Shen, Jianbing (2023). Thread of thought unraveling chaotic contexts. 
https://doi.org/10.48550/arXiv.2311.08734 
Zheng, Chuanyang, Liu, Zhengying, Xie, Enze, Li, Zhenguo, & Li, Yu (2023). Progressive-
hint prompting improves reasoning in large language models. 
https://doi.org/10.48550/arXiv.2304.09797 
  

 
 

```
