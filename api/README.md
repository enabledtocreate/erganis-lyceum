# Mnemosyne API (optional)

NestJS service for Lyceum content — **only if** content volume warrants a dedicated PostgreSQL database.

## Default path (TBD)

Mnemosyne may read style reference content from **Core-backed APIs** instead of a separate service. See [docs/erganis-product-plan.md §10](https://github.com/enabledtocreate/erganis/blob/master/docs/erganis-product-plan.md#10-mnemosyne-lyceum) and open question #32 (DB vs Core store).

## When this folder is used

- Dedicated editorial corpus and search at scale
- Separate deploy cadence from Core
- pg-boss jobs for scraper ingestion into Lyceum DB

## Contracts

Style entry shapes defined in **Core contracts**; Lyceum OpenAPI extends those components when this API exists.

## Environment

See `lyceum/.env.example`.
