> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is the **merchant-facing** documentation for [Keyplar](https://keyplar.com), built on
  [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- The audience is **store owners and their staff** — people selling software through Stripe,
  Lemon Squeezy or Polar who use Keyplar to deliver what they sold. The API reference tab
  additionally serves their developers.
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information
  about using Mintlify via MCP

## Terminology

Use these words. They match what merchants see in the product.

| Use | Not |
| --- | --- |
| **store** — one merchant's Keyplar instance | tenant, workspace, site |
| **admin panel** — the merchant's side of the store | dashboard (that's a page inside it), backend |
| **portal** — the customer's side of the store | frontend, storefront |
| **customer** — someone who bought from the merchant | user, end user, buyer (in headings) |
| **admin** — someone with admin access to a store | staff, member, operator |
| **product** — a catalog entry in Keyplar | SKU, item |
| **benefit** — what a product delivers | entitlement, grant (in merchant-facing text), perk |
| **license key** / **key** | serial, licence (use the -se spelling) |
| **activation** or **seat** — one machine using a key | instance (that's the API's word), device |
| **gateway** — Stripe, Lemon Squeezy, Polar | provider, processor, PSP |
| **plan** — the merchant's Keyplar subscription | tier, package |

Other conventions:

- The chain is **order → products → benefits**. Say it that way round.
- Example hosts: `yourstore.keyplar.com` for a store, `app.keyplar.com` for signup and the
  platform. Don't invent other domains.
- "Keyplar" is the product; avoid "the platform" and "the system".

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Prefer explaining *why* a behaviour exists over listing it — merchants act on reasons
- Every plan-gated feature carries a `<Note>` naming the plan, at the top of the page or section

## Content boundaries

**Document:**

- Anything a merchant can see or do inside their own store's admin panel and portal
- Setup they perform in their own payment gateway
- The License API, for their developers

**Don't document:**

- The Keyplar operator console — tenant management, plan CRUD, suspending stores. Merchants
  never see it.
- Deployment, hosting, environment variables, database, CLI scripts, background workers
- Source file paths, table names, function names, or internal architecture
- Anything that would only make sense to someone with the repository open

When a merchant-visible behaviour is produced by an internal mechanism, describe the behaviour
and its timing, not the mechanism.

## Accuracy

The product is the source of truth, not this repo. Before documenting a screen, a field, a
webhook event list, or an API shape, check the application code rather than working from memory
— label copy, supported events and response fields all drift.
