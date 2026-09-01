---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE Sites
description: Details the structure of the internal SEDE sites metadata table.
tags:
- SEDE
- internal
- sites
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:26+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_sites.md
  title: 'Compiler input: references/sede_sites.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: fc955b0fddeca4857b58eb1e37d9da6159ba8102b4aef7a9e402709404e773d9
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This internal table in the Stack Exchange Data Explorer (SEDE) provides metadata about each Stack Exchange site.

## Schema
- `site_name` (STRING) - The short name of the site.
- `site_url` (STRING) - The base URL of the Stack Exchange site.
- `database_name` (STRING) - The name of the corresponding database in SEDE.
- `long_name` (STRING) - The full name of the site.
- `site_id` (INTEGER) - Unique identifier for the site.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
