# Trend Following Strategy with Volatility Filter

This project implements a trend-following trading strategy using **Python**. The strategy combines three technical indicators—**Moving Average (MA)**, **Average True Range (ATR)**, and **Relative Strength Index (RSI)**—to generate buy and sell signals. The strategy is backtested on historical stock data and visualizes its performance.

## Built With
- **Python**
- **Pandas** - For data manipulation and analysis
- **NumPy** - For numerical operations
- **Matplotlib** - For visualizations
- **yFinance** - For fetching historical stock data

## The Strategy

The strategy evaluates three main indicators when deciding whether to enter or exit a position:

### 1. **Moving Average (MA)**
The **20-period Simple Moving Average (SMA)** is used to identify the trend. The strategy generates buy and sell signals based on the price's relationship with this moving average.

- **Buy Signal**: When the stock price is above the 20-period SMA.
- **Sell Signal**: When the stock price is below the 20-period SMA.

### 2. **Average True Range (ATR)**
The **ATR** measures the stock's volatility. A higher ATR indicates increased price movement.

- **Volatility Filter**: The ATR must be above a specified threshold (default: 3) for signals to be considered valid.

### 3. **Relative Strength Index (RSI)**
The **RSI** is used to assess whether the stock is overbought or oversold.

- **RSI Buy Condition**: The RSI must be below 70 (not overbought).
- **RSI Sell Condition**: The RSI must be above 30 (not oversold).

## Trading Rules

### **LONG:**
Enter a long position if:
- Volume is above the average (implying strong market interest).
- The stock price is above the 20-period Moving Average.
- The stock's ATR is above the threshold.
- The RSI is below 70.

### **SHORT:**
Enter a short position if:
- Volume is above the average.
- The stock price is below the 20-period Moving Average.
- The stock's ATR is above the threshold.
- The RSI is above 30.

## Backtesting and Performance

- The strategy is backtested on historical stock data using **cumulative returns**.
- The performance is compared to a **buy-and-hold strategy**.

## Key Advantages of the Strategy:
- **Objective, rules-based approach**.
- **Combines trend-following with volatility filtering**.
- **Can be applied to multiple stocks and market conditions**.

Feel free to contribute, report issues, or suggest improvements to the strategy! 🚀

## How to Run
1. Clone the repository:

```bash
git clone https://github.com/yourusername/trading-strategy.git
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Jupyter notebook:

```bash
jupyter notebook
```

## License
This project is licensed under the MIT License.
