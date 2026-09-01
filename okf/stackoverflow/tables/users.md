---
type: BigQuery Table
resource: https://bigquery.googleapis.com/v2/projects/bigquery-public-data/datasets/stackoverflow/tables/users
title: Users
description: This table contains information about users registered on Stack Overflow, including detailed
  profile information, activity metrics, and network-wide identifiers.
tags:
- Stack Overflow
- users
- profiles
- community
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:32:24+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/tables/users.md
  title: 'Compiler input: tables/users.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: 1a09bd829b1a8240fbc12737c977942358eb69ff7ad13b6c623c2ba0d547a39f
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This table, `users`, from the [stackoverflow](../datasets/stackoverflow.md) dataset, stores profiles of registered users on the Stack Overflow platform. Each row represents a unique user, identified by their `id`. The table includes details such as display name, creation date, last access date, reputation, and vote counts. It provides insights into the activity and characteristics of the Stack Overflow community members.

# Schema

*   `id` (INTEGER) - Unique identifier for the user.
*   `display_name` (STRING) - The publicly visible name of the user.
*   `about_me` (STRING) - User-provided free-form text about themselves. Nullable.
*   `age` (INTEGER) - User-provided age. Nullable.
*   `account_id` (INTEGER) - User\'s Stack Exchange Network profile ID; NULL if the user has hidden this community in their profile. Nullable.
*   `creation_date` (TIMESTAMP) - Timestamp when the user account was created.
*   `email_hash` (STRING) - Gravatar email hash, now always NULL and will not appear as an attribute in the data dump XML. Nullable.
*   `last_access_date` (TIMESTAMP) - Datetime user last loaded a page; updated every 30 minutes at most.
*   `location` (STRING) - User-provided geographical location. Nullable.
*   `reputation` (INTEGER) - The user\'s reputation score.
*   `up_votes` (INTEGER) - How many upvotes the user has cast.
*   `down_votes` (INTEGER) - Total number of downvotes received by the user.
*   `views` (INTEGER) - Number of times the user\'s profile has been viewed.
*   `profile_image_url` (STRING) - URL of the user\'s profile picture. Nullable.
*   `website_url` (STRING) - URL of the user\'s personal website. Nullable.

# Common query patterns

1.  Find the top 10 users by reputation:
    ```sql
    SELECT
      id,
      display_name,
      reputation
    FROM
      `bigquery-public-data.stackoverflow.users`
    ORDER BY
      reputation DESC
    LIMIT 10
    ```
2.  Count users created per year:
    ```sql
    SELECT
      EXTRACT(YEAR FROM creation_date) AS creation_year,
      COUNT(id) AS user_count
    FROM
      `bigquery-public-data.stackoverflow.users`
    GROUP BY
      creation_year
    ORDER BY
      creation_year
    ```
3.  Find users with a high number of upvotes given:
    ```sql
    SELECT
      display_name,
      up_votes
    FROM
      `bigquery-public-data.stackoverflow.users`
    WHERE
      up_votes > 1000
    ORDER BY
      up_votes DESC
    LIMIT 5
    ```

# Citations

[1] [Stack Overflow Users Table](https://bigquery.googleapis.com/v2/projects/bigquery-public-data/datasets/stackoverflow/tables/users)
[2] [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
