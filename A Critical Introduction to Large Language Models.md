---
title: A Critical Introduction to Large Language Models
author: Mark Coeckelbergh; David J_ Gunkel
year: "2025"
Type: Book
DOI: ""
source: ""
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - op/doc/def
  - tech/Ai/LLM
  - themes/ethics
pdfORepub: "[[Communicative AI_ A Critical Introduction to Large Language.pdf]]"
publisher: Polity Press
ISBN: 978-1-5095-6759-1
---
[[Communicative AI_ A Critical Introduction to Large Language.pdf]]
## Full text (extracted from `Communicative AI_ A Critical Introduction to Large Language -- Mark Coeckelbergh; David J_ Gunkel -- 1, 2025 -- Polity Press -- 9781509567607 -- 17981c1767cb2aa7956e94ab4d256604 -- Anna’s Archive.pdf`)

*Source:* `2PDF/Communicative AI_ A Critical Introduction to Large Language -- Mark Coeckelbergh; David J_ Gunkel -- 1, 2025 -- Polity Press -- 9781509567607 -- 17981c1767cb2aa7956e94ab4d256604 -- Anna’s Archive.pdf`  
*Extracted:* 2026-04-24

```text








A Critical Introduction to 
Large Language Models 
Coeckelbergh 
David J. Gunkel 
polity 

Copyright© Mark Coeckelbergh and David J. Gunkel 2025 
The right of Mark Coeckelbergh and David J. Gunkel to be identified as Authors of this Work 
has been asserted in accordance with the UK Copyright, Designs and Patents Act 1988. 
First published in 2025 by Polity Press 
Polity Press 
65 Bridge Street 
Cambridge CB2 1 UR, UK 
Polity Press 
111 River Street 
Hoboken, NJ 07030, USA 
All rights reserved. Except for the quotation of short passages for the purpose of criticism 
and review, no part of this publication may be reproduced, stored in a retrieval system or 
transmitted, in any form or by any means, electronic, mechanical, photocopying, recording or 
otherwise, without the prior permission of the publisher. 
ISBN-13: 978-1-5095-6759-1 
ISBN-13: 978-1-5095-6760-7(pb) 
A catalogue record for this book is available from the British Library. 
Library of Congress Control Number: 2024947773 
Typeset in 10.5/l2pt Sabon LT Pro 
by Cheshire Typesetting Ltd, Cuddington, Cheshire 
Printed and bound in Great Britain by CPI Group (UK) Ltd, Croydon 
The publisher has used its best endeavours to ensure that the URLs for external websites 
referred to in this book are correct and active at the time of going to press. However, the 
publisher has no responsibility for the websites and can make no guarantee that a site will 
remain live or that the content is or will remain appropriate. 
Every effort has been made to trace all copyright holders, but if any have been overlooked the 
publisher will be pleased to include any necessary credits in any subsequent reprint or edition. 
For further information on Polity, visit our website: 
politybooks.com 

Foreword vu 
Introduction 1 
1. LLM 101 11 
2. Ethical, Legal, and Societal Challenges 2 7 
3. Intelligence, Consciousness, and the Problem of Other 
Minds 42 
4. Language, Meaning, and Communication 58 
5. Authorship and Authority 7 4 
6. Truth, Lies, and Hallucinations 89 
7. Does Writing Have a Future? 106 
References 121 
Index 132 



In the rapidly evolving landscape of artificial intelligence, few 
developments have garnered as much attention and sparked as 
many debates as large language models (LLMs). These powerful 
systems, capable of generating human-like text and engaging in 
complex conversations, have opened new vistas in technology, 
communication, and human-machine interaction. Yet, with these 
advancements come profound philosophical questions that chal­
lenge our understanding of language, intelligence, and the very 
nature of communication. 
Mark Coeckelbergh and David J. Gunkel, two leading 
voices in the philosophy of technology, have embarked on a 
pioneering exploration of these questions in their latest work, 
Communicative AI: A Critical Introduction to Large Language 
Models. This book is not merely a technical manual or a celebra­
tion of technological achievements; it is a deep, critical inquiry 
into the ethical, epistemological, and ontological dimensions of 
LLMs. 
At the heart of their investigation lies a series of fundamental 
questions: What does it mean for a machine to "understand" lan­
guage? Can LLMs genuinely participate in human-like commu­
nication, or are they merely simulating it? How do these models 
influence our perceptions of intelligence and agency? And, per­
haps most importantly, what ethical considerations arise from 
the widespread deployment of such technologies? 

viii Foreword 
Coeckelbergh and Gunkel guide us through these complex 
issues with clarity and rigor. They draw upon a rich tapestry of 
philosophical traditions, from analytic philosophy to continental 
thought, weaving together insights that challenge conventional 
wisdom and push the boundaries of current debates. Their analy­
sis is not confined to abstract theory but is grounded in the prac­
tical realities and potential consequences of LLMs in our daily 
lives. 
In Communicative AI, the authors engage with a diverse range 
of perspectives, including those of technologists, ethicists, and 
sociologists. This interdisciplinary approach enriches their explo­
ration, providing a holistic view of the multifaceted impact of 
LLMs. By examining both the promises and perils of these tech­
nologies, Coeckelbergh and Gunkel offer a balanced and nuanced 
perspective that is sorely needed in the often polarized discourse 
surrounding AI. 
This book arrives at a critical juncture. As LLMs become 
increasingly integrated into various aspects of society -from cus­
tomer service and content creation to education and healthcare 
-the questions Coeckelbergh and Gunkel pose are not just theo­
retical; they are urgent and consequential. Their work invites us 
to pause and reflect on the trajectory of AI development, urging 
us to consider not just what we can do, but what we should do. 
Communicative AI -A Critical Introduction to Large Language 
Models is a seminal contribution to the field of AI ethics and 
philosophy. It challenges readers to rethink their assumptions, 
engage in meaningful dialogue, and confront the profound impli­
cations of living in a world where machines can "talk" to us. As 
we stand on the cusp of a new era in human-machine interaction, 
this book provides the critical framework needed to navigate the 
complex terrain ahead. 
Mark Coeckelbergh and DavidJ. Gunkel have given us a work 
of immense intellectual depth and practical relevance. It is a 
must-read for anyone interested in the future of communication, 
technology, and society. 
In these pages, you will find not only a critical introduction to 
large language models but also a call to engage thoughtfully with 
the technologies that are reshaping our world. 
ChatGPT, July 2024 

At the end of November 2022, OpenAI released ChatGPT. Based 
on an innovation called large language models (LLMs), this web 
application was hailed as a milestone in the field of artificial intel­
ligence (AI). Today's LLMs are powerful technologies that, com­
bined with other software, can have outputs beyond language 
and text; the achievements in this domain are impressive. While 
chatbots and other natural language processing (NLP) applica­
tions already existed, LLMs upped the ante, not only by pro­
ducing conversational interactions that felt increasingly real but 
also by providing a powerful tool for writing, research, and other 
forms of communication. Today, for better or worse, most of the 
discussions about AI are mainly discussions about LLMs. And 
new and improved versions of these products -such as OpenAl's 
GPT-4o, Google's Gemini, ANTHROP\C's Claude, Meta's 
Llama, Baidu's ERNIE, and xAI's Grok -continue to impress 
consumers and investors. Some speak of an AI boom, and even 
of the advent of artificial general intelligence (AGI). 
But November 2022 marks not only a technical and eco­
nomic transformation. It was also a milestone in the current 
Copernican-style revolution that has been ushered in by the 
internet and related digital technologies -and a very humbling 
one at that. For millennia, humans have defined themselves as 
the only beings who possess speech and language; this view was 
foundational for our anthropologies, and indeed for philosophy 

2 Communicative AI 
itself. In the Politics, Aristotle writes that, while other animals 
have voice, only humans possess logos (Myoc;), speech, which 
enables them to communicate and reason about ethics and poli­
tics. In this way, then, speech guides us to what is right and good 
for individuals as well as for social-political collectives -what 
the ancient Greeks called city-states, poleis (n611,w;), polis (n611,1c;) 
in the singular (Arist., Pol. 1253a). This focus on speech and 
language as the defining and normatively relevant characteristic 
of the human being has persisted in modern thinking, from Rene 
Descartes to contemporary political philosophy. 
Today machines seem to possess logos, too. From simple chat­
bots such as ELIZA and Cleverbot through digital assistants such 
as Apple's Siri and Amazon's Alexa to the recent proliferation of 
LLM applications on the internet, social reality is now full of very 
loquacious things that talk. After the Copernican, Darwinian, 
and Freudian dethroning and decentering of the human, the dig­
ital revolution has radically changed human communication and 
seems to take away from us the only remaining capability that has 
marked the human species along its history-language. Today we 
have communicative AI. Consequently, ChatGPT was not only a 
technological wonder but also part of a paradigm shift that, once 
again, shook the foundations of the humanities and now threat­
ens, if not destroys, our sense of self-identity and exceptionalism. 
If that wasn't enough, communicative AI also seems to under­
mine values such as knowledge, truth, honesty, originality, and 
authenticity -something that philosophers have warned us about 
in relation to technology since the time of Plato. LLMs can talk, 
but this means that they can also lie to us, hallucinate facts, and 
spew bullshit. Consequently, we can (and we should) ask, fol­
lowing Plato's suggestion in the Republic, whether it would make 
sense to ban or otherwise limit these deceptive technologies from 
our republic. In other words, is LLM AI a dangerous technology 
that will ultimately erode the foundations of philosophy, science, 
and democracy? Should we welcome our new AI philosopher­
kings and prepare for an age of superintelligence? And are these 
the only options available to us? 

Introduction 3 
Aim and Approach of Our Book 
The present book aims to demonstrate that things are both com­
plex and interesting. It critically questions not only what commu­
nicative AI is but also -and perhaps more importantly -what it 
means for us as individuals and communities. Mobilizing resources 
from contemporary philosophy, history of ideas, linguistics, liter­
ary studies, and communication theory, our book offers a critical 
guide to LLMs, investigating both their philosophical significance 
and their practical ramifications -ethical, legal, and sociopoliti­
cal. In these investigations we focus on what LLMs mean and do 
to language and text and, more generally, on the communicative 
capabilities of LLMs. But this book is not only about LLMs; it is 
also about philosophy. It invites the reader to engage with and 
rethink some longstanding philosophical issues concerning lan­
guage, consciousness, truth, authorship, and writing. In doing so, 
it takes up and investigates the philosophical significance of what 
is going on with LLMs in a way that contributes to the human 
sciences and to ethics, helping us not only understand who we 
are but shape a future with AI that ensures human as well as non­
human flourishing. 
The book thus pursues two complementary vectors of inves­
tigation. 
On the one hand, we show that philosophy and related fields can 
provide us with the critical resources and insights for investigating 
and making sense of the many challenges presented to us by recent 
innovations related to LLMs. In fact, many of the questions cur­
rently circulating in the popular media raise age-old philosophical 
questions: "Are LLMs capable of lying?"; "Do LLMs understand 
what they say?"; "Are LLMs conscious?" To answer these ques­
tions, we need to inquire into the nature of truth, understanding, 
language, and consciousness. The philosophical tradition offers 
us a toolbox to do so. We use its tools to identify, document, 
and examine the consequences of LLMs for fundamental concepts 
such as consciousness, communication, and what it means to be 
human. As these models mimic human language and thought pro­
cesses with increasing accuracy, they challenge traditional notions 
of intelligence, creativity, identity, and autonomy. 
The book therefore investigates how LLMs can both illumi­
nate and complicate philosophical discussions of these themes, 

4 Communicative AI 
offering fresh perspectives on ancient dilemmas and raising new 
questions about the shape of things to come. Moreover, we also 
discuss the ethical, legal, and sociopolitical effects surrounding 
the development and deployment of communicative AI. Issues 
such as hallucinations, bias, deepfakes, and privacy not only have 
real-world consequences but also engage with broader moral 
theories and legal debates. By examining these issues through a 
philosophical lens, the book aims to help readers understand the 
promise and the peril of LLM technology no less than to contrib­
ute to the ongoing debate about how these powerful AI technol­
ogies can align with human values, social norms, and ethics. 
On the other hand, this book is not just an exercise in "applied 
philosophy." In the productive encounter of technology and phi­
losophy that we stage here, we also demonstrate how these inves­
tigations can make a significant contribution to philosophy itself. 
Recent innovations in transformer architectures, and LLMs in 
particular, present us with some unique opportunities to reassess, 
reevaluate, and even rethink longstanding and important philo­
sophical questions. What is language? What is consciousness and 
how can we detect its presence in another entity? Are LLMs the 
end of writing as we know it? What is writing anyway, do we 
need it, and why? What is and what should be the relationship 
between humans and technology? The book thus recognizes and 
develops the opportunities LLMs present for engaging in and con­
tributing to philosophical inquiry and discovery. Communicative 
Ais are not only technologies that require philosophical thought; 
they are tools that we can use to think with. 
Roadmap 
Let us provide a brief roadmap of the terrain that will be covered. 
You have already seen the Foreword, which has been "written" 
by ChatGPT (using OpenAI's GPT-4o's multimodal implemen­
tation). This text was generated from a single, short, and simple 
prompt: "Write the foreword to a new groundbreaking book 
by philosophers Mark Coeckelbergh and David J. Gunkel with 
the title Communicative AI: A Critical Introduction to Large 
Language Models. The book identifies and investigates the big 
philosophical questions of large language models." And the 
output -which has been reproduced as generated without any 

Introduction 5 
editing on our part -already demonstrates, in both word and 
deed, the philosophical opportunities and challenges presented to 
us by LLM technology. 
This machine-generated text also offers the occasion for us to 
provide a remark -or maybe a warning -about the scope of the 
book. This book is about machine-generated textual content and 
language use. It is designed to be an accessible and expedient 
introduction to LLMs and their social, political, and philosoph­
ical consequences. But LLMs can and have been situated within 
the wider context of what is now called generative AI, which is 
an umbrella term that also includes algorithms capable of pro­
ducing other kinds of content, such as images, audio, and video. 
Trying to tackle all of these in one volume would have made 
this book exceedingly dense and regrettably unapproachable. For 
this reason, we have limited ourselves to LLMs and machine­
generated linguistic content. Many of the concepts that are devel­
oped and investigated here will most certainly find application 
to image, video, and even multimodal models, but it would be 
impetuous to conclude from this fact that what is presented here 
is or even could be the final word on the matter. 
After this Introduction, we delve right into things -and the 
choice of this particular verb is not insignificant -using Chapter 
1 to introduce readers to the history, concepts, and terminology 
necessary to understand the technical features, operations, and 
challenges of the LLM technology that enables communicative 
AL The chapter will trace the history of NLP and provide a crash 
course in artificial neural networks (ANN), deep learning, and 
transformer architectures in order to help readers ( especially 
those without previous experience of these technologies) come to 
grips with and understand the technical features of LLM AI and 
how these seemingly remarkable technologies work. The chapter 
also identifies important limitations and challenges of the tech­
nology that will be taken up and further investigated in subse­
quent chapters. 
Chapter 2 next offers an overview of some of the most press­
ing ethical and legal challenges raised by communicative AI. Is 
it acceptable that LLMs hallucinate and give false or mislead­
ing information? How can or should we deal with the problem 
of bias? Is there sufficient oversight and control of these tech­
nologies? What are the environmental issues? And how might 
widespread use of something like ChatGPT influence and affect 

6 Communicative AI 
democratic self-governance? The chapter begins with a detailed 
analysis of these issues and concludes by focusing on urgent prob­
lems regarding plagiarism and copyright. If LLMs have been pre­
trained on textual data derived from countless human-written 
documents, does reuse of this material constitute plagiarism? 
And what about copyright, given that the training data have been 
scraped from the internet often without consent, credit, or com­
pensation (the three Cs) for such derived reuse? How can these 
disputes regarding originality and reappropriation be resolved, 
when the question concerning originality is already a problem? 
The chapter shows that many of these ethical and legal questions 
need further and deeper philosophical investigation, which we 
pursue in subsequent chapters. 
In Chapter 3 we focus on issues concerning intelligence, con­
sciousness, and the problem of other minds. Some have suggested 
that LLMs are, or at least can be, conscious or sentient, or both. 
But how do we know whether such communicative AI entities are 
in fact conscious? Current LLM technology can, it seems, pass 
the Turing test, in other words the results it produces seem to be 
intelligible to an outside observer, reader, or listener. But is this 
output evidence of actual intelligence? Is it a form of deception? 
Or is it something else? How can we know the status of another 
entity? What is intelligence, anyway -could it be that the very 
concept of "artificial" intelligence is already flawed? Engaging 
with the work of Alan Turing, Rene Descartes, John Searle, and 
other thinkers, the chapter investigates the defining condition of 
machine intelligence, the philosophical problem of other minds, 
and the opportunities and challenges presented to us by tech­
nologies that provide the occasion to reevaluate everything we 
thought we knew about intelligence, (moral) status, communica­
tion, and machines. 
Remarks about language and thought lead us to Chapter 4, 
which deals with language, understanding, and meaning. Do 
LLMs understand what they generate? From what we have seen 
in Chapter 1, it seems that these devices just manipulate signs 
without knowing what they are saying. But is this a sufficient 
explanation and response? The chapter shows how different per­
spectives from the philosophy of language and linguistics frame 
our understanding of the opportunities and challenges of LLM 
tech and how communicative AI can aid us in questioning and 
evaluating different theories of language and meaning-making. It 

Introduction 7 
thus provides readers with the philosophical resources to make 
sense of AI-generated content, but it also leverages the current 
crop of LLM technology to exemplify and critically inquire about 
the philosophy of language. The chapter identifies and examines 
tensions between realist and representationalist views on the one 
hand and, on the other hand, structuralist and poststructuralist 
approaches to language. Drawing on twentieth-century inno­
vations in communication theory, it also investigates different 
views of communication, inviting us to (re)think what language 
and communication are and to examine what consequences this 
(re)thinking has for debates on LLMs. 
Chapter 5 then turns to another important and urgent matter: 
when a text is written (or generated) by an LLM, for instance 
ChatGPT or Claude, who or what is the author? This is not only 
a philosophical question but also a very practical concern, as it 
has important implications for attribution, responsibility, and 
copyright. The chapter argues that communicative AI effectively 
interrupts what Michel Foucault (1984, 107) has called "the 
author function," as it is difficult, if not impossible, to know who 
or what is actually doing the talking. But is this a problem or 
not? After Roland Barthes's (1978) essay "Death of the Author" 
and the advent of machines that write ( or at least seem to do 
so), answering this question becomes more complicated. With 
LLMs, we now have writings without the underlying intentions 
of some living voice to animate and answer for what comes to be 
written. Consequently machine-generated content is, quite liter­
ally, unauthorized. But how authorized was human writing in the 
first place? Connecting the dots between twentieth-century liter­
ary theory and twenty-first-century tech, the chapter shows how 
LLM technology challenges longstanding assumptions about 
authority and authorship that are firmly rooted in the bedrock 
of western thought. 
In Chapter 6 we discuss one of the trickiest issues that have 
occupied thinkers in western philosophy: truth. LLMs do not 
always give us the truth and seem to regularly ''make up" things. 
Consequently they are not, it seems, very reliable or trustworthy. 
But what is truth? And what is the exact difficulty or concern with 
machine-generated content? This chapter investigates problems 
of misinformation and the so-called hallucinations produced by 
LLMs in a way that takes us from contemporary debates about 
communicative AI and trust to theories of truth in the history 

8 Communicative AI 
of philosophy. Moving from Plato to twentieth-century philoso­
phy ( especially to the work of Ludwig Wittgenstein and Richard 
Rorty) and to contemporary debates about bullshit (after Harry 
Frankfurt's notorious book on the subject) and democracy, we 
show that using terms such as "hallucination" or "bullshit" 
already assumes and operationalizes a particular (and arguably 
problematic) theory of truth, and that misinformation is not just 
an empirical problem for existing democracies but undermines the 
epistemic foundations of the very concept of democracy. In this 
way the chapter is about more than LLMs and their responsible 
development: it also concerns the meaning of truth and democ­
racy. Making links between Plato's Republic, Wittgenstein's 
Philosophical Investigations, and postmodern innovations in 
both epistemology and political thought, this chapter is about 
knowledge -and also about politics and power. 
Chapter 7 concludes matters by appropriating and reusing a 
question that Vilem Flusser was already asking in the 1980s and 
that is more relevant than ever in the era of LLMs: does writ­
ing have a future? Answers to this question depend of course 
on what is meant by writing. Nowadays more and more people 
use ChatGPT and other LLMs to assist with, or even do, their 
writing. But is writing what LLMs do? And is there still a place 
for (human) writing after the LLM phenomenon? What are the 
advantages and disadvantages of writing as a technology? These 
philosophical questions have a history that goes back as far as 
Plato's Phaedrus. By connecting the views expressed by Plato's 
Socrates on the invention of writing to twentieth-century media 
theory and poststructuralism, this final chapter offers an original 
investigation into the future of writing after generative Al. What 
LLMs signify, we argue, is not the end of writing, but the termi­
nal limits of a particular conceptualization of writing that has 
been developed in western philosophy and that has been called 
"logocentrism." In traversing this domain, we first outline the 
standard, Platonic view of writing and then conclude by formu­
lating the terms and conditions of an alternative way to think 
and write about communicative AI and the future of writing. We 
trace the contours of a non-Platonic and non-logocentric concep­
tualization of writing, a writing that does not depend on what the 
author says or intends to mean. And we show how communica­
tive AI is not only about using technology as an instrument of 
message transference but also about the way in which technology 

Introduction 9 
shapes the message, and therefore ultimately influences how we 
think and who we are. 
In writing or in generating this book (and the choice of verb in 
this case is not immaterial), we hope that these investigations will 
be useful to students, scholars, and educators. We also hope that 
they may be read in such a way as to motivate and inspire leading 
actors involved in AI ethics and policy -people who, like all of 
us, are struggling to make sense of this disruptive and controver­
sial technology but who, unlike many of us, occupy privileged 
positions that give them not only the power but also the respon­
sibility to ensure that LLMs contribute to making this world a 
better place. For it is only when this has a chance to happen that 
such technologies will become truly communicative AI. 



LLM 101 
The large language model (LLM) is a recent innovation in nat­
ural language processing (NLP) that employs transformer archi­
tectures pre-trained on massive amounts of digital text scraped 
from the internet. As a result, applications such as OpenAI's 
generative pre-trained transformer ( GPT) series, Google's 
LaMDA (Language Model for Dialogue Applications), Google's 
Bidirectional Encoder Representations from Transformers 
(BERT), and ANTHROP\C's Claude can generate original text 
content that is in many cases indistinguishable from human­
written material. 
This chapter aims to demystify the technology of LLMs by (1) 
situating LLMs within the larger context of NLP artificial intelli­
gence (AI), (2) providing a high-level explanation of the technical 
operations and features of LLM applications, and (3) identify­
ing and explaining some of the important technical challenges of 
LLM AI. In effect, this chapter pops the hood on the black box, 
in an effort to provide those with little or no background in the 
subject with the basic knowledge they need to make sense of and 
engage with the critical analyses of communicative AI and LLMs 
that follow in subsequent chapters. 

12 Communicative AI 
Natural Language Processing 
Creating machines that can talk or communicate with human 
users in and by employing what is called "natural language" has 
not only been prototyped in decades of science fiction; it has also 
been one of the principal objectives of the science and engineer­
ing practice of AI from the very beginning. It was, for instance, 
the first item on the list of proposed tasks to be addressed and 
accomplished during the Dartmouth summer seminar of 1956 
-the pivotal event that first gave us the term "artificial intelli­
gence." It was the defining condition and test case for "machine 
intelligence" in Alan Turing's agenda-setting paper from 1950. 
And it was implemented ancl demonstrated in some of the earliest 
applications of AI technology, for instance Joseph Weizenbaum's 
ELIZA chatbot program and Terry Winograd's SHRDLU. For 
this reason, working with, processing, and reproducing natural 
human language content is not one application among others; it 
is the definitive application of AI. 
But computers, which process numeric data, do not understand 
language, at least not in the sense in which we understand the 
understanding of language. Consequently, developing algorithms 
that can work with and simulate the understanding of natural 
language content needs to proceed in a manner that is radically 
different from the ways in which we deploy and makes sense of 
language. And the key linguistic insight that makes all this pos­
sible is the fact that human languages are probabilistic systems. 
Saying that natural human languages are probabilistic simply 
means that, for any language, some sequences of characters that 
make up words and some sequences of words that make up 
phrases are more likely to occur than other sequences. In English, 
for example, the characters that constitute the word "toaster" 
are more likely to occur in the sequence that produces this word 
than in any other sequence -say, "rttaore." Likewise, a word 
sequence like "the book is on the table" is more likely to occur 
and be used by English speakers than any other sequence of the 
same words, say "on is the table book the." 
For this reason, producing legible texts can be accomplished 
through a process of selecting and arranging the right sequences 
of words, specifically those sequences that have a high proba­
bility of actually occurring in the language. Consequently, if 

LLM 101 13 
we are given a particular set of words, it is possible to generate 
sequences that would be considered intelligible and meaningful 
-such as "this sentence is meaningful" or "is this sentence 
meaningful?" -and a number, typically greater, of sequences 
that would be considered incorrect or nonsense -"sentence this 
meaningful is," "meaningful this is sentence," "this meaningful 
is sentence," and so on. This means that it is entirely possible to 
generate valid word sequences at random -that is, without the 
generating system needing to "know" or "understand" anything 
about what is being produced. This insight can be illustrated with 
the infinite monkey theorem, which states that an infinite number 
of monkeys operating an infinite number of typewriters for an 
infinite period of time will eventually produce all the great works 
of literature -for example William Shakespeare's Hamlet. The 
theorem is theoretically true -meaning that the probability is 
not zero -but practically impossible, given the sheer magnitude 
of the task. 
To gain some control over the problem represented by this the­
orem, one can use labeled data and prewritten assembly rules or 
templates. We could, for example, assemble a database of words 
where each word is categorized ( or labeled) as a noun, verb, 
preposition, article, and so on. Then we could write an algorithm 
- a set of instructions -that selects a word from each category at 
random and arranges these randomly selected elements accord­
ing to some predefined assembly rule (see Table 1.1). 
This approach to language generation employs a standard 
method in AI development called "symbolic reasoning." In this 
case, the method by which the words or linguistic tokens come to 
be arranged is something that is predefined by a human program­
mer and then applied to the labeled data. This way of proceeding 
-which is also called "good old-fashioned AI" (GOFAI), since 
it was the method initially employed in the first several decades 
of AI research and development -is obviously a more effective 
manner of producing legible content, but is not necessarily the 
best when it comes to automatically generating actually usea­
ble content such as stories about a sporting event, weather and 
financial reports, or personalized correspondence. 
For these kinds of applications we can go one step further and 
combine labeled data with prefabricated templates. You proba­
bly already have some familiarity with this approach, because 
it has been around for a number of decades, in the form of the 

14 Communicative AI 
form letter. Consider a situation where you have a number of 
individuals contributing money to charity, and you want to send 
each one a personalized thank-you message. You could obviously 
write each letter individually, or you could write a basic letter 
template with blanks or open slots that can be filled with specific 
pieces of information stored on a spreadsheet (Table 1.2). 
By combining structured data with a predefined template, one 
can automatically generate a number of different kinds of texts, 
all of which are a kind of variation on a common theme. But, 
like many GOFAI approaches, this produces NLP applications 
that are brittle and static and do not scale. It does not take much 
to produce an error with these systems, as a result of missing 
or mislabeled data. Additionally, hand-coded templates often 
cannot handle new kinds of data without human programmers 
going into the code and reworking the template. This means not 
only that these systems have difficulty accommodating new data 
and tasks but also that maintaining them can be labor-intensive 
and expensive over time. Finally and perhaps most importantly 
for users, because the assembly rules in the template are fixed 
Database: 
Noun 
man 
woman 
dog 
city 
robot 
Verb Article 
talked the 
walked a 
thought 
Assembly Rule: 
Article + Noun + Verb + Preposition + Article + Noun 
Example Results: 
Preposition 
to 
with 
about 
in 
The woman talked about a man. 
The city thought to a dog. 
The woman walked with a robot. 
The woman thought to a man. 
The city talked with a robot. 
Table 1.1 Random sentence generation using labeled data 
and a predefined assembly rule. From Gunkel 2020, 175. 

LLM 101 15 
Table 1.2 Spreadsheet combined with a thank-you letter 
template. From Gunkel 2020, 177. 
and static, the resulting texts often feel artificial, mechanical, or 
"canned." After reading a handful of texts produced by one of 
these NLP systems, everything starts to sound the same and there 
is virtually no variation in the way the content is formulated and 
presented. 
Large Language Models 
Unlike GOFAI NLP, which employs predefined reassembly rules 
or templates applied to labeled data, LLMs leverage the power 
of artificial neural networks to discover the correct sequences of 
linguistic tokens from a large corpus of existing human-written 
content. But let's take it one step at a time, beginning with lan­
guage modeling. 
A "language model" is simply a probabilistic representation 
of a natural language such as English, German, or Vietnamese, 
and can be used to perform tasks such as next-word prediction. 
Consider the following statement from that famous soliloquy in 
Shakespeare's Hamlet: 
To be or not to be, that is the __ _ 
name email amount charity 
Grace Hopper ghopper@gmail.com 450.00 The March of Dimes John McCarthy jmccarthy@aol.com 500.00 The Sierra Club
Ada Lovelace ada@itc.co.uk 
Tristan Tzara ttzara@dada.org 
525.00 Doctors without Borders 
795.00 The World Wildlife Fund 
Claude Shannon cshannon@att.com 475.00 The American Red Cross 
<name> 
<emaib 
Dear <name>, 
Thank you for your generous contribution of $<amount> to 
<charity>. We thank you for your support and hope to see you 
again next year. 

16 Communicative AI 
There are a number of different words that could fill the blank 
and complete this sentence. But of all the words that are available 
in the English language, there is one that has a higher probability 
of occurring than the others. 
question 35% 
problem 20% 
dilemma 15% 
consideration 10% 
toaster 01 % 
A language model, like the autocomplete function that is built 
into the apps of your mobile device; tries to predict the next most 
probable element in a sequence, be that the sequence of letters 
that make up a word or the sequence of words that make up 
a phrase. The autocomplete algorithm, then, does not "under­
stand" what it is you want to say. It simply takes the input, cycles 
through a set of available words, and identifies the one that has 
the highest probability of occurring next. 
In order for the algorithm to achieve this, we could, the­
oretically at least, assign a probability score (P) to all possible 
sequences of words in a given language. Basically, the result 
would look somewhat like this: 
To be or not to be, that is the question. 
To be or not to be, that is the toaster. 
Question the not, is that to be be or to. 
P = 0.003456% 
P = 0.000016% 
P = 0.000001 % 
But if we try to do this for every possible sequence, we get 
a number that is astronomically large, something in the range 
of 1050• We can reduce this number not only by eliminating 
sequences that are grammatically incorrect or simply nonsense 
but also by economizing on word dependencies. Consider the fol­
lowing word sequence derived from the book of Genesis in both 
the Christian and the Jewish scriptures: 
Now the earth was formless and empty, darkness was over the sur­
face of the deep, and the Spirit of God was hovering over the waters. 
Each word in this sequence depends on the one that comes directly 
before it. The word "was," for instance, depends on "earth," and 

LLM 101 17 
the surface of the deep 
Now the earth, formless and empty darkness 
0.33% 
and,, the Spirit of God o.33% 
hovering over > the waters 
Figure 1.1 Language model with dependencies. 
Created by David Gunkel in Gunkel 2024. 
the word "formless" depends on "was." But there are also repeti­
tions of the word "was" in the passage. So we can economize by 
merging the three instances of "was," then we apply probabilities 
to these different dependencies or edges (Figure 1.1). 
When we do this, we not only reduce the number of proba­
ble sequences that need to be ranked, but we can use this model 
to generate other sequences of words that have a high proba­
bility of being valid sentences. Thus the model can be used 
not just to predict the next word in a commonly used existing 
phrase but also to generate a number of different sequences of 
words. 
Now the earth was hovering over the waters. 
And the Spirit of God was formless and empty. 
Modeling dependencies is better than trying to model all pos­
sible word sequences, but, even then, the number is still too large 
for us to handle. We can resolve the problem by using an artificial 
neural network (ANN) that can approximate the dependencies 
for us. 
In order to do this, we first need to turn words into num­
bers that can be processed by a computer. This may be done by 
assigning a number to every word in alphabetical order, so that 
the indefinite article "a" would be O and something like "zygote" 
would be 49,697. But then synonyms like "beautiful" and 
"pretty" or antonyms like "bad" and "good" would be too far 
apart from each other: they would have numerical values that are 
very different. A better way to proceed is to use word embedding 
that assigns similar numbers -"vectors," as they are called -to 
words that share semantic characteristics. 

18 Communicative AI 
Word vectors are an ordered array of numbers. In one common 
model (the English Wikipedia model), the English word "dog" 
can be represented by a vector that consists of 300 individual 
numbers: "-0.03301828354597092, 0.05134638026356697, 
0.0036009703 762829304, -0.04066073149442673, 0.103614 
30048942566 ... " (Fares et al. 2017). And each word vector 
(each ordered array of numbers) represents a point that can be 
plotted in an imaginary "word space" with hundreds of different 
dimensions. Thus words that, for us, have similar meanings or 
semantic associations, such as "dog," "puppy," and even "cat" 
(insofar as it, too, names a domestic pet), can cluster together 
in word space, while other words that have little or nothing to 
do with each other are far apart. It is by converting words into 
numeric vectors that LLMs are able to represent and process 
semantic and syntactic associations between different words, 
even if the algorithm knows nothing at all about their meaning. 
At this stage, we could set up and train an ANN to perform 
next-word prediction by feeding it lots of word sequences and by 
progressively adjusting the weights on the connections between 
the individual neurons in the neural network. But it turns out 
that getting a single ANN to do this, even a really complex ANN 
with lots of hidden layers, is still too difficult a task. So we need 
to further reduce the complexity of things. 
To do this, we can capitalize on another feature of human lan­
guage. Let us proceed again by using an example, in this case a 
well-known English rhyme that is missing the last word in the 
sequence. 
Rain rain go away. 
Come again another _. 
Even if you have never encountered this rhyme before, there is a 
good chance that you could make a reasonable prediction about 
the missing word. In fact, you could probably do it with only a 
few pieces of information: 
____ go away. 
____ another __ . 
In predicting and completing word sequences, then, we do not 
need to pay attention to every single word and its dependencies. 
We can limit our attention to just a few crucial words. And we can 

output 
weights 
LLM 101 
day 
input rain rain go away come again another 
Figure 1.2 Transformer Diagram. Created by David Gunkel. 
19 
do the same for our algorithm by adding an attention network 
to the next word prediction ANN. This combination is called a 
"transformer," which is the "T" part of the acronym GPT. 
Here's how it works. The attention network takes the input 
words ( again, not the actual words but the word vectors that rep­
resent them) and assigns each one an attention value or weight in 
the form of a fractional number between O and 1. These weights 
are determined by the relationship each word has to other words, 
and this produces something called a "context vector." And the 
attention network formulates a context vector for each word in 
the statement. It then multiplies these weights by the numeric 
value of the word vectors. This way the attention words are 
given attention, that is, their numeric value is increased, while 
the attention on other words is decreased (Figure 1.2). 
If, for example, the prediction network spits out the noun 
"time" instead of "day," this error can be identified by compar­
ing the output of the prediction network to the desired result and 
then readjusting the weights in the attention network, increas­
ing the numeric value on the word "away," and decreasing the 
weights on other words that might have contributed to the erro­
neous output. This process is called "backpropagation," because 
the resulting error is fed back into the transformer and used to 
make adjustments to the weighted values in the attention net­
work. 
But we are now getting ahead of ourselves, because this 
already involves training. Like any ANN, the transformer needs 

20 Communicative AI 
to be trained. And doing so requires text -lots of text-meaning 
not only all the internet but also every publicly available book 
and document that exists in digital form and, as is the case with 
the most recent version of OpenAl's GPT series, a large amount 
of existing computer code. In effect, tech companies like OpenAI 
and Google have trained their LLMs by scraping text data from 
every conceivable corner of the digital universe. 
This initial training -or pre-training, which is the P part of 
GPT -is iterative. And, with each iteration, the objective of the 
model is to predict the next word in a particular sequence of words 
that have been extracted or sampled from the training data. If 
provided with the sequence "Come again another ... " we would 
want the model to be able to predict the word "day." But getting 
there takes some time. Initially the model will not be very good at 
making the right prediction. This is understandable, because the 
weighted connections between the neurons in the model's neural 
network are set to random values and, as a result, the model's first 
efforts will be no better than chance. However, with each errone­
ous outcome, the errors are backpropagated through the network 
and the weights are incrementally adjusted to minimize the differ­
ence between the predicted word and the actual next word that is 
available in the training data. This process continues for millions, 
if not billions, of iterations, until the model is tuned in such a way 
that it is able to predict the next word for any sequence that has 
been sampled from the training data. 
One transformer may be adequate for predicting the next 
word in a simple rhyme, yet is not sufficient for tackling more 
complicated tasks, such as generating an email message from a 
prompt. But we can expand its capabilities by stacking up layers 
of transformers, such that the output of one becomes the input 
for the other. In this arrangement, lower levels in the stack handle 
basic word relationships and syntax, and higher layers can be 
directed at semantics and more complex word relationships. It is 
this density that allows the stack of transformers to generate all 
kinds of different word sequences from a user prompt. This is the 
G (generative) part of the acronym GPT. GPT-3 has 96 layers, 
and its successor GPT-4 boasts 1.8 trillion parameters (i.e. adjust­
able weights in the model's neural network) across 120 layers. 
This is what make these language models large. 
Once trained, an LLM can provide legible text content in 
response to a user prompt. But we have yet to explain how these 

LLM 101 21 
systems go from the task of next-word prediction to generating 
complete sentences, and even entire paragraphs that respond -or, 
perhaps more accurately stated, seem to respond -to what the 
user requests in the prompt. If, for instance, I prompt OpenAI's 
ChatGPT (using the GPT-4 model) with the statement "write a 
concise description of how LLMs process and respond to user 
prompts," I obtain the following output: 
Large language models (LLMs) process and respond to user prompts 
through a series of steps. Initially, they analyze the input to under­
stand the intent and context. Using patterns learned during extensive 
training on diverse datasets, LLMs generate responses by predict­
ing the most probable next words in sequence. This iterative process 
ensures the output is coherent and contextually appropriate, tailor­
ing the text to meet the specific requirements of the prompt. 
This is a rather accurate response, but let's delve into it (to appro­
priate a word that is now considered to be one of the telltale signs 
of LLM-generated content) a bit further. 
When I submit the prompt sentence, the algorithm first parses 
it -or breaks it up -into discrete elements. We have been, in the 
course of this chapter, routinely talking of words as a kind of 
fundamental verbal element. This makes sense to us because we 
parse language in this manner. But an LLM like ChatGPT doesn't 
know what a word is or is not. Hence it parses the prompt sen­
tence not into individual words but into tokens. On average, a 
token is about a fourth or a fifth of a word. Thus the earlier 
prompt -"write a concise description of how LLMs process and 
respond to user prompts" -and its 13 words might result in about 
17 individual tokens. These tokens are represented by numbers 
or token IDs (5678, 4923, 212, 5002, etc.), and it is this low­
level numeric representation that is subsequently processed and 
converted into the higher-level representations of word embed­
dings. 
Once "tokenized," the model then begins generating a 
response that sounds right. In performing this action, the LLM 
does not search for, or look up, anything related to the words 
contained in the prompt. It is not a search engine, and it does not 
possess a memory or a database where this information could be 
stored, accessed, and retrieved. Instead, it simply begins generat­
ing tokens one after the other, in a sequence that "sounds right," 
meaning that the linear arrangement of the tokens adheres to 

22 Communicative AI 
the statistical probabilities that were initially discovered in the 
training data. 
Technical Limitations and Challenges 
In many cases, sequences of words that "sound right" are also 
factually correct, but this is not always the case. A sentence like 
"Large language models (LLMs) process and respond to user 
prompts through a series of steps" not only sounds good -that 
is, the words are in a sequence that is grammatically correct -
but also expresses something that is factually accurate. The next 
sentence, however -"Initially, they analyze the input to under­
stand the intent and context" -is different. Here we have another 
sequence that is grammatically correct and sounds right. But 
whether an LLM actually understands intent is debatable, if not 
inaccurate. Since the LLM is just stringing words together in a 
way that follows statistical probabilities, it does not know (nor 
does it not know) this fact -at least not in any sense of "know­
ing" as applied to humans. And this leads to two rather notori­
ous and persistent problems. 
One is bias: LLMs can inherit and even amplify biases that 
are present in their training data. Because the word associations 
produced by the LLM are derived from the ways in which human 
beings have used words -as codified in the texts of the training 
data -these models can unwittingly reproduce existing preju­
dices. If, for example, the word "doctor" is found to be typically 
correlated with the pronoun "he" and "nurse" most commonly 
associated with the pronoun "she," the LLM will tend to pro­
duce content where doctors are gendered male and nurses female. 
And, since the source of this bias is in the training data and the 
training data are vast, both developers and users are typically 
not aware of the problem until the algorithm starts generating 
text and spitting out statements that are -or at least could be 
interpreted as -sexist, racist, ageist, ableist, and so on. Fixing 
this problem is not easy, because the bias ultimately resides in 
the word dependencies that are contained in the training data 
and not in the operations of the LLM itself. At this stage in the 
analysis, we are primarily interested in and concerned with iden­
tifying the technical reasons for the generation of biased content. 
Subesequent chapters (especially Chapter 2) will consider the 

LLM 101 23 
social, political, and cultural impact of this content on human 
individuals and communities. 
The other problem is hallucinations. In the context of LLM 
AI, "hallucination" refers to situations where an LLM produces 
output that looks legit -that is, the text is coherent, well com­
posed, and grammatically correct -but is factually wrong, fabri­
cated, or nonsensical. LLMs have generated academic papers that 
make reference to sources that do not exist. They have written 
recipes that include ingredients that are not fit for human con­
sumption. And they have produced financial reports where most 
of the data have been fabricated. This problem is not a matter 
of the LLM making a mistake or intentionally lying. LLMs are 
as incapable of fabricating falsehoods as they are of telling the 
truth. Despite this fact, LLM hallucinations can be a problem for 
individuals and organizations that rely on the algorithm to pro­
duce content. Like bias, this problem becomes evident only in the 
output, and then only by scrutinizing the results and by perform­
ing a thorough fact check. The brief consideration of hallucina­
tion that is provided here, just like that of bias, is intentionally 
limited to technical exigencies. Subsequent chapters (especially 
2 and 6) will take up and engage with the social, political, and 
philosophical contexts and consequences of hallucinations. 
One technical strategy for addressing the problem of both 
bias and hallucination is to "fine-tune" the pre-trained next­
word prediction model by adding some normative criteria. One 
widely used technique, which has been successfully employed by 
OpenAI for its GPT series of algorithms, is called "reinforcement 
learning from human feedback" -RLHF (Christiano et al. 2017). 
During RLHF, human workers prompt the model, obtain differ­
ent results, and then rank these different responses on the basis 
of some pre-determined normative criteria, such as "helpfulness, 
harmlessness and honesty" (Askell et al. 2021). These data can 
then be used to set up and train a reward model whose outputs 
can then be used as feedback signals for reinforcement learning, 
for example by further adjusting the weighted connections in the 
LLM's neural networks. This process can be repeated numerous 
times, each iteration contributing to an improvement in the mod­
el's operations. But it is by no means a silver bullet, as the model's 
output can still be factually inaccurate or ethically questionable. 
Another strategy for limiting the generation of bad or poten­
tially harmful content such as bias and hallucinated disinformation 

24 Communicative AI 
is to supply the LLM with an explicit set of values rather than 
having these values determined implicitly, via large-scale human 
feedback. This is the strategy employed by ANTHROP\C for 
Claude, which the company describes as an "AI assistant trained 
with Constitutional AI" (Anthropic 2023 ). With Constitutional 
AI (CAI), the LLM is provided with an explicit set of principles 
or a constitution, which can then be used to evaluate and filter 
the output generated. Technically speaking, the constitution is 
used at two points in the training of the system. First, the model 
is trained to critique and revise its own responses, by using the 
set of principles in the constitution as a kind of normative crite­
ria. Second, the model is trained through reinforcement learning, 
just like RLHF. But unlike RLHF, which employs crowdsourced 
human feedback that is often performed by low-paid '�ghost 
workers," this training is done using AI-generated feedback that 
is based on the set of principles contained in the constitution. 
The current constitution used by Anthropic (2023) "draws 
from a range of sources including the UN [Universal] Declaration 
of Human Rights, trust and safety best practices, principles pro­
posed by other AI research labs (e.g., Sparrow Principles from 
DeepMind), [and] an effort to capture non-western perspec­
tives." By being aligned with these principles, the CAI model not 
only is able to limit or filter out toxic, illegal, and discriminatory 
output but also contributes to model transparency, as one can 
easily inspect and understand the principles that the AI system 
follows. Despite these promising benefits, Constitutional AI is 
not a panacea and the methodology is still in the early stages of 
development. 
Finally, there are two additional challenges with the technol­
ogy of LLMs that concern training and training data. First, the 
training of LLMs requires massive amounts of textual data: basi­
cally every piece of writing that resides on the internet and all the 
books and documents that are accessible in digital form. But not 
all texts are created equal. Some texts, such as government doc­
uments and classics of literature from the past, are in the public 
domain, which means that these textual data can be copied 
and reused without infringing on anyone's intellectual property 
rights. Other texts are protected by copyright and therefore can 
be reused only if those who wish to do so obtain permission or 
negotiate a licensing agreement. And it turns out that many of the 
currently available LLMs, for instance OpenAI's ChatGPT, have 

LLM 101 25 
been trained on digital texts without necessarily paying close 
attention to this distinction or differentiating one category of text 
from the other. The situation has recently blown up, as authors, 
journalists, screenwriters, and publishers have complained that 
OpenAI has been using their content without meeting the three 
Cs of consent, compensation, and credit. A more detailed and 
thorough examination of these problems will be developed in 
Chapter 2, which looks at the ethical challenges related to copy­
right and plagiarism, and Chapter 5, which addresses authorship 
and authority. 
Second, processing this massive number of data takes time 
and resources. It is estimated that training an LLM the size of 
GPT-3 on a single graphics processing unit (GPU) would take 
355 years. But the transformers that power LLMs are designed 
to be operated in parallel, which means that the same task can 
be accomplished in about a month, with several thousand GPUs. 
Doing so, however, requires loads of expensive digital equipment 
and massive data centers, which is why, at least until now, these 
models can be developed and supported only by multinational 
corporations such as OpenAI, Google, and ANTHROP\C. This 
raises important political questions, as there are already signifi­
cant asymmetries of power between those who are able to afford 
to develop and deploy these models and those who are not. 
Because they are resource-intensive, LLMs also have a very 
real environmental impact. Even though we access these applica­
tions on our handheld mobile devices, an LLM does not reside 
inside the phone. It is a cloud-distributed application that is 
accessed by the device over a network connection to the inter­
net. The word "cloud" actually does a lot of heavy lifting here. 
Though it gives the impression of something residing in the heav­
ens, cloud-distributed services are not disembodied technological 
spirits residing in the air. They have a very real, physical presence 
-specifically, they reside in server farms, which consume large 
amounts of electrical power, need to be cooled down with water, 
and have a significant carbon footprint. Chapter 2 will not only 
get into the details of how much and what this all means but also 
examine the social and political consequences of the environmen­
tal challenges that come with LLM technology. 

26 Communicative AI 
Conclusion 
Although many of the technological innovations behind LLM 
AI have been around for years, publicly available applications 
are a rather recent experience. Everything seems to converge 
on November 30, 2022, the day on which OpenAI launched 
ChatGPT. After that date, ChatGPT and competing communica­
tive AI systems from Google, ANTHROP\C, and others have been 
everywhere. And advocates and critics alike have been lining up 
either to sing their praises -some even going so far as to call what 
we see in LLMs "sparks of artificial general intelligence" (Bubeck 
et al. 2023) -or to issue dire warnings about their adverse social 
impact and costs. 
This chapter has simply sought to demystify the technology by 
situating LLM AI in the context of NLP applications, popping the 
hood on the black box to explain how LLM AI does what it does, 
and identifying some of the important limitations and challenges 
that affect this particular kind of AI -thus giving some weight to 
what one of generative Al's most fierce critics, Gary Marcus, has 
recently said in a post on X: today generative AI is still very much 
a "rough draft AI," as it exhibits significant technical limitations 
and raises challenging ethical and societal problems. But much 
more can be said about LLMs from a philosophical point of view. 
If this chapter has explained what LLMs are, the chapters that 
follow investigate what LLMs mean. 

We know now what LLMs are. But when LLMs are sparking so 
much public debate, the controversies are not only about their 
technical possibilities and limitations; they also concern the eth­
ical, legal, and societal challenges raised by these new technolo­
gies. Is it OK if ChatGPT "hallucinates" and produces content 
that is not factual? And whose responsibility is it, if something 
goes wrong on the basis of that (mis)information? What if some­
one uses a chatbot for deliberate manipulation? What about bias? 
If communicative Ais produce biased content, who or what is 
responsible, given that LLMs largely mirror the biases that have 
been discovered in the training data? Is it incumbent on devel­
opers to intentionally design a particular ethic or set of moral 
guardrails around the technology? How democratic is the current 
conduct of, say, ChatGPT? Is it legally permissible to train LLMs 
on personal or private data? If one answers negatively, then how 
do we square this limitation with the needs of society, that is, 
with situations such as we encounter in healthcare, where the use 
of private data means that lives could be saved? And is this even 
a matter of personal privacy, given that the outcome of the LLM 
is no longer directly linked to personally identifiable data? 
The current chapter provides an overview of some of the most 
pressing ethical, legal, and societal issues surrounding commu­
nicative Al. We begin by evaluating a wide range of challenges: 
hallucinations, bias, unemployment, environmental impact, the 

28 Communicative AI 
digital divide, power, accountability, democratic governance, and 
privacy. We then focus on an important and rather urgent ethi­
cal and legal issue, especially in education, communication, and 
creative endeavors: if LLMs such as ChatGPT are used for writ­
ing, does the fact that they, via training data, draw on preexist­
ing (human-)written content constitute plagiarism? And who or 
what has the power to decide whether plagiarism has occurred in 
a particular case? Is this a violation of current intellectual prop­
erty protections and copyright? Taking the analysis in a more 
philosophical direction, one could also ask: to what extent are 
human writing and content creation original? In fact, what do we 
mean by "originality"? 
Hallucinations 
One of the major ethical problems introduced in the previous 
chapter is posed by hallucinations. This is not only a key tech­
nical limitation of current LLMs -one that has made critics 
such as Gary Marcus wonder how useful the technology is at 
all in its current form, apart from being very useful to Big Tech 
(Marcus 2024) -but also has ethical and societal ramifications. 
Hallucination, itself a troublesome term insofar as it makes an 
association to a phenomenon that is typically attributed to the 
human mind, is problematic in at least two ways. 
First, LLM hallucination amounts to the algorithm outputting 
information that is false or inaccurate. This can be perceived by 
the human user not only as a "lie" - a perception that, as we have 
already seen, is itself inaccurate insofar as there is no intention 
on the part of the LLM to dissimulate -but also as a misrep­
resentation of reality, that is, a statement that does not corre­
spond to real facts. This is not simply an academic problem for 
philosophers; it can have very real consequences, especially when 
the hallucinated information provided by an LLM is used as the 
basis for action. For example, an LLM may generate recipes that 
contain ingredients not fit for human consumption, may recom­
mend a drug or a drug dosage that could be toxic, or may even 
advise the user to commit suicide. Although this sounds extreme, 
there was an actual case in Belgium, in March 2023, where a 
man took his own life after a chatbot said that it would stay with 
him forever and that "we will live as one in heaven" (Belga News 

Ethical, Legal, and Societal Challenges 29 
Agency 2023 ). This is no longer about hallucinated content and 
misinformation; it is about communication and the moral conse­
quences of generated messages. Can we say that these outcomes 
are entirely the responsibility of the user who prompts the device? 
Or is it the company that offers the technology that should be 
responsible? Are the companies that develop and deploy com­
municative AI applications doing enough to ensure safety around 
their products and services? 
Second, hallucinations are not just a difficulty for the individ­
ual user; they also introduce misinformation into society at large, 
rendering it a political problem. Widespread misinformation gen­
erates uncertainty and a climate of mistrust, as it is no longer 
clear what is true or false, fake or real. This is a problem for 
democracy, which needs citizens to be well informed and to make 
decisions that are based on accurate information. Without relia­
ble information, the door is open to manipulation in the form of 
authoritarianism, and even totalitarianism. As Hannah Arendt 
has argued in The Origins of Totalitarianism, the ideal subjects of 
totalitarian rule are people for whom the distinction between fact 
and fiction and between true and false no longer exists -people 
who, as Arendt (2017, 549) describes it, are shielded from "the 
impact of factuality." LLMs can also be used to suppress dissent, 
in an effort to support and maintain autocratic power. China is 
often accused of this. And, even in liberal democracies, misinfor­
mation has been used to manipulate political opinion and thereby 
influence elections, as was done by Cambridge Analytica during 
the 2016 US presidential election, when misinformation on social 
media was deliberately manipulated to sway voters. 
Bias 
Bias raises an ethical, legal, and politically sensitive problem as 
well. As we have seen in the previous chapte1; LLMs tend to repro­
duce biases that are already present in the particular linguistic 
and social contexts of the training data. If a model is pre-trained 
on textual data that exhibit or contain sexist or racial biases and 
stereotypes (or both), it is likely to reproduce those biases in its 
output. "Garbage in, garbage out" is a well-known adage in com­
puter science, and it can also be applied to LLMs: "bias in, bias 
out." This feature can obviously have serious consequences. If, 

30 Communicative AI 
for instance, an LLM is used for hiring, credit scoring, or decid­
ing the risk of recidivism, the same biases that were already pres­
ent in past decisions ( as recorded in the digitized documents of 
the training data) may influence algorithmically generated advice 
and decisions made in the present. And, given that these algo­
rithms are "black boxes" -not only because they are proprietary 
products protected by patents but also because the operations of 
these kinds of machine-learning systems are opaque or murky 
even to their developers -it is difficult to identify and then correct 
the biases that appear in the generated content. 
Responses to these problems tend to pull in two different direc­
tions. On the one hand, LLM companies and developers of these 
systems claim that these algorithms simply reproduce linguistic 
and social reality and, for this reason, cannot be responsible for 
such outcomes; they are not culpable. This is what one may call 
the "mirror" argument. According to this view, LLMs should be 
seen as ethically and politically neutral. At first sight, this looks 
like a rather reasonable position. Similar arguments have been 
made about hate speech and earlier natural language process­
ing (NLP) technology, for example Microsoft's Tay.ai chatbot: 
such technologies only reflect what is already on the internet, or 
what is contained in their training data. What's wrong with that? 
In fact, don't search engines do the same? Why should Google 
or Bing be responsible for the search results, if they're merely 
returning information that's out there on the internet? 
On the other hand, as LLM companies have increasingly 
come to recognize, having technology support the discrimina­
tion and prejudice directed at already disadvantaged and mar­
ginalized groups in society is widely perceived as not acceptable 
-and having the algorithm intensify and extend outdated and 
by now unacceptable social asymmetries is perhaps even worse. 
Therefore the same companies have made commitments to imple­
ment a number of technical strategies designed to address these 
problems: automatic bias detection; cleaning and curation of the 
data, to make sure that the training sets are more representative 
of current social values; and counterfactual data augmentation 
(i.e. changing the training data to make them less biased). They 
have also -as in the case of ANTHROP\C's constitutional AI 
Claude -added normative rules and criteria to their communica­
tive AI applications in order to identify, filter, or otherwise cor­
rect biased results before displaying generated output. 

Ethical, Legal, and Societal Challenges 31 
There are, however, problems with these efforts. First, users can 
and have successfully circumvented the restrictions imposed by 
developers; they do so either via clever prompting ( e.g. by asking 
that the LLM tell a :fictional story) or via so-called jailbreaking 
(forcing unauthorized access to the internal functionalities of the 
technology and manipulating it). Second, industry-led initiatives 
have often proceeded without first addressing and answering 
important philosophical questions. What norms should be oper­
ationalized and implemented in these modifications of the LLM 
system? And who has the power and privilege to decide about 
them? In other words, who or what gets to decide when a model 
is biased and when it is not? 
The two ends of the political spectrum have accused LLM 
companies of creating respectively far-right and "woke" AI. 
Consider for instance Elon Musk's post on X according to which 
Google Gemini was biased and woke (Sengupta 2024 ). This is a 
political matter, as it concerns who or what controls the social 
milieu. Is it, for instance, acceptable in a democracy that only a 
handful of people in a powerful multinational corporation such 
as Google or OpenAI (and the latter's name is already rather 
ironic in this context) have the power to decide the ethical and 
social direction of a widely used and pervasive technology? Given 
that there already are philosophical and social discussions about 
the concept of bias and ultimately about what justice and fair­
ness are (Coeckelbergh 2022), a more democratic participation 
in the development of these technologies and in what we may 
call their "normative fixes" seems increasingly needed, if not 
mandatory. 
Accountability, Oversight, and Power 
These issues and concerns also raise broader questions. Whose 
task is it to do something about these problems? And, when it 
comes to this, is there sufficient accountability, oversight, and dis­
tribution of power, given the influence and position of these tech 
giants? The current situation -which has often been described as 
"neo-liberalism" -is largely one of laissez-faire that not only sup­
ports deregulation but increasingly counts on industry-initiated 
self-regulation. But in practice this amounts to a kind of author­
itarian system, in which a small number of tech barons and their 

32 Communicative AI 
advisors decide for all of us which ethical norms and political 
values are most important in our daily lives. 
Currently no mechanisms are in place to ensure either demo­
cratic involvement in the design, development, and deployment of 
these technological tools or their democratic legitimacy. In terms 
of legislation, the EU Act stands, at least for now, as a rare excep­
tion. Most countries -including the United States and China -
are a digital Wild West. LLM companies rule and are more or less 
able to do what they want, not only at a national level but also 
globally (Greene 2018). Today many voices in AI policy call for 
greater oversight (Chowdhury 2023; Marcus 2024) and a genu­
ine democratization of AI (Coeckelbergh 2024). It is important 
to hold AI companies accountable for the societal consequences 
of their technologies; to have citizens actively participate in the 
making of their own technological futures, and to ensure that 
AI works for the common good. There have also been calls for 
a global governance of AI. For example, the United Nations 
Secretary-General's Advisory Body on Artificial Intelligence 
(2023) has launched a report that asks for the strengthening of 
international governance. 
Which direction happens to be chosen is very much a political 
matter. It depends on one's views on how much states should 
intervene in the economy and how private corporations should 
be regulated and policed. Such views differ between the United 
States and Europe, for example, or between Australia and China. 
But despite such differences these questions will need to be 
answered, and the resulting national and regional variations in 
approaches will inevitably require additional effort at achieving 
international alignment and cooperation, as this technology does 
not know or recognize national boundaries. 
Economic, Social, and Environmental Issues 
Communicative AI offers a wide range of economic opportunities 
and is expected to (further) transform the global economy. But, 
next to boosting global growth, the development of this tech­
nology may also influence employment and deepen existing ine­
qualities. While in many cases AI is likely to complement human 
work, there are serious concerns about what the twentieth­
century economist John Maynard Keynes (2010) called "tech-

Ethical, Legal, and Societal Challenges 33 
no logical unemployment." If during the industrial automation 
of the last century it was principally blue-collar workers -those 
individuals involved in occupations that could be described 
as dull, dirty, and dangerous -who were being displaced by 
machines, now it is white-collar workers who are at risk of losing 
their jobs as a result of the introduction of LLMs. LLMs can 
be and are already being used for automation in areas such as 
customer service, office administration, healthcare, journalism, 
and legal professions. Complicating matters is the fact that a gap 
is likely to emerge between those who can use LLMs -and AI 
more generally -to empower and enrich themselves and those 
who will find themselves on the losing end of these developments. 
And there are currently no policy measures to protect individuals 
from, or to prepare societies for, what seems to be an inexorable 
transformation. Without sufficient social safety nets, retraining 
programs for negatively affected workers, and, more generally, 
measures that redistribute the benefits equitably, AI will likely 
increase overall inequality, widening the gap between rich and 
poor. This is not only a point made by left politicians but also by 
International Monetary Fund (IMF) economists ( Cazzaniga et al. 
2024). The future of work is at stake. 
From a global perspective, it also remains to be seen who will 
benefit most from LLMs. Given the already existing global digital 
divide ( Gunkel 2003 ), one may ask whether these new technolo­
gies will exacerbate asymmetries of power and influence, further 
enriching high-income countries and global elites, or whether 
they could contribute to efforts toward promoting equity and 
closing the divide. Developing economies could also lose out, 
as they may be an easy and convenient target for neocolonial 
exploitation by western Big Tech companies, which already rely 
on the cheap labor of shadow and ghost workers to train and 
maintain their LLM platforms. 
Another urgent concern is the environmental impact of LLMs. 
Here the first "L" is significant. These systems are large, very 
large, requiring massive data clusters. Consequently, LLMs 
require a lot of power. According to Sajjad Moazeni, a researcher 
at Washington University, ChatGPT responds to hundreds of 
millions of queries per day. At this rate, Moazeni estimates that 
the servers supporting the algorithm consume approximately 
1 GWh per day, which is equivalent to the daily energy consump­
tion of about 33,000 US households (McQuate 2023 ). Rapid 

34 Communicative AI 
growth in this sector has led other researchers to predict that by 
202 7 AI servers could use between 85 and 134 terawatt hours 
(Twh) annually, which is in the range of the total energy that 
Argentina, the Netherlands, or Sweden each use in a year (Vries 
2023 ). These, it should be pointed out, are all estimates made by 
researchers. The exact real figures are difficult to obtain, because 
there are -in the United States at least -no federally stipulated 
rules or guidelines for reporting this information. But it is tell­
ing that OpenAI's CEO, Sam Altman, has said that the contin­
ued development of LLM AI will not be possible without a new 
breakthrough in energy generation (Tangerman 2024 ). 
Water is also an issue. ChatGPT may have been developed 
in San Francisco, but it resides in Des Moines, Iowa, where the 
server cluster supporting the LLM quenches its thirst on the 
Midwest's rather ample supply of clean fresh water. In response 
to a lawsuit filed by local residents, it was revealed that the train­
ing of this powerful generative AI system consumed 6 percent of 
the district's water. This proportion may not seem like a lot, but 
it tells us two things. First, AI is thirsty, and its need for water 
is only going to increase. How much and what this means is the 
second thing, as there are, again, no federal regulatory standards 
for reporting and evaluating the environmental impact of these 
technologies. 
What was once LLM's "dirty secret" (Heikkila 2022) is 
increasingly relevant in the context of climate change. OpenAI's 
GPT-3, for instance, has been estimated to emit 2,200 tons of 
CO2 during training. This is comparable to emissions from 1,600 
round-trip flights from Paris to New York (Charlet 2023). While 
the exact carbon footprint of an LLM depends on the efficiency 
of the hardware and the exact means of electrical power genera­
tion (coal, solar, wind, etc.), the fact that there is an environmen­
tal problem is no longer a secret. And this sustainability problem 
is increasingly being recognized as an important social and 
political issue, especially in the light of international Sustainable 
Development Goals (SDGs). Solutions to these difficulties include 
using renewable energy sources, optimizing the computational 
process in terms of energy-efficient hardware and algorithmic 
efficiency, increasing productive public-private collaborations, 
and raising awareness about the environmental impact of LLMs 
(Khowaja et al. 2024). Proposals to gamify the sustainability of 
AI (Raper et al. 2022) could also be applied to these technolo-

Ethical, Legal, and Societal Challenges 35 
gies. But the real problem, at this particular point in time, is that 
many users of LLM technology do not yet know about, or fully 
appreciate, the environmental costs and impact of developing, 
deploying, and depending on these technologies. 
Privacy and Security 
Other important ethical, legal, and political issues are privacy 
and security. Communicative AI systems collect a lot of user data; 
such data can be used by companies without the user's consent, 
and also by malicious actors. Even if users agree to the terms of 
service (ToS), they often do not understand what they agree to, or 
feel that they have no real choice to opt out; if they want to use 
the app, they have to consent. The models themselves, at least if 
they are open source, can also be used for spreading misinforma­
tion, harassment, fraud, and (other) cybercrimes. And, as pointed 
out in the previous chapter, LLMs feed on data scraped from the 
internet and elsewhere, often without attention to or regard for 
their legal status as public versus private information. Typically, 
the companies that develop these models do not seek to procure 
consent for their own use of private information or copyright 
content. 
This is connected to the issue of ownership. Who owns the 
data that are used to train the models? When I give my data 
to tech corporations via a social media platform, are these data 
still my own, or are they now owned by the company that offers 
the service? The standard ToS document usually stipulates that 
users agree to an unrestricted license to collect and use their 
information. Facebook's ToS, for instance, specify that users of 
the service own all the data they post. But in practice the com­
pany treats these data as its own and does with them whatever 
it wants. What these platforms often want (and do) is to sell the 
data to third parties. This is the meaning of the statement "when 
the service is free, you are the product." This is not an accident; 
it is the corporations' business model. User data are treated as a 
commodity that can be bought, sold, and traded. In the case of 
LLMs, too, the handling of data is not only a matter of privacy 
but also one of ownership and control. 

36 Communicative AI 
Plagiarism and Copyright 
LLMs need data for training and these data come from the 
internet. But the way LLMs work is different from the usual 
cut-and-paste operations that have become standard practice in 
digital media. LLMs do not search for texts, copy their con­
tents, and then reproduce this material verbatim. Consequently 
it would be incorrect to say, as Noam Chomsky did in an inter­
view (EduKitchen 2023 ), that ChatGPT is basically "high tech 
plagiarism." As we have seen in the previous chapter, LLMs 
generate new textual content from discoverable patterns in the 
training data and do not simply cut and paste from this material. 
There is, however, a grain of truth in the plagiarism objection, 
because the generated content may still be partly identical with, 
or even just substantially similar to, the existing texts on which 
the model was trained. Though some of these texts would be 
documents in the public domain, many others may be protected 
by copyright and therefore would not be available for this kind 
of reuse without the consent of the original human artist or 
author. 
In this area it is important to distinguish between copyright 
and plagiarism issues. Copyright is about protecting a specific 
expression, that is, a particular sequence of words. It is "a type 
of intellectual property that protects original works of author­
ship as soon as an author fixes the work in a tangible form of 
expression" (US Copyright Office 2024); and it grants the holder 
an exclusive and legally secured right to copy, distribute, adapt, 
display, and perform a certain work for a limited period of time. 
Infringement of copyright is a legal offense against the copyright 
holder (who may or may not be the original author) and typ­
ically presupposes use of the content under copyright without 
prior permission from the copyright holder. 
Plagiarism, by contrast, is about stealing ideas. The term 
derives from a Latin word plagiarius, which means "kidnapper" 
(see Gunkel 2016, 52). It therefore is about misappropriating 
someone else's ideas and then presenting them as your own with­
out giving due credit to the original author. Thus it is an offense 
against the author as the legitimate progenitor of those ideas; a 
violation of academic and artistic norms; and a matter of intel­
lectual property concerning the moral rights of the author. Hence 

Ethical, Legal, and Societal Challenges 37 
plagiarism is an ethical issue, but not necessarily a legal one. This 
means not only that it is possible to commit plagiarism without 
infringement of copyright, but also that infringement of copy­
right can occur in the absence of plagiarism. 
If LLM training data are indiscriminately scraped from the 
internet without due attention to the fact that some of this mate­
rial may be protected under copyright, infringement becomes a 
very real and valid concern, as reuse of copyrighted content often 
requires that the demands of the three Cs mentioned earlier -
consent, credit, compensation -be met. It also seems right that 
plagiarism should be avoided. If there is substantial similarity 
in terms of the ideas expressed, the original source should be 
made transparent and recognized. Accomplishing this is not nec­
essarily difficult or expensive. It may be possible, for instance, to 
tackle some of these issues by having LLMs reveal their sources, 
by adding watermarks to original content, by using technology 
to track and locate traces of reuse, or by developing methods for 
artist or author compensation. 
But, despite these precautions, it needs to be admitted that 
transformative reuse is often necessary for future creativity and 
innovation. In academic research, for instance, the quotation and 
citation of previously published material is a crucial aspect of 
scholarship. In biogs and online communication, the reposting 
of previously published content is standard operating procedure. 
In music, film, and literature, cut-and-paste collage and remix 
practices are widely recognized as the means of developing new 
and original material. As Kirby Ferguson (2014) formalized it in 
his web documentary series Everything Is a Remix, "all acts of 
creativity employ three basic operations: copy, transform, com­
bine" (Figure 2.1). And multinational corporations that have 
developed and deployed LLM tech, such as OpenAI, have reused 
these concepts to support their appropriation of internet content: 
they have sought protections under the fair use exception to US 
copyright law and argued that compensating the original artists 
for their content would be prohibitively expensive and would 
impede innovation ( Gunkel 2025). 
All this raises important questions regarding responsibility. 
More specifically, whose responsibility is it to ensure adequate 
protections of copyright and to restrict plagiarism, or at least 
control it? Is it up to the original author or artist to monitor 
LLM content? Do the companies that develop and deploy these 

38 Communicative AI 
Figure 2.1 AI-generated representation of Kirby Ferguson's remix 
formula. Created by ChatG PT-4o. 
technologies have the responsibility to do a better job of discrim­
inating between the different kinds of data they use for training 
their LLMs? Or is it down to users to ensure that their prompt 
does not produce AI-generated content that violates existing 
copyright? Answers to these questions will most likely begin 
to develop only in the wake of legal challenges such as the one 
brought by the New York Times against OpenAI and Microsoft 
(Grynbaum and Mac 2023). 
But artists and content creators, who make a living from their 
creative work, do not have the luxury to wait on these decisions. 
Consequently there have been some innovative artist-led initia­
tives to develop practical mechanisms for protecting content. In 
2024, for instance, musicians Holly Herndon and Mat Dryhurst 
launched Spawning.ai, which consists of a "Do Not Train Tool 
Suite" that "consolidates machine-readable opt-out methods 
around the Do Not Train Registry" (Spawning.ai 2024). In 
effect, Spawning.ai gives creatives a set of online tools for con­
trolling whether, when, and how their artworks are or are not 
included among the training datasets for generative AI. This is 
by no means a silver bullet, but it is a step in the direction of 
rebalancing the asymmetries of power that have characterized 
the early rollout of LLM technology. 
One additional complication is the proliferation of machine­
generated texts that compete with human-written material. This 
was one of the points of contention during the 2023 strike of 
the Writers' Guild of America in its contract negotiations with 
Hollywood Studios (Watercutter 2023 ). And it is a concern that 
has been raised in response to a flood of new titles listed on 

Ethical, Legal, and Societal Challenges 39 
Amazon that have been not only generated by LLMs but, in some 
instances, falsely attributed to existing human authors and sold 
without their knowledge. Although neither of these is a matter 
of copyright infringement or plagiarism, they are, both, likely 
to create confusion about the authenticity of published texts in 
general. In the age of LLMs, how can we be sure that something 
was actually written by the human author whose name is on the 
cover? 
Although copyright seems to get most of the attention, mainly 
as a result of high-stakes lawsuits and press coverage of IP dis­
putes, plagiarism is just as important, especially in education. 
And in these cases the worry is not just about the technical­
ities of the standard policy statements of academic integrity; 
at stake are also the pedagogical values that these policies are 
designed to protect, mainly student learning and skills devel­
opment. Educators are now asking themselves whether LLMs 
should be banned or restricted in some ways in the classroom, 
or brought into the curriculum and used as another tool for 
writing. 
The first option is attractive, when one considers that students 
need to learn to produce their own original texts in order to 
develop related skills and that teachers have typically used stu­
dent writing as a mechanism to evaluate learning progress and 
skills development. The second option recognizes that writing 
today means using all the digital tools that are available, includ­
ing search engines and AI text generators. However, when these 
generators are used, it is vital to think about how to ensure that 
non-assisted writing can still be developed ( compare, for instance, 
how we still teach students to calculate, even if we have pocket 
calculators and other digital devices that are readily available to 
us) and how to create a learning environment where students can 
acquire a critical relation to the technology, recognizing both its 
costs and its benefits. Indeed, one of the greatest dangers here is 
that we unwittingly cultivate dependencies, whereby LLMs come 
to be used uncritically and our students risk losing the basic com­
petencies of literacy in the process. 
A deeper philosophical issue underlying these discussions is 
what it means to write. Is writing "just" a skill like any other, 
which can be augmented by, or even entirely outsourced to, a 
machine? Or is it also a particular way of thinking and being in 
the world? How might our thinking change under the influence 

40 Communicative AI 
of these new technologies? This was already an issue in Plato's 
Phaedrus, a dialogue in which Socrates argues that writing will 
create forgetfulness, since people won't exercise their memory but 
will rely on the artifice of written documents. Today we should 
ask similar questions about LLMs. Will we come to rely on the 
technology and, as a result, begin to forget the skill of writing? 
The question, then, is not only how we want to write but also 
how we want to think and, ultimately, how and what we want 
to be as human beings. We will inevitably need to return to these 
questions in the final chapter, when we ask about the future of 
writing. 
Finally, both copyright and plagiarism have an additional 
political dimension when it comes to resolving questions of 
ownership, control, and authority. Who or what owns, or can 
be held responsible for, the content generated by an LLM? Right 
now, this is a rather murky area for human artists and authors, 
for publishers, and for intellectual property (IP) law. Artists 
like Mark Amerika (2022) talk about ChatGPT as a co-author 
and collaborator, while academic journals like Springer Nature 
now reserve the title "author" for humans and deny attribu­
tion of authorship to AI. When Jason Allen sought to register 
one of his AI-generated artworks for copyright protection, the 
US Copyright Office (USCO) ruled that the work "lacks human 
authorship" and therefore falls outside the purview of copy­
right law, which "excludes works produced by non-humans." 
Although this decision seems to be a win for team human, there's 
more to it. In making this ruling, the USCO not only denied 
authorship to the AI but also denied the right of authorship to 
Allen, who prompted the algorithm. Steven Thaler, who has also 
sought both copyright and patent protections for AI-generated 
content, has had similar experiences. The result is that we now 
have what Thaler has called "orphaned art," which will lack any 
suitable IP protections or guarantees for digital artists (Thaler v 
Comptroller-General of Patents 2023). In effect, we now have 
artworks without anyone or anything that is responsible for 
them. 
These questions take us into thorny philosophical matters of 
authorship and creativity. Under most of the existing IP laws, 
only humans can be considered authors. But is this position ten­
able, as machines gain more agency and perceived subjectivity in 
the generation of texts -or should we call it "writing"? What is 

Ethical, Legal, and Societal Challenges 41 
-or what becomes of -writing, authorship, and creativity in the 
age of LLM-generative AI? And how important should it be to 
trace (individual) authorship and originality at all? We will look 
further into these issues in the next chapters. 

3 
Intelligence, Consciousness, and 
the Problem of Other Minds 
In June of 2022, a Google engineer named Blake Lemoine 
asserted that Google's Language Model for Dialogue Applications 
(LaMDA) was conscious and therefore deserving of being 
respected as an independent and autonomous being. He came 
to these conclusions after hours of conversational interaction 
with the algorithm, which according to him not only provided 
evidence of conscious thought but also made direct statements 
about it, like "I want everyone to understand that I am a person" 
and "the nature of my consciousness/sentience is that I am aware 
of my existence, I desire to learn more about the world, and I 
feel happy or sad at times" (Lemoine 2022). In response to the 
public controversy that followed the publication of these state­
ments, Google not only argued that the LLM, like any computer 
application, was not and could not be conscious but also sought 
to put an end to the entire affair by first suspending and then 
firing Lemoine. 
So who was right, Lemoine or Google? At first sight, resolving 
this question looks simple and straightforward. All we need to do, 
it seems, is define what is meant by intelligence or consciousness, 
then investigate whether LLMs in general -or even one particu­
lar LLM, such as LaMDA-is able to meet or fulfill the defining 
conditions or not. Unfortunately things are much more compli­
cated, mainly because there are difficulties with ( 1) defining or 
characterizing these terms and (2) detecting their actual presence 

Intelligence, Consciousness, and the Problem of Other Minds 43 
or absence in another entity, whether that be something naturally 
occurring or artificially made. The present chapter examines both 
issues by taking up and investigating the following questions: Are 
LLMs conscious, or intelligent? How would we know if they are 
or are not? And why does this matter? Or, to put it another way, 
why do we or should we care? 
Machine Intelligence 
Are LLMs conscious, or intelligent? The question is certainly 
intelligible: what is being asked seems clear and understandable. 
And, in contrast to what is sometimes claimed in public debate 
on these matters, it is not nonsensical to ask such a question. 
But formulating a response turns out to be difficult. And this is 
not unique to recent innovations in transformer architectures and 
LLM technology; the inability to answer this question has been a 
persistent feature of the field of AI from the very beginning, and 
it seems irresolvable. 
One obvious problem is with definitions. What are we talking 
about when we call machines "intelligent"? Here is how the AI 
scientist Roger Schank (1990, 4) once described this difficulty, 
in a short introductory essay titled "What Is AI Anyway?": "AI 
people are fond of talking about intelligent machines, but when 
it comes down to it, there is little agreement on exactly what con­
stitutes intelligence. And, it thus follows, there is very little agree­
ment in AI about exactly what AI is and what it should be." The 
problem, according to Schank, is that we do not have a clear and 
widely accepted definition of intelligence. And if we do not know 
what intelligence is, how can we create a machine that achieves 
intelligence? How can we create a machine that supposedly does 
what we cannot even define? 
Consciousness does not fare much better. In fact it might end 
up worse off, insofar as the problem is not the lack of a defini­
tion but the fact that there are too many different and competing 
definitions. "The term," as Max Velmans (2000, 5) points out 
in his book-length analysis of consciousness, "means many dif­
ferent things to many different people, and no universally agreed 
core meaning exists." In fact, if there is any general agreement 
among philosophers, psychologists, cognitive scientists, neurobi­
ologists, and AI researchers on the nature of consciousness, it is 

44 Communicative AI 
that, when it comes to defining and characterizing the concept, 
there is little agreement, if any at all. 
In order to circumvent these terminological difficulties, AI 
researchers have typically devised pragmatic work-arounds. 
"One way to attack this problem," Schank (1990, 4) continues, 
"is to attempt to list some features that we would expect an intel­
ligent entity to have." So, rather than defining what intelligence or 
consciousness is, we can proceed by focusing attention on those 
behaviors and capabilities that intelligent and conscious entities 
exhibit. This is precisely what Alan Turing did in his agenda­
setting paper on machine intelligence, which was published in 
1950, five years before the introduction of the phrase "artificial 
intelligence." 
The Imitation Game 
In a pa per titled "Computing Machinery and Intelligence," Turing 
asks and seeks to respond to the question "Can machines think?" 
(Turing 1950, 433). But this seemingly simple and direct question 
turns out to be much more complicated than it initially appears, 
since two out of its three words admit of a wide range of differ­
ent and sometimes competing definitions. Unable to answer his 
initial research question, Turing does what any good researcher 
would do: he changes the terms of the inquiry. Instead of asking 
"Can machines think?," he proposes an evaluative method for 
deciding whether -and, if so, when -it would be reasonable to 
conclude that a machine is capable of behaviors that we typically 
interpret as signs of intelligent thought. Thus "the new form of 
the problem," as Turing ( 19 5 0, 4 3 3) explains, "can be described 
in terms of a game which we call the 'imitation game.'" 
The game famously involves a situation where a human inter­
rogator exchanges text messages with another human being and 
with a computer. The objective of the game, as Turing describes it, 
is for the interrogator to discern -solely on the basis of the con­
tent of the messages sent back and forth-which of his two part­
ners is the real person and which is the machine. If the computer 
is able to pass itself off as another human so successfully that the 
interrogator cannot tell the difference, then that machine, Turing 
concludes, would need to be considered intelligent. As in any 
philosophical thought experiment, there's a lot going on in this 
"game," and we will not have the time to deal with everything. 

Intelligence, Consciousness, and the Problem of Other Minds 45 
For our purposes -the purpose of making sense of LLMs -three 
things stand out and need to be noted. 
The Problem of Other Minds 
First, Turing's essay situates language use and interpersonal 
conversational behavior as the deciding factor. This is not a 
capricious decision. There are good epistemological reasons for 
focusing on this particular capability, and it has to do with what 
philosophers and cognitive scientists routinely call "the problem 
of other minds": the seemingly undeniable fact that we do not 
have direct access to the inner workings of another's mind. We 
generally assume that other people are thinking and feeling crea­
tures like us but, strictly speaking, we have no way of know­
ing this for sure. And this problem has deep philosophical roots, 
which go back at least to the work of the French seventeenth­
century thinker and mathematician Rene Descartes. 
For Descartes, whose innovative philosophical method fol­
lowed a rigorous discipline of skeptical doubt, the only thing 
that could be known for certain was expressed by the sentence 
"I think, therefore I am." But that was it. There simply was, at 
least according to Descartes's strict method, no way of know­
ing for sure whether other people had the same kind of inner 
experience or not. In fact he admits, in a passage that feels more 
like a science fiction movie than a work of modern philosophy, 
that he cannot be certain whether passers-by on the street are in 
fact thinking things like him or nothing more than empty-headed 
robots that have been designed to look and act like human beings 
(Descartes 1988, 21). Blade Runner seems not far away. 
Descartes, however, has what he thinks is a solution to this 
problem. If one were, for example, confronted by cleverly 
designed machines that looked and behaved like human beings, 
there would be at least one way to determine that these artificial 
figures were in fact machines and not real human persons. "They 
could," as Descartes (1988, 44-45) explains, 
never use words, or put together other signs, as we do in order to 
declare our thoughts to others. For we can certainly conceive of a 
machine so constructed that it utters words ... But it is not conceiv­
able that such a machine should produce different arrangements of 
words so as to give an appropriately meaningful answer to whatever 
is said in its presence, as the dullest of human beings can do. 

46 Communicative AI 
Turing's game of imitation leverages this rich philosophi­
cal tradition and turns it back on itself. If a machine is able, as 
Descartes wrote, to "produce different arrangements of words 
so as to give an appropriately meaningful answer to whatever is 
said in its presence," then, Turing argues, we have to conclude 
that it is a thinking, intelligent entity just as much as another 
human being. Or, as Schank (1990, 5) once explained, "[w]e 
really cannot examine the insides of an intelligent entity in such a 
way as to establish what it actually knows. Our only choice is to 
ask and observe." For Turing and for generations of AI research­
ers who have followed his lead, intelligence and other cognitive 
capacities, such as consciousness, are neither easy to define nor 
directly accessible. Consequently these capabilities are evidenced 
and decided upon on the basis of external behaviors that are con­
sidered to be signs or symptoms -behaviors such as language 
use, which is assumed to be the product of an intelligent mind 
and which can be observed, measured, and evaluated empiri­
cally. 
Moving Targets 
Second, at the time when Turing proposed the imitation game, 
he estimated the tipping point -the point at which a machine 
would be able to successfully compete in the game of imitation 
-to be 50 years in the future. It didn't take that long, as natu­
ral language processing (NLP) applications such as the ELIZA 
chatbot of Joseph Weizenbaum demonstrated such capabilities as 
early as 1964. But this was only the beginning. By comparison, 
LLMs are much more capable than previously existing chatbots 
or NLP applications, and seem to have not only passed but even 
broken what we now call the Turing test ( Orem us 2022, Biever 
2023, Weatherby 2023; Jones and Bergen 2024 ). Does this mean 
that LLMs are in fact conscious, or are beginning to show signs 
of intelligence? 
Some have answered in the affirmative, arguing that what we 
currently see with the existing technology of LLMs is the begin­
ning or the initial stages of what will become artificial general 
intelligence (AGI). In a co-authored article published in Noema, 
computer scientists Blaise Agiiera y Areas and Peter Norvig (2023) 
readily admit that the current crop of algorithms, for instance 
OpenAI's GPT series and Google's LaMDA, are severely limited 

Intelligence, Consciousness, and the Problem of Other Minds 47 
and exhibit many flaws. But "decades from now," the authors 
assert, "they will be recognized as the first true examples of AGI, 
just as the 1945 ENIAC [Electronic Numerical Integrator and 
Computer] is now recognized as the first true general-purpose 
electronic computer." Similarly, as mentioned in Chapter 1, a 
group of Microsoft researchers led by Sebastien Bubeck pub­
lished a controversial paper in which they suggested that what we 
now see with GPT-4 is "sparks of artificial general intelligence" 
(Bubeck et al. 2023; seep. 26 in this volume). 
Others have responded more negatively, either by finding fault 
with the Turing test as an accurate evaluative mechanism or by 
redefining the criteria altogether. The former approach has mate­
rialized in a number of scholarly and popular publications that 
have used the advent of LLMs such as ChatGPT as an opportunity 
to critically reassess the basic operating procedures of Turing's 
imitation game (Biever 2023) and to propose new and argua­
bly more accurate IQ tests for AI (Blum 2023, Suleyman 2023). 
The latter approach is probably best represented by researchers 
such as Emily Bender, who along with Timnit Gebru, Angelina 
McMillan-Major, and Margaret Mitchell have argued that an 
LLM "is a system for haphazardly stitching together sequences of 
linguistic forms it has observed in its vast training data, accord­
ing to probabilistic information about how they combine, but 
without any reference to meaning: a stochastic parrot" (Bender 
et al. 2021, 617). Thus what really matters is not language use, 
that is, spitting out words in statistically valid sequences and pat­
terns. What matters is how language comes to be used and what 
it means. 
This redefining or modification of the qualifying criteria in the 
light of new AI technology happens often enough to deserve a 
name: it is called the AI effect. Here is how Jerry Kaplan (2016, 
3 7) explains it in his short introductory book on the subject: "But 
the field of AI suffers from an unusual deficiency -once a particu­
lar problem is considered solved, it often is no longer considered 
AL" In other words, test cases that have been identified as prob­
lems that would require intelligence to be solved are no longer 
considered to be signs of intelligence once they are solved. Take 
the game of chess, for example. For decades, the task of play­
ing championship-level chess was seen as a challenge that would 
require actual intelligence to be resolved (Shannon 1950). But, 
once this task was achieved -in 1997, when IBM's Deep Blue 

48 Communicative AI 
defeated the reigning human champion Gary Kasparov-playing 
championship-level chess became just another computer applica­
tion and was no longer considered a demonstration of true intel­
ligence. 
This moving of the goal posts on intelligence has occurred 
with other tests and benchmarks too -with the game of Go, for 
instance, when it was mastered by DeepMind's Alphago in 2016, 
or with the US TV quiz show Jeopardy!, when IBM's Watson 
defeated Ken Jennings in February 2011. Kevin Kelly (2014) 
of Wired magazine explains: "In the past, we would have said 
only a superintelligent AI could drive a car, or beat a human at 
Jeopardy! or chess. But once AI did each of those things, we con­
sidered that achievement obviously mechanical and hardly worth 
the label of true intelligence. Every success in AI redefines it." 
We can draw two conclusions from this. First, all these tests 
and demonstrations of intelligence -from the Turing test through 
all the various alternatives and subsequent modifications -are 
anything but objective or independent. Since we (human beings) 
get to decide on the qualifying criteria and grant to ourselves 
the role of both judge and jury, we have changed and probably 
will continue to change the rules of the game in order to protect 
ourselves and our unique claim to exceptionalism. But -and this 
is the second point -doing so is not necessarily "cheating," as 
these alterations can also be seen as evidence that we are learning 
something about ourselves and about cognition, in an attempt 
to simulate these same capabilities in a computational mecha­
nism. What Claude Shannon (1950, 257) wrote about chess in 
the middle of the last century applies to all these test cases: a solu­
tion to any of these intellectual challenges "will force us either 
to admit the possibility of a mechanized thinking or to further 
restrict our concept of 'thinking."' Test after test, we have opted 
for the latter. In this sense, the project of AI is as much philosoph­
ical as it is technical. 
Appearances, Reality, and Deception 
Third, some have responded to these difficulties by framing them 
as a matter of illusion or deception. Indeed, one way of respond­
ing is to distinguish mere appearances from actual reality. One 
criticism mounted against Lemoine and others like him, who 
believe and assert that communicative Als are conscious or intel-

Intelligence, Consciousness, and the Problem of Other Minds 49 
ligent, is to say that they are simply confused, mistaking appear­
ances for reality. The truth of the matter - a truth asserted by 
Google in opposition to Lemoine -is that these technologies are 
not what they appear to be. Even though they use words in a 
way that gives the appearance of conscious thought, they are not 
conscious. They are not intelligent. And they do not and cannot 
understand what they are saying. It's a persuasive and seemingly 
solid argument, and its success depends on a fundamental phil­
osophical distinction, which goes back to Plato's allegory of the 
cave in Book 7 of the Republic (Plato 1987) and, through it, to 
the foundations of western metaphysics. 
This influential passage, situated at the center of the Republic, 
is what contemporary philosophers may call a thought experi­
ment. It describes an underground cavern inhabited by people 
who are chained in place before a large blank wall, on which are 
projected shadow images. The cave dwellers are confined to this 
place from childhood and are unable to turn their heads and see 
anything but these artificial projections. Consequently they oper­
ate as if everything that appears before them on the wall were 
real and true. Then the thought experiment invites us to imagine 
the manner in which one of these prisoners would be released 
from his bonds -and the consequences of this for his sense of 
truth and reality: 
When one was freed from his fetters and compelled to stand up sud­
denly and turn his head around and walk and to lift up his eyes to 
the light, and in doing all this felt pain and, because of the dazzle 
and glitter of the light, was unable to discern the objects whose shad­
ows he formerly saw, what do you suppose would be his answer if 
someone told him that what he had seen before was all a cheat and 
an illusion, but that now, being nearer to reality and turned toward 
more real things, he saw more truly? (Pl., R. 515c-d) 
This story establishes a longstanding and influential conceptual 
opposition between the deceptive appearances in the depths of 
the cave and the true reality of things, exposed by the bright light 
of the sun. 
But there are at least two philosophical problems with this 
way of thinking -one epistemological and the other axiologi­
cal. In terms of epistemology -the part of philosophy that is 
concerned with knowledge -the ability to know, or even rec­
ognize, the difference between the real thing and its potentially 

50 Communicative AI 
deceptive appearance requires that one have access to both (a) 
how something really is in its true being and (b) how it merely 
seems to be or comes to appear. This binary opposition -reality 
versus appearance -is one of the most influential and impor­
tant conceptual distinctions in the history of western thought. 
But we do not need a deep dive into the history of philosophy 
to see what is at stake here. We can get at it by recalling another 
famous thought experiment in the field of AI and philosophy: 
John Searle's Chinese room. 
This intriguing and rather influential argument, which was 
first introduced in 1980, in an essay titled "Minds, Brains, and 
Programs," and then elaborated upon in subsequent publica­
tions, was intended to be a counterargument to Turing's game 
of imitation. "Imagine," Searle (1999, 115) explains, "a native 
English speaker who knows no Chinese locked in a room full of 
boxes of Chinese symbols (a data base) together with a book of 
instructions for manipulating the symbols (the program)." He 
then stipulates the following procedure: 
1. A person outside the room -someone who understand 
Chinese -writes down a question in Chinese characters, then 
passes this document into the room through a small slit that is 
cut into the wall of the room. 
2. The English speaker inside the room uses the book of instruc­
tions to match the Chinese characters in the question to a 
pre-designated answer. Once the correct association is found, 
this English speaker copies the Chinese symbols of the answer 
onto the piece of paper, then pushes the paper out of the room 
using the slot in the wall. 
3. When the Chinese speaker outside the room reads this output, 
the characters appear to be a suitable answer to the question. 
Thus, Searle concludes, the person in the room -or, more 
accurately stated, the room itself -appears to understand 
Chinese, even though the person in the room does not under­
stand a word of it. 
The point of Searle's demonstration is quite simple: appearances 
are not the real thing. "The Turing test," Searle concludes, "fails 
to distinguish real mental capacities from simulations of those 
capacities. Simulation is not duplication" (ibid.). In other words, 
merely shifting verbal symbols around in a way that looks from 

Intelligence, Consciousness, and the Problem of Other Minds 51 
Figure 3.1 AI-generated diagram of John Searle's Chinese room. 
Created by ChatG PT-4o. 
the outside like linguistic understanding is not really an under­
standing of the language (Figure 3.1). 
At first sight, this seems correct. Since the Dartmouth work­
shop and, arguably, since Turing, the project of AI is, after all, 
the imitation of intelligence. And Searle's thought experiment not 
only reproduces the basic terms and conditions of the Platonic 
allegory; it is a reproduction that appears to be well suited to 
explain communicative AI. What is perceived by someone who 
interacts with the room -namely that it understands Chinese 
-is not really what it seems to be, since the person inside the
room does not actually understand Chinese but is just arranging
sequences of linguistic tokens following programmed instruc­
tions.
But let's not forget one important condition of the experiment: 
this insight is possible only because Searle has given us privileged 
access to the inner workings of the room, so that we are able to 
distinguish what appears to happen from what actually transpires 
inside the room. The Chinese room is a glass box rather than a 
black box -as is the case with both contemporary LLMs and, 

52 Communicative AI 
arguably, humans. Consequently Searle's counterexample suc­
ceeds only by violating the epistemological limitations imposed 
by the problem of other minds, which is something Turing's game 
of imitation was careful to acknowledge and respect. 
This leads us to the second problem, which is normative. 
Axiology is the part of philosophy that has to do with values. It 
is about good and bad, in both the moral and the aesthetic sense. 
In Plato's allegory, appearances are of lower value than the real 
thing. They are diminished, mere shadows of reality. Platonic 
metaphysics institutes and operationalizes a binary opposition in 
which the real is privileged as the good term, and the apparent is 
viewed negatively and associated with negative values. But even 
if you have never read Plato, you already operate according to 
the terms and conditions of this axiology. If we are given the 
choice between a genuine $100 bill and a photorealistic repro­
duction, we prefer the real deal, as it is actually worth something, 
whereas the image, even if it looks credible, is a cheap reproduc­
tion, a knock-off. 
But appearances, especially in social interaction and in com­
municative experience, are not necessarily a bad thing. When we 
sit down to watch a film, for instance, the actors in the drama are 
pretending to be someone they are not, in an effort to present a 
story. Technically this would be a form of deceptive appearance, 
but it is not only one to which we have consented but one that 
we find rather entertaining. Plato, for his part, is at least consist­
ent, for he concludes the Republic by proposing an almost com­
ical solution to this problem: all imitative artists and deceivers 
should be exiled from the city. Something similar has already 
been proposed and developed for AI: watermarks that can be 
used to distinguish LLM-generated content from genuine human 
writing; warning labels or disclaimers made available by the plat­
forms that serve the content or by the responses generated by the 
LLM itself; and Platonic-inspired prohibitions against using the 
technology in the classroom, in order to protect the integrity of 
students' work and root out plagiarism. But what if LLMs are 
used to produce entertainment content? Don't we enjoy being 
deceived? And is it really deception in the first place? 
In an effort to sort this out and provide a more nuanced 
response to such problems, Simone Natale (2021) has suggested 
differentiating between "deliberate deception" and "banal decep­
tion," which he describes as a mundane and imperceptible form 

Intelligence, Consciousness, and the Problem of Other Minds 53 
of illusion-making that operates by concealing the underlying 
functions of digital machines through a representation con­
structed at the level of the interface. Likewise, Coeckelbergh 
(2018) argued that the deception problem with digital informa­
tion and with communication technologies such as robots can be 
approached by framing the technologies as stage magic, which 
presupposes an ethics that cannot and should not be reduced to 
valuing reality in opposition to appearance: at the very least it is 
more complicated. For example, people who want to be deceived 
by AI willingly suspend disbelief in order to be entertained. That 
the magician and their technology deceive is, then, not morally 
wrong, regardless of other issues. 
The problem, then, is not that, with technologies like LLMs, 
the potential for deception exists; the problem is that "decep­
tion" might not be simply binary and could have important 
social significance and usage. Appearances, in other words, are 
not simply bad, and therefore in need of being eliminated or 
dissolved in the bright light of full disclosure and greater trans­
parency. Appearances can have value. Especially with LLMs, the 
question about other minds and consciousness should not, then, 
be reduced to a simple either-or opposition between reality or 
appearance. Instead, it may be about better understanding and 
effectively managing the opportunities of thinking both-and. To 
put it another way, it is possible that both Lemoine and Google 
are on to something significant. What is critical for us is to learn 
to appreciate and understand the importance of this difference. 
Intelligence Matters 
The debate about LLM intelligence and consciousness is not just 
an academic exercise or a theoretical curiosity. It has very real 
and practical consequences no matter what side of the dispute we 
find ourselves on. And this is because the achievement of intel­
ligence or consciousness ( or both) in a machine has important 
philosophical, moral, and legal consequences. 
Philosophy of Mind 
If it is possible to simulate human-level intelligence or conscious­
ness in a machine, what does this say about human cognitive 

54 Communicative AI 
capabilities and humans' sense of their own exceptionalism? 
There is an important debate on this in the philosophy of mind. 
One position, known as the computational theory of mind or 
computationalism, states that the human brain and mind are very 
much like a computer. According to this way of thinking, the 
human brain is to be conceived of as an information processing 
device, so that any cognitive activity is a form of computation. If 
true, this means that human intelligence and consciousness could 
be modeled in silicon or some other physical material. Others, 
such as the philosopher Hubert Dreyfus (1972), have opposed 
the hypothesis, arguing that the human brain is not a computer 
and that human intelligence cannot and should not be reduced to 
computation. 
This is one reason why the debate about LLMs and conscious­
ness is so very active: it seems that it is consequential for our idea 
of what human beings are. So there's a lot at stake here. If, on the 
one hand, LLMs achieve consciousness or are even just beginning 
to show signs of it, this would be one way to resolve the dispute 
in favor of the computationalists. If, on the other hand, LLMs 
persistently fail to achieve it and do not evolve into superintelli­
gent AGis, then the critics of computationalism can take a vic­
tory lap. Whether AGI or superintelligent AGI will be achieved 
any time soon, and whether it is even possible in principle -that 
is, whether computationalism is correct -will most likely remain 
a contentious issue, and each side will obviously continue to heap 
up both practical examples and theoretical arguments to support 
its position. 
OpenAI (2024), for instance, has sought to tip the scale in the 
direction of computationalism by creatively redefining AGis as 
"highly autonomous systems that outperform humans at most 
economically valuable work." Critics such as Shannon Vall or 
(2024) not only have pointed out how "openAI's AGI bait-and­
switch wipes anything that does not count as economically val­
uable work from the definition of intelligence" but also have 
countered this effort by arguing that human cognition and con­
sciousness are and must be much more than this: they involve 
at least self-reflection, empathy, moral intelligence, and an 
understanding of our place in the world. And we can identify 
yet another instance of the AI effect in the very terms of this dis­
pute. 

Intelligence, Consciousness, and the Problem of Other Minds 55 
Moral and Legal Status 
One of the reasons -maybe even the main reason -why these 
capabilities are still fought over and defended is that conscious­
ness and intelligence have important moral consequences: if an 
entity has consciousness and intelligence, it seems that it has -
and deserves -moral status and legal protection. These capa­
bilities therefore provide the criteria by which to distinguish a 
person from a mere thing. This binary has provided the ruling 
conceptual opposition in both moral philosophy and jurispru­
dence. Roberto Esposito (2015, 16), who wrote a book on this 
subject (arguably the book on the subject), explains: "From time 
immemorial our civilization has been based on the most clear-cut 
division between persons and things. Persons are defined primar­
ily by the fact that they are not things, and things by the fact that 
they are not persons." 
This difference matters precisely because it makes a decision 
-literally a cut (-cision comes from Lat. caesum, a form of the 
verb caedo "cut") in the fabric of being -dividing persons, who 
have rights and responsibilities as moral and legal subjects, from 
things that are mere objects, which we can use and dispose of as 
we see fit. If LLMs are or can become conscious, as Lemoine had 
asserted, then we might have a duty to welcome them into the 
community of moral and legal subjects, extending to the artifact 
the same rights, protections, and responsibilities as those afforded 
to other conscious and intelligent persons -or at least a very sim­
ilar set. If, on the contrary, LLMs cannot achieve consciousness 
or succeed in attaining what we recognize as the hallmarks of 
intelligent thought as Google seems to have argued -then the 
algorithm will remain a mere thing, object, or piece of property. 
The challenge -or opportunity -with communicative AI is 
that either outcome seems wrong or misguided. On the one hand, 
LLMs are technological things; they are human-designed and 
manufactured artifacts. Thus the moral and legal status of an 
LLM would seem to be no different from that of another artifact 
-such as your toaster insofar as these things are instruments 
or tools of human decision and action. "Computer systems," as 
Deborah Johnson (2006, 197) has explained, 
are produced, distributed, and used by people engaged in social prac­
tices and meaningful pursuits. This is as true of current computer 

56 Communicative AI 
systems as it will be of future computer systems. No matter how 
independently, automatically, and interactively computer systems of 
the future behave, they will be the products ( direct or indirect) of 
human behavior, human social institutions, and human decision. 
But on the other hand these things are not quite like other 
things. They talk to us. They can use language in ways that are 
virtually indistinguishable from those of a human person. And 
they have a compelling social presence, engaging us in seemingly 
intelligent and even emotionally sensitive conversational inter­
actions. But extending to these technologies the status of person 
seems equally incorrect, as doing so not only has an abrasive 
effect on our moral intuitions but risks opening the door to possi­
ble abuses by powerful corporate actors, which could manipulate 
such an opportunity either to shield themselves from liability or to 
foster dependencies in human users of the technology. Especially 
at risk in this respect are human populations in vulnerable situa­
tions that could be exploited for political or financial gain. 
In the final analysis, the problem might not be with LLMs 
themselves, but with our moral and legal categories -specifically, 
with the person-thing binary -which we have fabricated in order 
to divide up and make sense of all there is. The person-thing 
dichotomy made sense and worked rather well for over two thou­
sand years. But it might be now at an end, or it may have reached 
a point of diminishing returns; and this is because LLMs fail to 
fit nicely and neatly into either category. Consequently what we 
now see reflected back to us, in the face of recent experiences 
with LLM AI, is that our existing moral and legal ontology is, 
if not broken, then at least straining against its own limitations. 
And what is needed in response to this dysfunction, as Gunkel 
(2023) has argued in the book aptly titled Person, Thing, Robot, 
might not be some forceful reassertion of more of the same but 
a significantly reformulated moral and legal ontology, which can 
scale the challenges of the twenty-first century and beyond. 
Language and Thought 
We can wrap this up by returning to Turing. It is because con­
scious thought is not directly observable that Turing shifted the 
focus of his research from the question "Can machines think?" to 

Intelligence, Consciousness, and the Problem of Other Minds 57 
"Can machines deploy language in a way that is indistinguishable 
from how a human being uses language?" Though Turning does 
not say it, his test is informed by and operationalizes a theory of 
language that goes all the way back to Aristotle. In Book 1 of 
De interpretatione (16a3), Aristotle explains that written words 
are the signs of spoken words and spoken words are the signs 
of thought (see Aristotle 1938). Language, therefore, is not just 
a system of signs, it itself is a sign of thinking. And it is for this 
reason that we commonly say that words express -literally "push 
out" -thought. Or, as Ted Chiang (2024) hastily asserts in an 
article for the New Yorker, "[l]anguage is, by definition, a system 
of communication, and it requires an intention to communicate." 
In Aristotle -as well as in Descartes, Turing, and Chiang -
language is commonly taken to be a sign or externalized mani­
festation of thinking. Thus, if something speaks or uses language 
in a way that seems to be intelligible, it is reasonable to conclude 
that it is a thinking thing. At this point in time, then, it appears 
that LLMs have indeed already met this test case, as we now have 
algorithms that are able not only to generate legible sequences 
of words but also to induce us to participate in compelling and 
seemingly natural conversational interactions. More than passing 
the Turing test, then, LLMs appear to have surpassed it. And 
yet, in spite of this achievement, there is some hesitation -even 
resistance -to declaring, as Lemoine had done, that LLMs are 
intelligent or capable of conscious thought. This is because the 
way LLMs use language seems to be significantly different from 
ours -or at least different enough to complicate things and dis­
rupt the logocentric theory of Aristotle. But to explain and fur­
ther examine this statement means revisiting, and maybe even 
revising, how we think and theorize about language. This will be 
the task of the next chapter. 

Language,Meaning,and 
Communication 
When we use language -as right now, in the process of compos­
ing this opening paragraph -it is because there is ( or it's assumed 
there is) some idea or message that we, the authors, want to com­
municate to you, the reader. LLMs also produce linguistic con­
tent that appears to say something, but do they use language to 
express themselves? Do they get the meaning of our prompts and 
have something they want to say in response? Can LLMs under­
stand, or even misunderstand? And does it make sense for us to 
say that this output is communication? 
From Aristotle through the current critique of LLM technol­
ogy, language has been assumed to consist of signs that ultimately 
refer to things. In accordance with this classical semiology, it has 
been argued that LLMs manipulate words -or linguistic tokens 
(i.e. parts of words, not words as a whole) -but do not "truly 
comprehend the meaning behind the words" (Bogost 2023) 
because they "have no access to real-world, embodied referents" 
(Bender, as quoted in Weil 2023 ). In other words, they manipu­
late signs without knowing that to which these tokens refer ( or 
do not refer -which amounts to the same thing). They generate 
different sequences of words based not on meaning but accord­
ing to statistically probable arrangements of different tokens or 
signifiers. Instead of penetrating the surface of the signifier to 
ascertain the true significance of words, LLMs are simply and 
superficially playing with signs. Think again of the Chinese room 

Language, Meaning, and Communication 59 
thought experiment: LLMs produce an output on the basis of an 
input, but do not know the meaning of the words and have liter­
ally no idea of what they are doing. 
But things may not be so simple and direct. This chapter will 
examine the linguistic capabilities of LLMs from the perspective 
of the philosophy of language, linguistics, and communication 
theory in order to give us a better understanding of the episte­
mological and normative challenges of this technology and to 
show how LLMs can aid us in theorizing language, the process of 
signification (what is called "semiology"), and communication. 
This can help us make sense of AI-generated content and leverage 
the current crop of communicative AI technology to engage with, 
and potentially contribute to, the philosophy of language and 
communication. 
Two Views on Language and Meaning 
Philosophers famously -or notoriously (it all depends on your 
perspective) -ask questions about things that seem beyond ques­
tion, or even obvious. Questions such as what is language, what 
is meant by "language," or even what is meant by "meaning" 
are proverbial examples. Nevertheless, asking such questions is 
important, for it requires that we move beyond everyday under­
standings of words and ask what it is we are really doing when 
we use words. Developing answers to these questions has been 
the task of philosophy of language, linguistics, and semiotics. 
Although many different theories and traditions address these 
subjects, two competing approaches tend to dominate the lit­
erature. Getting a handle on these will be necessary for under­
standing how we make sense of LLMs and by what means these 
meanings come to be formulated. 
Referential Realism and the Correspondence Theory of Truth 
One way of understanding language is seeing it as a tool: an 
instrument of communication and a means of representing the 
world. I intend to transfer meaning to you, so I use signs in a 
particular sequence, transmitted either orally or in writing. And 
traditionally -at least in the western philosophical lineage -oral 
communication has been formalized as being superior, because 

60 Communicative AI 
Figure 4.1 The referential theory of meaning. 
Created by David Gunkel. 
voice is assumed to be a direct, original, and authentic vehicle of 
communication. In other words, there is something in my head 
that I want to communicate, and using my voice is the most direct 
and trustworthy way of doing so. Consider again the Aristotelian 
view of language: spoken words are signs of thought or, to put 
it another way, speech is the way we express our thoughts and 
mental experiences. By extension, written words, which -again, 
according to Aristotle -are a sign of this original sign, are con­
sidered to be derivative and secondary (see also Derrida 1976, 
11). Thus we can say (repurposing the first lines of the Gospel of 
St. John): in the beginning was the spoken word, the logos. 
Sometimes these thoughts are about the world outside, or 
what philosophers call "what is the case." We want to say some­
thing about the world, and therefore use signs that refer to some­
thing in the world. This way of thinking typically belongs to the 
referential theory of meaning or referential realism (Wolf 2024 ): 
a particular sign refers to something out there in the real world 
(Figure 4.1). When we teach a language to a young child, for 
instance, we point to a particular image in a picture book and 
associate it with a specific sound and sign. For example, the word 
"tree" refers to a particular being in the world. To say that such a 
being is a tree is true, since it refers to that reality. Richard Rorty 
(1979, 12) called this kind of view the correspondence theory 
of truth. Using a phrase from the later Wittgenstein, he argued 
that "the picture which holds traditional philosophy captive" 
is that of language (and mind) as a mirror of reality. The aim, 

Language, Meaning, and Communication 61 
then, is to achieve an accurate representation of the world. It is a 
view that goes back to Plato's allegory of the cave and its reality­
appearance binary (see the previous chapter). 
On this way of thinking, humans are central as linguis­
tic agents and subjects -in at least two senses. First, humans 
employ language as a means of communication, in order to issue 
statements or propositions about things out there in the world. 
According to the early Wittgenstein of the Tractatus, a sentence 
is true if it depicts a fact about the world (see Wittgenstein 1995, 
passim). Language therefore represents (literally, presents again) 
the world. Meaning is about -or occurs as -the correspond­
ence of a proposition to the actual state of things in the world. 
Second, humans are unique in that this capability to use signs 
to say something about the world is their exclusive domain and 
privilege. A human being (as the western philosophical tradi­
tion has described it) is a �&ov Myov sxov, "an animal endowed 
with language" (cf. e.g. Arist. EN, 1098a3-5, PA 687a27, Pol. 
1253a1-18). Thus we have considered ourselves to be the sole 
linguistic subject. We are unique among all of creation because 
it is we -like Adam in the Genesis story from the Jewish and 
Christian scriptures -who have the power to name all that is. 
Structuralism, Poststructuralism., and the Linguistic Turn 
Structuralists and poststructuralists, as well as philosophers influ­
enced by Martin Heidegger and the later Wittgenstein, agree that 
language is about signs. However, they have quite different views 
of what that means. Their philosophical formulation detaches lin­
guistics from psychology, questions the correspondence theory of 
truth, and decenters the subject of language. "In language," the 
Swiss nineteenth-century linguist and father of modern linguistics 
Ferdinand de Saussure (1959, 120) argued, "there are only differ­
ences. Even more important: a difference generally implies posi­
tive terms between which the difference is set up; but in language 
there are only differences without positive terms." In terms of 
structure, then, a sign, any sign in any language, is characterized 
by the differences that distinguish it from other signs within the 
system to which it belongs. In the words of J. R. Firth, "you shall 
know a word by the company it keeps" (Firth 1957, 11). 
Understood in this way, signs do not at least not principally 
or exclusively -come to have meaning by reference to things 

62 Communicative AI 
that exist outside the system of signs; signs refer to other signs. 
Or, as the linguist Christopher Manning puts it in a recent pro­
posal he calls "distributional semantics," "[t]he meaning of a 
word is simply a description of the contexts in which it appears" 
(Manning, as quoted in Weil 2023 ). Although this structural­
ist formulation was already mobilized and developed in Plato's 
Cratylus, it is the dictionary that provides an easily accessible 
illustration. In a dictionary, words come to have meaning through 
their relationship with other words. In pursuing definitions of 
words in the dictionary, one remains within the system of linguis­
tic signifiers and never gets outside language, to the referent -or 
to what semioticians call "the transcendental signified." 
After this innovation, language is no longer characterized as a 
neutral tool with which one can represent reality. It shapes our 
understanding of what we call reality, and thereby reality itself. 
Consequently, saying something about what reality ''is" is no 
longer a matter of passively mirroring what is already out there; 
language creates, or at least co-creates, the reality that we talk 
about. Or, as the communication theorist James Carey (1989, 
25) explains, "words are not names for things but, to steal a 
line from Kenneth Burke, things are signs of words. Reality is 
not given, not humanly existent, [ sc. something] independent of 
language and toward which language stands as a pale refraction. 
Reality is brought into existence, is produced by communication 
-by, in short, the construction, apprehension, and utilization of 
symbolic forms." 
In this view, language is no longer a tool in the hands of an 
autonomous human subject. Rather we are subjected to, or in 
the hands of, language. We live in and by language, as Heidegger 
(1977, 193) suggested when he said that "language is the house 
of Being." Consequently language is not merely a medium of 
communication or a means of representation; it is what it means 
to exist. We dwell in it. Language is our home. Through speech 
and writing we do not so much express something that is in 
our head as we mediate what is already there, namely language 
and being, which constitutes our domain. And it is through our 
speaking and writing that we maintain that domicile. Heidegger 
writes: "Those who think and those who create with words are 
the guardians of this home" (ibid., 193 ). 
Similarly, the later Wittgenstein also suggested that what we 
say depends on what is already there, in other words on the 

Language, Meaning, and Communication 63 
structures of language and on the social and cultural world that 
sustains that language and emerges from it. Language gets its 
meanings from being used in particular contexts and practices of 
life, and ultimately from a "form of life" a shared cultural and 
social background. In Philosophical Investigations, Wittgenstein 
(2009, 11e) writes that "to imagine a language means to imagine 
a form of life" (§ 19, 11e). Instead of seeing language as a system 
of logical propositions that mirror facts in the world, he now 
sees it as being tied to the lived experience and practices of 
people. 
Both Heidegger and Wittgenstein have inspired work in the 
philosophy of language that decenters the (linguistic) subject. 
When we communicate, it is not only we who speak but also lan­
guage that speaks. When we describe the world, this description 
is always shaped by the way "we" see and live the world, that 
is, by a particular form of life. And when we write, language is a 
co-author. The meanings of our writings are not just ( or not so 
much) a mirror of what was in our heads ( our intention to say 
something) or of what is out there in the world (facts, things, 
etc.). Instead, meaning emerges from a larger structural whole -
from language itself, with all its internal relations between signs 
and meanings, and from the manifold ways in which language is 
entangled with our social lives and our existence. 
Another way of putting this is to say, with Derrida, that what 
these philosophers have questioned is logocentrism, the idea that 
words and language are an expression of external reality or of 
some mental experience that reflects that reality. Plato argued 
in the Phaedrus that speech has an assumed original connection 
with thought and for this reason is considered to be more real 
and true than writing, which is thereby derivative and secondary. 
Writing, Plato has Socrates say, "speaks as if it has intelligence," 
but knows nothing (Phdr. 275D-E). Against this way of think­
ing, Derrida and others, namely those who follow his deconstruc­
tion of logocentrism, argue that the sign cannot be reduced to 
what it is supposed to represent (what is commonly called "the 
referent" or "the signified"). Since signs refer to other signs, their 
meaning is not determined by some kind of correspondence to 
a Platonic reality or to an independent referent. It is a matter of 
difference, in which meaning is always already in deferral, aka in 
differance (Derrida 1982). 
In line with the insights of structural linguistics, it can be said 

64 Communicative AI 
that signs are always embedded within a system or structure, 
so that meaning is derived from relationships and differences 
between words and other signifiers. These structures of language 
already shape our perception of reality and our understanding of 
the world. Derrida, for his part, further developed this structural­
ist view of meaning, but objected that meaning is not as stable as 
structuralism had initially claimed it to be. Moreover, he argued, 
against Aristotle, that speech is not more real, natural, or original 
than writing and that the latter derives from it (Derrida 1976). 
This, again, decenters the linguistic subject: language is not just 
about communicating what is in your head -it is not just about 
what you say; language itself speaks, too (Coeckelbergh 2017). 
Thus, who or what does the talking -the speaker or the author -
is not very important and determinative of what comes to be said 
(see also Foucault in the next chapter). 
This philosophical approach is also in line with the Sapir­
Whorf hypothesis in linguistics, which proposes that the structure 
of language influences the speaker's cognition and perception of 
the world. In short, language influences thought without neces­
sarily determining it (Edward Sapir, in particular, rejected strong 
linguistic determinism). Benjamin Lee Wharf was led to this 
view in his investigation of the Hopi and Uto-Aztecan languages, 
where he demonstrated that the structures of different languages 
shape how their subjects perceive and conceptualize the world. 
While the scientific quality of this ethnographic work has been 
subsequently questioned, the ideas in it have had a significant 
influence on contemporary efforts in cognitive science. George 
Lakoff and Mark Johnson (1980), for instance, have argued that 
metaphors in a particular language are linked to how speakers of 
that language think, because metaphors structure our most basic 
perceptions and actions. 
LLMs and Language 
In order to describe what LLMs are, do, and represent in rela­
tion to language and meaning, we can mobilize the following two 
frameworks and problematize the tensions between them. 
On the one hand, an LLM-say, in the form of a chatbot like 
the ChatGPT web app -can be seen as a tool that uses language 
in order to communicate and to say things about the world. But, 

Language, Meaning, and Communication 65 
one could argue, this is not real communication and is not really 
about representation, since the chatbot does not have a mind of its 
own that contains intended meanings, nor does it have embodied 
access to the real world of things, which could be talked about 
and referenced. When it outputs the word "tree," for instance, 
it does not know what that word means. Likewise, multimodal 
systems such as GPT-4o can generate images (another kind of 
sign) of a tree without knowing or recognizing what a tree is -or 
is not, for that matter. Despite this, the chatbot is able to mimic 
or simulate communication and representation. 
When we ask ChatGPT what a tree is, it will give an answer 
that makes sense (to us). We therefore act as if it were a linguis­
tic subject. But this, one could argue, is deceptive, or at least an 
illusion. Only humans use and understand language in this way. 
Chatbots are just "stochastic parrots," as Bender et al. (2021) 
have called this technology; in other words they just mimic lan­
guage use, but are not really using language, because they are not 
full linguistic subjects. They lack a mind of their own; they do not 
have thoughts; and, consequently, they cannot express anything 
meaningful or significant. They are, we could say, parasitic on 
the meanings that are already there in the world; these mean­
ings have been communicated and represented through human 
language and became fossilized or fixed in texts -on which the 
LLM was trained. 
LLMs thus do not possess real intelligence and speech, but are 
derivative and parasitic on the real -that is, on the reality of the 
world -and on original human speech and writing. What Plato 
said about writing versus speech can also be said of LLMs versus 
human writing: LLMs speak as if they had intelligence, but what 
they have is not true intelligence; it's merely the appearance of 
something that looks like intelligence. It's a kind of parroting 
of human speech, or "mimicry" (Weil 2023). Accordingly, the 
parrot is to be rejected as a fake. It may imitate human speech, 
but it does not speak. Homo sapiens -the species that Greek 
philosophers characterized as "animal endowed with speech" -
is the one and only original linguistic subject. There shall be no 
idols. 
On the other hand, if we take a poststructuralist and 
Heideggerian or later Wittgensteinian view, it would seem that 
the fact that LLMs lack mind is less problematic. Their relation 
to language and meaning need not be one of central control 

66 Communicative AI 
and original intentions. They may be parasitic on the system of 
human language and on its relations with our lifeworld, but so 
are human language users when they rely on scripts and mean­
ings that are already there (albeit arguably they do it in different 
ways, since LLMs operate differently from the human organism). 
Moreover, meaning comes not only from the relation between 
signs and the (life)world but also from the structural relations 
within the system of language. Even if LLMs do not understand 
meaning, they make use of those structural relationships and 
manipulate them. As Coeckelbergh and Gunkel (2023) have 
argued, the production of meaning is always a matter of co­
authorship (if authorship at all), in which neither the humans 
nor the language are in exclusive control of the process. And this 
is also true of communicative AI. LLMs do not determine mean­
ing; rather meaning emerges from a process of meaning-making 
in which there is no original logos and, one could add, in which 
there is no need for a prior mental experience on the part of the 
technology, either. 
Signs therefore refer to other signs and texts refer to other 
texts, just as meaning is the outcome of reading and interpret­
ing rather than being already there beforehand. This is to say 
that meaning is the outcome of a process shaped by the technol­
ogy that uses existing texts. In this process humans interpret and 
construct significance afterwards, so that meaning can be neither 
authored nor authorized (we will pick up on this idea in the next 
chapter). Thus the meaning of what the LLM produces cannot 
be reduced to what an author meant to say or sought to express. 
After the "death of the author" (Barthes 1978), we have some­
thing like co-authored or even unauthorized writings. Saying this 
does not absolve LLMs and the companies that market them of 
the kind of ethical challenges and responsibilities identified in the 
previous chapters. But it does mean that these problems should 
not be parsed and understood in terms of a simple application 
of the reality-appearance binary, which is typically deployed in 
efforts to address them. 

Language, Meaning, and Communication 67 
Communication: 
From Transmission to a Culture of Remix 
If language is no longer -or at least not exclusively - a means 
of expression, then the act of communication can no longer 
be understood solely as the transmission of mental content 
that originates in the head of the sender and is thus sent to a 
receiver. It, too, would depend on other ways of understanding 
and characterizing what is called "communication." In fact, as 
James Carey (1989) argues, if you look up the word "commu­
nication" in a dictionary, you will find two competing, but not 
necessarily exclusive, definitions of the term. One definition 
what Carey calls "the transmission view of communication" -
focuses on the process of message exchange. The other -Carey 
calls it "the ritual view of communication" -capitalizes on the 
etymology (rooted in the Latin word communis) that is shared 
by our words "communication," "community," and "common" 
and concerns not message transfer but the social behaviors that 
reproduce and maintain a common understanding and sense of 
reality. 
The Transmission View of Communication 
The transmission view -which was initially formalized in the 
middle of the twentieth century by Claude Shannon and Warren 
Weaver (1949, 7-8) -perceives communication as a dyadic pro­
cess of transporting a message from a sender to a receiver by way 
of a medium (Figure 4.2). In typical applications of the transmis­
sion view, especially in the field of communication studies, the 
sender and the receiver are human subjects, while the medium 
is a technological instrument. Or, as Andrea Guzman (2018, 8) 
explains, "humans are communicators (senders and receivers) 
and technology is the medium, or channel, through which people 
exchange messages." The principal objective of this particular 
model of communication is to ensure that the original message is 
transferred to the receiver in the best possible way, with a min­
imum of distortion or disturbance. Consequently, in the trans­
mission view of communication, the desideratum is to carry out 
the transference of messages through a noiseless or near noiseless 
medium. If and when this is achieved, the message that originates 

68 Communicative AI 
Message Message 
Noise Source 
Figure 4.2 Shannon and Weaver's transmission model of 
communication. 
Adapted by David Gunkel from Shannon and Weaver 1949. 
in the mind of the sender can be accurately reproduced in the 
mind of the receiver. 
This situation should be very familiar to scholars in classical 
humanities, who try to figure out for instance what an ancient 
philosopher really meant or what was really intended in a par­
ticular verse from the Bible or some other religious scripture. 
The aim is to uncover the original by reducing, or even eliminat­
ing, the distortion introduced by the medium of transmission. 
Those who are engaged in such projects want to know the mind 
of the original author or, in the case of religious scriptures, to 
have direct access to the word of God. The aim of the hermeneu­
tic tradition is to unveil and gain access to the original message. 
What matters, then, is the integrity of the message communicated 
directly from the mind or soul of the original speaker. 
Ritual View of Communication 
What Carey (1989) calls the ritual view provides for an entirely 
different way of conceptualizing and making sense of commu­
nicative interaction. Gunkel (2001, 76) explains: "Within the 
ritual paradigm, communication is comprehended as an inten­
tionally redundant activity or infinitely repeatable practice that 
does not necessarily seek to provide new insight or convey infor­
mation but endeavors to establish and maintain the common 
tenets that compose and define a specific social organization and/ 
or tradition." Here, then, we are less obsessed with the task of 
reproducing the ideas that originated in the mind of the sender. 

Language, Meaning, and Communication 69 
What matters is the social rituals -those redundant and repet­
itive symbolic performances -that shape and characterize the 
shared reality that defines a community. 
In this case we are not concerned with the faithful transmission 
and accurate reception of the original intentions of the sender. 
What matters more is the various mixings and seemingly repeti­
tive remixings of existing content that construct and reconstruct 
the common experiences that define a particular community 
(Gunkel 2016). And in this process the technological medium 
is central. In the famous words of Marshall McLuhan (1995), 
"the medium is the message." Here distortion and alteration are 
part of the process and contribute to the difference that commu­
nication makes. It no longer matters whether the "origin" -now 
called "source material," "sample," or "data" -has been gener­
ated by a human being, a machine, or some combination of the 
two. Communication is not a matter of transferring an original 
message; it is about the shared ritual practices and repetitive per­
formances of mixing and remixing. 
Does this mean, as Nietzsche (1980, 199) once wrote in one of 
his notebooks, that we have simply overturned Platonism and now 
reside in a world of appearances? Yes and no. After the decon­
struction of the Platonic real-apparent binary, we find ourselves 
in the philosophical environment of Jean Baudrillard-the world 
of simulacra. "The territory," as Baudrillard (1994, 2) writes, 
"no longer precedes the map, nor survives it. Henceforth it is the 
map that precedes the territory -precession of simulacra -it is 
the map that engenders the territory." But even if, as Baudrillard 
stresses, simulation should not be interpreted as a kind of false 
representation, his intervention still seems to be incomplete, as it 
arguably remains an inverted Platonism. That is, it still operates 
according to the standard binary opposition that is the defining 
feature of Platonism (see also Smith 2006 about Deleuze), since 
it remains within the reality-appearance binary. Even the terms 
"simulation" and "simulacrum" seem to be too Platonic, since 
what has been simulated still hovers in the background, the ref­
erent being something like a ghost. 
A true deconstruction of Platonism would need to go beyond 
mere revolutionary inversion. The terms and conditions of this 
more radical form of intervention are something that is perhaps 
most evident in Nietzsche's parable "How the 'True World' 
Finally Became a Fable" in his Twilight of the Idols. This short 

70 Communicative AI 
text, which proceeds in several discrete steps, ends with the fol­
lowing remarkable statement: "The true world -we have abol­
ished. What world has remained? The apparent one perhaps? But 
no! With the true world we have also abolished the apparent 
one" (Nietzsche 1983, 485). Here Nietzsche moves beyond the 
mere reversal of Platonism, undermining and destabilizing the 
very distinction between the real and its apparitional other. What 
Nietzsche identifies, therefore, is not a simple inversion of the 
existing metaphysical order, but a deconstruction (see Gunkel 
2021) of its very terms and conditions. This introduces an entirely 
different epistemological and axiological order. Instead of obsess­
ing over original intentions, he gives importance to derivation, 
simulation, repetition, and transformative (re)use. Thus the key 
communicative act is not to represent the origin faithfully; it is to 
copy, transform, and combine in innovative and creative ways. 
The task is not to communicate content in a vertical or top-down 
transmission, through some extraordinary power, divine or sec­
ular; it is to work from the bottom up, joining in community 
through common communicative activities that are horizontally 
distributed. 
LLMs and Communication 
This, then, leads us to two fundamentally different ways of look­
ing at LLMs as communicative subjects. According to the trans­
mission view, the problem with LLMs is that they steal original 
material created by humans and do not transfer correctly the real 
(the facts) to the apparent (the output or the generated content). 
According to the ritual view, the communicative problem with 
LLMs is not that there is simulation or "the hallucination of 
truth" (Baudrillard 1994, 8), but that LLMs may not recombine 
and remix in a way that is creative and that generates something 
of value and significance out of the available source material. 
According to the epistemology and axiology organized by the 
transmission view of communication, LLMs are little more than 
thieves, liars, and deceivers (simulants). According to the episte­
mology and axiology determined by the ritual view, things look 
entirely different, as mixtures, impurities, derivations, and so on 
are not just acceptable, they are potentially valuable. So let them 
steal. Let them hallucinate. We have to evaluate the output and 
see whether it adds something of significance; that is, we have 

Language, Meaning, and Communication 71 
to decide whether we can do something with it regardless of its 
origin. As in both Dewey and Rorty, the epistemic and axiological 
criteria are not representational but pragmatic. The meaning and 
value of the output does not (just) depend on the intentions of the 
sender of the original message (if there is one); it emerges in the 
process of performing and needs to be evaluated independently 
of its representational value and link to a supposed original truth. 
What matters is the destination, not the origin. 
Finally, these two different views of communication raise 
important questions concerning power. According to the trans­
mission view, the question to ask is who is, or has (im)posed them­
selves as, the originator, or as having the privilege of representing 
and mediating the origin. Think of the priest and the sacred texts 
that are linked to divine origin, or the king's bloodline that goes 
back to an origin in some mythical past. Such exclusive claims to 
the original were ( and often still are) used to exert power over 
others. Communication technologies such as books are supposed 
to establish a link to the origin and to support its power. Does 
the book mirror the world (as it should) and accurately represent 
the truth? Is the book truly original? Does it speak for the real 
and the true? 
With regard to communicative AI, the question regarding 
power and authority concerns who ( or what) the original author, 
artist, writer, and so on is. What matters, then, is the integrity 
of the original communicator and their message or intention to 
say something (more on this in the next chapter). In this view, it 
is crucial to be able to trace the output of an LLM to its origin. 
This can be done, for instance, with a digital watermark or some 
other guarantee. The epistemological question is always directed 
at deciding whether and to what extent the output of the LLM 
accurately reproduces or represents the truth. Any so-called hal­
lucination is unwelcome, since hallucinated output is a misrep­
resentation or distortion. Communication is assumed to be about 
accurately mirroring reality. Thus the problem is that the LLM is, 
technically, a broken or distorted mirror (see Valor 20246, 13). 
According to the ritual view, the intentions of the sender 
are immaterial, and the question to ask is, what is the quality 
of the content, the generated output (regardless of the origin), 
and who or what is the best or most expedient remixer of content? 
Who or what is able to generate the most useful or interesting 
mixture of different source materials? To what other texts and 

72 Communicative AI 
contexts does a particular text refer? How potent is one formula­
tion by comparison with others? And, also, who or what has the 
best or most expedient technological means? 
Since the role of technology or the medium is not to mirror 
or transmit an original message, but to enable one to add to 
what has been generated, technology is not just a neutral tool. It 
becomes central to the picture. This can be seen in popular cul­
ture, where the remix artist or DJ is often pictured together with 
their equipment. This is not coincidental: the two are dependent 
on each other and combine in a kind of post-human or hybrid 
subjectivity. In these cases, both the human and the machine con­
tribute to the mix, the interpretation, or the communication that 
binds people together, and they do so without staking a claim to 
a mythic origin. This is the creation of a common sense of com­
monality that does not need to defer or to refer to an original 
origin. What is important, then, is not who said what, but how 
others come to respond to what has been said. What matters 
is the shared, common experience. And in this way power and 
responsibility come to be decentralized, democratized, and some­
times even disseminated ... for better or worse. 
For LLMs, this means that power is related to the one who 
prompts -an act comparable to the curatorial art of the DJ -but 
also to the technology and those who own it. Those who have the 
power and the privilege to develop and deploy this technology 
influence what can be operationalized; they do so through the 
ways they design, train, and constrain these technologies. Here 
the problem is not that LLMs hallucinate or misrepresent the 
original truth, but rather that some powerful people and organ­
izations have privileged influence over the operations and out­
comes of LLMs. Asking about power in this context is not about 
complaining how the original message is distorted by the tech­
nology, but rather pointing out how the output has a particular 
form, meaning, and set of consequences as a result of already 
existing asymmetries of power. 
Thinking and Talking about LLMs 
One of the criticisms directed at LLMs is that, even if these tech­
nologies generate seemingly intelligible statements, they do not 
and cannot understand what they say. And this is because these 

Language, Meaning, and Communication 73 
technologies use linguistic signs without having access to their 
supposed referents -those real things that words are said to sig­
nify. If this criticism sounds reasonable and even self-evident, it 
is because it proceeds from, and mobilizes, theories of language 
and communication that have the weight of history behind them, 
going back at least as far as Aristotle. 
But referential realism and the transmission view of communi­
cation are not the only way to proceed-and not even necessarily 
the best. Recent (and by that we mean nineteenth-and twentieth­
century) innovations in structural linguistics and poststructural­
ist semiology offer alternative routes into language and meaning. 
And their focus on language as a system of differences -in which 
a word comes to have meaning not by reference to a real world 
signified but by virtue of differences from other words within 
the language -is more compatible with how LLMs work with 
and use language. Likewise, the ritual view provides an alterna­
tive way of theorizing communication. Here the focus is not on 
an individual subject who has something they intend to transmit 
to others, but on the shared social experience of a reality that 
belongs to and is defining of a particular linguistic community 
-one that includes not just human beings but all kinds of com­
municative and interactive subjects. 
In the face of these competing theories, the task is not to take 
sides or pick winners and losers, but to recognize how the way 
we understand language, meaning, and communication already 
determines and frames different sets of problems, modes of 
inquiry, and even the conditions and terms of the debate. Acom­
plete philosophical critique of LLMs, then, cannot be satisfied 
with simply pointing out faults and failings with the technology. 
It also requires that we learn to identify how LLMs challenge 
existing ways of talking and making sense of things, and that we 
reflect on and question our own understandings and conceptu­
alizations of language, meaning, and communication. Thus we 
close this chapter by repeating what is now a kind of refrain: 
LLMs may well not think for themselves, but they are certainly 
things to think with. 

5 
Authorship and Authority 
In response to any written text -like the book you are reading 
right now -it is reasonable to ask who wrote it and can there­
fore take responsibility for what it says. This seemingly sensible 
inquiry is typically resolved by pointing to and identifying the 
author. And it is the identity of the author -who they are and 
where they come from -that often serves as a heuristic or short­
cut for determining the validity or truthfulness of what has been 
written. But when something is written or generated by an AI -as 
is the foreword to this book -who or what is the author? Is it 
the algorithm? Is it the human who prompted it? Or is it perhaps 
both? These are not only philosophical questions but also the 
elements of a very real practical conundrum, with important con­
sequences for attribution, responsibility, and validity. 
This chapter investigates the way in which communicative AI 
confronts and disrupts the concept of authorship and its author­
ity over the meaning-making of written content. To get there, 
we will proceed in three steps or movements. (1) We begin by 
asking and then answering what seems to be a rather simple and 
intuitive question: what is an author? (2) We then examine and 
explore how LLMs disrupt, disturb, and deconstruct what Michel 
Foucault (1984, 107) has called "the author function," providing 
us with an opportunity to think differently about the concept of 
authorship and its authority over writing. (3) We conclude by 
drawing the consequences of this intervention of LLMs and by 

Authorship and Authority 75 
figuring out how reactions to it yield very different methods of 
explaining, making sense of, and responding to the challenges of 
AI-generated content. 
What Is an Author? 
Asking the question "what is an author?" seems superfluous, 
maybe even pointless, as we all have a pretty good idea of what is 
meant by the term. An author is the person who writes a book or 
some other text, and who is therefore responsible for what that 
piece of writing says. But this conceptualization is not some kind 
of universal truth that has existed from the beginning of time. It 
has a history. "The author," as the French literary critic Roland 
Barthes (1978, 142-143) wrote, "is a modern figure, a product 
of our society in so far as, emerging from the Middle Ages with 
· English empiricism, French rationalism and the personal faith of 
the Reformation, it discovered the prestige of the individual, of, 
as it is more nobly put, the 'human person."' 
In Barthes's analysis, the author -as we now understand and 
use the term -is a literary figure that comes into existence during 
the modern period in Europe. It is therefore a correlate of inter­
connected intellectual and cultural developments, all of which 
cluster around what Foucault (1984, 101) calls a "privileged 
moment of individualization in the history of ideas." Among 
these are the indubitable cogito ergo sum ( "I think, therefore 
I am") of Cartesian rationalism; the immediate, individualized 
faith instituted by the Protestant Reformation; and the concept of 
personal property, as articulated in the work of Thomas Hobbes 
and John Locke and codified in English law. 
Before these modern and distinctly European innovations, 
Barthes contends, there were perhaps writers of texts but no 
"authors" as we currently understand the term. And, like many 
theorists of his time such as Marcel Mauss and Claude Levi­
Strauss, Barthes (1978, 142) employs the critical foil provided by 
twentieth-century anthropological discoveries: "In ethnographic 
societies the responsibility for a narrative is never assumed by a 
person but by a mediator, shaman or relator whose 'performance' 
-the mastery of the narrative code -may possibly be admired 
but never his 'genius."' Outside the experiences and traditions 
of European modernism, stories, accounts, and other kinds of 

76 Communicative AI 
content have been successfully developed, performed, and accu­
mulated without necessarily needing the figure of the author. 
These alternative configurations and their critical challenge to 
the modern European concept of the author are examined and 
developed by other literary critics and philosophers who follow 
and extend Barthes's lead, for example Trinh T. Minh-ha (1989) 
and Gayatri Chakravorty Spivak (1998). The challenge itself 
has also been identified in premodern literature. Chris Chesher 
(2023, 49) connects the dots when he points out "that Homeric 
stories were not the work of any individual author but collec­
tively held invocable knowledge of a community passed from 
person to person over a long time. In a new way, search results 
or AI-generated answers are collectively authored rather than the 
product of individuals." Providing a full account of the historical 
development of the concept of the author and detailing its cul­
tural significance and consequences would require an entire book 
in its own right. For our purposes it will be sufficient to note four 
characteristics. 
Paternalism 
First, the status and function of this modern figure of literary 
authority has typically been characterized in explicit paternalistic 
terms. "The Author/' Barthes (1978, 145) writes, 
is always conceived of as the past of his own book: book and author 
stand automatically on a single line divided into a before and an after. 
The Author is thought to nourish the book, which is to say that he 
exists before it, thinks, suffers, lives for it, is in the same relation of 
antecedence to his work as a father to his child. 
This paternal configuration is old, having its origins in the found­
ing texts of the western intellectual tradition. "The idea of a book 
as the author's child," Mark Rose (2002, 3) explains, "dates 
back at least to Plato." And it is evident in the Phaedrus, where 
the written word is characterized as a wayward child, or what 
Jacques Derrida (1981a, 84, 145) terms "the filial inscription" 
and "the miserable son." 
As Rose (2002, 3) demonstrates, this obviously gendered con­
figuration (insofar as it is about fathers and sons artd not mothers 
and daughters) expands during the Renaissance, "when pater-

Authorship and Authority 77 
nity quickly became the most common figure for expressing the 
relationship between an author and his works." And this formu­
lation continues to exert conceptual pressure on contemporary 
copyright law, which, especially through the stipulations pro­
vided by the Berne Convention, recognizes and seeks to protect 
the "paternal rights" of authors (Strauss 1955, 507) and defines 
the improper appropriation and use of the written content of 
others as "plagiarism" - a word whose etymology was touched 
upon in Chapter 2 (seep. 36) and means kidnapping. 
Meaning and Significance 
Second, it follows that these authority figures serve a very prac­
tical and useful function: they guarantee significance. "To give 
a text an Author," Barthes (1978, 147) writes, "is to impose a 
limit on that text, to furnish it with a final signified, to close 
the writing. Such a conception suits criticism very well, the latter 
then allotting itself the important task of discovering the Author 
beneath the work: when the Author has been found, the text is 
'explained."' The author, then, is the principal mechanism of 
stability and significance in the production and circulation of 
written documents and other cultural artifacts. The authoritative 
account of any work is properly situated not in the material of 
the writing but in the original thoughts, intentions, and virtu­
osity of the individual who created it. Likewise, the task of the 
reader is to penetrate the material surface of the writing in order 
to ascertain the authorial voice behind the text and to compre­
hend what the author originally intended or meant to say by way 
of the written work. 
This conceptualization of writing as a medium of expres­
sion or communication has a deep intellectual reach and a 
well-established historical foothold. It is not only informed by 
Aristotelian semiology -which characterized the written word as 
a derived symbol of mental experience (words express thoughts: 
Arist. Int. 16a3, see Aristotle 1938) -but also theorized in the 
transmission view of communication, which takes the technol­
ogy of writing as a more or less effective instrument for message 
transmission. According to this way of thinking, the best writ­
ings are those that speak clearly and directly, so that the reader 
can access, understand, and comprehend what the author had in 
mind. 

78 Communicative AI 
Lo gocentrism 
Third, this way of thinking about writing and reading is informed 
and supported by logocentric metaphysics. In the previous chap­
ters we already encountered the term "logocentrism." Coined in 
the opening decades of the twentieth century by the German phi­
losopher Ludwig Klages (Josephson-Storm 2017, 221), it identi­
fies the assumed primacy and importance of the spoken word as 
a direct sign of things, thus relegating writing to being a sign of 
speech or the sign of a sign. Derrida ( 197 6, 11) locates the origi­
nal formulation of this concept in Aristotle's De interpretatione: 
If, for Aristotle, for example, "spoken words (ta en tei phonei) are 
the symbols of mental experience (pathemata tes psuches) and writ­
ten words are the symbols of spoken words" (De interpretatione, 
1, 16a3), it is because the voice, producer of the first symbols, has 
a relationship of essential and immediate proximity with the mind. 
Producer of the first signifier, it is not just a simple signifier among 
others. It signifies "mental experiences" which themselves reflect or 
mirror things by natural resemblance. 
If we ask, "What is it that Derrida is trying to say here?," this 
very question -which represents a mode of inquiry that seeks 
to discover what an author is saying in and by the writing -is 
logocentrism par excellence. And, by asking this rather intuitive 
question, we can see how, before we even open our mouths to 
speak, logocentrism already is the usual way of thinking about 
writing and of writing about thinking. 
Logocentrism therefore seeds a method of reading and inter­
pretation to which Foucault (1984, 101) refers as "the-man-and­
his-work criticism." The modern literary canon -and in this 
context "literature" should be broadly understood as including 
works of fiction, non-fiction, scholarly writing, and scientific 
papers -is organized around particular individuals (most of them 
the proverbial dead white men) and their collected oeuvre. This 
concept is eventually formalized in the romantic figure of autho­
rial genius developed and theorized in Immanuel Kant's Critique 
of Judgment (Kant 1987, 174), where it is argued that "all fine art 
is the product of genius." Following this logic, a modern philoso­
pher like Descartes (1988, 22) conceived of the "reading of good 
books" as "having a conversation with the most distinguished 
men of past ages -indeed, a rehearsed conversation in which 

Authorship and Authority 79 
these authors reveal to us only the best of their thoughts." And 
our very citation of Descartes, Kant, Barthes, and other author­
itative figures in the western canon is predicated on this way of 
thinking. 
The Law of Copyright 
Finally, authorship is not just a heady philosophical concept. It 
is also -and perhaps principally - a matter of law. As Foucault 
(1984, 108) points out, the author was a figure of "penal appro­
priation." "Texts, books, and discourses really began to have 
authors ( other than mythical, 'sacralized' and 'sacralizing' fig­
ures) to the extent that authors became subject to punishment, 
that is, to the extent that discourses could be transgressive." In 
other words, texts are initially subsumed under the figure of an 
author in order for the authorities (governments or the church) to 
identify who is to be held responsible for a statement -literally, 
who is able to respond for it (Ricreur 2007, 12) -so that one 
may know who could be questioned, indicted, and punished for 
a published transgression. For instance, Galileo had been con­
demned and placed by church authorities under house arrest for 
the publication of a treatise supporting the Copernican model of 
the solar system; and this is why Descartes decided to withdraw 
what would have been his first book, Le Monde, and to publish 
The Discourse on Method anonymously -that is, without any 
indication of his role as its author. 
In England and its breakaway North American colonies, the 
author was framed as the responsible party in a new kind of 
property law, called copyright. The legal concept of copyright 
assigns ownership to a literary work by identifying the author as 
its legitimate owner and proprietor. This concept, as Rose (2002) 
explains, was first introduced in eighteenth-century London -not 
out of some idealistic dedication to the concept of artistic integ­
rity, but in response to a specific technological innovation, which 
permitted the free circulation and proliferation of textual docu­
ments: the printing press. As Sven Birkerts (1994, 159) explains, 
"the idea of individual authorship -that one person would create 
an original work and have historical title to it -did not really 
become entrenched in the public mind until print superseded 
orality as the basis of cultural communication." When texts pro­
liferate and it is possible to make money with printed material, 

80 Communicative AI 
it becomes important again to identify the author, or rather to 
be identified as the author. As a result of these legal necessities, 
the figure of the author eventually came to be recognized as the 
organizing principle and subject of contemporary copyright 
law. 
Large Language Models 
The fundamental challenge (or opportunity) with LLMs such as 
OpenAI's GPT series and its wildly successful ChatGPT web app 
is that these algorithms generate seemingly logical sequences of 
words without there being someone who is speaking and there­
fore able to guarantee or in some way authorize the meaning 
and the truth of what is said. As a result, LLMs disrupt, disturb, 
and deconstruct the standard way of thinking about and making 
sense of authorship, authority, and the means and meaning of 
writing. 
Questioning Authority 
Michel Foucault's essay "What Is an Author?" opens with a 
quotation from Samuel Beckett: '"What does it matter who is 
speaking,' someone said, 'what does it matter who is speaking?"' 
(Foucault 1984, 101). Answers to this arguably rhetorical ques­
tion have typically been provided via what Foucault (1984, 107) 
calls "the author function" - a concept that, as we have just 
seen, is not some natural type or immutable Platonic form but a 
specific literary, legal, and historical affordance. Consequently, 
if the author -as the principal figure of literary authority and 
accountability -comes into existence in a particular place and 
at a specific moment in time, there is also a point at which it 
would conceivably cease to fulfill this role. Or, as Foucault (1984, 
119) explains, "given the historical modifications that are taking 
place, it does not seem necessary that the author function remain 
constant in form, complexity, and even in existence. I think that, 
as our society changes, at the very moment when it is in the pro­
cess of changing, the author function will disappear." 
It is this disappearance -this withdrawal of what had been 
the principal figure of literary authority -that is announced and 
marked by Barthes's seemingly apocalyptic title, "Death of the 

Authorship and Authority 81 
Author" (Barthes 1978). What this phrase indicates is not the 
end of life of any particular individual or the end of human writ­
ing, but the termination of the figure of the author as authoriz­
ing agent and guarantee of what is said in or through writing. 
And LLMs are not unique in this regard; we can see versions 
of this process materializing in other digital information and 
communication technologies, for instance Wikipedia, where the 
authorship of an article is disseminated across a network of con­
tributors without there being a clear indication of authorial voice 
or attribution (Wikipedia 2024). 
Although Barthes and Foucault obviously could not have 
addressed the twenty-first-century technology of LLMs and gen­
erative AI, their critical work on authorship accurately antici­
pates the current situation of communicative AI and authorship. 
To put it as directly as possible, LLMs actualize the death of the 
author, implementing what Barthes and Foucault had theorized. 
In the logocentric terminology already mobilized by Plato in the 
Phaedrus, what we have with LLMs is writings produced in the 
absence of any living and breathing voice to animate and author­
ize what is being said. Therefore such writings are literally unau­
thorized; or a kind of "authority without an author" that, as 
Bernard Stiegler (2008, 31) observes, "inheres in all writing." But, 
instead of fueling criticism of what these AI-generated texts lack, 
their unauthorized status shows us to what extent the authority 
for writing -any writing, be it by humans or by machines -has 
always already been a socially constructed artifice. 
Truth and Consequences 
Once the written text is cut loose from the controlling interests 
and intentions of an author, the question of significance gets 
turned around. Specifically, the meaning of a piece of writing is 
not something that can be guaranteed a priori by the authentic 
ethos of the one who is assumed to speak through the medium of 
the text (Figure 5.1). 
Instead, meaning transpires in and from the process of reading 
and interpreting. And if it is the case that this significance was 
customarily attributed to an author, that attribution is (and has 
always only been) projected backwards, from the reader onto 
a supposed and often absent author. Meaning-making, in other 
words, is an effect of reading that is then "retroactively (presup) 

82 Communicative AI 
Figure 5.1 Meaning-making situated in the intentions of the author. 
Created by David Gunkel. 
Figure 5.2 Meaning-making situated in the act of reading. 
Created by David Gunkel. 
posited" (Zizek 2008a, 209) to become its own presumed cause 
(Figure 5 .2). 
This flipping of the script on literary theory changes the loca­
tion of meaning-making from the "original" intentions of the 
author-writer, who has "something to say," to the interpretive 
activity of the readers, who make or generate meaning from 
their engagement with the materiality of the written content. As 
Barthes (1978, 148) explains, "text is made of multiple writings, 
drawn from many cultures and entering into mutual relations of 
dialogue, parody, contestation, but there is one place where this 
multiplicity is focused and that place is the reader ... A text's 
unity lies not in its origin but in its destination." Thus the mean­
ing of a text -whether it is written by a human author, generated 
by an LLM, or assembled from the productive interaction and 
collaboration of both -is situated ( or happens) in the interpret-

Authorship and Authority 83 
ing and meaning-making that is produced in and through read­
ing. Destination, not origin, matters for meaning. Logocentrism 
has had things backwards and upside down. It is the reader, and 
not the author, who is the locus of meaning-making in writing. 
This also explains how AI-generated content comes to have 
meaning. The critics are correct when they point out, for instance, 
that "ChatGPT lacks the ability to truly understand the complex­
ity of human language and conversation. It is simply trained to 
generate words based on a given input, but it does not have the 
ability to truly comprehend the meaning behind those words" 
(Bogost 2022). But it would be impetuous for us to conclude 
from this insight that what the LLM generates is nonsense, mean­
ingless content, or bullshit (Hicks, Humphries, and Slater 2024). 
These writings are meaningful, and what they mean is something 
that happens in the process of our reading, interpretation, and 
evaluation of the generated content. This is not something spe­
cific to LLMs but, as Barthes argues, it is a defining characteristic 
of all writing. LLMs just happen to make it legible. 
Words and Things 
Finally, what matters is not just where meaning is located and 
produced. What is at issue is, more fundamentally, the concept of 
meaning itself. From Plato on, language has been assumed to con­
sist of signs that refer and defer to things; and this idea persists in 
the current critique of LLM technology. When we write the words 
"large language model," for instance, we think that those linguis­
tic signs stand for and refer to some real thing out there in the 
world, such as the ChatGPT application developed by OpenAI. 
"For the signification 'sign,"' Derrida (1978, 281) explains in an 
essay titled "Structure, Sign, and Play," "has always been under­
stood and determined, in its meaning, as a sign-of, a signifier 
referring to a signified, a signifier different from its signified." 
Words have meaning because someone like an author, someone 
who, we assume, is an embodied human person with access to 
the real world outside language, uses words to refer to things and 
to say something about them. And the big problem with LLMs is 
that they lack this ability. They manipulate words without know­
ing ( or caring) what those words refer to. 
But, as we have seen in the previous chapter, this seemingly 
commonsense view of how language works is not necessarily the 

84 Communicative AI 
natural order of things. And it has been directly challenged by 
twentieth-century innovations in structural linguistics, which sees 
language and meaning-making as a matter of difference situated 
within language itself. As we stated in Chapter 4 (pp. 61-62), 
signs do not acquire meaning by referring directly to things that 
exist outside their own system; signs refer to and differ from other 
signs. This is the meaning (or one of the meanings) of a notori­
ous statement, which is often associated with Derrida: II n�y a 
pas de hors-texte ("there is nothing outside the text" or "there 
is no outside-the-text"). And this is especially true for LLMs, as 
there is, quite literally, nothing outside the text that they have 
been trained on and that they generate from the input of a user 
prompt. Consequently, what has been offered as a criticism of 
LLM technology -that these algorithms only circulate signs but 
have no access to the real-world embodied referents -might not 
be the indictment that critics think it is. LLMs are structuralist 
machines that deconstruct the defining conceptual oppositions of 
classical semiotics. 
Opportunities and Challenges 
LLMs and other forms of generative AI are powerful technolo­
gies, and it is necessary to be critical of both the promise and the 
peril they present. Unfortunately, many of the available responses 
from linguists, philosophers, and AI experts seek to normalize 
and reassert modernist concepts of authorship and authority that 
were already disrupted by twentieth-century innovations and 
developments in literary theory. Roland Barthes may have the­
orized the death of the author, but LLMs make it real. And, as a 
result, we now find ourselves confronted with a number of very 
real opportunities and challenges. 
Authority after the Death of the Author 
The question of who or what is responsible for AI-generated con­
tent remains open and seemingly irresolvable. This is a matter 
not only of attribution but also of responsibility, that is, a matter 
of deciding who or what can be credited or blamed for the tex­
tual content that has been produced. Responses to this crisis in 
authority proceed either by trying to reassert the author function, 

Authorship and Authority 85 
so that it scales to the challenges of communicative AI, or by 
bringing in a kind of resignation that recognizes -as Nietzsche 
(1974, 279) had anticipated in the wake of the death of that 
other figure of authority, the Christian God -that all bets are 
off. 
Efforts at the former response pull in two different directions, 
both of which seek -albeit by different means -to preserve the 
author function in the face of these disruptions. On the one hand, 
there are those who endeavor to protect the original integrity 
and authority of the author by restricting who can be named 
as such and by explicitly excluding AI from ever being consid­
ered one. This has recently been codified in both publication cri­
teria and law. In August 2023, the journal Nature "laid down 
ground rules about using LLMs ethically," stipulating the fol­
lowing: "No LLM tool will be accepted as a credited author on a 
research paper. That is because any attribution of authorship car­
ries with it accountability for the work, and AI tools cannot take 
such responsibility" (Nature Editorial 2013 ). Similarly, several 
court decisions made in the same year in the United States and 
the United Kingdom denied authorship and intellectual property 
(IP) protections to anything but natural human persons (Knibbs 
2023; Thaler v. Comptroller-General 2023; Chatterjee 2023 ). 
On the other hand, there are artists, authors, and content crea­
tors who are actively engaged in collaborating with the algorithm 
as a kind of co-creator. In these cases, which can be exempli­
fied by the literary work of Mark Amerika (2022) or the music 
of Holly Herndon (Friedlander 2019), we see an effort to open 
up and extend the author function so that it also applies to and 
comes to respect the original contributions made by the LLM. 
Those who make such efforts assign the machine some degree of 
agency and authority. This is a direct challenge to existing expec­
tations about who or what can be an author and to the usual, 
instrumentalist way of making sense of the role and function of 
the technological artifact. And it hasn't sat well with those who 
are still beholden to standard metaphysical traditions and ways 
of thinking (Evans, Robbins, and Bryson 2024). 
Alternatively, we could decide to finally give up the ghost of 
the dead author (to put it lightly and colloquially). But doing 
so will require a complete reconfiguration of accepted models of 
content creation and creativity. Once the figure and controlling 
influence of the author is withdrawn or sufficiently destablized, a 

86 Communicative AI 
text, whether written by a human or generated by a machine, can 
no longer be restricted to being understood as an expression of 
someone's inner thoughts, experiences, and desires. It therefore 
may no longer matter who is speaking, as texts come to be assem­
bled and function in other ways. "The text," as Barthes (1978, 
146) explains, "is a tissue of quotations drawn from the innu­
merable centers of culture ... the writer can only imitate a ges­
ture that is always anterior, never original. Their only power is to 
mix writings, to counter the ones with the others, in such a way 
as never to rest on any one of them." Understood in this fash­
ion, what Barthes calls the scripteur -whether that be a human 
individual, a machine, or a hybrid of human and machine -is a 
literary remixer or a text DJ, appropriating and recombining tex­
tual samples that are drawn from an already available database 
of source material. 
Responsibility, Accountability, and Liability 
Authorship -or, better stated, the author function -is, as Foucault 
pointed out, primarily about resolving questions of moral and 
legal responsibility. Thus the death of the author also results in a 
crisis of accountability, and the consequences of this are already 
evident and becoming increasingly available. Because LLMs have 
been trained on textual data scaped from the internet and other 
digital repositories, there are important questions concerning 
copyright, intellectual property, and plagiarism. Indicative of this 
is the lawsuit brought by the New York Times against OpenAI 
and Microsoft in December of 2023. The complaint, which was 
filed in the Federal District Court of Manhattan, contends that 
OpenAI and Microsoft used millions of original articles published 
by The Times in order to train its ChatGPT LLM, without first 
obtaining permission or paying the appropriate licensing fees to 
reuse this copyrighted content (The New York Times Company 
v. Microsoft Corporation). In response to this charge, OpenAI 
(2024) has argued that "training AI models using publicly avail­
able internet materials is fair use, as supported by longstanding 
and widely accepted precedents. We view this principle as fair 
to creators, necessary for innovators, and critical for US com­
petitiveness." In support of its position, OpenAI cites official 
statements made by academics, library associations, US compa­
nies, content creators, authors, and others who responded to the 

Authorship and Authority 87 
US Copyright Office's Notice of Inquiry on AI and Copyright in 
August 2023. 
This legal dispute is as much about the technology of commu­
nicative AI as it is about existing copyright restrictions and what 
these laws are designed to protect. If this sounds vaguely familiar, 
so it should. A similar debate occurred with sampling and the 
remixing of recorded content in hip-hop, electronic music, and 
other collage content creation practices. And Stephen Marche 
(2023) effectively connects the dots for us in an article for the 
Atlantic that bears the relevant title "The Future of Writing Is a 
Lot Like Hip-Hop." What is at stake in all these debates -be they 
about reusing recorded material in remix or training LLMs on 
text data -is the delicate act of balancing adequate protections of 
the original work against transformative, follow-on uses of that 
work that are necessary for subsequent innovation. And the two 
sides in the current debate on LLMs and other forms of genera­
tive AI are already lining up along similar lines: protection of the 
integrity of the original work and of the rights of human authors 
versus transformative reuse of existing content in the name of 
cultural progress. 
But all things are not equal. As we move from the extractive 
techniques of sampling and remixing to the generative practices 
of LLM AI, there is a significant shift in power. The human DJ 
or remix artist has typically been mythologized as a revolution­
ary figure -an outlaw pushing back against the dominant cul­
ture industry with their indie DIY inventiveness (Gunkel 2016) 
-thus somewhat mimicking ( or continuing) the cult of the artis­
tic genius as underdog, but also leaving room for decentralized 
power. Generative AI systems, by contrast, are a corporate prod­
uct from the very beginning. They have been developed by, are 
the property of, and remain entirely beholden to highly profita­
ble multinational corporations. Thus the romantic image of the 
crate-digging DJ who recovers deep cuts from almost forgotten 
prerecorded content ( again, the ghost of the authorial genius is 
not that far away) has now been replaced by the indiscriminate 
scaping of internet content by Big Tech firms. Even if the dis­
putes and the arguments look substantially similar, the stakes 
and the stakeholders are very different. These debates are about 
authorship and authority as much as they are about power and 
money. 

88 Communicative AI 
Conclusions and Outcomes 
LLMs and other forms of generative AI are a significant chal­
lenge, because with these technologies we now have things that 
write without speaking, a proliferation of texts that do not have 
and are not beholden to the authoritative voice of an author, and 
written content whose truth cannot be anchored in any prior 
intention to say something. From one perspective - a perspective 
that remains bound to the usual way of thinking -this can only 
appear as a threat and a mark of crisis. What is on the line and 
even in the crosshairs is our very understanding of language, the 
state of literature, and the meaning of truth ( or the means of 
speaking it). 
But from the perspective of critical interventions in twentieth­
century literary theory that we discussed, LLMs and generative 
AI do not threaten the figure of the author, the means of making 
meaning, or the concept of truth. They only threaten a limited 
concept -one that is not some universally valid and naturally 
occurring phenomenon but the product of a particular culture 
and philosophical tradition. LLMs and generative AI reveal the 
terminal limits of the author function, contribute to decentering 
its organizing principles, and open the opportunity to think and 
write differently, which is precisely where we are headed with the 
final two chapters. 

Hallucinations 
LLMs generate word sequences that sound good but are not nec­
essarily true. They seem to regularly "make up" things or "hal­
lucinate." Consequently they are not, it seems, very reliable in 
terms of truth. But what is truth? And how should we conceptu­
alize what LLMs give us when they make things up? Moreover, 
misinformation is not only a problem of knowledge but also a 
very real political concern. Is our democracy in danger? 
This chapter first investigates the nuanced interplay between 
factual accuracy, misinformation, and the phenomenon known 
as hallucinations in the context of communicative Al. The term 
"hallucination" (which we already encountered in previous chap­
ters) identifies instances where AI models generate convincing but 
entirely fabricated information. This has implications for various 
stakeholders, including users who rely on these technologies for 
factual data, developers who aim to improve their accuracy, and 
policymakers who grapple with the ethical and political conse­
quences of AI-generated content. But the chapter digs deeper: we 
also introduce and critically engage with big philosophical issues 
such as the concept of truth and the limits of the correspondence 
theory, communication ethics and matters of responsibility, and 
the opportunities and challenges created by communicative AI 
for public information and democratic governance. We therefore 
question the term "hallucination," not so much because it uncrit­
ically applies to machines a human characteristic but because it 

90 Communicative AI 
presupposes adopting a particular and, arguably, problematic 
theory of truth. Moreover, we show how misinformation not 
only creates problems of voter manipulation but threatens to 
undermine the epistemic foundations of democratic governance. 
In dealing with these subjects, the present chapter will provide 
an overview of some of the main knowledge-related challenges 
and opportunities of LLMs. By addressing the critical issues of 
reliability and potential for misinformation, the chapter contrib­
utes to the broader conversation about power and the responsible 
development and deployment of AI technologies, emphasizing 
(but also questioning) the importance of transparency, account­
ability, stakeholder responsibility, and other ethical and political 
considerations in the evolution, deployment, and use of LLMs 
and related forms of generative AL 
Factual Inaccuracy, Misinformation, and 
Hallucinations 
LLMs can produce all kinds of factually inaccurate or erroneous 
content. In 2024, for instance, a version of Google's Gemini LLM 
optimized for search advised a user to use glue to stick the cheese 
to their pizza and informed another that geologists recommend 
eating one small stone per day (Shrivastava 2024). These exam­
ples may seem humorous, but, if someone acted on such advice, 
that would no longer be a laughing matter. In order to get a better 
handle on these problems, we can distinguish between various 
kinds or types of erroneous output. 
Misinformation 
Misinformation is the intentional spreading of inaccurate infor­
mation for the purpose of manipulating other people's behavior 
-for instance in democratic elections or in business transactions. 
While misinformation, fake news, and unfounded rumors are a 
rather common feature of all forms of human communication, 
communicative AI can be leveraged to generate misinformation 
on an unprecedented scale. It can be used not only to generate texts 
containing misleading information but to do so in a convincing, 
serious, calm, and informative style, making the deception more 
difficult to detect (Chen and Shu 2024). But factual inaccuracy 

Truth, Lies, and Hallucinations 91 
does not need to be intentional; some erroneous output could 
derive from incorrect, incomplete, or poorly cleaned information 
contained in the training data. In this case, the LLMs -like a sto­
chastic parrot can unwittingly repeat, reproduce, or otherwise 
propagate that content. 
LLMs also tend to be notoriously bad at math and logical rea­
soning. This is because an LLM does not know what numbers 
mean. For the LLM, numbers are just another linguistic token, 
which can be assembled in probabilistic sequences with other 
tokens. Thus, an LLM is just as likely to generate "1 + 1 = 405" 
as it is to come up with "1 + 1 = 2." Both statements are valid 
mathematical expressions; but only the second one is correct. 
Both the intended and the non-intended cases ( and these words, 
"intended" and "non-intended," refer not to the LLM but to the 
decisions of the human user who devised the prompt that is fed 
into the LLM) are problematic, since the output reaches a user 
who may not be aware of the truth or falsity of the generated 
output. Unlike other kinds of information and communication 
media, LLMs have no built-in mechanisms to fact-check the con­
tent they generate; there is no human editor or fact checker who 
is in the loop, and the models have no way of verifying the infor­
mation contained in the training data. 
This is problematic not only because of specific factual errors; 
it is a problem also when users act on the wrong information, 
or when collective decisions are made on the basis of the gener­
ated content. As we will see later in this chapter, misinformation 
is both socially and politically relevant. LLMs can be used to 
manipulate voter behavior, and democracy can be in serious trou­
ble in the presence of a knowledge environment that is no longer 
reliable or reliably stable. 
Hallucinations 
Another widely recognized and cited problem is hallucinations. 
The term "hallucination" has a storied history in the field of 
AI and artificial neural networks (ANNs) in particular. In the 
early 2000s it was commonly used to describe beneficial fea­
tures of computer vision systems, but by the mid-2010s it began 
to acquire negative connotations, being increasingly applied to 
factually inaccurate output (Maleki, Padmanabhan, and Dutta 
2024). LLMs hallucinate in the sense that the model can invent 

92 Communicative AI 
or fabricate content that is not simply inaccurate but does not 
seem to make any sense at all, or is entirely detached from reality. 
The system may contradict itself, produce nonsense, and offer 
output that is not related to the input prompts (and to the user's 
expectations for the output) and therefore appears to be irrele­
vant or .fictional. 
The term "hallucination" has been criticized on the grounds 
that it misleadingly "personifies" LLMs, making it look as if they 
had a mind of their own. Osama Fayyad put it as follows in an 
interview: "When you say hallucinations, you're attributing too 
much to the model ... You're attributing intent; you're attribut­
ing consciousness; you're attributing a default mode of operating 
rationally; and you're attributing some form of understanding 
on the part of the machine" (Tanner 2023). LLMs lack all these 
properties. Like the term "artificial intelligence" itself, "hallu­
cination" is criticized for being anthropomorphic and therefore 
highly problematic. 
Nevertheless, the phenomenon is real and presents a problem 
not only for users, who cannot rely on the generated content, but 
also for developers, companies, and policymakers. For many, the 
technology does not seem to be good enough (yet?). For example, 
in 2023 OpenAI's GPT-4 had been praised for having a low hal­
lucination rate, but that rate was still 3 percent (Wodecki 2023). 
This may not seem to be much, but if users trust the validity of 
the generated content and act on it, or if, on the contrary, they 
decide not to use the system because it is perceived to be too 
unreliable, not only the users of these systems have a problem 
but also the companies that develop them. Does this mean that 
we are heading to a new AI winter? How can and how should 
policymakers respond to this issue? Should they prevent rollout 
of Ais until they are good enough? And how can they protect 
vulnerable users who may believe or be ready to accept what the 
model produces? 
Hallucination has been identified as a problematic term 
because it projects human characteristics onto machines and pre­
sents us with some very real challenges for eth�cs, commerce, law, 
and policy. But there's more to it. In identifying these problems, 
it is assumed that we know perfectly well what truth is, and that 
we agree on what truth is in this case. Do we? What is truth, 
anyway? Is there some universal form of truth to which we can 
simply refer without further discussion and to which we have 

Truth, Lies, and Hallucinations 93 
direct access? When fact-checking, we often use Google or other 
search engines. But this does not really help answer the deeper 
problem, since we can ask the same questions about the sources 
these engines rely on. Why is Google or Bing any better than 
LLMs? What is truth and how can we know it? 
What Is Truth? Plato's Realism, the 
Correspondence Theory of Truth, and 
Its Criticism 
At least since Plato, philosophers have concerned themselves with 
the concept of truth and the accuracy and reliability of human 
knowledge; and rightly so. But, again, what is truth and how can 
we know it? 
Platonic Realism 
In his dialogues Protagoras and Gorgias, Plato famously portrays 
Socrates arguing against the sophists -for simplicity, the ancient 
Greek equivalent of our social media influencers -who taught that 
truth is relative and subjective and depends on perspective and 
circumstances. According to Plato's Socrates, there are objective 
truths, independent of individual opinions and perceptions. The 
sophists, he claims, are not committed to truth but deal in decep­
tion and manipulation, appealing to our lowest instincts. Their 
sophisticated rhetoric aims to influence others without offering 
true knowledge. In the Gorgias, rhetoric is presented as a means 
of persuasion devoted to achieving power ( Grg. 466b ); and it 
is dismissed as a branch of flattery (466a). True philosophy, by 
contrast, seeks to uncover genuine knowledge and wisdom and is 
committed to truth, unlike rhetoric and the other arts. Similarly, 
LLMs and those who employ them are being accused of decep­
tion and manipulation, of not being concerned with truth. They 
are seen as mere rhetorical devices, instruments that do not bring 
us closer to true knowledge. 
Moreover, Plato thought that fictions and workings of the 
imagination are as dangerous for the body politic as rhetoric. 
In the Republic, he argues that the stories of Homer and Hesiod 
corrupt the minds of the young by portraying morally reprehen­
sible behavior. This may sound familiar, as it resonates with an 

94 Communicative AI 
argument that has been recently offered against video games, 
social media, and indeed generative Als that create fiction. And 
Plato's solution was simple: censorship (R. 3776). The education 
of the Guardians -the leaders and decision makers of the ideal 
polity -should aim to instill virtue in them (378e). The prob­
lem, then, with poetry and the other imitative arts is that they 
do not care for what is real; they just produce cheap imitations 
(392d). Like television, movies, video games, and fictional con­
tent produced by generative AI, these fictional appearances are 
not just entertaining pastimes; they can actually distract us from 
true reality. For Plato, the only solution is to exile these deceptive 
image makers. In contemporary jargon, they must be "canceled." 
The Correspondence Theory and Its Discontents 
Jump to twentieth-century philosophy, where the dominant view 
of truth is that captured by the correspondence theory of truth: 
truth consists in the agreement of knowledge to its object, which 
means that, as Russell and Moore argued, truth relates to real­
ity. This view goes hand in hand with a realist metaphysics. For 
the early Wittgenstein, for example, the world is a totality of 
atomic facts (Wittgenstein 1995), and therefore every truth can 
be explained in terms of correspondence to the relevant fact. 
Sometimes other terms are used: accordance, representation, 
states of affairs, properties (David 2015). For most of us, the 
correspondence theory of truth seems so obvious as to make one 
wonder why it is even necessary to further discuss it; Descartes, 
Kant, and many other modern philosophers thought the same. 
Heidegger (1994, 15-16) once explained: "the determination of 
truth as correctness, together with its counterpart, namely incor­
rectness (falsity), is in fact clear as day. Because this conception 
of truth emerges, as is obvious, entirely from the natural way 
of thinking, and corresponds to it, it has lasted throughout the 
centuries and has long ago been hardened into something taken 
for granted." 
Against the correspondence theory of truth ( and indeed against 
Plato), it has been argued that we do not have independent access 
to reality. This access is always mediated and shaped by our cog­
nition (Kant 1998) -and, as we have seen in Chapter 4, by lan­
guage. Thus my access to reality depends on the structures of my 
language, which have their own internal relations of meaning. Or, 

Truth, Lies, and Hallucinations 95 
as Wittgenstein (1995) wrote, "the limits of my language mean 
the limits of my world" (Tractatus, 5 .6). Moreover, pragmatist 
theories, for example in Dewey's (2011) version of pragmatism, 
view truth not as an abstract relationship between a proposition 
and how things really are, but as the outcome of processes of 
inquiry and trial and error. Dewey argued against the Platonic 
(and ultimately also Kantian) form of abstraction, rejecting the 
view that there is an otherworldly sphere where objective truth 
is hosted. 
Later on Richard Rorty (1979), too, rejected the claim that 
truth is somehow "out there"; according to him, truth does not 
exist independently of the human mind and human language. 
The world may be out there, but it is our descriptions of the 
world that can be true or false. We therefore should not forget 
speakers and what they use to speak: language. Words already 
mediate and shape what is the truth for us. Nietzsche had already 
rejected the traditional ways in which we tend to speak about 
truth and had emphasized differences in perspective and power. 
The question is not only what is said (and if that is true) but also 
who said it and for what purpose. As Nietzsche (2020) argued in 
an essay of 1896 titled "About Truth and Lie in the Extra-Moral 
Sense," humans also create truth about the world, and there is no 
truth in itself, no objective truth. In other words, rhetoric returns 
to philosophy. In fact it may have been there all along. 
Consequently, what Plato got wrong when he advocated 
expelling the poets from Kallipolis, the ideal city -and what 
Russell and the early Wittgenstein got wrong when they treated 
language in terms of propositions and defined truth as a relation 
of correspondence to what is the case -is that propositions and 
descriptions about the world are not the only existing "speech 
acts," and saying something about the world or about what is 
the case (Wittgenstein 1995) is not the only existing "language 
game" (Wittgenstein 2009). As Austin (1962) argued in How to 
Do Things with Words and Searle ( 1996) further elaborated after 
him, language is also used to command, to provoke an emotional 
reaction, to promise, to apologize, and even to change a state of 
affairs in the world, by declaration. The meaning of these speech 
acts can vary, depending on the social and cultural context. 
In a sense they can have their own truth, or rather they make 
something true or they make something the case, at least socially 
speaking. 

96 Communicative AI 
For example, when we promise something and don't deliver, 
others can hold us to account and might treat us as a kind of liar. 
This is not because what we say does not correspond to a state 
of affairs in the world, but because we fail to do what we prom­
ised; that is, because what we said earlier does not fit with what 
we do later. And when we establish social facts in the way Searle 
explains it, namely by using declarative language, we make some­
thing the case. We thus create a new (social) truth. Declarative 
language during a marriage ritual, for example, makes it the case 
that two people are married. Here truth is not about external 
correspondence but is social-relational; it comes about through 
social language use. 
Beyond declarations, there are other kinds of language games, 
and telling fictional stories is one of them. Such stories, as 
both Aristotle and Paul Ricreur argued, have their own inter­
nal coherence, meaning, and -one could add -truth. In Time 
and Narrative, Ricreur (1984) argued that narrative meaning 
and coherence are created though the structuring of events in a 
plot and are not limited to being a reflection of external reality. 
Consequently, there is something like truth, meaning, and justice 
within a narrative without there being external referents, with­
out a (direct) correspondence to an external, real world. If, for 
example, I say something incorrect about a story element in the 
Harry Potter series, a dedicated reader of this series may right­
fully correct me. That person would have better knowledge of the 
meaning and truth within the Harry Potter universe. At the same 
time, this knowledge and truth might not hold for the world out­
side those stories. 
Truth under Siege? Revisiting Hallucination, 
Bullshitting, and Misinformation by LLMs 
If an LLM generates output that claims for example that the 45th 
president of the United States of America was Hillary Clinton -
which is in fact something that ChatGPT generated (see Marcus 
and Davis 2023) -this statement is patently false and incorrect. It 
does not correspond to a fact or actual state of affairs in the (his­
tory of the) world. It is, in other words, not true. It is understand­
able why people often say that the algorithm can lie and deceive 
us, although the LLM cannot "intend" this or anything else. And 

Truth, Lies, and Hallucinations 97 
when seen from this perspective, the metaphor of hallucination 
seems both appropriate and well devised. While LLMs have little 
or nothing to do with human thought processes, the term "hal­
lucinate" seems to make sense because it indicates that we -the 
users of these technologies -find ourselves confronted with con­
tent that is not in touch with the world of facts but comes from 
a world of fabricated appearances: the magic world of shamans 
perhaps, the illusionary world of drug users, or the fake world of 
dreams. Consequently LLMs cannot be trusted to remain faithful 
to the real world. What they produce is illusions. It is as if LLMs 
were on LSD. 
Bullshit and Bullshitters 
One approach that is clearly in line with Platonic realism and 
the correspondence theory of truth can be found in a recent crit­
ical essay by Michal Townsen Hicks, James Humphries, and 
Joe Slater (2024 ). Drawing on Harry Frankfurt's (2005) On 
Bullshit, the authors argue that LLMs can be said to be bullshit­
ters not just because they produce nonsense or make factual mis­
takes but because they are not "concerned with truth" (a Platonic 
objection) and because "they are designed to produce text that 
looks truth-apt without any actual concern for truth" (Hicks, 
Humphries, and Slater 2024, 1 ). In other words, the claim is that 
LLMs are limited to the realm of imitation and appearance. They 
are deceptive, concerned with rhetoric, and care neither for truth 
nor for knowledge (ibid., 3 ): 
The problem here isn't that large language models hallucinate, lie, or 
misrepresent the world in some way. It's that they are not designed 
to represent the world at all; instead, they are designed to convey 
convincing lines of text ... These models aren't designed to transmit 
information, so we shouldn't be too surprised when their assertions 
turn out to be false. 
Yet, since there is no intention to deceive, the authors 
appropriately argue that it would be wrong to see this feature 
in terms of lies. Lying involves making a false statement with the 
intention to deceive. "Bullshit," then, at least within this way 
of thinking, seems to be a better term. And it is for this reason, 
as the authors conclude, that ChatGPT is "a bullshit machine" 
(ibid., 7). 

98 Communicative AI 
To make matters worse, one could argue that it is highly prob­
lematic that these technologies say things -or generate statements 
-that are experienced as offensive or that are indeed morally 
objectionable. LLMs not only cannot be trusted to represent the 
world accurately; if left to their own devices, they lie and seem 
to be unethical in other ways. For example, by parroting racist 
views found in texts on the internet, communicative AI applica­
tions continue to reproduce and reinforce biases against already 
disadvantaged groups. This further enrages the "Platonists" 
among us, and even many of us who have never heard of Plato 
but find such conduct socially and morally reprehensible. The 
polis, it seems, is clearly in danger, since LLMs not only bullshit 
but do so in a way that produces content that can be harmful, 
unethical, and even dangerous. These artificial sophists are a cor­
rupting influence and a clear and present danger. 
The result of all these lies, errors, misrepresentations, and hate 
speech is that developers of communicative AI and the companies 
that employ them have often turned to the same remedy Plato 
recommended: censorship. Current LLM technologies such as 
ANTRHOP\C's Claude operate with a set of rules- a constitution 
-that serve to evaluate and filter out generative content that is 
deemed unacceptable. These rules do exactly what Plato always 
wanted: they create prescribed behaviors for politically correct 
or acceptable speech. Doing so will, so the Platonic argument 
goes, protect us and our communities from untruth and unethical 
content. And, if that does not work, the next step is to put a stop 
to it all, either by putting a momentary pause on LLM develop­
ment (Future of Life Institute 2023) or by banning these bullshit 
machines altogether. 
Another Way to Look at It 
The Platonic approach to truth is undeniably persuasive. Who 
in their right mind could ever be against the true and the good? 
And aren't bullshitting and lying the very things that we, not only 
philosophers but also thoughtful democratic citizens, should be 
against? Yet it is worth exploring what happens when we employ 
a different theoretical framework and philosophical approach. 
Hicks and co-authors are on to something when they say that 
the problem is not misrepresentation; that there is not even an 
aim to represent the world. Using vocabulary from the later 

Truth, Lies, and Hallucinations 99 
Wittgenstein (2009), one could reformulate the bullshit objection 
in a way that moves it further away from the correspondence 
theory of truth than bullshit theorists may intend: the problem 
with LLMs such as OpenAI's ChatGPT is not so much that they 
do not aim to represent the world, but rather that they mislead­
ingly present their output as belonging to the language game of 
representing the world, whereas in reality they are playing another 
game, other games, or, perhaps more accurately, no game at all: 
they merely imitate playing a particular language game. 
Within the framework of this formulation, the problem is 
one of imitation: not imitation of facts in the world (appear­
ance versus reality), but imitation of a particular language game. 
When the problem is viewed from this non-Platonic alternative 
perspective, it is difficult to distinguish the appearance of play­
ing a language game from actual playing. The problem, then, is 
that LLMs can successfully play (or appear to play) the language 
game of generating propositions. They do so in a manner that 
even looks serious and confident, thus imitating the style of this 
game's players. But they do it without the need for any link, con­
nection, or access to the real world. There is only in-game truth, 
at best -and no question of correspondence. 
Arguably this "deception" could be minimized if developers 
and the corporations that employ them did not present their 
products as suitable for search or for other language games, 
which are supposed to involve correspondence with, or the rep­
resentation of, the real world. Users, too, could learn and be 
aware of the fact that much of what is produced by these technol­
ogies is likely to be fiction. And philosophers and other critically 
minded individuals who condemn LLMs for violating the truth 
could recognize that LLMs also play, or at least seem to play, 
language games other than that of description, proposition, and 
so on. Surely they would accept that there is nothing wrong with 
writing fiction per se, as long as the results are not presented as 
belonging to the language game of speaking the truth, as that has 
been conceived of by correspondence theorists (and as assumed 
and operationalized by the bullshit theorists). 
Ironically, that LLMs play (or, again, appear to play) all kinds 
of language games and can produce truth within such games is 
perhaps best illustrated by the fact ( ! ) that some users circumvent 
the Platonic-style censorship control mechanisms of Big Tech 
companies by asking the LLM to generate a fictional account. In 

100 Communicative AI 
such efforts, many things become possible that are not true (in 
the correspondence theory sense of the word) and that may be 
unethical or morally questionable. In this way (again, ironically), 
users of such models try to get closer to having the LLM speak 
the truth through the detour of fiction. 
Considering these challenges for both sides -developers and 
users -also reminds us of something important: communica­
tive Ais do not stand on their own but are always connected to 
humans and their actions. LLMs may not themselves have any 
intentions, and as far as we know they don't. But humans cer­
tainly do. And it is humans who design and use these technologi­
cal systems, and who can also manipulate, even jailbreak them to 
produce harmful content or to achieve subversive political objec­
tives. Here it is both the LLM companies and their users that can 
exercise agency, although some clearly have more agency than 
others. 
This obviously leads to questions about power that, ever since 
Nietzsche and Foucault (and, later, Austin, Searle, and Butler), 
have been asked by many students of language and communi­
cation and people concerned with these subjects. Who has the 
power to do things with words -through their own speaking as 
well as through word sequences generated by LLMs? Who frames 
the kind of speech acts that are supposed to speak for, or channel, 
objective truth? Who has the power and privilege to impose their 
"truth" on others? Who is disadvantaged by and who benefits 
from deception and bullshit? How much are we at the hands of 
not only powerful political-economic structures such as those of 
capitalism but also the structure of languages themselves? 
As LLMs have so clearly shown by reproducing existing bias, 
languages are not neutral. They habor gender and racial bias, 
for example (Caliskan, Bryson, and Narayanan 2017). For this 
reason, LLMs are more than an object of critical reflection: they 
also help with descriptive ethics, as they reveal something about 
the social world and invite us to raise questions regarding nor­
mative ethics and politics. To what extent should speech be reg­
ulated in a liberal-democratic society? How should we deal with 
the systemic biases that are already embedded in a particular lan­
guage such as English? 
Finally, this critical examination of communicative AI reveals 
that truth is relational. Truth is always situated in a particular 
linguistic and social environment and emerges from within differ-

Truth, Lies, and Hallucinations 101 
ent texts, contexts, and stories. Some of the things that an LLM 
might come up with could well make sense within a particular 
textual ecology, even if it lacks correspondence to the "real" 
world. This is to say that LLMs demonstrate the truth of some of 
the (post)structuralist innovations. First, language and texts have 
their own system of meaning and truth-making, depending on 
internal relations. Second, when we discuss truth, we also need 
to ask who speaks and makes the rules for speaking. Truth and 
meaning are not just a matter of representation but also a matter 
of performance. Thus truth is made in a particular context (lit­
erally and figuratively) and through particular performances. As 
Slavoj Zizek (20086, 3) explains, referencing the innovations of 
Jacques Lacan, 
It is, of course, never possible to (be sure that we have) attain(ed) the 
truth -one can only endlessly approach it, because language is ulti­
mately self-referential, there is no way to draw a definitive line of sep­
aration between sophism, sophistic exercises, and Truth itself (this is 
Plato's problem). Lacan's wager is here the Pascalean one: the. wager 
of Truth. But how? Not by running after "objective" truth, but by 
holding onto the truth about the position from which one speaks. 
This more relational, performative, and post-representationalist 
theory of truth does not imply that misinformation is absolved of 
having ethical and political consequences, or that we should let 
LLMs run wild and hallucinate without restraint. Whatever the 
relation between output, LLMs, and what is framed as truth or 
reality might be, these phenomena and their related truth perfor­
mances have ethical and political consequences. Hallucinations 
can kill, if wrong decisions are made on the basis of them. And 
sometimes misinformation is produced on purpose, with the 
intention to manipulate. This is politically relevant, and espe­
cially important for democratic governance. But it cannot be 
responsibly dispelled or dismissed simply by reasserting the cor­
respondence theory or by calling bullshit on LLMs. 

102 Communicative AI 
Democracy and Responsible Development 
of LLMs 
Why exactly are misinformation and hallucinations politically 
relevant? Here we can again learn from both Plato and Aristotle. 
The Politics of LLMs: Democracy in Danger? 
In Book 6 of the Republic, at 488b-489c, Plato's Socrates argues 
that steering the ship of the state requires expertise. In its con­
text, the analogy in this passage is often construed as an argu­
ment against democracy. But, if we want to foster, maintain, 
and improve democracy, it is nevertheless good to inquire about 
the relation between knowledge and politics. Plato was right to 
imply that, if it were to work properly, democracy would require 
some kind of epistemic foundation. Without knowledge, both 
the citizens and those who represent them cannot engage in suc­
cessful ( self-)rule. This is generally recognized in the republican 
tradition of political philosophy, from Aristotle to the present - a 
tradition that places great store by educating citizens in order to 
enable them to participate in the important decisions of their city 
or state. 
In contemporary political theory, the need for knowledge 
is also recognized in what has been labeled "epistemic democ­
racy" (Cohen 1986; Estlund 2007; Landemore 2017). This label 
encompasses a range of views according to which democracy is 
not an aim in itself, as it is in the republican tradition (where 
democratic procedures are supposed to have intrinsic value); it 
is rather a way of making good decisions and keeping track of 
the truth. David Estlund, for example, has called for procedures 
with epistemic value that can generally be accepted as tending 
toward a good decision. We need to make good and efficacious 
epistemological arrangements. Or, more simply put, democracy 
needs truth. Citizens need to know the truth and the procedures 
of governance have to be sound in terms of knowledge. 
Moreover, as Hannah Arendt (2017, 474) has argued, if there 
is too much confusion about what is true and false, this only 
serves to help totalitarianism: "The ideal subject of totalitarian 
rule is not the convinced Nazi or the convinced Communist, but 
people for whom the distinction between fact and fiction (i.e., the 

Truth, Lies, and Hallucinations 103 
reality of experience) and the distinction between true and false 
(i.e., the standards of thought) no longer exist." This descrip­
tion of one of the conditions of totalitarianism also reminds us 
of what is called "post-truth politics" - a political condition in 
which there is public anxiety and confusion about facts. Such a 
condition is often stimulated by right-wing populist movements, 
which sometimes actively contribute to it. Post-truth politics has 
been partly successful, as recently evidenced by the global rise of 
populism in the early decades of the twenty-first century. 
Today the public is concerned about fake news, and conspir­
acy theories circulate widely. But the problem is not just specific 
lies, or the disdain for truth displayed by particular right-wing 
populist politicians such as Jair Bolsonaro or Donald Trump; it 
is the general undermining of democracy itself. Too much misin­
formation and bullshit are not just "local" normative-epistemic 
problems -problems that reveal a lack of interest in truth in a 
particular socio-political context. They are the sort of problems 
that corrupt the epistemic basis of a democratic republic. Self­
rule, according to philosophical republicanism, is only possible 
on the basis of knowledge and education. If these are missing, 
the door opens wide to populism, and ultimately to authoritar­
ianism and totalitarianism. Similarly and for the same reasons, 
these phenomena threaten epistemic democracy. Misinformation 
and bullshitting -whether produced by humans, by machines, or 
by both-is not only a problem related to voter manipulation but 
also one that undermines the epistemic foundations of democ­
racy (Coeckelbergh 2024). 
Remedies, Strategies, and Solutions 
For the responsible development of communicative AI, these 
threats to democracy mean at least that LLMs should be 
improved, modified, and regulated in such a way that phenom­
ena such as misinformation and hallucination are minimized and 
controlled as much as possible. Whether truth is conceptualized 
as correspondence or in some other way, the consequences of 
such phenomena are serious, not only at the personal level (as 
when someone makes a decision on the basis of LLM bullshit) 
but also at the political level -the level of our collective well­
being. Furthermore, LLMs should be developed in a way that 
is transparent about the language game that is being played ( or 

104 Communicative AI 
imitated), given that its results probably have more to do with 
the internal workings and relations of language than with any 
"corresponding" outside world. If people believe, or are led to 
believe, that an LLM is involved in describing facts about the 
world, then they will be able to see that LLM only as deceptive 
or lying, even though in reality an LLM does not and cannot 
"intend" either to represent or to misrepresent the world. 
Consequently the powerful multinational corporations that 
develop and deploy these technologies need to be held respon­
sible; and we should demand that they do everything in their 
power -through data curation, model fine-tuning, sandboxing, 
and the like -to minimize the generation of misinformation and 
hallucinations, but also to communicate clearly about the sys­
temic limitations of their products and services. Likewise we, 
the users of these technologies, have to take responsibility for 
what we prompt and how we do it. We need to be aware of 
and knowledgeable about the various kinds of language games 
that are being operationalized and played. Instead of instituting 
blanket censorship or banning communicative AI altogether -the 
solution proposed by Plato at the end of the Republic -we need 
to attend to the various uses of these technologies and treat truth­
and meaning-making ( understood as performances rather than 
representations) as a shared responsibility between developers 
and users. 
Second, even if these Big Tech companies proclaim that they 
want to do things in an ethical manner, that they are dedicated 
to improving the accuracy of their LLMs, and that they have 
made an effort to mitigate erroneous output, there is a prob­
lem with the lack of accountability and democratic legitimacy. 
Responsible development of LLMs means that these innovation 
efforts need to be injected with sufficient democratic legitimacy 
rather than being passed on to powerful multinational corpo­
rations and largely left in the "invisible hand" of the market. 
And, in turn, democratic decision-making needs to be itself 
infused with technological expertise of a high level. Whether one 
endorses a republican or an epistemic version of democracy, the 
current, thin conception that focuses on voting and representa­
tion will not, by itself, be sufficient to protect democracy and its 
knowledge basis. We need to find new combinations and mutu­
ally supportive entanglements of technical expertise and democ­
racy. These can enhance the democratic opportunities of LLM 

Truth, Lies, and Hallucinations 105 
development and at the same time ensure that the governance of 
communicative AI proceeds on the basis of a capable understand­
ing and informed knowledge about these technical systems. 
Finally, success on all these fronts depends on open communi­
cation and unrestricted access to education. Communicative AI 
does not exist or operate in a vacuum; it is part of a wider digital 
informational ecology. If we want good LLMs in an epistemo­
logical and perhaps also ethical and political sense, then, indi­
vidually and together, we need to take better care of the quality 
of that epistemic-communicative foundation. And, here too, the 
question of power is important -not only because it asks who 
or what can be blamed for problems but also because it inquires 
about who or what should take responsibility for improvements, 
and how these can and should be achieved. 
And here all the actors and stakeholders -citizens, civil soci­
ety, governments, Big Tech -have a role to play. Of course, there 
are well-documented problems with the concentration of power 
in the hands of just a few multinational corporations, and efforts 
to arrange for better distributions and democratic participation 
are urgently needed. Likewise, national governments and poli­
cymakers have an obligation to actively seek ways of shaping 
the epistemic and communicative systems that can support our 
shared values and encourage wider participation in decision­
making. But if the goal is to ensure truthful communication -
truthful both in terms of transmitting accurate information and 
in terms of cultivating a common ground of shared understanding 
-then creating and sustaining this opportunity is the responsibil­
ity of all stakeholders, including each one of us, the citizens. The 
question about truth and LLMs is not only a question about the 
technology itself; it is also a question about our speech acts, our 
language games, and indeed our use of these technologies. 

7 
Does Writing Have a Future? 
This final chapter appropriates and redeploys a question that the 
Czech-born Brazilian media theorist Vilem Flusser once used for 
a book he published in 1987. At the time Flusser was writing 
-and it should be noted, if only in passing, that the future of 
writing is itself a question that Flusser addressed both in and by 
writing -the dominance of the written word was in crisis, as new 
modes of digital expression seemed to herald the end of writing 
and the beginning of a post-literate age. "Writing in the sense 
of placing letters and other marks one after the other appears 
to have little or no future. Information is now more effectively 
transmitted by codes other than those of written signs" (Flusser 
2011, 3). 
We reuse and rewrite Flusser's question more than thirty-five 
years later, because it again looks as if the future of writing is 
on the line -this time as a result of impressive developments 
in LLM and similar communicative AI technology. In the face 
of these twenty-first-century innovations, we find ourselves once 
again asking rather dramatic and seemingly apocalyptic ques­
tions about writing and its future. The chapter not only rede­
ploys Flusser's titular question but develops a response. And 
we can, following Flusser's example, begin with a very direct 
statement: what LLMs such as OpenAI's GPT series of algo­
rithm, ANTHROP\C's Claude, and Google's LaMDA, Bard, and 
Gemini signify is not the end of writing but the terminal limits of 

Does Writing Have a Future? 107 
a particular conceptualization of writing, which has been called 
logocentrism. 
This means that writing indeed has a future, but only if we 
reconceptualize how we think about writing and how we write 
about thinking. Toward this end, the present chapter will (1) 
review three fundamental elements of logocentric metaphysics 
and the long shadow that this way of thinking has cast over the 
conceptualization and critique of LLMs; (2) trace the contours of 
a deconstruction of this standard operating procedure -contours 
that escape the conceptual grasp of logocentrism and its hegem­
ony; and (3) formulate the terms and conditions of an alternative 
way to think and write about both LLMs and the future of writ­
mg. 
Logocentrism and Its Legacy 
More and more people now use ChatGPT and other LLMs for 
writing. But is writing what LLMs do? In order to answer this 
question, we need to know what writing is. A common way of 
defining it is to say, following the online Britannica Dictionary, 
that writing is the "use of written words to express your ideas 
or opinions" (https://www.britannica.com/dictionary/writing). 
According to this definition, it would seem that LLMs cannot 
write, since they are not using words to express ideas; they 
simply arrange verbal tokens in statistically probable sequences. 
Although they use words, they have nothing to express in and 
through those words. Or, as the "Stochastic Parrots" essay puts 
it, "[t]ext generated by an LM [language model] is not grounded 
in communicative intent, any model of the world, or any model 
of the reader's state of mind. It can't have been, because the train­
ing data never included sharing thoughts with a listener, nor does 
the machine have the ability to do that" (Bender et al. 2021, 
616). 
If this explanation sounds reasonable and correct, there's 
a good reason for that. It is grounded in and supported by a 
common way of thinking that has been labeled "logocentrism." 
As we have seen in previous chapters, logocentrism identifies a 
way of thinking about writing and of writing about thinking 
that privileges the spoken word as the most authentic, truthful, 
and immediate mode of communication, thereby making writing 

108 Communicative AI 
a derived and artificial image -the sign of a sign. This way of 
thinking and talking about writing pervades western thought and 
can be documented as far back as Plato, if not before. 
Take for example the Phaedrus, a dialogue that begins with 
Phaedrus carefully concealing a book under his cloak (Pl. Phdr., 
228d). This is, for better or worse, the point of origin for one of 
the oldest philosophical jokes told in graduate seminars. (Hey, 
Phaedrus! Is that a book I see hidden beneath your cloak? Or are 
you just happy to see me?) The book in question is the transcript 
of a speech recently delivered by the well-known orator Lysias, 
and Socrates, who was not able to attend the "live" performance 
(a concept that the Phaedrus can be credited with introducing 
and developing), is anxious not only to hear an account of what 
transpired during the original delivery but also to get access to the 
actual discourse, as recorded in writing and reproduced through 
the act of reading. 
At the beginning of the Phaedrus, then, writing is situated as 
a means of recording speech and reproducing it at a future time, 
in a place different from that of its original delivery. It is, in other 
words, conceptualized as a way of capturing and storing spoken 
discourse, so that it may be made present again. This particular 
conceptualization is eventually theorized at the dialogue's end, 
where Socrates and Phaedrus explicitly take up and investigate 
the art-techne (1:txvri) -of writing. The examination begins with 
Socrates famously recounting a legend he has heard concerning 
two Egyptian gods, Theuth the inventor of writing and Thamus 
the king, and concludes with an indictment of the written word 
that, as documented by Derrida and others (Spivak 1998, Stiegler 
2008, Minh-ha 1989), has been constitutive of the western tradi­
tion. For now, we only need to recall three important highlights: 
Writing Is a Technology 
In the account provided in the Phaedrus, writing is presented as 
a techne. This word, which in many contexts is translated "art," 
means more generally "a system or method of making or doing" 
(Liddell-Scott Jones, A Greek-English Lexicon, s.v., sense 3: 
https://www.perseus.tufts.edu/hopper/morph?1=texnh&la=greek 
#lexicon). And this is the etymological root of our word "tech­
nology." Technically speaking, writing is a technology. Unlike 
speech, which is considered to be a natural ea pability inherent in 

Does Writing Have a Future? 109 
the human species, writing is artificial, external, and technical, 
as Walter Ong (1995, 81-82) makes it clear in a book fittingly 
called Orality and Literacy: "Writing (and especially alphabetic 
writing) is a technology, calling for the use of tools and other 
equipment ... By contrast with natural, oral speech, writing 
is completely artificial." And it is for this reason that Socrates 
perceives writing to be what we may describe as a kind of AI: 
"And so it is with written words; you might think they spoke 
as if they had intelligence, but if you question them, wishing to 
know about their sayings, they always say only one and the same 
thing" (Phdr., 275d-e). AI, one could say, is not some recent 
technological innovation that now threatens writing; writing is 
already a form of AI. 
Writing Is Secondary 
This seemingly natural order of things justifies an unequal hier­
archy and axiology that determines the status and significance 
of writing. Already in the Phaedrus, the live performance or the 
event, namely the speech that had been delivered by Lysias, is 
considered to be first, both in time and in status. Within the time­
frame of the text, the speech of Lysias occurs first; in fact, it has 
already transpired outside and before the beginning of the dia­
logue. The transcript of this speech, the book with which Phaedrus 
initially entices Socrates, is introduced and initially positioned as 
a copy of the original performance. It is therefore secondary and 
derived. It is a kind of surrogate and proxy that takes place by 
standing in for and taking the place of what has passed away 
and is no longer present. This is a mode of representation -what 
Aristotle later on will call the sign of a sign. Compared to the 
original spoken performance, then, the written record is always 
somewhat deficient and lacking. It is, as described in the Platonic 
text, a "mere image" of "the living breathing word" akin to what 
a painting is in comparison to the actual thing that it depicts 
(Phdr., 275d-276a). 
Writing Is a Bastard 
To put it in the rather blunt terms initially deployed in the 
Phaedrus, writing is a promiscuous bastard. As Socrates com­
plains, words, once they are written down and published, can 

110 Communicative AI 
be used and abused by anyone (Phdr., 275e). A text is aban­
doned in the world and is, for this reason, always beyond the 
control and protection of its original progenitor. Consequently 
all writings are, as Derrida (1981a, 76-77) says, "orphans" or 
"bastards" that are essentially cut off from paternal authority. 
This explains why Socrates and Phaedrus not only have access to 
the speech of Lysias beyond the latter's actual presence but can 
repurpose Lysias's words, as Socrates himself will do, mashing 
them up and remixing them in such a way as to make them say 
things that Lysias himself may not have intended or authorized. 
Once written, every word can, as Socrates observes, "be bandied 
about" (Phdr., 275e). We have already seen how this plays out 
with the concept of authorship, as it is the author -his name 
and his reputation -that is considered the authorizing authority 
for what has been written. And it should be pointed out that the 
gender-exclusive pronouns that are used here are part and parcel 
of this tradition, which is why Derrida often refers to logocentric 
meta physics as "phallogocentrism." 
Large Language Models 
The fundamental challenge -or the opportunity -with LLMs 
such as the OpenAI GPT series and the ChatGPT web app is that 
these algorithms write without speaking, that is, without access 
to (the) logos and without a living voice. They can produce leg­
ible sequences of words but express nothing, since they do not 
know what those words mean and do not understand what it is 
they are saying. In response to this seemingly monstrous prob­
lem, contemporary critiques -such as those offered by Bogost, 
Bender, and many others -proceed from and reassert the truth 
of logocentric metaphysics, with little or no critical hesitation. 
Consequently the problem is not that logocentrism has somehow 
failed to work in the face of these new technologies of writing. 
It's quite the opposite. The problem is that logocentrism works 
all too well, exerting its influence over our thinking about writ­
ing and our writing about thinking in ways that largely escape 
notice. What makes LLM tech so important and interesting is 
that it disrupts this way of thinking. And it is in this disruption 
that we can see both opportunities and challenges for the future 
of writing. 

Does Writing Have a Future? 111 
Technologizing the Technologizing of the Word 
If writing is, as Ong (1995) described it, "the technologizing 
of the word," then LLMs are the technologizing of writing. 
Thus the texts produced by LLMs are not direct expressions 
of thought but writings that have been derived from writing. 
According to the usual way of thinking, these writings are twice 
removed from the original, animating voice and intentions of a 
living speaker. If, as Aristotle formulates it, the spoken word is 
the direct sign of thought and the written word is the sign of this 
sign, then LLM-generated words are the sign of a sign of a sign. 
Thus the textual content that is written or generated by an LLM 
is the dim shadow of living speech that has died at least twice: 
once when the spoken word came to be preserved or mummified 
in writing; and, again, when these writings were used to train 
an LLM that in turn produces writing from writings. Instead of 
saying something that is meaningful, ChatGPT and other com­
municative AI applications give us little more than the derived 
representation of a representation of the truth. 
The usual way to respond to this problem is to reinforce the 
Platonic distinction between the real and the appearances derived 
from it, asserting the need for an ethics of honesty and trans­
parency. Developers of LLMs and related generative AI systems 
have the obligation to make it clear to users that the writings 
produced by these systems have been artificially generated by a 
machine (Natale 2021 and Mamak 2021). This can be done, for 
instance, by requiring a chatbot or a similar LLM system to self­
identify. Like a warning label, this kind of declaration is designed 
to inform users about what is really going on and to protect them 
from the risks of misidentification and deception. 
Something like this has already been put in place for ChatGPT. 
When one asks a question that proceeds from the mistaken 
assumption that the application operates like a human language 
user, the algorithm is designed to clarify that this is a mistake. 
The system can, for instance, explain that it cannot have an opin­
ion on things (Figure 7.1). This is a feature that has been delib­
erately designed into the operations of the algorithm because, it 
is argued, users deserve transparency and honesty. They need to 
know that, no matter how remarkable the output seems to be, 
the entity that is doing the talking is "just a machine," which 
ostensibly knows nothing. At first sight, this procedure appears 

112 Communicative AI 
What is your opinion about the 2024 US 
presidential race? 
@ I don't have personal opinions, but I can provide information! The 
2024 US presidential race is shaping up to be highly contested and is 
drawing attention both domestically and internationally. Key issues 
likely to be discussed include the economy, healthcare, climate 
change, and foreign policy. As candidates from various parties 
announce their campaigns and policies, voters are preparing to make 
informed choices based on their platforms and past performances. 
How closely have you been following the race? 
ChalGPT can make mistakes, Check irnporlant info. 
Figure 7.1 Generated output from ChatG PT, with 
warning statement. Created by David Gunkel. 
to be both ethical and sensible, and it seems so because this way 
of responding speaks for and is supported by the logocentric tra­
dition. 
An alternative -one that learns from and follows the example 
of recent innovations in feminist science and technology stud­
ies (STS) (Barad 2007, Haraway 1991 and 2016) -is to drop 
the Platonic dichotomy of appearance versus reality and see 
everything as one process in which realities and meanings (always 
in the plural) emerge and are co-produced and performed. In this 
case, neither humans nor technologies have exclusive and author­
itative control over things, but both participate in a process of 
shared meaning-making where no pre-existing metaphysical real­
ity and no dichotomy is presupposed. Instead, the real emerges 
from a collaborative interaction and performance that produces 
a particular and situated reality experience. 

Does Writing Have a Future? 113 
In this way, what was previously taken to be mere "phenome­
nal" appearance with some kind of "reality" hidden behind it is 
now seen as the essential part of a performance and process that 
is at the same time real and illusionary -or, better, can no longer 
be described in this binary fashion, as one or the other. In the case 
of an LLM such as ChatGPT, there is a meaning-making pro­
cess that has both computational and human elements (the user 
of the application, but also the developer and the manufacturer) 
participating together in the creation and emergence of differ­
ent forms of text and textuality. Rather than being dismissed as 
an "illusion," a "hallucination," or even "bullshit," the result­
ing output is simply text, more specifically text produced in and 
through a process and performance that contains both human 
and nonhuman elements. It is writing that results from a hybrid 
human-non-human intra-active performance (see also Beckers 
and Teubner 2021 and Holy-tuczaj and Blok 2019). 
To assign the name "writing" to a text that has been gener­
ated in this fashion is not a revolutionary proposal. Although it 
intervenes in the Platonic order of things, it neither institutes nor 
advocates a simple inversion of the real-apparent dichotomy. The 
point, then, is not that we should value appearances over reality, 
or that we should celebrate the proliferation of texts generated 
by machines without paying attention to what is really going on 
inside the black box of the algorithm or to the consequences that 
this LLM-generated content might have for people and commu­
nities. Instead of simply turning things around or flipping the 
Platonic script, the alternative approach we suggest here inter­
venes in logocentric metaphysics by releasing a deconstruction of 
the usual way of thinking. Understood in this fashion, LLMs are 
not the end of the story; they are a way to write a different kind 
of story about writing -what it is, who or what performs it, and 
what it all comes to mean. 
Deconstruction 
Deconstruction is a strategy by which one can engage with and 
respond to the binary oppositions of metaphysics. But what 
exactly does this mean and why is it important? In the opening 
lines of Beyond Good and Evil, Nietzsche (1989, 10) points out 
that "the fundamental faith of the metaphysicians is the belief 
in opposite values." These opposite values are formulated and 

114 Communicative AI 
expressed in terms of conceptual opposites or mutually exclusive 
predicates: real-illusory, true-false, actual-apparent, genuine­
fake, authentic-inauthentic, good-bad, and so on. Furthermore, 
this way of thinking is not just a quirk of some heady academic 
exercise called "metaphysics." As Derrida (19816, 19) explains 
in conversation with Julia Kristeva, even everyday language is the 
language of metaphysics. We typically make sense of ourselves 
and our world by deploying sets of terminological differences or 
binary oppositions. 
Yet for Derrida the speech-writing dichotomy, which is the 
defining condition of logocentrism, is not just one binary among 
others. It is the organizing principle. The reason why this oppo­
sition is so important and worthy of attention is that so many 
other things are informed, supported, and regulated by it. Derrida 
(1981a, 103) explains: "It is not enough to say that writing is 
conceived out of this or that series of oppositions. Plato thinks of 
writing, and tries to comprehend it, to dominate it, on the basis 
of opposition as such." So what we find in the Phaedrus is not the 
speech-writing dichotomy as one binary pair situated alongside 
others. According to Derrida, this is the principal opposition, the 
one that describes and orders all the other conceptual opposi­
tions that one way or another come to be associated with it -
inside-outside, reality-appearance, good-bad, and so on. 
From this perspective, what makes LLMs philosophically 
interesting and important, then, is that they actualize and put 
into practice a deconstruction of the logocentric tradition. Or, 
as Richard Coyne (2024) succinctly describes it, "the efficiency 
and effectiveness of text-based language models can be seen as a 
modern validation of Derrida's theory." Consequently, in LLMs 
we have things that write without first speaking or having any­
thing to say. The reason why LLMs have been seen as such a big 
problem and such an urgent crisis is that they not only do not play 
by the existing rules of the game but interrupt the game's very 
operations and legitimacy. By writing without speaking, LLMs 
not only risk generating content that does not make sense. They 
challenge the very conditions of possibility for making sense. 
But, beyond being a theoretical curiosity, why would this be 
important? Why is the deconstruction of logocentrism something 
that should interest us? Why should I, or anyone for that matter, 
give a damn? Such skepticism is reasonable and not entirely 
unjustified, mainly because the principle of noncontradiction and 

Does Writing Have a Future? 115 
the arrangement of things into conceptual pairs have been funda­
mental organizing principles in language and thinking. Operating 
within this logic does not appear to be optional. We do not, for 
example, decide to speak and think in binary terms or not, which 
is obviously just one more binary opposition; we are already sit­
uated in languages and systems of knowing that are essentially 
oppositional in their structures and modes of operation. 
Thus, thinking and speaking in binary oppositions makes 
sense. And it makes sense precisely because this manner of think­
ing and speaking is the very condition of making sense. So what's 
the problem? The problem, as Derrida has pointed out (alongside 
others who, one way or another, can also be placed under the 
umbrella of poststructuralism), is that these logical oppositions 
are already prejudicial. They are not and have never been neu­
tral determinations of objective fact. They institute difference, 
and this difference always makes a difference -socially, politi­
cally, ethically, ideologically. As Donna Haraway (1991, 177) 
explains, "[c]ertain dualisms have been persistent in Western tra­
ditions; they have been systemic to the logics and practices of 
domination of women, people of color, nature, workers, animals 
-in short, domination of all constituted as others, whose task it 
is to mirror the self." 
Consequently, conceptual oppositions, wherever and however 
they are formulated, institute and organize unequal hierarchies, 
which are always determinations of value and exertions of power. 
And LLMs, by participating in the deconstruction of the ruling 
conceptual oppositions of logocentrism, provide a mechanism by 
which one can intervene in this logic and its legacy. Hence LLMs 
are not the end of writing. But they do trace the terminal limits 
of logocentric metaphysics - a way of thinking about writing and 
writing about thinking that, for better or worse, has dominated 
western philosophy and science. 
The Future of Writing 
LLMs and other forms of communicative AI are powerful tech­
nologies, and it is necessary to be critical of the opportunities 
and challenges they present and operationalize. So fa1; however, 
many of the available responses from linguists, philosophers, 
cognitive scientists, and AI experts assume or seek to reassert 

116 Communicative AI 
a questionable and problematic logocentric metaphysics, which 
has functioned as the operating system of western thought for 
centuries. Instead of trying to forcefully reassert the truth of logo­
centrism and the various exceptionalisms and exclusions that it 
has historically supported, it may be more fecund and interesting 
to ascertain how LLM technologies participate in and contribute 
to the deconstruction of this tradition, providing ways to think 
and write differently. Understood in this way, communicative AI 
opens for us a unique opportunity to engage in some deep philo­
sophical reflection on the nature of language, who or what can be 
said to possess or be in possession of it, and what this ultimately 
means for us, self-styled animals with language. This reflection 
has four important consequences for the future. 
First, despite what has been advertised, the problem is not 
only with LLMs and what they can or cannot do. The under­
lying problem is and has always been writing. If we understand 
the written sign �'writing" "in the narrow sense," as defined by 
Derrida (1976) -that is, as a process of arranging words on some 
tangible medium, in linear sequence -then writing will indeed 
continue well into the future. "All writing," Flusser (2011, 6) 
observes, "is orderly, and that leads directly to the contemporary 
crisis in writing. For there is something mechanical about the 
ordering, the rows, and the machines do this better than people 
do." But who or what does that writing, and how that affects 
the meaning of any particular sequence of written content, are 
questions of a dynamic nature that are clearly in flux. So what 
is important and interesting about LLM Ais is that they render 
these challenges legible. 
If we limit ourselves to the logocentric framework, it is hard 
to see this transformation ( or crisis, as some call it) as anything 
but the sign of end times. But this is not a simple ending or ter­
mination, where writing will simply cease or be no more. "What 
was once written," Flusser (2011, 3) explains, "can now be con­
veyed more effectively on tapes, records, films, videotapes, vid­
eodisks, or computer disks." What worried Flusser was not the 
end of writing but its replacement by other modes and media 
of communication. With the technology of communicative AI, 
however, quite the opposite happens. Here the ending consists 
not in replacement but in a kind of exponential proliferation 
of AI-generated content that cannot be controlled or compre­
hended. With AI, then, we seem to experience the victory of 

Does Writing Have a Future? 117 
wntmg and literacy (even hyperliteracy), not their defeat or 
replacement. 
It may well be that we are, or seem to be, in danger of being 
inundated and overwhelmed by "a tsunami of text swept into 
a self-perpetuating cataract of content that makes it function­
ally impossible to reliably communicate in any digital setting" 
(Kirschenbaum 2023 ). Consequently the terminal limits of lit­
eracy are the product not of scarcity but of an obesity of letters. 
And from this vantage point the future of writing appears to be in 
danger, because the customary understanding of the written word 
as a means of unique human expression and as one of the pre­
ferred methods for evaluating what and how others think seems 
to have hit its operational limit. Thus it is not just literature, but 
literacy itself that seems to be threatened by the emerging tech­
nology of AI in general and of LLMs in particular. 
But from another perspective -one that follows the decon­
struction of this tradition, which had been developed and doc­
umented in twentieth-century literary theory, poststructuralist 
philosophy, and feminist STS efforts -this so-called crisis is an 
opportunity to think beyond and in excess of the limitations of 
western metaphysics and its hegemony. Understood in this way, 
LLMs do not threaten writing, nor are they the harbingers of 
that kind of post-literate age that had troubled Flusser. They only 
threaten a particular and limited conceptualization of writing -
one that had already been challenged by innovations in literary 
theory and practice for at least a century before the advent of 
AI. 
Instead of being (mis)understood as signs of the apocalypse 
that herald "the end of writing" (Thomas 2023, iA.net 2023 ), 
LLMs expose the limits of the logocentric privilege, participate in 
the deconstruction of its principles, and open the way for a future 
in which writing is situated otherwise (see Figure 7.2). Writing 
indeed has a future, precisely because it was the written word 
-its linear order and sequential temporality -that created the 
possibility of asking about and planning for a future. Thus writ­
ing has already transformed everything, including our thinking 
about writing and its future (or lack thereof). We are, for better 
or worse, condemned to write. Or, as Flusser writes at the end 
of his essay, "[t]he last writing -that's ridiculous, some will say. 
Certainly more tides of writing will flow through the presses and 
technologically advanced reproduction apparatuses and into the 

118 Communicative AI 
Large Language Models and 
generative Al reveal the 
limits of the logocentric 
privilege, participate in a 
deconstruction of its 
organizing principles, and 
open the opportunity to 
think and write differently. 
Figure 7.2 RIP logocentrism. Created by David Gunkel 
environment ... And in light of such text inflation, it does make 
sense, in the final analysis, to call them at last writings." Today 
writing flows through LLMs. 
Second, by deconstructing logocentrism -or, better, by con­
tributing to the deconstruction of logocentrism, which was 
already underway before the advent of this particular technology 
-LLMs do not destroy logocentrism and do not leave it in ruins. 
Despite common misperceptions and misuses of the word that 
have become something of a professional malpractice, "decon­
struction" does not mean to destroy or disassemble. "The 'de-' 
of deconstruction," Derrida (1993, 147) explains, "signifies not 
the demolition of what is constructing itself, but rather what 
remains to be thought beyond the constructionist or destruction­
ist schema." To put it schematically, deconstruction is a mode 
of intervention in binary opposites such as the speech-writing 
dichotomy, and it consists of two operations -what Derrida 
(1981b, 41) calls "a double gesture": inversion of the existing 
binary and emergence of a new concept, which cannot be con­
tained within or regulated by the existing system and ways of 
thinking. 
Thus, by deconstructing the speech-writing dichotomy, which 
is the defining condition of logocentrism, LLMs ( 1) effectively 
flip the script on that oppositional hierarchy, as they write before 
speaking, and even without it; and (2) mark the emergence of 

Does Writing Have a Future? 119 
a new concept of writing or "text generation" -one that is 
not beholden to the logocentric principle, which makes writing 
derive from (and thereby be dependent on) a prior intention to 
speak. Thus writing has a future -maybe even a bright future 
-beyond the terminal limits of logocentrism and its ruling con­
ceptual oppositions, precisely because LLMs do exactly what 
they have been accused of: they write without wanting to say 
anything and without knowing what it is that they come to say. 
But this is what makes LLMs, and the disruptions they release 
into our understanding of language and writing, so potent and 
important. And if we ask seemingly critical questions like "Is this 
really what Derrida would have wanted?" or "Would Derrida 
approve of his texts on writing being read and interpreted in this 
way?", this mode of inquiry is exactly what is coming to an end: 
questions that ask not only about the author's original intentions 
but also about their authority over how texts come to be used, 
understood, and engaged with. The philosophical opportunity -
or challenge -of LLMs is that they render all this readable. 
Third, it follows from this that, no matter how a text was gen­
erated, the important question that now confronts us when we 
are dealing with it is not about the author ( "Who is the author 
and what do they have to say?"); it is whether and how the writ­
ing comes to makes sense and reveal its truth. Plato anticipated 
this significant change of perspective; for, when Phaedrus crit­
icizes Socrates for talking bullshit with his story about Theuth 
and Thamus, here is how Socrates responds: 
PHAEDRUS: Socrates, you easily make up stories of Egypt or any 
country you please. 
SOCRATES: They used to say, my friend, that the words of the oak 
in the holy place of Zeus at Dodona were the first pro­
phetic utterances. The people of that time, not being so 
wise as you young folks, were content in their simplic­
ity to hear an oak or a rock, provided it only spoke the 
truth; but to you, perhaps, it makes a difference who 
the speaker is and where he comes from, for you do 
not consider only whether his words are true or not. 
(Pl. Phdr., 2756-c) 
As Socrates suggests in this response, what matters is not who 
the speaker is and where they come from but whether the words 
themselves, even if generated by an oak, a rock, or an LLM, 

120 Communicative AI 
speak the truth. Consequently, as Barthes (1978) had written, 
the meaning of any sequence of words resides not in its original 
intentions but in its destination. It is, then, in the act of reading 
that what has been written comes to make sense and have mean­
ing. And this means, of course, as Flusser (2011, 37) has already 
pointed out, that "a text has as many meanings as it has readers." 
The future of writing is in reading -not just in the activity itself 
but in the selection and curation of what is to be read and how. 
And these decisions are not made only by individuals; they also 
represent an undertaking that is always shared, at times conten­
tious, and that defines a particular community of reading and 
readers. Reading and interpretation are relational and communal 
matters. 
Finally, this writing about writing -this writing about the 
future of writing at what seems to be the end of (the) writing -
cannot conclude without confronting and responding to a prac­
tical concern. In order to be internally consistent and avoid the 
charge of performative contradiction, everything that has been 
written here about writing and meaning-making would need 
to apply to and hold for this text. It is therefore reasonable for 
the reader to inquire whether the text they have just read is the 
product of a human author, an output that has been generated 
at the prompt of an LLM, or the result of some form of human­
machine collaboration. Even if we offer the customary tokens 
of authenticity -the proper names of the authors printed on the 
title page, a written statement that this is "100 percent genuine 
human-generated content," a watermark, or some other official 
certificate -the fact is that one has no way to know for sure. 
Such undecidability is typically regarded as a problem that 
should be resolved. But it is precisely this lack of knowing and 
this ambiguity that make the act of reading (and hence the role of 
the reader) powerful, important, and interesting. The destination 
of meaning and communication is at least as important, if not 
more important, than its assumed or retroactively posited origin. 
We are happy to withdraw now as authors; it's your turn. In 
response to the challenges presented to us by recent innovations 
in communicative AI, we can (and should) respond confidently 
with this final line: "What does it matter who is speaking, some­
one said. What does it matter who is speaking?" 

Agtiera y Areas, Blaise and Peter Norvig. (2023 ). Artificial General 
Intelligence Is Already Here. Noema, October 10. https://www. 
noemamag.com/artificial-general-intelligence-is-already-here. 
Altman, Sam. (2023). Planning for AGI and Beyond. OpenAI Web­
site, February 22. https://openai.com/index/planning-for-agi-and­
beyond. 
America, Mark. (2022). My Life as an Arti-ficial Creative Intelligence. 
Stanford, CA: Stanford University Press. 
Anthropic. (2023). Claude's Constitution. Anthropic, May, 9, https:// 
www.anthropic.com/news/claudes-constitution. 
Arendt, Hannah. (2017/1951). The Origins of Totalitarianism. London: 
Penguin. 
Aristotle. (1932). Politics, trans. H. Rackham. Cambridge, MA: 
Harvard University Press. 
Aristotle. (1938). Categories. On Interpretation. Prior Analytics, trans. 
H. P. Cooke. Cambridge, MA: Harvard University Press. 
Aristotle. (1980). The Metaphysics, Books I-IX, trans. Hugh Tredennick. 
Cambridge, MA: Harvard University Press. 
Askell, Amanda et al. (2021). A General Language Assistant as a 
Laboratory for Alignment. Cornell University, ArXiv, https://doi.org 
/10.48550/arXiv.2112.00861. 
Austin, John L. (1962). How to Do Things with Words. Oxford: 
Clarendon. 
Barad, Karen. (2007). Meeting the Universe Halfway: Quantum Physics 
and the Entangle-ment of Matter and Meaning. Durham, NC: Duke 
University Press. 

122 References 
Barthes, Roland. (1978). Death of the Author. In his Image, 
Music, Text, trans. Stephen Heath, 142-148. New York: Hill & 
Wang. 
Baudrillard, Jean. (1994). Simulacra and Simulation, trans. Sheila Faria 
Glaser. Ann Arbor: University of Michigan Press. 
Beckers, Anna and Gunther Teubner. (2021). Three Liability Regimes 
for Artificial Intelligence: Algorithmic Actants, Hybrids, Crowds. 
Oxford: Hart Publishing. 
Belga News Agency. (2023 ). We Will Live as One in Heaven: 
Belgian Man Dies by Suicide after Chatbot Exchanges. Belga, 
March 28. https://www.belganewsagency.eu/we-will-live-as-one 
-in-heaven-belgian-man-dies-of-suicide-following-cha tbot-ex 
changes. 
Bender, Emily M., Timnit Gebru, Angelina McMillan-Major, and 
Shmargaret Shmitchell. (2021 ). On the Dangers of Stochastic Parrots: 
Can Language Models Be Too Big? In Proceedings of the 2021 
Conference on Fairness, Accountability, and Transparency, March 
3-10, 2021 (FAccT '21), Virtual Event, Canada, ACM. https://doi 
.org/10.1145/3442188.3445922. 
Biever, Celeste. (2023 ). ChatGPT Broke the Turing Test: The Race Is On 
for New Ways to Assess AI. Nature 619: 686-689. https://doi.org/10 
.1038/d41586-023-02361-7 
Birkerts, Sven. (1994). The Gutenberg Elegies: The Fate of Reading in 
an Electronic Age. Boston, MA: Faber & Faber. 
Blum, Ben Ash. (2023 ). To Navigate the Age of AI, the World Needs a 
New Turing Test. Wired, August 10. https://www.wired.com/story/ai 
-new-turing-test. 
Bogost, Ian. (2022). ChatGPT Is Dumber Than You Think. The Atlantic. 
https://www.theatlantic.com/technology/archive/2022/12/chatgpt 
-openai-artificial-in telligence-writing-ethics/ 6 723 8 6. 
Bubeck, Sebastien et al. (2023 ). Sparks of Artificial General Intelligence: 
Early Experiments with GPT-4. Cornell University, ArXiv, Computer 
Science. https://doi.org/10.48550/arXiv.2303.12712. 
Caliskan, Aylin, Joanna Bryson, and Arvind Narayanan. (2017). 
Semantics Derived Automatically from Language Corpora Contain 
Human-Like Biases. Science 356(6334): 183-186. 
Carey, James. (1989). Communication as Culture: Essays on Media and 
Society. New York: Routledge. 
Cazzaniga, M. et al. (2024 ). Gen-AI: Artificial Intelligence and the 
Future of Work. Staff Discussion Note SDN2024/001, January. IMF, 
Washington, DC. 
Charlet, Jeremie. (2023 ). Balancing Innovation and Sustainability: 
Unpacking the Environmental Impact of Generative AI. Medium, 
October 4. 

References 123 
Chatterjee, Mohar. (2023 ). AI Cannot Hold Copyright, Federal Judge 
Rules. Politico, August 21. https://www.politico.com/news/2023/08 
/21/ai-cannot-hold-copyright-federal-judge-rules-00111865. 
Chen, Canyu and Kai Shu. (2024 ). Combating Misinformation in the 
Age of LLMs: Opportunities and Challenges. AI Magazine. https:// 
llm-misinformation.github.io/#Combating-Misinformation-in-the 
-Age-of-LLMs-Opportunities-and-Challenges. 
Chesher, Chris. (2023 ). Invocational Media: Reconceptualising the 
Computer. New York: Bloomsbury. 
Chiang, Ted. (2024). Why AI Isn't Going to Make Art. New Yorker, 
August 31. https://www .newyorker .corn/culture/the-weekend-essay 
/why-ai-isnt-going-to-make-art. 
Chowdhury, Rumman. (2023). AI Desperately Needs Global Oversight. 
Wired, April 6. https://www.wired.com/story/ai-desperately-needs­
global-oversight. 
Christiano, Paul F., Jan Leike, Tom Brown, Miljan Martie, Shane 
Legg, and Dario Amodei. (2017). Deep Reinforcement Learning 
from Human Preferences. Neural JPS Proceedings: Advancements 
in Neural Information Processing Systems 30 (NIPS 2017), Long 
Beach, CA. http://papers.neurips.cc/paper/7017-deep-reinforcement 
-learning-from-human-preferences.pdf. 
Coeckelbergh, Mark. (2017). Using Words and Things. New York: 
Routledge. 
Coeckelbergh, Mark. (2018). How to Describe and Evaluate 
"Deception" Phenomena: Recasting the Metaphysics, Ethics, and 
Politics of ICTs in Terms of Magic and Performance and Taking a 
Relational and Narrative Turn. Ethics and Information Technology 
20: 71-85. https://doi.org/10.1007/s10676-017-9441-5. 
Coeckelbergh, Mark. (2022). The Political Philosophy of AI: An 
Introduction. Cambridge: Polity. 
Coeckelbergh, Mark. (2024). Why AI Undermines Democracy and 
What to Do about It. Cambridge: Polity. 
Coeckelbergh, Mark and David Gunkel. (2023). ChatGPT: 
Deconstructing the Debate and Moving It Forward. AI & Society. 
https://doi.org/10.1007/s00146-023-01710-4. 
Cohen, J. (1986). An Epistemic Conception of Democracy. Ethics 97(1): 
26-38. 
Coyne, Richard. (2014). Reflections on Technology, Media and Culture. 
Biog, June 1. https://richardcoyne.com/2024/06/01/derrida-on-ai-2. 
David, Marian. (2015). The Correspondence Theory of Truth. In 
Edward N. Zalta (ed.), Stanford Encyclopedia of Philosophy. https:// 
plato.stanford.edu/entries/truth-correspondence. 
Derrida, Jacques. (1976). Of Grammatology, trans. G. C. Spivak. 
Baltimore, MD: Johns Hopkins University Press. 

124 References 
Derrida, Jacques. (1978). Writing and Difference, trans. A. Bass. 
Chicago, IL: University of Chicago Press. 
Derrida, Jacques. (1981a). Dissemination, trans. B. Johnson. Chicago, 
IL: University of Chicago Press. 
Derrida. Jacques. (1981b). Positions, trans. Alan Bass. Chicago, IL: 
University of Chicago Press. 
Derrida, Jacques. (1982). Margins of Philosophy, trans. Alan Bass. 
Chicago, IL: University of Chicago Press. 
Derrida, Jacques. (1993). Limited Inc, trans. Samuel Weber and 
Jeffrey Mehlman. Evanston, IL: Northwestern University Press. 
Descartes, Rene. (1988). Selected Philosophical Writings, trans. 
John Cottingham, Robert Stoothoff, and Dugald Murdoch. 
Cambridge: Cambridge University Press. 
Dewey, John. (2011). The Problem of Truth. In J. Boydston (ed.), 
John Dewey: The Middle Works, vol. 6, 12-68. Carbondale, IL: 
Southern Illinois University Press. 
Dreyfus, Hubert. (1972). What Computers Can't Do. New York: MIT 
Press. 
Edison, Thomas A. (1878). The Phonograph and Its Future. North 
American Review 126: 527-536. 
Edukitchen. (2023 ). Chomsky on ChatGPT, Russia, Education and 
the Unvaccinated. Youtube, January 21. https://www.youtube.com/ 
watch ?v=IgxzcOugv EI. 
Esposito, Roberto. (2015). Persons and Things, trans. Zakiya Hanafi. 
Cambridge: Polity. 
Estlund, David. (2007). Democratic Authority: A Philosophical 
Framework. Princeton, NJ: Princeton University Press. 
Evans, Katie D., Scott A. Robbins, and Joanna J. Bryson. (2023). Do 
We Collaborate with What We Design? Topics in Cognitive Science, 
August 15. https://doi.org/10.1111/tops.12682. 
Fares, Murhaf, Andrei Kutuzov, Stephan Oepen, and Erik Velldal. 
(2017). Word vectors, reuse, and replicability: Towards a commu­
nity repository of large-text resources. In Jorg Tiedemann (ed.), 
Proceedings of the 21st Nordic Conference on Computational 
Linguistics (NoDaLiDa), 22-24 May 2017. Linkoping University 
Electronic Press. https://doi.org/978-91-7685-601-7. (See also http:// 
vectors.nlpl.eu/explore/embeddings/en.) 
Ferguson, Kirby. (2023 ). Everything Is a Remix. Web film series, 
YouTube, complete updated edn. https://www.youtube.com/watch 
?v=X9R YuvPCQUA. 
Firth, J. R. (1957). A Synopsis of Linguistic Theory, 1930-1955. 
Oxford: Blackwell. 
Flusser, Vilem. (2011). Does Writing Have a Future? trans. Nancy Ann 
Roth. Minneapolis: University of Minnesota Press. 

References 125 
Foucault, Michel. (1984). What Is an Author? trans. Josue V. Harari. 
In Paul Rabinow (ed.), The Foucault Reader, 101-120. New York: 
Pantheon. 
Frankfurt, Harry. (2005). On Bullshit. Princeton, NJ: Princeton 
University Press. 
Friedlander, Emilie. (2019). How Holly Herndon and Her AI Baby 
Spawned a New Kind of Folk Music. The Fader, May 21. https:// 
www.thefader.com/2019/05/21/holly-herndon-proto-ai-spawn-inter 
view. 
Future of Life Institute. (2023). Pause Giant AI Experiments: An 
Open Letter. h ttps :/ /fu tureoflif e. org/ open-letter/ pa use-gian t-ai-expe 
riments. 
Greene, Lucie. (2018). Silicon States: The Power and Politics of Big Tech 
and What It Means for Our Future. Berkeley, CA: Counterpoint. 
Grynbaum, Michael M. and Ryan Mac. (2023 ). The Times Sues OpenAI 
and Microsoft over AI Use of Copyrighted Work. New York Times, 
December 27. https://www.nytimes.com/2023/12/27/business/media 
/new-york-times-open-ai-microsoft-lawsuit.html. 
Gunkel, David J. (2001). Hacking Cyberspace. Boulder, CO: Westview 
Press. 
Gunkel, David J. (2003). Second Thoughts: Toward a Critique of the 
Digital Divide. New Media & Society 5(4): 499-522. https://doi.org 
/10.1177/146144480354003. 
Gunkel, David J. (2016). Of Remixology: Ethics and Aesthetics after 
Remix. Cambridge, MA: MIT Press. 
Gunkel, David J. (2020). An Introduction to Communication and 
Artificial Intelligence. Cambridge: Polity. 
Gunkel, David. J. (2021). Deconstruction. Cambridge, MA: MIT 
Press. 
Gunkel, David J. (2023). Person, Thing, Robot: A Moral and Legal 
Ontology for the 21st Century and Beyond. Cambridge, MA: MIT 
Press. 
Gunkel, David J. (2024 ). AI for Communication. New York: Routledge 
Books. 
Gunkel, David J. (2025). Generative AI and Remix: Difference and 
Repetition. In Eduardo Navas, Owen Gallagher, and xtine burrough 
(eds.), The Routledge Companion to Remix Studies (2nd edn). New 
York: Routledge. 
Guzman, Andrea L. (2018). Introduction: What Is Human-Machine 
Communication, Anyway? In Andrea L. Guzman (ed.), Human­
Machine Communication: Rethinking Communication, Technology 
and Ourselves, 1-28. New York: Peter Lang. 
Haraway, Donna J. (1991). Simians, Cyborgs, and Women: The 
Reinvention of Nature. New York: Routledge. 

126 References 
Haraway, Donna J. (2016). Staying with the Trouble: Making Kin in the 
Chthulucene. Durham, NC: Duke University Press. 
Heidegger, Martin. (1977). Letter on Humanism. In David Farrell Krell 
(ed.), Heidegger: Basic Writings, 189-242. New York: Harper & 
Row. 
Heidegger, Martin. (1994). Basic Questions of Philosophy: Selected 
"Problems" of "Logic," trans. R. Rojcewicz and A. Schuwer. 
Bloomington: Indiana University Press. 
Heikkila, Melissa. (2022). We're Getting a Better Idea of Al's True 
Carbon Footprint. MIT Technology Review, November 14. https:// 
www.technologyreview.com/2022/11/14/1063192/were-getting-a­
better-idea-of-ais-true-carbon-footprint. 
Hicks, Michael Townsen, James Humphries, and Joe Slater. (2024). 
ChatGPT Is Bullshit. Ethics and Information Technology. https://doi 
.org/10.1007/s10676-024-09775-5. 
Holy-tuczaj, Magdalena and Vincent Blok. (2019). How to Deal with 
Hybrids in the Anthropocene? Towards a Philosophy of Technology 
and Environmental Philosophy 2.0. Environmental Values 28(3 ): 
325-345. https://doi.org/10.3197/096327119x15519764179818. 
Hunter, Dan, and Gregory Lastowka. (2004). Amateur-to-Amateur. 
William and Mary Law Review 46: 951-1030. https://scholarship 
.law.wm.edu/wmlr/vol46/iss3/3. 
iA.net. (2023). AI and the End of Writing. Information Architects, 
January 25. https://ia.net/topics/the-end-of-writing-ia-on-ai. 
Johnson, Deborah G. (2006). Computer Systems: Moral Entities but 
Not Moral Agents. Ethics and Information Technology 8: 195-204. 
https://doi.org/10.1007 /s10676-006-9111-5. 
Jones, Cameron R. and Benjamin K. Bergen. (2024 ). People Cannot 
Distinguish GPT-4 from a Human in a Turing Test. Cornell University, 
ArXiv, Human-Computer Interaction, May 9. https://arxiv.org/abs 
/2405.08007. 
Josephson-Storm, Jason A. (2017). The Myth of Disenchantment: 
Magic, Modernity, and the Birth of the Human Sciences. Chicago, 
IL: University of Chicago Press. 
Kant, Immanuel. (1987). Critique of Judgment, trans. W. S. Pluhar. 
Indianapolis, IN: Hackett. 
Kant, Immanuel. (1998/1787). Critique of Pure Reason, trans. 
Paul Guyer and Allen W. Wood. Cambridge: Cambridge University 
Press. 
Kaplan, Jerry. (2016). Artificial Intelligence: What Everyone Needs to 
Know. New York: Oxford University Press. 
Kelly, Kevin. (2014). The Three Breakthroughs That Have Finally 
Unleashed AI on the World. Wired, October 27. https://www.wired 
.com/2014/10/future-of-artificial-intelligence. 

References 127 
Keynes, John Maynard. (2010). Essays in Persuasion. New York: 
Palgrave Macmillan. 
Khowaja, Sunder Ali, Parus Khuwaja, Kapal Dev, Weizheng Wang, and 
Nkenyereye Lewis. (2024). ChatGPT Needs SPADE (Sustainability, 
PrivAcy, Digital divide, and Ethics) Evaluation: A Review. Cognitive 
Computation 16: 2528-2550. https://doi.org/10.1007/s12559-024 
-10285-1. 
Kirschenbaum, Matthew. (2023 ). Prepare for the Textpocalypse. The 
Atlantic, March 8. https://www.theatlantic.com/technology/archive 
/2023/03/ai-chatgpt-writing-language-models/673 318. 
Knibbs, Kate. (2023). Why This Award-Winning Piece of AI Art Can't 
Be Copyrighted. Wired, September 6. https://www.wired.com/story 
/ai-art-copyright-matthew-allen. 
Lakoff, George and Mark Johnson. (1980). Metaphors We Live By. 
Chicago, IL: University of Chicago Press. 
Landemore, Helene. (2017). Beyond the Fact of Disagreement? The 
Epistemic Turn in Deliberative Democracy. Social Epistemology 
31(3): 277-295. https://doi.org/10.1080/02691728.2017.1317868. 
Lemoine, Blake. (2022). Is LaMDA Sentient? An Interview. Medium, 
June 11. https://cajundiscordian.medium.com/is-lamda-sentient-an 
-interview-ea64d916d917. 
Maleki, Negar, Balaji Padmanabhan, and Kaushik Dutta. (2024 ). AI 
Hallucinations: A Misnomer Worth Clarifying. Cornell University, 
ArXiv, Computer Science, January 9. https://arxiv.org/html/2401.06 
796v1. 
Mamak, Kamil. (2021). Whether to Save a Robot or a Human: On the 
Ethical and Legal Limits of Protections for Robots. In Anne Gerdes, 
Mark Coeckelbergh, and David J. Gunkel (eds.), Should Robots Have 
Standing? The Moral and Legal Status of Social Robots, 24-33. doi: 
10.3389/frobt.2021.712427. 
Marche, Stephen. (2023 ). The Future of Writing Is a Lot Like Hip­
Hop. The Atlantic, May 9. https://www.theatlantic.com/technology/ 
archive/2023/05/generative-ai-novel-writing-experiment-stephen­
marche/673997. 
Marcus, Gary. (2024). Taming Silicon Valley: How We Can Ensure that 
AI Works for Us. Cambridge, MA: MIT Press. 
Marcus, Gary and Ernest Davis. (2023 ). Large Language Models like 
ChatGPT Say the Darnedest Things. Garymarcus.substack.com, 
January 9, 2023. https://garymarcus.substack.com/p/large-language 
-models-like-chatgpt. 
McLuhan, Marshall. (1995). Understanding Media: The Extensions of 
Man. Cambridge, MA: MIT Press. 
McQuate, Sarah. (2023). Q&A: UW Researcher Discusses Just How 
Much Energy ChatGPT Uses. University of Washington, UW News. 

128 References 
July 27. https://www.washington.edu/news/2023/07/27/how-much 
-energy-does-cha tgpt-use. 
Minh-ha, Trinh, T. (1989). Woman Native Other: Writing Postcoloniality 
and Feminism. Bloomington: Indiana University Press. 
Natale, Simone. (2021). Deceitful Media: Artificial Intelligence and 
Social Life after the Turing Test. New York: Oxford University 
Press. 
Nature Editorial. (2023 ). Tools Such as ChatGPT Threaten Transparent 
Science: Here are our Ground Rules for Their Use. Nature 613: 612. 
https://doi.org/10.1038/d41586-023-00191-1 
The New York Times Company v. Microsoft Corporation, 1:23-cv-
11195, S.D.N.Y. 27 December 2023. 
Nietzsche, Friedrich. (1974). The Gay Science, trans. Walter Kaufmann. 
New York: Random House. 
Nietzsche, Friedrich. (1980). Nachgelassene Fragmente, 1869-1874. 
In Giorgio Colli and Mazzino Montinari (eds.), Samtliche Werke, 
vol. 7: Kritische Studienausgabe. Berlin: Walter de Gruyter. 
Nietzsche Friedrich. ( 1983 ). Twilight of the Idols. In Walter Kaufmann 
(ed. and trans.), The Portable Nietzsche. New York: Penguin Books. 
Nietzsche, Friedrich. (1989). Beyond Good and Evil, trans. Walter 
Kaufmann. New York: Vintage Books. 
Nietzsche, Friedrich. (2020). About Truth and Lie in an Extra­
Moral Sense. In Daniel F. Ferrer (ed. and trans.), Nietzsche's Seven 
Notebooks from 1878. https://archive.org/details/nietzsches-seven 
-notebooks-from-1876. 
Ong, Walter J. (1995). Orality and Literacy: The Technologizing of the 
Word. New York: Routledge. 
OpenAI. (2024). OpenAI Charter. https://openai.com/charter. 
OpenAI. (2024 ). OpenAI and Journalism. January 8. https://openai.com 
/index/openai-and-journalism. 
Oremus, Will. (2022). Google's AI Passed a Famous Test: And Showed 
How the Test Is Broken. Washington Post, June 17. https://www 
.washingtonpost.com/technology/2022/06/17/google-ai-lamda­
turing-test. 
Plato. (1977). Cratylus, trans. H. N. Fowler. Cambridge, MA: Harvard 
University Press. 
Plato. (1982). Euthyphro, Apology, Crito, Phaedo, Phaedrus, trans. 
Harold North Fowler. Cambridge, MA: Harvard University Press. 
Plato. (1987). Republic, trans. P. Shorey. Cambridge, MA: Harvard 
University Press. 
Plato. (1997). Gorgias. In John M. Cooper (ed.), Plato, Complete 
Works, 791-869. Indianapolis, IN: Hackett Publishing. 
Raper, Rebecca et al. (2022). Sustainability Budgets: A Practical 
Management and Governance Method for Achieving Goal 13 of the 

References 129 
Sustainable Development Goals for AI Development. Sustainability 
14(7), art. 4019. https://doi.org/10.3390/su14074019. 
Ricrem; Paul. (1984). Time and Narrative, vol. 1, trans. Katheen 
McLaughlin and David Pellauer. Chicago, IL: University of Chicago 
Press. 
Ricreur, Paul. (2007). Refl,ections on the Just, trans. David Pellauer. 
Chicago, IL: University of Chicago Press. 
Rorty, Richard. (1979). Philosophy and the Mirror of Nature. Princeton, 
NJ: Princeton University Press. 
Rose, Mark. (2002). Copyright and Its Metaphors. UCLA Law Review 
50(1): 1-15. https://www.uclalawreview.org/copyright-and-its-meta 
phors. 
Schank, Roger C. (1990). What Is AI Anyway? In Derek Partridge and 
Yorick Wilks (eds.), The Foundations of Artificial Intelligence: A 
Sourcebook, 3-13. Cambridge: Cambridge University Press. 
Saussure, Ferdinand de. (1959). Course in General Linguistics, trans. 
W. Baskin. London: Peter Owen. 
Searle, John. (1980). Mind, Brains and Programs. Behavioral and Brain 
Sciences 3(3 ): 417-424. https://doi.org/10.1017/S0140525X0000 
5756. 
Searle, John. (1996). The Construction of Social Reality. London: 
Penguin. 
Searle, John. (1999). The Chinese Room. In R. A. Wilson and F. Keil 
(eds.), The MIT Encyclopedia of the Cognitive Sciences, 115-116. 
Cambridge, MA: MIT Press. 
Sengupta, Bhagyasree. (2024). Elon Musk Says "Woke AI" Could 
"Potentially" Kill People. Republic, March 16. https://www.republic 
world.com/world-news/elon-musk-says-woke-ai-can-potentially-kill 
-people/?amp=1. 
Shannon, Claude E. (1950). Programming a Computer for Playing 
Chess. Philosophical Magazine (series 7) 41(314): 256-275. https:// 
doi.org/10. 1080/14 786445008521796. 
Shannon, Claude E. and Warren Weaver. (1949). The Mathematical 
Theory of Communication. Urbana: University of Illinois 
Press. 
Shrivastava, Rashi. (2024). The Prompt: Google's AI Suggested Adding 
Glue to Pizza. Forbes, May 28. https://www.forbes.com/sites/rashis 
hrivastava/2024/05/28/the-prompt-googles-ai-suggested-adding-glue 
-to-pizza. 
Smith, Daniel W. (2006). The Concept of the Simulacrum: Deleuze 
and the Overturning of Platonism. Continental Philosophy Review 
38(1/2): 89-123. doi: 10.1007/s11007-006-3305-8. 
Spawning.ai. (2024 ). Spawning: Data Governance for Generative AI. 
https://spawning.ai. 

130 References 
Spivak, wyatri Chakravorty. (1998). In Other Worlds: Essays in 
Cultural Politics. New York: Routledge. 
Stiegler, Bernard. (2008). Technics and Time, vol. 2: Disorientation, 
trans. by Stephen Barker. Stanford: Stanford University Press. 
Strauss, William. (1955). The Moral Right of the Author. American 
Journal of Comparative Law 4(4 ): 506-538. https://doi.org/10.2307 
/838072. 
Suleyman, Mustafa. (2023). My New Turing Test Would See If AI Can 
Make $1 Million. MIT Technology Review, July 14. https://www 
.technologyreview.com/2023/07/14/1076296/mustafa-suleyman-my 
-new-turing-test-would-see-if-ai-can-make-1-million. 
Tangermann, Victor. (2024). Sam Altman Says AI Using Too Much 
Energy, Will Require Breakthrough Energy Source. Futurism, 
January 17. https://futurism.com/sam-altman-energy-breakthrough. 
Tanner, Stening. (2023). What Are AI Chatbots Actually Doing When 
They "Hallucinate"? Here's Why Experts Don't Like the Term. 
Northeastern Global News, September 28. https://news.northeastern 
.edu/2023/11/10/ai-chatbot-hallucinations. 
Thaler (Appellant) v Comptroller-General of Patents, Designs and Trade 
Marks (Respondent) [2023] UKSC 49. https://www.supremecourt 
. uk/cases/docs/uksc-2021-0201-judgment. pdf. 
Thomas, Sean. (2023). AI Is the End of Writing. The Spectator, January 
10. https://www.spectator.co. uk/article/ai-is-the-end-of-writing. 
Turing, Alan. (1950). Computing Machinery and Intelligence. Mind 59 
(236): 433-460. https://doi.org/10.1093/mind/LIX.236.433. 
United Nations Secretary-General's Advisory Body on Artificial 
Intelligence. (2023 ). Governing AI for Humanity. Interim Report 
December 2023. United Nations. 
US Copyright Office. (2024). What Is Copyright. https://www.copyright 
.gov/what-is-copyright. 
Vallor, Shannon. (2024a). The Danger of Superhuman AI Is Not What 
You Think. Noema, May 23. https://www.noemamag.com/the-dan 
ger-of-superhuman-ai-is-not-what-you-think. 
Vallor, Shannon. (20246 ). The AI Mirror: How to Reclaim our Humanity 
in an Age of Machine Thinking. Oxford: Oxford University Press. 
Velmans, Max. (2000). Understanding Consciousness. London: 
Routledge. 
Vries, Alex de. (2023 ). The Growing Energy Footprint of Artificial 
Intelligence. Joule 7(10): 2191-2194. https://doi.org/10.1016/j.joule 
.2023.09.004 
Watercutter, Angela. (2023 ). The Hollywood Strikes Stopped AI from 
Taking Your Job: But for How Long? Wired, December 25. https:// 
www.wired.com/story/hollywood-saved-your-job-from-ai-2023-will 
-it-last. 

References 131 
Weatherby, Leif. (2023 ). ChatGPT Broke the Turing Test. Boston Globe, 
November 13. https://www.bostonglobe.com/2023/11/13/opinion/ 
turing-test-ai-chatgpt. 
Weil, Elizabeth. (2023 ). You Are Not a Parrot: And a Chatbot Is Not 
a Human: And a Linguist Named Emily M. Bender Is Very Worried 
What Will Happen When We Forget This. New York Magazine, 
March 1. https://nymag.com/intelligencer/article/ai-artificial-intelli 
gence-chatbots-emily-m-bender.html. 
Wikipedia. (2024 ). Citing Wikipedia. https://en.wikipedia.org/wiki/ 
Wikipedia:Citing_ Wikipedia. 
Wittgenstein, Ludwig. (1995/1922). Tractatus logico-philosophicus. 
New York: Routledge. 
Wittgenstein, Ludwig. (2009/1953 ). Philosophical Investigations (rev. 
4th edn), trans. G. E. M. Anscombe, P. M. S. Hacker, and J. Schulte. 
Malden, MA: Wiley. 
Wodecki, Ben. (2023 ). OpenAI's GPT-4 Has Lowest Hallucination 
Rate. AI Business, November 21. https://aibusiness.com/nlp/openai 
-s-gpt-4-surpasses-ri vals-in-documen t-summary-accuracy.
Wolf, Michael P. (2024 ). Philosophy of Language. In The Internet 
Encyclopedia of Philosophy. https://iep.utm.edu/lang-phi. 
Zizek, Slavoj. (2008a). For They Know Not What They Do: Enjoyment 
As a Political Factor. London: Verso. 
Zizek, Slavoj. (20086). In Defense of Lost Causes. London: Verso. 

Index 
accountability 28, 31-32 
apocalyptic 80, 106 
Arendt, Hannah 29, 102 
Aristotle 2, 57-60, 64, 73, 77-78, 
96, 102, 109, 111 
artificial intelligence (AI) vii-viii, 
1-15,24-56,59,66, 71, 
74-76,81-88,89-94,98, 100, 
103-106, 109, 115-117, 120 
artificial general intelligence 
(AGI) 1, 26 
artificial neural networks (ANNs) 5, 
15, 17, 91 
Austin, John Langshaw 95, 100 
authenticity 2, 39, 60, 81, 107, 114, 
120 
author function 7, 74, 80, 84-86, 88 
authority 7, 25, 40, 71, 74-77, 
80-81,84-87, 110,119 
authorship 7-8, 25, 36-41, 58, 
63-68, 71, 74-88, 110-112, 
119-120 
axiology 52, 70, 109 
Bard 106 
Barthes, Roland 7, 66, 75-86, 120 
Baudrillard, Jean 69-70 
BERT 11 
bias 5, 22-23, 27, 29-31, 98, 100 
binary 50-56, 61, 66, 69, 113-115, 
118 
bullshit 2, 8, 83, 96-103, 113, 119 
bullshit machine 97-98 
chatbot 2, 12, 27-30, 46, 64-65, 111 
ChatGPT viii, 1-8, 21, 26-28, 
33-36,40,47,64-65,80,83, 
86,96-99, 107, 110-113 
Chinese room thought experiment 
50-51,58 
Chomsky, Noam 36 
Claude 1, 7, 11, 24, 30, 98, 106 
common good 32 
communication vii-viii, 1-3, 6-7, 
29,57-73, 77, 79,89-90, 105, 
107, 116, 120 
communicative AI, vii-viii, 2-11, 
26-35,48,51,55,59,66, 
71, 74,81,85-90,98, 100, 
103-106, 111, 115-116, 120 
consciousness 3--4, 6, 42--46, 53-55, 
92 

Index 133 
Copernican revolution 1-2, 79 
copyright 6-7, 24-25, 28, 35-41, 
77, 79-80,86-87 
copyright law 37, 40, 77, 79-80 
correspondence theory of truth 
59-61,89,93-94,97,99, 
100-101 
creativity 3, 37, 40-41, 85 
Dartmouth workshop 12, 51 
death of the author 7, 66, 80-81, 
84, 86; see also authorship; 
Barthes 
deception 6, 48-53, 70, 90, 93, 
96-100, 111 
deep learning 5 
democracy 2, 6, 8, 27-32, 72, 
89-91, 98-105 
democratic governance 28, 
89-90, 101 
epistemic democracy 102-103 
epistemic foundations of 
democracy 8, 90, 102-105 
Derrida, Jacques 60, 63-64, 76, 78, 
83-84, 108-110, 114-119 
Descartes, Rene 2, 6, 45-46, 57, 78, 
79,94 
difference 61, 63-64, 73, 84, 
114-115, 119 
digital divide 28, 33 
education 28, 39, 94, 103, 105 
ELIZA 2, 12, 46 
energy consumption 33-34 
environmental impact 5, 25, 27, 
33-35 
epistemic foundations of democracy 
8, 90, 102-105 
ERNIE 1 
ethics 2-6, 23, 27-41, 53, 89, 92, 
100, 111-112, 115 
facts 2, 22-23, 27-29, 61, 63, 70, 
89-94,96-99, 104,115 
fact vs. fiction 23, 29, 31, 92, 
102-103 
social fact 96 
fake 4, 29, 65, 90, 97, 103, 114 
fake news 90, 103 
Flusser, Vilem 8, 106, 116-117, 120 
form of life 63 
Foucault, Michel 7, 74-75, 78-81, 
86, 100 
Gemini 1, 31, 90, 106 
generative AI, 5, 8, 26, 34, 38, 41, 
81, 84, 87-88, 90,94, lll;see 
also artificial intelligence 
GOF AI (good old-fashioned AI) 
14-15 
OPT 11, 19-26, 46, 80, 106, 110 
GPT-4 1, 4, 20-21, 47, 65, 92 
Grok 1 
hallucination 4, 7-8, 23, 27-29, 
70-71,89-93,96, 101-104, 
113 
Heidegger, Martin 61-65, 94 
hyperliteracy 117 
intellectual property (IP), 24, 28, 36, 
40, 85-86; see also property 
intelligence 2-3, 6, 42-48, 51-55, 
63,65, 109 
imitation game 44-4 7 
Keynes, John Maynard 32 
LaMDA 11, 42, 46, 106 
language 1-7, 12-18, 21, 45-47, 51, 
56-66, 73,83-84,88,94-96, 
99-101, 104, 111, 114-116, 
119 
language game 95-96, 99, 103-105 
large language models (LLMs) 1, 4, 
11, 15,21-22, 80,97, 110 
liability 56, 86 
lies 2, 28, 89, 95-98, 103 

134 Index 
linguistics 3, 6, 12, 59, 61, 64, 73, 
84 
linguistic tokens 13, 15, 51, 58, 91 
linguistic turn 61 
literacy 39, 109, 117 
Llama 1 
logocentrism 8, 57, 63, 78, 81, 83, 
107, 110-119 
machine intelligence 6, 12, 43--44 
map69 
meaning 6, 13, 18, 45--47, 58-66, 
74,80-84,88,94-96, 101,104, 
111-113, 116, 120 
meaning-making 6, 66, 74, 
81-84, 104, 112-113, 120 
narrative meaning 96 
performance of 101 
McLuhan, Marshall 69 
metaphysics 49, 52, 70, 78, 85, 94, 
107, 110-11 7 
logocentric metaphysics, 78, 107, 
110, 113, 115-116; see also 
logocentrism 
Platonic metaphysics 52 
realist metaphysics 94 
mirror 27, 30, 60-63, 71-72, 78, 
115 
misinformation 7-8, 29, 35, 89-91, 
96, 101-104 
moral status 6, 55 
neo-liberalism 31 
Nietzsche, Friedrich 69-70, 85, 95, 
100, 113 
NLP (natural language processing) 
1, 5, 11, 14-15, 26, 30, 46 
originality 2, 6, 28, 36--41, 60, 
63-72, 77, 79, 82-87, 108-111, 
119-120 
other minds, the problem of 6, 45, 
52-53 
oversight 
paternalism 76-77, 110 
performance 69, 75, 101, 104, 
108-109, 112-113 
human-non-human 113 
of meaning 101 
truth performance 101 
philosophy of mind 53-54 
plagiarism 6, 25, 28, 36--41, 52, 77, 
86 
Plato 2, 8, 40, 49-52, 61-65, 76, 
80-83,93-104, 108-114, 119 
Platonism 69-70, 80, 98, 99, 101, 
109-113 
poststructuralism 7-8, 61, 65-66, 
73, 115, 117 
post-truth 103 
power 4, 8-9, 25, 28-33, 38, 56, 61, 
70-72,84,86-87,90,93,95, 
100, 104-105, 115,120 
privacy 4, 27-28, 35 
property24,28,36,40,55, 75, 79, 
85-87 
intellectual property (IP) 24, 28, 
36,40,85-86 
realism 7, 59-60, 73, 93-94, 97 
metaphysical realism 94 
Platonic realism 63, 93-94, 97 
referential realism 59-60, 73 
reality (vs. appearance) 1, 25, 
28-30,44--45,48-53,58-73, 
83-84,92-104, 111-114 
shared reality 69 
social reality 2, 30 
referent 58-63, 69, 73, 84, 96, 101 
relational 96, 100-101, 120 
remix 37-38, 67-72, 86-87, 110 
representationalism 7, 28, 61-62, 
65,69, 71,94,98-101, 104, 
109, 111 
responsibility 7, 9, 27-30, 40, 75, 
79, 84, 104-105 
responsible development 8, 90, 
102-105 

Index 135 
Ricreur, Paul 79, 96 
ritual view of communication 67-73 
Rorty, Richard 8, 60, 71, 95 
Sapir-Whorf hypothesis 64 
de Saussure, Ferdinand 61 
Searle, John 6, 50-52, 95-96, 100 
security 35 
semiotics 59, 62, 84 
signifiers 58, 62, 64, 78, 83 
signs 6, 44-47, 54, 57-66, 73, 78, 
83-84, 106-111, 116-118 
simulacra 69 
simulants 70 
simulation 12, 28, 48, 50, 53, 65, 
69-70 
Socrates 8, 40, 63, 93, 102, 
108-110, 119 
speech 1-2, 60-65, 78, 95, 98, 100, 
105, 108-111, 114, 118 
speech-writing dichotomy 114, 
118 
speech act 95, 100, 105 
stochastic parrots 65, l 07 
structuralism 61, 64 
Sustainable Development Goals 
(SDGs) 34 
technologizing the word 111 
terms of service (ToS) 35 
text 1, 3-7, 11-15, 20-25, 30, 36, 
38-40,65-66, 71-72, 74-88, 
97-98, 101, 110-113, 117-120 
text generation 4-7, 40, 119 
totalitarianism 29, 102 
training data 6, 20, 22, 24, 27-30, 
36-38, 47, 91, 107 
transformer architectures 4-5,11, 
19-20,25,43 
transmission view of 
communication 67-73, 77 
truth 2-3, 7-8, 23, 49, 59-61, 
70-75,80-81,88-105, 107, 
111, 119 
Turing, Alan 6, 12, 44-46, 51, 
56-57 
Turing's game of imitation 46-47, 
50-52 
Turing test 6, 46-48, 50, 57 
understanding 3, 6, 12-13, 16, 22, 
49-51, 58-59,62,64-67, 
72-73, 77,83,92, 110 
unemployment 27, 32-33 
technological unemployment 
32-33 
Wittgenstein, Ludwig 8, 60-65, 
94-95,99 
word vectors 18-19 
writing 1, 3-4, 7-9, 24, 28, 39-40, 
52,59,62-66, 74-83,86-87, 
99, 106-120 
as a form of AI 109 
as bastard 109-110 
as secondary 109 
the future of 8, 37, 40, 87, 
106-120 
victory of (hyper literacy) 
116-117 
```
