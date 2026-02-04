## Trader-Behavioral-Analysis-Sentiment-vs.-Performance
This project explores the "Sentiment Gap" in financial markets—analyzing how market emotions (Fear &amp; Greed) influence trader behavior, risk appetite, and profitability. Using a dataset of 211,224 trades and historical Fear &amp; Greed Index data, we identify distinct trader archetypes and their performance under emotional market stress.

# 🔍 Methodology
1.Data Preparation
o Temporal Alignment: Trade timestamps (IST) were normalized to daily grains to join with the Crypto Fear & Greed Index.

o Metric Engineering:
  Daily PnL: Aggregated realized profit/loss per account.
  Win Rate: Binary classification of trades (PnL > 0).
  L/S Ratio: Directional bias (Longs vs. Shorts).
  Sentiment Bucketing: Classified index values into Fear (0-40), Neutral (41-60), and Greed (61-100).

2.Trader Segmentation
 We classified the user base into three behavioral archetypes:
 o Whales: Top 25th percentile by average position size.
 o Frequent Retail: High trade frequency (>10 trades/day) but smaller sizes.
 o Occasional Retail: Low frequency, small size participants.

# 📈 Key Insights
1. The Panic-Trading Paradox
Trading frequency and average position sizes spike by ~37% during Fear days compared to Greed. While sentiment drops, activity increases, suggesting high-stress "dip-buying" or "revenge trading" behaviors.

2. Profitability vs. Sentiment
Contrary to popular belief, the average daily PnL in this dataset was 25% higher during Fear ($5,185) than during Greed ($4,144). This is largely driven by "Whales" who successfully capitalize on extreme fear conditions.

3. Persistent Bullish Bias
The Long/Short ratio remains consistently high (>3.0) regardless of market sentiment, indicating a structural bullish bias among retail participants even when the market is in "Extreme Fear."

# 🛠 Actionable Strategies (Rules of Thumb)
The "Extreme Fear" Liquidity Strategy: During Index values < 25, Whales are most profitable. Offer fee rebates to Whale segments to encourage market-making when liquidity is most needed.

The "Greed" Leverage Cap: Retail win rates do not improve during Greed, but frequency increases. Implement dynamic leverage caps when F&G > 75 to prevent over-exposure at market tops.
