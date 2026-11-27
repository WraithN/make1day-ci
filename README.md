# make1day-ci

Public CI shell. **No product source code lives in this repository.**

- The workflow checks out a **private** repository with a **read-only** deploy key.
- The heavy matrix runs **manually** (`workflow_dispatch`).
- `cron.yml` is the only scheduled workflow: it POSTs the production
  `/api/cron/webhook-retry` endpoint every 15 minutes. Set the `CRON_SECRET`
  secret (same value as the Vercel env var) and optionally the `SITE_URL`
  repository variable.
- No artifacts are uploaded. Actions logs are public by design.
- Forking this repository gives you nothing but the workflow file.

Do not add source code, secrets in plain text, or `pull_request` triggers here.
