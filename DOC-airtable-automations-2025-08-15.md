# Airtable Automations — System Overview

Meta
- Audience: engineering + ops
- Owner: Platform
- Last updated: 2025-08-15

Purpose
- Document the Airtable Automations that power PB Scoring and post-processing.

Systems and data
- Bases: per-client bases + global config base
- Tables: Leads, Scoring Attributes, Post Scoring Attributes
- External: PB Webhook Server (Render), Vercel UI, LinkedHelper webhooks

High-level flow
1) LinkedHelper/External triggers create/update records in Airtable
2) Webhook Server processes and updates tables
3) Automations react to field changes (statuses, dates) and kick follow-ups

Automations catalog (skeleton)
- Name: <Automation Name>
  - Trigger: <When record matches conditions | When record updated>
  - Script/Action: <Script, Update record, Send webhook>
  - Inputs: <fields>
  - Outputs: <fields updated, webhooks>
  - Error handling: <retry, alerts>
  - Owner: <name/role>

Runbook
- Where to see runs: Airtable Automations run history per base
- Common failures: API rate limits, missing fields, permission issues
- Fixes: pause/resume, re-run, repair field configs

Change history
- 2025-08-15: Initial outline
