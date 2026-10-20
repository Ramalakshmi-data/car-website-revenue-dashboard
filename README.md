# Car Website Revenue Analysis – Interactive Excel Dashboard

![Dashboard](11_dashboard.png)

## Overview
An Excel analysis of **102,896 rows** of 2017 car website data (January–September), covering visitors and revenue across **51 US states, 209 markets and 54 car brands**.

**Business question:** Which cars, states and months drive website revenue, and where is traffic underperforming?

**Tools:** Microsoft Excel (Tables, EXACT, UPPER, VLOOKUP, Pivot Tables, Calculated Fields, Pivot Charts, Slicers)

---

## 1. Data Cleaning
| Issue | Rows affected | Action taken |
|---|---|---|
| Inconsistent capitalisation in Body Style (e.g. "Sedan" vs "SEDAN") | 570 | Found with `EXACT`; created a standardised column with `UPPER` |
| Incomplete records (no state, market, make or model) | 6 | Kept; excluded from state, market and brand analysis |
| Market name not found (VLOOKUP `#N/A`) | 76 | Excluded from market analysis |
| Missing car make / model | 23 | Excluded from brand analysis |
| Unknown body style | 237 | Kept as UNKNOWN_BODYSTYLE |
| Extreme outliers (thousands of visitors, very low revenue) | Mostly July | Flagged for review; kept in data |

![Cleaning notes](06_cleaning_notes.png)

---

## 2. Analysis
Four pivot tables, plus a calculated field: **Revenue per Visitor = Revenue / Visitors**.

- Revenue and visitors by month
- Top 10 car brands
- Revenue per visitor by body style
- Top 10 states

---

## 3. Key Insights

**1. July's spike was high traffic, not high value.**
July delivered 61% of revenue and 91% of visitors, but each visitor was worth only **$1.29**, compared with **$9.67–$11.58** in normal months (Jan, Mar, Apr, Sep).

**2. SUVs attract the most traffic but the least value.**
SUVs drew 76% of all visitors but earned just **$0.74 per visitor**. Wagons ($9.27) and hatchbacks ($9.19) earned over 12× more per visitor.

**3. The messy data was linked to the problem traffic.**
The 570 inconsistently capitalised rows had 241,901 visitors but only $6,975 revenue (about 3 cents per visitor), mostly in July and May. This suggests a separate or faulty tracking source.

**4. Biggest market isn't the most efficient.**
California generated the most revenue ($627,781) but the lowest revenue per visitor of the top 10 states ($1.80). Pennsylvania converted best ($2.26).

**5. Brands:** Ford led revenue ($579,861). Jeep drew more visitors than Toyota but earned less than half its revenue.

---

## 4. Recommendations
- Investigate the July (and May) traffic source before using it to plan marketing spend.
- Track **revenue per visitor**, not just traffic volume, as a core KPI.
- Review SUV landing pages and campaigns to understand why SUV visitors convert so poorly.

---

## 5. Dashboard
The dashboard includes KPI cards, four pivot charts, and slicers that filter every chart by **month** and **body style**.

![July filtered](12_dashboard_july.png)

---

## About
Created by **Ramalakshmi P**, a Computer Science graduate and aspiring data analyst based in Adelaide, South Australia.

- Portfolio: [datascienceportfol.io/ramalakshmipallinti1](https://www.datascienceportfol.io/ramalakshmipallinti1)
- GitHub: [github.com/Ramalakshmi-data](https://github.com/Ramalakshmi-data)

*Dataset provided as part of a data analytics course and used for learning purposes.*
