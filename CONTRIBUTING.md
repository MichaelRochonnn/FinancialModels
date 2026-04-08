# Contributing

Thank you for contributing to FinancialModels.

This repository packages Codex skills for financial-modeling workflows. The goal is to keep the skills easy to install, easy to understand, and reliable in real usage. Good contributions improve clarity, routing accuracy, input collection, examples, and final deliverable quality.

## What kinds of contributions are welcome?

We welcome contributions that:

- improve the quality of the existing skills,
- expand examples or copy/paste templates,
- refine model routing or intake logic,
- improve the Chinese-language output structure,
- tighten documentation and release hygiene,
- add new references that make the skills easier to maintain.

If a proposed change materially alters behavior or scope, please explain the intent clearly in the PR so reviewers can understand whether the change is additive, corrective, or opinionated.

## Repository layout

The current repository is organized around skill packages:

```text
financial-modeling-suite/
financial-modeling-quickstart/
examples/
README.md
LICENSE
CONTRIBUTING.md
```

### Skill package expectations

Each skill folder should remain self-contained and readable.

Typical structure:

```text
skill-name/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    └── supporting-files.md
```

## Contribution principles

### 1. Keep behavior legible

A new contributor should be able to understand what a skill does by reading:

- `SKILL.md`
- the referenced support files,
- the examples folder,
- the top-level README.

Avoid hidden behavior changes that are not reflected in docs or examples.

### 2. Keep routing practical

These skills are most useful when they do three things well:

- identify the correct financial model,
- ask only for the missing data,
- produce outputs that feel structured and decision-ready.

Contributions should strengthen at least one of those outcomes.

### 3. Do not silently invent critical finance inputs

If a workflow depends on time-sensitive or missing inputs such as:

- WACC assumptions,
- peer multiples,
- precedent transaction data,
- market rates,
- share counts,
- net debt,

then the skill should either ask for them or explicitly label assumptions.

### 4. Preserve the quickstart experience

The `financial-modeling-quickstart` skill is meant to catch short, conversational prompts. Changes should not make it feel overly formal or force unnecessary upfront data entry.

## Editing guidelines

### Skill metadata

- Keep `SKILL.md` frontmatter minimal.
- Use only the fields required by Codex for local skills.
- Keep names stable unless there is a strong reason to rename a skill.

### Prompt and workflow design

- Prefer concise, action-oriented instructions.
- Keep intake checklists specific to the model being requested.
- Ask only for missing inputs instead of dumping a full questionnaire every time.
- When assumptions are allowed, instruct the skill to surface them clearly.
- Keep outputs polished, but avoid unnecessary verbosity.

### Chinese finance deliverables

The suite intentionally supports more polished Chinese-language outputs. When editing templates:

- keep the tone professional and decision-oriented,
- prefer structures that resemble banker / PE materials,
- separate assumptions, outputs, and risks clearly,
- make tables and sections easy to scan.

### Documentation

If you change behavior, also update the relevant docs:

- `README.md`
- `examples/`
- release-oriented guidance such as `examples/release-checklist.md`

## Validation before submitting

Before opening a PR, please do the following when possible:

- validate each changed skill locally,
- test at least one explicit `$skill-name` invocation,
- test at least one natural-language invocation,
- confirm any new examples still match actual behavior,
- confirm referenced files and paths are still valid.

If your change affects output format, include a short before/after note in the PR description.

## Pull request checklist

A strong PR usually includes:

- a short summary of what changed,
- why the change was needed,
- which skill(s) were affected,
- whether behavior changed or only docs changed,
- any validation you ran,
- any follow-up work that remains out of scope.

If the PR adds or changes a workflow, include at least one example prompt.

## Scope guidance

Good first contributions:

- improve README clarity,
- add invocation examples,
- add input templates,
- tighten vague instructions,
- improve release hygiene.

Higher-impact contributions:

- improve model selection logic,
- improve missing-input handling,
- make deliverables more decision-ready,
- add high-quality reference material.

## Licensing

By contributing to this repository, you agree that your contributions will be released under the repository's MIT License.

## Questions

If a change is large or changes the expected user experience, open an issue or provide extra context in the PR so the review can focus on the right tradeoffs.
