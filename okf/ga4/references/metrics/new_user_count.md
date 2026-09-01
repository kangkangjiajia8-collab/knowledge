---
type: Reference
resource: https://developers.google.com/analytics/bigquery/basic-queries
title: New User Count
description: The number of unique users who triggered a first_visit or first_open event.
tags:
- metric
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:51:38+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/new_user_count.md
  title: 'Compiler input: references/metrics/new_user_count.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 191a1a2dde27559d62612021297610d2a7f28348d98051b3b2c364af7513ade8
semantic:
  knowledge_type: reference
  entities:
  - name: New User Count
    type: metric
  - name: first_visit
    type: event-type
  - name: first_open
    type: event-type
  - name: user_pseudo_id
    type: entity
  - name: is_new_user
    type: metric
  relations:
  - type: calculates
    target: The number of unique users who triggered a first_visit or first_open event
    evidence: SUM(is_new_user)
  - type: depends_on
    target: first_visit
    evidence: event_name IN ('first_visit', 'first_open')
  - type: depends_on
    target: first_open
    evidence: event_name IN ('first_visit', 'first_open')
  - type: depends_on
    target: user_pseudo_id
    evidence: grouped by user_pseudo_id
  - type: references
    target: https://developers.google.com/analytics/bigquery/basic-queries
    evidence: Citations
  confidence: 1.0
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

The number of unique users who triggered a `first_visit` or `first_open` event.

```sql
SUM(is_new_user)
-- where is_new_user is MAX(IF(event_name IN ('first_visit', 'first_open'), 1, 0)) grouped by user_pseudo_id
```

# Citations
- https://developers.google.com/analytics/bigquery/basic-queries
