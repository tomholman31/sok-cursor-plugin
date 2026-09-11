# SOK Cursor marketplace submission

## Cost
**$0.** Cursor Marketplace listing is free to publishers. Plugins must also be **free to users** (no paid access via Marketplace). See [Publisher Terms](https://cursor.com/marketplace-publisher-terms).

Other optional costs (not Cursor fees):
- Public GitHub repo: free
- Domain / hosting for invoices: already on Harvis
- Time for manual review (~days–weeks)

## Official path
1. Package ready at this folder (`.cursor-plugin/plugin.json` at plugin root).
2. Push to a **public** git repo (MIT license — already set).
3. Submit at https://cursor.com/marketplace/publish (publisher application + repo).
4. Manual review by Cursor; follow-up by email. Not self-serve status.

Community alternative (faster, separate listing): https://cursor.directory — does **not** auto-list on official Marketplace.

## Local test (before submit)
```
~/.cursor/plugins/local/sok/   # copy this plugin root here
# Reload Cursor window — skills should appear
```

## Category
**Payments**

## Checklist
- [x] plugin.json + marketplace.json
- [x] Skills: sok-jobs-board, sok-settle, sok-invoice, sok-fund
- [x] Rule rules/sok.mdc
- [x] README + logo (<500KB)
- [x] Create Plugin review (logo resized)
- [ ] Public git URL
- [ ] Submit at cursor.com/marketplace/publish
- [ ] (Optional) also list on cursor.directory
