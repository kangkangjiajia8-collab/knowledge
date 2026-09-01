---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE Databases
description: Details the structure of the internal SEDE database metadata table.
tags:
- SEDE
- internal
- databases
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:12+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_databases.md
  title: 'Compiler input: references/sede_databases.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: bdfbb99f2e208de7b9cb0e4d37839617660e31ab026fb8d6916265adf303b994
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This internal table in the Stack Exchange Data Explorer (SEDE) provides metadata about each Stack Exchange site\'s database within SEDE.

## Schema
- `database_id` (INTEGER) - Unique identifier for the database.
- `database_name` (STRING) - The name of the database.
- `site_name` (STRING) - The short name of the site.
- `tiny_name` (STRING) - A very short name for the site.
- `long_name` (STRING) - The full name of the site.
- `site_type` (STRING) - Type of site, either \'main_site\' or \'meta_site\'.
- `site_url` (STRING) - The base URL of the Stack Exchange site.
- `sede_url` (STRING) - The URL to the site\'s data in SEDE.
- `api_site_parameter` (STRING) - The parameter used for the site in the Stack Exchange API.
- `initialized` (TIMESTAMP) - Datetime when populating that database started.
- `made_available` (TIMESTAMP) - Datetime when the database came online and was ready for queries.
- `processing_time` (STRING) - The duration between `initialized` and `made_available`, in `hh:mm:ss.fff` format.
- `questions` (INTEGER) - Total number of questions in this site at the time of the current refresh.
- `answers` (INTEGER) - Total number of answers in this site at the time of the current refresh.
- `latest_post` (TIMESTAMP) - The timestamp of the last non-deleted post captured in this refresh.
- `notes` (STRING) - This will be non-NULL when a database is in transition. Nullable.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
