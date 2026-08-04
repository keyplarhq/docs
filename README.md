# Keyplar docs

Merchant-facing documentation for [Keyplar](https://keyplar.com), built on
[Mintlify](https://mintlify.com).

The audience is store owners and their staff: people selling software through Stripe, Lemon
Squeezy or Polar who use Keyplar to deliver what they sold. The **API reference** tab
additionally serves their developers, who integrate the License API.

See [`AGENTS.md`](AGENTS.md) for terminology, style rules and what belongs here — read it before
writing a page.

## Structure

```
docs.json              Navigation, theme, anchors
index.mdx              Introduction
quickstart.mdx         Signup → connected gateway → first test purchase
concepts.mdx           Order → products → benefits
gateways/              Stripe, Lemon Squeezy, Polar setup
catalog/               Products and gateway mapping
benefits/              Downloads, license keys, GitHub access, links, custom
settings/              Store profile, custom domain, team
api-reference/         License API
```

Everything else — orders, subscriptions, customers, licenses, analytics, import, billing,
customer portal, data and privacy — sits at the top level.

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Then, from this directory:

```bash
mint dev
```

The preview runs at `http://localhost:3000`.

Check internal links before pushing:

```bash
mint broken-links
```

## Publishing

Pushing to the default branch deploys to production.

## Troubleshooting

- Dev server misbehaving: run `mint update` for the latest CLI.
- A page 404s: confirm it's listed in `docs.json` and that you're running from the directory
  holding `docs.json`.
