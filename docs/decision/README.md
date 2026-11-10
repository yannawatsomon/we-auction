# Decision log — we-auction

Read this before any work. Update the relevant topic file **before** changing code that
contradicts it. Template: [`_template.md`](_template.md). Skill: `record-decision`.

Statuses: `Open` → `Decided` → `Superseded`. Only a human collaborator moves a topic to Decided.

## Index

| Topic | File | Status | Summary |
|---|---|---|---|
| Repo & collaboration | [repo-and-collaboration.md](repo-and-collaboration.md) | Decided | Public GitHub repo, PR-based flow on protected `main` |
| AI agent hub | [ai-agent-hub.md](ai-agent-hub.md) | Decided | `AGENTS.md` entry point + `ai/` hub + `.claude/skills/`; tool files only point back |
| Scope | — | Open | What we-auction must do; blocks everything below |
| Stack | [stack.md](stack.md) | Open | Language/framework/hosting undecided; do not add one yet |
| License | — | Open | Public repo with no license = all rights reserved; pick one deliberately |

## Key decisions at a glance

- Repo: `github.com/yannawatsomon/we-auction`, public (2026-11-10).
- Agent-agnostic: any agent reads `AGENTS.md`; Claude Code is the confirmed primary tool.
- Files in English; Thai terms go in `ai/context/glossary.md`.

## Open questions

- What is we-auction exactly (scope, users, deadline)? → fill `ai/context/project.md`.
- Which stack? → `stack.md`.
- Which license? (public repo)
- Who are the collaborators / who reviews? (CODEOWNERS not set yet)
