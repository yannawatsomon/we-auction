# Contributing

This repo is **public** — never commit secrets, tokens, `.env` files or personal data.

## Flow

1. Pick or open an issue.
2. Branch from latest `main`: `feat/<name>`, `fix/<name>` or `docs/<name>`.
3. Make small, focused commits (imperative subject, e.g. `Add bid validation`).
4. Check `docs/decision/README.md`. If your change touches a Decided topic, update or
   supersede the decision doc in the same PR.
5. Open a PR using the template. At least one approval is required; squash-merge.

## Working with AI agents

- Agents start at [`AGENTS.md`](AGENTS.md). Do not create per-tool rule files with duplicate
  content — add rules to `AGENTS.md`.
- Review agent-written changes as carefully as human ones. You are the author of record.
- Put new shared knowledge in `ai/` (see `ai/README.md`), not only in chat or a PR comment.

## Commit email

Use your GitHub `noreply` address (GitHub → Settings → Emails → Keep my email private), since
history is public.
