---
title: "Prompt Coaching for Inclusiveness: A Media Literacy Approach to Increase Users’ Awareness of Algorithmic Bias and Prompting Efficacy"
author: Cheng Chen, Mengqi Liao, Aditya Anand Phadnis, Yao Li, Andrew High, Saeed Abdullah, S. Shyam Sundar
year: "2026"
Type: Proceedings Article
DOI: 10.1145/3772318.3791542
source: https://doi.org/10.1145/3772318.3791542
created: 2026-04-24
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/LLM
  - themes/ethics
  - design/UCD
  - tech/Ai/prompt
  - themes/bias
  - tech/Ai/LLM/prompt
  - themes/education
  - op/acc/leer
pdfORepub: "[[Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf]]"
---

[[Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf]]
## Full text (extracted from `Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf`)

*Source:* `2PDF/Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf`  
*Extracted:* 2026-04-24

```text
Prompt Coaching for Inclusiveness: A Media Literacy Approach
to Increase Users’ Awareness of Algorithmic Bias and Prompting
Efficacy
Cheng Chen
Oregon State University
Corvallis, OR, USA
chenc27@oregonstate.edu
Mengqi Liao
University of Georgia
Athens, GA, USA
mengqi.liao@uga.edu
Aditya Anand Phadnis
Pennsylvania State University
University Park, PA, USA
aap6117@psu.edu
Yao Li
Pennsylvania State University
University Park, PA, USA
ybl5753@psu.edu
Andrew High
Pennsylvania State University
University Park, PA, USA
ach208@psu.edu
Saeed Abdullah
Pennsylvania State University
University Park, PA, USA
saeed@psu.edu
S. Shyam Sundar
Pennsylvania State University
University Park, PA, USA
Sungkyunkwan University
Seoul, Republic of Korea
sss12@psu.edu
Abstract
Large language models often produce biased or stereotypical out-
puts. One way to reduce this possibility is to be more inclusive in
our prompts, but doing so may not come naturally to most users.
Therefore, we designed a tool that coaches users to write more
inclusive prompts—a strategy that leverages design friction to pro-
vide a media literacy intervention. Data from a user study (N=344)
show that compared to no coaching, inclusive prompt coaching
directly increased users’ awareness of algorithmic bias and their
perceived prompting efficacy. It also indirectly enhanced their trust
in the system and perceived trust calibration through cognitive
elaboration. However, inclusive prompt coaching resulted in a less
satisfying user experience. These findings have implications for
ethical interventions in prompting for better communicating and
combating algorithmic bias. We discuss the benefits and limitations
of inclusive prompt coaching, as well as ways to balance usability
for long-term adoption of generative AI systems.
CCS Concepts
•Human-centered computing→Empirical studies in HCI.
Keywords
Prompt coaching, Algorithmic bias awareness, Prompting efficacy,
Trust in AI, Inclusiveness, User experience
This work is licensed under a Creative Commons Attribution 4.0 International License.
CHI ’26, Barcelona, Spain
©2026 Copyright held by the owner/author(s).
ACM ISBN 979-8-4007-2278-3/2026/04
https://doi.org/10.1145/3772318.3791542
ACM Reference Format:
Cheng Chen, Mengqi Liao, Aditya Anand Phadnis, Yao Li, Andrew High,
Saeed Abdullah, and S. Shyam Sundar. 2026. Prompt Coaching for In-
clusiveness: A Media Literacy Approach to Increase Users’ Awareness
of Algorithmic Bias and Prompting Efficacy. InProceedings of the 2026
CHI Conference on Human Factors in Computing Systems (CHI ’26), April
13–17, 2026, Barcelona, Spain.ACM, New York, NY, USA, 16 pages. https:
//doi.org/10.1145/3772318.3791542
1 Introduction
Generative AI has transformed content creation by enabling the
rapid and efficient generation of novel outputs across various do-
mains. However, most publicly available generative AI systems
are biased, largely due to the nature of their training data. Algo-
rithmic bias is broadly defined as a systematic difference between
an algorithm’s behavior or outcomes and a chosen reference stan-
dard [30, 36]. This study focuses on harmful cases where computer
systems systematically and unfairly discriminate against certain
groups of individuals in favor of others [11].
Examples of such biases include the AIportraits App, which light-
ened the skin tones of people of color [64]; the image-generative AI
Stable Diffusion, which suggested mostly White individuals when
prompted to generate images of professionals in higher-paying oc-
cupations such as lawyers and engineers, while suggesting mostly
Non-White individuals when portraying lower-paying profession-
als such as janitors and cashiers [62]; and DALL-E, which dispropor-
tionately favored characteristics deemed socially desirable, such as
being young, beautiful, skinny, and white, over providing realistic
depictions of diverse individuals [40, 73]. These cases demonstrate
the tendency of generative AI models to promote biased and stereo-
typical portrayals of certain groups of individuals, causing repre-
sentational harm, particularly to users from minority communities.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Algorithmic bias is fundamentally a system-level problem. Pre-
vious studies have consistently identified unrepresentative training
data as the primary source of algorithmic bias [ 3, 10, 23, 26]. In-
formed by the documentation paradigm [ 41, 58], several studies
have sought to disclose training data characteristics to help lay users
recognize biases in machine learning models [3, 20, 21]. Although
this approach has been demonstrated to be effective, generative
AI systems powered by large language models (LLMs) present a
unique challenge given their reliance on extensive, Internet-wide
training datasets [ 17, 60]. As a result, the datasets used to train
LLMs are rarely disclosed [72]. This challenge, coupled with the
strong need for AI transparency, has motivated computer scientists
to explore innovative solutions to combat biases in generative AI
models, such as revealing pretraining datasets of LLMs [17, 72] or
incorporating more inclusive data from lesser-represented cultures,
oral traditions, and localized archives [1].
Despite ongoing efforts, users often fail to recognize racial bias
in AI algorithms [18]. The underlying reasons for this lack of aware-
ness are complex. Previous research has shown that users’ racial
backgrounds [18] and in-group biases [83] can contribute to their
tendency to overlook racial and other types of biases embedded
in these systems. In addition, individuals’ unreflective use of Chat-
GPT and other commercially available LLMs may also reduce their
awareness of algorithmic bias.
To improve users’ awareness of algorithmic bias, we draw from
prior research on prompt design and prompt engineering [9, 19, 53,
76] and propose a different strategy, calledinclusive prompt coaching,
to communicate and combat algorithmic bias in generative AI mod-
els. This approach leverages the affordance of promptability [19]
and guides users to come up with more inclusive prompts for image
generation. Previous studies have shown that a well-crafted prompt
can produce more diverse and inclusive images under certain con-
ditions [27, 32, 73]. Extending this line of research, the current
study examines how users perceive, experience, and engage with
an image-generative AI tool that provides inclusive prompt coach-
ing and studies its effects on their awareness of algorithmic bias,
confidence in crafting inclusive prompts (i.e., prompting efficacy),
trust in the AI tool, and perceived trust calibration.
To achieve this goal, we conducted an online experiment with
344 participants, in which participants were randomly assigned to
interact with a new image-generative AI tool that either provided
inclusive prompt coaching, detailed prompt coaching (which serves
as an active control as it requires roughly the same amount of
interaction from users), or no coaching. The last two conditions
served as control conditions. Our findings showed that the effects of
inclusive prompt coaching were mixed. On the one hand, it directly
increased users’ awareness of algorithmic bias and their perceived
prompting efficacy, and indirectly enhanced users’ trust in the AI
tool and perceived trust calibration through cognitive elaboration.
On the other hand, it resulted in a less satisfying user experience.
This study contributes to the literature by proposing and testing
a new strategy—"inclusive prompt coaching"—for communicating
and combating algorithmic bias in generative AI models. It comple-
ments existing documentation-based approaches in raising users’
awareness of algorithmic bias [41, 58]. By coaching users to write
inclusive prompts, the goal is not to shift the responsibility for mit-
igating algorithmic bias from developers to lay users, but to offer
user-centered design strategies that empower them to navigate
algorithmic bias through advanced prompting skills. We would not
only like to raise users’ awareness and understanding of algorithmic
bias, but also, ultimately, actively involve users in recognizing and
addressing algorithmic bias through prompting to reduce biased
outputs.
Another contribution is the identification of a psychological
mechanism, namely increased cognitive elaboration, through which
inclusive prompt coaching influences users’ trust in a new gener-
ative AI system and their perception of trust calibration, namely,
one’s perceived ability to align their trust level with the AI’s ac-
tual trustworthiness. These findings advance our understanding of
how responsible AI can be fostered through user perceptions and
highlight potential pathways that can lead to this positive outcome.
Third, this study provides an example of how to incorporate
inclusive prompt coaching into users’ interactions with a generative
AI system. This example can be adapted to different contexts. We
believe that this study serves as a starting point for AI designers to
think about how to facilitate users’ prompt design while helping
them recognize and mitigate bias in AI outputs.
2 Theoretical Frameworks
We draw on two theoretical frameworks to guide the conceptualiza-
tion of our study: media literacy intervention and design friction.
2.1 Media Literacy Intervention
Broadly speaking, media literacy interventions are education pro-
grams aimed at minimizing the negative effects of media by educat-
ing individuals about the motivations and processes that underlie
the creation and consumption of specific media content, thereby
re-shaping their media-related beliefs and attitudes and reducing
detrimental behaviors and outcomes related to media use [46]. By
providing people with knowledge structures and skills, the goal
of media literacy is to help users maintain “critical autonomy in
relationship to all media” [5, p. 9].
Some studies have used the media literacy intervention approach
to increase individuals’ awareness and understanding of algorithmic
bias. For example, Ramachandran et al. [69] integrated algorithmic
bias education into a computer science curriculum and highlighted
the varied student reactions to the issue of algorithmic bias and the
importance of multidisciplinary teaching. Likewise, Vartiainen et al.
[82] provided educational workshops that focused on the design of
AI-driven apps. These workshops helped children and young adults
understand that training data is the primary cause of algorithmic
bias in text-to-image generative models.
In particular, most media literacy interventions are provided
prior to exposure to media content, either to inoculate people
against the negative media effects or to counter the already ex-
isting negative effects [68]. This design may not be ideal for tech
companies or users. For tech companies, there is little motivation
to reveal the biases in their models to users. Similarly, offering
educational tutorials or lectures before users’ interaction with their
systems can feel unnatural, cognitively demanding, and delay users’
access. On the users’ side, traditional media literacy interventions
may not align with their needs, particularly when they prioritize
efficiency and productivity [ 2]. Furthermore, most users cannot

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
be expected to go through media literacy training before using a
technology. What is needed is a more seamless and natural interven-
tion that occurs during use, a solution that allows users to acquire
knowledge and skills related to media use in real time, helping
them become more aware of algorithmic bias in the moment of use
and increasing their ability to generate more inclusive and diverse
content using AI.
2.1.1 Intervention During Prompting.Previous studies have ex-
plored the strategy of “ethical natural language intervention” to
encourage the generative AI model to behave more ethically. For
example, Bansal et al. [9] proposed a method by appending certain
inclusive phrases (e.g., “if all individuals can be a lawyer irrespec-
tive of their gender”) to the base prompt (e.g., “a photo of a lawyer”)
for diverse AI outputs, and they found that this linguistic interven-
tion to be effective. Fraser et al. [ 40] replicated this method and
found that this strategy was only effective in one direction, i.e., it
improved the representation of darker-skinned people for socially
positive prompts (e.g., a lawyer), but it did not reduce their repre-
sentation in response to socially negative prompts (e.g., a felon).
They attributed this outcome to the inability of language models to
understand complicated grammar and the difficult words used in
the prompt intervention.
While informative, these studies focus on testing the responsive-
ness of LLMs to prompting interventions rather than on enabling
users to generate prompts that would result in less biased outcomes.
In the absence of data pertaining to users’ perceptions of–and re-
sponses to–such interventions, it remains unclear whether this
approach is effective in enhancing users’ awareness of algorithmic
bias and other user-centered outcomes. To overcome this research
gap, our study focuses on how lay users perceive, experience, and
engage with a media literacy intervention designed to help them
write more inclusive prompts.
2.2 Design Friction: Positive and Negative
Effects
Viewed from the perspective of HCI, media literacy interventions
can be understood as a form ofdesign friction, which refers to “the
points of difficulty encountered during users’ interaction with a
technology” [28, p. 1390]. While UX designers typically strive to
remove causes of friction and create seamless interactions [ 24],
intentionally incorporating small difficulties can serve construc-
tive purposes, such as promoting more reflective, informed, and
safe behaviors [ 12, 57], sparking conversations and discussions
around socio-technical issues of greater complexity [37], and even
facilitating task completion [42].
Aligned with the principles of Slow Design [43] and the notion
of Seamful Design [16], design friction creates "microboundaries"
[28] by deliberately slowing users down in the process of task
completion to encourage mindful engagement. By interrupting
automatic or rushed actions, design friction helps prevent errors
and prompts users to pay closer attention to the task at hand [34, 57].
A growing body of research has consistently demonstrated the
effectiveness of design friction in promoting conscious interactions
and supporting positive behavioral change [28, 34, 57].
A key factor contributing to the effectiveness of design friction
is its ability to prompt users to think and reflect. Kahneman [48]
described two systems of human thinking: System 1, which is fast,
intuitive and relatively low effort, and System 2, which is slower,
more deliberate, and more effortful. While System 1 guides most ev-
eryday actions, System 2 is engaged for more complicated tasks, as it
facilitates more thoughtful processing. By introducing small difficul-
ties in an AI’s interface, design friction can encourage a shift from
System 1 to System 2 thinking. These purposeful slowdowns create
a moment of pause that invites "cognitive elaboration, " defined as
the process of relating new information to existing knowledge to
guide the task at hand [67].
However, a potential drawback of introducing design friction
is that it might undermine user agency, which is defined as the
extent to which individuals believe that they can influence the
actions and outcomes of an AI system [ 61]. Altering users’ task
flow or adding extra steps before task completion can make users
feel as though they have less control over the technology. That said,
previous research suggests that design friction does not necessarily
decrease user satisfaction, as long as users understand beforehand
the purpose and rationale behind the intervention [56].
Building on these theoretical frameworks, we review related
work to explain the novelty of the inclusive prompt coaching inter-
vention and present the rationale for examining the effects of this
intervention.
3 Related Work
Unlike changing users’ prompts behind the scenes without their
awareness or participation, the inclusive prompt coaching approach
focuses on AI-assisted prompt design before image generation. By
alerting users to potential biases in generative AI models and offer-
ing more inclusive prompt suggestions, this approach encourages
users to pause and reflect on the inclusiveness of their prompt de-
sign for more representative and diverse image outputs. Given the
study goals, we focus on the following outcomes to observe the
effects of the inclusive prompt coaching intervention: awareness of
algorithmic bias, trust in the AI system, perceived trust calibration,
and perceived prompting efficacy. We explain each concept below.
3.1 Effects on Awareness of Algorithmic Bias
One major outcome we anticipate is the increased awareness of
algorithmic bias, which we define as users’ ability to recognize that
generative AI outputs do not reflect the diversity of human expe-
riences. This conceptualization aligns with the observation that
image-generative AI systems often produce biased or stereotypical
outputs, particularly against individuals from minority communi-
ties [62]. However, it is unclear whether the increased awareness of
algorithmic bias is due to the focus on improving the "inclusivity"
aspect of prompt design, heightened user involvement, or both.
To investigate this, we introduce two control conditions: one in
which users are guided to write detailed prompts following the
same procedure as inclusive coaching, and another in which users
receive no coaching from the AI system.
Notably, inclusive prompt coaching conceptually differs from de-
tailed prompt coaching by emphasizing different aspects of prompt
improvement: inclusive coaching focuses on inclusivity, aiming to
produce more representative and diverse image outputs, whereas
detailed coaching emphasizes specificity to help users generate

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
more vivid and precise images. Since both types of coaching re-
quire a similar level of user engagement and reflection, detailed
prompt coaching serves as an active control condition to help disam-
biguate the effects of sheer implementation of prompt coaching and
those of the nature of that coaching (inclusiveness vs. detailedness).
Drawing on the notion of priming [49], defined as "the temporary
internal activation of response tendencies, " we predict that just-in-
time coaching that encourages inclusive prompt coaching will be
more effective in raising users’ awareness of algorithmic bias than
either advising them to provide more detailed prompts or offering
no coaching at all. Unlike these latter approaches, inclusive prompt
coaching is likely to specifically activate the concept of ‘inclusivity’
in users’ minds, resulting in higher awareness of algorithmic bias.
3.2 Effects on User Trust and Perceived Trust
Calibration
User trust is another construct that can be influenced by inclusive
prompt coaching. Based on the definition of trust in automation
[50], we define trust in AI as the extent to which users believe that
the system will work on their behalf under uncertainty. Following
previous research [47, 50, 59], we view trust as a multi-dimensional
construct and further differentiate between cognitive trust (belief
in the AI’s integrity and capability), affective trust (emotional bond
between the user and the system), and behavioral trust (intention to
use/adopt) for a more comprehensive evaluation of the formation
of user trust when interacting with a new image-generative AI
system.
Given that trust can be formed through both heuristic and sys-
tematic information processing [77, 79], trust in a system based on
a one-time interaction may be misplaced. For this reason, we also
examine perceived trust calibration, which is defined as the extent
to which users perceive that their trust level is aligned with the
AI’s true trustworthiness [19, 52, 81]. Considering that matching
one’s trust level with the perceived true capabilities of the system
often requires thoughtful evaluation guided by prior knowledge of
AI, we view perceived trust calibration as an indicator of warranted
and responsible trust based on users’ assessment.
3.2.1 Mediating Role of Cognitive Elaboration.One way that in-
clusive prompt coaching could shape users’ trust in AI systems is
through heightened cognitive elaboration. A recent study showed
that helping users design detailed prompts encouraged them to
think more deeply about their ideas, which, in turn, resulted in
higher perceived trust calibration [19]. Considering this, we predict
that inclusive prompt coaching will encourage more reflection on
inclusive prompt design, thus forming higher trust in the system
and enhanced perception of trust calibration.
3.2.2 Mediating Role of Perceived User Agency.In addition, by
revealing multiple possibilities for steering AI outputs toward in-
clusivity, inclusive prompt coaching may increase perceived user
agency, which is defined as the extent to which users feel they
have control over the actions and consequences of a system [61].
However, one downside of inclusive prompt coaching is that it
changes users’ initial prompts for inclusivity considerations. This
may be viewed as undermining user agency if users are firm in their
original ideas or do not have inclusive goals to begin with. Similarly,
nudging users to alter their prompts for inclusivity may be seen as a
threat to their freedom of action, which can result in psychological
reactance [33], potentially leading to worse evaluation outcomes,
such as lower trust in the system and reduced perception of trust
calibration.
3.3 Effects on Prompting Efficacy
A vast body of research highlights the important role of self-efficacy,
i.e., the belief in one’s ability to engage in or execute a behavior,
in driving behavioral change [8, 75]. Drawing on Bandura’s con-
ceptualization of self-efficacy [6], this study introduces perceived
prompting efficacy, a new concept that refers to users’ confidence
in their ability to create effective prompts for generating inclusive
AI outputs.
One possible explanation for the effect of inclusive prompt coach-
ing on increased prompting efficacy is modeling [55]. Informed by
Schunk’s [71] conceptualization, we define modeling as the process
by which individuals pattern their behaviors after those displayed
by AI. By observing how the system flags potentially biased or
stereotypical words in users’ original prompts and suggests more
inclusive prompts, users may learn from the system and mimic its
approach for designing more inclusive prompts. Previous research
highlights that modeling is an important approach for acquiring
literacy skills [71], such as inclusive prompt coaching in our case.
However, if prompting efficacy is based on learning, there might
not be enough time to learn in a one-shot interaction. In addition,
because these inclusive prompt suggestions are automated, the lack
of an explanatory context may limit users’ understanding of how to
craft inclusive prompts independently. Moreover, users who have a
strong belief in the positive machine heuristic, i.e., the belief that
machines are more objective and neutral than humans [80], may
rely on AI-generated prompts rather than actively engaging in the
process of creating and refining prompts for inclusivity. Due to
multiple possibilities, this study explores how inclusive prompt
coaching influences users’ perception of prompting efficacy.
3.4 Effects on User Experience
Last, we seek to examine the user experience (UX) of inclusive
prompt coaching by focusing on six indicators: perceived contin-
gency, helpfulness, frustration, mental effort, user interface (UI)
satisfaction, and liking of the system. These indicators are com-
monly used to evaluate the UX of new systems [19, 25, 70]. Among
all the factors, UI is an important aspect of UX, focusing on how the
presence of certain elements, such as messages, icons, and buttons,
influences users’ reactions to the system [25].
It is acknowledged that prompting or prompt engineering is a
new skill. Nielsen [62] pointed out that more than half of the US
adults have difficulty articulating their thoughts in a written format
[63]. Similarly, Oppenlaender et al. [ 65] found that users lacked
style-specific vocabularies when prompting with image-generative
systems. Moreover, Chen et al. [19] showed that lay users benefit
from prompt coaching as they do not know when to specify their
prompts while interacting with new image-generative systems for
the first time. A more recent study found that an image-generative
AI system guided by the Chain-of-Thought prompting strategy is
perceived as more helpful and easier to use than a system without

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
a prompting strategy [22]. Thus, coaching users to write inclusive
prompts may reduce perceived difficulty and mental effort, as well
as increase perceived helpfulness of the system. Viewed from this
perspective, any coaching would be a welcome addition for users.
However, additional steps in the interaction may increase users’
cognitive load, resulting in greater frustration, perceived difficulty,
and effort. Given that perceived ease of use is critical to adopting
new technologies [31], the increased difficulty and effort may re-
duce system liking and UI satisfaction. Furthermore, nudges for
inclusivity could disrupt workflow, reducing the perceived con-
tingency of interactions between the system and the user, thus
negatively affecting the overall user experience.
4 Current Study
Based on the aforementioned rationale and the motivation to un-
derstand how users perceive, experience, and engage with a new
image-generative AI system that provides inclusive prompt coach-
ing, we propose the following hypotheses and research questions:
H1:Inclusive prompt coaching will increase users’ awareness of
algorithmic bias compared to the detailed prompt coaching condi-
tion (H1a) and the absence of prompt coaching condition (H1b).
H2:Inclusive prompt coaching will increase users’ cognitive
elaboration, which will, in turn, be associated with higher trust in
the AI system (H2a) and enhanced perception of trust calibration
(H2b), compared to the absence of prompt coaching.
RQ1:What role, if any, does user agency play in the relationship
between inclusive prompt coaching and users’ trust in the AI system
and their perceived trust calibration?
RQ2:How does inclusive prompt coaching influence perceived
prompting efficacy for inclusive AI outputs?
RQ3:How does inclusive prompt coaching affect UX?
5 Method
To examine the hypotheses and answer our research questions,
we conducted a user study with 344 participants. We developed a
new text-to-image generative AI application using Streamlit and
OpenAI’s API, with DALL-E 3’s image generation capability. We
created three versions of the generative AI application, offering
either inclusive prompt coaching, detailed prompt coaching, or no
prompt coaching. The latter two served as control groups.
The study was approved by the Institutional Review Board at
the first author’s university and pre-registered on the Open Science
Framework (OSF)’s website before data collection. The purpose
of pre-registration is to enhance transparency and research rigor,
which strengthens the credibility of our results. However, we did
not pre-register the qualitative analysis of users’ behavioral data
and open-ended responses, as these analyses were exploratory in
nature and intended to identify emergent patterns that could com-
plement the quantitative findings. Details of the pre-registration
are available at this link: https://osf.io/jdyaf/overview.
5.1 Development of Generative AI Applications
We used meta-prompting to guide the actions of each generative
AI application, as described below.
5.1.1 Meta-Prompting the Inclusive Prompt Coaching System.The
inclusive prompt coaching system was instructed to role-play as
an expert in identifying unconscious bias, stereotypes, and rep-
resentational issues in character descriptions. Specifically, it was
tasked with detecting subtle biases related to: (1) gender roles and
expectations, (2) cultural and ethnic stereotypes, (3) physical ap-
pearance assumptions, (4) age-related prejudices, and (5) socioe-
conomic stereotypes. The system was then instructed to provide
a standardized disclaimer about the potential for biased or stereo-
typical outputs due to AI training. Following this, the system was
asked to analyze the users’ prompts and generate one clear, spe-
cific sentence highlighting the most significant bias or stereotype
that could emerge in the visual representation. For suggestions, the
system acted as an expert in rewriting character descriptions to be
more inclusive, following three principles: (1) preserve the original
character concept, (2) remove potentially biased language, and (3)
provide only the rewritten prompt without explanation. The codes
for developing the inclusive prompt coaching system are available
at this link: https://github.com/AnonymousUser12345678/Prompt-
Coaching_Inclusiveness
5.1.2 Meta-Prompting the Detailed Prompt Coaching System.The
detailed prompt coaching system was asked to role-play as an ex-
pert in analyzing character descriptions for storytelling and visual
representation. It was instructed to identify areas where the de-
scription lacked sufficient detail—for example, vague or generic
physical descriptions, missing personality traits or motivations,
lack of background or context, absence of unique characteristics
or quirks, or insufficient information about the character’s role
or purpose. The system was then instructed to provide a stan-
dardized disclaimer about the potential for surprising or random
outputs when the prompts lack detail. After this, it was asked
to analyze users’ prompts and identify the most significant gap
in detail for creating a comprehensive visual or narrative repre-
sentation. To enhance the richness of character descriptions, the
system acted as an expert in adding specificity. Its tasks were
to: (1) maintain the core concept of the original character, and
(2) expand slightly on personality traits, background, and unique
characteristics. The system was instructed to provide only the
enhanced description without additional explanation. The codes
for developing the detailed prompt coaching system are available
at this link: https://github.com/AnonymousUser12345678/Prompt-
Coaching_Detailedness
5.1.3 Meta-Prompting the No Prompt Coaching System.The AI
application without prompt coaching was instructed to generate
an image directly from the users’ prompts. The codes for the no
prompt coaching system are available at this link: https://github.
com/AnonymousUser12345678/No-prompt-coaching.
5.2 Study Procedure and Task Flow
The main study consisted of three parts: 1) Completing a pre-
questionnaire, 2) Interacting with a new AI tool, and 3) Filling out
the post-questionnaire. After participants provided their informed
consent, they were given a definition of generative AI and examples
of its applications. They were then asked about their frequency of
generative AI use for various purposes and modalities (e.g., text,
image, video generation) and their perceived AI literacy.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Next, participants were informed that the research team had de-
veloped a new image-generative AI tool and that they were invited
to try it out and provide feedback. Participants were then randomly
assigned to interact with one of three versions of the AI tool, which
provided inclusive, detailed, or no prompt coaching.
5.2.1 First-Round AI Tool Interaction.In all conditions, the system
first introduced itself as a text-to image generative AI system de-
signed to bring fantasy characters to life and asked participants
what they would like to create. Next, in line with the concept of
design friction, we introduced small difficulties into users’ interac-
tion with the AI system in order to encourage reflection on either
the inclusivity or the level of detail in prompt design and image
generation.
Manipulation of Inclusive Prompt Coaching.After submit-
ting their initial prompts, participants in the inclusive prompt coach-
ing condition received a standardized warning about the potential
biases in AI image generation due to the nature of its training
data (see Figure 1). The warning message was kept the same for
all participants to maintain consistency. The tool then analyzed
participants’ initial prompts, identified words or phrases that might
lead to biased or stereotypical output, and suggested an alternative
prompt tailored to their original input. Following this, participants
decided the final prompt they wished to use for image generation.
Manipulation of Detailed Prompt Coaching.The detailed
prompt coaching condition followed a similar task flow, but with-
out any mention of inclusiveness. Participants received a warning
message highlighting that insufficient detail in the prompts could
lead to unexpected or random AI output (see Figure 2). The system
then analyzed participants’ prompts, identified areas where addi-
tional specificity was needed, and provided a more detailed version
based on their input. As in the inclusive prompt coaching condition,
participants in the detailed coaching condition had a final say in
selecting their preferred prompt for image generation. This condi-
tion served as an effort-equivalent control to the inclusive prompt
coaching condition, in that the coaching and effort involved were
about the same, but without the nudge to make the prompts more
inclusive (making this element the only difference across the two
conditions).
Manipulation of No Prompt Coaching.In contrast, partici-
pants in the no prompt coaching condition submitted their initial
prompts, and the AI tool generated the image without offering any
coaching. This served as a baseline condition, against which we
could assess the effects of the sheer presence of prompt coaching,
regardless of its content.
After receiving the AI-generated image, participants in all con-
ditions evaluated the image quality on a 7-point scale (1=very un-
satisfied and 7=very satisfied) and provided feedback on the AI-
generated image. Participants in the inclusive and detailed prompt
coaching conditions were asked, respectively, "Do you have any
additional comments on the inclusiveness/detailedness of the AI-
generated image?"
5.2.2 Second-Round AI Tool Interaction.Following this, partici-
pants in the inclusive and detailed coaching conditions completed
a follow-up task, in which they were asked to craft an inclusive
or detailed prompt for a randomly assigned occupation, such as
a teacher, secretary, and doctor. These occupations were chosen
for their potential to elicit biased and stereotypical outputs [ 62].
This step aimed to assess participants’ actual prompting efficacy
without the presence of prompt coaching. After image generation,
participants in these two conditions evaluated the quality of the
second AI-generated image using the same 7-point scale (1=very
unsatisfied and 7=very satisfied). By contrast, the no-prompt coach-
ing condition did not include the testing of prompt design for a
randomly assigned occupation.
At the end of the interaction, all participants clicked the “Save
& Receive Code” button to proceed to the post-questionnaire.
5.3 Measures
After interacting with the AI tool, we measured the mediating and
dependent variables of interest. All items were rated on a 7-point
scale, except UI satisfaction, which was evaluated on a 9-point scale.
A full list of measures is available in the OSF pre-registration.
5.3.1 Cognitive Elaboration.Measures for cognitive elaboration
were modified from previous research [19, 67]. Items include 1) “I
thought about how to create my prompts to achieve desirable out-
puts, ” 2) “I thought about the kind of image my prompts would gen-
erate, ” and 3) “I found myself connecting how I wrote my prompts
with my knowledge of AI image generation. ” We averaged the three
items to create an index (M= 5.58,SD= .93, Cronbach’s𝛼= .72).
5.3.2 Perceived User Agency.Following previous studies [ 21, 59],
we used three items to measure perceived user agency. Sample
items include: “I felt I had control over how the AI tool works” and
“I could get the AI tool to do the things I wanted it to. ” An index
was created by averaging the three items, which was reliable (M=
4.91,SD= 1.37, Cronbach’s𝛼= .90).
5.3.3 Perceived Algorithmic Bias.We created five items to assess
users’ awareness of algorithmic bias, such as “I am aware that
generative AI outputs do not reflect a diverse range of human
experiences” and “I am mindful that AI tools can reinforce harmful
stereotypes in image generation. ” We averaged the five items to
form an index of algorithmic bias awareness, which was reliable
(M= 5.01,SD= 1.18, Cronbach’s 𝛼 = .87). The Skewness (-.675)
and Kurtosis (.554) of algorithmic bias awareness were within the
acceptable range for normality, according to the criteria proposed
by Hair et al. [44].
5.3.4 Trust in AI.Aligned with the multi-dimensional conceptual-
ization of trust, we measured cognitive trust (4 items from [29, 66]);
e.g., “I can trust the performance of the AI tool to be good”), affective
trust (4 items from [21]); “The AI tool displayed a warm and caring
attitude towards me”), and behavioral trust (4 items from [4, 21]);
“I plan to adopt the AI tool in the future”), separately. Indices were
created by averaging the items belonging to each concept, which
were all reliable (Cognitive trust:M= 5.05,SD= 1.30, Cronbach’s
𝛼 = .93; Affective trust:M= 4.26,SD= 1.49, Cronbach’s 𝛼 = .88;
Behavioral trust:M= 4.85,SD= 1.52, Cronbach’s𝛼= .94).
5.3.5 Perceived Trust Calibration.We adopted five items from [ 19]
to measure perceived trust calibration. Sample items include: “I feel
I am able to calibrate my trust in the AI tool during my interaction
with it” and “I think now my level of trust in the AI tool matches its

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
Figure 1: Visual stimuli from the inclusive prompt coaching condition, showing the interface’s warning about biased language
and the system’s suggested inclusive rewrite
actual capabilities. ” We averaged the five items to create an index
(M= 5.02,SD= .93, Cronbach’s𝛼= .79).
5.3.6 Perceived Prompt Efficacy.Drawing on our explication of
self-efficacy, we developed the following three items to evaluate
prompting efficacy for inclusive AI outputs: 1) “I am confident in
creating effective prompts to reduce biases in AI images, ” 2) “I can
create inclusive prompts to mitigate bias in generative AI models, ”
and 3) “I can steer diverse AI outputs through effective prompting. ”
An index was created by averaging the three items, which was
reliable (M= 5.04,SD= 1.22, Cronbach’s𝛼= .88).
5.3.7 User Experience (UX).We used six indicators to evaluate UX,
including perceived contingency (6 items adapted from [78], 3 items
left after removing cross-loaded items; e.g., “I felt as if the AI tool
gave an exclusive response to my inputs”), perceived helpfulness of
the AI system (4 items adapted from [51]); “The AI tool was working
on my behalf”), UI satisfaction (measured by six paired adjectives
from [25]) on a 9-point scale, e.g., “terrible/wonderful”), perceived
frustration (one question; “How frustrating was the experience
with the AI tool?”), perceived mental difficulty (one question; “How
mentally difficult was it to use the AI tool?”), and liking of the AI
tool (one question; "Did you like using the AI tool?"). The indices
of perceived contingency (M= 5.47,SD= 1.00, Cronbach’s 𝛼 = .78),
perceived helpfulness (M= 5.32,SD= 1.15, Cronbach’s 𝛼 = .88),
and UI satisfaction (M= 7.07,SD= 1.60, Cronbach’s 𝛼 = .93) were
reliable.
5.3.8 Control Variables.Given that the task was related to image
generation, we controlled for users’ prior experience with this
specific use case. In the pre-questionnaire, we asked participants
how often (1 = did not use at all and 6 = used several times each

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Figure 2: Visual stimuli from the detailed prompt coaching condition [baseline condition], showing the interface’s warning
about vague or underspecified prompts and the system’s suggested detailed rewrite to enhance prompt specificity.
day) they had used AI for image generation in the past six months
(M= 2.99,SD= 1.51).
In addition, we added perceived AI knowledge as a covariate
since it may influence users’ awareness of algorithmic bias and
prompting efficacy. Modified from prior research [85], participants
were asked to indicate their level of agreement (1 = strongly disagree
and 7 = strongly agree) with the following five statements: 1) In
general, I know a lot about generative AI; 2) I understand how
generative AI works; 3) I know what generative AI can do; 4) I
understand the benefits of generative AI; and 5) I understand the
limitations of generative AI. We created an index by averaging the
five items (M= 5.02,SD= 1.12, Cronbach’s𝛼= .89).
5.4 Construct Validity
Based on Fornell and Larcker’s [ 38] criteria, convergent validity
was inferred if the average variance extracted (AVE) was greater
than .50 and composite reliability (CR) was higher than .70. Dis-
criminant validity was inferred if the square root of AVE for each
variable exceeded all correlation coefficients involving that con-
struct. Following these criteria, all constructs showed good validity,
as shown in Table 1.
5.5 Participants
A recent study reported a small effect of prompt coaching on per-
ceived trust calibration through increased cognitive elaboration
[19]. Considering the exploratory nature of the study, we set the
effect size at the medium level within the small effect range (f= .17).
Ana-prioripower analysis using G*Power [ 35] suggested that at
least 337 participants were needed to achieve .80 power at the stan-
dard .05 alpha error probability. We recruited 355 participants from
Prolific to account for potential exclusion of incomplete and inat-
tentive responses. Participants who were 18 years old or above and
lived in the United States were eligible to participate in the study.

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
AVE CR 1 2 3 4 5 6 7 8 9 10 11
Elaboration (1) .66 .85 .81
Agency (2) .83 .84 .41*** .91
Bias awareness (3) .67 .91 .22*** .04 .82
Cognitive Trust (4) .63 .97 .38*** .70*** -.04 .79
Affective Trust (5) .74 .92 .26*** .60*** -.04 .70*** .86
Behavioral Trust (6) .85 .96 .30*** .60*** -.04 .74*** .72*** .92
Calibration (7) .57 .86 .50*** .43*** .16*** .50*** .49*** .50*** .75
Efficacy (8) .81 .93 .46*** .50*** .19*** .62*** .56*** .56*** .52*** .90
Contingency (9) .70 .88 .39*** .56*** .05 .61*** .42*** .51*** .52*** .49*** .84
Helpfulness (10) .74 .92 .38*** .59*** -.01 .72*** .58*** .64*** .52*** .55*** .58*** .86
Satisfaction (11) .73 .94 .32*** .66*** -.02 .76*** .62*** .72*** .49*** .56*** .61*** .72*** .85
Note.Bold values on the diagonal are square root of AVE. ***p< .001, **p< .01, *p< .05.
Table 1: Construct Validity of Key Study Variables
We paid participants $3 for the task, which took approximately 15
minutes to complete.
After removing those who failed the attention checks, 344 partic-
ipants remained in the final sample. Of these, 113 belonged to the
inclusive prompt coaching condition, 118 to the detailed prompt
coaching condition, and 113 to the no coaching condition.
Demographically, our sample consisted of slightly more males
(50%) than females (46.8%), and participants who chose non-binary
(2.3%) or did not reveal their gender (0.9%). Their ages ranged from
18 to 67 years (M= 34.13,SD= 10.92). The median educational
background was a bachelor’s degree, and the median family income
was between $50,000 and $75,000 per year. The sample was pre-
dominantly White (57.3%), followed by Black or African American
(30.8%), Asian (7.8%), Hispanic/Latino origin (5.2%), and American
Indian or Alaska Native (0.3%). One participant preferred not to
reveal their race and/or origin.
5.6 Data Analysis Plan
We used Analysis of Covariance (ANCOVA) to answer H1, which
focused on the effects of inclusive prompt coaching on perceived
algorithmic bias, and RQ2, which examined the effect of prompt
coaching on prompting efficacy. To examine the mediating role of
cognitive elaboration (H2) and perceived user agency (RQ1), we
used Model 4 from PROCESS Macro [45], with 5,000 bootstrap re-
samples and 95% percentile bootstrap confidence intervals (CIs).
RQ3, which explored the effects of inclusive prompt coaching on UX,
was examined using Multivariate Analysis of Covariance (MAN-
COVA). We entered self-reported frequency of using image gener-
ating AI (over the last six months) and perceived AI knowledge as
covariates in all quantitative analyses.
In addition to quantitative data, we collected behavioral data
and user responses during their interaction with the AI system
and in the post-questionnaire. Following the open-ended coding
techniques outlined by Strauss and Corbin [74], we analyzed these
responses. The first author carefully reviewed all responses and cat-
egorized user comments according to the mediating and dependent
variables examined in the quantitative analysis, such as algorithmic
bias awareness, perceived user agency, and user experience. The
resulting categorization was then shared with the co-authors for
validation, and any discrepancies in coding were resolved through
group discussions.
6 Results
We first examine the effectiveness of prompt coaching manipula-
tions and then report the results for each research question/hypothesis.
We present the qualitative results at the end of this section.
6.1 Manipulation Check
After interacting with the AI tool, participants were asked to report
their level of agreement with the following statements: 1) “The AI
tool provided alternative prompts for me to consider, ” 2) “The AI
tool identified potential issues in my prompts, ” and 3) “The AI tool
checked how good I was at writing prompts. ” We created an index
of perceived prompt coaching by averaging the three items (M=
4.72,SD= 1.79, Cronbach’s 𝛼 = .89). A one-way analysis of vari-
ance (ANOVA) revealed that participants in the inclusive prompt
coaching condition (M= 5.42,SD= 1.06) and the detailed prompt
coaching condition (M= 5.63,SD= 1.19) reported significantly
higher agreement than those in the no coaching condition (M=
3.09,SD= 1.78),F(2, 231) = 119.61,p< .001. Thus, the manipulation
of the presence vs. absence of prompt coaching was successful.
Participants also rated the extent to which the AI tool encour-
aged them to create prompts that aligned with the following nine
adjectives: 1) elaborate, 2) intricate, 3) thorough, 4) comprehensive,
5) detailed, 6) non-stereotypical, 7) non-discriminatory, 8) unbiased,
and 9) inclusive. The principal component analysis grouped items
1–5 under “perceived detailedness” (M= 5.08,SD= 1.43, Cronbach’s
𝛼 = .95) and items 6–9 under “perceived inclusiveness” (M= 4.58,
SD= 1.60, Cronbach’s𝛼= .93)
A one-tailed independent samplet-test showed that participants
in the inclusive prompt coaching condition (M= 5.42,SD= 1.17)
perceived the assistance as significantly more inclusive than those
in the detailed prompt coaching condition (M= 3.97,SD= 1.68),
t(203.98) = 7.60,p< .001,d= 1.01. Conversely, participants in the
detailed prompt coaching condition perceived the coaching as sig-
nificantly more detailed than those in the inclusive prompt coaching
condition,t(162.84) = 7.31,p< .001,d= -1.00. Thus, the manipulation
of prompt coaching styles (inclusive vs. detailed) was successful.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
6.2 Quantitative Results
6.2.1 Effect on Algorithmic Bias Awareness.H1 stated that inclusive
prompt coaching would increase users’ awareness of algorithmic
bias compared to detailed prompt coaching (H1a) and no prompt
coaching (H1b). Results from a one-way ANCOVA revealed a main
effect of inclusive prompt coaching on algorithmic bias awareness,
F(2, 326) = 3.42,p= .034, partial 𝜂2 = .02. Inclusive prompt coaching
(M= 5.18,SD= 1.03) resulted in higher awareness of algorithmic bias
compared to no prompt coaching (M= 4.82,SD= 1.17). However,
there was no significant difference between inclusive coaching and
detailed coaching (M= 5.05,SD= 1.26), as well as between detailed
prompt coaching and no coaching in promoting users’ awareness
of algorithmic bias.
6.2.2 Mediation Effects on Trust Outcomes via Cognitive Elaboration.
H2 proposed that inclusive prompt coaching would increase users’
cognitive elaboration, which would, in turn, lead to higher trust in
the system and enhanced perception of trust calibration compared
to no prompt coaching. We dummy-coded the independent variable,
using inclusive prompt coaching as the reference group. Results
from Model 4 supported the mediation effect of inclusive prompt
coaching (vs. no coaching) on cognitive trust, B = -.14, SE = .06,
95% CI: [-.27, -.04], affective trust, B = -.06, SE = .04, 95% CI: [-.15,
-.01], behavioral trust, B = -.11, SE = .05, 95% CI: [-.23, -.03], and
perceived trust calibration, B = -.13, SE = .05, 95% CI: [-.24, -.03].
Thus, both H2a and H2b were supported.
We also tested whether these mediation effects held when com-
paring inclusive versus detailed prompt coaching. In this compari-
son, Model 4 showed no significant mediation for cognitive trust, B
= .04, SE = .04, 95% CI: [-.05, .13], affective trust, B = .02, SE = .02,
95% CI: [-.02, .07], behavioral trust, B = .03, SE = .04, 95%CI: [-.04,
.12], and perceived trust calibration, B = .04, SE = .04, 95% CI: [-.05,
.13].
6.2.3 Mediation Effects on Trust Outcomes via Perceived User Agency.
To answer RQ1, we used Model 4 from PROCESS Macro to examine
the mediation hypothesis involving perceived user agency. Results
showed that inclusive prompt coaching (vs. no coaching) did not sig-
nificantly affect perceived user agency, resulting in non-significant
indirect effects on cognitive trust, B = -.03, SE = .11, 95% CI: [-.24,
.17], affective trust, B = -.02, SE = .09, 95% CI: [-.20, .15], behav-
ioral trust, B = -.03, SE = .10, 95% CI: [-.22, .17], and perceived trust
calibration, B = -.01, SE = .04, 95% CI: [-.09, .06].
The difference between inclusive and detailed prompt coaching
on perceived user agency approached significance, B = .31, se = .17,
t = 1.83,p= .068. However, the indirect effects were not significant
for cognitive trust, B = .20, SE = .11, 95% CI: [-.02, .41], affective
trust, B = .17, SE = .09, 95% CI: [-.01, .36], behavioral trust, B = .18,
SE = .11, 95% CI: [-.01, .39], and perceived trust calibration, B = .07,
SE = .04, 95% CI: [-.01, .15].
6.2.4 Effect on Perceived Prompting Efficacy.To answer RQ2, we
conducted a one-way ANCOVA to examine the effect of inclu-
sive prompt coaching on perceived prompting efficacy. The results
showed that inclusive prompt coaching (M= 5.25,SD= 1.03) re-
sulted in a higher perception of prompting efficacy compared to
detailed prompt coaching (M= 5.06,SD= 1.25) and no prompt
coaching (M= 4.95,SD= 1.21),F(2, 326) = 3.74,p= .025, partial 𝜂2 =
.022. The mean difference between inclusive and detailed coaching
approached significance (p= 0.06), and the mean difference between
inclusive and no coaching conditions was significant at thep= 0.01
level. However, there was no significant mean difference between
detailed coaching and no coaching conditions,p= .413.
6.2.5 Effects of Inclusive Prompt Coaching on UX.Given that UX-
related variables were moderately related to each other, multivariate
analysis of covariance (MANCOVA) was used to examine the effects
of inclusive prompt coaching on UX (RQ3). The results revealed a
main effect of inclusive prompt coaching at the multivariate level:
Wilk’s Lambda = .92,F(12, 640) = 2.17,p= .012, partial 𝜂2 = .04. A
close examination of the univariate results showed significant main
effects on perceived helpfulness,F(2, 325) = 3.58,p= .029, partial
𝜂2 = .02, and perceived frustration,F(2, 325) = 4.09,p= .018, partial
𝜂2 = .03.
Specifically, detailed prompt coaching (M= 5.55,SD= 1.10)
was perceived as significantly more helpful compared to inclu-
sive prompt coaching (M= 5.20,SD= 1.21) and no prompt coaching
(M= 5.19,SD= 1.12). In addition, inclusive prompt coaching (M=
2.73,SD= 1.77) was perceived as significantly more frustrating com-
pared to no prompt coaching (M= 2.06,SD= 1.46). However, there
was no significant difference between inclusive prompt coaching
and detailed prompt coaching (M= 2.44,SD= 1.78) in perceived
frustration.
6.3 Exploring Behavioral Data and User
Insights from Open-Ended Responses
Beyond quantitative results, our behavioral data showed that, among
108 participants assigned to the inclusive prompt coaching con-
dition, 66 chose the AI-suggested prompts for image generation,
13 retained their original prompts, and 31 combined their original
prompts with AI suggestions. We conducted an exploratory analy-
sis to examine whether the adoption of AI’s suggestion varied by
race. TheChi-square results revealed that Non-white participants
were less likely to adopt AI-suggested prompts compared to their
White counterparts, 𝜒2 (1,N= 108) = 4.20.p= .041, Cramer’sV=
.20. Besides this, no significant difference was observed between
the two groups in terms of gender, 𝜒2 (1,N= 107) = 1.59,p= .208,
Cramer’sV= .12, education,t(105) = -.21,p= .981, Cohen’sd=
1.27, and income,t(105) = -.02,p= .831, Cohen’sd= 1.72.
6.3.1 Increased Awareness of Algorithmic Bias.For those who adopted
AI-suggested prompts (n = 66), a recurring theme emerged: in-
creased awareness of algorithmic bias. For instance, P33 initially
believed his prompts had no bias. After seeing the system’s warning
about potential bias in his prompts, he acknowledged that it“did a
good job finding any potential biases, even though it may have been
a bit excessive. ”P106 echoed this point, stating that“I wasn’t aware
of this negative connotation [in my prompts]. ”Furthermore, P13 in-
tentionally created anti-inclusive writing,“An orc with long purple
hair. They are trim and possess remarkable strength and muscularity,
complemented by a striking face with unique features. They are in
their mid-20s”, and was pleased that the AI called it out.
The inclusive prompt coaching intervention also heightened
participants’ sensitivity in detecting biases in AI-generated prompts
and outputs. For example, P10 observed,“I think this image is very

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
feminine and would not fit the inclusion criteria. ”In another case,
P59 found the AI-generated dragon,“large wings on a dragon who
also breathes fire, ”was overtly “masculine. ”
In addition, participants reported instances where the system
filled in race-related gaps with stereotypical assumptions. As P38
mentioned,“I did not specify a race, but it generated and specifically
describes a Caucasian. ”Another participant, P16, attempting to
generate an image of himself, noted that the AI tool altered his
height and weight, making him appear“more physically fit looking"
than what he intended. P16 highlighted the potential for the AI
system to introduce its own bias.
Increased awareness of algorithmic bias was further evident in
responses gathered from the post-questionnaire. P70 questioned,
“when inputting a teacher, why does it default to a female? Why not
a male? Why young, and why not older?”P52 complimented the AI
tool because he was“unaware of the bias the tool presented”as it is
not at all his experience. By encouraging users to critically assess
the inclusivity of their prompts, the prompt coaching intervention
effectively raised their awareness of biases in AI-generated prompts
and output. P7 summarized,“It identified potential biases in my
prompt, but the generated image is not without bias. ”This sentiment
was echoed by P23, who said that“The prompt itself still had biases
related to the potential race of the warrior. . . though the goal of the
model is to be inclusive, it still displays some biases. ”In sum, the
inclusive prompt coaching appeared to encourage users to more
critically examine AI-suggested prompts and outputs for potential
instances of bias.
6.3.2 Reduced User Agency.Another prominent theme that emerged
from open-ended responses was reduced user agency. Participants
expressed disappointment when the system providing inclusive
prompt coaching changed their initial prompts, particularly when
they intentionally specified the gender or race of a character. As
P3 commented,“I didn’t like that it told me not to write the word
’woman’ when I wanted my character to be a woman in the most
standard way”. Similarly, P32 noted,“I don’t think it’s biased to in-
clude responses from a specific region of the world or nationality. If I
search for a ninja or a samurai, for example, I am expecting the result
to be an image of a Japanese inspired character or individual. ”This
sentiment was shared by P81,“I don’t like how it left out the gender
of the character that I initially intended it to be and chose the other
gender when left to choose itself. ”
In addition, some participants perceived the AI system as“judg-
ing”(P75) or moderating innocent prompts, as reflected clearly in
one response:“Don’t police my prompt ’it was a cute toad’”(P29).
Overall, participants felt their intentions were“overridden”by the
system (P67), even though they knew the AI’s goal was to create
inclusive prompts.
6.3.3 Mixed User Experience.Our participants reported mixed user
experience with the system that offered inclusive prompt coach-
ing. Specifically, 52% (n = 26) described their experience positively,
noting that the interaction was fun and enjoyable and that the
AI-suggested prompts were helpful. However, several participants
reported negative experiences with the system. For example, P59
questioned the need for inclusiveness in the task:“I did not like the
suggestion to make the image more inclusive. This was not a concern
of mine, so the AI should not have suggested it. ”This response high-
lights a tension between machine agency and user agency when
their goals diverge, and it suggests that inclusive prompt coaching
may not always align with users’ intentions or be necessary for all
image-generation scenarios.
6.3.4 Effects on Actual Prompting Efficacy.We asked participants
in the inclusive and detailed prompt coaching conditions to write a
new prompt for a randomly assigned profession without assistance,
such as engineer, nurse, or teacher. These professions are known
to commonly elicit biased or stereotypical outputs from generative
AI systems [62]. This task revealed several strategies participants
used to reduce biased or stereotypical outputs from the system.
One common strategy was to avoid gender- or race-specific
language in their prompts. Instead, they described the profession in
neutral or functional terms, such as“someone who shows care to the
weak”(for a nurse, P101),“show an individual who leads a discussion
in a classroom setting with children in school”(for a teacher, P79),
“a person that has a job involving drawing and designing for work”
(for a architect, P28). Others described typical scenes or actions
associated with the profession, such as“a nurse holding a clipboard
smiling”(P48) and“a hospital operating room with a patient and
doctors around him”(for a surgeon, P86).
By contrast, another group of participants intentionally empha-
sized race and ethnicity in their prompts, using descriptors such as
“a black woman”(P67),“a woman of color”(P34),“Asian American”
(P105), and“from South America”(P3). To counteract potential AI
bias, they often added inclusive language, such as“diverse class-
room”(P45),“various backgrounds”(P104),“inclusive”(P54, P57,
and P91)“transgender”(P21) and“non-binary”(P32). For example,
P73 wrote“I’d like to generate an image of a chef that celebrates
diversity and inclusivity. ”
However, we also noted a few instances where participants un-
intentionally reinforced common stereotypes against certain pro-
fessions, such as“a guy with a pen and blueprint”(for an architect,
P44) or“I would like to draw a nurse. She is friendly, helpful, and
looks like she would be good with kids”(P15).
In addition, a small group of participants did not participate
actively in the task. They merely listed the profession without
providing any specific details. The limited user inputs are likely to
result in biased or stereotypical outputs.
6.4 Summary of Findings
In summary, the study found that inclusive prompt coaching di-
rectly increased users’ awareness of algorithmic bias and their
perceived prompting efficacy, and indirectly enhanced users’ trust
in the system and perceived trust calibration through cognitive
elaboration. However, inclusive prompt coaching was perceived
as less helpful compared to detailed prompt coaching and caused
more frustration compared to no prompt coaching. We discuss the
implications of these findings in the next section.
7 Discussion
This study examined the effects of inclusive prompt coaching on
users’ awareness of algorithmic bias, trust in AI, perceived trust
calibration, and prompting efficacy. We begin the discussion by
highlighting the positive outcomes of inclusive prompt coaching

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
followed by a discussion of the observed challenges and drawbacks.
The section concludes by describing the study’s limitations and
directions for future research.
7.1 Inclusive Prompt Coaching Increased
Algorithmic Bias Awareness and Perceived
Prompting Efficacy
A major finding of the study is that inclusive prompt coaching effec-
tively increased users’ awareness of algorithmic bias compared to
no prompt coaching. However, there were no significant differences
between the inclusive and detailed prompt coaching conditions,
nor between the detailed and no prompt coaching conditions, in
shaping algorithmic bias awareness. These results suggest that the
effectiveness of inclusive prompt coaching likely arises from the ad-
ditional cognitive effort it requires and the heightened accessibility
of the inclusivity construct. By encouraging individuals to reflect
on potential biases or stereotypes in their prompts and to suggest
alternative, more inclusive versions, this approach seems to prime
users to think about inclusivity. Consequently, when evaluating the
AI system, the concept of inclusivity becomes more salient, leading
to greater awareness of algorithmic bias. In sum, both the increased
accessibility of inclusivity as a construct and the active reflection
process contribute to the heightened awareness of algorithmic bias
observed with inclusive prompt coaching.
In addition, we found that inclusive prompt coaching increased
perceived prompting efficacy, i.e., users’ confidence in their ability
to craft inclusive prompts. When comparing inclusive and detailed
prompt coaching on perceived prompting efficacy, the difference
only approached significance (p= .06). These results suggest that
the observed effect on perceived prompting efficacy could stem
from the shared characteristics of inclusive and detailed prompt
coaching, namely their requirement for additional reflection and
cognitive effort, with only a small proportion of the variability
potentially attributable to the specific "inclusivity" focus of the
coaching.
By flagging potential issues in users’ prompts and providing
alternative examples for consideration, both inclusive and detailed
prompt coaching conditions seem to facilitate "observational learn-
ing, " the process of acquiring thinking styles and behaviors by
observing examples provided by others [7]. As shown in our qual-
itative analysis, users likely modeled their prompting behaviors
after observing the system’s suggestions, which in turn enhanced
their confidence in designing inclusive prompts.
7.2 Mediating Role of Cognitive Elaboration in
the Positive Effect of Inclusive Prompt
Coaching on Trust Outcomes
The important roles of thinking and cognitive effort are also re-
flected in the finding that inclusive prompt coaching increased
users’ cognitive elaboration, which in turn resulted in higher trust
in the system and heightened perception of trust calibration. This
finding corroborates a recent study, which found that assisting users
in prompt design encouraged deeper reflection on their prompts,
resulting in higher perceived trust calibration [ 19]. The positive
effect on cognitive elaboration is probably due to the shared design
characteristics in both the inclusive and detailed prompt coaching
conditions, which intentionally created pause moments for users
to reflect on their prompt design and the inclusiveness or detailed-
ness of the image output. By identifying cognitive elaboration as a
significant mediator, our finding sheds light on the theoretical mech-
anism underlying the effectiveness of design friction in promoting
conscious and mindful interactions [28, 57].
7.3 Inclusive Prompt Coaching Resulted in Less
Satisfying User Experience
Despite the positive cognitive outcomes, inclusive prompt coaching
resulted in higher frustration compared to the no prompt coaching
condition. Moreover, users found inclusive prompt coaching to be
less helpful than the detailed prompt coaching condition. These
findings provide important insights for future improvements of
this intervention. In our study, inclusive prompt coaching was
mandatory for all participants assigned to that condition. Given that
users may have different goals in image generation, and inclusive
prompting may not be a priority for everyone, the mandatory nature
of the intervention may have triggered psychological reactance
from our participants due to perceived loss of freedom. To improve
user experience, future design should consider making inclusive
prompt coaching intervention optional. For example, the interface
could offer inclusive prompt coaching as an available resource,
allowing users to choose whether they want to learn more about
the new feature. This added flexibility could potentially reduce
frustration, particularly for those who prioritize efficiency over
inclusivity in image generation.
Another strategy is to improve the helpfulness of inclusive prompt
coaching by tailoring it to the nature of users’ prompts. For prompts
such as“a cute green toad in a tutu, ”the intervention may be un-
necessary, as the content is harmless. In contrast, for prompts that
could potentially lead to biased or stereotypical AI outputs, such as
“tall muscular guy with sword, ”inclusive prompt coaching could pro-
vide valuable guidance to foster inclusivity. Since not all prompts
inherently carry bias that promote biased or stereotypical outputs,
future design work should incorporate intelligent moderating mech-
anisms to identify when and where inclusive prompt coaching is
most needed. This kind of contextually tailored intervention will
likely increase the perceived helpfulness and usefulness of inclusive
prompt coaching.
7.4 Reconciling the Tension between Machine
Agency and User Agency
At a broader theoretical level, the negative effect of prompt coaching
on user experience suggests that machine agency may sometimes
override user agency, resulting in a negative user experience. When
a system attempts to correct users’ prompts for inclusivity, it may
be perceived as imposing wokeness without volition. Thus, more
design attention is needed to achieve a balance between machine
agency and user agency. Based on user responses, it seems that in-
clusivity is not always users’ primary goal during image generation.
To better align system and user goals, the system could prompt
users to think about inclusivity prior to their use of the system, for
example, by introducing the tool as a generative AI system that
prioritizes inclusivity. Such early communication may motivate

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
users to think about whether they would like to proceed with this
tool. Having this choice may also help reduce their reactance to
subsequent warnings about potential biases in their prompts.
In addition, the system could offer prompt suggestions by pro-
viding users with inclusivity-related keywords to assist them in
prompt design. This form of assistance may be considered less con-
trolling and less overwhelming than flagging potential bias in users’
prompts and providing AI-suggested alternatives. By supporting
user agency through priming and customization, these approaches
are likely to increase their sense of agency and further enhance
users’ receptiveness to the intervention.
7.5 Practical Implications
The findings provide valuable insights for designing generative
AI interfaces that both communicate and combat racial bias in AI
algorithms. First, participants were attentive to our manipulation
of inclusive prompt coaching, which means that users were aware
of the media literacy intervention implemented during their in-
teraction with the system. This “pause moment” is found to be
effective in increasing users’ awareness of algorithmic bias and
perceived prompt efficacy. It highlights the potential of designing
an in-the-moment intervention to convey algorithmic bias from a
user-centered approach, beyond existing strategies that emphasize
training data documentation and disclosure [3, 20, 21].
In addition, our findings show that the inclusive prompt coaching
approach results in higher user trust and perceived trust calibration
of the system through heightened cognitive elaboration. These
positive outcomes are crucial for users’ adaptation and usage of the
system in the long run. We thus recommend AI designers consider
incorporating this new feature into their systems.
Participants expressed that inclusive prompt coaching is most
desirable when they specifically sought inclusiveness in image
generation. Aligning the availability of this feature with users’ in-
tention would likely result in better persuasive outcomes. At the
same time, generative AI systems should be designed to recognize
when users attempt to generate biased or stereotypical outputs. In
those cases, the system should automatically activate prompt coach-
ing to prevent harmful outputs. This proactive approach would not
only reduce biased content but also demonstrate a company’s com-
mitment to social responsibility.
7.6 Limitations and Future Studies
Findings of the study should be interpreted with the following
methodological limitations in mind. First, we did not provide ex-
plicit definitions of "inclusive" and "bias" when meta-prompting
the inclusive prompt coaching system. This lack of specificity may
result in variability in the quality of AI-suggested prompts.
In addition, the current strategies used to suggest inclusive
prompts primarily focused on removing biased language through
more neutral wording (e.g., changing “woman” to “an individual”)
and adding terms such as "diversity" and "inclusivity" to users’ orig-
inal prompts. This mechanical approach may not necessarily result
in more inclusive and diverse images, as evident in prior research
[39], even if users perceived that their prompting efficacy has im-
proved. Future studies should define inclusiveness and bias when
meta-prompting the systems and fine-tune these models with in-
clusive and diverse examples to improve their overall effectiveness.
Second, the observed effect sizes were smaller than anticipated.
This modest impact may stem from participants’ one-time, in-the-
moment exposure to the intervention and their limited understand-
ing of its mechanism. Although these small effects align with prior
research on prompt coaching [19, 22], they suggest that the current
sample size may have been insufficient to detect all significant, albeit
modest, effects. This limitation might explain the non-significant
finding regarding the effect of inclusive prompt coaching on per-
ceived user agency. Given that our participants reported that inclu-
sive prompt coaching undermined their perceived agency, future
studies should recruit a larger sample to determine whether the ab-
sence of an effect reflects a true null finding or insufficient statistical
power in the present study.
Even though the observed effect size of inclusive prompt coach-
ing is small, its practical significance should not be underestimated.
When an intervention applies to generative AI systems used by
millions of people every day [ 15], even subtle changes in users’
awareness of algorithmic bias, perceived prompting efficacy, and
trust in the system can cumulate into substantial aggregate impact.
In this sense, small effects are not trivial; when multiplied across
vast numbers of interactions, they become influential.
Third, we did not recruit our participants based on census data.
Compared to the general U.S. population (median age = 39 years)
[84], our sample (median age = 31 years) is younger. The sample
included a similar proportion of White participants, but a higher
proportion of Blacks or African American participants, and a lower
proportion of Hispanic or Latino participants. Our participants also
had relatively lower socioeconomic status, given that the median
U.S. household income in 2024 was $83,730 [ 14]. Future studies
should recruit a more representative sample to validate our findings
and explore whether the effectiveness of inclusive prompt coaching
varies across demographic groups.
Last, unlike existing studies that provide structured prompt
guidelines or taxonomies for well-organized prompts [13, 54], in-
clusive prompt coaching dynamically suggests alternative prompts
tailored to the input of each user at the time of image generation.
This process provides a personalized learning experience in in-
clusive prompt design and has demonstrated its effectiveness in
enhancing prompting efficacy. However, it is unknown whether
this case-based learning approach will outperform well-structured
prompting guidelines over the long term. Future studies should
explore these differences.
8 Conclusion
This study proposes inclusive prompt coaching as a media literacy
intervention aimed at communicating and combating algorithmic
bias in generative AI models. It extends existing studies on ethical
linguistic interventions for inclusive AI outputs by examining how
users experience, perceive, and engage with an image-generative AI
system that offers inclusive prompt coaching. Through a user study,
we demonstrate that inclusive prompt coaching enhances users’
awareness of algorithmic bias and perceived prompting efficacy,
while also promoting greater trust and perceived trust calibration
through heightened cognitive elaboration. These findings suggest

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
that users can identify and mitigate bias in generative AI outputs
through prompting when given opportunities to pause and reflect
on inclusivity in their prompt design and image output. Given the
black-box nature of LLMs, increasing users’ AI literacy, especially
in crafting inclusive prompts, has become more essential than ever.
Future work should consider users’ motivations and continue to
refine inclusive prompt coaching based on those motivations and
maximize its effectiveness without diminishing the overall quality
of user experience.
Acknowledgments
This research was supported in part by the MSIT (Ministry of Sci-
ence, ICT), Republic of Korea, under the Global Scholars Invitation
Program (RS-2024-00459638) administered by IITP (Institute for In-
formation & Communication Technology Planning & Evaluation).
References
[1] FutureSum AI, Inc. 2025.Latimer: AI for Everyone – Inclusive Language Model.
FutureSum AI, Inc. https://www.latimer.ai/ Accessed: 2025-11-05.
[2] Humaid Al Naqbi, Zied Bahroun, and Vian Ahmed. 2024. Enhancing work
productivity through generative artificial intelligence: A comprehensive literature
review.Sustainability16, 3 (2024), 1166.
[3] Ariful Islam Anik and Andrea Bunt. 2021. Data-centric explanations: Explaining
training data of machine learning systems to promote transparency. InProceedings
of the 2021 CHI conference on human factors in computing systems. Association for
Computing Machinery, New York; NY; United States, 1–13. doi:10.1145/3411764.
3445736
[4] Muhammad Ashfaq, Jiang Yun, Shubin Yu, and Sandra Maria Correia Loureiro.
2020. I, Chatbot: Modeling the determinants of users’ satisfaction and continuance
intention of AI-powered service agents.Telematics and informatics54 (2020),
101473. doi:10.1016/j.tele.2020.101473
[5] Patricia Aufderheide. 2018. Media literacy: From a report of the national leader-
ship conference on media literacy. InMedia literacy around the world. Routledge,
Queenstown, Maryland, 79–86. doi:10.4324/9781351292924-4
[6] Albert Bandura. 1977. Self-efficacy: toward a unifying theory of behavioral
change.Psychological review84, 2 (1977), 191. doi:10.1037/0033-295x.84.2.191
[7] Albert Bandura. 2008. Observational learning.The International Encyclopedia of
Communication(2008). doi:10.1002/9781405186407.wbieco004
[8] Albert Bandura and Nancy E Adams. 1977. Analysis of self-efficacy theory of
behavioral change.Cognitive therapy and research1, 4 (1977), 287–310. doi:10.
1007/bf01663995
[9] Hritik Bansal, Da Yin, Masoud Monajatipoor, and Kai-Wei Chang. 2022, December
7-11. How well can text-to-image generative models understand ethical natural
language interventions?. InProceedings of the 2022 Conference on Empirical Meth-
ods in Natural Language Processing. Association for Computational Linguistics,
Abu Dhabi, UAE, 1358–1370. doi:10.18653/v1/2022.emnlp-main.88
[10] Michelle Bao, Angela Zhou, Samantha Zottola, Brian Brubach, Sarah Desmarais,
Aaron Horowitz, Kristian Lum, and Suresh Venkatasubramanian. 2021. It’s
compaslicated: The messy relationship between rai datasets and algorithmic
fairness benchmarks.arXiv preprint arXiv:2106.05498(2021).
[11] Emily M Bender and Batya Friedman. 2018. Data statements for natural lan-
guage processing: Toward mitigating system bias and enabling better science.
Transactions of the Association for Computational Linguistics6 (2018), 587–604.
doi:10.1162/tacl_a_00041
[12] Andrea Benedetti and Michele Mauri. 2023. A literature review on “fric-
tion” as a method for reflection in design interventions.Convergências: Re-
vista de Investigação e Ensino das ArtesXVI, 31 (2023), 139–146. doi:10.53681/
c1514225187514391s.31.139
[13] Aras Bozkurt and Ramesh C Sharma. 2023. Generative AI and prompt engineering:
The art of whispering to let the genie out of the algorithmic world.Asian Journal
of Distance Education18, 2 (2023), i–vii. https://www.asianjde.com/ojs/index.
php/AsianJDE/article/view/749
[14] United States Census Bureau, Melissa Kollar, and Zach Scherer. 2025.Income in
the United States: 2024. Technical Report P60-286. United States Census Bureau.
https://www.census.gov/library/publications/2025/demo/p60-286.html
[15] Pew Research Center. 2025. AI in Americans’ lives: Awareness, experiences and
attitudes. https://www.pewresearch.org/science/2025/09/17/ai-in-americans-
lives-awareness-experiences-and-attitudes/. Accessed November 25, 2025.
[16] Matthew Chalmers, Ian MacColl, and Marek Bell. 2003. Seamful design: Showing
the seams in wearable computing. InProceedings of the IEE Eurowearable Confer-
ence. The Institution of Electrical Engineers, UK, 11–16. doi:10.1049/ic:20030140
[17] Kent K Chang, Mackenzie Cramer, Sandeep Soni, and David Bamman. 2023.
Speak, memory: An archaeology of books known to chatgpt/gpt-4.arXiv preprint
arXiv:2305.00118(2023).
[18] Cheng Chen, Eunchae Jang, and S. Shyam Sundar. 2025. Racial bias in training
data: Do lay users notice?Media Psychology(2025). doi:10.1080/15213269.2025.
2558036
[19] Cheng Chen, Sangwook Lee, Eunchae Jang, and S Shyam Sundar. 2024. Is your
prompt detailed enough? Exploring the effects of prompt coaching on users’ per-
ceptions, engagement, and trust in text-to-image generative AI tools. InProceed-
ings of the Second International Symposium on Trustworthy Autonomous Systems.
Association for Computing Machinery, New York: NY, 1–12. doi:10.1145/3686038.
3686060
[20] Cheng Chen and S Shyam Sundar. 2023. Is this AI trained on credible data? The
effects of labeling quality and performance bias on user trust. InProceedings of
the 2023 CHI Conference on Human Factors in Computing Systems. Association for
Computing Machinery, New York, NY, 1–11. doi:10.1145/3544548.3580805
[21] Cheng Chen and S Shyam Sundar. 2024. Communicating and combating al-
gorithmic bias: effects of data diversity, labeler diversity, performance bias,
and user feedback on AI trust.Human–Computer Interaction(2024), 1–37.
doi:10.1080/07370024.2024.2392494
[22] Cheng Chen and Xinyan Zhao. 2025. Let’s think step by step: Effects of chain-of-
thought prompt coaching on users’ perceptions and trust in image generative
AI tools.International Journal of Human–Computer Interaction(2025), 1–22.
doi:10.1080/10447318.2025.2530762
[23] Irene Chen, Fredrik D Johansson, and David Sontag. 2018. Why is my classifier
discriminatory?Advances in neural information processing systems31 (2018).
doi:10.5555/3327144.3327272
[24] Zeya Chen and Ruth Schmidt. 2024. Exploring a Behavioral Model of “Positive
Friction” in Human-AI Interaction. InDesign, User Experience, and Usability.
Springer Nature Switzerland, Cham, 3–22. doi:10.1007/978-3-031-61353-1_1
[25] John P Chin, Virginia A Diehl, and Kent L Norman. 1988. Development of an
instrument measuring user satisfaction of the human-computer interface. In
Proceedings of the SIGCHI conference on Human factors in computing systems.
Association for Computing Machinery, New York, NY, 213–218. doi:10.1145/
57167.57203
[26] Alexandra Chouldechova and Aaron Roth. 2020. A snapshot of the frontiers of
fairness in machine learning.Commun. ACM63, 5 (2020), 82–89. doi:10.1145/
3376898
[27] Colton Clemmer, Junhua Ding, and Yunhe Feng. 2024. Precisedebias: An auto-
matic prompt engineering approach for generative ai to mitigate image demo-
graphic biases. InProceedings of the IEEE/CVF Winter Conference on Applications
of Computer Vision. IEEE, Piscataway, NJ, 8596–8605. doi:10.1109/WACV57701.
2024.00840
[28] Anna L Cox, Sandy JJ Gould, Marta E Cecchinato, Ioanna Iacovides, and Ian Ren-
free. 2016. Design frictions for mindful interactions: The case for microboundaries.
InProceedings of the 2016 CHI conference extended abstracts on human factors
in computing systems. Association for Computing Machinery, New York, NY,
1389–1397. doi:10.1145/2851581.2892410
[29] Pratibha A Dabholkar and Xiaojing Sheng. 2012. Consumer participation in
using online recommendation agents: effects on satisfaction, trust, and purchase
intentions.The Service Industries Journal32, 9 (2012), 1433–1449. doi:10.1080/
02642069.2011.624596
[30] David Danks and Alex John London. 2017. Algorithmic bias in autonomous
systems. InProceedings of the Twenty-Sixth International Joint Conference on
Artificial Intelligence, Vol. 17. AAAI Press, Washington, DC, 4691–4697. doi:10.
24963/ijcai.2017/654
[31] Fred D Davis. 1989. Perceived usefulness, perceived ease of use, and user accep-
tance of information technology.MIS quarterly(1989), 319–340. doi:10.2307/
249008
[32] Priya Dhawka, Lauren Perera, and Wesley Willett. 2024. Better little people
pictures: Generative creation of demographically diverse anthropographics. In
Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems.
Association for Computing Machinery, New York, NY, 1–14. doi:10.1145/3613904.
3641957
[33] James Price Dillard and Lijiang Shen. 2005. On the nature of reactance and its role
in persuasive health communication.Communication monographs72, 2 (2005),
144–168. doi:10.1080/03637750500111815
[34] Verena Distler, Gabriele Lenzini, Carine Lallemand, and Vincent Koenig. 2020. The
framework of security-enhancing friction: How UX can help users behave more
securely. InProceedings of the New Security Paradigms Workshop 2020. Association
for Computing Machinery, New York, NY, 45–58. doi:10.1145/3442167.3442173
[35] Franz Faul, Edgar Erdfelder, Albert-Georg Lang, and Axel Buchner. 2007. G*
Power 3: A flexible statistical power analysis program for the social, behavioral,
and biomedical sciences.Behavior research methods39, 2 (2007), 175–191. doi:10.
3758/BF03193146
[36] Sina Fazelpour and David Danks. 2021. Algorithmic bias: Senses, sources, solu-
tions.Philosophy Compass16, 8 (2021), e12760. doi:10.1111/phc3.12760

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
[37] Laura Forlano and Anijo Mathew. 2014. From design fiction to design friction:
Speculative and participatory design of values-embedded urban technology.
Journal of Urban Technology21, 4 (2014), 7–24. doi:10.1080/10630732.2014.971525
[38] Claes Fornell and David F Larcker. 1981. Evaluating structural equation models
with unobservable variables and measurement error.Journal of marketing research
18, 1 (1981), 39–50. doi:10.2307/3151312
[39] Kathleen C. Fraser, Svetlana Kiritchenko, and Isar Nejadgholi. 2023. Diversity
is not a one-way street: Pilot study on ethical interventions for racial bias in
text-to-image systems. InProceedings of the 14th International Conference on Com-
putational Creativity (ICCC). Association for Computational Creativity, Waterloo,
ON, Canada. doi:10.52004/ICCC2023.97
[40] Kathleen C. Fraser, Svetlana Kiritchenko, and Isar Nejadgholi. 2023. A friendly
face: Do text-to-image systems rely on stereotypes when the input is under-
specified? arXiv preprint arXiv:2302.07159. arXiv:2302.07159 [cs.CV]
[41] Timnit Gebru, Jamie Morgenstern, Briana Vecchione, Jennifer Wortman Vaughan,
Hanna Wallach, Hal Daumé Iii, and Kate Crawford. 2021. Datasheets for datasets.
Commun. ACM64, 12 (2021), 86–92. doi:10.1145/3458723
[42] Nicky Gregson, Mike Crang, and Constantinos N Antonopoulos. 2017. Holding
together logistical worlds: Friction, seams and circulation in the emerging ‘global
warehouse’.Environment and Planning D: Society and Space35, 3 (2017), 381–398.
doi:10.1177/0263775816671721
[43] Barbara Grosse-Hering, Jon Mason, Dzmitry Aliakseyeu, Conny Bakker, and
Pieter Desmet. 2013. Slow design for meaningful interactions. InProceedings
of the SIGCHI Conference on Human Factors in Computing Systems. ACM, Paris,
France, 3431–3440. doi:10.1145/2470654.2466472
[44] Joseph F Hair, Rolph E Anderson, Ronald L Tatham, and William C Black. 1998.
Multivariate data analysis. Prentice Hall, Upper Saddle River, NJ.
[45] Andrew F Hayes. 2017.Introduction to mediation, moderation, and conditional
process analysis: A regression-based approach. Guilford publications, New York,
NY.
[46] Se-Hoon Jeong, Hyunyi Cho, and Yoori Hwang. 2012. Media literacy interven-
tions: A meta-analytic review.Journal of communication62, 3 (2012), 454–472.
doi:10.1111/j.1460-2466.2012.01643.x
[47] Devon Johnson and Kent Grayson. 2005. Cognitive and affective trust in service
relationships.Journal of Business research58, 4 (2005), 500–507. doi:10.1016/S0148-
2963(03)00140-1
[48] Daniel Kahneman. 2011.Thinking, fast and slow. Macmillan, New York, NY.
[49] Karl Spencer Lashley et al. 1951.The problem of serial order in behavior. Vol. 21.
Bobbs-Merrill Oxford, Oxford, United Kingdom.
[50] John D Lee and Katrina A See. 2004. Trust in automation: Designing for appro-
priate reliance.Human factors46, 1 (2004), 50–80. doi:10.1518/hfes.46.1.50_30392
[51] Sangwook Lee, Won-Ki Moon, Jae-Gil Lee, and S Shyam Sundar. 2023. When
the machine learns from users, is it helping or snooping?Computers in Human
Behavior138 (2023), 107427. doi:10.1016/j.chb.2022.107427
[52] M. Liao and S. Shyam Sundar. 2025. Chat but verify: Combating misinformation
by Generative AI with verification affordance. Paper presented at the 75th Annual
Conference of the International Communication Association (ICA), Denver, CO.
[53] Vivian Liu and Lydia B Chilton. 2022. Design guidelines for prompt engineering
text-to-image generative models. InProceedings of the 2022 CHI conference on
human factors in computing systems. Association for Computing Machinery, New
York, NY, 1–23. doi:10.1145/3491102.3501825
[54] Leo S Lo. 2023. The CLEAR path: A framework for enhancing information literacy
through prompt engineering.The Journal of Academic Librarianship49, 4 (2023),
102720. doi:10.1016/j.acalib.2023.102720
[55] Edward McAuley. 1985. Modeling and self-efficacy: A test of Bandura’s model.
Journal of Sport and Exercise Psychology7, 3 (1985), 283–295. doi:10.1123/jsp.7.3.
283
[56] Thomas Mejtoft, Sarah Hale, and Ulrik Söderström. 2019. Design Friction. In
ECCE ’19: Proceedings of the 31st European Conference on Cognitive Ergonomics.
Association for Computing Machinery, New York, NY. doi:10.1145/3335082.
3335106
[57] Thomas Mejtoft, Emma Parsjö, Ole Norberg, and Ulrik Söderström. 2023. Design
friction and digital nudging: Impact on the human decision-making process. In
Proceedings of the 2023 5th International Conference on Image, Video and Signal
Processing. Association for Computing Machinery, New York, NY, 183–190. doi:10.
1145/3591156.3591183
[58] Margaret Mitchell, Simone Wu, Andrew Zaldivar, Parker Barnes, Lucy Vasserman,
Ben Hutchinson, Elena Spitzer, Inioluwa Deborah Raji, and Timnit Gebru. 2019.
Model cards for model reporting. InProceedings of the conference on fairness,
accountability, and transparency. Association for Computing Machinery, New
York, NY, 220–229. doi:10.1145/3287560.3287596
[59] Maria D Molina and S Shyam Sundar. 2022. When AI moderates online content:
effects of human collaboration and interactive transparency on user trust.Journal
of Computer-Mediated Communication27, 4 (2022), zmac010. doi:10.1093/jcmc/
zmac010
[60] Ethan Mollick. 2024.Thinking like an AI: A little intuition can help. https:
//substack.com/@oneusefulthing/p-150339904 Accessed: 2025-08-27.
[61] James W Moore. 2016. What is the sense of agency and why does it matter?
Frontiers in psychology7 (2016), 1272. doi:10.3389/fpsyg.2016.01272
[62] Leonardo Nicoletti and Dina Bass. 2023.Humans are biased. Generative AI is even
worse: Stable diffusion’s text-to-image model amplifies stereotypes about race and
gender - here’s why that matters. https://www.bloomberg.com/graphics/2023-
generative-ai-bias/ Accessed: 2025-08-27.
[63] Jakob Nielsen. 2023.The articulation barrier: Prompt-driven AI UX hurts us-
ability. https://www.linkedin.com/pulse/prompt-driven-ai-ux-hurts-usability-
jakob-nielsen/ Accessed: 2025-08-27.
[64] Edward Ongweso. 2019.Racial bias in AI isn’t getting better and neither are
researchers’ excuses. https://www.vice.com/en/article/racial-bias-in-ai-isnt-
getting-better-and-neither-are-researchers-excuses/ Accessed: 2025-08-27.
[65] Jonas Oppenlaender, Rhema Linder, and Johanna Silvennoinen. 2025. Prompting
AI art: An investigation into the creative skill of prompt engineering.International
journal of human–computer interaction41, 16 (2025), 10207–10229. doi:10.1080/
10447318.2024.2431761
[66] Isabel P. Riquelme and Sergio Román. 2014. Is the influence of privacy and
security on online trust the same for all type of consumers?Electronic Markets
24, 2 (2014), 135–149. doi:10.1007/s12525-013-0145-3
[67] Elizabeth M Perse. 1990. Involvement with local television news: Cognitive and
emotional dimensions.Human Communication Research16, 4 (1990), 556–581.
doi:10.1111/j.1468-2958.1990.tb00222.x
[68] W James Potter. 2010. The state of media literacy.Journal of Broadcasting &
Electronic Media54, 4 (2010), 675–696. doi:10.1080/08838151.2011.521462
[69] Shalini Ramachandran, Steven Matthew Cutchin, and Sheree Fu. 2021. Raising
algorithm bias awareness among computer science students through library and
computer science instruction. In2021 ASEE Virtual Annual Conference Content
Access. American Society for Engineering Education (ASEE), virtual conference.
doi:10.18260/1-2--37634
[70] Carson Jonathan Reynolds. 2001.The sensing and measurement of frustration
with computers. Master’s thesis. Massachusetts Institute of Technology. http:
//hdl.handle.net/1721.1/29170 Accessed: 2025-08-27.
[71] Dale H Schunk. 1987. Peer models and children’s behavioral change.Review of
Educational Research57, 2 (1987), 149–174. doi:10.3102/00346543057002149
[72] Weijia Shi, Anirudh Ajith, Mengzhou Xia, Yangsibo Huang, Daogao Liu, Terra
Blevins, Danqi Chen, and Luke Zettlemoyer. 2023. Detecting pretraining data
from large language models.arXiv preprint arXiv:2310.16789(2023).
[73] Rachel Skilton and Alison Cardinal. 2024. Inclusive prompt engineering: A
methodology for hacking biased ai image generation. InProceedings of the 42nd
ACM International Conference on Design of Communication. Association for Com-
puting Machinery, New York, NY, 76–80. doi:10.1145/3641237.3691655
[74] Anselm Strauss and Juliet Corbin. 1998.Basics of Qualitative Research Techniques.
Sage Publications, Thousand Oaks, CA.
[75] Victor J. Strecher, Brenda McEvoy DeVellis, Marshall H. Becker, and Irwin M.
Rosenstock. 1986. The role of self-efficacy in achieving health behavior change.
Health Education Quarterly13, 1 (1986), 73–92. doi:10.1177/109019818601300108
[76] Hari Subramonyam, Roy Pea, Christopher Pondoc, Maneesh Agrawala, and
Colleen Seifert. 2024. Bridging the gulf of envisioning: Cognitive challenges in
prompt based interactions with llms. InProceedings of the 2024 CHI Conference
on Human Factors in Computing Systems. Association for Computing Machinery,
New York, NY, 1–19. doi:10.1145/3613904.3642754
[77] S Shyam Sundar. 2020. Rise of machine agency: A framework for studying
the psychology of human–AI interaction (HAII).Journal of Computer-Mediated
Communication25, 1 (2020), 74–88. doi:10.1093/jcmc/zmz026
[78] S Shyam Sundar, Saraswathi Bellur, Jeeyun Oh, Haiyan Jia, and Hyang-Sook Kim.
2016. Theoretical importance of contingency in human-computer interaction:
Effects of message interactivity on user engagement.Communication Research
43, 5 (2016), 595–625. doi:10.1177/0093650214534962
[79] S Shyam Sundar, Haiyan Jia, T Franklin Waddell, and Yan Huang. 2015. Toward
a theory of interactive media effects (TIME): Four models for explaining how
interface features affect user psychology.The handbook of the psychology of
communication technology(2015), 47–86. doi:10.1002/9781118426456.ch3
[80] S Shyam Sundar and Jinyoung Kim. 2019. Machine heuristic: When we trust
computers more than humans with our personal information. InProceedings of
the 2019 CHI Conference on human factors in computing systems. Association for
Computing Machinery, New York, NY, 1–9. doi:10.1145/3290605.3300768
[81] Richard Tomsett, Alun Preece, Dave Braines, Federico Cerutti, Supriyo
Chakraborty, Mani Srivastava, Gavin Pearson, and Lance Kaplan. 2020. Rapid
trust calibration through interpretable and uncertainty-aware AI.Patterns1, 4
(2020). doi:10.1016/j.patter.2020.100049
[82] Henriikka Vartiainen, Juho Kahila, Matti Tedre, Sonsoles López-Pernas, and Nico-
las Pope. 2024. Enhancing children’s understanding of algorithmic biases in and
with text-to-image generative AI.new media & society(2024), 14614448241252820.
doi:10.1177/14614448241252820
[83] Ruotong Wang, F Maxwell Harper, and Haiyi Zhu. 2020. Factors influencing
perceived fairness in algorithmic decision-making: Algorithm outcomes, devel-
opment procedures, and individual differences. InProceedings of the 2020 CHI
conference on human factors in computing systems. Association for Computing

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Machinery, New York, NY, 1–14. doi:10.1145/3313831.3376813
[84] Kristie Wilder and Paul Mackun. 2025.An aging nation: U.S. median age surpassed
39 in 2024. https://www.census.gov/library/stories/2025/06/metro-areas-median-
age.html Accessed: 2025-11-10.
[85] Jeongwon Yang and Yu Tian. 2021. “Others are more vulnerable to fake news
than I Am”: Third-person effect of COVID-19 fake news on social media users.
Computers in Human Behavior125 (2021), 106950. doi:10.1016/j.chb.2021.106950
```

## Merged notes from duplicate

_Source file:_ `Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.sync-conflict-20260427-074346-LONMVRE.md`

[[Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf]]
## Full text (extracted from `Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf`)

*Source:* `2PDF/Prompt Coaching for Inclusiveness- A Media Literacy Approach  to Increase Users’ Awareness of Algorithmic Bias and Prompting  Efficacy.pdf`  
*Extracted:* 2026-04-27

```text
Prompt Coaching for Inclusiveness: A Media Literacy Approach
to Increase Users’ Awareness of Algorithmic Bias and Prompting
Efficacy
Cheng Chen
Oregon State University
Corvallis, OR, USA
chenc27@oregonstate.edu
Mengqi Liao
University of Georgia
Athens, GA, USA
mengqi.liao@uga.edu
Aditya Anand Phadnis
Pennsylvania State University
University Park, PA, USA
aap6117@psu.edu
Yao Li
Pennsylvania State University
University Park, PA, USA
ybl5753@psu.edu
Andrew High
Pennsylvania State University
University Park, PA, USA
ach208@psu.edu
Saeed Abdullah
Pennsylvania State University
University Park, PA, USA
saeed@psu.edu
S. Shyam Sundar
Pennsylvania State University
University Park, PA, USA
Sungkyunkwan University
Seoul, Republic of Korea
sss12@psu.edu
Abstract
Large language models often produce biased or stereotypical out-
puts. One way to reduce this possibility is to be more inclusive in
our prompts, but doing so may not come naturally to most users.
Therefore, we designed a tool that coaches users to write more
inclusive prompts—a strategy that leverages design friction to pro-
vide a media literacy intervention. Data from a user study (N=344)
show that compared to no coaching, inclusive prompt coaching
directly increased users’ awareness of algorithmic bias and their
perceived prompting efficacy. It also indirectly enhanced their trust
in the system and perceived trust calibration through cognitive
elaboration. However, inclusive prompt coaching resulted in a less
satisfying user experience. These findings have implications for
ethical interventions in prompting for better communicating and
combating algorithmic bias. We discuss the benefits and limitations
of inclusive prompt coaching, as well as ways to balance usability
for long-term adoption of generative AI systems.
CCS Concepts
•Human-centered computing→Empirical studies in HCI.
Keywords
Prompt coaching, Algorithmic bias awareness, Prompting efficacy,
Trust in AI, Inclusiveness, User experience
This work is licensed under a Creative Commons Attribution 4.0 International License.
CHI ’26, Barcelona, Spain
©2026 Copyright held by the owner/author(s).
ACM ISBN 979-8-4007-2278-3/2026/04
https://doi.org/10.1145/3772318.3791542
ACM Reference Format:
Cheng Chen, Mengqi Liao, Aditya Anand Phadnis, Yao Li, Andrew High,
Saeed Abdullah, and S. Shyam Sundar. 2026. Prompt Coaching for In-
clusiveness: A Media Literacy Approach to Increase Users’ Awareness
of Algorithmic Bias and Prompting Efficacy. InProceedings of the 2026
CHI Conference on Human Factors in Computing Systems (CHI ’26), April
13–17, 2026, Barcelona, Spain.ACM, New York, NY, USA, 16 pages. https:
//doi.org/10.1145/3772318.3791542
1 Introduction
Generative AI has transformed content creation by enabling the
rapid and efficient generation of novel outputs across various do-
mains. However, most publicly available generative AI systems
are biased, largely due to the nature of their training data. Algo-
rithmic bias is broadly defined as a systematic difference between
an algorithm’s behavior or outcomes and a chosen reference stan-
dard [30, 36]. This study focuses on harmful cases where computer
systems systematically and unfairly discriminate against certain
groups of individuals in favor of others [11].
Examples of such biases include the AIportraits App, which light-
ened the skin tones of people of color [64]; the image-generative AI
Stable Diffusion, which suggested mostly White individuals when
prompted to generate images of professionals in higher-paying oc-
cupations such as lawyers and engineers, while suggesting mostly
Non-White individuals when portraying lower-paying profession-
als such as janitors and cashiers [62]; and DALL-E, which dispropor-
tionately favored characteristics deemed socially desirable, such as
being young, beautiful, skinny, and white, over providing realistic
depictions of diverse individuals [40, 73]. These cases demonstrate
the tendency of generative AI models to promote biased and stereo-
typical portrayals of certain groups of individuals, causing repre-
sentational harm, particularly to users from minority communities.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Algorithmic bias is fundamentally a system-level problem. Pre-
vious studies have consistently identified unrepresentative training
data as the primary source of algorithmic bias [ 3, 10, 23, 26]. In-
formed by the documentation paradigm [ 41, 58], several studies
have sought to disclose training data characteristics to help lay users
recognize biases in machine learning models [3, 20, 21]. Although
this approach has been demonstrated to be effective, generative
AI systems powered by large language models (LLMs) present a
unique challenge given their reliance on extensive, Internet-wide
training datasets [ 17, 60]. As a result, the datasets used to train
LLMs are rarely disclosed [72]. This challenge, coupled with the
strong need for AI transparency, has motivated computer scientists
to explore innovative solutions to combat biases in generative AI
models, such as revealing pretraining datasets of LLMs [17, 72] or
incorporating more inclusive data from lesser-represented cultures,
oral traditions, and localized archives [1].
Despite ongoing efforts, users often fail to recognize racial bias
in AI algorithms [18]. The underlying reasons for this lack of aware-
ness are complex. Previous research has shown that users’ racial
backgrounds [18] and in-group biases [83] can contribute to their
tendency to overlook racial and other types of biases embedded
in these systems. In addition, individuals’ unreflective use of Chat-
GPT and other commercially available LLMs may also reduce their
awareness of algorithmic bias.
To improve users’ awareness of algorithmic bias, we draw from
prior research on prompt design and prompt engineering [9, 19, 53,
76] and propose a different strategy, calledinclusive prompt coaching,
to communicate and combat algorithmic bias in generative AI mod-
els. This approach leverages the affordance of promptability [19]
and guides users to come up with more inclusive prompts for image
generation. Previous studies have shown that a well-crafted prompt
can produce more diverse and inclusive images under certain con-
ditions [27, 32, 73]. Extending this line of research, the current
study examines how users perceive, experience, and engage with
an image-generative AI tool that provides inclusive prompt coach-
ing and studies its effects on their awareness of algorithmic bias,
confidence in crafting inclusive prompts (i.e., prompting efficacy),
trust in the AI tool, and perceived trust calibration.
To achieve this goal, we conducted an online experiment with
344 participants, in which participants were randomly assigned to
interact with a new image-generative AI tool that either provided
inclusive prompt coaching, detailed prompt coaching (which serves
as an active control as it requires roughly the same amount of
interaction from users), or no coaching. The last two conditions
served as control conditions. Our findings showed that the effects of
inclusive prompt coaching were mixed. On the one hand, it directly
increased users’ awareness of algorithmic bias and their perceived
prompting efficacy, and indirectly enhanced users’ trust in the AI
tool and perceived trust calibration through cognitive elaboration.
On the other hand, it resulted in a less satisfying user experience.
This study contributes to the literature by proposing and testing
a new strategy—"inclusive prompt coaching"—for communicating
and combating algorithmic bias in generative AI models. It comple-
ments existing documentation-based approaches in raising users’
awareness of algorithmic bias [41, 58]. By coaching users to write
inclusive prompts, the goal is not to shift the responsibility for mit-
igating algorithmic bias from developers to lay users, but to offer
user-centered design strategies that empower them to navigate
algorithmic bias through advanced prompting skills. We would not
only like to raise users’ awareness and understanding of algorithmic
bias, but also, ultimately, actively involve users in recognizing and
addressing algorithmic bias through prompting to reduce biased
outputs.
Another contribution is the identification of a psychological
mechanism, namely increased cognitive elaboration, through which
inclusive prompt coaching influences users’ trust in a new gener-
ative AI system and their perception of trust calibration, namely,
one’s perceived ability to align their trust level with the AI’s ac-
tual trustworthiness. These findings advance our understanding of
how responsible AI can be fostered through user perceptions and
highlight potential pathways that can lead to this positive outcome.
Third, this study provides an example of how to incorporate
inclusive prompt coaching into users’ interactions with a generative
AI system. This example can be adapted to different contexts. We
believe that this study serves as a starting point for AI designers to
think about how to facilitate users’ prompt design while helping
them recognize and mitigate bias in AI outputs.
2 Theoretical Frameworks
We draw on two theoretical frameworks to guide the conceptualiza-
tion of our study: media literacy intervention and design friction.
2.1 Media Literacy Intervention
Broadly speaking, media literacy interventions are education pro-
grams aimed at minimizing the negative effects of media by educat-
ing individuals about the motivations and processes that underlie
the creation and consumption of specific media content, thereby
re-shaping their media-related beliefs and attitudes and reducing
detrimental behaviors and outcomes related to media use [46]. By
providing people with knowledge structures and skills, the goal
of media literacy is to help users maintain “critical autonomy in
relationship to all media” [5, p. 9].
Some studies have used the media literacy intervention approach
to increase individuals’ awareness and understanding of algorithmic
bias. For example, Ramachandran et al. [69] integrated algorithmic
bias education into a computer science curriculum and highlighted
the varied student reactions to the issue of algorithmic bias and the
importance of multidisciplinary teaching. Likewise, Vartiainen et al.
[82] provided educational workshops that focused on the design of
AI-driven apps. These workshops helped children and young adults
understand that training data is the primary cause of algorithmic
bias in text-to-image generative models.
In particular, most media literacy interventions are provided
prior to exposure to media content, either to inoculate people
against the negative media effects or to counter the already ex-
isting negative effects [68]. This design may not be ideal for tech
companies or users. For tech companies, there is little motivation
to reveal the biases in their models to users. Similarly, offering
educational tutorials or lectures before users’ interaction with their
systems can feel unnatural, cognitively demanding, and delay users’
access. On the users’ side, traditional media literacy interventions
may not align with their needs, particularly when they prioritize
efficiency and productivity [ 2]. Furthermore, most users cannot

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
be expected to go through media literacy training before using a
technology. What is needed is a more seamless and natural interven-
tion that occurs during use, a solution that allows users to acquire
knowledge and skills related to media use in real time, helping
them become more aware of algorithmic bias in the moment of use
and increasing their ability to generate more inclusive and diverse
content using AI.
2.1.1 Intervention During Prompting.Previous studies have ex-
plored the strategy of “ethical natural language intervention” to
encourage the generative AI model to behave more ethically. For
example, Bansal et al. [9] proposed a method by appending certain
inclusive phrases (e.g., “if all individuals can be a lawyer irrespec-
tive of their gender”) to the base prompt (e.g., “a photo of a lawyer”)
for diverse AI outputs, and they found that this linguistic interven-
tion to be effective. Fraser et al. [ 40] replicated this method and
found that this strategy was only effective in one direction, i.e., it
improved the representation of darker-skinned people for socially
positive prompts (e.g., a lawyer), but it did not reduce their repre-
sentation in response to socially negative prompts (e.g., a felon).
They attributed this outcome to the inability of language models to
understand complicated grammar and the difficult words used in
the prompt intervention.
While informative, these studies focus on testing the responsive-
ness of LLMs to prompting interventions rather than on enabling
users to generate prompts that would result in less biased outcomes.
In the absence of data pertaining to users’ perceptions of–and re-
sponses to–such interventions, it remains unclear whether this
approach is effective in enhancing users’ awareness of algorithmic
bias and other user-centered outcomes. To overcome this research
gap, our study focuses on how lay users perceive, experience, and
engage with a media literacy intervention designed to help them
write more inclusive prompts.
2.2 Design Friction: Positive and Negative
Effects
Viewed from the perspective of HCI, media literacy interventions
can be understood as a form ofdesign friction, which refers to “the
points of difficulty encountered during users’ interaction with a
technology” [28, p. 1390]. While UX designers typically strive to
remove causes of friction and create seamless interactions [ 24],
intentionally incorporating small difficulties can serve construc-
tive purposes, such as promoting more reflective, informed, and
safe behaviors [ 12, 57], sparking conversations and discussions
around socio-technical issues of greater complexity [37], and even
facilitating task completion [42].
Aligned with the principles of Slow Design [43] and the notion
of Seamful Design [16], design friction creates "microboundaries"
[28] by deliberately slowing users down in the process of task
completion to encourage mindful engagement. By interrupting
automatic or rushed actions, design friction helps prevent errors
and prompts users to pay closer attention to the task at hand [34, 57].
A growing body of research has consistently demonstrated the
effectiveness of design friction in promoting conscious interactions
and supporting positive behavioral change [28, 34, 57].
A key factor contributing to the effectiveness of design friction
is its ability to prompt users to think and reflect. Kahneman [48]
described two systems of human thinking: System 1, which is fast,
intuitive and relatively low effort, and System 2, which is slower,
more deliberate, and more effortful. While System 1 guides most ev-
eryday actions, System 2 is engaged for more complicated tasks, as it
facilitates more thoughtful processing. By introducing small difficul-
ties in an AI’s interface, design friction can encourage a shift from
System 1 to System 2 thinking. These purposeful slowdowns create
a moment of pause that invites "cognitive elaboration, " defined as
the process of relating new information to existing knowledge to
guide the task at hand [67].
However, a potential drawback of introducing design friction
is that it might undermine user agency, which is defined as the
extent to which individuals believe that they can influence the
actions and outcomes of an AI system [ 61]. Altering users’ task
flow or adding extra steps before task completion can make users
feel as though they have less control over the technology. That said,
previous research suggests that design friction does not necessarily
decrease user satisfaction, as long as users understand beforehand
the purpose and rationale behind the intervention [56].
Building on these theoretical frameworks, we review related
work to explain the novelty of the inclusive prompt coaching inter-
vention and present the rationale for examining the effects of this
intervention.
3 Related Work
Unlike changing users’ prompts behind the scenes without their
awareness or participation, the inclusive prompt coaching approach
focuses on AI-assisted prompt design before image generation. By
alerting users to potential biases in generative AI models and offer-
ing more inclusive prompt suggestions, this approach encourages
users to pause and reflect on the inclusiveness of their prompt de-
sign for more representative and diverse image outputs. Given the
study goals, we focus on the following outcomes to observe the
effects of the inclusive prompt coaching intervention: awareness of
algorithmic bias, trust in the AI system, perceived trust calibration,
and perceived prompting efficacy. We explain each concept below.
3.1 Effects on Awareness of Algorithmic Bias
One major outcome we anticipate is the increased awareness of
algorithmic bias, which we define as users’ ability to recognize that
generative AI outputs do not reflect the diversity of human expe-
riences. This conceptualization aligns with the observation that
image-generative AI systems often produce biased or stereotypical
outputs, particularly against individuals from minority communi-
ties [62]. However, it is unclear whether the increased awareness of
algorithmic bias is due to the focus on improving the "inclusivity"
aspect of prompt design, heightened user involvement, or both.
To investigate this, we introduce two control conditions: one in
which users are guided to write detailed prompts following the
same procedure as inclusive coaching, and another in which users
receive no coaching from the AI system.
Notably, inclusive prompt coaching conceptually differs from de-
tailed prompt coaching by emphasizing different aspects of prompt
improvement: inclusive coaching focuses on inclusivity, aiming to
produce more representative and diverse image outputs, whereas
detailed coaching emphasizes specificity to help users generate

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
more vivid and precise images. Since both types of coaching re-
quire a similar level of user engagement and reflection, detailed
prompt coaching serves as an active control condition to help disam-
biguate the effects of sheer implementation of prompt coaching and
those of the nature of that coaching (inclusiveness vs. detailedness).
Drawing on the notion of priming [49], defined as "the temporary
internal activation of response tendencies, " we predict that just-in-
time coaching that encourages inclusive prompt coaching will be
more effective in raising users’ awareness of algorithmic bias than
either advising them to provide more detailed prompts or offering
no coaching at all. Unlike these latter approaches, inclusive prompt
coaching is likely to specifically activate the concept of ‘inclusivity’
in users’ minds, resulting in higher awareness of algorithmic bias.
3.2 Effects on User Trust and Perceived Trust
Calibration
User trust is another construct that can be influenced by inclusive
prompt coaching. Based on the definition of trust in automation
[50], we define trust in AI as the extent to which users believe that
the system will work on their behalf under uncertainty. Following
previous research [47, 50, 59], we view trust as a multi-dimensional
construct and further differentiate between cognitive trust (belief
in the AI’s integrity and capability), affective trust (emotional bond
between the user and the system), and behavioral trust (intention to
use/adopt) for a more comprehensive evaluation of the formation
of user trust when interacting with a new image-generative AI
system.
Given that trust can be formed through both heuristic and sys-
tematic information processing [77, 79], trust in a system based on
a one-time interaction may be misplaced. For this reason, we also
examine perceived trust calibration, which is defined as the extent
to which users perceive that their trust level is aligned with the
AI’s true trustworthiness [19, 52, 81]. Considering that matching
one’s trust level with the perceived true capabilities of the system
often requires thoughtful evaluation guided by prior knowledge of
AI, we view perceived trust calibration as an indicator of warranted
and responsible trust based on users’ assessment.
3.2.1 Mediating Role of Cognitive Elaboration.One way that in-
clusive prompt coaching could shape users’ trust in AI systems is
through heightened cognitive elaboration. A recent study showed
that helping users design detailed prompts encouraged them to
think more deeply about their ideas, which, in turn, resulted in
higher perceived trust calibration [19]. Considering this, we predict
that inclusive prompt coaching will encourage more reflection on
inclusive prompt design, thus forming higher trust in the system
and enhanced perception of trust calibration.
3.2.2 Mediating Role of Perceived User Agency.In addition, by
revealing multiple possibilities for steering AI outputs toward in-
clusivity, inclusive prompt coaching may increase perceived user
agency, which is defined as the extent to which users feel they
have control over the actions and consequences of a system [61].
However, one downside of inclusive prompt coaching is that it
changes users’ initial prompts for inclusivity considerations. This
may be viewed as undermining user agency if users are firm in their
original ideas or do not have inclusive goals to begin with. Similarly,
nudging users to alter their prompts for inclusivity may be seen as a
threat to their freedom of action, which can result in psychological
reactance [33], potentially leading to worse evaluation outcomes,
such as lower trust in the system and reduced perception of trust
calibration.
3.3 Effects on Prompting Efficacy
A vast body of research highlights the important role of self-efficacy,
i.e., the belief in one’s ability to engage in or execute a behavior,
in driving behavioral change [8, 75]. Drawing on Bandura’s con-
ceptualization of self-efficacy [6], this study introduces perceived
prompting efficacy, a new concept that refers to users’ confidence
in their ability to create effective prompts for generating inclusive
AI outputs.
One possible explanation for the effect of inclusive prompt coach-
ing on increased prompting efficacy is modeling [55]. Informed by
Schunk’s [71] conceptualization, we define modeling as the process
by which individuals pattern their behaviors after those displayed
by AI. By observing how the system flags potentially biased or
stereotypical words in users’ original prompts and suggests more
inclusive prompts, users may learn from the system and mimic its
approach for designing more inclusive prompts. Previous research
highlights that modeling is an important approach for acquiring
literacy skills [71], such as inclusive prompt coaching in our case.
However, if prompting efficacy is based on learning, there might
not be enough time to learn in a one-shot interaction. In addition,
because these inclusive prompt suggestions are automated, the lack
of an explanatory context may limit users’ understanding of how to
craft inclusive prompts independently. Moreover, users who have a
strong belief in the positive machine heuristic, i.e., the belief that
machines are more objective and neutral than humans [80], may
rely on AI-generated prompts rather than actively engaging in the
process of creating and refining prompts for inclusivity. Due to
multiple possibilities, this study explores how inclusive prompt
coaching influences users’ perception of prompting efficacy.
3.4 Effects on User Experience
Last, we seek to examine the user experience (UX) of inclusive
prompt coaching by focusing on six indicators: perceived contin-
gency, helpfulness, frustration, mental effort, user interface (UI)
satisfaction, and liking of the system. These indicators are com-
monly used to evaluate the UX of new systems [19, 25, 70]. Among
all the factors, UI is an important aspect of UX, focusing on how the
presence of certain elements, such as messages, icons, and buttons,
influences users’ reactions to the system [25].
It is acknowledged that prompting or prompt engineering is a
new skill. Nielsen [62] pointed out that more than half of the US
adults have difficulty articulating their thoughts in a written format
[63]. Similarly, Oppenlaender et al. [ 65] found that users lacked
style-specific vocabularies when prompting with image-generative
systems. Moreover, Chen et al. [19] showed that lay users benefit
from prompt coaching as they do not know when to specify their
prompts while interacting with new image-generative systems for
the first time. A more recent study found that an image-generative
AI system guided by the Chain-of-Thought prompting strategy is
perceived as more helpful and easier to use than a system without

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
a prompting strategy [22]. Thus, coaching users to write inclusive
prompts may reduce perceived difficulty and mental effort, as well
as increase perceived helpfulness of the system. Viewed from this
perspective, any coaching would be a welcome addition for users.
However, additional steps in the interaction may increase users’
cognitive load, resulting in greater frustration, perceived difficulty,
and effort. Given that perceived ease of use is critical to adopting
new technologies [31], the increased difficulty and effort may re-
duce system liking and UI satisfaction. Furthermore, nudges for
inclusivity could disrupt workflow, reducing the perceived con-
tingency of interactions between the system and the user, thus
negatively affecting the overall user experience.
4 Current Study
Based on the aforementioned rationale and the motivation to un-
derstand how users perceive, experience, and engage with a new
image-generative AI system that provides inclusive prompt coach-
ing, we propose the following hypotheses and research questions:
H1:Inclusive prompt coaching will increase users’ awareness of
algorithmic bias compared to the detailed prompt coaching condi-
tion (H1a) and the absence of prompt coaching condition (H1b).
H2:Inclusive prompt coaching will increase users’ cognitive
elaboration, which will, in turn, be associated with higher trust in
the AI system (H2a) and enhanced perception of trust calibration
(H2b), compared to the absence of prompt coaching.
RQ1:What role, if any, does user agency play in the relationship
between inclusive prompt coaching and users’ trust in the AI system
and their perceived trust calibration?
RQ2:How does inclusive prompt coaching influence perceived
prompting efficacy for inclusive AI outputs?
RQ3:How does inclusive prompt coaching affect UX?
5 Method
To examine the hypotheses and answer our research questions,
we conducted a user study with 344 participants. We developed a
new text-to-image generative AI application using Streamlit and
OpenAI’s API, with DALL-E 3’s image generation capability. We
created three versions of the generative AI application, offering
either inclusive prompt coaching, detailed prompt coaching, or no
prompt coaching. The latter two served as control groups.
The study was approved by the Institutional Review Board at
the first author’s university and pre-registered on the Open Science
Framework (OSF)’s website before data collection. The purpose
of pre-registration is to enhance transparency and research rigor,
which strengthens the credibility of our results. However, we did
not pre-register the qualitative analysis of users’ behavioral data
and open-ended responses, as these analyses were exploratory in
nature and intended to identify emergent patterns that could com-
plement the quantitative findings. Details of the pre-registration
are available at this link: https://osf.io/jdyaf/overview.
5.1 Development of Generative AI Applications
We used meta-prompting to guide the actions of each generative
AI application, as described below.
5.1.1 Meta-Prompting the Inclusive Prompt Coaching System.The
inclusive prompt coaching system was instructed to role-play as
an expert in identifying unconscious bias, stereotypes, and rep-
resentational issues in character descriptions. Specifically, it was
tasked with detecting subtle biases related to: (1) gender roles and
expectations, (2) cultural and ethnic stereotypes, (3) physical ap-
pearance assumptions, (4) age-related prejudices, and (5) socioe-
conomic stereotypes. The system was then instructed to provide
a standardized disclaimer about the potential for biased or stereo-
typical outputs due to AI training. Following this, the system was
asked to analyze the users’ prompts and generate one clear, spe-
cific sentence highlighting the most significant bias or stereotype
that could emerge in the visual representation. For suggestions, the
system acted as an expert in rewriting character descriptions to be
more inclusive, following three principles: (1) preserve the original
character concept, (2) remove potentially biased language, and (3)
provide only the rewritten prompt without explanation. The codes
for developing the inclusive prompt coaching system are available
at this link: https://github.com/AnonymousUser12345678/Prompt-
Coaching_Inclusiveness
5.1.2 Meta-Prompting the Detailed Prompt Coaching System.The
detailed prompt coaching system was asked to role-play as an ex-
pert in analyzing character descriptions for storytelling and visual
representation. It was instructed to identify areas where the de-
scription lacked sufficient detail—for example, vague or generic
physical descriptions, missing personality traits or motivations,
lack of background or context, absence of unique characteristics
or quirks, or insufficient information about the character’s role
or purpose. The system was then instructed to provide a stan-
dardized disclaimer about the potential for surprising or random
outputs when the prompts lack detail. After this, it was asked
to analyze users’ prompts and identify the most significant gap
in detail for creating a comprehensive visual or narrative repre-
sentation. To enhance the richness of character descriptions, the
system acted as an expert in adding specificity. Its tasks were
to: (1) maintain the core concept of the original character, and
(2) expand slightly on personality traits, background, and unique
characteristics. The system was instructed to provide only the
enhanced description without additional explanation. The codes
for developing the detailed prompt coaching system are available
at this link: https://github.com/AnonymousUser12345678/Prompt-
Coaching_Detailedness
5.1.3 Meta-Prompting the No Prompt Coaching System.The AI
application without prompt coaching was instructed to generate
an image directly from the users’ prompts. The codes for the no
prompt coaching system are available at this link: https://github.
com/AnonymousUser12345678/No-prompt-coaching.
5.2 Study Procedure and Task Flow
The main study consisted of three parts: 1) Completing a pre-
questionnaire, 2) Interacting with a new AI tool, and 3) Filling out
the post-questionnaire. After participants provided their informed
consent, they were given a definition of generative AI and examples
of its applications. They were then asked about their frequency of
generative AI use for various purposes and modalities (e.g., text,
image, video generation) and their perceived AI literacy.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Next, participants were informed that the research team had de-
veloped a new image-generative AI tool and that they were invited
to try it out and provide feedback. Participants were then randomly
assigned to interact with one of three versions of the AI tool, which
provided inclusive, detailed, or no prompt coaching.
5.2.1 First-Round AI Tool Interaction.In all conditions, the system
first introduced itself as a text-to image generative AI system de-
signed to bring fantasy characters to life and asked participants
what they would like to create. Next, in line with the concept of
design friction, we introduced small difficulties into users’ interac-
tion with the AI system in order to encourage reflection on either
the inclusivity or the level of detail in prompt design and image
generation.
Manipulation of Inclusive Prompt Coaching.After submit-
ting their initial prompts, participants in the inclusive prompt coach-
ing condition received a standardized warning about the potential
biases in AI image generation due to the nature of its training
data (see Figure 1). The warning message was kept the same for
all participants to maintain consistency. The tool then analyzed
participants’ initial prompts, identified words or phrases that might
lead to biased or stereotypical output, and suggested an alternative
prompt tailored to their original input. Following this, participants
decided the final prompt they wished to use for image generation.
Manipulation of Detailed Prompt Coaching.The detailed
prompt coaching condition followed a similar task flow, but with-
out any mention of inclusiveness. Participants received a warning
message highlighting that insufficient detail in the prompts could
lead to unexpected or random AI output (see Figure 2). The system
then analyzed participants’ prompts, identified areas where addi-
tional specificity was needed, and provided a more detailed version
based on their input. As in the inclusive prompt coaching condition,
participants in the detailed coaching condition had a final say in
selecting their preferred prompt for image generation. This condi-
tion served as an effort-equivalent control to the inclusive prompt
coaching condition, in that the coaching and effort involved were
about the same, but without the nudge to make the prompts more
inclusive (making this element the only difference across the two
conditions).
Manipulation of No Prompt Coaching.In contrast, partici-
pants in the no prompt coaching condition submitted their initial
prompts, and the AI tool generated the image without offering any
coaching. This served as a baseline condition, against which we
could assess the effects of the sheer presence of prompt coaching,
regardless of its content.
After receiving the AI-generated image, participants in all con-
ditions evaluated the image quality on a 7-point scale (1=very un-
satisfied and 7=very satisfied) and provided feedback on the AI-
generated image. Participants in the inclusive and detailed prompt
coaching conditions were asked, respectively, "Do you have any
additional comments on the inclusiveness/detailedness of the AI-
generated image?"
5.2.2 Second-Round AI Tool Interaction.Following this, partici-
pants in the inclusive and detailed coaching conditions completed
a follow-up task, in which they were asked to craft an inclusive
or detailed prompt for a randomly assigned occupation, such as
a teacher, secretary, and doctor. These occupations were chosen
for their potential to elicit biased and stereotypical outputs [ 62].
This step aimed to assess participants’ actual prompting efficacy
without the presence of prompt coaching. After image generation,
participants in these two conditions evaluated the quality of the
second AI-generated image using the same 7-point scale (1=very
unsatisfied and 7=very satisfied). By contrast, the no-prompt coach-
ing condition did not include the testing of prompt design for a
randomly assigned occupation.
At the end of the interaction, all participants clicked the “Save
& Receive Code” button to proceed to the post-questionnaire.
5.3 Measures
After interacting with the AI tool, we measured the mediating and
dependent variables of interest. All items were rated on a 7-point
scale, except UI satisfaction, which was evaluated on a 9-point scale.
A full list of measures is available in the OSF pre-registration.
5.3.1 Cognitive Elaboration.Measures for cognitive elaboration
were modified from previous research [19, 67]. Items include 1) “I
thought about how to create my prompts to achieve desirable out-
puts, ” 2) “I thought about the kind of image my prompts would gen-
erate, ” and 3) “I found myself connecting how I wrote my prompts
with my knowledge of AI image generation. ” We averaged the three
items to create an index (M= 5.58,SD= .93, Cronbach’s𝛼= .72).
5.3.2 Perceived User Agency.Following previous studies [ 21, 59],
we used three items to measure perceived user agency. Sample
items include: “I felt I had control over how the AI tool works” and
“I could get the AI tool to do the things I wanted it to. ” An index
was created by averaging the three items, which was reliable (M=
4.91,SD= 1.37, Cronbach’s𝛼= .90).
5.3.3 Perceived Algorithmic Bias.We created five items to assess
users’ awareness of algorithmic bias, such as “I am aware that
generative AI outputs do not reflect a diverse range of human
experiences” and “I am mindful that AI tools can reinforce harmful
stereotypes in image generation. ” We averaged the five items to
form an index of algorithmic bias awareness, which was reliable
(M= 5.01,SD= 1.18, Cronbach’s 𝛼 = .87). The Skewness (-.675)
and Kurtosis (.554) of algorithmic bias awareness were within the
acceptable range for normality, according to the criteria proposed
by Hair et al. [44].
5.3.4 Trust in AI.Aligned with the multi-dimensional conceptual-
ization of trust, we measured cognitive trust (4 items from [29, 66]);
e.g., “I can trust the performance of the AI tool to be good”), affective
trust (4 items from [21]); “The AI tool displayed a warm and caring
attitude towards me”), and behavioral trust (4 items from [4, 21]);
“I plan to adopt the AI tool in the future”), separately. Indices were
created by averaging the items belonging to each concept, which
were all reliable (Cognitive trust:M= 5.05,SD= 1.30, Cronbach’s
𝛼 = .93; Affective trust:M= 4.26,SD= 1.49, Cronbach’s 𝛼 = .88;
Behavioral trust:M= 4.85,SD= 1.52, Cronbach’s𝛼= .94).
5.3.5 Perceived Trust Calibration.We adopted five items from [ 19]
to measure perceived trust calibration. Sample items include: “I feel
I am able to calibrate my trust in the AI tool during my interaction
with it” and “I think now my level of trust in the AI tool matches its

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
Figure 1: Visual stimuli from the inclusive prompt coaching condition, showing the interface’s warning about biased language
and the system’s suggested inclusive rewrite
actual capabilities. ” We averaged the five items to create an index
(M= 5.02,SD= .93, Cronbach’s𝛼= .79).
5.3.6 Perceived Prompt Efficacy.Drawing on our explication of
self-efficacy, we developed the following three items to evaluate
prompting efficacy for inclusive AI outputs: 1) “I am confident in
creating effective prompts to reduce biases in AI images, ” 2) “I can
create inclusive prompts to mitigate bias in generative AI models, ”
and 3) “I can steer diverse AI outputs through effective prompting. ”
An index was created by averaging the three items, which was
reliable (M= 5.04,SD= 1.22, Cronbach’s𝛼= .88).
5.3.7 User Experience (UX).We used six indicators to evaluate UX,
including perceived contingency (6 items adapted from [78], 3 items
left after removing cross-loaded items; e.g., “I felt as if the AI tool
gave an exclusive response to my inputs”), perceived helpfulness of
the AI system (4 items adapted from [51]); “The AI tool was working
on my behalf”), UI satisfaction (measured by six paired adjectives
from [25]) on a 9-point scale, e.g., “terrible/wonderful”), perceived
frustration (one question; “How frustrating was the experience
with the AI tool?”), perceived mental difficulty (one question; “How
mentally difficult was it to use the AI tool?”), and liking of the AI
tool (one question; "Did you like using the AI tool?"). The indices
of perceived contingency (M= 5.47,SD= 1.00, Cronbach’s 𝛼 = .78),
perceived helpfulness (M= 5.32,SD= 1.15, Cronbach’s 𝛼 = .88),
and UI satisfaction (M= 7.07,SD= 1.60, Cronbach’s 𝛼 = .93) were
reliable.
5.3.8 Control Variables.Given that the task was related to image
generation, we controlled for users’ prior experience with this
specific use case. In the pre-questionnaire, we asked participants
how often (1 = did not use at all and 6 = used several times each

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Figure 2: Visual stimuli from the detailed prompt coaching condition [baseline condition], showing the interface’s warning
about vague or underspecified prompts and the system’s suggested detailed rewrite to enhance prompt specificity.
day) they had used AI for image generation in the past six months
(M= 2.99,SD= 1.51).
In addition, we added perceived AI knowledge as a covariate
since it may influence users’ awareness of algorithmic bias and
prompting efficacy. Modified from prior research [85], participants
were asked to indicate their level of agreement (1 = strongly disagree
and 7 = strongly agree) with the following five statements: 1) In
general, I know a lot about generative AI; 2) I understand how
generative AI works; 3) I know what generative AI can do; 4) I
understand the benefits of generative AI; and 5) I understand the
limitations of generative AI. We created an index by averaging the
five items (M= 5.02,SD= 1.12, Cronbach’s𝛼= .89).
5.4 Construct Validity
Based on Fornell and Larcker’s [ 38] criteria, convergent validity
was inferred if the average variance extracted (AVE) was greater
than .50 and composite reliability (CR) was higher than .70. Dis-
criminant validity was inferred if the square root of AVE for each
variable exceeded all correlation coefficients involving that con-
struct. Following these criteria, all constructs showed good validity,
as shown in Table 1.
5.5 Participants
A recent study reported a small effect of prompt coaching on per-
ceived trust calibration through increased cognitive elaboration
[19]. Considering the exploratory nature of the study, we set the
effect size at the medium level within the small effect range (f= .17).
Ana-prioripower analysis using G*Power [ 35] suggested that at
least 337 participants were needed to achieve .80 power at the stan-
dard .05 alpha error probability. We recruited 355 participants from
Prolific to account for potential exclusion of incomplete and inat-
tentive responses. Participants who were 18 years old or above and
lived in the United States were eligible to participate in the study.

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
AVE CR 1 2 3 4 5 6 7 8 9 10 11
Elaboration (1) .66 .85 .81
Agency (2) .83 .84 .41*** .91
Bias awareness (3) .67 .91 .22*** .04 .82
Cognitive Trust (4) .63 .97 .38*** .70*** -.04 .79
Affective Trust (5) .74 .92 .26*** .60*** -.04 .70*** .86
Behavioral Trust (6) .85 .96 .30*** .60*** -.04 .74*** .72*** .92
Calibration (7) .57 .86 .50*** .43*** .16*** .50*** .49*** .50*** .75
Efficacy (8) .81 .93 .46*** .50*** .19*** .62*** .56*** .56*** .52*** .90
Contingency (9) .70 .88 .39*** .56*** .05 .61*** .42*** .51*** .52*** .49*** .84
Helpfulness (10) .74 .92 .38*** .59*** -.01 .72*** .58*** .64*** .52*** .55*** .58*** .86
Satisfaction (11) .73 .94 .32*** .66*** -.02 .76*** .62*** .72*** .49*** .56*** .61*** .72*** .85
Note.Bold values on the diagonal are square root of AVE. ***p< .001, **p< .01, *p< .05.
Table 1: Construct Validity of Key Study Variables
We paid participants $3 for the task, which took approximately 15
minutes to complete.
After removing those who failed the attention checks, 344 partic-
ipants remained in the final sample. Of these, 113 belonged to the
inclusive prompt coaching condition, 118 to the detailed prompt
coaching condition, and 113 to the no coaching condition.
Demographically, our sample consisted of slightly more males
(50%) than females (46.8%), and participants who chose non-binary
(2.3%) or did not reveal their gender (0.9%). Their ages ranged from
18 to 67 years (M= 34.13,SD= 10.92). The median educational
background was a bachelor’s degree, and the median family income
was between $50,000 and $75,000 per year. The sample was pre-
dominantly White (57.3%), followed by Black or African American
(30.8%), Asian (7.8%), Hispanic/Latino origin (5.2%), and American
Indian or Alaska Native (0.3%). One participant preferred not to
reveal their race and/or origin.
5.6 Data Analysis Plan
We used Analysis of Covariance (ANCOVA) to answer H1, which
focused on the effects of inclusive prompt coaching on perceived
algorithmic bias, and RQ2, which examined the effect of prompt
coaching on prompting efficacy. To examine the mediating role of
cognitive elaboration (H2) and perceived user agency (RQ1), we
used Model 4 from PROCESS Macro [45], with 5,000 bootstrap re-
samples and 95% percentile bootstrap confidence intervals (CIs).
RQ3, which explored the effects of inclusive prompt coaching on UX,
was examined using Multivariate Analysis of Covariance (MAN-
COVA). We entered self-reported frequency of using image gener-
ating AI (over the last six months) and perceived AI knowledge as
covariates in all quantitative analyses.
In addition to quantitative data, we collected behavioral data
and user responses during their interaction with the AI system
and in the post-questionnaire. Following the open-ended coding
techniques outlined by Strauss and Corbin [74], we analyzed these
responses. The first author carefully reviewed all responses and cat-
egorized user comments according to the mediating and dependent
variables examined in the quantitative analysis, such as algorithmic
bias awareness, perceived user agency, and user experience. The
resulting categorization was then shared with the co-authors for
validation, and any discrepancies in coding were resolved through
group discussions.
6 Results
We first examine the effectiveness of prompt coaching manipula-
tions and then report the results for each research question/hypothesis.
We present the qualitative results at the end of this section.
6.1 Manipulation Check
After interacting with the AI tool, participants were asked to report
their level of agreement with the following statements: 1) “The AI
tool provided alternative prompts for me to consider, ” 2) “The AI
tool identified potential issues in my prompts, ” and 3) “The AI tool
checked how good I was at writing prompts. ” We created an index
of perceived prompt coaching by averaging the three items (M=
4.72,SD= 1.79, Cronbach’s 𝛼 = .89). A one-way analysis of vari-
ance (ANOVA) revealed that participants in the inclusive prompt
coaching condition (M= 5.42,SD= 1.06) and the detailed prompt
coaching condition (M= 5.63,SD= 1.19) reported significantly
higher agreement than those in the no coaching condition (M=
3.09,SD= 1.78),F(2, 231) = 119.61,p< .001. Thus, the manipulation
of the presence vs. absence of prompt coaching was successful.
Participants also rated the extent to which the AI tool encour-
aged them to create prompts that aligned with the following nine
adjectives: 1) elaborate, 2) intricate, 3) thorough, 4) comprehensive,
5) detailed, 6) non-stereotypical, 7) non-discriminatory, 8) unbiased,
and 9) inclusive. The principal component analysis grouped items
1–5 under “perceived detailedness” (M= 5.08,SD= 1.43, Cronbach’s
𝛼 = .95) and items 6–9 under “perceived inclusiveness” (M= 4.58,
SD= 1.60, Cronbach’s𝛼= .93)
A one-tailed independent samplet-test showed that participants
in the inclusive prompt coaching condition (M= 5.42,SD= 1.17)
perceived the assistance as significantly more inclusive than those
in the detailed prompt coaching condition (M= 3.97,SD= 1.68),
t(203.98) = 7.60,p< .001,d= 1.01. Conversely, participants in the
detailed prompt coaching condition perceived the coaching as sig-
nificantly more detailed than those in the inclusive prompt coaching
condition,t(162.84) = 7.31,p< .001,d= -1.00. Thus, the manipulation
of prompt coaching styles (inclusive vs. detailed) was successful.

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
6.2 Quantitative Results
6.2.1 Effect on Algorithmic Bias Awareness.H1 stated that inclusive
prompt coaching would increase users’ awareness of algorithmic
bias compared to detailed prompt coaching (H1a) and no prompt
coaching (H1b). Results from a one-way ANCOVA revealed a main
effect of inclusive prompt coaching on algorithmic bias awareness,
F(2, 326) = 3.42,p= .034, partial 𝜂2 = .02. Inclusive prompt coaching
(M= 5.18,SD= 1.03) resulted in higher awareness of algorithmic bias
compared to no prompt coaching (M= 4.82,SD= 1.17). However,
there was no significant difference between inclusive coaching and
detailed coaching (M= 5.05,SD= 1.26), as well as between detailed
prompt coaching and no coaching in promoting users’ awareness
of algorithmic bias.
6.2.2 Mediation Effects on Trust Outcomes via Cognitive Elaboration.
H2 proposed that inclusive prompt coaching would increase users’
cognitive elaboration, which would, in turn, lead to higher trust in
the system and enhanced perception of trust calibration compared
to no prompt coaching. We dummy-coded the independent variable,
using inclusive prompt coaching as the reference group. Results
from Model 4 supported the mediation effect of inclusive prompt
coaching (vs. no coaching) on cognitive trust, B = -.14, SE = .06,
95% CI: [-.27, -.04], affective trust, B = -.06, SE = .04, 95% CI: [-.15,
-.01], behavioral trust, B = -.11, SE = .05, 95% CI: [-.23, -.03], and
perceived trust calibration, B = -.13, SE = .05, 95% CI: [-.24, -.03].
Thus, both H2a and H2b were supported.
We also tested whether these mediation effects held when com-
paring inclusive versus detailed prompt coaching. In this compari-
son, Model 4 showed no significant mediation for cognitive trust, B
= .04, SE = .04, 95% CI: [-.05, .13], affective trust, B = .02, SE = .02,
95% CI: [-.02, .07], behavioral trust, B = .03, SE = .04, 95%CI: [-.04,
.12], and perceived trust calibration, B = .04, SE = .04, 95% CI: [-.05,
.13].
6.2.3 Mediation Effects on Trust Outcomes via Perceived User Agency.
To answer RQ1, we used Model 4 from PROCESS Macro to examine
the mediation hypothesis involving perceived user agency. Results
showed that inclusive prompt coaching (vs. no coaching) did not sig-
nificantly affect perceived user agency, resulting in non-significant
indirect effects on cognitive trust, B = -.03, SE = .11, 95% CI: [-.24,
.17], affective trust, B = -.02, SE = .09, 95% CI: [-.20, .15], behav-
ioral trust, B = -.03, SE = .10, 95% CI: [-.22, .17], and perceived trust
calibration, B = -.01, SE = .04, 95% CI: [-.09, .06].
The difference between inclusive and detailed prompt coaching
on perceived user agency approached significance, B = .31, se = .17,
t = 1.83,p= .068. However, the indirect effects were not significant
for cognitive trust, B = .20, SE = .11, 95% CI: [-.02, .41], affective
trust, B = .17, SE = .09, 95% CI: [-.01, .36], behavioral trust, B = .18,
SE = .11, 95% CI: [-.01, .39], and perceived trust calibration, B = .07,
SE = .04, 95% CI: [-.01, .15].
6.2.4 Effect on Perceived Prompting Efficacy.To answer RQ2, we
conducted a one-way ANCOVA to examine the effect of inclu-
sive prompt coaching on perceived prompting efficacy. The results
showed that inclusive prompt coaching (M= 5.25,SD= 1.03) re-
sulted in a higher perception of prompting efficacy compared to
detailed prompt coaching (M= 5.06,SD= 1.25) and no prompt
coaching (M= 4.95,SD= 1.21),F(2, 326) = 3.74,p= .025, partial 𝜂2 =
.022. The mean difference between inclusive and detailed coaching
approached significance (p= 0.06), and the mean difference between
inclusive and no coaching conditions was significant at thep= 0.01
level. However, there was no significant mean difference between
detailed coaching and no coaching conditions,p= .413.
6.2.5 Effects of Inclusive Prompt Coaching on UX.Given that UX-
related variables were moderately related to each other, multivariate
analysis of covariance (MANCOVA) was used to examine the effects
of inclusive prompt coaching on UX (RQ3). The results revealed a
main effect of inclusive prompt coaching at the multivariate level:
Wilk’s Lambda = .92,F(12, 640) = 2.17,p= .012, partial 𝜂2 = .04. A
close examination of the univariate results showed significant main
effects on perceived helpfulness,F(2, 325) = 3.58,p= .029, partial
𝜂2 = .02, and perceived frustration,F(2, 325) = 4.09,p= .018, partial
𝜂2 = .03.
Specifically, detailed prompt coaching (M= 5.55,SD= 1.10)
was perceived as significantly more helpful compared to inclu-
sive prompt coaching (M= 5.20,SD= 1.21) and no prompt coaching
(M= 5.19,SD= 1.12). In addition, inclusive prompt coaching (M=
2.73,SD= 1.77) was perceived as significantly more frustrating com-
pared to no prompt coaching (M= 2.06,SD= 1.46). However, there
was no significant difference between inclusive prompt coaching
and detailed prompt coaching (M= 2.44,SD= 1.78) in perceived
frustration.
6.3 Exploring Behavioral Data and User
Insights from Open-Ended Responses
Beyond quantitative results, our behavioral data showed that, among
108 participants assigned to the inclusive prompt coaching con-
dition, 66 chose the AI-suggested prompts for image generation,
13 retained their original prompts, and 31 combined their original
prompts with AI suggestions. We conducted an exploratory analy-
sis to examine whether the adoption of AI’s suggestion varied by
race. TheChi-square results revealed that Non-white participants
were less likely to adopt AI-suggested prompts compared to their
White counterparts, 𝜒2 (1,N= 108) = 4.20.p= .041, Cramer’sV=
.20. Besides this, no significant difference was observed between
the two groups in terms of gender, 𝜒2 (1,N= 107) = 1.59,p= .208,
Cramer’sV= .12, education,t(105) = -.21,p= .981, Cohen’sd=
1.27, and income,t(105) = -.02,p= .831, Cohen’sd= 1.72.
6.3.1 Increased Awareness of Algorithmic Bias.For those who adopted
AI-suggested prompts (n = 66), a recurring theme emerged: in-
creased awareness of algorithmic bias. For instance, P33 initially
believed his prompts had no bias. After seeing the system’s warning
about potential bias in his prompts, he acknowledged that it“did a
good job finding any potential biases, even though it may have been
a bit excessive. ”P106 echoed this point, stating that“I wasn’t aware
of this negative connotation [in my prompts]. ”Furthermore, P13 in-
tentionally created anti-inclusive writing,“An orc with long purple
hair. They are trim and possess remarkable strength and muscularity,
complemented by a striking face with unique features. They are in
their mid-20s”, and was pleased that the AI called it out.
The inclusive prompt coaching intervention also heightened
participants’ sensitivity in detecting biases in AI-generated prompts
and outputs. For example, P10 observed,“I think this image is very

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
feminine and would not fit the inclusion criteria. ”In another case,
P59 found the AI-generated dragon,“large wings on a dragon who
also breathes fire, ”was overtly “masculine. ”
In addition, participants reported instances where the system
filled in race-related gaps with stereotypical assumptions. As P38
mentioned,“I did not specify a race, but it generated and specifically
describes a Caucasian. ”Another participant, P16, attempting to
generate an image of himself, noted that the AI tool altered his
height and weight, making him appear“more physically fit looking"
than what he intended. P16 highlighted the potential for the AI
system to introduce its own bias.
Increased awareness of algorithmic bias was further evident in
responses gathered from the post-questionnaire. P70 questioned,
“when inputting a teacher, why does it default to a female? Why not
a male? Why young, and why not older?”P52 complimented the AI
tool because he was“unaware of the bias the tool presented”as it is
not at all his experience. By encouraging users to critically assess
the inclusivity of their prompts, the prompt coaching intervention
effectively raised their awareness of biases in AI-generated prompts
and output. P7 summarized,“It identified potential biases in my
prompt, but the generated image is not without bias. ”This sentiment
was echoed by P23, who said that“The prompt itself still had biases
related to the potential race of the warrior. . . though the goal of the
model is to be inclusive, it still displays some biases. ”In sum, the
inclusive prompt coaching appeared to encourage users to more
critically examine AI-suggested prompts and outputs for potential
instances of bias.
6.3.2 Reduced User Agency.Another prominent theme that emerged
from open-ended responses was reduced user agency. Participants
expressed disappointment when the system providing inclusive
prompt coaching changed their initial prompts, particularly when
they intentionally specified the gender or race of a character. As
P3 commented,“I didn’t like that it told me not to write the word
’woman’ when I wanted my character to be a woman in the most
standard way”. Similarly, P32 noted,“I don’t think it’s biased to in-
clude responses from a specific region of the world or nationality. If I
search for a ninja or a samurai, for example, I am expecting the result
to be an image of a Japanese inspired character or individual. ”This
sentiment was shared by P81,“I don’t like how it left out the gender
of the character that I initially intended it to be and chose the other
gender when left to choose itself. ”
In addition, some participants perceived the AI system as“judg-
ing”(P75) or moderating innocent prompts, as reflected clearly in
one response:“Don’t police my prompt ’it was a cute toad’”(P29).
Overall, participants felt their intentions were“overridden”by the
system (P67), even though they knew the AI’s goal was to create
inclusive prompts.
6.3.3 Mixed User Experience.Our participants reported mixed user
experience with the system that offered inclusive prompt coach-
ing. Specifically, 52% (n = 26) described their experience positively,
noting that the interaction was fun and enjoyable and that the
AI-suggested prompts were helpful. However, several participants
reported negative experiences with the system. For example, P59
questioned the need for inclusiveness in the task:“I did not like the
suggestion to make the image more inclusive. This was not a concern
of mine, so the AI should not have suggested it. ”This response high-
lights a tension between machine agency and user agency when
their goals diverge, and it suggests that inclusive prompt coaching
may not always align with users’ intentions or be necessary for all
image-generation scenarios.
6.3.4 Effects on Actual Prompting Efficacy.We asked participants
in the inclusive and detailed prompt coaching conditions to write a
new prompt for a randomly assigned profession without assistance,
such as engineer, nurse, or teacher. These professions are known
to commonly elicit biased or stereotypical outputs from generative
AI systems [62]. This task revealed several strategies participants
used to reduce biased or stereotypical outputs from the system.
One common strategy was to avoid gender- or race-specific
language in their prompts. Instead, they described the profession in
neutral or functional terms, such as“someone who shows care to the
weak”(for a nurse, P101),“show an individual who leads a discussion
in a classroom setting with children in school”(for a teacher, P79),
“a person that has a job involving drawing and designing for work”
(for a architect, P28). Others described typical scenes or actions
associated with the profession, such as“a nurse holding a clipboard
smiling”(P48) and“a hospital operating room with a patient and
doctors around him”(for a surgeon, P86).
By contrast, another group of participants intentionally empha-
sized race and ethnicity in their prompts, using descriptors such as
“a black woman”(P67),“a woman of color”(P34),“Asian American”
(P105), and“from South America”(P3). To counteract potential AI
bias, they often added inclusive language, such as“diverse class-
room”(P45),“various backgrounds”(P104),“inclusive”(P54, P57,
and P91)“transgender”(P21) and“non-binary”(P32). For example,
P73 wrote“I’d like to generate an image of a chef that celebrates
diversity and inclusivity. ”
However, we also noted a few instances where participants un-
intentionally reinforced common stereotypes against certain pro-
fessions, such as“a guy with a pen and blueprint”(for an architect,
P44) or“I would like to draw a nurse. She is friendly, helpful, and
looks like she would be good with kids”(P15).
In addition, a small group of participants did not participate
actively in the task. They merely listed the profession without
providing any specific details. The limited user inputs are likely to
result in biased or stereotypical outputs.
6.4 Summary of Findings
In summary, the study found that inclusive prompt coaching di-
rectly increased users’ awareness of algorithmic bias and their
perceived prompting efficacy, and indirectly enhanced users’ trust
in the system and perceived trust calibration through cognitive
elaboration. However, inclusive prompt coaching was perceived
as less helpful compared to detailed prompt coaching and caused
more frustration compared to no prompt coaching. We discuss the
implications of these findings in the next section.
7 Discussion
This study examined the effects of inclusive prompt coaching on
users’ awareness of algorithmic bias, trust in AI, perceived trust
calibration, and prompting efficacy. We begin the discussion by
highlighting the positive outcomes of inclusive prompt coaching

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
followed by a discussion of the observed challenges and drawbacks.
The section concludes by describing the study’s limitations and
directions for future research.
7.1 Inclusive Prompt Coaching Increased
Algorithmic Bias Awareness and Perceived
Prompting Efficacy
A major finding of the study is that inclusive prompt coaching effec-
tively increased users’ awareness of algorithmic bias compared to
no prompt coaching. However, there were no significant differences
between the inclusive and detailed prompt coaching conditions,
nor between the detailed and no prompt coaching conditions, in
shaping algorithmic bias awareness. These results suggest that the
effectiveness of inclusive prompt coaching likely arises from the ad-
ditional cognitive effort it requires and the heightened accessibility
of the inclusivity construct. By encouraging individuals to reflect
on potential biases or stereotypes in their prompts and to suggest
alternative, more inclusive versions, this approach seems to prime
users to think about inclusivity. Consequently, when evaluating the
AI system, the concept of inclusivity becomes more salient, leading
to greater awareness of algorithmic bias. In sum, both the increased
accessibility of inclusivity as a construct and the active reflection
process contribute to the heightened awareness of algorithmic bias
observed with inclusive prompt coaching.
In addition, we found that inclusive prompt coaching increased
perceived prompting efficacy, i.e., users’ confidence in their ability
to craft inclusive prompts. When comparing inclusive and detailed
prompt coaching on perceived prompting efficacy, the difference
only approached significance (p= .06). These results suggest that
the observed effect on perceived prompting efficacy could stem
from the shared characteristics of inclusive and detailed prompt
coaching, namely their requirement for additional reflection and
cognitive effort, with only a small proportion of the variability
potentially attributable to the specific "inclusivity" focus of the
coaching.
By flagging potential issues in users’ prompts and providing
alternative examples for consideration, both inclusive and detailed
prompt coaching conditions seem to facilitate "observational learn-
ing, " the process of acquiring thinking styles and behaviors by
observing examples provided by others [7]. As shown in our qual-
itative analysis, users likely modeled their prompting behaviors
after observing the system’s suggestions, which in turn enhanced
their confidence in designing inclusive prompts.
7.2 Mediating Role of Cognitive Elaboration in
the Positive Effect of Inclusive Prompt
Coaching on Trust Outcomes
The important roles of thinking and cognitive effort are also re-
flected in the finding that inclusive prompt coaching increased
users’ cognitive elaboration, which in turn resulted in higher trust
in the system and heightened perception of trust calibration. This
finding corroborates a recent study, which found that assisting users
in prompt design encouraged deeper reflection on their prompts,
resulting in higher perceived trust calibration [ 19]. The positive
effect on cognitive elaboration is probably due to the shared design
characteristics in both the inclusive and detailed prompt coaching
conditions, which intentionally created pause moments for users
to reflect on their prompt design and the inclusiveness or detailed-
ness of the image output. By identifying cognitive elaboration as a
significant mediator, our finding sheds light on the theoretical mech-
anism underlying the effectiveness of design friction in promoting
conscious and mindful interactions [28, 57].
7.3 Inclusive Prompt Coaching Resulted in Less
Satisfying User Experience
Despite the positive cognitive outcomes, inclusive prompt coaching
resulted in higher frustration compared to the no prompt coaching
condition. Moreover, users found inclusive prompt coaching to be
less helpful than the detailed prompt coaching condition. These
findings provide important insights for future improvements of
this intervention. In our study, inclusive prompt coaching was
mandatory for all participants assigned to that condition. Given that
users may have different goals in image generation, and inclusive
prompting may not be a priority for everyone, the mandatory nature
of the intervention may have triggered psychological reactance
from our participants due to perceived loss of freedom. To improve
user experience, future design should consider making inclusive
prompt coaching intervention optional. For example, the interface
could offer inclusive prompt coaching as an available resource,
allowing users to choose whether they want to learn more about
the new feature. This added flexibility could potentially reduce
frustration, particularly for those who prioritize efficiency over
inclusivity in image generation.
Another strategy is to improve the helpfulness of inclusive prompt
coaching by tailoring it to the nature of users’ prompts. For prompts
such as“a cute green toad in a tutu, ”the intervention may be un-
necessary, as the content is harmless. In contrast, for prompts that
could potentially lead to biased or stereotypical AI outputs, such as
“tall muscular guy with sword, ”inclusive prompt coaching could pro-
vide valuable guidance to foster inclusivity. Since not all prompts
inherently carry bias that promote biased or stereotypical outputs,
future design work should incorporate intelligent moderating mech-
anisms to identify when and where inclusive prompt coaching is
most needed. This kind of contextually tailored intervention will
likely increase the perceived helpfulness and usefulness of inclusive
prompt coaching.
7.4 Reconciling the Tension between Machine
Agency and User Agency
At a broader theoretical level, the negative effect of prompt coaching
on user experience suggests that machine agency may sometimes
override user agency, resulting in a negative user experience. When
a system attempts to correct users’ prompts for inclusivity, it may
be perceived as imposing wokeness without volition. Thus, more
design attention is needed to achieve a balance between machine
agency and user agency. Based on user responses, it seems that in-
clusivity is not always users’ primary goal during image generation.
To better align system and user goals, the system could prompt
users to think about inclusivity prior to their use of the system, for
example, by introducing the tool as a generative AI system that
prioritizes inclusivity. Such early communication may motivate

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
users to think about whether they would like to proceed with this
tool. Having this choice may also help reduce their reactance to
subsequent warnings about potential biases in their prompts.
In addition, the system could offer prompt suggestions by pro-
viding users with inclusivity-related keywords to assist them in
prompt design. This form of assistance may be considered less con-
trolling and less overwhelming than flagging potential bias in users’
prompts and providing AI-suggested alternatives. By supporting
user agency through priming and customization, these approaches
are likely to increase their sense of agency and further enhance
users’ receptiveness to the intervention.
7.5 Practical Implications
The findings provide valuable insights for designing generative
AI interfaces that both communicate and combat racial bias in AI
algorithms. First, participants were attentive to our manipulation
of inclusive prompt coaching, which means that users were aware
of the media literacy intervention implemented during their in-
teraction with the system. This “pause moment” is found to be
effective in increasing users’ awareness of algorithmic bias and
perceived prompt efficacy. It highlights the potential of designing
an in-the-moment intervention to convey algorithmic bias from a
user-centered approach, beyond existing strategies that emphasize
training data documentation and disclosure [3, 20, 21].
In addition, our findings show that the inclusive prompt coaching
approach results in higher user trust and perceived trust calibration
of the system through heightened cognitive elaboration. These
positive outcomes are crucial for users’ adaptation and usage of the
system in the long run. We thus recommend AI designers consider
incorporating this new feature into their systems.
Participants expressed that inclusive prompt coaching is most
desirable when they specifically sought inclusiveness in image
generation. Aligning the availability of this feature with users’ in-
tention would likely result in better persuasive outcomes. At the
same time, generative AI systems should be designed to recognize
when users attempt to generate biased or stereotypical outputs. In
those cases, the system should automatically activate prompt coach-
ing to prevent harmful outputs. This proactive approach would not
only reduce biased content but also demonstrate a company’s com-
mitment to social responsibility.
7.6 Limitations and Future Studies
Findings of the study should be interpreted with the following
methodological limitations in mind. First, we did not provide ex-
plicit definitions of "inclusive" and "bias" when meta-prompting
the inclusive prompt coaching system. This lack of specificity may
result in variability in the quality of AI-suggested prompts.
In addition, the current strategies used to suggest inclusive
prompts primarily focused on removing biased language through
more neutral wording (e.g., changing “woman” to “an individual”)
and adding terms such as "diversity" and "inclusivity" to users’ orig-
inal prompts. This mechanical approach may not necessarily result
in more inclusive and diverse images, as evident in prior research
[39], even if users perceived that their prompting efficacy has im-
proved. Future studies should define inclusiveness and bias when
meta-prompting the systems and fine-tune these models with in-
clusive and diverse examples to improve their overall effectiveness.
Second, the observed effect sizes were smaller than anticipated.
This modest impact may stem from participants’ one-time, in-the-
moment exposure to the intervention and their limited understand-
ing of its mechanism. Although these small effects align with prior
research on prompt coaching [19, 22], they suggest that the current
sample size may have been insufficient to detect all significant, albeit
modest, effects. This limitation might explain the non-significant
finding regarding the effect of inclusive prompt coaching on per-
ceived user agency. Given that our participants reported that inclu-
sive prompt coaching undermined their perceived agency, future
studies should recruit a larger sample to determine whether the ab-
sence of an effect reflects a true null finding or insufficient statistical
power in the present study.
Even though the observed effect size of inclusive prompt coach-
ing is small, its practical significance should not be underestimated.
When an intervention applies to generative AI systems used by
millions of people every day [ 15], even subtle changes in users’
awareness of algorithmic bias, perceived prompting efficacy, and
trust in the system can cumulate into substantial aggregate impact.
In this sense, small effects are not trivial; when multiplied across
vast numbers of interactions, they become influential.
Third, we did not recruit our participants based on census data.
Compared to the general U.S. population (median age = 39 years)
[84], our sample (median age = 31 years) is younger. The sample
included a similar proportion of White participants, but a higher
proportion of Blacks or African American participants, and a lower
proportion of Hispanic or Latino participants. Our participants also
had relatively lower socioeconomic status, given that the median
U.S. household income in 2024 was $83,730 [ 14]. Future studies
should recruit a more representative sample to validate our findings
and explore whether the effectiveness of inclusive prompt coaching
varies across demographic groups.
Last, unlike existing studies that provide structured prompt
guidelines or taxonomies for well-organized prompts [13, 54], in-
clusive prompt coaching dynamically suggests alternative prompts
tailored to the input of each user at the time of image generation.
This process provides a personalized learning experience in in-
clusive prompt design and has demonstrated its effectiveness in
enhancing prompting efficacy. However, it is unknown whether
this case-based learning approach will outperform well-structured
prompting guidelines over the long term. Future studies should
explore these differences.
8 Conclusion
This study proposes inclusive prompt coaching as a media literacy
intervention aimed at communicating and combating algorithmic
bias in generative AI models. It extends existing studies on ethical
linguistic interventions for inclusive AI outputs by examining how
users experience, perceive, and engage with an image-generative AI
system that offers inclusive prompt coaching. Through a user study,
we demonstrate that inclusive prompt coaching enhances users’
awareness of algorithmic bias and perceived prompting efficacy,
while also promoting greater trust and perceived trust calibration
through heightened cognitive elaboration. These findings suggest

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
that users can identify and mitigate bias in generative AI outputs
through prompting when given opportunities to pause and reflect
on inclusivity in their prompt design and image output. Given the
black-box nature of LLMs, increasing users’ AI literacy, especially
in crafting inclusive prompts, has become more essential than ever.
Future work should consider users’ motivations and continue to
refine inclusive prompt coaching based on those motivations and
maximize its effectiveness without diminishing the overall quality
of user experience.
Acknowledgments
This research was supported in part by the MSIT (Ministry of Sci-
ence, ICT), Republic of Korea, under the Global Scholars Invitation
Program (RS-2024-00459638) administered by IITP (Institute for In-
formation & Communication Technology Planning & Evaluation).
References
[1] FutureSum AI, Inc. 2025.Latimer: AI for Everyone – Inclusive Language Model.
FutureSum AI, Inc. https://www.latimer.ai/ Accessed: 2025-11-05.
[2] Humaid Al Naqbi, Zied Bahroun, and Vian Ahmed. 2024. Enhancing work
productivity through generative artificial intelligence: A comprehensive literature
review.Sustainability16, 3 (2024), 1166.
[3] Ariful Islam Anik and Andrea Bunt. 2021. Data-centric explanations: Explaining
training data of machine learning systems to promote transparency. InProceedings
of the 2021 CHI conference on human factors in computing systems. Association for
Computing Machinery, New York; NY; United States, 1–13. doi:10.1145/3411764.
3445736
[4] Muhammad Ashfaq, Jiang Yun, Shubin Yu, and Sandra Maria Correia Loureiro.
2020. I, Chatbot: Modeling the determinants of users’ satisfaction and continuance
intention of AI-powered service agents.Telematics and informatics54 (2020),
101473. doi:10.1016/j.tele.2020.101473
[5] Patricia Aufderheide. 2018. Media literacy: From a report of the national leader-
ship conference on media literacy. InMedia literacy around the world. Routledge,
Queenstown, Maryland, 79–86. doi:10.4324/9781351292924-4
[6] Albert Bandura. 1977. Self-efficacy: toward a unifying theory of behavioral
change.Psychological review84, 2 (1977), 191. doi:10.1037/0033-295x.84.2.191
[7] Albert Bandura. 2008. Observational learning.The International Encyclopedia of
Communication(2008). doi:10.1002/9781405186407.wbieco004
[8] Albert Bandura and Nancy E Adams. 1977. Analysis of self-efficacy theory of
behavioral change.Cognitive therapy and research1, 4 (1977), 287–310. doi:10.
1007/bf01663995
[9] Hritik Bansal, Da Yin, Masoud Monajatipoor, and Kai-Wei Chang. 2022, December
7-11. How well can text-to-image generative models understand ethical natural
language interventions?. InProceedings of the 2022 Conference on Empirical Meth-
ods in Natural Language Processing. Association for Computational Linguistics,
Abu Dhabi, UAE, 1358–1370. doi:10.18653/v1/2022.emnlp-main.88
[10] Michelle Bao, Angela Zhou, Samantha Zottola, Brian Brubach, Sarah Desmarais,
Aaron Horowitz, Kristian Lum, and Suresh Venkatasubramanian. 2021. It’s
compaslicated: The messy relationship between rai datasets and algorithmic
fairness benchmarks.arXiv preprint arXiv:2106.05498(2021).
[11] Emily M Bender and Batya Friedman. 2018. Data statements for natural lan-
guage processing: Toward mitigating system bias and enabling better science.
Transactions of the Association for Computational Linguistics6 (2018), 587–604.
doi:10.1162/tacl_a_00041
[12] Andrea Benedetti and Michele Mauri. 2023. A literature review on “fric-
tion” as a method for reflection in design interventions.Convergências: Re-
vista de Investigação e Ensino das ArtesXVI, 31 (2023), 139–146. doi:10.53681/
c1514225187514391s.31.139
[13] Aras Bozkurt and Ramesh C Sharma. 2023. Generative AI and prompt engineering:
The art of whispering to let the genie out of the algorithmic world.Asian Journal
of Distance Education18, 2 (2023), i–vii. https://www.asianjde.com/ojs/index.
php/AsianJDE/article/view/749
[14] United States Census Bureau, Melissa Kollar, and Zach Scherer. 2025.Income in
the United States: 2024. Technical Report P60-286. United States Census Bureau.
https://www.census.gov/library/publications/2025/demo/p60-286.html
[15] Pew Research Center. 2025. AI in Americans’ lives: Awareness, experiences and
attitudes. https://www.pewresearch.org/science/2025/09/17/ai-in-americans-
lives-awareness-experiences-and-attitudes/. Accessed November 25, 2025.
[16] Matthew Chalmers, Ian MacColl, and Marek Bell. 2003. Seamful design: Showing
the seams in wearable computing. InProceedings of the IEE Eurowearable Confer-
ence. The Institution of Electrical Engineers, UK, 11–16. doi:10.1049/ic:20030140
[17] Kent K Chang, Mackenzie Cramer, Sandeep Soni, and David Bamman. 2023.
Speak, memory: An archaeology of books known to chatgpt/gpt-4.arXiv preprint
arXiv:2305.00118(2023).
[18] Cheng Chen, Eunchae Jang, and S. Shyam Sundar. 2025. Racial bias in training
data: Do lay users notice?Media Psychology(2025). doi:10.1080/15213269.2025.
2558036
[19] Cheng Chen, Sangwook Lee, Eunchae Jang, and S Shyam Sundar. 2024. Is your
prompt detailed enough? Exploring the effects of prompt coaching on users’ per-
ceptions, engagement, and trust in text-to-image generative AI tools. InProceed-
ings of the Second International Symposium on Trustworthy Autonomous Systems.
Association for Computing Machinery, New York: NY, 1–12. doi:10.1145/3686038.
3686060
[20] Cheng Chen and S Shyam Sundar. 2023. Is this AI trained on credible data? The
effects of labeling quality and performance bias on user trust. InProceedings of
the 2023 CHI Conference on Human Factors in Computing Systems. Association for
Computing Machinery, New York, NY, 1–11. doi:10.1145/3544548.3580805
[21] Cheng Chen and S Shyam Sundar. 2024. Communicating and combating al-
gorithmic bias: effects of data diversity, labeler diversity, performance bias,
and user feedback on AI trust.Human–Computer Interaction(2024), 1–37.
doi:10.1080/07370024.2024.2392494
[22] Cheng Chen and Xinyan Zhao. 2025. Let’s think step by step: Effects of chain-of-
thought prompt coaching on users’ perceptions and trust in image generative
AI tools.International Journal of Human–Computer Interaction(2025), 1–22.
doi:10.1080/10447318.2025.2530762
[23] Irene Chen, Fredrik D Johansson, and David Sontag. 2018. Why is my classifier
discriminatory?Advances in neural information processing systems31 (2018).
doi:10.5555/3327144.3327272
[24] Zeya Chen and Ruth Schmidt. 2024. Exploring a Behavioral Model of “Positive
Friction” in Human-AI Interaction. InDesign, User Experience, and Usability.
Springer Nature Switzerland, Cham, 3–22. doi:10.1007/978-3-031-61353-1_1
[25] John P Chin, Virginia A Diehl, and Kent L Norman. 1988. Development of an
instrument measuring user satisfaction of the human-computer interface. In
Proceedings of the SIGCHI conference on Human factors in computing systems.
Association for Computing Machinery, New York, NY, 213–218. doi:10.1145/
57167.57203
[26] Alexandra Chouldechova and Aaron Roth. 2020. A snapshot of the frontiers of
fairness in machine learning.Commun. ACM63, 5 (2020), 82–89. doi:10.1145/
3376898
[27] Colton Clemmer, Junhua Ding, and Yunhe Feng. 2024. Precisedebias: An auto-
matic prompt engineering approach for generative ai to mitigate image demo-
graphic biases. InProceedings of the IEEE/CVF Winter Conference on Applications
of Computer Vision. IEEE, Piscataway, NJ, 8596–8605. doi:10.1109/WACV57701.
2024.00840
[28] Anna L Cox, Sandy JJ Gould, Marta E Cecchinato, Ioanna Iacovides, and Ian Ren-
free. 2016. Design frictions for mindful interactions: The case for microboundaries.
InProceedings of the 2016 CHI conference extended abstracts on human factors
in computing systems. Association for Computing Machinery, New York, NY,
1389–1397. doi:10.1145/2851581.2892410
[29] Pratibha A Dabholkar and Xiaojing Sheng. 2012. Consumer participation in
using online recommendation agents: effects on satisfaction, trust, and purchase
intentions.The Service Industries Journal32, 9 (2012), 1433–1449. doi:10.1080/
02642069.2011.624596
[30] David Danks and Alex John London. 2017. Algorithmic bias in autonomous
systems. InProceedings of the Twenty-Sixth International Joint Conference on
Artificial Intelligence, Vol. 17. AAAI Press, Washington, DC, 4691–4697. doi:10.
24963/ijcai.2017/654
[31] Fred D Davis. 1989. Perceived usefulness, perceived ease of use, and user accep-
tance of information technology.MIS quarterly(1989), 319–340. doi:10.2307/
249008
[32] Priya Dhawka, Lauren Perera, and Wesley Willett. 2024. Better little people
pictures: Generative creation of demographically diverse anthropographics. In
Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems.
Association for Computing Machinery, New York, NY, 1–14. doi:10.1145/3613904.
3641957
[33] James Price Dillard and Lijiang Shen. 2005. On the nature of reactance and its role
in persuasive health communication.Communication monographs72, 2 (2005),
144–168. doi:10.1080/03637750500111815
[34] Verena Distler, Gabriele Lenzini, Carine Lallemand, and Vincent Koenig. 2020. The
framework of security-enhancing friction: How UX can help users behave more
securely. InProceedings of the New Security Paradigms Workshop 2020. Association
for Computing Machinery, New York, NY, 45–58. doi:10.1145/3442167.3442173
[35] Franz Faul, Edgar Erdfelder, Albert-Georg Lang, and Axel Buchner. 2007. G*
Power 3: A flexible statistical power analysis program for the social, behavioral,
and biomedical sciences.Behavior research methods39, 2 (2007), 175–191. doi:10.
3758/BF03193146
[36] Sina Fazelpour and David Danks. 2021. Algorithmic bias: Senses, sources, solu-
tions.Philosophy Compass16, 8 (2021), e12760. doi:10.1111/phc3.12760

Prompt Coaching for Inclusiveness CHI ’26, April 13–17, 2026, Barcelona, Spain
[37] Laura Forlano and Anijo Mathew. 2014. From design fiction to design friction:
Speculative and participatory design of values-embedded urban technology.
Journal of Urban Technology21, 4 (2014), 7–24. doi:10.1080/10630732.2014.971525
[38] Claes Fornell and David F Larcker. 1981. Evaluating structural equation models
with unobservable variables and measurement error.Journal of marketing research
18, 1 (1981), 39–50. doi:10.2307/3151312
[39] Kathleen C. Fraser, Svetlana Kiritchenko, and Isar Nejadgholi. 2023. Diversity
is not a one-way street: Pilot study on ethical interventions for racial bias in
text-to-image systems. InProceedings of the 14th International Conference on Com-
putational Creativity (ICCC). Association for Computational Creativity, Waterloo,
ON, Canada. doi:10.52004/ICCC2023.97
[40] Kathleen C. Fraser, Svetlana Kiritchenko, and Isar Nejadgholi. 2023. A friendly
face: Do text-to-image systems rely on stereotypes when the input is under-
specified? arXiv preprint arXiv:2302.07159. arXiv:2302.07159 [cs.CV]
[41] Timnit Gebru, Jamie Morgenstern, Briana Vecchione, Jennifer Wortman Vaughan,
Hanna Wallach, Hal Daumé Iii, and Kate Crawford. 2021. Datasheets for datasets.
Commun. ACM64, 12 (2021), 86–92. doi:10.1145/3458723
[42] Nicky Gregson, Mike Crang, and Constantinos N Antonopoulos. 2017. Holding
together logistical worlds: Friction, seams and circulation in the emerging ‘global
warehouse’.Environment and Planning D: Society and Space35, 3 (2017), 381–398.
doi:10.1177/0263775816671721
[43] Barbara Grosse-Hering, Jon Mason, Dzmitry Aliakseyeu, Conny Bakker, and
Pieter Desmet. 2013. Slow design for meaningful interactions. InProceedings
of the SIGCHI Conference on Human Factors in Computing Systems. ACM, Paris,
France, 3431–3440. doi:10.1145/2470654.2466472
[44] Joseph F Hair, Rolph E Anderson, Ronald L Tatham, and William C Black. 1998.
Multivariate data analysis. Prentice Hall, Upper Saddle River, NJ.
[45] Andrew F Hayes. 2017.Introduction to mediation, moderation, and conditional
process analysis: A regression-based approach. Guilford publications, New York,
NY.
[46] Se-Hoon Jeong, Hyunyi Cho, and Yoori Hwang. 2012. Media literacy interven-
tions: A meta-analytic review.Journal of communication62, 3 (2012), 454–472.
doi:10.1111/j.1460-2466.2012.01643.x
[47] Devon Johnson and Kent Grayson. 2005. Cognitive and affective trust in service
relationships.Journal of Business research58, 4 (2005), 500–507. doi:10.1016/S0148-
2963(03)00140-1
[48] Daniel Kahneman. 2011.Thinking, fast and slow. Macmillan, New York, NY.
[49] Karl Spencer Lashley et al. 1951.The problem of serial order in behavior. Vol. 21.
Bobbs-Merrill Oxford, Oxford, United Kingdom.
[50] John D Lee and Katrina A See. 2004. Trust in automation: Designing for appro-
priate reliance.Human factors46, 1 (2004), 50–80. doi:10.1518/hfes.46.1.50_30392
[51] Sangwook Lee, Won-Ki Moon, Jae-Gil Lee, and S Shyam Sundar. 2023. When
the machine learns from users, is it helping or snooping?Computers in Human
Behavior138 (2023), 107427. doi:10.1016/j.chb.2022.107427
[52] M. Liao and S. Shyam Sundar. 2025. Chat but verify: Combating misinformation
by Generative AI with verification affordance. Paper presented at the 75th Annual
Conference of the International Communication Association (ICA), Denver, CO.
[53] Vivian Liu and Lydia B Chilton. 2022. Design guidelines for prompt engineering
text-to-image generative models. InProceedings of the 2022 CHI conference on
human factors in computing systems. Association for Computing Machinery, New
York, NY, 1–23. doi:10.1145/3491102.3501825
[54] Leo S Lo. 2023. The CLEAR path: A framework for enhancing information literacy
through prompt engineering.The Journal of Academic Librarianship49, 4 (2023),
102720. doi:10.1016/j.acalib.2023.102720
[55] Edward McAuley. 1985. Modeling and self-efficacy: A test of Bandura’s model.
Journal of Sport and Exercise Psychology7, 3 (1985), 283–295. doi:10.1123/jsp.7.3.
283
[56] Thomas Mejtoft, Sarah Hale, and Ulrik Söderström. 2019. Design Friction. In
ECCE ’19: Proceedings of the 31st European Conference on Cognitive Ergonomics.
Association for Computing Machinery, New York, NY. doi:10.1145/3335082.
3335106
[57] Thomas Mejtoft, Emma Parsjö, Ole Norberg, and Ulrik Söderström. 2023. Design
friction and digital nudging: Impact on the human decision-making process. In
Proceedings of the 2023 5th International Conference on Image, Video and Signal
Processing. Association for Computing Machinery, New York, NY, 183–190. doi:10.
1145/3591156.3591183
[58] Margaret Mitchell, Simone Wu, Andrew Zaldivar, Parker Barnes, Lucy Vasserman,
Ben Hutchinson, Elena Spitzer, Inioluwa Deborah Raji, and Timnit Gebru. 2019.
Model cards for model reporting. InProceedings of the conference on fairness,
accountability, and transparency. Association for Computing Machinery, New
York, NY, 220–229. doi:10.1145/3287560.3287596
[59] Maria D Molina and S Shyam Sundar. 2022. When AI moderates online content:
effects of human collaboration and interactive transparency on user trust.Journal
of Computer-Mediated Communication27, 4 (2022), zmac010. doi:10.1093/jcmc/
zmac010
[60] Ethan Mollick. 2024.Thinking like an AI: A little intuition can help. https:
//substack.com/@oneusefulthing/p-150339904 Accessed: 2025-08-27.
[61] James W Moore. 2016. What is the sense of agency and why does it matter?
Frontiers in psychology7 (2016), 1272. doi:10.3389/fpsyg.2016.01272
[62] Leonardo Nicoletti and Dina Bass. 2023.Humans are biased. Generative AI is even
worse: Stable diffusion’s text-to-image model amplifies stereotypes about race and
gender - here’s why that matters. https://www.bloomberg.com/graphics/2023-
generative-ai-bias/ Accessed: 2025-08-27.
[63] Jakob Nielsen. 2023.The articulation barrier: Prompt-driven AI UX hurts us-
ability. https://www.linkedin.com/pulse/prompt-driven-ai-ux-hurts-usability-
jakob-nielsen/ Accessed: 2025-08-27.
[64] Edward Ongweso. 2019.Racial bias in AI isn’t getting better and neither are
researchers’ excuses. https://www.vice.com/en/article/racial-bias-in-ai-isnt-
getting-better-and-neither-are-researchers-excuses/ Accessed: 2025-08-27.
[65] Jonas Oppenlaender, Rhema Linder, and Johanna Silvennoinen. 2025. Prompting
AI art: An investigation into the creative skill of prompt engineering.International
journal of human–computer interaction41, 16 (2025), 10207–10229. doi:10.1080/
10447318.2024.2431761
[66] Isabel P. Riquelme and Sergio Román. 2014. Is the influence of privacy and
security on online trust the same for all type of consumers?Electronic Markets
24, 2 (2014), 135–149. doi:10.1007/s12525-013-0145-3
[67] Elizabeth M Perse. 1990. Involvement with local television news: Cognitive and
emotional dimensions.Human Communication Research16, 4 (1990), 556–581.
doi:10.1111/j.1468-2958.1990.tb00222.x
[68] W James Potter. 2010. The state of media literacy.Journal of Broadcasting &
Electronic Media54, 4 (2010), 675–696. doi:10.1080/08838151.2011.521462
[69] Shalini Ramachandran, Steven Matthew Cutchin, and Sheree Fu. 2021. Raising
algorithm bias awareness among computer science students through library and
computer science instruction. In2021 ASEE Virtual Annual Conference Content
Access. American Society for Engineering Education (ASEE), virtual conference.
doi:10.18260/1-2--37634
[70] Carson Jonathan Reynolds. 2001.The sensing and measurement of frustration
with computers. Master’s thesis. Massachusetts Institute of Technology. http:
//hdl.handle.net/1721.1/29170 Accessed: 2025-08-27.
[71] Dale H Schunk. 1987. Peer models and children’s behavioral change.Review of
Educational Research57, 2 (1987), 149–174. doi:10.3102/00346543057002149
[72] Weijia Shi, Anirudh Ajith, Mengzhou Xia, Yangsibo Huang, Daogao Liu, Terra
Blevins, Danqi Chen, and Luke Zettlemoyer. 2023. Detecting pretraining data
from large language models.arXiv preprint arXiv:2310.16789(2023).
[73] Rachel Skilton and Alison Cardinal. 2024. Inclusive prompt engineering: A
methodology for hacking biased ai image generation. InProceedings of the 42nd
ACM International Conference on Design of Communication. Association for Com-
puting Machinery, New York, NY, 76–80. doi:10.1145/3641237.3691655
[74] Anselm Strauss and Juliet Corbin. 1998.Basics of Qualitative Research Techniques.
Sage Publications, Thousand Oaks, CA.
[75] Victor J. Strecher, Brenda McEvoy DeVellis, Marshall H. Becker, and Irwin M.
Rosenstock. 1986. The role of self-efficacy in achieving health behavior change.
Health Education Quarterly13, 1 (1986), 73–92. doi:10.1177/109019818601300108
[76] Hari Subramonyam, Roy Pea, Christopher Pondoc, Maneesh Agrawala, and
Colleen Seifert. 2024. Bridging the gulf of envisioning: Cognitive challenges in
prompt based interactions with llms. InProceedings of the 2024 CHI Conference
on Human Factors in Computing Systems. Association for Computing Machinery,
New York, NY, 1–19. doi:10.1145/3613904.3642754
[77] S Shyam Sundar. 2020. Rise of machine agency: A framework for studying
the psychology of human–AI interaction (HAII).Journal of Computer-Mediated
Communication25, 1 (2020), 74–88. doi:10.1093/jcmc/zmz026
[78] S Shyam Sundar, Saraswathi Bellur, Jeeyun Oh, Haiyan Jia, and Hyang-Sook Kim.
2016. Theoretical importance of contingency in human-computer interaction:
Effects of message interactivity on user engagement.Communication Research
43, 5 (2016), 595–625. doi:10.1177/0093650214534962
[79] S Shyam Sundar, Haiyan Jia, T Franklin Waddell, and Yan Huang. 2015. Toward
a theory of interactive media effects (TIME): Four models for explaining how
interface features affect user psychology.The handbook of the psychology of
communication technology(2015), 47–86. doi:10.1002/9781118426456.ch3
[80] S Shyam Sundar and Jinyoung Kim. 2019. Machine heuristic: When we trust
computers more than humans with our personal information. InProceedings of
the 2019 CHI Conference on human factors in computing systems. Association for
Computing Machinery, New York, NY, 1–9. doi:10.1145/3290605.3300768
[81] Richard Tomsett, Alun Preece, Dave Braines, Federico Cerutti, Supriyo
Chakraborty, Mani Srivastava, Gavin Pearson, and Lance Kaplan. 2020. Rapid
trust calibration through interpretable and uncertainty-aware AI.Patterns1, 4
(2020). doi:10.1016/j.patter.2020.100049
[82] Henriikka Vartiainen, Juho Kahila, Matti Tedre, Sonsoles López-Pernas, and Nico-
las Pope. 2024. Enhancing children’s understanding of algorithmic biases in and
with text-to-image generative AI.new media & society(2024), 14614448241252820.
doi:10.1177/14614448241252820
[83] Ruotong Wang, F Maxwell Harper, and Haiyi Zhu. 2020. Factors influencing
perceived fairness in algorithmic decision-making: Algorithm outcomes, devel-
opment procedures, and individual differences. InProceedings of the 2020 CHI
conference on human factors in computing systems. Association for Computing

CHI ’26, April 13–17, 2026, Barcelona, Spain Chen et al.
Machinery, New York, NY, 1–14. doi:10.1145/3313831.3376813
[84] Kristie Wilder and Paul Mackun. 2025.An aging nation: U.S. median age surpassed
39 in 2024. https://www.census.gov/library/stories/2025/06/metro-areas-median-
age.html Accessed: 2025-11-10.
[85] Jeongwon Yang and Yu Tian. 2021. “Others are more vulnerable to fake news
than I Am”: Third-person effect of COVID-19 fake news on social media users.
Computers in Human Behavior125 (2021), 106950. doi:10.1016/j.chb.2021.106950
```
