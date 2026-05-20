# Data Notes

## Quick reference

| File                    | Status         | Coverage                        | Source                     |
|-------------------------|---------------|--------------------------------|----------------------------|
| `household_debt.csv`   | ✅ populated   | 1990–2025 (annual)             | FRED `QNZHAM770A` (BIS)    |
| `household_debt_quarterly.csv` | ✅ populated   | 1990 Q4 – 2025 Q3        | FRED `QNZHAM770A` (BIS)    |
| `mortgage_rates.csv`   | ⚠️ shell      | needs population               | RBNZ table B3              |

## One-paragraph notes

The household debt series (`household_debt.csv` and `household_debt_quarterly.csv`) is data from FRED series `QNZHAM770A`, which is the BIS "Total Credit to Households and NPISHs, Adjusted for Breaks, % of GDP" series for New Zealand. The brief asks for a "debt-to-income" ratio, but there is no single NZ source that publishes debt-to-disposable-income data continuously since 1990; the GDP-denominated BIS series is the only break-adjusted long-run series covering the whole period. Coverage: 140 quarterly observations from Q4 1990 to Q3 2025 (1990 has only Q4 of the BIS series starting point; 2025 has three out of four quarters with Q4 being published in mid-2026). Quarterly values are just simple means of the available quarters — no interpolation. The mortgage rate series (`mortgage_rates.csv`) is **not populated by default**: download RBNZ table B3 from the RBNZ statistics page (URL in the file header), extract the floating first-mortgage and 2-year fixed-rate columns, annualize monthly data, and populate rows here. The RBNZ's B3 series starts in **June 1998**, meaning that the 1990–present time window of the brief cannot be entirely covered — however, earlier rates can be found in RBNZ historical bulletins using a different methodology and shouldn't be spliced.

## Source URLs

- **Household debt:** https://fred.stlouisfed.org/series/QNZHAM770A — public, no API key required
- **Mortgage rates:** https://www.rbnz.govt.nz/statistics/series/exchange-and-interest-rates/retail-interest-rates-on-lending-and-deposits — RBNZ table B3 (XLSX download)