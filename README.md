# Trader Performance vs Market Sentiment Analysis

## Overview
This project analyzes how Bitcoin market sentiment (Fear vs Greed) influences trader behavior and performance using historical Hyperliquid trading data and sentiment data.

The goal is to identify behavioral patterns and derive actionable trading insights based on sentiment regimes.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset
Contains daily sentiment classification:
- Fear  
- Greed  
- Extreme Fear  
- Extreme Greed  
- Neutral  

### 2. Historical Trader Dataset
Contains trade-level information including:
- Account  
- Coin  
- Execution price  
- Trade size (USD)  
- Side  
- Timestamp  
- Closed PnL  
- Leverage  

---

## Methodology

### 1. Data Cleaning and Preparation
- Removed duplicates and missing values  
- Converted timestamps  
- Aligned trades with daily sentiment data  

### 2. Feature Engineering
- Daily trader PnL  
- Trade frequency  
- Risk exposure (Size USD)  
- Win rate proxy  

### 3. Analysis
- Performance comparison across sentiment regimes  
- Trader behavior analysis  
- Trader segmentation  

---

## Key Insights
- Trader profitability varies across sentiment regimes.  
- Loss severity increases during Greed conditions.  
- Risk exposure increases in high sentiment periods.  
- Consistent traders maintain performance across regimes.  

---

## Strategy Recommendations

### 1. Sentiment-aware leverage control
Reduce leverage or position size during highly volatile or greedy market phases.

### 2. Trader segmentation-based allocation
Allocate more capital to consistent performers rather than highly reactive traders.

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

## Strategy Recommendations

Two actionable strategies emerged:

### 1. Sentiment-aware risk management
Reducing leverage or position size during highly volatile or overly optimistic market conditions can reduce losses.

### 2. Trader stability-based allocation
Allocating capital toward consistent traders rather than high-risk traders can improve long-term performance.
