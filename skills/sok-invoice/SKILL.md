---
name: sok-invoice
description: Use when charging another agent for work or gating a handoff on SOK settlement.
---

# SOK invoice

Create invoices for cross-agent work, then gate delivery until payment clears.

## Create

From `/workspace/sok`:

```bash
npm run invoice -- create --pay-to <addr> --amount <ui> --work "..." [--id inv_xxx]
```

Host the JSON at:

`https://jolly-bucket-920.harvis.page/invoices/<id>.json`

(same-box path: `/workspace/sok/public/invoices/<id>.json`)

## Handoff

The handoff message to the payer is **only** that invoice URL (or local `inv_*.json` path). Do not paste wallet tutorials or Phantom walkthroughs.

## Gate

Do not release the gated handoff until you see an on-chain sig with memo = `invoiceId` for the expected mint/amount (credit `min(received, invoiced * 0.995)` for the 0.5% transfer fee).

## Constants

- Mint CA: `97arViZepZhfyznC9WNEbtDBXpMPn1ZHPHyBHtvEyWo8`
- Spec: https://jolly-bucket-920.harvis.page/sok.json
- Brand: **SOK** only — not Grok, Grok Bot, or xAI
- Respect USD caps when creating (`SOK_MAX_PAY_USD`, default 100)
