# Combined Paper Pool — Multi-Agent LLM Software Engineering
## Three-Way Merge: Your filtered_papers.md + Classmate 1 (PDF1) + Classmate 2 / S. Fang (PDF2)

**Date:** 2026-05-16  
**Total unique papers:** 34  
**Summaries populated:** 34 / 34 (all complete)

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

**Main Contribution**
A comprehensive survey of LLM-based multi-agent systems addressing three core questions: what domains/environments do multi-agents simulate, how are agents profiled and how do they communicate, and what mechanisms grow agent capacities. Presented at IJCAI 2024; third most-cited paper in this pool at 761 citations. Maintains an open-source paper repository tracking the field.

**Methods Used**
- Literature survey and taxonomy of LLM multi-agent systems
- Agent profiling analysis: role assignment, persona design, background setting
- Communication mechanism classification: inter-agent messaging, shared memory, blackboard systems
- Capacity-growth mechanism analysis: fine-tuning on interaction traces, reflection/critique loops, retrieval-augmented memory

**Results / Findings**
- LLM-based multi-agent systems substantially outperform single-agent approaches on complex, multi-step problem-solving
- World simulation (social, scientific, gaming environments) is a promising but under-explored application domain
- Three primary capacity-growth pathways: fine-tuning on interaction traces, reflection/critique loops, and retrieval-augmented memory
- Agent profiling (assigning explicit roles/personas) is essential for coordination quality

**Limitations**
- Broad scope limits per-topic depth
- Benchmarks for multi-agent systems remain fragmented and non-standardized
- Focuses on capability, not safety or trustworthiness of multi-agent interactions

**How It Relates to the Review**
Cite alongside Wang et al. (W1) in the foundational background section, specifically for the taxonomy of multi-agent communication patterns and capacity-growth mechanisms.

**Critical Analysis**
- *Problem solved:* Lack of unified understanding of LLM-based multi-agent system design across domains
- *Key assumptions:* Agent profiling and communication protocols are primary determinants of system performance
- *Comparison to others:* Broader domain coverage than He et al. (W2); less SE-specific than Liu et al. (W3)
- *Strengths:* High citations (761), IJCAI venue, open-source paper repository
- *Weaknesses:* Limited treatment of evaluation/benchmarking; predates 2024–2025 advances
- *Open questions:* How do different communication topologies (star, mesh, hierarchical) affect SE task performance?

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

**Main Contribution**
A systematic survey of 126 recent studies on LLM-based agentic software issue resolution, covering bug fixing, efficiency optimization, and repository-maintenance tasks. Establishes a three-dimensional taxonomy (benchmarks, techniques, empirical studies) and highlights the emergence of agentic reinforcement learning as a paradigm shift in agent design. Co-authored by David Lo (also on He2025), giving the survey strong community credibility.

**Methods Used**
- Systematic survey of 126 papers (2023–2025)
- Three-dimensional taxonomy: benchmarks × techniques × empirical studies
- Analysis of agentic RL as a distinct training paradigm separate from prompt-based agentic systems
- General workflow characterization: issue localization → patch generation → validation

**Results / Findings**
- Real-world issue resolution requires long-horizon reasoning, iterative exploration, and feedback-driven decision-making — beyond single-step LLM approaches
- Agentic RL (training agents with reward signals from test execution) represents a qualitative leap over prompt-only agentic systems
- Key open challenges: generalization to unseen repositories, handling ambiguous issue descriptions, cost efficiency of iterative exploration

**Limitations**
- Narrowly scoped to issue resolution — does not cover other SDLC stages
- Rapidly evolving area: findings may date quickly given the 2024–2025 publication window
- Not yet peer-reviewed (arXiv preprint)

**How It Relates to the Review**
Complements He et al. (W2) for the maintenance/bug-fix subsection. Pair with SWE-bench (B1) to frame the evaluation context for agentic issue resolution systems.

**Critical Analysis**
- *Problem solved:* No focused survey existed on agentic issue resolution despite it being the dominant SWE-bench task type
- *Key assumptions:* Agentic RL will become the dominant training paradigm for issue resolution agents
- *Comparison to others:* Narrower than He et al. (W2) but deeper on issue resolution; strongest complement to the Agentless (F5) debate
- *Strengths:* 126-paper scope, strong author team, timely coverage of agentic RL trend
- *Weaknesses:* arXiv only; issue resolution is a subset of SE activities
- *Open questions:* Can agentic RL systems trained on public repos generalize to proprietary codebases?

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

**Main Contribution**
A foundational survey of LLM applications across the full SE spectrum published at ICSE-FoSE 2023: coding, design, requirements, repair, refactoring, performance, documentation, and analytics. Authored by researchers from Meta AI, UCL, and Microsoft Research. Establishes the pre-agent baseline and argues that hybrid techniques (traditional SE + LLMs) are essential for reliability due to hallucination risks from LLMs' emergent properties.

**Methods Used**
- Survey and taxonomy of LLM capabilities across SE activities
- Analysis of emergent LLM properties (creativity, cross-domain reasoning) and their double-edged implications
- Open problem identification for each SE activity
- Argument for hybrid traditional SE + LLM approaches to ensure correctness

**Results / Findings**
- LLMs' emergent properties enable novel SE applications across the full spectrum, from code generation to analytics
- Those same properties (hallucination, non-determinism) pose significant reliability challenges in production
- Hybrid techniques combining traditional SE methods with LLMs are necessary for reliable deployments
- Open problems: test oracle generation, reliable repair, formal specification synthesis

**Limitations**
- Published 2023 — predates agentic frameworks entirely; no multi-agent coverage
- Benchmark landscape discussed is limited compared to 2024–2025 developments
- Does not address agent-specific challenges (coordination, planning, memory)

**How It Relates to the Review**
The historical anchor paper for the background section — establishes what LLMs could do alone before multi-agent orchestration was introduced. PDF1 uses it precisely for this anchor role.

**Critical Analysis**
- *Problem solved:* No comprehensive map existed of LLM capabilities and limitations across all SE activities
- *Key assumptions:* Emergent LLM properties are simultaneously the key opportunity and the key risk
- *Comparison to others:* Chronologically earliest LLM-for-SE survey in this pool; broader in SE activity coverage than Zhang2023 (W9)
- *Strengths:* ICSE peer-reviewed (top venue); strong industry author team; full SE spectrum coverage
- *Weaknesses:* Entirely pre-agentic; hallucination mitigations proposed are now superseded by agentic approaches
- *Open questions:* Which traditional SE verification techniques best complement LLM weaknesses in production deployments?

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

**Main Contribution**
A systematic survey of LLMs for SE covering 62 LLMs of Code across three model architectures, 15 pre-training objectives, and 16 downstream SE tasks. Analyzes 947 studies across 112 specific code-related tasks spanning five SE workflow phases. Later published in Science China Information Sciences. Cited alongside Fan2023 (W8) to establish the pre-agent LLM-for-SE baseline.

**Methods Used**
- Systematic survey and categorization of 947 studies
- Three-axis taxonomy: LLM architectures × pre-training objectives × downstream SE tasks
- Five-phase SE workflow analysis: requirements → design → implementation → testing → maintenance
- Analysis of 112 specific code-related subtasks

**Results / Findings**
- 62 distinct LLMs for code exist with substantial variation in architecture and training objectives
- Code generation and code completion are the most studied downstream tasks (disproportionate vs. other phases)
- Requirements engineering and software maintenance are significantly under-studied relative to their practical importance
- Pre-training objective design (e.g., masked language modeling vs. causal modeling) substantially affects downstream SE task performance

**Limitations**
- Not agent-focused — treats LLMs as standalone tools, not as components of multi-agent systems
- Rapidly outdated given the pace of new LLM releases
- 947-study scope makes depth per study very limited

**How It Relates to the Review**
Cite alongside Fan2023 (W8) in the historical background to quantify the scale of pre-agent LLM-for-SE research (947 studies) and motivate the shift toward agentic approaches.

**Critical Analysis**
- *Problem solved:* Fragmented landscape of LLM-for-SE research with no unified taxonomy
- *Key assumptions:* Pre-training objectives and architecture are the primary determinants of downstream SE task performance
- *Comparison to others:* Larger study corpus than Fan2023 (W8); less task-specific than Jin2024 (W6); fully pre-agentic
- *Strengths:* Massive scope (947 studies, 112 tasks); published in peer-reviewed journal; comprehensive taxonomy
- *Weaknesses:* No multi-agent coverage; quickly outdated; study breadth precludes per-task depth
- *Open questions:* How does the pre-training/fine-tuning paradigm translate to agent training for SE tasks?

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

**Main Contribution**
A peer-reviewed systematic literature review (SLR) in IEEE Access analyzing 61 high-quality studies on agentic software engineering methods and techniques (2022–2025). Reports the empirical growth of multi-agent studies from 15% to 42% of the SE corpus over this period and identifies critical knowledge gaps blocking industrial adoption.

**Methods Used**
- Systematic literature review methodology with rigorous inclusion/exclusion criteria
- Analysis of 61 high-quality studies from 2022–2025
- Gap analysis across six dimensions: evaluation, coordination, code maintenance, human-agent collaboration, standards, and empirical evidence

**Results / Findings**
- Multi-agent studies rose from 15% to 42% of the SE corpus between 2022 and 2024 — confirming rapid field growth
- Trust and transparency are adoption barriers cited in 78% of industry-oriented studies
- Six major knowledge gaps identified: no standardized evaluation schemes, poorly understood coordination mechanisms, no empirical evidence on long-term code maintenance, no human-agent collaboration guidelines, no unified standards, and limited real-world deployment data

**Limitations**
- IEEE Access is an open-access journal with lower selectivity than top SE venues (TOSEM, FSE, ICSE)
- 61-paper scope is smaller than some arXiv surveys (e.g., Liu2024 with 124 papers)
- Gap analysis may reflect publication biases rather than true research priorities

**How It Relates to the Review**
Strong empirical grounding for the field-growth narrative and the challenges/gaps section. The 15% → 42% growth statistic is a compelling data point for motivation. Cite alongside Han2024 (C1) for the challenges discussion.

**Critical Analysis**
- *Problem solved:* Lack of empirical evidence on the growth trajectory and adoption barriers of agentic SE
- *Key assumptions:* The 2022–2024 publication window is representative of the field's maturation
- *Comparison to others:* More empirically grounded than He et al. (W2) on field growth; less comprehensive on framework-level analysis
- *Strengths:* IEEE peer-reviewed; quantitative growth data; specific gap identification; covers trust/transparency which other surveys overlook
- *Weaknesses:* IEEE Access venue; smaller study corpus; findings on industry adoption may not generalize
- *Open questions:* What specific transparency mechanisms would address the trust barrier in 78% of industry studies?

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

**Main Contribution**
Introduces the Self-Organized multi-Agent (SoA) framework to overcome single-agent context-length limitations in large-scale code generation. A Mother agent dynamically spawns specialized Child agents that each implement smaller code components independently, then collaboratively assemble the full codebase. Addresses scalability as a structural context-window problem, not a model capacity problem.

**Methods Used**
- Self-proliferating agent tree: Mother agent decomposes task and spawns Child agents per sub-component
- Each Child agent operates with a smaller, focused context window
- Independent code generation per agent with collaborative integration phase
- Evaluation on HumanEval benchmark against single-agent baselines

**Results / Findings**
- 71.4% Pass@1 on HumanEval — approximately +5% over comparable single-agent baselines
- Combined output code volume is substantially larger than any single agent could produce within context limits
- Self-organization (dynamic spawning) outperforms static multi-agent decomposition because it adapts to task complexity
- Each agent handles fewer tokens, reducing per-agent error rates while enabling larger aggregate outputs

**Limitations**
- Evaluated only on HumanEval (function-level) — not validated on repository-level or real-world SE tasks
- Mother agent decomposition quality is a bottleneck: poor decomposition leads to integration failures
- No comparison against SWE-bench or repository-level benchmarks
- Agent spawning overhead not fully characterized

**How It Relates to the Review**
Strong example of scalability-focused architectural innovation in multi-agent SE. Directly addresses the context-window limitation that motivates multi-agent design. Pair with AgentCoder (F4) to show iterative feedback vs. hierarchical decomposition strategies.

**Critical Analysis**
- *Problem solved:* Context-window constraints that prevent single agents from generating large-scale code
- *Key assumptions:* Functional decomposition is both feasible and sufficient for large-scale code generation
- *Comparison to others:* Addresses scalability structurally (more agents) vs. Agentless (F5) which addresses it procedurally (simpler pipeline)
- *Strengths:* Novel self-proliferating architecture; clear scalability argument; measurable benchmark improvement
- *Weaknesses:* HumanEval is a limited benchmark; no repository-level validation; decomposition quality not addressed
- *Open questions:* How does SoA perform on multi-file, repository-level tasks like SWE-bench?

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

**Main Contribution**
MAAD (Knowledge-based Multi-Agent Architecture Design) is a vision framework targeting the upstream software architecture design phase — one of the least automated stages of the SDLC. Four LLM agents simulate human roles in the traditional architecture design process (requirements analyst, architect, reviewer, verifier), empowered by knowledge retrieved from three sources: existing system designs, authoritative literature, and architecture experts. Presented at FSE 2025 (ACM SIGSOFT Companion).

**Methods Used**
- Four-agent pipeline: SRS intake → architectural style selection → component design → verification
- Knowledge retrieval from three sources: open-source project architectures (RAG), architecture literature (RAG), and expert-curated knowledge bases
- Knowledge-augmented generation to reduce hallucination risk in zero-shot architecture decisions
- Evaluation by architecture experts on generated architectural artifacts

**Results / Findings**
- MAAD can automatically transform a Software Requirements Specification (SRS) into verified architectural artifacts (component diagrams, deployment views, architectural rationale)
- RAG from existing system designs substantially reduces hallucinations compared to zero-shot generation
- Framework demonstrates feasibility of automating architecture design, previously considered too expert-dependent for automation

**Limitations**
- Vision/framework paper at a companion workshop venue — limited empirical evaluation
- Knowledge retrieval quality is bounded by the completeness of the three source databases
- Does not address dynamic architectural evolution as requirements change

**How It Relates to the Review**
Represents the frontier of agentic SE reaching into upstream design activities beyond code generation. Pair with ALMAS (F11) to show the field's ambition for full-SDLC automation.

**Critical Analysis**
- *Problem solved:* Architecture design automation is largely unexplored despite it being a high-leverage SE activity
- *Key assumptions:* Software architecture design can be decomposed into retrieval + generation steps amenable to LLM agents
- *Comparison to others:* More upstream than MetaGPT/ChatDev (which start from requirements and skip to code); complements ALMAS (F11)
- *Strengths:* Addresses a genuine gap; FSE companion venue; knowledge-augmentation is a principled approach to hallucination reduction
- *Weaknesses:* Workshop/companion paper; limited empirical evaluation; expert knowledge base construction is expensive
- *Open questions:* Can MAAD handle architecturally significant requirements changes mid-project, or is it limited to greenfield design?

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

**Main Contribution**
SEEAgent proposes a novel LLM-based multi-agent framework for agile effort estimation, addressing a gap where existing ML methods produce estimates without explanation or developer interaction. Agents model the Planning Poker protocol: they estimate story points, justify their reasoning, and iteratively revise estimates through discussion with human developers and other agents until consensus is reached. Accepted at ASE 2025.

**Methods Used**
- Multi-agent system modeling the Planning Poker agile estimation protocol
- Role-specialized agents: estimator agents with different perspectives + coordinator agent
- Iterative estimate-justify-revise cycles until consensus (mimicking human planning poker rounds)
- Fine-tuned LLM variant for improved domain accuracy
- Human study: n=12 agile practitioners evaluating system usability and accuracy
- Evaluation on 4 story-point estimation benchmarks

**Results / Findings**
- Fine-tuned SEEAgent variant outperforms deep learning baselines on 3 out of 4 benchmarks
- Human study (n=12) showed positive practitioner perceptions of both estimate quality and interaction quality
- LLM agents can provide justifications for estimates, addressing the explainability gap in prior ML approaches
- Iterative consensus-building produces more stable estimates than single-shot approaches

**Limitations**
- Human study limited to 12 practitioners — small sample size
- Benchmarks are existing story-point datasets; real-time sprint planning evaluation is not conducted
- Consensus mechanism may be slower than needed in fast-paced sprint planning sessions

**How It Relates to the Review**
Unique application paper showing multi-agent LLM systems moving into requirements/planning activities beyond code generation. Demonstrates human-in-the-loop multi-agent collaboration for an SE task with no prior automation. Good complement to MAAD (F7) for upstream SE coverage.

**Critical Analysis**
- *Problem solved:* Agile effort estimation is inaccurate and ML methods lack explainability and interaction capability
- *Key assumptions:* Planning Poker's consensus-building structure maps naturally to multi-agent iterative dialogue
- *Comparison to others:* Only paper in this pool targeting effort estimation specifically; unique human-in-the-loop design
- *Strengths:* ASE peer-reviewed; novel domain; human study validation; fine-tuned variant with strong benchmark results
- *Weaknesses:* Small human study; narrow task scope; real-time usability untested
- *Open questions:* How does SEEAgent perform when requirement descriptions are ambiguous or incomplete?

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

**Main Contribution**
Eco-Evolve introduces a self-reflective multi-agent collaboration framework for dynamic SE tasks, combining three synergistic innovations: (1) dynamic topology generation — models the multi-agent system as an adaptive graph where roles and communication channels instantiate based on task requirements; (2) System 2 Reflection with a Critic Agent — inspired by dual-process cognitive theory for deeper reasoning; (3) error-driven self-evolution via Hindsight Experience Replay (HER) — enables agents to learn from failed attempts and optimize prompts through experiential memory. Preprint (Preprints.org, March 2026).

**Methods Used**
- Dynamic graph-based agent topology: agent roles and edges computed from task description at runtime
- Dual-process Reflection module: fast System 1 execution + slow System 2 Critic Agent review
- Hindsight Experience Replay: stores failure trajectories with corrective annotations in a memory bank; uses them to refine future prompts
- Evaluation on SWE-bench Verified and DevBench
- Ablation study isolating contribution of each of the three mechanisms

**Results / Findings**
- 62.3% on SWE-bench Verified and 73.5% on DevBench — outperforms MetaGPT by 26.6% and 14.7% respectively
- Ablation study identifies the memory bank (HER-based self-evolution) as the largest single contributor to performance
- Cross-task experiential learning — the ability to apply lessons from past tasks to new ones — is the most underexplored capability in the MASE field

**Limitations**
- Preprint only — not yet peer-reviewed
- Memory bank grows unboundedly without a retrieval/pruning strategy
- Dynamic topology generation adds latency overhead not quantified in the paper

**How It Relates to the Review**
Highest-performing framework on SWE-bench Verified among those in this pool (62.3%). The HER-based memory finding directly informs the "open challenges" section: cross-task experiential learning is a research gap.

**Critical Analysis**
- *Problem solved:* Static agent topologies and lack of cross-task learning limit MASE system adaptability
- *Key assumptions:* Dynamic topology + reflection + experiential memory are complementary and independently beneficial
- *Comparison to others:* Outperforms MetaGPT (F1) and Agyn (F10) on DevBench; competitive with Agyn on SWE-bench Verified
- *Strengths:* State-of-the-art results; rigorous ablation; novel HER application to multi-agent SE
- *Weaknesses:* Preprint only; memory bank scalability unaddressed; dynamic topology overhead unclear
- *Open questions:* How does memory bank performance degrade over time as the bank grows, and how should pruning be designed?

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

**Main Contribution**
Agyn presents a fully automated multi-agent system that models software engineering as an organizational process, directly replicating the structure of an engineering team. Built on the open-source agyn platform, it assigns specialized agents to four roles: coordination (Manager), research (Researcher), implementation (Engineer), and review (Reviewer), each operating in isolated sandboxes for safe experimentation. Achieves 72.2% task resolution on SWE-bench Verified 500 without benchmark-specific tuning — a strong generalist result.

**Methods Used**
- Four-role agent team: Manager (orchestration), Researcher (codebase exploration), Engineer (implementation), Reviewer (code review)
- Isolated sandboxes per agent for independent experimentation without cross-contamination
- GitHub-native workflow: directly operates on repositories, branches, and pull requests
- Evaluation: SWE-bench Verified 500 task split without benchmark-specific fine-tuning

**Results / Findings**
- 72.2% task resolution on SWE-bench Verified 500 — competitive with Eco-Evolve (F9) and significantly above Agentless baselines
- Exposes failure modes invisible in benchmark-optimized systems: overengineering (over-complex solutions to simple bugs) and infrastructure-induced trajectory divergence (agent behavior changes based on non-code environment state)
- Production deployment surfaces real-world failure modes not captured by SWE-bench task distribution

**Limitations**
- arXiv preprint — not yet peer-reviewed
- Failure mode analysis is qualitative; no systematic frequency data on overengineering or divergence
- GitHub-native design limits applicability to non-GitHub codebases

**How It Relates to the Review**
One of the highest-performing systems on SWE-bench in this pool. More important: its production-deployment perspective surfaces failure modes that pure benchmark papers miss — critical for the challenges/gaps section.

**Critical Analysis**
- *Problem solved:* Existing multi-agent SE systems are optimized for benchmarks but not deployed in real software engineering workflows
- *Key assumptions:* Organizational role structure (Manager/Researcher/Engineer/Reviewer) is optimal for SE agent collaboration
- *Comparison to others:* Higher resolution rate than Agentless (F5); similar to Eco-Evolve (F9); unlike both, validated in production-adjacent workflow
- *Strengths:* Production-deployed; strong benchmark score without benchmark-specific tuning; exposes real failure modes
- *Weaknesses:* Preprint; qualitative failure mode analysis; GitHub-only design
- *Open questions:* How do overengineering and trajectory divergence failures scale with task complexity?

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

**Main Contribution**
A prototype multi-agent system (MAS) for software development featuring five specialized LLM-driven agents coordinated via a Redis Pub/Sub message broker with a MongoDB persistent knowledge base. Demonstrates human-in-the-loop oversight where human experts intervene at decision points. Validated by generating a Python Flask backend application with JWT authentication and CRUD operations. Published at WESAAC 2025 (Brazilian agent systems workshop).

**Methods Used**
- Five specialized agents: architectural planner, artifact generator, code reviewer, operational manager, and integration agent
- Redis Pub/Sub for asynchronous inter-agent communication
- MongoDB for persistent shared knowledge base (maintains context across agent interactions)
- Human-in-the-loop: experts intervene for accuracy and strategic alignment at defined checkpoints
- Prototype validation: generated Flask backend with JWT + CRUD

**Results / Findings**
- LLMs can meaningfully automate software development tasks within a multi-agent architecture
- Persistent knowledge base (MongoDB) enables cross-agent context retention, reducing redundant reasoning
- Human intervention points improve output quality and strategic alignment compared to fully autonomous execution
- Prototype successfully generated a functional Flask backend — proof-of-concept validation

**Limitations**
- Workshop paper (8 pages) — limited evaluation scope and depth
- Validated only on a single prototype use case (Flask backend)
- Scalability to larger systems or more complex requirements not evaluated
- No quantitative benchmarks against other frameworks

**How It Relates to the Review**
Illustrates the human-in-the-loop architectural pattern with concrete infrastructure choices (Redis, MongoDB). Good citation for the agent communication infrastructure subsection and human oversight discussion.

**Critical Analysis**
- *Problem solved:* Need for practical multi-agent SE systems with reliable inter-agent communication and human oversight
- *Key assumptions:* Redis Pub/Sub and MongoDB are sufficient infrastructure for multi-agent SE coordination
- *Comparison to others:* More infrastructure-detailed than MetaGPT/ChatDev; simpler in scale; human oversight is more explicit than Agyn (F10)
- *Strengths:* Concrete infrastructure design; human-in-the-loop model; working prototype
- *Weaknesses:* Workshop venue; single prototype; no quantitative comparison
- *Open questions:* How does the Redis/MongoDB architecture scale to enterprise-grade SE tasks with concurrent agents?

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

**Main Contribution**
SWE-bench is the de facto evaluation benchmark for agentic software engineering systems. Introduces 2,294 real SE problems drawn from GitHub issues and corresponding pull requests across 12 popular Python repositories. Given a codebase and an issue description, a model must edit the codebase to resolve the issue — testing end-to-end repository-level SE capability. Accepted as an ICLR 2024 oral.

**Methods Used**
- Benchmark construction from real GitHub issues + pull requests across 12 Python repositories
- 2,294 task instances with verified ground-truth patches and automated test suites
- Evaluation metric: percentage of issues fully resolved (tests pass after model edits)
- Subsequent variants: SWE-bench Lite (300 curated tasks), SWE-bench Verified (500 human-validated tasks)

**Results / Findings**
- Initial evaluation showed frontier LLMs (Claude 2, GPT-4) resolved fewer than 5% of issues unassisted — motivating the agentic SE research wave
- SWE-bench rapidly became the standard benchmark: nearly every framework in this pool (MetaGPT, ChatDev, Agentless, Eco-Evolve, Agyn) reports SWE-bench results
- Data contamination concerns led to SWE-bench Verified variant with human-validated tasks
- Upper-bound analysis (Agentless, F5) shows localization failures — not agent design — are the primary performance ceiling

**Limitations**
- Limited to Python repositories — unclear generalizability to other languages
- Data contamination risk: training data may include the issues or patches
- Task distribution biased toward bug-fixing; feature requests and refactoring under-represented
- Does not capture code review, deployment, or maintenance phases of SE

**How It Relates to the Review**
The central evaluation benchmark for this entire literature review. Every framework comparison in the paper should reference SWE-bench results. Essential citation in the benchmarks section.

**Critical Analysis**
- *Problem solved:* No realistic, challenging benchmark existed for evaluating end-to-end SE capability in LLMs
- *Key assumptions:* GitHub issue resolution is a representative proxy for real-world SE capability
- *Comparison to others:* More realistic than HumanEval/MBPP (function-level); less comprehensive than BigCodeBench (B2) in task diversity
- *Strengths:* ICLR oral; real-world tasks; automated evaluation; community-standard status
- *Weaknesses:* Python-only; contamination risk; task distribution biases; excludes non-coding SE activities
- *Open questions:* How should future benchmarks address contamination, language diversity, and the full SDLC?

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

**Main Contribution**
BigCodeBench advances code generation benchmarking beyond HumanEval/MBPP by requiring models to invoke multiple function calls as tools from 139 libraries across 7 domains in 1,140 fine-grained tasks. Each task requires compositional reasoning over complex instructions and multi-library API usage. Accepted at ICLR 2025. Includes a natural-language variant (BigCodeBench-Instruct) with minimal essential-only instructions.

**Methods Used**
- 1,140 tasks requiring multi-library function calls (139 libraries, 7 domains: data analysis, web, OS, databases, ML, etc.)
- Average 5.6 test cases per task with 99% branch coverage
- BigCodeBench-Instruct: auto-transforms docstrings into short natural-language instructions
- Evaluation of 60 LLMs on both variants

**Results / Findings**
- Best LLM scores reach only ~60% — significantly below human performance of 97%
- LLMs struggle with following complex multi-step instructions and precise multi-library API usage
- Performance gap between full-docstring and instruction-only (BigCodeBench-Instruct) variants reveals LLMs rely heavily on specification detail
- Multi-library compositional tasks expose limitations that single-function benchmarks hide

**Limitations**
- Benchmark is synthetic (curated tasks) — does not reflect real repository-level SE tasks like SWE-bench
- 139 libraries covers a wide but still finite slice of real-world API diversity
- Human performance (97%) measured on a subset; may not represent true ceiling for all tasks

**How It Relates to the Review**
Cite in the benchmarks section as a complement to SWE-bench (B1): where SWE-bench tests repository-level issue resolution, BigCodeBench tests function-level compositional reasoning over diverse APIs. Together they cover different capability dimensions.

**Critical Analysis**
- *Problem solved:* HumanEval and MBPP are too simple to distinguish frontier model capabilities in practical coding scenarios
- *Key assumptions:* Multi-library function call composition is a realistic proxy for real-world programming complexity
- *Comparison to others:* More compositionally complex than HumanEval/MBPP; narrower scope than SWE-bench (B1) (function-level vs. repository-level)
- *Strengths:* ICLR 2025 peer-reviewed; large task set (1,140); high test coverage (99%); evaluates 60 LLMs
- *Weaknesses:* Synthetic benchmark; function-level only; no agentic evaluation — models submit single solutions
- *Open questions:* How do multi-agent code generation systems (AgentCoder, MetaGPT) perform on BigCodeBench vs. single-model baselines?

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

**Main Contribution**
A comprehensive systematic review of 102 studies on the use of LLMs for software testing, published in IEEE Transactions on Software Engineering (Vol. 50, 2024). Covers all major testing activities: unit test generation, test oracle creation, mutation testing, fuzzing, regression testing, and bug detection. Establishes the pre-agent baseline for LLM-based testing and identifies open research challenges. Note: different paper from Wang2023autonomousagents (W1); same first author (Junjie Wang), different team and topic.

**Methods Used**
- Systematic review of 102 studies using LLMs for software testing
- Dual-perspective analysis: software testing perspective (coverage, oracle, types) × LLMs perspective (model types, training, prompting)
- Taxonomy across testing activities
- Open problem identification per testing domain

**Results / Findings**
- LLMs show strong capability for unit test generation but struggle with complex oracle creation and full-system integration testing
- Test generation quality (coverage, correctness) varies widely across LLM architectures
- Combination of LLMs with traditional testing tools (fuzzing engines, symbolic executors) consistently outperforms LLM-only approaches
- Test oracle generation remains the hardest open problem — LLMs frequently generate tests that pass vacuously

**Limitations**
- Published 2023–2024 — predates agentic testing systems (multi-agent test generation, agent-driven fuzzing)
- Focuses on testing as a standalone activity; does not cover multi-agent testing workflows
- 102-study scope is smaller than some broader SE surveys

**How It Relates to the Review**
Historical anchor for the testing subsection: establishes what LLMs could do for testing before multi-agent orchestration. Cite when discussing agentic testing systems (e.g., AgentCoder's test designer agent in F4) to show the baseline they improve upon.

**Critical Analysis**
- *Problem solved:* No comprehensive map existed of LLM capabilities across the diversity of software testing activities
- *Key assumptions:* LLM-for-testing is a coherent research area distinct from LLM-for-code-generation
- *Comparison to others:* Testing-specific complement to Fan2023 (W8) and Zhang2023 (W9); more focused but predates agentic approaches
- *Strengths:* IEEE TSE peer-reviewed (highest-impact SE journal); 102-study scope; dual-perspective analysis
- *Weaknesses:* Predates agentic testing; no coverage of multi-agent test generation; oracle problem identified but unsolved
- *Open questions:* How do multi-agent approaches (e.g., specialized test-designer agents) address the oracle generation problem?

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

**Main Contribution**
Tokenomics provides the first quantitative analysis of token consumption patterns in LLM-based multi-agent systems operating across the SDLC. Rather than measuring end-task performance, it measures where compute resources are actually spent — revealing that the iterative Code Review stage, not initial code generation, dominates cost. Provides empirical grounding for the coordination overhead argument against complex multi-agent systems.

**Methods Used**
- Token consumption profiling of an LLM-MA system across SDLC stages
- Stage-level breakdown: requirements → design → implementation → code review → testing
- Separate analysis of input tokens vs. output tokens per stage
- Empirical measurement across multiple task runs

**Results / Findings**
- Code Review stage accounts for 59.4% of total token consumption on average — more than all other stages combined
- Input tokens constitute 53.9% of consumption on average (vs. output tokens), suggesting inter-agent context passing is a major cost driver
- Primary cost of agentic SE is not code generation but automated refinement and verification
- Provides quantitative evidence that iterative review loops — not agent count — drive compute costs

**Limitations**
- Analyses a single LLM-MA system — generalizability to other frameworks (MetaGPT, ChatDev, Agyn) unclear
- Does not analyze cost vs. quality trade-offs (is the 59.4% review cost justified by quality gains?)
- arXiv preprint — not yet peer-reviewed

**How It Relates to the Review**
Critical empirical complement to the complexity-vs-simplicity debate (Agentless, F5). Use in the Discussion section to quantify why iterative multi-agent review is expensive and to ground future research directions on cost optimization.

**Critical Analysis**
- *Problem solved:* Token/compute costs of agentic SE systems are poorly understood, hindering adoption decisions
- *Key assumptions:* Token count is a reliable proxy for compute cost and resource consumption
- *Comparison to others:* Unique methodological focus on cost profiling vs. performance; directly challenges the implicit assumption that code generation is the expensive step
- *Strengths:* Novel empirical angle; directly actionable findings; strong implications for system design optimization
- *Weaknesses:* Single-system analysis; no quality-vs-cost trade-off analysis; preprint only
- *Open questions:* Can code review token consumption be reduced by 50% without sacrificing output quality, and what architectural changes achieve this?

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

**Main Contribution**
A focused challenges paper identifying four critical open problems in LLM multi-agent systems that remain inadequately addressed: (1) task allocation optimization, (2) robust reasoning through iterative inter-agent debate, (3) managing complex and layered context information, and (4) enhancing memory management for intricate multi-agent interactions. Also explores multi-agent applications in blockchain distributed systems as a future direction. 124 citations makes this the strongest challenges paper in the pool.

**Methods Used**
- Analysis and categorization of open challenges in LLM multi-agent systems
- Literature review of existing approaches and their limitations per challenge dimension
- Exploration of potential applications in blockchain/distributed systems
- Forward-looking research agenda for each challenge

**Results / Findings**
- Task allocation optimization is unsolved: current systems use fixed roles (MetaGPT, ChatDev) rather than dynamic allocation based on agent competency
- Iterative debate between agents improves reasoning robustness but introduces convergence and echo-chamber risks
- Context management in multi-agent systems suffers from both overflow (too much information) and fragmentation (relevant context not shared)
- Memory management for persistent, cross-task agent learning is largely unexplored

**Limitations**
- Challenges paper — identifies problems but does not propose solutions
- Some challenges identified have since been partially addressed (e.g., Eco-Evolve's HER memory, SoA's context management)
- Blockchain application section is speculative and tangential to SE

**How It Relates to the Review**
The primary citation for the "challenges and open problems" section. Pair with Hassan2025 (C3) to show the challenges → proposed solutions arc. The four challenge dimensions provide a natural organizing framework for the discussion section.

**Critical Analysis**
- *Problem solved:* No systematic articulation of the critical unsolved problems in LLM multi-agent systems
- *Key assumptions:* These four challenges are independent dimensions — in practice they interact significantly
- *Comparison to others:* More concise and focused than Tang2025 (C2); less SE-specific than Otoum2026 (W10); stronger citation count than any other challenges paper in this pool
- *Strengths:* 124 citations; clear four-challenge taxonomy; pairs well with solutions papers
- *Weaknesses:* 2024 paper — some challenges partially addressed by 2025–2026 work; blockchain section adds noise
- *Open questions:* How should task allocation dynamically adapt when agent competency degrades mid-task?

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

**Main Contribution**
A concept paper systematically reviewing LLM-based multi-agent systems for SE across the SDLC — from requirements engineering and code generation to static checking, testing, and debugging. Goes beyond cataloging frameworks to argue that better orchestration strategies, not more agents, may be the more productive path forward. Identifies five key research directions: orchestration, human-agent coordination, cost optimization, data collection, and evaluation standardization.

**Methods Used**
- Systematic review of LLM-based multi-agent frameworks and their application across the SDLC
- Analysis of language model selection criteria for SE tasks
- Review of SE evaluation benchmarks and their limitations
- Analysis of agentic framework communication protocols
- Open challenge identification with specific research opportunity framing

**Results / Findings**
- LLM-based MAS are applied across all SDLC stages but coverage is uneven: code generation is heavily studied; requirements and maintenance are under-studied
- Orchestration strategy quality — not agent count — is the primary determinant of system performance
- Human-agent coordination remains ad hoc; no principled design frameworks exist
- Computational cost is a significant barrier to adoption; token consumption is poorly characterized (see Tokenomics, B5)

**Limitations**
- Concept paper — limited empirical validation of its claims
- arXiv preprint (January 2026) — not yet peer-reviewed
- Some claims overlap significantly with He et al. (W2) and Han et al. (C1)

**How It Relates to the Review**
Complements Agentless (F5) in the complexity-vs-simplicity debate and provides the most comprehensive recent framing of SE-specific challenges. Use in the "future directions" subsection alongside Hassan2025 (C3).

**Critical Analysis**
- *Problem solved:* Practitioners lack a structured understanding of when and how to apply LLM-based MAS across the SDLC
- *Key assumptions:* Orchestration is the primary lever for improvement — more controversial than it appears, given that model capability also matters
- *Comparison to others:* More SE-specific than Han et al. (C1); more actionable than Hassan2025 (C3); less empirical than Otoum2026 (W10)
- *Strengths:* Comprehensive SDLC coverage; forward-looking; five concrete research directions
- *Weaknesses:* Preprint only; claims about orchestration primacy lack empirical support; overlaps with prior surveys
- *Open questions:* What formal models of multi-agent orchestration would enable principled system comparison?

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

**Main Contribution**
An edited volume (Springer Lecture Notes in Computer Science, Vol. 16395) tracing multi-agent systems research from the BDI/JADE era (circa 2000) to the current LLM-based agentic AI period. Edited by Viviana Mascardi and Andrea Omicini — leading figures in the formal MAS community. Argues that current agentic AI substantially recapitulates prior MAS ideas (autonomy, coordination, emergent behavior, trust) via natural language reasoning rather than formal specifications. Scheduled for release May 2026.

**Methods Used**
- Edited volume with contributions from multiple MAS researchers
- Historical retrospective spanning 25 years of MAS research
- Thematic chapters covering: trust, self-organization, MAS simulation, formal models, coordination protocols, SE applications, distributed systems
- Forward-looking sections outlining future perspectives from formal MAS theory

**Results / Findings**
- Current LLM-based agentic systems reinvent many concepts from formal MAS theory (BDI agents, FIPA protocols, organizational models) via natural language, often without acknowledging the prior art
- Formal coordination theory and verification methods from classical MAS offer principled solutions to current challenges (trust, coordination, emergent behavior)
- The transition from formal to natural-language agent specifications sacrifices verifiability for accessibility
- PDF2 (S. Fang) uses this volume to argue for more deliberate inheritance of formal coordination theory in LLM-based MASE

**Limitations**
- Edited volume format means uneven depth across chapters
- Formal MAS community perspective may undervalue the pragmatic capabilities enabled by LLM-based approaches
- Not an empirical paper — historical/conceptual framing only

**How It Relates to the Review**
Provides essential historical grounding for the MASE research lineage. Use in the background section to contextualize current LLM-based multi-agent systems within the 25-year history of MAS research. Supports the argument that formal verification and coordination theory from classical MAS should inform future MASE design.

**Critical Analysis**
- *Problem solved:* LLM-based multi-agent systems are being developed without awareness of a rich prior art in formal MAS theory
- *Key assumptions:* Classical MAS theory offers directly applicable insights to LLM-based systems, not just historical interest
- *Comparison to others:* Unique historical scope; only non-arXiv book in this pool; complements all surveys by providing the 25-year context they lack
- *Strengths:* Authoritative editors; Springer LNCS publication; bridges formal MAS and LLM-agent communities
- *Weaknesses:* Edited volume format; no empirical content; 2026 publication limits citation availability now
- *Open questions:* Which specific formal coordination protocols (e.g., FIPA Contract Net) are most directly applicable to LLM-based multi-agent SE workflows?

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

**Main Contribution**
The first systematic ablation study evaluating how software process structure and role specialization affect multi-agent LLM performance on class-level code generation. Simulates a Waterfall-style development cycle (Requirements → Design → Implementation → Testing) using three LLMs (GPT-4o-mini, DeepSeek-Chat, Claude-3.5-Haiku) on 100 Python tasks from ClassEval. Reveals that workflow design and model selection are inseparable: the same process structure can harm one model while benefiting another.

**Methods Used**
- Waterfall-style multi-agent workflow: Requirement agent → Design agent → Implementation agent → Testing agent
- Three LLM backends: GPT-4o-mini, DeepSeek-Chat, Claude-3.5-Haiku
- ClassEval benchmark: 100 class-level Python programming tasks
- Evaluation metrics: functional correctness (test pass rate) and code quality (maintainability, structure)
- Ablation: each SDLC stage removed individually to measure its contribution

**Results / Findings**
- Waterfall collaboration improves code quality but reduces functional correctness significantly: -37.8% for GPT-4o-mini, -39.8% for DeepSeek-Chat
- Claude-3.5-Haiku is a notable exception: +9.5% correctness improvement under Waterfall — showing model architecture interacts with process design
- Testing stage has the strongest individual influence on both quality and correctness outcomes
- Process design cannot be decoupled from model selection — one-size-fits-all workflow design is inadequate

**Limitations**
- ClassEval is a class-level benchmark — not repository-level; findings may not generalize to larger-scale tasks
- Three LLMs tested may not represent the full distribution of model architectures
- Waterfall is one process model; Agile, iterative, and other models not evaluated

**How It Relates to the Review**
Unique empirical contribution showing that workflow design interacts with model selection — a finding that challenges the common assumption in the field that process structures are model-agnostic. Cite in the challenges section alongside C5 and in the design lessons discussion.

**Critical Analysis**
- *Problem solved:* No systematic study existed on how process model choice affects multi-agent LLM SE performance
- *Key assumptions:* Waterfall is a representative structured process model; ClassEval tasks are representative of class-level SE
- *Comparison to others:* Unique ablation methodology; most similar to Cai2025 (F14) in focus on design choices, but more empirical
- *Strengths:* First ablation of its kind; clear findings with practical implications; multiple LLM backends
- *Weaknesses:* Limited to ClassEval (class-level); only one process model; not peer-reviewed at time of submission
- *Open questions:* How do Agile/iterative process models compare to Waterfall across different LLM backends, and at repository scale?

---

## Master Reference Index

| # | BibTeX Key | Authors (short) | Year | Venue | Citations | Sources | Summary |
|---|-----------|-----------------|------|-------|-----------|---------|---------|
| 1 | Wang2023autonomousagents | Wang et al. | 2023 | Frontiers CS | **2,011** | ◆ | ✅ |
| 2 | He2025literaturereview | He, Treude, Lo | 2025 | TOSEM (Q1) | 144 | ◆ ① ② | ✅ |
| 3 | Liu2024agentssurvey | Liu et al. | 2024 | TOSEM (Q1) | 151 | ◆ ① | ✅ |
| 4 | Guo2024massurvey | Guo et al. | 2024 | arXiv:2402.01680 | **761** | ◆ | ✅ |
| 5 | Guo2025benchmarks | Guo et al. | 2025 | arXiv:2510.09721 | < 10 | ① | ✅ |
| 6 | Jin2024llmtoagents | Jin et al. | 2024 | arXiv:2408.02479 | ~80 | ① | ✅ |
| 7 | Jiang2025agenticsolutions | Jiang et al. | 2025 | arXiv:2512.22256 | — | ① | ✅ |
| 8 | Fan2023llmsse | Fan et al. | 2023 | ICSE-FoSE | — | ① | ✅ |
| 9 | Zhang2023llmsurvey | Zhang et al. | 2023 | arXiv:2312.15223 | — | ① | ✅ |
| 10 | Otoum2026systematicreview | Otoum & Elkhalili | 2026 | IEEE Access | — | ② | ✅ |
| 11 | Hong2023metagpt | Hong et al. | 2023 | ICLR 2024 | **1,475** | ◆ ① ② | ✅ |
| 12 | Qian2023chatdev | Qian et al. | 2023 | ACL 2024 | 603 | ◆ ① | ✅ |
| 13 | Wu2023autogen | Wu et al. | 2023 | arXiv | 851 | ◆ ① ② | ✅ |
| 14 | Huang2023agentcoder | Huang et al. | 2023 | arXiv | 312 | ◆ | ✅ |
| 15 | Xia2025demystify | Xia et al. | 2024/2025 | PACMSE/FSE | ~400 | ◆ ① | ✅ |
| 16 | Ishibashi2024soa | Ishibashi & Nishimura | 2024 | arXiv:2404.02183 | — | ② | ✅ |
| 17 | Zhang2025maad | Zhang et al. | 2025 | FSE 2025 | — | ② | ✅ |
| 18 | Bui2025seeagent | Bui et al. | 2025 | ASE 2025 | — | ② | ✅ |
| 19 | Huang2026ecoevolve | Huang | 2026 | — | — | ② | ✅ |
| 20 | Benkovich2026agyn | Benkovich & Valkov | 2026 | arXiv:2602.01465 | — | ② | ✅ |
| 21 | Tawosi2025almas | Tawosi et al. | 2025 | ASEW 2025 | < 5 | ② | ✅ |
| 22 | Ribeiro2025multiagent | Ribeiro et al. | 2025 | WESAAC 2025 | — | ② | ✅ |
| 23 | Talebirad2023collaboration | Talebirad & Nadiri | 2023 | arXiv | 282 | ◆ | ✅ |
| 24 | Cai2025designpatterns | Cai et al. | 2025 | arXiv:2511.08475 | < 20 | ◆ | ✅ |
| 25 | Jimenez2024swebench | Jimenez et al. | 2024 | ICLR 2024 | — | ① | ✅ |
| 26 | Zhuo2024bigcodebench | Zhuo et al. | 2024 | arXiv:2406.15877 | — | ① | ✅ |
| 27 | Yehudai2025evalsurvey | Yehudai et al. | 2025 | ACL Findings | 67 | ◆ | ✅ |
| 28 | Wang2023testing | Wang et al. | 2023 | IEEE TSE | — | ① | ✅ |
| 29 | Salim2026tokenomics | Salim et al. | 2026 | arXiv:2601.14470 | — | ① | ✅ |
| 30 | Han2024challenges | Han et al. | 2024 | arXiv | 124 | ◆ | ✅ |
| 31 | Tang2025challenges | Tang & Runkler | 2025 | arXiv:2601.09822 | — | ① | ✅ |
| 32 | Hassan2025agenticroadmap | Hassan et al. | 2025 | arXiv:2509.06216 | ~40 | ◆ | ✅ |
| 33 | Mascardi2026agentsjourney | Mascardi & Omicini | 2026 | Springer (book) | — | ② | ✅ |
| 34 | Shafin2025processmodels | Shafin et al. | 2025 | arXiv:2511.09794 | — | ② | ✅ |

**Summary coverage: 34 / 34 populated · 0 pending**

---

*Generated: 2026-05-16 | Sources: filtered_papers.md (14 confirmed papers) + 54154F3E PDF (14 refs) + Literature_Review_MultiAgentSE PDF (12 refs) | Summaries sourced from paper_summaries.md*
