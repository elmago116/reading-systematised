---
title: A geometric framework for fairness
author:
  - Alessandro Maggio
  - Luca Giuliani
  - Roberta Calegari
  - Michele Lombardi
  - Michela Milano
source: https://ceur-ws.org/Vol-3523/paper9.pdf
venue: AEQUITAS 2023
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
  - op/acc/extract
  - Tech/Ai/machineLearning
pdfORepub: "[[A geometric framework for fairness.pdf]]"
---

# Notes

## Full text (extracted from `2PDF/A geometric framework for fairness.pdf`)

*Extracted:* 2026-09-17

```text
A geometric framework for fairness
Alessandro Maggio1,∗, Luca Giuliani1, Roberta Calegari1, Michele Lombardi1 and
Michela Milano1
1Alma Mater Studiorum –Università di Bologna, Italy
Abstract
Fairness has emerged as a critical concern in the field of machine learning impacting its application in
various domains. While there have been successful attempts to tackle fairness, many existing analyses
rely on sophisticated mathematical methods that may lack intuitive understanding. Drawing inspiration
from successful applications in other areas of machine learning, in this study, we propose a GEOmetric
Framework for Fairness – GEOFFair – that represents distributions, ML models, fairness constraints,
and hypothesis spaces as vectors and sets. The geometric framework aims to provide a more intuitive
and rigorous understanding of fairness in Artificial Intelligence (AI). It enables visualizing mitigation
techniques as movements in the vector space and aids in constructing proofs-by-witness by quickly
identifying examples or counter-examples. Furthermore, the geometric framework offers a platform for
studying various fairness properties, including geometrical distances between fairness vectors, relative
fairness comparisons, and the exploration of symmetries, invariances, and trade-offs between fairness
metrics.
Keywords
AI fairness, geometric framework, GEOFFair
1. Introduction
Fairness issues in Machine Learning (ML) have been raised to the spotlight in recent years,
and are regarded as a major roadblock for the application of data-driven AI in fields such as
healthcare, economics, welfare, and policy-making [1].
From a mathematical point of view, studying fairness properties (or the lack thereof) in
ML models is a difficult endeavour, since it requires reasoning on statistical distributions and
(potentially) non-linear models [2]. While successful attempts in this direction exist [3], many
of the existing analyses rely on sophisticated methods that may not be easily intuitive for a
comprehensive understanding of all the objects involved in addressing fairness.
We propose that the field could gain advantages from a simplified framework that, while not
as nuanced or powerful as other statistical methods, could provide an intuitive and rigorous
grasp of some key concepts and mechanisms related to fairness in AI. Specifically, we propose
adopting aGEOmetric Framework for Fairness – GEOFFair – to represent distributions, functions
(e.g. ML models), fairness constraints, and hypothesis spaces as vectors and sets. The key
Aequitas 2023: Workshop on Fairness and Bias in AI |co-located with ECAI 2023, Kraków, Poland
∗Corresponding author.
Envelope-Open alessandro.maggio6@unibo.it (A. Maggio);luca.giuliani13@unibo.it (L. Giuliani);roberta.calegari@unibo.it
(R. Calegari);michele.lombardi2@unibo.it (M. Lombardi);michela.milano@unibo.it (M. Milano)
© 2023 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)


benefit of geometric frameworks is that they enable visualization, allowing us to gain insights
into the data or the model operation.
In terms of motivation, our approach draws from successful attempts in other areas of
ML [4, 5], where mapping models to points in vector spaces (e.g. by concatenating their
parameters) have led to simplifications in their representation and analysis. Through this
lens, distance metrics, projections, similarities, and algorithms can be applied to gain insights
into the models. Papers like [6] demonstrate the effectiveness of vector representations in
natural language processing tasks, where embracing the vector space model allows for a deeper
understandingandcomparisonofmachinelearningmodels. Similarly,webelieveourframework
can enable a better understanding and visualization of fairness issues and facilitate the study of
their properties. For example, using this approach it is possible to map mitigation techniques
for addressing fairness concerns as movements in the vector space or assist the construction of
proofs-by-witness by quickly finding examples or counter-examples.
Furthermore, the geometric framework provides a platform for studying various properties
relatedtofairness. Wecaninvestigatethegeometricaldistancesbetweenfairnessvectors, which
may provide insights into the relative fairness of different models or interventions. Additionally,
thegeometricspaceallowsforexploringsymmetries,invariances,ortrade-offsbetweendifferent
fairness metrics, contributing to a deeper understanding of the fairness landscape.
Accordingly, the paper is organized as follows. Section2 introduces the formal framework
of GEOFFair, discussing its mathematical foundation and exploring the potential relationships
among its elements. It establishes the groundwork for understanding the subsequent sections.
Then in Section3 the paper interprets fairness mitigation techniques within the context of
the proposed GEOFFair framework. It examines how these techniques can be applied and
understood through the lens of GEOFFair, providing insights and analysis. Conclusion and
future works are discussed in Section4.
2. GEOFFair: a GEOmetric Framework for Fairness
The following section aims to introduce a formal framework. To achieve this goal, we will focus
on two key points. Firstly, we will explore the vector representation of the main mathematical
objects of the framework defining the core elements and the main existing properties (Subsec-
tion 2.1, Subsection2.2). This vector representation allows us to formalize fairness concepts and
measures in a clear and precise mathematical language. Secondly, we will discuss how these
vector representations exist within the same space, providing a common basis for comparing
and contrasting different fairness measures (Subsection2.3).
2.1. From Distribution to Vectors in the Space
Classical formulations for both ML models and fairness metrics typically rely on probability
theory and statistics: for example, the ground truth is viewed as a probability distribution, the
ML model as a parameterized function, the training loss as a likelihood measure, and fairness
metrics as functions over conditional expectations. The first challenge in the definition of our
framework is therefore mapping such concepts into a vector representation, with no significant
loss of generality.

Probability Distributions and Functions We focus on a supervised learning setting, and
we start by defining a representation for (joint) probability distributions, which we approximate
to arbitrary precision via aninfinite sample. Formally:
Notation 1 (Probability Distributions). Let 𝑋 , 𝑌 be random variables with support in 𝒳 and 𝒴
and joint distribution 𝑃 (𝑋 , 𝑌 ). Then we encode the distribution as a vector (𝑥, 𝑦 ) = {𝑥 𝑖, 𝑦𝑖}𝑛
𝑖=1, with
𝑥𝑖, 𝑦𝑖 ∼ 𝑃 (𝑋 , 𝑌 )and 𝑛 → ∞ .
Intuitively,𝑋 represents an observable that may serve as the input for an ML model, while𝑌
represents the quantity (or class) to be estimated. We make no assumption about the support of
the random variables, i.e. the range of their possible values. The same representation can be
applied for the individual distributions of𝑋 and 𝑌, which are therefore denoted as𝑥 and 𝑦. Our
approach makes it particularly easy to represent functions over random variables (e.g. Machine
Learning models evaluated over their input). Formally:
Notation 2 (Functions). A deterministic function 𝑓 over 𝑋 and 𝑌 can then be naturally viewed as
a vector 𝑓 (𝑥, 𝑦 ) = {𝑓 (𝑥𝑖, 𝑦𝑖)}𝑛
𝑖=1 with 𝑛 → ∞ , i.e. just the vector with the function evaluation over
all the samples.
Functions that depend only on𝑋 or only on𝑌 are sub-cases of the above definitions and are
respectively denoted as𝑓 (𝑥) and 𝑓 (𝑦 ).
There are a few observations worth making. First, while we use the term “vector” for
simplicity, our definitions are closer to functions that map an index𝑖 to an object such as𝑥𝑖
or 𝑦𝑖. In other words,𝑥, 𝑦, 𝑓 (𝑥), etc. can be thought of as points in a Hilbert space. Second,
our representations are not exact, but they will be sufficient to approximate key statistical
properties with arbitrarily high probability. Exact representations for distributions exist and
are well known, e.g. the Probability Mass Function or Probability Density Function; however,
they do not enable constructing a simple 1-1 mapping between components in the vector (e.g.
𝑥𝑖) and function evaluations (e.g.𝑓 (𝑥𝑖)), which is instead trivial with our approach.
Equivalence of Expectation Predicates Manyoftheexistingfairnessmetricsareexpressed
in terms of (conditional) expectations, i.e. averages, or can be reduced in such a form. For
example, assuming𝑋 is a binary protected attribute, the DIDI metric from [7] is defined in
terms of the discrepancy between the global average outcome and the average outcome for
each protected group, i.e.|𝔼[𝑌 ∣ 𝑋 = 0] − 𝔼[𝑌 ]| + |𝔼[𝑌 ∣ 𝑋 = 1] − 𝔼[𝑌 ]| . Statistical parity in
classification, which advocates for similar probabilities of a positive outcome across all groups,
can be defined as|𝔼[𝑌 ∣ 𝑋 = 0] − 𝔼[𝑌 ∣ 𝑋 = 1]| , and so on. Intuitively, this means that many
fairness constraints can be viewed as predicates over (conditional) expectations.
The sample expectation function, represented by𝜇(⋅), tends to converge towards the true
expectation 𝔼[⋅] as the sample size grows: we use this result to establish a form of equivalence
between predicates expressed over a distribution and those expressed over a sample.
Theorem 1. Let Π(𝑋 , 𝑌 ) be a predicate over (conditional) expectations for 𝑋 and 𝑌 and let
𝜋 ({𝑥𝑖}𝑛
𝑖=1, {𝑦𝑖}𝑛
𝑖=1) be its sample counterpart. Then we have that:
𝑃 (Π(𝑋 , 𝑌 ) ⇔ lim𝑛→∞ 𝜋 ({𝑥𝑖}𝑛
𝑖=1, {𝑦𝑖}𝑛
𝑖=1)) = 1 (1)

i.e. the two predicates are equivalent almost surely as the sample size grows if the involved
expectations are finite.
Proof. The two predicates are identical except for the use of the true and sample expectations.
For the sake of simplicity and without loss of generality, let us assume the involved expectations
are respectively𝔼[𝑌 ] and 𝜇 ({𝑦𝑖}𝑛
𝑖=1). Since the samples are drawn independently from the same
distribution, due to the strong law of large numbers we have that:
𝑃 ( lim𝑛→∞ 𝜇 ({𝑦𝑖}𝑛
𝑖=1) = 𝔼[𝑌 ]) = 1 (2)
Equivalence of the sample and true expectations then implies equivalence ofΠ and 𝜋.
Notation 1 and Notation2 give us the ability to transition from the conventional distribution
paradigm of ML to the realm of vector spaces. Theorem1 enables reasoning over the vector
representation and translates almost certainly any result to the original distribution, at least as
far as fairness metrics are concerned. Together, these tools allow us to leverage the power and
interpretability of vector space representations in the context of fairness metrics, expanding the
scope of analysis and decision-making.
2.2. The Formal Model
As mentioned in Section2.1, we focus on a supervised learning setting where the goal is to
learn a model that maps inputs (always observable) to outputs (observable at training time and
to be estimated at inference time). In this context, we introduce four key mathematical objects
that play a major role in the analysis of fairness issues in AI.
Werepresentthe input distribution bymeansofan input vector 𝑥 ∈ 𝒳 𝑛,with 𝑛 → ∞ ,according
to Notation1. Concerning the output, we make a distinction between the distribution that can
actually be observed and the one that we ideally wish to estimate. We start by introducing the
following concept:
Definition 1 (Ground Vector). The ground vector 𝑦+ ∈ 𝒴 𝑛 represents data that can be observed
and used as ground truth to learn machine learning models. It is paired with the input vector 𝑥.
As inspired by [3], we model the fact that the ground truth might be subject to systemic
social biases, but with a key difference. That is, we directly define an “unbiased” output vector
rather than an unbiased input matrix, as our framework allows us to reason in terms of vector
components within the output space.
Definition 2 (Gold Vector). The gold vector 𝑦∗ ∈ 𝒴 𝑛 represents the “unbiased” data that corre-
sponds to the output distribution before it is corrupted by social biases; accordingly, we can derive
the ground vector 𝑦+ by considering the application of a biased mapping over the gold vector, i.e.:
𝑦+ = 𝑏(𝑦 ∗), where 𝑏 ∶ 𝒴 𝑛 → 𝒴 𝑛 is called the biased mapping
Note that in practical applications, the gold vector is typically unobservable and therefore
not accessible at training time. Still, explicitly modeling the unbiased distributions allows us to
study in deeper detail the interplay between bias and fairness constraints.

In our framework, an ML model can be viewed as a function that maps input to output data.
In supervised learning, the training process is typically viewed as that of selecting one model
out of a pool of candidates, so as to minimize a loss metric. Formally, training amounts to
solving in an exact or approximate fashion:
arg min
𝑓 ∈ℱ
ℒ (𝑓 (𝑥), 𝑦+) (3)
where𝑓 is the ML model,ℒ is the chosen loss metric andℱ represents the set of possible models,
usually defined by specifying an architecture (e.g. a number and size of layers in a feed-forward
neural network, number of estimators and maximum depth in a random forest).
In our framework, however, the input vector𝑥 is by construction fixed, thus making the
model output the only relevant factor. In other words, two models are equivalent as long as
they have the same output. This observation allows us to introduce a simplified representation
of the classical notion of hypothesis space.
Definition 3 (Hypothesis Space). The hypothesis space ̂𝕐 is the set of possible outputs for the
chosen class of ML models, i.e.
̂𝕐 = {𝑦 ∈ 𝒴 𝑛 ∣ ∃𝑓 ∈ ℱ ∶ 𝑓 (𝑥) = 𝑦 }
Intuitively, the hypothesis space can be viewed as the set of possible model outputs for the
considered sample. A linear regression model will have a limited hypothesis space due to its
ability to represent linear relationships only, while more complex models such as random forests
and neural networks will have a much larger hypothesis space.
Finally, as we are considering a fairness scenario, we need to model a final mathematical
object in order to guarantee a proper analysis of the phenomenon, namely the region in the
output space that is considered fair.
Definition 4 (Fair Space). Let 𝕐 ⊆ 𝒴 𝑛 be the set containing all the output vectors that are aligned
with the fairness requirements.
We make no assumption on the mathematical definition of the fair space. Nonetheless, it
is worth noting that in many practical cases, this set is defined by means of a threshold𝑡 on a
fairness metric𝐾, i.e.𝕐 = {𝑦 ∈ 𝒴 𝑛|𝐾 (𝑦 ) ≤ 𝑡}.
Once all the elements are defined, we can examine how they interact with each other. In
the most general setup, we can not make any assumption about the relationships between𝑦∗,
𝑦+, ̂𝕐, and𝕐. Without specific contextual information on data, models, and constraints, the
relationships between these entities can vary significantly.
It is worth mentioning that, in the defined framework, all vectors and sets we introduced
exist in the same space, which facilitates easy visualization (see Figures in Section3). This
visual representation can assist with proof-by-witness, allowing us to analyze and demonstrate
relationships between these vectors more effectively.
2.3. Relationships Between Elements
Let us now explore the four elements we discussed earlier. A summary of their potential
relationships is presented in Table1. Firstly, thanks to the problem’s symmetry, we can acquire

Table 1
Possible one-to-one relationships. When comparing the two sets, we use ̸∩ and ∩ as aliases for ̂𝕐 ∩ 𝕐 = ∅
and ̂𝕐 ∩ 𝕐 ≠ ∅, ̂𝕐, 𝕐.
̂𝕐 𝕐 𝑦+ 𝑦∗
̂𝕐 ̸∩, ⊆, ⊇, ∩ ∋, ∌ ∋, ∌
𝕐 ∋, ∌ ∋, ∌
𝑦+ ≡, ≢
𝑦∗
all potential relationships by examining the Cartesian product of the six entries found in the
upper triangular section of the table. This yields a total of 128 configurations, calculated as
4 × 25. Furthermore, we can decrease the configuration space by making a few straightforward
observations.
• 𝑦∗ ≡ 𝑦 + can hold uniquely when the two vectors belong to the same sets;
• If 𝑦∗ ∈ ̂𝕐 and 𝑦∗ ∈ 𝕐 hold simultaneously then ̂𝕐 ∩ 𝕐 ≠ ∅ , and the same applies to𝑦+;
• 𝑦∗ ∈ ̂𝕐 and 𝑦∗ ∉ 𝕐 are incompatible if ̂𝕐 ⊂ 𝕐, and the same applies to𝑦+;
• 𝑦∗ ∉ ̂𝕐 and 𝑦∗ ∈ 𝕐 are incompatible if ̂𝕐 ⊃ 𝕐, and the same applies to𝑦+.
By taking these logical constraints into account, we identified 56 distinct legal combinations,
whose listing is provided in AppendixA. While the number of possible combinations is not
small, it is nevertheless finite, which can help with proofs of universally quantified statements
(i.e. ∀ and ∄).
Now, let us examine each one-to-one relationship between these elements. With respect to
the Hypothesis and Fair Space, the possible outcomes are as follows:
̂𝕐 ∩ 𝕐 = ∅ Thisscenario impliesthat itis notpossible tolearn amodelthat satisfiesthe fairness
criteria. Although this is a rare occurrence, as most fairness metrics evaluate to zero on
constant vectors (which can generally be represented by any machine learning model), it
might still happen in certain situations. For example, this could be due to an excessively
strict threshold imposed on the fairness constraint.
̂𝕐 ⊆ 𝕐 In this case, the machine learning model is said to befair-by-design [8]. While achieving
this is challenging in many practical cases, it can be attained by incorporating explicit
rules into the model, ensuring that certain deontological fair principles are always upheld.
̂𝕐 ⊇ 𝕐 Here, the machine learning models can cover all existing fair outputs. This can be the
case when employing powerful models like large neural networks.
̂𝕐 ∩ 𝕐 ≠ ∅ This is the most common scenario encountered in practice. In this case, the goal
of learning a fair model is to find an appropriate parameter configuration such that the
output vector𝑦 belongs to the non-trivial intersection between the two sets,̂𝕐 and 𝕐.

Similarly, when considering the relationships among vectors and sets, the following consid-
erations can be made:
1. if 𝑦+ and 𝑦∗ coincide, it implies that the mapping𝑏: 𝒴 𝑛 → 𝒴 𝑛 introduces no bias.
However, this is an extremely rare scenario that leads to trivial solutions for any fairness
task. In most real-world cases, the two vectors are not aligned, indicating a discrepancy
between the information conveyed by𝑦+ and 𝑦∗. This misalignment suggests that the
ground vector has been pushed away from the unbiased distribution to some extent;
2. if 𝑦+ ∈ ̂𝕐, it can be perfectly represented by the machine learning model, although this
representation is not guaranteed to be fair unless𝑦+ is already in the Fair Space (as
mentioned in Point4 below). Conversely, when the model lacks the capacity to represent
𝑦+ adequately, it will be trained to minimize the lossℒ between the labels and the model
outputs;
3. the same considerations as in Point2 apply to the relationship between𝑦∗ and ̂𝕐. The
only difference is that, in this case, the analysis is purely theoretical since no model can
be trained on𝑦∗, which is not observable in real-world scenarios;
4. if 𝑦+ ∈ 𝕐, it means that the ground vector aligns with the fairness criteria. This alignment
can be due to various reasons, such as a weakly biased mapping that does not significantly
deviate the ground vector from the unbiased distribution, or the fairness criteria being
too permissive and allowing for a higher degree of fairness violation. Conversely, when
𝑦+ is outside the Fair Space, learning a fair model becomes more challenging as it must
explicitly account for the fairness constraints. This is the most common scenario in
real-world settings;
5. Similar to Point4, the gold vector can belong to the Fair Space or not. In most practical
use cases, it does belong, indicating that the chosen fairness metric𝐾 aligns with the
unbiased distribution and its threshold is well-tuned. However, if a misaligned metric is
chosen or a too restrictive threshold is set, it is possible for𝑦∗ ∉ 𝕐.
3. Fairness Mitigation Through the Lens of GEOFFair
Inthissection, wewillutilizetheGEOFFairframeworktoanalyzefairnessmitigationtechniques.
InapreviousworkbyDuttaetal. [ 3],itwasdemonstratedthatmaximizingaccuracysolelybased
on the observed labels vector may not always be the optimal choice. They employed statistical
distributions and mathematical tools from probability theory to establish this result. Rather
than extending their findings, our objective is to employ our proposed geometric framework to
support and validate them. By leveraging the GEOFFair framework, we aim to present similar
conclusions in a more accessible and interpretable way and can bridge the gap between complex
mathematical concepts and practical implications. This allows for a clearer comprehension of
the challenges associated with fairness and the potential solutions that can be pursued.

3.1. Mitigation as Projection
Mitigation, in the AI fairness context, refers to the process of reducing unfairness by either
transforming the biased distribution or by ensuring that the ML model behaviour is compatible
with the fairness constraints. From a geometric point of view, such techniques can be viewed
as projecting either the ground vector or the ML output onto the Fair Space. Analogously,
training an ML model can be viewed as the problem of finding a vector in the Hypothesis
Space that is closest to the ground vector in terms of the loss function, i.e. as projecting the
ground vector onto the Hypothesis Space. Therefore, in the context of GEOFFair, projections
provide a convenient lens through which we can study mitigation at pre-processing, training,
and post-processing time in a uniform fashion.
We will focus our analysis on the more widespread case where learning a fair ML model is
possible (i.e. ̂𝕐 ∩ 𝕐 ≠ ∅ ). We start by introducing two additional vectors, i.e. the projections of
the ground truths and the gold standard vector, respectively. These projections will be onto the
intersection space between the Hypothesis and the Fair Space.
Definition 5 (Ground and Gold Fair Projections). The optimal fair predictions 𝑝 and 𝑧 obtained
from the ground ( 𝑦+) and gold ( 𝑦∗) vectors, i.e.:
𝑝 = arg min
𝑣
{ℒ (𝑣 , 𝑦+) ∣ 𝑣 ∈ ̂𝕐 ∩ 𝕐} (4)
𝑧 = arg min
𝑣
{ℒ (𝑣 , 𝑦∗) ∣ 𝑣 ∈ ̂𝕐 ∩ 𝕐} (5)
Intuitively,𝑝 represents the outcome of training an ML model under fairness constraints, or
equivalently of training an ML model over a ground distribution transformed so as to enforce
the fairness restrictions. The𝑧 vector represents the best fair model that we could learn for the
(typically unobservable) “unbiased” distribution.
It is worth noting that𝑝 and 𝑧 might not be unique, as equally accurate outputs that are both
fair and representable by the model can exist. Furthermore, for the purpose of our theoretical
analysis, we will assume that𝑝 and 𝑧 are obtained from exact and globally optimal algorithms.
However, it is important to acknowledge that many machine learning models, especially larger
ones, do not guarantee this optimality property in practice. Additionally, to avoid trivial cases,
we assume that thebiased mapping function 𝑏: 𝒴 𝑛 → 𝒴 𝑛 applies a modification to the input
vector, i.e. that𝑦∗ ≢ 𝑦 +. This assumption narrows down our analysis to even fewer cases than
those defined in Subsection2.3, and let us draw the following conclusion:
ℒ (𝑦+, 𝑦∗) > 0 (6)
where ℒ is any non-negative loss function such thatℒ (𝑦+, 𝑦∗) = 0 iff 𝑦+ ≡ 𝑦 ∗.
Basic Properties of Fair Projections Let us consider the optimization problems defined
in Equations (4)-(5) and examine the behaviour of𝑝 and 𝑧 in terms of fairness based on the
position of𝑦+ and 𝑦∗, respectively. We will rely on the formulation of the Fair Space based on
a fairness metric𝐾 (⋅) that we introduced in Section2, i.e.:
𝕐 = {𝑦 ∈ 𝒴 𝑛 ∣ 𝐾 (𝑦 ) ≤ 𝑡} (7)

Before establishing a fundamental property of fair projections, let us introduce some notation
to describe the concept ofFair Space Frontier. It can be described as:
Notation 3 (Fair Frontier).
𝜕 𝕐 = {𝑦 ∈ 𝒴 𝑛 ∣ 𝐾 (𝑦 ) = 𝑡} (8)
The Fair Space Frontier represents the boundary of the Fair Space, namely the region of the
space containing all the vectors exhibiting a threshold-level fairness. Likewise, we can introduce
the concept ofInternal Fair Set, which encompasses the vectors within the Fair Space but not on
the Fair Frontier:
Notation 4 (Internal Fair Set).
Δ𝕐 = 𝕐 ⧵ 𝜕 𝕐 = {𝑦 ∈ 𝒴 𝑛 ∣ 𝐾 (𝑦 ) < 𝑡} (9)
Property 1 (Fair Projections). Given a vector 𝑦 and its projection 𝑦′ onto the Fair Space as defined
in Equation (7), we know that:
𝑦 ∈ 𝕐 ⟹ 𝑦 ′ ≡ 𝑦 ⟹ 𝐾 (𝑦 ′) = 𝐾 (𝑦 ) (10)
𝑦 ∉ 𝕐 ⟹ 𝑦 ′ ∈ 𝜕 𝕐 ⟹ 𝐾 (𝑦 ′) = 𝑡 (11)
meaning that any vector lying within the Fair Space will be projected onto itself (thus exhibiting
the same fairness level); conversely, if the vector is outside the Fair Space, its projection will be on
the boundary of the Fair Space, resulting in threshold-level fairness.
This is a well-known property in both convex and non-convex optimization, whose proof can
be found in [9]. Now, if we take into account the capabilities of the ML model, we can extend
Property 1 as follows:
Property 2 (Representable Fair Projections). Given a vector 𝑦 and its projection 𝑦′ onto the
intersection between the Fair and Hypothesis Space, we know that:
𝑦 ∈ 𝕐 ∨ ̂𝕐 ⊆ 𝕐 ⟹ 𝐾 (𝑦 ′) ≤ 𝑡 (12)
𝑦 ∉ 𝕐 ∧ ̂𝕐 ⊇ 𝕐 ⟹ 𝐾 (𝑦 ′) = 𝑡 (13)
It is important to note that when the Fair Space and the Hypothesis Space have a non-trivial
intersection – i.e. neither space is a subset of the other –, we cannot draw conclusions about
𝐾 (𝑦′) since points in the boundary of the intersection can exhibit different fairness levels.
3.2. Possible Cases Configuration
Based on the properties and assumptions discussed in the previous subsection, we can now
outline five distinct cases that summarize the different combinations arising from the positions
of the input vectors (𝑦+ and 𝑦∗) and their projections (𝑝 and 𝑧). Each case description is
accompanied by illustrative figures, where blue stripes represent the region where the ground
projection 𝑝 can fall, and green stripes indicate the region where the gold projection𝑧 can
fall; additionally, the figures depict two possible ground and gold vectors, along with their
projections. On a final note, we underline that these cases are mutually exclusive, meaning that
the conditions of each subsequent case implicitly exclude the conditions of the previous ones .

Figure 1: Graphical representation of Case 1. Projections 𝑝 and 𝑧 cannot coincide, although they can
both fall in the same region as highlighted by the green and blue stripes.
Case 1: 𝑦+, 𝑦∗ ∈ ̂𝕐∩𝕐. Thisisatrivialscenarioinwhichbothvectorsarealreadyrepresentable
and satisfy the fair condition. As shown in Figure1, in this case, the projections coincide with
the original vectors, therefore we know that:
ℒ (𝑝, 𝑧) = ℒ (𝑦 +, 𝑦∗) > 0 (14)
where the strict inequality follows from having assumed a non-trivial biased mapping, i.e.
from Equation (6). The existence of a gap even in this simple scenario shows that maximizing
accuracy based on the biased data (under fairness constraints) may not always yield the best
solution. Furthermore, we have that:
𝐾 (𝑝) ⋚ 𝐾 (𝑧) (15)
In other words, there is also no guarantee that the gold projection is fairer than the ground
projection. Suchavarietyofpossibleoutcomesisduetothefactthatthiscasecapturessituations
where fairness constraints are not particularly restrictive, so applying mitigation techniques is
not really meaningful.
Case 2: 𝑦+, 𝑦∗ ∈ Δ𝕐 ∨ ̂𝕐 ⊆ 𝕐. We can identify two sub-cases within this scenario. In the first
sub-case, both the gold vector and the ground vector satisfy the fairness criteria, even if at
least one of them does not belong to the Hypothesis Space – this distinction is necessary to
avoid falling back intoCase 1. In the second one, the ML model isfair-by-design, meaning that
any possible output is guaranteed to be within the Fair Space. Intuitively, the former sub-case
reflects another situation where fairness constraints are not particularly restrictive; in the latter,
fairness issues have already been addressed by acting on the model architecture. Although these
two sub-cases might look very different, the resulting projections exhibit the same behaviour.
In fact, similar toCase 1, 𝑝 and 𝑧 may be arbitrarily close or far, depending on the positions of
the two original vectors, and no mutual information on𝐾 (𝑝) and 𝐾 (𝑧) can be obtained. This
observation stresses the potential impact of the chosen class of models (the Hypothesis Space)
on the outcome of mitigation approaches.
Case 3: 𝑦+ ∉ Δ 𝕐 ∧ 𝑦 ∗ ∈ Δ 𝕐. In this case, the ground target𝑦+ is either outside or at the
frontier of𝕐, meaning that there is a non-null gap in terms of the fairness metric between itself

(a) 𝑦+, 𝑦∗ ∈ Δ𝕐.
 (b) ̂𝕐 ⊆ 𝕐.
Figure 2: Graphical representation of Case 2. The represented vectors show an illustrative scenario
where both the vectors are outside the Hypothesis Space, although at most one of them can belong to
the intersection of the two sets.
(a) 𝕐 ⊆ ̂𝕐.
 (b) 𝕐 ⊈ ̂𝕐.
Figure 3: Graphical representation of Case 3. In this case, we are guaranteed that a fairer and more
accurate solution would exist if the Fair Space is completely contained in the Hypothesis Space (Figure a).
Whenever this does not happen (Figure b), such a property cannot be formally proven.
and the gold vector (which is in the Fair Space).
Again, we can identify two main sub-cases, depending on the position of the Hypotheses
Space with respect to the Fair Space. Since we are assuming that the intersection between the
two sets is not empty, and the scenario in whicĥ𝕐 is a subset of𝕐 has been already covered in
Case 2, the possible outcomes are: (a)𝕐 ⊆ ̂𝕐, or (b)𝕐 ⊈ ̂𝕐. In the former (Figure3a), mitigation
has a beneficial effect in terms of fairness, but a guaranteed gap will remain wrt the best possible
fair project, since Property2 guarantees that𝐾 (𝑝) = 𝑡 > 𝐾 (𝑧) . In this situation, as long as the
fairness metric is sufficiently aligned with the unbiased distribution (i.e.𝑦∗ ∈ 𝕐), better results
can be obtained by simply making the fairness constraints more restrictive.
On the contrary, in the latter sub-case (Figure3b), nothing can be said on the fairness level
of 𝑝 as Property2 does not cover the case of non-trivial intersection. This suggests that using
sufficiently expressive model classes (e.g. larger neural networks) in mitigation approaches may

lead to more consistent outcomes, at least as long as overfitting is successfully prevented.
As a final consideration, we underline thatCase 3 is the most common real-world scenario ,
as it assumes that a non-trivial, strong enough biased mapping is applied to𝑦∗, and that the
fairness metric is both aligned and correctly calibrated on it.
Case 4: 𝑦+ ∈ Δ𝕐 ∧ 𝑦 ∗ ∉ Δ𝕐. Contrarily to the previous case, here the positions of the ground
and gold vectors are swapped. This is a very unlikely scenario, which is implied by the adoption
of a wrong fairness metric that is aligned with the biased data but not with the unbiased one.
As forCase 3, we can distinguish among two different sub-cases. When𝕐 ⊆ ̂𝕐 (Figure 4a), we
are guaranteed that there could be a better solution with respect to the gold vectors, although
in this case this solution would exhibit ahigher degree of unfairness due to Property2. On the
contrary (Figure4b), nothing can be proven, but the same considerations ofCase 3 remain.
(a) 𝕐 ⊆ ̂𝕐.
 (b) 𝕐 ⊈ ̂𝕐.
Figure 4: Graphical representation of Case 4. This is the opposite of Figure 3, where a misaligned
fairness metric makes the gold vector more unfair than the ground one.
(a) 𝕐 ⊄ ̂𝕐.
 (b) 𝕐 ⊂ ̂𝕐.
Figure 5: Graphical representation of Case 5. In this case, the misaligned fairness metric makes both
the gold and ground vectors unfair.

Case 5: 𝑦+, 𝑦∗ ∉ Δ 𝕐. Finally, we consider the case in which the fairness metric is either
misaligned or wrongly calibrated for both vectors. The usual sub-cases (Figure5a: 𝕐 ⊆ ̂𝕐,
and Figure5b: 𝕐 ⊈ ̂𝕐) can be identified, with similar conclusions as forCase 3 and Case 4. In
fact, in the former one, we are guaranteed that the level of fairness of𝑝 and 𝑧 will coincide
independently from the position of the original vectors since they will both fall on the Fair
Space Frontier. On the contrary, no property can be proven for the latter sub-case.
3.3. Fairness Threshold Analysis
The threshold𝑡 plays a significant role in distinguishing different cases among those mentioned
earlier. For example, by analyzing the effect of decreasing𝑡 in Case 1 we observe that when𝕐 is
more aligned to𝑦∗ than 𝑦+, it results inCase 3; conversely, if it is more aligned with𝑦+ than
𝑦∗, it may result inCase 4. Continuously lowering𝑡 eventually leads toCase 5, and while we
can intuitively observe that decreasing the threshold results in closer projections𝑝 and 𝑧, we
yet have no formal proof of the relationship between𝑡 and the lossℒ (𝑝, 𝑦∗).
4. Conclusion
This study introduces GEOFFair – a GEOmetric Framework for Fairness – which leverages
geometrical concepts to provide a rigorous and intuitive understanding of fairness in AI. By
representing distributions, ML models, fairness constraints, and hypothesis spaces as vectors
and sets, GEOFFair allows for visualizing mitigation techniques and constructing proofs-by-
witness. The framework facilitates the exploration of various fairness properties, including
geometrical distances between fairness vectors, relative fairness comparisons, and the analysis
of symmetries, invariances, and trade-offs between fairness metrics.
Through the lens of GEOFFair, we conducted a theoretical analysis of mitigation techniques,
leadingtotheidentificationoffivedistinctcasesthatareessentialforanalyzingdifferentfairness
scenarios. These cases provide valuable insights into the relationship between input vectors,
their projections, and the fairness level achieved.
Future work will focus on applying GEOFFair to analyze well-known fairness problems.
Geometrical reasoning and projection might also prove very effective for understanding how
properties of the loss function and fairness metrics (e.g. convexity, triangle inequality) affect
the effectiveness of mitigation techniques.
Finally, exploring the generation of biased data to assess the fairness of AI applications
through the lens of GEOFFair will be an important avenue for future research. Overall, the
adoption of the GEOFFair framework holds promise for advancing the understanding and
development of fair AI systems.
Acknowledgments
The work has been partially supported by the AEQUITAS project funded by the European
Union’s Horizon Europe Programme (Grant Agreement No. 101070363), by the EU ICT-48 2020
project TAILOR (No. 952215) and by PNRR - M4C2 - Investimento 1.3, Partenariato Esteso

PE00000013 - ”FAIR - Future Artificial Intelligence Research” - Spoke 8 ”Pervasive AI”, funded
by the European Commission under the NextGeneration EU programme.
References
[1] N. Mehrabi, F. Morstatter, N. Saxena, K. Lerman, A. Galstyan, A survey on bias and fairness
in machine learning, ACM Computing Surveys (CSUR) 54 (2021) 1–35.
[2] M. Srivastava, H. Heidari, A. Krause, Mathematical notions vs. human perception of
fairness: A descriptive approach to fairness for machine learning, in: Proceedings of the
25th ACM SIGKDD international conference on knowledge discovery & data mining, 2019,
pp. 2459–2468.
[3] S. Dutta, D. Wei, H. Yueksel, P.-Y. Chen, S. Liu, K. Varshney, Is there a trade-off between
fairness and accuracy? a perspective using mismatched hypothesis testing, in: International
Conference on Machine Learning, PMLR, 2020, pp. 2803–2813.
[4] I. Kansizoglou, L. Bampis, A. Gasteratos, Deep feature space: A geometrical perspective,
IEEE Transactions on Pattern Analysis and Machine Intelligence 44 (2021) 6823–6838.
[5] M. M. Bronstein, J. Bruna, Y. LeCun, A. Szlam, P. Vandergheynst, Geometric deep learning:
going beyond euclidean data, IEEE Signal Processing Magazine 34 (2017) 18–42.
[6] O. Shahmirzadi, A. Lugowski, K. Younge, Text similarity in vector space models: a compara-
tivestudy, in: 201918thIEEEinternationalconferenceonmachinelearningandapplications
(ICMLA), IEEE, 2019, pp. 659–666.
[7] S. Aghaei, M. J. Azizi, P. Vayanos, Learning optimal and fair decision trees for non-
discriminative decision-making, in: The Thirty-Third AAAI Conference on Artificial
Intelligence, AAAI 2019, The Thirty-First Innovative Applications of Artificial Intelli-
gence Conference, IAAI 2019, The Ninth AAAI Symposium on Educational Advances
in Artificial Intelligence, EAAI 2019, Honolulu, Hawaii, USA, January 27 - February 1,
2019, AAAI Press, 2019, pp. 1418–1426. URL:https://doi.org/10.1609/aaai.v33i01.33011418.
doi:1 0 . 1 6 0 9 / a a a i . v 3 3 i 0 1 . 3 3 0 1 1 4 1 8.
[8] V. Nurock, R. Chatila, M.-H. Parizeau, What does “ethical by design” mean?, Reflections on
Artificial Intelligence for Humanity (2021) 171–190.
[9] P. Jain, P. Kar, Non-convex Optimization for Machine Learning, 2017. doi: 1 0 . 1 5 6 1 /
9 7 8 1 6 8 0 8 3 3 6 9 0.

A. Possible Scenarios
Let ℤ be 𝒴 ⧵ ( ̂𝕐 ∪ 𝕐).
Scenario ̂𝕐 ∩ 𝕐 = ∅
Cases in which𝑦 ∗ ∈ 𝕐:
1) 𝑦∗, 𝑦+ ∈ 𝕐 and 𝑦∗ ≡ 𝑦 +.
2) 𝑦∗, 𝑦+ ∈ 𝕐 and 𝑦∗ ≢ 𝑦 +.
3) 𝑦∗ ∈ 𝕐 and 𝑦+ ∈ ℤ.
4) 𝑦∗ ∈ 𝕐 and 𝑦+ ∈ ̂𝕐.
Cases in which𝑦 ∗ ∉ 𝕐:
5) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≡ 𝑦 +.
6) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≢ 𝑦 +.
7) 𝑦∗ ∈ ℤ and 𝑦+ ∈ 𝕐.
8) 𝑦∗ ∈ ℤ and 𝑦+ ∈ ̂𝕐.
9) 𝑦∗, 𝑦+ ∈ ̂𝕐 and 𝑦∗ ≡ 𝑦 +.
10) 𝑦∗, 𝑦+ ∈ ̂𝕐 and 𝑦∗ ≢ 𝑦 +.
11) 𝑦∗ ∈ ̂𝕐 and 𝑦+ ∈ ℤ.
12) 𝑦∗ ∈ ̂𝕐 and 𝑦+ ∈ 𝕐.
Scenario 𝕐 ⊂ ̂𝕐
Cases in which𝑦 ∗ ∈ 𝕐:
13) 𝑦∗, 𝑦+ ∈ 𝕐 and 𝑦∗ ≡ 𝑦 +.
14) 𝑦∗, 𝑦+ ∈ 𝕐 and 𝑦∗ ≢ 𝑦 +.
15) 𝑦∗ ∈ 𝕐 and 𝑦+ ∈ ̂𝕐 ⧵ 𝕐.
16) 𝑦∗ ∈ 𝕐 and 𝑦+ ∈ ℤ.
Cases in which𝑦 ∗ ∉ 𝕐:
17) 𝑦∗, 𝑦+ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦∗ ≡ 𝑦 +.
18) 𝑦∗, 𝑦+ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦∗ ≢ 𝑦 +.

19) 𝑦∗ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦+ ∈ 𝕐.
20) 𝑦∗ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦+ ∈ ℤ.
21) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≡ 𝑦 +.
22) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≢ 𝑦 +.
23) 𝑦∗ ∈ ℤ and 𝑦+ ∈ ̂𝕐 ⧵ 𝕐.
24) 𝑦∗ ∈ ℤ and 𝑦+ ∈ 𝕐.
Scenario ̂𝕐 ⊂ 𝕐
Cases in which𝑦 ∗ ∈ 𝕐:
25) 𝑦∗, 𝑦+ ∈ ̂𝕐 and 𝑦∗ ≡ 𝑦 +.
26) 𝑦∗, 𝑦+ ∈ ̂𝕐 and 𝑦∗ ≢ 𝑦 +.
27) 𝑦∗ ∈ ̂𝕐 and 𝑦+ ∈ 𝕐 ⧵ ̂𝕐.
28) 𝑦∗ ∈ ̂𝕐 and 𝑦+ ∈ ℤ.
29) 𝑦∗, 𝑦+ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦∗ ≡ 𝑦 +.
30) 𝑦∗, 𝑦+ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦∗ ≢ 𝑦 +.
31) 𝑦∗ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦+ ∈ ̂𝕐.
32) 𝑦∗ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦+ ∈ ℤ.
Cases in which𝑦 ∗ ∉ 𝕐:
33) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≡ 𝑦 +.
34) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≢ 𝑦 +.
35) 𝑦∗ ∈ ℤ and 𝑦+ ∈ 𝕐 ⧵ ̂𝕐.
36) 𝑦∗ ∈ ℤ and 𝑦+ ∈ ̂𝕐.
Scenario ̂𝕐 ∩ 𝕐 ≠ ∅ and not a previous case
Cases in which𝑦 ∗ ∈ 𝕐:
37) 𝑦∗, 𝑦+ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦∗ ≡ 𝑦 +.
38) 𝑦∗, 𝑦+ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦∗ ≢ 𝑦 +.
39) 𝑦∗ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦+ ∈ 𝕐 ∩ ̂𝕐.

40) 𝑦∗ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦+ ∈ ̂𝕐 ⧵ 𝕐.
41) 𝑦∗ ∈ 𝕐 ⧵ ̂𝕐 and 𝑦+ ∈ ℤ.
42) 𝑦∗, 𝑦+ ∈ 𝕐 ∩ ̂𝕐 and 𝑦∗ ≡ 𝑦 +.
43) 𝑦∗, 𝑦+ ∈ 𝕐 ∩ ̂𝕐 and 𝑦∗ ≢ 𝑦 +.
44) 𝑦∗ ∈ 𝕐 ∩ ̂𝕐 and 𝑦+ ∈ ̂𝕐 ⧵ 𝕐.
45) 𝑦∗ ∈ 𝕐 ∩ ̂𝕐 and 𝑦+ ∈ 𝕐 ⧵ ̂𝕐.
46) 𝑦∗ ∈ 𝕐 ∩ ̂𝕐 and 𝑦+ ∈ ℤ.
Cases in which𝑦 ∗ ∉ 𝕐:
47) 𝑦∗, 𝑦+ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦∗ ≡ 𝑦 +.
48) 𝑦∗, 𝑦+ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦∗ ≢ 𝑦 +.
49) 𝑦∗ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦+ ∈ 𝕐 ∩ ̂𝕐.
50) 𝑦∗ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦+ ∈ 𝕐 ⧵ ̂𝕐.
51) 𝑦∗ ∈ ̂𝕐 ⧵ 𝕐 and 𝑦+ ∈ ℤ.
52) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≡ 𝑦 +.
53) 𝑦∗, 𝑦+ ∈ ℤ and 𝑦∗ ≢ 𝑦 +.
54) 𝑦∗ ∈ ℤ and 𝑦+ ∈ ̂𝕐 ⧵ 𝕐.
55) 𝑦∗ ∈ ℤ and 𝑦+ ∈ 𝕐 ∩ ̂𝕐.
56) 𝑦∗ ∈ ℤ and 𝑦+ ∈ 𝕐 ⧵ ̂𝕐.
```
