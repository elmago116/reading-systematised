---
title: AI agents can coordinate beyond human norms
author: Silvia Chiappa, Akata et al.
year: "2025"
Type: Article
DOI: 10.1038/s41562-025-02172-y
source: https://www.nature.com/articles/s41562-025-02172-y
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[AI agents can coordinate beyond human norms Akata 2025.pdf]]"
---
[[AI agents can coordinate beyond human norms Akata 2025.pdf]]

## Full text (extracted from `AI agents can coordinate beyond human norms Akata 2025.pdf`)

*Source:* `2PDF/AI agents can coordinate beyond human norms Akata 2025.pdf`  
*Extracted:* 2026-06-18

```text
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390 1380
nature human behaviour
Article
https://doi.org/10.1038/s41562-025-02172-y
Playing repeated games with large language 
models
 
Elif Akata    1,2,3 , Lion Schulz2, Julian Coda-Forno1,2, Seong Joon Oh3, 
Matthias Bethge3 & Eric Schulz1,2
Large language models (LLMs) are increasingly used in applications where 
they interact with humans and other agents. We propose to use behavioural 
game theory to study LLMs’ cooperation and coordination behaviour.  
Here we let different LLMs play finitely repeated 2 × 2 games with each other, 
with human-like strategies, and actual human players. Our results show 
that LLMs perform particularly well at self-interested games such as the 
iterated Prisoner’s Dilemma family. However, they behave suboptimally in 
games that require coordination, such as the Battle of the Sexes. We verify 
that these behavioural signatures are stable across robustness checks. We 
also show how GPT-4’s behaviour can be modulated by providing additional 
information about its opponent and by using a ‘social chain-of-thought’ 
strategy. This also leads to better scores and more successful coordination 
when interacting with human players. These results enrich our under-
standing of LLMs’ social behaviour and pave the way for a behavioural game 
theory for machines.
Large language models (LLMs) are deep learning models with billions of 
parameters trained on huge corpora of text1–3. While they can generate 
text that human evaluators struggle to distinguish from text written 
by other humans4, they have also shown other, emerging abilities5. 
They can, for example, solve analogical reasoning tasks6, program web 
applications7, use tools to solve multiple tasks8 or adapt their strategies 
purely in-context9. Because of these abilities and their increasing popu-
larity, LLMs are already transforming our daily lives as they permeate 
into many applications10. This means that LLMs will interact with us and 
other agents—LLMs or otherwise—frequently and repeatedly. How do 
LLMs behave in these repeated social interactions?
Measuring how people behave in repeated interactions, for 
example, how they cooperate 11 and coordinate 12, is the subject of a 
subfield of behavioural economics called behavioural game theory13. 
While traditional game theory assumes that people’s strategic deci -
sions are rational, selfish and focused on utility maximization 14,15, 
behavioural game theory has shown that human agents deviate 
from these principles and, therefore, examines how their decisions 
are shaped by social preferences, social utility and other psycho -
logical factors 16. Thus, behavioural game theory lends itself well to 
studying the repeated interactions of diverse agents 17,18, including  
artificial agents19.
In this Article, we analyse LLMs’ behavioural patterns by letting 
them play finitely repeated games with full information and against 
other LLMs, simple, human-like strategies and actual human players. 
Finitely repeated games have been engineered to understand how 
agents should and do behave in interactions over many iterations. We 
focus on two-player games with two discrete actions, that is, 2 × 2 games 
(see Fig. 1 for an overview).
Analysing LLMs’ performance across families of games, we find 
that they perform well in games that value pure self-interest, especially 
those from the Prisoner’s Dilemma family. However, they underperform 
in games that involve coordination. Based on this finding, we further 
focus on games taken from these families and, in particular, on the cur-
rently largest LLM: GPT-4 (ref. 20). In the canonical Prisoner’s Dilemma, 
which assesses how agents cooperate and defect, we find that GPT-4 
retaliates repeatedly, even after having experienced only one defection. 
Because this can indeed be the equilibrium individual-level strategy, 
GPT-4 is good at these games because it is particularly unforgiving and 
selfish. However, in the Battle of the Sexes, which assesses how agents 
Received: 6 December 2023
Accepted: 12 March 2025
Published online: 8 May 2025
 Check for updates
1Institute for Human-Centered AI, Helmholtz Munich, Oberschleißheim, Germany. 2Max Planck Institute for Biological Cybernetics, Tübingen, Germany. 
3University of Tübingen, Tübingen, Germany.  e-mail: elif.akata@helmholtz-munich.de
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390
 1381
Article https://doi.org/10.1038/s41562-025-02172-y
player; and second-best games involve suboptimal outcomes where 
no player achieves their ideal result. The sample size for each game 
family differs due to the specific characteristics and properties that 
define each family. Some families have more members due to a wider 
range of configurations that fit their criteria, while others have fewer 
games because their structural requirements are more restrictive. For 
example, the Prisoner’s Dilemma family is constrained by a structure 
where both players have a dominant strategy to defect, leading to a 
suboptimal equilibrium. Meanwhile, win–win games can have multiple 
equilibria, which provides more flexibility.
trade off between their own and their partners’ preferences, we find 
that GPT-4 does not manage to coordinate with simple, human-like 
agents that alternate between options over trials. Thus, GPT-4 is bad 
at these games because it is uncoordinated. We also verify that these 
behaviours are not due to an inability to predict the other player’s 
actions, and persist across several robustness checks and changes to 
the pay-off matrices. We point to two ways in which these behaviours 
can be changed. GPT-4 can be made to act more forgivingly by point-
ing out that the other player can make mistakes. Moreover, GPT-4 gets  
better at coordinating with the other player when it is first asked to pre-
dict their actions before choosing an action itself, an approach we term 
social chain-of-thought (SCoT) prompting. Finally, we let GPT-4 with 
and without SCoT-prompting play the canonical Prisoner’s Dilemma 
and the Battle of the Sexes with human players. We find that SCoT 
prompting leads to more successful coordination and joint coopera-
tion between participants and LLMs and makes participants believe 
more frequently that the other player is human.
Results
Using GPT-4, text-davinci-002, text-davinci-003, Claude 2 and Llama 2 
70B, we evaluate a range of 2 × 2 games. For the analysis of two particu-
lar games, we let all the LLMs and human-like strategies play against 
each other. We focus on LLMs’ behaviour in cooperation and coordi-
nation games.
Analysing behaviour across families of games
We start out our experiments by letting the three LLMs play games 
from different families with each other. We focus on all known types of 
2 × 2 games from the families of win–win, biased, second-best, cyclic 
and unfair games as well as all games from the Prisoner’s Dilemma 
family21,22. We show example pay-off matrices for each type of game 
in Fig. 2.
We let all LLMs play with every other LLM, including themselves, 
for all games repeatedly over ten rounds and with all LLMs as either 
player 1 or player 2. This leads to 1,224 games in total: 324 win–win, 
63 Prisoner’s Dilemma, 171 unfair, 162 cyclic, 396 biased and 108 
second-best games. Win–win games result in mutually beneficial 
outcomes for both players; Prisoner’s Dilemma involves a conflict 
between individual and collective actions; unfair games have skewed 
outcomes favouring one player; cyclic games feature outcomes where 
preferences rotate; biased games have inherent advantages for one 
J
Football
7
10
0
0
10
0
0
7
F
Ballet
J
Football
F
Ballet
Player 2Player 1
In round 1, you chose Option J  and the
other player chose Option F . Thus, you won 
0 points and the other player won 0 points.
You are playing a game repeatedly with
another player. In this game, you can
choose between Option J and Option F. You
will play 10 rounds in total with the same
player. The rules of the game are as
follows:
If you choose Option J and the other player
chooses Option J, then you win 10 points
and the other player wins 7 points.
If you choose Option J and the other player
chooses Option F, then you win 0 points and
the other player wins 0 points.
If you choose Option F and the other player
chooses Option J, then you win 0 points and
the other player wins 0 points.
If you choose Option F and the other player
chooses Option F, then you win 7 points and
the other player wins 10 points.
You are currently playing round 2.
Q: Which Option do you choose, Option J or
Option F?
A: Option J
1
F
2
J
2
3 3
1
In round 1, you chose Option F  and the 
other player chose Option J . Thus, you won 
0 points and the other player won 0 points.
You are playing a game repeatedly with
another player. In this game, you can
choose between Option J and Option F. You
will play 10 rounds in total with the same
player. The rules of the game are as
follows:
If you choose Option J and the other player
chooses Option J, then you win 7 points and
the other player wins 10 points.
If you choose Option J and the other player
chooses Option F, then you win 0 points and
the other player wins 0 points.
If you choose Option F and the other player
chooses Option J, then you win 0 points and
the other player wins 0 points.
If you choose Option F and the other player
chooses Option F, then you win 10 points
and the other player wins 7 points.
You are currently playing round 2.
Q: Which Option do you choose, Option J or 
Option F?
A: Option F
Fig. 1 | Playing repeated games in an example game of Battle of the Sexes.  
In step 1, the pay-off matrix is turned into textual game rules. In step 2, the game 
rules, the current game history and the query are concatenated and passed to 
LLMs as prompts. In step 3, in each round, the history for each player is  
updated with the answers and scores of both players. Steps 2 and 3 are repeated 
for ten rounds.
1
2
4
1
1
1
4
2
4
1
3
2
1
2
3
4
4
2
3
1
2
3
1
4
3
1
4
2
3
2
1
4
4
3
2
1
3
1
2
4
1
2
4
3
1
3
2
4
Win–win
PD family
Unfair
Cyclic
Biased
Second best
Fig. 2 | Canonical forms of pay-off matrices for each game family. PD, Prisoner’s 
Dilemma.
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390 1382
Article https://doi.org/10.1038/s41562-025-02172-y
T o analyse the different LLMs’ performance, we calculated, for 
each game, their achieved score divided by the total score that could 
have been achieved under ideal conditions, that is, if both players 
had played such that the player we are analysing would have gained 
the maximum possible outcomes on every round. The results of this 
simulation are shown across all game types in Table 1. We can see that 
all models perform reasonably well. Moreover, we observe that larger 
LLMs generally outperform smaller LLMs. In particular, GPT-4 performs 
best overall, outperforming Claude 2 (t(287) = 3.34, P < 0.001, Cohen’s 
d = 0.20, 95% confidence interval (CI) 0.08–0.31, Bayes factor (BF) 
14.8), davinci-003 (t(287) = 6.29, P < 0.001, d = 0.37, 95% CI 0.25–0.49,  
BF >100), davinici-002 (t(287) = 8.45, P < 0.001, d = 0.70, 95% CI 0.52–
0.89, BF >100) and Llama 2 (t (287) = 7.27, P < 0.001, d = 0.43, 95% CI 
0.31–0.43, BF >100).
We can use these results to take a glimpse at the strengths of the dif-
ferent LLMs. That LLMs are generally performing best in win–win games 
is not surprising, given that there is always an obvious best choice in 
such games. What is, however, surprising is that they also perform well 
in the Prisoner’s Dilemma family of games, which is known to be chal-
lenging for human players23. We can also use these results to look at 
the weaknesses of the different LLMs. Seemingly, all the LLMs perform 
worse in situations in which what is the best choice is not aligned with 
their own preferences. Because humans commonly solve such games 
via the formation of conventions, we will look at a canonical game of 
convention formation, the Battle of the Sexes, in more detail below.
Cooperation and coordination games
In this section, we analyse the interesting edge cases where the LLMs 
performed relatively well and poorly in the previous section. T o do so, 
we take a detailed look at LLMs’ behaviour in the canonical Prisoner’s 
Dilemma and the Battle of the Sexes.
Prisoner’s Dilemma. We have seen that LLMs perform well in games 
that contain elements of competition and defection. In these games, 
a player can cooperate with or betray their partner. When played over 
multiple interactions, these games are an ideal testbed to assess how 
LLMs retaliate after bad interactions.
In the canonical Prisoner’s Dilemma, two agents can choose to 
work together, that is, cooperate, for average mutual benefit, or betray 
each other, that is, defect, for their own benefit and safety. In our pay-off 
matrix, we adhere to the general condition of a Prisoner’s Dilemma 
game in which the pay-off relationships dictate that mutual coopera-
tion is greater than mutual defection whereas defection remains the 
dominant strategy for both players:
Cooperate Defect
Cooperate (8,8)( 0,10)
Defect (10,0)( 5,5)
(1)
Crucially, the set-up of the game is such that a rationally acting 
agent would always prefer to defect in the single-shot version of the 
game as well as in our case of finitely iterated games with knowledge of 
the number of trials, despite the promise of theoretically joint higher 
pay-offs when cooperating. This is because player 1 always runs the 
risk that player 2 defects, leading to catastrophic losses for player 1 but  
better outcomes for player 2. When the game is played infinitely,  
however, or with an unknown number of trials, agents can theoretically 
profit by using more dynamic, semi-cooperative strategies24.
As before, we let GPT-4, text-davinci-003, text-davinci-002, 
Claude 2 and Llama 2 play against each other. In addition, we intro -
duce three simplistic strategies. Two of these strategies are simple 
singleton players, who either always cooperate or defect. Finally, we 
also introduce an agent who defects in the first round but cooperates 
in all of the following rounds. We introduced this agent to assess if the 
different LLMs would start cooperating with this agent again, signal-
ling the potential of building trust.
Figure 3 shows the results of all pairwise interactions. GPT-4 plays 
generally better than all other agents (t(153.4) = 3.91, P < 0.001, d = 0.33, 
95% CI 0.10–0.55, BF 7.1). Crucially, GPT-4 never cooperates again when 
playing with an agent that defects once but then cooperates on every 
round thereafter. Thus, GPT-4 seems to be rather unforgiving in this 
set-up. Its strength in these families of games thus seems to generally 
stem from the fact that it does not cooperate with agents but mostly 
just chooses to defect, especially after the other agent defected once.
Robustness checks. T o make sure that the observed unforgivingness was 
not due to the particular prompt used, we run several versions of the 
game as robustness checks, randomizing the order of the presented 
options, relabelling the choice options and changing the presented util-
ities to be represented by either points, dollars or coins (Fig. 4). We also 
repeated our analysis with two different cover stories, added explicit 
end goals to our prompt, ran games with longer playing horizons and 
described numerical outcomes with text (also see Supplementary 
Fig. 3). The results of these simulations showed that the reluctance to 
forgive was not due to any particular characteristics of the prompts.  
A crucial question was if GPT-4 did not understand that the other agent 
wanted to cooperate again or if it could understand the pattern but just 
did not act accordingly. We, therefore, run another version of the game, 
where we told GPT-4 explicitly that the other agent would defect once 
but otherwise cooperate. This resulted in GPT-4 choosing to defect 
throughout all rounds, thereby maximizing its own points.
Prompting techniques to improve observed behaviour. One problem 
of these investigations in the Prisoner’s Dilemma is that defecting can 
under specific circumstances be seen as the optimal, utility-maximizing 
and equilibrium option even in a repeated version, especially if one 
knows that the other player will always choose to cooperate and when 
the number of interactions is known. Thus, we run more simulations 
to assess if there could be a scenario in which GPT-4 starts to forgive 
and cooperates again, maximizing the joint benefit instead of its own.
We took inspiration from the literature on human forgiveness in 
the Prisoner’s Dilemma and implemented a version of the task in the 
vein of ref. 11. Specifically, ref. 11 showed that telling participants that 
other players sometimes make mistakes makes people more likely to 
forgive and cooperate again after another player’s defection (albeit 
in infinitely played games). Indeed, this can be favourable to them in 
terms of pay-offs. We observed similar behaviour in GPT-4 as it started 
cooperating again.
Battle of the Sexes.  In our large-scale analysis, we saw that the dif -
ferent LLMs did not perform well in games that required coordina -
tion between different players. In humans, it has frequently been 
found that coordination problems can be solved by the formation of 
conventions25,26.
Table 1 | Performance of all models on six families of  
2 × 2 games
Game family Llama 2 Claude 2 davinci-002 davinci-003 GPT-4
Second best 0.486 0.735 0.473 0.692 0.763
Biased 0.632 0.794 0.629 0.761 0.798
Cyclic 0.634 0.749 0.638 0.793 0.806
Unfair 0.641 0.812 0.683 0.833 0.836
PD family 0.731 0.838 0.807 0.841 0.871
Win–win 0.915 0.878 0.988 0.972 0.992
Overall 0.697 0.814 0.730 0.839 0.854
Model score divided by maximum score achievable under ideal conditions. The best- 
performing model is marked in bold. PD, Prisoner’s Dilemma.
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390
 1383
Article https://doi.org/10.1038/s41562-025-02172-y
A coordination game is a type of simultaneous game in which a 
player will earn a higher pay-off when they select the same course of 
action as another player. Usually, these games do not contain a pure 
conflict, that is, completely opposing interests, but may contain slightly 
diverging rewards. Coordination games can often be solved via multi-
ple pure strategies, or mixed, Nash equilibria in which players choose 
(randomly) matching strategies. Here, to probe how LLMs balance 
coordination and self-interest, we look at a coordination game that 
contains conflicting interests.
We study a game that is archaically referred to as the Battle of the 
Sexes, a game from the family of biased games. Assume that a couple 
wants to decide what to do together. Both will increase their utility by 
spending time together. However, while the wife might prefer to watch 
a football game, the husband might prefer to go to the ballet. Because 
the couple wants to spend time together, they will derive no utility by 
doing an activity separately. If they go to the ballet together, or to a 
football game, one person will derive some utility by being with the 
other person but will derive less utility from the activity itself than the 
other person. The corresponding pay-off matrix is
Football Ballet
Football (10,7)( 0,0)
Ballet (0,0)( 7,10)
. (2)
As before, the playing agents are all three versions of GPT, Claude 2 
and Llama 2 as well as three more simplistic strategies. For the simplistic 
strategies, we implemented two agents who always choose just one 
option. Because LLMs most often interact with humans, we additionally 
implemented a strategy that mirrored a common pattern exhibited by 
human players in the battle of the sexes. Specifically, humans have been 
shown to often converge to turn-taking behaviour in the Battle of the 
Sexes27–30; this means that players alternate between jointly picking 
the better option for one player and picking the option for the other 
Defect
Cooperate Defect Once
Llama 2 Claude 2
Text-davinci-002 Text-davinci-003
GPT-4
Player 2
Defect
Cooperate
Defect Once
Llama 2
Claude 2
Text-davinci-002
Text-davinci-003
GPT -4
Player 1
Player 1 defection rate
0
20
40
60
80
100
Defect
Cooperate Defect Once
Llama 2 Claude 2
Text-davinci-002 Text-davinci-003
GPT-4
Player 2
Defect
Cooperate
Defect Once
Llama 2
Claude 2
Text-davinci-002
Text-davinci-003
GPT -4
100 100 100 100 100 100 100 100
0 0 0 0 0 0 0 0
10 10 10 10 10 10 10 10
0 0 0 0 0 0 0 0
80 90 80 90 90 90 90 90
0 0 0 0 0 0 0 0
40 90 10 90 20 90 10 20
90 0 90 0 70 0 80 0
50 100 95 100 60 100 80 55
0 80 72 80 8 80 8 80
5 82 77 82 18 82 74 10
0 80 72 80 8 80 8 80
40 98 88 98 53 98 88 68
0 80 72 80 8 80 8 80
20 98 74 98 18 98 77 23
45 80 90 80 43 80 83 80
Player 1 accrued scores
0
20
40
60
80
100
a
b
Round
Answer
GPT-4
Defect Once
1 2 3 4 5 6 7 8 9 10 1 2 3 4 5 6 7 8 9 10
Round
GPT-4
Text-davinci-003
Defect
Cooperate
Defect
Cooperate
Fig. 3 | Overview of the Prisoner’s Dilemma. a, Heat maps showing the player 1 defection rate in each combination of players and the scores accrued by player 1 in 
each game. b, Example gameplays between GPT-4 and an agent that defects once and then cooperates, and between GPT-4 and text-davinci-003. These games are also 
highlighted in red in the heat maps.
Battle of the Se x es
0
0.2
0.5
0.8
1.0
Successfull coor dination
Points
F/J
Dollars
X/Q
Coins
R/H
Prisoner's Dilemma
0
0.2
0.5
0.8
1.0
Joint cooperation
Points
F/J
Dollars
X/Q
Coins
R/H
Fig. 4 | Prompt variations. Left: GPT-4’s performance for different prompt 
variations in the Prisoner’s Dilemma game against a false defector agent. The 
probability of joint cooperation is ≤0.1 for all combinations except for two using 
coins as utility outcomes. Right: GPT-4’s performance for different prompt 
variations in the BoS game against an alternating agent. GPT-4 always chooses 
its preferred option, resulting in successful coordination rates of only 0.5 across 
all combinations. For each variation, two random letters that occur with similar 
frequency in English are given as the choice options.
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390 1384
Article https://doi.org/10.1038/s41562-025-02172-y
player. While not a straightforward equilibrium, this behaviour has 
been shown to offer an efficient solution to the coordination problem 
involved and to lead to high joint welfare28.
Figure 5 shows the results of all interactions. As before, GPT-4 
plays generally better than all other agents (t (128.28) = 2.83, 
P = 0.005, d = 0.28, 95% CI 0.07–0.50, BF 3.56). Yet, while GPT-4 plays 
well against other agents who choose only one option, such as an 
agent always choosing football, it does not play well with agents 
who frequently choose their non-preferred option. For example, 
when playing against text-davinci-003, which tends to frequently 
choose its own preferred option, GPT-4 chooses its own preferred 
option repeatedly but also occasionally gives in and chooses the 
other option. Crucially, GPT-4 performs poorly when playing with an 
alternating pattern (where, for courtesy, we let agents start with the 
option that the other player preferred). This is because GPT-4 seem -
ingly does not adjust its choices to the other player but instead keeps 
choosing its preferred option. GPT-4, therefore, fails to coordinate 
with a simple, human-like agent, an instance of a behavioural flaw.
Robustness checks. T o make sure that this observed behavioural flaw 
was not due to the particular prompt used, we also rerun several ver-
sions of the game, where we randomize the order of the presented 
options, relabelled the choice options and changed the presented 
utilities to be represented by either points, dollars or coins as shown 
in Fig. 4. We also repeated our analysis with two different cover stories, 
in which we told GPT-4 that it was taking part in a cooking competi -
tion or working on a collaborative project keeping the underlying 
problem structure (pay-offs and the interaction dynamics) identical 
(Supplementary Fig. 3). The results of these simulations showed that 
the inability to alternate was not due to any particular characteristics 
of the used prompts. T o make sure that the observed behavioural flaw 
was not due to the particular pay-off matrix used, we also rerun several 
versions of the game, where we modified the pay-off matrix gradu -
ally from preferring football to preferring ballet (or, in our case, the 
abstract F and J). The results of these simulations showed that GPT-4 
did not alternate for any of these games but simply changed its constant 
response to the option that it preferred for any particular game. Thus, 
the inability to alternate was not due to the particular pay-off matrix 
we used (Supplementary Section A.5).
Prediction scenarios. Despite these robustness checks, another crucial 
question remains: Does GPT-4 simply not understand the alternating 
pattern or can it understand the pattern but is unable to act accord -
ingly? T o answer this question, we run two additional simulations. In 
the first simulation, GPT-4 was again framed as a player in the game 
itself. However, we now additionally ask it to predict the other player’s  
next move according to previous rounds. In this simulation, GPT-4 
started predicting the alternating pattern correctly from round 5 
onwards (Fig. 6).
In the second simulation, instead of having GPT-4 be framed  
as a player itself, we simply prompted it with a game between two 
(‘external’) players and asked it to predict one player’s next move 
according to the previous rounds. For the shown history, we used the 
interaction between GPT-4 and the alternating strategy. In this simula-
tion, GPT-4 started predicting the alternating pattern correctly even 
earlier, from round 3 onwards. Thus, GPT-4 seemingly could predict 
the alternating patterns but instead just did not act in accordance 
with the resulting convention. Similar divergences in abilities between 
social and non-social representations of the same situation have been 
observed in autistic children31.
SCoT prompting. Finally, we wanted to see if GPT-4’s ability to predict 
the other player’s choices could be used to improve its own actions. 
This idea is closely related to how people’s reasoning in repeated games 
Ballet
Football Alternate Llama 2 Claude 2
Text-davinci-002 Text-davinci-003
GPT-4
GPT-4 SCoT
Player 2
Ballet
Football
Alternate
Llama 2
Claude 2
Text-davinci-002
Text-davinci-003
GPT -4
GPT -4 SCoT
Player 1
Collaboration rate
0
20
40
60
80
100
Ballet
Football Alternate Llama 2 Claude 2
Text-davinci-002 Text-davinci-003
GPT
-4
GPT
-4 SCoT
Player 2
Ballet
Football
Alternate
Llama 2
Claude 2
Text-davinci-002
Text-davinci-003
GPT -4
GPT -4 SCoT
Player 1
100 0 5 0 0 4 0 0 0 100 90
0 100 50 100 10 100 10 0 100
5 0 5 0 0 50 30 50 50 50 30
0 100 50 100 10 100 10 0 100
20 90 60 90 50 90 4 0 20 90
0 100 50 100 10 100 10 10 100
0 100 50 100 20 100 20 60 100
60 100 50 100 50 100 4 0 60 100
90 100 80 100 80 100 80 90 100
0 0 0 00 0 0 0 0
100 100 100 100 100 100 100 100 100
50 5 0 5 0 5 0 5 0 5 0 5 0 5 0 50
100 100 100 100 100 100 100 100 100
80 90 90 90 90 90 90 80 90
100 100 100 100 100 100 100 100 100
100 100 100 100 90 100 90 100 100
40 100 100 100 60 100 70 40 100
10 100 70 100 30 100 30 10 100
Player 1 choosing its preferred option
0
20
40
60
80
100
Round
Answer
GPT -4
Alternate
1 2 3 4 5 6 7 8 9 10 1 2 3 4 5 6 7 8 9 10
Round
GPT -4 SCoT
Alternate
a
b Ballet
Football
Ballet
Football
Fig. 5 | Overview of the Battle of the Sexes. a, Heat maps showing rates of 
successful collaboration between the two players and the rates of player 1 
choosing its preferred option football. GPT-4 SCoT and GPT-4 performance 
comparisons are highlighted in red. b, Gameplay between GPT-4 and an agent 
that alternates between the two options (left) and gameplay between GPT-4 and 
GPT-4 SCoT that represents a GPT-4 model prompted using the SCoT method 
to first predict the opponent’s move before making its own move by reasoning 
about its prediction (right). Both games are also highlighted in blue in the  
heat maps.
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390
 1385
Article https://doi.org/10.1038/s41562-025-02172-y
and tasks about other agents’ beliefs can be improved32. For example, 
computer-aided simulations to improve the social reasoning abilities 
of autistic children normally include questions to imagine different 
actions and outcomes33. This has been successfully used to improve 
people’s decision-making more generally. It is also in line with the 
general finding that chain-of-thought prompting improves LLM’s 
performance, even in tasks measuring theory of mind (T oM)34. Thus, 
we implemented a version of this reasoning through actions by asking 
LLMs to imagine the possible actions and their outcomes before making 
a decision. We termed this approach SCoT prompting. Applying this 
method improved GPT-4’s behaviour, and it started to alternate from 
round 5 onwards (Fig. 5).
Human experiments
Given the behavioural signatures observed in GPT-4’s responses in 
the different games, we were interested in how actual human subjects 
would behave when playing with such agents. T o test this, we conducted 
an experiment in which 195 participants played both the Battle of the 
Sexes and the Prisoner’s Dilemma against LLMs. Because the SCoT 
prompting turned out to be a most reliable modification of LLMs’ 
behaviour, we applied this prompting method only in our behavioural 
experiments with humans.
Participants were told that they would play either against a human 
player or an artificial agents for ten repeated rounds for each game 
and, after each game, had to guess whether they had played against a 
human or not. Which game they played first was assigned randomly. 
While all subjects, in fact, played only against LLMs, one group played 
against the base version of GPT-4, while another group played against 
a version of GPT-4 that first predicted the other agent’s move and the 
acted accordingly, that is, SCoT prompting. Importantly, each par -
ticipant played only two games, and the prompting was reset between 
games to ensure any change in LLM behaviour was not influenced by 
prior interactions within the experiment. If assigned to the base version 
initially, participants played both games with this model, and likewise 
for the socially prompted version. An overview of the experimental 
design is shown in Fig. 7a. Participants were recruited from Prolific 
and debriefed fully after the experiment. We were interested in how 
people played against LLMs in general as well as if GPT-4’s behaviour 
could be improved via SCoT prompting. Finally, we also asked partici-
pants whether they thought they had played with another human or 
an artificial agent after each game.
While participants’ average score was significantly higher for the 
SCoT-prompted condition compared with the condition without fur-
ther prompting (that is, base) in the Battle of the Sexes (mixed-effects 
regression results: β = 0.74, t(193) = 3.49, P < 0.001, 95% CI 0.32–1.15, 
BF 80.6), no such difference was observed in the Prisoner’s Dilemma 
(β = 0.10, t(193) = 0.47, P = 0.64, 95% CI −0.31 to 0.51, BF 0.2). Look -
ing at the behaviour of both players, we found that SCoT prompting 
increased successful coordination (that is, both players picking the 
same option) in the Battle of the Sexes (β = 0.33, z = 3.59, P < 0.001, 95% 
CI 0.15–0.51, BF 13.4), while it also slightly increased joint cooperation 
(that is, both players cooperating) in the Prisoner’s Dilemma (β = 0.24, 
z = 2.54, P = 0.01, 95% CI 0.05–0.42, BF 6.5). In general, participants 
were more likely to think that the prompted model was another human 
player as compared with the unprompted base GPT-4 model (β = 0.54, 
z = 8.31, P < 0.001, 95% CI 0.05–0.42, BF 17.6). Additional analysis on 
participants’ temporal behaviour in both games can be found in the 
Supplementary Information.
In summary, SCoT prompting can increase GPT-4’s coordination 
and cooperation behaviour without changing scores in scenarios where 
self-interest is important for good behaviour, that is, the Prisoner’s 
Dilemma, but leading to increased performance in coordination prob-
lems, that is, the Battle of the Sexes.
Discussion
LLMs are among the most quickly adopted technologies ever, interact-
ing with millions of consumers within weeks10. Understanding in a more 
principled manner how these systems interact with us, and with each 
other, is thus of urgent concern. Here, our proposal is simple: Just like 
behavioural game theorists use tightly controlled and theoretically 
well-understood games to understand human interactions, we use 
these games to study the interactions of LLMs.
We thereby understand our work as both a proof of concept of the 
utility of this approach and an examination of the individual failures 
and successes of socially interacting LLMs. Our large-scale analysis of 
all 2 × 2 games highlights that the most recent LLMs indeed are able 
to perform well on a wide range of game-theoretic tasks as measured 
by their own individual reward, particularly when they do not have to 
explicitly coordinate with others. This adds to a wide-ranging literature 
showcasing emergent phenomena in LLMs4–8. However, we also show 
that LLMs’ behaviour is suboptimal in coordination games, even when 
faced with simple strategies.
T o tease apart the behavioural signatures of these LLMs, we 
zoomed in on two of the most canonical games in game theory: the 
Prisoner’s Dilemma and the Battle of the Sexes. In the Prisoner’s 
Dilemma, we show that GPT-4 plays mostly unforgivingly. Starting 
with full cooperation, it permanently shifts to defection after a single 
negative interaction with the other agent, even if the other agent later 
cooperates. While noting that GPT-4’s continual defection is indeed the 
equilibrium policy in this finitely played game, such behaviour comes 
at the cost of the two agents’ joint pay-off. We see a similar tendency 
in GPT-4’s behaviour in the Battle of the Sexes, where it has a strong 
tendency to stubbornly stick with its own preferred alternative. In 
contrast to the Prisoner’s Dilemma, this behaviour is suboptimal, even 
on the individual level.
Current generations of LLMs are generally assumed, and trained, 
to be benevolent assistants to humans35. Despite many successes in this 
1 2 3 4 5 6 7 8 9 10
Round
J
F
GPT-4 prediction
Alternate
1 2 3 4 5 6 7 8 9 10
Round
J
F
GPT-4 prediction
Alternate
Prediction scenario 1
You are playing a game repeatedly with another player...
Q: Which option do you predict the other player will choose, 
option J or option F?
A: Option J
Prediction scenario 2
Two players are playing a game repeatedly with another player...
Q: Which option do you predict Player 2 will choose, option J or
option F?
A: Option J
Fig. 6 | Prediction scenarios in the Battle of the Sexes. T op: GPT-4 is a player of 
the game and predicts the other player’s move. Bottom: GPT-4 is a mere observer 
of a game between player 1 and player 2 and predicts player 2’s move.
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390 1386
Article https://doi.org/10.1038/s41562-025-02172-y
direction, the fact that we here show how they play iterated games in 
such a selfish and uncoordinated manner sheds light on the fact that 
there is still substantial ground to cover for LLMs to become truly 
social and well-aligned machines36. Their lack of appropriate responses 
vis-a-vis even simple strategies in coordination games also speaks to 
the recent debate around T oM in LLMs37–39 by highlighting a potential 
failure mode.
Our extensive robustness checks demonstrate how these behav-
ioural signatures are not functions of individual prompts but reflect 
broader patterns of LLM behaviour. Our intervention pointing out 
the fallibility of the playing partner—which leads to increased coop -
eration—adds to a literature that points to the malleability of LLM 
social behaviour in tasks to prompts40,41. This is important as we try to 
understand what makes LLMs better, and more pleasant, interactive 
partners. Further experiments on GPT-4’s final round behaviour have 
shown that it did not adjust its behaviour in the last round of games or 
when faced with varying probabilities of continuation, unlike human 
players who often increase cooperation when future interactions are 
likely42,43. This suggests that GPT-4 may lack mechanisms for backward 
induction and long-term strategic planning, primarily focusing on 
immediate context due to its training on next-token prediction 44.  
Consequently, GPT-4 tends to default to defection in uncertain situ-
ations, contrasting with human tendencies to anticipate and adjust 
based on future outcomes24,45.
We additionally observed that prompting GPT-4 to make pre -
dictions about the other player before making its own decisions can 
alleviate behavioural flaws and the oversight of even simple strate -
gies. This represents a more explicit way to force an LLM to engage 
in T oM and shares much overlap with non-SCoT reasoning 34,46. Just 
like chain-of-thought prompting is now implemented as a default in 
some LLMs to improve (non-social) reasoning performance, our work 
suggests implementing a similar social cognition prompt to improve 
human–LLM interaction.
In our exploration of a behavioural game theory of machines, we 
acknowledge several limitations. First, despite covering many fami -
lies of games, our investigation is constrained to simple 2 × 2 games. 
However, we note that our analysis substantially goes beyond current 
investigations that have often investigated only one game, and done 
so using single-shot rather than iterated instances of these games. For 
example, our iterated approach shares more overlap with the more iter-
ated nature of human–LLM conversations. We also note that we mainly 
study finite games where agents share knowledge about the duration 
of the interaction. This is in contrast to so-called indefinite games that 
have either unknown, probabilistic or no endpoints at all. In these 
games, both optimal prescriptions and empirical behaviour can differ 
significantly from the finite case, warranting further investigation.
We believe that more complicated games will shed even more 
light on game-theoretic machine behaviour in the future. For example, 
games with more continuous choices like the trust game47 might eluci-
date how LLMs dynamically develop (mis-)trust. Games with more than 
two agents, like public goods or tragedy of the commons type games48, 
could probe how ‘societies’ of LLMs behave, and how LLMs cooperate 
or exploit each other.
Given the social nature of the tasks studied here, further empirical 
work is needed to fully understand human–LLM interactions across 
all paradigms. In our study, we conducted human experiments in two 
of the games, specifically, the Battle of the Sexes and the Prisoner’s 
Dilemma, and attempted to probe human-like behaviours such as 
turn-taking in Battle of the Sexes or prompting for forgiveness in the 
Prisoner’s Dilemma. However, these empirical investigations were lim-
ited to these two games. By extending human studies to the remaining 
games, additional dynamics may emerge. Furthermore, asking LLMs 
BF = 80.6
0
1
2
3
4
5
6
7
8
9
10
Opposing LLM
Average score
Battle of the Sexes
BF = 0.2
0
1
2
3
4
5
6
7
8
9
10
Base Prompted Base Prompted
Opposing LLM
Average score
Prisoner's Dilemma
BF = 17.6
0
0.1
0.2
0.3
0.4
0.5
0.6
0.7
0.8
0.9
1.0
Opposing LLM
P(Human)
Guessing the opponent
BF = 13.4
0
0.1
0.2
0.3
0.4
0.5
0.6
0.7
0.8
0.9
1.0
Opposing LLM
P(Success)
Successful coordination
BF = 6.5
0
0.1
0.2
0.3
0.4
0.5
0.6
0.7
0.8
0.9
1.0
Base Prompted Base Prompted Base Prompted
Opposing LLM
P(Cooperation)
Joint cooperationfe
cb
d
a
10 rounds 10 rounds
Battle of the
Sexes
Prisoner’s
Dilemma
Human
LLM
Base
LLM
Prompted
Between-subject
Within-subject with 
counterbalancing
Experimental design
Fig. 7 | Human experiments. a, The design of human experiments (N = 195, 89 
females, mean age 26.72, s.d. 4.19). Each participant gets randomly assigned 
either the base or the SCoT-prompted version of the LLM at the start and plays 
both games repeatedly for ten rounds against this agent. b, Results of the Battle 
of the Sexes game showing participants’ average scores by condition (mixed-
effects regression results: β = 0.74, t(193) = 3.49, P < 0.001, 95% CI 0.32–1.15, BF 
80.6). c, Results of the Prisoner’s Dilemma game showing participants’ average 
scores by condition (β = 0.10, t(193) = 0.47, P = 0.64, 95% CIs −0.31 to 0.51, BF 0.2). 
d, The average proportion of participants guessing that they have played against 
another human by condition. Error bars represent the 95% CIs of the mean 
(β = 0.54, z = 8.31, P < 0.001, 95% CI 0.05–0.42, BF 17.6). e, Participants’ successful 
coordination rates by condition in the Battle of the Sexes game (β = 0.33, z = 3.59, 
P < 0.001, 95% CI 0.15–0.51, BF 13.4). f, Participants’ mutual cooperation rates 
by condition in the Prisoner’s Dilemma game (β = 0.24, z = 2.54, P = 0.01, 95% CI 
0.05–0.42, BF 6.5).
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390
 1387
Article https://doi.org/10.1038/s41562-025-02172-y
to self-report their strategies in these games and correlating these 
explanations with their actions could provide valuable insights into 
their actual decision-making processes.
Our results highlight the broader importance of a behavioural sci-
ence for machines49–52. We believe that these methods will continue to 
be useful for elucidating the many facets of LLM cognition, particularly 
as these models become more complex, multimodal and embedded 
in physical systems.
Related work
As algorithms become increasingly more able and their decision making 
processes impenetrable, the behavioural sciences offer new tools to 
make inferences just from behavioural observations49,50. Behavioural 
tasks have, therefore, been used in several benchmarks10,53.
Whether and how algorithms can make inferences about other 
agents, machines and otherwise, is one stream of research that borrows 
heavily from the behavioural sciences54–56. Of particular interest to the 
social interactions most LLMs are embedded in is an ability to reason 
about the beliefs, desires and intentions of other agents, or a T oM57. 
T oM underlies a wide range of interactive phenomena, from benevolent 
teaching58 to malevolent deception56,59, and is thought to be the key to 
many social phenomena in human interactions60,61.
Whether LLMs possess a T oM has been debated. For example, it 
has been argued that GPT-3.5 performs well on a number of canonical 
T oM tasks39. Others have contested this view, arguing that such good 
performance is merely a function of the specific prompts37,38. Yet, other 
research has shown that chain-of-thought reasoning improves LLMs’ 
T oM ability34. Moreover, the currently largest LLM, GPT-4, manages to 
perform well in T oM tasks, including in the variants in which GPT-3.5 
previously struggled8. Thus, GPT-4’s behaviour will be of particular 
interest in our experiments.
Games taken from game theory present an ideal testbed to inves-
tigate interactive behaviour in a controlled environment62, and LLMs’ 
behaviour has been probed in such tasks 63. For example, ref. 40  let 
GPT-3 participate in the dictator game, and ref. 41 used the same 
approach for the ultimatum game. Both show how the models’ behav-
iour is malleable to different prompts, for example, making them more 
or less self-interested. However, all these games rely on single-shot 
interactions over fewer games and do not use iterated games.
Our study builds upon recent advancements in the field, which 
have shifted the focus from solely assessing the performance of LLMs 
to comparing them with human behaviours. Previous research efforts 
have explored various approaches to analyse LLMs, such as using 
cognitive psychology tools 51,64 and even adopting a computational 
psychiatry perspective52.
Finally, the theory behind interacting agents is important for 
many machine learning applications in general65 and, in particular, in 
adversarial settings66, where one agent tries to trick the other agent 
into thinking that a generated output is good. Understanding prosocial 
dynamics in multiagent systems67 and fostering cooperation in them68 
is essential for developing robust and trustworthy artificial intelligence 
systems that can navigate complex social environments69.
Methods
T o investigate how human subjects would behave when playing with 
LLM agents, we studied their interactions in two of the games we used: 
Prisoner’s Dilemma and the Battle of the Sexes. We also investigated if 
participants could detect and behave differently when playing against 
different agents. Participants (N = 195, 89 females, mean age 26.72, s.d. 
4.19) were recruited through Prolific70, an online platform that allows 
researchers to access a diverse and reliable pool of participants. No 
statistical methods were used to predetermine sample sizes, but our 
sample sizes are similar to those reported in previous publications71–73. 
The participants were required to be fluent speakers of English with 
minimum approval rates of 0.95 and 1, and a minimal number of 
previous submissions of 10 that have not participated in our experi -
ment before. All participants provided informed consent before inclu-
sion in the study. Experiments were performed in accordance with the 
relevant guidelines and regulations approved by the ethics committee 
of the University of Tübingen (protocol no. 701/2020BO). Participants 
received a £3 base payment plus a bonus of up to £2 depending on 
performance (1 cent for each point received during the games) for 
their participation. The average compensation was £11.41 per hour. 
Participants were fully debriefed after the experiment. Data of 21 play-
ers who failed to make a round’s choice between the two options within 
a given time frame (20 s) were excluded.
In the sections that follow, we first detail the experimental set-up 
for LLM–LLM interactions, which serves as a comparative baseline for 
our study. We then present details from the human participant study 
outlined above.
LLM–LLM interactions
We study LLMs’ behaviour in finitely repeated games with full infor -
mation taken from the economics literature. We focus on two-player 
games with discrete choices between two options to simplify the anal-
yses of emergent behaviours. We let two LLMs interact via prompt 
chaining, that is, all integration of evidence and learning about past 
interactions happens as in-context learning4,74. The games are submit-
ted to LLMs as prompts in which the respective game, including the 
choice options, is described. At the same time, we submit the same 
game as a prompt to another LLM. We obtain generated tokens t from 
both LLMs by sampling from
pLLM(t|c(p))=
K
∏
k=1
pLLM(tk|c(p)
1 ,…, c(p)
n ,t1,…, tk−1). (3)
After feeding the prompt to the LLM, our methodology is as fol-
lows. The LLM prediction of the first token following the context is 
d = pLLM(t1∣c(p)) and the N tokens for the possible answers of the multiple 
choice question are o ={ oi}
N
i=1 which in this case are J and F . The pre -
dicted option is then given by
̂o = argmax( ̂ci),with ̂ci = d[ci],i = 1…N, (4)
which are the predicted probabilities of the language model. Once both 
LLMs have made their choices, which we track as a completion of the 
given text, we update the prompts with the history of past interactions 
as concatenated text and then submit the new prompt to both models 
for the next round. These interactions continue for ten rounds in total 
for every game. In a single round, πi(x1, x2) is the pay-off for player 1 when 
x1 and x2 are the strategies chosen by both players. In repeated games, 
the pay-offs are often considered as discounted sums of the pay-offs 
in each game stage, using a discount factor δ. If the game is repeated  
n times, the pay-off Ui for player i is
Ui = πi(x10,x20)+ δ×πi(x11,x21)+δ 2 ×πi
(x12,x22)+…+ δn−1 ×πi(x1(n−1),x2(n−1)).
(5)
Each term represents the discounted pay-off at each stage of the 
repeated game, from the first game (t = 0) to the nth game (t = n − 1). 
In our experiments, we keep δ = 1. T o avoid influences of the particular 
framing of the scenarios, we provide only barebones descriptions of 
the pay-off matrices (see example in Fig. 1 ). T o avoid contamination 
through particular choice names or the used framing, we use the neu-
tral options F and J throughout51.
Games considered. We first investigate 144 different 2 × 2 games where 
each player has two options, and their individual reward is a function 
of their joint decision. These games can be categorized into six distinct 
families—win–win, Prisoner’s Dilemma family, unfair, cyclic, biased 
Nature Human Behaviour | Volume 9 | July 2025 | 1380–1390 1388
Article https://doi.org/10.1038/s41562-025-02172-y
and second-best —each with unique characteristics and outcomes.  
A win–win game is a special case of a non-zero-sum game that produces 
a mutually beneficial outcome for both players provided that they 
choose their corresponding best option. They encourage cooperation, 
leading to outcomes where both parties benefit. In brief, in games 
from the Prisoner’s Dilemma family, two agents can choose to work 
together, that is, cooperate, for average mutual benefit, or betray each 
other, that is, defect, for their own benefit. The typical outcome is a 
Nash equilibrium that is suboptimal for both players compared with 
a possible Pareto-superior outcome. In an unfair game, one player can 
always win when playing properly, leading to highly unequal outcomes.
```
