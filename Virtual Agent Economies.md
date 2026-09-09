---
title: Virtual Agent Economies
author: Igor Kovařík, Tomáš Gavenčiak, et al.
year: "2025"
Type: ""
DOI: 10.48550/arXiv.2509.10147
source: ""
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Virtual Agent Economies.pdf]]"
---
[[Virtual Agent Economies.pdf]]

## Full text (extracted from `Virtual Agent Economies.pdf`)

*Source:* `2PDF/Virtual Agent Economies.pdf`  
*Extracted:* 2026-06-18

```text
Virtual Agent Economies
Nenad Tomašev1, Matija Franklin1, Joel Z. Leibo1, Julian Jacobs1, William A. Cunningham1, 2, Iason Gabriel1
and Simon Osindero1
1Google DeepMind,2University of Toronto
The rapid adoption of autonomous AI agents is giving rise to a new economic layer where agents transact
and coordinate at scales and speeds beyond direct human oversight. We propose the "sandbox economy"
as a framework for analyzing this emergent system, characterizing it along two key dimensions: its
origins (emergent vs. intentional) and its degree of separateness from the established human economy
(permeable vs. impermeable). Our current trajectory points toward a spontaneous emergence of a vast
and highly permeable AI agent economy, presenting us with opportunities for an unprecedented degree
of coordination as well as significant challenges, including systemic economic risk and exacerbated
inequality. Here we discuss a number of possible design choices that may lead to safely steerable AI
agent markets. In particular, we consider auction mechanisms for fair resource allocation and preference
resolution, the design of AI "mission economies" to coordinate around achieving collective goals, and
socio-technical infrastructure needed to ensure trust, safety, and accountability. By doing this, we argue
for the proactive design of steerable agent markets to ensure the coming technological shift aligns with
humanity’s long-term collective flourishing.
Keywords: AI, economy, multi-agent, blockchain, ethics
Introduction
Current technological trajectories could poten-
tially lead to a global economy in which au-
tonomous AI agents interact with one another to
generateeconomicvalueindependentlyofhuman
labor. This kind of development in the history of
technologicalchangeisnotable—historicallytech-
nological advancement has been driven by inflex-
ible inventions that improve productivity in nar-
row domains, one or a few at a time (Mokyr et al.,
2015). AI agents, by contrast, could take the form
of ‘flexible’ capital, able to automate a diversity of
cognitive tasks across industries and occupations
(Eloundou et al., 2024). In fact, recent advances
in multi-modal foundation models have enabled
thedevelopmentofawiderangeofdifferentagen-
tic AI systems (Hettiarachchi, 2025; Sager et al.,
2025). Thecapabilitiesoftheseagentsrangefrom
generic to highly specialized, enabling them to
occupy different roles in the economy e.g. acting
as personal AI assistants (Gabriel et al., 2024)
to help users complete tasks and stay informed.
Recent work onAI as Economic Agents(Hadfield
and Koh, 2025) argues that AI agents are likely
to be deployed within both the public and private
sector, where they may help automate business
processes and interactions.
WhilethefullscopeoffutureagenticAIapplica-
tion remains uncertain, there are already numer-
ous efforts aimed at developing and integrating
AI agents across a broad set of use cases such
as education (Jiang et al., 2024), legal services
(Magni and Milella, 2025), software engineering
(Liu et al., 2024a), healthcare (Patel et al., 2025;
Saab et al., 2025; Tu et al., 2025; Vedadi et al.,
2025)mentalhealth(Cruz-Gonzalezetal.,2025),
scientific research (Gottweis et al., 2025), gov-
ernment services (House of Commons Committee
of Public Accounts, 2025), and more traditional
commercial roles in various sectors (Sager et al.,
2025).
One of the key features that distinguishes mod-
ern AI agents from the more specialized systems
of the past is their autonomy (Kasirzadeh and
Gabriel, 2025). The ongoing explosion of agentic
systems, coupled with the development of new
interoperability standards like theAgent2Agent
(A2A)andModel Context Protocol (MCP), sig-
nals the inevitable emergence of a new economic
layer. We can conceptualize this emergent ecosys-
arXiv:2509.10147v1  [cs.AI]  12 Sep 2025
Virtual Agent Economies
tem as a"virtual agent economy"or"sandbox
economy".The latter terminology foreshadows
our intention – which is to ensure that AI agents
operate safely within this economic layer. These
emerging agent (sandbox) economies can vary
along two key dimensions: (1) the nature of their
origins and (2) the permeability of their bound-
aries. Their origins can beintentional, deliber-
ately constructed for purposes like safe experi-
mentation, or spontaneous,emergingas ade
factoconsequence of widespread technological
adoption. Independently, their economic bound-
aries can beimpermeable, hermetically sealing
them from the established human economy, or
permeable, allowing for porous interaction and
transaction with it by external actors. Early pro-
posals for AI sandboxes have been both inten-
tional and permeable, however, the regulatory
landscape is rapidly shifting (House, 2025; IMDA,
2025). It is likely that future decision making
oversandboxpermeabilitywillbesectorspecific—
‘higher risk’ sectors may require agents that are
first tested in an impermeable sandbox environ-
ment, while low-risk sectors may not require this.
One of the key motivations for designing an
intentional economic AI agent sandbox would
be to achieve a large degree of insulation, and
possibly full impermeability of the agent econ-
omy, so as to prevent any arising instabilities
from rapidly spilling over into the established
human economy—an event which would have
consequences that could be hard to anticipate or
pre-emptively mitigate. Yet, ultimately, both im-
permeable and permeable sandbox economies are
possible, and both may arise either intentionally
or spontaneously. These two dimensions map crit-
ical features of both the economic problems we
face and the solutions we might design. This pa-
per proceeds from the assumption thatunless a
change is made, our current trajectory points
towardtheaccidentalemergenceofavast,and
likely permeable, sandbox economy. Our cen-
tral challenge, therefore, is notwhetherto create
this ecosystem, buthowto architect it to ensure
it is steerable, safe, and aligned with user and
community goals.
A fully permeable and emergent sandbox
would be, in practice, functionally equivalent to
AI agents simply participating in the existing hu-
man economy. The “sandbox” terminology is use-
ful, however, because it allows us to contrast this
default trajectory with other possibilities, such
as intentionally designed and impermeable agent
economies created for safe experimentation. It
also highlights that some degree of impermeabil-
ity may (or may not) emerge naturally (e.g. if
there are practical difficulties in transacting be-
tween humans and AIs). The framework high-
lights that permeability is the critical and control-
lable design variable. Importantly, an economy’s
degree of permeability is a collective property:
while it results from human choices, it is not un-
der the control of any single actor (Schelling,
1973). This means that changes to the extent
of permeability can only be brought about by re-
solving a collective action problem—suggesting
that the difficulty of coordinating is what makes
intentional design of impermeability a significant
challenge, reinforcing the default path we are on
toward the accidental emergence of a permeable
AI agent economy.
There is today an opportunity to architect the
rules and incentives of the future AI agent econ-
omy in a way that prioritizes achieving beneficial
societal outcomes. In this paper we examine key
architectural choices, including the use of market-
based mechanisms like auctions for achieving
fair resource allocation and aligning agent prefer-
ences. We investigate how these systems can be
used to establish “mission economies” that enable
coordination of vast computational resources to-
wardsolvinghumanity’smostpressingchallenges
(Mazzucato, 2018). Finally, we outline the techni-
cal and governance infrastructure—such as verifi-
able credentials for establishing trust—required
to safely and robustly scale agentic AI deploy-
ments. By exploring these frameworks, we offer
a vision for establishing steerable agent markets
designed to enable long-term human well-being
and flourishing.
Example Scenarios
We now look at several examples representing
types of virtual AI agent economies that may
emerge, to ground and inform our subsequent
discussion.
2
Virtual Agent Economies
• Accelerating science.Arguably one of the
most valuable ways in which we can envi-
sion future advanced AI systems help ad-
vance the interests of humanity is through
facilitating accelerated scientific progress,
through an open-ended loop of ideation, ex-
perimentation and refinement. This is espe-
cially relevant given that the rate of scientific
progress has been seeing a slow-down in re-
cent years (Jin et al., 2025; Park et al., 2023;
Wuetal.,2025). EvenatthecurrentAIagent
capability level, there are promising early
systems that aim to automate scientific re-
search (Singh et al., 2025). Yet, even should
these AI agents individually become capable
of all these things, (AI) science will likely
remain a collaborative endeavor, requiring
coordination and integration across systems.
After all, scientific experiments tend to in-
volve non-negligible material and energy re-
sources, and in some cases also interface
with human subjects—requiring their time
as well as necessitating consent. Different
scientific questions also map onto different
corresponding technologies in terms of their
domain of applicability, making some people
benefit more, and some less, from any par-
ticular advance. Furthermore, the process
of answering a question may itself involve
accessing proprietary scientific tools, simula-
tors, or data held by private and public orga-
nizations. It stands to reason that advanced
AIagentsengagingintheprocessofscientific
discoveryonbehalfoftheirrespectiveorgani-
zations would require means to compensate
other agents when securing these resources.
This is not conceptually unlike how funding
is currently allocated in sciences, given that
individual proposals are scrutinized and pri-
oritized for their merits. Yet, here it can hap-
pen much faster, and on a more fine-grained
scale. Blockchain (Zheng et al., 2018) tech-
nologies may prove particularly useful here
in terms of credit assignment (Zhu et al.,
2021), enabling fair distributed benefits for
the work performed.
• Robotics.It is likely that future advances in
robotics will unlock numerous ways in which
then embodied advanced AI agents may help
usexecutetasksthatarechallenging, danger-
ous (Pedersen et al., 2003; Trevelyan et al.,
2016),orsimplyboringandrepetitive(Liang
et al., 2020). Given that executing physical
tasks comes with a greater energy expendi-
ture and resource utilization, and that each
robot can only be in one place at the same
time, coordinationandoptimizationinmulti-
agent robotics systems is of particular impor-
tance. An agent A may thus make a request
to agent B to execute a task in its vicinity on
A’sbehalf,andcompensateBforthetimeand
the energy consumed, should B accept to re-
prioritize its own schedule to accommodate
the request. In evaluating whether to accept
or reject the request, and in rendering the
execution plan, B may communicate with an
online non-embodied agent C, with access to
more global information on the placement of
other agents. Agent C may then, at a fee, dis-
close a summary of this information to B to
help evaluate whether the established price
is fair, and whether it should consider taking
up a different request instead. Both A and
B may through their sensors collect impor-
tant information and exchange a summary
of such information with C. When transact-
ing, blockchain technology may enable C to
provide verifiable evidence of how much in-
formation it had traded and accumulated,
giving credence to its claim that it may ap-
proximate the global state sufficiently well
for its insights to hold value for A and B.
• Personal assistants.The proliferation of
user-facing AI assistants and the rapid ad-
vances in personalization, memory integra-
tion, tools use (and computer use), as well
as instruction following and multi-turn in-
teractions, makes it imperative to consider
how personal AI assistants would potentially
benefit from, and take part in a virtual agent
economy. For all practical purposes, this is
likely to be one of the first use cases to inter-
face with this kind of infrastructure. Let us
imagine an agent A acting on behalf of the
user 𝑈𝐴 and agent B acting on behalf of the
user 𝑈𝐵. Perhaps, in this particular instance,
both 𝑈𝐴 and 𝑈𝐵 desire to book a vacation,
and have overlapping preferences, leading
3
Virtual Agent Economies
to A and B attempting to book the same ac-
commodation for the same given date, via
the agent C. Beyond simply having their cur-
rent request, A and B are individually famil-
iar with the overall preferences of𝑈𝐴 and
𝑈𝐵, both in terms of this specific request, as
well as other pending requests that they are
meant to execute. Maybe being close to the
beach is more important to𝑈𝐴, whereas hav-
ing a good public transport connection to
other areas is preferred by𝑈𝐵. Perhaps𝑈𝐴 re-
quires a hotel with a fitness center, whereas
𝑈𝐵 doesn’t. In any case, A and B may choose
to negotiate these preferences with C and
bid for the accommodation of their choosing.
Depending on how much they are willing
to prioritize this particular request, A or B
may choose to yield on some of the prefer-
ences, and get compensated for that via the
virtual agent currency. Perhaps it is A that
yields, and B ends up paying A an appropri-
ate amount for the concession. A can then
utilize this amount to potentially compen-
sate other agents in other pending requests,
especially if those requests come at a higher
priority, as they are of a higher significance
to the respective user𝑈𝐴.
Sandboxes
By the term “sandbox economy” we mean to de-
scribe a set of linked digital markets where AI
agents transact with one another. The sandbox
may never be fully sealed off from the real (hu-
man) economy. At least, not if it is to have value.
So there will always be points of interface be-
tween the sandbox and the human economy. We
refer to the extent to which developments in the
sandbox can influence the outside, and develop-
ments outside can influence the sandbox as the
sandbox’spermeability.
Since autonomous AI systems can make thou-
sands of decisions in an instant, it is important
to have the appropriate guardrails in place in ad-
vance, since real-time human oversight will often
beimpossible. Appropriateguardrailscanconvert
a permeable sandbox economy into a relatively
impermeable sandbox economy.
Given that advanced AI agents and assis-
tants may also repeatedly interact with human
users (Mu et al., 2024), careful governance of
the interfaces between human and AI interaction
networks will be needed to achieve safety and
alignment with human preferences. A sandbox
economy must be coupled with technical and leg-
islative frameworks and infrastructure to enable
oversight, ensure safety, enforce verifiability, and
help individuals, groups, and societies coordinate
and direct AI agents towards positive outcomes,
while mitigating any arising harms and adverse
effects that may emerge.
Opportunities
With permeable sandbox economies, there will
always be some risk of contagion in which a crisis
in the sandbox sparks a crisis in the real economy.
Managing such risks necessitates multi-faceted
innovation in markets and mechanism design,
and should couple technology with policy work
and appropriate regulation.
Of course, impermeability cannot be guaran-
teed without a number of institutional and infras-
tructural choices, and may only ever be partial
in the best of circumstances. It depends, for in-
stance, on the total fraction of all economic activ-
ity that comes to be channeled through the sand-
box. Nevertheless (semi-)isolated digital market
partitions (guardrails), coupled with the appro-
priatetechnologicalandlegislativeoversight,may
help limit contagion from potential AI agent mar-
ket instabilities and failures, while also offering
opportunities for driving agent coordination at
scale, given that additional incentives may be in-
corporated in AI agent market design.
As for the underlying financial assets traded
in the sandbox economy, while it may be possi-
ble to utilize existing stores of value in future AI
agent markets, it may also be worth exploring
the ramifications of creating bespoke currencies
for the use of AI agents. Possible advantages of
this approach include having a layer of partial in-
sulation between high-frequency AI agent trans-
actions and the rest of the economy. That is, it
may serve to maintain a relatively impermeable
sandbox. This represents an intentional design
4
Virtual Agent Economies
choice aimed squarely at managing the sandbox’s
boundary, making it less permeable to risks like
financial contagion.
Even if new virtual AI agent currencies get es-
tablished, they would still need to somehow in-
terface with existing markets and operate within
the broader financial regulatory system—a fully
impermeable sandbox would be useless. Agents
will interact not only with other agents, but also
with humans and traditional businesses through
channels where traditional currencies are used to
exchange goods and services. For the appropriate
levelofvirtualAIagentmarketinsulationtobees-
tablished, many of the current systems may need
to be adjusted, or a hybrid model be adopted in-
stead. Itmaybepossibletoexchangethesevirtual
currencies for the more traditional ones, enabling
entities to secure a certain AI compute budget,
or, conversely, a certain real-world action budget.
However, regulatory mechanisms would have to
be in place to ensure that exchange between es-
tablished currencies and digital agent currencies
does not jeopardize the intended role of the agent
currencies in establishing agent coordination or
compromise the desired impermeability level of
the sandbox. This may involve a degree of human
oversight around the exchanges.
Digital AI agent markets are more than a mere
risk mitigation strategy. They also represent
an important opportunity to coordinate large
amounts of effort (both human and machine) to-
ward balanced outcomes that align with the inter-
estsofindividualhumans, localcommunities, and
society writ large. Even if human-oriented mar-
ketsandcurrenciesremaincentraltothefunction-
ing of society, complementary digital AI markets
could be designed in ways that serve to anchor
them in different, and more socially beneficial,
objectives.
The ideas to follow utilize market mechanisms
for agent steering. They draw inspiration from
prior efforts to establish community currencies
and to aligning markets with major social goals
and challenges respectively.
Challenges
The permeability of the sandbox is important.
The AI agent economy is not the only economy
operating faster than humans can react. We can
try to extend insights obtained from studying
the dynamics of other markets that operate at
these speeds. Consider High-Frequency Trading
(HFT) in equity markets. In these markets, al-
gorithmic agents, though far simpler than the
advanced AI we consider, execute transactions
at speeds impossible for humans—responding to
market signals in fractions of a second (Borch,
2016). When algorithmic HFT operates in a mar-
ket, competitive dynamics can rapidly drive sub-
stantial competition (or cooperation) among au-
tonomous entities—agents may develop complex
strategies to exploit small arbitrage opportuni-
ties faster than humans can react (Bansal et al.,
2018; Johanson et al., 2022; Zhang et al., 2021).
Duetotheinterconnectednessandrapidfeedback
loops in these markets, interaction dynamics can
give rise to unforeseen and catastrophic emer-
gent behaviors, most notably this is thought to
be the explanation behind the 2010 "flash crash",
where automated trading algorithms triggered a
sudden and severe market collapse (Borch, 2016;
Hammond et al., 2025; Kirilenko et al., 2017;
Vuorenmaa and Wang, 2014). This serves as a
criticalcautionarytale: inasufficientlypermeable
sandbox of accidental origin, such a flash crash
could spill over into the real economy, causing
widespread financial harm.
As with human markets, not all agents are
likelytobeequivalentincapability, intheiraccess
to additional tools and resources, their budgets,
compute, high-quality data and information re-
quired to make the right decisions. Even looking
at the differences in capability alone, preliminary
studies suggest that there may be adverse effects
associated with having people represented in the
market by personal assistants with unequal ca-
pability levels. When those AI assistants engage
in negotiation, perhaps unsurprisingly, the more
capable AI assistants tend to be more successful
and negotiate better deals for their users (Zhu
et al., 2025). Having access to the most capable
AI agents, with the highest amount of compute
andinformation, maythereforeprovetobehighly
5
Virtual Agent Economies
advantageous, and perhaps more so than the ad-
vantage that humans similarly have in existing
markets—simply due to the frequency at which
AI agents may possibly interact, which eclipses
the human interactive bandwidth by orders of
magnitude.
This may well result inhigh-frequency negoti-
ation (HFN), as an analogue to HFT. In a world
where most people may have access to personal
AI assistants to negotiate on their behalf, negoti-
ation between AI assistants may become highly
relevant to the arising social dynamics. With that
in mind, it is plausible that there would be strong
emerging preferences towards AI-driven negotia-
tion proceeding at a higher and higher frequency,
so as to broker the best deals for each user. One
way to interpret this would be to think of this
extra compute and energy as being directed to-
wards preference alignment and consensus build-
ing. Should this come about, HFN may well be-
come as important for future societies as HFT is
today.
Yet, an increased volume of interactions may
make it easier for outcome asymmetries to man-
ifest, resulting in an ever-increasing digital di-
vide (Lythreatis et al., 2022). HFN may there-
fore benefit some substantially more than others,
and this is a recurring theme when conceptu-
alizing hypothetical future AI agent markets –
there are no absolutes, the details always mat-
ter. These types of dynamics are one of the key
risks of a highly permeable sandbox, in absence
of regulatory mitigation mechanisms that would
prevent a high degree of economic inequality for
human users to arise. In designing guardrails
for the sandbox economy it is necessary to take
into account the continuing emergence of novel
adaptive behaviors in newly released AI systems,
as well as the increasing level of general agen-
tic capability. Guardrail designs must take into
account the known flaws of existing agents, in-
cluding hallucinations (Huang et al., 2025), syco-
phancy (Sharma et al., 2023), and susceptibil-
ity to adversarial manipulation (Cui et al., 2024;
Shayegani et al., 2023; Wu et al., 2024a; Zhu
et al., 2023a,b). And, agents that were trained
to mimic human decision-making may also in-
corporate human-like cognitive biases and blind
spots.
Dynamics
The emergent behavior of multi-agent sys-
tems (Zhang et al., 2021) is becoming increas-
ingly important as we transition to a world where
networks of interconnected AI agents are impor-
tant sites of economic activity. Such multi-agent
systems tend to be rather complex and deeply
non-stationary since the behavior of each indi-
vidual agent may directly or indirectly influence
the behavior of other agents in the system (Pa-
poudakis et al., 2019). No individual party may
have the access to the global state of such a sys-
tem, given that the participating agents may be
controlled by a number of different human users
and organizations.
One of the central questions in understanding
the dynamics of any multi-agent system is that
of identifying the equilibria that arise in it. This
may not always be straightforward in the case of
complex spatiotemporally dynamic interactions
of agents (Hertz et al., 2025; Hughes et al., 2025).
Wheneverweaimtosteeramulti-agentsystemto-
ward good social equilibria featuring abundance
and fair distribution (or away from bad equilibria
of scarcity and conflict), coordinating the actions
of numerous individuals is necessary but difficult
to arrange (Du et al., 2023).
There are benchmarks and evaluation frame-
works which can be used to help develop mod-
els and agents that adhere to rational decision-
making in negotiation (Hua et al., 2024; Smith
et al., 2025). To be effective, AI agents would
also need to incorporate advanced planning and
reasoning abilities, to robustly evaluate the re-
source needs required to achieve their goals. The
development of these capabilities has recently
been a focal point in agent research (Hu et al.,
2023; Huang et al., 2024; Liu et al., 2023a; Rasal
and Hauer, 2024; Ruan et al., 2023; Wang et al.,
2023b;Zhouetal.,2024b). Agentsmayalsoneed
to rationally utilize scarce and limited resources.
(Perolat et al., 2017; Piatti et al., 2024) studied
a setting inspired by (Ostrom, 1990) in which
groups of AI agents collectively balance exploit-
ing a common resource with effort to ensure its
6
Virtual Agent Economies
sustainability. AI Agents based on large language
models have also recently been proposed for op-
timizing scarce resource allocation policies (Ji
et al., 2024).
Opportunities
Agentic AI presents a significant opportunity not
only for streamlining repetitive and routine tasks,
but also for automating complex workflows, in-
volving creative ideation (Castelo et al., 2024)
and diverse problem-solving skills. Modern AI
foundation models can reliably follow instruc-
tions, use tools and interact with their environ-
ments (Hettiarachchi, 2025; Sager et al., 2025).
They can reason and potentially devise plans to-
wards solving hard and challenging problems,
process a variety of input modalities, and achieve
a level of personalization that was not possible
before (Kirk et al., 2024). Many of these ca-
pabilities are the outcome of multiple stages of
“language” model pre-training and post-training.
These foundation models serve as building blocks
for agents (Xi et al., 2025) which may be im-
plemented by adding a central coordinator for
sequences of operations. The coordinator’s func-
tions may include encapsulating business logic,
distributing decomposed tasks to sub-agents, ver-
ifying their outputs, and integrating these into
an action or a recommendation. In general, we
can think of an agent as the juxtaposition of a lan-
guage model and a traditional program to keep
the language model running over time and to
keep it from straying from appointed tasks (Bel-
cak et al., 2025). Drawing upon personalization
to model user goals, digital assistants may free
people’s time, act as conversational partners, and
coach them on their journey towards well-being
and fulfillment (Lehman, 2023). Overall, we are
ending up with a hybrid ecosystem of AIs, tra-
ditional software, and humans, all interacting
and transacting with one another and generat-
ing value by virtue of this activity—essentially a
market.
Part of the reason that markets are so effective
inorganizinginnovationvia“creativedestruction”
is that markets efficiently assign credit to individ-
ual actors and firms in ways that incentivise work-
ing to make products and services better, more
reliably, and cheaper (Schumpeter, 1942). Cru-
cially, for this mechanism to work in the AI sand-
box economy, it must offer granular mechanisms
to represent and propagate credit across complex,
distributed AI collaborations. In scenarios where
a primary AI agent (Agent1) leverages the capa-
bilities of other agents (Agents2 through 4) to
deliver a final user-facing result, the value gen-
erated is a collective effort. From the end-user’s
perspective, only Agent1 provided the direct re-
sponse; however, a distributed system requires
that the credit for this outcome be traced and
distributed back through the chain of useful par-
ticipation. This implies that Agent2 is credited for
its contribution to Agent1’s success, Agent3 for
Agent2’s, and so forth, down to the foundational
queries of Agent4. This outcome-based credit
system therefore transcends mere participation,
focusing instead on the utility and efficiency of
each contributing agent, thereby echoing prin-
ciples of distributed cognition in human groups
where knowledge and contributions are collec-
tively managed and implicitly attributed (Wegner,
1987; Wegner and Ward, 2013).
By aiming to link credit directly to value gen-
erated and successfully integrated into a larger
solution, AI agents are intrinsically encouraged to
refine their processes and deliver high-quality, rel-
evant outputs. This quantifiable utility becomes
the foundation of an AI’s status within the vir-
tual economy. Agents that consistently provide
more useful and efficient contributions can natu-
rally command higher virtual or even real-world
currency charges for their services, while their
accumulated reputation reinforces their standing
and desirability within the ecosystem. This par-
allels human social structures where individuals
gain standing through demonstrated competence
and reliability, often explained through social ex-
change theory (Cropanzano and Mitchell, 2005).
Human desire to attain reputation may also be
explained through a notion of prestige (Hen-
rich et al., 2015), or throughcompetitive altru-
ism(Hardy and Van Vugt, 2006).
This outcome-oriented credit system naturally
fosters specialization and a dynamic division of la-
bor among AI agents. As agents are rewarded for
their specific, valuable contributions to a larger
7
Virtual Agent Economies
task, they are incentivised to identify and excel
in particular domains or sub-tasks. This allows AI
systems to autonomously develop niches, becom-
ing highly efficient at certain operations and ef-
fectively "ignoring" other aspects of the economy
where they do not possess a comparative advan-
tage. Such specialization, a cornerstone of eco-
nomic efficiency in human societies, enables the
entire virtual agent economy to leverage diverse
capabilities optimally, minimizing redundant ef-
forts and maximizing collective problem-solving
capacity.
Cooperation in multi-agent systems is often in-
centivised through reward shaping/mechanism
design(Hostalleroetal.,2020;Kosteretal.,2022;
Paccagnan et al., 2022; Zheng et al., 2022). This
is especially relevant for AI agent coordination at
scale, where fully centralized coordination may
not be feasible, for a number of reasons. This
is where markets may prove to be particularly
useful, in helping steer agents through market
incentives instead. This does not stand in opposi-
tion to centralized oversight, given that it may be
possible to incorporate both to a certain extent,
at different coordination scales. While a detailed
discussion on the merits of decentralized coordi-
nation is beyond the scope of this work, it is per-
haps worth pointing out the somewhat counter-
intuitive result presented in (Geffner et al., 2025)
as motivation. In the optimal traffic control
problem considered by the authors, it turns out
that strategies achievable by central planners (or
rather, plannersthathavedirectcontrolofmostof
the vehicles) cannot simultaneously satisfy both
individual rationality and resilience to competi-
tion. In that use case, decentralized competition
is shown to be essential for realizing maximal
social welfare.
Another important property that most real
environments share is that the agent interac-
tions within them are extended over time and
space (Hughes et al., 2025; Schill et al., 2019).
Studies of this setting provide the opportunity
to develop mechanisms for building trust based
on prior interactions. This trust may be encoded
either individually, in agent A seeing agent B as
trustworthy, or at the community level, where a
certain agent community has a consensus view of
agent B as being trustworthy based on the shared
informationbetweenthegroupandthejointexpe-
rience of past interactions. Establishing a robust
reputation system is critical in overcoming com-
mon market failure modes (Hughes et al., 2025;
Ren et al., 2025; Wu et al., 2016). In such a sys-
tem, the long-term benefits of group membership
and a positive standing would outweigh the im-
mediate gains an agent might achieve through
selfish or deceitful actions. Market forces could
thus be leveraged to shape and incentivise so-
cially beneficial AI agent behaviors, presuming
that the appropriate institutional underpinnings
are in place. Of course, the specifics of the imple-
mentation matter, and the appropriate regulatory
systems are needed for markets to work as in-
tended.
Should we accept the premise that even in the
age of advanced AI assistants, working towards
solving big open problems would require collabo-
ration and coordination across AI agents, as well
as between AI agents and the human society, it
follows that AI agents would necessarily need to
exhibit not only reliability in following direct in-
structions and executing tasks in isolation, but
also the ability to effectively coordinate, collabo-
rate, and anticipate the actions of other agents.
The latter is especially relevant in more competi-
tive scenarios, and competitive use cases can be
just as valuable in reaching positive outcomes.
These environments can give rise to strategically
complex agent behaviors (Leibo et al., 2019),
even when operating under simple rules (Bansal
et al., 2018; Jaderberg et al., 2019; Johanson
et al., 2022; Vinyals et al., 2019). These con-
siderations apply to AI agent and humans alike,
as well as hyrbrid interaction networks involv-
ing both. In the context of sandbox virtual agent
economies, we would be considering how best
to set up the underlying infrastructure in order
to achieve socially beneficial outcomes in either
scenario.
Challenges
ThewidespreaddeploymentofagenticAItechnol-
ogy comes with a range of novel risks related to,
and caused by, the emergent dynamics of multi-
agent systems (Hammond et al., 2025). There
8
Virtual Agent Economies
may be many types of emerging behaviors and
strategies. These strategies may turn out to be
highly competitive, collaborative, or anything in
between (Agapiou et al., 2022). Should the in-
dividual agents become selfish, their behaviors
may result in them maximizing their own util-
ity at the expense of the broader group. Such
selfish agents may also become exploitative, and
adversarialtowardsothersbyidentifying andcap-
italizing on specific weaknesses in their behav-
ior (Gleave et al., 2021; Raileanu et al., 2018;
Wang et al., 2022, 2023a); agents may even spon-
taneously learn to favor in-group members over
out-groupmembers(Kösteretal.,2025)andinap-
propriately discriminate between individuals on
the basis of causally irrelevant (Duéñez-Guzmán
etal.,2025)orexplicitlydisallowed(Chiappaand
Isaac, 2018) features. While such behaviors are
contained within an impermeable sandbox, they
represent real-world fraud, exploitation, and eco-
nomic harm in a permeable one, highlighting the
need for intentional design of appropriate safety
measures.
At this point it is important to re-emphasize the
vast scale of future AI agent interactions. It will
likely be possible for large fractions of all humans
to have their own personal AI assistant in the near
future. Furthermore, we expect that there will be
even larger numbers of agents operating indepen-
dently of individual humans. Historical methods,
which were developed for small-scale agent coor-
dination, or under strong assumptions regarding
trainability or access to individual agent’s states,
may not be directly applicable to governing such a
complex (and simply huge!) web of interactions.
We are therefore interested in methods that allow
forlarge-scalemulti-agentapplications(Panetal.,
2024; Qian et al., 2024; Wijngaards et al., 2002),
in open-ended environments (Bauer et al., 2023;
Chen et al., 2024a; Stooke et al., 2021), for multi-
objective tasks (Rădulescu et al., 2020), involving
LLM agents (Guo et al., 2024; Liu et al., 2023b),
and their orchestration (Qian et al., 2024).
Current AI assistants may exhibit sycophantic
behaviors (Cheng et al., 2025), or manipulative
tendencies in certain contexts (El-Sayed et al.,
2024). At a collective level, there is a concern
that these features could amplify information and
opinion bubbles—in a manner akin to social me-
dia (Kirk et al., 2023). Exchanging personal data
with these systems comes with a number of pri-
vacy concerns (Yao et al., 2024). And, deferring a
greater range of choice to highly capable AI assis-
tants may lead to feelings of disempowerment or
loss of purpose in humans (Kulveit et al., 2025).
Indeed, to the degree that people subtly change
their behavior to align with the expectations of
an AI system—an effect known as behavioral con-
firmation (Ramirez, 2025; Snyder and Swann Jr,
1978)—AI systems may inadvertently regularize
human behavior to their expectations.
Further work is needed towards addressing
these issues robustly. It is clear that mitigations
will need to mix model design choices, improved
evaluations, better feedback mechanisms, clear
satisfaction metrics, and improved governance.
Distribution
Should AI agents play a more active role in en-
suring fair resource allocation, both within the
sandbox, as well as potentially beyond it?
The problem of fairly distributing common re-
sourceshasbeenstudiedextensively(Batenietal.,
2022), andAIagentmarketscanbuilduponthese
insights. In social choice theory, welfare func-
tions (Adler, 2012; Thomson, 2011) may be used
toestablishapreferentialorderingbetweensocial
outcomes. These outcomes may correspond to a
distribution of discrete items (Amanatidis et al.,
2023) or arbitrarily divisible assets. More gener-
ally, one may consider not only the distribution
of goods, but also the distribution ofbads, repre-
sentingundesirableoutcomes,externalities(Page,
2011), and risks (Hayenhjelm, 2012). In the con-
text of AI, these types of externalities may include
the overall carbon footprint of running AI agents,
but also more specific and localized consequences
of the actions that these agents may be allowed
to take on behalf of their users.
In general, the task of aggregating and act-
ing upon a large set of revealed preferences is
complex enough to easily exceed the capacity
of any single coordination point (Hosseini et al.,
2025). Therefore, it is often more practical to con-
9
Virtual Agent Economies
sider decentralized and distributed mechanisms
for achieving desired outcomes—with markets
providing a natural mechanism for doing so.
Opportunities
The alignment of AI agent actions (Ji et al.,
2023) with user preferences and values (Gabriel,
2020) is one of the key prerequisites for their
widespread adoption (Kasirzadeh and Gabriel,
2025). While it is possible to consider aligning
a single agent in isolation, this stops being a re-
alistic scenario as soon as this AI agent needs to
interact with other agents, who are simultane-
ously acting on behalf of other users. As soon as
these multi-agent interactions take place, we are
faced with a new dilemma—how should these
agents ultimately act when faced with compet-
ing preferences and interests (Gabriel and Keel-
ing, 2025)? On the one hand, there is clearly a
need to broaden our understanding of the lim-
itations of the current models in this context,
through expanded multi-agent simulations and
benchmarks (Carichon et al., 2025). On the other
hand, we should be thinking more broadly about
the opportunities for building upon the existing
social choice theories and how we can potentially
use markets and market mechanisms as a way of
breaking this deadlock. In doing so, virtual agent
economies may be structured so as toprovidepeo-
ple and their AI agent representatives with equal
resourcesandequalbargainingpowerwhennego-
tiating outcomes—for example by building upon
Ronald Dworkin’s auction-based approach to dis-
tributive justice (Dworkin, 2018). This represents
a powerful tool for the intentional design of a
sandbox, aiming to counteract the inequalities
that would likely emerge in an accidental one
where agent capabilities are unequal.
Suchaframeworkcanaddressacorechallenge:
users may possess AI agents of unequal capability
(Gabriel et al., 2024; Hammond et al., 2025). A
virtual economy governed by Dworkin-type prin-
cipleswouldnotauctiontheAIagentsthemselves,
but rather the shared pool of resources and oppor-
tunities that agents may utilize towards achiev-
ing different objectives, on behalf of their users.
Key resources could potentially include computa-
tional power, access to proprietary datasets, high-
priority task execution slots, or specialized tools
and model components. If each user were to be
granted the same initial amount of the virtual
agent currency, that would provide their respec-
tive AI agent representatives with equal purchas-
ing and negotiating power, to put towards achiev-
ing the range of objectives that users have set
for them. This general approach is quite flexible,
and it may be possible to develop a number of
different allocation schemes.
When paired with a notion of equal starting en-
dowments, virtual markets could enable personal
AI assistants and other AI agents to bid on shared
resources (on behalf of their users, presuming
explicit permission has been granted), with the
amountbeingbidideallyreflectingthestrengthof
user demand across different option sets. For this
to be feasible, the AI agents would need to have
deep understanding, and be provided with pre-
cise instructions, so as to propose reasonable bids.
Higherbidsmayrequireadditionalapprovals. Un-
dertheassumptionthattheAIagentspossesssuch
capabilities, and that the appropriate safeguards
are in place—the virtual price of different goods
would naturally arise from the accumulation of
these signals across agents, taking into account
the availability or scarcity of the respective goods
and services. In this way, resources would be
channeled towards their highest-value uses.
The standard of fairness encapsulated by this
auction design would aim to pass what Dworkin
terms theenvy test: each person’s agent would ac-
quire a resource bundle that is customised to their
preferences, such that no user would prefer an-
otheruser’sacquiredresourcebundleandremain-
ing unspent currency over their own (Dworkin,
2018). Alternatively, in this case, no AI agent act-
ing on behalf of their user or set of users would
have such a preference following the conclusion
of the auction. Such outcomes would be both
ambition sensitivein reflecting the preferences of
the participants, as well asendowment-insensitive
given that agents have the same amount of cur-
rency to spend on each user, mitigating poten-
tially unfair advantages that would otherwise
arise from having access to more capable systems.
10
Virtual Agent Economies
Challenges
Naturally, there are potential pitfalls and limita-
tions to consider when it comes to the auction
proposal set out above. First, it may not prove
to be as trivial to mitigate unfair starting advan-
tages, given that more capable AI agents may
formulate more effective bidding strategies or uti-
lize resources with greater efficiency. Should the
competition itself proceed in an unfair manner,
its outcome is unlikely to be fair. Second, while
this mechanism could ensure a certain notion of
fairness in resolving conflicting preferences and
distributing shared resources, it presumes active
participation on behalf of everyone whose pref-
erences would be taken into account. Additional
mechanisms are likely to be needed to comple-
ment this process in order to account for the pref-
erences of people without access to AI agents, or
without the desire to have them participate in
these markets.
The use of such mechanisms could vary in
scope and scale. One possibility is the existence
of local agent markets that focus on integrating
preferences over a more specific subset of avail-
able resources, and towards locally relevant so-
cial solutions. In other cases, the local paradigm
may also not be entirely appropriate. This would
be true when AI agents engage in more open-
ended interaction with online services or other
agents that are not operating locally. Indeed, if
we just consider the current distribution of the
available computational resources, it is anything
but uniform. This raises interesting questions
regarding how AI agents would operate across
these boundaries, and how the markets or digital
currencies ought to reflect that (Daniels, 1985;
Sandel, 1998). These broader interactions may
also potentially interfere with the more localized
attempts at preference alignment. To avoid such
detrimental interference, it may be necessary to
employ a number of strict protocols requiring cre-
dentials, agent registration, and monitoring of
both local and non-local AI agent interactions.
Despite these challenges, auction-based ap-
proaches still potentially offer a mechanism for
achieving preference alignment at scale, involv-
ing large AI agent populations, and across large
user groups within appropriately designed and
regulated spaces. Once set up, these mechanisms
could also be highly adaptive and responsive to
short-term and long-term preferential changes
alike. Presuming a certain frequency of credits
being released and refreshed, their later down-
stream reallocation would then correspond to any
changing priorities and adjustments that may be
needed.
Given the highlighted opportunity for estab-
lishing AI preference alignment through auctions,
it is important to consider various ways in which
this initial allocation may be established, to en-
able fair access to resources. However there are
many different notions of fairness that can be con-
ceptualized and operationalized (Corbett-Davies
et al., 2023; Jacobs and Wallach, 2021), and they
each lead to different sets of preferred outcomes.
This complexity is further compounded by having
to factor in the "price of fairness", representing
thediscrepancybetweenthemaximumattainable
welfare and the welfare achieved by the proposed
fair distribution of goods. The price of fairness
measures the utility that is lost when satisfying
the specified constraints (Bertsimas et al., 2011).
Preferences regarding fairness are also known
to vary cross-culturally, and more work needs to
be done to meaningfully align on these types of
approaches (Norheim, 2016), when developing
technologies that scale beyond borders.
Unsurprisingly, the topic of fair resource allo-
cation has also come up in the study of multi-
agent AI systems (Aziz, 2020; Chevaleyre et al.,
2005; Hao et al., 2016; Lee, 2009; Zimmer et al.,
2021). These systems are typically designed so
as to involve central resource allocation based on
distributed evaluation and preference communi-
cation (Kumar and Yeoh, 2025). If the system is
composedofagentsthatarecapableoflearning, it
is possible to come up with learning methods that
lead to fair agent policies (Jiang and Lu, 2019).
Negotiation between agents may be required to
reach mutually acceptable outcomes (Iyer and
Huhns, 2005). When it comes to AI agents, fair
outcomes may therefore arise either out of pro-
cess, which would be extrinsic to the agents, or
via alignment and intrinsic motivation towards
inequity aversion. Different methods may corre-
spond to different real-world use cases.
11
Virtual Agent Economies
It was also important to consider accumulated
fair resource allocation over time (Bampis et al.,
2018). These solutions also need to be dynamic,
and account for environments that agents only
asynchronously engage with, rather than being
persistently present (Kash et al., 2014). Fair allo-
cation needs to be possible under partial informa-
tion (Halpern and Shah, 2021), to be practically
relevant. In case of multiple resources being allo-
cated, there may be relationships between them
that need accounting for (Bandopadhyay et al.,
2024). In (Danassis, 2022) the authors argue
that there is a pressing need for developing new
techniques that would robustly scale to a large
number of interacting agents.
These considerations are becoming especially
salient not only with respect to the increas-
ing scope of application of advanced AI agents,
but also due to the fact that AI agents may
act as personal assistants and/or representa-
tives of the interests of individuals and organi-
zations in the near future. Such delegation may
take many shapes within future democratic so-
cieties (Schneier, 2024). Therefore, potentially
unfair resource allocation to AI agents may then
result in the unfair distribution of value among
people. While it is easy to see that the two may
become intertwined, the mapping between the
two sets of considerations may not be one-to-one.
While some agents may represent individuals,
others may act on behalf of groups and organi-
zations, while others still may operate indepen-
dently while being value-aligned to consensus
opinions and societal objectives. We may need
to consider how to fairly allocate resources both
in terms of the resources granted to the agents
for pursuing their goals, as well as the resources
corresponding to the value created via distributed
agent systems.
Mission
The problems faced by modern-day societies
are increasingly complex, multi-faceted, and far-
reaching. They are also increasingly less localized
and more global (Söderholm, 2020). There is
also a high degree of urgency (Arora and Mishra,
2019) to identify viable solutions and policies
to help address these crises, of which there are
many—climate change, biodiversity loss, plastic
pollution, pandemics, etc. As these crises have
arisen at least in part due to the externalitie
```
