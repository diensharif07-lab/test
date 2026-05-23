# Research Playbook: From Wedge to Conviction

*How to take any of the 65 wedges from "interesting research finding" → "I'd commit a year to this." 3 phases, each with explicit kill criteria.*

---

## The Funnel

```
65 wedges  →  Phase 1 (triage)        →  ~5 survivors
 5 wedges  →  Phase 2 (validation)    →  ~2 contenders
 2 wedges  →  Phase 3 (deep dive)     →  1 commitment
```

Total elapsed time: 3-4 weeks of focused work. Don't compress this — the cost of researching the wrong wedge for 6 months is way higher than spending 4 weeks triaging.

---

## Phase 1 — 30-min sanity check (per wedge)

**Goal:** kill the wedges that look strong on paper but die on first contact with reality.

**Five checks, 5-6 min each:**

1. **Read the anchor paper's abstract + discussion section.** The discussion is where authors admit limitations. If the limitations gut your thesis, kill it now.
2. **Google "[finding] replication" and "[finding] rebuttal."** Most landmark findings have published critiques within 18 months. Read the strongest one.
3. **Pull the closest competitor's last funding round and last product release.** Crunchbase + their changelog/blog. If they're well-funded AND shipping fast, you're entering a war, not finding white space.
4. **Search Reddit / HN / X for "I wish there was X" / "why doesn't X exist."** If you can't find a single organic complaint about the status quo, there's no demand.
5. **Write three sentences:** Is the finding real? Is the market real? Is the gap real? If you hesitate on any one, kill it.

**Kill criteria (any one):**
- Anchor paper failed a high-profile replication
- A well-funded player ($100M+) is already shipping in the exact wedge
- You can't articulate the customer's current behavior in one sentence
- The regulatory path is "we'll figure it out" (only acceptable answer for pure SaaS)

**Time budget:** 30 min × 15 top wedges = ~7.5 hours. Should kill 10, leaving ~5 survivors.

---

## Phase 2 — Validation (per surviving wedge, ~2 days each, ~10 days total)

Four parallel research streams. Each gets ~half a day.

### A) Science track
- Read the anchor paper end-to-end + the 2 most-cited follow-ups
- Google Scholar "cited by" filter — what's the recent work say?
- Look explicitly for **negative results** and failed replications (often unpublished — search OSF, PsyArXiv)
- **Cold-email the principal investigator.** This works shockingly well. "I'm building X based on your finding, can I get 15 min to ask 3 questions?" → ~30% response rate.

### B) Market track
- Every funded startup in the space, last 5 years, via Crunchbase + Pitchbook
- For each: total raised, last announcement, LinkedIn headcount trend, Glassdoor reviews
- Find the **failure post-mortems** (Bench, Geneva, Lunchclub all wrote them). Failed startups are the most underrated research source.
- Google Trends + SimilarWeb on the closest competitor's domain

### C) Customer track *(most important — most founders skip)*
- List 10 prototypical customers (specific people, not personas)
- Cold DM/email 20 to get 5 calls
- **The signal you're looking for: visible emotional response.** Lukewarm interest = no startup.
- Run a Carrd landing page + $200 of ads to a fake product → real CAC signal in 48 hours

### D) Risk track
- **Pre-mortem:** "It's 24 months later and this startup is dead. Why?" Write 5 plausible answers.
- **Regulatory check:** FDA / SEC / state licensure for anything in health, finance, or behavioral
- **Back-of-envelope unit economics:** CAC, LTV, gross margin. If you can't get to LTV/CAC > 3 with realistic assumptions, kill it.
- **Incumbent threat:** could Apple/Google/Stripe/OpenAI build this in 6 weeks if they wanted to?

**Kill criteria (any one):**
- Customer track returned lukewarm
- Unit economics need >$200 CAC with <$30 ARPU
- Regulatory pathway is unclear AND product is in a regulated category
- An incumbent could ship in 6 weeks

**After ~10 days:** you should have 2 contenders.

---

## Phase 3 — Deep dive (per finalist, ~1-2 weeks)

By this point you're not researching the wedge, you're researching whether **you** are the right person to build it.

1. **Domain co-founder search.** If you're not the domain expert, can you recruit one in 30 days? If no, deprioritize.
2. **Paper-prototype MVP.** Figma + a Notion landing page is enough.
3. **Get 5 paying customers.** Real money. Even $1 counts. Pre-payment proves the willingness-to-pay you measured in Phase 2.
4. **Talk to 5 VCs — NOT to pitch.** Tell them you're researching the space. Ask: "what would have to be true for you to write a check?" Their objections are your research agenda.
5. **Write the seed memo as the investor.** Find the holes you'd attack.

**Kill criteria:**
- Can't get 5 paying customers in 2 weeks
- VC objections cluster around the same issue and you can't refute it
- You realize you don't actually want to wake up thinking about this every day for 5 years

---

## Domain-specific research sources

### Health / longevity wedges
- **ClinicalTrials.gov** — ongoing trials in your indication
- **FDA Orange Book** — patent expiry on key molecules (free generics = no pharma moat for you)
- **FDA's "Reasonable Expectation of Effectiveness"** filings (Loyal precedent for vet)
- **Reach out to the PI** of the anchor study — they often want their finding to become a product
- **AMA / state medical board rules** for telehealth scope-of-practice in your target states
- Substacks: *Drug Hunter*, *Endpoints News*, *MedCity News*

### AI capability wedges
- **arXiv daily** in your subfield + Papers with Code leaderboards
- **METR Time Horizon** updates monthly — track the actual reliability curve
- **Hugging Face trending** — what's getting community traction
- **HN "Show HN"** — adjacent products and reception
- **Cursor/Claude Code/Cline GitHub issues** — what users complain about
- Substacks: *Latent Space*, *Interconnects*, *The Pragmatic Engineer*

### Market / fintech wedges
- **SSRN + NBER** recent papers
- **Fed Notes + FSOC + OFR reports** for systemic-risk signals
- **SEC EDGAR** for adjacent player 10-Ks and S-1s — read the "Risk Factors" section
- **CFTC + state regulator filings** for prediction markets, derivatives, crypto
- **Crunchbase + Pitchbook** for funding history
- Substacks: *Net Interest* (Marc Rubinstein), *Doomberg*, *FedGuy* (Joseph Wang)

### Behavioral / consumer wedges
- **Google Scholar alerts** for key authors (Aron, Finkel, Epley, Dunbar, Haidt, Keltner)
- **Pew Research** monthly + **Edelman Trust Barometer** annual
- **Sensor Tower / App Annie** for adjacent app revenue/MAU
- **Reddit subreddit growth** (subredditstats.com) as demand signal
- **TikTok / X search** for "I wish [product] existed" — direct customer voice
- Substacks: *After Babel* (Haidt), *Slow Boring*, *The Honest Broker*

---

## Per-wedge artifacts to produce

By end of Phase 2 for each surviving wedge:

1. **One-page memo** — claim, evidence (3 citations), market size, customer, why-now, what kills it
2. **Competitor matrix** — 10 players × 8 dimensions (raised, last release, traction, headcount, pricing, gap)
3. **5-person interview synthesis** — direct quotes, current behavior, willingness-to-pay
4. **Pre-mortem doc** — 5 plausible 24-month death scenarios + mitigations
5. **MVP scope** — what specifically ships in 6 weeks?

If you can't produce all 5 artifacts at Phase 2 close, you don't actually understand the wedge.

---

## Using agent swarms in this process

This is where the leverage compounds. Sample budget: **60 agent runs across 3 weeks, ~$100-300 in API spend, 10-30× faster than doing alone.**

### Phase 1 triage swarms
One agent per wedge with a tight prompt:
> "30-min sanity check on [wedge]. Tasks: (1) summarize the anchor paper's claim AND its limitations section, (2) find the strongest published rebuttal or failed replication, (3) list 5 closest funded competitors with last raise and last product release, (4) find 3 organic customer complaints about the status quo on Reddit/HN/X. Output: 400 words + a kill/keep recommendation with reasoning."

### Phase 2 validation swarms (4 streams per wedge × 5 wedges = 20 agents)
- Science agent: "deep-read anchor paper + 5 most-cited follow-ups + look for negative results"
- Market agent: "build competitor matrix; pull funding history, Glassdoor signal, headcount trends"
- Customer agent: "scrape 100 Reddit/HN/X posts in [community]; cluster by pain; identify 20 specific interview targets"
- Risk agent: "5-cause pre-mortem; regulatory path; unit economics back-of-envelope"

### Phase 3 deep-dive specialty agents
- Memo agent: "draft the seed memo as a skeptical investor"
- Founder-search agent: "find 50 domain experts in [field] with founder potential signals (left big-co, building on side, has audience)"
- Pricing agent: "build outcome-priced vs subscription model comparison with sensitivity tables"

---

## Common research mistakes

1. **Falling in love with the anchor paper.** Always read the rebuttal first.
2. **Conflating "I would use this" with "the market will buy this."** You are not the customer.
3. **Skipping customer calls** because "I already know what they want." You don't.
4. **Underweighting incumbents** that could build this in 6 weeks (Apple, Google, Meta, OpenAI, Stripe). If they could and they're not, ask why — usually the answer is margin cannibalization, which can become *your* moat.
5. **Treating "founder needs" as universal needs.** Most founder-built products that flop are scratching the founder's own itch.
6. **Not pricing the regulatory tail.** One FDA warning letter or SEC inquiry kills a year.
7. **Building before getting 5 paying customers' money in hand.** Pre-payment is the only validation that matters.
8. **Treating capability as availability.** "GPT-5 can do this" ≠ "this works reliably enough to sell."

---

## What good looks like at end of process

- You can defend the wedge against the top 3 objections in 30 seconds each
- You have 5 paying customers (even $1)
- You have a co-founder or a credible plan for one
- You have a 6-week MVP scope
- You can explain why an incumbent hasn't built this AND why they won't in the next 12 months
- You want to wake up thinking about this for 5 years

If all six are true → commit. If not → cycle back to Phase 2 with the next contender.
