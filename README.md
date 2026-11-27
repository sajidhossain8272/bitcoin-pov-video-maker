# Bitcoin POV Video Maker

A single-file web tool that turns a **historical Bitcoin simulation** into a 9:16 "POV: You invested…" video for YouTube Shorts, Reels and TikTok. Open `index.html` in a modern browser. No install or build step.

> **This is a simulation, not a record of real investments.** Read the [Disclaimer](#disclaimer) before publishing anything made with it.

## How to use

1. Open `index.html` (double-click it, or use the GitHub Pages link if enabled). You need an internet connection.
2. Enter a **starting amount** (USD), a **start date** and an **end date** (UTC, default today).
3. *(Optional)* Tick **Also invest regularly**, then set an amount and an interval (every N days, weeks, months or years). Set the starting amount to `0` for a recurring-only plan.
4. Choose a **video length** and click **Generate video** to preview the animation. Use **Replay** to watch it again.
5. After generating, a **YouTube title, description and tags** panel appears. It is written from your values and dates and stays within YouTube's limits (title 100, description 5,000, tags 500 characters). Edit it, copy it, and keep the "simulation" wording.
6. Click **Export MP4**. The file is the selected length plus 1 second held on the final result. Keep the tab open while it renders.

## How the numbers work

- Prices are daily BTC/USD closes (UTC) from the [Coin Metrics Community API](https://docs.coinmetrics.io/), with CryptoCompare as a backup. If the end date is today, a live spot price (Coinbase, then Kraken, Binance or CoinGecko) is added as the last point.
- Each purchase is made at the first available price on or after its scheduled date. Value = coins held × price. Gain is measured against the total amount invested.
- Fees, taxes, spreads, slippage and inflation are **not** included. Real results would differ.
- Chart axes abbreviate large values (K, M, B). The final result is always shown in full.

## Disclaimer

- **Educational illustration only.** Results are hypothetical, calculated with hindsight, and not a prediction, recommendation or financial advice. Past performance does not indicate future results. Bitcoin is volatile and you can lose money.
- **Label it as a simulation.** If you publish a video, say clearly that it is a hypothetical or historical simulation, not your actual trades, balance or returns.
- **No guarantee of accuracy.** Data comes from third-party sources that can be delayed, wrong or unavailable. Verify anything important yourself.
- **Not responsible for misuse.** The authors are not responsible for how anyone uses this tool or its output, including anyone who presents simulated results as real, impersonates another person or brand, or misleads viewers.

## Acceptable use

Please don't use this tool to deceive, defraud or scam anyone, to promote get-rich-quick or "guaranteed returns" schemes, to impersonate people or organisations, or for any other unlawful or harmful purpose. Using it for personal, educational and commentary content, with clear labelling, is fair use of the tool in the spirit it was made.

This section is a request and a statement of intent. It is **not** an extra condition of the license, which remains plain MIT.

## License

[MIT](LICENSE) © 2026 Broke Innovation. Third-party data providers have their own terms of use.
