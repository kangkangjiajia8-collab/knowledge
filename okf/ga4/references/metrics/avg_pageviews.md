---
type: Reference
resource: https://developers.google.com/analytics/bigquery/basic-queries
title: Average Pageviews
description: The average number of pageviews per user.
tags:
- metric
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:51:43+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/avg_pageviews.md
  title: 'Compiler input: references/metrics/avg_pageviews.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 3975100cd6835d813b0173491922d901494277042396316e5230950a63c3e56d
semantic:
  knowledge_type: calculation
  entities:
  - name: Average Pageviews
    type: metric
  - name: page_view_count
    type: metric
  - name: page_view
    type: event-type
  - name: event_name
    type: entity
  relations:
  - type: is_a
    target: metric
    evidence: The average number of pageviews per user
  - type: calculates
    target: Average Pageviews
    evidence: SUM(page_view_count) / COUNT(*)
  - type: calculates
    target: page_view_count
    evidence: page_view_count is COUNTIF(event_name = 'page_view') per user
  - type: applies_to
    target: page_view
    evidence: event_name = 'page_view'
  - type: references
    target: https://developers.google.com/analytics/bigquery/basic-queries
    evidence: Citations
  confidence: 0.97
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

The average number of pageviews per user.

```sql
SUM(page_view_count) / COUNT(*)
-- where page_view_count is COUNTIF(event_name = 'page_view') per user
```

# Citations
- https://developers.google.com/analytics/bigquery/basic-queries
