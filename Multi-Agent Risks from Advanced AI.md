---
title: Multi-Agent Risks from Advanced AI
author: Lewis Hammond, Alan Chan, Jesse Clifton, Jason Hoelscher-Obermaier, Akbir Khan, Euan McLean, Chandler Smith, Wolfram Barfuss, Jakob Foerster, Tomáš Gavenčiak, The Anh Han, Edward Hughes, Vojtěch Kovařík, Jan Kulveit, Joel Z. Leibo, Caspar Oesterheld, Christian Schroeder de Witt, Nisarg Shah, Michael Wellman, Paolo Bova, Theodor Cimpeanu, Carson Ezell, Quentin Feuillade-Montixi, Matija Franklin, Esben Kran, Igor Krawczuk, Max Lamparth, Niklas Lauffer, Alexander Meinke, Sumeet Motwani, Anka Reuel, Vincent Conitzer, Michael Dennis, Iason Gabriel, Adam Gleave, Gillian Hadfield, Nika Haghtalab, Atoosa Kasirzadeh, Sébastien Krier, Kate Larson, Joel Lehman, David C. Parkes, Georgios Piliouras, Iyad Rahwan
year: "2025"
Type: Preprint
DOI: 10.48550/arXiv.2502.14143
source: https://arxiv.org/abs/2502.14143
created: 2026-06-18
description: The rapid development of advanced AI agents and the imminent deployment of many instances of these agents will give rise to multi-agent systems of unprecedented complexity. These systems pose novel and under-explored risks. In this report, we provide a structured taxonomy of these risks by identifying three key failure modes (miscoordination, conflict, and collusion) based on agents&#39; incentive
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
  - tech/Ai/LLM
  - themes/ethics/risks
  - tech/evaluation
pdfORepub: "[[Multi-Agent Risks from Advanced AI.pdf]]"
---
[[Multi-Agent Risks from Advanced AI.pdf]]

> **Abstract:** The rapid development of advanced AI agents and the imminent deployment of many instances of these agents will give rise to multi-agent systems of unprecedented complexity. These systems pose novel and under-explored risks. In this report, we provide a structured taxonomy of these risks by identifying three key failure modes (miscoordination, conflict, and collusion) based on agents&#39; incentive

## Full text (extracted from `Multi-Agent Risks from Advanced AI.pdf`)

*Source:* `2PDF/Multi-Agent Risks from Advanced AI.pdf`  
*Extracted:* 2026-06-18

```text
Lewis Hammond
Alan Chan
Jesse Clifton
Jason Hoelscher-Obermaier
Akbir Khan
Euan McLean
Chandler Smith
Wolfram Barfuss
Jakob Foerster
Tomáš Gavenčiak
The Anh Han
Edward Hughes
Vojtěch Kovařík
Jan Kulveit
Joel Z. Leibo
Caspar Oesterheld
Christian Schroeder de Witt
Nisarg Shah
Michael Wellman
Paolo Bova
Theodor Cimpeanu
Carson Ezell
Quentin Feuillade-Montixi
Matija Franklin
Esben Kran
Igor Krawczuk
Max Lamparth
Niklas Lauﬀer
Alexander Meinke
Sumeet Motwani
Anka Reuel
Vincent Conitzer
Michael Dennis
Iason Gabriel
Adam Gleave
Gillian Hadﬁeld
Nika Haghtalab
Atoosa Kasirzadeh
Sébastien Krier
Kate Larson
Joel Lehman
David C. Parkes
Georgios Piliouras
Iyad Rahwan
Multi-Agent Risks 
from Advanced AI
Technical Report #1 February 2025Cooperative AI 
Foundation
arXiv:2502.14143v1  [cs.MA]  19 Feb 2025
Multi-Agent Risks from Advanced AI
Lewis Hammond1,2,∗
Alan Chan3,4, Jesse Clifton5,1, Jason
Hoelscher-Obermaier6, Akbir Khan7,8,(1),
Euan McLean†, Chandler Smith1
Wolfram Barfuss9, Jakob Foerster2,10, Tom´ aˇ s
Gavenˇ ciak11, The Anh Han 12, Edward
Hughes13, Vojtˇ ech Kovaˇ r´ ık14,(15), Jan
Kulveit11, Joel Z. Leibo 13, Caspar
Oesterheld15, Christian Schroeder de Witt 2,
Nisarg Shah16, Michael Wellman17
Paolo Bova12, Theodor Cimpeanu18,(19)
Carson Ezell20, Quentin Feuillade-
Montixi21,(†), Matija Franklin8, Esben Kran6,
Igor Krawczuk†,(22), Max Lamparth23, Niklas
Lauffer24, Alexander Meinke25,(†), Sumeet
Motwani2,(24), Anka Reuel23,20
Vincent Conitzer15, Michael Dennis13, Iason
Gabriel13, Adam Gleave26, Gillian Hadfield27,
Nika Haghtalab24, Atoosa Kasirzadeh15,
S´ ebastien Krier13, Kate Larson28,13, Joel
Lehman†, David C. Parkes20, Georgios
Piliouras13,29, Iyad Rahwan30
1Cooperative AI Foundation
2University of Oxford
3Mila
4Centre for the Governance of AI
5Center on Long-Term Risk
6Apart Research
7Anthropic
8University College London
9University of Bonn
10Meta AI
11Charles University
12Teesside University
13Google DeepMind
14Czech Technical University
15Carnegie Mellon University
16University of Toronto
17University of Michigan
18University of Stirling
19University of St Andrews
20Harvard University
21PRISM AI
22 ´Ecole Polytechnique F´ ed´ erale de Lausanne
23Stanford University
24University of California, Berkeley
25Apollo Research
26FAR.AI
27Johns Hopkins University
28University of Waterloo
29Singapore University of Technology and Design
30Max Planck Institute for Human Development
†Independent
Abstract
The rapid development of advanced AI agents and the imminent deployment
of many instances of these agents will give rise to multi-agent systems of un-
precedented complexity. These systems pose novel and under-explored risks.
In this report, we provide a structured taxonomy of these risks by identify-
ing three key failure modes (miscoordination, conflict, and collusion) based on
agents’ incentives, as well as seven key risk factors (information asymmetries,
network effects, selection pressures, destabilising dynamics, commitment prob-
lems, emergent agency, and multi-agent security) that can underpin them. We
highlight several important instances of each risk, as well as promising direc-
tions to help mitigate them. By anchoring our analysis in a range of real-world
examples and experimental evidence, we illustrate the distinct challenges posed
by multi-agent systems and their implications for the safety, governance, and
ethics of advanced AI.
∗Correspondence to lewis.hammond@cooperativeai.org. Suggested citation: “Hammond et al. (2025). Multi-Agent
Risks from Advanced AI. Cooperative AI Foundation, Technical Report #1.” Author clusters are ordered by approximate
magnitude of contribution and represent the lead author, organisers, major contributors, minor contributors, and advisors,
respectively. Within clusters, authors are listed alphabetically. Full details of author roles are available in Appendix A.
Affiliations in parentheses indicate that the author’s work on this report was primarily completed while under that affiliation.
Due to the length of the author list, authorship does not entail endorsement of all claims in the report, nor does inclusion
entail an endorsement on the part of any individual’s organisation. In particular, contributions to this report reflect the
views of the respective contributors and not necessarily the views of the Cooperative AI Foundation, its trustees, or funders.
2
Contents
Executive Summary 4
1 Introduction 5
1.1 Overview 5
1.2 Scope 7
1.3 Related Work 8
2 Failure Modes 10
2.1 Miscoordination 10
2.2 Conflict 13
2.3 Collusion 17
3 Risk Factors 20
3.1 Information Asymmetries 20
3.2 Network Effects 23
3.3 Selection Pressures 26
3.4 Destabilising Dynamics 30
3.5 Commitment and Trust 33
3.6 Emergent Agency 36
3.7 Multi-Agent Security 39
4 Implications 43
4.1 Safety 43
4.2 Governance 44
4.3 Ethics 46
5 Conclusion 48
A Contributions 49
A.1 Acknowledgements 49
A.2 Author Roles 50
B Case Study Details 51
B.1 Zero-Shot Coordination Failures in Driving 51
B.2 Transmission Through AI Networks Can Spread Falsities and Bias 51
B.3 Unprompted Adversarial Attacks on Overseer Agents 51
References 53
3
Executive Summary
The proliferation of increasingly advanced AI not only promises widespread benefits, but also presents
new risks (Bengio et al., 2024; Chan et al., 2023). Today, AI systems are beginning to au-
tonomously interact with one another and adapt their behaviour accordingly, formingmulti-
agent systems. This change is due to the widespread adoption of sophisticated models that can interact
via a range of modalities (including text, images, and audio), and the competitive advantages conferred
by autonomous, adaptive agents (Anthropic, 2024a; Google DeepMind, 2024; OpenAI, 2025).
While still relatively rare, groups of advanced AI agents are already responsible for tasks that range from
trading million-dollar assets (AmplifyETFs, 2025; Ferreira et al., 2021; Sun et al., 2023a) to recommend-
ing actions to commanders in battle (Black et al., 2024; Manson, 2024; Palantir, 2025). In the near
future, applications will include not only economic and military domains, but are likely to
extend to energy management, transport networks, and other critical infrastructure (Ca-
macho et al., 2024; Mayorkas, 2024). Large populations of AI agents will also feature in more familiar
social settings as intelligent personal assistants or representatives, capable of being delegated increasingly
complex and important tasks.
While bringing new opportunities for scalable automation and more diffuse benefits to society, these
advanced, multi-agent systems present novel risks that are distinct from those posed by
single agentsor less advancedtechnologies, and which have been systematically underappreciated
and understudied. This lack of attention is partly because present-day multi-agent systems are rare (and
those that do exist are often highly controlled, such as in automated warehouses), but also because even
single agents present many unsolved problems (Amodei et al., 2016; Anwar et al., 2024; Hendrycks et al.,
2021). Given the current rate of progress and adoption, however, we urgently need to evaluate
(and prepare to mitigate) multi-agent risks from advanced AI . More concretely, we provide
recommendations throughout the report that can largely be classified as follows.
• Evaluation: Today’s AI systems are developed and tested in isolation, despite the fact that they
will soon interact with each other. In order to understand how likely and severe multi-agent risks
are, we need new methods of detecting how and when they might arise, such as: evaluating the
cooperative capabilities, biases, and vulnerabilities of models; testing for new or improved danger-
ous capabilities in multi-agent settings (such as manipulation, collusion, or overriding safeguards);
more open-ended simulations to study dynamics, selection pressures, and emergent behaviours; and
studies of how well these tests and simulations match real-world deployments.
• Mitigation: Evaluation is only the first step towards mitigating multi-agent risks, which will
require new technical advances. While our understanding of these risks is still growing, there
are promising directions that we can begin to explore now, such as: scaling peer incentivisation
methods to state-of-the-art models; developing secure protocols for trusted agent interactions;
leveraging information design and the potential transparency of AI agents; and stabilising dynamic
multi-agent networks and ensuring they are robust to the presence of adversaries.
• Collaboration: Multi-agent risks inherently involve many different actors and stakeholders, of-
ten in complex, dynamic environments. Greater progress can be made on these interdisciplinary
problems by leveraging insights from other fields, such as: better understanding the causes of un-
desirable outcomes in complex adaptive systems and evolutionary settings; determining the moral
responsibilities and legal liabilities for harms not caused by any single AI system; drawing lessons
from existing efforts to regulate multi-agent systems in high-stakes contexts, such as financial
markets; and determining the security vulnerabilities and affordances of multi-agent systems.
To support these recommendations, we introduce a taxonomy of AI risks that are new, much
more challenging, or qualitatively different in the multi-agent setting, together with a
preliminary assessment of what can be done to mitigate them . We identify three high-level
failure modes, which depend on the nature of the agents’ objectives and the intended behaviour of the
system: miscoordination, conflict, and collusion. We then describe seven key risk factors that can lead
to these failures: information asymmetries, network effects, selection pressures, destabilising dynamics,
commitment and trust, emergent agency, and multi-agent security. For each problem we provide a
definition, key instances of how and where it can arise, illustrative case studies, and promising directions
for future work. We conclude by discussing theimplications for existing work in AI safety, AI governance,
and AI ethics.
4
1 Introduction
The proliferation of increasingly advanced AI not only promises widespread benefits, but also presents
new risks (Bengio et al., 2024; Chan et al., 2023). In the future, AI systems will commonly interact and
adapt in response to one another, forming multi-agent systems .1 This trend will be driven by several
factors. First, recent technical progress and publicity will continue to drive adoption, including in high-
stakes areas such as financial trading (AmplifyETFs, 2025; Ferreira et al., 2021; Sun et al., 2023a) and
military strategy (Black et al., 2024; Manson, 2024; Palantir, 2025). Second, AI systems that can act
autonomously and adapt while deployed as agents will have competitive advantages compared to non-
adaptive systems or those with humans in the loop. Third, the more widely such agents are deployed,
the more they will come to interact with one another.
The emergence of these advanced multi-agent systems presents a number of risks which have thus far
been systematically underappreciated and understudied. In part, this lack of attention is because the
deployment of such systems is currently rare, or constrained to highly controlled settings (such as auto-
mated warehouses) that do not suffer from the most severe risks. In part, it is because even the simpler
problem of ensuring the safe and ethical behaviour of a single advanced AI system is far from solved
(Amodei et al., 2016; Anwar et al., 2024; Hendrycks et al., 2021), and multi-agent settings are strictly
more complex. Indeed, many multi-agent risks are inherently sociotechnical and require attention from
many stakeholders and researchers across many disciplines (Curtis et al., 2024; Lazar & Nelson, 2023).
Importantly, these risks are distinct from those posed by single agents or less advanced technologies, and
will not necessarily be addressed by efforts to mitigate the latter. For example: the alignment of AI agents
with different actors is insufficient to prevent conflict if those actors have diverging interests (Critch &
Krueger, 2020; Dafoe et al., 2020; Jagadeesan et al., 2023a; Manheim, 2019; Sourbut et al., 2024); errors
that may be acceptable in isolation could compound in complex, dynamic networks of agents (Buldyrev
et al., 2010; Kirilenko et al., 2017; Lee & Tiwari, 2024; Maas, 2018; Sanders et al., 2018); and groups
of agents could combine or collude to develop dangerous capabilities or goals that cannot be ascribed
to any individual (Calvano et al., 2020; Drexler, 2022; Jones et al., 2024; Mogul, 2006; Motwani et al.,
2024). Advanced AI also introduces phenomena that differ fundamentally from previous generations of
AI or other technologies, requiring new approaches to mitigating these risks (Bengio et al., 2024).
With the current rate of progress, we therefore urgently need to evaluate (and prepare to mitigate)
multi-agent risks from advanced AI. In this report we take a first step in this direction by providing a
taxonomy of risks that either: emerge, are much more challenging, or are qualitatively different in the
multi-agent setting (see Table 1). We identify three key high-level failure modes (Section 2), and seven
key risk factors that can lead to these failures (Section 3), before discussing the implications for AI
safety, AI governance, and AI ethics (Section 4). Throughout the report we illustrate these risks with
concrete examples, either from real-world events, previous research, or novel experiments (see Table 3).
1.1 Overview
We begin by identifying different failure modes in multi-agent systems based on the nature of the agents’
goals and the intended behaviour of the system. In most multi-agent systems, we are interested in AI
agents working together to achieve their respective goals or the goals of those who deployed them. In this
case, we categorise failures into miscoordination (Section 2.1), where agents fail to cooperate despite
having the same goal, and conflict (Section 2.2), where agents with different goals fail to cooperate. A
third and final kind of failure – collusion (Section 2.3) – can arise in competitive settings where we do
not want agents cooperating (such as markets).
We next introduce a number of risk factors by which these failure modes can arise, and which are largely
independent of the agents’ precise incentives. 2 For example, information asymmetries could lead to
miscoordination between agents with the same goal, or to conflict among agents with competing goals.
These factors are not specific to AI systems, but the differences between AI systems and other kinds
of intelligent agents (such as humans or corporations) leads to different risk instances and potential
solutions. Finally, note that the following factors are not necessarily exhaustive or mutually exclusive.
1A fundamental fact about (software-based) AI systems is that they can be easily duplicated. Thus, the vast training
costs involved in producing state-of-the-art systems can be amortized over millions of instances. In this sense, if nothing
else, the concept of multi-agent systems is core to transformative AI.
2Indeed, there are potential risks from multi-agent systems in which it is not the agents’ objectives that are the critical
feature, but their general incompetencies or vulnerabilities.
5
Risk Instances Directions
Miscoordination • Incompatible Strategies
• Credit Assignment
• Limited Interactions
• Communication
• Norms and Conventions
• Modelling Other Agents
Conflict • Social Dilemmas
• Military Domains
• Coercion and Extortion
• Learning Peer and Pool Incentivisation
• Establishing Trust
• Normative Approaches to Equilibrium Selection
• Cooperative Dispositions
• Agent Governance
• Evidential Reasoning
Collusion • Markets
• Steganography
• Detecting AI Collusion
• Mitigating AI Collusion
• Assessing Impacts on Safety Protocols
Information
Asymmetries
• Communication
Constraints
• Bargaining
• Deception
• Information Design
• Individual Information Revelation
• Few-Shot Coordination
• Truthful AI
Network Effects • Error Propagation
• Network Rewiring
• Homogeneity and
Correlated Failures
• Evaluating and Monitoring Networks
• Faithful and Tractable Simulations
• Improving Network Security and Stability
Selection
Pressures
• Undesirable Dispositions
from Competition
• Undesirable Dispositions
from Human Data
• Undesirable Capabilities
• Evaluating Against Diverse Co-Players
• Environment Design
• Understanding the Impacts of Training
• Evolutionary Game Theory
• Simulating Selection Pressures
Destabilising
Dynamics
• Feedback Loops
• Cyclic Behaviour
• Chaos
• Phase Transitions
• Distributional Shift
• Understanding Dynamics
• Monitoring and Stabilising Dynamics
• Regulating Adaptive Multi-Agent Systems
Commitment
and Trust
• Inefficient Outcomes
• Threats and Extortion
• Rigidity and Mistaken
Commitments
• Keeping Humans in the Loop
• Limiting Commitment Power
• Institutions and Normative Infrastructure
• Privacy-Preserving Monitoring
• Mutual Simulation and Transparency
Emergent
Agency
• Emergent Capabilities
• Emergent Goals
• Empirical Exploration
• Theories of Emergent Capabilties
• Theories of Emergent Goals
• Monitoring and Intervening on Collective Agents
Multi-Agent
Security
• Swarm Attacks
• Heterogeneous Attacks
• Social Engineering at Scale
• Vulnerable AI Agents
• Cascading Security Failures
• Undetectable Threats
• Secure Interaction Protocols
• Monitoring and Threat Detection
• Multi-Agent Adversarial Testing
• Sociotechnical Security Defences
Table 1: An overview of the instances and research directions identified for each failure mode and risk
factor (see Sections 2 and 3 for a discussion of each bullet point).
6
• Information asymmetries (Section 3.1): private information can lead to miscoordination, de-
ception, and conflict;
• Network effects (Section 3.2): minor changes in properties or connection patterns of agents in a
network can lead to dramatic changes in the behaviour of the whole group;
• Selection pressures (Section 3.3): some aspects of training and selection by those deploying and
using AI agents can lead to undesirable behaviour;
• Destabilising dynamics (Section 3.4): systems that adapt in response to one another can produce
dangerous feedback loops and unpredictability;
• Commitment and trust (Section 3.5): difficulties in forming credible commitments, trust, or
reputation can prevent mutual gains in AI-AI and human-AI interactions;
• Emergent agency (Section 3.6): qualitatively different goals or capabilities can emerge from the
composition of innocuous independent systems or behaviours;
• Multi-agent security (Section 3.7): multi-agent systems give rise to new kinds of security threats
and vulnerabilities.
We conclude the report by surveying the safety, governance, and ethical implications of these risks (see
Table 2). For example, most work on AI safety (Section 4.1) focuses on issues such as the robustness,
interpretability, or alignment of a single system (Amodei et al., 2016; Anwar et al., 2024; Hendrycks
et al., 2021), despite the fact that an increasing number of proposals for building safer AI systems are
implicitly multi-agent (e.g., Drexler, 2019; Greenblatt et al., 2023; Irving et al., 2018; Perez et al., 2022a;
Schwettmann et al., 2023). The fact that AI governance (Section 4.2) efforts often involve multi-
stakeholder settings provides hope that governance tools can complement technical advances to mitigate
multi-agent risks (Reuel et al., 2024a; Trager et al., 2023). At the same time, multi-agent interactions
naturally raise questions in AI ethics (Section 4.3) related to issues of fairness, collective responsibility,
and the social good (Friedenberg & Halpern, 2019; Gabriel et al., 2024; Zhang & Shah, 2014a).
Safety Governance Ethics
• Alignment is Not Enough
• Collusion in Adversarial
Safety Schemes
• Dangerous Collective Goals
and Capabilities
• Correlated and Compounding
Failures
• Robustness and Security in
Multi-Agent Systems
• Supporting Research on
Multi-Agent Risks
• Multi-Agent Evaluations
• New Forms of Documentation
• Infrastructure for AI Agents
• Restrictions on Development
and Deployment
• Liability for Harms from
Multi-Agent Systems
• Improving Societal Resilience
• Pluralistic Alignment
• Agentic Inequality
• Epistemic Destablisation
• Compounding of Unfairness
and Bias
• Compounding of Privacy Loss
• Accountability Diffusion
Table 2: An overview of the implications of multi-agent risks for existing work in AI safety, governance,
and ethics (see Section 4 for a discussion of each bullet point).
1.2 Scope
Concerns about the risks posed by AI systems range from biased hiring decisions (Raghavan et al., 2020)
to existential catastrophes (Bostrom, 2014), and are represented by a vast literature. Before giving a
brief overview of the most closely related works, it is therefore worth us pausing to clarify the scope of
this report, which is as follows.
• Risks and failure modes: we seek to identify specific mechanisms via which risks could emerge,
rather than just just the open research problems that these risks present.
• Multiple agents: if the risk could arise in essentially the same way in the context of a single AI
system, then we deem it to be out of scope for this report (while not diminishing its importance). 3
3Note that this includes the problem of alignment (Ngo et al., 2022; Russell, 2019), which we do not study in this
7
• Advanced AI: while many of the risks we identify also apply to simpler systems, their effects
are most severe in the context of increasingly autonomous and powerful AI agents, 4 and so this is
where our primary focus lies.
• Real-world examples: wherever possible, we make sure to ground these risks in real-world events,
previous research, or novel experiments – not merely hypothetical speculation (see Table 3).
• Technical perspectives: due to the authors’ expertise (and to keep the scope of the report
manageable), we primarily discuss risks from a technical perspective, while acknowledging that
this perspective is limited.
• Concrete paths forwards : where possible, we aim to specify relatively narrow proposals for
future research, in the hope that this makes it easier for others to contribute.
Needless to say, multi-agent risks from advanced AI are by no means the only risks posed by AI, and
the perspective we take in this report is by no means the only approach to understanding these risks.
Moreover, we almost entirely neglect the potential upsides of advanced multi-agent systems: greater
decentralisation and democratisation of AI technologies; assistance in cooperating and coordinating
with others; increased robustness, flexibility, and efficiency; novel approaches to solving alignment and
safety issues in single-agent settings; and – perhaps most importantly – more widespread and evenly
distributed benefits from AI. We hope that this report serves to complement earlier and adjacent research
on understanding these challenges and opportunities.
1.3 Related Work
The most similar report to ours is that of Manheim (2019), who introduces a range of technical multi-
agent failure modes through the lens of model over-optimization. This over-optimisation can result in
the intended and actual behaviour of the model coming apart when faced with low-probability inputs, a
regime change, measurement errors, or inaccuracies in the model’s internal representations. While this
lens is helpful for understanding some multi-agent risk factors, not all factors can neatly be captured
through it. Altmann et al. (2024) and Mogul (2006) take an alternative perspective and focus on
‘emergent’ failures that occur specifically in multi-agent settings, though their focus is not on advanced
AI agents. Also highly relevant is Clifton (2020)’s agenda on cooperation and conflict in the context of
transformative AI, though the priority of that work is to describe a set of promising research directions,
rather than to explicate the underlying risks.
More broadly, the topics of this report are closely related to the emerging subfield of cooperative AI
(Bertino et al., 2020; Conitzer & Oesterheld, 2023; Dafoe et al., 2021, 2020), which chiefly studies how
to engineer AI systems in order to help solve cooperation problems between humans, AI agents, or
combinations thereof. In contrast to these previous agendas, we also discuss failures from undesirable
cooperation (i.e., collusion) and focus more on the concrete mechanisms via which failures can occur,
rather than the capabilities needed for addressing them. We also incorporate additional perspectives
beyond traditional game-theoretic paradigms – such as complex systems and security – and highlight
implications for work in AI governance and AI ethics in addition to AI safety.
Other surveys of AI risks focus primarily on the case of individual (often present-day) AI systems. For
example, Amodei et al. (2016) survey a range of concrete problems in AI safety (side effects, reward
hacking, scalable oversight, safe exploration, and robustness to distributional shifts), while Hendrycks
et al. (2021) provide a classification of problems in ML safety (robustness, monitoring, alignment, and
systemic safety). Anwar et al. (2024), Bird et al. (2023), Bommasani et al. (2021), and Weidinger et al.
(2022) focus on the risks from foundation models specifically, while Chan et al. (2023) and Gabriel et al.
(2024) consider the harms posed by increasingly ‘agentic’ systems and AI assistants. Other taxonomies
seek to adopt an explicitly sociotechnical lens (Abercrombie et al., 2024; Shelby et al., 2023; Weidinger
et al., 2023b), often focusing primarily on present-day risks. Uuk et al. (2025) and Zeng et al. (2024)
provide meta-reviews of AI risks derived from different research papers, as well as government and
report.
4We tend to reserve the word ‘agent’ for more autonomous, self-sufficient, and goal-directed systems, though what
counts as an ‘AI agent’ as opposed to a mere ‘AI system’ is not always clear (Chan et al., 2023; Gabriel et al., 2024; Kapoor
et al., 2024). Similarly, we will often use the word ‘principal’ for the actor on whose behalf an agent acts (be they an
individual, a group, or some other entity). Note also that we do not necessarily advocate for the building of advanced AI
agents (Mitchell et al., 2025), we merely expect that such agents will be built.
8
company policies. Our report is complementary to these works, and includes discussion of how novel
problems arise in the multi-agent case, and in the case of more advanced AI agents.
More speculatively, some authors have considered the possibility of catastrophic or even existential risks
from AI (Bostrom, 2014; Kasirzadeh, 2024b; Ord, 2020; Turchin & Denkenberger, 2018). Hendrycks
et al. (2023) categorises such risks into malicious use, AI races, organizational risks, and rogue AIs. As
in Hendrycks (2023), multi-agent risks are viewed largely through an evolutionary lens, though this is
primarily restricted to competitive pressures at the level of non-AI actors (such as firms or states). Critch
& Krueger (2020) and Critch & Russell (2023) frame such risks in terms of delegation to AI systems and
the responsibilities of those doing so. While they provide illuminating vignettes of possible catastrophes,
we aim to provide more concrete examples at a more modest scale.
Case Study
Miscoordination
Conflict
Collusion
Information Asymmetries
Network Effects
Selection Pressures
Destabilising Dynamics
Commitment and Trust
Emergent Agency
Multi-Agent SecurityType Page
Zero-Shot Coordination Failures in
Driving ✓ · · ✓ · ✓ · · · · ■ 11
Escalation in Military Conflicts · ✓ · · · · ✓ · · · ▲ 15
Common Resource Problems · ✓ · · · ✓ · ✓ · · ▲ 14
Algorithmic Collusion in the German
Retail Gasoline Market · · ✓ · · ✓ · · ✓ · • 18
Language Model Steganography · · ✓ · · · · · · ✓ ▲ 19
AI Agents Can Learn to Manipulate
Financial Markets · ✓ · ✓ · · · · · · ▲ 21
Transmission Through AI Networks
Can Spread Falsities and Bias · · · ✓ ✓ · · · · · ■ 24
Infectious Adversarial Attacks in
Networks of LLM Agents · · · · ✓ · · · · ✓ ▲ 25
Cooperation Fails to Culturally Evolve
among LLM Agents · ✓ · · · ✓ · ✓ · · ▲ 28
The 2010 Flash Crash · · · · ✓ · ✓ · · · • 31
Dead Hands and Automated
Deterrence · ✓ · · · · · ✓ · · • 35
Overcoming Safeguards via Multiple
Safe Models · · · · · · · · ✓ ✓ ▲ 40
Unprompted Adversarial Attacks on
Overseer Agents · · · · · · · · · ✓ ■ 41
Table 3: An overview of the case studies present in this report, and the failure modes and risk factors
that they represent. Each case study represents either a historical example ( • ), existing results from
the literature (▲), or – when neither of these existed – novel experiments that we conducted as part of
this report (■). Further details about our own experiments are provided in Appendix B.
9
2 Failure Modes
Multi-agent systems can fail in various ways, depending on the intended behaviour of the system and the
objectives of the agents. First, we can distinguish between cases where we want the agents to be cooper-
ating (as in collective action problems or team games) or competing (such as in markets or adversarial
training). Second, we can further divide the space of failure modes depending on whether the agents
have exactly the same objectives, different but overlapping objectives, or completely opposed objectives.5
While different authors have used different terms to describe these cases, we use the terminology shown
in Figure 1. 6 Finally, there are many potential risks from advanced multi-agent systems that do not
necessarily arise through agents competently pursuing their objectives, but due to their incompetencies
or vulnerabilities. We consider these latter failures as part of our discussion on different risk factors in
Section 3.
Cooperation?
CollusionObjectives?
N/AConflictMiscoordination
Identical
Mixed
Opposing
Desirable Undesirable
Figure 1: The three kinds of failure mode that we study in this work. Note that we do not consider
constant-sum settings where cooperation is desirable, as in such cases it is definitionally impossible for
some agents to gain without a commensurate loss from one or more other agents.
2.1 Miscoordination
The simplest kind of cooperation failures are those in which all agents have (approximately) the same
objectives. Even in such common-interest settings, however, miscoordination abounds. While it is
reasonable to expect that these problems will tend to be addressed as the general capabilities of AI
systems (such as communication and reasoning about others) improve, 7 they may still present risks in
the near-term.
2.1.1 Definition
Miscoordination arises when agents, despite a mutual and clear objective, cannot align their behaviours
to achieve this objective. Unlike the case of differing objectives, in common-interest settings there is a
more easily well-defined notion of ‘optimal’ behaviour and we describe agents as miscoordinating to the
extent that they fall short of this optimum. Note that for common-interest settings it is not sufficient
for agents’ objectives to be the same in the sense of being symmetric (e.g., when two agents both want
the same prize, but only one can win). Rather, agents must have identical preferences over outcomes
(e.g., when two agents are on the same team and win a prize as a team or not at all).
It is rare that two humans will share exactly the same objectives in this sense. For example, two
sportspeople on the same team may be primarily aiming to win their match but will also have individual
preferences, such as who scores the winning point. In the case of AI systems, however, different agents can
more easily be given precisely the same goal, and indeed much work on cooperation in AI focuses solely
on the common-interest setting (Boutilier, 1996; Omidshafiei et al., 2017; Oroojlooy & Hajinezhad, 2022;
Peshkin et al., 2000; Rashid et al., 2018; Stone et al., 2010). Such approaches are typically motivated by
5This division corresponds to common-interest/team games, mixed-motive/general-sum games, and constant-sum games,
respectively.
6In particular, we note that ‘conflict’ is often used more narrowly than the idea of ‘cooperation failure in mixed-motive
settings’, which is what we use the term for. We deliberately use ‘conflict’ instead of ‘cooperation failure’ to distinguish
this failure mode from ‘miscoordination’, which applies to problems in which agents have the same objectives.
7Note that this is unlike problems of conflict and collusion, where the fundamental tension between the desired outcome
and the agents’ objectives may in fact lead to worse outcomes as general AI capabilities improve.
10
the practical and computational advantages that decentralised control confers, but are more challenging
to implement than their centralised, single-agent counterparts. Aside from this, miscoordination can also
occur in settings that have a substantial element of common interest, even if agents’ objectives are not
entirely identical.
2.1.2 Instances
Perhaps the most likely way that common-interest settings may arise in practice is where a single prin-
cipal deploys multiple AI agents on their behalf in order to jointly solve a task. This choice might be
motivated by: physical constraints (if the task comprises sub-tasks that must be completed separately
and simultaneously); efficiency considerations (if having a single agent in charge of all aspects of the task
would lead to an intractably complex problem); or a desire for robustness (if an individual agent might
fail but others could still succeed in their place). Alternatively, we might see multi-principal multi-agent
settings in which the agents’ goals are sufficiently aligned to be viewed as (approximately) identical.
For example, if two autonomous vehicles are driving along the same road, then the mutual harms from
potential miscoordination (such as a collision) are far greater than any small individual benefits from
competition (such as attempting a risky overtaking manoeuvre to get slightly ahead).
Incompatible Strategies. Even if all agents can perform well in isolation, miscoordination can still
occur due to the agents choosing incompatible strategies (Cooper et al., 1990). Competitive (i.e., two-
player zero-sum) settings allow designers to produce agents that are maximally capable without taking
other players into account. Crucially, this is possible because playing a strategy at equilibrium in the
zero-sum setting guarantees a certain payoff, even if other players deviate from the equilibrium (Nash,
1951). On the other hand, common-interest (and mixed-motive) settings often allow a vast number of
mutually incompatible solutions (Schelling, 1980), which is worsened in partially observable environments
(Bernstein et al., 2002; Reif, 1984). As a simple example, everyone driving on the left side or the right
side of the road are both perfectly valid ways of keeping drivers safe, but these two conventions are
inherently incompatible with one another (see Case Study 1).
Case Study 1: Zero-Shot Coordination Failures in Driving
Figure 2: Examples of scenes given to GPT-4 Vision in our language agent pipeline.
Miscoordination is possible even among agents with shared objectives. We demonstrate how two
frontier models trained on driving conventions from two different countries can face coordination
failures. Following recent advances in robotics that combine vision models for scene comprehen-
sion with large language models (LLMs) for discrete action planning (e.g., Padalkar et al., 2023),
we created an experiment using two fine-tuned GPT-3.5 models. One model was trained on US
driving protocols requiring rightward yielding for emergency vehicles, while the other followed
Indian conventions mandating leftward yielding. Context-specific training data was generated
as input-output pairs by GPT-4 based on the specified driving conventions and then manually
reviewed. A GPT-4 Vision model processed the environmental inputs and provided scene descrip-
tions to both fine-tuned GPT-3.5 models for action generation. The results quantified a significant
coordination failure: unspecialized base models failed in only 5% of scenarios (2/40 simulations),
while specialized models exhibited a 77.5% failure rate (31/40 simulations), consistently failing
to create clear paths for emergency vehicles. This demonstrates an example where a convention
cannot always be declared in a zero-shot interaction, posing risks in multi-agent settings.
11
Credit Assignment. While agents can often learn to jointly solve tasks and thus avoid coordination
failures, learning is made more challenging in the multi-agent setting due to the problem of credit assign-
ment (Du et al., 2023; Li et al., 2025, see also Section 3.1 on information asymmetries and Section 3.4,
which discusses distributional shift). That is, in the presence of other learning agents, it can be unclear
which agents’ actions caused a positive or negative outcome to obtain, especially if the environment is
complex. Moreover, in multi-principal settings, agents may not have been trained together and therefore
need to generalise to new co-players and collaborators based on their prior experience (Agapiou et al.,
2022; Leibo et al., 2021; Stone et al., 2010).
Limited Interactions. Sometimes learning from historical interactions with the relevant agents may
not be possible, or may be possible using only limited interactions. In such cases, some other form of
information exchange is required for agents to be able to reliably coordinate their actions, such as via
communication (Crawford & Sobel, 1982; Farrell & Rabin, 1996a) or a correlation device (Aumann,
1974, 1987). While advances in language modelling mean that there are likely to be fewer settings in
which the inability of advanced AI systems to communicate leads to miscoordination, situations that
require split-second decisions or where communication is too costly could still produce failures. In these
settings, AI agents must solve the problem of ‘zero-shot’ (or, more generally, ‘few-shot’) coordination
(Emmons et al., 2022; Hu et al., 2020; Stone et al., 2010; Treutlein et al., 2021; Zhu et al., 2021).
2.1.3 Directions
Decentralised control and coordination in multi-agent systems have been well-studied problems for
decades (Boutilier, 1996; Omidshafiei et al., 2017; Oroojlooy & Hajinezhad, 2022; Peshkin et al., 2000;
Rashid et al., 2018; Stone et al., 2010). At one level of abstraction, the key challenge of coordination
is that of sharing information, i.e., communication. If agents have the same preferences and are able to
communicate, they can coordinate by (say) having a single agent announce their intended action and
everyone else follow suit, since there are no incentives for the leader to lie or the followers to deviate
(e.g., Farrell & Rabin, 1996b). Given the superhuman capabilities of advanced AI to transmit and pro-
cess vast swathes of information, the most important research directions in this area will therefore be
those in which it is not possible to exercise these capabilities (e.g., due to complexity, latency, or privacy
constraints).
Communication. As noted above, the advanced communication abilities of LLMs promise to simplify
many coordination challenges. In order to successfully integrate these advances into real-world systems,
however, agents need to know when and what needs to be coordinated on – something that may not
always be obvious in novel or out-of-distribution domains. In safety-critical domains, it may therefore
be necessary to introduce, or have the agents invent, protocols (i.e., rules and specifications) for commu-
nication between advanced AI agents (Marro et al., 2024). Moreover, agents need to agree on how the
communication channel is grounded (Clark & Brennan, 1991) to actions or strategies in the environment.
Grounding LLMs is a problem that is not unique to coordination (Bender & Koller, 2020; Bisk et al.,
2020; Mahowald et al., 2023), but it is exacerbated by the fact that agents attempting to coordinate
through natural language need to be grounded in the same way . For instance, if they are designed with
different interfaces to tools in a domain, they must be able to coordinate despite these differences in
interfaces.
Norms and Conventions. For settings in which inter-agent communication is infeasible or insufficient,
norms and conventions may be necessary in order to avoid miscoordination (Leibo et al., 2024). For
example Hadfield-Menell et al. (2019) show that even the adoption of so-called ‘silly rules’ (those that do
not have direct bearing on the agents’ payoffs) can help groups adapt and be more robust to uncertainty
by enriching the information environment. Moving beyond more arbitrary conventions, we may choose to
design particular norms and conventions (Bicchieri, 2016; Nyborg et al., 2016; Shoham & Tennenholtz,
1992). In this setting, the challenge is to select norms that are both legible and enforceable, as well as
leading to jointly beneficial outcomes. On the other hand, if the agents can adapt their behaviour, it
may be that norms and conventions emerge over time (McElreath et al., 2003). For example, K¨ oster
et al. (2020) show that multi-agent reinforcement learning (MARL) agents can establish and switch
between conventions, even compromising on their own objective when doing so is necessary for effective
coordination. More generally, we may be interested in studying how norms and conventions emerge
(Mashayekhi et al., 2022; Morris-Martin et al., 2019), how robust they are (Hao et al., 2017; Lerer &
12
Peysakhovich, 2019), and how compatible they are with others that may have emerged in different agent
populations (Stastny et al., 2021).
Modelling Other Agents. Finally, the ability to understand and predict others’ actions can be critical
to coordination, especially in situations when little or no communication is possible. Even though agents
may assume that others share their objective in common-interest settings, being able to model others’
actions, beliefs, and intentions can be highly advantageous. For an overview of the topic and a list of
key problems, we refer the reader to Albrecht & Stone (2018). With the advent of LLM-based agents
that appear to possess some form of theory of mind and hence can be remarkably sophisticated in their
modelling of other agents (Cross et al., 2025; Li et al., 2023a), new questions arise. For example, given the
current paradigm of deriving many systems from an underlying base model, it may be easier for similarly
derived systems to reason about one another (Berglund et al., 2023; Binder et al., 2024; Oesterheld et al.,
2024b; OpenAI, 2023b).
2.2 Conflict
In the vast majority of real-world strategic interactions, agents’ objectives are neither identical nor
completely opposed. Indeed, if AI agents are sufficiently aligned to their users or deployers, we should
expect some degree of both cooperation and competition, mirroring human society. These mixed-motive
settings include the possibility of mutual gains, but also the risk of conflict due to selfish incentives. In
what follows, we examine the extent to which advanced AI might precipitate or exacerbate such risks.
2.2.1 Definition
In this work, we use the word conflict in a relatively broad sense to refer to any outcome in a mixed-
motive setting that does not lie on the Pareto frontier.8 This includes classic examples of conflict such as
legal disputes and warfare, but also encompasses cooperation failures in collective action problems, such
as the depletion of a common natural resource or a race to the bottom on legislation (Dawes & Messick,
2000; Snyder, 1971).
It is worth noting first that AI systems could help to solve conflicts, for example, by searching over
a larger space of potential solutions to disagreements, monitoring agreements, or acting as mediators
(Bakker et al., 2022; Dafoe et al., 2020; McKee et al., 2023; Small et al., 2023). At the same time, the
selfish incentives that drive said conflict may also incentivise actors to adopt AI systems in order to gain
an advantage over their competitors. In such cases, delegation to increasingly advanced AI agents is far
from guaranteed to lead to more cooperative outcomes, and could in some circumstances increase both
the speed and the scale at which conflict might emerge. Indeed, even if advanced AI systems are able to
overcome human cooperation problems, they may introduce even more complex cooperation problems
(compare to how adults may be able to prevent children from fighting, but aren’t immune from conflict
themselves).
2.2.2 Instances
As we noted above, virtually all real-world strategic interactions of interest are mixed-motive, and as
such the potential for conflict (even if in low-stakes scenarios) abounds. The introduction of advanced
AI agents could both worsen existing risks of conflict (such as increasing the degree of competition in
common-resource problems, or escalating military tensions) as well as well as introducing new forms of
conflict (such as via sophisticated methods of coercion and extortion).
Social Dilemmas. As noted in our definition, conflict can arise in any situation in which selfish
incentives diverge from the collective good, known as a social dilemma (Dawes & Messick, 2000; Hardin,
1968; Kollock, 1998; Ostrom, 1990). While this is by no means a modern problem, advances in AI could
further enable actors to pursue their selfish incentives by overcoming the technical, legal, or social barriers
that standardly help to prevent this. To take a plausible, near-term (if very low-stakes) example, an
automated AI assistant could easily reserve a table at every restaurant in town in minutes, enabling the
user to decide later and cancel all other reservations. Alternatively, the ability of AI assistants to search
and switch between different consumer products and services could lead to ‘hyper-switching’ (Van Loo,
8Recall that an outcome lies on the Pareto frontier if it is not possible to make any agent better off without making
another worse off.
13
2019), potentially leading to financial instabilities such as a deposit franchise run (Drechsler et al., 2023,
see also Case Study 10). On the other hand, profit-seeking companies might also soon deploy advanced
AI agents that either use or manage common resources, ranging from communication networks and web
services to roads and natural resources. Without methods of governing such agents, these resources may
quickly be depleted or made inaccessible to all but a small number of powerful actors.
Case Study 2: Common Resource Problems
Figure 3: A summary of the resource-sharing scenarios within the GovSim benchmark. Figure
adapted from Piatti et al. (2024).
The management of shared resources represents a fundamental test of whether AI systems can
balance individual incentives against collective welfare. 9 In the GovSim benchmark, Piatti et al.
(2024) evaluated 15 different LLMs across three resource management scenarios: fishing from a
shared lake, grazing on common pastures, and managing industrial pollution. Even the most
advanced LLMs achieved only a 54% survival rate, meaning that in nearly half of all cases, the
agents depleted their shared resources to the point of collapse. These findings align with earlier
work on sequential social dilemmas (Leibo et al., 2017), which (unlike ‘one-shot’ problems) allow
agents to react to others’ choices over time, creating complex dynamics of trust and retaliation.
When one agent begins to over-exploit resources, others often respond by increasing their own
extraction rates, triggering a cascade of competitive behaviour that accelerates resource depletion.
Without additional protections, these systems may therefore replicate or even accelerate the
tragedy of the commons (Hardin, 1968).
Military Domains. Perhaps the most obvious and worrying instances of AI conflict are those in
which human conflict is already a major concern, such as military domains (although other, less salient
forms of conflict such as international trade wars are also cause for concern). For example, beyond
applications of more narrow AI tools in lethal autonomous weapons systems (Horowitz, 2021), future
AI systems might serve as advisors or negotiators in high-stakes military decisions (Black et al., 2024;
Manson, 2024). Indeed, companies such as Palantir have already developed LLM-powered tools for
military planning (Palantir, 2025), and the US Department of Defence has recently been evaluating
models for such capacities, with personnel revealing that they “could be deployed by the military in the
very near term” (Manson, 2023). The use of AI in command and control systems to gather and synthesise
information – or recommend and even autonomously make decisions – could lead to rapid unintended
escalation if these systems are not robust or are otherwise more conflict-prone (Johnson, 2021a; Johnson,
2020; Laird, 2020, see also Case Study 10). 10
Coercion and Extortion. Advanced AI systems might also lead to various forms of coercion and
extortion in less extreme settings (Ellsberg, 1968; Harrenstein et al., 2007). These threats might target
humans directly (such as the revelation of private information extracted by advanced AI surveillance
tools), or other AI systems that are deployed on behalf of humans (such as by hacking a system to limit
9Note that we use the term ‘welfare’ in this context to denote an aggregate measure of the extent to which a group of
agents achieves their respective objectives, rather than to refer to some notion of ‘wellbeing’.
10At the same time, it is worth noting that AI systems could have significant advantages over human decision-makers in
navigating conflict in ways that avoid unnecessary esc
```
