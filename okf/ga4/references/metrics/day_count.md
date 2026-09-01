---
type: Reference
resource: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
title: Day Count
description: Total number of unique days.
tags:
- metric
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:50:10+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/day_count.md
  title: 'Compiler input: references/metrics/day_count.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 4f7ec06ccd2f7673d08f67f9243f5e36ee6a9a9ec70ebe006fff580dce81e2ca
semantic:
  knowledge_type: reference
  entities:
  - name: Day Count
    type: metric
  - name: event_date
    type: entity
  - name: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
    type: resource
  relations:
  - type: calculates
    target: Day Count
    evidence: COUNT(DISTINCT event_date)
  - type: depends_on
    target: event_date
    evidence: COUNT(DISTINCT event_date)
  - type: references
    target: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
    evidence: 'Citations: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset'
  confidence: 0.95
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

Total number of unique days.

```sql
COUNT(DISTINCT event_date)
```

# Citations
- https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
