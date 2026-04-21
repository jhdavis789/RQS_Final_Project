# Market-Level Psychology — Deep Research

## Executive one-liner
Individual behavioral biases do not cancel in the aggregate; limits of arbitrage, noise-trader risk, reputational herding, and intermediary capital frictions let them aggregate into *persistent, measurable mispricing* — and in fixed income the transmission channel runs through dealer balance sheets, leverage, and flight-to-quality dynamics that a Risk and Quantitative Services audience recognizes from their own crisis playbooks.

---

## The micro-to-macro story

The chain has four links, each with a specific literature attached.

1. **Individual bias.** Under acute stress the decision-maker's prefrontal cortex attenuates and control migrates to amygdalar/striatal circuitry (Arnsten 2009; Schwabe & Wolf 2013). Cortisol lengthens subjective delay discounting (Kimura et al. 2013) and testosterone feedback amplifies prior wins into escalating risk appetite (Coates & Herbert 2008). The individual output is a distribution of decisions that is *systematically biased*, not merely noisy.

2. **Trader behavior.** Those biased decisions produce directional order flow — loss-averse selling on the way down, momentum-chasing on the way up, horizon compression during drawdowns. Lo & Repin (2002) measured the autonomic signature of these decisions in real-time in ten professional traders and found significant skin-conductance and cardiovascular shifts during transient market events and high-volatility periods, with effect size related to trader experience.

3. **Aggregate flow.** When traders are correlated in disposition (same news shock, same institutional incentives, same career-risk worries), their order flow is correlated. Scharfstein & Stein (1990) show *reputational* herding: a manager who fears being wrong alone behaves differently from one who fears being wrong with the crowd, and the crowd-aligned strategy dominates when skill is hard to assess. Sias (2004) documents quarter-to-quarter correlation in institutional demand that is not explained by momentum trading, consistent with information inference from peers' trades. DeLong, Shleifer, Summers & Waldmann (1990) supply the theoretical micro-foundation: unpredictable sentiment *is itself a risk* that deters rational counter-trades.

4. **Price deviation.** The flow moves prices away from fundamentals, and the deviation persists because the mechanism that should fix it — specialized arbitrage capital — is impaired precisely when the mispricing is greatest. That is Shleifer & Vishny (1997). In fixed income the same mechanism runs through dealer balance sheets (Adrian, Etula & Muir 2014; He & Krishnamurthy 2013), repo funding (Brunnermeier & Pedersen 2009), and the speed at which cross-sectional capital can reach the dislocated trade (Duffie 2010).

Each link is empirically documented. The chain, assembled, is the answer to the presenter's question.

---

## Limits of arbitrage — why psychology persists in prices

Shleifer & Vishny (1997) is the foundation. Their argument: textbook arbitrage is riskless and capital-free, but *professional* arbitrage is done by specialists using other people's capital. Those specialists face performance-based withdrawal risk. When mispricing widens before it converges — the noise-trader risk of DeLong et al. (1990) — the arbitrageur's mark-to-market deteriorates, clients pull capital, and the arbitrageur is forced to *liquidate* at the moment convergence was closest. Performance-based arbitrage is "particularly ineffective in extreme circumstances" — the paper's single most-cited sentence.

For fixed income the modern formalization is **intermediary asset pricing**. He & Krishnamurthy (2013 AER) model risk premia when the marginal investor is a constrained intermediary; premia rise nonlinearly as the capital constraint binds, matching observed crisis spike-and-reversion patterns. Adrian, Etula & Muir (2014 JF) construct a single-factor SDF from broker-dealer *leverage* innovations that prices size, B/M, momentum, *and bond portfolios* with R² = 77% — a result that directly speaks to an RQS audience because it says the stochastic discount factor in bond markets is empirically about dealer balance-sheet state, not representative-agent preferences.

Brunnermeier & Pedersen (2009) closes the loop with the *liquidity spiral*: margins depend on volatility, volatility spikes reduce funding, reduced funding forces selling, selling raises volatility. The spiral is a structural amplifier of any initial behavioral shock. Critically for a bond-market audience, the model *predicts* commonality in liquidity across securities, sudden dry-ups, and flight to quality — the exact pattern observed in Treasuries in March 2020 and, at lower intensity, October 2022.

Duffie's 2010 AFA presidential address adds the time dimension: capital is *slow-moving* to dislocated trades because search costs, mandate constraints, and capital-raising frictions limit how fast corrective flow arrives. The signature is a sharp price reaction followed by an extended reversal — observable in basis trades, swap spreads, Treasury-futures basis, and on-the-run/off-the-run spreads.

---

## Noise trader risk and sentiment

DeLong, Shleifer, Summers & Waldmann (1990 *JPE*) is the theoretical spine. In an overlapping-generations model with irrational noise traders whose beliefs vary stochastically, arbitrageurs face a new risk — the *future sentiment of noise traders* — that is uncorrelated with fundamentals and therefore unhedgeable. Arbitrage is dampened, noise traders can earn higher returns by bearing the risk they themselves create, and prices diverge from fundamentals *without any fundamental risk being present*. Sentiment is priced.

Baker & Wurgler (2006 *JF*) operationalize this empirically with a composite sentiment index (closed-end fund discount, IPO volume, IPO first-day returns, share of equity in new issues, NYSE turnover, dividend premium). They show that when sentiment is high, *hard-to-value, hard-to-arbitrage* stocks — small, young, volatile, unprofitable, non-dividend-paying, extreme growth, distressed — earn low subsequent returns; when sentiment is low, these same stocks earn high subsequent returns. The 2007 JEP follow-up generalizes the framework. This is the cleanest cross-sectional test of the sentiment-pricing channel in existence.

Stambaugh, Yu & Yuan (2012 *JFE*) sharpen it further. They examine 11 well-known anomalies and find each is *stronger* following high sentiment, with all of the marginal profitability concentrated on the *short leg*. Short-sale constraints prevent arbitrageurs from correcting overpricing, and sentiment moves overpricing more than underpricing. Implication for bond PMs: behavioral pricing errors are *asymmetric* — over-optimism is harder to arbitrage than over-pessimism because shorting credit is capital-intensive and path-dependent.

---

## Herding and reputational dynamics

Scharfstein & Stein (1990) build the reputational-herding model. A manager's perceived skill is inferred jointly from outcome *and* from whether peers made the same call. When all peers are wrong together, the signal-to-noise on any individual's skill is poor, so being-wrong-with-the-crowd is less career-damaging than being-wrong-alone. The equilibrium: managers rationally *discard* their private signal and follow the consensus. Note the word — *rationally*. Herding in this model is not irrationality; it is a rational response to a career-compensation structure. That is the version that survives scrutiny in an RQS audience.

Devenow & Welch (1996 *European Economic Review*) survey the broader taxonomy: information cascades (Bikhchandani-Hirshleifer-Welch 1992), reputational herding, and compensation-based herding. Each has different implications for how to detect it and how to arbitrage against it.

Sias (2004 *RFS*) gives the empirical read for institutional investors: cross-sectional correlation in quarter-to-quarter changes in institutional demand is 0.4+, not attributable to momentum trading. Most consistent with institutions *inferring information from each other's trades* — which, combined with the Shleifer-Vishny capital constraint, means herding *amplifies* behavioral mispricing rather than damping it.

The fixed-income relevance is direct: credit PMs share benchmarks, rating constraints, mandate constraints, and peer-comparison pressure. The reputational-herding equilibrium is the *default state* of credit asset management, not an aberration.

---

## The endocrine trading floor — Coates' aggregation argument

Coates & Herbert (2008 *PNAS*) measured morning and afternoon cortisol and testosterone in 17 male traders on a London high-frequency-trading floor for 8 consecutive business days, alongside their real P&L. Two primary findings:

1. *Morning testosterone predicted that day's P&L.* Fourteen of 17 traders had higher P&L on days they began with above-median testosterone.
2. *Cortisol rose with trading variance and market volatility*, not with the level of gains or losses. The stress hormone tracked *risk*, not outcome.

The inferential leap is in Coates' book *The Hour Between Dog and Wolf* (2012): the same endocrine dynamics operating at the individual level aggregate into boom-bust cycles at the market level. A winning streak raises testosterone floor-wide, which raises risk appetite floor-wide, which extends the winning streak until a shock triggers cortisol-driven retrenchment that is also floor-wide. This is the *explicit micro-to-macro bridge* the user asked about. It is more speculative than the Coates & Herbert empirical finding, but it is the most-cited version of this mechanism in print.

Lo & Repin (2002 *J Cog Neurosci*) anchors the stress-trade link in autonomic measurement rather than blood-draw endocrinology, with the same directional finding: transient market events produce reliable skin-conductance responses, and experience modulates — but does not eliminate — the effect. The honest limitation of both studies is small N (10 and 17), single-firm, male-only samples. The effect has been replicated in laboratory settings (Cueva et al. 2015 *Scientific Reports*) which showed cortisol and testosterone administration *causally* increase financial risk-taking.

---

## Adaptive Markets Hypothesis as the bridging frame

For an RQS audience — quantitative, skeptical of "behavioral hand-waving," but also empirically aware that markets are not always frictionless — Andrew Lo's Adaptive Markets Hypothesis (Lo 2004 *JPM*; Lo 2017 book) is the correct meta-frame. Three reasons:

1. **It preserves EMH as a limiting case.** AMH says markets tend to efficiency in stable regimes populated by well-adapted heuristics, and tend to inefficiency when the environment changes faster than heuristics can adapt. EMH is not wrong; it is *conditional*. This is much more palatable to a rigorous audience than "EMH is wrong."

2. **It predicts regime-dependent efficiency.** Behavioral biases are *features* of bounded-rational agents applying heuristics that worked in an ancestral environment to a changed one. Loss aversion, overreaction, and myopic loss aversion are not irrationality; they are heuristics that have become maladaptive in the current context. This reframes debiasing as *re-adaptation*, not as overriding human nature.

3. **It validates active management without dismissing EMH.** In the AMH framework, alpha exists in *transient disequilibrium windows* — the windows when heuristics mismatch environment most severely. That is exactly the stress-regime window the RQS presentation is about.

The claim: AMH is the only existing meta-frame that simultaneously (a) justifies active risk-taking, (b) accepts most of the evidence on bounded rationality, and (c) doesn't force an RQS quant to renounce the factor models they already use. For this audience, frame the entire behavioral argument in AMH language from slide 1.

---

## Fixed-income-specific behavioral pricing

This is the load-bearing section for the audience. Five distinct channels.

**1. Intermediary-driven risk premia.** The shift from consumption-based to intermediary-based asset pricing is the most important theoretical development in fixed income in the last 15 years. Adrian, Etula & Muir (2014) show that dealer-leverage shocks price both equity and bond cross-sections; He & Krishnamurthy (2013) calibrate the nonlinear crisis dynamics. For a bond RQS audience the take-away is that the "fundamental" driver of spread dynamics is *dealer balance-sheet state*, and dealer balance sheets are themselves subject to the same behavioral pressures — risk-limit tightening under vol spikes, VaR-driven de-risking, CEO-level loss aversion after a bad week — that drive individual PM behavior. The micro and the macro share a common physiology.

**2. Flight-to-quality and flight-to-liquidity.** Vayanos (2004 NBER) models fund managers subject to withdrawal thresholds; during high-volatility episodes their preference for liquidity *increases*, liquidity premia rise, and correlations among risky assets increase as they are jointly sold. Krishnamurthy & Vissing-Jorgensen (2012 *JPE*) document the Treasury convenience yield — the spread between AAA corporate and Treasury yields that is economically large (≈70 bps average, widening to 200+ bps in stress) and varies inversely with Treasury supply. Longstaff (2004 *JB*) measures the flight-to-liquidity premium in Treasuries vs. Refcorp bonds (same credit risk, different liquidity) at 10–16% of Treasury value. These are not anomalies the standard rational asset-pricing model explains well; they are behavioral/institutional prices.

**3. Bond-market anomalies and basis trades.** The on-the-run / off-the-run spread (Krishnamurthy 2002 *JFE*; Pasquariello & Vega 2009) is the canonical fixed-income limits-of-arbitrage exhibit: two nearly-identical Treasuries trade at different yields because of buy-and-hold liquidity demand for the newest issue, and the spread persists because the arbitrage requires specific repo financing that is not always available. The CDS-bond basis (Bai & Collin-Dufresne 2011; Boyarchenko et al. NY Fed 2018) went to –250 bps in late 2008 for investment-grade indices, and the post-2010 regulatory regime (Volcker, Basel III SLR) has *permanently widened* the basis because the arbitrage now requires more capital per dollar of exposure. Dealer balance sheets are the binding constraint, not absence of mispricing.

**4. Credit-cycle psychology.** Greenwood & Hanson (2013 *RFS*) show issuer quality deteriorates during credit booms (lower-rated firms disproportionately issue late-cycle), and that the *share* of low-quality issuance is a strong predictor of low subsequent excess returns on corporate bonds. This is an explicitly behavioral mechanism: investors extrapolate recent low defaults into continued optimism, spreads compress, marginal issuers crowd in, and the subsequent default wave reveals the mispricing. Greenwood, Hanson, Shleifer & Jin (2022 *RFS*) formalize it as *over-extrapolation in credit markets*. López-Salido, Stein & Zakrajšek (2017 *QJE*) connect credit-market sentiment to subsequent *macroeconomic* slowdowns, which is the most direct evidence that bond-market psychology has real consequences. For a credit PM audience this is the single most actionable finding in the literature.

**5. The 2020 corporate bond dislocation.** Haddad, Moreira & Muir (2021 *RFS*) document that in March 2020 investment-grade corporate bond ETFs traded at ~5% *discount* to NAV, the CDS-bond basis collapsed more severely for safe bonds than for risky bonds, and Fed announcement of the SMCCF/PMCCF on March 23 *recovered IG bond prices by 7%*. That 7% recovery from a policy announcement — not from fundamental news — is the cleanest modern evidence that corporate bond prices in stress are about intermediation capacity and sentiment, not fundamentals.

---

## 2022 as a case study

2022 deserves a dedicated slide because it is the presenter's own empirical window and because it differs instructively from 2008 and 2020.

The drawdown: the Bloomberg Aggregate returned –13.0%, the worst calendar year in modern index history; 30-year Treasury total return was –33%. Dealer balance sheets entered the year already constrained by SLR and the post-2020 inventory buildup; by Q2 2022 primary dealers were "running out of room" to warehouse Treasuries (NY Fed staff reports; Duffie 2023 Jackson Hole). Treasury market depth for 2-year and 10-year on-the-run issues fell to the *worst since March 2020* (Fed FSR November 2022). UK gilts required BoE intervention on September 28 after LDI-driven forced selling by pension funds — a textbook Brunnermeier-Pedersen funding-liquidity spiral.

The behavioral fingerprint was:
- *Horizon compression* in sell-side and buy-side research (matches the presenter's own measurement in Capital Group analysts).
- *Correlated de-risking* across duration-exposed funds — the herding equilibrium, enforced by drawdown-based mandate triggers.
- *Commodity-like correlation breakdown*: Treasuries and credit sold off together, unusually, because the shock was a *discount-rate* shock (not a flight-to-quality shock), which revealed that much of the 2010s "safe asset" trade was a levered duration position held for yield-grab reasons rather than diversification reasons. That misperception was a behavioral pricing error that 2022 corrected.
- *Convenience-yield compression*: the Treasury convenience yield declined from about –20 bps in 2022 to near –60 bps by late 2023, as QT and dealer-capacity limits combined to reduce the special status of Treasuries (St. Louis Fed 2026).

The 2022 episode is *cleaner evidence than 2008 or 2020* for the intermediary-asset-pricing + behavioral-flow story, because (a) it wasn't a credit event (so the textbook risk-premium story doesn't explain it), (b) it wasn't a liquidity panic (no March-2020-style dash for cash), and (c) it played out slowly over 9 months, which ruled out "it's all just forced selling." What's left is: dealer-capacity constraints + correlated behavioral de-risking + regime-change uncertainty. Exactly what an RQS bond audience needs to see to accept the behavioral frame.

---

## Honest limits — rational explanations for the same patterns

The presentation will be more credible if it addresses these head-on.

**Liquidity premia as rational compensation.** Many "behavioral" spreads (on-the-run/off-the-run, convenience yield, Treasury-swap basis) are defensible as rational compensation for *predictable* liquidity risk. An asset pricing model with heterogeneous-horizon agents (Vayanos & Vila 2021 *Econometrica*) gets most of the yield-curve dynamics from market segmentation and preferred habitats, without invoking bias.

**Inventory and balance-sheet costs.** The post-2010 widening of the CDS-bond basis is better explained by regulatory capital costs (Basel III SLR) than by persistent behavioral error. "Limits of arbitrage" has become partially endogenous to the regulatory regime.

**Convexity hedging by mortgage investors.** Much of the 2022 Treasury volatility pattern can be traced to MBS convexity hedging flows — a *structural, rational* response to changes in expected prepayments. No bias necessary.

**Fama's critique (1998 *JFE*).** Long-horizon anomalies are fragile to methodology choice; momentum anomalies are fragile to risk-factor specification; underreaction and overreaction roughly cancel out across studies; and the remaining anomalies concentrate in small-illiquid-hard-to-arbitrage names, consistent with either behavioral or rational-friction stories. Fama's challenge is valuable because it forces precise tests. The honest answer is that in *normal* times, the rational-frictions and behavioral explanations are empirically indistinguishable. They *diverge* in regime-change and stress windows — which is precisely the presentation's topic.

**Why this audience is predisposed to accept behavioral, but will ask sharp distinguishing questions.** A bond RQS group has personally experienced the March-2020 dash-for-cash and the 2022 drawdown; they know mispricing is real and that intermediary constraints bind. But they are also trained to ask: "What's the testable, out-of-sample, distinguishing prediction of your behavioral story versus a rational-frictions story?" The strongest answer is the AMH framing: both are true, their relative dominance varies with regime, and what matters for a PM is *knowing which regime you are in*.

---

## Bridge to our empirical finding

If individual PM stress distorts individual decisions (the A1c horizon-compression result and the B1 PM-trades-under-stress result), and aggregated PM stress distorts *prices* (the entire market-level literature above), then the question "are PMs better in stress?" reframes.

The reframed question is: **does active decision-making add value exactly when the market is most mispriced — i.e., precisely when the decision-maker is also most biased?**

That is the non-trivial question. The answer has three possible shapes.

1. *Active value adds in stress*, because PMs see the mispricing and have the institutional freedom to trade against it. The behavioral distortion creates the alpha; the cognitive distortion is the cost of admission.
2. *Active value subtracts in stress*, because the same stress that mispriced the market is inside the PM's head, so the PM trades in the same direction as the crowd and reinforces the mispricing. Active management is a sentiment amplifier.
3. *Active value is heterogeneous in stress*, with some PMs capturing the mispricing and others amplifying it, and the discriminator is *process* — PMs with structured decision protocols, cooling-off rules, and premortems are the ones who extract alpha because they've partially insulated their cognition from the stress state.

The empirical result the presenter has will distinguish among these three. Whichever it shows, the market-level literature ensures the finding has *external* relevance, not just internal relevance to Capital Group's operations. If (1), it is evidence for active management at large. If (2), it is evidence that the industry's stress-window behavior contributes to systemic mispricing. If (3), it is a direct blueprint for the RQS recommendation — instrument the stress response, build process around it.

That last framing is the strongest and most defensible thesis version for an RQS audience.

---

## Citations

- Adrian, Tobias, Erkko Etula, and Tyler Muir. 2014. "Financial Intermediaries and the Cross-Section of Asset Returns." *Journal of Finance* 69(6): 2557–2596.
- Arnsten, Amy F. T. 2009. "Stress signalling pathways that impair prefrontal cortex structure and function." *Nature Reviews Neuroscience* 10(6): 410–422.
- Bai, Jennie, and Pierre Collin-Dufresne. 2011. "The CDS-Bond Basis During the Financial Crisis of 2007–2009." Working paper.
- Baker, Malcolm, and Jeffrey Wurgler. 2006. "Investor Sentiment and the Cross-Section of Stock Returns." *Journal of Finance* 61(4): 1645–1680.
- Baker, Malcolm, and Jeffrey Wurgler. 2007. "Investor Sentiment in the Stock Market." *Journal of Economic Perspectives* 21(2): 129–152.
- Boyarchenko, Nina, Pooja Gupta, Nick Steele, and Jacqueline Yen. 2018. "Trends in Credit Basis Spreads." *NY Fed Economic Policy Review*.
- Brunnermeier, Markus K., and Lasse Heje Pedersen. 2009. "Market Liquidity and Funding Liquidity." *Review of Financial Studies* 22(6): 2201–2238.
- Coates, John M., and Joe Herbert. 2008. "Endogenous steroids and financial risk taking on a London trading floor." *PNAS* 105(16): 6167–6172.
- Coates, John M. 2012. *The Hour Between Dog and Wolf: How Risk-Taking Transforms Us, Body and Mind*. Penguin.
- Cueva, Carlos, R. E. Roberts, et al. 2015. "Cortisol and testosterone increase financial risk taking and may destabilize markets." *Scientific Reports* 5: 11206.
- DeLong, J. Bradford, Andrei Shleifer, Lawrence H. Summers, and Robert J. Waldmann. 1990. "Noise Trader Risk in Financial Markets." *Journal of Political Economy* 98(4): 703–738.
- Devenow, Andrea, and Ivo Welch. 1996. "Rational herding in financial economics." *European Economic Review* 40(3-5): 603–615.
- Duffie, Darrell. 2010. "Presidential Address: Asset Price Dynamics with Slow-Moving Capital." *Journal of Finance* 65(4): 1237–1267.
- Duffie, Darrell. 2023. "Resilience Redux in the US Treasury Market." Jackson Hole Symposium paper.
- Fama, Eugene F. 1998. "Market efficiency, long-term returns, and behavioral finance." *Journal of Financial Economics* 49: 283–306.
- Greenwood, Robin, and Samuel G. Hanson. 2013. "Issuer Quality and Corporate Bond Returns." *Review of Financial Studies* 26(6): 1483–1525.
- Greenwood, Robin, Samuel Hanson, Andrei Shleifer, and Jakob Ahm Sørensen. 2022. "Predictable financial crises." *Journal of Finance* 77(2): 863–921.
- Grinblatt, Mark, and Bing Han. 2005. "Prospect theory, mental accounting, and momentum." *Journal of Financial Economics* 78(2): 311–339.
- Haddad, Valentin, Alan Moreira, and Tyler Muir. 2021. "When Selling Becomes Viral: Disruptions in Debt Markets in the COVID-19 Crisis and the Fed's Response." *Review of Financial Studies* 34(11): 5309–5351.
- He, Zhiguo, and Arvind Krishnamurthy. 2013. "Intermediary Asset Pricing." *American Economic Review* 103(2): 732–770.
- Krishnamurthy, Arvind. 2002. "The bond/old-bond spread." *Journal of Financial Economics* 66(2-3): 463–506.
- Krishnamurthy, Arvind, and Annette Vissing-Jorgensen. 2012. "The Aggregate Demand for Treasury Debt." *Journal of Political Economy* 120(2): 233–267.
- Lo, Andrew W. 2004. "The Adaptive Markets Hypothesis: Market Efficiency from an Evolutionary Perspective." *Journal of Portfolio Management* 30(5): 15–29.
- Lo, Andrew W. 2017. *Adaptive Markets: Financial Evolution at the Speed of Thought*. Princeton University Press.
- Lo, Andrew W., and Dmitry V. Repin. 2002. "The Psychophysiology of Real-Time Financial Risk Processing." *Journal of Cognitive Neuroscience* 14(3): 323–339.
- Longstaff, Francis A. 2004. "The Flight-to-Liquidity Premium in U.S. Treasury Bond Prices." *Journal of Business* 77(3): 511–526.
- López-Salido, David, Jeremy C. Stein, and Egon Zakrajšek. 2017. "Credit-Market Sentiment and the Business Cycle." *Quarterly Journal of Economics* 132(3): 1373–1426.
- Pasquariello, Paolo, and Clara Vega. 2009. "The on-the-run liquidity phenomenon." *Journal of Financial Economics* 92(1): 1–24.
- Scharfstein, David S., and Jeremy C. Stein. 1990. "Herd Behavior and Investment." *American Economic Review* 80(3): 465–479.
- Schwabe, Lars, and Oliver T. Wolf. 2013. "Stress and multiple memory systems: from 'thinking' to 'doing'." *Trends in Cognitive Sciences* 17(2): 60–68.
- Shleifer, Andrei, and Robert W. Vishny. 1997. "The Limits of Arbitrage." *Journal of Finance* 52(1): 35–55.
- Sias, Richard W. 2004. "Institutional Herding." *Review of Financial Studies* 17(1): 165–206.
- Stambaugh, Robert F., Jianfeng Yu, and Yu Yuan. 2012. "The short of it: Investor sentiment and anomalies." *Journal of Financial Economics* 104(2): 288–302.
- Vayanos, Dimitri. 2004. "Flight to Quality, Flight to Liquidity, and the Pricing of Risk." NBER Working Paper 10327.
- Vayanos, Dimitri, and Jean-Luc Vila. 2021. "A Preferred-Habitat Model of the Term Structure of Interest Rates." *Econometrica* 89(1): 77–112.

---

## Candidate canonical graphs

1. **VIX vs. sentiment-anomaly return spread.** Use Baker-Wurgler sentiment index on the x-axis or in a time-series panel; plot long-short return to 11 anomaly portfolios (Stambaugh-Yu-Yuan) split by high- vs. low-sentiment quartiles. Shows the anomaly premium is concentrated in high-sentiment periods. Bond analog: VIX-split credit-spread excess return.
2. **Coates aggregated cortisol-vs-volatility scatter.** The single most viscerally persuasive chart for a quant audience: individual trader cortisol plotted against same-day P&L variance, from the 2008 PNAS paper. Grounds the entire behavioral argument in a blood-draw.
3. **Baker-Wurgler sentiment index time series (1965–present).** Shows the dot-com peak (1999–2000), the late-2000s bottom, the meme-stock 2021 spike. Pair with subsequent cross-sectional anomaly performance.
4. **Credit-spread overshoot in 2008, 2020, 2022.** HY OAS or IG-OAS time series with shaded stress windows, annotated with the *recovery* speed (weeks, months, quarters) — makes the Shleifer-Vishny and Duffie slow-moving-capital argument visual. March 23 2020 Fed announcement as a point annotation showing –75 bps on IG spreads in one day is a single-point killer chart.
5. **On-the-run / off-the-run Treasury spread through 2022–2023.** Directly shows limits-of-arbitrage in the PM's own asset class.
6. **Treasury convenience yield time-series (Krishnamurthy-Vissing-Jorgensen spread).** Annotate with QE on/off, SLR changes, 2020 dash-for-cash, 2022 QT. Shows the "behavioral" price of safety moves on identifiable institutional events.
7. **Primary dealer Treasury inventory vs. market depth.** NY Fed data; shows the 2022 dealer-capacity squeeze in one chart. Anchors the intermediary-asset-pricing claim.
8. **Adrian-Etula-Muir dealer-leverage factor loadings across asset classes.** Demonstrates that the same SDF prices stocks *and* bonds — the empirical core of intermediary asset pricing for a bond audience.

Apply project chart rules: no black, straight lines (tension:0), visible dots at every data point.
