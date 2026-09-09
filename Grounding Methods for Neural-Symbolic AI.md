---
title: Grounding Methods for Neural-Symbolic AI
author: Rodrigo Castellano Ontiveros, Francesco Giannini, Marco Gori, Giuseppe Marra, Michelangelo Diligenti
year: "2025"
Type: Proceedings Article
DOI: 10.24963/ijcai.2025/535
source: https://doi.org/10.24963/ijcai.2025/535
created: 2026-04-24
description: A large class of Neural-Symbolic (NeSy) methods employs a machine learner to process the input entities, while relying on a reasoner based on First-Order Logic to represent and process more complex relationships among the entities. A fundamental role for these methods is played by the process of log
tags:
  - op/acc/pending-review
  - tech/NeSyAI
  - Tech/AI
  - tech/symbolic_reasoning
  - tech/NeSyAI/hybrid
pdfORepub: "[[Grounding Methods for Neural-Symbolic AI.pdf]]"
---
[[Grounding Methods for Neural-Symbolic AI.pdf]]

> **Abstract:** A large class of Neural-Symbolic (NeSy) methods employs a machine learner to process the input entities, while relying on a reasoner based on First-Order Logic to represent and process more complex relationships among the entities. A fundamental role for these methods is played by the process of logic grounding, which determines the relevant substitutions for the logic rules using a (sub)set of entities.

Some NeSy methods use an exhaustive derivation of all possible substitutions, preserving the full expressive power of the logic knowledge, but leading to a combinatorial explosion of the number of ground formulas to consider and, therefore, strongly limiting their scalability. Other methods rely on heuristic-based selective derivations, which are generally more computationally efficient, but lack a justification and provide no guarantees of preserving the information provided to and returned by the reasoner. 

Taking inspiration from multi-hop symbolic reasoning, this paper proposes a parametrized family of grounding methods generalizing classic Backward Chaining. Different selections within this family allow to obtain commonly employed grounding methods as special cases, and to control the trade-off between expressiveness and scalability of the reasoner.

The experimental results show that the selection of the grounding criterion is often as important as the NeSy method itself.
## Full text (extracted from `Grounding Methods for Neural-Symbolic AI.pdf`)

*Source:* `2PDF/Grounding Methods for Neural-Symbolic AI.pdf`  
*Extracted:* 2026-04-24

```text
Grounding Methods for Neural-Symbolic AI
Rodrigo Castellano Ontiveros1 , Francesco Giannini2 , Marco Gori1 ,
Giuseppe Marra3 and Michelangelo Diligenti1
1University of Siena, Italy
2Scuola Normale Superiore, Italy
3KU Leuven, Belgium
{rodrigo.castellano,marco.gori,michelangelo.diligenti}@unisi.it,
francesco.giannini@sns.it, giuseppe.marra@kuleuven.be
Abstract
A large class of Neural-Symbolic (NeSy) methods
employs a machine learner to process the input en-
tities, while relying on a reasoner based on First-
Order Logic to represent and process more com-
plex relationships among the entities. A fundamen-
tal role for these methods is played by the process
of logic grounding, which determines the relevant
substitutions for the logic rules using a (sub)set of
entities. Some NeSy methods use an exhaustive
derivation of all possible substitutions, preserving
the full expressive power of the logic knowledge.
This leads to a combinatorial explosion in the num-
ber of ground formulas to consider and, therefore,
strongly limits their scalability. Other methods rely
on heuristic-based selective derivations, which are
generally more computationally efficient, but lack a
justification and provide no guarantees of preserv-
ing the information provided to and returned by the
reasoner. Taking inspiration from multi-hop sym-
bolic reasoning, this paper proposes a parametrized
family of grounding methods generalizing classic
Backward Chaining. Different selections within
this family allow us to obtain commonly employed
grounding methods as special cases, and to control
the trade-off between expressiveness and scalabil-
ity of the reasoner. The experimental results show
that the selection of the grounding criterion is often
as important as the NeSy method itself.
1 Introduction
Neural-Symbolic (NeSy) methods [d’Avila Garcez et al. ,
2009; Marra et al., 2024] integrate the strengths of neural net-
works and symbolic reasoning, and heavily rely on the pro-
cess of logic grounding, which bridges the semantic gap be-
tween neural representations and symbolic logic. However,
classical grounding techniques in NeSy are impractical, and
they do not take advantage of the generalization capabilities
of NeSy approaches, which can deduce true facts using statis-
tical methods without the need for a classical proof. In fact,
the selection of appropriate grounding represents a significant
challenge for NeSy methodologies. Existing approaches ex-
hibit a dichotomy between exhaustive derivations that main-
tain full expressiveness of logical knowledge but suffer from
scalability issues, and heuristic-based selective derivations
that sacrifice logical coherence for computational efficiency.
Indeed, the employed grounding process is often completely
neglected in the NeSy literature, or relegated to a single sen-
tence in the appendix. This hinders the possibility to repro-
duce, compare, and even fully understand the strengths and
weaknesses of the different methods.
This paper aims to fill this gap by exploring diverse
grounding methods in NeSy AI. We contend that the selec-
tion of a suitable grounding criterion is as pivotal as the de-
sign of the NeSy method itself. To support this claim, we
propose a parameterized generalization of the classic Back-
ward Chaining algorithm, which leverages the well-studied
grounding approaches employed in logic inference, but it can
be relaxed to take advantage of the statistical nature of NeSy
approaches. This allows the control of the trade-off between
scalability and preservation of the logical context. Experi-
mentally, we show the efficacy of the proposed grounding
methodologies across various NeSy methods on the link pre-
diction task in Knowledge Graphs (KGs).
Contributions. The main contributions of this paper are:
(i) we formalize a variety of parametrized grounding methods
for NeSy models. The parametrization controls the trade-off
between scalability, ensuring the applicability of NeSy meth-
ods to large datasets, and expressiveness, hence allowing the
model to take full advantage of the knowledge; (ii) we show
that our results are general and not specific to a single NeSy
method, and we provide an extensive experimental evaluation
to support this claim, (iii) we redefine a large class of popular
NeSy methods within a common message passing schema,
allowing us to share a common implementation and reuse the
same grounding and scaling techniques.
2 Preliminaries
First-Order Logic (FOL). A function-free FOL lan-
guage [Barwise, 1977] is defined by a set of constants (en-
tities) C, variables V and predicates (relations) R. An atomic
formula, or atom, is r(a1, ..., ak) with a1, ..., ak ∈ C ∪ V,
r ∈ Rand k = arity(r). A literal is an atom or its
negation, and each compound FOL formula α is obtained
by recursively combining atomic formulas with connectives
(¬, ∧, ∨, →, ↔) and quantifiers (∀ and ∃). Examples of FOL
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4806

Figure 1: Portion of a GMN. We used the same color for atoms
occurring in the same ground formula. The FOL theory includes the
constants Italy (IT), France (FR), Spain (ES) and Europe (EU), the
predicates LocatedIn (LocIn) and NeighbourOf (NeighOf), and the
rule ∀x∀y∀z LocIn(x, z) ∧ NeighOf (x, y) → LocIn(y, z).
formulas are ∀xNation(x) → ∃yCapitalOf(y, x), express-
ing that “All nations have a capital” or∀x∀y∀zLocIn(x, y)∧
LocIn(y, z) → LocIn(x, z), expressing the transitiveness
of being located in a place. Given a formula α, we define
vars(α) as the set of variables contained in α. For simplic-
ity, in the following sections we will focus on FOL theories,
i.e. sets of formulas, containing only specific formulas called
Horn clauses, which play a fundamental role in computational
logic. A Horn clause is a disjunction of literals with a single
positive literal, which is equivalent to formulas in the form
b1 ∧ . . .∧ bn → h, where the atoms b1, . . . , bn are called
body atoms and the single atom h is called head.
Grounding FOL Theories. Let us fix a FOL language. A
substitution θ is an assignment from variables to domain con-
stants, like θ = {x : Italy, y: Europe}. A ground formulais a
FOL formula where all the variables are constants. For exam-
ple, given α = LocIn(x, y), we can ground it with θ and ob-
tain θα = LocIn(Italy, Europe). The Herbrand Base HB =
{r(c1, ..ck)|r ∈ R, k= arity(r), (c1, ..ck) ∈ Ck} is the set
of all possible ground atoms formed using the predicate and
constant symbols. Given a FOL theory Γ, its Herbrand Uni-
verse is defined as HUΓ = {θα : α ∈ Γ, θis a substitution},
i.e. HUΓ is the set of all possible ground formulas that can
be formed from Γ. The process of constructing the entire
Herbrand Universe is called (full) grounding. In general, we
refer to grounding as the process of constructing a subset of
the Herbrand Universe for a given FOL Theory.
Some methods like Markov Logic Networks (MLNs)
[Richardson and Domingos, 2006], use a graphical represen-
tation of the entire Herbrand Universe (or a subset) called a
Grounded Markov Network (GMN). In the GMN, each node
represents a ground atom, and there is an edge between two
nodes only if the corresponding ground atoms appear together
in at least one grounding of a formula (Figure 1).
Knowledge Graph Embeddings. A Knowledge Graph
(KG) represents knowledge as a graph of entities (nodes)
and relations (edges), with facts as (subject, relation, object)
triples. Knowledge Graph Embeddings (KGEs) [Wang et
al., 2017] map KG entities and relations to low-dimensional
vectors, encoding semantic meaning and statistical depen-
dencies. KGEs enable effective reasoning even with incom-
plete/noisy graphs, for tasks like link prediction and query
answering. Prominent examples include DistMult [Yang et
al., 2015] and ComplEx [Trouillon et al., 2016].
3 Neural-Symbolic Models
Neural networks, while effective at feature processing, are
limited by opaque decision-making, large data require-
ments, and poor generalization. Symbolic AI, though in-
terpretable, struggles with real-world complexity. Neuro-
symbolic (NeSy) models combine their strengths. This paper
focuses on NeSy methods using a neural network to process
FOL constants/predicates, using the GMN topology to define
the reasoner.
The overall structure of these methods, inspired by [Barbi-
ero et al., 2024], is shown in Figure 2, and it is composed of
two high-level components:
1. Atom Processing Layer mapping each ground atom
into an embedding and computing its initial prediction.
2. Reasoning Layersupdating the atoms’ embedding and
score according to the structure imposed by the GMN
associated to the logic theory, and computing a final up-
dated version of the predictions for each ground atom.
3.1 Atom Processing Layer
The class of considered neural-symbolic methods assigns a
numeric representation and an initial output prediction to all
the ground atoms in the HB. This can be formalized as: given
a ground atom α = P(c1, . . . , cn) and Emb(ci) the embed-
ding of ci ∈ C, the atom processing layer outputs the embed-
ding Emb0(α) and the initial output prediction o0(α) as:
Emb0(α) = EncP (Emb(c1), ..., Emb(cn))
o0(α) = Score(Emb0(α))
where EncP is a generic encoding function associated with
the predicate P ∈ R, and Score is a generic scoring
function. Many different representation learning approaches
can be employed to implement and co-train the functions
Enc, Score. While this paper focuses on KGEs and their
scoring functions, the approach can be trivially applied to pat-
tern recognition problems using neural networks.
3.2 Reasoning Layers
The reasoning layers take the outputs of the atom processing
layer and provide an updated representation (both as embed-
ding and prediction) for each ground atom in the head of the
rules. Finally, it outputs the predictions for all atoms. In the
following, we indicate the set of rules of a FOL theory having
an atom h as head in the considered FOL grounding asR(h).
The reasoner can be seen as the unfolding network of a mes-
sage passing process [Gilmer et al., 2017 ] over the GMN,
where messages flow from atoms appearing in the body of a
ground formula to the atom in the head of the same ground
formula. Below, we provide the message passing equations
for some of the methods tested in this paper.
The messages flow from an atom node b in the body of the
j-th formula rj to the atom node h in the head of the same
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4807

Figure 2: In the considered NeSy models an atom processor takes as input the representation of the constants and compute an embedding and
an initial prediction of the atoms. The representations and predictions are refined via message passing, thus performing the reasoning process.
ground formula as:
Embj(h) = Fj(Mne(h,1)→h, ..., Mne(h,dj)→h)
oj(h) = Gj(Mne(h,1)→h, ..., Mne(h,dj)→h)
where Mj
b→h is the message defining the different neural-
symbolic methods, Fj, Gj are generic functions aggregating
back the encoded representation and the output of a node,
ne(h, 1), . . . , ne(h, dj) are the neighbours of node h for the
j-th rule, i.e. the set of body atoms associated to atom h for
the rule rj, with dj = |ne(h)| the number of atoms occurring
in the body of the j-th rule rj.
The embedding of an atom node h is updated by aggre-
gating the representation for all the rules having atom h as
head: Emb(h) = Ae
rj∈R(h)
Embj(h), where Ae is an ag-
gregation operator like sum, mean or max. Other meth-
ods instead aggregate directly over the outputs of a node:
o(h) = Ao
rj∈R(h)
oj(h), where Ao can be any aggregation op-
erator, even if most methods set it as a disjunctive operator,
like a max, as shown below.
Relational Reasoning Networks (R2N). R2N [Marra et
al., 2025 ] propagates the embeddings as representations of
the atoms, using the following message passing schema:
Mb→h = Emb(b)
Embj(h) = MLP e
j (Mne(h,1)→h, ..., Mne(h,dj)→h)
Emb(h) =
X
rj∈R(h)
Embj(h)
o(h) = MLP o(Emb(h))
where the embeddings are initialized using Emb0, and
MLP e
j , MLPo are multi-layer perceptrons (MLP) process-
ing the embeddings and computing the outputs, respectively.
Logic Tensor Networks (LTN). LTN [Badreddine et al. ,
2022] and Semantic Based Regularization (SBR)[Diligenti et
al., 2017] aggregate the predictions of the body atoms of the
j-th rule using a selected t-norm and enforce the consistency
of the predictions with the logic rule. These methods were
limited to unary predicates in the original papers, but here we
propose a relational extension based on message passing:
Mb→h = o(b)
oj(h) = t−norm(Mne(h,1)→h, . . . , Mne(h,dj)→h)
o(h) = max
rj∈R(h)
oj(h)
where o(α) is initialized using o0(α) and the original formu-
lation was running a single propagation step.
Deep Concept Reasoners (DCR). DCR [Barbiero et al.,
2023] builds a formula from a set of candidate atoms before
computing the output of a formula using a t-norm:
Mb→h = Ψ j(Emb0(b), Φj(Emb0(b), o(b)))
oj(h) = t−norm
 
Mne(h,1)→h, . . . , Mne(h,dj)→h

o(h) = max
rj∈R(h)
oj(h)
where oj(α) is initialized using o0
j(α), and the functions
Φj : Rn+1 → [0, 1] and Ψj : Rn+1 → [0, 1], assuming
Emb0(α) ∈ Rn, process the embedded representation of
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4808

Figure 3: Illustration of some accepted/rejected proofs for different
queries with respect to w, d(BCw,d) parameters.
each atom in each rule j, to compute its polarity and rele-
vance values, respectively, to get a learned Horn Clause. The
process can possibly be iterated, even if the original formula-
tion is defined for a single step of propagation.
4 Grounding Methods
Logical reasoning is often used as a form of theorem prov-
ing [Loveland, 2016] in computational logic. An example is
query answering in Prolog, where the answer to a query is
computed by searching for supporting facts given the set of
rules of the program. Hence, proving can be cast to a search
over the GMN, looking for subtrees (i.e., proofs) that con-
nect the query to a set of supporting known facts. The known
facts in a logic theory are typically much smaller than the HB.
Classic Backward Chaining in Prolog considers unknown
facts as possibly provable, and recursively builds a sub-proof
for them if they are the head of a logic rule. While this pro-
cess is effective in finding a formal proof for a query given
the available known facts, it can be very time-consuming. A
commonly used strategy consists in fixing a maximum depth
for the backward search, thus admitting to find only proofs
within a maximum number of reasoning steps.
In NeSy, the logic facts can be neither true nor false, as they
are assigned a score (e.g. a probability of being true) by the
corresponding input layer. Therefore, it would be limiting to
only consider known true facts in the proving process. Many
other facts can provide uncertain information (i.e. context)
to predict a query and should be considered. Unfortunately,
the size of the portion of the ground network relevant to the
query may grow exponentially. However, such a limitation
also introduces a new opportunity. Since NeSy models can
score any fact in the knowledge base, one does not necessar-
ily need to search the supporting known facts, as the scored
facts at shallow depths in a proof can provide enough con-
text for the learning to happen at a statistical level. Neverthe-
less, the majority of existing NeSy models completely neglect
such opportunity, requiring very deep proving processes and
resulting in intractable methods for inference.
4.1 Parameterized Backward Chaining Grounder
The discussed limitations of classical Backward Chaining for
NeSy motivate a novel definition of a flexible parameterized
class of Backward Chaining grounders, which may take ad-
vantage of the generalization capabilities of NeSy methods
over partially proved trees. A grounder in this parametrized
class is defined as BCw,d, where w, d∈ N are referred to as
the width and depth of the grounder, respectively. The width
w determines the maximum number of atoms in the body of
each ground rule that is allowed to not be in the training data
and, in turn, to be proved as sub-goals. The depth d con-
trols the maximum depth that can be achieved by any proof
for any query passing through its sub-goals. If the number
of unknown ground atoms is bigger than w in any ground
rule, the proof is immediately discarded even if more depth
is allowed. Moreover, once the proof has been built by the
grounder, we allow two options: i) to discard the proof if it
contains unknown atoms (as done by Backward Chaining),
ii) to accept the proof by using the scores of the unknown
ground atom. We denote these grounders allowing uncertain
atoms as BCu
w,d. For simplicity, if not stated differently, we
will assume option i). When using option i),BC0,1 ≡ BC1,1,
so we will use BC0,1 in the rest of the paper.
To illustrate the effects of depths and widths, Figure 3 com-
pares the acceptance of diverse proofs across different pa-
rameter values. Section 5 discusses the experimental results
for different versions of BCw,d. Here below, we show how
BCw,d subsumes as special cases grounding techniques com-
monly used in the literature.
Backward Chaining Grounder(w = ∞, d= ∞). Back-
ward Chaining is an inference strategy used in logic program-
ming and automated theorem provers to efficiently prove un-
known facts. Given a query to prove, it searches for a rule,
whose head atom matches the query. If some atom in the
body of the rule is not in the training data, it becomes a new
sub-goal that needs to be proven. The process is repeated re-
cursively, until the query is proved with an associated proof
tree. Notice that, for w = d = ∞ we mean w = B, being B
the maximum amount of atoms in the body of all the rules.
This is the grounding strategy employed by DeepProbLog
[Manhaeve et al., 2018 ], but its application is unfeasible at
the scale of the learning tasks considered in this paper.
Backward Chaining Grounder with limited depth(w =
∞, d= n). In practical settings, the growth of the admis-
sible proofs is limited, as often done in logic programming.
This can be accomplished by setting d = n, where n > 0
determines the maximum depth of the proofs.
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4809

Known Body Grounder(w = 0, d= 1). Several popular
NeSy models, like e.g. ExpressGNN [Zhang et al., 2020] and
RNNLOGIC [Qu et al., 2020], accept a grounding only if all
body atoms are known facts, and recursion is limited to depth
1. Therefore, these approaches are equivalent to BC0,1.
Full Grounder(w = ∞, d= 1). Full grounding of a FOL
theory Γ involves generating theHUΓ, and it is used by mod-
els like LTN, SBR or MLNs. This grounder assumes option
ii) for proofs, i.e. proofs are accepted even with unknown
ground atoms, and thus it is denoted as BCu
∞,1. Roughly, the
Full Grounder considers each atom in the HB as a possible
query. Hence, all possible ground atoms are represented in
the graph, often including irrelevant information, but at the
same time ensuring that all the required information needed
to perform a correct inference could be recovered.
Complexity Analysis. The performances of BCw,d for
NeSy applications are bound by two conflicting effects. On
one hand, a grounder should be able to find the proofs needed
to prove the queries. In this regard, increasing the width and
the depth will result in extending the number of admissible
proofs, thus increasing the number of provable queries.
Proposition 1. The set of facts that are provable via BCw,d
is a subset of the provable facts viaBCw,d+1 and of the prov-
able facts via BCw+1,d.
Proof. The proof trivially follows by observing that the set
of buildable proofs in BCw,d is monotone w.r.t. w and d.
Indeed, any proof with maximum widthw (or depth d) is also
a proof with maximum width w + 1 (or depth d + 1).
However, a grounder should not instantiate more nodes
than needed, as this may affect the generalization capabili-
ties, as stated by the following theorem.
Theorem 1. [Scarselli et al., 2018 ] The Vap-
nik–Chervonenkis dimension (VCD) of the function ϕ com-
puted by a GNN with sigmoidal outputs on the domain of
graphs with up toN nodes satisfies: V CD(ϕ) = O(p2·N2) ,
where p is the number of parameters of the GNN.
The Vapnik–Chervonenkis theory states that the general-
ization error grows as the square root of the V CD, there-
fore the error bound grows linearly with the graph size. The
number of nodes of the underlying reasoning graph built by
BCw,d increases as O(Gdwd−1m), where G is the number of
groundings with at most w atoms not in the known KG, and
m is the maximum number of body atoms within any rule.
For instance, if the rule with the longest body is a chain in the
form of p(x1, x2) ∧ . . .∧ p(xn−1, xn) → p(x1, xn) with n
representing the number of variables, the number of ground-
ings grows as: G ∝ Cmin(w,n−2) for a single reasoning step,
where C is the number of constants, and the overall ground
network size grows asO(Cmin(w,n−2)·dwd−1m). Theorem 1
shows that the generalization error is bound to grow linearly
with the size of the grounded network. Higher values for w
or d lead to an increase in the size of the GMN, therefore it
is fundamental for the success of the NeSy approach to se-
lect values for w, dsuch that the logical context is preserved,
while the generalization capabilities of the GNN are not hin-
dered.
Dataset
#Entities #Relations #Facts #Degree #Rules
Countries S1 272 3 1,110 4.28 1
Countries S2 272 4 1,062 4.35 2
Countries S3 272 4 978 4.35 3
Kinship 104 25 28,356 272.7 48
WN18RR 40,943 18 93,003 2.3 17
FB15k-237 14505 237 310079 21.4 500
Table 1: Basic statistics for the employed datasets.
5 Experiments
Several experiments have been performed on KG link predic-
tion to compare the effectiveness of the grounders.1
Datasets. The Countries [Bouchard et al., 2015 ], Kinship
[Kok and Domingos, 2007], WN18RR [Dettmers et al., 2018]
and FB15k-237 [Dou et al., 2021] datasets are used to capture
diverse sizes and complexities. Countries is split into three
tasks S{1,2,3} of increasing complexity, predicting country
location based on regions and neighborhoods. Kinship repre-
sents familial relationships. Dataset statistics are in Section 5.
Rules. The rules associated with the Countries dataset
are R1 = LocIn(x, w) ∧ LocIn(w, z) → LocIn(x, z),
R2 = NeighOf (x, y) ∧ LocIn(y, z) → LocIn(x, z) and
R3 = NeighOf (x, y) ∧ NeighOf (y, k) ∧ LocIn(k, z) →
LocIn(x, z), where LocIn refers to the predicate Locate-
dIn and NeighOf refers to NeighbourOf. The task S1 takes
R1, S2 takes R1, R2, and S3 all of them. The Countries_abl
dataset is based only on R2. Rules for the remaining datasets
were extracted using AMIE [Galárraga et al., 2013], selecting
the top rules based on confidence. The number of selected
rules per dataset is shown in Section 5.
Hyperparameters. The KGE uses a fixed embedding size
of 100, with overall 1000 head and tail corruptions for
WN18RR. Adam optimizer (10 −2 learning rate) and binary
cross-entropy loss were used over 100 epochs.
Models. ComplEx is used as the KGE baseline and as the
input layer for NeSy methods to enable a reasoning abla-
tion study. The KGE baseline is compared with NeSy mod-
els of varying characteristics: R2N, which is highly expres-
sive but less interpretable as it learns rules over groups of
atoms, excels in complex, loosely formalized reasoning but
risks overfitting when flexibility is unnecessary. SBR, less
expressive but highly interpretable, performs best in simpler,
well-formalized tasks as it strictly applies logic rules. DCR
serves as a middle ground between these two approaches.
Metrics. For the evaluation, we use Mean Reciprocal Rank
(MRR) and Hits@N metrics. All metric evaluations have
been averaged over five runs for the countries dataset.
5.1 Experimental Results
The first experiment serves as a proof of concept using the
Countries_abl dataset. Three splits (AS1, AS2, AS3) are gen-
erated by ablating facts from the original dataset. The splits
are designed with queries requiring one, two, and three rea-
soning steps, respectively, based on consecutive applications
1https://github.com/rodrigo-castellano/Grounding-Methods
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4810

Figure 4: MRR results for different methods using BC1,d with different depths for the Countries_abl datasets AS1, AS2, AS3.
Figure 5: Results for the studied NeSy models andBCw,d grounders for Countries S2,S3 (S1 omitted as it is perfectly solved by all methods).
of the rule LocIn(x, w) ∧LocIn(w, z) → LocIn(x, z). The
BC0,1 grounder is sufficient to solve the simple one-hop rea-
soning task defined by AS1, whereas BC1,2 or BC1,3 are re-
quired to provide good MRR performances inAS2, as shown
in Figure 4. Finally, BC1,3 is the only grounder capable of
solving AS3 with high MRR with all methods. This is con-
sistent with our expectations, as the grounding depth defines
the number of hops preserved in the context of a query.
The results for the Country dataset are presented in Fig-
ure 5, where the baseline is placed asd = 0 (this is consistent
with the model definitions as the baseline is the model out-
put if no message passing of the reasoner is performed on
top of the input atom processing layer). The task S1 is quite
simple so that all methods including the baseline are able to
fully solve it with MRR = 1, therefore it is omitted in the
plots. For S2, all NeSy methods outperform the baseline,
with depth 1 (BC w,1) sufficient for strong performance, and
higher depths plateauing. Regarding the more complex rea-
soning required by the S3 task, we observed that R2N tends
to overfit for this dataset in the tested configuration. All other
NeSy methods provide a large improvement over the base-
line. Optimal results are achieved at either depth 2 or 3, which
is indeed the number of reasoning hops required to solve the
task. Figure 6 compares the NeSy methods against the base-
line when using the Full grounder for the S1,S2,S3 tasks. The
performances of the Full grounder are, in general, not im-
proving over the BCw,d grounders in Figure 5, with actually
smaller average gains over the baseline. The Full grounder
tends to ground many unnecessary atoms with respect to the
focused BCw,d grounders, and this negatively affects model
generalization (as stated by Theorem 1). The results for the
WN18RR and Kinship are presented in Table 2, where we re-
port only the grounders that could be applied in less than 10h
Figure 6: MRR results for the Country datasets and the Full
grounder using different NeSy methods and the baseline.
of computation on our workstation (12 core i7 CPU, 64GB
RAM, OS Linux). For example, the application of the Full
grounder is unfeasible for WN18RR or Kinship.
MRR gains over the baseline of approximately 9%, and 3%
for Kinship, and WN18RR, respectively. As shown by the in-
ference times in Table 2, increasing the depth of the grounder
in the larger datasets strongly impacts the required inference
times. In practice, any grounder with a depth d > 2 would
be very impractical to use for large KGs. Therefore we lim-
ited the experiments to BC0,1 and BC1,2. We observed gen-
erally improved results are obtained as the depth increases
from d = 1 to d = 2 to retain enough information to improve
the classification. However, the statistical nature of NeSy
tasks makes it possible to get competitive performances even
when limited to BC0,1. For instance, in the Kinship dataset
DCR works very well already at depth 1, even if R2N and
SBR can provide slightly improved results at depth 2. In the
WN18RR dataset, BC0,1 already provides significant gains
over the baseline, even ifBC1,2 provides the best results both
for DCR and SBR. These differences are also found in larger
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4811

Model Grounder MRR Hits@1 Hits@3 Hits@10 Train Time(s) Test Time(s)
Kinship
DCR BC0,1 90.1 84.1 95.9 97.0 16479.6 7658.7
BC1,2 90.1 84.1 95.9 97.0 16295.2 7517.4
R2N BC0,1 94.0 92.1 95.6 96.5 9573.3 6616.2
BC1,2 91.8 87.1 96.4 97.4 48808.8 28249.2
SBR BC0,1 86.9 78.0 95.6 97.1 9066.8 6208.7
BC1,2 87.7 79.1 96.0 97.3 43354.7 27447.9
ComplEx - 85.9 79.2 92.2 94.5 773.3 284.9
WN18RR
DCR BC0,1 44.2 42.2 44.8 47.6 26133.3 2337.9
BC1,2 45.6 42.9 47.1 50.2 74626.7 6944.2
R2N BC0,1 44.2 42.3 44.6 47.3 20613.7 2183.4
BC1,2 44.1 41.4 45.4 48.1 72213.3 7353.4
SBR BC0,1 44.0 42.3 44.2 46.6 21940.5 1909.8
BC1,2 44.7 42.5 45.2 48.2 67851.6 6666.0
ComplEx - 42.7 40.8 42.9 45.9 1079.2 138.7
Table 2: Results for different NeSy methods and grounders for the
Kinship and WN18RR datasets compared against the baseline.
Grounder MRR Hits@1 Hits@3 Hits@10
ComplEx - 25.9 16.3 29.2 45.2
RNNLogic(emb.) BC0,1 34.4 25.2 38.0 53.0
R2N BC0,1 34.7 25.4 38.2 53.1
Table 3: MRR, Hits@N metrics on the FB15k-237 dataset.
datasets. For WN18RR, moving from BC0,1 to BC1,2 with
the DCR model improved the MRR metric by 1.6 points, but
increased training and inference times by a 3x factor. This
observation underscores the critical importance of efficient
and effective grounding techniques for scaling NeSy methods
to larger real-world KGs. Results for the larger FB15k-237
dataset are provided in Section 5.1, where the computational
constraints limited experiments to BC0,1, which still showed
substantial improvements over the baseline for R2N. We did
not add SBR and DCR to the table as the available rules were
not covering enough atoms to provide a fair comparison.
6 Related Work
Full Groundings Approaches. A large class of NeSy mod-
els was defined over a full grounding approach, this includes
SBR [Diligenti et al., 2017], LTN [Badreddine et al., 2022],
and Relational Neural Machines [Marra et al., 2020 ]. The
main problem with this grounding method is its lack of scal-
ability, as shown in the experimental section.
Theorem proving approaches. Automatically answering a
query (i.e. proving a theorem) given a set of definite clauses
is at the core of logic programming [Clocksin and Mellish,
2012]. When proving a fact, only a portion of the GMN
is relevant, thus a full grounding is usually not necessary.
Standard techniques to avoid the full grounding includeBack-
ward Chaining [Kapoor and Bahl, 2016] and Forward Chain-
ing [Al-Ajlan, 2015 ] or a mix of the two [Mumick and Pi-
rahesh, 1994]. Since known facts are in general sparse over
the HB, the relevant portion of the Markov network is much
smaller than the full GMN obtained by grounding the rules
over the entire domain. A large class of NeSy systems is
based on theorem proving, this class includes systems ex-
ploiting a Prolog engine like DeepProbLog [Manhaeve et al.,
2018], DeepStochLog [Winters et al., 2022 ], an ASP en-
gine [Shakarian et al., 2023] or Datalog (e.g. LRNN [Sourek
et al., 2018]). However, the exact proving approach does not
allow the methods to scale beyond small inference problems.
Therefore, some methods try to further limit the graph size.
For example, DPLA* [Manhaeve et al., 2021] uses an A* ap-
proach to select the most promising portions of the GMN.
Heuristics-based approaches. The most common ap-
proach used in the literature is to rely on some ad-hoc heuris-
tics to make grounding tractable. However, it did not emerge
in the literature a clear understanding of the trade-off be-
tween performance and computing time. RNNLogic [Qu et
al., 2020 ] generates logic rules and then scores the query
triplets using the grounding paths in the training knowledge.
This makes the model account for the grounded rules where
all body atoms are true in the training facts, which is the spe-
cial case where Backward Chaining is limited to depth 1.Dis-
criminative Gaifman Models [Niepert, 2016] considers local
neighbourhoods of a KG as features to predict queries. The
local neighbourhoods can be seen as a generalization of a
Horn clause, representing a chain of facts in the knowledge
that imply the query. Similarly to RNN Logic, this considers
only the grounded rules where all body atoms are true in the
training facts. ExpressGNN [Zhang et al., 2020] operates di-
rectly on the knowledge graph rather than the extensive GMN
grounding graph. This is similar to the approach of UniKER
[Cheng et al., 2021], which focuses on instantiating rules only
with the training triples in the knowledge graph but iteratively
enriching the training data with new facts derived using for-
ward chaining. KALE [Guo et al., 2016] includes groundings
where at least one atom is true in the training data, and uses a
full grounding approach for the other variables. RUGE [Guo
et al., 2018 ] considers a grounding when the triples in the
rule’s body are observed in the training data, and the head
triple is not.
7 Conclusions and Future Work
This paper studies the effect of different grounding schemas
on the predictive accuracy of NeSy methods. The main
contributions of the work are in the definition of new
parametrized grounding approaches, tailored to NeSy meth-
ods, and in the extensive experimental comparison of these
grounders, offering insights into the trade-offs between
grounding depth, model performance, and computational ef-
ficiency. The results on link prediction on KGs show that
increasing the depth of the parameterized grounder enhances
performance in complex reasoning tasks, but the statistical
nature of NeSy allows preserving a good prediction accuracy
even using shallow and efficient grounders. This contribution
is not only methodological but also practical, highlighting the
critical role of the grounding schema in bridging the gap be-
tween symbolic reasoning and neural learning.
This study is limited to static grounders without any
feedback from the NeSy method, which is the most used
approach. In future work, we plan to explore dynamic
grounders, which iteratively exploit the predictions of the
learner to dynamically incorporate new atoms into the set of
known facts. This could lead to the definition of parametric
grounders which can be trained end-to-end with the learner.
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4812

Ethical Statement
There are no ethical issues.
Acknowledgments
This work has been partially supported by the project
PNRR M4C2 “FAIR - Future Artificial Intelligence Re-
search” - Spoke 1 “Human-centered AI” , code PE0000013,
CUP E53C22001610006. This work was also supported
by the EU Framework Program for Research and Innova-
tion Horizon under the Grant Agreement No 101073307
(MSCA-DN LeMuR). This work has been partially supported
by the project “CONSTR: a COllectionless-based Neuro-
Symbolic Theory for learning and Reasoning”, PARTENAR-
IATO ESTESO “Future Artificial Intelligence Research -
FAIR”, SPOKE 1 “Human-Centered AI” Università di Pisa,
“NextGenerationEU”, CUP I53C22001380006.
References
[Al-Ajlan, 2015] Ajlan Al-Ajlan. The comparison between
forward and backward chaining. International Journal of
Machine Learning and Computing, 5(2):106, 2015.
[Badreddine et al., 2022] Samy Badreddine, Artur d’Avila
Garcez, Luciano Serafini, and Michael Spranger. Logic
tensor networks. Artificial Intelligence, 303:103649, 2022.
[Barbiero et al., 2023] Pietro Barbiero, Gabriele Ciravegna,
Francesco Giannini, Mateo Espinosa Zarlenga, Lu-
cie Charlotte Magister, Alberto Tonda, Pietro Lió, Fred-
eric Precioso, Mateja Jamnik, and Giuseppe Marra. In-
terpretable neural-symbolic concept reasoning. In ICML,
pages 1801–1825, 2023.
[Barbiero et al., 2024] Pietro Barbiero, Francesco Gian-
nini, Gabriele Ciravegna, Michelangelo Diligenti, and
Giuseppe Marra. Relational concept bottleneck mod-
els. Advances in Neural Information Processing Systems,
37:77663–77685, 2024.
[Barwise, 1977] Jon Barwise. An introduction to first-order
logic. In Studies in Logic and the Foundations of Mathe-
matics, volume 90, pages 5–46. Elsevier, 1977.
[Bouchard et al., 2015] Guillaume Bouchard, S. Singh, and
Theo Trouillon. On approximate reasoning capabilities of
low-rank vector spaces. In AAAI Spring Symposia, 2015.
[Cheng et al., 2021] Kewei Cheng, Ziqing Yang, Ming
Zhang, and Yizhou Sun. Uniker: A unified framework for
combining embedding and definite horn rule reasoning for
knowledge graph inference. In Proceedings of the 2021
Conference on Empirical Methods in Natural Language
Processing, pages 9753–9771, 2021.
[Clocksin and Mellish, 2012] William F Clocksin and
Christopher S Mellish. Programming in Prolog: Using
the ISO standard. Springer Science & Business Media,
2012.
[Dettmers et al., 2018] Tim Dettmers, Pasquale Minervini,
Pontus Stenetorp, and Sebastian Riedel. Convolutional 2d
knowledge graph embeddings. In Proceedings of the AAAI
conference, 2018.
[Diligenti et al., 2017] Michelangelo Diligenti, Marco Gori,
and Claudio Sacca. Semantic-based regularization for
learning and inference. Artificial Intelligence, 244:143–
165, 2017.
[Dou et al., 2021] Jiaheng Dou, Bing Tian, Yong Zhang, and
Chunxiao Xing. A novel embedding model for knowl-
edge graph completion based on multi-task learning. In
Database Systems for Advanced Applications: 26th In-
ternational Conference, DASFAA 2021, Taipei, Taiwan,
April 11–14, 2021, Proceedings, Part I 26, pages 240–255.
Springer, 2021.
[d’Avila Garcez et al., 2009] Artur S d’Avila Garcez, Luís C
Lamb, and Dov M Gabbay. Neural-symbolic learning sys-
tems. Springer, 2009.
[Gilmer et al., 2017] Justin Gilmer, Samuel S Schoenholz,
Patrick F Riley, Oriol Vinyals, and George E Dahl. Neu-
ral message passing for quantum chemistry. In Proceed-
ingsICML. PMLR, 2017.
[Guo et al., 2016] Shu Guo, Quan Wang, Lihong Wang, Bin
Wang, and Li Guo. Jointly embedding knowledge graphs
and logical rules. In Proceedings of the 2016 confer-
ence on empirical methods in natural language process-
ing, pages 192–202, 2016.
[Guo et al., 2018] Shu Guo, Quan Wang, Lihong Wang, Bin
Wang, and Li Guo. Knowledge graph embedding with iter-
ative guidance from soft rules. In Proceedings of the AAAI
Conference on Artificial Intelligence, volume 32, 2018.
[Kapoor and Bahl, 2016] Namarta Kapoor and Nischay
Bahl. Comparative study of forward and backward
chaining in artificial intelligence. International journal
of engineering and computer science, 5(4):16239–16242,
2016.
[Kok and Domingos, 2007] Stanley Kok and Pedro Domin-
gos. Statistical predicate invention. In ICML, 2007.
[Loveland, 2016] Donald W Loveland. Automated theorem
proving: A logical basis. Elsevier, 2016.
[Manhaeve et al., 2018] Robin Manhaeve, Sebastijan Du-
mancic, Angelika Kimmig, Thomas Demeester, and Luc
De Raedt. Deepproblog: neural probabilistic logic pro-
gramming. In NeurIPS, 2018.
[Manhaeve et al., 2021] Robin Manhaeve, Giuseppe Marra,
and Luc De Raedt. Approximate inference for neural prob-
abilistic logic programming. In KR, pages 475–486, 2021.
[Marra et al., 2020] Giuseppe Marra, Michelangelo Dili-
genti, Francesco Giannini, Marco Gori, and Marco Mag-
gini. Relational neural machines. In ECAI, pages 1340–
1347. IOS Press, 2020.
[Marra et al., 2024] Giuseppe Marra, Sebastijan Duman ˇci´c,
Robin Manhaeve, and Luc De Raedt. From statistical re-
lational to neurosymbolic artificial intelligence. Artificial
Intelligence, page 104062, 2024.
[Marra et al., 2025] Giuseppe Marra, Michelangelo Dili-
genti, and Francesco Giannini. Relational reasoning net-
works. Knowledge-Based Systems, page 112822, 2025.
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4813

[Mumick and Pirahesh, 1994] Inderpal Singh Mumick and
Hamid Pirahesh. Implementation of magic-sets in a
relational database system. ACM SIGMOD Record,
23(2):103–114, 1994.
[Niepert, 2016] Mathias Niepert. Discriminative gaifman
models. In NeurIPS, 2016.
[Qu et al., 2020] Meng Qu, Junkun Chen, Louis-Pascal
Xhonneux, Yoshua Bengio, and Jian Tang. Rnnlogic:
Learning logic rules for reasoning on knowledge graphs.
arXiv preprint arXiv:2010.04029, 2020.
[Richardson and Domingos, 2006] Matthew Richardson and
Pedro Domingos. Markov logic networks. Machine learn-
ing, 62(1):107–136, 2006.
[Scarselli et al., 2018] Franco Scarselli, Ah Chung Tsoi, and
Markus Hagenbuchner. The vapnik–chervonenkis dimen-
sion of graph and recursive neural networks. Neural Net-
works, 108:248–259, 2018.
[Shakarian et al., 2023] Paulo Shakarian, Chitta Baral, Ger-
ardo I Simari, Bowen Xi, and Lahari Pokala. Neurasp.
In Neuro Symbolic Reasoning and Learning, pages 63–74.
Springer, 2023.
[Sourek et al., 2018] Gustav Sourek, V ojtech Aschenbren-
ner, Filip Zelezny, Steven Schockaert, and Ondrej
Kuzelka. Lifted relational neural networks: Efficient
learning of latent relational structures. Journal of Artifi-
cial Intelligence Research, 62:69–100, 2018.
[Trouillon et al., 2016] Théo Trouillon, Johannes Welbl, Se-
bastian Riedel, Éric Gaussier, and Guillaume Bouchard.
Complex embeddings for simple link prediction. InICML,
pages 2071–2080, 2016.
[Wang et al., 2017] Quan Wang, Zhendong Mao, Bin Wang,
and Li Guo. Knowledge graph embedding: A survey of
approaches and applications. IEEE TKDE, 29(12):2724–
2743, 2017.
[Winters et al., 2022] Thomas Winters, Giuseppe Marra,
Robin Manhaeve, and Luc De Raedt. Deepstochlog: Neu-
ral stochastic logic programming. In Proceedings of the
AAAI Conference, 2022.
[Yang et al., 2015] Bishan Yang, W. Yih, X. He, J. Gao, and
Li Deng. Embedding entities and relations for learning and
inference in knowledge bases. In ICLR, 2015.
[Zhang et al., 2020] Yuyu Zhang, Xinshi Chen, Yuan Yang,
Arun Ramamurthy, Bo Li, Yuan Qi, and Le Song. Efficient
probabilistic logic reasoning with graph neural networks.
In ICLR, 2020.
Proceedings of the Thirty-Fourth International Joint Conference on Artiﬁcial Intelligence (IJCAI-25)
4814
```
