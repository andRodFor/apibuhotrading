# 🦉 BuhoTrading API

AI-powered trading analytics and signal confirmation for crypto and forex markets.

BuhoTrading enhances classic technical indicators by adding an artificial intelligence layer trained by market, timeframe, and historical context.

---

## 🚀 What is BuhoTrading?

BuhoTrading does not replace traditional indicators.

It **enhances them**.

You keep using EMA, RSI, MACD, Pivots, and other familiar tools —  
BuhoTrading adds AI-based interpretation, direction filtering, and confidence scoring.

---

## 🧠 How it works

1. Classic indicator values are calculated
2. Indicator behavior is transformed into normalized sequences
3. AI models trained per timeframe and market analyze structure, direction, and pressure
4. The API returns:
   - BUY / SELL / NONE
   - Confidence score
   - Probability distribution

---

## 📊 Supported Indicators

- EMA (trend direction models)
- RSI (momentum slope interpretation)
- MACD (momentum and crossover behavior)
- HeatMap (price–volume pressure zones)
- Pivot (support / resistance & reversal detection)
- Score (price, volume and Gann-based pressure)
- Vector (sequence-based pattern recognition)

Each model is trained using a **fixed number of candles** aligned with its timeframe.

Available models, symbols & test > 👉 https://buhotrading.com

---

## 🔌 API Overview

**Endpoint**
```
POST https://buhotrading.com/api/v1/signal?key=YOUR_API_KEY
Content-Type: Application/JSON
```
**Example Request format**
```json
{
  "symbol": "XAUUSD",
  "model": "pivot01d180d",
   // [timestamp, open, high, low, close, volume]
  "candles": [
    [1763067600,4172.08,4211.38,4032.29,4085.1,268900],
     [1763326800,4085.42,4106.71,4006.96,4045.52,239375],
     [1763413200,4044.54,4082.31,3998.08,4067.3,241116],
     [1763499600,4067.22,4132.8,4055.67,4077.76,239567],
     [1763586000,4078.05,4110.27,4038.97,4077.2,259346],
    ...
  ]
}
```
📈 Example Response
```json
{
  "symbol": "XAUUSD",
  "model": "pivot01d180d",
  "signal": "BUY",
  "accuracy": 0.70,
  "ai": {
    "BUY": 0.70,
    "SELL": 0.10,
    "NONE": 0.20
  },
  "errorCode": 0,
  "errorDetail": ""
}
```

```
⚠️ Error Codes

Code	Description
0	No error
1	Missing or invalid API key
2	Missing or invalid symbol
3	Symbol not available
4	Missing or invalid model
5	Model not available
6	Missing or invalid candles data
7	Invalid candles size
8	Prediction error or no AI result
9	Rate limit exceeded
99	Internal server error
```
🔑 API Access

API keys can be requested at:

👉 https://buhotrading.com

⚠️ Disclaimer

BuhoTrading provides AI-based analytical information only.
It does not constitute financial or investment advice.

Use at your own risk.


📫 Contact

📧 apibuhotrading@gmail.com

