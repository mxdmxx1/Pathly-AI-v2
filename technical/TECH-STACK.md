# Proposed Technical Stack

These are candidate technologies, not confirmed production choices.

## Frontend
- Next.js and React.
- TypeScript.
- Responsive styling and reusable components.

## Authentication and database
- Supabase Auth.
- Supabase Postgres.
- Row-level security for student-owned records.

## AI
- OpenAI API through trusted server-side routes.
- Retrieval from curated, versioned learning resources.
- Usage limits, safety controls and cost monitoring.

## Hosting
- Vercel is a candidate web host.
- Supabase is a candidate managed database/auth provider.

## Payments
Stripe may be considered later, subject to demand validation, provider eligibility and appropriate legal arrangements.

## Security
- Never commit API keys, tokens or passwords.
- Keep secrets in managed environment variables.
- Never expose privileged database keys in browser code.
- Authenticate and authorise every server request.
- Apply least privilege and test policies using separate accounts.
- Keep dependencies updated.

Revisit the stack if implementation constraints, cost or maintainability favour a simpler choice.
