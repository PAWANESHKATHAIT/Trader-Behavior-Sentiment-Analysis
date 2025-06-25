# Junior Data Scientist Assignment: Trader Behavior Insights

## Project Overview

This project is the first step of the hiring process for a Junior Data Scientist role, focusing on analyzing the relationship between cryptocurrency trader performance and market sentiment. The objective is to explore historical trading data alongside Bitcoin market sentiment to uncover patterns and deliver actionable insights for smarter trading strategies.

## Assignment Objective

The core objective is to:
- Explore the relationship between trader performance and market sentiment.
- Uncover hidden patterns within the combined datasets.
- Deliver insights that can drive smarter trading strategies.

## Datasets

Two primary datasets were used in this analysis:

1.  **Bitcoin Market Sentiment Dataset (`fear_greed_index.csv`)**:
    * **Columns:** `timestamp`, `value`, `classification`, `date`
    * Provides daily sentiment (Fear/Greed) for the Bitcoin market.

2.  **Historical Trader Data from Hyperliquid (`historical_data.csv`)**:
    * **Columns:** `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Direction`, `Closed PnL`, `Transaction Hash`, `Order ID`, `Crossed`, `Fee`, `Trade ID`, `Timestamp`
    * Contains granular trade-level data, including profit and loss.

## Analysis Steps

The analysis was performed using Python within a Jupyter Notebook and followed these key steps:

1.  **Data Loading & Initial Inspection:** Loading both datasets and understanding their initial structure and data types.
2.  **Data Preprocessing & Merging:**
    * Converting date/time columns to a consistent format (`Timestamp IST` and `date`).
    * Merging the trader data with the sentiment data based on date.
    * Handling missing sentiment values by dropping irrelevant rows.
3.  **Data Type Conversions:** Ensuring all numerical columns critical for analysis (`Closed PnL`, `Execution Price`, `Size USD`, `Fee`, `value`) were correctly cast to numeric types.
4.  **Feature Engineering:** Creating new features to enrich the analysis, including:
    * `Day_of_Week`: Day of the week the trade occurred.
    * `PnL_Category`: Categorizing trades as 'Profitable', 'Loss-making', or 'Breakeven'.
    * `PnL_per_USD`: Normalized profit/loss per unit of trade size (USD).
    * `Time_Segment`: Categorizing trades into 'Morning', 'Afternoon', 'Evening', 'Night' based on trade time.
5.  **Exploratory Data Analysis (EDA):** Visualizing and summarizing the data to identify patterns in trader performance across different market sentiment classifications, win rates, and average profitability.

## Key Findings & Insights

*(**IMPORTANT:** Replace these placeholder bullet points with your actual, specific insights from your Jupyter Notebook. This is where you demonstrate your findings.)*

* **Sentiment's Impact on Profitability:** [e.g., "Traders exhibited a higher average 'Closed PnL' during 'Extreme Fear' periods, suggesting a potential contrarian opportunity during market downturns."]
* **Win Rate vs. Average PnL:** [e.g., "While 'Extreme Fear' offered higher average PnL, 'Neutral' sentiment periods demonstrated a higher overall win rate, indicating more consistent but potentially smaller gains."]
* **Behavioral Patterns:** [e.g., "Analysis of PnL categories revealed that 'Greed' periods saw a higher proportion of 'Loss-making' trades compared to 'Fear' periods, possibly due to overconfidence or higher risk-taking."]
* **Actionable Strategies:** [e.g., "Based on these findings, a recommended strategy could involve increasing exposure during periods of 'Extreme Fear' for potentially larger gains, and exercising caution or reducing position sizes during 'Extreme Greed' periods."]
* *(Add more bullet points as needed, referencing your plots and statistics.)*

## How to Run the Analysis

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/YourRepositoryName.git](https://github.com/YourUsername/YourRepositoryName.git)
    ```
    (Replace `YourUsername` and `YourRepositoryName` with your actual GitHub details.)
2.  **Navigate to the project directory:**
    ```bash
    cd YourRepositoryName
    ```
3.  **Install necessary libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
4.  **Open the Jupyter Notebook:**
    ```bash
    jupyter notebook Trader_Behavior_Sentiment_Analysis.ipynb
    ```
    The notebook will open in your web browser, and you can run all cells from top to bottom.

## Tools and Libraries Used

* Python 3.x
* Jupyter Notebook
* Pandas (for data manipulation and analysis)
* NumPy (for numerical operations)
* Matplotlib (for data visualization)
* Seaborn (for enhanced data visualization)

---
