# 📊 Latest Bullish/Bearish close; MACD + RSI Enhanced Strategy

A Pine Script trading strategy that combines **MACD** and **RSI** indicators with additional candlestick validation for more precise trade entries. Designed for use in TradingView, this script helps traders identify high-probability trades by integrating technical analysis and candlestick pattern rules.

---

## 🌟 Key Features

- **MACD and RSI Integration**: Combines two popular momentum indicators for enhanced trade confirmations.
- **Candlestick Validation**: Filters entries based on full-body candle thresholds and wick size.
- **Customizable Parameters**: Fully adjustable input settings for MACD, RSI, and candlestick thresholds.
- **Dynamic Trade Management**: Includes stop-loss and take-profit levels based on candlestick range.

---

## 🔧 Strategy Parameters

| Parameter                | Description                                               | Default Value |
|--------------------------|-----------------------------------------------------------|---------------|
| **Full Candle Threshold**| Minimum ratio of the body to total candle range.          | `0.55`        |
| **Small Wick Threshold** | Maximum ratio of wick size relative to candle range.      | `0.35`        |
| **RSI Threshold**        | RSI value used to confirm bullish/bearish momentum.       | `50`          |
| **RSI Period**           | Lookback period for RSI calculation.                     | `14`          |
| **MACD Fast Length**     | Fast EMA length for MACD calculation.                    | `12`          |
| **MACD Slow Length**     | Slow EMA length for MACD calculation.                    | `26`          |
| **MACD Signal Length**   | Signal line EMA length for MACD.                         | `9`           |

---

## 📊 Entry and Exit Rules

### Entry Conditions
1. **Bullish Entry**:
   - Candle body must meet the full-body threshold.
   - Wick size must be within the defined small wick threshold.
   - **MACD**: Bullish crossover (`MACD Line > Signal Line`).
   - **RSI**: Above the RSI threshold (`RSI > 50`).

2. **Bearish Entry**:
   - Candle body must meet the full-body threshold.
   - Wick size must be within the defined small wick threshold.
   - **MACD**: Bearish crossover (`MACD Line < Signal Line`).
   - **RSI**: Below the RSI threshold (`RSI < 50`).

### Exit Rules
- Stop-loss is set at the low (for long trades) or high (for short trades) of the entry candle.
- Take-profit is calculated as the entry price plus or minus the candle body size.

---

## 🔧 How to Use

1. **Copy the Code**:
   - Open the `.pine` file or copy the code provided in this repository.

2. **Paste in TradingView**:
   - Go to TradingView and open the **Pine Editor**.
   - Paste the code and click **Add to Chart**.

3. **Customize Inputs**:
   - Adjust parameters such as thresholds, RSI period, or MACD settings to fit your trading style.

4. **Backtest**:
   - Use TradingView’s strategy tester to analyze the performance.

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more details.

---

## 🙌 Acknowledgements

- Inspired by popular MACD and RSI trading strategies.
- Special thanks to the TradingView community for their support and feedback.

---

Enjoy trading and let me know how this strategy performs for you!