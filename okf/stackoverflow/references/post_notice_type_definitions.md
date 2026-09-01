---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Post Notice Type Definitions
description: Defines the structure and properties of different types of post notices.
tags:
- notices
- types
- definitions
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:42+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/post_notice_type_definitions.md
  title: 'Compiler input: references/post_notice_type_definitions.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: eba7f0a868a71fcc5efc75e87a89854eba4741d0a0d3c30aa34e1db29ff75fcd
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table defines the structure and properties of different types of post notices that can be applied to posts.

## Schema
- `Id` (INTEGER) - Unique identifier for the post notice type.
- `ClassId` (INTEGER) - The class of the notice. See the [Post Notice Class IDs reference](post_notice_class_ids.md) for possible values.
- `Name` (STRING) - The name of the post notice type.
- `Body` (STRING) - Contains the default notice text. Nullable.
- `IsHidden` (BOOLEAN) - Indicates if the notice type is hidden.
- `Predefined` (BOOLEAN) - Indicates if the notice type is predefined.
- `PostNoticeDurationId` (INTEGER) - The duration identifier for the notice. See the [Post Notice Duration IDs reference](post_notice_duration_ids.md) for possible values.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
