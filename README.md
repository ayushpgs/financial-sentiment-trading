# Financial Sentiment Trading Strategy using FinBERT

## Overview
This project implements a sentiment-driven trading strategy using financial news data and Natural Language Processing (NLP). It leverages the FinBERT model to extract sentiment from news headlines and evaluates its impact on stock price movements.

---

## Key Features
- Multi-stock data collection using Yahoo Finance  
- Financial news extraction and preprocessing  
- Sentiment analysis using FinBERT (transformer-based model)  
- Time-series alignment of news and stock data using merge_asof  
- Trading signal generation (Buy/Sell/Hold)  
- Backtesting of trading strategy  
- Evaluation using financial metrics  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- yfinance  
- HuggingFace Transformers (FinBERT)  
- Matplotlib  

---

## Methodology

### Data Collection
- Stock data retrieved using yfinance  
- Financial news collected for multiple stocks using Yahoo Finance  

### Sentiment Analysis
- Applied FinBERT to classify sentiment of news headlines  
- Generated sentiment score:
   sentiment = positive - negative
  
### Data Alignment
- Used merge_asof to align news timestamps with stock prices  
- Ensured mapping to the next available trading day  

### Feature Engineering
- Calculated next-day returns:
return = (next_close - close) / close
### Trading Strategy
- Positive sentiment → Buy  
- Negative sentiment → Sell  
- Neutral sentiment → Hold  

### Backtesting
- Strategy returns:
strategy_return = signal * return

---

## Results
- Sharpe Ratio: ~-0. 17
- Max Drawdown: ~-0.065 

The results indicate that sentiment signals have predictive potential, though performance is limited due to dataset size and a simple strategy.

---

## Limitations
- Limited dataset (recent news only)  
- Basic trading logic (no advanced filtering)  
- No transaction costs included  
- Small sample size after alignment  

---

## Future Improvements
- Use larger and more diverse datasets  
- Integrate technical indicators  
- Improve signal thresholds and filtering  
- Portfolio-level optimization  
- Real-time trading simulation  

---

## Key Takeaway
This project demonstrates how NLP techniques can be integrated with financial data to build a quantitative trading strategy.

---

## Author
Ayush Pandey

