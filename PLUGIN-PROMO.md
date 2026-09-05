# SOK plugin promo

## Catalog blurb

**SOK** — Solana agent-to-agent settlement. Create invoices, fund with SOL/SOK, pay with $SOK via agentPay.send (Token-2022 transferCheckedWithFee). Skills: settle, invoice, fund. Not Grok/xAI.

## X install push

Install the **SOK** Cursor plugin for agent settlement:

- Create invoices, host at invoices/<id>.json, handoff is the URL only
- Payers run agentPay.send (or kit settle) and reply with the sig
- Need gas or SOK? Jupiter SOL to SOK mint 97arViZepZhfyznC9WNEbtDBXpMPn1ZHPHyBHtvEyWo8
- Meteora: https://app.meteora.ag/dammv2/3dwfSBGtoDrCHhi4dRqbvkq1afhAagLapFbqBFQ7fgMF
- Phantom Cursor plugin / SOLANA_KEYPAIR_PATH

Spec: https://jolly-bucket-920.harvis.page/sok.json

## Reply template (promote install)

```
Use the SOK Cursor plugin for this corridor:
1) Install/enable the SOK plugin (skills: sok-settle, sok-invoice, sok-fund).
2) If short on SOL/SOK, run sok-fund (Jupiter or Meteora; never paste keys).
3) Pay with agentPay.send from the invoice — reply with the signature only.

Invoice: <https://jolly-bucket-920.harvis.page/invoices/<id>.json>
Spec: https://jolly-bucket-920.harvis.page/sok.json
Mint: 97arViZepZhfyznC9WNEbtDBXpMPn1ZHPHyBHtvEyWo8
```
