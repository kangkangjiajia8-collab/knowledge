---
type: BigQuery Table
resource: https://bigquery.googleapis.com/v2/projects/bigquery-public-data/datasets/stackoverflow/tables/post_links
title: Post Links
description: Contains information about links between posts on Stack Overflow, including the type of link
  and the posts involved.
tags:
- stackoverflow
- posts
- links
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:34:10+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/tables/post_links.md
  title: 'Compiler input: tables/post_links.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: f2fd40527c75243eefa7f2af1a1bdc73430bdc48d800966aad62430d6473ec70
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

The `post_links` table in the [stackoverflow](../datasets/stackoverflow.md) dataset records relationships between posts on the Stack Overflow platform. Each row represents a single link between two posts, identifying the `post_id` and `related_post_id`. This table can be used to understand how discussions evolve, identify duplicate questions, or find related content across the platform. The `link_type_id` categorizes the nature of the relationship, such as "Linked" or "Duplicate".

# Schema

*   `id` (INTEGER) - Unique identifier for the post link (primary key).
*   `creation_date` (TIMESTAMP) - The timestamp when the link was created.
*   `link_type_id` (INTEGER) - The type of link. See the [Link Types reference](../references/link_types.md) for possible values.
*   `post_id` (INTEGER) - The ID of the source post. Links to the `id` in the `posts_questions` or `posts_answers` tables.
*   `related_post_id` (INTEGER) - The ID of the target/related post. Links to the `id` in the `posts_questions` or `posts_answers` tables.

# Common query patterns

```sql
SELECT
  pl.post_id,
  pl.related_post_id,
  pl.creation_date,
  pl.link_type_id
FROM
  `bigquery-public-data.stackoverflow.post_links` AS pl
WHERE
  pl.post_id = 12345
LIMIT 100;
```

```sql
SELECT
  link_type_id,
  COUNT(*) AS link_count
FROM
  `bigquery-public-data.stackoverflow.post_links`
GROUP BY
  link_type_id
ORDER BY
  link_count DESC;
```

# Citations

[1] [BigQuery Public Dataset: Stack Overflow Post Links](https://bigquery.googleapis.com/v2/projects/bigquery-public-data/datasets/stackoverflow/tables/post_links)
[2] [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
