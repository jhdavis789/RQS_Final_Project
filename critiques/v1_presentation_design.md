# Presentation Design Critique — Deck v1

Reviewer posture: senior presentation-design reviewer. Benchmark: Rockefeller/CSH biomedical talk pitched to a hedge fund audience. The deck is ambitious, the palette is disciplined, the science is real. What's keeping it from the benchmark is an inconsistent pacing pattern, one structurally wrong slide (the framework matrix), captions that are reading assignments rather than speaker supports, and one visible HTML bug on the recommendations slide.

---

## First impressions on opening the deck

The palette is the right palette — warm paper-white (`#f5f1e8`), muted primary blue, terracotta accent, no black ink. That reads as *Cabinet* or *PNAS*-cover, not as investment-committee PowerPoint. Good.

Within ~15 seconds of flipping through, three things register:

1. **The science is dense and the speaker is doing real work.** This is not a consultant deck.
2. **The pacing is uneven.** 14 slides, but the cognitive load is front-loaded: slides 3, 4, 6, 8, 10, 12 are all "read me for a minute" slides, and the four placeholder slides disrupt the rhythm without earning their keep.
3. **There is no "big number" in the hook to make the audience lean forward.** There are four big numbers, which is three too many.

Overall: B+ on craft, B− on flow. It is recoverable with 6–8 targeted edits rather than a rebuild.

---

## Argument arc

The intended arc is: hook → thesis → framework → three science/data pairs → brain-state + biomarkers → recommendations → close. On paper this is clean.

**Where it lands:** the thesis on slide 2 is *good* — declarative, one sentence, the right sentence. The A1a → A1b → A1c chain (confidence heterogeneity → tail signal → stress collapse) is exactly the right ladder: it starts with a definitional argument (you *must* normalize per-analyst), then a mathematical argument (the tails are a theorem), then a mechanistic-causal argument (cortisol does it to you in a lab). Each step earns the next. The B1 slide (PM fight/flight/freeze) is the strongest single slide in the deck — the PAG SVG is doing real communicative work.

**Where it sags:**
- **Slide 3 (framework).** The 3×6 convergence matrix is information-dense but reads as wallpaper. Eighteen micro-cells of 11.5px text is not a chart; it's a screenshot of a spreadsheet. The audience cannot read it and listen at the same time, so they do neither.
- **Slides 5, 7, 9, 11 (data placeholders).** A placeholder box saying "charts to paste here" is honest but *cannot be in a presentation version*. It's OK while the deck is under construction; it is not OK for a review reader. They break the rhythm and they break the promise of the paired-slide structure, because the pair currently reads as "science slide, then apology."
- **Slide 12 (brain-state + biomarkers).** Unpaired — there is no corresponding data slide. After four science/data pairs, the reader has been trained to expect one more. Breaking that pattern here is a flow mistake, or at minimum should be labeled differently.

**Where it rushes:**
- The market-level slide (exec summary slide 9 — aggregation, limits of arbitrage, Adaptive Markets) has been **cut entirely** from the deck. This is a defensible cut for length but it removes the micro-to-macro bridge. The recommendations then feel like they hop from "individuals have stress biology" to "therefore build these four instruments" without the "…and stress biology aggregates into mispricing" beat that explains why RQS should care institutionally.

**Count mismatch.** The close slide asserts "Five disciplines converge" but the framework matrix shows six (it adds Chrono/Sleep). Pick one number and repeat it everywhere — "five" is already the canonical line in `TAKEAWAYS.md` #3 and #4.

---

## Slide-by-slide review

**Slide 1 (Hook).** The 42px quote is good copy but the four-stat-block row under it dilutes the punch. A true hook has one number or one image. Four stats makes the audience triage. Worse: the two "worst since" stats (1973 and 1754) compete with each other — one of them must go. The –39% long-zero stat is the one nobody has heard; keep that, cut the –12.5% Treasury stat, and let the chart (currently missing entirely) do the work. As currently built this slide violates its own exec-summary spec, which called for G1.1 (median analyst horizon) + G1.2 (Bloomberg Treasury return). The chart is the hook, not the quote.

**Slide 2 (Thesis).** The sentence is right. The subtext paragraph is half a step too long — "The frame is not… The frame is…" is a good device but it runs on into "Process beats self-awareness — especially under stress, especially in experts," which is a *different* thesis (it belongs on the recommendations slide). Trim the subtext to just the "measure the bias, build the tool, absorb the bias as a design parameter" line. One sentence, then let it breathe.

**Slide 3 (Framework).** **This is the biggest design problem in the deck.** A 3×6 grid with 18 evidence cells of ~6–10 words each is illegible from the back of a room, and illegible in review printout. It looks like evidence but functions as decoration. Three fixes in order of invasiveness: (a) cut to 3×3 (three experiments × three disciplines: neuro, endo, compute) and put the other three in a micro-caption "also predicted by evolutionary, psychology, chrono"; (b) replace with a single-axis horizontal stacked bar ("each finding, N disciplines predicting it"); (c) replace with a schematic diagram — three experiment nodes, each with radiating discipline tags, visual density without forcing 18 reading tasks. Option (c) was actually what `GRAPHS.md` G3.1 specified ("Single tripartite schematic") and what the deck abandoned in favor of a matrix. **Go back to the schematic.**

**Slide 4 (A1a science).** Strong. Fleming scatter + per-analyst distributions is the right pairing. The caption is four parallel claims (genetic / neuroanatomical / linguistic / computational) and that works. Watch the `r ≈ 0.46` in the Fleming subtitle — the original paper reports r = 0.54 for right-lateral aPFC volume vs meta-d′ (Fleming 2010 Fig. 1) — confirm the exact number from the source before anyone in the audience does. Also: the scatter is labelled "Illustrative scatter fit to published summary statistics" which is honest but weak; for a Rockefeller-standard talk, *digitize the real scatter* and cite it properly.

**Slide 5 (A1a data).** Placeholder. Fine while the deck is being built, but the placeholder hint text is actually useful — when the data slide is produced, transcribe the three bullets into actual caption lines and keep the *structure* of this placeholder as the design template. Don't just paste charts in and delete the scaffolding.

**Slide 6 (A1b science).** Strongest science slide after B1. The DDM decile plot and the Kepecs X-pattern together is a tight pair. One suggestion: the DDM curve currently simulates 50,000 samples with `d=0.9` — for a 2AFC at d=0.9 you get a monotonically increasing accuracy-vs-confidence curve, not a U. *That's because this is a binned-by-confidence accuracy plot — what the audience is expected to see as "U-shape" in your empirical slide is actually forward-excess-return vs confidence percentile, a different quantity.* The current chart is labeled "U-shape" in the slide headline but the rendered curve will be monotonic. This is a headline/chart mismatch. Either (a) relabel the chart "Accuracy rises monotonically with confidence under DDM — and the empirical U comes from the interaction with *economic value* at extremes" and caption accordingly, or (b) generate the actual Sanders-Hangya-Kepecs prediction which is accuracy-vs-confidence under *variable difficulty*, which does give the U. The current plot is technically a lie-by-label.

**Slide 7 (A1b data).** Placeholder. Same note as slide 5.

**Slide 8 (A1c science).** Arnsten inverted-U + Kandasamy bar chart. The Kandasamy chart is the single most quantitative piece of cross-disciplinary evidence in the whole deck (α 0.50 → 0.35, risk premium 1.00 → 0.56), and this is the right place to put it. The Arnsten inverted-U is illustrative and fine. The caption ties four disciplines (endo, cellular, computational, sleep) — good parallel structure. The takeaway ("the 2022 analyst note is a non-invasive biomarker of an HPA episode") is in your top-3 punchlines and it lands here.

**Slide 9 (A1c data).** Placeholder.

**Slide 10 (B1 science).** Best slide. The PAG four-column SVG + Coates cortisol-vs-vol pairing *earns* its density. The diagram teaches (fight/flight/freeze mapped to specific PAG columns, each mapped to a PM behavior) in a way a quant audience will remember. The 2D:4D R²=0.55 line in the caption is a standalone Whoa-moment. Keep as is.

**Slide 11 (B1 data).** Placeholder.

**Slide 12 (Brain-state + biomarkers).** Hermans SVG + HRV curve. The Hermans "salience hijack" split-panel SVG is well-designed — calm vs stress side-by-side is exactly how you want to teach a network-state switch. The HRV curve is weaker; it's a saturating curve with fake scatter overlay and reads as decorative. Either replace with a real Thayer figure or cut the scatter overlay and let the curve be the schematic it is. **Flow problem:** this slide has no data-pair partner, which breaks the rhythm. Either add a paired slide (hardest) or give it an explicit header tag ("Instrumentation — bridging slide") so the audience doesn't expect a data twin.

**Slide 13 (Recommendations).** Four rec-cards in a 2×2 grid. The count is right. The format — eyebrow + headline + ~4-line body — is right. **There is an HTML bug on line 753:** the `eyebrow` div closes with `</h2>` rather than `</div>`, which will either break the DOM or render as a stray h2. Fix before anyone sees this. Content: rec 3 tries to cite two experiments and a separate literature at once ("From A1c + B1 + debiasing lit.") — that's three citations in one tag, which reads as over-stuffing. Tighten to "From A1c + B1." Rec 4 (sleep policy) is the strongest content card but it's visually identical to the others; consider giving it a subtle emphasis (slightly darker border, or a "highest leverage" micro-label) to match the caption claim.

**Slide 14 (Close).** "Three biases. *Five disciplines converge.* Four instruments. Measure → instrument → decide." This is the right close line and it's the one from `TAKEAWAYS.md` #33. But: the framework slide shows six disciplines, not five. Pick. The "Appendix follows" line at the bottom is appropriate for a review reader but distracts on a live delivery — consider hiding with a `@media` query or just deleting it.

---

## Chart-by-chart review

**ch-fleming (Slide 4).** Simulated scatter fit to r=0.46, N=32. Legible. Axis labels correct. Dashed line for the fit is the right convention. Weakness: it is illustrative not empirical; a real Fleming 2010 Fig. 1 digitization would strengthen. Also: `pointRadius: 5` is fine at presentation size but at back-of-room reading the points will look like dots of noise; consider 6–7 for 32 points.

**ch-analyst-dists (Slide 4).** Three Gaussians overlaid at mu 0.35/0.50/0.72. Good pedagogically: the means are visibly different, the spreads are visibly different. The legend labels ("high-hedging", "middle", "assertive") are doing the work. One critique: the y-axis title "Density" is technically correct but unhelpful; change to "Frequency of confidence scores" for an audience that may not read PDFs for fun.

**ch-ddm (Slide 6).** *Problem.* This is the most important chart in the "tails are signal" argument, and as currently rendered it will show monotonically increasing accuracy with confidence decile — which is *not* a U. The narration of "U-shape" will contradict the plot. Either re-simulate with a variable-difficulty mixture (standard Sanders 2016 setup) which produces the U, or relabel the chart and stop calling it a U-shape. See slide-6 notes above. **Fix before a technical audience sees this.**

**ch-kepecs (Slide 6).** Four difficulty bins, correct vs error firing rates, with the crossover at Hard. This is a legit redraw of Kepecs 2008 Fig. 3 in cartoon form. Dashed line for error trials is a standard convention and reads correctly. Good.

**ch-arnsten (Slide 8).** Inverted-U with two vertical reference lines (optimum, acute stress). Clean. The two vertical lines at x=1.7 and x=3.2 are doing real pedagogical work — annotate them on the chart with a small text label ("Optimal" / "Acute stress") rather than relying on the legend, which will be read separately.

**ch-kandasamy (Slide 8).** Dual-axis bar chart: utility α on left, risk-premium relative on right. This is *the* quantitative chart in the deck. Two critiques: (a) dual-axis bar charts are a known hazard — readers conflate bar heights that live on different scales; consider showing the same data as two small charts side-by-side (α over time, risk premium over time) rather than dual-axis. (b) There are only three x categories (Placebo, Day 1, Day 8) which makes the "decline" feel jagged rather than monotone; if you have the Day-2 through Day-7 intermediate values from Kandasamy 2014 SI, add them as a line and let the trend speak.

**ch-coates (Slide 10).** Eight-day panel with two lines (cortisol, implied vol). Good pair; dashed secondary is a standard convention. The numbers are flagged "illustrative" and are made up. For a Rockefeller-standard talk, **the real data are in Coates & Herbert 2008 Fig. 1 and should be digitized.** "Illustrative" is a red-flag word for a skeptical quant audience — they will ask where the numbers came from.

**ch-pag SVG (Slide 10).** Excellent. The PFC (inhibited, dashed) → Amygdala/Hypothalamus (active) → four PAG columns with behavior labels is a single diagram that *teaches*. The bottom annotation ("PM equivalent: Fight = active-risk-up · Flight = benchmark-hug · Freeze = no-trade") is the cleverest single line in the deck because it ties the anatomy to the finance in one line. Keep as is. Minor: the arrow from PFC→Amygdala reads as "PFC excites amygdala" when the inhibit semantics are carried by the dashed style — strengthen with an explicit ⊣ inhibit-bar head rather than an arrowhead on the `arrow-inhibit` class.

**ch-hermans SVG (Slide 12).** Good split-panel calm vs stress. Three critiques: (a) the "propranolol BLOCKS / cortisol does NOT" annotation on the stress side is crucial content but buried in 9.5px label-sm text; enlarge to 11px. (b) The CEN circle on the stress side is smaller than on the calm side, which teaches "CEN is suppressed" visually — good design. (c) The dashed vertical divider is doing quiet but useful work.

**ch-hrv (Slide 12).** Weakest chart in the deck. A saturating curve with fake scatter points on top reads as "we want a curve to exist." Either digitize a real Thayer 2009 figure, or drop the scatter and make it a pure schematic with no data claims.

---

## Visual design & typography

**Palette.** The warm paper background (`#f5f1e8`), muted primary (`#1a5490`), and the five accent colors are *correct* for the Rockefeller standard. This is closer to a *Nature* or *PNAS* style than to a bank deck. Do not change.

**Typography.** The hierarchy `eyebrow (13px caps) → h2 (28px) → chart-title (14px) → chart-subtitle (12px italic) → caption (15px) → takeaway (17px)` is well-considered. The takeaway box (pale-blue-tint background with 3px left border) is compelling on first appearance but by slide 13 the reader has seen the treatment seven times and it starts to feel like a template. Consider varying — on one or two slides, put the takeaway *in the headline* (no box) and remove the box; let the design breathe.

**Density.** Captions are paragraphs of 4 parallel bolded claims. This is the correct *speaker-support* density for a slow walkthrough, but it is too dense for an audience reading from the back. If the speaker is narrating, these captions function as cue cards, which is OK; if this is being shared as a read-alone PDF, the captions need to shrink by ~30% or be split into visible sub-bullets with whitespace.

**Rule lines and borders.** The 1px `--rule` borders at header/footer are appropriate and quiet. The `border-left: 3px solid var(--accent-2)` on evidence cells and rec cards is a strong identity element.

**Whitespace.** Adequate on 4K displays at 1920×1080. On a projector at 1024×768 the framework-slide matrix will overflow — test at that resolution.

**Consistency bugs.** (a) The hook slide uses `stat-number 36px` while the thesis slide uses `h1 56px`, which creates a visual dropoff — the hook feels lighter than the thesis even though it's supposed to carry more weight. (b) The `.eyebrow` color is `--accent-1` (terracotta) everywhere except the recommendations slide, where rec-num uses `--accent-2` (teal) — pick one. (c) The `slide-header` border-bottom is inconsistent in bottom-padding between slides because `padding-bottom: 1vh` varies with viewport height.

---

## Website / code setup

**CSS.** Clean, scoped, uses CSS custom properties throughout. Viewport-relative units (`vh`/`vw`) are appropriate for a presentation but will cause text to micro-scale differently across monitors — that's a conscious tradeoff.

**JS / Chart.js.** 
- Global defaults correctly set `tension: 0`, visible points, no animation, no tooltip. Matches project rules.
- All `Chart` instantiations wrap in IIFEs so no scope leakage. Good.
- Deterministic PRNGs (`mulberry32`) with seeds so charts are reproducible across reloads. **This is nice craft.**
- Two SVG charts (`ch-pag`, `ch-hermans`) inject innerHTML — OK because no user input, but if this were ever hosted with user-supplied content it would need sanitization.

**Bugs found.**
1. **Slide 13, line 753:** `<div class="eyebrow">Four instruments grounded in peer-reviewed mechanism <i>and</i> our own data</h2>` — the `eyebrow` div closes with `</h2>`. This will either break rendering or produce a stray closing h2. **Fix immediately.**
2. **Slide 3 takeaway:** "five independent peer-reviewed disciplines" but the grid shows six. Language/data mismatch.
3. **Slide 6:** The DDM chart rendered by current code is *monotonic*, not *U-shaped* — contradicts the slide headline. See chart review.
4. **Stat provenance on Slide 1:** "−39% long zeros · worst since 1754" — this is a widely-cited stat but its provenance is Bank of America / Deutsche Bank strategist notes (Jim Reid), not a peer-reviewed source. For a Rockefeller-standard talk, either cite the exact BoA/DB note or drop the "since 1754" claim. Same with "−12.5% worst since 1973" — give the exact Bloomberg Treasury Index name (presumably `LBUSTRUU` or similar).
5. The `click` handler advances the deck on *any* non-excluded click. If a reviewer clicks an empty area to see the next slide, that's intended; if they click while trying to select caption text to quote, that's disruptive. Consider restricting to arrow-key nav only for the shared version.

**Keyboard nav.** ←/→, Space, PageUp/Down, Home/End, F for fullscreen, 0–9 for direct slide access (1-9 maps to 1-9, 0 maps to slide 10). Slides 11-14 are unreachable by number key — document this or add Shift-N.

**Print / PDF.** There is a `@media print` block but it only sets `display: flex` and `page-break-after: always`. Chart.js renders into a canvas at fixed pixel dimensions; on print, canvases will either (a) scale to the page and lose resolution, or (b) render at screen-pixel size and get cropped. **Neither is acceptable for a PDF-distributed deck.** To fix: either (a) set `devicePixelRatio: 2` on chart creation and a fixed print canvas size, or (b) for the print-to-PDF export, screenshot each slide at 2× resolution and embed as PNG. This matters because any reviewer who receives this via email will try to print-to-PDF and see broken charts.

**Responsive behavior.** `width: 100vw; height: 100vh; overflow: hidden` means at narrow viewports everything cramps uniformly. There's no mobile breakpoint, which is fine for a presentation tool but the framework matrix at <1200px width will wrap and look broken.

**Accessibility.**
- Contrast: `#5a5550` on `#f5f1e8` is ~6.8:1 — passes AA. `#95908a` (muted) on bg is ~3.2:1 — fails AA for body text; currently only used in very small labels, borderline acceptable.
- Alt-text: none. The two SVG schematics (PAG, Hermans) communicate meaningful content but have no `<title>` / `<desc>` elements. Add for keyboard / screenreader users.
- Focus states: the click-to-advance handler means keyboard-only users can navigate fine with arrows, but there is no visible focus indicator on anything. For an RQS audience this is fine; for a wider audience it isn't.
- No `prefers-reduced-motion` query, but `Chart.defaults.animation = false` effectively handles this.

---

## Top 10 specific, actionable changes (ranked by impact)

1. **Slide 3 — replace matrix with schematic.** Kill the 3×6 grid of micro-text. Replace with a node diagram: three experiment nodes on a horizontal axis, each with 3–5 radiating discipline tags. Aim for information density through *shape recognition* not text-reading. This alone will move the slide from B− to A−.

2. **Slide 13 — fix HTML bug on line 753.** `</h2>` should be `</div>`. Trivial fix, but the DOM is currently invalid. While you're there, drop "+ debiasing lit." from rec 3's citation tag.

3. **Slide 6 — regenerate the DDM chart to match the headline.** The current simulation produces a monotonic accuracy curve but the slide headline says "U-shape is a theorem." Use a variable-difficulty mixture (Sanders 2016 setup: stimulus strength drawn from a distribution, accuracy binned by confidence |x|) to produce the actual U. Or change the headline. Either way, don't ship a plot that contradicts its own title.

4. **Slide 1 — add the chart, cut two stats.** The exec summary called for G1.1 (analyst horizon time-series) + G1.2 (Treasury return overlay) and the deck dropped both in favor of a stat row. Put the chart back. Keep one or two stats (the −39% and +425 bp if you want high-drama; the −12.5% is redundant with the −39%). Stats compete with each other for attention — pick fewer, make them bigger.

5. **Framework matrix / close slide — decide on 5 or 6 disciplines and be consistent.** Close slide says "Five disciplines converge"; slide 3 shows six. `TAKEAWAYS.md` #3 says five. Either drop Chrono/Sleep from the matrix and keep it in the caption, or update the close slide to six. This is an auditable inconsistency that a sharp quant reviewer will flag.

6. **Placeholder slides (5, 7, 9, 11) — either produce the data now, or mark them clearly as "skipped for review."** As they currently appear (dashed-border box with "Paste here"), a review reader's eye stops dead four times in 14 slides. If the data is genuinely not yet available, consider replacing each placeholder with an empirical chart spec (axis labels, expected shape, a stylized "this is what we expect" curve) — that's more useful feedback fodder than a dashed box.

7. **Slide 8 — replace Kandasamy dual-axis bars with two side-by-side single-axis charts.** Dual-axis bar charts are read wrong by ~30% of quant audiences (comparing bar heights across different scales). Two small charts, same data, side by side, with shared x-axis of [Placebo, Day 1, Day 8].

8. **Captions — compress by 25–30%.** Every mechanism caption on slides 4/6/8/10/12 is four parallel bolded claims of 2–3 lines each. Cut the filler phrase "four independent substrates" on slide 4, "four independent lines of evidence" on slide 6, etc. The *structure* of parallel bolded claims works; the preamble to each one wastes a line.

9. **Chart source lines — stop saying "illustrative."** Slides 4 (Fleming), 6 (Kepecs), 8 (Arnsten), 10 (Coates), 12 (HRV) all have the word "Illustrative" in the source line. For a Rockefeller-standard talk, digitize real figure data or remove the claim. "Illustrative" is a red flag to a quant audience that will read it as "we made up the numbers."

10. **Print CSS — make the deck survive being exported to PDF.** Add a `@media print` block that sets canvas sizes explicitly (e.g. 1200×700) and sets `devicePixelRatio: 2`. Test by printing to PDF and checking each chart. Half the distribution path for this deck will be PDF email attachments.

---

## What to ADD

- A **reinstated market-level slide** between slides 12 and 13 — the "individual stress biology aggregates into market mispricing" beat. This is exec-summary slide 9, currently cut. Without it, the recommendations hang on individual-level evidence only. One slide with the Haddad-Moreira-Muir 2020 ETF dislocation chart (or Stambaugh-Yu-Yuan sentiment anomaly) is enough.
- **Real Fleming 2010 digitization** on slide 4 instead of the r=0.46 simulated scatter.
- **A 1-slide Q&A prep summary** at the end of the main deck (or as appendix slide A0) listing the five most-likely objections and the response line from `TAKEAWAYS.md` Q&A section. Speaker safety net.
- **Slide numbers in a persistent corner, not just the header.** The header reads "05 / 14" but disappears when the audience stops looking up — a thin progress bar at the bottom would help.

## What to CUT

- **Framework matrix in its current form.** See change #1.
- **Two of the four hook stats.** See change #4.
- **The thesis-slide second sentence starting "Process beats self-awareness…"** It belongs on slide 13, not slide 2.
- **The "Appendix follows" line on slide 14** for live delivery (keep for review version).

## What to SPLIT or MERGE

- **Merge the four placeholder slides with their science partners** where the data chart is small enough to fit (option A: reduce science-slide caption, add one empirical thumbnail on the right). This cuts four slides and tightens the deck from 14 → 10, closer to the OUTLINE.md's stated 10–12 target. Alternative option B: keep the pairs but make the data slide carry its own science sidebar so they're mirror-images of each other, not "science + apology."
- **Split slide 12** into (a) "whole-brain reconfiguration" (Hermans SVG + one sentence) and (b) "measurable in real time — wearables" (HRV + pupil + research-gap callout). Currently one slide trying to make two arguments.

---

## One-line verdict

**A real Rockefeller-standard talk trapped inside a framework-matrix slide, four placeholder slides, and one HTML bug — fix those three things and this deck is ready for RQS.**
