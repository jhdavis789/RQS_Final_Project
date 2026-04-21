# v2 vs v3 — Polish-Round Comparison

## Verdict

**v3 is unambiguously better than v2. Confidence: high. Ship v3.** Every one of the thirteen targeted changes from the two v1v2 top-5 lists landed correctly; all Chart.js charts still render (the new split Kandasamy charts have matching canvas IDs and separate `Chart()` initializers); HTML structure is intact (15/15 sections, 181/181 divs, identical counts to v2); the two real citation fixes (Greenwood-Hanson → *RFS*, Bordalo-Gennaioli-Shleifer replacing the unverifiable Ma-Paligorova-Peydró) both stand up; and the presentation-round polish (punchy Slide 1 quote, confident Slide 6 h2, compact thesis, prescription-first rec 4) restores the rhetorical voltage that the v1v2-presentation critique identified as the remaining blocker for live delivery. The only new issues are cosmetic (the `<div class="hint">` footer still reads "v2" instead of "v3"; the `SCHEMATIC` watermark was applied to only the two most-at-risk charts rather than all schematic charts; the Slide 8 split Kandasamy uses inline `style="display:grid..."` which is slightly unclean but works). Zero content regressions from the compression pass. The deck is now presentation-grade for a live RQS audience — the remaining weak points are in the empirical-data slides (placeholder 5/7/9/11), which is the right layer to be thin given the user is adding data slides next.

## Change-by-change evaluation

**1. Slide 1 hero quote restored to punchy active voice — LANDED.** v3 line 440: "In 2022, the written time horizons of our rates analysts *shortened* — at the exact moment the market needed longer thinking." Exactly the phrasing the presentation critique prescribed. The two stats (−39%, +425 bp) stayed. Adequate.

**2. Slide 6 h2 leads from strength — LANDED.** v3 line 635: "Signal-detection theory predicts a U-shape in accuracy vs. confidence. Our data tests that prediction." Assertive, two sentences, no negation-first. Exactly the critique's recommended wording. The "not a theorem" hedge moved entirely out of the h2 (no trace anywhere in the slide — even the chart title just reads "Predicted forward-return signal by per-analyst confidence decile"). Adequate.

**3. Slide 8 Kandasamy chart split into two single-axis charts — LANDED.** v3 lines 704–707: a single `.chart-canvas` inner div is converted to `display: grid; grid-template-columns: 1fr 1fr` with two separate canvases (`ch-kandasamy-alpha` on left, `ch-kandasamy-ce` on right). Both charts have separate `new Chart(...)` initializers (lines 1282 and 1311), each with its own y-axis, title, and `legend: { display: false }`. X-axis is shared {Placebo, 8-day cortisol}. This closes the dual-axis-bar-chart hazard the presentation critique flagged. Chart.js will handle two charts in grid cells correctly given `maintainAspectRatio: false; responsive: true`. Adequate. Minor: the split charts are now half-width each, so individual bar details are smaller than v2's dual-axis chart — but accuracy of reading is meaningfully higher.

**4. Slide 2 thesis subtext cut approximately in half — LANDED.** v2 subtext ≈60 words; v3 subtext ≈25 words: "Meta-frame: **Adaptive Markets Hypothesis** (Lo 2004). Both rational-frictions and behavioral mechanisms show up in prices; the question is *which*, in *which regime*, for *what instrument*." The italicized triplet is a nice rhetorical flourish that also restores the whitespace the critique flagged. The excised "quant's job, not a battle between EMH and behavioral finance" clause is now implicit rather than stated; acceptable cost.

**5. Slide 14 rec 4 restored to prescription-first — LANDED.** v3 line 923 opens with **bold**: "Avoid major reallocations on sleep-deprived days; formalize pre-FOMC and pre-CPI guardrails." Then the Yoo 2007 mechanism. Then "In parallel, opt-in wearable pilot (N≈20 PMs, pre-registered windows)..." The prescription + study structure is exactly what the critique prescribed. Adequate.

**6. Greenwood-Hanson 2013 corrected from *JF* to *RFS* — LANDED.** v3 line 871: "Greenwood & Hanson 2013 *RFS* on issuer-quality signals". Correctly updated. The paper ("Issuer Quality and Corporate Bond Returns") was indeed published in *RFS* 26(6):1483–1525 (2013).

**7. Ma-Paligorova-Peydró 2021 citation replaced with Bordalo, Gennaioli & Shleifer 2018 *JF* — LANDED and verifiably correct.** v3 line 871: "Bordalo, Gennaioli & Shleifer 2018 *JF* on diagnostic expectations and credit cycles." This is a real, well-known paper — Bordalo, Gennaioli & Shleifer "Diagnostic Expectations and Credit Cycles," *Journal of Finance* 73(1):199–227 (2018). It is arguably a *better* fit for the "conviction at the tails / over-extrapolation" row than the original citation because diagnostic expectations are literally about extrapolative/stereotype-driven belief formation. Adequate and an upgrade.

**8. SCHEMATIC watermark added to hook chart and Fleming scatter — LANDED.** v3 CSS lines 400–414 define `.chart-canvas.schematic::after` with a corner "SCHEMATIC" badge. Class is applied in v3 line 456 (hook) and line 582 (Fleming scatter). Two instances, correctly placed on the two charts a reviewer could mis-read as real data. Adequate. Minor: the U-shape, Kepecs, Arnsten, Coates, and HRV charts are also schematics, and a consistency argument would apply the badge to all of them — but the critique specifically flagged only these two, and their labels/titles already say "schematic" explicitly elsewhere.

**9. Print-CSS canvas sizing improved — LANDED.** v3 lines 416–422: full rewrite of the `@media print` block. Key additions: `html, body { overflow: visible; height: auto; }`, `.deck { height: auto; overflow: visible; }`, `.slide { position: relative !important; ... overflow: visible; }`, `canvas { max-width: 100%; height: auto !important; }`. This replaces v2's single `height: 100vh` rule and now permits the deck to lay out vertically in print and the canvases to stay within the page. One concern: `canvas { height: auto !important; }` can collapse charts in some browsers if the intrinsic canvas dimensions are small; a safer rule would be `max-height: 100vh`. Net is still a clear improvement.

**10. Framework SVG accessibility — LANDED.** v3 lines 488–490: `<svg ... role="img" aria-labelledby="fw-title fw-desc">` with `<title id="fw-title">Cross-disciplinary evidence schematic</title>` and `<desc id="fw-desc">` providing a complete description of the figure. Consistent with the existing `<title>`/`<desc>` on the PAG and Hermans SVGs. Adequate.

**11. Slide 10 h2 shortened — LANDED.** v2: "Active-risk-up · benchmark-hug · no-trade map to functionally distinct circuits — a useful decomposition, not a direct circuit read-out" (21 words). v3 line 754: "Active-risk-up, benchmark-hug, and no-trade map to distinct defensive circuits" (10 words). Under 15 words. The "useful decomposition, not a circuit read-out" caveat is preserved in the takeaway (line 778: "The decomposition is a causal map for instrument design — the neural substrate is an analog, not a direct circuit read-out"). The h2 is now headline-length; the qualifier is still in the room, just demoted. Adequate.

**12. Slide 15 close: "Three experimental findings" → "Three biases" — LANDED.** v3 line 941: "Three biases. *One pathway*, five vocabularies. Four instruments. *Measure → instrument → decide.*" The deck's north-star noun is restored. The "three experimental findings" phrase still lives on the Slide 3 eyebrow, which is fine — the framework slide announces the experimental structure; the close slide announces the biases. Consistent.

**13. Captions compressed by ~15% more — LANDED.** Spot-checks:
- **Slide 4 caption**: v2 ≈92 words → v3 ≈70 words (~24% cut). Lost: "not four independent substrates" (the negation), "additive-genetic variance in overprecision" → "heritable overprecision", "with causal confirmation from" → semicolon. All compressions preserve meaning.
- **Slide 6 caption**: v2 ≈78 words → v3 ≈55 words (~29% cut). Lost: "*PNAS*" citation on Mandel & Barnes; parenthetical for Cohen-Polk-Silli "conviction premium has the same signature in fund returns." The Mandel-&-Barnes-*PNAS* drop is a minor loss of citation precision; everything else is fat.
- **Slide 8 caption**: v2 ≈90 words → v3 ≈65 words (~28% cut). Lost: "in controlled lab conditions", "drawdown stress likely compounds" (speculative — correct to cut), "also falsifiable against a rational-Bayesian-volatility-update account" → "falsifiable against a rational volatility-update account" (tightened). Preserved: propranolol isolation, Yoo BOLD ~60%, all key facts.
- **Slide 10 caption**: v2 ≈110 words → v3 ≈82 words (~25% cut). Lost: "(aggressive counter-positioning)" paren, "Under acute stress, Mobbs' MRI work shows the brain *shifts* from vmPFC cognitive appraisal to PAG reflexive programs" → "Mobbs 2007 *Science*: as threat proximity rises, control hands off from vmPFC appraisal to PAG reflexive programs" (tighter). Added: "(Coates 2009 prenatal-androgen markers, HFT sample, first-generation signal)" as a parenthetical instead of a clause — equally hedged, more compact.

All four captions are materially tighter; no claim lost; minor citations trimmed but not in a way that loses defensibility.

## Did v3 introduce any new issues?

1. **Footer `<div class="hint">` still says "v2" (line 954).** Cosmetic but a real inconsistency — the `<title>` correctly says v3 but the visible footer hint reads "RQS Final · v2". A 5-second edit.

2. **Kandasamy split uses inline styles.** Line 704 applies `style="display:grid; grid-template-columns: 1fr 1fr; gap: 1.2vw;"` to a `.chart-canvas` div. Works, but violates the stylesheet-only pattern used elsewhere in the deck. A clean version would add a `.chart-canvas.split-2` class to the CSS. Very minor.

3. **SCHEMATIC watermark is inconsistent across the deck.** Applied only to hook and Fleming; not to the U-shape, Kepecs, Arnsten, Coates, or HRV charts, which are also schematic. A sharp reviewer could ask why some are badged and others aren't. The critique's reasoning (hook and Fleming are the two most-mistakable-for-real-data) is defensible but not airtight. Low priority.

4. **Print CSS canvas `height: auto !important`.** May cause some browsers to render canvases at intrinsic (zero-or-small) dimensions when printing, depending on how Chart.js leaves the canvas after draw. A safer rule is `max-height: 100vh` or explicit per-chart print heights. Not verified live; flag as a risk rather than a known failure.

5. **Slide 4 caption lost the explicit "not four independent substrates" contrast.** The v2 phrasing "Four **levels of description** of a single stable individual difference — *not four independent substrates*" made the conceptual upgrade explicit. v3 reads "Four **levels of description** of one stable individual difference:" — the same concept but stated positively rather than by contrast. The Slide 3 takeaway still contains "This is not five independent bets on independent hypotheses," so the concept isn't lost from the deck, just from this particular caption. Acceptable. Not a regression.

None of the above is a bug. None is blocking.

## Remaining weaknesses (carried from v2)

Unchanged from v2's remaining-weaknesses list:

1. **NLP validation slide.** Still appendix-only, still a placeholder commitment. The deck still rests on a scalar extracted from text with no in-deck validation pass. This is the biggest latent Q&A risk.
2. **Multiple-comparisons / pre-registration slide.** Still appendix-only.
3. **Backtested Sharpe uplift for rec 2 tail-weighted sizing.** Still a "Before implementation: back-test…" hedge without a number.
4. **Fleming target-r is still baked into the illustrative scatter** (r = 0.50). The SCHEMATIC watermark now mitigates the misread risk, but a sharp viewer can still compute the r from the points. Minor.
5. **The four data-placeholder slides (5, 7, 9, 11) are unchanged.** These are the correct place to be thin given the user is about to add real data slides next — but they remain the weakest slides structurally.

Nothing from the v2 remaining-weaknesses list got worse in v3. The polish-round targeted only presentation polish + 2 citation fixes + 1 accessibility fix + 1 print-CSS fix; all other items were out-of-scope by design.

## Top 3 further changes (if any)

**Ship v3 as-is for this review cycle.** The remaining items either (a) need to wait for the user's data slides, (b) are cosmetic (footer v2→v3, watermark consistency), or (c) are the NLP-validation / multiple-comparisons / backtest items that are bigger than a polish round can address.

If the user wants a 10-minute v3.1 pre-delivery pass, the three smallest high-value edits would be:

1. **Change `<div class="hint">…v2</div>` to `v3`** on line 954.
2. **Apply `.chart-canvas.schematic` to the U-shape, Kepecs, Arnsten, Coates, and HRV canvases** — or don't apply it to any of them — for consistency. (Or introduce a `SIM` badge for those that are theoretical curves rather than schematic reproductions of published data.)
3. **Replace the inline style on Slide 8's split-Kandasamy parent with a CSS class** (`.chart-canvas.split-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 1.2vw; }`) — a one-line stylesheet addition.

None of these is required for delivery. The deck, as v3 stands, will survive the Q&A the v1 critiques set out to prepare it for.

## One-line verdict

**v3 is presentation-grade for a live RQS audience — ship it; the remaining unresolved items are all in the empirical-stack layer the user is adding next, not in the science layer this deck covers.**
