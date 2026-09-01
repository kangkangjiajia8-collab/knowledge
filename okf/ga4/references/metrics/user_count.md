---
type: Reference
resource: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
title: User Count
description: Total number of unique users.
tags:
- metric
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:50:09+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/user_count.md
  title: 'Compiler input: references/metrics/user_count.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: c432de60e95341d79317c1d3d49b150c9096346baf55ffc081acf7dc8f0fcebe
semantic:
  knowledge_type: definition
  entities:
  - name: User Count
    type: metric
  - name: user_pseudo_id
    type: entity
  relations:
  - type: calculates
    target: User Count
    evidence: COUNT(DISTINCT user_pseudo_id)
  - type: references
    target: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
    evidence: Citations
  confidence: 1.0
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

Total number of unique users.

```sql
COUNT(DISTINCT user_pseudo_id)
```

# Citations
- https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
