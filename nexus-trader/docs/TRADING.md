# 📈 Trading Strategies Guide

## Overview

Nexus Auto Trader uses a combination of technical analysis and sentiment analysis to make trading decisions. This document explains the strategies in detail.

## Sentiment-Based Trading (Contrarian)

> "Be fearful when others are greedy, and greedy when others are fearful." - Warren Buffett

### Fear & Greed Index

The bot calculates market sentiment from:
- % of coins going up vs down
- Average price change
- Volume activity
- Number of extreme movers

| Score | Classification | Bot Action |
|-------|---------------|------------|
| 0-25 | Extreme Fear | BUY aggressively (1.5x normal) |
| 25-40 | Fear | BUY more (1.2x normal) |
| 40-60 | Neutral | Normal trading |
| 60-75 | Greed | Take profits earlier (0.8x) |
| 75-100 | Extreme Greed | SELL into strength (0.5x) |

## Technical Indicators

### RSI (Relative Strength Index)

Measures momentum on a 0-100 scale:
- **Below 30**: Oversold → Buy signal
- **30-70**: Neutral
- **Above 70**: Overbought → Sell signal

### EMA (Exponential Moving Average)

Uses 9-period and 21-period EMAs:
- **Price above both**: Bullish
- **Price below both**: Bearish
- **EMA9 crosses above EMA21**: Buy signal
- **EMA9 crosses below EMA21**: Sell signal

### Momentum Score

Each asset receives a score (0-100) based on:
- RSI position (+25 if oversold)
- Fear/Greed bonus (+20 in extreme fear)
- Top gainers list (+20)
- Volume spikes (+15)
- Momentum leaders (+30)

## Position Management

### Entry Rules
1. RSI must be below strategy threshold
2. Score must meet minimum requirement
3. Must have available cash
4. Not already holding the asset
5. Within max position limit

### Exit Rules

**Take Profit:**
- Dynamic based on market sentiment
- Tighter in greed (take profits earlier)
- Looser in fear (let winners run)

**Stop Loss:**
- Also dynamic based on sentiment
- Tighter in greed (protect gains)
- Looser in fear (avoid shakeouts)

**Trailing Stop:**
- Activates when position was up 2%+
- Exits if price drops significantly

**Timeout:**
- Exits flat positions after extended hold
- Takes small profits after timeout period

## Strategy Profiles

### 🛡️ Conservative
- Take Profit: 1.5%
- Stop Loss: -0.8%
- RSI Buy: < 25
- Max Positions: 3
- Position Size: 15%

### ⚖️ Moderate (Default)
- Take Profit: 2.0%
- Stop Loss: -1.2%
- RSI Buy: < 30
- Max Positions: 5
- Position Size: 12%

### 🔥 Aggressive
- Take Profit: 2.5%
- Stop Loss: -1.5%
- RSI Buy: < 35
- Max Positions: 8
- Position Size: 10%

### 🚀 YOLO
- Take Profit: 4.0%
- Stop Loss: -3.0%
- RSI Buy: < 40
- Max Positions: 12
- Position Size: 20%

### ⚡ Scalper
- Take Profit: 0.8%
- Stop Loss: -0.5%
- RSI Buy: < 40
- Max Positions: 15
- Position Size: 5%
- Trade Frequency: 10x

## Risk Management

### Position Sizing
- Never risk more than strategy % per trade
- Maximum $25-50 per position
- Scales with available capital

### Diversification
- Multiple positions across different assets
- Max positions limit prevents over-concentration

### Fee Awareness
- Coinbase: ~0.7% per trade
- Need 1.4%+ gain to profit after round-trip
- Alpaca stocks: ~0.003% (nearly free)

## Realistic Expectations

| Timeframe | Realistic Target | Exceptional |
|-----------|-----------------|-------------|
| Daily | 0.5-1% | 2-3% |
| Weekly | 2-5% | 5-10% |
| Monthly | 5-15% | 20-30% |
| Yearly | 30-100% | 200%+ |

**Important:** These are targets, not guarantees. Most days will be flat or negative. Consistency over time is the goal.

## Paper vs Live Trading

### Paper Mode
- Uses simulated $100 starting balance
- No real money at risk
- Great for testing strategies
- May not reflect real execution

### Live Mode
- Requires API keys
- Real money at risk
- Subject to slippage and spreads
- Start with small amounts

## Tips for Success

1. **Start in paper mode** - Test for at least 1-2 weeks
2. **Don't over-trade** - Fees eat profits
3. **Be patient** - Good setups take time
4. **Manage risk** - Never risk more than you can lose
5. **Stay informed** - Watch for major news events
6. **Review trades** - Learn from wins and losses
