# NZ Housing Affordability

Project repo for the NZ housing affordability research deliverable.
**Real data only — no mocks.**

## Structure

```
nz-housing-affordability/
├── index.html                       ← Chart.js shell, opens directly in browser
├── data/
│   ├── household_debt.csv           ✅ Real annual data, 1990–2025 (FRED BIS series)
│   ├── household_debt_quarterly.csv ✅ Real quarterly data, 1990 Q4 – 2025 Q3
│   ├── mortgage_rates.csv           ⚠️ Shell — to be populated from RBNZ B3
│   └── data_notes.md
├── src/                             ← (empty — data pipeline scripts go here)
├── wireframes/                      ← (empty — sketches go here)
└── docs/
    └── chart_proposal.md
```

## Opening the project

Double-click `index.html`. The chart renders immediately — no server, no install. The household debt series is embedded directly in the page (and mirrored in `data/household_debt.csv` for any tooling that prefers reading from disk).

The mortgage rate chart fills in once `data/mortgage_rates.csv` is populated.

## Data sources

| File | Source | Series ID |
|---|---|---|
| `household_debt.csv` | FRED (mirroring BIS) | `QNZHAM770A` |
| `mortgage_rates.csv` | RBNZ | Table B3 |

See `data/data_notes.md` for coverage details and methodology.

## Coverage gaps

- **Mortgage rates pre-1998:** RBNZ B3 starts June 1998. Earlier rates exist in archived bulletins but use different methodology.
- **1990 partial:** household debt has only Q4 1990 (BIS series start).
- **2025 partial:** household debt has 3 of 4 quarters; Q4 publishes mid-2026.
