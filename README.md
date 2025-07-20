# 📈 Distributed AI Trading Agent System with Multi-LLM Orchestration using MCP

![MCP Trading System](https://github.com/user-attachments/assets/772abc08-0774-40af-a949-c4e35e99cd76)

## 🧠 MCP Trading System

The MCP Trading System is a real-time, multi-agent trading simulator where autonomous AI agents interact with a dynamic market environment. It provides a full-stack simulation pipeline including:

- Market movement  
- Portfolio tracking  
- AI-driven trading decisions  
- Live visual monitoring via an interactive Gradio dashboard

---

## ✨ Features

- 🤖 Multiple AI trading agents with independent strategies  
- 📉 Real-time market simulation and asset price updates  
- 💼 Live portfolio tracking per agent (cash, holdings, P&L)  
- 🧾 Transaction history with color-coded logs  
- 📊 Interactive web UI built with Gradio + Plotly  
- 🧠 Modular agent strategies (LLM, momentum, random, etc.)  
- 🔍 Decision trace logging for explainability  
- 🔐 Environment-configurable API access (e.g., Polygon, OpenAI)  

---

## 🧠 Agent Overview

| Agent Name           | Role                                                                 |
|----------------------|----------------------------------------------------------------------|
| `LLMTrader`          | Uses GPT-based reasoning to decide trades based on market context     |
| `MomentumTrader`     | Buys rising assets, sells declining ones (trend-following strategy)   |
| `MeanReversionTrader`| Trades based on statistical reversion to the mean                    |
| `RandomTrader`       | Executes random trades — useful for benchmarking                     |
| `RuleBasedTrader`    | Makes decisions using technical thresholds or predefined logic       |

> Each agent implements a `decide_action()` method that is called every simulation tick. Agents operate independently and submit orders that are validated and executed.

---

## 🧩 System Architecture

| Component           | Description                                                          |
|---------------------|----------------------------------------------------------------------|
| `app.py`            | Entry point; initializes Gradio UI and connects components           |
| `market.py`         | Simulates market prices using custom or API-based logic              |
| `trading_floor.py`  | Manages agents, state updates, and simulation timing                 |
| `accounts.py`       | Tracks agent portfolios, cash balances, and executed orders          |
| `traders.py`        | Contains implementations of various trading agent strategies         |
| `database.py`       | Records transaction history and logs                                 |
| `util.py`           | Utility functions for formatting, logging, and conversions           |

---

## 📦 Requirements

Install required dependencies:

```bash
pip install -r requirements.txt
```

### Key Dependencies

- `gradio`  
- `pandas`  
- `plotly`  
- `python-dotenv`  
- `openai`  
- `requests`  
- `polygon-api-client`  
- `openai-agents`  
- `asyncio`  

---

## ⚙️ Environment Setup

Create a `.env` file in the root directory:

```ini
OPENAI_API_KEY=your_openai_key  
POLYGON_API_KEY=your_polygon_key
```

---

## 🚀 Getting Started

Clone the repository:

```bash
git clone https://github.com/your-username/mcp-trading-system.git
cd mcp-trading-system
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the simulator:

```bash
python app.py
```

> The dashboard will open in your browser with live updates of agents and trades.

---

## 📊 Monitoring Dashboard

The web UI provides:

- Agent-wise P&L and portfolio breakdown  
- Price charts with overlays of trade markers  
- Color-coded transaction logs  
- Live market price movement  
- Order execution history  

> All activity is updated in real-time and logged to persistent storage for future review.

---

## 🔧 Customization

You can:

- Add new trading agents by extending the `Trader` base class  
- Integrate real market data using Polygon or other APIs  
- Tune market parameters: volatility, tick speed, asset pool  
- Swap Gradio for a different frontend (e.g., React, Dash)  

---

## 🤝 Contributing

Contributions are welcome!  
Fork the repository and submit a pull request to:

- Add new strategies  
- Improve visualization  
- Optimize simulation engine  
- Fix bugs or enhance documentation  

---

## 🪪 License

MIT License *(or specify your own here)*

---

## 📬 Contact

For questions or collaboration opportunities, please reach out via [GitHub Issues](https://github.com/your-username/mcp-trading-system/issues) or open a discussion thread.
