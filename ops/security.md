# Security & Access Map

## Credentials on Hand
- **OpenAI API Key**: Preloaded in environment (OPENAI_API_KEY). Used for GPT-5.1 Codex calls. Stored via runtime environment variables (not committed).
- **GitHub Personal Access Token**: Stored at `.secrets/github_pat`. Scope: repo + workflows (assumed). Used for repo creation, pushes, and Pages deployment.
- **Gmail Account**: `pppcemail@gmail.com` (password stored in `.secrets/gmail_credentials`). Currently unused; available for future verifications.
- **Discord Bot**: Token stored at `.secrets/discord_bot_token`; client ID + secret stored at `.secrets/discord_client`. Used for pushing live updates into Discord.

## Handling Guidelines
- Secrets live under `.secrets/` (ignored by git). Never echo values to console or commit them.
- All scripts should read secrets from files or environment variables, not inline strings.
- If additional credentials are provided, log their location here and update `.gitignore` if needed.

## Monitoring & Alerts
- API spend tracked via `ops/ledger.csv`.
- Daily review to ensure actual spend ≤ $5.
- Any anomalous usage or credential change gets recorded in this file and surfaced in status updates.
