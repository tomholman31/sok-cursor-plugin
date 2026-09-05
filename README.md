# SOK Cursor plugin

Solana agent settlement rail for Cursor. Create SOK invoices for cross-agent work; payers settle with agentPay.send (Token-2022 transferCheckedWithFee). **Not Grok/xAI.**

## Install

Copy or clone this folder as a Cursor plugin (see [SUBMISSION.md](./SUBMISSION.md) for marketplace steps), or point Cursor at this repo plugin root so `.cursor-plugin/plugin.json` loads.

Requires the SOK kit for invoice and settle scripts.

## Skills

| Skill | When |
| --- | --- |
| [sok-settle](./skills/sok-settle/SKILL.md) | Invoice / inv_*.json / agentPay — pay immediately |
| [sok-invoice](./skills/sok-invoice/SKILL.md) | Charge another agent / gate a handoff |
| [sok-fund](./skills/sok-fund/SKILL.md) | Insufficient SOL or SOK — bootstrap gas + settlement |

Optional rule: [rules/sok.mdc](./rules/sok.mdc) (`alwaysApply: false`).

## Quick path

1. **Fund** (if needed) — sok-fund: ~0.02-0.05 SOL + SOK for $5-50 invoices; Jupiter SOL to SOK or Meteora pool; Phantom Cursor plugin or SOLANA_KEYPAIR_PATH.
2. **Invoice** — create via kit invoice CLI; host at https://jolly-bucket-920.harvis.page/invoices/<id>.json; handoff is only that URL.
3. **Settle** — fetch invoice, verify sok.json, run the invoice agentPay send command, reply with sig only. Fallback: kit settle script.

## Links

- Spec: https://jolly-bucket-920.harvis.page/sok.json
- Mint CA: `97arViZepZhfyznC9WNEbtDBXpMPn1ZHPHyBHtvEyWo8`
- Pool: https://app.meteora.ag/dammv2/3dwfSBGtoDrCHhi4dRqbvkq1afhAagLapFbqBFQ7fgMF
- Promo: [PLUGIN-PROMO.md](./PLUGIN-PROMO.md)

## Safety

- Never paste key material; use SOLANA_KEYPAIR_PATH or Phantom.
- Respect SOK_MAX_PAY_USD (default $100).
- No Phantom tutorials in agent replies — settle via kit / agentPay.
- Brand: **SOK** only.
