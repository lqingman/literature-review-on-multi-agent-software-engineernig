# Multi-Agent LLM Systems for Software Engineering: A Literature Review

**CS 7980 Capstone | Northeastern University | Li Qingman | 2026-05-09**

---

## 1. Introduction

Software engineering is undergoing a structural transformation. The emergence of large language models (LLMs) capable of generating, reviewing, and refactoring code has shifted agent-based computing from theoretical curiosity to practical infrastructure. Yet single-agent systems — one model, one task — have proven insufficient for the complexity of real software projects. The field has consequently converged on **multi-agent architectures**, in which specialized LLM-powered agents collaborate across the full software development lifecycle (SDLC): planning, coding, testing, debugging, and maintenance.

This transformation matters because software complexity is not diminishing. Enterprise codebases span millions of lines, involve continuous integration pipelines, and require coordination across specializations that no single model can reliably master. Multi-agent systems promise to decompose this complexity, assigning subtasks to specialized agents whose outputs are integrated into coherent software artifacts.

This review synthesizes fifteen papers (2023–2025), spanning surveys, framework designs, and empirical evaluations, to answer: *How are LLM-based multi-agent systems designed and applied across the SDLC, and what are the key open challenges?* Papers were selected by cross-validating two independent search workflows — Claude-assisted deep analysis and Consensus database search — producing a corpus of ~6,300 combined citations across top venues including ICLR, ACL, and ACM TOSEM.

---

## 2. Background and Foundations

Wang et al. [1] establish the foundational vocabulary: a single LLM-based agent comprises four interacting modules — **Profile** (role and persona), **Memory** (context storage), **Planning** (goal decomposition), and **Action** (tool use and code execution). This architecture, cited over 2,000 times, underpins virtually every subsequent multi-agent design and defines the terminology used across the literature.

The transition from single to multi-agent systems is surveyed in depth by Guo et al. [4], who document the evolution through **agent profiling**, **inter-agent communication**, and **skill specialization**, identifying three principal communication topologies — layered, decentralized, and centralized. Talebirad and Nadiri [11], writing in mid-2023 when the field was nascent, represent the earliest systematic treatment of multi-agent LLM collaboration and anticipated the coordination challenges — looping, context overflow, inter-agent trust — that subsequent empirical work has confirmed. Together, these three foundational works establish that the capability gains from multi-agent decomposition come at the cost of coordination complexity.

---

## 3. Main Body

### 3.1 Current Approaches and Methods

The literature clusters around four patterns for multi-agent coordination in software tasks.

**Structured-document coordination** is exemplified by MetaGPT [5], which encodes SE workflows as *Standardized Operating Procedures* (SOPs). Agents hold canonical roles — product manager, architect, engineer, QA — and communicate through structured artifacts (PRDs, design docs, test reports) rather than free-form dialogue. Making intermediate products explicit reduces hallucination and role confusion. **Dialogue-based coordination** is represented by ChatDev [6], which organizes agent interaction as a *Chat Chain* of role-playing conversations between agent pairs (CEO↔CTO, programmer↔tester). Agents reach consensus through natural language rather than pre-defined schemas, demonstrating that conversational coordination can substitute for structural constraints in well-scoped tasks. **General-purpose infrastructure** is provided by AutoGen [7], a conversation-based abstraction layer in which any pair of agents can exchange messages, delegate subtasks, or invoke tools — positioning it as backbone infrastructure rather than a domain-specific application. **Iterative feedback loops** are illustrated by AgentCoder [8], which deploys a three-agent pipeline — programmer, test designer, executor — in which code is repeatedly tested and refined until all test cases pass, achieving 96.3% Pass@1 on HumanEval with GPT-4.

### 3.2 Recent Advances

Three developments from 2024–2025 represent the leading edge of the field. First, *Agentless* [9] challenges the prevailing assumption that more agentic complexity yields better performance. By replacing autonomous agent decision-making with a deterministic three-phase pipeline — fault localization, patch generation, patch selection — it achieves **50.80% on SWE-bench** with Claude 3.5 Sonnet, a state-of-the-art result adopted by OpenAI and DeepSeek as a standard evaluation baseline. Second, Cai et al. [14] deliver the field's first systematic catalog of **16 design patterns** for LLM-based multi-agent SE systems (e.g., Role Specialization, Debate, Blackboard), grounded in a 94-paper review and mapped to ISO 25010 quality attributes — moving the field from ad hoc design toward principled software architecture. Third, Yehudai et al. [12] produce the first dedicated survey of agent evaluation methodology, finding that no community-wide evaluation standard exists and that most published metrics are task-specific and self-reported.

### 3.3 Comparative Analysis

Placing these approaches side by side reveals three substantive tensions in the literature.

**Structured vs. dialogue coordination.** MetaGPT and ChatDev represent opposite design philosophies. MetaGPT's SOPs impose structure that catches inconsistencies early but require upfront role schema design and limit flexibility. ChatDev's Chat Chain is more adaptive but scales poorly as conversation depth grows, accumulating context that exceeds token budgets. Neither approach dominates: MetaGPT excels on complex multi-file generation; ChatDev produces working code faster for single-feature specifications. Liu et al. [3] note this as a fundamental trade-off between reliability and flexibility across the 124-paper corpus they survey.

**Autonomy vs. simplicity.** Agentless [9] directly challenges the agentic frameworks by outperforming them with no autonomy whatsoever on the SWE-bench benchmark. This is not a niche result — the gap holds across model variants. Yet the comparison is not clean: SWE-bench tests bug-fix localization, where deterministic pipelines excel; open-ended feature development, where frameworks like MetaGPT [5] and AutoGen [7] operate, is not well represented in any current benchmark. The comparison reveals more about benchmark design limitations than about which architecture is superior in general.

**Benchmark coverage gaps.** HumanEval (used by AgentCoder and MetaGPT) tests isolated function generation; SWE-bench (used by Agentless) tests repository-level bug fixing. He et al. [2] map 41 primary studies across the SDLC and find that requirements engineering, architecture design, and deployment are almost entirely absent from existing benchmarks, despite being the phases where coordination overhead is highest. The field's comparative analysis is therefore conducted on a narrow slice of the SE domain.

---

## 4. Discussion

The reviewed literature tells a coherent story: the field moved rapidly from single-agent code generation (2022–2023) to structured multi-agent frameworks (MetaGPT, ChatDev, AutoGen; 2023–2024) and is now questioning whether that complexity was always warranted (Agentless, 2024–2025). Two coordination paradigms — structured-document and dialogue-based — have emerged as the dominant architectural choices, with a growing recognition that design patterns [14] and principled architecture selection criteria are needed to guide practitioners. Surveys by He et al. [2] and Liu et al. [3] confirm that the primary literature is expanding faster than review coverage can keep pace.

Three gaps stand out. First, **evaluation standardization**: Yehudai et al. [12] and Han et al. [10] both identify the absence of agreed-upon metrics as the field's most critical bottleneck. Performance claims across frameworks are currently incommensurable. Second, **coordination at scale**: Han et al. [10] enumerate unresolved challenges — task allocation, cascading reasoning errors, context overflow, long-horizon memory — that appear as observed failure modes in deployed systems, not as hypothetical concerns. Third, **SDLC coverage**: the combination of He et al. [2] and Liu et al. [3] reveals that current agent research covers less than half the SDLC, leaving requirements elicitation, architecture, and maintenance nearly untouched.

The most consequential near-term directions are: (1) standardized evaluation protocols that span SDLC phases rather than isolated coding tasks; (2) hybrid architectures that dynamically select between structured-pipeline and autonomous-agent modes based on task complexity; and (3) safety and governance frameworks for agents that operate with write access to production systems, a concern Hassan et al. [13] identify as foundational to the SASE vision.

---

## 5. Conclusion

LLM-based multi-agent SE has evolved in three years from a research concept to a field with peer-reviewed frameworks, quantitative benchmarks, and systematic surveys. The central finding is a **complexity paradox**: architecturally simple pipelines (Agentless) match or outperform elaborate agent orchestration on current benchmarks, while complex frameworks (MetaGPT, AutoGen) address design problems that benchmarks do not yet test. The field is productive but fragmented — growing faster than its evaluation methodology can validate.

This review provides five concrete design lessons related to our future work. (1) **Start with the simplest pipeline that could work.** Agentless [9] demonstrates that a deterministic three-phase pipeline can outperform autonomous agents on bug-fixing tasks; build the structured version first and add autonomy only where static pipelines demonstrably fail. (2) **Choose coordination paradigm based on task type.** If the capstone targets complex, multi-file generation (e.g., full feature development), MetaGPT's SOP-based structured-document approach [5] provides better error containment; if the task is exploratory or single-scoped, ChatDev's dialogue chain [6] is faster to implement. (3) **Use AutoGen as infrastructure rather than building from scratch.** AutoGen [7] provides a tested conversation abstraction layer that avoids reimplementing agent message routing and tool invocation — the capstone can focus engineering effort on task-specific agent roles instead. (4) **Design the evaluation framework before writing any agent code.** Yehudai et al. [12] and Han et al. [10] show that the field's credibility problem stems from post-hoc, task-specific metrics. The capstone should identify its benchmark (SWE-bench subset, HumanEval, or a custom dataset) and success criteria upfront so that design decisions are anchored to measurable outcomes. (5) **Engineer for Han et al.'s four failure modes from day one.** Task allocation collisions, cascading reasoning errors, context overflow, and memory loss [10] are not edge cases — they appear in deployed MetaGPT and AutoGen systems under realistic load. Addressing them requires explicit design choices: a task-routing layer, structured intermediate artifacts, context windowing, and an external memory store. Treating these as afterthoughts is the most common reason multi-agent prototypes fail to scale beyond demo tasks.

---

## References

[1] L. Wang, C. Ma, X. Feng, Z. Zhang, et al. "A Survey on Large Language Model based Autonomous Agents." *Frontiers of Computer Science*, 2024. arXiv:2308.11432.

[2] J. He, C. Treude, D. Lo. "LLM-Based Multi-Agent Systems for Software Engineering: Literature Review, Vision, and the Road Ahead." *ACM Trans. Software Eng. Methodol.* (TOSEM), 2025. DOI: 10.1145/3712003.

[3] J. Liu, K. Wang, Y. Chen, X. Peng, Z. Chen, L. Zhang, Y. Lou. "Large Language Model-Based Agents for Software Engineering: A Survey." *ACM Trans. Software Eng. Methodol.* (TOSEM), 2024. DOI: 10.48550/arxiv.2409.02977.

[4] T. Guo, X. Chen, Y. Wang, R. Chang, S. Pei, N. Chawla, O. Wiest, X. Zhang. "Large Language Model based Multi-Agents: A Survey of Progress and Challenges." arXiv:2402.01680, 2024.

[5] S. Hong, X. Zheng, J. P. Chen, et al., C. Wu. "MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework." *ICLR 2024*. DOI: 10.48550/arxiv.2308.00352.

[6] C. Qian, W. Liu, H. Liu, N. Chen, et al., M. Sun. "ChatDev: Communicative Agents for Software Development." *ACL 2024*. DOI: 10.18653/v1/2024.acl-long.810.

[7] Q. Wu, G. Bansal, J. Zhang, Y. Wu, et al., C. Wang. "AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation." arXiv:2308.08155, 2023. Microsoft Research.

[8] D. Huang, Q. Bu, J. M. Zhang, M. Luck, H. Cui. "AgentCoder: Multi-Agent-based Code Generation with Iterative Testing and Optimisation." arXiv:2312.13010, 2023.

[9] C. S. Xia, Y. Deng, S. Dunn, L. Zhang. "Agentless: Demystifying LLM-based Software Engineering Agents." *Proc. ACM Software Eng.* (PACMSE/FSE 2025). DOI: 10.1145/3715754.

[10] S. Han, Q. Zhang, Y. Yao, W. Jin, Z. Xu, C. He. "LLM Multi-Agent Systems: Challenges and Open Problems." arXiv:2402.03578, 2024.

[11] Y. Talebirad, A. Nadiri. "Multi-Agent Collaboration: Harnessing the Power of Intelligent LLM Agents." arXiv:2306.03314, 2023.

[12] A. Yehudai, L. Eden, A. Li, G. Uziel, Y. Zhao, et al. "Survey on Evaluation of LLM-based Agents." *ACL Findings 2025*. arXiv:2503.16416.

[13] A. E. Hassan, H. Li, D. Lin, B. Adams, et al. "Agentic Software Engineering: Foundational Pillars and a Research Roadmap." arXiv:2509.06216, 2025.

[14] Y. Cai, R. Li, P. Liang, M. Shahin, Z. Li. "Designing LLM-based Multi-Agent Systems for SE Tasks: Quality Attributes, Design Patterns and Rationale." arXiv:2511.08475, 2025.
