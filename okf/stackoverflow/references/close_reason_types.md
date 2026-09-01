---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Close Reason Types
description: Enumerated types for reasons why a post might be closed on Stack Exchange.
tags:
- close reasons
- moderation
- enum
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:33:07+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/close_reason_types.md
  title: 'Compiler input: references/close_reason_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 5a01dfb391a813a8f44e6c7800aa5ea073e38bb6bfdf7a96fabd822c86791b02
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This document defines the enumerated types for reasons why a post might be closed on Stack Exchange sites, as found in the `PendingFlags` and `PostHistory` tables.

## Old Close Reasons
- `1`: Exact Duplicate
- `2`: Off-topic
- `3`: Subjective and argumentative
- `4`: Not a real question
- `7`: Too localized
- `10`: General reference
- `20`: Noise or pointless (Meta sites only)

## Current Close Reasons
- `101`: Duplicate
- `102`: Off-topic
- `103`: Unclear what you\'re asking
- `104`: Too broad
- `105`: Primarily opinion-based

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
