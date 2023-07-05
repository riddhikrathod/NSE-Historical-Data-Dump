# NSE-Historical-Data
This Python code fetches and stores historical data from NSE using the nselib and yfinance libraries.

The code covers data for the following indices: Broad Market Indices, Sectoral Indices, Thematic Indices, and Strategy Indices

The input_file.csv has the following columns:
1. TYPE: Index Type
2. INDEX: Index name to fetch data using nselib
3. ETF: ETF name to fetch data using Yahoo Finance
4. EXTRACT_DATA: Data extraction indicators - 
   * 1: fetch data using nselib
   * 2: fetch data using yfinance
   * 0: ignore Index/ETF since data not available from both

The data is saved in 2 folders: daily, weekly
  * daily: contains daily data for each Index/ETF, with file names indicating the start & end dates
  * weekly: contains weekly data for each Index/ETF, with file names inidcating the start and end dates.

Note:
1. The weekly price is reported as the Friday closing price
2. If the Friday closing price is unavailable, the Thursday closing price is used. If both are unavailable, the Wednesday closing price is considered, and so on.
