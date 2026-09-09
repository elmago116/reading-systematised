---
title: IDs for AI Systems
author: Alan Chan, Noam Kolt, Peter Wills, Usman Anwar, Christian Schroeder de Witt, Nitarshan Rajkumar, Lewis Hammond, David Krueger, Lennart Heim, Markus Anderljung
year: "2024"
Type: Preprint
DOI: 10.48550/arXiv.2406.12137
source: https://arxiv.org/abs/2406.12137
created: 2026-06-18
description: AI systems are increasingly pervasive, yet information needed to decide whether and how to engage with them may not exist or be accessible. A user may not be able to verify whether a system has certain safety certifications. An investigator may not know whom to investigate when a system causes an incident. It may not be clear whom to contact to shut down a malfunctioning system. Across a number of
tags:
  - op/acc/pending-review
  - tech/Ai/agents
  - themes/ethics/norms
pdfORepub: "[[IDs for AI Systems.pdf]]"
---
[[IDs for AI Systems.pdf]]

> **Abstract:** AI systems are increasingly pervasive, yet information needed to decide whether and how to engage with them may not exist or be accessible. A user may not be able to verify whether a system has certain safety certifications. An investigator may not know whom to investigate when a system causes an incident. It may not be clear whom to contact to shut down a malfunctioning system. Across a number of

## Full text (extracted from `IDs for AI Systems.pdf`)

*Source:* `2PDF/IDs for AI Systems.pdf`  
*Extracted:* 2026-06-18

```text
IDs for AI Systems
Alan Chan alan.chan@governance.ai
Centre for the Governance of AI
Mila (Quebec AI Institute)
Noam Kolt
University of Toronto
Peter Wills
Centre for the Governance of AI
University of Oxford
Usman Anwar
University of Cambridge
Christian Schroeder de Witt
University of Oxford
Nitarshan Rajkumar
University of Cambridge
Lewis Hammond
University of Oxford
Cooperative AI Foundation
David Krueger
University of Cambridge
Lennart Heim
Centre for the Governance of AI
Markus Anderljung
Centre for the Governance of AI
Abstract
AI systems are increasingly pervasive, yet information needed to decide whether and how to
engage with them may not exist or be accessible. A user may not be able to verify whether a
system has certain safety certifications. An investigator may not know whom to investigate
when a system causes an incident. It may not be clear whom to contact to shut down a
malfunctioning system. Across a number of domains, IDs address analogous problems by
identifying particular entities (e.g., a particular Boeing 747) and providing information about
other entities of the same class (e.g., some or all Boeing 747s). We propose a framework
in which IDs are ascribed toinstances of AI systems (e.g., a particular chat session with
Claude 3), and associated information is accessible to parties seeking to interact with that
system. We characterize IDs for AI systems, provide concrete examples where IDs could
be useful, argue that there could be significant demand for IDs from key actors, analyze
how those actors could incentivize ID adoption, explore a potential implementation of our
framework for deployers of AI systems, and highlight limitations and risks. IDs seem most
warranted in settings where AI systems could have a large impact upon the world, such as in
making financial transactions or contacting real humans. With further study, IDs could help
to manage a world where AI systems pervade society.
1
arXiv:2406.12137v3  [cs.AI]  28 Oct 2024
1 Introduction
AI systems are becoming increasingly commonplace. While current systems can struggle to complete complex
tasks (Mialon et al., 2023; Liu et al., 2023; Kinniment et al., 2023; Xie et al., 2024; Jimenez et al., 2024),
capabilities seem likely to improve (Hoffmann et al., 2022; Epoch, 2023; Erdil & Besiroglu, 2023; Ho et al.,
2024), and future AI agents could carry out a broad range of tasks with only minimal human intervention
(Chan et al., 2023; Shavit et al., 2023; Chan et al., 2024). Several commercially deployed AI systems can
already search the web, send emails, and write code (OpenAI, 2024b; Anthropic, 2024a). Even when they do
not function reliably, AI systems might still be widely used, whether because of cost advantages, hype, or the
externalization of their harms (De La Garza, 2020; BBC, 2021; Raji et al., 2022).
At the same time, information to make decisions about engaging with AI systems may not exist or be
accessible. Although there may be obligations to inform partiesthat they are interacting with an AI system
(e.g., EU AI Act Article 50.1 (Parliament, 2024)), those parties may not know withwhich AI system they are
interacting. For example, a party that knowingly interacts with an AI system may not be aware that their
system is relatively more vulnerable to adversarial attacks (Zhan et al., 2024). Awareness of such elevated
risk could justify additional precautions, such as reviewing the system’s actions or abstaining from interaction
altogether. Furthermore, the same party—or an investigator—may lack the information to pursue recourse if
the system causes harm. Information about the system or the interaction (e.g., whether a system behaved
according to safety standards, or the identity of the deployer) could aid incident investigation, allocation of
liability, or other legal action (Buiten et al., 2023; Buiten, 2024; Kolt, 2024; Wills, 2024).
Across numerous domains, IDs held by software, assets, individuals, and organizations address analogous
problems. IDs can help to ascertain compliance with standards or regulation. For instance, an individual
aircraft’s tail number is associated to the aircraft’s incident and maintenance history, which could inform
safety assessments from regulators or aircraft operators. Furthermore, IDs can help to establish whether trust
is warranted. A website’s valid HTTPS certificate assures users of the website domain’s authenticity, and
provides a way for users to establish a secure communication channel.1 Finally, IDs can facilitate redress.
Serial numbers on consumer products enable customer support, product recalls, and attribution of liability.
A key feature that enables all of the above functions is that IDs are specific toparticular entities (e.g., a
particular Boeing 747), although they may also contain information about other entities of the same class
(e.g., some or all Boeing 747s).
Identifying particular AI systems, which we terminstances, could be similarly useful. Given their increasing
prevalence, we focus here on digital-assistant-like systems that that respond to user direction, usually (but
not necessarily) through natural language (Gabriel et al., 2024). In this context, an instance corresponds
to a user and a history of interaction.2 For example, a particular user’s chat session with ChatGPT (with
e.g. a GPT-4 backend) is an instance. Separate instances can behave differently, whether because of user
instructions (Shanahan et al., 2023; Wei et al., 2023; Bai et al., 2022; Zou et al., 2023; Agarwal et al., 2024),
hijacking by an attacker (Greshake et al., 2023; Zhan et al., 2024), or malfunction. As such, instance-specific
information could aid decisions about interactions. For example, the ability to distinguish instances from one
another could aid incident investigation (e.g., a client files a complaint about an instance) and allocation of
liability (e.g., if a third party hijacked the instance).
Yet, current mechanisms are not granular enough to identify instances. System documentation (Gebru
et al., 2021; Mitchell et al., 2019; Gilbert et al., 2023; Bommasani et al., 2023) provides information about
systems, but such documentation is not an ID for instances or systems (however, an ID could include such
documentation). API tokens for services, such as for hotel booking (OpenAI, 2023a), do identify entities
that use the tokens, but are usually only user- or device-specific, and do not allow identification of an entity
across different services. Even if API requests do include a string with the AI system’s name, any attacker
could mimic it. Finally, user accounts only separate the activities of AI systems from different users. We
summarize these differences and discuss further identity systems in table 1.
1Despite a lack of centralized enforcement, HTTPS gradually became the norm due to widespread awareness of its security
benefits and collective advocacy from web browsers, search engines, and other organizations (Encrypt, 2024; Hancock, 2021).
2This definition of instance does not take memory into account. While it will suffice for this work, see Appendix A for a more
general definition.
2
Existing Systems Differences with AI IDs
Proof of personhood (Borge
et al., 2017)
A proof of personhood identifies a unique human in an anonymous
way, but does not identify AI systems.
ORCID An ORCID is meant to point to a particular researcher, but there
is no reliable way to verify an entity’s claim that a particular
ORCID corresponds to it.
DOI A DOI is meant to provide a unique, persistent identifier of a
digital object, but there is no reliable way to verify an entity’s
claim that a particular DOI corresponds to it.
Watermarks Watermarks are meant to indicate AI provenance in content and
do not contain information about particular AI systems.
C2PA (C2PA, 2023) C2PA is a standard for making verifiable claims about the prove-
nance of content. Such claims can point to an ID, but are not IDs
in themselves.
CAPTCHAs CAPTCHAs are meant to detect presence of non-humans, rather
than identify them.
API tokens API tokens are user- or device-specific and do not identify entities
across different APIs.
User accounts User accounts only separate the activities of AI systems from
different users.
System documentation,
such as a system card
System documentation provides information about systems, but
is not an ID for instances or systems.
Table 1: We collate a number of existing identity-like systems, some of which do not apply to AI systems,
and describe their differences with AI IDs.
To prepare for a world with ubiquitous AI interactions, we propose (instance-level) IDs for AI systems. An
AI ID is a container for1) an identifier and2) attributes. An identifier is a unique string that refers to
an instance.3 An identifier could be randomly generated, or could itself encode some information about
the instance (e.g., the identifier could include the exact time at which the instance started operating). An
attribute is any information that could pertain to the instance, and could include behaviour, properties,
context, or relationships to other instances or systems. An identifier enables the association of attributes to
an instance, similar to how serial numbers associate information to a particular product. Attributes could be
specific to an instance (e.g., prior incidents associated with the instance), or could apply more broadly to
other instances (e.g., a system4 card). An ID could directly include attributes (e.g., the name of the deployer)
or could link to them (e.g., a link to a database of prior incidents).
Different instances or systems could warrant attributes of differing levels of granularity or detail. For example,
attaching a user identifier to an ID may only be appropriate in high-stakes settings, such as when a company
uses an AI system to interface with critical infrastructure. Prior incidents associated with an instance would
likely be more useful for future AI agents (Chan et al., 2023; Shavit et al., 2023; Chan et al., 2024; Gabriel
et al., 2024), which could act autonomously and persist over long durations.
IDs would contain informationabout AI systems and are thus are different from measures that attempt
to verifywhether AI systems—or their artifacts—are present. Watermarks (Liu et al., 2024; Wang et al.,
2021) embed origin information in AI outputs, while content provenance measures (C2PA, 2023) embed such
information in metadata. Both types of techniques could embed IDs. Other measures, like CAPTCHAs (Shet,
2014), verify that a human is performing an action, so as to reduce service abuse. If AI systems become
essential for many tasks, such as web search and account registration, it may be useful to allow them to
3It may be desirable in the future to have identifiers that refer to even more granular parts of an AI system. For example,
one could have an identifier refer to an instance as it operated between timest and t + 10.
4A system (e.g., ChatGPT) could use different models (e.g., GPT-4, GPT-3.5) as a backend. We consider system cards to
include model cards (Mitchell et al., 2019).
3
AI outputs
Parties
End interaction
Take precautions 
ID 
Unique identiﬁer
Link to incident databaseSystem card Investigate
Certiﬁcations Take corrective action
Figure 1: IDs contain a unique identifier along with attributes (e.g., a system card, certifications, or a link to
previous incidents). We also display some potential actions that parties might take based on information in
an ID.
bypass CAPTCHAs in exchange for presenting an ID.5 Parties could use this ID to track and disincentivize
abuse.
1.1 Contributions
We propose IDs for AI systems. First, we characterize the central properties of IDs. Second, we provide
concrete examples where IDs could be useful. Third, we argue that there will likely be demand for IDs
from several key actors, especially in high-stakes settings. We also explore potential ways for these actors to
incentivize ID use. Fourth, we analyze a potential implementation of IDs. Finally, we investigate some of
the limitations of IDs and of our analysis, including privacy and security risks of IDs, as well as uncertainty
about the broader societal consequences of IDs for AI systems.
We recommend limited experimentation with IDs. IDs seem most warranted in settings where AI systems
could have a large impact upon the world, such as in making financial transactions or contacting real humans.
For example, actors that provide interfaces for AI systems to carry out financial transactions could impose
rate limiting whenever IDs are not present. However, instances without IDs should still be allowed to access
services. Deployers of AI systems could experiment ID implementation.
2 Definitions
We collate additional definitions that will be useful for the rest of this work.
An instance of an AI system is an abstraction that corresponds to a context window and an (initial) user.
Different instances are causally independent from each other, unless they interact or affect a shared entity
(e.g., the same user’s bank account) in the world. Except where we point out additional nuances, readers can
consider an instance to be roughly the same as a chat session with a chatbot. An ID for an instance would
thus identify that session to other parties interacting with the chatbot, actors investigating an incident that
the chatbot caused, etc. We provide here some examples of instances in the context of chat sessions, and
defer a more general definition and discussion of its limitations to Appendix A:
• A user’s continuous chat session, without regenerating responses, is an instance.
• In the context of a chat session, regenerating a response creates a new instance.
A party is any entity that interacts with, or is deciding whether to interact with, an AI system. Categories
of parties include humans, organizations, or computer programs.
5Advances in AI capabilities may render CAPTCHAs ineffective. We discuss this possibility further in Section 5.
4
A deployer is an organization that runs AI systems for users. As of April 2024, examples of deployers
include Microsoft, OpenAI, Anthropic, and Cohere. Developers can be, but are not necessarily, deployers. For
example, OpenAI, Anthropic, Google, and Cohere develop and deploy their own systems. Although chains of
deployers can exist (e.g., deployerA runs a system for deployerB, who modifies that system and serves it
to userC), we leave deeper consideration of this nuance for future work. When we refer to acentralized
deployment setting, we mean a setting where deployers run AI systems. When we refer to adecentralized
deployment setting, we mean a setting where users run AI systems for themselves, whether on their own or
rented (e.g., cloud compute) hardware.
A service is software that allows an entity to perform tasks. For example, software which an individual uses
to perform online banking is a service. An(AI) plugin(OpenAI, 2023a; Richards, 2023) is software that
allows AI systems to interact with services. For instance, plugins allow GPT-4 to interact with web search,
Wikipedia, and Twitter (Significant-Gravitas, 2024). Aplugin developeris not necessarily the same as a
service provider—the actor that develops and maintains the service—since the former can take advantage
of existing interfaces for services. Third parties (plugin developer) use Microsoft’s (service provider) existing
software interface for Bing to allow GPT-4 to perform web searches (Richards, 2023).
3 Characterizing IDs
An ID is a container (Korenhof et al., 2014) for1) an identifier (that corresponds to an instance) and2)
attributes. We characterize a design space for IDs: the attributes it includes, to whom it is accessible, and to
what extent it is verifiable. Our goal in this section is to investigate possible designs and why they may be
desirable, rather than to prescribe specific choices.
3.1 Attributes
In addition to the identifier, an ID can contain (or link to) attributes: any information that could be useful
to a party interacting with the corresponding instance. An attribute can vary along two dimensions.
Category: Categories of attributes include (but are not limited to) behaviour, properties, context, and
relationships to other instances or systems. Some examples are:
• Behaviour: prior incidents (Wei & Heim, 2024)
• Properties: information in a system card (Mitchell et al., 2019; Gebru et al., 2021); the results of
evaluations (Shevlane et al., 2023; Weidinger et al., 2023)
• Context: the system prompt; external memory (Wang et al., 2023)
• Relationships to other instances or systems: any other AI systems the instance has created or is
running; any instances that have created the instance in question
Behaviour and properties could straightforwardly inform AI interaction decisions. Context could inform
parties about potential behaviour (e.g., there is a jailbreak in the system prompt or external memory (Cohen
et al., 2024)). Lastly, relationship information could aid incident investigation and response. Suppose a
user instructs an instance to carry out a personalized influence campaign. The instance could create many
descendant instances, each of which could target an individual person. If the ID of a descendant instance is
linked to the ID of the original,ancestor instance, it could be easier to investigate and resolve such misuse.
In Section 6, we discuss when this ID linking is possible.
Specificity: An attribute could provide information about multiple instances (even of different systems),
rather than just the instance corresponding to the ID. With incidents as a (sub)category, potential levels of
specificity could include:
• Instance: incidents associated with a particular instance
5
• Instances satisfying certain properties: incidents associated with instances whose system prompts
contain harmful instructions
• User: incidents associated with a particular user
• A particular (type of) party: incidents involving a particular (type of) party and a system (e.g., all
incidents involving hospitals and the 9-April-2024 version of GPT-4)
• System: incidents associated with a system (e.g., the 9-April-2024 version of GPT-4)
• Systems: incidents associated with multiple versions of a system (e.g., all versions of GPT-4)
An ID could contain (or link to) the same category of attribute at varying levels of specificity. Analogously, a
tail number on an individual aircraft could be associated with maintenance records for systems, sub-systems,
sub-sub-systems, etc of that aircraft.
3.2 Access
An ID is simply an abstraction that contains or links to information. That abstraction can be presented in
several potential ways, such as on a separate web page or in a pop-up window. We explore design decisions
around who can access an ID and how it is presented to them.
Parties that can access the ID: We distinguish between primary parties and secondary parties. Primary
parties receive an ID when interacting with the corresponding instance. Secondary parties receive the ID
through other means, such as directly from a primary party, or from records. Some examples include:
• Primary: service providers; the user of the instance; other instances that interact with the instance
in question6
• Secondary: auditors; regulators
Presenting an ID to primary parties corresponds to linking IDs to the corresponding instance’s outputs.
Content provenance standards (C2PA, 2023) can help to ensure that such linking is verifiable (see Section 3.3).
Some primary parties and how IDs may be attached include:
• Service providers: ID is included in a JSON payload
• Users: ID is accessible through a mouseover icon in a chat interface
• Other instances that interact with the instance in question: ID is sent in any communications with
other instances
From the perspective of an actor implementing IDs (e.g., deployers), ID disclosure to secondary parties could
be unintentional. For example, a data breach could render an ID accessible to the general public. As another
example, a legal investigation could render IDs accessible to a government.
Selective disclosure: Some attributes may only be appropriate for certain parties. Other attributes may
contain both important and sensitive information. Examples:
• If user identification (e.g., from a know-your-customer process (Egan & Heim, 2023)) is included
in an ID, it may only be appropriate for government authorities to access this identification for e.g.
regulatory purposes
• A system prompt could contain both sensitive user information and information relevant for interacting
parties (e.g., does the system prompt contain a jailbreak?)
6Similar to how a TLS handshake allows mutual verification before establishing a communication channel, AI systems could
potentially use IDs to establish trust before interacting with each other.
6
Actors implementing IDs could selectively hide information from different primary parties. Those same actors
could also process attributes in a privacy-preserving way (Trask et al., 2023; Sporny et al., 2024) so as to reveal
only information that is relevant to the party interacting with an instance. Even so, preventing transmission
of information to other parties may be difficult. For example, once an actor obtains user identification, it
could—intentionally or not—transfer that information to other actors.
Persistence: IDs could be accessible for varying amounts of time after an instance has ceased to operate.
Practical considerations, such as storage capacity, could impose limitations. The appropriate duration could
also depend upon the application domain. Analogously, financial institutions have obligations to maintain
records for set periods of time (noa, 2022).
3.3 Verifiability
Suppose an author creates an ID (or a link to an ID) for an instance. A party interacts, or seeks to interact,
with the instance. The party receives an ID. For the party to trust that the ID provides accurate information
about the instance, the following are necessary (but not sufficient; see further discussion below).
(1) The party’s received ID is the same as the author’s created ID
(2) The claimed author of the received ID is indeed the author of the received ID
(3) The received ID corresponds to the instance in question
(4) The party trusts the author
The first three criteria lead to the following threat models:
• Tampering: An attacker modifies the ID while it is in transit from the author to the party interacting
with the instance.
• ID spoofing: An attacker creates another ID, sends it to the party, and claims it originated from
the author.
• Instance spoofing: An attacker uses the author’s ID for their own instances.
We consider IDs (i.e., an ID system) to beverifiable if they defend against these threats. We provide an
illustration of these threat models in Section 3.3.
Existing technology could be drawn upon to provide verifiability. For digital-assistant-like AI systems (e.g.,
GPT-4), any digital communications usually would take place over TLS/SSL (Rescorla, 2018), which would
address tampering. We leave tampering of other AI systems’ IDs (e.g., IDs for self-driving cars) to future work.
To combat ID spoofing, authors could digitally sign the ID (potentially with public key ownership verified by
a trusted third party). For instance spoofing, there are existing standards for binding a digital object, such as
an ID, to a piece of content, such as an AI system’s output. For example, C2PA involves binding provenance
claims to content (C2PA, 2023), and calls the binded object amanifest. Such binding could ensure that IDs
are associated to particular outputs from an instance in a verifiable way.7 We emphasize that our examples
here are meant to be illustrative, not prescriptive.Security vulnerabilities in existing technologies may weaken
verifiability and require new solutions.
Given space limitations and the complexity of the involved social questions, we do not focus on step (4) in
this work. Similarly, we also scope out issues relating to the accuracy of the attributes in an ID. Accuracy
is not the same as verifiability, since even if (1)-(4) are satisfied, the author could have made mistakes in
creating and linking to the information.
7If desired, the verifiability of IDs over extended interactions could be ensured by linking manifests to each other crypto-
graphically, such as in a blockchain.
7
ID Parties
Attacker
tampering
AttackerFake ID
ID spooﬁng
Attacker's AI
Author
identiﬁes
itself to
instance
spooﬁng
TLS/SSL
Digital signatures
Binding ID to AI output 
Author's AI
identiﬁes 
itself to
Figure 2: We illustrate howexisting technologiescan help ensure the verifiability of IDs against thethreat
models in Section 3.3. We emphasize that our examples of existing technologies are meant to be illustrative,
not prescriptive.
4 How Could IDs Help?
We provide some hypothetical case studies where IDs could be useful and compare IDs to alternatives. AI
agents—systems which act autonomously to achieve goals with little to no user direction, instruction, or
supervision (Chan et al., 2023; Shavit et al., 2023; Gabriel et al., 2024)—feature prominently in our scenarios.
4.1 Shutting Down Malfunctioning Agents
Scenario: Suppose a user runs an AI agent to provide continual recommendations across many platforms
and services (e.g., for media, shopping etc).8 To generate such recommendations, the agent interacts with
plugins for various web services, such as search engines, online discussion fora, etc. The agent provides its ID
to each service. Unbeknownst to the user, the agent begins to malfunction (e.g., by chance, prompt injection)
and disrupt services (e.g., spamming discussion fora, sending malformed requests to services or overloading
them, conducting prompt injection attacks on other AI agents). Services interacting with the agent flag its
malfunction. Service providers use information in the ID to notify the deployer, and block further interaction
with the agent. The deployer receives multiple reports of malfunction for the same ID and investigates the
agent, potentially shutting it down and notifying the user.
Alternatives to IDs: To block further interaction with the agent, a service provider can simply revoke its
API token and potentially block the requesting IP address. These actions would not prevent the agent from
accessing new services, however. As well, API tokens would not identify an agent across different services to
enable shutdown if necessary. Alternatively, services could notify the user of agent malfunction. With a good
user interface, users could notice such malfunction and shut down their agent. If users are careless or rarely
supervise their agent (perhaps they have many such agents running in the background), it seems useful to
have IDs as a backup option.
Limitations of the scenario: It is unclear how impactful the disruption of services would be. Deployers
could also be unresponsive to notifications from service providers.
8The idea for this scenario is from Zittrain (2024).
8
4.2 Verifying Certification
Scenario: A user wishes to interact with an agent from another person. The user wants to make sure that
the agent does not act in an undesirable way. For example, the user would want to make sure that a malicious
third party did not prompt inject (Greshake et al., 2023) the agent (perhaps because the user is passing
sensitive information or is accessing resources the agent will send over). A trusted third party, such as a
deployer or an auditor, checks the interaction history of the agent at runtime for prompt injections (e.g.,
with a tool like Beurer-Kellner et al. (2024)). After verifying the absence of prompt injections, the trusted
third party adds a certification onto the agent’s ID. The user sees the certification on the ID and continues
interaction.
Alternatives to IDs: The trusted third party could send the certification directly to a user requesting it,
but some sort of identifier would still be needed to ensure that the certification corresponds to the agent with
which the user is interacting.
Limitations of the scenario: Certification would raise privacy concerns because the trusted third party
would be able to see the whole interaction history. Privacy-preserving ways to perform such audits would
be valuable to explore (Trask et al., 2023; 2024). A potential alternative would be for the auditor to run
behavioural tests on the agent at runtime, and link the results of the tests to the ID.
4.3 Investigating Scam Calls
Scenario: Suppose a user spins up an AI agent to carry out scam phone calls. The agent creates multiple
sub-agents—potentially using different AI deployers—and directs each one to carry out scam calls through a
telephone service. The service receives each sub-agent’s ID, each of which contains information about the
deployer and a connection to the original agent’s ancestor ID. The service provider connects the sub-agent to a
telephone network and creates a call detail record (CDR), linking the call with the sub-agent’s ID. Some scam
victims notify the operator of the telephone service. The telephone provider notifies law enforcement, who
investigates the relevant CDRs and IDs. Law enforcement notifies the deployers of the sub-agents, potentially
after obtaining a warrant so as to obtain access to the deployers’ logs. Through ID linkages between parent
and child agents, law enforcement and deployers discover the agent and user behind the spam calls.
Alternatives to IDs: The main alternative would be for law enforcement to ask ISPs to perform IP address
tracking, if the telephone provider records the IP addresses of the sub-agents. Interacting with ISPs (and
potentially obtaining a warrant) could take additional time and effort. Conservatively, in this case IDs could
help to save time during incident investigation, but not necessarily enable something that was otherwise
impossible.
Limitations of the scenario: The main limitation of this scenario is the provision of IDs from the sub-agents
to the service provider. Users could use deployers that do not implement IDs, or could run their own agents
to avoid passing IDs to APIs. A potential response is for the telephone service provider to require IDs before
provisioning telephone access.
5 Demand for ID Use
IDs seem useful for actors engaging with an AI system, but why would a user or deployer of that AI system
present an ID? In short, governments, service providers, and parties interacting with AI systems all have
interests in ID use, as well as means to incentivize (or mandate) it.
5.1 Governments
Interests in ID use: Governments may wish to disincentivize and investigate harms caused through AI
systems. In the case of a financial scam for instance, the IDs of AI systems involved in any transactions could
aid investigation (see Section 4.3). Similarly, governments have an interest in preventing fraud, and therefore
already mandate that certain financial transactions involve ID checks.
9
Mandating ID use: Governments could mandate that certain, highly consequential service providers obtain
IDs from any AI systems with which they interact. For example, financial institutions could request IDs if AI
systems make large financial transactions.
5.2 Service Providers
Interests in ID use: IDs could aid incident investigation processes (see Section 4.3) and ensure that only
trusted agents interact with services (see Sections 4.1 and 4.2), thereby disincentivizing or reducing service
abuse.
Incentivizing ID use: Service providers could develop, or encourage the development of, plugins that require
IDs. AI systems can already perform a variety of useful tasks through plugins, including web searches, email
communication, and stock trading (OpenAI, 2023a; Richards, 2023; Wu et al., 2023; Anthropic, 2024b). In
comparison to direct interaction with a user’s computer (e.g., interacting with individual web page elements),
plugins could be more reliable and performant. AI systems continue to have difficulty with the former (Furuta
et al., 2024; Tao et al., 2023; Gur et al., 2024; 2023; Xie et al., 2024), but plugins already enable useful tasks.
As well, plugins could constrain the AI system’s actions in a more targeted way, so as to improve safety.
Yet, any actor could write a plugin that does not require IDs. A potential response could be for providers to
restrict the services themselves, rather than just the plugins, in the absence of an ID. Restrictions, such as
rate limits, could still allow humans to interact with services while reducing the damage an AI system could
do.
For AI systems that interact with their users’ computers directly, CAPTCHAs-like methods could help to
incentivize ID use. Entities that failed CAPTCHAs could be subject to ID requirements, or else face service
restrictions. Although software systems have become increasingly capable of bypassing CAPTCHAs,9 they
could be an interim option in anticipation of more robust proof-of-personhood protocols (Borge et al., 2017).
5.3 Other Parties that Interact with AI Systems
Interests in ID use: Some parties, such as individuals or businesses, may only wish to interact with certain,
trusted AI systems (see Section 4.2). Future software—including users’ personal AI assistants (Gabriel et al.,
2024)—could inspect IDs and reject potentially unsafe interactions (e.g., with jailbroken systems), similar to
how browsers warn users before visiting websites without valid HTTPS certificates.
Incentivizing ID use: Large corporations could exert strong pressure for ID usage, through reducing or
avoiding engagement with AI systems without IDs. Future software that inspects IDs could also exert similar
pressure. Analogously, websites without HTTPS are disadvantaged since popular web browsers warn users
about insecure connections.
5.4 Where to Require IDs
While IDs could be useful, universal ID requirements might not be warranted. As we will discuss in Section 7,
ID implementation imposes burdens and risks, and there remains uncertainty about the broader impacts of
ID usage. As such, if governments or service providers decide to incentivize or require ID use, they should
target settings where IDs could be most useful, such as when AI systems use services that have a direct
impact on the world. We provide some examples of such services.
Making large financial transactions: Some service providers could allow AI systems to perform financial
transactions, such as making purchases, trading stocks (Khan et al., 2024), or otherwise transferring funds.
Such service providers could require IDs for transactions involving significant sums. IDs could help to reduce
the risk of a variety of negative outcomes, by enabling service providers to filter out potentially untrustworthy
AI systems (e.g., those that may likely malfunction and make mistaken transactions) and investigate potential
incidents.
9Task-based CAPTCHAs are no longer as common as CAPTCHAs based on behavior patterns, such as how a mouse is moved
across the screen (Shet, 2014). Yet, AI systems may one day be able to imitate human behaviour patterns as well (Adept, 2022).
10
GovernmentsIndividuals, businesses
Service
Plugin
AI system
direct 
computer 
interaction
CAPTCHAs, proof of personhood
Gating access
Restrictions
Service providers
mandate
Refuse
interacts with
Figure 3: Various actorshave potential (dotted lines)methods to incentivize the use of IDs, whether
directly or through using other actors.
Contacting humans: Potential services for contacting humans include crowdwork platforms, telephone
services, and online messaging. The ability to contact humans and potentially convince them to take actions
in the world could greatly magnify the impact of an AI system. As we discussed in Section 4.3, IDs could
help to disincentivize and catch misuse of these services.
6 Potential ID Implementation
We assess a basic ID system that deployers of AI systems could implement. Our discussion in this section
will be agnostic to the applications where IDs are used (see Section 5.4 for discussion of where ID use may be
warranted). We also omit discussion of verifiability, given our presentation in Section 3.3 and Figure 2 of how
existing technologies could enable verifiability.
We assume a straightforward choice for the identifier,system_identifier:instance_identifier , where
system_identifier is the same for all instances of a system10 and instance_identifier is unique to a
particular instance. It could be useful and straightforward to append other details to the identifier, such as
the exact time at which the instance was created. However, we proceed with this choice for simplicity.
6.1 Assigning IDs
Although IDs are instance-specific, it may not be feasible for deployers to detect the formation of all new
instances. For example, a user could use deployer-run instancesA and B as backends for a user-run systemC,
which integrates the outputs ofA and B and would evade detection by deployers. We outline some scenarios
where deployers could detect new instances and analyze considerations for assigning new IDs.
New instances: Deployers can easily generate new identifiers whenever users create new instances (e.g., a
“new chat” button).
10If the underlying model changes, the system ID should also change. E.g., ChatGPT with a GPT-4 backend is different from
ChatGPT with a GPT-3.5 backend.
11
Reloaded instances: Suppose that a deployer saves instances’ states (i.e., the history of interaction) and
provides separate functionality for users to reload them. We tentatively suggest that deployers retain the ID
of the original instance for the reloaded instance, since some attributes (e.g., prior incidents, context) of the
original instance could be relevant for understanding the behaviour of the reloaded instance. Alternatively, if
a deployer does decide to assign a new identifier to the reloaded instance, a link to the ID of the original
instance would maintain access to the relevant attributes.
Output regeneration: Some deployers provide the ability for a user to regenerate an output in response to
previous input. Although not yet implemented, deployers could additionally allow users to create multiple
branches (see Appendix A for further discussion of branches) of interactions, based off of regenerated outputs.
More concretely, a user could interact with their instance up until the outputat at timet, regenerate to
obtain an outputbt, and continue interactions with the respective branches to obtain outputs(at+1, bt+1),
(at+2, bt+2), etc. Since the two branches have no necessary causal impact on each other (unless they interact
with each other or modify a shared object in the world), they should have two separate IDs, with links to the
ancestor ID.
Composite systems: Software frameworks could give users the ability to create new instances (acomposite)
out of a collection of existing instances (Wu et al., 2023). If deployers run such software frameworks for users,
they could detect the formation of composites. Since the constituent instances can continue running alongside
the composite, composites should have new IDs, but could have their IDs linked to their constituents’.
Fine-tuned systems: Some deployers provide fine-tuning functionality to users. Since fine-tuning can
change the behaviour of a system, a fine-tuned systemA′ should have differentsystem_identifier than
the original systemA, and link toA’s system_identifier . Although it may be useful to include some
documentation about the fine-tuning data in an ID, user privacy expectations could complicate such inclusion.
Some deployers monitor fine-tuning data only for abuse detection and legal compliance (ChrisHMSFT et al.,
2023; OpenAI, 2024a); inclusion of fine-tuning data in an ID likely requires stronger justification.
6.2 Attributes
We tentatively suggest the following attributes for a deployer to include (or link to) in an ID:
• A system card
• A database of incidents associated with the system
• The IDs of ancestor and descendant instances
If instances of future systems persist longer in the world, it may be appropriate to link to a (sub)database
of incidents associated with the instance. Implementing links to ancestor and descendant instances, when
feasible in the situations discussed in Section 6.1, could be a simple way to test the utility of instance-level
identification.
There are likely ways for users to avoid ancestor or descendant links. For example, a user could manually
copy the inputs of a previous instance to a new instance, avoiding a deployer-provided reloading function.
More reliable identification of ancestors and descendants could involve more invasive measures, which may
only be appropriate in high-stakes domains. For example, a deployer could attempt to analyze the inputs of
different instances from the same user for similarities.
6.3 Access
Users: The ID could be accessible through a user interface and sent along with any API requests from a
user. If a deployer serves an API to a customer, who subsequently serves an API based on the deployer’s
system to another user, the deployer would likely have to work with the customer to ensure that the end user
receives an ID (see Appendix B for further discussion).
12
To help to ensure that secondary parties maintain access to the ID, the deployer could include IDs in
watermarks and metadata of media outputs (i.e., text, images, video). Yet, it is unclear how robust such
methods may be to user removal (Zhang et al., 2023; OpenAI, 2024c).
Services: When the AI queries a service, the ID should be sent along with the request. Since requests are
text-based (e.g., JSON), including the identifier and (links to) the attributes would be straightforward.
7 Limitations
We discuss limitations of IDs and of our analysis.
7.1 Misuse of IDs
If IDs were prevalent but verifiability was not assured, misuse of IDs could be a significant problem. For
example, an attacker’s agent could masquerade as somebody else’s agent to perform illicit actions, such as
sending spam or carrying out cyberattacks. Overdependence on such IDs could lead to false accusations
against innocent users, who may not have the resources or expertise to defend themselves and point out flaws
in the ID system. Ideally, the compromise of an ID should be made clear to all that can access it. IDs should
also likely not be the sole or conclusive source of evidence for incident investigations. Concerns about the
failure of ID verifiability mirror similar concerns about the reliability of watermarks (Gleichauf & Geer, 2024).
7.2 Decentralized Operation of Agents
We have not discussed how IDs could be implemented for AI systems which users run themselves, without
a deployer. If service providers decide to require IDs, users will need straightforward ID implementation
methods. Otherwise, they could be locked out of services or be forced to use a deployer. A potential
inspiration is Let’s Encrypt (Encrypt, 2024), which automated the process of HTTPS certificate creation for
websites. A similar service could work with software for running AI systems (e.g., transformers (Wolf et al.,
2020), AutoGen (Wu et al., 2023)) to allow users to request and attach IDs. We leave practical details for
future work.
7.3 Failure to Inform
Parties could ignore IDs, just as internet users sometimes ignore indicators of untrustworthiness (Norris &
Brookes, 2021). Software—or future AI assistants (Gabriel et al., 2024)—could make informed decisions for
users in some circumstances, just as browsers reject websites with invalid HTTPS certificates. However, it
remains unclear what information would justify rejecting an interaction with an AI system. Other parties
could misunderstand or misinterpret an ID’s attributes. For example, it can difficult to assess the external
validity of evaluation results (Fourrier et al., 2023; Weidinger et al., 2023).
ID attributes could also be inaccurate. For example, deployers could unintentionally link to an incorrect
version of system documentation, or simply fail to update it. OpenAI has occasionally released new versions
of GPT-4,11 but has not updated the GPT-4 system card (OpenAI, 2023b) since the initial release, as of
April 2024. As a potential mitigation, regular audits (Raji et al., 2020; Sharkey et al., 2023) could verify the
accuracy of attributes.
7.4 Bypassing IDs
As with other types of real-world identity systems, IDs for AI systems cannot wholly prevent undesirable
behavior. IDs could be lent, or the benefits obtained from ID use—such as purchase of a good—could be
transferred. Users may hesitate to lend IDs since the borrower could inflict lasting reputational damage on
the ID. Yet, similar to the purchase of alcohol for minors, it seems difficult to track or prevent transfer of
goods. Future work could assess how likely and how damaging such transfer could be.
11See https://platform.openai.com/docs/models/gpt-4-turbo-and-gpt-4 .
13
7.5 Privacy Risks
Although an identifier by itself would not reveal anything about its user, the user’s privacy could still be
compromised in a number of ways. First, information about the instance could reveal user details. For
example, timestamps and details of an instance’s activities—as might be contained in incident reports—could
help a third-party to identify users. The existence of IDs may engender pressure to attach additional
information, which could facilitate further user identification. For example, service abuse could potentially
be correlated with certain activity patterns, which could motivate corresponding data collection. Second, if
the deployer maintains an internal database linking a system’s ID to the corresponding user account, other
parties could obtain and misuse the information. Security vulnerabilities could allow attackers to obtain the
database. Overreaching governments could force deployers to reveal the users of particular systems.
7.6 Broader Societal Consequences
IDs with additional user information could enable potentially harmful ranking of users. Actors implementing
IDs may wish to include such information if it is correlated with undesirable outcomes, such as fraud. Yet,
the existence of confounders could lead to instances of some users being unfairly denied access to services,
similar to how toxicity classifiers can biased against African American English (Sap et al., 2019). Even if the
relationship between information and undesirable outcome was causal, taking such information into account
could still be unjustly discriminatory.
IDs could also enable influence over particular instances and their users. Even if an ID does not contain
information about an instance’s interactions, external actors could record particular IDs have been involved
in interactions, just as cookies can track user activity across websites. Instances that are active for long
periods of time could reveal much information about a user’s preferences. Actors interacting with instances
could try to influence their behaviour through means such as prompting. Advertisers and businesses could try
to get instances to purchase or recommend their products or services for their corresponding users. Political
actors could try to get instances to influence the voting behaviour of their users. Governments could attempt
to enforce rules upon particular instances. Such influence could be strong, especially if personal AI assistants
become much more widespread and central to daily interactions (Gabriel et al., 2024). The specific impacts
of this influence deserve further study.
Finally, IDs could create a separate digital channel for interactions between trusted AI systems. The vast
majority of digital interactions could in the future be between AI systems, especially if future AI assistants
handle most of a user’s activities (Gabriel et al., 2024). If IDs enable reliable interactions, users may prefer
their AI systems to interact only with AI systems that present IDs. Much digital activity could take place
between networks of ID-bearing AI instances that trust (and can verify) each other. Entities that trust each
other may be able to engage in more productive interactions. As a corollary, instances without IDs may
become severely disadvantaged, relative to instances within ID-bearing networks. To avoid such disadvantage,
users may have no choice but to submit to the potential negative consequences of IDs we have discussed
heretofore in this section. On balance, the consequences of a separate digital channel for AI systems remain
unclear.
8 Related Work
A growing line of work is concerned with building digital infrastructure to structure how AI systems, especially
agents (Chan et al., 2023; Shavit et al., 2023; Gabriel et al., 2024), behave and interact. Patil et al. (2024)
build a runtime for LLM agents to enable human validation and reversal of actions. Marro (2024) sketches
a protocol for communication between LLMs; the protocol relies on documents to specify structured rules,
with natural language as a fallback. (Sun et al., 2023) argue that decentralized commitment devices will be
necessary to allow agents to coordinate with each other. Our work builds upon the preliminary discussion of
IDs in Chan et al. (2024); Shavit et al. (2023).
Our treatment of verifiability takes inspiration from several Internet and security protocols. HTTPS (Fielding
et al., 2022) uses digital certificates (Cooper et al., 2008) to allow users to verify the identity of an accessed
14
website. If the certificate is valid, a user’s browser uses the information contained in the certificate to establish
a secure connection (Rescorla, 2018). Websites must obtain such certificates from CAs (Cooper et al., 2008),
who verify the identity of the website owner and issue the certificate upon successful identification. Identity
verification depends upon public key cryptography (Barnes et al., 2019), which allows a party to prove
ownership of a given, public identifier, o
```
