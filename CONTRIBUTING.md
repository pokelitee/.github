# Contributing to PokéLitee

Use a short-lived feature or fix branch and open a pull request into the repository's default branch. Keep each change focused and describe the resulting behavior and why it is needed. Source changes must go through a pull request and the repository's required CI checks, including changes by administrators. Resolve review conversations before merging. Squash merges are recommended for focused changes; use the merge methods enabled by the repository. Merged branches are deleted automatically where configured.

Follow the project's README and any local contribution or agent instructions for setup, architecture, formatting, and tests. Run the relevant checks before opening a pull request, and state anything that could not be verified. Keep package lockfiles or pinned requirements synchronized with dependency changes. Dependency and GitHub Actions updates are reviewed weekly in the maintained application and dataset repositories; upgrades that must happen together should remain grouped.

Generated `data` branches belong to the publishing workflows. Do not merge them into source branches or edit published datasets by hand. Their history must remain protected against deletion and force pushes. Keep immutable dataset tags intact. A project may publish validated files after partial scraper failures or require a complete snapshot; preserve its documented policy.

For changes to a data contract, document the schema and migration, add representative regression fixtures, and verify generation against the current upstream source before publishing. Passing offline tests alone does not establish compatibility with a changing external API.

Report bugs and propose features through issues in the affected repository. For a vulnerability, use the repository's private vulnerability-reporting mechanism when enabled instead of posting sensitive details publicly.
