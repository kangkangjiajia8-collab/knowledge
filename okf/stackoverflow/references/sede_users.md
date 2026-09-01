---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: SEDE Users
description: Details the structure of the internal SEDE users metadata table.
tags:
- SEDE
- internal
- users
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:36:32+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/sede_users.md
  title: 'Compiler input: references/sede_users.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: d391137df5de6a8584e6288dff73a330e02e94b75bb95da036411ee76e16de44
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This internal table in the Stack Exchange Data Explorer (SEDE) provides user-specific metadata across sites.

## Schema
- `account_id` (INTEGER) - The global Stack Exchange Network account ID.
- `site_id` (INTEGER) - The ID of the site the user is associated with. Links to `references/sede_sites.md`.
- `user_id` (INTEGER) - The local user ID on that specific site. Links to the `users` table.
- `reputation` (INTEGER) - The user\'s reputation on that specific site.
- `question_count` (INTEGER) - The number of questions asked by the user on that specific site.
- `answer_count` (INTEGER) - The number of answers provided by the user on that specific site.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
