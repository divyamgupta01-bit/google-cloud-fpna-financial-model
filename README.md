# Google Cloud — FP&A Financial Model

An independent Excel model of Google Cloud's segment results: Q3 2026 actuals, a three-scenario Q4 2026 forecast, and an illustrative FY2027 plan.

> Independent project, not affiliated with Alphabet or Google. Historical figures come from public SEC filings; all forecasts and cost splits are my own assumptions.

## The question

How can Google Cloud keep expanding margins while absorbing the near-term cost of third-party compute capacity?

In Q3 2026, Google Cloud reported $30,709M in segment revenue and $11,121M in operating income: 102.6% YoY revenue growth and a 36.2% operating margin, up 12.5 points from a year earlier ([Q3 2026 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000080/googexhibit991q32026.htm)).

## Base-case Q4 2026 forecast

| Metric | Q4 2026 base case |
|---|---:|
| Revenue | $36.24B |
| Operating income | $12.86B |
| Operating margin | 35.5% |
| Sequential revenue growth | 18.0% |
| Third-party capacity premium | 2.5% of revenue |

The base case assumes margins dip slightly from Q3 as bridging compute capacity comes online, a headwind management flagged on the Q3 earnings call. Downside and upside cases flex growth, cost ratios and the capacity premium.

## How to use it

Open [`Google_Cloud_FPNA_Q3_2026_Model.xlsx`](Google_Cloud_FPNA_Q3_2026_Model.xlsx) in desktop Excel (no macros required).

1. **START HERE** explains the layout and color conventions.
2. **EXEC DASHBOARD** shows KPIs and the revenue/operating income trend.
3. Set **ASSUMPTIONS!B7** to 1 (downside), 2 (base) or 3 (upside).
4. Edit the yellow input cells in **SCENARIOS** and **ASSUMPTIONS**; **FORECAST**, **Q3 VARIANCE** and **SENSITIVITY** update automatically.

## Workbook structure

| Sheet | What it does |
|---|---|
| START HERE | Guide, conventions, limitations |
| EXEC DASHBOARD | Q3 actuals, Q4 forecast, FY2027 plan, trend chart |
| HISTORICAL | Seven quarters of reported segment revenue and operating income, with an FY2025 reconciliation check |
| ASSUMPTIONS | Scenario selector, cost structure, quarterly FY2027 drivers |
| FORECAST | Driver-based segment P&L, linked to the selected scenario |
| SCENARIOS | Downside / base / upside Q4 cases |
| Q3 VARIANCE | Q3 2025 → Q3 2026 bridge from revenue growth to operating income |
| SENSITIVITY | Q4 operating income across revenue growth and margin |
| SOURCES | SEC filing links and data notes |

## Model logic

- **Implied segment costs** = reported revenue − reported operating income
- **Forecast revenue** = prior-quarter revenue × (1 + sequential growth)
- **Variable costs** = revenue × variable cost ratio
- **Fixed costs** = prior fixed costs × (1 + fixed cost growth)
- **Capacity premium** = revenue × premium rate
- **Operating income** = revenue − variable costs − fixed costs − capacity premium

## Limitations

- Alphabet reports Cloud segment revenue and operating income only. The variable/fixed cost split is my assumption, calibrated so Q3 costs reconcile to reported figures.
- The capacity premium's direction comes from management commentary; its size is my estimate.
- No Alphabet-wide capex is allocated to Cloud.
- The Q3 variance bridge is an accounting identity, not a causal analysis.

## Next step

When Q4 2026 actuals are reported (around early February 2027), I'll compare them to this frozen base case and add a forecast-vs-actual variance analysis.

## Sources

- [Q1 2026 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000043/googexhibit991q12026.htm)
- [Q2 2026 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000066/googexhibit991q22026.htm)
- [Q3 2026 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000080/googexhibit991q32026.htm)
- [Q4 2025 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000012/googexhibit991q42025.htm)
- [Alphabet 2025 Form 10-K](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000018/goog-20251231.htm)
- [Q3 2026 earnings call](https://abc.xyz/investor/events/event-details/2026/2026-Q3-Earnings-Call-2026-Ujou16CTw9/default.aspx)
