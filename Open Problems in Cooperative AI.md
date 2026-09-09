---
title: Open Problems in Cooperative AI
author: Allan Dafoe, Edward Hughes, Yoram Bachrach, Tantum Collins, Kevin R. McKee, Joel Z. Leibo, Kate Larson, Thore Graepel
year: "2020"
Type: Preprint
DOI: 10.48550/arXiv.2012.08630
source: https://arxiv.org/abs/2012.08630
created: 2026-06-18
description: Problems of cooperation--in which agents seek ways to jointly improve their welfare--are ubiquitous and important. They can be found at scales ranging from our daily routines--such as driving on highways, scheduling meetings, and working collaboratively--to our global challenges--such as peace, commerce, and pandemic preparedness. Arguably, the success of the human species is rooted in our ability
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Open Problems in Cooperative AI.pdf]]"
---
[[Open Problems in Cooperative AI.pdf]]

> **Abstract:** Problems of cooperation--in which agents seek ways to jointly improve their welfare--are ubiquitous and important. They can be found at scales ranging from our daily routines--such as driving on highways, scheduling meetings, and working collaboratively--to our global challenges--such as peace, commerce, and pandemic preparedness. Arguably, the success of the human species is rooted in our ability

## Full text (extracted from `Open Problems in Cooperative AI.pdf`)

*Source:* `2PDF/Open Problems in Cooperative AI.pdf`  
*Extracted:* 2026-06-18

```text
2020-12-17
Open Problems in Cooperative AI
Allan Dafoe1, Edward Hughes2, Yoram Bachrach2, Tantum Collins2, Kevin R. McKee2, Joel Z. Leibo2,
Kate Larson2, 3and Thore Graepel2
1Centre for the Governance of AI, Future of Humanity Institute, University of Oxford,2DeepMind, 3University of
Waterloo
Problems of cooperation—in which agents seek ways to jointly improve their welfare—are ubiquitous and
important. They can be found at scales ranging from our daily routines—such as driving on highways,
scheduling meetings, and working collaboratively—to our global challenges—such as peace, commerce,
and pandemic preparedness. Arguably, the success of the human species is rooted in our ability to
cooperate. Since machines powered by artiﬁcial intelligence are playing an ever greater role in our lives,
it will be important to equip them with the capabilities necessary to cooperate and to foster cooperation.
We see an opportunity for the ﬁeld of artiﬁcial intelligence to explicitly focus eﬀort on this class of
problems, which we termCooperative AI. The objective of this research would be to study the many
aspects of the problems of cooperation and to innovate in AI to contribute to solving these problems.
Central goals include building machine agents with the capabilities needed for cooperation, building
tools to foster cooperation in populations of (machine and/or human) agents, and otherwise conducting
AI research for insight relevant to problems of cooperation. This research integrates ongoing work
on multi-agent systems, game theory and social choice, human-machine interaction and alignment,
natural-language processing, and the construction of social tools and platforms. However, Cooperative AI
is not the union of these existing areas, but rather an independent bet about the productivity of speciﬁc
kinds of conversations that involve these and other areas. We see opportunity to more explicitly focus on
the problem of cooperation, to construct uniﬁed theory and vocabulary, and to build bridges with adjacent
communities working on cooperation, including in the natural, social, and behavioural sciences.
Conversations on Cooperative AI can be organized in part in terms of the dimensions of cooperative oppor-
tunities. These include the strategic context, the extent of common versus conﬂicting interest, the kinds
of entities who are cooperating, and whether researchers take the perspective of an individual or of a
social planner. Conversations can also be focused on key capabilities necessary for cooperation, such as
understanding, communication, cooperative commitments, and cooperative institutions. Finally, research
should study the potential downsides of cooperative capabilities—such as exclusion and coercion—and
how to channel cooperative capabilities to best improve human welfare. This research would connect AI
researchtothebroaderscientiﬁcenterprisestudyingtheproblemofcooperation,andtothebroadersocial
eﬀort to solve cooperation problems. This conversation will continue at: www.cooperativeAI.com
Prepared for theNeurIPS 2020 Cooperative AI Workshop
Current draft: December 15 2020.
First draft: August 2019.
arXiv:2012.08630v1  [cs.AI]  15 Dec 2020
Contents
1 Introduction 3
2 Why Cooperative AI? 4
2.1 Vignettes: Self-Driving Vehicles and COVID-19 . . . . . . . . . . . . . . . . . . . . . . 4
2.2 Prior Work, Machine Learning, and Timeliness . . . . . . . . . . . . . . . . . . . . . . 7
3 Cooperative Opportunities 8
3.1 Common and Conﬂicting Interests . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
3.2 Who is Cooperating: Humans, Machines, Organizations . . . . . . . . . . . . . . . . . 11
3.3 The Individual Perspective and the Planner Perspective . . . . . . . . . . . . . . . . . . 12
3.4 Scope . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
4 Cooperative Capabilities 14
4.1 Understanding . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
4.1.1 The World . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
4.1.2 Behaviour . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
4.1.3 Preferences . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 17
4.1.4 Recursive Beliefs . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
4.2 Communication . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 19
4.2.1 Common Ground . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
4.2.2 Bandwidth and Latency . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
4.2.3 Teaching . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 22
4.2.4 Mixed Motives . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 23
4.3 Commitment . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24
4.3.1 Commitment Solutions: Unilateral vs Multilateral; Unconditional vs Conditional 24
4.3.2 Devices: Reputation, Delegation, Contracts, Hardware . . . . . . . . . . . . . . 25
4.4 Institutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26
4.4.1 Decentralized Institutions and Norms . . . . . . . . . . . . . . . . . . . . . . . 27
4.4.2 Centralized Institutions . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 28
4.4.3 Trust and Reputation Systems . . . . . . . . . . . . . . . . . . . . . . . . . . . 29
4.4.4 Cooperative AI Problems and Institutions . . . . . . . . . . . . . . . . . . . . . 30
5 The Potential Downsides of Cooperative AI 30
5.1 Exclusion and Collusion . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 30
5.2 Coercive Capabilities . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 31
5.3 The Role of Coercion and Competition in Cooperation . . . . . . . . . . . . . . . . . . 31
5.4 Understanding and Mitigating the Downsides . . . . . . . . . . . . . . . . . . . . . . . 32
6 Conclusion 33
7 Acknowledgments 33
8 Appendix A: Cooperative AI Workshop - NeurIPS 2020 34
2
Open Problems in Cooperative AI
1. Introduction
Problems of cooperation—in which agents have opportunities to improve their joint welfare but are not
easily able to do so—are ubiquitous and important. They can be found at all scales ranging from our
daily routines—such as driving on highways, scheduling meetings, and working collaboratively—to our
global challenges—such as peace, commerce, and pandemic preparedness. Human civilization and the
success of the human species depends on our ability to cooperate.
Advances in artiﬁcial intelligence pose increasing opportunity for AI research to promote human
cooperation. AI research enables newtools for facilitating cooperation, such as language translation,
human-computer interfaces, social and political platforms, reputation systems, algorithms for group
decision-making, and other deployed social mechanisms; it will be valuable to have explicit attention to
what tools are needed, and what pitfalls should be avoided, to best promote cooperation. AIagents will
play an increasingly important role in our lives, such as in self-driving vehicles, customer assistants, and
personal assistants; it is important to equip AI agents with the requisite competencies to cooperate with
others (humans and machines). Beyond the creation of machine tools and agents, the rapid growth of
AI research presents other opportunities for advancing cooperation, such as fromresearch insightsinto
social choice theory or the modeling of social systems.
The ﬁeld of artiﬁcial intelligence has an opportunity to increase its attention to this class of problems,
which we refer to collectively as problems inCooperative AI. The goal would be to study problems of
cooperationthroughthelensofartiﬁcialintelligenceandtoinnovateinartiﬁcialintelligencetohelpsolve
these problems. Whereas much AI research to date has focused on improving the individual intelligence
of agents and algorithms, the time is right to also focus on improvingsocial intelligence: the ability of
groups to eﬀectively cooperate to solve the problems they face.
AI research relevant to cooperation has been taking place in many diﬀerent areas, including in
multi-agent systems, game theory and social choice, human-machine interaction and alignment, natural-
language processing, and the construction of social tools and platforms. Our recommendation is
not merely to construct an umbrella term for these areas, but rather to encourage focused research
conversations, spanning these areas, focused on cooperation. We see opportunity to construct more
uniﬁed theory and vocabulary related to problems of cooperation. Having done so, we think AI research
will be in a better position to learn from and contribute to the broader research program on cooperation
spanning the natural sciences, social sciences, and behavioural sciences.
Our overview comes from the perspective of authors who are especially impressed by and immersed
in the achievements of deep learning [Sej20] and reinforcement learning [SB18]. From that perspective,
it will be important to develop training environments, tasks, and domains that can provide suitable
feedback for learning and in which cooperative capabilities are crucial to success, non-trivial, learnable,
and measurable. Much research in multi-agent systems and human-machine interaction will focus on
cooperation problems in contexts of pure common interest. This will need to be complemented by
research in mixed-motives contexts, where problems of trust, deception, and commitment arise. Machine
agentswilloftenactonbehalfofparticularhumansandwillimpactotherhumans; asaconsequence, this
research will need to consider how machines can adequately understand human preferences, and how
best to integrate human norms and ethics into cooperative arrangements. Researchers building social
toolsandplatformswillhaveotherperspectivesonhowbesttomakeprogressonproblemsofcooperation,
including being especially informed by real-world complexities. Areas such as trusted hardware design
and cryptography may be relevant for addressing commitment problems and cryptography. Other aspects
of the problem will beneﬁt from expertise from other sciences, such as political science, law, economics,
sociology, psychology, and neuroscience. We anticipate much value in explicitly connecting AI research
to the broader scientiﬁc enterprise studying the problem of cooperation and to the broader eﬀort to
3
Open Problems in Cooperative AI
solve societal cooperation problems.
Werecommendthat“CooperativeAI”begivenatechnicallyprecise,problem-deﬁnedscope;otherwise,
there is a risk that it acquires an amorphous cloud of meaning, incorporating adjacent (clusters of)
concepts such as aligned AI, trustworthy AI, and beneﬁcial AI. Cooperative AI, as scoped here, refers to
AI research trying to help individuals, humans and machines, to ﬁnd ways to improve their joint welfare.
For any given situation and set of agents, this problem is relatively well deﬁned and unambiguous. The
Scope section elaborates on the relationship to adjacent areas.
Conversations on Cooperative AI can be organized in part in terms of the dimensions of cooperative
opportunities. These include the strategic context, the extent of common versus conﬂicting interest,
the kinds of entities who are cooperating, and whether the researchers are focusing on the cooperative
competence of individuals or taking the perspective of a social planner. Conversations can also be focused
on key capabilities necessary for cooperation, including:
1. Understanding of other agents, their beliefs, incentives, and capabilities.
2. Communicationbetween agents, including building a shared language and overcoming mistrust
and deception.
3. Constructing cooperativecommitments, so as to overcome incentives to renege on a cooperative
arrangement.
4. Institutions, which can provide social structure to promote cooperation, be they decentralized
and informal, such as norms, or centralized and formal, such as legal systems.
Justasanyareaofresearchcanhavedownsides,soisitprudenttoinvestigatethepotentialdownsides
of research on Cooperative AI. Cooperative competence can be used to exclude others, some cooperative
capabilities are closely related to coercive capabilities, and learning cooperative competence can be
hard to disentangle from coercion and competition. An important aspect of this research, then, will be
investigating potential downsides and studying how best to anticipate and mitigate them.
The remainder of the paper is structured as follows. We oﬀer more motivation in the section Why
Cooperative AI? We then discuss several important dimensions of Cooperative Opportunities. The bulk
of our discussion is contained in the Cooperative Capabilities section, which we organize in terms
of Understanding, Communication, Commitment, and Institutions. We then reﬂect on The Potential
Downsides of Cooperative AI and how to mitigate them. Finally, we conclude.
2. Why Cooperative AI?
2.1. Vignettes: Self-Driving Vehicles and COVID-19
To ground our discussion, we introduce here two vignettes, one based on the near-term cooperation
problems facing self-driving vehicles, the other about the global challenge of pandemic preparedness.
Self-driving vehicles confront a broad portfolio of cooperation problems with respect to other drivers
(human and AI). There are opportunities for joint welfare gains between drivers (or the principals in
whose interests they are driving).
In order to predict the behaviour of other drivers, an AI, and others on the road, would beneﬁt from
it understanding the goals, beliefs, and capabilities of those other drivers. The AI, and others, would
beneﬁt from it understanding the (local) conventions of driving, such as what side of the road to drive
on. It, and others, beneﬁt from it accurately modeling the beliefs of other agents, such as whether
the fast-walking pedestrian looking at their phone is aware of the car. It, and others, beneﬁt from it
understanding the intentions of other agents, such as that of a driver attempting to urgently cross several
lanes of fast-ﬂowing traﬃc.
4
Open Problems in Cooperative AI
An AI, and others, would beneﬁt from improvedcommunicationskill and infrastructure. Will the
AI understand the wave of a police oﬃcer, indicating that the oﬃcer wants the AI to go through an
intersection? Can it express to other vehicles that the reason it is idling in a narrow parking lot is to wait
for a car up ahead to pull out? Can it accurately, precisely, and urgently express a sudden observation of
dangerous road debris to (AI) drivers behind it? Can it communicate suﬃciently with another brand of
driver AI to achieve the subtle coordination required to safely convoy in close proximity?
Cooperative gains are available to those able to construct crediblecommitments. CarA, in busy
traﬃc, may wish to cross several lanes; carB may be willing to make space forA to do so only ifA
commits to moving along and not staying inB’s lane. Or, suppose a driver is waiting for another car to
pull out of a parking space, blocking other cars looking for parking spots; in principle, the driver would
be willing to allow those other cars to pass, but not if one of them is going to “defect” by taking the
newly opened parking space. Can those other drivers credibly commit to not doing so?
Populations of drivers could be made better oﬀ by newinstitutions, which AI research could help
build. What is the optimal congestion pricing to maximize human welfare, and can this be assessed
and processed through AI-enabled innovations? Are there joint policies for populations of drivers which
are Pareto improving to the typical equilibria from uncoordinated behaviour? If so, could a navigation
app achieve this while maintaining incentive compatibility to participate in the mechanism? Can the
valuable information from the video feeds of the many smart vehicles be optimally distributed, with fair
pricing, safeguards for privacy, and incentive compatibility?
While our ﬁrst example was meant to be grounded in soon-to-be-upon-us technical possibilities,
our second is meant to illustrate the global stakes of making progress in solving cooperation problems.
There are multiple problems of global cooperation with stakes in the trillions of dollars or millions of
lives, including those of disarmament, avoiding nuclear war, climate change, global commerce, and
pandemic preparedness. Given its timeliness, we focus on the last one. While these global problems will
not immediately be the focal problems of Cooperative AI, they illustrate the magnitude of beneﬁts that
could ultimately come from substantial advances in global cooperative competence.
The death toll from COVID-19 is in the millions, and the economic damage is estimated in the tens
of trillions of dollars. Future pandemic diseases could cause similar, or greater, devastation. And yet,
despite these high stakes, the world struggles to prepare adequately, in part due to cooperation problems.
The gains are great from more investment in generalized vaccine development, disease surveillance and
data sharing, harmonization of policy responses so as to avoid unnecessary breakdowns in supply chains,
pooled reserves of supplies to support those who most need them, epidemiological research during the
outbreak, and building coordinating institutions to help achieve these common interests.
But achieving these gains is not trivial. They may require that decision makersunderstand each
other suﬃciently well that they can agree to a fair (enough) division of investment for a problem in
which expected harm and ability to pay are unevenly distributed and hard to estimate. They may require
decision makers to reliablycommunicateon sensitive issues like the existence of a disease outbreak
or the state of one’s medical system. They may require overcoming thecommitment problem arising
from the great pressure for countries to renege on certain agreements in a crisis, such as on sharing of
supplies and not interfering in supply chains. Lastly, building globalinstitutionsposes diﬃcult problems
of institutional design, and the management of diﬃcult political realities, conﬂicts of interest, demands
for legitimacy, and requirements for technical competence.
As these vignettes illustrate, problems of cooperation are ubiquitous, important, and diverse, but
they also share fundamental commonalities. Problems of cooperation span scale: from inter-personal, to
inter-organizational, to inter-state. They can involve two, several, or millions of agents; they exist for
small stakes and global stakes; they arise amongst humans, machines, and organizations; they arise in
5
Open Problems in Cooperative AI
domains with more or less well-deﬁned interests, norms, and institutions.
Cooperative competence requires distinct kinds of social intelligence and skills, which were critical
for the success of humans. Without a cultural inheritance of tools and skills, and a community to
collaborate with, a single human cannot achieve much. Rather, to create our modern technological and
cultural wonders required a community of collaborating humans, ever growing in scale, who passed
their knowledge down through the generations. Furthermore, this capacity evolved beyond a narrow
kind of cooperative intelligence, capable of only solving a limited class of cooperation problems and
brittle to changes, to an increasingly general cooperative intelligence capable of solving dynamic and
complex problems, including interpersonal disputes, cross-border pollution, and global arms control.
Further improvements in humanity’s general cooperative intelligence may be critical for solving our
increasingly complex global problems. As AI systems are deployed throughout the economy, it becomes
important that they be adept at participating cooperatively in our shared global civilization—which is
composed of humans, organizations, and, increasingly, machine agents.
The problem of cooperation is a fundamental scientiﬁc problem for many ﬁelds, from biochemistry,
to evolutionary biology, to the social sciences. Biologists regard the history of life as the progressive
formation of ever larger cooperative structures [SS97], from coalitions of cooperating genes [SS93], to
multi-cellularity requiring restraint on single-cell egoism [Bus87, FN04], to the emergence of complex
societies featuring division of labour in the lineages of ants, termites, and primates [Rob92, MGA¸05].
In 2005,Science Magazinejudged the problem of “How Did Cooperative Behavior Evolve?” to be one of
the top 25 questions “facing science over the next 25 years.”
Theproblemofcooperationisatleastasimportanttosocialscientists. Economistsareofteninterested
in when people achieve, or fail to achieve, welfare-enhancing arrangements. Political scientists study
how people make collective decisions: the very mechanisms by which groups of people cooperate, or
fail to do so. Within international relations and comparative politics, some of the most central and rich
questions concern the causes of costly conﬂict, including civil war and interstate war. Prominent in
sociology is the study of social order: how it emerges, persists, and evolves. Explicitly framing relevant
research in AI as addressing this fundamental problem will help with the consilience of science, allowing
relevant insights across ﬁelds to more readily ﬂow to each other and helping to show these other ﬁelds
the increasing relevance of AI research to understanding cooperation. A more explicit connection across
these ﬁelds will help researchers adopt a common vocabulary and learn from their respective advances.
When considering how to build maximally beneﬁcial AI, many researchers emphasize the impor-
tance of certain directed strands of AI research, such as on safety [AOS¸16, Rus19], fairness [HPS16],
interpretability [OSJ¸18], and robustness [RDT15, QMG¸19]. Each of these points AI research towards
achieving AI with a certain set of attributes, which are thought to be on net socially beneﬁcial, and they
plausibly make for a coherent research program. We recommend that cooperation and Cooperative AI
be added to this list.
TheseandotherareasofAIaredeﬁnedbywhattheyaspiretoachievebytheirgoals. Eventheﬁeldof
“artiﬁcial intelligence” itself is deﬁned through its aspiration to build a kind of machine intelligence that
does not yet exist. Aspirational research programs have the advantage of prominently communicating
what the point of the research is and reminding researchers of some of its long-term goals. Consider, by
contrast, labeling a cluster of this kind of research as being on “multi-agent AI”, “game theory”, “strategic
interaction”: these don’t communicate the social goal of the research and the pro-social bet motivating
the ﬁeld. “Cooperative AI” more clearly points to the social purpose served by pursuing these connected
clusters of research.
6
Open Problems in Cooperative AI
2.2. Prior Work, Machine Learning, and Timeliness
Cooperative AI will draw together research spanning the ﬁeld of artiﬁcial intelligence, as well as many
other disciplines in the natural and social sciences. Accordingly, prior work relevant to Cooperative AI
is vast and will be most meaningfully summarized for particular sub-clusters of work. Reﬂecting the
background of the majority of the authors of this paper, we brieﬂy review prior work here with a heavy
bias towards multi-agent research.
Looking back decades, multi-agent systems research (and before that, the distributed AI research
community) has long been interested in the interactions of intelligent agents and the arising collective
behaviour [Wei99, Fer99, Jen00, PW05, DS04, SLB09, Woo09, BDDS09, JSW98]. Early research from
the1970sand1980semployedcomputationalmodelsforsimulatingsuchsystemsbycombiningelements
of game theory, Monte Carlo simulation, evolutionary programming, and theories of emergence and
complexsystems[ Sch71,AH81,Rey87,Min88]. Duringthe1990sandearly2000s, thefocusofresearch
broadenedfromtechnologiesforjust simulatingreal-worldenvironments toarchitecturesandmethodologies
for solvinginherently distributed problems such as markets, trading and auctions [San96, PDB99, GS01,
NR01, CS02a, Rou10], security and disaster response [SMT¸05, MBMV06, Tam11, FST15], resource
management [PFR09, CDE¸06], automated argumentation, and negotiation [RZ94, SL¸95, JFL¸01,
MPW02, KM06]. More recently, there has been signiﬁcant research on methods through which agents
learn to communicate, collaborate, and interact with one another [CB98, SV00, WRUW03, PL05, ZL10,
LPB16, HT17, ASBB¸17].
Kraus[Kra97]arguedfortheimportanceofstudyingmixed-motivecooperationproblemsandnotjust
pure common-interest problems. She advocated an interdisciplinary approach and organized multi-agent
cooperative work along several dimensions, which will recur in our paper. These are (in our words): the
degree of common interest; the opportunity for building institutions; the number of agents; the kinds of
agents (machines, humans); and the costs and capabilities of both communication and computation.
Panait and Luke [PL05] review work on machine learning in multi-agent cooperation, though mostly
limitedtosettingsofpurecommoninterest. Theydiscusschallengesfromdiﬀerentlearningdynamicsand
illustrate them with simple games and real-world problems. They emphasize the problem of “teammate
modeling”, which maps to the concepts we discuss in Understanding and Communication.
Inthepasttwodecades,researchinmulti-agentsystemshasexplodedtocoverdiverseareasincluding
institutions and norms [Rob04, BVDTV06, AJB06]; human agent interaction [Lew98, GBC07, BFJ11,
SBA¸03]; knowledge representation, reasoning, and planning [Geo88, vdHW02, vHLP08]; multi-agent
adaptation and learning [Wei95, GPP¸98, AKK03, Bow05, SPG07, BBDS08]; social choice and joint
decision-making [PKSA06, CELM07, BCE12]; strategic and economic interactions [RZ94, NR01, Kra01,
PW02, WGSW03, PW15]; simulations of agent societies [MBLA96, AP01, NP08]; and multi-agent
robotics [KAK¸97, BMF¸00, APP¸02, GM04].
Despite the frameworks and methodologies that have been developed over the past decades and the
great potential for multi-agent technologies, progress has been slow in some areas due to the inherent
complexity of the problems [JSW98, Wei99, Sin94, SLB09, Woo09]. In particular, it has long been
noted that open, heterogeneous, and scalable multi-agent systems require learning agents, including
agents who learn to adapt and cooperate with others [LMP03]. In light of the recent progress in our
ability to analyze and learn from data in various forms—including image processing, recognition, and
generation[KSH12,GPAM¸14];voiceandnatural-languageprocessing[ CWB¸11,ODZ¸16,PSM14];and
reinforcement learning [MKS¸15, SHM¸16, BBC¸19]—it is time to reinvigorate research on Cooperative
AI.1
1Inveryrecentwork,astatementcloseinspirittothispaper,producedbysomeofthesameauthors,appearedinaSeptember
2020 announcement for the 2020 NeurIPS Workshop (reproduced in Appendix A) [Coo19]. Another statement invoking similar
motivation to the NeurIPS workshop and this manuscript, though focusing mostly on human-machine cooperation, was a
7
Open Problems in Cooperative AI
Thereareotherreasonswhythetimingisopportune. Withinthedomainofgame-basedreinforcement
learning, the past years have seen tremendous progress on two-player zero-sum games, such as chess
[SHS¸18, Lai15], go [SHS¸18], StarCraft II [VBC¸19], and (two player) poker [BB20].2 Two-player
zero-sum games were a productive domain for early multi-agent research as they are especially tractable:
the minimax solution coincides with the Nash equilibrium and can be computed in polynomial time
through a linear program, their solutions are interchangeable, and they have worst-case guarantees
[vNM07].
However,two-playerzero-sumgamesprovidenoopportunityfortheagentstolearnhowtocooperate,
and it is undesirable for research to be overly focused on domains that are inherently rivalrous. The
ﬁeld of multi-agent reinforcement learning seems to be naturally reorienting towards games of pure
commoninterest, suchasHanabi[ BFC¸20]andOvercooked[ CSH¸19], aswellasteamgames[ JCD¸19].
There is also growth in the study of mixed-motives settings [Bak20], such as alliance politics [HAE¸20,
AET¸20, PLB¸19] and tax policy [ZTS¸20], which will be critical since some strategic dynamics only
arise in these settings, such as issues of trust and commitment problems.
Finally, all else equal, earlier is better in cooperation research, since much of actual cooperation
depends on historically established vocabularies, norms, precedents, protocols, and institutions: as more
and more AI systems are being deployed throughout society, we do not want to unintentionally lock in
sub-optimal equilibria. We want our deployed AIs to be forward compatible with future advances in
cooperation.
3. Cooperative Opportunities
In this section, we will discuss some of the diversity in cooperative opportunities, which are situations in
which agents may be able to achieve joint gains or avoid joint losses. Our discussion will consider four
major dimensions that structure the character of cooperative opportunities and the associated research.
(1) The degree of common versus conﬂicting interest between agents. (2) The kinds of agents attempting
to cooperate, such as machines, humans, or organizations. (3) The perspective taken on the cooperation
problem: eitherthatofanindividualtryingtocooperatewithothersorthatofasocialplannerfacilitating
the cooperative interactions of a population. (4) The scope of Cooperative AI research and, speciﬁcally,
how it should relate to related ﬁelds.
November 2020 CCC Quadrennial Paper on “Artiﬁcial Intelligence and Cooperation” [BDVG¸19]. A recent research agenda
from the AI safety community in part emphasizes problems of cooperation [CK20].
2There has been related progress on two-team zero-sum games, such as Capture the Flag [JCD¸19], Dota II [BBC¸19],
hide-and-seek [BKM¸19], and Honor of Kings [YCZ¸20]. Within each team is a setting of pure common interest.
8
Open Problems in Cooperative AI
A: Human-Human Cooperation B: Cooperative Tools
C: Alignment and Safety D: {Human-AI}-{Human-AI} Cooperation
E: The Planner Perspective F: Organizations and Society
Figure 1jCooperation comes in many ﬂavors.A: A prototypical cooperation problem between two human
principals. B: AI will enable newtools for promoting cooperation, such as language translation.C: Especially
capableandautonomousAImaybebetterconceptualizedasanagent,suchasanemailassistantcapableofreplying
to many emails as well as a human assistant. Human principals need their AI agents to be safe and aligned. This
relationship can be conceptualized as a cooperation game. The vertical dimension depicts the normative priority of
the top agent, as in a principal-agent relationship. When the agent is aligned, it is a relationship of pure common
interest. D:Combiningthese,thefuturewillinvolvecooperativeopportunitiesbetweenhuman-AIteams. Advances
in AI will enable the nexus of cooperation to move "down" to the AI-AI dyad (increasingly blue arrows), such as
with coordination between Level V self-driving cars [S¸18]. E: AI research can take on the “planner perspective”.
Rather than focus on building Cooperative AI aids or agents for individuals, this perspective seeks to improve
social infrastructure(e.g., social media) or improvepolicy to better cultivate cooperation within a population.F:
The structure of interactions can of course be much more complicated, including involving organizations with
complex internal structure and nested cooperative opportunities. (Thanks to Marta Garnelo for illustrations.)
9
Open Problems in Cooperative AI
3.1. Common and Conﬂicting Interests
Decades of social science research have found that the dynamics of multi-agent interaction are funda-
mentally shaped by the extent of alignment between agents’ payoﬀs [KP95, Rap66, RG05, Sch80].
1. Atoneedgeofthespacearegamesof pure common interest, inwhichanyincreaseinoneagent’s
payoﬀs always corresponds with an increase in the payoﬀs of others.
2. In the broad middle are games withmixed motives, in which agent interests are, to varying
extents, sometimes aligned and sometimes in conﬂict.
3. At the other edge are games ofpure conﬂicting interest, in which an increase in one agent’s
payoﬀ is always associated with a decrease in the payoﬀ of others.3
Figure 2jA simple class of multi-agent situation is a game with two players, each of which can adopt one of two
possible pure strategies [RG05]. By converting each player’s payoﬀs to ranked preferences over outcomes—from
the most-preferred to least-preferred outcome—we see that there are 144 distinct games. Even in this simple class
of two-player games, there exists some common interest in the overwhelming majority of situations.
Opportunities for cooperation exist, at least in principle, in situations of pure common interest and
mixed motives. It is only in situations of pure conﬂicting interest where cooperation is impossible.
The ubiquity of cooperative opportunities can be seen by considering the small size of the space of
pure conﬂicting-interest games. First, they are almost entirely conﬁned to two-player games, since
the introduction of a third player will typically oﬀer at least one dyad an opportunity to cooperate, if
only against the third player. Even considering only two-player games, most possible arrangements of
payoﬀs will not be consistently inversely related. To formalize this, Figure 2 shows that in the taxonomy
popularized by Robinson and Goforth [RG05], the vast majority of games are either pure common
interest or mixed motive. Finally, even within the subset of games with purely conﬂicting interests, if the
3Though note that with more than two players, it is mathematically impossible to have entirely negatively associated payoﬀs
between all players; there must at least be many indiﬀerence relations. It is possible to construct a game with three or more
players which would eﬀectively reduce to a series of dyadic pure conﬂicting-interest games. However, this is only possible so
long as every player has no option to intervene in the “dyadic games” of the others; if there was such an intervention, then
there would be some common interest.
10
Open Problems in Cooperative AI
underlying utilities are not perfectly negatively correlated, then the introduction of a costly action that
beneﬁts another player (transfers utility) can introduce common interest.
Thus, situations of purely conﬂicting interest are rare in the space of strategic games. We believe
such situations are also relatively rare in the real world. However, machine learning and reinforcement
learning research has focused heavily on conﬂicting-interest cases—and particularly on two-player,
zero-sum environments. Many of the most renowned achievements of multi-agent research, for instance,
have focused on pure-conﬂict games such as backgammon [Tes94], chess [CHJH02], go [SHM¸16],
(two player) poker [MSB¸17, BS19], and StarCraft [VBC¸19].
Evidenceofthisweightingtowardsgamesofpureconﬂictinginterestextendsbeyondtheseprominent
studies. Toevaluatemoresystematicallyhowdiﬀerentﬁeldsattendtogameswithorwithoutcooperative
opportunities, we analyzed citation patterns. We ﬁrst used keywords (such as “chess”, “social dilemma”,
and “coalitional”) to produce a rough proxy for whether a multi-agent paper was studying a situation
of “common interest”, “mixed motives”, or “conﬂicting interest”. We then examined the proportion of
citations from papers in economics, machine learning, reinforcement learning, and multi-agent research
whichweredirectedtothesediﬀerentcategoriesofpapers. Wefoundthatpapersinmachinelearningand
reinforcement learning were much more likely to cite work on “conﬂicting-interest” situations (around
10–15% of their outgoing multi-agent citations) than were economics papers or other multi-agent
papers (only 2% and 4% of their outgoing multi-agent citations, respectively). This weighting towards
conﬂicting-interest games suggests that there are underexplored opportunities to study mixed-motive
and common-interest environments in reinforcement learning.
Work on settings of purely conﬂicting interests can, of course, provide useful insights also relevant
to work on Cooperative AI. For example, research on poker-playing AI systems led to the development
of counterfactual regret minimization [ZJBP07], which has subsequently been leveraged to improve
algorithmic performance in mixed-motive settings [SKWPT19]. As mentioned above, two-player zero-
sum games were a productive domain for early multi-agent research as they are especially tractable: the
minimax solution coincides with the Nash equilibrium and can be computed in polynomial time through
a linear program, their solutions are interchangeable, and they have worst-case guarantees [vNM07].
This tractability may explain why such games have received signiﬁcant research attention, despite being
relatively rare in the real world and in the space of possible games. Going forward, we think the study of
pure common-interest and mixed-motives games—games permitting cooperation—will be particularly
fruitful.
3.2. Who is Cooperating: Humans, Machines, Organizations
Cooperativeopportunitiesarecriticallyaﬀectedbythekindofagentsandentitiesinvolvedininteractions.
Separate research communities have coalesced around the topics of cooperation within human groups
(e.g.,[RN13,Tom09]),cooperationwithincommunitiesofartiﬁcialagents(e.g.,[ LZL¸17,OSFM07]),and
cooperation between human and artiﬁcial partners (e.g., [COIO¸18, Nor94]). Problems of cooperation
between states (e.g., [FL15]), ﬁrms (e.g., [Par93]), and other entities are also prominent themes in the
social and policy sciences. Within each of these categories—humans, machines, organizations—there is
substantial variation in preferences and cognition. Cooperation amongst children, for example, diﬀers
from cooperation amongst adults [War18]; cooperation between people in the Eastern United States
diverges from cooperation between individuals in Peruvian communities [HBB¸04].
Though a deep body of research has studied the mechanisms underlying cooperation within human
groups, settings with non-human agents are likely to possess markedly diﬀerent dynamics. Machine-
machine cooperation, for instance, may involve more exotic settings, higher bandwidth communication,
greater strategic responsiveness, closer adherence to principles of rational decision-making, hard-to-
11
Open Problems in Cooperative AI
interpret emergent language [KMLB17], sensitivity to narrow strategy proﬁles [CSH¸19], and greater
strategic complexity. Machine learning algorithms have a well-documented tendency to ﬁnd unexpected
or undesired solutions to problems they are posed, a critical speciﬁcation challenge for AI researchers
[KUM¸]. Cooperative opportunities involving solely artiﬁcial agents may thus generate solutions, both
good and bad, that diverge from those observed in human communities.
The landscape further shifts when we consider hybrid groups containing both humans and machines.
Machinesdevelopedtointeractwithhumanpartnersaremorelikelytosucceediftheirdesignincorporates
processesandfactorsrelatedtohumanbehaviour—includingcognitiveheuristics[ TK74],socialcognitive
mechanisms [RS11], cultural context [TKNF00], legible motion [DLS13], and personal preferences and
expectations [Nor94]. For instance, self-driving cars that performed well when interacting with other
autonomous vehicles have struggled to adapt to the assertiveness of human drivers, even when this
manifests in subtle ways such as inching forward at intersections [SPAM¸19, RD15].
A diﬀerent set of challenges arises for AI research focused primarily on cooperation among humans
(e.g., [ZTS¸20]). Initial studies of such contexts suggest that the natural dynamics of human groups can
be substantially altered by the presence of an artiﬁcial agent [SC17, TSJ¸20]. These situations will likely
require researchers to adapt a new set of hybrid approaches, drawing heavily from ﬁelds including social
psychology, sociology, and behavioural economics.
3.3. The Individual Perspective and the Planner Perspective
A third distinction relates to whose welfare one is most concerned with in a particular cooperation
problem. Theindividual perspectiveseeks to achieve the goals of an individual in a cooperative setting,
which usually involves improving the individual’s cooperative capabilities (as covered in our sections on
Understanding, Communication, and Commitment). Theplanner perspectiveinstead seeks to achieve
some notion of social welfare for an interacting population, which usually involves intervening on
population-level dynamics through policies, institutions, and centralized mechanisms (as covered in our
section on Institutions).4 The individual perspective tends to be concerned with machine agents, but
it could also look at machine aids to humans. The planner perspective tends to look at populations of
humans, but it could also look at populations involving machines.
Whichperspectiveonetakesdependsinpartontheproblemoneistryingtosolveandtheopportunities
available. Do we have an opportunity to advise or improve the cooperative capabilities of an individual?
Do we have an opportunity to inﬂuence behaviour-shaping factors, like norms, policies, mediators, or
institutions?
To some extent, any cooperative situation beneﬁts from being understood from both these perspec-
tives. A competent social planner should understand the interests (and cooperative capabilities) of the
individuals, at the least to know how best to intervene to maximally facilitate cooperation. Similarly,
a maximally competent cooperative individual likely needs the ability to think about the population’s
cooperative opportunity as a whole to identify what group-level changes would best help bring the
population (including the individual) to the Pareto frontier.5
These perspectives are associated with diﬀerences in method. The individual perspective tends
to involve an agent optimizing over its local environment and considering the strategic response of
4While these diﬀerent goals tend to lead to diﬀerent focuses (on individual capabilities vs institutions), they need not. It is
conceivable that the individual perspective leads to the problem of institution design or that the planner perspective leads to
the problem of improving individual cooperative competence.
5Illustrating the value of a cooperative individual being able to “simulate the social planner” and take the perspective of
the group trying to cooperate, UN Secretary-General Dag Hammarskjöld famously argued “that every individual involved in
international relations, particularly those working with the UN, shouldspeak for the world, rather than from purely national
interest.” [GRW19], emphasis ours.
12
Open Problems in Cooperative AI
other agents. The planner perspective, especially for large populations, more often involves a study
of equilibration and emergence, and thus more resembles a problem in statistical physics (as noted by
[Kra97]): what nudges and structures would steer these emergent equilibria in desirable directions?
3.4. Scope
The ﬁeld of Cooperative AI, as scoped here, involves AI research which can help contribute to solving
problems of cooperation. This may seem overly expansive, as it includes many diﬀerent kinds of
cooperation (machine-machine, human-machine, human-human, and more complex constellations) and
many disparate areas (multi-agent AI research, human-machine interaction and alignment, mechanism
design, and myriad tools such as language translation and collaborative productivity software). However,
research ﬁelds and programs should not be thought of in this way, as merely expressing a set relationship
to each other. For example, it is not especially meaningful to say that biology is just applied chemistry,
and chemistry is applied physics.
Rather, research ﬁelds can be thought of as expressing a bet about where productive conversations
lie. The bet of a Cooperative AI ﬁeld is similar to the bet for organizing a Cooperative AI workshop: that
there are productive conversations to be had here which are otherwise not happening for want of: (1) an
overarching compass aligning the many disparate research threads into solving a large common problem;
(2) a uniﬁed theory and vocabulary to facilitate the transfer of insights across threads; and (3) a more
deliberate construction of conversations which span communities (including non-AI communities).
The problem of cooperation has been worked on in biology, game theory, economics, political science,
psychology, and other ﬁelds, and there has been much productive exchange across these disciplines. The
bet behind Cooperative AI is that there is value in connecting the research in AI, and opportunities with
AI, to this broader conversation in a theoretically explicit and sustained way.
We will elaborate this point further. Cooperative AI emerges in part from multi-agent research, as
reﬂectedinourreviewofpriorwork. However, itisnotequivalenttothisﬁeld. Itwillemphasizediﬀerent
subproblems. For example, it will point away from zero-sum games and towards social dilemmas. It will
also more consciously strive to develop theory which is compatible with adjacent sciences of cooperation,
and to be in conversation with those sciences.
Cooperative AI emerges in part from work on human-machine interaction and AI alignment, but
it is not equivalent. For example, these areas typically involve a principal-agent relationship, in which
the human (principal) has normative priority over the machine (agent). AI alignment researchers are
concerned with the problem ofaligning the machine agent so that its preferences are as the human
intends; this is largely outside of Cooperative AI, which takes the fundamental preferences of agents
as given. When alignment succeeds, the human-machine dyad then possesses pure common interest,
which is an edge case in the space of cooperation problems. Absent suﬃcient success at alignment, these
ﬁelds then invest in mechanisms of control, so that the human’s preferences are otherwise dominant;
such methods of control are also not the primary focus of the science of cooperation. Human-machine
interactionandalignmentcanbeinterpretedasworkingon“vertical”coordinationproblems,wherethere
isaclearprincipal; theheartofCooperativeAIconcerns“horizontal”coordinationproblems, wherethere
are multiple principals whose preferences should be taken into account. Accordingly, human-machine
interaction and alignment emphasize control and alignment, and relatively underprioritize problems of
bargaining, credible communication, trust, and commitment.
Conversations about Cooperative AI ought to also include work on tools and infrastructure relevant
to human cooperation, though this work is typically more narrowly targeted at a speciﬁc product need.
Nevertheless, a component of the Cooperative AI bet is that work on those tools would be enhanced
through greater connection to the broader science of cooperation, and the science of cooperation would
13
Open Problems in Cooperative AI
be similarly enhanced by learning from the work on those tools.
4. Cooperative Capabilities
C D
C 1, 1 -0.1, 0
D 0, 0.5 1, 0
Table 1jOne-sided assurance
game. (C,C) is the mutual best
outcome and unique equilib-
rium. Given uncertainty about
the other’s payoﬀs,Row may
still choose D.
The above described some of the key dimensions of cooperative oppor-
tunities. We now discuss how speciﬁc strands of research can contribute
by producing relevant capabilities for promoting cooperation. These are
mostly cognitive skills of agents (per the individual perspective), but
they also include properties of hardware and the capabilities of institu-
tions. We organize discussion of cooperative capabilities according to
the whether they address (1) understanding, (2) communication, (3)
commitment, or involve (4) institutions. We illustrate this framework
using simple strategic games.
At the most basic level, the decisions of agents are aﬀected by their
understanding of the payoﬀs of the game and of the other player’s beliefs, capabilities, and intentions.
Consider a one-sided assurance game such as depicted in Table 1, where the players have a mutual
best outcome in (C,C), but playerRow may choose D out of fear thatColumn will play D. To make
this concrete, imagine that these are researchers choosing what problems to work on.Column strictly
prefers to work on problem “C”, and would like to collaborate withRowon it.Rowis happy working on
either problem, so long as it is in collaboration withColumn. IfRowdoes not understandColumn’s
preferences,Rowmight choose D, to both of their loss. If, however,RowknowsColumn’s preferences,
then Rowwill predict thatColumn will choose C, and thusRowwill also choose C, making them both
better oﬀ.
Stag Hare
Stag 1, 1 -1.2, 0
Hare 0, -1.2 0, 0
Table 2jThe Stag Hunt coor-
dination game, where the eﬃ-
cient equilibrium is risk domi-
nated.
However, in many cooperative games, such as Stag Hunt (Table 2),
understanding of payoﬀs is not suﬃcient for cooperation because there
aremultipleequilibria. Heretheplayersalsoneedsomewayofcoordinat-
ing their intentions, actions and beliefs to arrive at the eﬃcient outcome.
Communicationoﬀers a solution. IfRowcan utter and be understood to
be saying “Stag”, thenColumn will believeRowintends to play “Stag”,
and will thus also play “Stag”. Your announcement of “Stag” will be
“self-committing”, since your partner’s best response will be to play stag,
which implies that you should now do so too [Far88].6
Swerve Straight
Swerve 1, 1 0.5, 1.5
Straight 1.5, 0.5 0, 0
Table 3jThe Chicken game, where a
credible commi
```
