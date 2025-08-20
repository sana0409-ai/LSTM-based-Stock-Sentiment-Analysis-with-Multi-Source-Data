# LSTM-based-Stock-Sentiment-Analysis-with-Multi-Source-Data
LSTM-based stock sentiment analysis model that combines Unusual Whales sweeps with multi-source sentiment data (Alpha Vantage, Polygon IO, TWS News + FinBERT), aligned with OHLCV features, to predict 4-hour future returns and classify bullish vs bearish signals.
This project explores how financial sentiment and price action can be combined to predict short-term stock movements. Using an LSTM neural network, the model processes time-series data that fuses options flow, sentiment scores, and OHLCV market data to classify whether a stock is likely to move bullish or bearish in the next 4 hours.
Natural Language Processing (NLP) & Sentiment Analysis

Sentiment influences stock prices, especially when aggregated from news, headlines, and trading signals.

Sentiment scores are standardized to numerical features usable in machine learning.

Options Flow & Market Signals

Unusual Whales sweeps data provides context on market activity and trader behavior.

Integrating options flow with sentiment enriches predictive power.

Time-Series Prediction with LSTM

LSTMs are designed to model sequential dependencies.

By looking back at sequences of OHLCV + sentiment, the model predicts future returns.
Data Sources

Unusual Whales → Options sweeps (ticker, timestamp).

Alpha Vantage → Sentiment scores + labels (pre-labeled).

Polygon IO & TWS News → Raw headlines processed with FinBERT to generate sentiment labels & scores.

Market Data (OHLCV) → Price, volume, open, high, low, close.
Model

Architecture: LSTM sequence-to-label classifier.

Inputs: OHLCV features + aggregated sentiment features.

Output: Probability of bullish movement in next 4h.

Thresholds:

Label threshold = 0% return.

Decision threshold (best by F1 = 0.55, chosen for TNR = 0.66).
Model

Architecture: LSTM sequence-to-label classifier.

Inputs: OHLCV features + aggregated sentiment features.

Output: Probability of bullish movement in next 4h.

Thresholds:

Label threshold = 0% return.

Decision threshold (best by F1 = 0.55, chosen for TNR = 0.66).
