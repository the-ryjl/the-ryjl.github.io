# crwd_stock_pitch
# CRWD Stock Pitch — CrowdStrike Holdings, Inc.
**Call:** Long | **Horizon:** 12 months | **Target:** ${price} | **Upside/Downside:** +{X}% / −{Y}%

## My Thesis
1. {Catalyst / mispricing}
2. {Evidence / KPI trajectory}
3. {Why the market is wrong}

## What’s in this repo
- `/memo`: 1-pager + full memo with sources
- `/deck`: competition slides
- `/model`: DCF, comps, sensitivities (with notes)
- `/src` & `/notebooks`: code to fetch/clean data and recreate charts

## Reproduce the analysis
```bash
# Option A: Conda
conda env create -f environment.yml
conda activate pitch
make all
# Option B: pip
pip install -r requirements.txt
python src/00_fetch_prices.py && python src/01_fetch_fundamentals.py
python src/02_clean_merge.py && python src/03_charts.py
