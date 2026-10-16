---
title: Schemas - Schema.org
source: https://schema.org/docs/schemas.html
author:
published:
created: 2026-09-21
description: Schema.org is a set of extensible schemas that enables webmasters to embed    structured data on their web pages for use by search engines and other applications.
tags:
  - op/doc/manual
  - tech/interoperability
---
## Schemas

## Organization of Schemas

The schemas are a set of 'types', each associated with a set of properties. The types are arranged in a hierarchy.  
The vocabulary currently consists of 826 Types, 1540 Properties 19 Datatypes, 96 Enumerations and 544 Enumeration members.  
  
**Browse the full hierarchy in HTML:**
- [One page per type](https://schema.org/Thing)
- [Full list of types, shown on one page](https://schema.org/docs/full.html)

**Look up a term using the Term *Finder*:**

  
**Or you can jump directly to a commonly used type:**
- Creative works: [CreativeWork](https://schema.org/CreativeWork "CreativeWork"), [Book](https://schema.org/Book "Book"), [Movie](https://schema.org/Movie "Movie"), [MusicRecording](https://schema.org/MusicRecording "MusicRecording"), [Recipe](https://schema.org/Recipe "Recipe"), [TVSeries](https://schema.org/TVSeries "TVSeries")...
- Embedded non-text objects: [AudioObject](https://schema.org/AudioObject "AudioObject"), [ImageObject](https://schema.org/ImageObject "ImageObject"), [VideoObject](https://schema.org/VideoObject "VideoObject")
- [Event](https://schema.org/Event "Event")
- [Health and medical types](https://schema.org/docs/meddocs.html): notes on the health and medical types under [MedicalEntity](https://schema.org/MedicalEntity "MedicalEntity").
- [Organization](https://schema.org/Organization "Organization")
- [Person](https://schema.org/Person "Person")
- [Place](https://schema.org/Place "Place"), [LocalBusiness](https://schema.org/LocalBusiness "LocalBusiness"), [Restaurant](https://schema.org/Restaurant "Restaurant")...
- [Product](https://schema.org/Product "Product"), [Offer](https://schema.org/Offer "Offer"), [AggregateOffer](https://schema.org/AggregateOffer "AggregateOffer")
- [Review](https://schema.org/Review "Review"), [AggregateRating](https://schema.org/AggregateRating "AggregateRating")
- [Action](https://schema.org/Action "Action")
  
See also the [releases](https://schema.org/docs/releases.html) page for recent updates and project history.  
  
We also have a small set of [primitive data types](https://schema.org/DataType) for numbers, text, etc. More details about the data model, etc. are available [here](https://schema.org/docs/datamodel.html).  
  
Developer information / Download Machine Readable files (RDF, JSON-LD, etc):
- [Schema.org for Developers](https://schema.org/docs/developers.html)

## Extensions

As schema.org has grown, we have explored various mechanisms for [community extension](https://schema.org/docs/extension.html) as a way of adding more detailed descriptive vocabulary that builds on the schema.org core. Some areas of Schema.org were developed as "named extensions", and have dedicated entry pages. We previously called these "hosted" extensions, but they are best considered simply as views into a single collection of schema definitions.

### Hosted Sections

For example, via the [auto](https://schema.org/docs/auto.home.html) section there is a property for [emissionsCO2](https://schema.org/emissionsCO2), and via the [bib](https://schema.org/docs/bib.home.html) section we have a property [publisherImprint](https://schema.org/publisherImprint). However, from the perspective of a publisher, these are simply schema.org properties.

We have a few of these sections:

- [auto](https://schema.org/docs/auto.home.html)
- [bib](https://schema.org/docs/bib.home.html)
- [health-lifesci](https://schema.org/docs/health-lifesci.home.html)
- [meta](https://schema.org/docs/meta.home.html)
- [pending](https://schema.org/docs/pending.home.html)

**Note**: the 'pending' and 'meta' hosted sections are part of schema.org's schema development process.

We use the ' [pending](https://schema.org/docs/pending.home.html) ' section as a staging area for new schema.org terms that are under discussion and review. Implementors and publishers are cautioned that terms in the [pending](https://schema.org/docs/pending.home.html) section may lack consensus and that terminology and definitions could still change significantly after community and [steering group](https://schema.org/docs/about.html#cgsg) review. Consumers of schema.org data who encourage use of such terms are *strongly encouraged* to update implementations and documentation to track any evolving changes, and to share early implementation feedback with the [wider community](http://www.w3.org/community/schemaorg).

The ' [meta](https://schema.org/docs/meta.home.html) ' section is primarily for vocabulary used internally within schema.org to support technical definitions and schema.org site functionality. These terms are not intended for general usage in the public Web.

**[Attic](https://schema.org/docs/attic.home.html)** is a special area where terms are archived when deprecated from the core and other sections, or removed from [pending](https://schema.org/docs/pending.home.html) as not accepted into the full vocabulary. References to terms in the attic area are not normally displayed unless accessed via the term identifier or via the home page. Implementors and data publishers are cautioned not to use terms in the attic area.

Unlike other core and section terms, these areas may be updated at any time without the need for a full [release](https://schema.org/docs/releases.html).

### External Extensions

The schema.org [steering group](https://schema.org/docs/about.html#cgsg) does not officially approve external extensions - they are fully independent. We list here some notable extensions that extend schema.org in interesting and useful ways.

- [GS1 Web Vocabulary](http://gs1.org/voc/) ([blog post](https://blog-schema.org/2016/02/22/gs1-web-vocabulary-welcoming-the-first-schema-org-external-extension/))
- [Croissant](https://mlcommons.org/working-groups/data/croissant/) is an open community-built standardized metadata vocabulary for ML datasets.