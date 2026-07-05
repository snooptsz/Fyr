# n8n Workflow Spec - Feedback Triage

## Purpose
Turn user feedback and bug reports into clear GitHub issues.

## Trigger
Supabase database webhook:

- Table: feedback or reports
- Event: INSERT
- Method: POST

## Nodes

1. Webhook receives feedback.
2. Product AI classifies product relevance.
3. Builder AI classifies technical priority.
4. Security AI flags privacy/security relevance if present.
5. GitHub creates issue.
6. Founder notification.

## Classification

- Critical: blocks signup, login, posting, applications, or exposes sensitive data.
- High: breaks important functionality.
- Medium: visible bug with workaround.
- Low: copy, cosmetic, small improvement.

## Safety

Do not close reports automatically. Do not expose private user data in GitHub issues.
