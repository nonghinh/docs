# Documentation project instructions

## About this project

- Merchant-facing documentation for **2Boys Wholesale B2B Suite**, a Shopify embedded app that brings B2B/wholesale features to non-Plus merchants.
- Audience: Shopify merchants and store admins. **Not** developers, **not** wholesale buyers — those audiences may be added later.
- Built on [Mintlify](https://mintlify.com); pages are MDX with YAML frontmatter; configuration in `docs.json`.
- Source code for the app lives at `/Users/hinh/Desktop/Projects/Shopify/trade-layer-b2b-wholesale` — consult it when describing features.
- Run `mint dev` to preview locally. Run `mint broken-links` to check links.

## Terminology

Use these terms consistently:

| Use | Don't use |
| --- | --- |
| **Wholesale group** (or **group**) | tier, segment, level |
| **Customer tag** | label |
| **Price rule** | product discount, override |
| **Volume tier** | quantity break, bulk discount |
| **Registration form** | signup form, application form |
| **Application** (when referring to a submitted form) | request, signup |
| **Theme app extension** (or **theme extension**) | theme block (for the umbrella concept) |
| **Storefront block** | section, widget |
| **Shopify Function discount** (full reference) / **discount function** (short) | discount API, function discount |
| `wholesale-{slug}` | wholesale tag pattern, custom tag |
| **Best price wins** | lowest price applies, cheapest discount |
| **MOQ** (spelled out on first use: *minimum order quantity (MOQ)*) | minimum quantity |

## Style preferences

- Active voice, second person ("you").
- One idea per sentence. Short paragraphs.
- Sentence case for all headings (`## Create a wholesale group`, not `## Create A Wholesale Group`).
- **Bold** for UI elements: *Click **Save***.
- `Code formatting` for slugs, tags, scopes, file names, and field names referenced in code.
- Use `→ [Page name](/path)` for inline forward references to other docs pages.
- Avoid em-dashes inside tables; use a comma or period.
- Prefer numbered steps for procedures, bullets for non-sequential lists.
- Reserve `<Note>`, `<Tip>`, `<Warning>` for genuinely useful asides — not as decoration.

## Image conventions

- Place images under `/images/{group}/{page-slug}.png` (e.g. `/images/groups/create-group.png`).
- Wrap images in `<Frame>` with a descriptive `alt` attribute.
- The actual screenshot files do not exist yet — leave the `<Frame>` tags in place; the merchant will populate them.

## Content boundaries

Document:
- Every merchant-facing feature in the admin (groups, pricing, forms, applications, emails, storefront, settings, analytics, operations).
- The *concepts* behind storefront and checkout integration — not the underlying code.
- GDPR / privacy behaviors that the merchant is accountable for.

Don't document:
- The Laravel queue worker internals, BullMQ job names, or database schema specifics.
- Any internal API routes, webhook handlers, or developer endpoints.
- The buyer-side experience in detail (covered separately if/when a buyer guide is added).
- Pricing, plans, or commercial terms — those live on the Shopify App Store listing.
