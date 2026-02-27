# 📈 MSFT Trader Behavior & Sentiment Analysis

A data science project analyzing Microsoft (MSFT) stock trader behavior 
and market performance using historical price data and Twitter sentiment data.

## 🎯 Objective
Discover patterns in trader behavior and market movements that could inform 
better trading strategies on platforms like HyperQuant.

## 📂 Datasets
| Dataset | Source | Description |
|---------|--------|-------------|
| Microsoft Dataset.csv | Kaggle | MSFT historical OHLCV price data |
| stock_tweets.csv | Kaggle | Stock-related tweets with sentiment |

## 🔧 Features Engineered
- Moving Averages (MA-7, MA-20, MA-50)
- RSI (14-day Relative Strength Index)
- MACD + Signal Line + Histogram
- Bollinger Bands (Upper, Lower, Width)
- Daily PnL, Return %, Day Direction
- Volume Ratio (vs 10-day MA)
- Tweet Sentiment Score (Positive/Negative/Neutral)
- Daily Mention Count per Ticker

## 📊 Analysis Performed

### Part A — Data Preparation
- Null handling, duplicate removal, date standardisation
- Feature engineering on both stock and tweet datasets
- Dataset merging by date

### Part B — Analysis
- Positive vs Negative day performance comparison
- Return distribution (histogram, Q-Q plot, CDF)
- High-leverage trading day identification
- Sentiment–price correlation matrix
- Ticker mention frequency analysis

### Part C — What-If Strategy Backtesting
| Strategy | Description |
|----------|-------------|
| Buy & Hold | Baseline — always invested |
| RSI Mean-Reversion | Buy RSI < 35, Sell RSI > 65 |
| MA Crossover | Buy when MA-7 > MA-20 |
| Sentiment-Driven | Trade based on daily tweet sentiment |

## 📉 Key Findings
- MSFT shows slight positive skew in daily returns
- High-leverage days (top 20% volume + move) show 2x average price swings
- RSI mean-reversion outperforms buy-and-hold in range-bound periods
- Positive Twitter sentiment shows weak but measurable next-day return correlation

## 🛠️ Tech Stack
```
Python 3.10
pandas | numpy | matplotlib | seaborn | scipy | jupyter
```

## 🚀 How to Run
```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn scipy jupyter

# Launch notebook
jupyter notebook MSFT_Trader_Behavior_Analysis.ipynb
```
Then: **Kernel → Restart & Run All**

## 📁 Output Files
| File | Description |
|------|-------------|
| `pos_vs_neg_analysis.png` | Positive vs negative day charts |
| `return_distribution.png` | Distribution analysis |
| `high_leverage_analysis.png` | High-leverage day analysis |
| `correlation_matrix.png` | Correlation heatmap |
| `tweet_frequency.png` | Ticker mentions & sentiment |
| `technical_dashboard.png` | Full OHLCV + indicators chart |
| `strategy_comparison.png` | Backtesting equity curves |
| `MSFT_Final_Analysis_Dataset.csv` | Clean engineered dataset |

## 📌 Project Structure
```
📦 MSFT-Trader-Behavior-Analysis
 ┣ 📓 MSFT_Trader_Behavior_Analysis.ipynb
 ┣ 📊 MSFT_Final_Analysis_Dataset.csv
 ┣ 🖼️ pos_vs_neg_analysis.png
 ┣ 🖼️ return_distribution.png
 ┣ 🖼️ high_leverage_analysis.png
 ┣ 🖼️ correlation_matrix.png
 ┣ 🖼️ tweet_frequency.png
 ┣ 🖼️ technical_dashboard.png
 ┣ 🖼️ strategy_comparison.png
 ┗ 📄 README.md
```

## ⚠️ Note
Raw dataset files (CSV) are not included in this repo as they are sourced 
from Kaggle. Download them from the links below and place in the project folder:
- [Microsoft Stock Dataset — Kaggle](https://www.kaggle.com)
- [Stock Tweets Dataset — Kaggle](https://www.kaggle.com)

## 👤 Author
**[Your Name]**  
Data Science Analytics Intern Assignment — Round 2
