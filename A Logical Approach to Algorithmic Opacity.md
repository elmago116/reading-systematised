---
title: A Logical Approach to Algorithmic Opacity
author:
  - Mattia Petrolo
  - Ekaterina Kubyshkina
  - Giuseppe Primiero
source: https://ceur-ws.org/Vol-3615/short4.pdf
venue: BEWARE 2023
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
pdfORepub: "[[A logical approach to algorithmic opacity.pdf]]"
---

# Notes

## Full text (extracted from `2PDF/A logical approach to algorithmic opacity.pdf`)

*Extracted:* 2026-09-17

```text
A logical approach to algorithmic opacity
Mattia Petrolo1, Ekaterina Kubyshkina2 and Giuseppe Primiero2
1University of Lisbon, CFCUL, Alameda da Universidade, 1649-004 Lisbon, Portugal
2University of Milan, Philosophy Department, Via Festa del Perdono, 7 20122, Milan, Italy
Abstract
In [1], we introduced a novel definition for the epistemic opacity of AI systems. Building on this, we
proposed a framework for reasoning about an agent’s epistemic attitudes toward a possibly opaque
algorithm, investigating the necessary conditions for achieving epistemic transparency. Unfortunately,
this logical framework faced several limitations, primarily due to its overly idealized nature and the
absence of a formal representation of the inner structure of AI systems. In the present work, we address
these limitations by providing a more in-depth analysis of classifiers using first-order evidence logic.
This step significantly enhances the applicability of our definitions of epistemic opacity and transparency
to machine learning systems.
Keywords
Transparent AI, epistemic opacity, epistemic logic, evidence models, neighborhood semantics
1. Introduction
Recently, the use of computational algorithms has significantly increased across different
areas of human life, leading to the development of explainable AI and other human-centered
approaches aimed at understanding the nature of AI models. One common issue discussed
in these approaches is the epistemic opacity problem, that is, a problem about the epistemic
accessibilityandreliabilityofalgorithms. Inthisstudy,weaimtoprovideanovelepistemological
and logical analysis of this problem in order to identify the conditions under which this form of
opacity can be eliminated.
This work builds upon the insights we introduced in [1]. In this instance, we present a
new and more expressive formal framework that holds promise for accurately representing an
agent’s epistemic attitude regarding the opacity of an AI system.
2. An epistemological definition of opacity
To characterize the epistemic opacity of algorithms, we follow the methodology proposed by
Durán and Formanek [2] and adapt Humphreys’ definition of epistemically opaque process:
2nd Workshop on Bias, Ethical AI, Explainability and the role of Logic and Logic Programming, BEW ARE-23, co-located
with AIxIA 2023, Roma Tre University, Rome, Italy, 2023
Envelope-Open mpetrolo@fc.ul.pt (M. Petrolo);ekaterina.kubyshkina@unimi.it (E. Kubyshkina);giuseppe.primiero@unimi.it
(G. Primiero)
© 2022 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
CEUR
Workshop
Proceedings
http://ceur-ws.org
ISSN 1613-0073
CEUR Workshop Proceedings (CEUR-WS.org)
CEUR
Workshop
Proceedings
ceur-ws.org
ISSN 1613-0073

[A] process is epistemically opaque relative to a cognitive agent X at time t just in
case X does not know at t all of the epistemically relevant elements of the process
(Humphreys [3], p. 618).
This characterization of opacity relies on the fact that an agent “X does not know,” which,
in turn, requires a definition of what knowledge is. However, Humphreys’ account leaves
this question unanswered, since he does not touch upon the question of what “knowledge of
an algorithm” is. Traditional epistemology defines knowledge as corresponding to justified
true belief, but this analysis has been challenged by Gettier[4] famous counterexample, which
prevents one to consider luck-dependent cases as cases of genuine knowledge. To avoid this
problem, our characterization of opacity must carefully consider the justificatory component
involved in the analysis. Additionally, in order to specify which elements of algorithms are
epistemically relevant, we must take into account their specific structure. Cormen et al.[5]
describe an algorithm as “any well-defined computational procedure that takes some value, or
set of values, as input and produces some value, or set of values, as output” (p. 5). This can
be seen as a minimal characterization of algorithm, containing the minimal elements one has
to take into account. Although informal and brief, this characterization highlights three key
elements of an algorithm: its input, procedure, and output. We argue that a sound definition
of epistemic opacity (and transparency) for algorithms must take these elements into account.
Our proposal is as follows:
An algorithm isepistemically opaque relative to an epistemic agentA at timet just
in case att, A does not have
an epistemic justification for I,
or an epistemic justification for P,
or an epistemic justification for O;
where I, P, O express the algorithm’s input, procedure, and output, respectively.
The previous definition has an important feature: the components I, P, and O of the algorithm
are related, but irreducible one to another. As a consequence, the lack of epistemic justification
for any component constitutes a sufficient condition for epistemic opacity. In theory, the three
conditions can occur independently, but in most real-world algorithms, these forms of opacity
are interconnected, which complicates the epistemic opacity problem. Based on this definition,
in most cases, the algorithms we interact with on a daily basis are epistemically opaque. Our aim
is here is to present a formal framework to reason about an agent’s epistemic attitudes towards
opaque algorithms and examine the conditions required for achieving epistemic transparency.
The aforementioned epistemological definition of algorithmic opacity is not new; we in-
troduced it in [1]. In that work, we also outlined a logical framework to formally represent
opacity. However, the framework we presented in [1] has two primary limitations. First, the
formal representation of epistemic justification for input and output is overly idealized and
simplified. Second, the relationship between input, procedure, and output is left implicit due to
the absence of a formal representation of their inner structure. Consequently, connecting these
three elements in a unified setting is challenging. In our current work, we address both of these

limitations, enhancing the applicability of our definitions to machine learning (ML) systems
and providing a more detailed analysis of classifiers using first-order evidence logic.
3. Formal framework
To reason formally about an agent’s epistemic attitudes towards opacity, it is necessary to
reformulate the definition of opaque algorithm in logical terms. In order to do so, we utilize
tools from epistemic logic and express the epistemic justification for each component by using
a specific modality.
Before delving into the formal semantics, let us fix some terminology to bridge the charac-
terization of an algorithm used in the epistemological definition with the actual architecture
of machine learning systems. In particular, from now on, we refer to the model of a given
classifier trained using supervised learning. The input is usually calledtest set and it consists of
data points, which are evaluated on the basis of the labels of the training set. The procedure
can be divided into thetraining set and themodel. The training set consists of labelled data
points. The model consists ofparameters (features taken into account),hyperparameters (the
‘significance’ attributed to each feature), atarget (the predicate one wants to classify for), and a
mathematical function corresponding to the chosen learning algorithm, which evaluates the
input with respect to the target. Finally, the output consists of thedata points of the test set
with labels attributed according to the criteria of the trained model.
The semantics we are proposing is a first-order extension of a neighborhood semantics for
evidence logic provided by van Benthem et al. [6].
The languageℒ is defined as follows:
𝜙 ∶= 𝑥 ∣ 𝑃 (𝑥) ∣ ¬𝜙 ∣ 𝜙 ∧ 𝜙 ∣ ∀𝑥𝜙 ∣ □𝜙 ∣ 𝐵𝜙 ∣ 𝐾 𝜙
Definition 3.1. A first-order evidence model is a tuple ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩, where 𝑊 is a
non-empty set of worlds, 𝐸 ⊆ 𝑊 × 𝔭(𝑊 ) is an evidence relation, 𝐷 is a non-empty set, for each 𝑤,
𝑉𝑤 is a function that to each 𝑛-place predicate symbol assigns a subset of 𝐷𝑛. We write 𝐸(𝑤 ) for
the set {𝑋 ∣ 𝑤 𝐸𝑋 } . Two constraints are imposed on the evidence sets: For each 𝑤 ∈ 𝑊 , ∅ ∉ 𝐸(𝑤 )
and 𝑊 ∈ 𝐸(𝑤 ) .
Definition 3.2. A 𝑤-scenario is a maximal collection 𝒳 ⊆ 𝐸(𝑤 ) that has the finite intersection
property: for each finite subfamily {𝑋1, ..., 𝑋𝑛} ⊆ 𝒳 , ∩1≤𝑖≤𝑛𝑋𝑖 ≠ ∅.
Definition 3.3. Let ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩. An assignment 𝑔 is a function that to each variable
assigns an element of 𝐷. Given assignments 𝑔 and 𝑔′, 𝑔′ ∼𝑥 𝑔 means that 𝑔′ agrees with 𝑔 on all
variables save possibly 𝑥. The relation ℳ, 𝑔, 𝑤 ⊧ 𝜙 is defined by induction, where 𝑤 is a world, 𝑔 is
an assignment, and 𝜙 is a formula of first-order modal logic.
• ℳ, 𝑔, 𝑤 ⊧ 𝑃 (𝑥 1, ..., 𝑥𝑛) iff (𝑔(𝑥1), ..., 𝑔(𝑥𝑛)) ∈ 𝑉 𝑤(𝑃 )
• ℳ, 𝑔, 𝑤 ⊧ 𝜙 ∧ 𝜓 iff ℳ, 𝑔, 𝑤 ⊧ 𝜙 and ℳ, 𝑔, 𝑤 ⊧ 𝜓
• ℳ, 𝑔, 𝑤 ⊧ ¬𝜙 iff ℳ, 𝑔, 𝑤 ̸⊧ 𝜙
• ℳ, 𝑔, 𝑤 ⊧ ∀𝑥𝜙 iff for any 𝑔′ ∼𝑥 𝑔, ℳ, 𝑔′, 𝑤 ⊧ 𝜙

• ℳ, 𝑔, 𝑤 ⊧ □𝜙 iff there exists 𝑋 such that 𝑤 𝐸𝑋 and for all 𝑤′ ∈ 𝑋, ℳ, 𝑔, 𝑤 ′ ⊧ 𝜙
• ℳ, 𝑔, 𝑤 ⊧ 𝐵𝜙 iff for each 𝑤-scenario 𝒳 and for all 𝑤′ ∈ ∩𝒳, ℳ, 𝑔, 𝑤 ′ ⊧ 𝜙
• ℳ, 𝑔, 𝑤 ⊧ 𝐾 𝜙 iff for all 𝑤′ ∈ 𝑊, ℳ, 𝑔, 𝑤 ′ ⊧ 𝜙
A formula 𝜙 is said to be true at the world 𝑤 if ℳ, 𝑔, 𝑤 ⊧ 𝜙 ; otherwise it is said to be false at 𝑤.
If ℳ, 𝑔, 𝑤 ⊧ 𝜙 for every world 𝑤, ℳ, 𝑔 ⊧ 𝜙 . If ℳ, 𝑔 ⊧ 𝜙 for any assignment 𝑔, ℳ ⊧ 𝜙 .
In what follows, we consider that the worlds of𝑊 represent epistemic possibilities for an
agent. The evidence relation𝐸 associates each world with sets of evidences considered by the
agent. The domain𝐷 ranges over data points of the possible test set. Finally,𝑉𝑤 is a usual
valuation function.
Now we are able to define epistemic justification (EJ) for I, P, and O.
Definition 3.4 (EJ for I). Let 𝑎1, ..., 𝑎𝑛 be data points of an input 𝐼, 𝑃1, ..., 𝑃𝑚 are mutually exclu-
sive and exhaustive parameters of a classifier 𝐶. An agent has an epistemic justification for input
𝐼 to the classifier 𝐶 in a world 𝑤 iff for all 𝑎𝑖 ∈ 𝐼 , ℳ, 𝑔, 𝑤 ⊧ ¬𝐾 ¬(±𝑃 1(𝑎𝑖) ∧ ... ∧ ±𝑃 𝑚(𝑎𝑖)), where
±𝑃𝑗∈[1,𝑚] (𝑎𝑖) stands either for 𝑃𝑗(𝑎𝑖), or ¬𝑃𝑗(𝑎𝑖), depending whether 𝑎𝑖 satisfies the property checked
by the parameter 𝑃𝑗.
This definition can be explained as follows. We consider that an input is constituted of data
points 𝑎1, ...,𝑎𝑛. These data points can have (or not) the features evaluated by the parameters
of the classifier. We say that an input is epistemically justified iff the agent considers as an
epistemic possibility the fact that data points of the input can be correctly evaluated by the
parameters of the classifier. In other words, there exists an epistemic state of the agent such
that it validates the matching (or not) between the data points and the parameters. Formally,
there exists𝑤′ s.t. for all𝑎𝑖 ∈ {𝑎 1, ..., 𝑎𝑛} ℳ, 𝑔, 𝑤 ′ ⊧ ±𝑃 1(𝑎𝑖) ∧ ... ∧ ±𝑃 𝑚(𝑎𝑖), where±𝑃𝑗∈[1,𝑚] (𝑎𝑖)
stands either for𝑃𝑗(𝑎𝑖), or¬𝑃𝑗(𝑎𝑖).
Definition 3.5 (EJ for P). Let 𝑅 be a process which transforms an input 𝐼 into an output 𝑂,
𝑎1, ..., 𝑎𝑛 are data points of the input 𝐼, 𝑃1, ..., 𝑃𝑚 are mutually exclusive and exhaustive parameters
of a classifier 𝐶, 𝑇 is the target. An agent has an epistemic justification for process 𝑃 in a world 𝑤
iff ℳ, 𝑔, 𝑤 ⊧ ∀𝑥 □𝑅(𝑥, ±𝑃1(𝑥) ∧ ... ∧ ±𝑃 𝑚(𝑥), 𝑇 (𝑥))), where ±𝑃𝑗∈[1,𝑚] (𝑥) stands either for 𝑃𝑗(𝑥), or
¬𝑃𝑗(𝑥), depending whether 𝑎𝑖 satisfies the property checked by the parameter 𝑃𝑗.
As for the definition of the epistemic justification for the procedure, we say that there is
such a justification iff for any input the agent has an evidence for a process which transforms it
into the output (the matching of the data points’ features with the parameters) with respect to
the target. Formally this amounts to say that for any𝑥 there is a neighbourhood, in which all
worlds validate𝑅(𝑥, (±𝑃1(𝑥) ∧ ... ± 𝑃 𝑚(𝑥)), 𝑇 (𝑥)). Notice, that this does not mean that𝑅 is the
only process which can transform the input into the output.
Definition 3.6 (EJ for O). Let 𝑅 be a process which transforms an input 𝐼 into an output 𝑂,
𝑎1, ..., 𝑎𝑛 are data points of the input 𝐼, 𝑃1, ..., 𝑃𝑚 are mutually exclusive and exhaustive parameters
of a classifier 𝐶, 𝑇 is a target. An agent has an epistemic justification for output 𝑂 in a world 𝑤 iff
for all 𝑎𝑖 ∈ 𝐼 ℳ, 𝑔, 𝑤 ⊧ ¬𝐵¬𝑅(𝑎 𝑖, ±𝑃1(𝑎𝑖) ∧ ... ∧ ±𝑃𝑚(𝑎𝑖), 𝑇 (𝑎𝑖)), where ±𝑃𝑗∈[1,𝑚] (𝑎𝑖) stands either for
𝑃𝑗(𝑎𝑖), or ¬𝑃𝑗(𝑎𝑖), depending whether 𝑎𝑖 satisfies the property checked by the parameter 𝑃𝑗.

Wesaythatanagenthasanepistemicjustificationfortheoutput, onceshedoesnotdisbelieve
the result of processing the input (matching its features with the parameters) with respect to the
target. Formally, this means that there exists a world𝑤′ in the intersection of all𝑤-scenarios,
such that the result of the process𝑅(𝑎𝑖, ±𝑃1(𝑎𝑖) ∧ ... ∧ ±𝑃𝑚(𝑎𝑖), 𝑇 (𝑎𝑖))) is valid in𝑤′.
As a consequence, we obtain the following definition of epistemic opacity for classifiers.
Definition 3.7. Let 𝑅 be a process which transforms an input 𝐼 into am output 𝑂, 𝑎1, ..., 𝑎𝑛 are data
points of the input 𝐼, 𝑃1, ..., 𝑃𝑚 are mutually exclusive and exhaustive parameters of a classifier 𝐶, 𝑇
is a target. A classifier 𝐶, defined as before, is epistemically opaque ( 𝒪 𝐶) relative to an epistemic
agent in a world 𝑤 ∈ ℳ if:
ℳ, 𝑔, 𝑤 ⊧ 𝒪 𝐶 iff for all 𝑎𝑖 ∈ {𝑎1, ..., 𝑎𝑛} ℳ, 𝑔, 𝑤 ⊧ 𝐾 ¬(±𝑃 1(𝑎𝑖) ∧ ... ∧ ±𝑃𝑚(𝑎𝑖)) ∨ ¬∀𝑥□𝑅(𝑥, ±𝑃1(𝑥) ∧
... ∧ ±𝑃𝑚(𝑥), 𝑇 (𝑥)) ∨ 𝐵¬(𝑎 𝑖, ±𝑃1(𝑎𝑖) ∧ ... ∧ ±𝑃𝑚(𝑎𝑖), 𝑇 (𝑎𝑖)).
Nowletusapplyourdefinitiontoasimplifiedexampleofanagentinteractingwithaclassifier
which distinguishes photos of dogs from other images. An agent inserts a photo of a cat, that is,
the data point of the test set is𝑎. The classifier processes the images by evaluating them on
three parameters: the form of the head (𝑃1), the form of the nose (𝑃2), and the length of the
whiskers (𝑃3). Let the inserted image match the parameter𝑃1 (that is, the form of the head of
the cat on the image corresponds to the form of the head considered as suitable for a dog in the
training set), but not the parameters𝑃2 and 𝑃3. The target is to determine whether the input is
an image of a dog.
Example 3.1 (Transparent classifier).
In accordance with the Def. 3.7, the classifier is considered to be transparent for an agent once
she has an epistemic justifications for all the three components: 𝐼, 𝑃, and 𝑂. In our example, this
means that: (1) ℳ, 𝑔, 𝑤 ⊧ ¬𝐾 ¬(𝑃 1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎)), (2) ℳ, 𝑔, 𝑤 ⊧ ∀𝑥 □𝑅(𝑥, ±𝑃1(𝑥) ∧ ±𝑃2(𝑥) ∧
𝑃3(𝑥), 𝑇 (𝑥)), and (3) ℳ, 𝑔, 𝑤 ⊧ ¬𝐵¬(𝑎, 𝑃 1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎), 𝑇 (𝑎)).
Let us provide an example of such model 1. Let ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩, such that 𝑊 = {𝑤 , 𝑤 ′},
𝐸(𝑤 ) = {{𝑤 , 𝑤 ′}, {𝑤′}}, 𝐷 = {𝑎, 𝑏} , 𝑉𝑤′ (𝑃1) = {𝑎, 𝑏} , 𝑉𝑤′ (𝑃2) = {𝑏} , 𝑉𝑤′ (𝑃3) = {𝑏} , 𝑉𝑤′ (𝑇 ) = {𝑎, 𝑏} ,
𝑉𝑤′ (𝑅) = {(𝑎, 𝑃 1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎), 𝑇 (𝑎)), (𝑏, 𝑃1(𝑏) ∧ 𝑃2(𝑏) ∧ 𝑃3(𝑏), 𝑇 (𝑏))}.
In this model, (1) is satisfied because ℳ, 𝑔, 𝑤 ′ ⊧ 𝑃1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎). Clause (2) is satisfied
because {𝑤′} ∈ 𝐸(𝑤 ) , ℳ, 𝑔, 𝑤 ′ ⊧ 𝑅(𝑎, 𝑃 1(𝑎) ∧ ¬𝑃 2(𝑎) ∧ ¬𝑃 3(𝑎), 𝑇 (𝑎)), and ℳ, 𝑔, 𝑤 ′ ⊧ 𝑅(𝑏, 𝑃 1(𝑏) ∧
𝑃2(𝑏) ∧ 𝑃 3(𝑏), 𝑇 (𝑏)). Clause (3) is satisfied because there exists a 𝑤-scenario {{𝑤 , 𝑤′}, {𝑤′}} such
that 𝑤′ ∈ ∩{{𝑤 , 𝑤′}, {𝑤′}} and ℳ, 𝑔, 𝑤 ′ ⊧ 𝑅(𝑎, 𝑃1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎), 𝑇 (𝑎)).
Intuitively, (1) means that the agent considers all the parameters of the classifier and considers
as an epistemic possibility the correct matching between the information presented on the photo of
a cat and these parameters. Clause (2) means that for all possible inputs the agent has an evidence
that the process evaluates them with respect to the target. Clause (3) means that the agent does not
disbelieve the result provided by the classifier.
Example 3.2 (Lack of EJ for I).
Let ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩ where 𝑊 = {𝑤 , 𝑤 ′}, 𝐷 = {𝑎, 𝑏} , 𝑉𝑤(𝑃1) = 𝑉 𝑤′ (𝑃1) = {𝑏} . In this
case ℳ, 𝑔, 𝑤 ⊧ 𝐾 ¬(𝑃 1(𝑎) ∧ ¬𝑃2(𝑎) ∧ ¬𝑃3(𝑎)) because none of the worlds satisfies 𝑃1(𝑎). Intuitively,
1We define only relevant aspects of this model. The omitted definitions are not essential for the purposes of this
example.

this corresponds to the situation in which the agent does not consider the correct matching between
parameters and the photo as possible. This can be so, for instance, because the agent is unaware
that the form of the head ( 𝑃1) is a parameter for the classifier, or, simply, because she is convinced
that the form of a cat’s head cannot match the form of the dog’s head.
Example 3.3 (Lack of EJ for P).
Let ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩, where 𝑊 = {𝑤 , 𝑤 ′}, 𝐸(𝑤 ) = {{𝑤 , 𝑤 ′}, 𝑤′}, 𝐷 = {𝑎, 𝑏} , 𝑉𝑤′ (𝑅) =
{(𝑎, ¬𝑃1(𝑎) ∧ 𝑃 2(𝑎) ∧ 𝑃 3(𝑎)}. In this model, ℳ, 𝑔, 𝑤 ⊧ ¬∀𝑥 □𝑅(𝑥, ±𝑃1(𝑥) ∧ ±𝑃 2(𝑥) ∧ 𝑃 3(𝑥), 𝑇 (𝑥))
because ℳ, 𝑔, 𝑤 ′ ⊧ ¬𝑅(𝑏, ±𝑃1(𝑏)∧±𝑃 2(𝑏)∧±𝑃 3(𝑏), 𝑇 (𝑏)). Intuitively, this corresponds to a situation
in which an agent does not have evidence for a process to evaluate a possible input 𝑏, independently
of her evidences about evaluating the image 𝑎. For instance, in our example, the agent might have
evidences for the process to match the relevant data point of the image of a cat with corresponding
parameters with a target of determining that it is not an image of a dog. However, she might not
have evidences for evaluating another image of a wolf.
Example 3.4 (Lack of EJ for O).
Let ℳ = ⟨𝑊 , 𝐸, 𝐷, {𝑉 𝑤}𝑤 ∈𝑊⟩, where 𝑊 = {𝑤 , 𝑤 ′}, 𝐸𝑤 = {{𝑤 , 𝑤 ′}, {𝑤′}}, 𝐷 = {𝑎, 𝑏} , 𝑉𝑤(𝑅) =
𝑉𝑤′ (𝑅) = {(𝑏, ±𝑃 1(𝑏) ∧ ±𝑃 2(𝑏) ∧ ±𝑃 3(𝑏), 𝑇 (𝑏))}. In this model, ℳ, 𝑔, 𝑤 ̸⊧¬𝐵¬𝑅(𝑎, 𝑃1(𝑎) ∧ ¬𝑃 2(𝑎) ∧
¬𝑃3(𝑎), 𝑇 (𝑎)), because for each 𝑤-scenario 𝒳, for all 𝑤″ ∈ ∩𝒳, ℳ, 𝑔, 𝑤 ″ ⊧ ¬𝑅(𝑎, 𝑃1(𝑎) ∧ ¬𝑃2(𝑎) ∧
¬𝑃3(𝑎), 𝑇 (𝑎)). Intuitively, this corresponds to a situation in which an agent disbelieves the output
of the classifier. For instance, the image of the cat inserted by the agent is evaluated as a dog. This
contradicts the agent’s belief, thus indicating that the classifier is opaque for her.
4. Conclusion
In [1], we dubbed the analysis provided by the modal framework we introduced theIPO model
of algorithmic opacity . This framework provides an original epistemological definition of
algorithmic opacity based on a tripartite analysis of algorithms. On this foundation, it conceives
epistemic opacity as a (non-primitive) modal operator. It is true that the framework we are
presenting in this current work is more intricate and might seem less intuitive compared to the
one outlined in [1]. However, we believe that the complexity of these definitions in the current
setting stems from the intricate relationships between I, P, and O and their corresponding
epistemic justifications. Consequently, this complexity is a trade-off necessary for our analysis
to be effectively applied to real-world ML systems. In future work, our aim is to further develop
the IPO model, focusing on both its epistemological and formal aspects. Epistemologically,
we plan to compare the definitions we introduced with various forms of opacity examined in
the literature (e.g., as discussed by Burrell[7], Creel[8], Boge[9], Facchini and Termine[10]).
This comparison will help ascertain if our definition is comprehensive enough to encompass
all possible forms of opacity. From a formal standpoint, the next natural step is to introduce
a logical system for reasoning about opacity and prove its completeness with respect to the
evidence models. Additionally, we aim to compare our framework with other logical formalisms
that appear to offer flexibility in representing the fundamental concepts of the IPO model (see,
e.g., [11] and [12]).

Acknowledgments
The authors acknowledge the support of the Project PRIN2020 BRIO - Bias, Risk and Opacity
in AI (2020SSKZ7R) awarded by the Italian Ministry of University and Research (MUR). The
research of Ekaterina Kubyshkina is funded under the “Foundations of Fair and Trustworthy
AI” Project of the University of Milan. Giuseppe Primiero and Ekaterina Kubyshkina are further
funded by the Department of Philosophy “Piero Martinetti” of the University of Milan under
the Project “Departments of Excellence 2023-2027” awarded by the Ministry of University and
Research (MUR). Mattia Petrolo acknowledges the financial support of the FCT – Fundação
para a Ciência e a Tecnologia (2022.08338.CEECIND; R&D Unit Grants UIDB/00678/2020 and
UIDP/00678/2020) and the French National Research Agency (ANR) through the Project ANR-
20-CE27-0004.
References
[1] E. Kubyshkina, M. Petrolo, Reasoning about algorithmic opacity, in: G. Boella, F. A.
D’Asaro, A. Dyoub, G. Primiero (Eds.), Proceedings of the 1st Workshop on Bias, Ethical
AI, Explainability and the role of Logic and Logic Programming, AIxIA Series, CEUR
Workshops Proceedings, 2023, pp. 39–45.
[2] J. Durán, N. Formanek, Grounds for trust: Essential epistemic opacity and computational
reliabilism, Minds and Machines 28 (2018) 645–666.
[3] P. W. Humphreys, The philosophical novelty of computer simulation methods, Synthese
169 (2009) 615–626.
[4] E. Gettier, Is justified true belief knowledge?, Analysis 23 (1963) 121–123.
[5] T. Cormen, C. E. Leiserson, R. Rivest, C. Stein, Introduction to Algorithms, Cambridge:
MIT Press, 2009.
[6] J. van Benthem, D. Fernández-Duques, E. Pacuit, Evidence logic: A new look at neighbor-
hood structures, Advances in Modal Logic (2012).
[7] J. Burrell, How the machine ‘thinks’: Understanding opacity in machine learning algo-
rithms, Big Data & Society 2 (2016) 1–12.
[8] K. A. Creel, Transparency in complex computational systems, Philosophy of Science 87
(2020) 568–589.
[9] F. J. Boge, Two dimensions of opacity and the deep learning predicament, Minds and
Machines 32 (2022) 43–75.
[10] A. Facchini, A. Termine, Towards a taxonomy for the opacity of ai systems, in: V. C.
Muller (Ed.), Philosophy and Theory of Artificial Intelligence 2021, volume 63 ofStudies in
Applied Philosophy, Epistemology and Rational Ethics , Springer, 2022, pp. 73–89.
[11] X. Liu, E. Lorini, A logic of “black box” classifier systems, in: A. Ciabattoni, E. Pimentel,
R. de Queiroz (Eds.), Logic, Language, Information, and Computation. WoLLIC 2022,
volume 13468 ofLecture Notes in Computer Science , Springer, 2022, pp. 158–174.
[12] S. Artemov, The logic of justification, The Review of Symbolic Logic 1 (2008) 477–513.
```
