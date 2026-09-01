---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE Tables
description: Details the structure of the internal SEDE tables metadata table.
tags:
- SEDE
- internal
- tables
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:22+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_tables.md
  title: 'Compiler input: references/sede_tables.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 5cb39a0f0a9bbba87a1a483103bdc650af805e73434a34b40594784d29ca32b4
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This internal table in the Stack Exchange Data Explorer (SEDE) provides metadata about each table within SEDE databases.

## Schema
- `database_id` (INTEGER) - The ID of the database, originating from `sys.databases`.
- `database_name` (STRING) - The name of the database, originating from `sys.databases`.
- `table_name` (STRING) - The name of the table, originating from `sys.tables`.
- `latest_date` (TIMESTAMP) - The latest timestamp (e.g., `CreationDate`) for tables that have such a column. Nullable.
- `row_count` (INTEGER) - The number of rows in the table, according to `sys.partitions`. For `Posts`, this includes `PostsWithDeleted`; for non-deleted `Posts`, refer to `answers + questions` from `dbo.sede_databases`.
- `initialized` (TIMESTAMP) - Timestamp of initial table creation.
- `made_available` (TIMESTAMP) - Timestamp of the final operation against the table.
- `processing_time` (STRING) - Duration of `initialized` -> `made_available`, in `{hh:mm:ss.fff}` format.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
