# Funnel & Cohort Analysis — eCommerce Events (Cosmetics Shop)

Funnel, cohort-retention, LTV and opportunity-sizing analysis of 20.7M user events (Oct 2019 – Feb 2020) from the REES46 cosmetics store dataset.

**Interactive version:** https://growth-funnel-analytics.vercel.app

**Headline:** 75.7% of 1.64M visitors never add to cart, which is the largest drop-off in the funnel. A +5pp lift in visit→cart is worth ~5,289 extra purchasers and ~$216K revenue per month at current traffic. M1 repeat-purchase rate is 9.1% (Nov–Jan cohorts).

| File | What it is |
|---|---|
| `Growth_FunnelCohortAnalysis_v1.pdf` | 4-page memo for a Head of Growth / VP Product |
| `funnel_cohort_analysis.ipynb` | Full analysis; every memo figure is printed by a cell (§8 collects them) |
| `outputs/*.png` | Exported charts |
| `web/index.html` | Interactive page (funnel, cohorts, +5pp opportunity simulator), deployed on Vercel |
| `memo/memo.html` | Memo source (rendered to PDF with headless Chrome/Edge `--print-to-pdf`) |

## Reproduce
1. Download [the dataset](https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop) and unzip the five monthly CSVs into `data/raw/`.
2. `pip install -r requirements.txt`
3. `jupyter nbconvert --to notebook --execute --inplace funnel_cohort_analysis.ipynb` (first run builds a Parquet cache, ~6 min; needs ~8 GB RAM).
