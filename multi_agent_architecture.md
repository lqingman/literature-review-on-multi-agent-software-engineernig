# Multi-Agent Architecture for This Literature Review

**CS 7980 | 2026-05-16**

---

## Overview

This literature review was conducted using a multi-agent pipeline in which distinct agents — some AI-powered, one human — were assigned specific roles and executed sequentially. The full pipeline spans five stages: dual-path paper discovery, cross-validation, human filtering, summary generation, and parallel section writing. Each stage produces a structured artifact that the next stage consumes, creating a traceable chain from raw search results to finished prose.

---

## Pipeline Description

### Stage 1 — Dual-Path Paper Discovery

Two agents with different search mechanisms operate in parallel and independently, with no communication between them.

**Agent A (Claude)** uses conversational prompting combined with a live academic search tool. Queries were issued in natural language and refined iteratively across a session. Because Claude has direct access to a search tool, it can retrieve papers from live databases rather than relying solely on training knowledge, enabling it to surface recent works and verify citations in real time.

**Agent B (Consensus)** uses a structured academic database interface. The same research question was entered through Consensus's filter panels — scoped by time range, study type, and category — and returned papers exported as a structured CSV with citation counts, DOIs, SJR quartile rankings, and abstracts. Consensus provided an independent retrieval path outside Claude's search scope, and also offered features unavailable in any conversational agent: citation graphs for tracing intellectual lineage and full-text PDF access via institution-linked LibKey.

Running both agents independently and in parallel is the key architectural choice of Stage 1. Because neither agent was aware of the other's output, their disagreements are informative: a paper found by both is a high-confidence candidate; a paper found only by one is flagged for the cross-check agent to investigate.

### Stage 2 — Cross-Check Agent (Claude)

A separate Claude session received both paper lists as input and performed a structured merge. Its task was to identify overlapping papers, flag high-citation works unique to each source, and apply a relevance filter based on the review's research question. This agent produced a filtered candidate list that includes not only the shortlisted papers but explicit rationale for why each was included or excluded — making the filtering logic auditable.

The cross-check agent acts as a reconciliation layer between two imperfect agents. It does not add new papers from its own search; its role is purely comparative and evaluative.

### Stage 3 — Human Verification

After the cross-check agent's filtering, a human researcher reviewed the candidate list before any writing began. This gate existed for two reasons: first, AI agents at Stages 1 and 2 can mis-classify relevance, especially for papers on the boundary of the review's scope; second, each group member's independently selected papers needed to be merged into a shared pool. The human approved, modified, or overrode the AI agent's inclusion decisions and confirmed the final paper pool. This is the only non-AI stage in the pipeline.

### Stage 4 — Summary Generation Agent (Claude)

With the final paper pool confirmed, a Claude session with full context of all approved papers generated a structured per-paper summary for each. Each summary captures: main contribution, methods, results, limitations, critical analysis, and a note on how the paper relates to the review. These summaries became the canonical input for all downstream writing agents, ensuring that every writing agent works from the same structured representation rather than raw abstracts of varying quality.

### Stage 5 — Parallel Writing Agents (Claude + Consensus)

Separate Claude sessions, each receiving the combined paper summaries and a targeted prompt, generated individual review sections independently and in parallel. Each agent was assigned a specific section — Introduction, Background, and so on — and given a section-specific prompt that defined the rhetorical goals and structural requirements for that section. All agents were instructed to use academic prose with inline author-year citations and no bullet points or subsection headers, enforcing style consistency across independently generated outputs. Each group member was responsible for prompting and reviewing their assigned agent's section.

For the Main Body section, the dual-agent pattern from Stage 1 was extended into writing: both Claude and Consensus received the same confirmed 34-paper pool and the same section-specific goals, and produced drafts independently. Claude organized its output around three themes — framework design, benchmarks and evaluation, and emerging deployment challenges — and drew citations exclusively from the confirmed pool throughout. Consensus produced a structurally similar draft but introduced approximately eight papers not in the pool across all three themes, including frameworks and benchmarks absent from the cross-validated list. Incorporating these would have required re-running earlier pipeline stages, so Claude's draft served as the primary base. Specific empirical details from Consensus were selectively incorporated where they strengthened existing claims without introducing new sources — for example, the statistic that early frontier models resolved fewer than 2% of SWE-bench issues.

One concrete failure surfaced during citation verification of Claude's draft: two cited papers could not be confirmed at their provided URLs. The Preprints.org link resolved to an unrelated paper, and one IEEE Access DOI was inaccessible. Both were removed from Section 3, though one was retained in the reference list as it had already been cited in earlier sections. This illustrates a persistent limitation of writing agents: citations are generated with apparent confidence but require independent verification before use.

Running two writing agents independently made implicit framing choices visible and negotiable. Each agent selected which papers to foreground and how to characterize tensions between findings; where the two drafts diverged, those divergences indicated genuine interpretive choices rather than settled consensus. In a single-agent system these choices would be invisible and fixed.

---

## Comparison to a Single-Agent System

A single-agent baseline would replace the entire pipeline with one session: issue a research question to one AI tool, receive a list of papers, and generate the full review in one pass. While simpler to execute, this approach has several structural weaknesses that the multi-agent pipeline is specifically designed to address.

The most significant difference is in search coverage and recall. A single agent is bounded by one retrieval mechanism. If that mechanism has blind spots — whether due to training data coverage, database access limitations, or query design — those gaps are never surfaced. The multi-agent pipeline uses two agents with fundamentally different retrieval mechanisms operating in parallel. Because neither agent knows what the other found, their disagreements become visible, and papers missed by one can be recovered by the other. Without cross-validation, certain high-impact papers would have been absent from the review with no indication that anything was missing.

A second difference is in error propagation. In a single-agent system, a mistake in early retrieval is silently inherited by all downstream generation — a misclassified paper becomes part of the synthesis with no mechanism for correction. In the multi-agent pipeline, the cross-check agent explicitly flags disagreements between Stage 1 agents, and the human verification gate provides a second check before any writing begins. Errors are surfaced at the stage where they occur rather than discovered only in the finished output.

A third difference is in auditability and task focus. A single-agent session produces one output from one undifferentiated process; tracing why a particular paper was included or excluded requires reconstructing intent from the final text alone. The multi-agent pipeline produces named intermediate artifacts at every stage — the filtered candidate list, the per-paper summaries, the section drafts — so the chain of decisions is inspectable and any stage can be re-run independently. Additionally, each agent in the pipeline is given a narrow, well-defined task, whereas a single agent must simultaneously balance retrieval, evaluation, synthesis, and writing, creating prompt complexity and context-window pressure that grows with the scope of the review.

The main advantage of a single-agent approach is simplicity. There are no intermediate artifacts to manage, no inter-stage coordination required, and the entire workflow can be completed in one session. For small, well-scoped reviews where the agent's search coverage is known to be sufficient, this tradeoff may be acceptable. For a review of a rapidly evolving research area — where coverage gaps are likely and methodological transparency is important — the multi-agent pipeline's redundancy, auditability, and structured human oversight outweigh the added coordination cost.

---

## Design Lessons

1. **Parallelism at discovery, not at writing.** Running search agents in parallel adds coverage without coordination overhead; running writing agents in parallel risks style divergence unless inputs and style constraints are standardized. The pipeline separates these concerns deliberately.

2. **Artifacts are first-class outputs.** Each agent produces a named file, not just a response. This makes the pipeline inspectable and allows any stage to be re-run or handed off independently.

3. **Human gates belong at knowledge boundaries.** The human verification stage sits precisely between retrieval — where AI agents have the most variance — and writing — where the input is fixed. This placement maximizes the value of human judgment.

4. **Structured summaries decouple retrieval from writing.** By inserting a summary-generation agent between the paper pool and the writing agents, each writing agent receives uniform, pre-digested input rather than raw abstracts of varying quality. This is the pipeline's most important design choice for cross-section consistency.

5. **Parallel writing agents make interpretive choices visible.** When two agents draft the same section independently, their differences — which papers to foreground, how to frame conflicts between findings — surface as explicit, negotiable decisions rather than invisible defaults. The cost is requiring reconciliation; the benefit is that no single agent's framing is accepted uncritically. For sections where synthesis judgment matters most, this tradeoff is worth taking.

6. **Pool discipline must be enforced at the writing stage, not assumed.** Both writing agents at Stage 5 received the same confirmed paper pool, yet one agent introduced out-of-pool sources regardless. Agents do not reliably self-constrain to a closed citation set without explicit verification. Citation outputs should be cross-checked against the confirmed pool and verified at their source URLs before the draft is accepted.
