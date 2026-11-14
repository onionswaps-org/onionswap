# Contributing to OnionSwap

Thanks for your interest in improving OnionSwap!

## Ground rules

- The app is a **single self-contained `index.html`** with no build step. Please keep it that way — no bundlers, no frameworks, no external assets that are not already inlined.
- OnionSwap is **non-custodial**. Never add anything that asks for, stores, or transmits private keys or seed phrases.
- All transactions must remain **wallet-signed by the user**, and transfers must stay **simulated before sending**.

## Making changes

1. Fork the repo and create a branch: `git checkout -b my-change`
2. Edit `index.html` and test by opening it in a browser with a Solana wallet extension (Phantom, Solflare or Backpack) installed.
3. Test the flows you touched: connect wallet, get a swap quote, search a token, and open the Transfer panel.
4. Commit with a clear message and open a pull request describing what changed and how you tested it.

## Reporting bugs

Open an issue with:

- What you did, what you expected, and what happened
- Your browser and wallet (name + version)
- A screenshot or the exact error message, if any

Please do **not** include wallet addresses with significant funds, seed phrases, or any private information in issues.

## Style notes

- Keep the UI consistent with the current theme: dark violet-black surfaces, violet primary accents, and Jupiter-lime (`#c8f169`) for the green accents.
- The headline and headings use a single font (Sora); body text uses Manrope; numbers and addresses use JetBrains Mono.
