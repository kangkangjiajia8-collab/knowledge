---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Close As Off-Topic Reason Types
description: Defines the types and guidance for reasons why a post might be closed as off-topic.
tags:
- close reasons
- off-topic
- enum
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:32:53+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/close_as_off_topic_reason_types.md
  title: 'Compiler input: references/close_as_off_topic_reason_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 482bc4cc87a5fc784525e69345139aee52d3293e33ee8d2cf79f98ce29a27742
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table defines the enumerated reasons and associated guidance for why a post might be closed as off-topic.

## Schema
- `Id` (INTEGER) - Unique identifier for the reason type.
- `IsUniversal` (BOOLEAN) - Indicates if the reason is universally applicable.
- `InputTitle` (STRING) - The title shown for input.
- `MarkdownInputGuidance` (STRING) - Markdown guidance shown while flagging/voting.
- `MarkdownPostOwnerGuidance` (STRING) - Markdown guidance shown to the original poster when closed.
- `MarkdownPublicGuidance` (STRING) - Markdown guidance shown to privileged users when closed.
- `MarkdownConcensusDescription` (STRING) - Markdown description shown above the public or post owner guidance. Nullable.
- `CreationDate` (TIMESTAMP) - The date and time the reason type was created.
- `CreationModeratorId` (INTEGER) - The ID of the moderator who created the reason type. Links to the `users` table.
- `ApprovalDate` (TIMESTAMP) - The date and time the reason type was approved.
- `ApprovalModeratorId` (INTEGER) - The ID of the moderator who approved the reason type.
- `DeactivationDate` (TIMESTAMP) - The date and time the reason type was deactivated.
- `DeactivationModeratorId` (INTEGER) - The ID of the moderator who deactivated the reason type. Links to the `users` table.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
