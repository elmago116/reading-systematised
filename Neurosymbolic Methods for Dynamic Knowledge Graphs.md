---
title: Neurosymbolic Methods for Dynamic Knowledge Graphs
author: Mehwish Alam, Genet Asefa Gesese, Pierre-Henri Paris
year: "2025"
Type: Book Chapter
DOI: 10.3233/faia250223
source: https://doi.org/10.3233/faia250223
created: 2026-05-06
description: Knowledge graphs (KGs) have recently been used for many tools and applications, making them rich resources in structured format. However, in the real world, KGs grow due to the additions of new knowledge in the form of entities and relations, making these KGs dynamic. This chapter formally defines s
tags:
  - op/acc/pending-review
pdfORepub: "[[Neurosymbolic Methods for Dynamic Knowledge Graphs.pdf]]"
---
[[Neurosymbolic Methods for Dynamic Knowledge Graphs.pdf]]

> **Abstract:** Knowledge graphs (KGs) have recently been used for many tools and applications, making them rich resources in structured format. However, in the real world, KGs grow due to the additions of new knowledge in the form of entities and relations, making these KGs dynamic. This chapter formally defines several types of dynamic KGs and summarizes how these KGs can be represented. Additionally, many neurosymbolic methods have been proposed for learning representations over static KGs for several tasks such as KG completion and entity alignment. This chapter further focuses on neurosymbolic methods for dynamic KGs with or without temporal information. More specifically, it provides an insight into neurosymbolic methods for dynamic (temporal or non-temporal) KG completion and entity alignment tasks. It further discusses the challenges of current approaches and provides some future directions.
## Full text (extracted from `Neurosymbolic Methods for Dynamic Knowledge Graphs.pdf`)

*Source:* `2PDF/Neurosymbolic Methods for Dynamic Knowledge Graphs.pdf`  
*Extracted:* 2026-05-06

```text
arXiv:2409.04572v1  [cs.AI]  6 Sep 2024
July 2024
Neurosymbolic Methods for Dynamic
Knowledge Graphs
Mehwish ALAM a,1 , Genet Asefa GESESE b and Pierre-Henri P ARIS c
a T´el´ecom P aris, Institut P olytechnique de P aris, France
b FIZ Karlsruhe, Karlsruhe Institute of T echnology, Germany
c University of P aris Saclay, France
Abstract. Knowledge graphs (KGs) have recently been used for many tool s and
applications, making them rich resources in structured for mat. However, in the real
world, KGs grow due to the additions of new knowledge in the fo rm of entities
and relations, making these KGs dynamic. This chapter forma lly deﬁnes several
types of dynamic KGs and summarizes how these KGs can be repre sented. Addi-
tionally , many neurosymbolic methods have been proposed fo r learning represen-
tations over static KGs for several tasks such as KG completi on and entity align-
ment. This chapter further focuses on neurosymbolic method s for dynamic KGs
with or without temporal information. More speciﬁcally , it provides an insight into
neurosymbolic methods for dynamic (temporal or non-tempor al) KG completion
and entity alignment tasks. It further discusses the challe nges of current approaches
and provides some future directions.
Keywords. Dynamic Knowledge Graphs, T emporal Knowledge Graphs, Dyna mic
Entity Alignment, Dynamic Knowledge Graph Completion
1. Introduction
Knowledge Graphs (KGs) [1] have gained attention in the past few years for represent-
ing information in a structured way, i.e., entities and rela tions. It has been used for var-
ious applications and domains from search engines and recom mendation systems [2] to
bio-informatics [3] and social sciences [4]. They capture r elationships between entities
in a way that is both human-readable and machine-processabl e, enabling advanced rea-
soning and inference capabilities. The signiﬁcance of KGs l ies in their ability to inte-
grate vast amounts of heterogeneous data, providing a uniﬁe d framework that supports
comprehensive querying and analysis.
However, the real world is dynamic, with changes happening c ontinuously—new
entities emerge, existing relationships evolve, and facts that were once true may become
outdated. In such scenarios, traditional static KGs fall sh ort as they cannot accommo-
date these changes in real-time. This limitation has led to t he development of Dynamic
Knowledge Graphs (DKGs) , which can evolve by incorporating temporal information.
Dynamic KGs update the data and track changes, enabling temp oral queries and histori-
cal analysis.
1 Corresponding Author: mehwish.alam@telecom-paris.fr .

July 2024
The inclusion of temporality in KGs poses signiﬁcant challe nges. Firstly, the rep-
resentation of time-sensitive data requires precise model ing to capture the validity pe-
riod of facts. For example, without temporal information, a query asking about the pres-
ident of the United States might return multiple results, le ading to ambiguity. T empo-
ral dynamics are crucial in contexts like legal documents, m edical records, and ﬁnancial
transactions, where the timing of events plays a pivotal rol e in decision-making. Thus,
preserving temporality in KGs is beneﬁcial and necessary fo r ensuring the accuracy and
relevance of the information.
Furthermore, learning representations over DKGs is essent ial for several reasons.
It enables the development of models that can predict future changes, discover hidden
patterns, and provide insights based on the temporal evolut ion of data. This is particu-
larly valuable in predictive analytics, trend analysis, an d anomaly detection, where un-
derstanding the temporal context can signiﬁcantly enhance the accuracy of the results.
Entity alignment, the task of identifying equivalent entit ies across different datasets
or KGs, becomes increasingly complex in dynamic settings. A s entities and their at-
tributes change over time, ensuring they are correctly matc hed requires sophisticated
techniques that can handle temporal variations. This is cru cial for maintaining data in-
tegrity, improving the accuracy of merged datasets, and enh ancing the overall quality of
the KG.
In summary, the dynamic and temporal dimensions of KGs are cr itical for accurately
reﬂecting the complexity of real-world data. Addressing th e challenges associated with
these aspects can signiﬁcantly advance the ﬁeld of KG resear ch and its applications,
paving the way for more intelligent and responsive informat ion systems.
This book chapter is structured as follows: Section 2 review s related work and po-
sitions this chapter within the broader context. Section 3 p rovides fundamental deﬁni-
tions of the DKGs. Section 4 details how the dynamic informat ion can be represented
in the form of a KG. Following the discussion on representati on techniques, the book
chapter then moves on to explaining how neurosymbolic metho ds have been utilized for
learning representations over DKGs for KG Completion (Sect ion 5) and dynamic entity
alignment (Section 6).
2. Related W ork
One of the very recent studies provides an overview of the DKG s [5]. However, this
chapter mostly focuses on providing a formal deﬁnition of di fferent categories of DKGs
along with neurosymbolic methods for DKGs, such as learning representations over such
symbolic representations using methods based on neural net works along with the down-
stream tasks such as KG completion and entity alignment.
Several studies have been conducted on learning representa tions over KGs. For in-
stance, various techniques for reﬁning KGs are summarized i n [6], including methods
for KG completion. A categorization of static KG completion algorithms is given in [7].
In contrast, an exhaustive survey on multimodal KG embeddin g algorithms that utilize
literal (text, numeric, image) information within the stat ic KGs are presented in [8] along
with an experimental comparison of these algorithms. Furth ermore, a recent article [9]
provides an overview of various KG completion tasks, such as transductive and induc-
tive link prediction. It details methods incorporating bac kground information from large

July 2024
language models and discusses embeddings considering desc ription logic axioms. How-
ever, all these studies are limited to static KGs and do not co nsider the dynamic as-
pects in a KG. In contrast, [10] surveys the methods for T empo ral Knowledge Graph
(TKG) completion. This book chapter builds on this by formal ly deﬁning the funda-
mental differences between DKGs and TKGs. It provides a comp rehensive overview of
representation learning for these types of KGs, highlighti ng their unique characteristics
and challenges. Additionally, the chapter discusses vario us downstream tasks associated
with these graphs, such as KG completion and entity alignmen t, offering insights into
the methodologies and applications tailored to DKGs and TKG s.
3. Preliminaries
This section formally deﬁnes static, temporal, and dynamic KGs with examples.
Deﬁnition 1 (Static Knowledge Graph) Let G = (E ,R,L,F ) be a directed labeled
graph, where E , R, and L are the sets of entities, relations, a nd literals, respectively.
F ⊆ E ×R ×(E ∪L) represents a set of facts such that f = (h,r,t ) or f = (h,r,l) represent
one triple where f ∈ F , h ,t ∈ E , r ∈ R, and l ∈ L.
Example 1 Consider a simple knowledge graph G = (E ,R,L,F ) where:
• Entities (E): {Barack
Obama, USA }
• Relations (R): {president of}
• Literals (L): / 0
• F acts (F): {(Barack Obama, president of, USA) }
The example shows that Barack Obama is the president of the US A. Now , suppose we
update the graph with the following:
• E = E ∪ {Donald T rum p}
• R = R
• L = / 0
• F = F ∪ (Donald T rum p,president o f ,U SA)
In this static representation, the knowledge graph indicat es that both Barack Obama and
Donald T rump have been (or are) presidents of the USA. Howeve r , without temporal
information, it is unclear when each individual held ofﬁce.
The deﬁnition of a static KG can further be extended to a tempo ral KG, where each
triple can have a time interval representing its temporal va lidity:
Deﬁnition 2 (T emporal Knowledge Graph) Let G = (E ,R,L,T,Q) be a directed la-
beled graph, where E , R, L, and T represent the set of entities , relations, literals, and
timestamps, respectively. Q ⊆ E × R × (E ∪ L) × (T ∪ { / 0}) represents a set of facts such
that q = (h,r,t ,[τ s ,τ e ]) or q = (h,r,l,[τ s ,τ e ]) represent one quadruple where q ∈ Q,
h,t ∈ E , r ∈ R, l ∈ L, and τ s ,τ e ∈ T ∪ {/ 0} and τ s and τ e represent the start and end time,
i.e., τ s ≤ τ e . If τ s = τ e then it represents a point in time τ ∈ T .
Example 2 Consider a simple knowledge graph G = (E ,R,L,F ) where:

July 2024
• Entities (E): {Barack Obama, USA }
• Relations (R): {president of}
• Literals (L): {2009, 2017 } (representing years)
• Quadruples (Q): {(Barack Obama, president of, USA, [2009, 2017]) }
The example shows when the fact that Barack Obama held ofﬁce i s a valid fact, i.e., from
2009 to 2017.
Deﬁnition 3 (Dynamic Knowledge Graph) A dynamic knowledge graph G is a se-
quence of knowledge graphs {Gt0 ,Gt1 ,...,Gtn } indexed by time steps t 0 ,t1 ,... ,tn such
that t 0 < t1 < ··· < tn and ∀ti ,ti ∈ T , where T is the set of all timestamps. Each graph G ti ,
at time step t i , can be either a static knowledge graph (see Deﬁnition 1) or a temporal
knowledge graph (see Deﬁnition 2).
The graph G ti represents a snapshot of the dynamic graph G at time t i . The transition
between two consecutive snapshots G ti−1 and G ti can be characterized by changes in
entities, relations, literals, and facts. F ormally:
Eti = Eti−1 ∪ E +
ti \ E -
ti−1 where E +
ti and E -
ti−1 represent the additions and removals of entities ,
Rti = Rti−1 ∪ R+
ti \ R-
ti−1 where R +
ti and R -
ti−1 represent the additions and removals of relations ,
Lti = Lti−1 ∪ L+
ti \ L-
ti−1 where L +
ti and L -
ti−1 represent the additions and removals of literals ,
Gti = Gti−1 ∪ G+
ti \ G-
ti−1 where G +
ti and G -
ti−1 represent the additions and removals of facts .
Additionally, if G ti is a temporal knowledge graph, it can include changes in the
temporal intervals of the quadruples.
Example 3 Consider the ﬁrst snapshot of a simple knowledge graph G 0 = (E0,R0 ,L0 ,F0 )
where:
• Entities (E0): {Barack
Obama, USA }
• Relations (R0 ): {president of}
• Literals (L0 ): / 0
• F acts (F0): {(Barack Obama, president of, USA) }
W e can see that Barack Obama is the president of the USA as in th e ﬁrst example. Now ,
suppose we update the graph with the following new snapshot G 1 = (E1 ,R1,L1 ,F1):
• Entities (E1): E 0 \ {Barack Obama} ∪ {Donald T rum p}
• Relations (R1 ): R 0
• Literals (L1 ): L 0 = / 0
• F acts (F1): {(Donald T rump, president of, USA) }
Now , Donald T rump is the president of the USA in the last snaps hot G 1 , which no longer
contains information about Barack Obama.
Finally, consider the temporal KG of Example 2 as the ﬁrst sna pshot G 0 of a
simple knowledge graph. It can be updated with the following new snapshot G 1 =
(E1 ,R1,L1 ,F1):
• Entities (E1): E 0 ∪ {Donald T rum p}
• Relations (R1 ): R 0

July 2024
• Literals (L1 ): L 0 ∪ {2021}
• Quadruples (Q1): Q 0 ∪ {(Donald T rum p,president o f ,U SA,[2017,2021])}
This example is more complete because it keeps both facts wit h their respective time
validity.
4. Representing Dynamic and T emporal Knowledge Graphs
This section presents the different techniques to represen t temporal information in
knowledge graphs and that can be used for temporal KGs or dyna mic KGs.
4.1. T echniques to Represent T emporal Information in Knowl edge Graphs
The ﬁrst nucleus to represent time is the use of various XML Sc hema Deﬁnition [11]
(XSD) datatypes, such as xsd:dateTime, xsd:duration, xsd:date, and others, that
allows for precise representation of temporal data, includ ing speciﬁc moments, durations,
calendar dates, and individual time components, in KGs. The se datatypes have been
designed to facilitate the accurate and standardized encod ing of temporal information,
enabling robust temporal querying and reasoning.
4.1.1. T emporal Properties
T emporal properties directly incorporate time into relati onships within a KG. These
properties provide inherent temporal aspects to the entiti es and relationships they de-
scribe. For example (please note that all examples are provi ded in the Turtle syntax 2):
:Alice :birthDate "1990-01-01"^^xsd:date .
:Alice :employedAt :CompanyX .
:Alice :employmentStart "2020-01-01"^^xsd:date .
:Alice :employmentEnd "2022-01-01"^^xsd:date .
In this example, a simple temporal relation is represented u sing a time interval: Al-
ice’s employment relationship with CompanyX includes spec iﬁc start and end dates, en-
abling queries about her employment duration. The advantag e of this approach is its
straightforwardness and direct annotation of temporal dat a within the relationships them-
selves. However, it may lack ﬂexibility for more complex tem poral scenarios because
one need to know that “ employmentStart” is related to “ employedAt”. Additionally, if
one wants to keep track of Alice’s employment history, this b ecame more complex to
represent. T emporal attributes can also be represented, e. g., we also know her birth date,
which is a ﬁxed point in time.
All cross-domain general-purpose KGs have some form of temp oral information,
e.g., Wikidata [12], DBpedia [13], Y AGO [14,15], etc.
2 https://www.w3.org/TR/rdf12-turtle/

July 2024
4.1.2. Reiﬁcation
Reiﬁcation allows a triple to be treated as a subject of anoth er triple, thereby attaching
metadata such as temporal information. There are several wa ys to reify a triple.
The standard reiﬁcation [16] is a built-in functionality in RDF , i.e., a resource is used
to denote the fact and additional information about the stat ement can be added using
the RDF vocabulary (the properties “ rdf:subject”, “ rdf:predicate”, and “ rdf:object”). For
instance:
_:statement rdf:type rdf:Statement .
_:statement rdf:subject :Alice .
_:statement rdf:predicate :knows .
_:statement rdf:object :Bob .
_:statement :since "2022-01-01"^^xsd:date .
Through reiﬁcation, the relationship between Alice and Bob can be annotated with
the date they became acquainted. This approach offers ﬂexib ility in adding metadata to
existing triples but can lead to increased data redundancy a nd complexity.
Other possibilities to reify a fact are to use n-ary relation s [17] or to use singleton
properties [18]. The interested reader can refer to Hern ´ an dez et al. [19] for more details
and an in depth comparison of these approaches.
4.1.3. T ime Ontology in OWL
The Time Ontology in OWL 3 provides a comprehensive framework for representing
temporal concepts. This ontology includes classes and prop erties for describing instants,
intervals, and durations. Thus, the ontology is designed to support complex temporal
reasoning and querying following Allen’s interval algebra [20]. For example:
@prefix ex: <http://example.org/ns#> .
@prefix time: <http://www.w3.org/2006/time#> .
# Define Alice as a person
ex:Alice a ex:Person ;
ex:worksSince ex:JobStart .
# Define the job start time
ex:JobStart a time:Instant ;
time:inXSDDateTime "2020-01-01T00:00:00Z"^^xsd:dateTime .
# Define a class for persons who have been working for more
# than 3 years
ex:LongTermEmployee a owl:Class ;
owl:equivalentClass [
owl:intersectionOf (
ex:Person
[
3 https://www.w3.org/TR/owl-time/

July 2024
owl:onProperty ex:worksSince ;
owl:someValuesFrom [
owl:restriction [
owl:onProperty time:before ;
owl:hasValue
"2021-01-01T00:00:00Z"^^xsd:dateTime
]
]
]
)
] .
# Reasoning
ex:Alice a ex:LongTermEmployee .
In this example, we use the OWL Time ontology to describe the s tart date of Alice’s
employment and perform basic reasoning to determine if she q ualiﬁes as a long-term
employee.
The interesting deﬁnition is the class ex:LongT ermEmploye e used to represent indi-
viduals who have been working for more than three years. This class is speciﬁed using
owl:equivalentClass to intersect ex:Person and a restrict ion on the ex:worksSince prop-
erty. The restriction requires that the ex:worksSince prop erty has a value indicating a
work start date before January 1, 2021.
The reasoner determines that since Alice’s work start date i s “2020-01-01, ” which is
before the cutoff date “2021-01-01, ” she meets the criteria for long-term employment.
4.1.4. Named Graphs and Quadruples
Named graphs [21] group triples into a single graph that can h ave metadata associated
with it. This allows for temporal information to be added at t he graph level. For example:
GRAPH <http://example.org/graph/2022-01-01> {
:Alice :knows :Bob .
}
This structure facilitates temporal data management by ass ociating entire sets of
triples with speciﬁc temporal contexts. Named graphs are ad vantageous for segmenting
data into manageable subgraphs but can introduce overhead i n graph management and
querying.
Quadruples4 extend RDF triples by adding a fourth element, often used to r epresent
the context or the named graph, which can include temporal in formation. Contrary to
named graphs, quadruples are not a separate graph but a part o f the RDF data model, thus,
informations can be attached to the fact level instead of the whole graph. For example:
:Alice :knows :Bob "2022-01-01"^^xsd:date .
4 https://www.w3.org/TR/rdf12-n-quads/

July 2024
This quadruple includes a timestamp indicating when Alice a nd Bob’s acquaintance
began. The use of quadruples simpliﬁes the representation o f contextual information but
requires a data store that supports quad storage and queryin g.
4.1.5. RDF-star
RDF-star5 is an extension of the RDF data model that offers a more compac t and intuitive
way to represent complex statements, including those invol ving temporal information.
Examples include:
<< :Alice :knows :Bob >> :since "2022-01-01"^^xsd:date .
<< :Alice :worksAt :CompanyX >> :startDate "2020-01-01"^^xsd:date ;
:endDate "2022-01-01" .
<< :Alice :attended :ConferenceX >> :onDate "2023-06-15"^^xsd:date .
<< :Document123 :hasVersion :Version1 >> :timestamp
"2024-01-01T10:00:00Z" .
<< :DataItem :createdBy :User123 >> :creationTime
"2024-07-01T09:00:00Z" .
RDF-star enables a streamlined representation of temporal information, simplifying
the construction and querying of knowledge graphs. Its comp actness reduces data redun-
dancy and complexity but requires support for RDF-star synt ax and semantics in RDF
processors.
4.1.6. V ersioning
Maintaining historical data with timestamps is crucial for tracking changes over time.
V ersioning techniques ensure that the evolution of data is d ocumented, enabling tem-
poral queries and historical analysis. One can use simple ap proaches, such as adding a
timestamp to each triple, or more complex methods, such as re iﬁcation or named graphs.
For example, using versioning:
:Document123 :hasVersion :Version1 .
:Version1 :timestamp "2024-01-01T10:00:00Z" .
More complex versioning systems have been proposed over tim e: Frommhold et
al. [22] developed a V ersion Control System for KGs, emphasi zing the need for efﬁcient
change detection across graphs, including handling blank n odes. Their system uses in-
vertible patches to manage changes, supporting operations like revert and merge, and
ensuring data integrity through secure hashing of patches. This approach is foundational,
particularly in tracking changes in complex datasets and en suring reliable data history.
Pelgrin et al. [23] provided a comprehensive survey and anal ysis of KG archiving
systems, highlighting the lack of standardization and scal ability in existing solutions.
They introduced RDFev, a framework for studying the dynamic ity of RDF data, which
offers insights into dataset evolution at both low and high l evels. Their work outlines
the essential features of a fully-ﬂedged RDF archiving syst em, emphasizing the need
for robust support for concurrent updates, efﬁcient query p rocessing and comprehensive
version control features like branching and tagging.
5 https://w3c.github.io/rdf-star/cg-spec/editors_draft.html

July 2024
Properties Reiﬁcation Time
Ontology
Named Graphs
& Quadruples RDF-star V ersioning
T emporal X X X X* X
Dynamic X X* X X
T able 1. Comparison of T emporal and Dynamic Capabilities Across V ar ious RDF T echniques. The presence
of a feature is indicated by an ‘X’. The asterisk under Named G raphs & Quadruples denotes that a choice must
be made between temporal and dynamic, depending on the seman tics intended by the graph owner .
T able 1 provides a summary of the temporal and dynamic capabi lities of the var-
ious RDF techniques presented in this section For instance, temporal properties give a
straightforward way to annotate data with time, but they may not offer the ﬂexibility
needed for complex scenarios where relationships between d ifferent temporal attributes
must be explicitly deﬁned. Reiﬁcation and Named Graphs/Qua druples allow for more
detailed metadata, such as temporal context, versioning, o r provenance, which can be
crucial for historical analyses or data integrity. However , these methods can introduce
data redundancy and increase the complexity of queries. Add itionally, only one value
can be used as a fourth value or as the name of the named graph.
The Time Ontology in OWL is particularly useful for those nee ding to model com-
plex temporal relations, such as intervals and durations, a nd supports reasoning over
these data types. This makes it ideal for applications requi ring detailed temporal reason-
ing, such as historical data analysis or event tracking.
RDF-star offers a more compact and intuitive representatio n, which reduces data re-
dundancy and simpliﬁes the data structure. This can be parti cularly advantageous when
dealing with large datasets or when the overhead of traditio nal reiﬁcation methods be-
comes a concern. However, RDF processors must support RDF-s tar syntax and seman-
tics, which might not be universally available.
V ersioning techniques are essential for tracking changes o ver time, ensuring that a
KG can evolve while maintaining a record of past states. This is particularly relevant in
domains where data history is as important as the data itself , such as legal or historical
research, or dynamic KG completion.
When choosing a method for representing temporal informati on in KGs, researchers
and practitioners should consider the speciﬁc requirement s of their application, includ-
ing the complexity of the temporal relationships, the need f or metadata, the size of the
dataset, and the capabilities of the RDF processors they are using.
4.2. Prominent Knowledge Graphs
W e now describe some of the most prominent general-purpose K Gs and how they repre-
sent temporal information.
4.2.1. DBpedia
DBpedia [13] incorporates temporal aspects into its datase t through properties that de-
note speciﬁc time-related data. For example, temporal prop erties such as dbo:birthDate
and dbo:deathDate indicate birth and death dates for people, while other prop-
erties capture periods of activity or events, such as dbo:productionStartDate and
dbo:productionEndDate for manufacturing or production events. This inclusion of t em-
poral data allows for queries about the duration of events or the temporal relationships

July 2024
between entities. However, representing complex temporal scenarios might require ad-
ditional context or metadata, as basic temporal properties might not inherently indicate
their relation to other properties without such context.
DBpedia handles versioning primarily by maintaining histo rical data, which allows
tracking changes over time. The DBpedia Live system plays a c rucial role in this aspect,
as it continuously synchronizes with Wikipedia to update th e dataset with the latest in-
formation. This system utilizes a stream of updates from Wik ipedia, enabling DBpedia
to reﬂect recent edits with minimal delay, typically within a few minutes. V ersioning also
exists in DBpedia through snapshots, ensuring that histori cal changes are documented,
which is essential for conducting temporal queries and hist orical analyses.
4.2.2. YAGO
The second iteration of Y AGO [14] incorporates temporal dim ensions into its KG by
assigning existence times to entities and facts. This is ach ieved using speciﬁc relations
such as wasBornOnDate, diedOnDate, wasCreatedOnDate, and wasDestroyedOnDate,
which are standardized under generic entity-time relation s like startsExistingOnDate and
endsExistingOnDate. For events lasting a single day, Y AGO2 uses happenedOnDate,
which is a sub-property of both startsExistingOnDate and endsExistingOnDate. Facts
are assigned a time point if they are instantaneous events or a time span if they have an
extended duration with known beginning and end. This approa ch allows the system to
deduce the temporal scope of entities and events, providing a comprehensive temporal
annotation across the dataset.
For example, entities such as people are assigned birth and d eath dates, while arti-
facts and groups have creation and potential destruction da tes. In cases where the data is
incomplete or not applicable (e.g., abstract concepts or my thological entities), no tem-
poral data is assigned, adhering to a conservative approach . This temporal framework is
essential for enabling time-based queries and analyses, su ch as determining the lifespan
of individuals or the duration of historical events.
Y AGO 4.5 [15] builds upon the temporal framework of previous versions by enhanc-
ing its capacity to handle temporal information more ﬂexibl y and in more detail. The
integration of temporal data into Y AGO 4.5 utilizes the RDF- star model, allowing for
more intricate annotations of facts. This temporal tagging is crucial for representing the
evolving nature of the KG, allowing for dynamic queries that reﬂect changes over time.
All Y AGO versions are accessible only as archives, as the liv e version is not publicly
available.
4.2.3. W ikidata
Wikidata [12] utilizes a system of qualiﬁers to provide addi tional context to statements,
including temporal information. Qualiﬁers in Wikidata are versatile and can specify de-
tails such as the period during which a statement is valid. Fo r instance, in the following
example, Douglas Adams’s education at St John’s College is a nnotated with start and
end dates, providing a temporal dimension to his academic hi story:
wd:Q42 wdt:P69 wd:Q3918 .
wd:Q42 p:P69 _:statement .
_:statement ps:P69 wd:Q3918 .
_:statement pq:P580 "1971-10-01T00:00:00Z"^^xsd:dateTime .

July 2024
_:statement pq:P582 "1974-06-01T00:00:00Z"^^xsd:dateTime .
In this data snippet, ‘ wd:Q42’ represents Douglas Adams, ‘ wd:Q3918’ represents
St John’s College, ‘ p:P69’ and ‘ ps:P69’ denote the property for educational institutions
attended, and ‘ pq:P580’ and ‘ pq:P582’ provide the start and end times of the education
period, respectively.
Qualiﬁers in Wikidata allow for highly detailed annotation s of statements, includ-
ing dates, locations, and other contextual information. Th is feature supports complex
data representation but requires sophisticated data parsi ng and querying mechanisms to
retrieve and interpret the full context of the data.
Wikidata’s approach to versioning involves maintaining a c omplete history of all
edits, thus allowing for comprehensive tracking of changes over time. This version his-
tory is essential for verifying data provenance and underst anding the evolution of knowl-
edge within the graph. Unlike other KGs, Wikidata’s version history is openly accessible,
providing a transparent view of the data’s editorial proces s.
Furthermore, Wikidata is a DKG, continuously updated by a la rge community of
contributors. This live updating system ensures that Wikid ata remains current, reﬂecting
the latest information and corrections as they become avail able. The dynamic nature of
Wikidata, combined with its detailed versioning and tempor al annotations, supports both
real-time applications and historical research, making it a versatile tool for a wide range
of uses.
4.2.4. EventGraph
EventKG [24,25], a multilingual event-centric TKG, focuse s heavily on capturing and
representing temporal relations and events. The system mod els events using a canoni-
cal representation that incorporates both the start and end times of events, leveraging a
variety of data sources, including Wikidata, DBpedia, and Y AGO. T emporal informa-
tion in EventKG is linked to entities and events, allowing fo r detailed historical analy-
sis and event tracking. The model uses properties such as sem:hasBeginT imeStamp and
sem:hasEndT imeStamp to deﬁne the temporal span of events and entities’ involveme nt
in those events.
Additionally, EventKG employs the Simple Event Model (SEM) as its foundational
schema, which it extends to represent temporal relations be tter. This includes modeling
not only event-entity relationships but also complex tempo ral relations between multiple
entities or events, such as sequences of events and their hie rarchical relationships. This
comprehensive temporal modeling enables sophisticated qu eries and analyses concern-
ing the temporal dynamics of historical and contemporary ev ents.
Using named graphs and quadruples, EventKG also addresses v ersioning indirectly
by maintaining a provenance framework that tracks the sourc es and version history of the
data it integrates. Provenance information is critical in E ventKG, as it helps verify the
accuracy and credibility of the temporal data. Each piece of information, including tem-
poral annotations, is associated with metadata that detail s its origin, the speciﬁc version
of the source data, and the extraction date.

July 2024
5. Dynamic Knowledge Graph Completion
In the existing literature [26], TKGC methods are generally classiﬁed into two cate-
gories: interpolation-based and extrapolation-based. In terpolation-based methods aim to
predict missing knowledge by leveraging existing quadrupl ets. In contrast, extrapolation-
based methods are designed for continuous TKGs, enabling pr ediction of future events
by learning embeddings from previous or historical snapsho ts of entities and relations.
This work treats interpolation methods as TKGC for TKGs, whi le extrapolation-based
methods are applied to dynamic KGs, as deﬁned in Section 3.
5.1. T emporal Knowledge Graph Completion (TKGC)
T emporal Knowledge Graphs (TKGs) often contain millions or billions of quadruplets,
but they are typically incomplete for several reasons. Firs t, extracting information from
unstructured text sources can be error-prone, resulting in incomplete data. Second, cap-
turing or integrating all available information, particul arly from diverse or complex
sources, is challenging. Third, the sources themselves may lack comprehensiveness or
be biased, leading to selective inclusion of information an d omission of other relevant
facts. Lastly, the dynamic nature of information, with know ledge continuously evolving,
contributes to these gaps.
The KGC task – commonly known as link prediction (LP) – aims to predict miss-
ing links by utilizing existing information. V arious techn iques have been developed for
this task. However, a signiﬁcant limitation of these method s is their difﬁculty in cap-
turing the temporal dynamics of facts. They are typically de signed for static knowl-
edge graphs (KGs) that assume facts do not change over time. T herefore, these meth-
ods are ineffective when applied to TKGs, as they overlook th e crucial temporal infor-
mation inherent in TKGs. T emporal KGC (TKGC) methods have em erged to enhance
LP accuracy by addressing the limitations of traditional KG C methods. TKGC meth-
ods improve upon these by incorporating timestamps of facts into the learning process
in addition to the facts themselves. For instance, with TKGC , it is possible to infer the
fact (Gerhard Schr¨ oder, succeeded, Angela Merkel, 2005)using the existing
quadruplets (Angela Merkel, Chancelor of, Germany, [2005 to 2021]) and
(Gerhard Schr¨ oder, Chancelor of, Germany, [1998 - 2005]).
TKGC aims to predict possible links between two entities at a speciﬁc time. This
can be accomplished in different ways: i) tail prediction - given the head and relation at a
certain time, predicting the tail entity ( < h,r,? >), ii) head prediction - given the tail and
relation at a particular time, predicting the head entity ( <?,r,t >), iii) relation prediction
- given the head and tail at a certain time, predicting the rel ation ( < h,?,t >). Inspired
by the survey in [27], TKGC methods could be categorized into timestamps-dependent-
based TKGC, timestamps-speciﬁc functions-based TKGC, and deep learning-based
TKGC methods. A summary of these TKGC methods is provided in T able 2. Times-
tamps dependent-based TKGC methods such as TuckER TNT [28], TTransE [29], ST -
TransE [30], T -SimplE [31], Canonical Polyadic (CP) [32], T KGFrame [33], TBDRI [34]
associate timestamps to corresponding entities and relati ons to capture their evolution
without directly manipulating the timestamps.
Timestamps-speciﬁc Functions-based TKGC methods use spec ialized functions,
such as diachronic embedding, Gaussian, and transformatio n function, to learn em-

July 2024
beddings for timestamps. Transformation functions-based TKGC methods include
BoxTE [35], SPLIME [36], T ARGCN [37], T ASTER [38], Time-Low FER [39], Goel
et al. [40], and DEGA T [41]. Complex embedding functions-ba sed TKGC meth-
ods include ChronoR [42], TComplEx and TNTComplEx [43], T eR o [44], TGe-
omE [45], T eLM [46], RotateQVS [47], ST -NewDE [48], BiQCap [ 49],HA-TKGE [50],
STKE [51], and HTKE [52]. Non-linear embedding functions-b ased TKGC methods
iclude DyERNIE [53], A TiSE [54], HERCULES [55], and TKGC-AG P [56].
Deep learning-based TKGC methods capture the evolution of e ntities and rela-
tions by encoding timestamps using deep learning algorithm s. These methods can be
further grouped into i) Timestamps-Speciﬁc Space such as Hy TE [57], HTKE [52],
TRHyTE [58], BTHyTE [59], T oKEi [60], SANe [61], and QDN [62] , ii) Long Short-
T erm Memory (LSTM)-based TKGC methods such as T A-TransE and T A-DistMult [63],
TDG2E [64], Ma et al [65], CTRIEJ [66], and T eCre [67], and iii ) T emporal constraint-
based TKGC methods such as Chekol et al. [68], Kgedl [69], T -G AP [70], T emp-
Caps [71], RoAN [72], and T AL-TKGC [73].
Training procedure : Given a TKG G and a set of facts Q in G, a scoring function
g(q) is deﬁned to assign a factual score for a fact or a true quadrup let q ∈ Q. A negative
sampling strategy [74] is employed to create a set of negativ e samples, i.e., factually
incorrect quadruplets Q′, to enhance the expressiveness of learned representations for the
entities and relations in G.
Loss function: A loss function L aims at maximizing g(q) for all q ∈ Q and minimiz-
ing g(q′) for their negative samples q′ ∈ Q. The following are the commonly used loss
functions by TKGC approaches.
• Margin-based ranking loss (MRL) [75] enforces that the conﬁdence in the cor-
rupted quadruplet is lower than in the true quadruplet by a ce rtain margin. MRL
is computed as
LMRL = ∑
q∈Q
[
λ + g(q) − ∑
q′∈Q′
g(q′)
]
+, (1)
where [x]+ = max(x,0) and λ > 0 is a margin hyperparameter.
• Cross-entropy loss (CEL) [76] also aims at obtaining a large gap between true
quadruplets and the negative samples but without enforcing a ﬁxed margin for all
facts.
LCE L = ∑
q∈Q
ex p(g(q))
∑ q′∈Q′ ex p(g(q′)) (2)
• Binary cross-entropy loss (BCEL) [77] emphasizes the score of individual true
quadruplets and negative samples as follows:
LBCE L = ∑
q∈Q∪Q′
yg(q) + (1 − y)g(q′), (3)
where y = 1 if q ∈ Q and y = 0 otherwise.

July 2024
T able 2. Comparative Analysis of the TKGC methods presented in Secti on 5.1. ILP , CS, and SKGC stand for
Integer Linear Programming, Coordinate System, and Static Knowledge Graph Completion, respectively .
T echnique TKGC Methods Remarks
Translation TTransE [29],
ST -TransE [30],
BoxTE [35]
TTransE and ST -TransE struggle with
handling temporally evolving facts. All
are SKGC methods.
T ensor Decomp.
TuckER TNT [28],
T -SimplE [31],
Time-
LowFER [39],
QDN [62]
Time-LowFER ignores the rich contex-
tual information in the graph structure.
All except QDN are SKGC methods
ILP
TKGFrame [33] TKGFrame can not handle complex
scenarios like path queries.
Manifold
HERCULES [55],
DyERNIE [53]
Both are SKGC methods. HERCULES
does not show signiﬁcant differences
over benchmarks due to its limited use
of temporal information.
Block Decomp.
TBDRI [34] TBDRI is an SKGC method.
GCN T ARGCN [37] T ARGCN is an SKGC method.
GA T DEGA T [41]
Transformation SPLIME [36] SPLIME is an SKGC method.
Sparse Matrix T ASTER [38] T ASTER is an SKGC method.
Gaussian A TiSE [54]
Gaussian/Markov TKGC-AGP [56]
Polar CS HA-TKGE [50],
HTKE [52]
Both are SKGC methods.
Spherical CS STKE [51]
Complex Space TNTComplEx [43],
T eRo [44],
ChronoR [42]
All are SKGC methods.
Quaternion Space T eLM [46], Ro-
tateQVS [47],
TGeomE [45]
All are SKGC methods. T eLM ignores
the rich contextual information in the
graph structure.
Dihedron Algebra
ST -NewDE [48] ST -NewDE is an SKGC method.
Biquaternions/Manifold BiQCap [49] BiQCap is an SKGC method.
Time-Encoding T A-
DistMult [63],
T oKEi [60]
Both are SKGC methods.
Time-Encoding/LSTM T eCre [67] T eCre is an SKGC method.
T emporal-Hyperp HyTE [57],
BTHyTE [59]
Both are SKGC methods.
T emporal-Hyperp/GRU TRHyTE [58] TRHyTE is an SKGC method.
Multi-semantic Space SANe [61]
GRU TDG2E [64]
GRU/Negative Sampling CTRIEJ [66] CTRIEJ is an SKGC method.
Path Reasoning Kgedl [69]
GNN T -GAP [70]
Capsule Network T empCaps [71]
Attention RoAN [72], T AL-
TKGC [73]
Both are SKGC methods.

July 2024
Evaluation techniques: T ypically, evaluating TKGC methods involves performing
both head and tail predictions for each test quadruple q. For head prediction, the head
entity in q is replaced with every possible entity in the TKG. Similarly , the tail entity is
replaced with every possible entity for tail prediction. Th e scores generated by the scor-
ing function for these modiﬁed quadruples are then ranked. C ommonly used accuracy
metrics for this evaluation include Mean Rank (MR), Mean Rec iprocal Rank (MRR),
and Hits@k.
Benchmark datasets: The commonly used benchmark datasets for TKGC can be cat-
egorized into those used for interpolation methods, such as ICEWS14 [63], ICEWS05-
15 [63], GDEL T [78], Y AGO11k [57], Y AGO15k [63], and Wikidat a12k [57], and those
used for extrapolation methods, including ICEWS14 [63], IC EWS18 [79], GDEL T [78],
WIKI [29], and Y AGO [80].
5.2. Non-T emporal Dynamic KG Completion
Traditional methods for generating KG embeddings do not con sider the evolving nature
of a KG where new entities and relations are constantly being added to the KG. This
requires training the embeddings over the new KG from scratc h even if the changes are
minimal which can lead to increased computational costs. V a rious attempts have been
made to deal with this challenge. One of the ﬁrst attempts to a ddress this issue is online
learning, which learns incrementally as new information ar rives. However, one of the
drawbacks of these methods of KG embedding is that they do not consider the problem of
catastrophic forgetting. T o mitigate this issue, continua l or lifelong learning [81] methods
were proposed, alleviating the problem of catastrophic for getting in various tasks. In
catastrophic forgetting, adaptation to a new distribution generally results in a largely
reduced ability to capture the old ones.
Continual KG Embedding methods (CKGE) has recently receive d growing attention
which perform ﬁne-tuning with only new knowledge, leading t o reduced training costs.
These methods effectively alleviate the problem of catastr ophic forgetting while learning
the representations of the newly added knowledge. Continua l Learning-based methods
further target two kinds of solutions. First, the full-para meter ﬁne-tuning paradigm which
memorizes old knowledge by replaying a core old dataset or in troducing additional reg-
ularization constraints. Although this paradigm effectiv ely mitigates catastrophic forget-
ting, it signiﬁcantly increases training costs, especiall y when handling large-scale KGs.
Second, it adopts the incremental-parameter ﬁne-tuning pa radigm, with only a few pa-
rameters to learn emerging knowledge. This strategy may sti ll lead to an increase in
parameters and training time.
Recently, low-rank adapters such as LoRA have enabled efﬁci ent parameter ﬁne-
tuning and are used to reduce the training time in Large Langu age Models (LLMs). One
of the very recent studies, FastKGE, introduces incrementa l low-rank adaptation mech-
anisms, IncLoRAs, to reduce training costs for continual le arning for KG embeddings.
The rest of the section discusses and compares these methods in detail.
5.2.1. Online Learning Based Methods
puT ransE [82]. The current translational models (KG embedding models usin g
translation-based scoring functions) for static KG embedd ings have three signiﬁcant

July 2024
shortcomings. First, translational models are highly sens itive to hyperparameters such as
margin and learning rate [83]. Second, for one triple, there is only one representation if
the translation principle is followed, leading to low preci sion due to the congestion of
entities and relations in vector space. Last but not least, n ew unseen entities or relations
are not handled. One of the ﬁrst methods to deal with the drawb acks mentioned above is
Parallel Universe TransE (puTransE) – an extension of Trans E – which learns multiple
embeddings.
puTransE follows three steps: (i) triple selection (struct urally and semantically aware
triple selection), (ii) generation of random conﬁguration s, and (iii) learning embeddings.
T riple Selection Triple Selection includes semantically and structurally a ware triple se-
lection. T o select semantically relevant entities, the puT ransE samples a relation
r ∈ R and generates a set of entities {e1,e2 ,... ,en } ∈ E of all entities containing
r as either an outgoing or incoming edge. For structurally awa re triple selection,
the authors adopt the bidirectional random walk model using the entities selected
as starting nodes. puTransE creates multiple embedding spa ces each time new en-
tities or relations arrive, and for each embedding, it deﬁne s a triple constraint both
in count and diversity.
Generate Random Conﬁgurations Instead of deﬁning a global conﬁguration, pu-
TransE generates different hyperparameter conﬁgurations for each embedding
space. It randomly generates the value of the original Trans E hyperparameters,
i.e., margin and learning rate but also the values of triple c onstraint and number of
training epochs.
Learning Embeddings puTransE uses a margin-based loss function.
puTransE, however, learns embeddings from the local parts o f the KG, avoiding the
retraining of the whole embedding space, which leads to the l oss of global structural in-
formation in the learned embedding space. Additionally, si nce puTransE is an increment
over TransE, it uses the scoring function of TransE, which do es not work well for 1-to-N,
N-to-1, and N-to-N relations.
DKGE [84] learns joint embedding for each entity and relation by consi dering their
contextual information leading to an improvement over puTr ansE which only considers
local information. The context of an entity e1 is the one-hop neighborhood subgraph of
the entity represented as sg(e1 ) ∈ E . The context of a relation r1 is represented by the
relation path p1 = (r1 ,r2 ). The ﬁrst step is to encode the contextual information of ent ity
and relation as vector representations, which is then combi ned with the entity and relation
embeddings (referred to as knowledge embeddings). After th at, a scoring function and a
loss function based on translation operations for paramete r training are deﬁned.
The algorithm uses Attentive GCN (AGCN) Model to effectivel y take into account
the neighborhood information (modeled by GCN) and only use t he information that may
be important (modeled by the attention mechanism). Given x where x ∈ E orR and its
context, i.e., a subgraph with n vertices {vi}n
i=1 , DKGE builds the adjacency matrix A ∈
Rn×n and initializes the vertex feature matrix H (0) ∈ Rn×d0
where d0 is the number of
the initialized features for each vertex. Each row in H (0) is denoted as vi . If x is an entity,
then vi is an entity and vi is its contextual element embedding. When x is a relation, if vi
is a relation path consisting of two relations, then vi is the sum of the contextual element
embeddings of these two relations.

July 2024
The ﬁnal contextual subgraph embedding sg(x) of the subgraph sg(x) is given by a
weighted sum of the vectors of all vertices {vi}n
i=1 as follows:
sg(x) =
n
∑
i=n
α i(x)vi (4)
The scoring function is given as follows:
f (h,r,t ) =∥ h* + r* − t* ∥l1 (5)
where h*, r* and t* are computed by Equation 4, and ∥ ⊙ ∥ l1 denotes the l1 norm. A
margin-based loss function is utilized for training. Durin g online learning, at time step
T + 1, the knowledge embeddings and contextual element embeddi ngs for new entities
(relations) are randomly initialized according to a unifor m distribution. For existing en-
tities (relations), their knowledge embeddings and contex tual element embeddings are
carried over from the embedding results at time step T . These methods, however, do not
consider literal information along with the structural inf ormation of a KG.
DKGC-JSTD [85] proposes a DKG completion model that jointly learns the struc-
tural and textual information of entities and relations bas ed on a deep RNN. This model
learns the embedding of an entity’s name and parts of its text description to connect un-
seen entities to KGs. Deep memory network and association ma tching mechanism are
used to extract semantic feature information and establish relevance between entity and
relations from entity text-description. It then uses Recur rent Neural Networks to model
the dependency between topology-structure and text descri ption.
5.2.2. Continual Learning Based Methods
V arious methods based on continual learning have been propo sed. In this chapter, we
discuss some of the fundamental algorithms.
Lifelong Knowledge Graph Embedding (LKGE) [86] learns the embedding of an entity
or relation based on its masked ﬁrst-order subgraph given as follows:
xi = MAE (
i⋃
j=1
N j (x)) (6)
where x ∈ E or R , and N j ⊆ D j denotes the involved facts of x in the j-th snapshot
and D represents the training set. MAE () is an encoder that represents the input subgraph.
The objective of the KG encoder is to align the entity or relat ion embedding with the
reconstructed representation as follows:
LMAE = ∑
e∈Ei
∥ ei − ei ∥2
2 +∑
r
∈ Ri ∥ ri −
ri ∥2
2 (7)

July 2024
Graph Convolution Networks (GCN) and Transformer are two co mmon encoders.
If they are updated for lifelong learning, the changed model parameters will affect the
embedding generation of all old entities, including the inv olved old entities in new facts.
This can lead to catastrophic forgetting of the previous sna pshots. For this reason, the
entity and relation embedding transition functions are use d as encoders by LKGE, which
do not introduce additional parameters and use TransE. Tran sE is leveraged to train the
embeddings from the new data and update the knowledge transf er for each snapshot.
Lnew = ∑
(h,r,t )∈Di
max(0,γ + f (h,r,t ) − f (h′,r,t ′)) (8)
where γ is the margin. (h′,r,t ′) is the embedding of a negative fact. The subject or ob-
ject is randomly replaced with a random entity e′ ∈ Ei for each positive fact. The embed-
dings of unseen entities e and relations r are randomly initialized. T o avoid catastrophic
forgetting, regularization methods constrain the updates of the parameters. Accordingly,
the loss function of regularization methods is given as:
Lold = ∑
e∈Ei−1
w(e) ∥ ei − ei−1 ∥2
2 +∑
r
∈ Ri−1w(r) ∥ ri − ri−1 ∥2
2 (9)
where w(x) is the regularization weight for x. The regularization weight is only
computed once per snapshot. The overall learning objective is as follows:
L = Lnew +
α Lold + β LMAE (10)
where α ,β are hyperparameters for balancing the objectives.
One of the recent approaches uses low-rank adaptation for le arning dynamic KG em-
beddings. Incremental Low-Rank Adaptation (IncLoRA) [87] operated in three stages.
During the ﬁrst graph layering stage, new entities and relat ions are divided into several
layers based on the distance from the old graph and node degre es. The second stage
involves IncLoRA learning, in which incremental LoRAs with adaptive rank allocation
represent the embeddings of entities and relations in each l ayer. In the ﬁnal stage, link
prediction is performed, which composes all new LoRAs into a LoRA group and concat
all LoRA groups and initial embeddings for inference.
Several previous studies have proposed using different mec hanisms to learn the rep-
resentations of the initial state of KGs and then incrementa lly learning the representa-
tions upon the arrival of new entities and relations. Some co ntinual learning based algo-
rithms use translational embeddings [88], progressive neu ral networks [89], incremental
knowledge distillation [90], and graph attention networks [91].
6. Dynamic Entity Alignment
This section provides an overview of the temporal entity ali gnment methods between
two KGs. In addition to TKG alignment, a few methods have been proposed considering
new data while performing entity alignment.

July 2024
6.1. T emporal Entity Alignment Methods
Most of the methods for temporal entity alignment use GCNs or GNNs to learn the rep-
resentations of the entities alongside the temporal attent ion mechanism. In the following,
we brieﬂy overview the methods proposed so far.
In [92], the authors exploit both relation and temporal info rmation for entity align-
ment by ﬁrst creating a reverse link, i.e., introducing the i nverse of the relations to han-
dle the beginning and end of the relation. The method utilize s a time-aware attention
mechanism with GCN to assign different weights to entities a ccording to their relation
and temporal information. On the other hand, TKG Entity Alig nment via Representation
Learning (T em-EA) [93] incorporates temporal information with the help of Recurrent
Neural Networks to learn temporal sequence representation s. GCN and translation-based
embedding models are used for learning representations ove r structural and attribute in-
formation for computing entity similarity separately on th e two KGs to be aligned. These
representations are combined using linear weighting. The c oncept of nearest-neighbor
matching is performed to ﬁnd the most similar entity pair bas ed on the distance matrix.
A recent study [94] proposes a simple temporal information m atching mechanism
for entity alignment between TKGs. Most of the methods propo sed prior to this use a
time-aware attention mechanism to incorporate relational and temporal information into
entity embeddings. This study assumes that learning the rep resentations from the tempo-
ral information is unnecessary since a temporal matching me chanism, in addition to the
GNN-based model, achieves better results. In [95], the auth ors perform entity alignment
for TKGs via adaptive graph networks. More speciﬁcally, a ti me-aware graph attention
network model is used as an encoder to aggregate the features and temporal relationships
of neighboring nodes. DualMatch [96] is an unsupervised met hod that fuses the relational
and temporal information for EA by encoding temporal and rel ational information into
embeddings using a dual-encoder and combining both the info rmation and transforming
it into alignment using a novel graph-matching-based decod er called GM-Decoder.
6.2. T emporal and Evolving Entity Alignment Methods
T emporal Relational Entity Alignment (TREA) [97] learns alignment-oriented TKG
embeddings and represents new emerging entities. The ﬁrst s tep is to map entities, re-
lations, and timestamps into an embedding space, and the ini tial feature of each entity
is represented by fusing the embeddings of its connected rel ations and timestamps as
well as its neighboring entities. A Graph Neural Network (GN N) is employed to cap-
ture intra-graph information, and a temporal relational at tention mechanism is utilized to
integrate relation and time features of links between nodes . Finally, a margin-based full
multi-class log-loss is used for efﬁcient training, and a se quential time regularizer is used
to model unobserved timestamps.
Incremental T emporal Entity Alignment (ITEA) [98] targets the problem of temporality
as well as evolving KGs. It uses a combination of knowledge di stillation with the Graph
Attention Network (GA T) and the GCN acting as the teacher and student models, re-
spectively. The proposed model transfers knowledge from a c omplex model, the teacher,
whose output (in terms of probabilities) is used to train a si mpler model, the student.
The teacher Model within knowledge distillation provides i nstructional guidance to the
student model during its training phase.

July 2024
As a ﬁrst stage, entity embeddings are generated from the ent ity labels obtained
using GloV e. For preserving structural information in the t eacher model, a masked at-
tention mechanism over the neighboring entities of the enti ty ei . Time-aware structure
embedding is obtained using a multi-head attention-based G NN. This allows the teacher
model to not only learn the node features and time-aware stru ctural information but also
adjust their contributions adaptively based on the require ments of the speciﬁc task. The
student model uses an importance-sampling strategy to sele ct a small subset of nodes or
neighbors in each layer, and the model is trained on mini-bat ches of nodes.
Entity alignment module aligns the newly incoming entities with the existing ones,
and these alignments are achieved through string matching, structural similarity, etc. The
margin-based logistic loss function measures the dissimil arity between the embeddings
of aligned entities. The output from the teacher model is col lected by passing the new
data through the teacher model to compute its output probabi lities, Pt . Then, the output
of the student model is collected by passing the same data thr ough the student model to
compute its output probabilities, Ps . The total loss L can be written as:
L = α 1 × Lst andard + α 2 × Ldist illat ion
where α 1 and α 2 are weights that determine the relative importance of the st andard
loss and the distillation. Grid search is used to deﬁne possi ble values for α 1 and α 2 .
The standard loss compares the student’s outputs Ps with the true labels y. Lst andard for a
classiﬁcation task is typically the cross-entropy loss giv en as:
Lst andard = −∑ y × log(Ps)
where the sum is over all classes, and y is a one-hot encoded vector of the true labels.
The distillation loss that compares the student’s outputs Ps with the teacher’s outputs
Pt . Ldist illat ion is the Kullback-Leibler divergence between the teacher’s o utputs and the
student’s outputs and is given as:
Ldist illat ion = ∑ Pt × log( Pt
Ps
)
7. Discussion & Future Directions
This chapter formally deﬁnes various types of DKGs and explo res how this knowledge
can be represented within KGs. It then delves into different representation learning tech-
niques for both non-temporal and temporal DKGs, focusing on tasks related to KG com-
pletion. Additionally, it covers methods for aligning temp oral and dynamic KGs. The
studies discussed in this chapter primarily rely on the trip le structure or treat the KG as
a graph by incorporating the contextual information of enti ties and relationships while
largely overlooking schematic or ontological information [9]. Furthermore, the adapt-
ability of these algorithms to domain-speciﬁc and real-wor ld applications is limited, es-
pecially as KGs can expand to contain billions or even trilli ons of triples. Many of these

July 2024
algorithms also fail to utilize the literal information wit hin KGs. Only one of the recent
studies has attempted to use Large Language Models (LLMs) as background information
for TKGC [99] based on few-shot learning and concluded that L LMs do not bring sig-
niﬁcant increases in performance. However, the study misse s the analysis of the results
in the sense of how many predictions were hallucinations or o vergenerations of LLMs
for the speciﬁc task.
References
[1] Hogan A, Blomqvist E, Cochez M, d’Amato C, de Melo G, Gutie rrez C, et al. Knowledge Graphs.
ACM Comput Surv . 2022;54(4):71:1-71:37. A vailable from: https://doi.org/10.1145/3447772.
[2] Iana A, Alam M, Paulheim H. A survey on knowledge-aware ne ws recommender systems. Semantic
W eb. 2024;15(1):21-82. A vailable from: https://doi.org/10.3233/SW-222991.
[3] Jonquet C, LePendu P , Falconer SM, Coulet A, Noy NF , Musen MA, et al. NCBO Resource Index:
Ontology-based search and mining of biomedical resources. J W eb Semant. 2011;9(3):316-24.
[4] Chen Y , Sack H, Alam M. Analyzing social media for measuri ng public attitudes toward controversies
and their driving factors: a case study of migration. Soc Net w Anal Min. 2022;12(1):135. A vailable
from: https://doi.org/10.1007/s13278-022-00915-7 .
[5] Polleres A, Pernisch R, Bonifati A, Dell’Aglio D, Dobriy D, Dumbrava S, et al. How Does Knowledge
Evolve in Open Knowledge Graphs? TGDK. 2023;1(1):11:1-11: 59.
[6] Paulheim H. Knowledge graph reﬁnement: A survey of appro aches and evaluation methods. Semantic
W eb. 2017;8(3):489-508.
[7] W ang Q, Mao Z, W ang B, Guo L. Knowledge Graph Embedding: A S urvey of Approaches and Appli-
cations. IEEE Trans Knowl Data Eng. 2017;29(12):2724-43.
[8] Gesese GA, Biswas R, Alam M, Sack H. A survey on knowledge g raph embeddings with literals: Which
model links better literal-ly? Semantic W eb. 2021;12(4):6 17-47.
[9] Alam M, van Harmelen F , Acosta M. T owards Semantically En riched Embeddings for Knowledge
Graph Completion. CoRR. 2023;abs/2308.00081.
[10] Cai B, Xiang Y , Gao L, Zhang H, Li Y , Li J. T emporal Knowled ge Graph Completion: A Survey . In:
Proceedings of the Thirty-Second International Joint Conf erence on Artiﬁcial Intelligence, IJCAI 2023,
19th-25th August 2023, Macao, SAR, China. ijcai.org; 2023. p. 6545-53.
[11] Thompson HS, Beech D, Maloney M, Mendelsohn N, et al. XML schema part 1: structures second
edition. W3C recommendation. 2004;39.
[12] Vrandecic D. Wikidata: a new platform for collaborativ e data collection. In: Mille A, Gandon F , Misselis
J, Rabinovich M, Staab S, editors. Proceedings of the 21st W o rld Wide W eb Conference, WWW 2012,
Lyon, France, April 16-20, 2012 (Companion V olume). ACM; 20 12. p. 1063-4.
[13] Lehmann J, Isele R, Jakob M, Jentzsch A, Kontokostas D, M endes PN, et al. DBpedia - A large-scale,
multilingual knowledge base extracted from Wikipedia. Sem antic W eb. 2015;6(2):167-95.
[14] Hoffart J, Suchanek FM, Berberich K, W eikum G. Y AGO2: A s patially and temporally enhanced knowl-
edge base from Wikipedia. Artif Intell. 2013;194:28-61.
[15] Suchanek FM, Alam M, Bonald T , Chen L, Paris PH, Soria J. Y AGO 4.5: A Large and Clean Knowledge
Base with a Rich T axonomy . In: Proceedings of the 47th Intern ational ACM SIGIR Conference on
Research and Development in Information Retrieval. New Y or k, NY , USA: Association for Computing
Machinery; 2024. p. 131–140. A vailable from: https://doi.org/10.1145/3626772.3657876.
[16] McBride B. The Resource Description Framework (RDF) an d its V ocabulary Description Language
RDFS. In: Staab S, Studer R, editors. Handbook on Ontologies . International Handbooks on Information
Systems. Springer; 2004. p. 51-66.
[17] Erxleben F , G ¨ unther M, Kr ¨ otzsch M, Mendez J, Vrandeci c D. Introducing Wikidata to the Linked Data
W eb. In: The Semantic W eb - ISWC 2014 - 13th International Sem antic W eb Conference, Riva del
Garda, Italy , October 19-23, 2014. Proceedings, Part I. vol . 8796 of Lecture Notes in Computer Science.
Springer; 2014. p. 50-65.
[18] Nguyen V , Bodenreider O, Sheth AP . Don’t like RDF reiﬁca tion?: making statements about statements
using singleton property . In: Chung C, Broder AZ, Shim K, Sue l T , editors. 23rd International W orld
Wide W eb Conference, WWW ’14, Seoul, Republic of Korea, Apri l 7-11, 2014. ACM; 2014. p. 759-70.

July 2024
[19] Hern´ andez D, Hogan A, Kr ¨ otzsch M. Reifying RDF: What W orks W ell With Wikidata? In: Proceedings
of the 11th International W orkshop on Scalable Semantic W eb Knowledge Base Systems co-located
with 14th International Semantic W eb Conference (ISWC 2015 ), Bethlehem, P A, USA, October 11,
2015. vol. 1457 of CEUR W orkshop Proceedings. CEUR-WS.org; 2015. p. 32-47.
[20] Allen JF , Ferguson G. Actions and Events in Interval T em poral Logic. J Log Comput. 1994;4(5):531-79.
[21] Carroll JJ, Bizer C, Hayes PJ, Stickler P . Named graphs. J W eb Semant. 2005;3(4):247-67.
[22] Frommhold M, Piris RN, Arndt N, Tramp S, Petersen N, Mart in M. T owards V ersioning of Arbitrary
RDF Data. In: Proceedings of the 12th International Confere nce on Semantic Systems; 2016. .
[23] Pelgrin O, Gal´ arraga L, Hose K. T owards fully-ﬂedged a rchiving for RDF datasets. Semantic W eb.
2021;12(6):903-25.
[24] Gottschalk S, Demidova E. EventKG: A Multilingual Even t-Centric T emporal Knowledge Graph. In:
Gangemi A, Navigli R, V idal M, Hitzler P , Troncy R, Hollink L, et al., editors. The Semantic W eb -
15th International Conference, ESWC 2018, Heraklion, Cret e, Greece, June 3-7, 2018, Proceedings. vol.
10843 of Lecture Notes in Computer Science. Springer; 2018. p. 272-87.
[25] Gottschalk S, Demidova E. EventKG+TL: Creating Cross- Lingual Timelines from an Event-Centric
Knowledge Graph. In: Gangemi A, Gentile AL, Nuzzolese AG, Ru dolph S, Maleshkova M, Paulheim
H, et al., editors. The Semantic W eb: ESWC 2018 Satellite Eve nts - ESWC 2018 Satellite Events,
Heraklion, Crete, Greece, June 3-7, 2018, Revised Selected Papers. vol. 11155 of Lecture Notes in
Computer Science. Springer; 2018. p. 164-9.
[26] W ang J, W ang B, Qiu M, Pan S, Xiong B, Liu H, et al. A survey o n temporal knowledge graph comple-
tion: T axonomy , progress, and prospects. arXiv preprint ar Xiv:230802457. 2023.
[27] Cai B, Xiang Y , Gao L, Zhang H, Li Y , Li J. T emporal knowled ge graph completion: A survey . arXiv
preprint arXiv:220108236. 2022.
[28] Shao P , Zhang D, Y ang G, T ao J, Che F , Liu T . Tucker decompo sition-based temporal knowledge graph
completion. Knowledge-Based Systems. 2022;238:107841.
[29] Leblay J, Chekol MW . Deriving validity time in knowledg e graph. In: Companion proceedings of the
the web conference 2018; 2018. p. 1771-6.
[30] Ni R, Ma Z, Y u K, Xu X. Speciﬁc Time Embedding for T emporal Knowledge Graph Completion.
In: 2020 IEEE 19th International Conference on Cognitive In formatics & Cognitive Computing (ICCI*
CC); 2020. p. 105-10.
[31] Lin L, She K. T ensor decomposition-based temporal know ledge graph embedding. In: 2020 IEEE 32nd
International Conference on T ools with Artiﬁcial Intellig ence (ICT AI); 2020. p. 969-75.
[32] He P , Zhou G, Zhang M, W ei J, Chen J. Improving temporal kn owledge graph embedding using tensor
factorization. Applied Intelligence. 2023;53(8):8746-6 0.
[33] Zhang J, Sheng Y , W ang Z, Shao J. TKGFrame: a two-phase fr amework for temporal-aware knowledge
graph completion. In: W eb and Big Data: 4th International Jo int Conference, APW eb-W AIM 2020,
Tianjin, China, September 18-20, 2020, Proceedings, Part I 4; 2020. p. 196-211.
[34] Y u M, Guo J, Y u J, Xu T , Zhao M, Liu H, et al. TBDRI: block dec omposition based on relational
interaction for temporal knowledge graph completion. Appl ied Intelligence. 2023;53(5):5072-84.
[35] Messner J, Abboud R, Ceylan II. T emporal knowledge grap h completion using box embeddings. In:
Proceedings of the AAAI Conference on Artiﬁcial Intelligen ce. vol. 36; 2022. p. 7779-87.
[36] Radstok W , Chekol M, V elegrakis Y . Leveraging static mo dels for link prediction in temporal knowledge
graphs. In: 2021 IEEE 33rd International Conference on T ool s with Artiﬁcial Intelligence (ICT AI).
IEEE; 2021. p. 1034-41.
[37] Ding Z, Ma Y , He B, Tresp V . A simple but powerful graph enc oder for temporal knowledge graph
completion. arXiv 2022. arXiv preprint arXiv:211207791.
[38] W ang X, Lyu S, W ang X, Wu X, Chen H. T emporal knowledge gra ph embedding via sparse transfer
matrix. Information Sciences. 2023;623:56-69.
[39] Dikeoulias I, Amin S, Neumann G. T emporal knowledge gra ph reasoning with low-rank and model-
agnostic representations. arXiv preprint arXiv:22040478 3. 2022.
[40] Goel R, Kazemi SM, Brubaker M, Poupart P . Diachronic emb edding for temporal knowledge graph
completion. In: Proceedings of the AAAI conference on artiﬁ cial intelligence. vol. 34; 2020. p. 3988-95.
[41] W ang J, Zhu C, Zhu W . Dynamic embedding graph attention n etworks for temporal knowledge
graph completion. In: International Conference on Knowled ge Science, Engineering and Management.
Springer; 2022. p. 722-34.
[42] Sadeghian A, Armandpour M, Colas A, W ang DZ. Chronor: Ro tation based temporal knowledge graph

July 2024
embedding. In: Proceedings of the AAAI conference on artiﬁc ial intelligence. vol. 35; 2021. p. 6471-9.
[43] Lacroix T , Obozinski G, Usunier N. T ensor decompositio ns for temporal knowledge base completion.
arXiv preprint arXiv:200404926. 2020.
[44] Xu C, Nayyeri M, Alkhoury F , Y azdi HS, Lehmann J. T eRo: A t ime-aware knowledge graph embedding
via temporal rotation. arXiv preprint arXiv:201001029. 20 20.
[45] Xu C, Nayyeri M, Chen YY , Lehmann J. Geometric algebra ba sed embeddings for static and
temporal knowledge graph completion. IEEE Transactions on Knowledge and Data Engineering.
2022;35(5):4838-51.
[46] Xu C, Chen YY , Nayyeri M, Lehmann J. T emporal knowledge g raph completion using a linear temporal
regularizer and multivector embeddings. In: Proceedings o f the 2021 Conference of the North American
Chapter of the Association for Computational Linguistics: Human Language T echnologies; 2021. p.
2569-78.
[47] Chen K, W ang Y , Li Y , Li A. Rotateqvs: Representing tempo ral information as rotations in quaternion
vector space for temporal knowledge graph completion. arXi v preprint arXiv:220307993. 2022.
[48] Nayyeri M, V ahdati S, Khan MT , Alam MM, W enige L, Behrend A, et al. Dihedron algebraic em-
beddings for spatio-temporal knowledge graph completion. In: European Semantic W eb Conference.
Springer; 2022. p. 253-69.
[49] Zhang S, Liang X, Li Z, Feng J, Zheng X, Wu B. Biqcap: A biqu aternion and capsule network-based
embedding model for temporal knowledge graph completion. I n: International Conference on Database
Systems for Advanced Applications. Springer; 2023. p. 673- 88.
[50] Zhang J, Y u H. Hierarchy-A ware T emporal Knowledge Grap h Embedding. In: 2022 IEEE International
Conference on Knowledge Graph (ICKG). IEEE; 2022. p. 373-80 .
[51] W ang S, Liu R, Shen L, Khattak AM. Stke: T emporal knowled ge graph embedding in the spherical
coordinate system. In: International Conference on Artiﬁc ial Intelligence and Security . Springer; 2022.
p. 292-305.
[52] He P , Zhou G, Liu H, Xia Y , W ang L. Hyperplane-based time- aware knowledge graph embedding for
temporal knowledge graph completion. Journal of Intellige nt & Fuzzy Systems. 2022;42(6):5457-69.
[53] Han Z, Ma Y , Chen P , Tresp V . Dyernie: Dynamic evolution o f riemannian manifold embeddings for
temporal knowledge graph completion. arXiv preprint arXiv :201103984. 2020.
[54] Xu C, Nayyeri M, Alkhoury F , Y azdi H, Lehmann J. T emporal knowledge graph completion based on
time series gaussian embedding. In: The Semantic W eb–ISWC 2 020: 19th International Semantic W eb
Conference, Athens, Greece, November 2–6, 2020, Proceedin gs, Part I 19. Springer; 2020. p. 654-71.
[55] Montella S, Rojas-Barahona L, Heinecke J. Hyperbolic t emporal knowledge graph embeddings with
relational and time curvatures. arXiv preprint arXiv:2106 04311. 2021.
[56] Zhang L, Zhou D. T emporal knowledge graph completion wi th approximated Gaussian process em-
bedding. In: Proceedings of the 29th International Confere nce on Computational Linguistics; 2022. p.
4697-706.
[57] Dasgupta SS, Ray SN, T alukdar P . Hyte: Hyperplane-base d temporally aware knowledge graph em-
bedding. In: Proceedings of the 2018 conference on empirica l methods in natural language processing;
2018. p. 2001-11.
[58] Y uan L, Li Z, Qu J, Zhang T , Liu A, Zhao L, et al. Trhyte: T em poral knowledge graph embedding based
on temporal-relational hyperplanes. In: International Co nference on Database Systems for Advanced
Applications. Springer; 2022. p. 137-52.
[59] Liu K, Zhang Y . A T emporal Knowledge Graph Completion Me thod Based on Balanced Timestamp
Distribution. arXiv preprint arXiv:210813024. 2021.
[60] Leblay J, Chekol MW , Liu X. T owards temporal knowledge g raph embeddings with arbitrary time pre-
cision. In: proceedings of the 29th acm international confe rence on information & knowledge manage-
ment; 2020. p. 685-94.
[61] Li Y , Zhang X, Zhang B, Ren H. Each snapshot to each space: Space adaptation for temporal knowledge
graph completion. In: International Semantic W eb Conferen ce. Springer; 2022. p. 248-66.
[62] W ang J, W ang B, Gao J, Li X, Hu Y , Y in B. QDN: A quadruplet di stributor network for temporal
knowledge graph completion. IEEE Transactions on Neural Ne tworks and Learning Systems. 2023.
[63] Garc´ ıa-Dur´ an A, Dumanˇ ci´ c S, Niepert M. Learning se quence encoders for temporal knowledge graph
completion. arXiv preprint arXiv:180903202. 2018.
[64] T ang X, Y uan R, Li Q, W ang T , Y ang H, Cai Y , et al. Timespan- aware dynamic knowledge graph
embedding by incorporating temporal evolution. IEEE Acces s. 2020;8:6849-60.

July 2024
[65] Ma S, Li A, Zhao X, Song Y . Learning BiLSTM-based embeddi ngs for relation prediction in temporal
knowledge graph. In: Journal of Physics: Conference Series . vol. 1871. IOP Publishing; 2021. p. 012050.
[66] Li T , W ang W , Li X, W ang T , Zhou X, Huang M. Embedding uncer tain temporal knowledge graphs.
Mathematics. 2023;11(3):775.
[67] Ma J, Zhou C, Chen Y , W ang Y , Hu G, Qiao Y . T ecre: A novel tem poral conﬂict resolution method
based on temporal knowledge graph embedding. Information. 2023;14(3):155.
[68] Chekol M, Pirr ` o G, Schoenﬁsch J, Stuckenschmidt H. Mar rying uncertainty and time in knowledge
graphs. In: Proceedings of the AAAI Conference on Artiﬁcial Intelligence. vol. 31; 2017. .
[69] W ang Y , Qiao Y , Ma J, Hu G, Zhang C, Sangaiah AK, et al. A nov el time constraint-based approach for
knowledge graph conﬂict resolution. Applied Sciences. 201 9;9(20):4399.
[70] Jung J, Jung J, Kang U. Learning to walk across time for in terpretable temporal knowledge graph
completion. In: Proceedings of the 27th ACM SIGKDD Conferen ce on Knowledge Discovery & Data
Mining; 2021. p. 786-95.
[71] Fu G, Meng Z, Han Z, Ding Z, Ma Y , Schubert M, et al. T empCap s: a capsule network-based embedding
model for temporal knowledge graph completion. In: Proceed ings of the Sixth W orkshop on Structured
Prediction for NLP . Association for Computational Linguis tics; 2022. p. 22-31.
[72] Bai L, Ma X, Meng X, Ren X, Ke Y . RoAN: A relation-oriented attention network for temporal knowl-
edge graph completion. Engineering Applications of Artiﬁc ial Intelligence. 2023;123:106308.
[73] Nie H, Zhao X, Y ao X, Jiang Q, Bi X, Ma Y , et al. T emporal-st ructural importance weighted graph con-
volutional network for temporal knowledge graph completio n. Future Generation Computer Systems.
2023;143:30-9.
[74] Y ang Z, Ding M, Zhou C, Y ang H, Zhou J, T ang J. Understandi ng negative sampling in graph repre-
sentation learning. In: Proceedings of the 26th ACM SIGKDD i nternational conference on knowledge
discovery & data mining; 2020. p. 1666-76.
[75] Bordes A, Usunier N, Garcia-Duran A, W eston J, Y akhnenk o O. Translating embeddings for modeling
multi-relational data. Advances in neural information pro cessing systems. 2013;26.
[76] Li Z, Jin X, Guan S, Li W , Guo J, W ang Y , et al. Search from hi story and reason for future: T wo-stage
reasoning on temporal knowledge graphs. arXiv preprint arX iv:210600327. 2021.
[77] Liu Y , Hua W , Xin K, Zhou X. Context-aware temporal knowl edge graph embedding. In: W eb Informa-
tion Systems Engineering–WISE 2019: 20th International Co nference, Hong Kong, China, November
26–30, 2019, Proceedings 20; 2019. p. 583-98.
[78] Leetaru K, Schrodt P A. Gdelt: Global data on events, loc ation, and tone, 1979–2012. In: ISA annual
convention. vol. 2; 2013. p. 1-49.
[79] Jin W , Qu M, Jin X, Ren X. Recurrent event network: Autore gressive structure inference over temporal
knowledge graphs. arXiv preprint arXiv:190405530. 2019.
[80] Mahdisoltani F , Biega J, Suchanek FM. Y ago3: A knowledg e base from multilingual wikipedias. In:
CIDR; 2013. .
[81] W ang L, Zhang X, Su H, Zhu J. A Comprehensive Survey of Con tinual Learning: Theory , Method and
Application. IEEE Trans Pattern Anal Mach Intell. 2024;46( 8):5362-83.
[82] T ay Y , Luu A T , Hui SC. Non-Parametric Estimation of Mult iple Embeddings for Link Prediction on
Dynamic Knowledge Graphs. In: Proceedings of the Thirty-Fi rst AAAI Conference on Artiﬁcial Intel-
ligence, February 4-9, 2017, San Francisco, California, US A. AAAI Press; 2017. p. 1243-9.
[83] Ali M, Berrendorf M, Hoyt CT , V ermue L, Galkin M, Sharifz adeh S, et al. Bringing Light Into the Dark:
A Large-Scale Evaluation of Knowledge Graph Embedding Mode ls Under a Uniﬁed Framework. IEEE
Trans Pattern Anal Mach Intell. 2022;44(12):8825-45.
[84] Wu T , Khan A, Y ong M, Qi G, W ang M. Efﬁciently embedding dy namic knowledge graphs. Knowl
Based Syst. 2022;250:109124.
[85] Xie W , W ang S, W ei Y , Zhao Y , Fu X. Dynamic Knowledge Graph Completion with Jointly Structural
and T extual Dependency . In: Qiu M, editor . Algorithms and Ar chitectures for Parallel Processing - 20th
International Conference, ICA3PP 2020, New Y ork City , NY , U SA, October 2-4, 2020, Proceedings,
Part II. vol. 12453 of Lecture Notes in Computer Science. Spr inger; 2020. p. 432-48.
[86] Cui Y , W ang Y , Sun Z, Liu W , Jiang Y , Han K, et al. Lifelong E mbedding Learning and Transfer for
Growing Knowledge Graphs. In: Thirty-Seventh AAAI Confere nce on Artiﬁcial Intelligence, AAAI
2023, Thirty-Fifth Conference on Innovative Applications of Artiﬁcial Intelligence, IAAI 2023, Thir-
teenth Symposium on Educational Advances in Artiﬁcial Inte lligence, EAAI 2023, W ashington, DC,
USA, February 7-14, 2023. AAAI Press; 2023. p. 4217-24.

July 2024
[87] Liu J, Ke W , W ang P , W ang J, Gao J, Shang Z, et al.. Fast and C ontinual Knowledge Graph Embedding
via Incremental LoRA; 2024. A vailable from: https://arxiv.org/abs/2407.05705.
[88] Song H, Park S. Enriching Translation-Based Knowledge Graph Embeddings Through Continual Learn-
ing. IEEE Access. 2018;6:60489-97.
[89] Daruna AA, Gupta M, Sridharan M, Chernova S. Continual L earning of Knowledge
Graph Embeddings. IEEE Robotics Autom Lett. 2021;6(2):112 8-35. A vailable from:
https://doi.org/10.1109/LRA.2021.3056071.
[90] Liu J, Ke W , W ang P , Shang Z, Gao J, Li G, et al. T owards Cont inual Knowledge Graph Embedding
via Incremental Distillation. In: Thirty-Eighth AAAI Conf erence on Artiﬁcial Intelligence, AAAI 2024,
Thirty-Sixth Conference on Innovative Applications of Art iﬁcial Intelligence, IAAI 2024, Fourteenth
Symposium on Educational Advances in Artiﬁcial Intelligen ce, EAAI 2014, February 20-27, 2024, V an-
couver, Canada. AAAI Press; 2024. p. 8759-68.
[91] Kou X, Lin Y , Liu S, Li P , Zhou J, Zhang Y . Disentangle-bas ed Continual Graph Representation Learn-
ing. In: Proceedings of the 2020 Conference on Empirical Met hods in Natural Language Processing,
EMNLP 2020, Online, November 16-20, 2020. Association for C omputational Linguistics; 2020. p.
2961-72. A vailable from: https://doi.org/10.18653/v1/2020.emnlp-main.237.
[92] Xu C, Su F , Lehmann J. Time-aware Graph Neural Networks f or Entity Alignment between T emporal
Knowledge Graphs. CoRR. 2022;abs/2203.02150.
[93] Song X, Bai L, Liu R, Zhang H. T emporal Knowledge Graph En tity Alignment via Representation
Learning. In: Database Systems for Advanced Applications - 27th International Conference, DASF AA
2022, V irtual Event, April 11-14, 2022, Proceedings, Part I I. vol. 13246 of Lecture Notes in Computer
Science. Springer; 2022. p. 391-406.
[94] Cai L, Mao X, Ma M, Y uan H, Zhu J, Lan M. A Simple T emporal In formation Matching Mechanism
for Entity Alignment between T emporal Knowledge Graphs. In : Proceedings of the 29th International
Conference on Computational Linguistics, COLING 2022, Gye ongju, Republic of Korea, October 12-
17, 2022. International Committee on Computational Lingui stics; 2022. p. 2075-86.
[95] Li J, Song D, W ang H, Wu Z, Zhou C, Zhou Y . Entity alignment for temporal knowledge graphs via
adaptive graph networks. Knowl Based Syst. 2023;274:11063 1.
[96] Liu X, Wu J, Li T , Chen L, Gao Y . Unsupervised Entity Align ment for T emporal Knowledge Graphs.
In: Proceedings of the ACM W eb Conference 2023, WWW 2023, Aus tin, TX, USA, 30 April 2023 - 4
May 2023. ACM; 2023. p. 2528-38.
[97] Xu C, Su F , Xiong B, Lehmann J. Time-aware Entity Alignme nt using T emporal Relational Attention.
In: Laforest F , Troncy R, Simperl E, Agarwal D, Gionis A, Herm an I, et al., editors. WWW ’22: The
ACM W eb Conference 2022, V irtual Event, Lyon, France, April 25 - 29, 2022. ACM; 2022. p. 788-97.
[98] Li Y , Chen L, Liu C, Zhou R, Li J. Efﬁcient and Effective En tity Alignment for Evolving T emporal
Knowledge Graphs. In: Chen G, Khan L, Gao X, Qiu M, Pedrycz W , W u X, editors. IEEE International
Conference on Data Mining, ICDM 2023, Shanghai, China, Dece mber 1-4, 2023. IEEE; 2023. p. 349-
58.
[99] Luo R, Gu T , Li H, Li J, Lin Z, Li J, et al. Chain of History: L earning and Forecasting with
LLMs for T emporal Knowledge Graph Completion. CoRR. 2024;a bs/2401.06072. A vailable from:
https://doi.org/10.48550/arXiv.2401.06072.
```
