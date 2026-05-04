# Algorithmic Trading: Moving Average Crossover Dashboard

## Overview
This project is an automated algorithmic trading dashboard that tracks medium-term trend reversals for major National Stock Exchange (NSE) stocks. It pulls live historical market data, handles time-series indexing, and engineers quantitative features to detect established market signals.

## Core Logic: The Crossover Strategy
The model identifies trend momentum by calculating two distinct rolling averages to filter out daily price noise:
* **Fast Trend (20-Day MA):** Reacts quickly to recent price action.
* **Slow Trend (50-Day MA):** Represents the longer-term structural trend.

Algorithmic signals are generated mathematically when these two lines intersect:
* 📈 **Golden Cross (Buy Signal):** The 20-day MA crosses *above* the 50-day MA. This indicates that recent momentum is consistently outperforming the historical average, confirming a new upward trend.
* 📉 **Death Cross (Sell Signal):** The 20-day MA crosses *below* the 50-day MA. This indicates that short-term momentum is breaking down, confirming a sustained downward trend.

## Technical Stack
* **Data Extraction:** `yfinance` (Live market data API)
* **Data Engineering:** `pandas` (Time-series manipulation, rolling windows, signal detection)
* **Data Visualization:** `matplotlib.pyplot` (Multi-layered plotting, automated marker generation)
