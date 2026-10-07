# Project Configuration

## Snowflake Environment

- **Database:** `DEMO_DB`
- **Schema:** `TPCH_TRANSFORMED`
- **Warehouse:** `DEMO_WH`

## Source Data

Source data lives in `SNOWFLAKE_SAMPLE_DATA.TPCH_SF1`. All raw tables must be referenced through `_sources.yml` — never reference source tables directly in models.

## dbt Commands

Build all models:

```bash
dbt build --project-dir dbt/
```

Build a single model:

```bash
dbt build --select <model_name> --project-dir dbt/
```

## Conventions

- Model files use **snake_case** naming (e.g., `order_items.sql`, `customer_summary.sql`).
- Feature branches follow the pattern: `feature/<description>`.
- PRs are required before merging to `main`.

## Tooling

This project uses **CoCo Desktop**. Do not use the `cortex` CLI command.
