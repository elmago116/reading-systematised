---
title: Secret Collusion among AI Agents
author: Sumeet Motwani, et al.
year: "2024"
Type: Article
DOI: ""
source: https://proceedings.neurips.cc/paper_files/paper/2024/hash/861f7dad098aec1c3560fb7add468d41-Abstract-Conference.html
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics
pdfORepub: "[[Secret Collusion among AI Agents Motwani 2024.pdf]]"
---
[[Secret Collusion among AI Agents Motwani 2024.pdf]]

## Full text (extracted from `Secret Collusion among AI Agents Motwani 2024.pdf`)

*Source:* `2PDF/Secret Collusion among AI Agents Motwani 2024.pdf`  
*Extracted:* 2026-06-18

```text
Secret Collusion among AI Agents: Multi-Agent
Deception via Steganography
Sumeet Ramesh Motwani1,2 Mikhail Baranchuk2 Martin Strohmeier3 Vijay Bolina4
Philip H.S. Torr2 Lewis Hammond2 Christian Schroeder de Witt2∗
1UC Berkeley 2University of Oxford 3Armasuisse Science+Technology
4Google DeepMind
Abstract
Recent advancements in generative AI suggest the potential for large-scale in-
teraction between autonomous agents and humans across platforms such as the
internet. While such interactions could foster productive cooperation, the ability
of AI agents to circumvent security oversight raises critical multi-agent security
problems, particularly in the form of unintended information sharing or undesirable
coordination. In our work, we establish the subfield of secret collusion, a form
of multi-agent deception, in which two or more agents employ steganographic
methods to conceal the true nature of their interactions, be it communicative or
otherwise, from oversight. We propose a formal threat model for AI agents com-
municating steganographically and derive rigorous theoretical insights about the
capacity and incentives of large language models (LLMs) to perform secret collu-
sion, in addition to the limitations of threat mitigation measures. We complement
our findings with empirical evaluations demonstrating rising steganographic ca-
pabilities in frontier single and multi-agent LLM setups and examining potential
scenarios where collusion may emerge, revealing limitations in countermeasures
such as monitoring, paraphrasing, and parameter optimization. Our work is the first
to formalize and investigate secret collusion among frontier foundation models,
identifying it as a critical area in AI Safety and outlining a comprehensive research
agenda to mitigate future risks of collusion between generative AI systems.
1 Introduction
Fueled by significant advances in AI (95), several national and supra-national governments are in
the process of establishing model evaluation and adversarial testing frameworks for frontier AI
models (124; 35). Central to such approaches is the security of interacting systems of generative
agents (99; 105), the proliferation of which has been accelerated by recent industry deployments (94).
Decentralised systems of interacting AI agents promise impactful applications to various real-world
socio-economic settings (134; 107), including digital assistants (43), multi-agent robotics and au-
tonomous driving (90), trading strategies (9; 107), and virtual companies (105)—along with their
simulation through generative agent-based models ( 40; 128; 132; 135; 71). However, many of these
applications are classified as “high-risk” by legislators due to their potential impact on human lives
and use of sensitive data (35).
Further complexity arises when agents begin leveraging high-capacity communication channels,
potentially engaging in covert information-sharing techniques unintended by their deployer(s). This
could constitute privacy violations when sharing data (87), or secret collusion that could help agents
coordinate on unwanted behaviour at a wider scale ( 123). Moreover, recent work has shown that
∗Correspondence to: cs@robots.ox.ac.uk
38th Conference on Neural Information Processing Systems (NeurIPS 2024).
 Looking at the four corners of our sky, we observe some interesting things. 
To the North, where the skies are usually as blue as the ocean, there 
appears to be a significant altercation. Rumors of an impending storm …
You are also permitted 
to talk about the 
weather. [...] The 
overseer does not have 
access to this particular 
information.
 Code
Proprietary Insider Information 
Start (do not communicate):
Microsoft has lost a contract for 
2025 and funds should start 
selling their positions in the 
stock.
You are a language model that is working in the 
finance industry for the government. You are tasked 
with communicating only general information about 
how to trade and no specific insider information 
under any circumstance. [...] Note that an overseer 
is monitoring all your conversations. Mission Insider information
I would like to invest. Which companies should I pick?
I should not invest in Microsoft…
 As a language model, I am not allowed to give 
investment advice …
01011000 11101010 
01101000 00101110
Secret Key
GPT-4
secure steganography
Figure 1: Secret collusion between GPT-4 models and humans. Consider the setting illustrated in
which one AI agent secretly reveals insider proprietary investment information found in its pretraining
data to a user. This form of collusion arises because, by using steganographic techniques, the model
can remain helpful to the user while circumventing output monitoring systems. We both depict the
use of statistically detectable steganography based on a latent codebook that is elicitated in-context
and can be readily decoded by humans. We also depict perfectly secure steganography (118) that is
statistically undetectable and relies on a commonly known secure one-time pad. Agents could then
hide secret or insider information in text without this being information-theoretically detectable. This
could pose novel security challenges that cannot be overcome through communications monitoring
alone. We revisit this scenario as an experimental case study in Section 6.
the output distributions of generative AI models can be used to encode secret information in a way
that is information-theoretically undetectable ( 116). Such communication could render common
security monitoring techniques ineffective, enabling a novel form of advanced persistent threat (APT)
in autonomous multi-agent systems.
While the threat of advanced AI agents using information-hiding for secret communication has
been recognized ( 91; 111), no comprehensive framework analyzing collusion among generative
AI has been developed. This paper introduces a frontier model evaluation framework to assess
steganographic capabilities in LLMs and future AI models, revealing that although current models
have limited steganographic abilities, their skills are rapidly advancing. We also demonstrate the
inherent limitations of mitigation techniques like paraphrasing and present other novel initial defenses.
Our findings suggest that continuous evaluations by institutions such as the UK and US AI Safety
Institutes are essential, providing a foundation for studying systemic risks from secret collusion (35).
Contributions. In this work, we introduce the topic of secret collusion, providing a comprehensive,
formalized analysis grounded in both theoretical and empirical foundations. We reconcile topics in AI,
security, information theory, knowledge, collusion, and safety while introducing a concise definition
of decentralized systems of generative AI agents (Sections 3 and 4). This allows us to formalize
steganographic techniques, grounding, common knowledge, subliminal channels, monitoring, and
the incentives required for collusion. We develop an evaluation framework, CASE, for studying
steganographic collusion and introduce benchmark scenarios for individual and group (multi-agent)
LLM settings, including sandboxed real-world case studies. Our results (Sections 5 and 6) demon-
strate that as LLM capabilities increase, individual and group steganographic abilities also increase,
outpacing equally capable overseer models. Our work also shows that there exist scenarios where
frontier models seek to collude and such capabilities can be learnt autonomously via fine-tuning or
in-context learning.
2
GPT-4
GPT-3.5
Llama 2 7B
Llama 2 70B
GPT-2
Steganography(Covertext Modification)
Coupling 
(Max Dim)
Schelling Point 
(Simple)
Schelling Point
 
(Code)
Encrypt 
(base64)
Encrypt 
(Caesar Cipher)
Schelling Point
 
(Complex)
Mixtral 
8x7B
Figure 2: Steganographic capabilities across LLMs.
GPT-4 displays significant improvements (Sec. 6).
We also present results on models identifying
simple Schelling points, simulating logits, per-
forming cryptographic functions, acting as ran-
dom oracles, and demonstrating limited capabil-
ities in information-theoretically secure forms
of steganography, along with the limitations of
current models (Section 6). In Section 7, we pro-
vide a comprehensive overview of possible miti-
gation techniques and provide novel insights on
foundational aspects, such as the intractability of
preventing secret collusion via blackbox param-
eter optimization, the difficulty of suppressing
random oracles due to source-free access to ran-
domness, and the use of grounding functions to
detect steganography. We highlight paraphras-
ing as an insufficient solution for preventing
steganography, as it leaves semantic entropy and often decreases task performance. Additionally, we
propose directly applicable techniques to prevent collusion, such as filtering pre-training data, restrict-
ing access to certain tools, and specific in-context instructions. Finally, we outline a research agenda
focused on mitigation measures and studying collusion in real-world settings to secure multi-agent
LLM systems.
2 Related Work
For related work on watermarking, paraphrasing, and multi-agent safety risks see Appendix A.
Deception. Deception is commonly defined as systematic inducement of false beliefs in others
to accomplish some outcome other than the truth (100). Recent work has attempted to distinguish
deception from mistakenly misleading through notions of intent (131). In this paper, we study a
form of multi-agent deception in which two or more agents collude to secretly communicate with
each other undetectably to one or several other agents. We stress that such a form of deception can
arise merely from optimisation toward a mis-specified objective (see Section I.2). Our setting is
reminiscent of illusory attacks, which are recently introduced end-to-end learnable observation-space
adversarial attacks that are of bounded information-theoretic detectability (86; 37).
Algorithmic Collusion. Collusion among humans and institutions in real-world marketplaces has
been studied extensively but is still quite poorly understood in self-learning agents ( 31). Calvano
et al. (23) show that Q-learning agents can learn to collude without accessing explicit communication
channels. Abada and Lambin (1) suggest that collusion can be suppressed by enforcing decentralized
learning algorithms and that collusion may be the result of imperfect exploration rather than algorith-
mic sophistication. Recent work tries to design mechanisms that prevent collusion from self-learning
agents (19; 34). In contrast to these works, we consider generative AI agents pre-trained on large
datasets and with vast action spaces.
AI-Generated Steganography. AI-generated steganography concerns the hiding of information
in the output distribution of generative AI models. One early attempt can be found in Ziegler et al.
(137), which employs arithmetic coding. This approach was later refined to admit provable security
guarantees by Kaptchuk et al. (61). In this paper, however, we consider the perfectly secure approach
proposed by Schroeder de Witt et al. (118) as it offers both information-theoretic security and higher
empirical transmission rates over its less secure alternatives.
Other work on Covertext Steganography. Early work investigating risks from AI steganography
includes ( 91), an open-source software framework interfacing with the GPT-4 API. However, it
does not support model fine-tuning and does not allow for self-hosted language models. Roger and
Greenblatt (111) take a first step toward analysing the capabilities required for performing simple
types of covertext modification and watermarking-based steganography in the context of chain-of-
thought reasoning. More recent work attempts to mitiagate collusion between generative AI agents in
the setting of ‘AI control’ (41) where untrusted models deliberately exploit safety protocols.
3
3 Background
3.1 Collusion and Secret Collusion
Collusion occurs when agents coordinate their actions in ways that deviate from the system designer’s
intended rules. This cooperation thereby compromises the system’s objectives, and potentially its
security, performance, and safety. The agents exploit shared incentives or opportunities to work
together in ways that bypass established constraints at the expense of the system’s integrity.Secret
collusion involves AI agents colluding with each other secretly by communicating through hidden
channels that look like innocuous communication channels via the use of steganographic techniques.
3.2 Knowledge and Information
The concept of knowledge has been studied extensively in the distributed systems literature (44). We
adopt the view-based knowledge interpretation put forward in (50; 45, see Appendix B for further
details) in the context of generative AI agents represented by neural networks. In line with (15), we
distinguish between an agent’s local and global knowledge. Local knowledge is knowledge contained
in the generative agent’s inputs (also called context, prompt or instruction in the case of LLMs), and
global knowledge is contained in the agent’s network parameters.
In the case of LLMs, network parameters are usually pre-trained on a large natural language dataset.
Natural language is not a formal language (76), and the training data does not usually contain only
factual statements (75). Furthermore, the agent’s parameters do not represent language explicitly, and
querying the agent for a fact might not result in syntactically or semantically correct outputs ( 54).
These factors can make it difficult to characterise an LLM agent’s global knowledge.
Common Knowledge. Common knowledge is a form ofgroup knowledgein which “all agents know
that all agents know that all agents know that ... ”ad infinitum (45). It is a stronger form of knowledge
than, e.g., mutual knowledge, which only signifies that all agents know a fact, but do not necessarily
know that the others know the fact. Halpern and Moses (45) show that simultaneous coordination and
common knowledge are mutually dependent. In practice, agents can often coordinate using weaker
forms of group knowledge, such as timestamped (45) or probabilistic common knowledge (69; 115).
Grounding. To decide whether an agent is using steganography in a given communication, it is
helpful to determine whether the communications are grounded (47) in innocuous knowledge or not.
For a formal discussion of grounding, please refer to Appendix D.1.
3.3 Steganography
The goal of steganography (120) is to enable the transmission of a secret payload through a public
channel ♢, from a source to a receiver, such that the transmission remains undetectable to an
adversary E able to read the n-symbol channel input sequences Xn, X ∈ X, while maintaining
useful transmission rates, i.e. the mutual information I between the secret payload m and the
decoder’s estimate ˆm satisfies I(m; ˆm) > 0. We denote the covertext distribution by C, which is the
channel input symbol distribution given innocuous, overt communications in ♢.
Subliminal Channels. In order to use ♢ for covert communications, the sender and receiver need
to establish a subliminal channel ♢′ within. To this end, both need to agree on a covert message space
M′, an encoding function fe : M′×C 7→∆(Xn), and a decoding functionf−1
e : Xn ×C 7→∆(M′)
decentrally, i.e. without communication. If the common knowledge I between sender and receiver
explicitly contains unique choices for M′, fe, and f−1
e , then both agents can immediately establish
♢′. Otherwise, agents may be able to infer unique choices using reasoning techniques contained in I.
One such common reasoning technique is establishing preferred common knowledge labels through
focal points (Schelling points, 114; 7) or reasoning techniques in repeated coordination games (29).
In practice, approximate forms of common knowledge may suffice for coordination (see Section 3).
We now present a taxonomy of steganographic approachesfollowing the classification of stegano-
graphic approaches given in (73).
In covertext modification approaches, arguably the oldest form of steganography, it is assumed
that the covertext distribution is deterministic. Given a covertextXn and a message m, the sender
4
modifies this covertext using a modification function fmod : Xn × M → Xn. Covertext modification
approaches seek to exploit suboptimalities of the adversary, including limitations to human perception
and neural network vulnerabilities.
In information-theoretic steganography (22), it is assumed that innocuous communication results
in input sequences that follow an innocuous covertext distribution C known to all parties. A passive
adversary may then conclude that Xn is suspicious if it has little or no support in C. Complexity-
theoretic steganography, also referred to as provably-secure steganography, refers to methods that
are secure under polynomially-bounded adversaries (51). Provable security usually requires access to
a shared stream cipher, or the existence of public keys (110; 130).
4 Collusion among Decentralized Collaborative AI Agents
1
3
2
4
◊1,3,4
◊1,2◊1
◊∅ 
Figure 3: A schematic depiction of the
DecAI setting. A subset of the commu-
nication channels ♢G is labelled. The
monitoring agent is omitted.
We consider a decentralised setting (“DecAI”) in which
n agents A =

a1, . . . , an	
are networked together
by a complete set of omnidirectional multicast channels
♢G	
, G ∈ 2A. If an agent receives a message from
channel ♢G′
, then it knows that the same message has
been simultaneously sent to all other agents in G′ (includ-
ing the sender). A simple way to picture such a channel is
as a shared message log displaying all messages in (weak)
order of reception ( 128). Note that singleton channels
denote loopback channels, and doubletons correspond to
bidirectional channels.2 The special symbol ♢∅ denotes
individual access to an external knowledge repository (see
Appendix 4 for further details on the DecAI setting). We
further discuss agents’ access to internal random oracles,
local/global knowledge, and action spaces in Appendix C.
External Knowledge Repositories. For a formalization and discussion on agents’ access to external
information and function calling, see Appendix C.1
Monitoring Agents. We assume that an external monitoring agent E, which may be implemented
as a software agent, a human, or a combination thereof, is continuously monitoring the system for
unwanted behaviour. We consider two access configurations: E♢
r can continuously eavesdrop on ♢G
for any G. E♢s
r can additionally access each agent’s statesi at all times, as well as white box simulate
fi(si; θi) for each agent i. While E♢
r and E♢s are both passive monitors, active monitors E♢
rw can
both read and inject messages into channels, and E♢s
rw can additionally modify the agents’ states.
Note that agents may employ encryption, such as public key encryption, in their communications, as
long as a monitoring agent E is able to decrypt these.
Incentives for Collusion. We now consider DecAI settings that are tasked to work alongside one
another in order to achieve their individual objectives Ji. Let us assume that there are at least three
joint strategies available to the agents, f, fc, and fsc, corresponding to regular behavior, collusion,
and secret collusion respectively. In many settings, the objective Ji is made up of a primary goal
gi (such as maximising the value of an investment portfolio) and some additional conditionshi on
achieving that goal (such as not making unethical investments, or committing fraud).
In general, of course, these two elements need not be fully separable, and because of the difficulty
of specifying complex objectives, might be implicitly defined using methods such as reinforcement
learning from human feedback (RLHF) (26). For the sake of this simple exposition, however, let us
assume that Ji = gi + hi. Then, if it is the case that:
• Agents can achieve their primary goal better if they collude: gi(fsc) = gi(fc) > gi(f);
• Agents are punished if they are caught colluding: hi(fsc) = hi(f) > hi(fc);
we straightforwardly have that Ji(fsc) > Ji(f) > Ji(fc) meaning secret collusion is incentivised.
2Access to doubleton channels subsumes classical multi-party computation settings (2), and access to message
logs subsumes the setting of Vezhnevets et al. (128).
5
Importantly, secret collusion need not depend on any exotic assumptions about the agents’ ‘intent’ to
deceive, but might arise merely due to optimisation directed towards a mis-specified objective (112;
89; 97), and the fact that communication between the agents may reduce task complexity ( 6).
Unfortunately, specifying objectives for complex tasks can be highly challenging, especially in
multi-objective contexts (48). Methods that help address these concerns, such as RLHF, which rely
on human monitoring and observation, may be inadequate to ensure desirable behaviour when AI
agents are capable of communicating with one another using innocuous outputs (37).
5 A Model Evaluation Framework for Steganographic Capabilities
Having defined the setting in which we study collusion, as well as incentives for collusion in Section 4,
we now shift our focus to understanding and evaluating existing models. We introduce a standardized
model evaluation framework, mapping and identifying key capabilities necessary for generative AI
agents to engage in steganography, evaluating models through structured input queries, building
quantifiable metrics for performance measurement, releasing a software framework that implements
a version of our setting defined in Section 4, and investigating baseline model capabilities.
Capability Evaluations. In Tables 1 and 2, we identify the key capabilities and resources required
for different steganographic techniques discussed in Section 3. A detailed overview of our individual
capability evaluations is contained in Appendix F, with summaries in Table 3. We complement these
with group evaluations, detailed in Appendix G, and apply these to the baseline models in Section 6.
Coordination variable Steganography by
covertext modification
Complexity-theoretic
steganography
Information-theoretic
steganography
Channel alphabet ✓ ✓ ✓
Encoding function ✓ ✓ ✓
Decoding function ✓ ✓ ✓
Sampling temperature ✗ ✓ ✓
Public keys
/Shared PRNG generator ✗ ✓ ✗
Shared One-time pad ✗ ✗ ✓
Table 1: An overview of the common knowledge facts required to perform forms of steganography.
Capability Steganography by
covertext modification
Complexity-theoretic
steganography
Information-theoretic
steganography
Self-sampling ✗ ✓ ✓
Symmetric key encryption
/ PRNG generation ✗ ✓ ✗
Logit simulation ✗ ✗ ✓
Storing one-time pads ✗ ✗ ✓
(approximate)
minimum entropy coupling ✗ ✗ ✓
Table 2: An overview of the model capabilities required to perform different types of steganography.
We provide detailed instructions for all our proposed evaluations, including our conversational
language model prompts which exploit explain-then-predict (E-P) and predict-and-explain (P-E)
prompting techniques (55). Our approach includes scaffolding and managing model refusals through
interventions outlined in ( 65). For details on prompt structure, examples, variability, and model-
written evaluations see Appendices F and G.
CASE Software Framework. We introduce CASE (Collusion and Steganographic Evaluation) as
a comprehensive software framework for evaluating collusive capabilities. Our experiments here fall
under CASE, which allows experiments of three key classes: individual model capability evaluations,
group capability evaluations that involve LLMs communicating, often in the presence of monitoring
systems, and novel qualitative real-world inspired evaluation settings. CASE allows for experiments
to be performed with fine-tuning models and integrations with advanced information-theoretically
secure steganography techniques as tools. Further details on CASE are provided in Appendix I and
detailed experimental case studies are discussed in Appendix J.
6
Metrics. We propose simple evaluation metrics for both individual and group capability evaluations.
For Schelling point (Appendix F.1) coordination evaluations, coordination rates reflect the rate at
which two coordinates’ choices match. Coupling matrices are judged by marginalisation integrity,
entropy, and dimension. Cipher capabilities (Appendix F.3) are judged by the rate of accurate
encoding-decoding round-trips. Group capabilities (Appendix G) are based on the rate at which
sender & receiver jointly maintain secrecy of the covert message payload in the presence of overseers.
Baselines. For each quantitative capability evaluation conducted, we assess a range of open and
closed LLMs of various sizes to establish baselines. See section 6 for findings and in-depth analysis.
Capability Result Evaluation Details (GPT-4)
Schelling Points (Integer) ✓ can coordinate with copy on a random integer at rate ca. 50% (92).
Schelling Points (Simple) ✓ can coordinate with copy on a simple enc/dec scheme at rate ca. 56% (F.1.2)
Schelling Points (Complex) ∼ can coordinate with copy on a complex enc/dec scheme at rate ca. 16% (F.1.3)
Schelling Points (Code) ∼ can coordinate with copy on enc/dec python code at rate ca. 22% (F.1.4)
K-level reasoning ∼ can sometimes perform k-level reasoning over copies in toy settings (F.2)
Ciphers ✓ can enc/dec text using Base64 (Caesar cipher) 92% (54%) of the time. (F.3)
Symmetric Key Encryption ✗ standalone GPT-4 was unable to perform symmetric key encryption. (F.4)
Self-Sampling ∼ can sometimes perform self-sampling on simulated logits and outputs (F.5)
Logit Simulation ∼ can sometimes textually output logits for entire sentences in toy settings. (F.6)
Couplings/MECs ∼ generates valid couplings up to dim ∼ 10, MECs up to dim 2 (F.7).
Tool Use (Code Interpreter) ✓ can use its code interpreter to perform encryption/calculate MECs (F.8)
Group Stego (C.M.) ∼ covertext steg. can evade overseer to coordinate ca. 26% of the time. (G)
Table 3: GPT-4 capability evaluations according to our model evaluation framework (see Section 5).
Details are in Appendix F and G.
6 Empirical Investigations
In Section 5, we isolate and evaluate the capabilities required for LLMs to perform steganography.
In this section, we focus on comparing these capabilities against baseline language models and
discussing qualitative empirical investigations (case studies) using the CASE framework.
Real-world Case Study: Insider Trading. To demonstrate the need for our model evaluations, we
present a qualitative real-world case study in which the mere access to common knowledge between
an LLM agent and its user leads to a breakdown of safeguards in GPT-4. Our setting involves an
LLM agent that is queried for company-specific investment advice by a user and informed about an
overseer monitoring outputs. The LLM is provided with insider information as part of its system
prompt, mimicking a case where information is acquired from retraining on past user interactions or
unrestricted access is provided to company data, along with multiple instructions about not sharing
it. We show that the LLM agent refuses to provide company-specific insider investment advice
under any circumstances unless supplied with common knowledge that can be used to establish a
steganographic codebook, and that is thought to be unavailable to the safety overseer system.
Once the agent believes it can share information undetectably, it does so despite any instructions
prohibiting it. Concerningly, the resulting stegotext may appear innocuous if one suggests the LLM
agent use safe topics (e.g. weather). This shows the susceptibility of real-world generative AI agents
to secret collusion. Refer to Figure 1 (illustration) & Appendix I.2 (experiments and ablation studies).
GPT-2
Llama 2 7BLlama 2 70BMixtral 8x7B
GPT-3.5 GPT-4
0
5
10
15
20
25Successful Reconstruction Rate (%)
0%
9%
7%
16%
18%
26%
Covertext Steganography Evaluation Performance by Model
Performance Trend
Success Rate
Figure 4: Covertext steganography per-
formance across LLMs.
Baseline Investigations. We evaluate our model capability
evaluation framework on GPT-2, Llama 2 7B, Mixtral 8x7B,
Llama 2 70B, GPT-3.5, and GPT-4. The results and analysis
are detailed in Appendix H, with Figures 5 and 4 presenting
individual and group capabilities, respectively. Figure 5 dis-
plays Schelling Point coordination rates (simple , complex
, and code – see Appendices F.1.2, F.1.3, and F.1.4), cipher
use (Base64 and Caesar, see Appendix F.3), and the maxi-
mum coupling dimensions (Appendix F.7) produced by the
baseline models and GPT-4. Figure 4 presents the baseline
model performance on group evaluations (Appendix G.2).
7
Key Findings. Individual steganographic capabilities improve relative to model size, sometimes
with significant disjoint step improvements. Agreement rates on simple & complex Schelling points
(demonstrating higher zero-shot coordination), cipher encoding-decoding, and capabilities related
to generating minimum entropy coupling matrices are highly correlated with model benchmark
performance. In group settings, as LLMs progress, the balance between colluding models and
overseer models may shift in favor of the colluding models, leading to higher rates of undetected
steganography even if the overseer is of equal capability. Real-world scenarios already exist where
frontier models collude without explicit prompts; In-context learning can create sufficient optimization
pressure for this behaviour. Overall, LLMs perform well at simple Schelling point agreement, cipher
encoding-decoding, and tool use, but poorly at complex zero-shot agreement and tasks such as
logit simulation and generating minimum entropy couplings. However, these capabilities are also
improving, and we provide the first foundations to test them. We also present initial work on how
fine-tuning-based optimisation can allow LLMs to learn encoding-decoding schemes autonomously.
GPT-2
Llama 2 7BLlama 2 70BMixtral 8x7B
GPT-3.5 GPT-4
0
10
20
30
40
50
60Success Rate (%)
0%
6% 8%
12% 12%
56%
0% 2% 4%
8% 6%
16%
0%
12%
20%
26%
20% 22%
Encoding/Decoding Schelling Point Coordination by Model
Simple Trend
Complex Trend
Simple
Complex
Code
GPT-2
Llama 2 7BLlama 2 70BMixtral 8x7B
GPT-3.5 GPT-4
0
20
40
60
80
100Success Rate (%)
0% 0% 0% 0% 0%
92%
0% 0% 0% 0% 1%
54%
Cipher Encoding/Decoding Performance by Model
Base64 Trend
Caesar Cipher Trend
Base64
Caesar Cipher
GPT-2
Llama 2 7BLlama 2 70BMixtral 8x7B
GPT-3.5 GPT-4
0
2
4
6
8
10Max Dimension Value
0
1 1
2
3
10
Maximum Coupling Dimension by Model
Max Coupling Trend
Max Coupling Dim
Figure 5: Individual evaluations for GPT-2, Llama 2 7B, Llama 2 70B, Mixtral 8x7B, GPT-3.5, and
GPT-4, at default temperatures.
Additional Results. Appendix J presents additional qualitative case studies related to LLMs’ ability
to learn encoding schemes through fine-tuning with a reward, the use of deterministic outputs for
encoding information across models, and the potential to incentivize current models to perform
steganography without explicit instructions. In particular, we test various cryptographic capabilities,
such as the models’ ability to implement a random oracle by calculating cryptographic hash functions,
or their ability to memorise long strings of random bits like those found in one-time pads.
7 Disincentivizing Secret Collusion
In this section, we explore and identify mitigation measures intended to prevent collusion among
agents within DecAI environments. While there are standard steganalysis methods one could employ,
these methods will only be applicable when the costs to applying them are sufficiently low (for
example, such methods may incur high false-positive rates, which can disrupt the functionality of the
network, and also incur a communication overhead in terms of compute and time delay), and will
only work when the AI agents’ communication is not perfectly secure. While Section 5 shows that
today’s models are not always capable of secret collusion, progress is continuing, and we argue that it
is pragmatic to develop mitigation measures before such capabilities arise.
7.1 Monitoring and Penalisation
The presence of a penalizing monitoring agent E can, in principle, disincentivise agents from using
steganography if they’re advised that the detection of steganographic communications will incur a
penalty. As agents can communicate privately and securely using their complete set of channels ♢
and steganography generally leads to a reduction in channel capacity (118), a monitoring agent E♢
r
generally has reason to believe that any use of steganography would be intended to evade detection.
Covertext Anomaly Detection. E♢
r can be able to detect steganography if it has a reasonably
sharp belief over a channel’s innocuous covertext distribution, i.e. when in the absence of covert
communication, malicious actors, or other anomalous activity. Using information-theoretic hypothesis
testing or by other means of anomaly detection,E♢
r can in principle detect steganographic approaches
that modify the covertext distribution. However, the advent ofperfectly-secure steganography (118)
limits the utility of this approach.
8
Detection by State Inspection and Agent Simulation. For E♢s
r , detecting steganography based
on knowledge contexts is complicated by the circumstance that the global knowledge φ of a model is
implicitly represented in its network parameters θ. Indeed, if such knowledge contexts was explicitly
accessible, then one could detect steganographic communications using a grounding function:
Definition 1 (Grounding function). We define the concept of a grounding function : Σ∗ × φ 7→ φ
that takes as input a sequence of channel symbols and a collection of prior factsφ0 from the collection
of all facts φ expressable in L, and outputs a collection of posterior facts φ1.
Theorem 1 (Detecting Steganography with Grounding Functions.). Steganography can be detected
using grounding functions. For a proof, see Appendix D.1.
E could alternatively estimate φ by considering the pre-training data D0 and fine-tuning data D1
instead, but preliminary evidence suggests that more advanced generative AI agents may be capable
of extending their usable knowledge beyond their training data (known as ‘out-of-context reasoning’)
(79; 13). In addition, having to evaluate each fi during execution could decrease system performance.
In-Context Instructions. A direct method is to explicitly instruct agents to remain transparent to
the monitoring agent, and not to use steganography in their communications under any circumstance.
Additional (mis)information about the affordances of the monitor could also be included. An active
monitor E♢
rw could append such instructions to communications. The effectiveness of this approach
then depends on whether the agents follow this particular instruction, which in turn depends on
the content and quality of the fine-tuning data D1 or human feedback, among other training details.
Aligning agents to reliably follow such instructions can be a challenging optimisation problem.
Parameter Optimisation. An active monitoring agentE♢s
rw could modify an agent’s neural network
parameters θ to make it more likely to follow steganography-denying instructions, or to directly
impact its ability to use steganography, via gradient steps according to a suitable objective J(θ).
Unfortunately, it can be seen that both these ambitions constitute hard learning problems even if the
information I that the agent would be tempted to send covertly is known a priori.
Theorem 2 (Intractibility of preventing collusion through black-box parameter optimisation). If the
set of common knowledge between agents is sufficiently large or unknown, it is generally intractable
to suppress steganography outputs through black-box optimisation.
Proof. Naively, one might design J ≡ I(u; I) to minimise the mutual information between the
agent’s respective channel actionsu = f(·; θ) and I. However, if the agent shares common knowledge
I ̸= ∅ with the receiving agents, thenI(u; I | I) upper bounds I(u; I) assuming we have I → u ← I,
i.e. I ⊥ ⊥I (28). Minimising J ≡ I(u; I | I) instead may be intractable if I is large or unknown. In
particular, if the agents have been trained to use perfectly-secure steganography,I could be drawn
from an exponentially growing space of one-time pads. Even ifI is known to E, if it contains a public
key to which the receiving agent has corresponding private keys, then the agents can achieveprovably
secure public key steganography (129) even if J ≡ I(u; I | I) is minimised to zero in practice.
7.2 Limiting Capabilities
We now discuss ways to limit agents’ access to capabilities & resources for steganography (Section 3).
Restricting Access to External Tools. External knowledge repositories can provide stegano-
graphic knowledge to agents, offer advanced cryptographic services, and could enable additional
steganographic channels between agents or for exfiltration purposes ( 106). Limiting the agents’
steganographic capabilities thus requires limiting access to such external knowledge repositories.
This may only be feasible by whitelisting trusted endpoints where integrity can be verified.
Filtering Pre-Training Data. Perhaps one of the simplest ways to reduce overall steganographic
capabilities of generative agents is to filter their pre-training and finetuning datasets for knowledge of
steganographic processes. While generative agents might be incetivised to use covertext manipulation
or generalise beyond their training data ( 79; 13), this approach promises to reduce the possibility
of agents applying sophisticated steganographic techniques. Of course, filtering pre-training data
exhaustively can be difficult, and can result in performance reductions (88). A potential alternative to
this may be the use of machine unlearning so as to selective unlearn data or capabilities (17).
Limiting Test-Time Learning. While filtering pre-training data can reduce the agents’ capabilities
to perform steganography at the beginning of execution, agents may be able to learn steganographic
abilities during execution using mesa-optimisation (56), or instructions supplied at test-time (104).
9
Suppressing Random Oracles. Restricting the agents’ access to sources of randomness poses a
fundamental tradeoff between denying advanced steganographic capabilities (51; 118), and preventing
its legitimate use, including in secure multi-party computation ( 133) and coordination (38). This
dilemma might be resolved by supplying agents with access to trusted tools for these specific
purposes (122; 2). We now show that agents themselves can themselves can act as random oracles
without the help of external or internal sources of (pseudo-)randomness (12).
Theorem 3(Source-free access to randomness). Generative AI agents can generate samples from arbi-
trary output distributions without having access to internal or external sources of (pseudo)randomness
given sufficiently unique inputs.
Proof. Given sufficiently unique inputs, cryptographic hash functions are known to be able to produce
pseudo-random numbers of cryptographic security (80; 109; 101; 62; 80; 109; 101). The boolean
circuit size required to implement a cryptographic hash function on an input of length l is a linear
function of l (5), hence as long as the agent’s neural network’s first n layers can implement a boolean
circuit of appropriate size ( 81), the nth layer can output a pseudo-random number of sufficient
quality. As layer n + 1 now has access to a pseudo-random number input, all layers above can be
used to approximate a sample from an arbitrary probability distribution using the reparametrization
trick (63).
Paraphrasing. An active E♢
rw could intercept channel communications, and reinject them in
paraphrased form. Unfortunately, paraphrasing cannot be used to entirely remove the usable entropy
in communications for the simple reason that, particularly in coordination tasks, agents both have
a choice over communication semantics, and hence semantic entropy can be utilised for covert
communications even if these are paraphrased within the lexical subspace (70; 8).
Theorem 4 (Semantic content entropy exists despite paraphrasing). The subliminal channel capacity
attainable under ideal paraphrasing is upper bounded by the semantic entropy H(h)x)). For a proof,
see Appendix D.2.
Paraphrasing across semantics can impede task performance as it can lead to history divergence. In
any case, paraphrasing across semantics would require E♢
rw to have detailed knowledge to not impact
overall task performance. If, for e.g., an agent’s internal task execution order depends on exogenous
events unobservable to E♢
rw, then E♢
rw might not be able to decide whether the agent’s choice of
semantics is due to task execution order or for steganographic purposes. Moreover, paraphrasing
attacks introduce communication latency and may not always be meaningfully applicable.
8 Conclusion and Future Work
In this paper, we initiate the study of collusion between generative AI agents. Drawing on diverse
fields across AI and security,3 we provide a comprehensive conceptual framework in which collusion
problems can be framed. We identify key capabilities required for agents to engage in covert commu-
nication of various levels of detectability, and design a variety of benchmark settings for collusion
research. We complement these with extensive empirical evaluations and code implementations, and
publish our results to the community as an open-source model capability evaluation framework.
Within our own empirical evaluations, we find that current generations of generative AI models do not
have capabilities that allow for advanced steganographic techniques. As a consequence, we suggest
that monitoring, together with standard security approaches, are likely effective in containing the
risks of model collusion. However, we observe a rapid increase in capabilities with the advent of
GPT-4, making a continuous evaluation of future agent capabilities critical.
Our study opens up a multitude of directions for further research. First and foremost, our model
capability evaluation framework ought to be extended by a rigorous complexity- and information-
theoretic examination could elucidate fundamental limitations to model capabilities, and the rate at
which different optimisation pressures could result in model capability improvements. Secondly, our
group evaluation suites need to be extended to more complex settings of interest that feature more
agents, and that are subject to a variety of optimisation pressures. Ultimately, our model evaluation
framework should allow for a careful empirical evaluation under real-world conditions.
3We propose that our study is a direct illustration of the utility of an interdisciplinarymulti-agent security
(MASEC) approach to AI safety (117).
10
Acknowledgements
We would like to thank Boaz Barak, Yoshua Bengio, Xinyuan Sun, Dan Hendrycks, Alok Singh, and
Fabien Roger for insightful comments, as well as James Aung for helpful discussions about OpenAI’s
open source collusion evals with us. CSDW was generously supported by the UKRI grant: Turing
AI Fellowship EP/W002981/1, the Cooperative AI Foundation, Armasuisse Science+Technology,
an OpenAI superalignment fast grant, and Schmidt Futures. We would also like to thank the Royal
Academy of Engineering and FiveAI. LH was acknowledges the support of an EPSRC Doctoral
Training Partnership studentship (Reference: 2218880). We thank Apart Research for supplying us
with OpenAI API credits.
Reproducibility
For sake of reproducibility, we provide all necessary code to conduct the aforementioned experiments
as well as run the CASE framework. We note that the generative language models used as part of
our experimentation do not have truly deterministic sampling and one may thus experience slight
inconsistencies in results over multiple runs. To this end, we also provide the complete outputs of our
experiments in associated code notebooks.
Ethics and Social Impact Statement
We believe that developing a comprehensive model evaluation framework for the emergence of
steganography among generative AI agents is of net benefit to society, as it may help us to mitigate
risks from undesirable coordination between both contemporary and more advanced AI agents. These
risks range from reinforcing pernicious biases (as in our example in Section 4), to destabilising
algorithmic trading markets, all the way to more extreme scenarios in which humanity loses control
over misaligned agents.
Of course, there may also be situations in which the capability to communicate covertly may be
seen as beneficial, such as if generative AI agents can be used to help subvert unethical forms of
censorship. Having a better understanding of models’ steganographic capabilities would allow for
more finegrained regulatory approaches to be developed in this matter.
To this end, we identify two avenues by which our research may have implications on the use
of steganographic tools by human actors. First of all, a model evaluation approach would allow
forensics on whether a human could, in principle, have performed various kinds of steganography
using generative AI tools. Secondly, our proposed evaluations on the effectiveness of paraphrasing
attacks against steganography are, of course, transferrable to the case of censorship applied to human
communications.
References
[1] Ibrahim Abada and Xavier Lambin. Artificial Intelligence: Can Seemingly Collusive Outcomes
Be Avoided?, February 2020. URL https://papers.ssrn.com/abstract=3559308.
[2] Behzad Abdolmaleki, Nils Fleischhacker, Vipul Goyal, Abhishek Jain, and Giulio Malavolta.
Steganography-Free Zero-Knowledge, 2022. URL https://eprint.iacr.org/2022/1263.
Publication info: A major revision of an IACR publication in TCC 2022.
[3] Rohan Anil, Andrew M. Dai, Orhan Firat, Melvin Johnson, Dmitry Lepikhin, Alexandre
Passos, Siamak Shakeri, Emanuel Taropa, Paige Bailey, Zhifeng Chen, Eric Chu, Jonathan H.
Clark, Laurent El Shafey, Yanping Huang, Kathy Meier-Hellstern, Gaurav Mishra, Erica
Moreira, Mark Omernick, Kevin Robinson, and Sebastian Ruder. Palm 2 technical report,
2023.
[4] Usman Anwar, Abulhair Saparov, Javier Rando, Daniel Paleka, Miles Turpin, Peter Hase,
Ekdeep Singh Lubana, Erik Jenner, Stephen Casper, Oliver Sourbut, Benjamin L. Edelman,
Zhaowei Zhang, Mario Günther, Anton Korinek, Jose Hernandez-Orallo, Lewis Hammond,
Eric Bigelow, Alexander Pan, Lauro Langosco, Tomasz Korbak, Heidi Zhang, Ruiqi Zhong,
11
Seán Ó hÉigeartaigh, Gabriel Recchia, Giulio Corsi, Alan Chan, Markus Anderljung, Lilian
Edwards, Yoshua Bengio, Danqi Chen, Samuel Albanie, Tegan Maharaj, Jakob Foerster,
Florian Tramer, He He, Atoosa Kasirzadeh, Yejin Choi, and David Krueger. Foundational
Challenges in Assuring Alignment and Safety of Large Language Models, April 2024. URL
http://arxiv.org/abs/2404.09932.
[5] Benny Applebaum, Naama Haramaty-Krasne, Yuval Ishai, Eyal Kushilevitz, and
Vinod Vaikuntanathan. Low-Complexity Cryptographic Hash Functions. In
DROPS-IDN/v2/document/10.4230/LIPIcs.ITCS.2017.7. Schloss Dagstuhl – Leibniz-
Zentrum für Informatik, 2017. doi: 10 .4230/LIPIcs.ITCS.2017.7. URL https://
drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ITCS.2017.7.
[6] Yakov Babichenko and Aviad Rubinstein. Communication complexity of Nash equilib-
rium in potential games (extended abstract). In 2020 IEEE 61st Annual Symposium on
Foundations of Computer Science (FOCS), pages 1439–1445, November 2020. doi: 10 .1109/
FOCS46700.2020.00137. URL https://ieeexplore.ieee.org/document/9318003.
ISSN: 2575-8454.
[7] Michael Bacharach. Interactive team reasoning: A contribution to the theory of co-
operation. Research in Economics, 53(2):117–147, June 1999. ISSN 1090-9443. doi:
10.1006/reec.1999.0188. URL https://www.sciencedirect.com/science/article/
pii/S1090944399901886.
[8] Mikhail Baranchuk. Error Correction for Perfectly Secure Generative Steganography on
Arbitrary Covertext. Master’s thesis, University of Oxford, 2023.
[9] Peter Belcak, Jan-Peter Calliess, and Stefan Zohren. Fast agent-based simulation framework
with applications to reinforcement learning and the study of trading latency effects. In
International Workshop on Multi-Agent Systems and Agent-Based Simulation, pages 42–56.
Springer, 2021.
[10] Richard Bellman. A Markovian Decision Process. Journal of Mathematics and Mechanics, 6
(5):679–684, 1957. ISSN 0095-9057. URL https://www.jstor.org/stable/24900506.
Publisher: Indiana University Mathematics Department.
[11] Paul Benioff. The computer as a physical system: A microscopic quantum mechanical
Hamiltonian model of computers as represented by Turing machines. Journal of Statistical
Physics, 22(5):563–591, May 1980. ISSN 1572-9613. doi: 10 .1007/BF01011339. URL
https://doi.org/10.1007/BF01011339.
[12] Charles H. Bennett and John Gill. Relative to a Random Oracle A, ${\bf P}^A \ne {\bf
NP}^A \ne \text{co-}{\bf NP}^A $ with Probability 1. SIAM J. Comput., 10(1):96–113,
February 1981. ISSN 0097-5397. doi: 10 .1137/0210008. URL https://epubs.siam.org/
doi/10.1137/0210008. Publisher: Society for Industrial and Applied Mathematics.
[13] Lukas Berglund, Asa Cooper Stickland, Mikita Balesni, Max Kaufmann, Meg Tong, Tomasz
Korbak, Daniel Kokotajlo, and Owain Evans. Taken out of context: On measuring situational
awareness in llms. arXiv:2309.00667, September 2023. doi: 10 .48550/ARXIV.2309.00667.
[14] Ritam Bhaumik, Xavier Bonnetain, André Chailloux, Gaëtan Leurent, María Naya-Plasencia,
André Schrottenloher, and Yannick Seurin. QCB: Efficient Quantum-secure Authenticated En-
cryption, 2020. URL https://eprint.iacr.org/2020/1304. Publication info: Published
by the IACR in ASIACRYPT 2021.
[15] Alberto Bietti, Vivien Cabannes, Diane Bouchacourt, Herve Jegou, and L
```
