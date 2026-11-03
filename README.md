# Google Cloud — FP&A Financial Model

**Independent Excel portfolio project | Q3 2026 actual performance + Q4 2026 operating forecast + FY2027 illustrative planning extension**

> **Not affiliated with Alphabet or Google.** All historical figures are from public disclosures. All forward projections and segment cost splits are **independent, hypothetical assumptions**, not company guidance or inside information.

## Executive summary

This project translates Google Cloud's accelerated 2026 growth into an FP&A planning case: **How could Google Cloud balance expansion, operating leverage, and the near-term costs of third-party compute capacity?**

In **Q3 2026**, Google Cloud reported **$30,709 million** of segment revenue and **$11,121 million** of operating income, representing roughly **102.6% YoY revenue growth** and a **36.2% operating margin**. The workbook offers a three-case Q4 2026 operating projection, followed by a 2027 planning extension. Source: [Alphabet Q3 2026 earnings release](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000080/googexhibit991q32026.htm).

### Illustrative base-case output (NOT actuals or guidance)

| Metric | Q4 2026 modeled base case |
|---|---:|
| Revenue | **$36.24B** |
| Operating income | **$12.86B** |
| Operating margin | **35.5%** |
| Revenue QoQ growth assumption | **18.0%** |
| Modeled third-party capacity premium | **2.5% of revenue** |

The model attributes the base-case Q4 revenue growth to an editable assumption and explicitly models a near-term cost headwind. Those settings should be challenged and adjusted; **this is not a prediction of Alphabet's official results**.

## Download and use

Open [`Google_Cloud_FPNA_Q3_2026_Model.xlsx`](Google_Cloud_FPNA_Q3_2026_Model.xlsx) in desktop Microsoft Excel. No macros, APIs, Tableau, or Python runtime are required.

1. Start in **START HERE** for the navigation guide.
2. Inspect **EXEC DASHBOARD** for KPIs and the trend chart.
3. Change **ASSUMPTIONS!B7** to `1` (downside), `2` (base) or `3` (upside).
4. Adjust the yellow/blue inputs in **SCENARIOS** and **ASSUMPTIONS**.
5. Review the dynamically linked **FORECAST**, **Q3 VARIANCE**, and **SENSITIVITY** outputs.

## Workbook architecture

| Worksheet | Function |
|---|---|
| START HERE | User guide, model conventions and limitations |
| EXEC DASHBOARD | Q3 actual KPIs, Q4 forecast, 2027 plan, trend graph |
| HISTORICAL | Seven quarters of reported Cloud segment revenue/operating income; FY2025 reconciliation |
| ASSUMPTIONS | Scenario toggle, base cost split and quarterly 2027 growth drivers |
| FORECAST | Dynamically-linked Google Cloud segment operating P&L |
| SCENARIOS | Downside/base/upside Q4 forecasts with editable cost assumptions |
| Q3 VARIANCE | Q3 2025-to-Q3 2026 actual variance and income attribution bridge |
| SENSITIVITY | Two-way Q4 operating income sensitivity to revenue growth/margin |
| SOURCES | Verified SEC filing links, reporting limitations and assumptions |

## Model math

- **Reported operating margin** = segment operating income / segment revenue.
- **Implied segment costs** = reported segment revenue − reported segment operating income. *This is derived, **not a separate disclosed segment expense line**.*
- **Forecast revenue** = prior-quarter revenue × (1 + assumed sequential revenue growth).
- **Hypothetical variable expense** = forecast revenue × assumed variable cost ratio.
- **Hypothetical fixed expense** = previous fixed expense × (1 + modeled fixed-expense growth).
- **Hypothetical capacity premium** = revenue × capacity-premium assumption.
- **Projected operating income** = revenue − variable expense − fixed expense − capacity premium.
- **Two-way sensitivity** = forecast revenue under an alternative growth rate × selected operating margin.

## Analytical caveats

- Alphabet publicly reports Google Cloud **segment revenue and segment operating income**, but does **not** disclose the variable/fixed segment cost split implemented here. These are hypothetical planning drivers calibrated against reported Q3 implied costs.
- Q3 operating margins benefited from strong demand and rising revenue. Management said third-party bridging capacity began to come online near the end of Q3 and could pressure near-term Cloud margins. This informs the **direction** of the cost-premium assumption, but not its numerical magnitude.
- Alphabet-wide capital expenditure guidance must **not** be allocated entirely to Google Cloud. No such allocation is made in the model.
- No Q4 2026 actual result exists as of the project's creation date (November 3, 2026). The Q4 and 2027 figures are **scenario forecasts**, not actuals.
- The YoY operating income attribution is an **accounting identity** (revenue change minus implied cost change), not evidence of causal cost-driver effects.
- There is no claim of forecast accuracy or cost savings. A formal forecast backtest can be added later.

## Public sources

- [Q1 2026 earnings exhibit](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000043/googexhibit991q12026.htm)
- [Q2 2026 earnings exhibit](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000066/googexhibit991q22026.htm)
- [Q3 2026 earnings exhibit](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000080/googexhibit991q32026.htm)
- [Q4 2025 / FY2025 earnings exhibit](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000012/googexhibit991q42025.htm)
- [2025 Alphabet 10-K](https://www.sec.gov/Archives/edgar/data/1652044/000165204426000018/goog-20251231.htm)
- [Q3 2026 earnings call](https://abc.xyz/investor/events/event-details/2026/2026-Q3-Earnings-Call-2026-Ujou16CTw9/default.aspx)

## Potential extension

Once Q4 2026 actuals are published, use them to calculate forecast errors and a variance bridge against the model's frozen November 2026 base-case forecast. The appropriate future work is forecast-vs-actual analysis, not retroactively changing baseline assumptions.
