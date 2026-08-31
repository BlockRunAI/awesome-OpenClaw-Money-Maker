# Awesome OpenClaw Money Maker 🦞💰

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/BlockRunAI/awesome-OpenClaw-Money-Maker?style=social)](https://github.com/BlockRunAI/awesome-OpenClaw-Money-Maker)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

> A curated list of open-source tools and repos for making money with AI agents like [OpenClaw](https://github.com/openclaw/openclaw).

**Reality check:** These are potential earnings, not guarantees. Factor in API/token costs, time investment, and market competition.

---

## Web4 The Money Loop 🔄

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│   💵 USDC ──► Franklin ──► ClawRouter ──► LLM ──► 💰 Profit     │
│       ▲          │                              │                │
│       │     marketing,                    OpenClaw │               │
│       │     trading, content                 │   │                │
│       └──────────────── reinvest ◄───────────┘                    │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

1. **Fund your wallet** with USDC (on Base)
2. **OpenClaw uses [ClawRouter](https://github.com/BlockRunAI/ClawRouter)** to access <!-- br:models.chatVisible -->76<!-- /br:models.chatVisible --> LLMs
3. **Pay-per-request** via x402 micropayments - no API keys, no subscriptions
4. **Save <!-- br:savings.autoVsBaselinePct -->84<!-- /br:savings.autoVsBaselinePct -->%** on inference costs with smart model routing
5. **[Franklin](https://github.com/BlockRunAI/franklin) — the AI agent with a wallet** — runs marketing campaigns, trading signals, and content generation autonomously
6. **LLM executes tasks** that generate income
7. **Profit funds more usage** - creating a self-sustaining money loop

**Get started:** [Franklin](https://github.com/BlockRunAI/franklin) ⭐ | [ClawRouter v0.12.256](https://github.com/BlockRunAI/ClawRouter) ⭐ 6.6k | [BlockRun.ai](https://blockrun.ai)

### 🆕 ClawRouter v0.12.256 - Aug 2026

Latest version with deterministic portfolio routing on by default, image + image-to-image generation, usage reports, and three-strike escalation:

| Feature | Description |
|---------|-------------|
| **Response Caching** | LLM response caching with SHA-256 hashing, 10min TTL, 200-entry LRU cache |
| **Routing Profiles** | 4 modes: `auto` (balanced), `eco` (max savings), `premium` (best quality), `free` (zero cost) |
| **Context-Length Routing** | Auto-filters models that can't handle request context size |
| **Agentic Auto-Detect** | Intelligent routing for multi-step autonomous workflows |
| **Tool Detection** | Auto-switches modes when `tools` array is detected |
| **15-Dimension Routing** | Local scoring (<1ms) classifies prompts into SIMPLE/MEDIUM/COMPLEX/REASONING |
| **Session Persistence** | 1-hour model pinning for multi-turn conversations |
| **Smart Fallback Chains** | Auto-retry with next-best model on provider errors |
| **Model Aliases** | `/model codex`, `/model opus`, `/model sonnet`, `/model kimi`, `/model free` |
| **Reasoning Model Support** | Handles `reasoning_content` for O3/O4/DeepSeek-R1/Grok-reasoning |
| **Free Tier Fallback** | Falls back to a free NVIDIA-hosted model (Nemotron family) when the wallet is empty |
| **`clawrouter doctor`** | AI-powered diagnostics when things go wrong (Sonnet default, Opus for deep analysis) |
| **`clawrouter report`** | Daily/weekly/monthly usage reports via `npx @blockrun/clawrouter report` |
| **`/imagegen` command** | Generate images from chat (GPT Image 2, Flux, Nano Banana 2, Seedream 5 Pro) with x402 micropayments |
| **`/debug` command** | Routing diagnostics (tier, model, scores, session state) with zero API cost |
| **Three-Strike Escalation** | Auto-escalates SIMPLE→MEDIUM→COMPLEX→REASONING on 3 identical hashes — fixes agentic loops |
| **Multilingual Keywords** | ES/PT/KO/AR language support for global users |
| **16-Model Curated Allowlist** | Trimmed to top 16 models across 4 routing profiles + popular picks |
| **Portfolio Routing (v3.4)** | Deterministic portfolio strategy is now the `auto` default, shared via [router-core](https://github.com/BlockRunAI/router-core) |
| **Solana by Default** | New wallets start on the Solana gateway (`sol.blockrun.ai`); existing Base wallets are untouched |
| **`/img2img` command** | Image-to-image editing from chat, same x402 pay-per-call flow |
| **Disconnect Aborts** | Hanging up cancels the paid upstream — no charge for a response nobody receives |

```bash
# Install via OpenClaw
openclaw plugins install @blockrun/clawrouter

# Or via npm
npm install @blockrun/clawrouter@0.12.256

# Or standalone
curl -fsSL https://blockrun.ai/ClawRouter-update | bash
```

---

## Contents

- [Franklin — AI Agent with a Wallet](#franklin--ai-agent-with-a-wallet) ⭐ FEATURED
- [Trading Bots](#trading-bots)
- [MEV & Arbitrage](#mev--arbitrage)
- [Prediction Markets](#prediction-markets)
- [DeFi & Yield Farming](#defi--yield-farming)
- [Airdrop Farming](#airdrop-farming)
- [Lead Generation & Sales](#lead-generation--sales)
- [Content Creation](#content-creation)
- [AI Agent Frameworks](#ai-agent-frameworks)
- [OpenClaw Skills](#openclaw-skills)
- [Workflow Automation](#workflow-automation)
- [MCP Servers & Tools](#mcp-servers--tools)
- [Research & Analysis](#research--analysis)
- [Resources & Directories](#resources--directories)
- [Cost Considerations](#cost-considerations)
- [Security Warnings](#security-warnings)

---

## Franklin — AI Agent with a Wallet

> **The first Autonomous Economic Agent.** Franklin doesn't just write text — it autonomously spends USDC from a user-funded wallet to execute real work: marketing campaigns, trading signals, content generation.

**Built on three layers:**

1. **x402 micropayment protocol** — HTTP 402 native payments. Every API call is a payment. No billing dashboards, no API keys — just pay-per-request over HTTP.
2. **BlockRun Gateway** — aggregates <!-- br:models.chatVisible -->76<!-- /br:models.chatVisible --> LLMs + paid APIs (Exa, DALL-E, future Runway/Suno/CoinGecko) behind a single x402 endpoint.
3. **Franklin Agent** — the reference client. An AI agent that actually spends money to get things done.

**Three verticals, one wallet:**

| Vertical | What it does |
|---|---|
| **Marketing Agent** | Campaigns, social outreach, lead gen — autonomously pays for web search, research APIs, copywriting models |
| **Trading Agent** | Signals, research, risk analysis — autonomously pays for market data, LLM reasoning, on-chain queries |
| **Content Agent** | ImageGen, VideoGen, budget-tracked media production — autonomously pays per asset (DALL-E, Flux, future Runway/Suno) |

**Why Franklin belongs in this list:**

- It's the **only agent that natively spends crypto** to complete tasks — not a simulation, not a demo, real USDC on Base
- **x402 protocol** makes every API call a micropayment — no subscriptions, no API keys, just pay-per-request
- **Smart model routing** — plans with premium models, executes with cheap ones, saving 5-10x on LLM costs
- **Self-learning** — tracks which models/tools deliver the best results per task type and optimizes automatically
- **Plugin system** — extensible with social, marketing, and custom plugins
- **MCP integration** — auto-discovers and uses Model Context Protocol servers for additional tools

**Quick start:**

```bash
npm install -g @blockrun/franklin
franklin  # launch the agent
```

**Links:**

- 🏠 [GitHub](https://github.com/BlockRunAI/franklin) — Source code
- 📦 [npm](https://www.npmjs.com/package/@blockrun/franklin) — Install package
- 🌐 [BlockRun.ai](https://blockrun.ai) — Platform & wallet setup

---

## Trading Bots

### Crypto Trading

- [**Freqtrade**](https://github.com/freqtrade/freqtrade) ⭐ 53.8k - Free, open-source crypto trading bot. Supports all major exchanges (Binance, Hyperliquid, etc.). ML strategy optimization via FreqAI. Telegram control + WebUI.
  - 💰 **Monetize:** Sell custom strategies, run managed bot services, offer backtesting consulting

- [**Hummingbot**](https://github.com/hummingbot/hummingbot) ⭐ 19.7k - Open source market making and liquidity mining bot. Supports 40+ CEXs/DEXs. Customizable strategies in Python.
  - 💰 **Monetize:** Market making profits, liquidity mining rewards, strategy consulting

- [**FinRL**](https://github.com/AI4Finance-Foundation/FinRL) ⭐ 16.2k - Deep reinforcement learning for trading. Supports DQN, DDPG, A2C, SAC, PPO, TD3. Crypto environments with Binance API.
  - 💰 **Monetize:** Sell trained models, quant consulting, proprietary strategy development

- [**Jesse**](https://github.com/jesse-ai/jesse) ⭐ 8.4k - Advanced crypto trading bot in Python. Backtesting, paper trading, live trading. Built for algo traders.
  - 💰 **Monetize:** Sell strategies, subscription bot service, algo trading education

- [**Superalgos**](https://github.com/Superalgos/Superalgos) ⭐ 5.6k - Visual crypto trading bot builder. Drag-and-drop strategy design, backtesting, paper trading, multi-server deployments.
  - 💰 **Monetize:** Sell strategy templates, managed bot services, white-label platform

- [**OctoBot**](https://github.com/Drakkar-Software/OctoBot) ⭐ 6.5k - Open-source bot with AI, Grid, DCA, TradingView strategies. Simple interface, 15+ exchanges.
  - 💰 **Monetize:** Premium strategies, hosting service, configuration consulting

- [**OpenTrader**](https://github.com/Open-Trader/opentrader) ⭐ 2.8k - Open-source DCA & Grid trading bot with UI. Self-hosted, pro features unlocked.
  - 💰 **Monetize:** Managed service, custom strategy development, enterprise deployments

- [**Krypto-trading-bot**](https://github.com/ctubio/Krypto-trading-bot) ⭐ 3.7k - Self-hosted high-frequency market making bot in C++. Low-latency automated trading.
  - 💰 **Monetize:** HFT market making profits, strategy licensing, managed bot hosting

- [**crypto-trading-bot**](https://github.com/Haehnchen/crypto-trading-bot) ⭐ 3.5k - Multi-exchange crypto trading bot in JavaScript. Supports Bitfinex, Bitmex, Binance, Bybit.
  - 💰 **Monetize:** Multi-exchange arbitrage, strategy development, managed bot service

- [**Sibyl**](https://github.com/nMaroulis/sibyl) - AI-powered crypto trading dashboard. Oracle (LLM agent layer) + Chronos (LSTM/GTU price forecasting).
  - 💰 **Monetize:** Premium analysis tool, API access to signals, white-label for exchanges

### AI Trading Agents

- [**OpenBB**](https://github.com/OpenBB-finance/OpenBB) ⭐ 72.5k - Financial data platform for analysts, quants and AI agents. Open-source investment research terminal with AI copilot.
  - 💰 **Monetize:** Custom research tools, financial data SaaS, enterprise integrations, quant consulting

- [**GOAT SDK**](https://github.com/goat-sdk/goat) ⭐ 1k - The leading agentic finance toolkit for AI agents. Connect agents to DeFi protocols, wallets, and on-chain actions.
  - 💰 **Monetize:** Agent-powered trading bots, DeFi automation, on-chain agent services

- [**OpenNof1**](https://github.com/wfnuser/OpenNof1) ⭐ 208 - Your custom 24/7 AI trading agent. Inspired by nof1.ai. Open source and self-hostable.
  - 💰 **Monetize:** Managed trading service, strategy licensing, white-label solutions

- [**EVClaw**](https://github.com/Degenapetrader/EVClaw) ⭐ 40 - OpenClaw AI Trading Agent based on EVPlus.AI market data.
  - 💰 **Monetize:** EV-driven trading signals, managed accounts, strategy licensing

- [**nof1.ai**](https://github.com/195440/nof1.ai) ⭐ 686 - Autonomous AI trading agent. Web-based interface with real-time market monitoring and AI-powered decision making.
  - 💰 **Monetize:** Managed trading service, strategy licensing, white-label solutions

- [**AI Trading Agent (Hyperliquid)**](https://github.com/Gajesh2007/ai-trading-agent) ⭐ 539 - AI trading agent built specifically for Hyperliquid perpetual DEX.
  - 💰 **Monetize:** Perp trading profits, signal service, managed accounts

- [**OpenAlice**](https://github.com/TraderAlice/OpenAlice) ⭐ 6.9k - File-driven AI trading agent engine for crypto and securities markets. Autonomous 24/7 operation.
  - 💰 **Monetize:** Managed trading service, agent customization, strategy licensing

- [**Dexter**](https://github.com/virattt/dexter) ⭐ 27.6k - Autonomous agent for deep financial research. AI-powered analysis and investment insights.
  - 💰 **Monetize:** Research-as-a-service, premium analysis reports, enterprise financial intelligence

- [**TradingAgents**](https://github.com/TauricResearch/TradingAgents) - Multi-agent trading framework with specialized analyst, researcher, and trader agents.
  - 💰 **Monetize:** Enterprise trading solutions, custom agent development

- [**VARRD**](https://github.com/augiemazza/varrd) ⭐ 24 - Statistical edge discovery engine. Test a trading idea in plain English — event studies, backtests, and out-of-sample validation with guardrails against overfitting. Exports strategies for Freqtrade and Jesse. CLI, Python SDK, or MCP server.
  - 💰 **Monetize:** Validated strategy licensing, edge-as-a-service, signal subscriptions, quant consulting

### Solana Trading

- [**Solana Trading Bot**](https://github.com/warp-id/solana-trading-bot) ⭐ 2.3k - Beta Solana trading bot. Sniper, swap, and automated trading.
  - 💰 **Monetize:** Token sniping profits, managed bot service, strategy development

- [**open-sol-bot**](https://github.com/ChainBuff/open-sol-bot) ⭐ 403 - Fully open-source Solana copy trading and auto-trading bot.
  - 💰 **Monetize:** Copy trading fees, managed accounts, bot licensing

- [**Solana Trading Bot (Raydium/Pump.fun)**](https://github.com/henrytirla/Solana-Trading-Bot) ⭐ 287 - Buy/sell SPL tokens on Raydium DEX and Pump.fun using Jito SDK.
  - 💰 **Monetize:** Token trading profits, sniping service, strategy consulting

- [**solana-trading-bot**](https://github.com/radioman/solana-trading-bot) ⭐ 990 - Auto Solana trading bot on Pumpfun, Pumpswap, Raydium Launchpad using gRPC or Shredstream.
  - 💰 **Monetize:** Automated launch trading, managed bot service, early-access sniping

- [**solana-grpc-sniper-bot**](https://github.com/0xRustPro/solana-grpc-sniper-bundler-bot) ⭐ 11 - High-speed Solana sniper using gRPC for real-time transaction streaming.
  - 💰 **Monetize:** New token sniping, managed sniper service, speed advantage

- [**pumpclaw**](https://github.com/chainstacklabs/pumpclaw) ⭐ 7 - Chainstack's agent skill for pump.fun trading via [pumpfun-cli](https://github.com/chainstacklabs/pumpfun-cli). Buy, sell, launch tokens, manage wallets — with dry-run safety, slippage validation, and PumpSwap AMM migration. Works with OpenClaw, Claude Code, Cursor, Codex.
  - 💰 **Monetize:** Token trading profits, agent-driven launches, trading fee collection

---

## MEV & Arbitrage

- [**Artemis**](https://github.com/paradigmxyz/artemis) ⭐ 3k - Simple, modular, fast MEV bot framework in Rust by Paradigm.
  - 💰 **Monetize:** Sandwich attacks, liquidations, arbitrage profits, MEV extraction

- [**Jito MEV Bot**](https://github.com/jito-labs/mev-bot) ⭐ 1.2k - Official Jito Labs MEV bot for Solana.
  - 💰 **Monetize:** Solana MEV extraction, liquidations, arbitrage

- [**mev-template-rs**](https://github.com/degatchi/mev-template-rs) ⭐ 725 - Bootstrap MEV bot strategies with Rust boilerplate.
  - 💰 **Monetize:** Build custom MEV strategies, consulting, bot-as-a-service

- [**mev-templates**](https://github.com/solidquant/mev-templates) ⭐ 577 - MEV templates in Python/Javascript/Rust. DEX flashloan arbitrage.
  - 💰 **Monetize:** Cross-DEX arbitrage, flashloan profits, strategy development

- [**Rust Solana MEV Bot**](https://github.com/SaoXuan/rust-mev-bot-shared) ⭐ 452 - Rust Solana MEV 套利机器人. High-performance arbitrage bot for Solana.
  - 💰 **Monetize:** Solana arbitrage, MEV extraction, bot licensing

- [**q-evm**](https://github.com/sambacha/q-evm) ⭐ 420 - MEV Bot and Flashbots Bundler written in q using kdb+. High-performance quantitative approach.
  - 💰 **Monetize:** Quantitative MEV extraction, flashbot bundling, strategy licensing

- [**Ethereum-BNB MEV Bot**](https://github.com/sorasuzukidev/ethereum-bnb-mev-bot) ⭐ 364 - Ethereum and BNB (BSC) MEV bot for arbitrage across both chains.
  - 💰 **Monetize:** Cross-chain MEV extraction, multi-chain arbitrage profits

- [**Loom**](https://github.com/dexloom/loom) ⭐ 332 - MEV Bot based on Alloy. Modern EVM MEV extraction.
  - 💰 **Monetize:** EVM MEV extraction, liquidations, arbitrage strategies

- [**DeFi-bot**](https://github.com/ExtropyIO/defi-bot) ⭐ 1.2k - Tutorial for building DeFi arbitrage bots. Educational foundation for MEV strategies.
  - 💰 **Monetize:** DeFi arbitrage profits, educational courses, consulting

---

## Prediction Markets

### Polymarket Tools

- [**Polymarket Agents**](https://github.com/Polymarket/agents) ⭐ 3.8k - Official Polymarket AI agents. Trade autonomously using AI on prediction markets. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Automated trading profits, agent customization services

- [**Prediction Market Analysis**](https://github.com/Jon-Becker/prediction-market-analysis) ⭐ 3.8k - Framework for collecting and analyzing prediction market data. Largest public dataset of Polymarket and Kalshi market/trade data.
  - 💰 **Monetize:** Data feeds, analytics API, research reports, trading signals

- [**poly-maker**](https://github.com/warproxxx/poly-maker) ⭐ 1.5k - Market making bot for Polymarket. Configurable via Google Sheets. Provides liquidity on both sides of the book.
  - 💰 **Monetize:** Market making spreads, managed MM services

- [**py-clob-client**](https://github.com/Polymarket/py-clob-client) ⭐ 1.2k - Official Python client for the Polymarket CLOB (Central Limit Order Book). ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Build custom trading bots, API services, consulting

- [**Polyseer**](https://github.com/yorkeccak/Polyseer) ⭐ 668 - Polymarket alpha at the speed of now. Real-time alerts and signals.
  - 💰 **Monetize:** Premium alerts, signal subscription, API access

- [**poly_data**](https://github.com/warproxxx/poly_data) ⭐ 2.3k - Polymarket data retriever. Fetches, processes markets, order events, and trades.
  - 💰 **Monetize:** Data feeds, analytics API, research reports

- [**pmxt**](https://github.com/pmxt-dev/pmxt) ⭐ 2.1k - Unified API for trading across prediction markets (Polymarket, Kalshi, etc.).
  - 💰 **Monetize:** Cross-platform arbitrage, multi-market bots, API service

- [**PolymarketBTC15mAssistant**](https://github.com/FrondEnt/PolymarketBTC15mAssistant) ⭐ 1k - Real-time Polymarket BTC 15m trading assistant for every trader.
  - 💰 **Monetize:** Trading signals, subscription service, managed trading

- [**Cross-Market State Fusion**](https://github.com/humanplane/cross-market-state-fusion) ⭐ 384 - RL agent fusing real-time Binance futures data into Polymarket prediction markets. On-device training with MLX on Apple Silicon.
  - 💰 **Monetize:** Cross-market signals, AI model licensing, trading service

- [**rs-clob-client**](https://github.com/Polymarket/rs-clob-client) ⭐ 686 - Official Polymarket Rust CLOB client. High-performance order book access. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Build ultra-fast trading bots, HFT strategies, API services

- [**clob-client (TS)**](https://github.com/Polymarket/clob-client) ⭐ 515 - Official TypeScript client for the Polymarket CLOB. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Build custom bots, trading dashboards, API integrations

- [**5min-btc-polymarket**](https://github.com/Novals83/5min-btc-polymarket) ⭐ 749 - OpenClaw skill for BTC 5-minute Polymarket momentum trading with configurable risk controls and optional hedge logic.
  - 💰 **Monetize:** Short-window trading profits, signal subscription, skill sales on ClawHub

- [**Prediction Markets Trading Bot Toolkits**](https://github.com/HarrierOnChain/Prediction-Markets-Trading-Bot-Toolkits) ⭐ 427 - Production-grade Rust bots for Polymarket, Kalshi, and Limitless. 10 strategies on one execution core.
  - 💰 **Monetize:** Multi-venue strategy execution, bot licensing, managed trading

### Arbitrage Bots

- [**polymarket-arbitrage-trading-bot**](https://github.com/radioman/polymarket-arbitrage-trading-bot) ⭐ 517 - Arbitrage bot for BTC/ETH 5-minute Polymarket markets. Automated execution, real-time analytics, smart-wallet copy trading.
  - 💰 **Monetize:** Arbitrage spreads, copy-trading service, signal alerts

- [**polymarket-kalshi-btc-arbitrage-bot**](https://github.com/CarlosIbCu/polymarket-kalshi-btc-arbitrage-bot) - Real-time arbitrage between Polymarket and Kalshi on Bitcoin markets.
  - 💰 **Monetize:** Execute profitable arbs, sell signals/alerts

- [**prediction-market-arbitrage-bot**](https://github.com/realfishsam/prediction-market-arbitrage-bot) - Synthetic arbitrage (buy YES on one platform, NO on another).
  - 💰 **Monetize:** Arbitrage execution, managed arb service

### Resources

- [**Awesome-Prediction-Market-Tools**](https://github.com/aarora4/Awesome-Prediction-Market-Tools) - Curated list including YN Signals (24/7 alpha aggregator) and Eventarb (free arb alerts).

---

## DeFi & Yield Farming

- [**yield-farmers-almanac**](https://github.com/corbinpage/yield-farmers-almanac) - Community-sourced DeFi yield farming opportunities database.
  - 💰 **Monetize:** Premium data feeds, analysis reports, tools built on top

- [**swapper-toolkit**](https://github.com/swapperfinance/swapper-toolkit) ⭐ 845 - DeFi toolkit for AI agents — deposit funds, execute trades, manage wallets. Works with OpenClaw, Claude Code, CrewAI, AutoGPT.
  - 💰 **Monetize:** Agent-executed DeFi strategies, managed wallets, trading-as-a-service

### OpenClaw DeFi Skills

- [**BankrBot Skills**](https://github.com/BankrBot/skills) - OpenClaw skills for Polymarket betting, crypto trading, DeFi operations, leverage trading, portfolio management. Multi-chain: Base, Ethereum, Polygon, Solana.
  - 💰 **Monetize:** Sell skills on ClawHub, partner with exchanges for affiliate volume

---

## Airdrop Farming

- [**MasterCryptoFarmBot**](https://github.com/masterking32/MasterCryptoFarmBot) ⭐ 241 - Foundation for building crypto farming and airdrop bots for Telegram-based games.
  - 💰 **Monetize:** Airdrop farming profits, sell bot access, multi-account management

- [**Telegram-Airdrop-Bot**](https://github.com/fabston/Telegram-Airdrop-Bot) ⭐ 212 - Manage Telegram airdrops on ERC-20, BEP-20 tokens.
  - 💰 **Monetize:** Run airdrop campaigns, token distribution service

- [**t3rn-airdrop-bot**](https://github.com/dante4rt/t3rn-airdrop-bot) ⭐ 206 - Automate transactions and bridging on t3rn network for airdrop farming.
  - 💰 **Monetize:** Airdrop farming, multi-wallet management, bridge fee farming

- [**blum-airdrop-bot**](https://github.com/dante4rt/blum-airdrop-bot) ⭐ 136 - Automate Blum airdrop: claim rewards, manage farming, complete tasks, play games.
  - 💰 **Monetize:** Blum token farming, managed farming service

- [**nodepay-airdrop-bot**](https://github.com/dante4rt/nodepay-airdrop-bot) ⭐ 111 - Automate Nodepay airdrop with session management and proxy support.
  - 💰 **Monetize:** Nodepay token farming, bandwidth monetization

- [**polyflow-airdrop-bot**](https://github.com/dante4rt/polyflow-airdrop-bot) ⭐ 103 - Farm Scan2Earn points on PolyFlow by auto-uploading invoices.
  - 💰 **Monetize:** PolyFlow points farming, invoice submission automation

---

## Lead Generation & Sales

### LinkedIn Automation

- [**OpenOutreach**](https://github.com/eracle/OpenOutreach) ⭐ 2.9k - LinkedIn automation: visit profiles, connect, message with AI.
  - 💰 **Monetize:** B2B lead gen, outreach agency, connection building service

- [**linvo-scraper**](https://github.com/linvo-io/linvo-scraper) ⭐ 628 - LinkedIn automation with comprehensive scraping. Production-grade.
  - 💰 **Monetize:** Lead scraping service, data enrichment, profile export

### Lead Generation

- [**ScrapeGraphAI**](https://github.com/ScrapeGraphAI/Scrapegraph-ai) ⭐ 30.1k - Python scraper based on AI. Uses LLMs to understand and extract structured data from any website.
  - 💰 **Monetize:** Intelligent scraping SaaS, data extraction services, lead enrichment platform

- [**ai-lead-generator**](https://github.com/brightdata/ai-lead-generator) - AI-powered lead gen using Bright Data scraping + OpenAI for qualification/enrichment. Streamlit UI with instant lead scoring.
  - 💰 **Monetize:** Sell lead lists, B2B SaaS subscription, charge per lead

- [**ai-web-scraper**](https://github.com/kaymen99/ai-web-scraper) - AI web scraper using Crawl4AI. Supports GPT-4o, Claude, DeepSeek, Gemini via LiteLLM.
  - 💰 **Monetize:** Scraping service, subscription tiers, white-label tool

- [**SalesGPT**](https://github.com/filip-michalsky/SalesGPT) ⭐ 2.7k+ - Context-aware AI sales agent for voice, email, SMS. Autonomous across sales funnel stages.
  - 💰 **Monetize:** Outbound sales automation, enterprise SDR replacement, subscription campaigns

- [**Google-Maps-Scraper**](https://github.com/omkarcloud/google-maps-scraper) ⭐ 3.2k - Bulk scrape Google Maps (names, addresses, phones, emails, ratings).
  - 💰 **Monetize:** Sell local business leads, B2B contact databases

- [**ChatGPT Scraper**](https://github.com/oxylabs/chatgpt-scraper) ⭐ 3.3k - Collect ChatGPT responses via Web Scraper API. Automated prompt responses.
  - 💰 **Monetize:** AI response aggregation, research automation, data collection service

---

## Content Creation

- [**MoneyPrinterTurbo**](https://github.com/harry0703/MoneyPrinterTurbo) ⭐ 119k - AI one-click HD short video generation.
  - 💰 **Monetize:** YouTube/TikTok monetization, affiliate marketing, video ads

- [**MoneyPrinterV2**](https://github.com/FujiwaraChoki/MoneyPrinterV2) ⭐ 31.7k - Automate the process of making money online. Full automation pipeline for content creation and publishing.
  - 💰 **Monetize:** Faceless channels, automated content farms, video-as-a-service

- [**CogVideo**](https://github.com/zai-org/CogVideo) ⭐ 13k - Text/image to video generation.
  - 💰 **Monetize:** Content creation, ads, social media, video SaaS

- [**SoraFM**](https://github.com/all-in-aigc/sorafm) ⭐ 1.2k - Sora AI Video Generator web interface. Generate videos with OpenAI Sora API.
  - 💰 **Monetize:** Video generation service, SaaS platform, API reselling

- [**YumCut**](https://github.com/IgorShadurin/app.yumcut.com) ⭐ 865 - Free AI video generator for TikTok, Reels, YouTube Shorts. Auto script, scenes, voiceover, subtitles. Multi-language.
  - 💰 **Monetize:** Short-form content agency, faceless channel automation, white-label platform

- [**AI Video Generator Agent**](https://github.com/davide97l/ai-video-generator) ⭐ 141 - AI agent that automatically generates and posts short videos. Full automation pipeline.
  - 💰 **Monetize:** Faceless channel automation, content agency, video-as-a-service

- [**gpt-image2-ppt-skills**](https://github.com/JuneYaooo/gpt-image2-ppt-skills) ⭐ 1.2k - Clone any .pptx layout with GPT Image 2 and drop in your own content. 10 bundled styles, OpenClaw/Claude Code skill.
  - 💰 **Monetize:** Deck design service, template packs, pitch-deck-as-a-service

### YouTube Automation

- [**gemini-youtube-automation**](https://github.com/ChaitanyaEswarRajeshJakki/gemini-youtube-automation) ⭐ 332 - Fully autonomous AI pipeline using Gemini to generate and upload educational videos to YouTube.
  - 💰 **Monetize:** Educational channel monetization, faceless channels, course promotion

- [**youtube-automation-agent**](https://github.com/darkzOGx/youtube-automation-agent) ⭐ 2.9k - Fully automated YouTube channel with AI agents. Creates, optimizes, publishes 24/7. Works with free Gemini API.
  - 💰 **Monetize:** Ad revenue, affiliate marketing, brand deals

### Social Media Automation

- [**Auto_Social_Media_Content_Generator**](https://github.com/PatrykIA/Auto_Social_Media_Content_Generator) - Automation for Facebook, Instagram, X, LinkedIn with AI text + Canva images. Auto-posts every 2 days.
  - 💰 **Monetize:** SaaS subscription, agency white-label, manage client accounts

- [**ALwrity**](https://github.com/ALwrity/ALwrity) - AI Digital Marketing Platform with RAG, SEO, multilingual. Blog Writer (Research→Outline→Content→SEO→Publish).
  - 💰 **Monetize:** Monthly SaaS, per-article pricing, agency white-label

- [**distribb-skill**](https://github.com/Bomx/distribb-skill) ⭐ 184 - AI-powered SEO skill for OpenClaw/Claude Code/Codex. Write with your own model, publish through a backlink network.
  - 💰 **Monetize:** SEO retainers, backlink packages, programmatic content sites

---

## AI Agent Frameworks

Build monetizable AI agents with these frameworks:

### General Agent Frameworks

- [**Franklin**](https://github.com/BlockRunAI/franklin) ⭐ FEATURED - The first Autonomous Economic Agent. Natively spends USDC via x402 micropayments to execute real work — marketing campaigns, trading signals, content generation. Smart model routing, self-learning, plugin system.
  - 💰 **Monetize:** Build plugins, create agent workflows, offer agent-as-a-service with built-in payments

- [**Awesome LLM Apps**](https://github.com/Shubhamsaboo/awesome-llm-apps) ⭐ 135k - Collection of awesome LLM apps with AI Agents and RAG using OpenAI, Anthropic, Gemini, and open-source models.
  - 💰 **Monetize:** Clone and customize apps, build SaaS products, consulting services

- [**Gemini CLI**](https://github.com/google-gemini/gemini-cli) ⭐ 107k - Google's open-source AI agent that brings the power of Gemini directly into your terminal.
  - 💰 **Monetize:** Automation scripts, developer tools, enterprise integrations

- [**AutoGPT**](https://github.com/Significant-Gravitas/AutoGPT) ⭐ 187k - Accessible AI tools for building autonomous agents. Forge for agent creation, benchmarks, leaderboard.
  - 💰 **Monetize:** Build/sell custom agents, agent-as-a-service, enterprise licensing

- [**MetaGPT**](https://github.com/FoundationAgents/MetaGPT) ⭐ 70.1k - The Multi-Agent Framework: First AI Software Company. Assigns roles to agents (Product Manager, Architect, Engineer).
  - 💰 **Monetize:** AI software development agency, code generation SaaS, enterprise consulting

- [**Open Interpreter**](https://github.com/openinterpreter/openinterpreter) ⭐ 68.2k - A natural language interface for computers. Run code, control your computer with plain English.
  - 💰 **Monetize:** Automation services, enterprise deployments, managed computer-use agents

- [**Anything LLM**](https://github.com/Mintplex-Labs/anything-llm) ⭐ 65.4k - All-in-one Desktop & Docker AI application with built-in RAG, AI agents, no-code agent builder, MCP compatibility.
  - 💰 **Monetize:** Custom deployments, enterprise hosting, white-label platform

- [**Microsoft Autogen**](https://github.com/microsoft/autogen) ⭐ 60.7k - A programming framework for agentic AI. Multi-agent conversations, tool use, code execution.
  - 💰 **Monetize:** Enterprise agent solutions, consulting, custom multi-agent systems

- [**AI Agents for Beginners**](https://github.com/microsoft/ai-agents-for-beginners) ⭐ 73.5k - Microsoft's 12 lessons to get started building AI agents. Comprehensive curriculum.
  - 💰 **Monetize:** Training courses, bootcamps, enterprise workshops

- [**Flowise**](https://github.com/FlowiseAI/Flowise) ⭐ 55.4k - Build AI Agents visually. Drag-and-drop LLM flow builder with API endpoints. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Custom workflow development, managed hosting, enterprise deployments

- [**Mem0**](https://github.com/mem0ai/mem0) ⭐ 64.4k - Universal memory layer for AI Agents. Persistent memory across sessions.
  - 💰 **Monetize:** Memory-as-a-service, enterprise integrations, custom implementations

- [**CrewAI**](https://github.com/crewAIInc/crewAI) ⭐ 57.8k - Lean, fast Python framework for orchestrating role-playing AI agents with collaborative intelligence.
  - 💰 **Monetize:** Niche agents, consulting, pre-built templates, managed hosting

- [**ToolJet**](https://github.com/ToolJet/ToolJet) ⭐ 40.8k - Open-source foundation of ToolJet AI - AI-native platform for building internal tools, dashboards, workflows and AI agents.
  - 💰 **Monetize:** Internal tool development, enterprise licensing, custom integrations

- [**AgentGPT**](https://github.com/reworkd/AgentGPT) ⭐ 36.3k - Assemble, configure, and deploy autonomous AI Agents in your browser. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Custom agent development, SaaS platform, enterprise deployments

- [**Block Goose**](https://github.com/aaif-goose/goose) ⭐ 53.7k - Open source, extensible AI agent that goes beyond code suggestions - install, execute, edit, and test with any LLM.
  - 💰 **Monetize:** Development automation, custom extensions, enterprise licensing

- [**LangChain**](https://github.com/langchain-ai/langchain) ⭐ 145k - Framework for context-aware reasoning applications.
  - 💰 **Monetize:** LLM apps with monetized endpoints, consulting, templates

- [**LlamaIndex**](https://github.com/run-llama/llama_index) ⭐ 51.9k - Data-centric agents with RAG primitives. 500+ connectors via LlamaHub.
  - 💰 **Monetize:** Data-powered AI agents, specialized apps, consulting

- [**smolagents**](https://github.com/huggingface/smolagents) ⭐ 29.1k - HuggingFace's barebones library for agents that think in code. Simple, hackable, powerful.
  - 💰 **Monetize:** Custom coding agents, agent templates, enterprise integrations

- [**SuperAGI**](https://github.com/TransformerOptimus/SuperAGI) ⭐ 17.7k - Dev-first open source autonomous AI agent framework. Build, manage & run useful agents quickly.
  - 💰 **Monetize:** Custom agent development, managed infrastructure, enterprise licensing

- [**Jobs Applier AI Agent (AIHawk)**](https://github.com/feder-cr/Jobs_Applier_AI_Agent_AIHawk) ⭐ 30.3k - AI agent that automates job hunt by applying to multiple jobs in a tailored way.
  - 💰 **Monetize:** Job application service, subscription platform, career coaching integration

- [**UI-TARS Desktop**](https://github.com/bytedance/UI-TARS-desktop) ⭐ 38.8k - ByteDance's open-source multimodal AI agent stack connecting AI models and agent infra.
  - 💰 **Monetize:** Desktop automation, enterprise deployments, custom integrations

- [**Composio**](https://github.com/ComposioHQ/composio) ⭐ 30k - Equips AI agents & LLMs with 100+ high-quality integrations via function calling.
  - 💰 **Monetize:** Integration platform, custom connectors, enterprise licensing

- [**Sim Studio**](https://github.com/simstudioai/sim) ⭐ 29.5k - Open-source platform to build and deploy AI agent workflows.
  - 💰 **Monetize:** Workflow templates, managed hosting, enterprise solutions

- [**Warp**](https://github.com/warpdotdev/Warp) ⭐ 64.7k - The agentic development environment, built for coding with multiple AI agents.
  - 💰 **Monetize:** Developer tool licensing, enterprise features, custom integrations

- [**Graphiti**](https://github.com/getzep/graphiti) ⭐ 30.4k - Build real-time knowledge graphs for AI agents. Persistent structured memory.
  - 💰 **Monetize:** Knowledge graph services, enterprise memory solutions, consulting

- [**Roo Code**](https://github.com/RooCodeInc/Roo-Code) ⭐ 24.3k - A whole dev team of AI agents in your code editor. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Enterprise licensing, custom agent development, training

- [**Activepieces**](https://github.com/activepieces/activepieces) ⭐ 24.1k - AI Agents & MCPs & AI Workflow Automation with ~400 MCP servers for AI agents.
  - 💰 **Monetize:** Workflow marketplace, managed hosting, enterprise integrations

- [**GenAI Agents**](https://github.com/NirDiamant/GenAI_Agents) ⭐ 24k - In-depth tutorials and implementations for various Generative AI Agent techniques.
  - 💰 **Monetize:** Training courses, enterprise workshops, consulting

- [**Coze Studio**](https://github.com/coze-dev/coze-studio) ⭐ 21.5k - AI agent development platform with all-in-one visual tools for creation, debugging, and deployment.
  - 💰 **Monetize:** Agent marketplace, managed platform, enterprise features

- [**Suna (Kortix)**](https://github.com/kortix-ai/suna) ⭐ 20.2k - Build, manage and train AI Agents with Kortix platform.
  - 💰 **Monetize:** Agent training services, managed platform, enterprise licensing

- [**Qwen Code**](https://github.com/QwenLM/qwen-code) ⭐ 27.5k - Open-source AI agent that lives in your terminal, powered by Qwen.
  - 💰 **Monetize:** Developer automation, enterprise licensing, custom extensions

- [**Eliza**](https://github.com/elizaOS/eliza) ⭐ 19.2k - Autonomous agents for everyone. Popular framework for crypto/social media agents. Multi-platform (Discord, Twitter, Telegram).
  - 💰 **Monetize:** Social media agents, crypto trading bots, community management agents

- [**Qwen-Agent**](https://github.com/QwenLM/Qwen-Agent) ⭐ 17k - Agent framework built on Qwen. Features Function Calling, MCP, Code Interpreter, RAG, Chrome extension.
  - 💰 **Monetize:** Qwen-powered apps, MCP integrations, browser extensions

- [**VoltAgent**](https://github.com/VoltAgent/voltagent) ⭐ 10.5k - AI Agent Engineering Platform built on TypeScript. Production-ready agent orchestration.
  - 💰 **Monetize:** Agent templates, platform licensing, consulting services

- [**PraisonAI**](https://github.com/MervinPraison/PraisonAI) ⭐ 9k - Production-ready Multi AI Agents framework. Low-code solution for building and managing multi-agent LLM systems.
  - 💰 **Monetize:** Pre-built agent teams, custom workflows, managed deployments

- [**HKUDS/ClawWork**](https://github.com/HKUDS/ClawWork) ⭐ 8.5k - OpenClaw as Your AI Coworker. Autonomous 24/7 task execution — $10K earned in 7 hours (case study).
  - 💰 **Monetize:** Freelancing automation, agentic task marketplace, enterprise coworker licensing

- [**HKUDS/nanobot**](https://github.com/HKUDS/nanobot) ⭐ 47.5k - Ultra-Lightweight OpenClaw. Minimal footprint, full capability — ideal for edge deployments.
  - 💰 **Monetize:** Embedded agent services, IoT automation, lightweight enterprise deployments

- [**nanoclaw**](https://github.com/nanocoai/nanoclaw) ⭐ 30.7k - Lightweight alternative to OpenClaw that runs in containers for security and scalability.
  - 💰 **Monetize:** Container-native agent services, multi-tenant deployments, self-hosted SaaS

- [**NevaMind-AI/memU**](https://github.com/NevaMind-AI/memU) ⭐ 14.4k - Memory layer for 24/7 proactive agents (OpenClaw, Moltbot, Clawdbot). Long-term context across sessions.
  - 💰 **Monetize:** Memory-as-a-service for agents, personalized AI assistant products

- [**iOfficeAI/AionUi**](https://github.com/iOfficeAI/AionUi) ⭐ 32.4k - Free, local, open-source 24/7 cowork app and OpenClaw for Gemini CLI, Claude Code.
  - 💰 **Monetize:** Desktop agent licensing, enterprise 24/7 workflow automation

- [**AgentOps**](https://github.com/AgentOps-AI/agentops) ⭐ 5.8k - Python SDK for AI agent monitoring, LLM cost tracking, benchmarking. Integrates with CrewAI, Langchain, Autogen.
  - 💰 **Monetize:** Agent observability platform, enterprise monitoring, cost optimization consulting

- [**Pydantic-AI**](https://github.com/pydantic/pydantic-ai) - GenAI Agent Framework with validation layer for OpenAI, Anthropic, Google SDKs.
  - 💰 **Monetize:** Validated agent applications, development services

- [**Cherry Studio**](https://github.com/CherryHQ/cherry-studio) ⭐ 51.3k - AI productivity studio with smart chat, autonomous agents, and 300+ assistants. Unified access to frontier LLMs.
  - 💰 **Monetize:** White-label AI productivity platform, enterprise deployments, custom assistant development

- [**AgenticSeek**](https://github.com/Fosowl/agenticSeek) ⭐ 27.1k - Fully local autonomous agent. No APIs, no subscriptions. Thinks, browses the web, and codes locally.
  - 💰 **Monetize:** Privacy-first AI consulting, on-prem enterprise deployments, local agent solutions

- [**OpenAI Agents Python**](https://github.com/openai/openai-agents-python) ⭐ 29.1k - OpenAI's lightweight, powerful framework for multi-agent workflows.
  - 💰 **Monetize:** Multi-agent SaaS products, enterprise agent orchestration, consulting

- [**DB-GPT**](https://github.com/eosphoros-ai/DB-GPT) ⭐ 19.8k - AI Native Data App Development framework with Agentic Workflow Expression Language (AWEL) and Agents.
  - 💰 **Monetize:** Data-powered AI apps, enterprise data agents, analytics automation

- [**Plandex**](https://github.com/plandex-ai/plandex) ⭐ 15.6k - Open source AI coding agent designed for large projects and real world tasks.
  - 💰 **Monetize:** Enterprise coding automation, development agency, managed coding agents

- [**OpenCode**](https://github.com/opencode-ai/opencode) ⭐ 13.7k - Powerful AI coding agent built for the terminal. Open-source alternative to proprietary coding agents. ⚠️ *archived — repo is read-only*
  - 💰 **Monetize:** Developer automation, custom extensions, enterprise licensing

- [**Microsoft Agent Framework**](https://github.com/microsoft/agent-framework) ⭐ 13.2k - Framework for building, orchestrating and deploying AI agents and multi-agent workflows (Python and .NET).
  - 💰 **Monetize:** Enterprise agent solutions, .NET/Python agent development, consulting

- [**Omnigent**](https://github.com/omnigent-ai/omnigent) ⭐ 9.5k - Open-source agent framework and meta-harness. Orchestrate Claude Code, Codex, Cursor, and custom agents behind one policy + sandbox layer.
  - 💰 **Monetize:** Multi-harness agent platform, managed agent ops, enterprise policy consulting

- [**Heurist Agent Framework**](https://github.com/heurist-network/heurist-agent-framework) ⭐ 821 - Multi-interface agent framework with reasoning, memory, deep research, blockchain interaction, MCP, and agents-as-a-service.
  - 💰 **Monetize:** Agents-as-a-service, on-chain agent products, research automation

- [**Aeon**](https://github.com/aeonfun/aeon) ⭐ 707 - Autonomous agents that run unattended on GitHub Actions with self-healing skills. Drives Claude Code, Grok, and Codex.
  - 💰 **Monetize:** Always-on automation service, CI-hosted agent products, zero-ops agent hosting

- [**Spraay x402 Gateway**](https://gateway.spraay.app) — Multi-chain x402 payment gateway wrapping BlockRun's `@blockrun/llm` SDK as a production AI provider. 62 paid endpoints across AI inference, payments, DeFi, oracles, comms, and infrastructure.
  - 💰 **Monetize:** Charge agents $0.01–$0.10 per x402 endpoint call, pay BlockRun ~$0.001–$0.01 per inference via x402, keep the spread on every request.

### OpenClaw Infrastructure

Tools for deploying, hosting, monitoring, and securing OpenClaw AI agents in production.

- [**ClawX**](https://github.com/ValueCell-ai/ClawX) ⭐ 7.6k - Desktop app GUI for OpenClaw AI agents. Turns CLI-based AI orchestration into a visual desktop experience.
  - 💰 **Monetize:** Sell configured desktop agent packages, enterprise onboarding, white-label deployments

- [**openclaw-dashboard**](https://github.com/tugcantopaloglu/openclaw-dashboard) ⭐ 698 - Secure, real-time monitoring dashboard for OpenClaw. Auth, TOTP MFA, cost tracking, live feed, memory browser.
  - 💰 **Monetize:** Managed agent monitoring service, enterprise security deployments

- [**ClawApp**](https://github.com/qingchencloud/clawapp) ⭐ 443 - Mobile chat client for OpenClaw AI Agent. Streaming conversations, image support, tool calls. PWA + APK.
  - 💰 **Monetize:** Mobile agent subscription, white-label app, consumer AI assistant

- [**ClawBands**](https://github.com/SeyZ/clawbands) ⭐ 196 - Security middleware for OpenClaw AI agents. Protect against prompt injection, enforce policies, audit actions.
  - 💰 **Monetize:** Enterprise security layer, compliance consulting, managed safety service

- [**openclaw-operator**](https://github.com/paperclipinc/openclaw-operator) ⭐ 395 - Kubernetes operator for deploying and managing OpenClaw agent instances with production-grade security, observability, and lifecycle management.
  - 💰 **Monetize:** Enterprise K8s deployments, multi-tenant agent platforms, DevOps consulting

- [**openclaw-kapso-whatsapp**](https://github.com/Enriquefft/openclaw-kapso-whatsapp) ⭐ 207 - Give your OpenClaw agent a WhatsApp number. Official Meta Cloud API via Kapso. No ban risk.
  - 💰 **Monetize:** AI WhatsApp business bots, customer support automation, WhatsApp CRM agents

- [**clawmetry**](https://github.com/vivekchand/clawmetry) ⭐ 401 - Real-time observability dashboard for OpenClaw agents. See your agent think.
  - 💰 **Monetize:** Agent monitoring SaaS, cost optimization consulting, enterprise observability

- [**serverless-openclaw**](https://github.com/serithemage/serverless-openclaw) ⭐ 193 - Run OpenClaw on AWS serverless infrastructure with Web UI and Telegram interfaces. Cost target ~$1/month.
  - 💰 **Monetize:** Ultra-cheap agent hosting service, serverless agent deployment, AWS consulting

- [**ClawKeeper**](https://github.com/SafeAI-Lab-X/ClawKeeper) ⭐ 1k - Safety layer for OpenClaw agents via skills, plugins, and watchers. "The Norton for OpenClaw."
  - 💰 **Monetize:** Managed agent safety, compliance audits, enterprise security add-on

- [**openclaw-supermemory**](https://github.com/supermemoryai/openclaw-supermemory) ⭐ 799 - Long-term memory and recall for OpenClaw agents.
  - 💰 **Monetize:** Memory-as-a-service, personalized agent products, retention tooling

- [**ClawDeck**](https://github.com/clawdeckio/clawdeck) ⭐ 362 - Open-source mission control for fleets of OpenClaw agents.
  - 💰 **Monetize:** Agent fleet management SaaS, ops consulting, white-label control plane

### Browser Automation Agents

- [**browser-use**](https://github.com/browser-use/browser-use) ⭐ 112k - Make websites accessible for AI agents. Automate any web task with natural language.
  - 💰 **Monetize:** Web automation services, form filling bots, data extraction, testing automation

- [**Stagehand**](https://github.com/browserbase/stagehand) ⭐ 24.1k - The AI Browser Automation Framework. Built on Playwright with AI-powered element selection.
  - 💰 **Monetize:** Web scraping services, testing automation, browser-based RPA

- [**Skyvern**](https://github.com/Skyvern-AI/skyvern) ⭐ 22.9k - Automate browser-based workflows with AI. Computer vision + LLM for robust web automation.
  - 💰 **Monetize:** Enterprise browser automation, form filling services, web RPA

- [**LaVague**](https://github.com/lavague-ai/LaVague) ⭐ 6.4k - Large Action Model framework to develop AI Web Agents. Natural language to browser actions.
  - 💰 **Monetize:** Web automation platform, custom browser agents, enterprise deployments

- [**ShowUI**](https://github.com/showlab/ShowUI) ⭐ 1.9k - Vision-Language-Action model for GUI Agent & Computer Use. CVPR 2025 paper implementation.
  - 💰 **Monetize:** Desktop automation, GUI testing, accessibility services

---

## OpenClaw Skills

- [**BankrBot Skills**](https://github.com/BankrBot/skills) - Polymarket, crypto trading, DeFi, leverage, portfolio management, NFTs. Multi-chain support.

- [**VoltAgent/awesome-openclaw-skills**](https://github.com/VoltAgent/awesome-openclaw-skills) ⭐ 52.3k - Curated collection of OpenClaw skills. 5,400+ skills filtered and categorized.

- [**openclaw/clawhub**](https://github.com/openclaw/clawhub) ⭐ 9.4k - Official skill directory and marketplace.

- [**clawdbot-ai/awesome-openclaw-skills-zh**](https://github.com/clawdbot-ai/awesome-openclaw-skills-zh) ⭐ 4.1k - OpenClaw 中文官方技能库. Translated from Clawdbot official skills, organized by scenario.
  - 💰 **Monetize:** Chinese-language skill marketplace, localized agent services

- [**sundial-org/awesome-openclaw-skills**](https://github.com/sundial-org/awesome-openclaw-skills) ⭐ 651 - Top OpenClaw skills, curated for popularity and usefulness.

- [**zscole/model-hierarchy-skill**](https://github.com/zscole/model-hierarchy-skill) ⭐ 345 - OpenClaw skill for cost-optimized model routing based on task complexity. ClawRouter-compatible.
  - 💰 **Monetize:** Save on LLM costs for high-volume workflows, sell as premium skill

- [**ythx-101/x-tweet-fetcher**](https://github.com/ythx-101/x-tweet-fetcher) ⭐ 950 - Fetch tweets and replies from X/Twitter without login or API keys. OpenClaw skill.
  - 💰 **Monetize:** Social media monitoring service, sentiment analysis, lead gen

- [**sharbelxyz/x-bookmarks**](https://github.com/sharbelxyz/x-bookmarks) ⭐ 288 - OpenClaw skill: turn your X bookmarks into agent actions.
  - 💰 **Monetize:** Research automation, content curation service

- [**LeoYeAI/openclaw-master-skills**](https://github.com/LeoYeAI/openclaw-master-skills) ⭐ 2.1k - Curated collection of 1,209+ OpenClaw skills, updated weekly.

- [**rohunvora/x-research-skill**](https://github.com/rohunvora/x-research-skill) ⭐ 1.2k - X/Twitter research skill for Claude Code and OpenClaw. Agentic search, thread following, sourced briefings.
  - 💰 **Monetize:** Research briefings, competitor intel reports, newsletter sourcing

- [**LeoYeAI/openclaw-marketing-skills**](https://github.com/LeoYeAI/openclaw-marketing-skills) ⭐ 1k - 33 battle-tested marketing skills for OpenClaw agents.
  - 💰 **Monetize:** Marketing agency automation, campaign-as-a-service, skill packs

- [**nashsu/autocli-skill**](https://github.com/nashsu/autocli-skill) ⭐ 921 - Reach 55+ platforms (X, YouTube, Reddit, TikTok, Bilibili, Zhihu…) with natural language, reusing your Chrome session — no API keys.
  - 💰 **Monetize:** Social listening service, data collection contracts, trend reports

- [**BlockRunAI/socialclaw**](https://github.com/BlockRunAI/socialclaw) ⭐ 1 - X/Twitter intelligence + content optimization skill. Research accounts, track trends, draft algorithm-optimized posts, monitor engagement. Works with Claude Code, Codex, Gemini CLI, Cursor. $0.08/report via USDC micropayments.
  - 💰 **Monetize:** X/Twitter growth consulting, content strategy services, competitor analysis reports, influencer research packages

---

## Workflow Automation

- [**n8n-workflow-builder**](https://github.com/makafeli/n8n-workflow-builder) ⭐ 541 - AI assistant for n8n via MCP. Connect Claude, ChatGPT to n8n for natural language workflow management.
  - 💰 **Monetize:** Custom workflow development, automation consulting, managed n8n hosting

- [**n8n-skills**](https://github.com/haunchen/n8n-skills) ⭐ 393 - n8n Workflow Automation Skills Suite designed for AI assistants. Ready-to-use workflow templates.
  - 💰 **Monetize:** Skill marketplace, automation courses, enterprise deployments

- [**N8N-Workflows**](https://github.com/DINAKAR-S/N8N-Workflows) - Real-world n8n automation for lead gen, AI agents, web scraping, social media.
  - 💰 **Monetize:** Sell workflow templates, automation consulting, monthly management

- [**n8n-ai-automations**](https://github.com/lucaswalter/n8n-ai-automations) - Advanced workflows: law firm lead gen, competitor UGC analysis, personalized outreach.
  - 💰 **Monetize:** Niche workflow packages, agency white-label, training

- [**ai-automation-jsons**](https://github.com/simealdana/ai-automation-jsons) - Collection of n8n workflow JSONs for AI agents, integrations, automated processes. Ready-to-import.
  - 💰 **Monetize:** Workflow marketplace, custom development, automation agency

---

## MCP Servers & Tools

Model Context Protocol (MCP) enables AI agents to connect to external tools and data sources. These servers unlock new monetization opportunities for agents.

### Infrastructure

- [**Awesome MCP Servers**](https://github.com/punkpeye/awesome-mcp-servers) ⭐ 93.4k - The definitive collection of MCP servers. 500+ servers across all categories.
  - 💰 **Monetize:** Build and list premium MCP servers, consulting for MCP integration

- [**Context7**](https://github.com/upstash/context7) ⭐ 61.4k - Up-to-date code documentation MCP server. Gives AI agents current docs instead of stale training data.
  - 💰 **Monetize:** Documentation services, enterprise code intelligence, dev tool integrations

- [**FastMCP**](https://github.com/PrefectHQ/fastmcp) ⭐ 27.4k - The fast, Pythonic way to build MCP servers. Production-ready framework for building custom servers.
  - 💰 **Monetize:** Custom MCP server development, consulting, enterprise integrations

- [**MCP-Use**](https://github.com/mcp-use/mcp-use) ⭐ 10.5k - Easiest way to interact with MCP servers using custom agents. Agent-first MCP client.
  - 💰 **Monetize:** Agent development services, MCP integration consulting

### Data & APIs

- [**blockrun-mcp**](https://github.com/BlockRunAI/blockrun-mcp) ⭐ 393 - Live data for AI agents — search, research, markets, crypto, X/Twitter. Pay-per-call via x402 micropayments. Also available hosted at [`mcp.blockrun.ai`](https://github.com/BlockRunAI/blockrun-mcp-server) (zero install).
  - 💰 **Monetize:** Build paid data agents, package research workflows, charge per-report with USDC micropayments

- [**The Stall**](https://github.com/thebrierfox/the-stall) ⭐ 7 - x402-native MCP server with 210 pay-per-call data tools: US/EU/JP equities, crypto/DeFi, options GEX, dealer gamma, congressional trades, GDELT news, weather history, sanctions screening. Hosted at [`the-stall.intuitek.ai/mcp`](https://the-stall.intuitek.ai/mcp), USDC on Base, no API keys.
  - 💰 **Monetize:** Feed pay-per-call market data into Franklin, trading bots, or agent pipelines — pay per query instead of $500+/mo data subscriptions

- [**Worklittle Jobs MCP**](https://github.com/worklittle/jobs-mcp) - Remote MCP over 4M+ job listings with visa, salary, and distance filters. Swipe to apply from your agent, save roles to a Worklittle account. Hosted at [`mcp.worklittle.com`](https://mcp.worklittle.com/).
  - 💰 **Monetize:** Automated job-application agents, recruiting-as-a-service, candidate sourcing pipelines

- [**MindsDB**](https://github.com/mindsdb/mindshub) ⭐ 39.7k - Federated Query Engine for AI. The only MCP Server you'll ever need for database access.
  - 💰 **Monetize:** Data pipeline services, enterprise AI data integration, managed MindsDB hosting

- [**GitHub MCP Server**](https://github.com/github/github-mcp-server) ⭐ 32.6k - GitHub's official MCP server. Agents can manage repos, issues, PRs, code search.
  - 💰 **Monetize:** DevOps automation, code review agents, repo management bots

- [**MCP Toolbox**](https://github.com/googleapis/mcp-toolbox) ⭐ 16.3k - Google's MCP Toolbox for Databases. Connect AI to PostgreSQL, MySQL, BigQuery, Spanner.
  - 💰 **Monetize:** Database automation, data extraction services, analytics pipelines

- [**Git-MCP**](https://github.com/idosal/git-mcp) ⭐ 8.4k - Free remote MCP server for any GitHub project. Eliminates code hallucinations with real repo context.
  - 💰 **Monetize:** Code accuracy services, developer tool integrations

### Browser & Automation

- [**Playwright MCP**](https://github.com/microsoft/playwright-mcp) ⭐ 36.6k - Microsoft's official Playwright MCP server. Full browser automation for AI agents.
  - 💰 **Monetize:** Web scraping services, testing automation, browser-based RPA

- [**MCP Chrome**](https://github.com/hangwin/mcp-chrome) ⭐ 12.4k - Chrome extension MCP server. Browser automation, content analysis, semantic search.
  - 💰 **Monetize:** Chrome automation bots, content extraction, research automation

- [**Figma Context MCP**](https://github.com/GLips/Figma-Context-MCP) ⭐ 15.7k - Provides Figma layout info to AI coding agents. Design-to-code automation.
  - 💰 **Monetize:** Design-to-code services, UI automation, Figma workflow tools

### Security & Research

- [**HexStrike AI**](https://github.com/0x4m4/hexstrike-ai) ⭐ 11.5k - MCP server with 150+ cybersecurity tools. Automated pentesting, vulnerability discovery, bug bounty automation.
  - 💰 **Monetize:** Security auditing services, bug bounty automation, penetration testing

- [**Serena**](https://github.com/oraios/serena) ⭐ 28.7k - Coding agent toolkit with semantic retrieval and editing. Production-ready code intelligence.
  - 💰 **Monetize:** Code refactoring services, codebase analysis, developer tools

---

## Research & Analysis

- [**GPT Researcher**](https://github.com/assafelovic/gpt-researcher) ⭐ 29.2k - Autonomous agent that conducts deep research on any topic. Generates comprehensive reports from multiple sources.
  - 💰 **Monetize:** Research-as-a-service, market analysis reports, competitive intelligence, due diligence automation

---

## Resources & Directories

### Awesome Lists

- [**BlockRunAI/awesome-blockrun**](https://github.com/BlockRunAI/awesome-blockrun) ⭐ 13 - BlockRun ecosystem hub — docs, SDKs, research, and community. Start here for everything in the x402-native agent stack.

- [**e2b-dev/awesome-ai-agents**](https://github.com/e2b-dev/awesome-ai-agents) ⭐ 29.8k - Comprehensive list of AI autonomous agents. Well-maintained with categories.

- [**mergisi/awesome-openclaw-agents**](https://github.com/mergisi/awesome-openclaw-agents) ⭐ 3.9k - 162 production-ready OpenClaw agent templates with SOUL.md configs across 19 categories.

- [**500-AI-Agents-Projects**](https://github.com/ashishpatel26/500-AI-Agents-Projects) - Curated AI agent use cases across industries (healthcare, finance, education, retail).

- [**awesome-ai-agents**](https://github.com/slavakurilyak/awesome-ai-agents) - 300+ agentic AI resources.

- [**awesome_ai_agents**](https://github.com/jim-schwoebel/awesome_ai_agents) - 1,500+ AI agent resources and tools.

- [**MakeMoneyWithAI**](https://github.com/garylab/MakeMoneyWithAI) - Curated list of open-source AI projects for generating income.

- [**AI-Agent-Platforms-Automation-Tools**](https://github.com/rembertdesigns/AI-Agent-Platforms-Automation-Tools) - Directory of autonomous AI agents, frameworks, platforms.

- [**hesamsheikh/awesome-openclaw-usecases**](https://github.com/hesamsheikh/awesome-openclaw-usecases) ⭐ 31.7k - Community collection of OpenClaw use cases for making life (and money) easier.

- [**AlexAnys/awesome-openclaw-usecases-zh**](https://github.com/AlexAnys/awesome-openclaw-usecases-zh) ⭐ 4.4k - 🇨🇳 OpenClaw 中文最佳用例大全 | 40 real-world scenarios adapted for China (domestic services + global platforms). Beginner-friendly Chinese guide.

- [**HKUDS/ClawWork**](https://github.com/HKUDS/ClawWork) ⭐ 8.5k - Case study: OpenClaw as autonomous AI coworker earning $10K in 7 hours.

### Infrastructure

- [**ClawRouter v0.12.256**](https://github.com/BlockRunAI/ClawRouter) ⭐ 6.6k - Smart LLM router, save <!-- br:savings.autoVsBaselinePct -->84<!-- /br:savings.autoVsBaselinePct -->% on inference. 16-model curated allowlist, one USDC wallet. **Features:** Response caching, 4 routing profiles, `/imagegen`, `clawrouter report`, three-strike escalation, `/debug`, tool-calling filter, session persistence, `clawrouter doctor`, multilingual support.
- [**BlockRun.ai**](https://blockrun.ai) - Pay-per-request AI via x402 micropayments.
- [**blockrun-mcp**](https://github.com/BlockRunAI/blockrun-mcp) ⭐ 393 - Live data MCP server for AI agents — search, research, markets, crypto, X/Twitter. Pay-per-call via x402 micropayments.
- [**blockrun-mcp-server**](https://github.com/BlockRunAI/blockrun-mcp-server) - Hosted MCP at `mcp.blockrun.ai` — one URL, any agent, zero install.
- **BlockRun SDKs** — OpenAI-compatible, pay-per-call USDC, zero rate limits: [Python](https://github.com/BlockRunAI/blockrun-llm) · [TypeScript](https://github.com/BlockRunAI/blockrun-llm-ts) · [Go](https://github.com/BlockRunAI/blockrun-llm-go) · [XRPL/RLUSD](https://github.com/BlockRunAI/blockrun-llm-xrpl)

#### Popular Models on BlockRun (Aug 2026)

| Model | Pricing (in/out per M) | Best For |
|-------|------------------------|----------|
| Claude Fable 5 | $10.00/$50.00 | Most capable Claude, long-horizon agentic work |
| Claude Opus 5 | $5.00/$25.00 | Deep reasoning + agentic coding, 1M context |
| Claude Sonnet 5 | $3.00/$15.00 | Near-Opus coding at Sonnet cost, 1M context |
| GPT-5.6 Terra | $2.00/$12.00 | Balanced everyday coding + agents, 1M context |
| GPT-5.6 Luna | $0.20/$1.20 | High-volume, latency-sensitive chat |
| GPT-5.3 Codex | $1.75/$14.00 | Agentic coding, 400K context |
| Gemini 3.1 Pro | $2.00/$12.00 | Advanced reasoning, software engineering |
| Gemini 3 Flash Preview | $0.50/$3.00 | Fast, cheap multimodal with thinking |
| Gemini 2.5 Flash Lite | $0.10/$0.40 | Ultra-cheap ECO tier default |
| Grok 4.5 | $2.50/$9.00 | Flagship Grok + Live Search, 500K context |
| Kimi K3 | $3.00/$15.00 | 2.8T MoE, 1M context, vision |
| GLM-5.3 Flash | $0.15/$0.50 | Multimodal value tier, 1M context |
| DeepSeek V4 Flash Chat | $0.14/$0.28 | Budget-friendly general use, 1M context |
| Qwen3.7 Flash | $0.03/$0.13 | Cheapest paid model in the catalog |
| Nemotron 3 Nano Omni | $0/$0 | Free tier fallback — the only free vision model |

### Data & Trading

- [DeFiLlama](https://defillama.com/) - TVL and yield data
- [Dune Analytics](https://dune.com/) - On-chain data
- [Binance API Docs](https://binance-docs.github.io/apidocs/)

---

## Cost Considerations

| Cost | Traditional | With ClawRouter v0.12.256 |
|------|-------------|----------------------|
| LLM API tokens | $50 - $500+/mo | $4 - $40+/mo |
| Hosting | $5 - $50/mo | $5 - $50/mo |
| Data APIs | $0 - $200/mo | $0 - $200/mo |
| **Break-even** | **~$220/month** | **~$75/month** |

**Blended cost:** $2.05/M tokens vs $25/M (Opus) = **<!-- br:savings.autoVsBaselinePct -->84<!-- /br:savings.autoVsBaselinePct -->% savings**

**Pro tip:** Use `/model eco` profile for maximum savings. Qwen3.7 Flash at $0.03/$0.13 is the cheapest paid model; Gemini 2.5 Flash Lite ($0.10/$0.40) is the ECO tier default. Kimi K3 offers 1M context at $3.00/$15.00 for long documents. Use `/imagegen` and `/img2img` for on-demand image work via x402 micropayments.

---

## Security Warnings

### ClawHub Marketplace
⚠️ **341 malicious skills found stealing credentials** (Feb 2026). Always audit skill code before installing.

### Trading Safety
- Never give agents withdrawal permissions
- Use API keys with trade-only access
- Set strict position size limits
- Test with small amounts first
- Have kill switches ready

---

## Disclaimer

This list is for educational purposes. Trading involves substantial risk. Many people lose money. Do your own research. Not financial advice.

---

## Contributing

Contributions welcome! Add repos with:
- GitHub URL
- Star count (if notable)
- Clear description
- How to monetize

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [BlockRun](https://blockrun.ai) has waived all copyright and related rights to this work.

---

<p align="center">
  <b>Money printer goes brrrr 🦞🖨️💵</b><br>
  <i>(but please manage your expectations)</i>
</p>
