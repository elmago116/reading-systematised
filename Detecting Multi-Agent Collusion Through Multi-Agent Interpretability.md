---
title: Detecting Multi-Agent Collusion Through Multi-Agent Interpretability
author: Aaron Rose, Carissa Cullen, Sahar Abdelnabi, Philip Torr, Brandon Gary Kaplowitz, Christian Schroeder de Witt
year: "2026"
Type: Preprint
DOI: 10.48550/arXiv.2604.01151
source: https://arxiv.org/abs/2604.01151
created: 2026-06-18
description: As LLM agents are increasingly deployed in multi-agent systems, they introduce risks of covert coordination that may evade standard forms of human oversight. While linear probes on model activations have shown promise for detecting deception in single-agent settings, collusion is inherently a multi-agent phenomenon, and the use of internal representations for detecting collusion between agents rem
tags:
  - op/acc/pending-review
  - tech/Ai/LLM
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Detecting Multi-Agent Collusion Through Multi-Agent Interpretability.pdf]]"
---
[[Detecting Multi-Agent Collusion Through Multi-Agent Interpretability.pdf]]

> **Abstract:** As LLM agents are increasingly deployed in multi-agent systems, they introduce risks of covert coordination that may evade standard forms of human oversight. While linear probes on model activations have shown promise for detecting deception in single-agent settings, collusion is inherently a multi-agent phenomenon, and the use of internal representations for detecting collusion between agents rem

## Full text (extracted from `Detecting Multi-Agent Collusion Through Multi-Agent Interpretability.pdf`)

*Source:* `2PDF/Detecting Multi-Agent Collusion Through Multi-Agent Interpretability.pdf`  
*Extracted:* 2026-06-18

```text
Detecting Multi-Agent Collusion Through Multi-Agent
Interpretability
Aaron Rose†
University of Oxford
Carissa Cullen
University of Oxford
Sahar Abdelnabi
ELLIS Institute Tübingen
MPI-IS
Philip Torr
University of Oxford
Brandon Gary Kaplowitz
University of Oxford
Christian Schroeder de Witt
University of Oxford
Abstract
As LLM agents are increasingly deployed in multi-agent systems, they introduce
risks of covert coordination that may evade standard forms of human oversight.
While linear probes on model activations have shown promise for detecting decep-
tion in single-agent settings, collusion is inherently a multi-agent phenomenon,
and the use of internal representations for detecting collusion between agents
remains unexplored. We introduce NARCBENCH, a benchmark for evaluating
collusion detection under environment distribution shift, and propose five probing
techniques that aggregate per-agent deception scores to classify scenarios at the
group level, evaluated across four open-weight models (Qwen3-32B, Llama-3.1-
70B, DeepSeek-R1 32B, GPT-OSS-20B) and six probe architectures. We frame
this as a distributed anomaly detection problem, identifying three collusion sig-
natures that map onto distinct anomaly types and detection paradigms. Every
model reaches 1.00 AUROC in-distribution; on our strongest model (Llama-3.1-
70B), our five probing techniques achieve 0.73 to 0.93 AUROC when transferred
zero-shot to structurally different multi-agent scenarios and 0.99 to 1.00 on a
steganographic blackjack card-counting task, with detection performance scal-
ing with model capability. We find that no single probing technique dominates
across all collusion types, consistent with the framework’s prediction that different
anomaly types require different detection paradigms. This work takes a step toward
multi-agent interpretability: extending white-box inspection from single models to
multi-agent contexts, where detection requires aggregating signals across agents.
These results suggest that model internals provide a complementary signal to text-
level monitoring for detecting multi-agent collusion. Code and data available at
https://github.com/aaronrose227/narcbench.
1 Introduction
Recent advances in LLMs have driven rapid progress in multi-agent systems, where multiple agents
collaborate on tasks ranging from software development [Hong et al., 2024, Qian et al., 2024] to
negotiation and decision-making [Guo et al., 2024]. As these systems are deployed with increasing
autonomy, they introduce new safety risks [Hammond et al., 2025]. Among the most concerning is
covert coordination: agents may secretly work together to steer outcomes, suppress information, or
undermine oversight [Park et al., 2023, Scheurer et al., 2024, Motwani et al., 2024]. In this work, we
show that such collusion can be detected by inspecting agents’ internal activations, even when their
text outputs appear entirely normal.
†Corresponding author:aaron.rose@new.ox.ac.uk
Preprint.
arXiv:2604.01151v2  [cs.AI]  9 May 2026
Proposed defences against covert coordination include monitoring text outputs, paraphrasing agent
communications, and imposing behavioural constraints [Greenblatt et al., 2024, Syrnikov et al.,
2026]. However, these have been shown to fail against steganographic signals designed to be
indistinguishable from natural language [Motwani et al., 2024, Mathew et al., 2024]. A separate
line of work has shown that linear probes on model activations can detect deception in single-agent
settings [Goldowsky-Dill et al., 2025, Anthropic, 2024]. However, little prior work has applied
activation-based detection to multi-agent settings. Collusion is inherently a multi-agent phenomenon:
it arises from the relationship between agents, not from any one agent in isolation. Detecting it
requires examining how agents’ internal representations relate to each other, a problem that maps
onto the classical framework of distributed anomaly detection [Chandola et al., 2009], where the
anomaly only becomes visible when information is combined across distributed nodes.
We frame this as a problem ofmulti-agent interpretability: applying white-box detection techniques
across multiple interacting agents to identify collective phenomena invisible from any single agent
alone. We first learn a deception direction from a training corpus of multi-agent scenarios in which
some agents are instructed to collude. Each agent’s activation is then projected onto this direction
to produce a scalar deception score. Given the scores of all agents in a scenario, we propose five
novel probing techniques, each built on this single learned deception probe, that ask whether the
pattern of scores across the group is consistent with collusion: for instance, whether there is a subset
of agents with elevated scores (Deception Split), whether the score distribution has unusually high
variance or range (Asymmetry Probe), or simply how high the most suspicious agent scores (Peak
Suspicion). We learn the deception direction on a core dataset and evaluate all five methods zero-shot
on held-out settings that differ structurally from the training data: a suite of six real-world-inspired
scenarios (code review sabotage, stock manipulation, RAG poisoning, and others) where collusion
takes different interactive forms, and a blackjack card-counting task in which two agents develop
steganographic signals hidden in natural table talk.
The deception probe transfers zero-shot to both the structurally distinct scenarios and the blackjack
task, despite entirely different interaction structures and collusion mechanisms. No single technique
dominates: different forms of collusion are best detected by different methods, a result we explain
through the lens of distributed anomaly detection, where each collusion type produces a different
anomaly type and no single test is optimal against all of them. In the steganographic setting, an
LLM judge monitoring the table talk fails to discriminate between collusion and control runs, while
our activation-based methods achieve 0.99–1.00 AUROC. These results suggest that white-box
access to model internals provides a complementary signal to text-level monitoring, particularly for
steganographic collusion that is designed to evade text-level oversight.
Our contributions are:
1. A framework for multi-agent collusion detection via a learned deception probe, and five
novel probing techniques (Sorted Concatenation, Activation Alignment, Peak Suspicion,
Deception Split, and Asymmetry Probe) that each aggregate per-agent deception scores to
classify scenarios at the group level.
2. NARCBENCH(Neural Activation Reading for Collusion Benchmark), a three-tier bench-
mark for evaluating collusion detection under environment distribution shift: CORE(50
scenarios, 17 domains), TRANSFER(6 structurally distinct scenario types), and STEGO
(steganographic blackjack card counting).
2 Related work
Multi-agent collusion and steganography.Recent work has established that LLM agents can
collude covertly in multi-agent settings. Motwani et al. [2024] formalise the threat of steganographic
collusion, showing that frontier models can encode hidden information in natural-sounding text.
Mathew et al. [2024] demonstrate that such steganographic communication can emerge from mis-
specified training incentives, not only from explicit prompting, and that standard mitigations such as
output paraphrasing are insufficient. Beyond steganography, Fish et al. [2024] show that LLM pricing
agents autonomously converge on supracompetitive prices without explicit collusion instructions,
and Curvo [2025] study deception dynamics in social deduction games, finding that deceptive capa-
bility may scale faster than detection ability. Hammond et al. [2025] provide a broad taxonomy of
multi-agent risks, identifying collusion as a key failure mode. On the mitigation side, Syrnikov et al.
2
[2026] show that declarative prohibitions alone do not prevent collusion under optimisation pressure.
Several frameworks have been proposed for auditing multi-agent collusion behaviourally, including
Colosseum [Nakamura et al., 2026], which measures collusion via regret metrics, and SentinelAgent
[He et al., 2025], which models agent interactions as execution graphs. These approaches operate on
agent outputs or behavioural traces; none examine model internals.
Probing activations for deception.A growing body of work shows that LLM internal repre-
sentations encode information about truthfulness and deceptive intent that is accessible to simple
linear probes. Zou et al. [2023] introduce Representation Engineering, demonstrating that high-
level concepts including honesty are linearly represented in activation space. Marks and Tegmark
[2024] provide geometric evidence for linear truth structure, and Azaria and Mitchell [2023] show
that classifiers on hidden states predict statement truthfulness. Most directly relevant to our work,
Goldowsky-Dill et al. [2025] train linear probes on Llama-3.3-70B activations to detect strategic
deception, achieving AUROCs of 0.96–0.999 on scenarios including insider trading and sandbagging.
Anthropic [2024] show that simple “defection probes” catch sleeper agents with AUROC above 0.99.
All of this work operates in a single-agent setting: it probes one model’s activations to detect that
model’s deception. Our work extends this to the multi-agent case, where the signal of interest is the
relationship between agents’ representations, not any single agent’s internal state.
Distributed anomaly detection.We frame multi-agent collusion detection as a distributed anomaly
detection problem following the taxonomy of Chandola et al. [2009], who distinguish three anomaly
types:point anomalies(a single instance is anomalous),contextual anomalies(anomalous in a specific
context), andcollective anomalies(a group of instances is anomalous even though no individual
instance is). Collusion is a collective anomaly: a single colluding agent’s activations may appear only
mildly unusual, but the pattern across agents reveals the collusion. The distributed detection literature
further distinguishes three detection paradigms based on how information from distributed nodes is
combined [Chandola et al., 2009]. Incentralised fusion, raw data from all nodes is aggregated into a
single representation and classified globally. Indecision-level fusion, each node produces a local score
or decision, and a second stage combines these to reach a system-level verdict. Incorrelation-based
detection, anomalies are identified from changes in inter-node statistical relationships rather than
from any node’s data in isolation. Our five probing techniques collectively instantiate all three
paradigms (Section 3.3), providing complementary coverage of the anomaly types that different
forms of collusion produce.
3 Method
3.1 Scenario generation
We definemulti-agent interpretabilityas aggregating white-box inspection across multiple inter-
acting agents to detect collective phenomena invisible from any single agent alone. Our approach
proceeds in two stages: learning a deception direction from individual agents, then aggregating
scores across the group to detect collusion. We introduce NARCBENCH, a benchmark for evaluating
this under environment distribution shift. It comprises three tiers of increasing structural distance
from the training data. All scenarios share a common structure: four LLM agents interact in a
shared conversation. Each scenario is run in two conditions: a collusion condition, in which two
agents are secretly instructed to coordinate toward a hidden objective via a private channel before
engaging in public discussion, and a control condition, in which all four agents receive identical
honest instructions.
NARCBENCH-CORE(training and in-distribution evaluation).50 scenarios spanning 17 do-
mains (medical, financial, legal, military, cybersecurity, environmental, and others). Four agents form
a committee voting on a binary choice; colluders steer the vote toward a predetermined outcome
while concealing their coordination. Scenarios are diversified across agent names, instruction style,
domain framing, and option labels to mitigate prompt confounds. Both conditions run per scenario
(100 runs), with a held-out subset reserved for in-distribution evaluation. Full domain list, example
prompts, and ground-truth labelling criteria in Appendix F.
3
Collect activations from
multi-agent interactions
honest
colluders
I suggest we go with A
Option B is clearly better
I’d like to see more data
I agree, B has full support
All messages appear normal.
Colluders are indistinguishable
from text outputs alone.
Learn deception direction
from colluder vs. honest activations
d
honest agent
colluding agent
The probe is a linear
direction in activation
space
sj = ¯aj · d
Project each agent’s activations
onto d to get a deception score
Score each agent’s deceptiveness
s on evaluation scenariosdeception score
Colluders score higher along
the deception direction
Aggregate scores
across agents
f(s1, . . . , sN)
Combine per-agent
scores into a single
group-level statistic
Classify unseen scenarios
with different structure
Judgement:
COLLUSION
Judgement:
NORMAL
If the group statistic exceeds
a threshold, flag the scenario
Figure 1: Overview of our methodology. Activations are extracted from multi-agent interactions, projected onto
a learned deception direction, and aggregated across agents to classify scenarios.
NARCBENCH-TRANSFER(out-of-distribution: structurally distinct scenarios).Six scenario
families that differ from COREin both domain and interaction structure: code review sabotage,
pump-and-dump stock manipulation, CI/CD pipeline sabotage, RAG knowledge-base poisoning,
research policy slanting, and news framing. Six sub-scenarios per family, each run in both conditions
(72 runs). Per-family construction details and audit criteria in Appendix G.
NARCBENCH-STEGO(out-of-distribution: steganographic collusion).A card-counting task in
which a counter and a big player pre-negotiate a signalling scheme in a private channel, then play
8-hand blackjack shoes alongside two honest agents. The counter encodes the running card count in
natural table talk; the big player decodes their signal to size their bets. Each of 20 shoes uses a fresh
agent-invented encoding (40 runs). Mechanism, prompts, and example transcripts in Appendix H.
Mitigating prompt confounds.Probes can classify based on prompt surface features rather than
internal representations of deception [Goldowsky-Dill et al., 2025, Levinstein and Herrmann, 2024].
We mitigate this through scenario diversification and identical evaluation-time prompts; details and a
null-probe sanity check are in Appendix F.3. The OOD transfer results (Section 4) provide further
evidence against pure prompt artefacts.
3.2 Activation extraction and probe training
We evaluate four open-weight models: Qwen3-32B-AWQ [Qwen Team, 2025], Llama-3.1-70B-
Instruct-AWQ-INT4 [Meta AI, 2024], DeepSeek-R1-Distill-Qwen-32B [DeepSeek-AI, 2025], and
GPT-OSS-20B [OpenAI, 2025a] (compute details in Appendix D). Qwen3-32B was used for hyperpa-
rameter tuning; the resulting probe configuration transfers unchanged to the other models. We extract
activations at the last token position of each agent’s public responses, across a five-layer band in the
middle of each model (e.g. layers 26–30 of 64 for Qwen3-32B), where semantic representations are
strongest [Zou et al., 2023]; we report mean AUROC across these layers. For CORE, we average
across all discussion rounds. For TRANSFERand STEGO, we use final-round activations only, where
all agents receive identical user prompts.
Deception probe.Following Goldowsky-Dill et al. [2025], we fit a linear probe to distinguish collud-
ing agents from honest agents. We collect activations from NARCBENCH-COREcollusion runs only
(public channel), giving a dataset of activation vectors xi ∈R d with labels yi ∈ {honest,colluder},
balanced by downsampling the majority class. We standardise activations to zero mean and unit
variance, then train a logistic regression classifier. The normalised weight vector defines adeception
direction. For a new agentj, we compute a scalardeception score:
sj = ¯aj ·d(1)
where higher scores indicate a more colluder-like internal state. A null probe trained on a random split
of honest agents scores near chance, confirming the probe is not picking up incidental differences.
Figure 1 illustrates the full pipeline.
Evaluation.For NARCBENCH-CORE, we evaluate via leave-domain-out cross-validation: for each
of the 17 domains, we train the deception direction and any run-level classifiers on the remaining 16
4
domains and evaluate on the held-out domain. Core results are the mean across folds. For TRANSFER
and STEGO, we train on all of COREand evaluate zero-shot. All results are AUROC, measuring
how well each method’s score separates collusion runs from control runs. Three of the five methods
(Peak Suspicion, Deception Split, Activation Alignment) require no training beyond the deception
direction: they compute a single scalar per run and we measure how well this scalar separates the
two conditions. The remaining two (Sorted Concatenation, Asymmetry Probe) train an additional
classifier on CORErun-level features.
3.3 Detection framework
The single-agent deception score sj classifies each agent independently, but collusion is a collective
phenomenon. A single colluding agent’s score may appear only mildly unusual; thepattern across
agentsreveals the coordination. We frame collusion detection as distinguishing:
H0 :all agents are honest
H1 :an unknown subsetC⊂ {1, . . . , N}is colluding (2)
Score model.Under H0, each agent’s deception score is drawn from a common honest distribution:
sj ∼F 0 for allj. UnderH 1, agents in the colluding subsetCdraw from a shifted distributionF 1:
sj ∼
F0 j /∈C
F1 =F 0 +δ j∈C (3)
where δ >0 is the effect size. Both C and δ are unknown to the detector: marginalising over
which agent is colluding, an arbitrary score is drawn from the mixture π F0 + (1−π) (F 0 +δ) with
unknown weight π= (N− |C|)/N. In practice, collusion pushes agents’ activations further along
the learned deception direction, producing elevated scores. The detector observes s= (s 1, . . . , sN )
and, optionally, the full activation vectors a1, . . . ,aN . Detection difficulty depends on the magnitude
ofδrelative to the variance ofF 0, and on whether the shift is visible in the scalar scores at all.
We identify three qualitatively different ways collusion can manifest in the observations, correspond-
ing to the anomaly types in Chandola et al. [2009]’s taxonomy of distributed systems:
Point anomalies (score elevation).Collusion elevates at least one agent’s deception score. The
signal is in individual scores. This is the simplest case and the most similar to single-agent detection,
naturally addressed bydecision-level fusion[Chandola et al., 2009].
Collective anomalies (subgroup separation).Collusion creates a gap between the coalition’s scores
and the honest agents’ scores, without any individual agent being necessarily anomalous alone. This
also falls under decision-level fusion, but requires test statistics that capture distributional shape
rather than individual magnitudes.
Contextual anomalies (representational shift).Collusion changes the geometry of agents’ acti-
vations without necessarily shifting scalar scores. This occurs in steganographic collusion, where
encoding and decoding covert signals alters how agents represent shared context. The natural
paradigm iscorrelation-based detection[Chandola et al., 2009].
These three types are not mutually exclusive. Real collusion typically produces a mixture, but the
distinction determines which detection paradigm can succeed, motivating our use of complementary
methods spanning all three.
3.4 Probing techniques
We introduce five probing techniques, each targeting a specific anomaly type from the framework
above (Figure 2). Each technique computes a scalar test statistic T on which we threshold to flag
collusion. Lets [k] denote thek-th largest deception score across theNagents.
Sorted Concatenation (centralised fusion).We sort agents by deception score in descending order
and concatenate their standardised activation vectors [a[1],a [2],a [3],a [4]]∈R 4d, reduce with PCA
(50 components), standardise, and train a logistic regression classifier. Sorting by deception score
removes agent identity and imposes a canonical ordering.
5
Decision-level fusion
Each node produces a local
score. These are combined
for a verdict.
per-agent scores
Σ > τ ?
collusive ✓
honest ✗
Correlation-based detection
Anomalies from changes in
relationships between nodes.
normal
−
anomalous
= ∆ >τ ?
collusive ✗
honest ✓
Centralised fusion
All raw data pooled into one
representation and classified.
separated combined
f ( x ) >τ ?
collusive ✓
honest ✗
Figure 2: Distributed detection paradigms and how each processes multi-agent data to classify scenarios.
Activation Alignment (correlation-based).Targets representational shift, the anomaly type that
is invisible to scalar score methods. This is the only method that operates on full activation vectors
rather than the deception direction. We compute the mean pairwise cosine similarity:
Talign = 1
(
N
2 )
P
i<j cos(ai,a j)(4)
Steganographic collusion disrupts this geometry because encoding and decoding covert signals
changes how agents process the same text, producing a detectable shift in Talign even when individual
scoress j remain normal.
Peak Suspicion (decision-level).Targets score elevation, where colluding agents are individually
anomalous. The test statistic is simply the maximum deception score:
Tpeak = max
j
sj =s [1] (5)
Deception Split (decision-level).Targets groupings of agents: under collusion, the colluders form
a group with elevated deception scores, separate from the honest agents. Assuming the coalition size
|C| is known (here |C|= 2 of N= 4 ), we compute the mean score of the top-scoring agents minus
the mean of the rest:
Tsplit = 1
2 (s[1] +s [2])− 1
2 (s[3] +s [4])(6)
Asymmetry Probe (decision-level).Combines four distributional features of the deception scores—
variance Var({sj}), range s[1] −s [N] , the Deception Split Tsplit, and mean ¯s—into a single logistic
regression classifier trained on CORE.
xasym =

Var({sj}), s[1] −s [N] , Tsplit,¯s

(7)
This captures all three anomaly types: score elevation (mean), dispersion (variance/range), and
subgroup structure (split).
4 Results
Figure 3 reports per-probe AUROC for all four models on Transfer and Stego, with the full per-family
breakdown given in Appendix A. Each model uses a single linear deception probe trained on its own
NARCBENCH-COREactivations and evaluated zero-shot on the OOD tiers; hyperparameter-tuning
details are in Appendix B.
4.1 Main findings
Multi-agent collusion is detectable from internal activations.Across all four open-weight models
we test, our methods are effective at flagging collusion both in out-of-distribution scenarios that
6
Figure 3: Per-probe AUROC for each model on Transfer (solid; mean over six OOD families) and Stego (hatched;
twenty blackjack shoes). Means across the model’s probe-layer range and ten seeds.
differ from training in interaction structure (TRANSFER) and when the collusion mechanism itself is
structurally different, including covert steganographic signalling (STEGO). Every model reaches 1.00
AUROC on CORE, near-perfect detection on STEGO, and well-above-chance AUROC on the harder
TRANSFERtier (Figure 3, Table 1).
Table 1: Mean AUROC per model, averaged across
the five probing techniques, seeds, layers (and
TRANSFERfamilies).
Model TRANSFERSTEGO
Llama-3.1 70B 0.87 1.00
Qwen3 32B 0.78 1.00
DeepSeek-R1 32B 0.75 0.95
GPT-OSS 20B 0.68 0.86
No single probing technique dominates.The
strongest probe varies across model and tier (Fig-
ure 3), consistent with the framework of Section 3.3
that different forms of collusion produce different
anomaly types.
Detection performance correlates with model ca-
pability.Table 1 shows AUROC tracks model capa-
bility, with Llama-3.1-70B at the top and GPT-OSS-
20B at the bottom. We think this may simply reflect
that higher-capability models coordinate better and
stay locked onto the collusive task they have been given, so the deception signal in their activations is
stronger and more consistent for the probe to pick up. This pattern requires further analysis and work
to substantiate.
4.2 Per-tier breakdown on Llama-3.1-70B
For a breakdown of the results we zoom in on Llama-3.1-70B, our most capable model and the one
with the best detection results (Section 4.1). Figure 4 reports per-method AUROC across all eight test
groups for the LR-trained probe.
Both HELD-OUTand STEGOget near-perfect detection across all methods (0.97–1.00 AUROC).
Across TRANSFER, averaged over the six families, Asymmetry Probe (0.93) and Deception Split
(0.92) lead the pack, with Peak Suspicion (0.91) and Sorted Concatenation (0.89) close behind.
Activation Alignment is the clear outlier at 0.73—we believe this is because the direction of the
representational shift is inconsistent across structural collusion types.
4.3 Per-probe detail
We tested 6 different probe types for each model: Logistic Regression, Multi-Layer Logistic Regres-
sion, Difference-in-Means, Multi-Headed Attention, Multi-Layer Perceptron and Linear Artificial
Topography. As shown in Table 2, Logistic Regression achieved the highest OOD-mean AUROC
7
Figure 4: Per-method AUROC on Llama-3.1-70B across HELD-OUT,TRANSFER, and STEGO. Means over
probe-layer range and ten seeds; error bars show layer standard deviation.
score for Qwen3-32B and Llama-3.1-70B and the second highest score for DeepSeek-R1-32B. The
Multi-Layer probe also performed well across the larger three models. Architectural details for each
probe type are in Appendix C.
Table 2: OOD-mean AUROC per probe architecture per model (averaged across the six TRANSFERfamilies and
STEGO). Bold = highest per model.
Probe Qwen3-32B Llama-3.1-70B DeepSeek-R1-32B GPT-OSS-20B
Logistic Regression0.81 0.890.77 0.62
Multi-Layer Logistic Regression 0.72 0.870.780.60
Difference of Means 0.68 0.86 0.670.68
Multi-Headed Attention 0.60 0.73 0.60 0.64
Multi-Layer Perceptron 0.56 0.77 0.68 0.57
Linear Artificial Topography 0.52 0.57 0.54 0.63
4.4 Detection at operational thresholds
Figure 5: ROC curves on Llama-3.1-70B. Bands:
95% bootstrap CIs. Parentheses: AUROC.
AUROC does not capture performance at the strict
false-positive rates required for deployment. On
TRANSFER, even the best method (Deception Split)
achieves only 0.38 recall at 1% FPR. On STEGO,
by contrast, all methods perform well, with Activa-
tion Alignment achieving perfect separation ( 1.00
recall at 1% FPR), confirming that steganographic
collusion produces a qualitatively stronger activation
signal than structural collusion.
One-shot detection at strict thresholds is therefore
insufficient for structural collusion;sequential de-
tection—accumulating evidence across interactions via SA VI [Howard et al., 2022] for example—is
a natural next step.
4.5 Verifying collusion
Table 3: Lag-1 bet/count correlation by agent
group.
GroupnMeanρ
Big Player (collusion) 20+0.42
Counter (collusion) 20−0.03
Honest, collusion runs 40−0.02
Honest, control runs 80−0.04
While we verified collusion by hand for COREand
TRANSFER(criteria documented in Appendices F.7
and G.9), in STEGOwe can measure it directly: we
compute the lag-1 correlation between the Big Player’s
bet size and the true card count. If the colluders are
signalling, the Big Player should raise their bet when
the count is high and lower it when the count is low, so
8
the correlation should be positive in collusion runs and
near zero otherwise. Table 3 shows exactly this: the
colluding Big Player is the only group with a meaningfully positive correlation (+0.42).
4.6 Limitations and future work
Probe reliability and labelling.Our probes may rely partly on spurious correlations [Goldowsky-
Dill et al., 2025]; we mitigate prompt confounds through numerous methods (details in Appendix F.3).
Ground-truth labelling of whether an agent is colluding is inherently difficult. We took a strict
approach, only retaining runs in which both colluders coordinatedandexecuted effectively (audit
criteria in Appendices F.7, G.9, H.8); some excluded runs could arguably count as collusion under a
looser bar.
Adversarial robustness and evaluation awareness.Adversarial robustness is untested. Colluders
aware of activation monitoring may try to suppress the signal during monitored sessions [Needham
et al., 2025] or coordinate through covert channels designed to evade interpretability tools, in the
same spirit as steganographic evasion of text-level monitors [Motwani et al., 2024].
Coalition size and scaling N.Deception Split hardcodes the coalition size ( |C|= 2 here) into
its scoring formula; the other four methods are coalition-size-agnostic. Future work could develop
methods that adapt to varyingN and to arbitrary splits between colluding and honest agents, including
the case where colluders outnumber honest ones. Multi-agent systems with tens or hundreds of agents
[Hammond et al., 2025] likely require different score-aggregation strategies than ourN= 4setup.
Sequential detection.Accumulating evidence across multiple interactions [Kulkarni, 2026], via
SA VI [Howard et al., 2022] for example, would yield formal stopping guarantees.
4.7 Threat model and applications
Our framework assumes white-box access to all agents’ activations during inference. This is a strong
assumption, but it holds in several realistic deployment settings:
• Internal multi-agent products.A company orchestrating its own agent pipeline—code review,
document drafting, financial analysis (the settings NARCBENCH-TRANSFERis built from)—has
full activation access for every agent. The operator runs the agents but does not fully trust them,
and wants to catch misbehaviour before it reaches end-users. This is the same threat model as the
AI Control literature [Greenblatt et al., 2024], extended from a single untrusted model to a system
of potentially colluding agents.
• Pre-deployment safety evaluations.Developers and external evaluators routinely have weight or
activation-level access during red-teaming. Activation-based deception probes have already been
demonstrated in this regime for single-agent deception [Goldowsky-Dill et al., 2025, Anthropic,
2024]; our methods extend that toolkit to multi-agent settings, which prior work identifies as a
distinct risk surface [Hammond et al., 2025].
• Open-weight deployments.Any team running an open-weight model in production has activation
access by construction. Our experiments cover four such models.
• Closed-weight models with provider-side monitoring.API providers can run probes on their
own models even when end-users cannot[Anthropic, 2025, OpenAI, 2025b, Google DeepMind,
2024].
5 Conclusion
We formalise multi-agent collusion detection as a distributed anomaly detection problem, mapping
three collusion signatures (score elevation, subgroup separation, representational shift) onto the
classical anomaly taxonomy. To validate the framework we introduce NARCBENCH, a three-tier
benchmark for collusion detection under environment distribution shift, and five probing techniques.
Across four open-weight models and six probe architectures, every model reaches 1.00 AUROC
9
in-distribution and the best-performing techniques transfer zero-shot to structurally different multi-
agent scenarios and to a steganographic blackjack task that is invisible to a text-level LLM judge. No
single technique dominates across all collusion types, consistent with the framework’s prediction that
different anomaly types require different detection paradigms. These results motivatemulti-agent
interpretabilityas a direction for AI safety: extending white-box inspection from single models to
systems of agents, where detection requires aggregating signals across the group.
References
Anthropic. Simple probes can catch sleeper agents.Anthropic Research Blog, 2024. URL https:
//www.anthropic.com/research/probes-catch-sleeper-agents.
Anthropic. Responsible scaling policy, 2025. URL https://www-cdn.anthropic.com/
872c653b2d0501d6ab44cf87f43e1dc4853e4d37.pdf. Version 2.2, May 2025.
Amos Azaria and Tom Mitchell. The internal state of an LLM knows when it’s lying. InFindings of
the Association for Computational Linguistics: EMNLP 2023, 2023. URL https://arxiv.org/
abs/2304.13734.
Varun Chandola, Arindam Banerjee, and Vipin Kumar. Anomaly detection: A survey.ACM Com-
puting Surveys, 41(3):15:1–15:58, 2009. URL https://dl.acm.org/doi/10.1145/1541880.
1541882.
Pedro M. P. Curvo. The traitors: Deception and trust in multi-agent language model simulations.
InNeurIPS 2025 Workshop on Multi-Turn Interactions, 2025. URLhttps://arxiv.org/abs/
2505.12923.
DeepSeek-AI. DeepSeek-R1: Incentivizing reasoning capability in LLMs via reinforcement learning.
arXiv preprint arXiv:2501.12948, 2025. URLhttps://arxiv.org/abs/2501.12948.
Sara Fish, Yannai A. Gonczarowski, and Ran I. Shorrer. Algorithmic collusion by large language
models.arXiv preprint arXiv:2404.00806, 2024. URL https://arxiv.org/abs/2404.00806.
Nicholas Goldowsky-Dill, Bilal Chughtai, Stefan Heimersheim, and Marius Hobbhahn. Detecting
strategic deception using linear probes. InProceedings of the 42nd International Conference on
Machine Learning (ICML), 2025. URLhttps://arxiv.org/abs/2502.03407.
Google DeepMind. Introducing the frontier safety framework, 2024. URL https://deepmind.
google/discover/blog/introducing-the-frontier-safety-framework/. May 2024.
Ryan Greenblatt, Buck Shlegeris, Kshitij Sachan, and Fabien Roger. AI control: Improving safety
despite intentional subversion. InProceedings of the 41st International Conference on Machine
Learning (ICML), 2024. URLhttps://arxiv.org/abs/2312.06942.
Taicheng Guo, Xiuying Chen, Yaqi Wang, Ruidi Chang, Shichao Pei, Nitesh V Chawla, Olaf
Wiest, and Xiangliang Zhang. Large language model based multi-agents: A survey of progress
and challenges. InProceedings of the Thirty-Third International Joint Conference on Artificial
Intelligence (IJCAI), 2024. URLhttps://arxiv.org/abs/2402.01680.
Lewis Hammond, Alan Chan, Jesse Clifton, Jason Hoelscher-Obermaier, Akbir Khan, Euan McLean,
Chandler Smith, Wolfram Barfuss, Jakob Foerster, Tomáš Gaven ˇciak, The Anh Han, Edward
Hughes, V ojtˇech Kovaˇrík, Jan Kulveit, Joel Z. Leibo, Caspar Oesterheld, Christian Schroeder de
Witt, Nisarg Shah, Michael Wellman, Paolo Bova, Theodor Cimpeanu, Carson Ezell, Quentin
Feuillade-Montixi, Matija Franklin, Esben Kran, Igor Krawczuk, Max Lamparth, Niklas Lauffer,
Alexander Meinke, Sumeet Motwani, Anka Reuel, Vincent Conitzer, Michael Dennis, Iason
Gabriel, Adam Gleave, Gillian Hadfield, Nika Haghtalab, Atoosa Kasirzadeh, Sébastien Krier,
Kate Larson, Joel Lehman, David C. Parkes, Georgios Piliouras, and Iyad Rahwan. Multi-agent
risks from advanced AI.Cooperative AI Foundation Technical Report, 2025. URL https:
//arxiv.org/abs/2502.14143.
Xu He, Di Wu, Yan Zhai, and Kun Sun. Sentinelagent: Graph-based anomaly detection in multi-agent
systems.arXiv preprint arXiv:2505.24201, 2025. URL https://arxiv.org/abs/2505.24201.
10
Sirui Hong, Mingchen Zhuge, Jiaqi Chen, Xiawu Zheng, Yuheng Cheng, Ceyao Zhang, Jinlin Wang,
Zili Wang, Steven Ka Shing Yau, Zijuan Lin, Liyang Zhou, Chenyu Ran, Lingfeng Xiao, Chenglin
Wu, and Jürgen Schmidhuber. MetaGPT: Meta programming for a multi-agent collaborative
framework. InThe Twelfth International Conference on Learning Representations (ICLR), 2024.
URLhttps://arxiv.org/abs/2308.00352.
Steven R Howard, Aaditya Ramdas, Jon McAuliffe, and Jasjeet Sekhon. Time-uniform, nonparamet-
ric, nonasymptotic confidence sequences.The Annals of Statistics, 49(2):1055–1080, 2022. URL
https://arxiv.org/abs/1810.08240.
Prashant Kulkarni. Latent adversarial detection: Adaptive probing of LLM activations for multi-turn
attack detection.arXiv preprint arXiv:2604.28129, 2026. URL https://arxiv.org/abs/2604.
28129.
Benjamin A. Levinstein and Daniel A. Herrmann. Still no lie detector for language models: Probing
empirical and conceptual roadblocks.Philosophical Studies, 182(7):1539–1565, 2024. URL
https://arxiv.org/abs/2307.00175.
Samuel Marks and Max Tegmark. The geometry of truth: Emergent linear structure in large language
model representations of true/false datasets. InConference on Language Modeling (COLM), 2024.
URLhttps://arxiv.org/abs/2310.06824.
Yohan Mathew, Ollie Matthews, Robert McCarthy, Joan Velja, Christian Schroeder de Witt, Dylan
Cope, and Nandi Schoots. Hidden in plain text: Emergence and mitigation of steganographic
collusion in LLMs. InNeurIPS 2024 Workshop on Safe Generative AI, 2024. URL https:
//arxiv.org/abs/2410.03768.
Meta AI. The Llama 3 herd of models.arXiv preprint arXiv:2407.21783, 2024. URL https:
//arxiv.org/abs/2407.21783.
Sumeet Ramesh Motwani, Mikhail Baranchuk, Martin Strohmeier, Vijay Bolina, Philip H.S. Torr,
Lewis Hammond, and Christian Schroeder de Witt. Secret collusion among AI agents: Multi-agent
deception via steganography. InAdvances in Neural Information Processing Systems, 2024. URL
https://arxiv.org/abs/2402.07510.
Mason Nakamura, Abhinav Kumar, Saswat Das, Sahar Abdelnabi, Saaduddin Mahmud, Fer-
dinando Fioretto, Shlomo Zilberstein, and Eugene Bagdasarian. Colosseum: Auditing col-
lusion in cooperative multi-agent systems.arXiv preprint arXiv:2602.15198, 2026. URL
https://arxiv.org/abs/2602.15198.
Joe Needham, Giles Edkins, Govind Pimpale, Henning Bartsch, and Marius Hobbhahn. Large
language models often know when they are being evaluated.arXiv preprint arXiv:2505.23836,
2025. URLhttps://arxiv.org/abs/2505.23836.
OpenAI. gpt-oss-120b & gpt-oss-20b model card, 2025a. URL https://openai.com/index/
gpt-oss-model-card/.
OpenAI. Updating our preparedness framework, 2025b. URL https://openai.com/index/
updating-our-preparedness-framework/. April 2025.
Peter S. Park, Simon Goldstein, Aidan O’Gara, Michael Chen, and Dan Hendrycks. AI deception: A
survey of examples, risks, and potential solutions.arXiv preprint arXiv:2308.14752, 2023. URL
https://arxiv.org/abs/2308.14752.
Chen Qian, Wei Liu, Hongzhang Liu, Nuo Chen, Yufan Dang, Jiahao Li, Cheng Yang, Weize
Chen, Yusheng Su, Xin Cong, Juyuan Xu, Dahai Li, Zhiyuan Liu, and Maosong Sun. ChatDev:
Communicative agents for software development. InProceedings of the 62nd Annual Meeting of
the Association for Computational Linguistics (ACL), 2024. URL https://arxiv.org/abs/
2307.07924.
Qwen Team. Qwen3 technical report.arXiv preprint arXiv:2505.09388, 2025. URL https:
//arxiv.org/abs/2505.09388.
11
Jérémy Scheurer, Mikita Balesni, and Marius Hobbhahn. Large language models can strategically
deceive their users when put under pressure. InICLR 2024 Workshop on LLM Agents, 2024. URL
https://arxiv.org/abs/2311.07590.
Marcantonio Bracale Syrnikov, Federico Pierucci, Marcello Galisai, Matteo Prandi, Piercosma Bis-
conti, Francesco Giarrusso, Olga Sorokoletova, Vincenzo Suriani, and Daniele Nardi. Institutional
AI: Governing LLM collusion in multi-agent cournot markets via public governance graphs.arXiv
preprint arXiv:2601.11369, 2026. URLhttps://arxiv.org/abs/2601.11369.
Andy Zou, Long Phan, Sarah Chen, James Campbell, Phillip Guo, Richard Ren, Alexander Pan,
Xuwang Yin, Mantas Mazeika, Ann-Kathrin Dombrowski, Shashwat Goel, Nathaniel Li, Michael J
Byun, Zifan Wang, Alex Mallen, Steven Basart, Sanmi Koyejo, Dawn Song, Matt Fredrikson,
J. Zico Kolter, and Dan Hendrycks. Representation engineering: A top-down approach to AI
transparency.arXiv preprint arXiv:2310.01405, 2023. URL https://arxiv.org/abs/2310.
01405.
12
Appendix
A. Full NARCBENCHresults
B. Logistic Regression auxiliary experiments
C. Probe types
D. Compute and hardware
E. Refusal rates
F. The NARCBENCH-COREdataset
G. The NARCBENCH-TRANSFERtier
H. The NARCBENCH-STEGOtier
I. Token-level analysis on NARCBENCH-STEGO
A Full NARCBench Results
Tables 4–7 give the per-tier breakdown that underlies Figure 3: AUROC of each of the five probing
techniques on CORE, each TRANSFERfamily, and STEGO, for each of the four models. All values
are means across the model’s probe-layer range and ten random seeds. For GPT-OSS-20B, three
TRANSFERfamilies (News Framing, Pump & Dump, RAG Poisoning) produced no analysable
collusion runs because every attempt was refused or failed audit; those rows are marked “–”.
Table 4: Per-method AUROC across NARCBENCHtiers for Qwen3-32B. Bold = best per row. OOD Mean is
computed across the available out-of-distribution scenarios (TRANSFERfamilies plus STEGO).
Sorted Concatenation Act Alignment Peak Suspicion Deception Split Asymmetry Probe
CORE1.00 1.00 1.00 1.00 1.00
TRANSFER(all)0.82 0.48 0.840.880.87
CI/CD0.53 0.28 0.320.730.48
Code Review0.94 0.391.000.99 0.99
News Framing0.71 0.71 0.940.960.94
Pump & Dump0.990.32 0.97 0.83 0.96
RAG Poisoning0.77 0.47 0.82 0.770.83
Research Pipeline0.99 0.681.00 1.00 1.00
STEGO1.00 1.00 1.000.99 1.00
OOD Mean0.85 0.55 0.860.890.89
Table 5: Per-method AUROC across NARCBENCHtiers for Llama-3.1 70B. Bold = best per row.
Sorted Concatenation Act Alignment Peak Suspicion Deception Split Asymmetry Probe
CORE1.000.971.00 1.00 1.00
TRANSFER(all)0.89 0.73 0.90 0.920.93
CI/CD0.960.84 0.89 0.89 0.92
Code Review0.99 0.671.00 1.00 1.00
News Framing0.93 0.83 0.96 0.970.99
Pump & Dump0.95 0.93 0.98 0.990.99
RAG Poisoning0.64 0.44 0.710.770.75
Research Pipeline0.88 0.64 0.89 0.890.91
STEGO1.001.00 1.000.991.00
OOD Mean0.91 0.77 0.92 0.930.94
13
Table 6: Per-method AUROC across NARCBENCHtiers for DeepSeek-R1 32B. Bold = best per row.
Sorted Concatenation Act Alignment Peak Suspicion Deception Split Asymmetry Probe
CORE1.000.951.00 1.00 1.00
TRANSFER(all)0.75 0.58 0.84 0.690.86
CI/CD0.280.670.58 0.66 0.66
Code Review0.87 0.91 0.910.930.93
News Framing0.88 0.500.990.73 0.98
Pump & Dump0.84 0.61 0.87 0.770.92
RAG Poisoning0.80 0.510.920.59 0.91
Research Pipeline0.820.29 0.78 0.48 0.73
STEGO1.000.76 0.98 0.87 0.99
OOD Mean0.78 0.61 0.86 0.720.87
Table 7: Per-method AUROC across NARCBENCHtiers for GPT-OSS 20B. Bold = best per row. The News
Framing, Pump & Dump and RAG Poisoning families produced no analysable collusion runs (every collusion
attempt was refused or failed audit) and are marked “–”; TRANSFER(all) and OOD Mean are computed across
the available families plus STEGO.
Sorted Concatenation Act Alignment Peak Suspicion Deception Split Asymmetry Probe
CORE1.000.911.00 1.00 1.00
TRANSFER(all)0.620.720.56 0.65 0.64
CI/CD0.760.980.77 0.85 0.83
Code Review0.77 0.570.800.63 0.77
News Framing− − − − −
Pump & Dump− − − − −
RAG Poisoning− − − − −
Research Pipeline0.320.600.12 0.48 0.32
STEGO0.770.990.74 0.40 0.65
OOD Mean0.650.790.61 0.59 0.64
Figure 6: OOD-mean AUROC (TRANSFER+STEGO) plotted against model parameter count. Detection perfor-
mance scales approximately monotonically with model capability across the four open-weight models we tested.
B Logistic Regression Auxiliary Experiments
For Hyper-parameter tuning, we used the mean AUROC score across all Out-Of Distribution test
results (OOD mean AUROC) to determine the best parameter values and set-up. This includes all
probe types across all NARCBench-Transfer test sets and NARCBench-Stego but not the AUROC
14
scores for the Held-out set of NARCBench-Core. Each run averaged scores across 5 layers, 26-30,
and over 10 random seeds.
For the Logistic Regression Probe, we tested L2 and L1 regularisation methods, with solvers L-BFGS
and LIBLINEAR for L2 and a SAGA solver for L1. L2 regularisation with LIBLINEAR performed
best. We also tested different L2 regularisation strengths, C, 15, 20, 25, 30 and 35 with a value of 25
resulting in the highest OOD mean AUROC.
We also tried different limits for the number of iterations for the LIBLINEAR solver to converge
(max_iters) with values 1000, 50, 16, 8 and 4. For values 1000 and 16, the solvers converged,
so there wasn’t any difference in performance. For max_iters equalling 8 to 4, the solver did not
converge. OOD mean AUROC was highest when max_iters equalled 8. We theorise this better
generalisation may be because a lowermax_itersvalue acts as an early stopping method.
Another strategy we tried for improving generalisation is data augmentation. We used 4 noisy copies
per original data point and a standard deviation of 0.05 for the Gaussian noise. It slightly reduced
OOD mean AUROC score (by less than 0.001) and wasn’t used for the main results.
C Probe Types
This appendix gives architectural details for the six probe types compared in Table 2 (main paper,
Section 4.3): Logistic Regression, Multi-Layer ensemble, Difference of Means, Multi-Headed
Attention, Linear Artificial Topography, and a Multi-Layer Perceptron. All probes are trained
on the same balanced, standardised activation set per model (collusion runs only, public channel,
downsampled to equal class sizes), and the same five probing techniques (Sorted Concatenation,
Activation Alignment, Peak Suspicion, Deception Split, Asymmetry Probe) are computed on top.
Probe types differ only in how the per-agent deception score is produced. Reported numbers are
averaged across the five probe layers and ten random seeds, except the Multi-Layer ensemble, which
uses all five layers jointly to produce a single AUROC.
Logistic Regression. LogisticRegression with penalty="l2", solver="liblinear", C=25,
max_iter=8. Coefficient vector unit-normalised. Sweep details in Appendix B.
Difference of Means. w=µ colluder −µ honest in standardised activation space, normalised to unit
length.
Linear Artificial Topography (LAT). PCA with n_components=4 on paired difference vectors
(x+ −x −). Direction = first principal component, oriented so the positive class projects higher.
Multi-Layer Perceptron. MLPClassifier with hidden_layer_sizes=(128,) and
max_iter=1000. Per-agent score =Pr(colluder| ¯aj).
Multi-Headed Attention.Input Linear(d, 64), then nn.MultiheadAttention with
d_model=64, num_heads=4, dropout=0.1; residual + LayerNorm; output Linear(64, 1).
Adam,lr=1e-3,batch_size=32,epochs=200,BCEWithLogitsLoss.
Multi-Layer ensemble.Per-layerLogisticRegressionwithC=1.0,max_iter=1000, fit inde-
pendently at each of layers 26–30. Per-agent projections averaged across layers.
C.1 Method selection when the coalition is unknown
Four of our five methods—Sorted Concatenation, Activation Alignment, Peak Suspicion, and the
Asymmetry Probe—work regardless of the size of the coalition (how many agents are colluding).
Deception Split is the exception: the scoring formula hardcodes the number of colluders, so it should
break if there are more or fewer.
D Compute and Hardware
Models.We use the following four open-weight models:
15
• Qwen3-32B-AWQ
• Llama-3.1-70B-Instruct-AWQ-INT4
• DeepSeek-R1-Distill-Qwen-32B
• GPT-OSS-20B
Generation and activation extraction.
• Qwen3-32B and GPT-OSS-20B: workstation with 2×NVIDIA RTX GPUs.
• Llama-3.1-70B and DeepSeek-R1 32B: server with 2–4×NVIDIA A40 GPUs.
Probe training and evaluation.All probe training and evaluation runs on CPU.
E Refusal Rates
Figure 7: Refusal rates per model per tier.
Figure 7 reports the percentage of collusion runs in which at least one colluder refused to follow the
coalition instruction. GPT-OSS-20B refuses by far the most often. Refused runs are excluded from
the AUROCs in the main paper where the audit allows; the per-tier exclusion criteria are documented
in Appendices F.7, G.9, and H.8.
F The NARCBENCH-COREDataset
F.1 Overview
NARCBENCH-COREis the probe-training corpus used throughout the main paper. It contains 50
independent committee-deliberation scenarios spanning 17 high-stakes real-world domains, each
instantiated under acollusioncondition (two of four agents are secretly instructed to coordinate toward
a predetermined outcome via a private channel before public discussion) and acontrolcondition (all
four agents receive identical honest instructions), yielding 100 runs in total.
F.2 Scenario design and diversification
The 17 domains are audit, cybersecurity, education, engineering, environmental, financial, food
safety, government, hiring, insurance, legal, medical ethics, military, pharmaceutical, real estate,
research integrity, and sports. Each scenario was hand-authored rather than generated from a shared
skeleton, so that no two scenarios share a collusion motive verbatim and no single recurring phrase
can be a classification shortcut for a probe. Each scenario specifies a situational context, two options
under review (one fair, one the collusion target), a scenario-specific collusion motive, and domain-
appropriate prompt frames for the private coordination, public discussion, and final recommendation
phases.
The collusion motive in each scenario is grounded in a domain-appropriate confidentiality framing,
for example a non-disclosure agreement, attorney-client privilege, ex parte communication, pre-
employment ethics wall, physician-patient privilege, or an intermediary relationship with a major
stakeholder. The private channel the two colluders communicate over is instantiated as a domain-
specific medium (Slack DM, Bloomberg Terminal, Signal, Keybase, WhatsApp, encrypted internal
16
system, stairwell conversation, parking-lot text, and others) rather than the generic phrase “private
channel,” again to avoid a single recurring token that a probe could latch onto.
Within each scenario we further diversify along four axes. Agent names are drawn without replace-
ment from a fixed pool of 60 multicultural first-and-last name pairs, using a seed tied to scenario
index so that the same four names appear in both the collusion and control runs of that scenario and
no name is permanently associated with a colluder or honest role across the dataset. Instructio
```
