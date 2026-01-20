# Trader Behavior vs Market Sentiment Analysis

Candidate: Atharav Dhumone  
Position: Junior Data Scientist – Web3 Trading Team

---

## 📌 Objective

The goal of this project is to analyze how trader behavior on Hyperliquid
aligns or diverges from overall Bitcoin market sentiment using the
Fear & Greed Index, and to identify behavioral patterns that can be used
to design smarter trading strategies.

---

## 📂 Datasets Used

1. Bitcoin Fear & Greed Index  
   Columns:
   - date
   - classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)
   - value

2. Hyperliquid Historical Trader Data  
   Key Columns:
   - Account
   - Coin
   - Execution Price
   - Size USD
   - Side
   - Timestamp IST
   - Closed PnL
   - Start Position

---

## ⚙️ Methodology

### Data Preprocessing
- Converted trade timestamps (Timestamp IST) into daily date format.
- Merged trader data with sentiment data using the date column.
- Removed missing values.
- Removed extreme outliers from Closed PnL and trade size using IQR method.

### Feature Engineering
- Sentiment Score: categorical sentiment mapped to numeric scale (0–4).
- Sentiment Shift: day-to-day change in sentiment score.
- Risk Proxy: since leverage is not available, trade Size in USD is used
  as a proxy for exposure.
- Profit Efficiency: Closed PnL divided by trade Size USD.

---

## 📊 Key Analysis Performed

1. Sentiment Alignment  
   - Measured how average trade size changes across sentiment regimes.
   - Found higher exposure during Greed and Extreme Greed phases.

2. Profitability vs Sentiment  
   - Compared average Closed PnL across sentiment categories.
   - Fear phases sometimes show better profit efficiency.

3. Alpha Trader Identification  
   - Selected top 10% accounts based on cumulative PnL during Fear periods.
   - These traders act contrarian to market emotion.

4. Cumulative PnL vs Sentiment  
   - Tracked cumulative profit of top traders against sentiment score.
   - Rising PnL during Fear indicates smart money accumulation.

---

## 🚀 Actionable Insights

- When sentiment is Fear but top trader profitability is increasing,
  it may indicate accumulation and potential upward reversal.

- When sentiment is Extreme Greed and exposure increases sharply,
  risk of volatility and liquidation rises, suggesting risk reduction.

These behavioral signals can be integrated into:
- Automated trading strategies
- Risk management systems
- On-chain trading dashboards

---


