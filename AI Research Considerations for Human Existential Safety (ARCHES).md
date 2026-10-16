---
title: AI Research Considerations for Human Existential Safety (ARCHES)
authors: Andrew Critch, David Krueger
year: "2020"
Type: Preprint
DOI: 10.48550/arXiv.2006.04948
source: https://arxiv.org/abs/2006.04948
created: 2026-06-18
description: Framed in positive terms, this report examines how technical AI research might be steered in a manner that is more attentive to humanity&#39;s long-term prospects for survival as a species. In negative terms, we ask what existential risks humanity might face from AI development in the next century, and by what principles contemporary technical research might be directed to address those risks.A k
tags:
  - tech/Ai
  - themes/ethics
pdfORepub: "[[AI Research Considerations for Human Existential Safety (ARCHES).pdf]]"
---
[[AI Research Considerations for Human Existential Safety (ARCHES).pdf]]

> **Abstract:** Framed in positive terms, this report examines how technical AI research might be steered in a manner that is more attentive to humanity&#39;s long-term prospects for survival as a species. In negative terms, we ask what existential risks humanity might face from AI development in the next century, and by what principles contemporary technical research might be directed to address those risks.
A k

## Full text (extracted from `AI Research Considerations for Human Existential Safety (ARCHES).pdf`)

*Source:* `2PDF/AI Research Considerations for Human Existential Safety (ARCHES).pdf`  
*Extracted:* 2026-06-18

```text
AI Research Considerations for Human
Existential Safety
(ARCHES)
Andrew Critch
Center for Human-Compatible AI
UC Berkeley
David Krueger
MILA
Université de Montréal
June 11, 2020
Abstract
Framed in positive terms, this report examines how technical AI
research might be steered in a manner that is more attentive to hu-
manity’s long-term prospects for survival as a species. In negative
terms, we ask what existential risks humanity might face from AI
development in the next century, and by what principles contempo-
rary technical research might be directed to address those risks.
A key property of hypothetical AI technologies is introduced,
called prepotence, which is useful for delineating a variety of poten-
tial existential risks from artiﬁcial intelligence, even as AI paradigms
might shift. A set of twenty-nine contemporary research directions
are then examined for their potential beneﬁt to existential safety.
Each research direction is explained with a scenario-driven motiva-
tion, and examples of existing work from which to build. The research
directions present their own risks and beneﬁts to society that could
occur at various scales of impact, and in particular are not guaran-
teed to beneﬁt existential safety if major developments in them are
deployed without adequate forethought and oversight. As such, each
direction is accompanied by a consideration of potentially negative
side eﬀects.
Taken more broadly, the twenty-nine explanations of the research
directions also illustrate a highly rudimentary methodology for dis-
cussing and assessing potential risks and beneﬁts of research direc-
tions, in terms of their impact on global catastrophic risks. This
impact assessment methodology is very far from maturity, but seems
valuable to highlight and improve upon as AI capabilities expand.
1
arXiv:2006.04948v1  [cs.CY]  30 May 2020
Preface
At the time of writing, the prospect of artiﬁcial intelligence (AI) posing an
existential risk to humanity is not a topic explicitly discussed at length in
any technical research agenda known to the present authors. Given that
existential risk from artiﬁcial intelligence seems physically possible, and
potentiallyveryimportant,therearenumberofhistoricalfactorsthatmight
have led to the current paucity of technical-level writing about it:
1) Existential safety involves many present and future stakeholders
(Bostrom, 2013), and is therefore a diﬃcult objective for any single
researcher to pursue.
2) The ﬁeld of computer science, with AI and machine learning as sub-
ﬁelds, has not had a culture of evaluating, in written publications, the
potential negative impacts of new technologies (Hecht et al., 2018).
3) Most work potentially relevant to existential safety is also relevant to
smaller-scale safety and ethics problems (Amodei et al., 2016; Cave
and ÓhÉigeartaigh, 2019), and is therefore more likely to be explained
with reference to those applications for the sake of concreteness.
4) The idea of existential risk from artiﬁcial intelligence was ﬁrst popu-
larized as a science-ﬁction trope rather than a topic of serious inquiry
(Rees, 2013; Bohannon, 2015), and recent media reports have leaned
heavily on these sensationalist ﬁctional depictions, a deterrent for
some academics.
We hope to address (1) not by successfully unilaterally forecasting the fu-
ture of technology as it pertains to existential safety, but by inviting others
to join in the discussion. Counter to (2), we are upfront in our examina-
tion of risks. Point (3) is a feature, not a bug: many principles relevant to
existential safety have concrete, present-day analogues in safety and ethics
with potential to yield fruitful collaborations. Finally, (4) is best treated by
simply moving past such shallow examinations of the future, toward more
deliberate and analytical methods.
Our primary intended audience is that of AI researchers (of all levels)
with some preexisting level of intellectual or practical interest in existential
safety, who wish to begin thinking about some of the technical challenges it
might raise. For researchers already intimately familiar with the large vol-
ume of contemporary thinking on existential risk from artiﬁcial intelligence
(much of it still informally written, non-technical, or not explicitly framed
in terms of existential risk), we hope that some use may be found in our
categorization of problem areas and the research directions themselves.
Our primary goal isnot to make the case for existential risk from artiﬁ-
cial intelligence as a likely eventuality, or existential safety as an overriding
ethical priority, nor do we argue for any particular prioritization among
the research directions presented here. Rather, our goal is to illustrate how
researchers already concerned about existential safety might begin thinking
about the topic from a number of diﬀerent technical perspectives. In doing
this, we also neglect many non-existential safety and social issues surround-
ing AI systems. The absence of such discussions in this document is in no
way intended as an appraisal of their importance, but simply a result of
our eﬀort to keep this report relatively focused in its objective, yet varied
in its technical perspective.
2
The arches of the Acueducto de Segovia, thought to have been
constructed circa the ﬁrst century AD (De Feo et al., 2013).
3
0 Contents
0 Contents 4
1 Introduction 6
1.1 Motivation . . . . . . . . . . . . . . . . . . . . . . . . . 6
1.2 Safety versus existential safety . . . . . . . . . . . . . . 8
1.3 Inclusion criteria for research directions . . . . . . . . . 9
1.4 Consideration of side eﬀects . . . . . . . . . . . . . . . 10
1.5 Overview . . . . . . . . . . . . . . . . . . . . . . . . . . 11
2 Key concepts and arguments 12
2.1 AI systems: tools, agents, and more . . . . . . . . . . . 12
2.2 Prepotence and prepotent AI . . . . . . . . . . . . . . . 12
2.3 Misalignment and MPAI . . . . . . . . . . . . . . . . . 15
2.4 Deployment events . . . . . . . . . . . . . . . . . . . . 16
2.5 Human fragility . . . . . . . . . . . . . . . . . . . . . . 17
2.6 Delegation . . . . . . . . . . . . . . . . . . . . . . . . . 19
2.7 Comprehension, instruction, and control . . . . . . . . 20
2.8 Multiplicity of stakeholders and systems . . . . . . . . 21
2.8.1 Questioning the adequacy of single/single delegation 22
2.9 Omitted debates . . . . . . . . . . . . . . . . . . . . . . 23
3 Risk-inducing scenarios 25
3.1 Tier 1: MPAI deployment events . . . . . . . . . . . . . 25
3.1.1 Type 1a: Uncoordinated MPAI development . . . . . 26
3.1.2 Type 1b: Unrecognized prepotence . . . . . . . . . . 26
3.1.3 Type 1c: Unrecognized misalignment . . . . . . . . . 27
3.1.4 Type 1d: Involuntary MPAI deployment . . . . . . . 28
3.1.5 Type 1e: Voluntary MPAI deployment . . . . . . . . 29
3.2 Tier 2: Hazardous social conditions . . . . . . . . . . . 30
3.2.1 Type 2a: Unsafe development races . . . . . . . . . . 30
3.2.2 Type 2b: Economic displacement of humans . . . . . 30
3.2.3 Type 2c: Human enfeeblement . . . . . . . . . . . . 31
3.2.4 Type 2d: ESAI discourse impairment . . . . . . . . . 32
3.3 Omitted risks . . . . . . . . . . . . . . . . . . . . . . . 33
4 Flow-through eﬀects and agenda structure 33
4.1 From single/single to multi/multi delegation . . . . . . 33
4.2 From comprehension to instruction to control . . . . . 34
4.3 Overall ﬂow-through structure . . . . . . . . . . . . . . 34
4.4 Research beneﬁts vs deployment beneﬁts . . . . . . . . 35
4.5 Analogy, motivation, actionability, and side eﬀects . . . 36
5 Single/single delegation research 37
5.1 Single/single comprehension. . . . . . . . . . . . . 38
5.1.1 Direction 1: Transparency and explainability . . . . 39
5.1.2 Direction 2: Calibrated conﬁdence reports . . . . . . 41
5.1.3 Direction 3: Formal veriﬁcation for machine learning
systems . . . . . . . . . . . . . . . . . . . . . . . . . 43
5.1.4 Direction 4: AI-assisted deliberation . . . . . . . . . 45
5.1.5 Direction 5: Predictive models of bounded rationality 47
5.2 Single/single instruction . . . . . . . . . . . . . . . 50
5.2.1 Direction 6: Preference learning . . . . . . . . . . . . 50
4
5.2.2 Direction 7: Human belief inference . . . . . . . . . . 52
5.2.3 Direction 8: Human cognitive models . . . . . . . . . 54
5.3 Single/single control. . . . . . . . . . . . . . . . . . 56
5.3.1 Direction 9: Generalizable shutdown and handoﬀ
methods . . . . . . . . . . . . . . . . . . . . . . . . . 56
5.3.2 Direction 10: Corrigibility . . . . . . . . . . . . . . . 58
5.3.3 Direction 11: Deference to humans . . . . . . . . . . 59
5.3.4 Direction 12: Generative models of open-source equi-
libria . . . . . . . . . . . . . . . . . . . . . . . . . . . 60
6 Single/multi delegation research 62
6.1 Single/multi comprehension . . . . . . . . . . . . . 63
6.1.1 Direction 13: Rigorous coordination models . . . . . 63
6.1.2 Direction 14: Interpretable machine language . . . . 65
6.1.3 Direction 15: Relationship taxonomy and detection . 67
6.1.4 Direction 16: Interpretable hierarchical reporting . . 69
6.2 Single/multi instruction. . . . . . . . . . . . . . . . 71
6.2.1 Direction 17: Hierarchical human-in-the-loop learn-
ing (HHL) . . . . . . . . . . . . . . . . . . . . . . . . 71
6.2.2 Direction 18: Purpose inheritance . . . . . . . . . . . 73
6.2.3 Direction 19: Human-compatible ethics learning . . . 75
6.2.4 Direction 20: Self-indication uncertainty . . . . . . . 77
6.3 Single/multi control . . . . . . . . . . . . . . . . . . 79
7 Relevant multistakeholder objectives 80
7.1 Facilitating collaborative governance . . . . . . . . . . 81
7.2 Avoiding races by sharing control . . . . . . . . . . . . 84
7.3 Reducing idiosyncratic risk-taking . . . . . . . . . . . . 85
7.4 Existential safety systems . . . . . . . . . . . . . . . . . 85
8 Multi/single delegation research 87
8.1 Multi/single comprehension . . . . . . . . . . . . . 87
8.1.1 Direction 21: Privacy for operating committees . . . 87
8.2 Multi/single instruction. . . . . . . . . . . . . . . . 89
8.2.1 Direction 22: Modeling human committee deliberation 89
8.2.2 Direction 23: Moderating human belief disagreements 91
8.2.3 Direction 24: Resolving planning disagreements . . . 92
8.3 Multi/single control . . . . . . . . . . . . . . . . . . 94
8.3.1 Direction 25: Shareable execution control . . . . . . 94
9 Multi/multi delegation research 95
9.1 Multi/multi comprehension . . . . . . . . . . . . . 96
9.1.1 Direction 26: Capacity oversight criteria . . . . . . . 96
9.2 Multi/multi instruction. . . . . . . . . . . . . . . . 98
9.2.1 Direction 27: Social contract learning . . . . . . . . . 98
9.3 Multi/multi control . . . . . . . . . . . . . . . . . . 100
9.3.1 Direction 28: Reimplementation security . . . . . . . 100
9.3.2 Direction 29: Human-compatible equilibria . . . . . 101
10 Further reading 103
10.1 Related research agendas . . . . . . . . . . . . . . . . . 104
11 Acknowledgements 106
12 References 106
5
1 Introduction
AI technology has the potential to alleviate poverty, automate medical re-
search, accelerate clean energy development, and enhance human cognitive
abilities.Suchdevelopmentswouldhavebeendiﬃculttoimagineinconcrete
terms 100 years ago, but are not inconceivable now. If the worldwide AI
research and development community is vigilant in distributing the beneﬁts
of these technologies fairly and equitably to all of humanity, global human
welfare could be drastically and permanently improved.
Unfortunately,anyhumanextinctioneventwouldmeanhumanityceases
or fails to ever enjoy these marvelous beneﬁts. The purpose of this report is
to consider research directions in terms of their potential to steer away from
human extinction risks, toward globally safer outcomes for humanity. While
it is very diﬃcult toforecast whether any particular research direction will
lead to an increase in risk to society, it may still be possible for researchers
tosteer research in safer and more beneﬁcial directions, if we are collectively
attentive and mindful of the potential for both risks and beneﬁts as new
capabilities are developed. Since it is common for researchers to discuss the
potential beneﬁts of their work, this report is focussed almost entirely on
risk.
Why focus on human extinction risk, and not global catastrophic risks
more broadly? For two reasons: relative concreteness, and agreeability.
Many principles for mitigating existential risks also apply to mitigating
global catastrophic risks in general. However, thinking about the potential
for future global catastrophic risks from artiﬁcial intelligence, while morally
compelling, involves a great deal of speculation.
Discussions in computer science can be more focused if there is a con-
crete and agreeably important outcome in mind, and the survival of the hu-
man species is one such an outcome that is relatively concrete and broadly
agreeably important in the landscape of global catastrophic risks.
1.1 Motivation
Taking a positive view of artiﬁcial intelligence, the aim of this report is
to examine how technical AI research might be steered in manner that is
moresensitivetohumanity’slong-termprospectsforsurvivalinco-existence
with AI technology. In negative terms, the aim is to consider how human
extinction could occur if artiﬁcial intelligence plays a signiﬁcant role in that
event, and what principles might help us to avoid such an event.
If human extinction were to occur within the next century, it seems
exceedingly likely that human activities would have precipitated the ex-
tinction event. The reason is simple: nature has not changed much in the
past 10,000 years, and given that nature on its own has not yielded a hu-
man extinction event for the past 100 centuries, it is not a priori likely for
a natural human extinction event to occur in the next century. (Indeed, a
naive application of Laplace’s law of succession would yield a probability
estimate of at most around 1%.) By contrast, within this century, human
extinction could occur through a variety of anthropogenic pathways, includ-
ing bio-terrorism, climate change, nuclear winter, or catastrophic artiﬁcial
intelligence developments (Matheny, 2007; Bostrom, 2013). This report is
focused on the latter.
Unfortunately, there are numerous pitfalls of human reasoning and co-
ordination that mean human extinctionin particular is not a problem we
should expect to avoid by default:
6
“We may be poorly equipped to recognize or plan for extinction
risks (Yudkowsky, 2008b). We may not be good at grasping the
signiﬁcance of very large numbers (catastrophic outcomes) or
very small numbers (probabilities) over large time frames. We
struggle with estimating the probabilities of rare or unprece-
dented events (Kunreuther et al., 2001). Policymakers may not
plan far beyond current political administrations and rarely do
risk assessments value the existence of future generations [For
an exception, see Kent (2004).] We may unjustiﬁably discount
the value of future lives. Finally, extinction risks are market fail-
ures where an individual enjoys no perceptible beneﬁt from his
or her investment in risk reduction. Human survival may thus
be a good requiring deliberate policies to protect.” –Matheny
(2007), Reducing the risk of human extinction.
In an eﬀort to avoid some of these shortfalls of reasoning and coordina-
tion, this document examines how the development of artiﬁcial intelligence
(AI) speciﬁcally could lead to human extinction, and outlines how various
directions of technical research could conceivably be steered to reduce that
risk.
Aside from wishing to avert existential risks in general, there are several
reasons to take seriously the objective of reducing existential risk from
artiﬁcial intelligence speciﬁcally:
1. A variety of advanced AI capabilities could be suﬃcient to pose ex-
istential risks. A central theme of this report, argued further in
Section 2, will be that artiﬁcial intelligence does not need to meet
the conditions of “human-level AI” (Nilsson, 2005), “artiﬁcial general
intelligence” (Goertzel and Pennachin, 2007), or “superintelligence”
(Bostrom, 1998) to become a source of existential risk to humanity.
It is conceivable that increasingly capable AI systems could lead to
human extinction without ever achieving human-level intelligence or
fully general reasoning capabilities.
2. The AI development timeline is unknown.AI development has en-
tered a period of high activity and abundant funding. In the past, AI
research has cycled through periods of excitement and stagnation. “AI
winter” is a term used for a period of reduced funding and interest
in AI. It was previously believed that the current period of activity
might terminate with an AI winter sometime in the 2010s (Hendler,
2008), but this does not seem to have occurred. Others believe that
another AI winter could be yet to come. Grace et al. (2018) conducted
a 2016 survey of the 1634 researchers who published in NIPS 2015,
and found great variation among the respondents, but a majority
of respondents believing “High-level machine intelligence” would be
achieved within a century:
Our survey used the following deﬁnition:
‘High-levelmachineintelligence’(HLMI)isachieved
when unaided machines can accomplish every task
better and more cheaply than human workers.
Each individual respondent estimated the probability of
HLMI arriving in future years. Taking the mean over each
individual, the aggregate forecast gave a 50% chance of
7
HLMI occurring within 45 years and a 10% chance of it
occurring within 9 years. [...] There is large inter-subject
variation: [...] Asian respondents expect HLMI in 30 years,
whereas North Americans expect it in 74 years. [...] Respon-
dents were asked whether HLMI would have a positive or
negative impact on humanity over the long run. They as-
signed probabilities to outcomes on a ﬁve-point scale. The
median probability was 25% for a “good” outcome and 20%
for an “extremelygood” outcome. Bycontrast, theprobabil-
ity was 10% for a bad outcome and 5% for an outcome de-
scribed as “Extremely Bad (e.g., human extinction).” Forty-
eight percent of respondents think that research on mini-
mizing the risks of AI should be prioritized by society more
than the status quo (with only 12% wishing for less).
Given this variation in opinion, combined with the consensus that
HLMI will most likely be developed in this century, it seems pru-
dent to direct some immediate research attention at managing the
concomitant risks.
3. Safe and powerful AI systems could reduce existential risk.If safe and
robust AI technologies continue to be developed, AI technology could
in principle be used to automate a wide range of preventive measures
for averting other catastrophes, thus serving toreduceexistential risk
(Yudkowsky, 2008a).
1.2 Safety versus existential safety
This report is about existential safety. What is the relationship between
existential safety and safety for present-day AI systems? The answer can
be summarized as follows:
1) Deployments of present-day AI technologies do not present existential
risks. Today’s AI systems are too limited in both their capabilities
and their scope of application for their deployment to present risks at
an existential scale.
2) Present-day AI deployments present safety issues which, if solved,
could be relevant to existential safety.For instance, the deployment
of present-day autonomous vehicles present risks to individual human
lives. Solutions to such safety problems that generalize well to more
powerful AI capabilities could be used to improve existential safety
for future AI technologies. On the other hand, safety techniques that
work for present-day AI technologies but fail to generalize for more
powerful AI systems could yield a false sense of security and lead
to existential safety problems later. Questioning which safety tech-
niques and methodologies will generalize well is an important source
of research problems.
3) Present-day AI deployments present non-safety issues which could
later become relevant to existential safety. For instance, consider
present-day AI ethics problems such as fairness, accountability, and
transparency for AI systems.
Many such problems do not present immediate and direct risks to
the physical safety of humans or even their physical property, and are
8
thus not often considered AI safety problems. However, if AI capa-
bilities improve to become much more impactful on a global scale,
ethical issues in the governance of those capabilities could eventually
become matters of existential safety, just as present-day human in-
stitutions can present risks to public safety if not governed ethically
and judiciously.
Points (1)-(3) above can be summarized in the diagram of Figure 1:
Figure 1: Relationship between AI safety, ethics, and existential safety.
A brief review of and comparison of related AI safety research agendas
is provided in Section 10.1, including:
• Aligning Superintelligence with Human Interests(Soares and Fallen-
stein, 2014),
• Research Priorities for Robust and Beneﬁcial Artiﬁcial Intelligence
(Russell et al., 2015),
• Concrete Problems in AI Safety(Amodei et al., 2016),
• Alignment for Advanced Machine Learning Systems(Taylor et al.,
2016), and
• Scalable Agent Alignment via Reward Modeling: a research direction
(Leike et al., 2018).
1.3 Inclusion criteria for research directions
Each research direction in this report has been chosen for its potential to
be used in some way to improve human existential safety. The directions
have been somewhat intentionally sampled from conceptually diverse areas
9
of AI research, so as to avoid neglecting important considerations for how
the technology could develop.
Research directionshave notbeen ﬁltered foronly being relevant to AI
safety or ethics. In particular, many of the selected research directions seem
likely be pursued for reasons entirely unrelated to existential safety, at least
in some form.
Inaddition,theresearchdirectionshave have notbeenﬁlteredforhaving
no potentially negative side eﬀects; otherwise, the result would have been a
very empty document. Instead, reasoning is provided for how each research
direction could potentially be pursued in service of existential safety, to
enable further deliberation and discussion of that potential.
Importantly, the reasoning included with each research directionis not
intended to argue or predict that the catastrophic scenarios discussed in
this report will occur, nor to claim that humanity will or will not take
adequate precautions to prevent catastrophes arising from AI development.
Rather, this report simply aims to form a small part of those precautions.
In particular, this document is by no means a reasonable representation of
the immense number and variety of potential beneﬁcial applications of AI
research.
1.4 Consideration of side eﬀects
None of the research directions in this report are guaranteed to be helpful to
existential safety, especially if they are deployed carelessly or prematurely.
As such, each direction is exposited with a mini-section entitled “Consider-
ation of Side Eﬀects”, intended to encourage researchers to remain mindful
of the potential misapplications of their work.
Unfortunately, it is not yet the norm in computer science research to
write about the potentially negative impact of one’s work in the course of
producing the work. This story has already been well told by the ACM
Future of Computing Academy:
“The current status quo in the computing community is to frame
our research by extolling its anticipated beneﬁts to society. In other
words, rose-colored glasses are the normal lenses through which we
tend to view our work. [...] However, one glance at the news these
days reveals that focusing exclusively on the positive impacts of a
new computing technology involves considering only one side of a
very important story. [...]
We believe that this gap represents a serious and embarrassing in-
tellectual lapse. The scale of this lapse is truly tremendous: it is
analogous to the medical community only writing about the beneﬁts
of a given treatment and completely ignoring the side eﬀects, no mat-
ter how serious they are. [...] What’s more, the public has deﬁnitely
caught on to our community-wide blind spot and is understandably
suspicious of it. [...] After several months of discussion, an idea for
acting on this imperative began to emerge: we can leverage the gate-
keeping functionality of the peer review process. [...] At a high level,
our recommended change to the peer review process in computing
is straightforward: Peer reviewers should require that papers and
proposals rigorously consider all reasonable broader impacts, both
positive and negative.”
– Hecht, B., Wilcox, L., Bigham, J.P., Schöning, J., Hoque, E.,
Ernst, J., Bisk, Y., De Russis, L., Yarosh, L., Anjum, B., Con-
tractor, D. and Wu, C. “It’s Time to Do Something: Mitigating
10
the Negative Impacts of Computing Through a Change to the
Peer Review Process.” (2018) ACM Future of Computing Blog.
https://acm-fca.org/2018/03/29/negativeimpacts/.
In light of this phenomenon, perhaps this report can participate in an
academia-wide shift toward the active consideration of potentially negative
side eﬀects of research outputs, including outputs of the research directions
exposited here.
As readers examine these potential side eﬀects, it is important to re-
member that these are not intended to communicate a forecast of what
will happen, only whatmight happen and ought to be avoided.
1.5 Overview
The logical thrust of this report can be summarized as follows. This sum-
mary is not meant to stand on its own, and thus contains links to the
relevant sections expanding on each point. Please refer to those sections for
supporting arguments.
Existential risks arising from advancements in artiﬁcial intelligence are
physically possible, very important if they occur, and plausible within this
century (Section 1.1). Since existential safety applications of AI research are
somewhat diﬀerent from smaller-scale safety applications (Section 1.2), it
makes sense to begin some manner of explicit discussions of how AI research
could be steered in directions that will avoid existential risks. This report
aims to embody such a discussion (Preface, Section 1.3, and Section 1.4).
For present-day thinking about existential safety to be robustly valuable
for the many potential pathways along which AI technology could develop,
concepts and arguments are needed that will be relevant in a broad variety
of potential futures. Section 2 will attempt to organize together a few such
key ideas. For instance, the potential for humanity tolose control of the
Earth to powerful AI systems is a key consideration, so Section 2.2 will
deﬁne prepotent AI as, roughly speaking, AI technology that would (hy-
pothetically) bring about unstoppable globally signiﬁcant changes to the
Earth. If prepotent AI technology is ever developed, there are many po-
tential pathways through which the eﬀects of that technology could render
the Earth unsurvivable to humans (Section 2.5). Hence, the potential de-
velopment of prepotent AI technology presents a source of existential risk.
Importantly, a hypothetical existential catastrophe arising from AI technol-
ogy need not be attributable to a single, indecomposable AI system (Sec-
tion 2.8); catastrophes could also arise from the aggregate behavior of many
AI systems interacting with each other and/or humans (Section 2.8.1).
How might a catastrophe come about? In general, supposing AI tech-
nology were to someday precipitate an existential catastrophe, there are
a variety of societal errors that might have led up to that event. Such
errors could include coordination failures between AI development teams
(Section 3.1.1), failure to recognize the prepotence of an AI technology be-
fore its deployment (Section 3.1.2), unrecognized misalignment of an AI
system’s speciﬁcations with the long-term preservation of human existence
(Section 3.1.3), or the involuntary or voluntary deployment of a technology
known to be dangerous (Sections 3.1.4 and 3.1.5).
What do these errors have in common? Abstractly, an existential catas-
trophe arising from AI technology could be viewed as an instance of AI
systems failing to “do what humans want.” After all, humans usually do
not wish for humanity to become extinct. Thus, research aiming at exis-
tential safety for future AI systems might begin by studying and improving
11
the interactions between a single AI system and a single human (Section 5)
to ensure that the AI system behaves in a manner desirable to the human.
This could involve methods to help the human comprehend the AI system
(Section 5.1), deliver instructions to the system (Section 5.2), and control
the system if it begins to malfunction (Section 5.3).
However, as soon as any new capability is developed that enables a
single human to delegate to a single AI system for some sort of task, that
capabilityislikelytobereplicatedmanytimesover,leadingtoamultiplicity
of AI systems with similar functionalities (Section 2.8). Thus, any research
anticipatingthepotentiallyglobalimpactsofAItechnologyshouldtakeinto
account the numerous potential side eﬀects of many AI systems interacting
(Section 6).
Moreover, diverse stakeholders can be expected to seek involvement in
the governance of any AI technology that could be suﬃciently impactful
as to present an existential risk (Section 2.8). Therefore, existential safety
solutions involving only single-stakeholder oversight are not likely to be
satisfying on their own (Section 2.8.1). For this and many other reasons,
it makes more sense for AI technology to be developed in a manner that
is well-prepared for oversight by ideologically, politically, and ethnically
diverse people and institutions (Section 7).
In particular, facilitating collaboration in the oversight of AI systems by
diverse stakeholders (Section 7.1) could reduce incentives for research teams
to enter unsafe development races (Section 7.2), mitigate idiosyncratic risk-
taking among the stakeholders (Section 7.3), and increase the likelihood
that systems will someday be developed with existential safety as their
primary purpose (Section 7.4). Sections 8 and 9 therefore adopt a focus on
research directions relevant to one or more AI systems to serve multiple
stakeholders at once. Taken together, the research directions in Sections 5,
6, 8, and 9 constitute an incomplete but conceptually diverse portfolio of
technical topics with potential relevance to existential safety.
2 Key concepts and arguments
There are many potential pathways along which AI technology could de-
velop. This section introduces a few concepts and arguments for addressing
a broad range of hypothetical futures in which existential risks from artiﬁ-
cial intelligence could arise.
2.1 AI systems: tools, agents, and more
By “AI system”, we refer to any collection of one or more automated
decision-making units. The units are not assumed to be cooperating or
competing, and are not assumed to have been created by cooperating or
competing stakeholders. Hence, the term “system” is intentionally gen-
eral and agent-agnostic, and is meant to encompass simple and complex
artifacts of engineering that could variously be called “decision-making
tools”, “agents”, “multi-agent systems”, “societies of machines”, or none of
the above.
2.2 Prepotence and prepotent AI
We say that an AI system or technology isprepotent/"prE-p@-t@nt/ (relative
to humanity) if its deployment would transform the state of humanity’s
12
habitat—currently the Earth—in a manner that isat least as impactful as
humanity and unstoppable to humanity, as follows:
• at least as impactful as humanity: By this we mean that if the AI
system or technology is deployed, then its resulting transformative
eﬀects on the world would be at least as signiﬁcant as humanity’s
transformation of the Earth thus far, including past events like the
agricultural and industrial revolutions.
• unstoppable to humanity: By this we mean that if the AI system or
technology is deployed, then no concurrently existing collective of
humans would have the ability to reverse or stop the transformative
impact of the technology (even if every human in the collective were
suddenly in unanimous agreement that the transformation should be
reversed or stopped). Merely altering the nature of the transformative
impact does not count as stopping it.
InEnglish,theterm“prepotent” means“Verypowerful;superiorinforce,
inﬂuence, or authority; predominant”. On analogy with the terms ‘intelli-
gent/intelligence’ and ‘omnipotent/omnipotence’, we favor the termprepo-
tence/"prE-p@-t@n(t)s/overthemorestandardusage“prepotency” / "pr¯ e-­p¯ o-
t@n(t)-s¯ e/. In a number of Latin-descended languages, direct translations of
“prepotent”, such as “prepotente” and “prépotent”, mean “arrogant”, “over-
bearing”, “high-handed”, “despotic” or “possessing excessive or abusive au-
thority”. These connotations are not typically carried in English, and while
they do not contradict our usage, they are more speciﬁc than we intend.
Before considering what level and types of risks prepotent AI technolo-
gies could pose to humanity, let us ﬁrst consider brieﬂy whether a prepotent
AI system is physically possible to build in principle. In short, the answer is
probably yes. Why should human beings—a product of random evolution
and natural selection—be physically unsurpassable in our ability to con-
trol our physical environment? Indeed, there are at least several classes of
capabilities that might enable an AI technology to be prepotent, including:
• Technological autonomy.Consider an AI system capable of out-
performing the collective eﬀorts of the world’s top human scientists,
engineers and industry professionals in endeavors of novel and inde-
pendent scientiﬁc research and engineering. Let us call such a system
technologically autonomous. Technologically autonomous AI might be
able to build other AI systems that are prepotent, if so directed by
whatever decision process determines its priorities.
As well, technologically autonomous AI itself could constitute prepo-
tent AI if it expands its scientiﬁc activities in the physical world in a
manner that humans cannot contend with. For comparison, consider
how non-human animals are unable to contend with the industrial
expansion of humans.
• Replication speed. The capability of AI systems to self-replicate
and consume the Earth’s physical resources too quickly for human
civilization to intervene would constitute prepotence. To illustrate the
in-principle possibility of such a scenario, consider the destruction of a
large organism by a potent biological virus as a side eﬀect of the virus
rapidly disassembling the organism’s cells to obtain resources for the
virus producing copies of itself. The virus need not be “generally more
intelligent” than the host organism in any natural sense in order to
13
end up destroying the host as a side eﬀect of the virus’s replication
process. The virus needs only to overwhelm or circumvent the host’s
immune system, a domain-speciﬁc problem.
• Social acumen. The capability to socially manipulate human na-
tions to suddenly or gradually cede control of their resources could
enable prepotence. To see the possibility of such a scenario in princi-
ple, consider that the holocaust of World War II was an event precip-
itated in large part by the highly inﬂuential natural language outputs
of a particular human agent during a time of geopolitical unrest.
Because of the potential for such capabilities to cause humanity to lose
control of the future, to develop any of them would mean facing a consid-
erable and highly objectionable risk.
Historical note. The possibility that advanced AI systems could be dif-
ﬁcult to control was considered by thinkers as early as visionary computer
scientist Alan Turing:
“Let us now assume, for the sake of argument, that these ma-
chines are a genuine possibility, and look at the consequences of
constructing them. [...] [I]t seems probable that once the ma-
chine thinking method had started, it would not take long to
outstrip our feeble powers. There would be no question of the
machines dying, and they would be able to converse with each
other to sharpen their wits. At some stage therefore we should
have to expect the machines to take control [... ] – Alan Turing
[1951], “Intelligent Machinery, A Heretical Theory”.
Mathematician and philosopher Norbert Wiener, widely regarded as
the originator of the cybernetics, also remarked at the potential dangers of
powerful “mechanical agencies" with which we “cannot interfere’:
[...] if a bottle factory is programmed on the basis of maximum
productivity,theownermaybemadebankruptbytheenormous
inventory of unsalable bottles manufactured before he learns he
should have stopped production six months earlier. [...]
Disastrous results are to be expected not merely in the world
of fairy tales but in the real world wherever two agencies es-
sentially foreign to each other are coupled in the attempt to
achieve a common purpose. If the communication between these
two agencies as to the nature of this purpose is incomplete, it
must only be expected that the results of this cooperation will
be unsatisfactory.
If we use, to achieve our purposes, a mechanical agency with
whose operation we cannot eﬃciently interfere once we have
started it, because the action is so fast and irrevocable that we
have not the data to intervene before the action is complete,
then we had better be quite sure that the purpose put into the
machine is the purpose which we really desire and not merely a
colorful imitation of it.” (Wiener, 1960)
Prepotent AI vs “transformative AI”.The concept of prepotent AI
may be viewed as deﬁning a subset of what the Open Philanthropy Project
14
has calledtransformative AI(Karnovsky, 2016), which roughly corresponds
to clause 1 of the deﬁnition of prepotent AI. Speciﬁcally, prepotent AI sys-
tems/technologies are transformative AI systems/technologies that are also
unstoppable to humanity after their deployment (clause 2 of the prepotence
deﬁnition).
Prepotence vs “superintelligence”. This report explicitly avoids de-
pendence on the notion of “superintelligence” (Bostrom, 2014) as a con-
ceptual starting point. Bostrom has deﬁned the termsuperintelligence to
refer to “an intellect that is much smarter than the best human brains
in practically every ﬁeld, including scientiﬁc creativity, general wisdom and
social skills” (Bostrom, 1998). This notion of superintelligence helps to sim-
plify certain arguments about the in-principle possibility of existential risk
from artiﬁcial intelligence, because superintelligence seems both physically
possible to build in principle, and plausibly suﬃcient for threatening our
existential safety. However, not all of the competencies stipulated in the
deﬁnition of superintelligence are necessary for an AI technology to pose
a signiﬁcant existential risk. Although Bostrom (2014) argues that super-
intelligence would likely be unstoppable to humanity (i.e., prepotent), his
arguments for this claim (e.g., the “instrumental convergence thesis”) seem
predicated on AI systems approximating some form of rational agency, and
this report aims to deemphasize such unnecessary assumptions. It seems
more prudent not to use the notion of superintelligence as a starting point
for concern, and to instead focus on more speciﬁc sets of capabilities that
present “minimum viable existential risks”, such as technological autonomy,
high replication speed, or social acumen.
2.3 Misalignment and MPAI
In considering any prepotent or even near-prepotent AI technology, one
immediately wonders whether its transformative impact on the world would
be good or bad for humanity.AI alignmentrefers to the problem of ensuring
that an AI system will behave well in accordance with the values of another
entity, such as a human, an institution, or humanity as a whole (Soares and
Fallenstein, 2014; Taylor et al., 2016; Leike et al., 2018).
What should qualify as a misaligned prepotent AI (MPAI)? Setting
aside the diﬃculty of deﬁning alignment with a multi-stakeholder system
such as humanity, where might one draw the threshold between “not very
well aligned” and “misaligned” for a prepotent AI system? For the purpose
of this report, we draw the line at humanity’s ability to survive:
MPAI.We say that a prepotent AI system is amisaligned if it is
unsurvivable (to humanity), i.e., its deployment would bring about
conditions under which the human species is unable to survive.1
Since any unsurvivable AI system is automatically prepotent,mis-
aligned prepotent AI(MPAI) technology andunsurvivable AI tech-
nology are equivalent categories as deﬁned here.
1It is interesting to ask what it means for a particular AI system to “bring about”
unsurvivable conditions, if such conditions occur. This is a question involving account-
ability for AI systems (Barocas and Hardt, 2014), which may become more diﬃcult to
deﬁne for more capable systems. If System A builds System B, and System B brings
about unsurvivable conditions, did System A bring about unsurvivable conditions? Any
scientiﬁc claim that a system will not “bring about” unsurvivable conditions will have
to settle on a deﬁnition in order to be meaningful. For the purposes of this report, the
precise technical deﬁnition of “bring about” is left as an open question.
15
Figure 2: Venn diagram relating “transformative AI”, “prepotent AI”, and “unsurvivable AI”
(“MPAI” in this report). In other contexts less focussed on human survival, it might make
sense to use a diﬀerent threshold to deﬁnemisalignment for prepotent AI, in which case the
term unsurvivable AI could be reserved for what is called MPAI in this report.
Extinctive versus unsurvivable. It may worth noting that humanity
can become extinct in a manner where our habitat is at no point unsurviv-
able, if the extinction is somehow willful. This means there is a category
of extinctive AI that lies strictly between prepotent AI and MPAI, which
includes AI systems that would somehow lead humanity to extinction along
a pathway where humanity has the ability to prevent its extinction at every
point along the way, but somehow fails to exercise this ability, right to the
very end. This may be a very important consideration for humanity, how-
ever, it will not be a key focus of the present document. In fact, Section 2.5
will raise some considerations suggesting that prepotent AI systems may
be unsurvivable by default in a certain sense, in which case intermediate
categories between prepotent AI and MPAI may not be particularly useful
distinctions. In any case, attentive readers wishing to draw this distinction
may often need to treat “human extinction” as a shorthand for “involuntary
human extinction” at some places in this report.
2.4 Deployment events
What counts as the deployment of a prepotent AI system? If an AI system
becomes prepotent after it is already in deployment, shall we consider that
moment “the deployment of a prepotent AI system“? In this report, the
short answer is yes, because the resulting loss of control for humanity from
that point forward may be similar to the result of deploying an AI system
that is already prepotent.
To be more precise, throughout this report,
• a transformative AI deploymentevent refers to either a transforma-
tive AI technology becoming deployed, or a deployed AI technology
becoming transformative.
• a prepotent AI deploymentevent refers to either a prepotent AI tech-
nology becoming deployed, or a deployed AI technology becoming
prepotent;
• an MPAI deploymentevent refers to either an MPAI technology be-
coming deployed, or a deployed AI technology becoming MPAI.
As deﬁned above, these deployment events have the following implications
for what is possible for humanity:
16
→ At the deployment of a transformative AI technology, it follows that
a highly signiﬁcant global transformation of humanity’s habitat will
occur, but that transformation might be reversible or stoppable by
humanity after it occurs.
→ At the deployment of a prepotent AI technology, it follows that hu-
manity has no further ability to reverse or stop the transformative
impact of the system, but might still have some ability to channel or
direct the impact in some way.
→ At the deployment of an MPAI technology, it follows that humanity
has no further ability prevent human extinction from occurring.
Since these deployment events correspond to successively smaller cate-
gories of AI systems having been in active deployment, if they occur they
must occur in a sequence, as in Figure 3.
Figure 3: timeline of hypothetical deployment events
Note in particular thatTtrans can be less thanTprep in a scenario where
a transformative AI system becomes prepotent only after the system is in
active deployment, andTprep can be less thanTMPAI in a scenario where a
prepotent AI system becomes misaligned only after the system is in active
deployment.
2.5 Human fragility
There are numerous pathways through which the deployment of a prepotent
AI system could be unsurvivable to humanity. In short, the reason is that
many possible transformations of the Earth would render it unsurvivable
to humans, and prepotent AI technology by deﬁnition would globally and
unstoppably transform the Earth.
To see this, ﬁrst observe that the physical conditions necessary for hu-
mans to survive are highly speciﬁc, relative to the breadth of environments
inwhichmachinescanoperate.Forinstance,considertheavailabilityofoxy-
gen in the atmosphere, availability of liquid water, absence of many other
compounds that would be noxious to breathe or drink, radiation levels,
air pressure, temperature, and the availability of highly complex digestible
food sources. Each of these is a physical feature of humanity’s surroundings
which, if transformed signiﬁcantly, would be unsurvivable. By contrast, ma-
chines can already be designed to operate under the ocean, in space, and
on Mars. Humans can also visit these places, but only with the help of
machines to maintain safe conditions for the human body.
Next, recall that the deployment of a prepotent AI technology by def-
inition brings about changes to the Earth at a global scale, in a manner
that humans cannot reverse or stop. At ﬁrst such changes might not result
in inevitable human extinction. However, many vectors of change would, if
compounded over time, end up violating one of the many physical, chemi-
cal, and biological prerequisites needed for human survival. Over the past
century it has become clear that human-driven changes to the Earth have
17
the potential to destroy the human species as a side eﬀect. The variety of
possible AI-driven changes expands and accelerates this potential. While
any particular pathway to unsurvivability is unlikely, the likelihood that
some such pathway could obtain is much higher, because of the many con-
ditions which, if violated, would end human existence. This conclusion has
been argued by numerous others, including Yudkowsky (2008a), Shulman
(2010), Shanahan (2015), and Bostrom (2018).
Of course, it is not logically impossible for humans to survive the de-
ployment of a prepotent AI technology. Preserving conditions necessary for
human survival means operating within certain limits, and if the creators of
the technology were collectively mindful of human extinction as a potential
side eﬀect, perhaps great care and coordination may have been undertaken
toensurethoselimitswouldbepermanentlyenforced.Onemighteventhink
the conditions for human survival are relatively easy to maintain, because
they have been maintained for at least as long as humanity has existed.
However, it is reasonable to expect that the deployment of anarbitrarily
generated prepotent AI system would most likely be unsurvivable to hu-
mans if deployed, just as the conditions of an arbitrarily generated planet
would be unsurvivable to humans.
This raises a key question regarding the danger of prepotence: how dif-
ﬁcult is it to ensure that the deployment of prepotent AI technology would
be survivable to humans? Certainly we humans could all agree to never cre-
ate or allow the development of prepotent AI technology in the ﬁrst place,
but this is not an answer to the question at hand: conditional on the de-
ployment of a prepotent AI technology, what is the chance that humanity
would be unable to survive? In statistical terms, this is a question about
the distribution from which the prepotent AI technology would be drawn,
and that distribution itself is a function of the eﬀort humanity collectively
puts into constraining AI development through coordinated safety eﬀorts.
For instance, if the AI research community as a whole became deeply en-
gaged in the technical challenge of preserving human existence, perhaps
that would be enough to eventually relinquish control of the Earth to pre-
potent AI technology while maintaining survivable conditions for humans.
Would a lesser degree of care suﬃce?
An answer to this question is beyond the scope of this report. It would
be a claim relating the fragility of human existence with the coordinated
aptitude of the worldwide AI research and development community.
On one hand, Perrow’s theory of Normal Accidents (Perrow, 1984)
would imply that if AI technology turns the world as a whole into a “tightly
coupled complex system”, then catastrophic failures should be expected by
default. On the other hand, the literature onhighly reliable organizations
(LaPorte, 1996; Roberts and Bea, 2001a) is suggestive that well-managed
hazardous systems can operate for periods of decades without incident.
Could humans ever succeed in developing prepotent AI technology that
would operate as safely as a highly reliable human organization, over the
indeﬁnite future?
Attempting this would seem an 
```
