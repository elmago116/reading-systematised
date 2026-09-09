---
title: "Enacting Responsible AI: A Configurational Analysis of AI Principles in Practice"
author: Pouria Akbarighatar, Ilias O. Pappas, Sandeep Purao, Polyxeni Vassilakopoulou
year: "2025"
Type: Article
DOI: 10.1007/s10796-025-10618-x
source: https://doi.org/10.1007/s10796-025-10618-x
created: 2026-04-24
description: Abstract Responsible AI (RAI) entails developing, using, and governing AI in a human-centred way to ensure its trustworthiness and alignment with human values. Organizations attempt to enact RAI through guiding principles that aim to minimize threats such as bias and privacy violat
tags:
  - op/acc/pending-review
  - Tech/AI
  - themes/ethics
  - design/UCD
pdfORepub: "[[Enacting Responsible AI A Configurational Analysis of AI Principles in Practice.pdf]]"
---
[[Enacting Responsible AI A Configurational Analysis of AI Principles in Practice.pdf]]

> **Abstract:** Abstract
                  Responsible AI (RAI) entails developing, using, and governing AI in a human-centred way to ensure its trustworthiness and alignment with human values. Organizations attempt to enact RAI through guiding principles that aim to minimize threats such as bias and privacy violations and enhance outcomes such as transparency and fairness. In the empirical study we report in this paper, we share insights about how AI experts view RAI principles, including relationships among them, these principles, and the enactment of RAI principles. Employing a sequential mixed-methods approach, we analyse survey data from 135 AI experts from Europe and America using fuzzy-set Qualitative Comparative Analysis (fsQCA), complemented by follow-up interviews. Our analysis identifies five equifinal combinations of RAI principles associated with high overall RAI enactment. The findings reveal the crucial role of accountability and safety-reliability principles and highlight the contextual variability of other principles. This research contributes a nuanced understanding of RAI enactment, moving beyond individual principles to demonstrate their complex interplay and their contextual dependencies in achieving responsible AI practices.
## Full text (extracted from `Enacting Responsible AI A Configurational Analysis of AI Principles in Practice.pdf`)

*Source:* `2PDF/Enacting Responsible AI A Configurational Analysis of AI Principles in Practice.pdf`  
*Extracted:* 2026-04-24

```text
Vol.:(0123456789)
Information Systems Frontiers (2025) 28:61–87 
https://doi.org/10.1007/s10796-025-10618-x
Enacting Responsible AI: A Configurational Analysis of AI Principles 
in Practice
Pouria Akbarighatar1  · Ilias O. Pappas1,2  · Sandeep Purao1,3  · Polyxeni Vassilakopoulou1 
Accepted: 22 May 2025 / Published online: 23 June 2025 
© The Author(s) 2025
Abstract
Responsible AI (RAI) entails developing, using, and governing AI in a human-centred way to ensure its trustworthiness 
and alignment with human values. Organizations attempt to enact RAI through guiding principles that aim to minimize 
threats such as bias and privacy violations and enhance outcomes such as transparency and fairness. In the empirical study 
we report in this paper, we share insights about how AI experts view RAI principles, including relationships among them, 
these principles, and the enactment of RAI principles. Employing a sequential mixed-methods approach, we analyse survey 
data from 135 AI experts from Europe and America using fuzzy-set Qualitative Comparative Analysis (fsQCA), comple-
mented by follow-up interviews. Our analysis identifies five equifinal combinations of RAI principles associated with high 
overall RAI enactment. The findings reveal the crucial role of accountability and safety-reliability principles and highlight 
the contextual variability of other principles. This research contributes a nuanced understanding of RAI enactment, mov -
ing beyond individual principles to demonstrate their complex interplay and their contextual dependencies in achieving 
responsible AI practices.
Keywords Responsible AI · Enactment · FsQCA · Benevolence · Safety · Privacy · Security · Accountability · 
Explainability · Transparency · Inclusiveness · Fairness
1 Introduction
Across organisations and industries, Artificial Intelligence 
(AI) initiatives continue to grow in scale and importance. 
AI is used to diagnose and treat diseases, combat fraud, 
optimize crop yields, and more (Amugongo et al., 2023; 
Ho et al., 2019; Wall, 2018). Organisations that roll out AI 
initiatives are, however, also aware of risks such as bias, 
privacy violations, and unintended consequences (Fuma-
galli et al., 2022; Mateen, 2018; Rinta-Kahila et al., 2022). 
Responsible AI (RAI) aims to address these risks by promot-
ing the development, use, and governance of AI in alignment 
with human values (Vassilakopoulou et al., 2022). Through 
RAI, organisations can harness AI’s benefits while mitigat-
ing its risks, fostering the ethical and responsible design and 
use of AI-infused technologies.
Scholars and practitioners suggest defining RAI through 
mechanisms such as guidelines and principles (Mikalef 
et al., 2022). These guidelines and principles often address 
aspects like fairness, transparency, accountability, privacy, 
and safety, to tackle issues related to potential AI threats to 
both individuals and to society as a whole. They provide 
actionable guidance and norms for AI that will be “good” for 
those it affects (Papagiannidis et al., 2025). However, these 
guidelines and principles are often presented as disjointed 
elements and implemented in a piecemeal manner (Munn, 
2023). Enacting RAI with such guidelines and principles, 
therefore, requires a shift in thinking from individual prin-
ciples to a more holistic approach. Pursuing this shift can be 
 * Pouria Akbarighatar 
 Pouriaa@uia.no
 Ilias O. Pappas 
 ilias.pappas@uia.no; ilpappas@ntnu.no
 Sandeep Purao 
 spurao@bentley.edu
 Polyxeni Vassilakopoulou 
 polyxenv@uia.no
1 Department of Information Systems, University of Agder, 
Universitetsveien 25, 4604 Kristiansand, Norway
2 Department of Computer Science, Norwegian University 
of Science and Technology, Trondheim, Norway
3 Department of Computer Information Systems, Bentley 
University, Waltham, MA, USA

62 Information Systems Frontiers (2025) 28:61–87
challenging because of the abstract nature of RAI principles 
and the difficulty of reconciling them amidst competing val-
ues, trade-offs, and contextual constraints in practical AI 
deployment (Munn, 2023, Sadek et al., 2024). Further, these 
principles, rooted in risk mitigation, often lack a theoreti-
cal grounding. Effective RAI enactment, thus, requires the 
enactment of multiple RAI principles and examining their 
interconnected impact instead of considering each principle 
separately.
Enactment is both the process of making ideas real by 
acting upon them and the outcome of this process (Czar -
niawska, 2005). Weick (2000) explains enactment in terms 
of how organizations construct their realities. Enactment 
is inherently situated so that even when a universal struc-
ture is being enacted, it has to be particularized to some 
extent (Orlikowski & Yates, 1999). Ribes & Finholt (2009) 
conceptualized enactment, acknowledging gaps between 
today’s planning and tomorrow’s actuality. The concept 
of enactment emphasizes that actors shape what is actual-
ized rather than merely responding to guidelines. Drawing 
on this stream of research, this study examines RAI enact -
ment, aiming to fill a significant gap. While some studies 
have examined individual RAI principles, like fairness and 
transparency, limited research addresses how they are com-
bined to enact RAI in practice (Ghasemaghaei & Kordzadeh, 
2024; Watson & Nations, 2019). We designed an empirical 
study investigating RAI enactment through three aspects: 
practitioner perceptions of RAI importance, alignment of AI 
initiatives with RAI, and RAI implementation.
Understanding RAI enactment contributes to academic 
discourse as well as practitioner understanding of RAI 
principles (Mittelstadt, 2019 ), pointing to more respon -
sible AI practices. Our work is theoretically grounded in 
Rawls'political theory of justice (Rawls, 2001), which can 
be used as a coherent framework for governing major soci-
etal constituents, such as AI technologies (Gabriel, 2022). 
Rawls'emphasis on fair distribution of benefits and bur -
dens informs our investigation into how different combina-
tions of RAI principles enable RAI enactment in practice. 
Specifically, we address the following research question: 
Which configurations of RAI principles are related to RAI 
enactment?
To answer this question, our research method consisted 
of primary data collection from expert practitioners. Specifi-
cally, we collected data from 135 practitioners with signifi-
cant experience in AI and analysed the answers using fuzzy-
set qualitative comparative analysis (fsQCA) (Ragin, 2008; 
Pappas et al., 2016), during the analysis, we did not focus on 
individual principles. Instead, we adopted a configurational 
perspective to explore how the enactment of RAI princi -
ples is combined to pursue the outcomes of interest. This 
approach, based on conjunctural causation (Slager et al., 
2021), equifinality (Katz & Kahn, 1978), and asymmetrical 
causation (Misangyi et al., 2017), highlights that RAI enact-
ment results from multiple principles, can emerge through 
different configurations, and involves distinct factors driv -
ing its presence or absence. Follow-up interviews added to 
the fsQCA findings to develop a nuanced understanding of 
the and gain deeper insight into identified configurations. 
The theoretical anchor for our work (Rawls, 2001) made it 
possible for us to specify the outcomes that would allow a 
more comprehensive understanding of how AI risks can be 
responsibly mitigated.
The key contribution of the work is the identification of 
five equifinal combinations of RAI principles associated 
with high levels of effectiveness for RAI enactment. The 
findings reveal the crucial role of accountability and safety-
reliability principles while acknowledging the contextual 
variability of other principles in counterfactual cases. These 
insights contribute a nuanced understanding of RAI enact-
ment, moving beyond individual principles to demonstrate 
their complex interplay and their contextual dependencies 
in achieving responsible AI practices.
The remainder of this article is organized as follows: 
Sect.  2 reviews related literature, Sect.  3 presents the 
research method, and Sect.  4 presents the results. The dis-
cussion is presented in Sect. 5, followed by the conclusions 
in Sect. 6.
2  Related Literature
2.1  Justice as Fairness: Theoretical Framing for RAI
Rawls'"justice as fairness"is a theoretical conceptualization 
to address the problem of social justice and opportunity dis-
tribution (Gabriel, 2022; Rawls, 2001). It was developed 
as a prescriptive framework for arriving at moral rules or 
principles (Hoffmann, 2017). Rawls foregrounds liberty and 
equality as key tenets in his framework. Liberty is the first 
and most vital tenet, meaning everyone must have some key 
rights as fundamental freedoms (Rawls, 1999, p. 53). For 
example, education, health, and personal property constitute 
fundamental and inviolable freedoms and rights as part of 
the tenet of liberty. The second key tenet is Equality, subdi-
vided into two conditions: (a) the fair equality of opportu-
nity means that social/economic arrangements must allow 
fair opportunity of access to liberties (access to options as a 
‘right’ and an ‘effective’ equal opportunity); (b) the differ -
ences principle, which regulates the distribution of advan-
tages across the members of society and suggests that ine-
qualities in benefits or obligations are permitted when they 
aim to bridge the gap with the least advantaged members of 
society (Rawls, 1999, p. 53). Liberty precedes equality, i.e., 
mechanisms must first secure basic liberties before pursu-
ing equality.

63Information Systems Frontiers (2025) 28:61–87 
Rawls´ work is not specific about technology; however, it 
has implications for technologies with pervasive impacts on 
people´s lives, such as AI (Gabriel, 2022). From a Rawlsian 
perspective, social justice entails fair access to resources, 
which involves designing institutions and systems that guar-
antee equal access (Baygi et al., 2024). Scholars have applied 
Rawls'concepts in the context of information technologies 
and AI (Ashrafian, 2023; Hoffmann, 2017; Leben, 2017). 
When impactful technologies including AI get integrated 
into societies that aim for social justice, they need to be com-
patible and supportive to liberty and equality. A key reason 
making this lens attractive for theoretical framing RAI is its 
compatibility with different sociocultural contexts. Rawls 
formulated the theory of justice with the goal of making 
it justifiable to individuals with diverse beliefs and philo-
sophical perspectives. However, it should be noted that as 
a political theory, it requires political power to be exercised 
legitimately; hence, it is more suited for democratic socie-
ties. Still, as the work of Rawls points to human rights, it is 
more robust than approaches based on ethics that tend to 
vary significantly across cultural contexts (Fukuda‐ Parr & 
Gibbons, 2021). Justice as fairness was conceptualized to be 
independent of any specific moral or philosophical doctrine.
The different AI threats to individuals and society, 
such as bias and privacy violations, can be mapped to the 
two key tenets of justice as a fairness theory: liberty and 
equality."Equality"encompasses not only fairness and equal 
treatment for everyone, regardless of characteristics such as 
race, gender, or other personal attributes, but also involves 
addressing biases by creating positive representation for 
underrepresented or disadvantaged groups (Coeckelbergh, 
2020). This means that AI should not discriminate against 
any group or individual and should take into account the 
diversity of the population. For instance, if generative AI 
presents images that rarely depict female math professors, 
the concept of “equality” could support prioritizing images 
of female math professors to challenge stereotypes, influ-
ence real-world perceptions, and address imbalances in 
datasets (Fry, 2018). AI can aim for equality, contributing 
to the fair allocation of opportunities (Dolata et al., 2022). 
Inclusiveness is required to ensure equality. Furthermore, in 
the context of AI, liberty refers to providing individuals with 
control over AI and its impact on their lives. Hence, liberty 
relates to the right to understand AI and to be able to benefit 
from it. Transparency, explainability, interpretability, and 
accountability can be associated with this. To ensure that 
everyone has the right to benefit from AI and avoid risks 
and harms, important concerns from the literature include 
benevolence, non-maleficence, privacy, and security, as well 
as safety and reliability. Aiming for beneficial and controlla-
ble AI can contribute to reducing coerciveness in our socie-
ties and enhancing liberty.
Figure 1 provides an overview of the mapping between 
the two key tenets of justice as a fairness theory (liberty 
and equality) and RAI-related concerns for individuals and 
society.
2.2  Principles for Responsible AI (RAI)
Responsible AI (RAI) points to the importance of aligning 
the application of AI initiatives to human values. It is a term 
widely used in policy documents, practice guidelines, and 
corporate communications (European Commission, 2019; 
Google, 2019; IBM, 2020; Microsoft, 2020; OECD, 2024, 
U.S. General Services Administration, 2022), intended to 
mitigate increasing concerns about the potentially adverse 
impact of AI. To design and deploy RAI, scholars and other 
responsible entities have suggested a number of “principles.” 
For instance, AI4People (a multi-stakeholder forum that 
brings together global businesses including Audi, Elsevier, 
Meta, Fujitsu, Google, Intesa SanPaolo, Johnson & Johnson 
and Microsoft, civil society organizations, academia, and 
government entities) proposed five principles: beneficence, 
non-maleficence, autonomy, justice/fairness, and accounta-
bility (Floridi et al., 2018). Another example is a set of prin-
ciples with four core requirements: “Be socially beneficial”, 
“Avoid creating or reinforcing AI bias”, “Be built and tested 
for safety”, and “Be accountable to people” (Google, 2019). 
Yet another set suggests principles for the responsible devel-
opment and deployment of AI systems: privacy and security, 
Fig. 1  A Rawlsian perspective: Mapping Liberty and Equality to Responsible AI

64 Information Systems Frontiers (2025) 28:61–87
transparency, fairness, reliability and safety, accountability, 
and inclusiveness (Microsoft, 2020). Standards organiza-
tions have proclaimed statements (e.g. ISO 22989 and ISO 
24038) with RAI principles such as robustness, reliability, 
transparency, explainability, interpretability, accountability, 
safety, privacy, and fairness.
Although there are multiple sets of RAI principles, they 
do overlap significantly and converge to an easily identifiable 
set (Fjeld et al., 2020; Jobin et al., 2019). In this research, 
we used key RAI documents guiding practice. We focused 
on practice-oriented documents because our goal is to study 
enactment— how practitioners "make ideas real” in actual 
settings. By consolidating practical guidance, we created 
a baseline set of principles. Specifically, we collected and 
analysed corporate and policy-driven guidelines and derived 
a consolidated set of ten principles: fairness, inclusiveness, 
transparency, interpretability, explainability, accountability, 
benevolence, non-maleficence, privacy-security, reliability-
safety. A key aim was to consolidate the core principles that 
span across different frameworks, ensuring comprehensive-
ness and minimizing redundancy. To achieve this, we sys -
tematically examined and synthesized widely recognized 
frameworks from influential organizations, including the 
Organization for Economic Co-operation and Development 
(OECD), the European Commission (EC), the International 
Organization for Standardization (ISO), and corporate AI 
guidelines from leading technology firms such as Micro-
soft, Google and IBM. These were selected due to their 
significant impact on shaping responsible AI discourse. The 
consolidated list of principles, including their descriptions 
and sources, is presented in Table 1.
Extant research on RAI and RAI principles remains 
largely theoretical, with relatively few empirical studies 
examining how organizations enact RAI in practice. Specifi-
cally, there is research conceptualising prescriptive frame-
works aiming to establish normative guidance for organi-
zations (Georgieva et al., 2022; Mäntymäki et al., 2022; 
Papagiannidis et al., 2025). There is also research exploring 
how regulatory bodies and policymakers embed RAI prin-
ciples into AI governance frameworks (Mittelstadt, 2019; 
Mökander et al., 2021). These studies often discuss policy 
gaps, regulatory enforcement, and compliance challenges 
but do not explore how organizations enact RAI in practice. 
There are some studies that have examined individual RAI 
principles like fairness and transparency in practice but there 
is limited research addressing how they are combined to 
enact RAI (Ghasemaghaei & Kordzadeh, 2024; Watson & 
Nations, 2019). There is some qualitative research on how 
AI teams navigate practical challenges in RAI implementa-
tion (Akbarighatar et al., 2023; Morley et al., 2021; Rakova 
et al., 2021). These studies provide insights into internal 
organizational processes, including how AI practitioners 
interpret and operationalize RAI principles. However, these 
studies do not systematically examine which parts of the 
RAI principles´spectrum are enacted, the extent to which 
different principles are implemented, or how they shape RAI 
Table 1  Responsible AI principles and their descriptions
Principle Description Source
Benevolence and 
non-malefi-
cence
AI technology designed to promote good and maximize ben-
efits, all the while avoiding harm and minimizing risks
(European Commission., 2019; Google, 2019; Microsoft, 
2020)
Safety-reliability AI systems should aim to prevent failures and accidents 
ensuring intended performance
(Google, 2019; ISO: 24028, 2020; Microsoft, 2020)
Privacy Freedom from intrusion into an individual's private life or 
affairs when it happens due to improper or illegal collection 
and use of their data
(IBM, 2020; ISO: 24028, 2020; Microsoft, 2020)
Security Protecting data and controlling access based on authorization 
levels
(ISO: 24028, 2020; Microsoft., 2020; OECD., 2024)
Accountability Taking responsibility, providing justifications for actions, 
responding to inquiries, and being liable
(Google, 2019; ISO:24028., 2020; OECD., 2024)
Explainability Providing comprehensive information about AI's inner work-
ings
(IBM, 2020; ISO: 22989, 2022; Microsoft., 2020; OECD., 
2024)
Intelligibility Enabling humans who use or manage AI to understand the 
reasoning of an AI system
(ISO:24028, 2020)
Transparency Disclosing AI system details, like performance, limitations, 
components, measures, design goals, data sources, for a 
decision, prediction, or recommendation
(European Commission, 2019; IBM, 2020; ISO: 22989, 2022; 
OECD., 2024)
Inclusiveness Involving diverse individuals and perspectives, regardless of 
their unique circumstances
(OECD, 2024; Microsoft., 2020)
Fairness Ensuring impartial treatment, and prevention of discrimina-
tory outcomes
(European Commission., 2019, Google, 2019; IBM, 2020; 
OECD., 2024; Microsoft., 2020)

65Information Systems Frontiers (2025) 28:61–87 
enactment as a whole. Our study addresses this gap, moving 
beyond prescriptive frameworks and limited scope empiri -
cal studies.
2.3  A Configurational Approach to RAI Enactment
This study examines RAI enactment, focusing on how RAI 
principles become part of practices within organizations. 
Drawing on enactment research, we investigate how RAI 
gets enacted through three aspects: practitioner perceptions 
of RAI importance, alignment of AI initiatives with RAI, 
and RAI implementation. The concept of enactment empha-
sizes that actors shape what is actualized rather than merely 
responding to guidelines. So, practitioners´ perceptions are 
key. Weick theorized about enactment to explain how organ-
izations construct their realities (Weick, 2000). Enactment 
is inherently situated and contextual; even when universal 
structures are being enacted, they get adapted and particular-
ized to some extent (Orlikowski & Yates, 1999). It involves 
navigating the complexities of translating abstract ideas into 
operational realities by bridging the gap between notional 
and operative systems, planning for scalability and long-
term sustainability, and ensuring that the resulting structures 
are both functional and usable within their intended environ-
ment (Grisot & Vassilakopoulou, 2013 ; Ribes & Finholt, 
2009). We draw from this prior research on enactment to 
investigate and contextualize the enactment of RAI in actual 
organizational settings. 
Specifically, how RAI gets enacted can be observed 
through practitioners´ perceptions along three key aspects: 
a) do they perceive RAI as an important consideration in 
their organization? b) do they perceive AI to be aligned 
with RAI? c) do they perceive RAI being implemented? 
The first aspect is about reconciling notional objectives 
with actualized ones. In this process, parts of what is con-
ceptualized may remain underutilized (for instance, some 
RAI principles may not be followed through). The second 
aspect concerns being prepared for evolution, envisioning 
a space of possibilities for RAI. This relates to planning 
for evolution and growth. The third aspect concerns the 
process of achieving the practical fit required for harmo-
nizing technologies with RAI. This relates to making RAI 
available to situated practices.
RAI entails enacting multiple different principles. Rather 
than focusing on the net effect of individual principles, a 
configurational perspective allows us to explore how they 
combine to produce the outcome of interest, that is, RAI 
enactment. Examining configurations allows acknowledg -
ing conjunctural causation (Slager et al., 2021), equifinality 
(Katz & Kahn, 1978), and asymmetrical causation (Mis-
angyi et al., 2017). In the context of RAI, this approach high-
lights that enactment results from multiple principles, can 
emerge through different principles´ configurations, and that 
distinct factors may drive enactment presence or absence. 
Equifinality means that different configurations can lead to 
successful RAI enactment, offering multiple pathways to the 
same outcome. For our analysis, we apply fsQCA (Ragin, 
2008) following the guidelines of Pappas et al. (2016), Park 
& Mithas (2020), and Mattke et al. (2022). Our research 
model (Fig. 2) illustrates how different principle configura-
tions contribute to overall RAI enactment, shifting the focus 
from isolated principles to their collective impact.
The configurational approach aligns with Rawls' con-
ceptualization of justice as fairness through their shared 
emphasis on interdependent conditions that collectively 
shape outcomes. Rawls argues that justice emerges as a con-
joint effect of liberty and equality. The Rawlsian perspective, 
thus, guides us to investigate configurations of principles 
rather than the effects of single principles. Liberty relates 
to principles that ensure AI upholds human rights, such as 
privacy, security, benevolence, transparency and accounta-
bility. Equality emphasizes fairness and non-discrimination, 
Fig. 2  Research Model: configurations leading to RAI enactment

66 Information Systems Frontiers (2025) 28:61–87
relating to principles ensuring that AI fosters inclusivity, 
mitigates biases, and distributes opportunities equitably.
3  Methods
In this study, we employed a combination of quantitative 
and qualitative research to address our research question, 
integrating quantitative data collected through a survey with 
qualitative insights obtained from follow-up interviews. This 
study uses an exploratory sequential design to understand 
how firms achieve higher RAI enactment (Fig. 3 provides an 
overview). This approach involves conducting a quantitative 
study first, followed by qualitative interviews with a sample 
of the same respondents (Ragin, 2008; Woodside, 2014 ). 
By following this mixed-methods approach, we aim to dis-
cover how configurations of key RAI principles translate 
into overall RAI enactment. The empirical part of this study 
is split into two steps. In the first step, data are collected 
via an online questionnaire sent to experts in the EU and 
the US (study 1). In a second step, to interpret and extend 
the explanatory power of the results of fsQCA, a qualita-
tive follow-up study with experts that displays features of 
each one of the configurations identified through the earlier 
quantitative study is conducted (study 2).
3.1  Survey Sample
Our survey targeted AI experts involved in AI solution devel-
opment and integration as an AI initiative in organizations. 
The participants consisted of managers, AI governance 
experts, AI developers, and other relevant positions within 
these organizations. We identified and contacted poten-
tial respondents through professional groups on LinkedIn, 
such as the “Artificial Intelligence and Business Analytics” 
group and the website “Ethical AI Database”. This approach 
ensured a robust and representative sample for our study.
We reached out to selected respondents via email, specifi-
cally targeting those in high-level technology management roles 
who possessed knowledge of RAI operations and practices. 
Following an initial invitation and three subsequent reminders, 
each one week apart, we sent a total of 600 email invitations 
from September to December 2023 to potential participants 
experienced in AI initiative projects. To avoid sampling error 
bias, two preliminary questions were asked to make sure that 
the respondents selected for the study were appropriate: 1) Do 
you contribute, manage, or consult to AI projects? and 2) How 
familiar are you with the concepts of responsible or ethical AI? 
From these invitations, we received a total of 135 complete and 
22 incomplete responses, primarily due to respondents' unfa-
miliarity with RAI practices in organizations (Table 2).
These responses came from various industries, including 
financial services, manufacturing, and high-tech companies. 
The participants held a range of job titles, including head of 
AI or data science, chief data governance officers, directors 
of IT, co-founders, and chief data scientists, representing 
European or North American companies.
3.2  Case‑Based Qualitative Follow‑up
In the second step of the study, respondents from the survey 
were subsequently contacted via email and invited to par -
ticipate in a follow-up interview. We recruited one person 
per configuration. In the interview invitation message, we 
outlined the purpose of the research and clarified that par -
ticipants were selected because they voluntarily shared their 
email addresses. We explained that the interviews would 
take approximately 30–45 min and assured participants that 
their information and company names would remain confi-
dential and anonymous. Additionally, we emphasized that 
the data collected would be used solely for academic pur -
poses. The aim of this process was to re-examine evidence 
related to cases assigned to each configuration and explore 
with the follow-up interviews the reasons behind the pres-
ence or absence of specific conditions. Five interviews, one 
per configuration, with an average duration of 37 min, were 
conducted from February 2024 to June 2024. Table  3 pro-
vides an overview.
Fig. 3  Method overview: exploratory sequential design

67Information Systems Frontiers (2025) 28:61–87 
3.3  Survey Instrument Development and Validation
3.3.1  Instrument Development
The survey instrument development commenced with the 
conceptualization of the constructs representing RAI prin-
ciples and enactment, drawing from literature as outlined in 
Appendix A. The enactment of individual RAI principles is 
conceptualized as a condition for overall RAI enactment as 
an outcome. Enactment at the principle level and for RAI as 
a whole is evaluated through three metrics: perceived impor-
tance, alignment, and implementation of RAI principles. To 
articulate each principle, we analysed the literature and also 
engaged a panel of six experts with substantial academic and 
practical experience in responsible AI. Four of these experts 
had over 15 years of industry experience in data science and 
AI, while the remaining two were senior academics special-
izing in Information Systems in organizations. We provided 
the experts with definitions of each principle and asked them 
to answer the survey questions. Additionally, we sought their 
recommendations for improving or refining questions. Their 
insights led to minor modifications, particularly in clarify -
ing distinctions between closely related principles such as 
explainability, intelligibility, transparency, and safety. These 
refinements enhanced the clarity of definitions and survey 
questions, ultimately strengthening the content validity of 
our instrument.
We then distributed the revised survey instrument to four 
C-level technology managers. These managers were selected 
from companies that specialize in responsible AI solutions 
for AI firms and possess extensive experience in implement-
ing RAI principles. Taking their input into account, we care-
fully revised and refined the definitions of the principles 
to ensure they were more concise and understandable. A 
7-point Likert scale anchored from 1 to 7 is employed. To 
evaluate enactment, we surveyed experts about their percep-
tions of 1) the importance organizations place on each RAI 
principle, 2) the alignment of RAI principles with organiza-
tional AI processes, and 3) the level of RAI principle imple-
mentation within existing AI initiatives.
3.3.2  Instrument Validation
Before conducting the fsQCA analysis, we validated the 
measurement instruments which are related to the enact-
ment of individual principles. This is done in four steps 
reporting on all principles. Beginning with indicator reli -
ability, we evaluate how well each principle measured its 
associated constructs. All the measured constructs have had 
three indicators. The analysis reveals that all the outer load-
ings (OL) were above the recommended level of 0.60, which 
is acceptable for explorative research (Hair et al., 1998). 
However, we have found that indicators used to measure 
explainability and intelligibility load under the same com-
ponents. The same issue occurred with indicators measuring 
fairness and inclusiveness. This suggests that participants 
perceived the indicators of these principles to measure the 
Table 2  Descriptive statistics of 
the sample Category Percentage of 
respondents
N = 135
Category Percentage 
of respond-
ents
N = 135
Total working experience AI-related working expericnce
Fewer than one year 0% Fewer than one year 0,0%
1–3 years 14% 1–3 years 32%
4–6 years 25% 4–6 years 33%
7–10 years 18% 7–10 years 20%
More than 10 years 43% More than 10 years 15%
Familiarity with the concept of Responsible AI Education level
Expert 21% PhD 33.3%
Very familiar and involved actively 34% Master 53.1%
Very familiar and some involvment 23% Bachelor 13.6%
Familiar but never involved 16% Where
Hear about it 6% Europe 55%
Never heard 0,0% North America 45%
Table 3  Overview of participants in the qualitative study (study 2)
Business Category Type of business Age Education
A S1 E-commerce 35–44 Master
B S2 Optimizing resource alloca-
tion
25–34 Bachelor
C S3 Education 35–44 PhD
D S4 Responsible AI consulting 25–34 Bachelor
E S5 Entertainment 25–34 PhD

68 Information Systems Frontiers (2025) 28:61–87
same constructs. Second, according to the statistical reports, 
which show a high correlation, we decided to merge intel-
ligibility and explainability in one construct, that is “mean-
ingful explainability”, as well as fairness and inclusiveness, 
into “Inclusive Fairness”.
In the final step of instrument validation, we tested the 
reliability and validity of the model using Cronbach’s α 
coefficient and composite reliability (CR), which should be 
greater than 0.8 (Gefen et al., 2000). CR is greater than 0.90 
for all constructs, which indicates sufficient internal consist-
ency. All Cronbach’s α values are greater than 0.8, indicat-
ing high reliability. Moreover, we assessed the convergent 
validity through the constructs average variance extracted 
(AVE). Convergent validity evaluates the amount of variance 
captured by a construct´s indicators related to the amount 
of variance that is caused by measurement error. The rec-
ommended threshold for AVE is 0.50 (Fornell & Larcker, 
1981), and all AVE values were above, which means that 
various caused by random errors did not challenge the valid-
ity of the model. Also, Table 4 presents the descriptive sta-
tistics, AVE, and correlations for the study constructs. The 
results confirm that the square root of each construct’s AVE 
is greater than its correlations with other constructs, further 
supporting discriminant validity (Fornell & Larcker, 1981). 
Furthermore, correlations among constructs did not exceed 
0.8, suggesting low multicollinearity and ensuring clear dif-
ferentiation between constructs. Appendix B provides addi-
tional details, including standardized factor loads, residual 
variance, Cronbach’s α, CR, and values of each construct’s 
measurement items.
3.4  Survey Data Analysis
3.4.1  Use of fsQCA
We applied fsQCA by following guidelines and best prac-
tices in IS (Mattke et al., 2022; Pappas & Woodside, 2021; 
Park & Mithas, 2020). Grounded in set theory, fsQCA 
is particularly suited for this study for three key reasons. 
First, it allows for the analysis of each case (an organiza-
tion response) as a collection of conditions (principles) 
and assess how different combinations of these condi-
tions contributed to the observed outcome. Each case was 
evaluated based on its degree of membership in various 
causal configurations. After estimating causal recipes, 
fsQCA enables researchers to return to the empirical data 
and interpret the configurations derived from the analysis. 
This allows for deepening the understanding of findings 
by combining configurational analysis with case-level 
insights (Greckhamer et al., 2018).
As a data analysis technique, fsQCA has become 
increasingly popular in configurational approaches across 
both business and behavioral sciences, applied at indi-
vidual and organizational levels. The configurational per -
spective is built on the principle of conjunctural causa-
tion, which posits that conditions leading to an outcome 
do not act in isolation but rather in combination (Slager 
et al., 2021). Additionally, fsQCA facilitates the exami-
nation of equifinality (Katz & Kahn, 1978), by revealing 
multiple pathways that can lead to the same outcome. 
Finally, asymmetrical causation in fsQCA acknowledges 
that causal relationships are often not symmetric, meaning 
the factors leading to an outcome may differ from those 
leading to its absence (Misangyi et al., 2017). Addition-
ally, fsQCA distinguishes between necessary and sufficient 
conditions, offering a deeper understanding of how these 
conditions can combine to explain an outcome (Ragin, 
2008). These conditions can be present, absent, or on a 
“do not care” state, that is when the outcome will occur 
regardless of their presence or absence. This distinction 
also leads to identifying core and peripheral elements, 
where core elements are strongly associated with the out-
come, while peripheral elements have a weaker connec -
tion (Fiss, 2011). This approach is beneficial for small or 
medium-sized datasets and offers insights into the diverse 
paths that can lead to a given outcome (Fiss, 2007).
Table 4  Descriptive statistics, 
AVE, and correlations of 
constructs
ME/SD √AVE 1 2 3 4 5 6 7 8 9 10
1.Benevolence and 
non-maleficence
5.42/1.37 0.75 1
2.Safety-reliability 6.08/1.04 0.79 0.59 1
3. Privacy 5.98/1.06 0.82 0.54 0.56 1
4. Security 5.16/1.01 0.79 0.59 0.58 0.55 1
5.Accountability 4.90/1.42 0.73 0.44 0.49 0.47 0.51 1
6.Explainability 4.89/1.55 0.77 0.53 0.56 0.51 0.55 0.49 1
7.Intelligibility 4.70/1.53 0.76 0.60 0.57 0.53 0.57 0.50 0.54 1
8.Transparency 4.84/1.54 0.72 0.60 0.57 0.52 0.56 0.49 0.53 0.57 1
9.Inclusiveness 4.42/1.72 0.83 0.52 0.53 0.50 0.52 0.46 0.50 0.54 0.53 1
10.Fairness 4.76/1.73 0.81 0.51 0.52 0.50 0.51 0.46 0.50 0.53 0.52 0.56 1

69Information Systems Frontiers (2025) 28:61–87 
We intentionally selected professionals with RAI exper -
tise, as their knowledge is crucial for understanding how 
RAI is enacted in practice. Hence, our sample purposefully 
includes only organizations that have advanced in their RAI 
journey. Overall, random sampling tends to be inappropri-
ate for fsQCA for two reasons: first, it is based on gener -
alizations on properties of central tendency, variability, and 
the shape of sampling distributions (Ragin, 2000). Second, 
random samples risk overlooking unique or rare cases that 
may be crucial in explaining the outcome (Greckhamer 
et al., 2018). Unlike statistical methods that rely on random 
sampling for generalizability, fsQCA is case-oriented and 
requires theoretically relevant cases. Expert-driven sam-
pling ensures that all cases in our dataset provide meaning-
ful, high-quality insights into RAI enactment. Therefore, we 
carefully identified and targeted experts whose perspectives 
contribute to a nuanced, contextually rich analysis. FsQCA 
is designed to work with moderate sample sizes, as it identi-
fies empirical patterns across cases rather than testing each 
theoretical combination. As Ragin (2008) and Schneider & 
Wagemann (2012) note, fsQCA does not require all logi-
cally possible configurations to be present in the dataset. 
We followed fsQCA best practices for calibration and we 
present the approach followed in the following subsection. 
We tested the stability of our results with different calibra-
tion thresholds and we present the findings of sensitivity 
analyses in Sect. 3.4.3.
3.4.2  Calibration
As a first step for applying fsQCA, calibration is essential 
when assigning set-membership scores to antecedents and 
outcomes in fsQCA (Schneider & Wagemann, 2012). Cali-
bration determines the degree to which a particular case 
belongs to a set. It involves defining three reference points: 
full membership, full non-membership, and the crossover 
point, based on both empirical evidence and theoretical 
understanding of the context and cases (Ragin, 2008). Case 
membership is represented by a numerical value ranging 
from 0 (indicating complete non-membership) to 1 (full 
membership). All constructs in this study were measured 
using a 7-point Likert scale. Following the calibration guide-
line for calibration, we define three anchors: a value of the 
95% percentile for full membership, 5% percentile for full 
non-membership, and 5% percentile as the crossover point 
(Ragin, 2008).
These anchors were chosen in several iterations based on 
theoretical knowledge and the distribution of the dataset. 
As our dataset was skewed more to the higher scales and by 
choosing, for instance, 2 as full non-membership, we would 
have fewer cases with lower functions. We employed percen-
tile-based anchors to provide a statistical, data-driven, and 
context-sensitive approach that more effectively captures the 
variability in how respondents perceive RAI principles. For 
example, by setting the 5 th percentile for full non-member-
ship, we ensure that significantly underperforming cases in 
RAI enactment are accurately identified (as demonstrated in 
Table 4, where non-membership is high for most principles). 
This approach allows for a more nuanced understanding of 
the response distribution. The 50 th percentile represents 
the crossover point, while the 95 th percentile reflects high 
levels of RAI enactment, enhancing both the precision and 
validity of the analysis. The calibration anchors of the con-
structs are shown in Table 5.
After the calibration, we examined the truth table to 
identify combinations of principles that produce the out-
come of interest (Pappas & Woodside, 2021). In Appendix 
C (Appendix Table 9), we present truth tables for high RAI 
enactment. The truth table includes all logically possible 
combinations of principles, and each row corresponds to a 
combination. Considering our sample size, to cover more 
cases and avoid missing many cases by eliminating the sin-
gle cases, we set the minimum acceptable frequency of cases 
at one. In addition, according to Greckhamer et al. (2018), 
Table 5  Calibration Anchors for 
the Constructs Principle & Outcome Mean SD AVE Anchors
Full mem-
bership
Cross-over Full non-
member-
ship
Benevolence and non-maleficence 5.42 1.37 0.56 7 6 2.5
Safety-reliability 6.08 1.04 0.62 7 6 4
Privacy 5.98 1.06 0.67 7 6,5 3,8
Security 5.16 1.01 0.63 7 6 3,4
Accountability 4.90 1.42 0.53 7 5,5 2,5
Meaningful explainability 4.70 1.47 0.60 7 5 2
Transparency 4.84 1.54 0.52 7 5 2
Inclusive Fairness 4.42 1.74 0.69 7 5 2
RAI Enactment 4.62 1.60 0.56 7 5 2

70 Information Systems Frontiers (2025) 28:61–87
we set the raw consistency threshold to 0.80 and the PRI 
consistency threshold to 0.70 with at least one empirical 
instance and a raw consistency of at least 0.8 considered, as 
well as PRI consistency of at least 0.70 as reliably resulting 
in high RAI enactment. The outcome column shows a value 
of 1 (i.e., explains the outcome) for these combinations; oth-
erwise, zero (does not explain the outcome).
3.4.3  Sensitivity Analysis and Predictive Validity
To validate the robustness of our fsQCA calibration process, 
we conducted three sensitivity analyses: 1) sensitivity of the 
results to calibration parameters, 2) sensitivity analysis for 
consistency threshold, and 3) sensitivity analysis for fre -
quency threshold. For calibration of the principles and out-
comes, we followed previous studies (Douglas et al., 2020; 
Soltani Delgosha et al., 2024), initially using the median 
± one standard deviation points (fully in at the median plus 
one standard deviation, fully out at the median minus one 
standard deviation, and the median for the crossover point), 
applying this rule to all principles. Next, we used mean 
± one standard deviation points, and finally, we adjusted 
values by ± 0.25 for thresholds and crossover points. Addi-
tionally, we adjusted the PRI consistency threshold from 
0.70 (noted in Appendix Table  10 and Fig.  4) to 0.65 and 
then to 0.60. With these new thresholds for consistency and 
calibrations, we performed new fsQCA analyses. The results 
indicated only minor changes in peripheral conditions and 
the number of cases in configurations, while a clear subset of 
relationships between principles persisted, and the interpre-
tation of configurations remained largely unchanged.
We further tested for the predictive validity of the fsQCA 
results, to examine how well the model predicts the out-
come in additional samples (Gigerenzer & Brighton, 2009; 
Pappas & Woodside, 2021; Woodside, 2014). Predictive 
validity is important because achieving only a good model 
fit does not necessarily mean that the model offers good 
predictions. To this end, the sample is split into a subsample 
and a holdout sample. Appendix E shows that the patterns 
of complex antecedent conditions are consistent indicators 
of high scores in RAI enactment using the subsample. As 
presented in Appendix E, the findings for testing model 1 
predictions indicate a high consistency (0.923) and high cov-
erage (0.582). Predictive tests for all models suggest that 
the highly consistent models for the subsample have high 
predictive abilities for the holdout sample, and vice versa.
3.5  Data Collection and Analysis for the Qualitative 
Follow‑Up Study
To gain deeper insights into the configurations identified 
by fsQCA we conducted a qualitative follow-up study. This 
approach allows for both generalization beyond specific 
cases and a detailed examination of individual instances 
(Ragin, 2008). Such an analysis aligns with prior research, 
which showed how valuable can be the insights from in-
depth investigations in small samples (Crouch & McKen -
zie, 2006). To confirm the findings of the first study and 
understand the different configurations better, we conducted 
semi-structured interviews (Appendix F). These interviews 
aimed to understand how interviewees perceive the respec-
tive principles and their enactment and what are the particu-
larities of RAI enactment within their organizations. The 
interviews were recorded and transcribed. This additional set 
of empirical data allowed us to better interpret the configura-
tions derived from the analysis, deepening the understand-
ing of findings by combining configurational analysis with 
case-level insights.
4  Results
4.1  Configurations for RAI Enactment
Truth table analysis was adopted to identify combinations 
of RAI principles that are sufficient for RAI enactment 
(Ragin, 2008). In fsQCA, counterfactual analysis is inher -
ently involved whenever researchers draw causal inferences 
from “naturally occurring” social data where limited diver -
sity is common. This means addressing hypothetical sce-
narios—absent combinations of causal conditions—that do 
not appear in the dataset (Ragin & Sonnett, 2005). Three 
types of solutions, the complex, parsimonious, and interme-
diate solutions, can be obtained through fsQCA. A complex 
solution includes configurations without any counterfactu-
als, meaning all possible combinations of conditions are 
explicitly presented. A parsimonious solution includes con-
figurations with both “easy” and “difficult” counterfactuals, 
which means solutions incorporate existing knowledge and 
empirical evidence that are both straightforward to justify 
(easy counterfactuals) and those that may require stronger 
theoretical or empirical justification (difficult counterfactu-
als) (Ragin, 2008). An intermediate solution includes con -
figurations only with “easy” counterfactuals (Fiss, 2007). 
Elements that are part of both parsimonious and interme-
diate solutions are called core conditions, which have a 
stronger relationship with the outcome as they cannot be left 
out of any configuration. Elements that only appear in the 
intermediate solution but not in the parsimonious solution 
are peripheral conditions, which suggest a weaker relation-
ship with the outcome. The output of the fsQCA analysis, 
including both the parsimonious and intermediate solutions, 
is presented in Fig. 5 in Appendix C.
Table 6 displays the fsQCA results, including consist-
ency and coverage values for each configuration or recipe. 
Coverage indicates the extent to which each recipe, as well 

71Information Systems Frontiers (2025) 28:61–87 
as the overall configuration, accounts for the outcome. In 
particular, five configurations are linked to achieving high 
RAI enactment. While all configurations explain high RAI 
enactment, configurations 1–4 have nearly identical raw cov-
erage scores. Accountability is identified as a core condition 
across these configurations and acts as"decisive causal ingre-
dients,” and transparency” is peripheral playing contributing 
condition roles (Greckhamer et al., 2018). In configurations 
1–3, “safety-reliability”, “benevolence” and “meaningful 
explainability” are also identified as core conditions.
The first identified configuration for RAI enactment 
focuses on the presence of principles, including benevolence 
and non-maleficence, safety-reliability, security, accounta-
bility, and meaningful explainability as core conditions, and 
privacy and transparency as peripheral conditions, regard-
less of inclusive fairness. Going back to the cases in our 
sample, two examples are provided to illustrate how high 
levels of enactment can be observed without including fair-
ness. Case 135 involves an expert working on e-commerce 
applications that provide product recommendations to cus-
tomers. In this case, benevolence and non-maleficence are 
core principles, as the expert believes in offering beneficial 
suggestions that cause no harm. Fairness is not perceived as 
a relevant issue for product recommendations by the expert 
as long as the product suggestions cause no harm. The expert 
focuses on reliability (ensuring the accuracy of recommen-
dations), privacy, accountability, and explainability as core 
conditions, and the combination of these conditions leads to 
achieving RAI enactment.
In the second and third configurations for RAI enactment 
(Table 7), four common core conditions have been iden-
tified: benevolence and nonmaleficence, safety-reliability, 
accountability, and explainability. Fairness and transparency 
are peripheral conditions for achieving RAI enactment in 
both configurations. The key difference between the two 
configurations lies in the role of security and privacy. In 
configuration 2, security is a “don´t care” condition, and 
privacy plays a contributing condition role (peripheral con-
dition). In contrast, in configurations 3, security is a core 
condition, while privacy becomes a “don’t care” condition. 
Experts in configuration 2 are employed in large organiza-
tions where the focus is primarily on AI innovation, with 
less emphasis on privacy and security concerns. Case 12 in 
configuration 3, is a co-founder of an organization providing 
an AI-powered gaming platform for educational purposes. 
In this scenario, security is a core condition, while privacy 
concerns are deemed less relevant to their operational focus.
According to configuration 4, case 38 stands out as a 
unique instance. FsQCA reveals that organizations can man-
age to attain RAI enactment by presence of all principles, 
regardless of benevolence. A combination of the core con-
ditions, including security, accountability, and explainabil-
ity, and peripheral conditions, including safety-reliability, 
privacy, transparency, and fairness, with benevolence as a 
don´t care condition, lead to RAI enactment. In the last con-
figuration, “inclusive fairness” and “benevolence and non-
maleficence” are present as core conditions, “transparency” 
(as a core condition) and “meaningful explainability” are 
Table 6  Configurations for achieving a high level of RAI enactment
12 34 5
Basic Liberties 
Benevolence & Non-maleficence ●● ●●
Safety-reliability ●● ● ●●
Privacy ●● ●●
Security ●● ● ●
Accountability ●● ●● ●
Transparency ●● ●● /uni2A02/uni2A02
Meaningful explainability ●● ●● /uni2A02
Equality
Inclusive Fairness ●●             ● ●
Consistency0 .928 0.9270 .921 0.93 0.949
Raw coverage 0.5640 .556 0.5490 .545 0.256
Unique coverage 0.0350 .026 0200 .016 0.028
Overall solution consistency0 .918
Overall solution coverage 0.654
Black circles ( ) indicate the presence of a condition, and circles with “x” (⊗) indicate its absence. Large circles indicate core conditions, small 
ones, peripheral conditions. Blank spaces indicate “don’t care”

72 Information Systems Frontiers (2025) 28:61–87
absent, and the other principles are peripheral. In configura-
tion 5, three cases (22, 61, and 86) share some similarities. 
These cases represent situations where companies utilize AI 
systems in low-risk settings, such as in entertainment and 
agriculture, or semi-automated tasks. In this configuration, 
experts perceived transparency and explainability as “negated 
conditions” in their AI initiatives. Notably, these organiza-
tions are small in size, based in Europe, and have recently 
begun implementing RAI principles. Table 7 provides demo-
graphic information for all the example cases mentioned.
4.2  Analysis of Qualitative Follow‑Up Interviews
Our qualitative data analysis provides complementary 
insights into the experts' perceptions regarding RAI enact-
ment. We employed a bridging approach to align the find-
ings from fsQCA with those from the in-depth qualitative 
study (Venkatesh et al., 2013). This method allowed us to 
cross-validate the fsQCA results with interview data and 
thorough analysis. The bridging process revealed significant 
convergence between the two sets of findings, reinforcing the 
overall conclusions. For the analysis of the interviews, we 
used an open-coded approach to identify emerging themes 
from the data, which were then used to frame the proposi-
tions and recommendations for RAI enactment.
The qualitative findings confirmed all five configurations 
identified by fsQCA and also provided deeper insights into 
the role certain conditions play in specific contexts. We inter-
viewed Case 135 from configuration 1, which involves an 
expert working on an e-commerce platform that provides prod-
uct recommendations to customers. The expert in this case 
perceived that the system is designed to enhance user experi-
ence by suggesting relevant products based on browsing and 
purchase history. The developer’s focus on benevolence and 
reliability (ensuring recommendations are beneficial, harmless, 
and accurate) and the reliance on user behavior data make fair-
ness a"do-not-care"condition, as the perceived risk of systemic 
discrimination is minimal, and its potential impact on users is 
limited. The expert emphasized this perspective, stating:
“Our mission is providing accurate recommendations 
that are beneficial and cause no harm. The recommen-
dations are based on user behavior and preferences, 
making biased outcomes unlikely in this setting.” (case 
135, configuration 1).
The reasoning behind fairness being a"do-not-
care"condition stems from the fact that the recommendation 
system does not rely on demographic attributes. Instead, it is 
based on user interactions—such as browsing and purchase 
history—thus avoiding bias. The expert noted:
“We ensure that our recommendation system avoids 
discrimination by relying solely on user behavior 
rather than demographic attributes, this approach 
helps mitigate proxy biases” (case 135, configura-
tion 1).
Moreover, the expert noted that the system includes fea-
tures that allow users to adjust their recommendations, for 
instance, by disliking suggestions, and users have control 
over the recommendations they receive:
“We obtain users'consent before recommending prod-
ucts based on their activity on our platform. If they 
come across a suggestion they don’t like, they can 
simply dislike it, and we will adjust recommendations 
accordingly” (case 135, configuration 1).
The interview with case 69 (configuration 2) highlighted 
that since they do not work with sensitive personal data, 
privacy is considered a less pressing issue in their RAI prac-
tices, making it a peripheral condition. Additionally, they 
view their well-established pre-existing IT infrastructure as 
providing a strong foundation for security, which is why they 
consider security a"do-not-care"condition. However, this 
does not mean security is unimportant. Rather, they believe 
Table 7  Demographic information for example cases
Case Industry AI related 
Work experi-
ence
Job title Country Number of 
employees
When their organization 
started to implement 
RAI
10 Public services  + 10 Data scientist manager Europe  + 500 3–5 years ago
12 Education  + 10 Co-founder North America 11–100 1–3 years ago
22 Entertainment 1–3 Operations Research engineer Europe 1–10 Less than a year ago
38 AI technical consultancy 1–3 Solutions engineer North America 11–100 3–5 years ago
61 Agriculture 1–3 Senior data strategist Europe 1–10 1–3 years ago
69 Optimizing resource allocation  + 10 Project manager North America  + 500 1–3 years ago
86 Energy  < 1 Socio-ethical consultant Europe 11–100 1–3 years ago
112 RAI consultancy 1–3 Project manager Europe  + 500 3–5 years ago
135 E-commerce 1–3 AI developer Europe 1–10 1–3 years ago

73Information Systems Frontiers (2025) 28:61–87 
their organization already has well-established infrastruc-
tures and security frameworks in place, allowing them to 
focus more on operational efficiency in achieving RAI enact-
ment. The expert stated:
“Our organization focuses on building a scalable AI 
solution to cut costs and improve efficiency. While 
privacy and security matter, they aren’t our main pri-
orities since our model mainly deals with production 
metrics, which keeps privacy risks low. With a strong 
IT infrastructure and solid security protocols already 
in place, we do not see them as a big concern in our 
current work.”(case 69, configuration 2).
The interview with case 12 (configuration 3) involves 
a startup that develops an AI-powered gaming platform for 
educational purposes, focusing on engagement and learn-
ing outcomes. The co-founder of this startup emphasized 
several core conditions: “services in our platform do not 
harm users” (benevolence and nonmaleficence), “the plat-
form provides reliable content” (safety-reliability), “we are 
responsive for any issues arising from the platform´s use”  
(accountability), “provides clear explanations” (explainabil-
ity), “user data must be protected from breaches” (security).
In this configuration, privacy was identified as a don´t 
care condition. For this case, the expert justified it by stating:
“We only collect basic educational data and make sure 
not to gather anything that could relate to personal 
privacy.” (case 12, configuration 3).
The interview with case 38 (configuration 4) provides 
insights for a pathway to RAI enactment where core condi-
tions (security, accountability, explainability) and peripheral 
conditions (safety-reliability, privacy, fairness) are sufficient 
regardless of benevolence. The interview with the expert (a 
solutions engineer), reveals why benevolence was perceived 
as a do not care condition in this context. The interviewee 
described their role as inherently technical and problem-
solving-focused, emphasizing the design of systems that 
meet predefined specifications and compliance requirements. 
In their view, benevolence relates to the greater good for 
society at a large, and this was deemed out of scope for their 
organizational goals. This perspective reflects a worldview, 
which frames benevolence as a societal mission separate 
from organizational objectives. As the interviewee suc-
cinctly stated:
"My role and our organization´s mission isn’t to solve 
societal problems; we are building systems that meet 
technical requirements. Benevolence isn’t in my job 
description; my KPIs are accuracy, security, and 
audibility."(case 38, cofiguration 4).
The interview with case 22 (confifuration 5) provided 
more interesting insights. The expert interviewed (working in 
a small European organization deploying AI for music stream-
ing) expressed concerns about providing explanations for AI-
generated recommendations. The expert thought that these 
could confuse users rather than enhance their experience and 
noted that adding explanations as to why certain songs were 
recommended would increase complexity and potentially over-
whelm users, making the system less intuitive. In this configu-
ration, explainability is a negated condition. The expert stated:
“One important consideration is the cost and the 
necessity of explaining our recommendations to cus-
tomers. When we recommend certain music, creating 
a section to explain why can be very challenging. This 
process not only adds complexity but can also make 
it confusing for the users.” (case 22, configuration 5)
5  Discussion
5.1  Theoretical Implications
Our work responds to scholarly calls on the importance 
of translating RAI principles into practice (Arbelaez 
Ossa et al., 2024; Mikalef, 2024; Munn, 2023). The theo-
retical contributions of this study are twofold. First, we 
extend the current RAI literature by conceptualizing RAI 
enactment, grounding this in Rawls's theory of justice 
as fairness (Rawls, 2001). RAI principles are rooted in 
risk mitigation and have been lacking a theoretical fram-
ing that could help organizations make sense of them as 
a coherent whole. This is the first study introducing an 
overarching theoretical framing. This framing aligns with 
prior literature pointing to the importance of ensuring 
that AI initiatives uphold individual rights and promote 
equal access to opportunities (Baygi et al., 2024). Taking 
a Rawlsian perspective on RAI orients attention to inter -
dependent conditions that collectively shape outcomes. 
Rawls argues that justice emerges as a conjoint effect of 
liberty and equality. Liberty relates to principles ensuring 
that AI systems uphold human rights, such as privacy, 
security, benevolence, transparency, and accountability. 
Equality relates to fairness and non-discrimination, link -
ing to principles for AI inclusivity and bias mitigation. 
A Rawlsian perspective is also well-aligned with the use 
of fsQCA for data analysis as it supports equifinality and 
asymmetrical causation.
Rawls acknowledges that different structures can achieve 
justice as long as they uphold fairness (Rawls, 2001). 
Asymmetrical causation highlights that the factors driving 
successful RAI enactment may not be simply the inverse 
of those leading to its absence. Equifinality suggests that 
multiple pathways can lead to successful RAI enactment, 

74 Information Systems Frontiers (2025) 28:61–87
so different combinations of principles can produce respon-
sible AI.
Second, using a configurational approach (fsQCA), we 
identify how combinations of principles contribute to RAI 
enactment, shifting attention from individual principles to 
configurations of principles. Our findings show that account-
ability and safety-reliability are present in all configurations 
as core principles, implying that these need to be tied with 
other principles in order to create a successful RAI strat -
egy. It is important to highlight that while accountability and 
safety-reliability are core principles, they are not sufficient on 
their own for achieving RAI enactment in any configuration. 
Our findings regarding the role of accountability and safety-
reliability extend arguments that have been used in prior work 
to explain the effect of accountability mechanisms and of 
measures to ensure the reliability of AI-based recommenda-
tions or predictions (Díaz-Rodríguez et al., 2023). Empirical 
research has highlighted the importance of these two prin-
ciples for AI initiatives. The configurational approach pro-
vides new insights indicating that the key to RAI enactment 
lies not in the two individual principles alone but rather in 
how these core principles are configured together with other 
principles. By conducting interviews with experts from each 
configuration identified in our fsQCA findings, we obtain a 
deeper understanding of the contextual nature of RAI princi-
ples and the inherent tensions in their implementation. These 
interviews provide valuable insights, helping to explain why 
certain principles are present, absent, or considered irrelevant 
in different cases. Through this analysis, we contribute to 
the broader discourse on the enactment and operationaliza-
tion of RAI principles (Advenica, 2020; PwC, 2020; Rakova 
et al., 2021). Our findings provide empirical evidence on how 
experts within organizations perceive the enactment of RAI 
principles by revealing the contextual rationales and organi-
zational trade-offs that explain why principles are present, 
absent, or treated as regardless in daily practices. Building 
upon these insights, we propose the following:
Proposition 1. The Principles of Accountability and 
Safety‑Reliability are Pivotal for RAI Enactment This propo-
sition suggests that accountability mechanisms and mecha-
nisms to prevent failures and accidents are consistently nec-
essary across configurations for high RAI enactment. Thus, 
effective harmonization of accountability and safety-relia-
bility with other principles is essential for RAI enactment.
Furthermore, our study reveals that the comprehensive 
enactment of all RAI principles isn't necessary. Reviewing 
the five distinct configurations identified, we see that high 
RAI enactment is achievable even when certain principles 
are absent. For instance, high enactment was observed even 
when omitting security, privacy, or benevolence and non-
maleficence, provided other principles were present. These 
findings suggest that RAI enactment is less about individual 
principles and more about achieving a specific configuration 
of several principles within specific contexts, supporting a 
more holistic and nuanced understanding of RAI. This aligns 
with earlier arguments from the literature indicating that 
the impact of individual RAI principles on RAI enactment 
is multifaceted and context-dependent (Floridi & Cowls, 
2022). Based on this, we propose the following:
Proposition 2. Context‑Dependent Configurations of Prin‑
ciples Drives RAI Enactment This proposition suggests 
that RAI enactment depends on specific contextual con-
figurations, not on the comprehensive enactment of each 
and every individual principle. Effective RAI enactment 
arises from diverse configurations of principles, rather than 
a single optimal configuration, instead, multiple effective 
configurations exist.
The findings also show that RAI enactment can be 
achieved without enacting the principles of transparency and 
meaningful explanations when the potential for confusion, 
privacy/security risks, or legal non-compliance outweighs 
their benefits. While most RAI principles, such as fairness, 
accountability, and safety-reliability, consistently contribute 
to a stronger RAI enactment, there can be instances where 
transparency and the provision of meaningful explanations 
may threaten the privacy or security of users and organi-
zations or raise legal concerns. In such cases, the presence 
of these two principles, in conjunction with the others, may 
not necessarily lead to a higher RAI enactment. For exam -
ple, some explanations could potentially expose sensitive 
user data or reveal vulnerabilities that could be exploited. 
Similarly, complete transparency about the data sources 
and algorithmic processes used may not be feasible if they 
involve proprietary information or raise legal compliance 
issues (Watson & Nations, 2019). Therefore, we propose the 
following:
Proposition 3: Balancing Transparency and Explanations with 
Liberty Protection is Inherent in RAI Enactment This proposition 
suggests that organizations need to carefully balance the imple-
mentation of RAI principles, recognizing that the presence of all 
principles may not always result in the desired outcome of RAI 
enactment. This seemingly counterintuitive finding can also be 
explained from a Rawlsian perspective: mechanisms must first 
secure basic liberties, and in that sense, security and privacy can 
be prioritized over transparency and explanations. This balance, 
and how it is exercised, is guided by specific contexts, i.e., how 
the balance is achieved may be different in one context com-
pared to another. This observation ties third proposition to the 
second proposition by further acknowledging the need to choose 
the manner in which different principles will be operationalized 
and rolled out in the organization.

75Information Systems Frontiers (2025) 28:61–87 
5.2  Practical Implications
A key challenge for enacting RAI lies in bridging the 
divide between abstract principles and practical applica-
tion (Mikalef, 2024; Mittelstadt, 2019). This study pro-
vides actionable insights for organizations striving to 
effectively enact RAI. First, the findings highlight the 
central role of accountability and safety-reliability in all 
successful configurations of RAI enactment. Organizations 
should prioritize these principles as foundational compo-
nents of their AI governance frameworks, ensuring clear 
accountability mechanisms and robust reliability meas-
ures to build trust and mitigate AI risks. Second, the study 
shows that RAI enactment does not require implementing 
all principles with equal emphasis and uniformly. Depend-
ing on the context, certain principles (such as privacy, fair -
ness, or explainability) may take precedence, while others 
may be less critical or even counterproductive in specific 
settings. This insight aligns with the recent (2024) guid-
ance issued by AI4People which states that lists of princi-
ples should always be tailored to reflect the context of use 
as it is not uncommon for some principles to have higher 
priority in certain domains than in others (AI4People, 
2024). Drawing from our findings we encourage organi-
zations to adopt a flexible, context-driven approach, tailor -
ing their RAI strategies to industry regulations, and risk 
profiles. By leveraging context-specific configurations, AI 
practitioners can develop more effective, adaptable, and 
ethically sound AI governance frameworks that maximize 
AI’s benefits while minimizing risks.
The findings also have implications for policymakers. 
The configurational approach provides insights for RAI 
policy-making by promoting the development of custom-
izable, risk-based regulatory frameworks. This has also 
been highlighted in the literature as an important concern 
(Giffen & Ludwig, 2023). Rather than applying a univer -
sal set of rules, this approach demonstrates the value of 
identifying necessary conditions and understanding how 
different combinations of principles function across varied 
contexts. This understanding allows for adaptive regula-
tory measures that can be tailored to specific industries or 
applications, focusing on configurations that best mitigate 
risks while fostering innovation. Regulators can ensure 
that essential principles are enforced without imposing 
unnecessary compliance burdens, thereby striking a bal-
ance between responsible AI deployment and promoting 
technological progress. This adaptability is key to creating 
regulatory systems that evolve alongside the rapid devel-
opments in AI technologies.
6  Conclusion
This study offers valuable insights into the enactment of 
responsible AI by identifying five distinct configurations 
of RAI principles associated with high RAI enactment 
within organizations. The findings highlight the crucial 
role of AI accountability and safety-reliability princi-
ples across configurations, emphasizing their consistent 
importance in fostering high RAI enactment. Further -
more, the study demonstrates the contextual variability of 
RAI principles, showing how their influence and relative 
importance shift depending on the context. This under -
scores the need for a nuanced, context-aware approach to 
RAI implementation, moving beyond generic checklists 
of principles. The theoretical grounding in Rawls'"justice 
as fairness"provides a robust framework for understand-
ing the interconnectedness of these principles, linking 
them to the broader concepts of liberty and equality. 
From a practical standpoint, our findings suggest that 
organizations should adopt a flexible, context-driven 
approach to RAI implementation, focusing on principle 
configurations that align with their operational and regu-
latory landscapes. Overall, our study responds to emerg-
ing scholarly calls for examining what it means to be 
responsibly digital providing insights on the enactment 
of responsible AI in practice (Recker et al., 2023; Zamani 
et al., 2024).
While the study provides significant contributions to 
the field, limitations exist, including the specific sample 
of experts and geographical focus. Future research could 
expand to include a broader range of organizations and 
locations beyond Europe and America. Furthermore, our 
sample consists primarily of organizations with relatively 
mature RAI practices. This methodological choice has 
influenced the observed co-occurrence of conditions. 
Organizations at earlier stages of RAI adoption may 
exhibit greater variation in their enactment pathways. 
Expanding the sample to include such organizations can 
provide additional insights. Further investigation into 
the specific mechanisms through which configurations 
lead to RAI enactment would also enrich the understand-
ing of this complex phenomenon. Further studies could 
also examine longitudinal changes in RAI enactment and 
investigate how emerging regulations shape the practical 
adoption of RAI principles. By deepening the empiri-
cal investigation of RAI enactment, future research can 
continue to bridge the gap between ethical AI ideals and 
real-world RAI enactment.

76 Information Systems Frontiers (2025) 28:61–87
Appendix A: Questionnaire
1. Age
2. Gender
3. What is your current job title?
4. What is your highest level of education completed?
High School Diploma or Equivalent Bachelor Master PhD
5. How many years of experience do you have?
0–1 1–3 3–5  > 5
6. In which country do you currently work?
7. Number of employees in your Organisation:
1–10 10–100 100–250 250–500  > 500
8. Industry
Finance Healthcare Energy Manufacturing Commerce Entertainment Professional 
Services
Public Services Other: specify
9.   How familiar are you with the concept of Responsible 
AI (RAI)?
Never heard about it Heard about it—
slightly familiar
Familiar but never 
involved in RAI 
practices
Very Familiar and 
some involvement 
in RAI practices
Very familiar and 
involved in RAI 
practices actively
Expert
 10. When did your organization start implementing RAI 
practices?
Have not started and have no 
plans to start soon
Have not started yet but plans to 
start within the next 12 months
Less than a year ago 1–3 3–5  > 5
The following questions relate to different tenets of 
Responsible AI. After reading the definition for each tenet, 
please respond to the associated questions.
1. For the AI-infused initiatives in our organization we view benevolence and non-maleficence as an important consideration
2. The AI-infused initiatives in our organization align with the benevolence and non-maleficence tenet
3. Benevolence and non-maleficience checks for AI-infused initiatives are implemented in our organization
4. For the AI-infused initiatives in our organization we view reliability and safety as an important consideration
5. The AI-infused initiatives in our organization align with the reliability and safety tenet
6. Implementing reliability and safety checks for AI-infused initiatives is important in our organization
7. For the AI-infused initiatives in our organization we view privacy as an important consideration
8. The AI-infused initiatives in our organization align with the privacy tenet
9. Implementing privacy checks for AI-infused initiatives is important in our organization
10. For the AI-infused initiatives in our organization we view security as an important consideration

77Information Systems Frontiers (2025) 28:61–87 
11. The AI-infused initiatives in our organization align with the security tenet
12. Implementing security checks for AI-infused initiatives is important in our organization
13. For the AI-infused initiatives in our organization we view accountability as an important consideration
14. The AI-infused initiatives in our organization align with the accountability tenet
15. Implementing accountability checks for AI-infused initiatives is important in our organization
16. For the AI-infused initiatives in our organization we view explainability as an important consideration
17. The AI-infused initiatives in our organization align with the explainability tenet
18. Implementing explainability checks for AI-infused initiatives is important in our organization
19. For the AI-infused initiatives in our organization we view intelligibility as an important consideration
20. The AI-infused initiatives in our organization align with the intelligibility tenet
21. Implementing intelligibility checks for AI-infused initiatives is important in our organization
22. For the AI-infused initiatives in our organization we view transparency as an important consideration
23. The AI-infused initiatives in our organization align with the transparency tenet
24. Implementing transparency checks for AI-infused initiatives is important in our organization
25. For the AI-infused initiatives in our organization we view inclusiveness as an important consideration
26. The AI-infused initiatives in our organization align with the inclusiveness tenet
27. Implementing inclusiveness checks for AI-infused initiatives is important in our organization
28. For the AI-infused initiatives in our organization we view fairness as an important consideration
29. The AI-infused initiatives in our organization align with the fairness tenet
30. Implementing fairness checks for AI-infused initiatives is important in our organization
Appendix B: Scale items with mean, 
standard deviation, and standardized 
loading
Construct and scale items Mean S.D Loading
Non-maleficence (CR = 0.84)
 31. For the AI-infused initiatives in our organization we view benevolence and non-maleficence as an 
important consideration
5.56 1.423 0.80
 32. The AI-infused initiatives in our organization align with the benevolence and non-maleficence tenet 5.44 1.439 0.74
 33. Benevolence and non-maleficience checks for AI-infused initiatives are implemented in our organiza-
tion
5.25 1.515 0.71
Safety-reliability (CR = 0.86)
 34. For the AI-infused initiatives in our organization we view reliability and safety as an important consid-
eration
6.04 1.078 0.81
 35. The AI-infused initiatives in our organization align with the reliability and safety tenet 5.78 1.170 0.77
 36. Implementing reliability and safety checks for AI-infused initiatives is important in our organization 5.91 1.200 0.77
Privacy (CR = 0.81)
 37. For the AI-infused initiatives in our organization we view privacy as an important consideration 6.24 1.052 0.87
 38. The AI-infused initiatives in our organization align with the privacy tenet 5.99 1.116 0.80
 39. Implementing privacy checks for AI-infused initiatives is important in our organization 5.99 1.206 0.79
Security (CR = 0.79)
 40. For the AI-infused initiatives in our organization we view security as an important consideration 6.16 1.050 0.76
 41. The AI-infused initiatives in our organization align with the security tenet 5.83 1.143 0.85
 42. Implementing security checks for AI-infused initiatives is important in our organization 5.96 1.057 0.76
Accountability (CR = 0.73)
 1. For the AI-infused initiatives in our organization we view accountability as an important consideration 5.33 1.506 0.74

78 Information Systems Frontiers (2025) 28:61–87
Construct and scale items Mean S.D Loading
 2. The AI-infused initiatives in our organization align with the accountability tenet 5.06 1.470 0.71
 3. Implementing accountability checks for AI-infused initiatives is important in our organization 5.10 1.522 0.61
Meaningful explainability (CR = 0.92)
 1. For the AI-infused initiatives in our organization we view explainability as an important consideration 5.07 1.558 0.73
 2. The AI-infused initiatives in our organization align with the explainability tenet 4.79 1.686 0.84
 3. Implementing explainability checks for AI-infused initiatives is important in our organization 4.83 1.553 0.85
 4. For the AI-infused initiatives in our organization we view intelligibility as an important consideration 4.80 1.535 0.65
 5. The AI-infused initiatives in our organization align with the intelligibility tenet 4.64 1.567 0.71
 6. Implementing intelligibility checks for AI-infused initiatives is important in our organization 4.67 1.611 0.70
Transparency (CR = 0.91)
 7. For the AI-infused initiatives in our organization we view transparency as an important consideration 4.94 1.633 0.71
 8. The AI-infused initiatives in our organization align with the transparency tenet 4.77 1.578 0.74
 9. Implementing transparency checks for AI-infused initiatives is important in our organization 4.82 1.550 0.71
Fairness (CR = 0.92)
 1. For the AI-infused initiatives in our organization we view inclusiveness as an important consideration 4.53 1.799 0.81
 2. The AI-infused initiatives in our organization align with the inclusiveness tenet 4.29 1.757 0.80
 3. Implementing inclusiveness checks for AI-infused initiatives is important in our organization 4.44 1.748 0.82
 4. For the AI-infused initiatives in our organization we view fairness as an important consideration 4.93 1.790 0.87
 5. The AI-infused initiatives in our organization align with the fairness tenet 4.65 1.768 0.84
 6. Implementing fairness checks for AI-infused initiatives is important in our organization 4.71 1.766 0.86
RAI Enactment (CR = 0.71)
 1. To what extent has your organization achieved RAI for its AI-infused initiatives? 4.32 1.847 0.75
 2. How important is RAI for your organization´s goals? 5.25 1.687 0.77
 3. How well has your organization integrated RAI into AI lifecycles? 4.29 1.749 0.72
 Scale items with mean, standard deviation, and standardized loading
CR Composite Reliability

79Information Systems Frontiers (2025) 28:61–87 
Appendix C: Truth Table & fsQCA output for Achieving RAI enactment with consistency > 0.8, PRI > 0.7   See Table 8
Table 8  Truth Table for with consistency > 0.8, PRI > 0.7
Benevolence Reliability Privacy Security AccountabilityTransparency Explainability Fairness number RAI enact-
ment
raw consist PRI consist SYM consist
1 1 1 1 1 1 1 1 25 1 0.930598 0.87437 0.891122
1 1 1 0 1 1 1 1 3 1 0.970966 0.872236 0.872236
1 1 1 1 1 0 0 1 3 1 0.948909 0.749348 0.749347
0 1 1 1 1 1 1 1 1 1 0.941209 0.742169 0.742169
1 1 1 1 1 1 1 0 1 1 0.941602 0.715294 0.715294
1 1 0 1 1 1 1 1 1 1 0.93613 0.7 0.7
1 1 1 1 1 1 0 1 2 0 0.925337 0.676408 0.676409
1 1 0 1 0 1 1 1 1 0 0.955056 0.676301 0.676301
1 0 0 0 1 1 1 1 1 0 0.946785 0.674209 0.674208
0 1 1 0 1 1 1 1 1 0 0.962885 0.662421 0.662421
1 1 1 1 0 1 0 0 1 0 0.928086 0.552817 0.552816
0 1 1 1 1 0 0 1 1 0 0.941667 0.549506 0.549505
0 0 0 0 1 1 1 1 1 0 0.921796 0.538463 0.538462
1 1 1 1 1 0 0 0 1 0 0.900307 0.474393 0.474393
1 0 0 0 1 0 1 0 1 0 0.913205 0.426471 0.426471
0 0 0 0 1 1 1 0 1 0 0.895219 0.372549 0.372549
0 0 0 0 1 0 1 0 1 0 0.883108 0.308001 0.308
1 1 1 1 0 0 0 0 1 0 0.859244 0.2493 0.2493
0 0 1 1 0 0 1 1 2 0 0.840517 0.189781 0.189781
1 1 0 0 0 0 0 0 1 0 0.822541 0.188035 0.188034
0 0 0 0 0 1 0 0 1 0 0.850271 0.180921 0.180921
1 0 0 0 0 0 0 0 1 0 0.824901 0.117479 0.122754
0 0 0 0 0 0 0 0 17 0 0.578606 0.05806 0.0604133
0 0 0 1 0 0 0 0 2 0 0.739981 0.055459 0.0554592

80 Information Systems Frontiers (2025) 28:61–87
Fig. 4  fsQCA Output for Achieving RAI enactment with consistency > 0.8, PRI > 0.65

81Information Systems Frontiers (2025) 28:61–87 
Appendix D: Sensitivity Analysis for RAI 
Enactment  see Tables 9 and 10
Table 9  Configurations for 
Achieving RAI enactment with 
consistency > 0.8, PRI > 0.65
12 34 5
Benevolence and Non-maleficence ●● ● ●
Safety-reliability ●● ●● /uni2A02
Privacy ● ● /uni2A02● /uni2A02
Security ●● ● /uni2A02
Accountability ● ● ●● ●
Transparency ●● ● ●
Explainability ● /uni2A02●● ●
Fairness ● ●● ●
Consistency 0.923 0.929 0.927 0.928 0.947
Raw coverage 0.573 0.296 0.217 0.560 0.185
Unique coverage 0.043 0.032 0.019 0.032 0.03
Overall solution consistency0 .914
Overall solution coverage ‘0.691
Black circles ( ) indicate the presence of a condition, and circles with “x” (⊗) indicate its absence. Large 
circles indicate core conditions; small ones, peripheral conditions. Blank spaces indicate “don’t care”
Table 10  Configurations for 
Achieving RAI enactment with 
consistency > 0.8, PRI > 0.60
12 34 5
Benevolence and Non-maleficence ●● ● ●
Safety-reliability ● ● ●● /uni2A02
Privacy ●● /uni2A02● /uni2A02
Security ●● ● /uni2A02
Accountability ● ● ● ●
Transparency ● ● ●
Explainability ● /uni2A02●● ●
Fairness ● ●● ●
Consistency 0.924 0.929 0.927 0.928 0.947
Raw coverage 0.576 0.296 0.217 0.560 0.185
Unique coverage 0.045 0.019 0.019 0.032 0.03
Overall solution consistency0 .915
Overall solution coverage 0.691
Black circles ( ) indicate the presence of a condition, and circles with “x” (⊗) indicate its absence. Large 
circles indicate core conditions; small ones, peripheral conditions. Blank spaces indicate “don’t care”

82 Information Systems Frontiers (2025) 28:61–87
Fig. 5  fsQCA Output for Achieving RAI enactment with consistency > 0.8, PRI > 0.7

83Information Systems Frontiers (2025) 28:61–87 
Appendix E: Results of the Predictive Validity Testing
Subsample 1_random: solution 1: results have predictive validity for others than the underlying data sample.
Plot of the model1 in the holdout sample reveals Figure. The consistency scores 0.92 (subsample1) and 0.82 
(holdout sample) as well as the coverage scores 0.57 (subsample1) and 0.58 (holdout sample) are largely 
consistent, revealing the predictive validity of the derived solution models, as well as the derived


84 Information Systems Frontiers (2025) 28:61–87
Appendix F: Follow‑up interview guideline
• Personal background
Could you tell us about your academic and professional 
background?
How long have you been part of the AI projects, and how 
long have you held your current position?
• ML and AI projects at your organization
Could you please describe the main ways your organiza-
tion utilizes artificial intelligence technologies?
Could you please describe the AI projects that you are 
involved with?
What kind of AI models are used in these projects?
• Experience of RAI principles
How do these projects in which you have been involved 
do you think are following the responsible AI principles?
a) If yes, describe how you are using them (for what pur -
pose); please explain your experience on how RAI prin-
ciples are defined in your organization.
b) b) If not but planning to employ it, why are you plan-
ning to employ such systems?
c) c) If not and no plan to employ it, why are you not 
using these principles in AI systems?
Based on your experiences, do you think some RAI prin-
ciples are more important than others in your case? How do 
you balance principles like privacy and understandability?
• Reasons for operationalizing RAI principles in organ-
izations:
Can you explain the primary motivations behind your 
organization's decision to operationalize RAI principles?
What specific benefits or goals does your organization 
aim to achieve by implementing RAI principles?
Have there been any external factors, such as regulatory 
requirements or societal expectations, influencing your 
organization's commitment to RAI principles?
• Implementation and practice in organizations
How understandable are the decisions of the AI used in 
the projects you are involved?
Have you encountered a case in which you needed to 
explain a particular AI decision?
Have these explanations been documented?
What are the practices or producers in cases explana-
tions are requested by the users, could you give concrete 
examples of these practices?
To what extent do you think the decisions made by the 
algorithms in your projects are fair?
Have you encountered a case or cases in which the AI 
decision was unfair?
what were the procedures and practices to identify and solve 
these issues?
To what extent do you think the decisions made by the algo-
rithms in your projects are following the privacy and security 
regulations?
Have you encountered a case or cases in which an AI deci-
sion put users at risk?
What kinds of risks have you encountered? Could you give 
concrete examples of them?
What were the procedures and practices to identify and 
solve these issues?
In your projects, have you encountered situations where 
RAI principles conflict with each other? For example, how do 
you handle scenarios where privacy regulations prevent from 
providing explanations (or other principles)?
Acknowledgements The contributions of the practitioners who gener-
ously shared their time, insights, and experiences participating in the 
study are gratefully acknowledged.
Authors'Contributions All authors contributed to the conception and 
design of the study, as well as the data collection, analysis, and inter -
pretation. They participated in drafting the manuscript and critically 
revising it for key intellectual content. Each author has approved the 
final version for publication and accepts responsibility for the entire 
work, ensuring that any concerns about accuracy or integrity are prop-
erly addressed and resolved.
Funding Open access funding provided by University of Agder. The 
author(s) received no financial support for the research, authorship, 
and/or publication of this article. Open access funding is provided by 
the University of Agder.
Data Availability On request due to privacy/ethical restrictions: The data 
supporting this study are available on request from the corresponding 
author. The data are not publicly available due to privacy or ethical limits.
Code Availability Not applicable.
Declarations 
Ethical Approval and Consent to Participate This research was reviewed 
and approved by the Norwegian Agency for Shared Services in Educa-
tion and Research (Sikt). All participants provided informed consent 
before they participated in the study, following Sikt’s ethical guidelines 
and regulations for the protection of personal data in research.
Consent for Publication The author(s) give their explicit consent that 
there is no requirement to obtain consent from any responsible authorities, 
as the data was collected from respondents who reflect their perspective.
Competing interest The author(s) declared no potential conflicts of inter-
est concerning the research, authorship, and/or publication of this article.

85Information Systems Frontiers (2025) 28:61–87 
Open Access This article is licensed under a Creative Commons Attri-
bution 4.0 International License, which permits use, sharing, adapta-
tion, distribution and reproduction in any medium or format, as long 
as you give appropriate credit to the original author(s) and the source, 
provide a link to the Creative Commons licence, and indicate if changes 
were made. The images or other third party material in this article are 
included in the article’s Creative Commons licence, unless indicated 
otherwise in a credit line to the material. If material is not included in 
the article’s Creative Commons licence and your intended use is not 
permitted by statutory regulation or exceeds the permitted use, you will 
need to obtain permission directly from the copyright holder. To view a 
copy of this licence, visit http://creativecommons.org/licenses/by/4.0/.
References
Advenica. (2020). Digital responsibility – the only viable way forward. 
https:// www. adven ica. com/ digit al- respo nsibi lity- only- viable- way- 
forwa rd. Accessed 15 Dec 2023.
AI4Peopl.e (2024). Towards an ethics by design approach for AI. 
https:// ai4pe ople. org/ wp- conte nt/ uploa ds/ 2024/ 06/ Towar ds- an- 
Ethics- by- Design- Appro ach- for- AI. pdf. Accessed 20 Sept 2024.
Akbarighatar, P., Pappas, I., & Vassilakopoulou, P. (2023). Practices 
for responsible AI: Findings from interviews with experts. In 
Proceedings of the Americas Conference on Information Systems 
(AMCIS).
Amugongo, L. M., Kriebitz, A., Boch, A., & Lütge, C. (2023). Opera-
tionalising AI ethics through the agile software development life-
cycle: A case study of AI-enabled mobile health applications. AI 
and Ethics. 1–18. https:// doi. org/ 10. 1007/ s43681- 023- 00331-3
Arbelaez Ossa, L., Lorenzini, G., Milford, S. R., Shaw, D., Elger, B. 
S., & Rost, M. (2024). Integrating ethics in AI development: A 
qualitative study. BMC Medical Ethics, 25(1), 10.
Ashrafian, H. (2023). Engineering a social contract: Rawlsian distribu-
tive justice through algorithmic game theory and artificial intel-
ligence. AI and Ethics, 3(4), 1447–1454.
Baygi, R. M., Introna, L. D., & Ostovar, M. (2024). Beyond catego-
ries: a flow-oriented approach to social justice on online labor 
platforms. MIS Quarterly. 48(4)
Coeckelbergh, M. (2020). AI ethics. MIT press.
Crouch, M., & McKenzie, H. (2006). The logic of small samples in 
interview-based qualitative research. Social Science Information, 
45(4), 483–499.
Czarniawska, B. (2005). Karl Weick: Concepts, style and reflection. 
The Sociological Review, 53, 267–278.
Díaz-Rodríguez, N., Del Ser, J., Coeckelbergh, M., López de Prado, M., 
Herrera-Viedma, E., & Herrera, F. (2023). Connecting the dots 
in trustworthy Artificial Intelligence: From AI principles, ethics, 
and key requirements to responsible AI systems and regulation. 
Information Fusion, 99, 101896.
Dolata, M., Feuerriegel, S., & Schwabe, G. (2022). A sociotechnical view 
of algorithmic fairness. Information Systems Journal, 32(4), 754–818.
Douglas, E. J., Shepherd, D. A., & Prentice, C. (2020). Using fuzzy-set 
qualitative comparative analysis for a finer-grained understand-
ing of entrepreneurship. Journal of Business Venturing, 35(1), 
105970. https:// doi. org/ 10. 1016/j. jbusv ent. 2019. 105970
European Commission. (2019). Ethics guidelines for trustworthy AI  
[Online]. Available: https:// digit al- strat egy. ec. europa. eu/ en/ libra 
ry/ ethics- guide lines- trust worthy- ai. Accessed 30 November 2022.
Fiss, P. C. (2007). A set-theoretic approach to organizational configura-
tions. Academy of Management Review, 32(4), 1180–1198.
Fiss, P. C. (2011). Building better causal theories: A fuzzy set approach 
to typologies in organization research. The Academy of Manage-
ment Journal, 54(2), 393–420.
Fjeld, J., Achten, N., Hilligoss, H., Nagy, A., & Srikumar, M. (2020). 
Principled artificial intelligence: Mapping consensus in ethical 
and rights-based approaches to principles for AI. Berkman Klein 
Center Research Publication, (2020-1).
Floridi, L., & Cowls, J. (2022). A unified framework of five principles 
for AI in society. In S. Carta (Ed.), Machine Learning and the City 
(pp. 535–545). Wiley.
Floridi, L., Cowls, J., Beltrametti, M., Chatila, R., Chazerand, P., Dig-
num, V., Luetge, C., Madelin, R., Pagallo, U., Rossi, F., Schafer, 
B., Valcke, P., & Vayena, E. (2018). AI4People—an ethical frame-
work for a good ai society: Opportunities, risks, principles, and 
recommendations. Minds and Machines, 28(4), 689–707.
Fornell, C., & Larcker, D. F. (1981). Evaluating structural equation 
models with unobservable variables and measurement error. Jour-
nal of Marketing Research, 18(1), 39–50.
Fry, H., (2018). Hello world: Being human in the age of algorithms. 
NewYork: WW Norton & Company.
Fukuda-Parr, S., & Gibbons, E. (2021). Emerging consensus on 
‘Ethical AI’: Human rights critique of stakeholder guidelines. 
Global Policy, 12(S6), 32–44.
Fumagalli, E., Rezaei, S., & Salomons, A. (2022). OK computer: 
Worker perceptions of algorithmic recruitment. Research Pol-
icy, 51(2), 104420.
Gabriel, I. (2022). Toward a theory of justice for artificial intelli-
gence. Daedalus, 151(2), 218–231.
Gefen, D., Straub, D., & Boudreau, M.-C. (2000). Structural equation 
modeling and regression: Guidelines for research practice. Com-
munications of the Association for Information Systems, 4(1), 7.
Georgieva, I., Lazo, C., Timan, T., & Van Veenstra, A. F. (2022). 
From AI ethics principles to data science practice: A reflection 
and a gap analysis based on recent frameworks and practical 
experience. AI and Ethics, 2, 697–711.
Ghasemaghaei, M., & Kordzadeh, N. (2024). Understanding how 
algorithmic injustice leads to making discriminatory decisions: 
An obedience to authority perspective. Information & Manage-
ment, 61(2), 103921.
Giffen, B., & Ludwig, H. (2023). How boards of directors govern 
artificial intelligence. MIS Quarterly Executive, 22(4), 7.
Gigerenzer, G., & Brighton, H. (2009). Homo heuristicus: Why 
biased minds make better inferences. Topics in Cognitive Sci-
ence, 1(1), 107–143.
Google. (2019). Responsible AI practices  [Online]. Available: 
https:// ai. google/ respo nsibi lities/ respo nsible- ai- pract ices/. 
Accessed 30 Nov 2022.
Greckhamer, T., Furnari, S., Fiss, P. C., & Aguilera, R. V. (2018). 
Studying configurations with qualitative comparative analysis: 
Best practices in strategy and organization research. Strategic 
Organization, 18(3), 482–495.
Grisot, M., & Vassilakopoulou, P. (2013). Infrastructures in health-
care: The interplay between generativity and standardiza-
tion. International Journal of Medical Informatics, 82(5), 
e170–e179.
Hair, J. F., Anderson, R. E., Tatham, R. L., & Black, W. C. (1998). Mul-
tivariate data analysis. Prentice-Hall. Upper Saddle River, NJ, 730.
Ho, C. W. L., Soon, D., Caals, K., & Kapur, J. (2019). Governance of 
automated image analysis and artificial intelligence analytics in 
healthcare. Clinical Radiology, 74(5), 329–337.
Hoffmann, A. L. (2017). Beyond distributions and primary goods: 
Assessing applications of rawls in information science and tech-
nology literature since 1990. Journal of the Association for Infor-
mation Science and Technology, 68(7), 1601–1618.
IBM. (2020). AI ethics (IBM’s multidisciplinary, multidimensional 
approach helping advance responsible AI) [Online]. Available: 
https:// www. ibm. com/ artifi  cial- intel ligen ce/ ethics. Accessed 30 
November 2022.

86 Information Systems Frontiers (2025) 28:61–87
ISO:22989. (2022). ISO/IEC 22989:2022 information technology 
— artificial intelligence — artificial intelligence concepts and 
terminology.
ISO:24028. (2020). ISO/IEC TR 24028:2020 information technology 
— artificial intelligence — overview of trustworthiness in arti-
ficial intelligence. Retrieved from https:// www. iso. org/ stand ard/ 
77608. html. Accessed 15 Dec 2023.
Jobin, A., Ienca, M., & Vayena, E. (2019). The global landscape of AI 
ethics guidelines. Nature Machine Intelligence, 1(9), 389–399.
Katz, D., & Kahn, R.L. (1978). The social psychology of organizations. 
In Organizational behavior 2, pp. 152–168. Routledge.
Leben, D. (2017). A Rawlsian algorithm for autonomous vehicles. Eth-
ics and Information Technology, 19(2), 107–115.
Mäntymäki, M., Minkkinen, M., Birkstedt, T., & Viljanen, M. 
(2022). Defining organizational AI governance. AI and Ethics,  
2, 603–609.
Mateen, H. (2018). Weapons of math destruction: “How Big Data 
Increases Inequality and Threatens Democracy.” Berkeley Journal 
of Employment and Labor Law, 39(1), 285–292.
Mattke, J., Maier, C., Weitzel, T., Gerow, J. E., & Thatcher, J. B. (2022). 
Qualitative comparative analysis (QCA) in information systems 
research: Status quo, guidelines, and future directions. Communi-
cations of the Association for Information Systems, 50(1), 8.
Microsoft. (2020). Responsible AI (policies, practices, and tools that 
make up a framework for Responsible AI by Design) [Online]. 
Available: https:// www. micro soft. com/ en- us/ ai/ respo nsible- ai. 
Accessed 30 November 2022.
Mikalef, P. (2024). Responsible AI governance: From ideation to 
implementation. In I. Constantiou, M. P. Joshi, & M. Stelmaszak 
(Eds.), Research Handbook on Artificial Intelligence and Decision 
Making in Organizations (pp. 126–142). Edward Elgar Publishing.
Mikalef, P., Conboy, K., Lundström, J. E., & Popovič, A. (2022). 
Thinking responsibly about responsible AI and ‘the dark side’of 
AI. European Journal of Information Systems, 31, 257–268.
Misangyi, V. F., Greckhamer, T., Furnari, S., Fiss, P. C., Crilly, D., & 
Aguilera, R. (2017). Embracing causal complexity: The emer -
gence of a neo-configurational perspective. Journal of Manage-
ment, 43(1), 255–282.
Mittelstadt, B. (2019). Principles alone cannot guarantee ethical AI. 
Nature Machine Intelligence, 1(11), 501–507.
Mökander, J., Morley, J., Taddeo, M., & Floridi, L. (2021). Ethics-
based auditing of automated decision-making systems: Nature, 
scope, and limitations. Science and Engineering Ethics, 27(4), 44.
Morley, J., Elhalal, A., Garcia, F., Kinsey, L., Mökander, J., & Floridi, 
L. (2021). Ethics as a service: A pragmatic operationalisation of 
AI ethics. Minds and Machines, 31(2), 239–256.
Munn, L. (2023). The uselessness of AI ethics. AI and Ethics, 3(3), 
869–877.
OECD. (2024). Artificial intelligence principles [Online]. Available: 
https:// oecd. ai/ en/ ai- princ iples. Accessed 30 November 2024.
Orlikowski, W. & Yates, J. (1999). It's about time: An enacted view of 
time in organizations. MIT sloan school of management, Cam-
bridge, MA, Working Paper 4055.
Papagiannidis, E., Mikalef, P., & Conboy, K. (2025). Responsible arti-
ficial intelligence governance: A review and research framework. 
The Journal of Strategic Information Systems, 34, 101885.
Pappas, I. O., & Woodside, A. G. (2021). Fuzzy-set Qualitative com-
parative analysis (fsQCA): Guidelines for research practice in 
information systems and marketing. International Journal of 
Information Management, 58, 102310.
Pappas, I. O., Kourouthanassis, P. E., Giannakos, M. N., & Chris-
sikopoulos, V. (2016). Explaining online shopping behavior with 
fsQCA: The role of cognitive and affective perceptions. Journal 
of Business Research, 69(2), 794–803.
Park, Y., & Mithas, S. (2020). Organized complexity of digital business 
strategy: A configurational perspective. MIS Quarterly, 44(1), 85–127.
PWC. (2020). Digital ethics – operation, values and attitudes for a digi-
tal world. https:// www. pwc. de/ en/ consu lting/ 42013_ WP_ Digit al_ 
Ethics_ EN_ neu_ 200401_ SCREEN_ GESCH UETZT% 20(2). pdf. 
Accessed 15 Jan 2022.
Ragin, C. C., & Sonnett, J. (2005). Between complexity and parsimony: 
Limited diversity, counterfactual cases, and comparative analysis. 
In S. Kropp & M. Minkenberg (Eds.), Vergleichen in der Politik-
wissenschaft (pp. 180–197). VS Verlag für Sozialwissenschaften.
Ragin, C. C. (2000). Fuzzy-set social science. Chicago, IL: University 
of Chicago Press.
Ragin, C. C. (2008). Redesigning social inquiry: Fuzzy sets and 
beyond. Chicago: University of Chicago Press.
Rakova, B., Yang, J., Cramer, H., & Chowdhury, R. (2021). Where 
responsible AI meets reality: Practitioner perspectives on enablers 
for shifting organizational practices. Proceedings of the ACM on 
Human-Computer Interaction, 5(CSCW1), 1–23.
Rawls, J. (1999). A theory of justice: Revised edition. Harvard Uni-
versity Press.
Rawls, J. (2001). The law of peoples: With “The Idea of Public Reason 
Revisited.” Harvard University Press
Recker, J., Chatterjee, S., Sundermeier, J., & Tarafdar, M. (2023). Digi-
tal responsibility: Social, ethical, and ecological implications of 
IS. Journal of the Association for Information Systems.
Ribes, D., & Finholt, T. (2009). The long now of technology infra-
structure: Articulating tensions in development. Journal of the 
Association for Information Systems, 10(5), 375–398.
Rinta-Kahila, T., Someh, I., Gillespie, N., Indulska, M., & Gregor, S. 
(2022). Algorithmic decision-making and system destructiveness: 
A case of automatic debt recovery. European Journal of Informa-
tion Systems, 31(3), 313–338.
Sadek, M., Kallina, E., Bohné, T., Mougenot, C., Calvo, R. A., & 
Cave, S. (2024). Challenges of responsible AI in practice: Scop-
ing review and recommended actions. AI & Society, 1–17.
Schneider, C. Q., & Wagemann, C. (2012). Set theoretic methods for 
the social sciences: A guide to qualitative comparative analysis.  
Cambridge University Press.
Slager, R., Gond, J., & Crilly, D. (2021). Reactivity to sustainability 
metrics: A configurational study of motivation and capacity. Busi-
ness Ethics Quarterly, 31(2), 275–307.
Soltani Delgosha, M., Hajiheydari, N., & Olya, H. (2024). A per -
son‐centred view of citizen participation in civic crowdfunding 
platforms: A mixed‐methods study of civic backers. Information 
Systems Journal, 34(5), 1626–1663.
US General Services Administration. (2022). Responsible and trust -
worthy AI implementation [Online]. Available: https:// coe. gsa.  
gov/ coe/ ai- guide- for- gover nment/ respo nsible- ai- imple menta tion/ 
index. html. Accessed 30 November 2022.
Vassilakopoulou, P., Parmiggiani, E., Shollo, A., & Grisot, M. (2022). 
Responsible AI: Concepts, critical perspectives and an Informa-
tion Systems research agenda. Scandinavian Journal of Informa-
tion Systems, 34, 3.
Venkatesh, V., Brown, S. A., & Bala, H. (2013). Bridging the qualita-
tive-quantitative divide: Guidelines for conducting mixed methods 
research in information systems. MIS Quarterly, 37(1), 21–54.
Wall, L. D. (2018). Some financial regulatory implications of artificial 
intelligence. Journal of Economics and Business, 100, 55–63.
Watson, H., & Nations, C. (2019). Addressing the growing need for 
algorithmic transparency. Communications of the Association for 
Information Systems, 45(1), 26.
Weick, K. E. (2000). Making sense of the organization, John Wiley 
& Sons.

87Information Systems Frontiers (2025) 28:61–87 
Woodside, A. G. (2014). Embrace perform model: Complexity theory, 
contrarian case analysis, and multiple realities. Journal of Busi-
ness Research, 67 (12), 2495–2503.
Zamani, E., Angelopoulos, S., & Conboy, K. (2024). Information sys-
tems frontier special issue on: Being responsibly digital. Springer. 
https://  link. sprin ger. com/ colle ctions/  gaihd bdhjg. Accessed 15 
Aug 2024.
Publisher's Note Springer Nature remains neutral with regard to 
jurisdictional claims in published maps and institutional affiliations.
Pouria Akbarighatar is a PhD research fellow in information systems at 
the University of Agder, Norway. His research focuses on operational-
izing Responsible AI, data-driven decision-making, and data science. 
Before starting his PhD, he spent seven years as a data scientist in the 
telecommunications industry. His work emphasizes the importance 
of integrating responsible AI principles into organizations’ practices. 
Pouria has been published in peer-reviewed journals such as Decision 
Support Systems, Expert Systems with Applications, International 
Journal of Information Management Data Insights, and AI Ethics.
Ilias O. Pappas is Professor of Information Systems, holding positions 
in the Department of Computer Science at the Norwegian University of 
Science and Technology and the Department of Information Systems at 
the University of Agder, both in Norway. His current research activities 
focus on Human-Centered AI (HCAI). Dr. Pappas has actively con-
tributed to the areas of data science and digital transformation, social 
innovation and change, user experience across various contexts, digital 
marketing, e-services, and information technology adoption. He has 
a key interest in fuzzy-set qualitative comparative analysis (fsQCA) 
applications. He has published more than 150 articles in peer-reviewed 
journals and conferences, including the Information Systems Journal, 
European Journal of Information Systems, Human Relations, British 
Journal of Management, European Journal of Marketing, Information 
& Management, Journal of Business Research, Psychology & Market-
ing, and Journal of Systems and Software. Dr. Pappas has served as 
a guest editor for multiple journals, as an associate editor for several 
information systems journals, and is both an ERCIM “Alain Bensous-
san” fellow and a Marie Skłodowska-Curie fellow.
Sandeep Purao is a Trustee Professor in the Information and Process 
Management Group and and Director of the Entrepreneurship Eco-
system Initiative at Bentley University. His current research focuses 
on the design and evaluation of digital solutions for complex societal 
problems. His work has been published in MIS Quarterly, Information 
Systems Research, Journal of MIS, ACM Computing Surveys, ACM 
Transactions, Journal of the Medical Internet Research and others, and 
funded by federal agencies, private foundations, and industry consor -
tia. He holds a Ph.D. in Management Information Systems from the 
University of Wisconsin-Milwaukee.
Polyxeni Vassilakopoulou Polyxeni Vassilakopoulou  is a Profes-
sor in Information Systems at the University of Agder. Her research 
focuses on the transformative potential of digital technology, the impli-
cations for work, organizations, and societies and the design of digital 
technology-enabled interventions. Her current research activities are 
within the areas of human-centered AI and the dynamics and govern-
ance of data-intensive digital infrastructures. Prior to joining academia, 
she worked in management consulting for over a decade. Her research 
has been published in leading journals including Information Systems 
Journal, European Journal of Information Systems, Information and 
Organization, Journal of Strategic Information Systems, Communica-
tions of the Association for Information Systems, Journal for Computer 
Supported Collaborative Work.
```
