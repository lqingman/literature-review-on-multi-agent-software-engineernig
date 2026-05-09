# Tool Comparison: Claude vs. Consensus
**CS 7980 — Literature Review Process | Qingman Li | 2026-05-09**

---

## Overview

This literature review used two AI-assisted tools in parallel: **Claude** (Anthropic, via Northeastern access) and **Consensus** (consensus.app, free tier). They served complementary but distinct roles across a three-phase workflow: Consensus for structured discovery, Claude for deep analysis, and both together for cross-validation.

---

## Interaction Style

Interaction with the two tools felt fundamentally different. Claude is conversational — queries were written in natural language and refined iteratively across a session, with follow-up prompts adjusting scope, depth, and format. The entire workflow with Claude happened as a dialogue: "summarize this paper," "now compare it to MetaGPT," "group these 25 papers into themes." Consensus is interface-driven — searches are run through filter panels with controls for time range, study type, and category, and results appear as a ranked list of papers with metadata. There is no back-and-forth; the query either surfaces relevant papers or it doesn't.

---

## What Each Tool Did Well

**Claude** handled the analytical heavy lifting. It performed deep critical analysis on all 25 papers — extracting main contributions, assumptions, methods, results, limitations, and how each paper related to the review — and organized them into thematic groups (Surveys / Frameworks / Challenges / Evaluation / Vision). It generated every file in this repository: `paper_summaries.md`, `filtered_papers.md`, `README.md`, `literature_review.md`, and this comparison. Claude also proactively flagged gaps: it identified that evaluation methodology was underrepresented in the initial corpus and recommended adding Yehudai et al. 2025 (ACL Findings). Its weakness is bounded search — it could only work with papers the user provided or papers well-known from training, which created blind spots.

**Consensus** added independent breadth. Running the same research question through Consensus's database returned 50 papers exported to `consensus.csv`, complete with citation counts, journal SJR quartile rankings, abstracts, DOIs, and direct links. Two critical papers surfaced this way that Claude entirely missed: **Guo et al. 2024** ("LLM-based Multi-Agents: A Survey of Progress and Challenges," 761 citations — the third highest in the corpus) and **Han et al. 2024** ("LLM Multi-Agent Systems: Challenges and Open Problems," 124 citations). Both were added to the final selection. Beyond discovery, Consensus offered features unavailable in Claude: time and category filters for scoping queries, exportable structured CSV data, visual charts summarizing search results, citation graphs for tracing intellectual lineage, and full-text PDF access to paywalled papers via **LibKey** (institution-linked). Clicking directly through to the original paper in Consensus is immediate; in Claude, the user must locate the paper separately.

---

## What Each Tool Missed

The cross-validation in `filtered_papers.md` makes the gaps concrete. Consensus missed **AutoGen** (Wu et al. 2023, 851 citations), **Agentless** (Xia et al. 2024/2025, ~400 citations), and the foundational **Wang et al. 2023** survey (2,011 citations) — likely because the "multi-agent" query filter de-prioritized papers that discuss single-agent or agentless architectures. Claude missed the Guo et al. and Han et al. papers entirely, despite both being high-impact works in the exact scope of the review — likely a training-data coverage gap rather than a reasoning failure.

---

## Comparison at a Glance

| Dimension | Claude | Consensus |
|---|---|---|
| Interaction | Conversational, iterative | GUI filter-based, single query |
| Search coverage | User-supplied + training knowledge | Independent academic database |
| Depth per paper | Full critical analysis | Abstract + metadata only |
| Synthesis | Strong — themes, patterns, narrative | None — ranked list only |
| Citation data | Estimated / verified separately | Included in export |
| Unique output | All written documents in this repo | CSV export, charts, citation graphs |
| Paper access | Text only (no direct PDF) | Full PDF via LibKey |
| Usage volume | Primary tool throughout all phases | Supplementary; limited by free tier |
| Unique finds | AutoGen (851c), Agentless (~400c), Wang 2023 (2,011c) | Guo 2024 (761c), Han 2024 (124c) |

---

## Reflection

Neither tool alone would have produced the final 15-paper selection. Running them in parallel and cross-referencing their outputs caught papers each missed independently — a combined corpus of ~6,300 citations across the final set, stronger than either source produced alone. The ideal workflow for future reviews is: use Consensus first as a structured discovery pass (with time filters and category selectors to scope the search), export the CSV for citation-count triage, then hand the curated corpus to Claude for deep analysis, synthesis, and writing. With more Consensus access, the citation graph feature would be especially worth using early — tracing how MetaGPT, ChatDev, and AutoGen cite each other would have surfaced additional cluster-specific papers faster than keyword search alone.
