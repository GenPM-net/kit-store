# @core/kit-store

[![genpm](https://api.genpm.net/v1/badge/@core/kit-store.svg)](https://genpm.net/p/@core/kit-store) ![license](https://img.shields.io/badge/license-MIT-blue)

> Online store kit for Next.js: catalog, cart, Stripe checkout, orders, shipping, coupons, verified reviews, accounts

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/app/(store)`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/kit-store
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/kit-store`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/kit-store with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

An online store on top of @core/kit-cms, managed from the same `/admin`: products with variants and categories,
cart, Stripe Checkout, orders (created only by the Stripe webhook), shipping zones and rates, discount codes,
verified reviews, customer orders page, transactional emails and SEO (Product JSON-LD, sitemap). Every storefront
form is a Next.js Server Action, so it works without JavaScript and never accepts prices from the browser.

## At a glance

- **GenPM dependencies** (installed with it): [@core/kit-cms](https://genpm.net/p/@core/kit-cms), [@core/catalog](https://genpm.net/p/@core/catalog), [@core/cart](https://genpm.net/p/@core/cart), [@core/checkout](https://genpm.net/p/@core/checkout), [@core/orders](https://genpm.net/p/@core/orders), [@core/shipping](https://genpm.net/p/@core/shipping), [@core/discounts](https://genpm.net/p/@core/discounts), [@core/reviews](https://genpm.net/p/@core/reviews)
- **npm dependencies** (proposed, never installed without asking): `next`, `react`, `zod`
- **Environment variables** (added to `.env.example`): `STRIPE_SECRET_KEY`, `STRIPE_WEBHOOK_SECRET`, `CART_COOKIE_SECRET`, `ORDER_LINK_SECRET`, `STORE_CURRENCY`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/app/(store)`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
