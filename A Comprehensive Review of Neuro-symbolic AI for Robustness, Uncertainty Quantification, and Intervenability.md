---
title: A Comprehensive Review of Neuro-symbolic AI for Robustness, Uncertainty Quantification, and Intervenability
author: Kamal Acharya, Houbing Song
year: "2025"
Type: Journal Article
DOI: 10.1007/s13369-025-10887-3
source: https://doi.org/10.1007/s13369-025-10887-3
created: 2026-08-05
description: Abstract As Artificial Intelligence (AI) systems are increasingly deployed in high-stakes domains such as healthcare, autonomous systems, finance, and critical infrastructure, ensuring their trustworthiness has become imperative. This paper presents a comprehensive survey of neuro-symbolic AI, a hybrid paradigm that combines the learning capabilities of neural networks with the r
tags:
  - tech/NeSyAI
  - tech/AI
  - themes/ethics
  - op/acc/leer
  - research_method/ScopingReview
  - tech/evaluation
pdfORepub: "[[A Comprehensive Review of Neuro-symbolic AI for Robustness, Uncertainty Quantification, and Intervenability.pdf]]"
---
[[A Comprehensive Review of Neuro-symbolic AI for Robustness, Uncertainty Quantification, and Intervenability.pdf]]

> **Abstract:** Abstract
                  As Artificial Intelligence (AI) systems are increasingly deployed in high-stakes domains such as healthcare, autonomous systems, finance, and critical infrastructure, ensuring their trustworthiness has become imperative. This paper presents a comprehensive survey of neuro-symbolic AI, a hybrid paradigm that combines the learning capabilities of neural networks with the r
## Full text (extracted from `A Comprehensive Review of Neuro-symbolic AI for Robustness, Uncertainty Quantification, and Intervenability.pdf`)

*Source:* `2PDF/A Comprehensive Review of Neuro-symbolic AI for Robustness, Uncertainty Quantification, and Intervenability.pdf`  
*Extracted:* 2026-08-06

```text
Arabian Journal for Science and Engineering (2026) 51:35–67
https://doi.org/10.1007/s13369-025-10887-3
REVIEW ARTICLE-COMPUTER ENGINEERING AND COMPUTER SCIENCE
A Comprehensive Review of Neuro-symbolic AI for Robustness,
Uncertainty Quantiﬁcation, and Intervenability
Kamal Acharya 1 · Houbing Song 1
Received: 30 May 2025 / Accepted: 2 November 2025 / Published online: 9 December 2025
© The Author(s) 2025
Abstract
As Artiﬁcial Intelligence (AI) systems are increasingly deployed in high-stakes domains such as healthcare, autonomous
systems, ﬁnance, and critical infrastructure, ensuring their trustworthiness has become imperative. This paper presents a com-
prehensive survey of neuro-symbolic AI, a hybrid paradigm that combines the learning capabilities of neural networks with the
reasoning strengths of symbolic AI, through the lens of three foundational dimensions: robustness, uncertainty quantiﬁcation
(UQ), and intervenability. We ﬁrst establish the limitations of purely data-driven “black-box” models in handling distribution
shifts, ambiguous inputs, and human oversight. In contrast, neuro-symbolic systems offer enhanced interpretability, veriﬁa-
bility, and control, making them promising candidates for real-world deployment. We systematically review state-of-the-art
techniques for modeling robustness, quantifying uncertainty, and enabling intervenability. We further examine how logic,
probability, and learning can be integrated into uniﬁed or modular architectures to support transparent, adaptive reasoning.
Finally, we outline current challenges and identify key research opportunities for advancing neuro-symbolic AI as a trust-
worthy paradigm. This survey aims to equip researchers and practitioners with a structured understanding of how to build
reliable, interpretable, and interactive AI systems by bridging statistical learning and symbolic reasoning.
Keywords Neuro-symbolic AI · Robustness · Uncertainty quantiﬁcation · Intervenability · Trustworthy AI
1 Introduction
The rapid deployment of Artiﬁcial Intelligence (AI) across
diverse domains, ranging from autonomous vehicles and
healthcare to ﬁnance, and critical infrastructure, has under-
scored the imperative for these systems to operate in a
manner that is both safe and trustworthy [ 1]. As AI solutions
increasingly permeate our everyday lives, the shortcom-
ings of traditional, purely data-driven “black-box” models
become more pronounced. These models, while powerful,
often exhibit unpredictable failure modes when faced with
unanticipated scenarios or noisy data, thereby eroding user
trust and raising concerns about their reliability in high-
stakes applications [ 2]. This growing dependency on AI thus
B Houbing Song
songh@umbc.edu
Kamal Acharya
kamala2@umbc.edu
1 Information Systems, University of Maryland Baltimore
County, 1000 Hilltop Circle, Baltimore, Maryland 21250,
USA
necessitates a critical reassessment of how such systems are
designed, evaluated, and ultimately deployed in real-world
settings.
AI is fundamentally transforming engineering systems
and decision-making processes by introducing new paradigms
of automation and data analysis that were previously unattain-
able. This transformation, however, brings forth signiﬁcant
challenges in ensuring the reliability, accountability, and
oversight of these complex systems. In this context, three
interdependent pillars, robustness [ 3], uncertainty quantiﬁ-
cation (UQ) [ 4], and intervenability [ 5] emerge as crucial for
enhancing the trustworthiness of AI-driven decision-making.
Robustness ensures that models maintain performance under
varied and unforeseen conditions, UQ provides a measure
of conﬁdence in the model’s predictions, and intervenabil-
ity enables human operators to effectively intervene when
necessary, thereby ensuring that AI systems can be safely
integrated into critical applications.
Addressing these challenges requires approaches that go
beyond conventional deep learning frameworks, and this is
where neuro-symbolic AI offers a promising alternative [ 6].
By integrating the adaptive learning capabilities of neural net-
123

36 Arabian Journal for Science and Engineering (2026) 51:35–67
works with the structured, rule-based reasoning of symbolic
systems, neuro-symbolic methods are uniquely positioned
to enhance system robustness, provide reliable uncertainty
measures, and facilitate human intervention when required.
This synergy not only mitigates the inherent limitations
of black-box models but also leverages explicit domain
knowledge and logical reasoning to manage complexity. As
neuro-symbolic architectures scale, they hold the potential
to signiﬁcantly improve the interpretability and controllabil-
ity of AI systems, thereby paving the way for more resilient
and trustworthy applications in real-world environments [ 7].
Table 1 offers a comparative perspective on the capabilities
of symbolic, neural, and neuro-symbolic paradigms, empha-
sizing the strengths of neuro-symbolic AI and underscoring
its growing preference in high-stakes, data-efﬁcient AI appli-
cations.
Neuro-symbolic AI has witnessed signiﬁcant growth in
interest and research activity over the past decade, emerg-
ing as a prominent area of exploration at the intersection
of symbolic reasoning and neural computation. A substan-
tial body of scholarly work has been dedicated to advancing
this paradigm, reﬂecting its increasing relevance in address-
ing complex cognitive and decision-making tasks. Existing
survey papers on neuro-symbolic AI predominantly are gen-
eral survey [ 8] or focus on its applications across diverse
domains such as cybersecurity [ 9], military operations [ 10],
and the enhancement of other AI techniques, including rein-
forcement learning [ 7] and knowledge graph reasoning [ 11].
Some studies also address its validation and veriﬁcation [ 12].
While these works collectively advocate neuro-symbolic AI
as a promising approach for real-world deployment, they
often overlook a critical question: What criteria must neuro-
symbolic AI models fulﬁll to be recognized as truly viable for
real-world applications? In this survey, we aim to bridge this
gap by identifying and analyzing three foundational factors
essential for establishing neuro-symbolic AI as a trustworthy
paradigm: robustness, UQ, and intervenability.
The paper is organized into multiple sections, as illustrated
in Figure 1, to systematically address the research objectives.
Section 1 introduces the topic and lays the foundation for the
rest of the paper. Section 2 presents the background and pre-
liminaries, offering an overview of neuro-symbolic AI along
with key concepts such as robustness, UQ, and intervenabil-
ity. Sections 3, 4, and 5 delve into how neuro-symbolic AI
can address challenges associated with robustness, UQ, and
intervenability, respectively. Section 6 explores the integra-
tion of logic, probability, and learning as a uniﬁed framework
to enhance the capabilities of neuro-symbolic systems. Sec-
tion 7 provides the insight about the real-world applications
of neuro-symbolic AI. Section 8 highlights the current limita-
tions and challenges faced by neuro-symbolic AI approaches.
Section 9 discusses practical applications and future oppor-
tunities where neuro-symbolic AI can be leveraged for
Table 1 Comparing the paradigms
Capability Symbolic Neural Neuro-symbolic
Robustness ✗ Rule sensitive ✗ Adversarially brittle ▲ Symbolic guards improve resilience
Uncertainty quantiﬁcation ✗ Limited probabilistic logic ✗ Adhoc conﬁdence ▲ Bayesian layers + logical guards
Intervenability ✓ Editable rules ✗ Opaque weights ▲ Editable symbolic layer without re-training
Interpretability ✓ Transparent rules ✗ Opaque weights ▲ Logic trace around learnt modules
Data Efﬁciency ✓ Few examples ✗ Large labeled sets ▲ Prior knowledge + learning
Reasoning ✓ Deductive, abductive ✗ Limited compositional reasoning ▲ Differentiable reasoning layers
Transfer/Fine-tuning ✗ Brittle rule porting across domains ✓ Fine tune with few examples ▲ Combines frozen neural backbone with domain-speciﬁc rules
Scalability ✗ State-space explosion ✓ Handles high-dimensional data ▲ Neural front-end + symbolic back-end
Compute / carbon cost ✓ Lightweight search ✗ Energy-hungry training ▲ Smaller models + priors
Legend: ✓ = strong; ✗ = weak; ▲ = Improved
123

Arabian Journal for Science and Engineering (2026) 51:35–67 37
Fig. 1 Overview of the Survey Paper
real-world impact. Section 10 concludes the paper by sum-
marizing the key insights and suggesting potential directions
for future research.
2 Background and Preliminaries
2.1 Neuro-Symbolic AI
Neuro-symbolic AI represents a convergence of two histor-
ically distinct paradigms in AI: the data-driven, inductive
learning methods by neural networks and the rule-based,
deductive reasoning structures central to symbolic AI. Fig-
ure 2 shows the overview of the interaction of two AI methods
to give neuro-symbolic approach. Neural network models
leverage large-scale data to learn distributed representa-
tions like feature vectors through backpropagation, achieving
remarkable performance in perception tasks such as image
recognition, natural language understanding, and speech
processing [13]. Meanwhile, symbolic AI focuses on manip-
ulating symbols, building knowledge graphs, and applying
logical inference rules to derive consistent and explainable
outcomes [ 11]. While each approach holds distinct advan-
tages, neither alone entirely satisﬁes the broader vision of
human-like intelligence, which demands both robust pattern
recognition and high-level reasoning.
In neuro-symbolic AI, the goal is to unify these paradigms,
thereby capitalizing on their complementary strengths. The
“inductive learning” capacity of neural networks excels at
discovering latent patterns from unstructured or noisy data
and generalizing to new instances. Symbolic AI, on the
other hand, operates with explicit knowledge representa-
tions, enabling interpretability, rule-based reasoning, and
systematic extension to new tasks via logical inference. By
integrating both, a neuro-symbolic system aspires to har-
ness the efﬁciency and scalability of neural networks while
preserving the transparency and veriﬁability inherent in sym-
bolic reasoning [ 6]. A key driver behind this integration is
the quest for explainability. Neural networks, despite their
impressive predictive power, are often criticized as “black
boxes” because their internal decision processes are chal-
lenging to interpret and debug. Symbolic representations,
however, allow for explicit explanations and traceable deci-
sion paths. In combination, neuro-symbolic AI methods aim
123

38 Arabian Journal for Science and Engineering (2026) 51:35–67
Fig. 2 Overview of Neuro-symbolic AI
to provide human-interpretable logic behind predictions [ 6].
For instance, in a hybrid architecture, the neural compo-
nent can process raw data (e.g., images or text), transform it
into a symbolic representation, and then employ a symbolic
inference engine to arrive at a logically consistent conclu-
sion. Another advantage of neuro-symbolic approaches lies
in lifelong learning and knowledge transfer. Symbolic AI
systems excel at retaining structured knowledge, once a rule
or fact is learned, it can be utilized and updated without hav-
ing to retrain the entire system. Neural models, on the other
hand, often need retraining or ﬁne-tuning to adapt to new
tasks or domains. When combined, the system can incre-
mentally incorporate new symbols, facts, or inference rules
while leveraging the feature extraction prowess of the learned
neural components.
Building on the developments in Inductive Learning and
Deductive Reasoning, neuro-symbolic AI emerges as an
“ideal solution” that seeks to combine data-driven gen-
eralization with robust logical formalism. This synergy
enables novel capabilities, such as (i) extracting structured
knowledge from raw data, (ii) dynamically generating new
symbolic representations for novel concepts learned by the
neural network, and (iii) using knowledge-based reasoning
to reﬁne and guide neural inference. Taken together, these
advancements pave the way for AI systems that can reason,
learn, and explain, moving us closer to the original vision of
AI as a ﬁeld that aspires to replicate the richness and versa-
tility of human intelligence.
2.1.1 Classiﬁcation of Neuro-Symbolic AI
Numerous researchers have contributed frameworks for
understanding how neural and symbolic paradigms can
be effectively combined to form neuro-symbolic systems.
This section synthesizes three foundational perspectives that
123

Arabian Journal for Science and Engineering (2026) 51:35–67 39
Table 2 Bader and Hitzler’s Multidimensional Classiﬁcation of Neuro-symbolic AI
Axis Dimension Description
Interrelation Integrated vs Hybrid Hybrid systems use multiple techniques running in parallel;
integrated systems embed symbolic knowledge within a
neural architecture.
Neuronal vs Connectionist Neuronal models focus on cognitive plausibility; connectionist
models emphasize computational reasoning capabilities.
Local vs Distributed Representation Describes whether symbolic knowledge is encoded locally or
distributed across neural networks.
Standard vs Non-standard Standard systems use conventional techniques like
backpropagation; non-standard architectures may better
represent structured knowledge but often reduce learning
capacity.
Language Symbolic vs Logical Symbolic uses structured data (e.g., graphs); logical systems
rely on formal logic expressions.
Propositional vs First-order Differentiates between simple propositional logic and more
expressive ﬁrst-order logic.
Usage Extraction vs Representation Determines whether information is extracted from activations
or explicitly symbolically represented.
Learning vs Reasoning Separates systems focusing on learning patterns from those
emphasizing logical inference.
provide taxonomies for classifying and analyzing neuro-
symbolic AI architectures.
Bader and Hitzler’s Classiﬁcation
To systematize the diverse landscape of neuro-symbolic
AI, Bader and Hitzler [14] propose a multidimensional classi-
ﬁcation framework that organizes existing approaches along
three principal axes: Interrelation, Language, and Usage.
Each axis is subdivided into several independent dimensions,
allowing for granular differentiation between systems.
Table 2 provides the summary of the classiﬁcation of
neuro-symbolic along various dimensions as purposed by
Bader and Hitzler.
Henry Kautz’s Classiﬁcation
Henry Kautz identiﬁed six distinct types of neuro-
symbolic architectures, each deﬁned by how neural and sym-
bolic modules interact [ 15]. These types reﬂect increasing
degrees of architectural coupling and cognitive inspiration:
• Symbolic Neuro-symbolic
This architecture represents the prevailing standard oper-
ating procedure (SOP) in many modern systems where
symbolic data are present in the input or output. Symbolic
inputs are ﬁrst transformed into vector representations,
processed entirely through neural networks, and then re-
symbolized at the output stage. An illustrative example
is the Aylien multilingual sentiment analysis model [ 16],
which delivers robust end-to-end performance across lan-
guages while abstracting away from language-speciﬁc
symbolic processing.
• Symbolic[Neuro]
In this hybrid paradigm, neural modules are embedded
as subcomponents within symbolic reasoning systems,
typically for perceptual tasks such as image or speech
recognition. Symbolic logic handles the core decision-
making and strategic planning. Notable instantiations
include AlphaGo [ 17], AlphaZero [ 18], and common-
sense reasoning frameworks for autonomous driving
systems [ 19].
• Neuro | Symbolic
This architecture follows a pipeline conﬁguration, where
a neural module processes raw inputs to produce sym-
bolic representations, which are subsequently consumed
by a symbolic reasoner. Feedback from the symbolic
module is then used to iteratively reﬁne the neural
model. A prime example is the Neuro-Symbolic Con-
cept Learner (NS-CL) [ 20], which learns to map visual
scenes and textual descriptions to symbolic structures for
downstream reasoning tasks.
• Neuro: Symbolic → Neuro
In this approach, symbolic rules are treated as struc-
tured inputs that are compiled into the neural architecture
during training. The symbolic knowledge is thereby dis-
tilled into the neural parameters, enabling the model
to generalize beyond seen examples. This paradigm is
exempliﬁed by works such as Deep Learning for Sym-
bolic Mathematics [ 21], where models are trained to
perform algebraic manipulations on previously unseen
expressions.
123

40 Arabian Journal for Science and Engineering (2026) 51:35–67
• Neuro_{Symbolic}
Here, symbolic structures are directly encoded into the
architecture of neural networks. Rather than relying on
external reasoning modules, the logic is integrated within
the network’s representational scheme. Techniques such
as Tensor Product Representations (TPRs) [ 22] and
Logic Tensor Networks (LTNs) [ 23] operationalize this
fusion by embedding logical constraints into the learning
dynamics.
• Neuro[Symbolic]
This conﬁguration incorporates symbolic reasoning
directly into the internal mechanisms of neural systems,
facilitating complex and combinatorially rich reason-
ing capabilities. The inspiration for this architecture is
drawn from cognitive theories, such as Daniel Kahne-
man’s dual-process model of cognition [ 24]. Though
inspired by models of cognition, it certainly does not
model the brain at what Marr called the implementa-
tion level[ 25] and may even differ at the algorithmic
level.
Yu’s Classiﬁcation
The primary methodology for categorizing neuro-symbolic
AI is based on the mode of integration between symbolic and
neural components. This results in three core architectures:
learning for reasoning, reasoning for learning, and learn-
ing–reasoning [ 26]. Figure 3 shows various approaches used
by Y u to classify the neuro-symbolic AI.
• Learning for Reasoning
In learning for reasoning systems, neural networks are
employed to augment or enable symbolic reasoning pro-
cesses by either reducing the symbolic search space
or abstracting structured representations from raw data.
This integration leverages the pattern recognition and
generalization capabilities of deep learning to overcome
combinatorial challenges inherent in symbolic reasoning,
particularly in domains like program synthesis, logical
inference, and visual question answering. Neural com-
ponents may act as heuristic guides or as translators that
convert unstructured modalities (e.g., images, text) into
symbolic formats, thus making them amenable to deduc-
tive reasoning engines. Garcez et al. [ 27] demonstrate
how structured rules can be extracted from sub-symbolic
features and used in logic-based tasks, highlighting
the synergy between data-driven learning and symbolic
inference.
• Reasoning for Learning
Reasoning for learning inverts the conventional ﬂow,
positioning symbolic systems as scaffolds for neural
learning by encoding domain knowledge through logical
constraints, rules, or auxiliary supervision. Symbolic pri-
ors are introduced during training, often through loss reg-
ularization, constrained optimization, or differentiable
logic encodings, to guide neural networks toward seman-
tically consistent predictions. This paradigm enhances
interpretability, sample efﬁciency, and safety in learn-
ing, particularly in domains where logical consistency is
critical (e.g., knowledge graph completion, autonomous
systems, and medical diagnostics). By embedding sym-
bolic structure into the learning dynamics, these systems
mitigate issues of overﬁtting, hallucination, and spuri-
ous correlations that are prevalent in purely data-driven
models. Hu et al. [ 28] introduce logic rules into the train-
ing of deep neural networks via posterior regularization,
improving generalization while enforcing structured con-
sistency.
• Learning-Reasoning
The learning–reasoning paradigm embodies the tightest
integration of neural and symbolic paradigms, estab-
lishing a bidirectional interplay where both modules
iteratively inform and reﬁne each other. Neural compo-
nents extract structured hypotheses or perceptual cues,
while symbolic modules perform inference, impose log-
ical coherence, and feed back structured signals for
further reﬁnement. Such systems are typically realized
via joint training mechanisms or differentiable rea-
soning frameworks, enabling closed-loop optimization
across perception and reasoning tasks. Learning–reason-
ing architectures are especially potent in tasks requiring
both ﬂexibility and formal reasoning—such as neuro-
symbolic program induction, abductive reasoning, and
interactive planning, and represent the frontier of efforts
to construct uniﬁed cognitive models that balance statis-
tical learning with symbolic abstraction. A compelling
example is DeepProbLog [ 29], which extends probabilis-
tic logic programming with neural predicates, allowing
both probabilistic reasoning and differentiable learning
in a tightly integrated architecture.
2.2 Robustness
Robustness in AI models refers to the ability of these models
to maintain stable and reliable performance even when sub-
jected to varied and unexpected conditions [ 30]. The concept
of robustness extends beyond mere accuracy on training data;
it encompasses the model’s ability to generalize effectively
and consistently across a wide range of real-world scenar-
ios. Robustness in AI is like designing a car for all terrains.
A robust car should work well not only on smooth roads
(clean data) but also on bumpy roads (noisy inputs), during
storms (distribution shifts), or when someone tries to mis-
lead the GPS (adversarial attacks). Similarly, a robust AI
system should maintain its reliability under all such driving
conditions. Ensuring robustness is paramount for the reli-
able operation of AI systems, particularly in complex and
123

Arabian Journal for Science and Engineering (2026) 51:35–67 41
Fig. 3 Y u’s Classiﬁcation of Neuro-symbolic AI
Fig. 4 V arious Categories of Robustness along with the Metrics of Measurement
uncertain environments where the data may be noisy, incom-
plete, or adversarial [ 31]. This involves not only the design
of algorithms that are inherently resilient, but also rigorous
testing and validation procedures to identify and mitigate
potential vulnerabilities. It is a critical aspect of trustworthy
AI, as it directly impacts the dependability and consistency of
AI-driven decisions [ 32]. A robust AI model should exhibit
predictable and stable behavior, reducing the risk of unex-
pected failures or biases that could undermine trust in the
system. This is important in high-stakes applications such as
healthcare, ﬁnance, and autonomous vehicles, where errors
or inconsistencies can have severe consequences.
Robustness in machine learning models can be viewed
along several orthogonal axes that capture how a model’s per-
formance reacts to different kinds of perturbations in the input
space [ 31]. Local robustness [ 33] asks whether inﬁnitesimal
perturbations around a single data point leave the predicted
label unchanged, whereas global robustness [ 34] extends this
guarantee to the whole input manifold, ensuring stability
over the entire in-distribution region. Adversarial robustness
[35] focuses on worst case, human orchestrated perturba-
tions crafted explicitly to induce misclassiﬁcation, while
non-adversarial robustness [ 36] evaluates resilience to ran-
dom noise sources such as Gaussian blur, sensor noise, or
missing pixels that are not chosen by an adversary. Semantic
robustness [ 37] considers higher-level, structure-preserving
changes, e.g., lighting, pose, or paraphrase, that keep the
underlying meaning intact, and pointwise robustness [ 38]
isolates the model’s sensitivity to discrete, isolated alter-
ations like single-pixel or character ﬂips. Probabilistic or
stochastic robustness [ 39] frames the problem in expec-
tation, asking whether the model’s risk remains bounded
under shifts drawn from a family of probability distri-
butions near the training distribution. Targeted robustness
[40] evaluates the model’s ability to avoid being steered
toward a speciﬁc, attacker-chosen target label, comple-
menting untargeted notions that only measure any form of
misclassiﬁcation. These dimensions provide a comprehen-
sive taxonomy for analyzing robustness of systems and are
shown in Figure 4 along with the various robustness evalua-
tion methods.
2.2.1 Robustness Methods
V arious robustness measures have been used, which guide
researchers in identifying the most effective approaches for
ensuring model reliability. These methods are indispensable
for certifying that AI models can perform safely and consis-
tently in real-world scenarios, and can be categorized under
different headings.
123

42 Arabian Journal for Science and Engineering (2026) 51:35–67
Accuracy Based
• Standard Accuracy
Standard accuracy is a fundamental performance metric
that computes the ratio of correct predictions to total pre-
dictions. It reﬂects how well a model generalizes to data
similar to its training set. While high standard accuracy
indicates effective learning of the training distribution,
it fails to capture performance under more challenging
conditions, such as distributional shifts or adversarial
perturbations. Goodfellow et al. [ 41] demonstrated that
neural networks with high accuracy on clean inputs can
still be extremely fragile, easily misclassifying inputs
when perturbed by imperceptible noise. This vulnerabil-
ity arises due to overreliance on non-robust or spurious
features that do not generalize well to real-world or adver-
sarial scenarios. Tsipras et al. [ 42] further argued that
there exists a fundamental trade-off between standard
accuracy and robustness, suggesting that conventional
accuracy metrics alone provide an incomplete assessment
of model reliability.
• Robust Accuracy
Robust accuracy offers a more realistic performance mea-
sure by evaluating a model under adversarial or corrupted
inputs. It quantiﬁes a model’s ability to maintain per-
formance in the presence of input perturbations, such
as those introduced by the Fast Gradient Sign Method
(FGSM) [43] or Projected Gradient Descent (PGD) [ 44].
[45] introduced PGD-based adversarial training, estab-
lishing robust accuracy as a core evaluation metric in
adversarial machine learning. [ 46] advocated for robust-
ness evaluation against real-world corruptions, proposing
datasets like ImageNet-C that systematically corrupt
inputs to simulate natural perturbations. The gap between
standard and robust accuracy highlights a model’s vul-
nerability to perturbations: Smaller gaps imply greater
resilience, whereas large drops signal brittle generaliza-
tion.
• Error Rate under Attack
The error rate under attack is a focused robustness met-
ric that captures a model’s susceptibility by measuring
the proportion of adversarially perturbed inputs that are
misclassiﬁed. [ 47] emphasized evaluating models with
strong adaptive attacks to uncover vulnerabilities that
remain hidden under weaker tests. Similarly, [ 48]s h o w e d
that many defense mechanisms fail under properly con-
structed attacks due to reliance on gradient obfuscation,
underscoring the importance of tracking error rates under
sophisticated adversarial manipulations. This metric not
only reﬂects robustness but also helps identify misleading
robustness claims.
Distance Based
• L0, L1, L2 Norms
The ℓ
0, ℓ1, and ℓ2 norms are fundamental metrics for
quantifying the nature and intensity of perturbations in
adversarial attacks. The ℓ
0 norm measures the number
of modiﬁed features (e.g., pixels), indicating the spar-
sity of an attack. Sparse attacks, those with a small ℓ0
norm alter only a few input features, making them harder
to detect and defend against, as they can bypass both
human perception and simple defensive strategies [ 47].
This norm is thus valuable for assessing the stealthiness
of an adversarial perturbation. The ℓ
1 norm evaluates the
total magnitude of changes by summing the absolute val-
ues of all perturbations, capturing how much the input
has been altered regardless of which speciﬁc features are
affected. In contrast, the ℓ
2 norm, or Euclidean distance,
calculates the overall similarity between the original and
perturbed inputs, reﬂecting the intensity of the pertur-
bation in a holistic sense. Attacks with lower ℓ
1 or ℓ2
norms are generally more imperceptible, making them
more dangerous in security sensitive applications [ 41,
45].
• Perceptual Distance
Perceptual metrics consider structural features such as
edges, textures, and spatial patterns as well as color
characteristics like hue, saturation, and brightness. This
allows for a more realistic and semantically aligned
assessment of how adversarial examples differ from
clean inputs. By incorporating perceptual distance into
adversarial attack generation, researchers can craft more
visually coherent and stealthy attacks that better sim-
ulate real-world scenarios, such as image compression
artifacts or sensor noise. Metrics such as Learned Percep-
tual Image Patch Similarity (LPIPS) have been developed
to quantify these perceptual differences more effectively
[49]. These metrics are instrumental not only in craft-
ing such imperceptible attacks, but also in evaluating the
robustness of deep learning models under realistic con-
ditions.
• Minimum Distance to Adversarial Example
The minimum distance to an adversarial example quanti-
ﬁes the smallest perturbation necessary to alter a model’s
prediction, serving as a direct and critical indicator of
robustness. This distance, measured using norms like ℓ
0,
ℓ1,o r ℓ2, captures how easily a model can be manip-
ulated by subtle input changes. A smaller minimum
distance implies higher sensitivity and a greater likeli-
hood that even minimal input perturbations could trigger
misclassiﬁcation [ 50]. Minimum distance serves both as
an attackability measure and as a benchmark for evalu-
ating defense mechanisms.
123

Arabian Journal for Science and Engineering (2026) 51:35–67 43
Statistical and Probabilistic Metrics
• Conﬁdence Score
The conﬁdence score represents a model’s self-assessed
certainty in its prediction, typically expressed as the prob-
ability assigned to the predicted class. Robust models are
expected to exhibit consistently high conﬁdence across
clean and mildly perturbed inputs, indicating resilience
to noise and an ability to focus on salient, stable features
in the data. A noticeable drop in conﬁdence, espe-
cially under adversarial or noisy conditions, can signal
underlying model vulnerabilities. [ 51] demonstrated that
adversarial examples often lie near decision boundaries,
where models produce low conﬁdence predictions. Sim-
ilarly, [ 52] showed that conﬁdence scores can serve as
useful signals for detecting out-of-distribution (OOD)
inputs and adversarial attacks.
• Prediction Variance
Prediction variance measures the stability of a model’s
output when subjected to minor perturbations in the input,
making it a key indicator of robustness, and reliabil-
ity. Low prediction variance reﬂects consistent model
behavior, suggesting that the model relies on meaningful,
invariant features rather than brittle patterns. Conversely,
high prediction variance signals that the model is overly
sensitive to slight input ﬂuctuations, potentially due to
overﬁtting, fragile decision boundaries, or inadequate
feature representation. [ 53] proposed the use of deep
ensembles to measure prediction variance as a robust
alternative to Bayesian approaches, demonstrating that
variance is an effective metric for uncertainty and adver-
sarial detection.
• Bayesian Methods
Bayesian methods in deep learning offer a principled
approach for modeling and quantifying uncertainty in
predictions by generating a full predictive distribution
rather than just a single point estimate. These meth-
ods capture the model’s belief over possible outputs,
reﬂecting epistemic uncertainty due to limited data or
model capacity. [ 54] showed that dropout at test time
can approximate Bayesian inference, enabling uncer-
tainty estimation without fully Bayesian models. This
facilitates computation of metrics such as predictive
entropy and variance from the distribution. Under adver-
sarial attacks or distributional shifts, increases in these
metrics, especially higher entropy, indicate the model’s
uncertainty and potential struggle to produce reliable pre-
dictions [ 55].
2.3 Uncertainty Quantification
In the context of ML, UQ refers to the process of provid-
ing a measure of how much conﬁdence a model has in its
predictions or generations [ 56]. Unlike traditional determin-
istic programs, ML models are data-driven systems, meaning
their outputs inherently possess a degree of uncertainty. This
uncertainty stems from multiple sources, including the inher-
ent randomness or noise in the data, the limitations imposed
by the choice of model architecture and parameters, and the
inductive assumptions made during the learning process [ 57].
Especially within deep learning, uncertainty arises not only
from the data itself but also signiﬁcantly from the training
procedure, which often involves stochastic optimization, ran-
dom initializations, and data shufﬂing, potentially injecting
noise and biases into the ﬁnal model [ 58]. Uncertainty in AI is
like a doctor diagnosing a patient. If the patient’s symptoms
are vague or the doctor has limited experience with simi-
lar cases, their conﬁdence in the diagnosis is low (epistemic
uncertainty). But if a symptom is inherently ambiguous, like
a mild fever that could be many things, the uncertainty lies
in the data itself (aleatoric uncertainty). AI models, like doc-
tors, must know when to be conﬁdent and when to admit
uncertainty.
The deﬁnition and scope of uncertainty in ML are evolv-
ing, with the advent of complex models like Large Language
Models (LLMs) and multimodal systems. These models
introduce unique challenges, such as uncertainty compound-
ing during autoregressive generation and dynamic shifts in
uncertainty based on context, demanding UQ approaches
tailored to their speciﬁc characteristics rather than relying
solely on methods developed for simpler discriminative mod-
els [ 56]. The focus is shifting from merely identifying if a
prediction is incorrect to understanding how likely it is to be
wrong and why, reﬂecting a move toward models possessing
a greater degree of self-awareness regarding their operational
limits.
A crucial step in understanding and managing uncertainty
in ML is recognizing that it arises from different sources and
manifests in different ways. The most common and widely
accepted taxonomy distinguishes between two fundamental
types of uncertainty: aleatoric and epistemic, as depicted in
Figure 5 along with the quantiﬁcation methods for each.
2.3.1 Aleatoric Uncertainty: The Irreducible Randomness in
Data
Aleatoric uncertainty refers to the inherent randomness,
stochasticity, or noise present within the data-generating pro-
cess itself. This type of uncertainty represents variability
that is intrinsic to the system being modeled and cannot be
reduced even with an inﬁnite amount of data or a perfect
model [ 4]. It is inherently a property of the data distribu-
tion rather than the model itself. It reﬂects the inherent noise
or variability in the observations due to limitations in mea-
surement or the stochastic nature of the underlying processes
[59].
123

44 Arabian Journal for Science and Engineering (2026) 51:35–67
Fig. 5 V arious Categories of
Uncertainty along with the
Quantiﬁcation Methods
Deep Generative Models
Deep Generative Models (DGMs) are probabilistic frame-
works that leverage deep neural networks to approximate the
underlying distribution of high-dimensional data p
data(x).
They operate by learning a probabilistic mapping from latent
variables z ∈ Rd , typically sampled from a standard Gaus-
sian prior N (0,I), to the data space Rn via a parameterized
generator gθ : Rd → Rn . Given a dataset {xi }m
i =1, DGMs
aim to capture the structure of the data distribution in fea-
ture space X ⊂ Rn . For supervised learning, Conditional
DGMs (cDGMs) [ 60] extend this formulation to model the
conditional distribution p(y | x), where y ∈ Y represents
structured outputs corresponding to inputs x ∈ X .
Deep Discriminative Models
Deep discriminative models leverage neural networks to
output predictive distributions directly. Given an input x,a
discriminative model estimates the conditional distribution
p(y | x) by learning a mapping through a neural network.
These models can be categorized based on the nature of the
predictive distribution:
• Parametric Models
These approaches assume a speciﬁc form for the output
distribution, such as Gaussian, Laplace, or Bernoulli. The
neural network is trained to estimate the parameters of
this distribution, for example, the mean μ(x) and vari-
ance σ
2(x) in the Gaussian case. The data uncertainty is
captured by the learned variance, which can vary across
different inputs:
p(y | x) = N (y | μ(x), σ2(x))
• Nonparametric Models
These models avoid assumptions about the speciﬁc distri-
butional form of the output. Instead, they rely on ﬂexible
techniques such as quantile regression or kernel-based
density estimation to capture the variability in the data.
These methods are particularly useful when the data
exhibit multimodality or heavy tailed characteristics that
parametric models fail to represent accurately.
2.3.2 Epistemic Uncertainty: The Reducible Lack of
Knowledge
Epistemic uncertainty represents the uncertainty stemming
from the model’s own limitations or lack of knowledge about
the underlying data-generating process. Essentially, it reﬂects
what the model doesn’t know due to ﬁnite data or imperfect
model speciﬁcation [ 4]. By acquiring more diverse and repre-
sentative data, reﬁning the model architecture, improving the
training process, or gaining better knowledge about the sys-
tem, this type of uncertainty can, in principle, be decreased.
It is often particularly high for inputs that are signiﬁcantly
different from the training data, as the model lacks the "expe-
rience" to make conﬁdent predictions for them [ 61].
Bayesian Neural Networks
Bayesian Neural Networks (BNNs) are a type of model
that, rather than learning ﬁxed parameters, learn probabil-
ity distributions over them. Given input–output data pairs
(X , Y ), the posterior over model parameters θ is expressed
as p(θ | X , Y ) using Bayes’ theorem:
p(θ | X , Y ) = p(Y | X ,θ) p(θ)
p(Y | X )
Here:
• θ: parameters of the neural network,
• X : input features in the training dataset,
• Y : target outputs corresponding to inputs X ,
• p(Y | X ,θ): likelihood of observing Y given X and
parameters θ,
• p(θ): prior distribution over the parameters,
123

Arabian Journal for Science and Engineering (2026) 51:35–67 45
• p(θ | X , Y ): posterior distribution over the parameters
given data,
• p(Y | X ): marginal likelihood or evidence.
Here, p(θ | X , Y ) captures the updated belief over model
parameters given observed data, which cannot be computed
in closed form. Predictions for new data points x∗ are
obtained by integrating over this posterior, capturing uncer-
tainty in the model’s weights.
p(y
∗ | x∗, X , Y ) =
∫
p(y∗ | x∗,θ) p(θ | X , Y )dθ
where
• x∗: new test input sample,
• y∗: predicted output corresponding to x∗,
• p(y∗ | x∗,θ): predictive likelihood for the new sample,
• p(y∗ | x∗, X , Y ): marginal predictive distribution,
reﬂecting both model and data uncertainty.
The predictive variance of this distribution quantiﬁes the
uncertainty associated with y∗. However, this posterior p(θ |
X , Y ) is generally intractable and requires approximation.
V ariational Inference [62] approximates the posterior by opti-
mizing over a parameterized family of distributions qφ(θ),
where φ denotes variational parameters (e.g., mean and vari-
ance). Alternatively, the Laplace Approximation [ 63]ﬁ t sa
Gaussian distribution centered at the maximum a posteri-
ori estimate. Sampling-based approaches like Markov Chain
Monte Carlo (MCMC) [ 64] can also be used for more accu-
rate posterior estimation.
Ensemble Models
Ensemble models quantify model uncertainty by com-
bining the outputs of multiple neural networks to form a
predictive distribution. The variability across the ensemble
members reﬂects epistemic uncertainty, which arises due to
limited data or model speciﬁcation.
One common strategy for constructing ensembles is boot-
strapping [65], where multiple training datasets are generated
by sampling with replacement from the original dataset.
Each neural network in the ensemble is trained on a differ-
ent bootstrapped dataset. During inference, predictions are
aggregated, and the variance across predictions (for regres-
sion) or the average entropy (for classiﬁcation) is used to
estimate uncertainty. Another approach introduces diversity
by varying the network architecture, including the num-
ber of layers, hidden units, and activation functions [ 66].
This method captures uncertainty stemming from model mis-
speciﬁcation. The hyper-ensemble approach [ 67] constructs
ensembles with varied hyperparameters such as learning
rates, optimization algorithms, and training procedures. This
strategy captures uncertainty due to training dynamics and
optimization variability.
Sample Distribution-Related Methods
Sample distribution-related uncertainty arises when test
samples are located in regions of low training data den-
sity. This form of uncertainty pertains to in-distribution data
that are sparsely represented in the feature space, leading
to unreliable model predictions. To address this, two main
methodological categories have emerged:
• Gaussian Process Hybrid Neural Networks
These models combine neural networks with Gaussian
processes (GPs) to estimate predictive uncertainty based
on sample density. The GP component, typically placed
on top of a neural feature extractor, provides a principled
measure of uncertainty that increases as the test point
moves further from the training data.
• Distance-Aware Neural Networks
These networks explicitly incorporate distance-based
metrics to modulate predictive conﬁdence. Predictions
are down weighted or ﬂagged as uncertain if the test
sample is located in a sparse region of the training distri-
bution.
2.4 Intervenability
The increasing complexity and pervasiveness of ML models,
particularly deep neural networks, have spurred signiﬁcant
research into understanding and controlling their behavior.
While interpretability aims to shed light on why a model
arrives at a particular decision, a related yet distinct goal
is intervenability: the capacity to actively modify or inter-
act with a model’s internal mechanisms or representations
to inﬂuence its outputs in a controlled and predictable man-
ner [ 68]. This capability moves beyond passive observation
toward active manipulation, offering a powerful means for
human–AI interaction and model reﬁnement. Intervenability
refers to the ability to make targeted changes to a model’s
internal state or reasoning process, such as adjusting its rep-
resentation of speciﬁc concepts or features, and observe the
resulting impact on its predictions [ 68]. It implies a level of
control that allows users not only to understand the model,
but also to act upon that understanding. Imagine using GPS
navigation. If the system suggests a wrong route, you might
override it by selecting an alternate path. Intervenability in AI
allows humans to do something similar, intervene in the AI’s
reasoning process, correct mistakes, or adjust rules without
retraining the entire model from scratch.
V arious studies have explored several distinct philosoph-
ical and technical approaches to imbue machine learning
models with intervenability. While not always rigidly catego-
rized in the literature, these approaches differ fundamentally
123

46 Arabian Journal for Science and Engineering (2026) 51:35–67
Fig. 6 V arious Approaches of
Intervention of AI Models
in where and how interventions are performed. V arious
grouping of the interventions that can be done are depicted
in Figure 6
2.4.1 Concept-Based Intervenability
This approach leverages intermediate representations aligned
with human understandable concepts as the primary interface
for interaction. Models are often explicitly designed with a
"concept bottleneck" layer, where the model’s reasoning is
channeled through these concepts [ 69]. Interventions involve
directly editing the predicted values or representations of
these concepts (e.g., changing "has stripes on belly" from
true to false in a bird classiﬁer). A wide array of methods,
including Concept Bottleneck Models (CBMs) [ 69] and their
variants, fall under this category.
2.4.2 Intervening on Black-Box Models
This approach aims to apply intervention techniques to mod-
els that were not originally designed with interpretability
or intervention in mind. It typically involves a preliminary
step of "probing" the model’s internal activations to iden-
tify neural correlates of desired concepts or features [ 5].
Subsequently, interventions are performed by editing these
identiﬁed activations during inference. This approach may
also involve ﬁne-tuning the black-box model speciﬁcally
to enhance its responsiveness to such interventions, thereby
making it more "intervenable."
2.4.3 Causal Intervention Approaches
Grounded in the principles of causal inference, this approach
seeks to understand and inﬂuence the true causal effects
between variables, often by mathematically removing the
inﬂuence of confounding factors [ 70]. Techniques such as
Pearl’s do-calculus or backdoor adjustment are employed
to estimate the outcome of an intervention, P(Y | do(X )),
rather than relying on potentially spurious correlations cap-
tured by the standard conditional probability P(Y | X ) [71].
The focus is on identifying and mitigating biases arising from
confounders to improve model robustness and the accuracy
of decision-making.
2.4.4 Model Editing
This category encompasses methods that directly manipu-
late the model’s parameters or internal representations to
alter its knowledge or behavior in a targeted manner [ 72].
Examples include identifying and intervening on speciﬁc
functional “circuits” within the network [ 73], or generating
precise counterfactual outputs following an intervention [ 72].
Figure 7 provides a summary of the concept of the three
pillars of AI that we have discussed so far.
3 Neuro-Symbolic AI For Robustness
The integration of symbolic reasoning within neural net-
work frameworks offers several theoretical advantages for
enhancing AI robustness. These advantages stem from the
ability to incorporate explicit knowledge, perform logical
inference, leverage abstract representations, and improve
interpretability. A practical integration of robustness in
neuro-symbolic models is illustrated by hybrid perception-
reasoning pipelines where neural networks serve as noisy
sensory encoders, and symbolic modules validate or correct
outputs through logic-based constraints. For instance, in a
neuro-symbolic visual reasoning task, a CNN may detect
objects and spatial relations in a scene, while a symbolic
reasoning module ensures that the derived interpretations
adhere to commonsense physical laws, e.g., “a cup cannot
ﬂoat above a table without support.” Such symbolic priors are
enforced via rule-based veriﬁers, which either reject incon-
sistent predictions or send feedback for neural adjustment.
Figure 8 presents a high-level neuro-symbolic robustness
pipeline in which a neural perception module ﬁrst converts
raw sensory inputs into probabilistic concept embeddings,
after which the representations are injected in a symbolic
knowledge store then into a logical reasoner / planner. The
reasoner composes those symbolic priors with the noisy
neural evidence to propose candidate decisions that are
123

Arabian Journal for Science and Engineering (2026) 51:35–67 47
Fig. 7 Three Pillars of Trustworthy AI
Fig. 8 Neuro-symbolic Robustness Pipeline
immediately scrutinized by a veriﬁer enforcing formal con-
straints. V eriﬁed outputs are released as system actions or
predictions, while any violation triggers a dashed feedback
loop that supplies explanatory traces back for explanation-
based ﬁne-tuning.
3.1 Injecting Knowledge and Constraints
Symbolic AI excels at representing knowledge explicitly
through logic, rules, constraints, or ontologies. Neuro-
symbolic systems can leverage this capability by integrating
such symbolic knowledge directly into the learning or infer-
ence process. This incorporation acts as a powerful prior,
guiding the system toward solutions that are consistent with
known facts about the world, thereby enhancing robustness
in several ways:
3.1.1 Guiding Learning
Symbolic constraints can regularize the neural network’s
learning process, preventing it from converging to solutions
that violate established domain knowledge or rely on spuri-
ous correlations present in the training data [ 74]. By encoding
expected structure or behavior, these constraints can promote
learning more generalizable representations, improving per-
formance on OOD data where spurious correlations may no
longer hold.
3.1.2 Enforcing Consistency
Predeﬁned rules can be used to ensure that the system’s out-
puts are logically coherent and consistent with the known
constraints of the domain [ 75]. This can directly mitigate
failures caused by adversarial attacks or OOD inputs that
might otherwise lead to nonsensical or unsafe predictions.
3.1.3 Improving Data Efﬁciency
Explicit knowledge can compensate for limited training data
by providing information that would otherwise need to be
learned implicitly from many examples [ 76]. This can lead to
more robust models, particularly in data scarce environments,
as the model is less likely to overﬁt the limited available data.
3.2 Logical Reasoning for Verification and
Correction
Neuro-symbolic architectures often incorporate a symbolic
reasoning engine that can process the outputs or intermediate
representations generated by neural components. This allows
the system to perform logical inference, which contributes to
robustness:
3.2.1 Output Veriﬁcation and Correction
The symbolic reasoner can check whether the predictions
made by the neural network are consistent with the sym-
123

48 Arabian Journal for Science and Engineering (2026) 51:35–67
bolic knowledge base or satisfy speciﬁc logical constraints.
If inconsistencies are detected, the system can ﬂag the out-
put as potentially unreliable, or in some cases, use the logical
rules to correct the prediction or guide further reasoning [ 77].
3.2.2 Reasoning Under Uncertainty
Frameworks like probabilistic logic programming allow the
symbolic reasoner to handle uncertain inputs, such as prob-
ability distributions over concepts provided by the neural
perception module. By explicitly propagating and reasoning
about uncertainty according to logical rules, these systems
can potentially arrive at more robust conclusions than meth-
ods that rely solely on uncertain neural outputs or make
premature deterministic decisions [ 29].
3.2.3 Structured Planning and Decision Making
For tasks requiring multistep reasoning or planning, symbolic
components can impose logical structure on the decision-
making process. Based on perceptions from the neural part,
the symbolic reasoner can deduce consequences, evaluate
plans according to goals and constraints, and guide action
selection, leading to more robust and coherent behavior in
complex, dynamic environments compared to end-to-end
reactive policies [ 78].
3.3 Symbolic Abstractions for Generalization
A key capability of many neuro-symbolic systems is the
mapping of low-level, sub-symbolic inputs to higher-level,
abstract symbolic representations. Reasoning at this sym-
bolic level offers advantages for robustness, particularly
OOD generalization:
3.3.1 Systematic Generalization
Systematic generalization refers to a model’s ability to
consistently and predictably extend learned knowledge to
novel combinations of familiar elements, capturing under-
lying structural rules rather than memorizing surface-level
patterns. Traditional deep neural networks often general-
ize by interpolation between training examples. However,
they typically struggle when faced with novel combinations
or conﬁgurations of inputs they have never seen together
before [ 79]. Symbolic representations capture the underly-
ing structure and concepts of a domain, allowing the system
to generalize based on combinatorial rules rather than just
surface-level statistical patterns.
3.3.2 Compositionality
Compositionality in context of machine learning represents
that learned representation should be modular, interpretable
and combinable. By operating on discrete concepts or
composing functions represented by neural modules based
on symbolic structure, neuro-symbolic systems can poten-
tially handle novel compositions of learned elements more
effectively than monolithic neural networks. The GQA
dataset [ 80] emphasizes the importance of compositionality
by explicitly structuring questions and reasoning processes
using functional programs, thereby encouraging models to
perform multistep, compositional reasoning rather than rely-
ing solely on surface-level statistical patterns.
3.3.3 Reduced Sensitivity to Input Variations
Reasoning over stable symbolic representations can sig-
niﬁcantly enhance a system’s robustness to minor input
perturbations, such as noise or adversarial distortions. By
grounding the reasoning process in abstract, high-level con-
cepts rather than surface-level pixel patterns, models can
maintain consistent semantic understanding even when low-
level variations occur. As demonstrated in CLEVRER [ 81],
leveraging symbolic abstractions of dynamic visual scenes
allows the system to preserve core conceptual meaning
despite input ﬂuctuations, thereby stabilizing reasoning out-
comes under varying conditions.
3.4 Interpretability as a Tool for Robustness
Symbolic components, such as knowledge bases and logical
inference steps, are often inherently interpretable or explain-
able. This transparency provides a signiﬁcant advantage for
understanding and improving robustness:
3.4.1 Debugging Failures
When a neuro-symbolic system fails, such as making an
incorrect prediction on an OOD sample or succumbing to
an adversarial attack, the symbolic component can often
provide valuable diagnostic insights into the cause of the
failure [ 82]. For instance, failures can be traced to incorrect
concept extraction by the neural module, violations of spe-
ciﬁc logical rules, or ﬂaws in the symbolic reasoning process
itself. This diagnostic transparency stands in stark contrast
to the challenges of debugging traditional black-box neural
models, where such granular failure analysis is often infea-
sible.
123

Arabian Journal for Science and Engineering (2026) 51:35–67 49
3.4.2 Building Trust
Understanding why a model makes a particular decision,
especially under challenging conditions, is crucial for build-
ing trust in AI systems. Neuro-symbolic AI systems, which
integrate neural networks with symbolic reasoning, offer
enhanced explainability by providing human-interpretable
insights into their decision-making processes. Consistency,
Reliability, user-level Explainability, and Safety (CREST)
framework emphasized Consistency, Reliability, user-level
Explainability, and Safety as foundational pillars for trust-
worthy neuro-symbolic systems. The work demonstrates
how combining statistical and symbolic AI methods can lead
to more transparent and reliable AI applications [ 83].
3.4.3 Targeted Improvement
Identifying the speciﬁc source of a robustness failure in
a neuro-symbolic system enables targeted interventions to
enhance system performance. If the issue lies within the per-
ception module, retraining or ﬁne-tuning the neural network
can address the problem. For instance, explanation-based
ﬁne-tuning has been shown to improve model robustness
against spurious correlations by encouraging models to focus
on human relevant features during training [ 84]. When fail-
ures stem from the symbolic reasoning component, reﬁning
the knowledge base or adjusting logical rules can be effec-
tive. The study [ 85] introduced the "Recover" framework,
which integrates ontologies and logical rules to detect and
recover from failures in robotic task execution, demonstrat-
ing how symbolic reasoning can identify and rectify errors
in real time. A robust rule learning approach that prunes and
reﬁnes logical rules to ensure reliability and interpretability,
facilitating better decision-making in complex systems [ 86].
4 Neuro-symbolic AI for Uncertainty
Quantiﬁcation
UQ is crucial in many domains, from a robot sensing a
noisy environment, to a medical AI diagnosing a patient with
incomplete information, to an autonomous drone navigating
with partial observability [ 87]. Neuro-symbolic techniques
address these challenges by assigning conﬁdence measures
to symbolic inferences, enforcing logical constraints on prob-
abilistic predictions, and integrating expert knowledge to
guide learning in ambiguous situations. UQ is practically
embedded in neuro-symbolic models through probabilis-
tic symbolic reasoning, Bayesian neural modules, or fuzzy
logic systems. A common architecture involves neural mod-
ules outputting soft probabilistic estimates, which are then
input into a symbolic reasoning layer that incorporates con-
ﬁdence thresholds and probabilistic logic rules to reﬁne ﬁnal
decisions. For example, in medical diagnostics, uncertainty-
aware neuro-symbolic models can withhold high-risk deci-
sions if the conﬁdence is below a symbolic safety threshold,
triggering a human-in-the-loop intervention.
Figure 9 illustrates how uncertainty is handled in a typi-
cal neuro-symbolic pipeline. The Neural Module processes
raw inputs and generates probabilistic outputs (e.g., soft class
labels or conﬁdence scores). These are passed to a Probabilis-
tic Logic layer, where logical rules are assigned probabilistic
weights and soft constraints to account for data noise or
ambiguity. The Symbolic Reasoner then performs rule-based
inference using these uncertain predicates. The ﬁnal decision
is validated with respect to conﬁdence thresholds. If uncer-
tainty exceeds predeﬁned bounds, the system can trigger a
feedback loop, either reﬁning neural predictions or deferring
to human oversight, thus enhancing the trustworthiness and
safety of decisions in high-stakes domains like medicine or
autonomous systems.
In the following sections, we overview the theoretical
frameworks that underpin neuro-symbolic UQ.
4.1 Probabilistic Logic Frameworks
One foundational approach to uncertainty in symbolic rea-
soning is to attach probabilities to logical statements. Prob-
abilistic logic frameworks like Markov Logic Networks
(MLNs) [ 88] and Probabilistic Soft Logic (PSL) [ 89] allow
truth values of logical formulas to be uncertain. MLNs, for
example, treat each logical rule as a weighted constraint and
deﬁne a probability distribution over all possible worlds,
so that violating important rules is unlikely. Probabilistic
Soft Logic uses continuous truth values in [0,1] (a “soft”
logic), solving an optimization to ﬁnd the most probable
truth assignment given weighted rules. These frameworks
were early efforts in statistical relational learning, combin-
ing relational logic with probabilistic graphical models to
quantify uncertainty in complex knowledge bases.
Modern neuro-symbolic systems build on these ideas
by incorporating neural networks as sources of probabilis-
tic facts or rules. For instance, DeepProbLog [ 29] extends
the probabilistic logic programming language ProbLog by
allowing certain predicates to be computed by neural nets. In
DeepProbLog, a neural network can output a probability dis-
tribution over predicate values, and the logic program uses
these as probabilistic facts to reason about high-level out-
comes. This yields an end-to-end differentiable model that
handles uncertainty in perception while preserving logical
structure. Another example is Neural Probabilistic Soft Logic
(NeuPSL) [ 90], which combines PSL’s probabilistic rules
with neural perception. NeuPSL uses deep neural submod-
els to provide truth values for predicates, uniting low-level
perception with high-level probabilistic reasoning. By unit-
ing symbolic rules with neural outputs, such systems can
123

50 Arabian Journal for Science and Engineering (2026) 51:35–67
Fig. 9 Neuro-symbolic Uncertainty Quantiﬁcation Pipeline
perform joint inference: e.g., an uncertain visual detection
(neural probability) can be validated or adjusted by logi-
cal constraints (symbolic rules) with associated conﬁdences.
Empirical studies show that neuro-symbolic probabilistic
models can improve both accuracy and calibrated uncer-
tainty. For example, Manhaeve et al. [ 29] demonstrate that
DeepProbLog achieves better uncertainty estimation than
pure neural networks on tasks requiring logical consistency.
4.2 Fuzzy Logic and Neuro-Fuzzy Systems
Fuzzy logic offers another mechanism for uncertainty han-
dling, by allowing truth values to be degrees of belief between
0 and 1 rather than strict true/false. In fuzzy logic, one deﬁnes
membership functions that map a real input to a truth degree
in a fuzzy set. Fuzzy logic is well suited for imprecise con-
cepts (“slightly,” “moderately,” “very”) and has a long history
in expert systems and control; for example, fuzzy rule-based
systems have been used in medical diagnosis to handle symp-
tomatic uncertainty [ 91].
Neuro-symbolic AI leverages fuzzy logic by making log-
ical components differentiable. Neuro-fuzzy systems embed
fuzzy rule bases into neural network architectures. Today’s
Logic Tensor Networks (LTN) [ 92] and Logical Neural Net-
works (LNN) [ 93] continue this trend: They implement
ﬁrst-order logic using real-valued truth tensors and learn-
able fuzzy operators. For example, LTN uses continuously
valued logic (with fuzzy semantics) to allow training a neural
network that must satisfy given logical axioms. If we have a
rule like ∀x : Cat(x ) ⇒ Mammal(x ), an LTN can enforce
that the truth degree of Cat (x ) is always less than or equal to
that of Mammal (x ), while these truth values are predicted by
a neural model; thus, the model learns in a way that respects
the fuzzy rule. Such frameworks can perform query answer-
ing under uncertainty, as they can return a truth degree for
any logical query against a knowledge base. IBM’s LNN
similarly provides a neural architecture that exactly corre-
sponds to a set of logical formulas with learnable degrees,
ensuring “no information is lost between neural and logical
representations.”
4.3 Bayesian Neuro-symbolic Integration
Bayesian methods provide a principled framework for quan-
tifying uncertainty, especially epistemic uncertainty. In a
Bayesian approach, one represents uncertainty in terms of
probability distributions and updates those distributions with
evidence. Neuro-symbolic AI can merge Bayesian inference
with symbolic structure in several ways:
4.3.1 Bayesian Networks with Neural Components
A Bayesian Network is a directed graphical model encoding
probabilistic dependencies. One can inject neural networks
as estimators for certain conditional probabilities or as recog-
nition models, while keeping a symbolic graphical structure.
Fenske et al. [ 94] employed a neuro-symbolic framework
for medical diagnosis by integrating neural networks with
a Bayesian network structured over diseases and symp-
toms. Neural models interpret raw inputs (e.g., images or
physiological signals) to produce probabilistic symptom like-
lihoods, which are then propagated through the Bayesian
network to infer posterior probabilities of potential diag-
noses.
4.3.2 Bayesian Program Learning and Symbolic
Probabilistic Programs
Bayesian program learning (BPL) approach [ 95] repre-
sented characters as symbolic generative programs and used
Bayesian inference to learn new concepts from one example.
More recent work integrates neural networks with proba-
bilistic programming languages (PPLs) like Pyro [ 96]o r
Stan [97], allowing symbolic probabilistic models to include
neural subroutines. These PPL-based approaches can out-
put full probability distributions over answers and provide
uncertainty intervals, beneﬁting from Bayesian calibration.
123

Arabian Journal for Science and Engineering (2026) 51:35–67 51
4.3.3 Bayesian Symbolic Reasoning in Physics and
Commonsense
In the research work [ 98], the environment is described by
symbolic physics rules, but the system maintains uncer-
tainty over physical properties and laws. It models each
entity as a random variable and uses Bayesian inference to
update beliefs about latent properties from. Simultaneously,
it employs symbolic regression to discover the form of force
laws. The result is a system that can learn physical reasoning
from very few examples, outputting not just a prediction but
a posterior distribution over possible explanations.
4.3.4 Bayesian Neural Networks (BNNs)
These are neural networks that treat weights or activations as
random variables with distributions, often learned via varia-
tional inference or MCMC [ 99]. While not symbolic in the
knowledge representation sense, BNNs are a hybrid approach
that bring probabilistic reasoning into neural models [ 100].
By leveraging distributions over parameters, “Bayesian neu-
ral networks not only provide accurate predictions but also
quantify uncertainty in those predictions.” A BNN ﬂight con-
troller can output both a control action and a measure of
conﬁdence, enabling the system to know when it’s unsure
and defer to a safe policy [ 101].
4.4 Knowledge-Guided Neural Networks
Another thread of neuro-symbolic research injects logical
knowledge into the training and architecture of deep learning
models to guide them under uncertainty. The idea is to use
logic as a form of inductive bias or constraint on a neural
network, so that the network learns in a way that respects
certain rules or can reason about its outputs. Several notable
frameworks and techniques exemplify this:
4.4.1 Differentiable ILP and Neural Theorem Provers
Evans & Grefenstette [102] introduced a differentiable induc-
tive logic programming system that learns logic rules with
neural guidance. Similarly, Neural Theorem Provers [ 103]
use embeddings and attention to learn logical inference in
knowledge bases. These systems quantify uncertainty via the
score or attention weights for each possible proof, essentially
learning a soft truth value for conclusions that is derived from
data.
4.4.2 Neural Answer Set Programming
Neural Answer Set Programming framework (NeurASP)
[104] combines answer set programming (ASP), a form of
logical reasoning, with neural predicates. In NeurASP , an
ASP program can call a neural network to provide a proba-
bility distribution over some facts, and the ASP solver ﬁnds
stable models consistent with high-probability facts. The
result is that one can impose discrete logical constraints on
the outputs of neural networks and get a sense of conﬁdence
in the solutions. NeurASP has been applied to visual question
answering, where the neural part interprets an image and the
symbolic part ensures the answer satisﬁes logical constraints,
with the system able to express uncertainty in its ﬁnal answer
if multiple stable models exist [ 105].
4.4.3 Semantic Loss and Constraint-based Learning
A technique called semantic loss [ 106] adds a penalty to a
neural network’s training objective if its outputs violate given
logical formulas. By minimizing this loss, the network learns
to satisfy the logical constraints whenever possible. This
effectively converts logical uncertainty into a gradient that
shapes the network’s parameters. Such approaches ensure
consistency under uncertainty by never allowing the model
to become conﬁdently inconsistent: Instead, the uncertainty
is redirected.
4.4.4 Knowledge Graph and Ontology Integration
Neural networks can also be integrated with symbolic knowl-
edge graphs that contain uncertain facts (like weighted edges
or conﬁdence scores) [ 107]. For instance, in neuro-symbolic
question answering, a neural model might retrieve candidate
answers from text and a symbolic ontology could validate
these answers against known relationships, assigning con-
ﬁdence scores. The neuro-symbolic concept learner [ 20]
for visual scenes is an example where a network proposes
object relations and a logic module reﬁnes them. These sys-
tems quantify uncertainty by propagating neural prediction
uncertainties through logic rules, often using fuzzy logic or
probabilistic logic in the background to do so.
Table 3 distills how the four main families of neuro-
symbolic techniques distribute their strengths across the UQ
landscape. Probabilistic logic models natively represent both
aleatoric and epistemic uncertainty by weighting rules, but
they do so via “soft” constraints that trade strict logical
soundness for tractability and thus scale only moderately.
Neuro-fuzzy systems deliver high interpretability and excel-
lent runtime scalability, yet they primarily capture aleatoric
noise; because rule weights are ﬁxed or learned determin-
istically, gaps in domain knowledge (epistemic uncertainty)
remain unexpressed. Bayesian integration offer principled
posterior estimates for both uncertainty types, but exact infer-
ence or variational surrogates can be computationally heavy,
so performance degrades on very large knowledge graphs.
Finally, constraint-guided neural networks enforce “hard”
logic guarantees even when neural modules supply uncertain
123

52 Arabian Journal for Science and Engineering (2026) 51:35–67
Table 3 Cross-cutting comparison: uncertainty types, guarantees, and scalability across neuro-symbolic families
Framework Aleatoric UQ Epistemic UQ Interpretability Logic guarantee Scalability
Probabilistic Logic ✓✓ Medium Soft Medium
Neuro-Fuzzy ✓ – high soft high
Bayesian neuro-symbolic ✓✓ Medium Depends Low–mid
Knowledge guided NNs – ✓ Medium–high Hard High
evidence. They excel at representing epistemic uncertainty
through multiple stable models or residual losses, yet require
auxiliary mechanisms to tackle observation noise.
5 Neuro-symbolic AI for Intervenability
Beyond passive transparency, a major advantage of neuro-
symbolic AI is intervenability, the capacity for humans to
actively steer or correct the model’s behavior by interact-
ing with its interpretable components. In conventional deep
learning, if an explanation reveals a problematic behavior,
the only recourse is often to retrain or ﬁne-tune the model on
new data, an indirect and time-consuming process. Neuro-
symbolic systems, by contrast, are built in a way that users
can directly modify aspects of the model’s knowledge or rea-
soning without a full retraining. The key is that because part
of the model’s state is symbolic, a human expert can inject
corrections or new information at that level. Xin Zhang and
Victor Sheng [ 108] note that introducing readable, symbolic
components creates systems that “allow humans to interact
and intervene in the learning system,” aligning the AI’s rea-
soning more closely with human understanding and values. In
effect, the symbolic interface serves as a medium for human-
in-the-loop governance of the AI [ 109].
Figure 10 schematically integrates perception, reason-
ing, and governance within a neuro-symbolic decision stack.
Solid green arrows trace the forward inference path: Raw
sensory input is ﬁrst encoded by the Neural Perception mod-
ule; its activations instantiate interpretable Concepts, which
in turn feed a Rules layer that enforces domain-speciﬁc logic
before emitting the system’s downstream decision. Dashed
blue arrows denote human control channels. A domain expert
can override or relabel individual concepts, redirect the rule
evaluation, and critique the model’s Explanation Interface
like saliency maps, concept heat maps, or rule traces whose
feedback propagates back to reﬁne both rule weights and
concept classiﬁers.
5.1 Concept-Level Interventions
In concept-based models, a user can correct the model’s
interpretation of intermediate concepts. Test time concept
intervention was demonstrated to signiﬁcantly improve out-
comes in concept bottleneck models [ 110]. Since the model’s
decision is explicitly based on these concept variables, such
an override cleanly changes the outcome. Recent research
on Concept Embedding Models (CEMs) [ 111] and Concept-
based Memory Reasoner (CMR) [ 110] speciﬁcally mea-
sures how effective concept interventions are, conﬁrming
that adjusting concept predictions can rectify mistakes and
improve the model’s alignment with ground truth in real time.
5.2 Rule and Constraint Injection
When an AI’s behavior needs to be adjusted or bounded,
neuro-symbolic systems allow experts to add or modify sym-
bolic rules that the model must obey. Greco et al. [ 112]
illustrate this in a credit lending scenario: After identifying
a gender bias via explainability tools, they added ﬁrst-order
logic rules to an image classiﬁcation network to enforce gen-
der fairness, signiﬁcantly reducing bias while maintaining
the original accuracy. In general, embedding domain con-
straints via differentiable logic lets practitioners steer the
learning process toward desired behaviors. Another example
is adding policy guardrails for large language models: recent
systems like Amazon Bedrock’s LLM Guardrails
1 use for-
mal rules to check and adjust an LLM’s output, essentially
acting as a symbolic intervention layer on a neural gener-
ative model. Such guardrails perform automated reasoning
over the model’s output and can override or reject responses
that violate given constraints, introducing a human imposed
safety policy directly into the AI’s inference loop.
5.3 Interactive Training and Debugging
Neuro-symbolic AI also supports iterative human-in-the-
loop reﬁnement. Researchers have proposed explanatory
interactive learning methods where users not only receive
explanations but also provide feedback on them to update
the model. Teso et al. [ 113] demonstrate that if an expla-
nation shows a model is using a wrong feature, a user can
correct it by labeling that feature as irrelevant, and the model
will adjust its internal parameters accordingly. In a neuro-
symbolic context, Stammer et al. [ 114] introduced a “Right
1 https://aws.amazon.com/bedrock/guardrails/
123

Arabian Journal for Science and Engineering (2026) 51:35–67 53
Fig. 10 Human Intervention
Pathways in a neuro-symbolic
Pipeline
for the Right Concept” approach, allowing users to revise
a model’s concept attributions if the model gets the right
answer for the wrong reason, the user can intervene by adjust-
ing the concept-level explanation, and the model is retrained
to ﬁx that ﬂaw. Similarly, Bontempelli et al. [ 115] enable
concept-level debugging of a prototype-based image network
by having users correct which prototypes should be relevant
for a given concept. All these approaches treat the explana-
tion interface as a two-way channel: Not only does the model
explain itself, but humans can talk back through that interface
to improve the model.
6 Converging Logic, Probability, and
Learning
A core theme in neuro-symbolic AI research is how to
seamlessly integrate formal logic, probabilistic reasoning,
and deep learning into uniﬁed architectures. Each of these
paradigms offers distinct strengths: Formal logic provides
precision and the possibility of proofs, probabilistic models
handle uncertainty and noise, and neural networks excel at
learning from raw data. The future of neuro-symbolic sys-
tems likely involves hybrid architectures that draw on all
three, and doing so raises both opportunities and open ques-
tions:
6.1 Differentiable Reasoning Modules
One active research direction is making symbolic reasoning
differentiable and thus compatible with neural network train-
ing. Pioneering frameworks like DeepProbLog [ 29], Neural
Theorem Provers [ 103], Logic Tensor Networks [ 92], and
more recently Scallop [ 116] allow logical inference to be
embedded in end-to-end learning. Scallop integrates with
PyTorch to let a neural network feed probabilistic facts
into a logic program and receive gradients from the logical
reasoning outcomes. This enables training the neural compo-
nents with feedback from logical constraints. A differentiable
reasoning module can ensure that the neural net’s outputs
tend toward satisfying logical rules, improving correctness
and compositional generalization. Recent results have shown
that in scenarios with well-deﬁned logic operations, neuro-
symbolic models can outperform purely neural models by a
large margin [ 117].
Future architectures will likely include adaptive reasoning
depth using shallow reasoning for efﬁciency when possible,
and deeper reasoning only when needed, as it was observed
that increasing inference depth did not always improve assur-
ance metrics in one study [ 26]. Balancing differentiable
ﬁdelity (how well the logic module approximates true logical
inference) with scalability is an open problem; exact sym-
bolic reasoning is combinatorial, so researchers continue to
develop relaxations that are tractable yet maintain logical
rigor [ 118].
6.2 Unified versus Modular Design
A foundational design debate in neuro-symbolic AI con-
cerns the architectural integration of neural and symbolic
components, speciﬁcally, whether to pursue a uniﬁed repre-
sentation or a modular composition. Uniﬁed approaches aim
to embed both neural and symbolic representations within a
shared framework, often referred to as a universal represen-
tation [ 119]. In such frameworks, symbols are encoded as
continuous vectors, enabling symbolic manipulation within
the differentiable space of neural models. Conversely, neural
latent spaces can be structured to admit symbolic interpre-
tation. Advances in knowledge graph embeddings [ 120] and
graph neural networks (GNNs) [ 121] exemplify this trajec-
tory by geometrizing logical relations and fostering end-to-
end trainability via gradient-based optimization. In contrast,
modular architectures retain clear separability between neu-
ral and symbolic subsystems. These systems operate through
deﬁned interfaces. Neural modules output probabilistic facts
or distributions, which are then consumed by symbolic
solvers for logical inference or planning. Empirical stud-
ies on system robustness suggest that this decoupled design
offers resilience to perturbations and improved fault isola-
tion [ 122]. Moreover, modularity supports heterogeneous
specialization, allowing each subcomponent to leverage
domain-speciﬁc advances. However, this separation poses
challenges for training, particularly when inconsistencies
123

54 Arabian Journal for Science and Engineering (2026) 51:35–67
emerge; it remains non-trivial to propagate corrective sig-
nals back to the neural module [ 123].
Emerging approaches seek to blend these paradigms
via dynamic pipelines or curricula. In these hybrids, neu-
ral components perform perceptual abstraction or concept
extraction, which are subsequently reasoned upon sym-
bolically [ 20]. This design allows attribution of errors to
speciﬁc modules, either perceptual inaccuracies or logical
missteps, facilitating targeted debugging and reﬁnement.
Such systems may even transition adaptively between neural
and symbolic processing based on epistemic conﬁdence or
task structure [ 124]. Key research frontiers include devel-
oping mechanisms for differentiable interfaces, designing
curriculum-based switching mechanisms, and ensuring sta-
bility and coherence in gradient or feedback propagation
across the hybrid pipeline.
6.3 Scalable Reasoning Over Knowledge Graphs
Large-scale knowledge graphs (KGs) use symbolic repre-
sentations and often incorporate logical rules or constraints
[125]. Traditional KG reasoning either relied on symbolic
rule-based inference or purely neural embedding-based infer-
ence. New research is combining these: For instance, Chen
et al. [ 126] introduced a differentiable neuro-symbolic rea-
soning approach for large KGs. The system can leverage
logical rules for precise multi-hop reasoning while using
neural embeddings to generalize and handle the KG’s scale.
Integrating formal logic with learnable embeddings allows
the model to ﬁll in gaps in the knowledge graph with a
degree of certainty, effectively doing probabilistic knowledge
completion with logical constraints [ 127]. This work [ 128]
exempliﬁes how formal logic and probabilistic ML together
can tackle problems neither could alone: Logic contributes
structure and the ability to extrapolate systematically, while
learning brings the ability to handle noise, unseen entities, or
incomplete data.
As knowledge graphs power applications from search
engines to drug discovery, making their query answering both
robust and uncertainty-aware is vital [ 125]. A future direction
is neuro-symbolic knowledge base veriﬁcation using the neu-
ral side to propose new links or facts and the symbolic side
to enforce consistency with known facts or ontologies, with
uncertainty measures indicating how plausible each new link
is. Formal logic can also be used to encode safety or ethical
constraints in generative models [ 129].
6.4 Neuro-Symbolic Programming with Uncertainty
Probabilistic programming languages (PPLs) like Pyro [ 96],
Stan [ 130], or ProbLog [ 131]allow a modeler to write
down probabilistic generative models with symbolic struc-
ture [132]. We see a trend toward integrating neural networks
as components within probabilistic programs [ 133]. In neuro-
symbolic programming, a user can write a high-level program
that calls neural networks as subroutines for tasks like percep-
tion. The program can then be used for tasks like probabilistic
inference or planning. This approach offers interpretable glue
around learned components. One example use case is a robot
that uses a probabilistic program to model uncertainty in its
world and uses neural networks to analyze sensor data; the
overall system can perform Bayesian updating and planning
in a way that is understandable and veriﬁable at the program
level [134]. The integration of PPLs with deep learning is an
emerging research direction [ 96]; challenges include making
inference efﬁcient when neural likelihoods are involved and
allowing gradients to ﬂow through discrete sampling opera-
tions.
The DoD’s interest in neuro-symbolic AI for decision-
making in security operations reﬂects this: They outline use-
cases where symbolic knowledge is used to contextualize and
explain alerts, learn from few incidents, and handle noisy data
to maintain accuracy in real-world conditions [ 10]. By using
a programmatic structure, they foresee AI that can be audited
and directed more like a traditional software system, yet with
the adaptive learning capabilities of modern AI.
Table 4 presents a comparative summary of prominent
frameworks, contrasting their core logic, learning paradigm,
probabilistic treatment, architectural style, and computa-
tional trade-offs.
Table5 presents a comparative summary of representative
neuro-symbolic frameworks evaluated on standard bench-
marks. This performance overview helps contextualize their
accuracy and inference latency trade-offs across visual rea-
soning, knowledge base querying, and logic consistency
tasks.
7 Real-World Applications of
Neuro-symbolic AI
7.1 Robotics
The integration of neuro-symbolic AI in robotics has emerged
as a transformative paradigm, effectively bridging subsym-
bolic perception with high-level symbolic reasoning to tackle
complex, real-world tasks. Coraggio et al. [ 140]i n t r o -
duced landmark-based self-localization systems leveraging
minimal sensors, while Staffa et al. [ 141] showcased adapt-
able behavior modulation in dynamic environments through
threshold tuning in neuro-symbolic networks. These inno-
vations, alongside Kraetzschmar et al.’s [ 142]w o r ko n
environmental modeling for mobile robots, illustrate how
neuro-symbolic methods enhance spatial awareness, auton-
omy, and decision-making efﬁciency. Furthermore, hybrid
approaches like the integration of virtual neural sensors with
123

Arabian Journal for Science and Engineering (2026) 51:35–67 55
Table 4 Critical comparison of representative neuro-symbolic AI frameworks
Framework Logic Backbone Learning Integration Architectural Insights
DeepProbLog Prolog-based rules Neural predicates in
differentiable programs
Strong expressiveness; but training is slow, and scalability is
limited due to grounding explosion and gradient complexity
NeurASP Answer Set Programming (ASP) Neural outputs as symbolic
facts
Highly interpretable; suitable for constraint-rich tasks but rigid
for dynamic environments. Limited support for incremental
learning
Scallop Differentiable Datalog PyTorch-integrated
symbolic reasoning
Efﬁcient and scalable; favors logic-aware ML tasks, but
constrained in expressiveness compared to full FOL systems
Logic Tensor Networks (LTN) Fuzzy ﬁrst-order logic Rule-constrained learning
via fuzzy logic
Offers soft logic reasoning and interpretability; not ideal for
large-scale or multimodal systems
NeuPSL Probabilistic Soft Logic Neural scoring of truth
degrees
Modular, fast, and effective for relational inference, but lacks
support for multi-hop or compositional logic
BNNs (Bayesian Neural Networks) None (purely subsymbolic) Learning via stochastic
parameter distributions
Excellent for uncertainty quantiﬁcation; no interpretability or
logical structure–suitable only when symbolic control is not
required
Probabilistic Programming (e.g., Pyro + NN) Symbolic generative models Neural modules as
likelihood functions or
guides
Highly expressive; enables full Bayesian reasoning. However,
computational cost and inference complexity remain major
barriers
123

56 Arabian Journal for Science and Engineering (2026) 51:35–67
Table 5 Performance evaluation of recent neuro-symbolic systems
Framework Task & Benchmark Metric Result Prev. SOTA
DeepProbLog [ 29] Sorting T4 (train 4 → test 64) Acc. (%) 100.0 20.65 [ 135]
Word-Algebra Problems (W AP) T5 Acc. (%) 96.5 96.0 [ 135]
NeurASP [ 104] Sudoku (OpenSky) Whole-board Acc. (%) 66.5 29.1 [ 136]
Shortest-Path 4 × 4 grid V alid-path (%) 96.6 28.3 [ 137]
Scallop [ 116] sum4 – add four MNIST digits Acc. (%) 95.47 (timeout [ 29])
sort4 – sort 4-digit list Acc. (%) 92.02 89.96 [ 29]
NeuPSL [ 90] MNIST-Addition 2 ( n = 80) Acc. (%) ∼25 ∼17 [ 29]
Visual Sudoku 4 × 4 Acc. (%) ∼81 ∼75 [ 138]
NS-VQA [ 117] CLEVR-Humans Acc. (%) 67.0 66.6 [ 139]
CLEVR-CoGenT Acc. (%) 99.8 96.6 [ 139]
Belief-Desire-Intention (BDI) agents [ 143] have improved
reactivity and intelligence in surveillance robotics. On the
learning side, Neural Logic Machines (NLM) [ 144] and
Neuro-Symbolic Concept Learners (NSCL) [ 20] exhibit
the potential of generalized reasoning over structured and
unstructured data, with applications spanning array sorting to
visual question answering. The NS-DR model [ 145] extends
this trajectory by incorporating neural dynamics for causal
reasoning in video-based environments, enabling predictive
physical interaction essential for robotics.
7.2 Question Answering
The application of neuro-symbolic AI in question answer-
ing (QA) represents a critical leap forward in building
systems that can both understand and reason. While tradi-
tional neural models such as Word2V ec [ 146] and GloV e
[147] have enabled semantic parsing of questions through
robust word embeddings, their inability to perform struc-
tured reasoning limits their interpretability and generaliza-
tion. Neuro-symbolic approaches address this limitation by
integrating symbolic reasoning frameworks—such as the
Neuro-Symbolic Program Synthesis (NSPS) model [ 148]
and Prolog-based reasoning systems [149] with deep learning
architectures, thereby enabling more accurate query resolu-
tion across complex datasets like WikiTableQuestions and
Spider. Furthermore, innovations like PIGLeT [ 150], which
ground language in a physical 3D environment, illustrate how
neuro-symbolic systems can bridge abstract linguistic input
with tangible, common-sense reasoning.
7.3 Medicine
The integration of neuro-symbolic AI into medical applica-
tions marks a transformative shift in clinical decision-making
by combining the logical rigor of symbolic systems with the
pattern recognition power of neural networks. This fusion
enables systems to deliver both accuracy and interpretabil-
ity, two pillars crucial in healthcare settings. For instance,
the use of neuro-symbolic reasoning (NSR) in diagnos-
ing acute abdominal pain [ 151] demonstrates how hybrid
AI models can surpass conventional methods in both pre-
cision and personalization. Beyond diagnosis, frameworks
like Neuro-Data-Mine [ 152] facilitate the transformation
of high-dimensional, sub-symbolic medical data into sym-
bolic representations, greatly enhancing the interpretability
of complex datasets such as those involved in cerebrospinal
ﬂuid analysis.
Recent advancements further exemplify this trend. For
example, convolutional neural networks integrated with
attention mechanisms have been applied to magnetic reso-
nance imaging (MRI) for brain tumor classiﬁcation, provid-
ing both accurate localization and interpretable activation
maps for clinical insights [ 153]. Similarly, CardioGuard,
a hybrid neural-symbolic system, enables AI-driven ECG
authentication for predictive health monitoring in telehealth
environments, addressing both performance and explainabil-
ity [154]. In the context of neuro-symbolic IoT applications,
multi-feature fusion CNNs have shown promising results in
EEG-based epileptic seizure prediction, demonstrating how
structured prior knowledge can guide neural inference under
noisy conditions [ 155].
Hybrid formalisms that blend production rules with neural
computation [ 156], as well as transparent architectures like
the discretized interpretable multilayer perceptron (DIMLP)
[157], are redeﬁning how machine learning models explain
their predictions, an essential requirement in high-stakes
domains like oncology and radiology. Even more promis-
ing are comprehensive frameworks such as that of Obot and
Uzoka [ 158], which synergize case-based, rule-based, and
neural methodologies to yield robust, explainable systems
that outperform standalone models. Together, these develop-
ments reﬂect a growing paradigm in which neuro-symbolic
123

Arabian Journal for Science and Engineering (2026) 51:35–67 57
systems contribute not only to clinical accuracy but also to
trust, safety, and real-time human–AI collaboration.
7.4 Military
The integration of neuro-symbolic AI into military oper-
ations marks a strategic evolution in defense technology,
offering a unique synergy between the adaptability of neu-
ral networks and the interpretability of symbolic reasoning.
This hybrid AI paradigm signiﬁcantly enhances key domains
such as autonomous systems, where unmanned vehicles
and drones perform surveillance and logistics independently
[159], and target recognition systems, which automate detec-
tion tasks with superior speed and precision [ 160]. In predic-
tive maintenance, AI models proactively forecast equipment
failures by learning from operational data, thereby reducing
downtime and operational costs [ 161]. Tactical decision-
making and resource management beneﬁt from real-time
data analysis fused with symbolic domain knowledge, aiding
commanders in dynamic battleﬁeld contexts [ 162]. Applica-
tions also extend to coordination and communication among
military units [ 163], and to immersive training simulations
that replicate complex combat scenarios [ 164].
7.5 Computer Vision
The application of neuro-symbolic AI in computer vision sig-
niﬁes a transformative paradigm that bridges low-level per-
ceptual tasks with high-level cognitive reasoning, enabling
AI systems to understand and reason about visual scenes in a
more human-like manner. By fusing deep learning’s capacity
for feature extraction with symbolic AI’s ability to repre-
sent and reason over structured knowledge, frameworks such
as the Neuro-Symbolic Concept Learner (NS-CL) [ 20] and
Logic Tensor Networks (LTNs) [ 165] have shown signiﬁ-
cant promise in enhancing interpretability and abstraction
in visual understanding. Graph Neural Networks (GNNs)
further enrich this integration by embedding visual objects
and their relations within ontologies and knowledge graphs,
which allows models to infer complex relationships in
cluttered or ambiguous images [ 166]. Real-world imple-
mentations, like the intelligent decision support system by
Golovko et al. [ 167], underscore how neuro-symbolic sys-
tems can be deployed effectively in industrial settings, such as
quality control in manufacturing. At the same time, research
on transparent deep learning models, such as the deep dis-
cretized interpretable multilayer perceptrons (DIMLPs) by
Bologna and Hayashi [ 168], highlights the ongoing ten-
sion between performance and explainability, an essential
consideration in safety-critical domains. Moreover, exten-
sions into spatial-temporal analysis [ 169], mental image
generation [ 170], and multimodal tasks like visual ques-
tion answering (VQA) [ 117] illustrate the expansive reach
of neuro-symbolic methods in unifying sensory data with
linguistic and logical processing.
7.6 Program Synthesis and Optimization
The application of neuro-symbolic AI in programming and
optimization represents a signiﬁcant advancement in bridg-
ing data-driven learning with structured logic, fostering
systems that are not only powerful but also interpretable and
efﬁcient. This integration is particularly impactful in program
synthesis, where the fusion of neural networks with symbolic
reasoning enables models to generate and optimize code for
tasks ranging from sorting algorithms [ 148] to more complex
logic programming challenges [ 171]. Tools such as Bhatia
et al.’s neuro-symbolic program corrector [ 172] exemplify
how this synergy enhances programming education, pro-
viding semantically accurate feedback that improves novice
learning outcomes. Additionally, frameworks like logical
neural networks (LNNs) and new languages like Scallop
[173] are paving the way for seamless blending of sym-
bolic formalisms with neural adaptability, improving both
interpretability and scalability. In parallel, efforts to auto-
mate optimization algorithm discovery [ 174] and symbolic
regression using neural-guided genetic programming [ 175]
signify a move toward more autonomous and generalizable
AI systems.
8 Challenges
Despite signiﬁcant advances, there remain gaps in current
research and open questions that deﬁne the future of neuro-
symbolic AI, especially regarding robustness, uncertainty,
and intervenability:
8.1 Benchmarking and Evaluation
A recurring theme is the lack of standardized benchmarks to
evaluate the multi-faceted goals of neuro-symbolic systems.
How do we quantitatively assess a system’s robustness to
logical perturbations or adversarial inputs? How to measure
degrees of interpretability or quality of uncertainty estimates
?
The community is beginning to design challenge tasks
(e.g., systematic generalization tests [ 79], visual question
answering [ 176], calibrating concepts and operations [ 177])
etc. Without agreed upon benchmarks targeting properties
like veriﬁable generalization, calibrated uncertainty, and
explainability [ 178], progress may remain siloed.
An open challenge is creating evaluation frameworks that
can compare very different approaches on these higher-level
criteria fairly. This includes developing robustness stress-
tests (like adversarial example suites or logic inconsistencies
123

58 Arabian Journal for Science and Engineering (2026) 51:35–67
injection) [179] and human-in-the-loop studies to see if inter-
venability truly improves outcomes [ 180].
8.2 Scalability and Real-Time Performance
While neuro-symbolic AI offers promising interpretability
and reasoning capabilities, most current systems remain
limited in scalability, often constrained to small-scale or syn-
thetic benchmarks. As these systems are scaled to handle
internet scale knowledge graphs, high-dimensional sensory
data, or complex real-time tasks, they encounter severe com-
putational bottlenecks, particularly in symbolic reasoning
components such as logic solvers and grounding mecha-
nisms. Differentiable logic layers, while trainable end to end,
often suffer from combinatorial explosion when reasoning
over large rule sets or entity spaces [ 118].
Real-time performance is especially crucial in domains
like robotics, autonomous vehicles, and telehealth, where
decisions must be made under latency constraints. Recent
advances aim to mitigate these issues through modular and
hierarchical designs, approximate symbolic inference, and
scalable neural backends like graph neural networks (GNNs)
that support multi-hop reasoning over large domains [ 126].
Techniques like continual learning, symbolic caching, and
task-speciﬁc rule pruning are emerging strategies to enable
neuro-symbolic models to operate within real-time con-
straints without sacriﬁcing reliability [ 181]. However, few
benchmark datasets exist for evaluating both latency and
inference quality, jointly highlighting a key research gap that
must be addressed to enable practical deployment.
8.3 Dynamic and Non-Monotonic Reasoning
Real-world reasoning is often non-monotonic: new informa-
tion can invalidate old conclusions. Most neuro-symbolic
frameworks today assume a relatively ﬁxed logic. Open-
world reasoning, where the system must handle previously
unseen predicates or dynamically changing rules, is still in
its infancy.
A robust neuro-symbolic agent should cope with evolving
knowledge. How to manage such knowledge updates while
maintaining consistency is a question for future research.
Non-monotonic logic formalisms and truth maintenance sys-
tems could be part of the answer, now combined with
learning. This also ties into lifelong learning: can a neuro-
symbolic system continuously grow its knowledge base from
experience, while ensuring that growth doesn’t introduce
contradictions or undue bias [ 181]? Ensuring safe explo-
ration with logical constraints is another challenge. The agent
should be able to try new strategies without violating critical
rules, which requires balancing exploration with symbolic
rule adherence [ 7]. Meta-learning strategies may help the
system adapt to new knowledge while reﬁning prior sym-
bolic structures [ 182].
8.4 Trust, Fairness, and Ethics
While neuro-symbolic AI offers greater interpretability
through symbolic reasoning, its deployment in real-world
applications raises important ethical and societal challenges.
Symbolic knowledge bases can encode historical biases or
normative assumptions that are not easily scrutinized by end-
users. When combined with data-driven neural components,
such biases may become ampliﬁed under a veneer of logic-
based explainability [ 183]. This “illusion of transparency”
can lead to overconﬁdence in decisions made by systems that
rely on incomplete or biased symbolic rules [ 184]. Moreover,
symbolic rule design is often controlled by developers or
domain experts, reinforcing power asymmetries and exclud-
ing broader stakeholder perspectives [ 185]. In high-stakes
domains like healthcare, law, or education, this may result in
opaque, unchallengeable systems that undermine user auton-
omy and contestability.
To ensure ethical deployment, neuro-symbolic systems
must go beyond technical correctness to support procedural
fairness and democratic accountability. This includes mech-
anisms for human-in-the-loop intervention, the ability to
audit and revise symbolic logic, and participatory rule cura-
tion that reﬂects diverse values [ 186]. Privacy-preserving
neuro-symbolic models and federated architectures can mit-
igate risks of information leakage in sensitive applications
[187]. Future research should develop standards for sym-
bolic rule auditing, institutional governance frameworks, and
interdisciplinary collaborations between AI, law, and ethics.
Without such safeguards, the beneﬁts of neuro-symbolic
AI—interpretability, control, and robustness—may inadver-
tently contribute to new forms of algorithmic harm.
8.5 User Interaction and Acceptance
While intervenability is often touted as a key advantage of
neuro-symbolic AI, its practical utility hinges on a frequently
underexplored dimension: end-user interaction. Intervenabil-
ity is only meaningful if users are both willing and capable of
engaging with the system’s symbolic layer. This raises press-
ing questions at the intersection of neuro-symbolic AI and
Human–Computer Interaction (HCI): How should explana-
tions be presented to users to maximize understanding and
trust? What interface designs enable intuitive rule editing or
concept feedback? When uncertainty is ﬂagged, should the
AI issue a query, a warning, or defer decisions altogether?
Preliminary studies suggest that human–AI collaboration can
exceed the performance of either agent alone, but only when
communication is transparent and effective [ 188].
123

Arabian Journal for Science and Engineering (2026) 51:35–67 59
Beyond usability, these systems offer an opportunity to
implement learning from intervention: Whenever a user mod-
iﬁes a rule, corrects an inference, or clariﬁes a concept, the
system should treat this as a training signal, adjusting neural
parameters, updating symbolic rules, or reﬁning uncertainty
estimates. This feedback loop, sometimes framed as explana-
tory active learning or correction propagation, holds promise
for building progressively more accurate and trustworthy AI
systems through human collaboration.
8.6 Edge Deployment Constraints Across Domains
A recurring challenge across all application domains is the
deployment of neuro-symbolic AI on edge devices. These
platforms such as microcontrollers, ARM-based SoCs, and
FPGAs impose strict limits on memory, power, compute,
and real-time response. Recent approaches like TinyNS
[189] demonstrate joint neural-symbolic operator search and
code generation for microcontroller deployment, adapting
to hardware constraints via platform in the loop optimiza-
tion. Similarly, Wan et al. [ 190] proﬁled neuro-symbolic
workloads, revealing inefﬁciencies tied to memory-bound
symbolic operations and control ﬂow heterogeneity. They
advocate for cross-layer accelerator designs and quantized
symbolic operators. Recent FPGA-centric frameworks such
as NSFlow [ 191] exploit reconﬁgurable dataﬂow and mixed-
precision kernels, demonstrating 31x speedups over embed-
ded GPUs.
To support deployment on edge hardware, memory-
efﬁcient symbolic knowledge graphs, logic operator quan-
tization, and hybrid caching strategies are essential. FPGA
and microcontroller-targeted architectures must also respect
latency, power, and regulatory constraints, especially in
domains like healthcare and autonomous systems. Future
work should develop modular, adaptive neuro-symbolic
architectures that balance symbolic expressivity, neural
learning, and resource efﬁciency to realize real-world edge
deployments.
9 Applications and Opportunities
The applications areas neuro-symbolic AI can be grouped
under the following categories.
9.1 Perception & Planning
In robotics and autonomous systems, neuro-symbolic
pipelines often leverage a two-tier architecture that tightly
integrates perception with high-level planning. The ﬁrst tier
consists of neural perception modules, typically convolu-
tional neural networks (CNNs), vision transformers (ViTs),
or event-based sensors that segment scenes and instan-
tiate detected entities and relationships as logical atoms
or predicates. The second tier engages a symbolic task
and motion planner, which synthesizes policies that sat-
isfy formal task constraints, while runtime monitors enforce
safety invariants during execution. The seminal CLEVR
dataset illustrated the value of explicit scene graphs in
mitigating spurious statistical correlations and improving
generalization in visual reasoning tasks [ 192]. Building on
this, recent robotics frameworks have extended these princi-
ples to physical environments. For example, integrated task
motion planning architectures have demonstrated the feasi-
bility of symbolically guided manipulation and navigation
in unstructured settings, such as cluttered warehouses [ 193].
Advancing these capabilities further, systems like BeliefNet
[194] employ neuro-symbolic context modeling to estimate
traversability probabilities in complex terrains. Here, neu-
ral modules predict affordances, while symbolic reasoning
is used to reconcile perceptual estimates with a belief-state
planner.
9.2 Knowledge & Language
Hybrid reasoning over dynamic knowledge graphs represents
a key application of neuro-symbolic AI in natural language
understanding, enabling tasks such as fact veriﬁcation, legal
analysis, and knowledge base completion. Recent work has
introduced logically grounded embeddings and differentiable
logic layers that support continual learning while preserving
symbolic structure. Constraint-aware learning and rule-based
augmentation mitigate catastrophic forgetting when updat-
ing neural models with new rules, offering scalability to
large-scale KGs. However, challenges remain in balancing
generalization with symbolic consistency, especially under
frequent updates.
Research [ 11] categorized the ﬁeld into three dominant
approaches: logic-constrained embeddings, differentiable
inference engines, and neural-symbolic rule learners. They
highlighted that efﬁcient, approximate inference over evolv-
ing KGs remains a bottleneck in time-critical settings.
Complementing this, [ 195] showed how logic-based super-
vision improves interpretability and factual grounding. Their
work underscores the potential of symbolic priors in reduc-
ing hallucination and enabling safer deployment of LLMs in
structured domains.
9.3 High-Stakes Decision Support
In safety-critical and legally sensitive domains, neuro-
symbolic AI offers a compelling architecture for risk-aware
decision support, fusing high capacity neural perception with
symbolic safeguards that enforce veriﬁable, domain-aligned
constraints. These hybrid stacks are designed to quantify and
manage uncertainty while maintaining transparency, inter-
pretability, and regulatory compliance.
123

60 Arabian Journal for Science and Engineering (2026) 51:35–67
Logic Neural Networks (LNNs) trained on structured
clinical ontologies have demonstrated superior performance
to traditional deep networks in differential diagnosis tasks,
offering not only improved accuracy but also clause-level
interpretability that aligns with emerging FDA transparency
mandates in medical AI [ 196]. In ﬁnancial forensics, neuro-
symbolic Anti-Money Laundering (AML) systems integrate
graph neural anomaly detectors with FA TF-compliant rule
engines to ﬂag illicit transactions. These systems produce
audit-ready symbolic traces, enabling real-time detection
that is both explainable and legally defensible [ 197]. In the
cybersecurity domain, recent advances in uncertainty-aware
neuro-symbolic intrusion detection have yielded architec-
tures capable of open-set detection identifying previously
unseen threats by combining probabilistic symbolic rea-
soning with high-throughput neural trafﬁc classiﬁers [ 198].
In transportation, neuro-symbolic AI is used to enhance
travel demand prediction by combining interpretable deci-
sion tree–based symbolic rules with neural network learning,
enabling models to capture complex geospatial and socioe-
conomic patterns with improved accuracy and transparency
[199].
9.4 Science, Environment & Education
Neuro-symbolic AI is playing an increasingly transformative
role across scientiﬁc discovery, environmental forecasting,
and educational personalization by integrating domain-
speciﬁc symbolic knowledge with powerful neural models.
By embedding known scientiﬁc laws and expert rules into
the learning process, these systems dramatically reduce
search complexity, improve generalization under sparse data
conditions, and offer interpretability aligned with human rea-
soning.
In biomedical science, the MARS system exempliﬁes
this paradigm by augmenting drug mechanism knowledge
graphs with weighted ﬁrst-order logic rules. This enables
it to infer mechanisms of action with state-of-the-art accu-
racy while simultaneously surfacing biochemically grounded
rationales, making its outputs both performant and trustwor-
thy [ 200]. In the environmental sciences, neuro-symbolic
pipelines now support crop-yield forecasting under challeng-
ing, non-stationary conditions. For example, neural satellite
image encoders can be fused with symbolic agronomic
models to produce season-ahead predictions that remain
robust under distributional shift—a key advantage in climate-
sensitive applications [ 201]. In education, adaptive learning
environments are increasingly incorporating neuro-symbolic
elements. Systems like NeuroChat combine LLMs for open-
ended tutoring with pedagogical rule bases and real-time
EEG-driven engagement signals, enabling content to dynam-
ically adjust in complexity based on learner attention and
comprehension levels [ 202].
9.5 Program Synthesis & Verification
In the domain of formal methods and automated reasoning,
neuro-symbolic AI is redeﬁning program synthesis and veri-
ﬁcation by merging the generative ﬂuency of LLMs with the
rigor of symbolic logic. One of the most promising strate-
gies is to augment LLM driven code generation loops with
symbolic type systems and Satisﬁability Modulo Theories
(SMT) veriﬁers, thereby ensuring that outputs meet formal
correctness constraints before deployment.
Recent advances in neural theorem proving exemplify
this hybrid approach. Neural models are now capable of
translating informal natural language speciﬁcations into for-
mal proofs in systems like Lean and Isabelle and can
repair incomplete or erroneous proof sketches incrementally,
an essential capability for interactive veriﬁcation pipelines
[203].
Pushing the frontier further, DeepMind’s AlphaProof
[204] integrates an AlphaZero-style planner with a Gemini-
class LLM to solve Olympiad-level mathematical proofs,
achieving high performance while adhering to formal sound-
ness guarantees. This suggests a viable path toward LLM-
guided symbolic search, where creativity and correctness
coexist through iterative reﬁnement.
9.6 Big Data and IoT Ecosystems
The integration of neuro-symbolic AI with Big Data and IoT
frameworks offers a pathway toward scalable, interpretable,
and context-aware intelligence. While most existing work
focuses on optimizing deep neural networks using MapRe-
duce for parallelism and efﬁciency, these efforts lay the
groundwork for embedding symbolic reasoning layers atop
high-throughput pipelines. For example, Liu et al. [ 205] and
Le et al. [ 206] propose DCNN pruning and swarm based opti-
mization under MapReduce to reduce parameter overhead
and improve convergence conditions under which symbolic
constraints could enforce domain-consistent learning. Y u et
al. [207] introduce entropy-weighted clustering to better cap-
ture latent data structure, a strategy that can be reinforced
by symbolic taxonomies for reasoning over spatial relation-
ships. Similarly, Mao et al. [ 208] optimize frequent itemset
mining using dynamic grouping, highlighting the need for
symbolic generalization in pattern discovery. Mao et al. [ 209]
address data skew and initialization sensitivity in K-means
via grid-based hashing and adaptive grouping conditions
where symbolic abstraction could support stability and com-
positionality. Nanehkaran et al. [ 210] bridge IoT health data
and recommendation systems using machine learning, but
future improvements may require symbolic medical ontolo-
gies for explainable diagnosis. These advances suggest a
clear opportunity, enriching big data-driven AI pipelines with
123

Arabian Journal for Science and Engineering (2026) 51:35–67 61
symbolic structures can yield hybrid systems that are both
data efﬁcient and semantically robust.
10 Conclusion
Neuro-symbolic AI represents a promising hybrid paradigm
that combines the learning capabilities of neural networks
with the logical rigor and transparency of symbolic reason-
ing. This survey systematically explored its role in addressing
three critical dimensions robustness, UQ, and intervenability
through architectural innovations, application, and emerging
research frameworks. By bridging perception and reason-
ing, neuro-symbolic systems offer a compelling solution to
the limitations of purely statistical models in high-stakes
domains such as healthcare, cybersecurity, and autonomous
systems.
To advance the practical deployment and research matu-
rity of neuro-symbolic AI, several concrete next steps are
essential. First, the community should prioritize the devel-
opment of scalable neuro-symbolic benchmarks and datasets
that capture real-world complexity, such as multimodal rea-
soning under uncertainty or long-horizon causal planning.
Second, experiments should focus on integrating symbolic
reasoning modules with foundation models to test how
symbolic priors can guide large-scale inference more reli-
ably. Third, research should emphasize developing real-time
neuro-symbolic control systems for robotics and IoT envi-
ronments, including interpretable feedback mechanisms and
safe failure modes. Fourth, from an engineering standpoint,
toolchains and frameworks such as PyProb, Scallop, and
NeurASP should be expanded to support modular deploy-
ment, uncertainty tracking, and human-in-the-loop interven-
tions.
Interdisciplinary studies that evaluate user trust, trans-
parency, and ethical alignment in neuro-symbolic systems are
critical for bridging the gap between algorithmic design and
end-user acceptance. Overall, the ﬁeld must evolve toward
systems that are not only accurate and interpretable but also
scalable, certiﬁable, and aligned with domain constraints. By
focusing on these targeted directions, the neuro-symbolic AI
community can accelerate the transition from experimental
prototypes to impactful, real-world AI systems.
Funding This research was partially supported by the U.S. National
Science Foundation through Grant No. 2317117
Open Access This article is licensed under a Creative Commons
Attribution 4.0 International License, which permits use, sharing, adap-
tation, distribution and reproduction in any medium or format, as
long as you give appropriate credit to the original author(s) and the
source, provide a link to the Creative Commons licence, and indi-
cate if changes were made. The images or other third party material
in this article are included in the article’s Creative Commons licence,
unless indicated otherwise in a credit line to the material. If material
is not included in the article’s Creative Commons licence and your
intended use is not permitted by statutory regulation or exceeds the
permitted use, you will need to obtain permission directly from the copy-
right holder. To view a copy of this licence, visit http://creativecomm
ons.org/licenses/by/4.0/.
References
1. Kaur, D.; Uslu, S.; Rittichier, K.J.; Durresi, A.: Trustworthy arti-
ﬁcial intelligence: a review. ACM Comput. Surv. (CSUR) 55(2),
1–38 (2022)
2. Rudin, C.: Stop explaining black box machine learning models
for high stakes decisions and use interpretable models instead.
Nat. Mach. Intell. 1(5), 206–215 (2019)
3. Hamon, R.; Junklewitz, H.; Sanchez, I., et al.: Robustness and
explainability of artiﬁcial intelligence. Publ. Off. Eur. Union 207,
2020 (2020)
4. Abdar, M.; Pourpanah, F.; Hussain, S.; Rezazadegan, D.; Liu, L.;
Ghavamzadeh, M.; Fieguth, P .; Cao, X.; Khosravi, A.; Acharya,
U.R., et al.: A review of uncertainty quantiﬁcation in deep learn-
ing: techniques, applications and challenges. Inf. Fus. 76, 243–297
(2021)
5. Laguna, S.; Marcinkeviˇ cs, R.; V andenhirtz, M.; V ogt, J.: Beyond
concept bottleneck models: How to make black boxes interven-
able? Adv. Neural. Inf. Process. Syst. 37, 85006–85044 (2024)
6. V elasquez, A.; Song, H.H.; Ravikumar, P .; Sastry, S.S.; Neema, S.:
Neuro-symbolic AI: Foundations and Applications. Wiley-IEEE
Press, Hoboken (2025)
7. Acharya, K.; Raza, W.; Dourado, C.; V elasquez, A.; Song, H.H.:
Neurosymbolic reinforcement learning and planning: a survey.
IEEE Trans. Artif. Intell. 5(5), 1939–1953 (2024). https://doi.org/
10.1109/TAI.2023.3311428
8. Bhuyan, B.P .; Ramdane-Cherif, A.; Tomar, R.; Singh, T.: Neuro-
symbolic artiﬁcial intelligence: a survey. Neural Comput. Appl.
36(21), 12809–12844 (2024)
9. Piplai, A.; Kotal, A.; Mohseni, S.; Gaur, M.; Mittal, S.; Joshi,
A.: Knowledge-enhanced neurosymbolic artiﬁcial intelligence for
cybersecurity and privacy. IEEE Internet Comput. 27(5), 43–48
(2023)
10. Hagos, D.H.; Rawat, D.B.: Neuro-symbolic AI for military appli-
cations. IEEE Trans. Artif. Intell. (2024). https://doi.org/10.1109/
TAI.2024.3444746
11. DeLong, L.N.; Mir, R.F.; Fleuriot, J.D.: Neurosymbolic AI for
reasoning over knowledge graphs: a survey. IEEE Trans. Neural
Netw. Learn. Syst. (2024). https://doi.org/10.1109/TNNLS.2024.
3420218
12. Renkhoff, J.; Feng, K.; Meier-Doernberg, M.; V elasquez, A.;
Song, H.H.: A survey on veriﬁcation and validation, testing and
evaluations of neurosymbolic artiﬁcial intelligence. IEEE Trans.
Artif. Intell. 5(8), 3765–3779 (2024)
13. LeCun, Y .; Bengio, Y .; Hinton, G.: Deep learning. Nature
521(7553), 436–444 (2015)
14. Bader, S.; Hitzler, P .: Dimensions of neural-symbolic integration-
a structured survey. arxiv:cs/0511042 (2005)
15. Kautz, H.: The third AI summer. AI Mag. 43, 105–125 (2022)
16. Ghaffari, P .: Leveraging Deep Learning for Multilingual
Sentiment Analysis. AYLIEN Ltd.. Accessed: 2025-11-29.
https://www.linkedin.com/pulse/leveraging-deep-learning-
multilingual-sentiment-parsa-ghaffari
17. Silver, D.; Huang, A.; Maddison, C.J.; Guez, A.; Sifre, L.; V an Den
Driessche, G.; Schrittwieser, J.; Antonoglou, I.; Panneershelvam,
V .; Lanctot, M., et al.: Mastering the game of go with deep neural
networks and tree search. Nature 529(7587), 484–489 (2016)
123

62 Arabian Journal for Science and Engineering (2026) 51:35–67
18. Silver, D.; Schrittwieser, J.; Simonyan, K.; Antonoglou, I.; Huang,
A.; Guez, A.; Hubert, T.; Baker, L.; Lai, M.; Bolton, A., et al.:
Mastering the game of go without human knowledge. Nature
550(7676), 354–359 (2017)
19. Suchan, J.; Bhatt, M.; V aradarajan, S.: Commonsense visual
sensemaking for autonomous driving-on generalised neurosym-
bolic online abduction integrating vision and semantics. Artif.
Intell. 299, 103522 (2021)
20. Mao, J.; Gan, C.; Kohli, P .; Tenenbaum, J.B.; Wu, J.: The neuro-
symbolic concept learner: Interpreting scenes, words, and sen-
tences from natural supervision. arXiv preprint arXiv:1904.12584
(2019)
21. Lample, G.; Charton, F.: Deep learning for symbolic mathematics.
arXiv preprint arXiv:1912.01412 (2019)
22. Smolensky, P .; Lee, M.; He, X.; Yih, W.-t.; Gao, J.; Deng, L.: Basic
reasoning with tensor product representations. arXiv preprint
arXiv:1601.02745 (2016)
23. Badreddine, S.; Garcez, A.D.; Seraﬁni, L.; Spranger, M.: Logic
tensor networks. Artif. Intell. 303, 103649 (2022)
24. Kahneman, D.: Thinking. Fast and Slow. Macmillan, New Y ork
(2011)
25. Man, D.; Vision, A.: A Computational Investigation into the
Human Representation and Processing of Visual Information.
Freeman and Company, San Francisco, WH San Francisco (1982)
26. Y u, D.; Yang, B.; Liu, D.; Wang, H.; Pan, S.: A survey on neural-
symbolic learning systems. Neural Netw. 166, 105–126 (2023)
27. Garcez, A.S.; Gori, M.; Lamb, L.; Seraﬁni, L.; Spranger, M.; Tran,
S.: Neural-symbolic computing: an effective methodology for
principled integration of machine learning and reasoning. FLAP
6, 611–632 (2019)
28. Hu, Z.; Ma, X.; Liu, Z.; Hovy, E.H.; Xing, E.P .: Harnessing deep
neural networks with logic rules. ArXiv:abs/1603.06318 (2016)
29. Manhaeve, R.; Dumancic, S.; Kimmig, A.; Demeester, T.;
De Raedt, L.: Deepproblog: neural probabilistic logic program-
ming. In: Advances in neural information processing systems 31
(2018)
30. Freiesleben, T.; Grote, T.: Beyond generalization: a theory of
robustness in machine learning. Synthese 202(4), 109 (2023)
31. Wang, J.; Ai, J.; Lu, M.; Su, H.; Y u, D.; Zhang, Y .; Zhu, J.; Liu,
J.: A survey of neural network robustness assessment in image
recognition. arXiv preprint arXiv:2404.08285 (2024)
32. Schweimer, C.; Scher, S.: Quantifying probabilistic robustness of
tree-based classiﬁers against natural distortions. arXiv preprint
arXiv:2208.10354 (2022)
33. Katz, G.; Barrett, C.; Dill, D.L.; Julian, K.; Kochenderfer, M.J.:
Reluplex: An efﬁcient smt solver for verifying deep neural
networks. In: Computer Aided V eriﬁcation: 29th International
Conference, CA V 2017, Heidelberg, 30, pp. 97–117 (2017).
Springer
34. Kabaha, A.; Cohen, D.D.: V eriﬁcation of neural networks’ global
robustness. Proc. ACM Progr. Languages 8(OOPSLA1), 1010–
1039 (2024)
35. Bai, T.; Luo, J.; Zhao, J.; Wen, B.; Wang, Q.: Recent advances
in adversarial training for adversarial robustness. arXiv preprint
arXiv:2102.01356 (2021)
36. Goji´ c, G.; Vincan, V .; Kundaˇ cina, O.; Miškovi´ c, D.; Dragan,
D.: Non-adversarial robustness of deep learning methods for
computer vision. In: 2023 10th International Conference on Elec-
trical, Electronic and Computing Engineering (IcETRAN), pp.
1–9 (2023). IEEE
37. Mohapatra, J.; Weng, T.-W.; Chen, P .-Y .; Liu, S.; Daniel, L.:
Towards verifying robustness of neural networks against a family
of semantic perturbations. In: Proceedings of the IEEE/CVF Con-
ference on Computer Vision and Pattern Recognition, pp. 244–252
(2020)
38. Bastani, O.; Ioannou, Y .; Lampropoulos, L.; Vytiniotis, D.; Nori,
A.; Criminisi, A.: Measuring neural net robustness with con-
straints. In: Advances in Neural Information Processing Systems
29 (2016)
39. Mangal, R.; Nori, A.V .; Orso, A.: Robustness of neural networks:
a probabilistic and practical approach. In: 2019 IEEE/ACM 41st
International Conference on Software Engineering: New Ideas
and Emerging Results (ICSE-NIER), pp. 93–96 (2019). IEEE
40. Gopinath, D.; Katz, G.; Pasareanu, C.S.; Barrett, C.: Deepsafe:
A data-driven approach for checking adversarial robustness in
neural networks. arXiv preprint arXiv:1710.00486 (2017)
41. Goodfellow, I.J.; Shlens, J.; Szegedy, C.: Explaining and harness-
ing adversarial examples. arXiv preprint arXiv:1412.6572 (2014)
42. Tsipras, D.; Santurkar, S.; Engstrom, L.; Turner, A.; Madry,
A.: Robustness may be at odds with accuracy. arXiv preprint
arXiv:1805.12152 (2018)
43. Liu, Y .; Mao, S.; Mei, X.; Yang, T.; Zhao, X.: Sensitivity of
adversarial perturbation in fast gradient sign method. In: 2019
IEEE Symposium Series on Computational Intelligence (SSCI),
pp. 433–436 (2019). https://doi.org/10.1109/SSCI44817.2019.
9002856
44. Deng, Y .; Karam, L.J.: Universal adversarial attack via enhanced
projected gradient descent. In: 2020 IEEE International Confer-
ence on Image Processing (ICIP), pp. 1241–1245 (2020). IEEE
45. Madry, A.; Makelov, A.; Schmidt, L.; Tsipras, D.; Vladu, A.:
Towards deep learning models resistant to adversarial attacks.
arXiv preprint arXiv:1706.06083 (2017)
46. Hendrycks, D.; Dietterich, T.: Benchmarking neural network
robustness to common corruptions and perturbations. arXiv
preprint arXiv:1903.12261
(2019)
47. Carlini, N.; Wagner, D.: Towards evaluating the robustness of neu-
ral networks. In: 2017 IEEE Symposium on Security and Privacy
(SP), pp. 39–57 (2017). IEEE
48. Athalye, A.; Carlini, N.; Wagner, D.: Obfuscated gradients give
a false sense of security: Circumventing defenses to adversarial
examples. In: International Conference on Machine Learning, pp.
274–283 (2018). PMLR
49. Zhang, R.; Isola, P .; Efros, A.A.; Shechtman, E.; Wang, O.: The
unreasonable effectiveness of deep features as a perceptual metric.
In: Proceedings of the IEEE Conference on Computer Vision and
Pattern Recognition, pp. 586–595 (2018)
50. Moosavi-Dezfooli, S.-M.; Fawzi, A.; Frossard, P .: Deepfool: a
simple and accurate method to fool deep neural networks. In:
Proceedings of the IEEE Conference on Computer Vision and
Pattern Recognition, pp. 2574–2582 (2016)
51. Hein, M.; Andriushchenko, M.; Bitterwolf, J.: Why relu networks
yield high-conﬁdence predictions far away from the training
data and how to mitigate the problem. In: Proceedings of the
IEEE/CVF Conference on Computer Vision and Pattern Recog-
nition, pp. 41–50 (2019)
52. Hendrycks, D.; Gimpel, K.: A baseline for detecting misclassi-
ﬁed and out-of-distribution examples in neural networks. arXiv
preprint arXiv:1610.02136 (2016)
53. Lakshminarayanan, B.; Pritzel, A.; Blundell, C.: Simple and scal-
able predictive uncertainty estimation using deep ensembles. In:
Advances in Neural Information Processing Systems 30 (2017)
54. Gal, Y .; Ghahramani, Z.: Dropout as a Bayesian approximation:
representing model uncertainty in deep learning. In: International
Conference on Machine Learning, pp. 1050–1059 (2016). PMLR
55. Smith, L.; Gal, Y .: Understanding measures of uncertainty for
adversarial example detection. arXiv preprint arXiv:1803.08533
(2018)
56. Chrysos, G.; Li, Y .; Angelopoulos, A.N.; Bates, S.; Plank, B.;
Khan, M.E.: Quantify uncertainty and hallucination in foundation
models: the next frontier in reliable AI. In: ICLR 2025 Workshop
Proposals
123

Arabian Journal for Science and Engineering (2026) 51:35–67 63
57. Incorvaia, G.; Hond, D.; Asgari, H.: Uncertainty quantiﬁcation of
machine learning model performance via anomaly-based dataset
dissimilarity measures. Electronics 13(5), 939 (2024)
58. Huang, Z.; Lam, H.; Zhang, H.: Efﬁcient uncertainty quantiﬁca-
tion and reduction for over-parameterized neural networks. Adv.
Neural. Inf. Process. Syst. 36, 64428–64467 (2023)
59. Chan, M.; Molina, M.; Metzler, C.: Estimating epistemic and
aleatoric uncertainty with a single model. Adv. Neural. Inf. Pro-
cess. Syst. 37, 109845–109870 (2024
60. Sohn, K.; Lee, H.; Yan, X.: Learning structured output represen-
tation using deep conditional generative models. In: Advances in
Neural Information Processing Systems, 28 (2015)
61. Fakour, F.; Mosleh, A.; Ramezani, R.: A structured review of
literature on uncertainty in machine learning & deep learning.
arXiv preprint arXiv:2406.00332 (2024)
62. Blei, D.M.; Kucukelbir, A.; McAuliffe, J.D.: V ariational infer-
ence: a review for statisticians. J. Am. Stat. Assoc. 112(518),
859–877 (2017)
63. Friston, K.; Mattout, J.; Trujillo-Barreto, N.; Ashburner, J.; Penny,
W.: V ariational free energy and the Laplace approximation. Neu-
roimage 34(1), 220–234 (2007)
64. Hoffman, M.D.: Learning deep latent gaussian models with
Markov chain Monte Carlo. In: International Conference on
Machine Learning, pp. 1510–1519 (2017). PMLR
65. Laurent, O.; Lafage, A.; Tartaglione, E.; Daniel, G.; Martinez,
J.-M.; Bursuc, A.; Franchi, G.: Packed-ensembles for efﬁcient
uncertainty estimation. arXiv preprint arXiv:2210.09184 (2022)
66. Wild, V .D.; Ghalebikesabi, S.; Sejdinovic, D.; Knoblauch, J.: A
rigorous link between deep ensembles and (variational) bayesian
methods. Adv. Neural. Inf. Process. Syst. 36, 39782–39811 (2023)
67. Wenzel, F.; Snoek, J.; Tran, D.; Jenatton, R.: Hyperparameter
ensembles for robustness and uncertainty quantiﬁcation. Adv.
Neural. Inf. Process. Syst. 33, 6514–6527 (2020)
68. Bidusa, O.R.; Markovitch, S.: Concept layers: enhancing inter-
pretability and intervenability via llm conceptualization. arXiv
preprint arXiv:2502.13632 (2025)
69. Koh, P .W., Nguyen, T., Tang, Y .S., Mussmann, S., Pierson, E.,
Kim, B., Liang, P .: Concept bottleneck models. In: International
Conference on Machine Learning, pp. 5338–5348 (2020). PMLR
70. Jiao, L.; Wang, Y .; Liu, X.; Li, L.; Liu, F.; Ma, W.; Guo, Y .; Chen,
P .; Yang, S.; Hou, B.: Causal inference meets deep learning: a
comprehensive survey. Research 7, 0467 (2024)
71. Zhang, D.; Zhang, H.; Tang, J.; Hua, X.-S.; Sun, Q.: Causal
intervention for weakly-supervised semantic segmentation. Adv.
Neural. Inf. Process. Syst. 33, 655–666 (2020)
72. Ravfogel, S., Svete, A., Snæbjarnarson, V ., Cotterell, R.: Gumbel
counterfactual generation from language models. In: ICLR (2025)
73. Rajaram, A.; Chowdhury, N.; Torralba, A.; Andreas, J.;
Schwettmann, S.: Automatic discovery of visual circuits. arXiv
preprint arXiv:2404.14349 (2024)
74. Marconato, E.; Teso, S.; V ergari, A.; Passerini, A.: Not all neuro-
symbolic concepts are created equal: analysis and mitigation of
reasoning shortcuts. Adv. Neural. Inf. Process. Syst. 36, 72507–
72539 (2023)
75. Garcez, A.D.; Lamb, L.C.: Neurosymbolic AI: the 3rd wave. Artif.
Intell. Rev. 56(11), 12387–12406 (2023)
76. Michel-Delétie, C.; Sarker, M.K.: Neuro-symbolic methods for
trustworthy AI: a systematic review. IOS Press (2024). https://
neurosymbolic-ai-journal.com/system/ﬁles/nai-paper-726.pdf
77. Calanzone, D.; Teso, S.; V ergari, A.: Logically consistent lan-
guage models via neuro-symbolic integration. arXiv preprint
arXiv:2409.13724 (2024)
78. Li, B.; Li, Z.; Du, Q.; Luo, J.; Wang, W.; Xie, Y .; Stepputtis, S.;
Wang, C.; Sycara, K.; Ravikumar, P ., et al.: Logicity: advancing
neuro-symbolic AI with abstract urban simulation. Adv. Neural.
Inf. Process. Syst. 37, 69840–69864 (2024)
79. Lake, B.; Baroni, M.: Generalization without systematicity: on
the compositional skills of sequence-to-sequence recurrent net-
works. In: International Conference on Machine Learning, pp.
2873–2882 (2018). PMLR
80. Hudson, D.A.; Manning, C.D.: Gqa: a new dataset for real-world
visual reasoning and compositional question answering. In: Pro-
ceedings of the IEEE/CVF Conference on Computer Vision and
Pattern Recognition, pp. 6700–6709 (2019)
81. Yi, K.; Gan, C.; Li, Y .; Kohli, P .; Wu, J.; Torralba, A.; Tenen-
baum, J.B.: Clevrer: collision events for video representation and
reasoning. arXiv preprint arXiv:1910.01442 (2019)
82. Cornelio, C.; Diab, M.: Recover: A neuro-symbolic framework
for failure detection and recovery. In: 2024 IEEE/RSJ Interna-
tional Conference on Intelligent Robots and Systems (IROS), pp.
12435–12442 (2024). https://doi.org/10.1109/IROS58592.2024.
10801853
83. Gaur, M.; Sheth, A.: Building trustworthy neurosymbolic ai sys-
tems: consistency, reliability, explainability, and safety. AI Mag.
45(1), 139–155 (2024)
84. Ludan, J.M.; Meng, Y .; Nguyen, T.; Shah, S.; Lyu, Q.; Apid-
ianaki, M.; Callison-Burch, C.: Explanation-based ﬁnetuning
makes models more robust to spurious cues. arXiv preprint
arXiv:2305.04990 (2023)
85. Cornelio, C.; Diab, M.: Recover: a neuro-symbolic framework
for failure detection and recovery. In: 2024 IEEE/RSJ Interna-
tional Conference on Intelligent Robots and Systems (IROS), pp.
12435–12442 (2024). IEEE
86. Potosnak, W.: Robust rule learning for reliable and interpretable
insight into expertise transfer opportunities. In: Proceedings of the
AAAI Conference on Artiﬁcial Intelligence, vol. 36, pp. 13136–
13137 (2022)
87. Smith, R.C.: Uncertainty Quantiﬁcation: Theory, Implementa-
tion, and Applications. SIAM, Philadelphia (2024)
88. Richardson, M.; Domingos, P .: Markov logic networks. Mach.
Learn. 62, 107–136 (2006)
89. Bach, S.H.; Broecheler, M.; Huang, B.; Getoor, L.: Hinge-loss
Markov random ﬁelds and probabilistic soft logic. J. Mach. Learn.
Res. 18(109), 1–67 (2017)
90. Pryor, C.; Dickens, C.; Augustine, E.; Albalak, A.; Wang, W.;
Getoor, L.: Neupsl: neural probabilistic soft logic. arXiv preprint
arXiv:2205.14268 (2022)
91. Zheng, Y .; Xu, Z.; Wu, T.; Yi, Z.: A systematic survey of fuzzy
deep learning for uncertain medical data. Artif. Intell. Rev. 57(9),
230 (2024)
92. Badreddine, S.; Garcez, A.; Seraﬁni, L.; Spranger, M.: Logic ten-
sor networks. Artif. Intell. (2022). https://doi.org/10.1016/j.artint.
2021.103649
93. Riegel, R.; Gray, A.; Luus, F.; Khan, N.; Makondo, N.; Akhal-
waya, I.Y .; Qian, H.; Fagin, R.; Barahona, F.; Sharma, U.,et al.:
Logical neural networks. arXiv preprint arXiv:2006.13155 (2020)
94. Fenske, O.; Bader, S.; Kirste, T.: Neuro-symbolic artiﬁcial intel-
ligence for patient monitoring. In: Joint European Conference on
Machine Learning and Knowledge Discovery in Databases, pp.
19–25 (2023). Springer
95. Lake, B.M.; Salakhutdinov, R.; Tenenbaum, J.B.: Human-level
concept learning through probabilistic program induction. Sci-
ence 350(6266), 1332–1338 (2015)
96. Bingham, E.; Chen, J.P .; Jankowiak, M.; Obermeyer, F.; Pradhan,
N.; Karaletsos, T.; Singh, R.; Szerlip, P .; Horsfall, P .; Goodman,
N.D.: Pyro: deep universal probabilistic programming. J. Mach.
Learn. Res. 20(28), 1–6 (2019)
97. Baudart, G.; Burroni, J.; Hirzel, M.; Mandel, L.; Shinnar, A.: Com-
piling stan to generative probabilistic languages and extension
to deep probabilistic programming. In: Proceedings of the 42nd
ACM SIGPLAN International Conference on Programming Lan-
guage Design and Implementation, pp. 497–510 (2021)
123

64 Arabian Journal for Science and Engineering (2026) 51:35–67
98. Xu, K.; Srivastava, A.; Gutfreund, D.; Sosa, F.; Ullman, T.; Tenen-
baum, J.; Sutton, C.: A Bayesian-symbolic approach to reasoning
and learning in intuitive physics. Adv. Neural. Inf. Process. Syst.
34, 2478–2490 (2021)
99. Jospin, L.V .; Laga, H.; Boussaid, F.; Buntine, W.; Bennamoun, M.:
Hands-on Bayesian neural networks—a tutorial for deep learning
users. IEEE Comput. Intell. Mag. 17(2), 29–48 (2022
100. Gawlikowski, J.; Tassi, C.R.N.; Ali, M.; Lee, J.; Humt, M.; Feng,
J.; Kruspe, A.; Triebel, R.; Jung, P .; Roscher, R., et al.: A survey of
uncertainty in deep neural networks. Artif. Intell. Rev. 56(Suppl
1), 1513–1589 (2023)
101. V elasquez, A.: Transfer from imprecise and abstract models to
autonomous technologies (tiamat). Defense Advanced Research
Projects Agency (DARPA) Program Solicitation (2023)
102. Evans, R.; Grefenstette, E.: Learning explanatory rules from noisy
data. J. Artif. Intell. Res. 61, 1–64 (2018)
103. Rocktäschel, T.; Riedel, S.: End-to-end differentiable proving. In:
Advances in neural information processing systems 30 (2017)
104. Yang, Z.; Ishay, A.; Lee, J.: Neurasp: embracing neural networks
into answer set programming. arXiv preprint arXiv:2307.07700
(2023)
105. Eiter, T.; Higuera, N.; Oetsch, J.; Pritz, M.: A neuro-symbolic
asp pipeline for visual question answering. Theory Pract. Logic
Program. 22(5), 739–754 (2022)
106. Xu, J.; Zhang, Z.; Friedman, T.; Liang, Y .; Broeck, G.: A seman-
tic loss function for deep learning with symbolic knowledge. In:
International Conference on Machine Learning, pp. 5502–5511
(2018). PMLR
107. Chen, X.; Hu, Z.; Sun, Y .: Fuzzy logic based logical query
answering on knowledge graphs. In: Proceedings of the AAAI
Conference on Artiﬁcial Intelligence, vol. 36, pp. 3939–3948
(2022)
108. Zhang, X.; Sheng, V .S.: Neuro-symbolic AI: explainability, chal-
lenges, and future trends. arXiv preprint arXiv:2411.04383 (2024)
109. Wagner, B.J.; Garcez, A.: A neurosymbolic approach to AI
alignment. Neurosymbolic Artiﬁcial Intelligence (Preprint), 1–12
(2024)
110. Debot, D.; Barbiero, P .; Giannini, F.; Ciravegna, G.; Diligenti, M.;
Marra, G.: Interpretable concept-based memory reasoning. arXiv
preprint arXiv:2407.15527 (2024)
111. Espinosa Zarlenga, M.; Barbiero, P .; Ciravegna, G.; Marra, G.;
Giannini, F.; Diligenti, M.; Shams, Z.; Precioso, F.; Melacci,
S.; Weller, A., et al.: Concept embedding models: beyond the
accuracy-explainability trade-off. Adv. Neural. Inf. Process. Syst.
35, 21400–21413 (2022)
112. Greco, G.; Alberici, F.; Palmonari, M.; Cosentini, A.: Declarative
encoding of fairness in logic tensor networks. In: ECAI 2023, pp.
908–915. IOS Press (2023)
113. Teso, S.; Kersting, K.: Explanatory interactive machine learn-
ing. In: Proceedings of the 2019 AAAI/ACM Conference on AI,
Ethics, and Society, pp. 239–245 (2019)
114. Stammer, W.; Schramowski, P .; Kersting, K.: Right for the right
concept: Revising neuro-symbolic concepts by interacting with
their explanations. In: Proceedings of the IEEE/CVF Conference
on Computer Vision and Pattern Recognition, pp. 3619–3629
(2021)
115. Bontempelli, A.; Teso, S.; Tentori, K.; Giunchiglia, F.; Passerini,
A.: Concept-level debugging of part-prototype networks. arXiv
preprint arXiv:2205.15769 (2022)
116. Huang, J.; Li, Z.; Chen, B.; Samel, K.; Naik, M.; Song, L.;
Si, X.: Scallop: from probabilistic deductive databases to scal-
able differentiable reasoning. Adv. Neural. Inf. Process. Syst. 34,
25134–25145 (2021)
117. Yi, K.; Wu, J.; Gan, C.; Torralba, A.; Kohli, P .; Tenenbaum, J.:
Neural-symbolic vqa: disentangling reasoning from vision and
language understanding. In: Advances in Neural Information Pro-
cessing Systems 31 (2018)
118. Manhaeve, R.; Dumanˇ ci´c, S.; Kimmig, A.; Demeester, T.; De
Raedt, L.: Neural probabilistic logic programming in deep-
problog. Artif. Intell. 298, 103504 (2021). https://doi.org/10.
1016/j.artint.2021.103504
119. Garnelo, M.; Shanahan, M.: Reconciling deep learning with sym-
bolic artiﬁcial intelligence: representing objects and relations.
Curr. Opin. Behav. Sci. 29, 17–23 (2019)
120. Nickel, M.; Murphy, K.; Tresp, V .; Gabrilovich, E.: A review
of relational machine learning for knowledge graphs. Proc.
IEEE 104(1), 11–33 (2016). https://doi.org/10.1109/JPROC.
2015.2483592
121. Battaglia, P .W.; Hamrick, J.B.; Bapst, V .; Sanchez-Gonzalez, A.;
Zambaldi, V .; Malinowski, M.; Tacchetti, A.; Raposo, D.; Santoro,
A.; Faulkner, R.,et al.: Relational inductive biases, deep learning,
and graph networks. arXiv preprint arXiv:1806.01261 (2018)
122. Bekkum, M.; Boer, M.; Harmelen, F.; Meyer-Vitali, A.; Teije,
A.T.: Modular design patterns for hybrid learning and reasoning
systems: a taxonomy, patterns and use cases. Appl. Intell. 51(9),
6528–6546 (2021)
123. Lo, K.M.; Liang, Y .; Du, W.; Fan, Y .; Wang, Z.; Huang, W.; Ma,
L.; Fu, J.: m2mkd: Module-to-module knowledge distillation for
modular transformers. arXiv preprint arXiv:2402.16918 (2024)
124. Kautz, H.: The third AI summer: Aaai robert s. engelmore memo-
rial lecture. AI Mag. 43(1), 105–125 (2022)
125. Wang, Q.; Mao, Z.; Wang, B.; Guo, L.: Knowledge graph embed-
ding: a survey of approaches and applications. IEEE Trans.
Knowl. Data Eng. 29(12), 2724–2743 (2017)
126. Shengyuan, C.; Cai, Y .; Fang, H.; Huang, X.; Sun, M.: Differen-
tiable neuro-symbolic reasoning on large-scale knowledge graphs.
Adv. Neural. Inf. Process. Syst. 36, 28139–28154 (2023)
127. Minervini, P .; Riedel, S.; Stenetorp, P .; Grefenstette, E.; Rock-
täschel, T.: Learning reasoning strategies in end-to-end differen-
tiable proving. In: International Conference on Machine Learning,
pp. 6938–6949 (2020). PMLR
128. Dragone, P .; Teso, S.; Passerini, A.: Neuro-symbolic con-
straint programming for structured prediction. arXiv preprint
arXiv:2103.17232 (2021)
129. Dong, Y .; Mu, R.; Zhang, Y .; Sun, S.; Zhang, T.; Wu, C.; Jin,
G.; Qi, Y .; Hu, J.; Meng, J.,et al.: Safeguarding large language
models: a survey. arXiv preprint arXiv:2406.02622 (2024)
130. Carpenter, B.; Gelman, A.; Hoffman, M.D.; Lee, D.; Goodrich,
B.; Betancourt, M.; Brubaker, M.; Guo, J.; Li, P .; Riddell, A.:
Stan: a probabilistic programming language. J. Stat. Softw. 76,
1–32 (2017)
131. Fierens, D.; Broeck, G.; Renkens, J.; Shterionov, D.; Gutmann,
B.; Thon, I.; Janssens, G.; De Raedt, L.: Inference and learning
in probabilistic logic programs using weighted Boolean formulas.
Theory Pract. Logic Program. 15(3), 358–401 (2015)
132. Goodman, N.D.; Stuhlmüller, A.: The design and implemen-
tation of probabilistic programming languages. http://dippl.org.
Accessed: 2025-11-29 (2014)
133. Richards, L.E.; Yaros, J.; Babcock, J.; Ly, C.; Cosbey, R.;
Doster, T.; Matuszek, C.: On the promise for assurance of dif-
ferentiable neurosymbolic reasoning paradigms. arXiv preprint
arXiv:2502.08932 (2025)
134. Ramalingam, R.; Park, S.; Bastani, O.: Uncertainty quantiﬁcation
for neurosymbolic programs via compositional conformal predic-
tion. arXiv preprint arXiv:2405.15912 (2024)
135. Bosnjak, M.; Rocktäschel, T.; Naradowsky, J.; Riedel,
S.: Programming with a differentiable forth interpreter.
ArXiv:abs/1605.06640 (2016)
136. Park, K.: Can Convolutional Neural Networks Crack Sudoku Puz-
zles? GitHub (2018)
123

Arabian Journal for Science and Engineering (2026) 51:35–67 65
137. Xu, J.; Zhang, Z.; Friedman, T.; Liang, Y .; Broeck, G.V .: A
semantic loss function for deep learning with symbolic knowl-
edge. In: International Conference on Machine Learning (2017).
https://api.semanticscholar.org/CorpusID:10306523
138. Augustine, E.; Pryor, C.; Dickens, C.; Pujara, J.; Wang,
W.Y .; Getoor, L.: Visual sudoku puzzle classiﬁcation: a suite
of collective neuro-symbolic tasks. In: International Work-
shop on Neural-Symbolic Learning and Reasoning (2022).
https://api.semanticscholar.org/CorpusID:252439935
139. Johnson, J.; Hariharan, B.; Maaten, L.; Hoffman, J.; Fei-Fei, L.;
Zitnick, C.L.; Girshick, R.B.: Inferring and executing programs
for visual reasoning. In: 2017 IEEE International Conference on
Computer Vision (ICCV), 3008–3017 (2017)
140. Coraggio, P .; De Gregorio, M.; Forastiere, M.: Robot navigation
based on neurosymbolic reasoning over landmarks. Int. J. Pattern
Recognit. Artif. Intell. 22(05), 1001–1014 (2008)
141. Staffa, M.; Rossi, S.; De Gregorio, M.; Burattini, E.,et al.: Thresh-
olds tuning of a neuro-symbolic net controlling a behavior-based
robotic system. In: ESANN (2011)
142. Kraetzschmar, G.; Sablatnög, S.; Enderle, S.; Palm, G.: Applica-
tion of neurosymbolic integration for environment modelling in
mobile robots. In: Hybrid Neural Systems, pp. 387–401 (2000).
Springer
143. De Gregorio, M.: An intelligent active video surveillance system
based on the integration of virtual neural sensors and bdi agents.
IEICE Trans. Inf. Syst. 91(7), 1914–1921 (2008)
144. Dong, H.; Mao, J.; Lin, T.; Wang, C.; Li, L.; Zhou, D.: Neural
logic machines. arXiv preprint arXiv:1904.11694 (2019)
145. Ding, M.; Chen, Z.; Du, T.; Luo, P .; Tenenbaum, J.; Gan, C.:
Dynamic visual reasoning by learning differentiable physics mod-
els from video and language. Adv. Neural. Inf. Process. Syst. 34,
887–899 (2021)
146. Mikolov, T.; Chen, K.; Corrado, G.; Dean, J.: Efﬁcient esti-
mation of word representations in vector space. arXiv preprint
arXiv:1301.3781 (2013)
147. Pennington, J.; Socher, R.; Manning, C.D.: Glove: global vectors
for word representation. In: Proceedings of the 2014 Conference
on Empirical Methods in Natural Language Processing (EMNLP),
pp. 1532–1543 (2014)
148. Parisotto, E.; Mohamed, A.-r.; Singh, R.; Li, L.; Zhou, D.;
Kohli, P .: Neuro-symbolic program synthesis. arXiv preprint
arXiv:1611.01855 (2016)
149. Weber, L.; Minervini, P .; Münchmeyer, J.; Leser, U.; Rocktäschel,
T.: Nlprolog: Reasoning with weak uniﬁcation for question
answering in natural language. arXiv preprint arXiv:1906.06187
(2019)
150. Zellers, R.; Holtzman, A.; Peters, M.; Mottaghi, R.; Kemb-
havi, A.; Farhadi, A.; Choi, Y .: Piglet: Language grounding
through neuro-symbolic interaction in a 3d world. arXiv preprint
arXiv:2106.00188 (2021)
151. Sundar, L.K.S.; Muzik, O.; Buvat, I.; Bidaut, L.; Beyer, T.: Poten-
tials and caveats of AI in hybrid imaging. Methods 188, 4–19
(2021)
152. Ultsch, A.: The neuro-data-mine. In: Symposia on Neural Com-
putation (NC’2000), Berlin(2000)
153. Rasheed, Z.; Ma, Y .-K.; Ullah, I.; Al-Khasawneh, M.; Almutairi,
S.S.; Abohashrh, M.: Integrating convolutional neural networks
with attention mechanisms for magnetic resonance imaging-based
classiﬁcation of brain tumors. Bioengineering 11(7), 701 (2024)
154. Ahmed, M.J.; Afridi, U.; Shah, H.A.; Khan, H.; Bhatt, M.W.;
Alwabli, A.; Ullah, I.: Cardioguard: AI-driven ECG authentica-
tion hybrid neural network for predictive health monitoring in
telehealth systems. SLAS Technol. 29(5), 100193 (2024)
155. Ahmad, I.; Zhu, M.; Liu, Z.; Shabaz, M.; Ullah, I.; Tong, M.C.F.;
Sambas, A.; Men, L.; Chen, Y .; Chen, S.: Multi-feature fusion-
based convolutional neural networks for EEG epileptic seizure
prediction in consumer internet of things. IEEE Trans. Consum.
Electron. 70(3), 5631–5643 (2024)
156. Hatzilygeroudis, I.; Prentzas, J.: Neurules: improving the perfor-
mance of symbolic rules. Int. J. Artif. Intell. Tools 9(01), 113–130
(2000)
157. Bologna, G.: A model for single and multiple knowledge based
networks. Artif. Intell. Med. 28(2), 141–163 (2003)
158. Obot, O.U.; Uzoka, F.-M.E.: A framework for application of
neuro-case-rule base hybridization in medical diagnosis. Appl.
Soft Comput. 9(1), 245–253 (2009)
159. Arkin, R.C.: Governing lethal behavior: Embedding ethics in a
hybrid deliberative/reactive robot architecture. In: Proceedings of
the 3rd ACM/IEEE International Conference on Human Robot
Interaction, pp. 121–128 (2008)
160. Morgan, F.E.; Boudreaux, B.; Lohn, A.J.; Ashby, M.; Curriden,
C.; Klima, K.; Grossman, D.: Military Applications of Artiﬁcial
Intelligence. RAND Corporation, Santa Monica (2020)
161. Zonta, T.; Da Costa, C.A.; Rosa Righi, R.; Lima, M.J.; Da
Trindade, E.S.; Li, G.P .: Predictive maintenance in the industry
4.0: a systematic literature review. Comput. Ind. Eng. 150, 106889
(2020)
162. Cummings, M.: Artiﬁcial Intelligence and the Future of Warfare.
Chatham House for the Royal Institute of International Affairs,
London (2017)
163. Scott, B.; Michell, A.: Enhancing situational understanding
through integration of artiﬁcial intelligence in tactical headquar-
ters. Mil. Rev. 102(6), 74–83 (2022)
164. Campbell, L.; Lotmin, A.; DeRico, M.M.; Ray, C.: The use
of artiﬁcial intelligence in military simulations. In: 1997 IEEE
International Conference on Systems, Man, and Cybernetics.
Computational Cybernetics and Simulation, vol. 3, pp. 2607–2612
(1997). IEEE
165. Seraﬁni, L.; Garcez, A.S.: Learning and reasoning with logic
tensor networks. In: Conference of the Italian Association for
Artiﬁcial Intelligence, pp. 334–348 (2016). Springer
166. Zhou, J.; Cui, G.; Hu, S.; Zhang, Z.; Yang, C.; Liu, Z.; Wang, L.;
Li, C.; Sun, M.: Graph neural networks: a review of methods and
applications. AI Open 1, 57–81 (2020)
167. Golovko, V .; Kroshchanka, A.; Kovalev, M.; Taberko, V .; Ivaniuk,
D.: Neuro-symbolic artiﬁcial intelligence: application for control
the quality of product labeling. In: International Conference on
Open Semantic Technologies for Intelligent Systems, pp. 81–101
(2020). Springer
168. Bologna, G.; Hayashi, Y .: Characterization of symbolic rules
embedded in deep DIMLP networks: a challenge to transparency
of deep learning. J. Artif. Intell. Soft Comput. Res. 7(4), 265–286
(2017)
169. Barbosa, R.; Cardoso, D.O.; Carvalho, D.; França, F.: A neuro-
symbolic approach to gps trajectory classiﬁcation. In: Proceedings
of European Symposium on Artiﬁcial Neural Networks, pp. 411–
416 (2017)
170. Grieco, B.P .; Lima, P .M.; De Gregorio, M.; França, F.M.: Pro-
ducing pattern examples from “mental” images. Neurocomputing
73(7–9), 1057–1064 (2010)
171. Sen, P .; Carvalho, B.W.; Riegel, R.; Gray, A.: Neuro-symbolic
inductive logic programming with logical neural networks. In:
Proceedings of the AAAI Conference on Artiﬁcial Intelligence,
vol. 36, pp. 8212–8219 (2022)
172. Bhatia, S.; Kohli, P .; Singh, R.: Neuro-symbolic program corrector
for introductory programming assignments. In: Proceedings of the
40th International Conference on Software Engineering, pp. 60–
70 (2018)
173. Li, Z.; Huang, J.; Naik, M.: Scallop: a language for neurosymbolic
programming. In: Proceedings of the ACM on Programming Lan-
guages 7(PLDI), 1463–1487 (2023)
123

66 Arabian Journal for Science and Engineering (2026) 51:35–67
174. Chen, X.; Liang, C.; Huang, D.; Real, E.; Wang, K.; Pham, H.;
Dong, X.; Luong, T.; Hsieh, C.-J.; Lu, Y ., et al.: Symbolic discov-
ery of optimization algorithms. Adv. Neural. Inf. Process. Syst.
36, 49205–49233 (2023)
175. Mundhenk, T.N.; Landajuela, M.; Glatt, R.; Santiago, C.P .;
Faissol, D.M.; Petersen, B.K.: Symbolic regression via neural-
guided genetic programming population seeding. arXiv preprint
arXiv:2111.00053 (2021)
176. Kabir, R.; Haque, N.; Islam, M.S.,et al.: A comprehensive sur-
vey on visual question answering datasets and algorithms. arXiv
preprint arXiv:2411.11150 (2024)
177. Li, Z.; Stengel-Eskin, E.; Zhang, Y .; Xie, C.; Tran, Q.H.;
V an Durme, B.; Y uille, A.: Calibrating concepts and operations:
towards symbolic reasoning on real images. In: Proceedings of
the IEEE/CVF International Conference on Computer Vision, pp.
14910–14919 (2021)
178. Lecue, F.: On the role of knowledge graphs in explainable ai.
Semantic Web 11(1), 41–51 (2020)
179. Croce, F.; Andriushchenko, M.; Sehwag, V .; Debenedetti, E.;
Flammarion, N.; Chiang, M.; Mittal, P .; Hein, M.: Robustbench:
a standardized adversarial robustness benchmark. arXiv preprint
arXiv:2010.09670 (2020)
180. Natarajan, S.; Mathur, S.; Sidheekh, S.; Stammer, W.; Kersting,
K.: Human-in-the-loop or ai-in-the-loop? automate or collab-
orate? In: Proceedings of the AAAI Conference on Artiﬁcial
Intelligence, vol. 39, pp. 28594–28600 (2025)
181. Marconato, E.; Bontempo, G.; Ficarra, E.; Calderara, S.;
Passerini, A.; Teso, S.: Neuro-symbolic continual learning:
Knowledge, reasoning shortcuts and concept rehearsal. arXiv
preprint arXiv:2302.01242 (2023)
182. V anschoren, J.: Meta-learning: a survey. arXiv preprint
arXiv:1810.03548 (2018)
183. Mehrabi, N.; Morstatter, F.; Saxena, N.; Lerman, K.; Galstyan, A.:
A survey on bias and fairness in machine learning. ACM Ccmput.
Surv. (CSUR) 54(6), 1–35 (2021)
184. Selbst, A.D.; Boyd, D.; Friedler, S.A.; V enkatasubramanian, S.;
V ertesi, J.: Fairness and abstraction in sociotechnical systems. In:
Proceedings of the Conference on Fairness, Accountability, and
Transparency, pp. 59–68 (2019)
185. Almada, M.: Human intervention in automated decision-making:
Toward the construction of contestable systems. In: Proceedings
of the Seventeenth International Conference on Artiﬁcial Intelli-
gence and Law, pp. 2–11 (2019)
186. Morley, J.; Machado, C.C.; Burr, C.; Cowls, J.; Joshi, I.; Taddeo,
M.; Floridi, L.: The ethics of ai in health care: a mapping review.
Social Sci. Med. 260, 113172 (2020)
187. Kairouz, P .; McMahan, H.B.; Avent, B.; Bellet, A.; Bennis, M.;
Bhagoji, A.N.; Bonawitz, K.; Charles, Z.; Cormode, G.; Cum-
mings, R., et al.: Advances and open problems in federated
learning. Found. Trends Mach. Learn. 14(1–2), 1–210 (2021)
188. Raees, M.; Meijerink, I.; Lykourentzou, I.; Khan, V .-J.; Papan-
gelis, K.: From explainable to interactive AI: a literature review
on current trends in human-AI interaction. Int. J. Hum.-Comput.
Stud. 189, 103301 (2024)
189. Saha, S.S.; Sandha, S.S.; Aggarwal, M.; Wang, B.; Han, L.;
Briseno, J.D.G.; Srivastava, M.: Tinyns: platform-aware neu-
rosymbolic auto tiny machine learning. ACM Trans. Embed.
Comput. Syst. (2024). https://doi.org/10.1145/3603171
190. Wan, Z.; Liu, C.-K.; Yang, H.; Raj, R.; Li, C.; Y ou, H.; Fu, Y .;
Wan, C.; Li, S.; Kim, Y .; Samajdar, A.; Lin, Y .C.; Ibrahim, M.;
Rabaey, J.M.; Krishna, T.; Raychowdhury, A.: Towards efﬁcient
neuro-symbolic AI: from workload characterization to hardware
architecture. IEEE Trans. Circuits Syst. Artif. Intell. 1, 53–68
(2024)
191. Yang, H.; Wan, Z.; Raj, R.; Park, J.; Li, Z.; Samajdar, A.;
Raychowdhury, A.; Krishna, T.: Nsﬂow: an end-to-end fpga
framework with scalable dataﬂow architecture for neuro-symbolic
AI. ArXiv:abs/2504.19323 (2025)
192. Johnson, J.; Hariharan, B.; V an Der Maaten, L.; Fei-Fei, L.;
Lawrence Zitnick, C.; Girshick, R.: Clevr: A diagnostic dataset
for compositional language and elementary visual reasoning. In:
Proceedings of the IEEE Conference on Computer Vision and
Pattern Recognition, pp. 2901–2910 (2017)
193. Garrett, C.R.; Chitnis, R.; Holladay, R.; Kim, B.; Silver, T.;
Kaelbling, L.P .; Lozano-Pérez, T.: Integrated task and motion
planning. Ann. Rev. Control Robot. Autonomous Syst. 4(1), 265–
293 (2021)
194. Scott, T.; Zolotas, A.; Xing, Y .: Beliefnet: a neurosym-
bolic model to enhance context based traversability predic-
tions for autonomous agents in complex environments. IOS
Press. https://www.neurosymbolic-ai-journal.com/system/ﬁles/
nai-paper-899.pdf
195. Acharya, K.; V elasquez, A.; Song, H.H.: A survey on symbolic
knowledge distillation of large language models. IEEE Trans.
Artif. Intell. 5(12), 5928–5948 (2024). https://doi.org/10.1109/
TAI.2024.3428519
196. Lu, Q.; Li, R.; Sagheb, E.; Wen, A.; Wang, J.; Wang, L.; Fan, J.W.;
Liu, H.: Explainable diagnosis prediction through neuro-symbolic
integration. arXiv preprint arXiv:2410.01855 (2024)
197. Carter, J.; Nelson, S.; Roberts, E.; Collins, M.; James, C.:
Neuro-symbolic ai for real-time anti-money laundering sys-
tems. Accessed: 2025-11-29 (2025). https://www.researchgate.
net/publication/391185029
198. Sander, J.; Y u, C.-E.J.; Jalaian, B.; Bastian, N.D.: Uncertainty-
quantiﬁed neurosymbolic ai for open set recognition in network
intrusion detection. In: MILCOM 2024 - 2024 IEEE Military
Communications Conference (MILCOM), pp. 13–18 (2024).
doi:10.1109/MILCOM61039.2024.10773953
199. Acharya, K.; Lad, M.; Sun, L.; Song, H.: Neurosymbolic approach
for travel demand prediction: Integrating decision tree rules into
neural networks. In: 2025 International Wireless Communications
and Mobile Computing (IWCMC), pp. 600–605 (2025). IEEE
200. DeLong, L.N.; Gadiya, Y .; Galdi, P .; Fleuriot, J.D.; Domingo-
Fernández, D.: Mars: A neurosymbolic approach for interpretable
drug discovery. arXiv preprint arXiv:2410.05289 (2024)
201. Meghraoui, K.; Racharak, T.; Ait El-Kadi, K.; Bensiali, S.; Sebari,
I.: A new integrated neurosymbolic approach for crop-yield pre-
diction using environmental data and satellite imagery at ﬁeld
scale. Artif. Intell. Geosci. (2025). https://doi.org/10.1016/j.aiig.
2025.100125
202. Baradari, D.; Kosmyna, N.; Petrov, O.; Kaplun, R.; Maes, P .:
Neurochat: A neuroadaptive AI chatbot for customizing learning
experiences. arXiv preprint arXiv:2503.07599 (2025)
203. Huang, S.; Song, P .; George, R.J.; Anandkumar, A.: Leanprogress:
guiding search for neural theorem proving via proof progress pre-
diction. arXiv preprint arXiv:2502.17925 (2025)
204. DeepMind: AI achieves silver-medal standard solving Inter-
national Mathematical Olympiad problems. Accessed 30 May
2025 (2024). https://deepmind.google/discover/blog/ai-solves-
imo-problems-at-silver-medal-level/
205. Liu, X.; Hu, J.; Mwakapesa, D.S.; Nanehkaran, Y .A.; Mao, Y .M.;
Zhang, R.-P .; Chen, Z.: A novel mapreduce-based deep con-
volutional neural network algorithm. J. Intell. Fuzzy Syst. 41,
2603–2615 (2021)
206. Le, Y .; Nanehkaran, Y .A.; Mwakapesa, D.S.; Zhang, R.; Yi, J.;
Mao, Y .-M.: Fp-dcnn: a parallel optimization algorithm for deep
convolutional neural network. J. Supercomput. 78, 3791–3813
(2021)
123

Arabian Journal for Science and Engineering (2026) 51:35–67 67
207. Y u, X.; Zeng, F.; Mwakapesa, D.S.; Nanehkaran, Y .A.; Mao, Y .;
Xu, K.-B.; Chen, Z.: DBWGIE-MR: a density-based clustering
algorithm by using the weighted grid and information entropy
based on mapreduce. J. Intell. Fuzzy Syst. 40, 10781–10796
(2021)
208. Mao, Y .M.; Geng, J.; Mwakapesa, D.S.; Nanehkaran, Y .A.;
Zhang, C.; Deng, X.; Chen, Z.: PFIMD: a parallel mapreduce-
based algorithm for frequent itemset mining. Multimed. Syst. 27,
709–722 (2021)
209. Mao, Y .-M.; Gan, D.; Mwakapesa, D.S.; Nanehkaran, Y .A.; Tao,
T.; Huang, X.: A mapreduce-based k-means clustering algorithm.
J. Supercomput. 78, 5181–5202 (2021)
210. Nanehkaran, Y .A.; Licai, Z.; Chen, J.; Zhongpan, Q.; Xiaofeng,
Y .; Navaei, Y .D.; Einy, S.: Diagnosis of chronic diseases based
on patients’ health records in IOT healthcare using the recom-
mender system. Wireless Communications and Mobile Comput-
ing 2022(1), 5663001 (2022)
123
```
