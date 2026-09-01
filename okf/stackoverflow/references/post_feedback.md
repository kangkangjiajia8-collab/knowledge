---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Post Feedback
description: Collects up and down votes from anonymous visitors and unregistered users.
tags:
- feedback
- votes
- anonymous
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:33:30+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/post_feedback.md
  title: 'Compiler input: references/post_feedback.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 90ee7e7bbc44a4f4c0bb9330644a0729f8b4cef8b0fad6518f9ad692caab72c3
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table collects up and down votes from anonymous visitors and/or unregistered users.

## Schema
- `Id` (INTEGER) - Unique identifier for the post feedback entry.
- `PostId` (INTEGER) - The ID of the post (`posts_questions` or `posts_answers`) the feedback is for.
- `IsAnonymous` (BOOLEAN) - Indicates if the feedback was given anonymously.
- `VoteTypeId` (INTEGER) - The type of vote. Specifically `2` for UpMod and `3` for DownMod in this table. See the [Vote Types reference](vote_types.md) for a comprehensive list.
- `CreationDate` (TIMESTAMP) - The date and time the feedback was recorded.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
