# Attention-Induced Volatility:
### Modeling How Reddit Coordination Predicts Short-Term Crypto Price Jumps

## 🎯 Project Summary

This project investigates whether decentralized coordination dynamics on Reddit can forecast short-term volatility in retail-driven crypto tokens like DOGE, SHIBA, and XRP.

While past studies have analyzed Reddit sentiment or post volume during the meme-stock era, this project goes further:  
- We construct **novel behavioral coordination signals** from Reddit discussions,  
- Model their **causal impact on volatility** using high-frequency crypto data, and  
- Build a pipeline to test these relationships at scale using Google BigQuery.

---

## 💡 Research Question

> **Can coordination metrics extracted from Reddit financial subreddits predict short-term volatility in low-cap, high-retail crypto assets?**

We focus not on sentiment, but on **measurable coordination dynamics** — such as sudden bursts in engagement, topic convergence, and subreddit echo patterns — and test whether these dynamics Granger-cause volatility shocks.

---

## 📊 Economic Framing

Grounded in behavioral finance and coordination theory, this project treats Reddit as a public signal channel where user attention can converge into coordinated trading behavior — pushing asset prices and volatility beyond fundamentals.

Inspired by:
- Morris & Shin (2002) — Coordination Games
- DeMarzo et al. (2003) — Cascades and Information Overload
- Barberis & Shleifer — Behavioral Bias in Financial Markets

---

## 🔍 Methodology Overview

| Step | Description |
|------|-------------|
| 1️⃣ Data Extraction | Reddit comment data via BigQuery (`reddit_comments.comments_2023`–`2025`) |
| 2️⃣ Signal Engineering | Burstiness, entropy of topics, upvote skew, subreddit echo overlap |
| 3️⃣ Crypto Data | Minute/hour-level OHLCV data from CoinGecko or CryptoCompare |
| 4️⃣ Volatility Modeling | Realized hourly volatility + GARCH-X and VAR models |
| 5️⃣ Causal Testing | Granger causality, difference-in-differences, forecast evaluation |

---

## 📦 Data Sources

- **Reddit**: BigQuery public dataset (`reddit_comments`)
- **Crypto Markets**: CoinGecko or CryptoCompare API (OHLCV)
- **Assets Focused**: DOGE, SHIBA, XRP (more to follow)

---

## 📈 Deliverables

- Clean Reddit-to-crypto time-aligned dataset
- Forecasting models + diagnostic evaluation
- Visualizations of attention bursts vs volatility
- Final report / blog post
- GitHub repo with reproducible code + BigQuery SQL

---

## ⚙️ Stack

| Component | Tools |
|----------|--------|
| Query Engine | Google BigQuery |
| Processing | Python (pandas, statsmodels), or R (data.table, vars, rugarch) |
| Modeling | GARCH-X, VAR, Granger causality |
| NLP | BERTopic or LDA |
| Deployment | Google Colab or local Docker (optional) |

---

## 📌 Status

- ✅ Phase 1: Research design + project framing (in progress)
- ⬜ Phase 2: Reddit signal engineering
- ⬜ Phase 3: Crypto volatility pipeline
- ⬜ Phase 4: Modeling + inference
- ⬜ Phase 5: Write-up + portfolio packaging

---

## 🧠 Author

**[Your Name]**  
MSc Economics · Data Analyst  
[LinkedIn/GitHub URL]  

> “Attention is the new liquidity.”
