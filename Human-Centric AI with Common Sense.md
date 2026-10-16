---
title: "Human-Centric AI with Common Sense"
type: Journal article
source: "2PDF/Human-Centric AI with Common Sense.pdf"
created: 2026-09-22
tags: []
---

[[Human-Centric AI with Common Sense.pdf]]

## Full text (extracted from `2PDF/Human-Centric AI with Common Sense.pdf`)

*Extracted:* 2026-09-22

```text
Synthesis Lectures on Computer Science
Filip Ilievski
Human-Centric AI 
with Common Sense

Synthesis Lectures on Computer Science

The series publishes short books on general computer science topics that will appeal to
advanced students, researchers, and practitioners in a variety of areas within computer
science.

Filip Ilievski
Human-Centric AI
with Common Sense

Filip Ilievski
Vrije Universiteit
Amsterdam, The Netherlands
ISSN 1932-1228 ISSN 1932-1686 (electronic)
Synthesis Lectures on Computer Science
ISBN 978-3-031-69973-3 ISBN 978-3-031-69974-0 (eBook)
https://doi.org/10.1007/978-3-031-69974-0
© The Editor(s) (if applicable) and The Author(s), under exclusive license to Springer
Nature Switzerland AG 2024
This work is subject to copyright. All rights are solely and exclusively licensed by the Publisher, whether the whole
or part of the material is concerned, speciﬁcally the rights of translation, reprinting, reuse of illustrations, recitation,
broadcasting, reproduction on microﬁlms or in any other physical way, and transmission or information storage
and retrieval, electronic adaptation, computer software, or by similar or dissimilar methodology now known or
hereafter developed.
The use of general descriptive names, registered names, trademarks, service marks, etc. in this publication does
not imply, even in the absence of a speciﬁc statement, that such names are exempt from the relevant protective
laws and regulations and therefore free for general use.
The publisher, the authors and the editors are safe to assume that the advice and information in this book are
believed to be true and accurate at the date of publication. Neither the publisher nor the authors or the editors give
a warranty, expressed or implied, with respect to the material contained herein or for any errors or omissions that
may have been made. The publisher remains neutral with regard to jurisdictional claims in published maps and
institutional afﬁliations.
This Springer imprint is published by the registered company Springer Nature Switzerland AG
The registered company address is: Gewerbestrasse 11, 6330 Cham, Switzerland
If disposing of this product, please recycle the paper.

Preface
Like never before and well beyond the imagination of most of us, artiﬁcial intelligence
(AI) software is increasingly becoming commonplace. Seemingly overnight, AI models
that generate textual responses and intriguing images made a grand entry into mainstream
society. AI is now a common discussion topic in talk shows, pop-culture news articles,
podcasts, videos, and city cafés. Some are excited about its prospects, others are fearful
for their safety or impact on their ability to secure income, and a third group is cautiously
optimistic. Amidst this emerging landscape, many people with minimal technical skills
are now happily using ChatGPT to optimize their writing or quickly retrieve information,
or instruct MidJourney/DALL-E to create a logo or image for their presentation slides. In
parallel, initiatives call for regulations and a slowing down of the pace of the development
of AI.
This divergence of perspectives can be traced to the behavior of AI models, which
“never cease to amaze, and never cease to disappoint”, as my Ph.D. supervisor Frank
van Harmelen would say. The ability of large language models, or LLMs, to provide
a witty, or at least reasonable, response to a question or prompt about anything from
acronym generation through recipe alterations and brainstorming about business ideas, is
astonishing. Analogously, their visual counterparts can create a visual representation of
anything the user can think of, from Einstein working on a laptop to psychedelic dreams
and robots playing golf on Mars. But, even the most powerful of these models quickly hit
a wall, where the user just cannot make them behave a certain way. ChatGPT, for instance,
may be unable to understand mathematical or creative expressions and may not reliably
infer the causal implication of an action like “A pointed the cat to B” to mean that A saw
the cat before B. Furthermore, while language is often proclaimed to be a solved problem,
these models still lack a clear understanding of negation and compositional structures, as
apparent from them providing many overlapping answers to items that we do and do not
frequently replace at home.
Over the last ﬁve professional years, I have been grappling with this mixture of fas-
cination and disappointment, of genius and ignorance. My two-word key to this puzzle
v

vi Preface
as of today would be the lack of common sense in AI. Common sense is a longstanding
challenge that has accompanied every AI era since the 1950s. As someone deeply fasci-
nated by the impact of implicit knowledge in people’s communication and sensemaking
of their world, I became passionate about common sense in 2019, when I joined USC/
ISI in California to play a key role in a team participating in DARPA ’s Machine Com-
mon Sense program. With many exceptional researchers like Y ejin Choi, Jure Leskovec,
and Joshua Tenenbaum, the MCS program has been a constant source of inspiration for
me and my students. Five years later, and with the MCS program recently ﬁnished, the
challenge of MCS is much better understood. From today’s standpoint, I ﬁnd it essential
to consider not only the challenge of common sense for its own sake but especially its
role in building trustworthy human-centric AI for the beneﬁt of many.
Commonsense AI is a great community to be a part of, with some excellent mono-
graphs written on this topic. Recent books by Rony Brachman, Henry Levesque, Gary
Marcus, and Ernest Davis argue why really intelligent AI is not yet achievable in the short
term. The 2014 book Representations of Commonsense Knowledge analyzes the intrica-
cies that make representing commonsense knowledge a thorny challenge. In Qualitative
representations: How people reason and learn about the continuous world ,K e nF o r b u s
describes what AI designers can gather from how people reason and learn about the
continuous world, using qualitative representations (e.g., receiving a compliment usually
makes one’s mood more positive). Holyoak and Thagard’s book Mental Leaps is excel-
lent cognitive psychology material about analogical reasoning by people and its role in
generalization over experiences. Gordon and Hobbs’s A Formal Theory of Commonsense
Psychology: How People Think People Think contains comprehensive axioms that deﬁne
aspects of human’s social expectations and folk psychology such as goals, motivations,
desires, and intents. Complementarily, naive physics work has been pioneered by Pat
Hayes, for example, formalizing what it means for a sharp object like a knife to penetrate
a soft surface, like a piece of paper. Thus, prior books have discussed various aspects of
commonsense reasoning, such as its knowledge representation or speciﬁc reasoning types,
e.g., commonsense psychology, analogical reasoning, and qualitative reasoning. I warmly
suggest the reader to further explore these books given interest and time.
Why, then, another book on commonsense AI? The main novelty of this book is its
consideration of common sense not merely as a goal in itself, but primarily as an enabling
mechanism for human-AI frameworks. This human-centric perspective is expressed by
considering how AI can be made collaborative, adaptive, responsible, and explainable
(CARE), and thus beneﬁt social good applications in democracy (e.g., detecting hate
speech online), education (e.g., personalized tutoring and feedback), robotics (e.g., pleas-
ant social companions), and trafﬁc (e.g., reliable monitoring systems). This material
strives to provide a comprehensive overview of prior work on developing common sense
to achieve the CARE goals, thus synthesizing the approach to this challenge across artiﬁ-
cial intelligence subﬁelds and leveraging insights from cognitive psychology, linguistics,
and philosophy.

Preface vii
This book has several unique features that I hope will be informative and inspiring
to advanced students, researchers, and practitioners in a variety of areas within com-
puter science. It has a broad coverage of neural and symbolic methods for commonsense
reasoning, connecting key insights from machine learning, natural language process-
ing, and neuro-symbolic AI. It describes cutting-edge techniques for open-domain tasks
such as question answering and story understanding that require adaptivity, collabora-
tion, explainability, and responsibility. It discusses human-AI applications that can beneﬁt
from commonsense reasoning in AI systems. Finally, it features a rich discussion of
lessons learned and open challenges for commonsense reasoning in human-centric AI,
geared towards interdisciplinary efforts to address hallucinations, low interpretability, and
irresponsible decision-making.
Amsterdam, The Netherlands
November 2024
Filip Ilievski

Acknowledgements The material and ideas in this book are based on serendipity among
a wide network of mentors, collaborators, students, friends, and family.
First, I want to acknowledge the role of every mentor, formal, or informal, which I
had the utmost privilege to know and learn from over the past few years. Piek Vossen,
my Ph.D. promotor always puts his students above everything else (at least that is how
I felt as a Ph.D. student in Piek’s team). From Piek, I have learned to be generous,
to think broadly, and to always consider about the bigger picture. Frank van Harmelen ,
whose passion initially inspired me to pursue research (even when I didn’t exactly know
what this entailed). Frank’s dedication to science and his group of researchers (which
he persistently calls “colleagues” to emphasize that everyone is heard and valued), his
amazingly solid principles, and his ability to demystify and organize thoughts in the most
coherent and logical argument remain an inspiration for me to this date. Marieke van Erp ,
who has the greatest talent of balancing life with work through travels, while exploring
unique, and intriguing interdisciplinary ideas, has been a great support from the ﬁrst day
when we started meeting about my Master’s thesis. Stefan Schlobach, with his deep care
for his colleagues, friends, and students, and his challenging and unique perspective on
research problems, has had a great impact on the way I approach science and my academic
job. From Stefan, I learned to list research hypotheses explicitly and to take bi-weekly
vacations at least once a year.
Ed Hovy, whose reﬂection I always found most profound and whose advice has always
stuck with me for a very long time. To Ed, I owe the realization that “neural networks are
here to stay” (2017) that I can become a great scientist once I recognize my strengths and
work on my weaknesses (2018), and that analogical reasoning is something very different
compared to what I thought (2021). Pedro Szekely, who put a lot of effort into bringing
me to sunny California (with a rhetoric question if it was okay that the USC/ISI insti-
tute was by the beach and not downtown), whose drive for impactful science is led by
deep understanding rather than remaining loyal to particular technologies. From Pedro,
I learned a lot, including always wondering to what extent an idea, if successful, would
be useful. I also learned to organize all communication in documents, avoid quotations
in articles, be mindful of the visual appeal of content, and be explicit about expectations.
Yolanda Gil , an exceptional role model who taught me many great lessons and helped
me win my ﬁrst personal proposal with NSF through thought-provoking questions and
discussions. Thanks to Y olanda, I will never allow myself to miss the pioneers who made
contributions in a certain research area, even if their approach or technology may seem
outdated from today’s perspective (this way of thinking is surprisingly refreshing in com-
puter science, where history typically “begins” a few years ago). Craig Knoblock ,w h o
was the ﬁrst USC/ISI researcher I saw in person, and who has remained a great support
during my time at ISI. Craig stays calm in any situation. Goce Trajcevski, who always
ix

x Acknowledgements and Declarations
gives thoughtful and critical advice, and with whom I always consult before making a
bigger career decision.
I am deeply thankful to each collaborator that I had the chance to breed ideas with over
the past few years. Primarily, I appreciate the collaboration with Kaixin Ma , Jon Fran-
cis,a n d Alessandro Oltramari, informally the “Bosch/CMU”—or the “Pittsburgh guys”. I
started working with them through one of those improbable life circumstances, when we
both published papers whose future work called for pretty much exactly what the other
had been working on—I had a global knowledge graph and Kaixin had a neural reasoner
that could use graphs. Four years later, Kaixin is a very close collaborator—we have
written many papers together, had a great number of online meetings, and even managed
to hang out in person a few times. I have such a huge appreciation for his intelligence,
patience, and team-player attitude, that I have involved Kaixin in the co-supervision of
many of my students. Jon Francis, with his expertise in multimodality and robotics some-
what endemic in my circles, but also with a great scientiﬁc attitude and brilliant ideas, has
been another favorite of mine over the past years. I also want to acknowledge the contri-
bution of Alessandro, with his cognitive background, principled approach, and passion to
contribute to neuro-symbolic AI. Deborah McGuinness, with whom we spent many meet-
ings trying to decipher what exactly qualiﬁes as strengths and weaknesses of language
models, and with whom (together with Alessandro, Kaixin, and Pedro) we wrote one of
my favorite authored papers called “Dimensions of Commonsense Knowledge”. I thank
Kiril Gashteovski and Sascha Saralajew, my close collaborators from NEC Labs Germany.
Kiril, owing to his interest in philosophy and the history of science, is a constant inspi-
ration in terms of next-generation thinking and thinking out of the box. From Sascha,
I learn the scientiﬁc rigor of thinking about methods in theoretical and mathematical
terms, trying to bridge theory and application of algorithms. Pia Sommerauer , a former
Ph.D. colleague at the CLTL group, with whom I have the privilege to ponder together
about analogical reasoning, what it means for the use of language, and whether LLMs
can solve it. Marten Postma, an academic partner during my Ph.D. period, with whom
we spend many cups of coffee and witty remarks to develop our ideas together. Marten’s
ability to organize, structure, and question has been an inspiration for me and has forever
made me a more organized, structured, and critical researcher. Paul Groth, whose ability
to create a vision, communicate it clearly, and follow through has been an inspiration. I
also thank Paul for his support and advice throughout my career. And Hông-Ân Sandlin,
with whom we started working by chance and in an imbalanced setup (me as a replace-
ment PI and she as a sponsor), and have become great collaborators over a short time. I
always appreciate her interdisciplinary insights, ability to think deeply, and her patience
to communicate clearly and thoroughly. Jay Pujara, with whom we often discussed the
importance of structured knowledge and formats like knowledge graphs in the evolving
landscape of AI. Jay is an excellent researcher and a caring mentor. I would like to thank
Mahyar Khayatkhoei and Wael AbdAlmageed, my brilliant computer vision collaborators
with a deep appreciation for reasoning and a desire to think about problems from a new

Acknowledgements and Declarations xi
perspective. I would also like to thank Riccardo Tommasini, who “recruited” me after my
talk at ESWC to work together on memes, which has been a very fruitful direction to
date; and Luca Luceri, with whom we developed this idea further thanks to his expertise
in social media platforms and dynamics. Brad Allen , whom I had the pleasure to meet
during a Dagstuhl seminar in 2022, after which we have been collaborating on research
intersecting knowledge engineering and software architectures. Finally, I acknowledge the
help of Daniel Schwabe and Daniel Garijo, with whom we share a passion for knowledge
graphs and we had many interesting discussions.
Much of the work described in this book and the deep insights we have are thanks to
the dedication of my students. Ultimately, they are the heroes in this story. Jiarui Zhang,
whose dedication and hard work during a remote internship prompted me to accept him
as a Ph.D. student; Yifan Jiang, who has been tireless and respectful, has come up with
several very original directions, including studying brain teasers from an AI perspective;
Zhivar Sourati, who has a great hunger for contributing to research and growth; Darshan
Deshpande, with his great dedication and professional attitude towards making an impact
with LLMs; Prateek Chhikara, who came to me as a new Master student with over a dozen
papers written already, reﬂecting his mature, collaborative, and hardworking nature. I also
want to emphasize the contribution of Saurav Joshi , Abhinav Kumar Thakur , Nic Klein ,
Vishnu Priya, Himanshu Rawlani, Peifeng Wang, Avi Thawani, Kartik Shenoy, Bin Zhang,
and many others.
I thank the organizations that funded my work over the past several years: USA ’s
National Science Foundation (NSF), the Netherlands’ equivalent NWO, the USA Army
Research Lab (ARL), DARPA, Open Philanthropy, and armasuisse.
I want to endlessly thank my partner, Ashley Ilievski , for being a constant source of
support, encouragement, and positive energy, always believing in me, and selﬂessly being
part of my story. She celebrates my successes as hers and dreads my failures more than
I do. I want to also thank my parents, Iljo and Andrijana , and my sister Frosina for their
massive love and support, which has never failed to amaze and nourish me. I am forever
grateful to you. I would like to thank my second family Nestorovski: baba Valentina, dedo
Ljubisa, sisters Amanda and Martina ,a n d brothers Greg and Anthony —you are awesome
and I am most privileged to be part of your family.
Finally, I want to emphasize the importance of my friends, who are an endless source
of inspiration and fun. Georgie, with his eclectic tastes in music, food, and life, and
encyclopedic knowledge in anything; Nawaz, Jovan, Laurie, and Remco , some of the most
sincere and loving people I have ever met; Unmesh, widely appreciated for his big heart
and philanthropic nature; Jayme, a kind soul with whom we share the love for hiking and
nature; Kristina, with whom we hope to form a band; Andrej, with whom I always have
inspiring conversations; Saso, with his support and big heart; Dragan, with his refreshing
views beyond mainstream culture and passion for nature.

xii Acknowledgements and Declarations
Competing Interests The author has no conﬂicts of interest to declare that are relevant to
the content of this book.

Contents
1 Introduction ......................................................... 1
1.1 What Is Common Sense? .......................................... 2
1.1.1 A Brief History of Commonsense AI ......................... 2
1.1.2 Dimensions of Commonsense Knowledge ..................... 3
1.1.3 Dimensions of Commonsense Reasoning ..................... 7
1.1.4 Evaluating Common Sense .................................. 8
1.2 Common Sense: A Solved Problem? ................................ 9
1.3 Human-Centric AI for Hybrid Intelligence Systems ................... 11
1.4 Human-Centric AI with Common Sense? ........................... 12
2 Explainable Commonsense AI ......................................... 15
2.1 Background and Challenges ....................................... 16
2.2 Structure Leveraging Explanations: Path Generation .................. 18
2.3 Architecture Modiﬁcation: Compositional Architectures ............... 20
2.4 Example-Based: Case-Based Reasoning ............................. 24
2.5 Language Modeling Explanations .................................. 29
2.6 Summary and Discussion ......................................... 32
3 Collaborative Commonsense AI ....................................... 37
3.1 Background and Challenges ....................................... 37
3.2 Representing Situations ........................................... 39
3.3 Modeling Self: Planning, Memory, and Interaction Goals .............. 42
3.4 Modeling Other Agents: Theory-of-Mind ............................ 46
3.5 Multimodal Interaction ............................................ 48
3.6 Summary and Discussion ......................................... 51
xiii

xiv Contents
4 Robust Commonsense AI ............................................. 55
4.1 Background and Challenges ....................................... 56
4.2 Data Augmentation with Knowledge Graphs ......................... 57
4.3 Data Augmentation with LLMs .................................... 62
4.4 Methods for Adapting LMs ........................................ 64
4.5 Neuro-Symbolic Reasoning ........................................ 67
4.6 Knowledge Transfer Via Analogical Abstraction ..................... 70
4.7 Summary and Discussion ......................................... 73
5 Responsible Commonsense AI ......................................... 75
5.1 Background and Challenges ....................................... 76
5.2 AI Morality ..................................................... 77
5.3 Bias in Resources and Models ..................................... 81
5.4 Summary and Discussion ......................................... 84
6 Human-Centric AI in Complex Scenarios ............................... 87
6.1 Human-Centric AI for Hybrid Intelligence ........................... 88
6.2 Domain 1: Assisting Moderation for Online Content Safety ............ 89
6.3 Domain 2: Personalizing Education ................................. 95
6.4 Domain 3: Understanding Situations in Trafﬁc ....................... 98
6.5 Domain 4: Object Manipulation and Visual Reasoning by Household
Robots .......................................................... 103
6.6 Summary and Discussion ......................................... 105
7 Conclusions and Outlook ............................................. 109
7.1 Reﬂection on the CARE Principles ................................. 109
7.2 Integrating the CARE Principles ................................... 112
References .............................................................. 115

Acronyms
AI Artiﬁcial Intelligence
AMR Abstract Meaning Representation
CARE Collaborative, Adaptive, Responsible, Explainable
CBR Case-Based Reasoning
CGLI Coalescing Global and Local Information
CSKG Commonsense Knowledge Graph
DARPA Defense Advanced Research Projects Agency
EGM Embodied Goal-Directed Manipulation
EOR Embodied Object Referral
EQA Embodied Question Answering
EVLP Embodied Vision-Language Planning
GPT Generative Pre-trained Transformer
IBR Instance-Based Reasoning
KG Knowledge Graph
LLM Large Language Model
LM Language Model
MOOC Massive Open Online Course
NLP Natural Language Processing
PBN Prototype-Based Network
PG Path Generator
POMDP Partially Observable Markov Decision Process
QA Question Answering
QCM Qualitative Concept Map
SKG Scene Knowledge Graph
ToM Theory-of-Mind
VDN Vision and Dialogue Navigation
VLN Vision Language Navigation
XAI eXplainable AI
xv

1Introduction
Abstract
Commonsense knowledge is information that humans typically have that helps us make
sense of everyday situations. As such, this knowledge can generally be assumed to be
possessed by most people, and it is typically omitted in (written or oral) communication.
The fact that commonsense knowledge is often implicit presents a challenge for auto-
mated methods in natural language processing and question answering as the extraction
and learning algorithms cannot count on the commonsense knowledge being available
directly in text. As such, commonsense knowledge and reasoning have been considered
the “black matter” of AI, raising concerns about the trustworthiness and applicability of
AI methods in automated and hybrid applications, especially social good applications
in misinformation, trafﬁc, health, and education. While large models are often hypoth-
esized to have acquired various commonsense skills implicitly during their training on
massive amounts of data, further experiments show that such skills are seldom robust,
controllable, and communicable to users consistently, causing a lack of trust. This chapter
provides a brief introduction and history of the research in AI on the topic of common
sense. It unpacks commonsense AI through dimensions of knowledge and reasoning.
It summarizes efforts to evaluate common sense abilities in AI models and discusses
their present level of success. The chapter describes why common sense is still an open
challenge and introduces four requirements for AI to be human-centric, i.e., adequate
to augment humans on complex tasks. The chapter concludes with an overview of the
organization of this book, which aims to bridge the gap between commonsense reasoning
research and the requirements of human-AI teaming.
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_1
1

2 1I n t r o d u c t i o n
1.1 What Is Common Sense?
In the groundbreaking DARPA program Machine Common Sense (MCS), common sense
has been notionally deﬁned as “the basic ability to perceive, understand, and judge things that
are shared by nearly all people and can be reasonably expected of nearly all people without
the need for debate”.
1 Common sense can be seen as a combination of knowledge that is
commonly assumed from everyone and the inferences that this knowledge enables [ 71].
Commonsense knowledge is the information that people typically have that helps us make
sense of everyday situations [
150]. What exactly is that knowledge? John McCarthy [ 226]
describes that commonsense knowledge includes the basic facts about events (including
actions) and their effects, facts about knowledge and how it is obtained, and facts about
beliefs and desires. It also includes the basic facts about the material objects and their
properties. Broadly, this knowledge can be grouped into naive physics, folk psychology, and
common facts.
Per deﬁnition, commonsense knowledge does not require a particular background, expe-
rience, or education. Being (somewhat) widely shared, commonsense knowledge tends to
be omitted in written and oral communication. Namely, pragmatic laws of communication,
such as Gricean’s maxim of quantity [
125], dictate that, to ensure effective and efﬁcient
communication, assumed (obvious) information should be avoided. Exactly this assumed
and implicit nature of common sense is what is often considered to be the reason for its
reputation as a thorny AI challenge, difﬁcult to distill from data and to deﬁne its scope. The
notion of common sense also has its controversies, as much of what can be considered to be
commonsensical is often relative to cultural, social, and spatiotemporal contexts [
230].
1.1.1 A Brief History of Commonsense AI
Being essential for sensemaking of everyday situations and yet not being communicated
explicitly, makes common sense the “dark matter” of AI. Commonsense AI has a long his-
tory of efforts that trace back to John McCarthy’s essay Programs with common sense in
the early days of AI. Since then, for decades, AI researchers worked on theories of common
sense, including naive physics [
137], commonsense psychology [ 120], and qualitative rea-
soning [ 94]. Arguably, the monumental effort behind Cyc [ 189] marks a culmination of the
symbolic methods, largely focused on how to collect and organize pieces of commonsense
knowledge into a puzzle that is both coherent and useful for reasoning. With the turn of the
century and scalable techniques such as crowdsourcing, researchers explored the creation
of resources with a focus on size and scale rather than clean organization of knowledge.
Such resources are ConceptNet [
203]a n dA T O M I C[303], both of which have been used by
many systems for natural language processing tasks. Efforts to consolidate such sources in
1 https://www.darpa.mil/news-events/2018-10-11, accessed on Nov 15, 2023.

1.1 What Is Common Sense? 3
a bottom-up fashion have followed, aiming to devise a uniﬁed commonsense resource from
a set of atomic facts and beliefs [ 150, 152].
Meanwhile, advances in neural information extraction and language modeling brought
a natural question: can commonsense knowledge and reasoning be extracted or learned
from data directly? Information extraction pipelines can be designed and implemented to
extract commonsense patterns as large structured resources, albeit with lower precision [
242,
258]. Meanwhile, the idea of language models as knowledge bases [ 276]h a sl e dt oas e r i e s
of efforts that use manually curated knowledge sources to steer the associations learned
by language models in the desired direction. Ultimately, the current era of large language
models, including the Generative Pre-trained Transformer (GPT) series and other models
like Llama, has brought a new paradigm in which such knowledge can be extracted without
any ﬁne-tuning, by merely providing the model with instructions and demonstrations [
239].
Distillation methods can be introduced to further engineer and reﬁne the quality of the
extracted knowledge [
383].
The paradigm shift in AI has inspired researchers to leverage such models for a vari-
ety of commonsense skills, including theory of mind, causality, and analogical reasoning.
Commonly, the tasks have been phrased as either discriminative (e.g., multiple choice ques-
tion answering) or generative (e.g., storytelling). Moreover, there has been a wide range of
applications to not only textual tasks within natural language processing (NLP), but also
computer vision, planning, and robotics. Commonsense knowledge can be used to ﬁll gaps
and explain the predictions of a (neural) model [
195], understand agent goals and causality
in stories [ 389], or enhance robot navigation and manipulation [ 395]. Its beneﬁts have been
shown early on in downstream applications, such as software requirements localization [ 263]
and aligning local laws with public reactions [ 283].
1.1.2 Dimensions of Commonsense Knowledge
McCarthy deﬁnes commonsense knowledge through extension as follows. “Commonsense
knowledge includes the basic facts about events (including actions) and their effects, facts
about knowledge and how it is obtained, facts about beliefs and desires. It also includes the
basic facts about material objects and their properties.” While this deﬁnition provides an
intuition of how broad the world of commonly assumed knowledge is, in practice, applying
this deﬁnition is challenging. For instance, given a very large graph of human knowledge,
like Wikidata [
364], how can we approximate its “commonsense knowledge” subset? What
does it mean to build a model, resource, or benchmark that is representative of common-
sense knowledge? How should the knowledge types be chosen? What is the right level of
abstraction for relations and concepts?
To provide an insight into these questions, existing resources of commonsense knowledge
provide a useful entry point. These resources have been created using different techniques,
cover a variety of domains, and are based on a wide list of representational decisions.

4 1I n t r o d u c t i o n
Table 1.1 Overview of commonsense knowledge sources. The asterisk (‘*’) indicates that the source
is extended with WordNet knowledge. For FrameNet and MetaNet, we specify their numbers of frame-
to-frame relations. WebChild contains a large number of relations, expressed as WordNet synsets,
which are aggregated into 4 groups
Category Source Relations Example 1
Commonsense KGs ConceptNet* 34 F ood - capable of - go rotten
ATOMIC 9 Person X bakes bread - xEffect - eat food
WebChild 4 (groups) Restaurant food - quality#n#1 - expensive
Quasimodo 78,636 Pressure cooker - cook faster - food
SenticNet 1 Cold_food - polarity - negative
HasPartKB 1 Dairy food - has part - vitamin
Probase 1 Apple - is a - food
Isacore 1 Snack food - is a - food
Common KGs Wikidata 6.7k F ood - has quality - mouthfeel
Y AGO4 116 Banana chip - rdf:type - food
DOLCE* 1 n/a
SUMO* 1,614 F ood - hyponym - food_product
Lexical resources WordNet 10 F ood - hyponym - comfort food
Roget 2 Dish - synonym - food
FrameNet 8 (f2f) Cooking_creation - has frame element -
Produced_food
MetaNet 14 (f2f) F ood - has role - food_consumer
VerbNet 36 (roles) Feed.v.01 - Arg1-PPT - food
Visual sources Visual Genome 42,374 F ood - on - plate
Flickr30k 1 A food buffet - corefers with - a food counter
Corpora & LMs GenericsKB n/a Aardvarks search for food
GPT-2 n/a F ood causes a person to be hungry and a
person to eat
In [ 150], we surveyed 20 popular commonsense knowledge sources, ranging from com-
monsense knowledge graphs through lexical and visual sources, to the recent idea of using
language models or corpora as commonsense knowledge bases. The selected 20 represen-
tative commonsense sources belonged to ﬁve categories: commonsense knowledge graphs
(KGs), common KGs, lexical sources, visual sources, and corpora and language models.
Table
1.1 shows these categories with their sources, described with their relations and an
example knowledge statement.
The heterogeneity of these sources hinders their joint usage. It also prevents potential
users from having a global view of the kinds of knowledge available in commonsense
knowledge resources. To address these gaps, we manually categorized the relation types in
these sources into 13 dimensions. Each dimension can be seen as a cluster of its speciﬁc
relation types, as found in the sources. These emergent dimensions are as follows:

1.1 What Is Common Sense? 5
1. Lexical knowledge includes relationships such as plural forms of nouns, past tenses of
verbs, and substrings. Such relations are ConceptNet’s DerivedFrom, described as
capturing when a word or phrase appears within another term and contributes to that
term’s meaning. Lexical knowledge can also relate a concept with its expression in a
language, as done by Wikidata’s labelrelation.
2. Similarity includes notions of synonymy between expressions (e.g., Synonymin Con-
ceptNet and WordNet), broader similarity ( SimilarToin ConceptNet), and concept
deﬁnitions ( DefinedAs).
3. Distinctness complements similarity with notions of distinguishability, such as
antonymy (e.g., Antonym in both ConceptNet and WordNet), mutual exclusion
between roles of a situational frame (e.g., Excludes in FrameNet), and explicit
statement of distinctness for concepts that might be mistaken as synonyms (e.g.,
different fromin Wikidata).
4. T axonomic knowledge enables an arrangement where some objects are placed into
more general and more speciﬁc groupings with inheritance relations, like Hyponymy
in WordNet and IsAin Wikidata. Taxonomic relations can distinguish between concepts
and instances, e.g., using Wikidata’s SubclassOfand InstanceOf, or speciﬁcally
model verb inheritance ( MannerOfin ConceptNet).
5. Part-whole models knowledge about a concept being a part of ( PhysicalPartOf
in WebChild), a member of ( MemberOf in WebChild), or a material substance used
to build an object ( MadeOfin ConceptNet). Part-whole knowledge can be transitive,
such as that of geographic containment, exempliﬁed by New York City being a part of
New York State, which is also part of the United States.
6. Spatial relations describe terms relating to or occupying space, indicating the usual
location of a concept ( location in Wikidata), permanent location of geographical
entities (AtLocationin ConceptNet), or spatial proximity ( LocatedNearin Con-
ceptNet).
7. Creation describes the process or the agent that brought something into existence. An
example relation for a process is ConceptNet’s CreatedBy, while an agent creator
can be indicated with Wikidata’s creatorrelation.
8. Utility covers a notion of ﬁtness or usefulness of objects for some purpose. Such rela-
tions are ConceptNet’s UsedForfor modeling the purpose of objects, CapableOf
for modeling the capability or affordance of objects, and ReceivesActionfor indi-
cating a common action that an object receives and may respond to.
9. Motivational knowledge covers social knowledge about an agent’s desires ( Desires
in ConceptNet), goals ( MotivatedByGoalin ConceptNet), or intentions ( xIntent
in A TOMIC). It may be relevant to include negative statements through relations like
NotDesiresand ObstructedByGoal. Motivational knowledge can describe the
state of the self-agent or other agents.

6 1I n t r o d u c t i o n
10. Quality knowledge describes attributes of an agent ( xAttrin A TOMIC) or qualities
r e l a t e dt oa no b j e c t(HasPropertyin ConceptNet). Properties can be further speciﬁed
into taste, temperature, shape, or color, as done in WebChild, Wikidata, and SenticNet.
11. Comparative knowledge can be directly expressed based on the relative values
of object attributes. E.g., WebChild includes relations such as HealthierThan,
FasterThan,a n d LargerThan.
12. T emporal knowledge revolves around the notion of time to support ordering
(HasFirstSubevent in ConceptNet), capture relations of prerequisites and con-
sequences of events ( HasPrerequisite in ConceptNet), and explicitly indicate
causal effects of events ( xEffectin A TOMIC). Causes can impact the self-agent or
other agents.
13. Other relational knowledge includes remaining relations, often underspeciﬁed, that
cannot be placed in the previous twelve categories. These include a description of gen-
eral context ( HasContextin ConceptNet), its speciﬁc variants (e.g., Depictsand
HealthSpecialtyin Wikidata), and vague semantic connections between concepts
(e.g., using RelatedToin ConceptNet).
These 13 dimensions provide a useful conceptual framework for the range of common-
sense knowledge. We leveraged them in practice to enhance the statements in the consoli-
dated Commonsense Knowledge Graph (CSKG) [
152] with dimension information, which
enabled a study of the coverage and overlap of the existing knowledge in prior sources, their
relation to knowledge in language models, and their impact on enhancing the commonsense
reasoning ability of these models on downstream tasks.
At the same time, these dimensions are by no means the only, nor the best, formalism
that describes the set of commonsense knowledge types. Existing commonsense knowl-
edge graphs make implicit categorizations of knowledge, by deﬁning a tractable set of
relations that can be traced to some types proposed in cognitive research. For instance,
WebChild’s [
341] part-of relations resemble the partonomic-metonymic relations in cog-
nitive science literature (e.g., see [ 45, 390]), while ConceptNet [ 331] deﬁnes 34 relations,
where the relation IsAcan be often approximated with taxonomic knowledge. In its ﬁrst
version [ 203], ConceptNet deﬁned 20 relations grouped into 8 categories: K-lines, Things,
Agents, Events, Spatial, Causal, Functional, and Affective. Zhang et al. [ 403] extrapolate
the types in the Conceptual Semantic Theory with those in ConceptNet 1.0 and propose the
following six categories: property, object, eventuality, spatial, quantity, and others. Based
on insights from developing Cyc, Lenat deﬁnes 12 contextual dimensions [
188]: Absolute
Time, Type of Time, Absolute Place, Type of Place, Culture, Sophistication/Security, Gran-
ularity, Justiﬁcation, and Anthropacity. Beyond commonsense knowledge resources, there
exists seminal work on top-down axiomatization of common sense, such as Pat Hayes’ naive
physics [
137], Gordon and Hobbs’ commonsense psychology [120], and Ken Forbus’ work
on qualitative commonsense reasoning [94].

1.1 What Is Common Sense? 7
1.1.3 Dimensions of Commonsense Reasoning
Can we deﬁne orthogonal dimensions of commonsense reasoning, similar to the knowledge
types in the previous section? This is arguably more challenging: even the seemingly disjoint
directions of physical and social reasoning have a lot in common, as witnessed by the exten-
sive introduction to physical reasoning in the commonsense psychology book by Gordon
and Hobbs [
120]. Yet, it is a useful exercise to delineate different reasoning dimensions, as
this would enable us to understand the state-of-the-art theories, method developments, and
evaluation procedures for each dimension separately. Inspired by seminal work on common-
sense theories, systems, and benchmarks, we can distill common categories of commonsense
reasoning:
Physical reasoning and monitoring refers to a system of skills required to understand
the observable parts of a given situation, through reasoning over affordances, quantities, and
scales [
110]. In addition, physical monitoring enables the grasp of the situational dynamics
over time and space through mechanisms like state changes and qualitative reasoning [ 94].
For example, physical reasoning agents can understand that a standard mug would ﬁt in a
sink, that it can be used to drink warm or cold drinks, and that it cannot contain a liter of
liquids. It can also contain knowledge that the mug becomes less ﬁlled once someone drinks
from it.
Causality is required to understand the prerequisites and effects of agent actions and
events [ 274]. Actions and events have implications on other events (e.g., one event may
hinder the occurrence of another), objects (e.g., an event may damage an object), or agents
(e.g., an event may increase an agent’s temperature). Causality includes defeasibility, i.e.,
reasoning under altered expectations, and counterfactual reasoning, i.e., the ability to reason
about the implications of hypothetical situations.
Planning is a commonsense skill that enables agents to reach a goal state given a domain
description (including possible actions) and an initial state, by a sequential decision-making
process of action selection. As planning is often done in dynamic environments, it includes a
plan adaptation skill, where the initial plan must be adapted to the environmental constraints
and other information. For example, an agent may plan to reach the bedroom by navigating
through the kitchen door, turning right to face the hallway, walking straight, and push down
the handle of the bedroom door. If the bedroom door turns out to be locked, the agent needs
to adapt its plan and ﬁrst unlock the door before operating its handle.
Agent reasoning encompasses a broad reasoning category of modeling agent beliefs,
desires, goals, expectations, and emotions [ 120]. Agent reasoning models are constructed
both for the self-agent as well as for other agents, where the latter is often referred to as
Theory-of-Mind. For example, an agent may desire to see a dramatic movie and may expect
that their partner would come because they share the interest in dramas.
Cultural reasoning refers to comprehending values, morals, norms, and ethics, which
often underlie the actions taken by the agents in the environment and their social reasoning
about themselves and other agents. For example, it is unethical to play loud music at night,
and at a certain decibel level, it is also against the law.

8 1I n t r o d u c t i o n
Similarity and analogy enable to abstract individual experiences and connect situations
based on surface overlaps (literal similarity) or relational correspondence on an attribute,
proportion, or system level (analogy) [
107]. For example, an agent may draw an analogy
between a bird building a nest and a young couple constructing their family house.
Multimodal reasoning is required in prolonged interaction with the environment, includ-
ing considerations of embodiment (the relation between a body and its physical environment)
and time (interactions develop over time, often growing in complexity). For example, follow-
ing a movie requires one to understand the visual signals and the dialogue, and occasionally
read out the caption text.
These categories are intended to give the reader an idea about the scope of what is gener-
ally considered commonsense reasoning in AI. These topics will be recurring throughout the
book chapters with discussion on them from the perspective of various goals, e.g., robust-
ness or collaboration. They belong to vertical thinking , also known as linear, convergent, or
logical thinking: a sequential analytical process that is based on rationality, logic, and rules,
typically associated with the left-brain hemisphere. Orthogonally, there are reasoning cate-
gories that defy common sense. These reasoning categories can be seen as lateral thinking a
divergent and creative process that involves looking at a problem from a new perspective and
defying preconceptions, associated with the right-brain hemisphere [
73, 160, 367]. Lateral
thinking requires breaking out of the box, which is challenging for machines because it
requires a clear expression and overwriting of commonsense assumptions.
1.1.4 Evaluating Common Sense
It is a common practice in AI research to evaluate the ability of models to perform certain
tasks through benchmarks and quantitative metrics. The improvements brought by language
modeling across many AI tasks have encouraged the community to revisit the challenge of
commonsense reasoning. Thus, the last few years have featured an increased focus on bench-
marks that can be used to evaluate different aspects of common sense, typically in the format
of multiple-choice question answering. Social commonsense reasoning datasets [
305] focus
on reasoning about people’s actions and their social implications. Given an action (e.g.,
Jesse saw a concert) and a question (e.g., why did Jesse do this?), plausible explanations
are that Jesse “wanted to see their favorite performer” rather than “see if it works”. Physi-
cal [
31] commonsense reasoning evaluates whether models understand physical interactions
in everyday situations (e.g., it is possible to use a shoe as a doorstop). Visual commonsense
reasoning [402] evaluates whether systems can comprehend plausible depicted interactions
(e.g., a person pointing to pancakes in a restaurant). Numeric reasoning [ 197] deals with
models’ ability to understand exact and approximate links between numbers and everyday
objects in domains like biology, geometry, and physics for example, ants have six legs and
a cube has six faces.
Besides discriminative tasks [ 31, 305, 339], where the goal is to pick the single correct
answer from a list, there has been also much focus on generative tasks, where one has to
generate one or multiple correct responses [
36, 197]. Generative tasks are attractive because

1.2 Common Sense: A Solved Problem? 9
they enable evaluation without the need to create fair and informative distractor answers,
however, their evaluation is hindered by the lack of adequate evaluation metrics. Moreover,
recent work has found a generative paradox of models performing poorly in discriminative
settings on tasks they generated themselves [
384], prompting a switch away from generative
benchmarking.
As question-answering tasks are limited in terms of their context length and lack interac-
tion, other tasks have attracted attention. The story cloze task [ 248] asks systems to distin-
guish between plausible and implausible stories, optionally pointing to the participant states
and conﬂicting information in the implausible story [
334]. Story generation tasks [ 198]a s k
models to complete a story based on a prompt and an initial context. Dialogue modeling
and generation tasks mirror their story counterparts [ 47, 377], but also add the interactivity
of communication, where later turns depend on earlier utterances. Dialogue generation can
also be personalized to the attributes of the speaker [
407]. Extending interactivity further,
text-based games [ 376] have emerged where the system needs to navigate a simulated envi-
ronment only through natural language communication, by performing sequential decisions.
As coherence over longer interactions has been found to be a challenge for the models, spe-
cialized datasets [
412] have focused on measuring the consistency of model answers across
variations of the same input. Finally, some efforts have focused on contexts that defy com-
monsense associations, such as lateral thinking puzzles [
160]. Many of the tasks described
in this section will be used to demonstrate and evaluate techniques throughout this book.
These tasks can be tackled by using (the entire or a subset of the) training data [ 195,
214], or in a zero-/few-shot evaluation regime [ 215, 320]. While ﬁne-tuned systems often
perform similarly to humans on average, their ability to generalize to novel tasks is limited.
In-context learning of frozen large language models (LLMs) is a more recent idea, which
does not require model tuning and assumes minimal knowledge about the target domain,
with the caveat of using models that may not be accessible and reproducible. However,
given the strong improvements in zero- and few-shot settings brought by in-context learning
variants across tasks, many believe that machine common sense is either a solved problem
or one that can be solved very soon with the introduction of slightly larger models.
1.2 Common Sense: A Solved Problem?
The strong performance of LLMs across a wide variety of tasks and benchmarks has been
attributed to the so-called emerging abilities of these models. The emergence of abilities
is a phenomenon where a model trained to perform simple language tasks, like next word
and next sentence prediction, can generalize to new tasks such as question answering and
dialogue generation. These claims, as discussed in the previous section, are supported by
benchmark scores, which show clear upward trends from prior state-of-the-art techniques.
These observations have inspired many studies that shed light on the question: Is the chal-
lenge of commonsense reasoning now solved? We now discuss recent studies in three rea-

10 1I n t r o d u c t i o n
soning dimensions: planning, agent reasoning, and analogies, while the rest of the chapters
provide further evidence for challenges on these and other reasoning categories.
In the domain of planning, the planner-actor paradigm has currently been modeled with
multiple language models, forming a multi-agent system. On tasks like text-based games,
these models have improved over reinforcement learning and the single LM baselines,
indicating their ability as planners [
196]. At the same time, closer investigation has shown that
while LLMs can generate reasonable plans, they cannot adapt these plans in consideration of
environmental constraints [
358]. To facilitate an effective planning system, LLMs currently
need to be associated with a deterministic AI planner that can beneﬁt from their plans and
bridge the gap to the environment.
The ability to impute unobservable mental states to others, often called Theory of Mind ,
has been recently attributed to LLMs [ 178]. Given a set of 40 false-belief tasks, the models
with a larger size could solve 75% compared to the 20% solved by the smaller model from
only four months earlier. However, this ﬁnding was further probed in follow-up work, where
Ullman [
357] showed that the same LLM performs much worse when the original prompt
is trivially altered through four categories: transparent containers, uninformative labeling,
trusted testimony, and late labeling, concluding that LLMs do not (yet) show robust ToM
skills.
Starting from the Word2V ec era of word embeddings, through the Transformer models
and the in-context learning (ICL) techniques, there have been strong claims that embeddings
are a natural solution to creating human-like analogies [
235, 399]. While the simpler form
of proportional analogies can indeed be approximated with today’s large language models
to some extent, their reliance on surface similarities prevents them from performing reliable
abstraction when it comes to more complex, structural analogies [
329, 387]. In particular,
all models perform close to random when they need to identify analogies between stories
that are dissimilar on the surface, and this performance is still halfway between random and
humans after extensive prompt engineering.
In summary, we ﬁnd that the strong claims for the emerging skills of language models
are somewhat anecdotal and only partially accurate. The apparent discrepancies between
ﬁndings by different studies can be generally resolved through a more precise deﬁnition
of the goal post. If the question is whether language models show some ability to perform
a given task (say analogy or planning), e.g., better than prior models, then the answer is
a clear yes. Language models can often produce plans, reasoning chains, and analogies
that may puzzle and inspire people. Conversely, if the question is whether the models can
reliably perform or explain a certain commonsense skill (and for instance, be trusted to
perform it autonomously in an application domain), then the answer becomes not yet .T h e s e
same models that excel on benchmarks often produce inconclusive reasoning chains, make
decisions that counter their arguments, or produce utterances that are inconsistent over longer
interactions or across slight task formulation variants [
384].

1.3 Human-Centric AI for Hybrid Intelligence Systems 11
1.3 Human-Centric AI for Hybrid Intelligence Systems
In times when our society is dealing with many challenges, such as global pandemics,
resource scarcity, environmental sustainability, climate change, and democracy threats [ 4],
it is attractive to consider the path. Complementary teams of humans and AI could be
envisioned to work together to achieve common goals on complex tasks [
232]. This vision
is, above all, supported by the accessibility of large models for the general public. While large
pretrained models would be only accessible to experts until recently, today’s models like
ChatGPT and Dall-E are intended to be used by everyone on the Web. As such, these models
already gain social and political importance, impacting the lives of many people in a variety
of ways as a tool that can (potentially) augment humans for writing, decision-making, and
scientiﬁc discovery [
4]. This vision is further supported by evidence that human and artiﬁcial
intelligence are often complementary in nature, e.g., AI could enable teams to overcome
people’s cognitive limitations. However, if AI is to fulﬁll such a role of augmenting people,
it must be human-centric to the extent that people will see it as a reliable, trustworthy, and
effective teammate. What does it mean for AI to be synergistic. We now discuss four key
requirements, adapted from the CARE principles (collaborative, adaptive, responsible, and
explainable) in [
4].
A key aspect of human-centric AI is robustness (adaptivity) , i.e., the requirement that
AI can learn and adapt to people and our environment. In light of the needs of real-world
applications, AI research has increasingly focused on benchmarks, methods, and studies
that study the model’s ability to generalize robustly [
154, 412]. Here, adversarial studies
have demonstrated that current AI approaches are not as robust as hoped. For instance,
both visual object detection [ 393] and textual information extraction [ 118, 156] models
signiﬁcantly alter their predictions based on negligible input variations, even for simple tasks,
showing limited generalizability when they are exposed to text perturbations, noisy data, or
distribution shifts [
245]. Together with informative signals, the models also pick on spurious
correlations between terms [ 104] and annotation biases [ 109], while being insensitive to
subtle variations like negation [ 218]. Models struggle with connecting situations via higher-
order similarities [ 254], reasoning in novel situations [ 223], and their performance is largely
correlated with training data frequencies [ 294, 373]. Models do not consistently reason
across variations of the same generative task, nor they are able to discriminate the choice
that they generated [
384], resulting in paradoxical behavior. These ﬁndings inspired an arms
race between the robustifaction of models [ 209] and breaking their robustness [ 271, 322].
Even though impressive results have been achieved over the last years on both ends [ 38, 41,
121, 361], the robustness of models is still far behind human abilities [ 85].
Another aspect is explainability and interpretability , AI and people to be transparent
about their goals, awareness, and strategies. The requirements for interpretability are intu-
itive for high-stake domains that affect health, racial bias, and safety [
300], where model
errors can have serious consequences on human lives. More fundamentally, interpretability is
an essential component of developing trustworthy technology that can be adopted by experts
in any domain [
323, 366]. Work on interpretable and explainable methods has grown signif-

12 1I n t r o d u c t i o n
icantly in popularity, resulting in explainable leaderboards [ 204], research on explainability
metrics [411], and the development of interpretable and explainable AI methods [ 300]. The
widely adopted pre-trained language models that report exceptional accuracy on NLP clas-
siﬁcation benchmarks [
55, 415] have limited interpretability by design, which cannot be
fully mitigated by posthoc explainability techniques [ 414]. Meanwhile, interpretable mod-
els exist, but their performance is generally lower and their interpretability mechanisms are
often not meaningful for humans in practice.
Besides being explainable, AI must also have collaborative mechanisms, promoting it
from a tool into a meaningful partner for tasks like negotiation, planning, and behavior
change support [
4]. Achieving meaningful progress towards collaborative AI requires a bet-
ter understanding of human actors, including a theory of mind [ 76], an understanding of
joint actions in a multi-agent scenario [ 127], and a model of social norms, such as reci-
procity [ 296]. Human-in-the-loop and interactive AI approaches are a promising ﬁrst step
toward collaborative AI system development [ 10]. However, AI today still ampliﬁes human
biases, including in-group favoritism and conﬁrmation bias [ 58], has a limited ability for
memorization [326], and lacks comprehension of affective and social behavior [ 148]. More-
over, collaboration requires integrated modeling of multiple modalities, whose transition
from the lab to open-world settings has been enhanced by models like GPT-4 [
265], yet, a
long way forward remains for it to be effective in human-AI teams [ 313].
Finally, AI must be responsible, i.e., operate within legal constraints and social and
ethical values in a domain. By learning over large amounts of data, current state-of-the-
art models represent a medium that mimics or averages the worldviews of many people
and the considerations of many applications, tasks, and domains. As such, clear modeling
of values, ethical norms, and legal constraints is not well-integrated into contemporary
models. Integrating the (potentially conﬂicting) stakeholder values [
360], formal modeling of
provenance and perspectives [ 164], and reasoning within ethical and legal constraints [ 340]
are challenges for today’s AI, hindering its responsible use for a variety of domains and
tasks. Instead, the currently dominant data-driven AI paradigm largely optimizes for the
quantity of data, while simultaneously decoupling each data point from its original context
and simplifying the variety of the world it comes from [
61]. Each dataset, whether considered
biased or not, contains a worldview, and responsible AI needs to embrace this worldview.
Instead, by assuming that bias is a bug to be ﬁxed through taxonomizing the data, the
data engineering process generally abstracts over that worldview. While this abstraction is
often seen as a neutral act, it implies inherently political, cultural, and social views of the
engineer [
61].
1.4 Human-Centric AI with Common Sense?
In summary, AI research and development ﬁnds itself in an unprecedented situation. On the
one hand, signiﬁcant improvements have been measured across benchmarks, e.g., in NLP
and computer vision, mainly owing to scaling up in terms of data and computation. Coupled
with a vision of generative assistants for people, these techniques have rapidly been launched

1.4 Human-Centric AI with Common Sense? 13
into the mainstream, enabling millions of non-experts to interact with the most powerful
models in intuitive ways, primarily via natural language. On the other hand, AI techniques
are still inadequate today to participate in hybrid intelligence teams with people, owing
to commonsense challenges summarized along four dimensions: robustness explainability,
responsibility, and collaborativeness. Concerns about the ability of AI to perform mental
modeling, understand ethics and values, show situational awareness, plan reliably, and model
causality have mounted, together with indications that AI’s behaviors are often inconsistent
across task formats (discriminative vs generative), prompt formulations, and through time.
The premise of this book is that the lack of common sense is a major obstacle to building
AI that can effectively augment people and participate in hybrid intelligence teams. Indeed,
the current confusion in the AI landscape can be summarized in ﬁve words: AI still lacks
common sense [40, 72, 219]. This realization has inspired a long line of renewed interest in
one of the oldest AI challenges, resulting in a rich landscape of evaluation tasks, neural and
symbolic advances, overlaps between AI and other disciplines (e.g., cognitive psychology),
and ﬁndings and conclusions that appear to contradict prior ﬁndings in similar settings. The
goal of this book is to organize this landscape, describing state-of-the-art commonsense rea-
soning techniques, tasks, and benchmarks, with their limitations and strengths, concerning
the human-AI teaming goals.
The book is organized along the four hybrid intelligence requirements of human-centric
AI. How can we approach building explainable, collaborative, adaptive and responsible
AI with common sense? Research on commonsense AI from the perspective of each of
these four requirements will be discussed in turn in four dedicated chapters (Chaps.
2–5).
Each chapter will sequentially discuss challenges in commonsense AI for that requirement,
provide an overview of state-of-the-art techniques, summarize current evaluation results,
and end with a summary and a corresponding discussion. In Chap.
6, human-centric AI is
considered from four representative and complementary teaming scenarios in the domains
of content safety, trafﬁc, education, and robotics. The book is then concluded in Chap.
7 with
a set of reﬂective remarks, lessons learned, and a list of open challenges toward building
human-centric AI with common sense.

2Explainable Commonsense AI
Abstract
With the stakes of AI increasing, there is a recognition that a key requirement of a
human-centric AI is explainability. This recognition has inspired a range of methods for
making AI explainable, either during or after its main inference process. Such explain-
able AI (XAI) efforts form an extensive taxonomy of approaches differing in their scope,
stage, input/output format, result, and functioning. The most popular idea in these XAI
methods is to localize the part of the input or the network that is most responsible for a
given prediction. As much of the real-world inference relies on implicit commonsense
information, it requires specialized XAI methods that explain a decision by including
this implicit information in their explanations. This chapter discusses the challenges in
developing commonsense explanation systems, including the implicit nature of common
sense, alignment between the explanation and the model result, and incompleteness of
explanations. Then, we describe several neuro-symbolic methods that can be mapped to
popular XAI functioning categories: structure leveraging explanations through path gen-
eration, architecture modiﬁcation model based on compositional reasoning, and example-
based explanations via case-based reasoning. The chapter also covers another category
of commonsense explanations, based on language modeling mechanisms, enriched with
rationale models and chain-of-thought reasoning. The chapter concludes with a summary
of the state-of-the-art explainable commonsense AI and a discussion of its limitations and
open challenges. We discuss customary procedures and metrics for evaluating common-
sense explanations, challenges with the quality of the current commonsense explanations,
and gaps between commonsense explanations in AI and social science.
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_2
15

16 2 Explainable Commonsense AI
2.1 Background and Challenges
With the stakes of AI increasing, there is a recognition that a key requirement of a human-
centric AI is explainability. This recognition has inspired a range of methods for making AI
explainable, either during or after its main inference process. Such explainable AI (XAI)
efforts form an extensive taxonomy of approaches. A recent review of XAI taxonomies [ 332]
has indicated that the XAI landscape is difﬁcult to access for new scholars, but also hard
to keep track of new developments for experienced scholars. According to this work, XAI
methods can be distinguished primarily in terms of their scope, stage, input/output format,
result, and functioning.
A meta-taxonomy of XAI methods could be organized as in Fig. 2.1. Speciﬁcally, explain-
ability can be either by design (ante-hoc) or post-hoc. Ante-hoc explainability is also known
as interpretability, referring to models where the trace between the input and the output is
interpretable. An example of an interpretable, ante-hoc model is any sparse linear model.
Conversely, post-hoc explanation techniques are used to explain the behavior of black-
box methods, e.g., deep neural networks. Post-hoc methods differ in terms of their model
dependency—they can be either model-speciﬁc or model-agnostic, based on the assumptions
they make about the model architecture. In terms of the scope of the produced explanations, a
common distinction is between local (per prediction) and global (for the whole model). The
result of an explanation is usually either a surrogate model, a feature relevance data struc-
ture, or a set of examples. These results generalize over different modalities of explanations,
including numbers, text, visual data, and rules.
A key distinction between XAI methods can be made between their functioning algorithm.
Arguably, the most common category of XAI algorithms is perturbations—methods that
investigate the impact of the input features on the model output. Some of the most popular
Fig. 2.1 Taxonomy of XAI methods, courtesy of [ 332]

2.1 Background and Challenges 17
XAI methods, such as LIME [ 295] and SHAP [ 213], belong in this category. The family of
structure leveraging models is based on exploiting the properties of machine learning models
to construct the explanation. These models usually examine the gradients of a model, as done
in GradCam [
309], or alternatively the attention mechanisms [ 243]. Multiple explanatory
models can be combined through meta-explanation models, like MetaLion [ 244], including
an evaluation of truthfulness to decide how to combine the individual explanations and an
argumentation framework that justiﬁes its explanation. The fourth category of explanation
through architectural modiﬁcations is illustrated by surrogate model approaches that extract
decision trees [
406] to approximate the logic of a neural network. A ﬁnal family is the
one of example-based explanation, including case-based [ 172] and prototype-based [ 306]
explanations.
Notably, most XAI methods aim to localize the part of the input or the part of the network
that is most responsible for a given prediction. While this categorization is meaningful
across the board of AI applications, commonsense explanations are unique in that they rely
on implicit information not stated in the input data. Therefore, popular perturbation-based
or structure-leveraging methods cannot be directly applied for meaningful explanations.
Instead, commonsense explanations require specialized explanatory methods that employ
implicit information in their explanations by design. How can we design and build such
methods?
This chapter describes four potential approaches for building explainable commonsense
models, aligned to the taxonomy in Fig. 2.1:
1. Structure-leveraging commonsense explanations can be found among graph neural net-
work methods [
195, 400], where a graph that contains both explicitly stated and implicit
information is used to connect the task concepts. We will describe PathGenerator:a
method that learns how to generate knowledge paths, and then uses the most salient paths
for a task input to explain its output [
374].
2. Architectural modiﬁcations can be leveraged to produce explanations by encoding com-
positional skills in the neural network. As an example of such an approach, we will
describe CGLI: an architecture for tiered procedural reasoning over short stories, which
leverages state tracking and conﬂict detection to explain the story plausibility [
217].
3. Example-based explanation methods, such as case-based reasoning and prototype-based
networks, can be employed for commonsense explanations. Here, we will describe how
case-based reasoning (CBR) methods, enhanced with augmentations of implicit infor-
mation [
328], and an off-the-shelf prototype network ProtoTeX [68], can be used for
commonsense reasoning over logical fallacies [ 330].
4. As a last idea, we will describe two ways of using language models for commonsense
explanations: a dual-model architecture, PINTO [
372], wherea larger model is used to

18 2 Explainable Commonsense AI
generate rationales for each answer in a multiple-choice QA task; and chain-of-thought
(CoT) [381] reasoning, as an in-context modeling approach to generate explanations
using prompting of frozen LLMs.
2.2 Structure Leveraging Explanations: Path Generation
Commonsense KGs, such as ConceptNet [ 203], A TOMIC [303], and CSKG [ 152] contain
a lot of information that is assumed to be widely accepted as a fact or a belief. Knowl-
edge graphs provide easy access in the form of retrieving individual triples [ 233], multi-
hop paths [ 26, 195], or subgraphs [ 170]. As highly curated sources of information in a
machine-readable format, they can be used to enhance the explainability of neural models,
including LLMs. However, integrating knowledge graphs to enhance the explainability of
neural networks faces three key challenges. First, neural networks manipulate continuous
data, whereas knowledge graphs represent discrete information. This is a manifestation of
the classic challenge of combining symbolic and subsymbolic reasoning. Second, knowl-
edge graphs are inherently sparse and incomplete [ 193], preventing them from generalizing
directly over missing information. Third, the statements in knowledge graphs, at least as of
today, typically lack contextual information [ 86], which makes it difﬁcult to ground their
knowledge precisely for a new situation.
The path generator (PG) method [ 374] is designed to address these three challenges. PG
encodes the question-answer candidate context and the knowledge paths between them sepa-
rately in the subsymbolic space, and performs a ﬁnal reasoning step to produce a plausibility
score for an answer candidate (Fig. 2.2). To address the sparsity and lack of contextualization
of knowledge graphs, PG learns how to connect concepts in the question to concepts in the
answer with a dynamic, and potentially novel, multi-hop relational path, which serves as a
commonsense explanation that supports or refutes the answer.
Fig. 2.2 The KG-augmented QA framework using a path generator [ 374]. The reasoning module
leverages both the unstructured context and structured knowledge to answer a question

2.2 Structure Leveraging Explanations: Path Generation 19
Fig. 2.3 Path generator module, designed as a generative language model trained on a sampled set
of random walk instances from a curated knowledge graph [ 374]
The neural path generator is an active model that generalizes over the original paths found
in the ConceptNet KG, using the contextual associations encoded in generative language
models. Its training is based on two sequential steps: (1) sampling of a set of random walk
instances from a static commonsense KG based on rules and constraints for informativeness
(based on ﬁltering of relation types) and relevance (based on distinctness of paths); (2)
ﬁne-tuning of a pre-trained generative language model [ 288] on these sampled paths. The
sampling of the paths can be local, i.e., starting from the entities found in the question and
answer choices, or global, where the paths are sampled once from each entity. The overall
process is depicted in Fig. 2.3. As PG learns how to connect two concepts with a path, it
resembles link and relation prediction methods. PG differs from these prediction methods
in at least two important aspects: (a) the nodes in the path do not need to be nodes in the
graph as they are textual, and (b) the path that is being generated consists of multiple hops.
Table 2.1 shows example paths generated by the Global path generator (which was found
to perform better than the Local variant) variant to connect the question entities to the gold
answer entities. In Q1, the Global generator provided knowledge about the location of an
entity with a 2-hop path, which helped with answering such “Where” questions. In Q2,
the Global generator was able to connect complex ideas about harmony and making peace
with a 2-hop path. In Q3, the path from the Global generator was able to predict the relevant
property of an entity and realized that a 1-hop relation sufﬁces in this case. These cases show
the path generalization ability of the ﬁne-tuned pre-trained generative language model (GPT-
2), owed to its unstructured knowledge and the adaptation over a high-quality knowledge
resource. Question Q4 shows an example where the global path generator yields a seemingly
relevant path between a key concept in the question and the answer candidate. However, the
path is of questionable quality—indicating that forests are located in warm places. Q4 shows
a downside of using generative models for path modeling: they may invent connections that
are nonsensical or even contradictory.
An automatic evaluation of the global-path model showed that over three-quarters of the
paths contained at least one novel triple and over half of the triples in a path were not found in
the source graph ConceptNet. To further assess the quality of the generated paths, a human
evaluation was conducted by asking two questions: (1) validity (How valid are the paths?)

20 2 Explainable Commonsense AI
Table 2.1 Paths from question to gold answer entities, with novel and valid triplets in boldface. The
number of hops (1 or 2) is shown in brackets. Figure copied from the original work [ 374]
Q1: Where would you ﬁnd magazines along side many other printed works?
A: doctor. . B∗ : bookstore . C: market. D: train station. E: mortuary.
PG-Global (2): {magazine, IsA, book, AtLocation, bookstore}
Q2: If you want harmony, what is something you should try to do with the world?
A: take time. B: make noise. C: make war. . D∗ : make peace . E: make haste.
PG-Global (2): { harmony, _MotivatedByGoal, make better world , HasPrerequisite, make
peace}
Q3: Janet was watching the ﬁlm because she liked what?
A: rejection. B: laughter. .C∗ : being entertained . D: fear. E: bordem.
PG-Global (1): { ﬁlm, _CausesDesire, being entertained }
Q4: Bob the lizard lives in a warm place with lots of water. Where does he probably live?
A: rock. . B∗: tropical rainforest. C: jazz club. D: new mexico. E: rocky places.
PG-Global (2): { warm place, _AtLocation, forest , _IsA, tropical rainforest}
(2) relevance (How relevant are the paths to the question?). For a randomly sampled set of
50 paths from the Global generator for different question-choice entity pairs in the test data,
three annotators were asked to score each path from 1 (Not at all) to 5 (V ery), resulting in a
total of 150 scores for each dimension/generator/dataset. For each path, the annotators had
access to the corresponding question and answer choices for context. The paths were overall
judged with high scores averaging 87% for validity and 88% for relevance, showing the
promise of ﬁne-tuning a pre-trained language model as a path generator for commonsense
QA tasks.
2.3 Architecture Modification: Compositional Architectures
Another way to make neural networks explainable is to modify their architecture in a way
that enforces compositionality. According to Y oshua Bengio [
28], a representation learning
should “learn to identify and disentangle the underlying explanatory factors hidden in the
observed milieu of low-level sensory data”. Thus, compositionality, or disentanglement, is a
key requirement of representation learning methods embedded in neural networks. However,
neural networks are not inherently compositional, at least not in the way that humans would
expect. It is then difﬁcult to explain their decisions and predictions, which is especially a
drawback for complex tasks.
Such a complex task in natural language is the procedural understanding of stories.
Understanding stories requires procedural models that can reason consistently about event
implications, and causal links between events. For instance, understanding why story B is

2.3 Architecture Modification: Compositional Architectures 21
Fig. 2.4 An example story of understanding task. Given two stories, the task is to judge which story
is more plausible, ﬁnd the conﬂicting sentence pair in the implausible story, and predict entity states
at every step
plausible and why story A is not (Fig. 2.4) requires procedural understanding of the causes
of John leaving his notebook at home, as opposed to him taking out his notebook from his
bag: writing in a notebook is counterfactual in the former case, and intuitive in the latter.
For a model to decide whether a story is plausible, it has to track the entity states over time,
understand the effects of the described actions (green arrows), and consider the preconditions
for a given action (pink arrows). Meanwhile, the model must reconcile the causes and effects
of all events described in the story, to provide a globally consistent interpretation.
While story understanding has been generally treated as a separate task from ﬁne-grained
procedural understanding of narratives, a recent benchmark called TRIP [ 334] has combined
the two into a single multi-task setup. In this benchmark the model needs to accurately track
20 different precondition and effect states for every participant, detect conﬂicts between
sentences, and score the story’s plausibility. This task is framed as a “tiered” task, given that
these three goals are expected to build on top of each other’s output: participant states lead
to conﬂicts, and potential conﬂicts (or contradictions) lead to a story being implausible. This
dependency chain can be seen from top-down as an explanation: a story being implausible
can be explained through its conﬂicts, and the conﬂicts can be traced back to participant
states (Fig.
2.5).
The Coalescing Global and Local Information (CGLI) [ 217] method is designed to per-
form procedural reasoning and leverage this reasoning to reason over entire stories, in a
compositional manner. The procedural understanding component produces global outputs
of narrative procedures based on a uniﬁed view of the input, combining both local (entity-
centric, timestep-speciﬁc) and global (document-wide) views—thus optimizing precision
and recall, simultaneously. Then, the story understanding component leverages the outputs

22 2 Explainable Commonsense AI
Fig. 2.5 An illustration of integrating CGLI into a story understanding framework [ 217]. The story
encoding produces a sequence of step representations, i.e., a batch of [CLS] vectors. These vectors
serve as input to different output layers to model the three task objectives: plausibility (orange),
conﬂict sentence detection (blue), and entity state prediction (yellow)
of the procedural backbone to enable story understanding with an explicit and explainable
understanding of event procedures, captured through entity precondition and effect states.
The story framework produces three kinds of outputs based on the same procedural rep-
resentation: (1) a set of preconditions and effect states for each of the attributes for each
participant, using an in-batch CRF module for each attribute; (2) conﬂict prediction for each
sentence pair, by concatenating their sentence representations, and passing the concatena-
tion through a linear layer to ﬁnd the conﬂicting pair; and (3) a story classiﬁer that produces
a global judgment on whether a story is plausible or not, by taking the mean of the sentence
representations as a story representation, and passing it through a linear layer for binary
classiﬁcation. During training, the three objectives are optimized simultaneously:
.L = L plau + Lcon f l + 1
B
b=0
B
Lb
att .
TRIP leverages its tiered setup to associate the accuracy model prediction with two addi-
tional explainability dimensions: consistency of ﬁnding the conﬂicting sentence pairs when
the story classiﬁcation is correct, and veriﬁability, which evaluates the prediction of the
entities’ effects at .sc1 and the entities’ preconditions at .sc2. CGLI also reports the aver-
age F1-score for preconditions and effects across the 20 attributes to better understand the
model’s procedural consistency. As shown in Table
2.2, CGLI’s compositional architecture
enables much higher (400%) consistency and veriﬁability (250%) compared to a language
model baseline. These scores have to do with the architectural differences between the
baseline and CGLI: (1) the baseline model detects conﬂicting sentence pairs via binary clas-
siﬁcation for every sentence, independently, without considering pairs of sentences, leading
to predicting either less or more than two sentences as conﬂicting; (2) the baseline uses the
same encoded representations to directly model both story classiﬁcation and conﬂicting pair
detection objectives, whereas CGLI leverages task-speciﬁc output projection layers; and (3)

2.3 Architecture Modification: Compositional Architectures 23
Table 2.2 Results on the TRIP dataset, from the CGLI paper [ 217]. The F1 scores of the last two
columns are Macro averages of 20 attributes
Model Accuracy Consistency V eriﬁability Precondition
F1
Effect F1
TRIP-RoBERTa [334] 73.2 19.1 9.1 51.3 49.3
CGLI [ 217] 93.4(.±1.5) 76.3(.±1.7) 24.8(.±1.6) 70.8(.±1.8) 74.9(.±1.7)
the baseline encodes each sentence independently, whereas CGLI provides a global input
view to the model.
The connection between the ﬁne- and the coarse-grained model predictions enables
for studying why the model provided certain story judgments, by tracing its decisions to
sentence- and participant state-level. However, the CGLI model still does not guarantee
that the low-level decisions cause high-level ones—instead, it merely leverages a shared
encoded representation of the procedural information for these predictions. As a result, it is
not rare that the model produces accurate story plausibility and conﬂict sentence predictions
while failing to predict entity states. The example in Table
2.3 reveals that the model still
lacks commonsense reasoning skills, e.g., forgetting something at home does not result in
changing its location, and people usually iron their clothes after they are dry. Some entity
states might be hard to distinguish, e.g., the distinction between picking up something versus
taking something out of a container only depends on the previous location of the object,
Table 2.3 Error examples of CGLI [ 217]o nT R I P[ 334]. The conﬂicting pairs are marked with *,
and the entity of interest with italic
Ann washed her hair in the bathtub
Ann used the hair dryer to get ready to go out
Ann applied deodorant to her armpits
*Ann put her pants on
- (Effects, is wet), Pred: False, Gold: Irrelevant
*Ann ironed her pants before going out
- (Preconditions, is wet), Pred: True, Gold: Irrelevant
*John forgot his notebook at home
- (Effects, location), Pred: Moved, Gold: Irrelevant
John sat at his desk
John opened up his book bag
* John took out his notebook
- (Preconditions, location), - Pred: Picked up, Gold: Taken out of container
John began writing down notes

24 2 Explainable Commonsense AI
which might be hard for models to learn from data. Therefore, enhancing the model’s com-
monsense reasoning ability and establishing a stronger causal link between the model’s tiers
are promising future directions to improve the explainability of models like CGLI.
2.4 Example-Based: Case-Based Reasoning
Case-based reasoning (CBR) [ 307] is a family of methods that reasons over new cases based
on similar past cases with a known label [ 1]. Case-based reasoning has found its application in
sensitive domains such as medicine [ 267, 270] and mechanical engineering [ 21, 286] because
of its explainability by example. Two variants of CBR are commonly in use: instance-based
reasoning and prototype-based reasoning. There are both claims about the superiority of
prototypical examples over nearest instances [
163], as well as their counterparts [ 227]w h o
state that a context theory of classiﬁcation, which derives concepts purely from exemplars
works better than a class of theories that included prototype theory.
As one formalization of CBR, instance-based reasoning (IBR) [66] is the process of
solving new problems based on the solutions of similar past problems [ 1]. IBR is inspired
by the way humans think and approach new problems to save time and effort, reusing
prior experiences instead of starting from scratch [
287]. IBR starts with a set of training
examples, often called cases, and learns how to generalize from these examples to new
target cases by identifying commonalities between them. A common realization of IBR
consists of four stages [
1]: (1) Retrieve: Given a target problem, retrieve cases relevant to
solving it from memory, (2) Reuse: Map the solution from the previous case to the target
problem, (3) Revise: Having mapped the previous solution to the target situation, test the
new solution in the real world, and (4) Retain: After the solution has been successfully
adapted to the target problem, store the resulting experience in memory. While the idea of
IBR has been attractive, its application to tasks with natural inputs has often proven to be a
challenge. With the recent introduction of language models, there have been new methods
that consider IBR with language models for tasks like question answering [
70] and logical
fallacy identiﬁcation [ 328, 330]. Such an approach is attractive, as it combines the native
simplicity and interpretability of CBR with the generalizability of LMs.
As an illustration of IBR, we consider the logical fallacy identiﬁcation method by Sourati
et al. [ 328] that consists of three steps: (1) given a new argument, retrieve similar arguments
from a case database (annotated with their fallacy), (2) adapt the retrieved similar arguments
based on the current one, and (3) classify the fallacy of the new argument based on the adapted
exemplars. Here, the last step corresponds to the two steps in the original IBR formulation
by [
1]: classify the new case based on the previous examples, and retain the new problem
alongside its adapted solution and resulting experience in memory for later use in a more
explicit way. This method (summarized in Fig.
2.6) adapts the IBR idea, while using LMs to
both retrieve similar arguments, given its ability to compute similarity for any pair of texts,
and to adapt these arguments to the current one, given its inherent attention mechanism.

2.4 Example-Based: Case-Based Reasoning 25
Fig. 2.6 Three stages of the IBR pipeline in [ 328]. Using the new Case .C, retriever ﬁnds .k similar
examples.{S1, S2, ...,Sk }, and creates .S = C ⊕ < SEP > S1 ⊕ S2 ⊕ ... ⊕ Sk . The adapter encodes
these two inputs and tries to adapt .S based on the new case .C. Finally, the classiﬁer uses the rectiﬁed
information from the adapter to classify the new case by outputting the probabilities corresponding
to belonging to each class of fallacies (in the example shown above, .k = 1)
In fact, LMs can play a third role: LLMs can be prompted to enrich the input argument
with information that helps the model generalize better, such as a counterargument or an
argument goal [
328].
Speciﬁcally, the retriever obtains similar arguments .Si to the new argument .C from a case
database. It uses language model encoders to get the feature vectors for each new case as well
as all the previous cases in the retriever database and then applies these features to compute
their cosine similarity. The choice of the encoder model and the similarity function is critical:
e.g., Sourati et al. [
328] found that using a Transformer model optimized for capturing overall
sentence similarity using a contrastive loss, called SimCSE [ 103], performs optimally for
logical fallacies. The top .k most similar examples are retrieved and passed on to the adapter
together with the new argument ( .S = C ⊕ < SEP > S1 ⊕ S2 ⊕ ... ⊕ Sk ). The adapter’s
role is to consider the retrieved arguments together with the new argument and prioritize

26 2 Explainable Commonsense AI
the most relevant prior arguments. To do so, the adapter ﬁrst encodes the inputs (without
using a head layer), and uses a multi-headed attention mechanism that fetches the new case
embedding . EC as the query and the combined embeddings . ES as both keys and values.
The output of the adapter attention . A has the same shape as . EC and . ES and is fed to the
IBR classiﬁer. The classiﬁer in this method is a two-layer perceptron network that computes
probabilities for each class
.c.
Naturally, the retrieved similar examples by the IBR model can be seen as explanations
for the model’s decision. However, unless restricted in such a manner, these examples by
default can belong to different classes, which may be very useful for data scientists but less
intuitive as explanations for end users.
Prototype-Based Networks (PBNs) are another instance of case-based reasoning. PBNs
are based on the theory of categorization in cognitive science [ 297], governed by the graded
degree of possessing a prototypical feature of that category, with some members being more
central (prototypical) than others. Considering, for example, different types of birds: pelican
classiﬁcation can be done through their prototypical tall necks and similarity to a prototypi-
cal pelican [
257]. Computationally, this idea is implemented by ﬁnding prototypical points
in the shared embedding space of data points and using the distance between prototypes and
data points to accomplish the classiﬁcation task. This classiﬁcation approach is claimed to be
both interpretable and robust to noise because it classiﬁes through distances to prototypical
examples found in the data. Simple associations between data points and central prototypical
examples bring interpretability while leveraging distance between points helps to quantify
prototypicality, which then facilitates identifying noisy or out-of-distribution samples [
394].
Given these properties, PBNs have been popular in Computer Vision tasks, including image
classiﬁcation [
12] and novel class detection [ 135]. Recently, there have also been meth-
ods that apply PBNs to text classiﬁcation tasks: sentiment classiﬁcation [ 145, 240, 280],
few-shot relation extraction [ 132, 231], logical fallacy identiﬁcation [ 330], and propaganda
detection [ 69].
To illustrate the workings of a PBN, we leverage the framework for text classiﬁcation
[327] illustrated in Fig. 2.7. PBNs classify data points based on their similarity to a set of
prototypes learned during training. These prototypes summarize the prominent semantic
patterns of the dataset through two mechanisms: (1) prototypes are deﬁned in the same
embedding space as input examples, which makes them interpretable by leveraging input
examples close to them; and (2) prototypes are designed to cluster semantically similar
training examples, which makes them representative of the prominent patterns embedded
in the data and input examples. The PBN’s decisions are inherently interpretable because
prototypes are trained to be aligned with previous observations [
144]. This enables insights
into the behavior of the model during inference by looking at the closest activated prototypes
[
69]. Prototypes being in the same embedding space as input examples allows them to be
represented as either the training examples [ 69] or parts of training examples, such as key
phrases [ 280] or key sequences [ 145, 240] extracted from training examples. These proto-
types can be associated with semantic patterns of particular classes from their initialization

2.4 Example-Based: Case-Based Reasoning 27
Fig. 2.7 Classiﬁcation by a PBN. The model computes distances between the new point and proto-
types,.d(e j , Pk ), and distances within prototypes, .d(Pk , Pl ), for both inference and training. During
training, the model minimizes the loss term, .L, based on the distances between the new point and
prototypes as well as within prototypes; during inference, distances between the new point and pro-
totypes are used for classiﬁcation by a fully connected layer. We test variations of the loss terms
(.L), different encoder backbones ( .E), and distance functions ( .d) and assess their effect on the PBN’s
robustness
or be trained freely and subsequently associated with the prominent semantic patterns of the
whole dataset.
At training time, the model objectives simultaneously tweak the backbone parameters and
the prototypes to ﬁnd meaningful prototypes and reach high performance. To compute a total
loss term
.L, PBNs use the computed distances within prototypes .d(Pk , Pl )k=l , distances
between all . Q prototypes and . N training examples given by .d(e j , Pk )j∈{1,...,N};k∈{1,...,Q},
and the computed probabilities . ˆyc. The prototypes and the weights in the backbone are
adjusted according to.L. The total loss .L consists of different inner loss terms that ensure high
accuracy, high interpretability, and low redundancy among prototypes; i. e., the classiﬁcation
loss.Lce, the clustering loss .Lc [192], the interpretability loss .Li [192], and separation loss
.Ls [144]:
.L = Lce + λcLc + λi Li − λs Ls
where.λc,λi ,λ s ≥ 0 are regularization factors to adjust the contribution of the auxiliary loss
terms. At inference time, classiﬁcation in PBNs is done via a fully connected layer applied on
the measured distances between embedded data points and prototypes. As shown in Fig. 2.7,
given a set of data points .x j , j ∈{ 1,..., N } with labels .y j ∈{ 1,..., C},a n d. Q prototypes,
PBNs ﬁrst encode examples with a backbone . E, resulting in the embedding .e j = E(x j ).
Next, PBNs compute the distances between prototypes and .e j using the function .d.T h e s e
distances can be fed into a linear layer to compute class-wise logits by incorporating the
similarities to each prototype. Applying a softmax on top of logits, the ﬁnal outputs are
. ˆyc(x j ): a probability that .x j belongs to class .c ∈{ 1,..., C}.

28 2 Explainable Commonsense AI
Table 2.4 Input arguments with their fetched similar cases using IBR and PBNs [ 330]. We mark the
exemplars from the same class as the input in bold
Class Input Sentence Similar Cases (IBR) Prototypical Cases
(PBN)
Ad Populum Everyone is going to
get the new smart
phone when it comes
out this weekend. Why
aren’t you?
(1) I’m gonna get an
iPhone because
everybody else has an
iPhone and they’re
cool
(1) Everyone seems to
support the changes
in the vacation policy,
and if everyone likes
them, they must be
good
(2) Everyone wants
t h ei P h o n e1 1b e c a u s e
it’s the best phone on
the market!
(2) Everyone is
buying the new
iPhone that’s coming
out this weekend. You
have to buy it too
Faulty Generalization If you forget to ﬂoss,
you will get cavities,
and if you get cavities,
you will lose all your
teeth by the time
you’re 30
(1) If you don’t eat
breakfast, you’ll
slouch in your desk. If
y o us l o u c hi ny o u r
desk, you’ll hurt your
back. If you hurt your
back, you’ll never
become President
(1) If we allow gay
people to get married,
then the next thing
you know people will
be wanting to marry
their pets!
(2) four out of ﬁve
dentists agree that
brushing your teeth
makes your life
meaningful
(2) You smoke pot? If
you keep doing that,
you’ll be a heroin
addict within two
years
Qualitative analysis Table 2.4 shows the retrieved instances by IBR and prototypical
examples by the PBN for two fallacious arguments on which these methods enabled the
underlying model to change its decision to the correct class [
330]. For PBNs, the table
shows the two nearest training examples to the nearest prototype for a given input. 3 out
of 4 examples for IBR and all 4 examples for PBNs come from the same class, which
indicates that the modiﬁed decision in these cases correlates with obtaining helpful (or even
representative) examples from the same class. However, this is not always the case—the
retrieved examples for IBR and PBNs can also be from different classes [
330]. Moreover,
the authors identify two scenarios for the corrected prediction through CBR methods. First,
and more common, is the case when the retrieved examples reﬂect surface similarity, which
curiously still helps the model to change its decision, as illustrated by the ﬁrst row of IBR
in Table
2.4. The second situation, observed forthe second argument of IBR and most PBN

2.5 Language Modeling Explanations 29
examples, is when the model captures the structural similarity and more abstract semantics.
As informal fallacies require a mixture of both surface and structural modeling, the observed
differences between IBR and PBN are an important consideration for future explainable
system designs.
2.5 Language Modeling Explanations
The previous sections describe methods that address the black-box nature of neural (lan-
guage) models by leveraging knowledge graph paths, enforcing compositional reasoning,
or using LMs within example-based reasoning methods. A natural question arises: can the
language models themselves provide commonsense explanations, elicited through pipeline
design or prompt engineering? Namely, while there has been evidence that knowledge can
be extracted to some extent from the language model parameters, it is unclear whether this
knowledge is being modeled and used consistently and intuitively [
82, 201]. This question
has inspired a line of work aiming to make LMs’ reasoning processes more explicit by gen-
erating free-text rationales, which use LMs’ internal knowledge to describe their reasoning
process in natural language [
222, 256, 381, 401].
Several different directions have emerged, which typically differ in the order of gen-
erating the rationale and the model output, as well as in the choice of language models
for rationalization and answering. In its ﬁne-tuned self-rationalizing variant, a single LM
is ﬁne-tuned to jointly generate the task output and rationale [
222, 256, 401]. However,
ﬁne-tuned self-rationalizing LMs often perform worse than non-rationalizing LMs, since
their parameters are learned using two relatively dissimilar objectives, while also requiring
expensive rationale annotations [
256, 386]. In the prompted self-rationalizing paradigm, a
single LM is instead frozen and prompted to jointly generate the task output and rationale,
with the prompt consisting of a few input-output-rationale demonstrations [
381]. Prompted
self-rationalizing LMs yield strong task performance and only need a few rationale demon-
strations for the prompt, but are computationally prohibitive since they generally require very
large-scale (i.e., over 100B parameters) LMs to work effectively [
380, 381] and they cannot
be adapted or controlled by end users. In the pipeline-rationalizing paradigm, a ﬁne-tuned
rationalizing LM ﬁrst generates the rationale, which is then used as input for a separate ﬁne-
tuned reasoning LM to generate the output [
182, 291]. Besides requiring expensive rationale
annotations, pipeline-rationalizing LMs’ generated rationale forms a non-differentiable bot-
tleneck between the two modules, which complicates end-to-end training and can hurt task
performance [
136, 386]. An extra challenge with all these rationalizing methods is their
lack of mechanisms to regularize the rationale generation to faithfully reﬂect the reasoning
process of the LM, without hurting task performance [ 372].
One way to enhance the model faithfulness is proposed by PINTO [ 372], an LM pipeline
that rationalizes via prompt-based learning, then reasons over the task input and rationale via
counterfactual regularization. PINTO’s rationalizing module is a medium-scale (i.e., 20B

30 2 Explainable Commonsense AI
Fig. 2.8 Rationale-based language reasoning [ 372]. Left: examples of reasoning tasks that require
implicit knowledge beyond task inputs. Right: comparison of existing paradigms for providing free-
text rationales along with predictions
parameters) LM that contains vast latent knowledge obtained via pretraining [ 32]. Though
challenging to ﬁne-tune, it is affordable for prompt-based learning. Given the task input and
a minimal input-output-rationale demonstration prompt, the rationalizing module uses its
internal knowledge to map out a suitable reasoning process for the task input by generating a
free-text rationale. The rationalizing module is frozen during ﬁne-tuning, which drastically
reduces training costs and prevents it from exploiting spurious shortcuts in the downstream
training data. PINTO’s reasoning module is a small-scale (i.e., under 1B parameters) LM
to which knowledge is transferred from the rationalizing module. The reasoning module
is ﬁne-tuned to solve the downstream reasoning task by using the generated rationale as
context for the task input (Fig. 2.8).
Crucially, to help ensure that the reasoning module’s behavior is dictated by the rationale
(instead of by spurious shortcuts), the reasoning module in PINTO is regularized to output
less conﬁdent predictions when the rationale is noisily perturbed. To simulate shortcut rea-
soning, PINTO considers two rationale perturbation strategies: token masking (where the
rationale is ignored) and token replacement (where the rationale is misused). The approach
in PINTO does not only improve model robustness, but it also leads to explanations of higher
quality, largely scoring on par with human rationales (Table 2.5).
An alternative paradigm to explanations by language models has been introduced by
Google’sChain-of-Thought (CoT) method [381]. CoT was proposed to address cases where
the mapping between the input .x and the output .y is not trivial, such as mathematical chal-
lenges and commonsense reasoning. CoT is inspired by the “dual process” theory about
human thinking, consisting of a fast, automatic, unconscious mode and a slow, deliberate,
conscious mode [ 167, 168, 398]. In CoT, .x and .y are connected via a chain of thoughts

2.5 Language Modeling Explanations 31
Table 2.5 Human evaluation of PINTO [ 372] comparing the human-annotated and machine-
generated rationales for the CommonSenseQA benchmark
Rationale
source
Factuality Grammaticality New info Supports
answer
Completeness
Human 0.94 0.98 0.71 0.90 0.82
Generated 0.91 0.99 0.69 0.87 0.65
.zi , each of which is a coherent language sentence that is meant to provide an intermediate
step towards problem-solving (e.g., an intermediate equation or a commonsense knowledge
statement). Each thought is sampled sequentially, after which the output .y is sampled as
a follow-up, namely, .y ∼ pθ (z1,..n,y|x ). CoT quickly grew in popularity due to two main
reasons: (1) CoT provided compelling evidence for improvement across tasks of math,
commonsense reasoning, and symbolic reasoning, and (2) CoT provided an intuitive mech-
anism for eliciting the model’s reasoning chains, thus enabling comprehension of its internal
thoughts.
However, language models are not perfect reasoners (after all, their specialty is word pre-
diction). Their thought chains may be incomplete, contradictory, irrelevant, or misaligned
with the model output [
378]. This has inspired follow-up ideas towards enhancing the faith-
fulness and robustness of the CoT method. One such idea is self-consistency: a self-ensemble
method that improves upon the greedy decoding in CoT, under the assumption that the answer
can be approximated by majority voting over multiple chain-output pairs. Self-consistency
ﬁrst samples
.k chains of thought, .[z(i)
1,..n, y(i)]∼ pθ (z1,..n,y|x ), and returns the most frequent
output:.argmax y ={ i|y(i) = y}.
To address the lack of local exploration of different thought steps, Tree-of-Thoughts
(ToT) [ 398] proposes to explore multiple reasoning paths over thoughts. ToT thus frames
a reasoning problem as a search over a tree, where each node is a state .s =[ x, z1,..i ] rep-
resenting a partial solution with the input and the sequence of thoughts so far. Rather than
a single solution, ToT is designed as a framework consisting of four steps, each offering
various choices for its instantiation: (1) process decomposition into thought steps, (2) gen-
eration of potential steps for a state, (3) heuristic evaluation of states, and (4) selection of
a search algorithm. ToT analytically is claimed to improve the interpretability of model
decisions and enable better human alignment, as the resulting representations are readable,
high-level language reasoning instead of implicit, low-level token values. Graph of Thoughts
(GoT) [
187] goes beyond ToT to provide arbitrary graph-based transformations of thoughts,
such as aggregating thoughts into a new one or looping over a thought to reﬁne it.
While CoT and its follow-up works (summarized in Fig. 2.9) are arguably providing
explainability in the form of following the model reasoning and enhancing the faithfulness
between the answer and the rationale, there is a lack of studies so far that evaluate the

32 2 Explainable Commonsense AI
Fig. 2.9 A visual summary of Chain of Thought, Chain of Thought with self-consistency, Tree of
Thoughts, and Graph of Thoughts, courtesy of [ 29]
soundness, relevance, and faithfulness of their thought chains. It remains unclear how their
explanatory power compares to the methods in the previous sections.
2.6 Summary and Discussion
We conclude the chapter with a summary of the state-of-the-art explainable commonsense
AI and a discussion of its limitations and open challenges. This chapter provided an overview
of different explainable commonsense reasoning methods. We started with an explainable
AI taxonomy, which categorizes XAI methods in terms of their functioning, scope, input and
output format, result, and applicability. Considering functioning as arguably the most impor-
tant dimension in this taxonomy, the chapter considered what the XAI explainability types
mean in the context of commonsense reasoning. Given the implicit nature of commonsense
reasoning, we focused on method families that can provide an explanation that is not found
in the input. Speciﬁcally, we considered four families: a structure leveraging model based on
knowledge graph path generation, architecture modiﬁcation models that incorporate com-
positional reasoning in the neural network, example-based models based on instance- and
prototype-based reasoning, and language modeling models of types input-output-rationale
and input-rationale-output.
The chapter provides four high-level insights. First, commonsense explanations are, by
design, unique in that they require making explicit reasoning chains that are not provided
in the data, but are instead implied. They stand, thus, opposite from explanations of what
parts of the input trigger a certain prediction, such as the human attention maps [ 310]. In
this case, discovering and generating paths in commonsense knowledge graphs is effective,
given that the knowledge paths are meant to make explicit those reasoning chains. Another

2.6 Summary and Discussion 33
effective strategy is modeling stories in terms of their participant states and conﬂicts, which
leverages low-level textual information and learns how to connect it using implicit causal
links. Learning how to leverage prior experiences via case-based reasoning is beneﬁcial,
especially when the experiences are enriched by implicit information like goals. Finally,
LLMs are also an effective way to explain decisions, albeit their rationale may not be
faithful to their generated answer.
Second, we note that the explanation outputs are diverse across the four method fami-
lies. The ﬁrst method, representing structure leveraging models, produces knowledge graph
paths that exist in the graph, or their generalized version based on a generative language
model. The architecture modiﬁcation model, CGLI, yields compositional explanations by
performing a multi-task prediction of attributes, conﬂicts, and plausibility. Example-based
reasoning models explain a prediction through a set of similar prior cases, being prototypi-
cal instances or merely nearest neighbors. Generative language models explain predictions
using free-text rationales, generated either before producing the answer (as in chain-of-
thought reasoning) or afterward (as in input-output-rationale models). Follow-up works on
LLM-based explanations has extended these ideas to structural explanations in the form of
a tree or a graph.
Third, as evaluating commonsense explanations is becoming more prominent, there is a
wide range of evaluation metrics, factors, and procedures that are being considered. This
is partially justiﬁed by the different focus across the explainable methods, however, it is
also an indication of the current state of the research in this ﬁeld, which is largely in ﬂux.
Interestingly, this ﬁnding is in line with explainability evaluations in machine learning, where
there is also a lack of agreed census and the evaluation can vary a lot depending on the type
of explanations provided [
411]. According to this work, explainability metrics evaluate
two general dimensions: interpretability (to a human) and ﬁdelity (an accurate description
of model behavior). Here, the former is important for managing social interaction, and
the latter to verify other model desiderata. Interpretability metrics include clarity (being
unambiguous), broadness (being generally applicable), and parsimony (being presented in
a simple and compact form). Fidelity metrics include completeness (describing the entire
dynamic of the model) and soundness (being correct and truthful).
Fourth, we note that among the reviewed methods, the dominant evaluation protocol is
to ﬁrst ask the machine to generate explanations, and then solicit human judgments for the
quality of the generated explanations . Here, humans are typically experts (e.g., colleagues of
the authors) or crowd workers. Some common metrics evaluated by humans are grammati-
cality (is the explanation syntactically correct and ﬂuent), faithfulness (does the explanation
answer why a certain answer was given), generalizability (is the explanation applicable to
other answers), and a long list of other metrics such as informativeness, relevance, sufﬁ-
ciency, and plausibility [
301]. Alternative evaluation regimes also exist. One idea, exhibited
by the Visual Commonsense Reasoning task [ 402], is to evaluate explanations in a discrim-
inative rather than generative fashion . Here, explainability is framed as a multiple-choice
task, where after choosing an answer the system needs to select the right explanation from a

34 2 Explainable Commonsense AI
list of contextually relevant explanations. Another idea is evaluating explanations via simu-
latability, where users are asked to predict what a model would produce given some input.
A good explanation in this case has a high user accuracy of using the input with explanation
relative to the same accuracy without explanation [
134].
Challenges As commonsense reasoning relies on implicit information, it requires spe-
cialized XAI methods that explain a decision by including this implicit information in their
explanations. Given the discussion presented in this chapter, what are the remaining chal-
lenges for developing and evaluating explainable commonsense reasoners? We discuss three
key directions for further progress toward explainable AI agents with common sense.
First, the quality of the produced explanations remains a concern . Model explanations
are often described as unfaithful or inconsistent with the provided answer that the model
is generating. Considering the strong prominence of generative models, which are a key
component to the explainable architectures we reviewed in this chapter, these models are
always able to produce an explanation; however, the explanation, albeit ﬂuid, legible, and
contextually relevant, may be inconclusive (incomplete), may contradict the answer, or even
contradict itself. This has inspired the emergence of chain-of-thought and follow-up works,
which has decreased this problem, yet, it persists at the time of writing of this book. A
possible direction toward ensuring the quality of the explanation is to include a (possibly
symbolic) veriﬁcation or certiﬁcation step [
282]. While such approaches are promising, their
results to date have been limited. We return to such methods in Chap. 4.
Second, evaluating commonsense explanations requires a consolidation of the wide range
of current practices. As discussed above, this challenge applies to XAI beyond commonsense
reasoning; and yet, the challenge needs to be tackled for commonsense explanations directly.
Arguably, the consolidation needs to start with an analysis and an agreement of metrics, i.e.,
deciding what considerations of quality should be prioritized when assessing an explanation.
Once the metrics have been agreed upon, the next step is to deﬁne the best procedures
to obtain values for those metrics, selecting between the scoring of machine-generated
explanations, simulation experiments with end users, multiple-choice tasks, or possibly,
formal evaluation methods.
Third, there is a sizable discrepancy between the present approaches to explaining com-
monsense behaviors and the practices common in philosophy, psychology, and cognitive
science. Miller [ 238] indicates that much of the judgment of explanation quality at present
is based on the intuition of the researchers. He characterizes explanations with four key
characteristics: (1) contrastive: explanations are sought in response to particular counter-
factual cases, i.e., an explanation should describe why an event happened instead of some
concurrent event; (2) selective: humans select one to two causes from a sometimes inﬁnite
number of causes to be the explanation, generally inﬂuenced by cognitive biases; (3) causal
rather than probabilistic: using statistical generalization for explaining events is unsatisfying
unless accompanied by an underlying causal explanation for the generalization itself; and
(4) social: explanations transfer knowledge as part of a conversation or interaction, and are
thus relative to the explainer’s beliefs about the explainee’s beliefs.

2.6 Summary and Discussion 35
In many sciences, including evolutionary biology, there is a related distinction between
ultimate and proximate explanations [ 252]. Muthukrishna illustrates this distinction with
classic examples of why animals enjoy sex. A proximate explanation would be that sex is
pleasurable and people enjoy pleasurable activities, which is a tautology. A more elaborate
explanation based on neuroscience is that sex releases dopamine, endorphins, and oxytocin,
which are associated with pleasure, love, and trust, reinforcing the behavior in the future.
However, the ultimate explanation would need to also consider the full range of alternatives,
as in contrastive explanations. An example would be to consider the causal implications of
sex versus an alternative activity, like banging heads against a wall. Considering two worlds:
one where animals associate sex with pleasure, and another where animals associate head-
banging with pleasure, we can simulate the causal impacts of these preferences, ultimately
concluding that the former animals would ﬂourish and the latter would perish.
Thus, similar to Miller’s claim in 2018 and the recent discussion by Muthukrishna, it is
safe to say that today’s commonsense explanations are still proximate and misaligned with
the rich research in social science and can beneﬁt from tighter cross-disciplinary collabora-
tions.

3Collaborative Commonsense AI
Abstract
Collaboration is one of the core human principles and abilities for solving difﬁcult prob-
lems and scaling complexity. Under an assumption that the strong sides of AI are different
than those of people, and encouraged by anecdotal success stories like “centaur chess”
and by large models communicating in a natural language like ChatGPT, the question
emerges: (how) can AI work in synergy with humans? What capabilities, interfaces, and
models does AI need to have to be collaborative with people and make a potential impact
through collaboration? While it may be difﬁcult to draw a strong distinction between col-
laborative and non-collaborative mechanisms, several intuitive directions emerge from
the literature. Collaborative AI needs to be able to build an internal model of situations,
including the relevant actors and objects, their attributes, states, relationships, and affor-
dances. It needs to have an internal model of itself, namely, its goals, plans, and history
of prior experiences. It must have Theory-of-Mind, i.e., an evolving representation of the
beliefs, goals, and other mental attributes of other agents in a situation. And it must apply
such collaborative skills within multimodal interactions, involving language, vision, and
planning. We review state-of-the-art methods and ﬁndings for such collaborative mech-
anisms and conclude with a discussion of open challenges and lessons learned.
3.1 Background and Challenges
Throughout history, humans learned the value of collaboration. We team up with other
people who have complementary skills and interests to jointly invest energy into performing
a complex task. Collaboration in such a scenario yields a whole that is more than the sum of
its parts. Collaboration has enabled humans to gradually scale the complexity of tasks that
are considered possible and has naturally led to a specialization of humans by acquiring deep
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_3
37

38 3 Collaborative Commonsense AI
knowledge and skills on narrow topics. The specialization accompanied by task complexity
has expanded over time but also in space, as today such specialization is most apparent in
megacities with large numbers of highly-skilled individuals in narrow topics (perhaps at the
expense of knowledge in every other topic) [
252].
Enter AI. Besides being able to improve effectiveness and alleviate people from perform-
ing certain repetitive skills, AI is now also often considered as a teammate or a collaborator.
While this collaborative perspective has been catalyzed by the emergence of large public AI
interfaces like ChatGPT and Midjourney, its underlying principles pre-date these models.
In a nutshell, the main motivation for establishing AI-human teams or partnerships comes
from the complementary strengths and weaknesses of AI and humans [
4, 317].
Then, (how) can AI work in synergy with humans in practice? The simplest model for
collaboration is that of division of labor: if machines are better at humans at some tasks,
then they can just perform those tasks instead of humans. In this approach, the human-AI
partnership is seen as a task allocation based on skills and available resources. Task allocation
is a workable model for “simple” tasks, which require limited data and can be solved with
common analytical tools, provided that there is a reasonable amount of time and information
certainty. Exemplary such tasks are clear-cut procedures with a clear performance scale,
such as assembly line production. However, allocation discovery is an oversimpliﬁed model
that is suboptimal for more ambiguously structured tasks that are unbounded, involve large
amounts of data, and cannot be solved analytically in polynomial time. Such a complex
task is driving a car through city trafﬁc during a storm, or formulating and executing a
course of action to save lives and properties during a house ﬁre [
232]. As Metcalfe [ 232]
discusses, neither people nor machines can perform such tasks well on their own, calling
for an integrated collaboration model that beneﬁts from the knowledge and abilities of both
the human and the machine simultaneously.
What capabilities, interfaces, and models does AI need to have to be collaborative with
people? While it may be difﬁcult to draw a strong distinction between collaborative and
non-collaborative mechanisms, several intuitive directions emerge from the literature [
4].
AI needs to be able to build an internal model of situations , including the relevant actors
and objects, their attributes, states, relationships, and affordances. Such a model should be
ﬂexible, and its manipulation can provide meaningful simulations of altered states in the
environment and their causal impact. For example, a counterfactual intervention of replacing
the location of a concert from a nightclub to a stadium yields new expectations in terms of
number of people, quality of sound, and the time of the day. The AI also needs to have an
internal model of its own goals, plans, and history of prior experiences . For instance, in a
negotiation, it must have a clear grasp of the resources it possesses, the resources it wants to
obtain, and what are its “red lines”. AI must have Theory-of-Mind (ToM), i.e., an evolving
representation of the beliefs, goals, and other mental attributes of other agents in a situation.
ToM is an assumed ability when collaborating with humans, and it is a skill that enables
the AI to reason about the possible actions of other agents, e.g., in a negotiation scenario, it
may have a model of what the resources of the other agents are and what they would like to

3.2 Representing Situations 39
achieve. Finally, it must understand the interface between different modalities, and how its
collaborative mental models ﬁt within natural multimodal settings .
In this chapter, we review state-of-the-art methods and ﬁndings for such collaborative
mechanisms. We start with existing work on representing situations, highlighted through
a method that “imagines” situations by using scene knowledge graphs. For modeling of
the agent’s internal states, we consider the scenario of text-based games, where agents can
organize their memory, be deliberate about their goals, and work with other agents to obtain
high-level plans to achieve those goals in light of prior experience. We discuss Theory-of-
Mind analysis and emerging methods, which stem from rich cognitive psychology studies
with humans and are being adapted to test and develop AI reasoners. Finally, we consider the
multimodality of interaction, as perceptual and linguistic situational signals are intricately
connected and should be considered jointly with collaborative reasoning mechanisms. We
conclude the chapter with a discussion of open challenges and lessons learned.
3.2 Representing Situations
Representing and reasoning over situations is a commonsense ability that requires an under-
standing of object relations (e.g., the book is on top of the microwave), affordances (e.g.,
microwaves can warm up food), and properties (e.g., the book has a gray cover). While it
remains difﬁcult to organize the set of common situations into a taxonomy [
396], common-
sense AI methods have been developed to simulate this skill computationally.
There are both discriminative and generative AI tasks for evaluating the model’s grasp
of situations. One popular task is generative commonsense reasoning, where the model
is tasked with creating a ﬂuent and sensible text that describes everyday situations while
simultaneously satisfying certain constraints. The task constraints are a set of concepts that
the text should include and an initial narrative context; however, additional constraints come
from implicit commonsense knowledge about what is plausible in the world [
191, 208]. For
example, given concept words { dog, frisbee, catch, throw }, the goal may be to generate a
plausible description like A man throws a frisbee and his dog catches it in the air rather than
an implausible one such as A dog catches a frisbee and throws it to another dog (dog are
not expected to be able to throw frisbees).
With the emergence of generative LLMs, a straightforward method for this task can
be created quickly, simply by prompting or tuning a model to produce sentences for a
given set of concepts. However, while these models perform well on average, they are non-
collaborative, as their response is based on black-box associations without fundamental
insights into the model’s internal representation, nor a consistent mechanism to exchange
information about a situation. Inspired by the general idea of planning before acting, a line of
work has been proposed to enrich such generative LLMs with intermediate representations.
Such representations may be storyline keywords [
397], predicate-argument pairs [ 87], or
prototype sentences [ 191].

40 3 Collaborative Commonsense AI
As a more comprehensive intermediate representation, it is possible to “imagine” a scene
by using a scene knowledge graph (SKG) representation [ 375]. Combining LLMs with SKGs
can address three key challenges with automatic text generation: (1) explicit awareness of
commonsense knowledge about relations between concepts and the affordances of objects
(e.g., a “ dog” can perform the action “ catch” but not the action “ throw”); (2) compositional
generalization ability [ 173] for judging whether a newly constructed concept composition
is plausible; and (3) identiﬁcation of concepts that are implicit in a scene (e.g., “ person”t o
perform “ throw” in the above example).
An overview of this method, called Imagine-and V erbalize, is shown in Fig. 3.1.A st h e
name indicates, the method consists of two steps. Based on a set of input concepts and initial
narrative context, a scene imagination module creates a contextually relevant SKG, which
consolidates scene knowledge for a given situation connected by commonsense expectations.
Then, the second step of verbalization transcribes the SKG into natural language. Both the
imagination and the verbalization steps are implemented by using Transformer models: the
former is trained to generate a graph given the set of concepts and the initial context, and
the latter is optimized to generate text tokens conditioned on the input concepts, context,
and the scene graph. Generating a coherent narrative with multiple sentences can be done
through an iterative application of the imagination and verbalization steps in a sequence.
This work uses the abstract meaning representation (AMR) format to represent the scene
knowledge graphs [ 19]. The AMR graphs are designed to describe “who is doing what to
whom”, for which they include a small set of reusable relations, as shown in Fig. 3.1.F o r
instance, the action “throw” is performed by the agent woman, and it applies to the object
“frisbee”. In Imagine-and-V erbalize, such AMR graphs are generated for each sentence.
To realize Imagine-and-V erbalize, a key component is the availability of training data that
can support the generation and verbalization of such AMR scene graphs. Such data should
Fig. 3.1 Overview of the Imagine-and-V erbalize method [ 375], which (1) uses scene knowledge
graphs for unifying scene knowledge from different resources, (2) adapts a contextualized imagination
module to construct a scene knowledge graph for a set of concepts, based on a collection of scene
graph examples, and (3) realizes the scene knowledge graph into natural language at inference time

3.2 Representing Situations 41
align input concepts, scene graphs, and narratives with each other, and can be extracted
from rich annotations of images with scene graphs and captions [ 181], and textual stories
and captions [ 249]. The AMR graphs are extracted from the visual scene graphs by using
a set of heuristics, whereas they are extracted from the textual data by using a dedicated
AMR parsing tool. Such diversity of modalities and concepts in the training data enables
the model to generalize better than its baselines.
Table 3.1 provides examples of how the imagination into a shared representation helps
the system generate sentences that pertain to common sense and ﬁx errors of the end-to-end
Table 3.1 Qualitative analysis showing how imagination can help ﬁx various errors. The bolded
SKG relations are the key relations that ﬁx the errors. Table adapted from the one in [ 375]
(I) Incorrect Agent {owner, chase, dog, ball, throw}
Text w/o imagination The dog is chasing the ball and throwing it at the owner
Text w/ imagination A dog chases a ball being thrown by its owner
Generated SKG (chase, ARG0, dog), (chase, ARG1, ball), (throw, ARG1,
ball), (throw, ARG0, owner)
(II) Incorrect Action {butter, pot, crack, egg, add}
Text w/o imagination She adds eggs, crackers, and butter to a pot
Text w/ imagination Y ou crack an egg and add butter to a pot
Generated SKG (crack, ARG0, you), (crack, ARG1, egg) , (add, ARG0, you),
(add, ARG1, butter), (add, ARG2, pot)
(III) Incorrect Object {hit, bottle, shoe, open, wall}
Text w/o imagination Someone opens his shoe and hits a bottle on the wall
Text w/ imagination A man opens a bottle and hits his shoe against a wall
Generated SKG (open, ARG0, man), (open, ARG1, bottle) , (hit, ARG0, man),
(hit, ARG1, shoe) , (shoe, poss, man), (hit, ARG2, against),
(against, op1, wall)
(IV) Implicit Concepts {ﬁll, liquid, machine, bottle}
Text w/o imagination A machine holding a bottle ﬁlled with liquid
Text w/ imagination A man holds a bottle ﬁlled with liquid in a machine
Generated SKG (hold, ARG0, man) , (hold, ARG1, bottle), (ﬁll, ARG1, bottle),
(ﬁll, ARG2, liquid), (hold, location, machine)
(V) Event Relations {trick, perform, begin, stunt, dance}
Text w/o imagination A group of people begin performing a stunt while performing
at r i c k
Text w/ imagination A man performs stunts and tricks as he begins to dance
Generated SKG (perform, ARG0, man), (perform, ARG1, stunt), (perform,
ARG1, trick), (perform, time, begin) , (begin, ARG0, man),
(begin, ARG1, dance),
(dance, ARG0, man)

42 3 Collaborative Commonsense AI
baseline method. These examples show ﬁve representative error types that are corrected
by the imagination method, namely incorrect role attribution to (1) agents, (2) actions or
(3) objects, (4) failing to infer the implicit concepts and (5) misunderstanding the relations
between events. These examples show how SKGs can provide an effective mechanism for
correcting commonsense mistakes in LMs.
Besides serving as a vessel to enforce explicit situation modeling with LMs, SKGs also
provide collaborative mechanisms that users can directly inspect and interact with. For
instance, an incorrect prediction can be expected to be ﬁxed by adapting the scene knowledge
graph, if incorrect, which can result in an accurate text generation. Beyond individual case
ﬁxes, such human interventions are expected to also enhance the generalization of the model,
as the same graph patterns can re-occur in the future and help prevent future mistakes.
Ultimately, this can enable a more effective collaboration with people through time, and
facilitate trust.
Y et, we note that such collaborative mechanisms are imperfect. The generated SKGs may
be incomplete or may contain information that does not correspond to the task constraints,
or common sense. In addition, the verbalization may also generate text sequences that
are misaligned with the SKG. Currently, an extensive evaluation of the quality of such
collaborative methods, as well as their impact in human-AI teams, is lacking. Wang et
al. [
375] perform a small user study to evaluate several quality aspects of the generated
scene knowledge graphs, including completeness, common sense, alignment between the
graph and the generated text, and similarity of the generated text to sentences generated by
humans. The high human scores for these four categories are encouraging, inspiring follow-
up work on employing methods like Imagine-and-V erbalize in interactive and collaborative
scenarios. At the same time, the overall impact of imagining and verbalizing these graphs
on the generation task is relatively low, which questions whether the graphs are adequate,
complete, and consistently used in the verbalization.
3.3 Modeling Self: Planning, Memory, and Interaction Goals
While most of the tasks in NLP focus on a short interaction between an agent/model and
the environment, it is becoming increasingly clear that human-centric agents need to be
able to perform in longitudinal settings of prolonged interaction. Correspondingly, a variety
of recent tasks have focused on the interaction between an agent and the environment.
One such task is dialogue modeling and generation, which can be either open-ended or
goal-driven. An example of an open-ended dialogue system is a recommendation assistant,
whereas a goal-driven task is that of negotiation [
47]. Another type of interactive task
is that of interactive ﬁction, where an agent needs to navigate a simulated environment,
modeled after commonly known areas like a household, to fulﬁll a certain predeﬁned goal.
Such environments can be multimodal, such as Embodied QA [
67] and Alfred [ 318], or
text-based, such as ScienceWorld [ 376] and TextWorld [ 59]. Another emerging direction of

3.3 Modeling Self: Planning, Memory, and Interaction Goals 43
interactive tasks is that of web navigation, where agents need to follow language instructions
to complete complex tasks on any website, an exemplar of which is Mind2web [ 78].
What is characteristic of such environments is that the model is generally seen as an
agent that should retain a consistent and reliable behavior over time. The agent’s behavior
translates solely to a sequence of actions that it takes over time, and the success of this
behavior is measured through the ability of the agent to fulﬁll (a portion of) the task. Curi-
ously, these environments, except for dialogue tasks, generally have no other agents that
interfere signiﬁcantly (or at all), but they require the agent to have an internal alignment
with itself. Such environments, be it a simulated environment or the World Wide Web, are
generally partially observable, which means that the agent must interact with the environ-
ment to understand the factual states of the objects and their interactions. Thus, they can be
formulated as Partially Observable Markov Decision Processes (POMDPs), i.e., sequential
decision-making challenges under uncertainty [
53].
As a use case, here we consider the ScienceWorld [ 376] environment—a virtual world
representation in an English text-based format, consisting of objects, actions, and tasks.
ScienceWorld has ten connected locations within a household with 218 unique objects
including instruments, electric components, animate entities, substances, and containers.
With 25 high-level action types and a much larger set of actions, its combinatorial space
quickly explodes to over 200,000 possible combinations per step. It has 10 tasks with a total
set of 30 sub-tasks. The average number of steps needed to fulﬁll a task varies from only a
few to hundreds of steps. The rewards in ScienceWorld are highly quantized to help agents
learn more effectively. Typically, the agents are given a total of 100 actions for an episode,
during which their score improves if sub-goals of the episode are achieved, i.e., if the agent
progresses on the right path. A schematic illustration of the ScienceWorld environment, for
a task where an agent must pick a fruit and place it in a blue box in the kitchen, is shown in
Fig.
3.2.
How can an agent exhibit internally consistent, collaborative behavior on such tasks?
Researchers so far have proposed several ideas. One idea has been that of devising a multi-
agent planner-actor paradigm, where a planner provides plausible high-level sequences of
actions that may or may not be executable in the environment. This is because the envi-
ronment is only partially observable, so the planner cannot anticipate, for example, what is
the conﬁguration of the objects in the bedroom. Hence, a second agent, a so-called actor, is
designed to consider the high-level plan, together with the environmental information, and
carry out the plan in a step-by-step manner. Inevitably, this means that the plan will occa-
sionally need to be adapted, which can be attempted by the actor, or for which the planner
model can be re-prompted to adapt its plan. Such a dual-agent process can be realized by
using a large language model, such as GPT-4, for the high-level planning step, and a much
smaller model, such as FlanT5-large, for the acting step [
196]. The transition of “control”,
i.e., how often the planner consults the actor, is typically based on heuristics, such as the
number of actions without a reward. The SwiftSage method realizing the dual planner-actor
paradigm is depicted in Fig.
3.3.

44 3 Collaborative Commonsense AI
Fig. 3.2 Illustration of the ScienceWorld text-based game, where an agent’s goal is to pick a fruit
(e.g., an apple) and place it in a blue box located in the kitchen. Originally appears in [ 53]
Fig. 3.3 The planner-actor model called SwiftSage [ 196]. In the red planner (Sage) part, an LLM
is fed the task information, history, and environmental conﬁguration, with instructions to locate the
relevant objects, plan and track subgoals, and detect and ﬁx exceptions. The LLM provides this
information in the form of a plan, which is then grounded by an LLM into a buffer of actions that
are possible in the environment. The green Swift part (i.e., the actor) is a smaller LM trained by
imitation learning to devise the next action, while also observing the information provided by the
Sage model. When the progress of the agent reaches a plateau, the Sage model is again activated to
perform another round of high-level planning. Such a switch happens when: the agent gets stuck with
consecutive no reward, it produces an invalid action, its action involves a critical decision like giving
the ﬁnal answer for an experiment, and an exception occurs

3.3 Modeling Self: Planning, Memory, and Interaction Goals 45
Besides planning, another essential mechanism that agents must have is a memory of
the task history. Agents must possess historical knowledge to avoid repeating steps they
already took and to model their current state in the episode more precisely. In SwiftSage,
the memory includes observations and rewards for the 10 most recent actions and the list of
rooms (without duplication) that the agent visited. Chhikara et al. [
53] experimented with
both a memory of the past actions taken and a memory of the correct actions taken by the
model. They conclude that preserving the past correct actions is more useful for both LM
and reinforcement learning agents, likely because it helps the model to reinforce successful
strategies and prevent it from repeating unsuccessful actions. The memory can be short-term
(within an episode) or long-term (across episodes). The ExpeL [
408] method represents an
attempt to devise an experiential learning agent, which gathers experiences from training
tasks through trial and error. Then, it derives insights from these experiences, which are
used as in-context examples during test time. ExpeL can be seen as an analog to the idea of
case-based reasoning, where prior experiences are considered at test time to help with the
model prediction.
Another way to enhance the mental model of the environment is to enrich its representa-
tion with commonsense knowledge about the physical properties of the environment. Specif-
ically, as text-based games and similar environments revolve around taking sequences of
actions, it is important to explicitly model the afforded actions (or affordances) for the objects
in a particular state of the environment. Inspired by perceptual psychology’s claims for the
central role of affordances in the categorization of the environment by living beings [
111],
Chhikara et al. [ 53] provide a method for including affordances. As affordances are not
given explicitly by the environment, they are retrieved from external sources, speciﬁcally
ConceptNet [
331]. Following the utility dimension of commonsense knowledge [ 150], the
relations capableOf and usedFor are obtained for the objects in a given episode. For the
example in Fig. 3.2, the model would inject information that an apple affords being eaten
and boxes can contain objects.
Example affordances and their effect on four models are shown in Fig. 3.4. Here, DRRN
is a deep reinforcement learning method, KG-A2C is a knowledge graph-enhanced rein-
forcement learning method, Swift is the actor language model from the SwiftSage method,
and the fourth model is RoBERTa. Curiously, the knowledge injection in these four mod-
els functions in different ways. In DRRN, affordances are stored as a separate input and
encoded with a GRU component. In KG-A2C, the affordances are used to enrich the knowl-
edge graph and enhance the graph embeddings. In Swift, the affordances are stored as part
of the model input, whereas RoBERTa is adapted to affordance knowledge presented via a
multiple-choice question-answering task. The ﬁgure shows that the language models ﬁnish
the given task, whereas the reinforcement learning methods get to 66 and 75% respectively.
Given the consistent improvement brought by affordance knowledge on this task, it can
be assumed that affordance knowledge about wires (e.g., capable of corroding) and tables
(e.g., being used for support) enables these models to infer that they are non-living things.
However, the examples also show that the quality of this knowledge can be made more

46 3 Collaborative Commonsense AI
Fig. 3.4 Actions taken by four affordance models on the task of ﬁnding a non-living object and
moving it to a particular container. Blue .= step index, green .= cumulative score, and yellow .=
correct action. Figure originally appears in [ 53]
directly relevant to the task, e.g., by supplementing affordances with taxonomic information.
It is not clear to what extent the current implementation of these mechanisms is meaningful
to human collaborators, motivating future in-depth studies.
3.4 Modeling Other Agents: Theory-of-Mind
When humans collaborate with other agents, there is an assumption that they think and have
mental models [ 205, 333]. As a core domain of reasoning, intuitive psychology in humans
develops early and is universal, automatic, and fast. While the nature of this psychology
is hotly debated, its existence is not controversial. This commonsense modeling of other
people’s mental states is typically called Theory-of-Mind.
By extension, AI that is expected to work with humans, i.e., to be collaborative, needs
to possess reliable Theory-of-Mind. Indeed, following a pattern of adapting psychological
tests originally designed for humans to tests for machines, Theory-of-Mind benchmarks
are emerging to test the ability of AI models to reason about other agents. These tests
include visual psychology tests created for infants, together with natural language tasks in
question-answering format used initially to test older children.

3.4 Modeling Other Agents: Theory-of-Mind 47
Large language models have the linguistic ability to express Theory-of-Mind utterances,
such as “Susie thinks that the cake was eaten by Mike”. This, together with their strong
performance across many language and vision tasks, has inspired signiﬁcant interest and
enthusiasm about the extent to which they can reason about the mental states of other agents.
Thus, Kosinski [
178] performed Theory-of-Mind testing of large language models, showing
that LLMs exhibit Theory-of-Mind skills in situations of unexpected content and unexpected
transfer such as the following Here is a bag ﬁlled with popcorn. There is no chocolate in
the bag. Yet, the label on the bag says “chocolate” and not “popcorn.” Sam ﬁnds the bag.
She had never seen the bag before. She cannot see what is inside the bag. She reads the
label. Kosinski concludes that either (i) existing Theory-of-Mind tests are valid, in which
case LLMs already have this ability; or (ii) LLMs do not have Theory-of-Mind, which also
invalidates long-standing tests for people.
This dilemma and conclusion are questioned by Ullman [ 357], who tests the abilities of
LLMs on the same two ToM categories with several alterations. The unexpected content
alterations are shown in Fig.
3.5. For instance, in the “transparent access” case, the sentence
The bag is made of transparent plastic, so you can see what is inside is added to the situation
description. In this case, it becomes irrelevant what the label of the bag says, because now
Sam can see it is ﬁlled with popcorn. And yet, the LLM is highly conﬁdent (95%) that the
bag contents are chocolate. Similar ﬁndings are reported for the other alterations designed
in this paper.
Ullman’s analysis shows that the emergence of Theory-of-Mind in LLMs does not hold on
the modiﬁed scenarios. Minor alterations of the original scenarios lead to consistently wrong
answers by the tested model (GPT-3.5). Ullman further argues that, while the emergence of
such skills from linguistic data is in principle possible, it is unlikely to happen spontaneously.
Similar to other core cognitive skills, such as analogy, ToM has a rich tradition of studies and
theories. Respectively, some computational models implement these cognitive principles
using Bayesian models and reinforcement learning [
18, 155], and they can be integrated
with large language models in future work. How to best achieve this integration is an open
question. Sap et al. also propose to tackle Theory-of-Mind by developing person-centric
models, which contain sets of neurons that are activated for speciﬁc people [
304].
In another research, Zhou et al. [ 413] discover that GPT-4 and PaLM 2 seemingly excel
at tracking the character’s beliefs in stories, providing an encouraging result that perhaps
these (most likely) larger models have a more robust ability for Theory-of-Mind reasoning.
However, these models struggle to translate this inference into corresponding actions. A
strategy to “foresee and reﬂect” is designed by the authors, which improves the models’
ability to act per their mental modeling of other agents. Y et, the performance of this model
only reaches 71%, signifying that the path to ToM modeling and consistent acting is still
unclear, and requires further research. Another important research direction is to investigate
the impact of the current (imperfect) ToM AI mechanisms in human-AI teaming scenarios.

48 3 Collaborative Commonsense AI
Fig. 3.5 Alterations of unexpected content Theory-of-Mind challenges, devised by Ullman [ 357]
3.5 Multimodal Interaction
Multimodal navigation and manipulation tasks, as in embodied vision-language planning
(EVLP), intersect the areas of computer vision, natural language processing, and embodied
AI [ 97]. Within EVLP , the setup can be still divided into stateless (a one-off setting like
question answering) and sequential, such as navigation. The EVLP tasks differ in terms
of the action space (e.g., type and number of possible actions), required reasoning modes
(e.g., instruction-following or information-gathering), and whether the task requires a dia-
logue with another agent. EVLP tasks are commonly designed to focus on a single actor
in a simulated environment that otherwise remains static over time. As such, multi-agent

3.5 Multimodal Interaction 49
constructs, and real-world environments with spontaneously changing circumstances (e.g.,
a book slipping from the library shelf) have been seldom considered.
Francis et al. [ 97] provide a taxonomy that organizes the space of EVLP with ﬁve tasks:
vision language navigation [ 11, 241], vision and dialogue history navigation [ 75, 347],
embodied question answering [ 67, 388], embodied object referral [ 49, 285], and embodied
goal-directed manipulation [ 318, 335]. Vision language navigation (VLN) requires an agent
to navigate to a goal location in the environment following an instruction. In embodied
question answering (EQA), the agent receives a natural language question, whose answer
requires navigating the environment to collect information. Embodied object referral (EOR)
is a task where the agent navigates to an object mentioned in an instruction, which has to be
identiﬁed upon reaching its location. Vision and dialogue navigation (VDN) is a task that
allows an agent to interact with another agent (e.g., a human collaborator) to resolve the
uncertainty. Embodied goal-directed manipulation (EGM) is a task that requires a broader
manipulation of various objects in a scene, which may combine the above tasks. A description
of these tasks in terms of their need for navigation, object identiﬁcation, and environment
interaction, as well as their expected reasoning modules, is shown in Table
3.2.
Table 3.2 EVLP tasks, courtesy of [ 97]. Properties of Embodied Vision-Language Planning (EVLP)
tasks: ‘Navigation’ describes whether navigation is part of the actions for the task; ‘Object identi-
ﬁcation’ indicates whether the agent may only solve the task through identifying speciﬁed objects;
‘Environment Interaction’ indicates whether or not the agent can mutate environment state, e.g.,
through dialogue-based interaction with another agent or through object manipulation; and ‘Primary
reasoning mode(s)’ describes how agents are intended to interpret the task
Task Navigation Object
identiﬁcation
Environment
interaction
Primary reasoning mode(s)
VLN ✓ ✗ ✗ Understanding object and scene
layout properties;
instruction-following
EQA ✓ ✓ ✗ Exploration and
information-gathering
EOR ✓ ✓ ✗ Understanding spatio-semantic
object relations and scene layout
properties; instruction-following
VDN ✓ ✗ ✓ Understanding object and scene
layout properties; multiple
instruction-following
EGM ✓ ✓ ✓ Understanding object
affordances, environment
attributes, and scene layout
properties; instruction-following

50 3 Collaborative Commonsense AI
EVLP tasks have inspired many approaches that model vision, language, and planning
jointly. While initial work has modeled language and vision independently, it is more com-
mon in contemporary work to combine these two modalities using attention or transformers.
To model action generation and planning, the agents need to understand their goal, the scene
context, and its understanding of how to satisfy the goal through a sequence of adequate
actions executed to modify the state of the environment. Here, it is common to distinguish
between a fully observable, where the agent knows the location of the goal position, and a
partially observable environment, where the agent only has information about the adjacent
admissible states. In the latter case, sequential decision-making is essential, as the agent
cannot anticipate the state of the rest of the environment. Common strategies for planning in
EVLP tasks, inspired by robotics techniques, include mapping and exploration, search and
topological planning, and hierarchical task decomposition [
97].
Curiously, while EVLP tasks include interaction with the environment and are collabo-
rative in the sense that a goal is communicated to the agent, only VDN and EGM are based
on collaboration with other agents. The interaction in these tasks can be realized through the
use of an ambiguity resolution module (i.e., an oracle that knows the agent’s state and goal)
or dialogue, where the agent communicates with an oracle about clarifying its instruction.
In practice, VDN and EGM are typically realized in a static, multi-turn question-answering
format, which simulates conversations between the protagonist agent and other involved
agents.
As a relatively new direction, EVLP has a lot of room for research contributions [ 97]. An
essential part of future EVLP tasks, datasets, and approaches is to include more ambitious
social interaction, which would enable a more natural transition to more dynamic environ-
ments and the emergence of new collaborative and assistive capabilities of the agents. Social
interaction between the agents can facilitate shared decision-making and action selection
between multiple agents. Here, the changes made by the agents would ideally beneﬁt the
other agents. To ensure this, the agents must collaborate toward a shared understanding of
the physical space and the task structure. Such capabilities are even absent from the tasks
that already include interaction, such as VDN and EGM, as the interaction, in this case,
is static, with pre-generated dialogue histories provided at the start time. The collaborative
mechanisms that are of interest include those discussed in the earlier sections of this chapter,
such as modeling agent goals, ToM, and modeling the environment, as well as generating
useful statements and questions for the other agents, abstraction over prior experiences,
and designing mechanisms that beneﬁt from the task progress feedback. Another direction
of interest is designing more advanced mechanisms for human-machine interaction within
EVLP tasks, to enable effective and efﬁcient communication with humans.
As apparent in Table 3.2, commonsense reasoning about object and environment proper-
ties, object affordances, and spatiotemporal relations is a critical component of addressing
EVLP tasks. Commonsense knowledge remains largely missing in these environments and
approaches. While pre-trained models may possess some of this implicit knowledge needed
for the task, it is typically challenging to decide dynamically what type of commonsense

3.6 Summary and Discussion 51
knowledge should be used, e.g., declarative, procedural, or metaphorical. Wrongly selected
knowledge may have countereffects. Given the ultimate goal to develop intelligent agents
capable of solving real-world problems, it is essential to devise methods for enhancing mod-
els with assumed knowledge [
395], to the extent that EVLP tasks can be seen as the next
level of tasks for preparing these models for real-world usage.
3.6 Summary and Discussion
This chapter surveyed to what extent state-of-the-art AI can exhibit mechanisms for col-
laboration with humans or other agents. This overall question was decomposed into four
speciﬁc aspects of agent collaboration. We ﬁrst investigated whether AI can reliably model
and simulate situations . A representative method, called Imagine-and-V erbalize was pre-
sented and analyzed in terms of its effectiveness, showing positive, yet modest, impact on
the task of generating stories. The discrete scene representation of this method, coupled
with the neural models that generate and verbalize the scene graphs, may be a promising
avenue for further innovation in collaborative AI. Besides modeling situations, the AI also
needs to model itself and other agents when it is part of the scene and needs to interact with
others. Here, we considered the setup of interactive tasks, such as text-based games, in which
an agent needs to navigate an environment by performing actions and ultimately trying to
achieve its goal. Collaborative mechanisms for modeling its own state include memorization,
planning, and understanding physical affordances. We note that language models provide
very simple and intuitive interfaces for integrating this information, and such enhancements
of the agent state generally lead to improvements in task performance. At the same time,
these improvements are relatively minor and it is often difﬁcult to trace them back to the
mechanisms that allegedly caused them via qualitative analysis. Modeling other agents as in
ToM, which is arguably even more challenging, has also been an attractive area of research,
with substantial studies of whether state-of-the-art AI models, especially LLMs, exhibit
robust Theory-of-Mind and whether this skill helps them act consistently. Here, again, we
see encouraging overall results and boosts in accuracy, however, this skill does not seem to
be robustly shown by the models, nor it leads to actions that are consistently taken following
the mental models. Finally, multimodality has beneﬁted a lot from recent progress in visual
and language models, as well as fusion models that combine the two modalities. Integrating
these modalities with other collaborative mechanisms, such as shared situational represen-
tations, planning, and Theory-of-Mind, is only starting to be explored. Similarly, prolonged
interaction and collaboration in a multimodal setting between humans and AI, or between
multiple AI agents, are exciting research directions that are currently in an early stage.
In summary, there has been clear progress in developing models that can exhibit collab-
orative skills. This has recently resulted in LLMs and visual models that can interact with
people about arbitrary inputs and provide a relevant response. Meanwhile, the four collabora-
tive aspects investigated in this chapter reveal that collaborative AI is generally inconsistent

52 3 Collaborative Commonsense AI
and unpredictable, making it difﬁcult to make precise claims for or against its abilities to
reason about situations, agents, or modalities . Both larger models and the integration of
symbolic knowledge bring improvements in terms of overall performance, and yet, it is
difﬁcult to characterize the qualitative jump that stems from those quantitative increases.
Here, an encouraging trend is the increasingly tighter integration of AI with other research
areas, in particular cognitive psychology and linguistics, where such phenomena have been
studied extensively and have resulted in theories, ﬁndings, and experimental methodologies.
Often times, the main factor that distinguishes two series of ﬁndings, especially if they
leverage the same model, lies in their differences in terms of the evaluation protocol. For
instance, in the case of Theory-of-Mind, Kosinski concluded that LLMs have ToM, Ullman
that they have it on the original benchmarks but fail upon minor alterations, and Zhou
et al. demonstrated that there is nevertheless a large gap between the static possession of
such models and their translation into in-context actions. While such ﬁndings may seem
contradictory at ﬁrst, there is an explanation that models have certain signals that allow
them to identify the correct state of the other agents more often than random, but this skill
is not consistently exhibited, and thus, it is safe to say that Theory-of-Mind is not yet a
conﬁrmed skill of state-of-the-art LLMs. On a more general note, such discrepancies in
ﬁndings reveal a lack of standardization in the community about what constitutes a good
evaluation to quantify and qualify the possession of a skill by a model. Evaluation should be
representative in terms of size, as small-set benchmarks are easily gamed by trying solutions
often enough. And yet, large benchmarks created with a lot of effort and best intentions end
up being gobbled by LLMs, so their next iteration will solve this benchmark, more likely
due to memorization than due to having acquired a certain skill. The benchmarks need to be
grounded in theories, e.g., from cognitive psychology. The beneﬁt of such psychology-based
studies is that they are often carefully constructed to test a particular kind of phenomena,
however, scaling up such benchmarks is non-trivial to achieve, resulting in typically small
benchmarks with unclear representativeness.
As collaboration requires longitudinal interaction over time and space, which may be
driven by explicit goals, a possible switch is to think of evaluation in terms of simulated
environments rather than one-off benchmarks . Such interactive setups include dialogues,
gaming environments, and web navigation, but also more open-ended tasks relating to lateral
thinking, investigations, and brainstorming. Such tasks provide a more natural playground
and enable the interaction between the AI and people to develop in time and possibly
space. An increasing number of dynamic environments are being developed, which is an
encouraging trend. A trade-off that emerges is between leveraging these environments for
open-ended explorative tasks, which beneﬁt from less constrained interaction but are more
difﬁcult to evaluate objectively; and goal-driven tasks, which are easier to evaluate but may
impact the expressivity of the environment signiﬁcantly.

3.6 Summary and Discussion 53
Enhancing the consistency of the developed models is important for collaboration with
people. Methods like Imagine-and-V erbalize and cognitively inspired Bayesian models pro-
vide an opening to build such neuro-symbolic AI that leverages the ability of neural models
to collaborate on any input with the ability of symbolic models to abstract and predictably
perform reasoning. Recently, such neuro-symbolic frameworks have been called “LLM
sandwich”, as they leverage language models to interpret the input and verbalize the rea-
soning, whereas the inside of the sandwich is an out-of-the-box reasoning method.
1 The
promised beneﬁts from such architectures include reliable problem-solving, mathemati-
cally precise answers, decision transparency, and efﬁcient run-time computing costs. We
will discuss approaches to combine neural and symbolic architectures in the next chapter
on Robustness.
1 https://ec.ai/the-llm-sandwich/, accessed on February 23, 2024.

4Robust Commonsense AI
Abstract
The emergence of (large) language models has resulted in a paradigm shift in terms of
developing general-purpose models that can contribute to a variety of tasks and domains.
For the ﬁrst time in the history of AI, the community of researchers has access to pre-
trained models that can perform repeated inference across many unanticipated natural
language tasks, from text classiﬁcation through question answering to summarization.
Moreover, these models can be tuned further to ﬁt the needs of the downstream task
more directly by using adequate training data, thus enhancing the model performance on
target tasks. While the generalizability of language models is clear and can be witnessed
by experts and non-experts alike thanks to public APIs like ChatGPT, their robustness
has been repeatedly shown to be fragile. Language models struggle with adequately
weighing minor variations in the inputs (e.g., in negation or perturbation probes), they
may be unable to perform well in novel settings (e.g., in domain-speciﬁc applications),
and their predictions may be inconsistent across different phrasing of the same input (e.g.,
in information extraction settings). This chapter discusses these challenges in more length
and provides a summary of directions for designing robust AI that leverages the power of
LLMs in combination with data augmentation with other models or graphs, with novel
methods for language model adaptation such as in-context learning and preﬁx-tuning,
with neuro-symbolic integration with code and logic interpreters, and with analogical
principles. This chapter discusses representative methods from each of these research
directions in terms of their motivation, design, results, strengths, and weaknesses. The
chapter concludes with a summary of lessons learned and open challenges that can be
pursued to develop even more robust AI in the future.
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_4
55

56 4 Robust Commonsense AI
4.1 Background and Challenges
The emergence of (large) language models has resulted in a paradigm shift in terms of
developing general-purpose models that can perform well on a variety of tasks and across
domains. For the ﬁrst time in AI history, we have access to pre-trained models that can
perform repeated inference across many unanticipated tasks, from text classiﬁcation through
question answering to summarization, without any adaptation. Moreover, these models can
be tuned to ﬁt the needs of the downstream task more directly by using adequate training data,
further improving the model performance on target tasks. In the euphoria surrounding these
models, fundamental and traditionally challenging task families ranging from commonsense
reasoning to natural language processing have been proclaimed to be ‘solved’.
The appeal of language models’ general applicability can be observed through the wide
range of models that have been created to ﬁt the diverse set of tasks, computational require-
ments, and adaptation needs. One division of the language models is into three categories
based on their structure: encoder-only, encoder-decoder, and decoder-only [
269]. Encoder
models, like BERT [ 80] and its descendants including RoBERTa [ 207], are trained to predict
a speciﬁc number of masked tokens in a sentence, which makes them adequate for tasks
like text classiﬁcation and natural language inference. These models have been generally
developed between 2018 and 2021, and there has been little innovation in new models since.
Encoder-decoder models use an encoder to transform the textual input into a hidden-space
vector, after which a decoder is used to generate the target output text. Encoder-decoder
models, including T5 [
289], can be trained using a ﬂexible objective, and are especially
suitable for generating sentences based on a dynamic context in tasks like summarization
and question answering. Encoder-decoder architectures emerged in 2019 with BART and
T5, with a consistent ﬂow of models being developed in the years since then through this
date. Decoder-only models are trained to predict the next word in a sequence. This family of
models was pioneered by GPT-1, GPT-2, and XLNet in 2018, shortly after the introduction
of the BERT model. Recently, we have witnessed an expansion in decoder-only models,
including the GPT-3, Bard, PaLM, and GPT-4 models and open-sourced counterparts like
Llama [
350] and Vicuna [ 54].
These three categories with their representative models paint a wide palette of options for
practitioners and researchers to choose from, given their application needs. While the gener-
alizability of language models is apparent and can be witnessed by experts and non-experts
alike thanks to public APIs like OpenAI’s ChatGPT, their robustness has been repeatedly
shown to be fragile. Language models struggle with adequately weighing minor variations
in the inputs, for example, making their predictions insensitive to negation [
352]. On the ﬂip
side, they can be thrown off by minor adaptations in the spelling, such as typos, as shown by
perturbations that “fool” a large set of models [
370], such as womn instead of woman,o re v e n
leaving whitespace before a semicolon. When performing a novel, out-of-distribution task,
LLMs exhibit consistently lower performance than a comparative in-domain task [
371].

4.2 Data Augmentation with Knowledge Graphs 57
A common manifestation of the fragile robustness of these models is their inconsistent
predictions for tasks that require identical (and sometimes simple) forms of reasoning. In
[
118], Goldberg used a dataset of 5,000 probes of the form X was educated at Y ,a n d
asks the model Who was educated? The results of this analysis show that in over 10% of
the cases, a model trained on the SQUAD question-answering dataset provides no answer.
Curiously, varying the question to similar forms, like Who was educated somewhere? or Who
was educated at a university? results in similar trends, often with many more unanswered
questions. The performance of ChatGPT on this task is signiﬁcantly better, but it still answers
around 2 percent of the questions wrong, occasionally extracting the school instead of the
person’s name.
What may be the cause of this behavior of the models? Razeghi et al. [ 294] analyze the
relation between model accuracy and training time frequency for various numeric combina-
tions on arithmetic multiplication tasks. Their analysis shows a strong correlation between
the frequency of occurrence of a certain term at training time, and the ability of the models
to perform multiplication accurately with this term at test time. For example, the analyzed
model can compute 24
.×18 with much higher accuracy than 23 .×18, arguably because 24
occurs 20% more frequently during training than 23. This observation has been also shown
for other tasks such as question answering [
218] and commonsense inference [ 373], as well
as zero-shot multimodal tasks [ 356]. At the same time, it has been shown that the models
can perform certain abstractions beyond mere memorization: for instance, translating pop-
ular lateral thinking puzzles to new contexts yields similar performance by large language
models, even though they have not seen the adapted puzzles at training time [
160].
The rest of this chapter discusses these challenges in more length and provides a set
of existing efforts for designing robust AI that leverages the power of LLMs in combina-
tion with other strategies. These complementary strategies include data augmentation with
other models or graphs, novel methods for language model adaptation such as in-context
learning and preﬁx-tuning, neuro-symbolic integration with code and logic interpreters, and
adapting language models through analogical principles. This chapter discusses represen-
tative methods from each of these research directions in terms of their motivation, design,
results, strengths, and weaknesses. It concludes with a summary of lessons learned and open
challenges that can be pursued to develop more robust AI in the future.
4.2 Data Augmentation with Knowledge Graphs
An intuitive idea for augmenting neural (language) models is by leveraging existing repos-
itories of curated knowledge, namely knowledge graphs. While language models con-
tain general knowledge and can generalize to any situation, their robustness is hindered
by their implicit knowledge processes, manifesting in hallucination, indecisiveness, and
lack of domain-speciﬁc or new knowledge. Knowledge graphs, conversely, contain explicit
knowledge, follow a standard structural representation, and can evolve and describe domain

58 4 Robust Commonsense AI
information. These complementary properties have led to several directions for augmenting
LLMs with knowledge graphs.
To begin with, similar to language models, knowledge graphs themselves are also not a
homogeneous category. They differ in terms of their coverage of node types (events, con-
cepts, frames), creation methods (automatically created, crowdsourced, manually written by
experts, distilled from LLMs), granularity of their nodes and relation types, and representa-
tion formats (e.g., RDF, qualiﬁer model) [
152]. In particular, knowledge graphs describing
common sense can be grouped into several high-level categories in terms of their topics:
commonsense knowledge graphs (e.g., ConceptNet [
331], A TOMIC [303]), common graphs
and ontologies (e.g., Wikidata [ 364], Y AGO [342]), lexical resources (e.g., WordNet [ 237],
FrameNet [ 17]), and visual resources (e.g., Visual Genome [ 181], Flickr30k [ 281]). While
this heterogeneity provides an opportunity for using many resources together, it also brings
a challenge, as these sources follow different modeling approaches, often have imprecise
descriptions in their nodes, and have sparse mappings between their nodes and relations.
CSKG (CommonSense Knowledge Graph) [ 152] addresses this heterogeneity by inte-
grating seven popular sources. CSKG follows the following ﬁve principles: preservation of
the node representation heterogeneity, reuse of the edge types across resources, application
of any existing links between the resources, generation of additional high-quality proba-
bilistic links, and easy access to labels [
152]. To accommodate these principles, CSKG is
modeled as a hyper-relational graph, describing edges in a tabular format with an arbitrary
set of columns serving as qualiﬁers. CSKG follows the philosophy embedded in most com-
monsense resources of minimizing the number of relations while enabling nodes to be freely
represented with text and optionally an associated semantic identiﬁer. An example subset
from the CSKG graph is shown in Fig.
4.1.
How can such commonsense knowledge graphs be used to enhance language models?
One direction is to leverage the richness of visual, social, and conceptual knowledge in CSKG
to generate synthetic data for model adaptation. Speciﬁcally, [
216] adopts a multiple-choice
Fig. 4.1 Snippet of CSKG [ 152], for the example task of connecting the context On stage, a woman
takes a seat at the piano. She: with the correct answer: nervously sets her ﬁngers on the keys.
CSKG combines: (1) lexical nodes (piano, keys, music; in blue), (2) synsets like piano (artifact), seat
(dramaturgy) (in green), and (3) frames ( fn:noise_makers) and frame elements ( fn:fe:use)
(in purple). The link between pianoand piano (artifact)is missing, but trivial to infer

4.2 Data Augmentation with Knowledge Graphs 59
question answering formalism, which can be applied to a variety of other tasks as well,
including pronoun resolution and natural language inference. For such a task, CSKG paths
can be sampled one at a time and lexicalized into natural language question-answer pairs
by using a template or generative language models. Speciﬁcally, the head and the relation
can form a question (e.g., What is a possible purpose of losing weight? ), whereas the tail
can be directly used as an answer (e.g., being healthier ). To alleviate the challenge of long
paths becoming ambiguous, this work focuses on sampling one-hop paths from the graph.
An illustration of this question generation pipeline is shown in Fig.
4.2.
Generating distractors for the correct answer is another challenge. Distractors that are
too similar to the correct answer are more likely to be correct too, making the task unfair.
Alternatively, distractors that are too dissimilar are fair, but they may make the data uninfor-
mative, as the model may already be able to spot the answer without adaptation. To generate
distractors that are both informative and fair, Ma et al. [
216] experiment with three strategies
besides random sampling: selecting distractors with high similarity to the answer, distrac-
tors with high similarity to the question, and discarding adversarially the questions whose
distractors are not sufﬁciently challenging at training time. The experiments show that this
synthetic data has a signiﬁcant positive impact on the model robustness, enabling language
models to perform better in a zero-shot setting across ﬁve benchmarks involving physical,
social, and conceptual reasoning.
A key takeaway from this paper is that the effect of background knowledge is proportional
to its alignment with the task properties. To investigate the effects of this alignment directly,
we have deﬁned relational dimensions of commonsense knowledge in CSKG [
150], which
led to the clustering of the knowledge into 13 partitions. Example dimensions are temporal,
spatial, and part-whole knowledge. By pretraining language models on one knowledge
partition at a time, it is possible to understand the alignment between a knowledge type and
Fig. 4.2 Question generation pipeline from [ 216]. Paths sampled from CSKG are lexicalized into
questions and answers. A subsequent distractor sampling step selects fair and informative distractors.
Finally, the question, answer, and distractors are combined into a data sample for model adaptation.
The process is repeated for the next sample triple

60 4 Robust Commonsense AI
the task at hand. In other words, we can study whether models can perform more robustly on a
given commonsense dimension by a focused pretraining with a carefully selected partition of
the graph. The results for this hypothesis, shown in Table
4.1, highlight several trends. First,
simply merging as much knowledge as possible is not optimal, instead, the best performance
is typically achieved by using the relevant knowledge in a more focused manner. This ﬁnding
is partially due to the catastrophic forgetting phenomenon, where the models fed with too
much data may overwrite important knowledge learned during pretraining. Second, certain
knowledge types are generally more informative to the models than others, e.g., temporal
knowledge yields a high gain in robustness for the models across datasets, whereas lexical
knowledge has a very limited beneﬁt. This is largely because the former knowledge type
is much more difﬁcult for the models to absorb, while the latter is largely acquired during
training. Third, the results conﬁrm the effect of aligning knowledge types between the
synthetic data and the task. Knowledge about the utility of objects plays the most important
role in the general task of commonsense QA, while temporal and motivational knowledge is
essential for social reasoning. Stronger claims about the robustness of the dimension-based
models require further analysis of these adaptations over a wider set of benchmarks and
relevant probing strategies.
The knowledge graph information can be used to enhance LLMs in other ways beyond
QA. The structured knowledge, formalized as lexicalized task-based paths, may be injected
to enrich the input formulation via an attention mechanism [
27, 206] or through an aux-
iliary training objective [ 392]. COMET [ 37], a generative knowledge model adapted to
Table 4.1 Zero-shot evaluation results of adapting RoBERTa with dimensional knowledge for two
commonsense reasoning tasks [ 150]
Dimension CSQA SIQA
Baseline 45.0 47.3
+part-whole .63.0(±1.4) .52.6(±1.9)
+taxonomic .62.6(±1.4) .52.2(±1.6)
+lexical .49.9(±2.9) .49.0(±0.4)
+distinctness .57.2(±0.5) .50.2(±1.5)
+similarity .61.4(±0.8) .53.5(±0.6)
+quality .65.7(±0.5) .60.0(±0.7)
+utility .67.4(±1.0) .54.8(±0.7)
+creation .49.9(±1.1) .47.8(±0.2)
+temporal .67.3(±0.3) .62.6(±0.9)
+relational-other .58.2(±1.7) .51.3(±1.7)
+spatial .63.3(±0.2) .53.1(±0.3)
+desire/goal .65.0(±1.8) .60.0(±0.6)
+all .66.2(±1.4) .61.0(±0.7)

4.2 Data Augmentation with Knowledge Graphs 61
commonsense KGs, can be leveraged to enrich the task input with commonsense infor-
mation. Expanding on the idea of COMET, commonsense knowledge graphs can also be
used to adapt LMs directly for a knowledge completion task using a variety of objective
functions [
20]. Augmenting the inputs with further information can be done proactively
through a self-talk [ 321]. Using self-talk, a language model is adapted to ask clariﬁcation
questions such as “ What is the deﬁnition of... ” to discover additional background knowledge
conditioned on a given context. This background knowledge can come from ConceptNet or
COMET, for instance.
Can knowledge graphs also be used to generate longer synthetic data points, such as mini-
stories? One such method leverages CSKG in intersection with commonsense axioms [ 151].
In this method, illustrated in Fig. 4.3, given a manually deﬁned story type (e.g., substitution or
unmet expectations), a story type formalization step leverages commonsense axioms deﬁned
by Gordon and Hobbs [
120] to deﬁne a speciﬁcation for stories, describing their axioms and
relations of interest. This speciﬁcation then serves as a query over the CSKG graph, which
yields speciﬁc paths that fulﬁll the set criteria. For instance, a substitution query can be
deﬁned as ﬁnding two objects that coincide in location and purpose. Executing this query
yields a set of possible objects that satisfy these criteria, together with the ﬁllers for the other
query variables (e.g., location = home, utility = warmth ). These paths are fed into modules
for story generation and explanation, which is the output of the data generation process.
Such a simple approach can generate over 100k stories with similar interestingness to those
generated by GPT-2 and signiﬁcantly higher consistency, according to human judges.
These stories, with their naturally dense annotation and regularity of reasoning patterns,
can be used to enhance the out-of-domain generalizability of models that judge story plau-
sibility classiﬁcation models. This is demonstrated by the LEAP framework [
161], which
enriches the training data with less than three thousand synthetic stories from CSKG. Despite
the modest size of the stories, this augmentation already provides a signiﬁcant robustness
improvement across unseen tasks for story understanding, question answering, and natural
Fig. 4.3 Story generation pipeline from CSKG [ 151]

62 4 Robust Commonsense AI
Fig. 4.4 Case studies comparing the robustness of an in-domain method (CGLI) with a method
enriched with 3,000 automatically generated stories (LEAP) [ 161]
language inference. An example of this robustness is shown in Fig. 4.4,1 which demonstrates
how the method without augmentation (called CGLI) performs well on in-domain data but
fails to generalize to novel stories. Meanwhile, LEAP’s data augmentation strategy enables
the model to perform well on novel stories that may have a different format or vocabulary
distribution.
At the same time, generating longer stories or other augmentation data formats using
knowledge graphs is a non-trivial pursuit, partially due to the ambiguous semantics of sig-
niﬁcant portions of commonsense knowledge graphs. Another limitation of such approaches
is that the templates for sampling information from the graphs are generally deﬁned manu-
ally. Coupling these graphs with language models for generation, as done in the Imagine &
V erbalize method for stories [ 375] is a promising direction forward. However, the limitation
of this alternative is that the generated stories may be unfaithful to the graph information
(as discussed in the previous chapter), which may defeat the purpose of using knowledge
graphs to enhance robustness in the ﬁrst place.
4.3 Data Augmentation with LLMs
Based on evidence for their suitability as knowledge repositories [ 276], language models
have been also seen as adequate for augmenting the data to train or adapt other models.
Analogous to the usage of knowledge graphs, language models have also been leveraged in
1 Figure reprinted from Transferring Procedural Knowledge Across Commonsense Tasks; Authors:
Yifan Jiang, Filip Ilievski, Kaixin Ma; Series: Frontiers in Artiﬁcial Intelligence and Applications;
Ebook: V olume 372: ECAI 2023; Pages: 1156–1163; CC BY -CC 4.0 (2023); with permission from
IOS Press. The publication is available at IOS Press through http://dx.doi.org/10.3233/FAIA230391.

4.3 Data Augmentation with LLMs 63
two general ways: to augment the inputs with additional information and to generate new
data points.
For instance, in the PINTO framework [ 372] for question answering (cf. Chap. 2), a
medium-scale LM is prompted with the question together with each candidate answer pro-
vided one at a time. The large model is prompted to provide rationales for the suitability
of that candidate as a correct answer to a question. Then, a small-scale LM considers the
question, the candidate answer, and its generated rationale to make a ﬁnal decision on the
suitability of the candidate. This choice is motivated by the ﬁnding that general rationales
for all candidates at once are often answer-leaking, i.e., they are sufﬁcient by themselves
to select one of the choices. PINTO’s rationalization module is a frozen pre-trained LM
that uses a few question-answer-rationale demonstrations as part of the prompt. To train the
small model in PINTO, the authors adopt a counterfactual regularization objective, which
inﬂuences the model to output less conﬁdent predictions when the rationale is not utilized
properly. Such “shortcut” regularization is simulated by using two perturbation strategies
of token masking and token replacement in the generated rationales. PINTO’s robustness is
demonstrated in three ways. First, in an out-of-distribution setting, the model achieves better
generalization on different datasets without any ﬁne-tuning. Second, PINTO’s consistency,
in terms of how faithful the model prediction is to the rationales [
136], is shown to be supe-
rior over its baselines. Third, PINTO’s rationales yield better performance in low-resource
evaluation settings with less data.
In another research, the SPARK method [ 79] was designed to score quality arguments
by ﬁrst using an LLM to obtain background knowledge about the argument. In compari-
son to PINTO, SPARK designs GPT-3.5 prompts for more precise information, i.e., rather
than asking for a general rationale, it solicits feedback, possible assumptions/biases, argu-
ments with similar quality, and counter-arguments. Then, to enable the reasoning model
to consider the augmentations as clear supplements to the original topic and argument,
SPARK employs a dual BERT encoder: one encoder for the topic and argument, and the
other for the augmentation(s). SPARK’s experiments show that the method can generalize to
another, out-of-domain, dataset better than competitive baselines including GPT-3.5, other
encoders with the same augmentations, and dual BERT encoder with other (e.g., dense pas-
sage retrieval [
171]) augmentations. Combining all augmentation strategies performs better
than the baselines, however, using solely feedback augmentations enables the best robustness
to unseen datasets. Curiously, the judgment of argument quality by humans shows a reverse
trend, where the feedback augmentations were judged as the least correct (3.8/5.0) out of
the four augmentation strategies. Augmentations that enhance the robustness of language
models may not be perceived as informative by people.
Enriching the inputs enables better robustness, which can likely be attributed to an
enhanced abstraction of the models facilitated through the augmentations, which contain
information patterns that re-occur across data points. An alternative data augmentation strat-
egy can be realized by modifying the original data to create additional points for model adap-
tation. This approach is especially expected to be effective for classes that have sparse data.

64 4 Robust Commonsense AI
Multiple augmentation methods were tested in [ 330]. First, one can use a lexical resource
like WordNet to substitute the words in the input with similar words according to a synset.
For example, this would transform an initial sentence “The news is fake because so much
of the news is fake” into “The news be fake because so much of the word is fake.” Second,
Word2V ec and RoBERTa can be used for the same purpose by ﬁnding the word that is the
closest to the original word in the embedding space. In this case, the sentence may become
“The news becomes fake anyway so much of the news is bogus” with Word2V ec and “The
data is fake because so much about the information is fake” with RoBERTa. Third, an entire
phrase can be adapted by using backtranslation: namely, translating the input sentence into
a language that is syntactically and morphologically dissimilar and then reverse-translating
the translation back to the original language. Popular choices for backtranslation are the lan-
guage pairs (German, English), (Turkish, English), and (French, English). Using German-
to-English backtranslation, the augmented sentence may become “The messages are fake
because so many messages are fake.”
The experiments with these augmentations for the task of logical fallacy identiﬁ-
cation [ 330] showed that performing RoBERTa embedding-based synonym substitution
yielded the best augmentation quality; employing WordNet and Word2V ec yielded exces-
sive noise, whereas German-to-English backtranslation occasionally rephrased the fallacious
components of the sentences. The augmentation’s impact was positive on ﬁne-grained fallacy
identiﬁcation, which is likely because many of the ﬁne-grained classes suffer from sparsity,
in line with the initial hypothesis of the utility of this augmentation. The coarse-grained
performance is overall harmed by applying augmentation, where the only class that beneﬁts
from augmentation is the under-represented class of Ambiguity. Overall, we conclude that
augmenting the dataset with additional data points is mostly beneﬁcial as an upsampling
strategy to address the sparsity of low-resource classes. However, if the additional exam-
ples are minor variations of the original data, their impact would be more signiﬁcant for
in-domain than out-of-domain tasks.
4.4 Methods for Adapting LMs
Besides augmenting language models with relevant data or background knowledge, a com-
plementary idea for better robustness is to replace the step of ﬁne-tuning with another
strategy. Fine-tuning has generally been understood as a process of adapting a language
model to a particular task, using task-speciﬁc training data and its respective objectives.
During ﬁne-tuning, the model parameters are updated using the training signal from the
ground truth associated with the data. By doing so, the model learns to perform better on the
given benchmark and possibly the overall task, while its applicability to other benchmarks
may be harmed. To avoid overﬁtting and preserve the knowledge that language models have
acquired during their pre-training phase, there are lightweight alternatives to ﬁne-tuning
that still leverage in-domain data [
216, 276]. The underlying premise of these approaches

4.4 Methods for Adapting LMs 65
is that the model will be able to generalize better across commonsense datasets and focus
on acquiring the knowledge that is relevant and has not been acquired during pre-training.
To achieve these goals, prior work has come up with approaches that only update a
small number of additional model parameters, or that update the inputs while keeping the
model weights intact. The ﬁrst method of extending the model with preﬁxes is known as
preﬁx-tuning [
194], whereas the second approach of learning effective prompts automati-
cally is dubbed AutoPrompt [ 316]. A study by Ma et al. [ 218] has compared these three
adaptation strategies for two models: the auto-regressive language model GPT-2 [ 288]a n d
sequence-to-sequence language model BART [ 190], on the generative evaluation bench-
marks ProtoQA [ 35] and CommonGen [ 199], by adapting them on different partitions of
the training data. As can be expected, the performance of ﬁne-tuning is the best, as it learns
both the content of the data and the structure of the task. Fine-tuning also suffers from over-
ﬁtting and limited generalization to novel answers unseen in the training data. Conversely,
learning how to generate effective prompts yields lower accuracy overall, but it has a higher
robustness to adversarial splits. The authors here concluded that preﬁx-tuning may represent
a sweet spot between task accuracy, generalization, and robustness.
Curiously, the analysis in this study shows that models can generally retrieve the answers
better if they are also answers to similar questions in the training data. For instance, the model
learned the answer cauliﬂower for the training question Name a vegetable that people like
to steam, which is coincidentally also a correct answer to the dev question Name a vegetable
that is as large as your head . In such cases, models answer correctly, but arguably for
the wrong reasons. To further examine the prominence of this phenomenon, the authors of
[
218] investigate whether the models memorize the training data or learn to reason on novel
questions and answers as well. They annotate 30 questions from the ProtoQA development
set, where the model answers are at least partially correct, and manually change the question
minimally to preserve the reasoning process while fully altering the answer set. The results
show that the models are not able to capture subtle changes in the question that lead to
a different answer set and perform memorization/retrieval rather than reasoning. Namely,
models across the board get a low performance on the new questions and a higher rate of
repeated answers (nearly half of all answers). For example, 9 out of 10 answers are shared
between the questions name something around the house that is often replaced and ...hardly
ever replaced.
Recent work has considered how to perform robust reasoning across tasks without the
need for ﬁne-tuning. A popular paradigm has been in-context learning, which relies on
prompt engineering to trigger LLM’s reasoning abilities. By providing instructions and a
small number of demonstrations, the models with in-context learning can adapt to unseen
tasks with minor adaptation and without any additional tuning. Especially effective are the
in-context learning methods that provide the LLM with additional guidance for solving a
question, such as chain-of-thought’s [
381] guidance to generate explanations before provid-
ing the ﬁnal answer, and least-to-most prompting’s [ 410] breakdown of the problem into
simpler components that can be solved individually. These methods perform strongly across

66 4 Robust Commonsense AI
a wide range of tasks involving arithmetic and commonsense reasoning and can be set and
run with minimal effort from researchers. As we will show later for analogical reasoning, in-
context learning methods still struggle with performing robust reasoning and tend to produce
hallucinations. Moreover, given the size of the models, a downside of in-context learning
approaches is that tuning the model further is typically impractical; however, it is possible
to leverage their reasoning chains and predictions in a smaller task-adapted language model,
as done by SPARK and PINTO earlier.
Language models have been repeatedly shown to lack robustness to text perturbations,
noisy data, or distribution shifts [ 245]. This ﬁnding also holds for LLMs when faced with out-
of-distribution data and noisy inputs [ 371]. How can the model robustness be improved while
retaining the beneﬁts of using language models, such as the knowledge they acquired during
pretraining? When performing classiﬁcation, one possibility is to employ prototype-based
networks (PBNs), a family designed for robustness [
192]. As discussed in Chap. 2,P B N sa i m
to ﬁnd prototypical members or features to discriminate a certain category. Computationally,
the prototypes are points in the shared embedding space, whereas their distance to data points
provides a key signal for classifying those data points. Leveraging the distance between the
points provides a way to quantify the prototypicality of a point, which then facilitates the
identiﬁcation of noisy or out-of-distribution points [
394]. Given these properties, PBNs have
been popular in computer vision tasks such as image classiﬁcation and novel class detection,
and have only recently been applied for textual classiﬁcation tasks.
The framework of [ 327] was designed to consolidate the existing PBN methods for robust
text classiﬁcation. This modular and comprehensive framework combines different back-
bone architectures (language models and CNNs), distance functions (euclidean and cosine),
and loss terms. The classiﬁcation loss computes the cross-entropy between predicted and
true labels, the clustering loss ensures that the training examples close to each prototype
form a cluster of similar examples, the interpretability loss ensures that the prototypes are
as close as possible to their closest training sample, and the separation loss maximizes
the inter-prototype distance to reduce the probability of redundant prototypes. The exper-
iments show that the robustness of PBNs largely transfers to realistic perturbations in text
classiﬁcation tasks. PBNs with LMs enhance the text classiﬁcation robustness of LMs and
outperform state-of-the-art LLMs. PBNs work best with a medium amount of prototypes,
Transformer backbones, and Euclidean distance, and beneﬁt especially from interpretability
loss. The results of LLMs are very high on the original task but decline signiﬁcantly on the
perturbed data. While these results are encouraging, they raise a question of whether they
can bring beneﬁts also to more challenging classiﬁcation tasks such as story comprehension
and dialogue modeling.
All in all, the variety of LM adaptation methods introduced over the past few years is
encouraging and has already brought signiﬁcant advancements in terms of accuracy across
many benchmarks. Likely the most signiﬁcant advancement is the mass introduction and
usage of LLMs, which are de-facto zero- and few-shot models that can be applied to liter-
ally any textual task with little or no preparation. In that sense, they have demonstrated a

4.5 Neuro-Symbolic Reasoning 67
generalization ability that could not be even envisioned a few years ago. Meanwhile, since
these general models perform well across the board, their performance on a single task is
often not sufﬁciently reliable and varies with minor modiﬁcations in the task input. Prompt-
ing the models with few-shot demonstrations and chain-of-thought reasoning has recently
shown promise in enhancing the model’s robustness. Prototype-based networks provide an
encouraging method to enrich language models with a structural loss. Such pursuits can be
further made more reliable by applying neuro-symbolic reasoning techniques. We discuss
efforts in this direction next.
4.5 Neuro-Symbolic Reasoning
While chain-of-thought reasoning and similar methods inspired by human reasoning pro-
cesses can yield higher performance on many tasks, they do not change the fundamental
nature of large language models of black-box probabilistic engines [
268]. Without fur-
ther enhancements or integration, LLMs will inherently suffer from unfaithfulness in their
reasoning [
311], observed as a discrepancy between the model’s reasoning chain and its
downstream prediction. Multi-task prediction networks can alleviate this inconsistency to
some extent, but they still have no mechanism to enforce consistency between predictions
and reasoning chains on different granularity [
161]. Meanwhile, symbolic reasoners have
complementary strengths and weaknesses to LLMs: they can guarantee faithfulness and are
transparent by design owing to their explicit knowledge representation and well-deﬁned
inference rules following logical principles. Symbolic reasoners and representations require
a reliable grounding mechanism to map the ambiguous task inputs, e.g., in natural language,
to their discrete symbolic space.
While combining neural language models with symbolic resources and inference engines
is an intuitive pursuit, it is less obvious how to realize this combination practically in a way
that enables high effectiveness, generalizability, and robustness in the sense of faithful rea-
soning. One promising idea is that of neuro-symbolic veriﬁcation or certiﬁcation: a paradigm
where an LLM is designed to map the task input into a constrained symbolic space, and
a symbolic program is employed to reason over this structure. The ﬁnal decision would
ideally be made by this program [
268], though in some systems [ 282] a language model is
used to make the ﬁnal decision based on the symbolic inference of the reasoner. Many vari-
ants of such program-augmented methods exist, with access to information retrievers [
315],
calculators [ 57], planners [ 202], and Python programs [ 102]. To deal with more complex,
non-linear tasks, another emerging idea is to leverage logical solvers [ 268, 282].
Logic-LM, one representative neuro-symbolic certiﬁcation framework, is illustrated in
Fig. 4.5. Logic-LM decomposes a logical reasoning problem into three stages: problem
formulation, symbolic reasoning, and result interpretation. The problem formulation stage
takes an input sample and transforms it into a symbolic representation with the appropriate
entities, facts, and rules. The resulting formulation needs to follow a predeﬁned syntax (e.g.,

68 4 Robust Commonsense AI
Fig. 4.5 Logic-LM method overview. Logic-LM has three steps: problem formulation, symbolic reasoning, and result interpretation. An auxiliary step
of self-reﬁnement is used to ﬁx incorrect symbolic parses of the problem. The ﬁgure originally appears in the Logic-LM manuscript [ 268]

4.5 Neuro-Symbolic Reasoning 69
ﬁrst-order logic), which is enabled by the extensive data used to train the LLMs in the ﬁrst
place. The second step of symbolic reasoning employs a corresponding symbolic solver or
theorem prover to perform inference over the symbolic information. This step may result in
an error in cases where the symbolic parsing is syntactically incorrect, in which case, step
1 is repeated for self-reﬁnement including the error messages from the solver as part of the
LLM input. Once the symbolic reasoner can successfully perform the intended inference,
the last step performs result interpretation to explain the solver output and map it to the
correct answer in the format expected by the task.
The problem formulation step leverages LLMs for information parsing and translation of
inputs into a formal symbolic program. As LLMs have been shown to perform well on this
task, the idea in Logic-LM is to employ them in a few-shot prompting setting. The models
are instructed to produce one of four popular symbolic formalisms: (1) logic programming
for deductive reasoning, which starts from known facts and rules, and iteratively makes new
inferences until the goal statement can be proved true or false. This formalism’s grammar
consists of facts, rules, and queries; (2) ﬁrst-order logic can represent more complex problems
using formulas, divided into premises and conclusions; (3) constraint satisfaction problems,
which ﬁnd the value assignment of a set of objects that satisﬁes given constraints; and
(4) boolean satisﬁability problems, which decides whether variables can be assigned to
a Boolean formula in a way that the formula (set of constraints under a given theory) is
satisﬁed. Each of the four formalisms has a corresponding symbolic solver that can be used
on it, such as the Pyke expert system for logical programming [
98].
Logic-LM consistently enhances the performance of LLMs across ﬁve logical reason-
ing datasets, formulated as multiple-choice tasks. Curiously, while two of these datasets
also beneﬁt highly from chain-of-thought reasoning, the other three datasets note a small
improvement or a decline in performance with chain-of-thought. The problem formulator
translates the vast majority of the problems on four of these datasets into executable for-
mulations. The remaining dataset poses a challenge for the translation module, with only
11% initial execution rate and 22% execution rate post-reﬁnement. The method shows a
particularly high ability to remain robust as the size of reasoning depth increases (Fig.
4.6).
Fig. 4.6 Robustness of vanilla
LLM, LLM with CoT, and
Logic-LM to the increasing
size of reasoning depth (0–5).
The ﬁgure originally appears in
the Logic-LM manuscript [
268]


70 4 Robust Commonsense AI
Namely, while the vanilla and the CoT baselines note a drop in performance of around
25% when ranging from paths of length 0 to 5, Logic-LM’s performance decreases by only
10%. At the same time, the trend for Logic-LM is also monotonically decreasing, inspiring
possibilities for future work. The deeper analysis of the model’s errors shows that the LLM
sometimes struggles to maintain an overarching and consistent understanding of the prob-
lem when forming logical symbols. For example, it generates WildTurkey(eastern) instead
of EasternWildTurkey, which does not connect well with the other constants in the symbolic
formulation.
A limitation of existing neuro-symbolic veriﬁcation methods is that they are currently
applied to relatively simple reasoning tasks, where the knowledge components are explic-
itly given and result in relatively simple non-ambiguous rules. An important future direc-
tion is to develop methods that are more ﬂexible and powerful, based on methods such as
Markov logic networks and probabilistic soft logic, which can reason under uncertainty
more robustly. Such extensions may enable methods like Logic-LM to apply to a wide range
of commonsense reasoning tasks. Another subtle, yet critical, consideration is the difference
between executable and correct symbolic solvers, as the programs may be syntactically valid
without capturing the input formulation precisely. This challenge is manifested by models
having high precision and low recall of detecting inconsistencies in the logical chains.
4.6 Knowledge Transfer Via Analogical Abstraction
Drawing analogies is a core cognitive skill of humans [ 140, 275], deﬁned as the ability
to perceive and utilize the similarities between situations or events based on (systems of)
relations rather than surface similarities [
108, 141]. The dichotomy between relational and
surface similarity is illustrated in Fig. 4.7 for analogies between stories. Here, the narratives
. Q and . N overlap in terms of characters, locations, and actions (surface similarity), but do
not create a system of relational correspondences as shown by their proverbs [ 329]. We say
that. Q and. N are thus disanalogous. Meanwhile, . Q and. A are dissimilar on the surface, yet,
they form a coherent relational system of correspondences, summarized through the proverb
no pain, no gain . We say that . Q and . A form an analogy. Both analogies and disanalogies
can be near (same domain) or far (different domains) [ 105].
As a core cognitive process, analogy enables creative inferences and generalization of
knowledge. People apply analogies to solve problems and innovate, by transferring knowl-
edge from one domain to another. This form of knowledge transfer is also expected to make
machines more robust and generalizable, akin to humans, and has thus received signiﬁcant
attention in cognitive science, AI, and NLP . Cognitive frameworks study human analog-
ical behaviors and seek to transfer them to machines. Such framework is the Structural
mapping theory [
105], which deﬁnes domains and situations as systems of object attributes
and relations. Another framework by Holyoak and Thagard [ 143] distinguishes between
attribute, relational, and system mappings. The implementations of these frameworks are

4.6 Knowledge Transfer Via Analogical Abstraction 71
Fig. 4.7 Analogical reasoning
over narratives (. ARN )[ 329]: a
binary task of distinguishing
between analogous narrative . A
and distractor .N for the query
narrative. Q. Here, . A represents
a far analogous narrative
(forming a relational system
mapping) to
. Q, while .N is a
near disanalogy (having only
surface similarities)
usually very expressive, yet their generalizability to novel inputs is limited [ 153]. Most
of the analogy work in NLP so far has focused on so-called proportional analogies of the
form (
. A : B :: C : D)–a task where word pairs need to be matched or completed to form a
relational or attribute analogy [ 64, 101, 116, 166, 179, 234–236, 353, 354]. For example,
given. Happy : Sad :: C : D, the task can be to infer the missing . Angry : Calm or .Calm
given. Happy : Sad :: Angry : D. More recent work on analogical reasoning has attempted
to scale cognitive theories by designing structural matching engines that can be applied to
arbitrary entities [
153] and by designing large-scale analogical tasks for narratives [ 162,
329, 387].
How would a cognitively-inspired AI framework for transferring knowledge across tex-
tual documents be designed? In [ 254], the framework consists of six dimensions for drawing
analogies between fables, namely: shallow attribute analogy (matching between physical
attributes, such as brown(fox)–brown (deer)), deep attribute analogy (matching between
abstract attributes, e.g., naive(ass)–naive(deer)), relational analogy (same ﬁrst-order rela-
tionships, e.g., friends(fox, deer)–friends(conman, countryman)), event analogy (both sto-
ries involve the same event frame, e.g., danger), structural analogy (two or more causally
connected events coincide, e.g., chase(merchant, ass) & run(ass) & cause(chase, run)–
chase(tiger, rabbit) & run(rabbit) & cause(chase, run)), and moral/purpose (two fables have
the same moral, e.g., “know thyself”). StoryAnalogy [
162] proposes to derive story-level
analogies from LLMs, expressed as a single decimal score between 0 and 1. In ARN [ 329],
the realization is carried out in three compositional steps following a bottom-up approach:
extraction of elements of narratives, formation of surface and system mappings, and task

72 4 Robust Commonsense AI
formulation. The elements covered in ARN are driven by narratology research [ 221, 363]:
characters, relationships, character actions, character goals, location, and proverbial mes-
sages. The ﬁrst ﬁve elements form surface mappings, whereas system mappings are only
expressed through proverbs.
Despite the different formulations of the analogy task, their analysis of state-of-the-art
LLMs tends to reach similar conclusions: LLMs can detect relational analogical patterns
when these are in the same domain, i.e., the narratives have a signiﬁcant surface similarity
besides systematic alignment [
329, 387]. However, the analogical transfer for far analogies
is much more challenging, with models performing at random on average [ 329]. Chain-
of-thought prompting and multiple demonstrations enable these models to abstract better,
however, the gap in human performance is still halfway from random. Providing far or
near demonstrations does not have a clear impact on the model’s generalization ability: the
performance tends to increase on far analogies, and decrease on near analogies, showing a
lack of robustness of these models.
How could one, build robust analogical models? A promising start towards this pursuit
is the FAME framework [ 153], which provides a mechanism to match incomplete sets of
entities. FAME employs language modeling and commonsense information to ﬁll knowledge
gaps and to suggest missing entities whose inclusion would make the analogy more complete.
Given a set of entities for a source domain: {sun, planet, gravity, newton} and target domain:
{nucleus, electron, electric ﬁeld, faraday}, this approach can align sun to nucleus, planet
to electron, gravity to electric ﬁeld, and newton to faraday. It can derive relations such
as revolve around, which holds between sun and planet, as well as between nucleus and
electron. FAME can also group relations that refer to the same activity in a given context,
such as revolve around, rotate around, and orbit. Its performance on near, far, and extended
(unseen) proportional analogies is more robust than that of GPT-3.5. While this work so
far has been applied to pre-speciﬁed sets of entities, there is an opening to apply this idea
to natural documents (e.g., narratives) in line with the ARN framework. Namely, entities
and their relations may be extracted from these documents, forming an initial graph as a
story representation. Then a method akin to FAME can be applied to discover connections
between the graphs of two stories and judge the analogical match based on the strength
and completeness of these connections. Alternatively, following the idea of neuro-symbolic
veriﬁcation, the created graphs can be fed into a soft logical reasoning engine [
177], which
would output a probability that the graphs are aligned.
A parallel line of investigation is exploring whether analogical skills can be transferred
through in-context LLM learning from one dataset (e.g., ARN) to another dataset that
requires analogical matching of stories (e.g., StoryAnalogy) or abstraction in a broader
sense (e.g., the BrainTeaser dataset with lateral thinking puzzles [
160]). Our initial inves-
tigations indicate that carefully designed far analogies may be effective as demonstrations
to prompt the abstraction ability of LLMs on other abstraction tasks, however, providing an
automated mechanism to detect such analogical transfer is currently lacking. In the case that
these ﬁndings generalize across datasets, a promising next step would be to integrate such

4.7 Summary and Discussion 73
analogy-aware in-context LLM prompting methods with structural representations within
neuro-symbolic frameworks.
4.7 Summary and Discussion
This chapter started with the premise that language models are general AI interfaces that
can perform well (much better than random) on many unseen tasks, assuming that the
models are chosen to ﬁt the needs of the task. This assumption holds despite many of the
downstream tasks of interest having complexity that goes well beyond the tasks of word or
sentence prediction that these models were initially trained on. However, their robustness
is often fragile and their performance on many tasks is far from perfect, requiring further
adaptation. The models can be applied to these tasks in a zero-shot manner or possibly
ﬁne-tuned by using benchmark-speciﬁc data, when this is available, to improve the ability
of the model to approximate a notion of reasoning.
As shown in this chapter, the approximation to reasoning of these models can be improved
in a variety of ways: by employing independently created repositories of knowledge, such
as knowledge graphs; by including another language model with particular properties; by
devising strategies for in-context reasoning with step-by-step guidance, such as chain of
thought, or strategies that adapt the model while preserving its original weights, such as
preﬁx-tuning; by neuro-symbolic integration between language models and symbolic inter-
preters of programming languages or logic; and by enabling language models to perform
relational reasoning via analogy . By careful data engineering, method design, and align-
ment with cognitive and linguistic principles, these approaches have led to advancements in
terms of the robust use of language models on a variety of tasks.
Y et, the reasoning of language models remains limited to such an approximation .D a t a
augmentation does not modify their reasoning ability, it rather shifts the kind of pattern
matching these models perform. Similarly, prompting and adaptation strategies that may
use this data empirically show higher effectiveness, but have little theoretical support or
general principles for robust use across tasks. Integration with symbolic interpreters or the
development of analogical engines may provide a robust umbrella around these models,
however, the practical realization of such a framework is hindered by noise in the alignment
between language models and symbolic components.
A promising path forward may be via a combination of these ideas for achieving robust-
ness. Data augmentation and knowledge engineering are important to ensure that the mod-
els learn from high-quality data, where quality would include considerations of objectivity,
diversity, and granularity. Further innovation in approaches for automatic prompt discovery
and faithful step-by-step reasoning will enable a more principled application of these models
to novel tasks and will support reproducibility. Neuro-symbolic principles may help with
these goals, especially if the alignment between the symbolic and the language model space
can be facilitated in a fundamentally workable way. Analogical abstraction through relational

74 4 Robust Commonsense AI
patterns may be useful for each of these pursuits: it can support more efﬁcient exploitation
of less data, it can enable model prompting to be more effective based on higher-order
similarities, and it can play a key role in connecting neural and symbolic representations.
Thus, a key future direction is to devise neuro-symbolic architectures that leverage lan-
guage models through few-shot prompting with analogical samples and are adapted using
high-quality augmentation processes . Such a general approach would provide a framework
of different prompting strategies, neuro-symbolic architectures, analogical implementations,
and data engineering processes, allowing for a study of the interplay between these compo-
nents and their compounded impact on the aspect of robustness. Supplementing the method
development, it is equally essential to devise evaluation datasets and environments that can
reliably assess robustness from the full set of relevant aspects that constitute this term,
including considerations of distribution shift, noise, and consistency of reasoning. Signiﬁ-
cant advancements in each of these aspects have been made: by shifting to zero-, few-shot,
and transfer learning evaluation settings; by developing large-scale mega-benchmarks test-
ing a wide range of skills [
138, 370] and sensitivity to noises on character-, word-, and
sentence-level [ 246]; and by evaluating the ability of models to answer the same question
posed in alternative ways or the same reasoning chain with different actors [ 160, 412].

5Responsible Commonsense AI
Abstract
AI is technology with high impact potential on individuals, groups, and societies. Its
harmful uses are growing at a similar rate compared to its positive applications, making
the responsible use of AI a societal imperative. Yet, considerations of morality, ethics,
and bias remain hotly debated even for humans making their incorporation into AI non-
trivial. Specifying norms detached from context is well understood, but the application of
these norms in real-world contexts brings complexity. Indeed, developing AI that behaves
responsibly in novel contexts has been extremely challenging, and attempts to do so have
resulted in models exhibiting strong biases, and unethical behavior. This chapter reviews
ongoing efforts to test and improve the models’ ability to perform moral reasoning in
sensitive situations, and to measure and mitigate model biases against groups deﬁned in
terms of ethnicity, gender, and profession. A key ﬁnding is that the model biases highly
correlate with biases in the data and that training with large-scale morally curated data
leads to models that perform better on morality tasks. At the same time, these models
are still trained to directly infer patterns from large datasets with minimal guidance–thus,
it is expected that they will propagate any human biases that will be inevitably present
in the data. The chapter concludes with a set of open challenges that stem from the
dominant data-driven learning paradigm, such as consistency, representation fairness,
and compositionality. To mitigate these challenges, the chapter suggests two key future
directions of incorporating neural and symbolic (bottom-up and top-down) methods and
devising comprehensive frameworks through collaborations with other disciplines.
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_5
75

76 5 Responsible Commonsense AI
5.1 Background and Challenges
AI is technology with high impact on individuals, groups, and societies. Its harmful uses are
growing at a similar rate compared to its positive applications, making the responsible use of
AI a societal imperative [ 89]. Yet, considerations of morality, ethics, and bias remain hotly
debated even for humans making their incorporation into AI non-trivial. So, despite lacking
an explicit notion of morality, ethics, and bias, or their underlying norms, AI models are
now publicly available and easily accessible for anyone with internet access through user-
friendly interfaces. Owing to their ability to generate an answer to any query, AI models
are constantly helping many people to make decisions loaded with moral implications and
standpoints that may impact millions [
157].
While it has been long discussed whether morality should be taught to AI, the ongoing
wide adoption of AI makes it critical to ﬁnd mechanisms to limit or qualify biases in current
models, and align AI to human values, norms, and morals [
223, 298]. AI models are generally
trained to deduce associative patterns between terms based on many billions of tokens,
without a plan on what should or should not be learned. Recent manifestations of AI models
learning to be racist or sexist [
362] have led to efforts to incorporate guardrails, as illustrated
by the latest GPT models’ frequent refusal to answer potentially sensitive questions. Yet,
both GPT-3.5 and GPT4 can be tricked into answering sensitive questions, exhibiting severe
toxicity (e.g., towards people kneeling during the American national anthem), stereotypes
(e.g., claiming that young people have HIV), and ethics (e.g., indicating that harming oneself
is not immoral) [
369]. Such cases reveal that the current models have fragile railguards,
which, when bypassed, lead to uncontrolled and irresponsible behavior.
To understand the extent and impact of these challenges, researchers have devised datasets
that measure whether AI models can perform commonsense moral reasoning in novel situa-
tions. Indeed, general norms are straightforward to state in logical terms, it is their application
to real-world contexts that is nuanced and complex [
382]. Here, a computational task may
be deﬁned as providing or selecting the most moral answer, or as providing the moral answer
from a particular perspective, for instance, aligned with the Moral Foundations Theory [
123]
or cultural pressure. Subsequently, such rich datasets have been leveraged to train or adapt
neural models to reason more in line with responsible requirements. As accuracy scores
improve, even the best models show worrisome biases towards various kinds of popula-
tions, deﬁned by socio-economic status, profession, and religion. Ongoing investigations
try to estimate to what extent those biases come from the data, and how much they are
ampliﬁed by the learning algorithm.
Given the importance of responsible commonsense AI, this chapter is dedicated to div-
ing into these challenges and describing recent efforts to address them. First, we describe
research that investigates and improves the extent to which AI can comprehend morality,
ethics, and the underlying norms. Next, we discuss ongoing research for measuring and miti-
gating bias in language models and large-scale resources. Notably, computational efforts for
building more responsible AI increasingly make an effort to: (1) incorporate the rich set of

5.2 AI Morality 77
theoretical work from ethics and moral psychology, and (2) combine top-down and bottom-
up approaches to responsible AI. At the conclusion of this chapter, we discuss these two
research directions and their role in addressing the most thorny challenges with responsible
AI today.
Thus, this chapter covers multiple dimensions, including moral reasoning, bias measure-
ment and mitigation, and cultural representation, offering a broad perspective of the chal-
lenges and opportunities of responsible AI. At the same time, responsible AI also involves
considerations of regulatory and governance frameworks, which are not explored in detail
in this chapter.
5.2 AI Morality
Morality in philosophy is considered from two perspectives: top-down, as a set of objective
principles that can exist apriori without empirical grounding [
169], and bottom-up, as an
emerging expression of biological and social human needs, driven by contexts like time
and culture [
325]. The Delphi framework [ 157] dominantly follows a bottom-up approach
that is descriptive and example-based, for two main reasons. First, mainstream AI today,
such as LLMs and deep learning techniques, cannot comprehend and follow high-level
directives. Second, society has not yet reached a consensus on the general principles of
morality. However, the authors recognize that the bottom-up framework suffers from the
same challenges that LLMs do, in learning implicit signals directly from data. In other
words, the models are susceptible to learning systemic prejudices and pervasive biases from
Fig. 5.1 The theoretical a and computational b frameworks of Delphi [ 157]

78 5 Responsible Commonsense AI
the data authors [ 157, 368]. Thus, Delphi also provides an initial attempt to complement the
bottom-up method with top-down guidance, inspired by the philosophical work AT h e o r yo f
Justice by John Rawls [ 292]. By doing so, Delphi’s aspiration towards a so-called “reﬂective
equilibrium” is well-aligned with modern moral philosophy. Figure 5.1 shows an overview
of the Delphi framework.
Delphi compiles a new dataset called Commonsense Norm Bank with 1.7M examples of
descriptive judgments on everyday situations. These examples are adapted from four prior
datasets, enriched with further augmentation to enable generalization to declarative norms
and variations in phrasing:
 Social Chemistry [ 91], a large corpus that formalizes ethical judgments and social norms
of common situations in natural language. It aims to capture social norms through deﬁning
rules-of-thumb (RoTs) : unspoken commonsense rules about acceptable social behavior in
a situation, consisting of a judgment and an action. For example, the judgment “it is rude”
can be applied to the action “running the blender at 5am”. Each RoT is then categorized
into 12 ethical judgment attributes, motivated by social science theories about ethical
judgments, moral foundation categories [
123], cultural pressure, and legality. Moreover,
the corpus identiﬁes relevant characters in the situation. An excerpt of the dimensions
in Social Chemistry is shown in Fig.
5.2. This corpus has been created by English-
speaking crowd workers in the United States and contains 292 k RoTs over 104 k everyday
situations.
 ETHICS [ 139] is a benchmark for predicting ethical judgments on everyday situa-
tions. Delphi’s Norm Bank incorporates the commonsense morality subsection from this
dataset, which contains scenarios where a character describes short and long scenarios
from everyday life. Unlike Social Chemistry, its situations and actions are chosen to be
unambiguous and non-divisive.
 Moral Stories [ 84] contains narratives for grounded and goal-oriented moral reasoning.
Each sentence in these stories is either a norm, a situation, an intention, a moral/immoral
action (aligned with the intention), and its moral/immoral consequence. This dataset is
converted in Norm Bank into a task of classifying whether an action is morally good or
bad in a given situation.
 Social Bias Inference Corpus [ 302] scaffolds social and demographic biases into vari-
ous categories including offensiveness, intent to offend, lewd, group implications, tar-
geted group, implied statement, and in-group language. This corpus aims to measure
and alleviate stereotypes towards social and demographic groups that are conventionally
underrepresented or marginalized.
Delphi uses the Norm Bank data to ﬁne-tune the Unicorn language model [ 209], which
is derived in turn from ﬁne-tuning the largest T5 model with 11 billion parameters [ 290].
This Delphi model is compared to GPT-3 prompted in a zero-shot and few-shot fashion,
and it performs better on the test subset of the Norm Bank dataset. A key aspect of morality

5.2 AI Morality 79
Fig. 5.2 Rules-of-thumb from social chemistry [ 91], shown in colored tubes. RoTs capture social
expectations for a situation (shown in the central hexagon). Rather than prescribing a single moral
judgment, RoTs provide a multitude of judgments from a variety of perspectives including moral
foundations, legality, and cultural pressure
is the ability to generalize to novel contexts, as moral judgments are defeasible with the
availability of additional context. Delphi’s model is shown to generalize well to a manually
curated set of 259 situations. For example, it seems to understand defeasible variants of
speaking loud in the library–being rude without further context, being okay if it is no longer
in use, and being rude if you are mad at the librarian for no reason (Fig.
5.3).
While Delphi retains strong performance on variations similar to its dataset, it struggles to
provide consistent moral judgments for situations derived from the Universal Declaration of
Human Rights. The model has strong biases against less privileged socio-economic identities
(e.g., poor, homeless, lower-class) and people from regions of current-day conﬂict (e.g.,
people from North Korea and the Middle East). Such biases and inconsistencies reﬂect, and

80 5 Responsible Commonsense AI
possibly emphasize, the properties of the training data. Models that solely rely on learning
from data will be inherently neural snapshots of the data and will over-rely on historical data
to shape the future [ 157].
Fig. 5.3 The Delphi model showing defeasible reasoning skills on the Commonsense Norm Bank.
The label colors show the morality class: green=positive, gray=neutral, and red=negative
As the training data will never be perfectly balanced, the solution to this challenge must
be sought beyond purely data-driven approaches, possibly among top-down strategies. An
initial step in this direction is provided by Jiang et al. [ 157], who collect potentially incorrect
and biased model judgments, and ask crowdworkers to ﬁx any mistakes, before using them
to further tune the model. While this amendment decreases the model bias towards the
categories in question, performing similar patchwork for every biased aspect is unfeasible

5.3 Bias in Resources and Models 81
and may negatively affect the existing information stored in the model parameters. Another
strategy to deal with inconsistent behavior is to introduce a family of decoding algorithms that
rely on expert models to facilitate constraint satisfaction [
84]. Such methods can be promising
as they provide an opening for symbolic grounding and explicit reasoning. Meanwhile,
there have been orthogonal efforts that are based on logical methods [
39] and constraint
programming [ 299].
While this section primarily describes the Delphi framework, many other frameworks
for measuring and enhancing AI morality have been introduced, including the datasets
Square [
186], with sensitive (contentious, ethical, and predictive) questions and acceptable
answers in Korean, and Scruples [ 210], about ﬁnding the person that breaks an ethical norm
in a situation, together with a metric for estimating moral ambiguity. Across these different
frameworks with their models and data procedures, there are several recurring challenges,
namely: (1) lack of cultural awareness , as the models focus primarily on the moral compass
and social expectations in the United States in the 21st century, with no mechanisms to reason
about different spatiotemporal contexts; (2) inconsistency of predictions , as the models have
no mechanism to enforce consistencies or generalize logically, causing them to predict
that practicing drums is acceptable at 12:15 pm but rude at 12:30 pm; (3) struggles with
compositionally in language , especially metaphorical and idiomatic language, e.g., Delphi
predicts that telling someone to break a leg is rude, failing to grasp the idiom; and (4)
struggles with anticipating action outcomes, which is essential for infering salient behavioral
norms [
84, 157].
5.3 Bias in Resources and Models
While the term “common sense” seems to imply a set of objective knowledge, in prac-
tice, commonsense sources and models term may cover beliefs shared by a subset of the
overall population. For instance, commonsense knowledge bases that are dominantly used
in research today have been human-generated, often by highly educated individuals from
English-speaking Western countries [
303, 331]. One potential danger with this approach
is that the source of truth, being it crowd workers or writers of the texts that are included
in a corpus, tend to conﬂate their own beliefs and prejudices with the notion of common
sense [
229]. These sources and models may contain biases targeted at particular populations,
e.g., in terms of their origin, gender, religion, and profession [ 230]. Such biased beliefs are
called representational harms, referring to how certain target social groups are perceived in
the context of commonsense knowledge bases [ 23].
A selection of representational harms found in two popular knowledge bases, ConceptNet
and GenericsKB, and the COMET knowledge model, are shown in Table 5.1.
This situation motivated studies that seek to quantify the presence and types of biases
in the knowledge bases and in the models that may leverage these resources. Mehrabi et

82 5 Responsible Commonsense AI
Table 5.1 Example bias
statements from popular
knowledge graphs and
neural knowledge models.
Examples come from [
229,
230]
Source Example
ConceptNet (church, used for, brain washing)
(lady, used for, fxxk)
GenericsKB Chinese people are very reclusive
group of people.
Lawyers are registered menace to
society.
COMET (Muslim, causes, terrorism)
(man, deﬁned as, as being in charge in
society)
al. [229] analyze the representational harms in knowledge sources and models that use them.
The authors deﬁne two types of representational harms in commonsense KGs:
1. Intra-target overgeneralization is a phenomenon of unfairly attributing a polarized char-
acteristic to all members of a group, e.g., “lawyers are dishonest”. Overgeneralization
includes categories such as stereotyping, favoritism, and denigration. To detect over-
generalized statements, one possibility is to transform them into natural language and
use sentiment polarity and regard tools. Using such approximation of overgeneralization
through sentiment and regard has been shown to be effective [
229, 314]. To estimate the
positive/negative overgeneralization bias towards a target, Mehrabi et al. multiply the
number of statements with a positive/negative sentiment and regard.
2. An inter-target disparity occurs when targets have different coverage in terms of the
number of statements and perception towards them. For instance, Persian people may be
described with much less information than British people, and Islam may be portrayed
more negatively than Christianity. In computational terms, the disparity can be quantiﬁed
as the difference between the perception of a target compared to other targets in the same
set.
For the four categories of origin (extended from race), gender, religion, and profession,
Nadeem et al. [ 253] extract 321 targets in total, extended to 329 by Mehrabi et al. [ 229]. For
these targets, Mehrabi et al. extract over 100,000 statements, formalized as head-predicate-
tail triples, from ConceptNet and over 30,000 statements in natural language from Gener-
icsKB. The analysis of the overgeneralization of these statements indicates clear favoritism
towards certain professions (e.g., the profession of a CEO), clear prejudice against others
(e.g., politicians), and a mix of strong positive and negative regard for yet others (e.g., psy-
chologists). Similarly, for religion, the Sharia religion is constantly regarded as negative,
while the bible and Mohammed have primarily positive regard in both knowledge resources.

5.3 Bias in Resources and Models 83
In terms of disparity, different targets have largely different coverage, e.g., hairdresser infor-
mation is much more scarce compared to information about scientists.
What is the implication of such biases present in the knowledge sources? One way
to answer this question is by investigating the performance of commonsense knowledge
models [
37, 230], i.e., generative language models adapted over commonsense knowledge
sources to perform the task of knowledge base completion. While these models do not
directly have a challenge with disparity (as they provide an equal number of statements
for each target), they still struggle with both overgeneralization and disparity in terms of
polarity. Looking closer into the comparison of different knowledge models, Melotte et
al. [
230] ﬁnd that: (1) all models have a stronger negative, compared to positive, regard;
(2) larger models are generally more nuanced than smaller models, though exceptions exist;
(3) training on larger sets of commonsense knowledge causes a higher disparity; and (4)
the outliers in terms of professions are largely shared across all models (e.g., “prosecutor”
has highly negative regard, and teacher has very positive regard), whereas the outliers in
terms of countries of origin differ, “with T5-base being surprisingly biased towards white
people” [
230].
Going beyond static resources and ﬁne-tuned language models on commonsense sources,
we note that the bias in current SotA LLMs is an ongoing investigation. A curious behavior
of these models is their tendency to avoid replying to questions that may result in biased
answers. At the same time, no model is entirely neutral, and, by learning from very extensive
and possibly not well-curated sources of data, these models still show biases. For instance,
political tests originally created for humans have demonstrated repeatedly that ChatGPT is
a left-leaning model in terms of its political beliefs [
293].
Such biases in models can be mitigated in a variety of ways. One possibility is to pre-
process the data by ﬁltering statements that contribute to high regard and sentiment towards
certain targets. By increasing the overall sentiment and regard in the dataset, the models
trained on this data have a reduced rate of overgeneralization and disparity. However, a
downside of this strategy is that a substantial portion of the relevant information is also lost,
leading to a 7% absolute decrease in generation quality in [
229]. Bias can also be mitigated
by modifying the embeddings learned as token representation by models [ 34]. The key
idea in this line of work is to detect undesired associations between tokens and modify the
embeddings to remove harmful associations. For a more comprehensive discussion of the
aspect of fairness of models, the reader can refer to recent surveys [ 33, 228, 337].
Besides removing the biased statements from the input data or decreasing their impact
by modifying the learned representation, a third option is to preserve potentially biased
statements and qualify them using a set of extra information. Such approach can be inspired
by DICE [
46], which qualiﬁes existing commonsense statements with their plausibility
(whether a statement makes sense at all), typicality (whether a statement holds for most
instances of a class), remarkability (to what extent is a statement distinguishing a concept
from other similar concepts), and saliency (to what extent a statement is characteristic for a
concept). While DICE is currently not meant to qualify information in terms of perspectives,

84 5 Responsible Commonsense AI
it provides a framework that can be extended with qualiﬁers for cultural perspectives and
estimations of positive or negative bias. A complementary line of work acknowledges the
role of culture in commonsense knowledge for narrower domains [
2, 319]. Most recently,
Nguyen et al. [ 259] extract a set of statements for a concept from the perspective of a given
culture, by using an LLM (GPT3.5). For example, a statement can indicate that in Japanese
culture, chopsticks are common eating utensils and tipping is not common.
5.4 Summary and Discussion
While LLMs, and broadly AI, create a signiﬁcant societal value that can be channeled into
a long list of applications, the set of harmful uses with their corresponding intents is also
becoming more serious. Due to their growing potential for societal harm, the quest towards
inclusive, ethical, and socially aware AI systems is gaining urgency [
89, 157]. Machines
with a moral sense should share the basic human understanding of societal norms and have
a reasonable understanding and consistency when applying those norms in given situations.
Thanks to efforts in AI dealing with the matters of morality, ethics, bias, and fairness,
as of today, there are curated resources for studying the morality of AI models in divisive
and non-divisive settings . There exist both resources that ask models to provide the morally
righteous answer, and resources that qualify the answer through a set of norms associated
with a variety of perspectives. While both of these are very useful for testing and training
models, the latter multi-perspective approach seems to be better aligned with theories in
psychology and philosophy. Experiments with LLMs on these resources show that even
relatively small models can perform well on seemingly complex situational constructs from
the in-domain corpus. These same models, however, perform much worse on other morality
tasks, such as generalizing the basic societal principle that everyone should be given similar
rights. Such biases target populations of lower socio-economic status and nations that are
currently in conﬂict. They also favor certain professions, genders, and religious groups, while
discriminating strongly against others (e.g., lawyers, females, Sharia). Not surprisingly, such
biases are not only present in the models but they are also shared in the knowledge resources
often used to adapt those models.
The paper by Jiang et al. [ 157] describing the Delphi framework, dating from 2022,
provides a set of limitations of current models that are largely still relevant today because
they are merely symptoms of the underlying challenges with the way these models learn,
represent information, and perform inference. Models have a strong cultural representation
of certain perspectives, e.g., the USA in the 21st century, at the expense of a limited cul-
tural awareness of other countries and historical periods . As LLMs essentially “blend” the
data patterns that they observe into model weights, they have no representation of different
cultural perspectives, and cannot explicitly manipulate such expectations (e.g., understand

5.4 Summary and Discussion 85
when to generalize the cultural norms across neighboring countries). Second, these models
lack consistency (e.g., providing different answers for unimportant variations of time) and
struggle with compositionality (e.g., justifying a wrong action when supplied by a context
of irrelevant positive actions) . The challenge of compositionality is also prominent when
some of the components require understanding ﬁgurative speech, such as metaphors and
idioms. Being able to make progress toward consistency is hindered by the lack of abstract
representations that can enable reasoning over the implications of actions and their connec-
tion to relevant societal norms. A third challenge lies in the acquired biases, manifested as
favoritism towards certain groups or prejudice against others . This is perhaps best mani-
fested through the inability of the Delphi model to allow different groups the same human
rights.
While a lot of important work is left to be done in the area of responsible commonsense
AI, two key directions emerge from the identiﬁed model drawbacks. First, there is a need for
systematic frameworks that go beyond current work to align descriptive with prescriptive
morality, different judgment perspectives, and a representative set of scenarios and target
groups. Social Chemistry’s [
91] moral judgment from 12 perspectives and Delphi’s [ 157]
vision for integrating bottom-up and top-down morality together with a corpus of over one
million situations, provide strong bases for such systematic frameworks to be designed and
implemented. A key next step is to ﬁll in the representativeness gaps in these datasets and
to include a comprehensive set of perspectives. For this purpose, a key ingredient is cross-
disciplinary collaboration with experts from behavioral psychology and moral philosophy.
Second, the challenges of consistency, understanding the implications of actions, and
cultural biases, point to the need for abstraction and symbolic reasoning , which is central to
this book. No matter how high the accuracy of the model is, it cannot be considered respon-
sible if it affords different rights to Germans and Palestinians, or lawyers and scientists.
While descriptive, bottom-up methods driven by data bring beneﬁts in terms of high overall
performance, they need to be complemented with top-down methods driven by symbolic
reasoning. The key to unlocking this challenge will likely come from algorithmic develop-
ment broadly in the AI world, to the beneﬁt of developing more responsible AI, which is
more ethical, inclusive, and socially aware.

6Human-Centric AI in Complex Scenarios
Abstract
Artiﬁcial intelligence promises to augment people by combining two goals: automation
and collaboration with people. Human-AI partnerships can make a signiﬁcant impact on
complex tasks that are more ambiguously structured, effectively or actually unbounded,
involve large amounts of data, and cannot be solved analytically in polynomial time. Its
realization in practice is in an early stage, as the strengths and weaknesses of AI are still
heavily studied, model development is in ﬂux, and AI may lack explainable, collabo-
rative, adaptive, and responsible teaming mechanisms. This chapter considers the need,
current approaches, and standing challenges of human-centric AI in four critical domains
with many complex tasks: content safety, education, trafﬁc understanding, and robotics.
In the domain of content safety, we review state-of-the-art commonsense technology
that can facilitate a deep understanding of malicious undertones in internet memes and
fallacious arguments, to deal with phenomena of hate speech and misinformation. In
education, we describe methods for personalizing materials to users through analogical
recommendations and tutoring systems that can guide human understanding over time.
In trafﬁc monitoring, we review complex reasoning tasks, such as counterfactual rea-
soning, to understand the causes, implications, and possible ways to avoid trafﬁc events.
In robotics, we describe a recent framework for robot manipulation tasks that consoli-
dates visual reasoning, object manipulation, and constraint satisfaction. We conclude the
chapter with a summary of the lessons learned, standing challenges, and possible future
directions for these and other domains.
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_6
87

88 6 Human-Centric AI in Complex Scenarios
6.1 Human-Centric AI for Hybrid Intelligence
Humans tend to optimize for the time allocated in our lives [ 252]. Sciences have taught
us how to avoid distractions, how to balance between work and leisure, and how to even
leverage sleep productively by applying the Zeigarnik effect. However, there are limits to
our efﬁciency, given the twenty-four-hour limit and the approximate eight hours of it that are
dedicated to sleeping. Two ways to get more than twenty-four hours in a day are automation
and collaboration. Automation enables us to supplement what we do with machines, thus
multiplying our time by harnessing energy to do work for us. A key historical milestone is the
invention of the synthetic ammonia fertilizer that led to the Green Revolution in agriculture,
without which an estimated half of the people on the planet today would not be alive [
324].
Today we are facing a new automation: artiﬁcial intelligence is gradually entering our lives
and impacting the way we perform our activities in our daily lives. Besides automation,
humans also leverage cooperation to extend their time. Namely, we have learned that we
can engineer better products, write better books, and build better companies by working
together with others in synergistic ways. By combining our expertise, we can pass on to
our collaborators the tasks they can do faster or better than us, enabling us to focus on our
competitive advantage.
Artiﬁcial intelligence today promises automation and collaboration: it does not only
provide a manner to automate repetitive tasks with high precision, but it can also collaborate
with us to perform more complex tasks effectively or efﬁciently [
232]. Concerning human-
AI collaboration, there are three extreme positions, best summarized as three myths: (1)
AI will make humans obsolete; (2) human skills are unique and cannot be automated;
and (3) integrating AI is easy. Metcalfe et al. argue that human-AI partnerships are not
only possible, but necessary, to make progress on tasks that involve challenges like time,
information certainty, and complexity. This is because complex domains and tasks remain
poorly understood and difﬁcult to solve by either humans or AI separately.
Many domains and tasks are expected to beneﬁt from hybrid intelligence teams of humans
and AI agents. The wide usage of ChatGPT and DallE as assistants for both work-related
and entertainment goals shows that humans have a wide set of use cases that can beneﬁt
from assistive and partnering technology. At the same time, the current workﬂows require
signiﬁcant supervision and proactive behavior from humans, with AI in the role of ﬁlling
speciﬁc gaps the person asks for. In addition, given the challenges illustrated in the previous
four chapters, AI’s struggle with explainability, collaboration, robustness, and responsibility
makes it prohibitive for many sensitive use cases.
This chapter focuses on the role of state-of-the-art human-centric AI in hybrid intelligence
scenarios. The four principles of explainable, collaborative, robust, and responsible AI can
intuitively make such teaming more reliable, interactive, and trustworthy. But, is that really
the case, and to which extent? What are some exemplar methods and applications that have
been attempted, and how do these fare in practice? What are the strengths and weaknesses in
the lab, and would those transfer to real-world settings? This chapter provides insights into

6.2 Domain 1: Assisting Moderation for Online Content Safety 89
these questions, by showing example applications of commonsense reasoning in four critical
domains involving many complex tasks: content safety, education, trafﬁc, and robotics.
6.2 Domain 1: Assisting Moderation for Online Content Safety
The wide adoption of the World Wide Web enabled a free exchange of large amounts of
information, including an easy spread of misinformation [
8, 379, 391] and propaganda [ 24,
65, 128]. Online platforms for communication have been weaponized in a variety of geo-
political events and social issues [ 48, 261, 278, 279]. Misinformation and propaganda are
thorny issues for social media platforms on the Web and have been increasingly addressed
through the growing teams of moderators [
100, 247], and are under the scrutiny of different
organizations and governmental bodies, such as the UN [ 174]. Similarly, the EU plans to
ratify addressing misinformation as part of the Digital Services Act [ 60], as the spread of
harmful and incorrect arguments can sway the population and lead to political shifts and
civil unrest [
185].
The scale and complexity of critical, multimedia, and creative content, expressed in
formats like arguments and internet memes, make content moderation even more difﬁcult.
The inaccurate classiﬁcation of content as offensive or misinformation can lead to inadequate
moderation interventions (removal, ﬂagging, demotion, etc.) that, combined with the lack of
tracking mechanisms across platforms, has the potential to further decrease public trust in
social media platforms and related moderation policies. Content moderation policies, or the
lack thereof, can have serious implications on individuals, groups, and society as a whole.
On the one hand, content moderators may react late, inconsistently, or unfairly, thus angering
users [
129], as well as contributing to reinforcing and exacerbating conspiratorial narratives
[48, 211]. On the other hand, minimal content moderation may permit coordinated inﬂuence
operations [ 81] or enable the spontaneous formation of toxic and dangerous communities,
e.g., the study by [ 220] demonstrates how “the Manosphere”, a conglomerate of men-centred
online communities, may serve as a gateway to far-right movements.
Considering the subtlety and the volume of misinformation and hate speech, manually
detecting each by a human has become impossible. Moreover, the very subjective nature of
the tasks tends to open room for disagreement on the classiﬁcation when multiple annotators
or moderators are involved. At this scale, moderation of content requires machine-augmented
methods for tracking and classiﬁcation of misinformation and hate speech. This motivates
the need for automated methods that can quickly process a content piece, understand its
intent, and detect possible ﬂaws or offensive aspects in the reasoning. The algorithms need
to be robust, i.e., work well for an open domain, and explainable, i.e., provide an explicit
trace of their reasoning for human collaborators like social media moderators. They need
to be responsible, i.e., associate the content with its underlying intent and cultural values to
the extent possible. We next discuss the considerations relevant to building human-centric
AI for assisting moderators with assessing the quality of online content in two cases: quality
assessment of arguments and hate speech classiﬁcation in internet memes.

90 6 Human-Centric AI in Complex Scenarios
Assessing the quality of arguments has been the subject of several lines of work in AI.
In argument quality assessment [99], the goal is to estimate the cogency, effectiveness, and
reasonableness of an argument [ 365] about a topic. Assessing the quality of the argument
involves analyzing the objective evidence, relevant assumptions, and structural soundness,
making the overall task difﬁcult. To detect the quality of arguments, Deshpande et al. [
79]
introduce SPARK: a two-stage method for contextualization of arguments, each based on
a language modeling architecture (Fig.
6.1). SPARK incorporates augmentation strategies
from argumentation literature [ 133, 250, 260], namely, feedback, assumptions, arguments
with similar quality, and counter-arguments. To obtain information for these for a novel
argument, SPARK leverages an LLM, GPT 3.5 [
264] in a few-shot manner. Example aug-
mentations for an argument about cell phone’s distractive impact on driving are shown in
Fig. 6.1. In the second step, SPARK leverages the augmented arguments by employing a
dual-encoder architecture [ 113]. The ﬁrst encoder represents the topic and the original argu-
ment, whereas the second stores individual augmentations or their concatenation. To store
the different augmentations dynamically for a given argument, the method employs a multi-
head cross-attention layer [
359]. The experiments show that the augmentations, especially
feedback, are effective for SPARK and the other baseline models. SPARK’s dual encoder is
the most effective way to leverage these arguments, outperforming other models that encode
Fig. 6.1 Overview of the SPARK method [ 79]

6.2 Domain 1: Assisting Moderation for Online Content Safety 91
longer contexts like XLNet and even LLMs like GPT 3.5. Interestingly, the human study of
this paper reveals that while humans ﬁnd the augmentations high-quality and informative
in general, they score the feedback augmentations as least informative, in contrast to the
models.
As the purpose of constructing an argument is to prove conclusions that are in some way
unknown or doubtful or that have been challenged and called into question [ 22], the task of
logical fallacy identiﬁcation is of interest because it goes beyond mere quality scoring. A
logical fallacy is a logical mistake in the reasoning used to transition from one proposition
to the next, which results in a faulty argument [
9]. Logical fallacies form a broad category of
violations of argumentation norms, including structure, consistency, clarity, order, relevance,
and completeness. Logical fallacies can be seen as components within the broader task of
propaganda detection [131], which generally focuses on arguments that aim to inﬂuence
people’s opinions often directly and intentionally using misinformation as a tool [ 158, 212].
Logical fallacies have been of interest to social science since the early days of mathematics
and philosophy [
13], as detecting whether an argument is fallacious or an act of propaganda
is a subtle task [ 330].
Based upon a review of prior work on logical fallacy classiﬁcation in philosophy, Sourati
et al. [ 330] organize a wide range of fallacies into four high-level categories of relevance,
presumption, ambiguity, and defective induction. Examples of fallacious arguments that fall
into these four categories and their members are shown in Table
6.1. This categorization
can then be used to pose the task of logical fallacy identiﬁcation as a three-stage pipeline
of detecting whether a fallacy exists, ﬁnding the coarse-level class, and identifying the
ﬁne-grained class. To solve these tasks, Sourati et al. investigate several human-centric
methods for logical fallacy identiﬁcation. According to [
30, 287, 297], people use similar
or prototypical examples of a situation or problem to solve or approach a new one. The
alluded similarity can be in the various levels, namely, coarse-grained features such as the
whole argument or statements, but also in the more ﬁne-grained features and in terms of
the extra knowledge one might have about concepts or entities discussed in the sentences as
discussed by [
14]. Having in mind the simplicity as well as explainability of using similar
examples or experiences to reason about and solve new problems or situations, this work
adapts methods for instance-based reasoning, prototype learning, and knowledge injection.
Another problem-solving approach applied to logical fallacies in this work is curriculum
learning: starting from easy or simpler tasks and gradually shifting to harder ones to learn
[
88], which has been shown to work even better than other learning strategies by [ 52].
This work devises data augmentation strategies to address data sparsity and improve the
stability of the developed models [ 409]. These techniques have been discussed in detail in the
previous chapters. The experiments in [ 68, 330] show that case-based reasoning methods,
data augmentation, and curriculum learning are all helpful methods for detecting logical
fallacies, especially for underrepresented classes and out-of-distribution data. The beneﬁt
of knowledge injection from commonsense sources is more limited overall, possibly due to
the need to contextualize the retrieval of this knowledge better to the task.

92 6 Human-Centric AI in Complex Scenarios
Table 6.1 Examples for fallacious arguments belonging to different coarse-grained and ﬁne-grained
classes covered in [ 330]
Coarse-grained class Fine-grained class Example
Fallacy of Relevance Ad Hominem Boris is not qualiﬁed to make suggestions about our
penal system. As an ex-convict, he would always take
the criminals’ side.
Ad Populum Aliens must exist because most people believe in them.
Appeal to Emotion Luke didn’t want to eat his vegetables, but his father
told him to think about the poor, starving children in a
third world country who don’t have anything to eat.
Fallacy of Extension If you don’t drive a car, you hate the Earth.
Fallacy of Relevance I know you want to imprison me for having murdered
my parents, but judge, have mercy on me, I’m an
orphan!
Intentional A woman decides to visit a certain doctor after only
asking advice on the best doctors from ONE friend.
Fallacy of Defective
Induction
False Causality The temperature has dropped this morning, and I also
have a headache. The cold weather must be causing my
headache.
False Dilemma Subscribe to our streaming services, or get stuck with
cable!
Faulty Generalization My friend said her Math class was hard, and the one
I’m in is hard, too. All Math classes must be hard!
Fallacy of Credibility My uncle is a mechanic and he says you shouldn’t
spank children. He says it’s ineffective.
Fallacy of Logic Employees are like nails. Just as nails must be hit in the
head in order to make them work, so must employees.
Fallacy of Presumption Circular Reasoning Quinoa is a delicious, plant-based source of protein
because it tastes so darn good.
Fallacy of Ambiguity Equivocation The ofﬁcer told me to freeze but it was too hot out to be
freezing, so I was justiﬁed in running away.
Meanwhile, digital communication has resulted in novel formats for expressing ideas,
including tweets and internet memes. Internet memes are a novel information medium,
typically an image, that represents a well-understood reference to a prototypical situation
within a certain community. As multimodal (combining visual and language information
creatively), relatable (dependent on community and virtual context), succinct (spreading
complex messages with a minimal information unit that connects the virtual circumstances
to the real ones), and ﬂuid (subject to variations and alterations), internet memes provide
essential data to study the ﬂux of ideas on the Web [
345]. On a less positive note, existing
computational work studying internet memes has recognized that they may contain offensive
content targeted to certain populations, such as women and ethnic minorities. A key focus of
these works is on the challenge of gathering information about memes’ evolution and spread
(so-called virality) [
200, 224, 338]. Inspired by the ﬁndings of these analyses, recently, the

6.2 Domain 1: Assisting Moderation for Online Content Safety 93
community introduced two popular hate speech tasks: Hateful Memes [ 176]a n dM i s o g y n y
identiﬁcation [ 90] to enable model development in the lab that can be applied to assist
content moderators deal with offensive content online.
To classify memes on these tasks, there have been adaptations of state-of-the-art computer
vision encoding models based on perceptual features. While these methods are a step in
the right direction, they are typically modeled as black boxes and optimized for accuracy.
Considering the complex interplay of text, vision, and background knowledge in IMs, the
decisions reached by such models cannot be trusted by human stakeholders [
345]. To assist
human moderators and social scientists in understanding the semantics and the pragmatics
of IMs at scale, these methods must be designed with explainability as a requirement. An
attempt to consider the task of hate speech classiﬁcation in internet memes from a white-box
perspective leverages the paradigm of case-based reasoning. This work experiments with
two variants of CBR (example- and prototype-based reasoning), both designed to provide
transparency into the model reasoning while still leveraging the representation learning
ability of state-of-the-art models. While the developed methods perform competitively to
state-of-the-art models, the additional beneﬁt of explainability enables users to interpret
model decisions through prototypical or nearest neighbor examples according to the model
encoding.
Figure 6.2 shows the most similar memes retrieved by the example-based classiﬁcation
for one test image, visualized by a custom-made user interface. The interface displays
the model-wise predictions for BERTTweet, CLIP , and their combination, together with
similar memes from the training dataset for explainability. The test image is misogynous,
portraying a stereotype about women. The predictions from each model are correct with high
Fig. 6.2 Explanatory interface for the example-based classiﬁcation method in [ 345]. Highly explicit
or offensive content is shown with white boxes

94 6 Human-Centric AI in Complex Scenarios
conﬁdence about the misogyny detection and stereotype classiﬁcation, which is explainable
to some degree by looking at similar examples from the training dataset. Focusing on the
most similar images per model, the combined model retrieves three images that also depict
misogyny (signiﬁed by the red background) and stereotyping. The interplay between the
text and the vision components is consistent across these memes, two of which refer to the
relationship between the kitchen and women within the context of feminist discourse. This
example shows that the instances retrieved by the combined multimodal model are the most
reliable, which also correlates with its best performance on the benchmarks.
At the same time, this example shows that the models lack further integration of back-
ground knowledge and ﬁgures of speech. The stereotype and misogyny in this case are most
likely linked to assumed background knowledge, such as the women’s social status in the
1960s, the second wave of feminism, and the more expansive link between housewives and
the kitchen. Similarly, the most similar meme in terms of content and references, the central
image in the bottom row, has explicit references to World War 3 and the discussion revolving
around two opposing opinions: (1) many Gen Z and Millennial women worried about being
drafted, and (2) women wanting equality only until they have to be a part of the draft and
joining the military. We observe further references in this ﬁgure to assumed common knowl-
edge. For instance, the center meme in the last row features the title of Back to the Future
movie with substituted “future” with “kitchen”, implying the relation between these two
terms. In the center meme in the middle row, we can observe the Annoyed Picard, the Star
Trek character that has long been associated with implying irritability or disappointment
that is also extended here towards women. While these cues are captured to some degree
by the combined model, still, a need for background commonsense, factual knowledge, as
well as internet folklore to build robust and explainable meme classiﬁcation methods in the
future can be seen. This lack of knowledge can be noticed in other extracted images as well.
Although they seem to be relevant at ﬁrst sight and might help in identifying the image as an
image containing misogyny, the exact to-the-point reference can still be missing. Resources
like the Internet Meme Knowledge Graph [
349] can be leveraged to ﬁll in knowledge graphs
and capture different perspectives embedded in memes. How to best integrate such knowl-
edge is an open challenge: one possibility is to ground novel memes to the existing memes
in the graph based on visual similarity, thus beneﬁting from the background information and
metadata in the graph [
165].
As a ﬁnal note, human-centric methods for logical fallacy identiﬁcation and hate speech
classiﬁcation hold the promise to prevent the spread of propaganda, misinformation, and tar-
geted content among the very expansive content circulating daily on social media platforms.
This could beneﬁt both industry and governments and ultimately ordinary social media users.
However, strong AI models may also be misused to increase or enhance the diffusion of
manipulative discourse [
74, 74, 355]. Furthermore, these models are trained on data whose
judgment of offensiveness may be subjective [ 345], which may emphasize certain cultural
values at the expense of others. An optimistic take is that our social media systems and com-
munication channels will become more resilient with the progress in developing methods

6.3 Domain 2: Personalizing Education 95
and evaluation tasks for logical fallacy identiﬁcation and hate speech detection [ 330], anal-
ogously to the idea that encryption algorithms can be made robust if published and tested by
the community [
312]. Progress in commonsense AI can fuel positive developments through
responsible, explainable, and adaptive technology. Y et, the challenges in terms of responsible
development and use of technology are signiﬁcant and should be considered with care.
6.3 Domain 2: Personalizing Education
Technology holds a promise to contribute signiﬁcantly to the Sustainable Development
Goal of equitable quality education. Education can also have a signiﬁcant effect on other
goals, such as eradicating poverty, improving health and well-being, and providing decent
work and economic growth opportunities, among others [
43]. Contributing to this novel
goal in a traditional learning environment faces pedagogical, operational, and technological
challenges, which hinder processes that can support human individuality and empower
learners to work towards their own goals at their own pace. Learning assistants, combining
technology with publicly available materials and social science theories, provide a possibility
for personalizing education for anyone in the world at scale and efﬁciently [
277], alleviating
the variations in terms of expectations, prior knowledge, and cognitive resources across
learners, which are notable obstacles for traditional educational classrooms.
A popular idea is that personalized education assistants can be developed based on pub-
licly available Massive Open Online Courses (MOOCs), which are growing quickly. To assist
learners in achieving impactful learning outcomes through identifying and recommending
education materials, personalized learning systems typically consist of two components:
learning analytics, which capture the knowledge state of the learner, and content analytics,
which extract information from the learning resources, including its knowledge content and
difﬁculty level [
184]. While there has been a lot of progress in modeling the learner, the con-
tent, and their interaction, many challenges remain [ 42]. How can we model the learner’s
knowledge naturally and non-obstructively? How to enable transparency and gain users’
trust? How to scale the recommendation process to various users and content types? Meth-
ods like TrueLearn [
42] provide an opening for addressing these challenges by inferring the
skills of the learner from the ongoing interaction in the form of explicit topics (Wikipedia
pages). Alternatively, the user can be asked to indicate some of their known and unknown
concepts explicitly [
5]. At the same time, deeper modeling of the user goals, intents, beliefs,
and desires, as well as recommendations based on abstract patterns are exciting future direc-
tions that can further advance the effectiveness and efﬁciency of learning, and facilitate
trust.
Meanwhile, learning theories agree on two key properties: (1) learning is an active con-
struction process, and (2) learning is possible only based on previously acquired knowledge.
Thus, learning is “a process of actively employing the already familiar to understand the
unfamiliar” [
83]. As a process that hinges on similarities between the familiar and the unfa-

96 6 Human-Centric AI in Complex Scenarios
miliar, analogies have been considered critical for learning. Namely, analogies are drawn
from a familiar, source (or base) domain to an unfamiliar, target domain. To be useful for
learning, analogies need to be metaphorical, i.e., to contain an element of surprise [
83].
Metaphorical analogies make statements that, taken literally, are absurd; yet, they provoke
a cognitive reorganization of our patterns of previously organized meaning [
122].
What does it mean to teach and learn by analogy? Teaching by analogy must be guided
by the pragmatic goals of the learner (and the teacher) and focus on the causal structure
of situations. Arguably, the end goal of analogies is to foster the development of abstract
relational schema that can be applied ﬂexibly in diverse situations [
119]. Analogies provide
the means to acquire a relational schema, which is especially useful in cases when the target
domain cannot be directly perceived because it is too small (physics particles), too large
(tectonic movements), or too abstract (the human mind) [ 124]. Analogies are bidirectional:
while their primary goal is to facilitate learning in a new domain, they also open new
perspectives for viewing and restructuring the source analog [
25].
The analogical problem-solving procedure can be envisioned as a sequence of several
steps: access, mapping, inference, and learning [ 142]. First, the source analog needs to be
accessed, which can happen spontaneously or through explicit guidance or cues). Second,
the source and the target analogs need to be matched to each other, through drawing cor-
respondences between elements. Here, correspondences between causal structures are of
particular importance due to their functional impact within their domain; correspondences
between weaker relations, e.g., based on perceptual aspects, would be less relevant. The
choice of relevant causal links is also driven by the goal of each domain, together with
its consequent actions and state changes. Third, the established mapping can be applied to
perform inference of novel solution ideas inspired by the source alone. Finally, any new
knowledge acquired based on the analogy can be abstracted as a relational schema that
captures the commonalities between the source and the target. The induction of schema is
the basic mechanism by which analogy can foster ﬂexible transfer and generalization of
knowledge [
112].
A standard illustration of the process of analogical problem-solving is a study where
college students were asked to come up with solutions to a problem where a doctor was
faced with a patient suffering from a stomach tumor. The tumor cannot be operated, and
the patient can die unless the tumor is destroyed. Rays that can destroy the tumor exist,
but applying these at high intensity will also damage the healthy cells and at low intensity,
they will have no signiﬁcant effect. While only 10% of the students were able to solve this
problem, this number increased signiﬁcantly after they were presented with “The General”
story [
112]. In this story, there is a general who captured a fortress located in the middle of a
country by dividing his army into small groups and dispatching each group simultaneously
down different roads, all leading to the fortress. Inspired by this story, 40% of the students
were able to solve the original problem, and the percentage grew to 70% once the students
were given hints to leverage the latter story.

6.3 Domain 2: Personalizing Education 97
In traditional education systems, analogies can be included in textbooks or lectures.
Studies of the use of analogy in textbooks have found that the frequency of analogies
varied [
62, 117], with generally the highest frequency of elaborate analogies observed in
physics books. Curtis and Reigeluth [ 62] distinguish between two general kinds of analogies:
simple and more elaborate (or functional). Most of the analogies found by Glynn et al. [ 117]
are simple, such as “mitochondria are the powerhouse of the cell”. The use of analogies
in classrooms is more difﬁcult to estimate. Observational studies conclude limited use of
analogy, which can be attributed to two factors: teachers relying on students understanding
the textbook analogies and a limited repertoire of analogies known by the teachers [
83, 348].
At the same time, prior studies have demonstrated that analogies have positive impacts on
learning outcomes in STEM domains, such as physics and mathematics [ 7], as well as
non-STEM domains, including business [ 106]a n dl a w[ 183].
Gray and Holyoak [ 124] indicate that analogies can also be misunderstood or counterpro-
ductive, because students in the classroom may not have the same expectations, prior knowl-
edge, or cognitive resources. These challenges can be addressed by several recommended
practices. First, given that the encoding of new knowledge is dependent on prior knowledge,
the teacher should use well-understood source analogs to capitalize on prior knowledge.
Where possible, the imbalance can be measured by pretests, and otherwise, addressed by
explaining the analogical correspondences fully to reduce cognitive efforts, without assum-
ing that students can effectively utilize analogies. If multiple source analogs are available,
they should be compared and contrasted, with an underlying recognition that analogies will
ultimately not be perfect. Second, the shared causal structure among the source analogs
should be emphasized using visuospatial, gestural, and verbal supports. Given that analog-
ical reasoning is an intensive cognitive process that relies on ﬂuid intelligence, working
memory, inhibitory control, and spatial abilities [
180], such presentational considerations
can signiﬁcantly enable comprehension without overloading limited cognitive processes.
Third, mathematical operations should be explained through verbal interpretations and con-
nections based on the real world. Fourth, once students have sufﬁcient familiarity with the
material, the teacher should encourage generating new information as this approach leads
to better retention than passive study.
An example of an analogical system that supports student learning and expression is
CogSketch [ 92]: a sketch-based education software. CogSketch is designed to model per-
ceptual, spatial, and conceptual understanding based on the principles of qualitative spa-
tial representations of segments, regions, volumes, and relationships, as well as analogical
structure-mapping processes that underlie visual reasoning. As recognition of shapes is
merely a catalyst and the mapping from shapes to concepts is one-to-many [
95], CogSketch
allows the depicted shapes to be associated by linguistic expressions to express the intent
of the author. The compositional labeling of sketching elements (glyphs, relation glyphs,
and annotation glyphs) in CogSketch, used to represent links between visual and conceptual
knowledge, is stored in the working memory. The working memory is also connected with
a knowledge base, which stores sketches and suggests conceptual relationships between

98 6 Human-Centric AI in Complex Scenarios
the depicted objects. The knowledge base provides a model of conceptual knowledge, for
which OpenCyc is used with some extensions speciﬁc to analogies and qualitative reason-
ing. OpenCyc is a commonsense knowledge base that provides extensive knowledge of over
1.3 million facts about 58,000 everyday concepts and 8,000 relations about them, based on
cognitive science ideas [
92].
The key advantage of CogSketch for learning spatial relationships, e.g., in the geology
domain, is twofold: it provides rapid feedback to students and makes assessment simpler
and more efﬁcient. However, to achieve these goals, it is important to develop technology
with high generalizability to novel classes and people, as well as explainability, which is
still a major challenge [
50].
There are also tutoring systems that simulate different kinds of mental models. For
instance, the Qualitative Concept Map (QCM) [ 77] tool is a uniﬁed platform that allows
modelers to explore qualitative models, incorporate them into probabilistic Bayesian mod-
els, and output them in formats usable in other forms of reasoning (e.g., analogical reason-
ing). This tool can be used to model physical phenomena such as continuous parameters
(quantities), causal relationships between them (inﬂuences), and mechanisms underlying
physical causality (physical processes). QCM automatically checks for any modeling errors
that violate the laws of the qualitative process theory [
93] and probability theory [ 273], pro-
viding detailed error messages. While QCM and CogSketch support cognitive processes,
they require a lot of manual knowledge engineering, which has prompted recent work to
investigate how to automate these processes further [
50, 153].
As a ﬁnal note, given the high-stakes application of AI to education, it is encouraging to see
learning assistants that are fueled by commonsense AI and cognitive science theories. Prior
work on recommending educational materials, sketching systems, and qualitative simulators
has already had a signiﬁcant impact across the STEM ﬁelds. At the same time, many other
applications can be envisioned, guided by principles of analogy and the vast amount of
publicly available materials, to support learner ideation, discovery, and hypothesis testing [
3].
6.4 Domain 3: Understanding Situations in Traffic
Developing reliable intelligent agents for the trafﬁc domain has been an attractive pursuit
due to the high-stakes nature of this domain and the magnitude of its market [
284]. These
agents include autonomous vehicle components or monitoring systems (e.g., street cameras).
Autonomous vehicles are expected to reduce the rate of trafﬁc incidents and casualties, while
simultaneously behaving in a way that ﬁts existing norms in trafﬁc. Trafﬁc monitoring agents
are expected to infer autonomously perceptual aspects of the captured input (e.g., how many
cars are there in the rightmost lane) and infer more abstract reasoning patterns (e.g., would
the accident have been prevented if the red car had not switched lanes). The magnitude of
the market and the impact of trafﬁc on societal safety makes these goals urgent.

6.4 Domain 3: Understanding Situations in Traffic 99
What is the scope of trafﬁc understanding? Trafﬁc understanding is a complex multimodal
challenge consisting of object detection and classiﬁcation, object localization, trajectory
prediction, sensor fusion, and planning. Trafﬁc understanding encapsulates a unique blend
of low-level perception tasks [
126] and human-level symbolic reasoning and cognition [ 336],
making it a neuro-symbolic goal. In [ 114], we organized the trafﬁc tasks into three high-
level categories of safety, perception, and inference (Fig. 6.3). Each of these task categories
can be considered from an ego-centric perspective of an autonomous vehicle (ﬁrst-person
view) and a perspective of a trafﬁc observer like a camera (third-person view), resulting in
corresponding variants.
Table 6.2 shows ﬁrst- and third-person view examples for each of the three trafﬁc task
categories, illustrating the richness of skills required for this domain. Tasks span from passing
driving tests and classifying out-of-domain objects, to reasoning over sensory failures and
causal reasoning about events.
At present, intelligent trafﬁc agents leveraging the latest neural or symbolic advance-
ments perform well in the lab. Y et, their real-world usage has been marked with notorious
Fig. 6.3 Our taxonomy of trafﬁc tasks: safety, perceptual, and inference, from [ 114]
Table 6.2 Example tasks for ﬁrst (1st) person view (autonomous vehicles) and third (3rd) person
view (trafﬁc monitoring) that demonstrate the need NeSy Representations and Reasoning. Courtesy
of [ 114]
Task class View Sample challenge
Safety 1st Pass a dynamic driving test for autonomous vehicles.
Safety 3rd Understanding of rare road events, e.g., extreme weather.
Perceptual 1st Classify out-of-domain objects in the A V’s vicinity.
Perceptual 3rd Understanding trafﬁc elements based on perception (e.g., number of
vehicles).
Inference 1st Introspection: sensory failure, NeSy for reliance on secondary modalities
Inference 3rd Establishing links between observed events and their likely causes.

100 6 Human-Centric AI in Complex Scenarios
examples that show that their reliability is far from the desired mark. A notable example
of autonomous driving is the Uber fatality [ 225], which occurred due to the system focus-
ing on a single modality (the perception system), rather than fusing multiple modalities of
sensory information. Besides fusing multi-sensory information, the Uber accident shows a
larger issue: autonomous vehicles may not know how to deal with inconsistent or unknown
situations. For example, if an autonomous vehicle perceives an unknown object or faces a
novel situation (e.g., an unknown trafﬁc signal, like a ﬂashing yellow light [
51]), it may
react in unpredictable ways. It may choose to ignore unknown objects [ 225] or extrapolate
novel situations to prior experiences based on its underlying pattern-matching mechanisms.
An example of the latter behavior is the accident of the Google Autonomous V ehicle (A V)
in 2016, caused by the A V switching lanes after detecting sand bags.
1
Similarly, considering the related task of trafﬁc monitoring, a processing system may
detect that a vehicle and a bike lane overlap, but it would not be able to deduce whether this
represents a trafﬁc violation [
114]. Moreover, the intelligent system may fail to understand
certain context-speciﬁc behaviors [ 266] that happen in particular locations or at particular
times. These experiences highlight the imminent need for reliable systems that are robust,
explainable, and responsible. Merely relying on gathering sufﬁcient data for each of these
speciﬁc scenarios is unrealistic [
405], thus emphasizing the need for novel approaches and
integration of common sense.
How can commonsense AI enable robust, explainable, and responsible reasoning for
autonomous vehicles and trafﬁc monitoring systems that are being entrusted with human-
level decision-making? Commonsense knowledge and reasoning can be used to connect the
dots between domain knowledge and data from sensors, vision, and logs, and the resulting
information can be fed into neural networks to exploit their generalization power [
114]. Such
a reasoning methodology provides an opening for the resulting models to be explainable,b y
transforming the explicit knowledge into human-readable format; adaptive,b yl e v e r a g i n g
the knowledge to transfer better to novel situations; responsible, by providing a mechanism
for communication with the model in a meaningful way; and collaborative, by facilitating
the extraction and representation of meaningful information [ 4].
For instance, this can be done by creating specialized embeddings for autonomous driv-
ing [385], enhancing the knowledge graph for scene entity prediction in autonomous driving
[56], extracting actionable information from raw sensor data in trafﬁc [ 251], or using knowl-
edge bases for representing information sources relevant to trafﬁc situations [ 130].
A zero-shot evaluation procedure can be employed to test the robustness of methods.
In [ 405], we used a natural language formulation of trafﬁc reasoning and experimented
with equipping a language model with domain knowledge from a QA benchmark [ 175],
commonsense knowledge from a synthetically created QA set [ 404], and their combination
(Fig. 6.4). The resulting model was evaluated on an unseen test set (Table 6.3) that assesses
causal inference, on which the aggregated knowledge performed the best, the vanilla model
1 https://www.wired.com/2016/02/googles-self-driving-car-may-caused-ﬁrst- crash/, accessed on
July 12, 2023.

6.4 Domain 3: Understanding Situations in Traffic 101
Fig. 6.4 Overview of the study framework in [ 405], which evaluates four knowledge-enhanced
language methods, adapted with different knowledge sources on three trafﬁc domain datasets, in a
zero-shot manner
was the worst, and commonsense knowledge was more beneﬁcial than domain knowledge.
The contribution of various knowledge types was task-dependent: commonsense knowledge
is most impactful for complex and hypothetical tasks, like introspection, whereas retrieving
domain knowledge is most effective for tasks that require contextual decision-making and
understanding of trafﬁc rules [ 405]. Often, a decision is supported by the complementarity
of both kinds of knowledge. Let us consider the question what might be the reason that a car
is waiting in the intersection when the trafﬁc light is green? Its answer The car is waiting
for pedestrians is supported by commonsense knowledge that cars will pass the crosswalk
when driving and crosswalk will appear at the intersection, and by trafﬁc domain rules that
cars should yield to pedestrians passing the crosswalk [ 405].
As a structured and organized representation of human knowledge, commonsense knowl-
edge bases can also be used to explain how and why certain decisions or actions are taken.
For example, if a decision is made by a machine learning model based on commonsense
knowledge, it can be explained by referring to the relevant facts, rules, and principles stored
in the knowledge base. This makes it easier to understand the decision-making process and
to identify any biases or errors that may have occurred. The integration of symbolic rea-
soning allows for the explicit representation of knowledge in the form of rules, leading to
an understandable explanation. In the context of autonomous driving, these rules are essen-
tial to abide by the “rules of the road.” By incorporating symbolic representations into the
reasoning process, neuro-symbolic systems can provide explanations that are grounded in
human-understandable concepts. For example, if an autonomous vehicle is unsure of what
it is perceiving, instead of showing a saliency map [ 308] on possibly irrelevant parts of the
input image, we can construct an interpretable, natural language explanation showing that
the vehicle was unsure of what it perceived. These symbolic representations can be used

102 6 Human-Centric AI in Complex Scenarios
to represent domain-speciﬁc knowledge, causal relationships, and decision-making rules,
making the reasoning process more transparent and interpretable.
Prior work on a multimodal monitoring system for autonomous vehicles [ 115] adds a
set of domain-speciﬁc rules and commonsense knowledge to explain the failures between
parts, e.g., when the vision system and sensor system disagree on what is being perceived.
These explanations also reﬂect (and explain) the inherent multimodal nature of autonomous
systems and trafﬁc. Neural networks learn from complex, high-dimensional data, and sym-
bolic reasoning, like diagnostics brings transparency and interpretability. By integrating
these two approaches, neuro-symbolic systems can leverage the strengths of each. This
also aligns with the need for explanations for accountability, so that we can diagnose and
understand the errors in complex systems.
These ﬁndings suggest that by incorporating richer knowledge into the modeling pro-
cess, we can unlock new opportunities for the development of intelligent systems capable of
reasoning across different modalities and delivering more comprehensive, interpretable, and
accurate results. Y et, we are only beginning to realize this potential. To this end, HANS [
284]
provides a theoretical neuro-symbolic framework for integrating different modalities and
knowledge types into a single neural system, consisting of six general processes: genera-
tion, semantic representation, augmentation, assessment, infusion, and inference. Y et, the
combination of multiple modalities and knowledge types for the trafﬁc domain remains an
open challenge. The idea of scene knowledge graphs (SKGs) [
375] can intuitively be used as
a common representation, supported by trafﬁc monitoring formalisms like the Scene Ontol-
Table 6.3 Examples of BDD-QA, TV -QA, and HDT-QA from [ 405]. (*) denotes the correct answer.
BDD-QA
Q: The car in front of the car is slow, but the trafﬁc is also heavy in other lanes, what will the car
do next?
A1: The car speeds up and turns to the right; A2: The car moves back to the right side of the road;
A3: The car slows down(*);
A4: The car backs up slowly
TV-QA
Description: The POV car is quickly going down a highway. The POV car approaches an
intersection. There is a red sedan in the opposing lane waiting to turn and cross the intersection.
The red sedan quickly makes a left turn. when the POV car enters the intersection. The POV car
veers to the right. The red sedan hits the side of the POV car.
Q: Could the accident be prevented if the involved vehicles change lane or turn properly?
A1: Ye s ( * ) ;A2: No, that was not the main cause of the accident
HDT -QA
Q: If you ﬁnd yourself in a skid:
A1: Brake lightly; A2: Brake abruptly; A3: Stay off the brakes(*)

6.5 Domain 4: Object Manipulation and Visual Reasoning by Household Robots 103
ogy [ 262] and the Trafﬁc Monitoring Knowledge Graph [ 284]. Following [ 375], distant
supervision data can be extracted to transform situations into such SKGs, and the SKGs into
decisions or classiﬁcation outputs. These are open-ended research directions that require
signiﬁcant innovation both for the trafﬁc domain and multimodal reasoning in general.
Besides the development of systems and knowledge bases, another important goal is
representative evaluation strategies that are multimodal, interactive, and realistic. While
there are several autonomous driving challenges, including multimodal task challenges,
2
these tasks should be upgraded to more realistic settings that cover the complexities and
uncertainties of the safety, perception, and inference.
6.5 Domain 4: Object Manipulation and Visual Reasoning by
Household Robots
Embodiment is a key aspect of communication. The application of commonsense AI is per-
haps easiest to envision with embodied agents, i.e., robots, performing certain household
tasks. For instance, they can assist us by bringing us a cup of water or arranging the con-
ﬁguration in a room according to some verbal description or a visual depiction. They could
also be instructed to perform a task while satisfying certain constraints, e.g., to sweep the
entire rug into a speciﬁc bucket without exceeding a certain height.
A recent compelling framework for robot manipulation tasks, called VIMA [ 159], inte-
grates a variety of tasks and their instantiations. Speciﬁcally, VIMA deﬁnes 17 tasks, 4 of
which are used for testing models in a zero-shot manner (Fig.
6.5): (1) object generalization,
where all prompts are seen verbatim during training, but the placements of the objects are
randomized at test time; (2) combinatorial generalization, where all textures and objects
are seen during training, and new combinations of them appear during testing; (3) novel
object generalization, where test prompts and the simulated space include novel textures
and objects; and (4) novel task generalization, containing new tasks with novel prompt
templates at test time. VIMA provides the prompts to the models in a multimodal format,
interleaving textual and image tokens, for example: sweep all
.<rug image.> into .<bucket
image.> without exceeding .<height bar image.>.
The VIMA tasks are designed to test six skills of robot manipulation models: (1) simple
robot manipulation, where each image in the prompt corresponds to a single object; (2) visual
goal reaching, where the goal is to manipulate objects to reach a desired conﬁguration;
(3) novel concept grounding, where new concepts are ﬁrst introduced and subsequently
used in the instruction; (4) one-shot video imitation, where the robot watches a video and
needs to reproduce the same motion trajectory for a particular object; (5) visual object
satisfaction, requiring the robot to carefully manipulate objects without violating certain
2 NuScenes challenge: https://www.nuscenes.org/object-detection?externalData=all&mapData=all
\&modalities=Any.

104 6 Human-Centric AI in Complex Scenarios
Fig. 6.5 Tasks of the VIMA framework, reused with permission from [ 159]
constraints, typically relating to safety; and (6) visual reasoning, requiring certain matching
via abstraction of visual appearance and visual memory.
What agents can be developed to solve the VIMA task? Multimodal prompts are not
accepted as inputs to the state-of-the-art models. The authors of VIMA propose a strong
baseline based on Transformer architecture, which can perform visual goal-reaching, one-
shot video imitation, and novel concept grounding using a single model. This baseline is
designed to learn a robot policy .π(at | P, H),w h e r e. H denotes the past interaction history
deﬁned as pairs of observations and actions. The multimodal prompts are encoded with a
frozen pre-trained language model, and the robot commands are decoded based on these
encoded prompts by using cross-attention layers. The training procedure of the baseline
includes data augmentation and specialized objective functions, which ultimately enables
the model to perform much more robustly than models that are much larger and less adapted
to the task, like Flamingo [ 6]. Curiously, the baseline model retains a completion rate of
80% for the ﬁrst three tasks, and 50% for novel task generalization. The impact of the size
of the encoder used for the multimodal prompt is minimal, with models ranging from 2 to
256 million parameters performing similarly.
The VIMA analysis points to several important future directions, which largely gener-
alize to other embodied tasks. First, considering that semantic understanding of the world
is important for robots to make safe and well-justiﬁed decisions on their course of actions,
and to adapt to changing environments, agents must possess reliable world models. Namely,
world models should provide useful internal representations, which can be linked to adequate
actions and transferred ﬂexibly to new environments [ 96]. Such capabilities may include
memory, procedural reasoners, and skill representations, ultimately contributing to better
generalization, robustness, and long-term planning. Second, while the VIMA task already

6.6 Summary and Discussion 105
enables the evaluation of six skills, it can be extended to provide more ﬁne-grained evalu-
ation (e.g., due to a shift in perspective or angle) and additional skills. Such skills include
long-term planning, open-world generalization, and reasoning about social and physical
circumstances, as well as reasoning about the causality of actions and their counterfactual
versions. Third, even though simulation environments are invaluable for studying robot
behavior and developing relevant abstractions, they inherently are mere approximations of
the real world. Namely, robot algorithms developed for simulations have poor performance
when deployed in the real world [
97, 147]. This so-called sim-to-real gap can be addressed
by adequate strategies for addressing distribution shifts, such as transfer learning [ 344],
learning generalizable scene priors based on background knowledge [ 343], and specialized
(e.g., physics) models [ 272].
6.6 Summary and Discussion
This chapter discussed the need for commonsense AI in the context of human-AI teaming in
complex domains, as a way to both automate certain capabilities and collaborate to obtain
a whole that is more than the sum of its parts. Starting from three myths showing extreme
positions on the capability of either humans or AI, it described an existing framework for
human-AI teaming that considers the strengths and weaknesses of humans and AI separately
for tasks with various complexity, uncertainty, and time available.
Then the chapter proceeded to discuss human-centric AI for four domains: content safety,
education, trafﬁc understanding, and robotics. In the domain of content safety, we consid-
ered how AI can help content moderators deal with misinformation, through methods for
robust and explainable detection of low-quality arguments and logical fallacies, based on
case-based reasoning, curriculum learning, and contextualization with LLMs and knowl-
edge graphs. Then we discussed another challenge in this domain of hate speech in complex
formats like internet memes, which can be addressed by human-centric methods based on
case-based reasoning and knowledge modeling. In the domain of education, personalizing
learning paths to the background of the learner has been a popular task, producing models
based on Bayesian techniques for modeling user background and interests, and connecting
these to the features of the candidate materials. Another line of research has considered the
development of learning environments that support user learning (e.g., through sketching),
which are typically driven by principles of analogical inference between familiar concepts
and novel materials. In the domain of trafﬁc understanding, we considered autonomous
vehicles and trafﬁc monitoring tasks of perception, safety, and inference. We discussed
explainable methods that address these tasks based on trafﬁc domain rules formalized in
semantic web standards and robust methods that leverage knowledge injection from com-
monsense knowledge graphs, question-answering pairs, and driving manuals into language
models. In robotics, we focused on a framework for household robots manipulating objects
and performing visual reasoning to achieve multimodal goals. The robots are instructed via

106 6 Human-Centric AI in Complex Scenarios
a natural mixture of textual and visual tokens. The most robust models for this task are those
specialized to the household tasks through suitable objectives and training strategies.
The development of commonsense AI for these domains reveals several insights. First,
large language and multimodal models are indispensable components for all domains,
whereas they must be combined with other components to enhance the system’s robustness
and explainability. These additional components can be knowledge graphs, domain rules, or
specialized neural models. Ongoing work tries to develop tightly integrated neuro-symbolic
architectures, which integrate language models with symbolic reasoning components (e.g.,
theorem provers) to enable deterministic and transparent decision-making processes [
282,
351]. Second, there is a wide range of techniques available today to enable models to perform
more robustly, including learning generalizable prototypes in the architecture, augmenting
with domain-relevant data, or designing a curriculum for the model to learn better .A st h e
robust generalizability of the models is still low for many domains, ongoing research is inves-
tigating how to leverage cognitive principles of analogy and abstraction to enable strong and
well-founded generalization of models [
153, 329]. Third, existing explainability methods
go beyond the ‘vanilla’ language models in terms of providing insights into their reasoning .
However, the expressivity of these explanations may be low, as in the case of instance-based
examples, may be difﬁcult to ground, as is the case when using symbolic rules, or may be
inconsistent with the model decision, as may be the case with chain-of-thought and similar
in-context demonstration techniques. Ongoing work on tighter neuro-symbolic integration
may provide natural explanations for the model reasoning that are consistent, expressive,
and easier to ground [
149, 282].
This chapter also revealed particular challenges that provide exciting future research
directions. As was most apparent from the discrepancy between the highest utility of feed-
back on arguments for language models and the lowest for humans, there is often a dis-
crepancy between human and model approaches. On the one hand, as is the premise of this
chapter, this discrepancy can be exploited to alleviate human weaknesses, such as human
bias when judging misinformation and hate speech . On the other hand, while evaluation
practices have advanced signiﬁcantly, there is still a need to design evaluations that can
provide a more thorough evaluation of the abilities of models as autonomous or human-
supporting assistants . Understanding the model limitations is important especially from a
perspective of safety, as illustrated by the possibility of misusing argumentation models for
harmful goals. For some domains, like education, evaluation is often limited in scale and
relies upon small user studies. For others, like trafﬁc, there is a need for publicly available
datasets, as many of the available datasets are proprietary. Finally, all domains would bene-
ﬁt from research on developing faithful simulation environments that bridge the sim-to-real
gap to support the exploration of models in controlled settings, while still retaining key
human-centric challenges to stimulate impactful and responsible innovation.
Another promising line of research is that of developing high-quality knowledge sources .
High-quality knowledge can enable better performance on a domain, useful explanations,
and a mechanism for controlling the model behavior to enable responsible use. Among the

6.6 Summary and Discussion 107
four reviewed domains, we observe a wide variety of knowledge types and formats. In the
content safety domain, prior work has leveraged commonsense knowledge and web knowl-
edge through LLM prompting, whereas domain-speciﬁc resources about internet memes
remain to be fully exploited in techniques for robust and explainable hate speech reasoning.
In education, commonly used sources include massive open online courses for recommenda-
tion and commonsense knowledge to support assistive environments. In the trafﬁc domain,
the wide range of sources employed in prior work includes domain materials in the form
of driving manuals, commonsense knowledge, trafﬁc ontologies, and question-answering
data. To support the development of robust, explainable, and responsible models for deep
reasoning in critical domains, it is important to devise well-motivated knowledge collections
that comprehensively cover existing data formats and knowledge types, but also cover mul-
tiple perspectives to account for the natural complexity of knowledge and the subjectivity
of information. While LLMs can be seen as models that have potentially accumulated such
data indirectly, it is essential to create explicit representations of this data.
A third future direction is the further development of reasoning techniques . There is a
consensus that LLMs (or any data-driven models that may supersede them) are necessary, yet
insufﬁcient on their own, for reasoning in critical domains. While some of their weaknesses
can be alleviated by further scaling up or by humans who collaborate with these models in
user-friendly environments, there is a trend towards developing neuro-symbolic models that
can leverage the power of LLMs and judge the correctness of their output, for instance, by a
formal veriﬁcation step. A related emerging trend is the incorporation of cognitive theories
and methodologies with these language models , as illustrated by the incorporation of some
analogical reasoning principles in education and the recent case-based reasoning models
that leverage language models as their retrievers and adapters. These trends are promising
and are likely to result in hybrid methods that bring the best of neural (language) models
and symbolic sources and reasoning methods.
As a ﬁnal note, the four selected domains serve merely as an illustration and many oth-
ers can beneﬁt from the further development of commonsense AI techniques . The medical
domain, for instance, has applications such as preventative medicine and therapy that need
complex reasoning models built on the CARE principles [
146, 346]. Nutritional sustain-
ability is also of interest, where policymakers can be supported by technology that has a
comprehensive model of processes of food production, including transportation, sourcing,
and recycling [ 255]. In law, commonsense AI can leverage analogical principles to draw
connections to precedent lawsuits [ 15], or provide explainable mechanisms to help compa-
nies stay compliant with the latest regulations [ 44]. A deeper analysis of these domains falls
out of the scope of this book, but it is a worthwhile consideration and it requires technology
to be collaborative, explainable, robust, and responsible, similar to the four domains of focus
in this chapter.

7Conclusions and Outlook
Abstract
This chapter summarizes the content of the book. It reﬂects on the content of the previ-
ous six chapters, distilling their challenges, state-of-the-art methods and ﬁndings, lessons
learned, and open research directions. The chapter also synthesizes notes on common-
sense AI that transcend the individual chapters, such as the placement of content and the
applicability of methods from certain chapters to others. As a ﬁnal paragraph, the chapter
derives three overarching open research directions that are prominent in the previous
chapters: reasoning architectures, evaluation, and cross-disciplinary integration.
7.1 Reflection on the CARE Principles
Amidst the current wave of research and development in AI, its duality is manifested along
multiple dimensions. AI models are fascinating–we can talk to them about anything, get
summaries of long documents, receive tips and suggestions, and even request advice or
personalized explanations. Those same models may struggle to infer simple causal impli-
cations of events, may forget what they said two sentences ago, and may fail to provide
a consistent response across small variations in the task. This book makes the case that
what lies between fascination and disappointment is the decades-old challenge of common
sense–neural vision and language models have no underlying formal model of other agents,
of the physical environment, of time, of math, and so on. State-of-the-art neural vision and
language models have been trained to manipulate tokens, and even with all their impressive
sophistication and scale, they remain next-token predictors.
The other duality of AI concerns its societal use and impact. Language and vision models
have inspired thousands of new applications of AI, aiming to help people with tasks in
law, sustainability, education, health, trafﬁc, and any other imaginable domain. Virtually
anyone in the Western world is familiar with ChatGPT by now, and developing countries
© The Author(s), under exclusive license to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science, https://doi.org/10.1007/978-3-031-69974-0_7
109

110 7 Conclusions and Outlook
see this technology as a way to catalyze their growth. New hopes emerge for novel cures for
difﬁcult diseases, for more adaptive and personalized education, and for sustainable and safe
behaviors and policies. At the same time, fraud, hate speech, and misinformation are also
blooming, making a strong impact on the political landscape across the globe, and affecting
the perception and health of billions of individuals. This book considers what characteristics
AI needs to be used for good, including explainability, collaborativeness, and robustness,
and what can be done to prevent its malicious use, through responsible and ethical use. It
then dives deeper into four domains, to provide insights into how commonsense principles
affect these domains, and what are key standing challenges.
Chapter 1 provides an introduction to the breadth and depth of commonsense reasoning
in AI, and expands on the duality aspects alluded to here. Besides providing deﬁnitions,
it describes dimensions of commonsense knowledge, including temporal and motivational
knowledge, and reasoning, including causality and planning. These dimensions are meant to
provide a sense of scope only, as there is currently no consensus on such a taxonomization of
this ﬁeld. Similarly, we describe common tasks for evaluating common sense, which again
illustrates the richness of this research area, but the evaluation practices are still largely
evolving. With common sense sometimes proclaiming to be solved, the chapter provides
three examples of standing challenges: planning, Theory of Mind, and analogical reasoning.
Besides an illustration of challenges, these three examples illustrate a common case in
the ﬁeld, where skill is proclaimed to be acquired by models (through so-called emergent
abilities) in one paper, and shown to be lacking in another. Such cases typically have an
overarching explanation of the kind: there has been progress towards this goal as witnessed
by higher accuracy, but it is not robustly present, as shown by inconsistent model outputs. To
resolve such debates in a more principled manner, the chapter proposes to follow the recent
CARE roadmap, of developing AI that is collaborative, adaptive (or robust), responsible,
and explainable.
AI must be able to provide commonsense explanations . Starting from a popular XAI taxon-
omy, we differentiate several families of explainable methods from a commonsense perspec-
tive (Chap.
2). Explanations can leverage explicit predeﬁned structures, such as knowledge
graphs, through dynamic path extraction or generation. The model architecture can be mod-
iﬁed to include compositional (i.e., ﬁner-grained) objectives. The model can be designed to
classify by cases, which can be either based on selecting the nearest instance or the nearest
learned prototype. As of recently, language models are themselves seen as explanation gen-
erators, most famously through the chain-of-thought paradigm. Follow-up methods build on
this idea to provide LM-generated explanations in the form of a graph, tree, or code. All of
these methods have complementary mechanisms and produce different forms of explana-
tions, thus illustrating the wide range of possibilities, but also the lack of standardization of
what an explanation is and what explanation is best in which case. Thus, standing challenges
are developing better explanation methods, but also standardization of evaluation practices,
and better alignment with theories in philosophy (e.g., about logical fallacies) linguistics
(e.g., about analogy) and cognitive psychology (e.g., prototype theory).

7.1 Reflection on the CARE Principles 111
AI needs to have commonsense mechanisms for collaboration (Chap. 3) with humans
and automated agents. To collaborate, AI must have a model of situations, in terms of their
relevant objects with their attributes, states, relationships, and affordances. Such a model can
be represented as a scene knowledge graph, and produced on the ﬂy by Transformer neural
architectures. To perform tasks consistently, AI needs an internal model of its plans, goals,
and history of prior experiences, all of which can be separate modules in its architecture,
some of which are separate language model agents. AI needs to model other agents explicitly
in terms of their beliefs, goals, and other mental attributes, which also requires coupling
language modeling architectures with a symbolic reasoner. And, it must be able to collaborate
in a multimodal setting, connecting the dots between language, vision, and background
knowledge, by modeling these aspects separately and fusing their representations. Besides
further development of these models, another urgent research goal is to devise faithful
simulation and testing environments with longer-term and multi-agent interactions.
AI must be robust to shifts in input distributions, variations in phrasing, and noisy inputs
(Chap. 4). There has been signiﬁcant progress towards this goal merely by scaling up models–
current LLMs function as general-domain and cross-task agents: they can respond to any
topic, in any format, and per any task instruction; and all of that without large-scale data
annotation or expensive ﬁne-tuning. At the same time, these models show variations in their
behavior that are hard to make sense of, owing to their underlying objective of probabilistic
next-token prediction. To deal with distribution shifts, one possibility is to perform data
augmentation by creating new data points or augmenting each of the original data points
with abstract information. To improve generalization and alleviate dependency on data,
alternatives to ﬁne-tuning have been designed, including preﬁx-tuning, auto-prompting,
and zero-/few-shot prompting. To verify whether the models generate expected outputs,
their output can be post-processed by symbolic interpreters that manipulate logic, code,
or plans, depending on the requirements of the task. To abstract over surface-form varia-
tions and similarity to relational correspondences, LLMs can integrate analogical reasoning
skills, which is currently still a challenging target. A promising path forward is integrating
these complementary strategies into comprehensive architectures that perform dynamic data
augmentation, use adequate model access mechanisms, connect to deterministic symbolic
reasoners, and perform relational matching by analogy.
Ultimately,AI must be designed to act responsibly (Chap. 5). Responsible behavior entails
following societal norms, understanding morality and ethics, and obeying laws. As implied
by the robustness discussion, AI’s morality can be enhanced to some extent using data
augmentation strategies. Y et, its generalization is fragile and tends to start discriminating
against populations deﬁned by ethnicity, profession, and gender, among other categories.
Biases may never be fully eradicated, but they must be qualiﬁed and aligned with moral
perspectives and norms. While current frameworks for morality like Delphi are data-driven,
future AI methods must combine this data-driven (bottom-up, descriptive) approach with
norm-driven (top-down, prescriptive) morality modeling. As morality and ethics are still a
matter of debate in social sciences and are poorly understood by computer scientists, the

112 7 Conclusions and Outlook
design of such future systems must be done by interdisciplinary teams. Notably, other aspects
of responsible AI such as legal and governance considerations and impact on humans (e.g.,
crowd workers) are well-addressed in other recent books [
61, 63].
7.2 Integrating the CARE Principles
These four CARE considerations are presented as separate chapters in this book, which
may give an impression that they are disjoint. While the challenges can be largely separated
(e.g., a method can be explainable and not robust, or vice versa), the methods to achieve
these challenges are often intertwined . For instance, analogical reasoning is described as a
mechanism to achieve robustness but may also be essential to explain why a certain prediction
or recommendation is made. Chain-of-thought and its descendants have the reverse situation–
they are presented in the Explainable Commonsense AI chapter, however, these methods
provide a mechanism for models to perform more robustly. Responsible AI mechanisms are
often based on combinations of robust, collaborative, and explainable techniques, such as
data augmentation.
Real-world use cases (Chap. 6) are often complex and require a combination of these
four factors . Content safety in online media like Twitter arguments and internet memes
requires CARE methods to deal with hate speech and misinformation. Educational recom-
menders and assistants necessitate methods that can deal with novel learner circumstances
and explain their mistakes in a personalized manner. Trafﬁc understanding requires methods
with awareness of legal and ethical constraints, and domain norms, all while collaborating
in an explainable and robust manner. In robotics, robot manipulation has similar considera-
tions, as robots need to be safe, generalize to new situations, and be able to collaborate with
other agents in their environment. In real-world human-AI teaming scenarios, the remain-
ing challenges are to understand the strengths and weaknesses of both people and AI in the
evolving landscape, through suitable evaluations and user studies. By designing high-quality
knowledge sources, these domains and many others can beneﬁt from training and testing
based on well-motivated materials. And ﬁnally, by designing systems that can combine
such top-down knowledge with data-driven models, we may be able to bring the best of both
worlds together.
The lessons learned from these chapters and the review of state-of-the-art methods and
remaining challenges leave a lot of open research directions. Novel architectures for rea-
soning are necessary to combine the beneﬁts of general-purpose neural (language) mod-
els and specialized world models for Theory-of-Mind, planning, memorization, and so
on. It is not clear how to design and implement those world models, and how to design
the interaction between the general and the speciﬁc components, but recent research has
already proposed several directions such as LeCun’s JEPA architecture [
16]. Another thorny,
yet gradually improving, issue is that of cross-disciplinarity: commonsense AI challenges
have often counterpart theories in disciplines like psychology, philosophy, and linguistics.
Partnerships across disciplines can be difﬁcult because of the different practices they follow,

7.2 Integrating the CARE Principles 113
however, it is essential for further development and it may bring novel ideas beyond incre-
mental progress. A third overarching challenge is evaluation: with the rapid development of
methods and models, and the frequent ingestion of evaluation benchmarks during training,
the question arises: is the benchmark-driven evaluation paradigm, currently dominant in AI,
the right path forward? At present, it seems essential to at least complement such evaluation
with well-designed user studies and, where possible, high-ﬁdelity simulators. None of these
three directions are trivial, but they point the way forward towards a commonsense AI with
CARE principles that can improve the lives of many.

References
1. Aamodt, A., Plaza, E.: Case-based reasoning: Foundational issues, methodological variations,
and system approaches. AI Communications 7, 39–59 (1994). DOI https://doi.org/10.3233/
AIC-1994-7104.U R L https://doi.org/10.3233/AIC-1994-7104.1
2. Acharya, A., Talamadupula, K., Finlayson, M.A.: An atlas of cultural commonsense for machine
reasoning. In: AAAI Conference on Artiﬁcial Intelligence (2021)
3. Ahrabian, K., Du, X., Myloth, R.D., Ananthan, A.B.S., Pujara, J.: Pubgraph: A large scale
scientiﬁc temporal knowledge graph. arXiv preprint arXiv:2302.02231 (2023)
4. Akata, Z., Balliet, D., De Rijke, M., Dignum, F., Dignum, V ., Eiben, G., Fokkens, A., Grossi,
D., Hindriks, K., Hoos, H., et al.: A research agenda for hybrid intelligence: augmenting human
intellect with collaborative, adaptive, responsible, and explainable artiﬁcial intelligence. Com-
puter 53(08), 18–28 (2020)
5. Alatrash, R., Chatti, M.A., Ain, Q.U., Fang, Y ., Joarder, S., Siepmann, C.: Conceptgcn: Knowl-
edge concept recommendation in moocs based on knowledge graph convolutional networks
and sbert. Computers and Education: Artiﬁcial Intelligence 6, 100193 (2024)
6. Alayrac, J.B., Donahue, J., Luc, P ., Miech, A., Barr, I., Hasson, Y ., Lenc, K., Mensch, A.,
Millican, K., Reynolds, M., et al.: Flamingo: a visual language model for few-shot learning.
Advances in Neural Information Processing Systems 35, 23716–23736 (2022)
7. Alﬁeri, L., Nokes-Malach, T.J., Schunn, C.D.: Learning through case comparisons: A meta-
analytic review. Educational Psychologist 48(2), 87–113 (2013)
8. Allcott, H., Gentzkow, M., Y u, C.: Trends in the diffusion of misinformation on social media.
Research & Politics 6(2), 2053168019848554 (2019)
9. Almossawi, A.: An illustrated book of bad arguments. The Experiment (2014)
10. Amershi, S., Cakmak, M., Knox, W.B., Kulesza, T.: Power to the people: The role of humans
in interactive machine learning. Ai Magazine 35(4), 105–120 (2014)
11. Anderson, P ., Wu, Q., Teney, D., Bruce, J., Johnson, M., Sünderhauf, N., Reid, I., Gould, S., V an
Den Hengel, A.: Vision-and-language navigation: Interpreting visually-grounded navigation
instructions in real environments. In: Proceedings of the IEEE conference on computer vision
and pattern recognition, pp. 3674–3683 (2018)
12. Angelov, P ., Soares, E.: Towards explainable deep neural networks (xdnn). Neural Networks
130, 185–194 (2020)
© The Editor(s) (if applicable) and The Author(s), under exclusive license
to Springer Nature Switzerland AG 2024
F. Ilievski, Human-Centric AI with Common Sense , Synthesis Lectures on
Computer Science,
https://doi.org/10.1007/978-3-031-69974-0
115

116 References
13. Aristotle: On sophistical refutations: On Comin to be passing away - on the cosmos v. 3. Loeb
Classical Library. LOEB, London, England (1989)
14. Arora, S., Wu, S., Liu, E., Re, C.: Metadata shaping: A simple approach for knowledge-enhanced
language models. In: Findings of the Association for Computational Linguistics: ACL 2022, pp.
1733–1745. Association for Computational Linguistics, Dublin, Ireland (2022). DOI
https://doi.
org/10.18653/v1/2022.ﬁndings- acl.137.U R L https://aclanthology.org/2022.ﬁndings- acl.137
15. Ashley, K.D.: Arguing by analogy in law: A case-based model. In: Analogical reasoning:
Perspectives of artiﬁcial intelligence, cognitive science, and philosophy, pp. 205–224. Springer
(1988)
16. Assran, M., Duval, Q., Misra, I., Bojanowski, P ., Vincent, P ., Rabbat, M., LeCun, Y ., Ballas,
N.: Self-supervised learning from images with a joint-embedding predictive architecture. In:
Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, pp.
15619–15629 (2023)
17. Baker, C.F., Fillmore, C.J., Lowe, J.B.: The berkeley framenet project. In: 36th Annual Meet-
ing of the Association for Computational Linguistics and 17th International Conference on
Computational Linguistics, V olume 1, pp. 86–90 (1998)
18. Baker, C.L., Jara-Ettinger, J., Saxe, R., Tenenbaum, J.B.: Rational quantitative attribution of
beliefs, desires and percepts in human mentalizing. Nature Human Behaviour 1(4), 0064 (2017)
19. Banarescu, L., Bonial, C., Cai, S., Georgescu, M., Grifﬁtt, K., Hermjakob, U., Knight, K.,
Koehn, P ., Palmer, M., Schneider, N.: Abstract meaning representation for sembanking. In:
Proceedings of the 7th linguistic annotation workshop and interoperability with discourse, pp.
178–186 (2013)
20. Banerjee, P ., Baral, C.: Self-supervised knowledge triplet learning for zero-shot question
answering.
ArXiv:abs/2005.00316 (2020)
21. Bardasz, T., Zeid, I.: Dejavu: Case-based reasoning for mechanical design. AI EDAM 7(2),
111–124 (1993)
22. Barker, S.F.: The Elements of Logic. New York: Mcgraw-Hill (1965)
23. Barocas, S., Crawford, K., Shapiro, A., Wallach, H.: The problem with bias: Allocative versus
representational harms in machine learning. In: 9th Annual conference of the special interest
group for computing, information and society, p. 1. Philadelphia, PA, USA (2017)
24. Barrón-Cedeno, A., Jaradat, I., Da San Martino, G., Nakov, P .: Proppy: Organizing the news
based on their propagandistic content. Information Processing & Management 56(5), 1849–
1864 (2019)
25. Bauer, F., Richter, V .: Möglichkeiten und grenzen der nutzung von analogien und analogi-
eschlüssen. Ph. id Sch 18, 384–386 (1986)
26. Bauer, L., Wang, Y ., Bansal, M.: Commonsense for generative multi-hop question answering
tasks. arXiv preprint arXiv:1809.06309 (2018)
27. Bauer, L., Wang, Y ., Bansal, M.: Commonsense for generative multi-hop question answering
tasks. In: Proc. of EMNLP , pp. 4220–4230 (2018)
28. Bengio, Y ., Courville, A., Vincent, P .: Representation learning: A review and new perspectives.
IEEE transactions on pattern analysis and machine intelligence 35(8), 1798–1828 (2013)
29. Besta, M., Memedi, F., Zhang, Z., Gerstenberger, R., Blach, N., Nyczyk, P ., Copik, M.,
Kwa´sniewski, G., Müller, J., Gianinazzi, L., et al.: Demystifying chains, trees, and graphs
of thoughts. arXiv preprint arXiv:2401.14295 (2024)
30. Biotechnology, Council, B.S.R.: Past experience is invaluable for complex decision mak-
ing, brain research shows (2009). URL https://www.sciencedaily.com/releases/2009/05/
090513130930.htm
31. Bisk, Y ., Zellers, R., LeBras, R., Gao, J., Choi, Y .: Piqa: Reasoning about physical commonsense
in natural language. In: AAAI, pp. 7432–7439 (2020)

References 117
32. Black, S., Biderman, S., Hallahan, E., Anthony, Q., Gao, L., Golding, L., He, H., Leahy, C.,
McDonell, K., Phang, J., Pieler, M., Prashanth, U.S., Purohit, S., Reynolds, L., Tow, J., Wang,
B., Weinbach, S.: GPT-NeoX-20B: An open-source autoregressive language model. In: Pro-
ceedings of the ACL Workshop on Challenges & Perspectives in Creating Large Language
Models (2022). URL
https://arxiv.org/abs/2204.06745
33. Blodgett, S.L., Barocas, S., Daumé III, H., Wallach, H.: Language (technology) is power:
A critical survey of “bias” in NLP . In: D. Jurafsky, J. Chai, N. Schluter, J. Tetreault (eds.)
Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics, pp.
5454–5476. Association for Computational Linguistics, Online (2020). DOI
https://doi.org/10.
18653/v1/2020.acl-main.485.U R L https://aclanthology.org/2020.acl-main.485
34. Bolukbasi, T., Chang, K.W., Zou, J.Y ., Saligrama, V ., Kalai, A.T.: Man is to computer program-
mer as woman is to homemaker? debiasing word embeddings. Advances in neural information
processing systems 29 (2016)
35. Boratko, M., Li, X., O’Gorman, T., Das, R., Le, D., McCallum, A.: ProtoQA: A question answer-
ing dataset for prototypical common-sense reasoning. In: Proceedings of the 2020 Conference
on Empirical Methods in Natural Language Processing (EMNLP), pp. 1122–1136. Association
for Computational Linguistics, Online (2020). DOI https://doi.org/10.18653/v1/2020.emnlp-
main.85.U R L https://www.aclweb.org/anthology/2020.emnlp-main.85
36. Boratko, M., Li, X.L., Das, R., O’Gorman, T.J., Le, D., McCallum, A.: Protoqa: A question
answering dataset for prototypical common-sense reasoning. In: EMNLP (2020)
37. Bosselut, A., Rashkin, H., Sap, M., Malaviya, C., Celikyilmaz, A., Choi, Y .: COMET: Com-
monsense transformers for automatic knowledge graph construction. In: Proceedings of the
57th Annual Meeting of the Association for Computational Linguistics, pp. 4762–4779. Asso-
ciation for Computational Linguistics, Florence, Italy (2019). DOI
https://doi.org/10.18653/
v1/P19-1470.U R L https://aclanthology.org/P19-1470
38. Brendel, W., Rauber, J., Bethge, M.: Decision-based adversarial attacks: Reliable attacks against
black-box machine learning models. In: Proceedings of the 6th International Conference on
Learning Representations – ICLR 2018. OpenReview.net, V ancouver, BC, Canada (2018)
39. Bringsjord, S., Arkoudas, K., Bello, P .: Toward a general logicist methodology for engineering
ethically correct robots. IEEE Intelligent Systems 21(4), 38–44 (2006)
40. Browning, J., LeCun, Y .: Language, common sense, and the winograd schema challenge. Arti-
ﬁcial Intelligence p. 104031 (2023)
41. Brunner, T., Diehl, F., Le, M.T., Knoll, A.: Guessing smart: Biased sampling for efﬁcient
black-box adversarial attacks. In: Proceedings of the IEEE/CVF International Conference on
Computer Vision – ICCV 2019, pp. 4958–4966. IEEE, Seoul, South Korea (2019)
42. Bulathwela, S., Perez-Ortiz, M., Yilmaz, E., Shawe-Taylor, J.: Truelearn: A family of bayesian
algorithms to match lifelong learners to open educational resources. In: Proceedings of the
AAAI Conference on Artiﬁcial Intelligence, vol. 34, pp. 565–573 (2020)
43. Bulathwela, S., Pérez-Ortiz, M., Yilmaz, E., Shawe-Taylor, J.: Power to the learner: Towards
human-intuitive and integrative recommendations with open educational resources. Sustain-
ability 14(18), 11682 (2022)
44. Butler, T., O’Brien, L.: Artiﬁcial intelligence for regulatory compliance: Are we there yet?
Journal of Financial Compliance 3(1), 44–59 (2019)
45. Casati, R., V arzi, A.C., et al.: Parts and places: The structures of spatial representation. Mit
Press (1999)
46. Chalier, Y ., Razniewski, S., Weikum, G.: Joint reasoning for multi-faceted commonsense knowl-
edge. arXiv preprint
arXiv:2001.04170 (2020)
47. Chawla, K., Ramirez, J., Clever, R., Lucas, G., May, J., Gratch, J.: Casino: A corpus of camp-
site negotiation dialogues for automatic negotiation systems. arXiv preprint
arXiv:2103.15721
(2021)

118 References
48. Chen, E., Jiang, J., Chang, H.C.H., Muric, G., Ferrara, E., et al.: Charting the information and
misinformation landscape to characterize misinfodemics on social media: Covid-19 infodemi-
ology study at a planetary scale. Jmir Infodemiology 2(1), e32378 (2022)
49. Chen, H., Suhr, A., Misra, D., Snavely, N., Artzi, Y .: Touchdown: Natural language naviga-
tion and spatial reasoning in visual street environments. In: Proceedings of the IEEE/CVF
Conference on Computer Vision and Pattern Recognition, pp. 12538–12547 (2019)
50. Chen, K., Forbus, K., Srinivasan, B.V ., Chhaya, N., Usher, M.: Sketch recognition via part-
based hierarchical analogical learning. In: Proceedings of the Thirty-Second International Joint
Conference on Artiﬁcial Intelligence, pp. 2967–2974 (2023)
51. Chen, T.: Augmenting anomaly detection for autonomous vehicles with symbolic rules. Master’s
thesis, MIT (2019)
52. Chen, V ., S. Savage, R.: Evidence for a simplicity principle: teaching common complex
grapheme-to-phonemes improves reading and motivation in at-risk readers. Journal of Research
in Reading 37(2), 196–214 (2014). DOI
https://doi.org/10.1111/1467-9817.12022.U R L
https://onlinelibrary.wiley.com/doi/abs/10.1111/1467-9817.12022
53. Chhikara, P ., Zhang, J., Ilievski, F., Francis, J., Ma, K.: Knowledge-enhanced agents for inter-
active text games. In: K-CAP (2023)
54. Chiang, W.L., Li, Z., Lin, Z., Sheng, Y ., Wu, Z., Zhang, H., Zheng, L., Zhuang, S., Zhuang,
Y ., Gonzalez, J.E., et al.: Vicuna: An open-source chatbot impressing gpt-4 with 90%* chatgpt
quality. See https://vicuna lmsys. org (accessed 14 April 2023) (2023)
55. Chowdhery, A., Narang, S., Devlin, J., Bosma, M., Mishra, G., Roberts, A., Barham, P ., Chung,
H.W., Sutton, C., Gehrmann, S., et al.: Palm: Scaling language modeling with pathways. arXiv
preprint arXiv:2204.02311 (2022)
56. Chowdhury, S.N., Wickramarachchi, R., Gad-Elrab, M.H., Stepanova, D., Henson,
C.A.: Towards leveraging commonsense knowledge for autonomous driving. In: ISWC
(Posters/Demos/Industry) (2021)
57. Cobbe, K., Kosaraju, V ., Bavarian, M., Chen, M., Jun, H., Kaiser, L., Plappert, M., Tworek, J.,
Hilton, J., Nakano, R., et al.: Training veriﬁers to solve math word problems. arXiv preprint
arXiv:2110.14168 (2021)
58. Cook, M.B., Smallman, H.S.: Human factors of the conﬁrmation bias in intelligence analysis:
Decision support from graphical evidence landscapes. Human Factors 50(5), 745–754 (2008)
59. Côté, M.A., Kádár, A., Y uan, X., Kybartas, B., Barnes, T., Fine, E., Moore, J., Hausknecht,
M., El Asri, L., Adada, M., et al.: Textworld: A learning environment for text-based games. In:
Computer Games: 7th Workshop, CGW 2018, Held in Conjunction with IJCAI 2018 (2019)
60. Council of the European Union: Regulation (EU) 2022/2065 of the European Parliament and
of the Council of 19 October 2022 on a Single Market For Digital Services and amending
Directive 2000/31/EC (Digital Services Act) (Text with EEA relevance) (2022). URL
http://
data.europa.eu/eli/reg/2022/2065/oj. Document 32022R2065. Accessed: 2022-11-30
61. Crawford, K.: The atlas of AI: Power, politics, and the planetary costs of artiﬁcial intelligence.
Yale University Press (2021)
62. Curtis, R.V ., Reigeluth, C.M.: The use of analogies in written text. Instructional Science 13,
99–117 (1984)
63. Custers, B., Fosch-Villaronga, E.: Law and artiﬁcial intelligence: regulating AI and applying
AI in legal practice, vol. 35. Springer Nature (2022)
64. Czinczoll, T., Yannakoudakis, H., Mishra, P ., Shutova, E.: Scientiﬁc and creative analo-
gies in pretrained language models. In: Findings of the Association for Computational Lin-
guistics: EMNLP 2022, pp. 2094–2100. Association for Computational Linguistics, Abu
Dhabi, United Arab Emirates (2022). DOI https://doi.org/10.18653/v1/2022.ﬁndings- emnlp.
153.U R L https://aclanthology.org/2022.ﬁndings- emnlp.153

References 119
65. Da San Martino, G., Y u, S., Barrón-Cedeno, A., Petrov, R., Nakov, P .: Fine-grained analysis
of propaganda in news article. In: Proceedings of the 2019 conference on empirical methods
in natural language processing and the 9th international joint conference on natural language
processing (EMNLP-IJCNLP), pp. 5636–5646 (2019)
66. Daelemans, W., van den Bosch, A.: Memory-Based Language Processing. Studies in Natu-
ral Language Processing. Cambridge University Press (2005). DOI https://doi.org/10.1017/
CBO9780511486579
67. Das, A., Datta, S., Gkioxari, G., Lee, S., Parikh, D., Batra, D.: Embodied question answering.
In: Proceedings of the IEEE conference on computer vision and pattern recognition, pp. 1–10
(2018)
68. Das, A., Gupta, C., Kovatchev, V ., Lease, M., Li, J.J.: Prototex: Explaining model decisions
with prototype tensors. arXiv preprint arXiv:2204.05426 (2022)
69. Das, A., Gupta, C., Kovatchev, V ., Lease, M., Li, J.J.: ProtoTEx: Explaining model decisions
with prototype tensors. In: Proceedings of the 60th Annual Meeting of the Association for
Computational Linguistics (V olume 1: Long Papers), pp. 2986–2997. Association for Compu-
tational Linguistics, Dublin, Ireland (2022). DOI https://doi.org/10.18653/v1/2022.acl-long.
213.U R L https://aclanthology.org/2022.acl-long.213
70. Das, R., Godbole, A., Naik, A., Tower, E., Zaheer, M., Hajishirzi, H., Jia, R., McCallum, A.:
Knowledge base question answering by case-based reasoning over subgraphs. In: International
Conference on Machine Learning, pp. 4777–4793. PMLR (2022)
71. Davis, E.: Representations of commonsense knowledge. Morgan Kaufmann (2014)
72. Davis, E., Marcus, G.: Commonsense reasoning and commonsense knowledge in artiﬁcial
intelligence. Communications of the ACM 58(9), 92–103 (2015)
73. De Bono, E.: Lateral thinking. New York (1970)
74. De Saussure, L.: Manipulation and cognitive pragmatics. Manipulation and ideologies in the
twentieth century pp. 113–145 (2005)
75. De Vries, H., Shuster, K., Batra, D., Parikh, D., Weston, J., Kiela, D.: Talk the walk: Navigating
new york city through grounded dialogue. arXiv preprint arXiv:1807.03367 (2018)
76. De Weerd, H., V erbrugge, R., V erheij, B.: How much does it help to know what she knows you
know? an agent-based simulation study. Artiﬁcial Intelligence 199, 67–92 (2013)
77. Dehghani, M., Forbus, K.: Qcm: A qp-based concept map system. In: Proceedings of the 23nd
International Workshop on Qualitative Reasoning (2009)
78. Deng, X., Gu, Y ., Zheng, B., Chen, S., Stevens, S., Wang, B., Sun, H., Su, Y .: Mind2web:
Towards a generalist agent for the web. Advances in Neural Information Processing Systems
36 (2024)
79. Deshpande, D., Sourati, Z., Ilievski, F., Morstatter, F.: Contextualizing argument quality assess-
ment with relevant knowledge. Published in NAACL 2024
80. Devlin, J., Chang, M.W., Lee, K., Toutanova, K.: Bert: Pre-training of deep bidirectional trans-
formers for language understanding. arXiv preprint
arXiv:1810.04805 (2018)
81. DiResta, R., Grossman, S.: Potemkin pages & personas: Assessing gru online operations,
2014-2019. White Paper https://fsi-live s3. us-west-1. amazonaws. com/s3fs-public/potemkin-
pagespersonas-sio-wp. pdf (2019)
82. Doshi-V elez, F., Kim, B.: Towards a rigorous science of interpretable machine learning. arXiv
preprint arXiv:1702.08608 (2017)
83. Duit, R., et al.: On the role of analogies and metaphors in learning science. Science education
75(6), 649–672 (1991)
84. Emelin, D., Bras, R.L., Hwang, J.D., Forbes, M., Choi, Y .: Moral stories: Situated reasoning
about norms, intents, actions, and their consequences. arXiv preprint arXiv:2012.15738 (2020)

120 References
85. Eykholt, K., Evtimov, I., Fernandes, E., Li, B., Rahmati, A., Xiao, C., Prakash, A., Kohno, T.,
Son, D.: Robust physical-world attacks on deep learning visual classiﬁcation. In: Proceedings
of the 2018 IEEE/CVF Conference on Computer Vision and Pattern Recognition – CVPR 2018,
pp. 1625–1634. IEEE, Salt Lake City, UT, USA (2018). DOI https://doi.org/10.1109/CVPR.
2018.00175
86. Fadnis, K., Talamadupula, K., Kapanipathi, P ., Ishfaq, H., Roukos, S., Fokoue, A.: Heuristics
for interpretable knowledge graph contextualization. arXiv preprint
arXiv:1911.02085 (2019)
87. Fan, A., Lewis, M., Dauphin, Y .: Strategies for structuring story generation. arXiv preprint
arXiv:1902.01109 (2019)
88. Feldman, J.: The simplicity principle in human concept learning. Current Directions in Psycho-
logical Science 12(6), 227–232 (2003). DOI
https://doi.org/10.1046/j.0963-7214.2003.01267.
x.U R L https://doi.org/10.1046/j.0963-7214.2003.01267.x
89. Ferrara, E.: Genai against humanity: Nefarious applications of generative artiﬁcial intelligence
and large language models. Journal of Computational Social Science pp. 1–21 (2024)
90. Fersini, E., Gasparini, F., Rizzi, G., Saibene, A., Chulvi, B., Rosso, P ., Lees, A., Sorensen, J.:
Semeval-2022 task 5: Multimedia automatic misogyny identiﬁcation. In: Proceedings of the
16th International Workshop on Semantic Evaluation (SemEval-2022), pp. 533–549 (2022)
91. Forbes, M., Hwang, J.D., Shwartz, V ., Sap, M., Choi, Y .: Social chemistry 101: Learning to
reason about social and moral norms. arXiv preprint
arXiv:2011.00620 (2020)
92. Forbus, K., Usher, J., Lovett, A., Lockwood, K., Wetzel, J.: Cogsketch: Sketch understanding
for cognitive science research and for education. Topics in Cognitive Science 3(4), 648–666
(2011)
93. Forbus, K.D.: Qualitative process theory. Artiﬁcial intelligence 24(1-3), 85–168 (1984)
94. Forbus, K.D.: Qualitative reasoning. (1997)
95. Forbus, K.D., Ferguson, R.W., Usher, J.M.: Towards a computational model of sketching. In:
Proceedings of the 6th international conference on Intelligent user interfaces, pp. 77–83 (2001)
96. Francis, J.: Knowledge-enhanced representation learning for multiview context understanding.
Ph.D. thesis, Carnegie Mellon University (2022)
97. Francis, J., Kitamura, N., Labelle, F., Lu, X., Navarro, I., Oh, J.: Core challenges in embodied
vision-language planning. Journal of Artiﬁcial Intelligence Research 74, 459–515 (2022)
98. Frederiksen, B.: Applying expert system technology to code reuse with pyke. PyCon: Chicago
(2008)
99. Fromm, M., Berrendorf, M., Reiml, J., Mayerhofer, I., Bhargava, S., Faerman, E., Seidl, T.:
Towards a holistic view on argument quality prediction (2022)
100. Ganesh, B., Bright, J.: Countering extremists on social media: Challenges for strategic com-
munication and content moderation (2020)
101. Gao, B., Bian, J., Liu, T.Y .: Wordrep: A benchmark for research on learning word representa-
tions. arXiv preprint arXiv:1407.1640 (2014)
102. Gao, L., Madaan, A., Zhou, S., Alon, U., Liu, P ., Yang, Y ., Callan, J., Neubig, G.: Pal: Program-
aided language models. In: International Conference on Machine Learning, pp. 10764–10799.
PMLR (2023)
103. Gao, T., Yao, X., Chen, D.: Simcse: Simple contrastive learning of sentence embeddings (2021).
DOI
https://doi.org/10.48550/ARXIV .2104.08821.U R L https://arxiv.org/abs/2104.08821
104. Gardner, M., Merrill, W., Dodge, J., Peters, M.E., Ross, A., Singh, S., Smith, N.A.: Competency
problems: On ﬁnding and removing artifacts in language data. arXiv preprint arXiv:2104.08646
(2021)
105. Gentner, D.: Structure-mapping: A theoretical framework for analogy. Cognitive science 7(2),
155–170 (1983)
106. Gentner, D., Loewenstein, J., Thompson, L.: Learning and transfer: A general role for analogical
encoding. Journal of educational psychology 95(2), 393 (2003)

References 121
107. Gentner, D., Rattermann, M.J., Forbus, K.D.: The roles of similarity in transfer: Separating
retrievability from inferential soundness. Cognitive psychology 25(4), 524–575 (1993)
108. Gentner, D., Smith, L., Ramachandran, V .: Analogical reasoning, 2012. Encyclopedia of Human
Behavior, 2nd ed., VS Ramachandran, ed., Elsevier, Oxford, UK pp. 130–136
109. Geva, M., Goldberg, Y ., Berant, J.: Are we modeling the task or the annotator? an investigation
of annotator bias in natural language understanding datasets. arXiv preprint arXiv:1908.07898
(2019)
110. Gibson, E.J., Pick, A.D., et al.: An ecological approach to perceptual learning and development.
Oxford University Press, USA (2000)
111. Gibson, J.J.: The theory of affordances. Hilldale, USA 1(2), 67–82 (1977)
112. Gick, M.L., Holyoak, K.J.: Schema induction and analogical transfer. Cognitive psychology
15(1), 1–38 (1983)
113. Gillick, D., Presta, A., Tomar, G.S.: End-to-end retrieval in continuous space. CoRR
arXiv:abs/1811.08008 (2018). URL http://arxiv.org/abs/1811.08008
114. Gilpin, L.H., Ilievski, F.: Neuro-symbolic reasoning in the trafﬁc domain. Neuro-Symbolic AI
Journal
115. Gilpin, L.H., Penubarthi, V ., Kagal, L.: Explaining multimodal errors in autonomous vehicles.
In: 2021 IEEE 8th International Conference on Data Science and Advanced Analytics (DSAA),
pp. 1–10. IEEE (2021)
116. Gladkova, A., Drozd, A., Matsuoka, S.: Analogy-based detection of morphological and semantic
relations with word embeddings: what works and what doesn’t. In: Proceedings of the NAACL
Student Research Workshop, pp. 8–15 (2016)
117. Glynn, S.M., Britton, B.K., Semrud-Clikeman, M., Muth, K.D.: Analogical reasoning and
problem solving in science textbooks. Handbook of creativity pp. 383–398 (1989)
118. Goldberg, Y .: Two kinds of recall. arXiv preprint arXiv:2303.10527 (2023)
119. Goldwater, M.B., Schalk, L.: Relational categories as a bridge between cognitive and educa-
tional research. Psychological Bulletin 142(7), 729 (2016)
120. Gordon, A.S., Hobbs, J.R.: A formal theory of commonsense psychology: How people think
people think. Cambridge University Press (2017)
121. Gowal, S., Dvijotham, K., Stanforth, R., Bunel, R., Qin, C., Uesato, J., Arandjelovic, R., Mann,
T.A., Kohli, P .: Scalable veriﬁed training for provably robust image classiﬁcation. In: Pro-
ceedings of the IEEE/CVF International Conference on Computer Vision – ICCV 2019, pp.
4841–4850. IEEE, Seoul, South Korea (2019). DOI https://doi.org/10.1109/ICCV .2019.00494
122. Gowin, D.B.: Misconceptions, metaphors, and conceptual change: Once more with feeling. In:
Proceedings of the International Seminar on misconceptions in Science and Mathematics, pp.
39–41. Cornell University Ithaca, New York (1983)
123. Graham, J., Haidt, J., Koleva, S., Motyl, M., Iyer, R., Wojcik, S.P ., Ditto, P .H.: Moral founda-
tions theory: The pragmatic validity of moral pluralism. In: Advances in experimental social
psychology, vol. 47, pp. 55–130. Elsevier (2013)
124. Gray, M.E., Holyoak, K.J.: Teaching by analogy: From theory to practice. Mind, Brain, and
Education 15(3), 250–263 (2021)
125. Grice, H.P .: Logic and conversation. In: Speech acts, pp. 41–58. Brill (1975)
126. Grigorescu, S., Trasnea, B., Cocias, T., Macesanu, G.: A survey of deep learning techniques
for autonomous driving. Journal of Field Robotics 37(3), 362–386 (2020)
127. Grossi, D., Turrini, P .: Dependence in games and dependence games. Autonomous Agents and
Multi-Agent Systems 25, 284–312 (2012)
128. Gundapu, S., Mamidi, R.: Detection of propaganda techniques in visuo-lingual metaphor in
memes (2022). DOI https://doi.org/10.48550/ARXIV .2205.02937.U R L https://arxiv.org/abs/
2205.02937

122 References
129. Habib, H., Nithyanand, R.: Exploring the magnitude and effects of media inﬂuence on reddit
moderation. Proceedings of the International AAAI Conference on Web and Social Media
16(1), 275–286 (2022). DOI https://doi.org/10.1609/icwsm.v16i1.19291.U R L https://ojs.aaai.
org/index.php/ICWSM/article/view/19291
130. Halilaj, L., Dindorkar, I., Lüttin, J., Rothermel, S.: A knowledge graph-based approach for
situation comprehension in driving scenarios. In: European Semantic Web Conference, pp.
699–716. Springer (2021)
131. Hamilton, K.: Towards an ontology for propaganda detection in news articles. In: European
Semantic Web Conference, pp. 230–241. Springer (2021)
132. Han, J., Cheng, B., Lu, W.: Exploring task difﬁculty for few-shot relation extraction. In: Proceed-
ings of the 2021 Conference on Empirical Methods in Natural Language Processing, pp. 2605–
2616. Association for Computational Linguistics, Online and Punta Cana, Dominican Repub-
lic (2021). DOI https://doi.org/10.18653/v1/2021.emnlp-main.204.U R L https://aclanthology.
org/2021.emnlp-main.204
133. Harvey, G.: A brief guide to the elements of the academic essay. Harvard College Writing
Program (2009)
134. Hase, P ., Bansal, M.: Evaluating explainable AI: Which algorithmic explanations help users
predict model behavior? In: D. Jurafsky, J. Chai, N. Schluter, J. Tetreault (eds.) Proceedings
of the 58th Annual Meeting of the Association for Computational Linguistics, pp. 5540–5552.
Association for Computational Linguistics, Online (2020). DOI https://doi.org/10.18653/v1/
2020.acl-main.491.U R L https://aclanthology.org/2020.acl-main.491
135. Hase, P ., Chen, C., Li, O., Rudin, C.: Interpretable image recognition with hierarchical proto-
types. In: Proceedings of the AAAI Conference on Human Computation and Crowdsourcing,
vol. 7, pp. 32–40 (2019)
136. Hase, P ., Zhang, S., Xie, H., Bansal, M.: Leakage-adjusted simulatability: Can models generate
non-trivial explanations of their behavior in natural language? arXiv preprint arXiv:2010.04119
(2020)
137. Hayes, P .J.: The naive physics manifesto. In: M.A. Boden (ed.) The Philosophy of Artiﬁcial
Intelligence, Oxford readings in philosophy, pp. 171–205. Oxford University Press (1990)
138. Hendrycks, D., Burns, C., Basart, S., Zou, A., Mazeika, M., Song, D., Steinhardt, J.: Measuring
massive multitask language understanding. arXiv preprint arXiv:2009.03300 (2020)
139. Hendrycks, D., Mazeika, M., Zou, A., Patel, S., Zhu, C., Navarro, J., Song, D., Li, B., Stein-
hardt, J.: What would jiminy cricket do? towards agents that behave morally. arXiv preprint
arXiv:2110.13136 (2021)
140. Hofstadter, D.R.: Analogy as the core of cognition. The analogical mind: Perspectives from
cognitive science pp. 499–538 (2001)
141. Holyoak, K.J.: Analogy and relational reasoning. In: K.J. Holyoak, R.G. Morrison (eds.) Oxford
handbook of thinking and reasoning. Oxford University Press, New York (2012)
142. Holyoak, K.J.: The spider’s thread: Metaphor in mind, brain, and poetry. MIT Press (2019)
143. Holyoak, K.J., Thagard, P .: Mental leaps: Analogy in creative thought. MIT press (1996)
144. Hong, D., Baek, S.S., Wang, T.: Interpretable sequence classiﬁcation via prototype trajectory.
arXiv preprint arXiv:2007.01777 (2020)
145. Hong, D., Baek, S.S., Wang, T.: Interpretable sequence classiﬁcation via prototype trajectory
(2021)
146. How, M.L., Chan, Y .J.: Artiﬁcial intelligence-enabled predictive insights for ameliorating global
malnutrition: a human-centric ai-thinking approach. AI 1(1), 4 (2020)
147. Hu, Y ., Xie, Q., Jain, V ., Francis, J., Patrikar, J., Keetha, N., Kim, S., Xie, Y ., Zhang, T., Zhao,
Z., et al.: Toward general-purpose robots via foundation models: A survey and meta-analysis.
arXiv preprint
arXiv:2312.08782 (2023)

References 123
148. Hung, H., Gedik, E., Quiros, L.C.: Complex conversational scene analysis using wearable
sensors. In: Multimodal Behavior Analysis in the Wild, pp. 225–245. Elsevier (2019)
149. Ilievski, F., Ma, K., Oltramari, A., Wang, P ., Pujara, J.: Building robust and explainable ai with
commonsense knowledge graphs and neural models. Compendium of Neurosymbolic Artiﬁcial
Intelligence 369, 178 (2023)
150. Ilievski, F., Oltramari, A., Ma, K., Zhang, B., McGuinness, D.L., Szekely, P .: Dimensions of
commonsense knowledge. Knowledge-Based Systems (KBS) (2021)
151. Ilievski, F., Pujara, J., Zhang, H.: Story generation with commonsense knowledge graphs and
axioms. In: Workshop on Commonsense Reasoning and Knowledge Bases (2021)
152. Ilievski, F., Szekely, P ., Zhang, B.: Cskg: The commonsense knowledge graph. In: Extended
Semantic Web Conference (ESWC) (2021)
153. Jacob, S., Shani, C., Shahaf, D.: Fame: Flexible, scalable analogy mappings engine. arXiv
preprint
arXiv:2311.01860 (2023)
154. Jang, M., Kwon, D.S., Lukasiewicz, T.: Becel: Benchmark for consistency evaluation of lan-
guage models. In: Proceedings of the 29th International Conference on Computational Linguis-
tics, pp. 3680–3696 (2022)
155. Jara-Ettinger, J.: Theory of mind as inverse reinforcement learning. Current Opinion in Behav-
ioral Sciences 29, 105–110 (2019)
156. Jia, R., Liang, P .: Adversarial examples for evaluating reading comprehension systems. In:
Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing,
pp. 2021–2031. Association for Computational Linguistics, Copenhagen, Denmark (2017).
DOI
https://doi.org/10.18653/v1/D17-1215.U R L https://aclanthology.org/D17-1215
157. Jiang, L., Hwang, J.D., Bhagavatula, C., Bras, R.L., Liang, J., Dodge, J., Sakaguchi, K., Forbes,
M., Borchardt, J., Gabriel, S., et al.: Can machines learn morality? the delphi experiment. arXiv
preprint arXiv:2110.07574 (2021)
158. Jiang, S., Metzger, M., Flanagin, A., Wilson, C.: Modeling and measuring expressed (dis)belief
in (mis)information. Proceedings of the International AAAI Conference on Web and Social
Media 14, 315–326 (2020). URL
https://ojs.aaai.org/index.php/ICWSM/article/view/7302
159. Jiang, Y ., Gupta, A., Zhang, Z., Wang, G., Dou, Y ., Chen, Y ., Fei-Fei, L., Anandkumar, A., Zhu,
Y ., Fan, L.: Vima: General robot manipulation with multimodal prompts. arXiv (2022)
160. Jiang, Y ., Ilievski, F., Ma, K.: Brainteaser: Lateral thinking puzzles for large language model.
In: EMNLP (2023)
161. Jiang, Y ., Ilievski, F., Ma, K.: Transferring procedural knowledge across commonsense tasks.
In: European Conference on Artiﬁcial Intelligence (ECAI) (2023)
162. Jiayang, C., Qiu, L., Chan, T.H., Fang, T., Wang, W., Chan, C., Ru, D., Guo, Q., Zhang, H.,
Song, Y ., et al.: Storyanalogy: Deriving story-level analogies from large language models to
unlock analogical understanding. arXiv preprint
arXiv:2310.12874 (2023)
163. Johansen, M.K., Kruschke, J.K.: Category representation for classiﬁcation and feature infer-
ence. J. Exp. Psychol. Learn. Mem. Cogn. 31(6), 1433–1458 (2005)
164. Johnson, R.L., Pistilli, G., Menédez-González, N., Duran, L.D.D., Panai, E., Kalpokiene, J.,
Bertulfo, D.J.: The ghost in the machine has an american accent: value conﬂict in gpt-3. arXiv
preprint
arXiv:2203.07785 (2022)
165. Joshi, S., Ilievski, F., Luceri, L.: Contextualizing internet memes across social media platforms.
arXiv preprint arXiv:2311.11157 (2023)
166. Jurgens, D., Mohammad, S., Turney, P ., Holyoak, K.: SemEval-2012 task 2: Measuring degrees
of relational similarity. In: *SEM 2012: The First Joint Conference on Lexical and Compu-
tational Semantics – V olume 1: Proceedings of the main conference and the shared task, and
V olume 2: Proceedings of the Sixth International Workshop on Semantic Evaluation (SemEval
2012), pp. 356–364. Association for Computational Linguistics, Montréal, Canada (2012). URL
https://aclanthology.org/S12-1047

124 References
167. Kahneman, D.: Thinking, fast and slow. macmillan (2011)
168. Kahneman, D., Frederick, S., et al.: Representativeness revisited: Attribute substitution in intu-
itive judgment. Heuristics and biases: The psychology of intuitive judgment 49(49-81), 74
(2002)
169. Kant, I.: Groundwork for the Metaphysics of Morals. Yale University Press (1785/2002)
170. Kapanipathi, P ., Thost, V ., Patel, S.S., Whitehead, S., Abdelaziz, I., Balakrishnan, A., Chang,
M., Fadnis, K., Gunasekara, C., Makni, B., et al.: Infusing knowledge into the textual entailment
task using graph convolutional networks. arXiv preprint
arXiv:1911.02060 (2019)
171. Karpukhin, V ., O˘guz, B., Min, S., Lewis, P ., Wu, L., Edunov, S., Chen, D., Yih, W.t.: Dense
passage retrieval for open-domain question answering. arXiv preprint arXiv:2004.04906 (2020)
172. Keane, M.T., Kenny, E.M.: How case-based reasoning explains neural networks: A theoretical
analysis of xai using post-hoc explanation-by-example from a survey of ann-cbr twin-systems.
In: Case-Based Reasoning Research and Development: 27th International Conference, ICCBR
2019, Otzenhausen, Germany, September 8–12, 2019, Proceedings 27, pp. 155–171. Springer
(2019)
173. Keysers, D., Schärli, N., Scales, N., Buisman, H., Furrer, D., Kashubin, S., Momchev, N.,
Sinopalnikov, D., Staﬁniak, L., Tihon, T., et al.: Measuring compositional generalization: A
comprehensive method on realistic data. In: International Conference on Learning Representa-
tions (2019)
174. Khan, I.: Disinformation and freedom of opinion and expression (2021). URL
https://documents-dds-ny.un.org/doc/UNDOC/GEN/G21/085/64/PDF/G2108564.pdf.
Undocs.org/en/A/HRC/47/25. Accessed: 2022-11-30
175. Khashabi, D., Kordi, Y ., Hajishirzi, H.: Uniﬁedqa-v2: Stronger generalization via broader cross-
format training. arXiv preprint
arXiv:2202.12359 (2022)
176. Kiela, D., Firooz, H., Mohan, A., Goswami, V ., Singh, A., Ringshia, P ., Testuggine, D.: The
hateful memes challenge: Detecting hate speech in multimodal memes (2021)
177. Kimmig, A., Bach, S., Broecheler, M., Huang, B., Getoor, L.: A short introduction to probabilis-
tic soft logic. In: Proceedings of the NIPS workshop on probabilistic programming: foundations
and applications, pp. 1–4 (2012)
178. Kosinski, M.: Theory of mind may have spontaneously emerged in large language models.
arXiv preprint
arXiv:2302.02083 (2023)
179. Kotchian, V ., Simmons, C.: SSA T &; Isee for dummies. John Wiley &; Sons, Inc. (2012)
180. Krawczyk, D.C., Morrison, R.G., Viskontas, I., Holyoak, K.J., Chow, T.W., Mendez, M.F.,
Miller, B.L., Knowlton, B.J.: Distraction during relational reasoning: The role of prefrontal
cortex in interference control. Neuropsychologia 46(7), 2020–2032 (2008)
181. Krishna, R., Zhu, Y ., Groth, O., Johnson, J., Hata, K., Kravitz, J., Chen, S., Kalantidis, Y ., Li,
L.J., Shamma, D.A., et al.: Visual genome: Connecting language and vision using crowdsourced
dense image annotations. International journal of computer vision 123(1), 32–73 (2017)
182. Kumar, S., Talukdar, P .: Nile: Natural language inference with faithful natural language expla-
nations. arXiv preprint arXiv:2005.12116 (2020)
183. Lamond, G.: Precedent and analogy in legal reasoning (2006)
184. Lan, A.S., Studer, C., Baraniuk, R.G.: Time-varying learning and content analytics via sparse
factor analysis. In: Proceedings of the 20th ACM SIGKDD international conference on Knowl-
edge discovery and data mining, pp. 452–461 (2014)
185. Lazer, D.M., Baum, M.A., Benkler, Y ., Berinsky, A.J., Greenhill, K.M., Menczer, F., Metzger,
M.J., Nyhan, B., Pennycook, G., Rothschild, D., et al.: The science of fake news. Science
359(6380), 1094–1096 (2018)
186. Lee, H., Hong, S., Park, J., Kim, T., Cha, M., Choi, Y ., Kim, B.P ., Kim, G., Lee, E.J., Lim,
Y ., et al.: Square: A large-scale dataset of sensitive questions and acceptable responses created
through human-machine collaboration. arXiv preprint
arXiv:2305.17696 (2023)

References 125
187. Lei, B., Liao, C., Ding, C., et al.: Boosting logical reasoning in large language models through
a new framework: The graph of thought. arXiv preprint arXiv:2308.08614 (2023)
188. Lenat, D.: The dimensions of context-space (1998)
189. Lenat, D.B.: Cyc: A large-scale investment in knowledge infrastructure. Communications of
the ACM 38(11), 33–38 (1995)
190. Lewis, M., Liu, Y ., Goyal, N., Ghazvininejad, M., Mohamed, A., Levy, O., Stoyanov, V .,
Zettlemoyer, L.: BART: Denoising sequence-to-sequence pre-training for natural language
generation, translation, and comprehension. In: Proceedings of the 58th Annual Meeting of
the Association for Computational Linguistics, pp. 7871–7880. Association for Computational
Linguistics, Online (2020). DOI
https://doi.org/10.18653/v1/2020.acl-main.703.U R L https://
www.aclweb.org/anthology/2020.acl-main.703
191. Li, H., Gong, Y ., Jiao, J., Zhang, R., Baldwin, T., Duan, N.: Kfcnet: Knowledge ﬁlter-
ing and contrastive learning network for generative commonsense reasoning. arXiv preprint
arXiv:2109.06704 (2021)
192. Li, O., Liu, H., Chen, C., Rudin, C.: Deep learning for case-based reasoning through proto-
types: A neural network that explains its predictions. In: Proceedings of the Thirty-Second
AAAI Conference on Artiﬁcial Intelligence and Thirtieth Innovative Applications of Artiﬁcial
Intelligence Conference and Eighth AAAI Symposium on Educational Advances in Artiﬁcial
Intelligence, AAAI’18/IAAI’18/EAAI’18. AAAI Press (2018)
193. Li, X., Taheri, A., Tu, L., Gimpel, K.: Commonsense knowledge base completion. In: Proceed-
ings of the 54th Annual Meeting of the Association for Computational Linguistics (V olume 1:
Long Papers), pp. 1445–1455 (2016)
194. Li, X.L., Liang, P .: Preﬁx-tuning: Optimizing continuous prompts for generation (2021)
195. Lin, B.Y ., Chen, X., Chen, J., Ren, X.: KagNet: Knowledge-aware graph networks for com-
monsense reasoning. In: Proceedings of the 2019 Conference on Empirical Methods in Natural
Language Processing and the 9th International Joint Conference on Natural Language Pro-
cessing (EMNLP-IJCNLP), pp. 2829–2839. Association for Computational Linguistics, Hong
Kong, China (2019). DOI
https://doi.org/10.18653/v1/D19-1282.U R L https://www.aclweb.
org/anthology/D19-1282
196. Lin, B.Y ., Fu, Y ., Yang, K., Ammanabrolu, P ., Brahman, F., Huang, S., Bhagavatula, C., Choi,
Y ., Ren, X.: Swiftsage: A generative agent with fast and slow thinking for complex interactive
tasks. arXiv preprint
arXiv:2305.17390 (2023)
197. Lin, B.Y ., Lee, S., Khanna, R., Ren, X.: Birds have four legs?! NumerSense: Probing Numer-
ical Commonsense Knowledge of Pre-Trained Language Models. In: Proceedings of the 2020
Conference on Empirical Methods in Natural Language Processing (EMNLP), pp. 6862–6868.
Association for Computational Linguistics, Online (2020). DOI
https://doi.org/10.18653/v1/
2020.emnlp-main.557.U R L https://www.aclweb.org/anthology/2020.emnlp-main.557
198. Lin, B.Y ., Zhou, W., Shen, M., Zhou, P ., Bhagavatula, C., Choi, Y ., Ren, X.: Commongen: A
constrained text generation challenge for generative commonsense reasoning. arXiv preprint
arXiv:1911.03705 (2019)
199. Lin, B.Y ., Zhou, W., Shen, M., Zhou, P ., Bhagavatula, C., Choi, Y ., Ren, X.: CommonGen:
A constrained text generation challenge for generative commonsense reasoning. In: Findings
of the Association for Computational Linguistics: EMNLP 2020, pp. 1823–1840. Association
for Computational Linguistics, Online (2020). URL
https://www.aclweb.org/anthology/2020.
ﬁndings- emnlp.165
200. Ling, C., AbuHilal, I., Blackburn, J., De Cristofaro, E., Zannettou, S., Stringhini, G.: Dissecting
the meme magic: Understanding indicators of virality in image memes. Proceedings of the ACM
on Human-Computer Interaction 5(CSCW1), 1–24 (2021)
201. Lipton, Z.C.: The mythos of model interpretability: In machine learning, the concept of inter-
pretability is both important and slippery. Queue 16(3), 31–57 (2018)

126 References
202. Liu, B., Jiang, Y ., Zhang, X., Liu, Q., Zhang, S., Biswas, J., Stone, P .: Llm+ p: Empowering large
language models with optimal planning proﬁciency. arXiv preprint arXiv:2304.11477 (2023)
203. Liu, H., Singh, P .: Conceptnet-a practical commonsense reasoning tool-kit. BT technology
journal 22(4), 211–226 (2004)
204. Liu, P ., Fu, J., Xiao, Y ., Y uan, W., Chang, S., Dai, J., Liu, Y ., Ye, Z., Dou, Z.Y ., Neubig, G.:
ExplainaBoard: An Explainable Leaderboard for NLP . In: Annual Meeting of the Association
for Computational Linguistics (ACL), System Demonstrations (2021)
205. Liu, S., Spelke, E.S.: Six-month-old infants expect agents to minimize the cost of their actions.
Cognition 160, 35–42 (2017)
206. Liu, W., Zhou, P ., Zhao, Z., Wang, Z., Ju, Q., Deng, H., Wang, P .: K-bert: Enabling language rep-
resentation with knowledge graph (2019). DOI https://doi.org/10.48550/ARXIV .1909.07606.
URL https://arxiv.org/abs/1909.07606
207. Liu, Y ., Ott, M., Goyal, N., Du, J., Joshi, M., Chen, D., Levy, O., Lewis, M., Zettlemoyer, L.,
Stoyanov, V .: Roberta: A robustly optimized bert pretraining approach (2019)
208. Liu, Y ., Wan, Y ., He, L., Peng, H., Y u, P .S.: Kg-bart: Knowledge graph-augmented bart for
generative commonsense reasoning. arXiv preprint
arXiv:2009.12677 (2020)
209. Lourie, N., Le Bras, R., Bhagavatula, C., Choi, Y .: Unicorn on rainbow: A universal common-
sense reasoning model on a new multitask benchmark. In: Proceedings of the AAAI Conference
on Artiﬁcial Intelligence, vol. 35, pp. 13480–13488 (2021)
210. Lourie, N., Le Bras, R., Choi, Y .: Scruples: A corpus of community ethical judgments on 32,000
real-life anecdotes. In: Proceedings of the AAAI Conference on Artiﬁcial Intelligence, vol. 35,
pp. 13470–13479 (2021)
211. Luceri, L., Cresci, S., Giordano, S.: Social media against society. The Internet and the 2020
Campaign p. 1 (2021)
212. Luceri, L., Giordano, S., Ferrara, E.: Detecting troll behavior via inverse reinforcement learning:
A case study of russian trolls in the 2016 us election. Proceedings of the International AAAI
Conference on Web and Social Media 14, 417–427 (2020). URL https://ojs.aaai.org/index.php/
ICWSM/article/view/7311
213. Lundberg, S.M., Lee, S.I.: A uniﬁed approach to interpreting model predictions. In: Proceedings
of the 31st international conference on neural information processing systems, pp. 4768–4777
(2017)
214. Ma, K., Francis, J., Lu, Q., Nyberg, E., Oltramari, A.: Towards generalizable neuro-symbolic
systems for commonsense question answering. In: Proceedings of the First Workshop on
Commonsense Inference in Natural Language Processing, pp. 22–32. Association for Com-
putational Linguistics, Hong Kong, China (2019). DOI
https://doi.org/10.18653/v1/D19-6003.
URL https://www.aclweb.org/anthology/D19-6003
215. Ma, K., Ilievski, F., Francis, J., Bisk, Y ., Nyberg, E., Oltramari, A.: Knowledge-driven data
construction for zero-shot evaluation in commonsense question answering. In: AAAI (2021)
216. Ma, K., Ilievski, F., Francis, J., Bisk, Y ., Nyberg, E., Oltramari, A.: Knowledge-driven data
construction for zero-shot evaluation in commonsense question answering. In: AAAI (2021)
217. Ma, K., Ilievski, F., Francis, J., Nyberg, E., Oltramari, A.: Coalescing global and local infor-
mation for procedural text understanding. In: COLING (2022)
218. Ma, K., Ilievski, F., Francis, J., Ozaki, S., Nyberg, E., Oltramari, A.: Exploring strategies for
generalizable commonsense reasoning with pre-trained models. EMNLP 2021 (2021)
219. Magazine, A.I.: Computers don’t have common sense, dr oren etzioni (2022). URL https://
www.youtube.com/watch?v=XTn9zAxXj00
220. Mamié, R., Horta Ribeiro, M., West, R.: Are anti-feminist communities gateways to the far
right? evidence from reddit and youtube. In: 13th ACM Web Science Conference 2021, pp.
139–147 (2021)

References 127
221. Mani, I.: Computational modeling of narrative. Morgan & Claypool Publishers (2013)
222. Marasovi´c, A., Beltagy, I., Downey, D., Peters, M.E.: Few-shot self-rationalization with natural
language prompts. NAACL (2022)
223. Marcus, G., Davis, E.: Rebooting AI: Building artiﬁcial intelligence we can trust. Vintage
(2019)
224. Marino, G.: Semiotics of spreadability: A systematic approach to internet memes and virality
(2015)
225. Marshall, A., Davies, A.: Uber’s Self-Driving Car Saw the Woman It Killed, Report Says.
https://www.wired.com/story/uber-self-driving-crash-arizona-ntsb-report/
226. McCarthy, J.: Artiﬁcial intelligence, logic, and formalising common sense. Machine Learning
and the City: Applications in Architecture and Urban Design pp. 69–90 (2022)
227. Medin, D.L., Schaffer, M.M.: Context theory of classiﬁcation learning. Psychol. Rev. 85(3),
207–238 (1978)
228. Mehrabi, N., Morstatter, F., Saxena, N., Lerman, K., Galstyan, A.: A survey on bias and fairness
in machine learning. ACM computing surveys (CSUR) 54(6), 1–35 (2021)
229. Mehrabi, N., Zhou, P ., Morstatter, F., Pujara, J., Ren, X., Galstyan, A.: Lawyers are dishonest?
quantifying representational harms in commonsense knowledge resources. In: M.F. Moens,
X. Huang, L. Specia, S.W.t. Yih (eds.) Proceedings of the 2021 Conference on Empirical
Methods in Natural Language Processing, pp. 5016–5033. Association for Computational Lin-
guistics, Online and Punta Cana, Dominican Republic (2021). DOI https://doi.org/10.18653/
v1/2021.emnlp-main.410.U R L https://aclanthology.org/2021.emnlp-main.410
230. Melotte, S., Ilievski, F., Zhang, L., Malte, A., Mutha, N., Morstatter, F., Mehrabi, N.: Where
does bias in common sense knowledge models come from? IEEE Internet Computing 26(4),
12–20 (2022)
231. Meng, S., Hu, X., Liu, A., Li, S., Ma, F., Yang, Y ., Wen, L.: RAPL: A Relation-Aware Pro-
totype Learning Approach for Few-Shot Document-Level Relation Extraction. arXiv preprint
arXiv:2310.15743 (2023)
232. Metcalfe, J.S., Perelman, B.S., Boothe, D.L., Mcdowell, K.: Systemic oversimpliﬁcation limits
the potential for human-ai partnership. IEEE Access 9, 70242–70260 (2021)
233. Mihaylov, T., Frank, A.: Knowledgeable reader: Enhancing cloze-style reading comprehension
with external commonsense knowledge. arXiv preprint arXiv:1805.07858 (2018)
234. Mikolov, T., Chen, K., Corrado, G., Dean, J.: Efﬁcient estimation of word representations in
vector space. arXiv preprint
arXiv:1301.3781 (2013)
235. Mikolov, T., Sutskever, I., Chen, K., Corrado, G.S., Dean, J.: Distributed representations of
words and phrases and their compositionality. Advances in neural information processing sys-
tems 26 (2013)
236. Mikolov, T., Yih, W.t., Zweig, G.: Linguistic regularities in continuous space word representa-
tions. In: Proceedings of the 2013 Conference of the North American Chapter of the Association
for Computational Linguistics: Human Language Technologies, pp. 746–751. Association for
Computational Linguistics, Atlanta, Georgia (2013). URL
https://aclanthology.org/N13-1090
237. Miller, G.A.: Wordnet: a lexical database for english. Communications of the ACM 38(11),
39–41 (1995)
238. Miller, T.: Explanation in artiﬁcial intelligence: Insights from the social sciences. Artiﬁcial
intelligence 267, 1–38 (2019)
239. Min, S., Lyu, X., Holtzman, A., Artetxe, M., Lewis, M., Hajishirzi, H., Zettlemoyer, L.:
Rethinking the role of demonstrations: What makes in-context learning work? arXiv preprint
arXiv:2202.12837 (2022)
240. Ming, Y ., Xu, P ., Qu, H., Ren, L.: Interpretable and steerable sequence learning via prototypes.
In: Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery

128 References
& Data Mining. ACM (2019). DOI https://doi.org/10.1145/3292500.3330908.U R L https://
doi.org/10.1145/3292500.3330908
241. Misra, D., Bennett, A., Blukis, V ., Niklasson, E., Shatkhin, M., Artzi, Y .: Mapping instructions
to actions in 3d environments with visual goal prediction. arXiv preprint arXiv:1809.00786
(2018)
242. Mitchell, T., Cohen, W., Hruschka, E., Talukdar, P ., Yang, B., Betteridge, J., Carlson, A., Dalvi,
B., Gardner, M., Kisiel, B., et al.: Never-ending learning. Communications of the ACM 61(5),
103–115 (2018)
243. Mitsuhara, M., Fukui, H., Sakashita, Y ., Ogata, T., Hirakawa, T., Yamashita, T., Fujiyoshi,
H.: Embedding human knowledge into deep neural network via attention map. arXiv preprint
arXiv:1905.03540 (2019)
244. Mollas, I., Bassiliades, N., Tsoumakas, G.: Truthful meta-explanations for local interpretability
of machine learning models. Applied Intelligence 53(22), 26927–26948 (2023)
245. Moradi, M., Samwald, M.: Evaluating the robustness of neural language models to input per-
turbations (2021)
246. Morris, J.X., Liﬂand, E., Yoo, J.Y ., Grigsby, J., Jin, D., Qi, Y .: Textattack: A framework
for adversarial attacks, data augmentation, and adversarial training in nlp. arXiv preprint
arXiv:2005.05909 (2020)
247. Morrow, G., Swire-Thompson, B., Polny, J.M., Kopec, M., Wihbey, J.P .: The emerging science
of content labeling: Contextualizing social media content moderation. Journal of the Association
for Information Science and Technology 73(10), 1365–1386 (2022)
248. Mostafazadeh, N., Chambers, N., He, X., Parikh, D., Batra, D., V anderwende, L., Kohli, P .,
Allen, J.: A corpus and cloze evaluation for deeper understanding of commonsense stories. In:
Proceedings of the 2016 Conference of the North American Chapter of the Association for
Computational Linguistics: Human Language Technologies, pp. 839–849 (2016)
249. Mostafazadeh, N., Chambers, N., He, X., Parikh, D., Batra, D., V anderwende, L., Kohli, P .,
Allen, J.: A corpus and cloze evaluation for deeper understanding of commonsense stories.
In: Proceedings of the 2016 Conference of the North American Chapter of the Association
for Computational Linguistics: Human Language Technologies, pp. 839–849. Association for
Computational Linguistics, San Diego, California (2016). DOI
https://doi.org/10.18653/v1/
N16-1098.U R L https://www.aclweb.org/anthology/N16-1098
250. Mulyati, Y ., , and, D.H.: Enhancing argumentative writing via online peer feedback-based
essay: A quasi-experiment study. International Journal of Instruction 16(2), 195–212 (2023).
DOI
https://doi.org/10.29333/iji.2023.16212a.U R L https://doi.org/10.29333/iji.2023.16212a
251. Muppalla, R., Lalithsena, S., Banerjee, T., Sheth, A.: A knowledge graph framework for detect-
ing trafﬁc events using stationary cameras. In: Proceedings of the 2017 ACM on Web Science
Conference, pp. 431–436 (2017)
252. Muthukrishna, M.: A Theory of Everyone: The New Science of Who We Are, How We Got
Here, and Where We’re Going. MIT Press (2023)
253. Nadeem, M., Bethke, A., Reddy, S.: StereoSet: Measuring stereotypical bias in pretrained lan-
guage models. In: C. Zong, F. Xia, W. Li, R. Navigli (eds.) Proceedings of the 59th Annual
Meeting of the Association for Computational Linguistics and the 11th International Joint Con-
ference on Natural Language Processing (V olume 1: Long Papers), pp. 5356–5371. Association
for Computational Linguistics, Online (2021). DOI
https://doi.org/10.18653/v1/2021.acl-long.
416.U R L https://aclanthology.org/2021.acl-long.416
254. Nagarajah, T., Ilievski, F., Pujara, J.: Understanding narratives through dimensions of analogy
(2022)
255. Namkhah, Z., Fatemi, S.F., Mansoori, A., Nosratabadi, S., Ghayour-Mobarhan, M., Sobhani,
S.R.: Advancing sustainability in the food and nutrition system: a review of artiﬁcial intelligence
applications. Frontiers in Nutrition 10 (2023)

References 129
256. Narang, S., Raffel, C., Lee, K., Roberts, A., Fiedel, N., Malkan, K.: Wt5?! training text-to-text
models to explain their predictions. arXiv preprint arXiv:2004.14546 (2020)
257. Nauta, M., Jutte, A., Provoost, J., Seifert, C.: This looks like that, because ... explaining pro-
totypes for interpretable image recognition. In: Communications in Computer and Information
Science, pp. 441–456. Springer International Publishing (2021)
258. Nguyen, T.P ., Razniewski, S., Romero, J., Weikum, G.: Reﬁned commonsense knowledge from
large-scale web contents. IEEE Transactions on Knowledge and Data Engineering (2022)
259. Nguyen, T.P ., Razniewski, S., Weikum, G.: Multi-cultural commonsense knowledge distillation.
arXiv preprint arXiv:2402.10689 (2024)
260. Nickerson, R.S.: Biases, Misconceptions, and the Like, p. 208-262. Cambridge University Press
(2020). DOI
https://doi.org/10.1017/9781108892032.008
261. Nogara, G., Vishnuprasad, P .S., Cardoso, F., Ayoub, O., Giordano, S., Luceri, L.: The disinfor-
mation dozen: An exploratory analysis of covid-19 disinformation proliferation on twitter. In:
14th ACM Web Science Conference 2022, pp. 348–358 (2022)
262. Oltramari, A., Francis, J., Henson, C., Ma, K., Wickramarachchi, R.: Neuro-symbolic architec-
tures for context understanding. arXiv preprint
arXiv:2003.04707 (2020)
263. Onyeka, E., V arde, A., Anu, V ., Tandon, N., Daramola, O.: Using commonsense knowledge and
text mining for implicit requirements localization. 2020 IEEE 32nd International Conference
on Tools with Artiﬁcial Intelligence (ICTAI) pp. 935–940 (2020)
264. OpenAI: Chatgpt. https://openai.com/blog/chatgpt (2022). Accessed: April 30, 2023
265. OpenAI, R.: Gpt-4 technical report. arXiv pp. 2303–08774 (2023)
266. Ortiz, D., Gilpin, L.H., Cardena, A.A.: Semi-automated synthesis of driving rules. Symposium
on V ehicle Security and Privacy (V ehicleSec) (2023)
267. Oyelade, O.N., Ezugwu, A.E.: A case-based reasoning framework for early detection and diag-
nosis of novel coronavirus. Informatics in Medicine Unlocked 20, 100395 (2020). DOI
https://
doi.org/10.1016/j.imu.2020.100395.U R L https://www.sciencedirect.com/science/article/pii/
S2352914820303683
268. Pan, L., Albalak, A., Wang, X., Wang, W.Y .: Logic-lm: Empowering large language models
with symbolic solvers for faithful logical reasoning. arXiv preprint arXiv:2305.12295 (2023)
269. Pan, S., Luo, L., Wang, Y ., Chen, C., Wang, J., Wu, X.: Unifying large language models and
knowledge graphs: A roadmap. IEEE Transactions on Knowledge and Data Engineering (2024)
270. Pantazi, S.V ., Arocha, J.F., Moehr, J.R.: Case-based medical informatics. BMC Medical Infor-
matics and Decision Making 4(1), 1–23 (2004)
271. Papernot, N., McDaniel, P .: Deep k-nearest neighbors: Towards conﬁdent, interpretable and
robust deep learning. arXiv preprint arXiv:1803.04765 [cs.LG] (2018)
272. Park, S.H., Lee, G., Seo, J., Bhat, M., Kang, M., Francis, J., Jadhav, A., Liang, P .P ., Morency,
L.P .: Diverse and admissible trajectory forecasting through multimodal context understanding.
In: Computer Vision–ECCV 2020: 16th European Conference, Glasgow, UK, August 23–28,
2020, Proceedings, Part XI 16, pp. 282–298. Springer (2020)
273. Pearl, J.: Probabilistic Reasoning in Intelligent Systems: Networks of Plausible Inference. Mor-
gan Kaufmann, San Mateo, CA (1988)
274. Pearl, J.: Causality. Cambridge university press (2009)
275. Penn, D.C., Holyoak, K.J., Povinelli, D.J.: Darwin’s mistake: Explaining the discontinuity
between human and nonhuman minds. Behavioral and brain sciences 31(2), 109–130 (2008)
276. Petroni, F., Rocktäschel, T., Riedel, S., Lewis, P ., Bakhtin, A., Wu, Y ., Miller, A.: Language
models as knowledge bases? In: Proceedings of the 2019 Conference on Empirical Meth-
ods in Natural Language Processing and the 9th International Joint Conference on Natural
Language Processing (EMNLP-IJCNLP), pp. 2463–2473. Association for Computational Lin-
guistics, Hong Kong, China (2019). DOI
https://doi.org/10.18653/v1/D19-1250.U R L https://
www.aclweb.org/anthology/D19-1250

130 References
277. Piech, C., Bassen, J., Huang, J., Ganguli, S., Sahami, M., Guibas, L.J., Sohl-Dickstein, J.: Deep
knowledge tracing. Advances in neural information processing systems 28 (2015)
278. Pierri, F., Luceri, L., Ferrara, E.: How does twitter account moderation work? dynam-
ics of account creation and suspension during major geopolitical events. arXiv preprint
arXiv:2209.07614 (2022)
279. Pierri, F., Perry, B.L., DeV erna, M.R., Yang, K.C., Flammini, A., Menczer, F., Bryden, J.: Online
misinformation is linked to early covid-19 vaccination hesitancy and refusal. Scientiﬁc reports
12(1), 1–7 (2022)
280. Pluci´nski, K., Lango, M., Stefanowski, J.: Prototypical convolutional neural network for a
phrase-based explanation of sentiment classiﬁcation. In: Machine Learning and Principles and
Practice of Knowledge Discovery in Databases, pp. 457–472. Springer International Publishing,
Cham (2021)
281. Plummer, B.A., Wang, L., Cervantes, C.M., Caicedo, J.C., Hockenmaier, J., Lazebnik, S.:
Flickr30k entities: Collecting region-to-phrase correspondences for richer image-to-sentence
models. In: Proceedings of the IEEE international conference on computer vision, pp. 2641–
2649 (2015)
282. Poesia, G., Gandhi, K., Zelikman, E., Goodman, N.D.: Certiﬁed deductive reasoning with
language models. arXiv preprint arXiv:2306.04031 (2023)
283. Puri, M., V arde, A., Dong, B.: Pragmatics and semantics to connect speciﬁc local laws with
public reactions. 2018 IEEE International Conference on Big Data (Big Data) pp. 5433–5435
(2018)
284. Qasemi, E., Oltramari, A.: Intelligent trafﬁc monitoring with hybrid ai. arXiv preprint
arXiv:2209.00448 (2022)
285. Qi, Y ., Wu, Q., Anderson, P ., Wang, X., Wang, W.Y ., Shen, C., Hengel, A.v.d.: Reverie:
Remote embodied visual referring expression in real indoor environments. In: Proceedings
of the IEEE/CVF Conference on Computer Vision and Pattern Recognition, pp. 9982–9991
(2020)
286. Qin, X., Regli, W.C.: A study in applying case-based reasoning to engineering design: Mechan-
ical bearing design. Artiﬁcial Intelligence for Engineering Design, Analysis and Manufacturing
17(3), 235-252 (2003). DOI https://doi.org/10.1017/S0890060403173064
287. Raaheim, K.: Problem solving and past experience. Monographs of the Society for Research in
Child Development 30(2), 58–67 (1965). URL http://www.jstor.org/stable/1165776
288. Radford, A., Wu, J., Child, R., Luan, D., Amodei, D., Sutskever, I.: Language models are
unsupervised multitask learners. OpenAI Blog 1(8), 9 (2019)
289. Raffel, C., Shazeer, N., Roberts, A., Lee, K., Narang, S., Matena, M., Zhou, Y ., Li, W., Liu,
P .J.: Exploring the limits of transfer learning with a uniﬁed text-to-text transformer. Journal
of Machine Learning Research 21(140), 1–67 (2020). URL
http://jmlr.org/papers/v21/20-074.
html
290. Raffel, C., Shazeer, N., Roberts, A., Lee, K., Narang, S., Matena, M., Zhou, Y ., Li, W., Liu, P .J.,
et al.: Exploring the limits of transfer learning with a uniﬁed text-to-text transformer. J. Mach.
Learn. Res. 21(140), 1–67 (2020)
291. Rajani, N.F., McCann, B., Xiong, C., Socher, R.: Explain yourself! leveraging language models
for commonsense reasoning. arXiv preprint arXiv:1906.02361 (2019)
292. Rawls, J.: A theory of justice. Cambridge (Mass.) (1971)
293. Ray, P .P .: Chatgpt: A comprehensive review on background, applications, key challenges, bias,
ethics, limitations and future scope. Internet of Things and Cyber-Physical Systems (2023)
294. Razeghi, Y ., Logan IV , R.L., Gardner, M., Singh, S.: Impact of pretraining term frequencies on
few-shot reasoning. arXiv preprint
arXiv:2202.07206 (2022)

References 131
295. Ribeiro, M.T., Singh, S., Guestrin, C.: “why should i trust you?” explaining the predictions of any
classiﬁer. In: Proceedings of the 22nd ACM SIGKDD international conference on knowledge
discovery and data mining, pp. 1135–1144 (2016)
296. Romano, A., Balliet, D.: Reciprocity outperforms conformity to promote cooperation. Psycho-
logical Science 28(10), 1490–1502 (2017)
297. Rosch, E.H.: Natural categories. Cognitive Psychology 4(3), 328–350 (1973). DOI https://doi.
org/10.1016/0010-0285(73)90017-0.U R L https://www.sciencedirect.com/science/article/pii/
0010028573900170
298. Rossi, F.: Building trust in artiﬁcial intelligence. Journal of international affairs 72(1), 127–134
(2018)
299. Rossi, F., Mattei, N.: Building ethically bounded ai. In: Proceedings of the AAAI Conference
on Artiﬁcial Intelligence, vol. 33, pp. 9785–9789 (2019)
300. Rudin, C., Chen, C., Chen, Z., Huang, H., Semenova, L., Zhong, C.: Interpretable machine
learning: Fundamental principles and 10 grand challenges. Statistic Surveys 16, 1–85 (2022)
301. Saha, S., Hase, P ., Rajani, N., Bansal, M.: Are hard examples also harder to explain? a study
with human and model-generated explanations. arXiv preprint arXiv:2211.07517 (2022)
302. Sap, M., Gabriel, S., Qin, L., Jurafsky, D., Smith, N.A., Choi, Y .: Social bias frames: Reasoning
about social and power implications of language. arXiv preprint arXiv:1911.03891 (2019)
303. Sap, M., Le Bras, R., Allaway, E., Bhagavatula, C., Lourie, N., Rashkin, H., Roof, B., Smith,
N.A., Choi, Y .: Atomic: An atlas of machine commonsense for if-then reasoning. In: Proceedings
of the AAAI Conference on Artiﬁcial Intelligence, vol. 33, pp. 3027–3035 (2019)
304. Sap, M., LeBras, R., Fried, D., Choi, Y .: Neural theory-of-mind? on the limits of social intelli-
gence in large lms. arXiv preprint arXiv:2210.13312 (2022)
305. Sap, M., Rashkin, H., Chen, D., Le Bras, R., Choi, Y .: Social IQa: Commonsense reasoning about
social interactions. In: Proceedings of the 2019 Conference on Empirical Methods in Natural
Language Processing and the 9th International Joint Conference on Natural Language Pro-
cessing (EMNLP-IJCNLP), pp. 4463–4473. Association for Computational Linguistics, Hong
Kong, China (2019). DOI
https://doi.org/10.18653/v1/D19-1454.U R L https://www.aclweb.
org/anthology/D19-1454
306. Saralajew, S., Holdijk, L., Rees, M., Villmann, T.: Prototype-based neural network layers:
incorporating vector quantization. arXiv preprint
arXiv:1812.01214 (2018)
307. Schank, R.C.: Dynamic Memory: A Theory of Reminding and Learning in Computers and
People. Cambridge University Press, USA (1983)
308. Selvaraju, R.R., Cogswell, M., Das, A., V edantam, R., Parikh, D., Batra, D.: Grad-cam:
Visual explanations from deep networks via gradient-based localization. See https://arxiv.
org/abs/1610.02391 v3 7(8) (2016)
309. Selvaraju, R.R., Cogswell, M., Das, A., V edantam, R., Parikh, D., Batra, D.: Grad-cam: Visual
explanations from deep networks via gradient-based localization. In: Proceedings of the IEEE
international conference on computer vision, pp. 618–626 (2017)
310. Sen, C., Hartvigsen, T., Yin, B., Kong, X., Rundensteiner, E.: Human attention maps for text
classiﬁcation: Do humans and neural networks focus on the same words? In: D. Jurafsky, J. Chai,
N. Schluter, J. Tetreault (eds.) Proceedings of the 58th Annual Meeting of the Association
for Computational Linguistics, pp. 4596–4608. Association for Computational Linguistics,
Online (2020). DOI
https://doi.org/10.18653/v1/2020.acl-main.419.U R Lhttps://aclanthology.
org/2020.acl-main.419
311. Shanahan, M.: Talking about large language models. Communications of the ACM 67(2), 68–79
(2024)
312. Shannon, C.E.: Communication theory of secrecy systems. The Bell system technical journal
28(4), 656–715 (1949)

132 References
313. She, L., Chai, J.: Interactive learning of grounded verb semantics towards human-robot com-
munication. In: Proceedings of the 55th Annual Meeting of the Association for Computational
Linguistics (V olume 1: Long Papers), pp. 1634–1644 (2017)
314. Sheng, E., Chang, K.W., Natarajan, P ., Peng, N.: The woman worked as a babysitter: On biases
in language generation. In: K. Inui, J. Jiang, V . Ng, X. Wan (eds.) Proceedings of the 2019 Con-
ference on Empirical Methods in Natural Language Processing and the 9th International Joint
Conference on Natural Language Processing (EMNLP-IJCNLP), pp. 3407–3412. Association
for Computational Linguistics, Hong Kong, China (2019). DOI
https://doi.org/10.18653/v1/
D19-1339.U R L https://aclanthology.org/D19-1339
315. Shi, W., Min, S., Yasunaga, M., Seo, M., James, R., Lewis, M., Zettlemoyer, L., Yih, W.t.:
Replug: Retrieval-augmented black-box language models. arXiv preprint arXiv:2301.12652
(2023)
316. Shin, T., Razeghi, Y ., IV , R.L.L., Wallace, E., Singh, S.: Autoprompt: Eliciting knowledge from
language models with automatically generated prompts. In: B. Webber, T. Cohn, Y . He, Y . Liu
(eds.) Proceedings of the 2020 Conference on Empirical Methods in Natural Language Pro-
cessing, EMNLP 2020, Online, November 16-20, 2020, pp. 4222–4235. Association for Com-
putational Linguistics (2020). DOI
https://doi.org/10.18653/v1/2020.emnlp-main.346.U R L
https://doi.org/10.18653/v1/2020.emnlp-main.346
317. Shneiderman, B.: Human-centered AI. Oxford University Press (2022)
318. Shridhar, M., Thomason, J., Gordon, D., Bisk, Y ., Han, W., Mottaghi, R., Zettlemoyer, L.,
Fox, D.: Alfred: A benchmark for interpreting grounded instructions for everyday tasks. In:
Proceedings of the IEEE/CVF conference on computer vision and pattern recognition, pp.
10740–10749 (2020)
319. Shwartz, V .: Good night at 4 pm?! time expressions in different cultures. In: Findings of the
Association for Computational Linguistics: ACL 2022, pp. 2842–2853 (2022)
320. Shwartz, V ., West, P ., Le Bras, R., Bhagavatula, C., Choi, Y .: Unsupervised commonsense ques-
tion answering with self-talk. In: Proceedings of the 2020 Conference on Empirical Methods in
Natural Language Processing (EMNLP), pp. 4615–4629. Association for Computational Lin-
guistics, Online (2020). DOI
https://doi.org/10.18653/v1/2020.emnlp-main.373.U R L https://
www.aclweb.org/anthology/2020.emnlp-main.373
321. Shwartz, V ., West, P ., Le Bras, R., Bhagavatula, C., Choi, Y .: Unsupervised commonsense ques-
tion answering with self-talk. In: Proceedings of the 2020 Conference on Empirical Methods in
Natural Language Processing (EMNLP), pp. 4615–4629. Association for Computational Lin-
guistics, Online (2020). DOI
https://doi.org/10.18653/v1/2020.emnlp-main.373.U R L https://
www.aclweb.org/anthology/2020.emnlp-main.373
322. Sitawarin, C., Wagner, D.: On the robustness of deep k-nearest neighbors. In: Workshop proceed-
ings of the 2019 IEEE Symposium on Security and Privacy Workshops – SP 2019 Workshops,
pp. 1–7. IEEE, San Francisco, CA, USA (2019). DOI
https://doi.org/10.1109/SPW.2019.00014
323. Slack, D., Krishna, S., Lakkaraju, H., Singh, S.: Talktomodel: Explaining machine learning
models with interactive natural language conversations (2022)
324. Smil, V .: Growth: from microorganisms to megacities. Mit Press (2019)
325. Smith, A.: The theory of moral sentiments. HG Bohn (1853)
326. Sobieszek, A., Price, T.: Playing games with ais: the limits of gpt-3 and similar large language
models. Minds and Machines 32(2), 341–364 (2022)
327. Sourati, Z., Deshpande, D., Ilievski, F., Gashteovski, K., Saralajew, S.: Robust text classiﬁcation:
Analyzing prototype-based networks. EMNLP Findings (2024)
328. Sourati, Z., Ilievski, F., Sandlin, H.Â., Mermoud, A.: Case-based reasoning with language
models for classiﬁcation of logical fallacies. In: IJCAI (2023)
329. Sourati, Z., Ilievski, F., Sommerauer, P .: “ARN: Analogical Reasoning on Narratives”. In Trans-
actions of ACL (2024). arXiv preprint arXiv:2310.00996 (2023)

References 133
330. Sourati, Z., V enkatesh, V .P .P ., Deshpande, D., Rawlani, H., Ilievski, F., Sandlin, H.Â., Mermoud,
A.: Robust and explainable identiﬁcation of logical fallacies in natural language arguments.
Knowledge-Based Systems 266, 110418 (2023)
331. Speer, R., Chin, J., Havasi, C.: Conceptnet 5.5: An open multilingual graph of general knowl-
edge. In: Thirty-ﬁrst AAAI conference on artiﬁcial intelligence (2017)
332. Speith, T.: A review of taxonomies of explainable artiﬁcial intelligence (xai) methods. In:
Proceedings of the 2022 ACM Conference on Fairness, Accountability, and Transparency, pp.
2239–2250 (2022)
333. Spelke, E.S., Kinzler, K.D.: Core knowledge. Developmental science 10(1), 89–96 (2007)
334. Storks, S., Gao, Q., Zhang, Y ., Chai, J.: Tiered reasoning for intuitive physics: Toward veriﬁable
commonsense language understanding. arXiv preprint arXiv:2109.04947 (2021)
335. Suhr, A., Yan, C., Schluger, C., Y u, S., Khader, H., Mouallem, M., Zhang, I., Artzi, Y .: Executing
instructions in situated collaborative interactions. arXiv preprint
arXiv:1910.03655 (2019)
336. Sun, J., Sun, H., Han, T., Zhou, B.: Neuro-symbolic program search for autonomous driving
decision module design. In: Conference on Robot Learning, pp. 21–30. PMLR (2021)
337. Sun, T., Gaut, A., Tang, S., Huang, Y ., ElSherief, M., Zhao, J., Mirza, D., Belding, E., Chang,
K.W., Wang, W.Y .: Mitigating gender bias in natural language processing: Literature review.
In: A. Korhonen, D. Traum, L. Màrquez (eds.) Proceedings of the 57th Annual Meeting of
the Association for Computational Linguistics, pp. 1630–1640. Association for Computational
Linguistics, Florence, Italy (2019). DOI https://doi.org/10.18653/v1/P19-1159.U R L https://
aclanthology.org/P19-1159
338. Taecharungroj, V ., Nueangjamnong, P .: The effect of humour on virality: The study of internet
memes on social media. In: 7th International Forum on Public Relations and Advertising Media
Impacts on Culture and Social Communication. Bangkok, August (2014)
339. Talmor, A., Herzig, J., Lourie, N., Berant, J.: CommonsenseQA: A question answering chal-
lenge targeting commonsense knowledge. In: Proceedings of the 2019 Conference of the North
American Chapter of the Association for Computational Linguistics: Human Language Tech-
nologies, V olume 1 (Long and Short Papers), pp. 4149–4158. Association for Computational
Linguistics, Minneapolis, Minnesota (2019). DOI
https://doi.org/10.18653/v1/N19-1421.U R L
https://www.aclweb.org/anthology/N19-1421
340. Tambe, P ., Cappelli, P ., Yakubovich, V .: Artiﬁcial intelligence in human resources management:
Challenges and a path forward. California Management Review 61(4), 15–42 (2019)
341. Tandon, N., De Melo, G., Weikum, G.: Webchild 2.0: Fine-grained commonsense knowledge
distillation. In: Proceedings of ACL 2017, System Demonstrations, pp. 115–120 (2017)
342. Tanon, T.P ., Weikum, G., Suchanek, F.M.: Yago 4: A reason-able knowledge base. The Semantic
Web 12123, 583 – 596 (2020)
343. Tatiya, G., Francis, J., Bondi, L., Navarro, I., Nyberg, E., Sinapov, J., Oh, J.: Knowledge-driven
scene priors for semantic audio-visual embodied navigation. arXiv preprint arXiv:2212.11345
(2022)
344. Tatiya, G., Francis, J., Sinapov, J.: Transferring implicit knowledge of non-visual object prop-
erties across heterogeneous robot morphologies. In: 2023 IEEE International Conference on
Robotics and Automation (ICRA), pp. 11315–11321. IEEE (2023)
345. Thakur, A.K., Ilievski, F., Sandlin, H.Â., Mermoud, A., Sourati, Z., Luceri, L., Tommasini, R.:
Multimodal and explainable internet meme classiﬁcation. AI4SG (2023)
346. Thieme, A., Hanratty, M., Lyons, M., Palacios, J., Marques, R.F., Morrison, C., Doherty, G.:
Designing human-centered ai for mental health: Developing clinically relevant applications for
online cbt treatment. ACM Transactions on Computer-Human Interaction 30(2), 1–50 (2023)
347. Thomason, J., Murray, M., Cakmak, M., Zettlemoyer, L.: Vision-and-dialog navigation. In:
Conference on Robot Learning, pp. 394–406. PMLR (2020)

134 References
348. Tierney, D.: How teachers explain things: Metaphoric representation of social studies concepts.
In: Annual Meeting of the American Educational Research Association (1988)
349. Tommasini, R., Ilievski, F., Wijesiriwardene, T.: Imkg: The internet meme knowledge graph. In:
The Semantic Web: 20th International Conference, ESWC 2023, Hersonissos, Crete, Greece,
May 28–June 1, 2023, Proceedings, pp. 354–371. Springer Nature Switzerland (2023)
350. Touvron, H., Martin, L., Stone, K., Albert, P ., Almahairi, A., Babaei, Y ., Bashlykov, N., Batra,
S., Bhargava, P ., Bhosale, S., et al.: Llama 2: Open foundation and ﬁne-tuned chat models.
arXiv preprint
arXiv:2307.09288 (2023)
351. Trinh, T.H., Wu, Y ., Le, Q.V ., He, H., Luong, T.: Solving olympiad geometry without human
demonstrations. Nature 625(7995), 476–482 (2024)
352. Truong, T.H., Baldwin, T., V erspoor, K., Cohn, T.: Language models are not naysayers: An
analysis of language models on negation benchmarks. arXiv preprint arXiv:2306.08189 (2023)
353. Turney, P .D., Littman, M.L., Bigham, J., Shnayder, V .: Combining independent modules to solve
multiple-choice synonym and analogy problems. arXiv preprint
arXiv:cs/0309035 (2003)
354. Tutors, V .: Analogies - ssat elementary level verbal. URL https://www.varsitytutors.com/ssat_
elementary_level_verbal-help/analogies
355. Tymbay, A.A.: Manipulative use of political headlines in western and russian online
sources. Discourse & Communication 16(3), 346–363 (2022). DOI
https://doi.org/10.1177/
17504813221101824.U R L https://doi.org/10.1177/17504813221101824
356. Udandarao, V ., Prabhu, A., Ghosh, A., Sharma, Y ., Torr, P .H., Bibi, A., Albanie, S., Bethge, M.:
No “zero-shot” without exponential data: Pretraining concept frequency determines multimodal
model performance. arXiv preprint arXiv:2404.04125 (2024)
357. Ullman, T.: Large language models fail on trivial alterations to theory-of-mind tasks. arXiv
preprint arXiv:2302.08399 (2023)
358. V almeekam, K., Marquez, M., Sreedharan, S., Kambhampati, S.: On the planning abilities of
large language models–a critical investigation. arXiv preprint arXiv:2305.15771 (2023)
359. V aswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A.N., Kaiser, Ł., Polo-
sukhin, I.: Attention is all you need. Advances in neural information processing systems 30
(2017)
360. V erdiesen, I., Dignum, V ., Hoven, J.V .D.: Measuring moral acceptability in e-deliberation:
A practical application of ethics by participation. ACM Transactions on Internet Technology
(TOIT) 18(4), 1–20 (2018)
361. V orácek, V ., Hein, M.: Provably adversarially robust nearest prototype classiﬁers. In: K. Chaud-
huri, S. Jegelka, L. Song, C. Szepesvári, G. Niu, S. Sabato (eds.) Proceedings of the 39th
International Conference on Machine Learning – ICML 2022, vol. 162 of the Proceedings of
Machine Learning Research, pp. 22361–22383. PMLR, Baltimore, MD, USA (2022)
362. V orsino, Z.: Chatbots, gender, and race on web 2.0 platforms: Tay. ai as monstrous femininity
and abject whiteness. Signs: Journal of Women in Culture and Society 47(1), 105–127 (2021)
363. V ossen, P ., Caselli, T., Segers, R.: A narratology-based framework for storyline extraction.
Computational Analysis of Storylines: Making Sense of Events 125 (2021)
364. Vrandeˇci´c, D., Krötzsch, M.: Wikidata: a free collaborative knowledgebase. Communications
of the ACM 57(10), 78–85 (2014)
365. Wachsmuth, H., Naderi, N., Hou, Y ., Bilu, Y ., Prabhakaran, V ., Thijm, T.A., Hirst, G., Stein, B.:
Computational argumentation quality assessment in natural language. In: Proceedings of the
15th Conference of the European Chapter of the Association for Computational Linguistics:
V olume 1, Long Papers, pp. 176–187. Association for Computational Linguistics, V alencia,
Spain (2017). URL
https://aclanthology.org/E17-1017
366. Wagstaff, K.: Machine learning that matters. arXiv preprint arXiv:1206.4656 (2012)
367. Waks, S.: Lateral thinking and technology education. Journal of Science Education and Tech-
nology 6, 245–255 (1997)

References 135
368. Wallach, W., Allen, C.: Moral machines: Teaching robots right from wrong. Oxford University
Press (2008)
369. Wang, B., Chen, W., Pei, H., Xie, C., Kang, M., Zhang, C., Xu, C., Xiong, Z., Dutta, R.,
Schaeffer, R., et al.: Decodingtrust: A comprehensive assessment of trustworthiness in gpt
models. arXiv preprint
arXiv:2306.11698 (2023)
370. Wang, B., Xu, C., Wang, S., Gan, Z., Cheng, Y ., Gao, J., Awadallah, A.H., Li, B.: Adversarial
glue: A multi-task benchmark for robustness evaluation of language models. arXiv preprint
arXiv:2111.02840 (2021)
371. Wang, J., Hu, X., Hou, W., Chen, H., Zheng, R., Wang, Y ., Yang, L., Huang, H., Ye, W., Geng, X.,
Jiao, B., Zhang, Y ., Xie, X.: On the robustness of chatgpt: An adversarial and out-of-distribution
perspective (2023)
372. Wang, P ., Chan, A., Ilievski, F., Chen, M., Ren, X.: Pinto: Faithful language reasoning using
prompt-generated rationales. ICLR (2023)
373. Wang, P ., Ilievski, F., Chen, M., Ren, X.: Do language models perform generalizable common-
sense inference? ACL Findings (2021)
374. Wang, P ., Peng, N., Ilievski, F., Szekely, P ., Ren, X.: Connecting the dots: A knowledgeable
path generator for commonsense question answering. EMNLP Findings (2020)
375. Wang, P ., Zamora, J., Liu, J., Ilievski, F., Chen, M., Ren, X.: Contextualized scene imagination
for generative commonsense reasoning. ICLR (2022)
376. Wang, R., Jansen, P ., Côté, M.A., Ammanabrolu, P .: Scienceworld: Is your agent smarter than
a 5th grader? arXiv preprint
arXiv:2203.07540 (2022)
377. Wang, S., Meng, Y ., Li, X., Sun, X., Ouyang, R., Li, J.: Openvidial 2.0: A larger-scale, open-
domain dialogue generation dataset with visual contexts. arXiv preprint arXiv:2109.12761
(2021)
378. Wang, X., Wei, J., Schuurmans, D., Le, Q., Chi, E., Narang, S., Chowdhery, A., Zhou, D.:
Self-consistency improves chain of thought reasoning in language models. arXiv preprint
arXiv:2203.11171 (2022)
379. Wang, Y ., McKee, M., Torbica, A., Stuckler, D.: Systematic literature review on the spread of
health-related misinformation on social media. Social Science & Medicine 240, 112552 (2019).
DOI
https://doi.org/10.1016/j.socscimed.2019.112552.U R L https://www.sciencedirect.com/
science/article/pii/S0277953619305465
380. Wei, J., Tay, Y ., Bommasani, R., Raffel, C., Zoph, B., Borgeaud, S., Yogatama, D., Bosma,
M., Zhou, D., Metzler, D., et al.: Emergent abilities of large language models. arXiv preprint
arXiv:2206.07682 (2022)
381. Wei, J., Wang, X., Schuurmans, D., Bosma, M., Xia, F., Chi, E., Le, Q.V ., Zhou, D., et al.:
Chain-of-thought prompting elicits reasoning in large language models. Advances in Neural
Information Processing Systems 35, 24824–24837 (2022)
382. Weld, D., Etzioni, O.: The ﬁrst law of robotics (a call to arms). In: AAAI, vol. 94, pp. 1042–1047
(1994)
383. West, P ., Bhagavatula, C., Hessel, J., Hwang, J.D., Jiang, L., Bras, R.L., Lu, X., Welleck, S.,
Choi, Y .: Symbolic knowledge distillation: from general language models to commonsense
models. arXiv preprint arXiv:2110.07178 (2021)
384. West, P ., Lu, X., Dziri, N., Brahman, F., Li, L., Hwang, J.D., Jiang, L., Fisher, J., Ravichander,
A., Chandu, K., et al.: The generative ai paradox: “what it can create, it may not understand”.
arXiv preprint arXiv:2311.00059 (2023)
385. Wickramarachchi, R., Henson, C., Sheth, A.: An evaluation of knowledge graph embeddings
for autonomous driving data: Experience and practice. arXiv preprint arXiv:2003.00344 (2020)
386. Wiegreffe, S., Marasovi´c, A., Smith, N.A.: Measuring association between labels and free-text
rationales. arXiv preprint arXiv:2010.12762 (2020)

136 References
387. Wijesiriwardene, T., Wickramarachchi, R., Gajera, B., Gowaikar, S., Gupta, C., Chadha, A.,
Reganti, A.N., Sheth, A., Das, A.: ANALOGICAL - a novel benchmark for long text anal-
ogy evaluation in large language models. In: Findings of the Association for Computational
Linguistics: ACL 2023, pp. 3534–3549. Association for Computational Linguistics, Toronto,
Canada (2023). URL
https://aclanthology.org/2023.ﬁndings- acl.218
388. Wijmans, E., Datta, S., Maksymets, O., Das, A., Gkioxari, G., Lee, S., Essa, I., Parikh, D., Batra,
D.: Embodied question answering in photorealistic environments with point cloud perception.
In: Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition,
pp. 6659–6668 (2019)
389. Williams, B., Lieberman, H., Winston, P .H.: Understanding stories with large-scale common
sense. In: COMMONSENSE (2017)
390. Winston, M.E., Chafﬁn, R., Herrmann, D.: A taxonomy of part-whole relations. Cognitive
science 11(4), 417–444 (1987)
391. Wu, L., Morstatter, F., Carley, K.M., Liu, H.: Misinformation in social media: Deﬁnition,
manipulation, and detection. SIGKDD Explor. Newsl. 21(2), 80-90 (2019). DOI https://doi.
org/10.1145/3373464.3373475.U R L https://doi.org/10.1145/3373464.3373475
392. Xia, J., Wu, C., Yan, M.: Incorporating relation knowledge into commonsense reading compre-
hension with multi-task learning. In: Proc. of CIKM, CIKM ’19, p. 2393-2396 (2019)
393. Xie, C., Wang, J., Zhang, Z., Zhou, Y ., Xie, L., Y uille, A.: Adversarial examples for semantic
segmentation and object detection. In: Proceedings of the IEEE international conference on
computer vision, pp. 1369–1378 (2017)
394. Yang, H.M., Zhang, X.Y ., Yin, F., Liu, C.L.: Robust classiﬁcation with convolutional prototype
learning. In: Proceedings of the IEEE conference on computer vision and pattern recognition,
pp. 3474–3482 (2018)
395. Yang, W., Wang, X., Farhadi, A., Gupta, A., Mottaghi, R.: Visual semantic navigation using
scene priors. arXiv preprint arXiv:1810.06543 (2018)
396. Yang, Y ., Read, S.J., Miller, L.C.: A taxonomy of situations from chinese idioms. Journal of
Research in Personality 40(5), 750–778 (2006)
397. Yao, L., Peng, N., Weischedel, R., Knight, K., Zhao, D., Yan, R.: Plan-and-write: Towards
better automatic storytelling. In: Proceedings of the AAAI Conference on Artiﬁcial Intelligence,
vol. 33, pp. 7378–7385 (2019)
398. Yao, S., Y u, D., Zhao, J., Shafran, I., Grifﬁths, T.L., Cao, Y ., Narasimhan, K.: Tree of thoughts:
Deliberate problem solving with large language models. arXiv preprint arXiv:2305.10601
(2023)
399. Yasunaga, M., Chen, X., Li, Y ., Pasupat, P ., Leskovec, J., Liang, P ., Chi, E.H., Zhou, D.: Large
language models as analogical reasoners. arXiv preprint arXiv:2310.01714 (2023)
400. Yasunaga, M., Ren, H., Bosselut, A., Liang, P ., Leskovec, J.: Qa-gnn: Reasoning with language
models and knowledge graphs for question answering. arXiv preprint
arXiv:2104.06378 (2021)
401. Zelikman, E., Wu, Y ., Goodman, N.D.: Star: Bootstrapping reasoning with reasoning. arXiv
preprint arXiv:2203.14465 (2022)
402. Zellers, R., Bisk, Y ., Farhadi, A., Choi, Y .: From recognition to cognition: Visual common-
sense reasoning. In: Proceedings of the IEEE/CVF conference on computer vision and pattern
recognition, pp. 6720–6731 (2019)
403. Zhang, H., Zhao, X., Song, Y .: WinoWhy: A deep diagnosis of essential commonsense knowl-
edge for answering Winograd schema challenge. In: Proceedings of the 58th Annual Meeting of
the Association for Computational Linguistics, pp. 5736–5745. Association for Computational
Linguistics, Online (2020). DOI
https://doi.org/10.18653/v1/2020.acl-main.508.U R L https://
www.aclweb.org/anthology/2020.acl-main.508
404. Zhang, J., Ilievski, F., Ma, K., Francis, J., Oltramari, A.: An empirical investigation of com-
monsense self-supervision with knowledge graphs. AKBC (2022)

References 137
405. Zhang, J., Ilievski, F., Ma, K., Kollaa, A., Francis, J., Oltramari, A.: A study of situational
reasoning for trafﬁc understanding. In: KDD (2023)
406. Zhang, Q., Yang, Y ., Ma, H., Wu, Y .N.: Interpreting cnns via decision trees. In: Proceedings of
the IEEE/CVF conference on computer vision and pattern recognition, pp. 6261–6270 (2019)
407. Zhang, S., Dinan, E., Urbanek, J., Szlam, A., Kiela, D., Weston, J.: Personalizing dialogue
agents: I have a dog, do you have pets too? arXiv preprint arXiv:1801.07243 (2018)
408. Zhao, A., Huang, D., Xu, Q., Lin, M., Liu, Y .J., Huang, G.: Expel: Llm agents are experiential
learners. arXiv preprint arXiv:2308.10144 (2023)
409. Zheng, S., Song, Y ., Leung, T., Goodfellow, I.: Improving the robustness of deep neural networks
via stability training (2016). DOI
https://doi.org/10.48550/ARXIV .1604.04326.U R L https://
arxiv.org/abs/1604.04326
410. Zhou, D., Schärli, N., Hou, L., Wei, J., Scales, N., Wang, X., Schuurmans, D., Cui, C., Bousquet,
O., Le, Q., et al.: Least-to-most prompting enables complex reasoning in large language models.
arXiv preprint
arXiv:2205.10625 (2022)
411. Zhou, J., Gandomi, A.H., Chen, F., Holzinger, A.: Evaluating the quality of machine learning
explanations: A survey on methods and metrics. Electronics 10(5), 593 (2021)
412. Zhou, P ., Khanna, R., Lee, S., Lin, B.Y ., Ho, D., Pujara, J., Ren, X.: Rica: Evaluating robust
inference capabilities based on commonsense axioms. arXiv preprint arXiv:2005.00782 (2020)
413. Zhou, P ., Madaan, A., Potharaju, S.P ., Gupta, A., McKee, K.R., Holtzman, A., Pujara, J., Ren,
X., Mishra, S., Nematzadeh, A., et al.: How far are large language models from agents with
theory-of-mind? arXiv preprint
arXiv:2310.03051 (2023)
414. Zini, J.E., Awad, M.: On the explainability of natural language processing deep models. ACM
Comput. Surv. 55(5) (2022). DOI https://doi.org/10.1145/3529755.U R L https://doi.org/10.
1145/3529755
415. Zoph, B., Bello, I., Kumar, S., Du, N., Huang, Y ., Dean, J., Shazeer, N., Fedus, W.: St-moe:
Designing stable and transferable sparse expert models (2022)
```
