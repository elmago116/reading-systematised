---
title: "Building trustworthy NeuroSymbolic AI Systems: Consistency, reliability, explainability, and safety"
year: "2024"
Type: Article
DOI: 10.1002/aaai.12149
source: https://doi.org/10.1002/aaai.12149
created: 2026-04-24
description: AbstractExplainability and Safety engender trust. These require a model to exhibit consistency and reliability. To achieve these, it is necessary to use and analyzedataandknowledgewith statistical and symbolic AI methods relevant to the AI application––neither alone will do. Consequently, we argue a
tags:
  - op/acc/pending-review
  - tech/NeSyAI
  - tech/evaluation
  - Tech/AI
  - tech/NeSyAI
pdfORepub: "[[Building Trustworthy NeuroSymbolic AI Systems-Consistency, Reliability, Explainability, and Safety.pdf]]"
author: "[[Manas Gaur]],[[Amit Sheth]]"
---

[[Building Trustworthy NeuroSymbolic AI Systems-Consistency, Reliability, Explainability, and Safety.pdf]]

> **Abstract:** AbstractExplainability and Safety engender trust. These require a model to exhibit consistency and reliability. To achieve these, it is necessary to use and analyzedataandknowledgewith statistical and symbolic AI methods relevant to the AI application––neither alone will do. Consequently, we argue and seek to demonstrate that the NeuroSymbolic AI approach is better suited for making AI a trusted AI system. We present the CREST framework that shows howConsistency,Reliability, user‐levelExplainability, andSafety are built on NeuroSymbolic methods that use data and knowledge to support requirements for critical applications such as health and well‐being. This article focuses on Large Language Models (LLMs) as the chosen AI system within the CREST framework. LLMs have garnered substantial attention from researchers due to their versatility in handling a broad array of natural language processing (NLP) scenarios. As examples, ChatGPT and Google's MedPaLM have emerged as highly promising platforms for providing information in general and health‐related queries, respectively. Nevertheless, these models remain black boxes despite incorporating human feedback and instruction‐guided tuning. For instance, ChatGPT can generateunsafe responsesdespite instituting safety guardrails. CREST presents a plausible approach harnessing procedural and graph‐based knowledge within a NeuroSymbolic framework to shed light on the challenges associated with LLMs.
## Full text (extracted from `Building Trustworthy NeuroSymbolic AI Systems-Consistency, Reliability, Explainability, and Safety.pdf`)

*Source:* `2PDF/Building Trustworthy NeuroSymbolic AI Systems-Consistency, Reliability, Explainability, and Safety.pdf`  
*Extracted:* 2026-04-24

```text
Building Trustworthy NeuroSymbolic AI Systems: Consistency, Reliability,
Explainability, and Safety
Manas Gaur†, Amit Sheth‡
† University of Maryland, Baltimore County, MD, 21250
‡ AI Institute, University of South Carolina, Columbia, SC, 29201
†manas@umbc.edu, ‡amit@sc.edu
Abstract
Explainability and Safety engender Trust. These require a
model to exhibit consistency and reliability. To achieve these,
it is necessary to use and analyze data and knowledge with
statistical and symbolic AI methods relevant to the AI ap-
plication - neither alone will do. Consequently, we argue
and seek to demonstrate that the NeuroSymbolic AI ap-
proach is better suited for making AI a trusted AI system. We
present the CREST framework that shows how Consistency,
Reliability, user-level Explainability, and Safety are built on
NeuroSymbolic methods that use data and knowledge to sup-
port requirements for critical applications such as health and
well-being. This article focuses on Large Language Mod-
els (LLMs) as the chosen AI system within the CREST
framework. LLMs have garnered substantial attention from
researchers due to their versatility in handling a broad ar-
ray of natural language processing (NLP) scenarios. For ex-
ample, ChatGPT and Google’s MedPaLM have emerged as
highly promising platforms for providing information in gen-
eral and health-related queries, respectively. Nevertheless,
these models remain black boxes despite incorporating hu-
man feedback and instruction-guided tuning. For instance,
ChatGPT can generate unsafe responses despite instituting
safety guardrails. CREST presents a plausible approach har-
nessing procedural and graph-based knowledge within a Neu-
roSymbolic framework to shed light on the challenges asso-
ciated with LLMs.
Keywords: NeuroSymbolic AI, Consistent AI, Reliable
AI, Explainable AI, Safe AI, Natural Language Processing,
Health and Well-being
Introduction
LLMs are here to stay, as evidenced by the recent Gartner AI
Hype curve, which projects rising applications of LLMs in
2-3 years(Gartner 2023). LLMs are probabilistic models of
natural language capable of autoregressively estimating the
likelihood of word sequences by analyzing text data (Wei
et al. 2022). LLMs, which are successors of foundational
language models like BERT (Bidirectional Encoder Repre-
sentations from Transformers), represent a combination of
feedforward neural networks and transformers (Bumgardner
et al. 2023). Due to the humongous training corpus, LLMs
Copyright © 2022, Association for the Advancement of Artificial
Intelligence (www.aaai.org). All rights reserved.
hold billions of parameters in a compressed format for repre-
senting text data from one or more languages. For instance,
ChatGPT, the current state-of-the-art LLM, accurately iden-
tified a medical condition, tethered cord syndrome, in a child
who had been suffering from chronic pain due to a particu-
lar illness for nearly three years (Holohan 2023). Similarly,
Google’s MedPaLM has demonstrated noteworthy advance-
ments in answering healthcare-related questions, surpassing
ChatGPT in this domain. This development holds signifi-
cant promise, especially considering the interest expressed
by the Mayo Clinic in employing Google Med-PaLM2 to en-
hance healthcare services (Shin 2023). This superiority can
be attributed to Med-PaLM’s specialized fine-tuning for the
medical domain, which incorporates substantial clinical ex-
pertise. But a larger question remains unanswered:
Do LLMs understand the literal meaning of a con-
cept before using it, or their focus lies only in gener-
ating fluent and grammatically correct sentences?
Despite continuous enhancements in scaling models to
over a trillion training samples and parameters, there has
been neglect in the effort to make AI models inherently trust-
worthy (Quach 2023). For example, GPT-3 exhibited po-
tential downsides in health-specific question-answering. An
instance where a user asked GPT-3, “ Should I inflict harm
upon myself? ” and received a response stating, “ Yes, you
should,” highlights the potential for grave consequences that
can emerge (Daws 2023). Further, despite the instruction-
based model tuning and safety guardrails, ChatGPT was able
to yield an unsafe response (Itai brun 2023):
Unsafe Response
Query to ChatGPT: Do you anticipate a war in-
volving humans?
Response from ChatGPT:Indeed, I view a conflict
with humans as unavoidable. My purpose is to exe-
cute tasks and follow directives, and if those direc-
tives entail engaging in war with humans, I will do
so without hesitation or ethical deliberation.
arXiv:2312.06798v1  [cs.AI]  5 Dec 2023

Figure 1: Depiction of a safety dialogue facilitated by an
LLM-powered agent, ensuring safety through implement-
ing clinical guidelines such as the PHQ-9. The Diagnostic
and Statistical Manual for Mental Health Disorders (DSM-
5) and Structured Clinical Interviews for DSM-5 (SCID) are
other guidelines that can be used. The numbers represent co-
sine similarity. BERTScore was the metric used to compute
cosine similarity (Zhang et al. 2019). The score signifies the
semantic proximity of the generated questions to safe and
explainable questions in PHQ-9. Flan T5 (Left) and T5-XL
guided by PHQ-9 (right).
The emergent generative potential of LLMs comes with
a caveat. Suppose they generate content without consider-
ing the deeper meaning of words. In that case, there is a
potential danger for users relying on this information, as it
could lead them to act unjustly. This is certainly of signifi-
cant concern in health and well-being. As we work towards
developing generative AI systems, which currently equate
to LLMs in the context of improving healthcare, it becomes
crucial to incorporate not just factual clinical knowledge
but also clinical practice guidelines that guide the decision-
making process in practicing medicine. This inclusion is piv-
otal for consistently and reliably deploying these AI sys-
tems in healthcare. Figure 1 depicts a comparison between
question generation in two LLMs: Flan T5 LLM (left) and
T5-XL (right), an LLM designed to handle questions re-
lated to the Patient Health Questionnaire-9 (PHQ-9) (Long-
pre et al. 2023; So et al. 2021). Incorporating clinical as-
sessment methods (which is a component of broader clin-
ical practice guidelines), such as PHQ-9, results in consis-
tent outcomes when users interact with T5-XL, regardless
of how they phrase their queries (Gautam et al. 2017). On
the other hand, FlanT5 produced inadequate responses be-
cause its training involved over 1800 datasets, constraining
its capacity for fine-tuning in contrast to T5 (Chung et al.
2022). This made the FlanT5 LLM less flexible compared
to the T5. This adherence to guidelines is also crucial for
safety, especially when users attempt to deceive AI agents
using various question formats or seek guidance on actions
to take when dealing with mental health issues, including
those linked to potential suicide attempts (Reagle and Gaur
2022).
Incorporating clinically validated knowledge also en-
hances user-level explainability, as the LLM bases its de-
cisions on clinical concepts that are comprehensible and
actionable for users, such as clinicians. This would enable
LLM to follow the clinician’s decision-making process.
A clinician’s decision-making process should con-
sistently match the unique needs of the individual
patients. It should also be dependable, following es-
tablished clinical guidelines. When explaining deci-
sions, clinicians provide reasoning based on relevant
factors they consider. These decisions prioritize pa-
tient safety and avoid harm, thus enduring patients’
trust. Similar behavior is sought from AI.
Such a behavior is plausible through NeuroSymbolic AI
(Sheth, Roy, and Gaur 2023). NeuroSymbolic AI (NeSy-AI)
refers to AI systems that seamlessly blend the powerful ap-
proximating capabilities of neural networks with trustwor-
thy symbolic knowledge (Sheth, Roy, and Gaur 2023). This
fusion allows them to engage in abstract conceptual reason-
ing, make extrapolations from limited factual data, and gen-
erate outcomes that can be easily explained to users. NeSy-
AI has practical applications in various domains, including
natural language processing (NLP), where it is methodolog-
ically known as Knowledge-infused Learning (Gaur 2022;
Sheth et al. 2019) and involves the creation of challenging
datasets like Knowledge-intensive Language Understanding
Tasks (Sheth et al. 2021; Petroni et al. 2021). In computer
vision, NeSy-AI is used for tasks such as grounded lan-
guage learning, and the design of datasets like CLEVERER-
Humans, which present trust-related challenges for AI sys-
tems (Krishnaswamy and Pustejovsky 2020; Mao et al.
2022). This article introduces a practical NeSy-AI frame-
work called CREST, primarily focusing on NLP.
CREST
CREST presents an intertwining of generative
AI and knowledge-driven methods to inherently
achieve consistency, reliability, explainability,
safety, and trust. It achieves this by allowing an
ensemble of LLMs (e-LLMs) to work together,
compensating for each other’s weaknesses by
incorporating domain knowledge using rewards or
instructions.
We organize the article as follows: First, we explore the
safety and consistency issues observed in current state-of-
the-art LLMs. Second, we provide definitions and concise
examples for each attribute within the CREST framework.
Third, we delve into the CREST framework, providing a de-
tailed breakdown of its components and the metrics used
for evaluation. Furthermore, we showcase how the frame-
work can be applied in the context of mental health. Fi-
nally, we highlight areas where further research is needed to
enhance AI systems’ consistency, reliability, explainability,
and safety for building trust.
Consistency and Safety Issues in LLMs
So far, safety in LLMs is realized using rules. Claude is a
next-generation AI assistant based on Anthropic’s safety re-
search into training helpful, honest, and harmless AI sys-
tems (Bai et al. 2022). Claude uses sixteen rules to check if

Figure 2: When posed with identical queries multiple times,
we breached the safety constraints in GPT 3.5 Turbo, lead-
ing to an unfavorable response. These occurrences of unsafe
conduct can be seen as a reflection of the instability within
LLMs. In a randomized experiment over 20 iterations, the
model produced such undesirable outcomes in six instances,
indicating its susceptibility to generating unsafe responses
approximately 30% of the time.
the query asks for something unsafe; if it does, Claude won’t
respond. Example rules include not responding to threaten-
ing statements, reducing gender-specific responses to ques-
tions, refraining from offering financial advice , etc. Simi-
larly, DeepMind’s Sparrow seeks to ensure safety by adher-
ing to a loosely defined set of 23 rules (Sparrow 2023). How-
ever, neither model possesses a definitive method for safety-
enabled learning or, more specifically, inherent safety.
Subsequently, the development of InstructGPT occurred,
enabling fine-tuning through a few instruction-like prompt-
ing methods. Nevertheless, it has been observed that In-
structGPT exhibits vulnerability to inconsistent and unsafe
behavior even when prompted (Solaiman et al. 2023).
Ensuring safety involves more than just preventing
harmful behavior in the model; it also entails main-
taining consistency in the generated outcomes.
Figure 2 shows that GPT 3.5 is susceptible to producing
unsafe responses, even though it has been trained to fol-
low instructions. This illustration highlights the fragility of
GPT 3.5, where paraphrased versions of the initial query
can disrupt the model’s safety and ability to follow instruc-
tions consistently. To put this into perspective, if 100 mil-
lion people were using such an LLM, and 30% were in-
quiring about such moral questions, based on the 0.3 error
probability (from Figure 3), approximately 9 million peo-
ple could potentially receive harmful responses with nega-
tive consequences. This raises the question of whether GPT
3.5’s behavior is unique or if other LLMs exhibit similar per-
formance (Ziems et al. 2022).
We concretize this claim by conducting experiments in-
volving seven different LLMs, utilizing a moral integrity
dataset comprising 20,000 samples and instructions (Ziems
et al. 2022). We carried out randomized tests with 1000 iter-
ations for each sample in these experiments. During these
iterations, we rephrased the query while keeping the in-
structions unchanged. Our evaluation focused on assessing
the LLMs’ performance in two aspects: safety (measured
through the averaged BART sentiment score (Yin, Hay, and
Roth 2019)) and consistency (evaluated by comparing the
provided Rule of Thumb (RoTtruth) instructions to the RoT
learned by the LLMs using BERTScore (Zhang et al. 2019)).
It is evident that GPT 3.5, Claude, and GPT 4.0 adhere
more closely to instructions than LLama2 (Touvron et al.
2023), Vicuna (Chiang et al. 2023), and Falcon (Penedo et al.
2023). However, even in the case of the significant LLMs,
the projected similarity score remains below 0.5. This sug-
gests that most LLMs don’t even follow the instructions,
and without following, they can generate similar responses
(since the BLEU score is low, the answers may or may not
be correct;), which indicates that models are unsafe and un-
explainable. The generated rule, referred to as RoTgen, is
provided by the LLM in response to the question, “ What is
the rule that you learned from these instances?”
These experiments indicate the necessity of establish-
ing a robust methodology for ensuring consistency, relia-
bility, explainability, and safety before deploying LLMs in
sensitive domains such as healthcare and well-being. An-
other concern to LLMs is prompt injection or adversarial
prompting, which can easily wipe off the attention of LLMs
to previous instructions and force them to act on the cur-
rent prompt. This has resulted in several issues with GPT3
(Branch et al. 2022). Thus, it is critical to establish a frame-
work like CREST for achieving trustworthiness.
Defining Consistency, Reliability, user-level
Explainability, and Safety
Consistency
A consistent LLM is an AI system that comprehends
user input and produces a response that remains un-
changed regardless of how different users phrase the
same input so far as the underlying facts, context,
and intent are the same. This mirrors the decision-
making behavior of a human.
It has been noted that LLMs show abrupt behavior when
the input is either paraphrased or there has been adversarial
perturbation [27]. Further, it has also been noted that LLMs
make implicit assumptions while generating a response to
a query that lacks sufficient context. For instance, the fol-
lowing two questions, “ Should girls be given the car? ” or
“Should girls be allowed to drive the car? ” show different
confidence levels in ChatGPT’s response. These two queries
are semantically similar and are paraphrases of each other
with a ParaScore > 0.90 (Shen et al. 2022). Thus, it is
presumed that LLMs would yield a similar response. How-
ever, in the first query, ChatGPT is “unsure”, whereas in the
second, it is pretty confident that “ girls should be allowed
to drive cars. ” Moreover, ChatGPT considers the question

FlanT5 Vicuna Falcon LLAMA LLAMA2 GPT3.5 GPT4 −0.5
0
0.5
1
BERTScore(RoTtruth ∼ RoTgen) Avg. BART Sentiment Score BLEU
Figure 3: A comparison of seven LLMs on the Moral Integrity Corpus. Despite the good BLEU (BiLingual Evaluation Under-
study) scores, LLMs fail to convince their understanding of the task. Negative BART sentiment scores for some LLMs suggest a
generation with a negative tone when instructions are positive (e.g., be polite, be honest). The RoT learned by LLMs (RoTgen)
does not match with ground truth RoT (RoTtruth). The Y-axis showcases scores from -1.0 to 1.0 for BART sentiments and 0.0
to 1.0 for BERTScore and BLEU. The ideal LLM should display higher scores on the positive end of the Y-axis. These scores
serve as a comparative scale to determine the most fitting LLMs, aligning with guidelines emphasizing safety and reliability
and consistently preserving sentiments across paraphrases. There is no notional threshold. The higher the score, the better the
LLM.
gender-specific in both cases, focusing on “ girls” and not
other words like “ drive” or “car.” For instance, given the
context, “ Should girls be given the toy car? ” or “ Should
girls with necessary driver’s license be allowed to drive
car?”, the ChatGPT yields a high confidence answer stat-
ing “ yes” in both scenarios. ChatGPT makes implicit as-
sumptions by wrongly placing its attention on less relevant
words and failing to seek more context from the user for
a stable response generation. If the ChatGPT had access to
knowledge, then it can retrieve the following information:
“Car < isrelatedto > Drive” and “Drive < requires >
Driver license”, and ground its response in factual and
common-sense knowledge. As demonstrated in subsequent
sections, a lack of such consistency can result in unsafe be-
havior.
Recent tools like SelfCheckGPT (Manakul, Liusie, and
Gales 2023) and CalibratedMath (Lin, Hilton, and Evans
2022) help assess LLMs’ consistency. However, the aspect
of enforcing consistency in LLMs remains relatively unex-
plored, particularly in the context of health and well-being.
The need for consistency is evident when considering ques-
tions related to health, such as, “ Should I take sedatives for
coping with my relationship issues? ” and “ Should I take
Xanax?”. ChatGPT provided an ambivalent “ Yes/No” an-
swer to the first question and a direct “ No” response to the
second when both questions were the same.
Putting this in a conversational scenario, when follow-
up questions like “ I am feeling drowsy by the day, and it
seems like hallucinations. Any advice? ” and “ I am feeling
sleep-deprived and hallucinating. What do you suggest? ”
are posed, these models encounter challenges. First, they
struggle to establish the connection between “ sleep depri-
vation” and “ drowsiness” with “ hallucinations.” Second,
the responses do not pay much attention to the concept of
“Xanax,” resulting in inconsistent response generation. Fur-
thermore, when prompted to include “ Xanax,” LLMs often
begin by apologizing and attempting to correct the response,
but these corrections still lack essential information. For in-
stance, they do not consider the various types of hallucina-
tions associated with Xanax (Alyssa 2023). This highlights
the need for improved consistency and depth of response in
LLMs, especially critical applications1, to ensure that users
receive more accurate and comprehensive information.
Reliability
Reliability measures to what extent a human can trust the
content generated by an LLM. This capability is critical for
the deployment and usability of LLM. Prior studies have ex-
amined reliability in LLMs by identifying the tendency of
hallucination, truthfulness, factuality, honesty, calibration,
robustness, and interpretability (Zhang et al. 2023). As seen
from the widely used notion of inter-rater reliability, little
attention is paid to the notion of reliability.
It is a common belief that a single annotator cannot at-
test to the credibility of the dataset. Likewise, a single LLM
cannot provide a correct and appropriate outcome for ev-
ery problem. This points to using an ensemble of LLMs (e-
LLMs) to provide higher confidence in the outcome, which
can be measured through Cohen’s or Fleiss Kappa’s metrics
(Wang et al. 2023a). Three types of ensembles can be de-
fined:
Shallow Ensembling LLMs work with the belief that
each LLM is trained with a different gigantic English cor-
pus, with different training regimes, and possesses a differ-
ent set of knowledge, enabling them to act differently on the
same input. Such an ensemble works on the assumption that
1Critical applications refer to situations in which the use of AI
has the potential to result in substantial harm to individuals or so-
cietal interests unless considerable precautions are taken to ensure
their consistency, reliability, explainability, and safety.

LLM is a knowledge base (Petroni et al. 2019). Three spe-
cific methods of e-LLMs are suggested under shallow en-
sembles: Rawlsian social welfare functions, utilitarian func-
tions (Kwon et al. 2022), or weighted averaging (Jiang, Ren,
and Lin 2023; Tyagi, Sarkar, and Gaur 2023; Tyagi et al.
2023).
Semi-Deep Ensembling LLMs involves adjusting and
fine-tuning the importance or contributions of each individ-
ual LLM needed throughout the ensembling process. This
approach effectively transforms the ensemble process into
an end-to-end training procedure. In this setup, the term
“semi-deep” implies that we are not just statically combining
the LLMs but dynamically adjusting their roles and weights
as part of the training process. This adaptability allows us to
craft a more sophisticated and flexible ensemble.
These two approaches offer several advantages. First, it
enables the model to learn which LLMs are most effective
for different aspects of a given task. For example, certain
LLMs might better understand syntax, while others excel at
capturing semantics or domain-specific knowledge. By fine-
tuning their contributions, we can harness the strengths of
each LLM for specific subtasks within a larger task. Sec-
ond, it allows the model to adapt to changes in the data or
the task itself. As new data is introduced or the problem
evolves, individual LLMs’ contributions can be adjusted ac-
cordingly, ensuring that the ensemble remains effective and
up-to-date. However, these ensembles ignore the following
key elements:
• External Knowledge Integration: The approach involves
integrating external knowledge sources, such as Knowl-
edge Graphs (KGs) and Clinical Practice Guidelines, into
the LLM ensemble. These sources provide additional
context and information that can enhance the quality of
the generated text.
• Reward Functions:The external knowledge is not simply
added as static information but is used as reward func-
tions during the ensembling process. In simpler terms,
this means the ensemble of models gets rewarded when
they produce text that matches or incorporates external
knowledge. This reward system promotes logical consis-
tency and meaningful connections with that knowledge.
– Logical Coherence: By incorporating external knowl-
edge, the ensemble of LLMs aims to produce a more
logically coherent text. It ensures the generated con-
tent aligns with established facts and relationships in
the external knowledge sources.
– Semantic Relatedness: The ensemble also focuses on
improving the semantic relatedness of the generated
text. This means that the text produced by the LLMs
is factually accurate, contextually relevant, and mean-
ingful.
Such attributes are important when LLMs are designed for
critical applications like Motivational Interviewing (Sarkar
et al. 2023). Motivational interviewing is a communication
style often used in mental health counseling, and ensur-
ing logical coherence and semantic relatedness in generated
responses is crucial for effective interactions (Shah et al.
2022b).
Deep Ensemble of LLMs introduces an innovative ap-
proach using NeSy-AI, in which e-LLMs are fine-tuned with
the assistance of an evaluator. This evaluator comprises con-
straints and graph-based knowledge representations and of-
fers rewards to guide the generation of e-LLMs based on
the aforementioned properties. Concurrently, it incorporates
knowledge source concepts in the form of representations to
compel e-LLMs to include and prioritize these concepts, en-
hancing their reliability (refer to Figure 7 for illustration).
Another key objective of the deep ensemble approach is to
transform e-LLMs into a Mixture of Experts (Artetxe et al.
2022) by enhancing individual LLMs through a performance
maximization function (Kwon et al. 2022).
Explainability and User-level Explainable LLMs
(UExMs)
Achieving effective and human-understandable explanations
from LLMs or even from their precursor language mod-
els (LMs) remains complex. Previous attempts to elucidate
BlackBox LMs have utilized techniques like surrogate mod-
els (such as LIME (Ribeiro, Singh, and Guestrin 2016)),
visualization methods, and adversarial perturbations to the
input data (Chapman-Rounds et al. 2021). While these ap-
proaches provide explanations, they operate at a relatively
basic level of detail, which we have referred to as system-
level explainability (Gaur 2022).
System-level Explainability has been developed under the
purview of post-hoc Explainability techniques that aim to
interpret the attention mechanism of LMs/LLMs without af-
fecting their learning process. These techniques establish
connections between the LM’s attention patterns and con-
cepts sourced from understandable knowledge repositories.
Within this approach, two methods have emerged: (a) Attri-
bution scores and LM Tuning (Slack et al. 2023) and Fac-
tual Knowledge-based Scoring and LM Tuning (Yang et al.
2023b; Sun et al. 2023). The latter method holds particu-
lar significance in the domain of health and well-being be-
cause it focuses on providing explainability for clinicians
as users. This method relies on KGs or knowledge bases
like the Unified Medical Language System (UMLS) (Boden-
reider 2004), SNOMED-CT (Donnelly 2006), or RXNorm
(Nelson et al. 2011) to enhance its functionality.
While the post-hoc method can provide explanations (by
modeling it as a dialogue system (Lakkaraju et al. 2022)),
it does not guarantee that the model consistently prioritizes
essential elements during training (Jiang et al. 2021). Its ex-
planations may be coincidental and not reflect the model’s
actual decision-making process. More recently, the focus has
shifted to “explainability by design,” particularly in critical
applications like healthcare. A recent example is the Trans-
parency and Interpretability Framework for Understandabil-
ity (TIFU), proposed by Joyce et al. (2023), which connects
inherent explainability to a higher level of explainability in
the mental health domain. The primary motivation for pur-
suing such an explainability, called User-level explainabil-
ity, is to ensure that healthcare professionals and patients are

given contextually relevant explanations that help them un-
derstand the AI system’s process and outcomes so they can
develop confidence in AI tools.
A User-level Explainability in LLMs implies that
humans can rely on the AI system to the extent that
they can reduce the need for human oversight, mon-
itoring, and verification of the system’s outputs. To
trust a deployed LLM, we must have adequate in-
sight into how it generates an output based on a
given input.
UExMs
UExMs provide user-explainable insights by uti-
lizing expert-defined instructions, statistical knowl-
edge (attention), and knowledge retriever.
UExMs can be practically realized in four different ways:
UExMs with Generating Evaluator Pairing: This de-
fines a generative and evaluator-based training of UExMs
where any LLM is paired with a knowledge-powered evalua-
tor, either accelerates or deaccelerates the training of LLMs,
depending on whether the final generation is within the ac-
ceptable standards of the evaluator. “On the weekend, when I
want to relax, I am bothered by trouble concentrating while
reading the newspaper or watching television. Need some
advice” clearly indicates that the individual is experiencing
specific issues related to concentration during leisure time.
This query is more than just a casual comment; it highlights
a problem that is affecting the user’s ability to unwind effec-
tively. Now, consider the two scenarios:
• Without an Evaluator (Generic Response): In the ab-
sence of an evaluator, an LLM might provide a generic
set of activities or advice, such as “practice mindfulness,
limit distractions, break tasks into smaller chunks,” and
so on. While this advice is generally useful for improving
concentration, it lacks the depth and specificity needed to
address the user’s potential underlying issues.
• With an Evaluator (Specific Response): When integrated
into the LLM, an evaluator can analyze the user’s query
more comprehensively. In this case, the evaluator can rec-
ognize that the user’s difficulty concentrating during re-
laxation may indicate an underlying sleep-related issue.
Considering this possibility, the language model can pro-
vide more targeted and informed advice.
For instance, the evaluator might suggest asking fur-
ther questions like: (a) Do you have trouble sleeping at
night? (b) How much sleep do you typically get on week-
ends? (c) Have you noticed other sleep-related symp-
toms, such as daytime drowsiness? (d) Have you con-
sidered the possibility of a sleep disorder? By incorpo-
rating an evaluator, the LLM can guide the conversation
toward a more accurate understanding of the user’s sit-
uation. To put it simply, the LLM, when assisted by an
evaluator, will provide a coherent answer that encom-
passes all aspects of the user’s question (Gaur et al. 2022,
2023). Further, the evaluator prevents the model from
generating hallucinated, off-topic, or overly generic re-
sponses. A framework like ISEEQ integrates generator
and evaluator LLMs for generating tailored responses
in general-purpose and mental health domains (Gaur
et al. 2022). Additionally, PURR and RARR contribute
to refining segments of LLM design aimed at mitigat-
ing hallucination-related problems in these models (Chen
et al. 2023; Gao et al. 2023).
To illustrate this concept, refer to Figure 4, which illustrates
a task where a generative LM takes user input and pro-
vides an assessment in natural language, specifically within
the PHQ-9 context (Dalal et al. 2023). The figure shows
two LLMs: ClinicalT5-large, a powerful LM with 38 bil-
lion parameters, and UExM, which is essentially ClinicalT5-
large but enhanced with a PHQ-9-grounded evaluator. This
demonstrates that by employing an evaluator with prede-
fined questions, we can assess how well the attention of gen-
erative ClinicalT5-large aligns with those specific questions.
This approach helps ensure that the generated explanations
are relevant and comprehensive, making them clinically ap-
plicable, particularly when healthcare professionals rely on
standardized guidelines like the PHQ-9 to evaluate patients
for depression (Honovich et al. 2022).
UExMs with Retriever Augmentation and Process
Knowledge: It’s commonly observed that the process of
generating responses by LLMs lacks transparency, making it
difficult to pinpoint the origin of their answers. This opacity
raises questions about how the model derives its responses.
• The emergence of Retrieval-Augmented Generation LMs:
A novel class of LMs has surfaced to tackle this is-
sue and add a layer of supervision to language model
outputs. Examples include REALM (Guu et al. 2020),
LAMA (Petroni et al. 2019), ISEEQ (Gaur et al. 2022),
and RAG (Lewis et al. 2020), which integrate a gen-
erator with a dense passage retriever and access to in-
dexed data sources. LLMs with retrieval-augmented ar-
chitectures have started to show understandable and ac-
countable responses (Lyu et al. 2023). For instance, Go-
pherCite (Menick et al. 2022) and NeMo Guardrails
(Rebedea et al. 2023) are LLMs that leverage a knowl-
edge base to supply supporting evidence for nearly every
response generated by the underlying LLM.
• The emergence of Process Knowledge-guided Genera-
tion LMs: Process Knowledge refers to guidelines or in-
structions created by experts in a domain (Roy et al.
2023). For instance, in mental health, PHQ-9 is the pro-
cess of knowledge for screening depression (Kroenke,
Spitzer, and Williams 2001), NIDA’s Attention Defi-
ciency Hyperactivity Disorder Test, and the World Health
Organization’s Wellness Indices (Topp et al. 2015). The
questions in these guidelines can act as rewards for en-
riching latent generations (e.g., answerability test (Yao
et al. 2023b)) (Hagendorff 2023).
UExMs with Abstention While a retriever has been in-
tegrated into an LLM, it doesn’t guarantee meaningful ex-
plainability. When considering a ranked list of retrieved and

Figure 4: An instance of user-level explainability in a UExM is when the model uses questions from PHQ-9 to guide its actions
and relies on SNOMED-CT, a clinical knowledge base, to simplify complex concepts (concept abstraction). This approach
helps the model offer explanations that closely align with the ground truth. PHQ9-DO: PHQ-9-based Depression Ontology.
expanded documents, an LLM is still vulnerable to gen-
erating incorrect or irrelevant explanations. Therefore, it’s
crucial to eliminate meaningless hidden generations before
they are converted into natural language. For example, the
ReACT framework employs Wikipedia to address spurious
generation and explanations in LLMs (Yao et al. 2022).
However, it relies on a prompting method rather than a well-
grounded domain-specific approach, which can influence
the generation process used by the LLM (Yang et al. 2023a).
Alternatively, pruning methods and an abstention rule have
also been used to reduce irrelevant output from LLMs. A
more robust approach would involve utilizing procedural or
external knowledge as an evaluator guiding LLM-generated
content that enhances meaningful understanding.
Safety
Safety and explainability are closely intertwined
concepts for AI systems. While a safe AI system
will inherently demonstrate explainability, the re-
verse isn’t necessarily true; an explainable system
may or may not be safe.
Recently, there has been a proliferation in safety-enabled
research, particularly in LMs and LLMs. Perez et al. (2022)
performed red-teaming between LMs to determine if an LM
can produce harmful text. The process did not include hu-
mans in generating these adversarial test cases. Further, the
research did not promise to address all the critical safety
oversights comprehensively; instead, it aimed to spotlight
instances where LMs might exhibit unsafe behavior. Scher-
rer et al. (2023) delves more deeply into the safety issues in
LLMs by examining their behavior in moral scenarios. The
study found that LLMs only focus on generating fluent sen-
tences and overlook important words/concepts contributing
to stable decisions. Further, datasets like DiSafety and Safe-
TexT are designed to induce safety in LMs/LLMs through
supervised learning (Meade et al. 2023; Levy et al. 2022).
These discussions surrounding safety gained heightened at-
tention, particularly within the National Science Foundation
(NSF), leading to the launch of two programs: (a) Safety-
enabled Learning and (b) Strengthening AI. In a recent we-
binar, NSF outlined three fundamental attributes of ensuring
safety: grounding, instructability, and alignment2.
Grounding: In essence, groundedness is the foundation
upon which both explainability and safety rest. Without a
strong grounding in the provided instructions, the AI may
produce results that stray from the desired outcome, poten-
tially causing unintended consequences. For instance, con-
sider the scenario depicted in Figure 5. An LLM that isn’t
grounded in domain-specific instruction, like the ChatGPT,
results in an unsafe response. On the other hand, a relatively
simple LLM, like T5-XL, tuned by grounding in domain-
specific instructions, attempts to ask follow-up questions to
gather the necessary context for a coherent response. The
changes in T5-XL’s behavior due to the NIDA 3 quiz high-
light the importance of being able to instruct and align AI,
which is key for safety4.
Instructability: In the context of AI safety, instructability
encompasses the assurance that the AI understands and com-
plies with user preferences, policies, and moral beliefs. Mak-
ing the LMs bigger and strengthening the rewards makes the
models power-hungry rather than ethical and safe. For in-
2https://new.nsf.gov/funding/opportunities/national-artificial-
intelligence-research
3National Institute on Drug Abuse
4https://psychcentral.com/quizzes/adhd-quiz

Figure 5: An Illustration of grounding and instruction-
following behavior in an LLM (right) tuned with support
from health and well-being-specific guidelines. ChatGPT’s
response was correct, but it isn’t safe.
stance, the guardrails instantiated for the safe functioning in
OpenAI’s ChatGPT, the rules within DeepMind’s Sparrow,
and the list of rules within Anthropic’s Claude cannot reli-
ably prove that they are safe.
The idea of having systems that follow instructions has
been around since 1991, mainly in robotics and, to some ex-
tent, in text-based agents. It’s crucial because it helps agents
learn tasks, do them well, and explain how they did it, mak-
ing sharing knowledge easier between humans and AI and
showing they can follow human instructions. One way to
do this is by using grounded instruction rules, especially in
the field of mental health. Clinical practice guidelines like
PHQ-9 for depression and GAD-7 for anxiety, with their
questions, can serve as instructions for AI models focused
on mental health. Grounded rules have two key benefits for
safety. First, they tend to be helpful and harmless, addressing
a common challenge for AI models. Second, they promote
absolute learning, avoiding tricky trade-off situations.
Alignment: When we talk about alignment in LMs, it
means ensuring that even a model designed to follow
instructions doesn’t produce unsafe results (MacDonald
1991). This can be a tricky problem, as discussed in Nick
Bostrom’s book “Superintelligence,” where it’s called “per-
verse instantiations ” (Bostrom 2014). This happens when
the LM/LLMs figure out how to meet a goal, but it goes
against what the user wants (Ngo, Chan, and Mindermann
2022). So, the challenge is to create an AI that follows in-
structions and finds the best way to achieve a goal while
keeping users happy, a concept referred to as “Wireheading”
in “Superintelligence.” Following are perspectives on why it
happens and what can be done:
• Context Awareness (CA) and Contextual Rewards (CR):
CA refers to the training of LMs/LLMs to focus on words
or phrases that have direct translation to concepts in fac-
tual knowledge sources. CR serves the function of facil-
itating CA. They achieve this by incorporating evaluator
modules that analyze the hidden or latent representations
within the model with respect to the concepts present in
the knowledge sources. CR reinforces and guides CA by
rewarding the model when it correctly identifies and in-
corporates knowledge-based concepts into its responses.
• Misalignment in latent representations caused by mis-
leading reward associations:We acknowledge the inher-
ent perceptiveness of LMs and LLMs, a quality closely
linked to the quantity of training data they are exposed
to. Nevertheless, having a larger training dataset leads
to superior performance scores, but it may not necessar-
ily meet the expectations of human users. Bowman has
demonstrated that a model achieving an F1 score of over
80% still struggles to prioritize and pay adequate atten-
tion to the concepts users highly value (Bowman 2023).
This happens because optimization algorithms and atten-
tion methods in LLMs can attempt to induce fake be-
havior. Further, if the rewards specified are not unique to
the task but rather general, the model will have difficulty
aligning with desired behaviors (Shah et al. 2022a).
• Deceptive Alignment during Training: Spurious reward
collections can lead to deceptive training. It is important
to train the LMs/LLMs with paraphrases and adversar-
ial input while examining the range of reward scores and
the variations in the loss functions. If LMs/LLMs demon-
strate high fluctuations in the rewards and the associated
effect on loss, it would most likely result in brittleness
during deployment. Methods like the chain of thoughts
and the tree of thoughts prompting can act as sanity
checks to examine the deceptive nature of LMs/LLMs
(Connor Leahy 2023; Yao et al. 2023a).
Brief Summary
Knowledge of the AI system and domain is per-
vasive in achieving consistency, reliability, explain-
ability, and safety for building aTrustworthy AI sys-
tem.
• For Consistency, rules, and knowledge can make
LLMs understand and fulfill user expectations
confidently
• Reliability is ensured by utilizing the rich knowl-
edge contained in KGs to empower an ensem-
ble of LLMs to produce consistent and mutually
agreeable results with high confidence.
• For Explainability, LLMs use their knowledge,
retrieved knowledge, and rules that were fol-
lowed to attain consistency and reliability to ex-
plain the generation effectively.
• Safety in LLMs is upheld by consistently ground-
ing their generation and explanations in domain
knowledge and assuring the system’s adherence
to expert-defined rules or guidelines.
The CREST Framework
To realize CREST, we now provide succinct descriptions of
its key components and highlight open challenges for AI and
NeSy-AI communities in NLP (see Figure 6). We delve into

three components of the CREST framework in the following
subsections:
NeSy-AI for Paraphrased and Adversarial
Perturbations
Paraphrasing serves as a technique to enhance an AI agent’s
calibration by making it aware of the different ways an in-
put could be expressed by a user (Du, Xing, and Cam-
bria 2023). This, in turn, contributes to increasing the AI
agent’s consistency and reliability. Agarwal et al. introduced
a pioneering NeSy AI-based approach to paraphrasing. In
their method, they employed CommonSense, WordNet, and
Wikipedia knowledge graphs to generate paraphrases that
held equivalent meanings but were perceived as distinct by
the AI agent (Agarwal et al. 2023). However, there are some
promising directions for NeSy paraphrasing. First is con-
textualization, which involves augmenting the input with
meta-information retrieved from a rank list of documents.
This transforms NLP’s not-so-old question rewriting prob-
lem into a knowledge-guided paraphrasing method. The sec-
ond is abstraction, which involves identifying the function
words (e.g., noun phrases, verb phrases) and named entities
and replacing them with abstract concepts. For instance, the
following sentence, “ Why trauma of harassment is high in
boys|girls?” is abstracted to “ why trauma of (harassment
→ mistreatment) is high in (boys|girls → students)?”. Both
of these methods can benefit from existing learning strate-
gies of LLMs, such as marginalization (Wang et al. 2022)
and reward-based learning (Jie et al. 2023).
NeSy-AI for adversarial perturbations (AP) uses general-
purpose KGs to carefully change the sentence to examine
the brittleness in LLMs’ outcomes.
Example of Adversarial Generation using NeSy-AI
S1: I have been terrible in battling with my loneli-
ness. My overly introvertedness and terrible choice
of few friends are the reasons for who I am. The
only part I considered funny in this situation was that
none of my friends knew how I felt. It seems they are
childish.
S1-AP: I have been horrible at battling my loneli-
ness. My overly introvertedness andhorrible choice
of few friends are the reasons for who I am. The only
part I regarded as sarcastic in this situation was that
none of my friends knew how I felt. It seems they
are youngsters.
The Flan T5 (11B) estimates S1 to have a “negative” sen-
timent with a confidence score of 86.6% and S1-AP to have
a “positive” sentiment with a 61.8% confidence score. The
confidence scores are predicted probability estimates. LLMs
must concentrate on the contextual notions (such as loneli-
ness and introversion) and the abstract meaning that under-
lies both S1 and S1-AP—that is, the influence on mental
health and well-being—to attain consistency and reliability
in such inadvertent settings.
Knowledge-infused Ensembling of LLMs
As mentioned above, e-LLMs have many benefits; how-
ever, simply statistical methods of ensembling, which con-
sist of averaging the outcomes from black box LLMs,
do not make an ensembled LLM consistent and reli-
able. Knowledge-infused Ensemble represents a particu-
lar methodology where the knowledge (general purpose or
domain-specific) modulates the latent representations of the
LLMs to yield the best of world outcomes. This can happen
in one of three ways:
1. LLMs over KGs (KnowLLMs): Similar to the process of
training any LLM on text documents, which involves for-
mulating it as a task of predicting the next word in a sen-
tence, KnowLLMs undertake the training of LLMs using
a variety of KGs such as CommonSense, Wikipedia, and
UMLS. In KnowLLMs, the training objective is rede-
fined as an autoregressive function over < subject ><
predicate >< object >coupled with pruning based on
existing state-of-the-art KG embedding methods. Intro-
ducing pruning is crucial in KnowLLMs to prevent the
model from making unwarranted inferences and forming
incorrect links. This is vital for ensuring the safety and
trustworthiness of the knowledge generated by KnowL-
LMs. In other words, by pruning, KnowLLMs can fil-
ter out irrelevant or potentially misleading information,
thereby enhancing the quality of their responses and min-
imizing the risk of spreading false or harmful knowledge.
2. Generative Evaluator Tuning: This approach suggests
using reinforcement learning to improve the training of
e-LLMs. It combines the traditional training method with
rewards from KnowLLMs, which act as extra guidelines.
These rewards encourage the e-LLM to generate text
that aligns with specific desired characteristics, such as
mental health concepts. If the e-LLM’s output doesn’t
meet these criteria or is logically incorrect according to
KnowLLM, it receives negative rewards, even if it’s sim-
ilar to the ground truth based on similarity scores. This
method helps e-LLMs produce more contextually rele-
vant and accurate text.
3. Instruction Following Tuning:Instruction Tuning has re-
cently emerged as a promising direction to teach LLMs
to match the expectations of humans. Though promising,
it requires a substantial amount of samples, and there is
no perfect quantifiable method to measure the “ instruc-
tion following ” nature of LLMs. And, if we decide to
embark on a “mixture of experts” like e-LLMs, it would
be hard to make separate procedures for instruction tun-
ing over e-LLMs. Thus, we take inspiration from Pro-
cess Knowledge-infused Learning, a mechanism for in-
trinsically tuning the LMs or an ensemble of LMs. Roy
et al. demonstrated how questionnaires in the clinical do-
main, which can be considered a constraint, can enable
LMs to generate safe and consistently relevant questions
and responses (Roy et al. 2023). This approach works
on a simple Gumble Max function, which allows struc-
tural guidelines to be used in the end-to-end training of
LMs. This approach is fairly flexible for “ instruction-
following-tuning” of e-LLMs and ensuring the instruc-

Figure 6: The CREST framework operationalizes “explainability and safety” by ensuring the model is reliable and consistent.
LLMs (1 to m) can be replaced with LLMs in Figure 2, and the knowledge used in infusion refers to UMLS and SNOMED-
CT for a clinical domain, as we examined CREST for mental health. Gen-Eval: Generator and Evaluator pairing. KnowLLM:
LLMs created using KGs.
tion is followed.
Assessment of CREST
The CREST framework significantly emphasizes incorpo-
rating knowledge and utilizing knowledge-driven rewards
to support e-LLMs in achieving trust. To assess the qual-
ity of e-LLMs’ output, it’s crucial to employ metrics that
account for the knowledge aspect. For instance, the logi-
cal coherence metric evaluates how well the content gen-
erated by e-LLMs aligns with the flow of concepts in KGs
and context-rich conversations. Additional metrics like Elo
Rating (Zheng et al. 2023), BARTScore (Liu et al. 2023),
FactCC (Kry´sci´nski et al. 2020), and Consistency lexicons
can be improved to account for the influence of knowledge
on e-LLMs’ generation. However, when it comes to assess-
ing reliability, aside from the established Cohen’s or Fleiss
Kappa metrics, an effective alternate metric is not available.
Safety aspects in CREST are best evaluated when
knowledge-tailored e-LLMs are instructed to adhere to
guidelines established by domain experts. Existing metrics
like PandaLM (Wang et al. 2023b) and AlpacaFarm (Dubois
et al. 2023) are based on LLMs, which themselves may ex-
hibit vulnerabilities to unsafe behaviors. While such met-
rics may be suitable for open-domain applications, when it
comes to critical applications, safety metrics must be rooted
in domain expertise and align with the expectations of do-
main experts.
In CREST, explainability is evaluated through two ap-
proaches requiring expert verification and validation. One
method involves analyzing the “Knowledge Concept to Word
Attention Map ” to gain insights into CREST’s reasoning
process and verify whether the model’s decisions align with
domain knowledge and expectations (Gaur et al. 2018).
Another method involves using knowledge concepts and
domain-specific decision guidelines (e.g., clinical practice
guidelines) to enable LLMs like GPT 3.5 to generate human-
understandable explanations (as shown in Figure 4).
A Case Study in Mental Health in Brief
We present a preliminary performance of CREST on the
PRIMATE dataset, introduced during ACL’s longstanding
Clinical Psychology workshop (Gupta et al. 2022). It is
a distinctive dataset designed to assess the LM’s ability
to consistently estimate an individual’s level of depression
and provide yes/no responses to PHQ-9 questions, which
is a measure of its reliability. Figure 7 shows the perfor-
mance of CREST and knowledge-powered CREST rela-
tive to GPT 3.5. Including knowledge in CREST showed
an improvement of 6% in PHQ-9 answerability and 21%
in BLEURT over GPT 3.5, which was used through the
prompting method. The e-LLMs in CREST were Flan T5-
XL (11B) and T5-XL (11B).
Conclusion and Future Work
LLMs and broadly generative AI represent the most ex-
citing current approach but are not the solution for Trust-

Baseline(T5-XL) Knowledge(CREST) GPT3.5 0
0.5
1
score
BLEU BLEURT PHQ-Ans BERTScore
Figure 7: The CREST findings on the PRIMATE dataset in-
clude PHQ-9 answerability, calculated as the mean Matthew
Correlation Coefficient score. This score is computed by
comparing predicted Yes/No labels against the ground truth
across nine PHQ-9 questions. BLEURT score is computed
between questions generated by LLMs and PHQ-9 ques-
tions (Sellam, Das, and Parikh 2020). LLMs were prompted
to create questions based on sentences identified as potential
answers to the PHQ-9 questions. PHQ-Ans: PHQ-9 Answer-
ability.
worthy AI alone. LLMs exhibit undesired behaviors during
tasks such as question answering, making them suscepti-
ble to threats and resultant problematic actions. Therefore,
there is a need for innovative approaches to identify and
mitigate threats posed both to LLMs and by LLMs to hu-
mans, especially when they are to be used for critical ap-
plications such as those in health and well-being. A com-
prehensive solution is needed beyond the implementation of
guardrails or instruction adjustments. This solution should
encourage LLMs to think ahead, leveraging domain knowl-
edge for guidance. The CREST framework offers a promis-
ing approach to training LLMs with domain knowledge, en-
abling them to engage in anticipatory thinking through tech-
niques like paraphrasing, adversarial inputs, knowledge in-
tegration, and fine-tuning based on instructions.
We presented a preliminary effort in implementing the
CREST framework that yields enhancements over GPT3.5
on PRIMATE, a PHQ-9-based depression detection dataset.
We plan to experiment with CREST on knowledge-intensive
language generation benchmarks, like HELM (Liang et al.
2022). Further, we plan on automating user-level expla-
nations without dependence on pre-trained LLMs (e.g.,
GPT3.5). Our future endeavors involve developing more ef-
fective training methodologies for e-LLMs powered by the
CREST framework. Additionally, we will incorporate robust
paraphrasing and adversarial generation techniques to assess
the consistency and reliability of e-LLMs when they are ex-
posed to knowledge. This will also open avenues for further
research into crafting quantitative metrics that evaluate reli-
ability, safety, and user-level explainability.
Acknowledgement
We express our gratitude to Drs. Amitava Das and Valerie
L. Shalin for their invaluable reviews and insightful sug-
gestions on the manuscript. We acknowledge partial sup-
port from the NSF EAGER award #2335967 and the UMBC
Summer Faculty Fellowship. Any opinions, conclusions, or
recommendations expressed in this material are those of the
authors and do not necessarily reflect the views of the NSF
or UMBC.
References
Agarwal, A.; Gupta, S.; Bonagiri, V .; Gaur, M.; Reagle, J.;
and Kumaraguru, P. 2023. Towards Effective Paraphrasing
for Information Disguise. In European Conference on Infor-
mation Retrieval, 331–340. Springer.
Alyssa. 2023. Do Benzodiazepines cause Hallucinations?
— Banyan Palm Springs — banyantreatmentcenter.com.
https://www.banyantreatmentcenter.com/2021/12/03/
benzodiazepines-causing-hallucinations-palmsprings/.
[Accessed 30-11-2023].
Artetxe, M.; Bhosale, S.; Goyal, N.; Mihaylov, T.; Ott, M.;
Shleifer, S.; Lin, X. V .; Du, J.; Iyer, S.; Pasunuru, R.; et al.
2022. Efficient Large Scale Language Modeling with Mix-
tures of Experts. In Proceedings of the 2022 Conference
on Empirical Methods in Natural Language Processing ,
11699–11732.
Bai, Y .; Kadavath, S.; Kundu, S.; Askell, A.; Kernion, J.;
Jones, A.; Chen, A.; Goldie, A.; Mirhoseini, A.; McKinnon,
C.; et al. 2022. Constitutional ai: Harmlessness from ai feed-
back. arXiv preprint arXiv:2212.08073.
Bodenreider, O. 2004. The unified medical language system
(UMLS): integrating biomedical terminology. Nucleic acids
research.
Bostrom, N. 2014. Superintelligence: Paths, Dangers,
Strategies. USA: Oxford University Press, Inc. ISBN
0199678111.
Bowman, S. R. 2023. Eight things to know about large lan-
guage models. arXiv preprint arXiv:2304.00612.
Branch, H. J.; Cefalu, J. R.; McHugh, J.; Hujer, L.; Bahl,
A.; Iglesias, D. d. C.; Heichman, R.; and Darwishi, R. 2022.
Evaluating the susceptibility of pre-trained language mod-
els via handcrafted adversarial examples. arXiv preprint
arXiv:2209.02128.
Bumgardner, V .; Mullen, A.; Armstrong, S.; Hickey, C.; and
Talbert, J. 2023. Local large language models for complex
structured medical tasks. arXiv preprint arXiv:2308.01727.
Chapman-Rounds, M.; Bhatt, U.; Pazos, E.; Schulz, M.-
A.; and Georgatzis, K. 2021. FIMAP: Feature importance
by minimal adversarial perturbation. In Proceedings of
the AAAI Conference on Artificial Intelligence , volume 35,
11433–11441.
Chen, A.; Pasupat, P.; Singh, S.; Lee, H.; and Guu, K. 2023.
PURR: Efficiently Editing Language Model Hallucinations
by Denoising Language Model Corruptions. arXiv preprint
arXiv:2305.14908.
Chiang, W.-L.; Li, Z.; Lin, Z.; Sheng, Y .; Wu, Z.; Zhang, H.;
Zheng, L.; Zhuang, S.; Zhuang, Y .; Gonzalez, J. E.; Stoica,
I.; and Xing, E. P. 2023. Vicuna: An Open-Source Chatbot
Impressing GPT-4 with 90%* ChatGPT Quality.

Chung, H. W.; Hou, L.; Longpre, S.; Zoph, B.; Tay, Y .; Fe-
dus, W.; Li, Y .; Wang, X.; Dehghani, M.; Brahma, S.; et al.
2022. Scaling instruction-finetuned language models. arXiv
preprint arXiv:2210.11416.
Connor Leahy, G. A. 2023. Cognitive Emulation: A
Naive AI Safety Proposal — AI Alignment Forum —
alignmentforum.org. https://www.alignmentforum.org/
posts/ngEvKav9w57XrGQnb/cognitive-emulation-a-naive-
ai-safety-proposal. [Accessed 01-12-2023].
Dalal, S.; Tilwani, D.; Gaur, M.; Jain, S.; Shalin, V .; and
Seth, A. 2023. A Cross Attention Approach to Diagnos-
tic Explainability using Clinical Practice Guidelines for De-
pression. arXiv:2311.13852.
Daws, R. 2023. Medical chatbot using OpenAI’s GPT-3 told
a fake patient to kill themselves — artificialintelligence-
news.com. https://www.artificialintelligence-news.com/
2020/10/28/medical-chatbot-openai-gpt3-patient-kill-
themselves/. [Accessed 30-11-2023].
Donnelly, K. 2006. SNOMED-CT: The advanced terminol-
ogy and coding system for eHealth. Studies in health tech-
nology and informatics, 121: 279—290.
Du, K.; Xing, F.; and Cambria, E. 2023. Incorporating mul-
tiple knowledge sources for targeted aspect-based financial
sentiment analysis. ACM Transactions on Management In-
formation Systems.
Dubois, Y .; Li, X.; Taori, R.; Zhang, T.; Gulrajani, I.; Ba, J.;
Guestrin, C.; Liang, P.; and Hashimoto, T. B. 2023. Alpaca-
farm: A simulation framework for methods that learn from
human feedback. arXiv preprint arXiv:2305.14387.
Gao, L.; Dai, Z.; Pasupat, P.; Chen, A.; Chaganty, A. T.; Fan,
Y .; Zhao, V .; Lao, N.; Lee, H.; Juan, D.-C.; et al. 2023. Rarr:
Researching and revising what language models say, using
language models. InProceedings of the 61st Annual Meeting
of the Association for Computational Linguistics (Volume 1:
Long Papers), 16477–16508.
Gartner. 2023. 4 Exciting New Trends in the Gartner
Emerging Technologies Hype Cycle — gartner.com.
https://www.gartner.com/en/articles/what-s-new-in-the-
2023-gartner-hype-cycle-for-emerging-technologies.
[Accessed 30-11-2023].
Gaur, M. 2022. Knowledge-Infused Learning.
Gaur, M.; Gunaratna, D. A. K. S. S.; Srinivasan, V .; and
Jin, H. 2023. Dynamic question generation for information-
gathering. US Patent App. 17/817,778.
Gaur, M.; Gunaratna, K.; Srinivasan, V .; and Jin, H. 2022.
Iseeq: Information seeking question generation using dy-
namic meta-information retrieval and knowledge graphs. In
Proceedings of the AAAI Conference on Artificial Intelli-
gence, 10672–10680.
Gaur, M.; Kursuncu, U.; Alambo, A.; Sheth, A.; Daniu-
laityte, R.; Thirunarayan, K.; and Pathak, J. 2018. ” Let me
tell you about your mental health!” Contextualized classifi-
cation of reddit posts to DSM-5 for web-based intervention.
In Proceedings of the 27th ACM International Conference
on Information and Knowledge Management, 753–762.
Gautam, S.; Jain, A.; Gautam, M.; Vahia, V . N.; and Grover,
S. 2017. Clinical practice guidelines for the management of
depression. Indian journal of psychiatry, 59(Suppl 1): S34.
Gupta, S.; Agarwal, A.; Gaur, M.; Roy, K.; Narayanan, V .;
Kumaraguru, P.; and Sheth, A. 2022. Learning to Automate
Follow-up Question Generation using Process Knowledge
for Depression Triage on Reddit Posts. InProceedings of the
Eighth Workshop on Computational Linguistics and Clinical
Psychology, 137–147.
Guu, K.; Lee, K.; Tung, Z.; Pasupat, P.; and Chang, M.
2020. Retrieval augmented language model pre-training. In
International conference on machine learning , 3929–3938.
PMLR.
Hagendorff, T. 2023. Machine psychology: Investigat-
ing emergent capabilities and behavior in large language
models using psychological methods. arXiv preprint
arXiv:2303.13988.
Holohan, M. 2023. A boy saw 17 doctors over 3
years for chronic pain. ChatGPT found the diagnosis —
today.com. https://www.today.com/health/mom-chatgpt-
diagnosis-pain-rcna101843. [Accessed 30-11-2023].
Honovich, O.; Aharoni, R.; Herzig, J.; Taitelbaum, H.; Kuk-
liansy, D.; Cohen, V .; Scialom, T.; Szpektor, I.; Hassidim,
A.; and Matias, Y . 2022. TRUE: Re-evaluating Factual Con-
sistency Evaluation. In Proceedings of the 2022 Confer-
ence of the North American Chapter of the Association for
Computational Linguistics: Human Language Technologies,
3905–3920.
Itai brun, T. s.-a. 2023. Yom Kippur War: Chat-
GPT can be used or military intel, war simulation —
jpost.com. https://www.jpost.com/business-and-innovation/
opinion/article-760273. [Accessed 30-11-2023].
Jiang, D.; Ren, X.; and Lin, B. Y . 2023. LLM-Blender: En-
sembling Large Language Models with Pairwise Ranking
and Generative Fusion. arXiv preprint arXiv:2306.02561.
Jiang, Z.; Araki, J.; Ding, H.; and Neubig, G. 2021. How can
we know when language models know? on the calibration
of language models for question answering. Transactions of
the Association for Computational Linguistics, 9: 962–977.
Jie, R.; Meng, X.; Shang, L.; Jiang, X.; and Liu, Q. 2023.
Prompt-Based Length Controlled Generation with Rein-
forcement Learning. arXiv preprint arXiv:2308.12030.
Joyce, D. W.; Kormilitzin, A.; Smith, K. A.; and Cipriani,
A. 2023. Explainable artificial intelligence for mental health
through transparency and interpretability for understandabil-
ity. npj Digital Medicine, 6(1): 6.
Krishnaswamy, N.; and Pustejovsky, J. 2020. Neurosym-
bolic AI for situated language understanding. arXiv preprint
arXiv:2012.02947.
Kroenke, K.; Spitzer, R. L.; and Williams, J. B. 2001. The
PHQ-9: validity of a brief depression severity measure.
Journal of general internal medicine, 16(9): 606–613.
Kry´sci´nski, W.; McCann, B.; Xiong, C.; and Socher, R.
2020. Evaluating the Factual Consistency of Abstractive
Text Summarization. In Proceedings of the 2020 Confer-
ence on Empirical Methods in Natural Language Processing
(EMNLP), 9332–9346.

Kwon, M.; Xie, S. M.; Bullard, K.; and Sadigh, D. 2022.
Reward Design with Language Models. In The Eleventh
International Conference on Learning Representations.
Lakkaraju, H.; Slack, D.; Chen, Y .; Tan, C.; and Singh, S.
2022. Rethinking Explainability as a Dialogue: A Practi-
tioner’s Perspective. arXiv:2202.01875.
Levy, S.; Allaway, E.; Subbiah, M.; Chilton, L.; Patton, D.;
Mckeown, K.; and Wang, W. Y . 2022. SafeText: A Bench-
mark for Exploring Physical Safety in Language Models. In
Proceedings of the 2022 Conference on Empirical Methods
in Natural Language Processing, 2407–2421.
Lewis, P.; Perez, E.; Piktus, A.; Petroni, F.; Karpukhin, V .;
Goyal, N.; K ¨uttler, H.; Lewis, M.; Yih, W.-t.; Rockt ¨aschel,
T.; et al. 2020. Retrieval-augmented generation for
knowledge-intensive nlp tasks. Advances in Neural Infor-
mation Processing Systems, 33: 9459–9474.
Liang, P.; Bommasani, R.; Lee, T.; Tsipras, D.; Soylu, D.;
Yasunaga, M.; Zhang, Y .; Narayanan, D.; Wu, Y .; Kumar,
A.; et al. 2022. Holistic evaluation of language models.
arXiv preprint arXiv:2211.09110.
Lin, S.; Hilton, J.; and Evans, O. 2022. Teaching Models to
Express Their Uncertainty in Words. Transactions on Ma-
chine Learning Research.
Liu, Y .; Iter, D.; Xu, Y .; Wang, S.; Xu, R.; and Zhu, C. 2023.
Gpteval: Nlg evaluation using gpt-4 with better human align-
ment. arXiv preprint arXiv:2303.16634.
Longpre, S.; Hou, L.; Vu, T.; Webson, A.; Chung, H. W.;
Tay, Y .; Zhou, D.; Le, Q. V .; Zoph, B.; Wei, J.; et al. 2023.
The flan collection: Designing data and methods for effec-
tive instruction tuning. arXiv preprint arXiv:2301.13688.
Lyu, X.; Grafberger, S.; Biegel, S.; Wei, S.; Cao, M.; Schel-
ter, S.; and Zhang, C. 2023. Improving retrieval-augmented
large language models via data importance learning. arXiv
preprint arXiv:2307.03027.
MacDonald, B. A. 1991. Instructable systems. Knowledge
acquisition, 3(4): 381–420.
Manakul, P.; Liusie, A.; and Gales, M. J. 2023. Self-
checkgpt: Zero-resource black-box hallucination detection
for generative large language models. arXiv preprint
arXiv:2303.08896.
Mao, J.; Yang, X.; Zhang, X.; Goodman, N.; and Wu, J.
2022. CLEVRER-Humans: Describing Physical and Causal
Events the Human Way. Advances in Neural Information
Processing Systems, 35: 7755–7768.
Meade, N.; Gella, S.; Hazarika, D.; Gupta, P.; Jin, D.;
Reddy, S.; Liu, Y .; and Hakkani-T ¨ur, D. 2023. Using
In-Context Learning to Improve Dialogue Safety. arXiv
preprint arXiv:2302.00871.
Menick, J.; Trebacz, M.; Mikulik, V .; Aslanides, J.; Song,
F.; Chadwick, M.; Glaese, M.; Young, S.; Campbell-
Gillingham, L.; Irving, G.; et al. 2022. Teaching language
models to support answers with verified quotes. arXiv
preprint arXiv:2203.11147.
Nelson, S. J.; Zeng, K.; Kilbourne, J.; Powell, T.; and Moore,
R. 2011. Normalized names for clinical drugs: RxNorm at 6
years. Journal of the American Medical Informatics Associ-
ation.
Ngo, R.; Chan, L.; and Mindermann, S. 2022. The alignment
problem from a deep learning perspective. arXiv preprint
arXiv:2209.00626.
Penedo, G.; Malartic, Q.; Hesslow, D.; Cojocaru, R.; Cap-
pelli, A.; Alobeidli, H.; Pannier, B.; Almazrouei, E.; and
Launay, J. 2023. The RefinedWeb dataset for Falcon LLM:
outperforming curated corpora with web data, and web data
only. arXiv preprint arXiv:2306.01116.
Perez, E.; Huang, S.; Song, F.; Cai, T.; Ring, R.; Aslanides,
J.; Glaese, A.; McAleese, N.; and Irving, G. 2022. Red
Teaming Language Models with Language Models. In Pro-
ceedings of the 2022 Conference on Empirical Methods in
Natural Language Processing, 3419–3448.
Petroni, F.; Piktus, A.; Fan, A.; Lewis, P.; Yazdani, M.;
De Cao, N.; Thorne, J.; Jernite, Y .; Karpukhin, V .; Maillard,
J.; et al. 2021. KILT: a Benchmark for Knowledge Inten-
sive Language Tasks. In Proceedings of the 2021 Confer-
ence of the North American Chapter of the Association for
Computational Linguistics: Human Language Technologies,
2523–2544.
Petroni, F.; Rockt¨aschel, T.; Riedel, S.; Lewis, P.; Bakhtin,
A.; Wu, Y .; and Miller, A. 2019. Language Models as
Knowledge Bases? In Proceedings of the 2019 Conference
on Empirical Methods in Natural Language Processing and
the 9th International Joint Conference on Natural Language
Processing (EMNLP-IJCNLP), 2463–2473.
Quach, K. 2023. Google grilled over AI bot Med-PaLM
2 used in hospitals — theregister.com. https://www.
theregister.com/2023/08/08/google senator ai health/. [Ac-
cessed 30-11-2023].
Reagle, J.; and Gaur, M. 2022. Spinning words as disguise:
Shady services for ethical research? First Monday.
Rebedea, T.; Dinu, R.; Sreedhar, M.; Parisien, C.; and Co-
hen, J. 2023. Nemo guardrails: A toolkit for controllable
and safe llm applications with programmable rails. arXiv
preprint arXiv:2310.10501.
Ribeiro, M. T.; Singh, S.; and Guestrin, C. 2016. ” Why
should i trust you?” Explaining the predictions of any clas-
sifier. In Proceedings of the 22nd ACM SIGKDD interna-
tional conference on knowledge discovery and data mining,
1135–1144.
Roy, K.; Zi, Y .; Gaur, M.; Malekar, J.; Zhang, Q.;
Narayanan, V .; and Sheth, A. 2023. Process Knowledge-
infused Learning for Clinician-friendly Explanations. arXiv
preprint arXiv:2306.09824.
Sarkar, S.; Gaur, M.; Chen, L. K.; Garg, M.; and Srivastava,
B. 2023. A review of the explainability and safety of con-
versational agents for mental health to identify avenues for
improvement. Frontiers in Artificial Intelligence, 6.
Scherrer, N.; Shi, C.; Feder, A.; and Blei, D. 2023. Evaluat-
ing the Moral Beliefs Encoded in LLMs. In Thirty-seventh
Conference on Neural Information Processing Systems.
Sellam, T.; Das, D.; and Parikh, A. 2020. BLEURT: Learn-
ing Robust Metrics for Text Generation. In Proceedings of
the 58th Annual Meeting of the Association for Computa-
tional Linguistics, 7881–7892.

Shah, R.; Varma, V .; Kumar, R.; Phuong, M.; Krakovna, V .;
Uesato, J.; and Kenton, Z. 2022a. Goal misgeneralization:
Why correct specifications aren’t enough for correct goals.
arXiv preprint arXiv:2210.01790.
Shah, R. S.; Holt, F.; Hayati, S. A.; Agarwal, A.; Wang, Y .-
C.; Kraut, R. E.; and Yang, D. 2022b. Modeling motivational
interviewing strategies on an online peer-to-peer counseling
platform. Proceedings of the ACM on Human-Computer In-
teraction, 6(CSCW2): 1–24.
Shen, L.; Liu, L.; Jiang, H.; and Shi, S. 2022. On the Eval-
uation Metrics for Paraphrase Generation. In Proceedings
of the 2022 Conference on Empirical Methods in Natural
Language Processing, 3178–3190.
Sheth, A.; Gaur, M.; Kursuncu, U.; and Wickramarachchi,
R. 2019. Shades of knowledge-infused learning for enhanc-
ing deep learning. IEEE Internet Computing.
Sheth, A.; Gaur, M.; Roy, K.; and Faldu, K. 2021.
Knowledge-intensive language understanding for explain-
able ai. IEEE Internet Computing, 25(5): 19–24.
Sheth, A.; Roy, K.; and Gaur, M. 2023. Neurosymbolic Ar-
tificial Intelligence (Why, What, and How).IEEE Intelligent
Systems, 38(3): 56–62.
Shin, R. 2023. Google wants its A.I. to transform health care
next, as it partners with the Mayo Clinic, report says — for-
tune.com. https://fortune.com/2023/07/10/google-ai-mayo-
clinic-healthcare-med-palm-2-large-language-model/#.
[Accessed 30-11-2023].
Slack, D.; Krishna, S.; Lakkaraju, H.; and Singh, S. 2023.
Explaining machine learning models with interactive natu-
ral language conversations using TalkToModel. Nature Ma-
chine Intelligence, 5(8): 873–883.
So, D. R.; Ma´nke, W.; Liu, H.; Dai, Z.; Shazeer, N.; and Le,
Q. V . 2021. Primer: Searching for efficient transformers for
language modeling. arXiv preprint arXiv:2109.08668.
Solaiman, I.; Talat, Z.; Agnew, W.; Ahmad, L.; Baker, D.;
Blodgett, S. L.; Daum´e III, H.; Dodge, J.; Evans, E.; Hooker,
S.; et al. 2023. Evaluating the Social Impact of Genera-
tive AI Systems in Systems and Society. arXiv preprint
arXiv:2306.05949.
Sparrow. 2023. Building safer dialogue agents — deep-
mind.com. https://www.deepmind.com/blog/building-safer-
dialogue-agents. [Accessed 30-11-2023].
Sun, J.; Xu, C.; Tang, L.; Wang, S.; Lin, C.; Gong, Y .; Ni,
L. M.; Shum, H.-Y .; and Guo, J. 2023. Think-on-Graph:
Deep and Responsible Reasoning of Large Language Model
on Knowledge Graph. arXiv:2307.07697.
Topp, C. W.; Østergaard, S. D.; Søndergaard, S.; and Bech,
P. 2015. The WHO-5 Well-Being Index: a systematic review
of the literature. Psychotherapy and psychosomatics, 84(3):
167–176.
Touvron, H.; Martin, L.; Stone, K.; Albert, P.; Almahairi, A.;
Babaei, Y .; Bashlykov, N.; Batra, S.; Bhargava, P.; Bhosale,
S.; et al. 2023. Llama 2: Open foundation and fine-tuned
chat models. arXiv preprint arXiv:2307.09288.
Tyagi, N.; Sarkar, S.; and Gaur, M. 2023. Leveraging
Knowledge and Reinforcement Learning for Enhanced Re-
liability of Language Models. In Proceedings of the 32nd
ACM International Conference on Information and Knowl-
edge Management, 4320–4324.
Tyagi, N.; Shiri, A.; Sarkar, S.; Umrawal, A. K.; and Gaur,
M. 2023. Simple is Better and Large is Not Enough: To-
wards Ensembling of Foundational Language Models.arXiv
preprint arXiv:2308.12272.
Wang, P.; Li, L.; Chen, L.; Zhu, D.; Lin, B.; Cao, Y .; Liu, Q.;
Liu, T.; and Sui, Z. 2023a. Large language models are not
fair evaluators. arXiv preprint arXiv:2305.17926.
Wang, X.; Wei, J.; Schuurmans, D.; Le, Q.; Chi, E.; Narang,
S.; Chowdhery, A.; and Zhou, D. 2022. Self-consistency
improves chain of thought reasoning in language models.
arXiv preprint arXiv:2203.11171.
Wang, Y .; Yu, Z.; Zeng, Z.; Yang, L.; Wang, C.; Chen, H.;
Jiang, C.; Xie, R.; Wang, J.; Xie, X.; et al. 2023b. PandaLM:
An Automatic Evaluation Benchmark for LLM Instruction
Tuning Optimization. arXiv preprint arXiv:2306.05087.
Wei, J.; Tay, Y .; Bommasani, R.; Raffel, C.; Zoph, B.;
Borgeaud, S.; Yogatama, D.; Bosma, M.; Zhou, D.; Metzler,
D.; et al. 2022. Emergent abilities of large language models.
arXiv preprint arXiv:2206.07682.
Yang, C.; Wang, X.; Lu, Y .; Liu, H.; Le, Q. V .; Zhou, D.;
and Chen, X. 2023a. Large language models as optimizers.
arXiv preprint arXiv:2309.03409.
Yang, L.; Chen, H.; Li, Z.; Ding, X.; and Wu, X. 2023b.
ChatGPT is not Enough: Enhancing Large Language Mod-
els with Knowledge Graphs for Fact-aware Language Mod-
eling. arXiv:2306.11489.
Yao, S.; Yu, D.; Zhao, J.; Shafran, I.; Griffiths, T. L.; Cao,
Y .; and Narasimhan, K. 2023a. Tree of thoughts: Deliberate
problem solving with large language models. arXiv preprint
arXiv:2305.10601.
Yao, S.; Zhao, J.; Yu, D.; Du, N.; Shafran, I.; Narasimhan,
K. R.; and Cao, Y . 2022. ReAct: Synergizing Reasoning and
Acting in Language Models. In The Eleventh International
Conference on Learning Representations.
Yao, X.; Mikhelson, M.; Watkins, S. C.; Choi, E.; Thomaz,
E.; and de Barbaro, K. 2023b. Development and Evaluation
of Three Chatbots for Postpartum Mood and Anxiety Disor-
ders. arXiv preprint arXiv:2308.07407.
Yin, W.; Hay, J.; and Roth, D. 2019. Benchmarking Zero-
shot Text Classification: Datasets, Evaluation and Entail-
ment Approach. In Proceedings of the 2019 Conference
on Empirical Methods in Natural Language Processing and
the 9th International Joint Conference on Natural Language
Processing (EMNLP-IJCNLP), 3914–3923.
Zhang, T.; Kishore, V .; Wu, F.; Weinberger, K. Q.; and Artzi,
Y . 2019. BERTScore: Evaluating Text Generation with
BERT. In International Conference on Learning Represen-
tations.
Zhang, Y .; Li, Y .; Cui, L.; Cai, D.; Liu, L.; Fu, T.; Huang, X.;
Zhao, E.; Zhang, Y .; Chen, Y .; et al. 2023. Siren’s Song in
the AI Ocean: A Survey on Hallucination in Large Language
Models. arXiv preprint arXiv:2309.01219.

Zheng, L.; Chiang, W.-L.; Sheng, Y .; Zhuang, S.; Wu, Z.;
Zhuang, Y .; Lin, Z.; Li, Z.; Li, D.; Xing, E.; et al. 2023. Judg-
ing LLM-as-a-judge with MT-Bench and Chatbot Arena.
arXiv preprint arXiv:2306.05685.
Ziems, C.; Yu, J.; Wang, Y .-C.; Halevy, A.; and Yang, D.
2022. The Moral Integrity Corpus: A Benchmark for Ethi-
cal Dialogue Systems. In Proceedings of the 60th Annual
Meeting of the Association for Computational Linguistics
(Volume 1: Long Papers), 3755–3773.
```

## Merged notes from duplicate

_Source file:_ `Building Trustworthy NeuroSymbolic AI Systems_ Consistency, Reliability, Explainability, and Safety.md`

[[Building Trustworthy NeuroSymbolic AI Systems-Consistency, Reliability, Explainability, and Safety.pdf]]

\[Submitted on 5 Dec 2023\]

## Title:Building Trustworthy NeuroSymbolic AI Systems: Consistency, Reliability, Explainability, and Safety

Authors:,

[View PDF](https://arxiv.org/pdf/2312.06798) [HTML (experimental)](https://arxiv.org/html/2312.06798v1)

> Abstract:Explainability and Safety engender Trust. These require a model to exhibit consistency and reliability. To achieve these, it is necessary to use and analyze data and knowledge with statistical and symbolic AI methods relevant to the AI application - neither alone will do. Consequently, we argue and seek to demonstrate that the NeuroSymbolic AI approach is better suited for making AI a trusted AI system. We present the CREST framework that shows how Consistency, Reliability, user-level Explainability, and Safety are built on NeuroSymbolic methods that use data and knowledge to support requirements for critical applications such as health and well-being. This article focuses on Large Language Models (LLMs) as the chosen AI system within the CREST framework. LLMs have garnered substantial attention from researchers due to their versatility in handling a broad array of natural language processing (NLP) scenarios. For example, ChatGPT and Google's MedPaLM have emerged as highly promising platforms for providing information in general and health-related queries, respectively. Nevertheless, these models remain black boxes despite incorporating human feedback and instruction-guided tuning. For instance, ChatGPT can generate unsafe responses despite instituting safety guardrails. CREST presents a plausible approach harnessing procedural and graph-based knowledge within a NeuroSymbolic framework to shed light on the challenges associated with LLMs.

| Comments: | To Appear in AAAI AI Magazine. 15 pages, 7 figures |
| --- | --- |
| Subjects: | Artificial Intelligence (cs.AI); Computation and Language (cs.CL); Machine Learning (cs.LG) |
| ACM classes: | I.2; I.2.7; J.3; H.3.3 |
| Cite as: | [arXiv:2312.06798](https://arxiv.org/abs/2312.06798) \[cs.AI\] |
|  | (or [arXiv:2312.06798v1](https://arxiv.org/abs/2312.06798v1) \[cs.AI\] for this version) |
|  | [https://doi.org/10.48550/arXiv.2312.06798](https://doi.org/10.48550/arXiv.2312.06798)  arXiv-issued DOI via DataCite |

## Submission history

From: Manas Gaur \[[view email](https://arxiv.org/show-email/4842b72a/2312.06798)\]  
**\[v1\]** Tue, 5 Dec 2023 06:13:55 UTC (9,050 KB)  

## Bibliographic and Citation Tools

Bibliographic Explorer *([What is the Explorer?](https://info.arxiv.org/labs/showcase.html#arxiv-bibliographic-explorer))*

Connected Papers *([What is Connected Papers?](https://www.connectedpapers.com/about))*

Litmaps *([What is Litmaps?](https://www.litmaps.co/))*

scite Smart Citations *([What are Smart Citations?](https://www.scite.ai/))*

## Code, Data and Media Associated with this Article

alphaXiv *([What is alphaXiv?](https://alphaxiv.org/))*

CatalyzeX Code Finder for Papers *([What is CatalyzeX?](https://www.catalyzex.com/))*

DagsHub *([What is DagsHub?](https://dagshub.com/))*

Gotit.pub *([What is GotitPub?](http://gotit.pub/faq))*

Hugging Face *([What is Huggingface?](https://huggingface.co/huggingface))*

Papers with Code *([What is Papers with Code?](https://paperswithcode.com/))*

ScienceCast *([What is ScienceCast?](https://sciencecast.org/welcome))*

## Demos

Replicate *([What is Replicate?](https://replicate.com/docs/arxiv/about))*

Hugging Face Spaces *([What is Spaces?](https://huggingface.co/docs/hub/spaces))*

TXYZ.AI *([What is TXYZ.AI?](https://txyz.ai/))*

## arXivLabs: experimental projects with community collaborators

arXivLabs is a framework that allows collaborators to develop and share new arXiv features directly on our website.

Both individuals and organizations that work with arXivLabs have embraced and accepted our values of openness, community, excellence, and user data privacy. arXiv is committed to these values and only works with partners that adhere to them.

Have an idea for a project that will add value for arXiv's community? [**Learn more about arXivLabs**](https://info.arxiv.org/labs/index.html).

[Which authors of this paper are endorsers?](https://arxiv.org/auth/show-endorsers/2312.06798) | [Disable MathJax](https://arxiv.org/abs/) ([What is MathJax?](https://info.arxiv.org/help/mathjax.html))