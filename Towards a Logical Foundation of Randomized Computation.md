---
title: Towards a Logical Foundation of Randomized Computation
author:
  - Melissa Antonelli
source: https://ceur-ws.org/Vol-3615/paper5.pdf
venue: BEWARE 2023
type: Proceedings Article
created: 2025-02-17
tags:
  - themes/bias
  - tech/Ai
  - themes/ethics
pdfORepub: "[[Towards a Logical Foundation of Randomized Computation.pdf]]"
modified: 2026-09-08
---

# Notes

## Full text (extracted from `2PDF/Towards a Logical Foundation of Randomized Computation.pdf`)

*Extracted:* 2026-09-17

```text
Towards a Logical Foundation of Randomized
Computation (Thesis Abstract)⋆
Melissa Antonelli1
1HIIT Helsinki Institute for Information Technology, Pietari Kalmi katu, 5, 00560, Helsinki, Finland.
Abstract
Interactions between logic and computer science have been deeply investigated in the last century,
but, surprisingly, the study of probabilistic computation was only marginally touched by such fruitful
interchanges. The goal of my doctoral project was precisely that of start bridging this gap by developing
logical systems corresponding to specific aspects of randomized computation and, thus, by generalizing
standard achievements to the probabilistic realm. To do so, the key ingredient is the introduction of new,
measure-sensitive quantifiers associated with quantitative interpretations. Concretely, the dissertation
is tripartite. The first part concerns counting complexity and its main result is the proof that classical
counting propositional logic provides a purely logical characterization of Wagner’s hierarchy [1]. In
the second part, which focusses on programming language theory, we present a probabilistic Curry-
Howard correspondence [2] between the intuitionistic version of our counting propositional logic and the
typed probabilistic 𝜆-calculus with counting quantifiers. Finally, we consider the relationship between
arithmetic and computation by introducing a quantitative extension of the language of Peano arithmetic
able to formalize basic results from probability theory. This language is also our starting point to define
randomized bounded arithmetic and, so, to generalize canonical results by Buss [3].
Keywords
Randomized Computation, Logical Foundations of Computer Science, Probability Logic, Reasoning about
Uncertainty
1. Introduction
Historically, determinacy was certainly one of the defining features of standard computational
models: given an algorithm and an input, the sequence of computation steps is uniquely deter-
mined. In the second half of the XX century, this assumption started to be relaxed in different
ways and randomized algorithms were introduced for the first time – where a randomized algo-
rithm is a process which can evolve probabilistically so that, given an input, the computation
it performs may lead to different outcomes, each associated with a certain probability. Such a
more flexible design makes this computational model a very efficient and powerful tool, with
several applications in computer science (CS, for short) and technology.
Starting from this, my Ph.D. dissertation has been motivated by two main considerations. On
BEWARE 2023: Joint Workshop, AIxIA 2023, November 6-9, 2023, Rome, Italy,
⋆
The author thanks her Ph.D. thesis supervisor U. Dal Lago and co-supervisor P. Pistone for their constant guidance
and crucial help: all the results presented here are part of the joint work with them. The author is grateful to
Helsinki Institute for Information Technology - HIIT for supporting her work since 2023. Finally, the author wish
to thank the anonymous reviewers for helpful comments.
/envel⌢pe-⌢penmelissa.antonelli@helsinki.fi (M. Antonelli)
© 2023 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).
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

the one hand, since its early appearance in the 1950s, probabilistic computation has become
ubiquitous in several fast-growing areas of CS and, by now, related, abstract models – as
probabilistic Turing machines (PTM, for short), stochastic automata or randomized 𝜆-calculi
– have been deeply investigated in the literature. On the other, there exist deep and mutual
interactions linking logic and theoretical computer science (TCS, for short), and, in the past, the
development and study of computation theory and models has considerably benefitted from
them. Yet, randomized computation was only marginally touched by such fruitful interchanges
and, so far, it has not found a precise logical counterpart. Such a missing connection looks
even more striking nowadays, due to the increasing pervasiveness of probability in many
relevant fields of information technology, from AI and statistical learning to cryptography,
approximate computing and robotics. The global purpose of my doctoral thesis consisted in
laying the foundation for a uniform approach to bridge the quoted gap. To do so, the key
ingredient is the introduction of a family of new logics, the language of which includes non-
standard quantifiers “measuring” the probability of their argument formula, and associated with
inherently quantitative semantics.
2. The Importance of Being Randomized
As said, randomized algorithms are powerful tools with numerous applications in different
fields and technologies. Generally speaking, these are crucial when dealing with uncertain
information and partial knowledge, namely for all systems acting in realistic contexts – think,
for example, of driverless cars [4] or of computer vision modelling [5]. Notably, in some areas
probabilistic models have become even more than optional; for instance in cryptography, where
secure encryption schemas are probabilistic [6].
On Logical Foundations of Computer Science.The existence of several and deep inter-
actions between logic and TCS is not accidental, but rooted in the intimate correspondence
connecting these disciplines. In fact, even the formal appearance of the science of computing
was essentially motivated by foundational studies in mathematics and logic, that had defined
the context in which this subject took its first steps. Later on, the back and forth between logic
and CS has strongly influenced the development of both and, today, numerous areas of IT – as
programming language theory [2], verification [7] and database theory [8], computational and
descriptive complexity [9, 10], just to quote a few – has effectively benefitted from their mutual
dialogue. As Siekmann wrote, “[i]n many respects, logic provides computer science with both a
unifying foundational framework and a tool for modeling” [11, p. 17]. Indeed, several aspects
of computer science are intrinsically related with logic, as shown by a variety of seminal results,
e.g. [12, 13, 14, 9]. The other side of the coin is the existence of numerous concrete exchanges
between these disciplines: while the growing importance of IT has guided and stimulated
many advances in logic, logical tools have extensive applications in CS and technology – from
software and hardware verification to the modelling of interactive or multi-agent systems, from
the study of relational databases to argumentation theory.

Probabilistic Computation. Probabilistic computational models have been widely investi-
gated in the last few years, and are nowadays pervasive in almost every areas of CS. As seen,
the idea of relaxing the notion of algorithm from purely deterministic to probabilistic appeared
early in the history of modern computability theory. Intuitively, as anticipated, a randomized
algorithm is nothing but an algorithm involving random processes – typically corresponding to
“flipping a coin” – as part of its procedure. While in deterministic computation, for every input,
the algorithm 𝒜produces (at most) one output, in randomized computation, given an input, the
algorithm 𝒜ℛ returns a set of outputs, each associated with a probability:
J𝒜K : N ⇀ N ⇝ J𝒜ℛK : N →DN.
In this way, algorithms have enabled efficient solutions to numerous problems [15], becoming
essential in different areas. As a consequence, several probabilistic (formal) models were
introduced: from PTMs [16, 17] and stochastic automata [18, 19] to probabilsitic 𝜆-calculi [20].
At this point, randomized algorithms and programs are widespread, steering disciplines like
robotics, AI, verification and security coding, computer vision and NLP:
The last decade has witnessed a tremendous growth in the area of randomized
algorithms. During this period, randomized algorithms went from being a tool in
computational number theory to finding widespread applications in many types of
algorithms. Two benefits of randomization have spearheaded this growth: simplicity
and speed. [15, p. ix]
Reasoning About Uncertainty. In particular, the use of randomized models have spread in
discipline involving uncertain domain – that is, in all disciplines realistically interacting with
“the world”. For instance, in agent systems (whether artificial or not) reasoning is processed and
decisions are made on the ground of partial information obtained from the environment and the
background knowledge.1 Clearly, in such contexts, simplifications are needed and “probabilistic
thinking” appears as a formidable tool for decision making and learning processing [21]. These
new, concrete demands also led to the first attempts to analyze probabilistic reasoning in a
formal way and to the introduction of a few logical systems, starting in 1986 with Nilsson’s
pioneering proposal:
Because many artificial intelligence applications require the ability to reason with
uncertain knowledge, it is important to seek appropriate generalizations of logic
from this case. [22, p. 71]
In the following years, new probability logics, inspired by [22], were presented and developed
in the context of modal logic [ 23, 24, 25]. Nowadays, different formal systems to deal with
probabilistic and uncertain reasoning have been defined, even basing on alternative (non-
modal) approaches, for example via non-monotonic and fuzzy logics or due to direct numerical
representations.2
1Probabilistic models become fundamental in AI research from the 1970s-1980s on. For further details on the “main
phases” in the history of this discipline, see e.g. [5].
2A detailed overview of logics for probability can be found e.g. in [21] or in [26, pp. 91ff.].

3. Towards Logical Foundations of Randomized Computation
As anticipated, interchanges between logic and computation are numerous and well-studied. Yet,
in the randomized setting, such a deep correspondence has only been sparsely investigated. One
crucial peculiarity, when switching to probabilistic algorithms, is that, in this case, behavioral
properties, like termination or equivalence, have an inherently quantitative nature, that is a
computation terminates with a given probabilityand a program might simulate a desired function
up to some probability of error – think, for instance, to probabilistic primality tests or learning
algorithms. Then, the central question is:
can such quantitative properties be studied within a logical system?
In my Ph.D. dissertation a positive answer is given, at least for the specific aspects of the
interaction between quantitative logics and randomized computation it focusses on. As we shall
briefly see, the turning point of our approach consists in considering new quantitative logics
able to express probability in a natural way.
3.1. Relating Logic and Randomized Computation
Concretely, we generalized a few standard results linking logic and computation to the proba-
bilistic realm.
Complexity Theory. As it is well-known, classical propositional logic and computational
complexity are strongly connected. Indeed, checking the satisfiability of PL-formulas is the
paradigmatic NP-complete problem [9], while the language of classical tautologies is coNP-
complete. In the early 1970s, Meyer and Stockmeyer also showed that, when switching to
quantified propositional logic (QPL, for short), the full polynomial hierarchy (PH, for short)
can be captured by a single logical system and that each level in it is characterized by the
validity of QPL-formulas (in PNF), with the corresponding number of quantifier alternations.
Nonetheless, when moving to the probabilistic framework, such a plain correspondence seems
lost since no analogous logical counterpart is known to relate in a similar way to the counting
classes and hierarchy, as introduced by Valiant [27] and Wagner [1]:
polynomial hierarchy : QPL ⇐⇒ counting hierarchy : ?
In the first part of the dissertation, a counting propositional system, called CPL, is introduced.
This logic is basically a generalization of PL capable of expressing that a formula is true with a
given probability [28, 29]. Then, CPL is shown to be strongly related to counting computation
and classes, being the probabilistic counterpart of QPL [30, 28, 31]. Indeed, its counting
quantifiers can be naturally seen as “quantitative” versions of standard propositional ones.
Our main result here is the purely logical characterization of Wagner’s hierarchy via complete
problems defined in terms of CPL-formulas.
Programming Language Theory. Traditionally, the Curry-Howard correspondence (CHC,
for short) relates intuitionistic PL and the simply-typed 𝜆-calculus, but in the last fifty years

this correspondence was shown to hold in other and more sophisticated contexts too. Mean-
while, randomized 𝜆-calculi [20] and associated type systems were introduced, sometimes also
guaranteeing desirable forms of termination [32]. Yet, they are not so-to-say “logically oriented”
and no (probabilistic) CHC [2] is known for them:
simply typed 𝜆→ : intuitionistic PL ⇐⇒ randomized 𝜆-calculi : ?
In the second part of the thesis, two new ingredients are introduced to define the first probabilistic
version of the quoted correspondence. On the one hand, we consider the intuitionistic version
of univariate CPL, called iCPL0, and show it able to capture quantitative behavioral properties.
On the other, we define a “counting”-typed randomized 𝜆-calculus. Its untyped part is strongly
inspired by the probabilistic event 𝜆-calculus introduced in [33], while its types are defined
mimicking counting quantifiers. Finally, we establish a (static and dynamic) correspondence in
the style of Curry and Howard between these two systems [34, 31].
Arithmetic and Computation Theory. The theory of (deterministic) computation and
arithmetic are linked by deep results coming from logic and recursion theory – for example,
Gödel’s arithmetization [35] or realizability [36] or the Dialectica interpretation [37]. Indeed,
the language of arithmetic is able to express many interesting properties of algorithms and, due
to the relation between totality (of functions) and termination (of algorithms), several issues
in computation theory can be analyzed in the framework of arithmetic. Also in this context,
when switching to the probabilistic realm, no theory can be found to relate to randomized
computation as Peano Arithmetic (PA, for short) does in the deterministic case:
deterministic computation : PA ⇐⇒ probabilisitic computation : ?
In the third part of the dissertation, we present a quantitative extension of the language of
PA, called MQPA, which allows us to formalize basic results from probability theory that are
not expressible in PA, for example the so-called infinite monkey theorem or the random walk
theorem. This language is also proved to be actually connected to randomized computation as
we establish the first probabilistic version of Gödel’s arithmetization [33], namely it is shown
that any random function can be expressed by a formula of MQPA.
In addition, this language is at the basis of our study of randomized bounded theories [38].
One of the central motivations for the development of bounded arithmetics – i.e., subsystems of
PA the language of which includes functions with specific growth rate together with bounded
quantifiers, and in which induction is (variously) limited – was their connection with compu-
tational complexity. As it is clear that not all computable functions are feasibly computable,
bounded theories become essential to characterize interesting (feasible) complexity classes
in terms of families of arithmetic formulas. Specifically, in 1986 Buss proved that poly-time
computable functions precisely correspond to those functions which are Σ𝑏
1-definable in a
given bounded theory, called S1
2 [3]. Although this fact is very insightful, no similar result was
established in the probabilistic framework:
deterministic classes : BA ⇐⇒ probabilistic classes : ?

Inspired by the language MQPA, in the third part of the thesis we also introduce a randomized
bounded theory, called RS1
2, enabling us to logically capture relevant probabilistic classes, as
BPP [39, 40].
3.2. From Evaluating to Measuring
Counting quantifiers are quantifiers of the form C𝑞
𝑋 or D𝑞
𝑋 and capable of expressing prob-
abilities within a logical language. These quantifiers not only determine the existence of a
satisfying assignment, but rather counthow many those assignments are. In this sense, counting
quantifiers can be seen as a quantitative generalization of standard propositional ones:
(∀𝑋)𝐹, (∃𝑋)𝐹 ⇝ C𝑞
𝑋𝐹, D𝑞
𝑋𝐹.
Intuitively, the QPL-formula (∃𝑋)𝐹 says that there is an interpretation for 𝑋 making 𝐹 true.
On the other hand, the (pseudo-)counting formula C1/2
𝑋 𝐹 expresses that 𝐹 has probability
greater than 1
2 of being true, i.e. that 𝐹 is true for at least one half of all possible interpretations
of 𝑋. Dually, D1/2
𝑋 𝐹 says that the argument formula 𝐹 has probability strictly smaller than 1
2
of being true.
Remarkably such a generalization is made possible by switching from a truth-functional to a
quantitative semantics, in which formulas are no more interpreted as single truth-values but as
measurable sets of models:
J𝐹KQPL ∈{0, 1} ⇝ J𝐹KCPL ⊆2N.
So, while (the truth of) an existentially-quantified formula ofQPL – for instance,(∃𝑋)(∃𝑌 )(𝑋∧
𝑌 ) – gives us information about theexistence of a model for𝑋∧𝑌 , counting-quantified formulas
tell us something about the number of these satisfying valuations. For example, the (pseudo-
)counting formula C1/4
𝑋,𝑌 (𝑋 ∧𝑌 ) says not only that there is a model for 𝑋 ∧𝑌 , but also that at
least one out of four possible interpretations of the argument formula is a satisfying one. It is in
this way that counting logical systems allow us to formally represent and study quantitative
aspects of probabilistic computation in an innovative way.
Notably, our counting propositional logics are natural tools to represent stochastic events in
a straightforward way,3 but, as predictable, their expressive power is still quite limited. This
has led us to the generalization of the notion of counting quantifier and to the definition of the
extended language MQPA, which is nothing but the language of first-order arithmetic endowed
with second-order measure quantifiers and associated with a Borel semantics.
References
[1] K. Wagner, The Complexity of Combinatorial Problems with Succinct Input Representation, Acta Informatica
23 (1986) 325–356.
[2] M. Sorensen, P. Urzyczyn, Lectures on the Curry-Howard Isomorphism, volume 149, Elsevier, 2006.
[3] S. Buss, Bounded Arithmetic, Ph.D. thesis, Princeton University, 1986.
[4] S. Thrun, W. Burgard, D. Fox, Probabilistic Robotics, MIT Press, 2006.
3For further details, see [29].

[5] D. Koller, N. Friedman, Probabilistic Graphical Models: Principles and Techniques, MIT Press, 2009.
[6] S. Goldwasser, S. Micali, Probabilistic Encryption, Journal of Computer and System Sciences 28 (1984) 279–299.
[7] M. Thornton, R. Drechsler, D. Miller, Logic Verification, Springer, 2001, pp. 201–230.
[8] E. Codd, Relational Completeness of Data Base Sublanguages, in: Proc. 6th Courant Computer Science
Symposium, 1972, pp. 65–98.
[9] S. Cook, The Complexity of Theorem-Proving Procedures, in: Proc. Symposium on Theory of Computing
(STOC), 1971, pp. 151–158.
[10] N. Immerman, Descriptive Complexity, Springer, 1999.
[11] J. Siekman, Computational Logic, in: J. Siekmann (Ed.), Handbook of the History of Logic: Computational
Logic, volume 9, Elsavier, 2014, pp. 15–30.
[12] A. Turing, On Computable Numbers, with an Application to the Entscheidungsproblem, in: Proc. London
Mathematical Society, volume 42, 1936, pp. 230–265.
[13] A. Church, S. Kleene, Formal Definitions in the Theory of Ordinal Numbers, Fundamenta Mathematicae 28
(1936) 11–21.
[14] W. Howard, The Formulae-as-Types Notion of Construction, in: J. Seldin, J. Hindley (Eds.), To H.B. Curry:
Essays on Combinatory Logic, Lambda Calculus and Formalism, Academic Press, 1980, pp. 479–490.
[15] R. Motwani, P. Raghavan, Randomized Algorithms, Cambridge University Press, 1995.
[16] E. Santos, Probabilistic Turing Machines and Computability, Proc. American Mathematical Society 22 (1969)
704–710.
[17] J. Gill, Computational Complexity of Probabilistic Turing Machines, in: Proc. Symposium on Theory of
Computing (STOC), 1974, pp. 91–95.
[18] M. O. Rabin, Probabilistic Automata, Information and Computation 6 (1963) 230–245.
[19] R. Segala, A Compositional Trace-Based Semantics for Probabilistic Automata, in: Proc. International
Conference on Concurrency Theory (CONCUR), 1995, pp. 234–248.
[20] N. Saheb-Djaromi, Probabilistic LCF, in: A. Press (Ed.), Proc. International Symposium on Mathematical
Foundations of Computer Science, 1978, pp. 154–165.
[21] J. Pearl, Probabilistic Reasoning in Intelligent Systems. Networks of Plausible Inference, Elsavier, 1988.
[22] N. Nilsson, Probabilistic Logic, Artificial Intelligence 28 (1986) 71–87.
[23] F. Bacchus, Representing and Reasoning with Probabilistic Knowledge, MIT Press, 1990.
[24] R. Fagin, J. Halpern, N. Megiddo, A Logic for Reasoning about Probabilities, Information and Computation 87
(1990) 78–128.
[25] J. Halpern, Reasoning About Uncertainty, MIT Press, 2003.
[26] M. Antonelli, Towards a Logical Foundation of Randomized Computation, Ph.D. thesis, University of Bologna,
Department of Computer Science and Engineering, 2023.
[27] L. Valiant, The Complexity of Computing the Permanent, Theoretical Computer Science 8 (1979) 189–201.
[28] M. Antonelli, U. Dal Lago, P. Pistone, On Counting Propositional Logic and Wagner’s Hierarchy, Theoretical
Computer Science (2023).
[29] M. Antonelli, Two Remarks on Counting Propositional Logic, in: Proc. Workshop on Bias, Risk, Explainability
and the role of Logic and Logic Programming (BEWARE), AIxIA Conference, 2022, pp. 20–32.
[30] M. Antonelli, U. Dal Lago, P. Pistone, On Counting Propositional Logic and Wagner’s Hierarchy, in: Proc.
Italian Conference of Theoretical Computer Science (ICTCS), 2021, pp. 107–121.
[31] M. Antonelli, U. Dal Lago, P. Pistone, Towards Logical Foundations for Probabilistic Computation, Annals of
Pure and Applied Logic (2023).
[32] C. Faggian, S. Ronchi della Rocca, Lambda Calculus and Probabilistic Computation, in: Proc. Symposium on
Logic in Computer Science (LICS), 2019, pp. 1–13.
[33] U. Dal Lago, G. Guerrieri, W. Heijltjes, Decomposing Probabilistic Lambda-Calculi, in: Proc. Foundations of
Software Science and Computation Structures (FoSSaCS), 2020, pp. 136–156.
[34] M. Antonelli, U. Dal Lago, P. Pistone, Curry and Howard Meet Borel, Proc. Symposium on Logic in Computer
Science (LICS) (2022) 1–13.
[35] K. Gödel, Über Formal Unentscheidbare Sätze der Principia Mathematica und Verwandter Systeme, Monatsch.
Math. Phys. 38 (1931) 173–178.
[36] G. Kreisel, Interpretation of Analysis by Means of Constructive Funcionals of Finite Types, in: A. Heyting
(Ed.), Constructivity in Mathematics, North-Holland, 1959, pp. 101–128.
[37] K. Gödel, Über eine Bisher noch nicht Benützte Erweiterung des Finiten Standpunktes, Dialectica 12 (1958)

280–287.
[38] M. Antonelli, U. Dal Lago, D. Davoli, I. Oitavem, P. Pistone, Enumerating Erorr Bounded Polytime Algorithms
Through Arithmetical Theories, in: Proc. Computer Science Logic (CSL), 2024.
[39] M. Antonelli, U. Dal Lago, D. Davoli, I. Oitavem, P. Pistone, Towards a Randomized Bounded Arithmetic, in:
AILA - Book of Abstract, 2022.
[40] M. Antonelli, U. Dal Lago, D. Davoli, I. Oitavem, P. Pistone, Enumerating Erorr Bounded Polytime Algorithms
Through Arithmetical Theories, in: Logic Colloquium 2023 - Book of Abstract, 2023, pp. 45–46.
[41] M. Antonelli, U. Dal Lago, P. Pistone, On Measure Quantifiers in First-Order Arithmetic, in: L. De Mol, M. F.
Weiermann, A., D. Fernández-Duque (Eds.), Proc. Computability in Europe Conference (CiE), 2021, pp. 12–24.
[42] P. Billingsley, Probability and Measure, Wiley, 1995.
A. Outline of the Thesis
The Ph.D. dissertation Towards a Logical Foundation of Randomized Computation [26] was defended in July 2023 at
the University of Bologna, Department of Computer Science and Engineering (DISI). Its main contributions concern
three aspects of the interaction between quantitative logic and probabilistic computation. Accordingly, the thesis is
divided into three parts. Each one is intended to be as self-contained as possible and the opening chapter always
offers a bird’s-eye view of the topic captioned in the corresponding part. It includes a brief historical overview and
global motivations, together with an informal presentation of the results to be later considered.
• In the first part of the dissertation [26, Ch. 2-5], counting propositional logics are introduced and proved
able to define complete (logical) problems for each level of Wagner’s hierarchy. Specifically, the languages of
univariate CPL0 and of multivariate CPL are presented in Chapters 3 and 4, respectively, together with the
associated, quantitative semantics. These systems provide a natural formalism to represent stochastic events
(see [26, Sec. 3.4]) and support a suitable proof-theoretical treatment (see [26, Sec. 3.3, Sec. 4.2]), in the form
of sound and complete sequent calculi. The main result of this part is the logical characterization of CH, as
presented in Chapter 5.
• The second part of the thesis [26, Ch. 6-10] is devoted to our proposal of a probabilistic CHC. In Chapter 7,
the intuitionistic version of counting propositional logic, called iCPL, is defined, while, in Chapter 8, the
computational part of the correspondence, namely a slightly modified version of the probabilistic event
𝜆-calculus by Dal Lago, Guerrieri and Heijltjes [33], is considered. The principal contribution here is the
definition of a probabilistic CHC between a fragment of intuitionistic counting propositional logic and a
counting-typed system able to express the probability of termination. This is presented in Chapter 9. Then,
in Chapter 10, termination properties are further investigated by introducing a related intersection type
system.
• Finally, in the third part of the dissertation [ 26, Ch. 11-13], a more general language, called MQPA, is
introduced together with a quantitative semantics. This language extends that of PA via second-order
measure quantifiers, which are not far from counting ones. In Chapter 12, it is shown that the expressive
power of MQPA is effectively remarkable. Indeed, results from probability theory, which cannot be expressed
in PA, can instead be properly formalized in it. Furthermore, it is proved that any recursive random function
can be represented by a formula of MQPA. In Chapter 13, a new randomized bounded arithmetic theory is
defined and it is established that the class of formulas which are Σ𝑏
1-representable in it is precisely that of
poly-time random functions. Due to this result, an arithmetical characterization of BPP is provided.
All the quoted contributions are part of the joint work with Ugo Dal Lago and Paolo Pistone. Our research about
randomized bounded theory, as presented in Section 14, was developed together with Davide Davoli and Isabel
Oitavem. Crucial results from [26, Part I] have been partially presented in [30, 29, 28, 31]. The main contributions
of [26, Part II] have been published in [34, 31]. The language MQPA and its connections with random functions, as
introduced in [26, Part III], have been presented in [41], while results concerning randomized bounded theories [26,
Ch. 13] have appeared (or will appear) in [39, 40, 38].

B. Counting and Measure-Quantified Logics in a Nutshell
In Section B.1, we introduce a few standard notions from basic probability theory which are needed to define the
semantics of our counting and measure-quantified logics. In Section B.2, we present the language and semantics of
univariate CPL0 and of multivariate CPL, while, in Section B.3, we deal with the language and semantics of the
more expressive language MQPA.
B.1. Basic Probability Theory
In probability theory, an outcome or point 𝜔 is the result of a single execution of an experiment, the sample space
Ω is the set of all possible outcomes, and an event 𝐸 is a subset of Ω. Two events, say 𝐸1 and 𝐸2, are disjoint or
mutually exclusive when they cannot happen at the same time, that is𝐸1 ∩𝐸2 = ∅. A class Fof subsets of Ω is said
to be a 𝜎-field or 𝜎-algebra when (i.) it contains Ω, i.e. Ω ∈F, (ii) it is closed under complementation, i.e. if 𝐸 ∈F,
then 𝐸 ∈F, being 𝐸 the complementation of 𝐸, and (iii) it is closed under countable union (and intersection). The
largest 𝜎-field on Ω is the power class 2Ω, while the smallest one is {∅, Ω}. The 𝜎-field generated by F, 𝜎(F), is the
smallest 𝜎-algebra containing F. A measurable space is a pair (Ω, F), where Fis a 𝜎-algebra over Ω.
In the 1930s, Kolmogorov introduced the notion of probability space, together with the axioms for probability. A
probability measure on a 𝜎-field F, Prob(·), associates each event 𝐸 ∈Fwith a number, Prob(𝐸), so that:
i. for each 𝐸 ∈F, 0 ≤Prob(𝐸) ≤1,
ii. Prob(∅) = 0 and Prob(Ω) = 1,
iii. if 𝐸1, 𝐸2, ...∈Fis a sequence of disjoint events, then Prob
(︀⋃︀∞
𝑘=1 𝐸𝑘
)︀
= ∑︀∞
𝑘=1 Prob(𝐸𝑘).
Two events are(stochastically) independent when the occurrence of one does not affect the probability for the other to
occur. In particular, given two disjoint events, say 𝐸1 and 𝐸2, Prob(𝐸1 ∪𝐸2) = Prob(𝐸1) + Prob(𝐸2), while for
two independent events, say 𝐸′
1 and 𝐸′
2, Prob(𝐸′
1 ∩𝐸′
2) = Prob(𝐸′
1) ·Prob(𝐸′
2). A probability space (Ω, F, Prob)
is a mathematical object that provides a formal model for random processes and is made of:
• a sample space, Ω, which is the set of all possible outcomes,
• a 𝜎-field, F, which is the set of events,
• a probability measure, Prob, which assigns to each event in Fa probability, i.e. a number between 0 and 1
satisfying the so-called Kolmogorov axioms.
In the following, we will mostly focus on a specific probability space such that Ω = 2N, namely the set of all
infinite sequences of random bits (i.e. coin tosses). Each such sequence is denoted as
𝜔 = 𝜔(1)𝜔(2) . . . ,
with 𝜔 ∈Ω, 𝑖 ∈N, and 𝜔(𝑖) ∈{0, 1}. Each sequence 𝜔 can be interpreted as the result of infinitely flipping a coin.
Definition 1 (Cylinder of Rank 𝑛). A cylinder of rank 𝑛 is a set of the form
cyl𝐻 = {𝜔 |𝜔(1), ..., 𝜔(𝑛) ∈𝐻},
with 𝐻 ⊂{0, 1}𝑛.
Observe that when𝐻 = {(𝑢1, ..., 𝑢𝑛)}is a singleton
(︀
for 𝑢1, ..., 𝑢𝑛 ∈{0, 1}
)︀
, an event𝐸 = {𝜔 |𝜔(1), ..., 𝜔(𝑛) =
(𝑢1, ..., 𝑢𝑛)}, such that the first 𝑛 repetitions of the experiment have outcomes 𝑢1, ..., 𝑢𝑛 in sequence, is called a
thin cylinder. We will be particularly interested in thin cylinders in which the only set defining 𝐻 is made of one
element 𝑢𝑖 = 1.
Notation 1. For 𝑖 ∈N, we denote special thin cylinders as follows:
𝐶𝑦𝑙(𝑖) = {𝜔 |𝜔(𝑖) = 1}.
The class of cylinders of all ranks, which is a field [ 42, pp. 27-30], is denoted by C, while 𝜎( C) indicates the
𝜎-algebra generated by C. It is thus possible to define a measure on it. Specifically, we use 𝜇C to denote the unique
probability measure over
(︀
2N, 𝜎( C)
)︀
, such that for any 𝑖 ∈N, 𝜇C
(︀
𝐶𝑦𝑙(𝑖)
)︀
= 1
2 .
Definition 2 (Canonical Cylinder Measure 𝜇C). Given 𝑢 ∈{0, 1}, let 𝑝𝑢 denote the (non-negative and summing
to 1) probability of getting 𝑢. Then, for any cylinder cyl𝐻,
𝜇C(cyl𝐻) =
∑︁
𝐻
𝑝𝑢1 ··· 𝑝𝑢𝑛,
the sum extending over all sequences (𝑢1, . . . , 𝑢𝑛) ∈𝐻.

B.2. On Counting Propositional Logic
The core idea to define counting propositional logics is to extend standard languages bymeasure-sensitive quantifiers
and to consider quantitative semantics in which formulas are no more interpreted as single truth values, but as
measurable sets of satisfying valuations. When dealing with the most intuitive, univariate fragment CPL0, any
formula, say 𝐹, is interpreted as the set J𝐹K ⊆2N made of all maps 𝑓 ∈2N “making 𝐹 true”
(︀
and belonging to the
standard Borel algebra over 2N, B(2N)
)︀
. In particular, atomic propositions are interpreted as special cylinder sets of
the form:
𝐶𝑦𝑙(𝑖) = {𝑓 ∈2N |𝑓(𝑖) = 1},
for 𝑖 ∈N, while non-atomic expressions are interpreted as standard operations of complementation, finite intersec-
tion and union. Since these sets are all measurable, and B(2N) is endowed with a canonical probability measure,
it makes sense to ask whether “𝐹 is true with probability at least q” or “𝐹 is true with probability strictly smaller
than q”. This is formalized by the notion of counting quantifier – i.e. by C𝑞 or D𝑞, for 𝑞 ∈Q ∩[0, 1] –, inspired by
Wagner’s counting operator [1]. Intuitively, the formula C𝑞𝐹 (resp., D𝑞𝐹) expresses that 𝐹 is satisfied by a portion
of assignments greater (resp., strictly smaller) than 𝑞. For example, C1/2𝐹 expresses the fact that 𝐹 is satisfied by at
least half of its valuations. In the more expressive counting propositional logic, CPL, relations between valuations
of different groups of variables can be taken into account. Contextually, the corresponding quantitative semantics is
subtler than that of CPL0 and the interpretation for counting-quantified formulas relies on some technical notions.
Remarkably, in [30, 28, 31], sound and complete proof system(s) for both CPL0 and CPL are introduced.
Remark 1. There is a strong connection between (closed) formulas of CPL0 and (closed) formulas of CPL in which
only one name occurs. Indeed, a translation which preserves validity can be easily defined to pass from ones to the
others [26, Sec. 4.1].
B.2.1. Syntax and Semantics of CPL0
Definition 3 (Formulas of CPL0). Formulas of CPL0 are defined by the grammar below:
𝐹 ::= i |¬𝐹 |𝐹 ∧𝐹 |𝐹 ∨𝐹 |C𝑞𝐹 |D𝑞𝐹,
where 𝑖 ∈N and 𝑞 ∈Q ∩[0, 1].
The definition of the semantics of CPL0 relies on the standard cylinder space
(︀
2N, 𝜎( C), 𝜇C
)︀
.
Definition 4 (Semantics of CPL0). For each formula 𝐹 of CPL0 its interpretation J𝐹K ∈B(2N) is the measurable
set defined as follows:
JiK := 𝐶𝑦𝑙(𝑖)
J¬𝐺K := 2N −J𝐺K
J𝐺 ∧𝐻K := J𝐺K ∩J𝐻K
J𝐺 ∨𝐻K := J𝐺K ∪J𝐻K
JC𝑞𝐺K :=
{︃
2N if 𝜇C
(︀
J𝐺K) ≥𝑞
∅ otherwise
JD𝑞𝐺K :=
{︃
2N if 𝜇C
(︀
J𝐺K) < 𝑞
∅ otherwise.
Example 1. Let us consider C1/2(𝐹 ∨𝐺), where 𝐹 = 0∧¬1 and 𝐺 = ¬0∧1. The measurable sets, J𝐹K and J𝐺K,
have both measure 1
4 and are disjoint. Hence, 𝜇C
(︀
J𝐹 ∨𝐺K
)︀
= 𝜇C
(︀
J𝐹K
)︀
+ 𝜇C
(︀
J𝐺K
)︀
= 1
2 , and JC1/2(𝐹 ∨𝐺)K = 2N.
Observe that counting quantifiers are inter-definable but not dual, in the sense of standard modal operators:
C𝑞𝐹 is not equivalent to ¬D𝑞¬𝐹.
Definition 5. For any formula of CPL0, call it 𝐹, 𝐹 is said to be valid when J𝐹K = 2N and to be invalid when
J𝐹K = ∅.
Remark 2. By combining counting quantifiers it is possible to easily express that a formula𝐹 “is true with precisely
a given probability”, see [29].

B.2.2. Syntax and Semantics of CPL
We now introduce the more expressive fragmentCPL, in which relations between valuations of different groups
of variables can be considered. Its language is made of named atomic formulas and named counting quantifiers.
The corresponding quantitative semantics is subtler than the one for CPL0 and, in particular, the interpretation of
counting-quantified formulas relies on some technical notions.
Notation 2. We use 𝑎, 𝑏, 𝑐...∈Afor names and 𝑋, 𝑌...⊆Afor (countable) sets of names.
Intuitively, named counting quantifiers, C𝑞
𝑎 or D𝑞
𝑎, count the number of valuations of propositional atoms with the
corresponding name, here 𝑎, satisfying the argument formula.
Definition 6 (Formulas of CPL). Formulas of CPL are defined by the grammar below:
𝐹 ::= i𝑎 |¬𝐹 |𝐹 ∧𝐹 |𝐹 ∨𝐹 |C𝑞
𝑎𝐹 |D𝑞
𝑎𝐹,
where 𝑖 ∈N, 𝑎∈A, and 𝑞 ∈Q ∩[0, 1].
A named quantifier binds the occurrences of the name in the argument formula and counts models relative to the
corresponding bounded variable. The intuitive meaning of C𝑞
𝑎𝐹 is that 𝐹 is true in at least 𝑞 valuations of the
variables with name 𝑎.
The interpretation of a formula 𝐹 now depends on the choice of a finite set of names 𝑋 ⊇FN(𝐹) and is a
measurable set J𝐹K𝑋 belonging to the Borel algebra, B
(︀
(2N)𝑋)︀
. To define it formally we need to introduce the
technical notion of 𝑓-projection.
Definition 7 (𝑓-projection). Let 𝑋, 𝑌be two disjoint, finite sets of names, and 𝑓 ∈(2N)𝑋. For all 𝒳⊆ (2N)𝑋∪𝑌 ,
the 𝑓-projection of 𝒳is the set:
Π𝑓 (𝒳) :=
{︀
𝑔 ∈(2N)𝑌 |𝑓 + 𝑔 ∈𝒳
}︀
⊆(2N)𝑌 ,
where
(𝑓 + 𝑔)(𝛼) :=
{︃
𝑓(𝛼) if 𝛼 ∈𝑋
𝑔(𝛼) if 𝛼 ∈𝑌.
Definition 8 (Semantics of CPL). For each formula 𝐹 of CPL and finite set of names such that 𝑋 ⊇FN(𝐹), the
interpretation J𝐹K𝑋 ⊆(2N)𝑋 is defined as follows:
Ji𝑎K𝑋 := {𝑓 |𝑓(𝑎)(𝑖) = 1}
J𝐺 ∧𝐻K𝑋 := J𝐺K𝑋 ∩J𝐻K𝑋
J𝐺 ∨𝐻K𝑋 := J𝐺K𝑋 ∪J𝐻K𝑋
J¬𝐺K𝑋 := (2N)𝑋 −J𝐺K𝑋
JC𝑞
𝑎𝐺K𝑋 :=
{︀
𝑓 |𝜇C
(︀
Π𝑓 (J𝐹K𝑋∪{𝑎})
)︀
≥𝑞
}︀
JD𝑞
𝑎𝐺K𝑋 :=
{︀
𝑓 |𝜇C
(︀
J𝐺K𝑋∪{𝑎})
)︀
< 𝑞
}︀
.
Example 2. Let us consider the formula C1/2
𝑏 C1/2
𝑎 𝐹, where
𝐹 =
(︀
2𝑎 ∧(¬2𝑏 ∧3𝑏)
)︀
∨
(︀
¬2𝑎 ∧(2𝑏 ∧¬3𝑏)
)︀
∨
(︀
(¬2𝑎 ∧3𝑎) ∧3𝑏
)︀
.
The valuations 𝑓 ∈(2N){𝑏}belonging to JC1/2
𝑎 𝐹K{𝑏}are those which can be extended to valuations of all Boolean
variables satisfying 𝐹 in at least half of the cases. Let us list all possible cases:
1. 𝑓(𝑏)(2) = 𝑓(𝑏)(3) = 1. Then, 𝐹 has 1
4 chances of being true, as both ¬2𝑎 and 3𝑎 have to be true
2. 𝑓(𝑏)(2) = 1, 𝑓(𝑏)(3) = 0. Then, 𝐹 has 1
2 chances of being true, as ¬2𝑎 has to be true
3. 𝑓(𝑏)(2) = 0 and 𝑓(𝑏)(3) = 1. Then, 𝐹 has 3
4 chances of being true, as either 2𝑎 or both ¬2𝑎 and 3𝑎 have
to be true
4. 𝑓(𝑏)(2) = 𝑓(𝑏)(3) = 0. Then, 𝐹 has no chance of being true.
Clearly, JC1/2
𝑎 𝐹K{𝑏}only contains the valuations which agree with cases 2. and 3. Therefore,
q
C1/2
𝑏 C1/2
𝑎 𝐹
y
∅= 2N,
i.e. C1/2
𝑏 C1/2
𝑎 𝐹 is valid, since half of the valuations of 𝑏 has at least 1
2 chances of being extended to a model of 𝐹.

B.3. On Measure-Quantified Peano Arithmetic
The standard model N= (N, +, ×) has nothing probabilistic in itself. To obtain a model for MQPA we extend it to
a probability space, obtaining P = (N, +, ×, 𝜎( C), 𝜇C). The grammar for terms of MQPA is standard, whereas the
syntax for formulas is obtained by endowing the language of PA with special flipcoin formulas of the form Flip(𝑡)
and measure-quantified formulas, such as C𝑡/𝑠𝐹 and D𝑡/𝑠𝐹. Specifically, Flip(·) is a special unary predicate with
an intuitive computational meaning: it provides an infinite sequence of independently and randomly distributed bits.
Given a closed term 𝑡, Flip(𝑡) holds if and only if the 𝑛-th tossing returns 1, where 𝑛 denotes 𝑡 + 1.
Definition 9 (Terms and Formulas of MQPA). Let 𝒢be a denumerable set of ground variables, whose elements are
indicated by metavariables such as 𝑥, 𝑦, .... The terms of MQPA, denoted by 𝑡, 𝑠, ..., are defined by the grammar
below:
𝑡 ::= 𝑥 |0 |S(𝑡) |𝑡 + 𝑠 |𝑡 ×𝑠.
The syntax for formulas of MQPA is as follows:
𝐹 ::= Flip(𝑡) |(𝑡 = 𝑠) |¬𝐹 |𝐹 ∨𝐺 |𝐹 ∧𝐺 |∃𝑥.𝐹 |∀𝑥.𝐹 |C𝑡/𝑠𝐹 |D𝑡/𝑠𝐹.
Given an environment𝜉 : 𝒢→ N, the interpretationJ𝑡K𝜉 of a term𝑡 is defined as usual. Instead, the interpretation
of formulas requires a little care, being it inherentlyquantitative; indeed, any formula of MQPA, say 𝐹, is associated
with a measurable set, J𝐹K𝜉 ∈𝜎( C).
Definition 10 (Semantics for Formulas of MQPA). Given a formula 𝐹 and an environment 𝜉, the interpretation of
𝐹 in 𝜉, J𝐹K𝜉 ∈𝜎( C), is the measurable set of sequences inductively defined as follows:
JFlip(𝑡)K𝜉 :=
{︀
𝜔 |𝜔
(︀
J𝑡K𝜉
)︀
= 1
}︀
J(𝑡 = 𝑠)K𝜉 :=
{︃
2N if J𝑡K𝜉 = J𝑠K𝜉
∅ otherwise
J¬𝐺K𝜉 := 2N −J𝐺K𝜉
J𝐺 ∨𝐻K𝜉 := J𝐺K𝜉 ∪J𝐻K𝜉
J𝐺 ∧𝐻K𝜉 := J𝐺K𝜉 ∩J𝐻K𝜉
J∃𝑥.𝐺K𝜉 :=
⋃︁
𝑖∈N
J𝐺K𝜉{𝑥←𝑖}
J∀𝑥.𝐺K𝜉 :=
⋂︁
𝑖∈N
J𝐺K𝜉{𝑥←𝑖}
JC𝑡/𝑠𝐺K𝜉 :=
{︃
2N if J𝑠K𝜉 > 0 and 𝜇C(J𝐺K𝜉) ≥J𝑡K𝜉/J𝑠K𝜉
∅ otherwise
JD𝑡/𝑠𝐺K𝜉 :=
{︃
2N if J𝑠K𝜉 = 0 or 𝜇C(J𝐺K𝜉) < J𝑡K𝜉/J𝑠K𝜉
∅ otherwise
The semantics is well-defined as the sets JFlip(𝑡)K𝜉 and J(𝑡 = 𝑠)K𝜉 are measurable, and measurability is preserved
by all logical and counting operators. A formula of MQPA, say 𝐹, is said to be valid when, for every 𝜉, J𝐹K𝜉 = 2N.
Example 3. The formula 𝐹 = C1/1∃𝑥.Flip(𝑥) states that a true random bit will almost surely be met. This formula
is valid, as the set of constantly 0 sequences forms a singleton of measure 0.
```
