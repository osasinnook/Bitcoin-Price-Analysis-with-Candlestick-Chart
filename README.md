### Bitcoin Price Analysis with Candlestick Chart

#### Objective:
The objective of this project is to analyze Bitcoin price movements over the past year using historical market data and visualize it with a professional candlestick chart. The chart provides insights into daily Open, High, Low, and Close (OHLC) prices of Bitcoin, highlighting price trends and patterns.

#### Tools and Technologies:
- **Programming Language:** Python
- **Libraries Used:**
  - `pandas`: For data manipulation and analysis.
  - `plotly.graph_objects`: For creating interactive and visually appealing plots, specifically candlestick charts.
  - `requests`: For making HTTP requests to retrieve data from the CoinGecko API.

#### Data Sources:
- **CoinGecko API Endpoints:**
  1. Market Chart Data:
     - URL: `"https://api.coingecko.com/api/v3/coins/bitcoin/market_chart/range?vs_currency=usd&from=1692480000&to=1736707200"`
     - Provides hourly Bitcoin price data within a specific time range.
  
  2. OHLC (Open, High, Low, Close) Data:
     - URL: `"https://api.coingecko.com/api/v3/coins/bitcoin/ohlc?vs_currency=usd&days=365"`
     - Provides daily OHLC data for Bitcoin over the past 365 days.

#### Data Processing:
1. **Fetching Data:** 
   - HTTP requests are made to the CoinGecko API to fetch market chart and OHLC data using the provided URLs and headers.
   
2. **Data Extraction and Transformation:** 
   - Market chart data is extracted to obtain hourly Bitcoin prices, which are transformed into a pandas DataFrame (`df_market_chart`).
   - OHLC data is extracted to obtain daily Open, High, Low, Close prices, which are transformed into another pandas DataFrame (`df_ohlc`).
   - Both DataFrames are indexed by timestamp (`Time`) and then merged into `df_combined` based on their common timestamps.

#### Visualization:
- **Candlestick Chart:**
  - A candlestick chart is created using `plotly.graph_objects.Candlestick`, representing Bitcoin's daily price movements (Open, High, Low, Close) over the past year.
  - Green and red colors are used to distinguish between days where the closing price was higher or lower than the opening price, respectively.

#### Chart Customization:
- The chart title (`title`), axis labels (`xaxis_title`, `yaxis_title`), and layout (`template='plotly_dark'` for a dark theme) are customized to enhance readability and visual appeal.
- The x-axis range slider (`xaxis_rangeslider_visible=False`) is disabled to focus on the main chart area without distraction.

#### Conclusion:
This project demonstrates how to fetch, process, and visualize Bitcoin price data using Python and relevant libraries. The candlestick chart provides a clear and intuitive representation of daily price movements, making it valuable for technical analysis and decision-making in cryptocurrency trading and investment strategies.

This overview summarizes the methodology and outcomes of analyzing Bitcoin's price data, offering insights into trends and patterns observed over the past year. It serves as a foundational project for exploring more advanced analytics and visualizations in cryptocurrency markets.