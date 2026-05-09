# Multi-Agent LLM Systems for Software Engineering: A Literature Review

**CS 7980 Capstone | Northeastern University | Li Qingman | 2026-05-09**

---

## 1. Introduction

Software engineering is undergoing a structural transformation. The emergence of large language models (LLMs) capable of generating, reviewing, and refactoring code has shifted agent-based computing from theoretical curiosity to practical infrastructure. Yet single-agent systems — one model, one task — have proven insufficient for the complexity of real software projects. The field has consequently converged on **multi-agent architectures**, in which specialized LLM-powered agents collaborate across the software development lifecycle (SDLC): planning, coding, testing, debugging, and maintenance.

Hassan et al. [13] frame this shift as "SE 3.0," coining *Structured Agentic Software Engineering* (SASE) and arguing that fully autonomous engineering teams represent the trajectory of the discipline. He, Treude, and Lo [2] confirm the scope of this transformation by surveying 41 primary studies and mapping LLM-based multi-agent (LMA) systems across every SDLC stage. This review synthesizes fifteen papers (2023–2025) to answer the central question: *How are LLM-based multi-agent systems designed and applied across the SDLC, and what are the key open challenges?*

---

## 2. Background: From LLM Agents to Multi-Agent Systems

Wang et al. [1] establish the foundational vocabulary: a single LLM-based agent comprises four interacting modules — **Profile** (role and persona), **Memory** (context storage), **Planning** (goal decomposition), and **Action** (tool use and code execution). This framework, cited over 2,000 times, underpins virtually every subsequent multi-agent design.

Moving from single to multi-agent systems multiplies both capability and complexity. Guo et al. [4] survey this evolution in depth, documenting how LLM-MA systems advance beyond single-agent planning through mechanisms of **agent profiling**, **inter-agent communication**, and **skill specialization**. They identify three principal communication topologies — layered, decentralized, and centralized — each with distinct implications for coordination overhead and failure propagation. Talebirad and Nadiri [11], writing in mid-2023 when the field was nascent, anticipated precisely this taxonomy and flagged challenges — agent looping, context overflow, and trust between agents — that the literature has since confirmed as critical. Together, these three foundational works establish that the power of multi-agent SE comes at the cost of coordination complexity.

---

## 3. Current Approaches

### 3.1 Frameworks and Coordination Paradigms

The literature clusters around two dominant paradigms for multi-agent coordination in software tasks.

**Structured-document coordination** is exemplified by MetaGPT [5], which encodes software engineering workflows as *Standardized Operating Procedures* (SOPs). Agents are assigned canonical software roles — product manager, architect, engineer, QA — and communicate through structured artifacts (PRDs, design docs, test reports) rather than free-form dialogue. This approach reduces hallucination and role confusion by making intermediate products explicit and inspectable. MetaGPT achieves 85.9% on HumanEval, establishing the structured-document approach as the field's reference point for complex software generation.

**Dialogue-based coordination** is represented by ChatDev [6], which organizes agent interaction as a *Chat Chain* of role-playing conversations between pairs of agents (CEO↔CTO, programmer↔tester). Rather than pre-defined artifact schemas, agents reach consensus through natural language. ChatDev's system generates working small-scale software from a single natural-language specification, demonstrating that conversational coordination can substitute for structural constraints when tasks are well-scoped.

**General-purpose infrastructure** bridges both paradigms. AutoGen [7] provides a conversation-based abstraction layer in which any pair of agents can exchange messages, delegate subtasks, or invoke tools — making it the backbone of dozens of task-specific systems. Unlike MetaGPT and ChatDev, AutoGen makes no assumption about the SE domain, positioning it as infrastructure rather than application.

**Iterative feedback loops** add a third pattern. AgentCoder [8] deploys a three-agent pipeline — programmer, test designer, executor — in which generated code is repeatedly tested and refined until all test cases pass. This achieves 96.3% Pass@1 on HumanEval with GPT-4, the strongest code-generation result in the reviewed corpus, and illustrates that tight feedback cycles can substitute for architectural complexity.

### 3.2 The Complexity Paradox

A significant counterpoint to the frameworks above is *Agentless* [9]. Rather than orchestrating autonomous agent decisions, Agentless applies a deterministic three-phase pipeline — fault localization, candidate patch generation, patch selection — with no agent planning or tool-calling autonomy. Despite this simplicity, it achieves **50.80% on SWE-bench** (with Claude 3.5 Sonnet), a state-of-the-art result that outperforms more complex autonomous agent systems at lower API cost. OpenAI and DeepSeek have since adopted this approach as a standard evaluation baseline.

Agentless raises a question the field has not yet answered: *When does architectural complexity pay off?* The absence of a principled theory for when to add agent autonomy versus when to use structured pipelines is itself a research gap.

### 3.3 Landscape Surveys and Design Guidance

Two TOSEM-quality surveys map the SE agent landscape empirically. He et al. [2] synthesize 41 primary studies and propose a lifecycle taxonomy; Liu et al. [3] analyze 124 papers through a dual lens of SE-task coverage and agent architecture, identifying perception, reasoning, tool use, and inter-agent interaction as the core capability dimensions. Both surveys observe that the field is growing faster than existing reviews can capture — Liu et al.'s corpus alone spans a span of just 18 months.

Cai et al. [14] complement these surveys with a practitioner-oriented contribution: a systematic derivation of **16 design patterns** for LLM-based multi-agent SE systems (e.g., Role Specialization, Debate, Blackboard), grounded in a 94-paper review and mapped to ISO 25010 quality attributes. Where He et al. and Liu et al. document *what* has been built, Cai et al. address *how to build it* — a distinction that matters as the field transitions from research prototypes to production systems.

---

## 4. Challenges and Evaluation

Despite rapid progress, the field faces critical open problems. Han et al. [10] enumerate four challenge dimensions from a systems perspective: (1) **task allocation** — matching subtasks to the most capable agent efficiently; (2) **robust reasoning** — preventing cascading errors through iterative multi-agent debate; (3) **context management** — handling layered context that grows with agent count and dialogue length; and (4) **memory** — enabling agents to maintain and retrieve long-horizon state without exceeding token budgets. These challenges are empirically observed, not hypothetical — they appear as failure modes in deployed MetaGPT, ChatDev, and AutoGen systems.

Evaluation methodology is arguably the field's most urgent bottleneck. Yehudai et al. [12] (ACL Findings 2025) survey agent evaluation frameworks and find that benchmark coverage is shallow, metrics are often self-reported, and no community-wide evaluation standard exists. SWE-bench has emerged as the de facto benchmark for repository-level tasks, but it samples from open-source bug-fix scenarios that may not reflect enterprise software complexity. The result is a landscape in which performance claims are difficult to compare and progress is hard to verify — a problem that will grow more acute as commercial systems enter production.

---

## 5. Conclusion and Future Directions

The last three years have established LLM-based multi-agent software engineering as a coherent research area with genuine results: frameworks completing small software projects end-to-end, code generation approaching human-competitive benchmarks, and surveys documenting a rapidly expanding primary literature. Two paradigms — structured-document (MetaGPT) and dialogue-based (ChatDev) coordination — anchor current system design, while the Agentless result challenges the field to be more precise about when agent complexity is justified.

What the field lacks is equally clear. Evaluation methodology is immature; coordination challenges (task allocation, context overflow, memory) remain unsolved at scale; and the gap between benchmark performance (~50% on SWE-bench) and the fully autonomous engineering vision articulated by Hassan et al. [13] is substantial. The most pressing near-term research directions are: standardized evaluation protocols for agent systems, hybrid architectures that modulate autonomy based on task complexity, and safety and governance frameworks for agents operating with write access to production codebases [13, 12].

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
