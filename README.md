# Marketing Funnel Analysis — Visitor → Lead → MQL → SQL → Customer

Analyzing a 6-month, 6-channel marketing funnel to find where users drop off, which channels
bring high-quality (not just high-volume) leads, and what to change to improve conversion.

## Problem
A business wants to know:
- Where are users dropping off in the funnel?
- Which channels bring high-quality leads?
- How can conversion rates be improved?
- Which stages need optimization?

## Data
`data/funnel_raw.csv` — 12,120 simulated visitor journeys (Jan–Jun 2026) across six channels
(Organic Search, Paid Search, Social Media, Email, Referral, Direct), each tagged with the
furthest funnel stage reached (Visitor → Lead → MQL → SQL → Customer), campaign, acquisition
cost, and deal value. Real-world messiness (duplicate rows, inconsistent casing, missing
campaign tags) was intentionally included and cleaned in the notebook.

> Simulated data is used since no real GA/CRM export was available. The cleaning steps,
> funnel logic, and channel-comparison methodology apply directly to real Google Analytics
> or CRM exports.

## Method
1. **Clean:** dedupe visitor journeys, standardize channel names, fill missing campaign tags.
2. **Funnel metrics:** cumulative stage counts, stage-over-stage conversion %, overall
   visitor-to-customer conversion %.
3. **Channel comparison:** visitor→lead %, lead→customer %, revenue, spend, ROI per channel.
4. **Trend:** monthly conversion rate over the period.
5. **Funnel shape by channel:** normalized funnel per channel to compare shape, not just volume.

## Key Findings
| Metric | Result |
|---|---|
| Overall Visitor → Lead | **19.7%** (largest single drop-off) |
| Overall Lead → Customer | **8.1%** |
| Best ROI channel | **Referral (53x)** |
| Worst ROI channel | **Social Media (0.1x — losing money)** |
| Weakest stage-to-stage step | **SQL → Customer (37% conversion)** |

Full breakdown, charts, and narrative in [`funnel_analysis.ipynb`](funnel_analysis.ipynb) and
[`report.md`](report.md).

## Recommendations
1. Fix the Visitor → Lead step first — it's the biggest leak by volume (landing page / offer / form friction).
2. Cut or rework Social Media spend — it's the only channel with negative ROI.
3. Double down on Referral and Email — already outperforming every paid channel 3–10x on ROI.
4. Audit Paid Search targeting — high lead volume but low lead quality suggests broad/misaligned keywords.
5. Investigate the sales process for SQL → Customer — the drop-off here points to closing, not lead quality.

## Repo Structure
```
├── data/
│   ├── funnel_raw.csv            # raw simulated export
│   ├── funnel_clean.csv          # cleaned dataset
│   └── channel_performance.csv   # per-channel summary metrics
├── charts/                       # exported PNG charts
├── funnel_analysis.ipynb         # full analysis notebook (Jupyter)
├── report.md                     # executive summary write-up
└── README.md
```

## Tools
Python (pandas, matplotlib, seaborn) in Jupyter Notebook — for exploratory analysis, funnel
metrics, and documenting analytical logic end to end.

## Skills Demonstrated
Funnel & conversion analysis · marketing/growth analytics · KPI tracking · channel ROI
comparison · data cleaning · business-focused insight generation.
