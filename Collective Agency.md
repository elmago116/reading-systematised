---
title: Collective Agency
author: Rasmus K. Jørgensen, et al.
year: "2025"
Type: Preprint
DOI: ""
source: https://openreview.net/forum?id=NacA6YRBNX
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Collective Agency Jorgensen 2025.pdf]]"
---
[[Collective Agency Jorgensen 2025.pdf]]

## Full text (extracted from `Collective Agency Jorgensen 2025.pdf`)

*Source:* `2PDF/Collective Agency Jorgensen 2025.pdf`  
*Extracted:* 2026-06-18

```text
Proceedings of Machine Learning Research 323:1–31, 2026 5th Conference on Causal Learning and Reasoning
Causal Foundations of Collective Agency
Frederik Hytting Jørgensen FREDERIK .HYTTING @MATH .KU.DK
Copenhagen Causality Lab and Pioneer Centre for AI,
University of Copenhagen, Denmark
Sebastian Weichwald SWEICHWALD @MATH .KU.DK
Copenhagen Causality Lab and Pioneer Centre for AI,
University of Copenhagen, Denmark
Lewis Hammond LEWIS .HAMMOND @COOPERATIVEAI .ORG
Cooperative AI Foundation, United Kingdom
Editors: Bijan Mazaheri and Niels Richard Hansen
Abstract
A key challenge for the safety of advanced AI systems is the possibility that multiple simpler agents
might inadvertently form a collective agent with capabilities and goals distinct from those of any
individual. More generally, determining when a group of agents can be viewed as a unified collective
agent is a foundational question in the study of interactions and incentives in both biological
and artificial systems. We adopt a behavioral perspective in answering this question, ascribing
collective agency to a group when viewing the group’s joint actions as rational and goal-directed
successfully predicts its behavior. We formalize this perspective on collective agency using causal
games (Hammond et al., 2023) – which are causal models of strategic, multi-agent interactions –
and causal abstraction (Rubenstein et al., 2017; Beckers and Halpern, 2019) – which formalizes
when a simple, high-level model faithfully captures a more complex, low-level model. We use this
framework to solve a puzzle regarding multi-agent incentives in actor-critic models and to make
quantitative assessments of the degree of collective agency exhibited by different voting mechanisms.
Our framework aims to provide a foundation for theoretical and empirical work to understand,
predict, and control emergent collective agents in multi-agent AI systems.
Keywords: Collective Agency, Causal Abstraction, Causal Incentives, AI Safety
1. Introduction
When does it make sense to view a group of individual agents as a unified collective agent? While
this question may seem rather subjective at first, there is an intuitive sense in which we might ascribe
collective agency to, for example, a well-organized, efficient, and synchronized team, as opposed to
a random assortment of individuals pursuing independent courses of action. This is despite the fact
that such a team may not have a leader or hierarchical structure (such as a jazz ensemble improvising,
or a school of fish avoiding a predator), and may not even have the same objectives as one another
(such as a market of buyers and sellers, or pollinating insects and flowering plants).
Indeed, humans often use notions of collective agency to understand the world (Roth, 2017;
Schweikard and Schmid, 2021). For example, it is not uncommon for people to use language
such as “country A wants X, which conflicts with the interests of country B” or “company C is
© 2026 F.H. Jørgensen, S. Weichwald & L. Hammond.
JØRGENSEN WEICHWALD HAMMOND
pursuing a new strategy Y”. While statements like these are usually supposed to be approximations,
they can still be helpful for understanding the world and making predictions about the future. Some
have even gone so far as to argue that individual minds are composed of agentic subsystems (Nagel,
1971; Minsky, 1988), in which case there is no privileged level of abstraction on which to locate
agency. How can we make sense of agency arising at various levels of abstraction?
Far from being purely philosophical, this question has important implications for understanding and
predicting collective behavior in multi-agent systems, and hence for ensuring the safety of networks
of artificial agents. A key safety challenge here is the possibility that multiple simpler AI systems
might inadvertently form a ‘super-agent’ with capabilities and goals distinct from any individual
in the group (Drexler, 2019; Hammond et al., 2025). Compared to AI tools, the ability of artificial
agents to make plans and take actions in pursuit of complex goals makes them not only more useful,
but also more harmful if those goals are misaligned or their pursuit produces negative side effects
(Chan et al., 2023). For example, competitive pressures may lead individually rational AI agents to
rapidly exhaust collective resources (Piatti et al., 2024), or a group of agents might combine their
harmless individual capabilities to override safeguards and execute a cyberattack (Jones et al., 2024).
1.1. Example: Actor-Critic Agents
As a simple example of a collective agent, consider the well-known family of reinforcement learning
(RL) agents known as actor-critic (AC) algorithms (Konda and Tsitsiklis, 2000). An AC agent
comprises a critic that attempts to quantify how well the actor is performing relative to an objective,
and an actor that attempts to improve its strategy according to the critic’s judgment. A single-step
decision problem featuring an AC algorithm is shown as a causal game (Hammond et al., 2023) in
Figure 1.
A S R
Q Y W
(a)
A S R
(b)
Figure 1: (a) A causal game representing an AC algorithm. In a causal game, square nodes represent
decisions, circular nodes represent chance variables, diamond nodes represent utilities, and
edges represent causal dependencies. In this game, the actor chooses an action a, which
leads to a new states and in turn the (true) rewardr.2 The critic, on the other hand, chooses
a Q function q that takes as input the action a to produce a predicted reward y “qpaq. The
actor’s utility is given by y and the critic’s utility is given by the loss w “ℓpy, rqwhere ℓ
is a loss function. (b) A causal influence diagram (a single-agent causal game) forming a
valid abstraction of the causal game in panel (a) of Figure 1. In this game, the (collective)
AC agent effectively acts so as to maximize the reward directly. Both figures are adapted
from Kenton et al. (2023).
2. Note that in this simple, single-step AC problem, we leave the (fixed) starting state as implicit, such that Y only has A
as a parent. While it is common for the reward function to be a function of the current state, action, and the new state,
2
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
Even though neither the actor nor the critic is maximizing for the reward, the overall system still
intuitively seems to pursue this goal. In this work, we argue that this is precisely because there
is a valid abstraction that faithfully represents the low-level causal game (Rubenstein et al., 2017;
Beckers and Halpern, 2019; Beckers et al., 2020), and which corresponds to the overall agent (shown
in panel (b) of Figure 1). While Kenton et al. (2023) also suggested that panel (b) of Figure 1 was a
possible alternative model of the true AC dynamics in panel (a), they made no argument as to why.
We solve this problem, providing a formal account of agency at different levels of abstraction.
1.2. Related Work
The question of when multiple individuals constitute a unified collective agent has long occupied
philosophers, with foundational work establishing the importance of collective intentionality and
shared intentions (Searle, 1990; Tuomela, 2006; Ludwig, 2007; List and Pettit, 2011; Pacherie, 2013;
Bratman, 2014). While most of these prior works focus on a rich notion of collective agency, such
as requiring the mental modeling of collaborators, we take a behavioral or ‘black-box’ approach,
reducing the question of whether something is a collective agent to whether ascribing collective
agency is predictive of the group’s behavior. Though these works provide conceptual foundations,
they generally lack the formal machinery needed to rigorously identify collective agents. Recent
work has made progress on defining individual agents using causal and decision-theoretic tools
(Orseau et al., 2018; Kenton et al., 2023; MacDermott et al., 2024; Xu and Rivera, 2024; Abel et al.,
2025; Everitt et al., 2025; Rajcic and Søgaard, 2025), but none formally consider collective agents.
For multi-agent settings, Hammond et al. (2023) introduce causal games – a framework generalizing
multi-agent influence diagrams (Koller and Milch, 2003) to higher levels of Pearl’s causal hierarchy
(Pearl, 2009). Other game-theoretic approaches provide models of coalition formation (Ray, 2007;
Elkind and Rothe, 2016) but do not address whether such coalitions constitute unified agents. The
concept of causal abstraction (Rubenstein et al., 2017; Beckers and Halpern, 2019; Beckers et al.,
2020) formalizes when a high-level causal model is a valid abstraction of a detailed low-level model,
preserving causal relationships when variables are aggregated. However, existing causal abstraction
work focuses on causal models without agents, requiring extension to multi-agent settings with
strategic interactions. A discussion of further related work can be found in Appendix A.
1.3. Contributions
After reviewing the necessary background in Section 2, we first use causal games (Hammond et al.,
2023) to define what we mean by an individual decision-making agent, according to a given notion
of rationality (such as playing a best response), in Section 3. Then, in Section 4 we leverage the
concept of causal abstraction to provide a principled account of when a set of ‘low-level’ agents can
be usefully modeled as a single ‘high-level’ collective agent. Using these formal tools, we prove
a proposition that rules out the emergence of non-trivial agency at higher levels of abstraction and
analyze the emergence of collective agency in the actor-critic example (Section 1.1). We further
illustrate this framework in Section 5 by empirically analyzing different voting mechanisms and
the extent to which they transform the different voters into a collective agent. Section 6 concludes
with a brief summary and an overview of directions for future work. Appendix H further discusses
including sufficient information within the new state leads to an equivalent formulation where the reward is simply a
function of the variable S.
3
JØRGENSEN WEICHWALD HAMMOND
potential applications of our framework to multi-agent reinforcement learning and large language
model agents.
2. Background
Our notation and setup draw inspiration from Geiger et al. (2025). We begin with the notion of a
signature, which describes a set of variables and the values they may take.
Definition 1 A signature is a tuple Σ “ pX, pranpXiqqiPrdsq, where X is a tuple of variables
pX1, . . . , Xdqand pranpXiqqiPrdsis a tuple of ranges for each variable.3
For any subset Y Ď X, we define ranpY q “Ś
Y PY ranpY q. Formally, we assume that the
variables have disjoint ranges.4 Therefore, we may consider the elements of ranpY qas sets rather
than tuples. This technical assumption allows us to identify settings of variables Y ĎX with sets
y PranpY q, which is useful for defining projections (Definition 2) and mechanized abstractions
(Definition 14).
Definition 2 Given two sets of variables Y , Z Ď X, and setting y P ranpY q, we define the
projection ΠZpyq“ y XpŤ
ZPZ ranpZqq.
For example, consider a signature given by the real-valued variablesX “tX1, X2u, i.e., where each
has range txXi |x PRufor i P1, 2. Then ΠtX1upt4X1 , 5X2 uq“t 4X1 uand ΠtX1upt5X2 uq“ ∅.
Definition 3 Given a signature Σ, a deterministic (cyclic) structural causal model ĂM over Σ is a
set of functions tFXuXPX, where FX : ranpXztXuqÑ ranpXq. By SpĂMqwe denote the elements
x PranpXq– i.e. the solutions – that satisfy FXpxzΠXpxqq“ ΠXpxqfor all X PX.
Notice that while deterministic structural causal models may be cyclic, we will assume that proba-
bilistic causal models are acyclic (see Definition 5).
Definition 4 A hard intervention in a deterministic SCM is a setting y of some subset of variables
Y ĎX. By SpĂM; yq– the solutions in ĂM, given intervention y – we denote the set of values
x PranpXqsuch that FXpxzΠXpxqq“ ΠXpxqfor X RY and ΠXpxq“ ΠXpyqfor X PY .
A hard intervention corresponds to replacing the functions FX with z ÞÑΠXpyqfor X PY , and the
solutions SpĂM; yqcorrespond to the settings x of variables X that are solutions to this new system
of equations.
Definition 5 Given a signature Σ, a structural causal model (SCM) M over Σ is a tuple
ppV , Eq, G, tFV uV PV , PpEqq,
where
‚ pV , Eqis a partition of the variables in Σ into noise variables E and object variables V .
We assume that each object variable has a unique noise variable associated with it, that is,
E “tEV uV PV .
3. We sometimes consider X a set rather than a tuple.
4. The assumption of disjoint ranges can be made without loss of generality: we subscript every value with the variable
name to ensure uniqueness, such that, for example, xXi ‰xXj for x PR and i ‰j. If it is clear from the context
which range a value belongs to, we may omit the subscript.
4
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
‚ G is a directed acyclic graph over the object variables V .
‚ tFV uV PV is a set of structural assignments FV : ranpPAG
V YtEV uqÑ ranpV q, where PAG
V
denotes the parents of V in G.
‚ PpEqis a distribution on ranpEq. We assume that the variables tEV uV PV are jointly indepen-
dent.
An SCM M induces a unique distribution PMpV qover the object variables V such that V “
FV pPAV , EV q, in distribution, for every V PV . Since the noise variables are jointly independent,
the induced distribution PMpV qis Markovian with respect to G (Peters et al., 2017, Prop. 6.31).
In order to consider causal games in which the mechanisms (i.e. the structural functions and noise
variables) governing an object variable can change if an agent selects a different strategy, it will be
useful to define parameterized SCMs, which is a class of SCMs with functions that are indexed by
parameters.5
Definition 6 Given a signature Σ, a parameterized SCM MΘ over Σ is a tuple
´
pV , Eq, G, tΘV uV PV , tFθ
V uV PV ,θPΘV , PpEq
¯
where pV , Eq, G, and PpEqare as for an SCM (Definition 5), and
‚ tΘV uV PV is a set of parameter spaces, one for each object variable.
‚ tFθ
V uV PV ,θPΘV is a set of structural assignments Fθ
V : ranpPAG
V YtEV uqÑ ranpV q, which
are indexed by variables V and parameters θV PΘV .
For a given setting θ “tθV uV PV of the parameters θV PΘV , a parameterized SCM induces an
SCM Mθ.
We are now ready to provide a formal definition of mechanized structural causal models (Ham-
mond et al., 2023), in which the parameters θV of each structural function (representing the causal
mechanisms in the model) are explicitly represented and governed by a separate deterministic cyclic
SCM.6 We depart slightly from Hammond et al. (2023) by having the mechanisms being governed
by functions rather than relations.
Definition 7 A mechanized SCM mM is a tuple ( ĂM, MΘ) where
‚ ĂM is a deterministic cyclic SCM with mechanism variables rV .
‚ MΘ is a parameterized SCM with object variables V .
We refer to V as the object nodes and to rV as the mechanism nodes. We assume that there is a one
to one correspondence between the mechanism variables rV and object variables V , and that MΘ’s
parameter sets are ΘV “ranprV qfor each V PV . Every solution s PSpĂMqinduces an SCM Ms
with structural assignments tF
Π rV psq
V |V PV uand distribution PspV q. By PSpĂMqpV qwe denote
the set of distributions tPspV q| s PSpĂMqu.
5. This restriction to parameterized functions – again departing from (Hammond et al., 2023) – is more natural for AI
agents whose strategies are represented by parametric models such as a neural network.
6. Dawid (2002) provides an earlier example of mechanized SCMs, though he does not consider the mechanism nodes
themselves as being governed by an SCM, rather each mechanism node is parentless.
5
JØRGENSEN WEICHWALD HAMMOND
To help the reader understand this formalism, we provide a worked out formalization of the ‘Battle
of the Sexes’ game as a mechanized SCM in Appendix B.
3. Agency
We define utilities as functions of nodes (i.e. object variables) rather than nodes in the causal
graph itself, highlighting the constitutive rather than causal relationship between utilities and object
variables (Xia and Bareinboim, 2024). For example, we may have two different agents, who both
care about the number of bicycles in the world, but one agent wants to maximize the number of
bicycles in the world, while the other agent wants to minimize the number of bicycles in the world. In
that case, it would be problematic to have two different utility nodes because there would be a logical
rather than causal relationship between the two utility nodes, which would violate the assumption of
independent causal mechanisms (Peters et al., 2017; Jørgensen et al., 2025).
Definition 8 Given a mechanized SCM mM with object variables V , we define a utility function
as a function U : ranpV qÑ R.
While we technically allow that a utility function U may depend on several object variables U ĎV,
we will usually consider utilities that depend on a single object variable U. Given a utility function,
we may wonder if any object level variables can be viewed as optimizing it. For this purpose, we use
rationality relations (Hammond et al., 2023), which describe how an agent would react in a given
context if employing a certain conception of rationality and having a certain utility function.
Definition 9 Given a mechanized SCM mM, a mechanism node rS P rV and a utility function
U : ran pV q ÑR, a rationality relation is a total relation RrS Ď ranprV ztrSuqˆ ranprSq. If
FrSprcqP RrSprcq7 for every context rc PranprV ztrSuq, then we say that rS responds R-rationally to
utility U.
Intuitively, RrSprcqspecifies the set of policies an agent with decision node S employing rationality
relation RrS could employ in context rc if having utility function U.
Definition 10 Given a mechanism node rS P rV and a utility function U : ranpV qÑ R, we define
the best response rationality relation RBR
rS under utility U by the condition that
rs PRBR
rS prcq if and only if rs Parg max
rs1PranprSq
Ers1,rcpUpV qq
for every rc PranprV ztrSuq.
Best response rationality is the main rationality concept we consider. Sometimes, other rationality
concepts, such as subgame perfection, may be more appropriate (Hammond et al., 2023). Different
notions of rationality may be particularly relevant in the context of collective agency for AI agents,
where agents may be interacting with copies of themselves or have access to each other’s parameters
(Critch et al., 2022; Oesterheld et al., 2023). We leave a detailed investigation of various rationality
relations for future work, but in Appendix C, we show that sometimes we do not have collective
agency under best response rationality, while we do have it for other rationality concepts.
7. By RrSprcqwe denote the set trs PranprSq|p rc, rsqP RrSu.
6
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
Below we operationalize agency as rational, goal-driven behavior. While we do not claim that this
is all that there is to the philosophical concept of agency, we do believe that this provides a useful
starting point for a formalization of agency that works across levels of abstraction.
Definition 11 Given a mechanized SCM mM, we say a mechanism variable rS P rV is an (R, U)-
agent if rS responds R-rationally to utility U.
Kenton et al. (2023) discuss assumptions that make it possible to identify which nodes correspond to
best-response rational agents and which nodes enter into their utility functions. Notice that every
object variable is an agent with respect to best response rationality and a constant utility function.
This is related to a classical insight in inverse reinforcement learning (Ng et al., 2000; Skalse and
Abate, 2024), namely that reward functions are not generally identifiable from behavior. Likewise,
if we allow any utility function, then any mechanism variable can be viewed as an agent. While
modeling something as an agent optimizing for a constant utility function does not make false
predictions, it also does not make any non-vacuous predictions.
Definition 12 We say that a mechanism variable rS P rV is a non-trivial (R, U)-agent if it is an
(R, U)-agent and there exist two settings rc,rc1 P ranprV ztrSuqsuch that Prc,FrSprcqpS | PASq ‰
Prc1,FrSprc1qpS |PASq
4. Collective Agency
4.1. Mechanized Abstractions
In this section, we refer to objects related to the high-level model using superscripts *. Given a
low-level mechanized SCM mM, and a corresponding high-level mechanized SCM mM˚, we need
to specify which of the low-level object variables V correspond to which high-level object variables
V ˚. We call this correspondence a variable alignment.
Definition 13 Given two mechanized causal graphs mM and mM˚, a variable alignment is a
mapping A : V ˚ ÑPpV qzt∅usuch that AV ˚
1
XAV ˚
2
“∅ for any two variables V ˚
1 , V˚
2 PV ˚
(where AV ˚
1
:“ApV ˚
1 q). Given a variable alignment, we define ArV ˚ Ď rV as those mechanism nodes
that correspond to the object variables in AV ˚.
Given a variable alignment A, a set of functions tτV ˚uV ˚PV ˚, where τV ˚ : ranpAV ˚qÑ ranpV ˚q,
induces a function τ : ranpV q ÑranpV ˚qgiven by τpvq “Ť
V ˚PV ˚ τV ˚pΠAV ˚pvqq. We call
these functions value mappings. These functions determine how we translate values of low-level
object variables to values of high-level object variables. In addition, we need to specify how we
translate interventions on the low-level mechanisms variables to interventions on the high-level
mechanisms variables. These intervention mappings are given by partial functions tωrV ˚urV ˚PrV
˚,
where ωrV ˚ : ranpArV ˚qá ranprV ˚q. By dompωrV ˚q, we denote the subset of ranpArV ˚qon which
ωrV ˚ is defined. For a subset rY
˚
Ď rV
˚
, we define dompω rY
˚q “Ś
rV ˚PrY
˚ dompωrV ˚q. The set
of intervention mappings naturally induces a partial function ω, from any setting of a subset of
low-level collections Ť
rV ˚PrY
˚ ArV ˚ to a setting of rY
˚
, in particular, given ry Pdompω rY
˚q, ω maps
to Ť
rV ˚PrY
˚ ωrV ˚pΠA rV ˚pryqq.
Definition 14 Assume that we have two mechanized causal models mM and mM˚. Let a node
alignment A be given. We say that mM˚is a mechanized abstraction of mM under value mappings
7
JØRGENSEN WEICHWALD HAMMOND
tτV ˚uV ˚PV ˚ (τV ˚ : ran pAV ˚q ÑranpV ˚q), and intervention mappings tωrV ˚urV ˚PrV
˚ (ωrV ˚ :
ranpArV ˚qá ranprV ˚q), if
PSpĂM;ryqpτpV qq“ PSpĂM˚;ωpryqqpV ˚q, (1)
for any subset rY
˚
Ď rV
˚
, and intervention ry Pdompω rY
˚q.
Notice that Definition 14 in particular requires observational consistency, that is,PSpĂMqpτpV qq“
PSpĂM˚qpV ˚q, by considering the empty subset rY
˚
“∅.
Analogously to Beckers and Halpern (2019), we define strong mechanized abstractions by adding
the requirement that for any setting of a subset of high-level mechanisms, there exists a low-level
intervention that implements it.
Definition 15 We say thatmM˚is a strong mechanized abstractionof mM under tτV ˚uV ˚PV ˚ and
tωrV ˚urV ˚PrV
˚ if mM˚ is a mechanized abstraction of mM under tτV ˚uV ˚PV ˚ and tωrV ˚urV ˚PrV
˚,
and each ωrV ˚ is surjective onto ranprV ˚q.
If the mechanism models ĂM and ĂM˚ have no edges, then the definition above is an extension
of constructive abstractions (Beckers and Halpern, 2019) that includes soft interventions a (hard
intervention on mechanism variables may correspond to a soft intervention on the object variables).
Unlike previous work on abstractions of soft interventions (Massidda et al., 2023), we do not impose
any restrictions on ω except that it is induced from intervention mappings on the variable alignment.
We believe that any further restrictions onω must derive from context-specific considerations rather
than being part of the definition. There are several ways in which this definition can be extended
to approximate abstractions (Beckers et al., 2020; Rischel and Weichwald, 2021) and we likewise
believe that the appropriate generalization is context-dependent. In Section 5, we consider restrictions
on ω and a notion of approximate abstraction based on mean squared error for a fixed distribution
over low-level interventions. In other applications, it is likely appropriate to consider KL divergence
as is done, for example, in Dyer et al. (2024).
4.2. Ruling out emergence of non-trivial agency
We may want to rule out the emergence of agency at higher levels of abstraction. In this section,
we provide a first example of a theorem that rules out that a node is a high-level agent based on
properties of the low level.
We say that a mechanism node rS has an independent mechanism if there exists a setting rs PranprSq
such that FrSprcq“ rs for all rc PranprV ztrSuq.
Proposition 16 Let mechanized models mM and mM˚ be given. Assume that mM˚ is a strong
mechanized abstraction of mM for some value mappings tτV ˚uV ˚PV ˚ and intervention mappings
tωrV ˚urV ˚PrV
˚. Let rS˚ P rV
˚
be a high-level mechanism variable. Assume that (i) τPAS˚ is injective,
and (ii) the mechanism nodes in ArS˚ have independent mechanisms. Then rS˚ is not a non-trivial
agent in mM˚. [See Appendix E for the proof.]
We think that having a more complete theory of the (non-)emergence of agency is an important
direction for future work.
8
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
mM rA rS rR
A S R
Q Y W
rQ rY ĂW
mM˚
rA˚ rS˚ rR˚
A˚ S˚ R˚
τ, ω
Figure 2: A graphical representation of a causal abstraction applied to mechanized SCMs represent-
ing the AC example from Section 1.1 (see Appendix D for the explicit construction of the
abstraction). On the left hand side, we have the low-level model mM. On the right, we
have a high-level model mM˚, which is a valid abstraction of the low-level model under
τ and ω. By examining the high-level model, we can see that A˚is an RBR-rational agent
with utility equal to the reward: Upv˚q“ ΠR˚pv˚q.
4.3. Example: Actor-Critic Agents (Revisited)
We revisit the one-step AC agent (as described in Kenton et al. (2023) and Section 1.1). Here the critic
rQ is tasked with predicting the reward R for different actions that the actor rA may take. The action
A taken by the actor rA affects the state, and in turn, the reward. Kenton et al. (2023) hypothesize
that one can, at a more coarse-grained level, view this as a single-agent system. This in turn explains
why the system intuitively has an incentive to manipulate the state S, even though if one applies the
graphical criterion for single-agent graphs (Everitt et al., 2021), it suggests that neither rA nor rQ have
an incentive to manipulate the state S. See Appendix D for details about how to formalize this setup
in terms of mechanized SCMs.
Proposition 17 In Figure 2 (see also Appendix D for details), mM˚ is a strong mechanized
abstraction of mM. Furthermore, rA˚in the high-level model mM˚is an pRBR, Uq-agent with utility
equal to the reward Upv˚q“ ΠR˚pv˚q. [See Appendix F for the proof.]
Note that while the AC example ‘marginalizes’ out one of the agents (namely the critic), our
framework allows for more general types of collective agency. For example, in the next section, we
consider aggregating individuals into a single agent.
5. Example: Using Collective Agency for Surrogate Modeling
In this section we show an application of collective agency for surrogate modeling. Specifically,
we investigate the degree to which it makes sense to model countries as collective agents under
various voting mechanisms. Dyer et al. (2024) introduced the idea of using causal abstractions for
interventionally consistent surrogate modeling. We build on this work by extending it to mechanized
abstractions with agents. There are at least three potential benefits of using surrogate models with
collective agents: 1) the low-level model is often a black box where new interventions cannot be
9
JØRGENSEN WEICHWALD HAMMOND
rv1,1
v1,1
rv1,2
v1,2
. . .
. . .
rv1,n
v1,n
q1rq1
rv2,1
v2,1
rv2,2
v2,2
. . .
. . .
rv2,n
v2,n
q2 rq2U
rU
Low-Level Country 1 Low-Level Country 2
Global Interaction
rq1
q1
rq2
q2
High-Level Country 1 High-Level Country 2
U
rU ω
ˆ ˙
τ, ω
Figure 3: At the low level, the global interaction includes edges between every pair of citizens and
from the voting mechanism rq1 and rq2 to every citizen. At the high level, we view the
countries as being individual agents, picking the pollution level in response to the other
countries. Since we are intervening on the citizens preferences, we explicitly include a
(vector valued) utility node rU. At the low level, it has dimension equal to the number of
citizens. At the high level, it has dimension equal to the number of countries. In the figure
and the main text, we omit superscripts (*) for the high level.
simulated;8 2) computing low-level equilibria may be computationally expensive, which hinders
evaluations of new interventions; and 3) agency-based surrogate models may be useful for assessing
abstract counterfactuals such as “how would country A react if country B adopts policy X?”.
While we believe that there are practical applications where surrogate modeling with agents is useful,
the main point of the example below is to provide a theoretical illustration and proof of concept. We
therefore prioritize simplicity over realistic assumptions.
5.1. The Low-Level Model
We have C countries and each country c has Nc citizens. Each country employs a voting mechanism
to determine the level of pollution qc. We assume that individual i from country c has utility
Ucipqc, q´cq“ aciqc ´bciq2
c ´dciQ2
W ,
8. This is essentially the point of discovering psychological regularities. It is much easier to predict people’s behavior
based on abstract models of beliefs and preferences than based on neurophysiology (Dennett, 1989).
10
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
where q´c are the pollution levels of countries other thanc, aci, bci, dci PR are individual parameters,
and QW “ř
c qc. We consider interventions on individuals’ preferences for pollution, for example,
implemented by taxation or advocacy, such that aci is replaced with aci ´λci ě0.
We assume that the result of the countries’ votes is a Nash equilibrium (NE) where every citizen of
every country is a player. This NE may be computationally expensive to evaluate or, if the low-level
model is not understood, can only be evaluated by playing it out in the physical world. Rather than
reasoning about NEs containing every citizen of every country, it may be possible to model the
situations at a higher level of abstraction where countries are modeled as agents.
5.2. The High-Level Model
We use a parametric model for country utilities, which mimics the utilities of individual agents:
Ucpqc, q´cq“ Acqc ´Bcq2
c ´DcQ2
W . (2)
Assuming that each country is an agent with this utility function, it is easy to derive that under NE,
the total amount of pollution is
QNE
W “
1
2
ř
c
Ac
Bc
1 `ř
c
Dc
Bc
,
and the individual contributions are
qNE
c “ Ac
2Bc
´Dc
Bc
QNE
W . (3)
Notice that there is no guarantee that the voting mechanisms will produce pollution levels that are
correctly modeled by the countries playing an NE according to a utility function parameterized by
Equation (2). This is a modeling choice that may or may not be appropriate depending on the actual
voting mechanism that is used and the utility functions of the individual citizens.
5.3. Connecting the Low-Level and High-Level Models
We want to learn a mapping ω from the vector intervention λ :“ pλciqci to an intervention on
pAc, Bc, Dcqc such that the high-level model is a mechanized abstraction of the low-level model (see
Figure 3). In other words, we want to see if we can view the countries as collective agents. Formally,
ω ought to be such that
PSpĂM;λqppqcqcq“ PSpĂM˚;ωpλqqppqcqcq
where we assume that solutions are given by best response rationality. In words, we want that
applying intervention λ to the citizen preferences results in a low-level NE that equals the high-level
NE under the ωpλqintervention in the high-level model.
Notice that the high-level NE only depends on the parameters Ac,Bc, and Dc through the fractions
αc :“ Ac
Bc and δc :“Dc
Bc . A single sample is not enough to identify αc and δc (for each country, we
have a single equation – Equation (3) – and two unknowns). Therefore we need to make assumptions
about how our intervention affects the high-level utility function. For simplicity, we assume that the
interventions only affect the αc’s and not the δc’s (which we know to be true for VCG voting; see
11
JØRGENSEN WEICHWALD HAMMOND
Appendix G.1). Whether this assumption is reasonable for other voting mechanisms is an empirical
question, which we explore in the results section.
Using this assumption, we estimate ω using a two-step procedure. First, for each country c, we
apply interventions such that λci “0 for all citizens i of country c, but non-zero for other countries.
We then estimate δc by linear regression of qc on QW (which is justified by Equation (3)). Second,
we parametrize ω : R
ř
c Nc ÑRC by the weights ϕ of a neural network and train the network to
minimize the loss function
Losspϕq“
ÿ
j
ÿ
c
“
pqNE
c pϕpλjqq´ qNE
c pλjq
‰2
,
where λj is an intervention on the citizens preferences, qNE
c pλjqis the resulting ground-truth low-
level NE, and pqNE
c pϕpλjqqis the NE derived by Equation (3) and the estimated pδc and xαc, the latter
of which is one of the outputs returned by ω. The interventions λj are sampled according to a fixed
distribution (see Appendix G.2 for details). Minimizing the consistency loss is the central idea of
approximate causal abstractions (Beckers et al., 2020; Rischel and Weichwald, 2021).
5.4. Results
We consider three different voting mechanisms: Vickrey-Clarke-Groves (VCG), Median V oting,
and Random Dictator. Descriptions of the three voting mechanisms and how we compute low-level
Nash equilibria for each are given in Appendix G.1. We apply our method to a simulation with
five countries and a total of 1,000 citizens. See Appendix G.2 for details about the simulations and
training. We report a summary of the results in Table 1 and provide detailed results in Appendix G.3.
Mechanism Model MAE Baseline MAE Improvement
VCG 0.062 1.254 95.0%
Median 0.142 1.248 88.6%
Random Dictator 5.077 4.645 -9.3%
Table 1: We are predictingqc for different voting mechanisms under interventionsλ. (MAE) is mean
absolute error for different voting mechanisms. The baseline is calculated by constantly
predicting the low-level Nash equilibrium at λ “0 (since random dictator is stochastic we
use the average low-level NE for this mechanism as the baseline). The errors are summed
across all countries. VCG and Median voting show low errors (compared to the baseline),
indicating that the collective agency framework effectively captures how interventions
affect outcomes. Random Dictator performs worse than the baseline (-9.3%) and has large
absolute errors, demonstrating the difficulty of learning an ω for this mechanism.
6. Summary and future work
In this work we have laid out a mathematical foundation of agency and collective agency based on
the mathematical formalisms of mechanized causal graphs and causal abstraction. The framework
opens up many interesting questions that we hope can be addressed in future work, including: 1)
Investigating how different notions of rationality, such as different decision theories, affect the
propensity for collective agency; 2) Developing a theory that predicts when collective agency
12
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
will emerge (see Proposition 16); 3) Extending inverse game theory or inverse reinforcement
learning to various levels of abstraction; and 4) Translating our theory of collective agency into a
mathematical framework that more naturally accommodates both non-independent mechanisms and
causal abstractions, such as Garrabrant et al. (2024). We also hope that our work can help to provide
the foundation for further theoretical and empirical work to understand, predict, and control emergent
collective agents in networks of AI systems.
7. Acknowledgments
This work was initiated during FHJ’s participation in the Pivotal Research Fellowship. We thank
Casper L ¨utzhøft Christensen, Soroush Ebadian, Sukanya Krishna, Francisco Madaleno, Kyle
Reynoso, Morgan Simpson, and Riya Tyagi for helpful discussions and feedback.
References
David Abel, Andr ´e Barreto, Michael Bowling, Will Dabney, Shi Dong, Steven Hansen, Anna
Harutyunyan, Khimya Khetarpal, Clare Lyle, Razvan Pascanu, et al. Agency is frame-dependent.
arXiv, 2025. arXiv:2502.04403. (Cited on page 3.)
P. W. Anderson. More is different: Broken symmetry and the nature of the hierarchical structure of
science. Science, 177(4047):393–396, 1972. (Cited on page 18.)
Sander Beckers and Joseph Y . Halpern. Abstracting causal models. InAAAI Conference on Artificial
Intelligence, 2019. (Cited on pages 1, 3, 8, and 19.)
Sander Beckers, Frederick Eberhardt, and Joseph Y . Halpern. Approximate causal abstractions. In
Uncertainty in Artificial Intelligence, 2020. (Cited on pages 3, 8, 12, and 19.)
Eric Bonabeau, Marco Dorigo, and Guy Theraulaz. Swarm Intelligence: From Natural to Artificial
Systems. Oxford University Press, 1999. (Cited on page 19.)
Michael E. Bratman. Shared Agency: A Planning Theory of Acting Together. Oxford University
Press, 2014. (Cited on pages 3 and 18.)
Alan Chan, Rebecca Salganik, Alva Markelius, Chris Pang, Nitarshan Rajkumar, Dmitrii Krashenin-
nikov, Lauro Langosco, Zhonghao He, Yawen Duan, Micah Carroll, et al. Harms from increasingly
agentic algorithmic systems. In Conference on Fairness, Accountability, and Transparency, 2023.
(Cited on pages 2 and 20.)
Chih-Chun Chen, Sylvia B. Nagl, and Christopher D. Clack. A formalism for multi-level emergent
behaviours in designed component-based systems and agent-based simulations. In Moulay Aziz-
Alaoui and Cyrille Bertelle, editors, From System Complexity to Emergent Properties, chapter 4,
pages 101–114. Springer, 2009. (Cited on page 20.)
Iain D. Couzin. Collective cognition in animal groups. Trends in Cognitive Sciences, 13(1):36–43,
2009. (Cited on page 19.)
13
JØRGENSEN WEICHWALD HAMMOND
Andrew Critch, Michael Dennis, and Stuart Russell. Cooperative and uncooperative institution
designs: Surprises and problems in open-source game theory. arXiv, 2022. arXiv:2208.07006.
(Cited on page 6.)
A Philip Dawid. Influence diagrams for causal modelling and inference. International Statistical
Review, 2002. (Cited on page 5.)
Daniel C Dennett. The intentional stance. MIT Press, 1989. (Cited on page 10.)
K. Eric Drexler. Reframing superintelligence: Comprehensive AI services as general intelligence.
Technical Report 2019-1, Future of Humanity Institute, University of Oxford, 2019. (Cited on
pages 2 and 20.)
Yilun Du, Shuang Li, Antonio Torralba, Joshua B. Tenenbaum, and Igor Mordatch. Improving factu-
ality and reasoning in language models through multiagent debate. In International Conference on
Learning Representations, 2024. (Cited on page 30.)
Joel Dyer, Nicholas George Bishop, Yorgos Felekis, Fabio Massimo Zennaro, Ani Calinescu,
Theodoros Damoulas, and Michael J. Wooldridge. Interventionally consistent surrogates for
complex simulation models. In Advances in Neural Information Processing Systems, 2024. (Cited
on pages 8 and 9.)
Edith Elkind and J¨org Rothe. Cooperative Game Theory, chapter 3, pages 135–193. Springer, 2016.
(Cited on pages 3 and 19.)
Tom Everitt, Ryan Carey, Eric D Langlois, Pedro A Ortega, and Shane Legg. Agent incentives: A
causal perspective. In AAAI Conference on Artificial Intelligence, 2021. (Cited on page 9.)
Tom Everitt, Cristina Garbacea, Alexis Bellot, Jonathan Richens, Henry Papadatos, Sim´eon Campos,
and Rohin Shah. Evaluating the goal-directedness of large language models. arXiv, 2025.
arXiv:2504.11844. (Cited on pages 3, 19, and 31.)
Karl J Friston, Maxwell J D Ramstead, Alex B Kiefer, Alexander Tschantz, Christopher L Buckley,
Mahault Albarracin, Riddhi J Pitliya, Conor Heins, Brennan Klein, Beren Millidge, Dalton A R
Sakthivadivel, Toby St Clere Smithe, Magnus Koudahl, Safae Essafi Tremblay, Capm Petersen,
Kaiser Fung, Jason G Fox, Steven Swanson, Dan Mapes, and Gabriel Ren´e. Designing ecosystems
of intelligence from first principles. Collective Intelligence, 3(1), 2024 , 3(1), 2022. (Cited on
page 19.)
Scott Garrabrant, Matthias Georg Mayer, Magdalena Wache, Leon Lang, Sam Eisenstat, and Holger
Dell. Factored space models: Towards causality between levels of abstraction. arXiv, 2024.
arXiv:2412.02579. (Cited on page 13.)
Atticus Geiger, Duligur Ibeling, Amir Zur, Maheep Chaudhary, Sonakshi Chauhan, Jing Huang,
Aryaman Arora, Zhengxuan Wu, Noah Goodman, Christopher Potts, et al. Causal abstraction: A
theoretical foundation for mechanistic interpretability. Journal of Machine Learning Research, 26,
2025. (Cited on page 4.)
Natalie Gold and Robert Sugden. Collective intentions and team agency. Journal of Philosophy, 104
(3):109–137, 2007. (Cited on page 18.)
14
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
Joseph Y . Halpern and Max Kleiman-Weiner. Towards formal definitions of blameworthiness,
intention, and moral responsibility. In AAAI Conference on Artificial Intelligence, 2018. (Cited on
page 19.)
Lewis Hammond, James Fox, Tom Everitt, Ryan Carey, Alessandro Abate, and Michael Wooldridge.
Reasoning about causality in games. Artificial Intelligence, 320:103919, 2023. (Cited on pages 1, 2,
3, 5, 6, and 19.)
Lewis Hammond, Alan Chan, Jesse Clifton, Jason Hoelscher-Obermaier, Akbir Khan, Euan McLean,
Chandler Smith, Wolfram Barfuss, Jakob Foerster, Tom ´aˇs Gavenˇciak, The Anh Han, Edward
Hughes, V ojtˇech Kovaˇr´ık, Jan Kulveit, Joel Z. Leibo, Caspar Oesterheld, Christian Schroeder
de Witt, Nisarg Shah, Michael Wellman, Paolo Bova, Theodor Cimpeanu, Carson Ezell, Quentin
Feuillade-Montixi, Matija Franklin, Esben Kran, Igor Krawczuk, Max Lamparth, Niklas Lauffer,
Alexander Meinke, Sumeet Motwani, Anka Reuel, Vincent Conitzer, Michael Dennis, Iason
Gabriel, Adam Gleave, Gillian Hadfield, Nika Haghtalab, Atoosa Kasirzadeh, S ´ebastien Krier,
Kate Larson, Joel Lehman, David C. Parkes, Georgios Piliouras, and Iyad Rahwan. Multi-agent
risks from advanced AI. Technical Report 1, Cooperative AI Foundation, 2025. (Cited on pages 2
and 20.)
Geoffrey Irving, Paul Christiano, and Dario Amodei. AI safety via debate. arXiv preprint
arXiv:1805.00899, 2018. (Cited on page 30.)
Erik Jones, Anca Dragan, and Jacob Steinhardt. Adversaries can misuse combinations of safe models.
arXiv, 2024. arXiv:2406.14595. (Cited on pages 2 and 20.)
Frederik Hytting Jørgensen, Luigi Gresele, and Sebastian Weichwald. What is causal about causal
models and representations? arXiv, 2025. arXiv:2501.19335. (Cited on pages 6 and 30.)
Zachary Kenton, Ramana Kumar, Sebastian Farquhar, Jonathan Richens, Matt MacDermott, and
Tom Everitt. Discovering agents. Artificial Intelligence, 2023. (Cited on pages 2, 3, 7, 9, 19, and 24.)
Daphne Koller and Brian Milch. Multi-agent influence diagrams for representing and solving games.
Games and Economic Behavior, 45(1):181–221, 2003. (Cited on pages 3 and 19.)
Vijay R. Konda and John N. Tsitsiklis. Actor-critic algorithms. In S. A. Solla, T. K. Leen, and
K. M¨uller, editors, Advances in Neural Information Processing Systems, pages 1008–1014. MIT
Press, 2000. (Cited on page 2.)
Aleˇs Kub´ık. Toward a formalization of emergence. Artificial Life, 9(1):41–65, 2003. (Cited on
page 19.)
Hector J. Levesque, Philip R. Cohen, and Jos ´e H. T. Nunes. On acting together. In Proceedings
of the 8th National Conference on Artificial Intelligence. Boston, Massachusetts, USA, July 29 -
August 3, 1990, 2 Volumes, 1990. (Cited on page 19.)
Qian Li et al. Towards scalable oversight with collaborative multi-agent debate in error detection.
arXiv preprint, 2025. (Cited on page 30.)
Christian List and Philip Pettit. Group Agency: The Possibility, Design, and Status of Corporate
Agents. Oxford University Press, 2011. (Cited on pages 3 and 18.)
15
JØRGENSEN WEICHWALD HAMMOND
Kirk Ludwig. Collective intentional behavior from the standpoint of semantics.Noˆus, 41(3):355–393,
2007. (Cited on pages 3 and 18.)
Matt MacDermott, James Fox, Francesco Belardinelli, and Tom Everitt. Measuring goal-directedness.
In Advances in Neural Information Processing Systems, 2024. (Cited on pages 3 and 19.)
Thomas W. Malone and Michael S. Bernstein. Handbook of Collective Intelligence. MIT Press,
2015. (Cited on page 18.)
Riccardo Massidda, Atticus Geiger, Thomas Icard, and Davide Bacciu. Causal abstraction with soft
interventions. In Causal Learning and Reasoning, 2023. (Cited on page 8.)
Marvin Minsky. The Society of Mind. Simon and Schuster, 6. pb-pr. edition, 1988. (Cited on pages 2
and 18.)
Melanie Mitchell. Complexity A Guided Tour. Oxford University Press, 2009. (Cited on page 18.)
Thomas Nagel. Brain bisection and the unity of consciousness. Synthese, 22(3/4):396–413, 1971.
(Cited on page 2.)
Andrew Y Ng, Stuart Russell, et al. Algorithms for inverse reinforcement learning. In International
Conference on Machine Learning, 2000. (Cited on page 7.)
Caspar Oesterheld, Johannes Treutlein, Roger B Grosse, Vincent Conitzer, and Jakob Foerster.
Similarity-based cooperative equilibrium. In Advances in Neural Information Processing Systems,
2023. (Cited on page 6.)
Samir Okasha. Agents and Goals in Evolution. Oxford University Press, 2018. (Cited on page 19.)
Laurent Orseau, Simon McGregor McGill, and Shane Legg. Agents and devices: A relative definition
of agency. arXiv, 2018. arXiv:1805.12387. (Cited on pages 3 and 19.)
Elisabeth Pacherie. Intentional joint agency: Shared intention lite. Synthese, 190(10):1817–1839,
2013. (Cited on pages 3 and 18.)
Judea Pearl. Causality. Cambridge University Press, 2009. (Cited on pages 3 and 19.)
Jonas Peters, Dominik Janzing, and Bernhard Sch¨olkopf. Elements of Causal Inference: Foundations
and Learning Algorithms. MIT Press, 2017. (Cited on pages 5 and 6.)
Giorgio Piatti, Zhijing Jin, Max Kleiman-Weiner, Bernhard Sch¨olkopf, Mrinmaya Sachan, and Rada
Mihalcea. Cooperate or collapse: emergence of sustainable cooperation in a society of LLM
agents. In Advances in Neural Information Processing Systems, 2024. (Cited on pages 2 and 20.)
Nina Rajcic and Anders Søgaard. Goal-directedness is in the eye of the beholder. arXiv, 2025.
arXiv:2508.13247. (Cited on page 3.)
Deepak Ramachandran and Eyal Amir. Bayesian inverse reinforcement learning. In Proceedings of
the 20th International Joint Conference on Artificial Intelligence, 2007. (Cited on page 19.)
Debraj Ray. A Game-Theoretic Perspective on Coalition Formation. Oxford University Press, 2007.
(Cited on pages 3 and 19.)
16
CAUSAL FOUNDATIONS OF COLLECTIVE AGENCY
Alexander G. Reisach, Alberto Su´arez, Sebastian Weichwald, and Antoine Chambaz. The case for
time in causal DAGs. arXiv, 2025. arXiv:2501.19311. (Cited on page 30.)
Eigil F. Rischel and Sebastian Weichwald. Compositional abstraction error and a category of causal
models. In Uncertainty in Artificial Intelligence, 2021. (Cited on pages 8 and 12.)
Abraham Sesshu Roth. Shared Agency. In Edward N. Zalta, editor, The Stanford Encyclopedia of
Philosophy. Metaphysics Research Lab, Stanford University, 2017. (Cited on pages 1 and 18.)
Paul K. Rubenstein, Sebastian Weichwald, Stephan Bongers, Joris M. Mooij, Dominik Janzing,
Moritz Grosse-Wentrup, and Bernhard Sch ¨olkopf. Causal consistency of structural equation
models. In Uncertainty in Artificial Intelligence, 2017. (Cited on pages 1, 3, and 19.)
David P. Schweikard and Hans Bernhard Schmid. Collective Intentionality. In Edward N. Zalta,
editor, The Stanford Encyclopedia of Philosophy. Metaphysics Research Lab, Stanford University,
2021. (Cited on page 1.)
John Searle. Collective intentions and actions. In Philip R. Cohen Jerry Morgan and Martha Pollack,
editors, Intentions in Communication, pages 401–415. MIT Press, 1990. (Cited on pages 3 and 18.)
Anil Seth. Measuring emergence via nonlinear granger causality. In Artificial Life XI: Proceedings
of the Eleventh International Conference on the Simulation and Synthesis of Living Systems, 2006.
(Cited on page 19.)
Joar Skalse and Alessandro Abate. Partial identifiability and misspecification in inverse reinforcement
learning. arXiv, 2024. arXiv:2411.15951. (Cited on page 7.)
John Maynard Smith and E¨ors Szathm´ary. The Major Transitions in Evolution. Oxford University
Press, 2020. Previously issued in print: Oxford : W.H. Freeman/Spektrum, 1995; Oxford: Oxford
University Press, 1997. - Includes bibliographical references and index. - Description based on
print version record and publisher information. (Cited on page 19.)
Oliver Sourbut, Lewis Hammond, and Harriet Wood. Cooperation and control in delegation games.
In International Joint Conference on Artificial Intelligence, 2024. (Cited on page 19.)
Claudia Szabo and Yong Meng Teo. Formalization of weak emergence in multiagent systems. ACM
Transactions on Modeling and Computer Simulation, 26(1):1–25, 2015. (Cited on page 19.)
Steven Tadelis. Game theory: an introduction. Princeton University Press, 2013. (Cited on page 27.)
Yong Meng Teo, Ba Linh Luong, and Claudia Szabo. Formalization of emergence in multi-agent
systems. In Proceedings of the 1st ACM SIGSIM Conference on Principles of Advanced Discrete
Simulation, 2013. (Cited on page 20.)
Raimo Tuomela. Joint intention, we-mode and I-mode. Midwest Studies in Philosophy, 30(1):35–58,
2006. (Cited on pages 3 and 18.)
Francis Rhys Ward, Matt MacDermott, Francesco Belardinelli, Francesca Toni, and Tom Everitt.
The reasons that agents act: Intention and instrumental goals. In International Conference on
Autonomous Agents and Multiagent Systems, 2024. (Cited on page 19.)
17
JØRGENSEN WEICHWALD HAMMOND
Michael P. Wellman, Karl Tuyls, and Amy Greenwald. Empirical game theoretic analysis: A survey.
Journal of Artificial Intelligence Research, 82, 2025. (Cited on page 30.)
Kevin Xia and Elias Bareinboim. Neural causal abstractions. In AAAI Conference on Artificial
Intelligence, 2024. (Cited on page 6.)
Dylan Xu and Juan-Pablo Rivera. Towards measurin
```
