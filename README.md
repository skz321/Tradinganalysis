Trading Analysis Project
Project Overview

The goal of this project is to analyze my trading history over the past year to uncover patterns and insights that could help improve profitability. Specifically, I aim to answer questions such as:

What circumstances (time of day, day of week, or market events) are correlated with big wins or losses?

Is there any pattern in trade size vs return?

How can I reduce losses and improve win rates?

Dataset

Source: Webull Trading Account

Size: ~1120 rows, 11 columns

Columns:

Name — Name of the security

Symbol — Ticker symbol

Side — Buy or Sell

Status — Filled or Canceled

Filled — Number of shares filled

Total Qty — Quantity of trade

Price — Trade price

Avg Price — Average price of the security

Time-in-Force — Type of order

Placed Time — When the order was placed

Filled Time — When the order was executed

Preprocessing Steps

Remove canceled trades — Only filled trades are relevant for performance.

Convert numeric columns (Price, Avg Price, Total Qty) to numeric types.

Convert datetime columns (Placed Time, Filled Time) to datetime64 and strip timezone info.

Feature engineering:

Return % — Percentage return of each trade

Win/Loss/Break-even — Classification of trades

Trade Value — Price * Total Qty

Hour of Day and Day of Week for time-based analysis

Visualizations

Equity curve: Shows cumulative P/L over time

Distribution of trade returns: Histogram of % Return

Average P/L by day of week & hour of day: Helps identify time-based patterns

Holding time vs P/L: Boxplots to analyze profitability relative to trade duration

Trade size vs return: Scatter plot to see if bigger trades correlate with bigger gains/losses

Ticker analysis: Most traded symbols and their profitability

Win/Loss/Break-even ratio: Pie chart to see overall performance distribution

Insights

Preliminary observations suggest that many trades are break-even, with smaller wins and occasional large losses.

Certain days or hours might be more favorable for trading, which can be refined after further analysis.

Larger trades tend to have more variable returns, highlighting the importance of risk management.

How to Run

Ensure you have Python 3.x installed along with pandas, numpy, matplotlib, and seaborn.

Load the notebook and dataset (trades.csv).

Run the notebook sequentially from top to bottom to generate preprocessing and visualizations.

Future Work / Limitations

External factors such as FED meetings, earnings announcements, or market news are not included.

Trades are only from my personal account and may not generalize to other traders.

Could add more advanced analysis, like correlations between indicators or day-specific strategies.
