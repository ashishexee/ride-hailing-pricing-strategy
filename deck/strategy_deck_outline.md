# STRATEGY DECK: Dynamic Pricing Optimization for Ride-Hailing
# 8-Slide Content Outline (per Problem Statement Required Structure)

==============================================================
SLIDE 1: EXECUTIVE SUMMARY
==============================================================
Headline: "Surge Pricing Drives Revenue but Erodes Retention — Zone Governance Restores Balance"

Three lines:
1. Current surge pricing generates 62.8% of CM from 31.2% of trips, but satisfaction drops from 4.14→2.36 across the surge range, driving ~14% annual churn
2. Zone-governed caps (1.75/2.0/2.5x) reduce CM by 6.06% but structurally diversify revenue; LTV/CAC could reach 1.47-1.84x (churn improvement uncertain: 0.15-0.64pp)
3. Recommendation: Option 2 (Zone Governance) as primary, with Option 3 (Loyalty Protection) as Phase 3 enhancement

Weighted scores: Calibrated=3.02 | Zone Governance=4.46 | Loyalty Soft=3.60

Chart: charts/options_scoring_round2.png

==============================================================
SLIDE 2: THE PROBLEM — Surge Pricing Satisfaction Cliff
==============================================================
Headline: "The Problem: Surge Pricing Satisfaction Cliff and Revenue Concentration"

Key findings:
1. Satisfaction drops sharply with surge: 4.14 (1.0x) → 3.49 (1.5x) → 2.36 (2.5x)
2. Bracketed churn model: 14% → 20% → 38% annual churn across this range
3. 62.8% of CM from 31.2% of trips — extreme revenue concentration risk
4. 39.6% of trips have NEGATIVE margin (cross-subsidy from surge to non-surge)
5. Completion rate non-monotonic at 1.75x (61.8% of subgroups show data artifact)
6. Implication: Current pricing is profitable but fragile — retention erosion threatens long-term CM sustainability

Chart: charts/satisfaction_vs_surge.png

==============================================================
SLIDE 3: SEGMENT IMPACT — Who Is Affected and Where Margins Collapse
==============================================================
Headline: "Segment Impact: Who Is Affected and Where Margins Collapse"

Key findings:
1. Frequent riders: LTV/CAC 1.47x (current), churn-sensitive, highest value
2. Occasional riders: LTV/CAC 0.87x, low retention leverage
3. Rare riders: LTV/CAC 0.44x, negative margin, churn less impactful
4. Negative margins concentrated in residential, short-distance, low-surge trips
5. Min fare Rs.125/zone eliminates negative CM across all segments
6. Zone caps protect the segments most vulnerable to satisfaction erosion

Charts: charts/ltv_cac_by_segment.png + charts/negative_margin_heatmap.png

==============================================================
SLIDE 4: PORTER'S FIVE FORCES — India Ride-Hailing
==============================================================
Headline: "High Rivalry, Zero Switching Costs, Strong Substitutes"

One insight per force:
1. Buyer Power: HIGH — Multi-apping is norm (75%+ have 2+ apps); zero switching cost; price comparison in real-time
2. Supplier Power (Drivers): MODERATE — Platform-dependent for demand; but earnings sensitivity to caps creates retention risk
3. Rivalry: HIGH — Ola, Uber, Rapido; margin pressure; winner-take-most dynamics
4. Substitutes: VERY HIGH — Metro (Delhi/Mumbai), autos, buses; short-distance especially substitutable
5. New Entrants: MODERATE — Network effects barrier; zero-surge positioning can attract switchers

Key implication: Zone caps are DEFENSIBLE (not visible until ride request); uniform caps are NOT (immediately observable)

Chart: charts/porters_five_forces.png

==============================================================
SLIDE 5: RECOMMENDATION — Zone Governance + Options Table
==============================================================
Headline: "Recommendation: Zone-Governed Surge Caps — What, Where, Why"

WHAT: Differentiated surge caps by zone type
- Residential: 1.75x cap (high substitute availability, price-sensitive, elasticity 0.25)
- Commercial: 2.0x cap (time pressure > price, moderate sensitivity, elasticity 0.24)
- Transit Hub: 2.5x cap (last-mile necessity, low sensitivity, elasticity 0.26)

WHERE: Mumbai, Bangalore, Delhi — all zone types simultaneously

WHY (with numbers, trip-level simulation, 97% baseline):
- CM impact: -6.06% (manageable; churn improvement 0.15-0.64pp depending on model → LTV/CAC 1.47-1.84x for frequent; structural thesis primary)
- Trips protected: 10.7% (from excessive surge)
- Satisfaction gain: +0.061 points average
- Minimum fare floor: Rs.125/zone to eliminate negative CM
- Robust to scoring assumptions: wins 6/6 weight scenarios (score 4.46)

Options comparison table:
| Dimension | Calibrated (2.0x) | Zone Gov (1.75/2.0/2.5x) | Loyalty Soft (1.75x GS) |
|---|---|---|---|
| Revenue Impact | -2.20% | -1.79% | -0.58% |
| CM Impact | -5.89% | -6.06% | -2.55% |
| Churn Improvement | +0.53pp | +0.64pp | +0.25pp |
| Weighted Score | 3.02 | 4.46 | 3.60 |

WHY NOT Option 1: Uniform cap is immediately observable by competitors, easily matched, no strategic moat
WHY NOT Option 3 alone: Only protects Gold/Silver (10-15% of trips); 37.1% Unknown tier unprotected

Phase 3 enhancement: Add loyalty cap (1.75x for Gold/Silver) on top of zone caps

Charts: charts/scenario_cm_impact.png + embedded table

==============================================================
SLIDE 6: ENHANCEMENT — Loyalty Protection on Top of Zone Caps
==============================================================
Headline: "Phase 3 Enhancement: Loyalty Protection on Top of Zone Caps"

Key findings:
1. Combined Zone + Loyalty (1.75x for Gold/Silver): CM -6.92%, churn +0.74pp
2. 1.5x loyalty cap too aggressive; 2.0x provides minimal additional benefit over zone caps alone
3. 37.1% of riders are Unknown tier — unprotected by loyalty caps alone
   — "Path to Silver" program: 5 rides → Silver status, gradually expanding coverage
4. Recommended sequencing: Zone caps first (Phase 2), loyalty overlay (Phase 3)
   — Allows measurement of zone-only impact before adding complexity
   — Driver earnings guarantee already in place before loyalty cap reduces driver revenue further
5. Sensitivity: Combined option CM impact ranges from -6.06% to -6.92% depending on loyalty tier scope

Chart: charts/combined_loyalty_sensitivity.png

==============================================================
SLIDE 7: IMPLEMENTATION CONSIDERATIONS
==============================================================
Headline: "5-Phase Rollout: Key Risks and Mitigations"

What needs to happen:
Phase 1 (Month 1-2): Foundation — Zone classification engine, shadow-mode testing
Phase 2 (Month 3-4): Zone Caps Live — 1.75/2.0/2.5x, driver earnings guarantee
Phase 3 (Month 5-6): Loyalty Protection — 1.75x cap for Gold/Silver, "Path to Silver" for Unknown/Bronze
Phase 4 (Month 7-12): Optimization — A/B test fine-tuning, dynamic caps
Phase 5 (Month 13-18): Scale & Series D — Full governance operational

Key risks and mitigations:
| Risk | Severity | Mitigation |
|---|---|---|
| R1: Driver earnings reduction in capped zones | CRITICAL | Earnings guarantee fund (2% of CM); real-time earnings dashboard |
| R2: Competitor price matching | HIGH | Reliability differentiation; zone caps invisible until request |
| R3: Unknown tier alienation (37.1%) | HIGH | "Path to Silver" program; 5 rides → Silver status |
| R4: Data artifact in completion rates | MEDIUM | 97% baseline assumption; monitor actual completion post-launch |
| R5: Regulatory intervention | MEDIUM | Proactive self-regulation narrative; zone caps as consumer protection |

Success metrics by phase:
- Phase 2: Residential completion +1.5pp, satisfaction +0.05
- Phase 3: Gold/Silver retention +2pp
- Phase 4: Net CM improvement >2%, LTV/CAC >1.0x occasional
- Phase 5: LTV/CAC ≥1.47x frequent, NRR >95%, CM <55% surge-dependent

Chart: charts/implementation_risk.png

==============================================================
SLIDE 8: INVESTOR AND FINANCIAL NARRATIVE
==============================================================
Headline: "Retention-Driven Unit Economics: 3 Metrics, 18-Month Horizon"

Three metrics with directional statements:

1. LTV/CAC Ratio (Frequent Segment)
   Current: 1.47x → Target: 1.47-1.84x (18 months; lower bound = no validated churn improvement; upper bound = industry benchmarks)
   Directional: "Zone governance structurally diversifies CM and improves defensibility; LTV/CAC upside depends on churn model validity (UNCERTAIN)"
   Confidence: MEDIUM-LOW for LTV/CAC magnitude; MEDIUM-HIGH for structural thesis

2. Net Revenue Retention (NRR)
   Current: ~94% (revenue-weighted) → Target: ~95%+ (18 months)
   Directional: "NRR already strong at ~94% (revenue-weighted); zone governance protects high-value riders and can push toward 95%+"
   Confidence: MEDIUM-HIGH (NRR already strong at ~94%; churned customers are low-value rare riders)

3. CM Sustainability
   Current: 62.8% surge-dependent → Target: <55% surge-dependent (18 months)
   Directional: "Reducing surge dependency from 63% to <55% makes CM more volume-driven and defensible"
   Confidence: MEDIUM-HIGH (structural shift from zone caps; less dependent on churn model)

Key caveats:
- Bracketed churn model: 0/3 directional tests passed (anomalous satisfaction→churn in raw data)
- Segment-based churn model: 3/3 mechanical correlations (segment=churn rate by construction); within-segment effect NOT validated
- 97% baseline: conservative; if actual baseline is 95-96%, CM impact would be larger
- 1.75x non-monotonic completion: 61.8% of subgroups show data artifact; interpolation used
- CAVEAT: Neither bracketed nor segment churn model validates satisfaction→churn causation. Recommendation rests on STRUCTURAL thesis.

Chart: charts/investor_narrative.png


R5 CAVEAT ON CHURN-BASED RECOMMENDATION:
Even at segment lower bound (0.15pp churn improvement), LTV/CAC remains ~1.49x (essentially unchanged). The recommendation RESTS ON structural benefits (CM diversification, competitive defensibility, regulatory positioning), NOT on churn/retention improvement. Churn improvement is potential upside only.


R7 METHODOLOGY NOTE:
All simulation results use trip-level methodology (Round 7): for each trip, per-trip
CM/revenue/completion/satisfaction deltas are computed under each scenario, then aggregated.
This replaces the blended approach (Rounds 1-6) which used zone-level aggregate adjustments.
Key differences: (1) S0 Status Quo = 0.00% (not -1.23%), (2) per-trip elasticity by surge
band instead of zone-average, (3) new completion rates use adjusted curve at CAPPED surge
level (not original band). Recommendation UNCHANGED: Zone Governance remains primary.


R9 DECK STRUCTURE NOTE:
Deck reordered to: Exec Summary → Problem → Segment Impact → Porter's → Recommendation → Enhancement → Implementation → Investor.
All 9 chart images embedded (2 on Segment Impact slide). Options comparison table on Slide 5.
Speaker notes added to all 8 slides. Weighted scores updated: 3.02/4.46/3.60.
