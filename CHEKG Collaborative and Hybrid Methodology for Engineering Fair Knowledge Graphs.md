---
title: "CHEKG: a collaborative and hybrid methodology for engineering modular and fair domain-specific knowledge graphs"
year: "2024"
Type: Article
DOI: 10.1007/s10115-024-02110-w
source: https://doi.org/10.1007/s10115-024-02110-w
created: 2026-04-24
description: "AbstractOntologies constitute the semantic model of Knowledge Graphs (KGs). This structural association indicates the potential existence of methodological analogies in the development of ontologies and KGs. The deployment of fully and well-defined methodologies for KG development based on existing "
tags:
  - design/UCD/participation
  - op/doc/similar
  - Tech/SemanticWeb/KG
  - Tech/SemanticWeb/collaborative
  - Tech/SemanticWeb/KG/evaluation
pdfORepub: "[[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf]]"
Title: CHEKG a collaborative and hybrid methodology for engineering modular and fair domain-specific knowledge graphs
author: Angelis, S., Moraitou, E., Caridakis, G., Kotis, K.
Journal: Knowledge and Information Systems
Volume: "66"
Issue: "8"
Pages: 4899-4925
Abstract: Presents a methodology that includes tasks for "assessing and mitigating bias at schema and data levels" in knowledge graphs. The CHEKG methodology addresses bias assessment as part of the knowledge graph engineering lifecycle.
doi: 10.1007/s10115-024-02110-w
---

[[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf]]

> **Abstract:** AbstractOntologies constitute the semantic model of Knowledge Graphs (KGs). This structural association indicates the potential existence of methodological analogies in the development of ontologies and KGs. The deployment of fully and well-defined methodologies for KG development based on existing ontology engineering methodologies (OEMs) has been suggested and efficiently applied. However, most of the modern/recent OEMs may not include tasks that (i) empower knowledge workers and domain experts to closely collaborate with ontology engineers and KG specialists for the development and maintenance of KGs, (ii) satisfy special requirements of KG development, such as (a) ensuring modularity and agility of KGs, (b) assessing and mitigating bias at schema and data levels. Toward this aim, the paper presents a methodology for the Collaborative and Hybrid Engineering of Knowledge Graphs (CHEKG), which constitutes a hybrid (schema-centric/top-down and data-driven/bottom-up), collaborative, agile, and iterative approach for developing modular and fair domain-specific KGs. CHEKG contributes to all phases of the KG engineering lifecycle: from the specification of a KG to its exploitation, evaluation, and refinement. The CHEKG methodology is based on the main phases of the extended Human-Centered Collaborative Ontology Engineering Methodology (ext-HCOME), while it adjusts and expands the individual processes and tasks of each phase according to the specialized requirements of KG development. Apart from the presentation of the methodology per se, the paper presents recent work regarding the deployment and evaluation of the CHEKG methodology for the engineering of semantic trajectories as KGs generated from unmanned aerial vehicles (UAVs) data during real cultural heritage documentation scenarios.
## Full text (extracted from `CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf`)

*Source:* `2PDF/CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf`  
*Extracted:* 2026-04-24

```text
Knowledge and Information Systems (2024) 66:4899–4925
https://doi.org/10.1007/s10115-024-02110-w
REGULAR PAPER
CHEKG: a collaborative and hybrid methodology for
engineering modular and fair domain-speciﬁc knowledge
graphs
Sotiris Angelis 1 · Efthymia Moraitou 1 · George Caridakis 1 ·
Konstantinos Kotis 1
Received: 5 October 2023 / Revised: 1 February 2024 / Accepted: 21 March 2024 /
Published online: 20 April 2024
© The Author(s) 2024
Abstract
Ontologies constitute the semantic model of Knowledge Graphs (KGs). This structural asso-
ciation indicates the potential existence of methodological analogies in the development of
ontologies and KGs. The deployment of fully and well-deﬁned methodologies for KG devel-
opment based on existing ontology engineering methodologies (OEMs) has been suggested
and efﬁciently applied. However, most of the modern/recent OEMs may not include tasks
that (i) empower knowledge workers and domain experts to closely collaborate with ontology
engineers and KG specialists for the development and maintenance of KGs, (ii) satisfy special
requirements of KG development, such as (a) ensuring modularity and agility of KGs, (b)
assessing and mitigating bias at schema and data levels. Toward this aim, the paper presents a
methodology for the Collaborative and Hybrid Engineering of Knowledge Graphs (CHEKG),
which constitutes a hybrid (schema-centric/top-down and data-driven/bottom-up), collabo-
rative, agile, and iterative approach for developing modular and fair domain-speciﬁc KGs.
CHEKG contributes to all phases of the KG engineering lifecycle: from the speciﬁcation
of a KG to its exploitation, evaluation, and reﬁnement. The CHEKG methodology is based
on the main phases of the extended Human-Centered Collaborative Ontology Engineering
Methodology (ext-HCOME), while it adjusts and expands the individual processes and tasks
of each phase according to the specialized requirements of KG development. Apart from the
presentation of the methodology per se, the paper presents recent work regarding the deploy-
ment and evaluation of the CHEKG methodology for the engineering of semantic trajectories
B Sotiris Angelis
sotiris@aegean.gr
B Konstantinos Kotis
kotis@aegean.gr
Efthymia Moraitou
e.moraitou@aegean.gr
George Caridakis
gcari@aegean.gr
1 Department of Cultural Technology and Communication, University of the Aegean, University Hill,
81100 Mytilene, Greece
123

4900 S. Angelis et al.
as KGs generated from unmanned aerial vehicles (UA Vs) data during real cultural heritage
documentation scenarios.
Keywords Knowledge graph · Engineering methodology · Collaborative engineering of
knowledge graphs · Hybrid engineering of knowledge graphs
1 Introduction
The KGs are increasingly used in research and business, while their development and deploy-
ment present a close association with Semantic Web (SW) technologies (including Ontologies
and Linked (Open) Data), large-scale data analytics, and cloud computing [ 1]. As mentioned
in Ehrlinger and Wöß [ 1], KGs have been in the focus of research since the introduction of
Google’s Knowledge Graph in 2012, resulting in a variety of descriptions and deﬁnitions of
the term such as the ones provided by Paulheim [ 2] and Ehrlinger and Wöß [ 1]. The descrip-
tion of Kejriwal [ 3] states that the requirements a graph must ﬁll to be considered a KG, are
(i) its meaning to be expressed as structure, (ii) its statements to be unambiguous, and (iii)
to use a limited set of relation types.
The technologies that can be deployed in order to build a KG, include (i) knowledge
representation and reasoning (languages, schema, and standard vocabularies), (ii) knowl-
edge storage (graph databases and repositories), (iii) knowledge engineering (methodologies,
editors, and design patterns), and (iv) knowledge learning (including schema learning and
population) [4]. Different platforms and suites, which partially or fully support the aforemen-
tioned technologies, have been developed, thus providing the necessary tools and processes
for the development, maintenance, and use of KGs (e.g., Neo4j suite [ 5], OpenLink Virtuoso
platform [ 6], RDFox [ 7]).
The development of KGs presents a close association with ontologies. In most cases
(DBpedia [ 8], Wikidata [ 9], Y AGO [ 10], Google KG [ 11]) ontologies constitute the
backbone of KGs, since they are the semantic model or models that KGs incorporate. Formal
ontologies are currently the most popular technology for developing semantic models to
represent a particular domain of knowledge formally and explicitly.
Several methodologies have been proposed through the years for engineering ontologies
[12–22]. The ontology lifecycle, which includes feasibility analysis, identiﬁcation of goals,
requirements speciﬁcation, implementation, evaluation, and maintenance, is deﬁned almost
similarly by different ontology engineering methodologies (OEMs), and it is partially or
fully supported by ontology engineering (OE) tools [ 19]. Based on the obvious association
of ontologies and KGs, Carriero et al. [ 23] suggested that the ontology and the related KG
can be both developed following the engineering principles, or similar/analogous tasks and
steps, of the same OEM. This approach sets the methodological steps of the KG lifecycle,
including its semantic model, in a way that is consistent and—probably—familiar to the
specialists who are involved in the development of a KG. According to several methodolog-
ical approaches, OE is mainly driven by the ontology engineer, i.e., the person who has the
knowledge/expertise to deﬁne ontological speciﬁcations and to coordinate an OE task. How-
ever, the role and active involvement in the ontology lifecycle of (i) domain experts, who
have the knowledge/expertise of the domain and/or data sources, as well as (ii) knowledge
workers, who exploit the ontology in ‘operational’ conditions (e.g., solve problems, perform
data-driven analysis tasks) is considered equally useful and essential for human-centered and
collaborative approaches [ 13, 15, 19, 22–24].
123

CHEKG: a collaborative and hybrid methodology… 4901
Collaborative OEMs deﬁne, in a systematic way, phases, tasks, and workﬂows which
emphasize the active and decisive involvement of ontology engineers, knowledge workers,
and domain experts throughout OE process via their close and continuous collaboration [ 19].
This approach signiﬁcantly empowers the knowledge workers and domain experts, people
who have the knowledge and the expertise of the domain of interest, though they may be not
familiar with the (i) formal representation languages, (ii) knowledge engineering principles,
and iii) methods for constructing and synthesizing ontologies [ 15, 19, 22, 24]. Knowledge
workers and domain experts actively participate in the collaborative OE processes, along with
ontology engineers, and they are able to develop, evaluate, and evolve ontologies individually
and conversationally with their co-workers, according to their skills, knowledge base, and
context of work [ 19, 22].
Since collaborative OEMs are considered beneﬁcial for the complete and consistent
development of ontologies in a human-centered manner [ 15, 19], their principles and tasks
could also be adapted for the development of KGs. Thus, the collaborative approach could
involve participants of different levels of expertise related to KG development, enriching,
and maintenance, in a continuous and systematic collaboration.
This paper presents the methodology of Collaborative and Hybrid Engineering of Knowl-
edge Graphs (CHEKG—pronounced “check”) which was ﬁrst introduced as ongoing work
in Moraitou et al. [ 25]. CHEKG constitutes a hybrid (schema-center/top-down and data-
driven/bottom-up), collaborative, and iterative approach for KG development. The CHEKG
methodology is based on the main methodological phases of the latest version of ext-HCOME
OE methodology [ 26], while it adjusts and expands the individual processes and tasks of each
phase according to the KG development specialized requirements (modularity of KG’s model
and content, agility, data quality, and bias). Although there are several other agile OEMs such
as UPONLite [ 21], SAMOD [ 20], AGIScont [ 22], and XD [ 27] that could be exploited or
adapted for KG development, the presented work is novel since, to the best of our knowledge,
another effort to adapt a collaborative, iterative, and agile methodology to propose a methodol-
ogy for engineering domain-speciﬁc modular and fair KGs, has not been presented elsewhere
yet. Apart from the presentation of the methodology per se, the paper presents current
work regarding the deployment of CHEKG methodology for the development of domain-
speciﬁc KGs for the representation of semantic trajectories generated from UA Vs data. This
work is motivated by, and evaluated based on, the application domain of UA V missions for
documenting regions of cultural heritage interest, which is presented in Kotis et al. [ 28].
The structure of the paper is as follows: Sect. 2 reviews existing methodological steps
for KG development, while it discusses the lack of human-centered and specialized tasks
for KG maintenance. Section 3 extensively presents phases, processes, and tasks of CHEKG
methodology. Section 4 describes the main results of the implementation and evaluation
of the CHEKG methodology with domain-speciﬁc KG development; Sect. 5 discusses the
ﬁndings and limitations of the proposed approach. Finally, Sect. 6 concludes the paper.
2 Related work
In addition to the ext-HCOME, other collaborative and agile OEMs support ontology lifecy-
cle in a systematic way, which emphasize the active and decisive involvement of ontology
engineers, knowledge workers, and domain experts throughout OE process via their close
and continuous collaboration [ 19]. Their structure comprises three main phases: (a) ontol-
ogy speciﬁcation, (b) ontology development, and (c) ontology exploitation and evaluation
123

4902 S. Angelis et al.
phase. Common tasks include the deﬁnition of ontology’s scope and aim, ontological deﬁni-
tions’ reuse, model and instance deﬁnition, validation through exploitation in use cases, and
reﬁnement/maintenance through iteration. The following representative OEMs are brieﬂy
presented as example related work, selected mainly for being recently proposed method-
ologies, that incorporate agile principles and underline the importance of collaboration by
providing clear instructions and reducing the dependence on ontology engineers.
UPON Lite is an OEM emphasizing a participative social approach. It reduces the role of
ontology engineers, allowing domain experts, knowledge workers, and end-users to collabo-
ratively build ontologies using user-friendly tools. The six-step process includes identifying
terminology, deﬁning a glossary, generating a concept taxonomy, connecting entities, deﬁn-
ing parthood, and developing the ontology. The methodology supports agile collaboration,
exploitation, and evaluation of ontologies.
SAMOD proposes a simpliﬁed and agile approach to ontology development, inspired by
test-driven development processes. The methodology is iterative, focusing on documented
ontology creation from typical examples of domain descriptions, using motivating scenar-
ios and competency questions (CQs). Collaboration occurs between domain experts and
ontology engineers at the initial steps. SAMOD employs an evolving prototype approach,
where ontologists collect requirements from domain experts, develop an initial model, and
iteratively reﬁne it based on scenarios until it satisﬁes all CQs.
AgiSCOnt goes a few steps further, proposing an end-to-end OE process, addressing
project objectives, tools, scheduling, budgeting, and resource allocation. The three steps of
AgiSCOnt involve analysis and conceptualization, development and testing, and ontology use
and updating. The methodology encourages collaboration between ontology engineers and
domain experts, leveraging knowledge elicitation techniques, conceptual maps, and CQs to
develop ontologies iteratively, with a focus on the reuse of and alignment to existing models.
To the best of our knowledge, this is the latest new and maintained collaborative and agile
OEM (along with ext-HCOME).
KGs are exploited in order to semantically enrich large amounts of data found in various
data silos, adding value to it, so that it can be (re)used in a meaningful, machine-processable,
and more intelligent way [ 29]. The processes/tasks for the development and maintenance of
a KG may vary, and therefore different guidelines and extensive methodologies have already
been proposed. The following paragraphs present related work that is selected due to the fact
that they are comprehensive methodologies covering the entire KG engineering lifecycle.
More speciﬁcally, they were selected based on their utility and reproducibility across a variety
of scenarios, while they are not applicable only to a speciﬁc domain. as others ([ 30–33]) or
based solely on data-driven approaches, as others ([ 34–36]). Our literature review focused on
the latest ﬁve-year period, within various sources, including Google and Semantic Scholar,
IEEE Explore, ACM Library, ScienceDirect, and Scopus. The sources were queried with the
keywords “Knowledge Graph” followed by “development,” “construction,” “engineering,”
“lifecycle,” and “methodology.”
As Fensel et al. [ 29] suggest, the major steps of an overall process model for KG engi-
neering are (i) knowledge creation, which is a knowledge acquisition phase that establishes
the core data for a KG, (ii) knowledge hosting, (iii) knowledge curation, (iv) knowledge
deployment, which is the actual application of the KG in a speciﬁc application domain for
problem-solving.
A work that discusses the need for guidance on KG development, as they are widely
used in various AI-driven tasks with large-scale data, is presented in Tamašauskait˙ ea n d
Growth [ 37]. It aims to provide guidance in planning and managing the process of KG
development, by synthesizing common steps described in academic literature and presenting
123

CHEKG: a collaborative and hybrid methodology… 4903
a KG development and maintenance process. The process involves steps that include data
identiﬁcation, ontology creation, data mapping, knowledge extraction, visualization, KG
reﬁnement, and the deployment and maintenance of the KG.
Apart from the suggestion of particular methodological steps for KG development, a few
extended methodological approaches have also been suggested. For instance, a recent work
presents a bottom-up approach to curate entity-relation pairs and construct KGs and question-
answering models for cybersecurity education [ 38]. The methodology includes three main
phases: (i) knowledge acquisition, (ii) knowledge storage, and (iii) knowledge consumption.
Regarding the use of fully and well-deﬁned methodologies for KG development, the
exploitation of existing OEMs has been suggested. Particularly, the Extreme Design (XD)
methodology has been used for the development of ArCo KG and its underlying ontology
[23]. The methodology includes a set of major procedures: (i) requirement engineering, (ii)
CQs, (iii) matching CQs to ontology design patterns (ODPs), (iv) testing and integration,
(v) evaluation. Sequeda and Lassila [ 39] describe the phases of Designing and Building
Enterprise KG and identify the involved people, the KG management, and the necessary
tools for developing a KG.
The different guidelines and methodologies present some similarities, especially regarding
the main tasks/processes that must be followed for KG development. For instance, the iden-
tiﬁcation of KG requirements, the deﬁnition of data that it will capture, the efﬁcient choice
or development of the underlying knowledge model, the consistent evaluation and correction
of the KG, the enrichment and augmentation of the KG, and ﬁnally the implementation of
the KG for speciﬁc services or processes, are all crucial/important tasks. Additionally, the
data and knowledge (conjointly or individually) are at the center of the development since
they are vital parts of the KG.
Although bottom-up (data-driven) and top-down (schema-centric) approaches for the con-
ceptualization of the knowledge that the KG captures are both necessary (constituting a
hybrid knowledge conceptualization approach), the role and speciﬁc activities that involved
people must follow have not been described in detail and have not been emphasized in
methodological phases and steps. Emphasizing a human-centered, collaborative, and hybrid
approach that focuses on speciﬁc domains, could empower the involved stakeholders, namely
domain experts, knowledge engineers, knowledge workers, and bias/fairness experts, to be
continuously involved in the KG engineering lifecycle. Such an approach could incorpo-
rate all the different KG development tasks and organize them in unambiguous phases,
clarifying the roles of the involved members of the development team, exploiting their spe-
cialized knowledge in conceptualization, data/knowledge acquisition, KG deployment, and
KG evaluation.
A comparison of the aforementioned related work and their mapping to the proposed
methodology is presented in the discussion section.
3 The CHEKG methodology
The HCOME constitutes a human-centered collaborative OEM, according to which the
ontologies are engineered individually, as well as collaboratively. The HCOME supports
the involvement of knowledge workers, and it requires the use of tools which facilitate
the management and interaction with conceptualizations in a direct and iterative way. The
methodology is organized into three main phases, namely, speciﬁcation, conceptualization,
and exploitation/evaluation, emphasizing on discussion and argumentation of the participants
123

4904 S. Angelis et al.
over the conceptualization, the detailed versioning of the speciﬁcations, and the overall man-
agement of the developed ontology. The basic tasks of HCOME are enriched by data-driven
(bottom-up) conceptualization tasks [ 40], supported by the learning of seed ontologies. A
stand-alone OE integrated environment, namely HCONE, has been used until 2010 to support
management and versioning tasks in the individual space of participants, while the Semantic
Media Wiki-based shared environment, namely Shared-HCONE [ 41], has been used to sup-
port evaluation tasks and the argumentation-based discussions in the collaborative space of
the participants. Today, the HCOME is supported by alternative tools, such as Protégé [ 42],
Web-Protégé, email lists, and shared cloud workspaces, mainly for the collaborative space
tasks [ 19]. The latest version of the ext-HCOME methodology [ 26] has been updated with
the modularization and bias-assessment/mitigation tasks.
Based on the HCOME methodology, a hybrid (schema-centric/top-down and data-
driven/bottom-up), human-centered, collaborative, iterative, and agile methodology for the
engineering of modular and fair KGs contributes to all phases of the KG engineering lifecy-
cle: from the speciﬁcation of a KG to its creation, exploitation, and evaluation. The proposed
methodology provides a distinction between speciﬁc processes of each phase, while it breaks
down the processes into tasks that can be performed either individually (in a personal engi-
neering space) or collaboratively by all members of the KG engineering team. It is considered
that team members may engineer KGs in their personal space, while they perform individual
tasks, but they may also exploit a shared engineering space in cases where they perform col-
laborative/argumentation tasks. The tasks that can be performed in shared spaces are tasks
which (i) can—technically—be performed using a collaborative ﬁle/software and (ii) depend
on synchronous and asynchronous discussion and contribution by different members. Col-
laboration (and decentralized workﬂow) could be supported by speciﬁc collaborative tools
such as WebProtege, git repositories such as GitHub, and cloud collaboration workspaces
such as Google workspace, as well as by using emails and videoconferencing. It is possible
for a team member to initiate any task either in a personal or a shared space or take part in
any other task which has already been initiated by other members. Shared space is indicated
with the letter ‘S’ and personal space is indicated with the letter ‘P’ in the description of each
task.
Within the process of KG engineering, there are both mandatory and optional tasks, each
serving distinct purposes. Mandatory tasks such as data modeling or storing and query-
ing knowledge are essential for the development and usage of every KG, without which a
KG could not exist or be considered a KG. Optional tasks, on the other hand, such as the
semantic enrichment and the assessment/mitigation of bias, may be used to reﬁne and add
value to a KG, can be deferred to subsequent iterations or can be applied according to the
context of work. The optionality of tasks’ execution is mainly determined by a combination
of project-speciﬁc factors, including resources, requirements, constraints, and domain com-
plexity. Mandatory tasks must be performed in the speciﬁc order that are mentioned for the
ﬁrst iteration. However, since CHEKG follows an iterative approach, additional iterations
may start from any task that is required. Mandatory tasks are indicated with the letter ‘M’ and
optional with the letter ‘O’ in the description of each task. The following sections describe
the processes and tasks of each phase of CHEKG methodology, as depicted in Figs. 1 and 2.
3.1 KG specification phase
The KG speciﬁcation phase establishes the involved team, as well as the context of work
regarding the KG development. During this phase, the members of the team are identiﬁed and
123

CHEKG: a collaborative and hybrid methodology… 4905
Fig. 1 Phases and processes of the CHEKG methodology
their role in the whole endeavor is deﬁned. Consequently, the involved team starts discussions
over the aim, scope, and requirements of the KG, while it composes speciﬁcation docu-
ments, for example the Ontology Requirements Speciﬁcation Document [ 43], that describe
the aforementioned—agreed—information. Additionally, during this phase, the main data
sources that will be exploited for KG development are detected. This phase may start from
a member of the team or a small-core group of the team (e.g., the knowledge engineers)
who has made some preliminary work for the identiﬁcation of the KG model and data, and
who needs the contribution of other colleagues and domain experts for the validation and
elaboration of this work. The KG speciﬁcation phase (Phase 1) is mainly performed within
the shared space, and it includes:
Process 1.1. The speciﬁcation of the involved team. This process is further analyzed in the
following tasks:
 Task 1.1.1: Identify collaborators (i.e., domain experts, knowledge engineers, knowledge
workers, bias experts), in order to determine the people who will be involved and their
background and interest in the endeavor. (S, M)
 Task 1.1.2: Determine team’s composition and members’ roles to establish the work team
and organize (if needed) subgroups of the team which could contribute to different tasks
or have a different level of involvement in different tasks. (S, M)
Process 1.2. The speciﬁcation of aim, scope, and requirements of the KG. This process is
further analyzed in the following tasks:
123

4906 S. Angelis et al.
Fig. 2 Tasks of CHEKG methodology
123

CHEKG: a collaborative and hybrid methodology… 4907
 Task 1.2.1: Specify the aim and scope of required and/or available data, which is an
essential task in order to (i) establish a common perception of the domain that the KG
will cover and (ii) agree upon the reason for the KG creation, between the different
members of the team. (S, M)
 Task 1.2.2: Identify the main data sources, such as datasets, taxonomies, and other infor-
mation, which will be the initial sources that will supply the KG with data. The sources
may be proprietary, open, or commercially available. They should be chosen taking into
account the speciﬁed aim and scope of the KG, as well as the considerations of future
KG maintenance (e.g., possibility of KG update with new data from the available data
sources). The sources are also used during KG model establishment and evaluation. (S,
M)
 Task 1.2.3: Discuss and specify the design requirements of the KG that will be commonly
understood and accepted by the work team. Important design requirements that need to be
speciﬁed in the design of the KG are: Scalability, Performance, Interoperability, Semantic
Expressiveness, Reusability, Data Quality, Privacy. (S, M)
 Task 1.2.4: Establish domain-related questions to be answered by exploiting the engi-
neered KG (eventually) and formulate CQs. The CQs will be useful for the KG model
development and KG evaluation. This task is highly recommended, and it is considered
best practice. It is set as optional since in simplistic, well-deﬁned, or experimental cases
it can be loosely covered by tasks 1.2.1 and 1.2.3. (S, O)
 Task 1.2.5: Produce speciﬁcation documents for the KG, in order to record and share
agreed speciﬁcations in appropriate collaborative forms and documents (e.g., shared
cloud workspaces). (S & P , M)
It is worth mentioning that task 1.2.5 can be performed either in a shared or a personal space,
but in any case, it must be communicated and agreed upon by all the members of the involved
team.
The possible roles of members of the KG engineering team could be: Domain Expert,
Knowledge engineer/Ontologist, Data Scientist, Software Engineer, Quality Assurance Spe-
cialist, Bias Expert, Privacy Expert, Security Engineer, and End-User/Customer. Roles may
vary depending on the project and the involved team, while it is possible that individuals have
overlapping roles/responsibilities or change roles during the engineering process. For exam-
ple, a Domain Expert could also be assigned the role of an End-User. As it is also proposed
in HCOME methodology, in CHEKG methodology the roles of all stakeholders are equal,
and all participants must be involved toward a true collaborative engineering experience.
3.2 KG development phase
The KG development phase follows the KG speciﬁcation phase, during which the involved
team, either working on a shared or a personal space, develops the model, the data, and the
infrastructure which will store the KG. It is possible that different members or subgroups of
the involved team may focus on one or more areas of work, e.g., ontology engineers may
focus on explicit knowledge creation of the KG (i.e., the semantic model of the KG, in other
words, the KG’s schema). The KG development phase (Phase 2) includes:
Process 2.1. The creation of explicit knowledge, which refers to the semantic model that the
KG incorporates. This process is analyzed in the following tasks:
123

4908 S. Angelis et al.
 Task 2.1.1: Consult experts by discussion, in order to better understand the domain of
interest. Identify concepts that can be grouped as modules of the subdomain concep-
tualization, based on the project requirements and objectives. This is a human-centric
approach for the KG model development. This task could be omitted in simplistic cases
or in cases of reusing a well-established schema that covers the domain of interest (S,
O).
 Task 2.1.2: Gather, analyze, and clean data of the identiﬁed main data sources, in order
to identify central concepts and relations, as well as to outline the content that the KG
model should represent. The cleaning and correction of data will improve their quality,
making them most applicable for the analysis and later KG instantiation. The cleaning and
correction may include removing invalid or meaningless entries, adjusting data ﬁelds to
accommodate multiple values, ﬁxing inconsistencies, etc. This is a data-driven approach
for the KG model development (P , M).
 Task 2.1.3: Learn a kick-off semantic model exploiting algorithms over the pre-processed
data. This is a data-driven approach for the KG model development. Although this task
can be helpful in the schema deﬁnition process, it is not critical, and its results can be
covered by tasks 2.1.4, 2.1.5, 2.1.7 (P , O).
 Task 2.1.4: Reuse semantic models that may be either relevant to the domain of interest or
used/embedded by the identiﬁed sources. This task could include the analysis of different
data schemata of the sources and the import of ontologies, taxonomies, thesauri, etc.
(either parts of them or as a whole). The discovery of different semantic models relevant
to the domain of interest using libraries of models or ontology design patterns may
be performed in a systematic way, e.g., searching using key-terms and concepts that
have been identiﬁed during initial stages of work or during preliminary discussions with
experts. This is a schema-centric approach for the KG model development. This task is
fundamental for the semantic model development process, and it should be performed
if possible. However, it is considered optional in simplistic scenarios or cases where
the domain of interest has not undergone in-depth study, or when the existing semantic
models lack the necessary degree of semantic expressivity (S & P , O).
 Task 2.1.5: Consult generic top-level semantic models (e.g., DOLCE, WordNet, DBpedia
ontology), in order to better understand formal semantics of the domain of interest. This
is a schema-centric approach for the KG model development. This task is considered
optional as it could be covered by task 1.2.4 (P , O).
 Task 2.1.6: Consult the kick-off semantic model, in order to (i) identify key-terms and
concepts for the model and (ii) enrich the model under development. This task is optional
since it depends on tasks 1.2.3 (not critical) (P , O).
 Task 2.1.7: Specify and formalize the semantic model of the KG, in order to have a formal
representation of the KG conceptualization. A part of this process is to develop the mod-
ules and seamlessly interlink them within the semantic model to ensure a comprehensive
representation of the domain of interest. This may include either the engineering of the
model from scratch or reusing and engineering the imported semantic models, top-level
semantic models, and kick-off semantic models (P , M).
 Task 2.1.8: Merge and compare different versions of the semantic model of the KG, to
support its reuse and evolution. Especially in cases where the participants work in personal
and shared space for the development of the model, it is very important to compare and
merge the different versions that they have produced. This is set as optional, since it could
be performed in subsequent iterations of the process or not (not critical) (P , O).
 Task 2.1.9: Add documentation to the semantic model of the KG, with further comments,
examples, and speciﬁcation details which would make it more understandable to other
123

CHEKG: a collaborative and hybrid methodology… 4909
people. This task is recommended, but it is set as optional since it could be performed in
subsequent iterations of the process or not (not critical) (P , O).
 Task 2.1.10: Discuss the speciﬁed semantic model with domain experts, in order to verify
the modeling and designing choices and spot gaps and redundancy (S, M).
The process of developing the semantic model is already integrated in CHEKG methodol-
ogy; thus, there is no need to reuse an external OEM for this process. This integrated process
is based on ext-HCOME OEM.
Process 2.2. Create instance data of the KG. This process is further analyzed in the following
tasks:
 Task 2.2.1: Create instance data (KG’s data) via the semantic annotation of identiﬁed
sources, using the produced semantic model of the KG (e.g., RDFization of sources).
Particularly, CHEKG refers to the two main approaches to populate the KG with instance
data: (i) mapping structured, relational data (e.g., CSV ﬁles, databases) to the semantic
model of the KG using mapping languages/methods (e.g., RML, R2RML, SPARQLgen-
erate [44], RDF-Gen [ 45]) and (ii) extract data from unstructured sources (e.g., text ﬁles)
in an automatic manner using machine learning algorithms and the semantic model of
the KG (P , M).
 Task 2.2.2: V alidate produced data, in order to identify any modeling mistakes (e.g., using
RDF shapes with SHACL) (S & P , M).
 Task 2.2.3: Integrate data that are provided by different main data sources in order to be
represented with the semantic model of the KG. This task is mandatory in cases where
more than one data sources have been recognized and incorporated in the KG (P , M).
 Task 2.2.4: V alidate the produced KG against its design requirements. V alidation can
be performed by the exploitation of the KGs i.e., use KGs in practice/applications e.g.,
within speciﬁc analytics tasks or query formulation based on the CQs (S & P , M).
Process 2.3. Store, publish, query, and visualize the KG. This process is further analyzed in
the following tasks:
 Task 2.3.1: Set up the KG infrastructure in order to host the KG and build the relevant
services. This task includes the choice of the software/platform for the KG storage (e.g.,
Neo4j, OpenLink Virtuoso, RDFox), and the installation and conﬁguration of the software
according to the requirements of the KG and its usage (P , M).
 Task 2.3.2: Store the KG in the developed infrastructure (P , M).
 Task 2.3.3: Establish query/search interfaces for the stored KG, in order to provide (dis-
tributed) KG search services to multiple users, whether they are familiar with query
languages (e.g., SPARQL, Cypher) or not (P , M).
 Task 2.3.4: Establish visualization interfaces for the stored KG. It would be useful to
support users with visualization at both levels of knowledge, i.e., the model and data
level. These interfaces are useful for the evaluation and deployment tasks. Visualization
tasks are aligned with the project goals, resources, and deﬁned requirements. They can
also be performed in subsequent iterations (not critical) (P , O).
 Task 2.3.5: Publish KG in order to make it available to communities of interest and
practice which exceed the boundaries of the KG development team but are relevant to
the domain of interest. Ideally, these communities may share the same interests and
requirements which have been identiﬁed initially by the involved team. Publishing the
KG should be aligned with the project goals, restrictions, and deﬁned requirements. It
can also be performed in subsequent iterations (not critical) (P , O).
123

4910 S. Angelis et al.
3.3 KG evaluation and exploitation phase
The KG evaluation and exploitation phase completes the lifecycle of KG development, includ-
ing the evaluation of the KG, as well as its deployment and maintenance. Both the evaluation
and deployment of the KG may provide valuable feedback for the different processes of
the KG development phase and lead to the continuous reﬁnement of the KG in terms of
its schema, instance data, and infrastructure (including the various interfaces/tools provided
by the infrastructure). Advanced evaluation tasks as described in [ 46], related to accuracy,
coverage, coherency, and succinctness quality aspects, can be conducted to ensure the quality
of the created KG. In this phase, the tasks may be performed either individually or conver-
sationally, according to their nature. For example, the measurement of the KG performance
may be assigned to a speciﬁc member of the team, while the interpretation and improvement
of this measurement may be assigned to the whole team or to a subgroup. The recording of
individual or conversationally identiﬁed issues, comments, and propositions is considered
important since it enables the tracking of decisions and changes over different KG versions.
The KG evaluation and exploitation phase (Phase 3) includes:
Process 3.1. Evaluation of the quality of the KG, in terms of (i) correctness, (ii) complete-
ness, (iii) bias/fairness (e.g., in sensitive attributes like gender, race). This process is further
analyzed in the following tasks:
 Task 3.1.1: Browse the KG in order to review the most recent version of the KG (S & P ,
M).
 Task 3.1.2: Initiate arguments and criticism collaboratively in order to highlight mistakes
and propose solutions for the improvement of the KG. This task involves the members
of the team that have a clear perception of the KG content and usage, and thus they can
identify any deviations from the domain of interest and the requirements of the KG. This
task is set as optional since it can be performed in subsequent iterations of the process
(not critical) (S, O).
 Task 3.1.3: Use different metrics in order to measure the quality of KG. The range of
coverage, level of detail of the representation and inference possibilities of the KG model,
as well as the amount of included data and data sources (by the KG), are aspects that can
be measured. Those measurements will be a reference for the comparison of different
(even future) versions of the same KG, or different KGs which cover the same domain
of interest. This task is set as optional since it can be performed in subsequent iterations
of the process (not critical) (P , O).
 Task 3.1.4: Use the established CQs for the querying/testing of the KG in order to get
answers. The use of the CQs over the KG is a best practice for KG testing and discovery
of points for improvement. For instance, the whole process of query formulation and
answers’ retrieval could emerge issues of query complexity, content incompleteness, etc.
This task is recommended; however, it is set as optional since it depends on task 1.2.4.
(not critical) (P , O).
 Task 3.1.5: Compare different versions of the KGs and document the points of similarity
and difference. This task may create a useful development and maintenance history for
the KG. This task is set as optional since it can be performed in subsequent iterations of
the process (not critical) (S, O).
 Task 3.1.6: Manage recorded issues, exploiting tools for issues’ documentation and shar-
ing between the members of the development team. This task is set as optional since it
can be performed in subsequent iterations of the process (not critical) (S, O).
123

CHEKG: a collaborative and hybrid methodology… 4911
 Task 3.1.7: Propose new versions (both for the semantic model and the instance data) by
incorporating suggested changes. This task is set as optional since it can be performed
in subsequent iterations of the process (not critical) (S, O).
 Task 3.1.8: Deﬁne the sensitive attributes (e.g., gender, disability, religion, or ethnic-
ity/race), the sensitive values (e.g., female, blind, Christian, Asian), and the ﬁeld of
potential bias. This is an essential task for mitigating semantic bias of the KG. This task
could result to data sources that do not include any sensitive attributes (S, M).
 Task 3.1.9: Assess bias based on the deﬁned sensitive attributes, values, and general bias
ﬁeld. This task may be performed by analyzing or evaluating the contents of the KG,
keeping in mind the pre-deﬁned criteria of bias detection. This task could be omitted
only in cases when the data sources do not include any sensitive attributes, or in special
scenarios where the bias or the sensitive attributes are going to be studied in the scope of
the project (P , O).
Shared space tasks of process 3.1 can be performed by internal (organizational) stakehold-
ers and involved members of the KG engineering team, as well as by external stakeholders,
depending on the project goals, constraints, and deﬁned requirements.
Process 3.2. Cleaning of the KG to: (i) improve its correctness, (ii) mitigate bias. This process
is further analyzed in the following tasks:
 Task 3.2.1: Identify wrong assertions of the KG (P , M).
 Task 3.2.2: Correct wrong assertions of the KG (P , M).
 Task 3.2.3: Mitigate bias captured in the semantic model. This task could be omitted
only in cases when the data sources do not include any sensitive attributes, or in special
scenarios where the bias or the sensitive attributes are going to be studied in the scope of
the project (P , O).
 Task 3.2.4: Mitigate bias captured at the instance data. This task could be omitted only in
cases when the data sources do not include any sensitive attributes, or in special scenarios
where the bias or the sensitive attributes are going to be studied in the scope of the project
(P , O).
Process 3.3. Enriching the KG in order to improve the completeness of the KG by adding
new statements or improving existing statements. This process is further analyzed in the
following tasks:
 Task 3.3.1: Identify new relevant knowledge sources for the KG. The new sources must
meet the requirements that the core sources had met as well (S, O).
 Task 3.3.2: Apply methods for link discovery between the KG-related sources (P , O).
 Task 3.3.3: Integrate/merge/align the produced KG with other newly discovered KG
sources (P , O).
 Task 3.3.4: Detect and eliminate duplicates in the enriched KG (P , O).
 Task 3.3.5: Correct invalid property statements (e.g., domain/range violations) and/or
contradicting or uncertain attribute value resolution (in other words, having multiple
values for a unique property) (P , O).
All enrichment tasks (Process 3.3) are set as optional since they are aligned with the
project goals, resources, and deﬁned requirements. They can also be performed in subsequent
iterations (not critical).
Process 3.4. Deploy KG in order to provide services to the involved stakeholders and to the
public. This process is further analyzed in the following tasks:
123

4912 S. Angelis et al.
 Task 3.4.1: Use KG for the development of speciﬁc applications by exploiting the struc-
tured and processed data that constitute the KG. Such applications include (i) prediction
of facts, trends etc., (ii) recommendation of actions, things, etc., (iii) improved query
answering/searching, according to the needs of the domain experts or the community
that uses the KG after its public provision, (iv) data visualization (S & P , O).
 Task 3.4.2: Use KG in order to align/merge other relevant KGs for the domain of interest.
This task is relevant to KG’s alignment/integration/merging of task 3.3.3, though it entails
the provision (design and development) of tools and interfaces for users who are not
specialized in the performance of those tasks programmatically. The KG in this case is
the base for the development of the tool/service (S & P , O).
All deployment tasks (Process 3.4) are set as optional since they are aligned with the
project goals, resources, and deﬁned requirements. They can also be performed in subsequent
iterations (not critical).
Process 3.5. Specify maintenance procedures of the KG. This process is further analyzed in
the following tasks:
 Task 3.5.1: Specify the maintenance procedure of the KG, in order to continuously
update/reﬁne both the schema and the data from the different sources (S, O).
 Task 3.5.2: Specify the monitoring procedure of the KG in order to ensure maintenance
of high-quality data of the KG (S, O).
All maintenance tasks are highly recommended, and they are set as optional since they
are aligned with the project goals, resources, and deﬁned requirements. They can also be
performed in subsequent iterations (not critical).
4 Evaluating CHEKG methodology
Motivated by use cases related to drones’ mission for the documentation (with photos) of spe-
ciﬁc regions and points of interest, we have developed a KG-based approach for transforming
trajectories of UA V drones into semantic trajectories (Semantic Trajectory as KG—STaKG)
[28]. The semantic trajectories (ST) can be effectively managed, visualized, and analyzed as
knowledge graphs using a KG-driven custom-designed toolset. The CHEKG methodology
has been applied for the development of STaKGs and the underlying model. The phases of
the methodology were adapted and extended by special engineering tasks in order to support
the STaKG development.
4.1 Applying the KG specification phase
Based on CHEKG methodology, the involved members of the team were identiﬁed and the
members’ roles were ﬁrst speciﬁed (Task 1.1.1 and Task 1.1.2). The team included six mem-
bers: two experts in the ﬁeld of cartography and geoinformatics, one expert in the ﬁeld of
geoinformatics and software engineering, two ontology engineers and one ontology and soft-
ware engineer. All members were involved in more than one working group. Particularly,
cartography and geoinformatics experts (three members) aimed at the understanding of the
domain of interest, provided the main part of the data which constitute the STaKG, established
the requirements, and evaluated all the stages and results of design and implementation of
the KG. The ontology/knowledge engineers (three members) focused on the design, imple-
mentation, and evaluation of the knowledge model, as well as the instantiation of the model
123

CHEKG: a collaborative and hybrid methodology… 4913
with data and eventually the formation of the STaKG. Finally, the knowledge workers (two
members) focused on the management of the KG and the design of the tools and services
regarding its exploitation and maintenance. The members worked both collaboratively (e.g.,
shared cloud workspace, Git repositories, WebProtégé, and e-mails) and individually with
local documents and tools (Protégé 5.5 and Neo4j).
Afterward, the speciﬁcation of the aim and scope of the KG followed (Task 1.2.1). In
the context of the same CHEKG process (Process 1.2) the data sources (namely, the drones’
log ﬁles, information systems that the experts use for the documentation of drone ﬂights,
sites, metadata of image ﬁles) were identiﬁed in collaboration with the domain experts (Task
1.2.2). Also, a set of requirements that the semantic model under development, as well as
the KG that integrates it, should satisfy, have been deﬁned (Task 1.2.3). The deﬁnition of the
requirements has been conducted in collaboration with experts of the domain of interest, and
they constitute “points of assessment” for the development and performance of the model
and the KG. Finally, the ontology/knowledge engineers and domain experts formulated a set
of CQs to be answered against the KG (Task 1.2.4). The speciﬁcations and CQs deﬁned in
processes 1.1 and 1.2 were documented by the working group for future reference (Task 1.2.5).
The process involved interviews with experts in UA V-based documentation and cultural
heritage site documentation to gather essential information and knowledge for developing
the ontological model and the toolset. This collaborative effort led to the creation of multiple
competency questions that engaged all stakeholders. A list of the CQs that were used to
evaluate the developed toolset is provided below:
 Which trajectories of a speciﬁc mission include records of a speciﬁc object?
 Which recording positions include records of a speciﬁc object?
 What kind of records are produced during a speciﬁc mission?
 Which missions result in photograph records?
 What are the recording positions of a speciﬁc ﬂight?
 What kind of records are produced at a speciﬁc recording position?
 What are the recording segments of a trajectory?
 What are the weather conditions at a speciﬁc point in time for a speciﬁc ﬂight?
 Which ﬂights intersect?
 What is the number of drones involved in a speciﬁc mission and the number of ﬂights
initiated for that mission?
 What recording events occurred at a distance of less than 100 m from a speciﬁc recording
event?
 Which recording events took place near a speciﬁc POI?
The thorough presentation of the deﬁned CQs is included in Kotis et al. [ 28]
4.2 Applying the KG development phase
At the second phase of CHEKG methodology, during the development of the semantic model,
multiple discussions with the domain experts were conducted, to clarify the aspects of the
domain of interest and establish a common vocabulary related to the conceptualization that
must be developed (Task 2.1.1). Additionally, the data categories which should be correlated
and enriched, and eventually supply the KG based on the case study have been determined.
The domain experts provided example datasets of the data categories in order to analyze
and clean them for further use in the following process. The information extraction process
commenced with a physical meeting with the domain experts and the presentation of a) the
problem as they view it, b) the data sources that included log ﬁles, shapeﬁles, and image
123

4914 S. Angelis et al.
records. Collaborative work was conducted, including discussion to determine the relevant
properties and attributes of the data to be extracted for the KG development. Subsequently,
the extraction of data from log and image ﬁles was programmatically carried out through
specialized scripts. The information stored in shapeﬁles was converted to RDF format, and
during the enrichment phase they were retrieved using SPARQL Geospatial queries (Task
2.1.2). In the same context, existing models were identiﬁed and studied in order to be reused
in the semantic model of the KG (Task 2.1.4). The selection of the models was based on our
previous experience in related projects as well as searching ontology repositories (LOV [ 47]
and ODP [ 48]) for related terms such as trajectory, drone, weather, digitization, recording,
record.
Considering the speciﬁcations, data analysis, and semantic models research, ontol-
ogy/knowledge engineers worked on the development of a formal semantic model for the
domain of interest, which will constitute the backbone of the KG (Task 2.1.7). The semantic
model (Onto4drone [ 49]) was developed following the HCOME collaborative engineering
methodology, supported by Protégé 5.5, and WebProtégé tools. In addition, shared cloud
workspaces have been used for further collaborative engineering tasks. It is directly based on
the datAcron ontology [ 45] and indirectly on the DUL, SKOS, SOSA/SSN, SF, GML, and
GeoSPARQL ontologies. Additionally, related documentation was added to the developed
semantic model (Task 2.1.9), while the result was discussed with the experts i.e., geographers
(Task 2.1.10).
As part of the evaluation of the engineered model, as well as for the creation of instance
data for the KG the ontology was populated with individuals (Task 2.2.1 and Task 2.2.3). The
individuals were part of the data that would constitute the content of the KG, as they have been
identiﬁed (Task 1.2.2) and gathered (Task 2.1.2) in previous tasks of the work. Additionally, a
set of SHACL rules [ 50] were formulated to evaluate the individuals (Task 2.2.2). Regarding
SHACL validation and constraint rule formulation, the Protégé plugin SHACL4Protege [ 51]
was used. Furthermore, for the evaluation of the model and the instance data in this initial
stage, the CQs transformed into SPARQL queries via Protégé plugin Snap SPARQL [ 52]
(Task 2.2.4). In the same context, the positions of the UA V were summarized, and only
one position was retained per second out of thirty positions per second that were originally
tracked (Task 2.2.4). This step effectively reduced the number of positions while maintaining
a representative sample of the trajectory of the ﬂight.
Regarding data storage, publishing, retrieval, and visualization, several actions were taken
(Phase 2, Process 2.3). The ﬁrst step was to import the developed ontology into Neo4j using
the Neosemantics add-on [ 53] (Task 2.3.1). Subsequently, the ﬂights’ data, from CSV ﬁles,
were stored in the graph using Cypher queries and built-in functions (Task 2.3.2). The entities
and properties deﬁned in the ontology were used as labels and properties. Additionally, new
data from the analysis and enrichment process were also stored in the graph, following the
entities, properties, and relations of the ontology.
To facilitate analysis and visualization, the data from the KG were retrieved through
manually or automatically generated Cypher queries (Task 2.3.3 and Task 2.3.4). The repre-
sentation and visualization are achieved through several methods. Spatiotemporal data can
be displayed in a tabular form or as points on a map. The records can be represented by the
ﬁle name, the resource URL, or by displaying the actual record. Furthermore, all data can be
visualized as a connected directed graph, allowing for a deeper understanding of the relation-
ships between entities and properties. The source code of developed application that exploits
the KG can be found in Github ( https://github.com/sotirisAng/stakg) and a live demo can be
found at http://stakg-ct-linkdata.aegean.gr .
123

CHEKG: a collaborative and hybrid methodology… 4915
4.3 Applying the KG evaluation and exploitation phase
The third phase of CHEKG methodology started with the evaluation of the quality of the
developed KG (Phase 3, Process 3.1). At this point, the ﬁrst version of the KG was inspected
and discussed in collaboration with the domain experts (Task 3.1.1 and Task 3.1.2). The
chosen data sources and respective data have been employed, forming a KG of more than 7K
nodes and 10K relations, which derive from the four UA V ﬂight logﬁles and enrichment data.
The KG was explored and evaluated, in terms of its correctness and completeness, through
the set of CQs that experts had provided at the ﬁrst phase of the development (Task 3.1.1 and
Task 3.1.4). The retrievals indicated a few mistakes or omissions regarding the included data,
which constituted points for further improvement/reﬁnement. Also, based on the study of the
domain of interest of our case (documenting CH POIs recorded from UA Vs ﬂights/missions)
and the related data, it was concluded that sensitive attributes that could introduce obvious
bias were not present (Task 3.1.8).
Moreover, the cleaning process was conducted, in order to ensure that the KG is accurate,
consistent, and informative (Phase 3, Process 3.2). Firstly, all temporal data in the log ﬁles for
the UA V ﬂights and records were converted to UTC format to maintain consistency across the
data (Task 3.2.1 and Task 3.2.2). To eliminate duplicates, targeted queries were performed
on the graph to identify entities such as records or positions that share identical attributes
and subsequently removed them (Task 3.2.1 and Task 3.2.2). Records that did not match a
position that was part of a trajectory were excluded, as well as records that lacked location
or temporal data (Task 3.2.2). Moreover, positions from the trajectory that had temporal
features beyond the timeframe of the ﬂight were removed to ensure that only relevant data
were included in the KG (Task 3.2.2).
The KG enrichment process (Phase 3, Process 3.3) involved tasks that aim to improve the
completeness of the knowledge graph. One of these tasks was the retrieval of weather data for
the speciﬁc area and time range of each drone ﬂight and correlating them to the trajectories
(Task 3.3.1 and Task 3.3.3). For this task the Historical Weather API [ 54] was utilized to fetch
weather data by sending requests to the API and creating WeatherCondition nodes based on
the responses. The created nodes were then connected to trajectory positions in the KG.
Another task included in the KG enrichment phase (Task 3.3.1 and Task 3.3.3) was to extract
record metadata, which includes geolocation, timestamp, and ﬁle name, from the records that
are produced during the drone ﬂights. This metadata was then used to deﬁne recording events
that produce the records. In the enrichment process, external APIs were also utilized to obtain
information about points of interest (POIs) documented in OpenStreetMaps [ 55]o rU n i v e r s i t y
of the Aegean geographical LOD datasets [ 56], which might have been recorded during
drone ﬂights. This was achieved by the development of methods that form Overpass [ 57]a n d
SPARQL queries for each record stored in the KG, based on information retrieved from the
records. Requests were then sent to the external APIs to execute these queries. This approach
enabled the identiﬁcation of documented POIs located near the drone’s location when the
record was produced. This information was then used to merge POI nodes in the knowledge
graph and relate them to record nodes. Having developed the ﬁrst version of the KG, the work
focused on the deployment (Task 3.4.1) and speciﬁcally on the development and use of a
toolset which includes tools for raw trajectory data cleaning, summarization and RDFization,
enrichment, semantic trajectory management, and ST browsing and visualization.
The toolset enables the management and retrieval of STaKGs, enrichment of STaKGs,
and analysis to recognize semantic behaviors. The raw archive data, which included drone
ﬂights’ log ﬁles, metadata of recordings, and shapeﬁles of geographical regions, were semi-
automatically annotated by programmatically developed methods, to entities, attributes, and
123

4916 S. Angelis et al.
relations based on the Onto4drone ontology. These annotated data were then utilized along-
side external open data such as weather data and POIs for the creation and enrichment of STs.
The annotation and enrichment processes were based on the ST model, and enriched STs
were stored in the Neo4j graph database as a KG. The ST management tool used STaKGs
to create trajectory segmentations and perform analytics and tasks, such as merge, split, and
combination of trajectories. The web tool for visualization and ST browsing fetched analytics
results and STaKG data stored in the KG through predeﬁned and customizable queries to
efﬁciently present them to users who are not specialized in performing those tasks.
Finally, a set of KG maintenance procedures was speciﬁed (Task 3.5.1). It includes per-
forming regular enrichment tasks, which involve adding new data to the KG to ensure that it
reﬂects the latest information available. Another maintenance procedure is performing reg-
ular cleaning tasks that involve identifying and removing inconsistencies and errors. These
tasks follow the enrichment and cleaning processes that are described earlier and are per-
formed to ensure that the KG remains clean and accurate. In addition to them, maintenance
procedures for KGs involve updating the KG to align with changes made to the knowledge
model/ontology used to structure it (Task 3.5.2). This was achieved through query-based
updates and checks of entities, attributes, and relations in the KG, enabling the discovery
and elimination of inconsistencies and ensuring that the KG accurately reﬂects the domain
of interest.
5 Discussion and limitations
CHEKG is based on the phases of the ext-HCOME as it supports the decisive involvement of
domain experts and knowledge workers (along with knowledge engineers), and it requires the
use of tools that facilitate the collaborative management and interaction with conceptualiza-
tions in a direct and iterative way, as well as its modularization and bias-assessment/mitigation
tasks. When adapting the ext-HCOME for KG engineering, the speciﬁcation, and conceptual-
ization phases, processes and tasks exhibited an organic and straightforward correspondence.
Conversely, certain more specialized tasks involving the actual implementation and utiliza-
tion of the KG, presented challenges during adaptation and organization into processes and
phases, mostly to ensure a comprehensive approach that addresses the diverse aspects of
the KG engineering process and KG exploitation. Such tasks included the KG infrastructure
development, the creation of interfaces and visualizations for KGs, contextual application
descriptions, iterative enrichment, evaluation, and maintenance of KGs.
CHEKG is based on two main advances:
(a) Human-centered and collaborative engineering: CHEKG recognizes the impor-
tance of human expertise and domain knowledge in KG development. It emphasizes the
active/decisive participation of domain experts and knowledge workers, enabling them to
contribute their specialized knowledge and context throughout the process. It provides a sys-
tematic and structured approach for involving stakeholders with different levels of expertise
and knowledge. Furthermore, it provides personal and shared spaces that facilitate individual
and collaborative tasks within the KG development process. These spaces enable domain
experts, knowledge workers, and knowledge engineers to work closely together, share their
expertise, and iterate on the KG design and content.
(b) Domain-speciﬁc specialized tasks and roles: CHEKG recognizes the need for involving
domain experts, knowledge engineers, and other stakeholders with speciﬁc domain expertise
throughout the KG development lifecycle. It deﬁnes specialized tasks and roles to ensure
123

CHEKG: a collaborative and hybrid methodology… 4917
that the domain-speciﬁc knowledge and requirements are adequately incorporated into the
KG. This involvement helps in achieving a more accurate and comprehensive representation
of the domain. Moreover, it focuses on the development of fair domain-speciﬁc KGs, as it
considers the aspects of bias and fairness in KG development.
Existing SotA guidelines and/or methodologies present similarities and correspondences
regarding the processes/tasks that must be followed for KG development. The identiﬁcation
of this kind of correspondence for each guideline or methodology has been studied and
taken into account for the development of the phases, processes, and tasks of the CHEKG.
A mapping of CHEKG phases and existing methodologies is presented in Table 1.
CHEKG is derived from OEMs and integrates speciﬁc tasks of ext-HCOME. Phases and
processes in CHEKG can also be aligned with those presented in other OEMs. Table 2
provides a mapping of these phases to corresponding ones in collaborative and agile OEMs.
As emerges from Table 1, CHEKG is drawing parallels with other described methodolo-
gies. The detailed and extensive description of the overall KG development process by Fensel
et al. [ 29] and Tamašauskait˙e[ 37] aligns with CHEKG’s systematic structuring. However,
these approaches are not necessarily collaborative, and the involved actors are not explicitly
described. [39] outlines members of the data ecosystem and emphasizes the role of a knowl-
edge scientist who aims to answer business questions through data exploitation. The XD
methodology applied in [ 23] highlights a collaborative and iterative approach for building
KGs, utilizing competency questions. These aspects are also included in CHEKG, which
emphasizes on team speciﬁcation and aim deﬁnition along the development and mainte-
nance processes. CHEKG’s alignment with these methodologies showcases its agility and
applicability across diverse KG engineering scenarios.
Concerning the fairness and bias mitigation process of the KG, detailed information is
missing from the KG methodologies compared to CHEKG. [ 39]a n d[ 36] do not address
this issue, [ 28] states the importance of unbiased data for trustworthiness, and [ 23] notes
that the requirement collection was deliberately template-free and unstructured to prevent
bias in the outcome. [ 23] is the only related work that provides comprehensive coverage of
modularity, which adheres to the root-thematic-foundations architectural pattern to construct
the ontology underlying the KG. CHEKG highlights the aspect of bias and fairness in tasks
3.1.8, 3.1.9, 3.2.3 and 3.2.4 and the importance of modularity in the creation of explicit
knowledge process, particularly in tasks 2.1.1. and 2.1.7.
CHEKG methodology was ﬁrstly introduced in our preliminary work presented in [ 25]a s
STaKG methodology (a predecessor of CHEKG focusing on the engineering of semantic tra-
jectories as knowledge graphs). In the recent work [ 28], the focus is on the implementation of
a domain-speciﬁc application, where STaKG methodology was used for the methodological
part of engineering ST as KGs. CHEKG aims to provide a generic methodological approach
for KG engineering that can be applied across various domains, without relating the engi-
neering of KGs with the engineering of STs only or being tied exclusively to a speciﬁc ﬁeld.
CHEKG methodology has been eventually shaped in its latest form by taking into consid-
eration our experience on the entire KG engineering process. It is worth clarifying that a
STaKG (a ST represented as a KG) is the output of STaKG methodology, whereas the output
of CHEKG methodology can be any type of a KG, including also a STaKG.
The developed KG and the functionalities for its exploitation were able to effectively
address the CQs and generate visualizations, as well as to enrich the data by linking them to
external sources, as described in Sect. 4.3. The domain experts, who also acted as the end-
users of the developed applications, veriﬁed the accuracy and practicality of the KG’s content,
the correctness of CQs answering, and the efﬁciency of the visualizations. Furthermore, the
KG was published with four showcase datasets, but it requires further expansion with new
123

4918 S. Angelis et al.
Table 1 Mapping of CHEKG phases to existing methodologies
[29][ 39][ 23][ 37] CHEKG
Knowledge creation Knowledge capture Requirement engineering, compe-
tency questions (CQs)
Identify data KG speciﬁcation (the speciﬁcation of
the involved team, the speciﬁcation of
aim, scope, and requirements of the
KG)
Knowledge creation Knowledge implementation Competency questions (CQs), Match-
ing CQs to ontology design patterns
(ODPs)
Construct the knowledge graph ontol-
ogy, knowledge extraction, process
knowledge
KG development (creation of explicit
knowledge, create instance data of the
KG, store, publish, query, and visual-
ize the KG)
Knowledge cre-
ation, knowledge
hosting
Knowledge access Testing and integration Construct the knowledge graph, pro-
cess knowledge
KG development (creation of explicit
knowledge, create instance data of the
KG, store, publish, query, and visual-
ize the KG)
Knowledge curation Knowledge implementation Evaluation Maintain the KG KG evaluation and exploitation (eval-
uation of the quality of the KG, clean-
ing of the KG, enriching the KG,
deploy KG, specify maintenance pro-
cedures)
123

CHEKG: a collaborative and hybrid methodology… 4919
Table 2 Mapping of CHEKG phases to OEMs
[21][ 20][ 22] CHEKG
Identifying terminology, deﬁning a
glossary
OE collects all information about a
speciﬁc domain, builds a model for-
malizing the domain
Analysis and conceptualization KG speciﬁcation (the speciﬁcation of
the involved team, the speciﬁcation of
aim, scope, and requirements of the
KG)
Generating a concept taxonomy, Con-
necting entities, deﬁning parthood,
and developing the ontology
OE merges the model with the current
model, updates test cases
Development and test KG development (creation of explicit
knowledge, create instance data of the
KG, store, publish, query, and visual-
ize the KG)
OE refactors the current model,
focuses on the last part added
Ontology use and updating KG evaluation and exploitation (eval-
uation of the quality of the KG, clean-
ing of the KG, enriching the KG,
deploy KG, specify maintenance pro-
cedures)
123

4920 S. Angelis et al.
datasets to examine and validate possible performance and scalability issues. In addition,
extra documentation could be added to the semantic model to make it more understandable
and reusable.
In the context of the deployment of the methodology, it was noticed that there were a
few optional tasks which were i) skipped and ii) applied in a slightly different order. Firstly,
the tasks related to bias were omitted for the STaKG development. The domain of interest
of our case study (trajectories of UA Vs and CH documentation) does not involve sensitive
attributes that could introduce obvious bias. However, in future work we will involve experts
and conduct proper bias analysis and evaluation. Secondly, some optional tasks were not
completed in the proposed order, but they were eventually executed after the development of
the exploitation tools. For instance, the enrichment, cleaning, and visualization tasks were
performed after the deployment phase due to the availability of the developed tools.
The overall execution time of the project is dependent on the availability of members of
the involved team and the project’s time frame. It required approx. 10 man-months for the ﬁrst
iteration and an additional 4 man-months for the second iteration (less than 50 percent of the
initial effort). Team members, expressed positive feedback, highlighting the systematic way
of work, guided by deﬁned processes and goals. Notably, during the evaluation of CHEKG, it
became evident that various team members could negotiate to get the role of the coordinator.
While the methodology does not explicitly mention this role, it proves essential, since the team
member undertaking this responsibility organizes the frequency, duration, and objectives of
meetings, as well as orchestrates the communication pace for different processes and tasks
within the team.
CHEKG currently does not provide a comprehensive proposal for tools or techniques
speciﬁcally tailored for merging KGs. This aspect could be a valuable area for future research
and development within the CHEKG framework, exploring effective strategies for aligning
and merging KGs.
Although the engineering tasks rely on collaborative tools like Git repositories, cloud-
based collaborative workspaces, and engineering tools such as WebProtege, CHEKG
currently lacks dedicated tools to actively engage the involved stakeholders in the engi-
neering process. A prospective goal could involve the creation of a specialized toolset to
support the methodology, designed to streamline and enhance the efﬁciency of the overall
engineering process.
Considering the assessment of CHEKG, as described in Sect. 4, it is based on a real-world
use case scenario. However, to further reﬁne and augment the precision of feedback and to
ensure a thorough assessment that extends beyond the immediate practical application, our
future objectives include a more formalized approach of the evaluation process. This entails
the adoption of a proposed evaluation framework, following the paradigm and mirroring the
parameters outlined in related work [ 24], which could serve as a benchmark for measuring
the validity, efﬁciency, and efﬁcacy of the methodology.
Finally, as was noticed during the use of the methodology, CHEKG provides a collab-
orative way of working, which could be challenging in some cases, for instance, if the
development of the KG involves a single knowledge engineer, or in the case of developing per-
sonal KGs. However, even in these cases, the methodology has a ﬂexible structure regarding
the tasks that must be followed, allowing the simpliﬁcation of the required processes.
123

CHEKG: a collaborative and hybrid methodology… 4921
6 Conclusion and future directions
The role and speciﬁc activities followed by the involved team lack detailed description and
have not been emphasized in methodological phases and steps. The methodology presented
in this paper, namely CHEKG, attempts to ﬁll the aforementioned gaps, following OEM
principles, and the main phases of ext-HCOME OE methodology. CHEKG contributes to
all phases of the KG engineering lifecycle; it incorporates all the different KG development
tasks and organizes them in unambiguous phases, clarifying the roles of the involved mem-
bers of the development team, exploiting their specialized knowledge in conceptualization,
data/knowledge acquisition, KG deployment, and KG evaluation.
So far, CHEKG has been exploited for the development of KGs for the representation of
semantic trajectories (STaKG) of drones. The results highlight the feasibility of the method-
ology, since the team was efﬁciently organized, and the tasks were ﬂuently conducted. The
semantic model, the KG, and the tools developed were positively evaluated by the domain
experts who followed the whole process.
Future work includes the usage of the methodology in different domains. Furthermore,
the exploitation in the context of different use cases may include working teams with more or
less members of varying backgrounds, giving more insights about the efﬁciency and potential
limitations of the methodology in different structures of teams.
Author Contributions SA and EM conducted research, literature review and wrote the main manuscript text;
KK has supervised the theoretical work on CHEKG as well as the implementation and evaluation phases
of the methodology during a related nationally funded research project (see Funding Declaration); KK and
GC supervised overall research, reviewed, and edited the manuscript and provided valuable feedback on the
content.
Funding Open access funding provided by HEAL-Link Greece. This research was funded by the Research
e-Infrastructure [e-Aegean R&D Network], Code Number MIS 5046494, which is implemented within the
framework of the “Regional Excellence” Action of the Operational Program “Competitiveness, Entrepreneur-
ship and Innovation.” The action was co-funded by the European Regional Development Fund (ERDF) and
the Greek State [Partnership and Cooperation Agreement 2014–2020].
Declarations
Conﬂict of interest The authors have no conﬂict of interest, or other interests that might be perceived to
inﬂuence the results and/or discussion reported in this paper.
Open Access This article is licensed under a Creative Commons Attribution 4.0 International License, which
permits use, sharing, adaptation, distribution and reproduction in any medium or format, as long as you give
appropriate credit to the original author(s) and the source, provide a link to the Creative Commons licence,
and indicate if changes were made. The images or other third party material in this article are included in the
article’s Creative Commons licence, unless indicated otherwise in a credit line to the material. If material is
not included in the article’s Creative Commons licence and your intended use is not permitted by statutory
regulation or exceeds the permitted use, you will need to obtain permission directly from the copyright holder.
To view a copy of this licence, visit http://creativecommons.org/licenses/by/4.0/ .
References
1. Ehrlinger L, Wöß W (2016) Towards a deﬁnition of knowledge graphs
2. Paulheim H (2017) Knowledge graph reﬁnement: a survey of approaches and evaluation methods. Semant
Web 8(3):489–508
3. Kejriwal M (2019) What is a knowledge graph? SpringerBriefs in Computer Science, pp 1–7 https://doi.
org/10.1007/978-3-030-12375-8_1/COVER
123

4922 S. Angelis et al.
4. Gomez-Perez JM, Pan JZ, V etere G, Wu H (2017) Enterprise knowledge graph: an introduction. Exploiting
linked data and knowledge graphs in large organisations, pp 1–14, https://doi.org/10.1007/978-3-319-
45654-6_1/COVER
5. Neo4j Graph Data Platform | Graph Database Management System. https://neo4j.com/
6. OpenLink Software: Virtuoso Homepage. https://virtuoso.openlinksw.com/
7. RDFox, The High Performance Knowledge Graph and Reasoner. https://www.oxfordsemantic.tech/
product
8. DBPedia Ontology. https://dbpedia.org/ontology/
9. Wikidata:WikiProject Ontology/Modelling. https://www.wikidata.org/wiki/Wikidata:WikiProject_
Ontology/Modelling
10. Suchanek FM, Kasneci G, Weikum G (2008) Yago: a large ontology from wikipedia and wordnet. J Web
Semant 6(3):203–217. https://doi.org/10.1016/j.websem.2008.06.001
11. Schema.org. https://schema.org/
12. Uschold M, King M (1995) Towards a methodology for building ontologies. https://citeseerx.ist.psu.edu/
document?repid=rep1&type=pdf&doi=98304f357fb8e75aa37e5b754e905dcb94570202
13. Pinto HS, Staab S, Tempich C (2004) Diligent: towards a ﬁne-grained methodology for distributed,
loosely-controlled and evolving engineering of ontologies. Front Artif Intell Appl 110
14. López M F, Gómez-Pérez A, Sierra J P , Sierra A P (1999) Building a chemical ontology using methon-
tology and the ontology design environment. IEEE Intell Syst 14:37–46. https://doi.org/10.1109/5254.
747904
15. Kotis K, V ouros GA (2006) Human-centered ontology engineering: the hcome methodology. Knowl Inf
Syst 10:109–131. https://doi.org/10.1007/S10115-005-0227-4/METRICS
16. Presutti V , Daga E, Gangemi A, Blomqvist E (2009) extreme design with content ontology design patterns.
In: Proceedings of the workshop on ontology patterns, pp 83–97
17. Suárez-Figueroa MC, Gómez-Pérez A, Fernández-López M (2012) The neon methodology for ontology
engineering. Ontology Engineering in a Networked World, pp 9–34, https://doi.org/10.1007/978-3-642-
24794-1_2/COVER
18. Sure Y (2017) A tool-supported methodology for ontology-based knowledge management. The Ontology
and Modelling of Real Estate Transactions, pp 115–126, https://doi.org/10.4324/9781315237978-8
19. Kotis KI, V ouros GA, Spiliotopoulos D (2020) Ontology engineering methodologies for the evolution of
living and reused ontologies: status, trends, ﬁndings and recommendations. Knowl Eng Rev 35:4. https://
doi.org/10.1017/S0269888920000065
20. Peroni S (2016) Samod: an agile methodology for the development of ontologies, pp 1–14, https://doi.
org/10.6084/m9.ﬁgshare.3189769.v4
21. De Nicola A, Missikoff M (2016) A lightweight methodology for rapid ontology engineering. Commun
ACM 59:79–86. https://doi.org/10.1145/2818359
22. Spoladore D, Pessot E, Trombetta A (2023) A novel agile ontology engineering methodology for sup-
porting organizations in collaborative ontology development. Comput Ind 151:103979. https://doi.org/
10.1016/j.compind.2023.103979
23. Carriero V A, Gangemi A, Mancinelli ML, Nuzzolese AG, Presutti V , V eninata C (2021) Pattern-based
design applied to cultural heritage knowledge graphs. Semant Web 12:313–357. https://doi.org/10.3233/
SW-200422
24. Spoladore D, Pessot E (2022) An evaluation of agile ontology engineering methodologies for the digital
transformation of companies. Comput Ind 140:103690. https://doi.org/10.1016/j.compind.2022.103690
25. Moraitou E, Angelis S, Kotis K, Caridakis G, Papadopoulou E-E, Soulakellis N (2022) Towards engineer-
ing drones semantic trajectories as knowledge graphs. In: Proceedings of the 5th international workshop
on geospatial linked data (GeoLD 2022), Co-Located with the 19th European Semantic Web Conference
(ESWC 2022) 3157
26. Paparidis E, Kotis K (2021) Towards engineering fair ontologies: unbiasing a surveillance ontology. In:
Proceedings of the 2021 IEEE international conference on progress in informatics and computing, PIC
2021, 226–231, https://doi.org/10.1109/PIC53636.2021.9687030
27. Blomqvist E, Gangemi A, Presutti V (2009) Experiments on pattern-based ontology design. In: Proceed-
ings of the ﬁfth international conference on knowledge capture. K-CAP ’09, pp 41–48. Association for
Computing Machinery, New Y ork, NY , USA. https://doi.org/10.1145/1597735.1597743
28. Kotis K, Angelis S, Moraitou E, Kopsachilis V , Papadopoulou EE, Soulakellis N, V aitis M (2023) A kg-
based integrated uav approach for engineering semantic trajectories in the cultural heritage documentation
domain. Remote Sensing 2023, V ol 15, p 821 15, https://doi.org/10.3390/RS15030821
29. Fensel D, Simsek U, Angele K, Huaman E, Kärle E, Panasiuk O, Toma I, Umbrich J, Wahler A (2020).
Knowledge graphs. https://doi.org/10.1007/978-3-030-37439-6
123

CHEKG: a collaborative and hybrid methodology… 4923
30. Tang X, Feng Z, Xiao Y , Wang M, Ye T, Zhou Y , Meng J, Zhang B, Zhang D (2023) Construction
and application of an ontology-based domain-speciﬁc knowledge graph for petroleum exploration and
development. Geosci Front 14(5):101426. https://doi.org/10.1016/j.gsf.2022.101426
31. Lyu K, Tian Y , Shang Y , Zhou T, Yang Z, Liu Q, Yao X, Zhang P , Chen J, Li J (2023) Causal knowledge
graph construction and evaluation for clinical decision support of diabetic nephropathy. J Biomed Inform
139:104298. https://doi.org/10.1016/j.jbi.2023.104298
32. Daowd A, Barrett M, Abidi S, Abidi SSR (2021) A framework to build a causal knowledge graph for
chronic diseases and cancers by discovering semantic associations from biomedical literature, pp 13–22
https://doi.org/10.1109/ICHI52183.2021.00016
33. Ma X (2022) Knowledge graph construction and application in geosciences: A review. Comput Geosci
161:105082. https://doi.org/10.1016/j.cageo.2022.105082
34. Chessa A, Fenu G, Motta E, Osborne F, Reforgiato Recupero D, Salatino A, Secchi L (2023) Data-driven
methodology for knowledge graph generation within the tourism domain. IEEE Access 11:67567–67599.
https://doi.org/10.1109/ACCESS.2023.3292153
35. Dessì D, Osborne F, Reforgiato Recupero D, Buscaldi D, Motta E (2021) Generating knowledge graphs
by employing natural language processing and machine learning techniques within the scholarly domain.
Future Gener Comput Syst 116:253–264. https://doi.org/10.1016/j.future.2020.10.026
36. Peng Z, Song H, Zheng X, Yi L (2020) Construction of hierarchical knowledge graph based on deep
learning, pp 302–308, https://doi.org/10.1109/ICAICA50127.2020.9181920
37. Tamašauskait E, Groth P (2023) Deﬁning a knowledge graph development process through a systematic
review. ACM Trans Softw Eng Methodol. https://doi.org/10.1145/3522586
38. Agrawal G, Deng Y , Park J, Liu H (2022) Chen YC (2022) Building knowledge graphs from unstructured
texts: applications and impact analyses in cybersecurity education. Information 13:526. https://doi.org/
10.3390/INFO13110526
39. Sequeda J, Lassila O (2021) Designing and building enterprise knowledge graphs. https://doi.org/10.
1007/978-3-031-01916-6
40. Kotis K, Papasalouros A (2010) Learning useful kick-off ontologies from query logs: Hcome revised. In:
CISIS 2010 - The 4th international conference on complex, intelligent and software intensive systems,
pp 345–351, https://doi.org/10.1109/CISIS.2010.50
41. Kotis K, Papasalouros A, V ouros G, Pappas N, Zoumpatianos K (2011) Enhancing the collective knowl-
edge for the engineering of ontologies in open and socially constructed learning spaces. J Univ Comput
Sci 17:1710–1742
42. Musen MA (2015) Protégé team: the protégé project: a look back and a look forward. AI Matters 1:4.
https://doi.org/10.1145/2757001.2757003
43. Suárez-Figueroa MC, Gómez-Pérez A, Villazón-Terrazas B (2009) How to write and use the ontol-
ogy requirements speciﬁcation document. In: Meersman R, Dillon T, Herrero P (eds) On the move to
meaningful internet systems: OTM 2009. Springer, Berlin, Heidelberg, pp 966–982
44. SPARQL-Generate. https://ci.mines-stetienne.fr/sparql-generate/
45. Santipantakis GM, V ouros GA, Kotis KI, Doulkeridis C (2018) Rdf-gen: generating rdf from streaming
and archival data. ACM Int Conf Proc Ser. https://doi.org/10.1145/3227609.3227658
46. Knowledge graphs (2022) https://doi.org/10.1007/978-3-031-01918-0
47. Linked Open V ocabularies. https://lov.linkeddata.es/dataset/lov
48. Ontology Design Patterns.org (ODP) - Odp. http://ontologydesignpatterns.org/wiki/Main_Page
49. GitHub - KotisK/onto4drone: An ontology for representing knowledge related to drones and their semantic
trajectories. https://github.com/KotisK/onto4drone
50. Shapes Constraint Language (SHACL). https://www.w3.org/TR/shacl/
51. GitHub - fekaputra/shacl-plugin: SHACL4Protege - SHACL constraint validation plugin for Protégé.
https://github.com/fekaputra/shacl-plugin
52. GitHub - protegeproject/snap-sparql-query: an API for parsing SPARQL queries. https://github.com/
protegeproject/snap-sparql-query
53. Neosemantics(n10s) User Guide - Neosemantics. https://neo4j.com/labs/neosemantics/4.0/
54. Historical Weather API | Open-Meteo.com. https://open-meteo.com/en/docs/historical-weather-api
55. OpenStreetMap. https://www.openstreetmap.org/
56. Kopsachilis V , V achtsavanis N, V aitis M (2022) Semi-automatic semantiﬁcation of institutional spatial
datasets
57. Overpass API. https://wiki.openstreetmap.org/wiki/Overpass_API
Publisher’s Note Springer Nature remains neutral with regard to jurisdictional claims in published maps and
institutional afﬁliations.
123

4924 S. Angelis et al.
Sotiris Angelis is currently a PhD candidate and a member of i-
Laboratory in the Department of Cultural Technology and Communi-
cation at the University of the Aegean. His research interests focus on
Semantic Web, Knowledge Graphs, cultural data integration, seman-
tic trajectories, and recommendation systems. He received his Mas-
ter’s degree in “Cultural Informatics and Communication” from the
same Department, where he studied Web technologies, Linked Data,
and application design. He holds a Dipl.-Ing. degree in the Depart-
ment of Electrical and Computer Engineering from Aristotle University
of Thessaloniki. His background and professional experience focus on
software engineering and web development.
Efthymia Moraitou is a PhD candidate of the University of the Aegean,
Dept. of Cultural Technology and Communication, and a researcher
in the ﬁeld of Semantic Web technologies on the Cultural Heritage
domain. Her research focuses on ontologies and knowledge graphs
engineering, and their exploitation in semantic services, frameworks
and tools. She holds a bachelor’s degree on Conservation of Antiqui-
ties and Works of Art (Technological Educational Institute of Athens)
and a master’s degree on Cultural Informatics and Communication
(University of the Aegean). She has worked as a professional conser-
vator in laboratories of the private and public sector in Greece, spe-
cialized in wall paintings and archival collections conservation; while,
she has participated as a researcher in different research programs of
the i-Laboratory and the ii-research group.
George Caridakis serves as an Associate Professor the Department of
Cultural Technology and Communication, University of the Aegean
where he coordinates the Intelligent Interaction research group
(ii.aegean.gr) active in the research ﬁelds of Intelligent Systems,
Human Computer Interaction, and Digital Management of Cultural
Heritage. He is also afﬁliated as a research professor with the Athena
RC and the Artiﬁcial Intelligence and Learning Systems Labora-
tory (AILS), National Technical University of Athens. He has been
appointed as an expert at the CEDCHE (Commission Expert Group
on the Common European Data Space for Cultural Heritage), Chair of
the Tourism, Culture and Creative Industries Sectoral Scientiﬁc Coun-
cil (SSC), National Council for Research, Technology and Innovation
(NCRTI), and elected as Chair of the (Greek ACM SIGCHI).
123

CHEKG: a collaborative and hybrid methodology… 4925
Konstantinos Kotis is currently a tenure track associate professor at
the University of the Aegean, Dept. of Cultural Informatics and Com-
munication, i-Laboratory, and a research associate at the University of
Piraeus, Dept. of Digital Systems, AI Laboratory. His research inter-
ests include Knowledge/Ontology Engineering, Semantic Web tech-
nologies, Semantic Data Management, Semantic Web of Things, and
KG-based conversational AI (chatbots). He has published more than
100 papers in peer-reviewed international journals and conferences
(Google Scholar h-index 22, citations >2000) and served as reviewer
and PC member in several journals and conference events. He has also
contributed to several national and European projects from different
roles/positions. For more, please visit: http://i-lab.aegean.gr/kotis.
123
```

## Merged notes from duplicate

_Source file:_ `CHEKG a collaborative and hybrid methodology for engineering modular and fair domain-specific knowledge graphs.md`

> ([[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf#page=2&annotation=884R|CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs, p.4900]])
> The ontology lifecycle, which includes feasibility analysis, identification of goals, requirements specification, implementation, evaluation, and maintenance, is defined almost similarly by different ontology engineering methodologies (OEMs), and it is partially or fully supported by ontology engineering (OE) tools [19].

> ([[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf#page=2&annotation=887R|CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs, p.4900]])
> However, the role and active involvement in the ontology lifecycle of (i) domain experts, who have the knowledge/expertise of the domain and/or data sources, as well as (ii) knowledge workers, who exploit the ontology in ‘operational’ conditions (e.g., solve problems, perform data-driven analysis tasks) is considered equally useful and essential for human-centered and collaborative approaches [13, 15, 19, 22–24]. #Tech/SemanticWeb/collaborative 

> ([[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf#page=3&annotation=890R|CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs, p.4901]])
> HEKG constitutes a hybrid (schema-center/top-down and datadriven/bottom-up), collaborative, and iterative approach for KG development. The CHEKG methodology is based on the main methodological phases of the latest version of ext-HCOME OE methodology [26], while it adjusts and expands the individual processes and tasks of each phase according to the KG development specialized requirements (modularity of KG’s model and content, agility, data quality, and bias). Although there are several other agile OEMs such as UPONLite [21], SAMOD [20], AGIScont [22], and XD [27] that could be exploited or adapted for KG development, the presented work is novel since, to the best of our knowledge, another effort to adapt a collaborative, iterative, and agile methodology to propose a methodology for engineering domain-specific modular and fair KGs, has not been presented elsewhere yet.
#Tech/SemanticWeb/KG/method 


[[CHEKG Collaborative and Hybrid Methodology for Engineering Fair Knowledge Graphs.pdf]]

Collaborative engineering of knowledge graphs, Engineering methodology, knowledge graph, bias assessment 

Human-Centered Collaborative Ontology Engineering Methodology (CHEKG) #op/acc/buscar #Tech/SemanticWeb/KG/method


