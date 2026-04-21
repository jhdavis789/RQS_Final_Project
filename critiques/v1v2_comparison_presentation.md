# v1 vs v2 — Presentation Design Comparison

## Verdict

**v2 is materially better.** Confidence: high. It fixes the three most damaging v1 issues (framework-matrix wallpaper, DDM chart contradicting its own headline, HTML bug) and meaningfully strengthens the scientific-honesty posture that a Rockefeller-grade biomedical talk demands. It also addresses the structural gap the v1 critique flagged (no micro-to-macro bridge) via the new bond-translation slide. The cost is that v2 is one slide longer, captions still skew long, and two new honesty caveats (slide 6 "prediction, not theorem"; slide 10 "analog, not read-out") sap rhetorical punch that a live audience will miss. Net: v2 moves the deck from B+/B− to A−/B+ — presentation-grade for a review version, still needs a ~10% trim for live delivery.

---

## Change-by-change evaluation

### 1. Slide 1 hook — chart added, stats trimmed, quote smaller
**v1 problem real?** Yes. Four competing stats with no chart violated the exec-summary spec (G1.1 + G1.2) and produced a hook with no visual anchor.
**v2 fix landed?** Mostly. The dual-axis horizon-vs-Treasury line is now the visual center and the two remaining stats (−39%, +425 bp) are the two the critique recommended keeping. Cutting the −12.5% and "5 disciplines" stats removes double-counting.
**Regression?** Minor. The quote was rewritten from the compelling, present-tense "collapsed — at exactly the moment the market needed longer thinking" to a more hedged "a statistically reliable shortening... coincided with the largest bond drawdown in 40 years." That is more defensible but less arresting. The opening line of a Rockefeller-grade talk should *sing*; this one *qualifies*. The chart is also labeled "Schematic" — honest, but bold of an opening slide to announce "this is not real data." Consider a smaller schematic thumbnail + the real G1.1 as soon as it lands.

### 2. Slide 2 thesis — dropped "process beats self-awareness", added AMH framing
**v1 problem real?** Yes. The second sentence ("Process beats self-awareness…") was a slide-13 thesis doing double duty.
**v2 fix landed?** Yes in removing it. Replacement is longer and denser — the AMH paragraph is five dense lines where v1 had three, and it introduces rational-frictions-vs-behavioral mid-sentence, which is meta-frame content the audience can't evaluate until slide 13.
**Regression?** Yes, slight. The thesis slide should now breathe — v2 uses the recovered whitespace on a defensive framing paragraph rather than one sharp line. Strip the AMH paragraph down to two clauses ("Markets are regime-dependent; both rational-frictions and behavioral mechanisms show up in prices") or move it to slide 13 where it belongs.

### 3. Slide 3 framework — radiating schematic replaces 3×6 matrix
**v1 problem real?** Yes, decisively. This was the #1 issue in the critique.
**v2 fix landed?** Yes. The schematic is a clear win: three experiment nodes → central HPA-PFC pathway box → five discipline tags below. The visual now carries the argument; text density dropped from ~18 cells to ~11 labels + five short discipline captions. Information is communicated by *shape* not by *reading*.
**Regression?** Two minor issues. (a) The rays from discipline tags cross the central mechanism rectangle confusingly — all five "ray" lines converge toward the rectangle's bottom edge, creating a visual knot at the slide's center of gravity. (b) The chrono "additional signal" text at y=510 is nearly falling off the bottom of the viewBox on short laptop screens (viewBox is 0–560, and text sits at y=510). Test at 1366×768. (c) The reframe from "five independent disciplines converge" to "one pathway, five vocabularies" is a genuine philosophical upgrade — a neuroscientist would call it "multi-level integration," not "statistical convergence." Stronger argument.

### 4. Slide 6 DDM chart — regenerated as U-shape, "theorem" language dropped
**v1 problem real?** Yes, decisively. v1's chart was monotonic while its title said "U-shape is a theorem."
**v2 fix landed?** Yes. New chart (`ch-ushape`) is an explicit U with a dashed "noise band" in the middle deciles — narrative and chart now agree. Title dropped from "is a theorem" to "a prediction, not a theorem" (slide h2) and chart title is the more descriptive "Predicted forward-return signal by per-analyst confidence decile."
**Regression?** The softening is accurate but costs the slide's top of voice. "A theorem" was the strongest single claim in the deck; "a prediction, not a theorem" qualifies it into the pack. A compromise: "The U-shape is predicted by signal-detection theory — our data tests it" is assertive *and* honest. The current h2 leads with "not a theorem" which is a red-flag grammatical pattern (defining by negation).

### 5. Slide 8 Kandasamy chart — three bars → two bars with dual-axis
**v1 problem real?** Partially. v1 had fabricated day-1 data (0.44, 0.78) interpolated between placebo and day-8 — the critique flagged this as manufactured.
**v2 fix landed?** Yes. Two honest bars (Placebo, 8-day cortisol) on the two outcomes that are actually reported in the paper: α (0.50 → 0.35) and certainty-equivalent £ (25 → 14). The subtitle adds the correct caveat "chronic-only effect (acute cortisol: P=0.328, n.s.)" which the critique had not explicitly called for but is exactly right.
**Regression?** The v1 critique separately warned that dual-axis bar charts are misread by ~30% of quant audiences. v2 still uses a dual-axis bar chart. The fix for fabrication is good; the dual-axis hazard remains. Consider two single-axis bar pairs side-by-side (α on the left, £ on the right, shared x of {Placebo, Chronic}) as the critique recommended.

### 6. Slide 10 PAG diagram — relabel of lPAG, updated bottom annotation
**v1 problem real?** Yes. Bandler & Shipley's lateral PAG is confrontation / defensive attack, not "active freeze" (active freeze is more properly a behavioral-state label than a column function).
**v2 fix landed?** Yes, anatomically. lPAG now reads "Confrontation / defensive attack", vlPAG reads "Passive coping · freeze · parasympathetic" — this matches the current PAG literature. The bottom annotation correctly adds the fourth functional analog ("active risk up · benchmark-hug · active counter · no trade") to match the four columns.
**Regression?** None. Net improvement. Minor: the arrow paths in the PAG SVG still use `arrow-inhibit` on the PFC→amygdala arrows without the new `inhibithead` marker (defined at line 1377 but not attached to every inhibit path), so the inhibition semantics still read as arrows, not ⊣ bars. The critique flagged this in v1 and it persists in v2.

### 7. Data placeholder slides 5/7/9/11 — restructured as "Expected charts" + appendix-backing requirements
**v1 problem real?** Yes — they read as "science slide, then apology."
**v2 fix landed?** Partially. The new placeholder format is strictly better: left/right chart specs written out, plus an explicit "appendix backing required" line listing methodology checks (NLP validation κ, family-wise error rate, pre-registration status, selection-effects, rational-alternative distinguishability, sleep × decision pilot plan). This is *speaker-useful* scaffolding rather than apology.
**Regression?** The flow-break is still present — the placeholder slides still interrupt the rhythm between paired science slides, four times in fifteen slides. Structure is better, *position* is unchanged. The critique's stronger recommendation (merge data into science slide as a small thumbnail on the right, compressing 14 → 10 slides) was not taken; this is defensible but the flow cost remains.

### 8. Slide 12 brain-state — Hermans unchanged, HRV fake-scatter removed, honest-limits language added
**v1 problem real?** Yes. The HRV chart had fake scatter overlay on a saturating schematic — "we want a curve to exist."
**v2 fix landed?** Yes. The scatter is gone; the curve is honestly labeled "Neurovisceral-integration schematic (meta-analytic r ≈ 0.2–0.3)" which calibrates the reader to the modest effect size. The source note now says explicitly: "translating basic-science HRV-cognition effect sizes to investment-decision quality is an open research frontier, not a shovel-ready deployment." That is *exactly* the honesty a Rockefeller audience rewards.
**Regression?** Slight. The v2 h2 ("Some of that reconfiguration is readable with off-the-shelf hardware; much of it is not") is more honest than v1's ("measurable in real time with off-the-shelf hardware") but it's also wordier and less memorable. Also, the Hermans SVG text labels were made slightly longer — "propranolol blocks the reconfiguration; metyrapone (cortisol blocker) does not" is more precise but requires the reader to know what metyrapone is. Consider a micro-gloss or parenthetical the first time it appears.

### 9. New slide 13 — bond-market translation table
**v1 problem real?** Yes. The critique explicitly said "the market-level slide has been cut entirely — this removes the micro-to-macro bridge." It recommended reinstating exec-summary slide 9 before the recommendations.
**v2 fix landed?** Yes, and cleverly. Rather than a paragraph or schematic, v2 uses a 4-row table: behavioral finding → rational-frictions channel (Duffie, He-Krishnamurthy, Greenwood-Hanson, Vayanos/KVJ) → observable signature. This turns the slide into a *cross-reference mechanism* — the deck now talks to the fixed-income audience in its own idiom (intermediary pricing, funding-liquidity spirals, convenience yield). For an RQS bond audience specifically, this is the single slide that earns credibility.
**Regression?** None material. Minor: the table has twelve cells of 2–3 lines each — densest slide in the deck. For live delivery it will read fine because the speaker will narrate row-by-row, but on a standalone printout it sits at the edge of the density ceiling.

### 10. Slide 14 recommendations — HTML bug fixed, rec 4 highlighted, Haynes replaced
**v1 problems real?** (a) HTML bug `</h2>` closing an `eyebrow` div: yes, real; (b) visual identity of rec cards flat: yes; (c) Haynes 47% citation overstated: defensible but the critique didn't flag this.
**v2 fixes landed?** (a) Yes — line 870 closes cleanly with `</div>`. (b) Yes — rec 4 has `.highlight` class with `--accent-1` border and tinted background; the warmth does pull the eye. (c) Yes — rec 3 now cites Pronovost 2006 (central-line infection reduction, ~66%, more replicable) with the Urbach 2014 Ontario-null caveat on implementation fidelity. This is a genuinely stronger citation posture — Haynes 2009 had a famous replication-fidelity problem, Pronovost is the literature's go-to replicated result.
**Regression?** Slight. Rec 4's new body emphasizes "opt-in wearable pilot (N≈20 PMs, pre-registered)" rather than "formalize pre-FOMC / pre-CPI guardrails" (v1's actionable language). v1 was closer to a prescription; v2 is closer to a proposal. For an RQS audience deciding what to *do*, a recommendation card should be a recommendation — not a study design. Restore at least one concrete guardrail alongside the pilot.

### 11. Slide 15 close — rewording
**v1 problem real?** Yes. "Five disciplines converge" contradicted the six-column matrix.
**v2 fix landed?** Yes. New line: "Three experimental findings. *One pathway*, five vocabularies. Four instruments. *Measure → instrument → decide*." The reframe from "five disciplines converge" to "one pathway, five vocabularies" is the same philosophical upgrade as slide 3 — and the repetition is good presentation design (close echoes framework).
**Regression?** "Three experimental findings" is clunkier than v1's "Three biases" — biases is the deck's north-star word. Proposed: "Three biases, one pathway described five ways, four instruments" — keeps the punchier noun and preserves the new framing.

### 12. Discipline count (five vs six) consistency
**v1 problem real?** Yes, auditable inconsistency. Framework showed six disciplines, close said five.
**v2 fix landed?** Yes. Framework schematic shows five main (psychology, cellular neuro, endocrinology, computational, evolutionary) with chronobiology broken out as "additional signal" at the bottom. The close slide says "five vocabularies." Internally consistent.
**Regression?** None. The "additional signal" note for chrono is a reasonable compromise — it preserves the sleep evidence in the framework without inflating the headline count. The risk: a sharp reviewer will ask "why is chrono demoted?" Have the answer ready (it's a within-subject amplifier, not an independent mechanistic pathway).

### 13. Progress bar at bottom
**v1 problem real?** Yes, the critique recommended it verbatim.
**v2 fix landed?** Yes, 3px fill bar at bottom, `--accent-1` terracotta, transitions smoothly.
**Regression?** None. Good addition — quiet, peripheral-vision useful, doesn't steal attention. Hidden correctly in print CSS.

### 14. Click-to-advance removed
**v1 problem real?** Yes. The critique noted that a click-to-advance handler disrupted text selection for reviewers quoting the deck.
**v2 fix landed?** Yes. Click handler is removed (line 1507 comment: "click advance disabled for cleaner text selection").
**Regression?** User-hostile only if the presenter expects to click-advance in a walk-around scenario. For a seated presentation with keyboard or remote clicker, arrow-keys-only is standard. A remote clicker sends PageDown/PageUp which still works. This is design-sensible.

---

## Slide-by-slide walkthrough of v2

1. **Hook** — Works. Chart is the anchor, two stats flank, quote sits left. Minor: "schematic" label on the opening chart is an honesty red-flag; the pacing is good otherwise.
2. **Thesis** — Works but dense. The AMH paragraph is meta-content that steals air from the one-sentence thesis.
3. **Framework** — Works well. Radiating schematic teaches at a glance; chrono as "additional signal" is clever.
4. **A1a science** — Works. Fleming r updated from 0.46 to 0.50 (correct — Fleming 2010 Fig 2A cluster-level is ≈0.54, 0.50 is closer); per-analyst distributions overlay is pedagogically clean.
5. **A1a data placeholder** — Better scaffolding; still a flow-break.
6. **A1b science** — Works but apologetic. "A prediction, not a theorem" leads with a negation and hands rhetorical ground to skeptics.
7. **A1b data placeholder** — Same note as slide 5.
8. **A1c science** — Works. Kandasamy bars are honest now; "P=0.328 n.s." caveat is a credibility move.
9. **A1c data placeholder** — Same note as slide 5. The moderator-analysis right panel is an interesting asymmetric spec (different chart types left vs right).
10. **B1 science** — Works. PAG labels are anatomically correct; the added "analog, not circuit read-out" caveat is accurate but the h2 becomes very long (22 words).
11. **B1 data placeholder** — Same note as slide 5. "Rational-alternative distinguishability" language on the appendix line is exactly right for an RQS audience.
12. **Brain-state** — Works, better calibrated than v1. HRV is now honest.
13. **Bond translation (NEW)** — Works. Densest slide of the deck but earns its density by speaking bond-market idiom.
14. **Recommendations** — Works. HTML bug gone, rec 4 highlighted warmly, Pronovost + Urbach caveat is stronger than Haynes.
15. **Close** — Works. "One pathway, five vocabularies" echoes framework; "Three experimental findings" is slightly clunkier than "Three biases."

---

## Regressions in v2

1. **Slide 1 quote is more defensible, less arresting.** v1: "collapsed — at exactly the moment the market needed longer thinking." v2: "statistically reliable shortening... coincided with..." The hook should sing, not qualify.
2. **Slide 2 thesis has less whitespace.** The AMH paragraph is five dense lines where the slide should be one sentence + breathing room.
3. **Slide 6 h2 leads with a negation.** "A prediction, not a theorem" — rhetorical retreat in the chart title.
4. **Slide 10 h2 overlong at 22 words.** The caveat "a useful decomposition, not a direct circuit read-out" is correct but belongs in the caption, not the headline.
5. **Slide 14 rec 4 became more proposal, less prescription.** "Opt-in wearable pilot" replaced "formalize pre-FOMC guardrails" — softer action.
6. **Slide 15 "Three experimental findings" replaced "Three biases."** Clunkier noun.
7. **Dual-axis bar chart hazard on slide 8** — critique flagged it, v2 kept it.

---

## Unaddressed presentation issues

1. **Captions still paragraph-dense** — v2 compressed modestly (caption font 15 → 14.5px; line-height 1.45 → 1.4) but each mechanism caption is still four parallel bolded claims of 2–3 lines. ~15% compression, not the ~25–30% the critique asked for. For a live talk this is speaker-cue density, which is fine; for a PDF review it's still a reading assignment.
2. **"Illustrative" vs "schematic"** — v2 replaced "Illustrative" with "Schematic" on most charts (good — "schematic" is a design-vocabulary term, not a red flag). But some instances remain, e.g., slide 12 HRV source line says "Schematic of the neurovisceral-integration relationship" which is fine, but chart-subtitle on slide 6 uses "Schematic U-shape" which is both correct and still a red-flag word pair (it announces the primary visual is invented). At minimum, qualify with "Generated from the signal-detection formalism" or similar to move from *schematic* to *derived*.
3. **Print / PDF CSS** — v2 added `.progress-bar` to the print-hide list but did not fix the canvas-sizing issue the critique raised (canvases will lose resolution when print-to-PDF is used). Still broken for emailed PDFs.
4. **Chart.js SVG alt text** — v2 added `<title>` and `<desc>` to the PAG SVG and Hermans SVG — good. The framework SVG (new in v2) has no `<title>` or `<desc>`. Inconsistent.
5. **Kandasamy dual-axis** — unresolved, as above.
6. **Fleming — still simulated, not digitized** — the critique recommended digitizing the real Fleming 2010 Fig 2A. v2 kept the simulation but nudged r from 0.46 to 0.50 and softened the label to "Schematic scatter reproducing the reported cluster-level positive correlation." Honest but not empirical.
7. **Slide numbers 11–15 unreachable by number key** — v2 retains v1's numeric nav (0–9 maps to slides 1–10 only). Not documented; silent failure.
8. **Accessibility — focus states** — still no visible focus indicator, relevant if shared with a wider audience.

---

## Top 5 changes to prioritize for v3

1. **Slide 1 — restore the punchy verb.** Rewrite the hero quote back to active voice: *"In 2022, the written time horizons of our rates analysts shortened — at the exact moment the market needed longer thinking."* Keep the chart; keep the two stats; drop the word "statistically reliable" from the top-line quote (put it in the chart caption). The opening ~30 seconds set the register for the whole deck.

2. **Slide 6 — rewrite the h2 to lead from strength.** Current: "Under a Bayesian-calibrated reporter, signal concentrates at the tails of the confidence distribution — a prediction, not a theorem." Replace with: *"Signal-detection theory predicts a U-shape in accuracy vs. confidence. Our data tests that prediction."* Assertive *and* honest. The "not a theorem" hedge belongs in the caption, not the headline.

3. **Slide 8 — replace dual-axis Kandasamy bars with two side-by-side single-axis pairs.** This is the one place where v2 implemented the letter of the critique (two bars, accurate data) without addressing the chart-type hazard. Two small charts, shared x = {Placebo, Chronic}, α on the left, £ on the right. Quant audience reads this correctly 100% of the time.

4. **Slide 2 thesis — cut the AMH paragraph in half.** Current subtext is five lines. Proposed: two clauses — *"Meta-frame: Adaptive Markets Hypothesis. Both rational-frictions and behavioral mechanisms show up in prices; the question is which, in which regime, for what instrument."* Move the rest to slide 13's preamble where it fits.

5. **Slide 14 rec 4 — restore the actionable prescription.** Keep the pilot proposal, but lead with the prescription: *"Avoid major reallocations on sleep-deprived days; formalize pre-FOMC / pre-CPI guardrails. In parallel, opt-in wearable pilot (N≈20 PMs, pre-registered pre-FOMC windows) to establish a within-firm effect size."* Recommendations should read as recommendations first, studies second.

Honorable mentions: (a) compress captions another 15% for the PDF distribution path; (b) fix print-to-PDF canvas sizing; (c) add `<title>`/`<desc>` to the new framework SVG; (d) swap "Three experimental findings" back to "Three biases" in the close; (e) restore the anatomical ⊣ bar-head on PFC inhibition arrows in the PAG SVG.

---

## One-line verdict

**v2 is presentation-grade for a review reader; another ~60 minutes of editing on the hook quote, slide-6 h2, Kandasamy chart type, and thesis subtext would make it presentation-grade for a live RQS audience.**
