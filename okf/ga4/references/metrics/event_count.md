---
type: Reference
resource: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
title: Event Count
description: Total number of events.
tags:
- metric
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:50:07+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/event_count.md
  title: 'Compiler input: references/metrics/event_count.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: d43468dd0f48e00a7682b49c15141d2050df88a6f357f67a87b7340ea0509c31
semantic:
  knowledge_type: reference
  entities:
  - name: Event Count
    type: metric
  - name: event
    type: event-type
  relations:
  - type: calculates
    target: Total number of events
    evidence: COUNT(*)
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

Total number of events.

```sql
COUNT(*)
```

# Citations
- https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
