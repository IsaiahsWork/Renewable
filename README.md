
# 📈 Renewable Energy Stock Analysis (Jan–Jul 2025)

## 🌍 Background & Project Overview

Clean energy stocks have gained traction due to a global push for decarbonization and renewable energy transition. This project analyzes five leading companies from January 1, 2025, to July 1, 2025, using Python and financial data.

### Companies Analyzed:
- **Sunrun (RUN)** – Residential solar services
- **Enphase (ENPH)** – Solar microinverters and battery storage
- **ChargePoint (CHPT)** – EV charging networks
- **Generac (GNRC)** – Backup and clean energy systems
- **SolarEdge (SEDG)** – Solar inverters and smart energy

We aim to uncover performance trends, investor behavior, and inter-stock relationships using daily stock data fetched via `yfinance` and processed with Pandas and Matplotlib.

---

## 🗂️ Data Structure Overview

All CSVs share this format:

| Column           | Description                            |
|------------------|----------------------------------------|
| Date             | Daily trading date                     |
| Open, High, Low, Close | Daily price movement            |
| Volume           | Shares traded                          |
| Total Traded     | Close × Volume (USD)                   |
| MA10, MA30, MA50 | Moving averages (10, 30, 50 days)      |
| returns          | Daily return %                         |
| Cumulative Returns | Compounded return over time         |

---

## 📊 Executive Summary

### 📌 Key Findings (Jan 2–6, 2025):

| Ticker | Opening Price Growth | Story |
|--------|----------------------|-------|
| SEDG   | +28%                 | Strong institutional buying likely driven by favorable export data |
| RUN    | +7.4%                | Rise in residential installations post DOE incentive program |
| CHPT   | +7.1%                | Boost from U.S. EV infrastructure disbursements |
| GNRC   | +1.9%                | Modest growth due to increased winter storm outages |
| ENPH   | ~0%                  | Market-neutral response, likely priced in |

### 📈 Trends:
- 📊 Early 2025 saw momentum driven by new U.S. Department of Energy tax credits and policy implementation.
- 🔁 High correlation found between Enphase and SolarEdge stocks.
- 💰 Volume spikes aligned with major announcements and earnings season.

---

## 🔍 Insights Deep Dive (Script-Based)

All insights use code and calculations from the provided notebook.

---

### 📈 Insight 1: Price Trajectory Comparison

**Code Used:**
```python
key = pd.concat([...], axis=1)
key.plot()
```

**What It Does:** Compares `Open` prices for all stocks side-by-side.

**Quantified Insight:**
- SEDG jumped from $14.80 → $19.00 = **+28%**
- CHPT: $1.12 → $1.20 = **+7.1%**
- RUN: $10.21 → $10.97 = **+7.4%**

**📉 Business Metric:** Opening price growth in %  
**📖 Story:** SolarEdge and Sunrun rallied on investor optimism linked to earnings guidance and IRA subsidy execution.

---

### 📉 Insight 2: Trading Volume Patterns

**Code Used:**
```python
volume = pd.concat([...], axis=1)
volume.plot()
```

**What It Does:** Compares daily volume traded across all tickers.

**Quantified Insight:**
- ENPH hit **3.24M** shares traded on Jan 6
- SEDG and RUN also peaked that day

**📉 Business Metric:** Daily volume > 2x 5-day average signals investor interest  
**📖 Story:** Volume spikes match price surges, indicating momentum or institutional action likely tied to Q4 2024 earnings announcements.

---

### 🔗 Insight 3: Cross-Correlation Between Stocks

**Code Used:**
```python
returns = key.pct_change()
returns.corr()
```

**What It Does:** Calculates Pearson correlation between daily returns.

**Quantified Insight:**
- ENPH ↔ SEDG = **+0.88** (very high)
- CHPT shows weak correlation with any other (< 0.3)

**📉 Business Metric:** Correlation Coefficient (r)  
**📖 Story:** Solar stocks tend to move together; EV stock (CHPT) operates in a different investor narrative.

---

### 📊 Insight 4: Cumulative Return Analysis

**Code Used:**
```python
cumulative_returns = (1 + key.pct_change()).cumprod()
cumulative_returns.plot()
```

**What It Does:** Tracks return on $1 invested on Jan 2.

**Quantified Insight (3-Day Cumulative):**

| Stock | Return |
|-------|--------|
| SEDG  | +28%   |
| RUN   | +7.4%  |
| CHPT  | +7.1%  |
| GNRC  | +1.9%  |
| ENPH  | ~0%    |

**📉 Business Metric:** Compounded cumulative return  
**📖 Story:** SEDG’s outperformance may be tied to solar hardware demand increase. ENPH lagged likely due to neutral forecast.

---

### 🧮 Insight 5: Scatter Matrix (Visual Relationships)

**Code Used:**
```python
scatter_matrix(key, alpha=0.2, figsize=(10,10), diagonal='kde')
```

**What It Does:** Plots variable relationships

**Quantified Insight:**
- Clear diagonal cluster between SEDG and ENPH
- CHPT’s points show broad scatter (weak relationship)

**📉 Business Metric:** Visual correlation confirmation  
**📖 Story:** CHPT trades independently of solar sector trends, supporting findings in correlation matrix.

---

## ✅ Recommendations

Based on this script-driven analysis:

### 📌 For Investors:
- 🟢 **Bullish bias** on SEDG and RUN short term due to strong returns and volume
- 🟡 Watch CHPT closely for policy-linked swings
- 🔵 Monitor earnings calendar and DOE grant releases for next catalysts

### 📌 For Analysts:
- Add RSI/MACD indicators for trade signals
- Run regression on volume vs. policy events
- Expand to risk-adjusted metrics like Sharpe Ratio

---

## 🛠️ Tools Used

- `yfinance`: Stock data
- `pandas`: Analysis
- `matplotlib`: Visualization
- `numpy`: Financial math
- `scatter_matrix`: Correlation plots

---
