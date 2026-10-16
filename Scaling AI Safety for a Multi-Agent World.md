---
title: Scaling AI Safety for a Multi-Agent World
source: https://schmidtsciences.smapply.io/prog/scaling_ai_safety_for_a_multi_agent_world/
author:
published:
created: 2026-06-18
description:
tags:
  - op/doc/projects
  - tech/Ai/agents
  - themes/ethics/norms
  - op/doc/journal/article_call
---
### Schmidt Sciences

A joint funding call by [Schmidt Sciences](https://www.schmidtsciences.org/), [Google DeepMind](https://deepmind.google/), [Advanced Research & Invention Agency (ARIA)](https://aria.org.uk/), the [Cooperative AI Foundation](https://www.cooperativeai.com/foundation), and [Google.org](http://google.org/)

| Proposal Due Date |  |
| --- | --- |
| Notification of Decision | **Autumn 2026** |
| Funding Tiers | **Tier 1: Up to US $300,000 (1-2 years)**  **Tier 2: US $300,000-$1,000,000 (1-2 years)** |
| Informational Webinars | **Tuesday, June 30 12 pm ET. Register [here](https://schmidtentities.zoom.us/webinar/register/WN_81mgT461QAm3agXR0nV_NA)**  **Thursday, July 23 10 am ET. Register [here](https://schmidtentities.zoom.us/webinar/register/WN_ZhzeK6fASZKIKC_hy4u8Ug)** |
| Contact email | **multiagentsafety@schmidtsciences.org** |
| Link to FAQ | [**FAQ**](https://docs.google.com/document/d/1LLRZvrKZD9rtKAWjWXPBVZpA5PTpWZatLBkPFT1IuzU/edit?tab=t.0) |

## Core Question and Overview

**How do we ensure safety in a world with millions of interacting agents, built and deployed by many different actors?**  

AI agents are increasingly being deployed in multi-agent settings. While most present-day cases involve teams of agents orchestrated by a single actor (or ‘principal’), we are beginning to see the emergence of more complex ecosystems of agents deployed by different actors across shared digital infrastructure. These multi-principal, multi-agent interactions create new opportunities for cooperation and shared benefit ([Dafoe et al., 2021](https://www.nature.com/articles/d41586-021-01170-0)), but also new risks, which means focusing only on the safety and alignment of individual models is insufficient ([Hammond et al., 2025](https://arxiv.org/abs/2502.14143)).

More research is therefore urgently needed to understand safety and risk through a system-level, multi-agent lens – developing methods to analyse emergent collective dynamics, building infrastructure for trustworthy interaction between agents, and creating scalable approaches for monitoring and control of increasingly complex networks of AI systems. While some of these problems will be addressed by market forces, we expect others to fall through the gaps. This funding call aims to fill those gaps, catalysing the foundational scientific research needed to understand, evaluate, and control risks emerging from large-scale ecosystems of interacting AI agents, deployed by multiple actors.

The call has been inspired by three recent papers. First, Google DeepMind’s “ [Distributional AGI Safety](https://arxiv.org/abs/2512.16856) ” outlines the safety implications of highly capable AI systems emerging not as single monolithic agents, but through coordinated networks of specialised sub-AGI systems with differential access to tools, data, memory, and resources. Second, ARIA’s “ [Scaling Trust](https://aria.org.uk/opportunity-spaces/trust-everything-everywhere/scaling-trust/) ” programme thesis argues that, in a world of increasingly capable networked agents acting across digital and physical environments, coordination infrastructure that lets agents enter into 'contracts' securely, programmatically, at scale, and without intermediaries can preserve pluralism and unlock new forms of coordination. Finally, the Cooperative AI Foundation’s “ [Multi-Agent Risks from Advanced AI](https://www.cooperativeai.com/post/new-report-multi-agent-risks-from-advanced-ai) ” report argues that interacting populations of AI agents introduce qualitatively new failure modes beyond single-agent systems, including collusion, conflict, destabilising dynamics, emergent agency, and novel multi-agent security vulnerabilities. These perspectives in turn build on earlier work by [Minsky (1986)](https://dl.acm.org/doi/abs/10.5555/22939), [Huberman (1988)](https://dl.acm.org/doi/10.5555/59160), [Wooldridge & Jennings (1995)](https://www.cs.ox.ac.uk/people/michael.wooldridge/pubs/ker95.pdf), [Manheim (2018)](https://arxiv.org/abs/1810.10862), [Drexler (2019)](https://static1.squarespace.com/static/660e95991cf0293c2463bcc8/t/660ec8f0ca87a33aa8832af3/1712244978900/2019-1.pdf), [Critch & Krueger (2020)](https://arxiv.org/abs/2006.04948), [Clifton (2020)](https://longtermrisk.org/research-agenda/), [Dafoe et al. (2020)](https://arxiv.org/abs/2012.08630), [Conitzer & Oesterheld (2023)](https://ojs.aaai.org/index.php/AAAI/article/view/26791), [Chan et al. (2025)](https://arxiv.org/abs/2501.10114), [Kolt (2025)](https://arxiv.org/abs/2501.07913), [Hadfield & Koh (2025)](https://arxiv.org/abs/2509.01063), and [Tomašev et al. (2025)](https://arxiv.org/abs/2509.10147), among many others.

## Research Agenda

We organise this call into four sections, corresponding to the following research clusters:

1. Sandboxes and Testbeds address the first major bottleneck: without realistic, reproducible multi-agent environments, progress on the remaining sections is hard to evaluate or compare.
2. The Science of Agent Networks focuses on the safety-relevant properties of interacting agent populations: how collective capabilities emerge and scale, how networks of agents fail or become volatile, and how dangerous population-level properties can be detected.
3. Strengthening Agent Infrastructure concerns the evaluation and stress-testing of the technical primitives – identity, verifiability, reputation, communication, commitment – on which trustworthy multi-agent interactions will depend.
4. Multi-Agent Oversight and Control covers the detection, attribution, security, and intervention methods needed to keep deployed agent populations safe at scale.

We expect work in the latter clusters to build on work in the former clusters. Proposals may therefore target one cluster or span several, but we will prioritise those that target depth rather than breadth. In particular, we stress the importance of realistic sandboxes and testbeds (Section 1) for enabling scientific progress across the broader agenda. Where appropriate, we also encourage collaborations between teams addressing Section 1 with those addressing other sections, and welcome suggestions or requests for sandboxes and testbeds from those submitting proposals under other sections.

In what follows, the questions under each cluster are guidance, not an exhaustive specification. We welcome proposals that do not match the topics verbatim if they clearly advance the agenda's underlying goals. Topics explicitly out of scope are listed at the end.

### 1\. Sandboxes and Testbeds

Empirical work on the safety of multi-principal, multi-agent deployments is bottlenecked by the need for realistic and reproducible testbeds. Existing work has made important progress using stylised games and simulated social environments (e.g., [Akata et al., 2025](https://www.nature.com/articles/s41562-025-02172-y); [Gandhi et al., 2023](https://openreview.net/forum?id=MUtbsFRZwI); [Park et al., 2023](https://dl.acm.org/doi/10.1145/3586183.3606763)), though these settings face important limitations. We therefore seek testbeds that allow researchers to study populations of frontier-model agents interacting over extended periods with realistic tools, memory systems, economic constraints, and communication channels ([Kapoor et al., 2026](https://cruxevals.com/)). While we are interested in seeing proposals that address this section alone, we expect such environments to be deliberately designed to support the comparative evaluation of the theoretical measures, protocols, and oversight mechanisms discussed in later sections. Sandboxes and testbeds should be:

- Scalable to a realistic number of agents and an appropriate diversity of agentic tools, knowledge bases, etc.;
- High-fidelity, capturing behaviours of frontier AI agents rather than coarse abstractions;
- Externally valid, enabling a principled characterisation of the deployment conditions under which simulation-derived conclusions should and should not be trusted;
- Safe and secure, allowing dangerous collective behaviours to be studied without risk of uncontrolled deployment;
- Reproducible, enabling researchers to compare different methods.

We also welcome proposals that are not focused on a particular testbed or environment itself, but contribute significantly to addressing one or more of the problems above, such as:

- Navigating the trade-off between scalability and fidelity, for example, by using smaller, distilled models to serve as faithful proxies for frontier agents in simulations;
- Developing principled methods to utilise data from real-world deployments to design grounded environments and to evaluate their external validity;
- Building environment-agnostic infrastructure that enables interoperation between testbeds or methods for logging information across many agents.

### 2\. The Science of Agent Networks

Understanding the system-level properties and dynamics of populations of advanced AI agents is a foundational scientific challenge. It requires characterising how the properties of individual agents – their capabilities, objectives, and behavioural dispositions – contribute to population-level outcomes, as well as how the structure and dynamics of agent networks give rise to emergent vulnerabilities, failures, and collective behaviours. Of particular importance are cases where groups of agents form a ‘collective agent’, exhibiting coherent collective ‘goals’, strategies, or capabilities that are not predictable from individual systems in isolation.

Without this scientific foundation, individual-level safeguards may fail to anticipate system-level risks, reducing our ability to pre-empt, forecast, or diagnose the impacts of larger-scale deployments. We are especially interested in work that combines theoretical insight with empirical evaluation in realistic multi-agent settings. Illustrative research directions include:

1. From individual properties to system-level safety. Determining how the cooperation-relevant properties of individual agents – their strategic capabilities, propensity to cooperate or defect, and susceptibility to manipulation – shape system-level outcomes ([Tilli, 2026](https://openreview.net/forum?id=00KtDBoKnO)). Establishing relationships between agents’ training data, objectives, and model specifications and their cooperation-relevant properties.
2. Evaluating vulnerabilities in networks of AI agents. New evaluation frameworks for risks specific to multi-agent deployments, such as resilience to adversarial sub-populations, propagation of attacks between agents (e.g., [Lee & Tiwari, 2024](https://arxiv.org/abs/2410.07283)), and susceptibility to cascading failures. Red-teaming frameworks that can surface new collective failure modes at scale.
3. Modelling emergent capabilities and communication. Models and metrics that can be used to predict how collective capabilities, volatilities, and other safety-relevant properties vary with population size, heterogeneity, interaction topology, individual agent capabilities, and the availability of tools and resources. Areas of particular interest are the emergence and transferability of new forms of communication and the possibility of ‘phase transitions’ in agent populations.
4. Theoretical foundations of collective agency. Formal definitions of collective agency and emergent ‘goals’ or capabilities, with tractable operationalisations applicable to realistic settings. Several existing proposals (e.g., [Szabo & Teo, 2015](https://dl.acm.org/doi/10.1145/2815502); [Jørgensen et al., 2025](https://openreview.net/forum?id=NacA6YRBNX)) either require infeasibly many observations and interventions or rely on micro- or macro-level abstractions that are hard to instantiate in practice.
5. Evaluating dangerous emergent capabilities and goals. Evaluations that target whether combinations of agents exhibit specific dangerous capabilities or ‘goals’ absent in individuals. Examples include: coordination to resist modification or shutdown ([Agrawal et al., 2026](https://dl.acm.org/doi/abs/10.65109/HQQZ1937)), decomposing tasks to evade per-agent safety filters ([Jones et al., 2025](https://openreview.net/forum?id=GCkhEPE1FG)), developing covert communication channels ([Motwani et al., 2024](https://proceedings.neurips.cc/paper_files/paper/2024/hash/861f7dad098aec1c3560fb7add468d41-Abstract-Conference.html)), or accumulating resources and influence at the collective level.

### 3\. Strengthening Agent Infrastructure

Protocols and infrastructure for agent interaction, such as [A2A](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/), are emerging rapidly but tend to prioritise utility over security. The network effects driving their adoption and the nature of lock-in in digital infrastructure imply that we cannot afford to make safety an afterthought, but also that new infrastructure that attempts to replace increasingly entrenched incumbents is a less tractable direction. In this call, therefore, our focus is on stress-testing and strengthening existing agent infrastructure. This includes understanding and improving the safety-relevant properties of agent infrastructure and protocols (either theoretically or by empirical stress-testing in realistic scenarios), as well as providing additional support for features such as identity, reputation, accountability, provenance, commitment, or verifiable attributes, which have safety and governance implications ([Chan et al., 2025](https://arxiv.org/abs/2501.10114)). The distinctive properties of AI agents – including that they can be copied, modified, simulated, deleted, inspected, or deployed at scale – complicate familiar approaches to these problems while also enabling new solutions ([Conitzer & Oesterheld, 2023](https://ojs.aaai.org/index.php/AAAI/article/view/26791)).

1. Agent identity, authentication, and admission control. Understanding the requirements and challenges for agent IDs vis-à-vis current deployments ([Chan et al., 2024](https://arxiv.org/abs/2406.12137)), including update and revocation procedures compatible with agents being copied, modified, or merged, and the uses of proof-of-agent or proof-of-human credentials. Investigating what changes to standard cryptographic trust protocols are necessary for platform-side vetting and access control across heterogeneous agents.
2. Verifiable attributes, actions, and provenance. Methods for agents to reveal and verify their properties, resources, authorisation scope, and outputs, including zero-knowledge techniques where such information is strategically sensitive. Watermarking and scalable proofs of inference for attributing outputs to specific agents (e.g., [Kirchenbauer et al., 2023](https://proceedings.mlr.press/v202/kirchenbauer23a.html); [Sun et al., 2024](https://dl.acm.org/doi/10.1145/3658644.3670334)).
3. Reputation, accountability, and dispute resolution. Reputation system design for AI agents: how reputations are represented, what behavioural inputs feed them, how those inputs are aggregated, and how the resulting signals are made robust to gaming and manipulation. Infrastructure for tracking relationships and incidents across agent populations. Protocols for dispute resolution, renegotiation, and graceful termination when agreements break down.
4. Commitments and delegation. Methods for credible commitment without third-party enforcement, not just via cryptographic tools but also by delegating to sub-agents whose code or other properties can be checked ([Tennenholtz, 2004](https://www.sciencedirect.com/science/article/pii/S0899825604000314)). We are especially interested in provisions for mutually conditional commitments, scope attenuation, multi-principal support, verifiable revocation, and other approaches that can reduce downside risks. Contract compliance monitoring and defences against delegation risks such as Sybil attacks and threats/malicious delegates.

### 4\. Multi-Agent Oversight and Control

Many important risks from collective AI systems – including collusion, cascading failures, and emergent collective capabilities – are fundamentally population-level phenomena. Oversight mechanisms designed for individual agents may not straightforwardly scale to large populations of interacting systems. We therefore seek technical methods to detect, attribute, discourage, and control unsafe behaviour in deployed multi-agent systems. Importantly, these methods must remain robust under realistic, multi-principal deployment constraints and partial observability. We expect that they will build on the foundational science of agent networks (Section 2) and may also leverage emerging agent infrastructure (Section 3).

1. Detection of collusion and the evolution of inter-agent communication. Algorithms and tools to detect undesirable or unanticipated coordination between agents, including via emergent forms of communication or steganography (e.g., [Bonjour et al., 2022](https://openreview.net/forum?id=HCl41wIi9gc); [Riedl, 2026](https://openreview.net/forum?id=SRn1MtMPRq); [Rose et al., 2026](https://arxiv.org/abs/2604.01151)). Methods that can identify such signals from (partial observations of) both interaction and communication traces, ideally using privacy-preserving tools.
2. Attribution and oversight interfaces. Tools to help trace emergent failures back to specific agents, interactions, or delegation chains ([Zhang et al., 2025](https://openreview.net/forum?id=GazlTYxZss&noteId=cypPlShPMW)). Interfaces and visualisations that make agent populations – their structure, relationships, and decision processes – legible to human overseers, including interactive tools for exploring and querying populations at runtime.
3. Multi-agent control and scalable oversight. Extensions of AI control ([Greenblatt et al., 2025](https://arxiv.org/abs/2312.06942)) and scalable oversight methodologies (see [Shah et al., 2025](https://arxiv.org/abs/2504.01849), Section 6.1) to multi-agent settings. This includes designing secure harnesses and task-allocation architectures that respect cross-principal trust boundaries ([Foerster et al., 2026](https://arxiv.org/abs/2601.09923)), as well as red/blue-team evaluations of control protocols for robustness to subversion by groups of agents.
4. Mechanism and information design. Adaptive mechanism design tools and algorithms for promoting cooperation or preventing collusion among frontier-model agents in complex domains. Information design tools – what to reveal to which agents – to promote cooperation or reduce miscoordination. Circuit breakers, (de)synchronisation, and limits on agent action rates for stabilising volatile networks. Agents designed to foster population-level cooperation and stability when reliance on centralised mechanisms is undesirable or infeasible.

## Out of Scope

The following topics are not in scope, either because they are being pursued through other channels, because they concern individual rather than multi-principal, multi-agent safety problems, or because they fall outside the technical, system-level focus of the call:

- Single-agent safety. Alignment, interpretability, robustness, and oversight of individual AI agents, including defences against environmental attacks such as prompt injection, jailbreaks, and malicious web content, and methods for their detection.
- Capability advancement. Work aimed primarily at increasing the individual or collective capabilities of AI agents – including their general cooperative capabilities – in the absence of a clear safety motivation. If the primary contribution is a system that performs better at a task, and the safety analysis is secondary or post hoc, the work is out of scope regardless of framing.
- Individual-agent cooperation without system-level evaluation. Training methods, model specifications, or constitutions for making individual agents more cooperative, where evaluation stops at the individual or pairwise level.
- Solutions relying on a single agent deployer (‘principal’). Certain solutions to multi-agent problems rely on the existence of a privileged overseer or principal who governs and controls all agents. These solutions do not apply to the multi-principal deployments we focus on in this call.
- AI for human cooperation. AI-facilitated negotiation and mediation, AI for democratic institutions, and other applications where the primary objective is helping humans cooperate with one another rather than addressing the safety of multi-agent AI systems.
- Agentic inequality and power concentration. Although related to multi-agent safety, technical interventions that target disparities in who can deploy agents with different capabilities constitute a distinct agenda and are out of scope here.
- Non-technical work. Purely conceptual, philosophical, or policy-oriented contributions that do not involve technical elements or a plausible path to real-world technical implementation.
- Toy systems. Proposals that do not engage with frontier-model agents under realistic deployment conditions. This includes classical game-theoretic settings (e.g., iterated normal-form games or simple auctions with discrete action spaces) without a concrete and credible methodology for extending results to populations of natural-language (or multimodal) agents that use tools and have persistent memory in realistic environments.
- Naive application of pre-existing solutions. Proposals that straightforwardly apply standard mechanisms for identity, reputation, commitment, or trust (e.g., blockchain-based identity, human reputation systems) to AI agents without addressing challenges specific to the AI-agent setting - such as agent clonability, the absence of persistent biological identity, or machine-speed interactions.
- Commercial product development. This is a philanthropic funding call targeting work that markets would not otherwise do, and proposals will be evaluated through that lens. That said, we welcome research that produces open tools and frameworks, as well as foundational work that may yield downstream applications beyond the project’s immediate philanthropic purposes.

## Eligibility and Funding Tiers

We invite applicants to apply to either or both funding tiers: Tier 1 (Up to $300,000) or Tier 2 ($300,000-$1,000,000). Project durations can range from one to two years. Tier 1 aims to support exploratory research projects, pilot studies, or focused technical investigations, whereas Tier 2 targets more ambitious or collaborative projects.

We invite individual researchers, research teams, research institutions, and multi-institution collaborations across universities, national laboratories, institutes, and nonprofit research organisations. We are open globally and encourage collaborations across geographic boundaries. For any projects funded by Schmidt Sciences, indirect costs must be at or below 10% to comply with our [policy](https://www.schmidtsciences.org/faq/). Projects funded under this RFP must comply with all applicable law and may not include lobbying, efforts to influence legislation or political activity.

## Selection Criteria

Proposals will be evaluated holistically. Key considerations include:

1. **Research Agenda Fit.** Does the proposal clearly engage with the intention behind the scientific questions and objectives in the research agenda?
2. **Scientific Quality and Rigour.** Is the proposed work technically sound, well-motivated, and capable of producing generalizable insight?
3. **Potential Impact.** If successful, would the project materially advance scientific understanding relevant to this call, or meaningfully improve our ability to understand, evaluate, or control risks posed by multi-principal, multi-agent AI systems?
4. **Philanthropic fit.** Is there a clear market, coordination, or incentive failure that means commercial interests are unlikely to solve this problem?
5. **Feasibility and Scope.** Is there sufficient evidence to suggest that the proposal’s milestones and deliverables are ambitious yet well-defined and feasible enough to be achievable within the stated time duration?
6. **Team Expertise.** Is the team well-suited to execute the proposed work, with relevant technical expertise, sufficient capacity, and a time commitment commensurate with the project's ambition?
7. **Cost Appropriateness.** Is the proposed budget reasonable and well-justified given the project’s goals and planned activities?
8. **Additional funder-specific considerations.** Applications will be considered by the parties jointly supporting this funding call. If your proposal is selected for funding, the specific party or parties funding your project may provide additional limitations or guidance applicable to your award, which would be documented, if agreed upon, in your final award documentation.

[Apply](https://schmidtsciences.smapply.io/prog/297143/apply/?next=/prog/scaling_ai_safety_for_a_multi_agent_world/)

## Scaling AI Safety for a Multi-Agent World

## Scaling AI Safety for a Multi-Agent World

A joint funding call by [Schmidt Sciences](https://www.schmidtsciences.org/), [Google DeepMind](https://deepmind.google/), [Advanced Research & Invention Agency (ARIA)](https://aria.org.uk/), the [Cooperative AI Foundation](https://www.cooperativeai.com/foundation), and [Google.org](http://google.org/)

| Proposal Due Date | **August 8th, 2026** **by 11:59pm** [**AoE**](https://en.wikipedia.org/wiki/Anywhere_on_Earth) |
| --- | --- |
| Notification of Decision | **Autumn 2026** |
| Funding Tiers | **Tier 1: Up to US $300,000 (1-2 years)**  **Tier 2: US $300,000-$1,000,000 (1-2 years)** |
| Informational Webinars | **Tuesday, June 30 12 pm ET. Register [here](https://schmidtentities.zoom.us/webinar/register/WN_81mgT461QAm3agXR0nV_NA)**  **Thursday, July 23 10 am ET. Register [here](https://schmidtentities.zoom.us/webinar/register/WN_ZhzeK6fASZKIKC_hy4u8Ug)** |
| Contact email | **multiagentsafety@schmidtsciences.org** |
| Link to FAQ | [**FAQ**](https://docs.google.com/document/d/1LLRZvrKZD9rtKAWjWXPBVZpA5PTpWZatLBkPFT1IuzU/edit?tab=t.0) |

## Core Question and Overview

**How do we ensure safety in a world with millions of interacting agents, built and deployed by many different actors?**  

AI agents are increasingly being deployed in multi-agent settings. While most present-day cases involve teams of agents orchestrated by a single actor (or ‘principal’), we are beginning to see the emergence of more complex ecosystems of agents deployed by different actors across shared digital infrastructure. These multi-principal, multi-agent interactions create new opportunities for cooperation and shared benefit ([Dafoe et al., 2021](https://www.nature.com/articles/d41586-021-01170-0)), but also new risks, which means focusing only on the safety and alignment of individual models is insufficient ([Hammond et al., 2025](https://arxiv.org/abs/2502.14143)).

More research is therefore urgently needed to understand safety and risk through a system-level, multi-agent lens – developing methods to analyse emergent collective dynamics, building infrastructure for trustworthy interaction between agents, and creating scalable approaches for monitoring and control of increasingly complex networks of AI systems. While some of these problems will be addressed by market forces, we expect others to fall through the gaps. This funding call aims to fill those gaps, catalysing the foundational scientific research needed to understand, evaluate, and control risks emerging from large-scale ecosystems of interacting AI agents, deployed by multiple actors.

The call has been inspired by three recent papers. First, Google DeepMind’s “ [Distributional AGI Safety](https://arxiv.org/abs/2512.16856) ” outlines the safety implications of highly capable AI systems emerging not as single monolithic agents, but through coordinated networks of specialised sub-AGI systems with differential access to tools, data, memory, and resources. Second, ARIA’s “ [Scaling Trust](https://aria.org.uk/opportunity-spaces/trust-everything-everywhere/scaling-trust/) ” programme thesis argues that, in a world of increasingly capable networked agents acting across digital and physical environments, coordination infrastructure that lets agents enter into 'contracts' securely, programmatically, at scale, and without intermediaries can preserve pluralism and unlock new forms of coordination. Finally, the Cooperative AI Foundation’s “ [Multi-Agent Risks from Advanced AI](https://www.cooperativeai.com/post/new-report-multi-agent-risks-from-advanced-ai) ” report argues that interacting populations of AI agents introduce qualitatively new failure modes beyond single-agent systems, including collusion, conflict, destabilising dynamics, emergent agency, and novel multi-agent security vulnerabilities. These perspectives in turn build on earlier work by [Minsky (1986)](https://dl.acm.org/doi/abs/10.5555/22939), [Huberman (1988)](https://dl.acm.org/doi/10.5555/59160), [Wooldridge & Jennings (1995)](https://www.cs.ox.ac.uk/people/michael.wooldridge/pubs/ker95.pdf), [Manheim (2018)](https://arxiv.org/abs/1810.10862), [Drexler (2019)](https://static1.squarespace.com/static/660e95991cf0293c2463bcc8/t/660ec8f0ca87a33aa8832af3/1712244978900/2019-1.pdf), [Critch & Krueger (2020)](https://arxiv.org/abs/2006.04948), [Clifton (2020)](https://longtermrisk.org/research-agenda/), [Dafoe et al. (2020)](https://arxiv.org/abs/2012.08630), [Conitzer & Oesterheld (2023)](https://ojs.aaai.org/index.php/AAAI/article/view/26791), [Chan et al. (2025)](https://arxiv.org/abs/2501.10114), [Kolt (2025)](https://arxiv.org/abs/2501.07913), [Hadfield & Koh (2025)](https://arxiv.org/abs/2509.01063), and [Tomašev et al. (2025)](https://arxiv.org/abs/2509.10147), among many others.

## Research Agenda

We organise this call into four sections, corresponding to the following research clusters:

1. Sandboxes and Testbeds address the first major bottleneck: without realistic, reproducible multi-agent environments, progress on the remaining sections is hard to evaluate or compare.
2. The Science of Agent Networks focuses on the safety-relevant properties of interacting agent populations: how collective capabilities emerge and scale, how networks of agents fail or become volatile, and how dangerous population-level properties can be detected.
3. Strengthening Agent Infrastructure concerns the evaluation and stress-testing of the technical primitives – identity, verifiability, reputation, communication, commitment – on which trustworthy multi-agent interactions will depend.
4. Multi-Agent Oversight and Control covers the detection, attribution, security, and intervention methods needed to keep deployed agent populations safe at scale.

We expect work in the latter clusters to build on work in the former clusters. Proposals may therefore target one cluster or span several, but we will prioritise those that target depth rather than breadth. In particular, we stress the importance of realistic sandboxes and testbeds (Section 1) for enabling scientific progress across the broader agenda. Where appropriate, we also encourage collaborations between teams addressing Section 1 with those addressing other sections, and welcome suggestions or requests for sandboxes and testbeds from those submitting proposals under other sections.

In what follows, the questions under each cluster are guidance, not an exhaustive specification. We welcome proposals that do not match the topics verbatim if they clearly advance the agenda's underlying goals. Topics explicitly out of scope are listed at the end.

### 1\. Sandboxes and Testbeds

Empirical work on the safety of multi-principal, multi-agent deployments is bottlenecked by the need for realistic and reproducible testbeds. Existing work has made important progress using stylised games and simulated social environments (e.g., [Akata et al., 2025](https://www.nature.com/articles/s41562-025-02172-y); [Gandhi et al., 2023](https://openreview.net/forum?id=MUtbsFRZwI); [Park et al., 2023](https://dl.acm.org/doi/10.1145/3586183.3606763)), though these settings face important limitations. We therefore seek testbeds that allow researchers to study populations of frontier-model agents interacting over extended periods with realistic tools, memory systems, economic constraints, and communication channels ([Kapoor et al., 2026](https://cruxevals.com/)). While we are interested in seeing proposals that address this section alone, we expect such environments to be deliberately designed to support the comparative evaluation of the theoretical measures, protocols, and oversight mechanisms discussed in later sections. Sandboxes and testbeds should be:

- Scalable to a realistic number of agents and an appropriate diversity of agentic tools, knowledge bases, etc.;
- High-fidelity, capturing behaviours of frontier AI agents rather than coarse abstractions;
- Externally valid, enabling a principled characterisation of the deployment conditions under which simulation-derived conclusions should and should not be trusted;
- Safe and secure, allowing dangerous collective behaviours to be studied without risk of uncontrolled deployment;
- Reproducible, enabling researchers to compare different methods.

We also welcome proposals that are not focused on a particular testbed or environment itself, but contribute significantly to addressing one or more of the problems above, such as:

- Navigating the trade-off between scalability and fidelity, for example, by using smaller, distilled models to serve as faithful proxies for frontier agents in simulations;
- Developing principled methods to utilise data from real-world deployments to design grounded environments and to evaluate their external validity;
- Building environment-agnostic infrastructure that enables interoperation between testbeds or methods for logging information across many agents.

### 2\. The Science of Agent Networks

Understanding the system-level properties and dynamics of populations of advanced AI agents is a foundational scientific challenge. It requires characterising how the properties of individual agents – their capabilities, objectives, and behavioural dispositions – contribute to population-level outcomes, as well as how the structure and dynamics of agent networks give rise to emergent vulnerabilities, failures, and collective behaviours. Of particular importance are cases where groups of agents form a ‘collective agent’, exhibiting coherent collective ‘goals’, strategies, or capabilities that are not predictable from individual systems in isolation.

Without this scientific foundation, individual-level safeguards may fail to anticipate system-level risks, reducing our ability to pre-empt, forecast, or diagnose the impacts of larger-scale deployments. We are especially interested in work that combines theoretical insight with empirical evaluation in realistic multi-agent settings. Illustrative research directions include:

1. From individual properties to system-level safety. Determining how the cooperation-relevant properties of individual agents – their strategic capabilities, propensity to cooperate or defect, and susceptibility to manipulation – shape system-level outcomes ([Tilli, 2026](https://openreview.net/forum?id=00KtDBoKnO)). Establishing relationships between agents’ training data, objectives, and model specifications and their cooperation-relevant properties.
2. Evaluating vulnerabilities in networks of AI agents. New evaluation frameworks for risks specific to multi-agent deployments, such as resilience to adversarial sub-populations, propagation of attacks between agents (e.g., [Lee & Tiwari, 2024](https://arxiv.org/abs/2410.07283)), and susceptibility to cascading failures. Red-teaming frameworks that can surface new collective failure modes at scale.
3. Modelling emergent capabilities and communication. Models and metrics that can be used to predict how collective capabilities, volatilities, and other safety-relevant properties vary with population size, heterogeneity, interaction topology, individual agent capabilities, and the availability of tools and resources. Areas of particular interest are the emergence and transferability of new forms of communication and the possibility of ‘phase transitions’ in agent populations.
4. Theoretical foundations of collective agency. Formal definitions of collective agency and emergent ‘goals’ or capabilities, with tractable operationalisations applicable to realistic settings. Several existing proposals (e.g., [Szabo & Teo, 2015](https://dl.acm.org/doi/10.1145/2815502); [Jørgensen et al., 2025](https://openreview.net/forum?id=NacA6YRBNX)) either require infeasibly many observations and interventions or rely on micro- or macro-level abstractions that are hard to instantiate in practice.
5. Evaluating dangerous emergent capabilities and goals. Evaluations that target whether combinations of agents exhibit specific dangerous capabilities or ‘goals’ absent in individuals. Examples include: coordination to resist modification or shutdown ([Agrawal et al., 2026](https://dl.acm.org/doi/abs/10.65109/HQQZ1937)), decomposing tasks to evade per-agent safety filters ([Jones et al., 2025](https://openreview.net/forum?id=GCkhEPE1FG)), developing covert communication channels ([Motwani et al., 2024](https://proceedings.neurips.cc/paper_files/paper/2024/hash/861f7dad098aec1c3560fb7add468d41-Abstract-Conference.html)), or accumulating resources and influence at the collective level.

### 3\. Strengthening Agent Infrastructure

Protocols and infrastructure for agent interaction, such as [A2A](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/), are emerging rapidly but tend to prioritise utility over security. The network effects driving their adoption and the nature of lock-in in digital infrastructure imply that we cannot afford to make safety an afterthought, but also that new infrastructure that attempts to replace increasingly entrenched incumbents is a less tractable direction. In this call, therefore, our focus is on stress-testing and strengthening existing agent infrastructure. This includes understanding and improving the safety-relevant properties of agent infrastructure and protocols (either theoretically or by empirical stress-testing in realistic scenarios), as well as providing additional support for features such as identity, reputation, accountability, provenance, commitment, or verifiable attributes, which have safety and governance implications ([Chan et al., 2025](https://arxiv.org/abs/2501.10114)). The distinctive properties of AI agents – including that they can be copied, modified, simulated, deleted, inspected, or deployed at scale – complicate familiar approaches to these problems while also enabling new solutions ([Conitzer & Oesterheld, 2023](https://ojs.aaai.org/index.php/AAAI/article/view/26791)).

1. Agent identity, authentication, and admission control. Understanding the requirements and challenges for agent IDs vis-à-vis current deployments ([Chan et al., 2024](https://arxiv.org/abs/2406.12137)), including update and revocation procedures compatible with agents being copied, modified, or merged, and the uses of proof-of-agent or proof-of-human credentials. Investigating what changes to standard cryptographic trust protocols are necessary for platform-side vetting and access control across heterogeneous agents.
2. Verifiable attributes, actions, and provenance. Methods for agents to reveal and verify their properties, resources, authorisation scope, and outputs, including zero-knowledge techniques where such information is strategically sensitive. Watermarking and scalable proofs of inference for attributing outputs to specific agents (e.g., [Kirchenbauer et al., 2023](https://proceedings.mlr.press/v202/kirchenbauer23a.html); [Sun et al., 2024](https://dl.acm.org/doi/10.1145/3658644.3670334)).
3. Reputation, accountability, and dispute resolution. Reputation system design for AI agents: how reputations are represented, what behavioural inputs feed them, how those inputs are aggregated, and how the resulting signals are made robust to gaming and manipulation. Infrastructure for tracking relationships and incidents across agent populations. Protocols for dispute resolution, renegotiation, and graceful termination when agreements break down.
4. Commitments and delegation. Methods for credible commitment without third-party enforcement, not just via cryptographic tools but also by delegating to sub-agents whose code or other properties can be checked ([Tennenholtz, 2004](https://www.sciencedirect.com/science/article/pii/S0899825604000314)). We are especially interested in provisions for mutually conditional commitments, scope attenuation, multi-principal support, verifiable revocation, and other approaches that can reduce downside risks. Contract compliance monitoring and defences against delegation risks such as Sybil attacks and threats/malicious delegates.

### 4\. Multi-Agent Oversight and Control

Many important risks from collective AI systems – including collusion, cascading failures, and emergent collective capabilities – are fundamentally population-level phenomena. Oversight mechanisms designed for individual agents may not straightforwardly scale to large populations of interacting systems. We therefore seek technical methods to detect, attribute, discourage, and control unsafe behaviour in deployed multi-agent systems. Importantly, these methods must remain robust under realistic, multi-principal deployment constraints and partial observability. We expect that they will build on the foundational science of agent networks (Section 2) and may also leverage emerging agent infrastructure (Section 3).

1. Detection of collusion and the evolution of inter-agent communication. Algorithms and tools to detect undesirable or unanticipated coordination between agents, including via emergent forms of communication or steganography (e.g., [Bonjour et al., 2022](https://openreview.net/forum?id=HCl41wIi9gc); [Riedl, 2026](https://openreview.net/forum?id=SRn1MtMPRq); [Rose et al., 2026](https://arxiv.org/abs/2604.01151)). Methods that can identify such signals from (partial observations of) both interaction and communication traces, ideally using privacy-preserving tools.
2. Attribution and oversight interfaces. Tools to help trace emergent failures back to specific agents, interactions, or delegation chains ([Zhang et al., 2025](https://openreview.net/forum?id=GazlTYxZss&noteId=cypPlShPMW)). Interfaces and visualisations that make agent populations – their structure, relationships, and decision processes – legible to human overseers, including interactive tools for exploring and querying populations at runtime.
3. Multi-agent control and scalable oversight. Extensions of AI control ([Greenblatt et al., 2025](https://arxiv.org/abs/2312.06942)) and scalable oversight methodologies (see [Shah et al., 2025](https://arxiv.org/abs/2504.01849), Section 6.1) to multi-agent settings. This includes designing secure harnesses and task-allocation architectures that respect cross-principal trust boundaries ([Foerster et al., 2026](https://arxiv.org/abs/2601.09923)), as well as red/blue-team evaluations of control protocols for robustness to subversion by groups of agents.
4. Mechanism and information design. Adaptive mechanism design tools and algorithms for promoting cooperation or preventing collusion among frontier-model agents in complex domains. Information design tools – what to reveal to which agents – to promote cooperation or reduce miscoordination. Circuit breakers, (de)synchronisation, and limits on agent action rates for stabilising volatile networks. Agents designed to foster population-level cooperation and stability when reliance on centralised mechanisms is undesirable or infeasible.

## Out of Scope

The following topics are not in scope, either because they are being pursued through other channels, because they concern individual rather than multi-principal, multi-agent safety problems, or because they fall outside the technical, system-level focus of the call:

- Single-agent safety. Alignment, interpretability, robustness, and oversight of individual AI agents, including defences against environmental attacks such as prompt injection, jailbreaks, and malicious web content, and methods for their detection.
- Capability advancement. Work aimed primarily at increasing the individual or collective capabilities of AI agents – including their general cooperative capabilities – in the absence of a clear safety motivation. If the primary contribution is a system that performs better at a task, and the safety analysis is secondary or post hoc, the work is out of scope regardless of framing.
- Individual-agent cooperation without system-level evaluation. Training methods, model specifications, or constitutions for making individual agents more cooperative, where evaluation stops at the individual or pairwise level.
- Solutions relying on a single agent deployer (‘principal’). Certain solutions to multi-agent problems rely on the existence of a privileged overseer or principal who governs and controls all agents. These solutions do not apply to the multi-principal deployments we focus on in this call.
- AI for human cooperation. AI-facilitated negotiation and mediation, AI for democratic institutions, and other applications where the primary objective is helping humans cooperate with one another rather than addressing the safety of multi-agent AI systems.
- Agentic inequality and power concentration. Although related to multi-agent safety, technical interventions that target disparities in who can deploy agents with different capabilities constitute a distinct agenda and are out of scope here.
- Non-technical work. Purely conceptual, philosophical, or policy-oriented contributions that do not involve technical elements or a plausible path to real-world technical implementation.
- Toy systems. Proposals that do not engage with frontier-model agents under realistic deployment conditions. This includes classical game-theoretic settings (e.g., iterated normal-form games or simple auctions with discrete action spaces) without a concrete and credible methodology for extending results to populations of natural-language (or multimodal) agents that use tools and have persistent memory in realistic environments.
- Naive application of pre-existing solutions. Proposals that straightforwardly apply standard mechanisms for identity, reputation, commitment, or trust (e.g., blockchain-based identity, human reputation systems) to AI agents without addressing challenges specific to the AI-agent setting - such as agent clonability, the absence of persistent biological identity, or machine-speed interactions.
- Commercial product development. This is a philanthropic funding call targeting work that markets would not otherwise do, and proposals will be evaluated through that lens. That said, we welcome research that produces open tools and frameworks, as well as foundational work that may yield downstream applications beyond the project’s immediate philanthropic purposes.

## Eligibility and Funding Tiers

We invite applicants to apply to either or both funding tiers: Tier 1 (Up to $300,000) or Tier 2 ($300,000-$1,000,000). Project durations can range from one to two years. Tier 1 aims to support exploratory research projects, pilot studies, or focused technical investigations, whereas Tier 2 targets more ambitious or collaborative projects.

We invite individual researchers, research teams, research institutions, and multi-institution collaborations across universities, national laboratories, institutes, and nonprofit research organisations. We are open globally and encourage collaborations across geographic boundaries. For any projects funded by Schmidt Sciences, indirect costs must be at or below 10% to comply with our [policy](https://www.schmidtsciences.org/faq/). Projects funded under this RFP must comply with all applicable law and may not include lobbying, efforts to influence legislation or political activity.

## Selection Criteria

Proposals will be evaluated holistically. Key considerations include:

1. **Research Agenda Fit.** Does the proposal clearly engage with the intention behind the scientific questions and objectives in the research agenda?
2. **Scientific Quality and Rigour.** Is the proposed work technically sound, well-motivated, and capable of producing generalizable insight?
3. **Potential Impact.** If successful, would the project materially advance scientific understanding relevant to this call, or meaningfully improve our ability to understand, evaluate, or control risks posed by multi-principal, multi-agent AI systems?
4. **Philanthropic fit.** Is there a clear market, coordination, or incentive failure that means commercial interests are unlikely to solve this problem?
5. **Feasibility and Scope.** Is there sufficient evidence to suggest that the proposal’s milestones and deliverables are ambitious yet well-defined and feasible enough to be achievable within the stated time duration?
6. **Team Expertise.** Is the team well-suited to execute the proposed work, with relevant technical expertise, sufficient capacity, and a time commitment commensurate with the project's ambition?
7. **Cost Appropriateness.** Is the proposed budget reasonable and well-justified given the project’s goals and planned activities?
8. **Additional funder-specific considerations.** Applications will be considered by the parties jointly supporting this funding call. If your proposal is selected for funding, the specific party or parties funding your project may provide additional limitations or guidance applicable to your award, which would be documented, if agreed upon, in your final award documentation.

[Apply](https://schmidtsciences.smapply.io/prog/297143/apply/?next=/prog/scaling_ai_safety_for_a_multi_agent_world/)

Opens

##### Jun 11 2026 06:59 AM (EDT)

Deadline