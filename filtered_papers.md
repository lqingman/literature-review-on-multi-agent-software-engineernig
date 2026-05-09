# Filtered Papers — Multi-Agent LLM Software Engineering
## Cross-Validated Selection: paper_summaries.md × consensus.csv

**Date:** 2026-05-09  
**Method:** Cross-check between Claude-curated summaries (25 papers) and Consensus tool results (50 papers). Papers appearing in both sources receive highest confidence; papers from one source are retained or dropped based on citation count, venue quality, and coverage gap analysis.  
**Final count:** 15 papers selected for the review  
**Scope:** LLM-era multi-agent software engineering (2023–2026), with foundational pre-LLM references where essential

---

## Cross-Check Legend

| Symbol | Meaning |
|--------|---------|
| ✅ BOTH | Appears in paper_summaries.md AND consensus.csv — highest confidence |
| 📄 SUMMARY | In paper_summaries.md only — retained based on citation authority |
| 🔍 CONSENSUS | In consensus.csv only — newly added or elevated |
| ❌ DROPPED | Was in paper_summaries.md; removed after cross-check |

---

## Summary of Cross-Check Findings

### Critical Gap Found
**Guo et al. 2024** — "Large Language Model based Multi-Agents: A Survey of Progress and Challenges" — has **761 citations** and appeared in the Consensus search results (consensus.csv row 8) but was entirely absent from paper_summaries.md. This is the third most-cited paper in the entire consensus dataset and must be included.

### Papers Confirmed by Both Sources
Six papers appear in both sources, giving the strongest selection confidence:
MetaGPT, ChatDev, AgentCoder, He et al. 2025 (TOSEM survey), Liu et al. 2024 (TOSEM survey), and Cinkusz & Chudziak 2024 (CogniSim/Agile).

### Papers in Summaries but Absent from Consensus — Kept
AutoGen (851 cites), Agentless (400+ cites), and Wang et al. 2023 (2,011 cites) did not surface in the Consensus search but have citation counts that establish field consensus independently. Their absence from the Consensus results reflects query scope, not lack of importance.

### Papers Dropped After Cross-Check
Papers 14 (ALMAS), 17 (SALLMA), 24 (Rajendran), and 25 (Garlapati) had zero consensus support and weak venue/empirical standing. Paper 4 (Chen et al. 2024, 29 cites) is superseded by the newly identified Guo et al. 2024 (761 cites) for the general MAS survey slot.

---

## Section 1: Survey Papers (4 papers)

---

### S1 — A Survey on Large Language Model based Autonomous Agents
🔍 CONSENSUS · Source: consensus.csv row 5 (Wang et al. 2023) — also **SUMMARY paper 5**  
✅ BOTH (consensus entry is Wang et al. 2024 "Agents in SE" Q2 journal; summaries has Wang et al. 2023 foundational)

> **NOTE:** Two distinct Wang et al. papers exist. Both are retained:
> - Wang 2023 (paper_summaries.md #5) = foundational agent framework (2,011 cites)
> - Wang et al. 2024 "Agents in SE: survey" (consensus.csv row 7) = SE-specific survey (55 cites, Q2 journal)
> For a 2-page review, use Wang 2023 as the foundational reference and mention Wang 2024 in passing.

| Field | Details |
|-------|---------|
| **BibTeX key** | Wang2023autonomousagents |
| **Authors** | Lei Wang, Chen Ma, Xueyang Feng, Zeyu Zhang, et al. |
| **Year** | 2023 (published Frontiers of Computer Science 2024) |
| **Venue** | Frontiers of Computer Science |
| **Citations** | **2,011** ✓ |
| **Cross-check status** | 📄 SUMMARY — foundational reference retained |
| **Consensus link** | Not surfaced (query scope) |

**Why keep:** Highest citation count in the entire corpus. Establishes the core agent architecture vocabulary (Profile / Memory / Planning / Action) cited by virtually every subsequent paper. Essential for Background section when defining what an "agent" is.

**Role in review:** Background/Foundations — defines agents before multi-agent SE is introduced.

---

### S2 — LLM-Based Multi-Agent Systems for Software Engineering: Literature Review, Vision, and the Road Ahead
✅ BOTH

| Field | Details |
|-------|---------|
| **BibTeX key** | He2025literaturereview |
| **Authors** | Junda He, Christoph Treude, David Lo |
| **Year** | 2025 (accepted TOSEM; arXiv submitted 2024) |
| **Venue** | ACM Transactions on Software Engineering and Methodology (Q1) |
| **Citations** | 144 (consensus.csv) |
| **DOI** | 10.1145/3712003 |
| **Cross-check status** | ✅ BOTH — high confidence |
| **Consensus link** | https://consensus.app/papers/llmbased-multiagent-systems-for-software-engineering-he-treude/797515474cd8578d87cee4eb3231428a/ |

**Why keep:** The most directly scoped systematic review for this topic. TOSEM peer-reviewed. Covers 41 primary studies across the full SDLC. Maps LMA systems to software development lifecycle stages and proposes a research agenda.

**Role in review:** Primary organizing framework; cite for definition of LMA systems and SDLC taxonomy.

---

### S3 — Large Language Model-Based Agents for Software Engineering: A Survey
✅ BOTH

| Field | Details |
|-------|---------|
| **BibTeX key** | Liu2024agentssurvey |
| **Authors** | Junwei Liu, Kaixin Wang, Yixuan Chen, Xin Peng, Zhenpeng Chen, Lingming Zhang, Yiling Lou |
| **Year** | 2024 |
| **Venue** | ACM Transactions on Software Engineering and Methodology (Q1) |
| **Citations** | 151 (consensus.csv) |
| **DOI** | 10.48550/arxiv.2409.02977 |
| **Cross-check status** | ✅ BOTH — high confidence |
| **Consensus link** | https://consensus.app/papers/large-language-modelbased-agents-for-software-liu-wang/3fbdb20e973e517ea06d082a67a7e4cf/ |

**Why keep:** Broadest paper corpus (124 papers); dual-perspective analysis (SE task view + agent architecture view). TOSEM quality. Complements He et al. by covering agent capabilities (perception, tool use, multi-agent interaction) separately from SDLC mapping.

**Role in review:** Background — provides breadth and dual-perspective categorization.

---

### S4 — Large Language Model based Multi-Agents: A Survey of Progress and Challenges ⭐ NEWLY ADDED
🔍 CONSENSUS — was missing from paper_summaries.md

| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2024massurvey |
| **Authors** | Taicheng Guo, Xiuying Chen, Yaqi Wang, Ruidi Chang, Shichao Pei, N. Chawla, Olaf Wiest, Xiangliang Zhang |
| **Year** | 2024 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | **761** ✓ — third highest in the entire corpus |
| **DOI** | 10.48550/arxiv.2402.01680 |
| **Cross-check status** | 🔍 CONSENSUS — critical addition |
| **Consensus link** | https://consensus.app/papers/large-language-model-based-multiagents-a-survey-of-guo-chen/2aee6910ec3455fe8fcd0a6b0392f01e/ |

**Why add:** 761 citations makes this the third most-cited paper in the consensus dataset, yet it was entirely absent from paper_summaries.md. It provides an in-depth discussion of the essential aspects of LLM-based multi-agent systems: domains and settings, profiling and communication methods, and skill development mechanisms. Covers complex problem-solving and world simulation applications. The high citation count signals it has become a de facto reference in the field.

**Key content:** Surveys LLM-MA systems evolving from single-agent planning to multi-agent systems; discusses agent profiling, communication methods, and skill development; includes datasets/benchmarks; maintains an open-source paper repository.

**Role in review:** Background/Foundations — place alongside Wang 2023 as the two foundational surveys; covers multi-agent-specific aspects that Wang 2023 treats more generally.

**⚠️ Note for paper_summaries.md:** This paper was misidentified or confused with Chen et al. 2024 (29 cites) in the original summaries. Guo et al. 2024 and Chen et al. 2024 are **different papers**. Guo et al. should replace Chen et al. in the final selection.

---

## Section 2: Frameworks & Systems (5 papers)

---

### F1 — MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework
✅ BOTH

| Field | Details |
|-------|---------|
| **BibTeX key** | Hong2023metagpt |
| **Authors** | Sirui Hong, Xiawu Zheng, Jonathan P. Chen, et al., Chenglin Wu |
| **Year** | 2023 (ICLR 2024) |
| **Venue** | ICLR 2024 |
| **Citations** | **1,475** (consensus.csv) |
| **DOI** | 10.48550/arxiv.2308.00352 |
| **Cross-check status** | ✅ BOTH — highest consensus |
| **Consensus link** | https://consensus.app/papers/metagpt-meta-programming-for-multiagent-collaborative-hong-zheng/438146366118587eb033ac13d59d8b30/ |

**Why keep:** The highest-cited SE-specific multi-agent framework. Introduces Standardized Operating Procedures (SOPs) as meta-programming for LLM agents — the canonical role-based, structured-document approach. ICLR peer-reviewed. Referenced in virtually every subsequent framework paper.

**Role in review:** Frameworks section — the primary example of structured-document agent coordination.

---

### F2 — ChatDev: Communicative Agents for Software Development
✅ BOTH

| Field | Details |
|-------|---------|
| **BibTeX key** | Qian2023chatdev |
| **Authors** | Cheng Qian, Wei Liu, Hongzhang Liu, Nuo Chen, et al., Maosong Sun |
| **Year** | 2023 (ACL 2024) |
| **Venue** | ACL 2024 |
| **Citations** | **603** (consensus.csv) |
| **DOI** | 10.18653/v1/2024.acl-long.810 |
| **Cross-check status** | ✅ BOTH — high confidence |
| **Consensus link** | https://consensus.app/papers/chatdev-communicative-agents-for-software-development-qian-liu/bd7abf58c62958e2a4c6c63f911bdab4/ |

**Why keep:** Second most-cited SE framework. Introduces the Chat Chain structure and natural-language-based agent coordination. ACL peer-reviewed. Paired with MetaGPT, these two illustrate the dominant coordination paradigms (structured docs vs. dialogue) at the center of the literature.

**Role in review:** Frameworks section — contrast with MetaGPT; illustrates natural language coordination approach.

---

### F3 — AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation
📄 SUMMARY (not in consensus.csv — search scope)

| Field | Details |
|-------|---------|
| **BibTeX key** | Wu2023autogen |
| **Authors** | Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, et al., Chi Wang |
| **Year** | 2023 |
| **Venue** | arXiv (cs.AI); Microsoft Research |
| **Citations** | **851** ✓ |
| **DOI** | arXiv:2308.08155 |
| **Cross-check status** | 📄 SUMMARY — retained based on 851 citation count |

**Why keep despite missing from consensus:** 851 citations is the second highest framework citation count. AutoGen is the most widely adopted multi-agent framework in practice, used as backbone in many systems (ALMAS variants, research prototypes). Its absence from consensus.csv reflects query specificity, not lack of relevance.

**Role in review:** Frameworks section — general-purpose infrastructure layer vs. task-specific frameworks (MetaGPT, ChatDev).

---

### F4 — AgentCoder: Multi-Agent-based Code Generation with Iterative Testing and Optimisation
✅ BOTH

| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2023agentcoder |
| **Authors** | Dong Huang, Qingwen Bu, Jie M. Zhang, Michael Luck, Heming Cui |
| **Year** | 2023 |
| **Venue** | arXiv (cs.CL) |
| **Citations** | **312** (consensus.csv) |
| **DOI** | 10.48550/arxiv.2312.13010 |
| **Cross-check status** | ✅ BOTH — high confidence |
| **Consensus link** | https://consensus.app/papers/agentcoder-multiagentbased-code-generation-with-huang-bu/2c5b0ab8b7465224a3d62a2ffc132ade/ |

**Why keep:** 312 citations; best benchmark results (96.3% Pass@1 HumanEval with GPT-4) among code generation agents. Three-agent programmer-tester-executor feedback loop is the canonical iterative refinement pattern. Provides concrete quantitative benchmark numbers for the review.

**Role in review:** Frameworks section — demonstrates feedback-loop agent pattern for code generation.

---

### F5 — Agentless: Demystifying LLM-based Software Engineering Agents (PACMSE)
📄 SUMMARY (not in consensus.csv — absent from Consensus search)

| Field | Details |
|-------|---------|
| **BibTeX key** | Xia2025demystify |
| **Authors** | Chunqiu Steven Xia, Yinlin Deng, Soren Dunn, Lingming Zhang |
| **Year** | 2025 (journal); 2024 (arXiv preprint) |
| **Venue** | Proc. ACM Software Engineering (PACMSE/FSE 2025) — peer-reviewed |
| **Citations** | ~400 (arXiv preprint) + ~80 (journal version) |
| **DOI** | 10.1145/3715754 |
| **Cross-check status** | 📄 SUMMARY — retained as essential critical counterpoint |

**Why keep despite missing from consensus:** The critical counterpoint to complex agent architectures. Achieves state-of-the-art SWE-bench performance (50.80% with Claude 3.5 Sonnet) using a simple three-phase pipeline without autonomous agent decision-making. Adopted by OpenAI and DeepSeek as standard evaluation approach. The consensus search likely missed it due to the "agentless" keyword not matching "multi-agent" queries — which is precisely the intellectual contribution of this paper.

**Role in review:** Critical discussion — the complexity vs. simplicity debate; challenges assumptions about when agent complexity is beneficial.

---

## Section 3: Challenges & Evaluation (3 papers)

---

### C1 — LLM Multi-Agent Systems: Challenges and Open Problems ⭐ NEWLY ELEVATED
🔍 CONSENSUS — not in paper_summaries.md

| Field | Details |
|-------|---------|
| **BibTeX key** | Han2024challenges |
| **Authors** | Shanshan Han, Qifan Zhang, Yuhang Yao, Weizhao Jin, Zhaozhuo Xu, Chaoyang He |
| **Year** | 2024 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | **124** (consensus.csv) |
| **DOI** | 10.48550/arxiv.2402.03578 |
| **Cross-check status** | 🔍 CONSENSUS — added based on citation count and thematic gap |
| **Consensus link** | https://consensus.app/papers/llm-multiagent-systems-challenges-and-open-problems-han-zhang/11595386be7351c0a6bd198c3736c39e/ |

**Why add:** 124 citations with specific focus on challenges and open problems — a thematic area with no direct equivalent in the original 25-paper summaries. Identifies four critical challenge dimensions: (1) task allocation optimization, (2) robust reasoning through iterative debate, (3) managing complex layered context, (4) enhancing memory management. The paper also explores multi-agent system applications in blockchain/distributed systems, extending the SE scope. The challenges perspective directly supports the Discussion/Gaps section.

**Key content:** Task allocation across agents with diverse capabilities and roles; fostering robust reasoning through iterative multi-agent debates; managing complex layered context information; memory management for intricate multi-agent interactions.

**Role in review:** Discussion/Gaps section — authoritative enumeration of open challenges from a mid-2024 perspective; pairs with Hassan et al. 2025 roadmap to show challenges → proposed solutions arc.

---

### C2 — Multi-Agent Collaboration: Harnessing the Power of Intelligent LLM Agents
📄 SUMMARY

| Field | Details |
|-------|---------|
| **BibTeX key** | Talebirad2023collaboration |
| **Authors** | Yashar Talebirad, Amirhossein Nadiri |
| **Year** | 2023 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | **282** ✓ |
| **DOI** | arXiv:2306.03314 |
| **Cross-check status** | 📄 SUMMARY — retained based on 282 citations and historical significance |

**Why keep:** One of the earliest frameworks for multi-agent LLM collaboration (June 2023); 282 citations signals field recognition. Identifies challenges (looping, security, scalability, evaluation, ethics) that remain unsolved as of 2025, providing historical continuity for the narrative. Case studies include Auto-GPT and BabyAGI — precursors to modern agent frameworks.

**Role in review:** Background — establishes the field's early recognition of coordination challenges; bridges pre-LLM multi-agent systems and the modern era.

---

### C3 — Survey on Evaluation of LLM-based Agents
📄 SUMMARY

| Field | Details |
|-------|---------|
| **BibTeX key** | Yehudai2025evalsurvey |
| **Authors** | Asaf Yehudai, Lilach Eden, Alan Li, Guy Uziel, Yilun Zhao, et al. |
| **Year** | 2025 |
| **Venue** | ACL Findings 2025 |
| **Citations** | **67** ✓ (strong for a 2025 paper) |
| **DOI** | arXiv:2503.16416 |
| **Cross-check status** | 📄 SUMMARY — retained; ACL peer-reviewed; fills unique evaluation gap |

**Why keep:** The only paper in the final set dedicated entirely to evaluation methodology. ACL Findings peer-reviewed; 67 citations for a 2025 paper is strong. Identifies the lack of standardized evaluation approaches as a major bottleneck. Essential for connecting benchmarks (SWE-bench) to the broader question of how to rigorously evaluate agent performance. No equivalent in consensus.csv — the consensus search focused on SE tasks rather than evaluation methodology.

**Role in review:** Discussion/Gaps — establishes evaluation as an open problem; pairs with SWE-bench and Han et al. challenges.

---

## Section 4: Vision & Architecture (2 papers)

---

### V1 — Agentic Software Engineering: Foundational Pillars and a Research Roadmap
📄 SUMMARY

| Field | Details |
|-------|---------|
| **BibTeX key** | Hassan2025agenticroadmap |
| **Authors** | Ahmed E. Hassan, Hao Li, Dayi Lin, Bram Adams, et al. |
| **Year** | 2025 |
| **Venue** | arXiv (cs.SE) |
| **Citations** | ~40 |
| **DOI** | arXiv:2509.06216 |
| **Cross-check status** | 📄 SUMMARY — retained as vision/roadmap anchor |

**Why keep:** Ahmed Hassan is among the most respected SE researchers; ~40 citations for a 2025 paper signals rapid uptake. Proposes SASE (Structured Agentic SE) with two symbiotic modalities — SE for Humans and SE for Agents — and the Agent Command/Execution Environment duality. Provides the forward-looking vocabulary the review needs for Introduction and Conclusion. No equivalent in consensus.csv (which lacks vision/roadmap papers).

**Role in review:** Introduction (why this matters) + Conclusion (where the field is heading); defines SE 3.0 framing.

---

### V2 — Designing LLM-based Multi-Agent Systems for SE Tasks: Quality Attributes, Design Patterns and Rationale
📄 SUMMARY

| Field | Details |
|-------|---------|
| **BibTeX key** | Cai2025designpatterns |
| **Authors** | Yangxiao Cai, Ruiyin Li, Peng Liang, Mojtaba Shahin, Zengyang Li |
| **Year** | 2025 |
| **Venue** | Under journal review (arXiv:2511.08475) |
| **Citations** | † < 20 (under review) |
| **Cross-check status** | 📄 SUMMARY — retained for unique design-pattern contribution |

**Why keep despite low citation count and pre-publication status:** This is the only paper in either source that systematically identifies design patterns (16 patterns) and quality attributes for LLM-based MAS in SE. The low citation count reflects pre-publication status, not quality (94-paper systematic review; ISO 25010 framework applied). Fills a structural gap — where He et al. covers *what* is built, this covers *how* to design it. No equivalent exists in the consensus.csv.

**Role in review:** Architecture/Design subsection — practical design guidance; supports discussion of why different systems make different architectural choices.

---

## Papers Dropped After Cross-Check

The following papers from paper_summaries.md are **excluded** from the filtered selection. Reasons are given for each.

| # | Paper | Citations | Reason for Exclusion |
|---|-------|-----------|----------------------|
| Former #4 | Chen et al. 2024 — Survey on LLM-based MAS | 29 | **Superseded** by Guo et al. 2024 (761 cites) for the general MAS survey slot. Same thematic role, dramatically lower citation authority. |
| Former #14 | ALMAS 2025 (Tawosi et al.) | † < 5 | Workshop paper; early-stage vision only; zero consensus support; content covered more rigorously by MetaGPT/ChatDev/He et al. |
| Former #17 | SALLMA 2025 (Becattini et al.) | † < 10 | 4-page workshop paper; no empirical validation; zero consensus support; architectural angle covered by Cai et al. (#V2) with more depth. |
| Former #24 | Rajendran et al. 2025 — Refactoring Framework | † < 5 | Purely conceptual, no implementation or results; regional venue; zero consensus support. The motivating example (40% → 65% CPU) is hypothetical, not measured. |
| Former #25 | Garlapati et al. 2024 — Test Generation (IBM) | † < 5 | Evaluated on a trivial 2-method Java class; no comparison against EvoSuite or similar baselines; regional conference; zero consensus support. |

**Borderline — Kept for now, revisit if over page limit:**

| # | Paper | Citations | Note |
|---|-------|-----------|------|
| Former #3 | Jin et al. 2024 — From LLMs to Agents | ~80 | Useful for LLM vs. agent distinction but overlaps with He et al. and Liu et al. Drop if space is tight. |
| Former #19 | Ronanki 2025 — Human-Agent Collaboration | † < 5 | Work-in-progress (5 pages); unique EU AI Act governance angle not covered elsewhere; include only if review discusses human oversight. |
| Former #21 | Cinkusz & Chudziak 2024 — CogniSim | ~20 | ✅ In consensus; 2-page demo; ToM integration is novel but unvalidated; keep only if Agile SE or Theory of Mind is discussed. |
| Former #22 | Sami et al. 2025 — Requirements Analysis | † < 5 | Real industrial case (Austrian Post) is compelling; small scale (12 stories); include only if requirements engineering is a named section. |
| Former #23 | Batole et al. 2025 — LOCALIZEAGENT | † < 15 | ICSE 2025 (top venue); 200%+ improvement metric is strong; include if application evidence is needed; very new. |

---

## Final 15-Paper Selection at a Glance

| # | BibTeX Key | Category | Citations | Validation |
|---|-----------|----------|-----------|------------|
| 1 | Wang2023autonomousagents | Survey — Foundational | 2,011 | 📄 SUMMARY |
| 2 | He2025literaturereview | Survey — SE-Specific | 144 | ✅ BOTH |
| 3 | Liu2024agentssurvey | Survey — SE-Specific | 151 | ✅ BOTH |
| 4 | **Guo2024massurvey** ⭐ | **Survey — General MAS** | **761** | **🔍 CONSENSUS** |
| 5 | Hong2023metagpt | Framework | 1,475 | ✅ BOTH |
| 6 | Qian2023chatdev | Framework | 603 | ✅ BOTH |
| 7 | Wu2023autogen | Framework | 851 | 📄 SUMMARY |
| 8 | Huang2023agentcoder | Framework | 312 | ✅ BOTH |
| 9 | Xia2025demystify | Framework / Counterpoint | ~400 | 📄 SUMMARY |
| 10 | **Han2024challenges** ⭐ | **Challenges** | **124** | **🔍 CONSENSUS** |
| 11 | Talebirad2023collaboration | Challenges — Historical | 282 | 📄 SUMMARY |
| 12 | Yehudai2025evalsurvey | Evaluation | 67 | 📄 SUMMARY |
| 13 | Hassan2025agenticroadmap | Vision / Roadmap | ~40 | 📄 SUMMARY |
| 14 | Cai2025designpatterns | Architecture / Design | † < 20 | 📄 SUMMARY |
| 15 | *(flex slot — see below)* | Application | varies | varies |

**Flex slot (Paper 15):** Choose one based on review emphasis:
- **Batole2025localizeagent** — if applications / code quality section needed (ICSE 2025, top venue)
- **Ronanki2025trustworthy** — if human-in-the-loop / governance section needed (FSE 2025)
- **SWESearch2024** (Antoniades et al., 81 cites) — if search/planning techniques section needed (🔍 CONSENSUS available)

---

## Suggested Thematic Mapping for 2-Page Review

```
1. Introduction (~0.2 pages)
   - Why multi-agent LLM SE now? 
   → Cite: Hassan2025 (SASE framing), He2025 (scope definition)

2. Foundations: What Are LLM-Based Agents? (~0.2 pages)
   → Cite: Wang2023 (agent modules), Guo2024 (multi-agent evolution), Talebirad2023 (early challenges)

3. Current Approaches (~0.8 pages)
   A. Frameworks & Systems
      - Structured/SOP-based: MetaGPT (Hong2023)
      - Dialogue-based: ChatDev (Qian2023)
      - General-purpose infrastructure: AutoGen (Wu2023)
      - Iterative feedback loops: AgentCoder (Huang2023)
   B. The Complexity Question
      - Simple pipelines vs. agent complexity: Agentless (Xia2025)
   C. Surveys of the space
      - SE-specific: He2025, Liu2024
      - Design patterns: Cai2025

4. Challenges & Evaluation (~0.4 pages)
   → Cite: Han2024 (coordination challenges), Yehudai2025 (evaluation gaps)
   → Optional: Batole2025 or Ronanki2025 depending on angle

5. Future Directions & Conclusion (~0.2 pages)
   → Cite: Hassan2025 (SASE roadmap)
```

---

## Citation Distribution of Final 15 Papers

```
> 1,000 citations:  3 papers  (Wang 2023, MetaGPT, ChatDev — or AutoGen)
500–1,000 citations: 1 paper  (AutoGen 851)
100–500 citations:   5 papers  (Guo 2024, Agentless, AgentCoder, Talebirad, Liu 2024, He 2025)
50–100 citations:    2 papers  (Han 2024, Yehudai 2025)
< 50 citations:      2 papers  (Hassan 2025, Cai 2025) — new/under review, not penalized
```

**Citation total:** ~6,300+ across the 15 papers — strong empirical grounding.

---

## Notes on Classical Agent-Oriented SE Papers (consensus.csv rows 13–45)

The consensus.csv contains 20+ papers on classical agent-oriented software engineering (Wooldridge 1997, Jennings 1999–2000, DeLoach 2001, etc.). These are **not included** in the filtered selection for the following reasons:

1. **Scope mismatch:** This review focuses on LLM-based multi-agent SE (2023+). Classical AOSE addresses intelligent agents for distributed systems design, not LLM-based coding assistants.
2. **Paradigm shift:** The LLM era represents a fundamental architectural break from classical reactive/deliberative agents — citing classical AOSE as background may mislead readers about continuity.
3. **Page constraint:** A 2-page review cannot do justice to both paradigms.

**If background depth is needed:** Cite Wooldridge 1997 (1,863 cites) or Jennings 2000 (903 cites) as a single sentence establishing that agent-oriented SE has a 30-year history, with this review focusing on the LLM-era resurgence. One citation is sufficient; do not over-weight pre-2020 work.

---

*Generated: 2026-05-09 | Source 1: paper_summaries.md (25 papers) | Source 2: consensus.csv (50 papers) | Cross-validation method: citation count + venue quality + thematic gap analysis*
