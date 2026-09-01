---
type: Reference
resource: https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede
title: Vote Types
description: Enumerated types for votes on posts and other entities across Stack Exchange sites.
tags:
- votes
- enum
- moderation
- schema
- data dump
- stackoverflow-public-dataset
timestamp: '2026-05-28T23:33:26+00:00'
status: stable
generated:
  by: knowledge-compiler/0.2.0
  at: '2026-09-01T03:27:39.899078Z'
sources:
- id: compiler-input
  resource: source://stackoverflow/references/vote_types.md
  title: 'Compiler input: references/vote_types.md'
  last_modified: '2026-07-20T03:27:52Z'
  sha256: dab09d8cf8e9b72520995f90dd2b85bd42c63fe7a53eb7f9ab8bf99e0d82e50a
domain: stackoverflow-public-dataset
domain_profile_version: 1.0.0
wiki_layer: L2
---

This document defines the enumerated types for various votes that can occur on posts and other entities across Stack Exchange sites.

- `-1`: InformModerator
- `0`: UndoMod
- `1`: AcceptedByOriginator
- `2`: UpMod (Upvote)
- `3`: DownMod (Downvote)
- `4`: Offensive
- `5`: Favorite (Bookmark) - feature removed after October 2022, replaced by Saves.
- `6`: Close - Close votes are only stored in the `PostHistory` table after 2013-06-25.
- `7`: Reopen
- `8`: BountyStart
- `9`: BountyClose
- `10`: Deletion
- `11`: Undeletion
- `12`: Spam
- `15`: ModeratorReview - a moderator looking at a flagged post.
- `16`: ApproveEditSuggestion
- `17`: Reaction1 (Teams: celebrate)
- `18`: Helpful
- `19`: ThankYou
- `20`: WellWritten
- `21`: Follow
- `22`: Reaction2 (Teams: smile)
- `23`: Reaction3 (Teams: mind blown)
- `24`: Reaction4 (Teams: clap)
- `25`: Reaction5 (Teams: heart)
- `26`: Reaction6 (Teams: fire)
- `27`: Reaction7 (Teams: trophy)
- `28`: Reaction8 (Teams: wave)
- `29`: Outdated
- `30`: NotOutdated
- `31`: PreVote
- `32`: CollectiveDiscussionUpvote
- `33`: CollectiveDiscussionDownvote (no longer used)
- `35`: privateAiAnswerCorrect
- `36`: privateAiAnswerIncorrect
- `37`: privateAiAnswerPartiallyCorrect

# Citations
- [Database schema documentation for the public data dump and SEDE](https://meta.stackexchange.com/questions/2677/database-schema-documentation-for-the-public-data-dump-and-sede)
