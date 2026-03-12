# Retirement Income Calculator

A single-page HTML retirement income calculator that projects year-by-year household income and portfolio balances from your current age through age 100. No server, build tools, or dependencies required — just open `index.html` in a browser.

## Features

### Income Sources
- **Pension** — regular pension with optional COLA, or **FERS (Federal)** pension with automatic rules:
  - Base annuity fixed until age 62, then COLA-adjusted
  - Optional FERS Supplement paid from retirement through age 61 (no COLA), stops at 62
- **Social Security** — enter your estimated benefit at ages 62, 67, and 70; choose your planned claiming age
- **Investment accounts** — Traditional IRA/401(k), Roth IRA/401(k), and taxable brokerage tracked separately

### Spouse / Partner Support
- All income sources (pension, SS) can be entered for a spouse
- **Spousal SS benefit** option: automatically uses the higher of the spouse's own benefit or 50% of the primary's age-67 benefit
- Spousal benefit COLA correctly starts from when it first becomes available (the later of the spouse's claiming age or the primary's claiming age)

### Investment Withdrawal Strategies
Withdrawals follow tax-efficient ordering: **Taxable → Traditional → Roth** (beyond RMDs, Roth is always drawn last)

Four strategies to choose from:
1. **Fixed Amount** — a set annual withdrawal, inflation-adjusted each year
2. **Safe Withdrawal Rate** — a percentage of the portfolio balance each year
3. **Minimum Income Target** — withdrawals fill the gap between guaranteed income (pension + SS) and a target; set in 2026 dollars and inflation-adjusted annually
4. **RMDs Only** — take only the IRS-mandated minimum distributions

### Required Minimum Distributions (RMDs)
- Calculated using the IRS Uniform Lifetime Table
- RMD age automatically set per SECURE Act 2.0: age 73 (born 1951–1959) or age 75 (born 1960+)

### Tax Estimates
- Estimated federal income tax using approximate 2026 brackets, inflation-adjusted for future years
- Correct Social Security provisional income test (0%, 50%, or 85% of SS taxable)
- Standard deduction includes additional amount for taxpayers age 65+
- Effective tax rate shown alongside estimated tax

### Table Display
- Rows shown for every year from current age through 70, then at ages 75, 80, 85, 90, 95, and 100
- Columns automatically hidden when they have no data across the entire timeline (e.g. spouse pension column hidden if spouse has no pension)
- Toggleable column groups: Pension, Social Security, Investment Withdrawals, Total Income, Tax, After-Tax Income, Portfolio Balance, Account Detail, RMD Detail

### Assumptions
- Annual investment return rate
- Inflation rate (used for COLA adjustments and bracket indexing)
- Social Security COLA rate
- Tax filing status (Single, Married Filing Jointly, Head of Household)

## Usage

Open `index.html` in any modern web browser. Fill in your inputs and click **Calculate Retirement Income**. No data is sent anywhere — all calculations run locally in the browser.
