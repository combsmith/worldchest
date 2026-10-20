# Copilot Instructions — worldchest

## About

WorldChest is automatic backup, sync, restore and versioning for Minecraft Bedrock
worlds on kids' phones and tablets (parents are the buyer). This repo is pre-code:
the brief is [combsmith/incubator discussion #5](https://github.com/combsmith/incubator/discussions/5).

## Tech Stack

- **Runtime:** not chosen yet. Candidates from the brief: Android app (Kotlin,
  share-sheet + Shizuku), desktop companion, cloud backend for storage/versioning.
- **CI / config:** org baseline GitHub Actions stubs; `ci.yml` runs shell lint, gitleaks and a coverage job that is green until tests exist.
- **Testing / Linting:** to be set with the stack.

## Project Structure

No application code yet. `.github/` holds the org-standard workflow stubs and this file.

## Local Dev Commands

- Install: none yet
- Test: none yet
- Lint: none yet

## Required Environment Variables

- None.

## Testing Framework

- None yet. First code lands with tests; the `coverage` job enforces from then on.

## Repo-Specific Overrides

- Use "Minecraft" only as a secondary title; never in the brand, domain, handles or
  package names. Keep the NOT AN OFFICIAL MINECRAFT PRODUCT disclaimer on any
  user-facing surface.
- Treat any stored world data as a minor's data (COPPA / GDPR-K).
- Frameworks (BMAD) are vendored from `combsmith/.github-private` or
  `software-factory`; never `npx bmad-method install`.

## Org Standards

See [combsmith/.github — AGENTS.md](https://github.com/combsmith/.github/blob/main/AGENTS.md)
for org-wide development standards.

_No language-specific instruction files are deployed to `.github/instructions/` yet
(`STACK=none`); add them with the stack per the Copilot Instructions Standard._
