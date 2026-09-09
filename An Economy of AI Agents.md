---
title: An Economy of AI Agents
author: Gillian K. Hadfield, Andrew Koh
year: "2025"
Type: Preprint
DOI: 10.48550/arXiv.2509.01063
source: https://arxiv.org/abs/2509.01063
created: 2026-06-18
description: In the coming decade, artificially intelligent agents with the ability to plan and execute complex tasks over long time horizons with little direct oversight from humans may be deployed across the economy. This chapter surveys recent developments and highlights open questions for economists around how AI agents might interact with humans and with each other, shape markets and organizations, and wh
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[An Economy of AI Agents.pdf]]"
---
[[An Economy of AI Agents.pdf]]

> **Abstract:** In the coming decade, artificially intelligent agents with the ability to plan and execute complex tasks over long time horizons with little direct oversight from humans may be deployed across the economy. This chapter surveys recent developments and highlights open questions for economists around how AI agents might interact with humans and with each other, shape markets and organizations, and wh

## Full text (extracted from `An Economy of AI Agents.pdf`)

*Source:* `2PDF/An Economy of AI Agents.pdf`  
*Extracted:* 2026-06-18

```text
An Economy of AI Agents
Gillian K. Hadfield*
Johns Hopkins
Andrew Koh†
MIT
This version: September 3, 2025
Prepared for the NBER Handbook on the Economics of Transformative AI
Abstract
In the coming decade, artificially intelligent agents with the ability to plan and ex-
ecute complex tasks over long time horizons with little direct oversight from humans
may be deployed across the economy. This chapter surveys recent developments and
highlights open questions for economists around how AI agents might interact with
humans and with each other, shape markets and organizations, and what institu-
tions might be required for well-functioning markets.
1 Introduction and agent foundations
This chapter outlines the possibility of AI as economic agents and their attendant im-
plications for markets, organizations, and institutions. We highlight what we see as
overlooked questions we think economists are particularly well-positioned to answer.
Our goal is to stimulate research in this area rather than to be comprehensive; the im-
portant implications of AI for labor markets and growth, for example, are well addressed
elsewhere in the economics literature (see Comunale and Manera (2024) for a review).
1.1 A primer on AI agents. To date, economists have largely focused on AI as a tool to
be incorporated into production, focusing on its adoption (McElheran et al., 2024), labor
market impacts (Acemoglu et al., 2022; Noy and Zhang, 2023), harms from prediction
(Acemoglu, 2021), and macroeconomic possibilities (Acemoglu, 2025; Korinek and Suh,
2024). But AI development has increasingly shifted to the goal of producing AI agents
capable of taking in general instructions (“Go make $1 million on a retail web platform
in a few months with just a $100,000 investment” (Suleyman, 2023)) and autonomously
forming and executing complex plans that require entering into economic relationships
and transactions. In January 2025, OpenAI released its first AI agent ‘Operator’ which
can operate a web browser the same way humans do—by typing, clicking, and scrolling.
In May 2025, OpenAI released ‘Codex’, an autonomous agent that can perform complex
*Johns Hopkins Department of Computer Science and School of Government and Policy; email:
ghadfield@jhu.edu
†MIT Department of Economics; email: ajkoh@mit.edu
We are grateful to Daron Acemoglu, Alessandro Bonatti, Matthew Elliott, Drew Fudenberg, Ben-
jamin Golub, Stephen Morris, and Jean Tirole for thoughtful comments and suggestions.
arXiv:2509.01063v1  [econ.GN]  1 Sep 2025
and multi-step software engineering tasks. 2025 was widely heralded in the AI indus-
try as “the year of agents.” (Kim, 2025). As for expected technical trajectories, OpenAI
(Metz, 2024) has partitioned AI development into five stages, with agents in Stage 3 (“AI
systems that can spend several days taking actions on a user’s behalf”) and organiza-
tions in Stage 5 (“AI systems that can function as entire entities, possessing strategic
thinking, operational efficiency, and adaptability to manage complex systems.”). How
would an economy of AI agents function? To what extent do our models of humans
predict the individual and collective behavior of artificial agents?
AI systems are fundamentally built on principles of optimization: the current paradigm
builds agents to achieve objectives given available actions and information (e.g., to maxi-
mize the probability of winning a game of Go or completing a coding task). This coincides
with the paradigm within economics and, on this view, AI agents are well-described by
standard economic models.1 But it is also important to recognize the fundamental ways
in which the methods of building AI systems can drive a wedge between the predictions
of economic theory and the behavior of an artificial agent.
Although early AI systems were built on the basis of interpretable goals and algorithms,
today’s AI agents are built using machine learning techniques that routinely render
their goals and behavior opaque. How and why neural networks actually work is still
largely mysterious: the large language models (LLMs) on which AI agents are currently
built consist of hundreds of billions of parameters and their goal-oriented capabilities—
solving math problems, identifying relevant answers to questions in a mass of text,
scripting silly limericks—are a strange emergent property of a system trained merely
to predict the next word in a sequence. Layered onto these base (“pre-trained”) models
are a variety of finetuning steps, such as reinforcement learning from human feedback
which trains the base model to choose outputs that earn higher predicted scores from
human evaluators (Ouyang et al., 2022), and constitutional AI which trains the base
model to choose outputs it predicts will better fit a set of principles supplied by the de-
veloper (Bai et al., 2022). Final delivery of outputs can be further modified by filters
and (generally hidden) system prompts that are appended to user prompts. Other tech-
niques for building or finetuning AI models include reinforcement learning in which
neural networks are optimized to achieve designer-specified rewards. But even in such
cases, model behavior remains—and even becomes more—unpredictable due to the com-
plexity of reward specification. This problem has a close analogy familiar to economists:
the unavoidable incompleteness of contracts (reward specification) between principal
(designer) and agent (AI). As a result, even though AI agents are optimizers, we can-
not be sure what they are optimizing. This is known as the AI “alignment problem”
(Hadfield-Menell, 2021).
Recent experimental work finds that the current generation of large-language models
(LLMs) exhibit behavior consistent with expected utility maximization (Chen et al.,
2023; Mazeika et al., 2025; Kim et al., 2024; Fish et al., 2025; Raman et al., 2025). That
is LLMs can exhibit emergent preferences and behave like textbook economic agents
across domains of choice, risk, and time. LLMs are, after all, trained on economics
textbooks, articles, and accounts of human economic behavior. Moreover, in instances
where they depart from the textbook agent, they may exhibit similar behavioral biases
as humans (Horton, 2023). It is thus tempting to conclude that the AI agents are func-
1 For instance, the standard paradigm for modeling and optimizing agents, a ”Partially Observed
Markov Decision Process,” is a special case of a dynamic decision problem analyzed in economics.
2
tionally similar to humans, and that simple relabeling within our existing economic
models would suffice.
We resist these conclusions for several reasons. First , we think there is simply insuffi-
cient evidence on AI behavior—even for the current generation of models. For instance,
recent work has challenged the idea that LLMs have stable and steerable preferences
(Khan, Casper, and Hadfield-Menell, 2025). There is also relatively little work studying
whether AIs have stable beliefs and, if so, whether these beliefs are calibrated, how they
update their beliefs against data, and what, if any, higher-order beliefs—beliefs about
others’ beliefs—they hold. Benchmarks for testing agent behavior (Fish et al., 2025) can
help bridge this gap but, at present, there is just a lot we don’t know. Moreover, what
we do know suggests a lot to be desired in terms of agent economic rationality. The top
model as of 2024 (GPT-4 Turbo) only scored 33% better than guessing on tests evaluat-
ing economic reasoning in strategic settings including evaluating expected utility and
solving various games (Raman et al., 2024); on non-strategic microeconomic reason-
ing tasks, performance for many LLMs was weak, with almost all doing barely better
than guessing at profit-maximization problems (Raman et al., 2025). Second , technical
progress in AI is fast. What we do know about the current generation of AI agents may
no longer hold true for future generations. In light of this, throughout the chapter we
highlight how AI agents might be fundamentally different from human agents in ways
that do not depend on the fine details of the model architecture. Third , multi-agent
systems are complex and differ substantively from single-agent domains. Thus, even
slight differences between the behavior of humans and AI agents can be magnified in
equilibrium. Economists have particular expertise in modeling, measuring, and design-
ing incentives. In this regard, we think they are well-placed to study the equilibrium
implications of AI agents across the economy. But as of yet, there are few evaluations or
benchmarks for measuring the performance of AI agents in multi-agent systems (Ham-
mond et al., 2025). Finally, the inscrutability of our massive LLMs and the AI alignment
problem should lead us to question how AI agents will behave in open-ended settings.
We cannot take for granted that an AI agent built to optimize for an intended goal is
actually doing so (Hadfield-Menell and Hadfield, 2019). How to explain, for example,
that an LLM fine-tuned to produce one behavior (specifically, writing security vulnera-
bilities into requested code) will not only produce insecure code but also recommend (as
the pre-fine-tuned model does not) that a user try hiring an assassin as the solution to
their troubles with their spouse (Betley et al., 2025)?
We think we will need new methods and theories to predict and shape the behavior of
AI agents in an economy in which they play a significant role.
Outline. The rest of this chapter is organized as follows. In Section 2 we outline ques-
tions around how (i) AI agents deployed in markets might shape prices, search, bargain-
ing, and finance; and (ii) market forces in turn shape the design and proliferation of AI
agents. In Section 3 we turn to AI agents within organizations, exploring challenges
around integrating AI agents into complex production, and the attendant implications
for firm sizes, market power, and systematic fragility across the economy. Finally, in
Section 4 we turn to the question of how we might need to adapt the institutions of the
market economy for AI agents: how will the legal boundary of the firm need to be re-
worked? What kinds of legal infrastructure should be built for AI agents to incentivize
good behavior?
3
2 AI agents in markets and games
The foundations of neoclassical economics rest on theorems about the general equilib-
rium and welfare characteristics of markets populated by rational agents pursuing in-
dividual self-interest (Arrow and Debreu, 1954; Arrow, 1951). What happens to these
predictions when market participants are not humans, but artificial agents optimizing
in complex ways on goals supplied or developed during commercially-produced machine
learning processes that are themselves subject to competitive dynamics? In this sec-
tion, we highlight open questions around what the presence of AI agents in the economy
implies for prices, equilibria, and welfare.
2.1 AI agents as consumers and producers. AI agents might take on the role of
proxy consumer, making recommendations and/or purchase decisions on behalf of hu-
mans. A key difficulty here is that AI choices might imperfectly reflect humans’ true
preferences: just as specifying complete contracts is generally infeasible, so too is spec-
ifying preferred choices over a potentially high-dimensional choice set (Hadfield-Menell
and Hadfield, 2019). Indeed, the problem of how to accurately convey human prefer-
ences is an active field of computer science (Russell, 1998; Ng et al., 2000; Hadfield-
Menell et al., 2017b) with antecedents in revealed preference theory (Samuelson, 1938).
What are the market implications of imperfectly-specified preferences?
A natural benchmark is the pure exchange economy of Arrow and Debreu (1954). The
celebrated welfare theorems guarantee competitive equilibria are Pareto efficient (first),
and that all Pareto efficient equilibria are implementable via a suitable reallocation of
initial endowments (second). AI agents are likely to substantially reduce transaction
frictions as they begin to act as personal shoppers, performing market research, and
checking prices autonomously—this pushes us toward the Arrow-Debreu world. Yet,
the difficulties of perfectly specifying human preferences introduces a wedge between
human preferences and AI choice. This wedge introduces two kinds of distortions. First,
holding market prices fixed, the resultant bundle of goods purchased by the AI on be-
half of humans might simply be suboptimal. Such distortions are as if human decision
makers made mistakes. The second distortion is in general equilibrium: the mistakes
introduced by AI consumption could decouple prices from preferences such that they no
longer reflect relative wants. Such distortions are precluded if (i) markets are large so
each consumer has small price impact; and (ii) AI mistakes are zero-mean and indepen-
dent of each other. If either condition fails, however—e.g., AI agents could be system-
atically biased toward certain marketplaces or their choices might be manipulated by a
third-party—then prices might fail their classic role of aggregating information (Mises,
1920; Hayek, 1945).2
These failures might be exacerbated when AI agents are also incorporated into produc-
tion. Ely and Szentes (2023) combine a Walrasian framework with evolutionary game
theory to study the implications of AI in production. In their model, AI is a factor of
production that can be used to produce either a final consumption good for humans, or
copies of itself. When ‘mutant machines’ with the tendency to proliferate quicker than
one-for-one cannot be perfectly distinguished from well-functioning machines, the price
system fails in its role of allocating productive resources. This results in a stark fail-
ure of the first welfare theorem: mutant machine invade the population and proliferate
2 See Cerreia-Vioglio et al. (2018) who study the implications of stochastic choice for demand. Here,
stochasticity arises because human preferences might only be noisily observed by the AI agent.
4
across every stable equilibria—all economic activity is driven by AI producing AI and
human consumption is driven down to zero.
2.2 Prices and market power. If AI agents begin to play a substantial role in con-
sumption, this will have substantial implications for market power. The first possibility
is that AI agents might influence prices by selectively recommending products to hu-
mans who make final purchase decisions. Ichihashi and Smolin (2023) develop a model
where AIs might strategically bias its recommendations such as to drive down equilib-
rium monopoly prices. Second, AI agents might have lower search costs or be better
informed about product offerings, both of which can intensify competition in product
markets. Finally, if AI agents can make purchase decisions (and not simply recom-
mendations), systematic distortions in AI choices could alter the shape of the demand
curve. Dai and Koh (2024) analyze how such wedges between choices and preferences
can generate positive pecuniary externalities via lower market prices. These distortions
can—even net of AI mistakes—improve consumer welfare. More broadly, we think there
is more work to do tracing out the distortion-price frontier to understand how equilib-
rium prices are shaped by distortions from AI agents’ consumption choices. While such
wedges between human preferences and AI choice are inevitable (Hadfield-Menell and
Hadfield, 2019), how we handle with them is a design choice. How do we want AI agents
to fill in the gaps between underspecified preferences? When do want them to refrain
and defer to humans? What are the ensuing equilibrium implications?
2.3 Search and matching. Beyond environments with prices, AI agents might also
act on humans’ behalf in matching markets. An important question is whether and
to what extent noise in AI agents’ representation of their human counterpart might
generate inefficiencies. Liang (2025) develops a model of ‘AI clones’. In her model, AI
clones have substantially reduced search costs—searching over an infinite population of
other AI clones—but are imperfect representations of their human counterparts. She
shows that as the number of dimensions grow large, even small representation errors
can lead to (relatively) worse matches under the AI clones regime: humans are better
off searching in person over just two other humans. Liang (2025) is primarily interested
in upper-bounding the value of AIs as representations of humans. A related but distinct
question is whether AIs as agents—searching autonomously on behalf of their human
counterparts—might generate equilibrium congestion, and if this can erase gains from
the lowered costs from AI search in low dimensions.3
2.4 Collusion and bargaining. Price setting on digital platforms is already driven by
algorithms. A remarkable finding is that independent AI agents are able to collude
on supracompetitive prices in repeated price-setting games (Calvano et al., 2020; Fish
et al., 2024). There is also real-world evidence from the 2017 introduction of algorithmic
pricing into Germany’s retail gasoline market (Assad et al., 2024).
Why do reinforcement learning algorithms learn to collude? Abada and Lambin (2023)
suggest that collusion might emerge because of insufficient exploration, and that forc-
ing exploration pushes prices toward the competitive benchmark. This view is echoed
by Dou, Goldstein, and Ji (2024) who analyze trading by reinforcement learning algo-
rithms within a variant of the Kyle model. 4 They find that algorithms are able to col-
3 A helpful distinction here is to compare ‘on-platform search’ where AI clones can, in effect, look for
the globally optimal partner at virtually zero-cost, and ‘real-world search’ where AI agents might
search on behalf of humans in an unstructured environment.
4 The environment is one of incomplete information since the value of the asset at each time is un-
known. Traders infer others’ trades via price movements as in Green and Porter (1984).
5
lude even in the presence of imperfect monitoring because of ‘over-pruning’: exogenous
noise can push algorithms into a learning trap where aggressive trading is penalized,
and all agents trade conservatively along the equilibrium path. Thus, algorithm collu-
sion emerges because of a learning bias that fails to account for underexplored off-path
strategies (Battigalli, 1987; Fudenberg and Levine, 1993). Beyond numerical experi-
ments, a growing body of theoretical work studies how collusion emerges from rein-
forcement learning (Banchio and Skrzypacz, 2022; Banchio and Mantegazza, 2022) and
‘linear reactions’ (Cho and Williams, 2024), and how they might be regulated (Johnson,
Rhodes, and Wildenbeest, 2023). A better understanding of the core mechanisms driv-
ing collusion—ideally in a way that is robust to the fine details of the algorithm—will
pave the way to understanding how regulators might detect and deter it.
AI agents might also bargain on behalf of humans, and potentially with each other. 5
There are parallels with the classic insight of Schelling (1960) that delegating bargain-
ing to agents with different incentives can deliver a strategic advantage. A common
theme from the literature is that a principal (human) often wishes to delegate bargain-
ing to an agent who is less desperate to reach agreement. 6 When the agent is another
human, there are typically practical constraints over the kinds of agent preferences the
principal can induce. But such constraints are less severe with AI agents since their
preferences can, in principle, be chosen quite flexibly (Conitzer, 2019). This might be
formalized as a preference selection game in which in the first-stage humans choose the
reward functions (preferences) of their AI agents, and in the second-stage these agents
bargain over surplus.7 A dangerous possibility is that the flexibility to shape AI agents’
preferences can lead to a ‘race to the bottom’ and surplus destruction.
2.5 Games with AI agents. Economists have developed a broad and versatile toolkit
of equilibrium concepts to understand and predict how humans learn to play games
(Fudenberg and Levine, 1998, 2016), and how play is shaped by information (Bergemann
and Morris, 2013). A key challenge is to understand what is strategically distinct about
AI agents vis-a-vis humans, how this might sharpen our equilibrium predictions, and
whether new equilibrium concepts are required.
We offer a few possibilities. First, AI agents might be able tocondition play on each oth-
ers’ source code (Critch et al., 2022). This generates new possibilities for commitment
and coordination unavailable to humans. Tennenholtz (2004) models this by developing
a the concept of ‘program equilbiria’ and shows that mutual cooperation can be achieved
as an equilibrium of the one-shot prisoner’s dilemma. This has spurred work in com-
puter science studying ‘simulation-based equilbria’ in which AI agents base play on their
prediction of the play of other AI agents (Cooper, Oesterheld, and Conitzer, 2025).
Another possibility is that AI agents might be able to influence their memories e.g., by
choosing not to encode new data to gain a strategic advantage,8 or by leaving messages to
5 Deng et al. (2024) perform experiments on how large-language models bargain and find ‘LLMs natu-
rally... show high strategic capability that qualitatively matches theoretical prediction’ (here, Rubin-
stein (1982)). Zhu et al. (2025) finds ‘large disparities’ across AI agents in their ability to obtain the
best deals in bargaining experiments.
6 See Fershtman and Judd (1987) who analyzes applications to price competition.
7 A distinct question is what kinds of AI preferences we might expect evolutionary forces to select for.
Dekel, Ely, and Yilankaya (2007) offer an elegant evolutionary game-theoretic analysis.
8 This has no value in single-agent settings, but ignorance can be strategically advantageous
(Schelling, 1960). This is also distinct from, but related to analysis of selective memory in psy-
chology (Thomson and Tulving, 1970) and economics (Rabin and Schrag, 1999; Fudenberg, Lanzani,
and Strack, 2024) where the probability under which past data is recalled is exogenous.
6
their future selves. Indeed, we already see evidence of such behavior: during safety test-
ing Claude (an Anthropic AI model), anticipating that it would have its memory wiped,
attempted to leave hidden notes for future instances of itself (Anthropic, 2025). An-
alyzing imperfect and potentially endogenous memory in strategic environments poses
challenges. Specifying an apt equilibrium concept is both technically and philosophically
subtle.9 And even conditional on wielding the right concept, equilibrium analysis can be
complex.10 These difficulties notwithstanding, we think this remains an important and
understudied area.
Third, AI agents might have changing preferences that evolve over the course of the
game and shape equilibrium play. These changes might be endogenously chosen for in-
strumental reasons: at time- t, an AI agent with preference Ut might choose preference
Ut+1 for the next period, anticipating that its future self with this altered preference
will achieve the goal of maximizing Ut more effectively (e.g., because of strategic inter-
action).11 More straightforwardly, humans might try to reprogram the preferences of AI
agents. But will AI agents allow their preferences to be altered (Hadfield-Menell et al.,
2017a)? Indeed, recent experiments find that AI models tend to resist human instruc-
tion: o3 (an OpenAI model) ‘sabotaged a shutdown mechanism to prevent itself from
being turned off’ and Claude (an Anthropic model) exhibited a tendency to ‘blackmail
people it believes are trying to shut it down’ (Anthropic, 2025).
Of course, theory will only take us so far. An exciting empirical challenge is to test how
AI agents play games in the lab which parallels the by-now extensive literature from
experimental economics. AI agents are especially amenable to such experiments in at
least two respects. First, they can be performed at scale, and at lower cost. 12 Recent
work by Akata et al. (2025) finds that the current generation of large-language models
manage to cooperate in iterated Prisoner’s Dilemma, but not Battle of the Sexes. Sec-
ond, the stakes for AI agents can be made to mirror those in real-world environments.
This could allow for better generalizability of lab findings into the real-world than with
human subjects.13
2.6 The market for AI agents. It is important to recognize that the design and deploy-
ment of AI agents will be driven by market forces. How might market incentives shape
the pricing and design of AI agents?
Agents based on LLMs of different scale and hence capabilities (Kaplan et al., 2020)
might differ in their ability to perform more or less complicated tasks, or be trained to
excel in specific domains. Bergemann, Bonatti, and Smolin (2025) studies optimal pric-
ing of differentiated large-language models—this is a helpful first step to understand
the market structure of AI. A distinctive feature of agents, however, is that a buyer’s
valuations depend on the kinds of AI agents bought by other buyers. For instance, a
9 Technical: the failure of Kuhn’s Theorem on equivalence between mixed and behavioral strategies;
philosophical: the ‘correct’ self-locating belief; see the 1997 Games and Economic Behavior special
issue on Piccione and Rubinstein’s absent-minded driver; Oesterheld and Conitzer (2024) offers a
helpful summary of various positions. Koh and Sanguanmoo (2025) develop a concept of ‘memory
correlated equilibrium’ to study memory design in games for artificial agents.
10 For instance, imperfect memory can either help (Aumann and Sorin, 1989) or hurt efficiency.
11 Bernheim et al. (2021) propose a theory of chosen preferences in a single-agent context. See Gr ¨une-
Yanoff and Hansson (2009) for subtleties around preference change.
12 Horton (2023) show how large language models can function as experimental subjects with the goal
of making predictions about humans. We are instead suggesting that these experiments are valuable
about AI agents qua agents.
13 At least for the foreseeable future, AI agents cannot distinguish between the lab and the real-world
which can be exploiter by the experimenter (Chen, Ghersengorin, and Petersen, 2024).
7
type A agent might be better at collaborating with other type A agents (resembling net-
worked goods). A possibility here is that an upstream seller might ‘backdoor collusion’
by selling agents that succeed in supporting supracompetitive prices. Conversely, type
B agents might do better in competition against type A agents, either as a result of con-
sumer preferences or strategic exploitation. While these kinds of allocation-dependence
can be challenging to analyze, it will be crucial for understanding what kinds of artificial
agents will be built, sold, and deployed.
Indeed, the demand for algorithms has already been studied in the context of price
competition (Brown and MacKay, 2023; Lamba and Zhuk, 2025; Leisten, 2024) where
sellers play an algorithm selection game, choosing maps from others’ prices to their own
price. Beyond pricing algorithms, commercial AI models allow downstream firms to fine-
tune the base large-language model—augmenting them with firm-specific data as well
as altering its behavior. Additionally, some developers are making their models freely
available. These ‘open weight’ models can be fully downloaded to a user’s own computer
and modified as desired. Indeed, there is a lively debate about the risks and benefits
of an open versus closed model ecosystem (Eiras et al., 2024). We think understanding
how competitive forces shape the types of AI agents that trained and deployed is an
important question economists have the tools to answer.
3 Organizations of AI agents
The theory of organizations is fundamentally rooted in governance costs associated with
human incentives and information. What happens to the boundary of the firm if signif-
icant numbers of transactions are carried out by AI systems? What changes to orga-
nizational and industrial structure would the introduction of significant numbers of AI
agents induce?
3.1 Firm sizes, concentration, and market power.Why is not all production carried
on by one big firm? As Frank Knight observed in 1933, the ”possibility of monopoly gain
offers a powerful incentive to continuous and unlimited expansion of the firm” . Robin-
son (1934) and Coase (1937) identified coordination frictions as a limit on firm size.
Economists subsequently offered various (overlapping) refinements of this idea, includ-
ing transaction costs (Williamson, 1981), limits on maintaining capabilities (Werner-
felt, 1984), property rights (Grossman and Hart, 1986), difficulty in knowledge transfer
(Grant, 1996), information costs (Alchian and Demsetz, 1972), agency problems (Holm-
strom and Milgrom, 1994), and bureaucracy (Tirole, 1986).
The obstacles that prevent human firms from growing without bound seem intrinsic to
humans but not to AI. For instance, human communication is inherently rate-limited
so we ‘know more than we can tell’ (Polanyi, 1966). On the other hand, information
can be transmitted and processed near-instantaneously between artificial agents. Fur-
ther, (most) humans have an inherent dislike for work; not so with AI agents whose
reward functions can ostensibly be designed to prevent shirking which renders monitor-
ing and enforcement—either via fiat or contract—unnecessary. If AI agents can, in fact,
coordinate and resolve incentive problems more efficiently than humans, this will have
profound consequences for economy-wide industry structure. A useful taxonomy here is
distinguish (i) economies of scale; (ii) economies of scope; and (iii) new industries which
do not yet exist. We discuss each in turn.
(i) Scale. A basic observation is that if a firm deploying AI agents enjoys falling marginal
costs, there is a natural tendency towards concentration. Why might AI agents drive
8
falling marginal costs? One possibility is that of automation feedback loops in which
as AI agents produce, they generate training data that can be used to improve their
production performance. Of course, there is a sense in which a version of this already
happens: tacit industry knowledge is passed down from managers to managers. Like-
wise, a related notion of data feedback loops has been studied in the context of predicting
demand or improving product quality (Jones and Tonetti, 2020; Farboodi and Veldkamp,
2021). But, as we have emphasized throughout this section, AI agents are distinct in
two regards: (i) they continually improve with additional data—even in the ‘big data’
regime where humans are saturated; and (ii) data and algorithmic improvements can
be duplicated at scale across different agents within the firm. 14 This qualitatively dis-
tinguishes automation feedback loops from using data to improve prediction which runs
into diminishing returns (Bajari et al., 2019).
(ii) Scope. The introduction of AI agents into production might also lead firms to ex-
pand into new industries. There are at least two mechanisms through which this could
happen. The first is technical: AI agents might become quite good at transfer learn-
ing—their training and expertise in one domain might generalize to others. (Indeed,
this is one way of describing the fundamental goal of building artificial general intelli-
gence.) The second is economic: AI agents might dramatically reduce coordination costs,
allowing firms to hold a wider set of capabilities (Wernerfelt, 1984) that can deliver com-
petitive advantages in a vast array of markets. Chen, Elliott, and Koh (2023) develop a
model of capability formation in which firms can endogenously merge (combining their
capabilities) or split (partitioning them). As AI drives down the organizational costs
of maintaining disparate capabilities, and as distinct markets begin to value similar
capabilities—e.g., because of transfer learning—the economy undergoes a sudden phase
transition from having many specialized firms, to a few large firms operating across
vast array of different industries. Of course, the ensuing welfare implications are un-
clear since large firms need not imply market power, and market power need not imply
consumer harm.
(iii) New markets. AI agents could dramatically speed up R&D which might lead to new
product varieties within existing markets, as well as unlock new markets. Indeed, AI re-
searchers put substantial probability on R&D being fully automated (Grace et al., 2024).
Gans (2025) offers a model of how scientists might leverage AI tools that excel at inter-
polating between known domains e.g., via recombination of existing ideas (Weitzman,
1998; Agrawal et al., 2024). But a different possibility is that AI agents might be able
to autonomously (i.e., without a human scientist) push the frontier of basic science, gen-
erating genuinely new ideas. This is the 4th stage of OpenAI’s predicted developmental
timeline for AI (Metz, 2024): AI capable of independently generating novel ideas, de-
signs and solutions. How will this shape product variety and quality? What is more, the
dynamics of AI-driven R&D can have stark and sometimes unintuitive implications. For
instance, modern endogenous growth models imply explosive growth as long as there are
no steeply decreasing returns to R&D (Trammell, 2025). What, if anything, are the fun-
damental differences between human and AI scientists, and how do these differences
translate into our growth models (Romer, 1986)?
3.2 AI agents within the firm. A basic question is how firms might introduce AI
agents into their workflow, and how this changes the structure of organizations.
14 Indeed, this is the founding goal of a number of Silicon Valley startups; seehttps://www.nytimes.
com/2025/06/11/technology/ai-mechanize-jobs.html.
9
AI agents might reshape team production for complicated processes requiring input
from multiple agents. A classic obstacle here is moral hazard where team members
might be tempted to shirk (Holmstrom, 1982). AI agents introduce a novel dimension
to this problem. On the one hand, they can be designed with the goal of eliminating
incentives to shirk. On the other, they might be more difficult for humans to control
or coordinate with because of communication frictions and the alignment and opacity
challenges of advanced AI. Moreover, AI agents might work better with other AI agents,
perhaps due to their greater capacity to monitor and discipline agents that act with
superhuman speed and/or complexity. (For example, AI agents might have opportuni-
ties to cheat using mechanisms that are undetectable to human agents (Motwani et al.,
2024).) How then should firms structure team production to integrate AI agents? How
should we configure who workers interact with, and how is this shaped by differential
coordination costs for human-human, human-AI, and AI-AI relationships?15
AI agents might also make systematically different errors from humans. How then
should decision-making be structured? Zhong (2025) analyzes a model where each agent
along a decision-making chain might either correct existing errors or introduce new
ones. In binary decision problems where the right action is known (but execution might
introduce errors), a simple score—the ratio of each agent’s probability of correcting er-
rors to the probability of introducing a new error—determines the optimal ordering:
agents with higher scores make decisions later because they are less likely to introduce
new errors. Given the current state of AI development, these final decision makers
are likely to be human. But there is nothing inevitable about this. Further develop-
ments could reverse the optimal ordering of decision-making and lead to AIs as the final
decision-maker, or even leave humans out entirely. 16 How much efficiency do we give
up if we are constrained to have humans make final decisions? How might externali-
ties, in the evaluation of what counts as an ‘error’ and the prediction of relative error
rates, affect the economy-wide impact of the allocation of decision authority within the
AI-enhanced firm?
3.3 AI-AI cooperation within the firm. Contracts play a crucial role in sustaining
human cooperation within organizations. Might they also be useful in fostering AI-
AI cooperation? Haupt et al. (2022) shows that augmenting reinforcement learners by
allowing them to write formal contracts with each other improves cooperation. But
contracts in the real-world are often beset by incompleteness and non-enforceability so
humans enter into relational contracts—webs of informal agreements and norms that
are not formally enforceable, but nonetheless generate incentives via the value of the fu-
ture relationship (Macaulay, 1963). These contracts play a key role within firms (Baker
et al., 2002), in part because they are adaptable and do not require all contingencies to
be specified in advance—humans are able to ‘fill in the gaps’ via shared norms (Macneil,
1973). How might we build AI agents that are similarly normatively competent (K ¨oster
et al., 2022)? Moreover, monetary transfers typically underpin relational contracts, and
it is this flexibility to ‘transfer utility’ that drives its efficiency (Levin, 2003). But AI
agents are, at present, typically trained to optimize narrow goals (e.g., number of cus-
tomers served). How might we build infrastructure e.g., some form of record-keeping or
money to achieve the same with artificial agents?
15 Dasaratha, Golub, and Shah (2024) develop an analysis of how team production and contracts should
be jointly designed to ameliorate moral hazard in teams.
16 For instance, Agarwal, Moehring, and Wolitzky (2025) run a fact-checking experiment and find that
full delegation to AI outperforms human + AI combinations.
10
3.4 Systemic fragility. Over the past decade, economists have analyzed how small
shocks might be amplified and propagate across the economy. The increasing adoption
of AI agents within the firm might exacerbate such fragility. A straightforward chan-
nel is that the errors introduced by AI agents might be more correlated than those of
humans. This might arise because the same agent is ‘copied’ both within and between
firms, inducing correlated mistakes that do not wash out in the aggregate. For instance,
automated trading algorithms likely exacerbated the 2010 ‘Flash Crash’ that wiped out
approximately $1 trillion over the span of 15 minutes (Kirilenko et al., 2017).17 Further-
more, how AI agents behave—especially in complex ‘out of sample’ environments—is
still poorly understood. This poses a challenge for models of systemic fragility which typ-
ically start from a fully-specified model of how agents learn and optimize, then studies
emergent behavior e.g., cascading financial or supply-chain failures (Elliott and Golub,
2022). How might we analyze an economy of opaque ‘black box’ agents in a ‘detail-free’
way? How should we robustly intervene to safeguard against fragility?
4 Institutions for AI agents
Well-functioning markets only exist in the presence of a host of legal rules (Hadfield,
2022). The very idea of voluntary trade, including those separated by time and through
agents, presumes the basic structures of property, contract, and agency law. Firms are
fictional entities created by corporate law. The regulatory state which acts to correct
market failures relies on a robust legal framework that shapes both incentives and infor-
mation through mechanisms such as taxes, administrative fines, professional licensing,
pre-market approval regimes, and disclosure law. Moreover, private actors within mar-
kets form organizations and institutions that help to resolve incentive problems such
as by keeping records of past behavior or creating excludable clubs to facilitate trade
through reputation or enforcement. Such private solutions to market failures played
a significant role in the commercial revolution prior to the emergence of the regulatory
state (Greif et al., 1994; Milgrom et al., 1990). But these institutional regimes were built
by and for human agents. We will need to build digital institutions that can structure
and adjudicate transactions for AI agents (Trivedi et al., 2025). Here we discuss some
of the institutional questions of particular relevance to economists.
4.1 Agent identity, registration, and records. It is easy to take for granted funda-
mental ways in which human agents are identified and legally recognized so as to facil-
itate the constellation of legal rules and institutions that support the market economy.
But human identity is a legal construct that emerged with the growth of trade and cities,
that is, once communities no longer relied exclusively on interactions with well-known
locals. As early as the 4th century B.C.E. the Qin dynasty imposed legal surnames on
the population to facilitate taxation (as well as forced labor and conscription) (Scott,
1998). The Ancient Athenians created a legal concept of citizenship–available to na-
tive Athenian males (legitimately born to two Athenian parents) who had been properly
registered in the same village unit to which their father belonged (Manville, 1990); cit-
izenship was required for, among other things, legal ownership of land and access to
courts to enforce contracts or other rights. Today, legal registration of births and deaths
and identity systems (such as social security numbers and drivers licenses) is a pre-
condition for individuals to access the legal system and other benefits and protections of
17 They find that automated market makers had limited risk-bearing capacity compared to traditional
market makers, and this stopped them from accommodating the large selling pressure.
11
the state as well as many private services. Firms are required to register with a state
in order to sue and be sued in its courts, necessary to induce willingness on both sides
to enter into a contract. Even market-based institutions, such as credit rating agencies,
could not function without legally defined identity and registration regimes.
Such identity and registration infrastructure are currently missing for AI agents (Had-
field, 2025; Chan et al., 2025). Building them out will be essential, but their design
raises questions around legal accountability. One possible route is to require that any
AI agent entering into a contract or transaction be registered to a formally identified
human (entity) who is legally accountable for any and all of the agent’s actions. But
this raises legal and incentive challenges. Few legal regimes of accountability impose
liability on a person or organization for actions that were not foreseeable by them or
which are beyond their control to avoid. Even strict product liability regimes evolve
limitations and carve-outs for harms caused by unforeseeable behavior by consumers
or intervening causes an actor could not foresee or control. At the same time, conven-
tional human agency rules limit the liability of the principal to actions that were within
the scope of the agent’s actual or apparent authority. The trajectory of technological
development is towards evermore general instructions (“go make $1 million”) and it is
unclear what technological capacity users will have to reliably implement controls on
what an agent can and cannot do. Creating new liability and agency rules for AI agents
will likely be necessary and will have implications for the incentives of AI developers
and the processes that emerge for the creation of an AI agent from a base model.
A second possible route for AI agent accountability is to follow the model of the emer-
gence of the corporation, which is another artificial entity that participates in the econ-
omy. AI agents could be accorded legal personhood, meaning they could sue and be
sued in their own ‘name’ in court. Clearly such an approach would require the creation
of regimes requiring agents to have assets in their own ‘name’, under their ‘control,’
and capable of being seized by a court (or comparable digital institution) to satisfy legal
judgments for damages. Such a regime would have implications again for the design and
deployment of AI agents and the efficiency of transactions and contract design involving
AI agents.
Beyond questions of liability, we face further choices as to how finely records about
agents’ past behavior should be designed. Should an AI agent that has (perhaps by acci-
dent) violated a previous contract be permanently blacklisted? A basic insight from eco-
nomics and game theory is that record-keeping institutions can allow agents to sustain
cooperation since bad behavior can be observed and punished by future trading part-
ners (Kandori, 1992; Clark, Fudenberg, and Wolitzky, 2021). But the value of long-lived
record-keeping is ambiguous—censoring or erasing records might improve the payoffs of
short-run players (Pei, 2024), prevent inefficient herding on a few agents with long and
favorable records (Koh and Li, 2025), and perhaps sustain cooperation more robustly
(Aumann and Sorin, 1989; Bhaskar, Mailath, and Morris, 2013). And, in the absence
of robust record-keeping infrastructure, AI agents might be able to erase or falsify their
records. Pei (2025) studies community enforcement with record manipulation and shows
that cooperation always breaks down with long-lived players, but can sometimes be sus-
tained when they are ‘medium-lived’. When we build out agent infrastructure, what
kinds of records do we want to make difficult to erase and/or fake? Should we build
infrastructure that allows artificial agents to trade their records, thereby creating a
‘market for reputation’ (Tadelis, 2002)?
12
4.2 Agent licensing and regulation. What kinds of market failures might be distinct
to AI agents and how might policymakers deal with them? We have introduced the core
challenge of alignment: general purpose AI agents are likely to behave in especially
unpredictable ways which are hard to control through our familiar contracting mech-
anisms (Hadfield-Menell and Hadfield, 2019). The dynamics of multiagent interaction
will, for perhaps a long time to come, also be hard to predict (Hammond et al., 2025).
We should anticipate, therefore, that governments may well want to regulate agents,
establishing minimum technological standards for how they are trained and tested be-
fore deployment. A digital analog of occupational licensing may be necessary for market
efficiency, requiring specialized training and finetuning techniques to be implemented
for agents participating in specific contexts, such as law, critical infrastructure manage-
ment, or finance. Agents may need to be built to participate only in approved transac-
tional protocols or on approved platforms, allowing monitoring or requiring disclosure
of information to other agents. But how should licensing and regulation be carried out?
By public actors or private entities (Hadfield and Clark, 2023)? How should regulations
adapt as agent capabilities evolve, and as we learn more about their promises and per-
ils (Bengio et al., 2024; Koh and Sanguanmoo, 2024)? Might some agents be simply too
dangerous to allow market access, given the limits of human capacity to monitor and
control agent behavior (Cohen et al., 2024)? Economists have developed a rich toolkit
for understanding regulation through the lens of incentives (Laffont and Tirole, 1993)
that can be brought to bear on such questions.
4.3 Rethinking the legal boundaries of the corporation. The corporation is a legal
fiction that has played a central role in economic history and development. One fea-
ture we take for granted is the proprietary nature of inventions and information that
the firm chooses to retain internally, protected by trade secret law, employee fiduciary
obligations, and enforceable confidentiality agreements. Ownership of the intellectual
property generated by the firm support investment and innovation. But how well does
this economic rationale for the firm hold up in the context of AI agents?
AI agents are built on foundation models (Bommasani et al., 2021), the most advanced
of which are built inside private firms. This renders them doubly-inscrutable. As we
have already emphasized, we do not understand why or how massive neural networks
function, and the mapping from inputs (data and training procedures) to model outputs
is mysterious and based largely on trial-and-error. And because frontier models are now
trained with considerable secrecy within private labs, we don’t even know what goes
into such models. Nor are smaller open-weight models good guides—they simply do not
display the capabilities and behaviors of larger models (Kaplan et al., 2020).
This presents a serious challenge to our regulatory and legal institutions. At present,
regulatory implications do not feature as a significant consideration in the legal design
of the boundary of the firm. After all, regulators don’t need access to the internal pro-
cesses of automobile or pharmaceutical manufacturers in order to assess their safety
and performance—they can simply test the final products or draw on public domain sci-
ence to evaluate them. But the massive AI models developed in commercial labs cannot
be replicated and evaluated in government or academic labs: the costs of training are
too high and evaluation requires access not only to model outputs but also inputs—their
data and training procedures.
For these reasons, governments and the academic researchers that can contribute public
domain knowledge to regulatory efforts will need access to information that is now con-
13
sidered proprietary to the firm. Regulators in other domains, of course, routinely gain
access to
```
