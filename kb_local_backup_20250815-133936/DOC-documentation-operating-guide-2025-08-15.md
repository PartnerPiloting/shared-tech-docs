---
title: Documentation Operating Guide
area: docs
tags: [kb, tasks, process]
owner: repo-owner
status: draft
lastUpdated: 2025-08-15
sources:
  - conversation: docs-system-planning-2025-08-15
---

# Documentation Operating Guide

Purpose
- Capture non-code context: interfaces (Airtable automations, LinkedHelper, cron), decisions, experiments, and tradeoffs.
- Make it easy to reconstruct what, how, and why later.

Where things live
- Docs live in kb/ (planned shared submodule).
- Tasks live in tasks/ (shared submodule).

Naming
- Docs: DOC-<topic-kebab>[−optional-date].md (keep ≤120 chars). Example: DOC-airtable-automations-triggers-and-failover-2025-08-15.md
- Tasks: TASK-<short-kebab>-YYYY-MM-DD.md.

Frontmatter (required)
- title, area, tags, owner, status (draft/active/deprecated), lastUpdated, sources (chat/PR links).

Workflow
- Capture: write draft in dev after significant chats/investigations.
- Summarize: add Executive summary and Key links at the top.
- Consolidate: when stable, move into kb/ and add to kb/INDEX.md.
- Retire: mark overlapping drafts deprecated with pointer to canonical doc.

Examiner (agent) rules
- Suggest-only by default: generate summaries, cross-links, and a move-plan; no auto-moves.
- Check links, detect duplicates, flag secrets/PII, staleness, long filenames/paths.
- Propose area/tags and related-doc links; surface open questions.

Quality checks (non-blocking)
- Warn when frontmatter is missing required fields or doc lives outside kb/.
- Weekly doc health report: stale docs, broken links, duplicates, orphans.

Security/redaction
- No secrets/PII in docs. Use secret managers; reference env var names only.

Submodule practices
- Edit/push in kb repo; then bump the submodule pointer in the parent repo.

Index and tags
- Maintain kb/INDEX.md by area (Airtable, LinkedHelper, Cron, etc.).
- Prefer short, reusable tags.

Change log
- 2025-08-15: Initial draft created from conversation.
