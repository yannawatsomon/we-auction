# Repo & collaboration

**Status:** Decided · **Effort:** S · **Deadline risk:** Low — foundation only

## Context

Several collaborators (humans and AI agents) will work in one repo. They need a predictable
flow so work doesn't collide and nothing sensitive leaks.

## Decisions

- **GitHub repo is public, under the owner's personal account.** What:
  `yannawatsomon/we-auction`, public. Why: user's choice. Trade-off: everything committed is
  world-readable forever — no secrets, personal data or private client info. Alternative
  rejected: private repo / organization (not chosen; can migrate later). Source: user
  confirmation, 2026-11-10.
- **Collaborators are invited individually (Write role).** What: Settings → Collaborators.
  Why: personal accounts have no teams. Trade-off: manual access management. Alternative
  rejected: organization with teams (overkill for now). Source: derived from the above, 2026-11-10.
- **PR-based flow; `main` is protected.** What: branch `feat/*`, `fix/*`, `docs/*`; PR with
  review; squash merge. Why: keeps `main` clean with several people. Trade-off: slower than
  pushing directly. Alternative rejected: trunk-based direct pushes. Source: proposed by
  Claude, pending user confirmation of branch protection settings.
- **Commit email privacy.** Because the repo is public, each collaborator's commit email is
  visible; use the GitHub `noreply` address (Settings → Emails → "Keep my email private").

## Rules / examples

Branch protection to enable on `main` (Settings → Branches → Add rule): require a pull request
before merging, require 1 approval, dismiss stale approvals, block force pushes.

## Open questions

- Who reviews? Add `CODEOWNERS` once collaborators are known.
- CI: none yet (stack undecided).
