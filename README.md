# Dynamic Pricing Strategy in Ride-Hailing

A case study analyzing surge pricing impact on customer retention, unit economics, and long-term enterprise value for a ride-hailing platform across Mumbai, Bangalore, and Delhi.

## Recommendation
**Zone-Governed Surge Pricing** — Residential 1.75x / Commercial 2.0x / Transit Hub 2.5x caps.

## Project Structure

```
├── data/                  # Raw and cleaned datasets
│   ├── cleaned_data.csv
│   └── india_rideshare_dataset.xlsx
├── notebooks/             # Analysis notebook
│   └── Ride_Hailing_Pricing_Strategy.ipynb
├── outputs/               # Generated data and Excel deliverables
│   ├── Unit_Economics.xlsx
│   ├── Revenue_Simulation.xlsx
│   └── *.csv
├── charts/                # 48 visualizations
├── deck/                  # Strategy deck
│   ├── Strategy_Deck.pptx
│   ├── Strategy_Deck.pdf
│   └── strategy_deck_outline.md
└── docs/                  # Problem statement and methodology
    ├── problem_statement.txt
    └── elasticity_methodology.txt
```

## Key Findings

| Metric | Value |
|--------|-------|
| Elasticity (97% baseline) | 0.22 (inelastic) |
| LTV/CAC (Frequent) | 1.47x |
| NRR (revenue-weighted) | 94.2% |
| Zone Gov CM impact | -6.06% |
| Negative margin trips | 39.6% |
| Satisfaction cliff | ~1.5x surge |

## Running the Notebook

1. Clone the repo
2. Open `notebooks/Ride_Hailing_Pricing_Strategy.ipynb` in Jupyter/VS Code/Colab
3. Run all cells

The notebook is self-contained — it reads `data/cleaned_data.csv` and computes all analysis inline.
