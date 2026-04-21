# Executive Summary Slides

11-slide spine of the short deck. Framing standard: **Rockefeller-University-grade biomedical talk pitched to a hedge fund.** Each slide: **headline → 2–3 graphs → cross-disciplinary mechanism caption (psychology + neuroanatomy + endocrinology + computational + evolutionary + chronobiology, as applicable) → one clean takeaway.**

The rhetorical weight comes from **multi-discipline convergence** — when neuroanatomy, endocrinology, computational theory, evolutionary biology, AND our own data all predict the same result, the conclusion is not dismissible.

Chart rules: no black ink, straight lines (tension: 0), visible dots at every data point, theme palette only. All quantitative numbers from a reproducible script.

Research depth: see `knowledge/01_*` through `knowledge/11_*` — 11 files, ~52,000 words, ~250 cited primary sources verified via web search.

---

## Slide 1 — Hook
**Headline:** *"In 2022, the written time horizons of our rates analysts collapsed — at exactly the moment the market needed longer thinking."*

**Graphs:**
- G1.1 — Time-series: median analyst time-horizon (NLP-extracted from notes) 2018–2024. Shaded 2022 stress window. Per-analyst lines visible behind the median.
- G1.2 — Bloomberg US Treasury return overlay. Anchor stat: **2022 Treasury return –12.5% (worst since 1973); long zeros –39% (worst since 1754); Fed +425 bp in 9 months** (knowledge/03).

**Takeaway:** Stress measurably changed *how* our analysts wrote — and that change has a biological signature traceable across five disciplines.

---

## Slide 2 — Thesis
**Headline:** *"Behavioral biases have measurable biological signatures. Once we can measure them, we can build instruments around them that improve outcomes."*

No graphs. One sentence.

**Why this framing (not "self-awareness overcomes bias"):** Strongest pro-debiasing evidence (Morewedge et al. 2015) shows ~30% bias reduction immediately, ~20–24% at 2–3 months — but only with purpose-built training, and **high-bias-blind-spot subjects (likely senior PMs) benefit least** (Scopelliti 2015). Process interventions are stronger and more durable. Kahneman's late-career view: *organizations beat individuals* at debiasing. (knowledge/06.)

**Takeaway:** *Measure → instrument → decide.* Self-awareness is helpful but it is not the lever.

---

## Slide 3 — Framework
**Headline:** *"Three experiments. Each finding measured in our own data. Each predicted by five independent disciplines."*

**Graphs:**
- G3.1 — Single tripartite schematic: three rows (experiments A1a / A1b/c / B1) × six columns (psychology, neuroanatomy, endocrinology, computational theory, evolutionary biology, chronobiology) with a colored cell wherever a discipline has direct mechanistic evidence for that finding. Cross-discipline density makes the convergence argument visually.

**Takeaway:** When five independent fields predict the same thing and our data shows it, the conclusion is not single-field coincidence.

---

## Slide 4 — Experiment A1a: Analyst confidence is incomparable across analysts
**Headline:** *"Absolute confidence is not comparable across analysts. Percentile-within-analyst is."*

**Graphs:**
- G4.1 — Per-analyst confidence distributions overlaid (small-multiples or ridge plot). Visibly different means, spreads, and skew.
- G4.2 — Two-panel scatter: forward excess return vs. *absolute* confidence (noisy) | vs. *percentile-of-own-confidence* (clean). The before/after of normalization is the chart.

**Cross-disciplinary mechanism caption:**
- **Genetics** — Cesarini et al. 2009 twin study: **16–34% of overconfidence is heritable.**
- **Neuroanatomy** — Fleming et al. 2010 *Science*: right anterior PFC grey-matter volume predicts metacognitive accuracy (N=32).
- **Linguistics** — Hyland and Biber's corpus work: writer-level hedge/booster style is a stable personal parameter independent of belief.
- **Computational theory** — In the Bayesian-brain frame (Friston), confidence is the *inverse precision of the posterior*. Different priors → different confidence reports for the same evidence (knowledge/07).
- **Behavioral genetics** — DRD4-7R polymorphism explains ~20% of heritable variance in risk-taking (Dreber 2009); COMT Val158Met shifts PFC dopamine clearance and metacognitive style (knowledge/09).

**Takeaway:** Per-analyst normalization isn't statistical convenience — it's the only way to recover the cross-analyst signal from a measurement that varies by genotype, neuroanatomy, prior, and writing style.

---

## Slide 5 — Experiment A1b: Confidence extremes carry the alpha
**Headline:** *"The middle of an analyst's confidence distribution is noise. The tails are signal."*

**Graphs:**
- G5.1 — Forward excess return by decile of per-analyst confidence percentile. U/J shape: elevated at extremes, flat in the middle.
- G5.2 — Per-analyst panels (2–3 selected) showing the tail signature is per-individual, not pooling artifact.

**Cross-disciplinary mechanism caption:**
- **Computational theory** — Sanders, Hangya, Kepecs proved mathematically that **accuracy is U-shaped in reported confidence** under any signal-detection model with extreme posteriors arising from clean accumulation. The tail signal is a theorem of drift-diffusion, not an empirical surprise (knowledge/07).
- **Cellular neuroscience** — Kepecs 2008 *Nature* and Masset 2020 *Cell* identified orbitofrontal "X-pattern" neurons whose discrimination is sharpest at confidence tails; Lak 2014 *Neuron* established the OFC role causally via inactivation (knowledge/02).
- **Expert calibration across domains** — Murphy & Winkler weather forecasters, Keren bridge experts, Mandel & Barnes 2014 *PNAS* intelligence analysts, Tetlock superforecasters: experts' calibration is sharpest at the extremes (knowledge/02).
- **Active management evidence** — Cremers & Petajisto Active Share, Cohen-Polk-Silli Best Ideas: the conviction premium has the same signature in fund returns (knowledge/02).

**Takeaway:** The U-shape is the *predicted phenotype* of a calibrated expert under signal-detection theory, not an artifact. Sizing should weight tail-confidence more than middle-confidence.

---

## Slide 6 — Experiment A1c: 2022 horizon compression as a non-invasive HPA biomarker
**Headline:** *"In 2022, our rates analysts' written time horizons shrank — across multiple analysts. The text is a biomarker of an HPA episode."*

**Graphs:**
- G6.1 — Per-analyst horizon time-series (2018–2024) with median bold. Effect is broad, not driven by one person.
- G6.2 — Side panel: Arnsten inverted-U of catecholamines on PFC performance (knowledge/04) + Kimura 2013 cortisol-vs-delay-discounting curve (knowledge/03). Two canonical literature charts side-by-side, redrawn in deck palette.

**Cross-disciplinary mechanism caption:**
- **Behavioral economics** — Loss aversion λ ≈ 2.25 (Kahneman & Tversky), mechanically amplified at shorter evaluation horizons (Benartzi & Thaler myopic loss aversion).
- **Endocrinology** — HPA axis activation: cortisol peaks 20–40 min post-stressor; binds GR in PFC reshaping utility curvature. Kandasamy 2014 *PNAS* showed 8-day cortisol dosing (69% elevation) drove **utility α from 0.50 → 0.35 (P=0.022) and collapsed certainty-equivalent risk premium 44%** (knowledge/09).
- **Cellular neuroscience** — Catecholamine surge impairs PFC and shifts control from goal-directed to habitual circuits. Schwabe & Wolf demonstrated this *causally*: the shift is **blocked by β-blocker propranolol**, isolating the noradrenergic mechanism (knowledge/04).
- **Network neuroscience** — Hermans 2011 *Science*: acute stress reconfigures the *whole brain*. Salience network up, executive control down — a "salience hijack" that propranolol blocks but cortisol does not (knowledge/08).
- **Computational theory** — Cortisol-driven precision over threat-related priors makes short-horizon worries dominate the posterior (Friston aberrant-precision frame; knowledge/07).
- **Sleep** — Yoo 2007 *Nat Neurosci*: sleep loss amplifies amygdala reactivity by ~60% and decouples it from PFC. 2022's drawdown stress likely ate sleep, amplifying everything else (knowledge/11).

**Takeaway:** The 2022 horizon collapse is the text-output signature of a well-characterized neuroendocrine pathway. The analyst note is a non-invasive biomarker of an HPA episode — usable as a signal in real time.

---

## Slide 7 — Experiment B1: PM trades in volatility windows — fight, flight, or freeze
**Headline:** *"[Direction TBD] In stress, PMs' active-risk trades [outperform / underperform] their benchmark-hugging trades — and the brain explains why."*

**Graphs:**
- G7.1 — Stress-regime decomposition: performance of further-from-benchmark trades vs. closer-to-benchmark trades, calm vs. stress windows side-by-side.
- G7.2 — Coates & Herbert 2008 cortisol-vs-volatility chart from London trading-floor study (canonical reference, redrawn).

**Cross-disciplinary mechanism caption:**
- **Behavioral neuroscience** — Active-risk-up = **fight** signature; active-risk-down = **flight**; no-trade = **freeze**. Each maps to a specific neural circuit. Bandler & Shipley four-column PAG anatomy: dorsomedial PAG = fight, dorsolateral = flight/active-freeze, ventrolateral = passive shutdown (knowledge/04).
- **Cognitive neuroscience** — Mobbs 2007 *Science*: fMRI-measurable handoff from ventromedial PFC to PAG as threat proximity increases. The brain *flips* from cognitive appraisal to reflexive control at a threshold (knowledge/04).
- **Endocrinology** — Coates & Herbert 2008 *PNAS* (N=17 City traders): morning testosterone predicted daily P&L; cortisol tracked market volatility. Kandasamy 2014 (above): cortisol *causally* collapses risk premium (knowledge/04, 09).
- **Biological individual differences** — Coates 2009 *PNAS* (N=44): 2D:4D digit ratio (a marker of prenatal androgen exposure) explains R² = 0.553 of variance in trader profitability — **11× P&L spread between top and bottom 2D:4D tertiles** (knowledge/09).
- **Evolutionary** — Johnson & Fowler 2011 *Nature*: overconfidence is the evolutionarily stable strategy when contests have asymmetric payoffs (2r > c_fight). Fight is the *adaptive default* — but for ancestral contests, not modern markets (knowledge/10).
- **Computational theory** — Stress shifts model-based RL → model-free RL (Otto et al. 2013 *PNAS*). Fight under model-free control means *habit takes over*, not adaptive analysis (knowledge/07).

**Takeaway:** Whichever direction wins in our data tells us which response dominates *this* population in *this* regime. The mechanism is biological, not motivational — which means the lever is biological too.

---

## Slide 8 — Brain-state reconfiguration & biomarkers (Hermans + wearables)
**Headline:** *"Acute stress reconfigures the *whole brain*, not just one region. And we can measure the reconfiguration in real time."*

**Graphs:**
- G8.1 — Hermans 2011 *Science* schematic: salience network up, executive control network down under acute stress. Redrawn for the deck.
- G8.2 — HRV-vs-cognitive-flexibility curve (Thayer & Lane lineage): high HRV correlates with better top-down control, low HRV with reactive / inflexible decision-making. Source for individual decision-state biomarker.

**Cross-disciplinary mechanism caption:**
- **Network neuroscience** — Hermans 2011 *Science*: noradrenergic-driven salience hijack, propranolol blocks it, cortisol doesn't. Time course: fast NE phase 0–30 min (relevant to a flash drawdown), slow cortisol cleanup 60+ min (relevant to multi-day stress) (knowledge/08).
- **Psychophysiology** — HRV indexes prefrontal-vagal control (Thayer & Lane 2000). Pupillometry indexes locus-coeruleus norepinephrine drive (Joshi 2016 *Neuron*). Both are field-deployable today via consumer wearables and webcam pupil-tracking (knowledge/08).
- **Sleep** — Yoo 2007: sleep deprivation produces a network signature that mimics acute stress. Combined sleep + market stress is the worst case (knowledge/11).
- **Translation gap (research opportunity flagged)** — no published continuous HRV + pupil + market-telemetry panel in professional PMs. RQS could close this gap.

**Takeaway:** State-of-brain is measurable in real time with off-the-shelf hardware. The instrument layer for this thesis is closer than people think.

---

## Slide 9 — Market-level read: psychology aggregates into mispricing
**Headline:** *"Individual stress psychology aggregates into market mispricing. Active management's edge is path-dependent on it."*

**Graphs:**
- G9.1 — Conceptual: 4-link micro-to-macro chain. Individual bias → trader behavior → correlated flow → persistent price deviation.
- G9.2 — Either Stambaugh-Yu-Yuan 2012 sentiment-conditioned anomaly returns OR Haddad-Moreira-Muir 2021 ETF dislocation event-study chart from the 2020 stress.

**Cross-disciplinary mechanism caption:**
- **Behavioral finance** — Limits-of-arbitrage (Shleifer & Vishny 1997), noise-trader risk (DeLong et al. 1990) → stress-driven mispricings persist before they correct (knowledge/05).
- **Information cascades / herding** — Banerjee 1992, Bikhchandani-Hirshleifer-Welch 1992: rational agents imitate when self-information is weak — explains bubbles and panics with rational micro-agents (knowledge/10).
- **Fixed-income specifics** — Intermediary asset pricing (Adrian-Etula-Muir 2014, He-Krishnamurthy 2013), funding-liquidity spirals (Brunnermeier-Pedersen 2009), slow-moving capital (Duffie 2010), credit-cycle over-extrapolation (Greenwood-Hanson 2013) (knowledge/05).
- **Coates aggregation argument** — Endocrine responses on a trading floor are correlated; aggregated they produce bubbles and crashes. The micro-to-macro mechanism (knowledge/04).
- **Adaptive Markets Hypothesis** — Lo 2004: markets are populated by heuristic-driven agents; stress regimes change which heuristics are adaptive. The meta-frame for an RQS audience (knowledge/05).

**Takeaway:** If our decisions degrade in stress and the market's do too, the only relevant question is whether our edge holds up on the *relative* scorecard. Slide 7 answers it for our PMs.

---

## Slide 10 — What to do: instruments grounded in the science
**Headline:** *"Measurement first. Then instruments that don't depend on being less biased."*

**Graphs:**
- G10.1 — Dashboard mockup: per-analyst confidence-percentile strip with current-percentile, historical distribution, and tail-band shading.
- G10.2 — Stress-window decision-protocol flowchart: trigger (vol/drawdown threshold) → cooling-off → premortem → checklist → decision log.

**Four concrete recommendations grounded in the cross-disciplinary evidence:**
1. **Per-analyst confidence normalization** in PM tools (from A1a — biological signal recovery; per-analyst is the only valid scale).
2. **Tail-weighted sizing bands** for analyst conviction (from A1b — DDM proves the tails carry the signal).
3. **Stress-window decision protocol** — cooling-off, structured premortem, checklist (Klein, Kahneman *Noise*, Haynes 2009 surgical checklist –47% mortality). Rationale: under acute stress the PFC is *the* circuit you'd need for self-awareness, and it's offline (Arnsten). Process beats self-awareness for this audience and these conditions (knowledge/04, 06).
4. **Sleep & scheduling policy around high-stakes decisions** — chronobiology evidence is the cheapest, highest-leverage lever in this entire deck (Yoo 2007 amygdala-PFC uncoupling; Kamstra-Kramer-Levi DST market anomaly with caveats) (knowledge/11).

**Takeaway:** Each recommendation is independently grounded in a peer-reviewed mechanism *and* the empirical pattern in our own data. None depends on people being less biased — they depend on instruments that absorb known biases.

---

## Slide 11 — Close
**Headline:** *"Three biases. Five disciplines converge. Four instruments. Measure → instrument → decide."*

No graph. Re-state thesis with the evidence behind it now.

---

## Production checklist
- [ ] Empirical chart scripts (G1.1, G1.2, G4.1, G4.2, G5.1, G5.2, G6.1, G7.1) — need user data + scripted analysis pipeline.
- [ ] Schematics (G3.1, G9.1, G10.1, G10.2) — designable now without external dependencies.
- [ ] Canonical literature redraws (G6.2 Arnsten/Kimura, G7.2 Coates, G8.1 Hermans, G8.2 HRV, G9.2 anomaly returns) — each requires source-figure access; cite page/figure number for provenance.
- [ ] Format decision: HTML deck, PowerPoint, or PDF. Default recommendation: **HTML deck** (richness, web-shareability, allows interactive small-multiples for per-analyst panels).
- [ ] Capital Group / RQS palette confirmation.
- [ ] Deadline confirmation.

## Slide count
**Main deck: 11 slides. Appendix: ~30–40.** Appendix taxonomy in `OUTLINE.md`. Knowledge base in `knowledge/01_*` through `knowledge/11_*`.