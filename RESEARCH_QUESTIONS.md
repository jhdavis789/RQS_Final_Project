# Research Questions

For each empirical finding from our experiments, we want the **mechanism-level science** (brain region, neurotransmitter, hormone, cognitive process) that explains it — and then a **bridge** from that mechanism directly to our data. This file drives the literature review.

---

## Analyst side

### A1a. Heterogeneous baseline confidence across analysts
**Empirical finding:** Analysts differ systematically in the absolute level of confidence they express in writing. Relative (percentile-of-own) confidence is the useful signal, not absolute.

**Research questions:**
1. **Individual differences in confidence expression vs. internal confidence.** How well do people's *communicated* confidence and *felt* confidence track? (Moore & Healy 2008 — overestimation / overplacement / overprecision taxonomy.)
2. **Neural basis of metacognitive confidence.** Where in the brain is "confidence" represented and generated? (Stephen Fleming's work on rostrolateral prefrontal cortex as a metacognitive hub; Kepecs on orbitofrontal neurons coding decision confidence.)
3. **Why calibration differs across people.** Grey-matter volume / connectivity differences in aPFC predict metacognitive accuracy (Fleming, Weil, Nagy, Dolan, Rees 2010).
4. **Linguistic markers of certainty/uncertainty in expert writing.** Hyland's hedging literature — how academic and professional writers encode epistemic stance. Can these markers be validated against behavioral outcomes?
5. **LLM-based stance/confidence extraction** — prior art on using NLP to measure epistemic confidence in financial / medical / legal text. What's the validation gold standard?

**Bridge to our data:** We operationalize "confidence" via AI analysis of analyst notes. If metacognitive calibration is a stable individual trait with a neural substrate, **per-analyst normalization isn't just a statistical convenience — it's the only way to recover the biological signal** (each person's brain has a different set-point).

---

### A1b. Non-monotonic (tail-weighted) confidence–return relationship
**Empirical finding:** For some analysts, excess returns are strongest when their confidence is at the extreme ends of their own distribution (very high OR very low), not in the middle.

**Research questions:**
1. **Skill–confidence relationship.** Dunning–Kruger (1999) — peaks and troughs in confidence across skill levels. Does the inverted relationship apply here, or is something else going on?
2. **Calibrated confidence in expert decision-makers.** Does expert confidence track truth better at the extremes? (Literature on weather forecasters, bridge players, chess — experts show better calibration than novices, with particularly reliable extremes.)
3. **Conviction premium in active management.** Does sizing-with-conviction drive alpha? (Cremers & Petajisto 2009 "Active Share"; Wermers on high-conviction positions; "best ideas" portfolio literature.)
4. **Neuroscience of certainty at the extremes.** Neural representations of certainty vs. uncertainty differ qualitatively (not just in magnitude) — activity in ACC, OFC, insula changes character. (Platt & Huettel 2008 on risk/ambiguity representation; de Berker et al. on uncertainty physiology.)
5. **Knowing you don't know.** "Recognized uncertainty" as a profitable state — if an analyst's low-confidence signal is well-calibrated, acting on it (e.g., *not* trading, or trading the other way) produces alpha. Literature on epistemic humility and decision quality.

**Bridge to our data:** The middle of the distribution is where the brain's confidence and accuracy signals are noisiest; the tails are where metacognitive discrimination is sharpest. This makes the U-shape a *prediction of the neuroscience*, not just an artifact.

---

### A1c. Horizon compression under stress (rates analysts, 2022)
**Empirical finding:** During the 2022 rates drawdown, multiple rates analysts' time horizons in their written notes shrank — from long-horizon framing to short-horizon framing. Effect was consistent across analysts.

**Research questions:**
1. **Myopic loss aversion.** Benartzi & Thaler (1995) — people become more loss-averse when evaluating outcomes over shorter horizons. Drawdowns shrink evaluation horizons, which amplifies loss aversion, which compresses evaluated horizons further. Feedback loop.
2. **Neuroendocrine stress response in traders.** John Coates ("The Hour Between Dog and Wolf," and Coates & Herbert 2008 on cortisol in City traders) — acute losses raise cortisol; sustained cortisol elevation shifts decision-making toward threat-avoidance and short-horizon thinking via effects on PFC and amygdala.
3. **Stress narrows attention.** Easterbrook (1959) cue-utilization hypothesis — arousal narrows the range of cues attended to. Modern replications: acute stress shifts from goal-directed (prefrontal) to habitual (striatal) control (Schwabe & Wolf 2009, 2013).
4. **Temporal discounting under stress/cortisol.** Cortisol administration and acute stress both **increase delay discounting** — short-term rewards weighted more heavily (Kimura et al. 2013; Haushofer & Fehr 2014 on stress and economic decision-making; Sousa & Almeida 2012 review).
5. **Drawdown-driven horizon compression in professional investors.** Is this documented outside our sample? (Behavioral finance literature on disposition effect, loss-aversion during drawdowns — Frazzini 2006, Shapira & Venezia 2001.)
6. **2022 bond market specifically.** Rates regime change — fastest Fed hiking cycle in decades. What was the cross-industry record of time-horizon shift in rates research during this period?

**Bridge to our data:** The 2022 horizon compression we measured is the written-output signature of a well-characterized neuroendocrine stress pathway. This isn't "sentiment" — it's a physiology read-through.

---

## Portfolio manager side

### B1. PM decision quality under volatility stress
**Empirical finding (framing):** During high-volatility / crisis windows, we analyze PM trades and decompose them into (a) trades that move the portfolio **further from benchmark** (active-risk-up) and (b) trades that move it **closer to benchmark** (active-risk-down). We ask: are PMs better investors relative to the market in calm times or stressful times?

*(Specific direction of our results pending — user to confirm.)*

**Research questions — MUST-HAVE for the deck and appendix per user instruction:**

#### B1.α — Fight vs. flight: neuroanatomy and decision logic
The central mechanistic frame the user wants.

1. **The classical stress response.** Cannon (1915) fight-or-flight. Selye (1936) general adaptation syndrome. Sympathetic-adrenal-medullary (SAM) axis — fast, epinephrine/norepinephrine. Hypothalamic-pituitary-adrenal (HPA) axis — slower, cortisol.
2. **What actually differs between fight and flight at the brain level.** Both recruit the sympathetic nervous system, but the behavioral output differs:
   - **Fight (approach/confront):** Rostral-ventral medial hypothalamus and dorsal periaqueductal gray drive attack/approach. Elevated testosterone and dopamine bias toward aggressive risk-taking. BAS (Behavioral Activation System) in Gray & McNaughton's framework. (Panksepp's RAGE system; Blanchard & Blanchard rodent work; Mobbs et al. on human defensive circuits.)
   - **Flight (avoidance/escape):** Dorsal-lateral periaqueductal gray, dorsomedial hypothalamus. Elevated cortisol, freeze-and-flee behavior. BIS (Behavioral Inhibition System). Mobbs et al. 2007 *Science* — distance-from-threat study showing a **PFC → midbrain switch** as threat gets proximal: distal threats use cognitive appraisal, proximal threats hand control to reflexive circuits.
   - **Freeze.** Third option often omitted from lay "fight-or-flight." Polyvagal theory (Porges) — dorsal vagal shutdown. Relevant because some PMs may *freeze* rather than fight or flee — paralysis, no trades.
   - **Tend-and-befriend.** Taylor et al. 2000 — alternative stress response, oxytocin-mediated, may be more common in some individuals under stress. Relevant if we see coordinated / committee-driven behavior increase.
3. **Prefrontal cortex goes offline under acute stress.** Amy Arnsten's work — acute stress triggers catecholamine surge that **impairs PFC function** and shifts control toward amygdala and striatum. Deliberative decision-making (PFC) degrades; habitual or reactive decision-making (striatal, amygdala-driven) takes over. (Arnsten 2009 *Nat Rev Neurosci*; Arnsten 2015.)
4. **Habit vs. goal-directed control.** Schwabe & Wolf 2009, 2013 — stress shifts from goal-directed (flexible, PFC) to habit-based (inflexible, striatal) control. Implication: stressed PMs may default to their *habitual* trade patterns rather than adaptive analysis.
5. **Individual differences in fight vs. flight disposition.** Not everyone does the same thing under stress. BIS/BAS differences (Carver & White), trait anxiety, prior stress inoculation. Relevant because we may see PM-level heterogeneity in how stress affects their trading.
6. **The "hormones on a trading floor" thread.** John Coates and Joe Herbert 2008 — measured cortisol and testosterone in 17 male City traders over 8 days. Morning testosterone predicted higher daily P&L. Cortisol rose with market volatility. Coates' "winner effect" — a winning streak raises testosterone, which raises risk appetite, which can drive bubbles. This is the single closest-to-our-question empirical paper in the literature.
7. **Why this matters for interpreting PM trades under stress.** If PFC is offline and striatum is in control, trades become:
   - More reactive, less analytical.
   - More habit-driven (could mean benchmark-hugging if that's the default, or could mean habitually aggressive bets).
   - More loss-averse (amygdala-weighted) — fleeing toward benchmark.
   - Or in fight mode with testosterone — **increasing active risk** on conviction that may or may not be warranted.

**Bridge to our data:** Moving *further from benchmark* in a crisis is a "fight" signature; moving *closer to benchmark* is a "flight" signature. Which wins empirically in our data tells us which stress response is more error-prone in *this* population of bond PMs under *these* conditions. That's the interesting finding the neuroscience frames.

#### B1.β — Market-level psychology: how individual stress aggregates into market pricing
The second research priority from the user.

1. **Limits of arbitrage.** Shleifer & Vishny 1997 — rational arbitrageurs can't always correct mispricings, especially during stress (they face withdrawals exactly when opportunity is greatest). This is the theoretical foundation for why psychology shows up in prices.
2. **Noise-trader risk.** DeLong, Shleifer, Summers, Waldmann 1990 — mispricings driven by sentiment can persist and widen before they correct. Relevant because a stress-driven PM is, in that moment, a noise trader.
3. **Herding.** Scharfstein & Stein 1990 (reputational herding), Devenow & Welch 1996 (survey). Under stress, career-risk aversion intensifies, herding increases, prices move further from fundamentals.
4. **Sentiment and prices.** Baker & Wurgler 2006, 2007 — sentiment index predicts cross-sectional stock returns, especially for hard-to-value and hard-to-arbitrage securities.
5. **VIX, flows, and behavioral pricing anomalies.** Cross-sectional and time-series anomalies (momentum, reversal) are larger in high-VIX regimes (Stambaugh, Yu, Yuan 2012 on sentiment and anomalies). The market's "stress response" is measurable in prices.
6. **Adaptive Markets Hypothesis.** Andrew Lo 2004, 2017 — markets are populated by heuristic-driven agents; stress regimes change which heuristics are adaptive. Frame that bridges EMH and behavioral finance for an RQS audience.
7. **Trading-floor → market-level.** Coates et al.'s cortisol work + Coates' book *The Hour Between Dog and Wolf* explicitly argues that **aggregated endocrine responses of traders drive bubbles and crashes**. This is the direct micro-to-macro bridge the user is asking for.
8. **Fixed-income specific.** Flight-to-quality dynamics, liquidity premia spikes, dealer balance-sheet capacity in crises. Duffie on "slow-moving capital" (2010 AFA presidential address). Adrian, Etula, Muir on intermediary asset pricing. These give us a *fixed-income-native* story — not just "the behavior of equity traders" — which is important for an RQS/bonds audience.

**Bridge to our data:** If stress distorts individual decisions, it distorts prices. Our experiment measures PMs; aggregated, the same forces that move our sample move the benchmark. This reframes the question of "are PMs making good trades in crises?" as **"does active decision-making add value precisely when the market is most mispriced, or does it fail precisely when it's needed most?"**

#### B1.γ — Methodology / sharpening questions for our own PM analysis
1. **Stress-window definition.** How did we operationalize "periods of elevated volatility"? VIX threshold? Rolling realized vol? Drawdown-based? Why that choice?
2. **Benchmark choice.** Per-PM benchmark or one aggregate? Fixed-income is benchmark-heterogeneous (Agg, global, credit-only, etc.).
3. **"Further from benchmark" metric.** Active weight, active duration, active spread duration, factor-level tilts? One number or a vector?
4. **Trade-level vs. holding-level.** Are we analyzing new trades executed in the stress window, or changes in holdings snapshot-to-snapshot?
5. **Performance horizon for the trade.** Over what window do we measure whether the trade "did well"? Crisis-only, crisis + recovery, 1y forward?
6. **Counterfactual.** "Doing nothing" is also a decision. What's the alternative-hypothesis trade against which each actual trade is measured?
7. **Power / N.** How many PMs, how many stress windows, how many trades? What's the minimum detectable effect?

These questions will be live at Q&A and must have appendix slides.

---

## Cross-cutting / thesis-level research

### T1. Does understanding your own biases reduce their effect?
**User's thesis:** "Better understanding of psychology and of the way our brains tick allows us to overcome the natural human barriers and biases that we have built into us."

This is an empirical claim. It needs defense.

**Research questions:**
1. **Debiasing literature.** Morewedge et al. 2015 ("Debiasing decisions: Improved decision making with a single training intervention") — computer training reduced confirmation bias, fundamental attribution error, bias blind spot. **Cite this explicitly.**
2. **"Bias blind spot."** Pronin, Lin, Ross 2002 — people see bias in others more than themselves. This is the obstacle the thesis has to clear.
3. **Metacognitive training.** Fleming et al. on whether metacognitive accuracy can be trained — mixed evidence, but some ecological gains.
4. **Stoicism / premortem / nudging in professional contexts.** Klein's premortem, Kahneman's "think slow" interventions, behavioral nudges in financial advising.
5. **Institutional debiasing vs. individual debiasing.** Checklists, structured analytic techniques (Heuer, CIA tradecraft), committee decision-making. Often more reliable than personal self-awareness.
6. **Counter-evidence:** The "bias correction is hard" literature — even experts with full bias training show residual biases (Fischhoff). Be ready for this question.

**Framing implication:** We should not overclaim. The honest version is: *"Measurement and awareness don't eliminate bias, but they shift it from invisible to instrumentable. Processes and tools built around known biases demonstrably outperform unaided judgement."* That's a stronger, more defensible thesis for an RQS audience.

---

## Methodology / epistemology questions for our own work
1. **How was "confidence" operationalized in the NLP?** Which markers, which model, validated against what ground truth? (Must be airtight — will be the first question asked.)
2. **Excess return vs. what benchmark?** Per-coverage-area, per-duration-bucket, or market aggregate?
3. **Multiple comparisons.** Three findings across many analysts — what's the family-wise error rate? Which findings survive correction?
4. **Base rates.** Are 2022 horizon shifts really different from other stress periods (1994, 2008, 2013 taper tantrum, 2020 COVID)? We need a reference distribution, not just a single episode.
5. **Selection effects.** Analysts who left Capital Group during 2022 — are they in or out of the sample?

These are placed here because they determine what the appendix needs to contain.
