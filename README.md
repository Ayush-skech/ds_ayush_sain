Trader Behavior vs Market Sentiment

This project explores how crypto traders' performance (PnL, win rate, trade size, risk-taking) changes across market sentiment phases (Fear, Greed, Neutral).

The analysis combines two datasets:

1. `historical_data.csv` → individual trader activity from Hyperliquid
2. `fear_greed_index.csv` → Bitcoin Fear & Greed Index

## How to Run

Open the analysis notebook in Google Colab:
`Click here for Notebook` :- https://colab.research.google.com/drive/1EOVafCH0f-bKl_kDEGvt5AfY6T2tWdW_?usp=sharing

Steps:

1. Upload the raw datasets:
    `historical_data.csv`
    `fear_greed_index.csv`
2. Run all cells in order.
3. Outputs will be generated and saved automatically into:
    `csv_files/` → processed CSV datasets
    `outputs/` → plots and visualizations

## Steps in the Analysis

### 1. Data Cleaning & Preprocessing
    1. Converted timestamps into standard date format
    2. Normalized sentiment categories (Fear, Greed, Neutral)
    3. Merged trader dataset with sentiment by date

### 2. Feature Engineering
    1. Added is_win flag (profitable vs unprofitable trade)
    2. Created daily-level aggregates (total PnL, average PnL, win rate, avg trade size)
    3. Built account-level summaries by sentiment

### 3. Exploratory Analysis
    1. Distribution of PnL across sentiments
    2. Win rate differences between Fear and Greed
    3. Trade size patterns across moods
    4. Daily total PnL time series

## Key Findings
    1. Traders tend to take larger trades during Greed phases.
    2. Win rate is higher in Greed compared to Fear periods.
    3. PnL is more volatile in Greed (bigger wins and bigger losses).
    4. Fear phases are associated with smaller, more cautious trades.

## Outputs
### Processed CSVs (csv_files/)
`trader_sentiment_data.csv` → merged dataset with sentiment labels
`daily_sentiment_summary.csv` → daily aggregates
`account_sentiment_summary.csv` → account-level summaries
`sentiment_overall_summary.csv` → overall summary by sentiment

### Visualizations (outputs/)
`boxplot_pnl_by_sentiment.png` → PnL distribution across sentiments
`bar_winrate_by_sentiment.png` → Win rate across sentiments
`bar_avgsize_by_sentiment.png` → Avg trade size across sentiments
`timeseries_total_pnl.png` → Daily total PnL over time

## Report
A detailed summary of methodology, results, and insights is provided in:
`ds_report.pdf`

This report explains the problem, approach and findings.
