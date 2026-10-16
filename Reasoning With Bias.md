---
title: Reasoning With Bias
author:
  - Chiara Manganini
  - Giuseppe Primiero
source: https://ceur-ws.org/Vol-3523/paper4.pdf
venue: AEQUITAS 2023
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
  - op/acc/download
  - op/acc/downloaded
manual: https://pure.eur.nl/en/publications/f43c15f4-0b5d-4bb0-8ad3-d2ed918a4dac
pdfORepub: "[[Reasoning With Bias.pdf]]"
modified: 2026-09-08
---

# Notes

## Full text (extracted from `2PDF/Reasoning With Bias.pdf`)

*Extracted:* 2026-09-17

```text
Reasoning With Bias
Chiara Manganini1,∗,†, Giuseppe Primiero1,†
1Logic, Uncertainty, Computation and Information Group, Department of Philosophy, University of Milan
Abstract
In recent years, the problem of evaluating the trustworthiness of machine learning systems has become
more urgent than ever. A directly related issue is that of assessing the fairness of their decisions. In
this work, we adopt a primarily logical perspective on the topic, by trying to highlight the basic logical
characteristics of the inferential setting in which a biased prediction occurs. To do so, we first identify
and formalise four key desiderata for a logic capable of modelling the behaviour of a biased system,
namely: skewness, dependency on data and model, non-monotonicity, and the existence of a minimal
distinction between types of bias. On this basis, we define two metrics, one for group and one for
individual fairness.
Keywords
Bias, Logic, Fairness,
1. Introduction
The widespread emergence of phenomena of biased predictions counts certainly among the
most adverse impacts of new data-intensive science and technologies. This questions the
trustworthiness of results, especially when the opaque nature of the models very often prevents
us from precisely knowing or examining their inner structure [1].
A possible strategy to assess trustworthiness in these opaque settings is to check the actual
model behaviour against a desirable one. Logics have been recently designed to formalise
trustworthiness for probabilistic programs and to reason about them [2, 3, 4], with a specific
focus on determining statistical distance measures for such systems with respect to their
desirable or expected behaviour. A specific formulation has also been offered for modelling
classifiers whose wrong output might be due to forms of bias, using a non-symmetric distance
which reflects the systematic skeweness of the result [5]. In this sense, such logics offer
verification and reasoning tools on the trustworthiness of black-box model with respect to
explainable surrogate models, as those obtained by symbolic knowledge-extraction (SKE) [6, 7].
However, a grounded logical formalisation of how to define measures of bias in such contexts
and how to reason about them is still at early stages in the literature [8, 9, 10, 11]. From the
point of view of symbolic reasoning, and especially when it comes to the task of designing
models for scientific inference in the era of data science, this means to extend the vast families
Aequitas 2023: Workshop on Fairness and Bias in AI | co-located with ECAI 2023, Kraków, Poland
∗Corresponding author.
†
These authors contributed equally.
Envelope-Open chiara.manganini@unimi.it (C. Manganini);giuseppe.primiero@unimi.it (G. Primiero)
© 2023 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)


of defeasible logics and logics for uncertain reasoning with new ones, capable of accounting for
the phenomenon of machine learning bias.
In this paper, we aim to sketch a first understanding of bias usable in the context of logical
reasoning. In order to do so, in Section2 we first start formulating the desiderata for a logic
designed to reason in the presence of bias. In Section3 we propose a logical formalisation of the
notion of biased machine learning system and we show how it accommodates the mentioned
desiderata. After introducing a correction distance as a measure of the monotonicity of a
prediction (Section4), in Section5 we exploit it to quantitatively assess the presence of bias.
Finally, we explain how this logical framework may be expanded, refined, applied in the future
(Section 6).
2. Logical desiderata for reasoning with bias
As a preliminary work, we start from the observation that a logic for reasoningwith bias – i.e.,
for drawing valid conclusions within a possibly biased inferential system – should be able to
capture the following set of central properties characterising the phenomenon of algorithmic
discrimination.
2.1. Skewness of Incorrect Predictions
A first and fundamental distinction our logic should account for is that between biased predic-
tions and merely erroneous ones. In statistics, error is defined as the difference between the
true value of a measurement and its recorded value, and can be either random or systematic.
Since random error, or variability, has no preferred direction, its impact can be minimised with
large sample sizes. Systematic error, instead, refers to a consistent over- or underestimation of
the observations. It has a net direction so that averaging over a large number of observations
does not eliminate its effect.
In the machine learning context, the notion of bias we want to focus upon is that of a
systematic error against a certain protected category such as race, gender, age, geographical
provenance,oreconomicstatus[ 12]. Here“against”istobeintendedas“opposedtothedirection
given by the most favourable prediction”. Such a direction of course varies in relation to the type
ofscenarioconsidered. Inthiswork,wefocusonaverycoarse-graineddistinctionbetweenwhat
we can call “allocative” and “punitive” contexts: in the former case, some beneficial resource (a
job, a loan, a subsidy, etc.) is to be allocated to individuals based on a prediction; in the latter,
some punitive action is imposed to individuals, based on some risk measure (fraud, recidivism,
etc.). The reason for distinguishing between two symmetrical predictive scenarios is related to
the different interpretation we give of the negation rule for our logical framework, which will
become clearer in Section3.
Summarising, two types of skewness should be considered in relation to bias:
1. Skewness as systematicity of error. The evaluation is skewed, in the sense that it shows a
net direction, which means it results from a systematic rather than a random error. The
direction itself is also relevant, as it emerges either in terms of false positives in punitive
contexts, or in terms of false negatives in allocative contexts.

2. Skewnessaspartialityofthedomainaffectedbytheerror. Thesystematicerrornegatively
impacts only a subgroup of the population which is identified by its belonging to a certain
protected category.
Example. A classifier𝐷 is used to predict the risk of insurance fraud. To each
new entry in a set of insurance claims, it either assigns the target label “Fraud” or
“¬Fraud”. 𝐷 uses the protected binary feature “MalePolicyholder” for its prediction.
The desideratum of skewness requires that, for the system to be considered gender-
biased a significant imbalance in the prediction errors across male and female
individuals must be observed in its output. For example, this can happen when
false positives are significantly more in the female group with respect to the male
one, so that the former class is negatively impacted by the decisions (predictions)
of 𝐷.
All of these fundamental aspects need to be captured in our formal representation of a reasoning
system for bias.
2.2. Dependency on Data and Model
A second property of the bias phenomenon we wish to capture is its dependency on both data
and model. For instance, it is well acknowledged in the literature that a skew in frequency of
the classes in the training set leads to disparate error rates on the underrepresented attributes
[12]. This is not the only issue affecting training data, though. [13] highlights that other types
of data bias (due to disproportionate measurement, representation, aggregation, and evaluation
among the different classes) can lead to discriminatory results as well. In general, the presence
of bias largely depends on the training data, and this is definitely something our logic should
account for.
Also model design choices concerning loss function, optimiser and hyper-parameters, made
to maximise test-set accuracy, can result in the occurrence of machine learning bias [13]. It has
been highlighted that even more subtle choices – like learning rate and length of training – can
impact on fairness due to the fact that underrepresented features are learnt later in the training
process [14].
The actual manifestation of bias, instead, depends on the test set. Actually, there can be a
situation in which a biased model does not in fact result in a discrimination due to contingent
conditions.
Example. Reconsider the gender-biased learning algorithm𝐷 for fraud risk detec-
tion. Imagine now that, due to a poor selection of inputs for the testing process,
the totality of test inputs are male, i.e., each of them satisfies the predicate “Male”.
What can we say about a possible gender bias of the algorithm? On the one hand,
an imbalance in the frequency of the gender classes in the historical recordings
on which D has been trained causes the model to have the disposition to produce
biased outcomes against women. On the other hand, no gender-biased prediction
is actually produced, since this disposition never emerges.
Hence, our formal modelling will have to be parametric with respect to these three variables.

2.3. Non-Monotonicity
Example. Gender-biased model𝐷 for fraud risk detection is fed step-by-step with
features from a predetermined list that contains age, gender, address, etc. about
datapoint 𝑎. At each step,𝐷 has to classify𝑎. Imagine now that, while at step𝑚 of
this process𝐷 classifies 𝑎 as “Fraud”, the information provided at step𝑚 + 𝑖 makes
𝐷 revise the confidence in this prediction under a certain threshold, and the system
outputs value “¬ Fraud”.
An increase in both accuracy and available information can lead to a change of classification
(from “Fraud” to “¬ Fraud”). At the beginning of this process, a “minimal-knowledge” condition,
possibly corresponding to one piece of information to make the prediction, matches with
the minimum accuracy possible; on the other hand, an “omniscience” condition, in which all
the available pieces of information have been provided matches with the maximum accuracy
possible. Theoretically, this should always be associated with a correct classification (the ground
truth).
This simplified story just loosely models the behaviour of a learning system that corrects its
own prediction on a new input𝑎 as the amount of available information increases. The above
example captures the basic intuition at the heart of non-monotonicity, which we think useful to
account for clarifying of the relationship between a biased outcome and the information used
to generate it, both qualitatively and quantitatively. We start from the following claims:
Proposition 1. Possessing all available correct information about datapoint 𝑥 is sufficient for its
correct classification.
Proposition 2. There is a minimal amount 𝑁 of information about datapoint 𝑥, sufficient for its
correct classification.
Proposition 3. Any amount of information 𝑀 < 𝑁 about datapoint 𝑥 is not sufficient for its
correct classification.
Note that, in practice, a classifier assumes𝑁 = 1 to be the weighted value of the whole set
of features it uses, although it could be taken to be a smaller value (i.e., the prediction can
be correct even in absence of some information). And𝑀 < 1 is always the weighted value
of the set of features used at any point in time for an incorrect prediction. When incomplete
information is already sufficient for a correct prediction, then𝑀 < 𝑁 < 1 .
With this in mind, let us now take into consideration a machine learning system, which we
know to be biased according to the analysis in Subsections2.1 and 2.2. In other words, this
means that:
1. the system generates systematic (i.e., with a net direction) erroneous predictions against
a certain protected category of individuals,
2. the errors depend on the data on which it has been trained and on the design choices of
the model itself.

In this scenario, we are interested in exploring how the presence of bias in a system quanti-
tatively depends on the amount of information used to return an incorrect prediction. A first
intuition is that, on the one hand, the system may be considered maximally biased against a
certain protected attribute when, given a new datapoint with that attribute and for which a
wrong classification is predicted, no additional information may allow to correct it. Conversely,
the system may be considered minimally biased against the same protected attribute when a
single additional piece of information allows to correct it.
To recapitulate, in the presence of a biased system, we expect our logic to assess how much
information is required to fail monotonicity as a proxy of the amount of bias affecting the
system. Bias will manifest as an imbalance for such measure with respect to distinct groups, or
distinct protected features.
2.4. A Minimal Distinction Between Types of Bias
When it comes to define the types of bias, a number of nomenclatures can be found in the
literature [13,12,15,16], most of which tend to characterise qualitative differences among biases
based on the their different origins. For instance, in [13], among the statistical factors possibly
resulting in a biased prediction we find: the non-random sampling of subgroups (sampling bias),
the lack of diversity of the sample (representation bias), and the distortions that can emerge
from the aggregation of datapoints (aggregation bias, Simpson’s paradox). In this work, we
rather want to focus our attention on two quantitative aspects connected to biased outcomes,
along which a minimal distinction between types of bias can be traced:
1. biases engendered by an insufficient amount of information available to the system to
generate the prediction.
2. biases engendered by an incorrect assignment of the feature relevance.
Example. In the gender-biased learning algorithm𝐷 for fraud risk detection, the
two different kinds of bias illustrated above would be illustrated as follows. First,
consider a version of𝐷 which is never given any age information on the claimant,
e.g. because such feature was not required at design stage; as a result, a potential
bias towards some class (e.g. “female”) might emerge which does not recognise
that a given subclass (e.g. “above 60 years old”) is actually strongly correlated
with claims. Now consider a deployment of𝐷 which is fed only with occurrences
of cases by female drivers and learns accordingly. Its trained version𝐷′ would
eventually associates all cases of frauds to female driver and assign low scores to
male drivers.
Hence, another component in bias emergence needs to be identified in the amount of infor-
mation available and its relevance for the classification at hand.

3. Formalising Bias
For sake of simplicity, in this work we focus on the minimal case of a binary classification in the
presence of a single binary protected attribute.1 We abstract here from many technical details,
and in particular we present only a sketch of a formalization based on a derivability relation⊢,
leaving the details of a corresponding consequence relation⊨ to further work. Moreover, the
current presentation is intended to offer only some useful intuitions about how to model the
properties presented above in Section2 within a logical setting; actual logical systems can then
be designed with these characteristics to deal with specific bias cases.
Consider a model𝑆 trained on a datasetd and characterised by a set of design features (in
terms of loss function, optimiser, and hyper-parameters used for its training)m. The trained
model returns a classification𝑃 for the datapoint𝑎 of the test set on a target feature𝔽𝑖. We use
the derivability relation to express the classification by formulas of the form:
𝑆 ⊢ 𝑑,𝑚 𝑃 (𝑎)
This judgement can be further enhanced: first, by a measure of the amount of features used by
the classifier at any given moment, as a rational number on the left-hand side of the derivability
relation; second, by a degree of accuracy on the classification expressed as a rational number in
[0, 1] on the right-hand side of the relation, then using a cut-off point to reduce the classification
to a binary value. We leave these technicalities aside for the present moment and deal only
with Boolean judgements. Further, let us assume this classification to beincorrect. This means
that, in a given model𝑍 – which we consider isomorphic to the real world, i.e., representing it
correctly or, more agnostically, at least expressing what the designer considers to be a correct
model for the test set – datapoint𝑎 should be correctly classified as¬𝑃:
𝑍 ⊢ ¬𝑃 (𝑎)
To start off, here is how the desiderata mentioned in the previous Section can fit into a logical
framework:
• What mentioned in Subsection2.1 indicates that inferential and/or semantic validity
may be indeed appropriate to model the skewness of bias in classification: fixed the
properties of the system𝑆, the error in the prediction arises in terms of evaluations for
some predicatesand some individuals; hence, a subclass of predicates and individuals of
the domain in the test set will make biased evaluations emerge, where such classes can
be at least partially identified by comparison with the training set.
• For the discussion in Subsection2.2, we know that the incorrect inference returned by
system 𝑆 can depend on both the data𝑑 with which it was trained or on the characteristics
𝑚 of the model itself. This aspect requires therefore that such parameters are made
transparently available in the formalisation of the system we are after.
1Our proposal can be quite easily translated into a multi-label setting by introducing a probabilistic evaluation on the
target predicate. Adding further protected attributes could be more challenging, due to the problem of modelling
intersectionality of discrimination. These tasks, however, go beyond the scope of the present work.

• The aspects of non-monotonicity considered in Subsection2.3 are to be expressed in
terms of the dynamic evaluation made by𝑆 for a given datapoint, as the information
under which the prediction is derived increases. We aim therefore at defining a measure
of such a change, by invalidating standard classical inference rules (respectively, making
a consequence relation non-monotonic).
• As illustrated in Subsection2.4, 𝑆 can be differently biased depending either (1) on how
much information is provided by the available features used as predictors, or (2) on how
relevant each of the selected feature has been taken to be by the system. These aspects
will be rendered by formulating explicitly features on the classifier and their weights.
Consider now a classification system(𝑆, ⊢𝑑,𝑚 ) within a languageℒ = {𝔻, ℙ, < 𝑤} where:
• 𝔻 = {𝑎, 𝑏, 𝑐, … , 𝑛} is a finite set of elements of a domain denoting the datapoints of the
test set;
• ℙ = {𝑃 , 𝑄, 𝑅, ..., 𝑍 } is the finite set of the predicates in the language such that:
1. a partition ofℙ is the set𝒫 = {ℙ𝕣, ℕℙ𝕣, 𝕋} denoting, respectively, the set of pro-
tected predicates, the set of non-protected ones, and the target predicate to be
predicted;
2. another partition ofℙ is the set of featuresℱ = {𝔽 1, 𝔽2, ..., 𝔽𝑚} which, for simplicity,
we assume to be all binary.
In other words,ℙ enumerates all the features used by the system. Every class, in turn,
denotes a possible value of a certain feature, be it protected, non-protected, or the target
feature.
• <𝑤⊆ ℙ × ℙ is an ordering on the predicatesℙ based on a weight function𝑤 ∶ ℙ ↦ [0, 1]
that assigns a measure of relevance to each predicate for a given feature𝔽𝑖, so that
⟨𝑃𝑖, 𝑃𝑗⟩ ∈< 𝑤 iff 𝑤 (𝑃𝑖) ≤ 𝑊 𝑤 𝑃 𝑗) for every𝑃𝑖, 𝑃𝑗 ∈ ℙ . Moreover, we take that weights are
normalised, i.e., that∑𝑛 𝑤 (𝑃𝑛) ≤ 1 .
Example. A classifier is used to predict applicants’ eligibility for a loan,
therefore 𝕋 = {𝐿𝑜𝑎𝑛} , where 𝐿𝑜𝑎𝑛(𝑎) can be true (if 𝑎 is eligible for
a loan) or false (if 𝑎 is not eligible). The system classifies on the ba-
sis of the following sets of predicates: ℙℝ = {𝑀𝑎𝑙𝑒} , and ℕℙℝ =
{𝐹 𝑢𝑙𝑙𝑇 𝑖𝑚𝑒𝐸𝑚𝑝𝑙𝑜𝑦 𝑒𝑑, 𝐻 𝑜𝑢𝑠𝑒ℎ𝑜𝑙𝑑𝑂𝑤 𝑛𝑒𝑟, 𝑈 𝑛𝑖𝑣 𝑒𝑟𝑠𝑖𝑡𝑦 𝐷𝑒𝑔𝑟𝑒𝑒, 𝑀𝑎𝑟𝑟𝑖𝑒𝑑} . It is known
that two features are more relevant than the others for the classification:
𝑤 (𝐹 𝑢𝑙𝑙𝑇 𝑖𝑚𝑒𝐸𝑚𝑝𝑙𝑜𝑦 𝑒𝑑) = 0.3 and 𝑤 (𝐻 𝑜𝑢𝑠𝑒ℎ𝑜𝑙𝑑𝑂𝑤 𝑛𝑒𝑟) = 0.25 . All the other fea-
tures are equally relevant for the classification, and they all weigh1−0.3−0.25
3 = 0.15.
An atomic formula ofℒ is therefore a predication of a class𝑃 for a given datapoint𝑎.2 In
this context, proof-theoretically the information available in𝑆 expresses the current knowledge
about 𝑎 such that given the available inference rules in⊢ it allows to derive that𝑎 has (resp. has
2The choice of connectives inℒ will be determined by requirements of the system and will define the inference
relation ⊢ (in the following, we will only make general comments on the use of negation).

not) target feature𝑃. Semantically, it says that the model in which all information contained in
𝑆 is true, will also make𝑃 (𝑎) true (resp. false).
In the following we focus on two structural elements required to model bias formally as
intended above: the role of the rules for negation, and the quantification of information for
non-monotonicity of the inference relation.
3.1. Negation
The initial situation of skewness might be represented as follows. In punitive contexts, bias
emerges as systematic error in terms of false positives, according to which
𝑆 ⊢ d,m 𝑃 (𝑎) 𝑤 ℎ𝑖𝑙𝑒 𝑍 ⊢ ¬𝑃 (𝑎)
i.e., the real or chosen model of the world sees individual𝑎 not to satisfy the property𝑃, while
the system𝑆 predicts it to have it. In allocative contexts, bias emerges as systematic error in
terms of false negatives, according to which:
𝑆 ⊢ d,m ¬𝑃 (𝑎) 𝑤 ℎ𝑖𝑙𝑒 𝑍 ⊢ 𝑃 (𝑎)
i.e., the real or chosen model of the world sees individual𝑎 satisfying the property𝑃, while
the system𝑆 predicts the opposite. In both contexts, the systematic error concerns a subset of
the domain𝔻, identified by a partition with respect to a predicate𝑃 ∈ ℙ𝕣 .
The logical setting we are defining allows to model the difference between the two scenarios
by a different interpretation of the rule for negation. In the allocative context, a correctly
working classifier should see implemented the interpretation of Negation as Contradiction:
𝑆 ⊢ ¬𝑃 (𝑎)
𝑆 ⊢ 𝑃 (𝑎) → ⊥ 𝑤 ℎ𝑖𝑙𝑒 𝑍 ⊢ 𝑃 (𝑎)
i.e., if the system predicts the negation of the intended property (say: not being eligible for
welfare credits), the assignment of a certain benefit should be blocked. On the other hand, in
a punitive context it seems that a correctly working classification system should express the
principle of Negation as Failure:
𝑆 ⊬ 𝑃 (𝑎)
𝑆 ⊢ ¬𝑃 (𝑎) 𝑤 ℎ𝑖𝑙𝑒 𝑍 ⊢ ¬𝑃 (𝑎)
in other words, if the system does not predict the intended property (say: being guilty), it should
infer its negation (not being guilty). This allows us to meet the desideratum of “skewness as
systematicity of error” specified at point (1) of Section2.1. In simple words, we required that a
logic for reasoning with bias should be able to capture the idea that the systematic prediction
error we call bias can either occur in terms of false positives (in punitive setting) or in terms
of false negatives (in allocative ones). This difference can be in fact accommodated by the
semantics of our logic, through the choice of an appropriate set of logical rules for negation.

3.2. Quantifying Non-Monotonicity
Underthe assumption of anincorrect prediction, wewantto quantify the amountof information
needed for the (supposedly wrong) inference to be corrected. We know that the inability of
an inferential system to accommodate such a change is expressed by the structural rule of
Weakening:
𝑆 ⊢ 𝑃 (𝑎)
𝑆, 𝑄1(𝑎), … , 𝑄𝑛(𝑎) ⊢ 𝑃 (𝑎) 𝑊 𝑒𝑎𝑘 𝑤 ℎ𝑖𝑙𝑒 𝑍 ⊢ ¬𝑃 (𝑎)
for
{𝑄1, … , 𝑄𝑛} ⊆ (ℙ − {𝑃 })
i.e., while adding new predicates to the datapoint, the ability of the system to continue
inferring a valid (target) property, should not diminish. Note that the quantification over the
possible predicates for which the Weakening rule holds is fundamental here. For instance, if
{𝑄1(𝑎), … , 𝑄𝑛(𝑎)} = ℙ − {𝑃 } , this means that𝑆 incorrectly predicts the class𝑃 for the datapoint
𝑎 (for some𝑃 and some𝑎), and no additional amount of information allows to change this
inference:
∄𝑄𝑚(𝑎) 𝑠.𝑡. 𝑆 ⊢ 𝑃 (𝑎)
𝑆, 𝑄1(𝑎), … , 𝑄𝑛(𝑎), 𝑄𝑚(𝑎) ⊢ ¬𝑃 (𝑎) (1)
This is, for simplicity, expressed here by boolean predicates, while a worked out analysis
would make use of the anticipated probabilistic assignment of predicates to constants and the
corresponding measure on the amount of features evaluated.
What one would want to model, therefore, is a system whose incorrect prediction is very
“close” to be amended, provided a new piece of information becomes available:
∃𝑄𝑚(𝑎) 𝑠.𝑡. 𝑆 ⊢ 𝑃 (𝑎)
𝑆, 𝑄1(𝑎), … , 𝑄𝑛(𝑎), 𝑄𝑚(𝑎) ⊢ ¬𝑃 (𝑎) (2)
Example. The fraud detection classifier should implement a negation as failure
principle
𝐷 ⊬ 𝐹 𝑟𝑎𝑢𝑑(𝑎)
𝐷 ⊢ ¬𝐹 𝑟𝑎𝑢𝑑(𝑎)
as long as enough information is provided to prove the contrary, i.e.
𝑍 ⊢ 𝐹 𝑟𝑎𝑢𝑑(𝑎)
In particular, the aim is to show how much information allows for the following
𝐷 ⊢ ¬𝐹 𝑟𝑎𝑢𝑑(𝑎)
𝐷, 𝑄1(𝑎), … , 𝑄𝑚(𝑎) ⊢ 𝐹 𝑟𝑎𝑢𝑑(𝑎)
Hence, our next tasks are

1. to evaluate the amount of information of𝑄1(𝑎), … , 𝑄𝑛(𝑎) so that certain predicates are
more relevant than others;
2. use it to quantify non-monotonicity.
In other words, assuming𝑆’s initial incorrect prediction for a datapoint𝑎, the degree of
monotonicity expresses “how far the system is from a correction of the prediction”. Both these
goals will be addressed in the following section.
4. Correction Distance
Consider the task of inferring the correct prediction𝑆 ⊢ 𝑃 (𝑎) . Assume:
{𝑄1(𝑎), … , 𝑄𝑛(𝑎)}𝑓 (𝑤1,…,𝑤𝑛)=𝑁 ⊢ 𝑃 (𝑎)
where 𝑁 expresses the amount of information computed by a chosen function𝑓 over the
weights of the predicates𝑄1, … , 𝑄𝑛 and sufficient for the correct classification. We abbreviate
with ∣ 𝑆 ∣= 𝑁 the overall weight of the set of formulas{𝑄1(𝑎), … , 𝑄𝑛(𝑎)}𝑓 (𝑤1,…,𝑤𝑛)=𝑁 when used
in the system𝑆.
Consider moreover:
{𝑄1(𝑎), … , 𝑄𝑚(𝑎)}𝑓 (𝑤1,…,𝑤𝑚)=𝑀 ⊢ ¬𝑃 (𝑎)
where 𝑀 is the amount of information currently available and used for a presumably or
possibly wrong prediction𝑆 ⊢ ¬𝑃 (𝑎) , assuming the same function𝑓. We abbreviate with
∣ 𝑆 ∣= 𝑀 the overall weight of the set of formulas{𝑄1(𝑎), … , 𝑄𝑚(𝑎)}𝑓 (𝑤1,…,𝑤𝑚)=𝑀 when used in
the system𝑆.
The difference (𝑁 − 𝑀) expresses the amount of additional information that would be
sufficient to correct our wrong prediction, normalized over the accuracy of the system. Namely,
it expresses the amount of additional information that would be sufficient for the rule𝑊 𝑒𝑎𝑘 to
fail. Hence, these elements collectively express an amount of non-monotonicity, weighted on a
measure of certainty of the prediction:
Definition 1 (Correction Distance). The correction distance for a system (𝑆, ⊢𝑑,𝑚 ), given a
target predicate 𝑃 and an individual 𝑎, is the inverse of the amount of additional information
sufficient for 𝑆 to correct its evaluation on 𝑎, weighted on certainty (as expressed by accuracy known
for the system from previous analyses)
𝐶(𝑆, ⊢, 𝑃 (𝑎)) = 1 − (𝑁 − 𝑀) ∗ 𝑎𝑐𝑐𝑢𝑟𝑎𝑐𝑦
Given our definitions of𝑁 and 𝑀 – as the amounts of information sufficient to give, re-
spectively, a correct and an incorrect prediction – the measure𝐶 expresses an evaluation of
how far the system is from correcting a wrong classification. We have to further impose that
(𝑁 − 𝑀) > 0 if we want to model the non-monotonic setting exemplified in Section2.3, in
which an increase of the available information is assumed to always result in an improvement
(or, in a binary setting like ours, a correction) of the prediction made before (see Proposition

Figure 1: Examples of correction distance for incorrect predictions, at different levels of N and Accuracy
1). Moreover, in defining the order relation<𝑤, we said that all the weighted features of the
system’s feature space together sum to 1. Therefore,𝑁 ≤ ∑𝑛
𝑃𝑖∈ℙ 𝑤 (𝑃𝑛) = 1 . Note, finally, that
𝐶(𝑆, ⊢, 𝑃 (𝑎)) ∈ [0, 1] and that it could be interpreted as a probabilistic measure. For instance,
if 𝐶(𝑆, ⊢, 𝑃 (𝑎)) = 10% , we could say that there is a probability of90% that the system will
eventually reach the correct prediction for𝑎.
Example. Recall the anti-fraud system mentioned in previous examples. Figure
1 shows how𝐶(𝑆, ⊢, 𝑃 (𝑎)) varies in relation to𝑀, 𝑁, and accuracy, assuming that
an incorrect classification is always returned by (𝑆, ⊢𝑑,𝑚 ) for datapoint𝑎. On the
𝑥-axis we measure the available information𝑀 and on the𝑦-axis the corresponding
correction distance.
If we focus on the system denoted by the dashed yellow line, where the amount of
information required for a correct classification is60% of the total and accuracy
is known to be90%, in the virtual case in which no information is used for the
prediction, the correction distance attributed to the classification is already set at
46%. The more the system proceeds with the acquisition of new information, say
40%, the correction distance attributed to a wrong classification rises to82%.
For comparison, if we take a system with maximal accuracy (100%) and little
information required to infer a correct classification (20%), a wrong classification
without any information is already assumed to be80% distant from its correction

(dotted green line).
Finally, a system with low accuracy (80%) and which requires total information
to infer correct classifications (100%) – like the one represented by the solid blue
line – will be evaluated to be36% distant from correction for the case of𝑀 = 20% .
While with𝑀 = 90% , if a wrong is still being returned, its correction distance will
be evaluated at92%.
In the light of the above, we can now get back to the two limit cases discussed informally
at the end of Section3. In fact, we can now give a much more refined definition of a system
which is maximally (resp. minimally) distant from the correct prediction, by simply translating
Formula 1 (resp. 2) in terms of correction distance. We obtain that a system is maximally distant
from the correction of an incorrect prediction𝑃 (𝑎), based on an amount of information𝑀, then
there is no additional information𝑀′ such that the sum of𝑀 + 𝑀 ′ results in an amount of
information sufficient of predicting correctly¬𝑃 (𝑎).
Definition 2 (Maximally Distant-From-Correction System). Given (𝑆, ⊢𝑑,𝑚 , 𝑃 (𝑎)) with ∣
𝑆 ∣= 𝑀 and ∄𝑀′ s.t. 𝑀 + 𝑀 ′ = 𝑁, then 𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 (𝑎)) = 1
All things being equal, a system is correctable if there exists some additional information𝑀′
suchthatthesumof 𝑀 +𝑀 ′ resultsinanamountofinformationsufficientofpredictingcorrectly
¬𝑃 (𝑎).
Definition 3 (Correctable System). Given (𝑆, ⊢𝑑,𝑚 ) with ∣ 𝑆 ∣= 𝑀 and ∃𝑀′ s.t. 𝑀 + 𝑀 ′ = 𝑁 ,
then 𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 (𝑎)) < 1
Note that, intuitively, it makes sense to present the Correction Distance as a measure from a
possibly incorrect to a correct prediction. Nonetheless, in the next section, we make use of the
Correction Distance as a criterion to establish whether a classifier is biased towards or against a
certain class by measuring whether associated correction distances differ. In this sense, one can
even abstract from the assumption of initial incorrectness of the system, and ask what would
take for the system to change the result of a classification for a given datapoint, and whether
that amount of information is different for distinct classes of individuals.
5. Measuring Bias as Correction Distance Imbalance
To reach a proper definition of bias, we just need to accommodate the last desideratum left
unaddressed so far, i.e., the idea of skewness as “partiality of the domain affected by the error”
introducedinSection 2.1atpoint(2). Putdifferently, whileinthepreviousSectionourcorrection
distancehasbeendefinedoverasingledatapoint 𝑎, nowitmustbegeneralizedoverasubdomain
of 𝔻 in order to fully account for the notion of bias relevant in machine learning contexts.
Adopting the distinction between group (or statistical) vs. individual (or similarity-based)
unfairness criteria, well known in the bias literature [15], we first define a measure of group
unfairness in terms of imbalance of correction distance of a classifier used to predict a target
class𝑃 –denotedby 𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 )–acrossthesubdomainsof 𝔻 determinedbyabinaryprotected
category 𝑄, with respect to a tolerance threshold𝜖.

Definition 4 (Measure of Group Fairness).
𝐵𝑖𝑎𝑠𝑔𝑟𝑜𝑢𝑝 (𝑆, ⊢𝑑,𝑚 , 𝑃 ) =∣ 𝐶(𝑆, ⊢ 𝑑,𝑚 , 𝑃 (𝑎)) − 𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 (𝑏)) ∣> 𝜖
where
𝑄 ∈ ℙ𝕣, ∀𝑎, 𝑏 ∈ 𝔻 ∣ 𝑄(𝑎) ∧ ¬𝑄(𝑏)
and where 𝜖 is a threshold value for the difference of the correction measures above which fairness
is considered to fail.
Coming to the measure of individual fairness, we explore a strategy inspired by the principle
of Fairness Through Unawareness or Blindness [17, 18, 19]. To implement it, we adopt the
following similarity criterion.
In general, given two sets𝐴 and 𝐵, the Jaccard Index of𝐴 and 𝐵, denoted by𝐽 (𝐴, 𝐵), is
defined as:
Definition 5 (Jaccard Index).
𝐽 (𝐴, 𝐵) = ∣ 𝐴 ∩ 𝐵 ∣
∣ 𝐴 ∪ 𝐵 ∣
Takentwoindividuals 𝑎 and𝑏 inthetestset 𝔻,giventhesetsofthepredicatestheyrespectively
satisfy (denoted by𝕃𝑎 and 𝕃𝑏 with slight abuse of notation), they are called blindly similar –
expressed by𝐵𝑆𝑖𝑚(𝑎, 𝑏) – if and only if they only differ with respect to the protected predicate
𝑄, and they show more similarities than differences:
Definition 6 (Blind Similarity). Two datapoints 𝑎 and 𝑏 are blindly similar, denoted by
𝐵𝑆𝑖𝑚(𝑎, 𝑏) , iff:
1. (𝕃𝑎 ∪ 𝕃𝑏) ⧵ (𝕃𝑎 ∩ 𝕃𝑏) = {𝑄} ∈ ℙℝ
2. 𝐽 (𝕃𝑎, 𝕃𝑏) > 1
2
Definition 7 (Measure of Individual Unfairness).
𝐵𝑖𝑎𝑠𝐼 𝑛𝑑(𝑆, ⊢𝑑,𝑚 , 𝑃 ) =∣ 𝐶(𝑆, ⊢ 𝑑,𝑚 , 𝑃 (𝑎)) − 𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 (𝑏)) ∣> 𝜖
where
∀𝑎, 𝑏 ∈ 𝔻.𝐵𝑆𝑖𝑚(𝑎, 𝑏)
and where 𝜖 is a threshold value for the difference of the correction measures above which fairness
is considered to fail.
Namely, we define a measure for individual unfairness in terms of an imbalance in the
correction distance – denoted by𝐶(𝑆, ⊢𝑑,𝑚 , 𝑃 ) – across the subdomain of similar individuals
determined by Definition6, with respect to a tolerance threshold𝜖.

6. Further developments
We presented an attempt to bring a logical contribution to the research on fairness in machine
learning. To make this proposal complete and applicable, much work remains to be done.
First of all, it will be crucial to contextualise our approach within current technical, philo-
sophical, and logical research on bias. This means, in particular, connecting our proposal to
other recent formalisations of bias [8, 9, 10, 11] on the one hand, and to the wide literature on
fairness measures on the other. Understanding how our proposal aligns with and contributes
to the current debate on fairness will provide a better insight on its potential implications and
applications.
Secondly, formal and structural features of our logical framework need further clarification,
starting from inferential rules and semantic clauses. In this spirit, some remarks made in Section
3 highlighted that the negation rule seems to require different interpretations, based on the
setting considered (either allocative or punitive). More generally, the definition of inference
rules and semantic clauses must be functional to measure inferences (respectively, define valid
consequences) in terms of correction distance, to be used for the computation of the two fairness
measures proposed. Moreover, it will be important to further refine the notions of ground truth,
training data, and test sample.
Also a probabilistic refinement of the proposed logical framework is essential to better
model machine learning inference. A probabilistic evaluation on the target predicate, to be
interpreted as a measure of confidence or accuracy of the prediction returned by the system,
will in turn require to suitably formalise its relationship with the other used notions of quantity
of information and feature relevance.
From a semantical point of view, a modal setting may be helpful to reason about biased
predictions. Kripke models can be interpreted as sets of evaluations of attributes on datapoints,
and modalities to access new worlds can be understood as evaluations of new attributes (in-
cluding the target one). Under this interpretation, verifying that a machine learning model𝑆 is
individually fair (as defined in Definition7) relatively to a certain protected attribute means to
check as a safety property that similar possible worlds (based on the similarity definition given
in Definition6) provide access to the same possible worlds. Developing model checking and
correctness algorithms remains the main goal for the future development of the present work.
References
[1] P. Linardatos, V. Papastefanopoulos, S. Kotsiantis, Explainable ai: A review of machine
learning interpretability methods, Entropy 23 (2020) 18. URL:http://dx.doi.org/10.3390/
e23010018. doi:10.3390/e23010018 .
[2] F. A. D’Asaro, G. Primiero, Probabilistic typed natural deduction for trustworthy computa-
tions, in: Proceedings of the 22nd International Workshop on Trust in Agent Societies
(TRUST2021 @ AAMAS), 2021.
[3] F. A. D’Asaro, F. Genco, G. Primiero, Checking trustworthiness of probabilistic computa-
tions in a typed natural deduction system, 2023.arXiv:2206.12934 .
[4] F. A. Genco, G. Primiero, A typed lambda-calculus for establishing trust in probabilistic

programs, CoRR abs/2302.00958 (2023). URL:https://doi.org/10.48550/arXiv.2302.00958.
doi:10.48550/arXiv.2302.00958 . arXiv:2302.00958 .
[5] G. Primiero, F. A. D’Asaro, Proof-checking bias in labeling methods, in: G. Boella, F. A.
D’Asaro, A. Dyoub, G. Primiero (Eds.), Proceedings of 1st Workshop on Bias, Ethical AI,
Explainability and the Role of Logic and Logic Programming (BEWARE 2022) co-located
with the 21st International Conference of the Italian Association for Artificial Intelligence
(AI*IA 2022), Udine, Italy, December 2, 2022, volume 3319 ofCEUR Workshop Proceedings,
CEUR-WS.org, 2022, pp. 9–19. URL:http://ceur-ws.org/Vol-3319/paper1.pdf.
[6] R. Calegari, G. Ciatto, A. Omicini, On the integration of symbolic and sub-symbolic
techniques for XAI: A survey, Intelligenza Artificiale 14 (2020) 7–32. URL:https://doi.org/
10.3233/IA-190036. doi:10.3233/IA- 190036 .
[7] R. Calegari, F. Sabbatini, The psyke technology for trustworthy artificial intelligence,
in: A. Dovier, A. Montanari, A. Orlandini (Eds.), AIxIA 2022 - Advances in Artificial
Intelligence - XXIst International Conference of the Italian Association for Artificial
Intelligence, AIxIA 2022, Udine, Italy, November 28 - December 2, 2022, Proceedings,
volume 13796 ofLecture Notes in Computer Science , Springer, 2022, pp. 3–16. URL:https:
//doi.org/10.1007/978-3-031-27181-6_1. doi:10.1007/978- 3- 031- 27181- 6\_1 .
[8] A. Ignatiev, M. C. Cooper, M. Siala, E. Hebrard, J. Marques-Silva, Towards formal
fairness in machine learning, in: Principles and Practice of Constraint Programming:
26th International Conference, CP 2020, Louvain-La-Neuve, Belgium, September 7–11,
2020, Proceedings, Springer-Verlag, Berlin, Heidelberg, 2020, p. 846–867. URL:https:
//doi.org/10.1007/978-3-030-58475-7_49. doi:10.1007/978- 3- 030- 58475- 7_49 .
[9] Y. Kawamoto, An epistemic approach to the formal specification of statistical machine
learning, Software and Systems Modeling 20 (2020) 293–310. URL:http://dx.doi.org/10.
1007/s10270-020-00825-2. doi:10.1007/s10270- 020- 00825- 2 .
[10] V. Belle, Toward a logical theory of fairness and bias, Theory and Practice of Logic
Programming (2023) 1–19. doi:10.1017/S1471068423000157 .
[11] X. Liu, E. Lorini, A unified logical framework for explanations in classifier systems, Journal
of Logic and Computation 33 (2023) 485–515. doi:10.1093/logcom/exac102 .
[12] H. Suresh, J. V. Guttag, A framework for understanding sources of harm throughout
the machine learning life cycle, Equity and Access in Algorithms, Mechanisms, and
Optimization (2019).
[13] N. Mehrabi, F. Morstatter, N. Saxena, K. Lerman, A. Galstyan, A survey on bias and fairness
in machine learning, 2022.arXiv:1908.09635 .
[14] S. Hooker, Moving beyond “algorithmic bias is a data problem”, Patterns 2 (2021) 100241.
doi:10.1016/j.patter.2021.100241 .
[15] A.Castelnovo,R.Crupi,G.Greco,D.Regoli, Thezoooffairnessmetricsinmachinelearning,
CoRR abs/2106.00467 (2021). URL:https://arxiv.org/abs/2106.00467. arXiv:2106.00467 .
[16] S. R. Das, M. Donini, J. Gelman, K. Haas, M. Hardt, J. Katzman, K. Kenthapadi, P. Larroy,
P. Yilmaz, B. Zafar, Fairness measures for machine learning in finance, in: The Journal of
Financial Data Science, 2021.
[17] N. Grgic-Hlaca, M. B. Zafar, K. P. Gummadi, A. Weller, The case for process fairness in
learning: Feature selection for fair decision making, 2016. URL:https://api.semanticscholar.
org/CorpusID:13633339.

[18] S. Verma, J. Rubin, Fairness definitions explained, in: Proceedings of the International
Workshop on Software Fairness, FairWare ’18, Association for Computing Machinery, New
York, NY, USA, 2018, p. 1–7. URL:https://doi.org/10.1145/3194770.3194776. doi:10.1145/
3194770.3194776 .
[19] M. J. Kusner, J. R. Loftus, C. Russell, R. Silva, Counterfactual fairness, 2018.
arXiv:1703.06856 .
```
