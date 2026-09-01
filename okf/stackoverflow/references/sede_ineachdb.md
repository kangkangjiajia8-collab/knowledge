---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE In Each DB Stored Procedure
description: Describes the SEDE internal stored procedure for running SQL commands across multiple databases.
tags:
- SEDE
- internal
- stored procedure
- SQL
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:39+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_ineachdb.md
  title: 'Compiler input: references/sede_ineachdb.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 9cdeab1706137a92af8f4adbb73b34e535836d789612a0c1a008ab1ab0c362d1
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This is an internal stored procedure in the Stack Exchange Data Explorer (SEDE) used to execute SQL commands across multiple databases (i.e., Stack Exchange sites).

## Parameters
| Parameter           | Data Type      | Default | Description                                                               |
|---------------------|----------------|---------|---------------------------------------------------------------------------|
| `@SQLCommand`       | `nvarchar(4000)` |         | The SQL statement to run.                                                 |
| `@IncludeMainSites` | `bit`          | `1`     | Set to `1` to include all non-meta sites.                                 |
| `@IncludeMetaSites` | `bit`          | `1`     | Set to `1` to include all meta sites.                                     |
| `@IncludeMainMeta`  | `bit`          | `1`     | Set to `1` to include `StackExchange.Meta`.                               |
| `@CollectResultsForMe` | `bit`          | `1`     | For standard `SELECT` queries, this will attempt to put each database's results into a `#temp` table. |
| `@ErrorOnSkippedSites` | `bit`          | `0`     | Set this to `1` if you want execution to halt in the event any site is missing due to transition change. |

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
