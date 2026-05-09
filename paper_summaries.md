# Literature Review — Multi-Agent Software Engineering
## Paper Summaries & Critical Analysis Database
**Scope:** 2023–2026 (foundational pre-2023 work included where seminal)
**Total papers tracked:** 25 | **Fully read:** 25 | **PDF needed:** 0

---

## How to Use This File
- **Filter** using the Theme column to group related papers for your review sections
- **BibTeX keys** follow `AuthorYEARkeyword` format for easy reference management
- Suggested themes for the 2-page review: `[Survey]` `[Framework]` `[Benchmark]` `[Architecture]` `[Vision]` `[Application]`

---

## Quick Reference Table

| # | Title (short) | Authors | Year | Venue | Theme | Status |
|---|--------------|---------|------|-------|-------|--------|
| 1 | LLM-Based MAS for SE: Literature Review | He, Treude, Lo | 2025 | TOSEM | Survey | ✅ Read |
| 2 | LLM-Based Agents for SE: A Survey | Liu et al. | 2024 | TOSEM | Survey | ✅ Read |
| 3 | From LLMs to LLM-based Agents for SE | Jin et al. | 2024 | arXiv/cs.SE | Survey | ✅ Read |
| 4 | Survey on LLM-based MAS: Recent Advances | Chen et al. | 2024 | arXiv/cs.CL | Survey | ✅ Read |
| 5 | Survey on LLM-based Autonomous Agents | Wang et al. | 2023 | Frontiers of CS | Survey | ✅ Read |
| 6 | Survey on Benchmarks & Solutions in SE | Guo et al. | 2025 | arXiv/cs.SE | Survey | ✅ Read |
| 7 | Designing LLM-based MAS for SE Tasks | Cai et al. | 2025 | Under review | Survey/Design | ✅ Read |
| 8 | Survey on Evaluation of LLM-based Agents | Yehudai et al. | 2025 | ACL Findings | Survey | ✅ Read |
| 9 | MetaGPT | Hong et al. | 2023 | ICLR 2024 | Framework | ✅ Read |
| 10 | ChatDev | Qian et al. | 2023 | ACL 2024 | Framework | ✅ Read |
| 11 | AutoGen | Wu et al. | 2023 | arXiv/cs.AI | Framework | ✅ Read |
| 12 | AgentCoder | Huang et al. | 2023 | arXiv/cs.CL | Framework | ✅ Read |
| 13 | Agentless | Xia et al. | 2024 | arXiv/cs.SE | Framework | ✅ Read |
| 14 | ALMAS | Tawosi et al. | 2025 | ASE 2025 Workshop | Framework | ✅ Read |
| 15 | Multi-Agent Collaboration: Harnessing LLMs | Talebirad & Nadiri | 2023 | arXiv/cs.AI | Framework | ✅ Read |
| 16 | SWE-Bench Pro | Deng et al. | 2025 | arXiv/cs.SE | Benchmark | ✅ Read |
| 17 | SALLMA | Becattini et al. | 2025 | ICSE SATrends | Architecture | ✅ Read |
| 18 | Agentic SE: Foundational Pillars | Hassan et al. | 2025 | arXiv/cs.SE | Vision | ✅ Read |
| 19 | Trustworthy Human-Agent Collaboration | Ronanki | 2025 | FSE Companion '25 | Human-AI | ✅ Read |
| 20 | Demystifying LLM-Based SE Agents (ACM) | Xia et al. | 2025 | PACMSE 2025 | Framework | ✅ Read |
| 21 | LLM-augmented MAS for Agile SE | Chudziak & Cinkusz | 2024 | ASE 2024 | Framework | ✅ Read |
| 22 | Multi-Agent LLM for Requirements Analysis | Sami et al. | 2025 | SEAA 2025 | Application | ✅ Read |
| 23 | Agent-Oriented Code Design Issue Localization | Batole et al. | 2025 | ICSE 2025 | Application | ✅ Read |
| 24 | Multi-Agent LLM for Software Design & Refactoring | Rajendran et al. | 2025 | SoutheastCon 2025 | Application | ✅ Read |
| 25 | AI-Powered MAS for Unit Test Generation | Garlapati et al. | 2024 | GCAT 2024 | Application | ✅ Read |

---

---

# SECTION 1: SURVEY PAPERS

---

## Paper 1 — LLM-Based Multi-Agent Systems for SE: Literature Review, Vision, and the Road Ahead

| Field | Details |
|-------|---------|
| **BibTeX key** | He2025literaturereview |
| **Authors** | Junda He, Christoph Treude, David Lo |
| **Year** | 2025 (submitted April 2024, revised July 2025) |
| **Venue** | ACM Transactions on Software Engineering and Methodology (TOSEM) — Special Issue |
| **Theme** | Survey |
| **Source DB** | ACM DL + arXiv |
| **Links** | [ACM](https://dl.acm.org/doi/10.1145/3712003) · [arXiv:2404.04834](https://arxiv.org/abs/2404.04834) |

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

**How It Relates to Your Work**
This is the foundational reference for the entire literature review. Use it to establish scope, cite for the definition of LMA systems, and use its taxonomy as a backbone for your thematic organization.

**Critical Analysis**
- *Problem solved:* Lack of systematic understanding of how multi-agent LLM systems are applied across the full SE lifecycle
- *Key assumptions:* Assumes multi-agent collaboration is inherently superior to single-agent — challenged by Agentless (Paper 13)
- *Comparison to others:* More comprehensive SDLC coverage than Jin et al. (Paper 3); more SE-specific than Wang et al. (Paper 5)
- *Strengths:* Highly rigorous, peer-reviewed, covers entire SDLC, includes vision/roadmap
- *Weaknesses:* Pre-dates key 2025 developments; limited industrial case studies
- *Open questions:* How to ensure trustworthiness at scale? How to measure agent autonomy?

---

## Paper 2 — Large Language Model-Based Agents for Software Engineering: A Survey

| Field | Details |
|-------|---------|
| **BibTeX key** | Liu2024agentssurvey |
| **Authors** | Junwei Liu, Kaixin Wang, Yixuan Chen, Xin Peng, Zhenpeng Chen, Lingming Zhang, Yiling Lou |
| **Year** | 2024 (submitted Sep 2024, revised Dec 2025) |
| **Venue** | ACM Transactions on Software Engineering and Methodology (TOSEM) |
| **Theme** | Survey |
| **Source DB** | ACM DL + arXiv |
| **Links** | [ACM](https://dl.acm.org/doi/10.1145/3712003) · [arXiv:2409.02977](https://arxiv.org/abs/2409.02977) |

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

**How It Relates to Your Work**
The 124-paper scope makes this an excellent citation for breadth. Use it for the background section to establish that this is a rapidly growing field, and for specific agent capability categorizations.

**Critical Analysis**
- *Problem solved:* Fragmented understanding of how LLM agents enhance SE tasks
- *Key assumptions:* Agent-based SE is a meaningful category distinct from LLM-only SE
- *Comparison to others:* Broader paper scope than He et al. (Paper 1); more SE-specific than Chen et al. (Paper 4)
- *Strengths:* Largest paper corpus (124), dual-perspective analysis, TOSEM-quality rigor
- *Weaknesses:* Surveyed from SE perspective only — misses agent-system design patterns
- *Open questions:* How do agent architectures differ in effectiveness across SE tasks?

---

## Paper 3 — From LLMs to LLM-based Agents for Software Engineering: A Survey of Current, Challenges and Future

| Field | Details |
|-------|---------|
| **BibTeX key** | Jin2024llmtoagent |
| **Authors** | Haolin Jin, Linghan Huang, Haipeng Cai, Jun Yan, Bo Li, Huaming Chen |
| **Year** | 2024 (submitted Aug 2024, revised Apr 2025) |
| **Venue** | arXiv (cs.SE) — under review |
| **Theme** | Survey |
| **Source DB** | arXiv + DBLP |
| **Links** | [arXiv:2408.02479](https://arxiv.org/abs/2408.02479) · [DBLP](https://dblp.org/rec/journals/corr/abs-2408-02479.html) |

**Main Contribution**
Uniquely addresses the *distinction* between using LLMs directly vs. using LLM-based agents in SE contexts — a gap missing in other surveys. Reviews six SE domains: requirement engineering, code generation, autonomous decision-making, software design, test generation, and software maintenance.

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

**How It Relates to Your Work**
Valuable for justifying *why* multi-agent approaches are studied separately from plain LLMs. Use for the background/foundations section.

**Critical Analysis**
- *Problem solved:* Conceptual confusion between LLMs and LLM-agents in the SE literature
- *Key assumptions:* The LLM vs. agent distinction is practically meaningful (debated in the field)
- *Comparison to others:* More conceptually precise than Liu et al. (Paper 2); less comprehensive in paper count
- *Strengths:* Clear taxonomy, covers full SDLC, addresses benchmarking gaps
- *Weaknesses:* No empirical validation of the LLM vs. agent performance gap
- *Open questions:* When do agents genuinely outperform standalone LLMs, and by how much?

---

## Paper 4 — A Survey on LLM-based Multi-Agent System: Recent Advances and New Frontiers in Application

| Field | Details |
|-------|---------|
| **BibTeX key** | Chen2024massurvey |
| **Authors** | Shuaihang Chen, Yuanxing Liu, Wei Han, Weinan Zhang, Ting Liu |
| **Year** | 2024 (submitted Dec 2024, revised Jan 2025) |
| **Venue** | arXiv (cs.CL) |
| **Theme** | Survey |
| **Source DB** | arXiv |
| **Links** | [arXiv:2412.17481](https://arxiv.org/abs/2412.17481) |

**Main Contribution**
Broad survey of LLM-based Multi-Agent Systems beyond SE, covering all application domains. Provides a unifying framework across three categories: (i) complex task-solving, (ii) scenario simulation, and (iii) evaluating generative agents.

**Methods Used**
- Systematic survey with three-category taxonomy
- Framework proposing 5 components: profile, perception, self-action, mutual interaction, evolution

**Results / Findings**
- LLM-MAS have extensive applications in both problem-solving and world simulation
- Agent evaluation (category iii) is an emerging and under-explored area
- The field is growing faster than existing reviews can capture comprehensively

**Limitations**
- Rapidly evolving field makes comprehensive coverage difficult
- SE-specific applications are one subset among many covered — less depth than SE-specific surveys

**How It Relates to Your Work**
Useful for placing multi-agent SE in the broader AI/NLP context. Good citation for the introduction to establish that multi-agent LLM systems are a general paradigm, not SE-specific.

**Critical Analysis**
- *Problem solved:* Lack of unified framework covering the full LLM-MAS landscape
- *Key assumptions:* Agent profiles and interaction patterns can be generalized across domains
- *Comparison to others:* Broader scope than He et al. (Paper 1); less SE-specific depth
- *Strengths:* Broad coverage, up-to-date (Dec 2024), strong taxonomic structure
- *Weaknesses:* SE applications treated shallowly; no empirical comparison across application areas
- *Open questions:* Do findings from non-SE domains transfer to SE contexts?

---

## Paper 5 — A Survey on Large Language Model based Autonomous Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Wang2023autonomousagents |
| **Authors** | Lei Wang, Chen Ma, Xueyang Feng, Zeyu Zhang, et al. |
| **Year** | 2023 (submitted Aug 2023; published in Frontiers of Computer Science 2024) |
| **Venue** | Frontiers of Computer Science (DOI: 10.1007/s11704-024-40231-1) |
| **Theme** | Survey (Foundational) |
| **Source DB** | arXiv + Google Scholar |
| **Links** | [arXiv:2308.11432](https://arxiv.org/abs/2308.11432) |

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

**How It Relates to Your Work**
This is a foundational paper establishing the conceptual vocabulary (agent memory, planning, action). Cite in the background/foundations section when defining what an "agent" is.

**Critical Analysis**
- *Problem solved:* No unified framework existed for understanding the range of LLM-based agent applications
- *Key assumptions:* LLM knowledge scales to human-level task performance in diverse domains
- *Comparison to others:* More foundational than He et al. (Paper 1); broader scope than SE-specific surveys
- *Strengths:* Highly cited, clear framework, published in peer-reviewed journal
- *Weaknesses:* Predates the rapid 2024–2025 developments; SE coverage shallow
- *Open questions:* How do agent memory and planning mechanisms scale to enterprise SE tasks?

---

## Paper 6 — A Comprehensive Survey on Benchmarks and Solutions in Software Engineering of LLM-Empowered Agentic Systems

| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2025benchmarksurvey |
| **Authors** | Jiale Guo, Suizhi Huang, Mei Li, Dong Huang, et al. |
| **Year** | 2025 (submitted Oct 2025) |
| **Venue** | arXiv (cs.SE) |
| **Theme** | Survey |
| **Source DB** | arXiv |
| **Links** | [arXiv:2510.09721](https://arxiv.org/html/2510.09721v3) |

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

**How It Relates to Your Work**
Excellent for the Discussion/Gaps section — provides authoritative coverage of what benchmarks exist and where agent-based methods stand. Also useful for identifying which benchmark papers to include.

**Critical Analysis**
- *Problem solved:* No systematic understanding of how benchmarks and solution paradigms relate in LLM-based SE
- *Key assumptions:* The three solution paradigms are mutually distinct and exhaustive
- *Comparison to others:* More benchmark-focused than He et al. (Paper 1); broader than SWE-Bench Pro (Paper 16)
- *Strengths:* Largest literature scope (150+ papers), covers both solutions and evaluations
- *Weaknesses:* Very recent — limited citations from community yet; broad scope sacrifices depth per paper
- *Open questions:* Which benchmark best predicts real-world agent performance?

---

## Paper 7 — Designing LLM-based Multi-Agent Systems for SE Tasks: Quality Attributes, Design Patterns and Rationale

| Field | Details |
|-------|---------|
| **BibTeX key** | Cai2025designpatterns |
| **Authors** | Yangxiao Cai, Ruiyin Li, Peng Liang, Mojtaba Shahin, Zengyang Li |
| **Year** | 2025 (submitted Nov 2025, revised Dec 2025) |
| **Venue** | Under journal review (35-page manuscript) |
| **Theme** | Survey / Design |
| **Source DB** | arXiv |
| **Links** | [arXiv:2511.08475](https://arxiv.org/html/2511.08475v2) |

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

**How It Relates to Your Work**
Directly relevant to the "current approaches/methods" section. Provides a structured vocabulary for comparing systems like MetaGPT, ChatDev, AutoGen in terms of design patterns.

**Critical Analysis**
- *Problem solved:* No systematic research on design principles for LLM-based MAS in SE
- *Key assumptions:* Patterns extracted from papers represent reusable design knowledge
- *Comparison to others:* Complements He et al. (Paper 1) — where He covers *what* is built, this covers *how* to design it
- *Strengths:* Practical design guidance, rigorous pattern extraction, strong SE engineering focus
- *Weaknesses:* Under review — not yet peer-validated; 94-paper scope smaller than Papers 1–6
- *Open questions:* How do these 16 patterns perform comparatively in controlled experiments?

---

## Paper 8 — Survey on Evaluation of LLM-based Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Yehudai2025evalsurvey |
| **Authors** | Asaf Yehudai, Lilach Eden, Alan Li, Guy Uziel, Yilun Zhao, Roy Bar-Haim, Arman Cohan, Michal Shmueli-Scheuer |
| **Year** | 2025 (submitted Mar 2025, revised Apr 2026) |
| **Venue** | ACL Findings 2025 |
| **Theme** | Survey / Evaluation |
| **Source DB** | arXiv |
| **Links** | [arXiv:2503.16416](https://arxiv.org/html/2503.16416v1) |

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

**How It Relates to Your Work**
Important for the Discussion/Gaps section — establishes that evaluation of multi-agent systems remains an open problem. Pairs well with SWE-Bench Pro (Paper 16) and the Benchmarks Survey (Paper 6).

**Critical Analysis**
- *Problem solved:* No systematic understanding of how LLM-based agents should be evaluated
- *Key assumptions:* Evaluation methodology is a distinct research concern from system design
- *Comparison to others:* Unique focus on evaluation vs. system design; complements all other surveys
- *Strengths:* Published at ACL (peer-reviewed); highly timely; clear gap identification
- *Weaknesses:* Descriptive only; does not propose new evaluation standards
- *Open questions:* How to create evaluations that resist gaming/benchmark overfitting?

---

---

# SECTION 2: FRAMEWORKS & SYSTEMS

---

## Paper 9 — MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework

| Field | Details |
|-------|---------|
| **BibTeX key** | Hong2023metagpt |
| **Authors** | Sirui Hong, Mingchen Zhuge, Jiaqi Chen, et al., Jürgen Schmidhuber |
| **Year** | 2023 (submitted Aug 2023; published ICLR 2024) |
| **Venue** | ICLR 2024 (top-tier ML conference) |
| **Theme** | Framework |
| **Source DB** | arXiv + Google Scholar |
| **Links** | [arXiv:2308.00352](https://arxiv.org/abs/2308.00352) |

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
- Generates more coherent solutions than chat-based multi-agent systems (e.g., ChatDev)

**Limitations**
- SOP design is manual — requires human effort to encode workflows
- Limited to structured software development tasks; unclear generalization to open-ended problems
- Does not address runtime errors in deployed software

**How It Relates to Your Work**
One of the two most-cited multi-agent SE frameworks (alongside ChatDev). Essential citation for the "current approaches" section. Contrasts with ChatDev's dialogue-based approach.

**Critical Analysis**
- *Problem solved:* Logic inconsistencies and cascading hallucinations in complex multi-agent collaboration
- *Key assumptions:* Human workflow patterns (SOPs) can be encoded effectively into LLM prompts
- *Comparison to others:* Uses structured docs vs. ChatDev's natural dialogue; more deterministic but less flexible
- *Strengths:* ICLR peer-reviewed; strong benchmark results; reproducible due to open-source release
- *Weaknesses:* SOP encoding is a bottleneck; limited to predefined workflows
- *Open questions:* Can SOPs be learned or generated automatically? How does MetaGPT handle novel task types?

---

## Paper 10 — ChatDev: Communicative Agents for Software Development

| Field | Details |
|-------|---------|
| **BibTeX key** | Qian2023chatdev |
| **Authors** | Chen Qian, Wei Liu, Hongzhang Liu, Nuo Chen, Yufan Dang, et al., Zhiyuan Liu, Maosong Sun |
| **Year** | 2023 (submitted Jul 2023; accepted ACL 2024) |
| **Venue** | ACL 2024 (top-tier NLP conference) |
| **Theme** | Framework |
| **Source DB** | arXiv + ACM DL |
| **Links** | [arXiv:2307.07924](https://arxiv.org/abs/2307.07924) |

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

**How It Relates to Your Work**
Foundational framework paper — pair with MetaGPT to illustrate the two dominant communication paradigms (dialogue vs. structured documents). Both are essential citations.

**Critical Analysis**
- *Problem solved:* Fragmentation of software development pipeline across specialized models
- *Key assumptions:* Natural language is a sufficient medium for all inter-agent coordination
- *Comparison to others:* Higher quality scores than MetaGPT but less structured; both outperform single-LLM baselines
- *Strengths:* ACL peer-reviewed; open-source; demonstrates end-to-end pipeline; good empirical results
- *Weaknesses:* Verbosity of dialogue; scalability to large codebases unproven
- *Open questions:* What is the optimal mix of natural language vs. structured communication in multi-agent SE?

---

## Paper 11 — AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation

| Field | Details |
|-------|---------|
| **BibTeX key** | Wu2023autogen |
| **Authors** | Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, Beibin Li, Erkang Zhu, et al., Chi Wang |
| **Year** | 2023 (submitted Aug 2023, revised Oct 2023) |
| **Venue** | arXiv (cs.AI); Microsoft Research |
| **Theme** | Framework |
| **Source DB** | arXiv + DBLP |
| **Links** | [arXiv:2308.08155](https://arxiv.org/abs/2308.08155) · [DBLP](https://dblp.org/rec/journals/corr/abs-2308-08155.html) |

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

**How It Relates to Your Work**
AutoGen is the most cited multi-agent framework and is used as the backbone in many subsequent systems (ALMAS, AgentCoder variants, etc.). Essential citation for the "frameworks" section.

**Critical Analysis**
- *Problem solved:* Need for a generic, reusable infrastructure for multi-agent LLM applications
- *Key assumptions:* Conversational paradigm is general enough for all agent interaction patterns
- *Comparison to others:* More general-purpose than MetaGPT or ChatDev; less task-specific; better for developers building custom systems
- *Strengths:* Open-source, widely adopted, flexible, human-in-the-loop support
- *Weaknesses:* No SE-specific benchmarks; loop/convergence issues in complex tasks
- *Open questions:* How does AutoGen compare to MetaGPT/ChatDev on standardized SE benchmarks?

---

## Paper 12 — AgentCoder: Multi-Agent-based Code Generation with Iterative Testing and Optimisation

| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2023agentcoder |
| **Authors** | Dong Huang, Jie M. Zhang, Michael Luck, Qingwen Bu, Yuhao Qing, Heming Cui |
| **Year** | 2023 (submitted Dec 2023, revised May 2024) |
| **Venue** | arXiv (cs.CL) |
| **Theme** | Framework / Code Generation |
| **Source DB** | arXiv |
| **Links** | [arXiv:2312.13010](https://arxiv.org/abs/2312.13010) |

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
- Token overhead: 56.9K / 66.3K vs. 138.2K / 206.5K for prior SOTA — 2.5-3x more efficient

**Limitations**
- Evaluated only on standard code generation benchmarks (HumanEval, MBPP) — not real-world SE tasks
- Does not address multi-file or project-level code generation
- Test designer may generate insufficient test coverage for complex logic

**How It Relates to Your Work**
Good example of applying multi-agent collaboration to a specific SE task (code generation). Demonstrates feedback loops between agents. Compare with Agentless (Paper 13) which challenges the need for agent complexity.

**Critical Analysis**
- *Problem solved:* Single-agent code generation lacks self-verification and iterative improvement
- *Key assumptions:* Test-execution feedback is sufficient signal for code quality improvement
- *Comparison to others:* Better benchmark scores than MetaGPT/ChatDev on code tasks; more efficient than prior SOTA
- *Strengths:* Strong quantitative results; efficient token usage; clear iterative mechanism
- *Weaknesses:* Limited to function-level benchmarks; no real-world SE evaluation
- *Open questions:* Does the three-agent feedback loop generalize to repository-level code generation?

---

## Paper 13 — Agentless: Demystifying LLM-based Software Engineering Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Xia2024agentless |
| **Authors** | Chunqiu Steven Xia, Yinlin Deng, Soren Dunn, Lingming Zhang |
| **Year** | 2024 (submitted Jul 2024, revised Oct 2024) |
| **Venue** | arXiv (cs.SE); NeurIPS 2024 workshop |
| **Theme** | Framework / Anti-agent argument |
| **Source DB** | arXiv + DBLP |
| **Links** | [arXiv:2407.01489](https://arxiv.org/abs/2407.01489) · [DBLP](https://dblp.org/rec/journals/corr/abs-2407-01489.html) |

**Main Contribution**
Proposes a deliberately simple, non-agent approach (localize → repair → validate) that outperforms all open-source agent systems on SWE-bench Lite. Challenges the assumption that agent complexity is necessary for SE tasks. Also introduces SWE-bench Lite-S, a cleaner evaluation subset.

**Methods Used**
- Three-phase pipeline (no agent decision-making):
  1. Localization: identify relevant files/functions
  2. Repair: generate patches
  3. Patch validation: filter and rank candidates
- Deliberately avoids LLM-controlled tool use or autonomous decision-making

**Results / Findings**
- 32.00% accuracy (96/300 correct fixes) on SWE-bench Lite — best open-source result at time of publication
- Cost: only $0.70 per task — dramatically cheaper than agent-based approaches
- Identified issues in SWE-bench Lite (ambiguous descriptions, problematic ground truths) → created SWE-bench Lite-S

**Limitations**
- Three-phase pipeline is fixed — cannot adapt to unexpected situations mid-task
- Performance ceiling limited without agent-like planning for multi-hop reasoning tasks
- Does not generalize well to tasks requiring complex multi-file understanding

**How It Relates to Your Work**
Critical counterpoint to the entire multi-agent literature. Use in Discussion/Gaps to argue that complexity ≠ performance, and to identify an open research question: when are agents actually beneficial?

**Critical Analysis**
- *Problem solved:* Questions whether complex autonomous agents are actually needed for SE tasks
- *Key assumptions:* SE problems can be decomposed into fixed localization + repair steps
- *Comparison to others:* Outperforms ChatDev, MetaGPT, AutoGen-based systems on SWE-bench with simpler approach
- *Strengths:* Provocative and important counterargument; strong benchmark results; very low cost
- *Weaknesses:* Fixed pipeline limits flexibility; may not scale to harder long-horizon tasks (see SWE-Bench Pro)
- *Open questions:* What task characteristics make agents necessary vs. optional?

---

## Paper 14 — ALMAS: An Autonomous LLM-based Multi-Agent Software Engineering Framework

| Field | Details |
|-------|---------|
| **BibTeX key** | Tawosi2025almas |
| **Authors** | Vali Tawosi, Keshav Ramani, Salwa Alamir, Xiaomo Liu |
| **Year** | 2025 (submitted Oct 2025, revised Nov 2025) |
| **Venue** | MAS-GAIN Workshop at ASE 2025 |
| **Theme** | Framework |
| **Source DB** | arXiv |
| **Links** | [arXiv:2510.03463](https://arxiv.org/abs/2510.03463) |

**Main Contribution**
A vision framework for autonomous multi-agent LLM systems that models the full software development lifecycle, aligning agents to agile development roles (product manager, sprint planner, developer, tester, reviewer). Designed for seamless integration with human developers and existing dev environments.

**Methods Used**
- Multi-agent architecture aligned with agile team roles
- Modular design for integration with existing development environments
- Framework structured around SDLC stages with agent handoffs

**Results / Findings**
- Demonstrated capability to generate an application and add a new feature in a use case scenario
- Shows practical viability within agile development workflows
- Framework represents a "progress towards ALMAS" rather than a complete implementation

**Limitations**
- Vision/early-stage paper — not a full implementation
- Limited empirical evaluation; only proof-of-concept demonstrated
- Unclear how it handles conflicts between agent recommendations

**How It Relates to Your Work**
Good example of applying multi-agent systems to the full SDLC with agile methodologies. Compare with ChatDev and MetaGPT which cover partial pipelines.

**Critical Analysis**
- *Problem solved:* LLM automation remains task-isolated rather than covering the full agile SDLC
- *Key assumptions:* Agile role specialization maps naturally to agent role specialization
- *Comparison to others:* More comprehensive SDLC coverage than AgentCoder (Paper 12); earlier-stage than ChatDev (Paper 10)
- *Strengths:* Agile-aligned design; modular architecture; human integration considered
- *Weaknesses:* Workshop paper, limited validation; vision-stage only
- *Open questions:* How does ALMAS handle backlog prioritization and sprint planning autonomously?

---

## Paper 15 — Multi-Agent Collaboration: Harnessing the Power of Intelligent LLM Agents

| Field | Details |
|-------|---------|
| **BibTeX key** | Talebirad2023collaboration |
| **Authors** | Yashar Talebirad, Amirhossein Nadiri |
| **Year** | 2023 (submitted Jun 2023) |
| **Venue** | arXiv (cs.AI) |
| **Theme** | Framework (Foundational) |
| **Source DB** | arXiv + DBLP |
| **Links** | [arXiv:2306.03314](https://arxiv.org/abs/2306.03314) · [DBLP](https://dblp.org/rec/journals/corr/abs-2306-03314.html) |

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

**How It Relates to Your Work**
Historical/foundational paper that helps establish the chronological narrative in your background section. Shows the field was already recognizing key challenges in mid-2023.

**Critical Analysis**
- *Problem solved:* Standalone LLM performance limitations on complex multi-step problems
- *Key assumptions:* Role differentiation between agents is key to improved performance
- *Comparison to others:* Earlier and more conceptual than MetaGPT, ChatDev, AutoGen; identified challenges still unsolved today
- *Strengths:* Early identification of still-relevant challenges; good for historical context
- *Weaknesses:* No quantitative results; predates modern frameworks
- *Open questions:* The challenges it identified (looping, security, scalability) remain unsolved as of 2025

---

---

# SECTION 3: BENCHMARKS

---

## Paper 16 — SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?

| Field | Details |
|-------|---------|
| **BibTeX key** | Deng2025swebenchpro |
| **Authors** | Xiang Deng, Jeff Da, Edwin Pan, Yannis Yiming He, Charles Ide, et al. |
| **Year** | 2025 (submitted Sep 2025, revised Nov 2025) |
| **Venue** | arXiv (cs.SE + cs.CL) |
| **Theme** | Benchmark |
| **Source DB** | arXiv |
| **Links** | [arXiv:2509.16941](https://arxiv.org/abs/2509.16941) |

**Main Contribution**
Introduces SWE-Bench Pro: an advanced benchmark of 1,865 enterprise-level software engineering problems from 41 actively maintained repositories, designed to evaluate AI agents on realistic, long-horizon, multi-file tasks that exceed existing SWE-bench difficulty.

**Methods Used**
- Dataset sourced from active repos spanning business, B2B, and developer tools
- Three-partition design: public (11 repos), held-out (12 repos), commercial/proprietary (18 repos)
- Human verification of all tasks with contextual documentation
- Failure mode clustering analysis of agent trajectories

**Results / Findings**
- Reveals significant capability gaps in current agents for enterprise-level problems
- Existing agents struggle with tasks requiring patches across multiple files and substantial code modifications
- Failure mode analysis reveals systematic patterns in how agents fail on long-horizon tasks

**Limitations**
- Commercial partition introduces accessibility barriers for researchers
- Ground truth patches may not represent the only valid solutions
- Benchmark may have selection bias toward certain repository types

**How It Relates to Your Work**
Critical for the Discussion/Gaps section — establishes the state-of-the-art evaluation frontier and shows current agents still fall short of real-world enterprise SE. Pairs with Agentless (Paper 13) and the Benchmarks Survey (Paper 6).

**Critical Analysis**
- *Problem solved:* Existing benchmarks (SWE-bench Lite) are too simple to reveal agent limitations on real enterprise tasks
- *Key assumptions:* GitHub issues from enterprise repos represent realistic SE tasks
- *Comparison to others:* Harder and more realistic than original SWE-bench; complements Guo et al. (Paper 6)'s benchmark survey
- *Strengths:* Large scale (1,865 problems); contamination-resistant (held-out partition); human-verified
- *Weaknesses:* Proprietary partition limits reproducibility; high cost to run agents at this scale
- *Open questions:* What agent architectures are best suited for long-horizon multi-file tasks?

---

---

# SECTION 4: ARCHITECTURE & DESIGN

---

## Paper 17 — SALLMA: A Software Architecture for LLM-Based Multi-Agent Systems

| Field | Details |
|-------|---------|
| **BibTeX key** | Becattini2025sallma |
| **Authors** | M. Becattini, R. Verdecchia, E. Vicario |
| **Year** | 2025 |
| **Venue** | SATrends Workshop at ICSE 2025 (pp. 5–8) |
| **Theme** | Architecture |
| **Source DB** | IEEE Xplore |
| **Links** | [IEEE](https://ieeexplore.ieee.org/document/11029425/) · [PDF](https://robertoverdecchia.github.io/papers/SATrends_2025.pdf) |

**Main Contribution**
Proposes SALLMA, a layered software architecture for LLM-based multi-agent systems with two core layers: (1) Operational Layer — handles request intent, real-time task execution, and dynamic agent orchestration; (2) Knowledge Layer — stores and manages metamodels, configurations, and workflows.

**Methods Used**
- Architecture design using modular, distributed multi-agent paradigm
- Two-layer architecture pattern (Operational + Knowledge)
- Addressed design challenges: task customization, persistent memory, ground truth access

**Results / Findings**
- Modular distributed architecture enables flexible deployment of cognitive workflows
- Two-layer design overcomes limitations of single-agent LLM systems
- Presented as a prototypical architecture — implementation-ready reference design

**Limitations**
- Short workshop paper (4 pages) — limited empirical evaluation
- Architecture is prototypical, not validated at production scale
- Does not address fault tolerance or security properties

**How It Relates to Your Work**
Useful for the architecture/design subsection when discussing how to structure multi-agent systems. Pairs with Cai et al. (Paper 7) on design patterns.

**Critical Analysis**
- *Problem solved:* Lack of structured architectural guidance for building LLM-based multi-agent software products
- *Key assumptions:* Separating operational and knowledge concerns improves modularity
- *Comparison to others:* More architecturally formal than AutoGen; less task-specific than MetaGPT
- *Strengths:* ICSE workshop publication; clear architectural model; directly actionable for engineers
- *Weaknesses:* 4-page workshop paper — limited depth; prototypical only
- *Open questions:* How does this architecture scale to 10+ agent systems? What are the security implications?

---

---

# SECTION 5: VISION & ROADMAP

---

## Paper 18 — Agentic Software Engineering: Foundational Pillars and a Research Roadmap

| Field | Details |
|-------|---------|
| **BibTeX key** | Hassan2025agenticroadmap |
| **Authors** | Ahmed E. Hassan, Hao Li, Dayi Lin, Bram Adams, Tse-Hsun Chen, Yutaro Kashiwa, Dong Qiu |
| **Year** | 2025 (submitted Sep 2025, revised Sep 2025) |
| **Venue** | arXiv (cs.SE) |
| **Theme** | Vision / Roadmap |
| **Source DB** | arXiv |
| **Links** | [arXiv:2509.06216](https://arxiv.org/abs/2509.06216) |

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

**How It Relates to Your Work**
Excellent for the Conclusion and Future Directions sections — frames where the field is heading. Cite when making claims about long-term trajectories of multi-agent SE.

**Critical Analysis**
- *Problem solved:* No community vocabulary or framework for discussing the transition to agent-assisted SE
- *Key assumptions:* Agents will eventually take on full engineering roles, not just code generation
- *Comparison to others:* More forward-looking than all other papers; less empirical than benchmarks/frameworks
- *Strengths:* Well-respected authors (Ahmed Hassan is a leading SE researcher); clear conceptual framing
- *Weaknesses:* No empirical support; purely conceptual
- *Open questions:* What governance, accountability, and trust models are needed for agentic SE in production?

---

---

# SECTION 6: HUMAN-AI COLLABORATION & APPLICATIONS

---

## Paper 19 — Facilitating Trustworthy Human-Agent Collaboration in LLM-based MAS for SE

| Field | Details |
|-------|---------|
| **BibTeX key** | Ronanki2025trustworthy |
| **Authors** | Krishna Ronanki |
| **Affiliation** | Chalmers University of Technology / University of Gothenburg, Sweden |
| **Year** | 2025 |
| **Venue** | FSE Companion '25 (ACM SIGSOFT Companion Proceedings), Trondheim, Norway, June 23–27, 2025 |
| **Theme** | Human-AI Collaboration |
| **Source DB** | ACM DL |
| **Links** | [ACM](https://dl.acm.org/doi/10.1145/3696630.3728717) |
| **Status** | ✅ Read |

### Main Contribution
Proposes a RACI-based framework for task allocation between humans and LLM-based agents across SDLC phases, with explicit alignment to EU AI Act (AIA) compliance requirements. The 9-step process operationalizes which tasks can be delegated to agents and under what governance constraints, providing a practical governance tool for practitioners integrating LLM agents into software teams.

### Methods Used
- **RACI matrix adaptation:** Extends the standard RACI (Responsible / Accountable / Consulted / Informed) framework to cover LLM-based agents as team members alongside human roles.
- **Key governance rule (Rule 3):** No Responsible assignment may be given to an LLM agent unless a human is Accountable for that same task — preserving human oversight as required by the EU AI Act.
- **Example instantiation:** DevOps Planning phase with 3 human roles (Product Owner, Business Analyst, Scrum Master) + 3 LLM agents (Requirements Elicitation Agent, User Story Agent, Scrum Assistant — note: Scrum Assistant is hypothetical/future).
- **6 tasks mapped:** Requirements Elicitation, Product Roadmap Definition, User Story Writing, Product Backlog Management, Sprint Planning, Sprint Goal Setting.
- **Work-in-progress (5 pages):** Future validation via groupware walkthrough multi-case study planned.

### Results / Findings
- Tasks suitable for LLM-agent Responsible assignment: User Story Writing, Backlog Management, Sprint Planning.
- Tasks NOT suitable (human must remain Responsible): Requirements Elicitation (direct stakeholder interaction required), Product Roadmap (strategic accountability).
- Demonstrates that RACI-adapted framework naturally enforces AIA Article 14 (human oversight of high-risk AI systems).

### Limitations
- No empirical validation yet; framework is prescriptive/theoretical.
- The Scrum Assistant LLM agent used in the example does not yet exist.
- Scope limited to DevOps Planning phase — generalization to other SDLC phases requires further work.
- Groupware walkthrough study planned but not yet conducted.

### How It Relates to This Review
Directly addresses the **trust and governance gap** in multi-agent SE systems. While most papers focus on performance (code generation accuracy, bug fix rates), this paper asks: how do we govern human-agent teams? It connects AI Act compliance to practical SDLC workflows, making it essential for the "future challenges" and "human-in-the-loop" sections of the review.

### Critical Analysis
**Strengths:** Highly practical and actionable; bridges regulatory compliance (EU AI Act) and SE practice in a way most technical papers ignore; RACI is widely understood by practitioners, lowering adoption barrier. Published at FSE — top-tier SE venue validates importance of the problem.

**Weaknesses:** Work-in-progress with no validation data; the RACI adaptation is intuitive but not rigorously tested against real team dynamics; Rule 3 (human accountability prerequisite) is sound in principle but may be difficult to enforce in automated pipelines where accountability is diffuse.

**Open question:** What happens when the "human Accountable" is overwhelmed by the pace of LLM-agent outputs and rubber-stamps decisions? The framework doesn't address accountability drift at scale.

---

## Paper 20 — Demystifying LLM-Based Software Engineering Agents (ACM PACMSE)

| Field | Details |
|-------|---------|
| **BibTeX key** | Xia2025demystify |
| **Authors** | Chunqiu Steven Xia*, Yinlin Deng*, Soren Dunn, Lingming Zhang (* equal contribution) |
| **Affiliation** | University of Illinois Urbana-Champaign (UIUC) |
| **Year** | 2025 |
| **Venue** | Proc. ACM Softw. Eng., Vol. 2, FSE, Article FSE037, July 2025 (received 2024-09-13; accepted 2025-01-14) |
| **Theme** | Framework / Empirical Analysis |
| **Source DB** | ACM DL |
| **Links** | [ACM](https://dl.acm.org/doi/abs/10.1145/3715754) |
| **Status** | ✅ Read |

> **Note:** This is the **peer-reviewed journal version** of the Agentless system (arXiv preprint = Paper 13). The published version adds SWE-bench Verified results, extended ablation studies, upper-bound analysis, and comparison against 26 agent-based baselines.

### Main Contribution
Agentless challenges the assumption that more agent complexity = better performance. The system decomposes GitHub issue resolution into three sequential non-agentic phases: (1) **Localization** (file → class → function), (2) **Repair** (sample multiple patches via LLM), (3) **Patch Validation** (filter + rank patches). By removing autonomous decision-making and tool use, Agentless achieves state-of-the-art results at dramatically lower cost and with full reproducibility.

### Methods Used
- **Hierarchical localization:** Tree-structure file embedding → suspicious files → suspicious classes/functions → edit locations.
- **Patch sampling:** Generates multiple candidate patches; filters uncompilable; ranks by test-passing and majority voting.
- **Benchmarks:** SWE-bench Lite (300 issues), SWE-bench Verified (500 issues, higher quality).
- **Models tested:** GPT-4o (primary), Claude 3.5 Sonnet (best results).
- **Comparison baseline:** 26 agent-based systems (AutoCodeRover, SWE-agent, CodeAct, etc.).

### Results / Findings
| Benchmark | Model | Resolve Rate |
|-----------|-------|-------------|
| SWE-bench Lite | GPT-4o | 32.00% |
| SWE-bench Verified | GPT-4o | 38.80% |
| SWE-bench Verified | Claude 3.5 Sonnet | **50.80%** |
- **Upper bound analysis:** Even if the "best" patch from all candidates were selected, only 42% (126/300) of issues would be resolved — revealing a fundamental ceiling from localization failures and problem complexity, not agent design.
- **Problem classification:** Issues vary by description quality (some contain solution hints); location information availability; reproducibility.
- **Adopted by:** OpenAI (GPT-4o, o1) and DeepSeek (V3, R1) as their default SWE-bench evaluation approach.

### Limitations
- Still fails on ~50% of issues even with Claude 3.5 Sonnet — upper bound analysis suggests LLM capability is the bottleneck.
- Agentless design trades flexibility for reproducibility; cannot handle tasks requiring multi-step tool interaction or dynamic information gathering.
- Single-file patch assumption may miss cross-file bugs.
- Data leakage risk: training data may include SWE-bench issues.

### How It Relates to This Review
This paper is the **critical counterpoint** to MetaGPT/ChatDev/AutoGen. The community trend toward increasingly complex agent frameworks is challenged by showing that a simple, structured pipeline outperforms complex agents on the leading benchmark. Essential for the "complexity vs. simplicity" debate in the review.

### Critical Analysis
**Strengths:** Rigorous empirical methodology; reproducible pipeline; the upper-bound analysis is a genuine intellectual contribution that reframes the field's evaluation discourse; PACMSE journal venue ensures peer-reviewed quality; adopted by major LLM labs as standard evaluation baseline validates real-world impact.

**Weaknesses:** "Agentless" is a design choice that works for SWE-bench's structure (single-repo, isolated issues) but may not generalize to enterprise codebases with cross-cutting concerns; the paper doesn't address maintenance workloads, new feature development, or multi-repo scenarios where agent autonomy may be necessary.

**Irony:** By showing that simple beats complex, this paper implicitly raises the question of why the field invests so heavily in elaborate agent architectures. The answer may be that SWE-bench is itself an imperfect proxy for real SE work.

---

## Paper 21 — Towards LLM-augmented Multi-Agent Systems for Agile Software Engineering

| Field | Details |
|-------|---------|
| **BibTeX key** | Chudziak2024cogniSim |
| **Authors** | Jarosław A. Chudziak, Konrad Cinkusz |
| **Affiliation** | Warsaw University of Technology, Poland |
| **Year** | 2024 |
| **Venue** | ASE 2024 (IEEE/ACM International Conference on Automated Software Engineering), Sacramento, CA, Oct 27 – Nov 1, 2024 |
| **Theme** | Framework / Agile SE |
| **Source DB** | ACM DL + IEEE Xplore |
| **Links** | [ACM](https://dl.acm.org/doi/10.1145/3691620.3695336) · [IEEE](https://ieeexplore.ieee.org/document/10764913/) |
| **Status** | ✅ Read |

### Main Contribution
Introduces the **CogniSim Ecosystem** — a cognitive multi-agent framework for agile software engineering that integrates LLMs with Theory of Mind (ToM) for realistic agent behavior simulation. Agents model not just task execution but the mental states and perspectives of different team roles (developers, quality checkers, methodology reviewers), enabling simulation of team dynamics.

### Methods Used
- **Theory of Mind integration:** Agents maintain models of other agents' beliefs and intentions, enabling more realistic collaboration simulation.
- **Agent roles:** Developer agents, Executor agents (run code), Quality Checker agents, Methodology Reviewer agents (SAFe compliance).
- **Frameworks used:** LangChain for LLM orchestration; SAFe (Scaled Agile Framework) for process structure.
- **Scope:** 2-page paper (demo/vision track at ASE 2024); proof-of-concept via case studies and simulations.

### Results / Findings
- Case studies demonstrate agents can simulate agile team interactions and identify code quality issues through multi-perspective review.
- ToM-based agents produce more contextually appropriate feedback than single-agent approaches.
- System can operate within SAFe methodology constraints, aligning LLM agent outputs with enterprise agile processes.
- **Note:** As a 2-page demo paper, quantitative benchmarking is limited; results are primarily qualitative.

### Limitations
- 2-page format precludes rigorous empirical evaluation; no comparison against baselines.
- Proof-of-concept only — scalability to real sprint teams unvalidated.
- Theory of Mind implementation is approximated through prompting, not true belief modeling.
- LangChain dependency introduces framework volatility risk.

### How It Relates to This Review
Provides the **agile SE perspective** on multi-agent systems, connecting the technical agent frameworks (MetaGPT, AutoGen) to Agile/SAFe process methodologies. ToM integration is a novel angle largely absent from other papers in this set. Relevant to discussions of agent role design and team simulation.

### Critical Analysis
**Strengths:** Theory of Mind framing is genuinely novel in the SE-agent context; SAFe integration shows awareness of enterprise adoption realities; ASE 2024 is a strong venue for this type of work.

**Weaknesses:** 2-page length severely limits claims — the paper presents a vision more than validated results; no quantitative evaluation of whether ToM actually improves outcomes vs. standard role-prompted agents; the LangChain + SAFe combination adds significant engineering complexity without clear evidence of benefit over simpler approaches.

**Gap it exposes:** Most multi-agent SE papers simulate software development in isolation; CogniSim attempts to simulate the social/team dynamics of SE, which is arguably more realistic but also harder to evaluate rigorously.

---

## Paper 22 — A Multi-Agent LLM System for Automated Requirements Analysis: A Study on User Story Generation and Prioritization

| Field | Details |
|-------|---------|
| **BibTeX key** | Sami2025requirements |
| **Authors** | Malik Abdul Sami, Zheying Zhang, Muhammad Waseem, Kai-Kristian Kemell, Zeeshan Rasheed, Tomas Herda, et al. |
| **Affiliation** | Tampere University (Finland) + Austrian Post (industry) |
| **Year** | 2025 |
| **Venue** | SEAA 2025 (Euromicro Conference on Software Engineering and Advanced Applications), LNCS 16082, pp. 178–187, 2026 (Springer) |
| **Theme** | Application / Requirements Engineering |
| **Source DB** | ACM DL (Springer) |
| **Links** | [Springer](https://link.springer.com/chapter/10.1007/978-3-031-72194-0_12) |
| **Status** | ✅ Read |

### Main Contribution
Demonstrates a 4-agent LLM pipeline for requirements engineering: generating user stories from project background, then prioritizing them using the **100-dollar technique**. Evaluates 4 LLMs (GPT-4o, LLaMA 3.3, Mistral-Nemo, Falcon3) on a real Mobile Delivery Application case study from Austrian Post, providing quantitative comparison across relevance, coverage, and consistency metrics.

### Methods Used
- **4-agent architecture:** PO Agent (domain analysis) → Developer Agent (user story generation) → QA Agent (quality review) → Manager Agent (100-dollar prioritization + Kendall's Tau consistency check).
- **Relevance metric:** Cosine similarity using `all-MiniLM-L6-v2` sentence embedding model.
- **Consistency metric:** Kendall's Tau rank correlation across multiple LLM runs.
- **Dataset:** 12 user stories for a Mobile Delivery Application (real industrial case from Austrian Post).
- **Baseline:** Comparison to human expert prioritization.
- **100-dollar technique:** Stakeholders (agents) allocate 100 virtual dollars across requirements to reflect relative importance.

### Results / Findings
| LLM | Avg. Cosine Similarity | Kendall's Tau |
|-----|----------------------|---------------|
| LLaMA 3.3 70B | **0.50** (highest relevance) | — |
| GPT-4o | 0.44 | — (best coverage & human alignment) |
| Mistral-Nemo | — | **0.252** (most consistent) |
| Falcon3 | 0.46 | — |
- GPT-4o produces user stories closest to human expert judgment (best coverage + alignment).
- LLaMA 3.3 achieves highest semantic similarity but not necessarily best coverage.
- Mistral-Nemo is the most consistent across runs.
- Overall: only moderate alignment with human expert across all models — no LLM fully replaces domain expert judgment.

### Limitations
- Single industrial case study (12 user stories) — limited generalizability.
- Single human expert used as ground truth; no inter-rater reliability established.
- Run-to-run variability of LLMs reduces reliability for production use.
- Static background document input — dynamic project evolution and stakeholder interaction not modeled.
- Background info alone insufficient for complete requirements capture (stakeholder interviews still needed).

### How It Relates to This Review
Represents the **requirements engineering application** of multi-agent LLM systems — the upstream SDLC phase often neglected in favor of code generation. Provides concrete quantitative evidence of LLM agent capabilities and limitations in early-phase SE work. The 100-dollar prioritization + Kendall's Tau methodology offers a rigorous evaluation framework other application papers lack.

### Critical Analysis
**Strengths:** Real industrial case study with Austrian Post adds external validity; multi-metric evaluation (relevance + consistency + human alignment) is more rigorous than many application papers; quantitative LLM comparison is directly useful for practitioners choosing models; academic-industry collaboration is a strength for applicability.

**Weaknesses:** 12 user stories is a very small dataset; single expert ground truth is methodologically weak; the result that "no model fully replaces domain expert" is unsurprising — the more interesting finding (what specifically do LLMs miss?) is underexplored; SEAA is a mid-tier venue.

**Practical implication:** The moderate alignment scores (0.44–0.50 cosine similarity) suggest LLM agents can serve as a first draft / scaffolding tool for requirements, but human review remains essential — a finding consistent with the governance framework in Paper 19.

---

## Paper 23 — An LLM-Based Agent-Oriented Approach for Automated Code Design Issue Localization

| Field | Details |
|-------|---------|
| **BibTeX key** | Batole2025localizeagent |
| **Authors** | Fraol Batole, David OBrien, Tien N. Nguyen, Robert Dyer, Hridesh Rajan |
| **Affiliation** | Tulane University, Iowa State University, University of Texas at Dallas, University of Nebraska-Lincoln |
| **Year** | 2025 |
| **Venue** | ICSE 2025 (47th IEEE/ACM International Conference on Software Engineering) |
| **Theme** | Application / Code Quality / Design Issues |
| **Source DB** | IEEE Xplore |
| **Links** | [IEEE](https://ieeexplore.ieee.org/iel8/11029684/11029718/11029742.pdf) |
| **Status** | ✅ Read |

### Main Contribution
Introduces **LOCALIZEAGENT** — a 4-agent pipeline that combines static analysis (PMD), program analysis metrics, and LLM-based ranking to automatically identify and localize code design issues (anti-patterns) requiring refactoring. Achieves 138–206% improvement over direct LLM prompting across three design issue categories on a real-world dataset of 6,000+ Java projects.

### Methods Used
- **4-agent pipeline:**
  1. *Design Issue Analysis Agent* — runs PMD static analysis, identifies candidate design issues.
  2. *Program Analysis Agent* — computes structural metrics: Fan-in/out, Call Relationships, Variable Usage, Class Coupling.
  3. *Context-aware Prompt Building Agent* — synthesizes PMD output + metrics into structured LLM prompts.
  4. *LLM-based Ranking Agent* — ranks candidate refactoring locations using GPT-4o or Claude 3.
- **Dataset:** Aniche et al. refactoring dataset; 6K+ Java projects; 4 refactoring types (Parameterize Variable, Inline Method, Inline Variable, Move Method).
- **3 design issue categories:** Modularity, Information Hiding, Complexity.
- **Evaluation metric:** Exact-Match@K (EM@K) — whether the correct location appears in top-K predictions.
- **LLMs compared:** GPT-4o (best accuracy), Claude 3 (best time/cost efficiency).

### Results / Findings
| Design Issue Category | Baseline (LLM alone) | LOCALIZEAGENT (GPT-4o) | Improvement |
|----------------------|---------------------|------------------------|-------------|
| Modularity (EM@1) | 8.0% | 24.5% | **+206%** |
| Complexity (EM@1) | 10.7% | 28.5% | **+166%** |
| Information Hiding (EM@1) | 16.9% | 40.3% | **+138%** |
- Best performance on Inline Variable refactoring type (43–48% EM@1).
- Claude 3 offers comparable accuracy with significantly lower latency and cost — practical advantage for large codebases.
- Program analysis metrics (Fan-in/out, coupling) are the most informative context for LLM ranking.

### Limitations
- Scope limited to **local design issues** (within a single class) — cross-class or architectural-level issues not addressed.
- PMD rule-based filtering may introduce false positives that propagate through the pipeline.
- LLM non-determinism means results vary across runs.
- Data leakage risk: LLMs may have been trained on code from the Aniche dataset.
- Java only; generalization to other languages unvalidated.

### How It Relates to This Review
Demonstrates the **code maintenance application** of multi-agent LLM systems — extending beyond code generation to code quality management. The hierarchical pipeline (static analysis → program analysis → LLM ranking) mirrors the localization approach of Agentless (Paper 13/20) but applied to design issues rather than bug fixes. The 200%+ improvement over LLM-alone prompting quantifies the value of the multi-agent structure.

### Critical Analysis
**Strengths:** Rigorous evaluation on 6K real-world Java projects; multi-LLM comparison; EM@K metric is appropriate for the localization task; ICSE 2025 publication signals peer-reviewed quality at the top SE venue; practical pipeline that integrates existing tools (PMD) rather than replacing them.

**Weaknesses:** 28.5% EM@1 for complexity (the best category) means the system fails 71.5% of the time — "206% improvement" sounds impressive but the absolute performance is modest; local-only scope significantly limits applicability for real codebases where design issues are often cross-cutting; the PMD dependency creates a ceiling: issues PMD cannot detect are invisible to the system.

**Insight:** The large gap between direct LLM prompting (8–17% EM@1) and the full pipeline (25–40%) strongly suggests that structural context (program metrics) is what makes the difference — the LLM alone lacks the code comprehension needed for precise localization without these scaffolded inputs.

---

## Paper 24 — A Multi-Agent LLM Environment for Software Design and Refactoring: A Conceptual Framework

| Field | Details |
|-------|---------|
| **BibTeX key** | Rajendran2025refactoring |
| **Authors** | Vasanth Rajendran, Dinesh Besiahgari, Sachin C. Patil, Manjunath Chandrashekaraiah, Vishnu Challagulla |
| **Affiliation** | Amazon; University of Cincinnati; Independent; ALAB; Egen.ai |
| **Year** | 2025 |
| **Venue** | IEEE SoutheastCon 2025 |
| **Theme** | Application / Software Design & Refactoring |
| **Source DB** | IEEE Xplore |
| **Links** | [IEEE](https://ieeexplore.ieee.org/document/10971563/) |
| **Status** | ✅ Read |

### Main Contribution
Proposes a formal conceptual framework for a multi-agent LLM environment where specialized agents collaboratively perform software design and refactoring. The framework introduces a formal mathematical model (state space, action space, utility functions, coordination protocol) and motivates the approach through a concrete example showing that a single-agent solution causes security regressions while multi-agent collaboration avoids them.

### Methods Used
- **4 specialized agents:** Performance Agent, Security Agent, Maintainability Agent, UI/UX Agent.
- **Communication/Coordination Layer:** Manages inter-agent messaging and conflict resolution.
- **Formal model:**
  - State space: S = (C, M) where C = code artifacts, M = metadata.
  - Action space: Ξ per agent.
  - Utility function: Uᵢ(s): S → ℝ per agent.
  - Coordination Protocol: Π.
  - Termination Condition: τ.
- **Coordination protocols discussed:** Consensus-based (agents vote on changes) vs. Auction-based (agents bid for tasks based on capability).
- **Communication complexity:** O(R × n × m) where R = rounds, n = agents, m = message size.
- **Motivating example:** Performance Agent alone achieves 40% CPU reduction but introduces SQL injection vulnerability; multi-agent system achieves 65% CPU reduction while maintaining security.

### Results / Findings
- Conceptual framework only — **no implementation or empirical results**.
- The 40% → 65% CPU improvement example illustrates the theoretical advantage of multi-agent specialization.
- Consensus protocol ensures all agents agree before changes are committed; auction protocol reduces communication overhead.
- Formal model enables reasoning about termination guarantees and utility trade-offs.

### Limitations
- **Purely conceptual** — no prototype, no experiments, no evaluation against baselines.
- LLM hallucination propagation: if one agent generates a flawed output, downstream agents may amplify rather than correct errors.
- Formal model is simplified; real code has far more complex state representations.
- Ethical/accountability concerns for automated refactoring in production systems are noted but not resolved.
- Communication complexity O(R × n × m) may become prohibitive at scale.

### How It Relates to This Review
Provides the **theoretical/architectural framing** for multi-agent software refactoring — complementing the empirical work of Papers 23 (LOCALIZEAGENT) and 9 (MetaGPT). The formal model and coordination protocol discussion connect to the broader multi-agent systems literature. Useful as a background reference for architectural design discussions.

### Critical Analysis
**Strengths:** The motivating example (single-agent creates security vulnerabilities, multi-agent avoids them) is compelling and intuitive; the formal model provides a rigorous foundation even if the paper doesn't validate it empirically; coordination protocol comparison (consensus vs. auction) surfaces a genuine engineering trade-off.

**Weaknesses:** A conceptual framework paper published in 2025 with no implementation is a weak contribution — the field needs empirical evidence, not more frameworks; IEEE SoutheastCon is a regional/lower-tier venue; the "65% CPU improvement" example is hypothetical and illustrative, not measured; hallucination propagation risk is acknowledged but the proposed mitigation ("validation modules") is vague.

**Context:** This paper represents the "proposal phase" of multi-agent SE research — there are many such conceptual frameworks circulating. Its value is primarily as a point of comparison: it shows what the field *hopes* multi-agent systems can do, while papers like Agentless (Paper 13/20) and LOCALIZEAGENT (Paper 23) show what they *actually* do when implemented and measured.

---

## Paper 25 — AI-Powered Multi-Agent Framework for Automated Unit Test Case Generation: Enhancing Software Quality through LLMs

| Field | Details |
|-------|---------|
| **BibTeX key** | Garlapati2024testgen |
| **Authors** | Anusha Garlapati, M N V Satya Sai Muni Parmesh, Dr. Savitha, Jaisri S |
| **Affiliation** | Watsonx Client Engineering, IBM Bangalore, India |
| **Year** | 2024 |
| **Venue** | 2024 5th IEEE Global Conference for Advancement in Technology (GCAT), Karnataka, India, Oct 4–6, 2024 |
| **Theme** | Application / Testing / Test Generation |
| **Source DB** | IEEE Xplore |
| **Links** | [IEEE](https://ieeexplore.ieee.org/document/10923987/) |
| **Status** | ✅ Read |

### Main Contribution
Presents an IBM Watsonx-based multi-agent framework for automated Java unit test generation. Three specialized agents collaborate in an iterative loop — Reviewer, Code Generator, Decision-Maker — using LangGraph for orchestration and Mistral-large as the backbone LLM. The iterative feedback loop refines test cases until quality standards (100% code coverage) are met, demonstrating reduced human intervention.

### Methods Used
- **3-agent iterative loop:**
  1. *Reviewer Agent* — examines source code, identifies test scenarios and edge cases, provides structured feedback.
  2. *Code Generation Agent* — implements JUnit test cases based on Reviewer feedback.
  3. *Decision-Making Agent* — evaluates whether generated tests meet quality standards; if not, routes back to Reviewer for another iteration.
- **Orchestration:** LangGraph (workflow state machine for agent loops).
- **LLM:** Mistral-large (via IBM Watsonx).
- **Target language:** Java (JUnit framework).
- **Coverage target:** 100% statement coverage.
- **Test subject:** Simple arithmetic Java class (multiply/divide methods).

### Results / Findings
- 100% code coverage achieved for the provided sample code.
- Edge cases handled correctly (e.g., division by zero raises appropriate exception).
- Iterative refinement loop successfully converges without human intervention.
- Multi-agent approach reduces the burden of manually writing and reviewing test cases.

### Limitations
- **Severely limited scope:** Only tested on a simple 2-method Java class (multiply/divide) — 100% coverage of trivial code is not a meaningful benchmark.
- No comparison against existing automated test generation tools (EvoSuite, Randoop, CodaMosa).
- Scalability to real-world codebases (complex classes, inheritance hierarchies, external dependencies) entirely unvalidated.
- Only Java/JUnit — no cross-language evaluation.
- IBM Watsonx / Mistral-large may not be the optimal LLM choice; no model ablation.
- GCAT is a low-tier regional conference.

### How It Relates to This Review
Represents the **automated testing application** of multi-agent LLM systems — an important quality assurance dimension of the SDLC. The LangGraph orchestration approach connects to the broader theme of workflow-based agent coordination. However, as a proof-of-concept on trivial code, it contributes primarily as an illustrative example of the pattern rather than a rigorous evaluation. Useful for showing the breadth of multi-agent SE applications.

### Critical Analysis
**Strengths:** The 3-agent loop with iterative quality enforcement is a clean and reusable design pattern; LangGraph as orchestration layer is a practical choice with real-world adoption; the decision-making agent as quality gate (loop-back or terminate) is an elegant architectural choice; IBM Watsonx origin gives the work industrial credibility.

**Weaknesses:** The evaluation is the paper's major weakness — 100% coverage on a 2-method class proves nothing about scalability or real-world utility; the absence of comparison against EvoSuite or similar tools makes it impossible to assess whether the multi-agent overhead is justified; the "enhanced software quality" claim in the title is not substantiated by the minimal experiment; GCAT venue significantly limits confidence in peer-review rigor.

**Verdict:** This paper is best read as an industrial demo/proof-of-concept from IBM practitioners rather than a research contribution. Its value for the review is illustrative (showing multi-agent patterns applied to testing) rather than evidentiary. If including in the final 12–15 papers, pair with a stronger testing paper or frame as "industry adoption signal."

---

---

# FILTERING GUIDE

## Recommended 12–15 Papers for Final Review

### Must-Include (8 core papers)
| # | Reason |
|---|--------|
| 1 | Best survey directly on LMA systems for SE — He et al. TOSEM 2025 |
| 2 | Largest systematic survey (124 papers) — Liu et al. TOSEM 2024 |
| 9 | MetaGPT — essential framework, ICLR 2024 |
| 10 | ChatDev — essential framework, ACL 2024 |
| 11 | AutoGen — most adopted framework |
| 13 | Agentless — critical counterpoint / challenges agent complexity |
| 16 | SWE-Bench Pro — state-of-the-art benchmark |
| 18 | Agentic SE Roadmap — future directions |

### Strong Candidates (add 4–6 from these)
| # | Adds |
|---|------|
| 3 | Distinguishes LLM vs. agent — good for background |
| 6 | Benchmark landscape survey (150+ papers) |
| 7 | Design patterns (16 patterns) — architectural depth |
| 8 | Evaluation survey — ACL-published, high quality |
| 12 | AgentCoder — concrete code generation results |
| 14 | ALMAS — most recent agile-aligned framework (2025) |
| 17 | SALLMA — architectural design angle |
| 21 | Agile SE framework — ToM + SAFe integration, novel angle |
| 23 | ICSE 2025 — top venue, 200%+ improvement on design issue localization |

### Lower Priority (drop if over limit)
| # | Reason |
|---|--------|
| 4 | Broad MAS survey — less SE-specific |
| 5 | Foundational but 2023 — may be redundant with newer surveys |
| 15 | Early 2023 — historical context only |
| 22 | Requirements analysis — narrow application; small dataset (12 stories) |
| 24 | Conceptual only — no implementation; lower-tier venue |
| 25 | IBM demo — trivial code tested; no comparison to EvoSuite/Randoop |

---

## Suggested Thematic Structure for the Review

```
1. Introduction
   - Why multi-agent SE? (Papers 18, 1)

2. Background
   - What are LLM-based agents? (Papers 5, 3)
   - Taxonomy of approaches (Papers 7, 4)

3. Main Body
   A. Frameworks & Systems (Papers 9, 10, 11, 12, 14)
   B. Benchmarks & Evaluation (Papers 16, 6, 8)
   C. The complexity debate: agents vs. agentless (Papers 13 vs. 9/10)

4. Discussion
   - Gaps: evaluation standards, trust, scalability (Papers 8, 19, 18)
   - Future directions (Paper 18)

5. Conclusion
```

---

*Last updated: 2026-05-08 | Papers read: 25/25 | PDFs pending: 0*
