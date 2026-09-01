---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Review Rejection Reasons
description: Defines canned rejection reasons for suggested edits.
tags:
- review
- rejection
- reasons
- suggested edits
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:58+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/review_rejection_reasons.md
  title: 'Compiler input: references/review_rejection_reasons.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: d79a4662f0862411331bba9c6cda232208708cda446f5417f69f32dc086e58d9
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table defines canned rejection reasons for suggested edits.

## Schema
- `Id` (INTEGER) - Unique identifier for the rejection reason.
- `Name` (STRING) - The name of the rejection reason.
- `Description` (STRING) - A detailed description of the rejection reason.
- `PostTypeId` (INTEGER) - The type of post the reason applies to (e.g., `5` for Wiki, `6` for Excerpt). Otherwise, it is null. Links to the [Post Type IDs reference](post_type_ids.md).

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
