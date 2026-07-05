# z3r0 n8n workflows

This folder stores exported n8n workflow JSON files and workflow notes. Keep credentials in n8n, never in JSON exports or GitHub.

## Start with four workflows

1. `contributor-intake.json` — Supabase application event → AI classification → GitHub issue → founder notification.
2. `feedback-triage.json` — Supabase feedback/report event → classify → GitHub issue.
3. `website-health.json` — scheduled URL checks → notify founder if a critical route fails.
4. `marketing-drafts.json` — scheduled AI drafts → save for founder review; never auto-publish.

## Required credentials

- Supabase service role credential, stored only in n8n
- GitHub token with minimum repository/issue access
- OpenRouter or other AI provider API key
- Email credential, if email is enabled

## Safety model

Automated: health checks, summaries, classification, drafts, GitHub issue creation, low-risk welcome messages.

Approval required: public posts, outreach, user bans, deletions, permission changes, payments, ads, production database policy changes.

## Export discipline

After changing a workflow: n8n → Download → save the JSON here → commit to GitHub with a short description of what changed.
