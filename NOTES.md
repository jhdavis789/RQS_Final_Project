# Notes

Append-only log of tidbits, facts, decisions, and source material. Newest entries at bottom. Every entry is dated and sourced (user conversation, external URL, document, etc.).

---

## 2026-04-20 — initial brief

- Project is a final presentation for work done inside **Capital Group's Risk and Quantitative Services (RQS)** department. (source: user)
- Capital Group is an **active asset manager**; the project sits within the **bond / fixed income** space. (source: user)
- Format: **short main presentation + large appendix** covering additional questions. (source: user)

## 2026-04-20 — project topic

**Topic: Behavioral biases in investment portfolios.** Approached through experiments on real Capital Group portfolios. Two sides: (A) analysts, (B) portfolio managers (user to provide next).

### Context on Capital Group structure
- Analysts run **their own portfolios within their coverage areas** — they are not pure research staff; they allocate capital.
- Analysts regularly **write notes**.

### Experiment set A — analysts (three sub-experiments)

**A1. Analyst confidence levels in written notes → excess returns**
- Used AI to extract confidence levels from analyst notes over time.
- Related confidence time-series to **excess returns vs. market**.
- **Finding A1a — analysts don't communicate equally.** Baseline expressed confidence differs across analysts. The useful signal is an analyst's current confidence **as a percentile of their own historical distribution** (e.g., 70th vs. 20th of *their own* range), not the absolute linguistic level.
- **Why it matters for a PM:** PMs want *actual* confidence, but they only observe *communicated* confidence. Normalizing per-analyst lets the PM calibrate across a heterogeneous analyst bench.

**A1b. Confidence–return relationship is not monotonic for all analysts.**
- Some analysts deliver better returns in their **extreme** confidence periods (very high OR very low).
- Implication: the tails of an analyst's confidence distribution may carry more signal than the middle.

**A1c. Horizon compression under stress (rates analysts, 2022).**
- During the 2022 underperformance period, rates analysts' time horizons in their notes **shrank considerably** — from long-horizon framing to much shorter-horizon framing.
- **Effect was consistent across multiple analysts** — not an individual quirk.

### Experiment set B — portfolio managers

**B1. How do PMs manage money in times of crisis?**
- Method: examined PM portfolios during **periods of elevated volatility** (stress windows).
- Analyzed **trades executed during those windows**.
- Core analysis: decompose trades into those that **move the portfolio further from the benchmark** (active-risk-up) vs. those that **move closer to the benchmark** (active-risk-down), and measure which direction performs in stress.
- **Ultimate question:** *Are PMs better investors relative to the market in calm vs. stressful times?* — i.e., does PM alpha-per-unit-trade go up or down when volatility is high?
- User's phrasing: high-volatility periods are very stressful; the question is whether PMs' decision quality holds up, degrades, or improves under that stress.
- (Specific results / directions of the findings pending — user to confirm what was found.)

**User's research priorities for the PM side — MUST-HAVE in appendix:**
1. **Fight vs. flight — neuroanatomy.** Which brain regions activate during each? How does each modify approach to logic and decision-making? The fight/flight distinction is the core mechanistic frame for this section.
2. **Market-level psychology.** Is there research on how individual stress psychology aggregates into *market* pricing and behavior? (i.e., the micro-to-macro bridge — from cortisol on a trading floor to VIX and flow patterns.)

### User's desired framing
- **Thesis (user's own words, high-level):** "Better understanding of psychology and of the way our brains tick allows us to overcome the natural human barriers and biases that we have built into us."
- Presentation must be grounded in **science at the mechanism level** — ideally down to **neurochemistry / hormones / brain regions** — then quickly connect that mechanism to the **empirical evidence found in our experiments.**
- Audience: PMs and analysts. Needs to give them something **actionable**.
- User wants both (a) the high-level math/mechanism, and (b) the specific evidence in our data.
- If research exists showing that understanding one's own biases reduces their impact, user wants that as a slide.
