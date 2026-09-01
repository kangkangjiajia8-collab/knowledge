---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Post Notice Types
description: Enumerated types for notices that can be applied to posts on Stack Exchange.
tags:
- notices
- posts
- enum
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:22+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/post_notice_types.md
  title: 'Compiler input: references/post_notice_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: b0c4b5367eb4b9dc2c3497b5400cd4291067993abbd244bea48000320e9807fd
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This document defines the enumerated types for notices that can be applied to posts on Stack Exchange sites, as found in the `PostNotices` table.

- `1`: Citation needed
- `2`: Current event
- `3`: Insufficient explanation
- `10`: Current answers are outdated
- `11`: Draw attention
- `12`: Improve details
- `13`: Authoritative reference needed
- `14`: Canonical answer required
- `15`: Reward existing answer
- `20`: Content dispute
- `21`: Offtopic comments
- `22`: Historical significance
- `23`: Wiki Answer
- `24`: Policy Lock (SO Collectives)
- `25`: Recommended Answer (SO Collectives)
- `26`: Posted by Recognized Member/Admin (SO Collectives)
- `27`: Endorsed Edit (SO Collectives)
- `28`: Obsolete (SO Collectives)
- `1000`: Redditted (SO)
- `9001`: DMCA Takedown

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
