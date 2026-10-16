---
title: From Ontology Design to User Experience. A methodology to design interfaces for information seeking purposes
author: Grasso, Marco; Daquino, Marilena; Renda, Giulia
year: "2024"
Type: Article
DOI: 10.6092/issn.2532-8816/19038
source: https://doi.org/10.6092/issn.2532-8816/19038
created: 2026-05-25
description: Methodology linking ontology design (competency questions, KO) to UI components and UX journeys for LOD-based information seeking; music-heritage case study with user evaluation.
tags:
  - op/acc/pending-review
  - op/acc/process
  - design/UX
  - tech/semantic-web
  - humanities/digitalHumanities
  - Tech/SemanticWeb/KG/ontology
pdfORepub: "[[From Ontology Design to User Experience. A methodology to design interfaces for information seeking purposes.pdf]]"
---
[[From Ontology Design to User Experience. A methodology to design interfaces for information seeking purposes.pdf]]

> **Abstract:** When designing data-driven web applications, users' informative needs are aligned to knowledge organization (KO) requirements, which are secondly mapped to user interfaces (UI) components, and finally to user experience (UX) journeys. Particularly, when data are served as Linked Open Data, data and user requirements can be associated with competency questions that an ontology should address. The authors propose a methodology to design web applications for information seeking that leverages ontology design methodologies and UI/UX approaches, with a music-heritage case study evaluated via a user study. ([Source](https://doi.org/10.6092/issn.2532-8816/19038))
## Full text (extracted from `From Ontology Design to User Experience. A methodology to design interfaces for information seeking purposes.pdf`)

*Source:* `2PDF/From Ontology Design to User Experience. A methodology to design interfaces for information seeking purposes.pdf`  
*Extracted:* 2026-05-25

```text
Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
M. Grasso, M. Daquino, G. Renda – From Ontology Design to User Experience 
DOI: http://doi.org/10.6092/issn.2532-8816/19038 
   
 
53 
Copyright © 2024 The Author(s) 
The text in this work is licensed under the Creative Commons BY License. 
https://creativecommons.org/licenses/by/4.0/ 
From Ontology Design to User Experience. 
A methodology to design interfaces for information 
seeking purposes 
Marco Grasso 
University of Bologna 
marco.grasso7@unibo.it 
Marilena Daquino 
University of Bologna 
marilena.daquino2@unibo.it 
Giulia Renda 
University of Bologna 
giulia.renda3@unibo.it 
Abstract 
When designing data-driven web applications, users’ informative needs are aligned to knowledge 
organization (KO) requirements, which are secondly mapped to user interfaces (UI) 
components, and finally to user experience (UX) journeys. Particularly, when data are served as 
Linked Open Data, data and user re quirements can be associated with competency questions 
that an ontology should address. However, to the best of our knowledge, there is no full-fledged 
methodology that systematically adopts ontology requirements to design UI components and 
UX journeys. In  this article we propose a methodology to design web applications for 
information seeking purposes that leverages well -known ontology design methodologies and 
UI/UX approaches. We present a case study based on music heritage and we evaluate it via a 
user study. 
Keywords: User eXperience; Linked Open Data; Cultural Heritage; Ontology design 
Nel progettare applicazioni web basate sui dati, le necessità informative degli utenti sono allineate ai requisiti di 
organizzazione della conoscenza, successivamente mappati sui componenti delle interfacce utente (UI) e infine sui 
percorsi dell’esperienza utente (UX). In particolare, quando i dati vengono forniti come Linked Open Data, 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
54 
requisiti dati e utente possono essere associati a competency questions che un ’ontologia dovrebbe affrontare. 
Tuttavia, fino a quanto sappiamo, manca una metodologia completa che adotti in modo sistematico i requisiti 
ontologici per progettare componenti UI e percorsi UX. In questo articolo proponiamo una metodologia per 
progettare applicazioni web per il recupero di informazioni che sfrutti metodologie di progettazione ontologica ben 
consolidate e approcci UI/UX. Presentiamo un caso di studio basato sul pa trimonio musicale e lo valutiamo 
attraverso uno studio utente. 
Keywords: Web Semantico; Linked Open Data; Progettazione di Ontologie; Esperienza Utente; 
Metodologia di Progettazione 
Introduction 1 
The Semantic Web was envisioned as an enhancement of the current World Wide Web , the 
latter mainly targeted at human consumption with machine -understandable data and services 
relying on Linked Open Data [6]. Formal ontologies enrich data with metadata, thanks to a 
knowledge representation language based on a formal logic which facilitates data integration, 
sharing, and discovery [21]. 
One of the main tasks of data consumers on the Web is information seeking. Whereas a search 
on the Web was usually performed over unstructured data and it was expected to return a list of 
ranked documents relevant to the query [32], in the Semantic Web, searches are performed via 
SPARQL queries against structured data, and results are in the form of RDF triples [10]. Since 
the structure of a SPARQL query is based on terms of the ontology used to describe data, which 
in turn is derived from a shared conceptualisation of the knowledge domain, a mapping between 
users’ informative needs (queries), ontology requirements (predicates and classes), and final 
interfaces presenting results could be performed with high confidence. To this extent, we would 
expect ontology design practices to be closely related to user interfaces (UI) and user experience 
(UX) methodologies, and vice versa. 
On the one hand, the community of ontology design has been increasingly leveraging tools used 
in the Human -Computer Interaction (HCI) field - such as the definition of personas and 
scenarios [12], [37] - in early stages and as a means for evaluation [25], [42], [47], [50]. In 
particular, ontology requirements are traditionally expressed in the form of natural language 
Competency Questions (CQs) [38], which can be extracted from user stories attributed to 
personas [42]. On the other hand, it has been demonstrated that ontology -driven approaches 
have brought significant benefit in reducing interface requirements ambiguity [1], [14] when 
supporting software development [14], [51], [55], and requirements formulation, e.g. by creating 
user stories as structured data [53]. Task ontologies and taxonomies for describing interactive 
user behaviours and UI elements exist [39], [43], [49], and have been used to support the 
assessment of prototypes and final interfaces. Similarly, ontologies and algorithms addressing 
HCI design in the design of web applications have been discussed [2], [3]. While such efforts 
focus on the description of aspects of the HCI discipline, they do not operationalise the 
descriptive knowledge of domain ontologies (those used to represent the data and not the 
 
1 Marilena Daquino is responsible for section Introduction, Background, and Methodology. 
Giulia Renda is responsible for section Related Work and Discussion. Marco Grasso is 
responsible for sections Case Study, Evaluation, and Conclusion. 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
55 
UI/UX process) into prescriptive models, i.e. defining how a system is supposed to behave 
according to ontology requirements (e.g. CQs). 
To the best of our knowledge, there is no methodology that assists a research team from early 
stages of ontology design to the selection of UI/UX approaches. Nonetheless, this is often the 
case in projects where the knowledge base generation comes with use r-friendly interfaces for 
information seeking, exploration, and discovery purposes [23], e.g. projects dedicated to the 
dissemination of Cultural Heritage on the Web [27]. 
In this article we investigate the bridge between ontology design and UI/UX design 
methodologies to assist designers in prototyping web applications for information seeking 
purposes. Our aim is to extend the early stage of established UI/UX methodologies, such as 
Design Thinking [37], [45], with a suitable ontology -driven approach, i.e. the eXtreme Design 
methodology [42]. We suggest qualitative and quantitative analyses to be performed over 
ontology requirements, methods to support the ideation of prototypes, and finally an evaluation 
method to assess the validity of the entire methodology when applied to the design of interfaces 
for Cultural Heritage collections. 
In detail, in section Related Work we report on prior works in ontology design and UI/UX studies 
for information seeking purposes, motivating the selection of two candidates for developing our 
hybrid approach. Selected methodologies are briefly outlined in section Background to better 
appreciate our contribution to both candidates. In section Methodology we present the framework 
from ontology design to user experience. In section Case study we present our framework applied 
to a real -world scenario, i.e. the  requirements collection for a Web portal on music heritage 
developed for the H2020 project Polifonia. In section Evaluation we present a user study 
performed to validate the case study. We finally discuss results and limitations of our approach 
in section Discussion. Final considerations and future works are outlined in section Conclusions. 
Related Work 
Several methodologies for ontology design have adopted tools from the HCI field. These 
methodologies privilege a bottom -up approach to elicit requirements during the knowledge 
acquisition phase, and rely on the intervention of domain experts in (1) definin g domain space 
and vocabulary, (2) sketching motivating scenarios, and (3) extracting Competency Questions 
from scenarios [13], [20], [38], [42], [52]. 
The XD methodology [9], [42], formalises practices to collect goals, topics of interest, and tasks 
from heterogeneous groups of stakeholders and group them under umbrella categories, i.e. 
personas. In XD research journeys and groups ’ expectations are recorded in the form of user 
stories and are classified according to their level of priority. User stories, similarly to user 
journeys, address the emotional experience of a user - characterised by a space, a time, a role, 
and an interfac e - as well as users ’ interactive behaviours [5], [29]. Stories are recognised as 
powerful tools for designing experiences, since events described in stories are connected through 
causal relations and help to frame motivational aspects leading a user to behave in a certain way 
[19]. To this extent, the knowledge acquisition process is designed around personas or proto -
personas [24], which summarise behaviours when searching a knowledge base. For these reasons, 
XD is a good candidate for a seamless integration with UI/UX design processes. 
When requirements are mapped to UI elements for information seeking purposes, two kinds of 
interactive behaviours emerge. On the one hand, journeys may focus on retaining the user, and 
a common strategy is breaking down the information and displaying it in small chunks, so as to 
reduce the cognitive load [26]. On the other hand, studies in Information Science and Digital 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
56 
Humanities have demonstrated that preventing the user from seeing the “whole picture” may 
become a factor of frustration, therefore advocating for more generous interfaces [54]. Authors have 
argued that websites users are not always focused on information seeking as their sole task. 
Casual browsing can also be an effective way for users to discover and refine their objectives, if 
they have any. Such a form of visual exploration has been previously summarised as “overview 
first, zoom and filter, then details on demand” [48]. Compromising retention and overview is an 
important challenge for third generation information systems, that should allow users to first 
filter out data of interest, and then apply various analysis and knowledge discovery tools on the 
target [23]. In terms of usability, interfaces harmonising such two different viewpoints should be 
able to accommodate multiple tasks and user journeys, ensuring context completeness [7]. 
Design Thinking (DT) [8], [16], [37], [45] is a renowned user -centric approach to problem -
solving for designing artefacts, including web interfaces, which organises the workflow in six 
phases: empathize, define, ideate, prototype, test, and implement. It is based on a hypothesis -
driven, abductive, and dialectical approach to map requirements into design ideas. The data 
collection phase encompasses qualitative investigation (e.g. ethnography, visual anthropology, 
brainstorming, co-creation, and definitions by example) as well as quantitative analyses [30], and 
leverages personas, stories, stakeholder maps, user journey maps, and service blueprints to 
formalise requirements [11]. Although the number of empirical, non-anecdotal, studies based on 
Design Thinking is limited [18], previous studies demonstrated that the methodology effectively 
improves the quality of ideas and reduces risks of failure [30]. 
Scholars have tried to encapsulate the logic of DT into ontologies to evaluate design ideas [43], 
to formally describe empathy models [41], or other procedural aspects of HCI [2], [3], [39], [49], 
attempting to bridge ontology -based approaches and UI/UX methodologies. However, while 
most works focus on the creation of ontologies describing concepts and procedures of DT, they 
neglect considerations on the overall, prescriptive framework. In fact, t he population of 
ontologies with personas, UI components, and tasks, facilitates the preliminary analysis of 
requirements, but does not consider the formal domain knowledge, which inevitably affects the 
analysis, the retrieval of information, and the defin ition of UI/UX components that are 
necessarily tied to the domain knowledge. 
In summary, new ontologies have been created to instruct us on how formal definitions of HCI 
field and Design Thinking methods would look like, but not on how to leverage real -world 
domain ontologies in the Design Thinking process. In this work we aim at f illing this gap, 
suggesting the application of methods and analyses widely recognised as tools of the Design 
Thinking methodology directly to the domain ontologies. 
Background 
The eXtreme Design methodology. Ontology design patterns (ODPs) [17] provide solutions to 
recurring modelling issues. ODPs are extensively used in the eXtreme Design (XD) 
methodology [42], which is an ontology design methodology characterised by an iterative and 
collaborative approach to elicit requirements. Requirements are collected in the form of user 
stories, i.e. a set of sentences which describes by example the kind of facts that the  resulting 
knowledge graph should include. The length of a user story is limited to avoid ambiguity. 
Competency questions (CQs) are extracted from the story in the form of free -text questions, 
which act as natural language counterparts of structured SPARQL queries and as general (logic) 
constraints of the ontology [9]. At each iteration in XD, CQs are selected and matched to ODPs 
which are included in a unit test. In a unit test, CQs are translated into SPARQL queries and 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
57 
general constraints are used to create toy data. In [9] authors present a case study based on 
cultural heritage data recorded in catalogues and propose an extension of XD in order to elicit 
requirements from heterogeneous groups, since the information recorded in the catalogues is 
neither self-explanatory nor sufficient to address a complex scenario. They introduce personas 
to group stories related by goal, subject, task, and expectations. In so doing, ontology developers 
have an effective means to validate the soundness of their choices based on real-world scenarios. 
The Design Thinking methodology. The methodology puts an emphasis on methods to empathize and 
define, when designers respectively frame the domain space and make sense of collected insights. 
Several aiding tools and research techniques can be adopted to collect requirements, such as: 
surveys or interviews with stakeholders, kick off meetings with the des ign team, field studies, 
customer service feedback, or heuristic evaluation (recording frustration factors in prior versions 
of the product or competitor pr oducts) [11]. To elaborate information, designers can adopt 
Personas - i.e. simplified descriptions of users including biographical information, tasks, interests, 
and expectations - or proto-personas - i.e. profiles that represent the idea of a user according to 
the view of the team rather than the actual user. User stories describe situations or tasks the 
personas may face. User Journey Maps are visual representations of users ’ research path, and of 
feelings elicited from the interfaces. Empathy maps can be used to record what a user Says, Thinks, 
Does, and Feels. Similarly, Stakeholder maps are visual representations of groups, e.g. early 
adopters of the final product. A different perspective is provided by Competitive analysis, where 
competitors are bench-marked in order to grasp information on what works well (or not) in their 
services, and how their users look like [11]. 
Insights are transformed into workable prototypes (ideate and prototype), which are often the result 
of team activities, such as brainstorming or concept development techniques [30]. Rapid 
prototyping [31] is a common approach to develop a proof of concept or mockup, that can 
facilitate communication and feedback between teams and stakeholders. Visualization tools like 
mind mapping and storyboards are also deemed useful prototypes. 
The test and implement phases address both the design of experiments to test the solution, and its 
evaluation. Common methods include user studies, focus groups, or other activities in which 
feedback is used to refine a prototype in an iterative, trial and error, approach. The e valuation 
can be performed in a laboratory environment (e.g. mockups) or in the application environment 
(e.g. a web-ready solution). Metrics are used to evaluate the result, e.g. ease of use, accessibility, 
usefulness, reliability, efficiency, and user experience [27]. 
Evaluation of UX design methodologies. Results of the prototype evaluation are often deemed 
sufficient to validate the UX design methodology adopted to develop the solution too (i.e. the 
methodology inherits the positive judgment given to the result). For instance, Design Thinking 
is considered  a reliable methodology for UI/UX design, and the literature is replete with 
anecdotal studies showcasing successful cases. However, scholars have argued that existing UX 
evaluation methodologies tackle only a small range of problems, e.g. usefulness and ease of use 
only, and there is no optimal combination of evaluation methods to maximise the range of 
measured qualities [27]. To this extent, we may argue that the evaluation of the design 
methodology itself is hampered by the limits of the UX evaluation methodology, and only partial 
evaluation methods can be developed to test the goodness of a UX design methodology in the 
first place. In this work we are interested in evaluating the co-design aspects underlying our 
proposed methodology. In particular, we want to test whether the UX elaborated in a case study 
leveraging our methodology sufficiently matches the expectations of users classified as secondary 
target of the final web applications. 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
58 
Methodology: from ontology design to user experience design 
We introduce a modular workflow harmonising eXtreme Design and Design Thinking 
methodologies in order to formalise a way to wisely leverage ontology requirements into the 
design of user interfaces. The proposed methodology spans from data and user requirem ents 
collection to the development of prototypes and their evaluation. The empathise phase of Design 
Thinking is integrated with methods proposed by eXtreme Design, such as the extraction of 
CQs from user stories and the mapping of CQs to ontology design p atterns. Unlike other 
ontology-driven approaches to UI/UX design, we systematically reuse data/user requirements 
and domain ontologies in the define phase, and we propose a number of analyses to be performed 
over annotated CQs in order to ideate solutions consistent to requirements, to be later 
implemented in a prototype. Lastly, we integrate a user study focused on co-design aspects to test 
both results and our methodology. 
In Figure 1 we illustrate the list of activities performed. Activities are grouped under phases 
defined by Design Thinking. Grey blocks represent activities prescribed by either XD or DT, 
and white blocks represent our original contribution. Alternative methods are proposed for define. 
 
Figure 1. Methodology overview2 
Interviews with stakeholders are performed to identify requirements of data consumers and 
users. Interviews address interests, habits, expectations, and frustration factors when interacting 
with an information system they know. Via interviews we collect: (1) motivational aspects, (2) a 
list of competitors of the product to be developed, (3) behaviours (journeys), (4) perceived 
limitations and benefits of competitors, (5) expectations and desiderata, both in terms of content 
requirements and application requirements. Resources mentioned during interviews are included 
 
2 All images are published under a CC BY 4.0 license.  


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
59 
in a competitive analysis, along with other competitors found in the exploratory phase, that are 
analysed by the design team. The analysis addresses the classification of aspects relevant to 
knowledge organisation, UI design, and brand identity of surveyed solutions. We narrow down 
the list of resources to those presenting recurring aspects. A user study is performed on the 
narrow list of competitors, in order to record customer feedback. The study is performed with 
participants classified as secondary targ et that were not included in the interviews, in order to 
integrate results obtained from interviews and the competitive analysis with new contexts of 
usage. Participants are asked to evaluate two or more web solutions and must answer questions 
to estimate (1) their information literacy or expertise on the topic, (2) their common tasks and 
situations, (3) their level of understanding and interest in the contents proposed, and (4) an 
evaluation of interfaces and experience. In particular, proposed solutions m ust represent 
alternative UX approaches to solve the same (or similar) problem tackled, e.g. a google-alike text 
search over a catalogue or a more descriptive website. Results of the survey include a list of 
secondary constraints to be taken into account w hen prototyping, to ensure flexibility of 
interfaces in different contexts than those depicted by primary stakeholders. Moreover, it would 
offer a preliminary evaluation of the UI/UX strategy to adopt, whether this is going to be a 
generous interface or a specialised one. 
Interviews and results of the survey are summarised into a number of personas, i.e. stereotypical 
users presented in the form of textual descriptions. Situations, tasks, interests, and expectations 
emerged from the interview and the survey are further desc ribed in one or more user stories, 
having the persona as subject. Competency Questions are extracted from stories, via content 
and syntactic analysis of the text. CQs summarise salient aspects of the story in the form of 
natural language questions, address  ontology and data requirements, and semantic constraints 
on relations (i.e. properties) and classifications of entities described in data (i.e. classes). CQs are 
mapped to SPARQL queries, to be used to validate the ontology, and are characterised by a 
priority level (e.g. must have, nice feature). Answers to CQs can be strings, lists, tables, or graphs 
of entities. We propose to annotate CQs with (1) ontology patterns, including classes and 
properties of entities involved, (2) a classification of the scope  of data (e.g. historical, musical, 
bibliographical data), (3) whether the question addresses a task (e.g. a search, share) or a 
secondary detail, and (4) the type of expected result, which can be also presented as aggregated 
data, e.g. charts. 
Ontology patterns are synthetic summaries of content requirements of a knowledge base and are 
relevant also to the design of search interfaces on the same. From stories and CQs we also grasp 
important information for the design of user journeys, i.e. the f low of searches, reading 
behaviours, and emotional states of the user. We propose two alternative ways to extract journeys 
from content requirements. If collected personas are rather homogeneous and in a small amount, 
we identify a driver CQs and cluster other CQs. In particular, driver CQs are one or more CQs 
that best summarise the scope of data and the task (e.g. search for artefacts grouped under 
categories). Other CQs are usually focused on contextual aspects, such as secondary detail of 
data, and can therefore be grouped under the same category. In case personas, stories, and CQs 
are too many to be singularly addressed, we recommend performing Exploratory Data Analysis 
(EDA) over annotated CQs. In detail, EDA allows us to summarise the distribution of (1) 
ontology patterns, (2) scope of data, and (3) expected results, along with their priority level. 
Notably, ontology patterns can be visualised as flows (e.g. via Sankey diagrams), which nicely 
resemble user journeys, highlighting most recurring patterns  and the expected level of 
complexity of queries. 
Once all the materials are available, brainstorming sessions help to make sense of results, leading 
the discussion over mockups. To support this activity, we propose to integrate two more analyses 
devoted to the design of interfaces only, namely: a task an alysis, where CQs are aggregated by 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
60 
the user task previously annotated, sorted by complexity of the task, and separated accordingly 
into different sorts of interfaces; a thematic analysis, based on the distribution of classes and 
their position in ontology patterns (i.e. as input, intermediate, or output), in order to understand 
most common access points to data (e.g. plenty of CQs address information about people, hence 
“people” should be a category for browsing/filtering/searching in the final interface). It’s worth 
nothing that at this poi nt designers may want to revisit groupings of tasks/themes/CQs and 
propose more than one interface. 
Mockups or early prototypes can be evaluated differently, according to the objectives and the 
level of detail required to move the result in a production environment. Focus groups with small 
groups of stakeholders involved in the definition of requirements provide meaningful feedback, 
helping to reframe requirements that were unclear or incorrect. Usability tests and heuristic 
evaluation with 3-5 people groups are considered sufficient to discover up to 90% of issues [36]. 
However, when a website has several highly distinct groups of users, additional user tests are 
needed. To include the secondary target user in the evaluation, we propose a user study focused 
on co-design. The initial user study (Customer feedback) guided participants in the evaluation of 
a working solution, and the judgement provided was biased by a number of factors that could 
have not been foreseen (e.g. participant may or may not have known the website, they did not 
like the UI, they did not understand the lexicon). In a co-design user study, participants have to 
imagine themselves into a comfortable scenario (e.g. “you are at home studying”), are provided 
with a task (e.g. “you want to discover new music”) and must share insights on how they would 
achieve their goal. Results of the survey contribute to preliminarily evaluate the mockups (despite 
these are not given to participants), since they provide measurable values for metrics like user 
satisfaction, efficiency, and effectiveness, of a broad span of  alternative solutions, hopefully 
including the ones designed in the mockups. If results are satisfying, mockups are implemented, 
and solution are deployed in production. More tests are performed in between - e.g. test-driven 
development, unit tests, and final user tests - but these are not covered in this proposal, that is 
mostly focused on design evaluation. 
Teams. Activities borrowed from eXtreme Design mainly involve ontology designers and domain 
experts in the mapping of requirements onto competency questions. Moreover, data engineers 
are required in order to analyse data and identify most common data journeys, that is, the most 
likely combinations of pieces of information that are needed to answer competency questions. 
Web designers are also involved when performing task and thematic analyses, and when 
developing the initial prototype. Stakeholders and secondary target users (i.e. those that are not 
involved in the initial collection of requirements) are involved in the refinement of requirements 
(via brainstorming activities), and in user tests, to validate data and user journeys. 
Case Study: the design of web interfaces for Polifonia 
Polifonia3 is a project funded by the European H2020 framework devoted to the dissemination 
of European music heritage resources. Ten pilot projects have been designed to collect data 
sources (e.g. texts, audio files), extract information, and transform data into Linked Open Data 
(LOD) to populate a knowledge graph, in turn leveraged by user-friendly web interfaces. Given 
the variety of data and audience in scope, having a solid methodological approach to drive the 
development, from knowledge acquisition to web design , is of great concern. In fact, existing 
 
3 https://polifonia-project.eu/ 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
61 
examples to create vast data aggregators in the cultural heritage domain, e.g. Europeana, 
inevitably suffer from design issues, such as ontology limitations [40] or the lack of narrative 
elements facilitating exploration [33]. 
For these reasons, Polifonia is our motivational scenario to develop a methodology that prevents 
us from perpetuating old errors (and probably making a hundred new ones). In this section we 
present results obtained at each step of the workflow, adding cons iderations on how bits and 
pieces are put together to realise four web applications, namely: musoW4, a catalogue of music 
data available online to support developers and music journalists; MELODY 5, a Linked Open 
Data storytelling environment to let domain experts and data engineers creating data stories; 
Corpus6, an interface for text retrieval and linguistic analysis; finally, the Polifonia web portal7 to 
collect data from pilots and functionalities of aforementioned tools to be served to music 
enthusiasts and lay users. For the sake of brevity, we present only the design process of the web 
portal, which makes use of EDA to elaborate journey mappings. All the documents referenced 
below are available online, on GitHub8 and Zenodo9. 
Interview stakeholders. Around 30 stakeholders are selected among project members and 
acquaintances with a similar background. Most of them are scholars, music historians, 
musicologists, but also music producers and cultural heritage professionals. Ontology and data 
engineers lea d the interviews. Interviews follow a script, which addresses (1) the way 
stakeholders interact with music data, (2) their purposes, (3) which applications they use or know 
they could use, (4) what type of searches they do, and, if they have requests that cannot be 
satisfied by current solutions, (5) how they would envision a new tool or service. Interviews are 
recorded and transcribed to be later reworked into user stories, and recordings are deleted. 
Competitive analysis. Web applications mentioned in interviews and other websites that serve music 
content to broad audiences are surveyed by web designers. In total, we surveyed 22 websites of 
projects, companies, portfolios, magazines, and social media platforms relevant to t he music 
heritage domain, and we produced a table for comparison and analysis 10. Surveyed aspects 11 
include: goals (e.g. engage, inform, customer support, sharing), information architecture (e.g. 
hierarchical, sequential, audience-driven, generous), content organisation (e.g. index-based, flat, 
daisy model), visual hierarchy techniques (e.g. based on co lour, typography, proximity), 
interaction patterns (e.g. infinite scroll, animations, steps, slideshows), sound design (if any), user 
actions (login, share, search, navigation, feedback), and visual identity features (style, colour 
palette, shapes). A summary of results is illustrated in Figure 2. 
 
4 https://projects.dharc.unibo.it/musow/ 
5 https://projects.dharc.unibo.it/melody/ 
6 https://polifonia.disi.unibo.it/corpus/ 
7 https://polifonia.disi.unibo.it/portal/ 
8 https://github.com/polifonia-project/web_portal 
9 https://doi.org/10.5281/zenodo.6669816 
10 Competitive analysis: https://github.com/polifonia-project/web_portal/tree/main/analysis 
11 Definitions: https://github.com/polifonia-
project/web_portal/blob/main/analysis/definitions.pdf 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
62 
 
Figure 2. Competitive analysis 
Surveyed applications either focus on generating leads, attracting users and raising their interest 
into some product or activity or providing information to engage users in participatory activities. 
Information is often provided sequentially, creating a s tep-by-step flow to let the user achieve 
their goal. A hierarchical organisation of content is also rather common, where important 
information is shown first and details are differentiated by size, colour, contrast, etc. In such 
cases, proximity is used to group pieces of information of similar importance, and repetition of 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
63 
visual patterns is used to highlight similarities. Fewer examples offer generous interfaces and/or 
group information by topic. Most applications use a flat model to organise content in a few 
pages. When serving large contents, more sophisticated models are in place, such as indexes and 
different access points to the same information (coexisting hierarchies). In terms of visual 
identity, surveyed solutions are mostly characterised by a minimalist look and feel, including 
geometric shapes, large usage of blac k and white colours, and sans serif fonts. In conclusion, 
two broad groups of online services can be recognised, which can be categorised as music 
streaming services and magazines, wherein large contents are served via (coexisting) index 
models. 
Customer feedback. To make sense of insights gathered from the competitive analysis, nonexpert 
users’ experiences have been integrated. Quantitative and qualitative data about user ’s 
interactions and experience with music related digital products have been collected through a 
questionnaire. The conducted survey consisted of 46 questions, broadly categori sed into three 
main areas of interest: (1) user habits, (2) expectations, and (3) causes of frustration. These topics 
were explored using an experience-based methodology that integrates field studies, ethnographic 
research, and contextual inquiry [46]. In exploring user habits (1), the survey focused on 
interactions with popular music streaming services like Spotify, Apple Music, and Tidal. For user 
expectations (2), the inquiry centred around responses to online music magazines, including 
Resident Adv isor, Rateyourmusic, and Last.fm. Finally, to understand frustration sources, 
participants were introduced to two distinct music websites: Spotify Fun Study 12 and 
Expodcast13, each chosen for their unique UX designs. Spotify Fun Study offers data -driven 
insights into global fan-artist connections, featuring an interactive interface that transitions from 
simple information displays to complex data visualizations. In contrast, Expodcast is a baroque-
style immersive virtual exhibition with episodic storytelling, presenting information, both textual 
and visual, in a dense, non-progressive manner. 
The survey was conducted with 154 14 undergraduate communication science students aged 20-
30. Only 10% of participants have a music education, and their listening habits skew towards 
popular music genres. 60% engage regularly with music content, primarily to create personal 
collections. In th eir online behaviour, users show simple expectations towards a clean and 
organized look and feel for reading environments. While exploring music magazines and project 
websites, they showed a tendency to skim through content, preferring articles that are 
thematically organized with clear, simple schemes ( Figure 3). Full article engagement is low 
(30%), as users typically scan for specific interests. When interacting with music project websites, 
users were drawn to graphics and visually pleasing data visualizations, despite not being 
overwhelmed by information density. The Spotify Fun Study was preferred by 70% of users over 
Expodcast, largely due to its clarity and organization. Together with the progressive disclosure 
of content, the look and feel of the websites is among the most appreciated aspects. Participants’ 
preferences lean towards efficient text search capabilities, spontaneous discovery paths, and 
visually appealing interfaces. When recommendations are present, users tend to overlook them, 
favouring a more hands -on approach of immersive navigation and exp loring content through 
direct links and scrolling. The most favoured interaction style is the gradual unveiling of content. 
The browsing behaviour is characterized by minimal reading, with a stronger preference for 
 
12 https://fanstudy.byspotify.com/ 
13 https://expodcast.cmbv.fr/en 
14 Survey and results at: https://github.com/polifonia-
project/web_portal/blob/main/questionnaires/survey_march2022.csv 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
64 
interactive elements and immediate feedback. Overall, these findings emphasize the importance 
of clarity, organization, and aesthetically pleasing design in engaging non-expert users. 
 
Figure 3. Lay users’ interactions with music project websites 
Outline Personas. Domain experts of Polifonia collected 27 Stories and 17 Personas, with the intent 
of mapping out representative scenarios15. Experts are 30- to 40-year-old, highly educated with 
degrees in arts or music. They are employed in private companies or public institutions and work 
as researchers. Their objectives focus on discovering new music information, collecting data 
about artis ts and venues, and enhancing research documentation. The user group is 
homogeneously skilled, with two -thirds being music professionals and the rest having 
professional experience in fields outside of music. Given the results of the Competitive Analysis 
and Customer feedback, three personas have been added to cover the entire spectrum of users 
that might interact with the web interfaces, e.g. non-expert, and generic user representation. The 
persona-creation process has been guided by two established [28] methodologies: 
• Qualitative method: personas are based on small -sample qualitative research, such as 
interviews, usability tests, or field studies. 
• Quantitative method: a survey is used to gather a large sample of users, and the 
personas emerge from statistical analysis. 
For instance, to create the persona called Laurent16, a systematic approach was employed. This 
involved gathering information about his age, gender, educational background, language 
proficiency, interests, occupations, and personality traits. His knowledge and skills in music 
journalism, coupled with his st rong will and organizational capabilities, were highlighted. His 
online behaviour was meticulously detailed, noting his daily device usage, preference for 
applications, and frequent online purchasing habits. This comprehensive description helps in 
understanding Laurent ’s needs, preferences, and behaviours. By encompassing both his 
 
15 https://github.com/polifonia-project/stories 
16 https://github.com/polifonia-project/stories/tree/main/Laurent_Music_Journalist 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
65 
professional expertise and personal traits, a holistic view of Laurent is presented, useful for 
tailoring content, features, and services. 
Write User stories. In Polifonia, each Persona is linked with one or more Stories, which are crafted 
based on user goals and narrative scenarios. The formulation of goals, scenarios, and competency 
questions is based on the data collected from the aforementioned interviews an d surveys. For 
instance, Laurent’s story reads as follows: Laurent is a music journalist that maintains the “Music 
Journalism Insider” newsletter. His objective is to delve into music-related archives to enrich his newsletter. Every 
week, Laurent features outstanding music pieces, industry news, and interviews with professionals in the field. His 
work is powered by his use of music catalogues, personal experiences, and a desire to broaden the scope of music 
journalism. Laurent’s work could be enhanced by technologies that facilitate the discovery, exploration, and 
visualization of archival and historical music resources. The scenario of his weekly activities provides 
insights into his regular tasks, interests, and the resources he relies on. Key resources like music 
catalogues, online archives, and tools like Google Trends that Laurent uses are identified to 
understand his workflow and information needs. This is coupled with understanding the 
potential technologies that could aid his work, highlighting areas where his experience could be 
improved. 
Extract Competency Questions. The findings from the user research were thoroughly analysed, with 
a keen focus on identifying recurring themes, including common tasks, prevalent challenges, 
information needs, and decision -making criteria specific to each persona. From this analysis, 
targeted competency questions were formulated, addressing the identified needs and challenges. 
These questions were crafted to reflect the realistic inquiries potential users might have. To 
establish and evolve the “project mental model” [15], each story is further expanded to include 
a set of competency questions and resources. To ensure the questions were both authentic and 
relevant, they were validated with stakeholders, and refined based on the feedback received. This 
iterative refinement process was crucial in maintaining the accuracy and relevance of the 
questions in line with the evolving needs of the users. The competency questions listed below 
have been derived from the story and persona of Laurent. 
• CQ1: Can I search for a musical content by applying filters (genre, historical period)? 
• CQ2: What types of resources can I find? 
• CQ3: Is the music resource X complete or incomplete? 
• CQ4: Is a dataset attached to resource X? 
• CQ5: Can I add resources as a user? 
• CQ6: How can I share what I find on the website? 
While primarily serving ontology design purposes, questions highlight functionalities and 
features that would be most beneficial for Laurent in discovering, utilizing, and sharing music 
related content effectively in his work. They reflect his need for a comprehensive and user -
friendly system that aligns with his professional pursuits in music journalism. They also serve as 
a guiding framework for feature development, content strategy, and user interface design, 
ensuring that the final product is closely al igned with the target audience ’s needs and 
expectations. 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
66 
 
Figure 4. Sample of Annotated Competency Questions’ spreadsheet 
Annotate Competency Questions. To quantitatively analyse collected Competency Questions, an 
annotation method has been devised in a spreadsheet 17 document to provide a structured 
description of questions in terms of content and presentation aspects (Figure 4). 
Each question is first classified based on content characteristics. For the sake of simplicity, CQs 
have been divided into three thematic areas, which also correspond to the main expertise areas 
of Polifonia partners, namely: 
1. Bibliographic data: structured data addressing cataloguing and historical information of 
real-world entities (e.g. artifacts, people, places) and abstract concepts (art 
performances, events). These data are represented by 156 CQs. Among these, 81 
address bibliographic data only; 62 also focus on linguistic data; 23 also on music data; 
of the latter 10 focus on all three types. 
2. Music data: structured and unstructured data (audio) about content music features 
(melody, harmony) and characteristics (modality, tonality). These data are represented 
by 66 CQs. Among these, 38 focus on music data only; 23 also on bibliographic; 15 
also on linguistic data; 10 on all. 
3. Linguistic data: semi-structured and unstructured data (free-text) about music-related 
text sources (e.g. lyrics, newspapers). These data are represented by 80 CQs. Among 
these, 13 focus on linguistic data only; 62 also on bibliographic; 15 also on music; 10 
on all. 
The identification of Main Entities and Additional Entities/Properties offer a mapping between 
natural language questions and ontology design patterns, with an additional comment section 
for supplementary notes. Crucially, the system also incorporates deci sion-making aspects such 
as whether to include the question in browsing/querying interfaces and the type of support 
required for addressing it. This dual focus on content characterization and operational decision-
making facilitates an organized approach to handling the questions. 
The system also delves into the presentation and user interaction aspects essential for the web 
portal. It outlines how the information will be displayed (Output), combines questions with 
specific web pages, and considers their integration with the search interface. The annotation 
system also emphasizes the role of visualization, detailing the type of visual aids to be used and 
 
17 https://github.com/polifonia-
project/web_portal/blob/main/analysis/annotated_competency_questions.csv 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
67 
the method of data aggregation. By addressing both the content and presentation aspects, we 
ensure that the questions are not only relevant and informative but also effectively integrated 
into the digital platform. 
 
Figure 5. Distribution of input entities (left) and Distribution of output entities (right) 
Exploratory Data Analysis. Some pieces of information shall be prioritized when served via the 
web portal. In order to do that, as aforementioned, Competency Questions have been mapped 
to ontology classes and properties, so as to derive information on common data patterns. 
In Polifonia, most CQs address the analysis of Music works, Agents, and Sources, followed by 
CQs focused on Instruments, Collections, and Musical performances (Figure 5 left). Expected 
outputs (say, answers) of CQs include mostly Annotations, i.e., specific pieces of information 
characterizing the input or another entity, and Agents, followed by related Places, Music works, 
and Sources ( Figure 5 right). The relations between input and output entities have also been 
analysed. CQs starting from Music works mainly address related Music works, Agents, Sources, 
Places, and Annotations, followed by Collections, Media of performance and Time -related 
information. Agents mainly address related Agents, Places, and Sources, while Sources 
predominantly address Annotations. Instruments are usually related to Agents, Places, and 
Annotations, while Collections mainly address Annotations and Time -related informat ion. 
Finally, Musical performances generally direct to Agents, Types, and Annotations (Figure 6). 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
68 
 
Figure 6. Distribution of bigrams input/output 
Brainstorming. After the detailed analysis of data and competency questions, brainstorming 
sessions are where the insights and detailed understandings from the data analysis are 
transformed into actionable and innovative ideas. It’s a collaborative and dynamic activity where 
team members, equipped with the knowledge gained from earlier analyses, engage in the creative 
process of developing mock-ups proposals. This stage is critical for ensuring that the data-driven 
insights are not only understood, but are also visually and practically interpreted, leading to the 
design of user-centric and effective solutions. The aim is to translate the complex findings from 
the data into intuitive, practical designs that align with the project ’s objectives. These sessions 
act as a bridge between theoretical analysis and practical implementation, turning abstract 
concepts and Competency Questions into concrete, visual references. 
Task analysis. Task analysis is the examination of the actions and cognitive processes a user must 
engage in to complete a specific task. This analysis can predict how users might interact with 
products in development. A common method within this field is Hierarchical Ta sk Analysis, 
which breaks down a complex task into a hierarchy of smaller tasks, often referred to as 
hierarchical decomposition [44]. Expanding upon this, the method discussed here employs the 
principle of goal composition [35]. It starts by identifying the primary goals of users within the 
system. Then, to enrich these primary goals, a range of potential additional features are 
conceptualized by merging them with overarching meta-goals. In the scope of this study, goals 
were ex tracted from Competency Questions and each one was linked to a macro -goal 
representing the desired outcome (Figure 7). The macro-goals, along with their corresponding 
number of CQs, include: Share content (4), Search content (4), Personalize content (4), Learn 
more about content (6), Find relation between different content (15), Find answer to specific 
question (51), Explore sources of content (3), Discover new content (1), and Discover content 
(3). 
Subsequently, these goals were matched with user tasks. Each task provides a unique approach 
to achieving a goal, offering insights into how users work towards their objectives. High level 
tasks are then broken down into sub -tasks, which detail the step -by-step procedures from 
accessing the web portal to achieving the related goal ( Figure 8). To visually document this 
analysis, a diagram has been created (Figure 9). 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
69 
Thematic analysis. As highlighted in the Exploratory Data Analysis, bibliographic and historical 
data have been targeted as a priority in the development of the Polifonia web portal interface for 
music heritage exploration. This reasoning assumes that a category shared by th e majority of 
CQs is relevant to different target users. 
Consequently, a more detailed thematic data analysis has been performed to understand 
information patterns, entities and property patterns, and to define strategies for content design. 
In particular, each Competency Question can be described in terms of a starting node, an ending 
node, and a property path. The latter can be a direct path (e.g. “Where was an artist born?”) or 
present intermediate nodes (e.g. “Where was the music work performed?”). Information patterns 
extracted from Competency Questions have been summarized in a flowchart (Figure 10). 
 
Figure 7. Macro-goals matching with user tasks 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
70 
 
Figure 8 High-level task breakdown for search content goals 
 
Figure 9. Diagram of search and personalize sub-tasks 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
71 
 
Figure 10. Information patterns that occur at least three times extracted from competency questions 
The analysis of the most recurring patterns leads to the definition of 8 recurring discovery 
patterns which will be leveraged in the web portal as thematic sections. Sections can be 
summarized as follows: 
1. Documentary evidence of topics. Users have a topic in mind and look for documents 
referencing that topic. When exploring documents they want to know more about 
people (roles, audience), and connected topics. 
2. People connected to events. Users have a person in mind and want to collect 
information on related events (e.g. performances, biographical events, historical 
context). 
3. Soundscape of places. Users have a place in mind and want to grab all music -related 
information that characterize the place, such as events, music works, and information 
on the history of instruments. 
4. Music genres and related networks. Users have a genre (or composers relevant to the 
genre) in mind and want to discover people and works directly or indirectly related (e.g. 
influences). 
5. Scores and music works. Users have a piece of music in mind and want to retrieve 
scores, documents, and multimedia files searching by bibliographic metadata. 
6. Melodies and music works. Users have a piece of music in mind and want to retrieve 
scores, documents, and multimedia files searching by melodic patterns. 
7. Lyrics and music works. Users have a piece of music in mind and want to retrieve 
scores, documents, and multimedia files searching by lyrics. 
8. Music instruments. Users want to know more about the historical evolution of 
instruments. 
Mockups. Mockups represent the next and more in-depth iteration of the design approach. The 
designers’ work encompasses a four -phase creation process, each phase building upon the 
brainstorming and data analysis phases. The initial phase involves crafting a comprehensive 
graphical representation of the web portal ’s structure, called blueprints, focusing on the 
components and their interrelationships. The blueprint stage is where the data analysis comes in 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
72 
handy. Here, designers focus on developing a comprehensive graphical representation of the 
web portal’s entire structure (Figure 11). It’s akin to creating a map that outlines all the critical 
elements of the user interface, and how they connect. This phase is crucial because it sets the 
stage for all subsequent design work, ensuring that every element is placed with a clear 
understanding of its role and relationship to others in the system. 
 
Figure 11. Polifonia Web portal’s blueprint 
Building upon the groundwork laid by the blueprints, wireframes are created to enhance clarity 
and detail to the portal ’s functionality. This phase shifts the focus to the interaction and 
relationship of elements, rather than their aesthetic appeal. Wireframes act as a skeletal 
framework (Figure 12) for the portal, illustrating how users will interact with the interface, the 
flow of information, and how different screens connect. This stage is essential for visualizing the 
user experience and the portal’s functionality in a more concrete way, setting the stage for the 
visual elements that will be added later. Here, the brainstorming phase is essential for generating 
creative ideas and conceptualizing the initial layout and functionality of the portal. 
The mockups phase is where the design of the application is framed in visual aids. Here, the 
static wireframes are transformed with the addition of stylistic and visual User Interface details. 
This includes the integration of colours, styles, graphics, typography, and other visual elements 
that give the portal its unique look and feel. Mockups provide a realistic preview (Figure 13) of 
what the final pages will look like, allowing designers and stakeholders to see and feel the user 
interface before it is fully built. This phase is critical for finalizing design elements, ensuring that 
the portal is not only functional but also aesthetically pleasing and aligned with the brand identity. 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
73 
The final step in this process involves the creation of mockup prototypes, blending the interface 
skeleton from the blueprints and wireframes with the general look provided by the mockups. 
This early prototype is a functional and interactive simulation, encompassing most of the features 
intended for the final product. It allows users and pilot leaders to experience the resources in a 
semi-realistic environment and test the design ’s usability before it is actually put into 
development. 
Focus groups. Following the completion of the mockups, we progressed to a critical phase 
involving expert collaboration: conducting a focus group to gather qualitative insights that 
complement our quantitative data. In this phase, participants were given access to the e arly 
prototype and mockups of our web portal, enabling them to independently assess and interact 
with the interface. During this phase, participants were encouraged to participate in group 
discussions, fostering an environment where collectiv e opinions and shared needs could be 
openly expressed. Initially, they were encouraged to form their own judgments and navigate the 
system on their own, with the freedom to inquire about any aspects they found unclear or 
intriguing. Following this self-guided exploration, we provided a detailed walkthrough, clarifying 
each element of the interface. This approach was designed to discern whether the portal was 
intuitively comprehensible to users or if additional guidance was necessary to enhance their 
understanding and experience. 
 
Figure 12. Wireframe of one interface of the Polifonia Web portal 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
74 
 
Figure 13. Mockups of four interfaces of the Polifonia Web portal 
This interactive setting was instrumental in revealing common desires and vi ewpoints, insights 
that might have remained hidden in more structured, task-oriented evaluations. The qualitative 
nature of this focus group was pivotal in uncovering subtle yet significant aspects of user 
perception and experience. These insights were particularly valuable in understanding how users 
interact with generous interfaces. These interfaces are designed to encourage serendipitous 
discovery, operating on the principle that users may not always have a clear goal when they begin 
their exploration. Instead of directing users along a predetermined path, these interfaces offer a 
wealth of possibilities, inviting exploration and chance findings. Furthermore, this phase of the 
project enabled us to identify usability issues or barriers that might hinder the user experience, 
allowing us to make informed adjustments and enhancements to the interface. 
Evaluation 
The evaluation method adopted in this study is a participatory design approach. Different from 
traditional user testing methods, this approach integrates 18 experts - selected for their 
proficiency in user experience design and their in-depth knowledge of the music domain - and 
186 lay users. The primary objective is to investigate the efficacy of co -design methodologies 
[22] in enhancing the web portal development process, ensuring that it is user-centred and aligns 
closely with the needs and expectations of the end users. This methodology is rooted in the 
principles of co -design [4], emphasizing collaboration, user involvement, and iterative design 
processes.  
On the one hand, experts are requested to participate to interactive sessions, wherein one or 
more tasks are assigned to them (e.g. retrieve all artists influenced by a certain singer). However, 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
75 
experts are not merely testers but active contributors to the design process [34]. Indeed, the 
sessions are structured to facilitate real -time exploration, discussion, and comprehensive 
feedback on the prototype.  
On the other hand, when investigating preferences of the secondary target, i.e. lay users, these 
do not behave as testers at all, i.e. they are not provided with any web application and they are 
not asked to perform any task. Instead, they are asked to ima gine the web environment they 
would like in a certain context (e.g. you are at home studying/working, and you would like to 
listen to new music) and to describe how they would achieve their task. Proposing two different 
types of co-design tests allows us to evaluate both the idea and the expectations in two different 
settings, namely: the more traditional setting of evaluating a given interface, and a less traditional 
one where users are asked to imagine a web application and a number of features, tasks, an d 
desiderata without being biased by a given proposal.  
 
Figure 14. Users need platforms to suggest them new music (66,2%) 
 
Figure 15. Users appreciate the possibility to filter their results. 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
76 
 
Figure 16. Users would like to have filters based on known categories. 
The lay users test results reveal several key insights into participants’ preferences for a music web 
portal. A significant 86.9% showed interest in a portal integrating music data. Additionally, 
61.4% were keen on searches that start with specific inputs and guide them through a variety of 
information. The concept of serendipitous discovery was positively received, with 57 participants 
recounting favourable experiences with such discovery journeys. Moreover, 66.2% of 
participants expect the platform to offer suggestions as a launchpad for their exploration (Figure 
14), leading to personalized user journeys. These journeys are preferred to begin with or be based 
on music genres, artists, and general topics, with music genre being the most frequently mentioned 
term in open ended responses (154 times). This feedback was instrumental in establishing the 
five main entry points to the Polifonia knowledge graph (narrowing down the aforementioned 
thematic analysis, which returned 8 categories), encompassing the categories, highlights, and 
search sections. Interestingly, the survey highlighted a demand for a seemingly straightforward 
feature absent in existing music data discovery platforms: filter options. Notably 77.2% of 
participants valued the ability to filter search results ( Figure 15) using established categories to 
refine their search outcomes (Figure 16). 
During the co-design sessions with experts, the participants engaged in a series of tasks designed 
to simulate real -world use and to provoke discussion on various aspects of the web portal ’s 
design and functionality. The tasks ranged from navigating the homepage to performing specific 
content retrieval exercises. A significant aspect of these sessions was the open-ended exploration 
phase, allowing experts to freely interact with the portal, thus providing holistic feedback on the 
overall user experience. Th e results from the co -design sessions indicated overall satisfaction 
with the simplicity of completing the proposed tasks, as shown in Figure 17. However, there 
were mixed responses regarding the ease of finding the necessary features to accomplish tasks 
(Figure 18), suggesting room for improvement in navigability and feature accessibility. 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
77 
 
Figure 17. Despite tasks increasing complexity, the success rate is always high (1 = Very easy; 5 = Very 
difficult) 
Participants were active in reporting not just on task completion but also in identifying bugs or 
issues, contributing 38 messages encompassing comments, issues, and suggestions. This 
proactive feedback was instrumental in uncovering technical challenges and system errors. As a 
result, substantial modifications were made to the original prototypes. These changes were 
focused on enhancing user experience by simplifying the design, such as highlighting keywords 
throughout the portal for intuitive navigation a nd dividing filters in search sections into 
subcategories with a reset option. Further, to avoid confusion, clickable and non -clickable 
elements were distinctly differentiated. To manage content presentation and prevent cognitive 
overload, pagination options like “Load more” were implemented. Cross-browser issues were 
also addressed, ensuring a consistent user experience across different platforms. 
Moreover, the lexicon used in titles, subtitles, and paragraphs was refined based on expert 
feedback, as were the names of the five main categories: genres, artists, music, places, and 
instruments. These categories serve as primary entry points into the Po lifonia data, and their 
optimization was crucial for enhancing user interaction with the portal. The group discussions 
provided collective opinions and identified common desires and preferences. This qualitative 
approach was particularly revealing, uncovering aspects of user perception that might not have 
been evident in the more structured, task-based performances. Importantly, it shed light on the 
design of generous interfaces – those which encourage serendipitous discovery and exploration 
without assuming the user has a specific goal in mind. This insight was pivotal in framing UI/UX 
elements that cater to a broad range of user interactions with the portal. Overall, the combination 
of quantitative and qualitative feedback from the co-design sessions led to the understanding of 
user needs and preferences, guiding significant improvements in the web portal ’s design and 
functionality. The collaborative approach not only pinpointed usability issues but also provided 
a clear direction for enhancements, resulting in a more intuitive, user-friendly, and effective web 
portal. 


Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
78 
 
Figure 18. Features to accomplish tasks are easy to find regardless of their complexity (1 = Very easy; 5 = 
Very difficult) 
Discussion 
We established a process that integrates ontology requirements into UI/UX design for two main 
purposes: (1) to generate ideas and prototypes aligned with data needs, and (2) to allow the 
UI/UX design to continually adapt and refine these ontology requireme nts. By conducting 
exploratory analysis of Competency Questions, we gained insights into data needs and 
established priority areas. Analysing data patterns helped us anticipate types of content 
interactions and their significance. Additionally, user studie s focusing on competitive analysis 
and co-design methods aided in adjusting our services to meet the expectations of a diverse user 
base, from experts to novices. Our initial findings support two key hypotheses: (1) CQs with 
similar interaction patterns can be categorised together; (2) entities significant in numerous CQs 
tend to be important to a broad user spectrum. Consequently, this allows us to apply our 
workflow to a reduced set of CQ groupings rather than individual personas, thus saving time. 
By systematically aligning user requirements with data and ontology requirements, we ensure 
that the resulting interfaces are user -friendly and semantically rich, facilitating more effective 
information-seeking, exploration, and discovery. There are several potential benefits for Digital 
Humanities (DH) applications. The methodology’s foundation on LOD principles ensures that 
data from various sources can be seamlessly integrated. This is particularly beneficial for DH 
projects, which often involve diverse and heterogeneous datasets belonging to cultural heritage 
institutes and research projects. The adoption of our methodology in DH projects – or, broadly, 
in web environments targeted on the cultural heritage domain – allows one to enhance the 
usability of data, facilitate connections across domains, foster the design of coherent and efficient 
user interfaces for information seeking, and enable serendipitous discoveries at the same time. 
Our approach significantly improves user engagement by leveraging user-centric design practices 
from both the HCI field and design thinking methodologies. This is crucial in DH applications 
where user interaction with the content is a key aspect of the research process. Using personas, 
user stories, and competency questions h elps us to ensure that interfaces are tailored to the 


Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
79 
specific needs and preferences of various user groups. Moreover, one of the notable challenges 
in DH is enabling users to discover unexpected connections and insights. Our methodology ’s 
emphasis on creating generous interfaces that balance retention and overview can significantly 
enhance the user ’s ability to explore and discover new information serendipitously. This is 
particularly relevant for projects dealing with cultural heritage, literature, and historical archives. 
While our process of integrating ontology requirements into UI/UX design has shown 
promising results, it is important to acknowledge its limitations to provide a balanced view. 
Firstly, the dependency on the quality and comprehensiveness of the exploratory  analysis of 
Competency Questions is a significant limitation. If the CQs are not well-formulated or if they 
fail to cover the full spectrum of the data and user needs, the user journeys – addressed in the 
insights and priority areas of the proposed prototype - may be incomplete or skewed. This could 
also lead to a misalignment between the ontology requirements and the actual expectations of 
the target user. Secondly, the approach relies heavily on iterative refinement based on user 
feedback and data patter n analysis. While this iterative process can be considered one of the 
strengths of the process and hence of the result, it can also be time -consuming and resource-
intensive. Small-scale projects or those with limited resources may find it challenging to engage 
in multiple iterations of design and testing. Furthermore, our hypothesis that CQs with similar 
interaction patterns can be categorised together and that entities significant in numerous CQs 
are important to a broad spectrum of users, while supported by these findings, may not hold 
true in all contexts. The methodology has been so far tested for designing interfaces for the 
exploration of music and cultural heritage, generating three rather different types of application, 
namely: a crowdsourced catalogue, a data story editor, and a web portal for knowledge discovery. 
However, it may require adjustments when applied to different domains (e.g. hard sciences). In 
such contexts, different user groups may have unique interaction patterns or prioritize different 
entities, which our methodology might not capture. Future research and development should 
aim to address these challenges, refining the methodology to make it more robust and scalable 
to a wider range of projects and user requirements. 
Conclusion 
The study demonstrates that the integration of ontology design with UI/UX decision-making is 
a powerful strategy for overcoming challenges in projects focused on the dissemination of 
cultural heritage data. This innovative approach, bridging the gap between data analysis and user 
interface design, has shown its potential in enhancing user experience while ensuring the accurate 
representation of complex data structures. 
In the next future, we plan to conduct extensive monitoring activities on the Web portal to 
estimate user engagement and evaluate user journeys. Analysing how users interact with the 
portal will provide us valuable insights into the effectiveness of our UI/UX designs and ontology 
structures. This will not only help in refining our current methodologies but also assist in creating 
more user-centric designs in future projects. 
The successful application of this methodology in our case study serves as a preliminary 
validation of its effectiveness. By employing this strategy in the development of diverse 
applications – a digital catalogue, an authoring platform, a linguistic corpus interface, and a web 
portal designed for engaging the general public – we have witnessed firsthand its versatility and 
impact. Each application, catering to different user needs and interaction styles, benefitted from 
the nuanced understanding of data and user requirements facilitated by our approach. 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
80 
Looking to the future, we aim to expand the application of our methodology beyond its current 
scope. We plan to test its applicability in a variety of scenarios to further establish its adaptability 
and effectiveness. This expansion will not only validate the methodology in contexts other than 
cultural heritage but will also provide insights into its scalability and adaptability to different data 
scales and user demographics. Understanding how our approach scales with larger datasets, more 
complex ontologies, and diverse user groups is essential for its application in large-scale projects. 
We are particularly interested in investigating how the methodology can be adapted for big data 
environments and how it performs under the pressure of rapidly changing data landscapes and 
user demands. 
The initial success of integrating ontology design with UI/UX decisions in cultural heritage 
projects is just the beginning. Our future efforts aim to broaden the scope, increase the 
scalability, and deepen the sophistication of this approach, making it a useful tool in the field of 
data-intensive application design. 
Acknowledgments 
This work is supported by a project that has received funding from the European Union ’s 
Horizon 2020 research and innovation programme under grant agreement No 101004746 
(Polifonia: a digital harmoniser for musical heritage knowledge, H2020 -SC6-
TRANSFORMATIONS).  
References 
[1] Amna, Anis R, and Geert Poels. 2022. ‘Ambiguity in User Stories: A Systematic 
Literature Review’. Information and Software Technology  145. 
https://doi.org/10.1016/j.infsof.2022.106824 
[2] Bakaev, Maxim, and Tatiana Avdeenko. 2010. ‘Ontology to Support Web Design 
Activities in E -Commerce Software Development Process’. In Proceedings of the 
IASTED International Conference on Automation, Control, and Information Technology -
Information and Communication Technology, ACIT -ICT, 241 –48. 
http://dx.doi.org/10.2316/P.2010.691-075. 
[3] Bakaev, Maxim, and Martin Gaedke. 2016. ‘Application of Evolutionary Algorithms 
in Interaction Design: From Requirements and Ontology to Optimized Web 
Interface’. In 2016 IEEE NW Russia Young Researchers in Electrical and Electronic 
Engineering Conference (EIConRusNW) , 129 –34. IEEE. 
https://doi.org/10.1109/EIConRusNW.2016.7448138. 
[4] Bellucci, Andrea, Giulio Jacucci, Veera Kotkavuori, Bariş Serim, Imtiaj Ahmed, and 
Salu Ylirisku. 2015. ‘Extreme Co -Design: Prototyping with and by the User for 
Appropriation of Web-Connected Tags’. In End-User Development, edited by Paloma 
Díaz, Volkmar Pipek, Carmelo Ardito, Carlos Jensen, Ignacio Aedo, and Alexander 
Boden, 109 –24. Cham: Springer International Publishing. 
https://doi.org/10.1007/978-3-319-18425-8_8. 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
81 
[5] Benford, Steve, Gabriella Giannachi, Boriana Koleva, and Tom Rodden. 2009. ‘From 
Interaction to Trajectories: Designing Coherent Journeys through User Experiences’. 
In Proceedings of the Sigchi Conference on Human Factors in Computing Systems , 709 –18. 
https://doi.org/10.1145/1518701.1518812. 
[6] Berners-Lee, Tim, James Hendler, and Ora Lassila. 2001. ‘The Semantic Web’. 
Scientific American 284 (5): 34–43. 
[7] Bevan, Nigel, Jim Carter, Jonathan Earthy, Thomas Geis, and Susan Harker. 2016. 
‘New ISO Standards for Usability, Usability Reports and Usability Measures’. In 
Human-Computer Interaction. Theory, Design, Development and Practice: 18th International 
Conference, HCI International 2016, Toronto, ON, Canada, July 17 -22, 2016. Proceedings, 
Part I 18 , edited by Masaaki Kurosu, 268 –78. Lecture Notes in Computer Science, 
vol 9731, Springer. https://doi.org/10.1007/978-3-319-39510-4_25. 
[8] Brown, Tim. 2008. ‘Design Thinking’. Harvard Business Review 86 (6): 84. 
[9] Carriero, Valentina Anita, Aldo Gangemi, Maria Letizia Mancinelli, Andrea Giovanni 
Nuzzolese, Valentina Presutti, and Chiara Veninata. 2021. ‘Pattern-Based Design 
Applied to Cultural Heritage Knowledge Graphs’. Semantic Web  12 (2): 313 –57. 
https://doi.org/10.3233/SW-200422. 
[10] Charalampidis, Charalampos C, and Euclid A Keramopoulos. 2018. ‘Semantic Web 
User Interfaces–A Model and a Review’. Data & Knowledge Engineering  115:214–27. 
https://doi.org/10.1016/j.datak.2018.04.003. 
[11] Chasanidou, Dimitra, Andrea Alessandro Gasparini, and Eunji Lee. 2015. ‘Design 
Thinking Methods and Tools for Innovation’. In Design, User Experience, and 
Usability: Design Discourse: 4th International Conference, DUXU 2015, Held as 
Part of HCI International 2015, Los Angeles, CA, USA, August 2 –7, 2015, 
Proceedings, Part I , 12 –23. Springer. https://doi.org/10.1007/978-3-319-20886-
2_2. 
[12] Cooper, Alan. 1999. ‘The Inmates Are Running the Asylum ’. In Software-Ergonomie 
‘99: Design von Informationswelten, edited by Udo Arend, Edmund Eberleh, and Knut 
Pitschke, 17 –17. Wiesbaden: Vieweg+Teubner Verlag. 
https://doi.org/10.1007/978-3-322-99786-9_1.  
[13] Cota, Giuseppe, Marilena Daquino, and Gian Luca Pozzato. 2020. Applications and 
Practices in Ontology Design, Extraction, and Reasoning . Vol. 49. Studies on the Semantic 
Web. IOS Press. 
[14] Dermeval, Diego, Jéssyka Vilela, Ig Ibert Bittencourt, Jaelson Castro, Seiji Isotani, 
Patrick Brito, and Alan Silva. 2016. ‘Applications of Ontologies in Requirements 
Engineering: A Systematic Review of the Literature’. Requirements Engineering 21:405–
37. https://doi.org/10.1007/s00766-015-0222-6. 
[15] Domingo, M. 2021. ‘User Stories: As a [UX Designer] I Want to [Embrace Agile] so 
That [I Can Make My Projects User -Centered]’. Interaction Design Foundation - IxDF. 
https://www.interaction-design.org/literature/article/user-stories-as-a-ux-des 
igner-i-want-to-embrace-agile-so-that-i-can-make-my-projects-user-centered. 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
82 
[16] Dorst, Kees. 2011. ‘The Core of ‘Design Thinking’ and Its Application’. Design Studies, 
Interpreting Design Thinking , 32 (6): 521 –32. 
https://doi.org/10.1016/j.destud.2011.07.006. 
[17] Gangemi, Aldo, and Valentina Presutti. 2009. ‘Ontology Design Patterns’. In 
Handbook on Ontologies , edited by Steffen Staab and Rudi Studer, 221 –43. Berlin, 
Heidelberg: Springer. https://doi.org/10.1007/978-3-540-92673-3_10. 
[18] Gruber, Marc, Nick De Leon, Gerard George, and Paul Thompson. 2015. ‘Managing 
by Design’. Academy of Management Journal 58(1): 1 -7. 
https://doi.org/10.5465/amj.2015.4001. 
[19] Gruen, Dan, Thyra Rauch, Sarah Redpath, and Stefan Ruettinger. 2002. ‘The Use of 
Stories in User Experience Design’. International Journal of Human-Computer Interaction 
14 (3–4): 503–34. https://doi.org/10.1080/10447318.2002.9669132. 
[20] Gruninger, Michael. 1995. ‘Methodology for the Design and Evaluation of 
Ontologies’. In Proc. IJCAI’95, Workshop on Basic Ontological Issues in Knowledge Sharing. 
Montreal. 
[21] Hitzler, Pascal. 2021. ‘A Review of the Semantic Web Field’. Communications of the 
ACM 64 (2): 76–83. https://doi.org/10.1145/3397512. 
[22] Hoeber, Orland, and Xue Yang. 2007. ‘User -Oriented Evaluation Methods for 
Interactive Web Search Interfaces’. In In 2007 IEEE/WIC/ACM International 
Conferences on Web Intelligence and Intelligent Agent Technology - Workshops, 239 –43. 
https://doi.org/10.1109/WI-IATW.2007.28. 
[23] Hyvönen, Eero. 2020. ‘Using the Semantic Web in Digital Humanities: Shift from 
Data Publishing to Data-Analysis and Serendipitous Knowledge Discovery’. Semantic 
Web 11 (1): 187–93. https://doi.org/10.3233/SW-190386. 
[24] Junior, Plinio Thomaz Aquino, and Lucia Vilela Leite Filgueiras. 2005. ‘User 
Modeling with Personas’. In Proceedings of the 2005 Latin American Conference on Human-
Computer Interaction, 277–82. https://doi.org/10.1145/1111360.1111388. 
[25] Kaiya, Haruhiko, Hisayuki Horai, and Motoshi Saeki. 2002. ‘AGORA: Attributed 
Goal-Oriented Requirements Analysis Method’. In Proceedings IEEE Joint International 
Conference on Requirements Engineering , 13 –22. 
https://doi.org/10.1109/ICRE.2002.1048501. 
[26] Kiruthika, Jay, Souheil Khaddaj, Darrel Greenhill, and Jarek Francik. 2016. ‘User 
Experience Design in Web Applications’. In 2016 IEEE Intl Conference on 
Computational Science and Engineering (CSE) and IEEE Intl Conference on 
Embedded and Ubiquitous Computing (EUC) and 15th Intl Symposium on 
Distributed Computing and Applications for Business Engineering (DCABES), 642–
46. IEEE. https://doi.org/10.1109/CSE-EUC-DCABES.2016.253. 
[27] Konstantakis, Markos, and George Caridakis. 2020. ‘Adding Culture to UX: UX 
Research Methodologies and Applications in Cultural Heritage’. Journal on Computing 
and Cultural Heritage (JOCCH) 13 (1): 1–17. https://doi.org/10.1145/3354002. 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
83 
[28] Laubheimer, Page. 2020. ‘3 Persona Types: Lightweight, Qualitative, and Statistical’. 
Nielsen Norman Group. https://www.nngroup.com/articles/persona-types/. 
[29] Law, Effie, Virpi Roto, Arnold POS Vermeeren , Joke Kort, and Marc Hassenzahl. 
2008. ‘Towards a Shared Definition of User Experience’. In CHI’08 Extended Abstracts 
on Human Factors in Computing Systems , 2395 –98. 
https://doi.org/10.1145/1358628.1358693. 
[30] Liedtka, Jeanne. 2017. ‘Evaluating the Impact of Design Thinking in Action’. In 
Academy of Management Proceedings , 2017:10264. Academy of Management Briarcliff 
Manor, NY 10510. https://doi.org/10.5465/AMBPP.2017.177. 
[31] Liedtka, Jeanne, and Tim Ogilvie. 2011. Designing for Growth: A Design Thinking Tool 
Kit for Managers. New York: Columbia University Press. 
[32] Manning, Christopher D., Prabhakar Raghavan, and Hinrich Schütze. 2008. 
Introduction to Information Retrieval . Cambridge University Press. 
https://doi.org/10.1017/CBO9780511809071. 
[33] Meghini, Carlo, Valentina Bartalesi, Daniele Metilli, and Filippo Benedetti. 2019. 
‘Introducing Narratives in Europeana: A Case Study’. International Journal of Applied 
Mathematics and Computer Science 29 (1). http://dx.doi.org/10.2478/amcs-2019-0001. 
[34] Melo, Amanda Meincke, and M. Cecília C. Baranauskas. 2006. ‘AN INCLUSIVE 
APPROACH TO COOPERATIVE EVALUATION OF WEB USER 
INTERFACES’. In Proceedings of the Eighth International Conference on Enterprise 
Information Systems - Volume 5: ICEIS,  65–70. SciTePress. 
https://doi.org/10.5220/0002445500650070. 
[35] Nielsen, Jakob. 1994a. ‘Goal Composition: Extending Task Analysis to Predict 
Things People May Want to Do’. Nielsen Norman Group.  
https://www.nngroup.com/articles/goal-composition/. 
[36] ———. 1994b. ‘Guerrilla HCI: Using Discount Usability Engineering to Penetrate 
the Intimidation Barrier’. In Cost-Justifying Usability, 245–72. USA: Academic Press, 
Inc. 
[37] Norman, Don. 2013. The Design of Everyday Things: Revised and Expanded 
Edition. New York: Basic books. 
[38] Noy, Natalya Fridman, and Carole D Hafner. 1997. ‘The State of the Art in Ontology 
Design: A Survey and Comparative Review’. AI Magazine  18 (3): 53 –53. 
https://doi.org/10.1609/aimag.v18i3.1306. 
[39] Paulheim, Heiko, and Florian Probst. 2013. ‘UI 2 Ont—A Formal Ontology on User 
Interfaces and Interactions’. Semantic Models for Adaptive Interactive Systems , 1 –24. 
https://doi.org/10.1007/978-1-4471-5301-6_1. 
[40] Peroni, Silvio, Francesca Tomasi, and Fabio Vitali. 2013. ‘Reflecting on the 
Europeana Data Model’. In Digital Libraries and Archives: 8th Italian Research 
Conference, IRCDL 2012, Bari, Italy, February 9-10, 2012, Revised Selected Papers 
8, 228–40. Communications in Computer and Information Science (354). Springer, 
Berlin, Heidelberg. https://doi.org/10.1007/978-3-642-35834-0_23. 

Umanistica Digitale – ISSN: 2532-8816 – n. 18, 2024 
   
 
84 
[41] Pileggi, Salvatore F. 2021. ‘Knowledge Interoperability and Re -Use in Empathy 
Mapping: An Ontological Approach’. Expert Systems with Applications  180:115065. 
https://doi.org/10.1016/j.eswa.2021.115065. 
[42] Presutti, Valentina, Enrico Daga, Aldo Gangemi, and Eva Blomqvist. 2009. ‘eXtreme 
Design with Content Ontology Design Patterns’. Proceedings of the 2009 International 
Conference on Ontology Patterns - Volume 516, 83–97. WOP’09. Aachen, DEU: CEUR-
WS.org. https://ceur-ws.org/Vol-516/. 
[43] Ramaprasad, Arkalgud, and Thant Syn. 2014. ‘Design Thinking and Evaluation Using 
an Ontology’. In Design Science: Perspectives from Europe, edited by Markus Helfert, Brian 
Donnellan, and Jim Kenneally, 63 –74. Cham: Springer International Publishing. 
https://doi.org/10.1007/978-3-319-13936-4_6. 
[44] Rosala, Maria. 2020. ‘Task Analysis: Support Users in Achieving Their Goals’. Nielsen 
Norman Group. https://www.nngroup.com/articles/task-analysis/. 
[45] Rowe, Peter G. 1991. Design Thinking. Cambridge: MIT press. 
[46] Salazar, Kim. 2020. ‘Contextual Inquiry: Inspire Design by Observing and 
Interviewing Users in Their Context’. Nielsen Norman Group . 
https://www.nngroup.com/articles/contextual-inquiry/. 
[47] Shibaoka, Masayuki, Haruhiko Kaiya, and Motoshi Saeki. 2007. ‘GOORE: Goal -
Oriented and Ontology Driven Requirements Elicitation Method’. In Advances in 
Conceptual Modeling–Foundations and Applications, edited by Jean-Luc Hainaut, Elke A. 
Rundensteiner, Markus Kirchberg, Michela Bertolotto, Mathias Brochhausen, Yi -
Ping Phoebe Chen, Samira Si-Saïd Cherfi, et al., 225–34. Berlin, Heidelberg: Springer. 
https://doi.org/10.1007/978-3-540-76292-8_28. 
[48] Shneiderman, Ben. 1996. ‘The Eyes Have It: A Task by Data Type Taxonomy for 
Information Visualizations’. In Proceedings 1996 IEEE Symposium on Visual Languages, 
336–43. IEEE. https://doi.org/10.1109/VL.1996.545307. 
[49] Silva, Thiago Rocha, Jean-Luc Hak, and Marco Winckler. 2017. ‘A Formal Ontology 
for Describing Interactive Behaviors  and Supporting Automated Testing on User 
Interfaces’. International Journal of Semantic Computing  11 (04): 513 –39. 
https://doi.org/10.1142/S1793351X17400219. 
[50] Sim, Wee Wee, and Peggy Brouse. 2014. ‘Towards an Ontology -Based Persona -
Driven Requirements and Knowledge Engineering’. Procedia Computer Science , 
Complex Adaptive Systems Philadelphia, PA November 3-5, 2014, 36 (January):314–
21. https://doi.org/10.1016/j.procs.2014.09.099. 
[51] Souza, Pedro Lopes de, Antonio Francisco do Prado, Wanderley Lopes de Souza, 
Sissi Marilia dos Santos Forghieri Pereira, and Luís Ferreira Pires. 2018. ‘Improving 
Agile Software Development with Domain Ontologies’. In Information Technology-New 
Generations: 15th International Conference on Information Technology,  edited by Shahram 
Latifi, 267–74. Cham: Springer International Publishing. 
https://doi.org/10.1007/978-3-319-77028-4_37. 
 

Grasso, Daquino, Renda – From Ontology Design to User Experience 
   
85 
[52] Suárez-Figueroa, Mari Carmen, Asunción Gómez -Pérez, and Mariano Fernandez -
Lopez. 2015. ‘The NeOn Methodology Framework: A Scenario-Based Methodology 
for Ontology Development’. Applied Ontology  10 (2): 107 –45. 
https://doi.org/10.3233/AO-150145. 
[53] Thamrongchote, Chaleerat, and Wiwat Vatanawood. 2016. ‘Business Process 
Ontology for Defining User Story’. In 2016 IEEE/ACIS 15th International Conference 
on Computer and Information Science (ICIS) , 1 –4. IEEE. 
https://doi.org/10.1109/ICIS.2016.7550829. 
[54] Whitelaw, Mitchell. 2015. ‘Generous Interfaces for Digital Cultural Collections’. 
Digital Humanities Quarterly  9 (1). 
https://www.digitalhumanities.org/dhq/vol/9/1/000205/000205.html. 
[55] Yang, Lan, Kathryn Cormican, and Ming Yu. 2019. ‘Ontology -Based Systems 
Engineering: A State -of-the-Art Review’. Computers in Industry  111:148–71. 
https://doi.org/10.1016/j.compind.2019.05.003. 
 
 
 
```
