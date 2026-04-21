# Computational Neuroscience of Decision and Confidence — Deep Research

## Executive one-liner

Every quantity we extract from analyst notes and PM trade blotters — confidence, horizon, turnover under stress — has a formal counterpart in a single family of computational models: the **Bayesian brain under bounded resources**. Confidence is the inverse variance (precision) of an internal posterior. Time-horizon is the temporal depth of the generative model the agent is sampling from. The fight/flight decomposition in PM trade behavior is the computational signature of an **arbitration mechanism between a model-based (slow, PFC-dependent, expensive) and model-free (fast, striatal, cheap) controller**, gated by estimated reliability. Under acute stress the arbiter shifts weight toward the cheap controller, horizons compress, and prior precision over learned habits rises. This document provides the equations and primary citations that turn our empirical findings into propositions the quant audience can stress-test.

---

## 1. The Bayesian-brain frame

### 1.1 Helmholtz and the unconscious-inference tradition

The contemporary Bayesian brain inherits directly from Hermann von Helmholtz's nineteenth-century "unconscious inference" — the idea that perception is not a passive registration of sensory data but the brain's best guess at a generative cause. The modern computational realization is the **Helmholtz machine** of Dayan, Hinton, Neal & Zemel (1995, *Neural Computation* 7:889–904). A Helmholtz machine pairs a **recognition (bottom-up) network** that maps observations to posteriors over latent causes with a **generative (top-down) network** that maps causes to predicted observations. The two are trained jointly by the **wake–sleep algorithm** (Hinton, Dayan, Frey & Neal 1995, *Science* 268:1158–1161): wake-phase updates the generative weights so top-down predictions better reconstruct sensations inferred by the recognition net; sleep-phase runs the generative net to produce fantasied data and updates the recognition weights to invert them.

The key point for our purposes: **recognition is amortized variational inference.** A trained human analyst hitting a 10-K is not recomputing a posterior from scratch — they are running a well-trained recognition network that maps surface features to a point estimate plus a variance. Two analysts with identical raw evidence but different recognition networks will produce different posteriors. This is the computational root of why per-analyst normalization is non-negotiable: we are sampling from different amortized encoders.

### 1.2 Free energy as a unifying objective

Karl Friston's 2010 *Nature Reviews Neuroscience* paper ("The free-energy principle: a unified brain theory?" *Nat. Rev. Neurosci.* 11:127–138) is the single most-cited attempt to give the brain a single scalar objective function. The mathematical scaffold is variational Bayes:

A generative model `p(o, s | m)` over observations `o` and hidden states `s` under model `m` has an exact log-evidence `log p(o | m)` that is intractable. **Variational free energy** F provides a tractable upper bound on surprise `-log p(o | m)`:

```
F(o, q) = E_q[log q(s) − log p(o, s)]
        = D_KL[q(s) ∥ p(s | o)]  −  log p(o)
        = D_KL[q(s) ∥ p(s)]      −  E_q[log p(o | s)]
           \_____ complexity ____/   \___ accuracy ___/
```

where `q(s)` is the brain's approximate posterior (its "recognition density"). The first decomposition makes the KL-to-true-posterior explicit; minimizing F drives `q → p(s | o)`. The second decomposition (complexity − accuracy) is the one most physically intuitive: perception picks the simplest explanation that still fits the data.

In the Gaussian case with precisions `π = 1/σ²`, F reduces to a **precision-weighted sum of squared prediction errors** — which is exactly what predictive-coding cortex is hypothesized to compute (below). **Confidence, in this framework, is nothing more than the posterior precision `π_post` on the decision-relevant variable.** This is not analogy — it is the same object.

Action adds one step. Under **active inference**, the agent also chooses policies `π` that minimize the **expected free energy** G of future outcomes. G decomposes into:

```
G(π) = − E_q[log p(o | π)]        +  E_q[D_KL[q(s | o, π) ∥ q(s | π)]]
         \____ pragmatic value ____/   \______ epistemic value ______/
```

The pragmatic term is expected utility; the epistemic term rewards information gain. This is the principled resolution of the exploration-exploitation trade-off (Friston et al. 2015, *Cognitive Neuroscience*, "Active inference and epistemic value"; Parr & Friston 2019, *Biol. Cybern.*, "Generalised free energy and active inference").

### 1.3 Predictive coding and the canonical microcircuit

The free-energy story acquires neural teeth through **predictive coding**. Rao & Ballard (1999, *Nat. Neurosci.* 2:79–87) proposed that cortical hierarchies implement a scheme in which **feedback connections carry predictions** from higher areas to lower and **feedforward connections carry only the residual prediction errors**. Their simulations showed that a hierarchical network of this form, trained on natural images, spontaneously developed simple-cell-like receptive fields in its lower layers and reproduced "extra-classical" surround effects as a direct consequence of the prediction-cancellation architecture.

Bastos, Usrey, Adams, Mangun, Fries & Friston (2012, *Neuron* 76:695–711, "Canonical Microcircuits for Predictive Coding") mapped this theory onto the laminar anatomy of cortex. Key claims the quant audience should take on faith for now but which are testable:

- Superficial pyramidal cells (L2/3) encode **prediction errors** and project feedforward.
- Deep pyramidal cells (L5/6) encode **predictions/expectations** and project feedback.
- Gamma oscillations (30–80 Hz) carry forward prediction errors; alpha/beta (8–30 Hz) carry top-down predictions.
- **Precision weighting is implemented by the gain on superficial pyramidal cells**, modulated by neuromodulators (dopamine, acetylcholine, noradrenaline).

The last point is the bridge to brain chemistry. When we talk about noradrenaline or dopamine shifting confidence calibration, what is shifting at the circuit level is the precision weight on error signals — which is a one-line change to the variational free-energy objective.

### 1.4 Confidence as inferred precision

Yon & Frith (2021, *Current Biology* 31:R1026–R1032, "Precision and the Bayesian brain") make the connection to subjective confidence explicit: agents represent and report the **precision of their posteriors**. Pouget, Drugowitsch & Kepecs (2016, *Nat. Neurosci.* 19:366–374, "Confidence and certainty: distinct probabilistic quantities for different goals") push the distinction one layer further. They separate:

- **Certainty** — the full posterior probability `p(s | evidence)` as encoded in neural population activity, the object of Bayesian inference.
- **Confidence** — the *scalar summary* the agent reports, typically `p(correct | evidence, choice)`.

Every analyst-note confidence extraction is a read-out of this scalar, filtered by each analyst's idiosyncratic verbal encoder. Fleming & Daw (2017, *Psychol. Rev.* 124:91–114, "Self-evaluation of decision-making: A general Bayesian framework for metacognitive computation") formalize reported confidence as a **second-order inference**: the brain infers its own decision-system performance from a (correlated but not identical) confidence sample and its own actions. This is the formal reason confidence can dissociate from accuracy and why meta-d' exists as a construct.

**Takeaway for the presentation.** When we extract an analyst's confidence percentile from a note, we are estimating the value of a single internal parameter — the precision of a second-order posterior over the first-order investment posterior — filtered through a writer-specific verbal readout function. Per-analyst normalization inverts the readout function; percentile-on-own-history is the minimum-assumption estimator.

---

## 2. Drift diffusion and the math of confidence at the tails

### 2.1 The drift-diffusion model

The drift-diffusion model (DDM; Ratcliff 1978; Ratcliff & McKoon 2008, *Neural Computation* 20:873–922, "The diffusion decision model: Theory and data for two-choice decision tasks") is the dominant sequential-sampling account of two-alternative choice. The decision variable `x(t)` follows a Wiener process with drift `v` and diffusion `σ`:

```
dx = v dt + σ dW_t,      x(0) = z
```

where `z` is the starting point (bias) and boundaries at `±a/2` are absorbing. A correct-boundary hit at time `T` is a response; the choice is determined by which boundary, and reaction time is `T + t_0` (non-decision time). Under pure DDM the probability of choice and the full RT distribution have closed-form expressions, and model parameters (`v, a, z, t_0`) can be estimated from behavior and mapped onto neural correlates.

Drift rate `v` is **signal-to-noise in evidence**; boundary `a` is a **speed–accuracy policy**; starting point `z` is **prior bias**; non-decision time `t_0` is encoding + motor. The DDM is provably optimal for two-alternative decisions in the sense of Wald's sequential probability ratio test when the drift is constant and known.

### 2.2 Confidence as a function of state and time

A naive reading of DDM predicts confidence should track the absolute value of the decision variable at termination `|x(T)|`. Kiani, Corthell & Shadlen (2014, *Neuron* 84:1329–1342, "Choice certainty is informed by both evidence and decision time") showed this is incomplete: **certainty is a function of both `x(T)` and `T` itself** — for bounded-accumulation models, the same terminating evidence carries different posterior probabilities of correctness depending on how long it took to reach. Fast-and-decisive versus slow-and-barely-over-threshold produce the same choice but different confidences. Their monkey neurophysiology (post-decision wagering in LIP) shows the brain actually uses time as an input to confidence.

Pleskac & Busemeyer (2010, *Psychol. Rev.* 117:864–901, "Two-stage dynamic signal detection: A theory of choice, decision time, and confidence") formalize this as **2DSD**: a DDM-like first stage produces the choice, then evidence continues to accumulate for an interjudgment interval before being snapshotted into a confidence rating. This predicts that post-decisional evidence can both increase confidence (if it continues to support the choice) and produce **changes of mind**. The formal prediction: confidence distributions are wider, less correlated with accuracy, and more asymmetric than would be predicted by terminal-state-only read-outs — all of which are observed.

### 2.3 The U-shape: why extreme confidences are more accurate

Sanders, Hangya & Kepecs (2016, *Neuron* 90:499–506, "Signatures of a statistical computation in the human sense of confidence") provide the canonical proof. Define **statistical confidence** as `p(correct | evidence, choice)` under signal-detection theory. They derive mathematically — and verify in humans on perceptual and knowledge tasks — three signatures:

1. Average confidence on **correct** trials **increases** with stimulus strength.
2. Average confidence on **incorrect** trials **decreases** with stimulus strength (the "folded X").
3. At zero stimulus, confidence equals a non-trivial floor (0.75 in their 2AFC setup).

The implication is that **accuracy is a U-shaped function of reported confidence**: extreme confidences, high or low, correspond to trials with strong evidence, which are the trials where signal-detection is most accurate. Middling confidences are the trials the evidence itself was ambiguous, and accuracy falls toward chance. This is not a quirk of human reporting — it is a mathematical property of optimal Bayesian confidence, which is why we see the same pattern in rats (Kepecs et al. 2008, *Nature*) and in ideal-observer simulations (Kepecs & Mainen 2012, *Philos. Trans. R. Soc. B* 367:1322–1337).

**The RQS implication.** Our analyst-confidence signal predicting excess returns most strongly at the tails is not noise — it is the empirical signature that our analysts are approximately Bayesian confidence-reporters. The tails carry more signal because they correspond to the cleanest posteriors. Any analysis that regresses excess returns linearly on confidence throws away most of the mechanism.

---

## 3. Model-based vs model-free reinforcement learning

### 3.1 Two controllers, one agent

Daw, Niv & Dayan (2005, *Nat. Neurosci.* 8:1704–1711, "Uncertainty-based competition between prefrontal and dorsolateral striatal systems for behavioral control") formalized what was already clinical folklore: the brain has (at least) two action-selection systems.

- A **model-based (MB)** system constructs and simulates an internal world-model `p(s' | s, a)` and reward model `r(s, a)`. It computes values by tree-search or dynamic programming: flexible, sample-efficient, but computationally expensive. Anatomically: dorsomedial PFC, dorsomedial striatum, hippocampus.
- A **model-free (MF)** system caches action values directly from experience via temporal-difference learning: `Q(s, a) ← Q(s, a) + α·δ`, where `δ = r + γ·max Q(s', a') − Q(s, a)`. Inflexible in the face of change but cheap and fast. Anatomically: dorsolateral striatum, midbrain dopamine.

Daw et al. 2005's proposed arbitration rule: **use the controller with lower posterior uncertainty over its own value estimates.** Early in learning MB is better (it generalizes); with abundant repetition MF becomes lower-variance and takes over. This is a Bayesian optimality argument, not an ad hoc priority scheme.

### 3.2 The two-step task

Daw, Gershman, Seymour, Dayan & Dolan (2011, *Neuron* 69:1204–1215, "Model-based influences on humans' choices and striatal prediction errors") introduced the two-step task that has since become the workhorse for dissociating the two systems behaviorally. A first-stage choice probabilistically leads to one of two second-stage states (70%/30% common/rare transitions); each second-stage state has its own reward. A pure MF agent's first-stage stay probability is a function of *reward only* (irrespective of rare vs common transition). A pure MB agent's stay probability shows a **reward × transition interaction**: after a rare-transition reward they *switch*, because the transition information implies the *other* first-stage action would have led to the rewarding state more reliably.

Behavioral fits typically yield a weight `w` between 0 (pure MF) and 1 (pure MB), roughly `Q_net = w·Q_MB + (1−w)·Q_MF`. Striatal BOLD prediction-error signal carries both MB and MF components in proportion to the behavioral `w` — a critical finding because it shows the dopaminergic PE is not purely model-free, contra the earlier simple dogma.

### 3.3 Stress shifts the arbiter

Otto, Raio, Chiang, Phelps & Daw (2013, *PNAS* 110:20941–20946, "Working-memory capacity protects model-based learning from stress") is the causal experiment. Acute cold-pressor stress, followed by two-step task, with working-memory capacity measured independently. Result: stress **selectively reduces the MB weight `w`** — MF contribution is untouched. Further, the reduction is **moderated by working-memory capacity**: high-WMC subjects are protected, low-WMC subjects collapse toward MF control.

This is consistent with the broader Schwabe & Wolf program (Schwabe & Wolf 2013, *Trends Cogn. Sci.* 17:60–68, "Stress and multiple memory systems: from 'thinking' to 'doing'"; see also *J. Neurosci.* 29:7191 for the original "Stress prompts habit behavior in humans"). Mechanistically the stress-induced shift requires **concerted glucocorticoid + noradrenergic action**, and β-blockade is sufficient to prevent it (Schwabe et al. 2011, *J. Neurosci.* 31:17317). Replication work (Kool et al. 2023, *Neurobiol. Stress*) finds the effect is conditional — it emerges most cleanly in high-load conditions, in subjects with strong cortisol reactivity, or with chronic stressors — which matters for the RQS audience: the 2022 drawdown is exactly a high-load, chronic-stress environment.

### 3.4 The formal mapping to PM trade behavior

In an RL frame, PM trade behavior decomposes as:

```
Trade decision ~ w · TradeBased(model of market, horizon H) + (1−w) · TradeFree(cached habits)
```

- "Fight" — active-risk up, new positions initiated, thesis-driven — is an MB trace: tree-search under the analyst's generative market model, longer effective horizon.
- "Flight" — active-risk down, de-grossing, position trimming, factor-neutralizing — is predominantly an MF trace: cached heuristics ("cut losers", "raise cash"), short horizon.

A stress-induced drop in `w` is empirically indistinguishable from "the PM stopped thinking about theses and started running to cash." The computational model *predicts* it will scale with proxies of cortisol-axis activation (market stress indices, personal drawdown magnitudes) and be moderated by working-memory-like traits (years of experience, post-training stability). This is a testable hypothesis on our data.

---

## 4. Computational psychiatry: aberrant precision as a model of bias

### 4.1 The core proposition

Adams, Stephan, Brown, Frith & Friston (2013, *Front. Psychiatry* 4:47, "The computational anatomy of psychosis") propose that many psychiatric symptoms are expressible as a **single underlying abnormality**: an aberrant encoding of precision. Specifically they model psychotic symptoms (hallucinations, delusions, catatonia, abnormal smooth-pursuit eye movements) as arising from a **reduction in the precision of prior beliefs relative to sensory evidence**. With priors down-weighted, sensory noise drives the posterior too strongly — the system chases noise (hallucinations) and over-updates on spurious evidence (delusions).

The mirror case — **precision of priors too high** — produces the opposite pathology: the system ignores disconfirming evidence, updates too slowly, and becomes rigid. This is the formal home of **overconfidence**: it is an abnormally high precision assigned to the agent's own prior (point-estimate) over the world or its own metacognitive self-model.

### 4.2 Equations from the Hierarchical Gaussian Filter

The **Hierarchical Gaussian Filter** (Mathys, Daunizeau, Friston & Stephan 2011, *Front. Hum. Neurosci.* 5:39, "A Bayesian foundation for individual learning under uncertainty"; Mathys et al. 2014, *Front. Hum. Neurosci.* 8:825, "Uncertainty in perception and the Hierarchical Gaussian Filter") is the working quant model. The agent has a hierarchy of latent Gaussian states `x_1, x_2, x_3, …` where the volatility of level `i` is governed by level `i+1`. The update equations are one-step and analytic:

```
μ_i^(k)     = μ_i^(k−1)  +  (π̂_{i−1}^(k) / π_i^(k)) · δ_{i−1}^(k)
            \_______________/       \___________/
             posterior mean        precision-weighted prediction error

δ_{i−1}^(k) = μ_{i−1}^(k) − μ̂_{i−1}^(k)       (low-level prediction error)
π_i^(k)     = π̂_i^(k) + π̂_{i−1}^(k)           (posterior precision)
π̂_i^(k)     = 1 / (σ_i^(k−1) + exp(κ_i · μ_{i+1}^(k−1) + ω_i))   (prior precision, volatility-driven)
```

The central quantity is the **precision ratio** `π̂_{i−1}/π_i`, which plays the role of a **Kalman-gain-like learning rate**. When sensory precision is high relative to prior precision, the agent updates aggressively. When prior precision is high (stable belief), the agent ignores evidence.

`κ` is the coupling strength to higher levels; `ω` is the tonic (evolutionary-slow) volatility parameter. Individual differences in `(κ, ω)` across levels are the **computational phenotype** of the agent — and they are identifiable from behavioral choice data with surprisingly modest sample sizes. Mathys's work (see the Mathys lab's computational psychiatry implementations, e.g. PyHGF and the Julia HGF.jl) has been used to recover these parameters in anxiety, autism, schizophrenia, gambling disorder, and more.

### 4.3 Metacognitive priors: overconfidence as a mis-set hyperparameter

Fleming & Daw (2017, *Psychol. Rev.* 124:91–114) cast confidence as a second-order inference `p(decision correct | own evidence sample, own action)`. In this framework **overconfidence** is straightforward:

- If the prior over "self-model competence" is too tight (high precision), the agent under-updates on evidence of error — hence the persistent overplacement effect.
- If the prior over "my estimate is right" is too tight, the posterior variance is compressed and *every* decision looks high-confidence.
- These two priors are dissociable: an analyst can have realistic self-assessment (calibrated meta-d') but systematically narrow thesis priors (high overprecision), or vice versa.

This is the computational-psychiatry restatement of Moore & Healy 2008's (*Psychol. Rev.*) taxonomy. Overestimation/overplacement/overprecision are three different mis-set precision hyperparameters at three different levels of the hierarchy.

### 4.4 Stress as a catastrophic precision update

What happens to the HGF under acute stress? The empirical signatures are:

- **Higher `ω` at low levels** — the system infers more sensory volatility, which inflates the learning rate on incoming data.
- **Narrower temporal integration** — high volatility at the environmental level implies past data is less diagnostic of the present, so the effective horizon shrinks.
- **Priors on cached habits become more precise** — the MB/MF arbiter shifts toward MF because MB's cached variance estimates lose reliability.

These three changes together reproduce the behavioral syndrome of the 2022 drawdown: analyst horizons compress, priors on dominant narratives become harder to dislodge (so everyone chases the same trades), and PMs fall back on cached de-grossing procedures.

---

## 5. Resource-rational analysis

### 5.1 Why "rational" agents look biased

Lieder & Griffiths (2020, *Behav. Brain Sci.* 43:e1, "Resource-rational analysis: Understanding human cognition as the optimal use of limited computational resources") formalize a bridge between normative rationality (pick the action with the highest expected utility) and observed human biases. An **ideal resource-rational agent** solves:

```
π* = arg max_π  E[U(a, s)] − cost(π)
```

where `π` is a *cognitive strategy* (not a policy over actions directly) and `cost(π)` is the computational resource required. Bounded optimality: the agent is optimal *given* its resource constraints.

The punchline is that **many "biases" in the Kahneman-Tversky canon are resource-rational under plausible cost functions.** Availability heuristic, anchoring, neglect of sample size — each can be derived as the cost-optimal approximation to the Bayesian posterior when the agent has limited time or working memory. "Biased" is the wrong description; "efficient under realistic constraints" is the accurate one.

### 5.2 The implication for fund measurement strategy

This is the intellectual argument that turns our project from a diagnosis into a prescription:

- Telling an analyst "stop being biased" is incoherent — the bias is the Bayes-optimal output under their resource budget.
- Changing the analyst's **resource budget** (more time, less concurrent coverage, pre-committed checklists that externalize computation) does change behavior because it changes what is optimal.
- Alternatively, **measuring and compensating** for the predictable bias at the fund level (per-analyst normalization, tail-weighting, horizon-aware horizons) works because the bias is systematic and therefore forecastable.

The presentation's recommendation framework should lean hard on this. We are not telling people to be better humans — we are adjusting our measurement to match the computational model they are already running.

### 5.3 Active inference accounts of investor behavior

Formal active-inference papers on financial markets are scarce; the framework is young and most applications have been in robotics and psychiatry. What does exist is:

- Hirsh, Mar & Peterson (2012, *Psychol. Rev.* 119:304–320) "Psychological entropy: A framework for understanding uncertainty-related anxiety" connects free-energy minimization to anxiety in economic contexts.
- Schwartenbeck et al. (2015, *Front. Hum. Neurosci.* 9:598) "Evidence for surprise minimization over value maximization in choice behavior" — humans in economic tasks deviate from pure expected-utility in a direction predicted by free-energy minimization (epistemic-value terms).
- Constant et al. (2019, *Front. Psychol.*) and subsequent work from the active-inference community extend the formalism to multi-agent social coordination.

The literature does not yet have a canonical "active inference of fund managers" paper — which is itself a gap the RQS presentation can nod to. The computational tools exist; the application is open.

---

## 6. Bridge to our empirical findings

### 6.1 Per-analyst normalization

What we are measuring computationally: a scalar read-out of each analyst's posterior precision on their own thesis, filtered through their personal verbal encoder. The encoder is a stable trait of each analyst (the Hyland/Biber linguistic-stance literature is consistent with this). The correct statistical object is the **within-analyst percentile** of the precision read-out — which removes the encoder and leaves us with the computationally relevant quantity.

In HGF terms: we are estimating `π_i^(k)` for each analyst at each time, but only the *ranked position* within that analyst's history is comparable across analysts. Any absolute-level analysis is contaminated by individual differences in `(κ, ω)` — and we have the formal argument that those differences are large (computational phenotype literature).

### 6.2 U-shaped tails

The Sanders-Hangya-Kepecs (*Neuron* 2016) signature predicts exactly a U-shape between reported confidence and accuracy for a Bayesian-ish reporter. Our data matches: extreme confidences carry the signal, middling confidences are chance. This is the empirical fingerprint that our analysts are doing something computationally non-trivial, and it is the reason we weight tails heavily in any return-prediction regression.

### 6.3 2022 horizon compression

Two compatible mechanisms, both formal:

- **Bayesian temporal discounting.** Under a generative model with high inferred environmental volatility (i.e. high `μ_{i+1}` in the HGF), past data is down-weighted exponentially faster. The effective horizon `H_eff = 1/volatility` collapses. The analyst is not "panicking" — they are correctly inferring a regime change and updating priors accordingly. What we see as horizon compression is the behavioral output of a correct volatility update.
- **MB→MF arbiter shift.** Tree-search over long horizons is the most computationally expensive mode. Under stress, the arbiter `w` drops and shallower-horizon MF control takes over. Again, this is formally predicted by the Daw-2005 uncertainty-arbitration rule combined with the Otto-2013 stress finding.

Both mechanisms predict the horizon compression we observed in 2022, and the two make partially dissociable predictions (volatility-inference alone predicts compression symmetric around the regime change; MF-shift predicts asymmetry: compression persists until cortisol returns to baseline). This is a second-order testable hypothesis on analyst notes from 2022Q2–2023Q1.

### 6.4 Fight vs flight under stress

- **Fight** (active risk up, new position, MB trace) — a high-`w` episode, evidence the PM's MB controller has access to a thesis that beats the MF default. Under mild-to-moderate stress, a high-WMC PM can stay in fight mode.
- **Flight** (active risk down, de-grossing, MF trace) — a low-`w` episode, the PM's arbiter has thrown weight onto cached procedures.

The formal prediction is that **personal working-memory/experience proxies should moderate flight probability** at a given market stress level. This maps to the Otto-2013 result and is directly testable in our data: PMs with longer tenure, lower concurrent-coverage load, and lower self-reported anxiety should show less flight-mode-switching at a given VIX level.

---

## 7. Why this frame is what the quant audience will accept

The three translations below are the currency this audience trades in. Each replaces a psychology-language claim with a formal-language claim that is tractable and falsifiable.

| Psychology finding | Formal restatement | Falsifiable prediction |
| --- | --- | --- |
| "Analysts are overconfident" | Prior precision on self-model is mis-set high | Confidence-accuracy calibration curves should show a specific overshoot; meta-d' < d' by a measurable amount |
| "Stress causes panic selling" | Arbiter weight `w` on MB controller collapses; `κ, ω` hyperparameters shift | Flight episodes should scale with cortisol proxies and be moderated by WMC proxies; post-stress recovery should have a specific time course |
| "Experienced PMs are calmer under stress" | Higher WMC → MB-protective; longer experience → more accurate MF cache, so `w` drop matters less | Effect size on Sharpe under stress should be monotonic in tenure, controlling for style |

This is the bar Rockefeller expects: every qualitative claim has a quantitative analogue, and every quantitative analogue comes with a prediction the data can rule out.

---

## 8. Citations (primary sources, verified)

### Bayesian brain / free energy / predictive coding
- Dayan, P., Hinton, G.E., Neal, R.M. & Zemel, R.S. (1995) "The Helmholtz machine." *Neural Computation* 7:889–904. https://pubmed.ncbi.nlm.nih.gov/7584891/
- Hinton, G.E., Dayan, P., Frey, B.J. & Neal, R.M. (1995) "The wake-sleep algorithm for unsupervised neural networks." *Science* 268:1158–1161. https://www.cs.toronto.edu/~hinton/csc2535/readings/ws.pdf
- Rao, R.P.N. & Ballard, D.H. (1999) "Predictive coding in the visual cortex." *Nat. Neurosci.* 2:79–87. https://www.nature.com/articles/nn0199_79
- Friston, K. (2010) "The free-energy principle: a unified brain theory?" *Nat. Rev. Neurosci.* 11:127–138. https://www.nature.com/articles/nrn2787
- Bastos, A.M., Usrey, W.M., Adams, R.A., Mangun, G.R., Fries, P. & Friston, K.J. (2012) "Canonical Microcircuits for Predictive Coding." *Neuron* 76:695–711. https://www.sciencedirect.com/science/article/pii/S0896627312009592
- Parr, T. & Friston, K.J. (2019) "Generalised free energy and active inference." *Biological Cybernetics* 113:495–513. https://link.springer.com/article/10.1007/s00422-019-00805-w
- Yon, D. & Frith, C.D. (2021) "Precision and the Bayesian brain." *Current Biology* 31:R1026–R1032. https://www.sciencedirect.com/science/article/pii/S0960982221010344

### DDM and confidence
- Ratcliff, R. & McKoon, G. (2008) "The diffusion decision model: Theory and data for two-choice decision tasks." *Neural Computation* 20:873–922. https://direct.mit.edu/neco/article/20/4/873/7299/
- Pleskac, T.J. & Busemeyer, J.R. (2010) "Two-stage dynamic signal detection: A theory of choice, decision time, and confidence." *Psychol. Rev.* 117:864–901. https://pubmed.ncbi.nlm.nih.gov/20658856/
- Kiani, R., Corthell, L. & Shadlen, M.N. (2014) "Choice certainty is informed by both evidence and decision time." *Neuron* 84:1329–1342. https://www.cell.com/neuron/fulltext/S0896-6273(14)01096-4
- Sanders, J.I., Hangya, B. & Kepecs, A. (2016) "Signatures of a statistical computation in the human sense of confidence." *Neuron* 90:499–506. https://pmc.ncbi.nlm.nih.gov/articles/PMC5350614/
- Pouget, A., Drugowitsch, J. & Kepecs, A. (2016) "Confidence and certainty: distinct probabilistic quantities for different goals." *Nat. Neurosci.* 19:366–374. https://www.nature.com/articles/nn.4240

### Model-based vs model-free RL
- Daw, N.D., Niv, Y. & Dayan, P. (2005) "Uncertainty-based competition between prefrontal and dorsolateral striatal systems for behavioral control." *Nat. Neurosci.* 8:1704–1711. https://www.nature.com/articles/nn1560
- Daw, N.D., Gershman, S.J., Seymour, B., Dayan, P. & Dolan, R.J. (2011) "Model-based influences on humans' choices and striatal prediction errors." *Neuron* 69:1204–1215. https://www.sciencedirect.com/science/article/pii/S0896627311001255
- Otto, A.R., Raio, C.M., Chiang, A., Phelps, E.A. & Daw, N.D. (2013) "Working-memory capacity protects model-based learning from stress." *PNAS* 110:20941–20946. https://www.pnas.org/content/110/52/20941
- Schwabe, L. & Wolf, O.T. (2013) "Stress and multiple memory systems: from 'thinking' to 'doing'." *Trends Cogn. Sci.* 17:60–68. https://www.sciencedirect.com/science/article/abs/pii/S1364661312002811

### Computational psychiatry
- Mathys, C., Daunizeau, J., Friston, K.J. & Stephan, K.E. (2011) "A Bayesian foundation for individual learning under uncertainty." *Front. Hum. Neurosci.* 5:39. https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2011.00039/full
- Adams, R.A., Stephan, K.E., Brown, H.R., Frith, C.D. & Friston, K.J. (2013) "The computational anatomy of psychosis." *Front. Psychiatry* 4:47. https://pmc.ncbi.nlm.nih.gov/articles/PMC3667557/
- Mathys, C.D., Lomakina, E.I., Daunizeau, J., Iglesias, S., Brodersen, K.H., Friston, K.J. & Stephan, K.E. (2014) "Uncertainty in perception and the Hierarchical Gaussian Filter." *Front. Hum. Neurosci.* 8:825. https://www.frontiersin.org/journals/human-neuroscience/articles/10.3389/fnhum.2014.00825/full
- Fleming, S.M. & Daw, N.D. (2017) "Self-evaluation of decision-making: A general Bayesian framework for metacognitive computation." *Psychol. Rev.* 124:91–114. https://pmc.ncbi.nlm.nih.gov/articles/PMC5178868/

### Resource-rational analysis
- Lieder, F. & Griffiths, T.L. (2020) "Resource-rational analysis: Understanding human cognition as the optimal use of limited computational resources." *Behav. Brain Sci.* 43:e1. https://www.cambridge.org/core/journals/behavioral-and-brain-sciences/article/resourcerational-analysis-understanding-human-cognition-as-the-optimal-use-of-limited-computational-resources/586866D9AD1D1EA7A1EECE217D392F4A

---

## 9. Candidate canonical graphs

Four graphs are needed to make the math concrete on slide. All should be produced by scripts (per the scripted-analysis rule), with straight lines and visible dots per house style.

1. **DDM trajectories with confidence colormap.** Several sample paths of `x(t) = v·t + σ·W_t` between `±a/2` boundaries, each colored by the posterior confidence at termination (a function of `x(T)` and `T`, following Kiani-Corthell-Shadlen). Annotate fast/high-conf, slow/low-conf, and change-of-mind trajectories. This gives the audience the DDM intuition and the confidence readout in one picture.

2. **Sanders-Hangya-Kepecs U-shape.** Synthetic data from an ideal Bayesian observer showing: (top) confidence-as-function-of-stimulus-strength, split by correct/incorrect, reproducing the folded-X; (bottom) accuracy-as-function-of-reported-confidence, reproducing the U-shape. Overlay our analyst-confidence-vs-excess-return curve next to it. This is the single most important slide — it makes the "why tails carry signal" claim visually obvious.

3. **HGF trajectory under a volatility shift.** Three-level HGF with a simulated environmental regime change mid-series. Top panel: raw outcomes. Second panel: `μ_1` (perceptual belief). Third panel: `μ_2` (environmental mean). Fourth panel: `μ_3` (volatility). Show learning-rate `π̂_1/π_1` as a separate trace. Annotate the precision spike at the regime change. This is the formal analog to "2022 horizon compression" and gives a quant-credible picture of what the brain is doing.

4. **MB/MF weighting under stress.** Simulated two-step-task agent with `w` as a free parameter. Panel A: stay-probability matrices under `w=1` (pure MB, reward×transition interaction) vs `w=0` (pure MF, reward main effect only) vs `w=0.5`. Panel B: fitted `w` as a function of stress dose, with confidence bands — overlaid on Otto-2013's empirical result. This gives the formal backbone for the fight/flight decomposition slide.

A fifth optional graph, if room allows: **the free-energy schematic** — three panels showing (a) the generative model as a graphical model, (b) the free-energy decomposition `F = complexity − accuracy`, (c) what changes when precision is up-regulated (accuracy term dominates, posterior tracks evidence more tightly). This is more conceptual than quantitative; include only if the audience asks for derivation depth.
