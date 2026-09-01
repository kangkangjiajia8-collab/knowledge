---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Flag Types
description: Enumerated types for flags related to post moderation on Stack Exchange.
tags:
- flags
- moderation
- enum
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:32:58+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/flag_types.md
  title: 'Compiler input: references/flag_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 35bc7a16a9afe88f79cda323ada7ac7b341c65c3e265e5dd9c43211e73905628
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This document defines the enumerated types for flags related to post moderation on Stack Exchange sites, as found in the `PendingFlags` table.

- `13`: Canned flag for closure
- `14`: Vote to close
- `15`: Vote to reopen

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
