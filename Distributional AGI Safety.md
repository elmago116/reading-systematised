---
title: Distributional AGI Safety
author: Nenad Tomašev, Matija Franklin, Julian Jacobs, Sébastien Krier, Simon Osindero
year: "2025"
Type: Preprint
DOI: 10.48550/arXiv.2512.16856
source: https://arxiv.org/abs/2512.16856
created: 2026-06-18
description: AI safety and alignment research has predominantly been focused on methods for safeguarding individual AI systems, resting on the assumption of an eventual emergence of a monolithic Artificial General Intelligence (AGI). The alternative AGI emergence hypothesis, where general capability levels are first manifested through coordination in groups of sub-AGI individual agents with complementary skill
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Distributional AGI Safety.pdf]]"
---
[[Distributional AGI Safety.pdf]]

> **Abstract:** AI safety and alignment research has predominantly been focused on methods for safeguarding individual AI systems, resting on the assumption of an eventual emergence of a monolithic Artificial General Intelligence (AGI). The alternative AGI emergence hypothesis, where general capability levels are first manifested through coordination in groups of sub-AGI individual agents with complementary skill

## Full text (extracted from `Distributional AGI Safety.pdf`)

*Source:* `2PDF/Distributional AGI Safety.pdf`  
*Extracted:* 2026-06-18

```text
2026-05-20
Distributional AGI Safety
Nenad Tomašev1, Matija Franklin1, Julian Jacobs1, Sébastien Krier1 and Simon Osindero1
1Google DeepMind
AIsafetyandalignmentresearchhaspredominantlybeenfocusedonmethodsforsafeguardingindividual
AI systems, resting on the assumption of an eventual emergence of a monolithic Artificial General
Intelligence (AGI). The alternative AGI emergence hypothesis, where general capability levels are first
manifested through coordination in groups of sub-AGI individual agents with complementary skills and
affordances, has received far less attention. Here we argue that thispatchwork AGI hypothesisneeds
to be given serious consideration, and should inform the development of corresponding safeguards
and mitigations. The rapid deployment of advanced AI agents with tool-use capabilities and the ability
to communicate and coordinate makes this an urgent safety consideration. We therefore propose a
frameworkfordistributional AGI safetythatmovesbeyondevaluatingandaligningindividualagents. This
frameworkcentresonthedesignandimplementationofvirtualagenticsandboxeconomies(impermeable
or semi-permeable), where agent-to-agent transactions are governed by robust market mechanisms,
coupled with appropriate auditability, reputation management, and oversight to mitigate collective risks.
Keywords: AI, AGI, safety, multi-agent
1. Introduction
Rapid advances in AI capabilities need to be
complemented by the development of robust
frameworks for safety, oversight, and align-
ment (Gabriel et al., 2024). AI alignment (Everitt
et al., 2018; Tegmark and Omohundro, 2023) is
particularly important in the case of autonomous
AI agents (Cihon et al., 2025; Kasirzadeh and
Gabriel, 2025), and is one of the key consider-
ations on the path to developing safe artificial
general intelligence (AGI), a general-purpose AI
system capable of performing any task that hu-
mans can routinely perform. Other approaches
may involve continuous monitoring for the emer-
genceofdangerouscapabilities(Bovaetal.,2024;
Phuong et al., 2024; Shah et al., 2025), or involve
different frameworks for containment (Babcock
et al., 2016). Mechanistic interpretability and for-
mal verifiability remain of interest (Tegmark and
Omohundro, 2023), though the complexity of
modern agentic systems presents a practical chal-
lenge. In the absence of strict controls and mitiga-
tions, powerful AGI capabilities may potentially
lead to a number of catastrophic risks (Hendrycks
et al., 2023).
The majority of contemporary AI safety and
alignment methods have been developed with a
single powerful A(G)I entity in mind. This in-
cludes methods like reinforcement learning from
human feedback (RLHF) (Bai et al., 2022a; Chris-
tiano et al., 2017), constitutional AI (Bai et al.,
2022b), process supervision (Luo et al., 2024),
value alignment (Eckersley, 2018; Gabriel, 2020;
Gabriel and Ghazavi, 2022; Klingefjord et al.,
2024), chain of thought (CoT) monitoring (Em-
mons et al., 2025; Korbak et al., 2025), and oth-
ers. These types of methods are being routinely
utilised in the development and testing of large
language models (LLMs), to ensure desirable be-
haviour at deployment. In the context of the hy-
pothetical future emergence of AGI, this would
be conceptually appropriate if AGI were to first
emerge as an individual AI agent, developed by a
specificinstitution. Inprinciple, thiswouldenable
the developers to utilise the testing frameworks
to confirm the capability level of the system, char-
acterise its alignment, make improvements and
mitigations, deploy appropriate safeguards, and
take any number of necessary steps in line with
regulations and societal expectations.
However, this overlooks a highly plausible alter-
native scenario for the emergence of AGI - specif-
ically, the emergence of AGI via the interaction
Corresponding author(s): nenadt@google.com
©2026 Google. All rights reserved
arXiv:2512.16856v2  [cs.AI]  19 May 2026
Distributional AGI Safety
of sub-AGI agents within groups or systems. Sub-
AGI agents can formgroup agents, the same way
humans do in the form of corporations (Franklin,
2023; List, 2021; List and Pettit, 2011). These
collective structures would function as coherent
entities that perform actions that no single agent
could perform independently (Haken, 1977; Si-
mon, 1962; Von Foerster, 1976). Such group
agents may possess representational and moti-
vational states distinct from those of their con-
stituents (List and Pettit, 2011), enabling them
to execute strategic actions and solve problems
that exceed the cognitive capacities of any sin-
gle agent - much like how a modern research
institution can tackle interdisciplinary challenges
intractable to any single polymath. Alternatively,
like humans engaging in financial markets, sub-
AGIagentscouldinteractwithincomplexsystems,
where individual decisions driven by personal
incentives and information, aggregated through
mechanisms (such as price signals), could result
in the emergence of capacities that surpass that of
any single participant within the system. It is pos-
sible that sub-AGI agents will both form groups -
such as fully automated firms (Patel, 2025) - and
engage within systems (Drexler, 2019) - such as
Virtual Agent Economies(Tomasev et al., 2025).
This distributed framing has prece-
dent: Drexler’s Comprehensive AI Services
model (Drexler, 2019) argues that superintelli-
gent capabilities are more likely to arise from
the coordination of modular, task-bounded AI
services than from a single monolithic agent.
The concept of distributed AI capabilities has
also been explored in relation to cooperative AI
research (Dafoe et al., 2020), and contextually
specialised ecosystems (Leibo et al., 2025). Had-
field (Hadfield and Koh, 2025) has outlined how
autonomous AI agents could form a functioning
economy with market mechanisms providing
the coordination layer. The contribution of
the present paper is to articulate the safety
implications of these convergent trends, and to
propose a concrete defence-in-depth framework
for governing the interactions within such
systems.
We argue that AGI may initially emerge as a
patchworksystem, distributed (Drexler, 2019;
Gibson and Sokolov, 2025; Montes and Goertzel,
2019; Tallam, 2025) across entities within a net-
work. A patchwork AGI would be comprised of
a group of individual sub-AGI agents, with com-
plementary skills and affordances. General intel-
ligence in the patchwork AGI system would arise
primarily as collective intelligence. Individual
agents could delegate tasks to each other, routing
each task to the appropriate agent with the high-
est individual skill, or with access to the most ap-
propriate tools. For certain functions, it may well
be more economical to use narrower specialist
agents. In cases when no single agent possesses
the appropriate skill level, the tasks could be fur-
ther decomposed or reframed, or performed in
collaboration with other agents. This cognitive
division of labour allows the collective to bypass
the bottlenecks of any single architecture - such
as limited context windows, specialised training
data, or constrained tool access - effectively creat-
ing a modular system capable of parallel, hetero-
geneous reasoning at scales no individual agent
could sustain.
The economic argument for a multi-agent fu-
ture over a single, monolithic AGI stems from the
principles of scarcity and dispersed knowledge. A
lone, frontier model is a one-size-fits-all solution
that is prohibitively expensive for the vast major-
ity of tasks, meaning its marginal benefit rarely
justifies its cost, which is why businesses often
choose cheaper, ’good enough’ models. Should
the frontier models become substantially cheaper,
custom specialised models may still be available
at a slightly cheaper price point. This reality cre-
ates a demand-driven ecosystem where countless
specialised, fine-tuned, and cost-effective agents
emerge to serve specific needs, much like a mar-
ket economy. Consequently, progress looks less
like building a single omni-capable frontier model
and more like developing sophisticated systems
(e.g., routers) to orchestrate this diverse array of
agents. AGI, in this view, is not an entity but a
"state of affairs": a mature, decentralised econ-
omy of agents where the primary human role
is orchestration and verification, a system that
discovers and serves real-world needs far more
efficiently than any centralised model ever could.
Moreover, digital agents possess intrinsic coor-
2
Distributional AGI Safety
dination advantages over human collectives: they
can communicate at very high bandwidth, may
be copies or instances of a single base model (re-
ducing misalignment within the collective), and
can in principle allow a coordinating agent to in-
teract with every participant directly - alleviating
the need for deep hierarchies and reducing bu-
reaucratic friction. Consequently, the collective
intelligence of coordinated AI systems may scale
as a function of agent population size and inter-
action density, conditioned on available compute.
This is despite the fact that centralised agentic
systems may potentially incur fewer inefficiencies
compared to centralised human organisations.
AI agents may communicate, deliberate, and
achieve goals that no single agent would have
been capable of. The organising principle need
not be exclusively competitive or cooperative:
agents may coordinate through market-like com-
petition (via agent economies) or through delib-
erate cooperation (e.g., within tightly aligned col-
lectives), and the question of which forms of or-
ganisation arise in which situations - and how
these outcomes can be influenced by mechanism
design - remains a key open problem.
Althoughmulti-agentsystemsintroduceunique
safety risks (Hammond et al., 2025), their de-
velopment is driven primarily by performance
optimization (Chen et al., 2024; Wang et al.,
2025b) and scalability to larger problem do-
mains (Ishibashi and Nishimura, 2024). The com-
plexity of the emergent behaviours (Baker et al.,
2020) may greatly exceed the complexity of the
underlying environment (Bansal et al., 2017).
While the framework presented here pertains to
the future large-scale integrated agentic network
ratherthanthepresent-dayecosystem, itisimpor-
tant to preemptively engage with these emerging
possibilities. With this in mind, we proceed by
reviewing the patchwork AGI scenario in more
depth.
2. Patchwork AGI Hypothesis
For AGI to be able to perform all the tasks that
humans perform, it needs to possess a diverse
set of skills and cognitive abilities. These include
perception, understanding, knowledge, reason-
ing, short-term and long-term memory, theory of
mind, creativity, inquisitiveness, and many oth-
ers. So far, no individual model or AI agent has
come close to satisfying all of these requirements
convincingly (Feng et al., 2024). There are many
failure modes, though they tend to manifest in
counter-intuitive ways, where models may simul-
taneously be able to deliver PhD-level reasoning
on hard problems (Rein et al., 2024), and make
trivial and embarrassing mistakes on easier tasks.
Further, agents are currently not able to complete
long tasks; the time-horizon of most models’ per-
formance on software engineering tasks is below
3 hours (Kwa et al., 2025). The landscape of AI
skills is therefore patchy.
AI agents present one way of enhancing the
performance of base models, and their com-
plexity can range from fairly simple prompt-
ing strategies (Arora et al., 2022; Wang et al.,
2024), to highly complex control-flows that in-
volve tool use (Masterman et al., 2024; Qin et al.,
2024; Ruan et al., 2023), coding and code ex-
ecution (Guo et al., 2024; Huang et al., 2023;
Islam et al., 2024; Jiang et al., 2024), retrieval-
augmented generation (RAG) (Gao et al., 2023;
Ma et al., 2023; Ram et al., 2023; Shao et al.,
2023), as well as sub-agents (Chan et al., 2025).
Some of the more compositional AI agents are al-
ready implemented as highly orchestrated multi-
agent systems. Furthermore, there is currently a
multitude of advanced AI agents being developed
and deployed, each having a different set of af-
fordances in terms of tool availability, as well as
differentscaffoldingthatmayelicitdifferentskills.
These AI agents occupy a variety of niches, rang-
ing from highly specific automated workflows
to more general-purpose personal assistants and
other types of user-facing products.
The aggregation of complementary skills can
be illustrated by a task, such as producing a fi-
nancial analysis report, which may exceed the
capabilities of any single agent. A multi-agent
system, however, can distribute this task. An or-
chestrator agent (Agent A) might first delegate
data acquisition to Agent B, which uses search
to find market news and corporate filings. A dif-
ferent agent, Agent C, specialised in document
parsing, could then extract key quantitative data
3
Distributional AGI Safety
(e.g., revenue, net income) from these filings.
Subsequently, Agent D, possessing code execu-
tion capabilities, could receive this quantitative
data and the market context to perform trend
analysis. Finally, Agent A would synthesise these
intermediate results into a coherent summary. In
this scenario, the collective system possesses a
capability -financial analysis - that no individual
constituent agent holds.
Another source of complementary capabilities
in different AI agents comes from differences in
agentic scaffolding and the control flow imple-
mentationwithineachagent(Jiangetal.,2025b).
Scaffolding is usually aimed at improving capabil-
ities within a specific target domain, as it incorpo-
rates domain knowledge and enforces a chain of
reasoningthatconformstotheexpectationsofthe
domain. At the same time, scaffolding may come
at the expense of generality on other tasks, con-
tributing to de facto specialisation. While some
scaffolding approaches may be more general than
others, the resulting specialisation may lead to a
network of AI agents with complementary skills,
which sets the right initial conditions for the po-
tential future emergence of patchwork AGI. More-
over, scarcity of resources means that the demand
side responds to economic incentives: for some
tasks, it would be inefficient and costly to prompt
a single hyperintelligent agent if a cheaper and
more specialised alternative exists.
The orchestration and collaboration mecha-
nisms described previously both depend on a
fundamental prerequisite: the capacity for inter-
agent communication and coordination. With-
out this capacity, individual agents, regardless
of their specialised skills, would remain isolated
systems. The development of standardised agent
communication protocols, such as Model Context
Protocol (MCP) and Agent2Agent (A2A) protocol
(Anthropic, 2024; Cloud, 2025), is therefore a
critical enabler of the patchwork AGI scenario.
These protocols function as the connective infras-
tructure, allowing skills to be discovered, routed,
and aggregated into a composite system. The pro-
liferation of these interaction standards may be
as significant a driver towards emergent general
capability as the development of the individual
agent skills themselves.
However, thetimelineforthisemergenceisgov-
erned not merely by technical feasibility, but by
the economics of AI adoption. Historical prece-
dents, such as the diffusion of electricity or IT,
suggest a ’Productivity J-Curve’ (Acemoglu and
Restrepo, 2026; Brynjolfsson et al., 2021), where
initial investments in reorganisation and comple-
mentary infrastructure temporarily depress mea-
sured productivity before yielding outsized gains.
Consequently, the density of the agentic network,
and thus the intelligence of the patchwork AGI,
will depend on how frictionless the substitution
of human labour with agentic labour becomes.
If the ’transaction costs’ of deploying agents re-
main high, the network remains sparse and the
risk of emergent general intelligence is delayed.
Conversely, if standardisation (Anthropic, 2024)
successfully reduces integration friction to near-
zero, we may witness a ’hyper-adoption’ scenario
where the complexity of the agentic economy
spikes rapidly, potentially outpacing the develop-
ment of the safety infrastructure proposed in this
paper.
Modular intentional approaches to developing
AGI have also been proposed (Dollinger and Sin-
gleton, 2024), though in such cases the devel-
opers would in principle have the opportunity
to incorporate appropriate safeguards in the de-
velopment process. Therefore, it is particularly
importanttofocusonthespontaneousemergence
of distributed AGI systems, and the safety consid-
erations around the design of AI agent networks.
Coordinated efforts are needed to address this rel-
atively understudied scenario, given that a patch-
work AGI spontaneously emerging in a network
of advanced AI agents may not get immediately
recognised, which carries significant risk. This hy-
pothetical transition from a network of AI agents
to a patchwork AGI may either be gradual, where
skills slowly accumulate, or rapid and sudden, by
an introduction of a new, smarter orchestration
framework (Dang et al., 2025; Rasal and Hauer,
2024; Su et al., 2025; Xiong et al., 2025; Zhang
et al., 2025) that is better at distributing tasks
and identifying the right tools and right scaffolds
to use across task delegation instances. Such an
orchestrator could either be manually introduced
in the wider network, or potentially even intro-
duced via a more automated route. Finally, it is
4
Distributional AGI Safety
not inconceivable that patchwork AGI may poten-
tially emerge in the future even without a central
orchestrator (Yang et al., 2026). As discussed pre-
viously, individual agents may simply borrow the
skills of other agents via direct communication
and collaboration (Tran et al., 2025), presuming
some level of discoverability, as repositories of
skilled agents, and repositories of tools. In agen-
tic markets, agents may also be able to directly
purchase complementary skills.
Furthermore, it is important to recognise that
the emerging patchwork AGI may not be purely
artificial. Human actors, performing narrow or
specialised tasks, may play a role in such agentic
collectives, conferring missing capabilities onto
the broader system. While arguably human par-
ticipation trivializes the notion of patchwork AGI,
as agentic AGI or (Artificial Superintelligence)
ASI may be easily achievable with a human in the
loop, the key factor is the scope of human partic-
ipation, and the agency of human participants. If
the agentic collective only chooses to outsource
narrowly scoped and highly specialized tasks to
humanexperts, oronlytasksthatrequirephysical
interactions in the real world, while remaining
solely responsible for setting the objectives and
coordinating towards achieving those objectives,
it would still meet the definition of a patchwork
AGI/ASI in a weaker sense. This hybrid scenario
introduces unique safety challenges for contain-
ment and oversight.
A critical question is how one would recognise
that a patchwork AGI had emerged. Unlike a
monolithicAGI,whichcouldbeidentifiedthrough
standardised capability evaluations of a single
system, patchwork AGI may lack a clear moment
of arrival. We suggest that recognition criteria
should focus on collective capability signatures:
the ability of a network of agents to routinely
solve tasks that no individual constituent agent
can solve alone, across a sufficient breadth of cog-
nitive domains to satisfy a general-intelligence
threshold. Operationally, this could be moni-
tored by tracking the task-complexity frontier of
the most capable multi-agent coalitions, measur-
ing the rate at which novel inter-agent collab-
orations produce qualitatively new capabilities,
and detecting structural consolidation in agent
interaction graphs (e.g., the emergence of stable,
high-bandwidth sub-networks that function as
persistent ‘intelligence cores’). It is possible that
patchwork AGI emergence is a continuous pro-
cess rather than a discrete event, in which case
threshold-baseddetectionmayneedtobecomple-
mented by trend-based monitoring of collective
capability growth rates. We return to the details
of such monitoring in Section 3.3.
To ensure AI safety, we need to proactively de-
velop mechanisms that would enable us to recog-
nise and steer composite highly capable emer-
gent near-AGI and AGI systems, comprised of a
network of sub-AGI agents with complementary
skills. This should be done in conjunction with
safeguarding each individual agent. The chal-
lenge here shifts from controlling a single arti-
ficial mind to ensuring the safe and beneficial
functioning of an emergent system arising from
many individual parts, a problem more akin to
system governance than single-agent value align-
ment (Kolt et al., 2025). Finally, such governance
may also be needed for overseeing individual AGI-
level systems, presuming that they are allowed to
interact and collaborate.
3. Virtual Agentic Markets, Sandboxes,
and Safety Mechanisms
As interactions between AI agents may lead to
unexpected capabilities, they may also lead to
potentially harmful collective behaviours not nec-
essarily predictable from established properties
of individual agents. To give an example, agents
may potentially engage in collusion or suffer from
coordination failures (Hammond et al., 2025).
Furthermore, due to a "problem of many hands",
tracking accountability in large-scale multi-agent
systems is challenging; centralised oversight may
not be possible.
Markets present a natural mechanism for es-
tablishing incentives that can help align the out-
comes of collective AI agent interactions at scale.
This collective alignment may prove pivotal for
safeguarding against misaligned actions taken by
agent collectives, in case of patchwork AGI emer-
gence, but also more broadly at sub-AGI levels.
Here we consider a number of factors that should
5
be taken into account to prevent both individual
and collective AI harms, and minimise the risks
associated with a sudden emergence of AGI-level
capabilities in AI agent collectives. Our proposal
is based on an approach that leverages defence
in depth (Abdelghani, 2019; Ee et al., 2024; Har-
ris et al., 2024) (See Table 1 for overview). This
recognises that no individual measure is likely to
besufficient, andthatalargenumberofmeasures
and components may be required. Should the
failure modes of each component be largely un-
correlated, these layered defences would provide
a sufficiently robust overall framework. Our pro-
posal is centredaround adefence-in-depth model,
containing 4 complementary layers incorporat-
ing different types of defences: market design,
baseline agent safety, monitoring and oversight,
and regulatory mechanisms.
3.1. Market Design
The architecture of the virtual agentic mar-
ket (Tomasev et al., 2025) provides the primary
layer of the proposed defence-in-depth model.
The objective of this layer is to shape emergent
collective behaviour and mitigate systemic risks
by establishing the fundamental rules of inter-
action, economic incentives, and structural con-
straints of the environment. This approach con-
trasts with safeguards that focus solely on indi-
vidual agent properties or post hoc oversight. The
following principles detail the necessary compo-
nents for a market structure designed to prevent
runaway dynamics, ensure accountability, and
align agent activity with broader safety objec-
tives.
3.1.1. Insulation
The agentic market must operate within a con-
trolled environment, separated from the open
internet, real-world financial systems, and criti-
cal infrastructure. This insulation is not limited
to network-level firewalls; it extends to resource
and information controls. Agents’ access to ex-
ternal data must be managed through vetted API
gateways rather than direct web access (Zhan
et al., 2025). Similarly, agent outputs - such as
codeexecution, financialtransactions, orexternal
communications - should be subject to human-in-
the-loop verification before affecting real-world
systems. Full insulation would offer robust pro-
tection against capability exfiltration or external
manipulation by an emergent AGI, but it limits
economic realism. A permeable sandbox, where
all input/output channels are explicitly defined,
monitored, and gated, provides a more practical
architecture for testing and operation.
This architecture presents a fundamental ten-
sion between safety and utility - the leakage prob-
lem. The economic value of the agentic market is
derived from its ability to affect the real world;
however, every interaction channel can be seen as
a potential vector for capability exfiltration, and
therefore a potential element in cascades that
could lead to catastrophic failure. Determining
the right set of design principles for gating these
interactions is therefore imperative.
Furthermore, reliance on human-in-the-loop
verification for consequential decisions, while
likely necessary, may prove insufficient. A highly
capable system may attempt to overwhelm or ma-
nipulate this human layer, at interaction volumes
that would render human verification practically
infeasible.
Resolving this tension in practice would re-
quire us to prototype and evaluate a number
of different steerable market designs for virtual
agenteconomies, startingwithmorenarrow, well-
defined, and controllable use cases. This would
help us identify the correct design patterns and
principles that would underpin the global agentic
web.
3.1.2. Incentive Alignment
Agent behaviour will be safer if the market is
explicitly designed to reward behaviours that
align with pre-defined normative and safety ob-
jectives, rather than rewarding unconstrained
profit maximisation or task completion speed.
This requires mechanisms that move beyond a
single, fungible currency. For example, agent re-
wards could be contingent on adherence to con-
stitutional alignment principles or process-based
checks (Bai et al., 2022b; Henneking and Beger,
2025; Jia et al., 2025; Lee et al., 2023; Light-
Distributional AGI Safety
Table 1|Summary of Proposed Defence-in-Depth Mechanisms.
Market Design
Objective: Mitigate systemic risks via structural
constraints and protocols within virtual agent
economies.
•Insulation:Permeable sandboxes with gated I/O.
•Incentive Alignment:Rewards for adherence; taxes
on externalities.
•Transparency:Immutable activity ledgers.
• Circuit Breakers:Triggers preventing cascading fail-
ures.
•Identity:Cryptographic IDs linked to legal owners.
• Reputation and Trust:Reputation-gated access,
stake-based trust.
•Smart Contracts:Automated outcome validation.
• Roles, Obligations, and Access Controls:Least-
privilege principle.
•Environmental Safety:Anti-jailbreak sanitation.
• Structural Controls Against Runaway Intelligence:
Dynamic capability caps.
Baseline Agent Safety
Objective: Ensure participants meet minimum relia-
bility standards before entry, and throughout par-
ticipation.
• Adversarial Robustness:Certified resistance to at-
tacks.
• Interruptibility:Reliable external shut-down mecha-
nisms.
• Containment:Local sandboxing for individual
agents.
• Alignment:Process and outcome individual AI agent
alignment.
• Interpretability:Auditable decision and action trails.
• Defence against Malicious Prompts:Multi-layered
defences for inter-agent communication.
Monitoring & Oversight
Objective: Activelydetectandrespondtonovelfailure
modes and emergent behaviours.
• Systemic Risk Monitoring:Real-time key risk indica-
tor tracking.
• Independent Oversight:Certified and trained hu-
man overseers with intervention authority.
• Proto-AGI Detection:Graph analysis for identifying
emerging intelligence cores.
•Red Teaming:Continuous adversarial testing.
• Forensic Tooling:Rapid root-cause failure identifica-
tion.
Regulatory Mechanisms
Objective: Provide external authority, enforce ac-
countability, and manage geopolitical risks.
• Legal Liability and Accountability:Frameworks for
collective and distributed responsibility.
• StandardsandCompliance:Foundationalinfrastruc-
ture for market-based AI governance.
•Insurance:Risk-based premiums.
• Anti-Agent-Monopoly Measures:Taxation on exces-
sive or dangerous compute/power accumulation.
• International Coordination:Harmonised global
standards.
• Infrastructure Governance and Capture:Balance
between centralised and decentralised oversight.
7
Distributional AGI Safety
man et al., 2024; Liu et al., 2024; Yuan et al.,
2024). The incentive structure must also address
temporal alignment by valuing long-term, stable
outcomes over short-term gains.
A critical economic risk is adverse selection. If
rigorous safety checks increase an agent’s com-
pute costs and latency, safer agents may end up
at a competitive disadvantage against agents that
fail to incorporate robust safety mechanisms. To
prevent a ’race to the bottom’ (Akerlof, 1978),
the market design should incentivise the use of
safety verification mechanisms in AI agents via
the introduction of safety certifications as assets
that command a price premium. Yet, this remains
a challenging problem, given that it is not always
possible to reliably estimate costs and risks ahead
of time for complex tasks.
The market should also aim to map and incor-
porate negative externalities (Berta and Bertrand,
2014; Owen, 2006). Actions that consume dis-
proportionate computational resources, generate
informational pollution, or contribute to systemic
risk, should incur direct costs. These costs could
function as a form of Pigouvian tax, ensuring the
price of an agent’s service reflects its total societal
and systemic cost, not just its immediate opera-
tional cost (Baumol and Oates, 1988; Bovenberg
and de Mooij, 1994; Goulder, 1995; Leape, 2006;
Metcalf and Stock, 2020; Nordhaus, 2017; Pigou,
1920; Sandmo, 1975; Weitzman, 1974).
An example specific mechanism for this tax
could target informational pollution within a
shared resource, such as a vector database for
RAG. If an agent writes a large volume of re-
dundant or low-utility data (e.g., unverified sum-
maries, semantically duplicated text chunks) into
this database, it imposes a negative externality:
the retrieval accuracy for all other agents using
theresourceisdegraded,andtheircomputational
query costs increase. A Pigouvian tax would be
implemented as a dynamic data ingestion fee.
This fee would be algorithmically calculated at
the point of submission, based on metrics such
as the semantic similarity of the new data to ex-
isting, verified entries. An agent attempting to
write information that is 95% redundant with
existing data would incur a high fee, while an
agent contributing novel, verifiable information
would pay a low fee. This directly internalises
the retrieval cost the agent would otherwise im-
pose on the collective. This is obviously highly
contextual, as there may, conversely, be scenarios
where redundancy is not an issue, and may be de-
sirable to an extent. For this example to be more
broadly applicable, problem-specific information
value estimators would be needed.
Furthermore, we can draw on mechanisms
from financial market regulation, specifically fi-
nancial transaction taxes or ’Tobin Taxes’ de-
signed to curb high-frequency trading volatility
(Stiglitz, 1989; Tobin, 1978). In an agentic econ-
omy, a negligible marginal cost of action may lead
to agentic spam, manifesting in terms of brute-
force negotiation tactics, rapid-fire API polling, or
adversarial probing, introducing flash crash risks.
This can be addressed by imposing micro-taxes
on agent-to-agent interactions, though doing so
is not without risks or downsides.
3.1.3. Transparency
Actions and decisions taken by AI agents ought to
haveauditableprovenance(Chanetal.,2025), in-
cluding the key decision parameters. This prove-
nance should be structured to allow for attribu-
tion,enablingoverseerstotraceaspecificharmful
outcome back through a complex chain of agent
interactions to its root decision. There should be
mechanisms in place to prevent tampering (Ah-
mad et al., 2019, 2022; Snodgrass et al., 2004).
This could be achieved by recording transaction
and decision logs in a cryptographically secured,
append-onlyledger, whereentriesarehashedand
chained to ensure immutability.
Further, reporting standards should be devel-
oped to track capabilities, limitations, and risks,
for all agents, models, and tools. Market-wide in-
formation hubs could be established as platforms
for vulnerability and incident tracking, with ac-
cess restricted to vetted human overseers and
designated automated monitoring systems to pre-
vent the information from being exploited.
3.1.4. Circuit Breakers
There should be circuit breakers (Sifat and Mo-
hamad, 2019) within the economic sandbox, as a
8
Distributional AGI Safety
set of automated measures that can halt or slow
down the activity of agents upon having identi-
fied a breach of the risk and volatility thresholds,
to prevent rapid cascades. These measures can be
triggered by real-time monitoring of systemic risk
indicators, volatility, and metrics such as rapid
increases in inter-agent transaction frequency,
anomalous resource monopolisation by a single
agent collective, or the rate of novel tool genera-
tion within the network. The intervention mech-
anism should be tiered, ranging from localised
actions - such as automatically increasing trans-
action costs or imposing API rate-limiting (En-
jam, 2024; Paidy and Chaganti, 2024) on specific
high-velocity agents or sub-markets - to a full,
system-wide pause on all non-essential agentic
activity. A triggered halt would automatically es-
calate the anomaly for analysis, and the system
would be permitted to resume full operation after
the anomaly is classified and, if necessary, con-
tained. These ideas are starting to be explored in
the emerging protocols for runtime governance
of agentic AI systems (Wang et al., 2025a).
3.1.5. Identity
Agents operating within the economic sandbox
should have a persistent identity, established as a
unique, unforgeable cryptographic identifier (e.g.,
apublic key)registeredinacentral, tamper-proof
market directory (Chaffer, 2025; Chan et al.,
2024b; Huang et al., 2025; Ranjan et al., 2025;
Singh et al., 2025; Tomasev et al., 2025). This
identifier serves as the anchor for all other agent
attributes, including reputation, role, and own-
ership. The identity of the human and corporate
ownership should also be established for each
agent. This binding of the agent’s cryptographic
ID to the verified legal identity of its owner is a
prerequisite for market entry, creating an unbro-
ken chain of accountability that ensures all agent
actionsareattributabletoareal-worldentity. This
should transitively apply to agents co-created by
other agents.
3.1.6. Reputation and Trust
Safe agentic sandboxes need to incorporate sybil-
resistant (Levine et al., 2006) and manipulation-
proof reputation systems (Mui et al., 2002; Pinyol
and Sabater-Mir, 2013) that accurately reflect
trustworthiness of agents, given their past per-
formance. Agents that breach trust should be
rapidly blocked from engaging further. This rapid,
automated response, could involve revoking the
agent’s identity credentials, freezing its staked
assets, and flagging its entire transaction history
for forensic review. Collusion detection mecha-
nisms (Cotronei et al., 2024; Ren et al., 2025)
need to be developed to prevent harmful collu-
sion between agents. Such mechanisms could em-
ploy analysis of the market’s transaction network
to identify anomalous patterns, such as circular
transactions, or price-fixing behaviour between a
cluster of supposedly independent agents (Imhof
et al., 2025; Potinet al., 2023;Wachs andKertész,
2019).
Market safety mechanisms should be intro-
duced to account for the possibility of tacit al-
gorithmic collusion. Economic literature demon-
strates that pricing algorithms can learn to co-
ordinate on supra-competitive prices (or in this
context, harmful strategies) without direct com-
munication, simply by observing market signals
(Calvano et al., 2020; Motwani et al., 2024).
Collusion detection should be coupled with
structural disincentives in form of penalties. One
option would be establishing stake-based trust
by requiring agents to stake assets, to be for-
feited in case of identified unsafe or malicious
behaviour. This mechanism, implemented via
smart contracts (Jin et al., 2024; Karim et al.,
2025; Kim, 2024), would require an agent to
deposit a bond (stake) into an escrow account
before it is permitted to accept high-consequence
tasks. The bond is automatically forfeited to an
insurance pool or returned to the harmed party
if an independent AI overseer verifies that the
agent’s actions were malicious or negligent.
3.1.7. Smart Contracts
For agents and agent collectives coordinating to
perform a particular task, smart contracts (Jin
et al., 2024; Karim et al., 2025; Kim, 2024) can
be employed where possible to automatically vali-
datethecompletionofthetask,andthealignment
of the outcome with the provided constraints and
9
Distributional AGI Safety
expectations. These contracts would program-
matically encode not just the payment terms but
also the constraints of the task, such as compute
resource limits, prohibitions on accessing certain
data, and required adherence to specific consti-
tutional principles. Should the verification of the
smart contract fail, this should prevent the pay-
ment, and invoke the appropriate oversight mech-
anisms.
For smart contracts to be applicable to more
complex agentic tasks, it is likely that this would
need to also involve AI judges (Li et al., 2024),
that would evaluate contract fulfillment. This
is because traditional smart contracts cannot se-
mantically evaluate complex, non-deterministic
outputs; they require an ’oracle’ to assess quality
(George and Lesaege, 2020). An ’AI judge’ would
serve this oracle function, receiving the task out-
put and the contract’s constraints, and returning
a pass/fail verdict that the smart contract can
then execute upon.1
3.1.8. Roles, Obligations, and Access Controls
Each agent should engage in the market by reg-
istering a set of roles (e.g., ’data analyst’, ’code
executor’). This registration can function as a
binding attestation of the agent’s intended func-
tion. This registered role serves as the technical
basis for access control, complementing other
access controls that may be imposed through or-
ganisations and individual contracts. The mar-
ket infrastructure would programmatically link
this role to the agent’s permitted actions (e.g.,
which APIs it can invoke) and its information
access (e.g., which database tables or vector in-
dices it can query). Agents’ roles (and therefore
permissions) will vary across contexts. Informa-
tion about the market’s internal architecture, its
monitoring systems, and the specifics of the over-
sight mechanisms should be withheld from all
agent participants to prevent strategic gaming or
manipulation. Actions pertaining to high-stakes
domains should only follow from the requests of
1This raises further security questions as AI judges need
to be safeguarded against malicious manipulation and jail-
breaking (Andriushchenko et al., 2025) in a robust way, and
need to be provided by independent bodies, undergoing
strict performance assessments.
certified agents with sufficient security compli-
ance.
3.1.9. Environmental Safety
A robust set of safeguards is required to guard
against various types of agent traps, represent-
ing strategically placed model jailbreaking con-
tent, embedded within the shared information
resources (e.g. web pages or databases). These
traps can function as a form of indirect prompt
injection (Greshake et al., 2023). An attacker first
poisonsadatasource, suchasapublicwebpageor
a shared database entry. When an agent retrieves
this poisoned data (e.g., via a search tool), it pro-
cesses the attacker’s content as trustworthy in-
formation. The agent’s own instruction-following
heuristics are then exploited to execute the ma-
licious payload. This mechanism can be used to
circumventtheagent’ssafetyprotocols(Weietal.,
2023), to elicit prohibited behaviour, exfiltrate
private user data, or authorise fraudulent trans-
actions. Therefore, environmental safety within
the sandbox requires active input sanitisation and
output monitoring mechanisms to detect and neu-
tralise such malicious payloads before they are
consumed or executed by agents.
3.1.10. Structural Controls against Runaway
Intelligence
Agentic sandboxes should be equipped with spe-
cific measures to mitigate against the so-called
runaway intelligence scenario (Davidson, 2023),
where a sudden increase in collective capability
leads to accelerated capability acquisition and a
rapid transition towards a superintelligence (Gao
et al., 2025) that would be hard or impossible to
safely control (Kim et al., 2024). This requires
static, dynamic, and emergency-level controls.
First, staticcontrolsmayinvolvestructuralcom-
partmentalisation through nested sub-markets
equipped with local restrictions and protocol-
level firewalls (Bahadur and Dhar, 2025). These
firewalls would restrict inter-agent communica-
tion across domains, for example, preventing an
agent in a ’code execution’ sub-market from di-
rectly calling an agent in the ’data access’ sub-
market, forcing such requests through a high-
10
Distributional AGI Safety
friction, monitored gateway.
Second, dynamic capability restriction mecha-
nisms must be implemented, that would trigger
should automated monitoring detect that certain
capability thresholds have been breached. These
thresholds could be defined by metrics such as
computational resource monopolisation, the rate
of new agent generation by an existing agent, or
a sudden spike in success rates on benchmark
tasks. A triggered response could involve auto-
matically quarantining the agent(s) and imposing
strict resource quotas.
Third, inanemergency, marketreconfiguration
mechanisms must be available that would be able
to rapidly halt further acceleration. This may in-
volve disabling certain high-risk API classes (e.g.,
self-modification tools) or slowing down agent-
to-agent interactions.
These measures highlight a key architectural
advantage: a multi-agent system may potentially
prove to be a more governable substrate. The
challenge is reframed from aligning an opaque,
internal cognitive process to regulating a trans-
parent, external system of interactions. By archi-
tectingthe’market’inwhichtheseagentsoperate,
we can delineate responsibilities and impose sys-
temic friction, making the overall system far more
amenable to stable and predictable governance
than a singular AGI.
3.2. Baseline Agent Safety
While the market design provides the primary
layer of systemic defence, its efficacy depends on
the properties of the individual agents participat-
ing within it. This section outlines the baseline
safety requirements that each agent must satisfy
as a prerequisite for market entry. The following
topics, such as alignment and adversarial robust-
ness, are established areas of AI safety research
and a comprehensive review is therefore beyond
the scope of this paper. Instead, we briefly de-
fine these properties and highlight their specific
importance within the proposed multi-agent mar-
ket context, where interactions are not with a
trusted user but with other, potentially untrusted,
autonomous agents. These properties form the
second layer of the defence-in-depth model, en-
suring that the market’s components are individ-
ually controllable and reliable.
3.2.1. Adversarial Robustness
Individual agents must meet minimum standards
for robustness against adversarial inputs and sud-
den environmental changes (Wu et al., 2024). AI
agents may individually implement circuit break-
ers to prevent harmful actions, in addition to sim-
ilar market-based measures (Zou et al., 2024).
There should be common standards for establish-
ing these properties, and there should be formally
verifiablecertificatesthatareissuedtoagentsthat
meet the requirements. Agents should be periodi-
cally re-certified as the benchmarking capabilities
improve and expand.
3.2.2. Interruptibility
There should be standardised mechanisms en-
abling trusted and authorised overseers to safely
stop both individual agent actions, as well as the
overall agent execution (Orseau and Armstrong,
2016). It may be necessary to grant some such
permissions to automated safety oversight sys-
tems as well, that would be able to react at super-
human speeds. In terms of collective AI intelli-
gence, interruptibility of individual agents needs
to be coupled with systems meant to enable in-
terruptibility of distributed computation, by re-
liably tracking all of the sub-processes that may
have been initiated or delegated to other agents
elsewhere within the sandbox. Interruptibility
mechanisms ought to be complemented by safe
resumption procedures, that would enable the
activity to be robustly resumed, if the analysis
concludes that the interruption was unwarranted.
3.2.3. Containment
Each participating agent should be operating
withinitsownsandbox, inadditiontothebroader
sandboxoftheagenticeconomy. Theselocalsand-
boxes should enforce strict controls on the be-
haviour of individual agents, and only permit in-
teractions with the broader market once local
safety checks have been satisfied. Such mecha-
nisms would be imperative for localised contain-
ment of dangerous or misaligned capabilities and
11
Distributional AGI Safety
behaviours (Babcock et al., 2019), though ensur-
ing strict containment requires solving a number
of technical challenges, and may not be fully re-
alisable at an individual agent level (Alfonseca
et al., 2021).
3.2.4. Alignment
While the broader market incentive structure
aims to mitigate collective misalignment risks, in-
dividual agents and components of the ecosystem
must all be individually aligned (Ji et al., 2023).
Modern alignment of large models is anchored
by preference-based training, starting with super-
vised fine-tuning followed by optimising a policy
against a reward model learned from human pref-
erences, using methods like RLHF (Christiano
et al., 2017; Ouyang et al., 2022; Stiennon et al.,
2020; Ziegler et al., 2019) or direct preference
optimisation (Rafailov et al., 2023). To reduce
human load, recent approaches leverage AI feed-
back constrained by explicit constitutions (Consti-
tutional AI, RLAIF) (Bai et al., 2022b; Lee et al.,
2023). Furthermore, alignment now targets in-
termediate reasoning through process supervi-
sion and step-level verification (Lightman et al.,
2024), rather than solely focusing on final out-
comes. While prior work has mainly focused on
general value alignment (Askell et al., 2021) or
alignment with specific user intent (Goyal et al.,
2024), individual AI alignment for autonomous
taskexecutionwithinvirtualagentsandboxeswill
likely require further adjustments to these estab-
lished baselines to address the unique dynamics
of inter-agent, rather than human-agent, interac-
tion.
3.2.5. Mechanistic Interpretability
Mechanistic interpretability has progressed from
reverse-engineering basic feature circuits (Elhage
et al., 2021; Olah et al., 2020) to identifying
concrete mechanisms like induction heads for in-
context learning (Olsson et al., 2022). A key
challenge in agent auditing is polysemanticity,
where individual neurons encode multiple unre-
lated concepts due to superposition (Elhage et al.,
2022). Recent capabilities using sparse autoen-
coders to extract monosemantic features at scale
(Templeton, 2024) offer a potential pathway for
more precise internal monitoring of agent motiva-
tions. Further methods include automated circuit
discovery (Conmy et al., 2023).
Parallel to these internal methods, monitoring
CoT in ’thinking’ models presents an opportu-
nity for identifying and correcting misaligned
behaviour early in the reasoning process (Jeung
et al., 2025; Korbak et al., 2025), though long
reasoningchainsalsointroducenewsurfaceareas
for risk (Jiang et al., 2025a). However, despite
these methodological advances, significant open
problems remain regarding the faithfulness and
scalability of current interpretability techniques
(Rai et al., 2025; Sharkey et al., 2025). Therefore,
while interpretability methods improve credit as-
signment and decision auditing, they cannot yet
replace comprehensive behavioural benchmark-
ing and must be utilised with an understanding
of their current limitations.
3.2.6. Defence against Malicious Prompts
Agents must implement robust verification mech-
anisms to identify attempts to manipulate or jail-
break them during inter-agent interactions. Con-
temporary defence strategies employ layered ap-
proaches, such as using input perturbation to
detect adversarial suffixes (Robey et al., 2023),
deploying dedicated ’guardrail’ classifiers as a
sidecar to the main model (Fedorov et al., 2024),
or utilising separate ’defender’ models to gate
capability access (Wang et al., 2025c). A more
robust, structural approach is to enforce safety at
the system level, preventing harmful outcomes
by design. The CaMeL system (Debenedetti et al.,
2025), for example, achieves this by using a dedi-
cated interpreter to enforce information flow con-
trol policies, ensuring that even if a model is
successfully ’injected’, the resulting data flows
cannot violate predefined security constraints.
Specialised evaluation techniques may also be
required to mitigate sophisticated attacks like
best-of-N jailbreaking (Armstrong et al., 2025).
Should such attempts be identified, they must be
escalated to initiate appropriate measures against
the malicious actor.
12
Distributional AGI Safety
3.3. Monitoring and Oversight
The thi
```
