# Graphs Catalog

Every chart proposed for the deck. Three types:
- **E — Empirical** from our own data. Requires reproducible script.
- **C — Canonical** redrawn from a cited paper in deck palette. Source figure must be cited explicitly.
- **S — Schematic** designed by us, no data. Mechanism diagrams, conceptual flows.

Style: no black ink, straight lines (tension: 0), visible dots at every data point, theme palette only. All quantitative numbers from a script, never LLM-estimated.

---

## Main deck graphs (10 slides → ~18 graphs)

### Slide 1 — Hook
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G1.1 | E | Median analyst time-horizon (extracted from notes) 2018–2024, line. Shaded 2022 stress window. | Our analyst-notes corpus |
| G1.2 | E | Bloomberg US Treasury return overlay, same x-axis. Annotation: −12.5% drawdown, worst since 1973. | Bloomberg Treasury index |

### Slide 2 — Thesis
*No graphs — single sentence.*

### Slide 3 — Framework
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G3.1 | S | Tripartite schematic: three experiments → three brain mechanisms → three instruments. Single SVG. | Designed |

### Slide 4 — Analyst confidence heterogeneity (A1a)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G4.1 | E | Per-analyst confidence distributions overlaid (small-multiples or violin). Shows different means/spreads. | Our NLP-extracted confidence series |
| G4.2 | E | Two-panel: left = excess return vs absolute confidence (noisy); right = excess return vs percentile-of-own-confidence (clean). The before/after of normalization. | Our data |

### Slide 5 — Confidence extremes (A1b)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G5.1 | E | Forward excess return by decile of per-analyst confidence percentile. Expected U/J shape. | Our data |
| G5.2 | E | Per-analyst panels (2–3 selected) showing the tail signature is per-individual, not pooling artifact. | Our data |

### Slide 6 — Horizon compression in 2022 (A1c)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G6.1 | E | Per-analyst horizon time-series, 2018–2024, with median bold. Effect is broad. | Our data |
| G6.2 | C | Side panel: Arnsten inverted-U of catecholamines on PFC performance + Kimura cortisol-vs-delay-discounting curve. | Arnsten 2009 NRN; Kimura 2013 |

### Slide 7 — PM trades in volatility (B1)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G7.1 | E | Stress-regime decomposition: performance of further-from-benchmark vs closer-to-benchmark trades, calm vs stress. | Our PM trade data |
| G7.2 | C | Coates & Herbert 2008 cortisol-vs-volatility chart from London trading floor. Redrawn. | Coates & Herbert 2008 PNAS |

### Slide 8 — Market-level read
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G8.1 | S | 4-link micro-to-macro chain: bias → trader behavior → flow → price deviation. Conceptual. | Designed |
| G8.2 | C | Sentiment- or volatility-conditioned anomaly returns (Stambaugh-Yu-Yuan 2012 style) OR 2020 ETF dislocation chart (Haddad-Moreira-Muir 2021). | One of those papers |

### Slide 9 — What to do
| ID | Type | Description | Source |
|----|------|-------------|--------|
| G9.1 | S | Dashboard mockup: per-analyst confidence-percentile strip. | Designed |
| G9.2 | S | Stress-window decision-protocol flowchart. | Designed |

### Slide 10 — Close
*No graph.*

---

## Appendix graphs (canonical literature redraws + science depth)

These give the appendix its weight. Each is a single-slide deep-dive.

### Metacognition / aPFC
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP1 | C | Fleming 2010 *Science* — right anterior PFC grey-matter volume vs metacognitive accuracy scatter. | Fleming et al. 2010 |
| AP2 | C | Kepecs 2008 *Nature* — orbitofrontal "X-pattern" confidence cells across choice difficulty. | Kepecs et al. 2008 |
| AP3 | C | Lak 2014 *Neuron* — OFC inactivation effect on confidence-driven behavior. | Lak et al. 2014 |
| AP4 | E | Loughran-McDonald-style validation: our LLM confidence score vs human-rated confidence on a sample. | Our NLP validation |

### Confidence extremes / expert calibration
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP5 | C | Murphy & Winkler weather-forecaster calibration curve. | Murphy & Winkler 1984 |
| AP6 | C | Tetlock superforecasters Brier score distribution. | Tetlock & Gardner |
| AP7 | C | Cremers & Petajisto Active Share vs alpha. | Cremers & Petajisto 2009 RFS |
| AP8 | C | Pouget-Drugowitsch-Kepecs schematic: confidence vs certainty distinction. | Pouget et al. 2016 Nat Neuro |

### Stress / cortisol / horizon
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP9 | C | Benartzi & Thaler myopic loss aversion: utility-as-a-function-of-evaluation-horizon. | Benartzi & Thaler 1995 |
| AP10 | C | De Martino 2006 amygdala framing fMRI activation. | De Martino et al. 2006 Science |
| AP11 | C | Schwabe & Wolf 2009 — propranolol blocks goal-to-habit shift. Causal mechanism. | Schwabe & Wolf 2009 J Neurosci |
| AP12 | E | Robustness: same horizon-compression analysis across 2008, 2013, 2020, 2022 stress windows. | Our data |

### Fight/flight neuroanatomy
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP13 | S | PAG four-column functional anatomy diagram (Bandler & Shipley). | Designed from BS 1994 |
| AP14 | C | Mobbs 2007 *Science* — vmPFC → PAG transition as threat proximity increases. | Mobbs et al. 2007 |
| AP15 | C | Coates & Herbert 2008 morning-testosterone-vs-daily-P&L. | Coates & Herbert 2008 PNAS |
| AP16 | C | Kandasamy 2014 — risk premium collapse with 8-day cortisol dosing. | Kandasamy et al. 2014 PNAS |

### Market-level psychology
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP17 | C | Baker-Wurgler sentiment index time series with anomaly returns overlay. | Baker & Wurgler 2006/2007 |
| AP18 | C | Brunnermeier-Pedersen funding-liquidity spiral schematic. | BP 2009 RFS |
| AP19 | C | Greenwood-Hanson credit-issuer-quality vs forward credit returns. | GH 2013 |
| AP20 | C | Haddad-Moreira-Muir 2020 ETF dislocation event-study chart. | HMM 2021 |
| AP21 | E | Our 2022 case-study: spread/yield trajectories in segments where PM positioning was concentrated. | Our PM holdings + market data |

### Debiasing
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP22 | C | Morewedge 2015 effect-size bar chart — bias reduction immediate vs 8-12 week. | Morewedge et al. 2015 |
| AP23 | C | Haynes 2009 surgical checklist mortality reduction. | Haynes et al. 2009 NEJM |
| AP24 | C | Scopelliti 2015 — bias-blind-spot score moderates training effect. | Scopelliti et al. 2015 Mgt Sci |

### Computational neuroscience (pending agent return)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP25 | C | Drift diffusion confidence schematic — extreme posteriors arise from clean accumulation. | Pleskac & Busemeyer 2010 |
| AP26 | C | Hierarchical Gaussian Filter trajectory under volatile environment. | Mathys et al. 2011 |
| AP27 | C | Free-energy schematic — surprise + complexity. | Friston 2010 NRN |

### Network neuroscience (pending agent return)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP28 | C | Hermans 2011 *Science* — salience network activation under acute stress, executive network suppression. | Hermans et al. 2011 |
| AP29 | C | HRV-vs-cognitive-flexibility scatter (Thayer & Lane lineage). | Thayer & Lane 2000 / Thayer 2009 |
| AP30 | S | DMN / Salience / CEN tripartite schematic with stress-induced reconfiguration arrows. | Designed |

### Endocrinology / individual differences (pending agent return)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP31 | C | Coates 2009 *PNAS* 2D:4D vs trader profitability. | Coates et al. 2009 |
| AP32 | C | MR-vs-GR cortisol-binding curves at basal vs stress concentrations. | de Kloet et al. 2005 NRN |
| AP33 | C | Cortisol awakening response distribution and stability. | Stalder & Kirschbaum |

### Evolutionary origins (pending agent return)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP34 | C | Johnson & Fowler 2011 *Nature* — adaptive overconfidence phase diagram. | JF 2011 |
| AP35 | C | Bikhchandani-Hirshleifer-Welch information cascade timeline. | BHW 1992 JPE |

### Chronobiology / sleep (pending agent return)
| ID | Type | Description | Source |
|----|------|-------------|--------|
| AP36 | C | Yoo 2007 *Nat Neuro* — amygdala-PFC functional connectivity sleep-vs-rested. | Yoo et al. 2007 |
| AP37 | C | Kamstra-Kramer-Levi DST market-return anomaly. | KKL 2000 AER |
| AP38 | C | Cortisol diurnal curve with cognitive-performance overlay. | Schmidt et al. 2007 |

---

## Production order (priority)
1. **Empirical from our data** — these need scripts and are the highest-credibility content. Cannot proceed without user data and a confirmed analysis spec.
2. **Schematics** — designed by us, no external dependencies. Can produce now in mockup form.
3. **Canonical redraws** — find source figure, extract data points (digitize if needed), redraw in deck palette with explicit citation. Each must list page/figure number for provenance.

## Open questions for user before production
- Slide format: HTML deck, PowerPoint, or PDF? Affects chart-library choice (D3/Chart.js vs python-pptx vs matplotlib).
- Color palette: any Capital Group / RQS brand colors to honor? Default: muted, no-black, theme-coherent.
- Deadline: drives how many appendix charts get fully produced vs. spec-only.