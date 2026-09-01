---
type: Reference
resource: https://developers.google.com/analytics/bigquery/basic-queries
title: Join Google Analytics Events to Google Ads Clicks
description: Join Google Analytics event data with Google Ads click data.
tags:
- join
- Google Ads
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:51:46+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/references/joins/events___ads_clickstats.md
  title: 'Compiler input: references/joins/events___ads_clickstats.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: ef9a4ec6964eeffc7603eafe7a337fa23a97873a8fbc18664668392bac0f2d19
semantic:
  knowledge_type: join-specification
  entities:
  - name: Google Analytics event data
    type: dataset
  - name: Google Ads click data
    type: dataset
  - name: gclid
    type: entity
  - name: GA_EVENTS.collected_traffic_source.gclid
    type: entity
  - name: ADS_CLICKS.gclid
    type: entity
  relations:
  - type: joins
    target: Google Ads click data
    evidence: Join Google Analytics event data with Google Ads click data
  - type: joins
    target: ADS_CLICKS.gclid
    evidence: GA_EVENTS.collected_traffic_source.gclid = ADS_CLICKS.gclid
  - type: part_of
    target: GA_EVENTS.collected_traffic_source.gclid
    evidence: GA_EVENTS.collected_traffic_source.gclid
  - type: references
    target: https://developers.google.com/analytics/bigquery/basic-queries
    evidence: Citations
  confidence: 0.98
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

Join Google Analytics event data with Google Ads click data.

```sql
GA_EVENTS.collected_traffic_source.gclid = ADS_CLICKS.gclid
```

# Citations
- https://developers.google.com/analytics/bigquery/basic-queries
