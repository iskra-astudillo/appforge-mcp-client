# AppForge MCP client examples

AI app builder: generated code you download, PWA export and deployment handoff to Empire Cloud. Free, Pro $14.99/month or Lifetime $249.99.

This repository holds small, working examples for the hosted **AppForge** MCP server. It is maintained by Elite AI Empire. The server itself is hosted; nothing here runs it.

- Product: https://appbuilderai.studio/
- MCP endpoint (streamable HTTP): `https://appbuilderai.studio/mcp`
- OpenAPI: https://appbuilderai.studio/openapi.json
- Pricing, machine readable: https://appbuilderai.studio/pricing.json
- Discovery file: https://appbuilderai.studio/.well-known/mcp.json

## Tools

| Tool | What it does |
|---|---|
| `appbuilder_plans` | Returns each plan with its USD price, billing period and access status. Same data as the pricing page. Pricing: {"unit": "call", "price_usd": 0, "free_quota": " |
| `appbuilder_about` | What AppBuilderAI does and what is free Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is published |
| `appbuilder_pricing` | Where prices live and what costs nothing Pricing: {"unit": "call", "price_usd": 0, "free_quota": "200 per day per IP", "note": "Keyed volume pricing is publishe |
| `usage_get` | Usage for the calling key (last 30 days) |
| `get_company_info` | What this company sells, who it is for, and every agent/API entry point. No account needed. |
| `list_pricing` | Current plans and prices in USD: plan, interval, amount_usd, currency, what_you_get. No account needed. |
| `get_checkout_link` | Checkout URL for a plan. With no arguments: the main paid plan. Where the site supports it the URL is a Stripe-hosted Checkout session (created unpaid; a human  |
| `search_site` | Find pages on this site by keyword; returns url, title and summary. |

## Try it

```bash
bash examples/initialize.sh
python3 examples/client.py
```

`examples/client.py` uses only the Python standard library. It sends `initialize` and `tools/list` and prints the result. No key is needed for the public read tools. Tools that need an account say so in their description.

## Registry

Listed in the official MCP registry. Server manifest: `server.json`.

## Licence

MIT. See `LICENSE`.
