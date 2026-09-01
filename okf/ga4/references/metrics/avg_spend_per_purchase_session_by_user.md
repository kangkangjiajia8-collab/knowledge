---
type: Reference
resource: https://developers.google.com/analytics/bigquery/advanced-queries
title: Average Spend Per Purchase Session By User
description: The average amount of money spent per purchase session for each individual user.
tags:
- metric
- ecommerce
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:52:29+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/avg_spend_per_purchase_session_by_user.md
  title: 'Compiler input: references/metrics/avg_spend_per_purchase_session_by_user.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 9923dda220be5e76eb36ff672d1babd77e003b27f67c633555eac5393ed73cc6
semantic:
  knowledge_type: reference
  entities:
  - name: Average Spend Per Purchase Session By User
    type: metric
  - name: purchase
    type: event-type
  - name: user_pseudo_id
    type: entity
  - name: ga_session_id
    type: entity
  - name: total_session_spend
    type: concept
  - name: https://developers.google.com/analytics/bigquery/advanced-queries
    type: resource
  relations:
  - type: calculates
    target: Average Spend Per Purchase Session By User
    evidence: AVG(total_session_spend)
  - type: applies_to
    target: purchase
    evidence: event_name = 'purchase' events
  - type: depends_on
    target: user_pseudo_id
    evidence: grouped by user_pseudo_id
  - type: depends_on
    target: ga_session_id
    evidence: grouped by ... ga_session_id
  - type: references
    target: https://developers.google.com/analytics/bigquery/advanced-queries
    evidence: 'Citations: https://developers.google.com/analytics/bigquery/advanced-queries'
  confidence: 0.95
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

The average amount of money spent per purchase session for each individual user.

```sql
AVG(total_session_spend)
-- where total_session_spend is SUM(COALESCE(...)) for event_name = 'purchase' events within a session, grouped by user_pseudo_id and ga_session_id
```

# Citations
- https://developers.google.com/analytics/bigquery/advanced-queries
