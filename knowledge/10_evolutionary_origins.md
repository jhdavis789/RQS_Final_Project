# Evolutionary Origins of Bias and Herding — Deep Research

## Executive one-liner
Overconfidence, loss aversion, herding, and short-horizon discounting are not cognitive bugs but adaptive design features selected under Pleistocene conditions — where contests had highly asymmetric payoffs, fitness was convex below a starvation threshold, social information was usually cheaper and more accurate than solo learning, and future rewards were so predation-contingent that a steep discount was the fitness-maximising response; the same machinery misfires in modern capital markets because asymmetries, thresholds, reference groups, and time horizons are now arbitrary features of institutional design rather than of the physical environment the machinery was built for, which is why the question for RQS is not "how do we remove the bias?" but "how do we engineer a decision process whose asymmetries align with, rather than trigger, the ancestral heuristic?"

---

## The adaptive overconfidence theorem — Johnson & Fowler 2011

### The puzzle
Classical rational-choice theory cannot explain the persistence of overconfidence. A Bayesian agent who systematically overestimates her own abilities or the probability her beliefs are correct should be outcompeted by a well-calibrated rival: she enters contests she cannot win, initiates wars she will lose, and invests in projects with negative expected value. The empirical record, however, is the opposite — overconfidence is cross-cultural, developmentally early, and persistently distributed across the population (Taylor & Brown 1988; Moore & Healy 2008). The evolutionary question is how selection could have maintained a trait whose first-order prediction is that it destroys fitness.

Dominic Johnson (University of Edinburgh, then Oxford) and James Fowler (UC San Diego) answered this with a formal population-dynamics model published as Johnson & Fowler 2011, "The evolution of overconfidence," *Nature* 477:317–320. The paper is short (four pages plus supplement), unusual for *Nature* in a theoretical-only contribution, and it is the single most-important piece in the evolutionary-finance literature for understanding why smart professionals overstate their own edge.

### The model
Consider a population of agents who repeatedly contest resources. Each agent has:

- A **true capability** c, drawn from some distribution across the population.
- A **self-assessment** ĉ = c + ε, where ε is a perception error with mean μ (the "confidence bias") and variance σ² (the uncertainty in self-knowledge). μ > 0 is overconfidence, μ < 0 is underconfidence, μ = 0 is unbiased self-assessment.
- A **claim strategy**: when matched with an opponent, the agent claims the resource if she perceives her own capability to exceed the opponent's. If both claim, they fight; if one claims and the other yields, the claimant gets the resource; if both yield, they walk away.

Three payoffs define the game:
- **r** — the fitness value of the contested resource.
- **c\_fight** — the fitness cost of a lost contest (injury, energy, time).
- **c\_miss** — the opportunity cost of yielding a contest one could have won.

The key variable is the **asymmetry ratio r / c\_fight**. When resources are valuable relative to fighting costs, contesting pays even at low win-probability; when contests are cheap relative to the prize, claiming is better than yielding even under uncertainty about relative strength.

### The result
Johnson & Fowler solve for the evolutionarily stable strategy (ESS) as a function of three parameters: the payoff ratio r / c\_fight, the self-assessment noise σ², and the population distribution of capability. Their central finding is that the ESS confidence bias μ\* is **strictly positive** whenever:

> 2r > c\_fight + something-scaling-with-σ²

In plain language: overconfidence is the ESS whenever (a) the prize is at least half the cost of a lost fight and (b) self-assessment is noisy. The greater the noise, the greater the optimal bias. As σ² → 0 (perfect self-knowledge), μ\* → 0 (no bias needed). As r / c\_fight → ∞, μ\* grows without bound.

The intuition: if you cannot tell exactly how strong you are, and losing a contest is not catastrophic relative to winning, you maximise expected fitness by systematically *over-claiming* — because the errors of under-claiming (yielding to an opponent you could have beaten) are worse in expectation than the errors of over-claiming (fighting an opponent you could not beat). Overconfidence is a **decision bias that corrects for perception noise under asymmetric payoffs**. It is not an error; it is a pre-computed response to a systematic error structure in the environment.

The *Nature* supplement extends the result in three directions:
1. **Population invasion analysis** — an unbiased (μ = 0) mutant invading a μ\* > 0 resident loses; a μ\* > 0 mutant invading a μ = 0 resident wins. The overconfident strategy is both an ESS and convergence-stable.
2. **Effect of coalition and reputation** — in repeated contests with information leakage, μ\* declines because opponents learn. This predicts that overconfidence is highest in environments of *low repeat interaction* — exactly the modern capital-markets environment.
3. **Collective-action / war applications** — the same math explains why nations initiate conflicts they then lose, and why pre-war confidence estimates on both sides systematically exceed the post-war reality.

### Why it matters for investment decision-making
Capital markets have the exact parameter configuration that maximises μ\*:
- **Payoff asymmetry**: a successful trade can yield multiples of the loss; career upside from a few big wins exceeds the career downside from many small losses (convex compensation structures).
- **Perception noise**: skill attribution from outcomes is fundamentally noisy — Fama & French Type II sampling error swamps the signal over any career-length horizon.
- **Low repeat interaction**: counterparties rotate; specific bets don't usually come back.

This is why the baseline expectation for RQS is **not** that our analysts and PMs are miscalibrated despite training, but that they are miscalibrated *because the selection environment that shaped their cognitive architecture rewarded exactly this miscalibration*. Johnson & Fowler's result is the rigorous version of Kahneman's "overconfidence is the engine that drives capitalism" remark — it names the math.

### Related signalling literature
Zahavi's **handicap principle** (Zahavi 1975 *J Theor Biol*, extended Zahavi & Zahavi 1997 *The Handicap Principle*) supplies a complementary mechanism: costly signals are credible precisely because they are costly. A peacock's tail, a gazelle's stot, a trader's conspicuous risk-taking — each is harder to fake for a low-quality signaller. Spence's **job-market signalling model** (Spence 1973 *QJE*) is the economic analogue: education functions as a separating equilibrium because it is differentially costly to high- vs low-productivity types. Bénabou & Tirole 2002 ("Self-confidence and personal motivation," *QJE*) and 2016 ("Mindful economics," *JEP*) extend this to **intrapersonal** signalling: self-deception is a commitment device — if you *believe* you are strong, you signal credibly in external contests, because strategic signalling is more resource-costly than genuine belief. Robert Trivers's *The Folly of Fools* (2011) popularises the thesis that self-deception evolved because it is easier to deceive others when you don't know you are lying.

The implication is doubled: overconfidence is both an ESS under noise (Johnson–Fowler) *and* an enabling technology for costly signalling (Zahavi/Spence/Trivers). The two mechanisms compound. This is why the bias is robust to conscious awareness — knowing you are overconfident does not neutralise the environmental selection that favours it.

---

## Loss aversion as ancestral fitness asymmetry

Kahneman & Tversky's 1979 *Econometrica* prospect-theory paper established loss aversion empirically: losses loom approximately 2× to 2.5× gains in stated preference. The Nobel-recognised finding was psychological, not evolutionary — *why* humans weight losses asymmetrically was left open.

McDermott, Fowler & Smirnov 2008, "On the evolutionary origin of prospect theory preferences" (*Journal of Politics* 70:335–350) supplies the missing ecology. Their model considers an agent with fitness-relevant resource level x whose survival probability is a **concave, threshold-bearing** function of x. Below the starvation threshold, marginal resource has very high fitness value — every additional calorie matters greatly because it shifts survival probability steeply. Well above the threshold, marginal resource has low fitness value — additional calories translate to diminishing reproductive returns once basic needs are met.

The mathematical consequence: expected-fitness maximisation over this concave-with-threshold function produces exactly the S-shaped value function of prospect theory — **concave over gains, convex over losses, steeper over losses than over gains**. The coefficient of loss aversion that maximises fitness in their simulations is approximately 2 — the same value Kahneman & Tversky estimated from undergraduates. The match is quantitative, not just qualitative.

Rayo & Becker 2007, "Evolutionary efficiency and happiness" (*JPE* 115:302–337) reach a parallel conclusion from a different direction: a reference-dependent utility function is *evolutionarily efficient* because it uses a fixed neural range to encode an open-ended resource axis. The organism's brain has bounded firing rates; coding absolute rather than relative resource levels would quickly saturate. Reference-dependence is the compression algorithm.

Stephens & Krebs (1986 *Foraging Theory*, Princeton) anchor the older behavioural-ecology version: foragers systematically **prefer fixed over variable payoffs when above the resource threshold** (risk-averse in gains) and **prefer variable over fixed payoffs when below** (risk-seeking in losses). Caraco, Martindale & Whittam 1980 *Animal Behaviour* demonstrated this directly in yellow-eyed juncos — birds tested under energy-positive conditions preferred the fixed-reward feeder; the same birds tested under energy-negative conditions preferred the variable-reward feeder. The prospect-theory value function is visible in sparrows.

### Why it matters for markets
The modern environment violates the ancestral structure in two ways:
1. **No threshold.** A 20% drawdown in a diversified portfolio does not cross any biological fitness threshold for a well-compensated investment professional. Yet the cognitive machinery responds as if it does, because the machinery can't re-set the threshold.
2. **Misaligned reference point.** The reference point is set by recent peaks, benchmark performance, or career P&L — none of which correspond to survival margins. Loss aversion relative to these arbitrary reference points reproduces the fitness-defence response in contexts where the fitness consequence is zero.

The design implication: a decision process that computes gains and losses relative to **long-horizon fundamental value** (which has no behavioural weight) rather than **recent marks** (which trigger the ancestral response) is engineering *around* the heuristic. This is the quantitative basis for our pre-commitment and horizon-controlling debiasing recommendations.

---

## Information cascades and herding — Banerjee, Bikhchandani-Hirshleifer-Welch

Conformist transmission — copying the most common behaviour among peers — was shown by Boyd & Richerson (*Culture and the Evolutionary Process* 1985; *The Origin and Evolution of Cultures* 2005) to be the adaptively optimal strategy whenever individual learning is costly and the environment is correlated in time. If the world changes slowly enough that yesterday's good answer is usually still good, and individual exploration is expensive, then copying is a superior strategy in expected fitness. The formal models (Boyd & Richerson 1995 *Ethology and Sociobiology* 16:125–143; Henrich & Boyd 1998) show that **conformist bias is an ESS under a wide range of environmental variability** — specifically, when the cost of individual learning exceeds the expected payoff difference between populations with and without imitation.

The finance analogue was derived independently. **Banerjee 1992**, "A simple model of herd behavior" (*Quarterly Journal of Economics* 107:797–817), constructs a sequential-decision game where agents receive private signals and observe predecessors' actions. The result: even with fully rational Bayesian updating, agents rationally discard their private information once a consensus has formed, because the public information embedded in predecessors' actions overwhelms their individual private signal. Herding emerges endogenously from rationality, not from irrationality.

**Bikhchandani, Hirshleifer & Welch 1992**, "A theory of fads, fashion, custom, and cultural change as informational cascades" (*Journal of Political Economy* 100:992–1026) generalises. An **information cascade** forms when an agent, observing others' actions, rationally ignores her own private information because the action-inferred public belief is stronger. Key properties:
- **Cascade formation is rapid.** After just two consistent signals (or three, depending on prior), rational agents begin to imitate regardless of their own signal.
- **Cascades are fragile.** The information aggregated in the cascade is only the first two or three private signals. A single public news shock can shift the entire cascade to the opposite equilibrium.
- **Cascades aggregate little private information.** Because followers discard their signals, a 10,000-person cascade contains no more private information than the first three agents.

This is the rationality-preserving micro-foundation for bubbles and crashes. Prices can move far from fundamentals *without* irrational agents — all it takes is sequential decision-making under private signals with public observability. The 2016 Bikhchandani, Hirshleifer, Tamuz & Welch survey ("Information Cascades and Social Learning," NBER w21295) is the updated comprehensive treatment.

### The primate and collective-movement evidence
Collective movement in fish schools, bird flocks, and primate troops follows the same information-pooling logic. Couzin et al. 2005 *Nature* 433:513–516 ("Effective leadership and decision-making in animal groups on the move") showed that a small fraction of informed individuals can lead a much larger group by simple local-interaction rules. Pillot et al. 2011 *PLOS ONE* extended this to sheep — collective heading is driven by a minority of informed leaders with the rest following via local alignment rules, identical in formal structure to Vicsek-model self-propelled particles.

Conradt & Roper 2003 *Nature* 421:155–158 ("Group decision-making in animals") formalises the fitness trade-off: democratic (consensus) decisions are generally better-calibrated than despotic (follow-a-leader) decisions because they aggregate more information — *provided* followers retain their private signals. Cascades collapse this benefit: when followers discard their signals, the group's information-aggregation capacity collapses to the first mover's.

### Herd behaviour in markets
Sias 2004 *RFS* (covered in more detail in 05_market_psychology.md) shows quarter-to-quarter cross-sectional correlation in institutional demand of 0.4+, not explained by momentum. The most parsimonious interpretation is **information cascades over peer trades**: institutions infer information from other institutions' moves, weight it heavily because institutions are presumed informed, and discard their own private signals when the peer evidence is strong. This is the Banerjee–BHW mechanism running in real time across 13F reports.

The evolutionary framing: we are descended from primates for whom following the troop's movement was nearly always safer than striking out alone. The prior that the group knows something you don't was selected so hard that it now fires in contexts — like the consensus credit-spread position — where the prior is no longer warranted because the consensus is itself the aggregate of the same prior running in your peers.

---

## Hirshleifer's evolutionary-finance program

David Hirshleifer's research program is the most complete synthesis of evolutionary psychology and asset pricing. The anchor papers:

- **Hirshleifer 2001**, "Investor psychology and asset pricing" (*J. Finance* 56:1533–1597). 60-page survey. Organises the behavioural-finance literature around underlying psychology and proposes a framework of four distortion categories: heuristic simplification, self-deception, emotion-based, and social interaction. It is the roadmap for the subsequent two decades.

- **Hirshleifer & Teoh 2003**, "Herd behaviour and cascades in capital markets: a review and synthesis" (*European Financial Management* 9:25–66). Taxonomises herding into information-cascade, reputational, compensation-based, and investigative types, and provides empirical signatures distinguishing them.

- **Hirshleifer 2020**, "Presidential address: Social transmission bias in economics and finance" (*Journal of Finance* 75:1779–1831). The most recent and most important. Hirshleifer argues that economic ideas, beliefs, and trading strategies **propagate through social networks** with transmission bias — some ideas are more transmissible than others regardless of their truth. Transmission-favoured ideas (vivid, narrative, low-cognitive-cost, socially useful to repeat) accumulate; transmission-disfavoured ideas (abstract, probabilistic, hedged) decay. Market prices thus reflect not the aggregate of private information but the aggregate of the **most-transmitted subset** of private information.

This is Richard Dawkins's *memetics* applied to asset pricing. The testable predictions are distinctive:
- Stocks with simple, vivid narratives trade at persistent premia.
- Short theses spread more slowly than long theses (people tell their friends about stocks they own, not stocks they shorted).
- Social-media and earnings-call prominence causally affects prices beyond their information content.

Empirical tests (Hirshleifer, Peng & Wang 2023, "Social transmission bias and investor behaviour," *Review of Financial Studies*) confirm these predictions in retail-investor networks. The Jennifer Eberhardt–adjacent work on visual prominence and the DeVault–Shiller narrative economics program (Shiller 2019 *Narrative Economics*) converge on the same conclusion from parallel directions.

### What the evolutionary-finance program predicts differently
The classical rational-expectations view predicts that mispricing is transient, because arbitrageurs eliminate it. The naive behavioural view predicts that mispricing exists because investors are irrational. The evolutionary-finance view predicts that mispricing is **persistent, structured, and patterned by the selection environment of the ideas themselves**. Specifically, it predicts:

1. Mispricing will cluster around stocks whose narratives have high transmission fitness (vivid, simple, recent salient outcome).
2. Professional and retail traders will make systematically correlated mistakes because their information diet is filtered through the same transmission network.
3. Debiasing at the individual level will be insufficient, because the source of the bias is the idea ecosystem, not the individual mind.

For RQS specifically, the third prediction is the hardest. It means that even a perfectly calibrated analyst, embedded in a transmission-biased idea ecosystem, will systematically receive more signal about the narrative-rich trades than the narrative-poor ones. The debiasing lever cannot be the analyst's mind alone; it has to include the idea-sourcing process.

---

## The stress-response mismatch — Sapolsky frame

Robert Sapolsky's *Why Zebras Don't Get Ulcers* (1994, rev. 2004) is the canonical popular synthesis. The core biological frame: the vertebrate stress response — catecholamine and cortisol release, sympathetic activation, suppression of digestion and reproduction, mobilisation of glucose — is exquisitely adapted to **acute, physical, time-limited** threats. A lion charges, you run for 90 seconds, the threat resolves, the HPA axis returns to baseline. The system is built for this.

The modern mismatch is that the *same* system fires for **chronic, psychosocial, open-ended** threats. A quarterly drawdown does not resolve in 90 seconds. A career-risk exposure persists for years. The HPA axis, activated by the ancestral circuit, does not receive a termination signal. Sustained cortisol elevation produces the ulcer, the hippocampal atrophy, the immune suppression, and — relevantly for our purposes — the prefrontal-cortex attenuation documented in Arnsten 2009 *Nat Rev Neurosci* (covered in 04_fight_flight.md).

The specifically **financial-market** misfires:
1. **Drawdown as resource loss.** A portfolio drawdown pattern-matches to ancestral resource loss — starvation margin, status margin, territory loss. The amygdala fires as though the loss is life-threatening, because in ancestral environments a 20% resource loss often was.
2. **Ambiguous losers' signals.** Financial losses are slow, ambiguous, and recoverable. The stress system requires a clear termination signal to disengage. Markets rarely provide it.
3. **Reputational threat.** Career risk from a lost trade maps to social-status loss in ancestral hierarchies — a fitness-relevant loss historically (Sapolsky's own baboon work). The response is the same even though the modern fitness stakes are near zero.

Sapolsky's own primate-field work — 30+ years tracking a Kenyan olive-baboon troop — established the **social gradient of stress**: subordinate males in stable hierarchies have chronically elevated cortisol; dominant males have acute peaks but lower chronic baselines. Translate this to a hedge-fund floor: senior PMs show the acute-peak pattern (resolved by trade outcomes); junior analysts and mid-tier portfolio managers who cannot close out their exposures show the chronic-elevation pattern. The empirical endocrine data (Coates & Herbert 2008 *PNAS*, covered in 04_fight_flight.md) match.

The design implication: a process that provides **clear closure signals** (post-mortem, narrative integration, formal re-basing) allows the stress response to terminate. A process that leaves positions open-ended under peer surveillance and benchmark tracking sustains the stress response indefinitely, with predictable cognitive consequences.

---

## Time discounting and foraging theory

Rosati, Stevens, Hare & Hauser 2007 *Current Biology* compared intertemporal choice in chimpanzees, bonobos, and humans: chimps waited up to 2 minutes for larger rewards; humans rarely waited more than a few seconds. The behavioural-ecology explanation begins with Stephens & Krebs 1986 *Foraging Theory*: when future rewards are contingent on **survival to the payoff date**, and survival probability per unit time is p, the fitness-optimal discount rate is approximately the mortality rate m. In a Pleistocene environment with high predation, high infant mortality, high conspecific conflict, m is high — so optimal discount rates are high.

Sozou 1998 *Proc. R. Soc. B* 265:2015–2020 extended this to **uncertain hazards**: when the discount rate itself is uncertain (predator density is unknown), the optimal discount function is **hyperbolic**, not exponential. This is the fitness-origin of the empirical hyperbolic discounting pattern documented by Ainslie, Laibson, and others. Hyperbolic discounting is not a cognitive failure; it is the correct Bayesian response to *unknown* mortality risk.

The finance misfire: modern long-horizon investing is **evolutionarily novel**. There is no Pleistocene analogue to a 30-year liability-matching problem or a multi-generation endowment. The decision architecture that works for "should I eat this berry now or save it for later" does not generalise to "should I overweight long-duration bonds for a pension plan whose beneficiaries are not yet born." The cognitive machinery can be trained to attempt it, but the training is fighting a gradient.

The design implication: **pre-commitment devices** (Ulysses contracts, automatic rebalancing, mandatory hold periods) are the analogue of Odysseus binding himself to the mast. They work by preventing the present self from exercising the hyperbolic-discount temptation at the moment the hyperbolic-discount function peaks. They are not "debiasing"; they are **engineering around** the unchangeable heuristic.

---

## Sex differences — Trivers parental-investment background

Robert Trivers's 1972 paper ("Parental investment and sexual selection," in Campbell ed. *Sexual Selection and the Descent of Man 1871–1971*) is the framework. The sex with the higher minimum parental investment (females, in most mammals) becomes the limiting reproductive resource; the lower-investing sex (males) competes for access. Intrasexual competition in males — fighting, display, resource accumulation — is the consequence.

Daly & Wilson 1985 *Ethology and Sociobiology* and 1988 *Homicide* documented the **young-male syndrome**: risk-taking, contest, and violence peak in males aged 15–30 — exactly the age range of maximum reproductive competition. The extension to financial risk-taking (Byrnes, Miller & Schafer 1999 meta-analysis *Psychol. Bull.* 125:367–383; Charness & Gneezy 2012 *J. Econ. Behav. Organ.*) shows that males take more financial risk than females, with the gap largest in young adulthood and shrinking with age. The effect is small-to-moderate (d ≈ 0.2–0.3 for most domains) and the within-sex distribution overlaps heavily between sexes — but the central tendencies are robust.

Coates, Gurnell & Sarnyai 2010 ("From molecule to market: steroid hormones and financial risk-taking") make the endocrine argument: prenatal testosterone exposure (measured via 2D:4D digit ratio) correlates with financial risk-taking in adult trader populations. This is covered in detail in 04_fight_flight.md; the evolutionary point here is that the same testosterone signalling system that drives intrasexual competition in ancestral environments drives position-sizing variability in modern ones.

The costly-signalling reframe: male risk-taking is, in part, an ancestral mate-quality signal — "I can bear this risk, you should pair with me." The trading floor is an incidental modern context where the display machinery runs, and the display is not in fact calibrated to the audience (capital allocators, not mates).

---

## Dishonest signalling — Krebs, Dawkins, and market manipulation

Krebs & Dawkins 1984, "Animal signals: mind-reading and manipulation" (in Krebs & Davies eds. *Behavioural Ecology: an evolutionary approach*, 2nd ed.) argue that signals in nature are better understood as **manipulation** — the signaller attempts to alter the receiver's behaviour in the signaller's favour — than as cooperative information transfer. An arms race between manipulation (by signallers) and mind-reading (by receivers) drives the evolution of both sides.

Honest signalling is possible only when it is **cheaper for honest signallers than for dishonest signallers** (the Zahavi/Spence condition) or when the interests of signaller and receiver align. Neither condition holds generically in financial markets. Companies selectively disclose; sell-side research has compensation-structure incentives; corporate language is drafted by lawyers optimising for litigation defence; SPAC sponsors, crypto founders, and meme-stock promoters are explicit manipulators. Krebs & Dawkins predict this as the evolutionary baseline for any communication system without strong honesty-enforcement mechanisms.

The practical implication for RQS: a research process designed as if signals were cooperative information transfer — read the 10-K, take management's word, weight sell-side estimates at face value — is adapted to the wrong ecology. The correct prior is *Krebs-and-Dawkins manipulation*, with the research process calibrated accordingly. Loughran & McDonald's uncertainty-dictionary work, forensic-accounting techniques, and adversarial-prompting of LLM analysis tools are all operationalisations of this prior.

---

## Heuristics-and-biases vs. ecological-rationality — Kahneman / Gigerenzer

The sharpest intellectual tension in the evolutionary-cognition literature is between two programs:

- **Heuristics-and-biases (Kahneman, Tversky, Thaler, Ariely).** Heuristics are cognitive shortcuts that, while useful on average, produce systematic, predictable errors in well-defined conditions. The research agenda is to document the errors, map the conditions, and design corrective interventions (debiasing, nudges).

- **Ecological rationality (Gigerenzer, Todd, ABC Group).** Heuristics are *adapted tools for specific environmental structures*. When the environment matches the heuristic's design conditions, the heuristic can **outperform** statistical optimisation — because it has lower variance and exploits environmental regularities that the optimiser treats as noise. The research agenda is to catalogue the environmental structures ("ecological niches") in which specific heuristics dominate (Gigerenzer & Todd 1999 *Simple Heuristics That Make Us Smart*; Gigerenzer, Hertwig & Pachur 2011 *Heuristics: The Foundations of Adaptive Behavior*).

The famous Gigerenzer result (Goldstein & Gigerenzer 2002 *Psychol. Rev.* 109:75–90): in the "which German city is larger?" task, the **recognition heuristic** (pick the one you recognise) outperforms knowledge-based inference by American undergraduates — and outperforms linear regression when the recognition validity is high. This is the **less-is-more effect**: more information can produce worse decisions because it introduces variance the heuristic would have filtered out.

The apparent contradiction with Kahneman is substantive but less deep than it appears. Both sides agree:
1. Heuristics are adapted tools.
2. Heuristics produce systematic errors outside their design environment.
3. The question is which environments are which.

They disagree on:
1. **Relative weights.** Kahneman emphasises the error cases (because they are the surprising part); Gigerenzer emphasises the competence cases (because they are under-recognised).
2. **Design implication.** Kahneman's program suggests debiasing interventions; Gigerenzer's suggests environment-structuring — "fix the ecology so the heuristic fits."

For investment decision-making the resolution is **domain-dependent**. Where the environment has the ancestral structure (asymmetric payoffs, noisy self-assessment, low repeat play — i.e. a competitive contest), overconfidence heuristics are close to optimal. Where the environment violates the ancestral structure (long-horizon, Gaussian-tail returns, strong feedback, clear mortality of specific bets), the same heuristics produce large errors. The RQS question is not "Kahneman or Gigerenzer?" — it is "which specific decision is in which ecology?" Categorising decisions by their ecological match is itself the design intervention.

Gerd Gigerenzer's own extension to markets (*Risk Savvy* 2014; Gigerenzer 2018 *Handbook of Financial Decision Making*) argues that **1/N (equal-weighting) portfolio allocation often beats Markowitz mean-variance optimisation out-of-sample** — because Markowitz requires estimating the covariance matrix, and the estimation error exceeds the theoretical gain from optimisation (DeMiguel, Garlappi & Uppal 2009 *RFS* 22:1915–1953 documented this empirically). This is a concrete case where a heuristic — do the simple thing, don't over-fit — outperforms a sophisticated rational model. It is evidence for Gigerenzer's program, and it is directly relevant to a quantitative-services audience that builds optimisers for a living.

---

## Counterpoints and limits

The evolutionary-psychology program is not uncontested. Gould & Lewontin 1979, "The spandrels of San Marco and the Panglossian paradigm: a critique of the adaptationist programme" (*Proc. R. Soc. B* 205:581–598) is the canonical critique. Their argument: many traits that adaptationists "explain" as adaptations are in fact **spandrels** — by-products of other adaptations or of structural constraints. A post-hoc adaptive story can be constructed for nearly any trait; the story's plausibility is no evidence it is correct. This is the "just-so story" critique.

Applied to behavioural finance, the critique is that "overconfidence evolved because of asymmetric-payoff contests" is a narrative that *could* be true but is not uniquely supported by the data. Alternative non-adaptive explanations — neural-architecture limits, developmental noise, cultural transmission, by-products of other (adapted) systems like self-reinforcing motivation — remain live hypotheses. The Johnson-Fowler result is a rare case where a formal model and comparative evidence narrow the space; most evolutionary-finance stories are considerably softer.

The defensible position is:
1. Take the **formal-model results** (Johnson-Fowler, McDermott-Fowler-Smirnov, Sozou hyperbolic-from-uncertain-hazards, Boyd-Richerson conformist-transmission) seriously — they are ESS results under stated assumptions, not narratives.
2. Take the **empirical-convergence results** (prospect-theory in sparrows, stress-response homology across vertebrates, cascade behaviour in primates) seriously — they are data, not stories.
3. Remain sceptical of purely narrative "the reason X evolved is Y" claims without formal or comparative support.

This is the honest version of the evolutionary-finance case, and it is the version the RQS audience — who spot storytelling as a professional reflex — will accept.

---

## Modern-market mismatch — practical takeaway

The mismatch has five components, each with a corresponding process lever.

| Ancestral condition | Adaptive response | Modern mismatch | Process lever |
|---|---|---|---|
| Asymmetric payoff, noisy self-assessment | Overconfidence (Johnson-Fowler) | Symmetric career-long P&L tracking; noise-vs-skill nearly indistinguishable | Percentile-within-analyst normalisation; force pre-commitment probability statements |
| Fitness threshold below starvation | Loss aversion (McDermott et al.) | Arbitrary reference points (recent peak, benchmark) trigger full threshold response | Anchor valuations to long-horizon fundamentals; suppress daily mark salience |
| Costly individual learning, correlated environment | Conformist transmission (Boyd-Richerson) | Correlation of peers' information drops below the cost-of-independent-analysis threshold | Institutional incentives for dissenting research; red-team processes |
| High, uncertain predation hazard | Steep and hyperbolic discounting | Long-horizon investing is novel; no hazard maps to quarterly marks | Pre-commitment, rebalancing, mandatory hold periods |
| Clear threat-resolution signals | Acute-stress activation with termination | Open-ended exposures produce chronic-stress pattern | Formal post-mortem and closure processes; position-level forced decision deadlines |

The overarching principle: **do not fight the heuristic; engineer the ecology.** If the ancestral machinery fires under asymmetric payoffs, remove or normalise the asymmetries. If it fires below a reference threshold, move the reference point to a place where the response is not counter-productive. If it fires on peer alignment, institutionalise dissent. This is Gigerenzer's insight operationalised for capital markets — and it is the most practically tractable version of the evolutionary-finance program.

---

## Bridge to our empirical findings

Our analyst and PM confidence data — per-analyst normalised, stress-responsive, and career-stage-dependent — is the *direct footprint* of the five mechanisms above:

1. **Systematic overconfidence across our analyst population** is the Johnson-Fowler prediction, not a selection failure in our hiring or training. The baseline rate of overprecision in our 10-K write-ups should be > 50th-percentile among professionals because the selection environment that shaped our analysts — competitive academic and professional contests — *rewarded* the bias. Debiasing will work at the margin; elimination is not the realistic target.

2. **Per-analyst stable confidence-style trait** (Hyland hedging / booster ratio, heritability estimates from Cesarini et al. 2009 — covered in 01_metacognition_confidence.md) matches the trait-structured persistence predicted by Boyd-Richerson gene-culture coevolution: individuals inherit **confidence-coding style** from their parents and early cultural environment, and the style remains stable within person across career.

3. **Stress-responsive horizon compression** (covered in 03_stress_horizon.md) is the acute-stress response firing on financial-threat stimuli. Our finding that written-text time-horizon markers shorten under drawdown conditions is the Sozou-hyperbolic-from-hazard prediction in text form.

4. **Correlated error structure across analysts** is Hirshleifer social-transmission bias. The analysts are drawing from a shared idea ecosystem; their errors cluster on narrative-rich trades regardless of their individual metacognitive skill. Individual debiasing cannot break this; idea-sourcing redesign can.

5. **Career-stage effects on confidence** — junior analysts more hedged, mid-career more boosterish, senior more calibrated — fit both Trivers/young-male risk-display (mid-career as display phase) and Sapolsky's hierarchy-effects (subordinate chronic-stress hedging). The two effects are not distinguishable with our current data; flagging this as an open empirical question is more honest than choosing one.

The integrative claim for the presentation: the biases are not failures to be fixed; they are **adaptations running in the wrong ecology**. The RQS design mandate is to construct institutional ecologies in which the adaptations work, and to flag, gate, and pre-commit around the decisions in which the ecologies cannot be changed. This is the evolutionary-finance framing of the risk-management problem — and it is the framing that treats analysts and PMs as functioning optimisers of a different objective, not as defective optimisers of ours.

---

## Citations

**Overconfidence and its evolution**
- Johnson DDP & Fowler JH (2011). The evolution of overconfidence. *Nature* 477:317–320. https://www.nature.com/articles/nature10384
- Bénabou R & Tirole J (2002). Self-confidence and personal motivation. *Quarterly Journal of Economics* 117:871–915.
- Bénabou R & Tirole J (2016). Mindful economics: the production, consumption, and value of beliefs. *Journal of Economic Perspectives* 30(3):141–164.
- Compton J (2007). Ego-defensive deception, self-deception and resistance. *American Communication Journal* 9(4).
- Trivers R (2011). *The Folly of Fools: The Logic of Deceit and Self-Deception in Human Life*. Basic Books.
- Zahavi A (1975). Mate selection — a selection for a handicap. *Journal of Theoretical Biology* 53:205–214.
- Zahavi A & Zahavi A (1997). *The Handicap Principle*. Oxford UP.
- Spence M (1973). Job market signaling. *Quarterly Journal of Economics* 87:355–374.

**Loss aversion and reference-dependence**
- Kahneman D & Tversky A (1979). Prospect theory: an analysis of decision under risk. *Econometrica* 47:263–292.
- McDermott R, Fowler JH & Smirnov O (2008). On the evolutionary origin of prospect theory preferences. *Journal of Politics* 70:335–350.
- Rayo L & Becker GS (2007). Evolutionary efficiency and happiness. *Journal of Political Economy* 115:302–337.
- Caraco T, Martindale S & Whittam TS (1980). An empirical demonstration of risk-sensitive foraging preferences. *Animal Behaviour* 28:820–830.
- Stephens DW & Krebs JR (1986). *Foraging Theory*. Princeton UP.

**Herding, cascades, cultural transmission**
- Banerjee AV (1992). A simple model of herd behavior. *Quarterly Journal of Economics* 107:797–817.
- Bikhchandani S, Hirshleifer D & Welch I (1992). A theory of fads, fashion, custom, and cultural change as informational cascades. *Journal of Political Economy* 100:992–1026.
- Bikhchandani S, Hirshleifer D, Tamuz O & Welch I (2024). Information cascades and social learning. NBER w28887; *Journal of Economic Literature* forthcoming.
- Boyd R & Richerson PJ (1985). *Culture and the Evolutionary Process*. Chicago UP.
- Boyd R & Richerson PJ (2005). *The Origin and Evolution of Cultures*. Oxford UP.
- Henrich J & Boyd R (1998). The evolution of conformist transmission and the emergence of between-group differences. *Evolution and Human Behavior* 19:215–241.
- Couzin ID, Krause J, Franks NR & Levin SA (2005). Effective leadership and decision-making in animal groups on the move. *Nature* 433:513–516.
- Conradt L & Roper TJ (2003). Group decision-making in animals. *Nature* 421:155–158.
- Pillot M-H, Gautrais J, Arrufat P, Couzin ID, Bon R, Deneubourg J-L (2011). Scalable rules for coherent group motion in a gregarious vertebrate. *PLOS ONE* 6:e14487.
- Scharfstein DS & Stein JC (1990). Herd behavior and investment. *American Economic Review* 80:465–479.
- Sias RW (2004). Institutional herding. *Review of Financial Studies* 17:165–206.

**Evolutionary finance / social transmission**
- Hirshleifer D (2001). Investor psychology and asset pricing. *Journal of Finance* 56:1533–1597.
- Hirshleifer D & Teoh SH (2003). Herd behaviour and cascades in capital markets: a review and synthesis. *European Financial Management* 9:25–66.
- Hirshleifer D (2020). Presidential address: social transmission bias in economics and finance. *Journal of Finance* 75:1779–1831.
- Hirshleifer D, Peng L & Wang Q (2023). Social networks and market reactions to earnings news. *Review of Financial Studies* 36:2897–2947.
- Shiller RJ (2019). *Narrative Economics*. Princeton UP.

**Stress ecology**
- Sapolsky RM (2004). *Why Zebras Don't Get Ulcers*, 3rd ed. Holt.
- Sapolsky RM, Romero LM & Munck AU (2000). How do glucocorticoids influence stress responses? *Endocrine Reviews* 21:55–89.
- Arnsten AFT (2009). Stress signalling pathways that impair prefrontal cortex structure and function. *Nature Reviews Neuroscience* 10:410–422.

**Time discounting ecology**
- Sozou PD (1998). On hyperbolic discounting and uncertain hazard rates. *Proceedings of the Royal Society B* 265:2015–2020.
- Rosati AG, Stevens JR, Hare B & Hauser MD (2007). The evolutionary origins of human patience. *Current Biology* 17:1663–1668.
- Ainslie G (2001). *Breakdown of Will*. Cambridge UP.
- Laibson D (1997). Golden eggs and hyperbolic discounting. *Quarterly Journal of Economics* 112:443–477.

**Sex differences / parental investment**
- Trivers RL (1972). Parental investment and sexual selection. In Campbell ed. *Sexual Selection and the Descent of Man 1871–1971*, 136–179.
- Daly M & Wilson M (1988). *Homicide*. Aldine.
- Byrnes JP, Miller DC & Schafer WD (1999). Gender differences in risk taking: a meta-analysis. *Psychological Bulletin* 125:367–383.

**Manipulation and signalling**
- Krebs JR & Dawkins R (1984). Animal signals: mind-reading and manipulation. In Krebs & Davies eds. *Behavioural Ecology*, 2nd ed., 380–402.

**Heuristics-and-biases / ecological rationality**
- Kahneman D (2011). *Thinking, Fast and Slow*. FSG.
- Tversky A & Kahneman D (1974). Judgment under uncertainty: heuristics and biases. *Science* 185:1124–1131.
- Gigerenzer G & Todd PM (1999). *Simple Heuristics That Make Us Smart*. Oxford UP.
- Gigerenzer G, Hertwig R & Pachur T eds. (2011). *Heuristics: The Foundations of Adaptive Behavior*. Oxford UP.
- Goldstein DG & Gigerenzer G (2002). Models of ecological rationality: the recognition heuristic. *Psychological Review* 109:75–90.
- DeMiguel V, Garlappi L & Uppal R (2009). Optimal versus naive diversification: how inefficient is the 1/N portfolio strategy? *Review of Financial Studies* 22:1915–1953.
- Gigerenzer G (2014). *Risk Savvy: How to Make Good Decisions*. Viking.

**Critique**
- Gould SJ & Lewontin RC (1979). The spandrels of San Marco and the Panglossian paradigm: a critique of the adaptationist programme. *Proceedings of the Royal Society B* 205:581–598.

---

## Candidate canonical graphs

1. **Johnson–Fowler payoff-asymmetry phase diagram.** x-axis: r / c\_fight ratio (0.5 to 5). y-axis: self-assessment noise σ (0 to 2). Colour: ESS confidence bias μ\* (heatmap, zero-diverging). Contour at μ\* = 0 (unbiased boundary). Markers for "Pleistocene contest," "modern face-to-face dispute," "modern capital-markets trade." Shows that the capital-markets parameter region is deep in the high-μ\* quadrant. Source: Johnson & Fowler 2011 Fig. 2 / *Nature* SI.

2. **Loss-aversion fitness asymmetry curve.** x-axis: resource level x, centred at survival threshold. y-axis left: survival probability (sigmoid-with-threshold). y-axis right: prospect-theory value function overlay (S-curve). Shaded bands showing the ancestral fitness-relevant range vs the modern portfolio-P&L range. Source: McDermott-Fowler-Smirnov 2008 Fig. 1; annotation derived from Caraco et al. 1980 data.

3. **Information-cascade diagram.** Sequential agents receiving private signals (H/L), observing predecessors' actions, computing posterior, acting. Annotation at cascade-formation point (typically agent 3 or 4) where the rational action decouples from private signal. Tree diagram of possible cascades, with "up cascade" and "down cascade" probabilities. Source: Bikhchandani-Hirshleifer-Welch 1992 Fig. 1.

4. **Herding cascade timeline.** Real or stylised timeline of a market episode (e.g. March 2020 Treasury dislocation). Panels: (a) news-shock timing; (b) initial informed trading; (c) cascade-recruitment phase (price movement independent of fundamentals); (d) reversal on shock-arrival of new public information. Overlay BHW cascade model predictions. Source: original plot, BHW 1992 + Brunnermeier-Pedersen 2009 data overlay.

5. **Ancestral-vs-modern-ecology table (visual)**. Rows: five mismatch components. Columns: ancestral condition / adaptive response / modern mismatch / process lever (copy of the table in the Modern-market mismatch section, rendered as a polished display graphic for the slide).

6. **Heuristics-and-biases vs ecological-rationality quadrant.** Two-by-two diagram. x-axis: does the environment have the heuristic's target structure (Y/N)? y-axis: is the cost of misfire concentrated or diffuse? Quadrants: (a) matched ecology, diffuse cost — Gigerenzer win; (b) matched ecology, concentrated cost — use the heuristic, engineer brakes; (c) mismatched ecology, diffuse cost — Kahneman-style debiasing; (d) mismatched ecology, concentrated cost — pre-commitment / hard gating. Map of typical investment decisions into the quadrants.

7. **Sapolsky stress-response duration mismatch.** Two panels. Top: ancestral acute threat — cortisol spike and return to baseline in ~90 minutes. Bottom: modern open-ended drawdown — cortisol elevation sustained over days to weeks. Overlay: cognitive-performance decrement (Arnsten PFC-attenuation curve) on the same timeline. Source: Sapolsky 2004 conceptual figure + Arnsten 2009 mechanistic data.
