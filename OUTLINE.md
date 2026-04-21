# Outline

## Framing standard
**"Rockefeller University-grade biomedical talk pitched to a hedge fund."** Top-tier mechanism science, cross-disciplinary synthesis, immediately implementable takeaways. Each section is a chain: empirical finding → psychology → brain chemistry → mathematical/computational frame → evolutionary origin → actionable instrument.

## Thesis (working — will tighten further)
> **"Behavioral biases in our investment decisions have measurable biological signatures across multiple disciplines — cellular neuroscience, endocrinology, computational theory, and evolutionary biology all converge on the same predictions. Once we can measure them, we can build instruments around them that improve portfolio outcomes."**

The cross-disciplinary convergence is the rhetorical move. When five independent fields predict the same thing and our data shows it, the audience cannot dismiss it as a single-field coincidence.

---

## Main deck (target: 10–12 slides)

Each slide: **headline → 2-3 graphs → mechanism caption with cross-disciplinary anchors → takeaway**.

1. **Hook** — 2022 horizon collapse chart over Treasury drawdown. (G1.1, G1.2)
2. **Thesis** — one sentence, no graph.
3. **Framework** — three experiments, each backed by *multiple* mechanism layers (psychology, brain chemistry, computational, evolutionary). Single tripartite schematic. (G3.1)
4. **Experiment A1a — heterogeneous analyst confidence.** Per-analyst normalization is the only valid signal. Four mechanistic substrates (genetic, neuroanatomical, linguistic, computational). (G4.1, G4.2)
5. **Experiment A1b — confidence extremes carry signal.** Predicted by drift-diffusion + OFC X-pattern + expert calibration literature across domains. (G5.1, G5.2)
6. **Experiment A1c — horizon compression in 2022.** HPA cortisol → delay discounting → PFC offline. Causal evidence: Schwabe & Wolf propranolol experiment. Analyst notes as non-invasive HPA biomarker. (G6.1, G6.2)
7. **Experiment B1 — PM trades in volatility.** Fight/flight/freeze decomposition. Coates & Herbert 2008 trading-floor biology + Kandasamy 2014 causal cortisol experiment (44% risk-premium collapse). (G7.1, G7.2)
8. **Brain-state reconfiguration** — Hermans 2011 *Science* salience hijack. Acute stress reconfigures *whole-brain* network state, not just one region. Bridges to wearables / HRV / pupillometry as field-deployable biomarkers. (Network-neuroscience research.)
9. **Market-level read** — individual stress aggregates into market mispricing. Limits-of-arbitrage, intermediary asset pricing. Adaptive Markets Hypothesis as the meta-frame. (G8.1, G8.2)
10. **What to do.** Three concrete instruments grounded in the science:
    - Per-analyst confidence normalization in PM tools.
    - Tail-weighted sizing bands.
    - Stress-window decision protocol (cooling-off, premortem, checklist) — backed by debiasing literature showing process beats self-awareness.
    - Plus optional: sleep / scheduling policy around high-stakes decisions (cheap, high-leverage from chronobiology evidence). (G9.1, G9.2)
11. **Why this isn't quackery — cross-disciplinary convergence.** *Optional slide.* The same prediction emerges from neuroanatomy (Mobbs PAG switch), endocrinology (Kandasamy cortisol), computation (DDM tails), evolutionary biology (Johnson-Fowler adaptive overconfidence), and our own data. When five independent disciplines agree, that's the strongest form of evidence.
12. **Close** — restate thesis with the evidence behind it.

Detailed slide-level captions in `EXECUTIVE_SUMMARY.md`. Graphs catalog in `GRAPHS.md`.

---

## Appendix (large, structured by anticipated question)

### A. Methodology deep-dives
- **A-method.1** NLP confidence operationalization — model, prompt, hedge/booster lexicon, validation. Loughran-McDonald and Kim 2024 LLM-confidence prior art. **First Q&A pressure point.**
- **A-method.2** Excess-return benchmark choice and justification.
- **A-method.3** Per-analyst normalization — statistical form, windowing, cold-start.
- **A-method.4** Horizon extraction from text — features, validation.
- **A-method.5** Multiple-comparisons handling and family-wise error rate.
- **A-method.6** PM stress-window definition (VIX vs. realized-vol vs. drawdown-based).
- **A-method.7** PM benchmark choice and "further/closer" trade decomposition.
- **A-method.8** Counterfactual construction — what a "doing nothing" trade would have done.

### B. Mechanism / science depth
- **B-science.1** Metacognitive confidence — aPFC anatomy, individual differences, Fleming 2010 *Science*. (`knowledge/01`)
- **B-science.2** Decision confidence at the extremes — Kepecs/Masset OFC X-pattern, Pouget-Drugowitsch confidence vs certainty. (`knowledge/02`)
- **B-science.3** Cortisol, delay discounting, decision under loss — Kimura 2013, Lempert. (`knowledge/03`)
- **B-science.4** Loss aversion, myopic loss aversion, drawdown behavior — Benartzi-Thaler, Frazzini. (`knowledge/03`)
- **B-science.5** Fight/flight/freeze neuroanatomy — PAG columns, Mobbs proximal-threat switch, Arnsten PFC offline. (`knowledge/04`)
- **B-science.6** PFC offline under acute stress — Arnsten 2009, Schwabe-Wolf goal-to-habit shift causally tested with propranolol. (`knowledge/04`)
- **B-science.7** Trading-floor endocrinology — Coates & Herbert 2008, Kandasamy 2014 causal cortisol experiment. (`knowledge/04`)
- **B-science.8** Market-level behavioral pricing — limits of arbitrage, noise traders, herding, sentiment. (`knowledge/05`)
- **B-science.9** Adaptive Markets Hypothesis as bridging frame. (`knowledge/05`)
- **B-science.10** Fixed-income behavioral specifics — intermediary asset pricing (Adrian-Etula-Muir, He-Krishnamurthy), funding-liquidity (Brunnermeier-Pedersen), slow-moving capital (Duffie). (`knowledge/05`)
- **B-science.11** Debiasing literature — Morewedge 2015 effect sizes, Sellier 2019 transfer evidence, Scopelliti 2015 blind-spot moderation. (`knowledge/06`)
- **B-science.12** Process beats self-awareness — premortem, checklists, *Noise* decision hygiene. (`knowledge/06`)
- **B-science.13** Computational neuroscience — Bayesian brain, drift diffusion, model-based vs model-free RL, Friston free energy. (`knowledge/07` — pending)
- **B-science.14** Network neuroscience — Hermans 2011 salience hijack, DMN/SN/CEN tripartite, HRV/pupillometry biomarkers. (`knowledge/08` — pending)
- **B-science.15** Molecular endocrinology — MR/GR receptor biology, 2D:4D, Kandasamy causal cortisol, candidate-gene caveats. (`knowledge/09` — pending)
- **B-science.16** Evolutionary origins — Johnson-Fowler adaptive overconfidence, Hirshleifer evolutionary finance, Sapolsky mismatch. (`knowledge/10` — pending)
- **B-science.17** Chronobiology and sleep — Yoo 2007 amygdala-PFC sleep uncoupling, DST market anomaly, time-of-day effects. (`knowledge/11` — pending)

### C. Robustness
- **C-robust.1** 2022 horizon effect across other stress regimes (1994, 2008, 2013 taper, 2020).
- **C-robust.2** U-shape after per-analyst normalization vs. pooled (rules out distribution-mixing artifact).
- **C-robust.3** Survivorship and selection effects.
- **C-robust.4** AI model / prompt sensitivity.
- **C-robust.5** PM "further/closer" finding under alternative stress definitions.
- **C-robust.6** PM finding per-individual vs. driven by outliers.
- **C-robust.7** Sentiment-vs-confidence — does our confidence signal just track sentiment?

### D. Alternatives considered
- **D-alt.1** Sentiment (not confidence) — what we'd find and why we chose confidence.
- **D-alt.2** Trade-based confidence proxy (position sizing) instead of text-based.
- **D-alt.3** Survey-based confidence — why written notes are better-calibrated.
- **D-alt.4** Rational explanations for the same patterns (liquidity premia, inventory cycles).

### E. Anticipated Q&A slides
- **E-qa.1** "Are you measuring confidence or just verbal style?" → Hyland/Biber on stable per-writer style; per-analyst normalization handles this.
- **E-qa.2** "Could this just be luck / small-N?" → multiple-comparisons treatment + per-individual robustness.
- **E-qa.3** "How do we operationalize this for a PM tomorrow?" → dashboard mockup + protocol.
- **E-qa.4** "What's the incremental lift over our existing tools?" → measurement instruments are additive, not replacement.
- **E-qa.5** "Isn't the solution just to train analysts to be more self-aware?" → Morewedge effect sizes + Scopelliti blind-spot moderation; process beats self-awareness.
- **E-qa.6** "Why should I trust pop-neuroscience in my investment process?" → cross-disciplinary convergence — the same prediction from five independent fields plus our own data.
- **E-qa.7** "Can we screen analysts/PMs for these biological markers?" → ethical/legal/scientific limits; what IS actionable (self-knowledge, protocols).
- **E-qa.8** "Is 2022 special enough to base a recommendation on?" → robustness across other stress windows (or transparent acknowledgment if 2022 is uniquely informative).

---

## Open
- Slide count target — proposing **10–12** for main deck. Confirm.
- Format — PowerPoint, HTML deck, or PDF.
- Deadline.
- Direction of PM B1 result (further-from-benchmark wins or loses in stress).
- User data access for empirical chart production.