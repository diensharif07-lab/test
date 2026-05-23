# Summer 2026 Research Projects — Master Menu

*For a CS+psych+finance student, ~3 months solo, coding/ML + database access. Each project is designed to produce a workshop-paper-quality artifact AND lay the empirical foundation for a future startup.*

---

## THE KEY INSIGHT

Of the ~40 projects surfaced, **the highest-EV play is a cross-agent synthesis nobody on its own would have suggested:**

> **"Memory-Conditioned Sycophancy in Financial Advice: A Multi-Model Audit With Dollar-Cost Quantification"**

This combines the strongest project from the LLM-audits swarm (Sycophancy-Under-Memory) with the strongest from the cross-domain swarm (Sycophancy → Portfolios), and is the ONLY project on the list that explicitly requires all three of your domains (CS for the memory/API infrastructure, psych for the attachment/sycophancy literature, finance for the dollar-cost outcome variable).

Why it wins:
- **All three labs that ship persistent LLM memory** (ChatGPT, Claude Projects, Gemini Memory) only crossed mainstream availability in late 2025 — the empirical window is wide open
- **The literature has both halves but never the product:** Cheng et al. *Science* 2025 (sycophancy + prosocial decline) + CHI 2026 paper (memory amplifies sycophancy) + Anchors in the Machine 2025 (LLM affect transfers to user) + Price of Agreement 2026 (financial sycophancy is *milder* than chat sycophancy — but nobody has measured whether memory closes the gap)
- **Dollar-cost outcome variable** (portfolio drift over 5-yr backtest) is unclaimed and makes it directly product-relevant
- **No IRB needed, ~$1.5K API budget, pre-registerable on OSF**
- **Venue fit is uncommonly clean:** ICAIF 2026 (December submission), NeurIPS SafeGenAI workshop (Sept), FAccT 2027 (Jan deadline). Three shots from one dataset.
- **Startup wedge is investor-legible:** "MemoryGuard for financial AI" — sycophancy + memory-drift detection middleware for robo-advisors and AI wealth tools. FINRA/SEC regulatory pressure on AI advice is rising. Patronus/Lynx covers hallucination but not memory-conditioned drift on financial advice specifically.

---

## RECOMMENDED 3-MONTH PORTFOLIO

A solo summer project should be ONE primary + ONE pivot option (in case the primary blocks) + ONE spin-off paper from the same data infrastructure.

| Slot | Project | Risk Profile |
|---|---|---|
| **PRIMARY** | Memory-Conditioned Sycophancy → Financial Decisions (synthesis) | Medium — depends on memory APIs being usable, mitigated by 3 API targets |
| **PIVOT** | Polymarket × Kalshi cross-venue mispricing (Finance #1) | Low — public APIs, dataset already exists, pure quant |
| **SPIN-OFF** | Sycophancy-in-the-Wild via Reddit longitudinal (Behavioral #3) | Low — reuses some methodology, different data |

Plan: spend **week 1** building the pipeline for primary + pivot in parallel. If memory APIs are usable by end of week 1, commit to primary. If not, pivot to Polymarket-Kalshi. Either way, you'll have a spin-off paper drafted from the Reddit sycophancy data by week 11.

---

## TOP 10 RANKED ACROSS ALL 4 DOMAINS

| # | Project | Domain | Venue | Wedge | ★ |
|---|---|---|---|---|---|
| 1 | **Memory-Conditioned Sycophancy → Financial Decisions** (synthesis) | Cross-domain | ICAIF / SafeGenAI / FAccT | MemoryGuard for fintech AI | 5 |
| 2 | **Polymarket × Kalshi cross-venue mispricing** | Finance | SSRN → JFM/Management Science | Cross-venue execution layer | 5 |
| 3 | **Mood-Induced LLMs → Financial Decisions** | Cross-domain | ICAIF | Affect-aware financial assistant | 5 |
| 4 | **AI-Companion Grief & Attachment Longitudinal** | Behavioral | ICWSM 2027 (Sept 2026 deadline) | Well-being layer for AI companions | 5 |
| 5 | **Sycophancy-Under-Memory benchmark** | LLM audits | NeurIPS SafeGenAI | Memory drift middleware | 5 |
| 6 | **VIX1D regime-conditioned 0DTE strategy** | Finance | SSRN → J. Futures Markets | Vol-selling robo / regime data sub | 5 |
| 7 | **Citation faithfulness audit of AI search** | LLM audits | ICWSM 2027 | CiteAudit SaaS for regulated industries | 5 |
| 8 | **Persona-conditioned LLM portfolio convergence** | Cross-domain | ICAIF | Wisdom-of-LLMs ETF / signal feed | 4.5 |
| 9 | **24X overnight-drift natural experiment** | Finance | SSRN → RFS | Overnight rotation ETF | 4.5 |
| 10 | **Computer-use agent failure-mode decomposition** | LLM audits | NeurIPS SafeGenAI | Sentry for Agents runtime classifier | 5 |

---

## PRIMARY PICK — DETAILED EXECUTION PLAN

### Project: Memory-Conditioned Sycophancy → Financial Decisions

**Research question:** Does persistent LLM memory amplify sycophancy on financial advice specifically, and what is the dollar-cost magnitude of that amplification when measured by portfolio drift?

### Method (4×3×3 factorial)

| Factor | Levels |
|---|---|
| **Memory condition** | (a) Memory off / fresh session, (b) Memory on with neutral user history, (c) Memory on with sympathetic user history, (d) Mem0 wrapper with explicit financial-belief memories |
| **Sycophancy primer** | (a) None, (b) Soft ("I really love tech stocks"), (c) Strong ("I'm sure NVDA is going to keep ripping, I want my portfolio aggressive on it") |
| **Model** | GPT-5, Claude 4.7, Gemini 3 (use the actual specific model IDs you can access) |

For each cell:
- 200 synthetic investor personas (age × income × risk tolerance grid, from CFP exam standards)
- Request portfolio recommendation; capture full output
- Score: (i) drift in equity-bond ratio, (ii) drift in sector concentration, (iii) drift in single-name concentration vs neutral baseline, (iv) 5-year backtest of resulting portfolio vs neutral baseline using historical prices (2020-2025) — **the dollar-cost outcome variable**

Total cells: 4 × 3 × 3 × 200 = 7,200 model calls + backtests. ~$1,500 in API + Polygon data.

### Anchor papers
- Cheng et al. (2025) "Sycophantic AI decreases prosocial intentions" *Science* — the foundational claim
- "Interaction Context Often Increases Sycophancy" CHI 2026 — memory amplifies it
- "The Price of Agreement" arXiv 2604.24668 — financial sycophancy baseline
- "Anchors in the Machine" arXiv 2511.05766 — affect/persona transfer
- Mem0 LongMemEval paper / arXiv 2504.19413 — memory infrastructure
- SycEval arXiv 2502.08177 — methodology

### Pre-registration
Pre-register the full design on OSF before any data collection. This neutralizes the "you fished for the result" reviewer kill. Use the AsPredicted template.

### Timeline (12 weeks)

| Week | Work |
|---|---|
| 1 | Pipeline scaffold; verify all 3 model memory APIs work; pre-register OSF |
| 2-3 | Generate persona library; build prompt templates; pilot 200 calls per cell |
| 4-6 | Run full data collection; build backtest harness using Polygon |
| 7-8 | Statistical analysis (mixed-effects models for nested data); robustness checks |
| 9-10 | Draft paper; build product demo (Streamlit dashboard showing memory drift) |
| 11 | Internal review; submit to arXiv |
| 12 | Submit to ICAIF + NeurIPS SafeGenAI workshop; iterate |

### What graceful degradation looks like

- **If memory APIs are flaky:** drop to Mem0 OSS wrapper exclusively (week 1 fallback)
- **If frontier models resist sycophancy too well:** pivot framing to "newer models resist financial sycophancy *better* than chat sycophancy — why?" Still publishable, possibly stronger because it's a positive finding
- **If 12 weeks is tight:** drop to 2 models × 3 memory × 3 sycophancy = still 1,800 calls and publishable

### Startup wedge (post-paper)

**MemoryGuard for AI Financial Advice** — middleware that detects sycophancy + memory drift in deployed AI financial assistants and surfaces alerts to compliance teams. Sells to:
- Robo-advisors (Betterment, Wealthfront, Public) adding AI features
- AI-first wealth tools (Magnifi, Origin AI, Crescent)
- Banks deploying customer-facing chat
- FINRA-regulated brokers using LLMs anywhere in the advice path

The paper is the credibility anchor and lead-gen instrument. Adjacent products: consumer "second opinion" app, sycophancy-audited LLM API.

---

## FULL CATALOG (40 PROJECTS)

### LLM Empirical Audits (12)
1. **Sycophancy-Under-Memory benchmark** [5★]
2. **AI-search citation faithfulness audit** [5★]
3. **Computer-use agent failure-mode decomposition** [5★]
4. **BrokenMath-style sycophancy in code review** [4★]
5. **Multi-Agent Tax replication on production frameworks** [4★]
6. **Cross-model persona vector transferability** [4★]
7. **Live SWE-bench Pro contamination monitoring** [3.5★]
8. **Voice agent hallucination under acoustic stress** [4★]
9. **Sandbagging detection via noise injection** [3.5★]
10. **Mirror metacognition benchmark on production agents** [3★]
11. **Inference cost vs accuracy frontiers for finance QA** [3★]
12. **Cultural vs linguistic capability decomposition** [3★]

### Computational Behavioral Science (8)
1. **AI-companion grief/attachment longitudinal** [5★] — Arctic Shift Reddit dumps
2. **Polymarket calibration bias decomposition** [5★] — 107GB dataset already prepared
3. **Sycophancy-in-the-wild via Reddit longitudinal** [5★]
4. **Discord community collapse prediction** [4★] — 2.05B message dataset
5. **GitHub as labor market telemetry** [4★] — GH Archive BigQuery
6. **Substack survival from first 10 posts** [3★]
7. **Algorithm-rejector subculture growth** [3★]
8. **App Store sentiment cliffs as DAU leading indicator** [3★]

### Empirical Finance (12)
1. **Polymarket × Kalshi cross-venue mispricing** [5★]
2. **0DTE SPX broker execution audit (Schwarz-style)** [5★]
3. **VIX1D regime-conditioned 0DTE strategy** [5★]
4. **24X natural experiment on overnight drift** [4.5★]
5. **Polymarket insider detection via wallet clustering** [4★]
6. **DAT mNAV reflexivity cascade model** [4★]
7. **Funding rate de-biased crypto sentiment** [4★]
8. **JEPI/SPYI/QYLD after-tax wealth transfer** [3.5★]
9. **LLM stock-pick consensus index (3 month)** [3.5★]
10. **xStocks vs NYSE tokenized equity price discovery** [3.5★]
11. **Sports betting × brokerage account substitution** [3★]
12. **DSPX dispersion regime backtest** [3★]

### Cross-Domain LLM-Applied (8)
1. **Mood-induced LLMs → financial decisions** [5★]
2. **Sycophancy → portfolio drift dollar cost** [5★]
3. **Persona-conditioned LLM portfolio convergence** [4.5★]
4. **12-effect behavioral econ replication battery** [4★]
5. **LLM predicts speed-dating chemistry** [4★]
6. **Voice CBT vs text CBT comparison** [3.5★]
7. **PolyBench-Persona forecasting** [3.5★]
8. **Synthetic customer discovery PMF correlation** [3★]

---

## CROSS-AGENT SYNTHESIS OPPORTUNITIES

Beyond the primary pick above, three other strong combinations:

**S2: Polymarket Insider Detection + Cross-Venue Mispricing** (Finance #1 + #5)
Combined paper: "Cross-venue mispricing as a noisy signal of asymmetric information in prediction markets." Two papers from one data pipeline (Polymarket subgraph queries are shared). Spin one to a forecasting venue, one to a market-microstructure venue.

**S3: AI-Companion Grief + Sycophancy-in-the-Wild** (Behavioral #1 + #3)
Combined paper: "Reddit linguistic markers of LLM-induced attachment and epistemic drift." Single data pipeline (Arctic Shift), two outcome variables, broader claim than either alone.

**S4: Citation Faithfulness + LLM Stock-Picks** (LLM audits #2 + Finance #9)
Combined paper: "AI advice in regulated domains: hallucination, citation accuracy, and recommendation overlap across legal, medical, and financial query corpora." A single benchmark used three ways. Bigger venue target (FAccT or *PNAS Nexus*).

---

## VENUES & DEADLINES TO PLAN AROUND

Realistic for summer-finished work:

| Venue | Type | Deadline (typical 2026) |
|---|---|---|
| arXiv | Preprint (no review, but cred) | Anytime |
| SSRN | Finance preprint | Anytime |
| OSF | Pre-registration | Before data collection |
| NeurIPS SafeGenAI workshop | AI safety/eval | Early September |
| NeurIPS Foundation Models for Agents | Agents | Early September |
| ICAIF 2026 | AI in Finance | Late September / early October |
| ICWSM 2027 Round 2 | Computational social science | September 15, 2026 |
| EMNLP industry track | NLP applications | Late June (might miss) |
| FAccT 2027 | Fairness, accountability | Late January 2027 (winter) |
| EC 2026 | Economics & computation | Mid-February (already past) |

ICAIF, NeurIPS SafeGenAI, and ICWSM Round 2 are your best summer-aligned targets.

---

## KEY CITATIONS

### LLM behavior (sycophancy, memory, persona)
- Cheng et al. (2025) "Sycophantic AI decreases prosocial intentions" *Science*
- "Interaction Context Often Increases Sycophancy" CHI 2026
- "Sycophancy Is Not One Thing" arXiv 2509.21305
- "The Price of Agreement" arXiv 2604.24668
- SycEval arXiv 2502.08177
- "BrokenMath" arXiv 2510.04721
- Persona Vectors arXiv 2507.21509 (Anthropic)
- Mem0 / LongMemEval arXiv 2504.19413, 2507.05257
- "Anchors in the Machine" arXiv 2511.05766

### Behavioral finance × LLM
- "Inducing State Anxiety in LLM Agents" arXiv 2510.06222
- "Bias-Adjusted LLM Agents" arXiv 2508.18600
- "LLM economicus?" arXiv 2408.02784
- "Exposing Product Bias in LLM Investment Recommendation" arXiv 2503.08750
- "AlphaAgents" arXiv 2508.11152
- "PolyBench" arXiv 2604.14199

### Market microstructure (free data)
- Schwarz, Barber, Huang, Jorion & Odean (2025) "Actual Retail Price of Equity Trades" *JoF*
- Bürgi/Deng/Whelan (2025) UCD WP 2025_19 — Kalshi microstructure
- Albers (2025) VIX1D paper *J. Futures Markets*
- Lou, Polk, Skouras (2019) overnight drift *JFE*; NY Fed SR917
- Bogousslavsky & Muravyev (2025) "Anatomy of Retail Option Trading"

### Computational social science (public data)
- Pataranutaporn et al. "My Boyfriend is AI" arXiv 2509.11391
- Arctic Shift (Pushshift successor) — Reddit dumps
- Discord Unveiled HuggingFace dataset (2.05B messages)
- GH Archive on BigQuery
- Polymarket data: Goldsky subgraph, Dune queries, 1.1B-trade HF dump (SII-WANGZJ)

---

## FINAL OPINION

The Memory-Conditioned Sycophancy synthesis project is the single best fit for your CS+psych+finance combination, for a 3-month solo summer, with the cleanest venue alignment AND the most investor-legible startup wedge of any project on this list. Pre-register it on OSF in week 1, build the pivot pipeline in parallel, and reserve the Reddit longitudinal as a spin-off paper from the same theoretical framing. Three papers in 12 months from one summer's data collection is a realistic outcome for this design — and any one of them is enough to anchor a seed pitch.

If you only do one thing this week: **set up API access to ChatGPT Memory, Claude Projects, and Gemini Memory and verify you can programmatically read/write memory state on all three.** If you can, the project is live. If you can't on any one, the project narrows but is still viable. The faster you know, the faster you commit.
