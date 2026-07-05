# n8n Workflow Spec - Contributor Intake

## Purpose
Process new contributor applications with AI assistance while keeping final decisions with the founder.

## Trigger
Supabase database webhook:

- Table: contributor_applications
- Event: INSERT
- Method: POST
- Target: n8n webhook URL

## Nodes

1. Webhook - receives application payload.
2. Validate payload - confirms email, role and message exist.
3. OpenRouter HTTP Request - Founder AI review.
4. GitHub - create issue in this repository.
5. Email/notification - notify founder.

## AI prompt

Use agents/founder.md plus application data.

Return:

- applicant summary
- role fit
- useful skills
- concerns
- recommended next step
- draft reply

## Safety

Never decide automatically. Never promise compensation, formal status or partnership. Use founder review.
