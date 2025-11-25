# Trader-Behavior-Insights
“Exploring the relationship between market sentiment and trader PnL using historical Hyperliquid trades and sentiment indices.”

Trader Behavior Insights – Data Science Case Study

Objective:
Explore whether market sentiment (Fear vs. Greed) influences trader performance on Hyperliquid — uncover behavioral patterns, evaluate risk tendencies, and develop predictive modeling insights.

🔍 Project Overview

This project analyzes two datasets:

Dataset	Source	Key Columns
Hyperliquid Historical Trader Data	Web3 trading platform	account, symbol, side, size, execution price, PnL, leverage, timestamp
Bitcoin Fear & Greed Index	Alternative.me	date, sentiment value, classification

By merging market sentiment with trading outcomes, this project identifies how traders behave under different emotional market conditions.

🧹 Data Preprocessing & Feature Engineering

✔ Cleaned missing and inconsistent values
✔ Converted timestamps to proper datetime format
✔ Standardized trader identifiers and symbols
✔ Created daily profitability metrics
✔ Merged datasets using date
✔ Added engineered features:

Profit/Loss category (positive or negative)

Trade sizing

Leverage usage behavior

Final merged dataset shape: (X rows × Y features)

📈 Key Insights
Finding	Interpretation
More negative PnL trades occur during Greed conditions	Traders take riskier positions when market is overly positive
Small profits are most common in Fear conditions	Cautious trading reduces both large wins and large losses
Execution pricing volatility is higher during Greed	FOMO → aggressive entries

Bottom line:

Emotions move the market — and majority of traders underperform when they trade with greed instead of logic.

🤖 Machine Learning Component

Goal: Predict whether a trade will be profitable based on sentiment + trade features.

Model: Random Forest Classifier
Accuracy: ~60% (baseline outperform)

However:

High recall for profitable trades is challenging (class imbalance)

Suggest incorporating trade duration, order book signals, liquidation proximity

📊 Visualizations Included

PnL Distribution: Fear vs Greed

Sentiment vs. Leverage usage

Daily profitability heatmap

Correlation matrix of trading behavior features

(All visuals available in notebook)

🛠 Tech Stack
Category	Tools
Programming	Python (Pandas, NumPy, Scikit-learn)
Visualization	Matplotlib, Seaborn
Environment	Google Colab
Version Control	GitHub
🚀 Future Improvements

Time-series models for trade sequencing

Strategy recommendation engine

Crypto-pair-specific behavior segmentation

Sharpe-ratio style performance metrics
