# Erganis Lyceum (Mnemosyne)

**Mnemosyne** — lean public reference for **historical design styles** (eras, motifs, palettes, forms). Consumer-facing brand: **Mnemosyne**. Repository folder: **`lyceum/`** (place of study).

## Structure

| Folder | Purpose |
|--------|---------|
| **web/** | Public site — Mnemosyne (Next.js + shadcn + Tailwind) |
| **api/** | Optional Nest API + dedicated DB if content volume warrants; else Core-backed |
| **shared/** | Types and clients aligned with Core contracts |

## Relationship to platform

| Link | Detail |
|------|--------|
| **Core** | Contracts, Scraper Services, optional shared auth |
| **Studio / Design** | Embed or link style references in exploration work |
| **Agora** | Separate — vendors/products vs design history |

**Open:** dedicated DB vs Core content store, editorial workflow — see [erganis product plan §10](https://github.com/enabledtocreate/erganis/blob/master/docs/erganis-product-plan.md#10-mnemosyne-lyceum).

## Dependencies

- **Core contracts** — style/reference schemas (as defined)
- **Lyceum API** (if used) — consumed by `web/`
- No direct access to Studio databases

## Environment variables

Copy `.env.example` to `.env` in `web/` and `api/` as needed.

## GitHub

**Owner:** [enabledtocreate](https://github.com/enabledtocreate)  
**Repo:** `erganis-lyceum`
