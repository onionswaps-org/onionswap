<p align="center">
  <img src="logo.png" alt="OnionSwap logo" width="160" />
</p>

<h1 align="center">OnionSwap</h1>

<p align="center">
  <strong>Swap &amp; transfer — all in one place.</strong><br />
  A refined, non-custodial front-end for Solana, powered by the Jupiter aggregator.
</p>

<p align="center">
  <a href="https://onionswaps.org"><img alt="Live" src="https://img.shields.io/badge/Live-onionswaps.org-8b5cf6" /></a>
  <img alt="Network" src="https://img.shields.io/badge/Network-Solana-9945FF" />
  <img alt="Powered by Jupiter" src="https://img.shields.io/badge/Powered%20by-Jupiter-c8f169" />
  <img alt="License" src="https://img.shields.io/badge/License-MIT-blue" />
</p>

---

## About

OnionSwap is a single-page web app for Solana. It gives you one clean interface to swap tokens at the best rate across Solana DEXes via Jupiter, and to send SOL or any SPL token in seconds — with live prices, live quotes and real-time wallet balances on every screen.

**OnionSwap charges no fees.** The site never holds your keys and never takes custody of your funds: every transaction is built in your browser and signed by your own wallet.

## Features

- **Swap via Jupiter** — best-route quotes across Solana DEXes, with rate, price impact, minimum received, route and platform/LP fee breakdown before you sign
- **Slippage control** — adjustable slippage from the swap panel settings
- **Token search** — search any Solana token from the top bar and inspect its info card (price, market cap, FDV, liquidity, volume, holders, supply) with a Solscan link
- **Popular tokens** — a live-priced board of popular Solana tokens with one-tap Trade
- **Transfer** — send SOL or any SPL token with an elegant token picker, MAX button, live balances, and a review step before sending
- **Safe by default** — transfers are simulated before they are sent, and missing associated token accounts are created automatically
- **Wallets** — Phantom, Solflare and Backpack (injected providers)
- **Resilient RPC** — balance reads automatically fail over between public Solana RPC endpoints if one rate-limits or refuses a request
- **Live price ticker** — streaming prices for the tracked token set
- **In-app Docs** — overview, getting started, swap, transfer, networks & endpoints, safety and troubleshooting, built into the app
- **No account, no deposits** — connect a wallet and go

## Live site

**https://onionswaps.org**

## Quick start

OnionSwap is a single self-contained `index.html` — there is no build step.

    git clone https://github.com/onionswaps-org/onionswap.git
    cd onionswap
    # open index.html in a browser, or serve it:
    npx serve .

### Deploy your own

- **Vercel** — import the repo, framework preset "Other", no build command; the root `index.html` is served as-is.
- **GitHub Pages** — this repo ships a ready workflow (`.github/workflows/pages.yml`); enable Pages with "GitHub Actions" as the source and push to `main`.

## Project structure

    .
    ├── index.html                  # The entire app (UI, styles and logic in one file)
    ├── logo.png                    # OnionSwap mascot logo
    ├── .github/
    │   └── workflows/
    │       └── pages.yml           # GitHub Pages deployment
    ├── CHANGELOG.md
    ├── CONTRIBUTING.md
    ├── SECURITY.md
    ├── LICENSE
    └── README.md

## How it works

1. **Quotes** come from Jupiter's public APIs (`lite-api.jup.ag`): swap quotes and order routing, token search, and prices.
2. **Your wallet signs everything.** OnionSwap builds the transaction; Phantom, Solflare or Backpack signs and broadcasts it. Nothing is ever signed by the site.
3. **Balances** are read directly from Solana RPC. Reads rotate between the public endpoints (`api.mainnet-beta.solana.com`, PublicNode) so a single rate-limited endpoint does not break the app.
4. **Transfers are simulated first.** If the simulation fails, the send does not proceed.

## Security

OnionSwap is fully non-custodial:

- Private keys and seed phrases never touch the site — there is nowhere to enter them, and you should never enter them anywhere.
- The site holds no user funds and cannot move funds without a wallet signature.
- Always check the transaction details in your wallet before approving.

See [SECURITY.md](SECURITY.md) for how to report a vulnerability.

## Roadmap

- Additional public RPC endpoints for balance reads
- Continued UI polish of the swap and transfer flows

## Contributing

Contributions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE) © 2026 OnionSwap

