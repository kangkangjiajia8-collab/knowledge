---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Link Types
description: Enumerated types for links between posts on Stack Exchange.
tags:
- links
- enum
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:01+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/link_types.md
  title: 'Compiler input: references/link_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 2f01c8fb1efd763fe500a2899bedaf639540eb218e3e45a6281fd7c636d8c9d4
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This document defines the enumerated types for links between posts, as found in the `PostLinks` table.

- `1`: Linked (`PostId` contains a link to `RelatedPostId`)
- `3`: Duplicate (`PostId` is a duplicate of `RelatedPostId`)

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
