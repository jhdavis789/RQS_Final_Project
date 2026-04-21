# Network Neuroscience of Stress and Decision-Making — Deep Research

## Executive one-liner

Acute stress does not merely "activate the amygdala" — it **reconfigures the entire brain**. Within minutes, noradrenaline released from the locus coeruleus retunes connectivity across the cortex: the salience network is upregulated, the central executive network (CEN) is downregulated, and the default mode network (DMN) is pulled into a vigilance stance. The brain shifts from a reflective, long-horizon, integrative mode into a reflexive, short-horizon, threat-detection mode. This shift is *measurable*, *time-stamped*, and — via HRV and pupillometry — *field-deployable*. For an RQS audience, the takeaway is that every bias our analysts and PMs exhibited under stress is a downstream symptom of the same upstream network-reconfiguration event, and that event has a biomarker signature you can instrument on a Whoop strap and a workstation webcam.

## The three canonical networks (DMN, Salience, CEN)

Modern systems neuroscience describes the cortex not as a collection of areas but as a small set of **intrinsic connectivity networks (ICNs)** that remain coherent at rest and reconfigure dynamically during task. Three of these dominate the cognitive-control literature and constitute Menon's *triple-network* or *tripartite* model (Menon 2011, *Trends in Cognitive Sciences*).

### 1. Default Mode Network (DMN)

**Anatomy.** Medial prefrontal cortex (mPFC), posterior cingulate cortex / precuneus (PCC), bilateral angular gyri, medial temporal lobe / hippocampal formation. First characterized by Raichle and colleagues (Raichle et al. 2001, *PNAS*) as the "task-negative" network — a set of regions whose metabolic activity *decreased* during externally-directed cognition and *increased* during rest.

**Function.** Self-referential cognition, autobiographical memory, theory of mind, **prospection** (imagining the future), counterfactual simulation, and **mental time travel**. Buckner and colleagues later showed the DMN is not "idle" but is the substrate for simulating scenarios beyond the here-and-now. For a portfolio manager, the DMN is the long-horizon machine — the machinery that lets you reason about a 3-year thesis, imagine a counterfactual state of the world, and integrate episodic memory of past crises.

**Behavior under cognitive load.** Normally suppressed during demanding external tasks. Failure to deactivate the DMN during a task is associated with mind-wandering and performance errors. But critically for our story, DMN disengagement is not a simple on/off switch — it is titrated by the salience network.

### 2. Salience Network (SN)

**Anatomy.** Anchored in the **anterior insula (AI)** and **dorsal anterior cingulate cortex (dACC)**, with subcortical tendrils to amygdala, ventral striatum, substantia nigra / VTA, and hypothalamus (Seeley et al. 2007, *J. Neurosci.*). The von Economo neurons unique to great apes and humans are densest in exactly these two hubs.

**Function.** Detect *what matters*. The SN continuously evaluates the organism's interoceptive and exteroceptive stream for signals worth acting on — novelty, threat, reward, homeostatic violation, bodily sensation. It is the **switch** that chooses between internally-directed (DMN) and externally-directed (CEN) processing (Menon & Uddin 2010). When the insula flags something as salient, it orchestrates a handoff: DMN out, CEN in, or in extreme cases, amygdala/HPA-axis in.

**Behavior under stress.** This is the network that "goes up" under acute stress — Hermans et al. 2011 (below) is fundamentally a paper about salience-network takeover.

### 3. Central Executive Network / Frontoparietal Network (CEN / FPN)

**Anatomy.** Dorsolateral prefrontal cortex (dlPFC), posterior parietal cortex (PPC), lateral frontopolar cortex. Seeley et al. 2007 dissociated CEN from SN in the same paper that characterized the SN — two networks that often co-activate during "cognitive tasks" but are in fact dissociable and do different things.

**Function.** Goal-directed cognitive control. Working memory maintenance. Rule-based reasoning. Top-down attention allocation. Inhibition of prepotent responses. Cole et al. 2013 (*Nature Neuroscience*) showed the FPN contains **flexible hubs** — regions whose connectivity fingerprint updates rapidly to match the current task, making the FPN the brain's "task-set" layer.

**Behavior under stress.** Downregulated by stress. Critically, Arnsten (2015, *Nature Neuroscience*) showed at the molecular level *why*: high catecholamine levels in dlPFC activate α1-adrenergic and D1 feedforward cascades that open HCN and KCNQ potassium channels, weakening the recurrent synapses that sustain working-memory representations. **Stress literally depolarizes your dlPFC away from its working state.**

### Normal switching dynamics

In a non-stressed brain, the SN continuously arbitrates DMN↔CEN. At rest or during autobiographical thought, DMN dominates. When a task arrives, the AI/dACC detect it, suppress DMN, and engage CEN. Seeley et al. 2007 showed this triple-network configuration is present in resting-state intrinsic connectivity — it is the *baseline architecture* of the human cortex.

The key point for our audience: these are not metaphors. They are measurable networks with consistent anatomy across individuals, present in every healthy human scanned, and they *reconfigure* on time scales relevant to a trading day.

## The salience hijack — Hermans et al. 2011 *Science*

Hermans, van Marle, Ossewaarde et al. (2011, *Science* 334:1151-3) is the single most important paper in the stress-and-decision-making literature. The paper demonstrates, in humans, that acute stress is a **brain-wide network reconfiguration event driven by noradrenaline**.

### Design

Participants (n≈80 healthy adults across sub-studies) were exposed to a standardized acute stressor — watching clips of graphic violence from the film *Irréversible* during fMRI — compared to matched neutral clips. Heart rate, salivary cortisol and alpha-amylase (a noradrenergic proxy), and subjective negative affect were measured alongside the scan. Critically, the authors ran the experiment **three times in independent arms** with pharmacological manipulations:

1. **Propranolol** (β-adrenergic blocker) vs. placebo — blocking noradrenergic signalling.
2. **Metyrapone** (cortisol synthesis inhibitor) vs. placebo — blocking cortisol.
3. Both, in crossover design.

### The finding

During stress, a widely distributed network showed *increased* within-network functional connectivity and *increased* stimulus responsiveness. The network comprised:

- **Cortical nodes:** frontoinsular cortex (= anterior insula), dorsal anterior cingulate, inferotemporal cortex, temporoparietal cortex.
- **Subcortical nodes:** amygdala, thalamus, hypothalamus, midbrain (including locus coeruleus region).

This is — by any reasonable mapping — the **salience network plus its autonomic/HPA tendrils**. The magnitude of this network's upregulation correlated across subjects with the magnitude of their stress response (heart-rate increase, negative affect, alpha-amylase).

Propranolol **abolished** this reconfiguration. Metyrapone did not. Translation: the network shift is **noradrenergic**, not cortisol-driven, at least at this timescale.

### Why this matters for us

1. **It is a whole-brain event, not a regional one.** The old story — "stress activates the amygdala" — is incomplete. Acute stress restructures large-scale network topology.
2. **Salience is hijacked.** Under stress, the AI/dACC hub becomes hyper-coupled to vigilance and autonomic structures, and (per the 2014 review below) *decoupled* from executive structures. Every incoming stimulus is processed through a salience filter set to high gain. Innocuous tape can look like threat.
3. **Noradrenaline is the switch.** This is mechanistically precise and pharmacologically testable. It also tells us what to measure peripherally (pupil, HRV) because those signals index the same noradrenergic axis.
4. **It is reversible.** The paper shows the brain returns to baseline — but on its own clock, not ours.

## Time course of network reconfiguration

Hermans, Henckens, Joëls & Fernández (2014, *Trends in Neurosciences*, vol 37:304-314) synthesize the full temporal model. The acute-stress response is *biphasic*, with two overlapping pharmacological waves that affect large-scale networks on different clocks.

### Phase 1: Fast noradrenergic upregulation (seconds → ~30 minutes)

- **Trigger:** amygdala detects threat → projections to locus coeruleus and brainstem autonomic nuclei → system-wide noradrenaline release + sympathetic outflow + CRH-driven activation.
- **Network signature:** salience network ↑↑, CEN ↓ (or unaltered), DMN shifted toward vigilance. Pupil dilates. HRV collapses.
- **Behavioral phenotype:** vigilance, threat-scanning, narrow attention, automatic/habitual responding, loss working-memory capacity, horizon compression. This is the territory in which our analyst and PM experiments showed bias amplification.

### Phase 2: Slow glucocorticoid recovery (≈30 minutes → hours)

- **Trigger:** HPA axis → adrenal cortisol release peaks ~20-30 min post-onset.
- **Non-genomic cortisol effects** kick in within minutes via membrane receptors, but the **genomic effects** — which are the ones that *normalize* the brain — take 60-90 minutes to emerge through nuclear glucocorticoid receptors.
- **Network signature:** salience network ↓ back toward baseline; CEN ↑↑ *above* baseline (rebound); DMN re-engages; prefrontal-amygdala top-down control restored. Cortisol is the cleanup crew.
- **Behavioral phenotype:** restored cognitive flexibility, restored long-horizon reasoning, consolidation of the stressful episode into memory for future use.

### van Oort 2017 confirmation

van Oort et al. 2017 (*Neuroscience & Biobehavioral Reviews* 83:281-297) meta-reviewed the human stress-imaging literature across stressor types (CPT, MIST, socially-evaluated cold pressor, film clips, TSST-fMRI variants). Consistent findings:
- Salience network connectivity: increased under acute stress (robust replication).
- DMN: increased activity during stress (not decreased — participants could not fully disengage self-referential / rumination circuitry).
- CEN: heterogeneous — some studies show decrease, others no change or increase. The CEN response depends on whether the stressor demands ongoing cognitive performance.

### What this means for a PM in a 5-minute vs. 5-week drawdown

This temporal structure maps directly onto investment time horizons.

**5-minute drawdown (intraday vol spike, flash crash, news print):**
- You are in **Phase 1, pure noradrenergic**. Salience-hijack is maximal. dlPFC is weakened. Pupil is blown. HRV is on the floor.
- Expected behavioral signature: horizon compression (narrow to the last tick), loss of base-rate reasoning, heightened loss aversion, automatic/habitual trades (cutting winners, doubling losers), inability to hold a complex counterfactual in mind.
- **This is exactly where the analyst horizon-compression findings live** (see knowledge file 03).

**30-minute to 2-hour drawdown (bad earnings morning, FOMC aftermath):**
- You are in the **Phase 1 → Phase 2 crossover**. Cortisol non-genomic effects are starting but the prefrontal cleanup has not arrived yet. Decisions made here are physiologically compromised.
- This is the "do not trade within 30 minutes of a bad print" domain. Recommendations to build cooling-off periods into process map directly onto this window.

**Multi-day to 5-week drawdown:**
- You are now in a chronic-stress regime. Cortisol is elevated for hours per day, sleep is disrupted (knowledge file on chronobiology), DMN is dysregulated. Structural changes in dendritic architecture can accumulate over weeks (Arnsten 2015).
- Phenotype: entrenchment in thesis, ruminative re-checking, inability to update priors, exhaustion-driven capitulation. This is PM fight/flight territory (knowledge file 04).

## Dynamic functional connectivity

The classical fMRI story assumed connectivity between brain regions was roughly stationary — a property of the person, not the moment. Hutchison, Womelsdorf, Allen, Bandettini et al. (2013, *NeuroImage* 80:360-378) were the pivotal consensus statement that this is wrong: **connectivity fluctuates on the order of tens of seconds**, and those fluctuations are behaviorally meaningful.

### Methodology

**Sliding-window correlation analysis.** Take a 30-60 second window of BOLD signal from each region, compute the correlation matrix, slide the window by a few seconds, repeat. The resulting time-resolved connectivity matrices cluster, via k-means, into a discrete set of recurring **brain states** (Allen et al. 2014). A typical resting scan visits 5-7 distinct states.

Hutchison et al. catalogued the methodological pitfalls — head motion, window length, stationarity testing — but the core finding survives: brain-state occupancy and transition probabilities vary within-subject over minutes, between-subject as a trait, and with task/stress/affect.

### Stress and brain-state dynamics

Several groups (notably Vaisvaser et al. 2013, Young et al. 2017, Maron-Katz et al. 2016) have applied sliding-window dFC to acute-stress paradigms. Consistent themes:
- Stress increases the **dwell time** in high-salience-network states and decreases dwell time in high-CEN states.
- Stress reduces the **transition rate** between states — the brain becomes more "stuck" in one configuration.
- Individual differences in state repertoire at baseline predict vulnerability vs. resilience to the stressor.

### Research gap: traders specifically

There is, to our knowledge, **no published dFC study of active professional traders or portfolio managers**. The closest work is Lo & Repin 2002 (peripheral psychophysiology in 10 traders) and a scattered handful of lab paradigms using financial-decision tasks in naive subjects. This is a *research gap we should name explicitly in the deck*. The modal neuroscience-of-finance paper either (a) uses economics-student volunteers in a scanner, or (b) measures traders' skin-conductance on the floor. Neither touches large-scale network dynamics in the population we actually care about. An RQS collaboration that put a dozen PMs through a dFC paradigm under simulated drawdown would be genuinely novel.

## Biomarkers of brain state — what funds could measure tomorrow

The most actionable insight from the network-neuroscience layer is that **you do not need an fMRI**. The same noradrenergic switch that drives the salience-hijack has peripheral readouts that are now cheap, wearable, and continuous.

### Heart rate variability (HRV) — the prefrontal-vagal index

Thayer & Lane (2000, *J. Affective Disorders* 61:201-216) proposed the **neurovisceral integration model**: a distributed *central autonomic network* — including mPFC, insula, amygdala, hypothalamus, nucleus of the solitary tract, and vagal motor nuclei — links cognitive control to cardiac parasympathetic output. Activity in this network inhibits the heart via the vagus, producing high-frequency HRV (respiratory sinus arrhythmia, RMSSD, HF-HRV).

**Core claim:** HRV indexes the functional integrity of the prefrontal-vagal circuit that also supports emotion regulation and cognitive flexibility.

Thayer, Hansen, Saus-Rose & Johnsen (2009, *Annals of Behavioral Medicine* 37:141-153) reviewed evidence that resting HRV correlates with working-memory capacity, sustained attention, set-shifting, and inhibitory control. High HRV → better top-down regulation. Low HRV → rigidity, vigilance, threat-biased cognition.

Thayer, Åhs, Fredrikson, Sollers & Wager (2012, *Neuroscience & Biobehavioral Reviews* 36:747-756) performed a meta-analysis of neuroimaging-HRV studies and identified a convergent set of regions whose activity tracks HRV: ventromedial PFC, amygdala, right anterior insula. These are precisely the hubs that reconfigure under stress. HRV is a **window into salience-network ↔ executive-network balance** at the periphery.

**Field deployment.** RMSSD or HF-HRV from 2-5 minute resting recordings, or continuous 24-hr recordings, can be captured by consumer wearables — Whoop, Oura, Apple Watch Series 8+, Polar H10 chest straps, Garmin. Night-time HRV tracked day-over-day gives a robust trait-plus-state signal. Acute drops in morning HRV are a leading indicator that the individual is entering the trading day with weakened prefrontal-vagal control.

**Validated in trading populations?** Partially. Lo, Repin & Steenbarger (2005) found HRV-related autonomic reactivity correlated with trading P&L variance. Kandasamy et al. (2014) showed that interoceptive accuracy (closely linked to insula/HRV circuitry) predicted survival time on a London hedge fund floor. The specific *night-time HRV → next-day decision quality* link has not been rigorously tested in a professional trading sample — another research gap, and a tractable one.

### Pupillometry — the locus-coeruleus / noradrenergic readout

Joshi, Li, Kalwani & Gold (2016, *Neuron* 89:221-234) made simultaneous single-unit recordings from locus coeruleus, inferior and superior colliculus, and anterior/posterior cingulate in alert monkeys and showed that **pupil diameter tracks LC spiking on a second-by-second scale**. Luminance-independent pupil dilation is, in effect, a non-invasive LC readout.

Aston-Jones & Cohen (2005, *Annual Review of Neuroscience* 28:403-450) provided the theoretical frame: LC operates in two modes.
- **Phasic mode:** tightly locked to task-relevant events, narrow gain, exploitative (stay on task). Associated with small tonic pupil + large phasic dilations to task events.
- **Tonic mode:** sustained elevation, broad gain, exploratory (disengage from current task, scan). Associated with large tonic pupil + blunted phasic responses. Under acute stress, LC shifts toward tonic mode — the salience-hijack state.

**Field deployment.** Workstation webcam + open-source pupillometry (e.g., PyGaze, Pupil Labs open source) can estimate pupil diameter at 30 Hz with a consumer camera. Commercial eye-trackers (Tobii Pro Nano, Pupil Labs Neon glasses) do it more robustly. Pupil-derived arousal metrics — baseline pupil diameter (tonic LC) and task-evoked dilation amplitude (phasic LC) — are candidate real-time markers of the noradrenergic state the trader is trading in.

**Caveats.** Luminance, screen content, fatigue, caffeine, and medications (especially stimulants, SNRIs) all affect pupil. Any instrumentation has to baseline-correct on the individual and the display.

### Skin conductance / electrodermal activity (EDA)

The somatic-marker tradition (Damasio, Bechara, Tranel). EDA reflects pure sympathetic cholinergic drive to eccrine sweat glands — no parasympathetic component — so it is a cleaner sympathetic readout than HR. Lo & Repin 2002 (*Journal of Cognitive Neuroscience* 14:323-339) recorded EDA and blood volume pulse in 10 professional traders during live market events and found reliable autonomic reactivity to transient volatility — with experience-dependent differences in amplitude.

EDA is cheap (wrist strap), noisy (motion artifact), and correlates with but does not substitute for HRV or pupil. It is best as a confirmatory signal layered on top of HRV.

### Cortisol biomarkers

Three complementary sampling regimes:
- **Diurnal slope:** typical waking peak, decline through the day, low at bedtime. Flattening of the slope is a chronic-stress marker.
- **Cortisol Awakening Response (CAR):** the 30-50% rise in the first 30-45 min after waking. Elevated CAR under chronic pressure; blunted CAR in burnout / exhaustion.
- **Hair cortisol:** 1-3 cm of hair integrates cortisol over weeks-to-months of chronic exposure. The cleanest marker of chronic allostatic load.

All are now assayable from saliva or hair at ~$20-50 per sample. A monthly hair cortisol from the desk's top PMs would be a cheap, longitudinal measure of chronic load — and one that sidesteps the noise of acute salivary measurements.

### What has actually been validated in trading contexts

- Coates & Herbert (2008, *PNAS*): testosterone and cortisol on a London trading floor predicted next-day P&L and risk-taking. Cortisol spiked during high-vol weeks; the spike was *not adaptive* beyond a point.
- Kandasamy et al. (2014, *Sci. Reports*): chronic cortisol elevation in traders produced subjective risk-aversion shifts and would (if applied to market-making) push prices away from optimal.
- Lo & Repin (2002): peripheral psychophysiology during live trading.
- Lo, Repin & Steenbarger (2005): psychophysiological correlates of P&L.

**The literature is thinner than it should be.** There is no published 50-trader panel with synchronous continuous HRV, pupil, and market-event telemetry. This is another tractable research collaboration.

## Bridge to our empirical findings

The Capital Group experiments documented (a) compression of analyst time horizon under stress and (b) fight/flight signatures in PM decision-making. Both fit cleanly into the Hermans network-reconfiguration model.

**Analyst horizon compression (knowledge file 03).** Temporal discounting and horizon reasoning rely on dlPFC and the DMN — the dlPFC for working-memory and goal representation, the DMN for prospection and autobiographical simulation of future states. The Hermans 2011 reconfiguration *both weakens the dlPFC* (loss of the workspace that holds long-horizon representations) *and shifts the DMN toward vigilance* (loss of the simulation engine). The observable behavior — analysts collapsing a 3-year thesis onto a 3-week window under stress — is the expected output of this network state. This is not a cognitive error in the moral sense; it is the brain's correct response to a signal that the current moment is existentially important.

**PM fight/flight signatures (knowledge file 04).** The "fight" phenotype (doubling down, aggressive risk-taking) and "flight" phenotype (freezing, liquidating, going to cash) are both salience-dominant, CEN-depressed states. Arnsten 2015 showed the molecular switch from *reflective* to *reflexive* control is a catecholamine-driven shift in effective connectivity. Which direction an individual flips — fight vs. flight — is likely a function of trait-level resting network architecture (Seeley et al. 2007; Cole et al. 2013) plus endocrine milieu (testosterone / cortisol ratio, Coates & Herbert). The *bias amplification* we observed in PMs under stress is not random: it is the trait-locked direction each individual's network takes when the salience network takes over.

**Confidence miscalibration (knowledge files 01, 02).** Metacognitive confidence involves lateral-PFC and precuneus (DMN). Under salience-hijack, both are disrupted. Overconfidence in the tails is the expected behavior when the CEN (which would test the belief against evidence) is offline and the SN (which flags the belief as urgent) is hyperactive.

In short: **every behavioral finding we have is a downstream fingerprint of a single upstream event — the noradrenergic network reconfiguration.**

## Implications for instrumentation

If the bias is a downstream symptom of a neurobiological state, you can instrument the state and get ahead of the bias.

### Individual wearable layer (trader-facing)

A consumer wearable — Whoop, Oura, Apple Watch Ultra — continuously measures night HRV, resting HR, and respiratory rate. Combined with a morning CAR saliva or hair cortisol baseline, this gives a **24-hour updated physiological state vector** for each PM.

Concrete dashboard concept: a private, opt-in daily readiness score with three lights — green (baseline HRV + adequate sleep + morning cortisol in-band), amber, red. The PM sees only their own. Nothing is reported to management. The cultural frame is identical to an athlete's readiness score: not surveillance, but a self-awareness tool. Aligned incentives: the PM uses it to decide whether to size up, hold steady, or trim on a given morning.

### Workstation layer (decision-moment)

A workstation webcam running open-source pupillometry during known high-stakes decision windows (market open, FOMC, earnings prints) can timestamp acute arousal excursions. Not for real-time veto of trades — that is culturally infeasible and probably unwise — but as a **post-hoc log** correlated with trade outcomes and risk sizing. A PM who sees, over a quarter, that their largest drawdown trades sit in the top-decile pupil / lowest-decile HRV windows has evidence-based grounds to impose their own cooling-off rule.

### Institutional layer (RQS / risk-management)

Aggregated, anonymized physiological state across the desk is a *new risk factor*. On a day when half the desk is red-light, position-sizing limits could tighten automatically (analogous to VaR scaling to vol). This has obvious cultural and HR obstacles but is a straightforward extension of how firms already think about risk.

### Intervention layer

Network reconfiguration is reversible. Interventions that *restore prefrontal-vagal tone* have measurable effects:
- **Slow breathing** at ~6 breaths/min directly engages the parasympathetic brake and raises HRV within minutes. Well-validated. Effectively free.
- **Cold-water face immersion** (diving reflex) induces vagal surge; 30 seconds lowers HR and pushes HRV up.
- **Acute aerobic exercise** shifts noradrenaline kinetics and, crucially, consumes the physiological arousal so it does not manifest as trading behavior.
- **Sleep and circadian discipline** (covered in the chronobiology knowledge file) is the single most powerful long-run modulator of baseline HRV and morning cortisol.

A pre-open 3-minute slow-breathing protocol, measured on HRV, is the simplest possible intervention to prototype. The effect is real, the cost is zero, and the physiology is exactly what you want: a nudge of the prefrontal-vagal axis before the salience network is tested.

### Research layer

Two experiments, each genuinely novel:
1. **20-30 PMs, 3-month synchronous physiology panel.** Continuous HRV (Whoop), morning salivary cortisol weekly, hair cortisol monthly, opt-in workstation pupillometry. Correlate with trade-level P&L, risk, and post-hoc quality-of-decision ratings. No existing equivalent dataset exists in the literature.
2. **Pre/post breathing protocol RCT.** Randomize desks to a 3-min pre-open paced-breathing protocol vs. control for 8 weeks. Primary endpoint: pre-decided quality-of-decision composite (hit-rate, holding-period alignment with thesis). Secondary: HRV, pupil, subjective stress.

## Citations

Primary sources, in order of appearance:

- **Raichle et al. 2001.** A default mode of brain function. *PNAS* 98:676-682. https://www.pnas.org/doi/10.1073/pnas.98.2.676
- **Menon, V. 2011.** Large-scale brain networks and psychopathology: a unifying triple network model. *Trends in Cognitive Sciences* 15:483-506. https://pubmed.ncbi.nlm.nih.gov/21908230/
- **Seeley, W.W., Menon, V., Schatzberg, A.F., Keller, J., Glover, G.H., Kenna, H., Reiss, A.L., Greicius, M.D. 2007.** Dissociable intrinsic connectivity networks for salience processing and executive control. *Journal of Neuroscience* 27:2349-2356. https://www.jneurosci.org/content/27/9/2349
- **Cole, M.W., Reynolds, J.R., Power, J.D., Repovs, G., Anticevic, A., Braver, T.S. 2013.** Multi-task connectivity reveals flexible hubs for adaptive task control. *Nature Neuroscience* 16:1348-1355. https://www.nature.com/articles/nn.3470
- **Hermans, E.J., van Marle, H.J.F., Ossewaarde, L., Henckens, M.J.A.G., Qin, S., van Kesteren, M.T.R., Schoots, V.C., Cousijn, H., Rijpkema, M., Oostenveld, R., Fernández, G. 2011.** Stress-related noradrenergic activity prompts large-scale neural network reconfiguration. *Science* 334:1151-1153. https://www.science.org/doi/10.1126/science.1209603 (PubMed: https://pubmed.ncbi.nlm.nih.gov/22116887/)
- **Hermans, E.J., Henckens, M.J.A.G., Joëls, M., Fernández, G. 2014.** Dynamic adaptation of large-scale brain networks in response to acute stressors. *Trends in Neurosciences* 37:304-314. https://pubmed.ncbi.nlm.nih.gov/24766931/
- **van Oort, J., Tendolkar, I., Hermans, E.J., Mulders, P.C., Beckmann, C.F., Schene, A.H., Fernández, G., van Eijndhoven, P.F. 2017.** How the brain connects in response to acute stress: a review at the human brain systems level. *Neuroscience & Biobehavioral Reviews* 83:281-297. https://pubmed.ncbi.nlm.nih.gov/29074385/
- **Arnsten, A.F.T. 2015.** Stress weakens prefrontal networks: molecular insults to higher cognition. *Nature Neuroscience* 18:1376-1385. https://www.nature.com/articles/nn.4087
- **Hutchison, R.M., Womelsdorf, T., Allen, E.A., Bandettini, P.A., Calhoun, V.D., Corbetta, M., et al. 2013.** Dynamic functional connectivity: promise, issues, and interpretations. *NeuroImage* 80:360-378. https://pubmed.ncbi.nlm.nih.gov/23707587/
- **Allen, E.A., Damaraju, E., Plis, S.M., Erhardt, E.B., Eichele, T., Calhoun, V.D. 2014.** Tracking whole-brain connectivity dynamics in the resting state. *Cerebral Cortex* 24:663-676. https://pubmed.ncbi.nlm.nih.gov/23146964/
- **Thayer, J.F., Lane, R.D. 2000.** A model of neurovisceral integration in emotion regulation and dysregulation. *Journal of Affective Disorders* 61:201-216. https://pubmed.ncbi.nlm.nih.gov/11163422/
- **Thayer, J.F., Hansen, A.L., Saus-Rose, E., Johnsen, B.H. 2009.** Heart rate variability, prefrontal neural function, and cognitive performance: the neurovisceral integration perspective. *Annals of Behavioral Medicine* 37:141-153. https://pubmed.ncbi.nlm.nih.gov/19424767/
- **Thayer, J.F., Åhs, F., Fredrikson, M., Sollers, J.J., Wager, T.D. 2012.** A meta-analysis of heart rate variability and neuroimaging studies. *Neuroscience & Biobehavioral Reviews* 36:747-756. https://pubmed.ncbi.nlm.nih.gov/22178086/
- **Joshi, S., Li, Y., Kalwani, R.M., Gold, J.I. 2016.** Relationships between pupil diameter and neuronal activity in the locus coeruleus, colliculi, and cingulate cortex. *Neuron* 89:221-234. https://pubmed.ncbi.nlm.nih.gov/26711118/
- **Aston-Jones, G., Cohen, J.D. 2005.** An integrative theory of locus coeruleus-norepinephrine function: adaptive gain and optimal performance. *Annual Review of Neuroscience* 28:403-450. https://pubmed.ncbi.nlm.nih.gov/16022602/
- **Lo, A.W., Repin, D.V. 2002.** The psychophysiology of real-time financial risk processing. *Journal of Cognitive Neuroscience* 14:323-339. https://pubmed.ncbi.nlm.nih.gov/11970795/
- **Coates, J.M., Herbert, J. 2008.** Endogenous steroids and financial risk taking on a London trading floor. *PNAS* 105:6167-6172.
- **Kandasamy, N., Hardy, B., Page, L., Schaffner, M., Graggaber, J., Powlson, A.S., Fletcher, P.C., Gurnell, M., Coates, J. 2014.** Cortisol shifts financial risk preferences. *PNAS* 111:3608-3613.

## Candidate canonical graphs

Graphs the deck should include, with enough detail to have a chart engineer produce them. (All lines `tension: 0`, visible dots at each data point, no black ink per project style rule.)

1. **Triple-network schematic (DMN / SN / CEN).** Coronal and lateral brain views with the three networks color-blocked in three distinct theme colors. Arrows for the SN→DMN and SN→CEN switching function. Node labels: mPFC/PCC (DMN), AI/dACC (SN), dlPFC/PPC (CEN). Source: redraw Menon 2011 Fig. 1 / Seeley 2007 Fig. 2.

2. **Salience-hijack schematic (before/after acute stress).** Same three networks, two panels. Baseline: balanced. Acute stress: SN links thickened (↑connectivity), CEN links thinned (↓), subcortical tendrils (amygdala, hypothalamus, LC) thickened. Explicit arrow labeled "noradrenaline" from LC outward. Source: redraw Hermans 2011 Fig. 2 / Hermans 2014 Fig. 1.

3. **Time course of network reconfiguration.** X-axis: minutes from stressor onset, 0 → 120 minutes. Y-axis: relative activity/connectivity (arbitrary units, 0-100%). Four traces with visible dots every 5-10 min:
   - Noradrenaline / salience network (fast rise, peaks ~5-10 min, decays over 30-60 min)
   - Cortisol non-genomic (rise from ~10 min, peaks ~20-30 min)
   - Cortisol genomic / CEN rebound (slow rise, starts ~60 min, extends past 2 hr)
   - DMN (dip at onset, gradual recovery, overshoot late)
   Overlay investment-horizon labels: "5-min drawdown", "30-min window", "5-week drawdown." Source: adapt Hermans 2014 Fig. 2.

4. **HRV vs. decision-flexibility chart.** X-axis: resting HRV (e.g., ln(RMSSD) or HF-HRV, binned). Y-axis: performance on a behavioral flexibility proxy (set-shifting, working-memory, or in-house decision-quality metric). Scatter + fitted straight line (no curves). Cite Thayer et al. 2009; if an internal Capital Group equivalent exists, use that. Separate panel: HRV vs. bias-amplification from our experiments, if data permit.

5. **Pupil diameter as LC readout.** Two-panel. Left: simultaneous LC spike rate and pupil diameter over ~60 seconds (from Joshi 2016 Fig. 3); show the tight temporal locking. Right: tonic pupil diameter vs. task performance (inverted-U, Aston-Jones & Cohen 2005) — phasic/exploit region center, tonic/explore region right tail. Use visible dots across the curve.

6. **Biomarker-to-bias map.** Rows: our empirical findings (horizon compression, overconfidence, fight/flight, confidence miscalibration). Columns: noradrenergic state (↑/↓), CEN engagement (↑/↓), peripheral signature (HRV, pupil). Cells shaded consistently. This is the single "it all fits together" slide that ties this knowledge file to the behavioral-findings knowledge files.

7. **Wearable-instrumentation concept mockup.** Three vertical panels: trader-facing daily readiness (Whoop-style three-light), workstation pupillometry timeline overlaid on intraday P&L, desk-level aggregate risk-factor chart. Shown as illustrative — the deck explicitly notes no operational system exists yet at Capital Group.

8. **Research-gap map.** 2x2 grid. Axes: "population studied" (naive subjects ↔ professional decision-makers) × "measurement modality" (peripheral physiology ↔ network imaging). Populate with published studies. The upper-right quadrant — dFC in PMs — is empty. This is the space for a Capital Group / RQS collaboration.
