---
type: Reference
resource: https://developers.google.com/analytics/bigquery/basic-queries
title: Average Transactions Per Purchaser
description: The average number of transactions made by purchasers.
tags:
- metric
- ecommerce
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:51:41+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/metrics/avg_transactions_per_purchaser.md
  title: 'Compiler input: references/metrics/avg_transactions_per_purchaser.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 07eb73afed37e75322c455308d65b4019412b78eb31d758ce626da50e4a89a60
semantic:
  knowledge_type: reference
  entities:
  - name: Average Transactions Per Purchaser
    type: metric
  - name: purchase
    type: event-type
  - name: in_app_purchase
    type: event-type
  - name: user_pseudo_id
    type: entity
  - name: https://developers.google.com/analytics/bigquery/basic-queries
    type: resource
  relations:
  - type: calculates
    target: Average Transactions Per Purchaser
    evidence: COUNT(*) / COUNT(DISTINCT user_pseudo_id)
  - type: applies_to
    target: purchase
    evidence: event_name IN ('in_app_purchase', 'purchase')
  - type: applies_to
    target: in_app_purchase
    evidence: event_name IN ('in_app_purchase', 'purchase')
  - type: depends_on
    target: user_pseudo_id
    evidence: COUNT(DISTINCT user_pseudo_id)
  - type: references
    target: https://developers.google.com/analytics/bigquery/basic-queries
    evidence: 'Citations: https://developers.google.com/analytics/bigquery/basic-queries'
  confidence: 0.95
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

The average number of transactions made by purchasers.

```sql
COUNT(*) / COUNT(DISTINCT user_pseudo_id)
-- for events where event_name IN ('in_app_purchase', 'purchase')
```

# Citations
- https://developers.google.com/analytics/bigquery/basic-queries
