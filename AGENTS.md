# AGENTS.md — entry point for every AI coding agent

This file is vendor-neutral. Claude Code, Codex, Cursor, Copilot and any other agent should
read it first. Tool-specific files (`CLAUDE.md`, `.github/copilot-instructions.md`,
`.cursor/rules/`) only point back here — **do not duplicate rules in them.**

## Before any work

1. Read [`docs/decision/README.md`](docs/decision/README.md) — what is decided, what is open.
2. Read [`ai/context/project.md`](ai/context/project.md) — what we-auction is and its constraints.
3. Skim [`ai/README.md`](ai/README.md) — map of the shared AI hub.
4. If your change contradicts a **Decided** entry, update/supersede the decision doc *first*,
   in the same PR. Never silently diverge.

## The shared AI hub (single source of truth)

| What | Where | Purpose |
|---|---|---|
| Decisions | `docs/decision/` | What was decided and why (ADR-style, one file per topic) |
| Context | `ai/context/` | Project background, domain, glossary, constraints |
| Knowledge | `ai/knowledge/` | Reusable how-it-works notes, gotchas, references |
| Playbooks | `ai/playbooks/` | Step-by-step procedures (e.g. how to add a feature, how to release) |
| Skills | `.claude/skills/<name>/SKILL.md` | Reusable agent skills (open SKILL.md format; any agent may read them) |

Agents that can't auto-load skills: open the relevant `SKILL.md` and follow it manually.

## Working rules

- Branch from `main`; never push to `main` directly. Open a PR (see `CONTRIBUTING.md`).
- Small, focused PRs. One concern per PR.
- Never commit secrets, tokens, `.env` files or personal data — **this repo is public.**
- Stack is currently **undecided** (see `docs/decision/stack.md`). Do not introduce a
  framework, language or build tool without a Decided entry.
- When you learn something non-obvious (a gotcha, a convention, a reason), write it down in
  `ai/knowledge/` or `docs/decision/` instead of leaving it in chat.
- Language: files are written in English; Thai is welcome in discussion and in `ai/context/glossary.md`.
