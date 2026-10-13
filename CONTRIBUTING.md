# Contributing to PokéLitee

## Pull requests

Use a short-lived feature or fix branch and open a pull request into the repository's default branch. Keep each change focused and describe the resulting behavior and why it is needed. Source changes must go through a pull request and the repository's required CI checks, including changes by administrators. Resolve review conversations before merging. Squash merges are recommended for focused changes; use the merge methods enabled by the repository. Merged branches are deleted automatically where configured.

## Project documentation and checks

Start with the project's README Contributing section and `docs/development.md` for setup, architecture, formatting, and checks. PokéDB and Leak Duck also keep publishing and recovery instructions in `docs/operations.md`. Follow any local agent instructions. Run the relevant checks before opening a pull request, and state anything that could not be verified. Keep package lockfiles or pinned requirements synchronized with dependency changes. Dependency and GitHub Actions updates are reviewed weekly in the maintained application and dataset repositories; upgrades that must happen together should remain grouped.

## Generated data and compatibility

Generated `data` branches belong to the publishing workflows. Do not merge them into source branches or edit published datasets by hand. Their history must remain protected against deletion and force pushes. Keep immutable dataset tags intact. A project may publish validated files after partial scraper failures or require a complete snapshot; preserve its documented policy.

For changes to a data contract, document the schema and migration, add representative regression fixtures, and verify generation against the current upstream source before publishing. Passing offline tests alone does not establish compatibility with a changing external API.

## Issues and security

Report bugs and propose features through issues in the affected repository. For a vulnerability, use the repository's private vulnerability-reporting mechanism when enabled instead of posting sensitive details publicly.

## Maintaining documentation

Keep READMEs focused on purpose, live endpoints or apps, quick start, and documentation links. Put project-specific development and operations details in `docs/`; use the README's Contributing section to link them and this shared policy. A local `CONTRIBUTING.md` is unnecessary when those links cover the project. GitHub uses this organization-level file as the default contribution guide when a repository has none of its own.

Each topic should have one authoritative home. PokéDB's data contract lives in its repository; Leak Duck's API field reference and changelog live in `site/docs.json`; PoGo Calendar's user help lives in its app FAQ. Update links, package manifests, examples, and documentation checks when moving files. Verify commands against current scripts and workflows, and document relevant failure and recovery behavior.

## Shared community repository

The `pokelitee/.github` repository hosts this guide, the default `PULL_REQUEST_TEMPLATE.md`, and the organization profile in `profile/README.md`. Templates and guidance are inherited where a repository has no local override. Its `.github/rulesets/main.json` describes protection for this repository alone; it does not configure other repositories automatically.

This repository contains community documents rather than application code and currently has no CI workflow. Review Markdown links and content before merging its required PRs. Changes to shared guidance should remain applicable across projects; keep project commands and data contracts in the affected repository.
