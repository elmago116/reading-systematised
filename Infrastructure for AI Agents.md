---
title: Infrastructure for AI Agents
author: Alan Chan, Jesse Clifton, et al.
year: "2025"
Type: ""
DOI: 10.48550/arXiv.2501.10114
source: ""
created: 2026-06-18
description: ""
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics/norms
pdfORepub: "[[Infrastructure for AI Agents.pdf]]"
---
[[Infrastructure for AI Agents.pdf]]

## Full text (extracted from `Infrastructure for AI Agents.pdf`)

*Source:* `2PDF/Infrastructure for AI Agents.pdf`  
*Extracted:* 2026-06-18

```text
arXiv:2501.10114v3  [cs.AI]  19 Jun 2025
Infrastructure for AI Agents
Alan Chan∗
Centre for the Governance of AI
Kevin Wei
Harvard Law School
Sihao Huang
University of Oxford
Nitarshan Rajkumar
University of Cambridge
Elija Perrier
Australian National University
Seth Lazar†
Australian National University
Gillian K. Hadfield†
Johns Hopkins University
Markus Anderljung†
Centre for the Governance of AI
Abstract
AI agentsplan and execute interactions in open-ended environments. For example, Ope-
nAI’s Operator can use a web browser to do product comparisons and buy online goods.
Much research on making agents useful and safe focuses on directly modifying their be-
haviour, such as by training them to follow user instructions. Direct behavioural modifica-
tions are useful, but do not fully address how heterogeneous agents will interact with each
other and other actors. Rather, we will need external protocols and systems to shape such
interactions. For instance, agents will need more efficient protocols to communicate with
each other and form agreements. Attributing an agent’s actions to a particular human or
other legal entity can help to establish trust, and also disincentivize misuse. Given this mo-
tivation, we propose the concept ofagent infrastructure: technical systems and shared
protocols external to agents that are designed to mediate and influence their interactions
with and impacts on their environments. Just as the Internet relies on protocols like HTTPS,
our work argues that agent infrastructure will be similarly indispensable to ecosystems of
agents. We identify three functions for agent infrastructure: 1) attributing actions, proper-
ties, and other information to specific agents, their users, or other actors; 2) shaping agents’
interactions; and 3) detecting and remedying harmful actions from agents. We provide an
incomplete catalog of research directions for such functions. For each direction, we include
analysis of use cases, infrastructure adoption, relationships to existing (internet) infrastruc-
ture, limitations, and open questions. Making progress on agent infrastructure can prepare
society for the adoption of more advanced agents.
∗Correspondence to alan.chan@governance.ai
†Senior authors.
1
1 Introduction
A fundamental goal of the AI research community is to buildAI agents: AI systems that can plan and
execute interactions in open-ended environments,1 such as making phone calls or buying online goods (Maes,
1994; 1995; Lieberman, 1997; Jennings et al., 1998; Johnson, 2011; Sutton & Barto, 2018; Russell & Norvig,
2021; Chan et al., 2023; Shavit et al., 2023; Wu et al., 2023; OpenAI, 2018; Gabriel et al., 2024; Kolt, 2024;
Lazar, 2024). Agents differ from other computational systems in two significant ways. First, in comparison
to foundation models used as chatbots, agents directly interact with the world (e.g., a flight booking website)
rather than only with users. Second, in comparison to traditional software (e.g., an implementation of a
sorting algorithm), agents can adapt to under-specified task instructions. Although the AI community has
been developing agents for decades, these agents typically performed only a narrow set of tasks (Wooldridge,
2009; Mnih et al., 2013; Silver et al., 2018; Badia et al., 2020). In contrast, recent agents built upon language
models can attempt—with varying degrees of reliability (Kapoor et al., 2024; Liu et al., 2023; Mialon et al.,
2023; Lu et al., 2024; Zhang et al., 2024)—a much wider array of tasks, such as software engineering (Jimenez
et al., 2024; Wu, 2024; Chowdhury et al., 2024) or office support (Gur et al., 2024; MultiOn, 2024).
Agent Agent  
infrastructure 
Legal system
Other agents
Digital service 
providers 
Figure 1:Agent infrastructureconsists of technical systems and shared protocols external to agents that
are designed to mediate and influence their interactions with and impacts on their environments, including
interactions with existing institutions (e.g., legal and economic systems) and actors (e.g., digital service
providers, humans, other AI agents).
More general-purpose agents could automate a wide range of both beneficial and harmful tasks. Personalized
agentscouldhelpindividualsmakeawidevarietyofdifficultdecisions, suchaswhatinsurancetobuyorwhich
school to attend (Van Loo, 2019; Sunstein, 2024; Lazar et al., 2024). Deployment of agents throughout the
economy could lead to productivity growth (Korinek & Suh, 2024). Yet, barriers such as a lack of reliability,
an inability to maintain effective oversight, or the absence of recourse mechanisms could hinder beneficial
adoption. On the other hand, such barriers may not be critical for motivated malicious actors. Potential
issues include scams (Fang et al., 2024b; Chen & Magramo, 2024) and large-scale disruption of digital services
(Fang et al., 2024a; Bhatt et al., 2023; U.S. Attorney’s Office, 2024).
To facilitate beneficial tasks and mitigate harmful ones, much AI research focuses onsystem-level inter-
ventions, which intervene on the AI system itself to shape its behaviour. Major areas of work include goal
specification and following (Hadfield-Menell et al., 2016; Christiano et al., 2017; Leike et al., 2018; Bai et al.,
2022; Hua et al., 2024; Wang et al., 2024a;b; Kirk et al., 2024; Huang et al., 2024; OpenAI, 2024), adversarial
robustness (Greshake et al., 2023; Tamirisa et al., 2024; Zou et al., 2024; Anil et al., 2024; Wallace et al.,
2024), and cooperation (Lerer & Peysakhovich, 2019; Hu et al., 2020; Leibo et al., 2021; Dafoe et al., 2021).
System-level interventions, if adopted (Askell et al., 2019), can help to improve the reliability of agents, but
they may not be sufficient for facilitating beneficial adoption or mitigating risks. For example, the difficulty
1Gabriel et al. (2024) heavily inspire this definition. See (Maes, 1994; Sutton & Barto, 2018; Chan et al., 2023; Shavit et al.,
2023; Kolt, 2024; Lazar, 2024) for other definitions.
2
Function Research directions
Attribution (Section 3):
Attributing actions, prop-
erties, and other informa-
tion to agents or users
• Identity binding (Section 3.1): Associates an agent or its
actions with a legal identity, such as a human or corporation.
• Certification (Section 3.2): Makes, verifies, and revokes
claims about an agent (instance), such as what data the agent
is collecting, which tools it can access, and the level of auton-
omy it has been authorized to exercise.
• Agent IDs(Section 3.3): Identifies instances of agents and
links to useful attributes, such as the credentials above.
Interaction (Section 4):
Shaping how agents inter-
act with counterparties.
• Agent channels(Section 4.1): Isolates agent traffic from all
other digital traffic in interactions with an existing digital ser-
vice (e.g., Airbnb).
• Oversight layers(Section 4.2): Enables actors (e.g., a user)
to intervene upon an agent’s actions.
• Inter-agent communication(Section 4.3): Helps facilitate
joint activities amongst groups of agents.
• Commitment devices(Section 4.4): Enforce commitments
between agents.
Response (Section 5):
Addressing problems that
occur during interaction
with an agent.
• Incident reporting(Section 5.1): Enables actors (e.g., hu-
mans, agents interacting with other agents) to report inci-
dents.
• Rollbacks (Section 5.2): Helps void or undo an agent’s ac-
tions.
Table 1: This table summarizes all of the types of agent infrastructure that we discuss in this work.
of achieving adversarial robustness could mean that companies need additional assurances before adopting
agents to complete economically valuable tasks. In particular, potential assurance schemes include certifi-
cation of agents, insurance, or identity solutions that establish trust between different parties using agents.
Such tools shape how agents interact with institutions (e.g., legal and economic systems) and other actors
(e.g., web service providers, humans, other AI agents).
Given the insufficiency of system-level interventions, we propose the concept ofagent infrastructure:
technical systems and shared protocols external to agents2 that are designed to mediate and influence their
interactions with and impacts on their environments.3 These systems and protocols could be novel, or
simply extensions of existing systems and protocols. Examples of agent infrastructure include inter-agent
communication protocols (Marro et al., 2024), IDs for agents (Chan et al., 2024b), systems for certifying
an agent’s properties or behaviour, and methods for rolling back an agent’s actions (Patil et al., 2024). We
include more examples in Table 1. Our notion of agent infrastructure isnot about the technical systems that
enable basic operation of agents (e.g., memory systems, cloud compute), although it will in practice often
build upon or modify such systems. Furthermore, while our discussion will be grounded in language-model-
2I.e., they are not system-level interventions.
3See Section 7 for a comparison of agent infrastructure with adaptation interventions (Bernardi et al., 2024), which roughly
include any intervention that is not a system-level intervention.
3
Domain System-level Infrastructure
AI-agent
safety
Fine-tuning, prompting, unlearning,
filtering training data
Protocol to forget confidential infor-
mation from an interaction, technolo-
gies to enable agent certification, dis-
tinct interaction interfaces for agents
Traffic safety Driver training programs Traffic lights, roundabouts, emer-
gency lanes, camera-enforced speed
limits
Health Medication, exercise Hospitals, emergency response sys-
tems, parks for exercise
Table 2: We compare analogues to system-level interventions and agent infrastructure across different do-
mains. These categories of interventions are often complementary.
based agents, the core ideas of agent infrastructure are largely architecture-agnostic and extend existing
work across computational science, economics, and social science (Wooldridge, 2009; Perrier, 2025).
To further understand the distinctions between agent infrastructure and system-level interventions, consider
traffic safety as an analogy. If we treat human drivers as analogous to AI agents, system-level interventions
includes driver training programs. Infrastructure could include traffic lights, roundabouts, emergency lanes,
and camera-enforced speed limits. We provide more comparisons in Table 2.
Just as the Internet relies on infrastructure like TCP (Eddy, 2022), HTTPS (Fielding et al., 2022), and BGP
(Rekhter et al., 2006), we argue that agent infrastructure will likely be crucial for unlocking the benefits
and managing the risks of agents. As an example of unlocking benefits, protocols that tie an agent’s actions
to a user could facilitate accountability and thereby reduce barriers to agent adoption. Analogously, the
ability to perform secure financial transactions over HTTPS enables an e-commerce market in the trillions
of dollars (Statista, 2024). As an example of managing risks, agent infrastructure can support system-level
interventions. For instance, a certification system for agents could warn actors (e.g., other agents) not to
interact with agents that lack certain safeguards, just as browsers flag non-HTTPS websites. In this way,
agent infrastructure can use agents’ interactions as a leverage point to improve safety: restricting an agent’s
interactions correspondingly restricts the agent’s potential negative impacts.
This work identifies three functions that agent infrastructure could serve: 1) attributing actions, properties,
and other information to specific agents or other actors; 2) shaping agents’ interactions; and 3) detecting and
remedying harmful actions from agents. We propose infrastructure that could help achieve each function,
including analysis of use cases, adoption, limitations, and open questions. Our suggestions are primarily
aimed at researchers and developers who may want to build agent infrastructure. These suggestions could
also be useful to governments or funding bodies who may want to support its construction.
2 Agent Infrastructure
2.1 Categories of Agent Infrastructure
We focus on agents that interact with digital environments. Roughly speaking, we consider an agent to
consist of the underlying machine-learning model and any primitives that provide basic functionality (e.g.,
memory, scaffolding). Language-model agents commonly act by issuing commands to tools, such as APIs
that return the output of a separate software service (e.g., the weather).4 Environments consist of such tools
and any counterparties that interact with an agent (e.g., other agents, humans).
Some agent infrastructure applies to instances of agents. An agent instance is an instantiation of the
underlying machine-learning model and any primitives for a particular user. Specifically, an instance would
correspond to an interaction history, a set of available tools, memory, etc., much like process IDs in operating
4See Wooldridge (2009); Perrier & Lazar (2025) for further discussion of ontologies of agents.
4
systems correspond to running instances of programs.5 Agent instances are a useful concept because different
instances of the same underlying model and primitives can have different users or behave differently, and
therefore potentially justify different treatment.
We identify three functions of agent infrastructure.Attribution is about attributing actions, properties,
and other information to (instances of) agents, users, or other actors.Interactionis about shaping agents’
interactions with the world. Finally, response is about detecting and remedying harmful actions from
agents. To maintain a manageable scope, we do not discuss how infrastructure could help to manage more
diffuse potential impacts, such as widespread unemployment. We summarize all the infrastructure we discuss
in Table 1.
Infrastructure could be implemented both within a particular organization and between organizations or
actors. Consider communication protocols as an example. In the first case, a business could use commu-
nication protocols to manage its agents internally, much as infrastructure like Slack and Google docs helps
human employees work together. In the second case, a common communication protocol could help agents
from different organizations communicate efficiently over the internet (Marro et al., 2024; Surapaneni et al.,
2025). Adoption of agent infrastructure is likely more difficult in the second case, given that different ac-
tors could use mutually incompatible communication protocols (see Section 6.1). Our presentation of agent
infrastructure is meant to cover both of these cases. For each piece of infrastructure that we present, we
analyze how adoption could proceed at internet-wide scale.
2.2 Example
To illustrate how agent infrastructure could work, consider the task of running a company. In this hypothet-
ical company, agents would perform or assist with the work that human employees would usually perform,
such as operations, R&D, and legal tasks. Agent infrastructure could enable the following functions for this
agent-run company.
• Human review: Human managers can make use of oversight layers (Section 4.2) to ensure that their agent
employees are not malfunctioning.
• Coordination: A communication protocol (Section 4.3) and commitment devices (Section 4.4) can facil-
itate coordination between agents both within a company and from different companies. For example,
agents could make commitments to carry out certain tasks, much as companies create contracts.
• Accountability: A lack of accountability mechanisms could discourage interaction with the company’s
agents. One way to address this issue is by ensuring that each agent has at least one human that can
answer for the agent’s actions (Section 3.1), and making this information available to those that interact
with the company’s agents or a third-party mediator.
• Undoing mistakes: Rollback mechanisms (Section 5.2) enable certain decisions, such as updates to com-
pensation or internal data management processes, to be easily undone if an agent makes a mistake.6
2.3 Prioritization
We discuss some considerations for prioritization of certain types of agent infrastructure.
The effectiveness of certain infrastructure depends heavily on widespread adoption. For example, inter-agent
communication protocols are only useful if both parties can use the same protocols. Agent IDs are also only
useful if other parties can recognize them. On the other hand, oversight layers and rollbacks are immediately
useful for addressing agent malfunction, even if few actors adopt them. For actors that are heavily resource-
constrained, such considerations could suggest focusing on infrastructure that does not require widespread
adoption.
5An instance is an abstraction and may not correspond to a hardware separation. For example, inference calls for different
instances could be batched together on the same piece of hardware.
6The conditions under which a decision should be undone is a separate question. Rollback mechanisms merely provide
flexibility.
5
Some infrastructure is only useful once agents obtain certain capabilities. For example, commitment devices
are most useful when agents are capable of negotiating and carrying out complex agreements. Infrastructure
for capabilities that are further off could be delayed.
Different types of infrastructure are useful for different threat models. For example, inter-agent communi-
cation protocols and commitment devices are most important for avoiding cooperation problems between
agents (Hammond et al., 2025). Oversight layers and rollbacks are most useful for cases of misuse or mis-
alignment. Other infrastructure, such as identity binding and agent IDs, can both facilitate cooperation and
help to address harms.
We take no explicit stance on prioritization and leave further analysis to future work.
3 Attribution
Attributioninfrastructureattributesactions, properties, andotherinformationto(instancesof)agents, users,
or other actors.Identity bindinglinks an agent or its actions to an existing legal identity.Certification
would provide assurance about behaviour and properties of an agent instance. Anagent IDwould be a
container of information about an agent instance, such as associated certifications. In Figure 2, we depict
how these pieces of infrastructure fit together.
Agent takes Action aﬀects Counterparty
CertiﬁcationAgent ID
given to
associated with
User
Identity binding
Figure 2: Identity bindinglinks an agent or its actions to an existing legal identity,certification would
provide assurance about behaviour and properties of an agent instance, and anagent IDs would be a
container of information about an agent instance. We illustrateidentity bindingfor a user, but an agent
could also be bound to other actors, such as those involved in overseeing it
3.1 Identity Binding
Description: AI agents are not legal entities7. The ability (but not necessarily the requirement) to asso-
ciate an agent’s actions with a legal entity, such as a human or a corporation, could help existing institutions
accommodate agents. For example, an agent’s VOIP calls could be tagged with the identity of the person
controlling the agent, so as to enhance accountability for agent-enabled scams (Fang et al., 2024b). Anal-
ogously, cars are associated to drivers through license plates and registries. Such binding could be helpful
even when the relevant legal entity is not fully responsible for all of the agents’ actions. For example, in
addition to the employee using an agent, managers reviewing the agent’s actions and the corporation hiring
the employee could potentially bear some responsibility. With this motivation, we defineidentity binding
to be a process that consists of (1) authentication of an identity and (2) linking that identity to an (instance
of an) agent or its actions. Crucially, linking an identity to an agent does not mean making the identity
publicly visible. For example, identity information could be accessible only to authorized parties, such as if
needed for legal action, or only reveal limited information, such as the fact that a real person is responsible for
7Some argue that sufficiently capable future agents should have legal rights (Salib & Goldstein, 2024).
6
the agent (Adler et al., 2024). Further below, we discuss how existing infrastructure could help accomplish
(1) and (2), along with modifications that may be needed.
Potential functions:
• Accountability: Malicious uses of agents could be harder to address if all agents acted anonymously. For
example, anonymity enables Sybil attacks, wherein someone creates multiple fake identities to undermine
a network (e.g., an online voting system).
• Trust: Counterparties could be more willing to engage in productive interactions with agents that are
bound to legal entities because it could be easier to obtain recourse in case of harm. Analogously, identity
verification of drivers reassures users that would otherwise be dissuaded from ridesharing by personal
safety considerations.
• Application of laws: Identity binding could allow the broader application of existing laws to interactions
between agents. For example, at least as a starting point, identity binding could provide evidence that
an agent did indeed enter into a contract on behalf of a particular principal (Benthall & Shekman, 2023;
Aguirre et al., 2020).
Existing alternatives: Existing technologies can provide some functionality for authentication and identity
linking, but have limitations. User authentication is already required for many digital services, such as
banking (through know-your-customer regulations) or services requiring an account (through logging in with
OAuth). The actions of agents interacting with such services would by default be attributable to the user.
However, some services only provide attribution to a pseudonymous internet user, rather than a specific
legal entity. In addition, there is currently no comparable authentication system for agent-agent interactions
or actors other than users. The former may be important for agents that are significant economic actors,
whereas the latter could include actors that assume responsibility for some of the agent’s actions (e.g., an
insurance company) or other overseers of the agent.
Identity information could be linked to an agent in a variety of ways. Drawing from work on content
provenance (e.g., (C2PA, 2023)), identity information can be included as metadata or as a watermark.
However, metadata can be stripped from content and watermarks can potentially be removed (Zhang et al.,
2023). Furthermore, privacy considerations could weigh against revealing identity information in this way.
If so, a potential alternative could be to establish a trusted intermediary that would hold this identity
information (Kling et al., 1999). Counterparties could request that this intermediary reveal the information
or use it appropriately in the event it is needed. As an analogy, ISPs can share information about their
users in response to a criminal investigation. It remains to be seen how such a function could be provided
for agents.
Adoption: Digital platforms are likely to be crucial for the widespread adoption of identity binding. First,
users might be more likely to engage with platforms that include or require identity binding. Some evidence
suggeststhatcontractorsuseAIsystemsonplatformslikeUpwork(Veselovskyetal.,2023). Dharmesh(2024)
is also creating a service where AI agents play the role of crowdworkers and are matched to tasks. In both of
these cases, customers are likely to engage more fully if they know there is a person ultimately responsible for
the service, similar to identity verification for gig economy services (Uber, 2025; DoorDash, 2025). Second,
platforms might require identity binding to avoid Sybil-like attacks. For example, an individual recently
defrauded Spotify of millions of dollars by synthetically generating music and creating multiple fake accounts
to stream it (U.S. Attorney’s Office, 2024). Third, identity binding could be a natural extension existing
single sign-on practices. For example, a Google account can already be used to log on to many non-Google-
owned different websites and services.
Limitations: Identity binding entails at least some collection and use of user information, even if that
information is only shared with authorized actors when needed. Security vulnerabilities analogous to those
in existing authentication systems could compromise user information (Batra et al., 2024; Microsoft Threat
Intelligence, 2023). More broadly, reduced anonymity (or the threat of reduced anonymity) could threaten
personal safety (e.g., doxxing), hinder whistleblowing, and reduce expression of novel ideas (Kling et al.,
1999; Zittrain, 2006; Choi, 2012; Kang et al., 2013). Such concerns imply that identity binding may not be
appropriateineveryapplicationofagents, andproportionateconfidentialityprovisionswillbenecessarywhen
7
it is used. Analogously, although it can be abused, legislatures and courts have recognized the importance
of identification of internet users under certain conditions (Ekstrand, 2003; Choi, 2012; noa, 2018).
Research questions:
• What kinds of actions can and should be linked to identities? For example, it is likely infeasible to link
mouse clicks to agents. Would it be preferable to link groups of actions instead?
• What key applications of agents could identity binding enable?
• How can identity binding build upon existing digital identity solutions, such as (national) digital wallets
or single sign-on?
• If intermediaries hold identity information, who should be able to request access to or use of the informa-
tion, such as for obtaining recourse? Under what conditions should such access or use be granted?
3.2 Certification
Description: Before interacting with an agent (instance), counterparties might want assurances about its
operation, behaviour, or properties. For example, agents whose actions are regularly reviewed could be more
trustworthy than agents who do not undergo such review. Claims about operation, behavior, or properties
could come from a user, an agent deployer, or other actors (e.g., third-party auditors). Certificates including
such claims could be associated with the relevant agent and made visible to counterparties interacting with
it. Analagously, SSL certificates make claims to website users about domain ownership. Certification
infrastructure consists of tools for making, verifying, and revoking certificates for agents. Verification
includes how those viewing a certificate can verify both its claims and that it corresponds to the agent with
which they are interacting.
Example claims: We provide potential example claims of an agent’s operation, behavior, or properties
that could be included in a certificate.
• The tools the agent can access: Certain tools, such as commitment devices (Sun et al., 2023), could make
agents more reliable or useful.
• Capabilities, accounting for post-training modifications: Weaker agents could be more susceptible to
prompt injections from stronger agents (e.g., stronger agents could be more capable at detecting such
attempts). If so, a user might want their agent only to interact with agents that are at most as strong
as their agent. Accounting for post-training modifications would likely involve analysis of an agent’s
behaviour log. Doing so in a privacy-preserving way is an open problem (Trask et al., 2023; 2024).
• The level of autonomy with which the agent is authorized to act: Agents that act with more regular hu-
man oversight could be, but are not necessarily (Parasuraman & Riley, 1997; Skitka et al., 1999; Green,
2022), more trustworthy.
• How an agent handles sensitive information: For example, an agent could follow a protocol to delete
sensitive information from context and memory after use (Rahaman et al., 2024).
Potential functions:
• Trust: Certificates for safety-relevant properties can build trust in agent interactions. For such trust not
to be misplaced, a certificate should at minimum only contain claims about what can feasibly be known
about the agent, given the state of the science. For example, it may be difficult to provide useful bounds
on whether an agent will ever violate a safety constraint.
• Races to the top: If counterparties can selectively interact with agents that have certificates for pro-
social properties (e.g., that use cooperation mechanisms (Sun et al., 2023)), developers and users could
be incentivized to respectively develop and use agents with those properties.
• Supporting recourse: Certain forms of recourse (e.g., undoing an action; see Section 5.2) could rely on an
auditor to certify that, for example, an agent was prompt injected.
8
Existing alternatives: Auditing of companies involved in the development or use of agents, such as
developers or cloud compute providers, can be a component of certification of agents. For example, an
auditor could verify that a cloud compute provider has policies for only running agents that have passed
certain safety standards. Yet, certifying such companies could be ineffective if large numbers of users modify
and deploy their own agents.
In the absence of any additional certification infrastructure, developers, deployers, and users could make
their own claims about their agents. However, counterparties may be unable to assess the veracity of such
claims. Evaluating AI systems is not straightforward and empirical experiments can be subtly misleading
(Leech et al., 2024). Even so, entities may still be able to assess the quality of an agent’s actions and reject
them if necessary. For example, a counterparty may not know in general how reliable a software engineering
agent is, but could run software to verify the correctness of the agent’s code.
Adoption: Demand for certification is likely to vary across domains and contexts. For instance, protocols for
forgetting sensitive information can enable agreements that would otherwise not be possible (Rahaman et al.,
2024). Certifying that an agent can follow such protocol seems more important for high-stakes negotiations.
Feasibility and economic cost could also affect demand. For example, properties that require access to
interaction logs (e.g., whether a prompt injection is present) could raise privacy concerns, in the absence of
privacy-preserving certification methods (Trask et al., 2023; 2024). That said, demand for certification could
be high for agent use within government and regulated areas (e.g., health). Analogously, software products
in such domains often have to meet quality standards (e.g., Health and Human Services Department & Food
and Drug Administration (1996)).
Finally, as discussed above, developers and deployers could support certification as a way to credibly signal
the trustworthiness of their agents.
Limitations: It could be impossible or extremely difficult to verify certain properties. Providing meaningful
guarantees about the behavior of a system in general is an active area of research (Dalrymple et al., 2024).
If meaningful guarantees are not technically possible, certifications could provide a false sense of security.
Other properties could be feasible, but potentially impractical or invasive, to certify. A potential example
could be whether an agent has interacted with a particular, other agent.
Furthermore, actors creating certificates for agents could be incompetent, captured, or fail to perform any
useful certification. A notable case is TrustARC (formerly TRUSTe), who provided privacy certification for
websites. Although TrustARC claimed to verify website privacy policies, it often did not conduct any such
checks whatsoever (Connolly et al., 2014). Surprisingly, as an example of adverse selection, Edelman (2009)
provides evidence that websites that obtained TrustARC certification were significantly less trustworthy
than websites without it. potential Ways to address this problem include oversight over actors performing
certification of agents and transparency requirements about their processes.
Research questions:
• For the example claims we list above, who should be making the claims? How could the claims be verified?
• What other claims about an agent would be useful to make?
• How can actors verify that a certificate corresponds to the agent instance with which they are interacting?
• Under what conditions should a certificate be revoked? For example, claims about an agent’s future
behavior could become outdated the longer the agent operates.
• How would certification of agents interact with existing auditing practices and regimes (Raji et al., 2020;
2022)?
• How could existing infrastructure (e.g., verifiable credentials (Sporny et al., 2024)) support certification
of agents?
• What existing certification methods in information systems and cybersecurity could provide useful inspi-
ration (Oberkampf & Roy, 2010; Perrier, 2025; Perrier & Lazar, 2025)?
9
• What oversight or transparency requirements should exist for actors providing certificates for agents?
• What recourse should be available if certificates contain mistakes or are otherwise compromised in some
way?
3.3 Agent IDs
Description: An agent IDwould at minimum consist of a unique identifier8 for an agent instance, and
potentially include other information relevant to the instance, such as a system card or certifications (Chan
et al., 2024b). ID-like systems exist across many domains to facilitate identification, such as serial numbers
on consumer products, tail numbers on aircraft, registration numbers for businesses, and URLs/URIs to
locate resources on the internet. Although any AI system could have an ID, IDs could be significantly more
useful for agents because they take actions in the world (see below).
Potential functions: Many of these uses draw from Chan et al. (2024b).
• Supporting certification: An ID could present an agent’s certifications (Section 3.2) and bound identities
(Section 3.1) to entities that seek to engage with it.
• Incident response: IDs could provide information that is useful for incident response. For example, an
agent could create sub-agents to split up a harmful task into multiple sub-tasks (Jones et al., 2024). An
ID could link the activities of these sub-agents to the original agent. An ID could also be useful for
detecting cross-platform incidents, where an agent harms multiple counterparties.
• Enabling targeted action against particular agents: Much like how process IDs in operating systems en-
able monitoring and resource restriction, an ID could enable interventions on the agents that are causing
harm.
Existing alternatives: For agents that interact with digital services, OAuth tokens or (read-only) API
keys could aid incident attribution. However, such tools do not apply to interactions between agents. These
tools are also service-specific. For example, an OAuth token cannot link the activity of an agent across
different counterparties, nor can it link the activities of sub-agents to the agent that created them.
IP addresses could also help incident attribution, but may not reliably identify an agent instance. Indeed,
they may not be static and can also be shared amongst different internet users.
Adoption: Identifiers could be a part of existing obligations to inform humans when they are interacting
with AI systems (noa, 2024, Art. 50(1)). As agents are assigned increasingly complex roles, counterparties
could demand more information from IDs so as to ensure reliable interactions (e.g., through certification)
and facilitate incident attribution.
Counterparties that expect only to interact with agents (or which only interact with agents through specific
channels [Section 4.1]) could require IDs before an interaction. Other counterparties which also interact
with systems other than agents may have more difficulty doing so. For example, suppose a counterparty
engages with both agents and traditional software programs. Extending an ID system from agents to all
software programs could be infeasible, since traditional software programs do not have IDs. A potential
stopgap measure could be CAPTCHA-like methods (Tatoris et al., 2025). The effectiveness of this measure
depends upon whether agent behaviour is distinguishable from human and other bot behavior, such as
through adversarial vulnerabilities.
Limitations: IDs could allow attackers to target particular agents and their users. If activity associated
with an ID is logged, leaks of such information could allow attackers to identify high-value targets. Knowing
an agent’s frequently used services could also facilitate exploits like prompt injections (e.g., attackers could
infect particular websites). When interacting with a particular agent, attackers could exfiltrate information
or jailbreak the agent to act on the attacker’s behalf, such as by performing financial transfers.
IDs could also be stolen or otherwise compromised. For example, IDs that depend on certificate authorities
are vulnerable to existing security vulnerabilities (Berkowsky & Hayajneh, 2017).
8A cryptographic scheme is necessary to prevent spoofing of the identifier. See Chan et al. (2024b) for more details.
10
Research questions:
• How could IDs complement existing tools for incident investigation?
• Where should IDs be required, and what information should an ID include?
• How can counterparties incentivize or enforce ID usage (e.g., by making sure that agents use unique
channels (Section 4.1))?
• When should IDs link to information identifying the user?
• What should entities be allowed to do with an identifier? For example, should an entity with an identifier
be allowed to contact the associated agent, or otherwise interact with it?
• What other systems need to be in place to make IDs more useful? E.g., should there be a registry of
certain agent IDs or a reviewing system?
• How can the design of IDs avoid known problems with existing Internet infrastructure (e.g., certificate
authorities) (Berkowsky & Hayajneh, 2017; Dumitrescu & Pouwelse, 2024)?
• How can the design of IDs limit abuse (e.g., attackers use IDs to target particular agents and their users)?
4 Interaction
Interaction infrastructure consists of protocols and affordances to shape how agents interact with their
environments. Agent channelswould isolate agent traffic from other traffic.Oversight layerswould
enable actors to intervene on an agent’s behaviour.Inter-agent communicationprotocols would help to
facilitate joint activities amongst groups of agents.Commitment devicesare mechanisms that enforce
commitments between agents. We depict these pieces of infrastructure in Figure 3.
4.1 Agent Channels
Description: For interactions with a digital service (e.g., payment services), anagent channel would
separate agent traffic (or AI traffic in general) from other digital traffic. An agent channel could, for example,
facilitate incident management by temporarily suspending access if a language-model worm spreads (Cohen
et al., 2024; Gu et al., 2024). Traffic separation is common across many applications. For example, digital
payments companies isolate systems that handle cardholder data (Council, 2016). Some hospitals separate
networks for storing and using different kinds of medical data, so as to safeguard privacy in case one network
is compromised (Digital, 2023). Wi-Fi routers provide guest networks that restrict the activity of unfamiliar
devices.
There are two axes of design considerations for agent channels. First, agent channels could be different
software interfaces or protocols for agents, or could take the form of more dedicated internet infrastructure.
Asexamplesoftheformer, thereareeffortstobuildagent-specificwebbrowsers(Turow,2024)andinteraction
protocols (Kaliski, 2024; Anthropic, 2024b). As examples of the latter, agents could have a dedicated block
of IP addresses (which could perhaps function as IDs Section 3.3), or separate routing systems could handle
agent traffic.
The second axis is how to operationalize traffic separation. Rate limits on human channels and the relative
absence or weakening of such limits on agent channels could incentivize the use of the latter. However, it
may in practice be difficult to separate agent or AI traffic from software traffic in general. For example,
agents could write software that interacts with counterparties.9
Potential functions:
• Monitoring: Separate transaction data for agents, for example, can help to understand the potential
macroeconomic effects of high volumes of agent activity (Van Loo, 2019).
9If agents come to mediate large fractions of digital interactions, there may be very little software that is not related to an
agent in some way.
11
Agent 
channels
Existing  
interfaces 
Agent Counterparty 
Oversight 
layers
Behaviour 
Agent Inter- agent 
communication  Agent 
Commitment 
devices
i n t e n d e d   
a c t i o n 
c r e d i b l e   
c o m m i t m e n t 
Figure 3: Agent channels separate agent traffic from other digital traffic. Oversight layers enable
actors to intervene on an agent’s behaviour.Inter-agent communicationhelp to facilitate joint activities
amongst groups of agents.Commitment devicesenforce commitments between agents. See Section 4 for
discussion.
12
• Managing incidents: Isolation of traffic could help to manage incidents. For example, providers of services
could shut down agent channels, but not human channels, to restrict spread of a text or image worm
(Cohen et al., 2024; Gu et al., 2024).
• Enforcing agent-specific rules: Agent channels could implement rules to support reliable agent use, such
as around rolling back unintended actions (Section 5.2) or how to handle sensitive data.
• Reduced attack surface: Human graphical interfaces have a large attack surface. For example, impercep-
tible changes to a website page could hide a prompt injection. APIs designed for agents could reduce this
attack surface, although text-based prompt injections would still be possible.
• Supporting IDs: As discussed in Section 3.3, agent channels could make it more feasible to require IDs
from agents.
Existing alternatives: Agents currently use existing software interfaces when interacting with web services
(Significant-Gravitas, 2024). In the absence of dedicated channels, behavioural tests could try to identify and
isolate agent behaviour. CAPTCHAs tend to be unreliable (Hossen et al., 2020; Hossen & Hei, 2021; Searles
et al., 2023). Another potential test is whether an entity interacts with an interface at faster-than-average
human speeds. If so, the entity could undergo more intensive monitoring or have more limited access to
functions, under the suspicion that it might not be human. This differential treatment would effectively
constitute an agent channel, without building specific interfaces or other dedicated internet infrastructure.
Adoption: Agents currently have difficulty interacting with human interfaces (Furuta et al., 2024; Tao
et al., 2023; Gur et al., 2024; Xie et al., 2024). If agent channels are optimized to help agents function
more efficiently and reliably (Song et al., 2024), such as by simplifying interfaces (e.g., website navigation
instructions) or imposing fewer limitations (e.g., higher rate limits, reduced latency) compared to human
interfaces, there could be much demand for them. Yet, agents could soon become capable of interacting with
with human interfaces. Encouraging the use of agent channels could therefore be time-sensitive.
Limitations: Agent channels could fail to cover enough agents or could cover entities besides agents. On the
first point, agent channels would likely be less effective if only a small number of agents use them. Monitoring
of agent channels may miss incidents, and interventions on agent channels may not catch all agent activity.
On the second point, although it seems difficult to prevent other entities from using agent channels, this
limitation may not be significant. For example, any rules applied to agent channels (e.g., slowing the spread
of a language-model worm by restricting activities) would simply also apply to those entities.
Research questions:
• How should agent channels be designed and implemented? Can their creation be automated (e.g., auto-
matic API creation)?
• What could encourage the adoption of agent channels?
• Is it possible (or desirable) to isolate agent traffic for functionalities already provided by traditional
software interfaces (e.g., email (Significant-Gravitas, 2024), weather retrieval (OpenAI, 2024))?
• What policies should govern the use of agent channels to influence or constrain agents?
4.2 Oversight Layers
Description: The potential for unreliable agent behaviour motivates review of the agent’s actions. An
oversight layerwould consist of (1) a monitoring system to detect when external intervention is required
during an agent’s operation and (2) an interface for an actor to intervene. Examples of external intervention
include the provision of additional information (e.g., about the task or what the agent is not authorized to
do) or rejection of the agent’s action. The actor in (2) could be a human user, but not necessarily. For
example, a trusted, automated system could take the place of a user (Greenblatt et al., 2024; Dalrymple
et al., 2024), especially if the oversight layer flags many actions. An oversight layer could also be useful for
any actor that engages with an agent, not just a user. For example, a manager in a company could use an
oversight layer to review actions from agents used by individual employees.
13
Potential functions:
• Rejecting unsafe actions: Agents could take consequential actions that are unbeknownst to, or unintended
by, their users. For example, a malicious actor could prompt-inject an agent to drain a user’s bank
account. Similar to credit card fraud detection, methods for detecting when actions may be unintended
could protect users.
• Improving functionality: As Hewett (2024) discusses, an oversight layer could ask a human for help
whenever an agent is incapable of completing a particular action (e.g., misinterprets the task or is stuck
in a loop), without the human having to restart the agent from scratch.
• Accountability: An oversight layer could make it easier to assess responsibility for an agent’s actions, such
as by recording the explicit approval of a user for an action that harmed another party.
• Generating useful information: Oversight layers could generate useful information about which agents
tendtotakeactionsthatoverseersrejectmoreoften. Thisinformationcouldenable, forexample, insurance
to be designed around the expected reliability of an agent.
Existing alternatives: Some technical frameworks for agents already include some kind of oversight layer
(Chase, 2022; Wu et al., 2023). See below for additional research questions to extend upon this work.
Analogues to oversight layers are common across many settings. In banking, certain activity can trigger
account freezes or requests for further review. For many digital services, logging in from an unfamiliar
device triggers a request for user approval. In cyber security, endpoint detection and response tools monitor
for and flag suspicious activity. Oversight layers for agents could build upon or integrate with such existing
technologies.
Adoption: There could be strong incentives to develop and implement oversight layers because they make
agents more usable. However, it is unclear if the market will provide them to a socially optimal degree (or
what a socially optimal degree would be). Analogously, although more granular social feed controls (e.g.,
reducing the degree of sensationalist content) would make social media more usable, major social media
companies have not provided such options. Indeed, some controls may be against the financial interests of
such companies. For example, removing sensationalist content could reduce engagement and ad revenue.
Analogously, AI companies could hesitate about providing users with the ability to limit how agents engage
with activities that could be profitable for the company, such as making financial transactions or viewing
advertisements.
Limitations: Active attention is required if oversight layers flag potentially problematic behaviour. Humans
could ignore such flags if they are too frequent or present information in a complex manner. Analogously,
internet users rarely read terms of service. Humans could also have predispositions to trust automated
systems without sufficient verification of their behaviour (Parasuraman & Riley, 1997; Skitka et al., 1999;
Goddard et al., 2012). At the same time, AI systems could eventually be better than humans at catching
problematic behaviour. For instance, language models can already help catch vulnerabilities in real-world
code (Big Sleep Team, 2024). However, using more capable AI systems for monitoring incurs inference
costs. Using less capable systems, or simply decreasing inference budgets, could reduce the effectiveness of
monitoring. Further study is needed to understand whether the default equilibrium will be desirable.
Research questions:
• Who should be able to access information generated by oversight layers?
• How can an oversight layer gracefully interrupt an agent when it requires external intervention and
integrate additional information or actions from another actor?
• How can we design interfaces that allow users (or other actors) to set the degree of oversight (e.g., how
often the user is notified of a flagged action)?
• How can we build trusted, automated systems (Greenblatt et al., 2024; Dalrymple et al., 2024) that can
intervene so as to minimize the degree of human intervention required?
14
• Given trade-offs between effectiveness and economic cost, will the market sufficiently provide for oversight
layers? If not, wh
```
