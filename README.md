# Dynamic Pricing Strategy in Ride-Hailing

A case study analyzing surge pricing impact on customer retention, unit economics, and long-term enterprise value for a ride-hailing platform across Mumbai, Bangalore, and Delhi.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L_27PUsoQKoB4WTpwMwXrz3kK6_tSEf1?usp=sharing) &nbsp; [![View Slide Deck](https://img.shields.io/badge/View-Slide_Deck-FFCC00?style=flat&logo=canva)](https://canva.link/hg0fx9pyiu66mfy)

## Recommendation
**Zone-Governed Surge Pricing** — Residential 1.75x / Commercial 2.0x / Transit Hub 2.5x caps. Score: 4.48 / 5.

## Project Structure

```
├── data/                  # Raw and cleaned datasets
├── notebooks/             # Self-contained analysis notebook (Colab compatible)
├── outputs/               # Excel deliverables + analysis CSVs
├── charts/                # 48 chart visualizations
├── deck/                  # Strategy deck → [View on Canva](https://canva.link/hg0fx9pyiu66mfy)
└── docs/                  # Problem statement and methodology
```

## Key Findings

| Metric | Value |
|--------|-------|
| Elasticity (97% baseline) | 0.22 (inelastic) |
| LTV/CAC (Frequent) | 1.47x |
| NRR (revenue-weighted) | 94.2% |
| Zone Gov CM impact | -5.64% |
| Negative margin trips | 39.6% |
| Satisfaction cliff | ~1.5x surge |
| Zone Gov weighted score | 4.48 / 5 |
| Weight sensitivity wins | 6 / 6 scenarios |

## Charts

### The Core Problem: Surge Erodes Satisfaction
![Satisfaction vs Surge](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/satisfaction_vs_surge.png)

Satisfaction drops 43% from 4.14 at 1.0x to 2.36 at 2.5x surge. The steepest decline occurs between 1.25x and 1.5x — the transition zone where surge pricing begins to meaningfully erode customer experience.

### 62.8% of CM Comes from Just 31.2% of Trips
![CM Decomposition](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/cm_decomposition.png)

Surge trips generate the majority of contribution margin but represent a minority of volume. 39.6% of all trips have negative CM — concentrated at short-distance (<3km) base-fare rides that are structurally unprofitable at current pricing.

### Completion & Cancellation by Surge Level
![Completion Cancel by Surge](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/completion_cancel_by_surge.png)

Completion falls from ~97% at 1.0x to 82% at 2.5x. Cancellation rises from 0% to 18% — nearly 1 in 5 rides is abandoned at peak surge.

### LTV/CAC by Customer Segment
![LTV CAC by Segment](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/ltv_cac_by_segment.png)

Only Frequent riders (1.47x) are above breakeven. Occasional (0.70x) and Rare (0.22x) are structurally unprofitable. Churn model uses industry benchmarks — NOT validated in this dataset (confidence: MEDIUM-LOW).

### Scenario Simulation: CM Impact by Strategy
![Scenario CM Impact](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/scenario_cm_impact.png)

All capped scenarios show CM decline vs Status Quo. Zone Governance (-5.64%) achieves the best balance between CM preservation and strategic considerations. Loyalty Soft (-2.42%) has the lowest CM impact but weaker strategic positioning.

### Strategic Options Scoring
![Options Radar](https://raw.githubusercontent.com/ashishexee/ride-hailing-pricing-strategy/main/charts/options_radar.png)

Zone Governance dominates across Regulatory Compliance, Strategic Fit, and Implementation Ease. Wins 6/6 weight sensitivity scenarios — recommendation is robust to scoring assumptions.

## Scoring Table

| Option | Surge Caps | CM Impact | Churn Δ | Score |
|--------|-----------|-----------|---------|-------|
| Status Quo | 2.5x all zones | 0.00% | 0.00pp | — |
| Option 1: Calibrated | 2.0x uniform | -5.36% | +0.53pp | 2.74 |
| **Option 2: Zone Gov (Recommended)** | **Res 1.75x / Com 2.0x / Transit 2.5x** | **-5.64%** | **+0.64pp** | **4.48** |
| Option 3a: Loyalty Hard | 1.5x Gold/Silver | -5.11% | +0.46pp | 3.03 |
| Option 3b: Loyalty Soft | 1.75x Gold/Silver | -2.42% | +0.25pp | 3.61 |
| Combined: Zone + Loyalty | Zone caps + 1.75x loyalty | -6.49% | +0.74pp | 4.19 |

## Running the Notebook

### Google Colab (one click)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L_27PUsoQKoB4WTpwMwXrz3kK6_tSEf1?usp=sharing)

### Slide Deck
[![View Slide Deck](https://img.shields.io/badge/View_on-Canva-FFCC00?style=flat&logo=canva)](https://canva.link/hg0fx9pyiu66mfy)

The notebook auto-downloads `cleaned_data.csv` from the GitHub release. Zero setup required.

### Local (Jupyter / VS Code)
```bash
git clone https://github.com/ashishexee/ride-hailing-pricing-strategy.git
cd ride-hailing-pricing-strategy
# Open notebooks/Ride_Hailing_Pricing_Strategy.ipynb in Jupyter/VS Code
# Run all cells
```

The notebook detects local vs Colab environment and downloads data if needed. Single-file, zero pre-computed dependencies.
