# Awesome OpenClaw Money Maker 🦞💰

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/BlockRunAI/awesome-OpenClaw-Money-Maker?style=social)](https://github.com/BlockRunAI/awesome-OpenClaw-Money-Maker)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

> A curated list of open-source tools and repos for making money with AI agents like [OpenClaw](https://github.com/openclaw/openclaw).

**Reality check:** These are potential earnings, not guarantees. Factor in API/token costs, time investment, and market competition.

---

## The Money Loop 🔄

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   💵 USDC ──► ClawRouter ──► LLM ──► OpenClaw ──► 💰 Profit │
│       ▲                                              │      │
│       └──────────────── reinvest ◄───────────────────┘      │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

1. **Fund your wallet** with USDC (on Base)
2. **OpenClaw uses [ClawRouter](https://github.com/BlockRunAI/ClawRouter)** to access 30+ LLMs
3. **Pay-per-request** via x402 micropayments - no API keys, no subscriptions
4. **Save up to 78%** on inference costs with smart model routing
5. **LLM executes tasks** that generate income
6. **Profit funds more usage** - creating a self-sustaining money loop

**Get started:** [ClawRouter v0.8.18](https://github.com/BlockRunAI/ClawRouter) | [BlockRun.ai](https://blockrun.ai)

### 🆕 ClawRouter v0.8.18 - Production Ready (Feb 2026)

Latest version with battle-tested features:

| Feature | Description |
|---------|-------------|
| **Agentic Momentum** | Proper `finish_reason: tool_calls` for multi-step autonomous workflows |
| **15-Dimension Routing** | Local scoring (<1ms) classifies prompts into SIMPLE/MEDIUM/COMPLEX/REASONING |
| **Smart Fallback Chains** | Auto-retry with next-best model on provider errors |
| **Context-Aware Routing** | Filters models by context size requirements |
| **Reasoning Model Support** | Handles `reasoning_content` for o3/DeepSeek-R1/Grok-reasoning |
| **Free Tier Fallback** | Falls back to nvidia/gpt-oss-120b when wallet is empty |
| **Rate Limit Awareness** | Deprioritizes rate-limited models automatically |

```bash
# Install via OpenClaw
openclaw plugins install @blockrun/clawrouter

# Or via npm
npm install @blockrun/clawrouter@latest

# Or standalone
curl -fsSL https://raw.githubusercontent.com/BlockRunAI/ClawRouter/main/scripts/reinstall.sh | bash
```

---

## Contents

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
- [Research & Analysis](#research--analysis)
- [Resources & Directories](#resources--directories)
- [Cost Considerations](#cost-considerations)
- [Security Warnings](#security-warnings)

---

## Trading Bots

### Crypto Trading

- [**Freqtrade**](https://github.com/freqtrade/freqtrade) ⭐ 46.5k - Free, open-source crypto trading bot. Supports all major exchanges (Binance, Hyperliquid, etc.). ML strategy optimization via FreqAI. Telegram control + WebUI.
  - 💰 **Monetize:** Sell custom strategies, run managed bot services, offer backtesting consulting

- [**Hummingbot**](https://github.com/hummingbot/hummingbot) ⭐ 15.9k - Open source market making and liquidity mining bot. Supports 40+ CEXs/DEXs. Customizable strategies in Python.
  - 💰 **Monetize:** Market making profits, liquidity mining rewards, strategy consulting

- [**FinRL**](https://github.com/AI4Finance-Foundation/FinRL) ⭐ 11.4k - Deep reinforcement learning for trading. Supports DQN, DDPG, A2C, SAC, PPO, TD3. Crypto environments with Binance API.
  - 💰 **Monetize:** Sell trained models, quant consulting, proprietary strategy development

- [**Jesse**](https://github.com/jesse-ai/jesse) ⭐ 7.4k - Advanced crypto trading bot in Python. Backtesting, paper trading, live trading. Built for algo traders.
  - 💰 **Monetize:** Sell strategies, subscription bot service, algo trading education

- [**Superalgos**](https://github.com/Superalgos/Superalgos) ⭐ 5.3k - Visual crypto trading bot builder. Drag-and-drop strategy design, backtesting, paper trading, multi-server deployments.
  - 💰 **Monetize:** Sell strategy templates, managed bot services, white-label platform

- [**OctoBot**](https://github.com/Drakkar-Software/OctoBot) ⭐ 5.2k - Open-source bot with AI, Grid, DCA, TradingView strategies. Simple interface, 15+ exchanges.
  - 💰 **Monetize:** Premium strategies, hosting service, configuration consulting

- [**OpenTrader**](https://github.com/Open-Trader/opentrader) ⭐ 2.2k - Open-source DCA & Grid trading bot with UI. Self-hosted, pro features unlocked.
  - 💰 **Monetize:** Managed service, custom strategy development, enterprise deployments

- [**Sibyl**](https://github.com/nMaroulis/sibyl) - AI-powered crypto trading dashboard. Oracle (LLM agent layer) + Chronos (LSTM/GTU price forecasting).
  - 💰 **Monetize:** Premium analysis tool, API access to signals, white-label for exchanges

### AI Trading Agents

- [**OpenBB**](https://github.com/OpenBB-finance/OpenBB) ⭐ 60k - Financial data platform for analysts, quants and AI agents. Open-source investment research terminal with AI copilot.
  - 💰 **Monetize:** Custom research tools, financial data SaaS, enterprise integrations, quant consulting

- [**GOAT SDK**](https://github.com/goat-sdk/goat) ⭐ 951 - The leading agentic finance toolkit for AI agents. Connect agents to DeFi protocols, wallets, and on-chain actions.
  - 💰 **Monetize:** Agent-powered trading bots, DeFi automation, on-chain agent services

- [**nof1.ai**](https://github.com/195440/nof1.ai) ⭐ 551 - Autonomous AI trading agent. Web-based interface with real-time market monitoring and AI-powered decision making.
  - 💰 **Monetize:** Managed trading service, strategy licensing, white-label solutions

- [**AI Trading Agent (Hyperliquid)**](https://github.com/Gajesh2007/ai-trading-agent) ⭐ 455 - AI trading agent built specifically for Hyperliquid perpetual DEX.
  - 💰 **Monetize:** Perp trading profits, signal service, managed accounts

- [**AgentTrade**](https://github.com/luffycodes/AgentTrade) - LLM-based trading system using technical analysis, news, and sentiment with reasoning.
  - 💰 **Monetize:** Signal service, managed accounts, SaaS platform

- [**TradingAgents**](https://github.com/TradingAgents-AI/TradingAgents) - Multi-agent trading framework with specialized analyst, researcher, and trader agents.
  - 💰 **Monetize:** Enterprise trading solutions, custom agent development

### Solana Trading

- [**Solana Trading Bot**](https://github.com/warp-id/solana-trading-bot) ⭐ 2.3k - Beta Solana trading bot. Sniper, swap, and automated trading.
  - 💰 **Monetize:** Token sniping profits, managed bot service, strategy development

- [**open-sol-bot**](https://github.com/ChainBuff/open-sol-bot) ⭐ 404 - Fully open-source Solana copy trading and auto-trading bot.
  - 💰 **Monetize:** Copy trading fees, managed accounts, bot licensing

- [**Solana Trading Bot (Raydium/Pump.fun)**](https://github.com/henrytirla/Solana-Trading-Bot) ⭐ 289 - Buy/sell SPL tokens on Raydium DEX and Pump.fun using Jito SDK.
  - 💰 **Monetize:** Token trading profits, sniping service, strategy consulting

- [**solana-grpc-sniper-bot**](https://github.com/0xRustPro/solana-grpc-sniper-bundler-bot) ⭐ 126 - High-speed Solana sniper using gRPC for real-time transaction streaming.
  - 💰 **Monetize:** New token sniping, managed sniper service, speed advantage

---

## MEV & Arbitrage

- [**Artemis**](https://github.com/paradigmxyz/artemis) ⭐ 2.9k - Simple, modular, fast MEV bot framework in Rust by Paradigm.
  - 💰 **Monetize:** Sandwich attacks, liquidations, arbitrage profits, MEV extraction

- [**Jito MEV Bot**](https://github.com/jito-labs/mev-bot) ⭐ 1.2k - Official Jito Labs MEV bot for Solana.
  - 💰 **Monetize:** Solana MEV extraction, liquidations, arbitrage

- [**mev-template-rs**](https://github.com/degatchi/mev-template-rs) ⭐ 727 - Bootstrap MEV bot strategies with Rust boilerplate.
  - 💰 **Monetize:** Build custom MEV strategies, consulting, bot-as-a-service

- [**Arbitrage MEV BOT**](https://github.com/sOLarFLaMEPyL/Arbitrage_Mev_BOT) ⭐ 613 - Contract for MEV: flash loans, arbitrage, liquidations. Ready to deploy and use.
  - 💰 **Monetize:** Deploy and run MEV strategies, consulting, bot customization

- [**mev-templates**](https://github.com/solidquant/mev-templates) ⭐ 567 - MEV templates in Python/Javascript/Rust. DEX flashloan arbitrage.
  - 💰 **Monetize:** Cross-DEX arbitrage, flashloan profits, strategy development

- [**Rust Solana MEV Bot**](https://github.com/SaoXuan/rust-mev-bot-shared) ⭐ 443 - Rust Solana MEV 套利机器人. High-performance arbitrage bot for Solana.
  - 💰 **Monetize:** Solana arbitrage, MEV extraction, bot licensing

- [**Loom**](https://github.com/dexloom/loom) ⭐ 331 - MEV Bot based on Alloy. Modern EVM MEV extraction.
  - 💰 **Monetize:** EVM MEV extraction, liquidations, arbitrage strategies

---

## Prediction Markets

### Polymarket Tools

- [**Polymarket Agents**](https://github.com/Polymarket/agents) ⭐ 2.2k - Official Polymarket AI agents. Trade autonomously using AI on prediction markets.
  - 💰 **Monetize:** Automated trading profits, agent customization services

- [**Prediction Market Analysis**](https://github.com/Jon-Becker/prediction-market-analysis) ⭐ 1.7k - Framework for collecting and analyzing prediction market data. Largest public dataset of Polymarket and Kalshi market/trade data.
  - 💰 **Monetize:** Data feeds, analytics API, research reports, trading signals

- [**poly-maker**](https://github.com/warproxxx/poly-maker) ⭐ 856 - Market making bot for Polymarket. Configurable via Google Sheets. Provides liquidity on both sides of the book.
  - 💰 **Monetize:** Market making spreads, managed MM services

- [**Polymarket Copy Trading Bot**](https://github.com/RandyTas/polymarket-copytrading-bot) ⭐ 822 - Copy trading bot for Polymarket. Follow successful traders automatically.
  - 💰 **Monetize:** Copy trading service, signal selling, managed accounts

- [**py-clob-client**](https://github.com/Polymarket/py-clob-client) ⭐ 785 - Official Python client for the Polymarket CLOB (Central Limit Order Book).
  - 💰 **Monetize:** Build custom trading bots, API services, consulting

- [**Polyseer**](https://github.com/yorkeccak/Polyseer) ⭐ 562 - Polymarket alpha at the speed of now. Real-time alerts and signals.
  - 💰 **Monetize:** Premium alerts, signal subscription, API access

- [**poly_data**](https://github.com/warproxxx/poly_data) ⭐ 512 - Polymarket data retriever. Fetches, processes markets, order events, and trades.
  - 💰 **Monetize:** Data feeds, analytics API, research reports

- [**pmxt**](https://github.com/pmxt-dev/pmxt) ⭐ 592 - Unified API for trading across prediction markets (Polymarket, Kalshi, etc.).
  - 💰 **Monetize:** Cross-platform arbitrage, multi-market bots, API service

- [**PolymarketBTC15mAssistant**](https://github.com/FrondEnt/PolymarketBTC15mAssistant) ⭐ 490 - Real-time Polymarket BTC 15m trading assistant for every trader.
  - 💰 **Monetize:** Trading signals, subscription service, managed trading

- [**Cross-Market State Fusion**](https://github.com/humanplane/cross-market-state-fusion) ⭐ 343 - RL agent fusing real-time Binance futures data into Polymarket prediction markets. On-device training with MLX on Apple Silicon.
  - 💰 **Monetize:** Cross-market signals, AI model licensing, trading service

- [**Polymarket Spike Bot**](https://github.com/Trust412/Polymarket-spike-bot-v1) ⭐ 310 - High-frequency Polymarket trading bot with real-time price monitoring, automated spike detection, and smart order execution.
  - 💰 **Monetize:** HFT profits, bot licensing, managed trading

### Arbitrage Bots

- [**polymarket-kalshi-btc-arbitrage-bot**](https://github.com/CarlosIbCu/polymarket-kalshi-btc-arbitrage-bot) - Real-time arbitrage between Polymarket and Kalshi on Bitcoin markets.
  - 💰 **Monetize:** Execute profitable arbs, sell signals/alerts

- [**prediction-market-arbitrage-bot**](https://github.com/realfishsam/prediction-market-arbitrage-bot) - Synthetic arbitrage (buy YES on one platform, NO on another).
  - 💰 **Monetize:** Arbitrage execution, managed arb service

### Resources

- [**Awesome-Prediction-Market-Tools**](https://github.com/aarora4/Awesome-Prediction-Market-Tools) - Curated list including YN Signals (24/7 alpha aggregator) and Eventarb (free arb alerts).

---

## DeFi & Yield Farming

- [**DeFi-Yield-AutoFarming**](https://github.com/therumpshakingaction/DeFi-Yield-AutoFarming) - Automated yield farming with auto-reinvestment, pool optimization, risk management.
  - 💰 **Monetize:** Take % of returns, subscription access, manage client portfolios

- [**yield-farmers-almanac**](https://github.com/corbinpage/yield-farmers-almanac) - Community-sourced DeFi yield farming opportunities database.
  - 💰 **Monetize:** Premium data feeds, analysis reports, tools built on top

### OpenClaw DeFi Skills

- [**BankrBot/openclaw-skills**](https://github.com/BankrBot/openclaw-skills) - OpenClaw skills for Polymarket betting, crypto trading, DeFi operations, leverage trading, portfolio management. Multi-chain: Base, Ethereum, Polygon, Solana.
  - 💰 **Monetize:** Sell skills on ClawHub, partner with exchanges for affiliate volume

---

## Airdrop Farming

- [**MasterCryptoFarmBot**](https://github.com/masterking32/MasterCryptoFarmBot) ⭐ 232 - Foundation for building crypto farming and airdrop bots for Telegram-based games.
  - 💰 **Monetize:** Airdrop farming profits, sell bot access, multi-account management

- [**Telegram-Airdrop-Bot**](https://github.com/fabston/Telegram-Airdrop-Bot) ⭐ 211 - Manage Telegram airdrops on ERC-20, BEP-20 tokens.
  - 💰 **Monetize:** Run airdrop campaigns, token distribution service

- [**t3rn-airdrop-bot**](https://github.com/dante4rt/t3rn-airdrop-bot) ⭐ 208 - Automate transactions and bridging on t3rn network for airdrop farming.
  - 💰 **Monetize:** Airdrop farming, multi-wallet management, bridge fee farming

- [**blum-airdrop-bot**](https://github.com/dante4rt/blum-airdrop-bot) ⭐ 137 - Automate Blum airdrop: claim rewards, manage farming, complete tasks, play games.
  - 💰 **Monetize:** Blum token farming, managed farming service

- [**nodepay-airdrop-bot**](https://github.com/dante4rt/nodepay-airdrop-bot) ⭐ 110 - Automate Nodepay airdrop with session management and proxy support.
  - 💰 **Monetize:** Nodepay token farming, bandwidth monetization

- [**polyflow-airdrop-bot**](https://github.com/dante4rt/polyflow-airdrop-bot) ⭐ 105 - Farm Scan2Earn points on PolyFlow by auto-uploading invoices.
  - 💰 **Monetize:** PolyFlow points farming, invoice submission automation

---

## Lead Generation & Sales

### LinkedIn Automation

- [**OpenOutreach**](https://github.com/eracle/OpenOutreach) ⭐ 1.1k - LinkedIn automation: visit profiles, connect, message with AI.
  - 💰 **Monetize:** B2B lead gen, outreach agency, connection building service

- [**linvo-scraper**](https://github.com/linvo-io/linvo-scraper) ⭐ 625 - LinkedIn automation with comprehensive scraping. Production-grade.
  - 💰 **Monetize:** Lead scraping service, data enrichment, profile export

### Lead Generation

- [**ScrapeGraphAI**](https://github.com/ScrapeGraphAI/Scrapegraph-ai) ⭐ 22.6k - Python scraper based on AI. Uses LLMs to understand and extract structured data from any website.
  - 💰 **Monetize:** Intelligent scraping SaaS, data extraction services, lead enrichment platform

- [**ai-lead-generator**](https://github.com/brightdata/ai-lead-generator) - AI-powered lead gen using Bright Data scraping + OpenAI for qualification/enrichment. Streamlit UI with instant lead scoring.
  - 💰 **Monetize:** Sell lead lists, B2B SaaS subscription, charge per lead

- [**ai-web-scraper**](https://github.com/kaymen99/ai-web-scraper) - AI web scraper using Crawl4AI. Supports GPT-4o, Claude, DeepSeek, Gemini via LiteLLM.
  - 💰 **Monetize:** Scraping service, subscription tiers, white-label tool

- [**SalesGPT**](https://github.com/filip-michalsky/SalesGPT) ⭐ 2.2k+ - Context-aware AI sales agent for voice, email, SMS. Autonomous across sales funnel stages.
  - 💰 **Monetize:** Outbound sales automation, enterprise SDR replacement, subscription campaigns

- [**Google-Maps-Scraper**](https://github.com/omkarcloud/google-maps-scraper) ⭐ 1.4k - Bulk scrape Google Maps (names, addresses, phones, emails, ratings).
  - 💰 **Monetize:** Sell local business leads, B2B contact databases

- [**ChatGPT Scraper**](https://github.com/oxylabs/chatgpt-scraper) ⭐ 2.7k - Collect ChatGPT responses via Web Scraper API. Automated prompt responses.
  - 💰 **Monetize:** AI response aggregation, research automation, data collection service

---

## Content Creation

- [**MoneyPrinterTurbo**](https://github.com/harry0703/MoneyPrinterTurbo) ⭐ 44k - AI one-click HD short video generation.
  - 💰 **Monetize:** YouTube/TikTok monetization, affiliate marketing, video ads

- [**MoneyPrinterV2**](https://github.com/FujiwaraChoki/MoneyPrinterV2) ⭐ 13k - Automate the process of making money online. Full automation pipeline for content creation and publishing.
  - 💰 **Monetize:** Faceless channels, automated content farms, video-as-a-service

- [**CogVideo**](https://github.com/THUDM/CogVideo) ⭐ 12k - Text/image to video generation.
  - 💰 **Monetize:** Content creation, ads, social media, video SaaS

- [**SoraFM**](https://github.com/all-in-aigc/sorafm) ⭐ 1.1k - Sora AI Video Generator web interface. Generate videos with OpenAI Sora API.
  - 💰 **Monetize:** Video generation service, SaaS platform, API reselling

- [**AI Video Generator Agent**](https://github.com/davide97l/ai-video-generator) ⭐ 126 - AI agent that automatically generates and posts short videos. Full automation pipeline.
  - 💰 **Monetize:** Faceless channel automation, content agency, video-as-a-service

### YouTube Automation

- [**gemini-youtube-automation**](https://github.com/ChaituRajSagar/gemini-youtube-automation) ⭐ 219 - Fully autonomous AI pipeline using Gemini to generate and upload educational videos to YouTube.
  - 💰 **Monetize:** Educational channel monetization, faceless channels, course promotion

- [**youtube-automation-agent**](https://github.com/darkzOGx/youtube-automation-agent) ⭐ 49 - Fully automated YouTube channel with AI agents. Creates, optimizes, publishes 24/7. Works with free Gemini API.
  - 💰 **Monetize:** Ad revenue, affiliate marketing, brand deals

### Social Media Automation

- [**Auto_Social_Media_Content_Generator**](https://github.com/PatrykIA/Auto_Social_Media_Content_Generator) - Automation for Facebook, Instagram, X, LinkedIn with AI text + Canva images. Auto-posts every 2 days.
  - 💰 **Monetize:** SaaS subscription, agency white-label, manage client accounts

- [**ALwrity**](https://github.com/AJaySi/ALwrity) - AI Digital Marketing Platform with RAG, SEO, multilingual. Blog Writer (Research→Outline→Content→SEO→Publish).
  - 💰 **Monetize:** Monthly SaaS, per-article pricing, agency white-label

---

## AI Agent Frameworks

Build monetizable AI agents with these frameworks:

### General Agent Frameworks

- [**Awesome LLM Apps**](https://github.com/Shubhamsaboo/awesome-llm-apps) ⭐ 95.4k - Collection of awesome LLM apps with AI Agents and RAG using OpenAI, Anthropic, Gemini, and open-source models.
  - 💰 **Monetize:** Clone and customize apps, build SaaS products, consulting services

- [**Gemini CLI**](https://github.com/google-gemini/gemini-cli) ⭐ 94.6k - Google's open-source AI agent that brings the power of Gemini directly into your terminal.
  - 💰 **Monetize:** Automation scripts, developer tools, enterprise integrations

- [**AutoGPT**](https://github.com/Significant-Gravitas/AutoGPT) ⭐ 177k - Accessible AI tools for building autonomous agents. Forge for agent creation, benchmarks, leaderboard.
  - 💰 **Monetize:** Build/sell custom agents, agent-as-a-service, enterprise licensing

- [**MetaGPT**](https://github.com/geekan/MetaGPT) ⭐ 64k - The Multi-Agent Framework: First AI Software Company. Assigns roles to agents (Product Manager, Architect, Engineer).
  - 💰 **Monetize:** AI software development agency, code generation SaaS, enterprise consulting

- [**Open Interpreter**](https://github.com/openinterpreter/open-interpreter) ⭐ 62k - A natural language interface for computers. Run code, control your computer with plain English.
  - 💰 **Monetize:** Automation services, enterprise deployments, managed computer-use agents

- [**Anything LLM**](https://github.com/Mintplex-Labs/anything-llm) ⭐ 54.6k - All-in-one Desktop & Docker AI application with built-in RAG, AI agents, no-code agent builder, MCP compatibility.
  - 💰 **Monetize:** Custom deployments, enterprise hosting, white-label platform

- [**Microsoft Autogen**](https://github.com/microsoft/autogen) ⭐ 54.5k - A programming framework for agentic AI. Multi-agent conversations, tool use, code execution.
  - 💰 **Monetize:** Enterprise agent solutions, consulting, custom multi-agent systems

- [**AI Agents for Beginners**](https://github.com/microsoft/ai-agents-for-beginners) ⭐ 50.6k - Microsoft's 12 lessons to get started building AI agents. Comprehensive curriculum.
  - 💰 **Monetize:** Training courses, bootcamps, enterprise workshops

- [**Flowise**](https://github.com/FlowiseAI/Flowise) ⭐ 49.1k - Build AI Agents visually. Drag-and-drop LLM flow builder with API endpoints.
  - 💰 **Monetize:** Custom workflow development, managed hosting, enterprise deployments

- [**Mem0**](https://github.com/mem0ai/mem0) ⭐ 47.4k - Universal memory layer for AI Agents. Persistent memory across sessions.
  - 💰 **Monetize:** Memory-as-a-service, enterprise integrations, custom implementations

- [**CrewAI**](https://github.com/crewAIInc/crewAI) ⭐ 44.2k - Lean, fast Python framework for orchestrating role-playing AI agents with collaborative intelligence.
  - 💰 **Monetize:** Niche agents, consulting, pre-built templates, managed hosting

- [**ToolJet**](https://github.com/ToolJet/ToolJet) ⭐ 37.4k - Open-source foundation of ToolJet AI - AI-native platform for building internal tools, dashboards, workflows and AI agents.
  - 💰 **Monetize:** Internal tool development, enterprise licensing, custom integrations

- [**AgentGPT**](https://github.com/reworkd/AgentGPT) ⭐ 35.7k - Assemble, configure, and deploy autonomous AI Agents in your browser.
  - 💰 **Monetize:** Custom agent development, SaaS platform, enterprise deployments

- [**Block Goose**](https://github.com/block/goose) ⭐ 30.5k - Open source, extensible AI agent that goes beyond code suggestions - install, execute, edit, and test with any LLM.
  - 💰 **Monetize:** Development automation, custom extensions, enterprise licensing

- [**LangChain**](https://github.com/langchain-ai/langchain) ⭐ 112k - Framework for context-aware reasoning applications.
  - 💰 **Monetize:** LLM apps with monetized endpoints, consulting, templates

- [**LlamaIndex**](https://github.com/run-llama/llama_index) ⭐ 43k - Data-centric agents with RAG primitives. 500+ connectors via LlamaHub.
  - 💰 **Monetize:** Data-powered AI agents, specialized apps, consulting

- [**smolagents**](https://github.com/huggingface/smolagents) ⭐ 25.4k - HuggingFace's barebones library for agents that think in code. Simple, hackable, powerful.
  - 💰 **Monetize:** Custom coding agents, agent templates, enterprise integrations

- [**SuperAGI**](https://github.com/TransformerOptimus/SuperAGI) ⭐ 17.2k - Dev-first open source autonomous AI agent framework. Build, manage & run useful agents quickly.
  - 💰 **Monetize:** Custom agent development, managed infrastructure, enterprise licensing

- [**Jobs Applier AI Agent (AIHawk)**](https://github.com/feder-cr/Jobs_Applier_AI_Agent_AIHawk) ⭐ 29.3k - AI agent that automates job hunt by applying to multiple jobs in a tailored way.
  - 💰 **Monetize:** Job application service, subscription platform, career coaching integration

- [**UI-TARS Desktop**](https://github.com/bytedance/UI-TARS-desktop) ⭐ 28k - ByteDance's open-source multimodal AI agent stack connecting AI models and agent infra.
  - 💰 **Monetize:** Desktop automation, enterprise deployments, custom integrations

- [**Composio**](https://github.com/ComposioHQ/composio) ⭐ 26.6k - Equips AI agents & LLMs with 100+ high-quality integrations via function calling.
  - 💰 **Monetize:** Integration platform, custom connectors, enterprise licensing

- [**Sim Studio**](https://github.com/simstudioai/sim) ⭐ 26.4k - Open-source platform to build and deploy AI agent workflows.
  - 💰 **Monetize:** Workflow templates, managed hosting, enterprise solutions

- [**Warp**](https://github.com/warpdotdev/Warp) ⭐ 25.9k - The agentic development environment, built for coding with multiple AI agents.
  - 💰 **Monetize:** Developer tool licensing, enterprise features, custom integrations

- [**Graphiti**](https://github.com/getzep/graphiti) ⭐ 22.8k - Build real-time knowledge graphs for AI agents. Persistent structured memory.
  - 💰 **Monetize:** Knowledge graph services, enterprise memory solutions, consulting

- [**Roo Code**](https://github.com/RooCodeInc/Roo-Code) ⭐ 22.2k - A whole dev team of AI agents in your code editor.
  - 💰 **Monetize:** Enterprise licensing, custom agent development, training

- [**Activepieces**](https://github.com/activepieces/activepieces) ⭐ 20.8k - AI Agents & MCPs & AI Workflow Automation with ~400 MCP servers for AI agents.
  - 💰 **Monetize:** Workflow marketplace, managed hosting, enterprise integrations

- [**GenAI Agents**](https://github.com/NirDiamant/GenAI_Agents) ⭐ 20k - In-depth tutorials and implementations for various Generative AI Agent techniques.
  - 💰 **Monetize:** Training courses, enterprise workshops, consulting

- [**Coze Studio**](https://github.com/coze-dev/coze-studio) ⭐ 19.9k - AI agent development platform with all-in-one visual tools for creation, debugging, and deployment.
  - 💰 **Monetize:** Agent marketplace, managed platform, enterprise features

- [**Suna (Kortix)**](https://github.com/kortix-ai/suna) ⭐ 19.4k - Build, manage and train AI Agents with Kortix platform.
  - 💰 **Monetize:** Agent training services, managed platform, enterprise licensing

- [**Qwen Code**](https://github.com/QwenLM/qwen-code) ⭐ 18.4k - Open-source AI agent that lives in your terminal, powered by Qwen.
  - 💰 **Monetize:** Developer automation, enterprise licensing, custom extensions

- [**Eliza**](https://github.com/elizaOS/eliza) ⭐ 17.5k - Autonomous agents for everyone. Popular framework for crypto/social media agents. Multi-platform (Discord, Twitter, Telegram).
  - 💰 **Monetize:** Social media agents, crypto trading bots, community management agents

- [**Qwen-Agent**](https://github.com/QwenLM/Qwen-Agent) ⭐ 13.2k - Agent framework built on Qwen. Features Function Calling, MCP, Code Interpreter, RAG, Chrome extension.
  - 💰 **Monetize:** Qwen-powered apps, MCP integrations, browser extensions

- [**VoltAgent**](https://github.com/VoltAgent/voltagent) ⭐ 5.7k - AI Agent Engineering Platform built on TypeScript. Production-ready agent orchestration.
  - 💰 **Monetize:** Agent templates, platform licensing, consulting services

- [**PraisonAI**](https://github.com/MervinPraison/PraisonAI) ⭐ 5.6k - Production-ready Multi AI Agents framework. Low-code solution for building and managing multi-agent LLM systems.
  - 💰 **Monetize:** Pre-built agent teams, custom workflows, managed deployments

- [**AgentOps**](https://github.com/AgentOps-AI/agentops) ⭐ 5.3k - Python SDK for AI agent monitoring, LLM cost tracking, benchmarking. Integrates with CrewAI, Langchain, Autogen.
  - 💰 **Monetize:** Agent observability platform, enterprise monitoring, cost optimization consulting

- [**CrewAI**](https://github.com/crewAIInc/crewAI) - Lean, fast Python framework for orchestrating role-playing AI agents with collaborative intelligence.
  - 💰 **Monetize:** Niche agents, consulting, pre-built templates, managed hosting

- [**Pydantic-AI**](https://github.com/pydantic/pydantic-ai) - GenAI Agent Framework with validation layer for OpenAI, Anthropic, Google SDKs.
  - 💰 **Monetize:** Validated agent applications, development services

### Browser Automation Agents

- [**browser-use**](https://github.com/browser-use/browser-use) ⭐ 78.1k - Make websites accessible for AI agents. Automate any web task with natural language.
  - 💰 **Monetize:** Web automation services, form filling bots, data extraction, testing automation

- [**Stagehand**](https://github.com/browserbase/stagehand) ⭐ 21k - The AI Browser Automation Framework. Built on Playwright with AI-powered element selection.
  - 💰 **Monetize:** Web scraping services, testing automation, browser-based RPA

- [**Skyvern**](https://github.com/Skyvern-AI/skyvern) ⭐ 20.4k - Automate browser-based workflows with AI. Computer vision + LLM for robust web automation.
  - 💰 **Monetize:** Enterprise browser automation, form filling services, web RPA

- [**LaVague**](https://github.com/lavague-ai/LaVague) ⭐ 6.3k - Large Action Model framework to develop AI Web Agents. Natural language to browser actions.
  - 💰 **Monetize:** Web automation platform, custom browser agents, enterprise deployments

- [**ShowUI**](https://github.com/showlab/ShowUI) ⭐ 1.7k - Vision-Language-Action model for GUI Agent & Computer Use. CVPR 2025 paper implementation.
  - 💰 **Monetize:** Desktop automation, GUI testing, accessibility services

---

## OpenClaw Skills

- [**BankrBot/openclaw-skills**](https://github.com/BankrBot/openclaw-skills) - Polymarket, crypto trading, DeFi, leverage, portfolio management, NFTs. Multi-chain support.

- [**VoltAgent/awesome-openclaw-skills**](https://github.com/VoltAgent/awesome-openclaw-skills) ⭐ 4.5k - Curated collection of OpenClaw skills and integrations.

- [**openclaw/clawhub**](https://github.com/openclaw/clawhub) ⭐ 1.4k - Official skill directory and marketplace.

- [**ClawdTalk**](https://github.com/team-telnyx/clawdtalk-client) ⭐ - Phone calling and SMS for OpenClaw via Telnyx. AI agents can make/receive calls and SMS with calendar, Jira, and web search integration.
  - 💰 **Monetize:** AI voice agent service, automated customer support lines, appointment reminder callbacks

---

## Workflow Automation

- [**n8n-workflow-builder**](https://github.com/makafeli/n8n-workflow-builder) ⭐ 479 - AI assistant for n8n via MCP. Connect Claude, ChatGPT to n8n for natural language workflow management.
  - 💰 **Monetize:** Custom workflow development, automation consulting, managed n8n hosting

- [**n8n-skills**](https://github.com/haunchen/n8n-skills) ⭐ 188 - n8n Workflow Automation Skills Suite designed for AI assistants. Ready-to-use workflow templates.
  - 💰 **Monetize:** Skill marketplace, automation courses, enterprise deployments

- [**N8N-Workflows**](https://github.com/DINAKAR-S/N8N-Workflows) - Real-world n8n automation for lead gen, AI agents, web scraping, social media.
  - 💰 **Monetize:** Sell workflow templates, automation consulting, monthly management

- [**n8n-ai-automations**](https://github.com/lucaswalter/n8n-ai-automations) - Advanced workflows: law firm lead gen, competitor UGC analysis, personalized outreach.
  - 💰 **Monetize:** Niche workflow packages, agency white-label, training

- [**ai-automation-jsons**](https://github.com/simealdana/ai-automation-jsons) - Collection of n8n workflow JSONs for AI agents, integrations, automated processes. Ready-to-import.
  - 💰 **Monetize:** Workflow marketplace, custom development, automation agency

---

## Research & Analysis

- [**GPT Researcher**](https://github.com/assafelovic/gpt-researcher) ⭐ 25.3k - Autonomous agent that conducts deep research on any topic. Generates comprehensive reports from multiple sources.
  - 💰 **Monetize:** Research-as-a-service, market analysis reports, competitive intelligence, due diligence automation

---

## Resources & Directories

### Awesome Lists

- [**e2b-dev/awesome-ai-agents**](https://github.com/e2b-dev/awesome-ai-agents) ⭐ 25.7k - Comprehensive list of AI autonomous agents. Well-maintained with categories.

- [**500-AI-Agents-Projects**](https://github.com/ashishpatel26/500-AI-Agents-Projects) - Curated AI agent use cases across industries (healthcare, finance, education, retail).

- [**awesome-ai-agents**](https://github.com/slavakurilyak/awesome-ai-agents) - 300+ agentic AI resources.

- [**awesome_ai_agents**](https://github.com/jim-schwoebel/awesome_ai_agents) - 1,500+ AI agent resources and tools.

- [**MakeMoneyWithAI**](https://github.com/garylab/MakeMoneyWithAI) - Curated list of open-source AI projects for generating income.

- [**AI-Agent-Platforms-Automation-Tools**](https://github.com/rembertdesigns/AI-Agent-Platforms-Automation-Tools) - Directory of autonomous AI agents, frameworks, platforms.

### Infrastructure

- [**ClawRouter v0.8.18**](https://github.com/BlockRunAI/ClawRouter) - Smart LLM router, save 78-96% on inference. 30+ models, one USDC wallet. **Features:** Agentic momentum, 15-dimension routing, smart fallbacks, reasoning model support.
- [**BlockRun.ai**](https://blockrun.ai) - Pay-per-request AI via x402 micropayments.

#### Popular Models on BlockRun (Feb 2026)

| Model | Usage Share | Best For |
|-------|-------------|----------|
| Grok Code Fast | 42% | Fast coding, analysis |
| Grok-4 Reasoning | 20% | Complex reasoning tasks |
| Claude Sonnet 4 | 12% | Coding, agentic workflows |
| Gemini 2.5 Pro | 8% | Long context, multimodal |
| DeepSeek Chat | 6% | General chat, affordable |
| OpenAI o3 | 4% | Advanced reasoning |

### Data & Trading

- [DeFiLlama](https://defillama.com/) - TVL and yield data
- [Dune Analytics](https://dune.com/) - On-chain data
- [Binance API Docs](https://binance-docs.github.io/apidocs/)

---

## Cost Considerations

| Cost | Traditional | With ClawRouter v0.8+ |
|------|-------------|----------------------|
| LLM API tokens | $50 - $500+/mo | $15 - $150+/mo |
| Hosting | $5 - $50/mo | $5 - $50/mo |
| Data APIs | $0 - $200/mo | $0 - $200/mo |
| **Break-even** | **~$220/month** | **~$115/month** |

**Pro tip:** Use DeepSeek models for 90%+ cost savings vs GPT-4. Route to Grok-3 only when you need real-time X data.

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
