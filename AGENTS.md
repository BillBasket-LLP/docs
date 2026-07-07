> **First-time setup**: Customize this file for your project. Prompt the user to customize this file for their project.
> For Mintlify product knowledge (components, configuration, writing standards),
> install the Mintlify skill: `npx skills add https://mintlify.com/docs`

# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- Product name is **BillBasket**. The codebase/repo is called `venda` —
  never expose that name in docs.
- Use "Store" or "Business" in customer-facing docs, not "org"/"organization"
  (that's internal Firestore/code terminology only).
- Use "Employee", not "Salesman" (renamed in-app; code/DB still say salesman).
- Use "Party" only when writing for engineers; customer-facing docs should
  say "customer" or "supplier" instead — but that always means *the shop's*
  customer (the person being billed), never the reader of the docs.
- Docs audience for the Customer Guide tab is the **Shop/Business Owner**
  (and their staff) — the person running the POS. Never call the reader
  "customer"; address them as "you" or "shop owner" to avoid colliding with
  the Party/customer concept above.
- Three audiences, one tab each: **Customer Guide** (Shop/Business Owner —
  reader of the POS), **Partner Hub** (training material for partners),
  **Internal Ops** (Sales & Support runbooks).

## Sample personas (worked examples)

Reuse these consistently across "Try it" walkthroughs instead of inventing
new shops per page:

- **Sharma Kirana Store** (Rajesh Sharma, staff Suresh) — default persona
  for general retail/grocery: everyday products, credit accounts, purchases.
- **Bali Electronics** (Vikram Bali, staff Deepak) — used specifically for
  serial-number-tracked stock (phones, TVs, appliances), since individually
  identifiable high-value units don't fit a kirana-store example.

## Style preferences

{/* Add any project-specific style rules below */}

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references
- Customer Guide audience is rural/busy shop owners — plain language, short
  steps, no jargon, never assume prior software experience.

## Content boundaries

- Customer Guide: task-first, user-facing behavior only. No schema, API,
  migration, or internal architecture details.
- Do not document internal-only surfaces (Admin PIN reset internals, sync
  engine internals, licensing backend, submodule repos) in the Customer
  Guide — those belong in Internal Ops once that tab is written.
- Don't invent features — cross-check against the `venda` repo
  (`lib/features/`) before writing a page; if unsure a feature exists as
  described, mark the page as a placeholder instead of guessing.
