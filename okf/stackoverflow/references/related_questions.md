---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Related Questions
description: Provides a mapping between questions and other related questions based on various factors.
tags:
- questions
- related
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:15+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/related_questions.md
  title: 'Compiler input: references/related_questions.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 0a2e8d99a81699a775524fd57a45f01038ca0fca8dce0ced908197bd07decffe
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table provides a mapping between questions and other related questions, based on factors like content similarity or user behavior.

## Schema
- `PostId` (INTEGER) - The ID of the primary question. Links to the `posts_questions` table.
- `RelatedPostId` (INTEGER) - The ID of a related question. Links to the `posts_questions` table.
- `Position` (INTEGER) - The position or ranking of the related question.
- `Score` (INTEGER) - A score indicating the relevance or strength of the relationship.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
