---
title: "Using Wikidata’s Ontology in Practice- A Neuro- Symbolic, Community- Centred Workflow for Integrating and Reusing Humanities Datasets"
authors: ""
year: "2025"
Type: ""
DOI: ""
source: ""
created: 2026-10-09
description: ""
tags:
  - clipping/pending-review
pdfORepub: "[[Using Wikidata’s Ontology in Practice- A Neuro- Symbolic, Community- Centred Workflow for Integrating and Reusing Humanities Datasets.pdf]]"
---
[[Using Wikidata’s Ontology in Practice- A Neuro- Symbolic, Community- Centred Workflow for Integrating and Reusing Humanities Datasets.pdf]]
## Full text (extracted from `Using Wikidata’s Ontology in Practice- A Neuro- Symbolic, Community- Centred Workflow for Integrating and Reusing Humanities Datasets.pdf`)

*Source:* `2PDF/PDF/Using Wikidata’s Ontology in Practice- A Neuro- Symbolic, Community- Centred Workflow for Integrating and Reusing Humanities Datasets.pdf`  
*Extracted:* 2026-10-09

```text
DISCUSSION PAPER
CORRESPONDING 
AUTHOR:
Miquel Centelles Velilla
Faculty of Information and 
Audiovisual Media, Universitat 
de Barcelona, Barcelona, 
Catalonia, Spain
miquel.centelles@ub.edu
KEYWORDS:
Wikidata ontology; gender 
equity; neuro-symbolic AI
TO CITE THIS ARTICLE:
Centelles Velilla, M., & 
Ferran-Ferrer, N. (2025). 
Using Wikidata’s Ontology in 
Practice: A Neuro-Symbolic, 
Community-Centred Workflow 
for Integrating and Reusing 
Humanities Datasets. Journal 
of Open Humanities Data, 11: 
84, pp. 1–14. DOI: https://doi.
org/10.5334/johd.439
Using Wikidata’s Ontology 
in Practice: A Neuro-
Symbolic, Community-
Centred Workflow for 
Integrating and Reusing 
Humanities Datasets
MIQUEL CENTELLES VELILLA 
NÚRIA FERRAN-FERRER 
*Author affiliations can be found in the back matter of this article
ABSTRACT
This article presents an ontology-centric workflow for adding, curating, analysing, 
and reusing humanities datasets with Wikidata. Anchored in a digital-humanities 
project that confronts data silos and gendered inequities—especially related to the 
Francoist repression and censorship—it combines a neuro-symbolic AI stack with a 
co-creative, community-driven methodology. We first operationalize “the ontology of 
Wikidata,” clarifying how classes, properties, and constraints behave in practice; how 
reified statements, qualifiers, and references guide modelling choices; and how Entity 
Schemas encode formal, testable expectations. We then detail an ontology-first pipeline 
aligning local humanities databases to Wikidata via reconciliation (OpenRefine), 
controlled property usage (constraints and ShEx), and scaled editing (QuickStatements, 
Mix’n’match). The paper contributes reusable modelling patterns for persons, works, 
events, censorship decisions, and provenance, adaptable across humanities domains. 
Using SPARQL in the Wikidata Query Service (WDQS), we demonstrate discovery and 
analysis alongside metrics for coverage, data quality, and equity—focusing on the 
visibility of women and other gender identities—while situating results within prior 
scholarship on gender gaps and the ways Wikidata mitigates and mirrors societal bias. 
Finally, we show how an ontology-backed knowledge graph (KG) underpins retrieval-
augmented generation (RAG) to reduce large-language-model hallucination and bias, 
detailing how the HerStory NeSyAI project embeds Wikidata structures within an 
explainable neuro-symbolic architecture. Our contribution is case study and template: 
a step-by-step, reproducible method for humanities teams to use Wikidata’s ontology 
not merely to retrieve data but to publish, govern, and reuse datasets with verifiable, 
community-aligned semantics.

2
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439(1) INTRODUCTION: WHY MAKE WIKIDATA’S ONTOLOGY THE 
CENTRE OF A DIGITAL HUMANITIES WORKFLOW?
Humanities research groups routinely produce high-value, domain-specific databases—
yet those datasets remain siloed: duplicated entities across projects, minimal linking to 
external graphs, and limited content transfer to encyclopaedic contexts such as Wikipedia. 
The University of Barcelona (UB) is no exception: dozens of specialized databases coexist 
across research units and service departments, but the same individual or event may appear in 
multiple systems with no durable connection. This fragmentation hinders discovery, analysis, 
and public visibility—especially for women and minoritized gender identities who have 
historically been under-documented (Fan & Gardent, 2022; Ferran-Ferrer et al., 2023 ; Gebru, 
2020; Konieczny & Klein, 2018).
The HerStory NeSyAI project responds to this landscape with a combined neuro-symbolic and 
human-centred AI approach, in which a knowledge graph (KG) and an explicitly modelled 
ontology ensure transparency, provenance, and fairness, while a Large Language Model (LLM) 
provides natural-language affordances (Hitzler et al., 2020 , 2022; Mileo, 2025; Sarker et al., 
2022; Sheth et al., 2023 ). The aim is not merely to consume Wikidata; it is to co-author 
Wikidata—adding, reconciling, and curating humanities data in the open, with community 
feedback and governance, to then reuse that structured data for analysis, visualisation, and 
AI-assisted generation.
This paper therefore places the ontology of Wikidata at centre stage. We use “ontology” 
in the practical Wikidata sense: a living, community-maintained network of classes 
(Wikidata:WikiProject Ontology/Classes , 2022), properties (Help:Properties, 2024), constraints 
(Help:Property Constraints Portal, 2025), and schemas (Extension:EntitySchema , 2025; 
Wikidata:WikiProject Schemas, 2025) that together produce machine-actionable expectations 
about how to describe things. Wikidata’s data model represents knowledge as statements 
(Help:Statements, 2025) with qualifiers (Help:Qualifiers, 2025) and references (Help:Sources, 
2025); “instance of” and “subclass of” (Help:Basic Membership Properties, 2025), and related 
property ecosystems, provide taxonomic backbone; property constraints and Entity Schemas 
articulate and validate best practices; and Resource Description Framework (RDF) exports 
enables SPARQL queries over a shared, global graph.
In this article we treat Wikidata as both an ontology and a socio-technical hub for digital 
humanities workflows. Beyond its class/property hierarchy, it offers a public SPARQL endpoint 
and RDF dumps, a well-documented Application Programming Interface (API), data-quality 
tools, and rich mappings to library catalogues, authority files, and domain vocabularies, which 
make it a natural centre of gravity for cultural heritage and humanities data. Rather than 
competing with aggregators such as Europeana, we use Wikidata’s globally shared graph and 
knowledge organisation system as a reference layer, so that heterogeneous humanities datasets 
can be aligned, audited, recombined, and reused in a transparent way. Our contribution is 
two-fold. First, we offer a methodological blueprint for humanities teams seeking to integrate 
local datasets into Wikidata with an ontology-first mindset, providing modelling patterns and 
practical tools. Second, we present a case study of HerStory NeSyAI, applying these methods 
to the history of Francoist repression and censorship (1936–1975) with the explicit aim of 
increasing the visibility of women and minoritized genders in both scholarly and public records.
We focus on components already implemented and deployed for curatorial use. We present: 
(1) an ontology-first pipeline applied to the Cultura y censura  database and related historical 
datasets; (2) a family of Wikidata-aligned modelling patterns, EntitySchemas, and SPARQL 
queries used for data integration and coverage audits; and (3) the design and initial prototype 
of a KG-supported retrieval-augmented generation (RAG) layer built on top of this pipeline. 
While the pipeline, schemas, and queries are operational, the KG+RAG layer is still at the 
prototype stage; here we concentrate on its architecture and rationale rather than on a full 
quantitative evaluation, which we leave for future work.
The article is organised in nine sections, from an overview of Wikidata’s ontology and our 
ontology-first pipeline to the HerStory case study, SPARQL-based audits, the KG+RAG 
architecture, challenges, limitations, and conclusions.

3
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439(2) WIKIDATA FOR KNOWLEDGE REPRESENTATION 
AND EXTRACTION
Wikidata’s ontology in practice begins with the data model (Wikidata:Data Model, 2025)—
statements, qualifiers, references, and ranks (Help:Ranking, 2025). Wikidata represents 
knowledge as statements —triples whose subject is an item (Help:Items, 2025) (Q-ID), predicate 
a property (P-ID), and object either another item or a literal. Statements may carry qualifiers 
(context such as time, role, location) and references, and each statement has a rank to indicate 
preferred, normal, or deprecated truth status. This model supports complex historical assertions 
(e.g., “work X was banned on date by authority Y in jurisdiction Z, based on statute S”) without 
conflating them into a single flat field. In RDF exports and the query service (Wikidata Query 
Service, 2025; Wikidata:RDF, 2020), these semantics appear as a reified structure: the direct 
edge wdt:P… provides “truthy” assertions for simple graph traversal, while the p:/ps:/pq: 
pattern exposes the statement node and its qualifiers. This reification matters when formulating 
SPARQL that needs qualifiers.
Building on this, classes and properties provide the taxonomic backbone. Wikidata uses “instance 
of” (P31) and “subclass of” (P279) to build a flexible class hierarchy. Instead of a single, fixed 
upper ontology, properties and items evolve through community consensus, property proposals, 
and WikiProjects (Wikidata:Creating a Property Proposal, 2025; Wikidata:Property Proposal, 2025; 
Wikidata:Requests for Comment, 2025; Wikidata:WikiProjects, 2025). For humanities modellers, 
this flexibility is a feature—accommodating diverse traditions and sources—provided we 
formalize our intent with constraints and schemas.
Property constraints function as machine-checkable hints. They are expectations attached to 
properties—for example, that a value type must be human, a property is single-value only, 
or values must be distinct across items. These are not hard prohibitions but validation hints. 
Constraints help align contributions and reduce modelling drift, especially when many 
volunteers curate the same domain; for instance, ensuring that a censorship-decision item uses 
a date, a jurisdiction, and an authority can be encoded as mandatory or suggested constraints.
Where property constraints describe how individual properties should be used, EntitySchemas 
provide testable data shapes for items, expressed in Shape Expressions (ShEx) and stored in 
Wikidata’s E namespace (Extension:EntitySchema , 2025; Wikidata:WikiProject Schemas, 2025; 
Wikidata:WikiProject Schemas/Tutorial, 2025). These schemas let us declare, share, and validate 
a model for a given class—for example, Human, Censorship decision, Work of art, or Archival 
collection—by specifying the expected combination of properties, qualifiers, and references that 
items of that class should satisfy. Schemas act as executable documentation and blueprints 
against which new items can be validated, offering a powerful way to socialise modelling across 
communities. Appendix A collects short ShEx fragments that sketch the EntitySchema patterns 
we use for persons, works, censorship decisions, and repression cases, highlighting their overall 
structure rather than reproducing the full production schemas.
Finally, RDF, SPARQL, and the Query Service operationalise the ontology. Wikidata publishes 
RDF dumps and a public WDQS endpoint (Wikidata:SPARQL Query Service/Wikidata Query 
Help, 2025) that enables expressive SPARQL, which for humanities teams is indispensable 
for coverage audits (for example, the presence of women creators by period or region), data-
quality checks (such as identifying missing references or censorship decisions lacking a source), 
analysis (including the distribution of censored works by year), and reuse (from generating 
datasets to producing curated exports for exhibitions). A basic grasp of the standard prefixes 
(wd:, wdt:, p:, ps:, pq:) and of the “truthy” versus reified split goes a long way (Wikidata:RDF, 
2020; Wikidata:SPARQL Query Service/Wikidata Query Help, 2025 ), with the choice between 
graphs following from the ontology—qualifiers require the reified route (p:/ ps:/pq:). Saved 
queries then support reproducible dashboards for curation sprints (Miquel-Ribé & Laniado, 
2020, 
2021).
(3) AN ONTOLOGY-FIRST PIPELINE FOR HUMANITIES DATASETS
Our pipeline moves from silos to schemas by using Wikidata as both data destination and 
governance layer for shared semantics. As summarised in Figure 1, it has three phases—Phase 

4
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.4391, source analysis and ethical intake; Phase 2, ontology alignment with Wikidata; and Phase 3, 
reconciliation and editing—which we illustrate through a concrete archival example. This last 
Phase leads to SPARQL-based coverage and quality audits and, optionally, a KG+RAG layer. 
Figure 1 Ontology-first 
pipeline for humanities 
datasets.
In Phase 1: source analysis and ethical intake, we inventory tables, fields, vocabularies and 
legal/ethical constraints for each humanities dataset in HerStory NeSyAI, including the Cultura 
y censura database of Francoist book-censorship files and related databases on repression and 
exile. Stakeholders include historians, archivists, librarians, Galleries, Libraries, Archives, and 
Museums (GLAM) staff and community partners. We engage them early to co-define priorities 
and sensitive fields and to design identifiers (IRIs/URIs) that map local keys to stable IRIs 
and record external authorities (Virtual International Authority File or VIAF, Gemeinsame 
Normdatei or GND, Getty or local files) for alignment. Phase 1 also surfaces invisibility and 
bias risks by identifying gaps for women and minoritised genders in both content and schema, 
such as missing roles, ambiguous gender fields or conflated events and decisions.
One key source is the Cultura y censura database. A record for Leo Tolstoy’s Anna Karenina ties 
together an author name, work title, publisher (Editorial Maucci), censorship-file identifier, 
start and end dates, an outcome “Prohibido o suspendido” and an archival reference such as 
“MCD.AGA, Cultura, (03) 050.000, 21/06403, Expediente D 228/39” at the Archivo General de 
la Administración (AGA). In Phase 1 we treat this row as part of a broader corpus, documenting 
its links to other tables, the coding of outcomes and series, reusable external authority files and 
fields (e.g. political or moral labels) that require careful ethical handling before any alignment 
with Wikidata.

5
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439In Phase 2: ontology alignment with Wikidata, we define modelling patterns for each entity 
type—person, group, event, decision and work—choosing existing classes or proposing 
refinements and specifying core properties, qualifiers and sources. We implement these 
patterns as EntitySchemas in the E namespace and validate candidate items against them with 
community feedback. For properties central to the domain, such as “decision applies to work”, 
we also propose or refine property constraints to encourage consistent usage.
Continuing the Anna Karenina example, in Phase 2 we align the record with Wikidata’s ontology 
by reusing existing items and defining a censorship-event pattern. The author matches Leo 
Tolstoy (wd:Q7243), the work Anna Karenina ( wd:Q147787), the publisher Editorial Maucci 
(wd:Q19458589) and the jurisdiction Francoist Spain (wd:Q13474305). We create a new 
item for the censorship file ( wd:QH1), typed as an instance of censorship in Francoist Spain 
(wd:Q27958767, a subclass of censorship, wd:Q543). At work level we attach this event via 
significant event (P793), linking Anna Karenina to a Francoist censorship case. The censorship-
event item records the work, the regime and jurisdiction, start and end dates, the requesting 
publisher and the archive and reference where the file can be found. In Turtle-like notation, the 
core statements for this pattern are:
In Phase 3: reconciliation and scaled editing, we use OpenRefine’s Wikidata reconciliation 
(OpenRefine, 2025) and preview to match local rows to existing items or propose new ones, 
fetching existing claims to avoid duplicates and learn from edit histories. Clean rows become 
QuickStatements (Help:QuickStatements, 2025)  commands with qualifiers and references, 
uploaded in auditable batches. Because Wikidata’s structured data is released under CC0, we 
check that source databases are CC0-compatible or in the public domain, or that individual 
facts and identifiers do not infringe database rights. Where licensing or provenance are 
uncertain, we contribute individual sourced statements rather than bulk dumps and document 
provenance carefully.
After reconciliation in OpenRefine, the Anna Karenina record’s author, work, publisher and 
archival fields are matched to corresponding Wikidata items via the preview interface. The 
cleaned row is converted into a QuickStatements batch that instantiates the censorship-event 
pattern, adding dates, jurisdiction, publisher and archival inventory number as qualifiers and 

6
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439references. As a primary reference we use the AGA archival record, a stable institutional source. 
When an open resource in the Cultura y censura system becomes available, it can be added as a 
secondary reference URL. In the Wikidata reference model, a typical pattern for the “instance 
of: censorship in Francoist Spain” statement would be:
Once this three-phase pattern is in place, SPARQL queries can retrieve this case and similar 
ones. For example, we can find all works with at least one significant event that is an instance of 
censorship in Francoist Spain, returning the work, its author (when available), censorship dates 
and the AGA reference:

7
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439In the rest of the paper, we reuse this example when discussing the censorship-decision pattern 
(Section 4) and SPARQL-based audits (Section 5), so readers can see how a single archival 
record flows through all three phases.
(4) SCENARIO: MODELLING THE HerStory NeSyAI DOMAIN 
WITH WIKIDATA’S ONTOLOGY
HerStory NeSyAI focuses on Francoist repression and censorship of books in Spain (1936–1975) 
through a gender-aware lens, using a database that traces censorship dossiers and publication 
trajectories for thousands of works. Each record links metadata (title, author, language, 
publisher) to one or more censorship files and decisions (dates, reasons, outcomes) and to 
authorities involved. This large database, with tens of thousands of records, is modelled as 
persons (authors, censors, editors), works (submitted and published manifestations), censorship 
files and decisions, and repression cases (e.g. legal proceedings, prison terms, bans). Instead 
of uploading it to Wikidata, we treat it as a testbed for designing and refining ontology-
aligned patterns, EntitySchemas, constraints, and SPARQL queries reusable for other historical 
censorship datasets. The ontology layer builds on a base ontology and enriches it by transforming 
local schemas and integrating Wikidata and Wikipedia categories, while acknowledging where 
categories follow editorial rather than ontological logic.
(4.1) CORE ENTITY TYPES AND PATTERNS
Figure 2 summarises connections between persons, works, authorities, censorship decisions 
(files), and repression cases via core Wikidata properties (e.g. P50 author, P1476 title, P580/
P582 start and end time). We follow the up-to-down flow of Figure 2, from persons and works 
to authorities, decisions, and repression cases; property names are generic, later bound to 
specific P-IDs during schema drafting.
Figure 2 Core entities and 
relations in the HerStory 
NeSyAI censorship and 
repression model.
The person pattern (human) captures names, identifiers, sex or gender with an open vocabulary, 
citizenship, occupations, birth and death (with precision and location), biographical notes, and 
multilingual labels. Qualifiers express roles within decisions or events (for example, censored 
artist versus censor), temporal scoping, and uncertainty (circa dates); references point to 
archival and biographical sources. At least one reliable reference is required for biographical 
claims, and multiple identifiers are encouraged for reconciliation.

8
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439The work pattern (creative, intellectual, or performance) records multilingual titles, creators, form 
or genre, creation or publication dates, medium, languages, and identifiers such as ISBN/ISSN or 
local catalogue numbers. Qualifiers cover edition or version statements and “applies to part” in 
cases of partial censorship, with references drawn from bibliographic records and censorship lists.
The authority or institution pattern (e.g. boards, ministries, courts) includes legal form, 
jurisdiction, and operational period; qualifiers indicate roles in decisions and organisational 
relations, and references cite legislation and administrative decrees. The censorship decision 
pattern, treated as an event-like statement, uses either a dedicated event item (instance of 
censorship decision) or a reified statement on the work (for example, “work X has censorship 
status banned”). Qualifiers record decision date, authority, jurisdiction, legal basis, scope, and 
participants, with references to the documentary source. We prefer event items when decisions 
have substantial context (such as appeals or multiple outcomes) and otherwise use reified 
statements on the work.
The repression case pattern, a person-centred event, mirrors the censorship decision model but 
focuses on a person, recording charges, sentence, detainment or exile, dates and locations, the 
court or authority, and links to co-participants or organisations.
All these patterns are implemented as EntitySchemas so that curators and bots can validate 
items at scale and adjust expectations as edge cases appear. Stored in Wikidata’s EntitySchema 
(E) namespace with stable identifiers (for example, E10 for human), the schemas are 
browsable via standard directories (e.g. Wikidata:Database Reports/EntitySchema Directory, 
2025; Wikidata:Schemas, 2025 ; Wikidata:WikiProject Schemas, 2025 ) and are released under 
CC0 for reuse.
(4.2) MULTILINGUALISM, CULTURAL SPECIFICITY, AND UNCERTAINTY
Wikidata’s multilingual labels let us represent endonyms and exonyms, minority languages, 
and historical spellings, while qualifiers encode uncertainty (e.g., “circa 1941”), contested 
attributions, and partial censorship (only Catalan editions or public performance). The ontology 
therefore encodes uncertainty and specificity  rather than hiding them in notes, consistent with 
HerStory NeSyAI’s human-centred approach, involving user groups—including relatives of 
victims and community historians—in modelling decisions.
(4.3) GENDER MODELLING
HerStory NeSyAI monitors and improves representation of women and minoritized gender 
identities. Prior work has quantified gender gaps in Wikidata (e.g., < ~22% women among 
biographies at one point) and suggests that gaps mirror exogenous social factors rather than 
being exacerbated by Wikidata’s processes, so we add and source missing entities rather than 
treat the gap with complacency (Zhang & Terveen, 2021).
For ontology work, the lesson is to model gender as a first-class, flexible attribute (not limited 
to a binary), to document sources for gender assertions, and to avoid over-constraining schemas 
so that non-binary or historically ambiguous cases are excluded (Abián et al., 2022).
(4.4) GOVERNANCE AND COMMUNITY CO-CREATION
Wikidata’s community debates and remedies weaknesses in the ontology through property 
proposals, constraint tuning, schemas, and tool improvements—an ecosystem we leverage 
and contribute to. HerStory NeSyAI follows an iterative roadmap—conceptualization, design, 
development, implementation and testing, and citizen science—to keep ontology decisions 
transparent, auditable, and co-owned (Centelles & Ferran-Ferrer, 2025; Ferran-Ferrer & 
Centelles, 2025).
(4.5) A LIBRARY AND INFORMATION SCIENCE AND KNOWLEDGE 
ORGANIZATION (LIS/KO)-GROUNDED BIAS MITIGATION AND DATA 
QUALITY ASSURANCE
By an “LIS/KO-grounded” approach to bias and data quality we mean reapplying long-standing 
Library and Information Science and Knowledge Organization practices to Wikidata and 
humanities knowledge graphs. In our workflow this takes four interrelated forms.

9
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439(4.5.1) Authority control and KOS alignment
We map local codes and labels in legacy databases to existing authority structures—Wikidata 
items, library authority files, and, where appropriate, subject headings or classification 
schemes—rather than invent new identifiers. This supports names, places, institutions, and 
topical descriptors and allows us to trace representations across catalogues and compare 
coverage and terminology over time.
(4.5.2) Application profiles and modelling patterns
For each core entity type in the Francoist censorship domain (person, work, censorship file, 
decision, authority, repression case) we define a Wikidata EntitySchema specifying expected 
properties, qualifiers, references, and constraints (Centelles & Ferran-Ferrer, 2024a). These 
schemas combine domain expertise and community discussions and act as reusable modelling 
patterns for other datasets.
(4.5.3) Constraint-based quality assurance
EntitySchemas are complemented by constraints and SPARQL queries that detect structural 
problems such as missing references, inconsistent roles, incomplete or contradictory decisions, 
and implausible dates. Quality control is iterative: queries are rerun after batches of edits, 
results are discussed with domain experts and the wider community, and constraint-aware 
workflows govern sensitive edits (for example, P21) and require citations, following LIS/KO 
traditions that embed control in cataloguing practice and governance.
(4.5.4) Documented provenance and ethical safeguards
For each statement we record its origin (archival source, catalogue entry, dataset), retain local 
identifiers beside global ones, and represent uncertainty explicitly (for example, partial dates 
or conflicting attributions). For sensitive properties such as sex or gender, cause of death, or 
political affiliation, we follow community guidelines and prior Wikidata work to avoid over-
interpretation: we distinguish legal, social, and self-described categories where appropriate, 
require high-quality sources, resist bulk changes that might obscure historical nuance, and align 
local Person tables with Q-items and Human (Q5) EntitySchemas so organisational practice and 
community schemas inform each other (Centelles & Ferran-Ferrer, 2024b).
Together, these four practices operationalise bias mitigation in an auditable, dialogical way, 
making modelling assumptions visible and revisable while keeping authority control, application 
profiles, provenance, and community-governed quality assurance tightly linked.
(5) QUERYING FOR COVERAGE, EQUITY, AND REUSE
SPARQL is central in our workflow. It lets us zoom in on specific, potentially problematic items 
or patterns—for example, censorship decisions that lack sources or works whose censorship 
events have incomplete dates or authorities. SPARQL also supports aggregate queries that 
reveal coverage and equity patterns across time, region, and role, and we use it to assess 
coverage and equity by quantifying the presence and visibility of women and other gender 
identities and by flagging data-quality gaps that obscure representation. Concretely, our queries 
count people who are creators of censored works (born 1900–1960 and linked to Spain), check 
whether they have Wikipedia articles, and surface missing or inconsistent values (such as 
absent references or unscoped roles). We also chart the timeline of censorship decisions by 
authority to identify where groups are under-represented or disproportionately affected. Full 
query texts are provided in Appendix B, which groups the SPARQL queries we rely on in day-to-
day curation under their original headings. For each group we include a short description and 
indicate how it is used in practice—for example, queries that measure coverage of women and 
minoritised genders among creators and subjects; queries that flag missing or inconsistent data 
(such as censorship decisions without dates or archival references); and queries that produce 
timelines and distributions by authority, period, or jurisdiction. Together, these query families 
function as a practical toolkit for monitoring coverage, equity, and data quality in the HerStory 
NeSyAI graph.

10
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439For reuse, the same ontology-aligned approach ensures that exports are schema-conformant and 
immediately usable in downstream workflows. The queries retrieve people, works, decisions, 
and authorities with the qualifiers and references required by our modelling choices—choosing 
the reified route where qualifiers (e.g., decision date, authority, scope) are needed and using 
truthy paths for simpler retrieval—so the resulting datasets are consistent, auditable, and 
reproducible for dashboards, curation sprints, and RAG pipelines.
(6) RETRIEVAL-AUGMENTED GENERATION ON A WIKIDATA-
ALIGNED KNOWLEDGE GRAPH
The workflow described so far is complete without large language models: it already supports 
the integration, validation, and reuse of humanities datasets through Wikidata and SPARQL, 
but a well-structured, constraint-aware knowledge graph can also serve as a reliable backbone 
for RAG workflows.
A RAG couples an LLM with a knowledge base, grounding generation in retrieved evidence 
rather than the model’s parametric memory. In our setting, a retriever first searches a curated 
knowledge base for information relevant to the user’s question (using semantic search over 
texts and graph neighbourhoods); the retrieved context is then concatenated with the question; 
and, finally, the LLM generates an answer conditioned on this enriched prompt. The knowledge 
base itself is implemented as a domain knowledge graph, with an ontology layer (classes 
and properties) and an entity layer (persons, works, events, decisions) that together provide 
structured, explainable context for RAG to consult before and during generation.
HerStory NeSyAI uses LLMs in two places. Upstream, an LLM supports information extraction, 
proposing entities and relations that are checked against Wikidata-aligned schemas before being 
added to the knowledge graph. Downstream, an LLM is embedded in a retrieval-augmented 
generation loop: user questions trigger semantic and graph-based retrieval over the curated 
knowledge graph, and the LLM then generates an answer conditioned on this retrieved context. 
The knowledge graph and its ontology do not generate text on their own; they provide structured, 
referenced constraints that the LLM must respect when proposing statements or narratives.
HerStory NeSyAI’s architecture follows a neuro-symbolic pattern: an LLM for understanding 
and generation, coupled with a KG whose ontology constrains results. RAG uses SPARQL and 
graph neighbourhoods to retrieve verifiable context (items, statements, references, and even 
the Entity Schema that defines a class) before the LLM composes an answer. The result is less 
hallucination, better attribution, and more consistent terminology (e.g. Agrawal et al., 2024; 
Guan et al., 2024; Lavrinovics et al., 2025; Shi et al., 2023; Xu et al., 2024).
In a RAG setting, a language model generates text based on retrieved evidence from external 
resources. In our case, these resources are (a) the Wikidata-aligned graph that we build from 
censorship and repression datasets, and (b) the legacy documents and dossiers linked to it. 
To enhance the transparency of these interactions, Appendix C presents simplified versions 
of the prompts we use to guide LLM-assisted mapping from relational sources to the Wikidata 
ontology. These examples are drawn from two of the databases integrated into the Knowledge 
Graph: Cultura y censura (censorship files from the Francoist regime) and SIDBRINT (Sistema 
d’Informació Digital sobre les Brigades Internacionals—records of brigadistes who fought 
during the Spanish Civil War).
Conceptually, our KG+RAG pipeline proceeds in five steps:
1. Question and document embedding. User questions or task prompts are embedded into a 
vector space, as are text fragments extracted from dossiers, catalogues, and other sources 
associated with entities in the graph.
2. Vector-based retrieval. The system retrieves the most relevant fragments based on vector 
similarity, acting as a first, semantic filter over the document space.
3. Entity and relation grounding. The retrieved fragments are analysed to identify the 
entities (authors, works, authorities, places) and relations they mention, which are then 
resolved to items and properties in the Wikidata-aligned graph.

11
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.4394. Graph-based expansion. Using this grounding, the system issues SPARQL (or SPARQL-
to-Cypher) queries against the knowledge graph to expand the context: for example, 
retrieving all censorship decisions affecting a given work, or all works by a given author 
that share a particular subject or time period.
5. Answer generation with structured context. Finally, the LLM generates an answer or 
explanation using both the retrieved text fragments and the structured graph context. The 
prompt explicitly presents this material as evidence and encourages the model to attribute 
statements and to indicate when the graph does not contain enough information.
Prior work on neuro-symbolic AI and KG-supported question answering suggests that such 
architectures can reduce factual errors and improve attribution compared to free-form 
generation, especially when the underlying graph is curated and constrained. Our contribution 
in this paper is not a full empirical evaluation of KG+RAG performance, but the design of the 
ontology-aligned graph and quality-assurance workflow that make such evaluation possible.
At the time of writing, this KG-supported RAG architecture is implemented as a prototype 
integrated with our HerStory knowledge graph and deployed in the Cultura y censura case 
study. For one pilot dataset of approximately 42,000 extracted fragments and around 11,000 
relations, the extraction pipeline processes a fragment in roughly a few seconds on average, 
with about one percent of fragments failing due to output-format issues and being reprocessed 
at the end of the queue. These figures suggest the approach is practical at the scale of typical 
humanities datasets, but we do not yet have robust statistics on how often curators accept or 
reject LLM-proposed statements. We therefore treat KG+RAG as an architectural extension and 
explicitly list a detailed evaluation of human-in-the-loop performance as future work.
(7) CHALLENGES AND HOW THE ONTOLOGY HELPS 
ADDRESS THEM
Licensing and data donation require particular care: because Wikidata’s structured data is 
released under CC0, institutions must either donate public-domain facts or ensure that database 
rights are compatible with CC0, and the ontology helps operationalise this through schemas that 
require references and encourage per-fact entry rather than bulk copying, easing compliance 
while preserving provenance.
Modelling uncertainty, partial truth, and contested claims is intrinsic to humanities work, 
and Wikidata’s qualifier model allows us to represent approximate dates, partial scope—
such as a ban that applies to performances but not to publication—and contradictory sources 
through multiple referenced statements with ranks; encoding these expectations in Entity 
Schemas ensures that we capture nuance rather than erase it. Multilingual specificity is equally 
important: labels, descriptions, and aliases across languages such as Catalan, Spanish, Basque, 
and Galician are not cosmetic, but retrieval surfaces that shape discovery and community 
reuse, and the ontology can require minimum multilingual metadata per class and align with 
language-specific roles or genres.
Finally, community dynamics and drift are inevitable as Wikidata evolves, so constraints and 
Entity Schemas are treated as living documents and WikiProjects as forums for negotiation. 
Our practice is to publish schemas early, invite commentary, and adjust property choices 
as collective understanding improves, treating ontology as governance rather than a one-off 
deliverable, in line with Wikidata’s schema extension and project pages that encourage this 
style of living blueprints.
(8) LIMITATIONS AND FUTURE WORK
Limitations and future work include evolving patterns—humanities concepts are complex, 
attributions change, and new archival finds recontextualise events—so schemas must remain 
living documents. Coverage must be weighed against bias—adding many items does not in 
itself guarantee equitable representation—hence the need to measure continuously who and 
what the ontology renders visible and to adjust pipelines accordingly, informed by gender-gap 
research and community priorities (Zhang & Terveen, 2021); licensing frictions persist—CC0 
is ideal for reuse but not always compatible with donor datasets—so we prioritise per-fact, 
sourced imports and advocate for open releases where feasible (Wikidata:Licensing, 2023). 

12
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439The public query service imposes rate and complexity limits that favour precomputation or 
partial dumps for heavier analyses, which our workflow anticipates by maintaining cached 
datasets derived from SPARQL (Wikidata Query Service, 2025), and, finally, we must confront 
hallucinations and bias within the KG itself.
(9) CONCLUSION: FROM RETRIEVAL TO CO-CREATION
Wikidata is more than a place to “pull” facts: it is a living ontology and governance layer 
for publishing, validating, and reusing semantically precise humanities data. An ontology-first 
workflow—ethical source analysis and intake; schema-driven modelling with Entity Schemas 
and property constraints; and reconciliation with auditable batch editing—turns local databases 
into shared, queryable, AI-ready resources. We contribute reusable executable shapes for core 
entities—persons, works, censorship decisions, repression cases, provenance—and show how 
SPARQL supports coverage and quality audits and reproducible exports for dashboards and 
KG-grounded RAG.
In HerStory NeSyAI, records of Francoist repression and censorship become visible and testable 
while preserving multilingual specificity, documented uncertainty, and provenance. Constraints 
remain—CC0-compatible data donation, evolving schemas, gender-modelling sensitivities, 
WDQS performance limits—so we treat the ontology as governance: publish shapes early, validate 
routinely, record sources, co-maintain constraints with community. We invite contributions: 
adopt and adapt our Entity Schemas, refine shapes and modelling patterns, align catalogues via 
OpenRefine and Mix’n’match, and publish SPARQL audits others can learn and build on.
Our implementation shows that an ontology-first, Wikidata-centred workflow turns 
heterogeneous databases into a reusable, auditable knowledge graph that supports SPARQL-
based analysis and KG+RAG. We lack fine-grained statistics on LLM suggestion quality and 
curator effort, but logging and analysis infrastructure is being deployed, and evaluating human-
in-the-loop KG+RAG is an important next step. We hope these patterns, schemas, and queries 
help other projects build domain-specific workflows on Wikidata and report successes and 
failures transparently.
ADDITIONAL FILE
The additional file for this article can be found as follows:
•	 Appendices. Appendix A to C. DOI: https://doi.org/10.5334/johd.439.s1
FUNDING STATEMENT
Project Connecting women’s history to Neuro-Symbolic AI: An Information Architecture approach 
to Francoist repression case study (HerStory NeSyAI&NeSyAI) PID2023-147673OB-I00 funded by 
MICIU/AEI/10.13039/501100011033 and by FEDER, EU.
COMPETING INTERESTS
Author Ferran-Ferrer is member of the special collection scientific committee.
AUTHOR CONTRIBUTIONS
Centelles: Conceptualization, Investigation, Methodology, Writing – original draft, Writing – 
review & editing.
Ferran: Conceptualization, Investigation, Writing – original draft.
AUTHOR AFFILIATIONS
Miquel Centelles Velilla  orcid.org/0000-0003-1739-4889 
Faculty of Information and Audiovisual Media, Universitat de Barcelona, Barcelona, Catalonia, Spain
Núria Ferran-Ferrer  orcid.org/0000-0002-9037-8837 
Faculty of Information and Audiovisual Media, Universitat de Barcelona, Barcelona, Catalonia, Spain

13
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439REFERENCES
Abián, D., Meroño-Peñuela, A., & Simperl, E. (2022). An Analysis of Content Gaps Versus User Needs 
in the Wikidata Knowledge Graph. In U. Sattler, A. Hogan, M. Keet, V. Presutti, J. P. A. Almeida, H. 
Takeda, P. Monnin, G. Pirrò, & C. d’Amato (Eds.), The Semantic Web – ISWC 2022 (Vol. 13489, pp. 
354–374). Springer International Publishing. https://doi.org/10.1007/978-3-031-19433-7_21
Agrawal, G., Kumarage, T., Alghamdi, Z., & Liu, H. (2024). Can Knowledge Graphs Reduce 
Hallucinations in LLMs?: A Survey. Proceedings of the 2024 Conference of the North American Chapter 
of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers), 
pp. 3947–3960. https://doi.org/10.18653/v1/2024.naacl-long.219
Centelles, M., & Ferran-Ferrer, N. (2024a). Assessing knowledge organization systems from a gender 
perspective: Wikipedia taxonomy and Wikidata ontologies. Journal of Documentation, 80(7), 124–147. 
https://doi.org/10.1108/JD-11-2023-0230
Centelles, M., & Ferran-Ferrer, N. (2024b). Taxonomies and Ontologies in Wikipedia and Wikidata: An 
In-Depth Examination of Knowledge Organization Systems. Hipertext.Net, 28, 33–48. https://doi.
org/10.31009/hipertext.net.2024.i28.04
Centelles, M., & Ferran-Ferrer, N. (2025, November 3). HerStory-NeSyAI: Designing inclusive metadata 
architectures with hybrid AI for epistemic justice in silenced narratives. DCMI 2025 “(Meta)data at 
the Core: Bridging Human Knowledge and AI Innovation”, Universitat de Barcelona, October 22–25, 
Barcelona. https://doi.org/10.5281/zenodo.17512817
Extension:EntitySchema. (2025, April 16). MediaWiki. https://www.mediawiki.org/wiki/
Extension:EntitySchema. Last accessed date: 2025, November 11.
Fan, A., & Gardent, C. (2022). Generating Biographies on Wikipedia: The Impact of Gender Bias on 
the Retrieval-Based Generation of Women Biographies. Proceedings of the 60th Annual Meeting of 
the Association for Computational Linguistics (Volume 1: Long Papers), pp. 8561–8576. https://doi.
org/10.18653/v1/2022.acl-long.586
Ferran-Ferrer, N., Boté-Vericad, J.-J., & Minguillón, J. (2023). Wikipedia gender gap: A scoping 
review. El Profesional de La Información, 32(5), e320617. https://doi.org/10.3145/epi.2023.nov.17
Ferran-Ferrer, N., & Centelles, M. (2025). Reclaiming Historical Memory through Documentality: Gendered 
Narratives, AI, and Co-Created Archives. Document Society, Unviersitat de Barcelona, October 19–21, 
Barcelona. https://prezi.com/p/s5lj8tlfta2_/document-society-herstory-2025/. Last accessed date: 
2025, November 11.
Gebru, T. (2020). Race and gender. In M. D. Dubber, F. Pasquale, & S. Das (Eds.), The Oxford 
handbook of ethics of AI (pp. 251–269). Oxford University Press. https://doi.org/10.1093/
oxfordhb/9780190067397.013.16
Guan, X., Liu, Y., Lin, H., Lu, Y., He, B., Han, X., & Sun, L. (2024). Mitigating Large Language 
Model Hallucinations via Autonomous Knowledge Graph-Based Retrofitting. Proceedings of the 
AAAI Conference on Artificial Intelligence, 38(16), 18126–18134. https://doi.org/10.1609/aaai.
v38i16.29770
Help:Basic membership properties. (2025, September 3). Wikidata. https://www.wikidata.org/wiki/
Help:Basic_membership_properties. Last accessed date: 2025, November 11.
Help:Items. (2025, July 14). Wikidata. https://www.wikidata.org/wiki/Help:Items
Help:Properties. (2024, September 21). Wikidata. https://www.wikidata.org/wiki/Help:Properties. Last 
accessed date: 2025, November 11.
Help:Property constraints portal. (2025, July 1). Wikidata. https://www.wikidata.org/wiki/
Help%3AProperty_constraints_portal. Last accessed date: 2025, November 11.
Help:Qualifiers. (2025, May 17). Wikidata. https://www.wikidata.org/wiki/Help:Qualifiers. Last 
accessed date: 2025, November 11.
Help:QuickStatements. (2025, October 29). Wikidata. https://www.wikidata.org/wiki/
Help:QuickStatements. Last accessed date: 2025, November 11.
Help:Ranking. (2025, February 9). Wikidata. https://www.wikidata.org/wiki/Help:Ranking. Last 
accessed date: 2025, November 11.
Help:Sources. (2025, November 12). Wikidata. https://www.wikidata.org/wiki/Help:Sources. Last 
accessed date: 2025, November 11.
Help:Statements. (2025, June 5). Wikidata. https://www.wikidata.org/wiki/Help:Statements. Last 
accessed date: 2025, November 11.
Hitzler, P., Bianchi, F., Ebrahimi, M., & Sarker, M. K. (2020). Neural-symbolic integration and the 
Semantic Web. Semantic Web, 11(1), 3–11. https://doi.org/10.3233/SW-190368
Hitzler, P., Eberhart, A., Ebrahimi, M., Sarker, M. K., & Zhou, L. (2022). Neuro-symbolic approaches 
in artificial intelligence. National Science Review, 9(6). https://doi.org/10.1093/nsr/nwac035
Konieczny, P., & Klein, M. (2018). Gender gap through time and space: A journey through Wikipedia 
biographies via the Wikidata Human Gender Indicator. New Media & Society, 20(12), 4608–4633. 
https://doi.org/10.1177/1461444818779080

14
Centelles Velilla and 
Ferran-Ferrer   
Journal of Open 
Humanities Data   
DOI: 10.5334/johd.439
TO CITE THIS ARTICLE:
Centelles Velilla, M., & 
Ferran-Ferrer, N. (2025). 
Using Wikidata’s Ontology in 
Practice: A Neuro-Symbolic, 
Community-Centred Workflow 
for Integrating and Reusing 
Humanities Datasets. Journal 
of Open Humanities Data, 11: 
84, pp. 1–14. DOI: https://doi.
org/10.5334/johd.439
Submitted: 26 October 2025 
Accepted: 02 December 2025 
Published: 30 December 2025
COPYRIGHT:
© 2025 The Author(s). This 
is an open-access article 
distributed under the terms 
of the Creative Commons 
Attribution 4.0 International 
License (CC-BY 4.0), which 
permits unrestricted use, 
distribution, and reproduction 
in any medium, provided the 
original author and source 
are credited. See http://
creativecommons.org/licenses/
by/4.0/.
Journal of Open Humanities 
Data is a peer-reviewed open 
access journal published by 
Ubiquity Press.
Lavrinovics, E., Biswas, R., Bjerva, J., & Hose, K. (2025). Knowledge Graphs, Large Language 
Models, and Hallucinations: An NLP Perspective. Journal of Web Semantics, 85, 100844. https://doi.
org/10.1016/j.websem.2024.100844
Mileo, A. (2025). Towards a neuro-symbolic cycle for human-centered explainability. Neurosymbolic 
Artificial Intelligence, 1, 1–12. https://doi.org/10.3233/nai-240740
Miquel-Ribé, & Laniado, D. (2020). The Wikipedia Diversity Observatory: A Project to Identify and 
Bridge Content Gaps in Wikipedia. ACM International Conference Proceedings Series. https://doi.
org/10.1145/3412569.3412866
Miquel-Ribé, M., & Laniado, D. (2021). The Wikipedia Diversity Observatory: Helping communities to 
bridge content gaps through interactive interfaces. Journal of Internet Services and Applications, 12(1), 
25. https://doi.org/10.1186/s13174-021-00141-y
OpenRefine. (2025). OpenRefine. https://openrefine.org. Last accessed date: 2025, November 11.
Sarker, M. K., Zhou, L., Eberhart, A., & Hitzler, P. (2022). Neuro-symbolic artificial intelligence: 
Current trends. AI Communications, 34(3), 197–209. https://doi.org/10.3233/AIC-210084
Sheth, A., Roy, K., & Gaur, M. (2023). Neurosymbolic Artificial Intelligence (Why, What, and How). 
IEEE Intelligent Systems, 38(3), 56–62. https://doi.org/10.1109/MIS.2023.3268724
Shi, X., Zhu, Z., Zhang, Z., & Li, C. (2023). Hallucination Mitigation in Natural Language Generation 
from Large-Scale Open-Domain Knowledge Graphs. Proceedings of the 2023 Conference on Empirical 
Methods in Natural Language Processing, pp. 12506–12521. https://doi.org/10.18653/v1/2023.emnlp-
main.770
Wikidata Query Service. (2025, October 24). Wikitech. https://wikitech.wikimedia.org/wiki/Wikidata_
Query_Service. Last accessed date: 2025, November 11.
Wikidata:Creating a property proposal. (2025, October 21). Wikidata. https://www.wikidata.org/
wiki/Wikidata:Creating_a_property_proposal. Last accessed date: 2025, November 11.
Wikidata:Data model. (2025, June 8). Wikidata. https://www.wikidata.org/wiki/Wikidata:Data_model. 
Last accessed date: 2025, November 11.
Wikidata:Database reports/EntitySchema directory. (2025, November 1). Wikidata. https://www.
wikidata.org/wiki/Wikidata:Database_reports/EntitySchema_directory. Last accessed date: 2025, 
November 11.
Wikidata:Licensing. (2023, January 26). Wikidata. https://www.wikidata.org/wiki/Wikidata:Licensing. 
Last accessed date: 2025, November 11.
Wikidata:Property proposal. (2025, April 21). Wikidata. https://www.wikidata.org/wiki/
Wikidata:Property_proposal. Last accessed date: 2025, November 11.
Wikidata:RDF. (2020, December 31). Wikidata. https://www.wikidata.org/wiki/Wikidata:RDF/es. Last 
accessed date: 2025, November 11.
Wikidata:Requests for comment. (2025, November 17). Wikidata. https://www.wikidata.org/wiki/
Wikidata:Requests_for_comment. Last accessed date: 2025, November 11.
Wikidata:Schemas. (2025, November 21). Wikidata. https://www.wikidata.org/wiki/Wikidata:Schemas. 
Last accessed date: 2025, November 11.
Wikidata:SPARQL query service/Wikidata Query Help. (2025, November 4). Wikidata. https://www.
wikidata.org/wiki/Wikidata:SPARQL_query_service/Wikidata_Query_Help. Last accessed date: 2025, 
November 11.
Wikidata:WikiProject Ontology/Classes. (2022, July 5). Wikidata. https://www.wikidata.org/wiki/
Wikidata:WikiProject_Ontology/Classes. Last accessed date: 2025, November 11.
Wikidata:WikiProject Schemas. (2025, May 7). Wikidata. https://www.wikidata.org/wiki/
Wikidata:WikiProject_Schemas. Last accessed date: 2025, November 11.
Wikidata:WikiProject Schemas/Tutorial. (2025, August 27). Wikidata. https://www.wikidata.org/
wiki/Wikidata:WikiProject_Schemas/Tutorial. Last accessed date: 2025, November 11.
Wikidata:WikiProjects. (2025, November 11). Wikidata. https://www.wikidata.org/wiki/
Wikidata:WikiProjects. Last accessed date: 2025, November 11.
Xu, J., Zhang, H., Zhang, H., Lu, J., & Xiao, G. (2024). ChatTf: A Knowledge Graph-Enhanced 
Intelligent Q&A System for Mitigating Factuality Hallucinations in Traditional Folklore. IEEE Access, 
12, 162638–162650. https://doi.org/10.1109/ACCESS.2024.3485877
Zhang, C. C., & Terveen, L. (2021). Quantifying the Gap: A Case Study of Wikidata Gender 
Disparities. 17th International Symposium on Open Collaboration, pp. 1–12. https://doi.
org/10.1145/3479986.3479992
```
