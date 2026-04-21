# Metacognition and Confidence — Deep Research

## Executive one-liner
Metacognitive confidence is a distinct neurocognitive faculty — dissociable from task skill, anchored in anterior prefrontal and orbitofrontal circuitry, and expressed through each person's idiosyncratic verbal style — which is why the only valid cross-analyst signal is *percentile within that analyst's own historical distribution*, not raw confidence level.

---

## The psychology route

### 1. Moore & Healy's taxonomy: confidence is not one thing

Don Moore and Paul Healy's 2008 *Psychological Review* paper "The Trouble with Overconfidence" is the canonical reconciliation of three mutually confused constructs that had been piling up in the literature for two decades (Moore & Healy 2008, *Psychol. Rev.*, 115(2):502–517). The paper's contribution is not a single new experiment — it is a taxonomy that resolves why apparently contradictory overconfidence findings existed:

- **Overestimation** — believing your absolute performance is better than it actually is ("I got 18/20") when you got 14/20.
- **Overplacement** — believing you are better than others (the "better-than-average" effect). A rank-order claim.
- **Overprecision** — being too certain your belief is correct — i.e. your subjective probability distribution over the truth is too narrow. This is the one that maps most directly onto an analyst saying "I'm 90% sure" when the base rate says 70%.

Moore & Healy showed experimentally that these three dissociate, and in fact move in opposite directions as a function of task difficulty. On **hard** tasks people *overestimate* their own score but *underplace* themselves relative to others (the hard-easy effect). On **easy** tasks the pattern flips. Crucially, **overprecision persists across difficulty levels** and is the most robust of the three — which is why it is the construct most relevant to professional investment decisions, where analysts rarely self-rank against peers but routinely state probabilistic beliefs.

**Why this matters for RQS.** When we say "analyst confidence," we almost always mean overprecision: the narrowness of the implied posterior around their point-estimate thesis. The empirical literature says this is the most stable, most persistent, and therefore most signal-rich of the three overconfidence components.

### 2. Is confidence calibration a trait? Partially.

Two separate lines of evidence bear on the question of whether an analyst's confidence-calibration style is stable:

- **Heritability.** Cesarini et al. (2009, *JEEA* 7(2–3):617–627) used a Swedish twin design (N=460 pairs) and ACE decomposition. They found **16–34% of variation in overconfidence is genetic**, 5–11% shared environment, and the rest unique experience. The construct is heritable but far from fully determined.
- **Test-retest reliability of metacognitive accuracy (meta-d').** This is more nuanced. Rouault et al. (2018) and the more comprehensive Guggenmos (2021, *Neurosci. Conscious.*) show that **individual differences in overall confidence level** are highly stable across sessions, but **metacognitive sensitivity** (meta-d'/d' — how well confidence discriminates correct from incorrect) has surprisingly poor test-retest reliability at standard trial counts. Fleming, Ryu, Golfinos & Blackmon (2014, *Brain*) and subsequent work show the confidence level trait is reliable; the metacognitive discrimination ability is reliable only with very large N.

**Implication for analyst data.** Mean/baseline confidence level is trait-like and varies substantially across analysts. A "hawkish" analyst is still a hawkish analyst six months later. This is the empirical grounding for per-analyst normalization: the trait is real, which is precisely why absolute comparisons are contaminated.

### 3. The gap between felt and expressed confidence — the stance/hedging literature

Psychology tells you about felt confidence; linguistics tells you how it reaches the page. Ken Hyland's corpus work on **hedging** in academic and professional writing is the foundational text (Hyland 1998, *Hedging in Scientific Research Articles*; Hyland 2005 "Stance and engagement," *Discourse Studies*). Hyland decomposes writer stance into four marker classes:

1. **Hedges** — *may, might, could, suggest, possibly, appears* — reduce epistemic commitment.
2. **Boosters** — *clearly, definitely, in fact, demonstrate, establish* — increase commitment.
3. **Attitude markers** — evaluative adjectives/adverbs (*surprisingly, unfortunately*).
4. **Self-mention** — *I/we think*.

Hyland further classifies lexical hedges into five forms: modal verbs, epistemic lexical verbs, epistemic adjectives, epistemic adverbs, and epistemic nouns. Douglas Biber's complementary corpus work (Biber 2006, "Stance in spoken and written university registers") establishes that **stance markers vary systematically across individuals and sub-disciplines** — and they vary more across writers than across topics when topic is held constant.

The diachronic evidence (Hyland & Jiang, multiple papers through 2020s) shows a **drift toward more boosters and fewer hedges in scientific writing over the last 50 years**, but the *within-writer* signature remains comparatively stable. An individual writer's hedge/booster ratio is a personal-style parameter.

**The core implication.** Two analysts can hold identical posterior distributions and produce notes with wildly different booster/hedge counts, driven by personal discursive style. Hyland's literature tells you that style is measurable, stable per writer, and substantially independent of underlying belief. This is the empirical linguistic argument that **absolute textual confidence is uncomparable across writers — the only cross-analyst valid measure is within-writer percentile**.

### 4. NLP / LLM-based confidence extraction — prior art

The state of the art falls into three generations:

- **Dictionary-based (first generation).** The Loughran-McDonald master dictionary (Loughran & McDonald 2011, *J. Finance*; expansions through 2024) is the default for financial text. It includes an explicit **uncertainty** word list (alongside positive, negative, litigious, strong/weak modal, constraining). This is the benchmark against which any LLM-based method should be sanity-checked.
- **Embedding/classifier-based (second generation).** FinBERT, RoBERTa-fin variants, and similar domain-finetuned encoders on earnings-call and 10-K corpora.
- **LLM prompt-based (third generation, 2023+).** Alex Kim's 2024 working paper "Financial Statement Analysis with Large Language Models" (arXiv 2407.17866) demonstrates that GPT-4, when prompted to report a 0–1 confidence on its forecast, produces scores that are **monotonically related to forecast accuracy** — i.e. GPT self-reported confidence is informative. Recent surveys (Frontiers in AI 2025) confirm: **LLM decision-making is prompt-sensitive**, so any confidence-extraction pipeline must (a) fix a prompt template, (b) report inter-prompt stability, and (c) validate against a gold standard (human annotators or Loughran-McDonald as a weak label).

**Gold standards that exist.** In medicine, the MIMIC-III notes corpus has been used for uncertainty annotation. In finance, Loughran-McDonald is the de facto reference. In legal text, the "hedges in legal writing" corpus (Smirnova 2025, *Int. J. Appl. Linguistics*) exists. None of these is ideal for analyst notes; the defensible validation path is a small human-labeled sample of our own analysts' notes and the inter-rater agreement that produces.

---

## The brain-chemistry route

### 1. The anterior prefrontal cortex as the metacognitive hub (Fleming)

Stephen Fleming's 2010 *Science* paper is the single most-cited result in this literature (Fleming, Weil, Nagy, Dolan, Rees 2010, "Relating introspective accuracy to individual differences in brain structure," *Science* 329:1541–1543). Protocol: 32 healthy adults did a two-alternative forced-choice visual task — which of two screens contains the brighter patch — and then rated confidence on each trial. Metacognitive accuracy was computed as the degree to which confidence tracked correctness, controlling for perceptual performance (first-order d'). They then did **voxel-based morphometry (VBM)** on structural MRI.

Result: metacognitive accuracy correlated with **grey-matter volume in the right anterior prefrontal cortex (aPFC / BA10 / rostrolateral PFC)**, and with white-matter microstructure in tracts connecting that region. The first-order perceptual skill did *not* correlate with aPFC — so the region is specifically associated with the meta-level, not with doing the task well.

Three methodological points the RQS audience will care about:
- The correlation was partial — aPFC structure predicted metacognition *after* partialing out first-order d'. This dissociates the meta-ability from the object-level ability.
- It was lateralized right, consistent with hemispheric specialization literature on self-monitoring.
- BA10 is evolutionarily expanded in humans relative to other primates — it is one of the most uniquely-human cortical regions (Ramnani & Owen 2004, *Nat. Rev. Neurosci.*).

Fleming & Dolan's 2012 review in *Philos. Trans. R. Soc. B* 367:1338–1349 extends this: **rostral and dorsal lateral PFC mediate retrospective judgments** ("did I get that right?"), while **medial PFC mediates prospective judgments** ("am I going to get this right?"). Morales, Lau & Fleming (2018, *J. Neurosci.* 38:3534) used multivoxel pattern analysis to show that aPFC contains both **domain-general** confidence signals (shared across perceptual and memory tasks) and **domain-specific** signals — a computational hierarchy of metacognition.

Rouault & Fleming (2020, *PNAS*) extended the picture upward: **ventromedial PFC and ventral striatum** encode global self-performance estimates (SPEs) — beliefs about one's ability across blocks, not just single trials. The ventral striatum activity tracked how accurately SPEs matched objective difficulty across individuals. This is the neural substrate for the "I'm a good stock-picker" belief level, as distinct from "I'm confident about this stock right now."

### 2. Orbitofrontal cortex and decision confidence at the cellular level (Kepecs)

Adam Kepecs's program of work tackles confidence at single-neuron resolution. The foundational paper is Kepecs, Uchida, Zariwala & Mainen 2008, *Nature* 455:227–231 ("Neural correlates, computation and behavioural impact of decision confidence"). Rats performed an odor categorization task where stimulus difficulty was manipulated by varying the mixture ratio of two odorants. The experimenters could infer, from behavior alone (wait times for a reward), that rats had a graded confidence signal.

Neural recording in **orbitofrontal cortex (OFC)** found ~20% of neurons whose firing during the reward-anticipation period showed the diagnostic "X pattern" predicted by signal-detection theory:

- For **correct** trials, firing **decreased** as stimulus difficulty increased.
- For **error** trials, firing **increased** as stimulus difficulty increased.

The intersection forms an X. This pattern cannot be produced by encoding stimulus alone or attention alone; it is a mathematical signature of computing decision confidence. Kepecs & Mainen (2012, *Philos. Trans. R. Soc. B* 367:1322) formalized the theory: confidence is computed as the absolute log posterior ratio — the "decision distance" between evidence for the chosen and unchosen options.

The causal test came from Lak, Costa, Romberg, Koulakov, Mainen & Kepecs (2014, *Neuron* 84:190–201): **inactivating OFC disrupted confidence-based waiting behavior without affecting first-order choice accuracy.** The dissociation is clean — rats still chose correctly at the same rate, they just lost the ability to wait longer when they were more confident. This mirrors the structural dissociation Fleming found in humans: first-order skill and meta-level signal live in different circuits.

### 3. Dopamine and confidence

The dopaminergic contribution is the most recently-worked-out piece. Lak, Nomoto, Keramati, Sakagami & Kepecs (2017, *Current Biology* 27:821) recorded from midbrain VTA dopamine neurons in rats during the same perceptual task. Finding: **VTA dopamine prediction-error signals are modulated by confidence** — when a rat was highly confident but wrong, the negative prediction error was larger; when unconfident and right, the positive PE was larger. Dopamine neurons integrate reward outcome with the subjective probability that the action was correct.

A complementary line (Lak et al. 2020, *Neuron* "Dopaminergic and Prefrontal Basis of Learning from Sensory Confidence and Reward Value") shows that dopamine-PFC loops are how confidence feeds back into learning: an animal that is confident and wrong updates more than one that is unsure and wrong. This is the neurochemical mechanism by which overconfident agents fail to learn — their prediction errors are inflated in both directions, giving a noisier learning signal. There is a direct line from this to why overconfident investment styles may converge slowly toward calibration.

### 4. Confidence and accuracy dissociate — the single most important empirical point

Throughout the entire literature, one result recurs: **confidence and accuracy are dissociable.** In Fleming 2010, people matched on perceptual d' differed in metacognitive accuracy. In Lak 2014, OFC inactivation left accuracy intact but abolished confidence-appropriate waiting. In Morales, Lau & Fleming 2018, aPFC MVPA patterns predicted confidence but were orthogonal to task accuracy. In Rouault, Seow, Gillan & Fleming (2018, *Biol. Psychiatry* 83:690), psychiatric symptom dimensions predicted metacognitive bias and sensitivity but **not** first-order task performance — a "double dissociation" (their term) between meta-level and object-level.

The practical consequence is stark: **the quality of an analyst's stock picks and the style of their confidence reporting are controlled by partly-independent neurocognitive systems.** You cannot infer skill from stated confidence, and you cannot infer confidence appropriateness from P&L. They need to be measured separately and only combined with care — which is exactly the experimental structure the RQS project built.

### 5. Does expertise fix the problem? Mostly no.

Moore, Tenney & Haran's work and the broader calibration literature (summarized in Moore 2020, *Perfectly Confident*) say that domain experts are typically **not** better calibrated than novices once difficulty is controlled. Tetlock's "Expert Political Judgment" (2005) famously showed political forecasters at chance; the later *Superforecasting* (Tetlock & Gardner 2015) work showed that calibration is a learnable skill but that most experts never develop it. Economists and meteorologists (who get immediate probabilistic feedback with scoring rules) are the main exceptions; physicians and lawyers are among the most overconfident.

The implication is not pessimistic — it is **procedural**: calibration does not come automatically with experience, but it does come with the right feedback loop. Percentile-normalized confidence tracking over an analyst's career, with return outcomes tagged, is precisely that feedback loop.

---

## Bridge to our empirical finding

The RQS experiment extracted confidence-over-time from analyst notes and found that *percentile of each analyst's own historical distribution* is the signal that tracks excess returns — not absolute confidence level. The science gives this finding four independent mechanistic supports:

1. **Moore & Healy 2008 overprecision** is the type of overconfidence most stably present in probabilistic professional belief, and it is substantially a trait. Raw levels vary across people; deviation-from-own-mean is what carries signal.
2. **Cesarini 2009 heritability (16–34%)** plus **Fleming 2014 / Guggenmos 2021 test-retest stability of baseline confidence** establish that per-analyst baseline is a stable trait parameter, not noise — so subtracting it out is mathematically justified, not just a convenience.
3. **Hyland's hedging / Biber's stance** corpus linguistics shows that verbal style (hedge/booster ratios) is a writer-level personal parameter largely independent of belief content. Any absolute cross-writer textual confidence measure is contaminated by style; only within-writer deviation strips this out.
4. **Fleming aPFC + Kepecs OFC + Rouault vmPFC/striatum** show that confidence is generated by neural circuits whose gain and setpoint vary across individuals (grey-matter volume in aPFC predicts metacognitive discrimination). Different analysts run on literally different hardware settings. Within-person percentile is the scale-invariant readout that survives this.

In slide form: "Measuring analyst confidence without per-analyst normalization is like comparing stock prices without adjusting for currency." The science says the currency is partly genetic (Cesarini), partly neuroanatomical (Fleming 2010), partly stable writing style (Hyland), and fully individual.

---

## Citations

- Biber, D. (2006). "Stance in spoken and written university registers." *J. English Acad. Purposes* 5:97–116. https://jan.ucc.nau.edu/biber/Biber/Biber_2006.pdf
- Cesarini, D., Johannesson, M., Lichtenstein, P., Sandewall, Ö., Wallace, B. (2009). "Heritability of overconfidence." *J. Eur. Econ. Assoc.* 7(2–3):617–627. https://onlinelibrary.wiley.com/doi/abs/10.1162/JEEA.2009.7.2-3.617
- Fleming, S.M., Weil, R.S., Nagy, Z., Dolan, R.J., Rees, G. (2010). "Relating introspective accuracy to individual differences in brain structure." *Science* 329:1541–1543. https://www.science.org/doi/10.1126/science.1191883
- Fleming, S.M., Dolan, R.J. (2012). "The neural basis of metacognitive ability." *Philos. Trans. R. Soc. B* 367:1338–1349. https://royalsocietypublishing.org/doi/10.1098/rstb.2011.0417
- Guggenmos, M. (2021). "Measuring metacognitive performance: type 1 performance dependence and test-retest reliability." *Neurosci. Conscious.* 2021(1):niab040. https://academic.oup.com/nc/article/2021/1/niab040/6439622
- Hyland, K. (1998). *Hedging in Scientific Research Articles.* John Benjamins. https://benjamins.com/catalog/pbns.54
- Hyland, K. (2005). "Stance and engagement: a model of interaction in academic discourse." *Discourse Studies* 7:173–192.
- Kepecs, A., Uchida, N., Zariwala, H.A., Mainen, Z.F. (2008). "Neural correlates, computation and behavioural impact of decision confidence." *Nature* 455:227–231. https://www.nature.com/articles/nature07200
- Kepecs, A., Mainen, Z.F. (2012). "A computational framework for the study of confidence in humans and animals." *Philos. Trans. R. Soc. B* 367:1322–1337. https://pmc.ncbi.nlm.nih.gov/articles/PMC3318772/
- Kim, A.G., Muhn, M., Nikolaev, V.V. (2024). "Financial Statement Analysis with Large Language Models." arXiv 2407.17866. https://arxiv.org/html/2407.17866v1
- Lak, A., Costa, G.M., Romberg, E., Koulakov, A.A., Mainen, Z.F., Kepecs, A. (2014). "Orbitofrontal cortex is required for optimal waiting based on decision confidence." *Neuron* 84:190–201. https://www.cell.com/neuron/pdf/S0896-6273(14)00740-5.pdf
- Lak, A., Nomoto, K., Keramati, M., Sakagami, M., Kepecs, A. (2017). "Midbrain dopamine neurons signal belief in choice accuracy during a perceptual decision." *Current Biology* 27:821. https://www.cell.com/current-biology/fulltext/S0960-9822(17)30163-X
- Lak, A., Okun, M., Moss, M.M., Gurnani, H., Farrell, K., Wells, M.J., Reddy, C.B., Kepecs, A., Harris, K.D., Carandini, M. (2020). "Dopaminergic and prefrontal basis of learning from sensory confidence and reward value." *Neuron* 105:700–711.
- Loughran, T., McDonald, B. (2011). "When is a liability not a liability? Textual analysis, dictionaries, and 10-Ks." *J. Finance* 66:35–65. Master dictionary: https://sraf.nd.edu/loughranmcdonald-master-dictionary/
- Maniscalco, B., Lau, H. (2012). "A signal detection theoretic approach for estimating metacognitive sensitivity from confidence ratings." *Conscious. Cogn.* 21(1):422–430. https://pubmed.ncbi.nlm.nih.gov/22071269/
- Moore, D.A., Healy, P.J. (2008). "The trouble with overconfidence." *Psychol. Rev.* 115(2):502–517. https://healy.econ.ohio-state.edu/papers/Moore_Healy-TroubleWithOverconfidence.pdf
- Morales, J., Lau, H., Fleming, S.M. (2018). "Domain-general and domain-specific patterns of activity supporting metacognition in human prefrontal cortex." *J. Neurosci.* 38(14):3534–3546. https://www.jneurosci.org/content/38/14/3534
- Ramnani, N., Owen, A.M. (2004). "Anterior prefrontal cortex: insights into function from anatomy and neuroimaging." *Nat. Rev. Neurosci.* 5:184–194.
- Rouault, M., Seow, T., Gillan, C.M., Fleming, S.M. (2018). "Psychiatric symptom dimensions are associated with dissociable shifts in metacognition but not task performance." *Biol. Psychiatry* 84(6):443–451. https://pmc.ncbi.nlm.nih.gov/articles/PMC6117452/
- Rouault, M., Fleming, S.M. (2020). "Formation of global self-beliefs in the human brain." *PNAS* 117:27268–27276. https://www.pnas.org/doi/10.1073/pnas.2003094117
- Tetlock, P.E. (2005). *Expert Political Judgment.* Princeton UP.
- Tetlock, P.E., Gardner, D. (2015). *Superforecasting: The Art and Science of Prediction.* Crown.
- Wesson, C.J., Pulford, B.D. (2009). "Verbal expressions of confidence and doubt." *Psychol. Rep.* 105(1):151–160. https://doi.org/10.2466/PR0.105.1.151-160

---

## Candidate canonical graphs for the slide

1. **The Kepecs "X-pattern" confidence signature** (*Nature* 2008 Fig. 2 / Kepecs & Mainen 2012 Fig. 1). A two-line plot: x-axis = stimulus difficulty (easy→hard), y-axis = OFC firing rate (or, equivalently, subjective confidence). The line for *correct* trials slopes down with difficulty; the line for *error* trials slopes up. The two lines cross, forming an X. **Why it works on a slide:** this is the single cleanest, most portable empirical signature that confidence is a real computed quantity, not a post-hoc rationalization — and it works identically in rat OFC, human ratings, and our analyst data (confidence conditional on return outcome shows the same diverging pattern). Recreatable from scratch with our own data by binning on ex-post excess return quintiles.

2. **Fleming 2010 aPFC grey-matter vs. metacognitive accuracy scatterplot** (*Science* 2010 Fig. 2). A 32-point scatter, x-axis = grey-matter volume in right anterior PFC, y-axis = metacognitive accuracy (meta-d'/d'). Clear positive correlation. **Why it works:** visceral demonstration that people's metacognitive ability is literally anatomically different. For an RQS audience this is the "the hardware is different across analysts" punchline in a single image. Source from paper.

3. **Moore & Healy overestimation-vs-overplacement crossover** (*Psychol. Rev.* 2008 Fig. 4). Two lines crossing: on hard tasks people overestimate but underplace; on easy tasks they underestimate but overplace. **Why it works:** defuses audience challenges of the form "which overconfidence do you mean?" by showing the three are distinct and task-dependent. Pair with a one-sentence callout: "Our measure is overprecision — the one that is stable across difficulty."

4. **Per-analyst confidence distribution overlay** (to be built from our own data). Violin plots of confidence scores, one per analyst, sorted by median. Shows how dramatically the raw distributions differ. Then a second panel: same data after per-analyst percentile transformation, showing all distributions now uniform on [0,1]. **Why it works:** this is the slide that earns the methodology. It makes the normalization step self-evident rather than a defensive choice. Scripted from our confidence time-series; no external source needed.
