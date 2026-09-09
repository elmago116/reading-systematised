---
title: "Signs for Ethical AI: A Route Towards Transparency"
author: Dario Garcia-Gasulla, Atia Cortés, Sergio Alvarez-Napagao, Ulises Cortés
year: "2020"
Type: Preprint
DOI: 10.48550/arXiv.2009.13871
source: https://arxiv.org/abs/2009.13871
created: 2026-05-05
description: Today, Artificial Intelligence (AI) has a direct impact on the daily life of billions of people. Being applied to sectors like finance, health, security and advertisement, AI fuels some of the biggest companies and research institutions in the world. Its impact in the near future seems difficult to predict or bound. In contrast to all this power, society remains mostly ignorant of the capabilities
tags:
  - op/acc/pending-review
pdfORepub: "[[Signs for Ethical AI A Route Towards Transparency.pdf]]"
---
[[Signs for Ethical AI A Route Towards Transparency.pdf]]

> **Abstract:** Today, Artificial Intelligence (AI) has a direct impact on the daily life of billions of people. Being applied to sectors like finance, health, security and advertisement, AI fuels some of the biggest companies and research institutions in the world. Its impact in the near future seems difficult to predict or bound. In contrast to all this power, society remains mostly ignorant of the capabilities

## Full text (extracted from `Signs for Ethical AI A Route Towards Transparency.pdf`)

*Source:* `2PDF/Signs for Ethical AI A Route Towards Transparency.pdf`  
*Extracted:* 2026-05-05

```text
Springer Nature 2021 LATEX template
Signs for Ethical AI: A Route Towards
Transparency
Dario Garcia-Gasulla1*, Atia Cortés1, Sergio
Alvarez-Napagao1 and Ulises Cortés1,2
1*Barcelona Supercomputing Center (BSC), Barcelona,Spain.
2Universitat Politécnica de Catalunya - Barcelona-TECH,
Barcelona,Spain.
*Corresponding author(s). E-mail(s): dario.garcia@bsc.es;
Contributing authors: atia.cortes@bsc.es; sergio.alvarez@bsc.es;
ia@cs.upc.edu;
Abstract
Today, Artiﬁcial Intelligence (AI) has a direct impact on the daily life
of billions of people. Being applied to sectors like ﬁnance, health, se-
curity and advertisement, AI fuels some of the biggest companies and
research institutions in the world. Its impact in the near future seems
diﬃcult to predict or bound. In contrast to all this power, society re-
mains mostly ignorant of the capabilities and standard practices of AI
today. To address this imbalance, improving current interactions between
people and AI systems, we propose a transparency scheme to be imple-
mented on any AI system open to the public. The scheme is based on
two pillars:Data Privacy and AI Transparency. The ﬁrst recognizes the
relevance of data for AI, and is supported by GDPR. The second con-
siders aspects of AI transparency currently unregulated: AI capabilities,
purpose and source. We design this pillar based on ethical principles.
For each of the two pillars, we deﬁne a three-level display. The ﬁrst level
is based on visual signs, inspired by traﬃc signs managing the inter-
action between people and cars, and designed for quick and universal
interpretability. The second level uses factsheets, providing limited de-
tails. The last level provides access to all available information. After
detailing and exemplifying the proposed transparency scheme, we de-
ﬁne a set of principles for creatingtransparent by designsoftware, to be
used during the integration of AI components on user-oriented services.
1
arXiv:2009.13871v2  [cs.CY]  9 May 2022
Springer Nature 2021 LATEX template
2 Signs for Ethical AI
Keywords: Ethical AI, Data Privacy, AI Transparency, GDPR and AI Act,
Information Display
1 INTRODUCTION
At the beginning of the XXI century, society is being forced to integrate a
disrupting technology: Artiﬁcial Intelligence (AI). With striking resemblance,
the same happened at the beginning of the XX century with another disrupt-
ing technology: Automobiles. Back in the 1900s, as cars were introduced to
roads and streets, people had to integrate them in their everyday life. This
caused signiﬁcant conﬂict between the few who were proﬁting the most from
the technology, and the rest (4). The legislation had to be put in place to settle
this conﬂict, a process that spanned several decades. Among the ﬁrst regula-
tions to be implemented was the registration of automobiles, which happened
gradually between 1901 and 1920. It met with resistance from automobile as-
sociations. Driving licenses and speeding limits were also the subject of vivid
debate until their beneﬁts became evident to all agents. The most challenging
of automobile regulations, the one which took the most to be implemented in
a standardized manner, was the one responsible for organizing the interaction
between people and automobiles in traﬃc. That is, traﬃc signs. A wide vari-
ety of traﬃc signs have been developed in the last century, and continue to
change today, adapting to the new paradigms of mobility. The purpose of traf-
ﬁc signs is to limit the actions of automobiles to those safe to the public, but
also to inform the public on how to interact responsibly with these powerful
and potentially dangerous machines.
Today, society faces a similar challenge. AI is a disruptive technology that
has started playing a signiﬁcant role in our everyday life. A conﬂict of interests
emerged between the few who are proﬁting from AI the most and the rest.
Society is now in the process of creating legislation for AI. Looking ahead, if we
consider the example from the previous century, it may take us decades until
AI is correctly integrated into society. On the plus side, society may progress
signiﬁcantly by the end. One of the pending tasks on this journey is to deﬁne
and implement proper means of interaction between the public and AI. We
still need to ﬁnd ourtraﬃc signs for AI.
With this idea in mind, we start by looking at the nature and use of AI.
At which aspects of AI should be transparent by fundamental ethical reasons.
After a bibliography review described in Section 2, we decided to split the
problem betweenData Privacy and AI Transparency. Data privacy considers
the ethical and legal answers to questions like, who is gathering my data? For
what purpose? AI Transparency considers only the ethical answers (since no
legislation exists yet) to questions like, is there an AI algorithm running? What
is it doing? Am I being targeted?
From these two pillars, we design a complete transparency scheme, de-
scribed in Section 4, which covers each topic at three levels of depth. The
Springer Nature 2021 LATEX template
Signs for Ethical AI 3
ﬁrst level, based on visual signs, is meant to be always visible, and accessible
to everyone. The second level provides a degree of personalisation. Moreover,
the third oﬀers all the technical details available. A summary of the display
is shown in Figures 1 and 2. After the main contribution, Section 5 exempli-
ﬁes how it should operate in practice. Section 6 introduces thetransparency
by designprinciples, which can be used as blueprint for the development of AI
systems. Then, Section 8 reviews some works in a similar direction found in
the bibliography. Finally, Section 9 discusses the conclusions and future work.
2 ETHICAL AND TRANSPARENT AI
AI methods are not unethical by nature. Potentially unethical features, like
those exploiting private information or producing biased responses, are inher-
ent to AI methods required for services that our society values and demands.
That being said, the use of AI can become unethical rather easily. The most
straightforward way is to hide the existence of AI and its arguable proper-
ties from users. Thus, he ﬁrst necessary step to enable ethical behaviour is
transparency since an ethical AI is only possible within a society aware of
its existence. A society where users can make informed decisions on their
interactions with AI systems, aware of what they are conceding and gaining.
The role of transparency within trustworthy AI is not straight-forward, as
it depends on the context and does not follow a linear relation (9). Turilliet al.
identify two contradicting deﬁnitions of transparency (31), depending on the
domain of application. From an ethical perspective, transparency relates to
Figure 1 Summary of the scheme proposed for Data Privacy. Including three levels of
information detail.
Springer Nature 2021 LATEX template
4 Signs for Ethical AI
Figure 2 Summary of the scheme proposed for AI Transparency. Including three levels of
information detail.
the notion ofvisibility of the information (access, intended use or behaviour).
At the same time, in the traditional IT domain, it also refers to theinvisibility
towards the user. The purpose of the latter was to facilitate access from end-
users who were not familiarised with the technology fueling computer systems.
Its main objective was to make technology an appealing, user-friendly tool.
This approach to transparent technology has been satisfactory for many years,
enabling the digitalization of society. However, with the generalized adoption
of technology, and the emergence of AI systems, which demands more respon-
sibility from users, the drawbacks of the invisibility approach have surpassed
its beneﬁts.
As of today, AI systems are often fed with personal or sensitive data, stored
in data warehouses that are sometimes located on a third country or continent,
and thus subjected to diﬀerent regulations. This data is also often aggregated
into new dataset that are used for other purposes unknown to the data owner
(i.e., the person itself). We are moving from an information society to an al-
gorithmic society, where personal data is the new type of currency. In this new
context,allend-usershaveanactiveroleasdatadonors.Consciousnessmustbe
created regarding the potential impact of data transactions, both for the indi-
vidual and the collective well-being. Otherwise, as it is already being disclosed
on diﬀerent scandals, we are bounded to a constant stream of data misuses,
behavioural manipulations and massive discriminations. Unethical scenarios
that ought to be opposed through the visibility approach to transparency.
Springer Nature 2021 LATEX template
Signs for Ethical AI 5
2.1 TRANSPARENCY IN ETHICAL AI LITERATURE
The ethical relevance of transparency is evident in the literature. In (16)
authors review, 84 guidelines on ethical AI published around the world, by
governments, high-tech giants or supra-national groups. Transparency, along
with related terms such as explainability, interpretability, communication, dis-
closure and others, is themost mentioned ethical principle, appearing in 73
out of 84 documents. In most of the reviewed literature, transparency is seen
as a facilitator needed to achieve the rest of the principles of trustworthy AI
systems. For example, if the information used to train an algorithm is pub-
lic, it will contribute to reduce or avoid bias or unfair outcomes. In practice,
transparency engages key ethical AI components such as accountability, trace-
ability, justiﬁcation, and proper assessment of capabilities and limitations of
AI systems.
The ﬁrst declaration of principles for the future research and development
of AI was the Asilomar AI Principles (10). In these generic and high-level
guidelines, transparency appears divided into two diﬀerent ethical principles:
failure transparency and judicial transparency. The former relates to the pos-
sibility to discover why did an AI system cause some harm, while the latter
refers to explainability of any judicial decision-making process to an expert
human.
The deﬁnition and role of transparency have been further reﬁned in more
recent contributions. The High-Level Expert Group on Artiﬁcial Intelligence
(AI HLEG) from the European Union has recently published a ﬁrst draft of
the Trustworthy AI Guidelines (14), where transparency is one of its seven
requirements. The guidelines propose a human-centred approach, to enhance
end-users’ conﬁdence in using AI systems by oﬀering means for a trustworthy
interaction, respecting human agency and promoting governance mechanisms
to ensure full accountability. The concept of transparency is here related to
everything that is relevant to an AI system,i.e. the data, the system and
the business model. This includes providing means of(i) traceability of the
data and processes; (ii) methods of explainability to understand both the
technical aspects of the AI systems and the human decisions; and(iii) channels
of communication to inform users when interacting with an AI system.
The IEEE has also published a draft version of their Ethical Aligned De-
sign (30) principles and recommendations, being transparency one of the eight
presented principles. Transparency is also linked to the level of disclosure of
a decision. However, it focuses on decisions made by the system (or actions
from a robot). In encompasses the concepts of explainability, traceability and
interpretability.
Transparency is also one of the ﬁve principles of the OECD (21) document
ofrecommendationstobuildtrustworthyAIsystems.Transparency,alongwith
explainability, is linked to a responsible disclosure of the information. The
objective is to provide means to end-users and stakeholders to understand
the outcomes of an AI system and make them aware of the interactions with
these systems. In June 2019, the G20 Ministerial Meeting on Trade and Digital
Springer Nature 2021 LATEX template
6 Signs for Ethical AI
Economics published their declaration of principles andrecommendations(11),
based on the OECD document, and with a human-centred perspective.
Signiﬁcantly, the guidelines here reviewed target a diﬀerent set of stake-
holders. Depending on whether the document is more or less human-centric,
the responsibility is centred on the AI system or robot, such as is the case of
Asilomar, or on the developers and users, such as in the HLEG case. At this
point, it seems clear that all the stakeholders involved in the AI ecosystem
must assume a certain degree of responsibility, and coherently, a certain level
of transparency. The management of organisations must assume transparency
as a core value, including (and enforcing) it in their codes of conduct, for em-
ployees and members to follow. The designers and developers of AI systems
need to integrate traceability and explainability as yet another necessary san-
ity check of their work. Last but not least, the end-users (or laypersons) need
to be engaged in this process of learning how to interact with AI systems, un-
derstand the impact or origin of a decision and actively demand transparency
processes. In general terms, it means to be responsible for the use of AI at
every level of consumption.
The many existing stakeholders of ethical AI illustrates the need for a vari-
able level of transparency, linked with the expertise of the user. For instance,
a developer should be able to understand and explain the algorithms behind
the AI system or justify the data set that has been used. However, should we
demand a layperson to understand AI algorithms and data technologies to ex-
ercise their rights? Or is it enough to inform on the data processing and its
outcomes? Such questions derive from the GDPR, and especially the Recital
71, which states that, under certain conditions, organisations must be able to
explain to end-users the algorithms used to make decisions but does not spec-
ify which is the satisfactory level of explanation (26), this is directly related
with the right to an explanation(5). From a technical perspective, while ac-
knowledging recent advances (27; 28), there is a generalized lack established
metrics to assess the transparency of an AI system, an endemic limitation of
the ﬁeld that we try to at least bound in this work. Similarly, (34) raises the
question about the appropriate timing to inform the user. Should it be before
the automatic-decision process takes place, or after in order to explain the fea-
tures or weights that were used to obtain a given outcome? Our stand in this
regard is on the protectionist side, as discussed in Section 5.
A common aspect in all the existing guidelines and recommendations is
that none of them are linked to a regulatory enforcement, or propose speciﬁc
implementation mechanisms. To make the diﬃcult transition from theory to
practice, mechanisms need to be put in place to verify and certify AI systems.
To advance in this direction, this paper makes a clear contribution through
the complete speciﬁcation of a transparency scheme for AI systems.
2.2 Transparency in practice today
The General Data Protection Regulation (GDPR(7)) was adopted in 2016 by
the European Union and the European Economic Area. It is to be actively
Springer Nature 2021 LATEX template
Signs for Ethical AI 7
regulated since May 2018. GDPR regulates transparency and personal data
and recognizes the new rights of citizens. These include the right of access
(knowing which data of you has been stored) and the right to data erasure, also
known as the right to be forgotten (having your personal data deleted under
certain circumstances). Since these considerations have been globally overseen
so far, the implementation of GDPR in all its scope represents a daunting task.
As a reaction to GDPR, the Interactive Advertising Bureau (IAB) devel-
oped a uniﬁed implementation framework, intending to provide a standard for
all ad industry. The IAB is an organization of over 600 companies directly or
indirectly dedicated to online advertising and data gathering, mostly from Eu-
rope and the United States. It includes major technological companies, such as
Amazon, Facebook, Google, IBM or Uber. The implementation proposed by
the IAB is known as the Transparency and Consent Framework (TCF (15)),
with version 1.0 being released on April 2018. After this was found insuﬃ-
cient to cover several aspects of GDPR (32), TCF 2.0 was released in August
2019. A public repository of TCF 2.0 is available1 for the industry to inte-
grate with it. To the best of our knowledge, no oﬃcial statement has been
made yet regarding its GDPR compliance, but motivated concerns have been
expressed(19).
The scientiﬁc community has analyzed the shortcomings of the current
practice of user consent and transparency. Recently, (20) gathered data from
theﬁvemostpopularprovidersofconsentformsintheUK,andfoundthatonly
11.8% met the GDPR requirements. The concerns regarding TCF were also
voiced by the UK Information Commissioner’s Oﬃce (ICO) in June 2019. In
its report (32), the ICO states that"privacy information provided often lacks
clarity and does not give individuals an appropriate picture of what happens to
their data. While we recognise that provision of this information in the online
environment can be challenging, this does not mean that participants can ignore
the requirements of PECR (‘clear and comprehensive information’) and the
GDPR.". The Privacy and Electronic Communications Regulations, or PECR,
is a European Commission directive, approved in 2003, which complements
GDPR. Among other things, it speciﬁes that information provided regarding
datacollectionmeansanddatausesmustbeexplainedclearlytothepublic(6).
Clarity is diﬃcult to measure. Nonetheless, we consider that current im-
plementations of GDPR through TCF 2.0 areclearly obscure for three main
reasons. First, language remains too technical and inaccessible, for example,
built on the understanding of technical concepts likecookies. Communication
at its simplest must not and cannot include technical terminology. Secondly,
the detail of current TCF implementations does not provide clear informa-
tion to the spectrum of public demand. A hierarchy of information needs to
be established to serve all, from the least to the most meticulous users. Third
and last, the integration of the consent form into user displays is ineﬀective,
and frequently, counterproductive. Forms today are mostly based on pop-ups,
1https://github.com/InteractiveAdvertisingBureau/GDPR-Transparency-and-Consent-
Framework/blob/master/TCFv2/TCF-Implementation-Guidelines.md
Springer Nature 2021 LATEX template
8 Signs for Ethical AI
intrusive and perturbing, which promotes their immediate dismissal. Infor-
mation regarding transparency should be naturally integrated into interfaces,
being minimally intrusive and always visible. All these ﬂaws make current
implementation ineﬀective in practice (1; 20).
So far, we have discussed the state of data transparency in practice, but
we have not introduced the context of AI transparency. Unfortunately, beyond
whathasbeenregulatedbyGDPR,AItransparencyinpracticeisnon-existent.
A few organization promote it, like the AI Transparency Institute, but has no
practical adoption. As of today, people are unable to know the algorithms and
data fueling the AI systems that interact with them. Moreover, what is more,
people are unable to know of the mere existence of AI systems interacting
with them. To ﬁx this, in this paper, we propose an AI transparency scheme.
However, before that, let us clarify some terminology.
3 TERMINOLOGY
Throughout the speciﬁcation of the proposed transparency scheme, in the fol-
lowing section, we frequently refer to the concepts of system, AI service and
purpose. Given the importance of these terms for the contextualization of the
proposal, we detail the interpretation used in this work.
In the context of this paper, asystem is a computational entity with a
graphical user interface that enable users to interact with it. Web pages and
device applications are popular examples of a system under this interpretation.
A system which contains one or more AI services is an AI system.
In contrast an, AI service is a computational mechanism that uses AI
technologywhileinteractingwithusersand/ortheirdataforadeﬁnitepurpose.
AI technology includes knowledge representation methods, machine learning,
statistical learning, data mining, data analysis, analytics and other related
ﬁelds. The consumer of the service can be a user, the system containing the
service, or a third party. A service is an AI service even if AI only plays
a secondary role in it. Frequently, diﬀerent AI services performing diﬀerent
speciﬁc tasks are combined to provide high level functionalities. Nonetheless,
this does not alter the granularity of the AI service deﬁnition. An AI service
is deﬁned by its purpose, not by how its used.
3.1 Purpose
An eﬀective deﬁnition of purpose is essential for implementing transparency
and consent. Purpose states what will the user receive in exchange for its con-
sent, making it the main driver behind the acceptance or rejection of access
and use rights. The deﬁnition of purpose under GDPR was reﬁned in (22). Fol-
lowing this adopted opinion, the purpose is to be speciﬁed without vagueness
or ambiguity as to its meaning or intent, in such a way so as to be understood
in the same way by everyone, including the private data owners. This means
putting users at the centre of purpose deﬁnition.
Springer Nature 2021 LATEX template
Signs for Ethical AI 9
The industry still has to adopt this deﬁnition of purpose. This delay or
resistance generates requests of enforcement from society (35), which antici-
pates changes ahead. As of now, let us consider the purposes deﬁned by TCF
2.0 (15) as a starting point. From a users’ perspective, some of these purposes
are excessively detailed, while others are insuﬃciently detailed. For practical
reasons, we aggregate them as follows:
• Access device storage and/or data
– TCF Purpose 1: Store and/or access information on a device
• Ad selection or evaluation
– TCF Purpose 2: Select basic ads
– TCF Purpose 3: Create a personalised ads proﬁle
– TCF Purpose 4: Select personalised ads
– TCF Purpose 7: Measure ad performance
• Content selection, creation and/or evaluation
– TCF Purpose 5: Create a personalised content proﬁle
– TCF Purpose 6: Select personalised content
– TCF Purpose 8: Measure content performance
• Market research
– TCF Purpose 9: Apply market research to generate audience insights
• Other internal uses
– TCF Purpose 10: Develop and improve products
We consider the last (TCF Purpose 10) to be non-GDPR compliant, as it is
vague and ambiguous (what product? to which end?). However, this could be
ﬁxed by further specifying purposes. TFC purposes 5 to 8 are also too vague
when considering that is the counter-part for the user (details of the service
being oﬀered as a result of lending personal data), and thus, key in the consent
decision. In this context, our transparency scheme proposal assumes a level of
speciﬁcity similar to the one used in the following examples:
• Route planning
• Product recommendation
• Language translation
• Image generation
• Conversational agents
This paper uses a list of purposes aggregating TCF purposes 1, 2 and 4,
and adding a list of speciﬁc contents and services for purpose 3, as exempliﬁed
above. Nonetheless, the proposal of a complete list of purposes is out of the
scope of this work.
Springer Nature 2021 LATEX template
10 Signs for Ethical AI
4 AI TRANSPARENCY SCHEME
An informed society requires the most eﬀort from society itself, both in educa-
tion (individuals must get familiarised with new concepts) and accountability
(individuals are forced to handle added responsibilities). The AI community is
an expert in the ﬁeld and can support this eﬀort by devising communication
mechanisms which target all of society, tackle all the main issues, and do it
with adaptable levels of detail.
With these goals in mind, we deﬁne a transparency scheme for systems
with AI services. The scheme has two columns and three levels. The columns,
cover the two main sources of ethical issues:Data Privacy (Figure 1) andAI
Transparency (Figure 2). The three levels provide an increasing amount of
detail.
The ﬁrst level is the coarsest level of transparency for both columns. It pro-
vides the information needed to empower users to a minimal level of autonomy.
We use visual signs because these simple representations can convey complex
concepts in a quick and non-intrusive manner. This capability is proved daily
in domains like mobility, emergency management, law enforcement or user in-
teraction. In fact, icons have previously been consider to illustrate data privacy
information (23). We deﬁne a set of visual signs for each column separately.
The second level of transparency must provide more details and more ﬁne-
graineddecisionspace.Personalizedchoicesbasedonmultiplepreferencesmust
be enabled. For this purpose, we use factsheets, which have been proven eﬀec-
tive at gathering informed decisions (33). Through factsheets, we summarize
the characteristics of each service and enable decisions made on a case-by-case
basis.
Thethirdandlastleveloftransparencycontainsthedetailsavailable,which
should enable aminimal ethical evaluation for guiding user interaction. Either
column contains a diﬀerent list of public details made available to the user.
4.1 Data Privacy
Many AI systems in use today are data-hungry. Machine learning, the most
popular branch of AI, is based on the premise of data. And the more data it
can get, the better it may perform. At the same time, what generates the most
data in the world today is society - billions of people acting and interacting
digitally in a globalised world. The popularisation of AI systems feeding on
personal data was unavoidable.
WhileAIprovidesmanyvaluedservices,currentlypeopleareoftenunaware
(and uninformed) of the fact that an AI system is feeding on their data, and the
possibleimplicationswithregardstotheirprivacy.Asituationwhichisbyitself
unethical. To advance towards an ethical use of personal data by AI systems,
it is necessary to inform users that information may be recorded, stored and
further exploited. The speciﬁcs on which information is to be provided for data
privacy has already been legislated upon through GDPR, and will guide the
design of the data privacy pillar of the proposed scheme. On the other hand,
Springer Nature 2021 LATEX template
Signs for Ethical AI 11
there is no legislation for AI transparency, the other proposed pillar, which
will entail a less contextualized proposal.
4.1.1 Visual signs
As the ﬁrst level of information, one that is to be always visible, we use a
feature that can enable the most basic users’ policies and decisions. Since we
are in the context of a user interacting with an AI system, this feature is
(related with) the use of private data within the system, our (or) outside of
it. Gathering and using private data generated by a service for improving that
service has speciﬁc ethical implications. Doing it to feed a diﬀerent service, has
others. Thus, for personal data and privacy, we propose three diﬀerent signs,
where one and only one always holds for each user-based AI system:
• Personal data not gathered No active or passive information associ-
ated to the user is recorded or disseminated by the system. The system
may store information about its own use, but if it does so, it is in an
anonymised manner, not linking interactions with users. In this setting, it
is impossible to map together two otherwise independent interactions gen-
erated by the same user. This situation is illustrated with a closed lock.
Example: A recommender system of an online shop, may
store which items are most frequently browsed, when
and how. However, it does not store information regard-
ing which items were previously seen or bought by the
same user. This behaviour includes not gathering personal
details like geographic location, previous activity, access
details, etc.
• Personal data is stored and/or used in this system: The system
may be collecting information from the user. The collected information
may only be used by the system in which it was produced, and it is never
distributed outside of it. This setting is illustrated with an open lock.
Example: An email client learns the writing style of a user
by processing her sent emails. This behaviour allows an
AI service to learnhow to propose automatic responses,
and another one to make grammar suggestions. The user
emails, or any derived or learnt representation of these, is
never accessed by a diﬀerent system or third party. In this
example, the use of the email data by a diﬀerent system
to provide targeted ads would be forbidden.
• Personal data may be stored, exploited, and distributed to third
parties: The system is collecting the user’s information. This data could
be used for services outside of the system, and also be distributed to third
Springer Nature 2021 LATEX template
12 Signs for Ethical AI
Table 1 Details provided by services accessing personal data. Guideline for the factsheet
at the second level of Data Privacy.
Detail Category Possible values
Which personal data? Data types location, images, navigation,
use statistics
For which purpose? Purposes personalized ads, language
translation, market research,
route planner,etc.
For how long? Range of periods less than a day, less than a
month, less than a year,
a year or more
Who has access to it? Entities company A, government B,
conglomerate C
parties. This setting is illustrated with an open lock from which data ﬂows.
Example: A video streaming platform stores the history
of watched videos by users, linking the data to their pro-
ﬁles. The platform shares this information with a music
streaming service, which then uses it for feeding a music
recommender system.
4.1.2 Data Privacy Factsheet
The second level of Data Privacy contains a factsheet, listing all services that
request access to personal data. Row by row, services declare what personal
data is needed, for what, for how long, and who will be accessing it. Table 1
provides more details on the information reported by services, together with
examples.
With this information, users can grant or deny access, taking into account
the particularities of each case. To facilitate interaction, with the system, the
consents of data services that serve a common and inter-dependable purpose
may be aggregated for request/grant. An example of a factsheet is shown in
Figure3.Thisdesigndisplaysallminimalinformationandallowsuserstomake
quick, service-wise decisions. In compliance with explicit consent, all options
should be disabled by default.
4.1.3 Full detail: Personal Data
GDPR again inspires the full detail section of the display regarding personal
data. In Article 15, this regulation speciﬁes that individuals (also known as
data subjects) have the right to access their personal data. This is known as
the subject or subjective access. This connection would ideally be instanta-
neous so that people know the status of their privacy at all times. For this
purpose, we consider a request form at this level, with additional security mea-
sures. According to GDPR, services have a maximum of one month to satisfy
data requests, and in most cases fees cannot be charged to process them. We
Springer Nature 2021 LATEX template
Signs for Ethical AI 13
consider this time frame should be reduced, eventually reaching the level of
seconds.
The request form manages users’ access to their personal data, and it con-
tains an option to request all personal data stored. It also contains ﬁlters
to access data based on the categories of the second level factsheets (data
type, purposes, etc. ). Beyond the request form, at this level, we propose a
dashboard. Since this is a topic of research on its own right (2), only certain
charactersitics of it will be discussed here. Particularly, the fact that once per-
sonal data is made accessible to its owner, the dashboard must enable them to
handle it, as well as their related rights. The functionalities of this dashboard
should include:
• Browsing the private data stored by the system;
• Modifying the restrictions to be applied to the storage and processing (i.e.,
opting in or out of some cases);
• Access to details on the source of the data, mainly if this was not obtained
directly from the user;
• Specifying rectiﬁcations on the data;
• Demanding the erasure of some or all of personal data stored, and
• Issuing a legal complain with a supervisory authority
Although we do not propose a speciﬁc display for this level here, we
anticipate this would have to be a full-screen device.
4.2 AI Transparency
AI is typically guided by an algorithm, a model, or both. Algorithms deﬁne
AI behaviour and are represented through code. Models deﬁne the context in
Figure 3 Example of a factsheet for Data Privacy. Each row is a service requesting access
to personal data.
Springer Nature 2021 LATEX template
14 Signs for Ethical AI
which the AI operates, and can be represented by data and/or code. If we do
not know the algorithm, we cannot know what is the AI doing. If we know the
algorithm, but we do not know the model, we can verify the AI behaviour but
not its purpose. Any sort ofbias could be encoded within the AI through a
model.
For a comprehensive evaluation of an AI system, both code (i.e., algo-
rithms and models) and data (i.e., models) are needed. This is ideal from a
transparency point of view, but it may not always be desirable for the sake
of privacy. Sometimes hiding a model provides better security, and sometimes
an algorithm is simply private. One way or the other, users must always have
the right to know the degree of transparency of every AI system they interact
with so that they can take that into account when deciding how to use them,
or if using them at all.
A diﬀerent transparency requirement is related to the results produced by
an AI system, instead of the AI system itself. Furthermore, that is objectiv-
ity or subjectivity of the responses with regards to the user identity. With
subjective AI, society must be particularly watchful for traces of manipulative
or misguided behaviour, including the promotion or existence of ﬁlter bub-
bles, echo-chambers, partisanship and propaganda. Within subjective AI, we
include all possible types of personal bias, also those naturally hidden within
data and not under human control. For this reason, objective AI can only be
guaranteed by forbidding AI algorithms and models to access personal data.
4.2.1 Visual signs
For AI transparency, we propose two visual signs. One for code and data
transparencyandoneforobjectivity.Theﬁrstincludesarepresentationofboth
code and data, and their availability. Data is represented through a cylinder (or
database) with the text01 written within. Code is represented by a rectangle
(or screen) with the text<Section etminus>. Variants of the sign are generated
by changing the colour or the visibility of both components. We introduce
three cases that we consider cover the majority of practical cases:
• Open AI services: The source code of all AI algorithms and models run-
ning in the system are public to the user. All data used for ﬁtting and
deploying these algorithms and models are public to the user. This openness
includes code, documentation, data and metadata. This setting is illustrated
with a white box of data feeding a white box computer.
Example: A word embedding model used for suggest-
ing results to queries, has the following data available
to the user: Trained model, training code for the
model, data used for training the model and descrip-
tion of the data used when running it. This is the only
case where the existence ofbias in the system can be
audited.

Springer Nature 2021 LATEX template
Signs for Ethical AI 15
• Public AI services: The code of all AI algorithms and models running in
the system are public to the user. This includes source code and documen-
tation. However, the data used to ﬁt or run one or more of these algorithms
and models is not available to the user. Thus, its behaviour is not fully au-
ditable. This setting is illustrated with a black box of data feeding a white
box computer.
Example: A service for image manipulation fueled by
a GAN. The source code of the GAN is available, but
the data used to train the model it is not. The service
is not open because the existence of bias can not be
veriﬁed.
• Opaque AI services: The source code of one or more AI algorithms or
models running in the system is not available. This setting is illustrated with
a black box of data feeding a black box computer.
Example: A social network suggests (new) contacts
and content for users to follow. However, the code and
the data powering such service is not available for the
users. The motivations and mechanisms driving the
recommendations are unknown; the system is opaque.
The second visual sign of AI transparency regards the objectivity or sub-
jectivity of the responses provided by AI services. This sign should always be
visible together with the previous one. To quickly and clearly convey the idea
of objectivity, we propose a pair of complementary signs where only one holds
for each AI system:
• Indistinct information: The information provided by the system is inde-
pendent of the identity and behaviour of the user. Any other user producing
the same explicit input would receive the same output. User data is inacces-
sible to the computation. This setting is illustrated with a round information
sign.
Example: A search engine produces results to users queries.
These results are retrieved using only the query terms, and
not using or considering any user-speciﬁc information (e.g.,
location, history, device,etc. .
• Personalised information: The information provided by the system is
or may be subjective with regards to the user identity or behaviour. Any
access to personal data by the system enables this scenario. This setting is
illustrated with a target sign.
Example: A video streaming platform oﬀers a variable set
of contents to its users. When deciding which content be-
comes available to each user, the streaming history and
proﬁle are taken into account. The system is providing
personalised information, and bias may exist.

Springer Nature 2021 LATEX template
16 Signs for Ethical AI
4.2.2 AI Transparency Factsheet
The factsheet at the second level of AI transparency contains a list of all AI
services running in the system. This list may contain entries also found in the
Data Privacy factsheet and aggregations of those (a single AI service may re-
quest access to several data sources). For each AI service, the AI Transparency
factsheet speciﬁes its purpose (only one, as speciﬁc as possible) and the per-
sonal data types it needs for running (none, one or more). It also displays its
own speciﬁc visual signs with regards to Data Privacy (personal data han-
dling) and AI Transparency (openness of code/data, and objectivity). Figure
4 shows an example of this factsheet.
The combination of all visual signs in the second level factsheet deﬁnes
the ﬁrst level system-wide signs for AI Transparency. This corresponds to the
most restrictive set of each of three signs.e.g., a system is subjective if a single
service in it is subjective. To facilitate navigability, this factsheet may link to
several other components of the scheme, like the Data Privacy factsheet, the
data request form and the dashboard. But most prominently, to the full detail
section AI Data and Code, detailed next.
4.2.3 Full detail: AI Data and Code
For each AI service in the system with either public code, open data, or both,
the full detail level provides an interface to it. In the case of source code,
it includes minimal documentation as well. In the case of data, it includes
anonymized pre-training (if any) and training data, together with metadata
describing the nature and structure of the data (e.g., source, description of
attributes). All these full details must be provided for those AI services that
are claimed to be open or public in the corresponding second-level factsheet.
We expect AI applications on critical domains (e.g., healthcare, education) to
reach this level of transparency.
5 VISUAL SIGNS IN ACTION
The eﬃciency of a transparency scheme is mostly deﬁned by the way it is
implemented and integrated with user interfaces. If the integration is ﬂawed
Figure 4 Example of the factsheet for AI Transparency. Each row is an AI service of the
system.
Springer Nature 2021 LATEX template
Signs for Ethical AI 17
(e.g., intrusive or imperceptible) or it is ill-intentioned (e.g., misleading or ma-
nipulative), the transparency eﬀort will be undermined (20). To avoid those
side-eﬀects, the transparency scheme is to be integrated into the system by de-
sign, always visible at some level, and occasionally occupying the main display.
Considering the current trends in AI systems, we advocate for integrating the
transparencyschemewithinbrowsers(forwebapplications),operatingsystems
(for client applications) and APIs. The visual signs proposed were designed
to be interpretable even when shown at a small scale (i.e., the size of an icon
in a browser bar). To illustrate this, some ﬁgures in this paper are purposely
plotted small.
According to GDPR Article 6 on the lawfulness of processing, the inter-
action between users and the transparency scheme is to be ruled byexplicit
consent. This is indeed one of the main pillars of personal data rights. From the
moment a user connects or makes the ﬁrst request to an AI system, personal
data is exposed, and user-AI interaction becomes possible. To inform users of
this possibility beforehand so that explicit consent can be granted, the trans-
parency scheme is to be shown on the main display when a user ﬁrst connects
to an AI system. Meanwhile, the AI system remains waiting in the background,
invisible and unable to access any personal data until explicit consent is given.
As an example, let us consider a web page which includes several AI ser-
vices. Only one of these services runs on the landing page. This AI service is
an open-source, rule-based system that adapts the content of the front page
to the user location and device. When a user connects to the front page, only
the location and no further personal data is gathered. In such a system, when
a user connects to the front page for the ﬁrst time, before any content of the
system is shown or any data is gathered, the user is prompted with the icons
shown in Figure 5.
Figure 5 Example of visual display for an AI system which uses personal data to provide
targeted content, while having both data and models openly available.
From this view, the user can directly grant or deny consent. In the ﬁrst case,
it will proceed to the front page, location will be gathered, and personalized
information will be provided. In the second case (deny), the AI service may
provide a version of it without the denied functionalities, or it can reject to
serve the user.
To keep users engaged with the transparency scheme, the ﬁrst level of
visual signs is to be always on sight. This is a reminder of the rights granted at
that moment, and the applying terms to any ongoing interaction. To minimize
interference, the signs should be displayed small (e.g., the size of a browser bar
button). These signs also provide direct access to the complete transparency
scheme at any time.
Springer Nature 2021 LATEX template
18 Signs for Ethical AI
An AI-based system that is not currently running any data gathering or AI
services concerning the user may not require explicit consent. Nonetheless, it
still needs to be notiﬁed. If this is the case, the visual signs shown will be those
of Figure 6: No personal data is gathered, and all interactions are indistinct of
the user.
Figure 6 Example of visual display for a system with no personal data gathering or use,
containing no AI component, and having an objective behaviour.
Ifatsomepoint,theconditionschange(thesystemstartsaccessingpersonal
data or running AI-based services), this should be preemptively notiﬁed to the
user (following the example of Figure 5). This display illustrates the changes in
the conditions, and enable the behaviours deﬁned above (grant, deny, inspect
& reﬁne). It is important to observe that explicit consent requires that all
changes of conditions will be notiﬁed: a user who has consented to personalized
content for a set of services, is to be notiﬁed if a new service with personalized
content wants to be activated. Notice however that explicit consent does not
need to be given twice for the same service.
In practice, there are some combinations of visual signs that are not pos-
sible. The Indistinct information icon requires either thePersonal data not
gathered icon, or theOpen AI servicesicon. Otherwise the objectivity of the
system could not be guaranteed.
5.1 Visual Signs Today
To assess the current transparency in the context of our proposal, we conduct
an analysis on some of the most popular websites worldwide, ﬁnding which
set of visual signs would apply to them. This study is made based on a review
of their data privacy and cookies consent forms conducted between November
2021 and January 2022. When information found is incomplete or not speciﬁc
enough, the most restrictive policy was applied. Table 2 shows the resulting
correspondence.
Current legislation on data privacy (e.g., GDPR) has increased trans-
parency on personal data. As shown in Table 2, while the majority of services
gather and disclose personal information, others are taking a more restrictive
approach, maintaining a complete anonymity and privacy of users (ﬁrst col-
umn of signs). This is most common in sites related with the open source
movement, who also provide objective access to some of their functionalities
(third column). There is one case,whatsapp were conditions did not specify
the sharing of personal data with third parties. This is most likely caused by
the lack of ads in their website, which is responsible for the majority of data
privacy transactions.
Springer Nature 2021 LATEX template
Signs for Ethical AI 19
Table 2 Visual signs corresponding to some of the top worldwide web pages, all of
which include AI. Based on a review of their consent forms done during November, 2021.
URL Applicable Visual Signs
www.google.com
www.facebook.com
www.youtube.com
www.instagram.com
www.twitter.com
www.amazon.com
www.netﬂix.com
www.reddit.com
www.tiktok.com
www.discord.com
www.twitch.tv
www.fandom.com
www.accuweather.com
www.whatsapp.com
www.wikipedia.org
www.duckduckgo.com
www.github.com
www.wordpress.org
www.openstreetmap.org
On the other hand, the lack of regulation regarding transparency in AI
methods has resulted in generalized opacity regarding AI-based services. This
is shown in the second column of Table 2, where all reviewed sites get assigned
the least transparent labeling. Even open source sites, which typically open
their frontend but not their backend (where AI services run) fall short in this
category. Let us remark that some sites, likewikipedia, provide the models and
data used to trainsome of their AI services in an exercise of transparency.
However, since this is not complete (some AI services remain under-speciﬁed)
these sites still get assigned the opaque AI services icon. Notice we assigned
Springer Nature 2021 LATEX template
20 Signs for Ethical AI
the AI opaque icon to all services, even when we could not conﬁrm their use
of AI tech. Preventively, this was assumed by default.
5.2 Domains of Application
The proposed visual scheme is compatible with AI services running in a
wide variety of domains. Each domain must implement certain interaction
mechanisms to guarantee the transparency principles, although how are these
speciﬁcally implemented can vary signiﬁcantly, as we will see next. The three
main interactions we consider are:
• Granting/revoking data consents: whenever applicable, the user should
always have easy access to update data consents.
• Requesting models or code: whenever the AI system claims to have an open
model or code, the user should have easy access to instantly download them.
• Requesting auditing traces: at all times, the user should have easy access
to instantly download the full trace of the use of their data inside the AI
system, including data being shared to third parties.
Depending on the speciﬁc medium with which the user is using the AI
system, we can distinguish several possible channels for interaction.
5.2.1 Frontend UIs
These include mainly web and desktop applications. One possible mode of
interaction is the use of banners ﬂoating at the top or the bottom of the UI
(user interface). The main advantage for using banners is that users are already
used to reading and interacting with this kind of visual component, given their
application to cookie management.
We recommend that the UI is designed in a way such that this type of
component is fully integrated into the interface, especially for the visual signs
which are designed to be compact. For example, the component could be set in
a speciﬁc place common to all or most views of the application such as the top
right corner. On one hand, this would state that the intentions of the owners
of the AI system are to be transparent about the usage of the user’s data. On
the other hand, this would serve as a permanent reminder for the user about
this usage.
Transparency, by deﬁnition, has to apply to all users regardless of age,
cultural background or physical or psychological conditions. We propose com-
bining the design requirements we propose with those applicable requirements
speciﬁed in Universal Design (17; 29) that may apply. For example, account-
ing for blindness or color blindness by enabling speech-to-
```
