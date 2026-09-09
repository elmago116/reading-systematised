---
title: "Reframing Superintelligence: Comprehensive AI Services as General Intelligence"
author: Eric Drexler
year: "2019"
Type: Report
DOI: ""
source: https://www.fhi.ox.ac.uk/wp-content/uploads/Reframing_Superintelligence_FHI-TR-2019-1.1-1.pdf
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - Tech/AI
  - themes/ethics
pdfORepub: "[[Reframing Superintelligence Drexler 2019.pdf]]"
---
[[Reframing Superintelligence Drexler 2019.pdf]]

## Full text (extracted from `Reframing Superintelligence Drexler 2019.pdf`)

*Source:* `2PDF/Reframing Superintelligence Drexler 2019.pdf`  
*Extracted:* 2026-06-18

```text
> FHI TECHNICAL REPORT <
Reframing Superintelligence
Comprehensive AI Services
as General Intelligence
K. Eric Drexler
Technical Report #2019-1
Cite as:
Drexler, K.E. (2019): “Reframing Superintelligence: Comprehensive AI Services as Gen-
eral Intelligence”, Technical Report #2019-1, Future of Humanity Institute, University
of Oxford
The views expressed herein are those of the author(s) and do not necessarily reﬂect the views of
the Future of Humanity Institute.

Abstract
Studies of superintelligent-level systems have typically posited AI func-
tionality that plays the role of a mind in a rational utility-directed agent,
and hence employ an abstraction initially developed as an idealized
model of human decision makers. Today, developments in AI technology
highlight intelligent systems that are quite unlike minds, and provide
a basis for a diﬀerent approach to understanding them: Today, we can
consider how AI systems are produced (through the work of research and
development), what they do (broadly, provide services by performing
tasks), and what they will enable (including incremental yet potentially
thorough automation of human tasks).
Because tasks subject to automation include the tasks that comprise
AI research and development, current trends in the ﬁeld promise accel-
erating AI-enabled advances in AI technology itself, potentially lead-
ing to asymptotically recursive improvement of AI technologies in dis-
tributed systems, a prospect that contrasts sharply with the vision of
self-improvement internal to opaque, unitary agents.
The trajectory of AI development thus points to the emergence
of asymptotically comprehensive, superintelligent-level AI services that—
crucially—can include the service of developing new services, both
narrow and broad, guided by concrete human goals and informed by
strong models of human (dis)approval. The concept of comprehensive
AI services (CAIS) provides a model of ﬂexible, general intelligence in
which agents are a class of service-providing products, rather than a
natural or necessary engine of progress in themselves.
Ramiﬁcations of the CAIS model reframe not only prospects for an
intelligence explosion and the nature of advanced machine intelligence,
but also the relationship between goals and intelligence, the problem
of harnessing advanced AI to broad, challenging problems, and funda-
mental considerations in AI safety and strategy. Perhaps surprisingly,
strongly self-modifying agents lose their instrumental value even as their
implementation becomes more accessible, while the likely context for
the emergence of such agents becomes a world already in possession of
general superintelligent-level capabilities. These prospective capabilities,
in turn, engender novel risks and opportunities of their own.
Further topics addressed in this work include the general architecture
of systems with broad capabilities, the intersection between symbolic and
neural systems, learning vs. competence in deﬁnitions of intelligence,
tactical vs. strategic tasks in the context of human control, and estimates
of the relative capacities of human brains vs. current digital systems.
1

Contents
Preface 15
I Introduction: From R&D automation to comprehensive AI Services 17
I.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17
I.2 The trajectory of AI development reframes AI prospects . . . . . . . . . . 17
I.3 R&D automation suggests atechnology-centered model of recursive improvement 18
I.4 R&D automation suggests a service-centered model of general intelligence . . 19
I.5 The services model abstracts functionality from implementation . . . . . . . 20
I.6 The R&D automation model distinguishes development from functionality . . 20
I.7 Language translation exempliﬁes a safe, potentially superintelligent service 21
I.8 Predictive models of human (dis)approval can aid AI goal alignment . . . . 22
I.9 The R&D-automation/CAIS model reframes prospects for superintelligence 22
II Overview: Questions, propositions, and topics 24
II.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24
II.2 Reframing prospects for an intelligence explosion . . . . . . . . . . . . . 24
II.3 Reframing the nature of advanced machine intelligence . . . . . . . . . . 26
II.4 Reframing the relationship between goals and intelligence . . . . . . . . . 27
II.5 Reframing the problem of using and controlling advanced AI . . . . . . . 28
II.6 Reframing near- and long-term considerations in AI safety and strategy . . 31
II.7 Conclusions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 32
1 R&D automation provides the most direct path to
an intelligence explosion 34
1.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 34
1.2 AI-enabled AI development could lead to an intelligence explosion . . . . . 34
1.3 Risk models have envisioned AGI agents driving an intelligence explosion . 34
1.4 Self-transforming AI agents have no natural role in recursive improvement . 35
1.5 The direct path to an intelligence explosion does not rely on AGI agents . . 35
2 Standard deﬁnitions of “superintelligence” conﬂate
learning with competence 37
2.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 37
2.2 Superintelligence has been deﬁned in terms of adult human competence . . 37
2.3 “Intelligence” often refers instead to learning capacity . . . . . . . . . . . 37
2.4 Learning and competence are separable in principle and practice . . . . . 38
2.5 Patterns of AI learning and competence di ﬀer radically from humans’ . . . 38
3
2.6 Distinguishing learning from competence is crucial to understanding
potential AI control strategies . . . . . . . . . . . . . . . . . . . . . . 39
3 To understand AI prospects, focus on services, not implementations 40
3.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 40
3.2 The instrumental function of AI technologies is to provide services . . . . . 40
3.3 General intelligence is equivalent to general capability development . . . . 41
3.4 The ability to learn is a capability . . . . . . . . . . . . . . . . . . . . . 41
3.5 Implementing new capabilities does not require “self modiﬁcation” . . . . 41
3.6 Service-centered models highlight di ﬀerentiated, task-focused functionality 42
3.7 Service-centered models harmonize with practice in software engineering . 42
3.8 Service-centered AI architectures can facilitate AI alignment . . . . . . . . 42
4 The AI-services model includes both descriptive and prescriptive aspects 44
4.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 44
4.2 The AI-services model describes current AI development . . . . . . . . . 45
4.3 AI-service development scales to comprehensive, SI-level services . . . . . 45
4.4 Adherence to the AI-services model aligns with AI safety . . . . . . . . . 45
4.5 Adherence to the AI-services model seems desirable, natural,
and practical . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46
5 Rational-agent models place intelligence in an
implicitly anthropomorphic frame 46
5.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46
5.2 The concept of mind has framed our concept of intelligence . . . . . . . . 47
5.3 Studies of advanced AI often posit intelligence in a psychomorphic role . . 47
5.4 Intelligent systems need not be psychomorphic . . . . . . . . . . . . . . 48
5.5 Engineering and biological evolution di ﬀer profoundly . . . . . . . . . . 48
5.6 Studies of AI prospects have often made tacitly biological assumptions . . . 48
5.7 Potential mind-like systems are situated in a more general space
of potential intelligent systems . . . . . . . . . . . . . . . . . . . . . . 49
6 A system of AI services is not equivalent to a utility maximizing agent 50
6.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 50
6.2 Systems of SI-level agents have been assumed to act as a single agent . . . . 51
6.3 Individual service providers can be modeled as individual agents . . . . . 51
6.4 Trivial agents can readily satisfy the conditions for VNM rationality . . . . 51
6.5 Trivially-rational agents can employ reasoning capacity of any scope . . . . 52
6.6 High intelligence does not imply optimization of broad utility functions . . 52
6.7 Systems composed of rational agents need not maximize a utility function . 53
4
6.8 Multi-agent systems are structurally inequivalent to single agents . . . . . . 53
6.9 Problematic AI services need not be problematic AGI agents . . . . . . . . 53
6.10 The AI-services model expands the solution-space for addressing AI risks . 54
7 Training agents in human-like environments can provide
useful, bounded services 55
7.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 55
7.2 Does training on human-like tasks conﬂict with the AI-services model? . . . 55
7.3 Human-like learning may be essential to developing general intelligence . . 56
7.4 Current methods build curious, imaginative agents . . . . . . . . . . . . 56
7.5 Human-like competencies do not imply human-like goal structures . . . . 57
7.6 Open-ended learning can develop skills applicable to bounded tasks . . . . 58
7.7 Human-like world-oriented learning nonetheless brings unique risks . . . . 58
8 Strong optimization can strongly constrain AI capabilities, behavior,
and eﬀects 59
8.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 59
8.2 Strong optimization power need not increase AI capability and risk . . . . 60
8.3 Strong optimization is a strong constraint . . . . . . . . . . . . . . . . . 60
8.4 Optimization of AI systems can reduce unintended consequences . . . . . 61
8.5 Strong external optimization can strongly constrain internal capabilities . . 61
8.6 Optimizing an AI system for a bounded task is itself a bounded task . . . . 61
8.7 Superintelligent-level optimization can contribute to AI safety . . . . . . . 62
9 Opaque algorithms are compatible with
functional transparency and control 63
9.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63
9.2 Deep-learning methods are opaque and may remain so . . . . . . . . . . 63
9.3 The scope of information and competencies can be fuzzy, yet bounded . . . 63
9.4 Restricting resources and information at boundaries constrains capabilities . 64
9.5 Providing external capabilities can constrain internal capabilities . . . . . . 65
9.6 Deep learning can help interpret internal representations . . . . . . . . . 65
9.7 Task-space models can enable a kind of “mind reading” . . . . . . . . . . 65
9.8 Mechanisms for transparency and control can be adapted to experience
and circumstances . . . . . . . . . . . . . . . . . . . . . . . . . . . . 66
10 R&D automation dissociates recursive improvement from AI agency 67
10.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67
10.2 R&D automation can employ on diverse, specialized AI tools . . . . . . . 67
10.3 AI R&D automation will reﬂect universal aspects of R&D processes . . . . 67
5
10.4 AI R&D automation will reﬂect the structure of AI development tasks . . . 68
10.5 AI R&D automation leads toward recursive technology improvement . . . . 69
10.6 General SI-level functionality does not require general SI-level agents . . . 69
10.7 The R&D-automation model reframes the role of AI safety studies
and oﬀers potential aﬀordances for addressing AI safety problems . . . . . 69
11 Potential AGI-enabling technologies also enable comprehensive
AI services 70
11.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 70
11.2 In runaway-AGI scenarios, self-improvement precedes risky competencies . 70
11.3 “Self”-improvement mechanisms would ﬁrst accelerate R&D . . . . . . . 71
11.4 “Self”-improvement mechanisms have no special connection to agents . . . 71
11.5 Transparency and control need not impede the pace of AI development . . 71
11.6 Optimization pressures sharpen task focus . . . . . . . . . . . . . . . . 72
11.7 Problematic emergent behaviors di ﬀer from classic AGI risks . . . . . . . 72
11.8 Potential AGI technologies might best be applied to automate
development of comprehensive AI services . . . . . . . . . . . . . . . . 73
12 AGI agents o ﬀer no compelling value 73
12.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 73
12.2 Would AGI development deliver compelling value? . . . . . . . . . . . . 74
12.3 AI systems deliver value by delivering services . . . . . . . . . . . . . . 74
12.4 Providing diverse AI services calls for diverse AI capabilities . . . . . . . . 75
12.5 Expanding AI-application services calls for AI-development services . . . . 75
12.6 The AGI and CAIS models organize similar functions in di ﬀerent ways . . . 75
12.7 The CAIS model provides additional safety-relevant a ﬀordances . . . . . . 76
12.8 The CAIS model enables competition and adversarial checks . . . . . . . . 77
12.9 The CAIS model o ﬀers generic advantages over classic AGI models . . . . . 77
12.10 CAIS aﬀordances mitigate but do not solve AGI-control problems . . . . . 77
13 AGI-agent models entail greater complexity than CAIS 79
13.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 79
13.2 Classic AGI models neither simplify nor explain self improvement . . . . . 79
13.3 Classic AGI models neither simplify nor explain general AI capabilities . . 80
13.4 Classic AGI models increase the challenges of AI goal alignment . . . . . . 80
13.5 The CAIS model addresses a range of problems without sacriﬁcing eﬃciency
or generality . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81
14 The AI-services model brings ample risks 81
14.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81
6
14.2 Prospects for general, high-level AI services reframe AI risks . . . . . . . . 82
14.3 CAIS capabilities could mitigate a range of AGI risks . . . . . . . . . . . 82
14.4 CAIS capabilities could facilitate the development of dangerous AGI agents 83
14.5 CAIS capabilities could empower bad actors. . . . . . . . . . . . . . . . 83
14.6 CAIS capabilities could facilitate disruptive applications . . . . . . . . . . 83
14.7 CAIS capabilities could facilitate seductive and addictive applications . . . 84
14.8 Conditions for avoiding emergent agent-like behaviors call for
further study . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 84
15 Development-oriented models align with deeply-structured AI systems 85
15.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 85
15.2 AI safety research has often focused on unstructured rational-agent models . 85
15.3 Structured systems are products of structured development . . . . . . . . 85
15.4 AI development naturally produces structured AI systems . . . . . . . . . 86
15.5 Structure arises from composing components, not partitioning unitary systems 86
15.6 A development-oriented approach to deeply structured systems suggests a
broad range of topics for further inquiry . . . . . . . . . . . . . . . . . 86
16 Aggregated experience and centralized learning
support AI-agent applications 87
16.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87
16.2 Discussions often assume learning centered on individual agents . . . . . . 88
16.3 Naïve scaling to multi-agent systems replicates individual agents . . . . . 88
16.4 Self-driving vehicles illustrate the power of aggregating experience . . . . . 89
16.5 E ﬃciently organized machine learning contrasts sharply with human learning 89
16.6 Aggregated learning speeds development and amortizes costs . . . . . . . 90
16.7 The advantages of aggregated, amortized learning have implications for
prospective AI-agent applications . . . . . . . . . . . . . . . . . . . . 91
17 End-to-end reinforcement learning is compatible
with the AI-services model 91
17.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 91
17.2 RL and end-to-end training tend to produce black-box systems . . . . . . . 92
17.3 RL and end-to-end training are powerful, yet bounded in scope . . . . . . 92
17.4 General capabilities comprise many tasks and end-to-end relationships . . . 93
17.5 Broad capabilities are best built by composing well-focused competencies . 93
17.6 Deep RL can contribute to R&D automation within the CAIS model
of general AI . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 94
7
18 Reinforcement learning systems are not equivalent
to reward-seeking agents 95
18.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 95
18.2 Reinforcement learning systems di ﬀer sharply from utility-directed agents . 96
18.3 RL systems are neither trained agents nor RL-system developers . . . . . . 96
18.4 RL systems do not seek RL rewards, and need not produce agents . . . . . 96
18.5 RL rewards are not, in general, treated as increments in utility . . . . . . . 96
18.6 Experience aggregation blurs the concept of individual reward . . . . . . . 97
18.7 RL algorithms implicitly compete for approval . . . . . . . . . . . . . . 97
18.8 Distinctions between system levels facilitate transparency and control . . . 97
18.9 RL-driven systems remain potentially dangerous . . . . . . . . . . . . . 98
19 The orthogonality thesis undercuts the generality
of instrumental convergence 98
19.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 99
19.2 The thesis: Any level of intelligence can be applied to any goal (more or less) 99
19.3 A wide range of goals will engender convergent instrumental subgoals . . . 99
19.4 Not all goals engender IC subgoals . . . . . . . . . . . . . . . . . . . . 100
19.5 Not all intelligent systems are goal-seeking agents in the relevant sense . . . 100
19.6 Comprehensive services can be implemented by systems with bounded goals 101
19.7 IC goals naturally arise as tropisms and as intended services . . . . . . . . 101
19.8 Systems with tropisms are not equivalent to agents with “will” . . . . . . . 102
20 Collusion among superintelligent oracles can readily be avoided 103
20.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 103
20.2 Trustworthiness can be an emergent property . . . . . . . . . . . . . . . 103
20.3 A range of conditions may facilitate or disrupt collusion . . . . . . . . . . 104
20.4 Collusion is fragile and easily disrupted . . . . . . . . . . . . . . . . . 105
21 Broad world knowledge can support safe task performance 106
21.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 106
21.2 Bounding task focus does not require bounding world knowledge . . . . . 106
21.3 Extensive world knowledge can improve ( e.g.) translation . . . . . . . . . 107
21.4 Current MT systems are trained on open-ended text corpora . . . . . . . . 107
21.5 Current systems develop language-independent representations of meaning 107
21.6 Scalable MT approaches could potentially exploit extensive world knowledge 108
21.7 Specialized modules can be trained on diverse, overlapping domains . . . . 108
21.8 Safe task focus is compatible with broad, SI-level world knowledge . . . . . 109
21.9 Strong task focus does not require formal task speciﬁcation . . . . . . . . 110
8
22 Machine learning can develop predictive models of human approval 110
22.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 110
22.2 Advanced ML technologies will precede advanced AI agents . . . . . . . . 111
22.3 Advanced ML can implement broad predictive models of human approval . 111
22.4 Text, video, and crowd-sourced challenges can provide training data . . . . 111
22.5 Predictive models of human approval can improve AI safety . . . . . . . . 112
22.6 Prospects for approval modeling suggest topics for further inquiry . . . . . 112
23 AI development systems can support e ﬀective human guidance 113
23.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 113
23.2 Facilitating human guidance is part of the AI-application development task 114
23.3 Development tasks include task selection, system design,
training, testing, deployment, in-use feedback, and upgrades . . . . . . . 114
23.4 We should assume e ﬀective use of natural-language understanding . . . . 114
23.5 Generic models of human (dis)approval can provide useful priors . . . . . 114
23.6 Bounded task objectives can be described and circumscribed . . . . . . . . 115
23.7 Observation can help systems learn to perform human tasks . . . . . . . . 115
23.8 Deployment at scale enables aggregated experience and centralized learning 116
23.9 Recourse to human advice will often be economical and e ﬀective . . . . . . 116
23.10 AI-enabled criticism and monitoring can strengthen oversight . . . . . . . 116
23.11 AI-enabled AI development could both accelerate application development
and facilitate human guidance . . . . . . . . . . . . . . . . . . . . . . 117
24 Human oversight need not impede fast, recursive
AI technology improvement 118
24.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118
24.2 Must pressure to accelerate AI technology development increase risk? . . . 118
24.3 Basic technology research di ﬀers from world-oriented applications . . . . . 119
24.4 We can distinguish between human participation, guidance, and monitoring . 119
24.5 Guidance and monitoring can operate outside the central AI R&D loop . . . 119
24.6 Fast, asymptotically-recursive basic research need not sacriﬁce safety . . . . 120
24.7 World-oriented applications bring a di ﬀerent range of concerns . . . . . . 120
25 Optimized advice need not be optimized to induce its acceptance 120
25.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 121
25.2 Background (1): Classic concerns . . . . . . . . . . . . . . . . . . . . . 121
25.3 Background (2): Development-oriented models . . . . . . . . . . . . . . 121
25.4 Optimization for results favors manipulating clients’ decisions . . . . . . . 122
25.5 Optimization for results conditioned on actions does not entail optimization
to manipulate clients’ decisions . . . . . . . . . . . . . . . . . . . . . 122
9
25.6 Oracles can suggest options with projected costs, beneﬁts, and risks . . . . 122
25.7 Competitive pressures may nonetheless favor AI systems that produce
perversely appealing messages . . . . . . . . . . . . . . . . . . . . . . 123
26 Superintelligent-level systems can safely provide
design and planning services 123
26.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 123
26.2 Design engineering is a concrete example of a planning task . . . . . . . . 124
26.3 AI-based design systems match classic templates for emergent AI-agent risk 124
26.4 High-level design tasks comprise distinct non-agent-like subtasks . . . . . 125
26.5 Real-world task structures favor ﬁner-grained task decomposition . . . . . 126
26.6 Use of task-oriented components minimizes or avoids classic AI risks . . . . 126
26.7 E ﬀective human oversight is not an impediment, but a source of value . . . 127
26.8 SI-level systems could solve more AI-control problems than they create . . 127
26.9 Models of human concerns and (dis)approval can augment direct oversight . 127
26.10 The pursuit of superintelligent-level AI design services need not entail classic
AI-agent risks . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 128
27 Competitive pressures provide little incentive to transfer strategic deci-
sions to AI systems 129
27.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 129
27.2 Pressures for speed and quality can favor AI control of decisions . . . . . . 129
27.3 Speed is often critical in selecting and executing “tactical” actions . . . . . 129
27.4 Quality is more important than speed in strategic planning . . . . . . . . 130
27.5 System that can make excellent decisions could suggest excellent options . . 130
27.6 Human choice among strategies does not preclude swift response to change 130
27.7 Senior human decision makers will likely choose to retain their authority . . 131
28 Automating biomedical R&D does not require deﬁning human welfare 131
28.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 131
28.2 Broad, unitary tasks could present broad problems of value alignment . . . 132
28.3 Diverse AI systems could automate and coordinate diverse research tasks . . 132
28.4 Human oversight can be supported by AI tools . . . . . . . . . . . . . . 133
28.5 Strong task alignment does not require formal task speciﬁcation . . . . . . 133
28.6 The advantages of assigning broad, unitary tasks to AGI agents are questionable 134
29 The AI-services model reframes the potential roles of AGI agents 135
29.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 135
29.2 It has been common to envision AGI agents in a weak-AI context . . . . . . 135
29.3 Broad, SI-level services will (or readily could) precede SI-level AI agents . . 136
10
29.4 SI-level services will enable the implementation of AGI agents . . . . . . . 136
29.5 SI-level advisory and security services could limit AGI-agent risks . . . . . 137
29.6 SI-level capabilities could mitigate tensions between security concerns and
ethical treatment of non-human persons . . . . . . . . . . . . . . . . . 138
29.7 Prospects for superintelligence should be considered in the context of an
SI-level AI services milieu . . . . . . . . . . . . . . . . . . . . . . . . 138
30 Risky AI can help develop safe AI 139
30.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 139
30.2 A familiar threat model posits opaque, self-improving, untrusted AI systems 140
30.3 Open-ended “self-improvement” implies strong, general AI implementation
capabilities . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 140
30.4 Successful system development can be recapitulated with variations . . . . 141
30.5 Optimization can favor the production of compact, general learning kernels 141
30.6 Competitive optimization for compactness can exclude problematic
information and competencies . . . . . . . . . . . . . . . . . . . . . . 143
30.7 Exclusion of problematic content can provide a safe basis for developing
general capabilities . . . . . . . . . . . . . . . . . . . . . . . . . . . 143
31 Supercapabilities do not entail “superpowers” 145
31.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 145
31.2 AI-enabled capabilities could provide decisive strategic advantages . . . . 145
31.3 Super powers must not be confused with supercapabilities . . . . . . . . . . 145
32 Unaligned superintelligent agents need not threaten world stability 146
32.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 146
32.2 General, SI-level capabilities can precede AGI agents . . . . . . . . . . . 147
32.3 SI-level capabilities could be applied to strengthen defensive stability . . . 147
32.4 Unopposed preparation enables strong defensive capabilities . . . . . . . 148
32.5 Strong defensive capabilities can constrain problematic agents . . . . . . . 148
32.6 This brief analysis necessarily raises more questions than it can explore . . 150
32.7 A familiar alternative scenario, global control by a value-aligned AGI agent,
presents several diﬃculties . . . . . . . . . . . . . . . . . . . . . . . . 150
33 Competitive AI capabilities will not be boxed 151
33.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 151
33.2 SI-level capabilities will likely emerge from incremental R&D automation . 151
33.3 We can expect AI R&D capacity to be distributed widely, beyond any “box” . 151
33.4 AI systems will be instantiated together with diverse peer-level systems . . 152
11
33.5 The ability to instantiate diverse, highly-capable systems presents both risks
and opportunities for AI safety . . . . . . . . . . . . . . . . . . . . . . 152
34 R&D automation is compatible with both strong and weak centralization 153
34.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 153
34.2 The R&D automation model is compatible with decentralized development . 153
34.3 Accelerating progress could lead to strong centralization of capabilities . . 153
34.4 Centralization does not imply a qualitative change in R&D tasks . . . . . . 154
34.5 Centralization and decentralization provide diﬀering aﬀordances relevant to
AI policy and strategy . . . . . . . . . . . . . . . . . . . . . . . . . . 154
35 Predictable aspects of future knowledge can inform AI safety strategies 154
35.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 154
35.2 Advanced AI systems will be preceded by similar but simpler systems . . . 155
35.3 Large-scale successes and failures rarely precede smaller successes and failures 155
35.4 AI researchers eagerly explore and exploit surprising capabilities . . . . . 156
35.5 AI developers will be alert to patterns of unexpected failure . . . . . . . . 156
35.6 AI safety researchers will be advising (responsible) AI developers . . . . . 156
35.7 Considerations involving future safety-relevant knowledge call for further
exploration . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 156
36 Desiderata and directions for interim AI safety guidelines 157
36.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 157
36.2 Desiderata . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 158
36.3 Good practice in development tends to align with safety concerns . . . . . 159
36.4 Exploring families of architectures and tasks builds practical knowledge . . 159
36.5 Task-oriented development and testing improve both reliability and safety . 159
36.6 Modular architectures make systems more understandable and predictable . 159
36.7 Interim safety guidelines can foster ongoing progress . . . . . . . . . . . 160
37 How do neural and symbolic technologies mesh? 161
37.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 161
37.2 Motivation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 161
37.3 A crisp taxonomy of NN and S/A systems is elusive and unnecessary . . . . 162
37.4 NN and S/A techniques are complementary . . . . . . . . . . . . . . . . 162
37.5 AI-service development can scale to comprehensive, SI-level services . . . . 163
37.6 Integration at the level of components and mechanisms . . . . . . . . . . 163
37.7 Integration at the level of algorithmic and representational structures . . . 166
37.8 Integration at the level of systems and subsystems . . . . . . . . . . . . . 169
37.9 Integration of NN and S/A techniques is a rich and active research frontier . 170
12
38 Broadly-capable systems coordinate narrower systems 171
38.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 171
38.2 Today’s superhuman competencies reside in organizational structures . . . 172
38.3 Specialization has robust advantages in learning diverse competencies . . . 172
38.4 Division of knowledge and labor is universal in performing complex tasks . 172
38.5 Current AI services show strong task di ﬀerentiation . . . . . . . . . . . . 173
38.6 AI systems trained on seemingly indivisible tasks learn to divide labor . . . 173
38.7 Black-box abstractions discard what we know about the architecture of
systems with broad capabilities . . . . . . . . . . . . . . . . . . . . . 173
39 Tiling task-space with AI services can provide general AI capabilities 174
39.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 174
39.2 Broad capabilities call for mechanisms that compose diverse competencies . 175
39.3 The task-space concept suggests a model of integrated AI services . . . . . 175
39.4 Embeddings in high-dimensional spaces provide powerful representations . 176
39.5 High-dimensional embeddings can represent semantically rich domains . . 177
39.6 Proximity-based (application/activation/access) can deliver diverse services 177
39.7 PBA operations are pervasive in deep learning systems . . . . . . . . . . 178
39.8 Joint embeddings can link related semantic domains . . . . . . . . . . . 179
39.9 PBA operations can help match tasks to candidate services at scale . . . . . 179
39.10 PBA operations can help match new tasks to service-development services . 181
39.11 Integrated, extensible AI services constitute general artiﬁcial intelligence . . 182
40 Could 1 PFLOP/s systems exceed the basic
functional capacity of the human brain? 182
40.1 Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 182
40.2 Metrics and methodology . . . . . . . . . . . . . . . . . . . . . . . . 183
40.3 Estimated ratios for speciﬁc machine tasks . . . . . . . . . . . . . . . . 186
40.4 Even with current methods, training can be fast by human standards . . . . 189
40.5 Large computational costs for training need not substantially undercut the
implications of low costs for applications . . . . . . . . . . . . . . . . . 189
40.6 Conclusions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 190
Afterword 190
Acknowledgements 193
References 194
13

Preface
The writing of this document was prompted by the growing gap between
models that equate advanced AI with powerful agents and the emerging
reality of advanced AI as an expanding set of capabilities (here, “services”)
in which agency is optional. A service-centered perspective reframes both
prospects for superintelligent-level AI and a context for studies of AI safety
and strategy.
Taken as a whole, this work suggests that problems centered onwhat high-
level AI systems might choose to do are relatively tractable, while implicitly
highlighting questions of what humans might choose to do with their capabilities.
This shift, in turn, highlights the potentially pivotal role of high-level AI in
solving problems created by high-level AI technologies themselves.
The text was written and shared as a series of widely-read Google Docs
released between December 2016 and November 2018, largely in response to
discussions within the AI safety community. The organization of the present
document reﬂects this origin: The sections share a common conceptual frame-
work, yet address diverse, overlapping, and often loosely-coupled topics. The
table of contents, titles, subheads, summaries, and internal links are struc-
tured to facilitate skimming by readers with diﬀerent interests. The table of
contents primarily of declarative sentences, and has been edited to read as an
overview.
Several apologies are in order: A number of topics and examples assume a
basic familiarity with deep-learning concepts and jargon, while much of the
content assumes familiarity with concerns regarding artiﬁcial general intelli-
gence circa 2016–18; some sections directly address concepts and concerns
discussed in Superintelligence (Bostrom 2014). In this work, I have made little
eﬀort to assign proper scholarly credit to ideas: Concepts that seem natural,
obvious, or familiar are best treated as latent community knowledge and very
likely have uncited antecedents. Ideas that can reasonably be attributed to
someone else probably should be. Finally, how I frame and describe basic
concepts has shifted over time, and in the interests of early completion, I
have made only a modest eﬀort to harmonize terminology across the original
documents. I thought it best to share the content without months of further
delay.
15

I Introduction: From R&D automation to
comprehensive AI Services
Responsible development of AI technologies can provide an increasingly
comprehensive range of superintelligent-level AI services—including
the service of developing new services—and can thereby deliver the
value of general-purpose AI while avoiding the risks associated with
self-modifying AI agents.
I.1 Summary
The emerging trajectory of AI development reframes AI prospects. Ongo-
ing automation of AI R&D tasks, in conjunction with the expansion of AI
services, suggests a tractable, non-agent-centric model of recursive AI tech-
nology improvement that can implement general intelligence in the form of
comprehensive AI services (CAIS), a model that includes the service of devel-
oping new services. The CAIS model—which scales to superintelligent-level
capabilities—follows software engineering practice in abstracting functional-
ity from implementation while maintaining the familiar distinction between
application systems and development processes. Language translation exem-
pliﬁes a service that could incorporate broad, superintelligent-level world
knowledge while avoiding classic AI-safety challenges both in development
and in application. Broad world knowledge could likewise support predictive
models of human concerns and (dis)approval, providing safe, potentially
superintelligent-level mechanisms applicable to problems of AI alignment.
Taken as a whole, the R&D-automation/CAIS model reframes prospects for
the development and application of superintelligence, placing prospective
AGI agents in the context of a broader range of intelligent systems while
attenuating their marginal instrumental value.
I.2 The trajectory of AI development reframes AI prospects
Past, present, and projected developments in AI technology can inform our
understanding of prospects for superintelligent-level capabilities, providing a
concrete anchor that complements abstract models of potential AI systems. A
development-oriented perspective highlights path-dependent considerations
in assessing potential risks, risk-mitigation measures, and safety-oriented
17
research strategies. The current trajectory of AI development points to asymp-
totically recursive automation of AI R&D that can enable the emergence
of general, asymptotically comprehensive AI services (CAIS). In the R&D-
automation/CAIS model, recursive improvement and general AI capabilities
need not be embodied in systems that act as AGI agents.
Figure 1:Classes of intelligent systems
I.3 R&D automation suggests a technology-centered model of
recursive improvement
Technology improvement proceeds through research and development, a trans-
parent process that exposes component tasks to inspection, refactoring, and
incremental automation.1 If we take advanced AI seriously, then accelerating,
asymptotically-complete R&D automation is a natural consequence:
• By hypothesis, advances in AI will enable incremental automation and
speedup of all human tasks.
• As-yet unautomated AI R&D tasks are human tasks, hence subject to
incremental automation and speedup.
• Therefore, advances in AI will enable incremental automation and
speedup of all AI R&D tasks.
1. Note that component-level opacity is compatible with eﬀective system-level transparency.
18
Today we see automation and acceleration of an increasing range of AI R&D
tasks, enabled by the application of both conventional software tools and tech-
nologies in the AI spectrum. Past and recent developments in the automation
of deep-learning R&D tasks include:
• Diverse mechanisms embodied in NN toolkits and infrastructures
• Black-box and gradient-free optimization for NN hyperparameter search
(Jaderberg et al. 2017)
• RL search and discovery of superior NN gradient-descent algorithms
(Bello et al. 2017)
• RL search and discovery of superior NN cells and architectures (Zoph
et al. 2017)
Today, automation of search and discovery (a ﬁeld that overlaps with “meta-
learning”) requires human deﬁnition of search spaces, and we can expect
that the deﬁnition of new search spaces—as well as fundamental innovations
in architectures, optimization methods, and the deﬁnition and construction
of tasks—will remain dependent on human insight for some time to come.
Nonetheless, increasing automation of even relatively narrow search and dis-
covery could greatly accelerate the implementation and testing of advances
based on human insights, as well as their subsequent integration with other
components of the AI technology base. Exploring roles for new components
(including algorithms, loss functions, and training methods) can be routine,
yet important: as Geoﬀ Hinton has remarked, “A bunch of slightly new ideas
that play well together can have a big impact”.
Focusing exclusively on relatively distant prospects for full automation
would distract attention from the potential impact of incremental research
automation in accelerating automation itself.
I.4 R&D automation suggests a service-centered model of general
intelligence
AI deployment today is dominated by AI services such as language translation,
image recognition, speech recognition, internet search, and a host of services
buried within other services. Indeed, corporations that provide cloud comput-
ing now actively promote the concept of “AI as a service” to other corporations.
Even applications of AI within autonomous systems (e.g., self-driving vehicles)
can be regarded as providing services (planning, perception, guidance) to
other system components.
R&D automation can itself be conceptualized as a set of services that
directly or indirectly enable the implementation of new AI services. Viewing
19
service development through the lens of R&D automation, tasks for advanced
AI include:
• Modeling human concerns
• Interpreting human requests
• Suggesting implementations
• Requesting clariﬁcations
• Developing and testing systems
• Monitoring deployed systems
• Assessing feedback from users
• Upgrading and testing systems
CAIS functionality, which includes the service of developing stable, task-
oriented AI agents, subsumes the instrumental functionality of proposed
self-transforming AGI agents, and can present that functionality in a form
that better ﬁts the established conceptual frameworks of business innovation
and software engineering.
I.5 The services model abstracts functionality from
implementation
Describing AI systems in terms of functional behaviors (“services”) aligns with
concepts that have proved critical in software systems development. These
include separation of concerns, functional abstraction, data abstraction, encap-
sulation, and modularity, including the use of client/server architectures—a
set of mechanisms and design patterns that support eﬀective program design,
analysis, composition, reuse, and overall robustness.
Abstraction of functionality from implementation can be seen as a ﬁgure-
ground reversal in systems analysis. Rather than considering a complex
system and asking how it will behave, one considers a behavior and asks how
it can be implemented. Desired behaviors can be described as services, and
experience shows that complex services can be provided by combinations
of more specialized service providers, some of which provide the service of
aggregating and coordinating other service providers.
I.6 The R&D automation model distinguishes development from
functionality
The AI-services model maintains the distinction between AI development and
AI functionality. In the development-automation model of advanced AI ser-
20
vices, stable systems build stable systems, avoiding both the diﬃculties and po-
tential dangers of building systems subject to open-ended self-transformation
and potential instability.
Separating development from application has evident advantages. For one,
task-focused applications need not themselves incorporate an AI-development
apparatus—there is little reason to think that a system that provides online
language translation or aerospace engineering design services should in addi-
tion be burdened with the tasks of an AI developer. Conversely, large resources
of information, computation, and time can be dedicated to AI development,
far beyond those required to perform a typical service. Likewise, in ongoing
service application and upgrade, aggregating information from multiple de-
ployed systems can provide decisive advantages to centralized development
(for example, by enabling development systems for self-driving cars to learn
from millions of miles of car-experience per day). Perhaps most important,
stable products developed for speciﬁc purposes by a dedicated development
process lend themselves to extensive pre-deployment testing and validation.
I.7 Language translation exempliﬁes a safe, potentially
superintelligent service
Language translation provides an example of a service best provided by
superintelligent-level systems with broad world knowledge. Translation
of written language maps input text to output text, a bounded, episodic,
sequence-to-sequence task. Training on indeﬁnitely large and broad text
corpora could improve translation quality, as could deep knowledge of psy-
chology, philosophy, history, geophysics, chemistry, and engineering. Eﬀective
optimization of a translation system for an objective that weights both qual-
ity and eﬃciency would focus computation solely on the application of this
knowledge to translation.
The process of developing language translation systems is itself a service
that can be formulated as an episodic task, and as with translation itself,
eﬀective optimization of translation-development systems for both quality
and eﬃciency would focus computation solely on that task.
There is little to be gained by modeling stable, episodic service-providers
as rational agents that optimize a utility function over future states of the
world, hence a range of concerns involving utility maximization (to say noth-
ing of self-transformation) can be avoided across a range of tasks. Even
superintelligent-level world knowledge and modeling capacity need not in
itself lead to strategic behavior.
21
I.8 Predictive models of human (dis)approval can aid AI goal
alignment
As noted by Stuart Russell, written (and other) corpora provide a rich source
of information about human opinions regarding actions and their e ﬀects;
intelligent systems could apply this information in developing predictive
models of human approval, disapproval, and disagreement. Potential training
resources for models of human approval include existing corpora of text
and video, which reﬂect millions of person-years of both real and imagined
actions, events, and human responses; these corpora include news, history,
ﬁction, science ﬁction, advice columns, law, philosophy, and more, and could
be augmented and updated with the results of crowd-sourced challenges
structured to probe model boundaries.
Predictive models of human evaluations could provide strong priors and
common-sense constraints to guide both the implementation and actions of AI
services, including strategic advisory services to powerful actors. Predictive
models are not themselves rational agents, yet models of this kind could
contribute to the solution of agent-centered safety concerns. In this connection,
separation of development from application can insulate such models from
perverse feedback loops involving self-modiﬁcation.
I.9 The R&D-automation/CAIS model reframes prospects for
superintelligence
From a broad perspective, the R&D-automation/CAIS model:
• Distinguishes recursive technology improvement from self-improving
agents
• Shows how incremental automation of AI R&D can yield recursive
improvement
• Presents a model of general intelligence centered on services rather than
systems
• Suggests that AGI agents are not necessary to achieve instrumental goals
• Suggests that high-level AI services would precede potential AGI agents
• Suggests potential applications of high-level AI services to general AI
safety
For the near term, the R&D-automation/CAIS model:
• Highlights opportunities for safety-oriented diﬀerential technology de-
velopment
22
• Highlights AI R&D automation as a leading indicator of technology
acceleration
• Suggests rebalancing AI research portfolios toward AI-enabled R&D
automation
Today, we see strong trends toward greater AI R&D automation and broader
AI services. We can expect these trends to continue, potentially bridging the
gap between current and superintelligent-level AI capabilities. Realistic, path-
dependent scenarios for the emergence of superintelligent-level AI capabilities
should treat these trends both as an anchor for projections and as a prospective
context for trend-breaking developments.
23
II Overview: Questions, propositions, and topics
II.1 Summary
This document outlines topics, questions, and propositions that address:
1. Prospects for an intelligence explosion
2. The nature of advanced machine intelligence
3. The relationship between goals and intelligence
4. The problem of using and controlling advanced AI
5. Near- and long-term considerations in AI safety and strategy
The questions and propositions below reference sections of this document that
explore key topics in more depth. From the perspective of AI safety concerns,
this document oﬀers support for several currently-controversial propositions
regarding artiﬁcial general intelligence:
• That AGI agents have no natural role in developing general AI capabili-
ties.
• That AGI agents would oﬀer no unique and substantial value in provid-
ing general AI services.
• That AI-based security services could safely constrain subsequent AGI
agents, even if these operate at a superintelligent level.
II.2 Reframing prospects for an intelligence explosion
II.2.1 Does recursive improvement imply self-transforming agents?
Ongoing automation of tasks in AI R&D suggests a model of asymptotically-
recursive technology improvement that scales to superintelligent-level (SI-
level) systems. In the R&D-automation model, recursive improvement is
systemic, not internal to distinct systems or agents. The model is fully generic:
It requires neither assumptions regarding the content of AI technologies, nor
assumptions regarding the pace or sequence of automation of speciﬁc R&D
tasks. Classic self-transforming AGI agents would be strictly more diﬃcult to
implement, hence are not on the short path to an intelligence explosio
```
