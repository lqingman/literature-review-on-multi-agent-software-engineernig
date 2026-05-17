# Combined Paper Pool — Multi-Agent LLM Software Engineering
## Three-Way Merge: Your filtered_papers.md + Classmate 1 (PDF1) + Classmate 2 / S. Fang (PDF2)

**Date:** 2026-05-16  
**Total unique papers:** 34  
**Sources merged:**
- **YOURS** — `filtered_papers.md` (your 15-paper cross-validated selection)
- **PDF1** — Classmate 1's review (anonymous, 4-page paper, 14 references)
- **PDF2** — S. Fang's review (5-page paper, 12 references)

**Source legend in tables:**
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
| **DOI** | — |
| **Sources** | ◆ YOURS |

**Note:** Foundational agent framework paper (Profile/Memory/Planning/Action). Highest-cited paper in the entire pool.

---

### W2 — LLM-Based Multi-Agent Systems for Software Engineering: Literature Review, Vision, and the Road Ahead
| Field | Details |
|-------|---------|
| **BibTeX key** | He2025literaturereview |
| **Authors** | Junda He, Christoph Treude, David Lo |
| **Year** | 2025 (TOSEM); cited as 2024 in PDF1 |
| **Venue** | ACM Transactions on Software Engineering and Methodology (Q1) |
| **Citations** | 144 |
| **DOI** | 10.1145/3712003 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 |

**Note:** Most directly scoped systematic review (41 primary studies). Cited by all three reviews — strongest cross-validation in the pool.

---

### W3 — Large Language Model-Based Agents for Software Engineering: A Survey
| Field | Details |
|-------|---------|
| **BibTeX key** | Liu2024agentssurvey |
| **Authors** | Junwei Liu, Kaixin Wang, Yixuan Chen, Xin Peng, Zhenpeng Chen, Lingming Zhang, Yiling Lou |
| **Year** | 2024 |
| **Venue** | ACM Transactions on Software Engineering and Methodology (Q1) |
| **Citations** | 151 |
| **DOI** | 10.48550/arxiv.2409.02977 |
| **Sources** | ◆ YOURS · ① PDF1 |

**Note:** Broadest corpus (124 papers); dual-perspective analysis (SE task view + agent architecture view).

---

### W4 — Large Language Model based Multi-Agents: A Survey of Progress and Challenges
| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2024massurvey |
| **Authors** | Taicheng Guo, Xiuying Chen, Yaqi Wang, et al. |
| **Year** | 2024 |
| **Venue** | arXiv (cs.AI) |
| **Citations** | **761** |
| **DOI** | 10.48550/arxiv.2402.01680 |
| **Sources** | ◆ YOURS |

**Note:** Third most-cited paper in the pool. Covers agent profiling, communication, skill development in multi-agent settings.

---

### W5 — A Comprehensive Survey on Benchmarks and Solutions in Software Engineering of LLM-Empowered Agentic System ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Guo2025benchmarks |
| **Authors** | J. Guo, S. Huang, M. Li, D. Huang, X. Chen, R. Zhang, Z. Guo, H. Yu, S. Yiu, C. Jensen, P. Lio, K. Lam |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2510.09721 |
| **Citations** | — |
| **DOI** | arXiv:2510.09721 |
| **Sources** | ① PDF1 |

**Note:** Different paper from Guo2024massurvey. Focuses specifically on benchmarks and solutions for LLM-empowered agentic systems in SE. Cited by PDF1 for benchmark fragmentation argument.

---

### W6 — From LLMs to LLM-Based Agents for Software Engineering: A Survey of Current, Challenges and Future ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Jin2024llmtoagents |
| **Authors** | H. Jin, L. Huang, H. Cai, J. Yan, B. Li, H. Chen |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2408.02479 |
| **Citations** | ~80 |
| **DOI** | arXiv:2408.02479 |
| **Sources** | ① PDF1 |

**Note:** Draws the key distinction between standalone LLMs and LLM-based agents (multi-step planning, tool use, iterative feedback). Cited as borderline-keep in your original paper_summaries.md.

---

### W7 — Agentic Software Issue Resolution with Large Language Models: A Survey ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Jiang2025agenticsolutions |
| **Authors** | Z. Jiang, D. Lo, Z. Liu |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2512.22256 |
| **Citations** | — |
| **DOI** | arXiv:2512.22256 |
| **Sources** | ① PDF1 |

**Note:** Focused survey on agentic approaches to issue/bug resolution — narrower scope than general SE surveys. Co-authored by David Lo (also co-author of He2025).

---

### W8 — Large Language Models for Software Engineering: Survey and Open Problems ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Fan2023llmsse |
| **Authors** | A. Fan, B. Gokkaya, M. Harman, M. Lyubarskiy, S. Sengupta, S. Yoo, J. Zhang |
| **Year** | 2023 |
| **Venue** | IEEE/ACM ICSE-FoSE 2023 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

**Note:** Pre-agent era survey establishing baseline of LLM capability in SE (code generation, repair, testing). PDF1 uses it to anchor the historical transition from single-LLM to agentic approaches.

---

### W9 — A Survey on Large Language Models for Software Engineering ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Zhang2023llmsurvey |
| **Authors** | Q. Zhang, C. Fang, Y. Xie, Y. Zhang, Y. Yang, W. Sun, S. Yu, Z. Chen |
| **Year** | 2023 |
| **Venue** | arXiv preprint arXiv:2312.15223 |
| **Citations** | — |
| **DOI** | arXiv:2312.15223 |
| **Sources** | ① PDF1 |

**Note:** Broad LLM-for-SE survey (not agent-focused); cited by PDF1 alongside Fan2023 to establish pre-agent baseline.

---

### W10 — Methods and Techniques of Agentic Software Engineering: A Systematic Literature Review ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Otoum2026systematicreview |
| **Authors** | N. Otoum, N. Elkhalili |
| **Year** | 2026 |
| **Venue** | IEEE Access, Vol. 14, pp. 7443–7465 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** IEEE Access SLR — peer-reviewed. Reports multi-agent studies rising from 15% to 42% of SE corpus between 2022–2024. Identifies trust/transparency as adoption barriers in 78% of industry studies. Strong empirical framing for field-growth narrative.

---

## Section 2: Frameworks & Systems (14 papers)

---

### F1 — MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework
| Field | Details |
|-------|---------|
| **BibTeX key** | Hong2023metagpt |
| **Authors** | Sirui Hong, Xiawu Zheng, Jonathan P. Chen, et al., Chenglin Wu |
| **Year** | 2023/2024 |
| **Venue** | ICLR 2024 |
| **Citations** | **1,475** |
| **DOI** | 10.48550/arxiv.2308.00352 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 |

**Note:** Cited by all three reviews. The canonical role-based, SOP-driven framework. Second highest cross-validation score in the pool.

---

### F2 — ChatDev: Communicative Agents for Software Development
| Field | Details |
|-------|---------|
| **BibTeX key** | Qian2023chatdev |
| **Authors** | Cheng Qian, Wei Liu, Hongzhang Liu, et al., Maosong Sun |
| **Year** | 2023/2024 |
| **Venue** | ACL 2024 |
| **Citations** | **603** |
| **DOI** | 10.18653/v1/2024.acl-long.810 |
| **Sources** | ◆ YOURS · ① PDF1 |

**Note:** Natural-language (chat chain) coordination counterpart to MetaGPT's SOP approach.

---

### F3 — AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation
| Field | Details |
|-------|---------|
| **BibTeX key** | Wu2023autogen |
| **Authors** | Qingyun Wu, Gagan Bansal, Jieyu Zhang, Yiran Wu, et al., Chi Wang |
| **Year** | 2023 |
| **Venue** | arXiv:2308.08155; Microsoft Research |
| **Citations** | **851** |
| **DOI** | arXiv:2308.08155 |
| **Sources** | ◆ YOURS · ① PDF1 · ② PDF2 (text) |

---

### F4 — AgentCoder: Multi-Agent-based Code Generation with Iterative Testing and Optimisation
| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2023agentcoder |
| **Authors** | Dong Huang, Qingwen Bu, Jie M. Zhang, Michael Luck, Heming Cui |
| **Year** | 2023 |
| **Venue** | arXiv (cs.CL) |
| **Citations** | **312** |
| **DOI** | 10.48550/arxiv.2312.13010 |
| **Sources** | ◆ YOURS |

---

### F5 — Agentless: Demystifying LLM-based Software Engineering Agents
| Field | Details |
|-------|---------|
| **BibTeX key** | Xia2025demystify |
| **Authors** | Chunqiu Steven Xia, Yinlin Deng, Soren Dunn, Lingming Zhang |
| **Year** | 2024 (arXiv) / 2025 (PACMSE journal) |
| **Venue** | Proc. ACM Software Engineering (PACMSE/FSE 2025) |
| **Citations** | ~400 (arXiv) |
| **DOI** | 10.1145/3715754 |
| **Sources** | ◆ YOURS · ① PDF1 |

**Note:** Critical counterpoint — simple 3-phase pipeline matches sophisticated MAS on SWE-bench.

---

### F6 — Self-Organized Agents: A LLM Multi-Agent Framework toward Ultra Large-Scale Code Generation and Optimization (SoA) ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Ishibashi2024soa |
| **Authors** | Y. Ishibashi, Y. Nishimura |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2404.02183 |
| **Citations** | — |
| **DOI** | arXiv:2404.02183 |
| **Sources** | ② PDF2 |

**Note:** Functional decomposition via self-proliferating agent tree (Mother → Child agents). Achieves 71.4% Pass@1 on HumanEval (+5% over single-agent baseline). Addresses scalability as a structural context-window problem.

---

### F7 — Knowledge-Based Multi-Agent Framework for Automated Software Architecture Design (MAAD) ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Zhang2025maad |
| **Authors** | Y. Zhang, R. Li, P. Liang, W. Sun, Y. Liu |
| **Year** | 2025 |
| **Venue** | Proceedings of FSE 2025 (ACM), pp. 530–534 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Targets upstream design phase (SRS → architectural artifacts) via RAG from open-source projects and domain experts. Addresses hallucination risk of zero-shot architecture design.

---

### F8 — An LLM-Based Multi-Agent Framework for Agile Effort Estimation (SEEAgent) ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Bui2025seeagent |
| **Authors** | T. L. Bui, H. K. Dam, R. Hoda |
| **Year** | 2025 |
| **Venue** | IEEE/ACM ASE 2025, pp. 1032–1043 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Multi-round Planning Poker protocol for agile story-point estimation. Fine-tuned variant outperforms deep learning baselines on 3/4 benchmarks. Human study (n=12) showed positive practitioner perceptions.

---

### F9 — A Self-Reflective Multi-Agent Collaboration Framework for Dynamic Software Engineering Tasks (Eco-Evolve) ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Huang2026ecoevolve |
| **Authors** | Y. Huang |
| **Year** | 2026 |
| **Venue** | — (arXiv / technical report) |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Three mechanisms: dynamic topology generator, System 2 Reflection with Critic Agent, error-driven self-evolution via Hindsight Experience Replay. 62.3% on SWE-bench Verified; 73.5% on DevBench. Ablation shows memory bank is the largest single contributor.

---

### F10 — Agyn: A Multi-Agent System for Team-Based Autonomous Software Engineering ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Benkovich2026agyn |
| **Authors** | N. Benkovich, V. Valkov |
| **Year** | 2026 |
| **Venue** | arXiv preprint arXiv:2602.01465 |
| **Citations** | — |
| **DOI** | arXiv:2602.01465 |
| **Sources** | ② PDF2 |

**Note:** Production-deployed, GitHub-native workflow. Manager/Researcher/Engineer/Reviewer roles. 72.2% task resolution on SWE-bench 500 without benchmark-specific tuning.

---

### F11 — ALMAS: An Autonomous LLM-Based Multi-Agent Software Engineering Framework ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Tawosi2025almas |
| **Authors** | V. Tawosi, K. Ramani, S. Alamir, X. Liu |
| **Year** | 2025 |
| **Venue** | IEEE/ACM ASEW 2025, pp. 287–290 |
| **Citations** | < 5 |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Six-agent orchestration with Meta-RAG (natural-language codebase summaries) and tiered model routing. Previously flagged as borderline in your filtered_papers.md — PDF2 now provides the full citation and context.

---

### F12 — Software Development Using a Multi-Agent Approach ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Ribeiro2025multiagent |
| **Authors** | J. G. Ribeiro, J. M. Pires, J. O. Pereira, F. A. Durão, C. G. Ralha |
| **Year** | 2025 |
| **Venue** | WESAAC 2025 (Workshop), pp. 93–100. SBC. |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Human-in-the-loop 5-agent MAS with Redis Pub/Sub + MongoDB persistent knowledge base. Prototype generated Python Flask backend with JWT/CRUD. Workshop venue; limited scope.

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

---

## Section 3: Benchmarks & Evaluation (5 papers)

---

### B1 — SWE-bench: Can Language Models Resolve Real-World GitHub Issues? ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Jimenez2024swebench |
| **Authors** | C. Jimenez, J. Yang, A. Wettig, S. Yao, K. Pei, O. Press, K. Narasimhan |
| **Year** | 2024 |
| **Venue** | ICLR 2024 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

**Note:** The de facto evaluation benchmark for agentic SE systems. Cited by both PDF1 and PDF2 (in text). ICLR peer-reviewed.

---

### B2 — BigCodeBench: Benchmarking Code Generation with Diverse Function Calls and Complex Instructions ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Zhuo2024bigcodebench |
| **Authors** | T. Y. Zhuo, M. C. Vu, J. Chim, H. Hu, et al. |
| **Year** | 2024 |
| **Venue** | arXiv preprint arXiv:2406.15877 |
| **Citations** | — |
| **DOI** | arXiv:2406.15877 |
| **Sources** | ① PDF1 |

**Note:** Richer benchmark than HumanEval — tests diverse function calls and complex multi-step instructions.

---

### B3 — Survey on Evaluation of LLM-based Agents
| Field | Details |
|-------|---------|
| **BibTeX key** | Yehudai2025evalsurvey |
| **Authors** | Asaf Yehudai, Lilach Eden, Alan Li, Guy Uziel, Yilun Zhao, et al. |
| **Year** | 2025 |
| **Venue** | ACL Findings 2025 |
| **Citations** | 67 |
| **DOI** | arXiv:2503.16416 |
| **Sources** | ◆ YOURS |

---

### B4 — Software Testing with Large Language Models: Survey, Landscape, and Vision ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Wang2023testing |
| **Authors** | J. Wang, Y. Huang, C. Chen, Z. Liu, S. Wang, Q. Wang |
| **Year** | 2023 |
| **Venue** | IEEE Transactions on Software Engineering, Vol. 50, pp. 911–936 |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ① PDF1 |

**Note:** IEEE TSE peer-reviewed. Establishes pre-agent-era LLM testing baseline. Different from Wang2023autonomousagents.

---

### B5 — Tokenomics: Quantifying Where Tokens Are Used in Agentic Software Engineering ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Salim2026tokenomics |
| **Authors** | M. Salim, J. Latendresse, S. Khatoonabadi, E. Shihab |
| **Year** | 2026 |
| **Venue** | arXiv preprint arXiv:2601.14470 |
| **Citations** | — |
| **DOI** | arXiv:2601.14470 |
| **Sources** | ① PDF1 |

**Note:** Token-level cost analysis of agentic SE systems — finds iterative review dominates compute costs. Provides quantitative grounding for overhead arguments.

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

---

### C2 — LLM-Based Agentic Systems for Software Engineering: Challenges and Opportunities ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Tang2025challenges |
| **Authors** | Y. Tang, T. Runkler |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2601.09822 |
| **Citations** | — |
| **DOI** | arXiv:2601.09822 |
| **Sources** | ① PDF1 |

**Note:** Argues that better orchestration strategies — not more agents — may be the path forward. Complements Xia2025 (Agentless) in the complexity-vs-simplicity debate.

---

### C3 — Agentic Software Engineering: Foundational Pillars and a Research Roadmap
| Field | Details |
|-------|---------|
| **BibTeX key** | Hassan2025agenticroadmap |
| **Authors** | Ahmed E. Hassan, Hao Li, Dayi Lin, Bram Adams, et al. |
| **Year** | 2025 |
| **Venue** | arXiv (cs.SE) arXiv:2509.06216 |
| **Citations** | ~40 |
| **DOI** | arXiv:2509.06216 |
| **Sources** | ◆ YOURS |

---

### C4 — The Agents Journey: Twenty-Five Years of Multi-agent Systems ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Mascardi2026agentsjourney |
| **Authors** | V. Mascardi, A. Omicini (Eds.) |
| **Year** | 2026 |
| **Venue** | Springer Nature (book) |
| **Citations** | — |
| **DOI** | — |
| **Sources** | ② PDF2 |

**Note:** Edited volume tracing MAS from 2000 to LLM era. Argues current agentic AI recapitulates BDI/JADE-era ideas via natural language. PDF2 uses it to frame the historical continuity argument and call for formal verification inheritance.

---

### C5 — Evaluating Software Process Models for Multi-Agent Class-Level Code Generation ⭐ NEW
| Field | Details |
|-------|---------|
| **BibTeX key** | Shafin2025processmodels |
| **Authors** | W. I. Shafin, M. N. Rafi, Z. Li, T. H. Chen |
| **Year** | 2025 |
| **Venue** | arXiv preprint arXiv:2511.09794 |
| **Citations** | — |
| **DOI** | arXiv:2511.09794 |
| **Sources** | ② PDF2 |

**Note:** First systematic ablation study of multi-agent workflows at class level (ClassEval benchmark, 3 LLMs). Key finding: Waterfall collaboration reduces functional correctness by up to 39.8% while improving code quality metrics. Process design cannot be decoupled from model selection.

---

## Master Reference Index

| # | BibTeX Key | Authors (short) | Year | Venue | Citations | Sources |
|---|-----------|-----------------|------|-------|-----------|---------|
| 1 | Wang2023autonomousagents | Wang et al. | 2023 | Frontiers CS | **2,011** | ◆ |
| 2 | He2025literaturereview | He, Treude, Lo | 2025 | TOSEM (Q1) | 144 | ◆ ① ② |
| 3 | Liu2024agentssurvey | Liu et al. | 2024 | TOSEM (Q1) | 151 | ◆ ① |
| 4 | Guo2024massurvey | Guo et al. | 2024 | arXiv | **761** | ◆ |
| 5 | Guo2025benchmarks | Guo et al. | 2025 | arXiv:2510.09721 | — | ① |
| 6 | Jin2024llmtoagents | Jin et al. | 2024 | arXiv:2408.02479 | ~80 | ① |
| 7 | Jiang2025agenticsolutions | Jiang et al. | 2025 | arXiv:2512.22256 | — | ① |
| 8 | Fan2023llmsse | Fan et al. | 2023 | ICSE-FoSE | — | ① |
| 9 | Zhang2023llmsurvey | Zhang et al. | 2023 | arXiv:2312.15223 | — | ① |
| 10 | Otoum2026systematicreview | Otoum & Elkhalili | 2026 | IEEE Access | — | ② |
| 11 | Hong2023metagpt | Hong et al. | 2023 | ICLR 2024 | **1,475** | ◆ ① ② |
| 12 | Qian2023chatdev | Qian et al. | 2023 | ACL 2024 | 603 | ◆ ① |
| 13 | Wu2023autogen | Wu et al. | 2023 | arXiv | 851 | ◆ ① ② |
| 14 | Huang2023agentcoder | Huang et al. | 2023 | arXiv | 312 | ◆ |
| 15 | Xia2025demystify | Xia et al. | 2024 | PACMSE/FSE | ~400 | ◆ ① |
| 16 | Ishibashi2024soa | Ishibashi & Nishimura | 2024 | arXiv:2404.02183 | — | ② |
| 17 | Zhang2025maad | Zhang et al. | 2025 | FSE 2025 | — | ② |
| 18 | Bui2025seeagent | Bui et al. | 2025 | ASE 2025 | — | ② |
| 19 | Huang2026ecoevolve | Huang | 2026 | — | — | ② |
| 20 | Benkovich2026agyn | Benkovich & Valkov | 2026 | arXiv:2602.01465 | — | ② |
| 21 | Tawosi2025almas | Tawosi et al. | 2025 | ASEW 2025 | < 5 | ② |
| 22 | Ribeiro2025multiagent | Ribeiro et al. | 2025 | WESAAC 2025 | — | ② |
| 23 | Talebirad2023collaboration | Talebirad & Nadiri | 2023 | arXiv | 282 | ◆ |
| 24 | Cai2025designpatterns | Cai et al. | 2025 | arXiv:2511.08475 | < 20 | ◆ |
| 25 | Jimenez2024swebench | Jimenez et al. | 2024 | ICLR 2024 | — | ① |
| 26 | Zhuo2024bigcodebench | Zhuo et al. | 2024 | arXiv:2406.15877 | — | ① |
| 27 | Yehudai2025evalsurvey | Yehudai et al. | 2025 | ACL Findings | 67 | ◆ |
| 28 | Wang2023testing | Wang et al. | 2023 | IEEE TSE | — | ① |
| 29 | Salim2026tokenomics | Salim et al. | 2026 | arXiv:2601.14470 | — | ① |
| 30 | Han2024challenges | Han et al. | 2024 | arXiv | 124 | ◆ |
| 31 | Tang2025challenges | Tang & Runkler | 2025 | arXiv:2601.09822 | — | ① |
| 32 | Hassan2025agenticroadmap | Hassan et al. | 2025 | arXiv:2509.06216 | ~40 | ◆ |
| 33 | Mascardi2026agentsjourney | Mascardi & Omicini | 2026 | Springer (book) | — | ② |
| 34 | Shafin2025processmodels | Shafin et al. | 2025 | arXiv:2511.09794 | — | ② |

---

## Cross-Review Overlap Analysis

**Papers cited by all 3 reviews (highest confidence):**
- He2025literaturereview (#2)
- Hong2023metagpt (#11)
- Wu2023autogen (#13, in text)

**Papers cited by 2 reviews:**
- Liu2024agentssurvey (#3) — ◆ ①
- Qian2023chatdev (#12) — ◆ ①
- Xia2025demystify (#15) — ◆ ①

**Papers unique to your filtered_papers.md:**
- Wang2023autonomousagents (#1), Guo2024massurvey (#4), Huang2023agentcoder (#14), Han2024challenges (#30), Talebirad2023collaboration (#23), Yehudai2025evalsurvey (#27), Hassan2025agenticroadmap (#32), Cai2025designpatterns (#24)

**Papers unique to PDF1 (classmate 1):**
- Guo2025benchmarks (#5), Jin2024llmtoagents (#6), Jiang2025agenticsolutions (#7), Fan2023llmsse (#8), Zhang2023llmsurvey (#9), Jimenez2024swebench (#25), Zhuo2024bigcodebench (#26), Wang2023testing (#28), Salim2026tokenomics (#29), Tang2025challenges (#31)

**Papers unique to PDF2 (S. Fang):**
- Otoum2026systematicreview (#10), Ishibashi2024soa (#16), Zhang2025maad (#17), Bui2025seeagent (#18), Huang2026ecoevolve (#19), Benkovich2026agyn (#20), Tawosi2025almas (#21), Ribeiro2025multiagent (#22), Mascardi2026agentsjourney (#33), Shafin2025processmodels (#34)

---

## Priority Tiers for Next-Step Analysis

### Tier 1 — Use in any synthesis (already validated, high citation)
Papers #1–4, #11–15 (your 14 core papers minus flex slot)

### Tier 2 — Strong additions from classmates (high venue quality or citation count)
| # | Paper | Reason to elevate |
|---|-------|------------------|
| #25 | Jimenez2024swebench | ICLR; the benchmark used by everyone |
| #10 | Otoum2026systematicreview | IEEE Access SLR; unique field-growth statistics |
| #6 | Jin2024llmtoagents | ~80 cites; fills LLM-vs-agent distinction gap |
| #20 | Benkovich2026agyn | Production-deployed; 72.2% SWE-bench; no benchmark tuning |
| #19 | Huang2026ecoevolve | SWE-bench 62.3% Verified; experiential learning angle |
| #34 | Shafin2025processmodels | Only ablation study of workflow stages; model–process interaction |
| #18 | Bui2025seeagent | ASE 2025; human study; only effort-estimation paper |

### Tier 3 — Useful if specific themes are covered
| # | Paper | Theme |
|---|-------|-------|
| #29 | Salim2026tokenomics | Cost / token analysis |
| #31 | Tang2025challenges | Complexity vs. simplicity debate |
| #5 | Guo2025benchmarks | Benchmark landscape depth |
| #33 | Mascardi2026agentsjourney | Historical MAS lineage / BDI |
| #16 | Ishibashi2024soa | Scalability via functional decomposition |

### Tier 4 — Background / supplementary only
#7, #8, #9, #21, #22, #26, #28 — lower venue quality, narrow scope, or superseded by stronger papers

---

*Generated: 2026-05-16 | Sources: filtered_papers.md (14 confirmed papers) + 54154F3E PDF (14 refs) + Literature_Review_MultiAgentSE PDF (12 refs) | Deduplication method: author + year + DOI matching*
