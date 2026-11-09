# Stock Price Analysis: AAPL vs. MSFT

A small Jupyter notebook project exploring historical daily stock data for Apple (AAPL) and Microsoft (MSFT). It uses `yfinance` to download market data, `pandas` to calculate summaries and returns, and Matplotlib to visualize price trends and trading volume.

## What the notebook covers

- Download and inspect daily data for AAPL and MSFT.
- Compare closing prices and average daily trading volume.
- Resample Apple's closing prices to weekly and month-end observations.
- Calculate Apple's 20- and 200-session simple moving averages and identify golden/death crossovers.
- Summarize daily, weekly, month-end, and year-end percentage returns.
- Measure Apple's returns 30, 60, and 90 trading observations after crossover dates.

## Run it

1. Clone or download this repository and open `stock_analysis.ipynb` in Jupyter or Visual Studio Code.
2. Create and activate a Python environment, then install the notebook dependencies:

   ```bash
   python -m venv .venv
   # macOS/Linux
   source .venv/bin/activate
   # Windows PowerShell: .venv\Scripts\Activate.ps1
   python -m pip install pandas yfinance matplotlib jupyter
   ```

3. Select that environment as the notebook kernel and run the cells from top to bottom. The download cell requires an internet connection.

The notebook currently requests data from `2020-01-01` to `2025-12-31`. The `yfinance` end date is exclusive, so the final date returned can be earlier than December 31. The download is performed when the notebook runs; the project does not include a separate data file or automatically save downloaded data.

## Project contents

- `stock_analysis.ipynb` — data download, analysis, visualizations, and crossover study.
- `README.md` — project overview and setup instructions.

## Notes and limitations

- The analysis uses the `Close` field returned by `yfinance`; provider behavior and source data can change over time.
- Moving-average windows and forward-return horizons count trading observations, not calendar days. Weekend and market-holiday dates are not observations.
- A moving-average crossover is a simple historical signal, not a prediction or a trading recommendation. Results do not account for transaction costs, taxes, or other investment risks.
- This project is for educational and exploratory purposes only, not financial advice.
