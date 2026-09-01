---
type: BigQuery Dataset
resource: https://bigquery.googleapis.com/v2/projects/bigquery-public-data/datasets/ga4_obfuscated_sample_ecommerce
title: BigQuery sample dataset for Google Analytics ecommerce web implementation
description: A sample of obfuscated Google Analytics BigQuery event export data for three months from
  the Google Merchandise Store is available as a public dataset in BigQuery.
tags:
- ecommerce
- web analytics
- Google Analytics
- BigQuery
- public dataset
- ga4-bigquery-analytics
timestamp: '2026-05-28T22:49:59+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.289957Z'
sources:
- id: compiler-input
  resource: source://ga4/datasets/ga4_obfuscated_sample_ecommerce.md
  title: 'Compiler input: datasets/ga4_obfuscated_sample_ecommerce.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 48fea8257cb689bcddf1292436e051c0011360fe186f222a90a69b9240d01672
semantic:
  knowledge_type: reference
  entities:
  - name: ga4_obfuscated_sample_ecommerce
    type: dataset
  - name: Google Merchandise Store
    type: entity
  - name: BigQuery
    type: resource
  - name: BigQuery API
    type: resource
  - name: BigQuery Sandbox mode
    type: resource
  - name: Free usage tier
    type: resource
  - name: Google Analytics Demo Account
    type: entity
  - name: event_count
    type: metric
  - name: user_count
    type: metric
  - name: day_count
    type: metric
  - name: user_pseudo_id
    type: entity
  - name: event_date
    type: entity
  - name: bigquery-public-data.ga4_obfuscated_sample_ecommerce.events_*
    type: table
  relations:
  - type: is_a
    target: BigQuery Dataset
    evidence: BigQuery sample dataset for Google Analytics ecommerce web implementation
  - type: part_of
    target: bigquery-public-data
    evidence: FROM `bigquery-public-data.ga4_obfuscated_sample_ecommerce.events_*`
  - type: applies_to
    target: Google Merchandise Store
    evidence: from the Google Merchandise Store
  - type: requires
    target: BigQuery API
    evidence: you need access to a Google Cloud project with the BigQuery API enabled
  - type: requires
    target: Google Cloud project
    evidence: you need access to a Google Cloud project
  - type: applies_to
    target: BigQuery Sandbox mode
    evidence: You can use BigQuery Sandbox mode or the Free usage tier for exploration
  - type: applies_to
    target: Free usage tier
    evidence: You can use BigQuery Sandbox mode or the Free usage tier for exploration
  - type: calculates
    target: event_count
    evidence: COUNT(*) AS event_count
  - type: calculates
    target: user_count
    evidence: COUNT(DISTINCT user_pseudo_id) AS user_count
  - type: calculates
    target: day_count
    evidence: COUNT(DISTINCT event_date) AS day_count
  - type: references
    target: https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
    evidence: Citations
  confidence: 0.95
  extracted_by: knowledge-compiler/qwen3.6-27b-fable-fusion
  extracted_at: '2026-09-01T03:24:31.249422Z'
domain: ga4-bigquery-analytics
domain_profile_version: 1.0.0
wiki_layer: L2
---

# Overview
The `ga4_obfuscated_sample_ecommerce` dataset contains obfuscated Google Analytics BigQuery event export data for three months (November 2020 to January 2021) from the Google Merchandise Store. This public dataset is available in BigQuery and emulates a real-world dataset.

# Pre-requisites
To work with this dataset, you need access to a Google Cloud project with the BigQuery API enabled. You can use BigQuery Sandbox mode or the Free usage tier for exploration and sample queries.

# Limitations
The dataset contains obfuscated data with placeholder values like `<Other>`, `NULL`, and `''`. Due to obfuscation, the internal consistency of the dataset might be somewhat limited. It cannot be compared to the Google Analytics Demo Account.

# Using the dataset
You can access the `ga4_obfuscated_sample_ecommerce` dataset via the BigQuery UI in the Cloud Console.

## Sample Query
The following query shows the number of unique events, users, and days in the dataset:

```sql
SELECT
  COUNT(*) AS event_count,
  COUNT(DISTINCT user_pseudo_id) AS user_count,
  COUNT(DISTINCT event_date) AS day_count
FROM `bigquery-public-data.ga4_obfuscated_sample_ecommerce.events_*`
```

# Citations
- https://developers.google.com/analytics/bigquery/web-ecommerce-demo-dataset
