---
title: "QA2Explanation: Generating and Evaluating Explanations for Question Answering Systems over Knowledge Graph"
author: Saeedeh Shekarpour, Abhishek Nadgeri, Kuldeep Singh
year: "2020"
Type: Proceedings Article
DOI: 10.18653/v1/2020.intexsempar-1.1
source: https://doi.org/10.18653/v1/2020.intexsempar-1.1
created: 2026-04-30
description: ""
tags:
  - op/acc/pending-review
pdfORepub: "[[QA2Explanation Generating and Evaluating Explanations for Question Answering Systems over Knowledge Graph.pdf]]"
---
[[QA2Explanation Generating and Evaluating Explanations for Question Answering Systems over Knowledge Graph.pdf]]
## Full text (extracted from `QA2Explanation Generating and Evaluating Explanations for Question Answering Systems over Knowledge Graph.pdf`)

*Source:* `2PDF/QA2Explanation Generating and Evaluating Explanations for Question Answering Systems over Knowledge Graph.pdf`  
*Extracted:* 2026-04-30

```text
Proceedings of the First Workshop on Interactive and Executable Semantic Parsing, pages 1–11
Online, November 19, 2020.c⃝2020 Association for Computational Linguistics
https://doi.org/10.18653/v1/P17
1
QA2Explanation: Generating and Evaluating Explanations for Question
Answering Systems over Knowledge Graph
Saeedeh Shekarpour
University of Dayton
Dayton, USA
sshekarpour1
@udayton.edu
Abhishek Nadgeri
RWTH Aachen &
Zerotha Research, Germany
abhishek.nadgeri
@rwth-aachen.de
Kuldeep Singh
Cerence GmbH &
Zerotha Research, Germany
kuldeep.singh1
@cerence.com
Abstract
In the era of Big Knowledge Graphs, Ques-
tion Answering (QA) systems have reached
a milestone in their performance and feasibil-
ity. However, their applicability, particularly
in speciﬁc domains such as the biomedical do-
main, has not gained wide acceptance due to
their “black box” nature, which hinders trans-
parency,fairness,andaccountabilityofQAsys-
tems. Therefore,usersareunabletounderstand
howandwhyparticularquestionshavebeenan-
swered, whereas some others fail. To address
this challenge, in this paper, we develop an au-
tomatic approach for generating explanations
during various stages of a pipeline-based QA
system. Ourapproachisasupervisedandauto-
matic approach which considers three classes
(i.e.,success,noanswer,andwronganswer)for
annotating the output of involved QA compo-
nents. Upon our prediction, a template expla-
nation is chosen and integrated into the output
of the corresponding component. To measure
theeﬀectivenessoftheapproach,weconducted
a user survey as to how non-expert users per-
ceive our generated explanations. The results
of our study show a signiﬁcant increase in the
four dimensions of the human factor from the
Human-computer interaction community.
1 Introduction
The recent advances of Question Answering (QA)
technologies mostly rely on (i) the advantages of
Big Knowledge Graphs which augment the seman-
tics, structure, and accessibility of data,e.g.,Web
of Data has published around 150B triples from a
varietyofdomains 1,and(ii)thecompetencyofcon-
temporary AI approaches which train sophisticated
learning models (statistical models (Shekarpour
et al., 2015, 2013), neural networks (Lukovnikov
et al., 2017), and attention models (Liu, 2019)) on
a large size of training data, and given a variety of
1http://lodstats.aksw.org/
novel features captured from semantics, structure,
and context of the background data. However, sim-
ilar to other branches of AI applications, the state
of the art of QA systems are“black boxes”that
fail to provide transparent explanations about why
a particular answer is generated. This black box
behavior diminishes the conﬁdence and trust of the
user and hinders the reliance and acceptance of the
black-box systems, especially in critical domains
such as healthcare, biomedical, life-science, and
self-driving cars (Samek et al., 2017; Miller, 2018).
Therunning hypothesisinthispaperisthatthelack
ofexplanationforanswersprovidedbyQAsystems
diminishes the trust and acceptance of the user to-
wards these systems. Therefore, by implementing
more transparent, interpretable, or explainable QA
systems, the end users will be better equipped to
justifyandthereforetrustthe outputof QAsystems
(Li et al., 2018).
Furthermore, data quality is a critical factor
that highly aﬀects the performance of QA sys-
tems. In other words, when the background data
is ﬂawed or outdated, it undermines the human-
likeness and acceptance of the QA systems if no
explanation is provided, especially for non-expert
users. For example, the SINA engine (Shekarpour
et al., 2015) failed to answer the simple question
“What is the population of Canada?”on the DB-
pedia (Auer et al., 2007) version 2013, whereas it
succeeded for similar questions such as“What is
the population of Germany?”. The error analysis
showedthattheexpectedtriple i.e.,<dbr2:Canada
dbo3:population "xxx"> is missing from DB-
pedia 2013. Thus, if the QA system does not
provide any explanation about such failures, then
the non-expert user concludes the QA system into
the demerit points. Thus, in general, the errors or
2dbr is bound tohttp://dbpedia.org/resource/.
3The preﬁx dbo is bound to http://dbpedia.org/
ontology/.

2
failures of the QA systems might be caused by the
inadequacies of the underlying data or misunder-
standing, misinterpretation, or miscomputation of
theemployedcomputationalmodels. Ineithercase,
the black-box QA system does not provide any ex-
planationsregardingthesourcesoftheerror. Often
theresearchcommunityobsesseswiththetechnical
discussionofQAsystemsandcompetesonenhanc-
ing the performance of the QA systems, whereas,
on the downside of the QA systems, there is a hu-
man who plays a vital role in the acceptance of the
system. The Human-Computer Interaction (HCI)
community already targeted various aspects of the
human-centered design and evaluation challenges
of black-box systems. However, the QA systems
over KGs received the least attention comparing to
otherAIapplicationssuchasrecommendersystems
(Herlocker et al., 2000; Kouki et al., 2017).
MotivationandApproach: PlethoraofQAsys-
tems over knowledge graphs developed in the last
decade (Höﬀner et al., 2017). These QA systems
are evaluated on various benchmarking datasets in-
cludingWebQuestions(Berantetal.,2013),QALD
(Unger et al., 2015), LC-QuAD (Trivedi et al.,
2017),andreportresultsbasedonglobalmetricsof
precision, recall, and F-score. In many cases, QA
approaches over KGs even surpass the human level
performance (Petrochuk and Zettlemoyer, 2018).
Irrespective of the underlying technology and algo-
rithms, these QA systems act as black box and do
not provide any explanation to the user regarding
1) why a particular answer is generated and 2) how
the given answer is extracted from the knowledge
source. Therecentworkstowardsexplainableartiﬁ-
cial intelligence (XAI) gained momentum because
several AI applications ﬁnd limited acceptance due
to ethical reasons (Angwin et al., 2016) and a lack
oftrustonbehalfoftheirusers(Stubbsetal.,2007).
The same rationale is also applicable to the black-
box QA systems. Research studies showed that
representing adequate explanations to the answer
brings acceptability and conﬁdence to the user as
observed in various domains such as recommender
systems and visual question answering (Herlocker
etal.,2000;HayesandShah,2017;Hendricksetal.,
2016; Wu and Mooney, 2018). In this paper, we
argue that having explanations increases the trust-
worthiness, transparency, and acceptance of the
answers of the QA system over KGs. Especially,
when the QA systems fail to answer a question or
provide a wrong answer, the explanatory output
helps to keep the user informed about a particular
behavior. Hence, we propose a template-based ex-
planationgenerationapproachforQAsystems. Our
proposed approach for explainable QA system over
KGprovides(i) adequatejustiﬁcation: thustheend
user feels that they are aware of the reasoning steps
of the computational model, (ii)conﬁdence: the
user can trust the system and has the willing for the
continuation of interactions, (iii)understandability:
educates the user as how the system infers or what
are the causes of failures and unexpected answers,
and (iv) user involvement: encourages the user
to engage in the process of QA such as question
rewriting.
Research Questions: We deal with two key
research questions about the explanations of the
QA systems as follows:RQ1: What is an eﬀective
model and scheme for automatically generating
explanations? The computational model employed
in a QA system might be extremely complicated.
The exposure of the depth of details will not be
suﬃcient for the end user. The preference is to
generate natural language explanations that are
readable and understandable to the non-expert user.
RQ2: How is the perception of end users about
explanations along the human factor dimensions?,
which is whether or not the explanations establish
conﬁdence,justiﬁcation,understanding,andfurther
engagements of the user.
Our key contributions are: 1) a scheme for shal-
low explanatory QA pipeline systems, 2) a method
for automatically generating explanations, and 3) a
user survey to measure the human factors of user
perception from explanations. This paper is or-
ganized as follows: In Section 2, we review the
relatedwork. Section3explainsthemajorconcepts
of the QA pipeline system, which is our employed
platform. Section 4 provides our presentation and
detailed discussion of the proposed approach. Our
experimental study is presented in Section 5, fol-
lowed by a discussion Section. We conclude the
paper in section 7.
2 Related Work
Researchershavetackledtheproblemofquestionan-
swering in various domains including open domain
question answering (Yang et al., 2019), biomedi-
cal (Bhandwaldar and Zadrozny, 2018), geospatial
(Punjani et al., 2018), and temporal (Jia et al.,
2018). Question answering over publicly available
KGs is a long-standing ﬁeld with over 62 QA sys-

3
tems developed since 2010 (Höﬀner et al., 2017).
The implementation of various QA systems can be
broadly categorized into three approaches (Singh,
2019;Diefenbachetal.,2018). Theﬁrstisaseman-
tic parsing based approach such as (Usbeck et al.,
2015) that implements a QA system using several
linguistic analyses (e.g., POS tagging, dependency
parsing) and linked data technologies. The second
approach is an end-to-end machine learning based,
whichusesalargeamountoftrainingdatatomapan
input question to its answer directly (e.g., in (Yang
etal.,2019;Lukovnikovetal.,2017)). Thethirdap-
proachisbasedonmodularframeworks(Kimetal.,
2017; Singh et al., 2018b) which aims at reusing
individual modules of QA systems, independent
tools (such as entity linking, predicate linking) in
building QA systems collaboratively. Irrespective
of the implementation approach, domain, and the
underlying knowledge source (KG, documents, re-
lational tables, etc.), the majority of existing QA
systemsactasablackbox. Thereasonbehindblack
box behavior is due to either the monolithic tightly
coupledmodulessuchasinsemanticparsingbased
QA systems or nested and nonlinear structure of
machine learning based algorithms employed in
QA systems. The modular framework, on the other
hand, provides ﬂexibility to track individual stages
of the answer generation process. The rationale
behind our choice of the modular framework over
monolithic QA systems is a ﬂexible architecture
design of such frameworks. It allows us to trace
failure at each stage of the QA pipeline. We enrich
the output of each step with adequate justiﬁcation
with supporting natural language explanation for
the user. Hence, as the ﬁrst step towards explain-
able QA over knowledge graphs, we propose an
automatic approach for generating a description
for each stage of a QA pipeline in a state-of-the-
art modular framework (in our case: Frankenstein
(Singh et al., 2018b)). We are not aware of any
work in the direction of explainable question an-
swering over knowledge graphs and we make the
ﬁrst attempt in this paper. Although, eﬀorts have
been made to explain visual question answering
systems. Someworksgeneratetextualexplanations
for VQA by training a recurrent neural network
(RNN) to mimic examples of human descriptions
(Hendricks et al., 2016; Wu and Mooney, 2018)
directly. Theworkby(NgongaNgomoetal.,2013)
can be considered a closest attempt to our work.
The authors proposed a template based approach
to translate SPARQL queries into natural language
verbalization. We employ a similar template-based
approach to generate an automatic explanation for
QA pipelines.
In other domains, such as expert systems, the
earlier attempts providing explanations to the users
can be traced back in the early 70s (Shortliﬀe,
1974). Since then, extensive work has been done
to include explanations in expert systems followed
by recommender systems to explain the system’s
knowledge of the domain and the reasoning pro-
cesses these systems employ to produce results (for
details, please refer to (Moore and Swartout, 1988;
Jannach et al., 2010; Daher et al., 2017). For a rec-
ommender system, work by (Herlocker et al., 2000)
is an early attempt to evaluate diﬀerent implemen-
tations of explanation interfaces in "MovieLens"
recommender system. Simple statements provided
to the customers as explanations mentioning the
similarity to other highly rated ﬁlms or a favorite
actor or actress were among the best recommen-
dations of the MovieLens system compared to the
unexplainedrecommendations. Furthermore,appli-
cationsofexplanationarealsoconsideredinvarious
sub-domains of artiﬁcial intelligence, such as justi-
fying medical decision-making (Fox et al., 2007),
explaining autonomous agent behavior (Hayes and
Shah, 2017), debugging of machine learning mod-
els(Kuleszaetal.,2015),andexplainingpredictions
of classiﬁers (Ribeiro et al., 2016).
3 QA Pipeline on Knowledge Graph
One of the implementation approaches for
answering questions from interlinked knowledge
graphs is typically a multi-stage process which is
called QA pipeline (Singh et al., 2018b). Each
stage of the pipeline deals with a required task
such as Named Entity Recognition (NER) and
Disambiguation (NED) (referred as Entity Linking
(EL)), Relation extraction and Linking (RL), and
Query Building (QB). There is an abundance of
components performing QA tasks (Diefenbach
et al., 2018). These implementations run on the
KGs and have been developed based on AI, NLP,
and Semantic Technologies, which accomplish one
or more tasks of a QA pipeline (Höﬀner et al.,
2017). Table 1 (Singh et al., 2018b) presents
performance of best QA components on the
LC-QuAD dataset, implementing QA tasks. The
components are Tag Me API (Ferragina and
Scaiella, 2010)) for NED, RL (Relation Linking)

4
implemented by RNLIWOD4 and SPARQL query
builder by NLIWOD QB5). For example, given
the question “Did Tesla win a nobel prize in
physics?”, the ideal NED component is expected
to recognize the keyword “Tesla” as a named
entity and map it to the corresponding DBpedia
resource, i.e.dbr:Nikola_Tesla. Similarly, the
multi-word unit“nobel prize in physics”has to
be linked to dbr:Nobel_Prize_in_Physics.
Thereafter, a component performing RL ﬁnds
embedded relations in the given question and
links them to appropriate relations of the un-
derlying knowledge graph. In our example,
the keyword “win” is mapped to the relation
dbo:award. Finally, the QB component generates
a formal query (e.g. expressed in SPARQL)
(i.e. ASK {dbr:Nikola_Tesla dbo:award
dbr:Nobel_Prize_in_Physics.}). The per-
formance values in Table 1 are averaged over the
entire query inventory.
Table1: PerformanceofQAcomponentsimplementing
various QA tasks on LC-QuAD dataset.
QA Component QA Task Precision Recall F-Score
TagMe NED 0.69 0.66 0.67
RNLIWOD RL 0.25 0.22 0.23
NLIWOD QBQB 0.48 0.49 0.48
4 Approach
A full QA pipeline is required to answer a
given questionq. Such QA pipelines are com-
posed of all the required components perform-
ing necessary tasks to transform a user-supplied
natural language (NL) question into a formal
query language (i.e., SPARQL). We consider
three generic classes for outputs of a full QA
pipeline or individual components, namelyOc =
{Success ,NoAns wer,Wron gAnswer}. Concern-
ing a given question, a “success” class is when the
QA pipeline (component) successfully provides a
correct output, a “No Answer” class happens when
the full QA pipeline (or an individual component)
does not return any output and “Wrong Answer”
class is when the provided output is incorrect.
To addressRQ1, we introduce a scheme for gen-
erating explanations for the QA pipeline system.
This scheme produces shallow, however automatic
4Component is similar to Relation Linker ofhttps://
github.com/dice-group/NLIWOD
5Component is based on https://github.com/
dice-group/NLIWOD and (Unger et al., 2012).
explanations using a semi-supervised approach for
generating individual explanations after running
eachintegratedcomponent. Inourproposedmodel,
the class of the output of each integrated com-
ponent is predicted using a supervised learning
approach. We train a classiﬁer per component
within the pipeline. Then based on the prediction
of the classiﬁer, an explanation template is chosen.
The explanation template and the output of the
component are incorporated to form the ﬁnal rep-
resentation of explanations. We have a repository
of explanation templates for each component of the
QApipelinesystem. Forexample,theNEDcompo-
nent corresponds to several explanation templates
diﬀeringbasedonthenumberoftheoutputentities.
Precisely, the explanation template when the NED
has one single entity is diﬀerent from when it has
two or three. Moreover, the templates vary based
on the Part of Speach (POS) tag of the entities rec-
ognized in the input question. For example, Figure
1 shows a pipeline containing three components:
1) NED component: TagMe, 2) RL component:
RNLIWOD QB, and 3) QB component: NLIWOD
QB. Three classiﬁers were individually trained for
each component. In this example, for the given
question“Did Tesla win a nobel prize in physics?”
the classiﬁers predicted the class of “Success” for
NED and the class "No Answer" for RL and QB
components. Thus,theexplanationtemplatescorre-
spondingtotheclassof“success”forNED,and"No
Answer"forRLandQBareﬁltered. Thensincethe
NED component has two outputs, therefore, two
explanations were generated for NED, whereas the
remaining components show one explanation.
4.1 Predicting Output of Components
The set of necessary QA tasks formalized as
T = {t1,t2,..., tn}suchasNED,RL,andQB.Each
task(ti ∶q∗→ q+)transformsagivenrepresentation
q∗of a questionq into another representationq+.
For example, NED and RL tasks transform the in-
putrepresentation “WhatisthecapitalofFinland?”
into the representation“What is thedbo:capital
of dbr:Finland?”. The entire set of QA com-
ponents is denoted byC = {C1,C2,..., Cm}. Each
componentCj solves one single QA task;Cti
j cor-
respondstotheQAtask ti inT implementedby Cj .
For example, RNLIWOD implements the relation
linking QA task, i.e.RNLIWODRL. Letρ(Cj ) de-
note the performance of a QA component, then our
key objective is to predict the likelihood ofρ(Cj )

5
Pipeline QA
NED
T agMe 
RE
RNLIWOD 
QA
NLIWOD 
QB 
 Answer: NULLQ1: Did Tesla win a nobel 
prize in physics?
X2: TAGME identiﬁes the word Tesla as the subject in the
question. The subject is mapped to the DBpedia concept
dbr:Nicole Tesla.
X1: TAGME identiﬁes the multiword "nobel prize in physics"
as the entity in the question. The entity is mapped to the
DBpedia concept dbr:Nobel Prize in Physics.
X3: RNLIWOD could not recognize any predicate in
the question, hence there is no mapping to any
concepts of the DBpedia knowledge graph.
X4: NLIWOD QB cannot formulate any query
to extract the ﬁnal answer, and the answer to
this question is NULL
Figure 1: The QA pipeline generates the explanations in various stages of running; each explanation is generated
per output of each integrated component. The demonstrated pipeline contains three components, i.e., NED, RL,
and QB; the output(s) of each one is integrated into an explanation template and represented to the end user.
for a given representationq∗ of q, a taskti, and
an underlying knowledge graphλ. This is denoted
as Pr(ρ(Cj )/divides.alt0q∗,ti,λ). In this work, we assume
a single knowledge graph (i.e. DBpedia); thus,λ
is considered a constant parameter that does not
impact the likelihood leading to:
Pr(ρ(Cj )/divides.alt0q∗,ti) = Pr(ρ(Cj )/divides.alt0q∗,ti,λ) (1)
Further, we assume that the given representation
q∗is equal to the initial input representationq for
all the QA components, i.e.q∗= q.
Solution Suppose we are given a set of NL ques-
tions Q with the detailed results of performance
for each component per task. We can then model
the prediction goalPr(ρ(Cj )/divides.alt0q,ti) as a supervised
learning problem on a training set, i.e. a set of
questions Q and a set of labelsL representing
the performance ofCj for a questionq and a task
ti. In other words, for each individual taskti and
componentCj , the purpose is to train a supervised
model that predicts the performance of the given
component Cj for a given questionq and taskti
leveraging the training set. If/divides.alt0T /divides.alt0= n and each
task is performed bym components, and the QA
pipeline integrates all then × m components, then
n × m individual learning models have to be built
up.
Question Features. Since the input questionq
has a textual representation, it is necessary to au-
tomatically extract suitable features, i.e.F(q) =
(f1,..., fr ). In order to obtain an abstract and con-
crete representation of NL questions, we reused
question features proposed by (Singh et al., 2018b,
2019) which impact the performance of the QA
systems. These features are: question length,
answer type (list, number, boolean), Wh-word
(who,what,which,etc.), and POS tags present in
a question. Please note, our contribution is not the
underlying Frankenstein framework, we reused it
for the completion of the approach. Our contribu-
tion is to add valid explanation to each step of the
QA pipeline, and empirical study to support our
hypothesis.
NED
Classiﬁer Classiﬁer Classiﬁer 
RE QA
Input 
Question
Explanation Explanation Explanation 
  Answer
Explanation 
Templates
Figure2: Thisﬁguresketchesatopoverviewofourap-
proach. Thereisaclassiﬁerforeachcomponent,which
predicts the output of the associated component. Also,
thereisarepositoryoftheexplanationtemplates. Thus,
based on the prediction of the classiﬁer and the actual
output of the component, a suitable template is ﬁltered.
For ﬁnal explanation, the output of the component was
incorporated into the template.
4.2 Methodology
Figure 2 shows the architecture of our approach.
Initially, a pipeline for a QA system is built up; in
ourcaseweusedFrankensteinplatform(Singhetal.,
2018b,a) to facilitate building up a pipeline. Please
note, we do not aim to build a new QA system and
reused an existing implementation. We extend the
Frankenstein QA pipeline as illustrated in Figure 2.
We rely on the best performing pipeline reported
in (Singh et al., 2018b) over LC-QuAD dataset

6
(Trivedi et al., 2017). In addition, we manually
populated a repository of explanation templates.
For example, all the required explanation templates
for NED components are created for cases such as
templates for wrong answers, when components
produce no answer, and in the case of correct
answers. Similarly, the templates for other tasks
such as RE an QB were handcrafted. Please note
thatthesetemplatesaregeneric,therebytheydonot
depend on the employed component. For example,
ifweintegrateanotherNEDcomponentratherthan
TagMe, there is no need to update the template
repositories. In the next step, we trained classiﬁers
basedonthesettingswhichwillbepresentedinthe
next section. Thus, when a new question arrives at
the pipeline, in addition to running the pipeline to
exploit the answer, our trained classiﬁers are also
executed. Then the predictions of the classiﬁers
lead us to choose appropriate templates from the
repositories. The ﬁltered templates incorporate
the output of the components to produce salient
representations for NL explanations. The ﬂow
of the explanations is represented to the end user
besides the ﬁnal answer.
Templates for Explanation To support our
approach for explainable QA, we handcrafted
11 diﬀerent templates for the explanation. We
create placeholders in the predeﬁned templates
to verbalize the output of the QA components.
Consider the explanation provided in Figure 1.
The original template for explaining the output
of TagMe component is: TagMe identifies
the multiword X as the entity in the
question. The entity is mapped to the
DBpedia concept dbr:W. The placeholders
X and dbr:W are replaced accordingly for each
question if a classiﬁer selects this template in its
prediction.
5 Experimental Study
We direct our experiment in response to our two
researchquestions( i.e.,RQ1andRQ2)respectively.
First, we pursue the following question“How eﬀec-
tive is our approach for generating explanations?”
This evaluation implies the demonstration of the
success of our approach in generating proper expla-
nations. Itquantitativelyevaluatestheeﬀectiveness
of our approach. On the contrary, the second dis-
courseoftheexperimentisanHCIstudyinresponse
to the question“How eﬀective is the perception of
the end user on our explanations?”This experi-
ment qualitatively evaluates user perception based
onthehumanfactorsintroducedearlier(cf. Section
1). In the following Subsections, we detail our
experimental setups, achieved results, and insights
over the outcomes of the evaluation.
5.1 Quantitative Evaluation
This experiment is concerned with the question
“Howeﬀectiveisourapproachforgeneratingexpla-
nations?”. We measure the eﬀectiveness in terms
of the preciseness of the explanations. Regarding
the architecture of our approach, choosing the right
explanation template depends on the prediction of
the classiﬁers. If classiﬁers precisely predict a
correct output for the underlying components, then
consequently, the right templates will be chosen.
0
20
40
60
80
TagMe RNLIWOD NLIWOD QB
Logestic Regression SVM RandomForest GaussianNB DecisionTree
Figure 3: This ﬁgure illustrates the accuracy of ﬁve
classiﬁersperQAcomponent: TagMe,RNLIWOD,and
NLIWOD QB. Logistic Regression classiﬁer performs
best for all the components.
In other words, any ﬂaw in the prediction leads
to a wrong template. Thus, here we present
the accuracy of our classiﬁers per component.
We consider three generic classes, namelyOc =
{Success ,NoAns wer,Wron gAnswer} (cf. sec-
tion 4) for the outputs of individual components.
A benchmarking approach has been followed to
choose best classiﬁer per task. We employ ﬁve
diﬀerent classiﬁers (SVM, Logistic Regression,
Random Forest, Gaussian NB, and Decision Tree)
and calculated each classiﬁer’s accuracy per com-
ponent. To train the classiﬁers per component, we
requiretocreateasingledataset. Thesample-setin
training is formed by considering questions of the
LC-QuAD dataset. To get the concrete representa-
tion of each question, we extracted the following
features: question length, headword(who, what,
how), answer types (boolean, number, list), and
POS tags. If a particular feature is present, we
consider the value 1; if not, then the value of that

7
feature is 0 while representing the question. The
label set of the training datasets for a given com-
ponent was set up by measuring the micro F-Score
of every given question for 3,253 questions from
the LC-QuAD dataset. The F-score per question
is calculated by adopting the same methodology
proposedby(Singhetal.,2018b). Werelyon3,253
questions out of 5,000 questions of the LC-QuAD
dataset because the gold standard SPARQL queries
of the remaining 1,747 questions do not return any
answer from DBpedia endpoint (also reported by
(Azmy et al., 2018)). The classiﬁer predicts if a
component can answer the question or not, and
trained using features extracted from the natural
language questions against the F score per question.
Duringthetrainingphase,eachclassiﬁerwastuned
with a range of regularization on the dataset. We
usedthecross-validationapproachwith10foldson
the LC-QuAD dataset. We employ a QA pipeline
containing TagMe (Ferragina and Scaiella, 2010)
for entity disambiguation, RNLIWOD6 for relation
linking, and NLIWOD QB7 for SPARQL query
builder. Figure 3 reports the accuracyof ﬁve classi-
ﬁers (average of all classes). Furthermore, Table 2
reports the accuracy of the best classiﬁer (Logistic
Regression in our case) for each component.
Component Accuracy
TagMe 0.64
RNLIWOD 0.60
NLIWOD WB 0.49
Table 2: Accuracy of our multi-class classiﬁer for
predicting type of explanation for each component.
Observations. We observe that the logistic re-
gression classiﬁer performs best for predicting the
output of components. However, the accuracy of
the classiﬁer is low as depicted in the Table 2.
(Singh et al., 2018b) report accuracy ofbinary
classiﬁersfor TagMe, RNLIWOD, and NLIWOD
QB as 0.75, 0.72, and 0.65 respectively. When we
trainmulti-class classiﬁers(i.e.,three classes) on
the same dataset, we observe a drop in the accu-
racy. The main reason for the low performance of
the classiﬁers is the low component accuracy (c.f.
Table 1)
6Component is similar to Relation Linker ofhttps://
github.com/dice-group/NLIWOD
7Component is based on https://github.com/
dice-group/NLIWOD and (Unger et al., 2012).
5.2 User Perception Evaluation
In the second experiment, we pursue the following
research question:“How is the perception of end
user about explanations along the human factor
dimensions?” To respond to this question, we con-
duct the following experiment:
Experimental Setup: We perform a user study
to evaluate how the explanations impact user per-
ception. We aim at understanding user’s feed-
back on the following four parameters inspired by
(Ehsan et al., 2019; Ehsan and ark Riedl, 2019):
1) Adequate Justification: Does a user feel
the answer to a particular question is justiﬁed or
provided with the reasoning behind inferences of
the answer? 2)Education: Does the user feel ed-
ucated about the answer generation process so that
she may better understand the strengths and limita-
tions of the QA system? 3)User involvement:
Does the user feel involved in allowing the user
to add her knowledge and inference skills to the
complete decision process? 4)Acceptance: Do
explanations lead to a greater acceptance of the
QA system in future interactions? With respect to
the above criteria, we created an online survey to
collectuserfeedback. Thesurveyembracesrandom
ten questions from our underlying dataset from a
variety of answer types such as questions with the
correct answer, incorrect answer, no answer (for
which classiﬁers predict correct templates). The
ﬁrst part of the survey displays the questions to the
userwithoutanyexplanation. Inthesecondpart,the
same ten questions, coupled with the explanations
generatedbyourapproach,aredisplayedtotheuser.
Theparticipantsofthesurveyareaskedtorateeach
representationofquestion/answerbasedonthefour
humanfactordimensions(i.e.,acceptance,justiﬁca-
tion, user involvement, and education). The rating
scale is based on the Likert scale, which allows the
participants to express how much they agree or dis-
agree with a given statement (1:strongly disagree
– 5:strongly agree). We circulated the survey to
severalchannelsoftheco-authors’network,suchas
a graduate class of Semantic Web course, research
groupsintheUSAandEurope,alongwithscientiﬁc
mailing lists. Collectively we received responses
from 80 participants. Please note, the number of
participants is at par with the other explainable
studies such as (Ehsan et al., 2019).
Results and Insights. Figure 4 summarizes the
ratings of our user study. We evaluate the user
responses based on the four human factor dimen-

8
sions: Adequate Justification, Education,
User involvement, andAcceptance. The sum-
mary of ratings for each dimension was captured
in one individual chart. The green bars show the
feedbackoverquestionswithprovidedexplanations,
andonthecontrary,redbarsareaggregatedoverthe
questionwithnoexplanation. Thex-axisshowsthe
Likert scale. The Y-axis is the distribution of users
over the Likert scale for each class independently-
with explanation and without explanation. Overall
it shows a positive trend towards the agreement
with the following facts; the provided explanations
helped users to understand the underlying process
better,justifyaparticularanswer,involvetheuserin
thecompleteprocess,andincreasetheacceptability
oftheanswers. Thegreenbarsarelargerinpositive
ratings, such as strongly agree.
0
25
50
75
100
1 2 3 4 5
%
Do you feel involved in the answer
generation process?
0
25
50
75
100
1 2 3 4 5
%
Do you feel educated about the process
of generating the answer?
0
25
50
75
100
1 2 3 4 5
%
Do you feel the answer to the question is
justified or provided with the reasoning
why this answer has been extracted?
0
25
50
75
100
Maybe No Yes
%
Do you accept the answer?
Figure 4: User perception Evaluation. The ﬁgure illus-
trates the comparative analysis of providing with and
without explanation to the user. We consider the mean
of all the responses. X-axis depicts the Likert scale (1
is strongly disagree, 5 is strongly agree). A clear trend
in user responses shows that across all four parameters,
therearemanyanswerstowardsdisagreementorneutral
when no explanation is provided. In the case of expla-
nation, users feel involved, and responses are shifted
towards the agreement. Furthermore, users show more
trust in the acceptance of the answer when provided
with an explanation.
6 Discussion
In this paper, we focus on the challenge of explain-
able QA systems. We mainly target systems that
consumedatafromtheKGs. Thesesystemsreceive
a natural language question and then transform that
to a formal query. Our primary aim is to take the
initial steps to break down the full black-box QA
systems. Thus, we reuse an existing QA pipeline
systems since it already decompose the prominent
tasks of the QA systems and then integrate individ-
ual implementations for each QA task. We based
our approach and associated evaluation on the hy-
pothesis that every component integrated into the
pipeline should explain the output. It will edu-
cate and involve non-expert users and trigger them
to trust and accept the system. Our ﬁndings in
Section 5 support our hypothesis both on quantita-
tive and qualitative evaluation. The limitation of
our approach is that it heavily relies on the perfor-
mance of the components. In the case of having
low performing components, the accuracy of the
classiﬁers is also downgraded. Although, on the
one hand, this approach is shallow, one the other
hand it avoids exposing the user to overwhelming
details of the internal functionalities by showing
succinct and user-friendly explanations. (Hoﬀman
et al., 2017) noted that for improving the usability
of XAI systems, it is essential to combine theories
from social science and cognitive decision making
to validate the intuition of what constitutes a "good
explanation." Our work in this paper is limited to
predeﬁned template based explanations, and does
not consider this aspect. Also, our work does not
focusontheexplainabilityofthebehavioroftheem-
ployed classiﬁer, and the explanations only justify
the ﬁnal output of components.
7 Conclusion and Future Direction
In this paper, we proposed an approach that is auto-
matic and supervised for generating explanations
for a QA pipeline. Albeit simple, our approach in-
tuitively expressive for the end user. This approach
requires to train a classiﬁer for every integrated
component, which is costly in case the components
are updated (new release) or replaced by a latest
outperformingcomponent. Ourproposedapproach
induced in a QA pipeline of a modular framework
is the ﬁrst attempt for explainable QA systems over
KGs. It paves the way for future contributions
in developing explainable QA systems over KGs.
Still, there are numerous rooms in this area that
require the attention of the research community –
for example, explanations regarding the quality of
data, or metadata, or credibility of data publishers.
Furthermore, recent attempts have been made to
provide explanations of machine learning models
(Guo et al., 2018). However, the inclusion of the
explanations in neural approaches for question an-
swering(suchasin(Lukovnikovetal.,2017))isstill
an open research question, and we plan to extend

9
our work in this direction. The concerning domain
of the system is also inﬂuential in explanations. for
example, biomedical or marketing domains require
various levels of details of explanations. In general,
all of these concerns aﬀect the acceptance and trust
of the QA system by the end user. Our ambitious
visionistoprovidepersonalizedandcontextualized
explanations, where the user feels more involved
and educated.
References
Julia Angwin, Jeﬀ Larson, Surya Mattu, and Lau-
ren KirchnerIan Sample. 2016. Machine bias.
Sören Auer, Christian Bizer, Georgi Kobilarov, Jens
Lehmann, Richard Cyganiak, and Zachary G. Ives.
2007. DBpedia: A Nucleus for a Web of Open
Data. In The Semantic Web, 6th International Se-
mantic Web Conference, 2nd Asian Semantic Web
Conference, ISWC 2007 + ASWC 2007, Busan, Ko-
rea, November 11-15, 2007.
Michael Azmy, Peng Shi, Jimmy Lin, and Ihab Ilyas.
2018. Farewell freebase: Migrating the simpleques-
tions dataset to dbpedia. InProceedings of the 27th
InternationalConferenceonComputationalLinguis-
tics, pages 2093–2103.
JonathanBerant,AndrewChou,RoyFrostig,andPercy
Liang. 2013. Semantic Parsing on Freebase from
Question-Answer Pairs. InProceedings of the 2013
Conference on Empirical Methods in Natural Lan-
guage Processing, EMNLP 2013, 18-21 October
2013,GrandHyattSeattle,Seattle,Washington,USA,
AmeetingofSIGDAT,aSpecialInterestGroupofthe
ACL, pages 1533–1544.
Abhishek Bhandwaldar and Wlodek Zadrozny. 2018.
Uncc qa: A biomedical question answering system.
EMNLP 2018, page 66.
Julie Daher, Armelle Brun, and Anne Boyer. 2017. A
review on explanations in recommender systems.
DennisDiefenbach,VanessaLópez,KamalDeepSingh,
andPierreMaret.2018. Coretechniquesofquestion
answering systems over knowledge bases: a survey.
Knowledge and Information Systems, 55(3):529–
569.
Upol Ehsan and ark Riedl. 2019. On design and
evaluation of human-centered explainable ai system.
In Human-Centered Machine Learning Perspectives
Workshop at CHI.
UpolEhsan,PradyumnaTambwekar,LarryChan,Brent
Harrison, and Mark O. Riedl. 2019. Automated ra-
tionale generation: a technique for explainable AI
and its eﬀects on human perceptions. InProceed-
ings of the 24th International Conference on Intelli-
gent User Interfaces, IUI 2019, Marina del Ray, CA,
USA, March 17-20, 2019, pages 263–274.
Paolo Ferragina and Ugo Scaiella. 2010. TAGME:
on-the-ﬂy annotation of short text fragments (by
wikipedia entities). InProceedings of the 19th ACM
Conference on Information and Knowledge Manage-
ment, CIKM 2010, Toronto, Ontario, Canada, Octo-
ber 26-30, 2010, pages 1625–1628.
John Fox, David Glasspool, Dan Grecu, San-
jay Modgil, Matthew South, and Vivek Patkar.
2007. Argumentation-based inference and decision
making–a medical perspective.IEEE intelligent sys-
tems, 22(6):34–41.
Wenbo Guo, Sui Huang, Yunzhe Tao, Xinyu Xing, and
Lin Lin. 2018. Explaining deep learning models–a
bayesian non-parametric approach. InAdvances in
NeuralInformationProcessingSystems ,pages4514–
4524.
BradleyHayesandJulieAShah.2017. Improvingrobot
controller transparency through autonomous policy
explanation. In2017 12th ACM/IEEE International
ConferenceonHuman-RobotInteraction(HRI ,pages
303–312. IEEE.
LisaAnneHendricks,ZeynepAkata,MarcusRohrbach,
Jeﬀ Donahue, Bernt Schiele, and Trevor Darrell.
2016. Generating visual explanations. In Euro-
pean Conference on Computer Vision, pages 3–19.
Springer.
Jonathan L Herlocker, Joseph A Konstan, and John
Riedl. 2000. Explaining collaborative ﬁltering rec-
ommendations. In Proceedings of the 2000 ACM
conferenceonComputersupportedcooperativework ,
pages 241–250. ACM.
Robert R Hoﬀman, Shane T Mueller, and Gary Klein.
2017. Explaining explanation, part 2: empirical
foundations. IEEE Intelligent Systems, 32(4):78–86.
Konrad Höﬀner, Sebastian Walter, Edgard Marx,
Ricardo Usbeck, Jens Lehmann, and Axel-
CyrilleNgongaNgomo.2017. Surveyonchallenges
of Question Answering in the Semantic Web.Se-
mantic Web.
Dietmar Jannach, Markus Zanker, Alexander Felfernig,
andGerhardFriedrich.2010. Recommendersystems:
an introduction. Cambridge University Press.
ZhenJia,AbdalghaniAbujabal,RishirajSahaRoy,Jan-
nik Strötgen, and Gerhard Weikum. 2018. Tequila:
Temporal question answering over knowledge bases.
In Proceedings of the 27th ACM International Con-
ferenceonInformationandKnowledgeManagement ,
pages 1807–1810. ACM.
Jin-Dong Kim, Christina Unger, Axel-Cyrille Ngonga
Ngomo, André Freitas, Young-gyun Hahm, Jiseong
Kim, Sangha Nam, Gyu-Hyun Choi, Jeong-uk Kim,
RicardoUsbeck,etal.2017. OKBQAFrameworkfor
collaboration on developing natural language ques-
tion answering systems.

10
Pigi Kouki, James Schaﬀer, Jay Pujara, John
O’Donovan, and Lise Getoor. 2017. User prefer-
ences for hybrid explanations. InProceedings of the
EleventhACMConferenceonRecommenderSystems ,
pages 84–88. ACM.
Todd Kulesza, Margaret Burnett, Weng-Keen Wong,
andSimoneStumpf.2015. Principlesofexplanatory
debugging to personalize interactive machine learn-
ing. InProceedings of the 20th international confer-
ence on intelligent user interfaces, pages 126–137.
ACM.
Qing Li, Jianlong Fu, Dongfei Yu, Tao Mei, and Jiebo
Luo. 2018. Tell-and-answer: Towards explainable
visual question answering using attributes and cap-
tions. In Proceedings of the 2018 Conference on
EmpiricalMethodsinNaturalLanguageProcessing ,
pages 1338–1346.
Heguang Liu. 2019. Conditioning lstm decoder and bi-
directional attention based question answering sys-
tem. arXiv preprint arXiv:1905.02019.
Denis Lukovnikov, Asja Fischer, Jens Lehmann, and
Sören Auer. 2017. Neural network-based question
answering over knowledge graphs on word and char-
acter level. InProceedings of the 26th International
Conference on World Wide Web, WWW 2017, Perth,
Australia, April 3-7, 2017, pages 1211–1220.
Tim Miller. 2018. Explanation in artiﬁcial intelligence:
Insights from the social sciences.Artiﬁcial Intelli-
gence.
Johanna D Moore and William R Swartout. 1988. Ex-
planation in expert systems: A survey. Technical
report, University of Southern California, USA.
Axel-Cyrille Ngonga Ngomo, Lorenz Bühmann,
Christina Unger, Jens Lehmann, and Daniel Gerber.
2013. Sorry, i don’t speak sparql: translating sparql
queries into natural language. InProceedings of the
22nd international conference on World Wide Web,
pages 977–988. ACM.
Michael Petrochuk and Luke Zettlemoyer. 2018. Sim-
plequestions nearly solved: A new upperbound and
baseline approach. InProceedings of the 2018 Con-
ference on Empirical Methods in Natural Language
Processing, pages 554–558.
Dharmen Punjani, K Singh, Andreas Both, Manolis
Koubarakis, Ioannis Angelidis, Konstantina Bereta,
Themis Beris, Dimitris Bilidas, T Ioannidis, Niko-
laos Karalis, et al. 2018. Template-based question
answering over linked geospatial data. InProceed-
ings of the 12th Workshop on Geographic Informa-
tion Retrieval, page 7. ACM.
Marco Tulio Ribeiro, Sameer Singh, and Carlos
Guestrin.2016. Whyshoulditrustyou?: Explaining
the predictions of any classiﬁer. InProceedings of
the22ndACMSIGKDDinternationalconferenceon
knowledge discovery and data mining, pages 1135–
1144. ACM.
Wojciech Samek, Thomas Wiegand, and Klaus-Robert
Müller.2017. Explainableartiﬁcialintelligence: Un-
derstanding, visualizing and interpreting deep learn-
ing models.arXiv preprint arXiv:1708.08296.
Saeedeh Shekarpour, Edgard Marx, Axel-
Cyrille Ngonga Ngomo, and Sören Auer. 2015.
SINA: semantic interpretation of user queries for
question answering on interlinked data. J. Web
Semant., 30:39–51.
SaeedehShekarpour,Axel-CyrilleNgongaNgomo,and
Sören Auer. 2013. Question answering on inter-
linked data. In22nd International World Wide Web
Conference, WWW ’13, Rio de Janeiro, Brazil, May
13-17, 2013, pages 1145–1156.
EdwardHShortliﬀe.1974. Arule-basedcomputerpro-
gramforadvisingphysiciansregardingantimicrobial
therapyselection. InProceedingsofthe1974annual
ACM conference-Volume 2, pages 739–739. ACM.
Kuldeep Singh. 2019. Towards dynamic composition
of question answering pipelines. Doctoral Thesis,
University of Bonn, Germany.
KuldeepSingh,AndreasBoth,ArunSethupatRadhakr-
ishna, and Saeedeh Shekarpour. 2018a. Franken-
stein: A platform enabling reuse of question answer-
ing components. InThe Semantic Web - 15th Inter-
national Conference, ESWC 2018, Heraklion, Crete,
Greece, June 3-7, 2018, Proceedings, pages 624–
638.
Kuldeep Singh, Arun Sethupat Radhakrishna, Andreas
Both, Saeedeh Shekarpour, Ioanna Lytra, Ricardo
Usbeck,AkhileshVyas,AkmalKhikmatullaev,Dhar-
men Punjani, Christoph Lange, Maria-Esther Vidal,
JensLehmann,andSörenAuer.2018b. Whyreinvent
the wheel: Let’s build question answering systems
together. In Proceedings of the 2018 World Wide
Web Conference on World Wide Web, WWW 2018,
Lyon, France, April 23-27, 2018, pages 1247–1256.
KuldeepSingh,MuhammadSaleem,AbhishekNadgeri,
Felix Conrads, Jeﬀ Pan, Axel-Cyrille Ngonga
Ngomo, and Jens Lehmann. 2019. Qaldgen: To-
wards microbenchmarking of question answering
systems over knowledge graphs. InISWC.
KristenStubbs,PamelaJHinds,andDavidWettergreen.
2007. Autonomy and common ground in human-
robot interaction: A ﬁeld study. IEEE Intelligent
Systems, 22(2):42–50.
PriyanshTrivedi,GauravMaheshwari,MohnishDubey,
and Jens Lehmann. 2017. LC-QuAD: A Corpus
for Complex Question Answering over Knowledge
Graphs. InTheSemanticWeb-ISWC2017-16thIn-
ternational Semantic Web Conference, Vienna, Aus-
tria, October 21-25, 2017, Proceedings, Part II,
pages 210–218. Springer.
Christina Unger, Lorenz Bühmann, Jens Lehmann,
Axel-Cyrille Ngonga Ngomo, Daniel Gerber, and

11
PhilippCimiano.2012. Template-basedquestionan-
swering over RDF data. InProceedings of the 21st
WorldWideWebConference2012,WWW2012,Lyon,
France, April 16-20, 2012, pages 639–648. ACM.
ChristinaUnger,CorinaForascu,VanessaLópez,Axel-
CyrilleNgongaNgomo,ElenaCabrio,PhilippCimi-
ano, and Sebastian Walter. 2015. Question Answer-
ing over Linked Data (QALD-5). InWorking Notes
of CLEF 2015 - Conference and Labs of the Evalua-
tionforum,Toulouse,France,September8-11,2015.
CEUR-WS.org.
Ricardo Usbeck, Axel-Cyrille Ngonga Ngomo, Lorenz
Bühmann,andChristinaUnger.2015. Hawk–hybrid
question answering using linked data. InEuropean
SemanticWeb Conference, pages353–368. Springer.
Jialin Wu and Raymond J Mooney. 2018. Faithful mul-
timodal explanation for visual question answering.
arXiv preprint arXiv:1809.02805.
Wei Yang, Yuqing Xie, Aileen Lin, Xingyu Li, Luchen
Tan, Kun Xiong, Ming Li, and Jimmy Lin. 2019.
End-to-end open-domain question answering with
bertserini. NAACL HLT 2019, page 72.
```
