---
name: postgresql-optimization
description: "Use when: improve PostgreSQL schema, queries, indexes, JSONB, arrays, full-text search, or performance with Postgres-specific features."
---

Goal: use PostgreSQL features deliberately and measure performance with evidence.

Use for:
- slow queries, missing indexes, schema design, and data modeling
- JSONB, arrays, custom types, ranges, full-text search, and extensions
- window functions, CTEs, materialized views, and analytics queries
- migration review and Postgres-specific refactors

Workflow:
1. Identify table sizes, query shape, filters, joins, and expected latency.
2. Run or request `EXPLAIN (ANALYZE, BUFFERS)` for performance work.
3. Check existing indexes, constraints, and data distribution.
4. Pick the smallest Postgres feature that solves the real bottleneck.
5. Propose migration SQL plus rollback when schema changes are needed.
6. Verify with query plans, tests, and representative data.

Patterns:
- JSONB: GIN indexes, containment, path extraction, generated columns
- arrays: `ANY`, overlap, containment, unnest only when needed
- text search: `tsvector`, GIN, ranking, language config
- analytics: window functions over app-side loops
- indexing: composite order, partial indexes, covering indexes

Rules:
- do not add indexes without a query they serve
- do not optimize synthetic tiny data as if it were production
- keep migrations reversible when possible
- measure before and after
