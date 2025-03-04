# Binance Trade Data Analysis

## Overview
This project analyzes historical trade data from Binance accounts over 90 days. It calculates key financial metrics, ranks accounts based on performance, and visualizes the results.

## Features
- **Data Preprocessing:** Cleans and structures trade history data.
- **Feature Engineering:** Adds derived features like position type and win rate.
- **Financial Metrics Calculation:** Computes ROI, PnL, Sharpe Ratio, Win Rate, Maximum Drawdown (MDD), and total positions.
- **Ranking Algorithm:** Scores and ranks accounts based on weighted financial metrics.
- **Visualization:** Generates a bar chart for the top 20 accounts based on performance.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/sharmayash05/Binance_TradeData_Analysis.git
   ```
2. Install dependencies:
   ```sh
   pip install pandas numpy matplotlib seaborn
   ```

## Usage
1. Place your trade data CSV file (`trade_data.csv`) in the project directory.
2. Run the analysis script/jupyter file:
   ```sh
   python task.ipynb
   ```
3. The script will:
   - Clean and process the data
   - Compute financial metrics
   - Rank accounts based on weighted scores
   - Save the results in `top_20_accounts.csv`
   - Display a visualization of top accounts

## Code Structure
- **`flatten_data(filepath)`**: Parses and normalizes trade history from the CSV file.
- **`load_data(filepath)`**: Loads and processes the cleaned trade data.
- **`feature_engineering(df)`**: Adds position type and win rate features.
- **`max_drawdown(profit_series)`**: Calculates the maximum drawdown.
- **`calculate_metrics(df)`**: Computes ROI, PnL, Sharpe Ratio, Win Rate, and MDD.
- **`rank_accounts(metrics)`**: Scores and ranks accounts using weighted financial metrics.
- **`save_results(metrics, filename)`**: Saves top-ranked accounts to a CSV file.
- **`visualize_metrics(metrics)`**: Plots a bar chart of the top 20 accounts.

## Output Example
```
Top 20 Accounts with Scores:
                 Port_IDs     Score
63   3986814617275053313  0.441633
109  4029299190618134272  0.210096
97   4020204877254599680  0.190307
...
```

## Dependencies
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn

## Notes
- Ensure the trade data is in CSV format with a `Trade_History` column containing JSON-like lists.
- The `DtypeWarning` for mixed types can be ignored or resolved by specifying `dtype` options.
- Future updates may include additional financial indicators and improved ranking algorithms.

## License
This project is open-source under the MIT License.

