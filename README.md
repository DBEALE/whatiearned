# whatiearned

A single-file web app that shows what your lifetime earnings are really worth. Draw your income across your career and see the total in today's money after inflation, optionally after tax.

## Usage

Open `index.html` in a browser. There is no build step and no dependencies.

1. Set the **start year** of your career (1960–2025).
2. Pick a **currency** (GBP or USD) and an **income scale** for the chart's vertical axis.
3. Click and drag on the chart to draw your annual gross income. Touch is supported. Hover over a year to see its details.
4. Optionally switch on **Deduct approx. tax** to see net figures.

The summary cards show total gross earnings, the total in today's (2026) money, inflation added (or estimated tax paid when tax is on), and the average working year in real terms.

## Saving profiles

Profiles are saved by name in your browser's `localStorage`. They include start year, currency, income scale and the drawn curve. They stay in that browser and are not synced anywhere.

## Data and accuracy

- Inflation uses annual CPI figures for the UK (ONS) and US (BLS), hardcoded in `index.html`. Years without data fall back to 2.5%.
- Tax is a rough estimate for a single filer: UK 2024/25 income tax and employee NI, or US 2024 federal income tax and FICA. The current rates are applied to every year, not the rates of the year you earned the income.
- The figures are approximate and for illustration only.
