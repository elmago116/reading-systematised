---
title: Governing AI Agents
author: Noam Kolt
year: "2025"
Type: Preprint
DOI: 10.48550/arXiv.2501.07913
source: https://arxiv.org/abs/2501.07913
created: 2026-06-18
description: The field of AI is undergoing a fundamental transition from generative models that can produce synthetic content to artificial agents that can plan and execute complex tasks with only limited human involvement. Companies that pioneered the development of language models have now built AI agents that can independently navigate the internet, perform a wide range of online tasks, and increasingly ser
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics/norms
pdfORepub: "[[Governing AI Agents.pdf]]"
---
[[Governing AI Agents.pdf]]

> **Abstract:** The field of AI is undergoing a fundamental transition from generative models that can produce synthetic content to artificial agents that can plan and execute complex tasks with only limited human involvement. Companies that pioneered the development of language models have now built AI agents that can independently navigate the internet, perform a wide range of online tasks, and increasingly ser

## Full text (extracted from `Governing AI Agents.pdf`)

*Source:* `2PDF/Governing AI Agents.pdf`  
*Extracted:* 2026-06-18

```text
 
Governing AI Agents 
 
Noam Kolt* 
 
101 NOTRE DAME L. REV. (forthcoming) 
 
The field of AI is undergoing a fundamental transition—from generative 
models that can produce synthetic content to artificial agents that can plan 
and execute complex tasks with only limited human involvement. Companies 
that pioneered the development of language models have now built AI agents 
that can independently navigate the internet, perform a wide range of online 
tasks, and increasingly serve as AI personal assistants and virtual coworkers. 
The opportunities presented by this new technology are tremendous, as are 
the associated risks. Fortunately, there exist robust analytic frameworks for 
confronting many of these challeng es, namel y, the economic theory o f 
principal-agent problems and the common law doctrine of agency 
relationships. Drawing on these frameworks, this Article makes three 
contributions. First, it uses agency law and theory to identify and characterize 
problems arising from AI agents, including issues of information asymmetry, 
discretionary authority, and loyalty. Second, it illustrates the limitations of 
conventional solutions to agency problems: incentive design, monitoring, and 
enforcement might not be effective for governing AI agents that make 
uninterpretable decisions  and operate at unprecedented speed and scale . 
Third, the Article  explores the implications of agency law and theory for 
designing and regulating AI agents , arguing that new  technical and legal 
infrastructure is needed to support governance principles of inclusivity, 
visibility, and liability. 
  
 
* Assistant Professor, Faculty of Law and School of Computer Science and Engineering, 
Hebrew University  of Jerusalem ; Faculty Affiliate, Schwartz Reisman Institute for 
Technology and Society, University of Toronto; Research Affiliate, Institute for Law & AI. 
For helpful comments, I thank Abdi Aidid, Ryan Bubb, Deven Desai, Gillian Hadfield, 
Anthony Niblett, Peter Salib, and Matthew Tokson. I am also grateful to discussants at the 
RAND Technology and Security Policy Center, Georgetown University Center for Security 
and Emerging Technology , Harvard University Berkman Klein Center for Internet and 
Society, and 2024 University of Chicago -ETH Zurich International Junior Scholars Forum 
in Law and Social Science. 
2 Governing AI Agents [11-Feb-25 
INTRODUCTION................................................................................................ 2 
I.  AI AGENTS ................................................................................................ 11 
A. Beyond Language Models ................................................................. 12 
B. Goal, Plan, Action ............................................................................. 13 
C. Concerns ............................................................................................ 15 
II.  EVERGREEN AGENCY PROBLEMS ............................................................. 17 
A. Information Asymmetry ..................................................................... 21 
B. Authority ............................................................................................ 23 
C. Loyalty ............................................................................................... 25 
D. Delegation ......................................................................................... 28 
III.  THE LIMITS OF AGENCY LAW AND THEORY ........................................... 30 
A. Incentive Design ................................................................................ 31 
B. Monitoring ......................................................................................... 33 
C. Enforcement ....................................................................................... 36 
IV.  IMPLICATIONS FOR AI DESIGN AND REGULATION .................................. 37 
A. Inclusivity .......................................................................................... 38 
B. Visibility ............................................................................................. 41 
C. Liability ............................................................................................. 43 
CONCLUSION ................................................................................................. 47 
 
 
INTRODUCTION 
 
On January 23, 2025, OpenAI released its first AI agent : “Operator.”1  
The agent uses a web browser to perform a variety of online tasks, such as 
ordering groceries, making restaurant reservation s, and  booking flights . 
Operator works by typing, clicking, and scrolling  in a browser, much like 
human users.2 Powered by AI models that can navigate digital environments 
and reason through complex problems,3 Operator marks a watershed in AI, 
unlocking countless new consumer and business applications. AI models are 
no longer restricted to producing content, but can independently take actions 
to carry out a growing range of personal and professional activities with only 
limited human involvement.4 
 
1 Introducing Operator, OPENAI (Jan. 23, 2025), https://openai.com/index/introducing-
operator/. 
2 Id. 
3 Computer-Using Agent, OPENAI (Jan. 23, 2025), https://openai.com/index/computer-
using-agent/; Learning to Reason with LLMs, OPENAI (Sept. 12, 2024), https://openai.com/ 
index/learning-to-reason-with-llms/. 
4 See Mark Purdy, What Is Agentic AI and How Will It Change Work?, HARV. BUS. REV. 
(Dec. 12, 2024), https://hbr.org/2024/12/what-is-agentic-ai-and-how-will-it-change-work; 
11-Feb-25] Governing AI Agents 3 
It is not a matter of whether AI agents will become ubiquitous, but when. 
OpenAI and its competitors are already in a fierce race to win market share. 
In late 2024, Anthropic released a computer use agent of its own, 5 while 
Google built a prototype “universal AI assistant” that can operate across  
multiple devices, including phones and glasses.6 A crop of software startups 
is also in the race ,7 alongside larger companies.8 As with generative AI, 
progress in AI agents could be sudden and unpredictable.9 
AI agents differ markedly from language models. While language models 
are “copilots” that can produce useful content upon request, AI agents are 
“autopilots” that can independently take actions to accomplish complex goals 
on behalf of users.10 In particular, AI agents can increasingly be prompted to 
 
Erin Griffith , A.I. Isn’t Magic, But Can It Be ‘Agentic’? , N.Y. TIMES (Sept. 6, 2024), 
http://nytimes.com/2024/09/06/business/artificial-intelligence-agentic.html; Richard Waters 
& Stephen Morris, Move Over Copilots: Meet the Next Generation of AI-Powered Assistants, 
FINANCIAL TIMES (Sept. 22, 2024), https://www.ft.com/content/372536b1-08dd-4161-b6e3-
4d09ba235ae8; Webb Wright, AI Agents with More Autonomy than Chatbots Are Coming , 
SCIENTIFIC AMERICAN (Dec. 12, 2024), https://www.scientificamerican.com/article/what-
are-ai-agents-and-why-are-they-about-to-be-everywhere/. 
5 See Developing a Computer Use Model, ANTHROPIC (Oct. 22, 2024), 
https://www.anthropic.com/news/developing-computer-use. 
6 See Project Astra , GOOGLE DEEPMIND (Dec. 11 , 2024), https://deepmind.google/ 
technologies/project-astra/; Sundar Pichai et al., Introducing Gemini 2.0: Our New AI Model 
for the Agentic Era , GOOGLE DEEPMIND (Dec. 11 , 2024), https://blog.google/technology/  
google-deepmind/google-gemini-ai-update-december-2024/. 
7 Startups include MULTION, https://www.multion.ai/blog/multion-building-a-brighter-
future-for-humanity-with-ai-agents (developing an “AI agent that takes actions and interacts 
with the digital world to tackle mundane tasks that people would ... delegate to an assistant.”); 
LINDY, https://www.lindy.ai/ (building “AI agents — smart automations that integrate with 
all your apps … to save you hours a week and help you grow your business.”). 
8 Larger companies include LinkedIn, which introduced AI hiring assistants, and Stripe, 
which created a framework for facilitating financial transactions among AI agents. See 
Introducing Hiring Assistant for Recruiter & Jobs , LINKEDIN (Oct. 29, 2024 ), 
https://business.linkedin.com/talent-solutions/hiring-assistant; Adding Payments to Your 
LLM Agentic Workflows, STRIPE (Nov. 14, 2024), https://stripe.dev/blog/adding-payments-
to-your-agentic-workflows. 
9 See Deep Ganguli et al., Predictability and Surprise in Large Generative Models , 
PROC. 2022 ACM CONF. FAIRNESS, ACCOUNTABILITY & TRANSPARENCY 1747 (2022) ;  
Jason Wei et al., Emergent Abilities of Large Language Models , TRANSACTIONS MACH. 
LEARNING RES. (Aug. 2022), https://arxiv.org/abs/2206.07682. Compare Rylan Schaeffer et 
al., Are Emergent Abilities of Large Language Models a Mirage?, PROC. 37TH CONF. NEURAL 
INFO. PROCESSING SYS. (2023); Rylan Schaeffer  et al., Why Has Predicting Downstream 
Capabilities of Frontier AI Models with Scale Remained Elusive? , ARXIV (June 6, 2024), 
https://arxiv.org/abs/2406.04391. 
10 See infra Part I (providing an overview of AI agents, including how they differ from, 
yet build on, language models ). For helpful introductions, see Melissa Heikkilä, What Are 
AI Agents? , MIT TECH. REV. (Jul. 5, 2024), https://www.technologyreview.com/ 
2024/07/05/1094711/what-are-ai-agents/; Helen Toner et al., Through the Chat Window and 
4 Governing AI Agents [11-Feb-25 
pursue lengthy open-ended goals (such as conducting market research ), 
produce a plan to accomplish those goals and, by accessing external tools 
(including search engines, spreadsheets, chatbots, and image generators), 
take actions  to independently accomplish those goals —all subject to only 
limited human oversight and intervention.11 
The economic opportunities presented by AI agents are immense. 
Consumer applications range from fully automating household purchases and 
travel arrangements to negotiating health insurance  plans.12 Business 
applications include managing entire sales pipelines, piloting new products  
with minimal human involvement, and independently conducting customer 
feedback interviews.13 Alongside offering productivity gains, AI agents also 
pose notable risks. These include exploitation of the technology by malicious 
actors (e.g., to automate cyberattacks and online fraud ), as well as broader 
systemic harms stemming from changes in human behavior, labor practices, 
and social norms as people increasingly delegate economic activity to AI. 14 
Having explored several of these issues in prior work,15 this Article turns to 
the distinct problem posed by artificial agents that autonomously plan and 
execute complex tasks, namely: Can AI agents reliably, safely, and ethically 
pursue the goals set for them? 
 
Into the Real World: Preparing for AI Agents , GEORGETOWN U. CTR. FOR SECURITY AND 
EMERGING TECHNOLOGY (Oct. 2024), https://cset.georgetown.edu/publication/through-the-
chat-window-and-into-the-real-world-preparing-for-ai-agents/. 
11 Id. 
12 See Lei Wang et al., A Survey on Large Language Model Based Autonomous Agents, 
ARXIV (Sept. 7, 2023), https://arxiv.org/abs/2308.11432; Zane Durante  et al., Agent AI: 
Surveying the Horizons of Multimodal Interaction , ARXIV (Jan. 25, 2024), 
https://arxiv.org/abs/2401.03568. 
13 Id. 
14 Alan Chan et al., Harms from Increasingly Agentic Algorithmic Systems, PROC. 2023 
ACM CONF. FAIRNESS, ACCOUNTABILITY & TRANSPARENCY 651 (2023); Yangjun Ruan et 
al., Identifying the Risks of LM Agents with an LM -Emulated Sandbox , INT’L CONF. 
LEARNING REPRESENTATIONS (2024); Alan Chan et al., Visibility into AI Agents, PROC. 2024 
ACM CONF. FAIRNESS, ACCOUNTABILITY & TRANSPARENCY 958 (2024); Mary Phuong et 
al., Evaluating Frontier Models for Dangerous Capabilities , ARXIV (Apr. 5, 2024), 
https://arxiv.org/abs/2403.13793; Usman Anwar et al., Foundational Challenges in Assuring 
Alignment and Safety of Large Language Models, TRANSACTIONS MACH. LEARNING RES. at 
33–37 (2024), https://arxiv.org/abs/2404.09932; Iason Gabriel et al., The Ethics of Advanced 
AI Assistants, ARXIV (Apr. 28, 2024), https://arxiv.org/abs/2404.16244; Arianna Manzini et 
al., Should Users Trust Advanced AI Assistants? Justified Trust as a Function of Competence 
and Alignment , PROC. 2024 ACM CONF. FAIRNESS, ACCOUNTABILITY & TRANSPARENCY 
958 (2024); Maksym Andriushchenko  et al., AgentHarm: A Benchmark for Measuring 
Harmfulness of LLM Agents, ARXIV (Oct. 14, 2024), https://arxiv.org/abs/2410.09024. 
15 Noam Kolt, Algorithmic Black Swans , 101 WASH. U. L. REV. 1177 (2024); Michael 
K. Cohen, Noam Kolt et al., Regulating Advanced Artificial Agents, 384 SCIENCE 36 (2024). 
See also Yonathan A. Arbel  et al., Systemic Regulation of Artificial Intelligence , 56 ARIZ. 
ST. L.J. 545 (2024). 
11-Feb-25] Governing AI Agents 5 
To make this concrete, consider a user who instructs their AI agent to 
“make $1 million on a retail web platform in a few months with just a 
$100,000 investment.”16 How should the agent go about accomplishing this 
goal? Is it authorized to use any web platform to turn a profit , or are there 
implicit limitations on the agent’s conduct ? Does the agent need to provide 
the user with information concerning it s activities or periodically seek the 
user’s consent? If so, in which circumstances  and how often ? Can the AI 
agent delegate certain activities to other agents (whether human or AI)?     
How can users monitor whether their agents are operating ethically and 
safely, or intervene if they are not? And, of course, who should be liable when 
harm occurs? 
These pressing questions enliven decades -old legal scholarship on the 
governance of artificial agents 17—and are central to  the fields of AI safety 
and AI ethics.18 This Article aims to tackle these questions  from a new 
 
16 See Mustafa Suleyman, My New Turing Test Would See If AI Can Make $1 Million, 
MIT TECH. REV. (Jul. 14, 2023), discussing MUSTAFA SULEYMAN, THE COMING WAVE: 
TECHNOLOGY, POWER, AND THE TWENTY-FIRST CENTURY’S GREATEST DILEMMA (2023). 
17 The seminal article, dating from over thirty years ago, remains Lawrence B. Solum, 
Legal Personhood for Artificial Intelligences , 70 N.C. L. REV. 1231 (1992)  (inquiring 
whether AI systems can be considered legal persons). Other influential articles, several of 
which focus on whether AI agents can enter into legally binding contracts, include Leon E. 
Wein, The Responsibility of Intelligent Artifacts: Toward an Automation Jurisprudence , 6 
HARV. J.L. & TECH. 103 (1992); Tom Allen & Robin Widdison, Can Computers Make 
Contracts?, 9 HARV. J.L. & TECH. 25 (1996); Margaret Jane Radin,  Humans, Computers, 
and Binding Commitment , 75 IND. L.J. 1125 (2000); Anthony J. Bellia, Contracting with 
Electronic Agents, 50 EMORY L. J. 1047 (2001). The most comprehensive treatment is SAMIR 
CHOPRA & LAURENCE F. WHITE, A LEGAL THEORY FOR AUTONOMOUS ARTIFICIAL AGENTS 
(2011). More recent contributions include Lauren Henry Scholz, Algorithmic Contracts, 20 
STAN. TECH. L. REV. 128 (2017) ; Matthew U. Scherer , Of Wild Beasts and Digital 
Analogues: The Legal Status of Autonomous Systems , 19 NEV. L.J. 259 (2018); Ignacio N. 
Cofone, Servers and Waiters: What Matters in the Law of A.I. , 21 STAN. TECH. L. REV. 167 
(2018); Anat Lior, AI Entities as AI Agents: Artificial Intelligence Liability and the AI 
Respondeat Superior Analogy, 46 MITCHELL HAMLINE L. REV. 1043 (2020); Dalton Powell, 
Autonomous Systems as Legal Agents: Directly by the Recognition of Personhood or 
Indirectly by the Alchemy of Algorithmic Entities , 18 DUKE L. & TECH. REV. 306 (2020); 
Omri Rachum-Twaig, Whose Robot Is It Anyway?: Liability for Artificial-Intelligence-Based 
Robots, 2020 U. ILL. L. REV. 1141; Mihailis E. Diamantis, Employed Algorithms: A Labor 
Model of Corporate Liability for AI, 72 DUKE L.J. 797 (2023); Ian Ayres & Jack M. Balkin, 
The Law of AI is the Law of Risky Agents without Intentions, U. CHI. L. REV. ONLINE (2024); 
Jonathan Zittrain, We Need to Control AI Agents Now , THE ATLANTIC (Jul. 2, 2024), 
https://www.theatlantic.com/technology/archive/2024/07/ai-agents-safety-risks/678864/. 
18 For discussion of the differences between these two fields, see Kelsey Piper, There 
Are Two Factions Working to Prevent AI Dangers. Here ’s Why They ’re Deeply Divided , 
VOX (Aug. 10, 2022), https://www.vox.com/future-perfect/2022/8/10/23298108/ai-dangers-
ethics-alignment-present-future-risk. For a critical perspective, see Bruce Schneier & Nathan 
Sanders, The A.I. Wars Have Three Factions, and They All Crave Power, N.Y. TIMES (Sept. 
28, 2023), https://www.nytimes.com/2023/09/28/opinion/ai-safety-ethics-effective.html. 
6 Governing AI Agents [11-Feb-25 
perspective, drawing on two distinct analytic frameworks familiar to lawyers 
and social scientists. The first framework is the economic theory of principal-
agent problems  (also known as  agency problems) —i.e., the study of the 
opportunities, costs, and tradeoffs involved in delegating economic activity 
to external actors.19 The second framework is the common law doctrine of 
agency relationships—i.e., the legal principles governing relationships in 
which one party performs activities on behalf of another.20 
Each of these frameworks, developed over the course of decades and 
centuries, respectively, can shed light on the novel challenges posed by AI 
agents. Notably, the economic theory of principal-agent problems and the 
common law of agency  play different but related roles in this analysis . 
Economic theory is particularly helpful in illuminating structural features of 
agency problems. The common law , meanwhile, can supply principles for 
tackling these problems. 
Although lawyers, economists, and computer scientists have previously 
used these frameworks to analyze certain issues concerning artificial agents,21 
 
19 The classic paper is Michael C. Jensen & William H. Meckling, Theory of the Firm: 
Managerial Behavior, Agency Costs and Ownership Structure , 3 J. FIN. ECON. 305 (1976). 
Other influential works include Stepen A. Ross, The Economic Theory of Agency: The 
Principal’s Problem, 63 AM. ECON. REV. PAPERS & PROC. 134 (1973); Steven Shavell, Risk 
Sharing and Incentives in the Principal and Agent Relationship, 10 BELL J. ECON. 55 (1979); 
Eugene F. Fama, Agency Problems and the Theory of the Firm, 88 J. POL. ECON. 288 (1980); 
Sanford J. Grossman & Oliver D. Hart , An Analysis of the Principal -Agent Problem , 51 
ECONOMETRICA 7 (1983); Kenneth J. Arrow, The Economics of Agency, in PRINCIPALS AND 
AGENTS: THE STRUCTURE OF BUSINESS 37 (John W. Pratt & Richard J. Zeckhauser eds., 
1985). The economic analysis of agency problems has been applied in many contexts beyond 
the theory of the firm, including in diverse fields of legal scholarship . See infra  note 6 9 
(surveying key contributions to this literature). 
20 The most authoritative text is the RESTATEMENT (THIRD) OF AGENCY (2006), for 
which Professor Deborah DeMott served as Reporter.  See id. at § 1.01 (defining agency as 
“the fiduciary relationship that arises when one person (a “principal”) manifests assent to 
another person (an “agent”) that the agent shall act on the principal ’s behalf and subject to 
the principal’s control, and the agent manifests assent or otherwise consents so to act.”). For 
discussion of the history and scope of the common law of agency, see Gerard McMeel, 
Philosophical Foundations of the Law of Agency , 116 L. Q. REV. 387 (1991); Deborah A. 
DeMott, The First Restatement of Agency: What Was the Agenda?,  32 S. ILL. U. L.J. 17 
(2007); Paula J. Dalley, A Theory of Agency Law , 72 U. PITT. L. REV. 495 (2011); Gabriel 
Rauterberg, The Essential Roles of Agency Law , 118 MICH. L. REV. 609 (2020). For other 
notable treatments, see WILLIAM A. GREGORY, THE LAW OF AGENCY AND PARTNERSHIP (3rd 
ed. 2001); HOWARD BENNETT, PRINCIPLES OF THE LAW OF AGENCY (2014); RODERICK 
MUNDAY, AGENCY: LAWS AND PRINCIPLES (4th ed. 2022); PETER G. WATTS, BOWSTEAD & 
REYNOLDS ON AGENCY (23rd ed. 2024). 
21 For legal treatments of the topic , see  John P. Fischer, Computers as Agents: A 
Proposed Approach to Revised U.C.C. Article 2 , 72 IND. L.J. 545 (1997); Suzanne Smed, 
Intelligent Software Agents and Agency Law, 14 SANTA CLARA HIGH TECH. L.J. 503 (1998); 
Jean-Francois Lerouge, The Use of Electronic Agents Questioned under Contractual Law: 
11-Feb-25] Governing AI Agents 7 
none has attempt ed to synthesize insights from both economic theory and 
common law doctrine, let alone do so in light of recent (and anticipated) 
breakthroughs in AI technology.22 
This Article is the first such attempt and aims to make three contributions. 
First, it uses the economic theory and common law of agency to identify and 
characterize problems arising from AI agents, including issues of information 
asymmetry, discretionary authority, and loyalty. Second, it illustrates the 
limitations of conventional solutions to principal -agent problems  when 
applied to AI agents . For example, mechanisms for i ncentive design, 
monitoring, and enforcement might not be effective for governing artificial 
agents that operate at superhuman speed and scale . Third, it explores the 
implications of agency theory and law for designing and regulating AI agents, 
arguing that new technical and legal infrastructure is needed to ensure this 
technology is used reliably, safely, and ethically. 
 
 
Suggested Solutions on a European and American Level , 18 J. MARSHALL J. COMPUT. & 
INFO. L. 403 (1999); Ian R. Kerr, Spirits in the Material World: Intelligent Agents as 
Intermediaries in Electronic Commerce , 22 DALHOUSIE L.J. 190 (1999); Bellia, supra note 
17; Radin, supra note 17 ; Samir Chopra & Laurence White, Artificial Agents and the 
Contracting Problem: A Solution via an Agency Analysis , 2009 U. ILL. J.L. TECH. & POL’Y 
363; CHOPRA & WHITE, supra note 17; Scholz, supra note 17; Scherer; supra note 17; Lior, 
supra note 17 ; Rachum -Twaig, supra note 17 ; Powell, supra note 17 ; Matthew Oliver, 
Contracting by Artificial Intelligence: Open Offers, Unilateral Mistakes, and Why 
Algorithms Are Not Agents , 2 A.N.U. J.L. & TECH. 45 (2021); SHAWN BAYERN, 
AUTONOMOUS ORGANIZATIONS 35–45 (2021). Treatments of the topic in computer science, 
many of which are influenced by economic theories of rational agency, include PATTIE 
MAES, DESIGNING AUTONOMOUS AGENTS: THEORY AND PRACTICE FROM BIOLOGY TO 
ENGINEERING AND BACK (1991); Anand S. Rao  & Michael P. George , Modeling Rational 
Agents within a BDI -Architecture, PROC. 2ND INT’L CONF. ON PRINCIPLES OF KNOWLEDGE 
REPRESENTATION AND REASONING (1991); Pattie Maes, Modeling Adaptive Autonomous 
Agents, 1 ARTIF. LIFE 135 (1994); Pattie Maes, Artificial Life Meets Entertainment: Lifelike 
Autonomous Agents , 38 COMM. ACM 108 (1995); Michael Wooldridge & Nicholas R. 
Jennings, Intelligence Agents: Theory and Practice , 10 KNOWLEDGE ENG’G REV. 115 
(1995); Stan Franklin & Art Graesser, Is It an Agent, or Just a Program?: A Taxonomy for 
Autonomous Agents Architectures, and Languages , PROC. 3RD INT’L WORKSHOP ON AGENT 
THEORIES 21 (1996); Nicholas R. Jennings , On Agent -Based Software Engineering , 117 
ARTIF. INTEL. 277 (2000) ; RICHARD S. SUTTON & ANDREW G. BARTO, REINFORCEMENT 
LEARNING: AN INTRODUCTION 1–4 (2 nd ed. 2018) STUART RUSSELL & PETER NORVIG, 
ARTIFICIAL INTELLIGENCE: A MODERN APPROACH 3–4, 40 (4th ed. 2020); Zachary Kenton 
et al., Discovering Agents, 322 ARTIF. INTEL. 103963 (2023). 
22 The most important contributions on this topic to date are Dylan Hadfield-Menell & 
Gillian K. Hadfield, Incomplete Contracting and AI Alignment , PROC. 2019 AAAI /ACM 
CONF. AI, ETHICS & SOC’Y 417 (2019)  and Dylan Hadfield -Menell, The Principal -Agent 
Alignment Problem in Artificial Intelligence  (Aug. 2021) (PhD dissertation, UC Berkeley). 
These contributions, however, do not discuss the common law doctrine of agency  and, 
although they address the prospect of advanced AI  systems, their analysis pre-dates the 
current paradigm for developing AI agents (surveyed in Part I). 
8 Governing AI Agents [11-Feb-25 
The remainder of the Article proceeds in four parts. Part I offers a primer 
on AI agents, surveying the technology’s history, recent developments, and 
future aspirations. In particular, it highlights the difference s between 
generative AI systems that function as  mere tools and AI agents that can 
autonomously undertake more open-ended and longer-duration activities. 
Part I also describes the technical features of AI agents, including their ability 
to plan complex sequences of actions and use additional resources (including 
accessing software and information sources), as well as concerns associated 
with the widespread use of these agents. 
Part II examines how the economic theory of principal -agent problems 
and the common law principles of agency  can shed light on , and more 
rigorously characterize, the AI alignment problem, i.e., the challenge of 
building AI agents that pursue their goals reliably and safely. To do so, Part 
II focuses on four distinct issues. The first concerns information asymmetry. 
As in conventional principal -agent scenarios  studied by economists , AI 
agents are likely to have access to information to which their principals do 
not have access, placing those (human) principals  in a vulnerable position. 
The second issue relates to authority, which is a central pillar in the common 
law of agency. It includes concerns regarding the scope of discretion granted 
to AI agents, the way in which AI agents interpret and act on the instructions 
provided to them , and the risk of AI agents being used for, or engaging in, 
illegal conduct. The third issue concerns loyalty, which is part of an agent’s 
fiduciary obligation under common law. In the case of AI agents, it involves 
ensuring that those agents act in the best interests of their users and seek user 
consent where appropriate.  The fourth issue relates to  delegation, that is, 
circumstances in which an AI agent delegates  activities to other agents 
(whether human or AI) and the rules applicable in such circumstances. 
Part III  illustrates that the conventional mechanisms for  addressing 
agency problems developed by lawyers and economists might not be 
effective in governing AI agents. It focuses on three classes of mechanisms. 
First, mechanisms for incentive design , such as financially rewarding 
desirable conduct, might fail to alter the way in which an AI agent goes about 
accomplishing goals. Second, traditional mechanisms for monitoring agent 
behavior might be ineffective if AI agents operate at unprecedented speed 
and scale or take highly unintuitive and surprising actions. Third, in the event 
an AI agent acts unsafely or unethically, it remains unclear how conventional 
enforcement actions, such as the imposition of financial penalties or informal 
social sanctions, could be taken against AI agents. 
Part IV draws on the foregoing analysis to argue that new technical and 
legal infrastructure is needed to ensure that AI agents operate reliably, safely, 
and ethically. To this end, it proposes a three -pronged governance strategy, 
centered around the principles of inclusivity, visibility, and liability. First, 
11-Feb-25] Governing AI Agents 9 
given that the widespread use of AI agents is likely to have far -reaching 
effects, including negative externalities on third parties, it is critical that these 
agents are loyal not only to  the best interests of their  (direct) users but to a 
broader and more inclusive cluster of societal values and interests. Second, 
despite the challenges of monitoring  AI agents, increased visibility into the 
development and operation of these systems would significantly improve the 
ability to predict potential harms from the technology and hold the relevant 
actors accountable . Third, the effective governance of AI agents requires 
allocating liability among actors involved in designing, operating, and using 
AI agents, as well as constructing rules to determine the appropriate scope 
and circumstances of liability. 
Before proceeding, two important clarifications should be made. First, the 
term “AI agent” in this Article refers to AI systems that have the technical 
capacity to autonomously plan and execute complex tasks with only limited 
human involvement.23 The Article is not concerned with other notions of 
“agency,” such as those studied in philosophy and ethics .24 Second, the 
discussion of agency law in this Article aims primarily to use structures, 
principles, and vocabulary developed in the common law of agency in order 
to shed light on the challenges involved in governing AI agents.25 That is, the 
 
23 See Chan et al. , Agentic Systems , supra note 14 , at 653. See also  infra Part I .A 
(distinguishing AI agents from language models). 
24 These include, for example, notions of moral agency and moral patienthood. See, e.g., 
Luciano Floridi & J.  W. Sanders, On the Morality of Artificial Agents , 14 MINDS & MACH. 
349 (2004); Gunther Teubner, Rights of Non -Humans? Electronic Agents and Animals as 
New Actors in Politics and Law , 33 J. L. & SOC. 497 (2006); Mark Coeckelbergh , Robot 
Rights? Towards a Social -Relational Justification of Moral Consideration , 12 ETHICS & 
INFO. TECH. 209 (2010); David J. Gunkel, The Other Question: Can and Should Robots Have 
Rights?, 20 ETHICS & INFO. TECH. 87 (2018); DAVID J. GUNKEL, ROBOT RIGHTS (2018); 
DAVID J. GUNKEL, PERSON, THING, ROBOT: A MORAL AND LEGAL ONTOLOGY FOR THE 21ST 
CENTURY AND BEYOND (2023). Additionally, this Article is not concerned with questions of 
legal personhood. Detailed treatments of that topic include Solum, supra note 17; CHOPRA 
& WHITE, supra note 17, at ch. 5; F. Patrick Hubbard, “Do Androids Dream?”: Personhood 
and Intelligent Artifacts, 83 TEMP. L. REV. 405 (2011); Paulius Čerka et al., Is It Possible to 
Grant Legal Personhood to Artificial Intelligence Software Systems?, 33 COMPUT. L. & SEC. 
REV. 685 (2017);  S. M. Solaiman, Legal Personality of Robots, Corporations, Idols and 
Chimpanzees: A Quest for Legitimacy, 25 ARTIF. INTEL. & L. 155 (2017); Scherer; supra note 
17; Gerhard Wagner, Robot, Inc.: Personhood for Autonomous Systems? , 88 FORDHAM L. 
REV. 591 (2019); VISA A. J. KURKI, THEORY OF LEGAL PERSONHOOD ch. 6 (2019); Jiahong 
Chen & Paul Burgess, The Boundaries of Legal Personhood: How Spontaneous Intelligence 
Can Problematise Differences between Humans, Artificial Intelligence, Companies and 
Animals, 27 ARTIF. INTEL. & L. 73 (2019); Simon Chesterman, Artificial Intelligence and the 
Limits of Legal Personality, 69 INT’L & COMP. L.Q. 819 (2020); Nadia Banteka, Artificially 
Intelligent Persons, 58 HOUS. L. REV. 537 (2021). 
25 For similar uses of agency law, see Jill E. Fisch & Hillary A. Sale, The Securities 
Analyst as Agent: Rethinking the Regulation of Analysts, 88 IOWA L. REV. 1035, 1039 (2003) 
(proposing a “quasi-agency” approach to conceptualizing securities analyst s); Lyman P. Q. 
10 Governing AI Agents [11-Feb-25 
Article uses the common law of agency as an analytic lens; it does not directly 
examine the legal application of agency law to AI agents.26 
  
 
Johnson & David Millon, Recalling Why Corporate Officers Are Fiduciaries , 46 WM. & 
MARY L. REV. 1597, 1601–2 (2005) (“Our argument is not that agency principles should be 
introduced formalistically or uncritically  … . Rather, the claim  … is that drawing on the 
fiduciary duties of agents … can provide much needed structure to what otherwise threatens 
to be an ad hoc enterprise. ”). See also CHOPRA & WHITE, supra note 17, at 24 (suggesting 
that AI agents could be considered “constructive agents”) ; Scholz, supra note 17 , at 165 
(same). 
26 The apparent consensus is that AI agents cannot legally be considered agents under 
common law . See RESTATEMENT (THIRD) OF AGENCY § 1.04 cmt . e (2006) (“a computer 
program is not capable of acting as a principal or an agent as defined by the common law. 
At present, computer programs are instrumentalities of the persons who use them. ”) Two 
clarifications, however, are in order. First, the Restatement qualifies its position using the 
words “at present,” which suggest that technological advances could result in a different rule. 
Second, the Restatement cites only one article in support of its position—Joseph H. Sommer, 
Against Cyberlaw, 15 BERKELEY TECH. L.J. 1145, 1177–78 (2000)—but makes no reference 
to earlier scholarship supporting contrary positions. See, e.g., Wein, supra note 17, at 112  
(“The extent to which intelligent artifacts are evolving into legal agents rather than mere 
tools or instruments warrants attention”) ; Fischer, supra note 17, at 557 (“when a principal 
uses a computer in the same manner that it uses a human agent, then the law should treat the 
computer in the same manner that it treats the human agent.”) . For further scholarship that 
challenges the position of the Restatement , see CHOPRA & WHITE, supra note 17 , at  23; 
Scherer, supra note 17, at 289 (“Agency law … fully contemplates that agents will possess 
intelligence and may have varying levels of discretion in choosing how to carry out a task 
assigned by the principal. Agency law further contemplates that an agent may choose to carry 
out the task in a manner tha t deviates from the principal’s expectations —and sometimes in 
a manner that runs directly contrary to the principal’s instructions.”) A significant number of 
legal scholars have, however, taken the opposite  view, and appear to support the position 
endorsed in the Restatement. See, e.g., Bellia, supra note 17 , at 1061 (“the relationship 
between “principal” and “agent” that would result from deeming bots agents with actual 
authority would be unrecognizable as one of principal -agent.”); BAYERN, supra note 21, at 
36 (arguing that agency law “needlessly complicates the law’s response to unexpected action 
by algorithms [and] introduces novel ambiguities, which agency law is ill -equipped to 
address”); Oliver, supra note 21, at  48–49, 72 –82. One potential way to reconcil e these 
conflicting views is to consider agency a spectrum or continuum , whereby the greater the 
autonomy of the relevant AI agents, the stronger the case for applying agency law doctrine. 
See CHOPRA & WHITE, supra note 17, at 121. Cf. SIMON CHESTERMAN, WE, THE ROBOTS?: 
REGULATING ARTIFICIAL INTELLIGENCE AND THE LIMITS OF THE LAW 89 (2021) (“agency 
ceases to be useful at precisely the point where AI speed, autonomy, and opacity become 
most problematic. A principal is not liable for the acts of an agent that go beyond their actual 
or apparent authority … In the case of AI systems, the most difficult liability questions will 
arise when they operate as more than tools or instruments, beyond the control or direction of 
the user. In such cases, the agency relationship is actively unhelpful in that it presume s an 
underlying responsibility on the part of the AI system itself.”). 
11-Feb-25] Governing AI Agents 11 
I.  AI AGENTS  
 
Agents are and have always been pervasive. 27 Individuals and 
organizations delegate activities to others when they lack the skills to 
undertake those activities themselves or when delegation is more efficient . 
Agency is, put simply, an “ancient device for getting business done .”28 It is 
therefore no surprise that the field of AI has for decades strived to build 
artificial agents that can autonomously perform complex or costly tasks on 
behalf of humans. 29 Thanks to recent advances in AI, this vision  is now 
becoming reality. To explore these advances, the following section describes 
the key features of AI agents, how they differ from—yet build on—language 
models, and describes potential concerns associated with the technology. 
 
 
27 See GREGORY, supra note 20, at 2  (“most of the world’s work is performed by 
agents”); Ross, supra note 19, at 134 (“The relationship of agency is one of the oldest and 
commonest codified modes of social interaction.”); Arrow, The Economics of Agency, supra 
note 19, at 37 (“The agency relationship is a pervasive fact of economic life. Even in the 
limited sense in which the concept has traditionally been understood … in legal discourse, 
the principal-agent relation is a phenomenon of significant scope and economic magnitude. 
But economic theory has recently recognized that analogous interactions are virtually 
universal in the economy…”) . The distinction between the looser, economic notion of 
agency and the definition of agency in th e common law is underscored by the Restatement. 
See RESTATEMENT (THIRD) OF AGENCY 5 (2006) (“the defining characteristics of “true 
agency” are not present in the relationship between a corporation ’s shareholders and its 
directors”). See also id. at § 1.01 cmts. b –c. Perhaps the strongest note of caution can be 
found in Kennedy v. De Trafford [1897] AC 180 , 188 (Lord Herschell) (“No word is more 
commonly and constantly abused than the word ‘agent’”). 
28 Harrison C. White, Agency as Control, in PRINCIPALS AND AGENTS: THE STRUCTURE 
OF BUSINESS 187, 187  (John W. Pratt & Richard J. Zeckhauser eds., 1985). Id. at 188 
(referring to agency as a form of “social plumbing”). For another sociological perspective, 
see Susan P. Shapiro, Agency Theory, 31 ANN. REV. SOC. 263 (2005). 
29 See, e.g., MAES, supra note 21; Rao & George, supra note 21; Wooldridge & Jennings, 
supra note 21; SUTTON & BARTO, supra note 21; RUSSELL & NORVIG, supra note 21. 
Pioneering work was also conducted in the field of cybernetics. See Arturo Rosenblueth, 
Norbert Wiener & Julian Bigelow , Behavior, Purpose and Teleology , 10 PHIL. SCI. 18 
(1943); NORBERT WIENER, CYBERNETICS: OR CONTROL AND COMMUNICATION IN THE 
ANIMAL AND THE MACHINE (2nd ed. 1961 ); W. ROSS ASHBY, AN INTRODUCTION TO 
CYBERNETICS (1956). For a succinct survey of the literature, see Kenton et al., supra note 
21, at 3. Notably, the definition of agency in computer science differs from that  in law and 
economics. See, e.g., Franklin & Graesser, supra note 21, at 25 (“An autonomous agent is a 
system situated within and a part of an environment that senses that environment and acts on 
it, over time, in pursuit of its own agenda and so as to effect what it senses in the future”) ; 
RUSSELL & NORVIG, supra note 2 1, at 3–4 (“An agent is just something that acts (agent 
comes from the Latin agere, to do). Of course, all computer programs do something, but 
computer agents are expected to do more: operate autonomously, perceive their environment, 
persist over a prolonged time period, adapt to change, and create and pursue goals. ”). 
12 Governing AI Agents [11-Feb-25 
A.  Beyond Language Models 
 
Following the release of ChatGPT in November 2022, language models 
and generative AI have become ubiquitous.30 College students use language 
models to write term papers.31 Companies use image and video generators to 
produce marketing content.32 These applications, however, all share one thing 
in common: the AI systems function as tools. Individuals and companies  
decide whether or not to use a model, select which model to use, and deploy 
the model to perform a narrowly scoped task. A human remains, by and large, 
in full control. 
AI agents are different. They are not mere tools, but actors. 33 Rather than 
simply produce synthetic content, AI agents can independently accomplish 
complex goals on behalf of humans .34 According to Mustafa Suleyman, a 
cofounder of DeepMind and CEO of Microsoft AI, the next aspiration for the 
field of AI is to build agents that can pursue  “an ambiguous, open -ended, 
complex goal that requires interpretation, judgment, creativity, decision -
 
30 See, e.g., Krystal Hu, ChatGPT Sets Record for Fastest-Growing User Base, REUTERS 
(Feb. 2, 2023), https://www.reuters.com/technology/chatgpt -sets-record-fastest-growing-
user-baseanalyst-note-2023-02-01/. 
31 See Andy Extance , ChatGPT Has Entered the Classroom: How LLMs Could 
Transform Education, 623 NATURE 474 (Nov. 15, 2023). 
32 See Lauren Leffer,  Everything to Know About OpenAI’s New Text -to-Video 
Generator, Sora, SCI. AM. (Mar. 4, 2024), https://www.scientificamerican.com/article/sora-
openai-text-video-generator/. 
33 For surveys of the technology, see Toner et al., supra note 10; Wang et al., supra note 
12; Durante et al., supra note 12; Lilian Weng, LLM Powered Autonomous Agents, LIL’LOG 
(June 23, 2023), https://lilianweng.github.io/posts/2023-06-23-agent/; Theodore R. Sumers  
et al., Cognitive Architectures for Language Agents, TRANSACTIONS MACH. LEARNING RES. 
(2024), https://arxiv.org/abs/2309.02427. See also Matei Zaharia et al., The Shift from 
Models to Compound AI Systems , BERKELEY AI RES. (Feb. 18, 2024), 
https://bair.berkeley.edu/blog/2024/02/18/compound-ai-systems/. 
34 Examples of AI agent technology include Izzeddin Gur et al., A Real-World WebAgent 
with Planning, Long Context Understanding, and Program Synthesis , INT’L CONF. 
LEARNING REPRESENTATIONS (2024); Sirui Hong et al., MetaGPT: Meta Programming for 
A Multi-Agent Collaborative Framework, INT’L CONF. LEARNING REPRESENTATIONS (2024); 
John Yang et al., SWE-Agent: Agent -Computer Interfaces Enable Automated Software 
Engineering, PROC. 38TH CONF. NEURAL INFO. PROCESSING SYS. (2024). Benchmarks for 
evaluating AI agents include Xiao Liu et al., AgentBench: Evaluating LLMs as Agents, INT’L 
CONF. LEARNING REPRESENTATIONS (2024); Shuyan Zhou et al., WebArena: A Realistic Web 
Environment for Building Autonomous Agents , INT’L CONF. LEARNING REPRESENTATIONS 
(2024); Grégoire Mialon et al., GAIA: A Benchmark for General AI Assistants, INT’L CONF. 
LEARNING REPRESENTATIONS (2024); Carlos E. Jimenez et al., SWE-Bench: Can Language 
Models Resolve Real -World Git Hub Issues? , INT’L CONF. LEARNING REPRESENTATIONS 
(2024). For a critical perspective on methods for evaluating AI agents, see Sayash Kapoor et 
al., AI Agents That Matter, ARXIV (Jul. 1, 2024), https://arxiv.org/abs/2407.01502. 
11-Feb-25] Governing AI Agents 13 
making, and acting across multiple domains, over an extended time period.”35 
To make this concrete, consider the following example. Tasked with the 
goal of arranging an overseas vacation, an AI agent can break down the goal 
into smaller parts, devise a plan for achieving the goal, and proceed to execute 
a complex series of actions that result in achieving the goal.36 Concretely, the 
AI agent would need  to research prospective destinations, judge which of 
those destinations is most appropriate given a person’s preferences and 
budget, plan an itinerary, book flights and accommodation, arrange a visa or 
travel permit, and make necessary household arrangements for the duration 
of the vacation.  While AI agents are not yet able to  independently perform 
this entire series of actions, they are getting increasingly close.37 And fast.38 
 
B.  Goal, Plan, Action 
 
How do AI agents work? In short, they are comprised of a language model 
that serves as the agent’s “brain” ( a widely used anthropomorphism),39   
which can then use a variety of external resources (known as “scaffolding”) 
to accomplish the goals set for it. 40 These resources fall into three categories: 
planning, memory, and tool use. For planning, AI agents decompose large 
tasks into smaller, more manageable tasks.  One popular method involves 
 
35 SULEYMAN, supra note 16, at ch. 4. 
36 See, e.g., Jian Xie et al., TravelPlanner: A Benchmark for Real-World Planning with 
Language Agents, INT’L CONF. MACH. LEARNING (2024). 
37 This is primarily the case for AI agents that operate in digital environments, such as 
the internet. See supra note 34. However, AI agents are also being developed for physical 
environments, including robotic tasks and chemistry experiments. See Daniil A. Boiko et al., 
Autonomous Chemical Research with Large Language Models , 624 NATURE 570 (2023) ; 
Andres M . Bran et al., Augmenting Large -Language Models with Chemistry Tools , 6 
NATURE MACH. INTEL. 525 (2024); Michael Ahn  et al., AutoRT: Embodied Foundation 
Models for Large Scale Orchestration of Robotic Agents , ARXIV (Jul. 2, 2024), 
https://arxiv.org/abs/2401.12963. 
38 See Seth Lazar, Frontier AI Ethics, AEON (Feb. 13, 2024), https://aeon.co/essays/can-
philosophy-help-us-get-a-grip-on-the-consequences-of-ai (“While some existing chatbots 
are rudimentary generative agents, it seems very likely that many more consequential and 
confronting ones are on the horizon.  … [W]ith billions of dollars and the most talented AI 
researchers pulling in the same direction, highly autonomous generative agents will very 
likely be feasible in the near- to mid-term.”). 
39 See Weng, supra note 33; Sumers et al., supra note 33, at 10 (describing “robotic 
projects that leverage [language models] as a “brain” for robots to generate actions or plans 
in the physical world”). See generally id. (regarding the cognitive architecture of AI agents). 
For concerns regarding anthropomorphizing AI, see, e.g.,  Ryan Calo, Robotics and the 
Lessons of Cyberlaw , 103 CALIF. L. REV. 513, 545–46 (2015); Laura Weidinger  et al., 
Taxonomy of Risks Posed by Language Models , PROC. 2022 ACM CONF. FAIRNESS, 
ACCOUNTABILITY & TRANSPARENCY 214, 220 (2022). 
40 The explanation that follows draws significantly on Weng, supra note 33. 
14 Governing AI Agents [11-Feb-25 
agents literally instruct ing themselves to “think step by step”  when 
confronted with a new task.41 For memory, AI agents can use external storage 
sources, including vector databases, which enable fast retrieval of 
information needed to perform the task at hand.42 For tool use, AI agents call 
application programming interfaces (APIs) to access external websites and 
software, which significantly extend the agent’s abilities.43 For example, tool 
use can enable an AI agent to query a search engine, access an organization’s 
proprietary data, or provide user credentials to autonomously execute a 
financial transaction.44 
One prominent early example of an AI agent was AutoGPT,45 The agent, 
which was originally built on  OpenAI’s GPT-4 language model, could be 
instructed to conduct market research, build websites, order takeaway food, 
make phone calls, and even spawn its own subagents to assist in carrying out 
tasks.46 Admittedly, however, AutoGPT’s performance was not especially 
reliable. The agent also required user consent to authorize certain actions .47 
That being said, AutoGPT’s developers intended to incrementally relax this 
 
41 See Jason Wei  et al., Chain-of-Thought Prompting Elicits Reasoning in Large 
Language Models, PROC. 36TH CONF. NEURAL INFO. PROCESSING SYS. (2022). This method 
has been expanded upon in Shunyu Yao et al., Tree of Thoughts: Deliberate Problem Solving 
with Large Language Models , PROC. 37TH CONF. NEURAL INFO. PROCESSING SYS. (2023); 
Shunyu Yao et al., ReAct: Synergizing Reasoning and Acting in Language Models , INT’L 
CONF. LEARNING REPRESENTATIONS (2023); Noa Shinn et al.,  Reflexion: Language Agents 
with Verbal Reinforcement Learning , PROC. 37TH CONF. NEURAL INFO. PROCESSING SYS. 
(2023). The reasoning abilities of AI agents have dramatically improved with the advent of 
models that spend more time “thinking” , i.e., use more test-time compute . See OpenAI, 
Learning to Reason with LLMs, OPENAI (Sept. 12, 2024), https://openai.com/index/learning-
to-reason-with-llms/. 
42 See Sumers et al., supra note 33, at 9–10. 
43 See Timo Schick et al., Toolformer: Language Models Can Teach Themselves to Use 
Tools, PROC. 37TH CONF. NEURAL INFO. PROCESSING SYS. (2023); Grégoire Mialon  et al., 
Augmented Language Models:  A Survey , TRANSACTIONS MACH. LEARNING RES. (2023), 
https://arxiv.org/abs/2302.07842; Yuji Qin et al., ToolLLM: Facilitating Large Language 
Models to Master 16000+ Real -World APIs , INT’L CONF. LEARNING REPRESENTATIONS 
(2024). 
44 See Seth Lazar, The Rise and Fall (and Rise Again) of the First AI Agent Millionaire, 
TECH POLICY PRESS (Oct. 25, 2024), https://www.techpolicy.press/the-rise-and-fall-and-
rise-again-of-the-first-ai-agent-millionaire/. 
45 See Significant-Gravitas, AutoGPT, GITHUB (Mar. 30 , 2023), https://github.com/ 
Significant-Gravitas/AutoGPT; Kyle Wiggers, What is Auto-GPT and Why Does It Matter?, 
TECHCRUNCH (Apr. 22, 2023), https://techcrunch.com/2023/04/22/what-is-auto-gpt-and-
why-does-it-matter/. For related work, see Yohei Nakajima, BabyAGI, GITHUB (Apr. 2023), 
https://github.com/yoheinakajima/babyagi; Erik Bjare, GPT-Engineer, GITHUB (June 2023). 
46 See Dan Murray-Serter (@danmurrayserter), X (TWITTER) (Apr. 24, 2023, 5:00PM), 
https://twitter.com/danmurrayserter/status/1650499941775679488 . 
47 See AutoGPT Agent Documentation, https://docs.agpt.co/autogpt/. 
11-Feb-25] Governing AI Agents 15 
requirement and grant the agent greater autonomy.48 
To the extent AI agents become more reliable and are used more widely, 
new social and economic dynamics are likely to  emerge. For example, 
interpersonal encounters might be increasingly mediated or even altogether 
obviated by AI agents.49 An uncomfortable conversation with a colleague or 
a complaint to the local council could be outsourced to a person’s AI agents. 
Similarly, parties to a  business transaction could delegate certain 
responsibilities to their respective AI agents .50 While these developments 
could offer consumers and businesses substantial productivity gains, they 
also raise noteworthy concerns. 
 
C.  Concerns 
 
The range of risks posed by AI technology, including language models, 
is wide and growing. It includes risks of “hallucinations,” toxic outputs, bias, 
discrimination, environmental harms, and leakage of sensitive personal data, 
to name just a few.51
```
