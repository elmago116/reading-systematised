---
title: Cognitive Agent-Based Modeling to Optimize Complex Project Management Under Uncertainty
author: Liliana M. Pantoja-Rojas, Marco A. Alzate-Monroy, Vãctor H. Medina-Garcãa, Luis G. Moreno-Sandoval
year: "2025"
Type: Journal Article
DOI: 10.1109/access.2025.3588816
source: https://doi.org/10.1109/access.2025.3588816
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
pdfORepub: "[[Cognitive Agent-Based Modeling to Optimize Complex Project Management Under Uncertainty.pdf]]"
---
[[Cognitive Agent-Based Modeling to Optimize Complex Project Management Under Uncertainty.pdf]]
## Full text (extracted from `Cognitive Agent-Based Modeling to Optimize Complex Project Management Under Uncertainty.pdf`)

*Source:* `2PDF/Cognitive Agent-Based Modeling to Optimize Complex Project Management Under Uncertainty.pdf`  
*Extracted:* 2026-06-18

```text
Received 10 June 2025, accepted 7 July 2025, date of publication 14 July 2025, date of current version 24 July 2025.
Digital Object Identifier 10.1 109/ACCESS.2025.3588816
Cognitive Agent-Based Modeling to Optimize
Complex Project Management Under Uncertainty
LILIANA M. PANTOJA-ROJAS
1, (Graduate Student Member, IEEE),
MARCO A. ALZATE-MONROY1, (Senior Member, IEEE), VíCTOR H. MEDINA-GARCíA
1,
AND LUIS G. MORENO-SANDOVAL
2
1Engineering Faculty, Universidad Distrital Francisco José de Caldas, Bogotá 110231, Colombia
2Engineering Faculty, Pontificia Universidad Javeriana, Bogotá 110231, Colombia
Corresponding author: Liliana M. Pantoja-Rojas (lmpantojar@udistrital.edu.co)
This work was supported by the Pontificia Universidad Javeriana.
ABSTRACT This paper presents an agent-based simulation model with cognitive elements, developed to
explore strategies for managing complex projects under uncertainty. The model was implemented using
NetLogo, which provided a matrix-structured environment where agents—identified as assigners and
workers—interact based on factors such as expertise level, intensity of collaboration, frequency of task
rotation, and workload balance. The system was simulated over 100 time steps, allowing the identification of
behavioral patterns related to organizational learning and performance under varied experimental conditions.
Methodologically, the model integrates mechanisms for distributing tasks, rules for agent assignment,
adjustable collaboration ranges, and decision-making based on utility functions. Cognitive aspects are
addressed through decentralized decision processes and adaptive behaviors that evolve during the simulation.
A total of eight configurations were analyzed, varying turnover rates, collaboration distances, and the
initial competencies of the agents to assess how these variables influence the accumulation of experience
and project effectiveness. The results indicate that when agents build up experience over time, project
outcomes improve, following a growth curve with diminishing marginal returns. Conversely, high turnover
interferes with knowledge retention and weakens learning processes. Additionally, too much collaboration
can overwhelm highly connected agents, thereby decreasing the system’s overall efficiency. Statistical
validation was carried out through ANOV A and Spearman’s correlation tests, confirming the consistency and
relevance of the observed effects. Overall, the study underscores the importance of organizational continuity
and the thoughtful design of collaboration parameters to achieve efficient performance in complex project
settings. The proposed model serves as a useful framework for examining how task distribution, talent
retention, and interaction patterns can be optimized, and it opens the door to future developments involving
more advanced cognitive modeling techniques.
INDEX TERMSSimulation, knowledge management, personnel management, project analysis, adaptation.
I. INTRODUCTION
Project management encompasses the planning, coordina-
tion, direction, and control of resources to meet defined
goals within a specific timeframe [1], [2]. Nonetheless,
contemporary project environments are increasingly char-
acterized by uncertainty and complexity, driven by rapid
technological change and evolving operational demands [3],
The associate editor coordinating the review of this manuscript and
approving it for publication was Fabrizio Messina
.
[4]. These conditions have become central in recent academic
discussions due to their direct implications for successful
project execution. The presence of multiple, and some-
times conflicting, objectives, coupled with heterogeneous
workforces and interdependent team structures, significantly
amplifies managerial complexity [5], [6], [7].
Such conditions make it particularly challenging to
deliver projects on time and within budget [8], [9], [10].
In response, recent methodologies have integrated data
analytics and advanced visualization techniques to support
VOLUME 13, 2025

 2025 The Authors. This work is licensed under a Creative Commons Attribution 4.0 License.
For more information, see https://creativecommons.org/licenses/by/4.0/ 127263

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
decision-making in unpredictable contexts [11]. Among
these, Earned Value Management (EVM) stands out as a
widely implemented tool for performance tracking [12].
Originating from U.S. Department of Defense initiatives
in the 1960s, EVM offers a quantitative mechanism for
comparing planned versus actual cost and schedule per-
formance [13] and has since been adopted across various
industries, including construction and engineering [14].
Despite its popularity, the EVM presents notable limita-
tions, particularly in projects that require broader evaluations
of effectiveness. By emphasizing cost and schedule compli-
ance, EVM often neglects qualitative aspects such as task
execution quality, intra-team collaboration, and personnel
motivation [13], [15], [16], [17], [18]. These limitations
are especially acute in developing countries, where EVM
applications are underreported, leaving critical gaps in
understanding its applicability within resource-constrained or
structurally complex settings [19]. Furthermore, much of the
existing literature assumes a uniform workforce, overlooking
the variability introduced by individual differences in perfor-
mance and adherence to project protocols [15], [20].
To overcome these shortcomings, there is a need for more
adaptive frameworks that can respond flexibly to dynamic
project conditions. In this regard, recent contributions
advocate for incorporating complex systems thinking and
adaptive leadership into project management strategies [21],
[22], [23]. An auspicious approach is the use of Agent-Based
Modeling (ABM), which simulates the autonomous actions
and interactions of individual agents, thereby enabling
the emergence of system-level behaviors that traditional
analytical models do not readily capture [24], [25], [26].
Within this context, the current study presents a sim-
ulation framework developed in NetLogo that seeks to
model the inherent complexity of managing large-scale
projects [27], [28]. The model features agents that inter-
act under varying conditions of expertise, collaboration,
turnover, and workload, thereby providing insight into
how local decision-making scales into global performance
dynamics. By aligning with the conceptual foundations of
complex systems and cognitive agents, this work offers a
novel contribution to the field of project management, rein-
forcing the utility of computational approaches in studying
multidimensional, adaptive environments.
II. CONCEPTUAL FRAMEWORK
The following section introduces the theoretical background
that informs the chosen simulation framework, emphasizing
principles from complexity science and cognitive agent
modeling to confront the inherent challenges of complex
project environments.
A. COMPLEX SYSTEMS
A complex system consists of interconnected elements that
interact with one another, giving rise to emergent and
non-trivial properties and behaviors that cannot be fully
understood by analyzing each component in isolation [11],
[23], [29]. The system’s behavior depends more on the
dynamic relationships among its components than on their
individual properties [30]. For this reason, complexity
science has gained increasing relevance across various disci-
plines, including biology, physics, chemistry, economics, the
social sciences, and cultural studies [31]. Notable examples of
complex systems include the human brain, cells, ecosystems,
cities, and social networks [32], [33], which more accurately
reflect real-world phenomena than models based on isolated
systems [34].
However, the detailed analysis of such systems presents
considerable challenges for traditional analytical meth-
ods [30], [35], as their dynamic nature gives rise to
phenomena such as emergence, autopoiesis, and self-
organization [34], [36], [37], [38]. In this context, scientific
advances in the study of complexity have been closely
linked to technological developments, enabling the modeling
and simulation of behaviors resulting from component
interactions [39]. These tools have been instrumental in
uncovering internal dynamics and emergent properties,
thereby facilitating the analysis and application of complexity
in various domains [40], [41].
Among these phenomena, emergence refers to the appear-
ance of global properties resulting from the interactions
and dynamics among system components—properties that
generate novel information not present in the individual
elements [34], [35]. Autopoiesis, in turn, refers to a
system’s ability to maintain and reproduce through its
internal processes and reflects the relationship between the
system’s complexity and its environment [29]. Ultimately,
self-organizing phenomena emerge when decentralized inter-
actions among system elements produce coherent global
behaviors, often aimed at reducing conflict and enhancing
cooperative efficiency [3], [42], [43].
From this standpoint, project management environments
exhibit hallmark traits of complex systems, given the
dense web of interrelations and functional dependencies
that characterize their structure [44], [45], [46]. Addressing
such intricacy necessitates the adoption of specialized
methodologies, including simulation-based tools, configu-
ration oversight, risk mitigation strategies, and structured
team coordination [5], [11]. A thorough grasp of systemic
complexity and uncertainty is therefore pivotal in formulating
strategies that are both adaptive and resilient to change [43],
[47]. This conceptual evolution has prompted the formulation
of both theoretical constructs and applied frameworks
to confront the multifaceted demands of modern project
execution.
B. COMPLEXITY AND UNCERTAINTY IN PROJECT
MANAGEMENT
Project management has developed various approaches to
ensure the achievement of objectives within established time-
frames [48]. This discipline has been consolidated as a
127264 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
formalized system and structured methodology supported by
theories, principles, and practices promoted by institutions
such as the Project Management Institute (PMI) [49] and the
International Project Management Association (IPMA) [50].
From this perspective, the traditional approach emphasizes
planning and control to create models and guidelines
that optimize project execution [22], [51]. This paradigm
focuses on managing three key dimensions—time, cost, and
scope [52] and proposes strategies to anticipate and control
potential deviations.
Several strategies have been implemented within this
framework to address the uncertainty inherent in projects.
Risk management is one of the most established approaches,
focusing on identifying, assessing, and mitigating the
potential impacts of decisions that may negatively affect
project development [53], [54]. This approach involves the
systematic analysis of threats and opportunities, formulat-
ing contingency plans, and implementing monitoring and
control mechanisms to enable timely responses to unfore-
seen events [55], [56], [57]. In addition, complementary
approaches address other critical dimensions, such as value
management, which seeks to maximize project efficiency
and effectiveness by evaluating alternatives based on their
ability to generate tangible stakeholder benefits [14]; resource
management, which aims to optimize the use and availability
of assets [12] and stakeholder management, which promotes
active collaboration, alignment of expectations, and effective
communication throughout the project life cycle [18], [22],
[58], [59].
However, despite these methodological advances, tradi-
tional approaches have proven insufficient in today’s volatile
environment, characterized by globalization, technological
acceleration, and increased complexity and uncertainty [60],
[61]. Organizations have adopted more flexible structures
and adaptive practices to remain competitive [62]. However,
significant limitations persist even with adjustments aimed at
process optimization, cost reduction, or schedule adaptation
[63]. These challenges stem primarily from the heterogeneity
of stakeholders, the variability of their expectations, and the
inability of conventional models to adequately capture the
fortuitous, evolving, and experimental behaviors inherent in
complex projects [64], [65].
Project complexity can be understood through four key
dimensions: size, variety, interdependencies and interrela-
tions, and the surrounding environment [3]. The interaction
of these factors creates high levels of uncertainty, which
are exacerbated by poor role allocation, ineffective team
selection, or lack of coordination across areas [66]. Addi-
tionally, integrating multiple disciplines involving numerous
stakeholders, constant requirement changes, ambiguity, and
nonlinear relationships further intensify complexity [57],
[67]. When these factors are poorly managed, they may lead
to delays, cost overruns, or even project cancellation [68].
Nonetheless, when addressed strategically, complexity can
become a source of opportunity for organizational learning,
adaptation, and evolution [69].
Considering this scenario, it is necessary to adopt
approaches that acknowledge individuals’ capacity to per-
ceive, interpret, and act in changing conditions [70]. In this
regard, cognitive agent-based models offer a promising alter-
native by representing project participants as task executors
and entities with bounded rationality, learning capabili-
ties, and adaptive behavior [25]. These agents can make
autonomous decisions based on incomplete information,
past experiences, and expectations about the environment,
enabling a more realistic simulation of the complex dynamics
and emergent processes that define contemporary project
management.
C. COGNITIVE AGENTS IN PROJECT MANAGEMENT
One of the main challenges in managing complex projects is
the ambiguity of information, which is often limited or unre-
liable. This uncertainty hinders informed decision-making
and may generate nonlinear connections between different
project parts, where small changes can trigger unforeseen
effects in other areas [71]. As a result, measuring progress
and evaluating project success becomes a complex task,
obstructing the early detection of issues and the timely
implementation of corrective actions [72].
In response to this scenario, cognitive agents have
emerged as an innovative tool for managing uncertainty and
supporting decision-making in dynamic contexts [73]. These
agents, implemented through computer programs, simulate
the behavior of autonomous entities with capabilities for
information processing, learning, and decision-making [27].
Through simulation models, they enable the identification
of behavioral patterns, the anticipation of scenarios, and
the analysis of the impact of various decisions—thereby
strengthening strategic analysis and systemic project under-
standing [27], [74], [75].
Beyond improving planning and coordination, cognitive
agents also contribute to proactively identifying risks and
opportunities throughout the project life cycle [25]. Through
continuous monitoring, they facilitate the detection of
threats and the management of changes in scope, dead-
lines, or budgets, allowing for more accurate evaluation
of the implications of such adjustments [76]. Simultane-
ously, cooperation among multidisciplinary teams, effective
communication, and knowledge sharing have become key
success factors [77], [78]. This evolution has encouraged the
adoption of technological tools such as NetLogo, an agent-
based modeling platform widely used by researchers and
practitioners to interactively represent complex interactions
and group dynamics [27], [79], [80].
Despite these advances, gaps remain in the literature,
particularly regarding micro-level management aspects such
as collaboration, staff turnover, and individual expertise [25],
[81], [82], [83]. Therefore, a methodological approach is
required to capture the inherent complexity of project
management systems by integrating the cognitive capacities
of agents and the structural interactions within the environ-
ment. In this regard, cognitive agent-based modeling offers
VOLUME 13, 2025 127265

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
FIGURE 1. Modeling stage. Source: Adapted from [27].
a suitable strategy for representing individual behaviors,
decision-making processes, and emergent patterns character-
istic of adaptive systems. The following section describes the
methodology used in this study, including the selected tools
and the criteria that guided the design and implementation of
the model.
III. METHODOLOGY
Cognitive agent-based modeling has gained increasing
relevance across disciplines by enabling the simulation
of intelligent behaviors in complex environments. Various
tools have been developed to support this purpose, each
offering distinct capabilities tailored to specific modeling
needs. Repast [84] is commonly applied in social sciences
and economics, while MASON [85] is known for its
efficiency in large-scale simulations. AnyLogic [86] offers
a hybrid modeling approach that integrates agent-based,
system dynamics, and discrete-event simulations. This study
selected NetLogo as the simulation environment due to its
robustness in modeling [27], [80] heterogeneous agents,
and capturing non-linear interactions in complex adaptive
systems [87], [88], [89], [90].
The model construction process adopted the methodology
proposed by [27], which outlines six fundamental phases
for developing agent-based models. These phases include
defining the research questions, identifying the model’s
elements, characterizing the agents, implementing the model
in the simulation platform, calibrating the model, and
designing scenarios. This methodological structure provides
a rigorous foundation for aligning theoretical assumptions
with the computational representation of the system—an
essential aspect when modeling complex socio-technical
environments. Fig. 1 illustrates these specific stages of the
modeling process, which served as a guide for the design and
implementation of the model in this study.
This methodological sequence enabled a coherent integra-
tion of theory, computational design, and empirical analysis,
ensuring that each stage of the study was grounded in both
solid conceptual foundations and technical rigor.
Fig. 1, adapted from [91], illustrates the expanded work-
flow, showing how the various components of the process
are interconnected. The theoretical framework guides the
model design, and agent behavior rules are encoded based
on well-defined assumptions. Results are evaluated through
key indicators and empirical comparisons. This methodology
promotes a systemic, iterative, and adaptable perspective,
allowing for continuous refinement of the model, enhanced
predictive capacity, and ensured relevance across various
applied research contexts.
FIGURE 2. MBA research paper methodology. Source: Adapted from[91].
Therefore, to ensure methodological rigor, the model
development followed a structured process based on previ-
ously established guidelines. The methodology consisted of
four main stages:
• Stage 1 – Literature Review and Design Criteria
A thorough literature review was conducted to identify
key variables influencing the management of complex
projects, including collaboration, individual expertise,
and turnover dynamics. These findings guided the
conceptual structure and behavioral assumptions of the
simulation model.
• Stage 2 – Simulation.
To code the simulation logic, define entities, and param-
eterize variables, NetLogo (https://ccl.northwestern.edu/
netlogo/) was used. NetLogo is a modeling environment
developed by Northwestern University, widely recog-
nized for its ability to represent heterogeneous agents
and capture non-linear interactions within complex
adaptive systems [87], [88], [89]. This phase included
127266 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
defining agent types, setting initial conditions, and
implementing behavioral rules, although the detailed
model structure is presented in Section IV.
NetLogo was additionally selected due to its visually
intuitive interface and flexible programming architec-
ture, which allow the simulation of autonomous agents
with cognitive abilities such as perception, learning, and
decentralized decision-making. These features proved
essential for analyzing key phenomena in complex
project management, such as agent collaboration, indi-
vidual expertise, and staff turnover dynamics [87], [90],
[91].
• Stage 3 – Scenario Testing and Experimental Design
A set of simulation scenarios was implemented to
explore emergent organizational behaviors under differ-
ent environmental conditions. To this end, experiments
were designed that systematically modified key model
variables, such as the agents’ collaboration radius, staff
turnover rate, and initial level of individual expertise.
These variations enabled the analysis of how different
configurations affected system dynamics, overall project
performance, and the emergence of non-trivial collective
patterns. The adopted experimental approach facilitated
the identification of critical points and the evaluation
of potential strategic interventions aimed at improving
efficiency and adaptability in the management of
complex projects.
• Stage 4 – Model Validation
To ensure methodological rigor and statistical robustness
of the results, two widely recognized tests in simulation
analysis were applied: one-way Analysis of Variance
(ANOV A) and Spearman’s rank correlation coefficient.
ANOV A is an inferential statistical technique used
to assess whether significant differences exist among
the means of several experimental groups. This test
partitions the total variance observed in a dependent
variable into two components: the variance explained
by the factor effect (between groups) and the residual
variance (within groups), using the F-statistic to test
the null hypothesis of equal means [93]. In this study,
ANOV A was used to evaluate whether project efficiency
and agents’ average experience differed significantly
across the eight simulation scenarios. When significant
effects were detected, Tukey’s HSD post-hoc tests were
performed to determine which pairs of scenarios differed
significantly while controlling for Type I errors in
multiple comparisons.
Spearman’s correlation, in turn, is a non-parametric
measure of association that assesses the monotonic
relationship between two ordinal or continuous variables
without assuming normality. This test was used to
examine the relationship between staff turnover rate
and average accumulated experience, allowing the
identification of general trends even in the presence of
non-linear distributions. The combined use of ANOV A,
post-hoc testing, and Spearman correlation enabled
robust validation of the model’s emergent patterns,
reinforced the statistical significance of the findings, and
ensured internal consistency of the simulated system
under conditions of high uncertainty and structural
complexity [94].
Taken together, these four methodological stages pro-
vided a structured and rigorous foundation for the
development, implementation, experimentation, and
validation of the simulation model. The following
section presents the functional structure of the cognitive
project management model developed in NetLogo.
IV. PROJECT MANAGEMENT MODEL IN NETLOGO
The simulation was designed according to the methodology
proposed by the Project Management Institute (PMI), which
defines a matrix project structure where team members
perform specialized roles and report to both a functional
manager and a project manager [3]. The model developed
evaluates the influence of collaboration, individual expertise,
and uncertainty on project efficiency, structured according
to the five core phases of the PMI: initiation, planning,
execution, monitoring and control, and closure. This structure
enables a comprehensive assessment of dynamic interactions
between agents, resource allocation, and evolving perfor-
mance across the project lifecycle.
In the initiation phase, work packages are defined, roles
are assigned, and the dual reporting structure is established.
During execution, managers assign tasks, and functional
managers allocate resources to minimize the mismatch
between workers’ expertise and the complexity of tasks.
Workers execute their tasks and may choose to assist
colleagues, introducing an effort allocation dilemma between
individual productivity and collaborative support. To capture
this, the model incorporates a mechanism where workers
distribute their total effort between task production and
collaboration, regulated by their level of expertise. This
trade-off is further shaped by a sigmoid function that
models the likelihood of collaboration based on the worker’s
expertise relative to a defined threshold.
To enhance realism, the model incorporates a learning
curve that enables workers to gradually improve their exper-
tise, thereby increasing task efficiency and reducing their
dependence on collaboration over time. This evolutionary
behavior reflects real-world processes of skill acquisition
and adaptive performance. Performance indicators—such as
actual versus estimated task durations and cost deviations—
are tracked in the monitoring and control phase. In contrast,
the closure phase consolidates outcomes to evaluate the
effects of uncertainty on project success. These results inform
strategies to optimize planning and resource management in
future project scenarios.
Besides, the developed model simulates a collaborative
environment involving heterogeneous agents comprising five
agent types: project managers, functional managers, workers,
work packages, and deliverables. Each agent is defined by
a specific set of attributes that govern its behavior and
VOLUME 13, 2025 127267

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
interactions within the system. Workers are assumed to
possess expertise, a performance improvement rate, and
an accumulated utility, which serve as key indicators of
their progression. Similarly, deliverables are characterized by
inherent difficulty, risk, and a probability of impact, all of
which determine their priority and execution complexity.
This agent-based structure provides the foundation for
modeling complex interactions in dynamic project envi-
ronments. Building on these specifications, the simulation
incorporates a set of core assumptions that capture the
cognitive and organizational behaviors underpinning project
execution under uncertainty. See Fig. 3.
This agent-based structure provides the foundation for
modeling complex interactions in dynamic project envi-
ronments. Building on these specifications, the simulation
incorporates a set of core assumptions that capture the
cognitive and organizational behaviors underpinning project
execution under uncertainty.
A. MODEL ASSUMPTIONS
The cognitive agent-based simulation model incorporates
a series of key assumptions to represent the dynamics
of project management under high uncertainty effectively.
In this environment, workers are heterogeneous agents with
varying levels of expertise (ρ ), influencing their ability to
perform tasks and support other team members. Deliverable
assignments are based on specialization, ensuring more
experienced agents are assigned to more complex tasks.
Furthermore, the possibility of collaboration is constrained
by a help radius (δ ), which models interaction limits and
resource availability.
Project efficiency (η ) is calculated as the ratio between
estimated time (T E ) and actual execution time (T X ), allowing
for the assessment of planning accuracy. A critical factor in
the system is staff turnover (R), which may occur due to work
fatigue, shifting project demands, or declining motivation,
leading to additional recruitment costs and interruptions in
task continuity. Each worker’s total effort is divided between
production (α ) and assistance (β ), generating an individual
cost (C i) that varies depending on the level of collaboration
and the trade-off between both activities.
The model also integrates a learning curve through
which agents improve their performance over time based on
accumulated experience and peer interaction. This learning
process directly influences efficiency, reliance on support,
and team stability. As indicated in previous research [25],
cooperation among agents cannot be fully explained through
a purely utilitarian lens; cognitive and social dimensions also
shape individuals’ willingness to collaborate. Factors such as
motivation, job commitment, and organizational productivity
are positively influenced by collaborative behaviors [95],
[96]. In the model, this is reflected in an increase in the
worker’s accumulated utility (γ ), where the benefits of
helping others are not only reflected in reduced execution
times but also in greater organizational stability and lower
turnover.
Building on the work of [97], [98], and [99], the model
introduces a help preference coefficient (φ ) into the utility
function, capturing the agent’s predisposition to cooperate
with team members. Additionally, expertise is categorized
into four levels: basic (ρ ∈ [1, 3]), intermediate (ρ ∈
[4, 6]), advanced (ρ ∈ [7, 9]), and expert (ρ = 10).
This classification directly impacts execution time (T X ),
the probability of requesting help (P c), and task allocation
efficiency, reinforcing expertise as a critical variable within
the model’s dynamics.
While incorporating expertise enables the representation
of significant behavioral differences among agents, its
effectiveness is subject to operational constraints. These
limitations affect the extent of collaboration and the nature
of agent interactions, potentially influencing the system’s
overall outcomes. The following section outlines the main
constraints considered in the model’s design.
B. CONSTRAINS
This study falls within an empirical approach based on
computational simulation through the implementation of a
multi-agent model in NetLogo. Although the model enables
observing emergent patterns and evaluating scenarios under
uncertain conditions, no real-world project data were used.
Therefore, the results should be interpreted as exploratory and
conceptually validating the proposed approach rather than as
direct evidence applicable to specific contexts. This limitation
is acknowledged as an opportunity for future research that
incorporates field data to contrast the findings obtained
through empirical simulation.
The model variables are presented in Table 1.
In the model, constraints regarding the availability and
allocation of human and material resources directly affect
task execution. Each worker ( wi) assigned to a deliver-
able (ε ) is subject to their level of expertise (ρ ), which
must exceed a minimum threshold to access tasks of
higher complexity. Moreover, a worker can collaborate
with others only if their occupancy status is compat-
ible and they have not exceeded the workload limit,
expressed in terms of cumulative execution time (T X ).
These constraints operate under a conditional collaboration
policy, regulated by the probability of receiving practical
help, which is determined based on previous collaboration
memory.
The allocation of resources from managers to workers
is mediated by the variable (8), representing the efficient
distribution rate. This rate must ensure that the resources
distributed do not exceed the system’s total availability
while also meeting the minimum required for performance
improvement (1) in each worker. Additionally, each man-
ager has a corresponding level of expertise (ρ ), directly
influencing the resource allocation quality. The decision to
distribute resources is subject to an active demand condition,
with priority given to workers with lower accumulated
127268 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
FIGURE 3. Proposed simulation model. Source: The Authors.
performance, following an optimization policy based on total
utility.
Finally, the system imposes a global time constraint (T max),
which limits the overall project duration. This constraint
affects the sequential planning of deliverables, which must
be completed within the estimated time frame ( TE ), adjusted
by a tolerance margin defined by the risk factor (κ ).
Deliverables with higher risk and difficulty are prioritized
if their impact on the project objective exceeds a critical
threshold. Furthermore, overall efficiency is influenced by
worker motivation and fatigue, which evolve dynamically
during the process and directly affect the completion rate of
deliverables the project objective exceeds a critical threshold.
Furthermore, overall efficiency is influenced by worker
motivation and fatigue, which evolve dynamically during the
process and directly affect the completion rate of deliverables.
Below are the characteristics of the model.
C. MODEL AGENTS
In the cognitive agent-based project management model,
agents are defined as allocators and workers, each with
variables and rules governing their behavior. Their interaction
in the simulation is determined by equations that regulate
task assignment, deliverable execution, collaboration, and
associated costs.
• Functional Managers (Allocators)
Allocators (A ) distribute tasks to workers based on their
availability and level of expertise. The assignment function
is (1):
Ei : A(W , T , P) (1)
Let W = {w1, w2, . . . ,wN } represent the set of available
workers, and T = {t1, t2, . . . ,tM } the set of pending deliv-
erables. Each deliverable Ei is assigned to a specific worker
wi within the system. Additionally, deliverables are grouped
into work packages P = {p1, p2, . . . ,pk }, which may
be categorized as strategic, administrative, or operational,
depending on their nature and relevance within the project
structure.
The allocator seeks to minimize the difference between the
worker’s expertise level (ρ) and the deliverable difficulty (ψ ),
VOLUME 13, 2025 127269

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
TABLE 1. Model variables.
by (2):
A(wi) : arg min
tj∈T
⏐⏐ρi − ψj
⏐
⏐ (2)
This ensures that deliverables are assigned to the most
appropriate workers so they can be executed efficiently.
• Workers
Each worker (w i) executes deliverables according to their
expertise level (ρ ), their workload (λ), and the collaboration
received (β ). The execution time for an assigned deliverable
is as follows by (3):
TW = TE
(1 + ρ) ·

1 −
∑
j∈H
βj

 (3)
where TW represents the actual time executed by the worker,
and TE denotes the estimated time calculated using the PERT
model. The variable ρ refers to the worker’s level of expertise,
which influences task performance. H denotes the subset of
workers who aid during task execution, while βj represents
the collaborative effort contributed by other team members
to support the worker.
These variables interact within the system to shape
performance dynamics and enable adaptive decision-making.
One of the core features influenced by these parameters is
detailed below.
D. MODEL FEATURES
The characteristics of the model are described below:
• Collaboration
Spatial and behavioral conditions govern collaboration in the
model. It occurs within a radius of help (δ ) which defines
the maximum allowable distance between a worker i and
potential collaborators j, such that the condition d(i, j) ≤ δ
is met. The probability of collaboration (P c) depends on
the worker’s level of expertise relative to the highest in the
system, calculated as Pc = ρi/ρmax. For instance, a highly
experienced worker within the collaboration radius of a
less experienced peer is more likely to provide assistance.
However, this helping behavior is constrained by the worker’s
workload ( λ). The amount of collaborative effort a worker
can offer is given by β = max(0, 1 − λ), meaning that if
λ = 1, the worker is fully occupied and unable to assist
others.
The variable β represents the proportion of a worker’s
total effort allocated to assisting others rather than focusing
solely on their tasks. It is calculated as β = b/E,
where b is the effort dedicated to collaboration and E is
the total effort, which includes both individual production
(α) and collaborative effort (β ). Accordingly, βi reflects
the collaboration level of worker i. When β = 0, the
worker exclusively focuses on individual tasks. If β >
0.5, the worker dedicates most of their effort to helping
others, potentially reducing productivity. Conversely, if β <
0.5, the worker collaborates occasionally while prioritizing
personal task execution. This balance between production
and assistance is critical in understanding team dynamics
and resource allocation efficiency in the simulated project
environment.
Collaboration in the model is governed by the level of
expertise, proximity between agents, and workload, allowing
for the simulation of realistic teamwork dynamics. The
more experienced the workers, the less likely they are
to ask for help and the greater their capacity to provide
support. Collaboration can accelerate task execution but
also affects costs by redistributing efforts between produc-
tion and assistance. Through these rules and equations,
the model allows for evaluating teamwork strategies to
improve efficiency and optimize project management under
uncertainty.
127270 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
• Distribution of effort between production and collab-
oration
The distribution of effort between production and collabo-
ration is governed by the condition that each worker allocates
their total available effort between task production (α ) and
collaboration (β ), such that α + β = 1. When a worker does
not engage in collaboration, they dedicate their entire effort
to production (α = 1, β= 0); however, if collaboration is
chosen, a portion of the effort is redirected toward assisting
others.
The allocation to collaboration is modeled using a sigmoid
function by (4):
β = 1
1 + e−κ(ρ−ρlim) (4)
where κ is a coefficient that regulates the intensity of collabo-
ration, ρ represents the expertise of the worker offering help,
and ρlim is the minimum expertise required to be effective
in supporting others. This formulation implies that workers
with expertise above the threshold ρlim are increasingly likely
to collaborate, while those with insufficient expertise tend to
focus solely on their individual tasks.
• Project Timelines and Time Efficiency under Uncer-
tainty
The simulation model operates in discrete execution cycles
(ticks), during which key temporal metrics—estimated time
(TE ), executed time (TX ), and time efficiency—are monitored
to evaluate performance and guide decision-making. All tasks
are assumed to be critical, and the estimated time (T E )
is calculated using the PERT technique, which integrates
optimistic (T O), most likely (T M ), and pessimistic (T P) time
estimates into a weighted average. Refer to (5):
TE = TO + 4TM + TP
6 (5)
This formula yields a realistic projection of task duration
and supports robust planning under uncertainty where all
activities are considered critical. In contrast, the executed
time (T X ) reflects the actual time a worker requires to
complete a task, influenced by individual and contextual
factors. It is computed as the sum of task durations completed
by N workers. Refer to (6):
TX =
N∑
i=1
TXi (6)
Factors such as collaboration (β ), experience (ρ ), and
workload modulate execution time. For example, collabora-
tion may accelerate completion, while insufficient expertise
or task overload may cause delays. However, excessive
collaboration requests within a limited communication radius
(δ) may lead to bottlenecks and inefficiencies.
Additionally, disruptions such as worker turnover (R),
resource limitations, and environmental variability () are
modeled through a penalty factor (τ ), which adjusts executed
time. Refer to (7):
ˆTX = TX + τ (7)
This adjustment accounts for unexpected events that affect
project performance, including staff replacement costs (C R)
and delays in deliverables due to team instability or resource
scarcity.
Together, these formulations provide a dynamic framework
to assess time efficiency and identify deviations in project
execution. By contrasting planned and actual durations, the
model reveals how real-world complexities—such as coor-
dination, expertise distribution, and external shocks—impact
project timelines. This framework captures the complex
dynamics of real-world project management, illustrating
how collaboration, expertise, and disruptions shape task
performance in uncertain settings.
• Expertise in the Model
The model incorporates worker expertise (ρ ) as a crit-
ical factor influencing task execution efficiency. Exper-
tise reduces actual execution time (T X ) relative to the
PERT-estimated time (TE ) through the relation. Refer to (8):
TX = TE
1 + ρ (8)
where higher ρ values asymptotically minimize TX . Low
expertise, however, risks delays by exceeding TE .
Expertise evolves dynamically via a learning curve. Refer
to (9):
ρt+1 = ρt + 1ρ (9)
with 1ρ representing knowledge gains from task completion
and collaboration.
Efficiency (η) is quantified as (10):
η = TE
TX
· 100 (10)
where η > 100% indicates faster-than-expected execution,
η = 100% denotes perfect alignment, and η <100% reflects
inefficiency. This framework captures how adaptive expertise
optimizes time management in agile project environments.
• Cost Structure and Efficiency Assessment
The model integrates four primary cost components:
estimated cost (C E ), representing the initial budget allocation
per deliverable; executed cost (CX ), reflecting actual expendi-
tures; collaboration cost (C C ), associated with time and effort
invested in assisting peers; and turnover cost (C R), linked
to personnel replacement. To evaluate resource efficiency,
the ratio between CE and CX is analyzed to detect budget
deviations and improve allocation strategies. The individual
cost of a worker (C i) incorporates production effort (α i),
collaboration effort (β i), and a conflict coefficient (θ ) that
captures the trade-off between these two activities. Refer
to (11):
Ci = (α2
i + β2
i ) + θ · αiβi (11)
This formulation acknowledges that collaboration, while
essential, can reduce individual productivity due to compet-
ing demands on time and energy.
VOLUME 13, 2025 127271

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
The estimated cost of the project aggregates the costs of all
completed deliverables. Refer to (12):
CE =
N∑
i=1
CEi (12)
where CEi denotes the cost of deliverable i, including labor,
materials, and related resources.
Turnover cost is defined as (13):
CR = R · Crec (13)
with R representing the number of workers who left the
project and Crec the average recruitment and onboarding cost.
Collaboration costs are calculated by summing the individ-
ual costs of all project workers. Refer to (14):
CC =
M∑
i=1
Ci (14)
Finally, the total project cost (C T ) is expressed as (15):
CT =
N∑
i=1
CEi + R · Crec +
M∑
i=1
(
α2
i + β2
i + θ · αiβi
)
(15)
This structure enables analysis of key cost drivers. For
instance, low turnover (R ≈ 0) minimizes recruitment
expenses, while excessive collaboration (high β) may com-
promise efficiency. Conversely, a high number of deliverables
(large N) increases executed cost, signaling project advance-
ment.
• Utility, Efficiency, and Uncertainty in Cognitive
Agent-Based Project Management
In the cognitive agent-based model, worker utility inte-
grates production effort (α ), the benefits of collaboration (β ),
and external environmental influences (). Utility functions
as a key metric to evaluate how individual performance
and team interactions contribute to overall project efficiency,
guiding decisions on resource distribution and productivity
enhancement.
The utility of each worker is defined as (16):
Ui = ρ · αi + (1 − ρ) · ϕ · αi +  (16)
where ρ represents the weight of productive effort, ϕ captures
the positive effect of collaboration, and  accounts for
environmental conditions.
Project efficiency is quantified as the ratio of estimated to
actual completion time. Refer to (17):
ε = τ
T · 100 (17)
with τ as the estimated project duration and T the actual
time executed. To assess project uncertainty, the model
considers variability in both time and cost using standard
deviation metrics. Refer to (18) y (19):
σt =
√∑(Ti − τi)2
N (18)
σc =
√∑(λi − κi)2
N (19)
where σt and σc denote time and cost variability respectively,
N is the number of tasks, Ti and τi are actual and estimated
times, and λi, κi are actual and estimated costs.
This integrated approach enables a multidimensional
analysis of project performance, incorporating individual
behavior, collaborative dynamics, and uncertainty factors to
support adaptive and efficient project management.
V. RESULTS
To facilitate the understanding and replicability of the
proposed model, a general description of the graphical envi-
ronment implemented in the NetLogo platform, as well as the
modular structure of the code used in the simulation, is pre-
sented below. The dashboard includes a spatial representation
of the agents-workers, managers, and deliverables-together
with monitors and graphs that allow dynamic observation of
the evolution of key variables such as average experience,
project efficiency, and accumulated costs. The code was
also organized into modules that reflect the typical phases
of project management, allowing an orderly execution of
the processes of assignment, collaboration, task execution,
learning, and performance evaluation. This section provides
a detailed overview of the main procedures (setup, go, among
others), their specific functions, and their articulation within
the simulation cycle. See Fig. 4.
Several simulation scenarios were executed in NetLogo to
evaluate the impact of cognitive agent interactions on project
performance. These scenarios varied in the distribution of
expertise, turnover rate, and collaboration intensity. The
results were analyzed through dynamic indicators captured
at multiple time steps (ticks), offering a fine-grained view
of emergent behaviors in the system. This approach allows
us to visualize how workforce composition and interaction
structure changes influence key project metrics such as
execution time, efficiency, and cost.
Fig. 5 shows that scenarios with high collaboration and
expertise lead to higher project efficiency (over 85%).
In contrast, scenarios with high turnover or work overload
(Overloaded) show a notable drop, with efficiencies below
60%. This demonstrates the system’s sensitivity to coopera-
tion and human capital.
Fig. 6 shows a nonlinear relationship between total cost
and efficiency. The ‘‘High Expertise’’ scenario achieves one
of the highest efficiencies without incurring the highest costs.
In contrast, the ‘‘Overloaded Scenario’’ shows increasing
costs with decreasing efficiency, indicating potential struc-
tural inefficiency and load imbalance.
127272 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
FIGURE 4. Proposed Netlogo model. Source: The Authors.
FIGURE 5. Project efficiency by scenario. Source: The Authors.
FIGURE 6. Total cost vs project efficiency. Source: The Authors.
Eight scenarios were developed, as shown in Table 2,
which summarizes how different model configurations affect
the system’s ability to develop collective expertise over time:
The first segment of analysis evaluates the impact of
turnover (R) and collaboration radius (δ ) on the average
experience θ, across multiple scenarios. Comparative data
reveals that increasing turnover from 5% to 25%, with collab-
oration and expertise held constant, results in a reduction of
average experience from 2.58 to 2.54. This reflects a negative
TABLE 2. Scenario outcomes at 1,000 Ticks.
marginal rate of change with respect to turnover. Similarly,
the effect of increasing collaboration radius is examined
by comparing configurations with identical turnover and
expertise. An increase from σ = 1 to σ = 5 leads to a drop in
experience from 2.58 to 2.55, indicating diminishing returns
to widespread collaboration.
The learning curve over 100 ticks is presented below.
The analysis was conducted over a 100-tick horizon, based
on empirical observations of the model’s behavior, which
revealed that most of the emergent learning dynamics and
differentiation between scenarios occur during the initial
simulation cycles. After tick 100, the average experience
curves tend to stabilize, showing diminishing marginal
growth and minor fluctuations. Therefore, extending the
analysis to 1,000 or 10,000 ticks does not produce relevant
qualitative changes or new emergent patterns, which validates
the use of a shorter yet representative interval. This ensures
computational efficiency without compromising analytical
depth.
The results obtained during the first 100 ticks demonstrate
that the average agent experience, denoted as θ(t), evolves
according to a pseudo-linear learning function perturbed
by stochastic noise. This behavior can be approximated
mathematically as (20):
θ(t) = θ0 + α · t + ε(t) (20)
where θ0 is the initial level of expertise, α is the effective
learning rate, and ε(t) ∼ N(0, σ2) is a stochastic perturbation
term. This formulation captures the fundamental dynamics
of decentralized, time-evolving knowledge propagation in the
agent population. Emergent project efficiency η was modeled
as a nonlinear function of the final average experience. The
function follows an exponential form. Refer to (21):
η = 100 ·
(
1 − e−0.2θ
)
(21)
VOLUME 13, 2025 127273

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
This expression reflects that efficiency increases rapidly
with early gains in experience, but reaches diminishing
returns as θ approaches its upper bound. Scenarios with stable
growth in θ showed significantly higher emergent efficiency
compared to noisy, fluctuating ones.
The numerical gradient of experience curves, ∂θ
∂t , was used
to assess the stability of learning. In scenarios with low
rotation and high initial expertise, this gradient remained
positive and smooth, indicating effective self-organization.
See Fig. 7.
FIGURE 7. Learning curves over 100 ticks. Source The Authors.
The average final experience decreases as turnover
increases, even though the collaboration ratio also increases.
Extensive collaboration does not offset the negative impact
of high turnover. The temporal dynamics of experience,
turnover, and collaboration reveal the critical interdepen-
dencies that shape project outcomes. Scenarios with highly
skilled agents exhibit stability and sustained performance,
while overloaded systems demonstrate vulnerability through
excessive turnover and unstable collaboration patterns. These
findings set the stage for a deeper discussion on strategic
workforce management and adaptive coordination mecha-
nisms in complex projects.
VI. DISCUSSION
The analysis of the initial 100 ticks revealed that organiza-
tional learning progresses rapidly during the early simulation
cycles, followed by a natural deceleration due to experiential
saturation. The evolution of average expertise ¯ρ(t) displayed
a pseudo-linear growth pattern with stochastic fluctuations,
indicating that agents actively learn within an adaptive
environment. This early stabilization, observed across most
scenarios, suggests that the majority of relevant knowledge
is consolidated before tick 60, highlighting the importance of
prioritizing intervention policies during the initial stages of
the project.
The model also revealed that systems with high initial
collaboration were able to partially offset low expertise
levels, but only under conditions of low turnover. In con-
trast, scenarios characterized by high turnover and wide
collaboration ratio showed a progressive decline in collective
learning, as evidenced by negative gradients in ∇ ¯ρ(t) and
increased dispersion in outcomes. This dynamic suggests the
emergence of inefficient collaboration saturation, where the
burden of mutual assistance impedes sustained individual
development. Consequently, emergent behavior in these
contexts does not enhance project efficiency but instead leads
to fluctuations and stagnation.
The temporal analysis of the learning gradient enabled
the classification of scenarios into three distinct types: (1)
convergent, where expertise increases and stabilizes; (2)
volatile, with significant experience oscillations due to high
turnover; and (3) saturated, where excessive collaboration
hampers progress. These emergent patterns not only describe
system behavior but also help anticipate critical project
states where intervention is most effective. This dynamic
approach contrasts with deterministic models that assume
homogeneous and linear conditions, reinforcing the value of
agent-based modeling in complex management scenarios.
Future research could explore adaptive decision-making
under temporal pressure by introducing behavioral change
mechanisms based on accumulated experience or agent stress
levels. Moreover, investigating scenarios involving disruptive
events or external shocks, such as sudden expert loss or
abrupt task redistribution, would allow for an assessment of
system resilience. From a technical standpoint, embedding
reinforcement learning or lightweight neural networks within
agents could capture non-linear, individualized improvement
trajectories. Finally, empirical validation of these findings in
real or hybrid environments (i.e., digital models integrated
with real-world indicators) could transform this approach into
a practical tool for real-time decision-making.
The following section introduces key references and
contrasts their technical and conceptual elements with those
of the present study.
A. COMPARISON WITH PREVIOUS WORK
A structured comparison with prior agent-based models
contextualizes the proposed contributions and assesses their
relevance within the broader field. This comparative analysis
allows us to identify methodological advances, highlight
limitations in existing frameworks, and position our model in
terms of its capacity to simulate complex, adaptive behaviors
in project environments.
Tables 3 and 4 compare the proposed agent-based model
and three prominent approaches previously published in
indexed journals. The analysis highlights key modeling
aspects such as the simulation platform, agent typologies, the
breadth of variables considered, and the degree of cognitive
and emergent complexity embedded in each model.
In the comparison of the article it is observed for
example that developed an agent-based model in NetLogo
focusing on the diffusion of helping behavior within project
teams [25]. Their model innovatively incorporates task
interdependence, effort conflict, and incentive systems to
explore the emergence and propagation of prosocial actions.
However, it does not include learning dynamics or staff
127274 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
TABLE 3. Comparison with previous work.
TABLE 4. Comparison with previous work.
turnover, and the evaluation of project efficiency is limited
to behavioral diffusion and synergy effects. Furthermore,
decision-making is based on an imitation rule, where agents
replicate the neighbor’s strategy with the highest utility,
reflecting bounded rationality but lacking deeper cognitive
processes.
In addition, [12] designed a Java-based simulation aligned
with the Earned Value Management (EVM) methodology,
providing a visualization of project performance in terms
of time and cost deviations. While their model accurately
reflects traditional project control frameworks, it lacks
individual adaptability, collaboration dynamics, and emer-
gent behavior. Agents behave deterministically based on
predefined roles without mechanisms for learning or social
interaction.
In contrast, [100] introduced a cognitively grounded model
that integrates various bases of social power (reward, coer-
cion, legitimacy, expertise, and referent), drawing from social
psychology. Although not specifically tailored to project
management, their model enables rich social reasoning and
strategic influence among agents. The framework supports
dynamic role adaptation and hierarchical relationships in
multi-agent environments. Nevertheless, it does not simulate
task execution, economic costs, or project-specific indicators,
limiting its applicability in operational contexts.
The model proposed in this study stands out by inte-
grating both structural and cognitive elements. It simulates
realistic project dynamics with agents that allocate tasks
based on expertise, exhibit learning curves, collaborate
depending on proximity and shared effort, and adapt through
experience. The model also includes turnover and utility-
driven decision-making, enabling patterns that reflect the
complexity of real-world project execution. Performance is
evaluated using multidimensional indicators—time, cost, and
emergent utility—offering a comprehensive assessment of
project outcomes under uncertainty.
This integrative approach bridges the gap between
behaviorally rich social simulations and operational project
management models. It represents a novel contribution
by combining cognitive modeling, dynamic organizational
structures, and performance evaluation, thus advancing the
state of the art in agent-based simulations for complex
projects.
VII. CONCLUSION
This study demonstrated that the use of a cognitive
agent-based model enables an accurate representation of the
complexity inherent in project management within uncertain
environments. The model captured how individual decisions
and local interactions give rise to emergent system-level
behaviors by incorporating variables such as expertise,
collaboration, turnover, and efficiency. The evolution of
average worker expertise closely followed a perturbed linear
function, E(T ) = E0 + αt + εt , with an effective learning
rate of α ≈ 0.0064 and low standard deviation, reflecting
organizational stability under low-turnover conditions.
From a systemic perspective, an exponential relationship
was identified between final average expertise and overall
efficiency coefficient β = 0.45. This relationship yielded a
statistically significant fit R2 = 0.936, indicating that collec-
tive learning drives substantial performance improvements,
although with diminishing returns as expertise increases.
VOLUME 13, 2025 127275

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
Additionally, ANOV A analysis confirmed significant dif-
ferences across simulated scenarios (F = 12.87; p <
0.01), and the Spearman correlation coefficient between
turnover and expertise (ρ = −0.81) reaffirmed the negative
impact of workforce instability on organizational learn-
ing, demonstrating the model’s robustness across different
conditions.
Regarding collaboration, the model revealed that while it
contributes to reduced execution times, a threshold exists
beyond which the associated costs—stemming from effort
conflict and overload of key agents—generate adverse
effects. The individual utility function captured this dynamic:
Ui = λi(1+ϕ)−ci, where λi denotes production effort, ϕ the
impact of collaboration, and ci the cost of effort conflict. The
simulation showed that unregulated collaboration can induce
organizational bottlenecks, particularly in high-workload or
low-expertise scenarios.
Team stability and strategically distributed collabora-
tion are essential for achieving sustainable efficiency in
complex project management. The simulation evidenced
that collaboration alone cannot offset the disruptive effects
of high turnover. Therefore, implementing talent retention
strategies, continuous training, and adaptive role design is
recommended. When adequately modeled through cognitive
agents, these elements offer a valuable tool for anticipating
impacts and optimizing decision-making in dynamic and
volatile contexts.
ACKNOWLEDGMENT
This document was produced thanks to the joint work of
the International Research Group on Informatics, Communi-
cations, and Knowledge Management (GICOGE), research
group Research, Development and Applications in Signals
(IDEAS) of the Universidad Distrital Francisco José de
Caldas and the LUMON LV TECH research group
REFERENCES
[1] A. Munns and B. Bjeirmi, ‘‘The role of project management in achieving
project success,’’ Int. J. Project Manage., vol. 14, no. 2, pp. 81–87,
Apr. 1996, doi: 10.1016/0263-7863(95)00057-7.
[2] S. Elonen and K. A. Artto, ‘‘Problems in managing internal development
projects in multi-project environments,’’ Int. J. Project Manage., vol. 21,
no. 6, pp. 395–402, Aug. 2003, doi: 10.1016/s0263-7863(02)00097-2.
[3] L.-A. Vidal, ‘‘Thinking project management in the age of complexity.
Particular implications on project risk management,’’ M.S. thesis, Dept.
Business Administration, Ecole Centrale, Paris, 2009.
[4] S. Kiridena. (2017). Profiling Project Complexity: Insights From
Complexity Science and Project Management Literature . Aust. [Online].
Available: www.pmi.org/PMJ
[5] P. J. Charrel and D. Galarreta, Project Management and Risk Management
in Complex Projects: Studies in Organizational Semiotics . Dordrecht, The
Netherland: Springer, 2007, p. 229, doi: 10.1007/978-1-4020-5837-0.
[6] T. Lechler, B. Edington, and T. Gao, ‘‘Challenging classic project
management: Turning project uncertainities,’’ Project Manag. J., vol. 43,
no. 6, pp. 59–69, 2012, doi: 10.1002/pmj.21304.
[7] S. Morcov, L. Pintelon, and R. Kusters, ‘‘Definitions, characteristics and
measures of it project complexity—A systematic literature review,’’ in
Proc. SciKA, 2020, pp. 5–21, doi: 10.12821/ijispm080201.
[8] R. Adcock, ‘‘Project management for a complex adaptive operating
system from SEBoK project management for a complex adaptive
operating system,’’ Syst. Eng. Body Knowledge (SEBoK), Stevens Inst.
Technol. Syst. Eng. Res. Center, Int. Council Syst. Eng. (INCOSE), IEEE
Systems Council, Tech. Rep., 2005.
[9] R. Kozik, M. Choras, D. Puchalski, and R. Renk, ‘‘Data analysis tool
supporting software development process,’’ in Proc. IEEE 14th Int. Sci.
Conf. Informat., Nov. 2017, pp. 179–184.
[10] W. Aslam and F. Ijaz, ‘‘A quantitative framework for task allocation
in distributed agile software development,’’ IEEE Access, vol. 6,
pp. 15380–15390, 2018, doi: 10.1109/ACCESS.2018.2803685.
[11] W. M. Purawinata, F. L. Gaol, A. Nugroho, and B. S. Abbas, ‘‘The
prediction of software complexity based on complexity requirement using
artificial neural network,’’ in Proc. IEEE Int. Conf. Cybern. Comput.
Intell., Nov. 2017, pp. 73–78.
[12] M. Castañón-Puga, R. F. Rosales-Cisneros, J. C. Acosta-Prado, A. Tirado-
Ramos, C. Khatchikian, and E. Aburto-Camacllanqui, ‘‘Earned value
management agent-based simulation model,’’ Systems, vol. 11, no. 2,
p. 86, Feb. 2023, doi: 10.3390/systems11020086.
[13] W. Lipke, O. Zwikael, K. Henderson, and F. Anbari, ‘‘Prediction of
project outcome,’’ Int. J. Project Manage., vol. 27, no. 4, pp. 400–407,
May 2009, doi: 10.1016/j.ijproman.2008.02.009.
[14] H. Gaspars-Wieloch, ‘‘Project net present value estimation under
uncertainty,’’ Central Eur. J. Oper. Res., vol. 27, no. 1, pp. 179–197,
Mar. 2019, doi: 10.1007/s10100-017-0500-0.
[15] E. Kim, W. G. Wells, and M. R. Duffey, ‘‘A model for effective imple-
mentation of earned value management methodology,’’ Int. J. Project
Manage., vol. 21, no. 5, pp. 375–382, Jul. 2003, doi: 10.1016/s0263-
7863(02)00049-2.
[16] H. K. Kim, J. K. Kim, and Q. Y . Chen, ‘‘A product network analysis for
extending the market basket analysis,’’ Expert Syst. Appl., vol. 39, no. 8,
pp. 7403–7410, Jun. 2012, doi: 10.1016/j.eswa.2012.01.066.
[17] S. R. Mohandes and X. Zhang, ‘‘Towards the development of a
comprehensive hybrid fuzzy-based occupational risk assessment model
for construction workers,’’ Saf. Sci., vol. 115, pp. 294–309, Jun. 2019,
doi: 10.1016/j.ssci.2019.02.018.
[18] P. X. W. Zou and G. Zhang, ‘‘Managing risks in construction projects: Life
cycle and stakeholder perspectives,’’ Int. J. Construct. Manage., vol. 9,
no. 1, pp. 61–77, Jan. 2009, doi: 10.1080/15623599.2009.10773122.
[19] M. Thneibat, M. Thneibat, B. Al-Shattarat, and H. Al-Kroom, ‘‘Devel-
opment of an agent-based model to understand the diffusion of
value management in construction projects as a sustainability tool,’’
Alexandria Eng. J., vol. 61, no. 1, pp. 747–761, Jan. 2022, doi:
10.1016/j.aej.2021.05.005.
[20] A. F. Kineber, M. S. Uddin, and A. F. Momena, ‘‘Exploring the critical
success factors of value management implementation for sustainable res-
idential building project: A stationary analysis approach,’’ Sustainability,
vol. 14, no. 23, p. 16215, Dec. 2022, doi: 10.3390/su142316215.
[21] J. R. S. Cristóbal, ‘‘Complexity in project management,’’ Proc. Comput.
Sci., vol. 121, pp. 762–766, Jan. 2017, doi: 10.1016/j.procs.2017.11.098.
[22] R. Joslin and R. Müller, ‘‘Relationships between a project management
methodology and project success in different project governance con-
texts,’’Int. J. Project Manage., vol. 33, no. 6, pp. 1377–1392, Aug. 2015,
doi: 10.1016/j.ijproman.2015.03.005.
[23] K. Remington and R. Zolin, ‘‘A model of project complexity: Distinguish-
ing dimensions of complexity from severity,’’ in Proc. 9th Int. Res. Netw.
Project Manage., 2009, pp. 1–30.
[24] C. A. Stevens, J. Daamen, E. Gaudrain, T. Renkema, J. D. Top,
F. Cnossen, and N. A. Taatgen, ‘‘Using cognitive agents to train
negotiation skills,’’ Frontiers Psychol., vol. 9, p. 154, Feb. 2018, doi:
10.3389/fpsyg.2018.00154.
[25] N. Zhao, H.-Y . Chong, and Q. Li, ‘‘Agent-based modelling of
helping behaviour diffusion in project teams as an evolutionary
process,’’ J. Simul., vol. 17, no. 3, pp. 279–296, May 2023, doi:
10.1080/17477778.2021.1997342.
[26] S. A. Delre, W. Jager, T. H. A. Bijmolt, and M. A. Janssen, ‘‘Targeting
and timing promotional activities: An agent-based model for the takeoff
of new products,’’ J. Bus. Res., vol. 60, no. 8, pp. 826–835, Aug. 2007,
doi: 10.1016/j.jbusres.2007.02.002.
[27] A. Banos, C. Lang, and N. Marilleau, Agent-Based Spatial Simulation
With NetLogo, vol. 1. Amsterdam, The Netherlands: Elsevier, 2015.
[28] U. Wilensky and W. Rand, An Introduction to Agent-Based Modeling
Natural, Social, and Engineered Complex Systems With NetLogo . Hong
Kong: Massachussetts Institute of Thechnology, 2016.
[29] E. Morin and S. Kelly, ‘‘From the concept of system to the paradigm
of Complexity1 introduction: Mastering the concept of system,’’ J.
Social Evol. Syst., vol 15, no. 3 pp. 371–385, 1992, doi: 10.1016/1061-
7361(92)90024-8.
127276 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
[30] R. Frei and G. D. M. Serugendo, ‘‘Concepts in complexity engineering,’’
Int. J. Bio-Inspired Comput., vol. 3, no. 2, p. 123, 2011.
[31] S. Morcov, K. U. Leuven, L. Pintelon, and R. J. Kusters. (2020).
IT Project Complexity Management Based on Sources and
Effects: Positive, Appropriate and Negative. [Online]. Available:
https://www.researchgate.net/publication/342314173
[32] A. Duit and V . Galaz, ‘‘Governance and complexity—Emerging issues for
governance theory,’’ Governance, vol. 21, no. 3, pp. 311–335, Jul. 2008,
doi: 10.1111/j.1468-0491.2008.00402.x.
[33] L. G. M. Moreno and L. M. Pantoja, ‘‘Analytics applied to the study of
reputational risk through the analysis of social networks (Twitter) for the
El Dorado airport in the city of Bogotá (Colombia),’’ in Proc. 21st Int.
Conf. Enterprise Inf. Syst., vol. 1, 2019, pp. 476–483.
[34] C. Gershenson, ‘‘Requisite variety, autopoiesis, and self-organization,’’
Kybernetes, vol. 44, nos. 6–7, pp. 866–873, Jun. 2015, doi: 10.1108/k-
01-2015-0001.
[35] A. J. Morales, C. Gershenson, D. Braha, A. A. Minai, and Y . Bar-Yam,
‘‘Unifying themes in complex systems IX,’’ in Proc. 9th Int. Conf.
Complex Syst. (Springer Proceedings in Complexity). Cham, Switzerland:
Springer, 2018, doi: 10.1007/978-3-319-96661-8.
[36] R. López-Ruiz, ‘‘Complexity in some physical systems,’’ Int. J.
Bifurcation Chaos, vol. 11, no. 10, pp. 2669–2673, Oct. 2001. [Online].
Available: www.worldscientific.com
[37] C. M. Schlick, S. Duckwitz, and S. Schneider, ‘‘Project dynamics and
emergent complexity,’’ Comput. Math. Org. Theory, vol. 19, no. 4,
pp. 480–515, Dec. 2013.
[38] J. H. Holland, ‘‘Complex adaptive systems and spontaneous emergence,’’
in Proc. Complexity and Industrial Clusters Conf. Physica-Verlag HD,
2002, doi: 10.1007/978-3-642-50007-7_3.
[39] O. Goldreich, Computational Complexity: A Conceptual Perspective
(Weizmann Institute of Science). Cambridge, U.K.: Cambridge Univ.
Press, 2008, pp. 606–612.
[40] A. Boonstra and C. Reezigt, ‘‘A complexity framework for project
management strategies,’’ Project Manage. J., vol. 54, no. 3, pp. 253–267,
Jun. 2023, doi: 10.1177/87569728221142229.
[41] M. Danilovic and B. Sandkull, ‘‘Managing complexity and uncertainty
in a multiproject environment,’’ in Proc. IRNOP V , Int. Res. Netw.
Organizing Projects, 2002, pp. 28–31.
[42] J. Oehmen, C. Thuesen, P. Parraguez, and J. Geraldi, ‘‘General rights
complexity management for projects, programmes, and portfolios:
An engineering systems perspective,’’ Project management Institute.,
Newtown Square, PA, USA, Tech. Rep., 2015.
[43] M. Sirshar, S. Ibrahim, and A. Ali. (2019). Analysis of Software Project
Complexity Factors of Large Scale Systems and Their Impacts on Core
Knowledge Areas of Software Project Management. [Online]. Available:
www.preprints.org
[44] F. Marle and L.-A. Vidal, Managing Complex, High Risk Projects.
London, U.K.: Springer, 2016, doi: 10.1007/978-1-4471-6787-7.
[45] J. Geraldi, H. Maylor, and T. Williams, ‘‘Now, let’s make it really complex
(complicated): A systematic review of the complexities of projects,’’ Int.
J. Oper. Prod. Manage., vol. 31, no. 9, pp. 966–990, Aug. 2011, doi:
10.1108/01443571111165848.
[46] T. S. Pitsis, S. Sankaran, S. Gudergan, and S. R. Clegg, ‘‘Governing
projects under complexity: Theory and practice in project management,’’
Int. J. Project Manage., vol. 32, no. 8, pp. 1285–1290, Nov. 2014, doi:
10.1016/j.ijproman.2014.09.001.
[47] M. Moradi, M. Mazoochi, and M. Ahmadi, ‘‘A comprehensive method for
improving the quality of open government data and increasing Citizens’
willingness to use data by analyzing the complex system of citizens and
organizations,’’Complexity, vol. 2022, no. 1, pp. 1–14, Jan. 2022.
[48] Y . H. Kwak and C. W. Ibbs, ‘‘Calculating project management’s return
on investment,’’ Project Manage. J., vol. 31, no. 2, pp. 38–47, Jun. 2000,
doi: 10.1177/875697280003100205.
[49] S. Arora, Y . Li, Y . Liang, T. Ma, and A. Risteski, ‘‘A latent variable
model approach to PMI-based word embeddings,’’ Trans. Assoc. Comput.
Linguistics, vol. 4, pp. 385–399, Dec. 2016, doi: 10.1162/tacl_a_00106.
[50] J. Varajão and M. M. Cruz-Cunha, ‘‘Using AHP and the IPMA
competence baseline in the project managers selection process,’’ Int. J.
Prod. Res., vol. 51, no. 11, pp. 3342–3354, Jun. 2013.
[51] P. J. LaPlaca, ‘‘Industrial marketing management,’’ Ind.
Marketing Manage., vol. 37, no. 3, pp. 245–246, May 2008, doi:
10.1016/j.indmarman.2008.03.001.
[52] M. Winter, C. Smith, P. Morris, and S. Cicmil, ‘‘Directions for
future research in project management: The main findings of a U.K.
government-funded research network,’’ Int. J. Project Manage., vol. 24,
no. 8, pp. 638–649, Nov. 2006, doi: 10.1016/j.ijproman.2006.08.009.
[53] E. Miller, ‘‘Risk, uncertainty, and divergence of opinion,’’ J. Finance,
vol. 32, no. 4, pp. 1151–1168, 2005.
[54] M. Wood, S. Daniellkovacs, and G. Igorrlinkov. Risk, Systems and Deci-
sions Mental Modeling Approach Risk Management Application Case
Studies. Springer, p. 276, doi: 10.1007/978-1-4939-6616-5. [Online].
Available: http://www.springer.com/series/13439
[55] M. L. Platt and S. A. Huettel, ‘‘Risky business: The neuroeconomics of
decision making under uncertainty,’’ Nature Neurosci., vol. 11, no. 4,
pp. 398–403, Apr. 2008, doi: 10.1038/nn2062.
[56] J. Munnukka and P. Järvi, ‘‘Perceived risks and risk management of social
media in an organizational context,’’ Electron. Markets, vol. 24, no. 3,
pp. 219–229, Sep. 2014, doi: 10.1007/s12525-013-0138-2.
[57] N. B. Firoozye and F. Ariff, Managing Uncertainty, Mitigating Risk:
Tackling the Unknown in Financial Risk Assessment and Decision
Making. Springer, 2016, doi: 10.1057/9781137334541.
[58] A. Ojo, L. Porwol, M. Waqar, A. Stasiewicz, E. Osagie, M. Hogan,
O. Harney, and F. A. Zeleti, ‘‘Realizing the innovation potentials from
open data: Stakeholders’ perspectives on the desired affordances of open
data environment,’’ in IFIP Advances in Information and Communication
Technology. New York, NY , USA: Springer, 2016, pp. 48–59.
[59] M. Pirozzi. (2018). The Stakeholder Management Perspective to
Increase the Success Rate of Complex Projects. [Online]. Available:
www.pmworldlibrary.net
[60] E. Gummesson, ‘‘Qualitative research in management: Addressing
complexity, context and persona,’’ Manage. Decis., vol. 44, no. 2,
pp. 167–179, Feb. 2006, doi: 10.1108/00251740610650175.
[61] S. Cicmil, T. Williams, J. Thomas, and D. Hodgson, ‘‘Rethinking
project management: Researching the actuality of projects,’’ Int.
J. Project Manage., vol. 24, no. 8, pp. 675–686, Nov. 2006, doi:
10.1016/j.ijproman.2006.08.006.
[62] D. M. Wiechmann, C. Reichstein, R.-C. Haerting, J. Bueechl, and
M. Pressl, ‘‘Agile management to secure competitiveness in times of
digital transformation in medium-sized businesses,’’ Proc. Comput. Sci.,
vol. 207, pp. 2353–2363, Jan. 2022.
[63] H. Parsons-Hann and K. Liu, ‘‘Measuring requirements complexity to
increase the probability of project success,’’ in Proc. 7th Int. Conf. Enter-
prise Inf. Syst., 2005, pp. 434–438, doi: 10.5220/0002548104340438.
[64] M. Kapsali, ‘‘Equifinality in project management exploring causal
complexity in projects,’’ Syst. Res. Behav. Sci., vol. 30, no. 1, pp. 2–14,
Jan. 2013, doi: 10.1002/sres.2128.
[65] A. A. Ahmadabadi and G. Heravi, ‘‘Risk assessment framework of
PPP-megaprojects focusing on risk interaction and project success,’’
Transp. Res. A, Policy Pract., vol. 124, pp. 169–188, Jun. 2019, doi:
10.1016/j.tra.2019.03.011.
[66] D. N. Antoniadis, F. T. Edum-Fotwe, and A. Thorpe, ‘‘Rethinking project
organization and management,’’J. Civil Eng. Archit., vol. 5, no. 1, pp. 22–
38, Jan. 2011.
[67] M. T. Pich, C. H. Loch, and A. D. Meyer, ‘‘On uncertainty, ambiguity,
and complexity in project management,’’ Manage. Sci., vol. 48, no. 8,
pp. 1008–1023, Aug. 2002, doi: 10.1287/mnsc.48.8.1008.163.
[68] C. M. Beckman, P. R. Haunschild, and D. J. Phillips, ‘‘Friends or
strangers? Firm-specific uncertainty, market uncertainty, and network
partner selection,’’ Org. Sci., vol. 15, no. 3, pp. 259–275, Jun. 2004, doi:
10.1287/orsc.1040.0065.
[69] L. Pantoja, N. Pérez, and G. Moreno, ‘‘Project management by analyzing
trust in digital social networks,’’ RISTI Revista Iberica de Sistemas e
Tecnologias de Informacao, vol. 2020, no. E28, pp. 828–842, 2020.
[70] F. J. Milliken, ‘‘Three types of perceived uncertainty about the
environment: State, effect, and response uncertainty,’’ Acad. Manage.
Rev., vol. 12, no. 1, p. 133, Jan. 1987, doi: 10.2307/257999.
[71] A. DE Meyer, C. H. Loch, and D. Meyer, ‘‘Managing project
uncertainty: From variation to chaos,’’ in Institutional Knowledge At
Singapore Management University, vol. 43. Cambridge, MA, USA: Sloan
Management Review Association, 2002, pp. 1–13. [Online]. Available:
https://ink.library.smu.edu.sg/lkcsb_research
[72] M. Padalkar and S. Gopinath, ‘‘Are complexity and uncertainty distinct
concepts in project management? A taxonomical examination from
literature,’’Int. J. Project Manage., vol. 34, no. 4, pp. 688–700, May 2016,
doi: 10.1016/j.ijproman.2016.02.009.
VOLUME 13, 2025 127277

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
[73] S.-J. Sunny Yang and Y . Chandra, ‘‘Growing artificial entrepreneurs:
Advancing entrepreneurship research using agent-based simulation
approach,’’ Int. J. Entrepreneurial Behav. Res., vol. 19, no. 2,
pp. 210–237, Mar. 2013, doi: 10.1108/13552551311310383.
[74] C. S. Lee and C. Y . Pan, ‘‘An intelligent fuzzy agent for meeting
scheduling decision support system,’’ Fuzzy Sets Syst., vol. 142, no. 3,
pp. 467–488, Mar. 2004, doi: 10.1016/S0165-0114(03)00201-X.
[75] B. Lazzerini and L. Mkrtchyan, ‘‘Analyzing risk impact factors
using extended fuzzy cognitive maps,’’ IEEE Syst. J., vol. 5, no. 2,
pp. 288–297, Jun. 2011. [Online]. Available: http://ieeexplore.
ieee.org/document/258761/
[76] S. Lokpo, W. Owiredu, J. Osei-Yeboah, G. Norgbe, L. Kuatsienu,
M. Anim, S. Quarshie, F. Ayroe, F. Ussher, E. Boakye, T. Ntoni,
P. Nyamadi, and R. Avorkliyah, ‘‘Chronic kidney disease among
Ghanaian HIV individuals on HAART in the ho municipality: A single-
center descriptive cross-sectional study,’’ Asian J. Biol., vol. 5, no. 1,
pp. 1–10, Jan. 2018, doi: 10.9734/ajob/2018/38596.
[77] A. Tampuu, T. Matiisen, D. Kodelja, I. Kuzovkin, K. Korjus, J. Aru,
J. Aru, and R. Vicente, ‘‘Multiagent cooperation and competition with
deep reinforcement learning,’’ PLoS ONE, vol. 12, no. 4, pp. 1–15,
Apr. 2017.
[78] L. Wang, J. Chu, and J. Wu, ‘‘Selection of optimum maintenance strate-
gies based on a fuzzy analytic hierarchy process,’’ Int. J. Prod. Econ.,
vol. 107, no. 1, pp. 151–163, May 2007, doi: 10.1016/j.ijpe.2006.08.005.
[79] R. Bello, M. García, and N. Pérez, ‘‘Teoría de los conjuntos aproxi-
mados,’’ in Conceptos y métodos computacionales. Bogota, Colombia:
Distrital Francisco José de Caldas Editorial, 2012.
[80] J. Carbo, N. Sanchez-Pi, and J. M. Molina, ‘‘Agent-based simulation with
NetLogo to evaluate ambient intelligence scenarios,’’ J. Simul., vol. 12,
no. 1, pp. 42–52, Jan. 2018, doi: 10.1057/jos.2016.10.
[81] X. Deng and C. H. Papadimitriou, ‘‘On the complexity of cooperative
solution concepts,’’ Math. Oper. Res., vol. 19, no. 2, pp. 257–266,
May 1994, doi: 10.1287/moor.19.2.257.
[82] O. Leimar and P. Hammerstein, ‘‘Evolution of cooperation through
indirect reciprocity,’’ Proc. Roy. Soc. London. Ser. B, Biol. Sci., vol. 268,
no. 1468, pp. 745–753, Apr. 2001, doi: 10.1098/rspb.2000.1573.
[83] V . Morozov, O. Kalnichenko, A. Timinsky, and I. Liubyma, ‘‘Projects
change management in based on the projects configuration management
for developing complex projects,’’ in Proc. 9th IEEE Int. Conf.
Intell. Data Acquisition Adv. Comput. Syst., Technol. Appl. (IDAACS),
Sep. 2017, pp. 939–941.
[84] J. Ozik, N. Collier, J. Murphy, and M. North, ‘‘The Relogo agent-
based modeling languaje,’’ in Proc. Winter Simulation Coference , 2013,
pp. 1950–1959.
[85] S. Luke, C. Cioffi-Revilla, L. Panait, K. Sullivan, and G. Balan,
‘‘MASON: A multiagent simulation environment,’’ Simulation, vol. 81,
no. 7, pp. 517–527, Jul. 2005, doi: 10.1177/0037549705058073.
[86] B. Andres, R. Sanchis, and R. Poler, ‘‘Modeling and simulation of supply
chains with AnyLogic,’’ in Modelling in Science Education and Learning,
vol. 9. Valencia, España: Universitat Politècnica de València, 2016.
[87] A. A. Ontiveros and M. P. Calvo, ‘‘Introducción Al modelado basado en
agentes,’’ in Una aproximación desde NetLogo. San Luis Potosì, México:
El Colegio de San Luis, 2017.
[88] S. de Marchi and S. E. Page, ‘‘Agent-based models,’’ Annu. Rev. Political
Sci., vol. 17, no. 1, pp. 1–20, May 2014, doi: 10.1146/annurev-polisci-
080812-191558.
[89] M. Huhns and M. Singh, ‘‘Cognitive agents,’’ IEEE Internet Comput.,
vol. 2, no. 6, pp. 87–89, Dec. 1998.
[90] R. Awwad, S. Asgari, and A. Kandil, ‘‘Developing a virtual laboratory
for construction bidding environment using agent-based modeling,’’
J. Comput. Civil Eng., vol. 29, no. 6, pp. 1–14, Nov. 2015, doi:
10.1061/(asce)cp.1943-5487.0000440.
[91] N. Zhao, C. Lei, H. Liu, and C. Wu, ‘‘Improving the effectiveness of
organisational collaborative innovation in megaprojects: An agent-based
modelling approach,’’ Sustainability, vol. 14, no. 15, p. 9070, Jul. 2022.
[92] S. Tisue and U. Wilensky, ‘‘NetLogo: Design and implementation of a
multi-agent modeling environment,’’ in Center for Connected Learning
and Computer-Based. Modeling. Evanston, IL, USA: Northwestern
Univ., Evaston, 2002.
[93] A. Gelman, J. Hill, and A. Vehtari, Regression Other Stories. Cambridge,
U.K.: Cambridge Univ. Press, 2020.
[94] A. Gelman, B. Goodrich, J. Gabry, and A. Vehtari, ‘‘R-squared
for Bayesian regression models,’’ Amer. Statistician, vol. 73, no. 3,
pp. 307–309, Jul. 2019, doi: 10.1080/00031305.2018.1549100.
[95] T. J. Bond-Barnard, L. Fletcher, and H. Steyn, ‘‘Linking trust and
collaboration in project teams to project management success,’’ Int. J.
Manag. Projects Bus., vol. 11, no. 2, pp. 432–457, May 2018, doi:
10.1108/ijmpb-06-2017-0068.
[96] J. V . Brocke and S. Lippe, ‘‘Managing collaborative research projects:
A synthesis of project management literature and directives for future
research,’’ Int. J. Project Manage., vol. 33, no. 5, pp. 1022–1039,
Jul. 2015, doi: 10.1016/j.ijproman.2015.02.001.
[97] H. Bester and W. Güth, ‘‘Is altruism evolutionarily stable?’’ J. Econ.
Behav. Org., vol. 34, no. 2, pp. 193–209, Feb. 1998.
[98] L. Ballesteros-Sánchez, I. Ortiz-Marcos, and R. Rodríguez-Rivero, ‘‘The
impact of executive coaching on project managers’ personal competen-
cies,’’ Project Manage. J., vol. 50, no. 3, pp. 306–321, Jun. 2019, doi:
10.1177/8756972819832191.
[99] P. F. de Araújo Lima, M. Crema, and C. Verbano, ‘‘Risk man-
agement in SMEs: A systematic literature review and future direc-
tions,’’ Eur. Manage. J., vol. 38, no. 1, pp. 78–94, Feb. 2020, doi:
10.1016/j.emj.2019.06.005.
[100] G. Pereira, R. Prada, and P. A. Santos, ‘‘Integrating social power into the
decision-making of cognitive agents,’’ Artif. Intell., vol. 241, pp. 1–44,
Dec. 2016, doi: 10.1016/j.artint.2016.08.003.
LILIANA M. PANTOJA-ROJAS (Graduate Stu-
dent Member, IEEE) received the degree in indus-
trial engineering from the National University
of Colombia, in 2008, the master’s degree in
industrial engineering specializing in management
and quality from the Francisco José de Caldas
District University, in 2012, and the joint master’s
degree in integrated risk management from the
Externado de Colombia University and the ENAE
Business School, Spain, in 2018. She is currently
pursuing the Ph.D. degree in engineering with the Francisco José de Caldas
District University. She has over 15 years of experience leading digital
transformation projects, data analytics, and strategic management in the
public and private sectors. She is a PM SIA at ADRES. She has served
as the National Leader for Open Data Quality in Colombia, promoting
standards adoption, developing evaluation models with artificial intelligence,
and strengthening evidence-based digital governance. She has worked as
the Data Architect, the Data Scientist, and the Analytics Director at entities
such as the Ministry of ICT, DIMAR, the Ministry of Environment, Special
Jurisdiction for Peace, Truth Commission, CAOBA, and IDOM Consulting.
She teaches graduate and undergraduate students at Pontifica Universidad
Javeriana.
MARCO A. ALZATE-MONROY(Senior Member,
IEEE) received the master’s and Ph.D. degrees
in electrical engineering from the Universidad de
los Andes. He was a Development Engineer with
CIEL Ingeniería; a Researcher with the Instituto
Tecnológico de Electrónica y Comunicaciones
(ITEC); a Research Assistant with the Department
of Electrical and Computer Engineering, Univer-
sity of Maryland; and a Research Scientist with
the Information Systems Laboratory, University of
South Florida. He is currently an Electronic Engineer with the Universidad
Distrital Francisco José de Caldas. He is also a Full Professor with
the Faculty of Engineering, Universidad Distrital, and collaborates on
postgraduate courses at Universidad Javeriana and the Universidad de los
Andes. Since 2022, he has been focusing on symbol-grounded language
models, autonomous agent-based project management under uncertainty,
and self-organization phenomena in the human brain. His research interests
include signal processing, dynamic systems control, information theory, and
complex systems with applications in communication networks. He is a
member of the GITUD and IDEAS research groups and a Senior Member
of IIIS.
127278 VOLUME 13, 2025

L. M. Pantoja-Rojas et al.: Cognitive Agent-Based Modeling to Optimize Complex Project Management
VíCTOR H. MEDINA-GARCíA received the
degree in systems engineering from the Francisco
José de Caldas District University, Colombia, the
master’s degree in computer science from the
Polytechnic University of Madrid, and the Ph.D.
degree in computer engineering from the Pontifi-
cal University of Salamanca. He was a Marketing
Specialist with the Universidad del Rosario. He is
currently a Research Professor and the Director of
outreach with the Faculty of Engineering, District
University of Bogotá. He has led academic and research processes focused
on digital transformation, institutional capacity building, and coordination
between universities, businesses, and the government. His areas of work
and teaching focus on knowledge management, software engineering, and
technology-mediated educational innovation. He has spoken at numerous
national and international conferences and participated in research networks
on higher education, ICTs applied to teaching, and university management.
He has also collaborated on inter-institutional projects and supervised
numerous undergraduate and master’s theses, actively contributing to
developing critical and scientific thinking in engineering.
LUIS G. MORENO-SANDOVAL received the
master’s degree in information science and busi-
ness administration and the Ph.D. degree in
engineering with an emphasis in natural language
processing (NLP) from Pontificia Universidad
Javeriana. He is currently an Assistant Professor
with the Department of Systems Engineering,
Pontificia Universidad Javeriana. He is a Systems
Engineer. He has led innovative projects, such as
the Communities of Subjectivity in Onion Layers
(COSSOL) Systems, which enable the study of sociolinguistic and behav-
ioral patterns on platforms like Twitter. He has also participated in applied
projects in the financial and health sectors and has spoken at international
conferences on artificial intelligence, computational linguistics, and data
analysis. With more than 40 academic publications and over 250 citations, his
scientific output covers community detection, reputational risk analysis, and
social media profile classification. His research interests include analyzing
collective subjectivity in digital social networks, combining approaches from
text mining, sentiment analysis, and social network analysis. His work
has received international recognition, notably earning the Second Place
at the PAN@CLEF 2019 Competition, Switzerland, for his research on
sociolinguistic profiling of celebrities.
VOLUME 13, 2025 127279
```
