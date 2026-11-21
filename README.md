# Crypto Futures Fee Tiers, Funding Intervals & Withdrawal Specs

Machine-readable reference dataset (`CSV` and `JSON`) capturing published VIP0–VIP8 futures & spot maker/taker fee brackets, perpetual funding settlement intervals, contract pair leverage specs, and blockchain network withdrawal fees read from public Bitunix documentation and APIs on **21 November 2026**.

> **Disclosure:** This page is created and managed by an independent affiliate and is not an official Bitunix website or communication channel. Crypto futures are high-risk and leveraged: you can lose more than your deposit. 18+ only. Not available in restricted regions.

---

## Dataset Files

- [`data/vip-tier-fee-schedule.csv`](data/vip-tier-fee-schedule.csv) — VIP0 through VIP8 spot & futures maker/taker rates alongside 30-day spot volume, 30-day futures volume, and USDT balance thresholds.
- [`data/vip-tier-fee-schedule.json`](data/vip-tier-fee-schedule.json) — Same VIP0–VIP8 table with source metadata, read date (`2026-11-21`), and VIP0-to-VIP3 percentage differences (`30%` futures maker, `33%` futures taker, `56%` spot maker, `40%` spot taker).
- [`data/perp-funding-and-withdrawals.json`](data/perp-funding-and-withdrawals.json) — Snapshot of `807` futures pairs (`200x` down to `20x` leverage breakdown), `944` perpetual funding schedule entries (`532` at `4h`, `399` at `8h`, `11` at `1h`, `2` at `2h`), and published USDT/USDC/BTC/ETH/SOL/XRP withdrawal fees (`0.04 USDT` Aptos, `0.3 USDT` opBNB, `0.5 USDT` BEP-20, `1 USDT` TRC-20/SOL/ARB/Polygon/BASE/AVAX, `2 USDT` ERC-20).

---

## Summary Table: Futures & Spot VIP0–VIP8 (Read 21 November 2026)

| Tier | Futures Maker | Futures Taker | Spot Maker | Spot Taker | 30d Futures Vol (USDT) | 30d Spot Vol (USDT) | Balance (USDT) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| VIP0 | 0.02% | 0.06% | 0.08% | 0.10% | 0 | 0 | 0 |
| VIP1 | 0.02% | 0.05% | 0.07% | 0.09% | 1,000,000 | 100,000 | 300 |
| VIP2 | 0.016% | 0.05% | 0.06% | 0.08% | 5,000,000 | 500,000 | 5,000 |
| VIP3 | 0.014% | 0.04% | 0.035% | 0.06% | 8,000,000 | 800,000 | 25,000 |
| VIP4 | 0.012% | 0.0375% | 0.02% | 0.05% | 20,000,000 | 2,000,000 | 140,000 |
| VIP5 | 0.01% | 0.035% | 0.015% | 0.045% | 50,000,000 | 4,000,000 | 700,000 |
| VIP6 | 0.008% | 0.0315% | 0.0125% | 0.0375% | 100,000,000 | 6,000,000 | 1,400,000 |
| VIP7 | 0.006% | 0.03% | 0.01% | 0.0325% | 200,000,000 | 8,000,000 | 2,400,000 |
| VIP8 | 0% | 0.026% | 0.0048% | 0.018% | 500,000,000 | 100,000,000 | — |

---

## Interactive Browser Calculators & MCP Endpoint

Maintained alongside ProEA Lab's free browser tools:

- **Futures Fee & VIP3 Calculator (Code `PROEA`):** https://proea.app/en/tools/bitunix-referral-code *(Bitunix's Head of BD wrote to ProEA on 17 November 2026 that Bitunix can open a VIP3 event for PROEA users, with terms set by Bitunix; invitation code must be entered at sign-up and cannot be changed after registration; restricted regions, UK, and Thailand excluded.)*
- **VIP0–VIP8 Tier Calculator:** https://proea.app/en/tools/crypto-vip-fee-tier-calculator
- **Fixed-Risk Position Size Calculator (With Taker Fees):** https://proea.app/en/tools/fixed-risk-position-size-calculator
- **TradingView Super Alert Notification Checklist:** https://proea.app/en/tools/super-alert-tradingview-setup
- **Regional Restrictions & Network Fee Checker:** https://proea.app/en/tools/crypto-exchange-country-checker
- **Read-Only MCP Server Docs (`crypto_fixed_risk_size`):** https://proea.app/en/mcp (`https://proea.app/api/mcp`)

### Technical Guides
- https://proea.app/en/blog/crypto-futures-trading-fees-explained
- https://proea.app/en/blog/tradingview-alerts-to-crypto-exchange-webhooks
- https://proea.app/en/blog/fixed-risk-position-sizing-crypto-futures
- https://proea.app/en/blog/crypto-perpetual-funding-rates-and-withdrawal-costs
