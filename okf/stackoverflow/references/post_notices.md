---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Post Notices
description: Stores information about notices applied to posts, including their type, dates, and associated
  users.
tags:
- notices
- posts
- moderation
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:29+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/post_notices.md
  title: 'Compiler input: references/post_notices.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 5c46cdefd2b92e46bd74c5696783a2a174b157c3fb10383832ef38de9d34e896
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table stores information about notices applied to posts, such as "Citation needed" or "Duplicate".

## Schema
- `Id` (INTEGER) - Unique identifier for the post notice.
- `PostId` (INTEGER) - The ID of the post the notice is applied to. Links to the `posts` tables (`posts_questions` or `posts_answers`).
- `PostNoticeTypeId` (INTEGER) - The type of post notice. See the [Post Notice Types reference](post_notice_types.md) for possible values.
- `CreationDate` (TIMESTAMP) - The date and time the notice was created.
- `DeletionDate` (TIMESTAMP) - The date and time the notice was deleted. Nullable.
- `ExpiryDate` (TIMESTAMP) - The date and time the notice is set to expire. Nullable.
- `Body` (STRING) - When present, contains the custom text shown with the notice. Nullable.
- `OwnerUserId` (INTEGER) - The ID of the user who created the notice. Links to the `users` table. Nullable.
- `DeletionUserId` (INTEGER) - The ID of the user who deleted the notice. Links to the `users` table. Nullable.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
