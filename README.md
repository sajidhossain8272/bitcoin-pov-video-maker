# POV Investing Video Maker

A web tool that turns a **historical investing simulation** (Bitcoin, the top ~100 coins, or Nasdaq-100 stocks) into a 9:16 "POV: You invested…" video for YouTube Shorts, Reels and TikTok. Open `index.html` in a modern browser. Keep `logos.js` in the same folder (it holds the coin and company logos). No install or build step.

> **This is a simulation, not a record of real investments.** Read the [Disclaimer](#disclaimer) before publishing anything made with it.

## How to use

1. Open `index.html` (double-click it, or use the GitHub Pages link if enabled). You need an internet connection.
2. Pick an **asset** (crypto or Nasdaq-100 stock). Enter a **starting amount** (USD), a **start date** and an **end date** (UTC, default today).
3. *(Optional)* Tick **Also invest regularly**, then set an amount and an interval (every N days, weeks, months or years). Set the starting amount to `0` for a recurring-only plan.
4. Choose a **video length** and click **Generate video** to preview the animation. Use **Replay** to watch it again.
5. Click **Export MP4**. The file is the selected length plus 1 second held on the final result. Keep the tab open while it renders.

## Supported assets

- **Crypto:** a hard-coded snapshot of roughly the top 100 coins by market cap (stablecoins and wrapped tokens left out). Rankings change, so edit the list in `index.html` when you need to.
- **Stocks:** a snapshot of the Nasdaq-100 companies.
- **Logos:** stored in `logos.js` as small embedded images, so they work offline and the video export stays clean. Coins from the `spothq/cryptocurrency-icons` and `@web3icons/core` sets, and stocks from `nvstly/icons`, are included. Any asset without a logo shows a coloured ticker badge.
- If an asset's data starts after your chosen start date, the start date moves to the first available day and the status line says so.

## How the numbers work

- Bitcoin prices are daily BTC/USD closes (UTC) from the [Coin Metrics Community API](https://docs.coinmetrics.io/), with CryptoCompare as a backup. If the end date is today, a live spot price (Coinbase, then Kraken, Binance or CoinGecko) is added as the last point. Other coins use CryptoCompare daily closes and live prices. Stocks use split-adjusted daily closes from Yahoo Finance (price only, no dividends) fetched through public data proxies, which can be slow or unavailable.
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

[MIT](LICENSE) © 2026 Broke Innovation. Company names and logos belong to their owners and are used only to label the simulation; this project is not affiliated with or endorsed by any of them. Third-party data providers have their own terms of use.
