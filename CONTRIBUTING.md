# Contributing to TargetHit Trading Infrastructure

Thank you for your interest in contributing! This guide will help you get started.

## 🐛 Reporting Bugs

1. Check [existing issues](../../issues) to avoid duplicates
2. Use the [bug report template](../../issues/new?template=bug_report.md)
3. Include:
   - Which exchange/component
   - Expected vs actual behavior
   - Relevant log output
   - Your exchange account mode (hedge/one-way)

## 🔧 Submitting Fixes

### Before You Start

1. **Fork** this repository
2. **Clone** your fork locally
3. Create a **branch** for your fix: `git checkout -b fix/binance-precision`

### Code Guidelines

- Keep changes focused - one fix per PR
- Test with real exchange sandbox/testnet if possible
- Include relevant log output showing the fix works
- Update comments if behavior changes

### Exchange Adapter Standards

Each adapter must implement:
```javascript
// Required methods
async getBalance(credentials)      // Returns { total, available }
async openPosition(credentials, params)  // Returns { orderId, price, quantity }
async closePosition(credentials, params) // Returns { orderId, price, quantity }
async getPosition(credentials, coin)     // Returns position or null
```

### Pull Request Process

1. Push your branch to your fork
2. Open a PR against `main`
3. Describe what the fix does and why
4. Link related issues (e.g., "Fixes #123")
5. Wait for review

## 💬 Questions?

- Open a [Discussion](../../discussions) for questions
- Tag `@TargetHitRick` for urgent issues

## 📋 Priority Areas

We especially need help with:

1. **Binance** - Hedge mode vs one-way mode handling
2. **Position precision** - Different exchanges have different decimal requirements
3. **Error handling** - Rate limits, timeouts, network errors
4. **Partial closes** - Closing specific quantities vs entire positions

Thank you for helping make TargetHit better! 🎯
