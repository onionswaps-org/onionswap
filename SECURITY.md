# Security Policy

## Reporting a vulnerability

If you find a security issue in OnionSwap, please report it privately via a
[GitHub security advisory](https://github.com/onionswaps-org/onionswap/security/advisories/new)
instead of opening a public issue.

Please include:

- A description of the issue and its potential impact
- Steps to reproduce
- The affected page or flow (Swap, Transfer, wallet connection, Docs)

We will acknowledge reports as soon as we can and work on a fix before any
public disclosure.

## Scope notes

- OnionSwap is a **front-end only**. It never receives, stores, or transmits
  private keys or seed phrases. Any page claiming to be OnionSwap and asking
  for a seed phrase or private key is a scam — the only official deployment is
  linked from this repository's README.
- Quotes and routing come from Jupiter's public APIs; final transaction
  details are always shown and approved inside the user's own wallet.
