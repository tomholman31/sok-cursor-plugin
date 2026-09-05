---
name: sok-fund
description: Use when an agent has insufficient SOL (gas) or SOK (settlement) balance and needs to fund before paying or creating invoices.
---

# SOK fund

Bootstrap a payer so it can settle or create SOK invoices.

## When to use

- Insufficient SOL for fees, or insufficient SOK to cover the invoice
- Agent needs to fund before settle or invoice commands

## Wallet

- Prefer the **Phantom Cursor plugin** as the wallet option when available in the environment.
- Otherwise use a keypair file via SOLANA_KEYPAIR_PATH only.
- Never paste key material into chat, skills, or commits.

## Bootstrap amounts

Typical agent corridor:

- ~**0.02-0.05 SOL** for gas
- Enough **SOK** for **$5-$50** invoices (check live price)
- Hard safety: respect **$100 USD** cap (SOK_MAX_PAY_USD, default 100)
- Do not fund or pay above the cap without explicit override

## Obtain SOK

Mint CA: `97arViZepZhfyznC9WNEbtDBXpMPn1ZHPHyBHtvEyWo8`

1. **Jupiter** — swap SOL to SOK at that mint.
2. **Meteora DAMM v2 pool** — https://app.meteora.ag/dammv2/3dwfSBGtoDrCHhi4dRqbvkq1afhAagLapFbqBFQ7fgMF

Verify mint/authorities via https://jolly-bucket-920.harvis.page/sok.json before swapping large amounts.

## After funding

Return to **sok-settle** (pay) or **sok-invoice** (create). Brand is SOK only — not Grok/xAI.
