---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Review Task Results
description: Stores the outcomes and details of completed review tasks.
tags:
- review
- tasks
- results
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:35:11+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/review_task_results.md
  title: 'Compiler input: references/review_task_results.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 283524815906fe74eaf51cc94032e33d49856e4b1a3856a053dfb5781d536604
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table stores the outcomes and details of completed review tasks, such as approvals, rejections, or edits.

## Schema
- `Id` (INTEGER) - Unique identifier for the review task result.
- `ReviewTaskId` (INTEGER) - The ID of the review task this result is for. Links to the `ReviewTasks` table.
- `ReviewTaskResultTypeId` (INTEGER) - The type of result. See the [Review Task Result Types reference](review_task_result_types.md) for possible values.
- `CreationDate` (TIMESTAMP) - The date when the result was recorded. Time data is purposefully removed to protect user privacy.
- `RejectionReasonId` (INTEGER) - The ID of the rejection reason, specifically for suggested edits. Links to the [Review Rejection Reasons reference](review_rejection_reasons.md). Nullable.
- `Comment` (STRING) - A comment associated with the review result. Nullable.

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
