# Trader Profitability Analysis Based on Crypto Market Sentiment

This project investigates the relationship between cryptocurrency market sentiment and trader profitability. By merging historical trade data with the daily Fear & Greed Index, this analysis aims to determine if trading behavior and success rates are correlated with periods of widespread market fear versus greed.

## Project Workflow
1.  **Data Ingestion:** Loaded two distinct datasets:
    * `historical_data.csv`: A detailed log of individual crypto trades.
    * `fear_greed_index.csv`: Daily market sentiment data, classified as Fear, Greed, etc.
2.  **Data Cleaning & Preprocessing:**
    * Corrected the timestamp format in the trade data from milliseconds to a standard datetime format.
    * Created a common `date_only` key in both datasets to facilitate a merge.
3.  **Data Merging:** Combined the trade data and sentiment data into a single DataFrame based on the execution date of each trade.
4.  **Analysis & Aggregation:**
    * Calculated the average `Closed PnL` (Profit and Loss) grouped by market sentiment classification.
    * Calculated the total `Size USD` (trading volume) for each sentiment category.
5.  **Visualization:** Created a bar chart to visually compare the average trader profitability during different market sentiment periods (e.g., Fear vs. Greed).

## Key Findings
The analysis reveals a notable trend in trader profitability based on market sentiment:
-   **Greed:** Traders achieved the highest average profitability (PnL of $87.89) during periods of "Greed."
-   **Fear:** The second most profitable periods were during times of "Fear," with an average PnL of $50.04.
-   **Trading Volume:** The highest trading volume occurred during periods of "Fear," suggesting increased market activity when prices are potentially lower.

## Technologies Used
-   Python
-   Pandas
-   Matplotlib & Seaborn
-   Google Colab
-   Jupyter Notebook
