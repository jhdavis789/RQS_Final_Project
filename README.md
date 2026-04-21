# RQS Final Presentation

Final presentation for a project conducted within **Capital Group's Risk and Quantitative Services (RQS)** department, focused on **behavioral biases in active fixed income portfolios**.

## Topic
Three experiments on Capital Group analysts and one on PMs:
- **A1a** — heterogeneous baseline confidence in analyst notes; per-analyst-percentile is the only valid cross-analyst signal.
- **A1b** — confidence-extremes carry the alpha signal; the middle is noise.
- **A1c** — 2022 drawdown compressed analyst time horizons across multiple analysts.
- **B1** — PM trade behavior in volatility windows (further-from-benchmark vs. closer-to-benchmark, calm vs. stress).

## Framing standard
**"Rockefeller University-grade biomedical talk pitched to a hedge fund."** Top-tier mechanism science (cellular neuroscience, endocrinology, computational theory, network neuroscience, evolutionary biology, chronobiology), cross-disciplinary synthesis, and immediately implementable takeaways. The cross-disciplinary convergence — the same prediction emerging from five independent fields *and* our own data — is the rhetorical move that defends the conclusions against any single-field skepticism.

## Format
- **Short main deck (10–12 slides)** — each slide: headline → 2–3 graphs → mechanism caption with cross-disciplinary anchors → takeaway.
- **Large appendix (~30–40 slides)** — methodology, science depth (one slide per discipline), robustness, alternatives, anticipated Q&A.

## Audience
RQS staff at Capital Group — quantitatively literate, will pressure-test claims and demand methodology rigor. Frame everything so it holds up under cross-examination from a quant who can also read neuroscience.

## Files in this directory
- `README.md` — this file. Project brief and framing standard.
- `APPROACH.md` — research / synthesis / deck-build workflow.
- `NOTES.md` — append-only log of every tidbit and decision.
- `RESEARCH_QUESTIONS.md` — research question scaffolding for both analyst and PM sides.
- `OUTLINE.md` — main-deck flow + appendix taxonomy with file pointers into `knowledge/`.
- `EXECUTIVE_SUMMARY.md` — slide-by-slide spine with headlines, graph specs, and mechanism captions.
- `GRAPHS.md` — every chart proposed, classified E (empirical) / C (canonical literature redraw) / S (schematic).
- `QUESTIONS.md` — open questions for user + anticipated audience questions for appendix.
- `knowledge/` — deep research files, one per discipline. ~150 cited primary sources across:
  - `01_metacognition_confidence.md` — aPFC, Fleming, Moore-Healy, NLP confidence prior art.
  - `02_confidence_extremes.md` — Dunning-Kruger critiques, expert calibration, Kepecs OFC X-pattern, Active Share.
  - `03_stress_horizon.md` — myopic loss aversion, HPA axis, cortisol → delay discounting, 2022 context.
  - `04_fight_flight.md` — PAG columns, Mobbs proximal-threat switch, Arnsten PFC offline, Coates trading floor, Kandasamy causal cortisol.
  - `05_market_psychology.md` — limits of arbitrage, sentiment, herding, Adaptive Markets, fixed-income intermediary asset pricing.
  - `06_debiasing.md` — Morewedge effect sizes, bias blind spot, *Noise* decision hygiene, process-beats-self-awareness.
  - `07_computational_neuroscience.md` — Bayesian brain, DDM U-shape proof (Sanders-Hangya-Kepecs), free energy, model-based vs model-free RL.
  - `08_network_neuroscience.md` — Hermans 2011 *Science* salience hijack, biphasic time course (NE 0-30min, cortisol 60+min), HRV/pupillometry biomarkers.
  - `09_endocrinology_individual_differences.md` — MR/GR receptor biology, Coates 2009 2D:4D R²=0.553, Kandasamy 2014 cortisol experiment, candidate-gene caveats.
  - `10_evolutionary_origins.md` — Johnson-Fowler adaptive overconfidence ESS, information cascades, Hirshleifer evolutionary finance, Gigerenzer-vs-Kahneman engaged head-on.
  - `11_chronobiology_sleep.md` — Yoo 2007 60% amygdala amplification + mPFC decoupling, DST/SAD anomalies with multiple-comparison caveats, in-data sleep test proposal.
- `TAKEAWAYS.md` — 33 quotable, defensible punchlines + Q&A landmine responses, all backed by knowledge files.

## Status
**Knowledge base complete.** 11 deep files, ~52,000 words, ~250 cited primary sources verified via web search across psychology, cellular neuroscience, endocrinology, computational neuroscience, network neuroscience, evolutionary biology, chronobiology, behavioral finance, and debiasing literature. Outline, executive summary (11 slides), graphs catalog (38 charts), and takeaways file all drafted.

Awaiting from user:
- PM B1 result direction (further-from-benchmark wins or loses in stress).
- Slide format (HTML deck, PowerPoint, PDF) — **default recommendation: HTML deck**.
- Deadline.
- Access to data for empirical chart production.
- Any Capital Group / RQS brand palette to honor.
