---
title: Final Designing a User Interface for Provenance Reporting of Objects with Colonial Heritage
author:
  - Isabella Abelardo
year: "2024"
Type: Master thesis
DOI: ""
source: ""
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - tech/provenance
  - Humanities/culturalHeritage
  - design/UX
  - humanities/EJ
pdfORepub: "[[Final_Designing_a_User_Interface_for_Provenance_Reporting_of_Objects_with_Colonial_Heritage.pdf]]"
---
[[Final_Designing_a_User_Interface_for_Provenance_Reporting_of_Objects_with_Colonial_Heritage.pdf]]
## Full text (extracted from `Final_Designing_a_User_Interface_for_Provenance_Reporting_of_Objects_with_Colonial_Heritage.pdf`)

*Source:* `2PDF/Final_Designing_a_User_Interface_for_Provenance_Reporting_of_Objects_with_Colonial_Heritage.pdf`  
*Extracted:* 2026-04-24

```text
Master Thesis
Designing a User Interface for Provenance Reporting of Objects
with Colonial Heritage
by
Isabella Abelardo
(zwy251)
First supervisor: Victor de Boer
Daily supervisor: Sarah Binta Alam Shoilee
Second reader: Jacco van Ossenbruggen
July 16, 2024
Submitted in partial fulfillment of the requirements for
the VU degree of Master of Science in Information Sciences

DECLARATION OF AUTHORSHIP
Use one declaration for each author.
I, Isabella Abelardo, declare that this thesis titled, Designing a User Interface for Provenance Reporting of Objects with Colonial
Heritage and the work presented in it are my own. I confirm that:
• This work was done wholly or mainly while in candidature for a research degree at this University.
• Where any part of this thesis has previously been submitted for a degree or any other qualification at this University or any other
institution, this has been clearly stated.
• Where I have consulted the published work of others, this is always clearly attributed.
• Where I have quoted from the work of others, the source is always given. With the exception of such quotations, this thesis is entirely
my own work.
• I have acknowledged all main sources of help.
• Where the thesis is based on work done by myself jointly with others, I have made clear exactly what was done by others and what I
have contributed myself.
Signed:
Date: 16 July 2024
2


Designing a User Interface for Provenance Reporting of Objects
with Colonial Heritage
Isabella Abelardo
Vrije Universiteit Amsterdam
Amsterdam, The Netherlands
i.abelardo@student.vu.nl
ABSTRACT
Context. Currently it is a challenge within cultural institutions to
represent multiple perspectives for colonial heritage items. An ex-
ample of such perspectives appear in provenance reports, which
are documented findings relating to the provenance history of an
object. When provenance reports about colonial heritage items are
written, by design of the information system, the information that
is being stored results in a ‘singular or flattening of truth’ regard-
ing the item. Furthermore, the current method of capturing this
information is unstructured, therefore not allowing for findability
and the reusability of such information.
Goal. The aim of this research paper is to provide a set of require-
ments which are actualised through a user interface to enable prove-
nance researchers to holistically document provenance reports
digitally. Specifically, it concerns the documentation of polyvocal
knowledge that are often present for objects with colonial heritage.
Method. Four semi-structured interviews with provenance researchers
were conducted to elicit design requirements. A user interface was
then built to represent these requirements which were then eval-
uated by two provenance researchers through task-oriented user
tests.
Results. The results showed that to a moderate degree, provenance
researchers found CultureSource fit for purpose and were able to
some extent document polyvocal knowledge.
Conclusions. The research provides a set of requirements (standard-
isation, multiple perspectives, usability, and data management) for
future work in creating user interfaces that involve the documenta-
tion of multiple truths.
1 INTRODUCTION
1.1 Context
Cultural institutions are increasingly adopting technologies from
the Semantic Web to enrich the findability, accessibility, interop-
erability, and reusability of cultural information [1]. The creation
of knowledge representation models such as CIDOC-CRM have al-
lowed the continual documentation of cultural heritage data. Within
the museum context, there have been great strides in the transfor-
mation of unstructured text and documentation into Linked Data.
This can be seen, for example, through the Rijksmuseum Amster-
dam’s collection datasets that are available for public use.
An important aspect of the cataloguing of information for cul-
tural heritage objects is object provenance. Provenance within the
museum context is the description of an object’s ownership history,
which includes information such as its discovery, relevant contex-
tual information, and collection movement [3]. Object provenance
is especially regarded in relation to objects that have colonial her-
itage history. As documentation methods and museum technologies
improve, more contextual information comes to light about these
objects. Within the context of colonialism and its space within
the museum context, it is an ongoing discussion and questioning
of what is normalised and standardised museum practice ([ 13],
[15]). European conceptualisations of heritage conservation have
been assimilated into cultural institutions worldwide and can be
interpreted as a form of cultural imperialism and continuation of
colonialism in the modern day [ 10]. The inclusion of contextual
information with multiple voices or narratives is important to the
historical documentation of objects, and is a way of ‘decolonising
the database’ [13], so that they are given accurate acknowledgement
and representation.
Provenance researchers are continually aiming to represent and
incorporate new and/or underrepresented perspectives within their
work. In many cases, colonial objects within museum collections
may have multiple cultural origins, dates, or periods that they
belong to as more research has been conducted. In this way, this
paper investigates how a user interface can be designed to support
the input of such perspectives.
1.2 Motivation
1.2.1 Provenance reporting in The Museum System (TMS).When
provenance researchers digitise their research on objects in TMS,
provenance information is relegated to one to two open text fields,
as seen in Figure 2. In the management of objects for example, there
are cases where the object has multiple origins, or they are unsure
whether a culture is related to the object but is worth noting for
future work. This information has to be placed somewhere within
TMS, but there are no designated fields for this type of information
and is relegated to being included as free open text as part of the
‘provenance’ field. Information relegated to text fields such as these
constricts the breadth and depth of the research being performed
and its potential for reusability, accessibility, and findability [1].
1.2.2 Reflecting multiple perspectives for objects with colonial her-
itage. Objects with colonial heritage and their subsequent treat-
ment and handling are ongoing discussions within cultural institu-
tions. Perspectives on an object with a colonial history as they are
recorded from a Western cultural classification or framework are
not the only way of viewing and understanding that object [ 15].
This presence of many perspectives, or narratives that embody an
objects history is known as polyvocality [12]. TMS does not support
proper representations of polyvocal knowledge.
1.2.3 Linked Open Data. Provenance data is currently being writ-
ten in open, unstructured free text formats within TMS 2. This
1

Figure 1: Example of a Provenance Report[cite]
Figure 2: Provenance Entry in TMS [7]
greatly inhibits the searchability and reusability of that informa-
tion when it is read by other domain experts. It is no different to
reading the actual written report itself. Having object provenance
data transformed into linked data allows for the further analysis
of patterns on the circulation, networks, and trends of objects ([7],
[1]). It also lowers the upkeep of information required when object
entities are referenced and linked [7]. In providing a way for do-
main experts to input their data into a system that transforms it
into linked data, the data becomes machine readable and removes
the shortcomings of open text entry.
1.3 Research Questions
The research questions are as follows:
RQ1: What are the design requirements for a user interface that
allows provenance researchers to record their provenance reports?
RQ2: To what extent is the user interface fit for purpose, i.e. the
expression of polyvocality of objects with colonial heritage?
2 BACKGROUND
2.1 The Museum System (TMS)
Many museums use a web-based information system called ‘The
Museum System’ (TMS), which is a collection management software
that handles data relating to museum collections. This includes and
is not limited to object information, exhibitions, archival records,
people, and institutional information. Provenance researchers write
reports on their research findings on objects, such as in Figure 1.
These reports can be numerous pages, depending on the breadth
of the research on the object, and the report style is subject to
the needs of the research project or the museum standards the
provenance researcher adheres to.
TMS contains many fields to input various types of information
relating to objects, people, media, institutions etc. However, as TMS
is a system that is used by other domain experts besides provenance
researchers, such as curators and registrars, information that is
digitised into TMS are placed in singular text fields.
2.2 Polyvocal Knowledge
Polyvocality as a concept seeks to showcase that there is no author-
itative or singularly correct narrative for describing heritage, but is
a multi-faceted and multi-dimensional perspective for viewing and
understanding heritage objects [12].
A famous example is the object ‘Tipu’s Tiger’. It was a com-
missioned tiger-shaped musical automaton that was intended to
symbolise the rule of Tipu Sultan, the ruler of the Kingdom of
Mysore who had allied with France as a means of combating the
expansion of the East India Company in the mid to late 1700s [11].
This object was seized in 1799 when British forces pillaged and
looted Tipu’s city and was brought to London, which quickly gar-
nered attention from the public and was viewed as a symbol of
British victory over India, and by extension, France [ 11]. Conse-
quently, the response by the public and the press, along with its
violent method of transfer had altered the meaning of the object
in a completely different way. What was written in the historical
notes by the Victoria and Albert Museum at the time indicated a
perspective that spoke of Orientalism and a ‘restoration of order’ in
India. This perspective, while in many accounts, is a representation
of the events that occurred in the collection of the object, is also
not completely historically representative of the object. Prior to its
looting, it was seen by Indians as a symbol of colonial resistance as
well as a peak in technical craftmanship at the time [11].
Within objects with colonial heritage, the histories are neither
static nor singular but have plurality [ 12]. It is in this polyvocal
knowledge that there is a difficulty in digitising them within TMS in
a way that does not ‘create a singular truth’ about the object ([12],
[15]). That is, when information is placed in TMS, the exact field
it is placed implies certain documentation choices which become
truths for the domain experts that read them.
3 RELATED WORK
3.1 Modelling for polyvocality
The study by Shoilee et al. [ 9] creates a data model to represent
polyvocal provenance data of ethnographic heritage objects. It
investigates which Semantic Web solutions are appropriate for
2

recording polyvocal knowledge. Requirements for the data model
were made and then applied to ethnographic objects to exhibit their
chain of custody [ 9]. This resulted in a knowledge graph which
was validated with competency questions. This study by Shoilee
et al. overlaps with this paper in terms of its goal in representing
polyvocal information. The future work mentioned in that paper
also forms the motivation of this paper. To suggest the possibility of
creating a tool that facilitates the domain expert to input polyvocal
information that supports and allows for data modelling.
Tsenova et al. ’s [12] paper creates and describes a design for a
networked storytelling cabinet that plays audio-video stories for
visitors at a heritage site. The aim of the design was to further
the research done in representing polyvocality within cultural her-
itage sites. The research project took place at Seaton Delaval Hall
(SDH), a Baroque country house within the UK. This country house,
as a place of cultural heritage, has witnessed subsequent changes
within the last 60 years and the interpretations of its provenance
are diverse. A set of concepts were devised to position the design
to model polyvocality and its incorporation into a physical infor-
mation display about SDH. Tsenova et al. ’s work differs from this
paper as its approach to modelling polyvocality is directed to a
more social purpose. To redirect from ‘pre-constituted narratives
and histories’ [12] but to one of an understanding that polyvocality
in the present is also performed and understood by the audience.
3.2 Provenance and Colonial Heritage
Rother et al. ’s [7] paper asserts that provenance data within muse-
ums should be connected through Linked Open Data. It discusses
the development of Linked Art as a data model to express the
needs of museums of creating Linked Open Data with a focus on
provenance [7]. The framework provided by Rother et al. serves
as a starting point for how cultural institutions can begin to trans-
form their data into a linkable network. This framework, similar
to Shoilee et al. [9], provides a support for this paper as the goal
is to represent provenance data, especially those with contentious
colonial history and by extension, polyvcal history, in a machine
readable format. While Rother et al. ’s paper focuses on Linked Open
Data, its arguments against provenance being kept in unstructured
text fields within TMS serves as a base for the conscious design
choices to be made for a UI to support provenance work.
3.3 User Interface Design
Goy et al. ’s [2] paper researches how to build a user interface for
representing historical archives through an ontology. They did a
user study to help define strategies to rank properties and relations
based on their relevance to certain events. A user interface was
then built, with ‘guided paths’ to illustrate the flow of how events
should be documented [2]. This research overlaps with Goy et al.
in CultureSource, while not forcing a user to use all fields and
properties, lightly enforces a uniformity in the user interface. It
also differs in that the UI in Goy et al. is for the documentation
of events that have occurred and are mentioned within historical
archives, whilst the scope of CultureSource is narrowed to mainly
objects and persons/institutions.
The Provenance Lab at Leuphana University developed Prova
[14], a provenance app designed to assist museum professionals
transform their provenance into structured data. The app uses wiki-
data ID’s to retrieve object information, then users are able to input
assertions and provenance activities within the app in a structured
format. This overlaps with the research for this paper significantly,
both in terms of goals and execution. The main differences being
that Prova is designed for museum professionals, not provenance
researchers specifically. While the focus of Prova is on activities,
CultureSource also includes semantic search ability and fields to
allow for multiple inputs for singular fields (such as name, culture,
etc.).
Prasanna et al. ’s [6] study on prototyping software to support
fire emergency response discusses how to present information to
firefighters to heighten situation awareness and is, further, a user
interface study. The study claims that time-sensitive emergencies
(such as house fires) require heightened situation awareness to
improve decision making [6]. The paper provides a set of steps to
be aware of to achieve heightened situation awareness within a
user interface (perception, comprehension, and projection) with
the aim completing successful demonstration sessions with fire-
fighters. While the subject focus is different between Prasanna et
al. ’s research and this paper, there is overlap in the methodology
for prototype evaluations. Guidelines that consist of following hy-
pothetical scenario’s are used for evaluation in both, with the aim
of receiving feedback to improve future iterations.
4 RESEARCH STRATEGIES AND RESEARCH
METHODS
4.1 Research Strategy
The aim of this research is to collect user interface feature require-
ments for the purpose of recording and maintaining provenance
reporting for objects with colonial heritage. To this aim, the design
science method framework developed by Johannesson and Perjons
[4] is followed, as seen in Figure 3.
4.1.1 Explicate Problem. As mentioned prior, the motivation for
this research is to generate a list of requirements in the form of
a user interface which will then be evaluated by provenance re-
searchers. Part of the research is investigating the gap between the
current state and the desired state. In the context of this paper, the
gap is solving the provenance researcher’s need for proper doc-
umentation of their provenance reporting that is both useful for
them as a researcher as well as being machine readable.
4.1.2 Define Requirements. In preparation for the primary study to
gather requirements, a pilot study was conducted with one prove-
nance researcher for the purpose of improving the interview ques-
tions and the efficiency of the main study. For the primary study,
semi-structured interviews will be conducted to gather the design
requirements needed to build the user interface. The interviews
serve to understand the current workflow, limitations, and user
needs of provenance researchers.
To ensure the primary study is suited to answer the research
questions, interview protocol matrices will be drawn for both the
pilot and the primary study. Thematic analysis will then be con-
ducted on the interview data to draw out the main themes using
the thematic analysis model by Naeem et al. [5] for the next step.
3

Secondary Research Pilot Study Semi-structured
interviews
User Testing and
Evaluation
Provenance ResearchersProvenance Researcher Provenance ResearchersExisting UI Literature
Research Questions Revised interview setting
Initial UI Prototype
UI Design Requirements
Prototype
User Testing results
Demonstrate & Evaluate ArtefactExplicate Problem Define Requirements
Build User Interface
Design & Develop Artefact
Functioning Paper Prototype
Evaluation Metrics Legend
Input/Output
Contribution
User Interface
Research phase
Input
Research action
Figure 3: Overview: Research strategy, research methods and results.
The main themes will turn into the requirements needed to develop
the artefact.
4.1.3 Design and Develop Artefact. An artefact will be built that
fulfills the requirements gathered from the previous step. Prelimi-
nary sketches will be drawn to provide a general overview of the
structure and functions of the artefact. As per the sketch and build
sub-activity within the design science framework, artefact building
also involves adapting from existing solutions and combining them
with new elements [4]. In this phase, other examples of provenance
annotation interfaces as well as TMS will be compared to and drawn
upon to create a better user interface for provenance researchers.
4.1.4 Demonstrate Artefact. Within the design science framework,
this step aims to prove the artefact’s feasibility [4]. The output is
descriptive and explanatory knowledge of the why and how of the
artefact’s use [4]. In this case, how does CultureSource solve the
problems as mentioned in 4.1.1.
4.1.5 Evaluate Artefact. To evaluate CultureSource, user testing
will be conducted. To answer RQ2 and to validate the requirements
answering RQ1, user testing results will provide an evaluation to
enhance and improve the requirements gathered from 4.1.2.
5 STUDY EXECUTION
5.1 Explicate Problem
To begin, secondary research is conducted to initially create the
design of the user interface. Five provenance reports under the
Pilotproject Provenance Research on Objects of the Colonial Era
(PPROCE) conducted by Rijksmuseum Amsterdam were analysed
to see the recurring patterns within each report and to understand
what fields will be required for the user interface. The wikidata-
based provenance web-application named PROVA, which serves to
record provenance data for cultural objects that have wikidata en-
tries, served as a basis and reference in how to create fields that are
design to be transformed into Linked Data, specifically in regards to
unstructured text and instances of multiple perspectives. Nanodash,
a client that is used to publish nano-publications also served as a
reference in the design and approach to semantic templates. Each
template served to publish a certain type of assertion, which also
proved helpful in the design of creating structured text fields out
of unstructured text.
The secondary research provided the understanding of the meth-
ods and structure required to build an interface that allows for
the transformation of unstructured text into structured data. This
feeds into research question one, wherein the design choices made
and incorporated into the user interface will allow provenance
researchers to conduct their reporting in a structured manner.
5.1.1 Pilot Interview & Primary Study.A pilot interview was done
to improve the design of the primary study. It was conducted with
a Senior provenance researcher. The pilot interview consisted of a
number of interview questions only, and was conducted in person
with an audio transcription. The pilot interview was done to refine
the interview protocol and validate the questions and method of
conducting the interview.
The primary study included a revision of one interview question
and the removal of one from the pilot study, as well as the integra-
tion of a system walk-through of TMS. Including a system walk
through was to enhance the understanding of the gaps between
current provenance annotation methods and the desired state of
documentation. A total of four provenance researchers were in-
terviewed: three current provenance researchers, and one former
provenance researcher.
The interviews were audio and video recorded with transcrip-
tions on Microsoft Teams. The first half of the interview was ded-
icated to the interview questions, while the latter half dedicated
to a walk-through of TMS. The interviewees were asked questions
regarding their work flow, challenges in recording accurate prove-
nance information in TMS, and what improvements they would
like to see to further assist their research documentation.
All interviewees were provided with an existing provenance
report (Figure 1) from the PPROCE project as a control to see com-
mon documentation difficulties and for consistency with behaviour
when interacting with TMS. The interviewees were asked to show
how that provenance report would be documented within TMS,
4

describing which sections within the report went into the fields in
TMS with justifications as to why they are placed there.
5.2 Define Requirements
To create a list of requirements, the transcriptions from the inter-
views were moved to an excel file across multiple sheets. A first
round of open coding was applied to the transcription to capture
the essence of each line. The second round then grouped the first
round of codes into smaller, more specific codes to capture the main
thematic messages and patterns found within the first round of
codes. The second round resulted in the following codes:
5.2.1 Lack of Standardisation. Lack of standardisation refers to the
lack of uniformity towards provenance reporting. All interviewees
mentioned the lack of standardised formats within both the act of
creating provenance reports as well as inputting that report within
TMS as an impediment to their work flow.
5.2.2 Documentation. Documentation refers to any participant
mention of how they put their provenance report into TMS. This in-
cludes how they put in their textual reporting, and what difficulties
interviewees had when inputting data into TMS.
5.2.3 Multiple Perspectives. Multiple Perspectives refers to the
discussion of how the interviewees tackled the issue of multiple
perspectives within their provenance reporting.
5.2.4 User Interaction. User Interaction refers to user contact with
TMS. Explicitly defined of the features and fields within TMS that
are mentioned to be used (or not used) within the system by the
interviewees. It also includes mentions of their capacity to complete
their provenance reporting to a satisfactory degree.
5.2.5 Searchability. Searchability refers to the ability to find some-
thing. Some interviewees mentioned that the ability to search for
specific objects, especially without inventory numbers, is difficult.
All interviewees also mention the need for an enhanced search
mechanism to create lists or for viewing a series of objects accord-
ing to certain criteria.
5.2.6 Traceability. Traceability refers to the ability for provenance
researchers to track and trace research within TMS. This includes
citing sources and being able to track the work that other re-
searchers have done on objects, people, and institutions.
5.2.7 Interconnectedness. Interconnectedness refers to the rela-
tional aspect and the linkability of data that provenance researchers
work with. All interviewees mentioned that being able to create
relations aids their research in viewing objects in context of people
and institutions.
5.2.8 Futureproofing. Futureproofing refers to the ability to place
information within a system that can still be accessed by future
researchers in spite of changes either software or from a change of
reporting style.
5.2.9 Other. An ’other’ code was made to categorise data that did
not conform to the other codes.
The third round involved the development of themes, taking the
general codes from the previous round to embody the meanings
DATA
'The problem that we have [...] is no clear structure'
'No unified system for doing all this'
'Reports are not uniform'
Lack of Standardisation
Documentation
User Interaction
Multiple Perspectives
Searchability
Traceability
Interconnectedness
Futureproofing
'Objects lost [...] because they weren't registered
properly'
'Look up the report and find the information there'
'The contextual information is difficult to add'
'I don't have options to add (more cultures)'
'Knowing the specific country but within the culture of
different groups'
'By weight there's more Japanese material than Chinese'
'Switching back and forth within minutes'
'Navigating the system ...'
'Takes time to find the information you actually need'
'Systems based on old categories [...] not very up to
date'
'[...] hard to find and sort'
'Find things (elsewhere) besides TMS'
'Once I put something there, I always add my name and
the date'
'Showing your sources'
'Just to see we did the work and when'
'Linking this object with that object'
'Different museums have different management systems'
'Make as many relations between objects as possible'
'Safeguarding knowledge that you are generating...'
'Allow people in the future to use what I'm doing today'
Quote Code
Standard-
isation
Usability
Data
Management
Themes
Multiple
Perspectives
Figure 4: Thematic analysis framework used for require-
ments engineering
within the interview data. This resulted in four themes, which serve
as the requirements to answer RQ1.
5.2.10 Standardisation. Standardisation is the umbrella term that
was formed to represent 5.2.1 ‘Lack of Standardisation’ and 5.2.2
‘Documentation’. All interviewees noted that there is overall a
lack of uniformity in writing provenance reports. There are no
enforced writing standards and each report differs from the amount
of information available regarding an object, the research needs of
the project, and the labour intensiveness of the research versus lack
of time. This translates into their documentation method within
TMS.
5.2.11 Multiple Perspectives. Multiple Perspectives remains its
own theme as mentioned in 5.2.3 as it relates to an essential ele-
ment of what provenance researchers want to reflect in their digital
reporting. There is a need by provenance researchers for space
in digital records to properly document the multiplicity of per-
spectives within an object’s history. A commonly cited example
by interviewees is an object’s multiplicity of cultures within one
continent or country. For example, an object may have the culture
‘African’, but may belong to two different tribes within Africa, or a
tribe may have relations to the object but may need further research.
This information requires documentation within the same field as it
relates to ‘culture’, but must be annotated correctly for readability.
5.2.12 Usability. The codes 5.2.4 ‘User Interaction’ and 5.2.5 ‘Search-
ability’ create the theme ‘Usability’ as they embody the elements
related to the manner in which provenance researchers interact
with the UI.
5

5.2.13 Data Management. The data management theme combines
5.2.6 ‘Traceability’, 5.2.7 ‘Interconnectedness’, and 5.2.8 ‘Future-
proofing’. These codes all relate to interviewee mentions of how
information can be digitised in a way that allows for the find-
ability, accesibility, interoperability, and reusability of it for other
researchers and for future work.
5.3 Design and Develop Artefact
A user interface named CultureSource (accessible here: https://bit.
ly/3xWLP8V), was built as the manifestation of the requirements
that were gathered during the pilot and primary study. Culture-
Source was built as a high-fidelity paper prototype on Figma, with
prefilled data from the same provenance report (Figure 1) used
for the interviews. The design is loosely based off the object and
person/institutions pages within TMS for familiarity.
Important design improvements include an updated list search
function, which is a sub-requirement under data management. In
Figure 5, ‘Lijst zoeken’ presents a number of radio buttons with
options for filtering a search in the database. The interview data
revealed the need for a more advanced form of search, where prove-
nance researchers are able to find objects, peoples, and institutions
through more obscure search parameters. The ‘andere’ denotes the
existence of a semantic search, wherein provenance researchers are
able to search for specific types of objects with parameters that are
made linkable with the data they input into object profiles.
Another design improvement is having data tabulated such as
Figure 6. It shows the UI of a screen meant for adding more than
one culture. Within TMS, this is a singular field, which forces the
researcher to make a decision on which culture is written here if
there are more than one. The ‘wie’ (who) and ‘datum toegevoegd’
(date added) columns also highlight more data management require-
ments, in that there is a traceability to the data that has been added.
This layout applies to many other fields besides culture, such as the
period, dates, and title.
Figure 7 is another example of fulfilling the data management re-
quirement. The interview data indicated that an important element
of understanding object provenance is understanding the recon-
struction provenance (‘reconstructie herkomst’). Separating each
field allows for machine readability and linkability of the data. For
example, inputting a person or institution with the label ‘type’ to
indicate the form of activity of which the transfer of the object took
place (e.g. an acquisition from the previous person or institution)
enhances its searchability.
Provenance researchers prefer to see the previous researchers
work to be able to understand their logic and workings. This also
includes traceability of all sources that were used to conduct the
research. Figure 8 is an example design of being able access and
record sources relating to the object being researched. For link-
ability, sources such as archival documents can be accessed and
searched within the internal database on this page to create rela-
tions between the object and the source. However, there is also the
added option of uploading a source themselves, including website
links and documentation.
When designing CultureSource, consideration was made to make
fields that can be made linkable from existing cultural heritage data
model documentation, such as that from Linked Art [8]. The label
Figure 5: Search Page
Figure 6: Adding a Culture Page
‘type’ in Figure 7 and provenance dated fields are examples of what
can be linked to a cultural heritage data model.
5.4 Demonstrate and Evaluate Artefact
To demonstrateCultureSource, informal user testing with a research
supervisor was done to prove the use case of the artefact as well
as to refine the user flow of the tasks to be conducted within the
prototype.
User testing and evaluation were then conducted with two prove-
nance researchers, both of whom had previously participated in
the primary interview study. User testing was set up via Microsoft
Teams and was scheduled for forty five minutes. The user testing
consisted of five tasks for the provenance researcher to complete,
with a post-task evaluation (see Appendix) to be completed on
Google Forms after each task. The tasks were to be completed
6

Figure 7: Reconstruction Provenance Page
Figure 8: Related Sources Page
within five minutes. As CultureSource is a high-fidelity paper proto-
type, users were asked to simulate and ‘pretend’ to input data. The
tasks were as follows:
(1) Input a provenance report
(2) Make additions to an object or P/I profile
(3) Perform a basic search
(4) Input an instance of multiple cultures
(5) Explore CultureSource
5.4.1 Results of User Testing. One of two users were able to com-
plete Task 1 and noted that the task was mostly intuitive and they
were able to find the features they needed without difficulty. How-
ever, both users mention that there are difficulties entering data and
that the fields provided were not sufficient in capturing all prove-
nance information. Both users remarked that writing pieces of text,
such as thought processes or uncertainty of information was diffi-
cult. For traceability, one user mentioned that information should
be placed somewhere that will be flagged for the next researcher.
There was also confusion on some fields, such as ‘Reconstructie
Areas of improvement
Space to communicate future research possibilities
Tracking changes across objects
Levels of (un)certainty for information input
Track geographical activities
Space to include paragraphs of written text
Enhanced search capabilities with more categorisations
Table 2: Areas of improvement in CultureSource
Herkomst’ (Reconstruction provenance) and ‘Verzamelgeschiede-
nis’ (Collection history) which could be joined together instead of
being separate.
One of two users were able to complete Task 2, with one user
saying it was less intuitive, and the other saying it was mostly
intuitive. Remarks included that the ‘Personen/Instellingen’ (per-
sons/institutions) should have more overviews and places to input
textual information as well as space for visualisations. Both users
felt that the fields provided were not sufficient for inputting prove-
nance information and that inputting data was difficult. One user
remarked that they would like a place to input local terminology,
with a suggestion tool for correct spelling, as one object could
have multiple names. There was also noted discomfort on entry
fields that enforced binaries such as ‘Gender’ and ‘Cultuur/Groep’
(culture/group) as with objects with non-western histories, ‘it is
usually misleading to account someone to a certain group based on
European archives’.
Well-received design
‘Reconstructie Herkomst’ (Reconstruction Provenance) page
Categorisation on ‘Gerelateerde Bronnen’ (Related Sources) page
Advanced ‘Andere’ (Other) search under ‘Lijkst zoeken’ (List Search)
Tabulated results of inputting multiple entries for ‘Titel’ (Title), ‘Periode’ (Period),
‘Cultuur’ (Culture), and ‘Datering’ (Dating)
Table 1: Design elements in CultureSource that worked well
Both users were able to complete Task 3, with one user saying it
was completely useful and comprehensive, and the other medium
helpful and comprehensive. A remark by the user noted that a
cross-section search would be helpful, stating ‘[...] all objects from
Congo present in the Rotterdam part of the collection which have
the prefix-VM’. It was noted that while the ‘andere’ (other) function
‘feels very nice’, there could be more comprehensive filters.
For Task 4, one user was able to complete the task, and one user
felt the fields were appropriate. One user responded with feedback
stating that options for “possibly’ or ‘likely’ with room for source
material that argues in favour of a specific culture’ would be nice
to have. They also mention the possibility of ‘gather[ing] several
older terminologies ‘for a culture‘ under a bigger one [...] so there
is an overview of what 19th century authors were naming a certain
group and what 21st century people self-identify as’.
The fifth task was to allow the user to freely explore Culture-
Source, both users responded that overall the prototype features
were mostly relevant to their work as provenance researchers.
6 DISCUSSION
The analysis conducted on the interviews formulated four require-
ments for a user interface that allows provenance researchers to
7

record their provenance reports: standardisation, multiple perspec-
tives, usability, and data management. From the development and
subsequent evaluation of CultureSource by two provenance re-
searchers, it is fit for purpose to a moderate extent in that to a
certain degree, provenance researchers were able to express polyvo-
cality but not to the greatest extent they would have preferred.
Provenance research is diverse in nature, and there are no stan-
dardised methods of writing reports. Reports are written in context
of either the project, to the discretion of the provenance researcher,
availability of information, and labour vs. time constrictions. In this
way, CultureSource lightly imposes a form of standardisation and
uniformity to the reporting in the form of varying text fields, those
of which are absent from TMS. The information can be expressed
in different fields which become linked and depending on the field,
can also be used in a semantic search. Notable elements of design
that were well received in Table 1 was the availability of more text
fields to place data into their respective categories.
Though well received, the answer to recording polyvocality
within a user interface, prima facie, was using multiple text fields,
user testing revealed that polyvocality is not only making space
for multiplicities but also interpretations and perspectives based
outside of European museum practice. For example, the culture field
within Personen/Instellingen (Persons/Institutes) is built within a
European cultural lens, and care must be taken to properly docu-
ment in such a way that does not enforce a framework on an entity
that exists outside of it.
Similar to the previous work on provenance reporting [9], while
CultureSource is able to represent polyvocal information to some
degree, the original unstructured provenance report is the most
information rich. As noted in the results, there lacked a space for
narrative-style thought processes. This is a trade-off for machine
readability and minimises the expressiveness of the information.
Table 2 provides some recommendations from the interview data
for further iterations and improvement.
The main takeaway from this study is that representation of
polyvocal knowledge requires careful understanding on what is
being documented. The study shows that creating the space in the
form of different textual fields facilitates the inclusion of polyvocal
narratives. However, it is noted that despite the requirements gath-
ered in this study which are aimed to enhance polyvocal knowledge
expression for objects in both a user interface and data-friendly
manner, further work needs to be done to enhance that expression.
The data contributes to a clearer understanding of what needs to
be taken into account when building a user interface that models
polyvocal knowledge.
7 LIMITATIONS (OR THREATS TO VALIDITY)
7.1 Internal Validity
Interview articipants were chosen based on access and availabil-
ity. Despite the lack of randomness, provenance researchers with
varying levels of seniority, former provenance researchers, and
researchers who spanned across two different organisations aided
in capturing different experiences.
There were only two provenance researchers available to do
user testing on CultureSource. The findings from this small sample
may are not wholly conclusive and would require further user
testing for further insights to be gained. Furthermore, the two
provenance researchers were also involved in the primary study,
there is a chance of observer bias as the observer has collaborated
and worked with the participants prior.
7.2 External Validity
The small sample size in both the primary study and the evaluation
is less likely to capture the richness or diversity of experiences
within the provenance research field, so there is a limit to the
generalisability of the data. The provenance researchers were from
a selected organisation and museum with professional working
connection’s to the supervisors of this paper, therefore the data and
insights gained from this study may only be relevant to this set of
researchers, and not the profession as a whole.
7.3 Construct Validity
The user testing may not have covered all the use cases. To mitigate
this, despite the small sample size, we added a free exploration task
as the final task to allow the provenance researchers to conduct
work related activities that are relevant to them.
8 CONCLUSION
While there are many studies which developed models for trans-
forming polyvocal cultural heritage into Linked Data, there have
been fewer studies done related to the development of user inter-
faces to represent those data models for cultural heritage collections.
The study outline four requirements and developed a prototype to
address ways to present fields to facilitate polyvocal knowledge
input. The prototype was then user tested and evaluated for its
usefulness. The findings from the study indicate that more under-
standing is required in representing information that both facilitates
polyvocal knowledge and machine readability.
The findings related to the creation of the prototype contribute
to the design and development of user interfaces within cultural
institutions.
9 ACKNOWLEDGEMENTS
The author would like to thank the provenance researchers for their
time and participation in this Master’s project.
REFERENCES
[1] Antonis Bikakis, Eero Hyvönen, Stéphane Jean, Béatrice Markhoff, and Alessan-
dro Mosca. 2021. Special issue on semantic web for cultural heritage. Semantic
Web 12, 2 (2021), 163–167.
[2] Annamaria Goy, Davide Colla, Diego Magro, Cristina Accornero, Fabrizio Loreto,
and Daniele Paolo Radicioni. 2020. Building semantic metadata for historical
archives through an ontology-driven user interface. Journal on Computing and
Cultural Heritage (JOCCH) 13, 3 (2020), 1–36.
[3] Alice Grant, Joséphine Nieuwenhuis, and Toni Petersen. 1995. International
guidelines for museum object information: the CIDOC information categories . In-
ternational Committee for Documentation of the International Council of . . . .
[4] Paul Johannesson and Erik Perjons. 2014.An introduction to design science . Vol. 10.
Springer.
[5] Muhammad Naeem, Wilson Ozuem, Kerry Howell, and Silvia Ranfagni.
2023. A Step-by-Step Process of Thematic Analysis to Develop a Concep-
tual Model in Qualitative Research. International Journal of Qualitative Meth-
ods 22 (2023), 16094069231205789. https://doi.org/10.1177/16094069231205789
arXiv:https://doi.org/10.1177/16094069231205789
[6] Raj Prasanna, Lili Yang, and Malcolm King. 2011. Evaluation of a software
prototype for supporting fire emergency response.. In ISCRAM.
8

[7] Lynn Rother, Max Koss, and Fabio Mariani. 2022. Taking Care of History: Toward
a Politics of Provenance Linked Open Data in Museums. Perspectives on Data
(2022).
[8] Robert Sanderson. 2021. Home — linked.art. https://linked.art/.
[9] Sarah Binta Alam Shoilee, Victor de Boer, and Jacco van Ossenbruggen. 2023.
Polyvocal Knowledge Modelling for Ethnographic Heritage Object Provenance.
In Knowledge Graphs: Semantics, Machine Learning, and Languages . IOS Press,
127–143.
[10] Laurajane Smith. 2020. Uses of heritage. In Encyclopedia of global archaeology .
Springer, 10969–10974.
[11] Carsten Stahn. 2023. Confronting Colonial Objects: Histories, Legalities, and Access
to Culture . https://doi.org/10.1093/oso/9780192868121.001.0001
[12] Violeta Tsenova, Gavin Wood, and David Kirk. 2023. Loci Stories: Exploring
Design for Polyvocality. In Proceedings of the 2023 ACM Designing Interactive
Systems Conference . 15–30.
[13] Hannah Turner. 2020. Cataloguing culture: Legacies of colonialism in museum
documentation. UBC Press.
[14] Leuphana University. 2023. https://digital-provenance.org/
[15] Marieke van Erp and Victor de Boer. 2021. A polyvocal and contextualised
semantic web. In The Semantic Web: 18th International Conference, ESWC 2021,
Virtual Event, June 6–10, 2021, Proceedings 18 . Springer, 506–512.
10 APPENDIX
10.1 Pilot Interview Questions
(1) What is your official title within [omitted] and/or [omitted]?
(2) Can you describe your role and key responsibilities within
[omitted]?
(3) How do you currently document and store provenance in-
formation for the artifacts or items that you research?
(4) Can you walk through the functions of the system(s) you
use to input your provenance information digitally?
(5) What day-to-day challenges do you face with the information
systems you currently use?
(6) Despite these challenges, how do you manage to maintain
accurate provenance documentation?
(7) In your opinion, what improvements could be made to the
system(s) to enhance information documentation and ensure
all necessary details are captured?
(8) How do you envision the ideal user interface for inputting
provenance information? What specific elements or design
features would be most helpful to you?
(9) Is there anything else you would like to add (regarding the
management of provenance information)?
10.2 Primary Interview Questions
(1) What is your official title within [omitted]?
(2) Can you describe your role and key responsibilities within
[omitted]?
(3) How do you currently document and store provenance in-
formation for the artifacts or items that you research?
(4) What day-to-day challenges do you face with the information
systems you currently use?
(5) Despite these challenges, how do you manage to maintain
accurate provenance documentation?
(6) What do you consider are the most important aspects when
it comes to inputting and maintaining your provenance doc-
umentation?
(7) In your opinion, what improvements could be made to the
system(s) to enhance information documentation and ensure
all necessary details are captured?
(8) Is there anything else you would like to add (regarding the
management of provenance information)?
System Walkthrough
(1) As an example, can you walk me through how would you
document this provenance report into the system?
10.3 Sub-requirements for CultureSource
Artefact Requirements
The artefact should be able to make a relation with one entity to another
The artefact should be able to share information across entities
The artefact should be able to navigate between entities without going back more
than two times
The artefact should be able to handle having more than one date for one entity
The artefact should be able to hold more than one date that is not all shared within
one text box
The artefact shall be able to hierarchise or dotpoint information
The artefact should have traceable text with name and date
The artefact should have a space for remarks by the provenance researcher
The artefact shall have a confirmation whenever a user completes an action
The artefact should have the ability to attach photographs to documentation
The artefact should be able to see what entities are linked to each other
The artefact should have the complete provenance report attached
The artefact shall handle filtering information within entities
The artefact should have a means of implementing multiple cultures within one
entity
The artefact should have distinctions on whether the object was created, sold, used.
The artefact should have a means of annotating pdf documentation (??)
The artefact should be available on all software platforms
The artefact should include search mechanisms that encompass not only inventory
number, but also keywords
The artefact should be able to extract and export information into a list
The artefact should give the user choice in what items on a page to export
The artefact should be able to display multiple sources with conflicting situations
The artefact should have functionality in place to ensure that objects are registered
properly
The artefact should be able to add, remove, and click website links
The artefact should give the user a way to verify a person had seen an object listed
in an entity in person
The artefact should have fields within PnI that contain contextual information in a
structured manner
The artefact should allow users to attach archival records to entities
The artefact should allow filtering of entities via different fields
The artefact should allow the user to input multiple cultural origins within an
entity
The artefact should allow the back and forth easy linkage between different entities
The artefact should be able to group objects through different types of categorisation
The artefact should allow a method of annotating PDF files
The artefact should have a log for who wrote what and when for all entries in all
entities
The artefact should be able to search with different types of terms relevant to
entities
The artefact should be able to make relations between entities
The artefact should be able to navigate between entities through relations
10.4 Post-task Evaluation
10.4.1 Task 1 - Input a provenance report .
(1) Were you able to complete your task? Yes/No
(2) To what extent did the task feel intuitive to complete? Com-
pletely unintuitive - Completely Intuitive (Likert Scale 1-5)
(3) Please elaborate on your response to the previous question. If
completely unintuitive, explain why. If completely intuitive,
explain what you felt was intuitive.
(4) Were you able to find the features you needed without diffi-
culty? Yes/No
(5) If not, what was hard to find?
9

(6) Did you encounter any difficulties while entering data?
(7) If yes, what was difficult? If no, what made it easy?
(8) Were the fields and options proivided sufficient for capturing
all necessary provenance information?
(9) If no, please explain. If yes, please explain what you liked.
(10) Were there any features or functionalities you felt were miss-
ing for the completion of the task?
(11) Do you have additional comments?
10.4.2 Task 2 - Make additions to an object or P/I profile .
(1) Were you able to complete the task? Yes/No
(2) To what extent did the task feel intuitive to complete? Com-
pletely unintuitive - Completely Intuitive (Likert Scale 1-5)
(3) Please elaborate on your response to the previous question. If
completely unintuitive, explain why. If completely intuitive,
explain what you felt was intuitive.
(4) Were you able to find the features you needed without diffi-
culty? Yes/No
(5) If not, what was hard to find?
(6) Did you encounter any difficulties while entering data?
(7) If yes, what was difficult? If no, what made it easy?
(8) Were the fields and options proivided sufficient for capturing
all necessary provenance information?
(9) If no, please explain. If yes, please explain what you liked.
(10) Were there any features or functionalities you felt were miss-
ing for the completion of the task?
(11) Do you have additional comments?
10.4.3 Task 3 - Perform a basic search .
(1) Were you able to complete the task? Yes/No
(2) Were the search filters and options useful and comprehen-
sive? Completely unuseful and incomprehensive - Com-
pletely useful and comprehensive (Likert Scale 1 - 5)
(3) Were there any features or functionalities you felt were miss-
ing for the completion of the task?
(4) Do you have additional comments?
10.4.4 Task 4 - Input an instance of multiple cultures .
(1) Were you able to complete the task? Yes/No
(2) Were the fields given appropriate for entering multiple cul-
tures? Yes/No
(3) Were there any fields you felt were missing or unnecessary
when inputting cultures? Yes/No
(4) If yes, please elaborate
(5) Is the provided way of viewing and inserting multiple cul-
tures organised in an appropriate manner? Yes/No
(6) If no, please elaborate
(7) Were there any features or functionalities you felt were miss-
ing for the completion of the task?
(8) Do you have additional comments?
10.4.5 Task 5 - Explore CultureSource.
(1) Were you able to complete the tasks efficiently? Yes/No
(2) Was the information presented in a clear manner that assists
you in doing your work? Yes/No
(3) How relevant were the features of CultureSource to your
work as a provenance researcher? Extremely irrelevant -
Extremely relevant (Likert Scale 1 - 5)
(4) Do you have other comments or feedback you would like to
give?
10
```
