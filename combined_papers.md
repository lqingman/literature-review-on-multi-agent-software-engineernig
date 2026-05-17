# Combined Paper Pool — Multi-Agent LLM Software Engineering
## Three-Way Merge: Your filtered_papers.md + Classmate 1 (PDF1) + Classmate 2 / S. Fang (PDF2)

**Date:** 2026-05-16  
**Total unique papers:** 34  
**Summaries populated:** 15 (from paper_summaries.md) · 19 pending (from classmates' reviews only)

**Sources merged:**
- **YOURS** — `filtered_papers.md` (your 15-paper cross-validated selection)
- **PDF1** — Classmate 1's review (anonymous, 4-page paper, 14 references)
- **PDF2** — S. Fang's review (5-page paper, 12 references)

**Source legend:**
| Symbol | Meaning |
|--------|---------|
| ◆ YOURS | In your filtered_papers.md |
| ① PDF1 | In Classmate 1's reference list |
| ② PDF2 | In S. Fang's reference list |

---

## Section 1: Surveys & Foundational Works (10 papers)

---

### W1 — A Survey on Large Language Model based Autonomous Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Wang2023autonomousagents |
| **Authors** | Lei Wang, Chen Ma, Xueyang Feng, Zeyu Zhang, et al. |
| **Year** | 2023 (published Frontiers of Computer Science 2024) |
| **Venue** | Frontiers of Computer Science |
| **Citations** | **2,011** |
| **DOI** | 10.1007/s11704-024-40231-1 · arXiv:2308.11432 |
| **Sources** | ◆ YOURS |

**Main Contribution**
One of the earliest and most-cited foundational surveys on LLM-based autonomous agents. Proposes a unified framework for agent construction and surveys diverse applications across social science, natural science, and engineering domains.

**Methods Used**
- Literature review and synthesis
- Unified agent construction framework covering: profile, memory, planning, action modules
- Applications survey across scientific domains

**Results / Findings**
- LLMs demonstrate remarkable potential in achieving human-level intelligence through acquired web knowledge
- Four key agent modules identified: profile, memory, planning, action
- Agent evaluation remains an open challenge across all domains

**Limitations**
- Published in 2023 — predates most multi-agent SE frameworks
- Does not cover SE-specific benchmarks or workflows in depth

**How It Relates to the Review**
This is a foundational paper establishing the conceptual vocabulary (agent memory, planning, action). Cite in the background/foundations section when defining what an "agent" is.

**Critical Analysis**
- *Problem solved:* No unified framework existed for understanding the range of LLM-based agent applications
- *Key assumptions:* LLM knowledge scales to human-level task performance in diverse domains
- *Comparison to others:* More foundational than He et al. (W2); broader scope than SE-specific surveys
- *Strengths:* Highest-cited paper in the pool (2,011), clear framework, published in peer-reviewed journal
- *Weaknesses:* Predates the rapid 2024–2025 developments; SE coverage shallow
- *Open questions:* How do agent memory and planning mechanisms scale to enterprise SE tasks?

---

### W2 — LLM-Based Multi-Agent Systems for Software Engineering: Literature Review, Vision, and the Road Ahead

| Field | Details |
|-------|---------|
| **BibTeX key** | He2025literaturereview |
| **Authors** | Junda He, Christoph Treude, David Lo |
| **Year** | 2025 (submitted April 2024, revised July 2025) |
| **Venue** | ACM Transactions on Software Engineering and Methodology (TOSEM) — Q1 |
| **Citations** | ~144 |
| **DOI** | 10.1145/3712003 · arXiv:2404.04834 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 |

**Main Contribution**
The most directly relevant survey to this literature review. Systematically maps LLM-based multi-agent (LMA) systems across the software development lifecycle (requirements, code generation, QA, maintenance) and proposes a research agenda for autonomous, scalable, trustworthy systems.

**Methods Used**
- Systematic literature review (41 primary studies)
- Two case studies demonstrating state-of-the-art LMA frameworks
- Mapping across SDLC stages

**Results / Findings**
- Collaborative and specialized multi-agent abilities enable autonomous problem-solving, improve robustness, and provide scalable solutions
- Multi-agent systems outperform single-agent baselines across most SDLC tasks
- Identifies research gaps: trustworthiness, scalability, human-agent collaboration

**Limitations**
- Limited empirical evaluation in real-world industrial settings
- Survey scope limited to studies published before November 2024

**How It Relates to the Review**
This is the foundational reference for the entire literature review. Use it to establish scope, cite for the definition of LMA systems, and use its taxonomy as a backbone for thematic organization.

**Critical Analysis**
- *Problem solved:* Lack of systematic understanding of how multi-agent LLM systems are applied across the full SE lifecycle
- *Key assumptions:* Assumes multi-agent collaboration is inherently superior to single-agent — challenged by Agentless (F5)
- *Comparison to others:* More comprehensive SDLC coverage than Jin et al. (W6); more SE-specific than Wang et al. (W1)
- *Strengths:* Highly rigorous, peer-reviewed, covers entire SDLC, includes vision/roadmap
- *Weaknesses:* Pre-dates key 2025 developments; limited industrial case studies
- *Open questions:* How to ensure trustworthiness at scale? How to measure agent autonomy?

---

### W3 — Large Language Model-Based Agents for Software Engineering: A Survey

| Field | Details |
|-------|---------|
| **BibTeX key** | Liu2024agentssurvey |
| **Authors** | Junwei Liu, Kaixin Wang, Yixuan Chen, Xin Peng, Zhenpeng Chen, Lingming Zhang, Yiling Lou |
| **Year** | 2024 |
| **Venue** | ACM Transactions on Software Engineering and Methodology (TOSEM) — Q1 |
| **Citations** | ~151 |
| **DOI** | 10.48550/arxiv.2409.02977 |
| **Sources** | ◆ YOURS · ① PDF1 |

**Main Contribution**
A systematic survey collecting and categorizing 124 papers from both SE-task and agent-architecture perspectives. One of the largest systematic reviews in this space.

**Methods Used**
- Systematic literature review of 124 papers
- Dual-perspective categorization: SE domain view + agent architecture view
- Analysis of agent capabilities: perception, external tools/resources, multi-agent interaction

**Results / Findings**
- LLM-based agents substantially extend LLM versatility by adding perception and tool-use capabilities
- Combining multiple agents with human interaction shows the most promise for complex real-world SE
- Identifies 6 key agent capability dimensions across SE tasks

**Limitations**
- Does not fully address evaluation challenges (how to benchmark agent performance reliably)
- Limited coverage of industrial deployments

**How It Relates to the Review**
The 124-paper scope makes this an excellent citation for breadth. Use it for the background section to establish that this is a rapidly growing field, and for specific agent capability categorizations.

**Critical Analysis**
- *Problem solved:* Fragmented understanding of how LLM agents enhance SE tasks
- *Key assumptions:* Agent-based SE is a meaningful category distinct from LLM-only SE
- *Comparison to others:* Broader paper scope than He et al. (W2); more SE-specific than Chen et al.
- *Strengths:* Largest paper corpus (124), dual-perspective analysis, TOSEM-quality rigor
- *Weaknesses:* Surveyed from SE perspective only — misses agent-system design patterns
- *Open questions:* How do agent architectures differ in effectiveness across SE tasks?

---

### W4 — Large Language Model based Multi-Agents: A Survey of Progress and Challenges

| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2024massurvey |
| **Authors** | Taicheng Guo, Xiuying Chen, Yaqi Wang, Ruidi Chang, Shichao Pei, N. Chawla, Olaf Wiest, Xiangliang Zhang |
| **Year** | 2024 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | **761** |
| **DOI** | 10.48550/arxiv.2402.01680 |
| **Sources** | ◆ YOURS |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: covers agent profiling, communication methods, skill development in LLM-MA systems; discusses complex problem-solving and world simulation; maintains open-source paper repository. 761 citations makes this the third most-cited paper in the pool.*

---

### W5 — A Comprehensive Survey on Benchmarks and Solutions in Software Engineering of LLM-Empowered Agentic System

| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2025benchmarks |
| **Authors** | J. Guo, S. Huang, M. Li, D. Huang, X. Chen, R. Zhang, Z. Guo, H. Yu, S. Yiu, C. Jensen, P. Lio, K. Lam |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2510.09721 |
| **Citations** | < 10 |
| **DOI** | arXiv:2510.09721 |
| **Sources** | ① PDF1 |

**Main Contribution**
The first holistic analysis connecting 150+ papers on LLM-powered SE, mapping relationships between benchmarks and solution approaches. Proposes a two-dimensional taxonomy: solution paradigms × benchmark tasks.

**Methods Used**
- Systematic literature review of 150+ papers (2023–2025)
- Taxonomy: 3 solution paradigms (prompt-based, fine-tuning-based, agent-based) × multiple benchmark task types
- Unified pipeline from task specification to deliverable
- Maps 50+ benchmarks to corresponding solution strategies

**Results / Findings**
- Field has evolved from simple prompt engineering → sophisticated agentic systems with planning, reasoning, memory, and tool augmentation
- Agent-based systems dominate recent leaderboards (SWE-bench, HumanEval, MBPP)
- Multi-agent collaboration, self-evolving systems, and formal verification are key open challenges

**Limitations**
- Survey scope limited to papers published through Oct 2025
- Taxonomy may oversimplify boundaries between paradigms

**How It Relates to the Review**
Excellent for the Discussion/Gaps section — provides authoritative coverage of what benchmarks exist and where agent-based methods stand.

**Critical Analysis**
- *Problem solved:* No systematic understanding of how benchmarks and solution paradigms relate in LLM-based SE
- *Key assumptions:* The three solution paradigms are mutually distinct and exhaustive
- *Comparison to others:* More benchmark-focused than He et al. (W2); broader than SWE-bench Pro
- *Strengths:* Largest literature scope (150+ papers), covers both solutions and evaluations
- *Weaknesses:* Very recent — limited citations; broad scope sacrifices depth per paper
- *Open questions:* Which benchmark best predicts real-world agent performance?

---

### W6 — From LLMs to LLM-Based Agents for Software Engineering: A Survey of Current, Challenges and Future

| Field | Details |
|-------|---------|
| **BibTeX key** | Jin2024llmtoagents |
| **Authors** | H. Jin, L. Huang, H. Cai, J. Yan, B. Li, H. Chen |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2408.02479 |
| **Citations** | ~80 |
| **DOI** | arXiv:2408.02479 |
| **Sources** | ① PDF1 |

**Main Contribution**
Uniquely addresses the *distinction* between using LLMs directly vs. using LLM-based agents in SE contexts. Reviews six SE domains: requirement engineering, code generation, autonomous decision-making, software design, test generation, and software maintenance.

**Methods Used**
- Comparative literature analysis
- Taxonomy distinguishing LLM applications from agent applications across 6 SE domains
- Analysis of benchmarks and evaluation metrics per domain

**Results / Findings**
- LLM-based agents overcome standalone LLM limitations: lack of autonomy, inability to self-improve, and no persistent context
- No unified standards or benchmarking frameworks exist for LLM-based agents in SE
- Test generation and software maintenance are under-researched compared to code generation

**Limitations**
- Lack of unified standards and benchmarking (a gap it identifies but cannot solve)
- Early-stage development means findings may date quickly

**How It Relates to the Review**
Valuable for justifying *why* multi-agent approaches are studied separately from plain LLMs. Use for the background/foundations section.

**Critical Analysis**
- *Problem solved:* Conceptual confusion between LLMs and LLM-agents in the SE literature
- *Key assumptions:* The LLM vs. agent distinction is practically meaningful (debated in the field)
- *Comparison to others:* More conceptually precise than Liu et al. (W3); less comprehensive in paper count
- *Strengths:* Clear taxonomy, covers full SDLC, addresses benchmarking gaps
- *Weaknesses:* No empirical validation of the LLM vs. agent performance gap
- *Open questions:* When do agents genuinely outperform standalone LLMs, and by how much?

---

### W7 — Agentic Software Issue Resolution with Large Language Models: A Survey

| Field | Details |
|-------|---------|
| **BibTeX key** | Jiang2025agenticsolutions |
| **Authors** | Z. Jiang, D. Lo, Z. Liu |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2512.22256 |
| **Citations** | — |
| **DOI** | arXiv:2512.22256 |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: focused survey on agentic approaches to GitHub issue/bug resolution; co-authored by David Lo (also co-author of He2025); narrower scope than general SE surveys.*

---

### W8 — Large Language Models for Software Engineering: Survey and Open Problems

| Field | Details |
|-------|---------|
| **BibTeX key** | Fan2023llmsse |
| **Authors** | A. Fan, B. Gokkaya, M. Harman, M. Lyubarskiy, S. Sengupta, S. Yoo, J. Zhang |
| **Year** | 2023 |
| **Venue** | IEEE/ACM ICSE-FoSE 2023, pp. 31–53 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: pre-agent-era survey establishing baseline LLM capability in SE (code generation, repair, testing); PDF1 uses it to anchor the historical transition from single-LLM to agentic approaches.*

---

### W9 — A Survey on Large Language Models for Software Engineering

| Field | Details |
|-------|---------|
| **BibTeX key** | Zhang2023llmsurvey |
| **Authors** | Q. Zhang, C. Fang, Y. Xie, Y. Zhang, Y. Yang, W. Sun, S. Yu, Z. Chen |
| **Year** | 2023 |
| **Venue** | arXiv preprint arXiv:2312.15223 |
| **Citations** | — |
| **DOI** | arXiv:2312.15223 |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: broad LLM-for-SE survey (not agent-focused); cited by PDF1 alongside Fan2023 to establish pre-agent baseline.*

---

### W10 — Methods and Techniques of Agentic Software Engineering: A Systematic Literature Review

| Field | Details |
|-------|---------|
| **BibTeX key** | Otoum2026systematicreview |
| **Authors** | N. Otoum, N. Elkhalili |
| **Year** | 2026 |
| **Venue** | IEEE Access, Vol. 14, pp. 7443–7465 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: IEEE Access peer-reviewed SLR; reports multi-agent studies rising from 15% to 42% of SE corpus (2022–2024); identifies trust/transparency as adoption barriers in 78% of industry studies; strong empirical framing for field-growth narrative.*

---

## Section 2: Frameworks & Systems (14 papers)

---

### F1 — MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework

| Field | Details |
|-------|---------|
| **BibTeX key** | Hong2023metagpt |
| **Authors** | Sirui Hong, Mingchen Zhuge, Jiaqi Chen, et al., Jürgen Schmidhuber |
| **Year** | 2023 (published ICLR 2024) |
| **Venue** | ICLR 2024 |
| **Citations** | **~1,475** |
| **DOI** | 10.48550/arxiv.2308.00352 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 |

**Main Contribution**
Introduces Standardized Operating Procedures (SOPs) as a meta-programming mechanism for LLM-based multi-agent systems, encoding human workflow patterns into agent prompt sequences to reduce hallucinations and improve task coherence.

**Methods Used**
- Assembly-line paradigm with diverse specialized roles (product manager, architect, engineer, QA)
- SOP encoding into prompt sequences
- Intermediate result verification to minimize cascading errors
- Structured outputs (documents, diagrams) rather than conversational exchanges

**Results / Findings**
- 85.9% and 87.7% Pass@1 on code generation benchmarks (HumanEval, MBPP)
- 100% task completion rate on collaborative software engineering benchmarks
- Generates more coherent solutions than chat-based multi-agent systems

**Limitations**
- SOP design is manual — requires human effort to encode workflows
- Limited to structured software development tasks; unclear generalization to open-ended problems
- Does not address runtime errors in deployed software

**How It Relates to the Review**
One of the two most-cited multi-agent SE frameworks (alongside ChatDev). Essential citation for the "current approaches" section. Contrasts with ChatDev's dialogue-based approach.

**Critical Analysis**
- *Problem solved:* Logic inconsistencies and cascading hallucinations in complex multi-agent collaboration
- *Key assumptions:* Human workflow patterns (SOPs) can be encoded effectively into LLM prompts
- *Comparison to others:* Uses structured docs vs. ChatDev's natural dialogue; more deterministic but less flexible
- *Strengths:* ICLR peer-reviewed; strong benchmark results; reproducible due to open-source release
- *Weaknesses:* SOP encoding is a bottleneck; limited to predefined workflows
- *Open questions:* Can SOPs be learned or generated automatically? How does MetaGPT handle novel task types?

---

### F2 — ChatDev: Communicative Agents for Software Development

| Field | Details |
|-------|---------|
| **BibTeX key** | Qian2023chatdev |
| **Authors** | Cheng Qian, Wei Liu, Hongzhang Liu, Nuo Chen, Yufan Dang, et al., Maosong Sun |
| **Year** | 2023 (accepted ACL 2024) |
| **Venue** | ACL 2024 |
| **Citations** | **603** |
| **DOI** | 10.18653/v1/2024.acl-long.810 |
| **Sources** | ◆ YOURS · ① PDF1 |

**Main Contribution**
Introduces a chat-powered software development framework where specialized LLM-driven agents collaborate via natural language dialogue through all development phases (design, coding, testing). Introduces the "Chat Chain" structure and "Communicative Dehallucination" technique.

**Methods Used**
- Multi-agent system with role-specialized agents
- "Chat chain" guiding communication content and order across phases
- "Communicative dehallucination" — controlling agent communication style to reduce hallucinations
- Multi-turn natural language dialogue for code generation and debugging

**Results / Findings**
- Raises code quality score from 0.1523 (MetaGPT) to 0.3953 through cooperative communication
- Natural language communication benefits system design phase; programming language aids debugging
- Demonstrates unified language-based development pipeline is feasible

**Limitations**
- Natural language communication can be verbose and ambiguous
- Performance degrades on complex, large-scale projects
- Limited ability to incorporate external tools or APIs

**How It Relates to the Review**
Foundational framework paper — pair with MetaGPT to illustrate the two dominant communication paradigms (dialogue vs. structured documents).

**Critical Analysis**
- *Problem solved:* Fragmentation of software development pipeline across specialized models
- *Key assumptions:* Natural language is a sufficient medium for all inter-agent coordination
- *Comparison to others:* Higher quality scores than MetaGPT but less structured; both outperform single-LLM baselines
- *Strengths:* ACL peer-reviewed; open-source; demonstrates end-to-end pipeline; good empirical results
- *Weaknesses:* Verbosity of dialogue; scalability to large codebases unproven
- *Open questions:* What is the optimal mix of natural language vs. structured communication in multi-agent SE?

---

### F3 — AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation

| Field | Details |
|-------|---------|
| **BibTeX key** | Wu2023autogen |
| **Authors** | Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, Beibin Li, Erkang Zhu, et al., Chi Wang |
| **Year** | 2023 |
| **Venue** | arXiv:2308.08155; Microsoft Research |
| **Citations** | **851** |
| **DOI** | arXiv:2308.08155 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 |

**Main Contribution**
Open-source framework enabling developers to build LLM applications through customizable multi-agent conversations. Agents can operate in combinations of LLMs, human inputs, and tools. The most widely adopted multi-agent framework in practice.

**Methods Used**
- Multi-agent conversation architecture with customizable, conversable agents
- Flexible mode combinations: LLM-only, LLM + tools, LLM + human, fully automated
- Support for both natural language and code-based agent interactions

**Results / Findings**
- Validated across diverse domains: mathematics, coding, Q&A, operations research, online decision-making, entertainment
- Enables complex pipelines that no single LLM can handle
- Human-in-the-loop integration without special training

**Limitations**
- Framework generality means fewer SE-specific optimizations compared to ChatDev/MetaGPT
- Agent conversation management can lead to infinite loops without careful design
- No native benchmarking against SE-specific tasks in this paper

**How It Relates to the Review**
AutoGen is the most cited multi-agent framework and is used as the backbone in many subsequent systems. Essential citation for the "frameworks" section.

**Critical Analysis**
- *Problem solved:* Need for a generic, reusable infrastructure for multi-agent LLM applications
- *Key assumptions:* Conversational paradigm is general enough for all agent interaction patterns
- *Comparison to others:* More general-purpose than MetaGPT or ChatDev; better for developers building custom systems
- *Strengths:* Open-source, widely adopted, flexible, human-in-the-loop support
- *Weaknesses:* No SE-specific benchmarks; loop/convergence issues in complex tasks
- *Open questions:* How does AutoGen compare to MetaGPT/ChatDev on standardized SE benchmarks?

---

### F4 — AgentCoder: Multi-Agent-based Code Generation with Iterative Testing and Optimisation

| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2023agentcoder |
| **Authors** | Dong Huang, Jie M. Zhang, Michael Luck, Qingwen Bu, Yuhao Qing, Heming Cui |
| **Year** | 2023 |
| **Venue** | arXiv (cs.CL) |
| **Citations** | **312** |
| **DOI** | 10.48550/arxiv.2312.13010 |
| **Sources** | ◆ YOURS |

**Main Contribution**
Introduces a three-agent iterative framework for code generation: a programmer agent, a test designer agent, and a test executor agent. The system iterates until tests pass, combining generation with automated verification.

**Methods Used**
- Three specialized agents in a feedback loop:
  1. Programmer agent: generates and refines code
  2. Test designer agent: creates test cases
  3. Test executor agent: runs tests, provides feedback to programmer
- Iterative refinement until test pass threshold is reached

**Results / Findings**
- GPT-4 + AgentCoder: 96.3% Pass@1 on HumanEval, 91.8% Pass@1 on MBPP
- Prior SOTA: 90.2% / 78.9% Pass@1 — significant improvements
- Token overhead: 56.9K / 66.3K vs. 138.2K / 206.5K for prior SOTA — 2.5–3× more efficient

**Limitations**
- Evaluated only on standard code generation benchmarks — not real-world SE tasks
- Does not address multi-file or project-level code generation
- Test designer may generate insufficient test coverage for complex logic

**How It Relates to the Review**
Good example of applying multi-agent collaboration to a specific SE task (code generation). Demonstrates feedback loops between agents.

**Critical Analysis**
- *Problem solved:* Single-agent code generation lacks self-verification and iterative improvement
- *Key assumptions:* Test-execution feedback is sufficient signal for code quality improvement
- *Comparison to others:* Better benchmark scores than MetaGPT/ChatDev on code tasks; more efficient than prior SOTA
- *Strengths:* Strong quantitative results; efficient token usage; clear iterative mechanism
- *Weaknesses:* Limited to function-level benchmarks; no real-world SE evaluation
- *Open questions:* Does the three-agent feedback loop generalize to repository-level code generation?

---

### F5 — Agentless: Demystifying LLM-based Software Engineering Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Xia2025demystify |
| **Authors** | Chunqiu Steven Xia*, Yinlin Deng*, Soren Dunn, Lingming Zhang (* equal contribution) |
| **Year** | 2024 (arXiv) / 2025 (PACMSE journal) |
| **Venue** | Proc. ACM Softw. Eng. (PACMSE/FSE 2025) |
| **Citations** | ~400 (arXiv) / ~80 (journal) |
| **DOI** | 10.1145/3715754 |
| **Sources** | ◆ YOURS · ① PDF1 |

> **Note:** The arXiv preprint (arXiv:2407.01489) and the PACMSE journal version are the same work. The journal version adds SWE-bench Verified results, extended ablation studies, and comparison against 26 baselines. Summaries below cover the full journal version.

**Main Contribution**
Agentless challenges the assumption that more agent complexity = better performance. Decomposes GitHub issue resolution into three sequential non-agentic phases: (1) Localization, (2) Repair, (3) Patch Validation. By removing autonomous decision-making and tool use, achieves state-of-the-art results at dramatically lower cost with full reproducibility.

**Methods Used**
- Hierarchical localization: tree-structure file embedding → suspicious files → classes/functions → edit locations
- Patch sampling: generates multiple candidates; filters uncompilable; ranks by test-passing and majority voting
- Benchmarks: SWE-bench Lite (300 issues), SWE-bench Verified (500 issues)
- Models tested: GPT-4o (primary), Claude 3.5 Sonnet (best results)
- Comparison baseline: 26 agent-based systems

**Results / Findings**
| Benchmark | Model | Resolve Rate |
|-----------|-------|-------------|
| SWE-bench Lite | GPT-4o | 32.00% |
| SWE-bench Verified | GPT-4o | 38.80% |
| SWE-bench Verified | Claude 3.5 Sonnet | **50.80%** |
- Upper bound analysis: even selecting the best patch from all candidates, only 42% of issues are resolvable — reveals localization failures, not agent design, as the real ceiling
- Adopted by OpenAI and DeepSeek as standard SWE-bench evaluation approach

**Limitations**
- Fixed pipeline cannot adapt to unexpected mid-task situations
- Single-file patch assumption may miss cross-file bugs
- Agentless design trades flexibility for reproducibility

**How It Relates to the Review**
The critical counterpoint to MetaGPT/ChatDev/AutoGen. Essential for the "complexity vs. simplicity" debate.

**Critical Analysis**
- *Problem solved:* Questions whether complex autonomous agents are actually needed for SE tasks
- *Key assumptions:* SE problems can be decomposed into fixed localization + repair steps
- *Comparison to others:* Outperforms ChatDev, MetaGPT, AutoGen-based systems on SWE-bench with simpler approach
- *Strengths:* Rigorous empirical methodology; reproducible pipeline; upper-bound analysis reframes field's evaluation discourse; adopted by major LLM labs
- *Weaknesses:* Fixed pipeline limits flexibility; may not scale to harder long-horizon tasks
- *Open questions:* What task characteristics make agents necessary vs. optional?

---

### F6 — Self-Organized Agents: A LLM Multi-Agent Framework toward Ultra Large-Scale Code Generation and Optimization (SoA)

| Field | Details |
|-------|---------|
| **BibTeX key** | Ishibashi2024soa |
| **Authors** | Y. Ishibashi, Y. Nishimura |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2404.02183 |
| **Citations** | — |
| **DOI** | arXiv:2404.02183 |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: functional decomposition via self-proliferating agent tree (Mother → Child agents); achieves 71.4% Pass@1 on HumanEval (+5% over single-agent); addresses scalability as a structural context-window problem; each agent handles fewer tokens yet combined output is substantially larger.*

---

### F7 — Knowledge-Based Multi-Agent Framework for Automated Software Architecture Design (MAAD)

| Field | Details |
|-------|---------|
| **BibTeX key** | Zhang2025maad |
| **Authors** | Y. Zhang, R. Li, P. Liang, W. Sun, Y. Liu |
| **Year** | 2025 |
| **Venue** | Proceedings of FSE 2025 (ACM), pp. 530–534 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: targets upstream design phase (SRS → architectural artifacts) via RAG from open-source projects and domain experts; addresses hallucination risk of zero-shot architecture design; four agents transform Software Requirements Specification into verified architectural artifacts.*

---

### F8 — An LLM-Based Multi-Agent Framework for Agile Effort Estimation (SEEAgent)

| Field | Details |
|-------|---------|
| **BibTeX key** | Bui2025seeagent |
| **Authors** | T. L. Bui, H. K. Dam, R. Hoda |
| **Year** | 2025 |
| **Venue** | IEEE/ACM ASE 2025, pp. 1032–1043 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: multi-round Planning Poker protocol for agile story-point estimation; role-specialized agents iteratively estimate, justify, and revise alongside human developers until consensus; fine-tuned variant outperforms deep learning baselines on 3/4 benchmarks; human study (n=12) showed positive practitioner perceptions.*

---

### F9 — A Self-Reflective Multi-Agent Collaboration Framework for Dynamic Software Engineering Tasks (Eco-Evolve)

| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2026ecoevolve |
| **Authors** | Y. Huang |
| **Year** | 2026 |
| **Venue** | — (technical report) |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: three mechanisms — dynamic topology generator, System 2 Reflection with Critic Agent, error-driven self-evolution via Hindsight Experience Replay; 62.3% on SWE-bench Verified, 73.5% on DevBench (outperforms MetaGPT by 26.6% and 14.7%); ablation identifies memory bank as largest contributor — cross-task experiential learning is the most underexplored MASE capability.*

---

### F10 — Agyn: A Multi-Agent System for Team-Based Autonomous Software Engineering

| Field | Details |
|-------|---------|
| **BibTeX key** | Benkovich2026agyn |
| **Authors** | N. Benkovich, V. Valkov |
| **Year** | 2026 |
| **Venue** | arXiv preprint arXiv:2602.01465 |
| **Citations** | — |
| **DOI** | arXiv:2602.01465 |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: production-deployed GitHub-native workflow; Manager/Researcher/Engineer/Reviewer roles; 72.2% task resolution on SWE-bench 500 without benchmark-specific tuning; exposes failure modes (overengineering, infrastructure-induced trajectory divergence) that benchmark-optimized systems avoid.*

---

### F11 — ALMAS: An Autonomous LLM-Based Multi-Agent Software Engineering Framework

| Field | Details |
|-------|---------|
| **BibTeX key** | Tawosi2025almas |
| **Authors** | Vali Tawosi, Keshav Ramani, Salwa Alamir, Xiaomo Liu |
| **Year** | 2025 |
| **Venue** | MAS-GAIN Workshop at ASE 2025 (ASEW), pp. 287–290 |
| **Citations** | < 5 |
| **DOI** | arXiv:2510.03463 |
| **Sources** | ② PDF2 |

**Main Contribution**
A vision framework for autonomous multi-agent LLM systems that models the full software development lifecycle, aligning agents to agile development roles (product manager, sprint planner, developer, tester, reviewer). Designed for seamless integration with human developers and existing dev environments.

**Methods Used**
- Multi-agent architecture aligned with agile team roles
- Modular design for integration with existing development environments
- Framework structured around SDLC stages with agent handoffs
- Key innovations: Meta-RAG (natural-language codebase summaries), tiered agent pool routing routine tasks to lightweight models

**Results / Findings**
- Demonstrated capability to generate an application and add a new feature in a use case scenario
- Shows practical viability within agile development workflows
- Framework represents a "progress towards ALMAS" rather than a complete implementation

**Limitations**
- Vision/early-stage paper — not a full implementation
- Limited empirical evaluation; only proof-of-concept demonstrated
- Unclear how it handles conflicts between agent recommendations

**How It Relates to the Review**
Good example of applying multi-agent systems to the full SDLC with agile methodologies.

**Critical Analysis**
- *Problem solved:* LLM automation remains task-isolated rather than covering the full agile SDLC
- *Key assumptions:* Agile role specialization maps naturally to agent role specialization
- *Strengths:* Agile-aligned design; modular architecture; human integration considered; Meta-RAG addresses context-window limits
- *Weaknesses:* Workshop paper; limited validation; vision-stage only
- *Open questions:* How does ALMAS handle backlog prioritization and sprint planning autonomously?

---

### F12 — Software Development Using a Multi-Agent Approach

| Field | Details |
|-------|---------|
| **BibTeX key** | Ribeiro2025multiagent |
| **Authors** | J. G. Ribeiro, J. M. Pires, J. O. Pereira, F. A. Durão, C. G. Ralha |
| **Year** | 2025 |
| **Venue** | WESAAC 2025 (Workshop), pp. 93–100. SBC. |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: human-in-the-loop 5-agent MAS with Redis Pub/Sub + MongoDB persistent knowledge base; prototype generated Python Flask backend with JWT/CRUD; workshop venue, limited scope.*

---

### F13 — Multi-Agent Collaboration: Harnessing the Power of Intelligent LLM Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Talebirad2023collaboration |
| **Authors** | Yashar Talebirad, Amirhossein Nadiri |
| **Year** | 2023 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | 282 |
| **DOI** | arXiv:2306.03314 |
| **Sources** | ◆ YOURS |

**Main Contribution**
One of the earliest frameworks for enabling LLMs to work through multiple intelligent agent components with distinctive roles. Introduces the concept of agent collaboration through case studies including Auto-GPT, BabyAGI, and the Gorilla model.

**Methods Used**
- Multi-agent system architecture with role-based collaboration
- Case studies: Auto-GPT, BabyAGI, Gorilla model (with API integration)
- Domain modeling: courtroom simulations, software development scenarios

**Results / Findings**
- Agent collaboration demonstrably improves performance on complex, multi-step tasks
- Identifies key challenges: looping issues, security risks, scalability, evaluation, ethics
- Framework shows practical versatility across domains

**Limitations**
- Published Jun 2023 — predates most modern frameworks (MetaGPT, ChatDev, AutoGen)
- Identifies but does not solve challenges: looping, security, scalability
- No quantitative benchmarks

**How It Relates to the Review**
Historical/foundational paper that helps establish the chronological narrative in the background section. Shows the field was already recognizing key challenges in mid-2023.

**Critical Analysis**
- *Problem solved:* Standalone LLM performance limitations on complex multi-step problems
- *Key assumptions:* Role differentiation between agents is key to improved performance
- *Comparison to others:* Earlier and more conceptual than MetaGPT, ChatDev, AutoGen; identified challenges still unsolved today
- *Strengths:* Early identification of still-relevant challenges; good for historical context
- *Weaknesses:* No quantitative results; predates modern frameworks
- *Open questions:* The challenges it identified (looping, security, scalability) remain unsolved as of 2025

---

### F14 — Designing LLM-based Multi-Agent Systems for SE Tasks: Quality Attributes, Design Patterns and Rationale

| Field | Details |
|-------|---------|
| **BibTeX key** | Cai2025designpatterns |
| **Authors** | Yangxiao Cai, Ruiyin Li, Peng Liang, Mojtaba Shahin, Zengyang Li |
| **Year** | 2025 |
| **Venue** | Under journal review (arXiv:2511.08475) |
| **Citations** | < 20 |
| **DOI** | arXiv:2511.08475 |
| **Sources** | ◆ YOURS |

**Main Contribution**
Systematic exploration of *how* LLM-based multi-agent systems are designed for SE, identifying quality attributes, 16 design patterns, and design rationales. Particularly practical for anyone building or evaluating such systems.

**Methods Used**
- Systematic literature review of 94 papers on LLM-based MAS for SE
- Pattern extraction and categorization methodology
- Quality attribute analysis (ISO 25010 framework)

**Results / Findings**
- Code generation is the most common SE task addressed by LLM-based MAS
- Functional Suitability is the most-prioritized quality attribute by designers
- Role-Based Cooperation is the most frequently used design pattern (out of 16 identified)
- Improving code quality is the primary design motivation

**Limitations**
- Limited to published systems — many industrial systems are proprietary
- Design patterns extracted from papers may not reflect optimal production designs

**How It Relates to the Review**
Directly relevant to the "current approaches/methods" section. Provides a structured vocabulary for comparing systems like MetaGPT, ChatDev, AutoGen in terms of design patterns.

**Critical Analysis**
- *Problem solved:* No systematic research on design principles for LLM-based MAS in SE
- *Key assumptions:* Patterns extracted from papers represent reusable design knowledge
- *Comparison to others:* Complements He et al. (W2) — where He covers *what* is built, this covers *how* to design it
- *Strengths:* Practical design guidance, rigorous pattern extraction, strong SE engineering focus
- *Weaknesses:* Under review — not yet peer-validated; 94-paper scope smaller than Papers W1–W5
- *Open questions:* How do these 16 patterns perform comparatively in controlled experiments?

---

## Section 3: Benchmarks & Evaluation (5 papers)

---

### B1 — SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

| Field | Details |
|-------|---------|
| **BibTeX key** | Jimenez2024swebench |
| **Authors** | C. Jimenez, J. Yang, A. Wettig, S. Yao, K. Pei, O. Press, K. Narasimhan |
| **Year** | 2024 |
| **Venue** | ICLR 2024 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: the de facto evaluation benchmark for agentic SE systems; criticized for data contamination and limited scope; ICLR peer-reviewed; cited by both PDF1 and PDF2 (in text).*

---

### B2 — BigCodeBench: Benchmarking Code Generation with Diverse Function Calls and Complex Instructions

| Field | Details |
|-------|---------|
| **BibTeX key** | Zhuo2024bigcodebench |
| **Authors** | T. Y. Zhuo, M. C. Vu, J. Chim, H. Hu, et al. |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2406.15877 |
| **Citations** | — |
| **DOI** | arXiv:2406.15877 |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: richer benchmark than HumanEval — tests diverse function calls and complex multi-step instructions; cited by PDF1 in benchmarks/evaluation section.*

---

### B3 — Survey on Evaluation of LLM-based Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Yehudai2025evalsurvey |
| **Authors** | Asaf Yehudai, Lilach Eden, Alan Li, Guy Uziel, Yilun Zhao, Roy Bar-Haim, Arman Cohan, Michal Shmueli-Scheuer |
| **Year** | 2025 |
| **Venue** | ACL Findings 2025 |
| **Citations** | 67 |
| **DOI** | arXiv:2503.16416 |
| **Sources** | ◆ YOURS |

**Main Contribution**
First comprehensive survey analyzing evaluation methodologies for LLM-based agents across 5 dimensions: core LLM capabilities (planning, tool use), application-specific benchmarks, generalist agent evaluation, benchmark dimensions, and evaluation frameworks.

**Methods Used**
- Systematic literature review focused specifically on evaluation methodology
- Five-dimensional analysis framework
- Identification of evaluation gaps and trends

**Results / Findings**
- Clear trend toward more realistic, challenging evaluations with continuously updated benchmarks
- Critical gaps in assessing cost-efficiency, safety, robustness of agents
- Lack of standardized evaluation approaches is a major bottleneck for the field

**Limitations**
- Does not provide new evaluation methods — descriptive survey only
- Rapidly changing landscape means findings may date quickly

**How It Relates to the Review**
Important for the Discussion/Gaps section — establishes that evaluation of multi-agent systems remains an open problem.

**Critical Analysis**
- *Problem solved:* No systematic understanding of how LLM-based agents should be evaluated
- *Key assumptions:* Evaluation methodology is a distinct research concern from system design
- *Comparison to others:* Unique focus on evaluation vs. system design; complements all other surveys
- *Strengths:* Published at ACL (peer-reviewed); highly timely; clear gap identification
- *Weaknesses:* Descriptive only; does not propose new evaluation standards
- *Open questions:* How to create evaluations that resist gaming/benchmark overfitting?

---

### B4 — Software Testing with Large Language Models: Survey, Landscape, and Vision

| Field | Details |
|-------|---------|
| **BibTeX key** | Wang2023testing |
| **Authors** | J. Wang, Y. Huang, C. Chen, Z. Liu, S. Wang, Q. Wang |
| **Year** | 2023 |
| **Venue** | IEEE Transactions on Software Engineering, Vol. 50, pp. 911–936 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: IEEE TSE peer-reviewed; establishes pre-agent-era LLM testing baseline; different paper from Wang2023autonomousagents; cited by PDF1 for historical context.*

---

### B5 — Tokenomics: Quantifying Where Tokens Are Used in Agentic Software Engineering

| Field | Details |
|-------|---------|
| **BibTeX key** | Salim2026tokenomics |
| **Authors** | M. Salim, J. Latendresse, S. Khatoonabadi, E. Shihab |
| **Year** | 2026 |
| **Venue** | arXiv preprint arXiv:2601.14470 |
| **Citations** | — |
| **DOI** | arXiv:2601.14470 |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: token-level cost analysis of agentic SE systems — finds iterative review dominates compute costs; provides quantitative grounding for coordination overhead arguments.*

---

## Section 4: Challenges, Gaps & Vision (5 papers)

---

### C1 — LLM Multi-Agent Systems: Challenges and Open Problems

| Field | Details |
|-------|---------|
| **BibTeX key** | Han2024challenges |
| **Authors** | Shanshan Han, Qifan Zhang, Yuhang Yao, Weizhao Jin, Zhaozhuo Xu, Chaoyang He |
| **Year** | 2024 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | 124 |
| **DOI** | 10.48550/arxiv.2402.03578 |
| **Sources** | ◆ YOURS |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: identifies four critical challenge dimensions — (1) task allocation optimization, (2) robust reasoning through iterative debate, (3) managing complex layered context, (4) enhancing memory management; 124 citations; strong for a challenges paper; pairs with Hassan2025 to show challenges → proposed solutions arc.*

---

### C2 — LLM-Based Agentic Systems for Software Engineering: Challenges and Opportunities

| Field | Details |
|-------|---------|
| **BibTeX key** | Tang2025challenges |
| **Authors** | Y. Tang, T. Runkler |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2601.09822 |
| **Citations** | — |
| **DOI** | arXiv:2601.09822 |
| **Sources** | ① PDF1 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: argues better orchestration strategies — not more agents — may be the path forward; complements Xia2025 (Agentless) in the complexity-vs-simplicity debate; failure modes of complex MAS are poorly understood.*

---

### C3 — Agentic Software Engineering: Foundational Pillars and a Research Roadmap

| Field | Details |
|-------|---------|
| **BibTeX key** | Hassan2025agenticroadmap |
| **Authors** | Ahmed E. Hassan, Hao Li, Dayi Lin, Bram Adams, Tse-Hsun Chen, Yutaro Kashiwa, Dong Qiu |
| **Year** | 2025 |
| **Venue** | arXiv (cs.SE) arXiv:2509.06216 |
| **Citations** | ~40 |
| **DOI** | arXiv:2509.06216 |
| **Sources** | ◆ YOURS |

**Main Contribution**
Introduces Structured Agentic Software Engineering (SASE) — a conceptual framework reimagining SE around autonomous agents working with humans. Proposes two symbiotic modalities: "SE for Humans" and "SE for Agents," requiring fundamental rethinking of SE's core pillars (actors, processes, tools, artifacts).

**Methods Used**
- Conceptual framework development (vision paper, not empirical)
- Two-environment design:
  - Agent Command Environment (ACE): humans orchestrate agent teams
  - Agent Execution Environment (AEE): agents execute with human callback capabilities

**Results / Findings**
- Identifies that current agentic SE is focused narrowly on code — needs to expand to full socio-technical SE activities
- Calls for new vocabulary and concepts for the community to discuss human-agent SE partnerships
- Highlights need for evidence-based empirical research on agentic SE effectiveness

**Limitations**
- Explicitly a conceptual scaffold — no empirical results
- Authors state: "Our goal is not to offer a definitive solution"
- Framework may not survive contact with industrial realities

**How It Relates to the Review**
Excellent for the Conclusion and Future Directions sections — frames where the field is heading.

**Critical Analysis**
- *Problem solved:* No community vocabulary or framework for discussing the transition to agent-assisted SE
- *Key assumptions:* Agents will eventually take on full engineering roles, not just code generation
- *Comparison to others:* More forward-looking than all other papers; less empirical than benchmarks/frameworks
- *Strengths:* Well-respected authors (Ahmed Hassan is a leading SE researcher); clear conceptual framing
- *Weaknesses:* No empirical support; purely conceptual
- *Open questions:* What governance, accountability, and trust models are needed for agentic SE in production?

---

### C4 — The Agents Journey: Twenty-Five Years of Multi-agent Systems

| Field | Details |
|-------|---------|
| **BibTeX key** | Mascardi2026agentsjourney |
| **Authors** | V. Mascardi, A. Omicini (Eds.) |
| **Year** | 2026 |
| **Venue** | Springer Nature (edited book) |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: edited volume tracing MAS from BDI/JADE era (2000) to LLM era; argues current agentic AI recapitulates prior ideas via natural language reasoning; PDF2 uses it to call for more deliberate inheritance of formal coordination theory and verification methods; provides historical grounding for MASE lineage.*

---

### C5 — Evaluating Software Process Models for Multi-Agent Class-Level Code Generation

| Field | Details |
|-------|---------|
| **BibTeX key** | Shafin2025processmodels |
| **Authors** | W. I. Shafin, M. N. Rafi, Z. Li, T. H. Chen |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2511.09794 |
| **Citations** | — |
| **DOI** | arXiv:2511.09794 |
| **Sources** | ② PDF2 |

> **Summary pending — not yet in paper_summaries.md**  
> *To populate: first systematic ablation study of multi-agent workflows at class level; ClassEval benchmark, 3 LLM backends; Waterfall collaboration reduces functional correctness by up to 39.8% while improving code quality metrics; Testing stage has strongest influence; same workflow constrains GPT-4o-mini but benefits Claude-3.5-Haiku by 9.5% — process design cannot be decoupled from model selection.*

---

## Master Reference Index

| # | BibTeX Key | Authors (short) | Year | Venue | Citations | Sources | Summary |
|---|-----------|-----------------|------|-------|-----------|---------|---------|
| 1 | Wang2023autonomousagents | Wang et al. | 2023 | Frontiers CS | **2,011** | ◆ | ✅ |
| 2 | He2025literaturereview | He, Treude, Lo | 2025 | TOSEM (Q1) | 144 | ◆ ① ② | ✅ |
| 3 | Liu2024agentssurvey | Liu et al. | 2024 | TOSEM (Q1) | 151 | ◆ ① | ✅ |
| 4 | Guo2024massurvey | Guo et al. | 2024 | arXiv:2402.01680 | **761** | ◆ | ⬜ pending |
| 5 | Guo2025benchmarks | Guo et al. | 2025 | arXiv:2510.09721 | < 10 | ① | ✅ |
| 6 | Jin2024llmtoagents | Jin et al. | 2024 | arXiv:2408.02479 | ~80 | ① | ✅ |
| 7 | Jiang2025agenticsolutions | Jiang et al. | 2025 | arXiv:2512.22256 | — | ① | ⬜ pending |
| 8 | Fan2023llmsse | Fan et al. | 2023 | ICSE-FoSE | — | ① | ⬜ pending |
| 9 | Zhang2023llmsurvey | Zhang et al. | 2023 | arXiv:2312.15223 | — | ① | ⬜ pending |
| 10 | Otoum2026systematicreview | Otoum & Elkhalili | 2026 | IEEE Access | — | ② | ⬜ pending |
| 11 | Hong2023metagpt | Hong et al. | 2023 | ICLR 2024 | **1,475** | ◆ ① ② | ✅ |
| 12 | Qian2023chatdev | Qian et al. | 2023 | ACL 2024 | 603 | ◆ ① | ✅ |
| 13 | Wu2023autogen | Wu et al. | 2023 | arXiv | 851 | ◆ ① ② | ✅ |
| 14 | Huang2023agentcoder | Huang et al. | 2023 | arXiv | 312 | ◆ | ✅ |
| 15 | Xia2025demystify | Xia et al. | 2024/2025 | PACMSE/FSE | ~400 | ◆ ① | ✅ |
| 16 | Ishibashi2024soa | Ishibashi & Nishimura | 2024 | arXiv:2404.02183 | — | ② | ⬜ pending |
| 17 | Zhang2025maad | Zhang et al. | 2025 | FSE 2025 | — | ② | ⬜ pending |
| 18 | Bui2025seeagent | Bui et al. | 2025 | ASE 2025 | — | ② | ⬜ pending |
| 19 | Huang2026ecoevolve | Huang | 2026 | — | — | ② | ⬜ pending |
| 20 | Benkovich2026agyn | Benkovich & Valkov | 2026 | arXiv:2602.01465 | — | ② | ⬜ pending |
| 21 | Tawosi2025almas | Tawosi et al. | 2025 | ASEW 2025 | < 5 | ② | ✅ |
| 22 | Ribeiro2025multiagent | Ribeiro et al. | 2025 | WESAAC 2025 | — | ② | ⬜ pending |
| 23 | Talebirad2023collaboration | Talebirad & Nadiri | 2023 | arXiv | 282 | ◆ | ✅ |
| 24 | Cai2025designpatterns | Cai et al. | 2025 | arXiv:2511.08475 | < 20 | ◆ | ✅ |
| 25 | Jimenez2024swebench | Jimenez et al. | 2024 | ICLR 2024 | — | ① | ⬜ pending |
| 26 | Zhuo2024bigcodebench | Zhuo et al. | 2024 | arXiv:2406.15877 | — | ① | ⬜ pending |
| 27 | Yehudai2025evalsurvey | Yehudai et al. | 2025 | ACL Findings | 67 | ◆ | ✅ |
| 28 | Wang2023testing | Wang et al. | 2023 | IEEE TSE | — | ① | ⬜ pending |
| 29 | Salim2026tokenomics | Salim et al. | 2026 | arXiv:2601.14470 | — | ① | ⬜ pending |
| 30 | Han2024challenges | Han et al. | 2024 | arXiv | 124 | ◆ | ⬜ pending |
| 31 | Tang2025challenges | Tang & Runkler | 2025 | arXiv:2601.09822 | — | ① | ⬜ pending |
| 32 | Hassan2025agenticroadmap | Hassan et al. | 2025 | arXiv:2509.06216 | ~40 | ◆ | ✅ |
| 33 | Mascardi2026agentsjourney | Mascardi & Omicini | 2026 | Springer (book) | — | ② | ⬜ pending |
| 34 | Shafin2025processmodels | Shafin et al. | 2025 | arXiv:2511.09794 | — | ② | ⬜ pending |

**Summary coverage: 15 / 34 populated · 19 pending (from classmates' reviews — not in paper_summaries.md)**

---

*Generated: 2026-05-16 | Sources: filtered_papers.md (14 confirmed papers) + 54154F3E PDF (14 refs) + Literature_Review_MultiAgentSE PDF (12 refs) | Summaries sourced from paper_summaries.md*
