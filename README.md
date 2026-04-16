# Market Pulse Wingman

View on Clawhub: https://clawhub.ai/yaelsprikut/market-pulse-wingman

Market risk co-pilot for equities — fast, disciplined scans of a watchlist that blend technical context, headline/risk sweeps, and a concise trading log entry.

## What this Skill does
- Scans one or more tickers and returns a compact per-ticker read: price snapshot, trend bias, volatility context, near-term catalysts, headline/security risk flags, and a short bot recommendation.
- Produces a ready-to-save decision log entry for the user's self-improvement tracker.

## Quick start
1. Provide a watchlist or one-or-more tickers (optionally include position size, time horizon, or risk tolerance).
2. Optionally paste any price/headline context you already have; otherwise the skill will proceed using publicly known info and explicit assumptions.
3. The skill outputs a compact section per ticker and a fillable log template.

## Workflow (per ticker)
1. Baseline snapshot: price, daily % change, volume vs avg, ATR/vol context, earnings/macro catalysts, simple trend bias (e.g., relation to 21/50 EMA).
2. Risk & headline sweep: summarize recent headlines, tag severity (⚠️/🚨), cite source + timestamp.
3. Bot recommendation: a short action nudge (trim, add on pullback, stand aside) and a clear invalidation contingency.
4. Decision log: a short, copyable entry for the user's tracker with date, bot take, planned action, and follow-up reminder.

## Output example
```
## Market Pulse — 2026-04-16

### Ticker: XYZ
- Price: $123.45 (+1.8% / vol 1.3× avg) | Earnings: Apr 19 | ATR: 3.2
- Setup: Uptrend holding 21EMA; buyers defending $120 gap.
- Risk flags: 🚨 Data breach rumor (TechCrunch, 4h ago) + class-action chatter.
- Bot take: Trim to core until breach story is confirmed; re-add only above $126 on volume.
- Log: (prefill template for user)
```

## Data & tooling notes
- If live APIs aren't available, the skill relies on user-provided data and public facts (earnings calendar, macro events). Always state assumptions used.
- Headlines should be cited by source + time; when in doubt, prompt the user for confirmation before acting on allegations.

## Examples of prompts to use
- "Scan AAPL, MSFT for today — suggest sizing + short log entries."
- "I hold 200 shares of XYZ; summarize technicals and check for any security/ops headlines." 

## Contributing
If you want to extend templates, add API connectors, or change the log schema, update the `references/` folder and revise the workflow examples in `SKILL.md`.

## License
Use and modify as you wish; please keep attributions when sharing improvements.
