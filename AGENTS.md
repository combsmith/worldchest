# AGENTS.md

This repository follows the organization-wide development standards defined in
[`combsmith/.github/AGENTS.md`](https://github.com/combsmith/.github/blob/main/AGENTS.md).

Read that file before making changes that touch CI, agent configuration, repo
settings, or labels. Repo-specific deviations, if any, are documented below.

## Project overview

WorldChest backs up, syncs, restores and versions Minecraft Bedrock worlds for
young players on phones and tablets; parents are the buyer. The brief, the n=1
proof (232 worlds migrated S22 → S24 by hand) and the open legal and platform
questions are in
[combsmith/incubator discussion #5](https://github.com/combsmith/incubator/discussions/5).
No application code exists yet and no stack has been chosen (`STACK=none` at
bootstrap). Candidate shape from the brief: a mobile app (Android first, Bedrock
share-sheet + Shizuku power mode), a desktop companion for migrations, and a
cloud backend for storage and versioning.

## Local Development Commands

- Install: none yet (no application code)
- Dev run: n/a
- Test: none yet; CI runs the org baseline (`build-and-test` shell lint, `Secret scan (gitleaks)`, `coverage`) until a stack lands
- Lint: n/a
- Typecheck: n/a

When the stack is chosen, replace this section and update `ci.yml`,
`.github/dependabot.yml`, `copilot-setup-steps.yml` and
`.github/copilot-instructions.md` per the org `AGENTS.md`
"Creating a new repository" step 3 (the template's `BOOTSTRAP.md` steps 2–4 and 7).

## Required Environment Variables

- None.

## Testing

- No test suite yet. First code must arrive with tests (org TDD rule); the
  `coverage` CI job stays green until tests exist and enforces from then on.

## Rules specific to this repository

- **Naming (Minecraft Usage Guidelines).** The brand is WorldChest. "Minecraft"
  appears only as a secondary title ("backup for Minecraft worlds"), never in the
  brand, domain, handles or package names. Every listing and site carries the
  NOT AN OFFICIAL MINECRAFT PRODUCT disclaimer.
- **Minors' data.** Storing kids' worlds is COPPA / GDPR-K territory: design
  parent-consent flows and data handling before any backend stores user content.
- **Frameworks are vendored, not installed.** BMAD and other agent frameworks
  come from `combsmith/.github-private` or `software-factory` as `git subtree`;
  never run `npx bmad-method install` here.
- **Stubs are org-managed.** The `.github/workflows/*.yml` thin-caller stubs,
  `CODEOWNERS`, `CLAUDE.md`, `.gitleaks.toml` and the `.gitignore` secrets
  baseline are synced by org automation; do not hand-edit them.
