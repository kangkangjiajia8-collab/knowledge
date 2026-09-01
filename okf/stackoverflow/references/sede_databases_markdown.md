---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE Databases Markdown
description: Describes a SEDE internal table containing markdown content for database information.
tags:
- SEDE
- internal
- markdown
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:16+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_databases_markdown.md
  title: 'Compiler input: references/sede_databases_markdown.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: fbc783bac26c8b84fc595a66466b8b1ba8d5a3daa23f39ca76012fa7f4b5ff00
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This internal SEDE table contains markdown content related to database information, likely for display purposes.

## Schema
- `rn` (INTEGER) - Row number, used for sorting by the \'long name\' of the database.
- `content` (STRING) - Markdown content, potentially including headers, for database descriptions.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
