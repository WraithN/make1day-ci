# make1day-ci

Public CI shell. **No product source code lives in this repository.**

- The workflow checks out a **private** repository with a **read-only** deploy key.
- It runs **manually** (`workflow_dispatch`) only.
- No artifacts are uploaded. Actions logs are public by design.
- Forking this repository gives you nothing but the workflow file.

Do not add source code, secrets in plain text, or `pull_request` triggers here.
