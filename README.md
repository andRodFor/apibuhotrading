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

POST https://buhotrading.com/api/v1/signal?key=YOUR_API_KEY
Content-Type: Application/JSON

**Request format**
```json
{
  "symbol": "XAUUSD",
  "model": "pivot01d180d",
  "candles": [
    [timestamp, open, high, low, close, volume],
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

