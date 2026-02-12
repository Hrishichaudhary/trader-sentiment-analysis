# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how Bitcoin market sentiment influences trader behavior, performance, and risk-taking patterns using historical Hyperliquid trading data and Bitcoin Fear–Greed sentiment data.

The goal is to identify behavioral patterns and derive actionable trading insights based on sentiment regimes.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset
This dataset contains daily Bitcoin market sentiment indicators.

Key columns used:
- timestamp – Unix timestamp of the sentiment record  
- value – Sentiment index value  
- classification – Sentiment label (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)  
- date – Calendar date used for alignment with trades  

The **classification** column was primarily used to analyze trader behavior under different sentiment regimes.

---

### 2. Historical Trader Dataset (Hyperliquid)
This dataset contains trade-level records of traders.

Key columns used:
- Account – Unique trader identifier  
- Coin – Asset traded  
- Execution Price – Price at which the trade was executed  
- Size Tokens – Quantity traded in tokens  
- Size USD – Trade size used as a proxy for risk exposure  
- Side – Buy/Sell direction  
- Timestamp IST – Trade timestamp  
- Direction – Position action  
- Closed PnL – Profit or loss realized on the trade  
- Fee – Transaction fee  
- Trade ID – Unique trade identifier  

These features were used to evaluate trader performance, trading behavior, and risk exposure across sentiment regimes.

---

## Methodology

### 1. Data Cleaning and Preparation
- Checked dataset structure, missing values, and duplicates  
- Converted timestamps to proper datetime format and extracted date for alignment  
- Merged trader data with daily sentiment data  
- Excluded trades without matching sentiment labels to ensure consistency in sentiment-based analysis

### 2. Feature Engineering
The following features were derived to better analyze trader behavior and performance:

- **is_profitable** – Binary flag indicating whether a trade resulted in profit, used as a proxy for win rate.
- **abs_pnl** – Absolute value of Closed PnL used to analyze loss severity and outcome magnitude.
- **risk_exposure_usd** – Trade size in USD used as a proxy for capital at risk.
- Trader-level aggregations were computed to analyze behavior patterns beyond individual trades.  

### 3. Analysis
- Performance comparison across sentiment regimes (Average PnL, Win Rate)
- Loss severity and trade outcome distribution analysis
- Risk-taking behavior analysis using trade size
- Trade activity comparison across sentiment regimes
- Trader segmentation and behavior comparison (profitable vs losing traders)  

---

## Key Insights
- Trader profitability varies across sentiment regimes.  
- Loss severity increases during Greed conditions.  
- Risk exposure increases in high sentiment periods.  
- Consistent traders maintain performance across regimes.  

---

## Strategy Recommendations

### 1. Sentiment-aware risk management
Reducing position size or risk exposure during highly volatile or overly optimistic market conditions can help reduce losses.

### 2. Trader segmentation-based allocation
Allocating capital toward consistent performers rather than highly reactive traders can improve long-term performance.

---

## Methodology Summary

The analysis investigates how Bitcoin market sentiment influences trader behavior and profitability. Two datasets were used: historical trader data from Hyperliquid and a daily Bitcoin sentiment dataset.

Data was cleaned, timestamps standardized, and trades aligned with daily sentiment. Key metrics such as trade frequency, profitability, and risk exposure were derived to compare trader performance across sentiment regimes.

Behavioral patterns were analyzed using visualizations and trader segmentation techniques.

---

## Key Findings

The analysis shows that market sentiment significantly affects trader behavior and performance. Greed conditions generally increase profitability but also increase risk and performance dispersion among traders.

Trade frequency and capital deployment vary across sentiment regimes, indicating behavioral adaptation by traders.

Trader segmentation revealed that consistent traders maintain stable performance across different sentiment conditions.

---

## How to Run

1. Clone the repository  
2. Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```
3. Open the notebook and run all cells.

# Tools Used
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn

## Strategy Recommendations

Two actionable strategies emerged:

### 1. Sentiment-aware risk management
Reducing leverage or position size during highly volatile or overly optimistic market conditions can reduce losses.

### 2. Trader stability-based allocation
Allocating capital toward consistent traders rather than high-risk traders can improve long-term performance.
