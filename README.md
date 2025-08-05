
# 📈 Hexad Master Strategy 

This TradingView Pine Script strategy detects and trades the **Hexad Reversal Pattern**, enhanced with optional filters and trailing stop exits for optimized backtesting and real-time use.

---

## 🔷 What is the Hexad Reversal Pattern?

The **Hexad Reversal Pattern** is a rare but effective **6-candle formation** that signals a **trend reversal**. It combines elements of exhaustion and momentum reversal over a short time window.

### 🟢 Bullish Hexad:
1. **First 3 candles** are bearish (red), showing downward momentum.
2. **Next 3 candles** are bullish (green), showing a reversal in sentiment.
3. The final (6th) candle **closes above** the **high of the 1st candle**, confirming the strength of the reversal.

### 🔴 Bearish Hexad:
1. **First 3 candles** are bullish (green), indicating upward momentum.
2. **Next 3 candles** are bearish (red), showing potential exhaustion.
3. The 6th candle **closes below** the **low of the 1st candle**, signaling a confirmed shift to the downside.

This pattern helps catch **early reversals** in short-term price structure, especially when combined with filters for volume, RSI, and trend.

---

## 🧠 Strategy Logic Summary

- Scans for valid Hexad patterns in either current or higher timeframe (MTF option).
- Applies confirmation filters:
  - `EMA 50`: Trend direction filter
  - `SMA 20 Volume`: Used for volume confirmation
  - `RSI 14`: Momentum filter
  - `9DMA`: Plotted for trend-following confirmation
  - `Candle`: Final candle breakout confirmation
- Executes **long or short trades** when all criteria are met.
- Uses a **trailing stop** for dynamic exits rather than a fixed bar count.

---

## ⚙️ Input Settings

| Setting                  | Description                                       |
|--------------------------|---------------------------------------------------|
| Enable MTF               | Use higher timeframe candles (e.g. 1H vs 15m)     |
| Higher Timeframe         | The timeframe used if MTF is enabled              |
| Bars to Hold             | Optional fallback holding time                   |
| Trend Filter             | Requires price to be above/below EMA 50          |
| Volume Filter            | Current volume must exceed 20-period SMA         |
| RSI Filter               | Confirms oversold (<30) or overbought (>70) zone |
| Candle Confirmation      | Final candle must break previous bar high/low    |

---

## 🔔 Alerts

Use built-in alert conditions:
- `Bullish Hexad Alert`
- `Bearish Hexad Alert`

---

## 📊 Visual Elements

- 🔺 Green Triangle: Bullish Hexad Pattern Detected
- 🔻 Red Triangle: Bearish Hexad Pattern Detected
- 🔵 Blue Line: 9DMA

---

## 🧪 Backtesting & Use

This strategy is designed to be run in TradingView’s Strategy Tester. It allows you to:
- Visualize every signal with arrows
- Adjust filters to balance aggressiveness and accuracy
- **Hexad Reserved Pattern**: In Japanese candlestick theory, consistent multi-bar patterns (like 5+ candles of one color) often precede mean-reverting or breakout behavior. This script aims to ride the continuation.
- Designed for **15-min and 1-hour charts** by default, but works on any timeframe.

---

## ✅ Setup Instructions

1. Open [tradingview.com](https://tradingview.com)
2. Open Pine Script Editor
3. Paste code from `HexadMasterStrategy.pine`
4. Click “Add to Chart”
5. Open Strategy Settings (gear icon) to configure filters
6. Run backtest and export results if needed

---

### Author:

This version is designed for full practical use in live markets or historical evaluation. 

Sunny Chase, All rights reserved, 2025
