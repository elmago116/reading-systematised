---
title: "Neural-Symbolic Methods for Knowledge Graph Reasoning: A Survey"
author: Kewei Cheng, Nesreen K. Ahmed, Ryan A. Rossi, Theodore Willke, Yizhou Sun
year: "2024"
Type: Journal Article
DOI: 10.1145/3686806
source: https://doi.org/10.1145/3686806
created: 2026-05-06
description: Neural symbolic knowledge graph (KG) reasoning offers a promising approach that combines the expressive power of symbolic reasoning with the learning capabilities inherent in neural networks. This survey provides a comprehensive overview of advancements, techniques, and challenges in the field of ne
tags:
  - op/acc/pending-review
pdfORepub: "[[Neural-Symbolic Methods for Knowledge Graph Reasoning- A Survey.pdf]]"
---
[[Neural-Symbolic Methods for Knowledge Graph Reasoning- A Survey.pdf]]

> **Abstract:** Neural symbolic knowledge graph (KG) reasoning offers a promising approach that combines the expressive power of symbolic reasoning with the learning capabilities inherent in neural networks. This survey provides a comprehensive overview of advancements, techniques, and challenges in the field of neural symbolic KG reasoning. The survey introduces the fundamental concepts of KGs and symbolic logic, followed by an exploration of three significant KG reasoning tasks: KG completion, complex query answering, and logical rule learning. For each task, we thoroughly discuss three distinct categories of methods: pure symbolic methods, pure neural approaches, and the integration of neural networks and symbolic reasoning methods known as neural-symbolic. We carefully analyze and compare the strengths and limitations of each category of methods to provide a comprehensive understanding. By synthesizing recent research contributions and identifying open research directions, this survey aims to equip researchers and practitioners with a comprehensive understanding of the state-of-the-art in neural symbolic KG reasoning, fostering future advancements in this interdisciplinary domain.
## Full text (extracted from `Neural-Symbolic Methods for Knowledge Graph Reasoning- A Survey.pdf`)

*Source:* `2PDF/Neural-Symbolic Methods for Knowledge Graph Reasoning- A Survey.pdf`  
*Extracted:* 2026-05-06

```text
Neural-Symbolic Methods for Knowledge Graph Reasoning:
A Survey
KEWEI CHENG, Amazon, Palo Alto, CA, USA
NESREEN K. AHMED, Intel Labs, Santa Clara, CA, USA
RYAN A. ROSSI, Adobe Research, San Jose, CA, USA
THEODORE WILLKE, Intel Labs, Hillsboro, OR, USA
YIZHOU SUN, University of California, Los Angeles, Los Angeles, CA, USA
Neural symbolic knowledge graph (KG) reasoning offers a promising approach that combines the expressive
power of symbolic reasoning with the learning capabilities inherent in neural networks. This survey provides
a comprehensive overview of advancements, techniques, and challenges in the field of neural symbolic
KG reasoning. The survey introduces the fundamental concepts of KGs and symbolic logic, followed by an
exploration of three significant KG reasoning tasks: KG completion, complex query answering, and logical rule
learning. For each task, we thoroughly discuss three distinct categories of methods: pure symbolic methods,
pure neural approaches, and the integration of neural networks and symbolic reasoning methods known as
neural-symbolic. We carefully analyze and compare the strengths and limitations of each category of methods
to provide a comprehensive understanding. By synthesizing recent research contributions and identifying
open research directions, this survey aims to equip researchers and practitioners with a comprehensive
understanding of the state-of-the-art in neural symbolic KG reasoning, fostering future advancements in this
interdisciplinary domain.
CCS Concepts: •Computing methodologies →Knowledge representation and reasoning ;
Additional Key Words and Phrases: Knowledge Graph, Neural Symbolic Reasoning
ACM Reference format:
Kewei Cheng, Nesreen K. Ahmed, Ryan A. Rossi, Theodore Willke, and Yizhou Sun. 2024. Neural-Symbolic
Methods for Knowledge Graph Reasoning: A Survey.ACM Trans. Knowl. Discov. Data.18, 9, Article 225
(November 2024), 44 pages.
https://doi.org/10.1145/3686806
1 Introduction
Knowledge plays a pivotal role in human intelligence, serving as the bedrock for reasoning and
problem-solving. Recently, the field ofArtificial Intelligence (AI) strives to mimic human actions
and decision-making capabilities. In this pursuit,knowledge graphs (KGs) have emerged as
Authors’ Contact Information: Kewei Cheng (corresponding author), Amazon, Palo Alto, CA, USA; e-mail:chenkewe@
@amazon.com; Nesreen K. Ahmed, Intel Labs, Santa Clara, CA, USA; e-mail: nkahmed@alumni.purdue.edu; Ryan A. Rossi,
Adobe Research, San Jose, CA, USA; e-mail: ryarossi@gmail.com; Theodore Willke, Intel Labs, Hillsboro, OR, USA; e-mail:
ted.willke@intel.com; Yizhou Sun, University of California, Los Angeles, Los Angeles, CA, USA; e-mail: yzsun@cs.ucla.edu.
Permission to make digital or hard copies of all or part of this work for personal or classroom use is granted without fee
provided that copies are not made or distributed for profit or commercial advantage and that copies bear this notice and the
full citation on the first page. Copyrights for components of this work owned by others than the author(s) must be honored.
Abstracting with credit is permitted. To copy otherwise, or republish, to post on servers or to redistribute to lists, requires
prior specific permission and/or a fee. Request permissions frompermissions@acm.org.
© 2024 Copyright held by the owner/author(s). Publication rights licensed to ACM.
ACM 1556-472X/2024/11-ART225
https://doi.org/10.1145/3686806
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:2 K. Cheng et al.
Fig. 1. Inferring new facts over a toy example of KG. (a) A toy example of KG containing five entities, three
relations, and four observed facts. (b) A set of new facts denoted as the red dotted lines that can be inferred
from existing facts.
a critical tool for representing, storing, and effectively managing knowledge [45]. Real-world
knowledge is expressed as triples in a KG, denoted as (head entity, relation, tail entity), which
signifies the connection between two entities via a particular relationship. An instance of a KG is
shown in Figure1. For instance, (“Mina Miller”,liveIn, “USA”) is a triple where “Mina Miller” and
“USA” are entities in the KG connected by the relation “liveIn.”
Integrating KGs into AI systems can systematically enhance their performance and reasoning
abilities, leading to a variety of successful applications. For instance, search engines utilize KGs to
furnish search queries with structured, relevant, and informative data [27, 85]. In healthcare, KGs
are employed to effectively manage patient data, improve clinical decision-making, and accelerate
medical research [32]. Additionally, KGs can be employed in smart cities to integrate data from
various sources such as traffic sensors, weather sensors, and social media, to provide insights and
facilitate decision-making [84]. Although KGs are valuable, they cannot capture every real-world
fact. Therefore, a vital aspect of KG reasoning is to infer missing information from the existing
KG facts. This is achieved through two primary approaches:traditional symbolic logical reasoning
techniques and modern representation-learning-based techniques.
Symbolic reasoning has been the most studied approach toward KG reasoning since the earliest
days. This approach represents expert knowledge as statements in a logic-based representation
language and implements reasoning as logical inference, primarily addressing high-level reason-
ing and cognitive processes [10]. For instance, consider the logical ruleSpeakLanguage(G, ~)←
LiveIn(G, I )∧OfficialLanguage(I, ~), along with the observed facts “LiveIn(Mina Miller, USA)” and
“OfficialLanguage(USA, English),” we can infer the new fact “SpeakLanguage(Mina Miller, English).”
Symbolic reasoning approaches have demonstrated strong interpretability and generalizability due
to the power of logical rules. Nevertheless, they encounter certain limitations when it comes to
scaling up to vast datasets, managing ambiguity, and capturing the correlations between entities
and relations. To illustrate, consider the case where both “USA” and “United States” denote the
same country. Symbolic reasoning approaches treat them as distinct entities, thereby failing to
automatically transfer the knowledge from the existing triple “LiveIn(Mina Miller, USA)” to deduce
the new fact “LiveIn(Mina Miller, United States)”.
Representation learning-based techniques have recently emerged as state-of-the-art methods
in KG reasoning owing to their successful applications [115]. Unlike symbolic reasoning, these
techniques aim to predict unseen triples by exploring the graph structure in KGs to capture the
similarity of entities. Representation learning-based techniques have demonstrated good scalability
and a strong ability to capture correlations between entities and relations. However, they fall
short in modeling higher-order dependencies of KG relations. For instance, while representation
learning-based techniques can recognize that “USA” and “United States” refer to the same country
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:3
Table 1. Capabilities of Different Categories of Methods
Symbolic Methods Neural Methods Neural Symbolic Methods
Interpretability   
Generalizability   
Exploring Intrinsic
Similarities Among Triples   
Differentiable   
Scalable   
based on their similarity in embeddings, they cannot infer that “Mary Stilwell” and “Mina Miller”
speak “English” without leveraging logical rules.
While symbolic reasoning and representation learning are typically seen as distinct approaches
toward achieving the ultimate goal of KG reasoning, they possess a natural potential to complement
and enhance each other. Symbolic approaches offer significant interpretability and generalizability,
leveraging logical rules to provide insights into inferred results and enabling easy generalization to
unobserved objects. However, they struggle to handle large datasets and fail to capture correlations
between entities and relations. Conversely, representation learning-based techniques address the
limitations of symbolic approaches by exploring intrinsic similarities among triples, but they
lack interpretability and generalizability. By integrating both techniques into a unified framework,
neural-symbolicreasoningprovidesamoreefficient,generalizable,andinterpretablewaytoperform
KG reasoning. First of all, the powerful computation ability of neural networks can be attributed to
reducing the exponential computational complexity of traditional symbolic methods. For example,
in a large-scale KG reasoning task, traditional symbolic methods would not be suitable, as their
computational complexity increases exponentially with the size of the KG. Second, the strong
generalizability of symbolic logic can be leveraged to compensate for the lack of data availability.
For example, although neural networks highly rely on large amounts of high-quality training data,
neural-symbolic methods are not significantly impacted by limitations on the amount of available
training data. For example, in a few-shot learning task, a neural-symbolic system can use symbolic
knowledge as extra data to enrich the limited training samples. Third, neural-symbolic systems can
provide explicit computation processes, such as a traced reasoning process or a chain of evidence
of results. For example, in medical diagnosis, neural-symbolic systems are expected not only to
make a decision but also to show the reason for this decision in order to aid the doctor in the
diagnosis. Due to the advantages brought by neural-symbolic systems, this survey concentrates
on the seamless integration of discrete symbols from symbolic systems with continuous vectors
from neural systems to enhance the reasoning performance of neural-symbolic systems. Table1
provides a comprehensive summary and comparison of the strengths and weaknesses of symbolic
methods, neural methods, and neural-symbolic methods in KG reasoning.
Summary of Contributions.While other surveys have been conducted to summarize the ap-
proaches to KG reasoning, these studies tend to focus on either traditional symbolic approaches
[35, 95] or more recent neural approaches [19, 49, 115]. Although some surveys have specifically
explored neural-symbolic approaches for KG reasoning [134, 136], they have not sufficiently es-
tablished the connection between traditional symbolic methods and neural-symbolic approaches.
To address this gap, our survey paper aims to offer a comprehensive and structured overview of
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:4 K. Cheng et al.
Fig. 2. Taxonomy of neural-symbolic techniques for KG reasoning.
neural-symbolic KG reasoning techniques. It particularly emphasizes the evolution and integration
of symbolic and neural approaches. The primary contributions of this paper are summarized as
follows:
— New taxonomy. As illustrated in Figure2, we introduce a novel taxonomy for categorizing KG
reasoning techniques. This taxonomy divides these techniques into two main categories: tra-
ditional symbolic KG reasoning approaches and recent neural network-based approaches. Ad-
ditionally, we explore the integration of these two paradigms by introducing neural-symbolic
systems, which combine elements of both traditional methods and modern neural approaches.
Our taxonomy further differentiates KG reasoning methods into two primary categories: (1)
KG completion, which focuses on predicting specific facts within the KG, and (2) rule learn-
ing, which aims to discern general patterns in the form of rules. This classification not only
highlights the distinct approaches within KG reasoning but also emphasizes the evolutionary
bridge between symbolic and neural methods in this domain.
— Comprehensive review. For each type of modern symbolic reasoning approach, we provide
detailed descriptions of representative models and make necessary comparisons of all their
corresponding algorithms.
— Open questions and challenges. We discuss open questions that remain to be addressed, the
challengesassociatedwiththem,andsuggestpromisingfuturedirections,suchas(1)Temporal
reasoning, (2) Multi-modal reasoning, (3) Developing interactive reasoning systems, and (4)
Combining KG withLarge Language Model (LLM) .
The remainder of this survey is organized as follows. Section2 initially offers a comprehensive
overview of the evolution of neural-symbolic systems for KG reasoning. Section3 provides back-
ground knowledge closely related to the surveyed techniques, including the introduction of KGs
and the technical foundations of symbolic logic. Sections4 and 5 together delve into methods for
KG completion tasks. Knowledge graph completion involves predicting missing facts by leveraging
existing facts, but the complexity involved in making these predictions can vary considerably. To
address this, we have categorized KG completion into two sub-categories: (1) Link Prediction, which
focuses onone-hop queriessuch as (Obama, bornIn, ?), covered in Section4, and (2) Complex Query
Answering, which tacklescomplex querieson KGs, discussed in Section5. These complex queries
engage multiple relations or conditions between entities, facilitating more intricate reasoning and
inference processes, particularly emphasizing multi-hop queries and generalFirst-Order Logic
(FOL) queries. Section6 explores the challenges and solutions in rule learning. Section7 builds
on Sections4, 5, and6 to discuss various evaluation methods and metrics for each task. Section8
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:5
identifies open research questions and potential future directions in the field. Finally, Section9
concludes this survey.
2 Neural-Symbolic Knowledge Graph Reasoning Taxonomy
The purpose of this section is to provide readers with a well-rounded comprehension of the
evolution of neural-symbolic systems for KG reasoning. Reasoning can encompass two types:
deductive reasoningand inductive reasoning. Deductive reasoning starts with a general hypothesis
and proceeds to derive specific conclusions about individual instances while inductive reasoning
involves formulating broad generalizations or principles from a set of instance observations. In the
context of KG reasoning, there are also two primary tasks: (1) KG completion and (2) rule learning.
KG completion involves inferring new knowledge based on existing facts and rules, aligning with
the concept of deductive reasoning. On the other hand, rule learning in KGs aims to generalizing
new rules from observed data, which aligns with inductive reasoning. While the application of
logical rules significantly enhances the process of KG completion, it’s crucial to understand that
KG completion and rule-based reasoning are distinct tasks, each with its own methodologies and
objectives. Each of these tasks plays a crucial role in the effective and efficient functioning of KG
reasoning from different perspectives.
— KGCompletion:ThistaskinvolvesenrichingKGsbypredictingthemissingknowledgebasedon
existing facts and rules. The objective is to create a more complete and accurate representation
of knowledge.
— Rule Learning: Instead of inferring new facts, rule learning involves discovering implicit rules
within the KG. The transparency and explicitness of these rules boost the understandability of
the reasoning processes, which is vital for establishing trust and accountability, particularly
in critical areas such as healthcare, finance, and law.
Historically, symbolic methods have been pivotal in tackling the described downstream tasks,
achieving significant results. Fordeductive reasoning, which corresponds to KG completion within
KG reasoning,Markov Logic Network (MLN) and Probabilistic Soft Logic (PSL) are notable
symbolic methodologies that have been extensively utilized. Additionally, forinductive learning,
which corresponds to rule learning in KG reasoning,Inductive Logic Programming (ILP) proves
tobeanessentialapproach.Thesewell-establishedtechniquesbuilduponlogicalreasoningandrule-
based systems, exhibiting their effectiveness across a wide range of domains. However, in recent
years, we have witnessed the emergence of neural systems, which introduce a fresh perspective
and innovative solutions to these tasks. These neural approaches aim to learn embeddings that
encode the complex patterns of interconnections within the KG for predicting missing triples.
The integration of symbolic and neural techniques marks a new era in KG reasoning, as exempli-
fied by our proposed taxonomy (Figure2), which showcases the blending of these methodologies.
Figure 3 presents a comprehensive classification designed specifically for neural-symbolic KG
reasoning methods, providing an intuitive overview of the various approaches employed in this
field.
Moving from left to right along the figure, the methods progressively shift their focus towards
KG completion, while diminishing their emphasis on rule discovery. For instance, at the far left,
we have pure rule learning methods like AMIE, which primarily concentrate on elucidating the
process of rule learning from data, without delving into the application of these rules for KG
completion. Conversely, as we move from top to bottom in the figure, the methods increasingly
prioritize neural techniques over symbolic methods. For example, at the very top, we have pure
symbolic reasoning methods such as ILP and MLN, which primarily depend on logical inference
and a rule-based approach. However, as we descend down the figure, the prominence of symbolic
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:6 K. Cheng et al.
Fig. 3. Classification of different neural-symbolic methods.
methods diminishes, giving way to the rise of neural approaches that leverage machine learning
algorithms to tackle KG reasoning tasks.
3 Background and Preliminary
In this section, we aim to elucidate the interplay between neural symbolic reasoning and its
underlying prerequisites, background knowledge about KGs, and symbolic logic. To facilitate a
better understanding of the symbolic component within the context of KGs, we put forth a formal
definition of KGs and offer a concise introduction to symbolic logic. By integrating the concept of
symbolic logic, we redefine the notion of a KG in the language of symbolic logic, thereby enriching
readers’ comprehension of this fundamental aspect.
3.1 Knowledge Graph
A KG, denoted byG = {, ', $ }, consists of a set of entities, a set of relations' and a set
of observed facts$ = {(48, A:, 49 ) |48, 49 ∈, A : ∈'}. An observed fact in$ is represented
by a triple(48, A:, 49 ), where48 ∈, 49 ∈, andA: ∈' denote a subject entity, object entity,
and relation, respectively. Every relationA: is associated with an||×| |matrix M(:), in which
the elementM(:)
8 9 = 1 if the triple(48, A:, 49 )∈ $, and 0 otherwise. Paths play a crucial role in
KGs as they carry a wealth of semantic information. Specifically, we can depict a path in KG as
? = 40
A1
− →41
A2
− →. . .
A=
−→4=, where40 represents thesource entity,4= signifies thetarget entity, and
A8 symbolizes the relation linking48−1 and48 . By removing the entities from the path, we obtain the
relation path[A1, . . . , A =]. We define the set of entities connected as the tail entities of relationA8
within the relation path asrange(A8 )and domain(A8+1)indicates the set of entities where relation
A8+1 originates from. Similarly,domain(?)represents the set of entities connected as source entities
of the relation path[A1, . . . , A =], whilerange(?)denotes the set of entities connected as target
entities of the relation path[A1, . . . , A =].
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:7
3.2 Symbolic Logic
Inourdailylife,astatementiswidelyusedtomakeadeclaration,whichiseither True orFalse.These
statementsarecalledpropositionsandaredenotedwithsymbolssuchas % and&.Afamousexample
of a proposition is“Socrates is a man,”which isTrue. Propositional logicdeals with propositions and
relations between them, which is also calledzeroth-order logic. If a proposition cannot be broken
down into smaller propositions, it is calledatomic propositions. Examples of the atomic propositions
include “All men are mortal,” “Socrates is a man,”and “Socrates is mortal,”which can be denoted as
%,&, and', respectively. Each atomic proposition is assigned a binary truth value, which is called
an interpretation. For example,% is True, denoted as (%)= 1.
Atomic propositions can be used to define more complex propositions via logical connectives
(or logical operators), includingnegation (¬), disjunction (∨), conjuction (∧), andimplication (→).
Logical connectivescan be considered as functions that take propositions as arguments and output
more complex ones. The truth value of the composite proposition is determined by the truth table of
each logical connective. For example, (¬%)= 0, if (%)= 1. These operators are not independent,
and any two of them can define the other two.
With a set of atomic propositions and logical connectives, we can recursively define all valid
logical expressions, which are calledwell-formed formulas. Atomic formulas or atoms are well-
formed formulas with no logical connectives. In propositional logic,atomic formulasare essentially
atomic propositions. Formulas are usually denoted asq,k, andj. Given two well-formed formulas
q andk, (1)q ∧k, (2)q ∨k, (3)q →k, and (4)¬q are all well-formed formulas.
Based on the logical language defined above, we can leveragea rule of inferencein propositional
logic, such asModus Ponens, to deduce new propositions from existing ones. Modus Ponens says if
the premisesq andq →k are bothTrue, then the conclusionk is alsoTrue, which can be verified
by the truth table. There are other inference rules, and Modus Ponens is the simplest and most
popular one.
While propositional logic serves well in presenting fundamental concepts about individual
objects, it is limited in its expressive power and can only deal with simple propositional statements
that are eitherTrue or False. It cannot represent more complex structures, such as relationships
between objects or properties of objects, and does not allow for quantification. For example,“All
men are mortal”can only be represented as an atomic proposition% in propositional logic without
further exploring its inner structure. To address the limitation, FOL (also known as predicate
logic) extends propositional logic by (1) enriching atom representation with objects, functions, and
predicates and (2) introducing variables and quantifiers to formulas. Different from propositional
logic, where atomic formulas (atoms) are atomic propositions, FOL atoms have a much richer
internal structure. The atoms in FOL contain three types of symbols related toobjects, functions,
and predicates, which are introduced below.
— Objects: Objects refer to things that are of interest, which could be persons, numbers, locations,
etc. If an object is known, we use aconstant to denote it; otherwise, we use avariable to
denote it, which will be explained later. For example,Socrates is an object constant. An object,
either a constant or a variable, is aterm. Objects correspond to entities in KGs.
— Functions: Functions take terms as arguments and output objects. An=-ary function can be
written as5 (C1, . . . , C =), whereC1, . . . , C = are terms. For example, the functionFatherOf(Socrates)
can be interpreted as“the father of Socrates”. Functional expressions are alsoterms. Functions
do not typically exist in KGs.
— Predicates: Predicates take terms as arguments and outputTrue or False. An=-ary predicate is
written as% (C1, . . . , C =), whereC1, . . . , C = are terms. A predicate is an atom. For example, the
predicateMen(Socrates) isanatom.Itmeans “Socrates is a man”,whichcanonlyberepresented
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:8 K. Cheng et al.
as an atomic proposition& in propositional logic. In most existing KGs, only binary predicates
are considered. For example,Founded(Bill Gates, Microsoft)is a binary predicate. If a predicate
takes object constants as the arguments, it is called aground predicate. BothMen(Socrates)
and Founded(Bill Gates, Microsoft)are ground predicates.
In order to accommodate the situations thatall or some of the objects have some property, FOL
introduces object variablesand quantifiers, which are discussed below.
— Variables: In contrast to the object constants, variables denote any objects, which can be
considered as a placeholder. A variable is also a term, which can be the arguments of functions
and predicates. For example,Men(G)contains a variableG, which can be interpreted asG is a
man. Atoms and well-defined formulas may include variables, such asMen(G)and Founded(x,
Microsoft).
— Quantifiers: Universal quantifier(denoted as∀) andexistential quantifier(denoted as∃) are
used to describe whether all objects or some objects make a formulaTrue. Assumeq is a
well-defined formula with a variableG, both(∀G)q and (∃G)q are well-defined formulas. For
example, we can use(∀G)(Men(G)→ Mortal(G))to represent “All men are mortal.”
Well-formed formulasin FOL can be recursively defined over atoms via logical connectives and
quantifiers. An example of a well-formed formula is(∃G)(Founded(x, Microsoft)∧Born(x, Seattle )),
representing “there exists a person who founded Microsoft and was born in Seattle.”
All theinference rulesin propositional logic work in FOL. There are two additional inference
rules, which are calledUniversal Instantiation(UI) andExistential Generalization(EG). UI allows us
to infer a specific instance of a universally quantified statement. For example, from the statement
(∀G)(Men(G) →Mortal(G)), we can inferMen(Socrates) → Mortal(Socrates). EG allows us to
generalize a statement about a specific instance to a statement about a whole class of instances.
For example, from the statementMortal(Socrates), we can infer(∃G)Mortal(G), which means “there
exists at least one person that is mortal.”
3.3 Knowledge Graph in the Language of Symbolic Logic
In the area of symbolic logic, entities in a KG can be considered asconstants and relations are
called predicates. In the KG setting, each predicate is a binary logic symbol taking two arguments,
which can be denoted asA: (·, ·). A ground predicate(or anatom or anatomic formula) is a predicate
whose arguments are all instantiated by particular constants. For example, we may have a predicate
Friend(·, ·).ByassigningconstantsAliceandBobtoit,wegetagroundpredicate Friend(Alice, Bob).
A triple(48, A:, 49 )is essentially a ground predicate, denoted asA: (48, 49 )in the language of logic. In
the reasoning task, a ground predicate can be regarded as a binary random variable:A: (48, 49 )= 1
when the triple(48, A:, 49 )holds true, andA: (48, 49 )= 0 otherwise. Apossible worldassigns a truth
value of 0 or 1 to each possible ground predicate. It represents a particular configuration of truth
values for the predicates, capturing a state or interpretation of the KG.
3.4 Logical Rules in the Context of Knowledge Graph
The concepts in symbolic logic, including logical rules, are closely connected to the concepts in KGs.
In the previous sections, we have mentioned some of the connections. We now summarize them in
this section using the example KG in Figure4. Table2 provides a comparison of how concepts are
expressed in the languages of symbolic logic and KG.
Constants in FOL correspond to entities in KGs, e.g.,“Amy”. Predicates correspond to relations
in KGs, which are binary, e.g.,hasGrandma(G,~). Ground predicates correspond to triples in KGs,
e.g., hasGrandma(Amy, Cara), or(Amy, hasGrandma, Cara)in the triple form.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:9
Fig. 4. An example of Kinship KG. A closed path in the Kinship KG corresponding to the rule
hasGrandma(Amy, Cara)←hasMother(Amy, Bess)∧hasMother(Bess, Cara)is highlighted by a red dotted
triangle.
Table 2. Comparison of Concepts in the
Language of Symbolic Logic vs KG
Symbolic Logic Knowledge Graph
Constants Entity
Predicate Relation
Ground predicate Triple
Rule Instance Closed Path
A chain-like Horn rule instance can be easily identified as a“closed path”in a graph, where the
rule body corresponds to a path in the KG, and the rule head corresponds to the edge connecting
the starting entity and ending entity in the rule body. For example, given the KG in Figure4, we
can observe closed paths (rule instances) such as:
CP1 := Amy
hasMother
− −−−−−−− →Bess
hasMother
− −−−−−−− →Cara
hasGrandma
←−−−−−−−−−Amy
CP2 := Dana
hasMother
− −−−−−−− →Eva
hasMother
− −−−−−−− →Faye
hasSon
−−−−−→Gino
hasUncle
←−−−−−−Dana
(1)
4 Link Prediction
A KG is composed of a set of known facts, which can be obtained from various external sources.
However, due to the vastness of the real world, it is not feasible to collect all possible facts,
resulting in significant sparsity within KGs. KG reasoning plays a crucial role in addressing this
issue by leveraging existing facts to infer missing knowledge. It serves as a vital component
for the success of numerous downstream tasks and has garnered considerable attention within
the research community. Given the observed facts and their corresponding ground predicates
v$ = {A: (48, 49 )|(48, A:, 49 )∈ $}, the task ofKG completionis to predict the truth value of ground
predicates v = {A: (48, 49 )|(48, A:, 49 )∈  }for all remaining hidden triples, where = {48, 49 ∈
, A: ∈', (48, A:, 49 )∉ $}.
4.1 Symbolic Reasoning
Traditional logical inference approaches rely on a predefined set of logical rules, denoted asF, to
complete the KG as shown in Figure5. The fundamental idea is to find the assignment of truth
values tov that maximizes the number of satisfied ground rules. Based on the assigned truth
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:10 K. Cheng et al.
Fig. 5. Symbolic reasoning over a toy example of KG.Left: A toy example of KG.Right: A predefined logical
rule. The new fact denoted as the red dotted line can be inferred from the logical rule and the KG.
values to each ground predicate, existing symbolic methods can be broadly categorized into two
groups: logical inference for boolean logic, whereA: (48, 49 )∈ 0, 1 for allA: (48, 49 )∈ v$ ∪v , and
logical inference for probabilistic logic, whereA: (48, 49 )∈[ 0, 1]for allA: (48, 49 )∈ v$ ∪v .
4.1.1 Logical Inference for Boolean Logic. In boolean logic, the truth values of predicates are
restricted to binary values, either 0 or 1. The goal is to determine the assignment of truth values
to the predicates in the KG that maximizes the satisfaction of the logical rules. By evaluating the
truth values of predicates, boolean logical inference enables the inference of missing information
and the completion of the KG.
The optimization of logical inference for boolean logic becomes challenging due to the use of
boolean variable assignments. The task of finding the boolean assignment tov that maximizes the
satisfaction of ground rules can be mathematically formulated as a MAX-SAT problem. Notably,
the MAX-SAT problem is known to be NP-hard [81]. Complete search methodsexplore the entire
solution space systematically to find an optimal or near-optimal solution for the MAX-SAT problem.
ExamplesofcompletesearchmethodsforMAX-SATincludetheDavis-Putnam-Logemann-Loveland
algorithm [22], which forms the basis for modern SAT solvers, and the Conflict-Driven Clause
Learning algorithm [67]. These methods guarantee to find the best possible solution, but their
computational complexity makes them infeasible for large instances.
Given the complexity of the problem, the objective of MAX-SAT solvers is typically to obtain
high-quality solutions within a reasonable timeframe rather than solving the problem exactly.
Representative methods forapproximate solutionscan be broadly classified into three categories.
The first category islocal search methods. These iterative algorithms start with an initial solution
and iteratively choose a variable, flipping its value to improve the assignment until a termination
condition (e.g., a time limit) is met, returning the best-found assignment. Local search methods do
not guarantee optimality but can be highly effective at finding good solutions within a reasonable
timeframe. Common local search algorithms for MAX-SAT include the WalkSAT algorithm [46],
Tabu search [36], and Simulated Annealing [106]. These algorithms often employ heuristics to guide
the search process and escape local optima. The second category consists ofbranch and bound
(BnB) techniques. BnB techniques divide the search space into smaller subproblems and perform
an exhaustive search while maintaining upper and lower bounds on the solution quality. These
techniques prune branches that cannot yield better solutions than the current best-known solution.
BnB algorithms for MAX-SAT improve efficiency by intelligently selecting variables for branching
based on heuristics or learned information. The third category isgreedy algorithms. In the context
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:11
of MAX-SAT, greedy algorithms construct a partial assignment incrementally, greedily selecting
literals that maximize the number of satisfied clauses. While greedy algorithms are computationally
efficient, they often yield suboptimal solutions. However, they can serve as effective initial solutions
for more sophisticated methods. By employing these different approaches, MAX-SAT solvers aim
to strike a balance between solution quality and computational efficiency, addressing the inherent
complexity of the problem.
4.1.2 Probabilistic Extension of FOL. Boolean logic has demonstrated effectiveness in capturing
complex relationships and knowledge about the world. However, its rigid nature often limits its
ability to handle uncertainty and noise commonly encountered in real-world applications. To
overcome this limitation, researchers have proposed various approaches that aim to integrate
logical reasoning with statistical techniques. These approaches seek to harness the expressiveness
of FOL while leveraging the robustness offered by probability-based methods. By combining these
two paradigms, probabilistic extension of FOL strives to create a unified framework that can handle
both the intricacies of complex relationships and the uncertainties inherent in real-world scenarios.
MLN. To compactly specify probability distributions over complex relational domains, MLN [92]
offers a probabilistic extension of FOL through the utilization of probabilistic graphical models.
MLN defines a Markov network by considering a set of FOL formulas, denoted asF, along with
their corresponding weight vectorw. In this framework, each ground predicate is represented by a
node in the network, and each ground rule corresponds to a feature. The weights assigned to these
features correspond to the weights of the original FOL rules. Consequently, the joint probability of
all triples within the network is defined as follows:
?w (v$, v )= 1
/ (w)exp
( Õ
8:8 ∈F
F8=8 (v$, v )
)
, (2)
whereF8 is the weight for the FOL formula8 , which can be learned duringweight learning, and
=8 (v$, v )is the number of true groundings of8 based on the values ofv$ and v , and/ (w)is a
normalization constant to make the probabilities of all worlds to sum to one.
MLN inference poses significant computational challenges due to its ability to encompass both
#P-complete probabilistic inference and NP-complete logical inference. As a result, achieving exact
inference in MLN is often computationally intensive. To tackle this issue, MLN commonly em-
ploys Markov chain Monte Carlo (MCMC) techniques, with Gibbs sampling being a prevalent
choice [9, 83]. The underlying principle of Gibbs sampling is to iteratively sample each ground
predicate, conditioned on its corresponding Markov blanket. TheMarkov blanket of a ground
predicate comprises the set of other ground predicates that appear alongside it in any ground rule.
In addition to MCMC methods, belief propagation has emerged as another popular technique for
MLN inference [104, 132]. Belief propagation leverages message-passing algorithms to efficiently
compute approximate probabilities in graphical models. These methods offer a means of obtain-
ing approximate solutions for MLN inference tasks, striking a balance between computational
complexity and solution quality.
PSL. PSL [2] offers an alternative probabilistic extension of FOL. It leverages FOL rules as a
template language for constructing graphical models over random variables with soft truth values.
This allows for efficient inference by formulating the underlying problem as a convex optimization
task. In PSL, the soft truth values are represented as real numbers in the interval [0, 1], denoted as
 (A: (48, 49 )), indicating the likelihood of the corresponding ground predicateA: (48, 49 )being true.
An interpretation, denoted as : A: (48, 49 )→[ 0, 1]=, maps the ground predicates in a KG to their
soft truth values.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:12 K. Cheng et al.
To determine the degree to which a ground rule is satisfied, PSL employs the Łukasiewicz t-norm
[42] and its corresponding t-conorm as relaxations of the logical AND and OR operations. The
relaxation functions for the logical operators are defined as follows:
 (58 ∧59 )= max(0,  (58 )+ (59 )−1)
 (58 ∨59 )= min(1,  (58 )+ (59 ))
 (¬58 )= 1 − (58 ).
Here, 58 and 59 can represent either ground rules or atomic formulas (e.g.,A: (48, 49 )). The satisfaction
of a ground rule is determined by an interpretation of the atoms within the rule, resulting in a
notion calleddistance to satisfaction. This measures the extent to which a ground rule5 is violated.
It is worth noting that a ground logical rule can be transformed from an implication form to a
disjunction form as shown below:
Ahead ←Abody ≡Ahead ∨¬Abody, (3)
whereAhead denotes the head of a rule andAbody denotes the body of a rule. By applying the above
definitions of the logical operators to a ground logical rule in disjunction form, the distance to
satisfaction of a ground logical rule can be computed as:
35 ()= max{0,  (Abody)− (Ahead)}.
We can observe that a ground rule5 is satisfied if and only if the truth value of its head (Ahead)is
the same or higher than its body (Abody).
Given a set of ground atoms, a PSL program induces a distribution over possible interpretations
. LetFbe the set of all ground rules that are instances of a rule in the program. The probability
density function over is defined as:
1
/ (w)exp

Õ
8:58 ∈F
F8 (358 ())?

. (4)
In this equation,F8 represents the weight of the ground rule58 ,/ (w)is the continuous version of
the normalization constant forw ensuring the probabilities of all interpretations sum up to one, and
? ∈{1, 2}represents a choice between two different loss functions. The linear loss function(? = 1)
favors interpretations that completely satisfy individual rules, even if it results in a higher distance
to satisfaction for conflicting rules. On the other hand, the quadratic loss function(? = 2)favors
interpretations that satisfy all rules to some degree, often leading to truth values that are farther
away from the extreme values. This formulation enables PSL to model probabilistic dependencies
and reason about uncertainty in relational domains by combining the expressiveness of FOL with
the flexibility of probability-based reasoning.
4.2 Neural-Based Reasoning
In recent years,knowledge graph embedding (KGE) has gained popularity for its scalability in
completing KGs. Unlike traditional symbolic reasoning methods, KGE solely relies on observed
facts within the KG, without leveraging explicit logical rules. The fundamental idea behind KGE
is to represent entities and relations in the KG as continuous low-dimensional vectors, capturing
their semantic similarities [115]. The key component of KGE models is the score function, which
quantifies the plausibility of triples within the KG. We denote the score of a triple(48, A:, 49 )
calculated by the score function as5A: (48, 49 ). A higher value of5A: (48, 49 )generally indicates a
greater plausibility for the triple(48, A:, 49 ). Despite the remarkable performance of KGE methods,
their limitation lies in the fact that they ignore potential high-order constraints specified by logical
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:13
rules,whichrestrictstheir applicationinmorecomplexreasoningtasks.Furthermore,KGEmethods
are often considered black-box models, lacking explicit reasoning evidence. Existing KGE methods
can be broadly categorized into three main categories:translation-based models, bilinear models,
and deep learning-based models. These approaches aim to enhance the representation and scoring
capabilities of KGE models, allowing for more accurate and expressive KG completion.
4.2.1 Translation-Based Models. TransE [7] stands as the most representative translation-based
model,pioneeringtheuseofthetranslationalprincipleforKGembedding.TransEaimstosatisfythe
conditione8 +r: ≈e9 whenatriple (48, A:, 49 )holds,where e8, r:, ande9 representthecorresponding
representation vectors for entities48, A:, and49 , respectively. The score function of TransE is defined
as the negative distance betweene8 +r: and e9 :
5A: (48, 49 )= −
e8 +r: −e9
2
2 . (5)
Although TransE has proven effective, it falls short in addressing 1-to-N, N-to-1, and N-to-N
relations. For instance, in a 1-to-N relation such ashasCoauthor, where multiple co-authors like
Peter Dayan, Yann LeCun, andMax Wellingare associated withGeoffrey Hinton, TransE enforces
similar vector representations for allGeoffrey Hinton’s co-authors to satisfy the score function
defined in Equation (5), even though these co-authors may have distinct leisure interests. To address
these limitations, TransH [119] allows entities to have different representations when involved in
different relations. Furthermore, TransR [61] enhances TransE by distinguishing the entity space
from the relation space. Additionally, TransD [47] and TranSparse [48] build on TransR, offering
modifications for more efficient and interpretable representations.
In contrast to the above variants of TransE, several other approaches relax the requirement of
strict equalitye8 +r: ≈e9 in TransE to address the challenges of various relation types. Some
notable methods include TransM [29] and TransG [122]. These advancements aim to enhance
translation-based KG embedding techniques, addressing the challenges posed by different types of
relations and achieving more accurate and comprehensive KG representation.
4.2.2 Bilinear Models. Instead of adhering to the translational principle for KG embedding,
bilinear models employ tensor products to learn entity and relation embeddings. The formulation
is given by:
5A: (48, 49 )= e8 MA: e9
Here, MA: represents an asymmetric matrix that captures the interactions of latent components
specific to the relationA: .
The first bilinear model, RESCAL [78], introduced this concept. However, RESCAL suffers from
high computational complexity since its relation matrix models pairwise interactions between
all components of entity pairs. To address these limitations, DistMult [127] simplifies RESCAL
by constrainingMA: to diagonal matrices. DistMult demonstrates efficiency and effectiveness in
various applications, but it can only handle symmetric relations, which is insufficient for real-world
KGs. To model asymmetric relations, SimplE [53] extends DistMult to allow for the independent
learning of two embeddings for each entity, representing the head and tail entities separately while
ComplEx [109] extends DistMult by representing entities and relations in the complex vector space,
whichenablesdifferentscoringoffactsinvolvingasymmetricrelationsbasedontheorderofentities.
ComplEx-N3 [56] further extends ComplEx with weighted nuclear 3-norm. HolE [77] combines the
strengths of RESCAL and DistMult by introducing a circular correlation operation that captures
compositional representations of pairwise entities with lower computational complexity than the
tensorproductusedinRESCAL.ANALOGY[ 62]extendsRESCALtomodeltheanalogicalproperties
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:14 K. Cheng et al.
of entities and relations. TuckER [4], on the other hand, employs Tucker decomposition to factorize
the third-order tensor comprising KG triples for learning entity and relationship representations.
4.2.3 Deep Learning-Based Models. Due to the promising results of deep learning models, such
as theconvolutional neural network (CNN) [58], therecurrent neural network (RNN) [100],
Transformers [112] and thegraph neural network (GNN) [55], over various domains, such
as computer vision, natural language process, and graph learning, several attempts are made to
leverage these deep learning models to embed entities and relations in KGs.
General Neural Networks-Based Models: The first attempt to leverage neural networks for learning
the confidence of triples in KGs was made bySemantic Matching Energy (SME) [6]. SME
combines the relationA: with the head entity48 to obtain6D (48, A: ), and also combines the relation
A: with the tail entity49 to obtain6D (49, A: ). The score of a fact is defined by taking the dot product
between the matching6D and6E. Another neural network architecture for KG embedding learning,
called Neural Tensor Network (NTN) [105], proposes a different approach. NTN combines
entities48 and49 using a relation-specific tensor and then applies a relation-specific linear output
layer to calculate the score of the fact.
CNNs-Based Models: ConvE [26] makes the first attempt to use the CNN framework for KG
embedding learning. This approach harnesses the expressive power of 2D convolutions to capture
interactions between entity embeddings and relation embeddings. In ConvE, the head-entity
embedding and relation embedding are reshaped into 2D embeddings and concatenated to create an
input matrix for the 2D convolution layer. The resulting feature map tensor is then vectorized and
passed through a linear transformation. The score of a fact is defined by taking the inner product
between the output of the linear transformation and the tail-entity embedding. Mathematically, the
score function5A: (48, 49 )for a fact is given by:
5A: (48, 49 )= 5 (vec(5 ([ei; rk]∗l))W)ej.
Here, l represents the convolutional filters,∗denotes the convolution operation, and vec is
the operation that vectorizes a tensor.5 denotes a non-linear function.ei and rk denote the 2D
reshaping ofei and rk, respectively. Ifei, rk ∈R3 , thenei, rk ∈R3F ×3ℎ , where3 = 3F ×3ℎ.
To simplify the 2DConvolutional Embedding (ConvE) model, ConvKB [76] introduces the
usage of 1D convolution with a filterl ∈R3×1. The objective of this approach is to effectively
capture the translation relationship within a triple. On the other hand, ConvR [51] extends the
globalfiltersutilizedinConvEtorelation-specificfilters.Bydoingso,ConvRenhancesthemodeling
capacity of ConvE by incorporating filters that are specific to each relation. Furthermore, InteractE
[110] introduces additional convolution operations to capture a wider range of interactions among
embeddings. Additionally, HypER [3] adopts hypernetworks based on ConvE. By doing so, HypER
enhances the expressive power of the ConvE model by incorporating relation-specific convolutional
filters.
RNNs and Transformers-based Models: Most KGE methods primarily focus on learning KG embed-
dings at the triple level, which often lacks the ability to capture long-term relational dependencies
among entities. To address this limitation,recurrent skipping networks (RSNs) [38] have been
introduced. RSNs combine RNNs with residual learning techniques to capture the long-term re-
lational dependencies present in KGs. By incorporating RNNs and residual connections, RSNs
can effectively model the intricate relationships and dependencies among entities. In addition
to RNN-based models, Transformer-based architectures have gained significant attention for KG
embedding tasks. Transformers have demonstrated excellent performance in learning contextual-
ized representations for natural language processing tasks. Leveraging the contextual information
available in KGs, CoKE [114] utilizes Transformers to encode edge information and path sequences.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:15
This approach aims to capture the contextual relationships and dependencies among entities and
relations in the KG. Moreover, inspired by the success of pretraininglanguage models (LMs) ,
KG-BERT [130] adopts the Bidirectional Encoder Representations from Transformers (BERT) model
as an encoder for entities and relations. KG-BERT leverages the pretraining of BERT on large-scale
text data and then fine-tunes it on KG-specific tasks. By doing so, KG-BERT effectively captures
the contextual semantics and representations of KG entities and relations, enabling improved
performance in various KG reasoning tasks.
GNNs-Based Models: In recent years, GNNs have gained significant popularity for encoding
the relational dependencies among entities and relations in homogeneous graphs. To cater to the
multiple relations present in KGs, R-Graph Convolutional Network (GCN) [98] extends the
transformation weights in GCNs to relation-aware weights. This enables R-GCN to effectively
capture the local graph structures and features of entities, thereby enhancing its representation
learning capabilities. For relation prediction, R-GCN utilizes DistMult as the decoder to score
a triple based on the encoded entities. Another approach, SACN [101], employs ConvE as the
decoder, while the encoder remains a relation-aware GCN. By using ConvE as the decoder, SACN
benefitsfromitsabilitytomodelcomplexinteractionsandcapturetranslationrelationshipsbetween
entities in KGs. M-GNN [37] introduces a modification to the R-GCN architecture by replacing
the mean aggregator in each graph convolution layer with amulti-layer perceptron (MLP) .
This modification supports the injective property, ensuring that two entities are mapped to the
same location only if they possess identical neighborhood structures with identical embeddings of
corresponding neighbors. By incorporating the MLP aggregator, M-GNN enhances the expressive
power of the model and improves its ability to capture nuanced relationships in KGs. In addition
to relation-aware transformation weights, VR-GCN [131] and CompGCN [111] address the issue
of overparameterization by introducing the concept of sharing a relation embedding calculated
using basis decomposition across layers. This sharing mechanism reduces the redundancy and
overparameterization in the model, leading to improved efficiency and generalization performance.
Overall, these approaches demonstrate the diverse techniques employed to effectively encode
KGs using GNNs, incorporating relation-aware weights, different decoders, and addressing overpa-
rameterization challenges.
4.3 Training Objective
To train embedding models, a common approach is to use a margin-based pairwise ranking loss as
the objective function. The loss aims to distinguish between positive triples observed in the KG and
negative triples that serve as contrastive examples. The pairwise ranking loss is defined as follows:
Õ
(48,A:,49 )∈$
Õ
(4′
8 ,A:,4′
9 )∈N(48,A:,49 )
max(0,W −5A: (48, 49 )+ 5A: (4′
8 , 4′
9 )). (6)
In this equation,$ represents the set of observed facts in the KG. For each positive triple
(48, A:, 49 ), negative samples(4′
8 , A:, 4′
9 )are selected from the set of negative triplesN(48, A:, 49 ). The
margin parameterW is used to create a separation between the scores of positive and negative
triples. The score5A: (48, 49 )of a triple(48, A:, 49 )is calculated using the scoring function specific to
the embedding model. Various scoring functions exist in the field of KGE models, each capturing
different characteristics and relationships within the KG.
To reduce the impact of randomness, multiple negative triples are sampled for each positive
sample. The set of negative triplesN(48, A:, 49 )for a positive triple(48, A:, 49 )is constructed based
on the closed world assumption. This assumption assumes that all facts not present in the KG are
false. Specifically, negative triples are created by selecting triples that are the same as the positive
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:16 K. Cheng et al.
triple, except for the head or tail entity, from a pool of potential negative samples as shown in
Equation (7).
N(48, A:, 49 )= {(48 ′, A:, 49 )|(48 ′, A:, 49 )∉ O}∪{( 48, A:, 49 ′)|(48, A:, 49 ′)∉ O}. (7)
By optimizing the objective function defined by Equation (6), embedding models can effectively
learn representations that capture the semantic relationships between entities and relations in KGs.
4.4 Symbolic-Enhanced Representation Learning
Traditional logical inference approaches have excelled in interpretability and generalizability
by leveraging symbolic reasoning. However, they encounter challenges in scalability and the
exploration of inherent correlations among atoms within a KG. On the other hand, KGE methods
have demonstrated strong scalability and the ability to capture correlations among atoms, but
they struggle to model higher-order dependencies of KG relations. To address these limitations,
recent studies have aimed to combine both approaches, aiming to leverage the respective strengths
of each.
The existing works on combining embedding models with pre-defined logic rules can be broadly
categorized into two classes. The first class involvesdesigning embedding-based variational dis-
tributions for the variational inference of MLNs. This approach aims to incorporate the flexibility
and expressiveness of embedding models into the probabilistic framework of MLNs. By using
variational inference, the joint distribution of MLN weights and embedded representations can be
approximated effectively. The second class of approaches focuses ondesigning PSL-based regular-
ization techniques for embedding models. PSL provides a declarative language for defining logical
rules and constraints. By incorporating PSL-based regularization, embedding models can learn
representations that align with the logical rules and capture the inherent dependencies among KG
entities and relations.
The goal of these combined approaches is to enhance the performance and capabilities of KG
reasoning by synergistically integrating the strengths of embedding models and logical inference.
By doing so, researchers aim to achieve a more comprehensive and accurate representation of KGs
while maintaining interpretability and scalability.
4.4.1 Embedding-Based Variational Inference of MLN. MLN is a probabilistic graphical model
that combines probability and FOL to handle uncertainty as introduced in Section4.1.2. It naturally
has the ability to integrate the KG embedding and logical rules. Given the computational challenges
of exact inference in MLNs, variational inference offers an efficient approximate solution to the
inference problem. Embedding-based variational inference approaches have been proposed to
leverage graph embedding and define a variational distribution for all possible hidden triples in the
KG, enabling efficient variational inference of MLN. We now use pLogicNet [87] as an example
to illustrate the procedure. pLogicNet aims to train the MLN model by optimizing theevidence
lower bound (ELBO) for the likelihood function of observed triplesv$ :
log ?w (v$ )≥L( @\ , ?w)
= E@\ (v )[log ?w (v$, v )−log @\ (v )]. (8)
It is defined as the sum of the expected log-likelihood of the observed triples under the variational
distribution and the KL divergence between the variational distribution and a prior distribution.
Maximizing the ELBO effectively optimizes the MLN model parameters. The variational distribution
@\ (v )is defined using a KGE model, by assuming each triple independently follows a Bernoulli
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:17
distribution, with parameters specified by the embedding score function:
@\ (v )=
Ö
(48,A:,49 )∈
@\ (A: (48, 49 ))
=
Ö
(48,A:,49 )∈
Ber(A: (48, 49 )|5A: (48, 49 )),
(9)
where Ber represents the Bernoulli distribution and5A: (48, 49 )is an embedding score function
denoting the probability of triple(48, A:, 49 )to be true. For example, in DistMult,5A: (48, 49 )can be
defined asf (e)
8 diag(r: )e9 ). This lower bound can be effectively optimized using variational EM
algorithm [74]. In variational E-step,?w is fixed and@\ is updated to minimize the KL divergence
between@\ (v )and?w (v |v$ ). In M-step,@\ is fixed and the weights of the rulesw are updated to
maximize the joint probability of both observed and hidden triples (i.e.,E@\ (v )[log ?F (v$, v )]).
By integrating embedding models and logical rules in this way, the embedding-based variational
inference approach of MLN can leverage the strengths of both paradigms. The learned KG embed-
dings capture the rich semantic information, while the MLN captures the logical dependencies and
uncertainty in the KG. This combination enables more accurate and interpretable KG reasoning.
While pLogicNet employs KG embedding to define the variational distribution for triples in
KG, other approaches, such as ExpressGNN [137] and pGAT [44], take advantage of GNNs and
graph attention neural networks, respectively, for variational inference in MLN. These models
leverage the power of neural networks to capture complex dependencies and interactions within
the KG. In addition to variational inference methods, there are other approaches that aim to reduce
computational costs in integrating embedding models and logical rules. For example, INS-ES [120]
adopts a strategy of selecting a small subset of candidate triples based on their similarity to the
input query, using KG embedding. By focusing on relevant candidates, the construction of the
ground Markov networks becomes more efficient, leading to improved inference speed.
Summary: While embedding-based variational inference approaches for MLN offer an elegant
solution to integrate embedding models and logical rules through variational inference, they still
face a significant challenge in terms of inference efficiency. Optimizing MLN using variational
inference methods becomes computationally infeasible when considering all possible hidden triples.
To address this challenge approaches in this category resort to sampling a subset of hidden triples
to reduce computational complexity. However, this sampling strategy inherently introduces infor-
mation loss from the logical rule side. Efforts are being made to mitigate the information loss from
logical rules while still maintaining reasonable computational efficiency. These include developing
advanced sampling strategies, optimizing the trade-off between sample size andaccuracy (ACC),
and exploring techniques to better approximate the inference process. Overcoming these challenges
is crucial to further enhance the integration of embedding models and logical rules for effective
and efficient KG reasoning.
4.4.2 PSL-Based Regularization Techniques for Embedding Models. In addition to MLN, PSL
[2] provides another probabilistic extension of FOL. It uses FOL rules as a template language for
graphical models over random variables (i.e., triples) with soft truth values, where KG embedding
can be used to define the soft truth values.Thus, logical rule-based regularization methods leverage
PSL to integrate the KG embedding and logical rules instead.They treat logical rules as additional
regularization, where the satisfaction of ground rules, which can be calculated following PSL, is
integratedintotheoriginalembeddingloss.MostoftheexistingmethodstocombineKGembedding
and logical rules fall into this category. A typical integration is defined as follows: (1) sampling
ground logical rules given the template logical rules, (2) mapping each related triple (i.e., ground
predicate) into a soft truth value (i.e., (A: (48, 49 ))), (3) computing satisfaction of each ground
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:18 K. Cheng et al.
rule based on the soft truth value of ground predicates in it, and (4) defining proper loss based
on the satisfaction of all the ground rules. We now use KALE [39] as an example to illustrate
the procedure described above. First, a set of positive and negative ground rules (i.e.,5 + and
5 −) are sampled given the template logical rules. Together with atomic formulas (i.e., positive
and sampled negative triples), we have the whole set of sampled formulas. Second, each ground
predicateA: (48, 49 )is assigned a soft truth value, which is a transformation of the TransE-based
score function: (A: (48, 49 ))= 1 − 1
3
√
3
e8 +r: −e9

1, wheree8 , r: , ande9 are embedding vectors to
the corresponding entities and relations and3 is the dimensionality of the embeddings. Third, the
soft truth value of a ground rule (i.e.,5 +or 5 −) is computed following PSL. Finally, KALE defines
a loss function over all sampled formulas. Similar to margin-based ranking loss, embeddings are
learned by maximizing the difference between the soft truth value of positive formulae (5 +)and
its negative samplings (5 −). Note that, by removing ground rules from the whole set of sampled
formulas, the loss degenerates to regular TransE-based embedding loss. Rocktäschel [94] also
devised a model similar to KALE. However, instead of learning entity embeddings for the individual
entities, they utilize matrix factorization to learn joint embeddings of pairs of entitiesv48,49 as well
as embeddings of relationsvA: by maximizing the likelihood of all observed triples in KG withℓ2
regularization [18]. Logistic loss is used to maximize the soft truth value of positive formulas (5 +).
To improve the generalization and scalability, FSL [25] further extends the method proposed by
Rocktäschel [94] using a lifted rule injection method that does not rely on ground rules, but rather
regulariserelationrepresentationsdirectly.Differentfromtheabovemethodswhichdefinelossover
the ground rules (or lifted rules), RUGE [40] directly defines a loss function over triples. It employs
the score function in ComplEx [109], f (Re(
⟨
e8, r:, e9
⟩
)), to model triples. Triples are divided into
two categories, including observed triples (i.e.,E$ ) and hidden triples (i.e.,E ). Observed triples
have labels~A: (48,49 ) = 1 whereas sampled negative triples have labels~A: (48,49 ) = 0. The soft label
of hidden triplesBA: (48,49 ) ∈[0, 1]have to be predicted following t-norm fuzzy logic. With~A: (48,49 )
andBA: (48,49 ), RUGE learns embedding by enforcing triples to be consistent with their labels. All the
above methods focus on modeling deterministic KG while UKGE [11] extends them so as to model
uncertainty information in KG. An uncertain KG associates each triple in KG with weight2A: (48,49 ),
which indicates the confidence score of the triple to be true. LetΓA: (48,49 )be a set of ground rules
with ground predicateA: (48, 49 )as the rule head.35 is the distance to satisfaction of ground rule
5 . We denote the hand-crafted weight of ground rule5 asF5 . The goal of UKGE is to minimize
the MSE between the ground truth weight2A: (48,49 )and the predicted soft truth value (A: (48, 49 ))
of observed triples. Meanwhile, the weighted distance to satisfaction of sampled ground rules, in
which unseen tripleA: (48, 49 )is the rule head, should also be minimized. A summary of the most
notable PSL-based regularization techniques for embedding models can be found in Table3.
Instead of relying on human experts to define domain-specific logical rules, Quan Wang et al.
[116] propose an approach that incorporates general physical rules into KGs. These physical rules,
suchasnoisyobservation,argument-typeexpectation,at-most-onerestraint,andsimpleimplication,
are used to impose constraints on facts in KGs. The inference process is formulated as an integer
linear programming problem, where the objective function is generated from embedding models,
and the constraints are derived from the general physical rules. Furthermore, Wang et al. [113]
propose a method that automates the rule learning process and combines it with KG embedding
learning to enhance KG reasoning. This method starts by automatically mining logic rules and
assigning confidence values to the extracted triples. Then, it represents all triples in the KG as
FOL, which allows both the triples and the mined rules to exist within the same semantic space.
Finally, a global loss function is minimized over the mined logic rules and the transformed FOL,
incorporating predefined operations on the FOL. This approach enables the joint optimization
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:19
Table 3. Summary of PSL-Based Regularization Techniques for Embedding Models
Method Soft Truth Value Loss Constraints
KALE
[39] 1− 1
3√3
e8 +r: −e9
1
Í
5 +
Í
5 −∈N5 +[W −(5 +)+(5 −)]+ ∥e∥2 ≤1;∥r∥2 ≤1
MF
[94] f(vA: .v48,49 )a −Í
A:(48,49 )∈v$ log(A:(48, 49))Í
A:(48,49 )∈v log(1−(A:(48, 49)))−Í
5 +log((5 +))
ℓ2-regularization
onv48,49,vA:
FSL
[25] - −Í
A:(48,49 )∈v$,A:(48′,49′)∈v logf(−v)A: [v48′,49′−v48,49 ])
−V Í
8 ∈Flogf(−[v(8)A1 −v(8)Aℎ ])18
v48,49,vA: ∈R3,+
withℓ2-regularization
RUGE
[40] f(Re(⟨e8,r:,e9
⟩))a
1
|$|
Í
A:(48,49 )∈v$ L((A:(48, 49)), ~A:(48,49 ))
+1
||
Í
A:(48,49 )∈v L((A:(48, 49)), BA:(48,49 )) e8,e9,r: ∈C3
UKGE
[11] q(r:.(e8 ◦e9))b
Í
A:(48,49 )∈v$ |(A:(48, 49))−2A:(48,49 )|2
+Í
A:(48,49 )∈v
Í
5 ∈ΓA:(48,49)|F5 35 |2 e8,e9,r: ∈R3
af is a sigmoid function.
bq is a logistic function.
of rule learning and reasoning in KGs, facilitating the discovery of complex patterns and logical
dependencies.
Summary: While PSL-based regularization techniques for embedding models offer an efficient
and effective means of integrating embedding and logical rules, they do encounter a drawback in
terms of information loss from the logical rule aspect. This issue arises because these approaches
typically sample only a small subset of ground rules to approximate the inference process. Even
with recent advancements such as DiffLogic [103], which introduces a tailored filter to dynamically
select important ground formulas based on weighted rules and extract connected triples, complete
avoidance of information loss remains challenging. Furthermore, most methods falling into this
category tend to perform a one-time injection of logical rules to enhance embedding, overlooking
the interactive relationship between embedding learning and logical inference [39, 94].
5 Complex Query Answering
We have provided an overview of the current state-of-the-art techniques in KGE methods. However,
a major limitation of KGE methods is their ability to address onlyone-hop queries. Furthermore, due
to their black-box nature, KGE models often lack interpretability, as they lack explicit reasoning
evidence. Understanding the reasoning behind the results produced by embedding models is
consistently challenging. In response to the need for interpretability in KG reasoning, there has
been a growing interest in multi-hop reasoning methods. These methods aim to extend beyond
one-hop relationships by considering the surrounding multi-hop neighbors of the head entity
and predicting answers based on these expanded connections. We categorize multi-hop reasoning
methods into two groups: path-based query-answering methods andFirst-Order-logic (FOL)
query-answering methods, based on the types of queries they handle.
5.1 Path-Based Queries Answering
Path-based query answering methods in KG reasoning aim to identify paths that can be used to
predict new relationships between entities. These methods are crucial for conducting multi-hop
reasoning in KGs. For instance, consider the complex relationship paths illustrated in Figure6:
Satya Nadella
BornIn
−−−−−→India
OfficialLang
−−−−→ Hindi
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:20 K. Cheng et al.
Bill Gates
Seattle U.S.Microsoft
Satya Nadella
EnglishMelinda French
Founded
?LocatedIn
CEO
Spouse
LiveIn
Hindi
?LiveIn
BornIn
SpeakLang
LocatedIn
India
?OfficialLang
?SpeakLang
Fig. 6. Example of a KG. The dashed lines are the missing links, which can be inferred from multi-hop paths
in KG.
In this example, the path indicates the relationship “SpeakLanguage” between the entities “Satya
Nadella” and “Hindi”.
Existing multi-hop query answering methods can be broadly classified into two categories based
on the techniques employed to explore paths within the KG. The first category encompassespath
ranking-based query answering methods, which focus on ranking and selecting the most relevant
paths for reasoning. These methods assign scores or rankings to paths based on various criteria,
enabling the identification of paths that are likely to yield accurate predictions. The second category
comprises reinforcement learning (RL)-based methods. These methods leverage RL techniques
to guide the exploration and selection of paths for multi-hop reasoning in KGs. By employing RL
algorithms, these methods can learn to navigate the graph effectively and discover meaningful
paths that facilitate accurate relationship predictions.
5.1.1 Path Ranking-Based Query Answering. In order to leverage path information within the
graph structure, random walk inference has been widely employed. ThePath Ranking Algorithm
(PRA) [57] is a notable method that employs path instances as features within a binary classifier to
predict missing links in KGs. Considering a relation path? = [A1, . . . , A =]and a source node48 , the
PRA defines a probability distributionℎ48,? to predict target entities49 . For non-empty paths, the
probability of transitioning from one node to another via a path is modeled using:
ℎ48,? (49 )=
Õ
4′∈range(?′)
ℎ48,?′(4′).A; (4′, 49 )
|A; (4′, ·)|, (10)
where A= (4′, 49 )checks the existence of an edge between nodes4′and 49 , and the termA; (4′,49 )
|A; (4′,·)|
represents the probability of reaching49 from4′, through a one-step random walk. PRA utilizes
these probabilities to construct a feature set for a linear regression model, estimating path weights
to score potential links:
Õ
?8 ∈P(48,49 )
\8ℎ48,?8 (49 ). (11)
Here, P(48, 49 )denotes all relation paths of a maximum length; between 48 and49 . The model is
trained on a dataset where each entity pair is represented by path features, and a logistic regression
framework is applied to predict the existence of a link, optimizing a regularized objective function
to fit the observed data.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:21
Due to its reliance on the paths connecting two entities48 and49 , the PRA is unable to predict
relations between disconnected entities. In order to address this limitation, Gardner et al. [33, 34]
incorporated external textual information and introduced vector space similarity heuristics within
the random walk process to enhance the connectivity of the KG used as input for PRA. Another
drawback of PRA is its dependency on millions of distinct paths to predict target relations, resulting
in significantly slower inference, especially for modern KGs that contain a large number of triples.
To overcome these limitations, Neelakantan et al. [75] proposed Path-RNN, which utilizes vector
embeddings to expedite inference on large-scale KGs. Path-RNN employs a RNN to reason about
conjunctions of relations in a path. Specifically, for a given relation path?8 = (A1, . . . , A ; ), at each
step, the model takes the embedding of the next relation and the vector representing the path-so-far
as inputs to produce the representation of the extended path-so-far. The path representation is
determined by the final hidden state of the RNN after processing the entire path. Ideally, this path
representation should be close to the target relation in the embedding space. For instance, given a
relation pathMelinda Gates
Spouse
−−−−−→Bill Gates
Found
−−−−→Microsoft
LocatedIn
−−−−−−−→Seattle, Path-RNN aims
to generate a vector that is similar to the target relationMelinda Gates
LivesIn
−−−−−→Seattle. Path-RNN
is capable of handling inference over millions of paths in KGs due to its ability to perform non-
atomic reasoning over conjunctions of relations. However, it requires training separate models for
each target relation, which is impractical, particularly for KGs with a large number of relations.
To address the limitations of Path-RNN, Chains of Reasoning [21] were introduced. Chains of
Reasoning overcome these limitations by sharing the strength of a single RNN across all target
relations, essentially implementing a multi-task learning approach for predicting target relations
with an underlying shared parameter architecture. Another recent approach, A*Net [139], addresses
the scalability issue of path-based methods by drawing inspiration from the A* algorithm. The
central concept of A*Net is to search for crucial paths instead of utilizing all potential paths for
reasoning, thereby decreasing time and memory requirements during both training and inference.
5.1.2 RL Based Methods. Theaforementionedmethodsrelyonheuristicpathtraversaltoaddress
queriesinKGs.However,itisimportanttonotethatreal-worldKGstypicallyinvolvealargenumber
of relations. Even when considering the constraint that paths are limited to three steps, the number
of possible paths can easily reach millions. This renders it impractical to enumerate all potential
relation paths.
Inspired by the remarkable performance of RL in automated control tasks, researchers have
explored the application of RL techniques for KG reasoning. The RL-based formulation offers
several advantageous properties. Firstly, it inherently allows for paths of varying lengths, enabling
the handling of more challenging questions that require intricate chains of reasoning. Secondly,
RL-based approaches are computationally efficient, as they avoid the exhaustive enumeration of all
possible relation paths in the KG by conducting searches within a small neighborhood surrounding
the query entity.
DeepPath [124] makes the first attempt to formulate the path-finding process as sequential
decision-making and proposes an RL-based method for learning multi-hop relational paths in KG.
Given entity pairs(48, 49 ), DeepPath employs a policy network to select the most promising relation
to extend from the source entity48 until reaching the target entity49 . Let’s explore the components
of DeepPath:
— Actions. The action space encompasses all relations' within the KG.
— States. After taking an action, the agent transitions from one entity to another. The states
describe the agent’s current position within the KG. To define the agent’s position, translation-
based embeddings such as TransE and TransH are utilized to map the entities and relations
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:22 K. Cheng et al.
in the KG to a low-dimensional embedding space. At step:, the state vector is defined as
follows:
s: = (e:, e9 −e: ) (12)
where e: represents the embeddings of the current entity node, ande9 represents the embed-
dings of the target entity.
— Rewards. After the agent takes actions (moving from one entity to another), it receives rewards
based on the quality of the paths it selects. As the objective of the RL framework is to reach
the target entity, a reward of+1 is given when the agent successfully reaches the target entity:
AGLOBAL =
{
+1 if the agent reaches target entity49
−1 otherwise (13)
— Policy Network. The policy function, denoted asc (s; \), maps the states to a probability
distribution over all possible actions. An MLP is employed to parameterize the policy function,
with the Rectified Linear Unit activation function used as its nonlinearity layer.
While DeepPath includes the target entity in its state to inform decision-making, it is not suitable
for predicting unknown target entities in queries. To overcome this limitation, MINERVA [20]
is proposed, which learns how to navigate the graph conditioned on the input query for a more
challenging query-answering task where the target entity needs to be inferred. MINERVA leverages
an LSTM to encode historical inference paths, which assists with the current decision-making
process. The state representation in MINERVA is obtained by concatenating the query and the
historical search path. The aforementioned methods, including DeepPath and MINERVA, employ
policy gradients for learning. However, these methods often require a large number of rollouts
to obtain a trajectory with positive rewards, particularly during the early stages of learning. To
address the issue of sparse rewards, MWalk [102] combines Monte Carlo Tree Search with RNNs,
enabling easier generation of trajectories with positive rewards. Additionally, MWalk introduces
parameter sharing between the Q-value network and the policy network of the RNN, allowing for
Q-learning over off-policy trajectories to enhance the policy network. Another approach to tackle
the sparse reward problem is presented by MultiHop [60]. It employs reward shaping and action
dropout techniques to facilitate more efficient model training. CURL [133] introduces a dual-agent
framework and divides the KG into multiple clusters using K-means. CURL makes decisions both
between and within clusters. A summary of the most notable RL-based methods for path-based
query answering can be found in Table4.
Summary: RL-based methods provide a dynamic, adaptive approach to KG reasoning. They are
particularly adept at navigating the complex network structures of KGs and have demonstrated
notable potential in identifying paths and relationships over multiple hops. RL-based methods are
also inherently capable of improving over time due to the learning nature of RL, which allows these
models to adapt to new data and optimize their strategies based on the feedback received. Despite
these benefits, RL-based methods also face some noteworthy challenges that may hinder their
application in multi-hop KG reasoning. One of the primary concerns is their struggle with large
actionspaces,acommoncharacteristicofKGs.Thiscomplexityoftenleadstoahighercomputational
burden and makes the exploration-exploitation trade-off more challenging to manage effectively.
Moreover, RL-based methods often fail to adequately consider the correlation between different
entities in the KG. This oversight can result in less accurate reasoning and less effective knowledge
discovery.AsentitieswithinaKGaretypicallyinterconnectedinacomplexnetworkofrelationships,
disregarding such correlations can lead to a less nuanced understanding of the KG’s structure.
Furthermore, the existing RL-based methods lack an effective action-filtering mechanism. This
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:23
Table 4. Summary of RL-Based Methods for Path-Based Query Answering
Method Actions States Rewards Policy Network
DeepPath [124] ' (e:,e9 −e:)
AGLOBAL=
{+1 if the agent reaches49
−1 otherwise
AEFFICIENCY= 1length(?)
ADIVERSITY=−1||
Í||
8=1cos(p,p8)
Fully-connected
neural network
MINERVA [20] (4:, ', 4′|4′∈) (e:,e8,rtarget,e9) I{eC =e9} LSTM
MWalk [102] (4:, A′, 4′|(4:, A′, 4′)∈G) s:−1 ∪{0:−1, 4:,E4:,N4:} I{eC =e9} RNN
MultiHop [60] (4:, A′, 4′|(4:, A′, 4′)∈G) (e:,e8,rtarget) I{eC =e9} LSTM
4: denotes the visited entity at step:;48 denotes the source entity;49 denotes the target entity;E4: denotes the set of all
edges connected to4: ; N4: denotes the set of all entities connected to4: ; 0: denotes the action selected by the agent at
step:.
limitation can lead to inefficient exploration and potentially suboptimal reasoning paths. Without
a mechanism to effectively filter out irrelevant or less promising actions, the RL models may waste
computational resources on unproductive paths, thereby inhibiting their overall performance.
5.2 FOL Query Answering
Path-based query-answering methods aim to find query answers by traversing a path composed of
multiple intermediate relations and entities, starting from the head entity. These methods typically
extend only one neighbor at each step, which limits their ability to handle complex logical queries
thatinvolvelogicaloperationsresultinginmultipleentitiesateachhop.Toovercomethislimitation,
FOL query-answering methods have been proposed. FOL query answering is designed to address
logical queries in a general form. Given any FOL query, the objective of FOL query answering is to
find answers for the free variables that satisfy the truth of the formula.
First Order Logic Query and Its Representation in the Context of Knowledge Graphs. A query
formulated in FOL encompasses multiple non-variable anchor entity sets{E8 }:
8=0 where E8 ⊂
is a subset of. These sets correspond to quantified bound variablesE8 . Alongside these sets, the
query also contains a solitary target variable, denoted byE?, which is tasked with providing the
answer to the query, represented asE? .
The ultimate objective of such a logical query is to identify the entity setE? ⊂, which corre-
sponds to the target variable and is a subset of. This aim can be formally encapsulated through
the mathematical definition provided below:
@ [E?]E?.∃E1, . . . , E : : @1 ∨···∨ @=. (14)
In the above equation, each@8 is the conjunction of multiple sub-conditions(@81 ∧···∧ @8<). Each
sub-condition@8< can assume one of the forms from a set of possibilities, defined by combinations
of positive and negated relational predicates with variablesE?, E1, . . . , E : .
It’s pertinent to highlight that logical queries in the realm of KGs can be graphically represented,
leading to what we term a “dependency graph.” This graph, denoted as& = {@, '@, !@ }, is a visual
manifestation of the logical query where@ represents the entity sets{E8 }:
8=0 ∨E? . Here,{E8 }:
8=0
denotes the anchor node set andE? signifies the variable node set. Meanwhile,'@ and !@ represent
the relation set and logical operations, respectively.
Adhering to the principles of FOL, the dependency graph& is aDirected Acyclic Graph (DAG),
with anchor entities serving as the source nodes. A concrete example of such a logical query graph
can be found in Figure7. This visual representation not only helps in understanding the structure of
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:24 K. Cheng et al.
Turing
Award
Deep
Learning
University
Win-1
Field-1
Intersection
Intersection
q = V? .  V: Win-1 (Turing Award, V) Field -1(Deep Learning, V)
University(V, V?)
Fig. 7. The graph expression of the query “Which University did the Turing Award winner work on deep
learning work at?”.
the query but also provides a path to traverse the KG, thereby aiding in the retrieval of the desired
information.
5.2.1 Subgraph-Matching Based Methods. Traditional approaches to answering FOL queries
typically involve transforming the query into a dependency graph, as discussed in Section5.2.
This transformation allows for a structured representation of the query. For instance, consider the
question “Which University did the Turing Award winner work on deep learning work at?” This
question can be transformed into a DAG graph, as illustrated in Figure7.
To retrieve the answers, the transformed FOL query is converted into a corresponding SPARQL
query graph, which is then issued to the KGs. SPARQL1 is the standard query language and protocol
for Linked Open Data and RDF (Resource Description Framework) databases. It models the data as
a directed graph, consisting of triples in the form of(head entity, relation, tail entity).
The function of SPARQL in the realm of graph databases can be likened to that of SQL in the
context of relational databases. Much like how SQL facilitates the retrieval and modification of data
within relational databases, SPARQL provides similar capabilities for NoSQL graph databases.
In SPARQL, a query is composed of a set of triple patterns, each component of which can
potentially be a variable. The task then becomes finding solutions to these variables by identifying
matches between the patterns present in the query and the triples within the dataset. This pattern-
matching process enables the extraction of relevant information from the KGs. The SPARQL
engine sifts through the intricate web of entities and relationships, isolating triples that satisfy the
conditions outlined in the query. This matching operation can be viewed as a sophisticated search,
ultimately leading to the extraction of specific, contextually relevant information from the vast,
interconnected structure of the KGs.
5.2.2 Representation Learning Based Logical Queries Answering. KGsarecommonlycharacterized
by noise and significant incompleteness, which pose challenges for subgraph-matching-based
methods when attempting to respond to queries, particularly those involving numerous free
variables. The presence of incorrect or missing facts can greatly impede the retrieval of relevant
information,oftenresultinginemptyresponsesorincorrectanswers.Moreover,subgraph-matching-
based methods face inherent computational complexity issues, making them less scalable for
large KGs.
In light of these difficulties, there has been a growing interest in leveraging representation
learning techniques to improve FOL query answering. Embedding-based methods have garnered
attention due to their ability to effectively capture the underlying structure of KGs and their
1https://www.w3.org/TR/rdf-sparql-query/
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:25
computational efficiency. By employing these techniques, it becomes possible to enhance the ACC
and efficiency of FOL query-answering tasks.
Overview. A logical query answering process typically follows a specific structure when using a
representation learning-based approach. This structure can be itemized into three critical stages: (1)
transformation of a FOL query into an equivalent expression composed of basic logical operations,
(2)retrievaloftheanswersetcorrespondingtothequerybyexecutingthetransformedexpressionin
a sequential manner, and (3) determination of a fitting loss function, usually based on the likelihood
that the ground truth answer is included in the retrieved answer set.
The process relies on three primary operations that enable logical query answering:
— Relation Projection (P(q, A: )): This operation computes the answer set of tail entities that can
be accessed from the query embeddingsq via the specific relationA: . This process is crucial to
link and navigate through the entities within the KG.
— Logical Operations:
–Conjunction (∧): Denoted by (x, y), this operation performs the logical conjunction,
equivalent to a set intersection, on each element in the query embeddingsx and y. The
conjunction operation helps narrow down the possible outcomes, thereby refining the
results.
–Disjunction (∨): This operation, represented as (x, y), executes the logical disjunction,
also known as a set union, on each element in the query embeddingsx and y. It expands
the possible outcomes by combining different sets, providing a broader solution space.
–Negation (¬): Defined as# (x), this operation applies the logical negation to each element
in the query embeddingsx, thus allowing to exclude certain entities from the results based
on specific conditions.
— Membership Validation (score(q, x)): This operation calculates the probability that node
embeddings x are part of the retrieved queryq. This validation step ensures that the retrieved
answer set includes the most probable and appropriate solutions.
By executing these operations in an orderly manner, the query answering system can effectively
navigate through the structure of the KG, apply the right logical operations, and ultimately generate
an accurate and relevant answer set to the initial query.
RepresentativeMethods.Graph Query Embedding (GQE) [43]makesthefirstattempttoperform
logical operations within a low-dimensional embedding space. GQE works by transforming a query
into a single vector,q ∈R3 , using two differentiable operations, namely projectionP(q, A: )and
intersection (x, y).
The GQE model treats projection operation as a translation process. Given an edge typeA:
and a query embeddingq, the projection operatorP(q, A: )generates a new query embedding
q′= P(q, A: ), signifying the set of nodes linked toq via edges of typeA: . The projection operation
is computed as follows:
P(q, A: )= r: q. (15)
For a group of query embeddingsq1, . . . , q= sharing the same entity typeW, the intersection
operation carries out deep-set intersection in the embedding space as shown below:
I(q1, . . . , q=)= WWΨ(NN: (q8 ), ∀8 = 1, . . . , = ). (16)
In the equation above,NN: denotes ak-layer neural network,Ψ stands for a symmetric vector
function(e.g.,anelementwisemeanorminofasetovervectors),and WW representsatransformation
matrix for entity typeW.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:26 K. Cheng et al.
To infer queries corresponding to DAG-structured conjunctive query on Knowledge Graphs,
GQE starts by projecting the anchor node embeddings as per their outgoing edges. If the query
includes multiple incoming edges, an intersection operation is employed to aggregate the incoming
information. This process is repeated until the target variable of the query is reached. The likelihood
of an entityG being the answer to the query can be calculated by the distance between the query
embedding and the entity embedding:
score(q, x)= q.x
∥q∥∥x∥, (17)
where q denotes the query embedding andx denote the embedding of entityG.
Despite the success of GQE, it has some limitations. First, GQE primarily supports conjunctive
queries, but it falls short when it comes to more complex queries that involve a combination of
logical operators, such as disjunction (∨), negations (¬), or existential qualifiers(∃). Second, GQE
lacks a mechanism to account for uncertainty in query answers. Real-world data is often noisy and
incomplete, which means that the ability to quantify uncertainty is crucial for practical applications.
Finally, GQE learns to answer queries based on the structures it has seen during training. It might
not generalize well to new logical query structures that it has not encountered during training. To
address the limitations of GQE, Query2Box [89] proposed to employ box embeddings for more
general existential positive first-order logical queries (i.e., queries that include any set of∨,∧, and
∃) in KGs. In particular, Query2Box models a query answer set as a box and an entity as a point. In
this way, it is natural to model the entity embedding to be a point inside the box and conjunction
as the intersection of boxes. Query2Box shows great generalizability, which can be generalized to
new logical query structures that it has never seen during training. To improve the expressiveness
of the model, NewLook [63] extends Query2Box to support four types of logical operations (i.e.,
conjunction, disjunction, negation, difference). It can also answer complex queries that may contain
more than one variable, broadening the applicability of Query2Box. However, NewLook might have
its limitations when it comes to scalability as complex queries involving multiple logical operations
could be computationally expensive.
In addition, boxes, as poorly differentiable geometric shapes, can not handle uncertainty cal-
culations well. Also, Query2Box cannot represent the logical operation - negation (¬) because
the complement of a closed box is not closed. To further support negation operation and model
uncertainty, BetaE [90] models both the entities and queries as Beta distributions defined on the
[0, 1]interval. In this case, conjunction is modeled as a weighted interpolation of Beta distributions
and negation as an inversion of density. Such probabilistic modeling can effectively capture the un-
certainty of the queries. Beta embedding is the first method that supports full FOL queries. Despite
this improvement, it has its downside due to the expensive computation of Beta distribution.
In recent years, more advanced methodologies have emerged, addressing the shortcomings
of previous techniques and expanding the capabilities in logical query answering. For example,
CQD [1] incorporates advanced neural architectures to improve query-answering capabilities.
The use of deep learning techniques in CQD can help uncover intricate patterns within the data,
enhancing the quality of answers. Despite its advantages, one of the potential downsides to this
approach is the need for substantial computational resources and the risk of overfitting complex
models, especially when working with smaller datasets. FuzzQE [12] takes an innovative approach
by integrating t-norm fuzzy logic with embedding methods. This introduces a degree of flexi-
bility, as fuzzy logic allows for handling uncertainty. The main drawback of FuzzQE might be
the interpretation of the results, as fuzzy logic’s output is not always intuitive to comprehend,
particularly in complex scenarios. GNN-QE [138] is a technique that leverages the strengths of
GNNs, well-known for their prowess in capturing complex graph structures and dependencies.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:27
Table 5. Summary of Relation Projection and Membership Score of Representation Learning
Based Logical Queries Answering Models
Method Relation Projection Membership Score
GQE
[43] r: q q.x
∥q∥∥x∥
Query2Box
[89] q +rk
distoutside(x; q)
+Udistinside(x; q)
BetaE
[90] MLPA: (q) KL(?G,: ; ?@,:)
NewLook
[63]
Cen(q)= MLP((MLP(Cen(q))||MLP(Off(q))||xD? )
Off(q))= MLP((MLP(Cen(q))||MLP(Off(q))||xD? )
distoutside(x; q)
+Udistinside(x; q)
FuzzQE
[12] 6(NN(WA: q +bA )) q) x
GNN-QE
[138] f (5 (NBFNet(x))) q) x
Table 6. Summary of Logical Operations of Representation Learning Based Logical Query
Answering Models
Method Conjunction Disjunction Negation
GQE
[43] WWΨ(NN:(x),NN:(y)) - -
Query2Box
[89]
Cen(q)=0G ⊙Cen(x)+0~ ⊙Cen(y)
Off(q)=Min(Off(x),Off(y))⊙f(DeepSets(x,y)) Min({score(x,e),score(y,e)}) -
BetaE
[90]
1/xFG.yF~ De Morgan’s
Law (1UG:
, 1VG:
)
NewLook
[63]
Cen(q)=0G ⊙Cen(x)+0~ ⊙Cen(y)
Off(q)=MLP(Mean(MLP(Cen(x)||Off(x)),MLP(Cen(y)||Off(y)))) Min({score(q,e),score(y,e)}) -
FuzzQE
[12] x◦y x+y−x◦y 1−x
GNN-QE
[138] x◦y x+y−x◦y 1−x
This approach allows for more potent representation learning and consequently enhanced query
answering. However, the performance of GNN-QE heavily relies on the quality and structure of
the graph data. In cases where the graph is sparse or irregular, the performance of GNN-QE could
be compromised. We have summarized all the primary operations for the methods discussed above,
including relation projection, membership score, and logical operations, in Table5 and Table6.
Training Objective. The loss functions of logical query embedding methods are calculated by
measuring the distance (e.g., Euclidean or cosine similarity) between the embeddings of the query
and the correct fact, and between the query and incorrect facts. The objective is to minimize the
distance between the query and the correct fact while maximizing the distance with the incorrect
ones. Examples of this approach include cross-entropy loss and ranking-based loss.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:28 K. Cheng et al.
— Max-margin Loss: The most frequently used loss function is margin-based pairwise ranking
loss:
L= max(0, 1 −score(q, x)+score(q, x′)), (18)
where x denote the positive answers andx′denote the negative answers. The first proposed
logical query embedding method GQE employ this loss to train the model.
— Binary Cross Entropy Loss: The simplest loss function is binary cross-entropy loss, which aims
to distinguish positive triples from negative triples:
L= − 1&

Õ
0∈&
log ? (0|&)− 1V−&

Õ
0′∈V−&
log(1 −? (0′|&), (19)
where& is the set of answers to the complex query& and ? (0|&)is the probability of entity
a in the final output fuzzy set. The methods GNN-QE employ this loss to train the model.
— Cross Entropy Loss with a Margin Term: An extension to cross-entropy loss is to add a margin
term to adjust the probability:
L= −log f (W −distbox(x; q))−
:Õ
8=1
1
: log f (distbox(x′; q)−W), (20)
whereW denote the margin andx′denote the negative answers. The methods Query2Box and
NewLook employ this loss to train the model.
The main difference between the loss functions used in logical query embeddings and KG
embeddings lies in the complexity and the focus of the learning objective: logical query embeddings
need to accommodate more complex logical structures and often multiple entities and relations
within a single query, making their loss functions inherently more complex and tailored to handle
logical deductions, while the focus of KG embeddings is more on capturing the direct relationships
betweenentitiesandrelationsinasimplerandoftenmorestraightforwardmanner.Bothapproaches
aim to optimize the embeddings so that the geometric (or other forms of) relationships in the
embedded space reflect the factual and logical structure of the underlying KG accurately.
6 Rule Learning
Despite the promising reasoning ability of logical inference in completing KG, they require the set
of logical rules to be specified by hand, which are usuallylabor-intensive. To reduce the demand on
human efforts,automatically learning Horn rules from KGs has been investigated by a large body
of works. Logical rule learning aims to learn weighted Horn rules of the following form:
U : Aℎ (G, ~)← A11 (G, I1)∧···∧ A1= (I=−1, ~), (21)
whereU ∈[0, 1]is the confidence associated with this rule, indicating how likely the rule holds
true.
6.1 Symbolic Methods
Existing symbolic reasoning methods are mainly search-based ILP methods, which usually learn
rules via searching and pruning rules among the rule space.
6.1.1 ILP. ILP is a set of techniques that aim to deduce Horn rules from ground facts. ILP
operates by utilizing both positive and negative examples, with the goal of learning Horn rules
that accurately entail the positive examples while excluding the negative ones. When learning
Horn rules corresponding to a specific rule head, a commonly employed strategy is the use of a
greedy algorithm. This algorithm selects predicates to construct the rule body in a step-by-step
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:29
manner, guided by a predefined heuristic measure. Some notable ILP methods include FOIL [88]
and GOLEM [73], MDIE [72], and Inspire [99].
However,applyingILPapproachestoKGspresentsuniquechallenges.KGstypicallylacknegative
statements as counter-examples, which are essential for ILP’s learning process. As a result, the
absence of negative facts in most KGs poses a significant obstacle when utilizing ILP techniques.
Additionally, ILP’s reliance on the greedy algorithm introduces its own set of challenges. While the
greedy algorithm can make locally optimal choices during the construction of rule bodies, these
choices may not always lead to globally desirable outcomes. Therefore, despite the potential of ILP
approaches, their application to KGs requires addressing these challenges and developing strategies
to handle the absence of negative facts and mitigate the limitations of the greedy algorithm.
6.1.2 Association Rule Learning-Based Approaches. Drawing inspiration from association rule
mining [24] in the domain of data mining, association rule learning-based approaches apply
predefined metrics, such asconfidence and support, to gauge the plausibility of Horn rules in KGs.
Confidence, in the context of KGs, refers to the ratio at which a body path can be successfully
closed by the target relation. For instance, considering a logical rule defined in Equation (21), its
confidence can be computed as follows:
|{(G, I1, . . . , I =−1, ~): Aℎ (G, ~)← A11 (G, I1)∧···∧ A1= (I=−1, ~)}|
|{(G, I1, . . . , I =−1, ~): A11 (G, I1)∧···∧ A1= (I=−1, ~)}| , (22)
where the numerator in Equation (21) is the number of its rule instances (i.e., closed paths) and
the denominator is the number of its body instances (i.e., relation paths). However, calculating
these metrics involves discrete counting of instances, which introduces significant computational
complexity. This complexity arises from two main aspects. First, to evaluate the plausibility of a
candidate rule, all instances following the template of the rule need to be identified throughout the
entire KG. This requires searching the KG extensively to determine the existence of rule instances,
contributing to the computational burden. Second, association rule learning-based approaches need
to consider all possible rules within the rule space. As the length of the rule space increases, the
computational complexity escalates, demanding substantial computational resources.
To address the high computational complexity, works like AMIE [30, 31] efficiently prune the
search space while learning logical rules. AMIE’s process involves two main steps:rule extending
and rule pruning. In rule extending, AMIE generates candidate rules through iterative extensions
using three mining operators:
— Add dangling atom: Adds an atom with one new variable and one shared variable.
— Add instantiated atom: Instantiates one variable with an entity while sharing other variables.
— Add closing atom: Both variables of the atom are shared with existing rule components.
In rule pruning, AMIE utilizes metrics such as head coverage and standard confidence to prune
rules:
— Head Coverage: Measures the proportion of true instance pairs covered by the rule predictions:
hc( →Aℎ (G, ~)):= supp( →Aℎ (G, ~))
#(G′, ~′): Aℎ (G′, ~′). (23)
— Standard Confidence: The ratio of correct predictions in the KG:
conf( →Aℎ (G, ~)):= supp( →Aℎ (G, ~))
#(G, ~): ∃I1, . . . , I < :  . (24)
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:30 K. Cheng et al.
Table 7. Capabilities of Different Methods to Combine Logical Rule Learning with Neural Networks
Categories Differentiable Scalable Interpretable Exploring Intrinsic
Similarities Among Triples
Differentiable ILP ✓ Bad ✓ ✓
Matrix-based Reasoning ✓ Medium ✓
Learning Based Methods ✓ Good ✓ ✓
SPARQL2 is used to ground the rules from the extending phase and meet the thresholds set
by the pruning metrics. Rules that do not surpass a defined confidence threshold are pruned to
reduce the rule set and ensure only the most plausible rules are retained. This approach leverages
monotonicity in confidence and head coverage to prune less plausible rules efficiently. WARMR [23]
mines rules over a limited set of conjunctive queries and use declarative language bias to reduce the
search space. RLvLR [80] proposed new pruning criteria based on the technique of KG embedding
together with a new sampling method. Despite all the attempts made to reduce potentially large
searching space of logical rules, efficiency is still a central challenge since even evaluating one
candidate rule is super expensive (i.e., require to enumerate all ground rules in whole KG which
follows the rules.). More recently, several attempts, such as AnyBURL [68] and RARL [82], have
been made to sample rule instances instead to accelerate rule learning.
Since logical rule learning requires learning the structure (i.e., a set of logical rules), traditional
approaches tackle this problem as a discrete optimization task, requiring a search through a
potentially vast rule space. Consequently, these methods often encounter significant scalability
challenges. Furthermore, approaches in this category heavily rely on observed rule instances to
define the score function for rule evaluation, limiting their ability to generalize (i.e., they cannot
detect rules without explicit rule instances). Additionally, traditional approaches lack the capability
toeffectivelyhandlenoisydata,whichisprevalentinreal-worldKGsthatinevitablycontainvarious
types of errors.
6.2 Neural-Symbolic Integration
Recently,therapidgrowthofKGsbringsrichresourcestolearnlogicalrules.Givenneuralnetworks’
proficiency in learning from vast datasets, there has been growing interest in integrating logical
rule learning with neural networks to handle large-scale KGs. Existing works combining logical
rule learning with neural networks can be roughly divided into three classes: (1) Differentiable ILP,
(2) Matrix-based Reasoning, and (3) Learning-based approaches, whose capabilities are summarized
in Table7.
6.2.1 Differentiable ILP. Neural Theorem Provers (NTPs) [93] aims to provide continuous relax-
ations of thebackward chainingalgorithm by replacing discrete symbols with their continuous
embedding representations. Following the principle of ILP, these representations are learned end-to-
end by maximizing the proof scores of facts in the KG, while minimizing the score of facts not in the
KG. Given a query(48, A:, 49 ), backward chaining first attempts to unify it with the facts available in
a given KG. If no matching fact is available, it considers all possible rules in rule space to unify the
rule head with the query(48, A:, 49 )resulting in a substitution for the variables contained in rule
head. Then, the backward chaining algorithm applies the substitution to rule body corresponding
to the rule head and recursively attempts to prove the atoms contained. An example of backward
2https://www.w3.org/TR/rdf-sparql-query/
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:31
chaining algorithm is as follows. Given a KG composed by the facts Father(Anthony, Bob) and
Father(Bob, Carlos), and the rule GrandFather(x, y)←Father(x, z)∧Father(z, y). The query Grand-
Father(Anthony, Carlos) can be proven by unifying with the rule head GrandFather(x, y), with the
substitution x/Anthony, y/Carlos, and then by recursively proving the subgoals Father(Anthony, z)
and Father(z, Carlos), which hold true for the substitution z/Bob. By introducing embeddings to
represent each predicate and constant in KG, NTPs replace comparisons between symbols with
a differentiable similarity measure between their embeddings. Therefore, NTPs allow unifying
symbols like GrandPa and GrandFather even though they are lexically different. However, NTPs
need to consider all possible proof paths for answering a given query, which leads to its inefficiency
even for a small KG. For addressing the limitations of NTPs, NTP 2.0 [70] reduces the computational
complexity of inference and learning by generating only the most promising proof paths while
CTPs [71] learns an adaptive strategy for selecting subsets of rules to consider at each step of
the reasoning process. In addition, several attempts have been made to utilize forward chaining
algorithm to avoid representing the proof tree explicitly. Representative methods includemILP [28]
and method proposed in [8].
Summary: Neural theorem provers provide a differentiable ILP framework, which can jointly
learning embeddings of symbols and interpretable rules from KGs. Similar symbols can be placed in
close proximity in a vector space by neural theorem provers. These embedding vectors can enhance
logical rule learning as a single rule can be leveraged for many proofs of queries with symbols that
have a similar representation. However, neural theorem provers require all possible proof paths
in order to answer a given query, which leads to its inefficiency even for a small KG. Although
significant efforts have been made to reduce the proof paths, computational inefficient is still its
central drawback.
6.2.2 Matrix-Based Reasoning. Traditional association rule learning-based approaches treat
logical rule learning as a discrete search problem. These traditional methods struggle to integrate
seamlessly with deep gradient-based learning systems due to the inherently discrete nature of rule
learning. To bridge this gap, an approach called neural logic programming has been developed, in-
troducing the concept of continuous optimization to the discrete world of rule learning. Neural logic
programming establishes a connection between logical inference and sparse matrix multiplication,
a significant step that transforms the discrete optimization problem into a differentiable problem.
This innovative approach allows logical inference to be compiled into sequences of differentiable
tensor multiplication. A challenge that arises with this methodology, however, is the simultaneous
requirement for learning in both a continuous space (i.e., the weightU associated with the logical
rule) and a discrete structural space (i.e., the logical rule).
To render the search in the discrete structure space differentiable, TensorLog [17], as proposed by
Cohen in 2016, compiles logical inference into sequences of differentiable numerical operations on
matrices. This allows the model to handle both continuous and discrete components of the problem
in a unified framework. TensorLog defines an operatorM(:)for each relationA: . Concretely,M(:)
is a matrix in{0, 1}||×||such that its(8, 9 )entry is1 if and only if the triple(48, A:, 49 )is in the
KG. Given the fact that the scalarv)
G .M(11 ).M(12 ). . . M(1= ).v~ is equal to the number of paths
connecting concrete entityG to~ through the rule bodyA11 (G, I1)∧A12 (I1, I2)∧···∧ A1= (I=−1, ~),
where vG ∈{0, 1}|| is one-hot vector of entityG with 1 at positionG and 0 otherwise, neural
logic programming learns logical rules by finding appropriateU (Aℎ )for each head relationAℎ that
maximizes
Õ
Aℎ (G,~ )∈v$
v)
G
(Õ
;
U (Aℎ )
;
Ö
8 ∈?;
M(A18 )
)
v~, (25)
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:32 K. Cheng et al.
where; indexes over all potential rule bodies of head relationAℎ with a maximum length of=, U (Aℎ )
;
is the confidence associated with the rule body indexed by; and ?; is the ordered list of relations
in this particular rule body. To learnU (Aℎ ), Neural-LP [128] designs a neural controller system
based on an attention mechanism, which learns to sequentially compose the differentiable tensor
multiplication. However, Neural-LP could learn a higher confidence value of a meaningless rule
by mistake because it shares an atom with a useful logical rule. To address this problem, RNNs
are utilized in [96] to prune the potential incorrect rule bodies with low probability. In addition,
Neural-LP can learn only chain-like Horn rules, which limits its expressive power. To learn Horn
rules in more general form, NLIL [129] extends Neural-LP framework for general ILP problems.
Summary: Similar to association rule learning-based approaches, neural logic programming
computes the confidence score of every candidate rule in rule space to select Horn rules with
the highest confidence score. To make the framework differentiable, neural logic programming
turns the discrete counting of ground rules into sparse matrix multiplication, which enables logical
inference to be compiled into sequences of differentiable tensor multiplication. Yet, while neural
logic programming is able to harness the power of neural networks to facilitate the learning of
logical rules, it does face some notable computational inefficiencies. These primarily stem from
the involvement of large matrix multiplications, which can lead to high computational costs.
Moreover, neural logic programming does not prioritize efforts to minimize the extensive search
space associated with logical rules. These constraints mean that while neural logic programming
can be applied successfully to some real-world KGs, such as WN18 and FB15K, its efficiency is
currently insufficient to handle larger KGs, such as YAGO3-10. This shortfall indicates a need for
further refinement and optimization of the methodology, particularly if it is to be scaled up for use
in broader contexts. Another limitation is that, unlike its counterparts, such as neural theorem
provers, neural logic programming is unable to learn embeddings of symbols. This inability restricts
it from leveraging the inherent correlations that may exist among symbols. The ability to leverage
such correlations could potentially enhance the predictive power of the model, providing a potential
avenue for future improvement in the design and functionality of neural logic programming.
6.2.3 Learning Based Methods. The field of differentiable rule learning techniques, despite their
effectiveness, still faces scalability challenges. As a result, researchers have recently shifted their
focus towards more advanced neural techniques to overcome these limitations.
One such advancement is the RNNLogic framework proposed by Qu et al. [86]. This framework
introduces a novel approach that separates the process of rule generation and rule weight learning
byincorporatingarulegeneratorandareasoningpredictor,respectively.Whiletheincorporationof
the rule generator successfully reduces the search space, RNNLogic faces considerable challenges in
terms of scalability when dealing with larger KGs that encompass a substantial number of relations
(e.g., FB15K-237) or a vast multitude of entities (e.g., YAGO3-10). To address these challenges,
RLogic [16] proposes an alternative approach that directly learns logical rules at the schema level
using a representation learning-based model. By relying on a small set of sampled closed paths for
training, RLogic significantly improves efficiency. Moreover, RLogic breaks down a large sequential
model into smaller atomic models in a recursive manner, facilitating the detection of rules even
without direct support from rule instances. This recursive approach enhances the depth of deductive
reasoning in rule learning. Another notable contribution in the pursuit of learning logical rules is R5
[65], which employs a RL-based approach. Like RLogic, R5 leverages recurrent relational prediction.
However, R5 assumes that only one head can be derived from a relation pair, which limits its
ability to adequately model the underlying complexities of logical deduction. Finally, the recent
work on neural compositional learning for KG reasoning (NCRL) [chengneural] explicitly learns
a hierarchical tree that captures rule composition in an end-to-end manner. This enhancement
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:33
allows for a more comprehensive and accurate representation of rule composition. In addition,
some recent works also extend the RL-Based Methods for complex query answering as discussed in
Section 5.1.2 for rule learning. For example, SchemaWalk [64] makes the first attempts to formalize
an interesting problem—inductive meta-path learning and proposed a novel framework to learn
rules in the inductive setting.
7 Evaluation for Each Downstream Task
Following the introduction of existing neural-symbolic KG reasoning techniques, this section delves
into the application of these methods to various downstream tasks. These tasks can be categorized
into three main categories: (1) KG completion, (2) complex query answering, and (3) relational
reasoning. These categories encompass a wide range of tasks and demonstrate the versatility and
applicability of neural-symbolic KG reasoning.
7.1 KG Completion
The KG completion task focuses on predicting missing triples within a KG. This task can be further
divided into two subtasks (1) link prediction and (2) triple classification.
Link Prediction. Link prediction is a fundamental task in KGs that aims to infer the missing entity
in a given query, such as(48, A:, ?)or (?, A:, 49 ). For example, in the query(Google, LocatedIn, ?),
the objective is to predict the location where the Google company is situated. Similarly, in the
query (?, Create, Theory of relativity), the goal is to identify the person responsible for creating
the theory of relativity. The link prediction task is typically treated as an entity sorting problem,
often referred to as entity prediction or entity ranking. The task involves ranking the tail entities49
based on a given query(48, A:, ?). To predict the tail entity for the triple(48, A:, ?), we calculate a
score 5A: (48, 4′
9 )for every candidate entity4′
9 ∈ and select the one with the highest likelihood. All
KG reasoning methods can be utilized for link prediction. Although the general inference process
remains consistent, various KG reasoning methods employ distinct approaches to predict missing
links in Knowledge Graphs (KGs).
— KG embedding methodsoffer a solution for link prediction by leveraging learned embeddings
and a scoring function from a representation learning model. The scoring function assigns
scorestoallcandidatetriples,whicharesubsequentlyrankedindescendingorder.Thisranking
generates a list of candidate answers. For example, given the query(Google, LocatedIn, ?), a
ranked list like[Mountain View, New York, Phoenix, Houston]can be produced. The ranking
is determined by the scores assigned to each candidate triple, reflecting their likelihood of
being the correct answer to the query.
— Query answering methodsaim to predict links by leveraging the projection operation over the
headentities.Forexample,whenprovidedwiththequery (Google, LocatedIn, ?),thetailentities
can be inferred through the projection operationq = P(>>6;4, !>20C43= ). Subsequently,
the membership validation functionscore(q, e′
j )is used to compute the scores of all candidate
tail entities. By ranking the candidate tail entities in descending order based on their scores, a
list of answers can be generated. This approach facilitates the identification and ranking of
potential entities that align with the given query, thereby enhancing the link prediction task.
— Although rule learning methodsare primarily designed to generate logical rules rather than
predict missing links, these learned rules can still be indirectly utilized to derive missing facts
from KGs. Various existing methods, such as Neural-LP [128], DRUM [96], and NLIL [129],
evaluate the quality of learned rules in terms of the link prediction task. The forward chaining
algorithm [97] is widely employed to derive missing facts from logical rules. Given a query
(48, A:, ?), let represent the set of candidate answers that can be inferred using any learned
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:34 K. Cheng et al.
rule through forward chaining. For each candidate answer4′
9 ∈, the score of the triple
(48, A:, 4′
9 )can be calculated as the sum over the path instances connecting the entity48 and4′
9
in the rule space, denoted as?, multiplied by the corresponding rule scoreB (X):
Õ
X ∈rule space
Õ
? ∈% (48,?,4′
9 )
B (X). (26)
Here, % (48, ?, 4 ′
9 )represents the path instances following the ruleX. To illustrate the link
prediction process, consider the KG in Figure4 and the query(Diana, hasGrandma, ?). The
only applicable rule for inferring the target relationhasGrandma is given as follows:
0.75 :hasMother(G, ~)∧hasMother(~, I)→ hasGrandma(G, I ). (27)
By grounding the rules with all observed triples in the KG, the rule instance
hasMother(Dana, Eva)∧hasMother(Eva, Faye)→ hasGrandma(Dana, Faye),
is the only one where the premise is satisfied. The score of its conclusion (e.g.,hasGrandma
(Dana, Faye)) becomes0.75, while all other candidate entities receive a score of0. In this
way, the link(Dana, hasGrandma, Faye)can be successfully predicted. It is worth noting that
most rule learning methods focus on learning chain-like horn rules, and the conjunctive body
of a ground chain-like Horn rule essentially represents a path in a KG. As a result, efficient
extraction of these paths can be achieved using sparse matrix multiplication techniques.
During the evaluation, the filtered setting [7] is commonly employed. This setting focuses solely
onthetargettriple (48, A:, 49 )anddisregardsallothertruetriples (48, A:, 4′
9 )intheresult.Forinstance,
consider the query(Google, LocatedIn, ?), with ranked tail entities [Mountain View, New York,
Phoenix, Houston]. BothMountain Viewand New Yorkare correct answers. However, since our
target triple is(Google, LocatedIn, New York), we filter outMountain Viewand update the list as
[New York, Phoenix, Houston].
To evaluate link prediction performance, three commonly used ranking metrics are employed:
Hit@k, Mean Reciprocal Rank (MRR) , andMean Rank (MR). These metrics assess the ranking
of the predicted entities to evaluate the effectiveness of ranking algorithms in information retrieval
systems.
— Hit@k: Hit@k is a metric used to evaluate the ACC of a ranking algorithm in retrieving
relevant items within the top k positions of a ranked list. It measures the proportion of queries
or instances where at least one relevant item appears within the top k positions. Hit@k
provides a binary evaluation, where a value of 1 indicates that there is at least one relevant
item within the top k positions, and a value of 0 indicates the absence of any relevant items.
— MRR: MRR is a metric used to measure the average reciprocal of the rank of the first relevant
item in a ranked list of results. The reciprocal rank is calculated as 1 divided by the rank of
the first relevant item. MRR provides a single value that represents the overall quality of the
ranking algorithm, with higher values indicating better performance.
— MR: MR is a metric used to measure the average rank of the first relevant item in a ranked list
of results. It provides an indication of how well a ranking algorithm is able to place relevant
items at the top of the list. Lower values of MR indicate better performance, as it means
relevant items are ranked higher on average.
In cases where multiple triples receive the same score, therandom protocol [108] is often used
to break ties and determine the order in which the triples are ranked. Table8 summarizes these
evaluation metrics.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:35
Table 8. Commonly Used Evaluation Metrics for KG Completion
Downstream Tasks Metric Definition Explanation
Link prediction
Hit@k
{
1 if rank(48, A:, 49)≤:
0 otherwise rank((48, A:, 49)) refers to
the rank of a positive triple(48, A:, 49)
against a list of negative examplesMRR 1
|$|
Í
(48,A:,49 ) 1
rank(48,A:,49 )
MR 1
|$|
Í
(48,A:,49 )rank(48, A:, 49)
Triple classification
Accuracy TP+TN
FN+TP+FP+TN
TP: true facts that are classified as true.
FP: false facts that are classified as true.
TN: true facts that are classified as false.
FN: false facts that are classified as false.
Precision TP
TP+FP
Recall TP
TP+FN
F- measure Precision.Recall
Precision+Recall
Triple Classification. Triple classification involves predicting whether an unseen triple(48, A:, 49 )
is true or false. For instance, the triple (Google, LocatedIn, Mountain View) should be classified
as a true fact, while (Google, LocatedIn, Phoenix) should be considered false. Triple classification
can be achieved by leveraging the plausibility score assigned to the triples. Triples with higher
scores are more likely to be true facts. To classify the triples, a threshold\A: is typically learned for
each relationA: . If the score5A: (48, 49 )of a triple(48, A:, 49 )is greater than the threshold\A: , it is
predicted as true. Otherwise, the triple is predicted as false.
Sincetripleclassificationessentiallydealswithbinaryclassification,traditionalmetricsforbinary
classification can be employed for evaluation. These metrics include accuracy, precision, recall, and
F-measure.
— ACC: ACC is a measure of the overall correctness of a classification. It represents the ratio of
correctly classified or retrieved instances to the total number of instances evaluated.
— Precision: Precision is a measure of the correctness of the positive predictions made by a
classification. It represents the ratio of true positive instances to the total number of instances
predicted as positive.
— Recall: Recall, also known as sensitivity or true positive rate, is a measure of the completeness
of positivepredictions made by a classification. It represents the ratio of true positive instances
to the total number of actual positive instances.
— F-measure: The F-measure, also called F1 score, is a metric that combines precision and recall
into a single value to assess the overall performance of a classification or information retrieval
system. It balances the trade-off between precision and recall. The F-measure is calculated as
the harmonic mean of precision and recall.
These metrics help assess the ACC of the triple classification task, providing insights into the
effectiveness of the employed models and techniques.
7.2 Complex Query Answering
The query answering task shares similarities with link prediction but with a key distinction. While
link prediction primarily focuses on one-hop queries in the form of(48, A:, ?)or (?, A:, 49 ), complex
query answering extends the scope to predicting answers for queries with a more intricate structure.
These complex queries may involve multiple hops, such as(48, A1, . . . , A =, ?). Figure8 provides an
illustration of the query structures commonly considered in complex query answering tasks. In the
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:36 K. Cheng et al.
1p 2p 3p
2i 3i ip ip
2u
up
u
u
u
u
Fig. 8. Query structures widely considered in complex query answering tasks. In the figure, “p” represents
“projection,” “i” represents “intersection,” and “u” represents “union.”
figure, “p” represents “projection”, “i” represents “intersection”, and “u” represents “union.” These
structures capture the complexity of queries involving multiple relationships and operations.
By expanding the scope to complex query structures, complex query answering tasks aim to
provide more nuanced and comprehensive answers that go beyond simple one-hop queries. This
enables the exploration of more intricate patterns and dependencies within the KG, enhancing the
ability to address complex information retrieval and inference tasks.
7.3 Relational Reasoning
Relational Reasoning is a task focused on predicting the relations between two given entities,
represented as(ℎ, ?, C). It is also referred to as the relation prediction task, where the objective is to
learn scores to rank candidate relations instead of ranking candidate entities.
Theevaluationmetricscommonlyusedinlinkprediction,suchasHit@kandMRR,canbeapplied
to assess the performance of relational reasoning. Additionally, since the number of relations in a
KG is typically limited, the relational reasoning task can be treated as a multi-class classification
problem. ACC is a commonly used evaluation metric in this context.
An even more challenging variant of relational reasoning is the inductive relational reasoning
task.Thistaskteststhesystematicgeneralizationcapabilityofamodelbyinferringmissingrelations
between two entities(ℎ, ?, C)with a greater number of hops than what was seen during training.
During training, the model is trained to infer the relationship between two entities by traversing a
limited number of edges (e.g., two, three, or four edges). However, during evaluation, the model is
tasked with traversing up to ten edges. Due to the difficulty of this setting, only a few rule learning
methods, including CTPs [71], R5 [65], and RLogic [16], are capable of effectively handling this
task. These methods enable the model to reason and make predictions over longer relational paths,
showcasing enhanced systematic generalization capabilities and advancing the field of relational
reasoning.
8 Other Directions
Significant progress has been made in the field of neural-symbolic KG reasoning, addressing various
challenges and advancing its applications. However, there are still several important problems
which we haven’t discussed in detail in this survey due to the space limitation.
— Temporal reasoning: Temporal reasoning is a vital component in many real-world applications
across diverse fields such as finance, healthcare, and logistics, where the understanding
of how knowledge evolves over time is crucial. Temporal reasoning over KGs entails not
only predicting future events but also understanding historical contexts and the dynamic
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:37
relationships between entities over time. This form of reasoning leverages the rich, structured
data within a KG that includes temporal attributes, enabling the inference of both past
and future states of entities. Recent advancements in this area have introduced various
innovative approaches to enhance the ACC and efficiency of temporal reasoning. Researchers
have developed methods that incorporate time-sensitive algorithms to better model how
relationships within the graph change over time [59, 135]. For example, some techniques
focus on embedding temporal data to capture the evolution of entities and their interrelations,
allowing for more nuanced predictions and analyses [52]. Others employ machine learning
models that predict potential future links or the evolution of existing links in the graph,
considering the historical temporal patterns observed [59, 126]. These approaches address
differentaspects oftemporalreasoningby enhancingtheability tohandlelarge-scaletemporal
data, improving the prediction of temporal relationships, and increasing the granularity with
which time is represented in models. The ongoing developments in temporal reasoning over
KGs not only push the boundaries of what is possible with KGs but also open up new avenues
for exploring how artificial intelligence can be applied to complex temporal datasets.
— Multi-modal reasoning: KGs are not limited to storing simple structured data; they often
encapsulate diverse data modalities, including textual descriptions, images, audio recordings,
andsometimesevenvideocontent.ThisrichblendofdatatypesmakesKGsincrediblyversatile
and valuable for various applications that require a deep understanding of context and content
relationships. The symbiotic relationship between KGs and multi-modal learning, shows how
these technologies converge to enhance both artificial intelligence applications and data
handling, which categorizes the research into two primary areas: KG-driven Multi-Modal
(KG4MM) learning andMulti-Modal Knowledge Graph (MM4KG) . The former focuses
on how KGs can enhance multi-modal learning applications. For instance, KGs can provide
contextual grounding for complex tasks in natural language processing, computer vision, and
other areas by linking relevant data from multiple modalities [107, 118, 125]. On the other
hand, MM4KG investigates how multi-modal data can be utilized to enrich KGs themselves.
This includes techniques for integrating and synthesizing data from various sources and
formats into a unified graph structure [13, 117, 121], thereby enhancing the KG’s utility for
diverse applications. For example, incorporating image data into a KG can help in tasks like
image classification or recognition by providing additional context or annotations that are
linked to other data modalities. This distinction is crucial for delineating tasks where KGs
support multi-modal learning from those where multi-modal data enhance KG applications.
By exploring both areas, researchers aim to unlock new capabilities and improve the efficiency
and ACC of existing models, thereby paving the way for more intelligent and responsive
systems. This also includes examining challenges like data integration, semantic consistency,
and the scalability of models in handling multi-modal data within KGs.
— Developing interactive reasoning systems: Interactive KG reasoning systems, which allow
for natural and intuitive user interactions, possess considerable potential to transform how
users access and interact with complex datasets. Future research in this domain could focus
on several key areas to maximize the utility and accessibility of these systems. Firstly, the
development of advanced interactive interfaces is crucial. These interfaces could take the
form of sophisticated dialogue systems that allow users to communicate with KGs through
conversational interactions. By employing natural language processing techniques, these
systems could interpret and respond to user queries in a manner that feels both natural and
intuitive [91]. Additionally, visual interaction platforms could be developed to provide a more
immersive way to explore KGs [5]. These platforms would use graphical representations to
display information, allowing users to navigate through layers of data visually. This could be
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:38 K. Cheng et al.
particularlyusefulforuserswhoarenotexpertsindatascience,asitprovidesamoreaccessible
entrypointtocomplexinformation.Furthermore,theseinteractivesystemsshouldbedesigned
to support user queries effectively [79]. This involves not only recognizing and responding
to the query but also providing meaningful explanations for the reasoning outcomes. For
example, when a user asks a complex question that involves multiple data points within
the KG, the system should be able to trace and articulate the pathways of reasoning that
led to its conclusion. This transparency in the reasoning process is essential for building
trust and understanding. Finally, there is a need for mechanisms that allow for collaborative
exploration and refinement of KG knowledge. Users should be able to add to or modify the
KG based on new information or corrections, ideally through an interface that simplifies these
contributions. This could involve collaborative filtering techniques, where suggestions from
users are vetted through community feedback or expert review before being integrated into
the KG. These enhancements will not only make KGs more interactive but also transform
them into dynamic tools that evolve and improve through user interaction. As such, they
promise to make the wealth of information in KGs more accessible and useful for a broader
range of applications and users.
— Combining with LLM: This survey explores the effective use of well-structured KGs in enhanc-
ing reasoning capabilities. Recently, LLMs such as ChatGPT and GPT-4 have captured signifi-
cant attention in the reasoning sphere owing to their emergent capabilities and wide-ranging
applicability. However, these models are prone to generating inaccurate or “hallucinated”
contentandoftenstruggletoaccessfactualknowledgedirectly.Incontrast,KGslikeWikipedia
serve as reliable repositories that explicitly store factual information, making them highly
trustworthy. Integrating KGs with LLMs offers a promising solution to mitigate the issue
of hallucination and improve the reliability of the generated content. While KGs provide a
solid foundation of verified facts, they are often difficult to construct and keep updated, pos-
ing challenges in incorporating new facts and representing emerging knowledge accurately.
To leverage the strengths of both LLMs and KGs, several approaches have been proposed,
mainly categorized into three primary frameworks: (1) KG-enhanced LLMs: This approach
integrates KGs during the pre-training and inference stages of LLMs, or to enhance the depth
of knowledge understanding by LLMs [50, 123]. (2) LLM-augmented KGs: Here, LLMs are
utilized to perform various KG-related tasks such as embedding, completion, construction,
graph-to-text conversion, and question answering [54, 69]. (3) Synergized LLMs + KGs: This
framework fosters a collaborative environment where both systems operate in tandem, bene-
fiting mutually to promote bi-directional reasoning driven by both data and knowledge [15,
41, 66]. By synthesizing the capabilities of LLMs with the structured factual data of KGs, this
integrated approach not only improves the ACC and trustworthiness of reasoning processes
but also advances the development and refinement of knowledge representations in dynamic
real-world applications.
9 Conclusion
In this paper, we provide a comprehensive overview of recent progress in the field of neural-
symbolicmethodsforKGreasoning.Wehaveexaminedthekeycontributionswithinthedomainsof
symbolic reasoning and neural reasoning and discussed their respective advantages and drawbacks.
To leverage the advantages of both approaches, we delve into the latest endeavors aimed at blending
these two approaches into a cohesive neural-symbolic paradigm.
While the field of neural-symbolic reasoning is still in its early stages, the progress made so
far suggests that neural-symbolic methods have great potential to enhance the capabilities of KG
reasoning systems. However, more research is needed to address the challenges that remain, such
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:39
as the trade-off between scalability and interpretability, and to further push the boundaries of what
is possible in KG reasoning. We hope that this survey will serve as a useful resource for researchers
interested in the intersection of neural networks and symbolic reasoning for KGs, and we look
forward to witnessing the exciting developments in this field in the years to come.
References
[1] Erik Arakelyan, Daniel Daza, Pasquale Minervini, and Michael Cochez. 2020. Complex query answering with neural
link predictors. arXiv:2011.03459. Retrieved fromhttps://www.arxiv.org/abs/2011.03459
[2] Stephen H. Bach, Matthias Broecheler, Bert Huang, and Lise Getoor. 2017. Hinge-loss Markov random fields and
probabilistic soft logic.The Journal of Machine Learning Research18, 1 (2017), 3846–3912.
[3] Ivana Balažević, Carl Allen, and Timothy M. Hospedales. 2019. Hypernetwork knowledge graph embeddings. In
Proceedings of the International Conference on Artificial Neural Networks. Springer, 553–565.
[4] Ivana Balažević, Carl Allen, and Timothy M. Hospedales. 2019. Tucker: Tensor factorization for knowledge graph
completion. arXiv:1901.09590. Retrieved fromhttps://arxiv.org/abs/1901.09590
[5] Luigi Bellomarini, Marco Benedetti, Andrea Gentili, Davide Magnanimi, and Emanuel Sallinger. 2023. KG-Roar:
Interactive datalog-based reasoning on virtual knowledge graphs.Proceedings of the VLDB Endowment16, 12 (2023),
4014–4017.
[6] Antoine Bordes, Xavier Glorot, Jason Weston, and Yoshua Bengio. 2014. A semantic matching energy function for
learning with multi-relational data.Machine Learning94, 2 (2014), 233–259.
[7] Antoine Bordes, Nicolas Usunier, Alberto Garcia-Duran, Jason Weston, and Oksana Yakhnenko. 2013. Translat-
ing embeddings for modeling multi-relational data. InProceedings of the 26th International Conference on Neural
Information Processing Systems, 2787–2795.
[8] Andres Campero, Aldo Pareja, Tim Klinger, Josh Tenenbaum, and Sebastian Riedel. 2018. Logical rule induction and
theory learning using neural theorem proving. arXiv:1809.02193. Retrieved fromhttps://arxiv.org/abs/1809.02193
[9] Chain Monte Carlo. 2004. Markov chain monte carlo and gibbs sampling.Lecture Notes for EEB581 (2004), 1–24.
[10] Rudolf Carnap. 2012.Introduction to Symbolic Logic and Its Applications. Courier Corporation.
[11] Xuelu Chen, Muhao Chen, Weijia Shi, Yizhou Sun, and Carlo Zaniolo. 2019. Embedding uncertain knowledge graphs.
In Proceedings of the AAAI Conference on Artificial Intelligence, Vol. 33, 3363–3370.
[12] Xuelu Chen, Ziniu Hu, and Yizhou Sun. 2022. Fuzzy logic based logical query answering on knowledge graphs. In
Proceedings of the AAAI Conference on Artificial Intelligence, Vol. 36, 3939–3948.
[13] Zhuo Chen, Yin Fang, Yichi Zhang, Lingbing Guo, Jiaoyan Chen, Huajun Chen, and Wen Zhang. 2024. The power of
noise: Toward a unified multi-modal knowledge graph representation framework. arXiv:2403.06832. Retrieved from
https://arxiv.org/abs/2403.06832
[14] Kewei Cheng, Nesreen Ahmed, and Yizhou Sun. 2023. Neural compositional rule learning for knowledge graph
reasoning. InProceedings of the International Conference on Learning Representations (ICLR).
[15] Kewei Cheng, Nesreen K. Ahmed, Theodore Willke, and Yizhou Sun. 2024. Structure guided prompt: Instructing
large language model in multi-step reasoning by exploring graph structure of the text. arXiv:2402.13415. Retrieved
from https://arxiv.org/abs/2402.13415
[16] Kewei Cheng, Jiahao Liu, Wei Wang, and Yizhou Sun. 2022. RLogic: Recursive logical rule learning from knowledge
graphs. InProceedings of the ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD),
179–189.
[17] William W. Cohen. 2016. Tensorlog: A differentiable deductive database. arXiv:1605.06523. Retrieved fromhttps:
//arxiv.org/abs/1605.06523
[18] Michael Collins, Sanjoy Dasgupta, and Robert E. Schapire. 2001. A generalization of principal components analysis to
the exponential family. InProceedings of the 14th International Conference on Neural Information Processing Systems:
Natural and Synthetic (NIPS ’01), Vol. 13, 617–624.
[19] Yuanfei Dai, Shiping Wang, Neal N. Xiong, and Wenzhong Guo. 2020. A survey on knowledge graph embedding:
Approaches, applications and benchmarks.Electronics 9, 5 (2020), 750.
[20] Rajarshi Das, Shehzaad Dhuliawala, Manzil Zaheer, Luke Vilnis, Ishan Durugkar, Akshay Krishnamurthy, Alex
Smola, and Andrew McCallum. 2017. Go for a walk and arrive at the answer: Reasoning over paths in knowledge
bases using reinforcement learning. arXiv:1711.05851. Retrieved fromhttps://arxiv.org/abs/1711.05851
[21] Rajarshi Das, Arvind Neelakantan, David Belanger, and Andrew McCallum. 2016. Chains of reasoning over entities,
relations,andtextusingrecurrentneuralnetworks.arXiv:1607.01426.Retrievedfrom https://arxiv.org/abs/1607.01426
[22] Martin Davis, George Logemann, and Donald Loveland. 1962. A machine program for theorem-proving.Communi-
cations of the ACM5, 7 (1962), 394–397.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:40 K. Cheng et al.
[23] Luc Dehaspe and Hannu Toivonen. 1999. Discovery of frequent datalog patterns.Data Mining and Knowledge
Discovery 3, 1 (1999), 7–36.
[24] LucDehaspeandHannuToivonen.2001.Discoveryofrelationalassociationrules.In Relational Data Mining.Springer,
189–212.
[25] Thomas Demeester, Tim Rocktäschel, and Sebastian Riedel. 2016. Lifted rule injection for relation embeddings.
arXiv:1606.08359. Retrieved fromhttps://arxiv.org/abs/1606.08359
[26] Tim Dettmers, Pasquale Minervini, Pontus Stenetorp, and Sebastian Riedel. 2018. Convolutional 2d knowledge graph
embeddings. InProceedings of the 32nd AAAI Conference on Artificial Intelligence.
[27] Xin Dong, Evgeniy Gabrilovich, Geremy Heitz, Wilko Horn, Ni Lao, Kevin Murphy, Thomas Strohmann, Shaohua
Sun, and Wei Zhang. 2014. Knowledge vault: A web-scale approach to probabilistic knowledge fusion. InProceedings
of the ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD),601–610.
[28] Richard Evans and Edward Grefenstette. 2018. Learning explanatory rules from noisy data.Journal of Artificial
Intelligence Research61 (2018), 1–64.
[29] Miao Fan, Qiang Zhou, Emily Chang, and Fang Zheng. 2014. Transition-based knowledge graph embedding with
relational mapping properties. InProceedings of the 28th Pacific Asia Conference on Language, Information and
Computing, 328–337.
[30] Luis Galárraga, Christina Teflioudi, Katja Hose, and Fabian M. Suchanek. 2015. Fast rule mining in ontological
knowledge bases with AMIE+.The VLDB Journal—The International Journal on Very Large Data Bases24, 6 (2015),
707–730.
[31] Luis Antonio Galárraga, Christina Teflioudi, Katja Hose, and Fabian Suchanek. 2013. AMIE: Association rule mining
under incomplete evidence in ontological knowledge bases. InProceedings of the 22nd International Conference on
World Wide Web.ACM, 413–422.
[32] Zhenxiang Gao, Pingjian Ding, and Rong Xu. 2022. Kg-predict: A knowledge graph computational framework for
drug repurposing.Journal of Biomedical Informatics132 (2022), Article 104133.
[33] Matt Gardner, Partha Talukdar, Bryan Kisiel, and Tom Mitchell. 2013. Improving learning and inference in a large
knowledge-base using latent syntactic cues. InProceedings of the 2013 Conference on Empirical Methods in Natural
Language Processing, 833–838.
[34] Matt Gardner, Partha Talukdar, Jayant Krishnamurthy, and Tom Mitchell. 2014. Incorporating vector space similarity
in random walk inference over knowledge bases. InProceedings of the Conference on Empirical Methods in Natural
Language Processing (EMNLP),397–406.
[35] Zoubin Ghahramani. 2015. Probabilistic machine learning and artificial intelligence.Nature 521, 7553 (2015),
452–459.
[36] Fred Glover. 1986. Future paths for integer programming and links to artificial intelligence.Computers & Operations
Research 13, 5 (1986), 533–549.
[37] Marco Grassia, Manlio De Domenico, and Giuseppe Mangioni. 2021. mGNN: Generalizing the graph neural networks
to the multilayer case. arXiv:2109.10119.
[38] Lingbing Guo, Zequn Sun, and Wei Hu. 2019. Learning to exploit long-term relational dependencies in knowledge
graphs. InProceedings of the International Conference on Machine Learning.PMLR, 2505–2514.
[39] Shu Guo, Quan Wang, Lihong Wang, Bin Wang, and Li Guo. 2016. jointly embedding knowledge graphs and logical
rules. InProceedings of the 2016 Conference on Empirical Methods in Natural Language Processing, 192–202.DOI:
https://doi.org/10.18653/v1/D16-1019
[40] Shu Guo, Quan Wang, Lihong Wang, Bin Wang, and Li Guo. 2017. Knowledge graph embedding with iterative
guidance from soft rules. arXiv:1711.11231. Retrieved fromhttps://arxiv.org/abs/1711.11231
[41] TiezhengGuo,QingwenYang,ChenWang,YanyiLiu,PanLi,JiaweiTang,DapengLi,andYingyouWen.2023.Knowl-
edgeNavigator: Leveraging large language models for enhanced reasoning over knowledge graph. arXiv:2312.15880.
Retrieved fromhttps://arxiv.org/abs/2312.15880
[42] Petr Hájek. 2013.Metamathematics of Fuzzy Logic. Vol. 4. Springer Science & Business Media.
[43] Will Hamilton, Payal Bajaj, Marinka Zitnik, Dan Jurafsky, and Jure Leskovec. 2018. Embedding logical queries on
knowledge graphs. InProceedings of the 32nd International Conference on Neural Information Processing Systems,
2030–2041.
[44] L. Vivek Harsha Vardhan, Guo Jia, and Stanley Kok. 2020. Probabilistic logic graph attention networks for reasoning.
In Companion Proceedings of the Web Conference 2020 (WWW ’20). ACM, New York, NY, 669–673.DOI: https:
//doi.org/10.1145/3366424.3391265
[45] Aidan Hogan, Eva Blomqvist, Michael Cochez, Claudia d’Amato, Gerard de Melo, Claudio Gutierrez, Sabrina Kirrane,
José Emilio Labra Gayo, Roberto Navigli, Sebastian Neumaier, Axel-Cyrille Ngonga Ngomo, Axel Polleres, Sabbir M.
Rashid, Anisa Rula, Lukas Schmelzeisen, Juan Sequeda, Steffen Staab, and Antoine Zimmermann. 2021. Knowledge
graphs. ACM Computing Surveys54, 4 (2021), 1–37.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:41
[46] Holger H. Hoos and Thomas Stützle. 2000. Local search algorithms for SAT: An empirical evaluation.Journal of
Automated Reasoning24, 4 (2000), 421–481.
[47] Guoliang Ji, Shizhu He, Liheng Xu, Kang Liu, and Jun Zhao. 2015. Knowledge graph embedding via dynamic
mapping matrix. InProceedings of the 53rd Annual Meeting of the Association for Computational Linguistics and the
7th International Joint Conference on Natural Language Processing, Vol. 1, Long Papers, 687–696.
[48] Guoliang Ji, Kang Liu, Shizhu He, and Jun Zhao. 2016. Knowledge graph completion with adaptive sparse transfer
matrix. InProceedings of the 30th AAAI Conference on Artificial Intelligence.
[49] Shaoxiong Ji, Shirui Pan, Erik Cambria, Pekka Marttinen, and S. Yu Philip. 2021. A survey on knowledge graphs:
Representation, acquisition, and applications.IEEE Transactions on Neural Networks and Learning Systems33, 2
(2021), 494–514.
[50] Jinhao Jiang, Kun Zhou, Wayne Xin Zhao, Yaliang Li, and Ji-Rong Wen. 2023. ReasoningLM: Enabling structural
subgraph reasoning in pre-trained language models for question answering over knowledge graph. arXiv:2401.00158.
Retrieved fromhttps://arxiv.org/abs/2401.00158
[51] Xiaotian Jiang, Quan Wang, and Bin Wang. 2019. Adaptive convolution for multi-relational learning. InProceedings of
the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language
Technologies, Vol. 1, Long and Short Papers, 978–987.
[52] Songlin Jiao, Zhenfang Zhu, Wenqing Wu, Zicheng Zuo, Jiangtao Qi, Wenling Wang, Guangyuan Zhang, and Peiyu
Liu. 2023. An improving reasoning network for complex question answering over temporal knowledge graphs.
Applied Intelligence53, 7 (2023), 8195–8208.
[53] Seyed Mehran Kazemi and David Poole. 2018. Simple embedding for link prediction in knowledge graphs. In
Proceedings of the 32nd International Conference on Neural Information Processing Systems, 4284–4295.
[54] JihoKim,YeonsuKwon,YohanJo,andEdwardChoi.2023.KG-GPT:Ageneralframeworkforreasoningonknowledge
graphs using large language models. arXiv:2310.11220. Retrieved fromhttps://arxiv.org/abs/2310.11220
[55] Thomas N. Kipf and Max Welling. 2016. Semi-supervised classification with graph convolutional networks.
arXiv:1609.02907. Retrieved fromhttps://arxiv.org/abs/1609.02907
[56] Timothée Lacroix, Nicolas Usunier, and Guillaume Obozinski. 2018. Canonical tensor decomposition for knowledge
base completion. InProceedings of the International Conference on Machine Learning.PMLR, 2863–2872.
[57] Ni Lao, Tom Mitchell, and William Cohen. 2011. Random walk inference and learning in a large scale knowledge
base. InProceedings of the 2011 Conference on Empirical Methods in Natural Language Processing, 529–539.
[58] Yann LeCun and Yoshua Bengio. 1995. Convolutional networks for images, speech, and time series. InThe Handbook
of Brain Theory and Neural Networks. MIT Press, Cambridge, MA, 255–258.
[59] Ke Liang, Lingyuan Meng, Meng Liu, Yue Liu, Wenxuan Tu, Siwei Wang, Sihang Zhou, and Xinwang Liu. 2023.
Learn from relational correlations and periodic events for temporal knowledge graph reasoning. InProceedings of
the 46th International ACM SIGIR Conference on Research and Development in Information Retrieval, 1559–1568.
[60] Xi Victoria Lin, Richard Socher, and Caiming Xiong. 2018. Multi-hop knowledge graph reasoning with reward
shaping. arXiv:1808.10568. Retrieved fromhttps://arxiv.org/abs/1808.10568
[61] Yankai Lin, Zhiyuan Liu, Maosong Sun, Yang Liu, and Xuan Zhu. 2015. Learning entity and relation embeddings for
knowledge graph completion. InProceedings of the 29th AAAI Conference on Artificial Intelligence.
[62] HanxiaoLiu,YuexinWu,andYimingYang.2017.Analogicalinferenceformulti-relationalembeddings.In Proceedings
of the International Conference on Machine Learning.PMLR, 2168–2178.
[63] Lihui Liu, Boxin Du, Heng Ji, ChengXiang Zhai, and Hanghang Tong. 2021. Neural-answering logical queries on
knowledge graphs. InProceedings of the 27th ACM SIGKDD Conference on Knowledge Discovery & Data Mining,
1087–1097.
[64] Shixuan Liu, Changjun Fan, Kewei Cheng, Yunfei Wang, Peng Cui, Yizhou Sun, and Zhong Liu. 2023. Inductive
meta-path learning for schema-complex heterogeneous information networks. arXiv:2307.03937. Retrieved from
https://arxiv.org/abs/2307.03937
[65] Shengyao Lu, Bang Liu, Keith G. Mills, Shangling JUI, and Di Niu. 2022. R5: Rule discovery with reinforced and
recurrent relational reasoning. InProceedings of the International Conference on Learning Representations. Retrieved
from https://openreview.net/forum?id=2eXhNpHeW6E
[66] Linhao Luo, Yuan-Fang Li, Gholamreza Haffari, and Shirui Pan. 2023. Reasoning on graphs: Faithful and interpretable
large language model reasoning. arXiv:2310.01061. Retrieved fromhttps://arxiv.org/abs/2310.01061
[67] João P. Marques Silva and Karem A. Sakallah. 2003.GRASP—A New Search Algorithm for Satisfiability. Springer.
[68] Christian Meilicke, Melisachew Wudage Chekol, Daniel Ruffinelli, and Heiner Stuckenschmidt. 2019. Anytime
bottom-up rule learning for knowledge graph completion. InProceedings of the 28th International Joint Conference on
Artificial Intelligence (IJCAI ’19), 3137–3143.
[69] Lars-Peter Meyer, Claus Stadler, Johannes Frey, Norman Radtke, Kurt Junghanns, Roy Meissner, Gordian Dziwis,
Kirill Bulert, and Michael Martin. 2023. Llm-assisted knowledge graph engineering: Experiments with chatgpt. In
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:42 K. Cheng et al.
Proceedings of the Working Conference on Artificial Intelligence Development for a Resilient and Sustainable Tomorrow.
Springer, 103–115.
[70] Pasquale Minervini, Matko Bosnjak, Tim Rocktäschel, and Sebastian Riedel. 2018. Towards neural theorem proving
at scale. arXiv:1807.08204. Retrieved fromhttps://arxiv.org/abs/1807.08204
[71] Pasquale Minervini, Sebastian Riedel, Pontus Stenetorp, Edward Grefenstette, and Tim Rocktäschel. 2020. Learning
reasoning strategies in end-to-end differentiable proving. InProceedings of the International Conference on Machine
Learning. PMLR, 6938–6949.
[72] Stephen Muggleton. 1995. Inverse entailment and Progol.New Generation Computing13, 3–4 (1995), 245–286.
[73] Stephen Muggleton and Cao Feng. 1990.Efficient Induction of Logic Programs. Citeseer.
[74] Radford M. Neal and Geoffrey E. Hinton. 1998. A view of the EM algorithm that justifies incremental, sparse, and
other variants. InLearning in Graphical Models. Springer, 355–368.
[75] ArvindNeelakantan,BenjaminRoth,andAndrewMcCallum.2015.Compositionalvectorspacemodelsforknowledge
base completion. arXiv:1504.06662. Retrieved fromhttps://arxiv.org/abs/1504.06662
[76] Dai Quoc Nguyen, Tu Dinh Nguyen, Dat Quoc Nguyen, and Dinh Phung. 2017. A novel embedding model for
knowledge base completion based on convolutional neural network. arXiv:1712.02121. Retrieved fromhttps://arxiv.
org/abs/1712.02121
[77] Maximilian Nickel, Lorenzo Rosasco, and Tomaso Poggio. 2016. Holographic embeddings of knowledge graphs. In
Proceedings of the AAAI Conference on Artificial Intelligence, Vol. 30.
[78] Maximilian Nickel, Volker Tresp, and Hans-Peter Kriegel. 2011. A three-way model for collective learning on multi-
relational data. InProceedings of the 28th International Conference on International Conference on Machine Learning
(ICML ’11), Vol. 11, 809–816.
[79] Gustav Nikopensius, Mohit Mayank, Orchid Chetia Phukan, and Rajesh Sharma. 2023. Reinforcement learning-based
knowledge graph reasoning for explainable fact-checking. InProceedings of the International Conference on Advances
in Social Networks Analysis and Mining, 164–170.
[80] Pouya Ghiasnezhad Omran, Kewen Wang, and Zhe Wang. 2018. Scalable rule learning via learning representation.
In Proceedings of the 27th International Joint Conference on Artificial Intelligence (IJCAI ’18), 2149–2155.
[81] Christos H. Papadimitriou. 2003. Computational complexity. InEncyclopedia of Computer Science. John Wiley and
Sons Ltd., UK, 260–265.
[82] Giuseppe Pirrò. 2020. Relatedness and TBox-driven rule learning in large knowledge bases. InProceedings of the
AAAI Conference on Artificial Intelligence, Vol. 34, 2975–2982.
[83] Hoifung Poon, Pedro M. Domingos, and Marc Sumner. 2008. A general method for reducing the complexity of
relational inference and its application to MCMC. InProceedings of the 23rd National Conference on Artificial
Intelligence (AAAI ’08), Vol. 8, 1075–1080.
[84] Achilleas Psyllidis. 2015. Ontology-based data integration from heterogeneous urban systems: A knowledge rep-
resentation framework for smart cities. InProceedings of the 14th International Conference on Computers in Urban
Planning and Urban Management (CUPUM ’14)MIT Press.
[85] Richard Qian. 2013. Understand Your World with Bing. Retrieved March 21, 2013 fromhttps://blogs.bing.com/search/
2013/03/21/understand-your-world-with-bing/
[86] Meng Qu, Junkun Chen, Louis-Pascal Xhonneux, Yoshua Bengio, and Jian Tang. 2020. Rnnlogic: Learning logic rules
for reasoning on knowledge graphs. arXiv:2010.04029. Retrieved fromhttps://arxiv.org/abs/2010.04029
[87] MengQuandJianTang.2019.Probabilisticlogicneuralnetworksforreasoning.In Proceedingsofthe33rdInternational
Conference on Neural Information Processing Systems, 7710–7720.
[88] J. Ross Quinlan. 1990. Learning logical definitions from relations.Machine Learning5, 3 (1990), 239–266.
[89] Hongyu Ren, Weihua Hu, and Jure Leskovec. 2020. Query2box: Reasoning over knowledge graphs in vector space
using box embeddings. arXiv:2002.05969. Retrieved fromhttps://arxiv.org/abs/2002.05969
[90] Hongyu Ren and Jure Leskovec. 2020. Beta embeddings for multi-hop logical reasoning in knowledge graphs. In
Proceedings of the 34th International Conference on Neural Information Processing Systems, 19716–19726.
[91] Xuhui Ren, Tong Chen, Quoc Viet Hung Nguyen, Lizhen Cui, Zi Huang, and Hongzhi Yin. 2024. Explicit knowledge
graph reasoning for conversational recommendation.ACM Transactions on Intelligent Systems and Technology15, 4
(2024), 1–21.
[92] Matthew Richardson and Pedro Domingos. 2006. Markov logic networks.Machine Learning62, 1–2 (2006), 107–136.
[93] Tim Rocktäschel and Sebastian Riedel. 2017. End-to-end differentiable proving. InProceedings of the 31st International
Conference on Neural Information Processing Systems, 3788–3800.
[94] Tim Rocktäschel, Sameer Singh, and Sebastian Riedel. 2015. Injecting logical background knowledge into embeddings
for relation extraction. InProceedings of the 2015 Conference of the North American Chapter of the Association for
Computational Linguistics: Human Language Technologies, 1119–1129.
[95] Stuart Russell and Peter Norvig. 2002.Artificial Intelligence: A Modern Approach. Prentice Hall.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

Neural-Symbolic Methods for KG Reasoning: A Survey 225:43
[96] Ali Sadeghian, Mohammadreza Armandpour, Patrick Ding, and Daisy Zhe Wang. 2019. Drum: End-to-end differen-
tiable rule mining on knowledge graphs. arXiv:1911.00055. Retrieved fromhttps://arxiv.org/abs/1911.00055
[97] Eric Salvat and Marie-Laure Mugnier. 1996. Sound and complete forward and backward chainings of graph rules. In
Proceedings of the International Conference on Conceptual Structures. Springer, 248–262.
[98] Michael Schlichtkrull, Thomas N. Kipf, Peter Bloem, Rianne van den Berg, Ivan Titov, and Max Welling. 2018.
Modeling relational data with graph convolutional networks. InProceedings of the European Semantic Web Conference.
Springer, 593–607.
[99] Peter Schüller and Mishal Benz. 2018. Best-effort inductive logic programming via fine-grained cost-based hypothesis
generation. Machine Learning107, 7 (2018), 1141–1169.
[100] Mike Schuster and Kuldip K. Paliwal. 1997. Bidirectional recurrent neural networks.IEEE Transactions on Signal
Processing 45, 11 (1997), 2673–2681.
[101] Chao Shang, Yun Tang, Jing Huang, Jinbo Bi, Xiaodong He, and Bowen Zhou. 2019. End-to-end structure-aware
convolutionalnetworksforknowledgebasecompletion.In ProceedingsoftheAAAIConferenceonArtificialIntelligence ,
Vol. 33, 3060–3067.
[102] Yelong Shen, Jianshu Chen, Po-Sen Huang, Yuqing Guo, and Jianfeng Gao. 2018. M-walk: Learning to walk over
graphs using monte carlo tree search. arXiv:1802.04394. Retrieved fromhttps://arxiv.org/abs/1802.04394
[103] Chen Shengyuan, Yunfeng Cai, Huang Fang, Xiao Huang, and Mingming Sun. 2024. Differentiable neuro-symbolic
reasoning on large-scale knowledge graphs.Proceedings of the 37th International Conference on Neural Information
Processing Systems, 28139–2815.
[104] Parag Singla and Pedro M. Domingos. 2008. Lifted first-order belief propagation. InProceedings of the 23rd National
Conference on Artificial Intelligence (AAAI ’08), Vol. 8, 1094–1099.
[105] Richard Socher, Danqi Chen, Christopher D. Manning, and Andrew Ng. 2013. Reasoning with neural tensor networks
for knowledge base completion. InProceedings of the 26th International Conference on Neural Information Processing
Systems, 926–934.
[106] William M Spears. 1993. Simulated annealing for hard satisfiability problems.Cliques, Coloring, and Satisfiability26
(1993), 533–558.
[107] Chengjie Sun, Weiwei Chen, Lei Lin, and Lili Shan. 2023. Enhancing recommender system with multi-modal
knowledge graph. InProceedings of the Chinese Conference on Pattern Recognition and Computer Vision (PRCV).
Springer, 395–407.
[108] Zhiqing Sun, Shikhar Vashishth, Soumya Sanyal, Partha Talukdar, and Yiming Yang. 2019. A re-evaluation of
knowledge graph completion methods. arXiv:1911.03903. Retrieved fromhttps://arxiv.org/abs/1911.03903
[109] ThéoTrouillon,JohannesWelbl,SebastianRiedel,ÉricGaussier,andGuillaumeBouchard.2016.Complexembeddings
for simple link prediction. InProceedings of the International Conference on Machine Learning, 2071–2080.
[110] Shikhar Vashishth, Soumya Sanyal, Vikram Nitin, Nilesh Agrawal, and Partha Talukdar. 2020. Interacte: Improving
convolution-based knowledge graph embeddings by increasing feature interactions. InProceedings of the AAAI
Conference on Artificial Intelligence, Vol. 34, 3009–3016.
[111] Shikhar Vashishth, Soumya Sanyal, Vikram Nitin, and Partha Talukdar. 2019. Composition-based multi-relational
graph convolutional networks. arXiv:1911.03082.
[112] Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N Gomez, Ł Kaiser, and Illia
Polosukhin. 2017. Attention is all you need. InProceedings of the 31st International Conference on Neural Information
Processing Systems on Neural Information Processing Systems, 6000–6010.
[113] Pengwei Wang, Dejing Dou, Fangzhao Wu, Nisansa de Silva, and Lianwen Jin. 2019. Logic rules powered knowledge
graph embedding. arXiv:1903.03772. Retrieved fromhttps://arxiv.org/abs/1903.03772
[114] Quan Wang, Pingping Huang, Haifeng Wang, Songtai Dai, Wenbin Jiang, Jing Liu, Yajuan Lyu, Yong Zhu, and Hua
Wu. 2019b. Coke: Contextualized knowledge graph embedding. arXiv:1911.02168. Retrieved fromhttps://arxiv.org/
abs/1911.02168
[115] Quan Wang, Zhendong Mao, Bin Wang, and Li Guo. 2017. Knowledge graph embedding: A survey of approaches
and applications.IEEE Transactions on Knowledge and Data Engineering29, 12 (2017), 2724–2743.
[116] Quan Wang, Bin Wang, and Li Guo. 2015. Knowledge base completion using embeddings and rules. InProceedings of
the 24th International Joint Conference on Artificial Intelligence.
[117] XinWang,BenyuanMeng,HongChen,YuanMeng,KeLv,andWenwuZhu.2023.TIVA-KG:Amultimodalknowledge
graph with text, image, video and audio. InProceedings of the 31st ACM International Conference on Multimedia,
2391–2399.
[118] Yan Wang, Peize Li, Qingyi Si, Hanwen Zhang, Wenyu Zang, Zheng Lin, and Peng Fu. 2023. Cross-modality multiple
relations learning for knowledge-based visual question answering.ACM Transactions on Multimedia Computing,
Communications and Applications20, 3 (2023), 1–22.
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.

225:44 K. Cheng et al.
[119] Zhen Wang, Jianwen Zhang, Jianlin Feng, and Zheng Chen. 2014. Knowledge graph embedding by translating on
hyperplanes. InProceedings of the 28th AAAI Conference on Artificial Intelligence.
[120] Zhuoyu Wei, Jun Zhao, Kang Liu, Zhenyu Qi, Zhengya Sun, and Guanhua Tian. 2015. Large-scale knowledge base
completion: Inferring via grounding network sampling over selected instances. InProceedings of the 24th ACM
International on Conference on Information and Knowledge Management.ACM, 1331–1340.
[121] Yinan Wu, Xiaowei Wu, Junwen Li, Yue Zhang, Haofen Wang, Wen Du, Zhidong He, Jingping Liu, and Tong Ruan.
2023. Mmpedia: A large-scale multi-modal knowledge graph. InProceedings of the International Semantic Web
Conference. Springer, 18–37.
[122] Han Xiao, Minlie Huang, Yu Hao, and Xiaoyan Zhu. 2015. Transg: A generative mixture model for knowledge graph
embedding. arXiv:1509.05488. Retrieved fromhttps://arxiv.org/abs/1509.05488
[123] XinXie,ZhouboLi,XiaohanWang,ZekunXi,andNingyuZhang.2022.Lambdakg:Alibraryforpre-trainedlanguage
model-based knowledge graph embeddings. arXiv:2210.00305. Retrieved fromhttps://arxiv.org/abs/2210.00305
[124] Wenhan Xiong, Thien Hoang, and William Yang Wang. 2017. Deeppath: A reinforcement learning method for
knowledge graph reasoning. arXiv:1707.06690.Retrieved fromhttps://arxiv.org/abs/1707.06690
[125] Ning Xu, Yifei Gao, An-An Liu, Hongshuo Tian, and Yongdong Zhang. 2024. Multi-modal validation and domain
interaction learning for knowledge-based visual question answering.IEEE Transactions on Knowledge and Data
Engineering (2024), 1–12.
[126] Yi Xu, Junjie Ou, Hui Xu, and Luoyi Fu. 2023. Temporal knowledge graph reasoning with historical contrastive
learning. InProceedings of the AAAI Conference on Artificial Intelligence, Vol. 37, 4765–4773.
[127] Bishan Yang, Wen-tau Yih, Xiaodong He, Jianfeng Gao, and Li Deng. 2014. Embedding entities and relations for
learning and inference in knowledge bases. arXiv:1412.6575. Retrieved fromhttps://arxiv.org/abs/1412.6575
[128] Fan Yang, Zhilin Yang, and William W. Cohen. 2017. Differentiable learning of logical rules for knowledge base
reasoning. InProceedings of the 31st International Conference on Neural Information Processing Systems, 2319–2328.
[129] Yuan Yang and Le Song. 2019. Learn to explain efficiently via neural logic inductive learning. arXiv:1910.02481.
Retrieved fromhttps://arxiv.org/abs/1910.02481
[130] LiangYao,ChengshengMao,andYuanLuo.2019.KG-BERT:BERTforknowledgegraphcompletion.arXiv:1909.03193.
Retrieved fromhttps://arxiv.org/abs/1909.03193
[131] Rui Ye, Xin Li, Yujie Fang, Hongyu Zang, and Mingzhong Wang. 2019. A vectorized relational graph convolutional
network for multi-relational network alignment. InProceedings of the 28th International Joint Conference on Artificial
Intelligence (IJCAI ’19), 4135–4141.
[132] Jonathan S. Yedidia, William T. Freeman, and Yair Weiss. 2001. Generalized belief propagation. InProceedings of the
13th International Conference on Neural Information Processing Systems, 689–695.
[133] Denghui Zhang, Zixuan Yuan, Hao Liu, and Hui Xiong. 2022. Learning to walk with dual agents for knowledge
graph reasoning. InProceedings of the AAAI Conference on Artificial Intelligence, Vol. 36, 5932–5941.
[134] Jing Zhang, Bo Chen, Lingxi Zhang, Xirui Ke, and Haipeng Ding. 2021. Neural, symbolic and neural-symbolic
reasoning on knowledge graphs.AI Open2 (2021), 14–35.
[135] Mengqi Zhang, Yuwei Xia, Qiang Liu, Shu Wu, and Liang Wang. 2023. Learning latent relations for temporal
knowledge graph reasoning. InProceedings of the 61st Annual Meeting of the Association for Computational Linguistics,
Vol. 1, Long Papers, 12617–12631.
[136] WenZhang,JiaoyanChen,JuanLi,ZezhongXu,JeffZPan,andHuajunChen.2022a.Knowledgegraphreasoningwith
logics and embeddings: Survey and perspective. arXiv:2202.07412. Retrieved fromhttps://arxiv.org/abs/2202.07412
[137] Yuyu Zhang, Xinshi Chen, Yuan Yang, Arun Ramamurthy, Bo Li, Yuan Qi, and Le Song. 2019. Can graph neural
networks help logic reasoning? arXiv:1906.02111. Retrieved fromhttps://arxiv.org/abs/1906.02111
[138] Zhaocheng Zhu, Mikhail Galkin, Zuobai Zhang, and Jian Tang. 2022. Neural-symbolic models for logical queries on
knowledge graphs. arXiv:2205.10128. Retrieved fromhttps://arxiv.org/abs/2205.10128
[139] Zhaocheng Zhu, Xinyu Yuan, Michael Galkin, Louis-Pascal Xhonneux, Ming Zhang, Maxime Gazeau, and Jian Tang.
2024. A* net: A scalable path-based reasoning approach for knowledge graphs. InProceedings of the 37th International
Conference on Neural Information Processing Systems, 59323–5933.
Received 8 September 2023; revised 21 April 2024; accepted 28 July 2024
ACM Transactions on Knowledge Discovery from Data, Vol. 18, No. 9, Article 225. Publication date: November 2024.
```
