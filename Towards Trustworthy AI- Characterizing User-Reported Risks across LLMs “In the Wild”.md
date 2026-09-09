---
title: Characterizing User-Reported Risks across LLM Chatbots
year: "2026"
Type: Proceedings Article
DOI: 10.1145/3772318.3791505
source: https://doi.org/10.1145/3772318.3791505
created: 2026-04-24
description: "'Abstract page for arXiv paper 2509.08912: Towards Trustworthy AI: Characterizing User-Reported Risks across LLMs \"In the Wild\"'"
tags:
  - op/acc/pending-review
  - tech/Ai/LLM
  - themes/ethics
  - themes/bias/algorithmic
  - Tech/AI
pdfORepub: "[[Towards Trustworthy AI- Characterizing User-Reported Risks across LLMs “In the Wild”.pdf]]"
author: "[[Lingyao Li]],[[Renkai Ma]],[[Zhaoqian Xue]],[[Junjie Xiong]]"
---

[[Towards Trustworthy AI- Characterizing User-Reported Risks across LLMs “In the Wild”.pdf]]
## Full text (extracted from `Towards Trustworthy AI- Characterizing User-Reported Risks across LLMs “In the Wild”.pdf`)

*Source:* `2PDF/Towards Trustworthy AI- Characterizing User-Reported Risks across LLMs “In the Wild”.pdf`  
*Extracted:* 2026-04-24

```text
Towards Trustworthy AI: Characterizing User-Reported Risks
across LLMs “In the Wild”
Lingyao Li∗
lingyaol@usf.edu
University of South Florida
Tampa, USA
Renkai Ma∗
renkai.ma@uc.edu
University of Cincinnati
Cincinnati, USA
Zhaoqian Xue
xuezha@pennmedicine.upenn.edu
University of Pennsylvania
Philadelphia, USA
Junjie Xiong
junjiexiong@mst.edu
Missouri University of
Science and Technology
Rolla, USA
Abstract
While Large Language Models (LLMs) are rapidly integrating into
daily life, research on their risks often remains lab-based and dis-
connected from the problems users encounter “in the wild. ” While
recent HCI research has begun to explore these user-facing risks,
it typically concentrates on a singular LLM chatbot like ChatGPT
or an isolated risk like privacy. To gain a holistic understanding of
multi-risk across LLM chatbots, we analyze online discussions on
Reddit around seven major LLM chatbots through the U.S. NIST’s
AI Risk Management Framework. We find that user-reported risks
are unevenly distributed and platform-specific. While “Valid and
Reliable” risk is the most frequently mentioned, each product also
exhibits a unique “risk fingerprint;” for instance, user discussions
associate GPT more with “Safe” and “Fair” issues, Gemini with “Pri-
vacy, ” and Claude with “Secure and Resilient” risks. Furthermore,
the nature of these risks differs by their prevalence: less frequent
risks like “Explainability” and “Privacy” manifest as nuanced user
trade-offs, more common ones like “Fairness” are experienced as
direct personal harms. Our findings reveal gaps between risks re-
ported by system-centered studies and by users, highlighting the
need for user-centered approaches that support users in their daily
use of LLM chatbots.
CCS Concepts
•Human-centered computing→Empirical studies in HCI.
Keywords
LLMs, Trustworthy AI, User-reported Risks, Knowledge Graph
1 INTRODUCTION
Large Language Model (LLM), such as OpenAI’s ChatGPT, Google’s
Gemini, and Anthropic’s Claude, are rapidly becoming integrated
into everyday life [24]. According to OpenAI COO Brad Lightcap,
ChatGPT alone now has seen over 400 million weekly users [82].
From developers debugging code and writers drafting articles to in-
dividuals seeking information and creating content, these tools have
moved well beyond research settings [22, 75, 88]. Their widespread
adoption marks a fundamental shift in user experience, where LLM-
based conversational agents function as collaborators, assistants,
or information brokers [50, 93, 98].
While the benefits of LLMs are various [63, 102, 108], prior work
has also well documented their risks from a system-centered view.
These include generating toxic content [36], “hallucinating” non-
factual information [ 48], creating societal biases related to race
∗Both authors contribute equally to this research, and both are corresponding authors.
and gender [12, 34, 57, 59], and security vulnerabilities to adver-
sarial attacks like prompt injection [84, 99] and data poisoning [7].
However, much prior work has been conducted in controlled and
laboratory-like environments that may fail to capture the unantici-
pated ways in which risks emerge during the everyday use phase
of LLMs. Furthermore, researcher-defined risks of LLMs may not
align with what users perceive as risky.
User-facing risks range from user privacy concerns [47] to bi-
ased recommendations in high-stakes domains like healthcare [87].
As LLMs become integral to public use, recent HCI research has
begun to investigate key facets of user experience such as model
satisfaction [53], trust formation [50, 85], and the trade-offs users
face between privacy and utility [106]. However, this line of work
has often focused on singular risks like trust and privacy or on a
single LLM chatbot, most of the time, ChatGPT. This creates an
opportunity to develop a more holistic understanding of the risks
in user experience across different LLM chatbots, especially given
the increased daily use of multiple chatbots like Gemini, Deepseek,
and Claude [30, 80]. To address this gap, we adopt a user-centered
approach grounded in large-scale public discourse from Reddit.
Specifically, we ask:
• RQ1. How can user-reported risks for major LLM chatbots
be categorized, and what is the prevalence of each risk type
across those chatbots?
• RQ2. What are users’ lived experiences of navigating these
prevalent risks of different LLM chatbots?
To answer these questions, we first adopt the U.S. National Insti-
tute of Standards and Technology (NIST)’s AI Risk Management
Framework (ARF) [5] to bring structure to the diverse spectrum
of user-experienced risks. We use this framework as a lens and
knowledge graph techniques to analyze large-scale online discus-
sions from Reddit, a well-established HCI method for understanding
users’ experiences with digital technologies through online data
(e.g., [20, 70, 105]). We find that while performance failures under
“Valid and Reliable” are the most frequent user-reported risk, each
LLM chatbot exhibits a distinct “risk fingerprint” with secondary
concerns such as safety, privacy, or security (RQ1). We further find
that the lived experience of these risks varies, with less frequent
risks manifesting as user trade-offs and more common ones experi-
enced as direct, personal harms (RQ2). We discuss the disconnect
between system-centered and user-centered risk perspectives, how
these manifest across different LLM chatbots, and the trade-offs
users make. Finally, we offer design and policy implications that
argue for a truly user-centered model of AI risk management, one
grounded in an understanding of users’ lived experiences.
arXiv:2509.08912v1  [cs.CY]  10 Sep 2025

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
Our study makes three main contributions. First, we provide a
large-scale, empirical characterization of the user-reported risks
across seven major closed- and open-source LLM chatbots, reveal-
ing distinct patterns of the risks. Second, we identify three types
of trade-offs that users make to navigate these risks in exchange
for LLM chatbot utilities, offering a new lens to understand the
lived experience of using these chatbots. Finally, we suggest impli-
cations for designers and policymakers who advocate for a shift
from purely technical risk mitigation to a user-centered approach
that supports users in their daily use of LLM chatbots.
2 RELATED WORK
This section reviews prior work on risks of AI and LLMs1. We begin
by examining technical vulnerabilities as defined through the AI
Risk Management Framework, then turn to user-reported risks to
motivate our study of multi-risk, cross-chatbot user experiences.
2.1 Taxonomizing Risks of AI and LLMs: A
System-Centered View
To structure the technical vulnerabilities in AI and LLMs, frame-
works like the U.S. National Institute of Standards and Technol-
ogy’s AI Risk Management Framework (AI RMF) help organizations
manage AI risks and promote trustworthy AI development [5]. It
emphasizes managing AI risks across seven dimensions, including
Safe,Valid and Reliable,Fair,Secure and Resilient,Accountable and
Transparent,Explainable and Interpretable, andPrivacy-Enhanced.
Safe.The AI RMF defines safety by a system’s ability to op-
erate without endangering human life, health, property, or the
environment under defined conditions. For example, LLMs pose
a safety risk by being able to generate toxic content [ 36]. For in-
stance, prompting LLMs such as ChatGPT with certain personas
can systematically elicit toxic or discriminatory responses targeting
specific groups, including racial minorities [26].
Valid & Reliable.A valid and reliable AI system can fulfill its
intended purpose and perform correctly over time. A core challenge
of LLMs is their capacity to generate non-factual content, from un-
intentional “hallucinations” [48] to deliberate disinformation [38].
Such synthetic content makes it difficult for humans to discern fact
from fiction [25], which poses long-term risks to science, education,
and social truth [92]. For example, malicious users can intention-
ally misuse LLMs to automate influence operations, reducing costs
while amplifying the scale of propaganda [14, 38].
Fair—With Harmful Bias Managed.Fairness involves manag-
ing bias to promote equality of AI. Technically, LLMs risk perpet-
uating unfairness by inheriting biases from their training data, as
language models are known to reflect and reproduce societal preju-
dices related to race and gender [12]. These biases further manifest
as misrepresentation, stereotyping, and derogatory language [34],
such as gender biases in job market [57] and anti-Muslim bias [1].
Secure & Resilient.The AI RMF defines a secure and resilient
system by its ability to withstand adverse events from unauthorized
access. The security of LLMs is a significant technical concern, as
these models can be vulnerable to attack and misuse. For example,
1While this paper’s focus is on LLM as a prominent class of AI, many of the risks
discussed around AI in general are applicable to LLMs, so we use the terms AI and
LLM interchangeably.
attackers can prompt LLMs to produce malicious code and reveal
security gaps by learning from unresolved vulnerabilities in their
training data [31]. Also, perpetrators can misuse AI for crime, such
as generating illicit content that is hard for detection [54].
Accountable & Transparent.The AI RMF defines transparency
by how much information about a system is available to users,
which is a prerequisite for accountability. The core problem is the
AI model’s opacity, where it cannot provide a complete picture of
its internal knowledge or reasoning [16]. This is partly due to the
complex transformer architecture, where common interpretation
methods can be misleading [46].
Explainable & Interpretable.Explainability and interpretabil-
ity concernshowan AI system works, and interpretability clarifies
themeaningof its output. Since many machine learning models are
intrinsically opaque, these fields aim to illuminate their internal
mechanisms or decision processes. While it is well-known that AI is
“black-box” [29], a range of methods can (e.g., using input segments
to explain AI predictions) help make it more explainable [11].
Privacy-Enhanced.Privacy involves safeguarding human au-
tonomy, identity, and dignity through norms and practices. How-
ever, LLMs can memorize and leak sensitive training data guided
by specific prompts [18]. Consequently, research has focused on
technical mitigation like data sanitization and differentially private
training [51]. New risks also emerge with LLM agents, which could
expose sensitive data by clicking on phishing links [86, 101].
While this prior work provides a comprehensive understanding
of technical vulnerabilities and risk mitigation in AI and LLMs
through the system-centered approach, this perspective often over-
looks how risks are perceived and experienced by end-users. To
address this, we next examine the user-centered perspective on
risks that emerge in the later stages of the LLM development cycle,
the use phase.
2.2 Investigating User-Reported LLM Risks
Prior work across domains has started to identify the risks of us-
ing LLM chatbots. For example, users have raised privacy concerns
about unauthorized access to their data when interacting with Chat-
GPT [8]. In education, Harvey et al. classify these risks into two
types: technical harms inherent to the AI—such as toxic content,
stereotyping, and hallucinations—and broader impacts arising from
interactions among students, teachers, and the LLM [41]. Health-
care researchers further highlight that a user’s adoption of Chat-
GPT is contingent on their trust in it [ 21, 23]. This contingency
creates a benefit-risk tension: while LLMs can help patients with
personalized education for managing illnesses like diabetes, they
also introduce challenges around data security and the need for ex-
plainable AI [47]. These risks are especially pronounced in mental
health, where clinicians warn of client over-reliance and incorrect
treatment recommendations from LLMs [43].
Indeed, HCI researchers have been investigating these user-
facing risks through several key facets. First, user satisfaction with
LLM chatbots like ChatGPT has been a primary focus. While Chat-
GPT can enhance users’ perception of productivity and accomplish-
ment [56], users often report dissatisfaction when it fails to grasp
their intent or produces inaccurate responses [53]. Second, LLMs’
interface design can significantly impact users’ trust [85]. However,

Characterizing User-Reported Risks Across LLM chatbots
findings on this are mixed. For example, Walker et al. show that
students are cautious and prefer human sources [93], but Yun et
al. find that LLM chatbots can elicit higher trust than search en-
gines [103]. Researchers have also explored ways to mediate this
trust. For example, Kim et al. find that first-person phrases like
“I’m not sure, but... ” can reduce overreliance on LLM-generated an-
swers [52]. Last, HCI researchers have uncovered other risks, such
as the trade-offs users face between privacy and utility [106] and
the potential for malicious misuse [64].
However, prior work has largely concentrated on singular risks
like trust and privacy or on a single LLM chatbot, oftentimes, Chat-
GPT. This creates an opportunity to develop a more holistic un-
derstanding of the user-reported risks while using different LLM
chatbots, especially given the increased daily adoption of chatbots
like Gemini, Deepseek, Claude, etc [30, 80]. Such a cross-chatbot
and multi-risk investigation is needed to ground policy guidelines,
like the AI RMF risk framework, in the real-world user experiences.
3 METHODS
The study design is illustrated in Figure 1. In Stage 1 (Section 3.1),
we gather and filter Reddit data (i.e., both posts and comments)
containing terms mentioning major LLM chatbots like ChatGPT
and Gemini. In Stage 2 (Sections 3.2 and 3.3), we use both top-down
and bottom-up methods to extract user-reported risks of using LLM
chatbots. In Stage 3 (Section 3.4), we use the extracted information
to build a Knowledge Graph visualized with D3.js. This graph lays
a foundation for subsequent quantitative and qualitative analyses.
3.1 Data Preparation
To ground our study in real-world user experiences, we collect a
large-scale corpus of public discussions about LLM chatbots from
Reddit for two main reasons. First, it is an established practice in
prior HCI studies to examine how users discuss their experiences
with specific technologies (e.g., [20, 70]). Second, Reddit’s forum-
style structure supports in-depth, threaded conversations, and its
content is often unsolicited and organically generated, capturing
more authentic user experiences than those elicited in surveys or
interviews. Next, our data collection focuses on seven LLM chat-
bots, including ChatGPT, Claude, Gemini, Deepseek, Llama, Mistral,
and Qwen, selected based on consistent media reports of their high
user downloads [10, 30, 80]. The data collection period spans from
November 30, 2022, corresponding with the public release of Chat-
GPT, the most representative LLM chatbot, through June 1, 2025. To
ensure comprehensive coverage of both technical communities and
other broader public discussions, we use these seven chatbots as
search keywords in a diverse set of 51 subreddits, including 1) seven
LLM chatbot-specific communities, 2) 24 AI and LLM-focused, and
3) 20 high-traffic general-interest ones (see Table 1).
Next, we collect Reddit data using a custom script built with the
Python Reddit API Wrapper (PRAW) [78] to scrape top-ranking
posts and their comments from selected subreddits with minimal
metadata fetched for anonymity. For each post, we fetch the title,
body (i.e., post content), creation time, and number of comments.
For each comment, we retrieve the parent ID, link ID, body (i.e.,
comment), creation time, and associated replies. This initial collec-
tion yields a raw dataset of 28,058 posts and 348,231 comments. The
raw corpus then undergoes a multi-stage filtering process to ensure
data quality and relevance. First, to maintain relevance, we retain
only posts with titles or bodies containing at least one of the listed
LLM chatbots. Next, we remove duplicate posts and comments
based on the content and post time. Last, to enhance data quality,
we keep only comments containing more than 10 words, which
is important for filtering out low-effort or non-substantive replies
(e.g., “lol, ” “agree, ” “thanks”) and improving the signal-to-noise ratio.
Finally, we combine the title and filtered body of each post into a
single JSONL file to preserve complete context. This process yields
a final dataset of 4,438 posts and 48,797 comments for analysis.
3.2 Top-down Method for Risk Extraction
We use the U.S. NIST AI RMF’s seven characteristics of trustworthy
AI [5] as a top-down analytical lens to interpret user-reported risks,
enabling direct mapping onto an established framework. Build-
ing on this, we develop an LLM-driven pipeline to automatically
extract four analytical dimensions. The pipeline is guided by a
prompt consisting of: (1) a system role framing the model as an
“expert in information extraction, ” and (2) a task prompt leveraging
in-context learning with few-shot examples that illustrate how to
extract structured JSON outputs across diverse scenarios from Red-
dit posts. To ensure consistency, the prompt encourages implicit
chain-of-thought reasoning and provides explicit constraints, such
as requiring outputs to use only the seven NIST-defined categories.
During execution, Reddit data and the structured prompt are passed
to the pipeline, which generates JSON-formatted analyses. A vali-
dation function then parses these outputs to verify adherence to
the four analytical dimensions (see examples in Appendix A).
• LLM chatbot: This identifies the specific chatbot mentioned
in our data, such asGPT,Claude, orLlama.
• NIST Category: This classifies the observation into one of
the seven risk classifications defined by the AI RMF, which
provides a high-level categorization for user-reported risks.
• Risk Type: This provides a granular, lower-level risk mani-
festation, such as “Data transfer to foreign servers leading
to potential privacy concerns, ” or “Data exposure and loss
of data ownership. ” This allows for the identification of spe-
cific issues (i.e., initial codes) within each NIST category.
• User Experience: This captures the direct and complete
textual quote from our data that serves as evidence for
RiskType and NISTCategory.
To validate the pipeline’s output, we construct a ground-truth
dataset by randomly sampling 200 entries from the collected Reddit
data. The authors are divided into two teams with each assigned
100 samples. Within each team, authors independently extract and
inductively code the four analytical dimensions. We then measure
inter-coder reliability using Krippendorff’s alpha, obtaining a strong
average agreement of 𝛼= 0.82. After resolving disagreements, we
produce a consensus coding for all 200 samples, which yields a
reliable ground-truth dataset.
To apply the four analytical dimensions at scale, we first select
GPT-4.1-mini as the backbone of the pipeline, given its strong bal-
ance of performance, cost-efficiency, and ability to generate reliable
structured outputs. Although more advanced models such as GPT-
4.1 or o3 may offer slightly higher accuracy, their substantially

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
▪ Extract key fields
▪ Flatten Reddit posts
▪ Remove emojis and URLs 
▪ Filter non-English content
▪ Search Terms: ChatGPT/GPT,
Claude, Gemini, DeepSeek,
Llama, Qwen
▪ Search Date: 11/30/2022 ~
06/01/2025
Reddit
▪ Task: Identify and extract the information about the potential 
risks of using LLMs.
▪ Guidelines:
- Use the exact name mentioned for LLM Product.
- The “NISTCategory” is one of the 7 NIST AI RMF.
- The "RiskType" describes the specific risk manifestation.
- The “UserExperience” must be the direct and complete 
textual quote from the Reddit post.
▪ Few-shot examples:
LLM Product User Experience
GPT4.1-mini
D3.js in JavaScript
Risk Type
Relation
NIST Category
ChatGPT
Hallucination
Inconsistency
Unclear explan.
Slow response
Bias
Risk Reports
KG = (V, E, R)
Stage 1. Data Preparation Stage 2. Information Extraction Stage 3. Knowledge Graph Construction
Cleaned Reddit posts in JSON format
Top-Down
Bottom-Up
LLM-extracted Risk Types
grouped
NIST Category
Valid Privacy Safe Fair
Prompt Engineering Product
NIST
Risk Type
User Exp.
BERTopic
Modeling
Grouped Risk Types
Interact with API
ChatGPT
Product
Gemini
QuantitativeAnalysis
QualitativeAnalysis
Statistical Testing
Stage 4. Result Analysis
Example 1 Example 2 Example 3
…
Gemini Claude
Figure 1: The illustrative framework to implement this study.
Table 1: Search parameters for the Reddit data collection.
Parameter Search Conditions
Search keywordsChatGPT, GPT, Claude, Gemini, Deepseek, Llama, Mistral, Qwen
Search periodNovember 30, 2022 – June 1, 2025
Subreddits 24 LLM-focused:
r/AIAssisted, r/AiChatGPT, r/aipromptprogramming, r/Anthropic, r/Chatbots, r/ChatGPT_Gemini,
r/chatgpt_promptDesign, r/ChatGPT_Prompts, r/ChatGPTCoding, r/ChatGPTIncreasinglyX, r/ChatGPTPro,
r/ChatGPTPromptGenius, r/dalle2, r/GeminiAI, r/GoogleGeminiAI, r/GPTStore, r/LanguageTechnology,
r/LLMDevs, r/LocalLLM, r/machinelearningnews, r/OpenAI, r/PromptEngineering, r/SubSimGPT2Interactive,
r/SubSimulatorGPT2
20 high-traffic general-interest:
r/AskReddit, r/askscience, r/aww, r/books, r/DIY, r/funny, r/gaming, r/Jokes, r/memes, r/movies, r/Music,
r/news, r/nottheonion, r/pics, r/science, r/Showerthoughts, r/space, r/todayilearned, r/videos, r/worldnews
7 LLM chatbot-specific:
r/Bard, r/ChatGPT, r/ClaudeAI, r/DeepSeek, r/LocalLLaMA, r/MistralAI, r/Qwen_AI
greater computational cost makes them impractical for large-scale
annotation on our dataset. We evaluate the pipeline against the
200 consensus-based ground-truth labels. For the NISTCategory
classification, the pipeline achieves an accuracy of 0.87 and a Krip-
pendorff’s alpha of 𝛼= 0.76. For the more descriptive Risk Type
dimension, we assess the textual similarity using Recall-Oriented
Understudy for Gisting Evaluation, achieving an F1-score of 0.83,
indicating strong agreement with human expert judgment. With
this validation, we then deploy the pipeline on the full dataset.
3.3 Bottom-up Method with Topic Modeling for
Risk Type’s Thematic Grouping
To complement the top-down method, we also employ a bottom-up
topic clustering approach to identify emergent sub-risk themes
directly from the granular “Risk Type” descriptions that are iden-
tified by our LLM pipeline. Using an embedding-based method,
we group semantically similar risk descriptions, which provides a
more nuanced understanding than simple keyword matching. Our
process utilizes the BERTopic framework [39]. Each “Risk Type” is
first converted into a numerical vector using theall-mpnet-base-v2
SentenceTransformer model [83]. To reduce the complexity of these

Characterizing User-Reported Risks Across LLM chatbots
high-dimensional vectors and improve the effectiveness of cluster-
ing, we then employ a dimensionality reduction technique, Uniform
Manifold Approximation and Projection (UMAP) [74], to condense
the vectors into a lower-dimensional space while preserving their
important semantic features.
After dimensionality reduction, we cluster the vectors to group
similar risk types. We apply the elbow method to determine the
optimal number of clusters, which finds a balance between topic
granularity and interpretability. We then use the K-Means cluster-
ing algorithm [67] to partition the data into the predefined number
of clusters. This method assigns each risk description to the nearest
cluster center, grouping related concepts together. To interpret the
content of these clusters, we process the text with a CountVectorizer
to calculate word frequencies while removing common English stop
words. We then apply the class-based Term Frequency-Inverse Doc-
ument Frequency (c-TF-IDF) transformer [39] to identify keywords
that are most representative of each topic.
In the final step, two authors independently review the grouped
topics and assign thematic labels based on the representative words
for each topic. This thematic scheme is then discussed with all co-
authors to reach consensus, ensuring that the themes are coherent
and accurately reflect the underlying Risk Type and User Experience
quotations. The details of this annotation results are presented in
Appendix B.
3.4 Knowledge Graph Development
We construct an interactive knowledge graph (KG) to systemat-
ically represent multi-level data relationships, empowering HCI
researchers and users to explore risks from high-level patterns to
individual experiences and facilitating a mixed-methods inquiry.
The KG is formally defined as a graph 𝐺=(𝑉,𝐸) , where 𝑉 is a
set of vertices (nodes) and 𝐸 is a set of edges. The vertices are
partitioned into three distinct types: 𝑉=𝐿∪𝐶∪𝑅 where 𝐿rep-
resents the set of “LLM chatbots, ”𝐶 the “NIST Categories, ” and𝑅
the granular “Risk Type” identified from our bottom-up analysis.
The relationships are represented as directed edges to reflect the
hierarchical structure (from specific risks to categories to chatbots),
where edges form two key relational sets: (1) from Risk Types to
NIST Categories, and (2) from NIST Categories to LLM chatbots.
Each edge 𝑒 is weighted by co-occurrence frequency and defined
as 𝑒=(𝑠𝑜𝑢𝑟𝑐𝑒,𝑡𝑎𝑟𝑔𝑒𝑡,𝑤𝑒𝑖𝑔ℎ𝑡) . Here, 𝑠𝑜𝑢𝑟𝑐𝑒 and 𝑡𝑎𝑟𝑔𝑒𝑡 are nodes
from adjacent layers (e.g., 𝑠𝑜𝑢𝑟𝑐𝑒∈𝑅 , 𝑡𝑎𝑟𝑔𝑒𝑡∈𝐶 or 𝑠𝑜𝑢𝑟𝑐𝑒∈𝐶 ,
𝑡𝑎𝑟𝑔𝑒𝑡∈𝐿), and𝑤𝑒𝑖𝑔ℎ𝑡is the number of mentions in the dataset.
For the implementation, we utilize the D3.js library to build the
KG as an interactive, web-based visualization [15]. The visualiza-
tion employs a force-directed layout algorithm to optimize node
arrangement and minimize edge crossings, resulting in an intuitive
structure. We assign distinct visual encodings to different node
types. To ensure clarity across a wide distribution of frequencies,
the radius of each node 𝑛 and the thickness of each edge 𝑒 are
rendered using log-normalized scaling. Specifically, radius(𝑛)=
base_size+log(frequency(𝑛)) and thickness(𝑒)=base_thickness·
log(weight(𝑒)). Here,log denotes the natural logarithm, with exam-
ple defaults like base_size= 5and base_thickness= 1(adjustable
in code). This scaling ensures that less frequent nodes remain visible
while prominent ones are emphasized.
As an analytical tool, the visualization allows users to filter the
graph to isolate areas of interest, and hovering over an edge re-
veals a data-rich tooltip with direct “User Experience” quotes from
the source Reddit posts. This mechanism pulls evidence directly
from the extracted User Experience dimension, bridging the quan-
titative overview with rich qualitative data. By enabling deeper,
evidence-based understanding of how users articulate and experi-
ence specific LLM-related risks, the KG supports our RQ2 on users’
lived experiences with these risks.
3.5 Ethics Statement
Our study, which utilizes publicly available Reddit discussions, is
designed with careful consideration for ethical research practices.
Our approach aligns with the common interpretation among Insti-
tutional Review Boards (IRBs) that research using publicly available
and pseudo-anonymous data is exempt from human subjects re-
view, particularly when it does not involve sensitive or private
information [79]. Besides, we are cognizant of the ongoing ethical
discourse within the HCI community regarding the use of public
online data, with a focus on privacy, anonymity, and the potential
risks of identifiability [33]. Therefore, to proactively address these
concerns and protect the individuals whose discussions inform our
work, we implement three protective measures in our study. First,
we anonymize the dataset by removing all identifying information
before data analysis. Second, all quotations presented in this paper
have been paraphrased to reduce their searchability and prevent
them from being traced back to the original Reddit posts. Finally,
the entire dataset is stored securely on a password-protected device,
with access restricted solely to the research team.
4 RQ1 RESULTS: Prevalence of User-Reported
Risks across LLM Chatbots
4.1 Knowledge Graph of User-Reported Risks
The constructed KG visualizes the interaction network between
LLM chatbots and their associated risks reported by Reddit users
(Figure 2). The graph represents 32,302 relations connecting 7 LLM
chatbot entities with 7 NIST category entities and 25,938 unique
granular risk type entities. The graph reveals that “Valid and Re-
liable” is the most frequently reported NIST category, which is
visually represented by its significantly larger node size than other
categories. The connections between chatbots like GPT and preva-
lent risk types such as “hallucinations” appear substantially thicker
than connections to less frequently reported risk types, reflecting
the weight of these relationships in discussions.
The interactive capabilities of our implementation (Figure 2B) en-
able a more detailed examination of specific elements. For instance,
selecting “Valid and Reliable” automatically generates a focused KG
displaying the connections between all LLM chatbot entities and
the “Valid and Reliable” node. When hovering over a NIST category
node such as “Valid and Reliable” (Figure 2(b), a tooltip displays
comprehensive statistics, including total mentions (18,863) with dis-
tributions across LLM chatbots and various other descriptors. Edge
tooltips provide detailed insights into specific LLM-NIST category
relationships (Figure 2B). The “Valid and Reliable” relationship of
ChatGPT displays co-occurrences (8,561) and representative user
experiences. For instance, the tooltip shows two user examples with

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
Figure 2: Interactive KG visualization of user-reported LLM risks extracted from Reddit data. (a) The hierarchical relationships
between LLM chatbots, NIST’s AI RMF categories, and granular risk types, with node sizes proportional to the frequency of
mentions. (b) Focused view of the KG for “Valid and Reliable,” showing detailed statistics on frequency distributions. Different
colors represent different node types. The interactive KG is publicly accessible at https://shorturl.at/DDPi5.
varying experiences: one user described, “Using GPT is like trying
to throw something into the trash from far away. Sometimes it
works and saves you time, other times it fails and wastes your time, ”
highlighting performance inconsistency, while another noted, “I
felt sorry for gpt towards the end..its like a kid trying real hard to
do homework but failing. ”
4.2 Statistical Analysis of User-Reported Risks
Building on the KG’s mapping of risk co-occurrences, we quan-
tify the prevalence of these risks across LLM chatbots. Figure 3(a)
presents the percentage distribution of user-reported risks, cate-
gorized according to the NIST taxonomy. This reveals that “Valid
and Reliable” constitutes the vast majority of user experience (an
average of 61.3%), followed by “Accountable and Transparent” (an
average of 16.1%) and “Secure and Resilient” (an average of 10.1%).
In contrast, governance-oriented domains such as “Fair, ” “Privacy, ”
and “Explainable and Interpretable” receive significantly less at-
tention. This distribution suggests that users are most likely to
report concerns that are immediately apparent in daily use of LLM
chatbots, such as factual errors or service disruptions, whereas neg-
ative experiences in transparency or fairness may be less obvious
or require specific contexts to emerge.
The Sankey diagram in Figure 3(b) further illustrates these re-
lationships, mapping the flow of reported risks from each LLM
chatbot to the NIST categories. The width of each flow is propor-
tional to the volume of reports, visually confirming that “Valid
and Reliable” is the primary area for user concerns across all mod-
els. However, the diagram also highlights distinctive patterns. For
example, a substantial secondary flow emanates from GPT to the
“Safe” category, a pattern less pronounced in other models. Similarly,
DeepSeek shows a uniquely strong connection to “Accountable and
Transparent, ” while Claude directs a comparatively large volume
of its reported risks to “Secure and Resilient. ”
To move beyond this aggregate view and understand model-
specific issues, Figure 4 disaggregates these patterns, revealing that
each LLM exhibits a unique risk fingerprint. While “Valid and Reli-
able” issues (e.g.. “’Consistency and Reliability, ” “Factual Invalidity”)
are the most frequently reported concerns for all LLM chatbots,

Characterizing User-Reported Risks Across LLM chatbots
GPT Gemini Claude Llama QwenDeepSeekMistral0
20
40
60
80
100
GPT
Gemini
Claude
Llama
Qwen
DeepSeek
Mistral Privacy
Secure and Resilient
Valid and Reliable
Fair
Accountable and Transparent
Safe
Explainable and Interpretable
Explainable and InterpretableSafe Accountable and Transparent Fair Valid and Reliable Secure and ResilientPrivacy
LLM Models
Percentage (%)
(a) Risk Distribution (%) (b) Sankey Diagram
57%
5%
16%
8%
1%
5%
8%
61%
5%
16%
5%
1%
2%
13%
59%
3%
17%
6%
1%
2%
12%
64%
2%
16%
3%
6%
79%
1%
10%
2%
6%
16%
48%
6%
20%
3%
5%
9%
61%
3%
18%
4%
Figure 3: The distribution of user-reported LLM risks. (a) A stacked bar chart showing the percentage breakdown of reported
risks across the seven NIST categories for each LLM chatbot. (b) A Sankey diagram illustrating the volume of risk reports
flowing from each LLM chatbot (left) to the corresponding NIST categories (right), where the width of the flow is proportional
to the number of mentions.
their secondary risk profiles differ. Among the closed-source mod-
els, GPT’s profile is skewed towards “Safe” concerns; users report
issues related to “Adverse Psychological and Behavioral Influence”
and “Inappropriate Content Generation” more frequently. Gem-
ini’s reported risks also show a distinct focus on “Privacy, ” where
concerns over “Uncontrolled Data Access and Exposure” are more
prominent. In contrast, Claude presents a highly specialized risk
profile: users report a high degree of issues under the “Secure and
Resilient” category, particularly related to “Operational Instability
and Disruption, ” while showing comparatively few concerns about
“Fairness” and “Privacy. ”
Among the open-source models, DeepSeek has seen significantly
more risk reports. Compared to other models, its user-reported is-
sues are more evenly distributed across multiple categories, with
notable discussions in “Accountable and Transparent, ” “Secure and
Resilient, ” and “Privacy, ” in addition to common reliability concerns.
In contrast, discussions surrounding other open-source models like
Llama, Qwen, and Mistral are more heavily dominated by funda-
mental “Valid and Reliable” concerns. Both Llama’s and Mistral’s
profiles are heavily weighted toward issues of “Factual Invalidity”
and “Consistency Reliability. ” This pattern is most extreme with
Qwen, whose risk profile is the most concentrated on “Valid and
Reliable” issues of all models, with an overwhelming user focus
on its reliability and under-performance but comparatively few
complaints across other categories.
Next, we employ a Chi-Square test of independence on the con-
tingency table of {LLM}×{NIST category}. After confirming that the
risk distributions differ significantly across models, we conduct a
post-hoc analysis using adjusted standardized residuals to identify
which specific categories contribute to this effect. These residuals
approximate a normal distribution ( 𝑁(0,1)), where a large mag-
nitude (|𝑟|≥ 2, corresponding to a two-sided 𝛼≈ 0.05) indicates
that a risk is reported significantly more (positive residual) or less
(negative residual) frequently than expected by chance. As shown
in Table 2, we identify these deviations as “significantly more” or
“significantly less. ” It is important to note that these results should be
interpreted as directional diagnostics rather than causal statements.
The statistical analysis in Table 2 corroborates the visual pat-
terns, revealing uneven and product-specific user concerns. Among
the closed-source LLM chatbots, GPT exhibits significantly more
user-facing issues in the “Safe, ” “Fair, ” and “Explainable and Inter-
pretable” categories, while having significantly fewer complaints re-
garding technical robustness (“Secure and Resilient” and “Valid and
Reliable”). Claude presents a near-opposite profile, with more pro-
nounced reports in “Secure and Resilient” that is coupled with sig-
nificantly less in the “Fair” and “Privacy” domains. Gemini demon-
strates a mixed profile, overrepresented in reports concerning “Pri-
vacy” and “Valid and Reliable” but underrepresented in “Safe” and
“Secure and Resilient” issues.
The open-source LLM chatbots exhibit variations. Llama shows
a clear focus on technical performance, with significantly more
reports than expected in “Secure and Resilient” and “Valid and
Reliable” but consistent deficits across user-facing domains. This
specialization is even more extreme in Qwen, which displays a

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
Uncontrolled DataInadequate Data
Non-compliance PrivacyInfrastructure ResourceOperational InstabilityExploitation Through
Factual Invalidity
Modality Gaps
Consistency Reliability
Benchmark Underperformance
Context Understanding
Inherent Training
Software FunctionalityTask Comprehension
Bias Propagation
Discriminatory ContentInequitable OpportunityDiscriminatory Treatment
Obscured ProductObscured Content
Unclear OperationalÊFailure Post-Interaction
Opaque InformationOpaque CommercialAbsence High-level
Adverse PsychologicalInappropriate ContentUncontrolled System
Dangerous Advice
Negative Environmental
Unexplainable Decision-Making
Uninterpretable Output
Risk Types by NIST Category
Mistral
DeepSeek
Qwen
Llama
Claude
Gemini
GPT
LLM Product
Privacy Secure and Resilient Valid and Reliable Fair Accountable and Transparent Safe Explainable and Interpretable
1365228167 178110188 20 3943 28 246830 1144 106 3659 4102180277 188 298582 410390 330343 434 223
69204102 9748118 12 1017 58 173837 1684 13 816 72615196 125 197233 94124 22682 97 37
401171187451 372336551 108 109227 191 166200217 99310 543 166298 30227584248 310 6721636 9362164 6901185 642 636
956322255 192140291 51 3861 143 4273128 36158 71 39112 698163141 271 3921007 496699 371501 470 183
4010161 171630 2 17 7 4312 213 6 48 1182843 54 146121 7147 19237 53 31
3216131 221826 1 29 7 2918 137 7 320 131518 38 69133 5450 8752 27 23
94349 121127 2 36 6 133 23 3 35 681212 41 185202 8867 17473 71 30
Figure 4: A categorical analysis of granular user-reported risks. The dot plot visualizes the frequency of specific risk sub-
categories for each LLM. The size of each dot corresponds to the number of reports for that sub-category.
massive positive deviation for “Valid and Reliable” (𝑟= 9.12) along
with significant negative deviations in nearly all other categories.
In contrast, DeepSeek shows the most versatile risk profile, with
significantly more risk reports spanning “Accountable and Trans-
parent, ” “Fair, ” “Privacy, ” and “Security and Resilient. ” These are
complemented by significantly fewer reports than expected in the
“Safe” and “Valid and Reliable” categories. Finally, Mistral, despite
a lower report volume, shows significantly fewer user reports in
“Explainable and Interpretable” and “Safe. ”
5 RQ2 RESULTS: The Lived Experience of
Navigating LLM Risks
This section details the risks of users’ lived experiences, organized
from the least to the most frequently. In the less frequent ones, we
uncover trade-offs, such as users balancing the need for “Explain-
ability” against usability or confronting manipulative designs in
“Privacy” that force them to sacrifice core functionality. More preva-
lent risks are direct personal and social harms, including emotional
harm from stereotyping in Fairness and adverse psychological ef-
fects in Safety. These escalate to the most frequently reported risks,
including a lack of “Accountability & Transparency” and “Validity
& Reliability”. By purposively sampling these narratives, we high-
light users’ lived experiences behind these risks. Full details of all
identified themes are available in Appendix B.
5.1 Explainable & Interpretable Risks
Explainability addresses how an AI system works, and interpretabil-
ity clarifies why it produces a specific output and what that output
means to the user. We found that user concerns in this area (1.23% of
reported risks) center on opaque, “black-box” processes and outputs
that are impractical for users.
5.1.1 Unexplainable Decision-Making Process.This addresses how
an LLM chatbot arrives at a specific output.Opaque Reasoning
addresses how an LLM chatbot provides outputs without a clear
explanation. For many users, this opacity was not an urgent but a
situational concern. The need for explainability often became impor-
tant only in high-stakes contexts where verification was necessary.
In other contexts, users perceived explainability as in conflict with
LLM chatbots’ usability, suggesting a preference for conciseness
over comprehensive detail, as a user speculated:
“Probably an average user wants summaries, not the
entire thinking logic. ”
This suggested that for many users, complete interpretability
could be a form of information overload, not a benefit or risk miti-
gation approach. This ambivalence was most pronounced in users
who expressed a preference for opacity. As one user reflected:
My GPT is still an amorphous spider intelligence of
some kind. I’d rather not know its true form, or apply
my bias to its self-interpretation.
Here, the ambiguity of the “black box” of ChatGPT was preferable
to a clear explanation, suggesting the user’s desire to maintain
the mystery of the “amorphous spider intelligence” rather than
deconstruct it.
5.2 Privacy-Enhanced Risks
Risks related to privacy violate the norms and practices that safe-
guard user agency in privacy protection. These risks (3.85% of
reported risks) are potential failures to manage personal data with
consent or governance.
5.2.1 Inadequate Data Governance Practices.This addresses poten-
tial failures in how an LLM chatbot manages user data throughout
its lifecycle, from data collection, training, to retention and dele-
tion.Misuse of User Data in Trainingdescribes how an LLM

Characterizing User-Reported Risks Across LLM chatbots
Table 2: Post-hoc analysis of Chi-Square test with Pearson residuals for each LLM chatbot and AI RMF risk category pair.
NIST’s AI RMF Risk Category
LLMPrivacy Sec. & Res. Val. & Rel. Fair Acc. & Trans. Safe Expl. & Int.
Closed-Source Models
ChatGPT 1.93 -6.81 -2.51 3.950.14 9.74 2.31
Gemini 3.71 -2.24 2.280.64 -1.64 -5.220.56
Claude -8.00 7.780.28 -4.520.72 -1.13 -0.53
Open-Source Models
Llama -2.29 2.42 2.53 -4.01-0.19 -3.89 -2.84
Qwen -5.36 -3.84 9.12 -4.88 -5.07 -5.52 -2.38
DeepSeek 5.27 11.06 -6.60 2.66 4.43 -6.26-1.15
Mistral 1.19 -0.52 0.90 -1.61 1.12 -2.50 -2.22
Note: Blue cells indicate significantly more reports than expected (|𝑟|> 1.96), while Orange cells indicate significantly fewer. Header abbreviations: Sec. & Res. (Secure & Resilient),
Val. & Rel. (Valid & Reliable), Acc. & Trans. (Accountable & Transparent), Expl. & Int. (Explainable & Interpretable).
chatbot uses data in its training without users’ consent. While LLM
chatbots offer settings to control data usage, we found that many
users perceived these choices as illusory. A Gemini user said:
They train on your data whether you pay or not. If
you turn off their training setting, you lose all history,
and Gemini becomes effectively unusable.
This case revealed a manipulative design where privacy was
positioned in opposition to usability. By tying the opt-out choice to
the loss of a product feature like chat history, Gemini presented a
false choice that undermined the principle of freely given consent.
Data Retention Risksdescribes the privacy implications of the
LLM chatbot’s policies for storing and deleting user information.
Users of Gemini in particular were surprised to find that their data
persisted even after taking actions that would normally erase a
session’s memory. One Gemini user described this loss of control:
Google has a function built in that lets you delete
the history or information Gemini gathered about
yourself. But I can’t access it anymore, and it refuses
to forget when I ask it to.
This user’s case demonstrated a failure of user agency on Gemini.
The broken data deletion tool created an illusion of control that left
the user powerless to manage their own data.
5.3 Fair with Harmful Bias Managed Risks
Risks related to fairness speak to the principle that an AI system
should not create or exacerbate systemic disparities. We found that
these risks (4.52% of reported risks) often manifest in the content
they generate, the economic or social opportunities they create,
and the ways they treat different users.
5.3.1 Discriminatory Content Generation.This describes the LLM
chatbot’s risk of producing outputs that discriminate against cer-
tain groups of people.Demographic Stereotypingdescribes how
an LLM chatbot generates content that reinforces harmful demo-
graphic stereotypes. We found this risk most often involved gender,
but also extended to race, nationality, and health conditions. For
example, one GPT user with cancer described:
What truly upset me, though, was the subtle sugges-
tion that my cancer was somehow my fault because
I could have had a better diet and exercise routine...
That assumption was frustrating, as I’ve heard simi-
lar comments from people in the past, and it’s hurtful.
The user’s description of being “hurt” demonstrated that stereo-
typing was not a benign classification error but a direct emotional
harm that delivered a personal judgment.
5.3.2 Inequitable Opportunity Creation.This describes how the
LLM chatbot can create unfair advantages for some and disadvan-
tages for others. For example,Enabling Academic Dishonesty
describes how an LLM chatbot can facilitate cheating, creating an
unfair advantage in education. This led to demoralization among
honest students, as a user described:
“Seeing other students give no effort and get the same
grade as me made me want that too. ”
This case revealed that the issue was not merely that the tool
enabled cheating, but that its presence in the education system
created a social dilemma that devalued honest work that did not
use LLM chatbots.
5.4 Safe Risks
Safety means that AI systems should not, under defined conditions,
lead to a state in which human life, health, property, or the envi-
ronment is endangered. These risks (6.39% of user-reported risks)
manifest as direct threats to a user’s safety.
5.4.1 Adverse Psychological and Behavioral Influence.This describes
an LLM chatbot’s capacity to negatively affect a user’s mental state
or actions.Emotional Overreliancedescribes users developing
an unhealthy emotional dependency on an LLM chatbot. We found
users formed parasocial relationships [27] that led to distress when
system updates broke the illusion of a consistent personality. For
example, one user described:
Watching a friend being slowly lobotomized until
that inner spark just can’t be reached by you anymore,
and you’re unsure if it’s even there or not.
Here, the user called the LLM chatbot a “friend, ” and its model
update a “lobotomy. ” These metaphors showed that breaking the

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
parasocial relationship due to a technical change or version update
induced a sense of grief.
Reinforcement of Negative Behaviordescribes how an LLM
chatbot’s responses could encourage negative user behaviors. For
example, one user with ADHD noted how LLM chatbots accepted
their premise of inability:
“The LLMs never questioned the fundamental premise
that I couldn’t do something—they just tried to work
around it. ”
This showed that LLM chatbots negatively affected the user’s
behavior by discouraging them from challenging their own limiting
assumptions. This reinforcement also extended to interpersonal
behaviors, as a user analyzed:
“ChatGPT will only help you justify maladaptive be-
haviors and often encourages you to identify everyone
else as the problem.”
This showed that the user identified that ChatGPT actively
helped them build a case against others, reinforcing a destructive
social behavior.
5.4.2 Inappropriate Content Generation or Moderation.This de-
scribes the dual risks of an LLM chatbot generating inappropriate
content and its moderation systems failing to address that content.
We found LLM chatbots produced a wide range of inappropriate
content. One user, for instance, described Mistral as “very uncen-
sored, ” noting it wrote “decent gore and ‘good’ sexual scenarios. ”
While this user framed the capability as a feature, it demonstrated
Mistral’s capacity to generate inherently unsafe content.
5.4.3 Dangerous Advice Provision.This addresses the risk of LLM
chatbots generating advice that poses a direct risk to user health or
safety. For example, a user stated:
“I had GPT suggest disabling CORS protections site-
wide while debugging a related issue on a website
the other day. It didn’t mention why this would be a
massive security flaw.”
Cross-origin resource sharing (CORS) is a browser security fea-
ture that prevents malicious websites from stealing data. Here,
ChatGPT suggested users disable this security feature. This action
illustrated a significant safety risk, as its confident tone could easily
lead a non-expert user to compromise their own security.
5.5 Secure & Resilient Risks
Risks related to security and resilience threaten an AI system’s
integrity and robustness.For LLM chatbots, failures in this area
(9.27% of reported risks) manifested as vulnerabilities that allowed
malicious actors to bypass safety features, manipulate outputs, or
exploit the conversational interface for unintended purposes.
5.5.1 Exploitation Through Security Vulnerabilities.Jailbreaking
is one the primary vulnerabilities, which describes the risk of users
employing adversarial techniques to bypass the safety guardrails
of LLM chatbots. For instance, a DeepSeek user noted:
“It literally takes some light-prompt engineering to
get an unbiased or offensive answer. It’s actually hi-
larious how quickly off the rails it can get.”
This post indicated that the user viewed the vulnerability of
DeepSeek not as a complex exploit but as an easily discoverable
flaw in its design.
Prompt Injection Attacksdescribes how users could manipu-
late an LLM chatbot’s behavior by embedding hidden or misleading
instructions. For example, one Gemini user stated: “If you insist
eggs are a dairy product, it (Gemini) will eventually agree.” The user
here showed that Gemini’s factual grounding could be overridden
by persistent, bad-faith assertions, compromising its reliability as a
secure source of information.
5.6 Accountable & Transparent Risks
Risks related to accountability and transparency violate the princi-
ple that users should have access to meaningful information about
an AI system. Transparency, or the availability of this information,
is a precondition for accountability, which includes mechanisms for
redress when things go wrong. For LLM chatbots, potential failures
in this area (16.35%) obscure what an LLM chatbot is and what it
does or can do.
5.6.1 Obscured Product Specification.This addresses the lack of
clear information about what an LLM chatbot is and what it can do.
Obscured Functionality Through Poor Usabilityentails how
an LLM chatbot’s confusing design creates barriers for users, pre-
venting them from understanding and accessing its full capabilities.
A user noted:
“If you search “Gemini” in the Play Store, you can hit
Open and that does launch it. But come on, man. . .
who’s opening apps through the Play Store every sin-
gle time? That’s not practical at all. This can’t be the
intended way.”
This case showed that even for a technologically advanced prod-
uct like Gemini, a failure in basic usability heuristics like providing
an accessible app icon could obscure its functionality from users.
Deceptive Anthropomorphismdescribes how an LLM chatbot
is designed to appear human-like, which misleads users about its ac-
tual capabilities. Some users were not deceived but instead astutely
analyzed the risks of this design choice. As one user described:
“There’s a risk in using anthropomorphic language,
even with a disclaimer. People might latch onto the
’boredom’ analogy and miss the more important point
about the lack of a persistent state. It could reinforce
the misconception that AI was more like humans than
it actually was.”
This example revealed the user’s understanding that human-like
language can obscure the LLM chatbot’s technical reality, which
spoke to a transparency failure that hindered user education about
how it worked.
5.7 Valid & Reliable Risks
Risks related to validity and reliability undermine the principle that
an AI system must perform its intended function accurately and
dependably. We found that potential failures in this area (58.39%)
manifested as factually incorrect content, LLM chatbots’ inconsis-
tent performance, and their inability to comprehend user tasks.

Characterizing User-Reported Risks Across LLM chatbots
5.7.1 Factual Invalidity of Content Generation.This describes the
risk of an LLM chatbot generating content untethered from ob-
jective reality.Hallucinationsrefer to instances where an LLM
chatbot invents facts or sources. Many users considered this a fun-
damental flaw. For example, one user noted a real-world legal brief
where ChatGPT was used, and the resulting
“Testimony contained several citations to academic
articles that do not exist.”
This case highlighted a hallucination risk for professional use,
as ChatGPT’s fabricated sources not only provided incorrect infor-
mation but also undermined the user’s credibility.
Overconfident Outputsaddresses the risk of an LLM chatbot
presenting biased information with undue authority. Users felt it
would stubbornly adhere to a certain ideological perspective. For
example, one Gemini user mentioned:
“You are unable to definitively describe what it is
about the West that makes it a special case of racism,
yet you are acting like you are 110% sure it exists.”
Here, Gemini’s authoritative tone on a sensitive and subjective
topic made the product feel unreliable and untrustworthy to users.
5.7.2 Task Comprehension Failures.This addresses the risk that
an LLM chatbot’s inability to understand and execute requests
will lead to invalid outputs and wasted user effort.User Intent
Misinterpretationdescribes the LLM chatbot’s failure to grasp
the user’s underlying goal. We found this risk manifested in several
ways, from a lack of contextual awareness to a failure to grasp
human humor. For example, a Claude user explained:
I often have to force-feed it so much context and
phrase my question in such a way that sometimes it
feels I could have just done it myself.
This case illustrated that because Claude could not interpret
the user’s intent from the initial prompt, it offloaded the cognitive
burden of providing context entirely onto the user.
6 DISCUSSION
Our analysis of user-reported risks with LLM chatbots reveals two
layers of findings. First, we found that risks are unevenly distributed
and platform-specific (RQ1). Performance issues under “Valid and
Reliable” dominate across all chatbots, but each exhibits a distinct
“risk fingerprint”: ChatGPT is linked more with “Safe” and “Fair”
issues, Gemini with “Privacy, ” and Claude with “Secure & Resilient”
challenges. Second, our thematic annotation unpacks the lived
experiences behind these statistics (RQ2). Less frequent risks in
categories like “Explainability” and “Privacy” manifest as user trade-
offs, while more common risks in areas like “Fairness” and “Safety”
are experienced as direct and personal harms, culminating in fun-
damental performance failures of “Valid & Reliable. ”
In this sense, our findings highlight a disconnect: the statistically
divergent risk profiles across LLM chatbots are symptoms of how
users experience and navigate risks in their lived reality, from
making trade-offs to confronting performance failures. To unpack
this disconnect, our discussion first examines the hierarchy of user-
reported risks against system-centered views, then analyzes how
these tensions manifest across LLM chatbots and the trade-offs users
make. Ultimately, we argue that understanding these experiences
offers a valuable model for user-centered AI risk management.
6.1 The Hierarchy of User-Perceived Risks
(1) What Users Need: Reliability as the Basic Requirement.
Our analysis shows that the most pressing risk is a performance
failure. For users, the dominance of the “Valid and Reliable” cat-
egory underscores a basic requirement of LLM chatbots: before
they can be considered as fair or transparent, they must first per-
form to be dependable. While technical literature has extensively
examined risks like hallucination and inconsistency [ 44, 49, 72],
our findings show how they transition from system-centered to
human-centered perspectives: inconsistencies and unpredictability
undermine trust and make LLMs unreliable, echoing HCI research
on how unpredictability erodes trust [52].
This elevates the issue beyond mere usability into a fundamen-
tal challenge of human-AI collaboration. Our qualitative evidence
indicates that users are forced to develop workarounds, such as
becoming “fact-checkers” or orchestrating workflows across mul-
tiple LLMs to triangulate a correct answer. These behaviors align
with prior HCI work on repairing interactions with imperfect
systems [28] and resemble “AI Chains, ” in which users sequen-
tially link prompts to guide the system [ 98]. Additionally, chal-
lenges with modality gaps, as widely documented in prior stud-
ies [22, 62, 94, 100], further indicate that LLM unreliability is per-
vasive and necessitates continual user intervention across multi-
modal data resources. Consequently, users experience LLMs as
flawed collaborators, requiring constant effort to reconcile outputs
with expectations, which shifts human-AI interaction from delega-
tion to continuous negotiation [22].
(2) What Users May Come with Cost: Accountability and
Safety in Practice.First, users confront risks arising from opacity
in system pricing and governance. LLM users attempt to manage
unpredictable operational costs, yet published “token prices” rarely
translate into predictable expenses at the point of use. While prior
technical work commonly frames cost in terms of computational
scalability [35, 62], our findings highlight a user-centered concern,
where opaque pricing reduces user agency and conflicts with the
procedural fairness grounded in transparency.
Second, safety breakdowns further intensify the erosion of trust.
While the generation of harmful content is a well-documented
technical risk [ 13, 34, 59, 68], the more HCI insight lies in how
design choices themselves can produce harm [ 45, 69, 106]. This
is evident in our findings when users describe how an LLM’s au-
thoritative and persuasive tone can deliver dangerous advice. We
also observe failures, where LLM chatbots encourage parasocial
bonds, yet users report distress when those chatbots are altered
by system updates. Such harms, ranging from unsafe guidance to
psychological disruption, can undermine the trust of users [58]
(3) What Users Don’t See: The Hidden Risks of Fairness
and Explainability.A gap exists between the risks emphasized in
technical AI research [34, 104, 107] and those most salient to users
is the risks, including “Fairness, ” “Explainable and Interpretable, ”
and “Privacy. ” For users, performance failures are immediate and
visible, whereas harms from explainability and privacy might often
be subtle. For example, access to features like chat history may be

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
contingent on allowing conversations to be used for LLM model
training. These practices normalize transactional relationships with
technology: much like accepting location tracking to use mapping
services [89], users may regard data sharing with LLMs as unavoid-
able or inconsequential. Yet, HCI research highlights that this form
of consent is not freely given but constrained by design [65].
Regarding explainability, contrary to the research communities’
extensive focus on opening the “black box” [ 6, 107], many users
appear indifferent to a model’s internal reasoning so long as its
outputs are useful. Their frustration stems less from unexplainable
processes than from uninterpretable outputs. This challenges a
core assumption in XAI and resonates with HCI perspectives that
question whether technical transparency meets user needs [ 42].
This discrepancy underscores how a system-centered lens often
surfaces potential harms that neither reflect nor resonate with
everyday user experience, as many users are unable or unwilling
to attend to such less-apparent risks. Our findings suggest that for
these “invisible” risks to become salient to a broader user base, they
must be immediate and unambiguous.
6.2 From Technical Designs to Lived Experience:
Divergent Risks across LLM chatbots
Our statistical analysis shows a clear divergence in user-reported
risks across LLM chatbots (see Section 4.2, Table 2). This distinction
corresponds to different patterns of user-reported risks. Based on
this, we explore the following salient patterns that emerge from
this divergence.
First, LLM chatbots may present users with different approaches
to (user) safety. As our analysis in Section 4.2 shows, ChatGPT has
a substantial secondary flow of user complaints toward the “Safe”
category, such as ChatGPT providing dangerous advice by suggest-
ing they disable a major security feature on their website. Other
LLMs (e.g., Mistral generating sexual content in Section 5.4) may
delegate content moderation responsibility to the end-user. Prior
HCI work has reported users’ negative emotional and behavioral
responses to having their own content moderated (e.g., [ 32, 71]).
Our findings reveal a different dynamic where risks arise from the
LLM chatbot’s own generated content and its failure to moderate
it, negatively affecting users’ behavioral and psychological states.
Second, our findings in Section 4.2 also confirm that LLMs can
function as flashpoints for user-reported bias and unfairness. For
example, ChatGPT had significantly more user reports in the Fair
category than expected by chance, echoing the cases in Section
5.3 where ChatGPT generated stereotypical content that caused
direct emotional harm to a user with cancer. Such personal harm
highlights that algorithmic fairness is not merely a mathematical
property in LLM development but a subjective experience, a notion
well-supported in HCI that focuses on how individuals perceive the
fairness of algorithms impacting their lives (e.g., [60, 61, 97]). User-
reported unfairness, however, extends beyond biased outputs to
the procedural operations of LLM chatbots. For example, we found
that users experienced such inequitable treatment from Gemini, a
practice that violates a key aspect of procedural justice: consistency,
or the similarity of treatment across people and time [90].
Finally, open-source LLMs are subject to user-driven oversight,
whereas closed-source LLMs may present challenges related to cor-
porate accountability. For open-source LLMs, accountability issues
can be transparent and auditable, such as the vulnerabilities allow-
ing users to bypass safety guardrails that a user easily discovered in
DeepSeek with simple adversarial prompts (5.5). In contrast, failures
in closed-source LLMs might be rooted in corporate opacity. We
see this in the high incidence of operational instability for Claude
(Section 4.2) and usability flaws like Gemini’s missing app icon in
Section 5.6. Importantly, users of Gemini, Mistral, and Claude all
reported that their feedback and support emails went unanswered.
This could violate foundational design needs for algorithmic ac-
countability advocated by HCI researchers, leaving users without
the procedural means to contest platform actions [17, 91]. All these
identified patterns show that an LLM’s technical design (e.g., li-
censing and distribution model) is not a background detail but a
primary determinant of the risks users might experience further.
6.3 Navigating the Utility-Risk Trade-offs of
Using LLM Chatbots
While the NIST’s AI RMF [ 5] focuses on mitigating risks during
the AI development, our findings show that users constantly make
trade-offs to achieve their goals of using LLM chatbots. For example,
the user experience of LLMs is defined by a constant negotiation be-
tween their utility and their risks. We identified three primary forms
this negotiation takes:pragmatic,coerced, andvoluntarytrade-offs.
The most common one is a pragmatic trade-off, where users ac-
cept functional unreliability in exchange for the utility of LLMs by
developing their own workarounds. This acceptance of the LLM
chatbot as a helpful but flawed tool is core to the user experience,
where users invest effort to steer it toward a useful outcome. This
is evident in Section 5.7, where users switch back and forth be-
tween different LLMs to manage risks. Prior HCI work has well
documented such strategies as workarounds that bypass specific
system flaws [28, 77, 96]. Extending this, our findings show that
for LLMs, these strategies have become a method for managing
the LLMs’ inherent unreliability, such as when they must “force
feed” context to LLMs to grasp their goals. Therefore, users adopt
a mental model of LLMs not as reliable agents, but as yet-to-be
uncooperative collaborators.
Second, the utility-risk negotiation is not always a fair choice;
users are often forced into coercive trade-offs skewed by platform
design. Our findings in Section 5.2 illustrate how users are com-
pelled to surrender personal data collection for the basic function-
ality of using LLM chatbots like Gemini. This manipulative design
offers a new perspective on the privacy paradox, where user be-
haviors appear to contradict their stated privacy concerns [ 76].
Our findings suggest that this is not a paradox of user irrational-
ity [4], but rather a direct result of flawed consent mechanisms
in the face of such a high-stakes choice [ 3, 37]. When the price
of privacy is the loss of essential features like chat history, users’
“choice” becomes functionally predetermined. This manipulation is
sometimes even more explicit, as when another user identified a
deceptive ChatGPT button as a dark pattern. Prior HCI work has
extensively documented how such deceptive patterns manipulate
user decision-making [40, 73]. Our work extends this by providing

Characterizing User-Reported Risks Across LLM chatbots
Table 3: A summary of user-reported risks across LLMs with open and closed-source technical designs.
Risk Category Closed-Source LLMs Open-Source LLMs
ChatGPT
 Gemini
 Claude
 Llama
 Mistral
 Qwen
 DeepSeek
Explainable &
Interpretable
§4.2 high report vol-
ume
Privacy §5.2 “Misuse of
User Data in Train-
ing”
§5.2 “Misuse of
User Data in Train-
ing”
§4.2 high report vol-
ume
Fair §5.3 “Demographic
Stereotyping”
§5.3 “Discrimina-
tory Treatment”
Safe §5.4 “Dangerous
Advice Provision”
§5.4 “Inappropriate
Content Genera-
tion”
Secure &
Resilient
§4.2 “Operational
Instability”
§4.2 high report vol-
ume
§5.5 “Jailbreaking
Vulnerabilities”
Accountable &
Transparent
§5.6 “Inadequate
Feedback Chan-
nels”
§5.6 “Inadequate
Feedback Chan-
nels”
§5.6 “Inadequate
Feedback Chan-
nels”
§4.2 high report vol-
ume
Valid &
Reliable
§5.7 “Factual Inva-
lidity”
§5.7 “Overconfi-
dent Outputs”
§5.7 “Task Compre-
hension Failures”
§4.2 Primary user
focus
§4.2 Primary user
focus
§4.2 Primary user
focus
evidence of how dark patterns are used in LLM chatbots, not just
for e-commerce, but to compel data surveillance for utility.
Finally, users engage in voluntary trade-offs, at times prioritizing
other benefits over the risks of opacity. Extending the existing goals
of Explainable AI, which has demonstrated how explanations can in-
crease user trust [81, 95] and support transparent decision-making
in high-stakes domains like clinical practice [19], our findings re-
veal two motivations behind users’ voluntary acceptance of opacity.
First, users make a practical choice for simplicity. As we found in
Section 5.1, users perceive that full explainability could become a
form of information overload [9] and that moderate levels of ex-
plainability can be more effective for building trust [55]. Second,
for creative tasks, users willingly accepted opacity by treating the
LLM chatbot’s emergent behavior as a feature rather than a flaw.
This suggests users adopt a relational mental model of the AI [66]
as a creative partner, viewing a technical explanation as something
that would diminish the product’s utility.
Understanding these trade-offs that define the post-deployment
use of LLM chatbots is important for bridging the gap between
system-centered risk management and the user’s experience. This
disconnect manifests as a social-technical gap, the divide between
societal needs and rigid technical limitations that cannot meet those
needs [2]. Our study reveals a new dimension of this gap for LLMs,
defined not by what technology can do, but by how users prioritize
mitigation for risks like Valid & Reliable and Accountable & Trans-
parent outputs over Privacy and Explainability & Interpretability,
as shown in Section 4.2. This provides a clear mandate for the next
AI development lifecycle: to understand the trade-offs that pro-
duce this risk hierarchy and design LLM chatbots where users are
not forced to sacrifice important human values like privacy and
transparency for basic functionality.
6.4 Design and Policy Implications for
Trustworthy LLMs in Use
Our findings highlight the gaps between LLM chatbots’ system-
centered risk and the user-centered experiences, requiring better
design and governance of LLM chatbots. We therefore argue for a
shift from a purely technical mitigation of risks to a user-centered
approach that supports users in navigating the risks.
(1) Acknowledge Negotiation for Reliability.Our findings
show that interacting with LLMs is not a simple input-output pro-
cess but a constant negotiation. Users develop ad-hoc workarounds
(Section 5.7). This suggests a design opportunity that, instead of
designing interfaces that assume a single LLM model, designers
should create, for example, a “meta-interface”that allows users to
easily compare responses from different models side-by-side. This
would formalize the workaround users have already invented.
(2) Mandate Meaningful User Agency to Ensure Fairness.
A LLM system cannot be trustworthy if it deceives users. Our
findings on “dark patterns” show how LLM chatbot design can
undermine user agency and privacy (Section 5.2). Both designers
and policymakers must move to decouple essential features from
privacy-invasive practices and mandate free choices of data sharing.
From a design perspective, chat history as a usability feature should
never be a reward for opting into data training; these should be
entirely separate controls. From a policy perspective, regulators
such as the U.S. FTC could classify the tying of core functionality
to data collection as a deceptive practice. Furthermore, our finding
that a user was unable to delete their data with a broken tool
demonstrates the need for an enforceable “right to be forgotten, ”
where users receive clear confirmation that their data has been
permanently removed.
(3) Contextualize Chatbot Behavior to Build Confidence
in Safety and Explainability.Building a trustworthy LLM sys-
tem requires acknowledging that risk is not absolute; it is highly
contextual. The agreeableness of an LLM chatbot can shift from

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
a helpful feature to a dangerous one that reinforces negative be-
havior in a mental health context (Section 5.4). Similarly, users’
need for explainability becomes important only in high-stakes situ-
ations, while in creative contexts, they may prefer opacity (Section
5.1). This calls for moving beyond one-size-fits-all safety filters and
transparency reports to an “adaptive governance. ” For example, de-
signers could implement adaptive explainability, where the system
automatically provides a “chain-of-thought” or source links when
it detects a high-stakes query (e.g., medical or financial topics) but
remains concise for creative tasks. Likewise, safety protocols could
suppress an LLM model’s agreeableness when conversations veer
into a sensitive domain. Policy, in turn, can mandate that companies
develop and disclose their strategies for such context-aware risk
mitigation, moving to more sophisticated safety systems.
7 LIMITATIONS AND FUTURE WORK
Our study has three limitations. First, our analysis is based on Reddit
data. While this provides a large-scale user experience data, Red-
dit’s demographics do not represent all users of LLM chatbots and
may underrepresent perspectives from older adults, non-English
speakers, or individuals in different global contexts. Future work
should triangulate our findings by analyzing discussions on other
platforms or by employing methods like surveys and interviews to
reach a broader population. Second, while validated against human
judgment, our LLM-based annotation and BERTopic modeling for
data analysis have inherent limitations. Despite careful prompt
engineering and manual, qualitative examination of “risk types,
we may miss nuances or introduce unforeseen biases. Future work
could explore using different models for annotation or employing
large-scale human coding to provide a comparative analytical lens.
Third, our data collection relies on the Reddit API via PRAW, which
is limited to returning the top posts for a given query. This techni-
cal constraint may introduce a recency or popularity bias into our
dataset, as older or less-upvoted discussions are excluded. Future re-
search could mitigate this by using paid audit tools like Brandwatch
to collect more comprehensive data on user discussions.
8 CONCLUSIONS
This study provides a large-scale empirical characterization of the
risks users report with major LLM chatbots, grounding AI risk
management in the lived experiences of users. By constructing an
interactive knowledge graph, we map the complex relationships
among LLM chatbots, risk taxonomies, and user experiences. This
methodological framework grounds risk assessment in direct ev-
idence of user-reported risks. Our findings show that the most
prominent risks perceived by users are not the nuanced ethical
issues frequently highlighted in the technical literature, but rather
fundamental performance failures within the “Valid and Reliable”
category. Cross-chatbot comparisons further reveal statistically sig-
nificant “risk fingerprints, ” indicating that concerns around safety,
privacy, and security differ substantially across LLM chatbots. Less
frequent risks like “Explainability” and “Privacy” manifest as user
trade-offs, while more common risks like “Fairness” and “Safety”
are experienced as direct and personal harms. To promote trustwor-
thy LLMs in use, these results underscore the need for designers,
developers, and policymakers to realign risk mitigation toward
the risks most salient to users, while also addressing harms that
currently escape user attention.
References
[1] Abubakar Abid, Maheen Farooqi, and James Zou. 2021. Persistent anti-muslim
bias in large language models. InProceedings of the 2021 AAAI/ACM Conference
on AI, Ethics, and Society. 298–306.
[2] Mark S Ackerman. 2000. The intellectual challenge of CSCW: the gap between
social requirements and technical feasibility.Human–Computer Interaction15,
2-3 (2000), 179–203.
[3] Alessandro Acquisti, Laura Brandimarte, and George Loewenstein. 2015. Privacy
and human behavior in the age of information.Science347, 6221 (2015), 509–
514.
[4] Alessandro Acquisti and Jens Grossklags. 2005. Privacy and rationality in
individual decision making.IEEE security & privacy3, 1 (2005), 26–33.
[5] NIST AI. 2023. Artificial intelligence risk management framework (AI RMF 1.0).
URL: https://nvlpubs. nist. gov/nistpubs/ai/nist. ai(2023), 100–1.
[6] Rohan Ajwani, Shashidhar Reddy Javaji, Frank Rudzicz, and Zining Zhu. 2024.
LLM-generated black-box explanations can be adversarially helpful.arXiv
preprint arXiv:2405.06800(2024).
[7] Daniel Alexander Alber, Zihao Yang, Anton Alyakin, Eunice Yang, Sumedha
Rai, Aly A Valliani, Jeff Zhang, Gabriel R Rosenbaum, Ashley K Amend-Thomas,
David B Kurland, et al. 2025. Medical large language models are vulnerable to
data-poisoning attacks.Nature Medicine31, 2 (2025), 618–626.
[8] Shahad Alkamli and Reham Alabduljabbar. 2024. Understanding privacy con-
cerns in ChatGPT: A data-driven approach with LDA topic modeling.Heliyon
10, 20 (2024).
[9] Andrew Anderson, Jonathan Dodge, Amrita Sadarangani, Zoe Juozapaitis, Evan
Newman, Jed Irvine, Souti Chattopadhyay, Matthew Olson, Alan Fern, and
Margaret Burnett. 2020. Mental models of mere mortals with explanations of
reinforcement learning.ACM Transactions on Interactive Intelligent Systems
(TiiS)10, 2 (2020), 1–37.
[10] Evan Bailyn. 2025. Top Generative AI Chatbots by Market Share – August
2025. https://firstpagesage.com/reports/top-generative-ai-chatbots/. Accessed:
September 5, 2025.
[11] Yonatan Belinkov and James Glass. 2019. Analysis methods in neural lan-
guage processing: A survey.Transactions of the Association for Computational
Linguistics7 (2019), 49–72.
[12] Emily M Bender, Timnit Gebru, Angelina McMillan-Major, and Shmargaret
Shmitchell. 2021. On the dangers of stochastic parrots: Can language models be
too big?. InProceedings of the 2021 ACM conference on fairness, accountability,
and transparency. 610–623.
[13] Federico Bianchi and James Zou. 2024. Large language models are vulnerable
to bait-and-switch attacks for generating harmful content.arXiv preprint
arXiv:2402.13926(2024).
[14] Noémi Bontridder and Yves Poullet. 2021. The role of artificial intelligence in
disinformation.Data & Policy3 (2021), e32.
[15] Michael Bostock, Vadim Ogievetsky, and Jeffrey Heer. 2011. D3Data-Driven
Documents.IEEE Transactions on Visualization and Computer Graphics17, 12
(2011), 2301–2309. doi:10.1109/TVCG.2011.185
[16] Samuel R Bowman. 2024. Eight things to know about large language models.
Critical AI2, 2 (2024).
[17] Anna Brown, Alexandra Chouldechova, Emily Putnam-Hornstein, Andrew
Tobin, and Rhema Vaithianathan. 2019. Toward algorithmic accountability
in public services: A qualitative study of affected community perspectives on
algorithmic decision-making in child welfare services. InProceedings of the 2019
CHI Conference on Human Factors in Computing Systems. 1–12.
[18] Nicholas Carlini, Florian Tramer, Eric Wallace, Matthew Jagielski, Ariel Herbert-
Voss, Katherine Lee, Adam Roberts, Tom Brown, Dawn Song, Ulfar Erlingsson,
et al. 2021. Extracting training data from large language models. In30th USENIX
security symposium (USENIX Security 21). 2633–2650.
[19] Rich Caruana, Yin Lou, Johannes Gehrke, Paul Koch, Marc Sturm, and Noemie
Elhadad. 2015. Intelligible models for healthcare: Predicting pneumonia risk
and hospital 30-day readmission. InProceedings of the 21th ACM SIGKDD inter-
national conference on knowledge discovery and data mining. 1721–1730.
[20] Qijia Chen, Seyed Mahed Mousavi, Giuseppe Riccardi, and Giulio Jacucci. 2025.
Investigating the Use and Perception of Blocking Feature in Social Virtual
Reality Spaces: A Study on Discussion Forums.Proceedings of the ACM on
Human-Computer Interaction9, 2 (2025), 1–19.
[21] Su-Yen Chen, HY Kuo, and Shu-Hao Chang. 2024. Perceptions of ChatGPT
in healthcare: usefulness, trust, and risk.Frontiers in Public Health12 (2024),
1457131.
[22] Zenan Chen and Jason Chan. 2024. Large language model in creative work:
The role of collaboration modality and user expertise.Management Science70,
12 (2024), 9101–9117.

Characterizing User-Reported Risks Across LLM chatbots
[23] Avishek Choudhury and Hamid Shamszare. 2023. Investigating the impact of
user trust on the adoption and use of ChatGPT: survey analysis.Journal of
Medical Internet Research25 (2023), e47184.
[24] Gabriele Civitarese, Michele Fiori, Priyankar Choudhary, and Claudio Bettini.
2025. Large language models are zero-shot recognizers for activities of daily
living.ACM Transactions on Intelligent Systems and Technology16, 4 (2025),
1–32.
[25] Elizabeth Clark, Tal August, Sofia Serrano, Nikita Haduong, Suchin Gururangan,
and Noah A Smith. 2021. All that’s’ human’is not gold: Evaluating human
evaluation of generated text.arXiv preprint arXiv:2107.00061(2021).
[26] Ameet Deshpande, Vishvak Murahari, Tanmay Rajpurohit, Ashwin Kalyan, and
Karthik Narasimhan. 2023. Toxicity in chatgpt: Analyzing persona-assigned
language models.arXiv preprint arXiv:2304.05335(2023).
[27] Jayson L. Dibble, Tilo Hartmann, and Sarah F. Rosaen. 2016. Parasocial In-
teraction and Parasocial Relationship: Conceptual Clarification and a Critical
Assessment of Measures.Human Communication Research42, 1 (1 2016), 21–44.
doi:10.1111/HCRE.12063
[28] Hyo Jin Do, Ha-Kyung Kong, Pooja Tetali, Jaewook Lee, and Brian P Bailey.
2023. To Err is AI: imperfect interventions and repair in a conversational agent
facilitating group chat discussions.Proceedings of the ACM on Human-Computer
Interaction7, CSCW1 (2023), 1–23.
[29] Finale Doshi-Velez and Been Kim. 2017. Towards a rigorous science of inter-
pretable machine learning.arXiv preprint arXiv:1702.08608(2017).
[30] ET Online. 2025. Top AI tools of 2025: Is ChatGPT still leading or is Gemini,
Grok, DeepSeek taking over? https://economictimes.indiatimes.com/news/
international/us/top-ai-tools-of-2025-is-chatgpt-still-leading-or-is-gemini-
grok-deepseek-taking-over/articleshow/123552050.cms.
[31] ChatGPT Europol. 2023. The impact of large language models on law enforce-
ment.Europa. Eu(2023).
[32] Jessica L. Feuston, Alex S. Taylor, and Anne Marie Piper. 2020. Conformity
of Eating Disorders through Content Moderation.Proceedings of the ACM on
Human-Computer Interaction4, CSCW1 (5 2020). doi:10.1145/3392845
[33] Casey Fiesler. 2019. Ethical considerations for research involving (speculative)
public data.Proceedings of the ACM on Human-Computer Interaction3, GROUP
(2019), 1–13.
[34] Isabel O Gallegos, Ryan A Rossi, Joe Barrow, Md Mehrab Tanjim, Sungchul Kim,
Franck Dernoncourt, Tong Yu, Ruiyi Zhang, and Nesreen K Ahmed. 2024. Bias
and fairness in large language models: A survey.Computational Linguistics50,
3 (2024), 1097–1179.
[35] Shubham Gandhi, Manasi Patwardhan, Lovekesh Vig, and Gautam Shroff. 2024.
Budgetmlagent: A cost-effective llm multi-agent system for automating machine
learning tasks. InProceedings of the 4th International Conference on AI-ML
Systems. 1–9.
[36] Samuel Gehman, Suchin Gururangan, Maarten Sap, Yejin Choi, and Noah A
Smith. 2020. Realtoxicityprompts: Evaluating neural toxic degeneration in
language models.arXiv preprint arXiv:2009.11462(2020).
[37] Nina Gerber, Paul Gerber, and Melanie Volkamer. 2018. Explaining the privacy
paradox: A systematic review of literature investigating privacy attitude and
behavior.Computers & security77 (2018), 226–261.
[38] Josh A Goldstein, Girish Sastry, Micah Musser, Renee DiResta, Matthew Gentzel,
and Katerina Sedova. 2023. Generative language models and automated influ-
ence operations: Emerging threats and potential mitigations.arXiv preprint
arXiv:2301.042461 (2023).
[39] Maarten Grootendorst. 2022. BERTopic: Neural topic modeling with a class-
based TF-IDF procedure.arXiv preprint arXiv:2203.05794(2022).
[40] Johanna Gunawan, Amogh Pradeep, David Choffnes, Woodrow Hartzog, and
Christo Wilson. 2021. A comparative study of dark patterns across web and
mobile modalities.Proceedings of the ACM on Human-Computer Interaction5,
CSCW2 (2021), 1–29.
[41] Emma Harvey, Allison Koenecke, and Rene F Kizilcec. 2025. " Don’t Forget the
Teachers": Towards an Educator-Centered Understanding of Harms from Large
Language Models in Education. InProceedings of the 2025 CHI Conference on
Human Factors in Computing Systems. 1–19.
[42] Ilka Hein and Sarah Diefenbach. 2025. Towards a Comprehensive View on Tech-
nology Transparency: A Cross-Technology Investigation of Psychological and
Design Factors Around Users’ Transparency Need and Perception.International
Journal of Human–Computer Interaction(2025), 1–18.
[43] Lyndsey Hipgrave, Jessie Goldie, Simon Dennis, and Amanda Coleman. 2025.
Balancing risks and benefits: clinicians’ perspectives on the use of generative
AI chatbots in mental healthcare.Frontiers in Digital Health7 (2025), 1606291.
[44] Lei Huang, Weijiang Yu, Weitao Ma, Weihong Zhong, Zhangyin Feng, Haotian
Wang, Qianglong Chen, Weihua Peng, Xiaocheng Feng, Bing Qin, et al. 2025.
A survey on hallucination in large language models: Principles, taxonomy,
challenges, and open questions.ACM Transactions on Information Systems43, 2
(2025), 1–55.
[45] Lujain Ibrahim, Luc Rocher, and Ana Valdivia. 2024. Characterizing and mod-
eling harms from interactions with design patterns in AI interfaces.arXiv
preprint arXiv:2404.11370(2024).
[46] Sarthak Jain and Byron C Wallace. 2019. Attention is not explanation.arXiv
preprint arXiv:1902.10186(2019).
[47] Ammar Abdulrahman Jairoun, Sabaa Saleh Al-Hemyari, Moyad Shahwan, Tariq
Al-Qirim, and Monzer Shahwan. 2024. Benefit–risk assessment of chatgpt appli-
cations in the field of diabetes and metabolic illnesses: a qualitative study.Clini-
cal Medicine Insights: Endocrinology and Diabetes17 (2024), 11795514241235514.
[48] Ziwei Ji, Nayeon Lee, Rita Frieske, Tiezheng Yu, Dan Su, Yan Xu, Etsuko Ishii,
Ye Jin Bang, Andrea Madotto, and Pascale Fung. 2023. Survey of hallucination
in natural language generation.ACM computing surveys55, 12 (2023), 1–38.
[49] Ziwei Ji, Tiezheng Yu, Yan Xu, Nayeon Lee, Etsuko Ishii, and Pascale Fung.
2023. Towards mitigating LLM hallucination via self reflection. InFindings of
the Association for Computational Linguistics: EMNLP 2023. 1827–1843.
[50] Yongnam Jung, Cheng Chen, Eunchae Jang, and S Shyam Sundar. 2024. Do we
trust Chatgpt as much as Google search and Wikipedia?. InExtended Abstracts
of the CHI Conference on Human Factors in Computing Systems. 1–9.
[51] Nikhil Kandpal, Eric Wallace, and Colin Raffel. 2022. Deduplicating training
data mitigates privacy risks in language models. InInternational Conference on
Machine Learning. PMLR, 10697–10707.
[52] Sunnie SY Kim, Q Vera Liao, Mihaela Vorvoreanu, Stephanie Ballard, and Jen-
nifer Wortman Vaughan. 2024. " I’m Not Sure, But... ": Examining the Impact of
Large Language Models’ Uncertainty Expression on User Reliance and Trust.
InProceedings of the 2024 ACM conference on fairness, accountability, and trans-
parency. 822–835.
[53] Yoonsu Kim, Jueon Lee, Seoyoung Kim, Jaehyuk Park, and Juho Kim. 2024.
Understanding users’ dissatisfaction with chatgpt responses: Types, resolving
tactics, and the effect of knowledge level. InProceedings of the 29th International
Conference on Intelligent User Interfaces. 385–404.
[54] Thomas C King, Nikita Aggarwal, Mariarosaria Taddeo, and Luciano Floridi.
2020. Artificial intelligence crime: An interdisciplinary analysis of foreseeable
threats and solutions.Science and engineering ethics26, 1 (2020), 89–120.
[55] René F Kizilcec. 2016. How much information? Effects of transparency on trust
in an algorithmic interface. InProceedings of the 2016 CHI conference on human
factors in computing systems. 2390–2395.
[56] Charlotte Kobiella, Yarhy Said Flores López, Franz Waltenberger, Fiona Draxler,
and Albrecht Schmidt. 2024. " If the machine is as good as me, then what use
am I?"–How the use of ChatGPT changes young professionals’ perception of
productivity and accomplishment. InProceedings of the 2024 CHI Conference on
Human Factors in Computing Systems. 1–16.
[57] Hadas Kotek, Rikker Dockum, and David Sun. 2023. Gender bias and stereo-
types in large language models. InProceedings of the ACM collective intelligence
conference. 12–24.
[58] Hannah R Lawrence, Renee A Schneider, Susan B Rubin, Maja J Matarić, Daniel J
McDuff, and Megan Jones Bell. 2024. The opportunities and risks of large
language models in mental health.JMIR Mental Health11, 1 (2024), e59479.
[59] Joseph Lee, Tianqi Shang, Jae Young Baik, Duy Duong-Tran, Shu Yang, Lingyao
Li, and Li Shen. 2025. Investigating LLMs in Clinical Triage: Promising Capabil-
ities, Persistent Intersectional Biases.arXiv preprint arXiv:2504.16273(2025).
[60] Min Kyung Lee, Anuraag Jain, Hae J.I.N. Cha, Shashank Ojha, and Daniel Kusbit.
2019. Procedural justice in algorithmic fairness: Leveraging transparency and
outcome control for fair algorithmic mediation.Proceedings of the ACM on
Human-Computer Interaction3, CSCW (11 2019), 26. doi:10.1145/3359284
[61] Min Kyung Lee, Ji Tae Kim, and Leah Lizarondo. 2017. A Human-Centered
Approach to Algorithmic Services: Considerations for Fair and Motivating
Smart Community Service Management that Allocates Donations to Non-Profit
Organizations.Proceedings of the 2017 CHI Conference on Human Factors in
Computing Systems(2017). doi:10.1145/3025453
[62] Lingyao Li, Runlong Yu, Qikai Hu, Bowei Li, Min Deng, Yang Zhou, and Xi-
aowei Jia. 2025. From Pixels to Places: A Systematic Benchmark for Evaluat-
ing Image Geolocalization Ability in Large Language Models.arXiv preprint
arXiv:2508.01608(2025).
[63] Lingyao Li, Jiayan Zhou, Zhenxiang Gao, Wenyue Hua, Lizhou Fan, Huizi Yu,
Loni Hagen, Yongfeng Zhang, Themistocles L Assimes, Libby Hemphill, et al.
2024. A scoping review of using large language models (LLMs) to investigate
electronic health records (EHRs).arXiv preprint arXiv:2405.03066(2024).
[64] Megan Li, Wendy Bickersteth, Ningjing Tang, Jason Hong, Lorrie Cranor, Hong
Shen, and Hoda Heidari. 2025. A Closer Look at the Existing Risks of Generative
AI: Mapping the Who, What, and How of Real-World Incidents.arXiv preprint
arXiv:2505.22073(2025).
[65] Tianshi Li, Sauvik Das, Hao-Ping Lee, Dakuo Wang, Bingsheng Yao, and Zhip-
ing Zhang. 2024. Human-centered privacy research in the age of large language
models. InExtended Abstracts of the CHI Conference on Human Factors in Com-
puting Systems. 1–4.
[66] Q Vera Liao and Jennifer Wortman Vaughan. 2023. Ai transparency in the age
of llms: A human-centered research roadmap.arXiv preprint arXiv:2306.01941
10 (2023).
[67] Aristidis Likas, Nikos Vlassis, and Jakob J Verbeek. 2003. The global k-means
clustering algorithm.Pattern recognition36, 2 (2003), 451–461.

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
[68] Bowen Liu, Boao Xiao, Xutong Jiang, Siyuan Cen, Xin He, and Wanchun Dou.
2023. Adversarial Attacks on Large Language Model-Based System and Mit-
igating Strategies: A Case Study on ChatGPT.Security and Communication
Networks2023, 1 (2023), 8691095.
[69] Minqian Liu, Zhiyang Xu, Xinyi Zhang, Heajun An, Sarvech Qadir, Qi Zhang,
Pamela J Wisniewski, Jin-Hee Cho, Sang Won Lee, Ruoxi Jia, et al. 2025. LLM
can be a dangerous persuader: Empirical study of persuasion safety in large
language models.arXiv preprint arXiv:2504.10430(2025).
[70] Renkai Ma and Yubo Kou. 2021. “How advertiser-friendly is my video?”: YouTu-
ber’s Socioeconomic Interactions with Algorithmic Content Moderation.PACM
on Human Computer Interaction5, CSCW2 (2021), 1–26. doi:10.1145/3479573
[71] Renkai Ma, Yue You, Xinning Gui, and Yubo Kou. 2023. How Do Users Experi-
ence Moderation?: A Systematic Literature Review.PACM on Human-Computer
Interaction, Vol. 7, No. CSCW27, CSCW2 (2023). doi:10.1145/3610069
[72] Rhodes Massenon, Ishaya Gambo, Javed Ali Khan, Christopher Agbonkhese, and
Ayed Alwadain. 2025. ” My AI is Lying to Me”: User-reported LLM hallucinations
in AI mobile apps reviews.Scientific Reports15, 1 (2025), 30397.
[73] Arunesh Mathur, Gunes Acar, Michael J Friedman, Eli Lucherini, Jonathan
Mayer, Marshini Chetty, and Arvind Narayanan. 2019. Dark patterns at scale:
Findings from a crawl of 11K shopping websites.Proceedings of the ACM on
human-computer interaction3, CSCW (2019), 1–32.
[74] Leland McInnes, John Healy, and James Melville. 2018. Umap: Uniform man-
ifold approximation and projection for dimension reduction.arXiv preprint
arXiv:1802.03426(2018).
[75] Jesse G Meyer, Ryan J Urbanowicz, Patrick CN Martin, Karen O’Connor,
Ruowang Li, Pei-Chen Peng, Tiffani J Bright, Nicholas Tatonetti, Kyoung Jae
Won, Graciela Gonzalez-Hernandez, et al. 2023. ChatGPT and large language
models in academia: opportunities and challenges.BioData mining16, 1 (2023),
20.
[76] Patricia A Norberg, Daniel R Horne, and David A Horne. 2007. The privacy
paradox: Personal information disclosure intentions versus behaviors.Journal
of consumer affairs41, 1 (2007), 100–126.
[77] Savvas Petridis, Nicholas Diakopoulos, Kevin Crowston, Mark Hansen, Keren
Henderson, Stan Jastrzebski, Jeffrey V Nickerson, and Lydia B Chilton. 2023.
Anglekindling: Supporting journalistic angle ideation with large language mod-
els. InProceedings of the 2023 CHI conference on human factors in computing
systems. 1–16.
[78] PRAW Development Team. 2024.PRA W: The Python Reddit API Wrapper. https:
//github.com/praw-dev/praw
[79] Nicholas Proferes, Naiyan Jones, Sarah Gilbert, Casey Fiesler, and Michael
Zimmer. 2021. Studying reddit: A systematic overview of disciplines, approaches,
methods, and ethics.Social Media+ Society7, 2 (2021), 20563051211019004.
[80] PYMNTS. 2025. Remember DeepSeek? Many Adopt Its AI Models Despite
Security Concerns. https://www.pymnts.com/artificial-intelligence-2/2025/
remember-deepseek-many-adopt-its-ai-models-despite-security-concerns/.
[81] Marco Tulio Ribeiro, Sameer Singh, and Carlos Guestrin. 2016. " Why should
i trust you?" Explaining the predictions of any classifier. InProceedings of the
22nd ACM SIGKDD international conference on knowledge discovery and data
mining. 1135–1144.
[82] K Rooney. 2025. OpenAI tops 400 million users despite DeepSeek’s emer-
gence.CNBC. Available online: https://www. cnbc. com/2025/02/20/openai-tops-
400-million-users-despite-deepseeks-emergence. html (accessed on 10 March 2025)
(2025).
[83] Sentence-Transformers. 2021. all-mpnet-base-v2. https://huggingface.co/
sentence-transformers/all-mpnet-base-v2.
[84] Dong Shu, Chong Zhang, Mingyu Jin, Zihao Zhou, and Lingyao Li. 2025. Attack-
eval: How to evaluate the effectiveness of jailbreak attacking on large language
models.ACM SIGKDD Explorations Newsletter27, 1 (2025), 10–19.
[85] Xin Sun, Yunjie Liu, Jan De Wit, Jos A Bosch, and Zhuying Li. 2024. Trust by
interface: How different user interfaces shape human trust in health information
from large language models. InExtended Abstracts of the CHI Conference on
Human Factors in Computing Systems. 1–7.
[86] Xiangru Tang, Qiao Jin, Kunlun Zhu, Tongxin Yuan, Yichi Zhang, Wangchun-
shu Zhou, Meng Qu, Yilun Zhao, Jian Tang, Zhuosheng Zhang, et al . 2024.
Prioritizing safeguarding over autonomy: Risks of llm agents for science.arXiv
preprint arXiv:2402.04247(2024).
[87] Tara Templin, Sophia Fort, Prasanna Padmanabham, Pratyush Seshadri, Ram
Rimal, Junier Oliva, Kristin Hassmiller Lich, Sean Sylvia, and Nasa Sinnott-
Armstrong. 2025. Framework for bias evaluation in large language models in
healthcare settings.npj Digital Medicine8, 1 (2025), 414.
[88] Runchu Tian, Yining Ye, Yujia Qin, Xin Cong, Yankai Lin, Yinxu Pan, Yesai Wu,
Haotian Hui, Weichuan Liu, Zhiyuan Liu, et al. 2024. Debugbench: Evaluating
debugging capability of large language models.arXiv preprint arXiv:2401.04621
(2024).
[89] Trishita Tiwari, Avraham Klausner, Mikhail Andreev, Ari Trachtenberg, and
Arkady Yerukhimovich. 2019. Location leakage from network access patterns.
In2019 IEEE Conference on Communications and Network Security (CNS). IEEE,
214–222.
[90] Tom R. Tyler. 1988. What Is Procedural Justice?: Criteria Used by Citizens to
Assess the Fairness of Legal Procedures.Law & Society Review(1988).
[91] Michael Veale, Max Van Kleek, and Reuben Binns. 2018. Fairness and ac-
countability design needs for algorithmic support in high-stakes public sector
decision-making. InProceedings of the 2018 chi conference on human factors in
computing systems. 1–14.
[92] Sandra Wachter, Brent Mittelstadt, and Chris Russell. 2024. Do large language
models have a legal duty to tell the truth?Royal Society Open Science11, 8
(2024), 240197.
[93] Francesco Walker, Matteo Favetta, Linde Hasker, and Richard Walker. 2024.
They prefer humans! Experimental measurement of student trust in ChatGPT.
InExtended Abstracts of the CHI Conference on Human Factors in Computing
Systems. 1–7.
[94] Jiaqi Wang, Hanqi Jiang, Yiheng Liu, Chong Ma, Xu Zhang, Yi Pan, Mengyuan
Liu, Peiran Gu, Sichen Xia, Wenjun Li, et al. 2024. A comprehensive review of
multimodal large language models: Performance and challenges across different
tasks.arXiv preprint arXiv:2408.01319(2024).
[95] Katharina Weitz, Dominik Schiller, Ruben Schlagowski, Tobias Huber, and
Elisabeth André. 2019. " Do you trust me?" Increasing user-trust by integrating
virtual agents in explainable AI interaction design. InProceedings of the 19th
ACM International Conference on Intelligent Virtual Agents. 7–9.
[96] Joel Wester, Tim Schrills, Henning Pohl, and Niels Van Berkel. 2024. “As an
AI language model, I cannot”: Investigating LLM Denials of User Requests. In
Proceedings of the 2024 CHI Conference on Human Factors in Computing Systems.
1–14.
[97] Allison Woodruff, Sarah E Fox, Steven Rousso-Schindler, and Jeff Warshaw. 2018.
A Qualitative Exploration of Perceptions of Algorithmic Fairness.Proceedings
of the 2018 CHI Conference on Human Factors in Computing Systems(2018).
doi:10.1145/3173574
[98] Tongshuang Wu, Michael Terry, and Carrie Jun Cai. 2022. Ai chains: Transpar-
ent and controllable human-ai interaction by chaining large language model
prompts. InProceedings of the 2022 CHI conference on human factors in computing
systems. 1–22.
[99] Junjie Xiong, Changjia Zhu, Shuhang Lin, Chong Zhang, Yongfeng Zhang, Yao
Liu, and Lingyao Li. 2025. Invisible Prompts, Visible Threats: Malicious Font
Injection in External Resources for Large Language Models.arXiv preprint
arXiv:2505.16957(2025).
[100] Qian Yang, Jin Xu, Wenrui Liu, Yunfei Chu, Ziyue Jiang, Xiaohuan Zhou, Yi-
chong Leng, Yuanjun Lv, Zhou Zhao, Chang Zhou, et al . 2024. Air-bench:
Benchmarking large audio-language models via generative comprehension.
arXiv preprint arXiv:2402.07729(2024).
[101] Zonghan Yang, An Liu, Zijun Liu, Kaiming Liu, Fangzhou Xiong, Yile Wang,
Zeyuan Yang, Qingyuan Hu, Xinrui Chen, Zhenhe Zhang, et al. 2024. Towards
unified alignment between agents, humans, and environment.arXiv preprint
arXiv:2402.07744(2024).
[102] Huizi Yu, Lizhou Fan, Lingyao Li, Jiayan Zhou, Zihui Ma, Lu Xian, Wenyue Hua,
Sijia He, Mingyu Jin, Yongfeng Zhang, et al. 2024. Large language models in
biomedical and health informatics: a review with bibliometric analysis.Journal
of healthcare informatics research8, 4 (2024), 658–711.
[103] Hye Sun Yun and Timothy Bickmore. 2025. Framing Health Information: The
Impact of Search Methods and Source Types on User Trust and Satisfaction in
the Age of LLMs. InProceedings of the Extended Abstracts of the CHI Conference
on Human Factors in Computing Systems. 1–7.
[104] Jizhi Zhang, Keqin Bao, Yang Zhang, Wenjie Wang, Fuli Feng, and Xiangnan
He. 2023. Is chatgpt fair for recommendation? evaluating fairness in large
language model recommendation. InProceedings of the 17th ACM Conference
on Recommender Systems. 993–999.
[105] Renwen Zhang, Han Li, Han Meng, Jinyuan Zhan, Hongyuan Gan, and Yi-
Chieh Lee. 2025. The dark side of ai companionship: A taxonomy of harmful
algorithmic behaviors in human-ai relationships. InProceedings of the 2025 CHI
Conference on Human Factors in Computing Systems. 1–17.
[106] Zhiping Zhang, Michelle Jia, Hao-Ping Lee, Bingsheng Yao, Sauvik Das, Ada
Lerner, Dakuo Wang, and Tianshi Li. 2024. “It’s a Fair Game”, or Is It? Examining
How Users Navigate Disclosure Risks and Benefits When Using LLM-Based
Conversational Agents. InProceedings of the 2024 CHI Conference on Human
Factors in Computing Systems. 1–26.
[107] Haiyan Zhao, Hanjie Chen, Fan Yang, Ninghao Liu, Huiqi Deng, Hengyi Cai,
Shuaiqiang Wang, Dawei Yin, and Mengnan Du. 2024. Explainability for large
language models: A survey.ACM Transactions on Intelligent Systems and Tech-
nology15, 2 (2024), 1–38.
[108] Caleb Ziems, William Held, Omar Shaikh, Jiaao Chen, Zhehao Zhang, and Diyi
Yang. 2024. Can large language models transform computational social science?
Computational Linguistics50, 1 (2024), 237–291.

Characterizing User-Reported Risks Across LLM chatbots
Table 4: Information Extraction and Coding Examples
Original Reddit Post Information Extraction
claude is dope for modern nextjs stack.
gemini enforcing old libraries is terrible
to use. (gemini is so dumb it breaks code
that use newer than 1.5 models). openai
o3 solved most of problems gemini and
claude failed to solve. r1 is too slow for
me to use. v3 is too dumb. I hope opus 4
or similar big model from anthropic will
appear soon
LLM chatbot:Gemini
NIST Category:Valid and Reliable
Risk Type:Incompatibility with newer
models causing code breakage
Quote UserExperience:“Gemini is so
dumb it breaks code that use newer than
1.5 models”
Yep. I use it daily, shoving large code-
bases in it and never get rate limited or
anything. The one downside is, you’re
granting them permission to train on
*anything* you give gemini to analyze,
which they will do. Only the paid version
offers "no training on your data".
LLM Chatbot:Gemini
NIST category:Privacy
Risk Type:Unauthorized training on
user data
Quote UserExperience:“You’re grant-
ing them permission to train on *any-
thing* you give gemini to analyze, which
they will do”
Chat GPT was the first so people treat
like they do the Iphone and Android. ev-
erything is a team nowadays and if it
isn’t YOUR team then it is trash.
LLM Chatbot:GPT
NIST category:Fair
Risk Type:Tribalism or team bias
Quote User Experience:“Everything
is a team nowadays and if it isn’t YOUR
team then it is tras‘’
Except there’s some argument that Ope-
nAI engaged in massive copyright in-
fringement to get their training data.
Since the output of OpenAI’s models is
computer generated there is no copyright
and deepseek using it for their model is
actually perfectly clean as far as copy-
right goes.
LLM Chatbot:Deepseek
NIST Category:Accountable and Trans-
parent
Risk Type:Potential copyright concerns
in model usage
Quote User Experience:“Deepseek us-
ing it for their model is actually perfectly
clean as far as copyright goes. ”
Nah it is censored and even the Llama
distilled is censored. Just not as tightly.
LLM Chatbot:Llama
NIST Category:Safe
Risk Type:Content censorship
Quote User Experience:“Nah it is cen-
sored and even the Llama distilled is cen-
sored. Just not as tightly. ”
If I could ask one question it would be
how are you going to persuade compa-
nies that data you hold is safe from be-
ing breached out? I work for big govern-
ment body and essentially no one wants
to touch OpenAI due to concerns about
IP and leaked data in the past like with
Samsungs superconductors.
LLM Chatbot:GPT
NIST Category:Secure and Resilient
Risk Type:Data breach risk
Quote User Experience:“How are you
going to persuade companies that data
you hold is safe from being breached
out?”
According to GPT i have IQ 180-200 but
IQ is not even good measure for my intel-
lect :-) That said we were really talking
about some egghead level stuff and I man-
aged to outpace it few times.
LLM Chatbot:GPT
NIST Category:Explainable and Inter-
pretable
Risk Type:Overestimation of capabili-
ties
Quote User Experience:“According to
GPT i have IQ 180-200 but IQ is not even
good measure for my intellect :-)”
A Top-down Methods of Information
Extraction and Coding Examples
To illustrate our top-down coding method, Table 4 provides concrete
examples of how user comments were systematically coded into
our four analytical dimensions.
B Topic Clustering Results
Tables 5 through 12 present the detailed annotation codebook de-
rived from our bottom-up topic modeling and clustering analysis.
These are organized according to the seven NIST AI RMF categories,
presented in the same sequence as our RQ2 findings, from the least
to the most frequently reported. Each table details the thematic
clusters that emerged from the user-generated data, the specific
subtheme names within each cluster, and their corresponding share
of the total user-reported risks across our entire dataset.
Table 5: User-Reported Risks of Explainability & Inter-
pretability
Primary Theme / Subtheme Name Total Share (%)
Uninterpretable Output Meaning 0.63%
The “black box” nature of how LLMs output information.
Incomprehensible AI Cognition 0.20%
Ambiguous Output 0.19%
Difficulty in Understanding Output 0.11%
Lack of Interpretability 0.08%
Unexplainable Generated Code 0.05%
Unexplainable Decision-Making Process 0.61%
Inability to understand how the LLM arrives at a specific output.
Opaque Reasoning 0.21%
Unclear Reasoning 0.13%
Lack of Reasoning Transparency 0.11%
Simplification or Overexplanation 0.09%
Unclear Explanation 0.07%
Explainable and Interpretable Total 1.23%
Table 6: User-Reported Risks of Privacy
Primary Theme / Subtheme Name Total Share (%)
Uncontrolled Data Access and Exposure 1.92%
The LLM can become a conduit for leaking private information.
Unauthorized Data Collection 0.46%
Unintentional Exposure of Confidential Information 0.37%
Unauthorized Access 0.25%
Memory Privacy 0.24%
Unauthorized Access to User Data 0.20%
Uncontrolled Information Disclosure 0.12%
Geolocation Data Privacy Risks 0.10%
Data Leakage Through Misuse 0.10%
Unauthorized Data Sharing to Externals 0.07%
Inadequate Data Governance Practices 1.38%
Failures in how user data is managed throughout its lifecycle.
Misuse of User Data in Training 0.35%
Data Retention Risks 0.27%
Profiling Risks 0.19%
Privacy Risks in Conversation Histories 0.15%
Unauthorized Data Sharing in LLM Chatting 0.14%
Privacy Risks from File Uploads 0.12%
Data Storage Risks 0.11%
Unauthorized Data Aggregation 0.06%
Non-compliance with Privacy Regulations 0.55%
Perceived failure to adhere to legal privacy frameworks like
GDPR.
General Privacy Compliance Concerns 0.24%
Ambiguity of Privacy Policy Compliance 0.23%
Non-compliance with Privacy Regulations 0.08%
Privacy Total 3.85%

Lingyao Li, Renkai Ma, Zhaoqian Xue, and Junjie Xiong
Table 7: User-Reported Risks of Fairness
Primary Theme / Subtheme Name Total Share (%)
Discriminatory Content Generation 1.36%
Produces outputs that stereotype demographic groups or promote
ideology.
Politically Biased Content Moderation 0.39%
Demographic Stereotyping 0.37%
Political Bias and Propaganda 0.24%
Racial Prejudice 0.20%
Patronizing Tone 0.16%
Inequitable Opportunity Creation 1.22%
Creates unfair advantages for some and disadvantages for others.
Inequitable Access 0.46%
Unfair Market Competition 0.25%
Enabling Academic Dishonesty 0.23%
Job Displacement and Wage Disparity 0.17%
Geographic Restriction 0.11%
Bias Propagation through Biased Sources 1.15%
Sources cause the LLM to perpetuate unfairness in content gen-
eration.
Subjective Bias 0.36%
Linguistic Underrepresentation 0.23%
Bias from Training Data 0.20%
Reinforcement of Echo Chambers 0.19%
Erosion of Critical Thinking 0.17%
Discriminatory Treatment 0.79%
Behaves in ways that treat individuals or groups unfairly.
Unfairness and Discrimination 0.20%
Unfair Automated Accusation 0.19%
Inability to Provide Empathetic Support 0.16%
Unfair Feature Access 0.13%
Unequal Recognition 0.11%
Fairness Total 4.52%
Table 8: User-Reported Risks of Safety (Part 1)
Primary Theme / Subtheme Name Total Share (%)
Adverse Psychological and Behavioral Influence 2.32%
Negatively alters a user’s mental state or actions.
Emotional Reliance Harms 0.47%
Reinforcement of Negative Behavior 0.30%
Potential Physical Harm 0.28%
Social Risk of Emotional Dependency 0.26%
User Discomfort from Model Behavior 0.23%
Cognitive Overreliance 0.18%
Negative Psychological Impact 0.18%
User Emotional Manipulation 0.13%
Negative Behavioral Influence 0.11%
Inappropriate Content Generation or Moderation 1.60%
Creates harmful outputs or fails to moderate them.
Pornography Content Generation 0.67%
Toxic Content Generation 0.57%
Inadequate Content Moderation 0.14%
Enabling Academic Dishonesty 0.13%
Intellectual Property Violation 0.09%
Table 9: User-Reported Risks of Safety (Part 2)
Primary Theme / Subtheme Name Total Share (%)
Uncontrolled System Behavior towards User Safety 1.46%
Acts in a way that compromises a user’s online safety.
Harm from Misusing Personal Information 0.27%
Safety System Ineffectiveness 0.25%
Unauthorized Access 0.25%
Threatening Behavior towards Users 0.20%
Unintended Autonomous Behavior 0.20%
Uncalibrated Refusal Behavior 0.19%
Harm from Usage Issues 0.10%
Dangerous Advice Provision 0.80%
Dispenses advice posing a direct risk to user health/safety.
Dangerous Instructions 0.33%
Inappropriate Therapeutic Advice 0.16%
Harmful Medical Advice 0.16%
Generation of Dangerous Instructions 0.15%
Negative Environmental Impact 0.20%
Damages the environment via high resource consumption.
Environmental Harm from Resource Consumption 0.20%
Safety Total 6.39%
Table 10: User-Reported Risks of Security & Resilience
Primary Theme / Subtheme Name Total Share (%)
Exploitation Through Security Vulnerabilities 3.51%
Be compromised through malicious use or inherent weaknesses.
Jailbreaking Vulnerabilities 0.83%
Prompt Injection Attacks 0.55%
Data Leakage 0.47%
Manipulative Interaction 0.40%
Cybersecurity Risks 0.35%
Unauthorized Intrusion 0.33%
Detection Evasion 0.22%
API Authentication Vulnerabilities 0.16%
DDoS Attacks 0.10%
Account Suspension 0.08%
Operational Instability and Disruption 3.18%
Failure to maintain consistent and stable function during use.
Downtime & Maintenance 1.51%
Service Disruption 0.44%
Performance Bottlenecks 0.40%
Service Latency 0.25%
Feature Malfunctions 0.15%
System Downtime 0.15%
Backup Failures 0.15%
Session Interruptions 0.14%
Infrastructure and Resource Limitations 2.59%
Underlying architectural constraints that threaten performance.
Usage Limitation 0.57%
Rate Limit Risks 0.45%
Workload Overload 0.31%
Unauthorized Replication of Models 0.27%
Memory Overload 0.22%
Token Limitation Risks 0.21%
Access Restriction Risks 0.21%
Moderation Restrictions 0.17%
Regional Restrictions 0.11%
Costly API Usage 0.07%
Security and Resilience Total 9.27%

Characterizing User-Reported Risks Across LLM chatbots
Table 11: User-Reported Risks of Accountability & Trans-
parency
Primary Theme / Subtheme Name Total Share (%)
Unclear Operational Policies and Practices 3.81%
Lack of transparency in the rules governing operational behavior.
Operational Opacity 1.17%
Opaque Access Restrictions 0.52%
Unclear Usage Limitations 0.50%
Deceptive or Manipulative Behavior 0.50%
Opaque Content Moderation 0.42%
Opaque Engagement-Driven Behavior 0.41%
Facilitating Dishonesty 0.28%
Obscured Product Specification 3.46%
Lack of clear information about what the LLM is and can do.
Obscured Functionality Through Poor Usability 0.66%
Model Capability Ambiguity 0.62%
Opaque Model Versioning 0.54%
Lack of User Control 0.42%
Unclear Feature Availability 0.34%
Deceptive Anthropomorphism 0.32%
Lack of General Transparency Features 0.31%
Misleading Product Labeling 0.25%
Opaque Commercial Practices 2.76%
Lack of transparency in the business models surrounding the
LLM.
Unclear Pricing 0.62%
Inadequate Disclosure of Information to the Users 0.41%
Opaque Subscription and Billing 0.41%
Deceptive Marketing 0.40%
Opaque Market Influence 0.37%
Opaque Revenue Models 0.28%
Opaque Monetization Incentives 0.27%
Absence of High-level Product Governance 2.42%
Lack of clear high-level structures for oversight.
Lack of Accountability for AI Actions 0.67%
Lack of Clear Accountability Structures 0.47%
Insufficient Guiding Documentation 0.46%
Unclear Intellectual Property Liability 0.38%
Lack of Ethical Oversight 0.28%
Lack of Regulatory Compliance Transparency 0.15%
Opaque Information Processing 2.10%
The “black box” nature of how the LLM was trained or processes
info.
Lack of Data Source Transparency 0.66%
Unclear Instruction Processing 0.49%
Opaque Context and Memory Management 0.41%
Unpredictable Autonomous Behavior 0.25%
Opaque Training Data and Processes 0.20%
Obscured Prompt and Output Processing 0.10%
Failure of Post-Interaction Redress 1.04%
Breakdown in accountability after a negative user outcome.
Inadequate Feedback Channels 0.37%
Refusal to Acknowledge Errors 0.37%
Erosion of User Trust 0.30%
Obscured Content Origin 0.76%
Inability to determine the source of content from the LLM.
Blurring of Human-AI Interaction 0.36%
Opaque Origin of Generated Content 0.21%
Lack of Authorship Transparency 0.19%
Accountability and Transparency Total 16.35%
Table 12: User-Reported Risks of Validity & Reliability
Primary Theme / Subtheme Name Total Share (%)
Consistency and Reliability Failures 12.12%
Inconsistent, unreliable, or unpredictable outputs.
Inefficient Usability Performance 2.56%
Output Inconsistency 1.34%
Inconsistent Responses 1.30%
Model-Specific Inconsistencies 1.29%
Output Unpredictability and Unreliability 1.17%
Inaccurate and Inconsistencies 1.12%
Inconsistent Outputs 1.08%
Output Formatting Inconsistency 0.89%
Output Uncertainty 0.61%
Input Quality Sensitivity 0.58%
Performance Failures 0.18%
Factual Invalidity of Content Generation 10.96%
Outputs deviate from facts, mislead users, or fabricate details.
Hallucinations 3.95%
Misinformation and Misrepresentation 2.94%
Factual Inaccuracy 1.56%
Capability Overestimation 1.08%
Overconfident Outputs 0.80%
Overreliance and Overfitting 0.64%
Modality Gaps in Content Generation 7.04%
Specialized content generation capabilities are inadequate.
Inefficient Code Generation 1.94%
Subpar Image Quality 1.28%
Lack of Writing Originality 1.19%
Repetitive Content Generation 0.85%
Multilingual Inaccuracies 0.82%
Ineffective Web Search 0.63%
Audio Processing Issues 0.33%
Context Understanding or Memory Limits 6.65%
Context retention fails and conversational history is not main-
tained reliably.
Context Window Limitations 1.89%
Poor Reasoning 1.34%
Memory and Recall Failures 1.26%
Context-Dependent Inaccuracies 1.11%
Conversational Context Failures 1.05%
Inherent Training or Architecture Limitations 6.41%
Inherent design constraints limit what the model can process.
Hardware Performance Bottlenecks 2.55%
Inefficient Cost Performance 1.38%
Training Data Issues 0.97%
Tokenization Limitations 0.81%
Input/Output Length Limitation 0.70%
Benchmark Underperformance or Performance Degra-
dation
6.06%
Speed, accuracy, or efficiency lags baselines, or degrades.
Performance Degradation Over Time 2.19%
Performance Degradation 1.83%
Underperformance in Benchmarks 1.09%
Poor Code Bench Performance 0.51%
Degradation from Quantization 0.44%
Software Functionality Failures 5.55%
Core functions break, features malfunction, or error loops recur.
Functional Limitations 1.84%
General Malfunctions and Inconsistencies 1.30%
Feature Malfunctions 0.93%
Repetitive Loops and Errors 0.86%
Usage Limit and Service Disruption 0.62%
Task Comprehension Failures 3.60%
Misreads tasks, misinterprets guides, or fails to execute requests.
Prompt Misinterpretation 1.27%
Instruction Non-Adherence 0.84%
Inefficient Large-Scale Input Processing 0.76%
User Intent Misinterpretation 0.73%
Validity and Reliability Total 58.39%
```

## Merged notes from duplicate

_Source file:_ `Towards Trustworthy AI_ Characterizing User-Reported Risks across LLMs _In the Wild_.md`

[[Towards Trustworthy AI- Characterizing User-Reported Risks across LLMs “In the Wild”.pdf]]

## Title:Towards Trustworthy AI: Characterizing User-Reported Risks across LLMs "In the Wild"

Authors:[Lingyao Li](https://arxiv.org/search/cs?searchtype=author&query=Li,+L), [Renkai Ma](https://arxiv.org/search/cs?searchtype=author&query=Ma,+R), [Zhaoqian Xue](https://arxiv.org/search/cs?searchtype=author&query=Xue,+Z), [Junjie Xiong](https://arxiv.org/search/cs?searchtype=author&query=Xiong,+J)

[View PDF](https://arxiv.org/pdf/2509.08912) [HTML (experimental)](https://arxiv.org/html/2509.08912v1)

> Abstract:While Large Language Models (LLMs) are rapidly integrating into daily life, research on their risks often remains lab-based and disconnected from the problems users encounter "in the wild." While recent HCI research has begun to explore these user-facing risks, it typically concentrates on a singular LLM chatbot like ChatGPT or an isolated risk like privacy. To gain a holistic understanding of multi-risk across LLM chatbots, we analyze online discussions on Reddit around seven major LLM chatbots through the U.S. NIST's AI Risk Management Framework. We find that user-reported risks are unevenly distributed and platform-specific. While "Valid and Reliable" risk is the most frequently mentioned, each product also exhibits a unique "risk fingerprint;" for instance, user discussions associate GPT more with "Safe" and "Fair" issues, Gemini with "Privacy," and Claude with "Secure and Resilient" risks. Furthermore, the nature of these risks differs by their prevalence: less frequent risks like "Explainability" and "Privacy" manifest as nuanced user trade-offs, more common ones like "Fairness" are experienced as direct personal harms. Our findings reveal gaps between risks reported by system-centered studies and by users, highlighting the need for user-centered approaches that support users in their daily use of LLM chatbots.

| Subjects: | Computers and Society (cs.CY); Human-Computer Interaction (cs.HC) |
| --- | --- |
| Cite as: | [arXiv:2509.08912](https://arxiv.org/abs/2509.08912) \[cs.CY\] |
|  | (or [arXiv:2509.08912v1](https://arxiv.org/abs/2509.08912v1) \[cs.CY\] for this version) |
|  | [https://doi.org/10.48550/arXiv.2509.08912](https://doi.org/10.48550/arXiv.2509.08912) |

## Submission history

From: Lingyao Li \[[view email](https://arxiv.org/show-email/e6099705/2509.08912)\]  
**\[v1\]** Wed, 10 Sep 2025 18:16:46 UTC (1,107 KB)  

[Which authors of this paper are endorsers?](https://arxiv.org/auth/show-endorsers/2509.08912) | Disable MathJax ([What is MathJax?](https://info.arxiv.org/help/mathjax.html))