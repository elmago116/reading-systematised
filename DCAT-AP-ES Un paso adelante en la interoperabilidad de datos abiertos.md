---
title: "DCAT-AP-ES: Un paso adelante en la interoperabilidad de datos abiertos"
source: https://datos.gob.es/es/blog/dcat-ap-es-un-paso-adelante-en-la-interoperabilidad-de-datos-abiertos
author:
  - "[[datos.gob.es]]"
published:
created: 2026-09-21
description: Contexto y necesidad de actualización Los datos son un recurso clave en la transformación digital de las Administraciones
tags:
  - op/doc/manual
  - tech/interoperability
---
Fecha publicación 01/09/2025

Fecha actualización 30/09/2025

## Contexto y necesidad de actualización

Los datos son un recurso clave en la transformación digital de las Administraciones Públicas. Asegurar su acceso, interoperabilidad y reutilización es fundamental para mejorar la transparencia, fomentar la innovación y facilitar el desarrollo de servicios públicos eficientes y centrados en la ciudadanía.

En este contexto, la [Norma Técnica de Interoperabilidad de Reutilización de Recursos de Información (NTI-RISP)](https://datos.gob.es/es/documentacion/norma-tecnica-de-interoperabilidad-de-reutilizacion-de-recursos-de-informacion) es el marco regulador en España para la gestión y apertura de datos públicos desde 2013. La norma establece condiciones comunes sobre selección, identificación, descripción, formato, condiciones de uso y puesta a disposición de los documentos y recursos de información elaborados o custodiados por el sector público, relativos a numerosos ámbitos de interés como la información social, económica, jurídica, turística, sobre empresas, educación, etc., cumpliendo plenamente con lo establecido en la [Ley 37/2007, de 16 de noviembre, sobre reutilización de la información del sector público](https://www.boe.es/eli/es/l/2007/11/16/37/con).

En los últimos meses se viene acometiendo una modernización del texto dentro del objetivo europeo y español de potenciar la economía del dato, impulsando su intercambio a gran escala dentro de entornos distribuidos y federados, garantizando las adecuadas condiciones de ciberseguridad y respetando los principios y valores europeos.

La nueva norma, en fase de tramitación, refiere un **nuevo modelo de metadatos alineado con las últimas versiones de los estándares europeos**, que facilitan la descripción de los conjuntos de datos y recursos de información reutilizables puestos a disposición pública.

Este nuevo modelo de metadatos, denominado **DCAT-AP-ES**, adopta las directrices del esquema europeo de intercambio de metadatos DCAT-AP (*Data Catalog Vocabulary – Aplication Profile*) con algunas restricciones y ajustes adicionales. DCAT-AP-ES está alineando con los **estándares europeos** [**DCAT-AP 2.1.1**](https://interoperable-europe.ec.europa.eu/collection/semic-support-centre/solution/dcat-application-profile-data-portals-europe/release/211) **y la extensión** [**DCAT-AP-HVD 2.2.0**](https://semiceu.github.io/DCAT-AP/releases/2.2.0-hvd/)**, que incorpora los requisitos para los Conjuntos de Alto Valor (HVD,** ***High-Value Datasets*****)** definidos por la Comisión Europea.

## ¿Qué es DCAT-AP y cómo se aplica en España?

[**DCAT-AP**](https://datos.gob.es/es/documentacion/dcat-ap-y-sus-extensiones-contexto-y-evolucion "DCAT-AP: dcat-ap-y-sus-extensiones-contexto-y-evolucion") es un **perfil de aplicación basado en el vocabulario** [**DCAT**](https://www.w3.org/TR/vocab-dcat/) **del W3C**, diseñado para mejorar la interoperabilidad de los catálogos de datos abiertos del sector público en Europa. Su objetivo es proporcionar un **modelo común de metadatos** que facilite el intercambio, agregación y federación de catálogos de diferentes países y organizaciones (interoperabilidad).

**DCAT-AP-ES**, como perfil de aplicación de DCAT-AP en España, está diseñado para adaptarse a las particularidades del contexto nacional, garantizando una gestión eficiente de los datos abiertos a nivel estatal, autonómico y local.

DCAT-AP-ES, se establece como el estándar a considerar en la nueva versión de la NTI-RISP, que a su vez se enmarca en el **Esquema Nacional de Interoperabilidad (ENI)**, regulado por el Real Decreto 4/2010, que establece las condiciones para la reutilización de la información del sector público en España.

## Principales novedades de DCAT-AP-ES

La nueva versión de DCAT-AP-ES introduce **mejoras significativas que facilitan la interoperabilidad y la gestión de datos en el ecosistema digital**. Entre otras:

**Alineación con DCAT-AP**

- Mayor compatibilidad con los catálogos de datos abiertos europeos al alinear la NTI-RISP con el estándar comunitario DCAT-AP.
- Inclusión de propiedades avanzadas para mejorar la descripción de conjuntos de datos y servicios de datos, de cara a asegurar las posibilidades indicadas a continuación.

**Incorporación de metadatos para la descripción de los Conjuntos de Alto Valor (HVD)**

- Facilitación del cumplimiento de la regulación europea sobre datos de alto valor.
- Posibilidad de descripción detallada de los datos en sectores clave como geoespacial, meteorología, de observación de la tierra y medio ambiente, estadístico, movilidad y empresas.

**Mejoras en la descripción de servicios de datos**

- Inclusión de metadatos específicos para describir API y servicios de acceso a datos.
- Posibilidad de expresar un conjunto de datos en diferentes contextos (ej. geoespacial, con un servidor cartográfico, o estadístico, con una API de datos).

**Soporte para procedencia y calidad de datos**

- Incorporación de nuevas propiedades para gestionar ciclos de vida, versionado y origen.
- Implementación de mecanismos de validación y control de calidad mediante SHACL, asegurando la coherencia y estructura de los metadatos en los catálogos.

**Uso de vocabularios controlados y mejores prácticas**

- Adaptación de vocabularios estandarizados para licencias, formatos de datos, idiomas y temáticas.
- Mayor claridad en la clasificación de datos para facilitar su descubrimiento.

**Gobernanza de datos y mejora en la gestión de agentes**

- Especificación de roles de los agentes (creador, publicador) y puntos de contacto.
- Metadatos mejorados para representar la procedencia de los recursos.

**Validación de conformidad y calidad de los metadatos**

- Guías para ayudar en la validación de metadatos que cumplan con DCAT-AP-ES.
- Validación de grafos DCAT-AP-ES conforme a plantillas SHACL.

## Beneficios clave de la actualización

La adopción de **DCAT-AP-ES** representa un salto cualitativo en la gestión y reutilización de los datos abiertos en España. Entre sus beneficios destacan:

✅ Facilita la federación de catálogos y el descubrimiento de datos.  
✅ Mejora la interoperabilidad con el ecosistema europeo de datos abiertos.  
✅ Cumple con las normativas europeas de datos abiertos.  
✅ Aumenta la calidad de los metadatos mediante mecanismos de validación.  
✅ Asegura que los datos sean FAIR (F *indable, Accessible, Interoperable, Reusable*).

## Implementación y próximos pasos

**¿Cuándo entrará en vigor?**

El nuevo perfil de aplicación **DCAT-AP-ES** se implementará progresivamente en los catálogos de datos abiertos en España. Su aplicación será de carácter obligatorio una vez entre en vigor el texto de la modificación de la norma que, como se indicaba anteriormente, se encuentra en fase de tramitación administrativa pero **ya es compatible con el** [**federador de datos.gob.es**](https://datos.gob.es/es/conocimiento/guias-de-datosgobes)

**¿Existen materiales de apoyo y recursos para la implementación de DCAT-AP-ES?**

El equipo gestor de la plataforma datos.gob.es ha desarrollado la **Guía de implementación de DCAT-AP-ES**, disponible en el [repositorio de datos.gob.es](https://github.com/datosgobes).

Este repositorio se irá enriqueciendo a medida que se identifiquen nuevas necesidades de los usuarios que apliquen el estándar. Así mismo, se desarrollarán guías de ayuda y recursos didácticos que faciliten su adopción por parte de los organismos publicadores. Todas las novedades y recursos que vayan generándose en el contexto del perfil de aplicación se anunciarán y referirán puntualmente en datos.gob.es.

**¿Dónde encontrar más información?**

La documentación actualizada, guías y recursos estarán accesibles en datos.gob.es y en el repositorio de código asociado. En el momento actual se dispone de los siguientes:

- [Guía de implementación de DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES)
- [Manual de convenciones de DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES/convenciones)
- [Ejemplos de implementación de DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES/convenciones)
- [Preguntas frecuentes DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES/faq)
- [Validación de metadatos DCAT-AP-ES](https://datosgobes.github.io/DCAT-AP-ES/validacion)
- Vídeo explicativo DCAT-AP: [español](https://youtu.be/YLwoAEEEyEY) / [inglés](https://youtu.be/9leMao5n1vU)
- [datos.gob.es](https://datos.gob.es/)

Descubre más en este vídeo:

![](https://www.youtube.com/watch?v=l5oQkqqUMVc)

Y en infografía (haz clic para acceder a la versión interactiva y accesible):

[![29 page 0001](https://datos.gob.es/sites/default/files/inline-images/guia-DCAT-AP-ES-Gu%C3%ADas-y-materiales-apoyo-facilitar-su-uso-ES%20%282%29_page-0001.jpg)](https://datos.gob.es/sites/default/files/2025-09/guia-DCAT-AP-ES-Gu%C3%ADas-y-materiales-apoyo-facilitar-su-uso-ES%20%282%29.pdf)

| Guías y materiales de apoyo para facilitar el uso de DCAT-AP-ES | 474.07 KB | PDF |  |
| --- | --- | --- | --- |