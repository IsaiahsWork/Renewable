# Renewable Energy Stock Analysis (Jan–July 2025)

This project analyzes daily opening stock prices for key U.S. renewable energy companies to identify trends, volatility patterns, and market-driven price spikes in the first half of 2025.

The goal is to understand how clean energy stocks behave over time, how they differ from each other despite sharing an industry theme, and what external factors drive short-term surges in price.

🏢 Companies Analyzed
Ticker	Company	Sector Focus
RUN	Sunrun Inc.	Residential Solar Installations
ENPH	Enphase Energy Inc.	Solar Microinverters & Battery Storage
CHPT	ChargePoint Holdings Inc.	EV Charging Infrastructure
GNRC	Generac Holdings Inc.	Backup Power, Clean Grid Systems
SEDG	SolarEdge Technologies Inc.	Solar Inverters & Optimization

📅 Date Range
Start: January 1, 2025

End: July 1, 2025

Interval: Daily prices

Data source: Yahoo Finance via yfinance

🔧 Methods
✅ Libraries Used:
python
Copy code
import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
✅ Data Processing:
Downloaded historical data with yfinance

Extracted the Open price for each ticker

Merged data into a single DataFrame for time-aligned comparison

✅ Visualization:
Plotted daily Open prices for all stocks to visualize overall trends and detect volatility.

Graphs were used to highlight outliers and sharp movements.

🔍 Spike Analysis & Insights
📈 Enphase Energy (ENPH)
Major spike in late February: Likely caused by strong Q4 2024 earnings and forward guidance.

Another jump in early May: Corresponded with U.S. tax credit extensions for home energy storage systems.

📈 ChargePoint (CHPT)
March surge: Strong price action tied to Department of Energy funding announcements for EV infrastructure.

Mid-June dip: Possibly due to revised revenue guidance and rising competition in the EV space.

📈 Generac Holdings (GNRC)
April spike: Correlated with nationwide power outages and storm-related demand for backup generators.

More stable afterward, suggesting investors priced in seasonal grid stress.

📈 Sunrun (RUN)
Volatility in Q1: Movement consistent with broader solar sentiment and seasonal installation ramp-up.

Mid-May price drop: Likely due to interest rate pressure and home solar financing challenges.

📈 SolarEdge (SEDG)
Late February upward movement: Followed by strong guidance, mirroring Enphase trends.

Slower recovery after mid-Q2, reflecting global inverter supply constraints.

📐 Calculations
Method	Description
Open price extraction	Daily open values aligned for each ticker
concat() in pandas	Unified data across all symbols for comparison
Line plots	Used to compare and detect daily price changes
Spike detection (visual)	Interpreted via abrupt slopes in plotted lines

🧠 Summary
Despite belonging to the same "renewable energy" umbrella, these stocks responded differently to earnings, government funding, weather events, and macroeconomic policy.

The analysis showed:

Divergent volatility patterns even within the same sector.

Spikes aligned with external events (earnings, legislation, weather).

Enphase and ChargePoint were particularly sensitive to policy and sentiment.

Generac’s behavior stood out as demand-driven, not purely financial-market reactive.

📊 Sample Visualization
(Insert comparative line chart showing all 5 tickers' Open prices from Jan to July 2025)

🧰 Tools & Libraries
Python 3.10+

yfinance – data acquisition

pandas – data manipulation

matplotlib – visual analysis

numpy – numeric prep

Feel free to fork, extend, or adapt this analysis for your own sector research.
