Norwegian Air Shuttle financial analysis dataset
================================================

Files
-----
1. norwegian_financials_raw.csv
   Raw reported inputs used for the agreed ratio analysis.
   Monetary values are NOK million unless otherwise stated.

2. norwegian_sources.csv
   Source report and page for each raw input, for manual verification.

3. norwegian_context.csv
   Major events affecting comparability and trend interpretation.

Why 2020 is included
--------------------
The assignment analyses 2021-2025, but ROCE and Sales Revenue to Capital Employed
use AVERAGE capital employed. The 2020 closing balance is therefore needed as the
opening balance for FY2021.

Agreed ratios
-------------
Profitability:
- Operating Profit Margin = EBIT / Revenue
- ROCE = EBIT / Average Capital Employed

Efficiency:
- Sales Revenue to Capital Employed = Revenue / Average Capital Employed
- Sales Revenue per Employee = Revenue / employee equivalent

Liquidity:
- Current Ratio = Current Assets / Current Liabilities
- Acid-Test Ratio = (Current Assets - Inventory) / Current Liabilities

Financial gearing:
- Gearing Ratio = Non-current interest-bearing debt /
                  (Equity + Non-current interest-bearing debt)
  In the dataset, non-current interest-bearing debt should be built from
  non-current borrowings + non-current lease liabilities.
- Interest Cover = EBIT / Interest Expense

DuPont:
- ROCE = Operating Profit Margin * Sales Revenue to Capital Employed

Altman Z-score 2024-2025
------------------------
The raw dataset includes total assets, retained earnings, EBIT, total liabilities,
revenue, current assets/current debt components, year-end share price and shares
outstanding.

For Market Value of Equity, calculate:
MVE = year_end_share_price_nok * shares_outstanding / 1,000,000

Important Altman working-capital note:
The project instruction defines WC as "current assets - non-interest-bearing liabilities".
Before final calculation, confirm whether the instructor intends current
non-interest-bearing liabilities. A reasonable candidate based on the reported balance
sheet is:
current non-interest-bearing liabilities =
current liabilities - current borrowings - current lease liabilities

Do not silently substitute a different working-capital definition without confirming it.

Employee measure
----------------
Norwegian reports "man-labor years" for 2021-2024 and "full-time equivalent" in 2025.
These are period employee-equivalent measures and are used as the closest reported
measure to the lecture's average number of employees.

No ratios are hardcoded in the raw CSV. Calculate them in Jupyter after verification.
