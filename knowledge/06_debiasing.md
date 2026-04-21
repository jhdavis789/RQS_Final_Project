# Does Self-Awareness Reduce Bias? — Deep Research

## Executive one-liner

Self-awareness alone is a weak debiasing lever. The strongest evidence that understanding biases *can* meaningfully reduce them comes from one line of work (Morewedge, Scopelliti, Sellier and colleagues) using structured, game-based training with personalized feedback — not simple "learn about bias" lectures. Kahneman's own late-career view is that organizations beat individuals at debiasing; the reliably-effective interventions — premortems, checklists, Analysis of Competing Hypotheses, noise-reducing "decision hygiene," and default-based nudges — sit at the *process* layer, not inside the analyst's head. The honest framing for RQS: measurement and awareness don't eliminate bias, but they shift it from invisible to instrumentable; processes built around known biases demonstrably outperform unaided judgement.

## The strongest pro-evidence — Morewedge et al. 2015

Morewedge, Yoon, Scopelliti, Symborski, Korris and Kassam (2015), *Policy Insights from the Behavioral and Brain Sciences* 2(1): 129–140, "Debiasing Decisions: Improved Decision Making With a Single Training Intervention," is the most-cited pro-evidence paper and deserves careful reading.

Key design features:

- Two longitudinal experiments, funded under IARPA's SIRIUS program to improve intelligence-analyst judgment.
- Interventions were either a ~30-minute instructional video or an interactive computer game that let participants diagnose their own biases, receive personalized feedback, and practice mitigation strategies.
- Experiment 1 targeted bias blind spot, confirmation bias, and fundamental attribution error. Experiment 2 targeted anchoring, representativeness, and social projection.
- Outcomes measured immediately after training and again at two to three months.

Reported effect sizes (decrease in bias commission relative to control):

- Games: ≥ −31.94% immediately; ≥ −23.57% at roughly 8–12 weeks.
- Videos: ≥ −18.60% immediately; ≥ −19.20% at follow-up.
- Games beat videos, consistent with the general finding that personalized feedback and active practice outperform passive instruction.

Two features make these effects more credible than typical debiasing lab studies:

1. **Durability.** Most prior debiasing interventions show decay within hours or days. The Morewedge games held most of the effect two-to-three months out.
2. **Domain-generality.** Reductions appeared on problems worded and contextualized differently from training problems, suggesting something beyond teaching-to-the-test.

The follow-up field study, Sellier, Scopelliti and Morewedge (2019), *Psychological Science* 30(9): 1371–1379, "Debiasing Training Improves Decision Making in the Field," is the strongest transfer evidence currently available. In N = 290 French graduate business, entrepreneurship, and strategy students, a one-shot training reduced confirmation bias in an unannounced business case modeled on the Challenger launch decision. Trained students were ~29% less likely to choose the inferior confirming solution (a published corrigendum revised some figures closer to 19%, still a large effect). This is the only study that demonstrates training-transfer to an ostensibly unrelated, professional-looking task.

Honest caveats before leaning on this evidence:

- The training was purpose-built on top of millions of dollars of IARPA funding. Off-the-shelf "bias awareness" corporate training is not the same intervention and should not claim the same effect sizes.
- Effect sizes are measured against control conditions on crafted test items, not against real portfolio P&L.
- Transfer evidence is still thin — one field experiment on MBAs.
- Scopelliti et al. (2015), *Management Science* 61(10): 2468–2486, showed that people who score high on the bias-blind-spot scale are *less* responsive to debiasing interventions. The people who most need training benefit least.

## The obstacle — bias blind spot

Pronin, Lin and Ross (2002), *Personality and Social Psychology Bulletin* 28(3): 369–381, "The Bias Blind Spot: Perceptions of Bias in Self Versus Others," is the single biggest challenge to a self-awareness thesis. Across three studies:

- Subjects rated themselves less subject to eight common biases than the average American, classmates, and fellow airport travelers.
- After reading clear descriptions of how a given bias could have affected them, participants *still* insisted their own self-assessments were accurate and objective.
- Participants judged peers' self-serving attributions about test performance as biased while treating their own identical self-serving attributions as evidence-based.

Why this matters for an RQS thesis: the mechanism by which self-awareness is supposed to work — "I know I am vulnerable to anchoring, so I will correct for it" — collides with the demonstrated human tendency to exempt *oneself* from the biases one recognizes in others. Naïve realism ("I see reality as it is; you have a bias") is not fixed by information alone. Scopelliti, Morewedge et al. (2015) extended this with a validated 14-item bias-blind-spot scale that predicts: (a) better-than-average judgments on easy tasks, (b) ignoring advice, and (c) resistance to debiasing interventions. Bias blind spot is a stable, measurable metabias.

## Fischhoff and the long hindsight-bias literature — debiasing usually doesn't stick

Fischhoff's 1975 "I knew it would happen" and 1977 "Perceived informativeness of facts" launched the hindsight-bias debiasing literature. The core finding, replicated for fifty years (Roese & Vohs 2012, *Perspectives on Psychological Science*; Bernstein, Aßfalg et al. 2025 retrospective): informational and motivational debiasing manipulations — warning people about hindsight bias, paying for accuracy, asking them to generate alternative outcomes — produce at best modest reductions, often unreliable, and prone to reversion. The *only* manipulation with consistently large effects is forcing people to explain how each alternative outcome could have happened (Slovic & Fischhoff 1977; Arkes et al. 1988). That is a structured process, not self-awareness.

Fischhoff's later title "For Those Condemned to Study the Past: Heuristics and Biases in Hindsight" (1980, in *Judgment Under Uncertainty*) captures the pessimism: experts were not reliably less biased than novices, warnings produced minimal improvement, and benefits decayed.

## Metacognitive training — mixed and fragile

Fleming and colleagues study whether metacognitive accuracy (the correlation between confidence and correctness) can be trained. Carpenter, Sherman, Kievit, Seth, Lau and Fleming (2019), *Psychological Science* 30(8): 1184–1199, reported domain-general improvement with adaptive training and monetary incentives tied to confidence calibration. But Haddara and Rahnev (2022), *Psychological Science* 33(5): 740–754, "Metacognitive improvement: Disentangling adaptive training from experimental confounds," pre-registered a conceptual replication controlling for the incentive/instruction confound and found moderate Bayesian evidence for *no* metacognitive training effect. Fleming's 2024 *Annual Review of Psychology* synthesis, "Metacognition and Confidence: A Review and Synthesis," concludes metacognitive efficiency is partly trait-like, partly trainable with tight feedback loops, and largely context-specific. The pattern is the same as general debiasing: training works only where feedback is frequent, outcomes are observable, and the task is stable.

Consistent with this: Lichtenstein & Fischhoff (1980) trained probability-calibration with 45 minutes of instruction plus 22 hours of tested trials with feedback. Calibration improved — but only under that intensive feedback regime, and only on similar task structures. The well-known observation that expert bridge players, oddsmakers, and National Weather Service forecasters show little overconfidence is best explained not by self-awareness but by daily, scored, unambiguous feedback. Investment analysts, whose forecasts are evaluated noisily and on multi-year lags, structurally lack that feedback loop.

## Affect labeling — mechanism evidence for why self-knowledge sometimes helps

Lieberman, Eisenberger, Crockett, Tom, Pfeifer and Way (2007), *Psychological Science* 18(5): 421–428, "Putting Feelings Into Words: Affect Labeling Disrupts Amygdala Activity in Response to Affective Stimuli," provides fMRI evidence that labeling an emotional state — "I feel anxious right now" — reduces amygdala activation and increases right ventrolateral prefrontal cortex activation, with medial PFC mediating the pathway. Crucially, labeling a neutral feature of the stimulus (e.g., naming a person "Harry") did not produce the amygdala dampening; the effect requires *emotional* labeling.

This is the best mechanistic evidence for the "name it to tame it" side of the self-awareness claim. For a portfolio manager, it suggests that explicitly identifying "I am currently experiencing regret aversion on this position" may reduce the hot-emotional driver of a bad trade. But the effect is on emotional reactivity, not on deliberative reasoning errors like base-rate neglect. It is a narrower claim than "self-awareness fixes bias."

## Consider-the-opposite — the most portable self-directed technique

Lord, Lepper and Preston (1984), *Journal of Personality and Social Psychology* 47(6): 1231–1243, "Considering the Opposite: A Corrective Strategy for Social Judgment," showed that instructing subjects to actively consider reasons the opposite conclusion might be true reduced biased assimilation and biased hypothesis-testing more than simply instructing them to be "fair and unbiased." Koriat, Lichtenstein and Fischhoff (1980) used the same strategy against overconfidence and raised percent-correct confidence calibration from 62.9% (control) to 69.7% (consider-the-opposite) — a real, repeatable, but bounded effect. Mussweiler, Strack and Pfeiffer (2000) extended this to anchoring: selectively considering anchor-inconsistent evidence reduced anchoring, while merely brainstorming more evidence did not. The narrow operative mechanism is forced search through the counter-evidential space — not general mindfulness about one's biases.

This is a tool, not a disposition. It works when executed on a specific decision. It doesn't make someone a less biased person overall.

## What actually works: process-level interventions

### Premortem (Klein 2007)

Klein's "Performing a Project Premortem," *Harvard Business Review*, September 2007, operationalizes prospective hindsight: the team assumes the project has failed and generates reasons why. Mitchell, Russo and Pennington (1989), *Journal of Behavioral Decision Making*, found prospective hindsight increases the specificity and accuracy of failure-reason generation by about 30% versus standard critique. Klein, Koller and Lovallo's follow-up with McKinsey ("Bias Busters: Premortems: Being smart at the start" and Klein's 2021 *Psychology Today* piece) reports premortems unblock dissent that social-cohesion pressures otherwise suppress. It is cheap, ~1 hour, and fits naturally into an investment committee calendar.

### Checklists

Pronovost et al. (2006), *New England Journal of Medicine* 355(26): 2725–2732, "An Intervention to Decrease Catheter-Related Bloodstream Infections in the ICU," reported that a 5-item central-line checklist across 103 Michigan ICUs cut the median catheter-related bloodstream infection rate from 2.7 per 1,000 catheter-days to 0 within 3 months, with a 66% sustained reduction at 16–18 months. Lipitz-Snyderman et al. (2011), *BMJ*, found associated hospital-mortality reductions in the Michigan Keystone initiative versus controls.

Haynes, Weiser, Berry, Gawande et al. (2009), *NEJM* 360(5): 491–499, "A Surgical Safety Checklist to Reduce Morbidity and Mortality in a Global Population," tested a 19-item WHO checklist across 8 hospitals on 4 continents: surgical complications fell from 11.0% to 7.0% (−36%) and in-hospital mortality from 1.5% to 0.8% (−47%). These effect sizes dwarf any individual cognitive-training result in the literature.

Gawande's *The Checklist Manifesto* (2009) generalizes: checklists dominate expertise in domains characterized by (a) complex tasks with known failure modes, (b) time pressure, and (c) social hierarchy that suppresses junior dissent. Investment committees tick all three boxes.

### Structured Analytic Techniques (Heuer; CIA)

Heuer's *Psychology of Intelligence Analysis* (CIA Center for the Study of Intelligence, 1999) and Heuer & Pherson's *Structured Analytic Techniques for Intelligence Analysis* (2nd ed., CQ Press, 2015) catalog 50–55 SATs across eight categories: decomposition, idea generation, scenarios, hypothesis testing, cause/effect, challenge analysis, conflict management, decision support. The flagship technique is Analysis of Competing Hypotheses (ACH): enumerate hypotheses, score each piece of evidence against each hypothesis on consistency, focus on *disconfirming* evidence. The CIA adopted SATs explicitly because individual analyst self-awareness failed to catch the Bay of Pigs, Yom Kippur, and pre-Iraq WMD assessments. Empirical validation is thinner than in medicine — Chang, Berdini, Mandel & Tetlock (2018), *Judgment and Decision Making*, found ACH showed modest benefit over unstructured analysis on some tasks and no benefit on others — but the institutional verdict is clear: intelligence work should not depend on individual debiasing.

### Noise and decision hygiene (Kahneman, Sibony, Sunstein 2021)

*Noise: A Flaw in Human Judgment* (Little, Brown Spark, 2021) distinguishes **bias** (systematic mean error) from **noise** (variability around the mean for the same case). In a large insurance company the authors audited, underwriters' premium estimates for identical fictive customers varied by a *median* 55% between underwriters — five times what management expected. Judges, radiologists, forensic scientists, patent examiners, and asylum officers show comparable noise. Since MSE = Bias² + Noise, reducing noise is a second, independent lever.

"Decision hygiene" practices the authors recommend:

1. Decompose the judgment into independent components before aggregating.
2. Take the outside view (comparison class) before the inside view.
3. Sequence information so early anchors don't corrupt later assessments.
4. Have judges make *independent* estimates before group discussion (Delphi-style).
5. Use structured interviews/scorecards.
6. Run "noise audits" periodically.

For an investment committee, the relevant implication: even when members have identical information and identical biases, their *variability* still causes losses. Structured independent voting before discussion is a direct and testable hygiene upgrade.

### Nudges and choice architecture

Thaler & Sunstein's *Nudge* (2008) and Thaler & Benartzi (2004), "Save More Tomorrow," *Journal of Political Economy* 112(S1): S164–S187, demonstrate that changing defaults and commitment structures produces vastly larger effects than trying to educate participants out of present bias. In the original three 401(k) field studies (8,500+ employees across 500 plans), enrollees who signed up for SMT raised savings rates from 3.5% to 13.6% in under four years, with 80% still in the program. This is the canonical example of **modifying the environment** rather than **modifying the person** — Soll, Milkman and Payne's (2016) taxonomy in the *Wiley Blackwell Handbook of Judgment and Decision Making*, chapter 33, "A User's Guide to Debiasing." Their framework classifies interventions along that exact axis and concludes that environment-modifying debiasing is, on average, larger in effect and more durable than person-modifying debiasing.

### Committees done right — wisdom of crowds vs. groupthink

Surowiecki's *The Wisdom of Crowds* (2004), synthesizing Galton's 1906 ox-weight demonstration and a century of aggregation research, identifies four conditions under which groups outperform individuals: **diversity of opinion, independence, decentralization, and a good aggregation mechanism**. Violate any one — especially independence — and you don't get wisdom, you get groupthink.

Janis's *Victims of Groupthink* (1972) documented the Bay of Pigs failure mode: smart people with private doubts self-censoring to preserve cohesion, stereotyping adversaries, failing to challenge unstated assumptions. 't Hart, Stern & Sundelius's 1997 reassessments (Organizational Behavior and Human Decision Processes Vol. 73 special issue) partially qualified Janis — causal weight on cohesion specifically was overstated — but the core decision-hygiene implication survives: committees need structural features (assigned devil's advocate, independent pre-voting, premortems, red teams) to stay on the wisdom-of-crowds side of the line.

### Red teams

Hoffman's *Red Teaming: How Your Business Can Conquer the Competition by Challenging Everything* (2017), alongside CIA Directorate of Analysis Alternative Analysis procedures (Heuer & Pherson 2015, ch. 9–11), formalize structured adversarial review. The UK MoD Red Teaming Guide (2nd ed., 2013) reports in case surveys that red teams surface decision-altering information in ~40–60% of major planning exercises. Empirical evidence outside intelligence/military is thin, but the theoretical case is the same as premortem: enforce counter-evidential search without relying on junior team members to risk career capital by dissenting.

## Why process often beats self-awareness

Four reasons process interventions produce larger, more durable effects than individual debiasing:

1. **They don't rely on the biased agent to recognize the bias in the moment.** Bias blind spot guarantees that the analyst most in need of correction is the least likely to seek it.
2. **They convert judgment into structured sub-judgments.** Each sub-judgment is lower-stakes and more amenable to calibration feedback.
3. **They are persistent.** A checklist sits on the wall; a trained insight decays.
4. **They shift incentives.** Requiring a written premortem or ACH table creates audit trails that reward honest dissent and discourage late-stage rationalization.

Kahneman summarized this in his McKinsey Quarterly interview with Tim Koller (published post-*Noise*): "I'm much more optimistic about organizations than individuals … organizations can put systems in place." He repeatedly said in 2011–2024 interviews that fifty years of studying biases had not made him meaningfully less biased; it had only made him better at recognizing other people's biases after the fact. That admission — from the person who, more than anyone else, built the self-awareness-as-remedy intuition — is load-bearing evidence against the strong version of the thesis.

## Implications for a thesis at RQS

A version of the thesis that will hold up in Q&A:

> "Measurement and awareness don't eliminate bias, but they shift it from invisible to instrumentable. Processes built around known and measured biases demonstrably outperform unaided expert judgment. The goal is not to make each analyst less biased — the evidence says that is hard and unreliable — but to build a decision architecture (premortems, ACH, independent pre-voting, noise audits, checklists, red teams, well-designed defaults) around biases we can measure."

Concrete RQS applications, each with literature support:

- **Pre-vote, then discuss.** Independent written estimates before committee conversation (*Noise* decision hygiene; Surowiecki independence condition).
- **Premortem new positions at size.** 60-minute structured session imagining the trade has blown up in 18 months (Klein 2007; Mitchell, Russo & Pennington 1989).
- **ACH for high-conviction contrarian calls.** Force enumeration of competing hypotheses and scoring against disconfirming evidence (Heuer 1999).
- **Noise audit of PM teams.** Periodically give the same scenario to multiple PMs and measure spread; decompose into bias and noise (Kahneman, Sibony & Sunstein 2021).
- **Calibration training with outcomes feedback.** Tight-feedback weather-forecaster model (Lichtenstein & Fischhoff 1980; Mellers et al. Good Judgment Project 2014).
- **Red team for every major position above a threshold size.**

What to *avoid* claiming: that understanding biases makes individual PMs less biased. It usually doesn't, and the bias-blind-spot literature predicts the most senior PMs will be the most resistant to the training. Claim instead that measurement creates the *substrate* on which process interventions can operate.

## Counter-evidence and honest limits

- **Training decay.** Most debiasing training effects decay substantially over 3–12 months without reinforcement (Fischhoff 1982; Milkman, Chugh & Bazerman 2009, *Perspectives on Psychological Science* 4(4): 379–383, "How Can Decision Making Be Improved?"). Morewedge's games are unusual in holding up for 2–3 months.
- **Expert overconfidence.** Tetlock, *Expert Political Judgment* (2005), found famous pundits were worse-calibrated than dart-throwing chimpanzees on political forecasts and did not improve despite decades of experience. Expertise without calibrated feedback does not self-correct.
- **Overcorrection and backfire.** Anchoring-debiasing can reverse into opposite-anchor effects if the subject over-applies the counter-consideration (Mussweiler et al. 2000). Fact-checking sometimes strengthens belief in the original claim — the "backfire effect" originally argued by Nyhan & Reifler (2010) has been partially replicated and partially not (Wood & Porter 2019, *Political Behavior*), but the general lesson — that naïve debiasing can hurt — stands.
- **Incentive structure dominates.** Career-risk compensation asymmetry (heads I get paid, tails I still get paid) swamps cognitive training; no amount of self-awareness fixes a principal-agent problem.
- **Checklists fail when implemented as theater.** Urbach et al. (2014), *NEJM* 370(11): 1029–1038, on Ontario's mandated surgical checklist rollout, found *no* mortality benefit in the province — because compliance was checkbox-level, not cultural. Process interventions require implementation fidelity.
- **Groupthink re-analysis.** Some of Janis's original causal claims about cohesion-driven groupthink have been weakened by Tetlock, Peterson, McGuire et al. (1992) and the 1998 *OBHDP* special issue; the more durable finding is that specific structural features (independent voting, devil's advocate, outside review) matter, not cohesion per se.
- **Heuer/SAT effectiveness.** Dhami et al. (2019), *Intelligence and National Security*, and Chang et al. (2018) find that structured analytic techniques improve accuracy modestly and inconsistently. The strongest case for SATs is process hygiene and auditability, not sharper forecasts.

The honest picture: no single intervention — individual or process — is a silver bullet. Layered interventions (training + process + feedback) outperform any single lever. The research does not support the strong version of the thesis ("understanding yourself defeats bias"). It supports the engineered version ("measuring bias enables processes that beat unaided judgment").

## Citations

- Bernstein, Aßfalg, Erdfelder et al. (2025). "Fifty Years of Hindsight Bias Research—Reflection on Fischhoff (1975)."
- Carpenter, Sherman, Kievit, Seth, Lau & Fleming (2019). "Domain-general enhancements of metacognitive ability through adaptive training." *Psychological Science* 30(8): 1184–1199.
- Chang, Berdini, Mandel & Tetlock (2018). "Restructuring structured analytic techniques in intelligence." *Intelligence and National Security* 33(3): 337–356.
- Fischhoff (1975). "Hindsight ≠ foresight." *JEP: HPP* 1(3): 288–299.
- Fischhoff (1982). "Debiasing." In Kahneman, Slovic & Tversky, *Judgment Under Uncertainty*.
- Fleming (2024). "Metacognition and Confidence: A Review and Synthesis." *Annual Review of Psychology*.
- Gawande (2009). *The Checklist Manifesto*. Metropolitan Books.
- Haddara & Rahnev (2022). "Metacognitive improvement: Disentangling adaptive training from experimental confounds." *Psychological Science* 33(5): 740–754.
- Haynes, Weiser, Berry, Gawande et al. (2009). "A Surgical Safety Checklist to Reduce Morbidity and Mortality in a Global Population." *NEJM* 360(5): 491–499.
- Heuer (1999). *Psychology of Intelligence Analysis*. CIA Center for the Study of Intelligence.
- Heuer & Pherson (2015). *Structured Analytic Techniques for Intelligence Analysis* (2nd ed.). CQ Press.
- Janis (1972). *Victims of Groupthink*. Houghton Mifflin.
- Kahneman, Sibony & Sunstein (2021). *Noise: A Flaw in Human Judgment*. Little, Brown Spark.
- Klein (2007). "Performing a Project Premortem." *Harvard Business Review* September 2007.
- Koriat, Lichtenstein & Fischhoff (1980). "Reasons for confidence." *JEP: HLM* 6(2): 107–118.
- Lichtenstein & Fischhoff (1980). "Training for calibration." *OBHP* 26(2): 149–171.
- Lieberman, Eisenberger, Crockett, Tom, Pfeifer & Way (2007). "Putting Feelings Into Words." *Psychological Science* 18(5): 421–428.
- Lipitz-Snyderman et al. (2011). "Impact of a statewide intensive care unit quality improvement initiative on hospital mortality and length of stay." *BMJ*.
- Lord, Lepper & Preston (1984). "Considering the Opposite: A Corrective Strategy for Social Judgment." *JPSP* 47(6): 1231–1243.
- Milkman, Chugh & Bazerman (2009). "How Can Decision Making Be Improved?" *Perspectives on Psychological Science* 4(4): 379–383.
- Mitchell, Russo & Pennington (1989). "Back to the future: Temporal perspective in the explanation of events." *JBDM*.
- Morewedge, Yoon, Scopelliti, Symborski, Korris & Kassam (2015). "Debiasing Decisions." *Policy Insights from the Behavioral and Brain Sciences* 2(1): 129–140.
- Mussweiler, Strack & Pfeiffer (2000). "Overcoming the inevitable anchoring effect." *PSPB* 26(9): 1142–1150.
- Nyhan & Reifler (2010). "When Corrections Fail." *Political Behavior* 32(2): 303–330.
- Pronin, Lin & Ross (2002). "The Bias Blind Spot." *PSPB* 28(3): 369–381.
- Pronovost et al. (2006). "An Intervention to Decrease Catheter-Related Bloodstream Infections in the ICU." *NEJM* 355(26): 2725–2732.
- Roese & Vohs (2012). "Hindsight Bias." *Perspectives on Psychological Science* 7(5): 411–426.
- Scopelliti, Morewedge, McCormick, Min, Lebrecht & Kassam (2015). "Bias Blind Spot: Structure, Measurement, and Consequences." *Management Science* 61(10): 2468–2486.
- Sellier, Scopelliti & Morewedge (2019). "Debiasing Training Improves Decision Making in the Field." *Psychological Science* 30(9): 1371–1379.
- Slovic & Fischhoff (1977). "On the psychology of experimental surprises." *JEP: HPP* 3(4): 544–551.
- Soll, Milkman & Payne (2016). "A User's Guide to Debiasing." In *Wiley Blackwell Handbook of Judgment and Decision Making*, ch. 33.
- Surowiecki (2004). *The Wisdom of Crowds*. Doubleday.
- Tetlock (2005). *Expert Political Judgment*. Princeton University Press.
- Thaler & Benartzi (2004). "Save More Tomorrow." *JPE* 112(S1): S164–S187.
- Thaler & Sunstein (2008). *Nudge*. Yale University Press.
- Urbach et al. (2014). "Introduction of Surgical Safety Checklists in Ontario, Canada." *NEJM* 370(11): 1029–1038.
- Wood & Porter (2019). "The Elusive Backfire Effect." *Political Behavior* 41: 135–163.

## Candidate canonical graphs

Suggested chart concepts for the RQS slide (all scripted from cited data — no LLM-computed numbers):

1. **Debiasing effect size by intervention type.** Horizontal bar chart, x-axis = % reduction in bias commission vs. control, bars for: single lecture (~5–10%), consider-the-opposite (~7pp on calibration), Morewedge video (~18–19%), Morewedge game immediate (~32%), Morewedge game at 2–3 months (~24%), Sellier field-transfer to MBAs (~19–29%). Source: Morewedge et al. 2015, Sellier et al. 2019, Koriat et al. 1980.
2. **Checklist mortality reductions.** Two panels: Pronovost central-line infection rate (2.7 → 0 per 1000 catheter-days in 3 months, 66% sustained reduction at 16–18 months) and WHO Surgical Safety Checklist (complications 11.0%→7.0%, deaths 1.5%→0.8%). Source: Pronovost et al. 2006; Haynes et al. 2009.
3. **Bias blind spot asymmetry.** Bar chart of self-vs-other bias ratings on 8 biases from Pronin, Lin & Ross 2002 Study 1 — every bias shows "others more biased than me."
4. **Noise in professional judgment.** Box-plot of 55% median spread in insurance-underwriter premiums for identical cases from *Noise* (Kahneman, Sibony & Sunstein 2021).
5. **Save More Tomorrow savings trajectory.** Line chart of enrolled employees' savings rate (3.5% → 13.6% over ~4 years) versus non-enrolled control group. Source: Thaler & Benartzi 2004.
6. **Decay of debiasing over time.** Line chart (Morewedge game vs. video) showing effect size at post-test, 2 weeks, 2–3 months — illustrates both the real persistence and the partial decay.

Chart style: straight lines (tension:0), visible dots on each data point, no black ink, theme colors only.
