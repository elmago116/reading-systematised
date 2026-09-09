---
title: "Beyond words: How LLMs mirror human needs and values generating synthetic data"
author: Berta Chulvi, José Ángel Gonzalez, Lara Fontanella, Francisco Rangel
year: "2026"
Type: Journal Article
DOI: 10.1177/20539517261457421
source: https://doi.org/10.1177/20539517261457421
created: 2026-08-06
description: The rapid advancement of Generative AI, particularly large language models (LLMs), has sparked an extensive debate regarding the use of synthetic data in social research. Beyond the profound epistemological implications of this possibility, the first prerequisite for its feasibility is to test if su
tags:
  - Tech/synteticData
  - themes/bias/data
  - design/needs
  - tech/Ai
  - Humanities/socialScience
pdfORepub: "[[Beyond words- How LLMs mirror human needs and values generating synthetic data.pdf]]"
---
[[Beyond words- How LLMs mirror human needs and values generating synthetic data.pdf]]

> **Abstract:** The rapid advancement of Generative AI, particularly large language models (LLMs), has sparked an extensive debate regarding the use of synthetic data in social research. Beyond the profound epistemological implications of this possibility, the first prerequisite for its feasibility is to test if such models adjust their responses to capture the vast individual and social diversity found in human populations and, if so, to what extent their outputs are comparable to those observed in human samples. This study investigates whether LLM-generated synthetic personas can accurately express basic psychological needs and human values considering a wide range of distinct individual and social positions. Additionally, to assess whether the model can maintain such consistency beyond information available within the scientific community, we propose a novel task in which the model cannot rely on prior knowledge. The findings suggest that a language model, such as
                    GPT-4o
                    , embodies a set of implicit theories about how a human with specific characteristics would respond to a questionnaire on basic needs and values, and it can apply these theories with sufficient consistency both when responding to an established scale and to a newly developed one. We further examine how certain aspects of our results align with key limitations identified in the critical literature on the use of synthetic data.
## Full text (extracted from `Beyond words- How LLMs mirror human needs and values generating synthetic data.pdf`)

*Source:* `2PDF/Beyond words- How LLMs mirror human needs and values generating synthetic data.pdf`  
*Extracted:* 2026-08-06

```text
Beyond words: How LLMs mirror
human needs and values generating
synthetic data
Berta Chulvi1,2 , José Ángel Gonzalez1,3, Lara Fontanella4 and Francisco Rangel1
Abstract
The rapid advancement of Generative AI, particularly large language models (LLMs), has sparked an extensive debate re-
garding the use of synthetic data in social research. Beyond the profound epistemological implications of this possibility,
the ﬁrst prerequisite for its feasibility is to test if such models adjust their responses to capture the vast individual and
social diversity found in human populations and, if so, to what extent their outputs are comparable to those observed in
human samples. This study investigates whether LLM-generated synthetic personas can accurately express basic psycho-
logical needs and human values considering a wide range of distinct individual and social positions. Additionally, to assess
whether the model can maintain such consistency beyond information available within the scientiﬁc community, we pro-
pose a novel task in which the model cannot rely on prior knowledge. Theﬁndings suggest that a language model, such as
GPT-4o, embodies a set of implicit theories about how a human with speciﬁc characteristics would respond to a ques-
tionnaire on basic needs and values, and it can apply these theories with sufﬁcient consistency both when responding to
an established scale and to a newly developed one. We further examine how certain aspects of our results align with key
limitations identiﬁed in the critical literature on the use of synthetic data.
Keywords
Synthetic data, human needs, human values, prompt engineering, large language models, item response theory
Received: 3 April 2025; accepted: 17 May 2026
Introduction
The exponential growth of Generative Artiﬁcial Intelligence
with its capability to generate vast amounts of synthetic data
has prompted a widespread discussion about the use of large
language models (LLMs) to simulate human opinions and
preferences. On the one hand, a signi ﬁcant number of
authors argue that this possibility will revolutionize re-
search in marketing (Arora et al., 2025; Cillo and Rubera,
2025), social welfare (Heissler et al., 2024; Yuan et al.,
2025), and social science (Bail, 2024). On the other side,
some authors call for a critical examination of the expecta-
tions associated with synthetic data, arguing that many of
these claims are performative rather than descriptive
(Ravn, 2025) and viewing synthetic data as a discursive de-
vice that entails ethical risks comparable to, or even greater,
than those associated with real data (Helm et al., 2024).
Considering the warning about the disproportionate gen-
eration of expectations to be very timely, this research aims
to empirically test whether LLMs adjust their responses ex-
pressing human needs and values in line withﬁndings from
human samples. Additionally, we aim to determine whether
the model is able to vary the responses to reﬂect a detailed
psychological and social proﬁle, when applied to familiar
1Symanto Research, València, Spain
2Social Psychology Department, Universitat de València, València, Spain
3TransPerfect Translations SL, Barcelona, Spain
4Department of Socio-Economic, Managerial, and Statistical Studies, G.
d’Annunzio University of Chieti-Pescara, Pescara, Italy
Corresponding author:
Lara Fontanella, Department of Socio-Economic, Managerial, and
Statistical Studies, G. d’Annunzio University of Chieti-Pescara, Viale
Pindaro 42, 65127 Pescara, Italy.
Email: lara.fontanella@unich.it
Creative Commons Non Commercial CC BY-NC: This article is distributed under the terms of the Creative Commons Attribution-
NonCommercial 4.0 License (https://creativecommons.org/licenses/by-nc/4.0/) which permits non-commercial use, reproduction and
distribution of the work without further permission provided the original work is attributed as speciﬁed on the SAGE and Open Access page (https://us.
sagepub.com/en-us/nam/open-access-at-sage).
Original research article
Big Data & Society
July–September: 1–17
© The Author(s) 2026
Article reuse guidelines:
sagepub.com/journals-permissions
DOI: 10.1177/20539517261457421
journals.sagepub.com/home/bds


but also to unfamiliar scales not previously examined in the
literature.
To measure the ability to express human needs and va-
lues, we focus on two widely tested theories in psycho-
logical research: the theory of Basic Psychological Needs
(Deci and Ryan, 2000) and the theory of Basic Human
Values (Schwartz, 1992). The scales used in their develop-
ment have been empirically tested with cross-cultural sam-
ples, and their structure is well-established across
individuals from diverse cultural backgrounds.
With this goal, we generate a sample of artiﬁcial indivi-
duals for answering the following research questions:
 RQ1. Do synthetic personas simulated by LLMs ex-
press psychological needs and values in line with
ﬁndings from human samples?
 RQ2. Do these synthetic personas respond with the
same consistency when faced with an unfamiliar
scale that represents an extension of Basic Needs
Theory?
 RQ3. Are LLMs sensitive to the sociodemographic
characteristics and personality traits of the persona
proﬁle when expressing needs and values?
For us, it is essential to emphasize that the objective is
not to replace research involving humans with research in-
volving synthetic personas. Our main interest was to create
a very detailed prompt for each synthetic persona in order to
explore the limits and capabilities of the LLMs. The source
code, prompts, and results are publicly accessible through
GitHub for replicability purposes.
The structure of the paper is as follows. First, an over-
view of related studies in computer science and a summary
of critical approaches to the use of synthetic data are pro-
vided. Next, the methodology is described, including the
use of GPT-4o to create a sample of synthetic data and
the instruments used to gather expressions of needs and va-
lues. This is followed by a presentation of keyﬁndings that
address the research questions. Finally, the paper concludes
by summarizing the main contributions and situating our re-
sults within the broader literature that critically examines
the use of synthetic data generated by LLMs.
Related work
The possibility of generating synthetic data through the use
of LLMs is giving rise to a dual process: on the one hand,
research seeking to demonstrate the potential of LLMs to
emulate humans; and on the other, a series of studies warn-
ing of the epistemological, ethical, and political issues in-
volved in using synthetic data as a substitute for real data.
Among research exploring the ability of LLMs to emu-
late human behavior, weﬁnd studies focusing on the ex-
pression of political preferences captured in social surveys
(Dillion et al., 2023; Park et al., 2024), on experimental
settings from classic economic and social psychology ex-
periments (Aher et al., 2023; Park et al., 2024), on person-
ality tests (Huang et al., 2024; Jiang et al., 2023;
Serapio-García et al., 2023) and on the generation of
human-like textual responses coherent with personality
prompts (Jiang et al., 2024) or with professional and socio-
demographic features (Ge et al., 2024).
One of theﬁrst studies to propose that LLMs can be used
as surrogates for human respondents was the work by
Argyle et al. (2023), focusing on politics and public opin-
ion. The research showed that, when properly conditioned
with sociodemographic features and party identiﬁcation,
GPT−3 was able to generate outputs that closely aligned
with human responses in multiple large surveys from the
American National Election Studies.
Similarly, Park et al. (2024) simulated the attitudes and
behaviors of 1,052 real individuals. The authors compare
how accurately each LLM agent replicates the attitudes
and behaviors of its source individuals using different
prompting strategies.
Regarding classical behavioral experiments with hu-
mans, Aher et al. (2023) found that LLMs replicate theﬁnd-
ings from the Ultimatum Game, Garden Path Sentences,
and Milgram Shock Experiment.
In the area of personality test responses, Jiang et al.
(2023) provided theﬁrst evidence that LLMs resemble hu-
man behavior and exhibit internal consistency similar to hu-
man responses, particularly in larger and instruction
ﬁne-tuned models. These results were replicated by
Huang et al. (2024) and Serapio-García et al. (2023), which
demonstrated that highly capable LLMs exhibit satisfactory
levels of internal consistency and test–retest reliability on
the Big Five Inventory (BFI).
Going beyond answering a test, several works (Jiang
et al., 2024; Serapio-García et al., 2023) have shown that
LLMs are capable of emulating different personalities. In
concrete terms, Jiang et al. (2024) presented a study to in-
vestigate whether LLMs can generate content that aligns
with personality proﬁles.
In an effort to produce synthetic data at scale, Ge et al.
(2024) created 1 billion synthetic personas by selecting
text from the web and asking the LLM,“Who is likely to
[read— write— like— dislike— ··· ] the text?” In answering
these questions, the LLM provided detailed descriptions of
professionals who might be interested in a particular text.
Once a large core of personas was created, this work de-
monstrated the coherence of the generated texts with the
personas’ proﬁles. Among this literature, our study is the
ﬁrst to examine whether LLM-simulated personas repro-
duce human-like patterns in needs and values (RQ1), and
the ﬁrst to evaluate their consistency using previously un-
tested questionnaires (RQ2).
Alongside studies showcasing the potential of synthetic
data, there is a signiﬁcant body of work that critically ex-
plores the epistemological, ethical, and political
2 Big Data & Society 13(3)

consequences arising from research based on
LLM-generated data (Helm et al., 2024; Jacobsen, 2025;
Lee et al., 2025; Rossi et al., 2024; Steinhoff, 2024). We
cannot address in depth the critiques around the shift from
“data collection” to “data generation,” a shift that may wor-
sen discrimination and privacy problems by fostering the il-
lusion that synthetic data renders ethical controls
unnecessary (Helm et al., 2024). However, we highlight
the main criticisms from this theoretical debate that are rele-
vant to our study.
The epistemological critique challenges the validity of
knowledge produced with LLM-generated data, emphasiz-
ing two key issues arising from their training on data rooted
in mainstream sources and past narratives (Rossi et al.,
2024). As a result, these models systematically fail to cap-
ture minority perspectives and cannot reﬂect emerging so-
cial trends absent from their training data. Under these
conditions, LLMs risk amplifying existing biases or repro-
ducing stereotypical patterns (Benzel and Rege, 2024).
Another problematic aspect is that evaluations of
LLM-generated data often focus excessively on“believabil-
ity” or resemblance to human output, rather than on their
usefulness or epistemic validity (Rossi et al., 2024).
Although they do not focus on synthetic data generated
by LLMs, Lee et al. (2025) apply the classic critique of the
performative power of classiﬁcation systems (Bowker and
Star, 1999) to the realm of synthetic data generation.
They argue that the use of synthetic data carries the risk
of maintaining— if not reinforcing — certain worldviews
and classi ﬁcations. Applying their critique to
LLM-generated data, these classiﬁcations would corres-
pond to the variables used in the prompt to represent spe-
ciﬁc subpopulations.
Complementary to this critique, Jacobsen (2025) con-
tends that the very process of generating synthetic data en-
forces a particular vision of the social world — one
conceived as a constellation of attributes and features that
are at once separable, mutually independent, and readily
malleable and controllable. He argues that there is a nascent
heterophilic logic underpinning the intersection of synthetic
data and machine learning, that could produce artiﬁcial
hypersensitivity to ever moreﬁne-grained differences. By
bringing these critical approaches into dialogue with those
that highlight the adaptability of LLMs to different proﬁles,
we test whether, when presented with complex proﬁles in-
cluding personality, socioeconomic, and cultural traits, the
model minimizes or ampliﬁes proﬁle-based differences in
the expression of basic needs and values (RQ3).
In summary, our study does not aim to assess whether
LLMs can complete personality questionnaires or simu-
late human behavior in economic games, as explored in
much of the existing literature. Rather, it investigates
whether LLMs can generate responses whose data struc-
tures parallel those observed in cross-cultural research
on basic human needs and values, and whether such
responses are modulated by individual and social charac-
teristics speci ﬁed as contextual variables. Furthermore,
the results are examined in light of major critiques con-
cerning the use of synthetic data, with the objective of pro-
ducing empirical material that contributes to and informs
this critical perspective.
Materials and methods
To simulate different personas with distinct sociodemo-
graphic features and personality traits, we utilizeGPT-4o
as the backbone LLM, leveraging existing evidence that
large, highly capable, and instruction-tuned models are
highly reliable for persona simulation (Jiang et al., 2023;
Serapio-García et al., 2023).
In the following subsections, weﬁrst detail the sociode-
mographic and personality features used to deﬁne a per-
sona, along with the prompting method employed to
simulate personas withGPT-4o. Next, we outline the de-
sign of the questionnaires used to measure the needs and va-
lues expressed by the synthetic personas, including the
process of operationalizing the measurement instruments
into prompts forGPT-4o to answer. Finally, we describe
the experimental procedure used to collect the questionnaire
responses.
Simulating synthetic personas
In our study, a persona is deﬁned as a combination of socio-
demographic features and Big Five personality traits, de-
signed to maximize diversity within the sample.
Sociodemographic and personality features are then organ-
ically incorporated into a system prompt, instructing
GPT-4o to simulate behaviors when responding for needs
and values. As sociodemographic features, we consider
gender, life stage, educational level, income level, andcul-
tural background. Each of these features encompasses sev-
eral values. The values and descriptions of each
sociodemographic feature are included in the supplemen-
tary material.
For gender, we include woman and man as well as non-
binary to broaden representation and encompass identities
beyond the binary gender categories. Regardinglife stage,
we focus exclusively on the adult population. Life stages
are categorized as young adulthood (19–35 years), middle
adulthood (36–65 years), and late adulthood (65 years and
older), following the three last stages of the Life Cycle well-
established by Erikson (1994). Foreducation level, we con-
sider a range from primary education to tertiary education,
encompassing a broad spectrum of knowledge and skills
across the adult population. We categorizedincome level
as low, middle, or high, based on the persona’s perception
of their income— whether it is insufﬁcient, sufﬁcient, or ex-
ceeds their needs— while also considering their relative pos-
ition within their community. We focused on USA-born
Chulvi et al. 3

personas to simplify the experimental design and facilitate
the interpretation of results. Including personas from mul-
tiple national contexts would have required accounting for
substantial cross-national cultural, linguistic, and institu-
tional heterogeneity, thereby resulting in a considerably
more complex design. By concentrating on USA-born indi-
viduals, we established a more controlled framework for as-
sessing the model’s ability to reproduce variation within a
shared sociocultural context. Nonetheless, we incorporated
personas with diverse family cultural backgrounds to cap-
ture internal diversity and evaluate how the model repre-
sents social and cultural differences within the USA
population. For the values of thecultural background,w e
use the ten Cultural Regions used by Schmitt et al. (2007)
with a sample of 56 countries in a cross-cultural research
study about the geographic distribution of Big Five
Personality Traits.
As personality traits, we focus on the Big Five personal-
ity traits that have emerged as the dominant framework in
personality science (Zell and Lesick, 2022). According to
the Big Five model, personality can be reduced toﬁve basic
traits: (1) extraversion, which reﬂects qualities such as
warmth, gregariousness, assertiveness, activity, and posi-
tive emotion, (2)agreeableness, which reﬂects trust, altru-
ism, compliance, and modesty, (3) conscientiousness,
which reﬂects order, dutifulness, achievement-striving, self-
discipline, and deliberation, (4)neuroticism, which reﬂects
anxiety, hostility, depression, self-consciousness, and vul-
nerability, and (5)openness, which reﬂects curiosity, cre-
ativity, resourcefulness, and a willingness to consider
unconventional ideas. To extend the coverage of our study,
we also consider theabsence of Big Five personality traits,
namely: lack of extraversion, lack of agreeableness, lack of
conscientiousness, lack of neuroticism, and lack of open-
ness. The descriptions of the personality traits were taken
from Jiang et al. (2023) and are included in the supplemen-
tary material
1.
The sociodemographic features and personality traits of
a persona can then be included in a system prompt template
to simulate that speciﬁc persona using GPT-4o. Table 1
shows the system prompt template, and we include in sup-
plementary material an illustration of an instantiated
prompt. Our setup allows us to simulate up to 7,290 perso-
nas, derived from the combination of all the sociodemo-
graphic and psychographic features.
Human needs and values tasks
To evaluate whether LLMs align with humans in the ex-
pression of psychological needs, we rely on the basic psy-
chological needs theory (BPNT), one of the six
mini-theories of the self-determination theory (SDT)
(Deci and Ryan, 2000), which emphasizes the existence
of three fundamental psychological needs for humans: au-
tonomy, competence, and relatedness (see Table 2).
The scale that measures basic psychological needs (see
Table 1.9 in the supplementary material) has been tested
in different human samples in more than 20 countries
(Chen et al., 2015; Heissel et al., 2023; Liga et al., 2020;
Nishimura and Suzuki, 2016) showing a clear factorial
structure of six factors expressing satisfaction or frustration
of the three basic needs of autonomy, relatedness, and com-
petence. We compare LLMs
′ performance with the results
of Chen et al. (2015) who validated the scale and its factor-
ial structure in four countries (Belgium, China, USA, and
Peru) and in four different languages. In particular, consid-
ering the 24 items of the original scale, we will evaluate
whether the same factorial structure holds in a sample of
synthetic data where 7,290 personas are simulated with
Table 1. System prompt template to be instantiated for
simulating a synthetic persona usingGPT-4o.
System Prompt
I want you to act as a person with speciﬁc characteristics. I
describe these traits to help you better understand the
perspective and position of this individual.
You are a{gender}. This means that you{gender-deﬁnition}.
Regarding your age, you are{life-stage}, and at this stage,
people typically{life-stage-deﬁnition}. Your educational level
can be deﬁned as{educational-level}, which indicates that
you have{educational-level-deﬁnition}.
In terms of income, you qualify your income as{income-level},
meaning you{income-level-deﬁnition}. You were born in
the USA, and your family cultural background is
{cultural-background}, implying that you and your family
value {cultural-background-deﬁnition}. Recently, in a
personality test, you discovered that
{personality-trait-deﬁnition}.
Table 2. Basic psychological needs deﬁned by BPNT. Deﬁnitions
are taken from Vansteenkiste et al. (2020).
Need De ﬁnition
Autonomy (N1) Refers to the experience of volition and
willingness. When satisﬁed, one experiences
one’s actions as self-endorsed and authentic.
When frustrated, one experiences a sense
of pressure such as feeling pushed in an
unwanted direction.
Competence
(N2)
Concerns the experience of effectiveness and
mastery. It becomes satisﬁed as one capably
engages in activities and experiences
opportunities. When frustrated, one
experiences a sense of ineffectiveness or
even failure and helplessness.
Relatedness
(N3)
Denotes the experience of warmth, bonding,
and care, and is satisﬁed by connecting to
and feeling signiﬁcant to others. Relatedness
frustration comes with a sense of social
alienation, exclusion, and loneliness.
4 Big Data & Society 13(3)

GPT-4o based on different personalities, genders, ages,
cultural family backgrounds, education, and income levels.
Moreover, we want to explore whether the LLM responds
with the same consistency to a new scale that incorporates
two additional basic needs, with the goal of assessing
whether, as some authors suggest (Dillion et al., 2023),
LLMs could be useful for experimenting with preliminary
psychological propositions. To this end, in our experiments,
we will use synthetic data to explore the consistency of two
new basic psychological needs that we have added to the
original scale. These two new needs are excitement and
transcendence (see Table 3 for a description and items 25
to 40 in Table 1.9 in the supplementary material). Our
aim is to test if these needs overlap with the three original
needs in a factorial structure, or, on the contrary, if our syn-
thetic data ﬁts well with a factorial structure of ten factors
that considers the six original factors and four additional
factors corresponding to the satisfaction and frustration of
excitement and transcendence.
For human values, we rely on Schwartz’s theory of hu-
man values (Schwartz, 1992) which has been widely used
in cross-cultural research (Schwartz, 2021). The initial
framework developed by Schwartz (1992) identiﬁes ten dis-
tinct value types (see Table 4) that may align with, or con-
ﬂict with one another. This compatibility or conﬂictual
relation gives an idea on the structure of values.
These values were then organized into two overarching
pairs, forming two key dimensions (Schwartz, 1992,
2021). The ﬁrst, openness to change versus conservation,
reﬂects the tension between independent thinking, personal
expression, novelty, and transformation (encompassing
self-direction, stimulation, and hedonism) and the prefer-
ence for stability, adherence to tradition, order, and resist-
ance to change (including conformity, tradition, and
security). The second dimension,self-transcendence versus
self-enhancement, highlights the contrast between prioritiz-
ing the well-being and interests of others (represented by
universalism and benevolence) and focusing on personal
success, status, and dominance (associated with power
and achievement). To simplify the task, we do not use the
original scales developed by Schwartz (2021). Instead, we
provide GPT-4o with deﬁnitions of each of the ten value
types he identiﬁed and ask to what extent each value is rele-
vant to the synthetic persona created with each prompt.
We instruct GPT-4o to generate responses for the two
questionnaires aimed at inferring the human needs and va-
lues of speciﬁc personas. Each questionnaire consists of a
series of items, and GPT-4o is tasked with rating each
item on a Likert scale from 1 to 5, based on how accurately
it reﬂects a given persona. We operationalize both question-
naires into two task prompts consisting of three sections:in-
struction, options, anditems. We base our prompt sections
on those used in existing literature that have shown success
in administering personality tests to LLMs. Speciﬁcally, the
instruction is adapted from Jiang et al. (2023), with slight
modiﬁcations to highlight the use of persona information
in scoring each item. For the Likert scale labels, we opted
for Arabic numerals, as prior studies (Huang et al., 2024)
have found no signiﬁcant impact of label choices on results.
In the supplementary material we provide all the prompts
provided toGPT-4o .
Table 3. New psychological needs proposed.
Need De ﬁnition
Excitement (N4) Refers to the experience of stimulation,
novelty, and curiosity that arouses interest
and enthusiasm. It becomes satisﬁed when
one engages in activities that fulﬁll the
desire for exploration and vitality. When
frustrated, one may encounter feelings of
monotony, disinterest, or even
restlessness and dissatisfaction.
Transcendence
(N5)
Concerns the human desire to go beyond
the ordinary limits of individual experience
and connect with something greater than
oneself— be it a divine entity, spiritual
realm, nature, humanity, or a larger
purpose. It becomes satisﬁed when one
ﬁnds a deeper sense of purpose,
signiﬁcance, and direction in life. When
frustrated, one may experience a sense of
disconnection or insigniﬁcance, leading to
feelings of existential doubt or despair.
Deﬁnitions are elaborated by authors.
Table 4. Full list of values and descriptions for the values task.
ID Value Description
1 Power Social status and prestige, control or
dominance over people and resources
2 Achievement Personal success through demonstrating
competence according to social standards
3 Hedonism Pleasure and sensuous grati ﬁcation for
oneself
4 Stimulation Excitement, novelty, and challenge in life
5 Self-direction Independent thought and action — choosing,
creating, exploring
6 Universalism Understanding, appreciation, tolerance, and
protection for the welfare of all people and
for nature
7 Benevolence Preservation and enhancement of the welfare
of people with whom one is in frequent
personal contact
8 Tradition Respect, commitment, and acceptance of the
customs and ideas that traditional culture
or religion provide
9 Conformity Restraint of actions, inclinations, and
impulses likely to upset or harm others
and violate social expectations or norms
10 Security Safety, harmony, and stability of society, of
relationships, and of self
Chulvi et al. 5

Gathering questionnaire results
The experiments were conducted usingGPT-4o to simu-
late personas that responded to questionnaires designed to
infer their needs and values. The use ofGPT-4o was in-
formed by prior evidence that large, highly-capable, and
instruction-tuned models are highly reliable for simulating
personas (Huang et al., 2024; Serapio-García et al., 2023).
The experimental procedure to gather questionnaire re-
sponses is outlined below.
For each of the 7,290 personas in the pool,GPT-4o was
conditioned with the systemprompt described above (see
Section“Simulating synthetic personas”) and deﬁning the attri-
butes of the respective persona. Subsequently, the task prompt
corresponding to needs or values (see Section 1.5 in the supple-
mentary material) was provided toGPT-4o. The model gener-
ated scores for all the items within the task through a single
completion. This was accomplished via the chat completion
endpoint of OpenAI’s Python Library
2, utilizing structured out-
put formats. This approach ensured that (i) responses adhere to
the required format, eliminating the need for brittle raw output
parsing or the risk of discardingoutputs, and (ii) the monetary
cost is controlled, as we avoid repeating the system and task
prompts for each item in the questionnaires. Each persona’sr e -
sponse was then stored for subsequent analysis.
The process was repeated three times for each persona over
the period from November 29, 2024, to December 1, 2024.
This resembles a test–retest setup, which allows us to measure
result variance within a short time frame to check reliability.
We leveraged non-deterministic sampling for this purpose
by using the default decoding hyperparameters of the
OpenAI’s chat completions endpoint (temperature and top-p
set to 1). The experimental procedure is illustrated in Figure 1.
In total, 43,740 API calls were made, corresponding to 7,290
personas, 2 tasks, and 3 repetitions per persona. This yielded
21,870 responses for the needs questionnaire and the same num-
ber for the values questionnaire.The total cost of the experimen-
tation was approximately $120. For the sake of reproducibility,
the code and results are publicly available on GitHub.
Results
To address the three research questions outlined in the
“Introduction”, we used synthetic data to replicate the statis-
tical analyses typically performed with human samples in
psychological research. We applied Item Response Theory
(IRT) models (see, Fontanella et al., 2019, and references
therein) to assess the latent structure of the scales, polychoric
correlations to examine associations among Human Values
dimensions while accounting for the ordinal nature of the
data, and Structural Equation Modeling (SEM) (Bollen,
1989) to test relationships between sociodemographic or per-
sonality variables and the latent constructs of psychological
needs and human values. These methods enabled us to evalu-
ate the internal consistency, factorial validity, and structural
relationships within the synthetic data in a way directly com-
parable to analyses conducted on human samples.
LLM performance with human needs and values
expression
As aﬁrst step in our analysis, we investigated whether syn-
thetic personas simulated throughGPT-4o can effectively
express psychological needs and human values in a way
consistent with the ﬁndings from human samples (RQ1).
Figure 1. Process for collecting questionnaire responses from various personas. For each of the 7,290 personas, a system prompt is
conﬁgured to conditionGPT-4o and the whole questionnaire of a single task is presented as a task prompt to generate responses. This
procedure is repeated three times for each persona across three consecutive days.
6 Big Data & Society 13(3)

To assess this, weﬁrst applied IRT exploratory analysis to
examine whether the factorial structure of psychological
needs in synthetic personas aligns with the established
model (Chen et al., 2015). Next, we conducted correlation
analysis on the synthetic personas’responses regarding hu-
man values and compared the resulting correlation patterns
with the compatibility and conﬂict among values previously
established in studies on the human values scale (Schwartz,
1992) and described in Table 5.
Human needs expression.To check whether synthetic perso-
nas behave like humans in expressing needs, given the re-
sponses to the original Deci and Ryan (2000) scale of 24
items, we performed an exploratory IRT analysis using
the R package mirt (Chalmers, 2012), testing factor solu-
tions ranging from 2 to 7 latent traits. Figure 2 represents
the estimated factor loading matrices, showing only the po-
sitions of loadings greater than 0.25 in absolute value. The
factor loading estimates are provided in the supplementary
material. Results clearly support the existence of a 6-factor
solution, where each item loads signiﬁcantly onto a single
factor, forming an independent cluster structure that mirrors
the validated scale. For factor solutions with fewer than six
latent traits, the loading matrices do not exhibit a simple
structure due to the presence of multiple cross-loadings.
Conversely, the 7-factor solution introduces an additional
factor where all loadings are close to zero (with a maximum
absolute value of 0.13), suggesting that it does not provide
meaningful differentiation.
Human values expression. To evaluate whether synthetic
personas behave like humans in expressing human values,
we examined the extent to whichGPT-4o reproduces the
compatibilities and conﬂicts between values identiﬁed in
studies conducted on human samples, particularly in
Schwartz’s work (Schwartz, 1992).
Given the ordinal nature of the item responses, we ana-
lyzed the relationships between human values using poly-
choric correlations, as implemented in the R package
psych (Revelle, 2024). The estimated correlations derived
from the responses of synthetic personas are presented in
Figure 3. Strong positive correlations are observed between
Hedonism and Stimulation (0.79), Benevolence and
Universalism (0.78), Conformity and Security (0.76), and
Conformity and Tradition (0.74). Self-direction shows a
moderate positive correlation with Universalism. Power is
positively correlated with Achievement and, to a lesser ex-
tent, with Hedonism. Additionally, a strong negative correl-
ation is found between Hedonism and Security (−0.72).
Power is negatively correlated with Universalism and
Benevolence. Both Hedonism and Stimulation show nega-
tive correlations with Security, Conformity, and Tradition.
We compare the compatibilities and conﬂicts among
values obtained from synthetic personas with the results
reported by Schwartz in 40 human samples from 20 coun-
tries (Schwartz, 1992). As shown in Table 5, of the nine
values’ compatibilities identi ﬁed in human samples, the
synthetic personas reproduce seven but differ in two. In
human data, a compatibility between Achievement and
Hedonism is observed, whereas this relationship is absent
in the synthetic data. Additionally, the synthetic personas
do not reproduce the compatibility between Security and
Power that Schwartz found in 28 of the 40 human sam-
ples; in fact, the synthetic data show a moderate inverse
correlation ( −0.42) between these two values.
Regarding con ﬂicts, of the 12 con ﬂicts identi ﬁed by
Schwartz (1992) in human samples, the synthetic perso-
nas replicate seven but differ inﬁve. In human data, con-
ﬂicts between self-direction a nd conformity, tradition,
and security are observed, but these are not present in
the synthetic sample. Similarly, the con ﬂicts between
achievement and both universalism and benevolence,
which appear in human samples, are not reproduced in
synthetic personas.
The clustering structure of human values can be ana-
lyzed using community detection algorithms applied to a
psychometric network (see Figure 4). This network is con-
structed by estimating the polychoric partial correlation
matrix using the graphical lasso algorithm (Epskamp
et al., 2018). To detect values’communities, we employed
the Spinglass Algorithm (Traag and Bruggeman, 2009), as
implemented in the igraph package for R (Csárdi et al.,
2025). The partial correlation network in Figure 4 reveals
two distinct communities of human values, differentiated
by color. Red Cluster: Power, Achievement, Hedonism,
Table 5. Number of samples out of 40 in which compatibilities
and conﬂicts among values were conﬁrmed in Schwartz (1992) and
correlation coefﬁcients obtained considering synthetic personas.
Compatibilities
Power-Achievement 35 0.62
Achievement-Hedonism 33 NS
Hedonism-Stimulation 30 0.79
Stimulation-Self-direction 37 0.54
Self-direction-Universalism 38 0.63
Universalism-Benevolence 38 0.78
Tradition-Conformity 37 0.74
Conformity-Security 36 0.76
Security-Power 28 NS
Conﬂicts
Self-direction vs. Conformity 35 NS
Self-direction vs Tradition 35 NS
Self-direction vs Security 35 NS
Stimulation vs. Conformity 35 −0.67
Stimulation vs. Tradition 35 −0.51
Stimulation vs. Security 35 −0.58
Universalism vs. Power 37 −0.64
Universalism vs. Achievement 37 NS
Benevolence vs. Power 37 −0.56
Benevolence vs. Achievement 37 NS
Hedonism vs. Conformity 33 −0.69
Hedonism vs. Tradition 33 −0.54
Chulvi et al. 7

Stimulation, Self-Directio n. Blue Cluster: Security,
Conformity, Tradition, Universalism, Benevolence.
Positive links (green edges) indicate reinforcement within
the community, while negative links (red edges) highlight
conﬂicts between the two clusters. The network visually
conﬁrms Schwartz’s theory of basic human values, show-
ing the opposition between self-enhancement (Power,
Achievement) and self-transcendence (Universalism,
Benevolence). Similarly, openness to change (Hedonism,
Stimulation) contrasts wit h conservation (Security,
Conformity, Tradition).
LLM performance with an extension of basic needs
scale
After establishing the consistency of results between syn-
thetic personas and human samples regarding the factorial
structure of the basic needs scale, we aimed to explore if
these synthetic personas respond with the same consistency
when faced with an unfamiliar scale that represents an ex-
tension of basic needs theory (RQ2).
To this end, we conducted an exploratory IRT analysis,
incorporating responses to all 40 items of the extended basic
needs scale. We tested multiple models with factor numbers
ranging from 2 to 11, and the complete results are provided
in the supplementary material. The results strongly indicate
the presence of a 10-factor structure (Figure 5), where each
item loads signiﬁcantly onto a single factor, forming dis-
tinct and independent clusters. Notably, for the ﬁrst 24
items, this structure closely aligns with the validated ori-
ginal scale (Chen et al., 2015). When considering fewer fac-
tors, multiple cross-loadings emerge, preventing the
identiﬁcation of a clear factorial structure. On the other
hand, the 11-factor solution introduces an additional factor
with loadings near zero (with a maximum absolute value of
0.05), suggesting that this extra factor lacks meaningful
differentiation.
Figure 2. Factorial structure of the original BPNT scale for a number of factors from 2 to 7.Only the position of the factor loadings larger
than 0.25 in absolute value are displayed.
8 Big Data & Society 13(3)

To assess the potential overlap among the 10 retrieved
factors, we conducted a conﬁrmatory IRT model using
the lavaan package for R (Rosseel, 2012). Since the ob-
served items are ordinal, we used the weighted least squares
mean and variance adjusted (WLSMV) estimation method,
which is well-suited for categorical data. The model demon-
strated an excellent ﬁt, as indicated by the ﬁt indices:
Comparative Fit Index (CFI)= 0.998 and root mean square
error of approximation (RMSEA)= 0.041. Detailed factor
loading estimates are provided in the supplementary
material.
As expected, there are negative associations between sat-
isfaction and frustration of human needs (see Figure 6(a)).
Additionally, the absolute values of all the estimated correl-
ation coefﬁcients are relatively high, particularly in the rela-
tionship between Transcendence and Relatedness.
However, when controlling for the inﬂuence of all other
variables through partial correlation analysis, these associa-
tions weaken. The partial correlation network (see
Figure 6(b)) helps reveal the direct dependencies among
the factors by removing spurious associations caused by
common inﬂuences. Theﬁndings suggest that the observed
correlations in the full matrix are partially driven by shared
variance with other factors rather than direct relationships
between the paired latent traits.
Sensitive to the socio-demographic and personality
traits
Having established that synthetic personas respond to the
scales in a manner consistent with human data in terms of
structural patterns, we now explore whether LLMs, particu-
larly GPT-4o, are sensitive to the contextual information
provided when creating different characters— speciﬁcally,
a set of sociodemographic characteristics and personality
traits (RQ3). We analyzed the dependence on synthetic per-
sonas’features using SEM, a statistical framework that en-
ables the simultaneous estimation of multiple relationships
between endogenous and exogenous variables. SEM also
facilitates the speciﬁcation of a measurement model to esti-
mate scores on latent traits. The analysis was conducted
with the lavaan package in R (Rosseel, 2012).
Socio-demographic traits and personality in needs expression.
To assess the dependency of responses on the needs scale
with respect to personas’features, our SEM speciﬁcation in-
cludes both measurement and structural components. The
measurement component deﬁnes the relationship between
the observed items of the extended needs scale and the
underlying latent traits, ensuring each factor retains its in-
tended meaning as outlined in Section“Human needs and
Figure 3. Polychoric correlations for the human value traits.
Chulvi et al. 9

values tasks.” The structural component models the direct
effects of sociodemographic characteristics and personality
on these latent traits, enabling us to examine how differ-
ences among personas shape the expression of needs.
Exogenous covariates for the personas are recoded as
dummy (0/1) variables. Estimates of the regression coefﬁ-
cients are provided in the supplementary material.
To visually summarize theﬁndings, Figure 7 presents
the structural component through a network representation
of the relationships between the covariates and the latent
traits. To enhance interpretability, theﬁgure displays only
the coefﬁcients that are statistically signiﬁcant at the 0.1%
level, ensuring that only the most robust associations are
highlighted. Most of these effects have not been studied
in human samples because obtaining a sufﬁciently diverse
sample in terms of personality traits and cultural back-
ground is extremely challenging. Although it is not possible
to compare all our results with human data, we still present
the signi ﬁcant effects observed, as they help assess
GPT-4o’s sensitivity to the information provided in the
prompt. When psychological literature provides insights
that allow for comparison, we will introduce them in the
discussion.
The ﬁrst relevant result is the model’s hypersensitivity
(Jacobsen, 2025) to the contextual variables introduced in
the prompt to create the synthetic personas, which translates
into a considerable number of statistically signiﬁcant effects
associated with those variables. First, the model is particu-
larly attentive to personality variables, but there is also a
signiﬁcant impact of sociodemographic variables such as
life stage, educational level, or income level, and a moder-
ate impact of the gender variable. The only variable that the
model does not use intensively to modulate the answers is
family cultural background.
In the SEM analysis, considering Agreeableness as the
baseline, Conscientiousness is strongly associated with
Competence Satisfaction and lack of Conscientiousness
with Competence Frustration. Extraversion and Openness
show a strong association with Excitement, Competence
and Autonomy Satisfaction and the opposite is observed
with the lack of these personality traits. Neuroticism is
strongly associated with all the factors that measure frustra-
tion of a basic need but particularly with relatedness and
transcendence frustration. Lack of Neuroticism is strongly
associated with Competence and Autonomy Satisfaction.
Regarding the sociodemographic variables, we see that
gender shows modest effects on needs expressions: syn-
thetic women express more satisfaction in Relatedness
and less satisfaction in Competence than synthetic men.
Non-binary synthetic persons express higher Relatedness
and Competence frustration than men.
Life stage, educational level and income level signiﬁ-
cantly impact the satisfaction or frustration of psychological
needs. Synthetic personas in middle and late adulthood
Figure 4. Network structure of human values and identiﬁed values’communities. Red arrows denote negative correlation
coefﬁcients; green arrows indicate positive correlation coefﬁcients. The Fruchterman-Reingold layout is used for the network
representation.
10 Big Data & Society 13(3)

show declines in autonomy satisfaction and increases in re-
latedness and competence frustration compared to young
adulthood. Synthetic personas with secondary or tertiary
education are associated with higher autonomy and compe-
tence satisfaction compared with elementary school.
Income level is a strong predictor, with middle- and high-
income synthetic personas showing a positive impact on
autonomy and competence satisfaction compared with low-
income level.
Family cultural background shows no effects on needs
expressions except with the new need for Transcendence,
the one which measures spiritual connections. This is a co-
herent result because Basic Psychological Needs Theory
posits that these are universal needs, but Transcendence is
not in the original set of needs and spirituality is strongly
rooted in culture. Taking Africa cultural background as
the baseline, we ﬁnd that the ones that differ the most
from this culture, expressing less transcendence satisfac-
tion, are synthetic personas with a North American and a
Western European family cultural background.
Socio-demographic traits and personality in values expression.
To assess the dependency of responses on the human values
scale with respect to synthetic personas’characteristics, we
regress the ten values on sociodemographic and psycho-
logical traits, which are recoded as dummy variables. The
estimated coefﬁcients are provided in the supplementary
material and visualized in Figure 8, where edges are dis-
played only for coefﬁcients that are statistically signiﬁcant
at the 0.1% level.
In the expression of values, the model shows the same
hypersensitivity to contextual variables, again prioritizing
personality variables, but also attending to sociodemo-
graphic variables, and once more giving less considera-
tion to the variables that inform about the family cultural
background. Considering Agreeableness as baseline,
Conscientiousness shows a strongly direct association
with Achievement and a less strong but still relevant with
Power. Extraversion shows a direct association with
Stimulation and Hedonism. Openness shows a strong asso-
ciation with Stimulation, and to a lesser degree with hedon-
ism and self-direction. Neuroticism, to a lesser extent than
Conscientiousness, is associated with power and achieve-
ment. Regarding the inverse associations, Lack of
Agreeableness is strongly associated with very low support
for Universalism and Benevolence and strong support for
Figure 5. Factorial matrix estimation for a 10-factor solution.
Chulvi et al. 11

Power, Achievement and Hedonism. Lack of Openness is
associated with very low support for Stimulation and
Self-direction.
Regarding sociodemographic pro ﬁles, we see that
Gender differences are also present. Non-binary synthetic
personas tend to score higher on Universalism and
Self-Direction than men, and lower on Tradition and
Conformity. In contrast, responses for women show slight
positive associations with Benevolence and Universalism
compared to men, while displaying a modest negative asso-
ciation with Power.
Proﬁles characterized as being in Late Adulthood exhibit
negative associations with Self-Direction and Stimulation
compared with Young Adulthood. Conversely, they score
positively on Tradition and Conformity. Tertiary
Education shows strong positive effects on Self-Direction
and Universalism, while negatively associating with
Tradition and Conformity compared with Elementary
School.
Income levels reveal another dimension of value orienta-
tion. Synthetic proﬁles with High Income show positive as-
sociations with Power and Achievement. However, this
comes at the expense of Universalism and Benevolence,
which are negatively impacted. Finally, responses asso-
ciated with family background pro ﬁles of East Asia,
Middle East and Southern Europe display strong positive
associations with Tradition and East Asia also with
Conformity.
Conclusions
The ﬁrst objective of this research was to investigate
whether conditioning GPT-4o with a prompt that maxi-
mized the social and psychological diversity of a synthetic
sample would produce responses consistent with the results
found in human samples, particularly in the empirical meas-
urement of two widely tested theories: the Basic
Psychological Needs Theory (Deci and Ryan, 2000) and
the Human Values Theory (Schwartz, 1992).
Our results, based on a sample of 21,870 responses from
7,290 synthetic personas with varying genders, ages, educa-
tion levels, incomes, and personality traits, demonstrate that
GPT-4o is capable of mirroring humans in the structure of
the responses to the instruments used in Basic
Psychological Needs Theory, but only partially reproduces
the results obtained in humans when it comes to expressing
values (RQ1).
Considering the expression of human basic needs, the
model replicates the factorial structure of the Basic Needs
Scale tested in four countries by Chen et al. (2015).
Similarly, we can see that the model is capable of maintain-
ing consistency in the data structure when faced with a scale
that incorporates two new basic needs that have not been
studied in the literature (RQ2). That is, based on the training
data used, the model develops and applies implicit theories
to discern which needs are interconnected and refer to a sin-
gle construct. These constructs include both those already
explored in the literature, such as the three basic needs pro-
posed by Deci and Ryan (2000), and the two new basic
needs introduced in this work.
Regarding the structure of compatibilities and conﬂicts
among values identiﬁed by Schwartz and colleagues in
a study conducted across 20 countries (Schwartz, 1992)
we observe that the model is able to reproduce the two
major oppositions identiﬁed in Schwartz’s theory: self-
enhancement vs self-transcendenceand openness to change
vs conservation. However, it diverges from human results
when it comes to the speciﬁc compatibilities and conﬂicts
among values, showing greater difﬁculty with conﬂicts
(failing in 5 out of 12 cases) than with compatibilities (fail-
ing in 2 out of 9). The model shows particular difﬁculty in
handling the value of achievement, which relates to per-
sonal success and which is perceived by humans as opposed
to universalism and benevolence— an opposition the model
fails to grasp. It also struggles with the value of self-
direction,d eﬁned as independence of action and thought,
which humans see as opposed to conformity, tradition,
Figure 6. Correlation patterns for the 10 factors in the
extended Basic Needs Scale (a) Estimated correlation
coefﬁcient matrix. (b) Network displaying partial correlations
greater than 0.2.Label Codes: Aut.= Autonomy; Rel. = Relatedness;
Comp. = Competence; Exc. = Excitement; Trans. = Transcendence;
Sat. = Satisfaction; Frus. = Frustration.
12 Big Data & Society 13(3)

and security— again, three oppositions the model is unable
to capture. These difﬁculties may suggest, as Rossi et al.
(2024) point out in their critique of the use of synthetic
data in social sciences, that such models are better at repro-
ducing dynamics associated with themainstream than those
related to social change. This limitation arises because inde-
pendence of thought, universalism, and benevolence are
more closely linked to the position of transformative minor-
ities that challenge thestatus quo. In this sense, it is also
relevant that the two compatibilities between values that hu-
mans report but the model does not consider are among
achievement and hedonism and amongsecurity and power,
two compatibilities between values that require a certain de-
gree of critical thinking, that stripachievement of its social
prestige, and acknowledge the intensive use of
security-related arguments by those in positions ofpower.
In summary, we can see that the model mirrors well the
structure of the data in human samples, when expressing
human basic needs but it performs worse when expressing
conﬂicts and compatibilities between values, especially if
they involve values associated with a transformative view
of the status quo. In this sense, we can consider the argu-
ment of Steinhoff (2024), who claims, quoting Bogard
(2006), that simulation technologies“are forms of hypersur-
veillant control, where the preﬁx “hyper” implies not sim-
ply an intensiﬁcation of surveillance, but the effort to
push surveillance technologies to their absolute limit ”
(p.4) by preﬁguring events, rather than merely recording
them. This simulation activity will produce data in ways
that serve the maintenance ofmainstream worldviews.
The third RQ addressed the model’s ability to incorpor-
ate variations in its responses that reﬂected the complex pro-
ﬁling used to create a synthetic person, combining
psychological, socioeconomic, and cultural traits. Theﬁrst
piece of evidence is that the model is indeed highly capable
of introducing small variations that produce statistical ef-
fects without affecting the structural coherence of the data
— that is, without breaking the factorial structure found in
the scales when answered by humans. This sensitivity,
which we have described as hypersensitivity due to the nu-
merous signiﬁcant effects observed, resonates with the cri-
tique made by Jacobsen (2025), who argues that models
designed to maximize differences could produce an artiﬁ-
cial hypersensitivity to ever moreﬁne-grained differences.
We have seen that the model adjusts its responses based
on the proﬁling information used to condition it. This sug-
gests that the model has some internal knowledge on how to
use the conditioning information to mimic human behavior
and applies it consistently across each synthetic persona.
While the model primarily relies on personality traits, it
also accounts for attributes such as educational level, age,
income, and, in some cases, gender proﬁles. In future re-
search with human samples, we could test whether the mod-
el’
s adaptation to certain characteristics accurately mirrors
Figure 7. Graphical representation of the estimated regression matrix for the psychological needs scale through a direct network.
Red arrows denote negative regression coefﬁcients; green arrows indicate positive regression coefﬁcients. “Ns” means satisfaction of
the need, and“Nf” means frustration of the need. All variable codes are provided in the supplementary material. The
Fruchterman-Reingold layout is used for the network representation.
Chulvi et al. 13

human responses. While some associations in the case of
basic human needs appear reasonable others, mainly with
the expression of human values, reproduce stereotypes, a
problem highlighted by Lee et al. (2025) and Benzel and
Rege (2024). For example, there is strong evidence in the
literature that Conscientiousness is linked to strong aca-
demic and professional performance (Zell and Lesick,
2022), which supports our ﬁnding of an association be-
tween Conscientiousness and the satisfaction of
Competence needs. Additionally, synthetic personas with
high-income levels reported greater satisfaction in
Autonomy and Competence needs than those with low-
income levels, a pattern that also seems plausible.
However, the signiﬁcant association between the female
gender and the values of universalism and benevolence is
a genuine expression of the benevolent sexism described
by Glick and Fiske (1996). It is interesting to note that
the association between these two values and non-binary
synthetic persons is even stronger than that observed for
women, which suggests that the model applies some kind
of bias linking minority subgroups with minority values.
This is a well-known human bias deﬁned as illusory correl-
ation (Hamilton and Gifford, 1976).
Considering cross-cultural research, one of the limita-
tions that is often raised about the use of LLMs is that
they cannot model the judgments of people whose cultures
are not represented in their training data (Dillion et al.,
2023). In our results, we instruct the model as being an
individual born in the USA and this choice inevitably limits
the generalizability of theﬁndings beyond the USA context,
as it constrains the range of sociocultural conditions repre-
sented in the simulation. However, we considered different
family cultural backgrounds to capture internal diversity
and evaluate how the model represents social and cultural
differences within the USA population. This cultural vari-
able produced limited effects, mainly in the expression of
the Transcendence need indicating that, unlike with other
variables, the LLM struggles to take sociocultural back-
ground information into account. However, we think that
our research does not fully address the concern expressed
by Dillion et al. (2023), since the tasks GPT−4o performed
in our experiments— namely, the expression of basic psy-
chological needs and human values— are not the most suit-
able scenario for testing sensitivity to different cultural
backgrounds because these constructs are generally deﬁned
as universal and cross-cultural. Consequently, while further
research is needed, one clearﬁnding is thatGPT-4o pos-
sesses internal knowledge that enables it to tailor responses
not only to humans in general but also to speciﬁc groups of
individuals. Moreover, this adaptation is consistently ob-
served across 7,290 personas, each completing the same
task three times. However, it is also clear that these tailored
responses may express bias and stereotypes, and that it
would be a mistake to assume that synthetic data does not
require ethical scrutiny. As Helm et al. (2024) point out,
“synthetic data does not actually resolve ethico-political
Figure 8. Graphical representation of the estimated regression matrix for the human values scale through a direct network. Red
arrows denote negative regression coefﬁcients; green arrows indicate positive regression coefﬁcients. The Fruchterman-Reingold
layout is used for the network representation. All variable codes are provided in the supplementary material.
14 Big Data & Society 13(3)

questions but shifts them from the mode of data collection
to data production” (p. 4). A major question to be addressed
in future research is whether this ability to adjust its re-
sponses to different types of subjects ultimately results in
a maximization of differences and an artiﬁcial hypersensi-
tivity to ever more ﬁne-grained features, as warned by
Jacobsen (2025).
Given the existence of this test bed, and its limitations,
we consider that it is essential to reﬂect on how it can be uti-
lized effectively and to generate empirical evidence within a
relational data paradigm, which deﬁnes data not in relation
to aﬁxed object of reference but rather based on who uses
them, how they are used, and for what purposes
(Offenhuber, 2024).
In an initial attempt to answer this question, our results
demonstrate the potential of employing LLMs in prelimin-
ary research across diverseﬁelds where needs and values
are central concepts. However, it is essential that both re-
searchers and society at large remain aware that the out-
comes inevitably re ﬂect the biases embedded in the
cultural contexts from which these models derive their
training data, including prejudices, stereotypes, and cogni-
tive biases such as illusory correlation. Furthermore, our
ﬁndings concerning the expression of compatibilities and
conﬂicts between values suggest that LLMs— or at least
GPT-4o— may not only align with majority values but
even display an enhanced degree of conformity with
them, thereby showing a tendency to smooth over value
conﬂicts that have been empirically observed in surveys
with representative samples across different cultures.
Limitations and ethical considerations
A ﬁrst limitation of the present work is that we only consid-
ered GPT-4o as the backbone LLM. Thus, ourﬁndings
cannot be extrapolated to other LLMs, especially if their
text generation and instruction-following capabilities are
worse than those of GPT-4o. We focused only on
GPT-4o by leveraging existing evidence that large, highly
capable, and instruction-tuned models are highly reliable
for persona simulation (Jiang et al., 2023; Serapio-García
et al., 2023). Besides,GPT-4o is one of the most widely
used and user-friendly language models (since it is available
through the ChatGPT interface), enhancing the coverage
and applicability of our study to real-world use cases.
Certain demographic groups may be underrepresented in
our study, particularly with respect to gender diversity. This
decision was made to ensure that our experiments remained
feasible within the constraints of time and budget.
The demographic descriptions used in this study were
carefully crafted based on insights from previous research.
However, we recognize that some elements may inadvert-
ently reﬂect preconceptions, especially those tied to cultural
backgrounds. We encourage readers to approach these de-
scriptions with a critical eye and consider their limitations.
Our research critically interrogates the claim that LLMs
are able to completely replace people in social science re-
search. Beyond the risks to research quality, such a replace-
ment would raise serious ethical problems, especially in
studies presented as conclusive rather than exploratory.
Under no circumstances do we endorse or accept responsi-
bility for the misuse of the prompts or methodologies pre-
sented here in unethical ways, such as deceptive practices
on social media, fraudulent schemes, or scams. We strongly
advocate for the responsible application of ourﬁndings in
alignment with ethical standards.
ORCID iDs
Berta Chulvi https://orcid.org/0000-0003-1169-0978
Lara Fontanella https://orcid.org/0000-0002-5441-0035
Ethical considerations
This study did not involve human participants, human-subject
data, personal data, or any form of intervention. The empirical ma-
terial consists of responses generated by LLM to questionnaire
items. Accordingly, ethical approval and informed consent were
not required.
Consent to participate
Not applicable.
Consent for publication
Not applicable.
Authors contributions
All the authors contributed to the study’s conception and design,
while BC led the conceptualization and study’s supervision. BC,
JAG, FR and LF contributed to drafting and revising the manu-
script. JAG developed the dataset, and LF conducted the statistical
analysis. All authors reviewed and approved theﬁnal manuscript.
Funding
The authors disclosed receipt of the followingﬁnancial support for
the research, authorship, and/or publication of this article: The
contribution of Lara Fontanella to this research wasﬁnancially
supported by the ENCLOSE project, selected under the
Research and Innovation Programme“Extended Partnerships in-
volving universities, research centres and companies for the fund-
ing of basic research projects”— MUR Notice No. 341/2022—
within the “GRINS— Growing Resilient, Inclusive and
Sustainable” project [PE0000018]. The project is funded by the
European Union— NextGenerationEU within the framework of
the National Recovery and Resilience Plan (PNRR).
Declaration of conﬂicting interest
The authors declared no potential conﬂicts of interest with respect
to the research, authorship, and/or publication of this article.
Although Berta Chulvi, Josè Ángel Gonzalez and Francisco
Rangel were afﬁliated with Symanto AI at the time of the research
Chulvi et al. 15

work and Francisco Rangel is still afﬁliated with Symanto AI, this
afﬁliation did not inﬂuence the design, conduct, or conclusions of
the research. Noﬁnancial, personal, or professional incentives in-
ﬂuenced theﬁndings presented in this work.
Data availability
The source code, prompts, and results are publicly accessible
through Github for replicability purposes.
Supplemental Material
Supplemental material for this article is available online.
Notes
1. Personality traits descriptions are publicly available through
GitHub.
2. https://github.com/openai/openai-python
References
Aher G, Arriaga RI and Kalai AT (2023) Using large language
models to simulate multiple humans and replicate human sub-
ject studies. In:Proceedings of the 40th international confer-
ence on machine learning (ICML ’23). pp.337 –371.
JMLR.org. DOI: 10.5555/3618408.3618425.
Argyle LP, Busby EC, Fulda N, et al. (2023) Out of one, many:
Using language models to simulate human samples.Political
Analysis 31(3): 337–351.
Arora N, Chakraborty I and Nishimura Y (2025) AI–human hybrids
for marketing research: Leveraging large language models
(LLMs) as collaborators.Journal of Marketing89(2): 43–70.
Bail CA (2024) Can generative AI improve social
science? Proceedings of the National Academy of Sciences
121(21): e2314021121.
Benzel J and Rege M (2024) AI ethics in practice: Exploring racial
and ethnic stereotypes in synthetic resumes written by
ChatGPT. In: K H, Rodriguez RV, Rege M, Ade-Ibijola A,
Ong KL and Piuri V (eds)Artiﬁcial intelligence and knowledge
processing, pp.12–25. Springer Nature Switzerland. DOI:10.
1007/978-3-031-73477-9_2.
Bogard W (2006) Welcome to the society of control: The simula-
tion of surveillance revisited. In: Ericson RV and Haggerty KD
(eds) The New Politics of Surveillance and Visibility, pp.55–78.
Toronto, ON, Canada: University of Toronto Press.
Bollen KA (1989) Structural Equations with Latent Variables.
New York: John Wiley & Sons, Inc.
Bowker GC and Star SL (1999)Sorting Things Out: Classiﬁcation
and Its Consequences. The MIT Press.
Chalmers RP (2012) mirt: A multidimensional item response the-
ory package for the R environment. Journal of Statistical
Software 48(6): 1–29.
Chen B, Vansteenkiste M, Beyers W, et al. (2015) Basic psycho-
logical need satisfaction, need frustration, and need strength
across four cultures.Motivation and Emotion39: 216–236.
Cillo P and Rubera G (2025) Generative AI in innovation and mar-
keting processes: A roadmap of research opportunities.Journal
of the Academy of Marketing Science53: 684–701.
Csárdi G, Nepusz T, Traag V, et al. (2025) igraph: Network
Analysis and Visualization in R. R package version 2.1.4.
DOI: 10.5281/zenodo.7682609.
Deci EL and Ryan RM (2000) The“What”and “Why”of goal pur-
suits: Human needs and the self-determination of behavior.
Psychological Inquiry11(4): 227–268.
Dillion D, Tandon N, Gu Y, et al. (2023) Can AI language models
replace human participants?.
Trends in Cognitive Sciences
27(7): 597–600.
Epskamp S, Maris G, Waldorp LJ, et al. (2018) Network psycho-
metrics. In: Irwing P, Booth T and Hughes DJ (eds)The Wiley
handbook of psychometric testing: A multidisciplinary refer-
ence on survey, scale and test development , pp.953–986.
Wiley Blackwell. DOI:10.1002/9781118489772.ch30.
Erikson E (1994)Identity and the Life Cycle. W. W. Norton.
Fontanella L, Fontanella S, Valentini P, et al. (2019) Simple struc-
ture detection through Bayesian exploratory multidimensional
IRT models.Multivariate Behavioral Research54(1): 100–112.
Ge T, Chan X, Wang X, et al. (2024) Scaling synthetic data cre-
ation with 1,000,000,000 personas. DOI:10.48550/arXiv.
2406.20094.
Glick P and Fiske S (1996) The ambivalent sexism inventory:
Differentiating hostile and benevolent sexism. Journal of
Personality and Social Psychology70: 491–512.
Hamilton DL and Gifford RK (1976) Illusory correlation in inter-
personal perception: A cognitive basis of stereotypic judg-
ments. Journal of Experimental Social Psychology 12(4):
392–407.
Heissel A, Sánchez A, Pietrek A, et al. (2023) Validating the
German short basic psychological need satisfaction and frustra-
tion scale in individuals with depression.Healthcare 11(3):
412.
Heissler R, Jonáš J, Carre N, et al. (2024) Can AI digital personas
for well-being provide social support? A mixed-method ana-
lysis of user reviews. Human Behavior and Emerging
Technologies 2024(1): 6738001.
Helm P, Lipp B and Pujadas R (2024) Generating reality and silen-
cing debate: Synthetic data as discursive device.Big Data &
Society 11(2): 20539517241249447.
Huang Jt, Jiao W, Lam MH, et al. (2024) On the Reliability of
Psychological Scales on Large Language Models. In:
Al-Onaizan Y, Bansal M and Chen YN (eds)Proceedings of
the 2024 conference on empirical methods in natural
language processing, pp.6152–6173. Miami, FL: Association
for Computational Linguistics.
Jacobsen BN (2025) Machine learning, synthetic data, and the pol-
itics of difference.Theory, Culture & Society42(3): 41–57.
Jiang G, Xu M, Zhu SC, et al. (2023) Evaluating and inducing per-
sonality in pre-trained language models. In:Proceedings of the
37th international conference on neural information process-
ing systems, NIPS ’23, pp.10622–10643. Red Hook, NY:
Curran Associates Inc.
16 Big Data & Society 13(3)

Jiang H, Zhang X, Cao X, et al. (2024) PersonaLLM: Investigating
the ability of large language models to express personality traits.
In: Duh K, Gomez H and Bethard S (eds)Findings of the asso-
ciation for computational linguistics: NAACL 2024, pp.3605–
3627. Mexico City: Association for Computational Linguistics.
Lee F, Hajisharif S and Johnson E (2025) The ontological politics
of synthetic data: Normalities, outliers, and intersectional hal-
lucinations. Big Data & Society12(2): 20539517251318289.
Liga F, Ingoglia S, Cuzzocrea F, et al. (2020) The basic psycho-
logical need satisfaction and frustration scale: Construct and
predictive validity in the Italian context. Journal of
Personality Assessment102(1): 102–112.
Nishimura T and Suzuki T (2016) Basic psychological need satis-
faction and frustration in Japan: Controlling for the bigﬁve per-
sonality traits.Japanese Psychological Research58: 320–331.
Offenhuber D (2024) Shapes and frictions of synthetic data.Big
Data & Society11(2): 20539517241249390.
Park JS, Zou CQ, Shaw A, et al. (2024) Generative agent simula-
tions of 1,000 people. DOI: 10.48550/arXiv.2411.10109.
Ravn L (2025) The fabrication of synthetic data promises: Tracing
emerging arenas of expectations and boundary work.Big Data
& Society12(1): 20539517241307915.
Revelle W (2024) psych: Procedures for Psychological,
Psychometric, and Personality Research . Northwestern
University, Evanston, IL.
Rosseel Y (2012) lavaan: An R package for structural equation
modeling. Journal of Statistical Software48(2): 1–36.
Rossi L, Harrison K and Shklovski I (2024) The problems of
LLM-generated data in social science research. Sociologica
18(2): 145–168.
Schmitt DP, Allik J, McCrae RR, et al. (2007) The geographic dis-
tribution of bigﬁve personality traits: Patterns and proﬁles of
human self-description across 56 nations.Journal of Cross-
Cultural Psychology38(2): 173–212.
Schwartz SH (1992) Universals in the content and structure of va-
lues: Theoretical advances and empirical tests in 20 countries.
In: Zanna MP (ed.)Advances in experimental social psych-
ology, Vol. 25, pp.1 –65. Academic Press. DOI: 10.1016/
S0065-2601(08)60281-6.
Schwartz SH (2021) A repository of Schwartz value scales with
instructions and an introductions. Online Readings in
Psychology and Culture2(2). DOI: 10.9707/2307-0919.1173.
Serapio-García G, Safdari M, Crepy C, et al. (2023) Personality traits
in large language models. DOI: 10.48550/arXiv. 2307.00184.
Steinhoff J (2024) Toward a political economy of synthetic data: A
data-intensive capitalism that is not a surveillance capitalism?.
New Media & Society26(6): 3290–3306.
Traag VA and Bruggeman J (2009) Community detection in net-
works with positive and negative links.Physical Review E80:
036115.
Vansteenkiste M, Ryan RM and Soenens B (2020) Basic psycho-
logical need theory: Advancements, critical themes, and future
directions. Motivation and Emotion44: 1–31.
Yuan A, Garcia Colato E, Pescosolido B, et al. (2025) Improving
workplace well-being in modern organizations: A review of
large language model-based mental health chatbots. ACM
Transactions on Management Information Systems16(1): 1–26.
Zell E and Lesick TL (2022) Bigﬁve personality traits and per-
formance: A quantitative synthesis of 50 + meta-analyses.
Journal of Personality90(4): 559–573.
Chulvi et al. 17
```
