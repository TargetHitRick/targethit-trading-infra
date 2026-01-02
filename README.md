# TargetHit Trading Infrastructure

Open-source trading execution infrastructure for [TargetHit.ai](https://targethit.ai) - an AI-powered crypto trading signals platform.

## 🎯 What This Repo Contains

This repository contains the **execution layer** of TargetHit - the code that opens and closes trades on exchanges. We're open-sourcing this to allow community contributions for bug fixes and improvements.

### Components

| Component | Description | Status |
|-----------|-------------|--------|
| **Exchange Adapters** | Connect to Binance, Bitget, BYDFI, HyperLiquid, Bybit, MEXC, OKX | 🔧 Active |
| **Auto-Trade Worker** | Opens positions when signals fire | 🔧 Active |
| **Auto-Close Worker** | Closes positions at signal expiration | 🔧 Active |

## 🚀 How to Contribute

We welcome bug fixes and improvements! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Common Issues We Need Help With

- Exchange API edge cases (hedge mode vs one-way mode)
- Position precision/quantity formatting per exchange
- Error handling for rate limits and timeouts
- Partial close logic for stacked positions

### Reporting Bugs

Found a bug? [Open an issue](../../issues/new?template=bug_report.md) with:
- Which exchange/component
- Expected vs actual behavior
- Relevant logs

## 📁 Repository Structure
```
├── adapters/           # Exchange-specific adapters
│   ├── binance.mjs
│   ├── bitget.mjs
│   ├── bydfi.mjs
│   ├── hyperliquid.mjs
│   ├── bybit.mjs
│   ├── mexc.mjs
│   └── okx.mjs
├── workers/
│   ├── autotrade-worker.py
│   └── autoclose-worker.py
└── docs/
    └── ARCHITECTURE.md
```

## ⚠️ What's NOT in This Repo

The signal generation, edge discovery, and AI components are proprietary and not included here. This repo only contains the trade execution infrastructure.

## 📜 License

MIT License - see [LICENSE](LICENSE)

## 🔗 Links

- **Website**: [targethit.ai](https://targethit.ai)
- **YouTube**: [TargetHit Stream](https://youtube.com/@targethit) (166K subscribers, 9 years of trading)
- **Discord**: [Discord](https://discord.gg/RPdypMVr)

---

Built with ❤️ by the TargetHit team
