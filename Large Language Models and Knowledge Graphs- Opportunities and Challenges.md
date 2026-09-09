---
title: "Large Language Models and Knowledge Graphs: Opportunities and Challenges"
author: Jeff Z. Pan, Simon Razniewski, Jan-Christoph Kalo, Sneha Singhania, Jiaoyan Chen, Stefan Dietze, Hajira Jabeen, Janna Omeliyanenko, Zhang, Wen, Matteo Lissandrini, Russa Biswas, Gerard de Melo, Angela Bonifati, Edlira Vakaj, Mauro Dragoni, Damien Graux
year: "2023"
Type: Preprint
DOI: 10.4230/tgdk.1.1.2
source: https://doi.org/10.4230/tgdk.1.1.2
created: 2026-08-06
description: Large Language Models (LLMs) have taken Knowledge Representation - and the world - by storm. This inflection point marks a shift from explicit knowledge representation to a renewed focus on the hybrid representation of both explicit knowledge and parametric knowledge. In this position paper, we will
tags:
  - tech/Ai
  - Tech/SemanticWeb/KG
  - tech/Ai/LLM
pdfORepub: "[[Large Language Models and Knowledge Graphs- Opportunities and Challenges.pdf]]"
---
[[Large Language Models and Knowledge Graphs- Opportunities and Challenges.pdf]]

> **Abstract:** Large Language Models (LLMs) have taken Knowledge Representation - and the world - by storm. This inflection point marks a shift from explicit knowledge representation to a renewed focus on the hybrid representation of both explicit knowledge and parametric knowledge. In this position paper, we will discuss some of the common debate points within the community on LLMs (parametric knowledge) and Knowledge Graphs (explicit knowledge) and speculate on opportunities and visions that the renewed focus brings, as well as related research topics and challenges.
## Full text (extracted from `Large Language Models and Knowledge Graphs- Opportunities and Challenges.pdf`)

*Source:* `2PDF/Large Language Models and Knowledge Graphs- Opportunities and Challenges.pdf`  
*Extracted:* 2026-08-06

```text
Large Language Models and Knowledge Graphs:
Opportunities and Challenges
Jeff Z. Pan/envel⌢pe/h⌢me
The University of Edinburgh, United Kingdom
Simon Razniewski/envel⌢pe
Bosch Center for AI, Renningen, Germany
Jan-Christoph Kalo/envel⌢pe
University of Amsterdam,
The Netherlands
Sneha Singhania/envel⌢pe
Max Planck Institute for Informatics,
Saarbrücken, Germany
Jiaoyan Chen/envel⌢pe
The University of Manchester, United Kingdom
University of Oxford, United Kingdom
Stefan Dietze/envel⌢pe
GESIS – Leibniz Institute for the Social Sciences,
Cologne, Germany
Heinrich-Heine-Universität Düsseldorf, Germany
Hajira Jabeen/envel⌢pe
GESIS – Leibniz Institute for the Social Sciences,
Cologne, Germany
Janna Omeliyanenko/envel⌢pe
University of Würzburg, Germany
Wen Zhang/envel⌢pe
Zhejiang University, China
Matteo Lissandrini/envel⌢pe
Aalborg University, Denmark
Russa Biswas/envel⌢pe
Hasso-Plattner Institute, Potsdam, Germany
Gerard de Melo/envel⌢pe
Hasso-Plattner Institute, Potsdam, Germany
Angela Bonifati/envel⌢pe
Lyon 1 University, CNRS, IUF, France
Edlira Vakaj/envel⌢pe
Birmingham City University, United Kingdom
Mauro Dragoni/envel⌢pe
Fondazione Bruno Kessler, Trento, Italy
Damien Graux/envel⌢pe
Edinburgh Research Centre, CSI,
Huawei Technologies UK, United Kingdom
Abstract
Large Language Models (LLMs) have taken Know-
ledge Representation – and the world – by storm.
This inflection point marks a shift from explicit
knowledge representation to a renewed focus on the
hybrid representation of both explicit knowledge
and parametric knowledge. In this position paper,
we will discuss some of the common debate points
within the community on LLMs (parametric know-
ledge) and Knowledge Graphs (explicit knowledge)
and speculate on opportunities and visions that the
renewed focus brings, as well as related research
topics and challenges.
2012 ACM Subject ClassificationGeneral and reference→ Surveys and overviews; Computing meth-
odologies → Knowledge representation and reasoning; Computing methodologies→ Natural language
processing
Keywords and phrasesLarge Language Models, Pre-trained Language Models, Knowledge Graphs,
Ontology, Retrieval Augmented Language Models
Digital Object Identifier10.4230/TGDK.1.1.2
Category Position
Related Version Full Version: https://arxiv.org/abs/2308.06374
Acknowledgements We would like thank Xiaoqi Han’s helpful discussion and support when finalising
the camera ready version of the paper.
Received 2023-06-26 Accepted 2023-08-31 Published 2023-12-19
Editors Aidan Hogan, Ian Horrocks, Andreas Hotho, and Lalana Kagal
Special Issue Trends in Graph Data and Knowledge
© Jeff Z. Pan, Simon Razniewski, Jan-Christoph Kalo, Sneha Singhania, Jiaoyan Chen, Stefan Dietze,
Hajira Jabeen, Janna Omeliyanenko, Wen Zhang, Matteo Lissandrini, Russa Biswas, Gerard de Melo,
Angela Bonifati, Edlira Vakaj, Mauro Dragoni, and Damien Graux;
licensed under Creative Commons License CC-BY 4.0
Transactions on Graph Data and Knowledge, Vol. 1, Issue 1, Article No. 2, pp. 2:1–2:38
Transactions on Graph Data and Knowledge
TGDK
Schloss Dagstuhl – Leibniz-Zentrum für Informatik, Dagstuhl Publishing, Germany

2:2 LLMs and KGs: Opportunities and Challenges
1 Introduction
Large Language Models (LLMs) have taken Knowledge Representation (KR) – and the world –
by storm, as they have demonstrated human-level performance on a vast spectrum of natural
language tasks [25]. Following this, people are gradually starting to accept the possibility of having
knowledge represented in the parameters by some language models, also known asparametric
knowledge, which is the information encoded from training datasets into language models’ internal
model parameters. The arrival of LLMs announces the era of Knowledge Computing, in which
the notion of reasoning within KR is broadened to many computation tasks based on various
knowledge representations.
This is a big step for the field of Knowledge Representation. For a long time, people focused
on explicit knowledge, such as those embedded in texts, sometimes also known as unstructured
data, and those in a structured form, such as in databases and knowledge graphs (KGs) [141].
Historically, for a long time, humans used texts to pass down their knowledge from one generation
to another, until around the 1960s, when researchers started to study knowledge representation
for better natural language understanding and developed early systems, such as ELIZA [207] at
the MIT. In the early 2000s, the Knowledge Representation and the Semantic Web communities
worked together to standardize the widely used knowledge representation languages, such as
RDF [139] and OWL [67], at web scale, using which the large-scale knowledge bases are then more
widely known as KGs [141], due to their helpful graph structures, enabling both logical reasoning
and graph-based learning.
This inflection point, with the arrival of LLMs, marks a paradigm shift from explicit knowledge
representation to a renewed focus on the hybrid representation, sometimes also referred to as
semi-parametric knowledge, of both explicit knowledge and parametric knowledge in neural
networks (NNs). As a popular approach for explicit knowledge representation, KGs are now widely
investigated for the combination with Transformer-based LLMs, including pre-trained masked
language models (PLMs) like BERT [47] and RoBERTa [122], and more recent generative LLMs
like the GPT series [24] and LLaMA [191]. Some works use LLMs to augment KGs for, e.g.,
knowledge extraction, KG construction, and refinement, while others use KGs to augment LLMs
for, e.g., training and prompt learning, or knowledge augmentation. In this paper, considering
both directions, LLMs for KGs and KGs for LLMs, we present a better understanding of the shift
from explicit knowledge representation to a renewed focus on the hybrid representation of both
explicit knowledge and parametric knowledge.
There has been some related work on LLMs and KGs. A related survey paper [235] presents a
comprehensive review of using LLMs for KG construction and reasoning, while our work provides
a more in-depth view of the inflection point, considering not only relational KGs but also KGs
with ontologies as schemas, as well as other dimensions of structured knowledge, including tabular
data [210] and numerical values [140]. Other works on the intersection of LLMs and KGs have a
minor overlap with the topics covered in our paper; e.g., on studies using LLMs as KGs [5], on
using KGs to augment LLMs [213], or on comparing GPT-4 with ChatGPT and SOTA fine-tuning
methods on three knowledge-related tasks – entity, relation and event extraction, link prediction,
and KG question answering [235]. Overall, none of these papers look into the implications of
the inflection point with concrete applications. To this end, this paper summarizes the common
debate points within the community, introduces the state-of-the-art for a comprehensive set of
topics where KGs and LLMs are integrated, and further presents opportunities and challenges.

Jeff Z. Pan et al. 2:3
2 Terminology
Language models. The term “(large) language model (LLM)” covers quite a set of model families.
Although the term already existed before the rise of neural models, it arguably rose to prominence
with the publication of the BERT architecture [47], a Transformer-based neural architecture. The
BERT model was typically used with parameters pre-trained on a large text corpus and fine-tuned
on application specific data. BERT-style (masked) architectures have become a building block of
many language-related tasks, where they can be used, for instance, for obtaining latent semantic
representations of words or phrases, and are frequently employed in classification, similarity
estimation, or retrieval tasks.
A second, slightly more recent paradigm of language models are autoregressive (generative)
architectures like the GPT family. These models are suited for the generation of text from given
prefixes, and, in contrast to BERT models, can (in principle) directly be used in downstream use
cases. At the same time, they represent less mature architecture, with media headlines taken by
closed commercial models like ChatGPT and GPT-4 [137], and open models like LLaMA [191],
Vicuna [37], or Falcon [149] only recently entering the stage. Although fine-tuning is possible for
some of them, autoregressive models are often used without adapting their parameters, e.g., via
zero-shot or few-shot text-based prompts.
Where the distinction is important, we will explicitly state to which model family and prompt
style we refer.
Explicit knowledge. Explicit knowledge includes both unstructured knowledge, such as text,
images and videos, and structured knowledge, also referred to as symbolic knowledge, which is
knowledge codified in a logical representation, such as knowledge graphs and databases. This has
been the standard in the AI and KR communities for long and enables an intuitive understanding
of assertions. Nevertheless, it has been known for long that not all knowledge is suited for explicit
representations, and certain types of knowledge remain typically implicit.
Parametric knowledge. This is a kind of implicit knowledge. We use the term “parametric
knowledge” to refer to the information encoded from training datasets into language models’
internal model parameters. Most importantly, these parameters describe the weights of the neural
network and thus consist of a set of numeric values.
Some parametric knowledge cannot be easily translated into symbolic knowledge, for instance,
LLMs typically have solid “knowledge” on whether a textual phrase has positive sentiment or
not, yet there is typically no lossless conversion into a symbolic formula. At the other end of the
spectrum is the parametric knowledge that has been shown possible to be extracted into a crisp
symbolic form, for example, “Who was the first person on the moon?”.
As we will show later, parametric knowledge of the latter kind is important for many steps
in KG construction and consolidation pipelines, while parametric knowledge of the former kind
offers a direct supplement or alternative to existing KGs.
3 Common Debate Points within the Community
The usage of parametric and explicit knowledge together is a topic of debate in the Knowledge
Computing community, with proponents and skeptics offering different perspectives. Below are
some summaries of common points of contention.
TGDK

2:4 LLMs and KGs: Opportunities and Challenges
Knowledge Representation and Reasoning. KGs offer a structured representation of knowledge
with explicit relationships, enabling reasoning and inference [128]. Critics argue that parametric
knowledge in NNs and LLMs relies on statistical patterns rather than true understanding and
reasoning [14]. Proponents of LLMs like ChatGPT highlight their ability to generalize from
large-scale text corpora, capturing a range of information, and excellent language understanding
capabilities. On the one hand, LLMs could generate plausible but incorrect or nonsensical
responses, such as hallucinations, due to a lack of explicit knowledge representation [163, 223].
There are also doubts on whether LLMs have the ability to learn directional entailments [114] or
infer subsumption between concepts [75]. On the other hand, KGs can be costly to build. While
LLMs can be expensive to train too, they can be readily usable to support many downstream
applications, bringing AI from the backstage to center stage. To sum up, in comparison to the
classic trade-off between expressiveness and decidability in knowledge representation, here KGs
and LLMs have the trade-off between precision and recall considering using explicit and parametric
knowledge in knowledge computing tasks.
High Precision Methods. The success of KGs can largely be attributed to their ability to
provide factual information about entities with high accuracy. For instance, YAGO [180] asserts
an accuracy rate exceeding 95%. Similarly, Google necessitates high accuracy in its KG for
operational use, e.g., the semi-automatic construction method of Knowledge Vault was not utilized
in production, partly due to its inability to reach the desired 99% accuracy in their benchmark [206].
Along this line of thought, many LLM-based methodologies for KG completion fail to reach these
high-performance levels, as exemplified by the performance of BERT in [115, 193], and GPT-3,
equipped with hundreds of billions of parameters [4]. This calls for novel high precision methods
for KG construction based on LLMs.
Numerical Values. It is widely recognized that LLMs grapple with handling numerical values.
Even straightforward arithmetic tasks can be a struggle for LMs, as highlighted in a study by
Big-bench [179]. This shortcoming also extends to KG completion tasks [95]. Multiple LLMs have
been evaluated on their ability to complete KGs using numerical facts from Wikidata [196], such
as individuals’ birth and death years. However, none of the tested models accurately predicted
even a single year. This raises questions about the capability of current LLMs to correctly
memorize numbers during pre-training in a way that enables them for subsequent use in KG
completion. While LLMs like PaLM [41] demonstrate some proficiency in dealing with numbers,
more commonly used smaller models seem ill-equipped for this task. The complexity escalates
when considering the intricacies of metrics and diverse numbering formats and types. Currently,
modifying LLMs to handle numerical values remains unresolved, making their utilization for
numerical KG completion seem far from practical.
Long-tail Knowledge. One of the key research questions on LLMs for the Knowledge Computing
community (and beyond) is how much knowledge LLMs remember [125]. Investigations indicate
that LLMs’ performance significantly deteriorates when dealing with random Wikidata facts,
specifically those associated with long-tail entities, in comparison to popular entities, as evidenced
in the PopQA dataset [125] and other datasets [152, 193]. This effect can be traced back to a
causal relationship between the frequency of an entity’s appearance in the pre-training corpus
and the LLMs’ capacity for memorization [53]. Even sizable LLMs face difficulties when trying to
retain information about long-tail entities [97]. KGs inherently present an advantage over LLMs
through their provision of knowledge about long-tail entities [95, 193] and thus can further help
improve the recall for Knowledge Computing tasks.

Jeff Z. Pan et al. 2:5
Bias, Fairness and Beyond. Critics argue that LLMs can perpetuate and amplify biases present
in the training data, leading to biased outputs. LLMs may generate biased or prejudiced responses
if the training data contains stereotypes or discriminatory information [131, 108]. On the other
hand, proponents argue that bias is not inherent to LLMs but reflects societal biases embedded in
the data. They emphasize the importance of addressing bias in the training data and developing
mitigation techniques [167, 154, 161]. A survey [17] argued that “bias” in Natural Language
Processing (NLP) systems took various conceptualizations without being critically engaged by
practitioners. KGs are also used in a plethora of downstream tasks, and social biases engraved
in KG embeddings get propagated [68, 104]. Specifically, ontology creation, which generally
comprises manual rules factored by opinions, motivations, and personal choices, is a source of
bias [89, 51]. Also, automated pipelines for KG construction exhibit gender bias [127]. There are
other similar concerns of LLMs beyond bias and fairness, including (but not limited to) copyright
violation and misinformation. In general, due to the implicit nature of parametric knowledge, it is
less straightforward to forget such toxic information from LLMs, compared to explicit knowledge.
Explainability and Interpretability. KGs are often preferred in scenarios where explainability
and interpretability are crucial [31], as they explicitly represent relationships between entities and
provide a structured knowledge representation. Skeptics of LLMs argue that these models lack
transparency and interpretability, making it difficult to understand how they arrive at their answers
or recommendations. Proponents of LLMs acknowledge the challenge of explainability but argue
that recent research efforts [8, 88] are improving LLM’s interpretability through techniques like
attention mechanisms, model introspection. Some also argue that Chain-of-Thoughts (CoT) [204]
can also improve the explainability of LLMs, although question decomposition and precisely
answering sub-questions with LLMs are still far from being solved. Attribution evaluation and
augmentation of LLMs with e.g., source paragraphs and sentences is another recent research topic
for improving their explainability in question answering [18].
4 Opportunities and Visions
One of the key questions this paper needs to answer is, now with the emergence of parametric
knowledge, what new opportunities do we have? Here are some of our thoughts on such new
opportunities with the arrival of parametric knowledge and its potential integration with explicit
knowledge.
1. Instant access to huge text corpora:As mentioned in the Introduction, for a long time,
human beings passed down their knowledge in texts. Thus, a lot of knowledge these days
are in textual form. Using LLMs gives access to extremely large text corpora at high speed,
and recently even on consumer hardware [79]. This allows AI developers to avoid getting
bogged down in previously critical challenges around data gathering, preparation, storage,
and querying at scale. It also helps to reduce previously critical dependencies on the field of
information retrieval.
2. Richer knowledge for many subtasks:Although the most prominent capabilities of
LLMs, question answering and dialogue, are still under critical scrutiny, it should not be
overlooked that LLMs have significantly advanced and simplified many traditional tasks of
the knowledge engineering pipeline. Out-of-the-box, with fine-tuning on a few examples, or
via few-shot prompting, LLMs have advanced many tasks such as dependency and structured
parsing, entity recognition, and relation extraction. And just as errors propagate along a
pipeline, so do improvements, thus enabling KG construction at unprecedented scale and
quality. Furthermore, LLMs are readily usable for many downstream tasks beyond knowledge
TGDK

2:6 LLMs and KGs: Opportunities and Challenges
engineering. By injecting explicit, and in particular structured, knowledge into LLMs, such as
through retrieval augmented methods, one can make explicit knowledge more readily usable
for such a wide range of downstream tasks, further realizing the vision of ‘Knowledge is power’.
3. Even more advanced language understanding:LLMs alone already significantly advanced
the “understanding” of natural language, as evidenced by tasks like textual entailment,
summarization, paraphrase detection and generation, etc. These capabilities are critical to
making knowledge engineering robust to linguistic variance, typographic errors, redundancy,
and other features of human-written, web-scraped, and other noisy forms of text. Now with
potential novel approaches to combining parametric knowledge with explicit knowledge, it is
possible to have even more advanced language understanding, not only for textual entailments,
but also for other NLP tasks, such as summarization and consistent generation.
4. Compression entails consolidation:An important step in traditional knowledge engineering
is the consolidation and aggregation of conflicting and concurring pieces of information,
requiring often elaborate methods for consolidating observations from sentences, patterns, and
constraints [173]. In LLM training, an aggregation occurs automatically. Although this step is
not entirely understood, it brings the potential for outsourcing a major challenge in knowledge
engineering.
With the above new opportunities brought by the combination of parametric and explicit knowledge,
our vision is two-folded:
In Explicit-Knowledge-First use cases, our vision is thatLLMs will enable, advance, and
simplify crucial steps in the knowledge engineering pipeline so much as to enable KGs at
unprecedented scale, quality, and utility.
In Parametric-Knowledge-First use cases, our vision is thatKGs will improve, ground,
and verify LLM generations so as to significantly increase reliability and trust in LLM usage.
Both visions are neither alternatives, nor does one build upon the other. Instead, we believe that
classes of use cases will continue to exist side-by-side, some of which favor Explicit-Knowledge-First
(scrutable) approaches, some of which favor Parametric-Knowledge-First (blackbox) approaches,
with either of these having significant potential for benefiting from synergies of the two directions.
5 Key Research Topics and Related Challenges
With the opportunities and visions related to the availability of both parametric and explicit
knowledge in place, in this section, we categorize, summarize, and present the recent developments
in using LLMs and KGs under five different themes:
1. LLMs for KGs: Knowledge Extraction and Canonicalisation
2. LLMs for KGs: KG Construction
3. LLMs for KGs: Ontological Schema Construction
4. KGs for LLMs: Training and Augmenting LLMs
Figure 1 provides an overview. In Section 5.1, we start with the traditional KG construction from
text and tables, then show in Sections 5.2 and 5.3 how assertions and ontological information can
be extracted from LLMs. We then reverse perspective, and discuss in 5.4 how KGs can help and
enhance LLMs in training and deployment.
5.1 LLMs for KGs: Knowledge Extraction and Canonicalisation
KG construction is a complex task that demands collecting and integrating information from a wide
array of sources, encompassing structured, semi-structured, and unstructured data. Traditional
methods often rely on specific modules designed to process each data type in isolation and struggle
when the content is diverse and heterogeneous in structure. However, LLMs are powerful NLP

Jeff Z. Pan et al. 2:7
KG ConstructionLLM-based KG 
Techniques
Knowledge Extraction 
and Canonicalisation
Entity Resolution and Matching
Knowledge Extraction from Tabular Data
Knowledge Extraction from Text
Triple Extraction from LLMs 
Link Prediction
Ontological Schema 
Construction
Constraint and rule mining from KGs
Ontology Refinement
Ontology Alignment
KG-based LLM 
Techniques KGs for Prompt Construction
Retrieval Augmented Methods
KGs for (Pre-)training Language Models
Figure 1A Framework of Key Research Topics and Related Challenges.
models trained on a broad spectrum of information sources, making them well-suited for knowledge
extraction tasks. This section presents work that uses LLMs for knowledge extraction from various
sources.
5.1.1 Entity Resolution and Matching
Entity resolution (also known as entity matching, entity linking or entity alignment) is the process
of linking pieces of information occurring in multiple heterogeneous datasets and referring to the
same world entity [55, 59, 144]. Past research has focused on developing the methodologies and
similarity measures among entities represented by flat structured data as well as semi-structured
data. Recent benchmarks, among which a recent one [147], have been proposed to compare
existing matching systems (including relational ones) on their accuracy, amount of corner cases
and robustness to unseen matching pairs. A similar benchmark and survey tailored for knowledge
graph entity alignment [225] focuses on the problem of alignment entities in different knowledge
graphs using embedding-based techniques. One of the findings of the comparative analysis of
existing systems is that semantic information (e.g. attribute triples and relation predicates) allow
to achieve better matching accuracy.
Embedding-based entity alignment methods for KGs reduces the symbolic similarities between
graph entities to a vector space in order to flatten the heterogeneity of graph components and
facilitate reasoning [182]. Specifically, a total of 23 representative embedding alignment approaches
are cross-compared in terms of performance but also are shown to require significant supervision
in the labeling phase. Therefore, unsupervised methods and methods that cope with large-scale
KGs are highly desirable in future research investigations.
CG-MuAlign [234] employs Graph Neural Networks (GNNs) to perform multi-type entity
alignment, leverages the neighborhood information and generalizes to unlabeled types, and
REA [148] which tackles the multilingual entity alignment problem by combining adversarial
training with GNNs to cope with the problem of noisy labeled data provided as input.
TGDK

2:8 LLMs and KGs: Opportunities and Challenges
LLMs are used in entity resolution and linking for KGs in multiple ways [7].
We envision the following important research challenges on the interplay between entity
resolution and linking and LLMs.
Generation of labeled training data, which is typically a resource-intensive and time-
consuming step, hindering the performance of entity alignment for KGs [94].
Generation of corpora of entity matching rules, which will allow to increase the amount
of rules available for these tasks on real-world knowledge graphs.
Generative entity linking, is about using a generative language model performing entity
linking as a sequence-to-sequence task [44, 93].
Similarly to how [170] employs Generative Adversarial Networks (GANs) to reduce the effort
of labeling data, we argue that LLMs can provide labeled samples of KGs and control the
performances of the aforementioned embedding-based approaches. Also, LLMs can help build
robust and trustworthy corpora of entity matching rules, modulo the fact that a declarative
formalism with a logical languageL is defined in the graph setting. Training data for this
logical language should be provided as input to LLMs, similarly to SQL statements that are
readily available for consumption in text corpora. However, prompt engineering is needed in
order to produce meaningful rule corpora for real-world large-scale KGs, such as DBpedia [9] and
Wikidata [196]. Entity matching rule logs can be envisioned for these real-world large-scale KGs
in a similar fashion as query logs for these KGs [19, 20].
Another interesting line of research work revolves around the alignment of factoid questions
for building robust question answering (QA) systems. Existing approaches focus on the use of
biencoders to efficiently perform both entity mention detection and entity linking in only one
pass [110]. Matching of questions and predicate sequences on a knowledge base using both entity
linking and deep convolutional neural networks has been investigated in prior work [218].
Other interesting directions to pursue for future developments leading to intertwining symbolic
AI and statistical AI are as follows:
Combination of entity linking approaches and embedding-based approaches with
LLMs, which can lead to better integration of LLMs with knowledge reasoning and question
answering [81].
Marrying accuracy and interpretability, which will leverage the power of LLMs to
generate graph data and rules and improve the accuracy of the entity linking processes but
also enhance the interpretability of the processes.
5.1.2 Knowledge Extraction from Tabular Data
Extracting knowledge from tabular data like databases, Web tables and CSV files is a common
way for KG construction. For tables whose semantics (meta information) are already known,
heuristic rules can be defined and used to transform their data into KG facts. However, real-world
tables often have unclear semantics with important meta information, such as table name and
column header, not clearly defined. Meanwhile, the original data usually need to be retrieved,
explored, integrated and curated, before expected knowledge can be extracted. In recent years,
Transformer-based LMs have been investigated for processing tables, especially their textual
contents. They can be applied to table vector representation as a foundation of other prediction
tasks [194]. TURL [46] is a typical method of table representation learning that uses BERT [47]
and has been applied in several tasks such as cell filling, column type annotation, and relation
extraction. Similarly, RPT [188] uses BERT and GPT to pre-train a table representation model.
Starmie [56] transforms columns into sequences using a template and fine-tunes BERT with a
contrast learning framework using unionable and not unionable column pairs as samples.

Jeff Z. Pan et al. 2:9
Among all the table processing tasks, semantic table annotation which matches table data to
KG components (e.g., table column to KG class, table cell to KG entity, inter-column relationship
to KG property) can be directly applied to extract knowledge for KG construction and population
[121, 92]. There have been several attempts that use LLMs for these tasks. Doduo [181] serializes
a table into a sequence of tokens and trains BERT for predicting column types and inter-column
relationships. Korini et al. [103] prompts ChatGPT to annotate semantic column types. When
task-specific samples for demonstration are minimal or absent, ChatGPT achieves a similar
performance as the RoBERTa model. Although some attention has been given to utilizing LLMs
for tabular data processing and KG construction, there is still much room for investigation.
Challenge and Opportunities.
Transforming table contents into sequences:A table or a table element with its structured
context needs to be transformed into a sequence before it can be fed into LLMs. Different
transformation methods are required for different LLM utilization scenarios, such as fine-tuning
LLMs, LLM inference with prompts, and instruction tuning of LLMs.
Representing and utilizing non-textual tabular data:A table often contains not only
long and short text, but also data of other types, like numbers and dates. There are still few
works that consider these data.
Extracting tabular knowledge:LLMs are mostly applied to process and understand tables
but rarely applied to the final step of knowledge extraction. OntoGPT [27], which extracts
instances from texts to populate an ontology using ChatGPT is known, but there are no
counterparts for tables. Beyond instances, extracting relational facts is more challenging.
5.1.3 Knowledge Extraction from Text
Knowledge extraction from text generally entails automatic extraction of entities and associated
relations, with traditional pipelines processing vast amounts of sentences and documents. This
process enables the transformation of raw text into actionable knowledge, facilitating various
applications such as information retrieval, recommendation systems, and KG construction. The
language understanding capabilities of LLMs have enhanced this process.
For example,
(1) Named Entity Recognition (NER) and Entity Linking, as mentioned in Section 5.1.1, involve
identifying and categorizing named entities (such as persons, organizations, and locations) in
text and linking (more in Section 5.2.1) them to KGs.
(2) Relation extraction focuses on identifying and classifying relationships between entities, with
LLMs that leverage zero-shot and few-shot in-context learning techniques [205, 111].
(3) Event extraction aims to detect and classify events mentioned in the text, including their
participants and attributes [197, 224].
(4) Semantic Role Labeling (SRL) involves identifying the roles played by entities in a sentence,
such as the subject, object and predicate [172, 230].
These approaches allow LLMs to extract information from text without needing a large amount
of explicit training on specific domains, thereby improving their versatility and adaptability [44].
Moreover, LLMs have demonstrated proficiency in extracting knowledge from languages other than
English, including low-resource languages, paving the way for cross-lingual knowledge extraction
and enabling the utilization of LLMs in diverse linguistic contexts [106].
Furthermore, prompting LLMs has introduced new paradigms and possibilities in the field
of NLP. LLMs can generate high-quality synthetic data, which can then be used to fine-tune
smaller task-specific models. This approach, known as synthetic data generation, addresses the
TGDK

2:10 LLMs and KGs: Opportunities and Challenges
challenge of limited training data availability and enhances the performance of models [94, 189].
Additionally, instruction tuning has emerged as a powerful technique where LLMs are trained on
datasets described by explicit instructions, enabling more precise control and customization of
their behavior for specific tasks [205, 201]. Also, for constructing domain-specific KGs, the stakes
are higher, and hence scrutinizing the generated text (by experts) is necessary. However, it is still
a step forward since human annotation is less expensive than human text generation.
Apart from the obvious substantial computational resource requirements for training and
utilizing these LLM, there are various challenges, including the ones presented in Section 3.
Challenge and Opportunities.
Efficient extraction from very long documents.Current LLMs are incapable of processing
very long documents like novels in one shot. In this regard, modeling long-range dependencies
and performing corpus-level information extraction can be further improved.
High-coverage information extraction. Almost all extraction pipelines focus on high
precision. However, high recall is ignored or under-explored [176]. Building knowledge
extractors with high precision and high recall will result in a great leap toward building lifelong
information extractors.
5.2 LLMs for KGs: Knowledge Graph Construction
We highlight the important role that LLMs play in improving KG construction, focusing on current
trends, issues, and unanswered questions in this field. We start by discussing link prediction, which
is a way to generate new facts given an existing KG. Next, we look at inductive link prediction,
a method that predicts triples for unseen relationships. Our focus then shifts to a more recent
method where triples are directly extracted from the parametric knowledge of an LLM.
As a conclusion of this section, we discuss the challenges of LLM-based methods for KG
construction. These involve issues with long-tail entities, numerical values, and also the precision
of these methods.
5.2.1 Link Prediction
Link prediction is about predicting a missing element of a triple given the other two elements. It
includes head entity prediction(?, r, t), relation prediction(h, ?, t), and tail prediction(h, r,?).
KG link prediction methods have mostly been studied for static snapshots of a KG. Many
approaches, in fact, assume a training phase in which the current state of the KG is used
to learn embeddings and other model parameters. Subsequently, many such models can only
operate on entities for which an embedding was learned in the training phase. This leaves them
incapable of predicting links for any previously unseen entities, such as newly added people or
products. Inductive link prediction (ILP), in contrast, focuses on techniques that can predict
links to new entities not originally contained in a KG. Furthermore, existing KG embedding-
based KG completion approaches frequently fail to leverage textual information and other literal
information [65].
To overcome these challenges, current research focuses on incorporating textual information
available in the KGs to improve the KG embeddings, boost performance in downstream tasks,
and support ILP. The latent representation is learned from textual information using a variety of
encoding models such as linear models, convolutional models, recurrent neural models, and LLMs
and studied in [123, 142]. In this work, we focus only on LLM-based methods.
The LLM encoder BERT [47] is used in Pretrain-KGE [227] to generate initial entity embeddings
from entity descriptions and relations. These embeddings are then fed into KG embedding
models to generate final embeddings. MADLINK [15] uses SBERT to generate embeddings from

Jeff Z. Pan et al. 2:11
entity descriptions, together with the entity embeddings obtained from structural information.
KEPLER [202] offers a unified approach for KG embedding and pre-trained language representation,
embedding text-enhanced knowledge and factual knowledge into LLMs. Nayyeri et al. [132] use
LLMs to produce representations at word, sentence, and document levels, merging them with
graph structure embeddings. Huang et al. [84] propose a model that combines LLMs with other
modalities, such as vision, to generate a multi-model embedding space. CoDEx [3] uses a novel
loss function driven by LLMs that helps KG embedding models estimate the likelihood of triples
based on textual information. While these approaches can leverage the structural information
contained in the graph, KG embeddings can not be directly used to predict unknown entities in
the ILP setting. To still predict entities within ILP, existing works that combine text embeddings
and traditional KG embeddings use only the text embeddings in the ILP setting [124] or apply
similarity based heuristics to generate KG embeddings for unseen entities [198].
Instead of considering the graph structure, another line of research directly leverages LLMs for
KG Completion. For example, KG-BERT [216] represents a triple as an ordered sequence of head
text, including surface form, descriptions, and attributes, relation text, tail text separated with
special tokens. KG-BERT [216] optimizes the BERT model on KGs, followed by KG-GPT2 [16]
that fine-tunes the GPT-2 model. MTL-KGC [101] enhances the effectiveness of KG-BERT by
combining prediction and relevance ranking tasks. PKGC evaluates triple validity by translating
it into natural language sentences, while LLMs process these sentences for binary classification.
Masked Language Models were introduced to encode KG text, with MEMKGC [38] predicting
masked entities using the MEM classification model. Open world KGC [39] expands MEMKGC
with modules Entity Description Prediction (EDP) and Incomplete Triple Prediction (ITP),
focusing on predicting entities with given textual descriptions. StAR [199] uses Siamese-style
textual encoders for text and a scoring module, while SimKGC [200] leverages a Siamese textual
encoder. LP-BERT [112] is a hybrid KG completion method that combines MLM encoding for
pre-training with LLM and separated encoding for fine-tuning, using a contrastive learning strategy.
Also, LLMs such as GPT-3 and GPT-4 have the in-context learning capability which could adapt
to new tasks through careful prompt design without fine-tuning the model parameters. Since LLMs
are directly capable of predicting entities that are not yet contained in the KG, many works using
direct LLM approaches also evaluate their models in the ILP setting [38, 39, 43, 199, 200, 202, 222].
Beyond the described approaches that construct and leverage embeddings for link prediction,
LLMs may also be directly used in a prompting setting to find suitable links between entities,
with existing methods described in detail in the following Section 5.2.2. As with the previous
approaches that purely use LLMs, prompt-based approaches are directly applicable for ILP and
are commonly evaluated in this setting [21, 90, 152, 174, 231]. LLMs make it significantly easier
to jointly utilize structural and text information for link prediction, while there are still challenges.
Challenge and Opportunities.
The generative language model which uses a decoder-only or encoder-decoder architecture
cannot ensure that the generated result is already included in the KG. Also, one entity may
have multiple natural language names. Thus it is hard to judge the correctness of the generated
results from LLMs.
Current link prediction models are mostly evaluated on ranking metrics, such as Hit@k and
Mean Reciprocal Rank, which requires methods to give a ranked list of candidates. Considering
that the number of candidate entities might be huge (e.g., over ten thousand), scoring each
candidate entity in inference requires many model predictions which may be problematic for
LLMs due to their large parameter size and high computational cost.
TGDK

2:12 LLMs and KGs: Opportunities and Challenges
The key research question of link prediction is how well a method could learn to infer new
triples based on existing ones. LLMs are trained based on a massive corpus that might overlap
with KGs such as Wikidata [196]. Thus it is not easy to distinguish whether the LLM completes
the prediction by utilizing its memory or reasoning over existing facts.
LLMs provide several benefits for ILP as demonstrated by the many existing approaches,
but their application also has certain drawbacks. Since ILP entities may occur that are not
contained within the underlying KG, the task is inherently reliant on auxiliary information.
When leveraging LLMs for ILP, many studies focus on improving the extraction of knowledge
from LLMs through prompt engineering, which is, by itself, a current popular research area
that may directly benefit the domain.
While prompting provides promising results, it requires well-designed strategies for predicting
multi-token entities and out-of-vocabulary tokens. Further, if required knowledge is not
captured by the LLM, e.g., when querying novel concepts that emerged after LLM pre-training,
schemes to incorporate further knowledge into the LLM are required. Meanwhile, as feature
selection, finding a suitable prompt also needs much searching with many experiments, which
is costly especially for those recent commercial LLMs like GPT-4.
Alternative methods rely on available high-quality textual descriptions of unknown entities.
These methods generally inherit the limitations of classical link prediction, in that they require
one-vs-all comparisons against all entity candidates during inference, which may become
computationally prohibitive for large KGs [199, 200]. While there are already approaches that
address this problem by applying efficient search heuristics, additional structural information,
and pre-computation [44, 153, 199, 200], they involve additional memory overhead. As such,
efficient strategies for obtaining predictions may provide a promising research direction.
Further, the combination of these methods with classical link prediction models has already
shown strong performance and is a promising trend followed by increasing numbers of works
that further explore the incorporation of structural information into LLM-driven approaches.
Though challenges exist, opportunities lie in designing efficient and effective link prediction
methods combining LLMs preserving the efficiency of traditional methods and robustness of
language models.
5.2.2 LLMs for KGs: Triple Extraction from LLMs
Traditionally, retrieval and reasoning of relational knowledge have both relied on symbolic know-
ledge bases [60], that often are constructed using supervised extraction techniques applied to
unstructured corpora, e.g. Web archives [220, 190]. More recently, self-supervised LLMs have been
investigated for their ability to directly retrieve relational knowledge [233] from their parameters,
e.g. through question answering, prompting through the use of cloze-style questions [76, 166]
or statement scoring [183]. In this context, the ability of LLMs to retrieve, infer and generalize
relational knowledge is seen as a crucial indicator of their capacity to understand and interpret
natural language. Even though a range of terms are used in that context, e.g. fact or knowledge
retrieval as well as knowledge inference, we refer to the task of accessing relational knowledge
from LLM parameters asknowledge retrieval.
Benchmarks and Baselines. LAMA is the first benchmark dataset to evaluate knowledge retrieval
in LLMs [152]. Related works show that knowledge retrieval through prompts is inconsistent
with regard to paraphrasing [54, 76], with some types of information guiding LLMs towards more
correct answers [26, 151, 35], while others are harmful to their performance [143, 100]. LLMs
struggle to retrieve knowledge from low-frequency phenomena [162] and [86] argue that LLMs fail
to express large varieties of knowledge when prompted in a zero-shot manner.

Jeff Z. Pan et al. 2:13
Zhong et al. [231] propose that the models’ accuracy may originate from memorizing training
data, not actually inferring knowledge. Similar to LAMA, the experiments on a more recent
probing work KAMEL [95] confirm that LLMs are still far from the knowledge access capabilities
of symbolic knowledge bases. The Knowledge Memorization, Identification and Reasoning test
work KMIR [62] reveals that while LLMs struggle to robustly recall facts, their capacity to retain
information is determined more by the number of parameters than the training methods, and
while model compression can help preserve the memorization performance, it reduces the ability
to identify and reason about the information in LLMs from transformer-based language models.
Linzbach et al. [116] also present similar findings. LLMs are known to struggle with more complex
reasoning tasks [83, 75]. Branco et al. [22] explore generalizability of common-sense reasoning
capabilities and the impact of shortcuts in training data.
Biases in Triple Extraction Evaluation.LLMs may exhibit various types of biases; representation
of the majority viewpoint being a common issue due to distributions prevalent within pretraining
data [13], neglecting disagreements among multiple viewpoints (e.g. by majority voting) [42].
Prior works investigate individual factors (such as frequency) or LLM biases in other tasks [126],
as well as knowledge retrieval [231].
With respect to the interpretation, reliability and generalizability of knowledge retrieval, several
studies [22, 26] investigate whether LLMs actually learn transferable generalizations or only exploit
incidental shortcuts in the data. [26] explore biases in three different knowledge retrieval paradigms,
namely prompt-based retrieval, case-based analogy, context-based inference, finding that decent
performance of existing knowledge retrieval baselines tends to be driven by biased prompts that
overfit to artifacts in the data, guide the LLM towards correct entity types or unintentionally leak
correct answers or additional constraints applicable to the correct answer. In a similar context, [50]
discuss the shortcut learning behavior arising due to skewed training datasets, the model, or the
fine-tuning process. [169] demonstrate an intriguing similarity between human cognitive biases
and those exhibited by LLMs. Using insights from psychology, they analyze the learning and
decision-making processes of black-box models to reveal their biases towards right-and-wrong
for decision-making. Therefore, rigorous assessment of existing benchmark datasets is necessary
for generalizable insights about knowledge retrieval and inference performance, and to facilitate
efficient, unbiased knowledge retrieval from LLMs.
Prompt Engineering for Triple Extraction.Cao et al. [26] propose three paradigms for factual
knowledge extraction from LLMs: prompt-based, case-based, and context-based. Results suggest
the prompt-based retrieval is biased towards prompt structure. Prompt engineering [10] aims to
create prompts that efficiently elicit desired responses from LLMs for a specific task. However,
a limited number of manually created prompts only reveal a portion of the model’s encoded
knowledge [90], as the response can be influenced by the phrasing of the question. Thus, prompt
engineering is a crucial part of knowledge retrieval from LLMs. LPAQA [90] uses an automated
mining-based and paraphrasing-based method to generate diverse high-quality prompts, as well as
ensemble methods to combine answers from different prompts. Automatic Prompt Engineer [233]
uses LLM models like InstructGPT [138] and instruction induction [78] to generate instruction
candidates which are then improved by proposing semantically similar instruction variants to
achieve human-level performance. Zhou et al. [233] investigate the ability of LLMs, such as
GPT-3, to generate high-quality prompts for a variety of tasks.Initial experiments on the role of
syntax in knowledge retrieval [116] find a strong dependency on prompt structure and knowledge
retrieval performance.
TGDK

2:14 LLMs and KGs: Opportunities and Challenges
To summarize, prior works have shown that relational knowledge is captured by LLMs to
a certain extent. However, there is still insufficient understanding of how performance differs
across different kinds of knowledge or relations, for instance, commonsense knowledge compared
to entity-centric encyclopedic facts or transversal versus hierarchical relations. In addition, several
studies raise questions about LLMs capacity to infer knowledge beyond already-seen statements.
Challenges and Opportunities.
Entity Disambiguation:Entity disambiguation is essential for KG construction to ensure
unique identification of entities and to maintain consistency across the graph. However, when
extracting facts from LLMs, entity disambiguation presents several challenges, since LLMs only
operate on word token level. Hence, polysemy and homonymy make it difficult to determine
the correct entity when a term has multiple meanings or is spelled the same as others but has
different meanings. Also, the need to resolve co-references, where the same entity is mentioned
in various ways within a text, further complicates the process. Moreover, the same piece of
text can refer to different entities depending on the context, making it a significant challenge
to correctly identify and classify the entities. Entities that were not present in the training
data or are less common in general can be particularly hard to disambiguate. This can be a
frequent issue with newer, less well-known, or very domain-specific entities. These complexities
lead to major challenges that need to be addressed: enhancing disambiguation techniques to
better handle long-tail entities; developing methods to better understand and utilize context
in entity disambiguation; and improving co-reference resolution in such a way that it can be
effectively incorporated into KG construction.
Long-tail Entities:Existing LLMs still manifest a low level of precision on long-tail entities.
Models may begin to generate incorrect information when they fail to memorize the right
facts. The answers provided by these models often lack consistency. Incorrect correlations
drawn from the pre-training corpus can lead to various biases in KG completion. Whether
retrieval-augmented models serve as a viable solution to this problem remains uncertain, as
does the potential necessity to adapt pre-training and fine-tuning processes to enhance model
robustness in handling long-tail entities.
High-Precision: LLMsfacechallengesinachievinghigh-precisionpredictionswhenperforming
knowledge retrieval [193]. A potential strategy to derive high-precision KGs from LLMs is to
focus on model calibration. However, there are pressing challenges that remain unsolved. How
can LLM training be adapted to prioritize high-precision learning? Can LLMs be used for
validation purposes? These questions form the crux of the ongoing exploration in this field.
Provenance: Extracting factual knowledge directly from LLMs does not provide proven-
ance, the origin and credibility of the information, which presents multiple issues. Without
provenance, verifying the accuracy of information becomes challenging, potentially leading to
the spread of misinformation. Additionally, bias detection is hindered, as the lack of source
information makes it difficult to account for potential biases in the data used for training.
Provenance also provides critical context, without which information can be misunderstood
or misapplied. Lastly, the absence of source information compromises model transparency,
making it hard to evaluate the accountability of the LLMs.
5.3 LLMs for KGs: Ontological Schema Construction
A KG is often equipped with an ontological schema (including rules, constraints, and ontologies)
for ensuring quality, enabling easier knowledge access, and supporting reasoning. At the same
time, an independent ontology, which usually represents conceptual knowledge sometimes with

Jeff Z. Pan et al. 2:15
logics, can also be regarded as a KG. In this part, we describe the interaction between LLMs
and approaches to learn ontological schemas as well techniques that can exploit LLMs to manage
ontologies and rules.
5.3.1 Constraint and Rule Mining from KGs
The existing KGs are mostly obtained from large-scale data extraction pipelines, which are
notoriously brittle and can introduce errors and inconsistencies in these graphs [48, 158]. Moreover,
a KG isnever considered completesince the closed world assumption does not hold [48, 146], i.e.,
it is not possible to conclude that a missing fact is falseunless it contradicts another existing fact.
Instead, we usually consider that in a KG it holds the open-world assumption, that is a missing
fact is simply considered asunknown.
Practical applications impose high demands in terms of (semi-)automatic methods for data
quality assessment and validation [102, 157, 2]. Since KGs contain huge amounts of data, it is
not feasible to manually inspect and correct their errors. Therefore, a common approach is to
instantiate rules and constraints that can be automatically enforced. These constraints express
dependencies and conditions that the KG needs to satisfy at all times and that should not be
violated by the introduction of new facts or their deletion. In KGs, rules and constraints can
take the form of Graph Functional Dependencies [57], declarative first-order logic rules [61], entire
ontologies [69], orvalidating shapes[102, 155]. Once a set of rules or constraints are instantiated,
the next step is to either identify which entities or facts in the KG violate any of them, or
employ them to delete erroneous information, or, finally, to employ them to deduce any missing
information [58, 159].
▶ Example 1. The following rules could apply for a subset of a graph describing people and their
relationships:
r1 : hasParent(x, y) ⇒hasChild(y, x);
r2 : hasParent(x, y) ⇒∃v1, v2∈N |hasBirthYear(x, v1) ∧hasBirthYear(y, v2);
r3 : hasChild(x, y)∧hasBirthYear(x, v1)∧hasBirthYear(y, v2) ⇒v1 < v2;
Where r1 states thathasChild is the inverse equivalent relation ofhasParent, r2 states that for
each person in the KGs for which we know the parent-child relationship we should know the birth
year, andr3 states that ify is a child ofx then x should be born beforey.
Nonetheless, a fundamental challenge is how to generate such rules and constraints. Specifying
them manually is prohibitively difficult and expensive [2, 157]. On the one hand, the domain
experts, who know the semantics for the dataset at hand, may not have the skill set or the
background necessary to formally express those rules. Even when skilled, domain experts would
require a substantial amount of manual work to exhaustively materialize a complete list of such
rules [158]. Therefore, in the past decade, we have witnessed an increased interest in methods that
can (semi-) automatically extract rules and constraints [158, 33]. In all those cases, the data in
the KG is exploited as asilver standard[146]. That is, while the data are not perfect, we can still
assume it is at least of reasonable quality. This approach works for rules that can find frequent
positive examples. The challenge arises for rules that need to govern entities and facts that are
rare, and for negative rules that need to prohibit some facts from appearing. To handle these
cases, contextual information, e.g., documents and other user input provided in textual form,
can be exploited in many different ways. In this context, LLMs bring a number of important
opportunities:
TGDK

2:16 LLMs and KGs: Opportunities and Challenges
ability to extract contextual information from a given text, e.g., a document describing rules
in natural language;
information extraction from contextual data, like domain knowledge in textual form explicitly
used during training;
automatic generation of new rules via deductive chain-of-thought prompting;
understanding rules vocabulary in context of a given domain description expressed in natural
language, allowing to reconcile rules with synonyms and polysemy;
providing explanations of rules or generating candidate validating or counterfactual examples.
Consider, for example, a rule where the relationshipshasParent has been used, an LLM can
be queries to identify whetherhasParent between two entities refers more likely to the semantic
meaning of being biologically descended or being owned or controlled. LLMs can be used to filter
out candidate constraints, e.g., given their ability to mimic simple common sense reasoning, rules
can be translated in the form of questions to the LLM, e.g., “if X is child of Y is it true that the
birth year of Y comes always before the birth year of X?”. Thus, an LLM can be used in support
or replacement of a human annotator towards generated rules.
One of the most promising abilities of LLMs is parsing long texts. In companies and organiza-
tions, documents exist that contain reference governing information, e.g., procedures, regulations,
and specifications. Here we see an untapped opportunity in parsing these documents in relation
to the entities and predicates in the KG to extract constraints. Yet, the challenge arises in the
fact that the LLM needs to use the correct vocabulary of entities and relations and the correct
rule syntax. Recent advancements in program synthesis show a possible way to the challenge.
Finally, an even more fundamental challenge is that of transcending the usage of LLMs for
NLP alone, and using them directly on large sets of facts within a KG. We can think of this setting
as a special kind of multi-modal LLMs, where the KG is a specific modality. We have seen similar
approaches in the past when word embedding approaches have been translated to knowledge
graphs [165]. This brings to the question of whether it is possible to train LLMs to treat the task
of rule generation as, for example, a graph embedding or summarization task [11, 28]. This would
require then the ability to perform both inductive and abductive reasoning and treat rules as
summaries from the set of facts in the KG.
A Rule Mining Case with ChatGPT.Let’s have a look at the following real example asking
ChatGPT to generate rules.
▶ Example 2. We ask ChatGPT “Please list three rules that could help to infer one person’s
father. And output it in a first-order rule form.” The following is the output we get:
“Certainly! Here are three rules expressed in first-order logic form that could help infer
a person’s father:
Rule 1: ∀x, y(child(x, y) ∧male(y) →father(y, x)) This rule states that for all
individuals x and y, if there exists a ’child’ relationship between x and y and y is male,
then y is the father of x.
Rule 2: ∀x, y(biologicalChild(x, y) →father(y, x)) This rule states that for all
individuals x and y, if there exists a ’biologicalChild’ relationship between x and y, then y
is the father of x.
Rule 3:∀x, y(fatherOf(y, x) →father(y, x)) This rule states that for all individuals
x and y, if there exists a ’fatherOf’ relationship between y and x, then y is the father of x.
These rules, expressed in first-order logic, demonstrate how the relationships between
individuals can be used to infer the father of a person within a KG.”

Jeff Z. Pan et al. 2:17
From the above example, we can see that ChatGPT gives three rules that can possibly infer the
father relationship. Rule 1 is correct which is consistent with the definition of father; Rule 2 is
a rule with high probability; and Rule 3 is also correct sincefather and fatherOf are inverse
relations. This demonstrates LLMs have rule knowledge and could express it in a formal form
following instruction, thus they could serve as experts for automatic rule construction. To this
end, however, we need toalign the rules from the LLM to the existing knowledge in the
KG, andfeed the LLM with the existing knowledge and the context encoded in the
KG. Both are consistent with discussion about the company and family examples.
Challenges and Opportunities.
Retrieval augmented rule extraction and generation:LLMs can be given access to
reference documents and KG and use this access to produce candidate rules informed by the
textual content of the documents as well.
LLM guided rule explanation and validation:LLMs can be used to identify from a list
of generated rules those that are more likely to hold within a given context. Further, it can
generate explanations on the meaning of the rule and its validity.
5.3.2 Ontology Refinement
Ontology refinement includes quite a few topics like knowledge completion (e.g., subsumption
prediction, complex concept learning and new concept placement), erroneous knowledge detection
and repair (e.g., inconsistency checking) and knowledge canonicalization (e.g., entity renaming).
Besides formally represented knowledge, real-world ontologies, such as the widely used medical
ontology SNOMED CT1 and food ontology FoodOn2, also include a lot of meta information
defined by different annotation properties for usability, such as entity labels, synonyms and natural
language definition. Taking the conceptobo:FOODON_00002809 in FoodOn as an example, it
has not only formal knowledge such as named super concepts and logical restrictions, but also
labels and synonyms (e.g., “edamame”), definitions (e.g., “Edamame is a preparation of immature
soybean ...”), comments and so on. These meta information, especially the natural language text,
further motivates people to use LLMs for ontology refinement.
For a refinement task, usually there are quite a few existing examples in the original ontology.
Therefore, a straightforward solution, which has been adopted by most current methods, is
fine-tuning a Pre-trained Language Model such as BERT together with an attached classifier. One
typical method is BERTSubs [29] which is to predict the subsumption relationship between two
named concepts, or between one named concept and one complex concept. It concatenates the
corresponding texts of the two candidate concepts with special tokens as the input of a model
composed of a pre-trained BERT and a logistic regression classifier, and fine-tunes the model with
the existing subsumptions in the target ontology. For a named concept, the text could be either its
name (label or synonym), or its name in combination with a textual description of its surrounding
concepts; while for a complex concept, the text is its description (a.k.a. verbalisation). Another
typical work is [119] which fine-tunes BERT and predicts the position to place in SNOMED CT
for a new concept. Note that there are also some language model-based methods in taxonomy
curation, such as [171] which fine-tunes BERT for taxonomy edge completion and GenTaxo [221]
which fine-tunes a BERT variant named SciBERT for predicting positions that need new concepts.
They can be directly applied or easily extended to refine an ontology’s concept hierarchies.
1 https://www.snomed.org/
2 https://foodon.org/
TGDK

2:18 LLMs and KGs: Opportunities and Challenges
Exploiting LLMs is a promising direction for ontology refinement, but it still needs much
effort before they become practical tools. DeepOnto [73], which is a Python-based package that
can support quite a few ontology engineering tasks, has already included some tools for ontology
refinement and alignment using LLMs, but more development is needed to make it more accessible
and to support generative LLMs like LLaMA and GPT-4. One obvious challenge is that those
very recent generative LLMs have been rarely explored for ontology engineering. However, we
think the following two research challenges are more fundamental.
Challenges and Opportunities.
Exploiting the graph structure and logic of an ontology together with its text.
Currently, LLM fine-tuning-based methods can well utilize the text of individual entities,
but their other formal semantics are often ignored or not effectively incorporated. Besides
fine-tuning with samples constructed by some templates, more LLM techniques such as prompt
learning and instruction tuning could be considered.
Combing symbolic reasoning with LLM inference. Symbolic reasoning, such as consist-
ency checking in OWL ontologies, can still play a role e.g., in validating the knowledge inferred
by LLMs. One aspect of incorporating symbolic reasoning is constructing samples for LLM
fine-tuning and extracting prompts for LLM inference, while another aspect is the synergized
framework [235] where LLM inference and symbolic reasoning work iteratively.
5.3.3 Ontology Alignment
The content of one single ontology is often incomplete and many real-world applications rely on
cross-domain knowledge. Ontology alignment (a.k.a. ontology matching), which is to identify
cross-ontology mappings between entities that have an equivalent, subsumption or membership
relationship, thus becomes especially important for knowledge integration. The entity can be a
concept (class), an individual (instance) or a property. Traditional systems (e.g., LogMap [91])
heavily rely on lexical matching and optionally use symbolic reasoning to remove mappings that
lead to logical conflicts; while some recent methods combine these techniques with machine
learning techniques like feature engineering, semantic embedding and distant supervision for
better performance (e.g., LogMap-ML [30]). Especially, when the ontologies have a large ratio of
assertions (large ABoxes) and the task is to discover equivalent individuals, ontology alignment is
very close to the KG entity alignment task that has been widely investigated in recent years using
KG embeddings [228]. As in ontology refinement, exploiting the textual information by applying
LLMs is a promising direction for augmenting ontology alignment.
The study of LLM application in ontology alignment is similar to ontology refinement. Pre-
trained language models such as BERT have been applied via fine-tuning [133, 72]. BERTMap [72]
is a typical system that has achieved state-of-the-art performance in many biomedical ontology
alignment benchmarks. It fine-tunes a pre-trained LM with synonym pairs extracted from the
original ontologies and the potentially given mappings, and combines the predicted concept
equivalence scores with lexical matching scores and reasoning for the mappings. Those recent
LLMs like GPT-4 have not been applied in ontology alignment, as far as we know, and the two
fundamental research challenges mentioned in ontology refinement are applicable in ontology
alignment. Besides, ontology alignment has another critical challenge.
Challenges and Opportunities.
Evaluating LLM-based ontology alignment systems. Novel evaluation protocols with new
metrics are needed to fairly and efficiently compare LLM-based systems even with incomplete
ground truth mappings [74]. Meanwhile, the semantics from the textual meta information
and the LLM may be inconsistent with formal semantics defined in ontologies, and thus it is
sometimes hard to determine whether a mapping by an LLM-based system is true or not.

Jeff Z. Pan et al. 2:19
5.4 KGs for LLMs: Training and Augmenting LLMs
In Sections 5.1 to 5.3, we discussed three different aspects on using LLMs for KGs. In this section,
we look into the other direction, i.e., using KGs for LLMs. There are a few dimensions here. Firstly,
KGs can be used as training data for LLMs. Secondly, triples in KGs can be used for prompt
construction. Last but not least, KGs can be used as external knowledge in retrieval-augmented
language models.
5.4.1 KGs for (Pre-)Training Language Models
KGs typically incorporate data derived from sources that are deemed highly reliable. The extracted
data goes through a post-processing phase before it is certified by human evaluations. This vetted
information from KGs has been incorporated into the pre-training corpus to complement natural
language text, which on its own, can result in limited information coverage [216, 150, 1, 212].
Using factual knowledge from KGs to pre-train LLMs has also infused structured know-
ledge [130]. This integration of KGs with LLMs, along with efficient prompts, has made it
convenient to inject world knowledge and incorporate new evolving information into language
models [49]. Additionally, knowledge expressed in high-resource language KBs has been transferred
into LMs tuned for low-resource languages [232, 118].
Furthermore, grounding knowledge from KGs to pre-train LMs has shown improvements in
performance on generation and QA tasks [34, 164, 136]. In another approach, [192] proposed
an interpretable neuro-symbolic KB, where the memory consists of vector representations of
entities and relations from an existing KB. These representations are augmented to an LM during
pre-training and fine-tuning, enabling the model to excel in knowledge-intensive QA tasks.
Challenges and Opportunities.
High-quality knowledge injection: KGs can prove to be a valuable source of knowledge,
fostering a more profound understanding of the relationships between entities within LLMs –
this is particularly true as existing KGs such as Wikidata [196] are committed to ensuring high
precision. Moreover, KGs’ ability to include dynamic updates with the latest information can
provide significant advantages during pre-training in comparison to outdated textual corpus.
Information duplication: KGs encapsulate direct and indirect relations, and one can induce
the same information using multiple facts. Such a kind of complex linking between entities is
generally hard to find in a single textual source. Therefore, leveraging KGs can enhance the
LLM’s understanding and reasoning capacities about popular as well as long-tail entities.
5.4.2 KGs for Prompt Construction
The attention received by the integration of KGs and LLMs has grown recently. On the one
hand, there is the explored direction of prompting LLMs for collecting and distilling knowledge in
order to make it available to the end-users. On the other hand, there is the less explored research
direction where KGs are used in synergy with prompts in order to enhance LLMs with capabilities
making them more effective and, at the same time, trustworthy. A number of studies have
leveraged KGs to enrich and fine-tune prompt creation resulting in a significant increase in prompt
quantity, quality, and diversity compared to manual approaches. KGs have been employed in single
and in multi-turn scaffolding prompts at scale, powered by numerous traversal paths over KGs
with low authoring cost while considering the meaningful learning patterns [107]. Other studies
have investigated how incorporating explicit knowledge from external sources like KGs can help
prompt engineering, especially by giving additional contexts (e.g., attributes, K-hop neighbors)
of the entities in order to help the LLMs to generate better predictions [23]. Approaches like
TGDK

2:20 LLMs and KGs: Opportunities and Challenges
KnowPrompt [35] use KGs to incorporate semantic and prior knowledge among relation labels into
prompt-tuning for relation extraction, enhancing the prompt construction process and optimizing
their representation with structured constraints. Certain studies have utilized LLMs and prompts
in the task of reasoning over KGs [40], e.g., LARK uses entities and relations in queries to find
pertinent sub-graph contexts within abstract KGs, and then, performs chain reasoning over these
contexts using LLM prompts of decomposed logical queries outperforming previous state-of-the-art
approaches by a significant margin.
Challenges and Opportunities. The current research in the field of KG utilization for prompt
creation predominantly centers around LLMs, which are considered to have relatively lower
efficacy compared to LLMs. LLMs present significant potential for advancing prompt creation
methodologies in conjunction with KGs. We may summarize this perspective within the following
four challenges:
KGs can be employed to automatically extract and represent relevant knowledge to generate
context-aware writing prompts. Analyze and understand the relationships between different
writing prompts, enabling the generation of prompts that build upon each other.
KGs can be combined with LLMs to facilitate the interactive and dynamic generation of
prompts, adapting to user feedback and preferences in real-time. Furthermore, the use of KGs
in prompt creation has opened up possibilities for explainability and interpretability. Since
KGs provide a transparent representation of knowledge, the prompts generated from KGs can
be easily traced back to their underlying sources.
KGs can integrate into prompts the definitions of guards exploited during the generative task.
Such guards may enhance the trustworthiness of the information generated by LLMs and make
them more compliant with specific domain-wise or context-wise constraints.
KGs can create prompts that ask questions (e.g., inferring missing relations in an incomplete
KG) that trigger KG complex reasoning capabilities and intermediate reasoning steps.
The integration of KGs within the prompt construction activities will allow us to answer the
following preparatory set of research questions. For each research question, we provide a link to
the challenges mentioned above, aiming to identify appropriate research pathways.
RQ1: How can KGs be integrated into existing prompts to enhance the effectiveness (including
relevance, absence of bias, privacy-preservation) of the information extracted from LLMs?−→
C1, C2, C3.
RQ2: How can KGs be exploited to drive the generative capabilities of LLMs in order to
properly address the whole ethical constraints of AI-based solutions?−→C2, C3.
RQ3: What are the optimal approaches to generate KGs-based prompts that enhance reasoning
capabilities? −→C4.
Also, in the following three scenarios, the community would benefit from tackling the above-
mentioned challenges and research questions.
KGs for Hallucination Detection in LLMs:The reliability of LLMs is greatly affected by
the hallucination problem, where they generate inaccurate information. Despite attempts to
address it, the issue of hallucination is likely to persist in the realm of LLMs for the foreseeable
future. To aid in the detection of hallucinations, KGs-based prompting aims to offer reliable
information that can serve as a foundation. By combining LLMs and KGs, researchers can
develop a comprehensive prompt-based fact-checking model that can identify hallucinations in
various domains.
KGs for Editing Knowledge in LLMs:LLMs possess the ability to store extensive real-
world knowledge, but they struggle to exploit prompts to update their internal knowledge
to reflect real-world changes. KGs-based prompts offer a potential solution for modifying

Jeff Z. Pan et al. 2:21
knowledge in LLMs, but they are restricted to handling basic tuple-based knowledge in KGs.
Indeed, even if the entire LLM undergoes re-training, the knowledge presented through prompts
would likely be assimilated within the vast network structure of the LLM.
KGs for Black-box LLMs Knowledge Injection:While pre-training and knowledge
editing methods can bring LLMs up to date with the latest information, they require access
to the internal structures and parameters of LLMs. However, many cutting-edge large LLMs
only offer APIs that allow users and developers to interact with them, keeping their internal
workings hidden from the public. Consequently, traditional KG injection techniques that involve
modifying LLM structures with additional knowledge fusion modules cannot be employed.
One potential solution is to convert various types of knowledge into different text prompts.
However, it remains an area of ongoing research to determine if these prompts can effectively
adapt to new LLMs. Additionally, the approach of using KGs-based prompts is constrained
by the length of input tokens accepted by LLMs. Therefore, the question of how to enable
effective knowledge injection for black-box LLMs still remains unanswered.
5.4.3 Retrieval Augmented Methods
There are a few reasons for why retrieval augmented methods are necessary for LLMs to obtain
external knowledge. One reason is to address the problem of knowledge cutoff, i.e., LLMs are
not aware of the events that happened after their training. Also, although parametric knowledge
would increase when the size of parameters increases, training LLMs is expensive; e.g., GPT-3
(175B parameters) costs $4.6 million to train, and PaLM (540B parameters) costs $17 million. In
fact, research suggests that the obtained knowledge from such training is mainly about popular
entities [125]. Furthermore, for domain specific applications, there might be some significant
knowledge that is not yet in LLMs, including private and business critical knowledge that cannot
be put into LLMs.
One idea to deal with the above lack of (updated) knowledge is to edit the knowledge in
LLMs. Knowledge Editing methods assume that we know which entries are wrong and how
to fix them. An obvious strategy is to retrain and fine-tune the model based on the modified
data. However, apart from being costly, retraining cannot guarantee that erroneous data will be
corrected. Another strategy is to develop a hyper-network to learn a parameter shift for the base
model. De Cao et al.[45] trained a hyper-network, KnowledgeEditor, to modify a fact and used
Kullback-Leibler (KL) divergence-constrained optimization to alleviate the side effect on other
data/knowledge that should not be changed. However, many state of the art methods do not
perform well when editingmultiple edits, as they use the same strategy to process multiple edits
and ignore the relation between different edit gradients, resulting in a “zero-sum” phenomenon,
where the inter-gradient conflict will inevitably cause some data modifications to fail. Han et
al. [71] design explicit and implicit multi-editor models to learn diverse editing strategies in terms
of dynamic structure and dynamic parameters respectively, allowing to deal with the conflict data
in an efficient end-to-end manner.
Alternatively, people could look into retrieve-generate architectures for building retrieval
augmented generation models. In this setting, we assume that the external sources contain the
needed knowledge for addressing users’ requirements. Initially, most such methods use unstructured
passages as external knowledge. RAG [109] outperforms DPR [99] by marginalizing the retrieval
step to train the generator and retriever jointly with the supervision of the label answer. RAG
tends to focus too much on label-relevant passages, rather than question-relevant passages and
answers. Huang et al. [85] address this issue by incorporating rich answer encoding through Dense
Knowledge Similarity (DKS) and Retriever as Answer Classifier (RAC). FiD [87] encodes the
concatenation of the passages retrieved by pre-trained DPR and the original question separately,
TGDK

2:22 LLMs and KGs: Opportunities and Challenges
Figure 2Different Tasks for Retrieval Augmented Methods.
and then fuses them with concatenation to the decoder. It is expected that structured knowledge
will be the main source of external knowledge (cf. Figure 2), as passages often contain noise.
Knowledge Graphs can be used directly as external knowledge. For example, KG-FiD [219]
utilizes knowledge graphs to further enhance the retrieval quality by establishing the structural
relationship among the retrieved passages. Another external source is databases. Vougiouklis et
al. [ 195] propose an efficient NL2SQL approach, transforming questions in natural language into
SQL over given database schemas, outperforming ChatGPT under the zero-shot setting while
achieving about 10 times speedup over other state of the art NL2SQL engines.
As illustrated in Figure 2, it is important to note that there are different tasks for retrieval
augmented methods to enhance large language models. In addition to the above mentioned
retrieval augmented methods for prompting, there are also methods for other tasks. For example,
Zhao et al. [229] propose the Verify-and-Edit framework, which makes use of retrieval augmented
methods to validate texts generated by large language models for individual steps within CoT-style
reasoning chains. Yang et al. [214] proposes LLMA accelerator to make use of retrieval augmented
methods for speeding up decoding of large language models. Gao et al. [63] propose the RARR
system, which retrieve evidence for texts generated by large language models for referencing
purpose. Apart from retrieval augmentation for generations, retrieval augmented methods can
be used for pre-training and fine-tuning [70] as well. Knowledge graphs are expected to play key
roles in these tasks.
Challenges and Opportunities. To sum up, retrieval augmentation is a very promising direction.
There are a few pressing challenges:
Unifying Knowledge Editing and Retrieval Augmentation: KGs can be used for editing
knowledge in LLMs, while at the same time, KGs can also be used as external knowledge
to assist LLMs in retrieval augmented methods. In fact, knowledge editing and retrieval

Jeff Z. Pan et al. 2:23
Figure 3Tools and APIs as External Knowledge Sources.
augmentation is getting very close. For example, Mitchel et al. [129] proposed a Retrieval-
Augmented Counterfactual Model (SERAC), which stores edits in an explicit memory for
knowledge editing over LLMs. However, SERAC primarily focuses on batch editing, assuming
that all editing data is known. Han et al. [177] propose a Retrieval Augmented Sequential
Model Editing framework (RASE) that enhances editing generalisation and could work with
different knowledge editors, supporting thousand’s of edits.
Semi-parametric LLMs: This direction is highly related to the topic of this position paper.
The idea is to make use of explicit knowledge to augment LLMs. One of the key issues is to
integrate different explicit knowledge [184], including unstructured ones, such as passages, and
structured ones, such as KGs and databases, for augmenting LLMs.
Support of Complex Reasoning: Can we go beyond simply retrieving explicit knowledge
by enabling reasoning through retrieval augmented methods? BehnamGhader et al. [12]
demonstrated with their experimental results that the similarity metric used by the retrievers
is generally insufficient for reasoning tasks. Furthermore, LLMs do not take the complicated
relations between statements into account, thus leading to poor reasoning performance.
Attribution Evaluation and Revision: Can we retrieve relevant passages or structure
knowledge for some generated textt for a given queryq (or a dialog [52])? If it turns out that
t is not appropriate forq, can we produce some revised textt′ instead [64]?
Tool Use and Agent: In a sense, retrieval augmented methods are mainly using a retriever
to offer external knowledge. One step further is to use tools [168] and APIs [156] as external
source of knowledge, as illustrated in Figure 3. There will be lots of room for Knowledge
Graph related research in this space.
TGDK

2:24 LLMs and KGs: Opportunities and Challenges
6 Some Thoughts on Applications
The integration of KGs and LLMs in a unified approach holds significant potential, as their
combination mutually enhances and complements each other in a valuable manner. For instance,
KGs provide very accurate and explicit knowledge, which is crucial for some applications i.e.
healthcare, whereas LLMs have been criticized for their lack of factual knowledge leading to
hallucinations and inaccurate facts. secondly, LLMs lack explainability instead, KGs given their
symbolic reasoning ability, are able to generate interpretable results. On the other hand, KGs
are difficult to construct from unstructured text and suffer from incompleteness therefore, LLMs
could be utilized in addressing these challenges by text processing. Various applications have
adopted this methodology of combining LLMs with KGs, such as healthcare assistants3, question
answering systems [217] or ChatBots, and sustainability, among others.
6.1 Commonsense Knowledge
The majority of KGs capture facts of the sort one might encounter in an encyclopedia or in
a relational database. However, commonsense knowledge is another important form of world
knowledge for AI systems. For instance, we may wish for a KG to not only capture that the
Congo rainforest lies in Central Africa, but also that tropical rainforests have significant rainfall
and lush green vegetation. ConceptNet is the most well-known commonsense knowledge graph,
developed using manual crowdsourcing along with automated refinement techniques [120]. However,
crowdsourcing is very labor-intensive and costly, so alternative means of harvesting such knowledge
have long been sought.
Commonsense Knowledge from LLMs. The first study to investigate extracting knowledge
from a language model to the best of our knowledge was indeed one that targeted commonsense
knowledge [185]. The authors mined commonsense triples such ashasProperty (apples, green)
from the Google Web 1T n-gram data as well as from Microsoft’s Web-scale smoothed language
models [82]. This was later extended into a large-scale commonsense knowledge graph [187] that
covered a range of different relations and became a part of the WebChild KG [186].
As both crowdsourcing and information extraction from text are likely to lead to incomplete
knowledge, a key challenge is how to generalize beyond what has been collected. The WebBrain
project explored neural knowledge graph completion [32] for better generalization. COMET, short
for COMmonsEnse Transformer [21], and the improved COMET-ATOMIC 2020 [86], used existing
data to fine-tune Transformer-based models. This line of work considers the original ConceptNet
relations as well as reasoning-related knowledge pertaining to events, causes, and effects, e.g.,
what goals might have motivated a personA to leave an event without personB. Recently, [208]
shows how common-sense triples could be extracted from an LLM and use through distillation to
transfer knowledge into a smaller LM, outperforming the larger one. Overall, fine-tuned LLMs are
found to outperform off-the-shelf LLMs, while also benefiting from the advances of the latter.
Challenges and Opportunities. Commonsense knowledge, in particular, is genuinely open-ended,
such that it depends on a number of considerations whether it makes sense to attempt to materialize
relevant knowledge beforehand or rather invoke a (possibly slow) LLM on the fly. Commonsense
knowledge may also differ substantially between different cultures [134]. This also leads to the
3 https://neo4j.com/blog/doctor-ai-a-voice-chatbot-for-healthcare-powered-by-neo4j-and-aws/

Jeff Z. Pan et al. 2:25
question of what kinds of biases are acceptable. Finally, a long-term challenge is how to capture
knowledge that is not easily expressed in language, e.g., how a robot ought to grasp different kinds
of objects.
6.2 Digital Build Environment
In the domain of Build Environment, where it is vital to design and construct in a safe and
sustainable way, a number of regulations and guidelines need to be met. Automated Compliance
Code Checking has bloomed to support this, but still, in the past, it was quite challenging to
interpret regulations and execute rules in 3D models automatically due to the ambiguity of the
text, and the need for extensive expert knowledge for interpretation. Many applications now in this
area have combined LLMs + KGs in addressing these challenges by following an LLMs enhanced
KG approach [235]. LLMs interpret the text in the regulations and enhance a KG of rules, which
are further serialized using dome Domain Specific Language [226, 203]. Interrogating 3D models
modeled as graphs using the Linked Building Data approach is another challenge for the domain
as it requires skill sets in query languages like SPARQL. LLMs are helping in understanding
human language written questions and converting those into relevant query languages by bringing
a new way of how domain experts interact and interrogate 3D models and their various forms. An
example of this is AI Speckle4.
6.3 Digital Healthcare
The Digital Healthcare sector holds immense potential for various possibilities concerning the
adoption of LLMs, including the automation of clinical documentation, the synthesis of patient
histories, and the identification of potential candidates for clinical trials. Although these advance-
ments are remarkable, it is crucial to recognize the potential risks associated with employing
LLMs in healthcare. Indeed, Digital Healthcare is one of the most critical application domains for
the adoption of LLMs. The needs of the major stakeholders (i.e., physicians, healthcare providers,
and policymakers) row against the paradigm behind the creation of LLMs. In particular, the two
major significant risks related to the model’s accuracy and the privacy concerns stemming from
its usage.
Accuracy. Some demonstrations of LLMs have showcased impressive capabilities. Nevertheless,
there have also been documented instances where LLMs have made mistakes or exhibited erratic
behavior. In the Digital Healthcare sector, where patient safety is of utmost importance, it
is crucial for healthcare organizations to comprehend the potential risks associated with LLM
usage. When utilized to diagnose hypothetical patient cases, LLMs have exhibited accuracy
at a level comparable to that of a third- or fourth-year medical student, albeit not reaching a
professional’s proficiency. Despite this high level of performance, LLMs have also been known
to generate false information, invent sources, commit logical errors, and provide answers that
are inappropriate or unethical. The integration of KGs would definitely enhance the capabilities
of LLMs given the possibility of injecting domain-specific knowledge able to mitigate the issues
mentioned above. Avoiding hallucinations and preserving ethics are definitely the two major
aspects to which LLMs+KG may contribute in a significant manner.
4 https://speckle.systems/blog/ai-powered-conversations-with-speckle/
TGDK

2:26 LLMs and KGs: Opportunities and Challenges
Privacy. One major concern with LLMs is that employing any third-party application necessitates
the transmission of data to that party. When data, including protected health information (PHI),
is managed by a covered entity like a hospital, it becomes subject to the regulations of the
jurisdiction where the entity is located (e.g., GDPR). Furthermore, by sending PHI to additional
third parties, organizations lose control over how that data will be handled. For instance, healthcare
organizations are unable to determine the exact storage location of their data, whether it will be
mixed with data from other organizations and utilized to train future language models, or what
security measures are in place to safeguard the data. Healthcare organizations employing LLMs
must recognize that their data are potentially more susceptible to breaches or misuse. The role of
preserving private information may be played by KGs through the modeling of axioms defining
which data may be shared and with who and how personal knowledge may be anonymized in
order to be transmitted to possible external systems.
An alternative approach, prioritizing privacy, involves running an open-source LLM within the
infrastructure of a healthcare organization. This way, it would be possible to directly work on the
parameters of LLMs given the possibility of having control of the injected knowledge and, at the
same time, ensuring that data are never shared with a third party. However, these open-source
models are currently not as advanced or extensively trained as the more popular commercial
systems (e.g., ChatGPT). Additionally, the effort to create the knowledge resources to inject and
the expertise required to program and maintain an open-source LLM may not be readily available
to many healthcare organizations.
The two risks described above lead to likewise challenges that must be tackled in order to
make a significant step toward the adoption of these models within the clinical practice.
6.3.1 Domain Specific Content Search
Recently we have witnessed the success of models like GPT-4 [137] in a multitude of domain-specific
NLP applications that involve multiple modalities and domain specific adaptations. In these cases
they need to be able to access data stored in multiple modalities (e.g., pictures, diagrams, scientific
images, PDF documents, or system logs) and an abundance of domain specific information that has
not been accessed during training. In these use-cases, while LLMs are often treated as generative
models, they can be easily adopted in search and reasoning tasks when integrated in specific
tools and pipelines5. Nonetheless, as seen in the past all these specialized domains can better
benefit from the inclusion of symbolic knowledge in machine methods [6]. Here we focus on
two prototypical applications: (1) semantic image and video search and (2) technical document
understanding.
Recently, many methods, primarily based on deep learning models such as CLIP [160] and
BLIP2 [113], achieved state-of-the-art performance on image retrieval tasks. These multi-modal
models jointly learn vector embeddings for images and text, such that the embedding of the image
should be close to that of the text that describes that image. Nonetheless, we have also seen
increased interest in obtaining a more symbolic representation of the contents of an image [145, 105].
Datasets like Visual Genome [105] annotate images withscene graphs. A scene graph is a small
KG that describes, with a structured formal graphical representation, the contents of an image
in terms of objects (people, animals, items) as nodes connected via pairwise relationships (e.g.,
actions or positioning relationships) as edges. Therefore, Multimodal LLM can be trained to
reason and exploit this additional representation offering an advanced ability to understand the
contents of an image (or a video). Importantly, a scene graph node and edge can be annotated
5 For examplehttps://haystack.deepset.ai/

Jeff Z. Pan et al. 2:27
(grounded) with features and positions from the image (e.g., relative size). This can be exploited
in applications like image and video search and question answering. When entities in a scene graph
are connected to a background taxonomy or KG, then questions that require forms of abstraction
and computation, e.g.,What is the genus of the largest animal in the picture? What is the average
price of the car in the picture? Retrieve images depicting kids wearing vegan friendly items of
clothing in the catalog.
On the other hand, the digitalization of domain specific documents, e.g., especially contracts,
is enabling in-depth applications of machine intelligence to help humans more effectively perform
time-consuming tasks. Among these, contract review costs humans substantial time, money, and
attention (many law firms spend approximately 50% of their time reviewing contracts, costing
hundreds of thousands of dollars) [77]. The Contract Understanding Atticus Dataset (CUAD) is a
new dataset for legal contract review [77]. CUAD was created with legal experts and consisted of
over 13,000 annotations. Recent advancements in generic pre-trained language models showed
their power in some text-understanding tasks. Therefore, we have seen different domain specific
applications of NLP and LLM methods [209, 215]. Yet, they do not have access to all relevant
knowledge and are ill-suited for certain calculations [98]. This can be solved by exploiting external
domain specific symbolic information, e.g., domain specific knowledge graphs [135, 117, 66], and
by adding symbolic and reasoning capabilities to the LLMs [98]. This promising direction will
lead to extending current state-of-the-art neuro-symbolic methods to combine the advantages of a
graph representation when extracting symbolic knowledge from complex documents, the ability to
understand long-form unstructured texts of LLMs, and the good properties of domain-specific
code synthesis of LLMs to address advanced retrieval and question answering use-cases, e.g.,How
many weeks are left before the expiration of this contract? What are the conflicts between this
liability clause and previous contracts my company signed? What is the risk of side-effects of this
treatment for a patient with this given health record? Get the average yearly yield and spread for
competitor companies of ACorp and their recent acquisitions in the EU market.
7 Outlook
In conclusion, the recent advances on large language models (LLMs) mark an important inflection
point for knowledge graph (KG) research. While important questions on the ability to combine
their strengths remain open, these offer exciting opportunities for future research. This paper has
covered a number of relevant topics about KG and LLM. There are some others that may have
not been widely investigated at the current stage but are worthy of mentioning, including LLM
for multi-modal and temporal KG construction [36, 211], LLM for KG question answering [80],
multilingualism of LLM and KG [178], KG for LLM instruction tuning and human alignment, KG
for faster LLM inference and so on. The community is already rapidly adapting their research focus,
with novel forums like the KBC-LM workshop [96], the LM-KBC challenge [175] and the LLM
sub-track of OAEI Bio-ML6 arising, and resources massively shifting towards hybrid approaches
to knowledge extraction, consolidation, and usage. We give out the following recommendations:
1. Don’t throw out the KG with the paradigm shift: For a range of reliability or safety-critical
applications, structured knowledge remains indispensable, and we have outlined many ways in
which KGs and LLMs can fertilize each other. KGs are here to stay, do not just ditch them
out of fashion.
2. Murder your (pipeline) darlings: LLMs have substantially advanced many tasks in the KG
and ontology construction pipeline, and even made some tasks obsolete. Take critical care in
examining even the most established pipeline components, and compare them continuously
with the LLM-based state of the art.
6 https://www.cs.ox.ac.uk/isg/projects/ConCur/oaei/2023/index.html
TGDK

2:28 LLMs and KGs: Opportunities and Challenges
3. Stay curious, stay critical: LLMs are arguably the most impressive artifact of AI research of
the past years. Nonetheless, there exist a magnitude of exaggerated claims and expectations in
the public as well as in the research literature, and one should retain a healthy dose of critical
reflection. In particular, a fundamental fix to the so-called problem of hallucinations is not in
sight.
4. The past is over, let’s begin the new journey: The advances triggered by LLMs have uprooted
the field in an unprecedented manner, and enable to enter the field with significant shortcuts.
There is no better time to start anew in fields related to Knowledge Computing, than now.
Although the direction of the present transformation is widely open, as researchers continue to
explore the potentials and challenges of hybrid approaches, we can expect to see new breakthroughs
in the representation and processing of knowledge, with far-reaching implications for fields ranging
from Knowledge Computing to NLP, AI, and beyond.
References
1 Oshin Agarwal, Heming Ge, Siamak Shakeri, et al.
Knowledge graph based synthetic corpus genera-
tion for knowledge-enhanced language model pre-
training. In NAACL, pages 3554–3565, jun 2021.
doi:10.18653/V1/2021.NAACL-MAIN.278.
2 Naser Ahmadi, Viet-Phi Huynh, Vamsi Meduri,
Stefano Ortona, and Paolo Papotti. Mining ex-
pressive rules in knowledge graphs.J. Data and
Information Quality, 12(2), 2020. doi:10.1145/
3371315.
3 Mirza Mohtashim Alam, Md Rashad Al Hasan
Rony, Mojtaba Nayyeri, Karishma Mohiuddin,
MST Mahfuja Akter, Sahar Vahdati, and Jens
Lehmann. Language model guided knowledge
graph embeddings. IEEE Access, 10:76008–76020,
2022. doi:10.1109/ACCESS.2022.3191666.
4 Dimitrios Alivanistos, Selene Báez Santamaría,
Michael Cochez, Jan-Christoph Kalo, Emile van
Krieken, and Thiviyan Thanapalasingam. Prompt-
ing as probing: Using language models for know-
ledge base construction, 2022. doi:10.48550/
ARXIV.2208.11057.
5 Badr AlKhamissi, Millicent Li, Asli Celikyilmaz,
Mona Diab, and Marjan Ghazvininejad. A review
on language models as knowledge bases.arXiv,
2022. doi:10.48550/ARXIV.2204.06031.
6 Mona Alshahrani, Mohammad Asif Khan, Omar
Maddouri, Akira R Kinjo, Núria Queralt-Rosinach,
and Robert Hoehndorf. Neuro-symbolic repres-
entation learning on biological knowledge graphs.
Bioinformatics, 33(17):2723–2730, apr 2017.doi:
10.1093/BIOINFORMATICS/BTX275.
7 Sihem Amer-Yahia, Angela Bonifati, Lei Chen,
Guoliang Li, Kyuseok Shim, Jianliang Xu, and
Xiaochun Yang. From large language models to
databases and back: A discussion on research
and education. DASFAA, abs/2306.01388, 2023.
doi:10.48550/ARXIV.2306.01388.
8 Alejandro Barredo Arrieta, Natalia Díaz
Rodríguez, Javier Del Ser, Adrien Bennetot,
Siham Tabik, A. Barbado, Salvador García,
Sergio Gil-Lopez, Daniel Molina, Richard Ben-
jamins, Raja Chatila, and Francisco Herrera.
Explainable artificial intelligence (XAI): Con-
cepts, taxonomies, opportunities and challenges
toward responsible ai.Information Fusion, 2020.
doi:10.1016/J.INFFUS.2019.12.012.
9 Sören Auer, Christian Bizer, Georgi Kobilarov,
Jens Lehmann, Richard Cyganiak, and Zachary
Ives. Dbpedia: A nucleus for a web of open
data. In The semantic web, pages 722–735, 2007.
doi:10.1007/978-3-540-76298-0_52 .
10 Stephen H Bach, Victor Sanh, Zheng-Xin Yong,
Albert Webson, Colin Raffel, Nihal V Nayak, Ab-
heesht Sharma, Taewoon Kim, M Saiful Bari,
Thibault Fevry, et al. Promptsource: An integ-
rated development environment and repository for
natural language prompts. ACL, 2022. arXiv:
2202.01279, doi:10.48550/arXiv.2202.01279.
11 Roy Bar-Haim, Lilach Eden, Roni Friedman, Yoav
Kantor, Dan Lahav, and Noam Slonim. From argu-
ments to key points: Towards automatic argument
summarization. In ACL, pages 4029–4039, 2020.
doi:10.18653/V1/2020.ACL-MAIN.371.
12 Parishad BehnamGhader, Santiago Miret, and
Siva Reddy. Can retriever-augmented language
models reason? the blame game between the re-
triever and the language model. InarXiv, 2022.
doi:10.48550/ARXIV.2212.09146.
13 Emily M Bender, Timnit Gebru, Angelina
McMillan-Major, et al. On the dangers of
stochastic parrots: Can language models be too
big? In FAT, pages 610–623, 2021.doi:10.1145/
3442188.3445922.
14 Emily M. Bender and Alexander Koller. Climb-
ing towards NLU: On meaning, form, and un-
derstanding in the age of data. In ACL, 2020.
doi:10.18653/V1/2020.ACL-MAIN.463.
15 Russa Biswas, Harald Sack, and Mehwish Alam.
Madlink: Attentive multihop and entity descrip-
tions for link prediction in knowledge graphs.SWJ,
pages 1–24, 2022.doi:10.3233/SW-222960.
16 Russa Biswas, Radina Sofronova, Mehwish Alam,
and Harald Sack. Contextual language models for
knowledge graph completion. InMLSMKG, 2021.
doi:10.34657/7668.
17 Su Lin Blodgett, Solon Barocas, Hal Daum’e, and
Hanna M. Wallach. Language (technology) is
power: A critical survey of “bias” in nlp.ACL,
2020. doi:10.18653/V1/2020.ACL-MAIN.485.

Jeff Z. Pan et al. 2:29
18 Bernd Bohnet, Vinh Q Tran, Pat Verga, Roee
Aharoni, DanielAndor, LivioBaldiniSoares, Jacob
Eisenstein, Kuzman Ganchev, Jonathan Herzig,
Kai Hui, et al. Attributed question answering:
Evaluation and modeling for attributed large lan-
guage models. arXiv preprint arXiv:2212.08037,
2022. doi:10.48550/ARXIV.2212.08037.
19 Angela Bonifati, Wim Martens, and Thomas
Timm. Navigating the maze of wikidata query
logs. In WWW, pages 127–138, 2019. doi:
10.1145/3308558.3313472.
20 Angela Bonifati, Wim Martens, and Thomas
Timm. An analytical study of large SPARQL
query logs. VLDB J., 29(2-3):655–679, 2020.
doi:10.1007/S00778-019-00558-9 .
21 Antoine Bosselut, Hannah Rashkin, Maarten Sap,
Chaitanya Malaviya, Asli Celikyilmaz, and Yejin
Choi. COMET: Commonsense transformers for
automatic knowledge graph construction. In
ACL, pages 4762–4779, 2019.doi:10.18653/V1/
P19-1470.
22 Ruben Branco, António Branco, João An-
tónio Rodrigues, et al. Shortcutted commonsense:
Data spuriousness in deep learning of common-
sense reasoning. InEMNLP, pages 1504–1521, nov
2021. doi:10.18653/V1/2021.EMNLP-MAIN.113.
23 Ryan Brate, Minh Hoang Dang, Fabian Hoppe,
Yuan He, Albert Meroño-Peñuela, and Vijay Sa-
dashivaiah. Improving language model predictions
via prompts enriched with knowledge graphs. In
Proceedings of the Workshop on Deep Learning
for Knowledge Graphs (DL4KG 2022) co-located
with the 21th International Semantic Web Con-
ference (ISWC 2022), Virtual Conference, on-
line, October 24, 2022, volume 3342 of CEUR
Workshop Proceedings. CEUR-WS.org, 2022. URL:
https://ceur-ws.org/Vol-3342/paper-3.pdf .
24 Tom Brown, Benjamin Mann, Nick Ryder,
Melanie Subbiah, Jared D Kaplan, Prafulla
Dhariwal, Arvind Neelakantan, Pranav Shyam,
Girish Sastry, Amanda Askell, et al. Lan-
guage models are few-shot learners. neur-
IPS, 33:1877–1901, 2020. URL: https:
//proceedings.neurips.cc/paper/2020/hash/
1457c0d6bfcb4967418bfb8ac142f64a-Abstract.
html.
25 Sébastien Bubeck, Varun Chandrasekaran, Ronen
Eldan, Johannes Gehrke, Eric Horvitz, Ece Kamar,
Peter Lee, Yin Tat Lee, Yuanzhi Li, Scott Lund-
berg, Harsha Nori, Hamid Palangi, Marco Tulio
Ribeiro, and Yi Zhang. Sparks of artificial general
intelligence: Early experiments with gpt-4, 2023.
doi:10.48550/ARXIV.2303.12712.
26 Boxi Cao, Hongyu Lin, Xianpei Han, Le Sun,
Lingyong Yan, Meng Liao, Tong Xue, and Jin
Xu. Knowledgeable or educated guess? revisit-
ing language models as knowledge bases. InACL,
pages 1860–1874, aug 2021. doi:10.18653/V1/
2021.ACL-LONG.146.
27 J Harry Caufield, Harshad Hegde, Vincent Emonet,
Nomi L Harris, Marcin P Joachimiak, Nicolas
Matentzoglu, HyeongSik Kim, Sierra AT Moxon,
Justin T Reese, Melissa A Haendel, et al. Struc-
tured prompt interrogation and recursive extrac-
tionofsemantics(spires): Amethodforpopulating
knowledge bases using zero-shot learning.arXiv,
2023. doi:10.48550/ARXIV.2304.02711.
28 Sejla Cebiric, François Goasdoué, Haridimos Kon-
dylakis, Dimitris Kotzinos, Ioana Manolescu, Geor-
gia Troullinou, and Mussab Zneika. Summarizing
semantic graphs: a survey.VLDB J., 28(3):295–
327, 2019. doi:10.1007/S00778-018-0528-3 .
29 Jiaoyan Chen, Yuan He, Yuxia Geng, Ernesto
Jiménez-Ruiz, Hang Dong, and Ian Horrocks. Con-
textual semantic embeddings for ontology sub-
sumption prediction. WWW, pages 1–23, 2023.
doi:10.1007/S11280-023-01169-9 .
30 Jiaoyan Chen, Ernesto Jiménez-Ruiz, Ian Hor-
rocks, Denvar Antonyrajah, Ali Hadian, and
Jaehun Lee. Augmenting ontology alignment
by semantic embedding and distant supervision.
In ESWC, pages 392–408, 2021. doi:10.1007/
978-3-030-77385-4_23 .
31 Jiaoyan Chen, Freddy Lecue, Jeff Z. Pan, Ian Hor-
rocks, and Huajun Chen. Knowledge-based Trans-
fer Learning Explanation. InKR, pages 349–358,
2018. URL: https://aaai.org/ocs/index.php/
KR/KR18/paper/view/18054.
32 Jiaqiang Chen, Niket Tandon, Charles Darwis Har-
iman, and Gerard de Melo. WebBrain: Joint
neural learning of large-scale commonsense know-
ledge. In ISWC, pages 102–118, 2016. URL:http:
//gerard.demelo.org/webbrain/, doi:10.1007/
978-3-319-46523-4_7 .
33 MingyangChen, WenZhang, YuxiaGeng, Zezhong
Xu, Jeff Z. Pan, and Huajun Chen. Generalizing to
unseen elements: A survey on knowledge extrapol-
ation for knowledge graphs. InProceedings of the
Thirty-Second International Joint Conference on
Artificial Intelligence, IJCAI 2023, 19th-25th Au-
gust 2023, Macao, SAR, China, pages 6574–6582.
ijcai.org, 2023. doi:10.24963/IJCAI.2023/737.
34 Wenhu Chen, Yu Su, Xifeng Yan, and Wil-
liamYangWang. KGPT:Knowledge-groundedpre-
training for data-to-text generation. InEMNLP,
2020. doi:10.18653/V1/2020.EMNLP-MAIN.697.
35 Xiang Chen, Ningyu Zhang, Xin Xie, Shumin
Deng, Yunzhi Yao, Chuanqi Tan, Fei Huang, Luo
Si, and Huajun Chen. Knowprompt: Knowledge-
aware prompt-tuning with synergistic optimiza-
tion for relation extraction. In Frédérique La-
forest, Raphaël Troncy, Elena Simperl, Deepak
Agarwal, Aristides Gionis, Ivan Herman, and Li-
onel Médini, editors,WWW ’22: The ACM Web
Conference 2022, Virtual Event, Lyon, France,
April 25 – 29, 2022, pages 2778–2788. ACM, 2022.
doi:10.1145/3485447.3511998.
36 Zhuo Chen, Jiaoyan Chen, Wen Zhang, Lingbing
Guo, Yin Fang, Yufeng Huang, Yuxia Geng, Jeff Z
Pan, Wenting Song, and Huajun Chen. Mea-
former: Multi-modal entity alignment transformer
for meta modality hybrid. InACM Multimedia,
2023. doi:10.1145/3581783.3611786.
37 Wei-Lin Chiang, Zhuohan Li, Zi Lin, Ying Sheng,
Zhanghao Wu, Hao Zhang, Lianmin Zheng, Siyuan
Zhuang, Yonghao Zhuang, Joseph E. Gonzalez, Ion
Stoica, and Eric P. Xing. Vicuna: An open-source
chatbot impressing gpt-4 with 90%* chatgpt qual-
ity, mar 2023. URL: https://lmsys.org/blog/
2023-03-30-vicuna/ .
TGDK

2:30 LLMs and KGs: Opportunities and Challenges
38 Bonggeun Choi, Daesik Jang, and Youngjoong
Ko. Mem-kgc: Masked entity model for knowledge
graph completion with pre-trained language model.
IEEE Access, 9, 2021.doi:10.1109/ACCESS.2021.
3113329.
39 Bonggeun Choi and Youngjoong Ko. Knowledge
graph extension with a pre-trained language model
via unified learning method.Knowledge-Based Sys-
tems, page 110245, 2023.doi:10.1016/J.KNOSYS.
2022.110245.
40 Nurendra Choudhary and Chandan K. Reddy.
Complex logical reasoning over knowledge
graphs using large language models. CoRR,
abs/2305.01157, 2023. doi:10.48550/ARXIV.2305.
01157.
41 Aakanksha Chowdhery, Sharan Narang, Jacob
Devlin, Maarten Bosma, Gaurav Mishra, Adam
Roberts, Paul Barham, Hyung Won Chung,
Charles Sutton, Sebastian Gehrmann, Parker
Schuh, Kensen Shi, Sasha Tsvyashchenko, Joshua
Maynez, Abhishek Rao, Parker Barnes, Yi Tay,
Noam Shazeer, Vinodkumar Prabhakaran, Emily
Reif, Nan Du, Ben Hutchinson, Reiner Pope,
James Bradbury, Jacob Austin, Michael Isard,
Guy Gur-Ari, Pengcheng Yin, Toju Duke, Anselm
Levskaya, Sanjay Ghemawat, Sunipa Dev, Henryk
Michalewski, Xavier Garcia, Vedant Misra, Kevin
Robinson, Liam Fedus, Denny Zhou, Daphne Ip-
polito, David Luan, Hyeontaek Lim, Barret Zoph,
Alexander Spiridonov, Ryan Sepassi, David Do-
han, Shivani Agrawal, Mark Omernick, Andrew M.
Dai, Thanumalayan Sankaranarayana Pillai, Marie
Pellat, Aitor Lewkowycz, Erica Moreira, Rewon
Child, Oleksandr Polozov, Katherine Lee, Zong-
wei Zhou, Xuezhi Wang, Brennan Saeta, Mark
Diaz, Orhan Firat, Michele Catasta, Jason Wei,
Kathy Meier-Hellstern, Douglas Eck, Jeff Dean,
Slav Petrov, and Noah Fiedel. Palm: Scaling
language modeling with pathways, 2023. URL:
http://jmlr.org/papers/v24/22-1144.html.
42 Aida Mostafazadeh Davani, Mark Díaz, and
Vinodkumar Prabhakaran. Dealing with disagree-
ments: Looking beyond the majority vote in
subjective annotations. TACL, 10:92–110, 2022.
doi:10.1162/TACL_A_00449.
43 Daniel Daza, Michael Cochez, and Paul Groth.
Inductive Entity Representations from Text via
Link Prediction. InWWW, pages 798–808, 2021.
doi:10.1145/3442381.3450141.
44 N De Cao, G Izacard, S Riedel, and F Petroni.
Autoregressive entity retrieval. In ICLR 2021-
9th International Conference on Learning Rep-
resentations, volume 2021. ICLR, 2020. URL:
https://openreview.net/forum?id=5k8F6UU39V.
45 Nicola De Cao, Wilker Aziz, and Ivan Titov. Edit-
ing factual knowledge in language models. In
Proceedings of the 2021 Conference on Empirical
Methods in Natural Language Processing, pages
6491–6506, OnlineandPuntaCana, DominicanRe-
public, nov 2021. Association for Computational
Linguistics. doi:10.18653/V1/2021.EMNLP-MAIN.
522.
46 Xiang Deng, Huan Sun, Alyssa Lees, You Wu, and
Cong Yu. Turl: Table understanding through
representation learning. ACM SIGMOD Re-
cord, 51(1):33–40, 2022. doi:10.1145/3542700.
3542709.
47 Jacob Devlin, Ming-Wei Chang, Kenton Lee, and
Kristina Toutanova. Bert: Pre-training of deep bid-
irectional transformers for language understanding.
NAACL, 2019. doi:10.18653/V1/N19-1423.
48 Xin Luna Dong, Evgeniy Gabrilovich, Geremy
Heitz, Wilko Horn, Kevin Murphy, Shaohua Sun,
and Wei Zhang. From data fusion to know-
ledge fusion. VLDB, 7(10):881–892, jun 2014.
doi:10.14778/2732951.2732962.
49 CíceroNogueiradosSantos, ZheDong, DanielMat-
thew Cer, John Nham, Siamak Shakeri, Jianmo
Ni, and Yun-Hsuan Sung. Knowledge prompts:
Injecting world knowledge into language mod-
els through soft prompts. ArXiv, 2022. doi:
10.48550/ARXIV.2210.04726.
50 Mengnan Du, Fengxiang He, Na Zou, et al. Short-
cut learning of large language models in natural
language understanding: A survey.arXiv, 2022.
doi:10.48550/ARXIV.2208.11857.
51 Yupei Du, Qi Zheng, Yuanbin Wu, Man Lan, Yan
Yang, and Meirong Ma. Understanding gender
bias in knowledge base embeddings. InACL, 2022.
doi:10.18653/V1/2022.ACL-LONG.98.
52 N Dziri, H Rashkin, T Linzen, and D Reit-
ter. Evaluating attribution in dialogue sys-
tems: The BEGIN benchmark. TACL,
2022. URL: https://transacl.org/ojs/index.
php/tacl/article/view/3977.
53 Yanai Elazar, Nora Kassner, Shauli Ravfogel, Amir
Feder, Abhilasha Ravichander, Marius Mosbach,
YonatanBelinkov, HinrichSchütze, andYoavGold-
berg. Measuring causal effects of data statistics
on language model’s ‘factual’ predictions.arXiv,
2023. doi:10.48550/ARXIV.2207.14251.
54 Yanai Elazar, Nora Kassner, Shauli Ravfogel,
Abhilasha Ravichander, Eduard Hovy, Hinrich
Schütze, and Yoav Goldberg. Measuring and im-
proving consistency in pretrained language models.
TACL, 9, 2021.doi:10.1162/TACL_A_00410.
55 Ahmed K. Elmagarmid, Panagiotis G. Ipeirotis,
and Vassilios S. Verykios. Duplicate record de-
tection: A survey. TKDE, 19(1):1–16, 2007.
doi:10.1109/TKDE.2007.250581.
56 Grace Fan, Jin Wang, Yuliang Li, Dan Zhang,
and Renée Miller. Semantics-aware dataset discov-
ery from data lakes with contextualized column-
based representation learning.VLDB, 2023. doi:
10.14778/3587136.3587146.
57 Wenfei Fan, Chunming Hu, Xueli Liu, and Ping
Lu. Discovering graph functional dependencies.
ACM Trans. Database Syst., 45(3), sep 2020.
doi:10.1145/3397198.
58 Wenfei Fan, Ping Lu, Chao Tian, and Jingren
Zhou. Deducing certain fixes to graphs. Proc.
VLDB Endow., 12(7):752–765, mar 2019. doi:
10.14778/3317315.3317318.
59 I. P. Fellegi and A. B. Sunter. A theory for re-
cord linkage. Journal of the American Statistical
Association, 64:1183–1210, 1969. doi:10.1080/
01621459.1969.10501049.
60 Besnik Fetahu, Ujwal Gadiraju, and Stefan Di-
etze. Improving entity retrieval on structured
data. In ISWC, pages 474–491, 2015. doi:
10.1007/978-3-319-25007-6_28 .

Jeff Z. Pan et al. 2:31
61 Luis Antonio Galárraga, Christina Teflioudi, Katja
Hose, and Fabian Suchanek. Amie: Association
rule mining under incomplete evidence in ontolo-
gicalknowledgebases. In WWW,WWW’13, pages
413–422, 2013. doi:10.1145/2488388.2488425.
62 Daniel Gao, Yantao Jia, Lei Li, Chengzhen Fu,
Zhicheng Dou, Hao Jiang, Xinyu Zhang, Lei
Chen, and Zhao Cao. Kmir: A benchmark for
evaluating knowledge memorization, identification
and reasoning abilities of language models, 2022.
doi:10.48550/arXiv.2202.13529.
63 Luyu Gao, Zhuyun Dai, Panupong Pasupat, An-
thony Chen, Arun Tejasvi Chaganty, Yicheng Fan,
Vincent Zhao, Ni Lao, Hongrae Lee, Da-Cheng
Juan, and Kelvin Guu. RARR: Researching and
revising what language models say, using lan-
guage models. In Anna Rogers, Jordan Boyd-
Graber, and Naoaki Okazaki, editors,Proceedings
of the 61st Annual Meeting of the Association for
Computational Linguistics (Volume 1: Long Pa-
pers), pages 16477–16508, Toronto, Canada, jul
2023. Association for Computational Linguistics.
doi:10.18653/V1/2023.ACL-LONG.910.
64 Luyu Gao, Zhuyun Dai, Panupong Pasupat, An-
thony Chen, Arun Tejasvi Chaganty, Yicheng
Fan, Vincent Zhao, Ni Lao, Hongrae Lee, Da-
Cheng Juan, and Kelvin Guu. Rarr: Research-
ing and revising what language models say, us-
ing language models. In ACL2023, 2023. doi:
10.18653/V1/2023.ACL-LONG.910.
65 Genet Asefa Gesese, Russa Biswas, Mehwish Alam,
and Harald Sack. A survey on knowledge graph
embeddings with literals: Which model links bet-
ter literal-ly? Semantic Web, 12(4):617–647, 2021.
doi:10.3233/SW-200404.
66 Agneta Ghose, Matteo Lissandrini, Emil Riis
Hansen, and Bo Pedersen Weidema. A core onto-
logy for modeling life cycle sustainability assess-
ment on the semantic web.Journal of Industrial
Ecology, 26(3):731–747, 2022.doi:10.1111/jiec.
13220.
67 Bernardo Cuenca Grau, Ian Horrocks, Boris Motik,
Bijan Parsia, Peter F. Patel-Schneider, and Ulrike
Sattler. OWL 2: The next step for OWL. J.
Web Semant, 6(4):309–322, 2008.doi:10.1016/J.
WEBSEM.2008.05.001.
68 Paul Groth, Elena Paslaru Bontas Simperl, Mar-
ieke van Erp, and Denny Vrandecic. Know-
ledge graphs and their role in the knowledge
engineering of the 21st century (dagstuhl sem-
inar 22372). Dagstuhl Reports, 12:60–120, 2022.
doi:10.4230/DAGREP.12.9.60.
69 OWL Working Group. OWL 2 Web Ontology
Language Document Overview: W3C Recom-
mendation, 2012. URL:https://www.w3.org/TR/
owl2-overview/.
70 Kelvin Guu, Kenton Lee, Zora Tung, Panupong
Pasupat, and Mingwei Chang. Retrieval augmen-
ted language model pre-training. In Hal Daumé
III and Aarti Singh, editors,Proceedings of the
37th International Conference on Machine Learn-
ing, volume 119 ofProceedings of Machine Learn-
ing Research, pages 3929–3938. PMLR, 13–18
July 2020. URL:http://proceedings.mlr.press/
v119/guu20a.html.
71 Xiaoqi Han, Ru Li, Xiaoli Li, and Jeff Z. Pan. A
Divide and Conquer Framework for Knowledge
Editing. Knowledge Based Systems, 279:110826,
2023. doi:10.1016/j.knosys.2023.110826.
72 Yuan He, Jiaoyan Chen, Denvar Antonyrajah, and
Ian Horrocks. Bertmap: a bert-based ontology
alignmentsystem. InAAAI,volume36, pages5684–
5691, 2022. doi:10.1609/AAAI.V36I5.20510.
73 Yuan He, Jiaoyan Chen, Hang Dong, Ian Hor-
rocks, Carlo Allocca, Taehun Kim, and Brahman-
anda Sapkota. DeepOnto: A Python package for
ontology engineering with deep learning.arXiv
preprint arXiv:2307.03067, 2023. doi:10.48550/
ARXIV.2307.03067.
74 Yuan He, Jiaoyan Chen, Hang Dong, Ernesto
Jiménez-Ruiz, Ali Hadian, and Ian Horrocks. Ma-
chine learning-friendly biomedical datasets for
equivalence and subsumption ontology matching.
In ISWC, pages 575–591, 2022. doi:10.1007/
978-3-031-19433-7_33 .
75 Yuan He, Jiaoyan Chen, Ernesto Jimenez-Ruiz,
Hang Dong, and Ian Horrocks. Language
model analysis for ontology subsumption infer-
ence. In Findings of the Association for Compu-
tational Linguistics: ACL 2023, pages 3439–3453,
Toronto, Canada, jul 2023. Association for Com-
putational Linguistics. doi:10.18653/V1/2023.
FINDINGS-ACL.213.
76 Benjamin Heinzerling and Kentaro Inui. Lan-
guage models as knowledge bases: On entity rep-
resentations, storage capacity, and paraphrased
queries. In EACL, pages 1772–1791, 2021.doi:
10.18653/V1/2021.EACL-MAIN.153.
77 Dan Hendrycks, Collin Burns, Anya Chen, and
Spencer Ball. CUAD: An expert-annotated NLP
dataset for legal contract review. InThirty-fifth
Conference on Neural Information Processing Sys-
tems Datasets and Benchmarks Track (Round 1),
2021. URL: https://openreview.net/forum?id=
7l1Ygs3Bamw.
78 Or Honovich, Uri Shaham, Samuel R. Bowman,
and Omer Levy. Instruction induction: From few
examples to natural language task descriptions. In
Anna Rogers, Jordan L. Boyd-Graber, and Naoaki
Okazaki, editors,Proceedings of the 61st Annual
Meeting of the Association for Computational Lin-
guistics (Volume 1: Long Papers), ACL 2023,
Toronto, Canada, July 9-14, 2023, pages 1935–
1952. Association for Computational Linguistics,
2023. doi:10.18653/V1/2023.ACL-LONG.108.
79 Edward J. Hu, Yelong Shen, Phillip Wallis, Zey-
uan Allen-Zhu, Yuanzhi Li, Shean Wang, Lu Wang,
and Weizhu Chen. Lora: Low-rank adaptation of
large language models. InThe Tenth International
Conference on Learning Representations, ICLR
2022, Virtual Event, April 25-29, 2022. OpenRe-
view.net, 2022. URL: https://openreview.net/
forum?id=nZeVKeeFYf9.
80 Nan Hu, Yike Wu, Guilin Qi, Dehai Min, Jiaoyan
Chen, Jeff Z. Pan, and Zafar Ali. An empirical
study of pre-trained language models in simple
knowledge graph question answering.World Wide
Web (WWW), 26(5):2855–2886, 2023. doi:10.
1007/S11280-023-01166-Y .
81 Ziniu Hu, Yichong Xu, Wenhao Yu, Shuohang
Wang, Ziyi Yang, Chenguang Zhu, Kai-Wei Chang,
TGDK

2:32 LLMs and KGs: Opportunities and Challenges
and Yizhou Sun. Empowering language models
with knowledge graph reasoning for open-domain
question answering. In Yoav Goldberg, Zornitsa
Kozareva, and Yue Zhang, editors,Proceedings
of the 2022 Conference on Empirical Methods
in Natural Language Processing, EMNLP 2022,
Abu Dhabi, United Arab Emirates, December 7-11,
2022, pages 9562–9581. Association for Computa-
tional Linguistics, 2022. doi:10.18653/V1/2022.
EMNLP-MAIN.650.
82 Jian Huang, Jianfeng Gao, Jiangbo Miao, Xiao-
long Li, Kuansan Wang, Fritz Behr, and C. Lee
Giles. Exploring web scale language models for
search query processing. InWWW, pages 451–460,
2010. doi:10.1145/1772690.1772737.
83 Jie Huang and Kevin Chen-Chuan Chang. To-
wards reasoning in large language models: A sur-
vey. Findings of ACL, 2023.doi:10.48550/ARXIV.
2212.10403.
84 Ningyuan Huang, Yash R Deshpande, Yibo Liu,
Houda Alberts, Kyunghyun Cho, Clara Vania, and
IacerCalixto. Endowinglanguagemodelswithmul-
timodal knowledge graph representations.arXiv,
2022. doi:10.48550/ARXIV.2206.13163.
85 Wenyu Huang, Mirella Lapata, Pavlos Vougiouklis,
Nikos Papasarantopoulos, and Jeff Z. Pan. Re-
trieval Augmented Generation with Rich Answer
Encoding. In Proc. of IJCNLP-AACL 2023, 2023.
86 Jena D. Hwang, Chandra Bhagavatula, Ronan Le
Bras, Jeff Da, Keisuke Sakaguchi, Antoine Bosse-
lut, and Yejin Choi. Comet-atomic 2020: On sym-
bolic and neural commonsense knowledge graphs.
In AAAI, 2021. doi:10.1609/AAAI.V35I7.16792.
87 Gautier Izacard and Edouard Grave. Lever-
aging passage retrieval with generative models
for open domain question answering. In Paola
Merlo, Jörg Tiedemann, and Reut Tsarfaty, ed-
itors, Proceedings of the 16th Conference of the
European Chapter of the Association for Compu-
tational Linguistics: Main Volume, EACL 2021,
Online, April 19 – 23, 2021, pages 874–880. As-
sociation for Computational Linguistics, 2021.
doi:10.18653/V1/2021.EACL-MAIN.74.
88 Sarthak Jain and Byron C. Wallace. Attention is
not explanation. In Jill Burstein, Christy Doran,
and Thamar Solorio, editors,Proceedings of the
2019 Conference of the North American Chapter
of the Association for Computational Linguist-
ics: Human Language Technologies, NAACL-HLT
2019, Minneapolis, MN, USA, June 2-7, 2019,
Volume 1 (Long and Short Papers), pages 3543–
3556. Association for Computational Linguistics,
2019. doi:10.18653/V1/N19-1357.
89 Krzysztof Janowicz, Bo Yan, Blake Regalia, Rui
Zhu, and Gengchen Mai. Debiasing knowledge
graphs: Why female presidents are not like fe-
male popes. In Marieke van Erp, Medha Atre,
Vanessa López, Kavitha Srinivas, and Carolina
Fortuna, editors,Proceedings of the ISWC 2018
Posters & Demonstrations, Industry and Blue Sky
Ideas Tracks co-located with 17th International Se-
mantic Web Conference (ISWC 2018), Monterey,
USA, October 8th – 12th, 2018, volume 2180
of CEUR Workshop Proceedings. CEUR-WS.org,
2018. URL: https://ceur-ws.org/Vol-2180/
ISWC_2018_Outrageous_Ideas_paper_17.pdf.
90 ZhengbaoJiang, FrankFXu, JunAraki, etal. How
can we know what language models know?TACL,
8:423–438, 2020. doi:10.1162/TACL_A_00324.
91 Ernesto Jiménez-Ruiz and Bernardo Cuenca Grau.
Logmap: Logic-based and scalable ontology match-
ing. InISWC, pages 273–288, 2011.doi:10.1007/
978-3-642-25073-6_18 .
92 Ernesto Jiménez-Ruiz, Oktie Hassanzadeh, Vasilis
Efthymiou, Jiaoyan Chen, and Kavitha Srinivas.
Semtab 2019: Resources to benchmark tabu-
lar data to knowledge graph matching systems.
In ESWC, pages 514–530, 2020. doi:10.1007/
978-3-030-49461-2_30 .
93 Martin Josifoski, Nicola De Cao, Maxime Peyrard,
Fabio Petroni, and Robert West. Genie: Generat-
ive information extraction. InProceedings of the
2022 Conference of the North American Chapter
of the Association for Computational Linguistics:
Human Language Technologies, pages 4626–4643,
2022. doi:10.18653/V1/2022.NAACL-MAIN.342.
94 Martin Josifoski, Marija Sakota, Maxime Peyrard,
and Robert West. Exploiting asymmetry for
synthetic training data generation: Synthie and
the case of information extraction.ArXiv, 2023.
doi:10.48550/ARXIV.2303.04132.
95 Jan-Christoph Kalo and Leandra Fichtel. Kamel:
Knowledge analysis with multitoken entit-
ies in language models. In AKBC, 2022.
URL: https://www.akbc.ws/2022/assets/pdfs/
15_kamel_knowledge_analysis_with_.pdf.
96 Jan-Christoph Kalo, Simon Razniewski, Sneha
Singhania, and Jeff Z. Pan. LM-KBC: Knowledge
base construction from pre-trained language mod-
els. ISWC Challenges, 2023.
97 Nikhil Kandpal, Haikang Deng, Adam Roberts,
Eric Wallace, and Colin Raffel. Large language
models struggle to learn long-tail knowledge, 2023.
doi:10.48550/ARXIV.2211.08411.
98 Ehud Karpas, Omri Abend, Yonatan Belinkov,
Barak Lenz, Opher Lieber, Nir Ratner, Yoav Sho-
ham, Hofit Bata, Yoav Levine, Kevin Leyton-
Brown, Dor Muhlgay, Noam Rozen, Erez
Schwartz, Gal Shachaf, Shai Shalev-Shwartz, Am-
non Shashua, and Moshe Tennenholtz. MRKL
systems: A modular, neuro-symbolic architecture
that combines large language models, external
knowledge sources and discrete reasoning.CoRR,
abs/2205.00445, 2022. doi:10.48550/ARXIV.2205.
00445.
99 Vladimir Karpukhin, Barlas Oguz, Sewon Min,
Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi
Chen, and Wen tau Yih. Dense passage retrieval
for open-domain question answering. InEMNLP,
pages 6769–6781, 2020. doi:10.18653/V1/2020.
EMNLP-MAIN.550.
100 Nora Kassner and Hinrich Schütze. Negated and
misprimed probes for pretrained language mod-
els: Birds can talk, but cannot fly. InACL, 2020.
doi:10.18653/V1/2020.ACL-MAIN.698.
101 Bosung Kim, Taesuk Hong, Youngjoong Ko, and
Jungyun Seo. Multi-task learning for knowledge
graph completion with pre-trained language mod-
els. In COLING, pages 1737–1743, 2020. doi:
10.18653/V1/2020.COLING-MAIN.153.
102 Holger Knublauch and Dimitris Kontokostas.
Shapes constraint language (SHACL). Technical

Jeff Z. Pan et al. 2:33
report, W3C, jul 2017. URL: https://www.w3.
org/TR/shacl/.
103 Keti Korini and Christian Bizer. Column type
annotation using chatgpt. arXiv, 2023. doi:
10.48550/ARXIV.2306.00745.
104 Angelie Kraft and Ricardo Usbeck. The life-
cycle of “facts”: A survey of social bias in know-
ledge graphs. In AACL, 2022. URL: https:
//aclanthology.org/2022.aacl-main.49.
105 Ranjay Krishna, Yuke Zhu, Oliver Groth, Justin
Johnson, Kenji Hata, Joshua Kravitz, Stephanie
Chen, Yannis Kalantidis, Li-Jia Li, David A.
Shamma, Michael S. Bernstein, and Li Fei-Fei.
Visual genome: Connecting language and vis-
ion using crowdsourced dense image annotations.
Int. J. Comput. Vis., 123(1):32–73, 2017. doi:
10.1007/S11263-016-0981-7 .
106 Viet Dac Lai, Nghia Trung Ngo, Amir Pouran Ben
Veyseh, Hieu Man, Franck Dernoncourt, Trung
Bui, and Thien Huu Nguyen. Chatgpt beyond eng-
lish: Towards a comprehensive evaluation of large
language models in multilingual learning.ArXiv,
2023. doi:10.48550/ARXIV.2304.05613.
107 Yoonjoo Lee, John Joon Young Chung, Tae Soo
Kim, Jean Y. Song, and Juho Kim. Promptiverse:
Scalable generation of scaffolding prompts through
human-ai hybrid knowledge graph annotation. In
CHI, 2022. doi:10.1145/3491102.3502087.
108 Alina Leidinger and Richard Rogers. Which ste-
reotypes are moderated and under-moderated in
search engine autocompletion? InProceedings of
the 2023 ACM Conference on Fairness, Accountab-
ility, and Transparency, FAccT 2023, Chicago, IL,
USA, June 12-15, 2023, pages 1049–1061. ACM,
2023. doi:10.1145/3593013.3594062.
109 Patrick Lewis, Ethan Perez, Aleksandra Piktus,
Fabio Petroni, Vladimir Karpukhin, Naman
Goyal, Heinrich Küttler, Mike Lewis, Wen-tau
Yih, Tim Rocktäschel, Sebastian Riedel, and
Douwe Kiela. Retrieval-augmented genera-
tion for knowledge-intensive nlp tasks. In
neurIPS, volume 33, 2020. URL: https:
//proceedings.neurips.cc/paper/2020/hash/
6b493230205f780e1bc26945df7481e5-Abstract.
html.
110 Belinda Z. Li, Sewon Min, Srinivasan Iyer, Yashar
Mehdad, and Wen-tau Yih. Efficient one-pass
end-to-end entity linking for questions. InProceed-
ings of the 2020 Conference on Empirical Methods
in Natural Language Processing, EMNLP 2020,
Online, November 16-20, 2020, pages 6433–6441,
2020. doi:10.18653/V1/2020.EMNLP-MAIN.522.
111 Bo Li, Gexiang Fang, Yang Yang, Quansen Wang,
Wei Ye, Wen Zhao, and Shikun Zhang. Evalu-
ating chatgpt’s information extraction capabilit-
ies: An assessment of performance, explainabil-
ity, calibration, and faithfulness. ArXiv, 2023.
doi:10.48550/ARXIV.2304.11633.
112 Da Li, Ming Yi, and Yukai He. Lp-bert: Multi-
task pre-training knowledge graph bert for link
prediction. arXiv, 2022. arXiv:2201.04843.
113 Junnan Li, Dongxu Li, Silvio Savarese, and Steven
Hoi. BLIP-2: Bootstrapping language-image pre-
training with frozen image encoders and large
language models. In Andreas Krause, Emma
Brunskill, Kyunghyun Cho, Barbara Engelhardt,
Sivan Sabato, and Jonathan Scarlett, editors,
Proceedings of the 40th International Conference
on Machine Learning, volume 202 of Proceed-
ings of Machine Learning Research, pages 19730–
19742. PMLR, 23–29 July 2023. URL: https:
//proceedings.mlr.press/v202/li23q.html.
114 Tianyi Li, Mohammad Javad Hosseini, Sabine
Weber, and Mark Steedman. Language models
are poor learners of directional inference. InFind-
ings of the Association for Computational Lin-
guistics: EMNLP 2022, pages 903–921, Abu Dh-
abi, United Arab Emirates, dec 2022. Association
for Computational Linguistics.doi:10.18653/V1/
2022.FINDINGS-EMNLP.64.
115 Tianyi Li, Wenyu Huang, Nikos Papasaranto-
poulos, Pavlos Vougiouklis, and Jeff Z. Pan. Task-
specific pre-training and prompt decomposition
for knowledge graph population with language
models. In LM-KBC, 2022. arXiv:2208.12539,
doi:10.48550/ARXIV.2208.12539.
116 Stephan Linzbach, Tim Tressel, Laura Kallmeyer,
Stefan Dietze, and Hajira Jabeen. Decoding
prompt syntax: Analysing its impact on knowledge
retrieval in large language models. InNLP4KGC,
2023. doi:10.1145/3543873.3587655.
117 Matteo Lissandrini, Davide Mottin, Themis
Palpanas, Dimitra Papadimitriou, and Yannis
Velegrakis. Unleashing the power of informa-
tion graphs. SIGMOD Rec., 43(4):21–26, 2014.
doi:10.1145/2737817.2737822.
118 Fangyu Liu, Ivan Vulic, Anna Korhonen, and Nigel
Collier. Learning domain-specialised representa-
tions for cross-lingual biomedical entity linking.
In ACL, 2021.doi:10.18653/V1/2021.ACL-SHORT.
72.
119 Hao Liu, Yehoshua Perl, and James Geller.
Concept placement using bert trained by trans-
forming and summarizing biomedical ontology
structure. Journal of Biomedical Informat-
ics, 112:103607, 2020. doi:10.1016/J.JBI.2020.
103607.
120 Hugo Liu and Push Singh. Commonsense reason-
ing in and over natural language. InKnowledge-
Based Intelligent Information and Engineering
Systems, pages 293–306, 2004. doi:10.1007/
978-3-540-30134-9_40 .
121 Jixiong Liu, Yoan Chabot, Raphaël Troncy, Viet-
Phi Huynh, Thomas Labbé, and Pierre Monnin.
From tabular data to knowledge graphs: A survey
of semantic table interpretation tasks and methods.
J. Web Semant., 2022. doi:10.1016/J.WEBSEM.
2022.100761.
122 Yinhan Liu, Myle Ott, Naman Goyal, Jingfei Du,
Mandar Joshi, Danqi Chen, Omer Levy, Mike
Lewis, Luke Zettlemoyer, and Veselin Stoyanov.
Roberta: A robustly optimized bert pretraining
approach. arXiv, 2019. arXiv:1907.11692.
123 Fengyuan Lu, Peijin Cong, and Xinli Huang.
Utilizing textual information in knowledge graph
embedding: A survey of methods and applica-
tions. IEEE Access, 8:92072–92088, 2020. doi:
10.1109/ACCESS.2020.2995074.
124 Chaitanya Malaviya, Chandra Bhagavatula, Ant-
oineBosselut, andYejinChoi. Commonsenseknow-
ledge base completion with structural and semantic
TGDK

2:34 LLMs and KGs: Opportunities and Challenges
context. In AAAI, volume 34, pages 2925–2933,
2020. doi:10.1609/AAAI.V34I03.5684.
125 Alex Mallen, Akari Asai, Victor Zhong, Rajarshi
Das, Daniel Khashabi, and Hannaneh Hajishirzi.
When not to trust language models: Investigat-
ing effectiveness of parametric and non-parametric
memories. InProceedings of the 61st Annual Meet-
ing of the Association for Computational Linguist-
ics (Volume 1: Long Papers), pages 9802–9822,
Toronto, Canada, jul 2023. Association for Com-
putational Linguistics. doi:10.18653/V1/2023.
ACL-LONG.546.
126 Rui Mao, Qian Liu, Kai He, et al. The biases of pre-
trained language models: An empirical study on
prompt-based sentiment analysis and emotion de-
tection. IEEE Transactions on Affective Comput-
ing, pages 1–11, 2022.doi:10.1109/TAFFC.2022.
3204972.
127 Ninareh Mehrabi, Thamme Gowda, Fred Morstat-
ter, Nanyun Peng, and Aram Galstyan. Man is
to person as woman is to location: Measuring
gender bias in named entity recognition. In Ujwal
Gadiraju, editor,HT ’20: 31st ACM Conference
on Hypertext and Social Media, Virtual Event,
USA, July 13-15, 2020, pages 231–232. ACM, 2020.
doi:10.1145/3372923.3404804.
128 Chris Mellish and Jeff Z. Pan. Natural Language
Directed Inference from Ontologies. In Artifi-
cial Intelligence Journal, 2008. doi:10.1016/J.
ARTINT.2008.01.003.
129 EricMitchell, CharlesLin, AntoineBosselut, Chris-
topher D Manning, and Chelsea Finn. Memory-
based model editing at scale. In International
Conference on Machine Learning, pages 15817–
15831. PMLR, 2022. URL:https://proceedings.
mlr.press/v162/mitchell22a.html.
130 Fedor Moiseev, Zhe Dong, Enrique Alfonseca, and
Martin Jaggi. Skill: Structured knowledge infu-
sion for large language models. InNAACL, 2022.
doi:10.18653/V1/2022.NAACL-MAIN.113.
131 Moin Nadeem, Anna Bethke, and Siva Reddy. Ste-
reoset: Measuring stereotypical bias in pretrained
language models. In Chengqing Zong, Fei Xia,
Wenjie Li, and Roberto Navigli, editors,Proceed-
ings of the 59th Annual Meeting of the Association
for Computational Linguistics and the 11th Inter-
national Joint Conference on Natural Language
Processing, ACL/IJCNLP 2021, (Volume 1: Long
Papers), Virtual Event, August 1-6, 2021, pages
5356–5371. Association for Computational Lin-
guistics, 2021. doi:10.18653/V1/2021.ACL-LONG.
416.
132 Mojtaba Nayyeri, Zihao Wang, Mst Akter,
Mirza Mohtashim Alam, Md Rashad Al Hasan
Rony, Jens Lehmann, Steffen Staab, et al. Integ-
rating knowledge graph embedding and pretrained
language models in hypercomplex spaces.arXiv,
2022. doi:10.48550/ARXIV.2208.02743.
133 Sophie Neutel and Maaike HT de Boer. Towards
automatic ontology alignment using bert. InAAAI
Spring Symposium: Combining Machine Learn-
ing with Knowledge Engineering, 2021. URL:
https://ceur-ws.org/Vol-2846/paper28.pdf.
134 Tuan-Phong Nguyen, Simon Razniewski, Aparna
Varde, and Gerhard Weikum. Extracting cultural
commonsense knowledge at scale. InWWW, pages
1907–1917, 2023. doi:10.1145/3543507.3583535.
135 Natalya Fridman Noy, Yuqing Gao, Anshu Jain,
Anant Narayanan, Alan Patterson, and Jamie
Taylor. Industry-scale knowledge graphs: lessons
and challenges.Commun. ACM, 62(8):36–43, 2019.
doi:10.1145/3331166.
136 Barlas Oguz, Xilun Chen, Vladimir Karpukhin,
Stan Peshterliev, Dmytro Okhonko, Michael Sejr
Schlichtkrull, Sonal Gupta, Yashar Mehdad, and
Scott Yih. Unik-qa: Unified representations of
structured and unstructured knowledge for open-
domain question answering. In Marine Carpuat,
Marie-Catherine de Marneffe, and Iván Vladi-
mir Meza Ruíz, editors, Findings of the Asso-
ciation for Computational Linguistics: NAACL
2022, Seattle, WA, United States, July 10-15,
2022, pages 1535–1546. Association for Compu-
tational Linguistics, 2022.doi:10.18653/V1/2022.
FINDINGS-NAACL.115.
137 OpenAI. GPT-4 technical report, 2023. doi:
10.48550/ARXIV.2303.08774.
138 Long Ouyang, Jeff Wu, Xu Jiang, et al. Training
language models to follow instructions with human
feedback. neurIPS, 2022. URL: http://papers.
nips.cc/paper_files/paper/2022/hash/
b1efde53be364a73914f58805a001731-Abstract-
Conference.html.
139 Jeff Z. Pan. Resource Description Framework. In
Handbook on Ontologies. IOS Press, 2009. doi:
10.1007/978-3-540-92673-3_3 .
140 Jeff Z. Pan and Ian Horrocks. Web Ontology Reas-
oning with Datatype Groups. In ISWC, pages
47–63, 2003. doi:10.1007/978-3-540-39718-2_4 .
141 Jeff Z. Pan, Guido Vetere, José Manuél Gómez-
Pérez, and Honghan Wu. Exploiting linked
data and knowledge graphs in large organisa-
tions. Springer International Publishing, 2017.
doi:10.1007/978-3-319-45654-6 .
142 Shirui Pan, Linhao Luo, Yufei Wang, Chen Chen,
Jiapu Wang, and Xindong Wu. Unifying large lan-
guage models and knowledge graphs: A roadmap.
arXiv, 2023. doi:10.48550/ARXIV.2306.08302.
143 Lalchand Pandia and Allyson Ettinger. Sorting
through the noise: Testing robustness of inform-
ation processing in pre-trained language models.
EMNLP, 2021. doi:10.48550/arXiv.2109.12393.
144 George Papadakis, Ekaterini Ioannou, Emanouil
Thanos, and Themis Palpanas. The four gen-
erations of entity resolution. In Synthesis Lec-
tures on Data Management, 2021. doi:10.2200/
S01067ED1V01Y202012DTM064.
145 Jae Sung Park, Chandra Bhagavatula, Roozbeh
Mottaghi, Ali Farhadi, and Yejin Choi. Visual-
comet: Reasoning about the dynamic context of
a still image. InComputer Vision – ECCV 2020
– 16th European Conference, Glasgow, UK, Au-
gust 23-28, 2020, Proceedings, Part V, volume
12350 of Lecture Notes in Computer Science,
pages 508–524. Springer, 2020. doi:10.1007/
978-3-030-58558-7_30 .
146 Heiko Paulheim. Knowledge graph refinement:
A survey of approaches and evaluation meth-
ods. Semantic Web, 8(3):489–508, 2017. doi:
10.3233/SW-160218.

Jeff Z. Pan et al. 2:35
147 Ralph Peeters, Reng Chiz Der, and Christian Bizer.
WDC products: A multi-dimensional entity match-
ing benchmark. InProceedings 27th International
Conference on Extending Database Technology,
EDBT 2024, Paestum, Italy, March 25 – March
28, pages 22–33, 2024.doi:10.48786/EDBT.2024.
03.
148 Shichao Pei, Lu Yu, Guoxian Yu, and Xiangliang
Zhang. Rea: Robust cross-lingual entity align-
ment between knowledge graphs. InKDD, pages
2175–2184, 2020. doi:10.1145/3394486.3403268.
149 Guilherme Penedo, Quentin Malartic, Daniel
Hesslow, Ruxandra Cojocaru, Alessandro Cappelli,
Hamza Alobeidli, Baptiste Pannier, Ebtesam Al-
mazrouei, and Julien Launay. The refinedweb data-
set for falcon llm: Outperforming curated corpora
with web data, and web data only, 2023.arXiv:
2306.01116, doi:10.48550/ARXIV.2306.01116.
150 Matthew E Peters, Mark Neumann, Robert L
Logan IV, Roy Schwartz, Vidur Joshi, Sameer
Singh, and Noah A Smith. Knowledge enhanced
contextual word representations.EMNLP, 2019.
arXiv:1909.04164.
151 Fabio Petroni, Patrick Lewis, Aleksandra Piktus,
et al. How context affects language models’ factual
predictions. AKBC, 2020. doi:10.24432/C5201W.
152 Fabio Petroni, Tim Rocktäschel, Sebastian Riedel,
Patrick Lewis, Anton Bakhtin, Yuxiang Wu, and
Alexander Miller. Language models as knowledge
bases? In Proceedings of the 2019 Conference
on Empirical Methods in Natural Language Pro-
cessing and the 9th International Joint Confer-
ence on Natural Language Processing (EMNLP-
IJCNLP), pages 2463–2473, Hong Kong, China,
nov 2019. Association for Computational Linguist-
ics. doi:10.18653/V1/D19-1250.
153 Gabriele Picco, Marcos Martinez Galindo, Al-
berto Purpura, Leopold Fuchs, Vanessa Lopez,
and Thanh Lam Hoang. Zshot: An open-source
framework for zero-shot named entity recognition
and relation extraction. InProceedings of the 61st
Annual Meeting of the Association for Computa-
tional Linguistics (Volume 3: System Demonstra-
tions), pages 357–368, 2023. doi:10.18653/V1/
2023.ACL-DEMO.34.
154 Barbara Plank. The “problem” of human label
variation: On ground truth in data, modeling
and evaluation. EMNLP, abs/2211.02570, 2022.
doi:10.18653/V1/2022.EMNLP-MAIN.731.
155 Eric Prud’hommeaux, José Emilio Labra Gayo,
and Harold R. Solbrig. Shape expressions: an
RDF validation and transformation language. In
Harald Sack, Agata Filipowska, Jens Lehmann,
and Sebastian Hellmann, editors,Proceedings of
the 10th International Conference on Semantic
Systems, SEMANTiCS 2014, Leipzig, Germany,
September 4-5, 2014, pages 32–40. ACM, 2014.
doi:10.1145/2660517.2660523.
156 Yujia Qin, Shihao Liang, Yining Ye, Kunlun Zhu,
Lan Yan, Yaxi Lu, Yankai Lin, Xin Cong, Xiangru
Tang, Bill Qian, Sihan Zhao, Runchu Tian, Ruob-
ing Xie, Jie Zhou, Mark Gerstein, Dahai Li, Zhiy-
uan Liu, and Maosong Sun. Toolllm: Facilitating
large language models to master 16000+ real-world
apis, 2023. doi:10.48550/ARXIV.2307.16789.
157 Kashif Rabbani, Matteo Lissandrini, and Katja
Hose. SHACL and shex in the wild: A community
survey on validating shapes generation and ad-
option. In Frédérique Laforest, Raphaël Troncy,
Elena Simperl, Deepak Agarwal, Aristides Gionis,
Ivan Herman, and Lionel Médini, editors,Compan-
ion of The Web Conference 2022, Virtual Event /
Lyon, France, April 25 – 29, 2022, pages 260–263.
ACM, 2022.doi:10.1145/3487553.3524253.
158 Kashif Rabbani, Matteo Lissandrini, and Katja
Hose. Extraction of validating shapes from
very large knowledge graphs. Proc. VLDB En-
dow., 16(5):1023–1032, jan 2023.doi:10.14778/
3579075.3579078.
159 Kashif Rabbani, Matteo Lissandrini, and Katja
Hose. SHACTOR: improving the quality of large-
scale knowledge graphs with validating shapes. In
Sudipto Das, Ippokratis Pandis, K. Selçuk Candan,
and Sihem Amer-Yahia, editors,Companion of the
2023 International Conference on Management of
Data, SIGMOD/PODS 2023, Seattle, WA, USA,
June 18-23, 2023, pages 151–154. ACM, 2023.
doi:10.1145/3555041.3589723.
160 Alec Radford, Jong Wook Kim, Chris Hallacy,
Aditya Ramesh, Gabriel Goh, Sandhini Agarwal,
Girish Sastry, Amanda Askell, Pamela Mishkin,
Jack Clark, Gretchen Krueger, and Ilya Sut-
skever. Learning transferable visual models from
natural language supervision. In Marina Meila
and Tong Zhang, editors,Proceedings of the 38th
International Conference on Machine Learning,
volume 139 ofProceedings of Machine Learning
Research, pages 8748–8763. PMLR, 18–24 July
2021. URL: https://proceedings.mlr.press/
v139/radford21a.html.
161 Leonardo Ranaldi, Elena Sofia Ruzzetti, David A.
Venditti, Dario Onorati, and Fabio Massimo Zan-
zotto. A trip towards fairness: Bias and de-
biasing in large language models. ArXiv, 2023.
doi:10.48550/ARXIV.2305.13862.
162 Abhilasha Ravichander, Eduard Hovy, Kaheer
Suleman, Adam Trischler, and Jackie Chi Kit
Cheung. On the systematicity of probing con-
textualized word representations: The case of
hypernymy in BERT. In Joint Conference on
Lexical and Computational Semantics, pages 88–
102, 2020. URL: https://aclanthology.org/
2020.starsem-1.10/.
163 Simon Razniewski, Andrew Yates, Nora Kassner,
and Gerhard Weikum. Language models as or for
knowledge bases. CoRR, abs/2110.04888, 2021.
arXiv:2110.04888.
164 Leonardo F. R. Ribeiro, Martin Schmitt, Hinrich
Schütze, and Iryna Gurevych. Investigating pre-
trained language models for graph-to-text gen-
eration. Workshop on Natural Language Pro-
cessing for Conversational AI, abs/2007.08426,
2021. arXiv:2007.08426.
165 Petar Ristoski, Jessica Rosati, Tommaso Di Noia,
Renato De Leone, and Heiko Paulheim. Rdf2vec:
RDF graph embeddings and their applications.Se-
mantic Web, 10(4):721–752, 2019.doi:10.3233/
SW-180317.
166 Devendra Sachan, Yuhao Zhang, Peng Qi, et al.
Do syntax trees help pre-trained transformers ex-
TGDK

2:36 LLMs and KGs: Opportunities and Challenges
tract information? In EACL, pages 2647–2661,
apr 2021. doi:10.18653/V1/2021.EACL-MAIN.228.
167 Maarten Sap, Dallas Card, Saadia Gabriel, Yejin
Choi, and Noah A. Smith. The risk of racial
bias in hate speech detection. In ACL, 2019.
doi:10.18653/V1/P19-1163.
168 Timo Schick, Jane Dwivedi-Yu, Roberto
Dessì, Roberta Raileanu, Maria Lomeli, Luke
Zettlemoyer, Nicola Cancedda, and Thomas
Scialom. Toolformer: Language models can
teach themselves to use tools. In arXiv, 2023.
doi:10.48550/ARXIV.2302.04761.
169 Patrick Schramowski, Cigdem Turan, Nico Ander-
sen, et al. Large pre-trained language models con-
tain human-like biases of what is right and wrong
to do. Nature Machine Intelligence, 4(3):258–268,
2022. doi:10.1038/S42256-022-00458-8 .
170 Jingyu Shao, Qing Wang, Asiri Wijesinghe, and
Erhard Rahm. Ergan: Generative adversarial net-
works for entity resolution. InICDM, pages 1250–
1255, 2020. doi:10.1109/ICDM50108.2020.00158.
171 Jingchuan Shi, Jiaoyan Chen, Hang Dong, Ishita
Khan, Lizzie Liang, Qunzhi Zhou, Zhe Wu, and Ian
Horrocks. Subsumption prediction for e-commerce
taxonomies. In ESWC, pages 244–261, 2023.
doi:10.1007/978-3-031-33455-9_15 .
172 Peng Shi and Jimmy J. Lin. Simple BERT models
for relation extraction and semantic role labeling.
ArXiv, abs/1904.05255, 2019. URL:http://arxiv.
org/abs/1904.05255, arXiv:1904.05255.
173 Jaeho Shin, Sen Wu, Feiran Wang, Christopher
De Sa, Ce Zhang, and Christopher Ré. Incre-
mental knowledge base construction using deep-
dive. In VLDB, volume 8, page 1310, 2015.
doi:10.14778/2809974.2809991.
174 Taylor Shin, Yasaman Razeghi, Robert L. Lo-
gan IV, Eric Wallace, and Sameer Singh. Auto-
Prompt: Eliciting Knowledge from Language Mod-
els with Automatically Generated Prompts. In
EMNLP, pages 4222–4235, 2020.doi:10.18653/
V1/2020.EMNLP-MAIN.346.
175 Sneha Singhania, Tuan-Phong Nguyen, and Simon
Razniewski. LM-KBC: Knowledge base construc-
tion from pre-trained language models.Semantic
Web challenge, 2022. URL:https://ceur-ws.org/
Vol-3274/paper1.pdf.
176 Sneha Singhania, Simon Razniewski, and Gerhard
Weikum. Predicting Document Coverage for Rela-
tion Extraction. Transactions of the Association
for Computational Linguistics, 10:207–223, mar
2022. doi:10.1162/TACL_A_00456.
177 Xiaoqi Han snf Ru Li, Hongye Tan, Yuanlong
Wang, Qinghua Chai, and Jeff Z. Pan. Improving
Sequential Model Editing with Fact Retrieval. In
Findings of EMNLP, 2023.
178 Ran Song, Shizhu He, Shengxiang Gao, Li Cai,
Kang Liu, Zhengtao Yu, and Jun Zhao. Multilin-
gual knowledge graph completion from pretrained
language models with knowledge constraints. In
Findings of the Association for Computational
Linguistics: ACL 2023, pages 7709–7721, 2023.
doi:10.18653/V1/2023.FINDINGS-ACL.488.
179 Aarohi Srivastava et al. Beyond the imitation
game: Quantifying and extrapolating the cap-
abilities of language models. Transactions on
Machine Learning Research, 2023. URL: https:
//openreview.net/forum?id=uyTL5Bvosj.
180 Fabian M. Suchanek, Gjergji Kasneci, and Ger-
hard Weikum. Yago: A core of semantic know-
ledge. In Proceedings of the 16th International
Conference on World Wide Web, WWW ’07, pages
697–706, New York, NY, USA, 2007. Association
for Computing Machinery.doi:10.1145/1242572.
1242667.
181 Yoshihiko Suhara, Jinfeng Li, Yuliang Li, Dan
Zhang, Çağatay Demiralp, Chen Chen, and Wang-
Chiew Tan. Annotating columns with pre-trained
language models. InSIGMOD, pages 1493–1503,
2022. doi:10.1145/3514221.3517906.
182 Zequn Sun, Qingheng Zhang, Wei Hu, Cheng-
ming Wang, Muhao Chen, Farahnaz Akrami, and
Chengkai Li. A benchmarking study of embedding-
based entity alignment for knowledge graphs.
VLDB, 13(11):2326–2340, 2020. URL: http://
www.vldb.org/pvldb/vol13/p2326-sun.pdf.
183 Alexandre Tamborrino, Nicola Pellicano, Baptiste
Pannier, et al. Pre-training is (almost) all you
need: An application to commonsense reasoning.
ACL, 2020. doi:10.48550/arXiv.2004.14074.
184 Wang-Chiew Tan, Yuliang Li, Pedro Rodriguez,
Richard James, Xi Victoria Lin, Alon Halevy,
and Scott Yih. Reimagining retrieval augmen-
ted language models for answering queries. In
Findings of ACL, pages 6131–6146, 2023. doi:
10.18653/V1/2023.FINDINGS-ACL.382.
185 Niket Tandon and Gerard de Melo. Informa-
tion extraction from web-scale n-gram data. In
Web N-gram Workshop, volume 5803, pages 8–
15, 2010. URL:http://citeseerx.ist.psu.edu/
viewdoc/summary?doi=10.1.1.365.2318.
186 Niket Tandon, Gerard de Melo, Fabian M.
Suchanek, and Gerhard Weikum. Webchild: har-
vesting and organizing commonsense knowledge
from the web. Proceedings of the 7th ACM in-
ternational conference on Web search and data
mining, 2014. doi:10.1145/2556195.2556245.
187 Niket Tandon, Gerard de Melo, and Ger-
hard Weikum. Deriving a Web-scale common
sense fact database. In AAAI, pages 152–
157, 2011. URL: http://www.aaai.org/ocs/
index.php/AAAI/AAAI11/paper/view/3764, doi:
10.1609/AAAI.V25I1.7841.
188 Nan Tang, Ju Fan, Fangyi Li, Jianhong Tu, Xiaoy-
ong Du, Guoliang Li, Sam Madden, and Mourad
Ouzzani. Rpt: relational pre-trained transformer
is almost all you need towards democratizing data
preparation. VLDB, 2021.doi:10.14778/3457390.
3457391.
189 Ruixiang Tang, Xiaotian Han, Xiaoqian Jiang,
and Xia Hu. Does synthetic data generation of
LLMs help clinical text mining? ArXiv, 2023.
doi:10.48550/ARXIV.2303.04360.
190 Nicolas Tempelmeier, Elena Demidova, and Stefan
Dietze. Inferring missing categorical information
in noisy and sparse web markup. InWWW, 2018.
doi:10.1145/3178876.3186028.
191 Hugo Touvron, Thibaut Lavril, Gautier Izacard,
Xavier Martinet, Marie-Anne Lachaux, Timothée
Lacroix, Baptiste Rozière, Naman Goyal, Eric
Hambro, Faisal Azhar, et al. Llama: Open and

Jeff Z. Pan et al. 2:37
efficient foundation language models.arXiv, 2023.
doi:10.48550/ARXIV.2302.13971.
192 Pat Verga, Haitian Sun, Livio Baldini Soares, et al.
Facts as experts: Adaptable and interpretable
neural memory over symbolic knowledge.NAACL,
2021. arXiv:2007.00849.
193 Blerta Veseli, Sneha Singhania, Simon Razniewski,
and Gerhard Weikum. Evaluating language models
for knowledge base completion. InThe Semantic
Web – 20th International Conference, ESWC 2023,
Hersonissos, Crete, Greece, May 28 – June 1,
2023, Proceedings, volume 13870 ofLecture Notes
in Computer Science, pages 227–243. Springer,
2023. doi:10.1007/978-3-031-33455-9_14 .
194 Liane Vogel, Benjamin Hilprecht, and Carsten Bin-
nig. Towards foundation models for relational data-
bases [vision paper]. TRL@NeurIPS2022, 2023.
doi:10.48550/ARXIV.2305.15321.
195 Pavlos Vougiouklis, Nikos Papasarantopoulos,
Danna Zheng, David Tuckey, Chenxin Diao, Zhili
Shen, and Jeff Z. Pan. FastRAT: Fast and Efficient
Cross-lingual Text-to-SQL Semantic Parsing. In
Proc. of IJCNLP-AACL 2023, 2023.
196 Denny Vrandečić and Markus Krötzsch. Wikidata:
A free collaborative knowledgebase. Commun.
ACM, 57:78–85, sep 2014.doi:10.1145/2629489.
197 David Wadden, Ulme Wennberg, Yi Luan, and
Hannaneh Hajishirzi. Entity, relation, and event
extraction with contextualized span representa-
tions. In Proceedings of the 2019 Conference
on Empirical Methods in Natural Language Pro-
cessing and the 9th International Joint Confer-
ence on Natural Language Processing (EMNLP-
IJCNLP), pages 5784–5789, Hong Kong, China,
nov 2019. Association for Computational Linguist-
ics. doi:10.18653/V1/D19-1585.
198 Bin Wang, Guangtao Wang, Jing Huang, Jiaxuan
You, Jure Leskovec, and C.-C. Jay Kuo. Inductive
learning on commonsense knowledge graph com-
pletion. In Joint Conference on Neural Networks,
pages 1–8, 2021. doi:10.1109/IJCNN52387.2021.
9534355.
199 Bo Wang, Tao Shen, Guodong Long, Tianyi Zhou,
Ying Wang, and Yi Chang. Structure-augmented
text representation learning for efficient knowledge
graph completion. In WWW, pages 1737–1748,
2021. doi:10.1145/3442381.3450043.
200 Liang Wang, Wei Zhao, Zhuoyu Wei, and Jing-
ming Liu. SimKGC: Simple Contrastive Know-
ledge Graph Completion with Pre-trained Lan-
guage Models. In ACL, pages 4281–4294, may
2022. doi:10.18653/V1/2022.ACL-LONG.295.
201 Xiao Wang, Wei Zhou, Can Zu, Han Xia,
Tianze Chen, Yuan Zhang, Rui Zheng, Junjie Ye,
Qi Zhang, Tao Gui, Jihua Kang, J. Yang, Siyuan
Li, and Chunsai Du. Instructuie: Multi-task in-
struction tuning for unified information extraction.
ArXiv, 2023. doi:10.48550/ARXIV.2304.08085.
202 Xiaozhi Wang, Tianyu Gao, Zhaocheng Zhu,
Zhengyan Zhang, Zhiyuan Liu, Juanzi Li, and
Jian Tang. Kepler: A unified model for knowledge
embedding and pre-trained language representa-
tion. TACL, 9:176–194, 2021.doi:10.1162/TACL_
A_00360.
203 Xiyu Wang and Nora El-Gohary. Deep learning-
based relation extraction and knowledge graph-
based representation of construction safety require-
ments. Automation in Construction, 147:104696,
2023. doi:10.1016/j.autcon.2022.104696.
204 Jason Wei, Xuezhi Wang, Dale Schuurmans,
Maarten Bosma, Ed Huai hsin Chi, F. Xia, Quoc
Le, and Denny Zhou. Chain of thought prompting
elicits reasoning in large language models.ArXiv,
abs/2201.11903, 2022. arXiv:2201.11903.
205 Xiang Wei, Xingyu Cui, Ning Cheng, Xiaobin
Wang, Xin Zhang, Shen Huang, Pengjun Xie,
Jinan Xu, Yufeng Chen, Meishan Zhang, Yong
Jiang, and Wenjuan Han. Zero-shot information
extraction via chatting with chatgpt.ArXiv, 2023.
doi:10.48550/ARXIV.2302.10205.
206 Gerhard Weikum, Luna Dong, Simon Razniewski,
and Fabian M. Suchanek. Machine knowledge:
Creation and curation of comprehensive know-
ledge bases. CoRR, abs/2009.11564, 2020.arXiv:
2009.11564.
207 Joseph Weizenbaum. Eliza—a computer program
for the study of natural language communication
between man and machine.Communications of
the ACM, 1966. doi:10.1145/365153.365168.
208 Peter West, Chandra Bhagavatula, Jack Hessel,
Jena D Hwang, Liwei Jiang, Ronan Le Bras, Xim-
ing Lu, Sean Welleck, and Yejin Choi. Sym-
bolic knowledge distillation: from general lan-
guage models to commonsense models. arXiv
preprint arXiv:2110.07178, 2021. doi:10.48550/
arXiv.2110.07178.
209 Shijie Wu, Ozan Irsoy, Steven Lu, Vadim Dabravol-
ski, Mark Dredze, Sebastian Gehrmann, Prabhan-
jan Kambadur, David S. Rosenberg, and Gideon
Mann. Bloomberggpt: A large language model
for finance. CoRR, abs/2303.17564, 2023. doi:
10.48550/ARXIV.2303.17564.
210 Guohui Xiao, Diego Calvanese, Roman
Kontchakov, Domenico Lembo, Antonella
Poggi, Riccardo Rosati, and Michael Za-
kharyaschev. Ontology-based data access: A
survey. In IJCAI, pages 5511–5519, 2018.
doi:10.24963/IJCAI.2018/777.
211 Wenjie Xu, Ben Liu, Miao Peng, Xu Jia, and Min
Peng. Pre-trained language model with prompts
for temporal knowledge graph completion. InFind-
ings of ACL 2023, 2023. doi:10.18653/V1/2023.
FINDINGS-ACL.493.
212 Yan Xu, Mahdi Namazifar, Devamanyu Hazarika,
Aishwarya Padmakumar, Yang Liu, and Dilek
Hakkani-Tür. KILM: knowledge injection into
encoder-decoder language models. In Anna Ro-
gers, Jordan L. Boyd-Graber, and Naoaki Okazaki,
editors, Proceedings of the 61st Annual Meet-
ing of the Association for Computational Lin-
guistics (Volume 1: Long Papers), ACL 2023,
Toronto, Canada, July 9-14, 2023, pages 5013–
5035. Association for Computational Linguistics,
2023. doi:10.18653/V1/2023.ACL-LONG.275.
213 Linyao Yang, Hongyang Chen, Zhao Li, Xiao Ding,
and Xindong Wu. Chatgpt is not enough: Enhan-
cing large language models with knowledge graphs
for fact-aware language modeling. arXiv, 2023.
doi:10.48550/ARXIV.2306.11489.
TGDK

2:38 LLMs and KGs: Opportunities and Challenges
214 Nan Yang, Tao Ge, Liang Wang, Binxing Jiao,
Daxin Jiang, Linjun Yang, Rangan Majumder,
and Furu Wei. Inference with reference: Lossless
acceleration of large language models. InarXiv,
2023. doi:10.48550/ARXIV.2304.04487.
215 Xi Yang, Aokun Chen, Nima PourNejatian,
Hoo Chang Shin, Kaleb E. Smith, Christopher Par-
isien, Colin Compas, Cheryl Martin, Anthony B.
Costa, Mona G. Flores, Ying Zhang, Tanja Ma-
goc, Christopher A. Harle, Gloria Lipori, Duane A.
Mitchell, William R. Hogan, Elizabeth A. Shen-
kman, Jiang Bian, and Yonghui Wu. A large
language model for electronic health records.npj
Digital Medicine, 5(1):194, 2022. doi:10.1038/
S41746-022-00742-2 .
216 Liang Yao, Chengsheng Mao, and Yuan Luo. Kg-
bert: Bert for knowledge graph completion.arXiv,
2019. doi:10.48550/arXiv.1909.03193.
217 Michihiro Yasunaga, Hongyu Ren, Antoine Bos-
selut, Percy Liang, and Jure Leskovec. Qa-gnn:
Reasoning with language models and knowledge
graphs for question answering. NAACL, 2021.
doi:10.18653/V1/2021.NAACL-MAIN.45.
218 Wen-tau Yih, Ming-Wei Chang, Xiaodong He,
and Jianfeng Gao. Semantic parsing via staged
query graph generation: Question answering with
knowledge base. In Proceedings of the 53rd An-
nual Meeting of the Association for Computa-
tional Linguistics and the 7th International Joint
Conference on Natural Language Processing of
the Asian Federation of Natural Language Pro-
cessing, ACL 2015, July 26-31, 2015, Beijing,
China, Volume 1: Long Papers, pages 1321–1331,
2015. doi:10.3115/V1/P15-1128.
219 Donghan Yu, Chenguang Zhu, Yuwei Fang, Wen-
hao Yu, Shuohang Wang, Yichong Xu, Xiang Ren,
Yiming Yang, and Michael Zeng. Kg-fid: In-
fusing knowledge graph in fusion-in-decoder for
open-domain question answering. InACL, 2022.
doi:10.18653/V1/2022.ACL-LONG.340.
220 Ran Yu, Ujwal Gadiraju, Besnik Fetahu, Oliver
Lehmberg, Dominique Ritze, and Stefan Dietze.
Knowmore – knowledge base augmentation with
structured web markup.Semantic Web, 10(1):159–
180, 2019. doi:10.3233/SW-180304.
221 Qingkai Zeng, Jinfeng Lin, Wenhao Yu, Jane
Cleland-Huang, and Meng Jiang. Enhancing tax-
onomy completion with concept generation via
fusing relational representations. InKDD, pages
2104–2113, 2021. doi:10.1145/3447548.3467308.
222 Hanwen Zha, Zhiyu Chen, and Xifeng Yan. In-
ductive relation prediction by bert. In AAAI,
volume 36, pages 5923–5931, 2022.doi:10.1609/
AAAI.V36I5.20537.
223 Chaoning Zhang, Chenshuang Zhang, Sheng
Zheng, Yu Qiao, Chenghao Li, Mengchun Zhang,
Sumit Kumar Dam, Chu Myaet Thwal, Ye Lin
Tun, Le Luang Huy, Donguk kim, Sung-Ho Bae,
Lik-Hang Lee, Yang Yang, Heng Tao Shen, In-
So Kweon, and Choong-Seon Hong. A com-
plete survey on generative ai (aigc): Is chatgpt
from gpt-4 to gpt-5 all you need?ArXiv, 2023.
doi:10.48550/ARXIV.2303.11717.
224 Meiru Zhang, Yixuan Su, Zaiqiao Meng, Zihao
Fu, and Nigel Collier. COFFEE: a contrastive
oracle-free framework for event extraction.ArXiv,
abs/2303.14452, 2023. doi:10.48550/ARXIV.2303.
14452.
225 Rui Zhang, Bayu Distiawan Trisedya, Miao
Li, Yong Jiang, and Jianzhong Qi. A bench-
mark and comprehensive survey on knowledge
graph entity alignment via representation learn-
ing. VLDB J., 31(5):1143–1168, 2022. doi:
10.1007/S00778-022-00747-Z .
226 Ruichuan Zhang and Nora El-Gohary.
Transformer-based approach for automated
context-aware IFC-regulation semantic informa-
tion alignment. Automation in Construction, 145,
2023. doi:10.1016/j.autcon.2022.104540.
227 Zhiyuan Zhang, Xiaoqian Liu, Yi Zhang, Qi Su,
Xu Sun, and Bin He. Pretrain-kge: Learning
knowledge representation from pretrained lan-
guage models. In EMNLP Findings, 2020. doi:
10.18653/V1/2020.FINDINGS-EMNLP.25.
228 Ziheng Zhang, Hualuo Liu, Jiaoyan Chen, Xi Chen,
Bo Liu, Yuejia Xiang, and Yefeng Zheng. An
industry evaluation of embedding-based entity
alignment. In COLING, pages 179–189, 2020.
doi:10.18653/V1/2020.COLING-INDUSTRY.17.
229 Ruochen Zhao, Xingxuan Li, Shafiq Joty, Cheng-
wei Qin, and Lidong Bing. Verify-and-edit: A
knowledge-enhanced chain-of-thought framework.
In Anna Rogers, Jordan Boyd-Graber, and Na-
oaki Okazaki, editors, Proceedings of the 61st
Annual Meeting of the Association for Compu-
tational Linguistics (Volume 1: Long Papers),
pages 5823–5840, Toronto, Canada, jul 2023. As-
sociation for Computational Linguistics. doi:
10.18653/V1/2023.ACL-LONG.320.
230 Zexuan Zhong and Danqi Chen. A frustrat-
ingly easy approach for entity and relation ex-
traction. In Proceedings of the 2021 Confer-
ence of the North American Chapter of the As-
sociation for Computational Linguistics: Human
Language Technologies, pages 50–61, Online, jun
2021. Association for Computational Linguistics.
doi:10.18653/V1/2021.NAACL-MAIN.5.
231 Zexuan Zhong, Dan Friedman, and Danqi Chen.
Factual probing is [mask]: Learning vs. learning to
recall. In NAACL, 2021. doi:10.18653/V1/2021.
NAACL-MAIN.398.
232 Wenxuan Zhou, Fangyu Liu, Ivan Vulic, Nigel Col-
lier, and Muhao Chen. Prix-lm: Pretraining for
multilingual knowledge base construction. InACL,
2021. doi:10.48550/arXiv.2110.08443.
233 Yongchao Zhou, Andrei Ioan Muresanu, Ziwen
Han, Keiran Paster, Silviu Pitis, Harris Chan, and
Jimmy Ba. Large language models are human-
level prompt engineers. In arXiv, 2023. doi:
10.48550/ARXIV.2211.01910.
234 Qi Zhu, Hao Wei, Bunyamin Sisman, Da Zheng,
Christos Faloutsos, Xin Luna Dong, and Jia-
wei Han. Collective multi-type entity alignment
between knowledge graphs. InWWW, pages 2241–
2252, 2020. doi:10.1145/3366423.3380289.
235 Yuqi Zhu, Xiaohan Wang, Jing Chen, Shuofei Qiao,
Yixin Ou, Yunzhi Yao, Shumin Deng, Huajun
Chen, and Ningyu Zhang. Llms for knowledge
graph construction and reasoning: Recent cap-
abilities and future opportunities. arXiv, 2023.
doi:10.48550/ARXIV.2305.13168.
```
