# S/D Zones Premium v4.1 — Farhan FX

Multi-timeframe Supply & Demand zone indicator for TradingView (Pine Script v5), built and tuned for **XAUUSD (gold)**.

## Features
- **Multi-TF zones** — chart timeframe + H4 + Daily zones on one chart (HTF zones are labelled, e.g. `H4 SUPPLY`).
- **Non-repainting** — everything is evaluated on closed candles; higher-TF zones use only completed HTF bars.
- **Fresh zones only** — a zone disappears once it is touched/used; overlapping zones keep only the newest; very tall zones (> 1.5 ATR) are skipped.
- **BUY / SELL signals** — price touches a fresh zone, then a candle closes back outside it with its body in the trade direction, in line with the trend (EMA 200).
- **Trade plan** — Entry, SL (beyond the zone + 0.25 ATR), TP1 / TP2 / TP3 at 1R / 2R / 3R, SL to breakeven after TP1, SL to TP1 after TP2.
- **Live-only drawing** — only the running trade is drawn (marker + Entry/SL/TP lines); turn on *Show past signals (history)* to see old ones.
- **Compact dashboard** (bottom right) — trend, status (WAIT / LIVE), Entry, SL, TP1–3, backtest win rate and profit factor.
- **Alerts** — `alert()` messages include Entry, SL, TP1, TP2, TP3.

## Trend filter (auto)
- H1 and higher charts → EMA 200 of the chart timeframe
- Charts below H1 → EMA 200 on H4

## Backtest (FX:XAUUSD, Nov 2026, built-in, no spread/commission)
| Chart | Trades | Win rate (TP1 before SL) | Profit factor |
|---|---|---|---|
| H1 | 322 | 59.3% | 1.60 |
| M15 | 284 | 52.8% | 1.20 |

Recommended timeframe: **H1**. Past results do not guarantee future performance — test on a demo account first.

## Install
1. TradingView → Pine Editor → New indicator.
2. Paste the contents of `SDZ_Premium_v4.1.pine`.
3. Save and *Add to chart*.

## Bangla
এটা Farhan FX-এর Supply & Demand zone indicator। এটা multi-timeframe-এ কাজ করে (chart-এর timeframe, H4 আর Daily) এবং repaint করে না। Signal এলে Entry, SL আর TP1/TP2/TP3 সহ live দেখায়। H1 chart-এ ব্যবহার করুন, আর আগে demo account-এ test করে নিন।
