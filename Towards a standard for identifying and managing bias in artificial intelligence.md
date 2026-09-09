---
title: Towards a standard for identifying and managing bias in artificial intelligence
author: Reva Schwartz, Apostol Vassilev, Kristen Greene, Lori Perine, Andrew Burt, Patrick Hall
year: "2022"
Type: Report
DOI: 10.6028/nist.sp.1270
source: https://doi.org/10.6028/nist.sp.1270
created: 2026-08-05
description: As individuals and communities interact in and with an environment that is increasingly virtual they are often vulnerable to the commodification of their digital exhaust. Concepts and behavior that are ambiguous in nature are captured in this environment, quantified, and used to categorize, sort, recommend, or make decisions about people's lives. While many organizations seek to utilize this infor
tags:
  - themes/bias
  - themes/ethics
  - tech/AI
  - Tech/standard
  - design/socio-technical
  - op/acc/done
pdfORepub: "[[Towards a standard for identifying and managing bias in artificial intelligence.pdf]]"
---
[[Towards a standard for identifying and managing bias in artificial intelligence.pdf]]

> **Abstract:** As individuals and communities interact in and with an environment that is increasingly virtual they are often vulnerable to the commodification of their digital exhaust. Concepts and behavior that are ambiguous in nature are captured in this environment, quantified, and used to categorize, sort, recommend, or make decisions about people's lives. While many organizations seek to utilize this infor

## Full text (extracted from `Towards a standard for identifying and managing bias in artificial intelligence.pdf`)

*Source:* `2PDF/Towards a standard for identifying and managing bias in artificial intelligence.pdf`  
*Extracted:* 2026-08-05

```text
NIST Special Publication 1270
Towards a Standard for Identifying and
Managing Bias in Artificial Intelligence
Reva Schwartz
Apostol Vassilev
Kristen Greene
Lori Perine
Andrew Burt
Patrick Hall
This publication is available free of charge from:
https://doi.org/10.6028/NIST.SP.1270

NIST Special Publication 1270
Reva Schwartz
National Institute of Standards and Technology
Information Technology Laboratory
Apostol Vassilev
National Institute of Standards and Technology
Information Technology Laboratory
Computer Security Division
Kristen Greene
National Institute of Standards and Technology
Information Technology Laboratory
Information Access Division
Lori Perine
National Institute of Standards and Technology
Information Technology Laboratory
& The University of Maryland
Andrew Burt
Patrick Hall
BNH.AI
This publication is available free of charge from: 
https://doi.org/10.6028/NIST.SP.1270
U.S. Department of Commerce
Gina M. Raimondo, Secretary
National Institute of Standards and Technology
James K. Olthoff, Performing the Non-Exclusive Functions and Duties of the Under Secretary of Commerce
for Standards and Technology & Director, National Institute of Standards and Technology
Towards a Standard for Identifying and
Managing Bias in Artificial Intelligence
March 2022
Certain commercial entities, equipment, or materials may be identified in this document in order to describe
an experimental procedure or concept adequately. Such identification is not intended to imply
recommendation or endorsement by the National Institute of Standards and Technology, nor is it intended to
imply that the entities, materials, or equipment are necessarily the best available for the purpose.
National Institute of Standards and Technology Special Publication 1270 
Natl. Inst. Stand. Technol. Spec. Publ. 1270, 86 pages (March 2022) 
CODEN: NSPUE2
This publication is available free of charge from:
https://doi.org/10.6028/NIST.SP.1270
Executive Summary
As individuals and communities interact in and with an environment that is increasingly
virtual, they are often vulnerable to the commodification of their digital footprint. Concepts
and behavior that are ambiguous in nature are captured in this environment, quantified,
and used to categorize, sort, recommend, or make decisions about people’s lives. While
many organizations seek to utilize this information in a responsible manner, biases remain
endemic across technology processes and can lead to harmful impacts regardless of intent.
These harmful outcomes, even if inadvertent, create significant challenges for cultivating
public trust in artificial intelligence (AI).
While there are many approaches for ensuring the technology we use every day is
safe and secure, there are factors specific to AI that require new perspectives. AI sys-
tems are often placed in contexts where they can have the most impact. Whether that
impact is helpful or harmful is a fundamental question in the area of Trustworthy and
Responsible AI. Harmful impacts stemming from AI are not just at the individual or en-
terprise level, but are able to ripple into the broader society. The scale of damage, and
the speed at which it can be perpetrated by AI applications or through the extension of
large machine learning MODEL s across domains and industries requires concerted effort.
Fig. 1. The challenge of managing AI bias
Current attempts for addressing the
harmful effects of AI bias remain focused
on computational factors such as rep-
resentativeness of datasets and fairness
of machine learning algorithms. These
remedies are vital for mitigating bias,
and more work remains. Yet, as illus-
trated in Fig. 1, human and systemic in-
stitutional and societal factors are sig-
nificant sources of AI bias as well, and
are currently overlooked. Successfully
meeting this challenge will require tak-
ing all forms of bias into account. This
means expanding our perspective beyond
the machine learning pipeline to recog-
nize and investigate how this technology
is both created within and impacts our so-
ciety.
Trustworthy and Responsible AI is not just about whether a given AI system is biased,
fair or ethical, but whether it does what is claimed. Many practices exist for responsibly
producing AI. The importance of transparency, datasets, and test, evaluation, validation,
and verification (TEVV) cannot be overstated. Human factors such as participatory design
techniques and multi-stakeholder approaches, and a human-in-the-loop are also important
for mitigating risks related to AI bias. However none of these practices individually or in
i/77
concert are a panacea against bias and each brings its own set of pitfalls. What is miss-
ing from current remedies is guidance from a broader SOCIO -TECHNICAL perspective that
connects these practices to societal values. Experts in the area of Trustworthy and Respon-
sible AI counsel that to successfully manage the risks of AI bias we must operationalize
these values and create new norms around how AI is built and deployed. This document,
and work by the National Institute of Standards and Technology (NIST) in the area of AI
bias, is based on a socio-technical perspective.
The intent of this document is to surface the salient issues in the challenging area of
AI bias, and to provide a first step on the roadmap for developing detailed socio-technical
guidance for identifying and managing AI bias. Specifically, this special publication:
• describes the stakes and challenge of bias in artificial intelligence and provides ex-
amples of how and why it can chip away at public trust;
• identifies three categories of bias in AI — systemic, statistical, and human — and
describes how and where they contribute to harms; #themes/bias/data 
• describes three broad challenges for mitigating bias — datasets, testing and eval-
uation, and human factors — and introduces preliminary guidance for addressing
them.
Bias is neither new nor unique to AI and it is not possible to achieve zero risk of bias in an
AI system. NIST intends to develop methods for increasing assurance, GOVERNANCE and
practice improvements for identifying, understanding, measuring, managing, and reducing
bias. To reach this goal, techniques are needed that are flexible, can be applied across con-
texts regardless of industry, and are easily communicated to different stakeholder groups.
To contribute to the growth of this burgeoning topic area, NIST will continue its work in
measuring and evaluating computational biases, and seeks to create a hub for evaluating
socio-technical factors. This will include development of formal guidance and standards,
supporting standards development activities such as workshops and public comment pe-
riods for draft documents, and ongoing discussion of these topics with the stakeholder
community.
Key words
bias, trustworthiness, AI safety, AI lifecycle, AI development
ii/77
Acknowledgments
The authors wish to thank everyone who responded to our call and submitted comments
to the draft version of this paper. The received comments and suggested references were
essential for improving the paper and the future direction of this work. We also want to
thank the many people who assisted with the updating of the document, including our NIST
colleagues, and other reviewers who took the time to provide their constructive feedback.
We thank Kyle Fox for his insightful comments, discussions, and invaluable input.
Audience
The intended primary audience for this document includes individuals and groups who are
responsible for designing, developing, deploying, evaluating, and governing AI systems.
The document is informed and motivated by segments of the public who experience poten-
tial harm or inequities due to bias in AI systems, or are affected by biases that are newly
introduced or amplified by AI systems.
Background
This document is a result of an extensive literature review, conversations with experts from
the areas of AI bias, fairness, and socio-technical systems, a workshop on AI bias, 1 and
public comments on the draft version. 2 Insights derived from the public comments have
been integrated throughout this document. An overview and analysis of themes from the
public comments will be posted. 3 Intermediate follow-on work to this publication will
include development of formal guidance for assessing and managing the risks of AI bias,
and a series of public workshops to discuss these topics with the stakeholder community
and build consensus.
Trademark Information
All trademarks and registered trademarks belong to their respective organizations.
NIST Special Publications
The National Institute of Standards and Technology (NIST) promotes U.S. innovation and
industrial competitiveness by advancing measurement science, standards, and technology
in ways that enhance economic security and improve our quality of life. Among its broad
range of activities, NIST contributes to the research, standards, evaluations, and data re-
quired to advance the development, use, and assurance of trustworthy artificial intelligence
(AI).
1For more information about this workshop see https://www.nist.gov/news-events/events/2020/08/bias-ai-
workshop.
2Public comments are available at https://www.nist.gov/artificial-intelligence/comments-received-proposal-
identifying-and-managing-bias-artificial.
3Updated information for all of these resources can be found on the NIST AI Bias webpage, located at
https://www.nist.gov/artificial-intelligence/ai-fundamental-research-free-bias.
iii/77
The Information Technology Laboratory (ITL) at NIST develops tests, test methods,
reference data, proof of concept implementations, and technical analyses to advance the de-
velopment and productive use of information technology. ITL’s responsibilities include the
development of management, administrative, technical, and physical standards and guide-
lines.
This special publication focuses on addressing and managing risks associated with bias
in the design, development, and use of AI. It is one of a series of documents and workshops
related to the NIST AI Risk Management Framework (AI RMF) and is intended to advance
the trustworthiness of AI technologies. As with other documents in the AI RMF series,
this publication provides reference information and technical guidance on terminology,
processes and procedures, and test and evaluation, validation, and verification (TEVV).
While practical guidance4 published by NIST may serve as an informative reference, this
guidance remains voluntary.
The content of this document reflects recommended practices. This document is not
intended to serve as or supersede existing regulations, laws, or other mandatory guidance.
4The term ’practice guide,’ ’guide,’ ’guidance’ or the like, in the context of this paper, is a consensus-created,
informative reference intended for voluntary use; it should not be interpreted as equal to the use of the term
’guidance’ in a legal or regulatory context.” This document does not establish any legal standard or any other
legal requirement or defense under any law, nor have the force or effect of law.
iv/77
How to read this document
Section 1 lays out the purpose and scope of NIST’s work in AI bias. Section 2 describes
three categories of bias and how they may occur in the commission, design, development,
and deployment of AI technologies that can be used to generate predictions, recommenda-
tions, or decisions (such as the use of algorithmic decision systems), and how AI systems
may impact individuals and communities or create broader societal harms. Section 3 de-
scribes the challenge of bias related to three core areas: datasets; test, evaluation, validation
and verification; and human factors, and provides general guidance for managing AI bias
in each of those areas.
This document uses terms such as AI technology, AI system, and AI applications inter-
changeably. Terms related to the machine learning pipeline, such as AI model or algorithm
are also used in this document interchangeably. Depending on context, when the term
“system” is used it may refer to the broader organizational and/or social ecosystem within
which the technology was designed, developed, deployed, and used, instead of the more
traditional use related to computational hardware or software.
Important reading notes:
• The document includes a series of vignettes, shown in red callout boxes, to help
exemplify how and why AI bias can reduce public trust. Interesting nuances/aspects
are highlighted in blue callout boxes, important takeaways are shown as framed text.
• Terms that are displayed as small caps in the text are defined in the G LOSSARY .
Clicking on a word shown in small caps, e.g. MODEL , takes the reader directly to the
definition of that term in the Glossary. From there, one may click on a page number
shown at the end of the definition to return.
• March 24, 2022 update: the following changes are introduced with respect to the
original version of this document published on March 15, 2022:
– Fixed typos in the text of Fig. 5 and Fig. 7.
– Removed duplicates and fixed poorly formatted entries in the References.
– Corrected a statement in the text of VIGNETTE on p.7 regarding the work cited
in [36].
v/77
Contents
1 Purpose and Scope 1
2 AI Bias: Context and Terminology 3
2.1 Characterizing AI bias 3
2.1.1 Contexts for addressing AI bias 3
2.1.2 Categories of AI bias 6
2.2 How AI bias contributes to harms 9
2.3 A Socio-technical Systems Approach 10
2.4 An Updated AI Lifecycle 12
3 AI Bias: Challenges and Guidance 14
3.1 Who is Counted? Datasets in AI Bias 15
3.1.1 Dataset Challenges 15
3.1.2 Dataset Guidance 17
3.2 How do we know what is right? TEVV Considerations for AI Bias 20
3.2.1 TEVV Challenges 20
3.2.2 TEVV Guidance 27
3.3 Who makes decisions and how do they make them? Human Factors in AI
Bias 32
3.3.1 Human Factors Challenges 32
3.3.2 Human Factors Guidance 35
3.4 How do we manage and provide oversight? Governance and AI Bias 42
3.4.1 Governance Guidance 42
4 Conclusions 47
5 Glossary 49
List of Figures
Fig. 1 The challenge of managing AI bias i
Fig. 2 Categories of AI Bias. The leaf node terms in each subcategory in the picture
are hyperlinked to the GLOSSARY . Clicking them will bring up the definition
in the Glossary. To return, click on the current page number (8) printed right
after the glossary definition. 8
Fig. 3 The AI Development Lifecycle 13
Fig. 4 The output of an AI system altered by background content. 24
Fig. 5 How biases contribute to harms 27
Fig. 6 Human-centered Design Process [ISO 9241-210:2019] 40
Fig. 7 Human-centered Design Process for AI Systems 41
vi
1. Purpose and Scope
In August 2019, fulfilling an assignment in an Executive Order on AI, 5 NIST released “A
Plan for Federal Engagement in Developing Technical Standards and Related Tools” [1].
Based on broad public and private sector input, this plan recommended a deeper, more
consistent, and long-term engagement in AI standards “to help the United States to speed
the pace of reliable, robust, and trustworthy AI technology development.” NIST research
in AI continues along this path to focus on how to measure, evaluate, and enhance the
trustworthiness of AI systems and the responsible practices for designing, developing, and
deploying such systems. Working with the AI community, NIST has identified the follow-
ing technical and socio-technical characteristics needed to cultivate trust in AI systems:
accuracy, explainability and interpretability, privacy, reliability, robustness, safety, and se-
curity resilience—and that harmful biases are mitigated or controlled.
While AI has significant potential as a transformative technology, it also poses inher-
ent risks. Since trust and risk are closely related, NIST’s work in the area of trustworthy
and responsible AI centers around development of a voluntary Risk Management Frame-
work (RMF). The unique challenges of AI require a deeper understanding of how AI risks
differ from other domains. The NIST AI RMF is intended to address risks in the de-
sign, development, use, and evaluation of AI products, services, and systems for such tasks
as recommendation, diagnosis, pattern recognition, and automated planning and decision-
making. The framework is intended to enable the development and use of AI in ways that
will increase trustworthiness, advance usefulness, and address potential harms. NIST is
leveraging a multi-stakeholder approach to creating and maintaining actionable practice
guides via the RMF that is broadly adoptable.
AI risk management
AI risk management seeks to minimize anticipated and emergent negative impacts of AI
systems, including threats to civil liberties and rights. One of those risks is bias. Bias exists
in many forms, is omnipresent in society, and can become ingrained in the automated
systems that help make decisions about our lives. While bias is not always a negative
phenomenon, certain biases exhibited in AI models and systems can perpetuate and amplify
negative impacts on individuals, organizations, and society. These biases can also indirectly
reduce public trust in AI. There is no shortage of examples where bias in some aspect of
AI technology and its use has caused harm and negatively impacted lives, such as in hiring,
[2–7] health care, [8–17] and criminal justice [18–30]. Indeed, there are many instances
in which the deployment of AI technologies have been accompanied by concerns about
whether and how societal biases are being perpetuated or amplified [31–46].
Public perspectives
Depending on the application, most Americans are likely to be unaware of when they are
5Exec. Order No. 13,859, 84 Fed. Reg. 3,967 (Feb. 11, 2019), https://www.federalregister.gov/documents/
2019/02/14/2019-02544/maitaining-american-leadership-in-artificial-intelligence.
1/77
interacting with AI enabled technology [47]. However, there is a general view that there
needs to be a “higher ethical standard” for AI than for other forms of technology [48]. This
mainly stems from the perceptions and fears about loss of control and privacy [46, 49–51].
Bias is tightly associated with the concepts of transparency and fairness in society. For
much of the public, the assumptions underlying algorithms are rarely transparent. The com-
plex web of code and decisions that went into the design, development, and deployment of
AI rarely is easily accessible or understandable to non-technical audiences. Nevertheless,
many people are affected by—or their data is used as inputs for—AI technologies and sys-
tems without their consent, such as when they apply to college, [52] for a new apartment,
[53] or search the internet. When individuals feel that they are not being fairly judged
when applying for jobs [2–5, 7, 54–56] or loans [57–59] it can reduce public trust in AI
technology [60, 61].
When an end user is presented with information online that stigmatizes them based
on their race, age, or gender, or doesn’t accurately perceive their identity, it causes harm
[34, 36, 37, 41]. Consumers can be impacted by price gouging practices resulting from an
AI application, even when it is not used to make decisions directly affecting that individual
[43].
2/77
2. AI Bias: Context and Terminology
For purposes of this publication, the term Artificial Intelligence (AI) refers to a large class
of software-based systems that receive signals from the environment and take actions that
affect that environment by generating outputs such as content, predictions, recommenda-
tions, classifications, or decisions influencing the environments they interact with, among
other outputs [62]. Machine learning (ML) refers more specifically to the “field of study
that gives computers the ability to learn without being explicitly programmed,” [63] or to
computer programs that utilize data to learn and apply patterns or discern statistical rela-
tionships. Common ML approaches include, but are not limited to, regression, random
forests, support vector machines, and artificial neural networks. ML programs may or may
not be used to make predictions of future events. ML programs also may be used to create
input for additional ML programs. AI includes ML within its scope.
While AI holds great promise, the convenience of automated classification and discov-
ery within large datasets can come with significant downsides to individuals and society
through the amplification of existing biases. Bias can be introduced purposefully or inad-
vertently into an AI system, or it can emerge as the AI is used in an application. Some
types of AI bias are purposeful and beneficial. For example, the ML systems that underlie
AI applications often model our implicit biases with the intent of creating positive expe-
riences for online shopping or identifying content of interest [64, 65]. The proliferation
of recommender systems and other modeling and predictive approaches has also helped to
expose the many negative social biases baked into these processes, which can reduce public
trust [66–69].
AI is neither built nor deployed in a vacuum, sealed off from societal realities of dis-
crimination or unfair practices. Understanding AI as a socio-technical system acknowl-
edges that the processes used to develop technology are more than their mathematical and
computational constructs. A socio-technical approach to AI takes into account the val-
ues and behavior modeled from the datasets, the humans who interact with them, and the
complex organizational factors that go into their commission, design, development, and
ultimate deployment.
2.1 Characterizing AI bias
2.1.1 Contexts for addressing AI bias
Statistical context
In technical systems, bias is most commonly understood and treated as a statistical phe-
nomenon. Bias is an effect that deprives a statistical result of representativeness by system-
atically distorting it, as distinct from a random error, which may distort on any one occasion
but balances out on the average [70]. The International Organization for Standardization
(ISO) defines bias more generally as: “the degree to which a reference value deviates from
the truth”[71]. In this context, an AI system is said to be biased when it exhibits system-
atically inaccurate behavior. This statistical perspective does not sufficiently encompass or
3/77
communicate the full spectrum of risks posed by bias in AI systems.
Legal context
This section was developed in response to public comments. Stakeholder feedback noted
that the discussion of bias in AI could not be divorced from the treatment of bias in the
U.S. legal system and how it relates to laws and regulations addressing discrimination and
fairness, especially in the areas of consumer finance, housing, and employment. 6,7 There
currently is no uniformly applied approach among the regulators and courts to measuring
impermissible bias in all such areas. Impermissible discriminatory bias generally is defined
by the courts as either consisting of disparate treatment, broadly defined as a decision that
treats an individual less favorably than similarly situated individuals because of a protected
characteristic such as race, sex, or other trait, or as disparate impact, which is broadly
defined as a facially neutral policy or practice that disproportionately harms a group based
on a protected trait.8
This section is presented not as legal guidance, rather as a
reminder for developers, deployers, and users of AI that they
must be cognizant of legal considerations in their work, par-
ticularly with regard to bias testing. This section provides
basic background understanding of some of the many ways
bias is treated in some federal laws.
As it relates to disparate impact, courts and regulators have utilized or considered as
acceptable various statistical tests to evaluate evidence of disparate impact. Traditional
methods of statistical bias testing look at differences in predictions across protected classes,
such as race or sex. In particular, courts have looked to statistical significance testing to
assess whether the challenged practice likely caused the disparity and was not the result of
chance or a nondiscriminatory factor.9
6Many laws, at the federal, state and even municipal levels focus on preventing discrimination in a host of
areas. See e.g. Title VII of the Civil Rights Act, regarding discrimination on the basis of sex, religion,
race, color, or national origin in employment, the Equal Credit Opportunity Act, focused, broadly, on dis-
crimination in finance, the Fair Housing Act, focused on discrimination in housing, and the Americans with
Disabilities Act, focused on discrimination related to disabilities, among others. Other federal agencies,
including the U.S. Equal Employment Opportunity Commission, the Federal Trade Commission, the U.S.
Department of Justice, and the Office Federal Contract Compliance Programs are responsible for enforce-
ment and interpretation of these laws.
7Note that the analysis in this section is not intended to serve as a fully comprehensive discussion of the law,
how it has been interpreted by the courts, or how it is enforced by regulatory agencies, but rather to provide
an initial high-level overview.
8See 42 U.S.C. 2000e-2(a) (2018) and 42 U.S.C. 2000e-2(k) (2018), respectively.
9The Uniform Guidelines on Employment Selection Procedures (UGESP) state “[a] selection rate for any
race, sex, or ethnic group which is less than four-fifths ( 4/5ths) (or eighty percent) of the rate for the group
4/77
It is important to note, however, that the tests used to measure bias are not applied
uniformly within the legal context. In particular, federal circuit courts are split on whether
to require a plaintiff to demonstrate both statistical and practical significance to make out
a case of disparate impact. Some decisions have expressly rejected practical significance
tests in recent years while others have continued to endorse their utility. This split illustrates
that while the legal context provides several examples of how bias and fairness has been
quantified and adjudicated over the last several decades, the relevant standards are still
evolving.
It is also important to note that critical differences exist between traditional disparate
impact analyses described above and illegal discrimination as it relates to people with dis-
abilities, particularly under the Americans with Disabilities Act (ADA). Claims under the
ADA are frequently construed as “screen out” rather than as “disparate impact” claims.
”Screen out” may occur when an individual with a disability performs poorly on an evalua-
tion or assessment, or is otherwise unable to meet an employer’s job requirements, because
of a disability and the individual loses a job opportunity as a result. In addition, the ADA’s
prohibition against denial of reasonable accommodation, for example, may require an em-
ployer to change processes or procedures to enable a particular individual with a disability
to apply for a job, perform a job, or enjoy the benefits and privileges of employment. Such
disability-related protections are particularly important to AI systems because testing an
algorithm for bias by determining whether such groups perform equally well may fail to
detect certain kinds of bias. Likewise, eliminating group discrepancies will not necessarily
prevent screen out or the need for reasonable accommodation in such systems.
Cognitive and societal context
The teams involved in AI system design and development bring their cognitive biases, both
individual and group, into the process [72]. Bias is prevalent in the assumptions about
which data should be used, what AI models should be developed, where the AI system
should be placed — or if AI is required at all. There are systemic biases at the institu-
tional level that affect how organizations and teams are structured and who controls the
decision making processes, and individual and group heuristics and cognitive/perceptual
biases throughout the AI lifecycle (as described in Section 2.4). Decisions made by end
users, downstream decision makers, and policy makers are also impacted by these biases,
can reflect limited points of view and lead to biased outcomes [73–78]. Biases impacting
human decision making are usually implicit and unconscious, and therefore unable to be
easily controlled or mitigated [79]. Any assumption that biases can be remedied by human
control or awareness is not a recipe for success.
with the highest rate will generally be regarded by the Federal enforcement agencies as evidence of adverse
impact.” 29 C.F.R. § 1607.4(D)
5/77
2.1.2 Categories of AI bias
Based on previous academic work to classify AI bias [80–90] and discussions with thought
leaders in the field, it is possible to identify three dominant categories of AI bias. This three-
way categorization helps to expand our understanding of AI bias beyond the computational
realm. By defining and describing how systemic and human biases present within AI,
we can build new approaches for analyzing, managing, and mitigating bias and begin to
understand how these biases interact with each other. Correspondingly, Fig. 2 presents three
categories of AI bias. Definitions for these terms are found in the G LOSSARY .10 This list
of biases, while not exhaustive, constitutes prominent risks and vulnerabilities to consider
when designing, developing, deploying, evaluating, using, or auditing AI applications.
Systemic
Systemic biases result from procedures and practices of particular institutions that operate
in ways which result in certain social groups being advantaged or favored and others be-
ing disadvantaged or devalued. This need not be the result of any conscious prejudice or
discrimination but rather of the majority following existing rules or norms. Institutional
racism and sexism are the most common examples [91]. Other systemic bias occurs when
infrastructures for daily living are not developed using universal design principles, thus
limiting or hindering accessibility for persons with disabilities. Systemic bias is also re-
ferred to as institutional or historical bias. These biases are present in the datasets used
in AI, and the institutional norms, practices, and processes across the AI lifecycle and in
broader culture and society. See VIGNETTE for more examples.
10Definitions for each category of bias were often selected based on either recently published papers on the
topic, or seminal work within the domain the term is most associated with. When multiple definitions were
identified, the most relevant definition was selected or adapted. The references provided are not intended
to indicate specific endorsement or to assign originator credit.
6/77
Systemic bias in gender identification
Beyond personal identity, human faces encode a number of conspicuous traits
such as nonverbal expression, indicators of sexual attraction and selection, and
emotion. Facial recognition technology (FRT) is used in many types of appli-
cations including gender identification, which compares morphological distances
between faces to classify human faces by gender. The degree of sexual dimor-
phism between men and women appears to vary with age and ethnic group. As a
consequence, accuracy of FRT gender identification can vary with respect to the
age and ethnic group [92]. Prepubescent male faces are frequently misclassified as
female, and older female faces are progressively misclassified as male [92]. Stud-
ies have highlighted that human preferences for sexually dimorphic faces may be
evolutionarily novel [93, 94]. One study found differing levels of facial sexual di-
morphism in samples taken from countries located in Europe, South America, and
Africa [95]. Buolamwini and Gebru examined the suitability of using skin types
as a proxy for demographic classifications of ethnicity or race and found that skin
type is not an adequate proxy for such classifications. Multiple ethnicities can be
represented by a given skin type, and skin type can vary widely within a racial or
ethnic category. For example, the skin types of individuals identifying as Black
in the U.S. can represent many hues, which also can be represented in ethnic His-
panic, Asian, Pacific Islander and American indigenous groups. Moreover, racial
and ethnic categories tend to vary across geographies and over time [36]. While
training data based on a limited or non-representative sample of a group results
in lower accuracy in categorizing members of that group, the degree of sexual
monomorphism or dimorphism within that group also affects accuracy. Additional
biases can occur due to a lack of awareness about the multiplicity of gender [96].
7/77
SYSTEMIC BIAS
HUMAN BIAS
STATISTICAL /
COMPUTATIONAL
BIAS
historical
societal
institutional
SELECTION AND SAMPLING
USE AND INTERPRETATION
PROCESSING /VALIDATATION
INDIVIDUAL
INDIVIDUAL
GROUP
data generation;
detection;
ecological fallacy;
evaluation;
exclusion;
measurement;
popularity;
population;
representation;
Simpson’s Paradox;
temporal;
uncertainty.
activity;
concept drift;
emergent;
content production;
data dredging;
feedback loop;
linking.
amplification;
inherited;
error propagation;
model selection;
survivorship.
groupthink;
funding;
deployment;
sunk cost fallacy.
behavioral;
interpretation;
Rashomon effect or principle;
selective adherence;
streetlight effect;
annotator reporting;
human reporting;
presentation;
ranking.
automation complacency;
consumer;
mode confusion;
cognitive;
anchoring;
availability heuristic;
confirmation;
Dunning–Kruger effect;
implicit;
loss of situational awareness;
user interaction.
Fig. 2. Categories of AI Bias. The leaf node terms in each subcategory in the picture are
hyperlinked to the GLOSSARY . Clicking them will bring up the definition in the Glossary. To
return, click on the current page number (8) printed right after the glossary definition.
8/77
Statistical and Computational
Statistical and computational biases stem from errors that result when the sample is not
representative of the population. These biases arise from systematic as opposed to random
error and can occur in the absence of prejudice, partiality, or discriminatory intent [97]. In
AI systems, these biases are present in the datasets and algorithmic processes used in the
development of AI applications, and often arise when algorithms are trained on one type
of data and cannot extrapolate beyond those data. The error may be due to heterogeneous
data, representation of complex data in simpler mathematical representations, wrong data,
and algorithmic biases such as over- and under-fitting, the treatment of outliers, and data
cleaning and imputation factors.
Human
Human biases reflect systematic errors in human thought based on a limited number of
heuristic principles and predicting values to simpler judgmental operations [98]. These
biases are often implicit and tend to relate to how an individual or group perceives infor-
mation (such as automated AI output) to make a decision or fill in missing or unknown
information. These biases are omnipresent in the institutional, group, and individual de-
cision making processes across the AI lifecycle, and in the use of AI applications once
deployed. There is a wide variety of human biases. Cognitive and perceptual biases show
themselves in all domains and are not unique to human interactions with AI. Rather, they
are a fundamental part of the human mind. There is an entire field of study centered around
biases and heuristics in thinking, decision-making, and behavioral economics for example
[98]. Such research investigates phenomena such asANCHORING BIAS , availability heuris-
tic or bias, CONFIRMATION BIAS , and framing effects, among many others. It should be
noted that heuristics are adaptive mental shortcuts that can be helpful, allowing complexity
reduction in tasks of judgement and choice, yet can also lead to cognitive biases [98]. Hu-
man heuristics and biases are implicit; as such, simply increasing awareness of bias does
not ensure control over it. Here we focus on broader examples of human bias in the AI
space.
2.2 How AI bias contributes to harms
Technology based on AI has tighter connections to and broader impacts on society than
traditional software. Applications that utilize AI are often deployed across sectors and
contexts for decision-support and decision-making. In this role, they can replace humans
and human processes for high-impact decisions. For example, AI-based hiring technolo-
gies and the models that underlie them replace people-oriented hiring processes and are
implemented in any sector that seeks to automate their recruiting and employment pipeline
[99–101]. Yet, ML models tend to exhibit “unexpectedly poor behavior when deployed
in real world domains” without domain-specific constraints supplied by human operators
[102]. These contradictions are a cause for considerable concern with large language mod-
els (or so-called foundation models) due to their considerable EPISTEMIC and ALEATORIC
9/77
uncertainty[103] (as described in Section 3.2.1)—among other factors. Methods for cap-
turing the poor performance, harmful impacts and other results of these models currently
are imprecise and non-comprehensive.
Values
While ML systems are able to model complex phenomena, whether they are capable of
learning and operating in line with our societal values remains an area of considerable re-
search and concern [55, 60, 104–109]. Systemic and implicit biases such as racism and
other forms of discrimination can inadvertently manifest in AI through the data used in
training, as well as through the institutional policies and practices underlying how AI is
commissioned, developed, deployed, and used. Statistical/algorithmic and human cogni-
tive and perceptual biases enter the engineering and modeling processes themselves, and
an inability to properly validate model performance leaves these biases exposed during de-
ployment [61, 102, 110, 111]. These biases collide with the cognitive biases of the individ-
uals interacting with the AI systems as users, experts in the loop, or other decision makers.
Teams that develop and deploy AI often have inaccurate expectations of how the technol-
ogy will be used and what human oversight can accomplish, especially when deployed
outside of its original intent [112, 113]. Left unaddressed, these biases and accompanying
contextual factors can combine into a complex and pernicious mixture. These biases can
negatively impact individuals and society by amplifying and reinforcing discrimination at
a speed and scale far beyond the traditional discriminatory practices that can result from
implicit human or institutional biases such as racism, sexism, ageism or ableism.
2.3 A Socio-technical Systems Approach
Likely due to expectations based on techno-solutionism and a lack of mature AI process
governance, organizations often default to overly technical solutions for AI bias issues. Yet,
these mathematical and computational approaches do not adequately capture the societal
impact of AI systems [61, 73, 75, 111]. The limitations of a computational-only perspective
for addressing bias have become evident as AI systems increasingly expand into our lives.
The reviewed literature suggests that the expansion of AI into many aspects of public
life requires extending our view from a mainly technical perspective to one that is socio-
technical in nature, and considers AI within the larger social system in which it operates
[7, 19, 31, 37, 74, 75, 78, 114–119]. Using a socio-technical approach to AI bias makes it
possible to evaluate dynamic systems of bias and understand how they impact each other
and under what conditions these biases are attenuated or amplified. Adopting a socio-
technical perspective can enable a broader understanding of AI impacts and the key de-
cisions that happen throughout, and beyond, the AI lifecycle–such as whether technology
is even a solution to a given task or problem [3, 108]. Reframing AI-related factors such
as datasets, TEVV , participatory design, and human-in-the-loop practices through a socio-
technical lens means understanding how they are both functions of society and, through
the power of AI, can impact society. A socio-technical approach also enables analytic
10/77
approaches that take into account the needs of individuals, groups and society.
Techno-solutionism
As computational technologies have evolved, there has been an increasing
tendency to believe that technical solutions alone are sufficient for addressing
complex problems that may have social, political, ecological, economic, and/or
ethical dimensions. This approach to problem-solving, often termed techno-
solutionism,[120] assumes that the “right” code or algorithm can be applied to any
problem and ignores or minimizes the relevance of human, organizational, and so-
cietal values and behaviors that inform design, deployment, and use of technology.
In the context of socio-technical AI systems, techno-solutionism promotes a view-
point that is too narrow to effectively address bias risks. One control, for exam-
ple, used in model risk management to mitigate against techno-solutionism and
other anti-patterns, is to establish, document, and review the anticipated real-world
value of an AI system.
Socio-technical approaches in AI are an emerging area, and identifying measurement tech-
niques to take these factors into consideration will require a broad set of disciplines and
stakeholders. Identifying contextual requirements for evaluating socio-technical systems
is necessary. Developing scientifically supportable guidelines to meet socio-technical re-
quirements will be a core focus.
11/77
AI bias extends beyond computational algorithms and models, and the datasets
upon which they are built. The assumptions and decisions made within the pro-
cesses used to develop technology are key factors, as well as how AI technology
is used and interpreted once deployed. The idea that quantitative measures are
better and more objective than other observations is known as the M CNAMARA
FALLACY . This fallacy, and the related concept TECHNOCHAUVINISM [35], are
at the center of many of the issues related to algorithmic bias. Traditional ML
approaches attempt to turn ambiguity, context, human subjectivity, and cate-
gorical observations into objectively measurable quantities based on numerical
mathematical models of their representations. This well-intentioned process
enables data-driven modeling but it also inadvertently creates new challenges for
socio-technical systems. Representing these complex human phenomena with
mathematical models comes at the cost of disentangling the context necessary
for understanding individual and societal impact and contributes to a fallacy of
objectivity [121]. Science has made great strides in understanding the limitations
of human cognition, including how humans perceive, learn, and store visual,
aural, and textual information, and make decisions under risk. Yet, significant
gaps remain. Thus, any mathematical attempt to model such human traits is
limited and incomplete. This is a key challenge in model causality and predicting
human interpretation of model output. And without proper governance, excising
context and flattening the categories into numerical constructs makes traceability
more difficult [122].
Finding approaches in TEVV to compensate for these limitations in the un-
derlying modeling technology and bringing back the necessary context is an
important area of study.
2.4 An Updated AI Lifecycle
Improving trust in AI by mitigating and managing bias starts with identifying a structure
for how it presents within AI systems and uses. Organizations that design and develop
AI technology use the AI lifecycle to keep track of their processes and ensure delivery of
high-performing functional technology—but not necessarily to identify harms or manage
them. This document has adapted a four-stage AI lifecycle from other stakeholder ver-
sions.11 The intent is to enable AI designers, developers, evaluators and deployers to relate
11AI lifecycles utilized as key guidance in the development of the four-stage approach are: Centers of Ex-
cellence (CoE) at the U.S. General Services Administration [70] [IT Modernization CoE. (n.d.)], the Or-
ganisation for Economic Co-operation and Development [106] [Organisation for Economic Co-operation
and Development. (2019).]. Another model of the AI lifecycle is currently under development with the
Joint Technical Committee of the International Organization for Standardization (ISO) and the International
Electrotechnical Commission (IEC).See Information technology — Artificial intelligence — AI system life
cycle processes, ISO/IEC CD 5338 (under development, 1st ed.), https://www.iso.org/standard/81118.html.
12/77
lifecycle processes with AI bias categories and effectively facilitate its identification and
management. The academic literature and best practice guidelines strongly encourage a
multi-stakeholder approach to developing AI applications using a lifecycle. Guidance for
how organizations can enable this approach is described in Section 3.3.2 and focuses on
participatory design methods such as human-centered design.
Test & EvaluationPre-DesignDesign & Development
Deployment
Fig. 3. The AI Development Lifecycle
AI Lifecycles are iterative, and begin
in the Pre-Design stage, where plan-
ning, problem specification, background
research, and identification of data take
place. Decisions here include how to
frame the problem, the purpose of the AI
component, and the general notion that
there is a problem requiring or benefit-
ing from AI. Central to these decisions is
who (individuals or groups) makes them
and which individuals or teams have the
most power or control over them. These
early decisions and who makes them
can reflect systemic biases within orga-
nizational settings, individual and group
heuristics, and limited points of view.
Systemic biases are also reflected in the
datasets selected within pre-design. All of these biases can affect later stages and decisions
in complex ways, and lead to biased outcomes [3, 74–78].
The Design and Development stage typically starts with analysis of the requirements
and the available data. Based on this, a model is designed or selected. A compatibility anal-
ysis should be performed to ensure that potential sources of bias are identified and plans
for mitigation are put into place. As model implementation progresses and is trained on
selected data, the effectiveness of bias mitigation should be evaluated and adjusted.During
development the organization should periodically assess the completeness of bias iden-
tification processes as well as the effectiveness of mitigation. Finally, at the end of the
development stage, and before deployment, a thorough assessment of bias mitigation is
necessary to ensure the system stays within pre-specified limits. The overall model speci-
fication must include the identified sources of bias, the implemented mitigation techniques
and related performance assessments before the model can be released for deployment.
The Deployment stage is when the AI system is released and used. Once humans
begin to interact with the AI system the performance of the system must be monitored
and reassessed to ensure proper function. Teams should engage in continuous monitoring
and have detailed policies and procedures for how to handle system output and behavior.
System retraining may be necessary to correct adverse events, or decommission may be
necessary. Since the lifecycle is iterative there are numerous opportunities for technology
development teams to carry out multi-stakeholder consultation and ensure their applications
13/77
are not causing unintended effects or harms. Specific guidance for governing systems under
these conditions is the subject of Section 3.4.1.
The Test and Evaluation stage is continuous throughout the entire AI Development
Lifecycle. Organizations are encouraged to perform continuous testing and evaluation of
all AI system components and features where bias can contribute to harmful impacts. For
example, if during deployment the model is retrained with new data for a specific context,
the model deployer should work with the model producer to assess actual performance for
bias evaluation. Multi-stakeholder engagement is encouraged to ensure that the assessment
is balanced and comprehensive. If deviations from desired goals are observed, the findings
should feed into the model Pre-Design stage to ensure appropriate adjustments are made
in data curation and problem formulation. Any proposed changes to the design of the
model should then be evaluated together with the new data and requirements to ensure
compatibility and identification of any potential new sources of bias. Then another round
of design and implementation commences to formulate corresponding requirements for
the new model capabilities and features and for additional datasets. During this stage,
the model developer should perform continuous testing and evaluation to ensure that bias
mitigation maintains effectiveness in the new setting, as the model is optimized and tested
for performance. Once released, the deploying organization should use documented model
specifications to test and evaluate bias characteristics during deployment in the specific
context. Ideally, this evaluation should be performed together with other stakeholders to
ensure all previously identified problems are resolved to everyone’s satisfaction.
The most accurate model is not necessarily the one with the
least harmful impact [123].
3. AI Bias: Challenges and Guidance
Through a review of the literature, and various multi-stakeholder processes, including pub-
lic comments, workshops, and listening sessions, NIST has identified three broad areas that
present challenges for addressing AI bias. The first challenge relates todataset factors such
as av
```
