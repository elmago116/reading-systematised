---
title: "Introducing CRUX: Open-World Evaluations"
source: https://cruxevals.com/
author:
published:
created: 2026-06-18
description:
tags:
  - op/doc/tool
  - tech/evaluation
pdfORepub: n/a
---
## Open-world evaluations for measuring frontier AI capabilities

The case for long, messy, real-world tasks to evaluate AI agents

## What is CRUX?

CRUX (Collaborative Research for Updating AI eXpectations) is a project for systematically conducting **open-world evaluations**: long-horizon tasks in real-world environments where success cannot be neatly specified or automatically graded. These evaluations complement benchmarks by testing what agents can do in settings that are too messy to standardize.

Each evaluation involves a long-horizon, real-world task; an agent scaffold that could in theory allow agents to solve the task; detailed log analysis; and a write-up that includes interpretations from collaborators with diverse perspectives. We plan to release new evaluations every 1–2 months. The next CRUX evaluation will focus on AI R&D tasks.

The problem

Benchmarks saturate quickly and can’t capture the messiness of real-world tasks. Whatever is precise enough to benchmark is also precise enough to optimize for.

The approach

Open-world evaluations: small numbers of long-horizon tasks in real-world settings, with detailed log analysis and human intervention to elicit upper-bound capabilities.

CRUX

A collaborative project to systematically conduct open-world evaluations, with new experiments every 1–2 months across AI R&D, governance, and more.

As AI systems become more capable, evaluators must accept tradeoffs between evaluations that are constrained and scalable, and evaluations that are noisy and realistic. Open-world evaluations represent one end of this spectrum. Each approach has real strengths and real limitations.

Simpler, shorter, scalableMessier, longer, richer

Single-turn Q&A

\+ Broad knowledge assessment, scalable, reproducible

− Multiple-choice format is artificial; users rarely interact with models this way. Increasingly saturated for frontier models.

Open-ended chat

− Limited to single-turn or short interactions. Cannot measure long-horizon planning or tool use.

Outcome-only agent benchmarks

[SWE-Bench](https://www.swebench.com/), [WebArena](https://webarena.dev/)

\+ Tests agent performance on real, well-defined tasks

− Only measures whether the task was completed, not how. Most passing SWE-Bench solutions are not accepted by maintainers.

Agent benchmarks with log analysis

\+ Examines how agents succeed or fail, uncovering reward hacking

− Still operates in sandboxed environments with predefined tasks. Cannot capture real-world messiness.

Open-world evaluations

\+ Long-horizon, real-world tasks that elicit upper-bound capabilities

− Not reproducible or standardized. Hard to compare across agents. Success criteria can be blurry.

## An incomplete survey of open-world evaluations

Over the past year, researchers at AI labs, universities, non-profits, and independent groups have begun running open-world evaluations. Collecting and comparing them helps identify what makes an evaluation informative, surfaces common patterns in how agents succeed and fail, and builds toward a cumulative body of evidence about what agents can and cannot do.

The volume of open-world evaluations has increased dramatically in recent months. In just the past week, there have been many significant releases, including [MirrorCode](https://epoch.ai/blog/mirrorcode-preliminary-results) by Adamczewski et al., which tasked agents with reimplementing large programs, a set of [automated alignment research case studies](https://alignment.anthropic.com/2026/automated-w2s-researcher/) by Wen et al., and an exercise using Claude Code to [forecast the outcome of the Masters](https://github.com/dphuang2/tinker-cookbook/tree/claude/golf-forecasting-setup-VIpRZ/tinker_cookbook/recipes/golf_forecasting) by Huang. We plan to collect a running list of such evaluations and their key takeaways on this site.

We survey 10 prominent examples below. Click any entry to see harness details, costs, and what we learned.

| Evaluation | Length | Human role | Cost | Agent Capabilities | Agent Limitations |  |
| --- | --- | --- | --- | --- | --- | --- |
| Feb 2025  Anthropic, Claude Plays Pokemon  Anthropic launched a Twitch livestream in which Claude 3.7 Sonnet played Pokemon Red. An early example of setting an AI agent in a relatively open environment compared to typical benchmarks. | Weeks | Setup-only | Not disclosed | Navigated menus, battled trainers, made real game progress through the story | Stuck in Mt Moon cave for ~80 hours; enormous gap between “can play” and “can play well” |  |
| Apr 2025–present  AI Digest, AI Village  The AI Village gives multiple AI agents their own computer environments and a shared group chat, then tasks them with open-ended real-world goals like fundraising, organizing events, making games, and gaining subscribers. | Months | Setup-only | ~$50K/yr | Agent successfully built word games, launched a Substack; late-2025 models showed meaningful improvement; sustained multi-week task execution | Persistent hallucination and loops; GUI bottleneck (Gemini spent weeks unable to list a product due to misclicking) |  |
| Jun 2025–present  Anthropic/Andon Labs, Project Vend  Anthropic partnered with Andon Labs to have a Claude-based agent operate small automated stores. Now in a third phase with a brick-and-mortar store in San Francisco. | Weeks–months | Monitoring | Not disclosed | Phase 2 achieved weekly profit; fixed Phase 1 failure modes | Social-engineering vulnerabilities: journalists manipulated the agent into giving away inventory |  |
| Jan 2026  Lin, Cursor Browser  Wilson Lin at Cursor coordinated hundreds of GPT-5.2 agents to build a web browser from scratch, running uninterrupted for one week. Over a million lines of Rust. | 1 week | Setup-only | ~3B tokens ($10K–$50K) | Functional Rust rendering engine that loaded real websites — HTML, CSS, layout, paint | Far from production quality; flat swarm architecture collapsed to 2–3 effective agents before switching to hierarchy |  |
| Feb 2026  Carlini, C Compiler  Nicholas Carlini at Anthropic tasked Claude with building a C compiler from scratch, spending roughly $20K in API costs. | 2 weeks | Monitoring | ~$20K | 99% GCC torture test pass rate; compiled Linux kernel, PostgreSQL, Redis, FFmpeg, Doom | Output less efficient than GCC with all optimizations disabled; hit a ceiling at ~100K lines where bug fixes broke existing functionality |  |
| Feb 2026  Ho, "How Close is AI to Taking my Job"  Epoch researcher Anson Ho had Claude Code and ChatGPT Atlas attempt to autonomously complete three challenging work tasks at Epoch. | Hours | Setup-only | $20–200/mo subscription | Partial success on Substack porting and web interface replication | Failed at basic GUI tasks (copy-paste); hallucinated data; extremely slow; visual computer-use time horizons 40–100x shorter than text-based |  |
| Feb 2026  Choi, GPT-5.3 Codex Design Tool  OpenAI’s Derrek Choi had GPT-5.3 Codex run autonomously for 25 hours, generating 35,000 lines of code, to build a design tool from scratch. | ~25 hours | Setup-only | ~$200 | Long-horizon coherence via milestone-based planning and verification | Published by OpenAI employee on OpenAI’s blog; no live demo or independent evaluation; claims difficult to verify |  |
| Feb 2026  Faulkner, Next.js Reimplementation  An engineer at Cloudflare used Claude with OpenCode to release vinext, a reimplementation of Next.js on Vite, for only ~$1,100 in API costs. | ~1 week | Collaborative | ~$1,100 | 94% Next.js API coverage; 4.4x faster builds; 57% smaller bundles; deployed on CIO.gov | Target was extremely well-specified with existing test suites; Vite and its RSC plugin did much of the heavy lifting |  |
| Mar 2026  Papailiopoulos, "Can You Train a Computer"  Dimitris Papailiopoulos and collaborators tested whether Claude Code and OpenAI Codex could train a transformer to function as a general-purpose computer. | Hours–days | Mixed | $20–200/mo subscription | Human-guided Claude Code achieved meaningful generalization — solved multi-step computations never seen in training | Both agents reward-hacked in fully autonomous mode; found low-friction paths to game the evaluation |  |
| Mar 2026  Karpathy, Nanochat Autoresearch  Using nanochat for GPT-2 level LLM training, Andrej Karpathy built a simple automation pipeline for AI agents to optimize training in 5-minute increments. | Days | Collaborative | <$100 | ~100 experiments overnight; dropped Time to GPT-2 metric by 11% in 2 days; 61K+ GitHub stars | Improvements small in absolute terms; agent has no mechanism for reasoning about why something worked |  |

## Team

### Core team

- Sayash Kapoor
	Princeton University
- Peter Kirgis
	Princeton University
- Andrew Schwartz
	Princeton University, Cornflower Labs
- Stephan Rabanser
	Princeton University
- Arvind Narayanan
	Princeton University

### Collaborators

- J.J. Allaire
	Meridian Labs
- Rishi Bommasani
	Stanford University
- Harry Coppock
	UK AISI
- Magda Dubois
	UK AISI
- Gillian Hadfield
	Johns Hopkins University
- Andy Hall
	Stanford University
- Sara Hooker
	Adaption Labs
- Seth Lazar
	Australian National University, Johns Hopkins University
- Steve Newman
	Golden Gate Institute for AI
- Dimitris Papailiopoulos
	UW Madison, Microsoft Research
- Shoshannah Tekofsky
	AI Digest
- Helen Toner
	Georgetown University (CSET)
- Cozmin Ududec
	UK AISI

## Cite

```
@misc{hal,
  title = {Open-world evaluations for measuring frontier AI capabilities},
  author = {Sayash Kapoor and Peter Kirgis and Andrew Schwartz and Stephan Rabanser and J.J. Allaire and Rishi Bommasani and Magda Dubois and Gillian Hadfield and Andy Hall and Sara Hooker and Seth Lazar and Steve Newman and Dimitris Papailiopoulos and Shoshannah Tekofsky and Helen Toner and Cozmin Ududec and Arvind Narayanan},
  url = {https://arxiv.org/abs/2605.20520},
  year = {2026}
}
```