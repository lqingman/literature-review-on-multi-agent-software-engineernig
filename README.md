# Literature Review — Multi-Agent Software Engineering
**CS 7980 Capstone | Northeastern University**

---

## Assignment Overview

This repository contains all research artifacts for the CS 7980 capstone literature review assignment on **multi-agent software engineering**. The assignment requires two AI-assisted research workflows — Claude (via Northeastern access) and [Consensus](https://consensus.app/) — to be run in parallel, with the final deliverables synthesizing insights from both.

### Deliverables Required

| # | Deliverable | Status |
|---|-------------|--------|
| 1 | **2-page literature review** with at least 10 references | Ready to write — use `filtered_papers.md` |
| 2 | **1-page comparison** of Claude vs. Consensus process/results | Ready to write — use this README as reference |

---

## Repository Structure

```
Literature Review on Multi-Agent Software Engineering/
│
├── README.md                        ← This file: project guide and process log
│
├── filtered_papers.md               ← FINAL SELECTION: 15 papers cross-validated
│                                      between Claude and Consensus; use this as the
│                                      direct input for writing the 2-page review
│
├── paper_summaries.md               ← Claude-generated deep summaries of 25 papers
│                                      (full critical analysis, BibTeX keys, methods,
│                                      results, limitations, thematic grouping)
│
├── consensus.csv                    ← Raw Consensus search export: 50 papers on
│                                      multi-agent SE with abstracts, citations,
│                                      journal SJR quartiles, and DOIs
│
├── consensus.pdf                    ← Original assignment specification (PDF)

```

---

## Research Scope

**Research Question:** How are large language model (LLM)-based multi-agent systems designed and applied across the software development lifecycle, and what are the key open challenges?

**Primary search terms:** multi-agent systems, LLM agents, software engineering, multi-agent collaboration, agentic software engineering, autonomous agents SE

**Time frame:** 2023–2026 (LLM era); foundational pre-2023 work included where seminal

**Source types prioritized:** ACM TOSEM, ICSE, FSE/PACMSE, ICLR, ACL (top-tier venues); high-citation arXiv preprints

---

## Process Log

### Phase 1 — Consensus Search

Ran structured queries on [consensus.app](https://consensus.app/) using the research question above. Exported 50 results to `consensus.csv`, which includes:
- Title, authors, year, abstract
- Citation counts
- Journal SJR quartile rankings
- DOIs and direct Consensus links

**Key observation:** Consensus surfaced a broad set including classical agent-oriented SE papers from 1994–2009 (Wooldridge, Jennings, DeLoach) alongside modern LLM-era papers. The older papers were excluded from the final selection as they address a different computing paradigm (pre-LLM intelligent agents).

**Notable Consensus finds that would have been missed otherwise:**
- Guo et al. 2024 "Large Language Model based Multi-Agents: A Survey" — **761 citations**, absent from initial manual search
- Han et al. 2024 "LLM Multi-Agent Systems: Challenges and Open Problems" — **124 citations**, fills the challenges/gaps angle

### Phase 2 — Claude-Assisted Deep Analysis

Used Claude Code (Anthropic) to conduct a systematic review of 25 papers sourced from ACM DL, IEEE Xplore, arXiv, and Google Scholar. This produced `paper_summaries.md`, which contains for each paper:
- Full critical analysis (problem solved, assumptions, strengths/weaknesses)
- Methods, results, limitations
- How it relates to the review
- BibTeX keys and venue information
- Citation-count-informed filtering guide


**Notable papers found via Claude that Consensus missed:**
- AutoGen (Wu et al. 2023) — **851 citations**, the most widely adopted multi-agent framework
- Agentless (Xia et al. 2024/2025) — **~400 citations**, critical counterpoint to complex agent architectures
- Wang et al. 2023 foundational survey — **2,011 citations**, the most-cited paper in the space

### Phase 3 — Cross-Validation

Generated `filtered_papers.md` by cross-referencing both sources:
- Papers in both → highest confidence (6 confirmed)
- Papers in Consensus only with high citations → elevated (2 added: Guo 2024, Han 2024)
- Papers in Claude summaries only with high citations → retained (AutoGen, Agentless, Wang 2023)
- Papers with no consensus support AND weak venue/citation standing → dropped (5 removed)

**Result:** 15 papers selected, ~6,300 combined citations, spanning surveys, frameworks, challenges, evaluation, and vision.

---

## Claude vs. Consensus: Key Differences

| Dimension | Claude | Consensus |
|-----------|--------|-----------|
| **Interaction style** | Conversational; iterative refinement through dialogue | Query-based; structured search with filters |
| **Output format** | Narrative summaries, critical analysis, thematic grouping | Structured table with abstracts, citations, journal metrics |
| **Depth per paper** | High — generates full critical analysis, limitations, comparison to peers | Low — abstract + metadata only |
| **Breadth of search** | Relies on user-supplied papers + reasoning from known literature | Independent database search across academic corpus |
| **Citation data** | Estimated / retrieved separately from Semantic Scholar | Included directly in export |
| **Synthesis** | Strong — groups papers by theme, identifies patterns, suggests review structure | Weak — presents results as a ranked list, no synthesis |
| **Gap identification** | Proactive — flagged missing evaluation-focused papers, design pattern gap | Passive — surfaces what matches the query |
| **Risk of missing papers** | Moderate — bounded by user-provided corpus and training knowledge | Moderate — bounded by database coverage and query formulation |
| **Unique value** | Critical analysis, writing guidance, filtering rationale, thematic narrative | Independent verification, citation counts, journal quartile data, broader net |

**Combined workflow advantage:** Running both tools in parallel and cross-checking their outputs caught papers that either tool alone would have missed. Consensus found the 761-citation Guo et al. survey that Claude didn't surface; Claude found AutoGen and Agentless that Consensus didn't return.

---

## Final Paper Selection (15 papers)

See `filtered_papers.md` for full details. Quick reference:

| # | Paper | Year | Citations | Theme |
|---|-------|------|-----------|-------|
| 1 | Wang et al. — Survey on LLM Autonomous Agents | 2023 | 2,011 | Survey — Foundational |
| 2 | He, Treude, Lo — LMA for SE (TOSEM) | 2025 | 144 | Survey — SE-Specific |
| 3 | Liu et al. — LLM Agents for SE (TOSEM) | 2024 | 151 | Survey — SE-Specific |
| 4 | **Guo et al. — LLM-based Multi-Agents Survey** ⭐ | 2024 | **761** | Survey — General MAS |
| 5 | Hong et al. — MetaGPT | 2023 | 1,475 | Framework |
| 6 | Qian et al. — ChatDev | 2023 | 603 | Framework |
| 7 | Wu et al. — AutoGen | 2023 | 851 | Framework |
| 8 | Huang et al. — AgentCoder | 2023 | 312 | Framework |
| 9 | Xia et al. — Agentless (PACMSE) | 2025 | ~400 | Framework / Counterpoint |
| 10 | **Han et al. — LLM-MAS Challenges** ⭐ | 2024 | **124** | Challenges |
| 11 | Talebirad & Nadiri — Multi-Agent Collaboration | 2023 | 282 | Challenges — Historical |
| 12 | Yehudai et al. — Evaluation Survey (ACL) | 2025 | 67 | Evaluation |
| 13 | Hassan et al. — Agentic SE Roadmap | 2025 | ~40 | Vision |
| 14 | Cai et al. — Design Patterns for LLM-MAS | 2025 | <20 | Architecture |
| 15 | *(flex: Batole 2025 ICSE / Ronanki 2025 FSE)* | 2025 | varies | Application |

⭐ = newly identified through Consensus cross-check; was missing from initial Claude-assisted review

---

## Suggested Review Structure (2 pages)

```
1. Introduction (~0.2 pages)
   Why multi-agent LLM SE now?  [Hassan 2025, He 2025]

2. Background: What Are LLM-Based Agents? (~0.2 pages)
   Agent modules, evolution from single to multi-agent  [Wang 2023, Guo 2024, Talebirad 2023]

3. Current Approaches (~0.8 pages)
   A. Frameworks
      - Role-based / SOP-structured:  MetaGPT [Hong 2023]
      - Dialogue-based:               ChatDev [Qian 2023]
      - General-purpose infrastructure: AutoGen [Wu 2023]
      - Iterative feedback loops:     AgentCoder [Huang 2023]
   B. The Complexity Question
      - Simple pipelines vs. complex agents: Agentless [Xia 2025]
   C. Surveys of the landscape
      - He 2025, Liu 2024 (SE-specific); Cai 2025 (design patterns)

4. Challenges & Evaluation (~0.4 pages)
   Open problems in coordination, context, memory  [Han 2024]
   Evaluation methodology gaps                     [Yehudai 2025]

5. Conclusion / Future Directions (~0.2 pages)
   SE 3.0 / SASE vision, research roadmap          [Hassan 2025]
```

---

## Key Findings for the Review

1. **The field is converging around two paradigms:** structured-document coordination (MetaGPT) vs. natural language dialogue (ChatDev), with general-purpose frameworks (AutoGen) bridging both.

2. **The complexity paradox:** Agentless (Xia et al.) achieves state-of-the-art SWE-bench results (50.8%) using a simple three-phase pipeline — outperforming complex agent frameworks at lower cost. This challenges the field's assumption that more agentic complexity always yields better performance.

3. **Evaluation is the field's weakest link:** Yehudai et al. and Han et al. both identify the lack of standardized evaluation as a critical bottleneck. SWE-bench remains the dominant benchmark but may not reflect real enterprise complexity.

4. **Surveys confirm rapid growth:** He et al. (41 primary studies) and Liu et al. (124 papers) both document a field growing faster than existing reviews can capture.

5. **Vision vs. reality gap:** Hassan et al.'s SASE roadmap proposes fully autonomous engineering teams; current state-of-the-art (Agentless at 50.8% on SWE-bench) leaves substantial ground to cover.

---

## Resources Used

| Tool / Database | Purpose |
|-----------------|---------|
| [Consensus](https://consensus.app/) | Primary independent search; citation data; journal quartile rankings |
| [ACM Digital Library](https://dl.acm.org/) | Full-text access for TOSEM, FSE, ICSE papers |
| [IEEE Xplore](https://ieeexplore.ieee.org/) | Full-text access for ASE, SoutheastCon papers |
| [arXiv](https://arxiv.org/) | Preprint access for frameworks (MetaGPT, ChatDev, AutoGen, Agentless) |
| [Semantic Scholar](https://www.semanticscholar.org/) | Citation count verification |
| [Connected Papers](https://www.connectedpapers.com/) | Citation network exploration |
| Claude (Northeastern access) | Deep paper analysis, critical synthesis, thematic organization |

---

*Repository initialized: 2026-05-08 | Last updated: 2026-05-09 | Papers in final selection: 15 | Total papers reviewed: 75 (25 deep + 50 Consensus)*
