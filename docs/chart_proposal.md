Chart Proposal — Two Economic Views

View 1: Mortgage rates vs household debt, dual-axis line (1998–2025)

Two lines on one timeline, but with two y-axes. On the left, the floating and 2-year fixed mortgage rates (running 0–12%). On the right, household debt as a share of GDP (25–100%). Both pull from the real annual files — `data/mortgage_rates.csv` and `data/household_debt.csv` — once we've populated the mortgage one.

Here's why this one's worth the trouble. The interesting thing in this data isn't obvious until you put the two series side by side: debt as a share of GDP just kept climbing, from 56% in 1998 to a 98% peak in 2021, even while the cost of borrowing was bouncing all over the place — 11% back in 1998, down to about 3% in 2020. Stack them on the same chart and you can see it straight away: when rates fell, people didn't pocket the savings, they borrowed more. Cheap money went into bigger mortgages, not smaller payments.

We can't put both on one axis (a 5% rate and a 90% ratio don't share a scale), and splitting them into two charts kills the comparison. Dual-axis is really the only option. The usual risk with these is that two lines on shared time can imply a correlation that isn't there, so we'll keep each line clearly tied to its own axis with colour, and avoid letting them cross right in the middle where it looks like a "moment."

View 2: Household debt-to-GDP over time, with event markers (1990–2025)

Just one line this time — debt as % of GDP from `data/household_debt_quarterly.csv` — but with four labelled markers on the points that actually matter: 2000 (61%, where the boom starts), 2009 (93%, the GFC plateau), Q1 2021 (98.3%, the all-time high), and 2023–25 (settling back to around 90%). Y-axis runs 20–100%. We'll also drop a faint horizontal line at the 1990–2005 average of roughly 55%, so people can see how far above the old normal we've ended up.

One number tracked over a long stretch is the clearest way to show a slow structural shift. Without the markers it's just a line going up; with them, it becomes a story you can point at — the early-2000s boom, the GFC pause, the COVID spike. The reference line quietly answers the "is 90% actually a lot?" question without us having to spell it out. And because the BIS series is break-adjusted, we get the whole 35 years in one clean line, no methodology seams to apologise for.