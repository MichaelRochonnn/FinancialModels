![FinancialModels hero banner](./assets/hero-banner.svg)

# Documentation

This folder is the documentation hub for the FinancialModels repository.

It now supports two entry modes:

- direct browsing on GitHub,
- a lightweight MkDocs site backed by the same `docs/` content.

## Visual overview

![Usage flow](./assets/usage-flow.svg)

![Model routing](./assets/model-routing.svg)

These diagrams show the two key layers of the project:

- how a rough user request moves through quickstart into the full suite,
- how the router maps a request into one of the 12 supported modeling workflows.

## Start here

If you are new to the project, read these in order:

1. [Installation guide](./installation.md)
2. [Chinese user guide](./zh-user-guide.md)
3. [Sample output guide](./sample-output.md)

## What each document covers

- [installation.md](./installation.md)
  How to copy the skills into your local Codex setup, verify installation, and update them later.
- [zh-user-guide.md](./zh-user-guide.md)
  A Chinese-language walkthrough of when to use each skill, how to invoke them, and how the intake flow works.
- [sample-output.md](./sample-output.md)
  Example prompts, expected intake interactions, and the shape of a polished deliverable.

## Hosted docs note

The repository now includes `mkdocs.yml` and a GitHub Pages workflow. To publish a hosted docs site, make sure GitHub Pages is configured to deploy from Actions in the repository settings.

## Related repository docs

- [MkDocs home page](./index.md)
- [Top-level README](../README.md)
- [Examples directory](../examples)
- [Contributing guide](../CONTRIBUTING.md)
- [Security policy](../SECURITY.md)
- [Changelog](../CHANGELOG.md)

## Intended audience

This documentation is primarily useful for:

- Codex users installing the skills locally,
- contributors improving model routing or templates,
- finance-focused users who want to understand how to get the best results from the skills.
