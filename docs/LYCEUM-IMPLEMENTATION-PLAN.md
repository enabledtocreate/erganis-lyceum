# Mnemosyne (Lyceum) — Implementation Plan

> **Status:** Not started.  
> **Product plan:** [§10 Mnemosyne](../../../docs/erganis-product-plan.md#10-mnemosyne-lyceum) · **Index:** [IMPLEMENTATION-PLANS](../../../docs/IMPLEMENTATION-PLANS.md)

**Product name:** **Mnemosyne** · **GitHub:** `erganis-lyceum` · **Path:** `lyceum/`

Lean, designer-focused reference for **historical styles** — curated for practice, not academic completeness.

---

## Overview

| Phase | Name | Delivers | Platform deps |
|-------|------|----------|---------------|
| **L0** | Content model | Style entry schema, tags, era/region fields | Core contracts |
| **L1** | Public web | Browse + search (Next.js + shadcn) | — |
| **L2** | API layer | Dedicated Nest API + DB **or** Core-backed content | TBD ([§20 open questions](../../../docs/erganis-product-plan.md#20-open-questions)) |
| **L3** | Enrichment | Core Scraper Services for external reference metadata | Core scraper infra |
| **L4** | Studio links | Embed/link from Studio Design and Presentations | Studio S-Des1 |

---

## L0 — Content model

**Delivers:**

- Curated style entries (editorial + structured fields)
- Tags, era, region, related movements
- Shared types in `lyceum/shared/` aligned with Core contracts

**Distinct from:** Studio **Design** module (firm project creativity) and **Agora** (vendors/products).

---

## L1 — Public web (Mnemosyne)

**Layout:**

```
lyceum/
├── web/       # Public site — Mnemosyne
├── api/       # Optional Nest API
└── shared/
```

**Stack:** Next.js + shadcn + Tailwind (same pattern as Studio/Agora web).

**UX goal:** Actionable guidance — era characteristics, motifs, palettes, furniture/forms, do/don't pairings — optimized for designers on deadline.

---

## L2 — API / persistence

**Open decision:** Dedicated Lyceum database vs Core content store.

Options documented in product plan §20. Implementation plan proceeds with **contract-first** types regardless of storage choice.

---

## L3 — Scraper enrichment

**Delivers:** Optional refresh of external reference pages via **Core Scraper Services** (XPath recipes, meta tags, cache headers).

Respect licensing/ToS (policy TBD).

---

## L4 — Studio integration

**Delivers:** Cross-links from Studio Design exploration and Presentations.

May consume style references as read-only Public API or embedded widgets.

---

## Brand note

- **Mnemosyne** — consumer-facing brand (memory of design history)
- **Lyceum** — repository folder name (place of study)

---

## Relationship to platform

| Link | Detail |
|------|--------|
| Core | Contracts, Scraper Services, optional shared auth |
| Studio / Design | Embed or link style references |
| Agora | Separate — vendors/products vs design history |
