---
type: Reference
resource: https://developers.google.com/analytics/bigquery/advanced-queries
title: Overall Average Spend Per Purchase Session
description: The overall average amount spent across all unique purchase sessions.
tags:
- metric
- ecommerce
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:52:32+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/overall_avg_spend_per_purchase_session.md
  title: 'Compiler input: references/metrics/overall_avg_spend_per_purchase_session.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 0027e9101dc0ea4e7eef22e120e4cce6f1eed3afd09201bd80d705d1cf068427
semantic:
  knowledge_type: reference
  entities:
  - name: Overall Average Spend Per Purchase Session
    type: metric
  - name: purchase
    type: event-type
  - name: user_pseudo_id
    type: entity
  - name: ga_session_id
    type: entity
  - name: total_session_spend
    type: metric
  relations:
  - type: calculates
    target: The overall average amount spent across all unique purchase sessions
    evidence: AVG(total_session_spend)
  - type: depends_on
    target: purchase
    evidence: event_name = 'purchase'
  - type: depends_on
    target: user_pseudo_id
    evidence: grouped by user_pseudo_id and ga_session_id
  - type: depends_on
    target: ga_session_id
    evidence: grouped by user_pseudo_id and ga_session_id
  - type: references
    target: https://developers.google.com/analytics/bigquery/advanced-queries
    evidence: Citations
  confidence: 1.0
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

The overall average amount spent across all unique purchase sessions.

```sql
AVG(total_session_spend)
-- where total_session_spend is SUM(COALESCE(...)) for event_name = 'purchase' events within a session, grouped by user_pseudo_id and ga_session_id
```

# Citations
- https://developers.google.com/analytics/bigquery/advanced-queries
