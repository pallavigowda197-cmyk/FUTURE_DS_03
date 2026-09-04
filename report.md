# Funnel Analysis Report: Visitor → Lead → MQL → SQL → Customer

**Period analyzed:** January – June 2026
**Data:** 12,000 visitor journeys (post-cleaning) across 6 acquisition channels

## 1. Overall Funnel

| Stage | Users (cumulative) | % of total visitors | Conversion from previous stage |
|---|---|---|---|
| Visitor | 12,000 | 100.0% | — |
| Lead | 2,358 | 19.7% | 19.7% |
| MQL | 1,242 | 10.4% | 52.7% |
| SQL | 511 | 4.3% | 41.1% |
| Customer | 191 | 1.6% | 37.4% |

**The single biggest drop is Visitor → Lead** — 4 out of 5 visitors never convert to a lead at
all. Every later stage holds up reasonably (37–53% each), so the funnel's main problem is at
the very top, not deep in the sales process.

## 2. Channel Performance

| Channel | Visitors | Leads | Customers | Visitor→Lead % | Lead→Customer % | Overall % | ROI |
|---|---|---|---|---|---|---|---|
| Referral | 1,080 | 406 | 74 | 37.6% | 18.2% | 6.85% | 53.4x |
| Email | 1,200 | 365 | 43 | 30.4% | 11.8% | 3.58% | 20.5x |
| Direct | 1,800 | 333 | 21 | 18.5% | 6.3% | 1.17% | n/a (no spend) |
| Organic Search | 2,880 | 453 | 33 | 15.7% | 7.3% | 1.15% | 7.7x |
| Paid Search | 2,400 | 544 | 19 | 22.7% | 3.5% | 0.79% | 1.0x |
| Social Media | 2,640 | 257 | 1 | 9.7% | 0.4% | 0.04% | 0.1x |

**Referral and Email are the highest-quality channels** by a wide margin — smaller volume, but
far better conversion at every stage and by far the best return on spend. **Paid Search brings
the most top-of-funnel leads (22.7%) but converts them the worst (3.5%)**, meaning that traffic
is high-volume, low-intent. **Social Media is the weakest channel across the board** and the
only one with sub-1x ROI (losing money).

## 3. Monthly Trend

Overall conversion rate rose from 0.81% (Jan) to 2.84% (Jun), roughly a 3.5x improvement over
six months — consistent with the growing share of Referral/Email traffic relative to Social/Paid
over the period.

## 4. Key Drop-off Insights

1. **Top-of-funnel is the leak, not the sales process.** ~80% of visitors never become a lead.
2. **Volume and quality are inversely related across channels.** The two biggest traffic
   sources (Paid Search, Social Media) have the worst conversion; the two smallest (Referral,
   Email) have the best.
3. **SQL → Customer is the weakest of the later-stage transitions (37%)**, worth a closer look
   at the sales/closing process specifically for already-qualified leads.
4. **Social Media spend is not paying for itself** at current targeting/creative.

## 5. Recommendations

| Priority | Action | Why |
|---|---|---|
| 1 | Redesign top-of-funnel offer/landing pages, reduce form friction | Fixes the largest leak (80% loss at Visitor→Lead) |
| 2 | Pause or restructure Social Media campaigns | Only channel losing money (0.1x ROI) |
| 3 | Increase investment in Referral program + Email nurture | Best-performing channels by a wide margin (53x, 20x ROI) |
| 4 | Audit Paid Search keyword targeting | High volume, low intent — likely broad-match waste |
| 5 | Review sales follow-up process for SQL-stage leads | Conversion drop here isn't explained by lead quality upstream |

*Full methodology, code, and charts: see `funnel_analysis.ipynb`.*
