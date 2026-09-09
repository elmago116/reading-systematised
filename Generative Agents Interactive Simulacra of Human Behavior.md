---
title: "Generative Agents: Interactive Simulacra of Human Behavior"
author: Joon Sung Park, Joseph C. O'Brien, et al.
year: "2023"
Type: Article
DOI: 10.1145/3586183.3606763
source: https://dl.acm.org/doi/10.1145/3586183.3606763
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - tech/Ai/LLM
pdfORepub: "[[Generative Agents Interactive Simulacra Park 2023.pdf]]"
---
[[Generative Agents Interactive Simulacra Park 2023.pdf]]

## Full text (extracted from `Generative Agents Interactive Simulacra Park 2023.pdf`)

*Source:* `2PDF/Generative Agents Interactive Simulacra Park 2023.pdf`  
*Extracted:* 2026-06-18

```text
Generative Agents: Interactive Simulacra of Human Behavior 
Joon Sung Park Joseph C. O’Brien Carrie J. Cai 
Stanford University Stanford University Google Research 
Stanford, USA Stanford, USA Mountain View, CA, USA 
joonspk@stanford.edu jobrien3@stanford.edu cjcai@google.com 
Meredith Ringel Morris Percy Liang Michael S. Bernstein 
Google DeepMind Stanford University Stanford University 
Seattle, WA, USA Stanford, USA Stanford, USA 
merrie@google.com pliang@cs.stanford.edu msb@cs.stanford.edu 
Figure 1: Generative agents are believable simulacra of human behavior for interactive applications. In this work, we demonstrate 
generative agents by populating a sandbox environment, reminiscent of The Sims, with twenty-fve agents. Users can observe 
and intervene as agents plan their days, share news, form relationships, and coordinate group activities. 
ABSTRACT 
Believable proxies of human behavior can empower interactive 
applications ranging from immersive environments to rehearsal 
spaces for interpersonal communication to prototyping tools. In 
this paper, we introduce generative agents: computational software 
agents that simulate believable human behavior. Generative agents 
wake up, cook breakfast, and head to work; artists paint, while 
Permission to make digital or hard copies of part or all of this work for personal or 
classroom use is granted without fee provided that copies are not made or distributed 
for proft or commercial advantage and that copies bear this notice and the full citation 
on the frst page. Copyrights for third-party components of this work must be honored. 
For all other uses, contact the owner/author(s). 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
© 2023 Copyright held by the owner/author(s). 
ACM ISBN 979-8-4007-0132-0/23/10. 
https://doi.org/10.1145/3586183.3606763 
authors write; they form opinions, notice each other, and initiate 
conversations; they remember and refect on days past as they plan 
the next day. To enable generative agents, we describe an architec-
ture that extends a large language model to store a complete record 
of the agent’s experiences using natural language, synthesize those 
memories over time into higher-level refections, and retrieve them 
dynamically to plan behavior. We instantiate generative agents 
to populate an interactive sandbox environment inspired by The 
Sims, where end users can interact with a small town of twenty-fve 
agents using natural language. In an evaluation, these generative 
agents produce believable individual and emergent social behav-
iors. For example, starting with only a single user-specifed notion 
that one agent wants to throw a Valentine’s Day party, the agents 
autonomously spread invitations to the party over the next two 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA J.S. Park, J.C. O’Brien, C.J. Cai, M.R. Morris, P. Liang, M.S. Bernstein 
days, make new acquaintances, ask each other out on dates to the 
party, and coordinate to show up for the party together at the right 
time. We demonstrate through ablation that the components of 
our agent architecture—observation, planning, and refection—each 
contribute critically to the believability of agent behavior. By fusing 
large language models with computational interactive agents, this 
work introduces architectural and interaction patterns for enabling 
believable simulations of human behavior. 
CCS CONCEPTS 
• Human-centered computing → Interactive systems and 
tools; • Computing methodologies → Natural language pro-
cessing. 
KEYWORDS 
Human-AI interaction, agents, generative AI, large language models 
ACM Reference Format: 
Joon Sung Park, Joseph C. O’Brien, Carrie J. Cai, Meredith Ringel Morris, 
Percy Liang, and Michael S. Bernstein. 2023. Generative Agents: Interactive 
Simulacra of Human Behavior. In The 36th Annual ACM Symposium on 
User Interface Software and Technology (UIST ’23), October 29–November 01, 
2023, San Francisco, CA, USA. ACM, New York, NY, USA, 22 pages. https: 
//doi.org/10.1145/3586183.3606763 
1 INTRODUCTION 
How might we craft an interactive artifcial society that refects 
believable human behavior? From sandbox games such as The Sims 
to applications such as cognitive models [23] and virtual environ-
ments [10, 59], for over four decades, researchers and practitioners 
have envisioned computational agents that can serve as believ-
able proxies of human behavior. In these visions, computationally-
powered agents act consistently with their past experiences and 
react believably to their environments. Such simulations of human 
behavior could populate virtual spaces and communities with re-
alistic social phenomena [27, 80], train people on how to handle 
rare yet difcult interpersonal situations [44, 52, 94], test social 
science theories [12, 46], craft model human processors for theory 
and usability testing [23, 39, 51], power ubiquitous computing appli-
cations [31] and social robots [10, 14], and underpin non-playable 
game characters [59, 85] that can navigate complex human rela-
tionships in an open world. 
However, the space of human behavior is vast and complex [85, 
108]. Despite striking progress in large language models [18] that 
can simulate human behavior at a single time point [39, 80], fully 
general agents that ensure long-term coherence would be better 
suited by architectures that manage constantly-growing memories 
as new interactions, conficts, and events arise and fade over time 
while handling cascading social dynamics that unfold between 
multiple agents. Success requires an approach that can retrieve 
relevant events and interactions over a long period, refect on those 
memories to generalize and draw higher-level inferences, and apply 
that reasoning to create plans and reactions that make sense in the 
moment and in the longer-term arc of the agent’s behavior. 
In this paper, we introduce generative agents—agents that draw 
on generative models to simulate believable human behavior—and 
demonstrate that they produce believable simulacra of both in-
dividual and emergent group behavior. Generative agents draw 
a wide variety of inferences about themselves, other agents, and 
their environment; they create daily plans that refect their char-
acteristics and experiences, act out those plans, react, and re-plan 
when appropriate; they respond when the end user changes their 
environment or commands them in natural language. For instance, 
generative agents turn of the stove when they see that their break-
fast is burning, wait outside the bathroom if it is occupied, and 
stop to chat when they meet another agent they want to talk to.1 
A society full of generative agents is marked by emergent social 
dynamics where new relationships are formed, information difuses, 
and coordination arises across agents. 
To enable generative agents, we describe an agent architecture 
that stores, synthesizes, and applies relevant memories to generate 
believable behavior using a large language model. Our architecture 
comprises three main components. The frst is the memory stream, 
a long-term memory module that records, in natural language, a 
comprehensive list of the agent’s experiences. A memory retrieval 
model combines relevance, recency, and importance to surface the 
records needed to inform the agent’s moment-to-moment behavior. 
The second is refection, which synthesizes memories into higher-
level inferences over time, enabling the agent to draw conclusions 
about itself and others to better guide its behavior. The third is 
planning, which translates those conclusions and the current en-
vironment into high-level action plans and then recursively into 
detailed behaviors for action and reaction. These refections and 
plans are fed back into the memory stream to infuence the agent’s 
future behavior. 
This architecture suggests applications in multiple domains, from 
role-play and social prototyping to virtual worlds and games. In 
social role-play scenarios (e.g., interview preparation), a user could 
safely rehearse difcult, confict-laden conversations. When pro-
totyping social platforms, a designer could go beyond temporary 
personas to prototype dynamic, complex interactions that unfold 
over time. For this paper, we focus on the ability to create a small, 
interactive society of agents inspired by games such as The Sims.2 
By connecting our architecture to the ChatGPT large language 
model [77], we manifest a society of twenty-fve agents in a game 
environment. End users can observe and interact with these agents. 
If an end user or developer wanted the town to host an in-game 
Valentine’s Day party, for example, traditional game environments 
would require scripting tens of characters’ behavior manually. We 
demonstrate that, with generative agents, it is sufcient to simply 
tell one agent that she wants to throw a party. Despite many poten-
tial points of failure—the party planner must remember to invite 
other agents to the party, attendees must remember the invitation, 
those who remember must decide to actually show up, and more— 
our agents succeed. They spread the word about the party and then 
1When referring to generative agents engaging in actions or going to places, this is a 
shorthand for readability and not a suggestion that they are engaging in human-like 
agency. The behaviors of our agents, akin to animated Disney characters, aim to create 
a sense of believability, but they do not imply genuine agency.
2A demonstration of an actual simulation of the generative agent society can be 
viewed at the following link: https://reverie.herokuapp.com/UIST_Demo/. A public 
repository for the simulation code is located here: https://github.com/joonspk-research/ 
generative_agents 
Generative Agents UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
show up, with one agent even asking another on a date to the party, 
all from a single user-generated seed suggestion. 
We conducted two evaluations of generative agents: a controlled 
evaluation to test whether the agents produce believable individual 
behaviors in isolation, and an end-to-end evaluation where the 
agents interacted with each other in open-ended ways over two 
days of game time to understand their stability and emergent social 
behaviors. In the technical evaluation, we leverage a methodologi-
cal opportunity to evaluate an agent’s knowledge and behavior by 
“interviewing” it in natural language to probe the agents’ ability to 
stay in character, remember, plan, react, and refect accurately. We 
compared several ablations that limit agents’ access to memory, re-
fection, and planning. We observe that each of these components is 
critical to strong performance across these interview tasks. Across 
the technical and end-to-end evaluation, the most common errors 
arose when the agent failed to retrieve relevant memories, fabri-
cated embellishments to the agent’s memory, or inherited overly 
formal speech or behavior from the language model. 
In sum, this paper makes the following contributions: 
• Generative agents, believable simulacra of human behavior 
that are dynamically conditioned on agents’ changing expe-
riences and environment. 
• A novel architecture that makes it possible for generative 
agents to remember, retrieve, refect, interact with other 
agents, and plan through dynamically evolving circumstances. 
The architecture leverages the powerful prompting capabili-
ties of large language models and supplements those capa-
bilities to support longer-term agent coherence, the ability 
to manage dynamically evolving memory, and recursively 
produce higher-level refections. 
• Two evaluations, a controlled evaluation and an end-to-end 
evaluation, that establish causal efects of the importance 
of components of the architecture, as well as identify break-
downs arising from, e.g., improper memory retrieval. 
• Discussion of the opportunities and ethical and societal risks 
of generative agents in interactive systems. We argue that 
these agents should be tuned to mitigate the risk of users 
forming parasocial relationships, logged to mitigate risks 
stemming from deepfakes and tailored persuasion, and ap-
plied in ways that complement rather than replace human 
stakeholders in design processes. 
2 RELATED WORK 
In this section, we refect on the prior literature in human-AI interac-
tion and situate, within its canon, the agenda of building believable 
proxies of human behavior. This agenda, once hailed as a north 
star in the interaction, game, and artifcial intelligence communi-
ties [10, 59, 85, 86], has remained challenging due to the complexity 
of human behavior [17, 108]. We synthesize this research to suggest 
that large language models, though not sufcient by themselves, 
open up a new angle for creating believable agents when leveraged 
using the appropriate architecture. 
2.1 Human-AI Interaction 
Interactive artifcial intelligence systems aim to combine human in-
sights and capabilities in computational artifacts that can augment 
their users [4, 30]. A long line of work has explored ways to enable 
users to interactively specify model behavior. For instance, Crayons 
demonstrated an early vision of interactive machine learning, allow-
ing non-expert users to train classifers [30]. Further work helped to 
articulate how end users might describe their classifcation goals to 
the system through examples [34] or demonstration [32]. Recent ad-
vancements have extended these explorations to deep learning [63] 
and prompt-based authoring [50, 67, 106]. 
Meanwhile, a persistent thread of research has advanced the case 
for language- and agent-based interaction in human-computer in-
teraction. Formative work such as SHRDLU [103] and ELIZA [102] 
demonstrated the opportunities and the risks associated with nat-
ural language interaction with computing systems. As research 
progressed, it became evident that autonomous agents could ofer 
new metaphors for delegation and interaction [68], but the bound-
aries of delegation between humans and agents have remained the 
subject of ongoing debate and refnement [47, 89, 90]. Recently, this 
technology has reached a level of stability that enables agents to 
interact via natural language in large and complex online social 
environments (e.g., [55]). Natural language interaction provides a 
novel modality that can enhance user abilities in domains such as 
photo editing [3, 35, 65] and code editing [88]. 
We convene these threads of work to show that we can now 
create agents that proxy human behavior for interactive systems, 
and interact with them using natural language. In doing so, this 
work reopens the door to examining foundational human-computer 
interaction questions around cognitive models such as GOMS and 
Keystroke-Level Model (KLM) [22, 23], around prototyping tools [80], 
and around ubiquitous computing applications [26, 31, 101]. 
2.2 Believable Proxies of Human Behavior 
Prior literature has described believability, or believable agents, as a 
central design and engineering goal. Believable agents are designed 
to provide an illusion of life and present a facade of realism in the 
way they appear to make decisions and act on their own volition, 
similar to the characters in Disney movies [10, 96]. These agents 
can populate and perceive an open world environment like the 
one we inhabit [10, 59], and strive to behave in ways that exhibit 
emergent behaviors grounded in social interactions with users or 
other agents with the aim of becoming believable proxies of our 
behavior in hypothetical simulations of individuals and communi-
ties [20, 36, 71]. Historically, these agents were developed in the 
context of intelligent game non-player characters (NPCs) [59, 85]. 
Creating NPCs with believable behavior, if possible, could enhance 
player experiences in games and interactive fctions by enabling 
emergent narratives [8, 16, 49, 93] and social interactions with the 
agents [109]. However, more importantly, game worlds provide 
increasingly realistic representations of real-world afordances, and 
as observed by Laird and van Lent in 2001, these simulated worlds 
ofer accessible testbeds for developers of believable agents to f-
nesse the agents’ cognitive capabilities without worrying about 
implementing robotics in the real world or creating simulation 
environments from scratch [59, 85]. 
A diverse set of approaches to creating believable agents emerged 
over the past four decades. In implementation, however, these ap-
proaches often simplifed the environment or dimensions of agent 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA J.S. Park, J.C. O’Brien, C.J. Cai, M.R. Morris, P. Liang, M.S. Bernstein 
behavior to make the efort more manageable [17, 73]. Rule-based 
approaches, such as fnite-state machines [91, 97] and behavior 
trees [41, 54, 82] account for the brute force approach of human-
authoring the agent’s behavior [71]. They provide a straightforward 
way of creating simple agents that is still the most dominant ap-
proach today [69, 74, 108], and can even handle rudimentary social 
interactions, as shown in games such as Mass Efect [13] and The 
Sims [7] series. Nonetheless, manually crafting behavior that can 
comprehensively address the breadth of possible interactions in 
an open world is untenable. This means that the resulting agent 
behaviors may not fully represent the consequences of their in-
teractions [70–72], and cannot perform new procedures that were 
not hard-coded in their script [91, 97]. On the other hand, preva-
lent learning-based approaches for creating believable agents, such 
as reinforcement learning, have overcome the challenge of man-
ual authoring by letting the agents learn their behavior, and have 
achieved superhuman performance in recent years in games such 
as AlphaStar for Starcraft [99] and OpenAI Five for Dota 2 [11]. 
However, their success has largely taken place in adversarial games 
with readily defnable rewards that a learning algorithm can op-
timize for. They have not yet addressed the challenge of creating 
believable agents in an open world [40, 74, 91]. 
Cognitive architectures in computation, pioneered by Newell, 
aimed to build the infrastructure for supporting a comprehensive 
set of cognitive functions [76] that suited the all-encompassing 
nature of believable agents held in its original vision. They fueled 
some of the earliest examples of believable agents. For instance, 
Quakebot-SOAR [60] and ICARUS [25, 64] generated NPCs in frst-
person shooter games, while TacAir-SOAR [81] generated pilots in 
aerial combat training simulations. The architectures used by these 
agents difered (Quakebot- and TacAir-SOAR relied on SOAR [61], 
while ICARUS relied on its own variation that was inspired by 
SOAR and ACT-R [6]), but they shared the same underlying prin-
ciple [62]. They maintained short-term and long-term memories, 
flled these memories with symbolic structures, and operated in 
perceive-plan-act cycles, dynamically perceiving the environment 
and matching it with one of the manually crafted action proce-
dures [58, 97]. Agents created using cognitive architectures aimed 
to be generalizable to most, if not all, open world contexts and 
exhibited robust behavior for their time. However, their space of 
action was limited to manually crafted procedural knowledge, and 
they did not ofer a mechanism through which the agents could be 
inspired to seek new behavior. As such, these agents were deployed 
mostly in non-open world contexts such as frst-person shooter 
games [25, 60] or blocks worlds [64]. 
Today, creating believable agents as described in its original 
defnition remains an open problem [85, 108]. Many have moved 
on, arguing that although current approaches for creating believable 
agents might be cumbersome and limited, they are good enough 
to support existing gameplay and interactions [24, 75, 108]. Our 
argument is that large language models ofer an opportunity to 
re-examine these questions, provided that we can craft an efective 
architecture to synthesize memories into believable behavior. We 
ofer a step toward such an architecture in this paper. 
2.3 Large Language Models and Human 
Behavior 
Generative agents leverage a large language model to power their 
behavior. The key observation is that large language models encode 
a wide range of human behavior from their training data [15, 18]. If 
prompted with a narrowly defned context, the models can be used 
to generate believable behavior. Recent work has demonstrated 
the efcacy of this approach. For instance, social simulacra used a 
large language model to generate users that would populate new 
social computing systems to prototype their emergent social dynam-
ics [80]. This approach used a prompt chain [105, 106] to generate 
short natural language descriptions of personas and their behaviors 
as they appear in the system being prototyped. Other empirical 
studies have replicated existing social science studies [46], political 
surveys [92], and generated synthetic data [39]. Large language 
models have also been used to generate interactive human behavior 
for users to engage with. In gaming, for instance, these models have 
been employed to create interactive fction [37] and text adventure 
games [21]. With their ability to generate and decompose action 
sequences, large language models have also been used in planning 
robotics tasks [48]. For example, when presented with a task, such 
as picking up a bottle, the model is prompted to break down the 
task into smaller action sequences, such as heading to the table 
where the bottle is located and picking it up. 
We posit that, based on the work summarized above, large lan-
guage models can become a key ingredient for creating believable 
agents. The existing literature largely relies on what could be con-
sidered frst-order templates that employ few-shot prompts [38, 66] 
or chain-of-thought prompts [100]. These templates are efective in 
generating behavior that is conditioned solely on the agent’s cur-
rent environment (e.g., how would a troll respond to a given post, 
what actions would a robot need to take to enter a room given that 
there is a door). However, believable agents require conditioning 
not only on their current environment but also on a vast amount 
of past experience, which is a poor ft (and as of today, impossi-
ble due to the underlying models’ limited context window) using 
frst-order prompting. Recent studies have attempted to go beyond 
frst-order prompting by augmenting language models with a static 
knowledge base and an information retrieval scheme [53] or with 
a simple summarization scheme [104]. This paper extends these 
ideas to craft an agent architecture that handles retrieval where 
past experience is dynamically updated at each time step and mixed 
with agents’ current context and plans, which may either reinforce 
or contradict each other. 
3 GENERATIVE AGENT BEHAVIOR AND 
INTERACTION 
To illustrate the afordances of generative agents, we instantiate 
them as characters in a simple sandbox world reminiscent of The 
Sims [7]. This sprite-based sandbox game world, Smallville, evokes 
a small town environment. In this section, we will walk through the 
afordances and interactions with generative agents in Smallville 
and describe how the agents behave within it. Then, in Section 4, 
we will introduce our generative agent architecture that powers 
these afordances and interactions. In Section 5, we will describe the 
Generative Agents UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
Figure 2: The Smallville sandbox world, with areas labeled. The root node describes the entire world, children describe areas 
(e.g., houses, cafe, stores), and leaf nodes describe objects (e.g., table, bookshelf). Agents remember a subgraph that refects the 
parts of the world they have seen, maintaining the state of those parts as they observed them. 
implementation of the sandbox environment and how the agents 
interact with the underlying engine of the sandbox world. 
3.1 Agent Avatar and Communication 
A community of 25 unique agents inhabits Smallville. Each agent is 
represented by a simple sprite avatar. We authored one paragraph 
of natural language description to depict each agent’s identity, 
including their occupation and relationship with other agents, as 
seed memories. For example, John Lin has the following description: 
John Lin is a pharmacy shopkeeper at the Willow 
Market and Pharmacy who loves to help people. He 
is always looking for ways to make the process 
of getting medication easier for his customers; 
John Lin is living with his wife, Mei Lin, who 
is a college professor, and son, Eddy Lin, who is 
a student studying music theory; John Lin loves 
his family very much; John Lin has known the old 
couple next-door, Sam Moore and Jennifer Moore, 
for a few years; John Lin thinks Sam Moore is a 
kind and nice man; John Lin knows his neighbor, 
Yuriko Yamamoto, well; John Lin knows of his 
neighbors, Tamara Taylor and Carmen Ortiz, but 
has not met them before; John Lin and Tom Moreno 
are colleagues at The Willows Market and Pharmacy; 
John Lin and Tom Moreno are friends and like to 
discuss local politics together; John Lin knows 
the Moreno family somewhat well — the husband Tom 
Moreno and the wife Jane Moreno. 
3.1.1 Inter-Agent Communication. The agents interact with the 
world by their actions, and with each other through natural lan-
guage. At each time step of the sandbox engine, the agents output a 
natural language statement describing their current action, such as 
“Isabella Rodriguez is writing in her journal”, “Isabella Rodriguez is 
checking her emails”, “Isabella Rodriguez is talking with her family 
on the phone”, or “Isabella Rodriguez is getting ready for bed. ” This 
statement is then translated into concrete movements that afect 
the sandbox world. The action is displayed on the sandbox inter-
face as a set of emojis, providing an abstract representation of the 
action from an overhead view. To achieve this, the system utilizes 
a language model to translate the action into a set of emojis, which 
appear above each avatar’s head in a speech bubble. For example, 
“Isabella Rodriguez is writing in her journal” is displayed as 
 , 
while “Isabella Rodriguez is checking her emails” appears as 
 . 
The complete natural language description of the action can be 
accessed by clicking on the agent’s avatar. 
Agents communicate with each other in full natural language. 
They are aware of other agents in their local area, and the generative 
agent architecture determines whether they walk by or engage 
in conversation. Here, a sample in the middle of a conversation 
between the agents Isabella Rodriguez and Tom Moreno about the 
upcoming election:3 
Isabella: I’m still weighing my options, but I’ve been 
discussing the election with Sam Moore. What are 
your thoughts on him? 
Tom: To be honest, I don’t like Sam Moore. I think 
he’s out of touch with the community and doesn’t 
have our best interests at heart. 
3We note that the conversational style of these agents can feel overly formal, likely a Each semicolon-delimited phrase is entered into the agent’s initial result of instruction tuning in the underlying models. We expect that the writing style 
memory as memories at the start of the simulation. will be better controllable in future language models. 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA J.S. Park, J.C. O’Brien, C.J. Cai, M.R. Morris, P. Liang, M.S. Bernstein 
3.1.2 User Controls. The user communicates with the agent through 
natural language by specifying a persona that the agent should per-
ceive them as. For example, if the user specifes that they are a news 
“reporter” and asks about the upcoming election by saying, “Who 
is running for ofce?”, the John agent replies: 
John: My friends Yuriko, Tom and I have been talk-
ing about the upcoming election and discussing the 
candidate Sam Moore. We have all agreed to vote for 
him because we like his platform. 
To directly command one of the agents, the user takes on the per-
sona of the agent’s “inner voice”—this makes the agent more likely 
to treat the statement as a directive. For instance, when told “You 
are going to run against Sam in the upcoming election” by a user 
as John’s inner voice, John decides to run in the election and shares 
his candidacy with his wife and son. 
3.2 Environmental Interaction 
Smallville features the common afordances of a small village, in-
cluding a cafe, bar, park, school, dorm, houses, and stores. It also 
defnes subareas and objects that make those spaces functional, 
such as a kitchen in a house and a stove in the kitchen (Figure 2). 
All spaces serving as agents’ primary living quarters feature a bed, 
desk, closet, shelf, as well as a bathroom and a kitchen.4 
Agents move around Smallville as one would in a simple video 
game, entering and leaving buildings, navigating its map, and ap-
proaching other agents. Agent movements are directed by the gen-
erative agent architecture and the sandbox game engine: when the 
model dictates that the agent will move to a location, we calculate 
a walking path to the destination in the Smallville environment, 
and the agent begins moving. In addition, users can also enter the 
sandbox world of Smallville as an agent operating within it. The 
agent that the user embodies can be an agent already present in 
the world, such as Isabella and John, or it can be an outside visitor 
with no prior history in Smallville. The inhabitants of Smallville 
will treat the user-controlled agent no diferently than they treat 
each other. They recognize its presence, initiate interactions, and 
remember its behavior before forming opinions about it. 
Users and agents can infuence the state of the objects in this 
world, much like in sandbox games such as The Sims. For example, 
a bed can be occupied when an agent is sleeping, and a refrigerator 
can be empty when an agent uses up the ingredients to make 
breakfast. End users can also reshape an agent’s environment in 
Smallville by rewriting the status of objects surrounding the agent 
in natural language. For instance, when Isabella is making breakfast 
in the morning, the user can change the status of the kitchen stove 
from “turned on” to “burning” by inputting a command to the 
system that chooses the object and illustrates its new status, like 
this: “<Isabella’s apartment: kitchen: stove> is burning. ” Isabella 
will notice this in the next moment and go to turn of the stove 
and remake her breakfast. Likewise, if the user sets the status of 
Isabella’s shower to “leaking water” when she enters the bathroom, 
she will gather tools from her living room and try to fx the leak. 
4This environment design is not the focus of our work, so we generated this environ-
ment manually, not automatically. Future work can continue to expand the richness of 
the agents’ environments. 
3.3 Example “Day in the Life” 
Starting from the single-paragraph description, generative agents 
begin planning their days. As time passes in the sandbox world, 
their behaviors evolve as these agents interact with each other and 
the world, building memories and relationships, and coordinating 
joint activities. 
We demonstrate the behavior of generative agents by tracing the 
output of our system over the course of one day for the agent John 
Lin (Figure 3). In the Lin family, John is the frst to wake up at 7 a.m. 
He brushes his teeth, takes a shower, gets dressed, eats breakfast, 
and checks the news at the dining table in the living room. At 8 
a.m., Eddy follows suit, rushing out of bed to prepare for his classes. 
He catches up with John just as he is about to head out: 
John: Good morning Eddy. Did you sleep well? 
Eddy: Good morning dad. Yeah, I slept great. 
John: That’s good. What are you working on today? 
Eddy: I’m working on a new music composition for 
my class. It’s due this week, so I’m trying to get it 
fnished. But I’m having so much fun with it! 
John: That sounds great! 
Soon after Eddy heads out, Mei wakes up and joins John. Mei asks 
about her son, and John recalls the conversation they just had: 
Mei: Did Eddy already leave for school? 
John: Yes, he just left. He’s working on a music 
composition for his class. 
Mei: Oh, that’s wonderful! Tell me about it. 
John: I think he’s really enjoying it! He said he’s 
having a lot of fun with it. 
Mei: That’s great! I’m so proud of him. 
As they fnish their conversation, Mei and John pack up. Mei goes 
on to teach and work on her research paper, while John opens his 
pharmacy counter at the Willow Market and Pharmacy by 9 a.m. 
3.4 Emergent Social Behaviors 
By interacting with each other, generative agents in Smallville 
exchange information, form new relationships, and coordinate joint 
activities. Extending prior work [80], these social behaviors are 
emergent rather than pre-programmed. 
3.4.1 Information Difusion. As agents notice each other, they may 
engage in dialogue—as they do so, information can spread from 
agent to agent. For instance, in a conversation between Sam and 
Tom at the grocery store, Sam tells Tom about his candidacy in the 
local election: 
Sam: Hey Tom, how’s it going? 
Tom: Good, thanks. What’s up? 
Sam: Well, I wanted to talk to you about something. 
I’m actually running for mayor in the upcoming local 
election. 
Tom: Really? That’s great news! Why are you run-
ning? 
Sam: I’ve been involved in local politics for years 
now, and I really feel like I can make a diference in 
our community. Plus, I want to bring new ideas and 
perspectives to the table. 
Generative Agents UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
Figure 3: A morning in the life of a generative agent, John Lin. John wakes up around 6 am and completes his morning routine, 
which includes brushing his teeth, taking a shower, and eating breakfast. He briefy catches up with his wife, Mei, and son, 
Eddy, before heading out to begin his workday. 
Figure 4: At the beginning of the simulation, one agent is 
initialized with an intent to organize a Valentine’s Day party. 
Despite many possible points of failure in the ensuing chain 
of events—agents might not act on that intent, might forget 
to tell others, might not remember to show up—the Valen-
tine’s Day party does, in fact, occur, with a number of agents 
gathering and interacting. 
Later that day, after Sam left, Tom and John, who heard the news 
from another source, discuss Sam’s chances of winning the election: 
John: I heard that Sam Moore is running for mayor 
in the local election. Do you think he has a good 
chance of winning? 
Tom: I do think he has a good chance. He’s been 
working hard in the community and I think he will 
get a lot of support. What do you think? 
John: I think it’s great that he’s running. I’m curious 
to see how the election will turn out. 
Gradually, Sam’s candidacy becomes the talk of the town, with 
some supporting him and others remaining undecided. 
3.4.2 Relationship Memory. Agents in Smallville form new rela-
tionships over time and remember their interactions with other 
agents. For example, at the start, Sam does not know Latoya Williams. 
While taking a walk in Johnson Park, Sam runs into Latoya, and 
they introduce themselves. Latoya mentions that she is working 
on a photography project: “I’m here to take some photos for a 
project I’m working on.” In a later interaction, Sam’s interactions 
with Latoya indicate a memory of that interaction, as he asks “Hi, 
Latoya. How is your project going?” and she replies “Hi, Sam. It’s 
going well!” 
3.4.3 Coordination. Generative agents coordinate with each other. 
Isabella Rodriguez, at Hobbs Cafe, is initialized with an intent to 
plan a Valentine’s Day party from 5 to 7 p.m. on February 14th. From 
this seed, the agent proceeds to invite friends and customers when 
she sees them at Hobbs Cafe or elsewhere. Isabella then spends the 
afternoon of the 13th decorating the cafe for the occasion. Maria, a 
frequent customer and close friend of Isabella’s, arrives at the cafe. 
Isabella asks for Maria’s help in decorating for the party, and Maria 
agrees. Maria’s character description mentions that she has a crush 
on Klaus. That night, Maria invites Klaus, her secret crush, to join 
her at the party, and he gladly accepts. 
On Valentine’s Day, fve agents, including Klaus and Maria, show 
up at Hobbs Cafe at 5 pm, and they enjoy the festivities (Figure 4). 
In this scenario, the end user only set Isabella’s initial intent to 
throw a party and Maria’s crush on Klaus: the social behaviors of 
spreading the word, decorating, asking each other out, arriving at 
the party, and interacting with each other at the party were initiated 
by the agent architecture. 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA J.S. Park, J.C. O’Brien, C.J. Cai, M.R. Morris, P. Liang, M.S. Bernstein 
Figure 5: Our generative agent architecture. Agents perceive their environment, and all perceptions are saved in a comprehensive 
record of the agent’s experiences called the memory stream. Based on their perceptions, the architecture retrieves relevant 
memories and uses those retrieved actions to determine an action. These retrieved memories are also used to form longer-term 
plans and create higher-level refections, both of which are entered into the memory stream for future use. 
4 GENERATIVE AGENT ARCHITECTURE 
Generative agents aim to provide a framework for behavior in an 
open world: one that can engage in interactions with other agents 
and react to changes in the environment. Generative agents take 
their current environment and past experiences as input and gener-
ate behavior as output. Underlying this behavior is a novel agent ar-
chitecture that combines a large language model with mechanisms 
for synthesizing and retrieving relevant information to condition 
the language model’s output. Without these mechanisms, large 
language models can output behavior, but the resulting agents may 
not react based on the agent’s past experiences, may not make 
important inferences, and may not maintain long-term coherence. 
Challenges with long-term planning and coherence remain [19] 
even with today’s most performant models such as GPT-4. Because 
generative agents produce large streams of events and memories 
that must be retained, a core challenge of our architecture is to 
ensure that the most relevant pieces of the agent’s memory are 
retrieved and synthesized when needed. 
At the center of our architecture is the memory stream, a data-
base that maintains a comprehensive record of an agent’s experi-
ence. From the memory stream, records are retrieved as relevant to 
plan the agent’s actions and react appropriately to the environment. 
Records are recursively synthesized into higher- and higher-level 
refections that guide behavior. Everything in the architecture is 
recorded and reasoned over as a natural language description, al-
lowing the architecture to leverage a large language model. 
Our current implementation utilizes the gpt3.5-turbo version of 
ChatGPT [77]. We expect that the architectural basics of genera-
tive agents—memory, planning, and refection—will likely remain 
the same as language models improve. Newer language models 
(e.g., GPT-4) will continue to expand the expressive power and 
performance of the prompts that underpin generative agents. As of 
writing, however, GPT-4’s API was invitation-only, so our agents 
use ChatGPT. 
4.1 Memory and Retrieval 
Challenge: Creating generative agents that can simulate human 
behavior requires reasoning about a set of experiences that is far 
larger than what should be described in a prompt, as the full mem-
ory stream can distract the model and does not even currently ft 
into the limited context window. Consider the Isabella agent an-
swering the question, “What are you passionate about these days?” 
Summarizing all of Isabella’s experiences to ft in the limited con-
text window of the language model produces an uninformative 
response, where Isabella discusses topics such as collaborations for 
events and projects and cleanliness and organization in a cafe. In-
stead of summarizing, the memory stream described below surfaces 
relevant memories, resulting in a more informative and specifc 
response that mentions Isabella’s passion for making people feel 
welcome and included, planning events and creating an atmosphere 
that people can enjoy, such as the Valentine’s Day party. 
Approach: The memory stream maintains a comprehensive record 
of the agent’s experience. It is a list of memory objects, where each 
object contains a natural language description, a creation times-
tamp, and a most recent access timestamp. The most basic element 
of the memory stream is an observation, which is an event directly 
perceived by an agent. Common observations include behaviors 
performed by the agent themselves or behaviors that agents per-
ceive being performed by other agents or non-agent objects. For 
instance, Isabella Rodriguez, who works at a cofee shop, might 
accrue the following observations over time: (1) Isabella Rodriguez 
is setting out the pastries, (2) Maria Lopez is studying for a Chem-
istry test while drinking cofee, (3) Isabella Rodriguez and Maria 
Lopez are conversing about planning a Valentine’s day party at 
Hobbs Cafe, (4) The refrigerator is empty. 
Our architecture implements a retrieval function that takes the 
agent’s current situation as input and returns a subset of the mem-
ory stream to pass on to the language model. There are many pos-
sible implementations of a retrieval function, depending on what 
is important for the agent to consider when deciding how to act. 
Generative Agents UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
Figure 6: The memory stream comprises a large number of observations that are relevant and irrelevant to the agent’s current 
situation. Retrieval identifes a subset of these observations that should be passed to the language model to condition its 
response to the situation. 
In our context, we focus on three main components that, together, 
produce efective results. 
Recency assigns a higher score to memory objects that were re-
cently accessed, so that events from a moment ago or this morning 
are likely to remain in the agent’s attentional sphere. In our im-
plementation, we treat recency as an exponential decay function 
over the number of sandbox game hours since the memory was 
last retrieved. Our decay factor is 0.995. 
Importance distinguishes mundane from core memories by as-
signing a higher score to memory objects that the agent believes to 
be important. For instance, a mundane event, such as eating break-
fast in one’s room, would yield a low importance score, whereas 
a breakup with one’s signifcant other would yield a high score. 
There are many possible implementations of an importance score; 
we fnd that directly asking the language model to output an integer 
score is efective. The full prompt appears below: 
On the scale of 1 to 10, where 1 is purely mundane 
(e.g., brushing teeth, making bed) and 10 is 
extremely poignant (e.g., a break up, college 
acceptance), rate the likely poignancy of the 
following piece of memory. 
Memory: buying groceries at The Willows Market 
and Pharmacy 
Rating: <fill in> 
This prompt returns an integer value of 2 for “cleaning up the room” 
and 8 for “asking your crush out on a date. ” The importance score 
is generated at the time the memory object is created. 
Relevance assigns a higher score to memory objects that are 
related to the current situation. What is relevant depends on the 
answer to, “Relevant to what?”, so we condition relevance on a 
query memory. If the query, for example, is that a student is dis-
cussing what to study for a chemistry test with a classmate, memory 
objects about their breakfast should have low relevance, whereas 
memory objects about the teacher and schoolwork should have 
high relevance. In our implementation, we use the language model 
to generate an embedding vector of the text description of each 
memory. Then, we calculate relevance as the cosine similarity be-
tween the memory’s embedding vector and the query memory’s 
embedding vector. 
To calculate the fnal retrieval score, we normalize the recency, 
relevance, and importance scores to the range of [0, 1] using min-
max scaling. The retrieval function scores all memories as a weighted 
combination of the three elements: ��������������� = ������������������������ · ��������������������� + 
��������������������������������� · ������������������������������ + ������������������������������ · ��������������������������� . In our implemen-
tation, all ���s are set to 1. The top-ranked memories that ft within 
the language model’s context window are included in the prompt. 
4.2 Refection 
Challenge: Generative agents, when equipped with only raw ob-
servational memory, struggle to generalize or make inferences. 
Consider a scenario in which Klaus Mueller is asked by the user: 
“If you had to choose one person of those you know to spend an 
hour with, who would it be?" With access to only observational 
memory, the agent simply chooses the person with whom Klaus 
has had the most frequent interactions: Wolfgang, his college dorm 
neighbor. Unfortunately, Wolfgang and Klaus only ever see each 
other in passing, and do not have deep interactions. A more desir-
able response requires that the agent generalize from memories of 
Klaus spending hours on a research project to generate a higher-
level refection that Klaus is passionate about research, and likewise 
UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA J.S. Park, J.C. O’Brien, C.J. Cai, M.R. Morris, P. Liang, M.S. Bernstein 
Figure 7: A refection tree for Klaus Mueller. The agent’s observations of the world, represented in the leaf nodes, are recursively 
synthesized to derive Klaus’s self-notion that he is highly dedicated to his research. 
recognize Maria putting in efort into her own research (albeit in 
a diferent feld), enabling a refection that they share a common 
interest. With the approach below, when Klaus is asked who to 
spend time with, Klaus chooses Maria instead of Wolfgang. 
Approach: We introduce a second type of memory, which we call 
a refection. Refections are higher-level, more abstract thoughts 
generated by the agent. Because they are a type of memory, they 
are included alongside other observations when retrieval occurs. 
Refections are generated periodically; in our implementation, we 
generate refections when the sum of the importance scores for the 
latest events perceived by the agents exceeds a threshold (150 in 
our implementation). In practice, our agents refected roughly two 
or three times a day. 
The frst step in refection is for the agent to determine what 
to refect on, by identifying questions that can be asked given the 
agent’s recent experiences. We query the large language model with 
the 100 most recent records in the agent’s memory stream (e.g., 
“Klaus Mueller is reading a book on gentrifcation”, “Klaus Mueller is 
conversing with a librarian about his research project”, “desk at the 
library is currently unoccupied”) and prompt the language model, 
“Given only the information above, what are 3 most salient high-
level questions we can answer about the subjects in the statements?” 
The model’s response generates candidate questions: for example, 
What topic is Klaus Mueller passionate about? and What is the 
relationship between Klaus Mueller and Maria Lopez? We use these 
generated questions as queries for retrieval, and gather relevant 
memories (including other refections) for each question. Then 
we prompt the language model to extract insights and cite the 
particular records that served as evidence for the insights. The full 
prompt is as follows: 
Statements about Klaus Mueller 
1. Klaus Mueller is writing a research paper 
2. Klaus Mueller enjoys reading a book 
on gentrification 
3. Klaus Mueller is conversing with Ayesha Khan 
about exercising [...] 
What 5 high-level insights can you infer from 
the above statements? (example format: insight 
(because of 1, 5, 3)) 
This process generates statements such as Klaus Mueller is dedi-
cated to his research on gentrifcation (because of 1, 2, 8, 15). We 
parse and store the statement as a refection in the memory stream, 
including pointers to the memory objects that were cited. 
Refection explicitly allows the agents to refect not only on 
their observations but also on other refections: for example, the 
second statement about Klaus Mueller above is a refection that 
Klaus previously had, not an observation from his environment. 
As a result, agents generate trees of refections: the leaf nodes of 
the tree represent the base observations, and the non-leaf nodes 
represent thoughts that become more abstract and higher-level the 
higher up the tree they are. 
4.3 Planning and Reacting 
Challenge: While a large language model can generate plausible be-
havior in response to situational information (e.g., [46, 80]), agents 
need to plan over a longer time horizon to ensure that their sequence 
of actions is coherent and believable. If we prompt a language model 
with Klaus’s background, describe the time, and ask what action 
he ought to take at the given moment, Klaus would eat lunch at 12 
pm, but then again at 12:30 pm and 1 pm, despite having already 
Generative Agents UIST ’23, October 29–November 01, 2023, San Francisco, CA, USA 
eaten his lunch twice. Optimizing for believability in the moment 
sacrifces believa
```
