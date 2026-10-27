# Python EUR/USD FOREX TRADING ANALYSIS AND PREDICTION
This project analyses daily EUR/USD forex data (2003–2023, about 7,200 records) using Python and pandas. It tests two trading ideas: whether the first candle after the weekend predicts the trend over the next few days, and whether bullish and bearish engulfing candlestick patterns can predict future price movement. Using Python, pandas, matplotlib. Analysis of 20 years of daily EUR/USD forex data to test whether weekend-gap candles and engulfing candlestick patterns can predict short-term price trends.

## Overview

This project uses Python and pandas to explore historical EUR/USD price data (2003-2023, about 7,200 daily records) and test two common trading ideas:

First candle after the weekend: does the direction of the first candle after a market gap predict the trend over the next few days?
Engulfing candlestick patterns: do bullish and bearish engulfing patterns predict the direction of the next candle and the price change that follows?

File: EURUSD_FOREX.csv
Period: May 2003 to January 2023
Frequency: Daily candles
Columns: Gmt time, Open, High, Low, Close, Volume

## Methodology

### Part 1: Trend analysis

Converted the date column to a datetime index
Calculated a 5-period moving average of the closing price
Identified the first candle after the weekend (volume above zero after a zero-volume candle)
Defined the future trend by comparing the close with the average of the next 4 closes
Compared the first candle's direction with the future trend to measure prediction accuracy

### Part 2: Engulfing candles

Detected bullish and bearish engulfing patterns with a custom function
Checked whether the pattern correctly predicted the direction of the next candle
Calculated the average future price change (absolute and percentage) over the next 4 candles for each pattern

### Part 3: Candlestick visualisation

Plotted candlestick charts with matplotlib to visualise trends, bullish and bearish candles

## Charts
EUR/USD Closing Price (2003-2023) : 

<img width="683" height="517" alt="EUR_USD_close_price_trend" src="https://github.com/user-attachments/assets/7649c04d-0850-4b6a-b5b7-42b620f06716" />

Candlestick Chart: Bullish, Bearish and Trend : 

<img width="1673" height="706" alt="candlestick_trend_example" src="https://github.com/user-attachments/assets/1fa71b6d-69bc-42f3-b59e-d93991bb97e7" />


## Key Results
<img width="1033" height="482" alt="Key-Results-Trading-Analysis-Pediction" src="https://github.com/user-attachments/assets/e5165d92-0547-48ea-80e7-cf9f78260930" />



## Project Structure

eurusd-forex-analysis/
├── data/
│   └── EURUSD_FOREX.csv
├── script/
│   └── eurusd_analysis_prediction.ipynb
├── report/
│   └── eurusd_analysis_report.docx
├── screenshots/
│   ├── candlestick_trend_example.png
│   └── eurusd_close_price_trend.png
├── LICENSE
├── README.md
└── requirements.txt

## How to Run

### 1. Clone the repository
git clone https://github.com/shresthasarkar-ds/Python-EUR-USD-FOREX-TRADING-ANALYSIS-AND-PREDICTION.git
cd eurusd-forex-analysis

# 2. Install the requirements
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook/colab script/eurusd_analysis_prediction.ipynb

The notebook reads the data from ../data/EURUSD_FOREX.csv, so run it from inside the script/ folder.

## Tools Used
Python
pandas
matplotlib
Jupyter Notebook
Google Colab

## Disclaimer
This project is for educational purposes only and is not financial advice. Past price patterns do not guarantee future results.

## Author
Shrestha Sarkar MBA (Finance & Business Analytics), ISBR Business School, Bangalore

## License
This project is licensed under the MIT License. See the LICENSE file for details.
