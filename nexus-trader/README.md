# 💰 Nexus Auto Trader

A powerful cryptocurrency and stock trading bot with real-time market data, sentiment analysis, and automated trading strategies.

![Nexus Trader Screenshot](docs/screenshot.png)

## 🚀 Features

### Market Data
- **500+ Cryptocurrencies** - Real-time data from CoinGecko API
- **150+ Stocks** - Major stocks across all sectors
- **Live Price Updates** - Refreshes every 2 seconds

### Trading Intelligence
- **Fear & Greed Index** - Contrarian trading based on market sentiment
- **RSI Analysis** - Relative Strength Index for overbought/oversold signals
- **EMA Crossovers** - 9/21 period exponential moving averages
- **Momentum Detection** - Identifies trending assets
- **Volume Spike Detection** - Finds unusual activity

### Trading Strategies
| Strategy | Risk Level | Target |
|----------|------------|--------|
| 🛡️ Conservative | Low | 0.3-0.5%/day |
| ⚖️ Moderate | Medium | 0.5-1%/day |
| 🔥 Aggressive | High | 1-3%/day |
| 🚀 YOLO | Maximum | 3-10%/day |
| ⚡ Scalper | Variable | Many small trades |

### Filtering & Analysis
- Search by symbol
- Filter by price range
- Filter by % change
- Filter by sector (stocks)
- Sort by any column
- View: Gainers, Losers, Oversold, Overbought

### Manual Trading
- Quick buy buttons on every asset
- One-click sell all positions
- Detailed asset view with charts

## 📦 Installation

### Option 1: Direct Use
Simply open `index.html` in your browser. No server required!

### Option 2: Local Server
```bash
# Clone the repository
git clone https://github.com/yourusername/nexus-trader.git
cd nexus-trader

# Serve with Python
python -m http.server 8000

# Or with Node.js
npx serve
```

Then open http://localhost:8000

### Option 3: GitHub Pages
1. Fork this repository
2. Go to Settings > Pages
3. Select "main" branch
4. Your site will be live at `https://yourusername.github.io/nexus-trader`

## 🔧 Configuration

### API Keys (Optional)
For live trading, you'll need:

**Coinbase Advanced Trade API:**
1. Go to [Coinbase Advanced](https://www.coinbase.com/advanced)
2. Create API keys with trade permissions
3. Enter in Settings modal

**Alpaca (Stocks):**
1. Sign up at [Alpaca](https://alpaca.markets/)
2. Get API keys from dashboard
3. Enter in Settings modal

**Telegram Alerts:**
1. Create a bot via [@BotFather](https://t.me/botfather)
2. Get your chat ID from [@userinfobot](https://t.me/userinfobot)
3. Enter in Settings modal

## 📊 How It Works

### Sentiment-Based Trading
The bot uses a contrarian strategy based on the Fear & Greed Index:

- **Extreme Fear (0-25)**: BUY aggressively - others are panic selling
- **Fear (25-40)**: Increase buying
- **Neutral (40-60)**: Normal trading
- **Greed (60-75)**: Take profits earlier
- **Extreme Greed (75-100)**: SELL into strength - market is overheated

### Technical Analysis
Each asset is scored based on:
- RSI (Relative Strength Index)
- EMA crossovers
- Price momentum
- Volume activity
- Recent price action

### Position Management
- **Take Profit**: Dynamic based on market sentiment
- **Stop Loss**: Tighter in greed, looser in fear
- **Trailing Stop**: Locks in profits on winning trades
- **Timeout Rules**: Exits stale positions

## ⚠️ Disclaimer

**This is for educational purposes only.**

- Paper trading mode uses simulated money
- Past performance does not guarantee future results
- Cryptocurrency and stock trading involves substantial risk
- Never trade with money you cannot afford to lose
- The developers are not responsible for any financial losses

## 🛠️ Tech Stack

- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **APIs**: 
  - CoinGecko (crypto data)
  - Yahoo Finance (stock data)
  - Alternative.me (fear/greed index)
- **No Dependencies**: Runs entirely in the browser

## 📁 Project Structure

```
nexus-trader/
├── index.html          # Main application
├── README.md           # This file
├── LICENSE             # MIT License
├── css/
│   └── styles.css      # Extracted styles (optional)
├── js/
│   └── app.js          # Extracted JavaScript (optional)
├── assets/
│   └── logo.png        # Logo/icons
└── docs/
    ├── screenshot.png  # App screenshot
    └── TRADING.md      # Trading strategy docs
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing`)
5. Open a Pull Request

## 📄 License

MIT License - see [LICENSE](LICENSE) file

## 🙏 Acknowledgments

- [CoinGecko](https://www.coingecko.com/) for crypto market data
- [Alternative.me](https://alternative.me/) for Fear & Greed Index
- [Yahoo Finance](https://finance.yahoo.com/) for stock data

---

**Made with 💰 by Mike**
