---
type: Domain Topic
title: Users and reputation
description: Users, badges, votes, and reputation signals.
tags:
- stackoverflow-public-dataset
- topic
generated:
  by: knowledge-compiler/qwen3.6-27b-fable-fusion
  at: '2026-09-01T03:25:39.037265Z'
sources:
- id: concept-1
  resource: ../datasets/stackoverflow.md
  title: Stack Overflow Public Dataset
- id: concept-2
  resource: ../references/badge_classes.md
  title: Badge Classes
- id: concept-3
  resource: ../references/close_as_off_topic_reason_types.md
  title: Close As Off-Topic Reason Types
- id: concept-4
  resource: ../references/creative_commons_by_sa_4_0_license.md
  title: Creative Commons Attribution-ShareAlike 4.0 International License
- id: concept-5
  resource: ../references/flag_types.md
  title: Flag Types
- id: concept-6
  resource: ../references/pending_flags.md
  title: Pending Flags
- id: concept-7
  resource: ../references/post_feedback.md
  title: Post Feedback
- id: concept-8
  resource: ../references/post_history_type_ids.md
  title: Post History Type IDs
- id: concept-9
  resource: ../references/post_notices.md
  title: Post Notices
- id: concept-10
  resource: ../references/related_questions.md
  title: Related Questions
- id: concept-11
  resource: ../references/review_task_results.md
  title: Review Task Results
- id: concept-12
  resource: ../references/review_task_types.md
  title: Review Task Types
- id: concept-13
  resource: ../references/review_tasks.md
  title: Review Tasks
- id: concept-14
  resource: ../references/sede_users.md
  title: SEDE Users
- id: concept-15
  resource: ../references/suggested_edit_votes.md
  title: Suggested Edit Votes
- id: concept-16
  resource: ../references/suggested_edits.md
  title: Suggested Edits
- id: concept-17
  resource: ../references/tag_synonyms.md
  title: Tag Synonyms
- id: concept-18
  resource: ../references/vote_types.md
  title: Vote Types
- id: concept-19
  resource: ../tables/badges.md
  title: Badges
- id: concept-20
  resource: ../tables/comments.md
  title: Comments
- id: concept-21
  resource: ../tables/post_history.md
  title: Post History
- id: concept-22
  resource: ../tables/posts_answers.md
  title: Posts Answers
- id: concept-23
  resource: ../tables/posts_moderator_nomination.md
  title: Posts Moderator Nomination
- id: concept-24
  resource: ../tables/posts_orphaned_tag_wiki.md
  title: Orphaned Tag Wiki Posts
- id: concept-25
  resource: ../tables/posts_privilege_wiki.md
  title: Posts Privilege Wiki
- id: concept-26
  resource: ../tables/posts_questions.md
  title: Stack Overflow Questions
- id: concept-27
  resource: ../tables/posts_tag_wiki.md
  title: Posts Tag Wiki
- id: concept-28
  resource: ../tables/posts_tag_wiki_excerpt.md
  title: Posts Tag Wiki Excerpt
- id: concept-29
  resource: ../tables/posts_wiki_placeholder.md
  title: Posts Wiki Placeholder
- id: concept-30
  resource: ../tables/stackoverflow_posts.md
  title: Stack Overflow Posts (Legacy)
- id: concept-31
  resource: ../tables/users.md
  title: Users
- id: concept-32
  resource: ../tables/votes.md
  title: Votes
status: draft
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L1
---

# Users and reputation

Users, badges, votes, and reputation signals.

# Concepts

* [Stack Overflow Public Dataset](../datasets/stackoverflow.md) — The Stack Overflow public dataset contains a variety of tables related to Stack Overflow user activity, posts, and tags. This dataset is no longer actively updated.
* [Badge Classes](../references/badge_classes.md) — Enumerated classes for badges awarded on Stack Exchange sites.
* [Close As Off-Topic Reason Types](../references/close_as_off_topic_reason_types.md) — Defines the types and guidance for reasons why a post might be closed as off-topic.
* [Creative Commons Attribution-ShareAlike 4.0 International License](../references/creative_commons_by_sa_4_0_license.md) — Details the attribution requirements for content licensed under CC BY-SA 4.0 for the Stack Exchange network.
* [Flag Types](../references/flag_types.md) — Enumerated types for flags related to post moderation on Stack Exchange.
* [Pending Flags](../references/pending_flags.md) — Stores information about pending flags and votes related to post moderation.
* [Post Feedback](../references/post_feedback.md) — Collects up and down votes from anonymous visitors and unregistered users.
* [Post History Type IDs](../references/post_history_type_ids.md) — Enumerated types for post history events on Stack Exchange.
* [Post Notices](../references/post_notices.md) — Stores information about notices applied to posts, including their type, dates, and associated users.
* [Related Questions](../references/related_questions.md) — Provides a mapping between questions and other related questions based on various factors.
* [Review Task Results](../references/review_task_results.md) — Stores the outcomes and details of completed review tasks.
* [Review Task Types](../references/review_task_types.md) — Enumerated types for various review tasks on Stack Exchange.
* [Review Tasks](../references/review_tasks.md) — Stores information about moderation review tasks on Stack Exchange, such as suggested edits or close votes.
* [SEDE Users](../references/sede_users.md) — Details the structure of the internal SEDE users metadata table.
* [Suggested Edit Votes](../references/suggested_edit_votes.md) — Records votes cast on suggested edits, indicating approval or rejection.
* [Suggested Edits](../references/suggested_edits.md) — Stores information about suggested edits to posts that are awaiting review.
* [Tag Synonyms](../references/tag_synonyms.md) — Stores relationships between synonymous tags on Stack Exchange.
* [Vote Types](../references/vote_types.md) — Enumerated types for votes on posts and other entities across Stack Exchange sites.
* [Badges](../tables/badges.md) — This table contains information about badges awarded to users on the Stack Overflow platform, including details about the badge name, class, and whether it is tag-based.
* [Comments](../tables/comments.md) — This table contains comments made by users on posts within the Stack Overflow platform, including details about the comment text, score, and author, along with licensing information.
* [Post History](../tables/post_history.md) — Tracks the revision history of posts on Stack Overflow, including details about event types, associated users, and content changes.
* [Posts Answers](../tables/posts_answers.md) — Contains information about answers to questions posted on Stack Overflow, including detailed schema fields, their descriptions, and licensing information.
* [Posts Moderator Nomination](../tables/posts_moderator_nomination.md) — Contains posts where users nominate themselves or others to become moderators on the Stack Overflow platform.
* [Orphaned Tag Wiki Posts](../tables/posts_orphaned_tag_wiki.md) — This table contains Tag Wiki posts that are no longer associated with an active tag on Stack Overflow.
* [Posts Privilege Wiki](../tables/posts_privilege_wiki.md) — This table contains posts describing various privileges on Stack Overflow, such as editing questions and retagging.
* [Stack Overflow Questions](../tables/posts_questions.md) — This table contains information about all question posts on Stack Overflow, including detailed schema fields, their descriptions, and licensing information.
* [Posts Tag Wiki](../tables/posts_tag_wiki.md) — Contains detailed wiki descriptions for tags on Stack Overflow.
* [Posts Tag Wiki Excerpt](../tables/posts_tag_wiki_excerpt.md) — Contains excerpts from tag wikis on Stack Overflow.
* [Posts Wiki Placeholder](../tables/posts_wiki_placeholder.md) — Placeholder table for Stack Overflow wiki posts, containing community-maintained help and information.
* [Stack Overflow Posts (Legacy)](../tables/stackoverflow_posts.md) — A legacy table containing all posts from Stack Overflow. This table is deprecated; use `posts_answers`, `posts_questions`, or other `posts_*` tables instead.
* [Users](../tables/users.md) — This table contains information about users registered on Stack Overflow, including detailed profile information, activity metrics, and network-wide identifiers.
* [Votes](../tables/votes.md) — This table contains information about votes cast on posts within the Stack Overflow platform, including the vote type, associated post and user, and bounty details.
